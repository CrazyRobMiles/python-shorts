# Putting a Micro Python device into firmware download mode

If you don't have access to the BOOTSEL button on your Micro Python device you can put it into firmware download mode (where it appears as a storage device into which you can drop a .uf2 image) by typing the following commands at the command line (or running them in a program)
```Python
import machine
machine.bootloader()
```
[home](/README.md)