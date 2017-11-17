# Rainforest Eagle Manager

Facillitates local LAN connection between the Rainforest Eagle and the SmartThings hub. 

## Notes
- Both the SmartThings hub and the Eagle must be on the same LAN
- Eagle will need a fixed IP address. Using a DHCP reservation seems to be the easiest way to go about this
- As far as I know you cannot have both cloud and local access to your Eagle, so you will need to turn off both remote management and security in the Eagle settings. 
- The MAC address listed on the bottom your Eagle device is slightly different (more zeros) that what will show up in network logs, when the smart app reqeusts the MAC please use what is printed on the bottom of the device.
- IP address must include the port. 80 is the default for the Eagle, ex. `192.168.0.17:80`
- The smart app will query the device every 30 seconds
- I don't know if this is a widespread issue but my Eagle consistently stops working every 24 hours and requires a reboot. You can ping the device successfully, but any API requests return an error.