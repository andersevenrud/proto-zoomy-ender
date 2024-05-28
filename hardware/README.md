# Hardware

A Cartesian (aka "bed slinger") FFF/FDM 3D printer.

## Specs

* Weight: ~10kg
* Noise level: <60dB
* Print Volume: 230x230x250mm
* Probe Area: 205x220mm
* Probe Speed: <=10mm/s
* Probe Accuracy: <0.0020mm
* Endstop Accuracy: ~0.1mm
* Bed Flatness: <0.2mm (Probed range)
* Bed Temperature: 100°C (Max)
* Chamber Temperature: 70°C (Max)
* Print Temperature: 280°C (Max)
* Print Speed: <=200mm/s (Optimal), ~500mm/s (Max)
* Print Acceleration: <=5000ms/s² (Optimal), ~8000mm/s² (Max)
* Extruder Acceleration: <=3000mm/s² (Optimal), ~8000mm/s² (Max)
* Extrusion Force: 10kg (Max)
* Retraction Speed: ~120mm/s (Max)
* Heatup Time: Bed ~120s, Nozzle <60s (Ambient to PLA parameters)
* Communication: CAN bus (Toolhead), USB (Mainboard and Host)
* Volumetric Flow
  * 20-30mm³/s (0.4mm V6/HF)
  * 30-50mm³/s (0.6mm Volcano/UHF)
  * 75mm³/s (Theoretical/Vendor benchmarked)
* Motion/Drive Train
  * X: Belt, Linear Rail
  * Y: Belt, Dual Linear Rails
  * Z: Belt, Dual Linear Rails, 80:16 Gearbox
  * E: Direct Drive, 7.5:1 Gearbox
* Cooling
  * Parts: 25m³/h, 6.5kpa (Max)
  * Hotend: 13.1m³/h (Max)
  * Mainboard: 7.0m³/h (Max)
  * Toolhead: 4.0m³/h (Max)
  * PSU: 10.0m³/h (Max)
* Steppers
  * X: 1.8°, 55Ncm, 2.50A/Phase (Max)
  * Y: 1.8°, 55Ncm, 2.50A/Phase (Max)
  * Z: 1.8°, 55Ncm, 2.50A/Phase (Max)
  * E: 1.8°, 10Ncm, 1.20A/Phase (Max)
* Power Draw
  * Bed: ~220W (Max)
  * Hotend: ~115W (Max)
  * Steppers: ~200W (Max)
  * Cooling: 80W (Max)
  * Total: ~360W (Max)
      * Idle: ~50W
      * Ready: ~150W
      * Printing: ~200W (PLA parameters)

## Parts

> All custom parts was printed in ABS

* **Frame**
    * Creality stock frame
    * RatRig Cast 90 Degree Corner brackets
    * DIY Extrusion end caps
    * DIY Carrying handle
    * DIY Braces (Stiffeners) on Z axis (8mm rods)
    * DIY Cases for MCUs, power converters and boards
    * DIY Nozzle Wiper
* **Bed**
    * Creality stock heated aluminum bed
    * Creativity Silicon solid mounts
    * Creativity Replacement lightweight frame
    * Brass M4 thumb tramming nuts
    * 3M magnetic surface
        * Polyalkemi Smooth PEI Sheet
        * PrimaFlex Textured PEI Sheet
        * Homemade Probe/Offset/Limit Calibration Sheet
* **X-Axis**
    * LDO 42STH48-2504AC stepper
    * Creativity Aluminum tensioner (w/custom adjuster)
    * Creality stock endstop switch
    * HIWIN MGN12H Linear Rail (300mm)
    * Polisi3D Copper Belt Clamps
    * Gates Powergrip GT2/6mm Belt
    * RatRig GT2/6mm 20T/5mm Pulley
    * RatRig GT2/6mm 20T/5mm Idler
    * DIY stepper cover and endstop position
* **Y-Axis**
    * LDO 42STH48-2504AC stepper
    * Creativity Aluminum tensioner (w/custom adjuster)
    * Creativity Linear Rail brackets
    * Creality stock endstop switch
    * HIWIN MGN12H Linear Rails (Dual 300mm)
    * Polisi3D Copper Belt Clamps
    * Gates Powergrip GT2/6mm Belt
    * RatRig GT2/6mm 20T/5mm Pulley
    * RatRig GT2/6mm 20T/5mm Idler
* **Z-Axis**
    * LDO 42STH48-2504AC stepper
    * Generic MGN12H Linear Rails (Dual 300mm)
    * Polisi3D Copper Belt Clamps
    * Gates GT2/6mm 188mm Belt Loop
    * Gates Powergrip GT2/6mm Belt
    * Gates Powergrip GT2/6mm Idlers
    * Gates Powergrid GT2/6mm 16T Pulleys
    * Gates GT2/6mm Belt Tension Springs
    * Siboor GT2/6mm 80T Gear
    * Openbuilds brass shims
    * Powge D shafts
    * PlusReprap Bearings for gearbox
    * Custom belt system standoffs/mounts
* **Toolhead**
    * LDO Orbiter Extruder (v2)
    * LDO Orbiter Filament Sensor (v2.2)
    * Antclabs BLTouch (v3.1)
    * Capricorn XS PTFE Tubes
    * Sunon Maglev 4040 extruder cooling fan
    * Siboor Filament Cleaner Clip
    * Bondtech HeatLink adapters
    * Neopixel LEDs for parts lighting
    * Mellow 15mm ID CPAP Pipe
    * Phaetus Rapido UHF (Volcano/V6)
      * E3D V6 Nozzle-X 0.4mm (V6)
      * Phaetus Hardened Steel 0.4mm (V6)
      * Phaetus Hardened Steel 0.6mm (Volcano)
* **MCUs**
    * BTT U2C CAN Bridge (v2.1)
    * BTT EBB36 w/MAX31865 CAN (v1.2) (TMC2209)
        * SHCHV 25mm CAN board cooling fan (5V)
    * BTT SKR E3 v3 Mainboard (TMC2209)
        * Sunon Maglev 4020 cooling fan
    * Raspberry Pi 3B+ Host
        * Sunon Maglev 4010 cooling fan
* **Misc**
    * Mellow WS7040 24V CPAP Blower fan (remote cooling)
* **PSU**
    * Meanwell LRS-350-24 (24V, 350W)
    * KIS3R33S Buck Converter (5V, 15W)
