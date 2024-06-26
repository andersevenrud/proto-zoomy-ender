# Filaments

Personal tuning and parameter tables used in the slicer and firmware.

Retraction, Pressure Advance and Extrusion factors are always set in firmware via macros
to eliminate the need for re-slicing models for any hardware change.

## Filament table

Tested optimal values:

> NB: eSun ABS+ Seems to have poor layer adhesion compared to regular ABS no matter what temperature it is printed at. Also it has 5-10C lower max serice temperature. It is easier to print though, but not reliable for parts that are under a lot of force.

| Filament              | Temperature    | Speed     | Retraction    | Fan Speed | PA    | Extrusion |
| --------------------- | -------------- | --------- | ------------- | --------- | ----- | --------- |
| Generic PLA           | 205C /  60C    | 200mm/s   | 0.7 @ 100mm/s | <= 50%    | 0.050 | 100%      |
| eSun PLA+             | 220C /  60C    | 200mm/s   | 0.5 @ 100mm/s | <= 50%    | 0.044 | 100%      |
| eSun ABS+             | 235C / 100C    | 120mm/s   | 0.5 @ 100mm/s | <= 30%    | TBD   | 100%      |
| ProtoPasta PLA        | 210C /  60C    | 200mm/s   | 0.5 @ 100mm/s | <= 50%    | TBD   | 100%      |
| ProtoPasta HTPLA      | 210C /  60C    | 120mm/s   | 0.5 @ 100mm/s | <= 50%    | 0.036 | 100%      |
| Fiberlogy TPU 40D     | 210C /  60C    |  30mm/s   | 0.0 @  30mm/s | <= 10%    | 0.720 | 105%      |
| 3DNet PETG            | 230C /  80C    | 120mm/s   | 0.5 @ 100mm/s | <= 30%    | 0.042 | 100%      |
