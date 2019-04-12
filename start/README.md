# aprs.startmbusd

Starts [mbusd](https://github.com/3cky/mbusd). Uses sysfs interface to control
the RS-485 transmit. Uses `/dev/ttyS0` if exists, otherwise uses `/dev/ttyAMA0`. Runs mbusd in foreground. 

