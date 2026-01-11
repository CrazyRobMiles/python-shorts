# Turning off the Circuit Python storage device

When you connect a CircuitPython powered device to a desktop PC the device appears on the PC as a usb storage device onto which you can write your program and data files. If you don't want this to happen you can put a **boot.py** file on the device. When a CircuitPython powered device wakes up it runs the program in this file.
```python
import storage
import usb_cdc

# Disable USB mass storage
storage.disable_usb_drive()

# Keep USB REPL enabled to allow deploying files via REPL tools
usb_cdc.enable(console=True, data=True)

# Remount the filesystem so CircuitPython code can write to it
storage.remount("/", readonly=False)
```
This program disables the usb storage, ensures that we can still deploy files using the REPL commands and then remounts the Circuit Python file system so that it can be written to. 

**Note:** If you don't enable the REPL console you will have a slightly more secure device (it will not be possible to easily fiddle with the filestore via a serial connection). However, you will have to erase the current program in the device if you want to make any changes to it. 

[home](/README.md)