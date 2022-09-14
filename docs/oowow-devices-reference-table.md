# OOWOW devices reference table

| Device | Support state| Embedded | SD card | Wi-Fi   | Ethernet |
| :--    | :--          | :--      | :--     | :--     | :--      |
  VIM4   | Full         | Yes      | Yes     | [Full]  | Yes
  VIM3L  | [Partially]  | No       | Yes     | [Basic] | Yes
  VIM3   | [Partially]  | No       | Yes     | [Basic] | Yes
  VIM2   | [Partially]  | No       | Yes     | [Basic] | Yes
  VIM1   | [Partially]  | No       | Yes     | [Basic] | Yes
  VIM1S  | Full         | Yes      | Yes     | [Basic] | Yes
  Edge   | [Partially]  | No       | Yes     |         |
  Edge2  | Full         | Yes      | Ext/USB | [Full]  | USB-Dongle

Descriptions:
+ **SD card** - bootable from SD card
+ **Embedded** - ready for standalone usage as embedded service (SPI-Flash)
+ **WIP** - work in progress

### Wi-Fi full mode

Client and hotspot mode can used at same times

### Wi-Fi basic mode

Only client or hotspot mode works stable same time

### Partially support status

Old generation boards VIM1 VIM2 VIM3 VIM3L - marked as partially support

[Basic]:      <#wi-fi-basic-mode> "Only client or hotspot mode works at same time"
[Full]:       <#wi-fi-full-mode> "Client or hotspot mode can works at same time"
[Partially]:  <#partially-support-status> "Old generation boards marked as partially support"

[USB-Dongle]: <#usb-ethernet-dongle> "Usb Ethernet dongle"
