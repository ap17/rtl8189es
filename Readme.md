rtl8189es driver v4.3.18.1_15373.20151005

origin : unknown

It is very old driver.
Currently (march 2020) used by me on Xunlong Orange OPi PC Plus 2E (H3) with Linux 5.6, Debian 10. Works good enough both in access point mode and in infrastructure mode.

This driver must be built in "in-tree" mode.

1.    put driver sources to ".../drivers/net/wireless/realtek/rtl8189es"
2.    into file ".../drivers/net/wireless/realtek/Kconfig" insert line:

source "/drivers/net/wireless/realtek/rtl8189es/Kconfig"

3.    into file ".../drivers/net/wireless/realtek/Makefile" insert line:

obj-$(CONFIG_RTL8189ES) += rtl8189es/

4.    do : make menuconfig -> device drivers-> network device support -> wireless LAN -> select 8189es
5.    do make.
