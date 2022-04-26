---
layout: post
title: I don't like USB3 anymore
---
# I don't like USB3 anymore

I should love USB3, right? Well... I learned that it makes interferences with ZigBee[1], Bluetooth [2] and Logitech dongles [3]. So, I'm in the way of forgetting running mi raspberry-pi-4 in an external drive.

It looks like the speed running on USB3-HD will be higher than USB2 or micro-sd but as of today I have 37 ZigBee + 4 BLE configured devices that simply don't work anymore as expected.

I wonder if that why Home Assistant Yellow comes without USB3 ports [4]...

[1] https://www.youtube.com/watch?v=2PK3TrOGWNs

[2] My raspberry-pi 4 with Ubuntu is not able to see the Bluetooth adaptorwhen USB3-HD is used

[3] https://www.amazon.es/gp/product/B087C15X5B/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1
> 5)Si encuentra que sus dispositivos inalámbricos de 2.4 GHz están interferidos (como teclados y ratones inalámbricos, WLAN de 2.4 GHz), aleje los dispositivos del concentrador (o conecte los dispositivos en el puerto USB 2.0), porque la frecuencia de USB 3.0 es demasiado cercana a la frecuencia de wifi inalámbrico y 2.4Ghz, pueden interferir entre sí

[4] https://www.crowdsupply.com/nabu-casa/home-assistant-yellow
