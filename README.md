# ProtoZoomyEnder

A repository for one of my personal 3D printers used as a learning/research project.

> Originally a Creality Ender 3 (v2) I got super cheap second hand.

## About

Main features:

* Prints pretty much any filament
* High speeds and acceleration
* Magnetic bed sheets and level probe
* Linear rails and accurate belt systems
* High torque stepper motors and drivers
* High flow extrusion
* Highly efficient cooling
* Runs on CAN bus
* Fairly quiet

Uses portions of designs from the following projects:

* LDO BeltEnder Motion System (Beta 2) [^1]
* Hero Me Toolhead (Gen 7) [^2]
* Universal Frame Stiffener [^3]

Runs on Klipper firmware with the following features:

* Bed Meshes
* Firmware Retraction
* Pressure Advance
* Resonance Compensation
* Object Exclusion
* Custom Filament Macros

## TODO

* Set up CANboot
* Install Rapido Plus block (PT1000 / 350C max)
* Calibrate Square Corner Velocity (`jerk * sqrt(2)`)
* Custom `CANCEL_PRINT` gcode macro
* Custom `M600` (automatic filament change) gcode macro
* Create an Enraged Rabbit!

[^1]: https://www.orbiterprojects.com/beltender-linear-rail-upgrade-for-ender-printers/
[^2]: https://www.printables.com/model/39322-hero-me-gen-7-platform-release-4
[^3]: https://www.printables.com/model/22099-universal-frame-stiffener-for-geeetech-a20-a30-cre
