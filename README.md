esp8266-wifi-setup
======

ESP8266 Wifi setup using SoftAP, Captive Portal and EEPROM.  

1. booting and read Wifi config from EEPROM.
2. if Wifi config is not found, starting SoftAP at SSID "ESP8266_SETUP".
3. connect this Access point with your devices. (ex. iPhone, Android...)
4. Wifi Settings page will automatically open by Captive Portal.
5. select the SSID, enter the password.
6. writing SSID and password to EEPROM, then reboot ESP8266 automatically.
7. booting with STA(client) mode and get IP address from DHCP, then start web server.
8. now you can connect from within the same LAN.

日本語の解説は[ブログ](http://eleclog.quitsq.com/2015/08/esp8266-wifi-setup.html)を参照してください。

## Wiring

Boot from flash memory:

* GPIO 0 - Pulled HIGH with a 10k resistor
* GPIO 2 - Pulled HIGH with a 10k resistor
* GPIO 15 - Pulled LOW with a 10k resistor

![schematic](https://raw.githubusercontent.com/9SQ/esp8266-wifi-setup/master/schematic.png)

If GPIO 0 pin is pulled low during power-up it will start firmware flashing mode.

See also [official documents](https://github.com/espressif/esptool/wiki/ESP8266-Boot-Mode-Selection).

## Demo
### mobile
![sample](http://3.bp.blogspot.com/-ETIrnJynYj8/VdzTZQfJqLI/AAAAAAAATPU/_qUS0v57Bk0/esp8266-wifi-setup.gif)

### serial monitor
![sample_serial](http://2.bp.blogspot.com/-OOwLd6lHLTY/VdzWCOpQFUI/AAAAAAAATPg/9M1z1Lm3iWQ/s600/esp8266-wifi-setup_serial.png)

## Requirements

* [Arduino core for ESP8266 WiFi chip](https://github.com/esp8266/Arduino)