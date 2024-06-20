# Assign fixed USB port names to your Raspberry Pi

<pre>
pi@RasPi4B32BIT:~ $ lsusb
Bus 002 Device 002: ID 056e:6a10 Elecom Co., Ltd ESD-EJ_R
Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 001 Device 006: ID 1a86:55d4 QinHeng Electronics USB Single Serial
Bus 001 Device 005: ID 1a86:55d4 QinHeng Electronics USB Single Serial
Bus 001 Device 004: ID 2341:0043 Arduino SA Uno R3 (CDC ACM)
Bus 001 Device 003: ID 1a40:0101 Terminus Technology Inc. Hub
Bus 001 Device 002: ID 2109:3431 VIA Labs, Inc. Hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
</pre>

<pre>
pi@RasPi4B32BIT:~ $ ls /dev/ttyACM?
/dev/ttyACM0  /dev/ttyACM1  /dev/ttyACM2
</pre>

<pre>
pi@RasPi4B32BIT:~ $ ls /dev/*USB*
ls: cannot access '/dev/*USB*': No such file or directory
</pre>

<pre>
 pi@RasPi4B32BIT:~ $ dmesg | grep ttyACM
[    6.408344] cdc_acm 1-1.3.2:1.0: ttyACM0: USB ACM device
[    6.429443] cdc_acm 1-1.3.3:1.0: ttyACM1: USB ACM device
[  175.772307] cdc_acm 1-1.3.4:1.0: ttyACM2: USB ACM device
</pre>

## References

Assign fixed USB port names to your Raspberry Pi • freva.com

https://www.freva.com/assign-fixed-usb-port-names-to-your-raspberry-pi/
