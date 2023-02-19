# GBE_Plus
GBE Plus is an enhancement to the GBE Pico Controller.  There are two versions, the GBE_Plus Pico by itself, and the GBE-Plus Pico with a Raspberry Pi.  THe Raspberry Pi adds additional sensors and a camera,
and interaccts with the Pico as an IOT sensor.
## Modes
### "AeroGarden" Mode
In this mode the Pico is stand-alone.  Settings default to 14 hours photo-period, and the light turns on based on the time the unit is plugged in.
There is no automatic logging of sensor data, but it is possible to wifi connect to the Pico to see and copy the sensor data.  This is the default start-up mode.
It is also possible to set the clock and light settings via wifi, wiile in stand-alone mode.
### IOT Mode
In this mode the Pico acts similar an IOT (internet of things) device.  The Pico is connected to a Raspberry Pi via wifi and acts as a remote sensor.
The Raspberry Pi communicataes with the Pico, setting the clock and pulling sensor data.  The Raspberry Pi logs the Pico sensors (and the Raspberry Pi sensors) to MongoDB where the data can be pulled and displayed in charts.
## Indicator Light meaning
* Fast Flashing Red: External power, lights not set up.
* Slow Flashing Green: Aerogarden mode, timer running and lights controlled
* Slow Flashing Orange: Lost power
* Slow Flashing White: IOT mode, lights set up
* Slow Flashing Blue: USB power, files accessible via file browser
## Set-Up
When powered on, the Pico acts as a wifi 'Hot Spot', it is a wifi access point that any computer or phone may log onto.  When logged in, the Home page should automatically show up on the browser.
From the Home page, there are pages to set the time, lights-on time and photo-period.  There is also a page for seeing the current sensor data.
## Issues to be resolved
1) Setting unique IP name for the Pico.  Is this by custom setting the code (in the Pico and the Raspberry Pi), or can this be done via a screen?
