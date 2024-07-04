# Flashing

These are instructions for flashing all the firmware of this printer in flash modes.

Bootloaders like [Katapult](https://github.com/Arksine/katapult) allows for flashing over serial,
but that is not covered here. The instrutions are the same, except the FLASH_DEVICE instrutions
`/dev/serial/by-id/<device>`.

## Host

```bash
KCONFIG_CONFIG=config.host make menuconfig

KCONFIG_CONFIG=config.host make clean
KCONFIG_CONFIG=config.host make
KCONFIG_CONFIG=config.host make flash
```

```menuconfig
[ ] Enable extra low-level configuration options
    Micro-controller Architecture (Linux process)  --->
```

## BTT SKR E3 v3

> Use SD card to flash firmware.

```bash
KCONFIG_CONFIG=config.skre3v3 make menuconfig

KCONFIG_CONFIG=config.skre3v3 make clean
KCONFIG_CONFIG=config.skre3v3 make
cp out/klipper.bin /mnt/sd-card/firmware.bin
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

## BTT EBB36

> Put the device into USB mode and set VUSB jumper.
> DISCONNECT THE 24V power supply before powering up!
> To flash hold down BOOT button and press RST to enter DFU mode.

> See [CAN.md](CANBus) for additional information.

```bash
KCONFIG_CONFIG=config.ebb36 make menuconfig

KCONFIG_CONFIG=config.ebb36 make clean
KCONFIG_CONFIG=config.ebb36 make
KCONFIG_CONFIG=config.ebb36 make flash FLASH_DEVICE=0483:df11
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

## BTT Eddy

```bash
KCONFIG_CONFIG=config.eddy make menuconfig

KCONFIG_CONFIG=config.eddy make clean
KCONFIG_CONFIG=config.eddy make
KCONFIG_CONFIG=config.eddy make flash FLASH_DEVICE=0000:0000
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

## Fly ADXL

> Hold down the button on the board before inserting USB cable to enter flash mode.

```bash
KCONFIG_CONFIG=config.adxl345 make menuconfig

KCONFIG_CONFIG=config.adxl345 make clean
KCONFIG_CONFIG=config.adxl345 make
KCONFIG_CONFIG=config.adxl345 make flash FLASH_DEVICE=2e8a:0003
```

```menuconfig
[*] Enable extra low-level configuration options
    Micro-controller Architecture (Raspberry Pi RP2040)  --->
    Bootloader offset (16KiB bootloader)  --->
    Communication Interface (USBSERIAL)  --->
    USB ids  --->
()  GPIO pins to set at micro-controller startup
```
