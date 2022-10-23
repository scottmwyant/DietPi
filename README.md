# DietPi

Taking some notes on how to use [DietPi](https://dietpi.com/).

## Using an automatic base installation at first boot (running an unattended base installation)

- Attempt to use wifi.  I have a static address reserved for this device, so I used the static IP config section as well.

Had to install `iptables` and `iptables-persistent`.  When installing `iptables-persistent`, it saves rules that exist at time of install to `/etc/iptables/rules.v4` and `/etc/iptables/rules.v6`.  Additional changes have to be saved to these files, using `iptables-save`.  The `iptables-persistent` package loads these config files at boot.
