# Gigabyte C246 WU4 Hackintosh on OpenCore

## macOS Versions
#### macOS Catalina 10.15.5

## SMBIOS
#### iMac19,1

### What works
- **dGPU** Hardware Accelaration (Final Cut Pro X, VideoProc, Compressor), DRM Content (Apple TV+/Safari Netflix/Amazon Prime)
- **iGPU** Hardware Accelaration (Final Cut Pro X), Apple Sidecar
- **WIFI,Bluetooth** BCM94360CD Required
- **AirDrop, Handoff** BCM94360CD Required
- **USB** All USB3.1/USB2.0 Port
- **Audio** Realtek ALC1220-VB, (layout id: 1,PS: ApplcALC doesn't seem to support ALC1220-VB very well, it can make sound, but there will be very serious noise, so it is regarded as abnormal, if you use Bluetooth, this problem can be ignored.)
- **iMessage,FaceTime,Siri** All work fine

### Not works
- Not

### Device Lists
| Device | Model |
|----|----|
| MotherBoard | Gigabyte C246 WU4 |
| CPU | Intel Xeon E-2278G |
| RAM | Asgard LOKI 51℃ 2666 8GB * 4 |
| Video Card | Sapphire RX 5500XT 8GB |
| Sound Card | Realtek ALC1220-VB （MotherBoard）|
| Network Interface Card | PCI-E BCM94360CD (WI-FI + Bluetooth) |
| Hard Disk | Hikvision C2000Pro 1TB NVMe SSD |
| Case | Cooler Master S600 |

### Software Version
#### Boot firmware
| Boot  | Versions |
|----|----|
| OpenCore | [Latest release(0.5.9)](https://github.com/acidanthera/OpenCorePkg) |

#### Kext
| Kext | Downloads |
|----|----|
| Lilu | [Latest release(1.4.5)](https://github.com/acidanthera/Lilu) |
| VirtualSMC,SMCProcessor,SMCSuperIO| [Latest release(1.1.4)](https://github.com/acidanthera/VirtualSMC) |
| WhateverGreen | [Latest release(1.4.0)](https://github.com/bugprogrammer/WhateverGreen) |
| AppleALC | [Latest release(1.5.0)](https://github.com/acidanthera/AppleALC) |
| IntelMausi | [Latest release(1.0.3)](https://github.com/acidanthera/IntelMausi) |
| USBInjectAll | [Version: 2018-1108](https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/?tab=downloads) |
| USBPower | |
| CPUFriend | [Latest release(1.2.0)](https://github.com/acidanthera/CPUFriend) |

#### EFI
| EFI | Downloads |
|----|----|
| ApfsDriverLoader | [Latest release](https://github.com/acidanthera/AppleSupportPkg) |
| HfsPlus | Latest release |
| FwRuntimeServices | [Latest release](https://github.com/acidanthera/AppleSupportPkg) |
| MemoryAllocation | [Latest release](https://github.com/williambj1/OpenCore-Factory/releases/tag/OpenCore-UEFI-Drivers) |


### Where you need to modify

- **Use Tools:** Macserial

![Where you need to modify](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC/raw/master/Images/1.png)

- **Use tools:** Hackintool > PCI

![DeviceProperties_Edit](https://github.com/SeonMe/Gigabyte-C246-WU4-Hackintosh-OC/raw/master/Images/2.png)

### BIOS Settings
- **BIOS Version** F5

| Disabled | Enabled |
|----|----|
| Fast Boot | Above 4G |
| VT-d | EHCI/XHCI Hand-off |
| CSM | OS type: other types |
### Changelog

#### 22/7 2020
* replace CPU to Intel Xeon E-2278G

#### 11/7 2020
* delete SSDT-RTC-AWAC.aml,The SSDT is not needed, it will cause ACPI ERROR.

#### 13/6 2020
* Opencore version upgraded to 0.5.9
* Kext all upgrade

#### 7/6 2020
* Initial release
