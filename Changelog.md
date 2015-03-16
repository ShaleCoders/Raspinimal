Raspbian Wheezy
---------------


_v1.0.3_ - **Testing Stages**

NTP added to keep Raspberry Pi's time updated. Default time servers will be used

* Added default package **NTP**
* Moved **wget,iputils-ping** to _minimal_ preset


_v1.0.2_ - **Released 24/12/13**

* Added default `/boot/config.txt` with no overclocking & 16mb gpu memory
* Updated server preset `rsyslog,wget,iputils-ping,cron,nano,vim-tiny,ca-certificates,man-db,less,iptables`
* Added Package **raspberrypi-bootloader** to be installed during install for latest kernel & modules
* Added Jessie mirrors to `/etc/apt/sources.list` for **apt-get dist-upgrade** [See Notes][1]
* Added watchdog module to `/etc/modules` - see [Install Watchdog][2]

_v1.0.1_ - **Released 26/10/2013**

* Changed hostname to pi.localhost
* Added firmware/contrib/rpi to `/etc/apt/sources.list`
* _minimal_ `kmod,fake-hwclock,ifupdown,net-tools,isc-dhcp-client,openntpd,openssh-server,dialog,locales,udev,apt-utils`
* _server_ `rsyslog,wget,iputils-ping,cron,nano,vim-tiny,ca-certificates,man-db,less`
* Added IPv6 module to `/etc/modules`

Wheezy to Jessie upgrade
------------------------

We'ved added mirrors for Jessie to latest version 1.0.2, however commented out so wheezy is still used by default. If you require _**raspi-config**_ please install `apt-get install raspi-config` before doing the following steps (You can't install after)

please make sure your `/etc/apt/sources.list` look like the following:

> deb http://mirrordirector.raspbian.org/raspbian/ jessie main contrib firmware rpi

> deb http://archive.raspbian.org/raspbian jessie main contrib firmware rpi

> deb-src http://archive.raspbian.org/raspbian jessie main contrib firmware rpi


If you only have the 3 above lines in your `/etc/apt/sources.list` then your ready to run `apt-get dist-upgrade` and wait for this complete. When completed you can go ahead and `reboot` and that's it. You are now running the latest Raspbian :-)

[1]: https://github.com/TheRPi/Raspinimal/blob/master/Changelog.md#wheezy-to-jessie-upgrade "See Notes"
[2]: http://harizanov.com/2013/08/putting-raspberry-pis-hardware-watchdog-to-work "Install Watchdog"
