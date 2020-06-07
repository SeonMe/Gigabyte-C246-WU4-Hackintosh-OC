# Gigabyte C246 WU4 Hackintosh on OpenCore

## macOS Versions
#### macOS Catalina 10.15.4

## SMBIOS
#### iMac19,1

### What works
- **dGPU** Hardware Accelaration (Final Cut Pro X, VideoProc, Compressor), DRM Content (Apple TV+/Safari Netflix/Amazon Prime)
- **iGPU** Hardware Accelaration (Final Cut Pro X), Apple Sidecar
- **WIFI,Bluetooth** BCM94360CD Required
- **AirDrop, Handoff** BCM94360CD Required
- **USB** All USB3.1/USB2.0 Port
- **Audio** Realtek ALC1220-VB, (layout id: 1)
- **iMessage,FaceTime,Siri** All work fine

### Not works
- Not

### Device Lists
| Device | Model |
|----|----|
| MotherBoard | Gigabyte C246 WU4 |
| CPU | Intel i5 9500 |
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
| OpenCore | [Latest release(0.5.7)](https://github.com/acidanthera/OpenCorePkg) |

#### Kext
| Kext | Downloads |
|----|----|
| Lilu | [Latest release(1.4.3)](https://github.com/acidanthera/Lilu) |
| VirtualSMC,SMCProcessor,SMCSuperIO| [Latest release(1.1.2)](https://github.com/acidanthera/VirtualSMC) |
| WhateverGreen | [Latest release(1.3.7)](https://github.com/bugprogrammer/WhateverGreen) Revision |
| AppleALC | [Latest release(1.4.8)](https://github.com/acidanthera/AppleALC) |
| IntelMausi | [Latest release(1.0.2)](https://github.com/acidanthera/IntelMausi) |
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

![Where you need to modify](https://github.com/SeonMe/ASRock-Hackintosh-OC/raw/master/Images/config_edit.png)

- **Use tools:** Hackintool > PCI

![DeviceProperties_Edit](https://github.com/SeonMe/ASRock-Hackintosh-OC/raw/master/Images/DeviceProperties_Edit.png)

### BIOS Settings
- **BIOS Version** 4.30

| Disabled | Enabled |
|----|----|
| Fast Boot | VT-x |
| CFG Lock (MSR 0xE2 write protection) | Above 4G |
| VT-d | Hyper Threading (If you use a CPU with K) |
| CSM | Execute Disable Bit |
| | EHCI/XHCI Hand-off |
| | OS type: other types |

### Changelog

#### 7/6 2020
* Initial release
