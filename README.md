# Gigabyte C246 WU4 Hackintosh on OpenCore

## macOS Versions
#### macOS Big Sur 11.3(20E232)

## SMBIOS
#### MacPro7,1

### What works
- **WIFI,Bluetooth,AirDrop, Handoff** BCM94360CD Required
- **USB** All USB3.1/USB2.0 Port
- **Audio** Realtek ALC1220-VB, (layout id: 7)
- **Siri,iMessage,FaceTime** Work fine
- **DRM** Apple TV+/Safari Netflix(1080P)/Amazon Prime

### Not works
- **NO**

### How to use

1.[Download EFI](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC/archive/master.zip)

2.[Look here](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html)

### Device Lists
| Device | Model |
|----|----|
| MotherBoard | Gigabyte C246 WU4 |
| CPU | Intel Xeon E-2278G |
| RAM | Samsung 8GB DDR4 2666MHz ECC Memory Module * 4 |
| Video Card | Sapphire RX 5500XT 8GB |
| Sound Card | Realtek ALC1220-VB （MotherBoard）|
| Network Interface Card | PCI-E BCM94360CD (WI-FI + Bluetooth) |
| Optical Network Card | Intel X520-DA2 2-Port 10GbE FCoE SFP+ NIC |
| Thunderbolt Card | Gigabyte GC-TITAN-RIDGE ver.1|
| FireWire Expansion Card | PCI 1394A+1394B FireWire 800 |
| Hard Disk | Hikvision C2000Pro 1TB NVMe SSD |
| Case | Cooler Master S600 |

### Software Version
#### Boot firmware
| Boot  | Versions |
|----|----|
| OpenCore | [Latest release(0.6.8)](https://github.com/acidanthera/OpenCorePkg) |

#### Kext
| Kext | Versions |
|----|----|
| Lilu | [Latest release(1.5.2)](https://github.com/acidanthera/Lilu) |
| VirtualSMC,SMCSuperIO,SMCProcessor | [Latest releases(1.2.2)](https://github.com/RehabMan/OS-X-FakeSMC-kozlek) |
| AppleALC | [Latest release(1.5.9)](https://github.com/acidanthera/AppleALC) |
| IntelMausi | [Latest release(1.0.5)](https://github.com/acidanthera/IntelMausi) |
| SmallTreeIntel8259x | [intel 82599ES Drive](https://small-tree.com/) |
| USBPorts | Custom made |
| USBPower | USB Powered (MacPro7,1)|
| CPUFriend | [Latest release(1.2.3)](https://github.com/acidanthera/CPUFriend) |
| CPUFriendDataProvider | CPU Frequency Conversion |
| NVMeFix | [Latest release(1.0.6)](https://github.com/acidanthera/NVMeFix) |

#### Drivers
| Drivers | Versions |
|----|----|
| HfsPlus | [Latest release](https://github.com/acidanthera/OcBinaryData) |
| OpenCanopy | [Latest release](https://github.com/acidanthera/OpenCorePkg) |
| OpenRuntime | [Latest release](https://github.com/acidanthera/OpenCorePkg) |


### Where you need to modify

- **Use Tools:** Macserial

![](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC/raw/master/Images/1.png)

### USB port customization (optional)

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

#### 30/5 2021
* Update OpenCore Version 0.6.8
* Delete FakeSMC
* Add VirtualSMC

#### 10/11 2020
* Delete WhateverGreen.kext
* Add FakeSMC
* Change SMBIOS to MacPro7,1
* Update All Kext Latest Release
* Update OC 0.6.3

#### 23/10 2020
* Add NVMeFix.kext

#### 05/10 2020
* Repair sleep
* Update All Kext Version
* Cange SMBIOS iMacPro1,1

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
