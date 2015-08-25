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
