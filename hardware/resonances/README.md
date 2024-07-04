# Resonances

Measured using ADXL345 over SPI on a Pico running as separate MCU.

> Printer rests on a 35mm thick concrete slab with a 20mm thick foam dampening sheet.

## X-Axis

![shaper_calibrate_x](./shaper_calibrate_x.png)

```
Fitted shaper 'zv' frequency = 123.6 Hz (vibrations = 22.1%, smoothing ~= 0.015)
To avoid too much smoothing with 'zv', suggested max_accel <= 59500 mm/sec^2
Fitted shaper 'mzv' frequency = 30.2 Hz (vibrations = 7.5%, smoothing ~= 0.223)
To avoid too much smoothing with 'mzv', suggested max_accel <= 2700 mm/sec^2
Fitted shaper 'ei' frequency = 40.4 Hz (vibrations = 5.5%, smoothing ~= 0.197)
To avoid too much smoothing with 'ei', suggested max_accel <= 3000 mm/sec^2
Fitted shaper '2hump_ei' frequency = 39.0 Hz (vibrations = 1.1%, smoothing ~= 0.355)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 1500 mm/sec^2
Fitted shaper '3hump_ei' frequency = 86.6 Hz (vibrations = 0.1%, smoothing ~= 0.109)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 5500 mm/sec^2
Recommended shaper is 3hump_ei @ 86.6 Hz
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
