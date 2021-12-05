# custommac.service
ENC28J60 doesn't have a built in MAC address. This service sets the MAC
address from I2C MAC EEPROM before the interface is brought up.

## requirements
Requires aprsI2C repo and specifically `mac\_24AA02E48T` to be in `/usr/local/sbin`.

Requires `aprs.set_interface_mac_from_24AA02E48T` to be in `/usr/local/sbin` as well.

## install

Copy file
`sudo cp custommac.service /lib/systemd/system`

Make executeable
`sudo chmod 644 /lib/systemd/system/custommac.service`

Enable the service
`sudo systemctl enable custommac.service`

Rebooot. Make sure that `mac_24AA02E48T --read-mac` and ifconfig show the same MAC address

