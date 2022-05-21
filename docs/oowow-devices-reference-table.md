# OOWOW devices reference table

| Device | Support state| Embedded | SD card | Wi-Fi   | Ethernet
| :--    | :--          | :--      | :--     | :--     |
| VIM4   | Full         | Yes      | Yes     | [Full]  | Yes
| VIM3L  | Partially    | No       | Yes     | [Basic] | Yes
| VIM3   | WIP          | No       | Yes     | [Basic] | Yes
| VIM2   | WIP          | No       | Yes     | [Basic] | Yes
| VIM1   | WIP          | No       | Yes     | [Basic] | Yes
| VIM1S  | Expected     | -        | -       |         |
| Edge   | WIP          | No       | Yes     |         |
| Edge2  | Expected     | -        | -       |         |

Descriptions:
+ **SD card** - bootable from SD card
+ **Embedded** - ready for standalone usage as embedded service (SPI-Flash)
+ **WIP** - work in progress

### Wi-Fi full mode

Client and hotspot mode can used at same times

### Wi-Fi basic mode

Only client or hotspot mode works stable same time

[Basic]: <#wi-fi-basic-mode> "Only client or hotspot mode works stable same time"
[Full]:  <#wi-fi-full-mode> "Client or hotspot mode can works at same time"
