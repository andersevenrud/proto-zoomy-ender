# Resonances

Measured using ADXL345 over SPI on a Pico running as separate MCU.

> Printer rests on a 35mm thick concrete slab with a 20mm thick foam dampening sheet.

## X-Axis

![shaper_calibrate_x](./shaper_calibrate_x.png)

```
Fitted shaper 'zv' frequency = 132.8 Hz (vibrations = 16.6%, smoothing ~= 0.014)
To avoid too much smoothing with 'zv', suggested max_accel <= 68700 mm/sec^2
Fitted shaper 'mzv' frequency = 83.4 Hz (vibrations = 6.5%, smoothing ~= 0.032)
To avoid too much smoothing with 'mzv', suggested max_accel <= 20500 mm/sec^2
Fitted shaper 'ei' frequency = 126.2 Hz (vibrations = 6.9%, smoothing ~= 0.023)
To avoid too much smoothing with 'ei', suggested max_accel <= 29700 mm/sec^2
Fitted shaper '2hump_ei' frequency = 43.0 Hz (vibrations = 2.1%, smoothing ~= 0.292)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 1900 mm/sec^2
Fitted shaper '3hump_ei' frequency = 96.0 Hz (vibrations = 0.2%, smoothing ~= 0.089)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 6700 mm/sec^2
Recommended shaper is ei @ 126.2 Hz
```

## Y-Axis

![shaper_calibrate_y](./shaper_calibrate_y.png)

```
Fitted shaper 'zv' frequency = 21.0 Hz (vibrations = 33.8%, smoothing ~= 0.349)
To avoid too much smoothing with 'zv', suggested max_accel <= 1400 mm/sec^2
Fitted shaper 'mzv' frequency = 35.6 Hz (vibrations = 24.5%, smoothing ~= 0.161)
To avoid too much smoothing with 'mzv', suggested max_accel <= 3700 mm/sec^2
Fitted shaper 'ei' frequency = 49.8 Hz (vibrations = 27.2%, smoothing ~= 0.130)
To avoid too much smoothing with 'ei', suggested max_accel <= 4600 mm/sec^2
Fitted shaper '2hump_ei' frequency = 45.4 Hz (vibrations = 18.2%, smoothing ~= 0.262)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 2200 mm/sec^2
Fitted shaper '3hump_ei' frequency = 49.0 Hz (vibrations = 15.5%, smoothing ~= 0.341)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 1600 mm/sec^2
Recommended shaper is ei @ 49.8 Hz
```
