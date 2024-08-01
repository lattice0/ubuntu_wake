# ubuntu_wake

# on /etc/rc.local, put:

#!/bin/bash 

echo enabled > /sys/bus/usb/devices/usb3/power/wakeup

# but pay attention to the usb, check at lsusb I guess

# Disable autosuspend of bluetooth (https://askubuntu.com/a/1482242)

Change the `/etc/default/grub` file and add the following line `GRUB_CMDLINE_LINUX="usbcore.autosuspend=-1"` then `sudo update-grub`

