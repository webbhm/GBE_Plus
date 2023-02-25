# GBE_Plus
GBE Plus is an enhancement to the GBE Pico Controller.  There are two versions, the GBE_Plus Pico by itself, and the GBE-Plus Pico with a Raspberry Pi.  THe Raspberry Pi adds additional sensors and a camera, and interaccts with the Pico as an IOT sensor.
Both versions have the same hardware and software.  The Pico starts up as a CaptivePortal, a wifi-hotspot that hosts a set of web pages.  The pages allow for setting the time (RTC), light settings and photoperiod, and changing the domain name.  A dashboard page gives all the current data.  A http request can retreive the data.</br>
Power can be supplied via the usb, or an external power feed (5v).  In the GBE, power will come off of the 20v power supply.  5v is needed to power the NeoPixel.  An external RTC (real time clock) avoids the need to reset the time after a power failure (but serves no other use).  It currently has the SHTC3 temperature and humidity sensor.
## Modes
### Stand-Alone Mode
There is no automatic logging of sensor data, but it is possible to wifi connect to the Pico to see and copy the sensor data (via the dashboard).
Not implemented at this time, but it This is the default start-up mode.

### IOT Mode
In this mode the Pico acts similar an IOT (internet of things) device.  The raspberry pi connects to the Pico via wifi and the Pico acts as a remote sensor.
The Raspberry Pi logs the Pico sensors (and the Raspberry Pi sensors) to MongoDB where the data can be pulled and displayed in charts.
## Indicator Light meaning
* Fast Flashing Red: External power, lights not set up.
* Slow Flashing White: IOT mode, lights set up
* Slow Flashing Blue: USB power, files accessible via file browser
## Set-Up
When powered on, the Pico acts as a wifi 'Hot Spot', it is a wifi access point that any computer or phone may log onto.  When logged in, the Home page should automatically show up on the browser.
From the Home page, there are pages to set the time, lights-on time and photo-period.  There is also a page for seeing the current sensor data.
## Issues to be resolved
1)
