# ubuntu_wake

Instructions to wake ubuntu from suspend using only bluetooth and/or USB. TODO: confirm these steps work on a fresh installation.

## on /etc/rc.local, put: (https://jolahde.kapsi.fi/2018/02/05/enabling-usb-keyboard-and-mouse-to-wake-up-ubuntu-from-suspension/)

```bash
#!/bin/bash 

echo enabled > /sys/bus/usb/devices/usb3/power/wakeup
```

but pay attention to the usb3, check at lsusb I guess

## Disable autosuspend of bluetooth (https://askubuntu.com/a/1482242)

Change the `/etc/default/grub` file and add the following line 

`GRUB_CMDLINE_LINUX="usbcore.autosuspend=-1"` 

then `sudo update-grub`

