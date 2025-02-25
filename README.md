# hubble
A switched USB hub. 

# Rev 1.0:
* USB 2.0 and USB 3.0
* Tested working (see errata)
* Toggle SW1 to select between host 1 and 2
* Debug connector provides I2C to use via TotalPhase Aardvark (or other debug device)
  * Also routed to USB-C SBU

## Errata
* USB5744 does not enter runtime, looks for I2C host. Remove R14 and R17, puts hub in headless mode.

# Rev 2.0:
* Enable USB5744 port power toggling
* Optionally drive mux sel via Raspberry Pi Pico W (useful for home automation)
* Add DisplayPort mux so I can stop using my monitor OSD (TBD which connectors I'll use)
