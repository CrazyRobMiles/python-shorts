# Using CircuitPython’s Two USB Serial Ports

Making a CircuitPython program talk to a usb serial device is quite easy to do:

```python
import usb_cdc

# Send a line of text to the host
usb_cdc.data.write(b"Hello!\n")

# Wait for a line of text from the host
while True:
    if usb_cdc.data.connected:
        try:
            line = usb_cdc.data.readline()
            if line:
                print("Received:", line.decode("utf-8").strip())
        except Exception as e:
            print("Error reading:", e)

```

Howwever, when using CircuitPython on boards like the Raspberry Pi Pico, it exposes **two USB serial ports** over USB:

- `usb_cdc.console` → used for the REPL (interactive shell)
- `usb_cdc.data` → intended for raw programmatic communication

When you use a browser that supports Web Serial (like Chrome or Edge), it might show both ports as separate choices. It's easy to accidentally connect to the **`console`** port instead of the **`data`** port. Your CircuitPython code ends up listening on `usb_cdc.data`, but the browser is sending to `usb_cdc.console`.

There are two ways you can fix this:
- Try both ports while connecting  
- Or disable the REPL/console port in production using:

```python
# boot.py
import usb_cdc
usb_cdc.disable(console=True)
```
Note that if you disable the console port you will not be able to interact with the device using tools such as Thonny. You will have to erase the EEPROM in the PICO and the re-flash it to get back control of the device. 

[home](/README.md)