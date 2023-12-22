# Raspberry Pi Zero W
## Serial Console
_ on linux _
Mount the `/dev/sdc1` partition on `/mnt` 
This is the partition that gets mounted at /boot/firmware.
Edit the config.txt file and add `enable_uart=1` to enable UART1 on GPIO13 (hdr pin8) and GPIO14 (hdr pin10) with GND being hdr pin6.
**early console - Pi Zero ONLY**
Edit cmdline.txt and add `earlycon=uart8250,mmio32,0x20215040` to the beginning of the line with console.

This should be all that is needed to see the serial console messages.

I use `screen /dev/ttyUSB0 115200` to access the serial console.
