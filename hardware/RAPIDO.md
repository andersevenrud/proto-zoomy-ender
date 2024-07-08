# Phaetus Rapido UHF

The "Plus" and "Regular" is the exact same hotend, except the thermistor is different
and requires custom cirtuitry to read the values correctly.

## Klipper configuration

### Regular

```
sensor_type: ATC Semitec 104NT-4-R025H42G
max_temp: 290
```

### Plus

```
sensor_type: MAX31865
max_temp: 350
spi_bus: spi1
rtd_nominal_r: 100
rtd_reference_r: 430
rtd_num_of_wires: 2
```
