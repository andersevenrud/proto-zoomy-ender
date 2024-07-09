# Flashing

These are instructions for flashing all the firmware of this printer in flash modes.

Bootloaders like [Katapult](https://github.com/Arksine/katapult) allows for flashing over serial,
but that is not covered here. The instrutions are the same, except the FLASH_DEVICE instrutions
`/dev/serial/by-id/<device>`.

## Host

```bash
make KCONFIG_CONFIG=config.host menuconfig
```

```menuconfig
[ ] Enable extra low-level configuration options
    Micro-controller Architecture (Linux process)  --->
```

```bash
make KCONFIG_CONFIG=config.host clean
make KCONFIG_CONFIG=config.host
make KCONFIG_CONFIG=config.host flash
```

## BTT SKR E3 v3

> Use SD card to flash firmware.

```bash
make KCONFIG_CONFIG=config.skre3v3 menuconfig
```

```menuconfig
[*] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32)  --->
    Processor model (STM32G0B1)  --->
    Bootloader offset (8KiB bootloader)  --->
    Clock Reference (8 MHz crystal)  --->
    Communication interface (USB (on PA11/PA12))  --->
    USB ids  --->
()  GPIO pins to set at micro-controller startup
```

```bash
make KCONFIG_CONFIG=config.skre3v3 clean
make KCONFIG_CONFIG=config.skre3v3
cp out/klipper.bin /mnt/sd-card/firmware.bin
```

## BTT EBB36 v1.2

> Put the device into USB mode and set VUSB jumper.
> DISCONNECT THE 24V power supply before powering up!
> To flash hold down BOOT button and press RST to enter DFU mode.

> See [./CAN.md](CANBus) for additional information.

```bash
make KCONFIG_CONFIG=config.ebb36 menuconfig
```

```menuconfig
[*] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32)  --->
    Processor model (STM32G0B1)  --->
    Bootloader offset (No bootloader)  --->
    Clock Reference (8 MHz crystal)  --->
    Communication interface (CAN bus (on PB0/PB1))  --->
(250000) CAN bus speed
()  GPIO pins to set at micro-controller startup (NEW)
```

```bash
make KCONFIG_CONFIG=config.ebb36 clean
make KCONFIG_CONFIG=config.ebb36
make KCONFIG_CONFIG=config.ebb36 flash FLASH_DEVICE=0483:df11
```

## BTT Eddy Coild (i2c)

```bash
make KCONFIG_CONFIG=config.eddy menuconfig
```

```menuconfig
[*] Enable extra low-level configuration options
    Micro-controller Architecture (Raspberry Pi RP2040)  --->
    Bootloader offset (No bootloader)  --->
    Flash chip (W25Q080 with CLKDIV 2)  --->
    Communication Interface (USB)  --->
    USB ids  --->
()  GPIO pins to set at micro-controller startup
```

```bash
make KCONFIG_CONFIG=config.eddy clean
make KCONFIG_CONFIG=config.eddy
make KCONFIG_CONFIG=config.eddy flash FLASH_DEVICE=0000:0000
```

## Fly ADXL345 (USB)

> Hold down the button on the board before inserting USB cable to enter flash mode.

```bash
make KCONFIG_CONFIG=config.adxl345 menuconfig
```

```menuconfig
[*] Enable extra low-level configuration options
    Micro-controller Architecture (Raspberry Pi RP2040)  --->
    Bootloader offset (No bootloader)  --->
    Flash chip (W25Q080 with CLKDIV 2)  --->
    Communication Interface (USBSERIAL)  --->
    USB ids  --->
()  GPIO pins to set at micro-controller startup
```

```bash
make KCONFIG_CONFIG=config.adxl345 clean
make KCONFIG_CONFIG=config.adxl345
make KCONFIG_CONFIG=config.adxl345 flash FLASH_DEVICE=2e8a:0003
```
