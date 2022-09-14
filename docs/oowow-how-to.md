# OOWOW How-to

## Resolve boot-up problem

if Boot OOWOW doesn't works via hold (FUNCTION) and short press (RESET)

* [Manualy restore OOWOW SPI-Flash firmware](#manualy-restore-oowow-spi-flash-firmware)
* [Boot-up OOWOW from SD-card](#boot-up-oowow-from-sd-card)

## Manualy restore OOWOW SPI-Flash firmware

For same cases if OOWOW can't bootup automaticly or via [button shortcut](oowow-user-manual.md#vim4-button-shortcuts)

* download XXX-oowow-latest-spi-upgrade-sd.img.gz from http://dl.khadas.com/products/oowow/system/
* write image XXX-oowow-latest-spi-upgrade-sd.img.gz to SD-card
* boot-up from SD-card and wait upgrade process will be complited
* remove SD-card and reboot device

NOTE: replace XXX to right board name

## Boot-up OOWOW from SD-card

For same cases if embedded OOWOW can't bootup from SPI-Flash. OOWOW can be started from SD-card anytime.

* download XXX-oowow-latest-sd.img.gz from http://dl.khadas.com/products/oowow/system/
* write image XXX-oowow-latest-sd.img.gz to SD-card
* boot-up from SD-card

NOTE: replace XXX to right board name

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

All devices have on-board Wi-Fi module, also can used for for Internet access.

 + Configure Wi-Fi connection one time / automaticly will be used next time
 + or can use [Easy Wi-Fi](oowow-user-manual.md#easy-wi-fi) mode

## Headless usage

OOWOW easily can used without display and keyboards.

+ [Easy Wi-Fi](oowow-user-manual.md#easy-wi-fi)
+ [Hot-Spot mode](oowow-user-manual.md#hotspot)

## OOWOW and Smartphone

OOWOW easily can controlled by smatphone

+ [Easy Wi-Fi](oowow-user-manual.md#easy-wi-fi)
+ [Hot-Spot mode](oowow-user-manual.md#hotspot)
+ [Hot-spot QR-code](oowow-user-manual.md#hotspot-qr-code)
+ [Web-Access QR-code](oowow-user-manual.md#web-access-qr-code)
