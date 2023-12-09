# Resonances

Measured using ADXL345 over SPI on a Pico running as separate MCU.

> Printer rests on a 35mm thick concrete slab with a 20mm thick foam dampening sheet.

## X-Axis

![shaper_calibrate_x](./shaper_calibrate_x.png)

```
Fitted shaper 'zv' frequency = 40.0 Hz (vibrations = 16.4%, smoothing ~= 0.100)
To avoid too much smoothing with 'zv', suggested max_accel <= 6200 mm/sec^2
Fitted shaper 'mzv' frequency = 29.0 Hz (vibrations = 4.8%, smoothing ~= 0.242)
To avoid too much smoothing with 'mzv', suggested max_accel <= 2500 mm/sec^2
Fitted shaper 'ei' frequency = 37.8 Hz (vibrations = 1.8%, smoothing ~= 0.225)
To avoid too much smoothing with 'ei', suggested max_accel <= 2700 mm/sec^2
Fitted shaper '2hump_ei' frequency = 39.0 Hz (vibrations = 0.0%, smoothing ~= 0.355)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 1500 mm/sec^2
Fitted shaper '3hump_ei' frequency = 81.0 Hz (vibrations = 2.0%, smoothing ~= 0.125)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 4800 mm/sec^2
Recommended shaper is 3hump_ei @ 81.0 Hz
```

## Y-Axis

![shaper_calibrate_y](./shaper_calibrate_y.png)

```
Fitted shaper 'zv' frequency = 40.2 Hz (vibrations = 6.9%, smoothing ~= 0.099)
To avoid too much smoothing with 'zv', suggested max_accel <= 6300 mm/sec^2
Fitted shaper 'mzv' frequency = 39.4 Hz (vibrations = 0.0%, smoothing ~= 0.131)
To avoid too much smoothing with 'mzv', suggested max_accel <= 4600 mm/sec^2
Fitted shaper 'ei' frequency = 47.6 Hz (vibrations = 0.0%, smoothing ~= 0.142)
To avoid too much smoothing with 'ei', suggested max_accel <= 4200 mm/sec^2
Fitted shaper '2hump_ei' frequency = 59.4 Hz (vibrations = 0.0%, smoothing ~= 0.153)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 3900 mm/sec^2
Fitted shaper '3hump_ei' frequency = 71.6 Hz (vibrations = 0.0%, smoothing ~= 0.160)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 3800 mm/sec^2
Recommended shaper is mzv @ 39.4 Hz
```
