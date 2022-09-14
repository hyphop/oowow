# OOWOW How-to

## Resolve boot-up problem

if Boot OOWOW doesn't works via hold (FUNCTION) and short press (RESET)

* [Manualy restore OOWOW SPI-Flash firmware](#manualy-restore-oowow-spi-flash-firmware)
* [Boot-up OOWOW from SD-card](#boot-up-oowow-from-sd-card)

## Manualy restore OOWOW SPI-Flash firmware

For same cases if OOWOW can't bootup automaticly or via [button shortcut](oowow-user-manual.md#vim4-button-shortcuts)

* download http://dl.khadas.com/products/oowow/system/vim4-oowow-latest-spi-upgrade-sd.img.gz
* write image vim4-oowow-latest-spi-upgrade-sd.img.gz to SD-card
* boot-up from SD-card and wait upgrade process will be complited
* remove SD-card and reboot device

## Boot-up OOWOW from SD-card

For same cases if embedded OOWOW can't bootup from SPI-Flash. OOWOW can be started from SD-card anytime.

* download http://dl.khadas.com/products/oowow/system/vim4-oowow-latest-sd.img.gz
* write image vim4-oowow-latest-sd.img.gz to SD-card
* boot-up from SD-card

## write custom OS image into eMMC from removable storage

+ copy your OS image into any removable storage SD / USB Flash , etc (formatted by exfat or ext2/3/4 or fat)
+ start oowow by press FUNCTION + RESET
+ exit from wizard
+ plug removable storage with OS image
+ choose this image to write by __menu -> Write image to eMMC __ and up to .. mounts

NOTE: supported images

+ raw images `dd` suitable - .img
+ compressed images img.xz lzma , img.gz gzip, img.zst zstd

## Install online OS image without ethernet

wip...

## Headless usage

[Easy Wi-Fi](oowow-user-manual.md#easy-wi-fi)
wip...

## OOWOW and Smartphone

wip...
