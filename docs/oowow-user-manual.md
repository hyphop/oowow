# OOWOW User Manual

## What is OOWOW?

OOWOW is an embedded service (integrated into your device) - it can be
run at any time if you need to perform essential maintenance services on
your device.

## About VIM4

VIM4 is the first device from Khadas that includes the OOWOW embedded
service. Since VIM4 comes without any pre-installed OS, users can use
OOWOW to select and install their preferred OS.

## OS Delivery

OOWOW provides rapid online OS download and installation, which will
improve quality of life for single board computer users - with OOWOW, you
can install / reinstall your preferred OS in just 2-3 minutes.

## OOWOW Wizard

The OOWOW wizard will guide you to install a new OS in just 4 steps, and
it automatically starts if your device storage is empty.

* Connect to internet over Wi-Fi or Ethernet
* Display OS images for your device
* Select OS installation image
* Download and install OS into your device

Wizard Usage Example: [quick-start](../screencasts/quick-start/-gallery?play=loop)

Tip: If you need other features, exit from the wizard to the main menu.

## Main Features
* Install / reinstall OS
* Download online OS images
* Backup and restore system
* Display full device information
* Configure device
* Device hardware testing
* Online script collection
* Rescue shell
* Developer and advanced features

# Hardware

## Hardware Buttons

You can use the three physical buttons on your device to interact
directly with the OOWOW system, we will describe them in more detail
within the next section.

* (RESET) - reset device
* (FUNCTION) - multi functions
* (POWER) - multi functions

## VIM4 Button Shortcuts

* Boot OOWOW - hold (FUNCTION) and short press (RESET)
* Toggle Easy Wi-Fi - short press (POWER) button
* Toggle Hotspot -  short press (FUNCTION) button
* Accept Hotspot client  - short press (POWER) button
* Power off - Long press the (POWER) button until device shuts down
* Enter multifunction mode - press and hold (FUNCTION) button, release to
  activate selected function.
  (loop cycle: _HotSpot -> Firewall Allow -> Firewall Block -> Cancel ->_,
  each mode wait 2 sec)

Tip: All shortcut events will be displayed on OOWOW status bar and indicated by LEDs

## Tips to Boot OOWOW

* Eject your SD card before booting OOWOW (SD card has highest priority)
* Boot OOWOW from sleep: hold (FUNCTION) + short press (POWER) button
* Boot OOWOW with power cable: hold (FUNCTION) + plug power cable

## LED Indication Table

Most system events have corresponding LED indications:

| Events | Indications |
| :-- | :-- |
Device starts or reboots | White solid
Device power off | Red solid
System start in default mode | White heartbeat
Network connected | White solid
HotSpot mode activated | White fast blinking
HotSpot mode ready | White solid
HotSpot client pending | White and red blinking
HotSpot client accepted | White slow blinking
HotSpot mode deactivated | White heartbeat
Easy Wi-Fi activated | White blinking
Easy Wi-Fi awaits connection | White slow blinking
Easy Wi-Fi deactivated | White heartbeat
Firewall block incoming | Red breathing
Firewall allow incoming | White solid, red off
Firewall disabled | Red blinking
Image installation progress | Red & white blinking
Image installation done | White solid, red off

Multifunctional modes:

| Events | Indications |
| :-- | :-- |
Hotspot | White off
Firewall block incoming | White solid, red off
Firewall allow incoming | White & red solid
Cancel | White blinking

Boot stages:

| Events | Indications |
| :-- | :-- |
Early board start | White & red off
U-boot start | White solid
OOWOW loading | White solid, red heartbeat
OOWOW fail | White & red solid
OOWOW starting | White solid, red off

# Interfaces

## Main menu

OOWOW provides a universal user interface (terminal mode menu + top
status line) for HDMI, WEB, SSH, Serial-UART, etc (all interfaces work
simultaneously)

### Navigation
* Keys: [0-9] [A-Z] [⇦] [⇨] [⇧] [⇩] [Space] [Enter] [Esc] [Tab]
* Mouse: select menu items and press buttons

### HDMI + keyboard
A HDMI screen and keyboard is the primary interface modality.

### Web access
Examples:
* http://DEVICE_IP or http://DEVICE_HOST_NAME - device page
* http://vim4-xxxxx.local/x/ - welcome page
* http://vim4-xxxxx.local/x/control - main menu

Tip: Access can be restricted by the Firewall

### Mobile navigation
* keys: [0-9] [A-Z] [Space] [Enter]
* touchscreen: select menu items and press buttons
* some virtual keyboard have additional keys: [⇦] [⇨] [⇧] [⇩] [Esc] [Tab]

### SSH access
* root access works by default without password
* `ssh root@vim4-xxxxx.local` - plain shell
* `ssh root@vim4-xxxxx.local system` - main menu

Tip: Access can be restricted by the Firewall

### Serial UART access
For developers and advanced users only
* baudrate: 921600 ( `screen /dev/ttyUSB0 921600`)
* root access works by default without password
* `system` - main menu

## WEB API
For developers and advanced users only

# Networks
Network connection is required for:

* OS downloading and installation
* OOWOW system updates
* Dynamic syncing of online scripts
* Remote control over LAN and WLAN

## Device network name
Every OOWOW device can be accessed remotely via its unique LAN name.

device-xxxxx:
* device: lowercase device name, e.g. VIM4 => vim4
* xxxxx: last 5 digits of the device serial number

Network name examples:
* vim4-00010
* vim4-00012
* vim3-12333

## Network name resolution
Depends on your LAN configuration, for example:
* vim4-00010 - dns resolver
* vim4-00010.local - umdns resolving - canonical variant for oowow
* …

Tips:
* Use device ip address if name resolution doesn't work
* oowow uses the DHCP hostname
* oowow uses the MDNS hostname announcement

## Network name usage examples
```
# ping vim4-05690
PING vim4-05690 (192.168.30.203) 56(84) bytes of data.
64 bytes from 192.168.30.203 (192.168.30.203): icmp_seq=1 ttl=64 time=37.3 ms

# ping -c1 vim4-05690.local
PING vim4-05690.local (192.168.30.203) 56(84) bytes of data.
64 bytes from 192.168.30.203 (192.168.30.203): icmp_seq=1 ttl=64 time=37.3 ms

# curl http://vim4-05690.local
# curl http://192.168.30.203
# curl 192.168.30.203
# ssh root@vim4-05690
# ssh root@vim4-05690.local
```

## Ethernet LAN

Ethernet works automatically; just plug in an ethernet cable from your
router.

## Wireless LAN

User can setup and configure a WLAN connection
_Network -> Wi-Fi -> Wi-Fi Select Connection_

Tips:
* Wi-Fi configurations are automatically saved and will persist after rebooting
* All system configurations will be saved only after a planned shutdown
[how-to save setting](../screencasts/howto-save-setting/-gallery?play=auto&delay=2)

## Easy Wi-Fi

In cases wherein you are unable to configure a WLAN or LAN connection
locally on your device, you can share your internet connection from a
mobile device (e.g. smartphone) to your single board computer using the
Easy Wi-Fi mode.

You can enable the Easy Wi-Fi mode on your device in two ways:

* Toggle Easy Wi-Fi - short press (POWER) button
* _Network -> Wi-Fi -> Easy Wi-Fi oowow > Enable / Disable_

Setup a new hotspot from your mobile device with the following configuration:

* Name: **oowow**
* Password: **12345678**

Once OOWOW is in the Easy Wi-Fi mode, it will automatically scan and
connect to your Wi-Fi hotspot generated by your mobile device.

## Hotspot
You can enable the OOWOW hotspot feature in two ways:

* Toggle hotspot - short press (FUNCTION) button
* _Network -> Hotspot -> Hotspot Enable / Disable_

The OOWOW hotspot will have the following configuration:

* SSID: **vim4-xxxxx** ( xxxxx - last 5 digits from device serial number )
* Password: **12345678**

These hostnames can be used for device access via the hotspot:

* http://172.23.0.1
* http://oowow or http://oowow.local - works only for hotspot network
* http://vim4-xxxxx or http://vim4-xxxxx.local

Tip: For security reasons, you need to manually accept incoming hotspot
connections by short pressing the (POWER) button once.

## HotSpot QR code
_Network -> HotSpot -> HotSpot QR code_

## Web access QR code
+ _Network -> HotSpot -> Device Web Access QR code_
+ _Network -> Wi-Fi -> Device Web Access QR code_

## USB-OTG network

Connect your device directly to your computer using a USB cable. This
feature will interest developers or advanced users; there is only a
peer-to-peer network connection, no internet packets will be forwarded to
your device.

## Firewall
_Network -> Firewall Mode:_

* block - Block all incoming connections **SECURE**
* allow - Allow incoming connections from local networks **RECOMMENDED**
* disabled -  Allow all connections, firewall disabled **DANGER**

Tips:
   * By default, remote access is blocked by the firewall
   * Easily configure the firewall with the hardware button shortcuts 
   * ICMP pings are always allowed, irrespective of firewall mode
   * Hotspot mode allows incoming connections only after pressing the (POWER) button (device access: 172.23.0.1 or http://172.23.0.1)
   * USB-OTG connection is always allowed

## Usage examples

### Configure Wi-Fi with Wizard
[wizard-wifi-usage](screencasts/wizard-wifi-usage/-gallery?play=loop)

### Wi-Fi connection
[network-wifi-setup](screencast/network-wifi-setup/-gallery?play=loop)

### Easy Wi-Fi connection
[easy-wifi-mode](screencast/easy-wifi-mode/-gallery)

### Hotspot mode
[hotspot-mode](screencast/hotspot-mode/-gallery)

### Hotspot mode + ethernet LAN
Internet access provided by LAN ethernet cable, user device access provided by WLAN hotspot

### Hotspot mode + Wi-Fi WLAN connection
Internet access provided by WLAN wifi-connection and user device access provided by WLAN hotspot same time

### Ethernet
wip…

# Security and privacy
* OOWOW works only by user demand, and never works in the background 
* OOWOW never sends any private data from your device to the internet
* By default, remote access to your device is blocked by the firewall

# Limitations
* Unicode international symbols don’t display properly for HDMI (Wi-Fi network names)
* IPV6 disabled at this time

# Updates
* Automatically looks for updates when internet is connected, user will be notified if new updates need to be applied
* System updates must be manually approved by the user
* Don't turn off computer - during update

# Download OOWOW
* https://dl.khadas.com/products/oowow/ - oowow main page
* https://dl.khadas.com/products/oowow/system/ - oowow system/firmware images

## Image types
* vim4-oowow-latest-sd.img.gz - latest oowow image for SD-card or USB-thumb drive
* vim4-oowow-latest-spi.img.gz - latest oowow image for SPI-flash
* vim4-oowow-latest-spi-upgrade-sd.img.gz - upgrade oowow SPI-flash firmware from SD-card

## Filename for latest OOWOW version
* vim4-oowow-latest-sd.img.gz => versions/vim4/vim4-oowow-VERSION-sd.img.gz

Tip: Latest firmware link: https://dl.khadas.com/products/oowow/system/vim4-oowow-latest-sd.img.gz

Download images using command line:
   * `curl -JOL https://dl.khadas.com/products/oowow/system/vim4-oowow-latest-sd.img.gz`
   * `wget --content-disposition https://dl.khadas.com/products/oowow/system/vim4-oowow-latest-sd.img.gz`

# About OOWOW

## Why create OOWOW?

The process of new OS Installation is the biggest headache for users of
single board computers (SBC); before installing an OS, users must read
tons of manuals, trawl through online forums, learn how to
install/reinstall using their desktop/laptop PC, learn where to find
proper images etc... If something goes wrong it is possible to “BRICK”
(destroy) your device.

In other words, any form of device upgrade, maintenance, or OS
reinstallation requires advanced skills and external hardware, and this
is out of reach for the average user, or users in regions without
desktop/laptop PCs. With OOWOW your SBC becomes a standalone device;
perform all maintenance functions and OS installation directly from the
device itself.

Another issue is that manufacturers of SBCs release extremely powerful
hardware without mature OS support, as they are focused primarily on
hardware development. OOWOW is a solution for such companies to delegate
their software development to external independent groups, who can
provide a standard embedded system architecture for device configuration
and online OS delivery to end users.

OOWOW understands the end user deeply; it provides an out-of the-box,
universal OS delivery and device configuration solution for all SBCs in
the market today and into the future.

Live life easily with OOWOW!

## What is the meaning of "OOWOW"?

oowow - infinity level wow (will be a new 77th word in the English dictionary)

+ Pronunciation: /uː/  +  /wau/ = /u:wau/
+ Variations: ∞wow, infinity wow, endless wow 

Tips:
* https://en.wiktionary.org/wiki/wow
* https://www.crosswordsolver.org/words-starting-with-oo
