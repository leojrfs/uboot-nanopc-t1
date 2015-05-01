# Nanopc-T1 u-boot

## Compile

```
cd uboot-nanopc-t1
make tiny4412_config
make
```
## Writing u-boot image to SD card

### Prepare the necessary tools

```
cd sd_fuse
make
```

### u-boot programmed to SD card

```
cd tiny4412
sudo ./sd_fusing.sh YOUR_SD_DEVICE #such as /dev/sdb
```
## Test

1. Plug in SD card, while pressing bootmode button, turn on and then release the bootmode button.

Terminal output example:

```
OK

U-Boot 2010.12-00000-g8ac4182-dirty (Mar 01 2015 - 11:56:19) for TINY4412


CPU:    S5PC220 [Samsung SOC on SMP Platform Base on ARM CortexA9]
        APLL = 1500MHz, MPLL = 800MHz

Board:  TINY4412
DRAM:   2047 MiB

vdd_arm: 1.2
vdd_int: 1.0
vdd_mif: 1.1

BL1 version:  N/A (TrustZone Enabled BSP)


Checking Boot Mode ... SDMMC
REVISION: 1.1
MMC Device 0: 15193 MB
MMC Device 1: 7456 MB
MMC Device 2: N/A
*** Warning - using default environment                                         
                                                                                
Net:    No ethernet found.                                                      
Hit any key to stop autoboot:  0
TINY4412 #
```

## Special thanks to:

1. wanyuhang: <http://www.arm9home.net/read.php?tid-83336-uid-105026.html>
2. halechan: <https://github.com/halechan/uboot-nanopc-t1>
