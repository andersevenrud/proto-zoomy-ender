# Maintenance

## General

* Ensure that surfaces are not covered in grease and dust/plastic debris/etc.
* Ensure that cable connections are secured
* Check if screws are loose
* Check if fans and ducts are dusty
* Check if there is any audible bad noises

## Belts

Every 100hrs running time just ensure that belts are firm.

Make sure there are no deep cracks.

* Use the measurement tool for Z belt
* **TODO** Use ? for X belt
* **TODO** Use ? for Y belt

## Extruder

Clean every 100hrs running time with eSun Cleaning Filament.

## Rails

Ensure smooth travel on inspection every 100hrs.

Every **TODO** interval perform a full cleaning procedure:

> Before actually running the Tuning step ensure that everything is operation like normal.

1. Unmount
    1. Loosen all belts
    2. Unscrew X/Y mounts
    3. Unscrew Z belt mount
    4. Unscrew linear rails
2. Clean & Lube
    1. Soak rails in a mix if IPA and 50% water for an hour at room temperature
    2. Scrub with a nylon brush and and rag then let it dry completely
    3. Apply PTFE grease in the blocks (and light librication oil)
3. Re-Mount
    1. Mount linear rails with alignment guides
    2. Screw linear rails back into place (lightly from the center outwards)
    3. Screw X/Y mounts back into place
    4. Tighten all belts
4. Alignment
    1. Perform a Z gantry alignment with a straight edge ruler
    2. Screw Z belt mount back into place
    3. Ballpark tram the bed to the nozzle using a spacer (like a 20mm calibration cube)
5. Tuning (Klipper)
    1. Perform automatic bed tramming with wizard
    2. Perform a probe alignment (optional, but recommended)
    3. Re-run bed mesh calibration
