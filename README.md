# Gigabyte C246 WU4 Hackintosh on OpenCore

## macOS Versions
#### macOS Big Sur Beta9 (20A5384c)

## SMBIOS
#### iMacPro1,1

### What works
- **WIFI,Bluetooth,AirDrop, Handoff** BCM94360CD Required
- **USB** All USB3.1/USB2.0 Port
- **Audio** Realtek ALC1220-VB, (layout id: 7)
- **Siri** Work fine
- **DRM Content** Apple TV+/Safari Netflix/Amazon Prime

### Not works
- **iMessage,FaceTime** ??

### Device Lists
| Device | Model |
|----|----|
| MotherBoard | Gigabyte C246 WU4 |
| CPU | Intel Xeon E-2278G |
| RAM | Samsung 16GB DDR4 2666MHz ECC Memory Module * 4 |
| Video Card | Sapphire RX 5500XT 8GB |
| Sound Card | Realtek ALC1220-VB （MotherBoard）|
| Network Interface Card | PCI-E BCM94360CD (WI-FI + Bluetooth) |
| Optical Network Card | Intel X520-DA2 2-Port 10GbE FCoE SFP+ NIC |
| Thunderbolt Card | Gigabyte GC-TITAN-RIDGE |
| FireWire Expansion Card | PCI 1394A+1394B FireWire 800 |
| Hard Disk | Hikvision C2000Pro 1TB NVMe SSD |
| Case | Cooler Master S600 |

### Software Version
#### Boot firmware
| Boot  | Versions |
|----|----|
| OpenCore | [Latest release(0.6.2)](https://github.com/acidanthera/OpenCorePkg) |

#### Kext
| Kext | Versions |
|----|----|
| Lilu | [Latest release(1.4.7)](https://github.com/acidanthera/Lilu) |
| VirtualSMC,SMCProcessor,SMCSuperIO| [Latest release(1.1.6)](https://github.com/acidanthera/VirtualSMC) |
| WhateverGreen | [Latest release(1.4.2)](https://github.com/acidanthera/WhateverGreen) |
| AppleALC | [Latest release(1.5.2)](https://github.com/acidanthera/AppleALC) |
| IntelMausi | [Latest release(1.0.3)](https://github.com/acidanthera/IntelMausi) |
| SmallTreeIntel8259x | intel 82599ES Drive |
| USBInjectAll | [Version: 2018-1108](https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/?tab=downloads) |
| USBPower | USB Powered |
| CPUFriend | [Latest release(1.2.1)](https://github.com/acidanthera/CPUFriend) |
| CPUFriendDataProvider | CPU Frequency Conversion |

#### Drivers
| Drivers | Versions |
|----|----|
| HfsPlus | Latest release |
| OpenCanopy | Latest release |
| OpenRuntime | Latest release |


### Where you need to modify

- **Use Tools:** Macserial

![](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC/raw/master/Images/1.png)

- **USB port customization (optional)**
![](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC/raw/master/Images/2.png)
![](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC/raw/master/Images/3.png)

### BIOS Settings
- **BIOS Version** F5

| Disabled | Enabled |
|----|----|
| Fast Boot | Above 4G |
| VT-d | EHCI/XHCI Hand-off |
| CSM | OS type: other types |
### Changelog

#### 05/10 2020
* Repair sleep
* Change SMBIOS to iMacPro1,1

#### 03/10 2020
* Update OpenCore Version 0.6.2

#### 20/9 2020
* Add 10GB SFP+ network card and driver

#### 08/09 2020
* Update macOS Version To Big Sur Beta6
* Update OpenCore 0.6.1
* Update Kext To Latest Version

#### 06/08 2020
* Update macOS Version 10.15.6
* Update OpenCore 0.6.0
* Update Lilu 1.4.6
* Update VirtualSMC,SMCProcessor,SMCSuperIO 1.1.5
* Update WhateverGreen 1.4.1
* Update AppleALC 1.5.1
* Update CPUFriend 1.2.1
* Delete ApfsDriverLoader.efi

#### 22/07 2020
* replace CPU to Intel Xeon E-2278G

#### 11/07 2020
* delete SSDT-RTC-AWAC.aml,The SSDT is not needed, it will cause ACPI ERROR.

#### 13/06 2020
* Opencore version upgraded to 0.5.9
* Kext all upgrade

#### 07/06 2020
* Initial release
