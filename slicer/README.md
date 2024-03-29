# Prusa Slicer

Main configuration entries customized for my setup.

## Print Settings

### Speed

Example profile:

> Where `P(erimiters)`/`I(nfill)`/`T(ravel)`/`S(ides)` is the target max speed.
> I.e: 200/200/300/30 for a fast profile.

> All acceleration control and values not mentioned are `0` (disabled)

> Maximum flow is dependent on nozzle and filament (including temperature)

```
Perimiters: P
Small perimiters: 90% of P
External perimiters: 60% of P

Infill: I
Solid infill: 90% of I
Top solid infill: S

Support material: 60% of P
Bridges: 60% of P
Gap fill: 60% of P

Travel: T

First layer speed: S
Max print speed: 300
Max volumetric flow: 20
```

### Output options

```
Label objects: Firmware-spesific
```

## Filament Settings

### Advanced

> Assumes PLA

```
Max volumetric speed: 0
```

### Cooling

> Assumes PLA

```
Keep fan always on: Yes
Enable auto cooling: Yes
Fan Speed: 40 - 50
Bridges Fan Speed: 70
Disable fan for the first: 1
Full fan speed at layer: 0
Enable dynamic fan speeds: No
Slow down if layer print time is below: 1
Min print speed: 60
```

### Custom G-code

#### Start

> Unknown brand and/or material type will fall back to the defaults defined in hardware.cfg

```
SETUP_FILAMENT brand=eSun material=PLA+
```

## Printer Settings

### General

```
Bed Shape: 220 x 220 (0x0 offset)
Max print height: 250
G-code flavour: Klipper
G-code thumbnails: 32x32,400x300
Supports stealth mode: No
Supports remaining time: Yes
Use relative E distances: Yes
Use firmware retraction: Yes
Use volumetric E: No
Enable variable layer height feature: Yes
```

### Custom G-code

#### Start

```
START_PRINT EXTRUDER_TEMP={first_layer_temperature[initial_extruder]} BED_TEMP={first_layer_bed_temperature[initial_extruder]}
SET_PRINT_STATS_INFO TOTAL_LAYER=[total_layer_count]
```

#### End

```
END_PRINT
; total layers count = [total_layer_count]
```

#### Before layer change

```
G92 E0
;{layer_z}
```

#### After layer change

```
SET_PRINT_STATS_INFO CURRENT_LAYER={layer_num + 1}
;{layer_z}
```

### Machine Limits

```
How to apply limits: Use for time estimate
Maximum X feedrate: 500
Maximum Y feedrate: 500
Maximum Z feedrate: 10
Maximum E feedrate: 120
Maximum X acceleration: 4500
Maximum Y acceleration: 4500
Maximum Z acceleration: 500
Maximum E acceleration: 3000
Maximum acceleration when extruding: 3000
Maximum acceleration when retracting: 3000
Maximum X Jerk: 10
Maximum Y Jerk: 10
Maximum Z Jerk: 0.3
Maximum E Jerk: 10
```

### Extruder

> Firmware retraction with exception of "Retract only on layer change"
> that is filament dependent and slicer only.

```
Minimum travel after retraction: 2
Retract only on layer change: No
```
