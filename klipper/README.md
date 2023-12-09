# Klipper

## Installation

Setting up on bare metal debian is the way to go. https://github.com/th33xitus/kiauh makes this insanely easy.
There are Docker setups out there, but the Klipper stuff ain't really designed to be run that way so it requires
running privileged anyways, and has quite a lot of wonk.

I'm running everything from a Lenovo T420s (2C/4T, 8G RAM, 120G SSD) with Openbox and Chromium in kiosk mode. I first tried a Pi with a 7" inch touch screen, but it felt kinda laggy even with the fastest possible SD card (or even USB SSD).

## Setup

This was fairly staright forward. I found configuration samples for all my hardware via the official repos from Klipper (for factory E3v2), BTT (Pinout changes) and LDO (Orbiter extruder).

> The experience would probably have been completely different if I came into this completely fresh. After many months of digging into Marlin firmware, kinematics and 3D printing in general; doing everything from the bottom up like this felt quite natural.

Then it was just a matter of combining these into a singular `printer.cfg` file in the order above. Then running through the standard checklist:

* Test heating and thermistors (40C)
  * `M104 S40` For the extruder
  * `M140 S40` For the bed
* See if steppers are running (and in correct direction)
  * `STEPPER_BUZZ STEPPER=stepper_x`
  * `STEPPER_BUZZ STEPPER=stepper_y`
* Test probe
  * Verify probe deploy
    * `BLTOUCH_DEBUG COMMAND=pin_down`
    * `BLTOUCH_DEBUG COMMAND=pin_up`
  * Verify probe trigger
    * `BLTOUCH_DEBUG COMMAND=pin_down`
    * `BLTOUCH_DEBUG COMMAND=touch_mode`
    * `QUERY_PROBE` Should report "open"
    * Touching the probe lightly with a finger nail should make it retract
    * `QUERY_PROBE` Should report "triggered"
* Endstops and limits
  * `G28` To home all axes
  * Adjusting endstop positions so `0,0` nozzle position is at the correct location
  * Adjusting min/max positions for printable area
  * Set probe offset
  * Set homing position
* Set up Z offset
  * `PROBE_ACCURACY`
  * `PROBE_CALIBRATE`
* PID tunings
  * `PID_CALIBRATE HEATER=extruder TARGET=200`
  * `PID_CALIBRATE HEATER=heater_bed TARGET=60`
* Bed screws
  * `SCREWS_TILT_CALCULATE`
* Resonance compensation
  * `ACCELEROMETER_QUERY`
  * `MEASURE_AXES_NOISE`
  * `TEST_RESONANCES AXIS=X`
  * `TEST_RESONANCES AXIS=Y`
* Misc Tuning
  * Extrusion (stepper rotation distance)
* Create bed mesh
* Test extrusion on standard temperature
* Test print!

## Mentions

https://github.com/rootiest/zippy_guides/tree/main has some excellent information relating to setting up Klipper

https://realdeuce.github.io/Voron/PA/pressure_advance.html provides a Marlin-y PA calculator.

Handy Klipper extensions:

* https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging
