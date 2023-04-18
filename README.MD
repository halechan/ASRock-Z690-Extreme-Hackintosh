# ASRock Z690 Extreme Wifi 6E Hackintosh EFI

EFI Partition and Guidelines for my 13th Intel Hackintosh.

![About](./assets/about_this_mac.png)

![Case](./assets/case.png)

## Changelog

```
0.0.1 - initial release
```

## Hardware

Component | Model
--- | ---
Motherboard | ASRock Z690 Extreme WiFi 6E
CPU | Intel Core i7 13700KF
GPU | YESTON RX6800XT 16G
Memory | KINGBANK 2x32GB DDR4-3600CL18
NVME | Predator SSD GM7000 1TB
Cooler | Thermalright Frozen Notte 360 WHITE ARGB
Case | Segotep Memphis Gaming PC Case White
Power Supply | SAMA Power Supply 750W Gold Black
Wifi/BT | BCM94360CS2 WiFi/BT With AP18 to M.2 Adaptor

## UEFT Settings

- Load UEFI Defaults
- XHCI Hand-off - on (Optional)

### USB Ports Map

Name | U2 Port | U3 Port | Active | Comment
--- | --- | --- | --- | ---
F_USB32_TC_1 | 0x1 | 0x11 | All | Front type-c header
USB_3_4 | 0x9, 0xa | NA | None
USB_1_2 | 0xb, 0xc | NA | None
USB3_5_6, USB3_7_8 | 0x8 | 0x18 | All | Connected with ASMedia ASM1074 hub
M2_WIFI | 0xe | NA | U2 Only |
LED Controller | 0xd | NA | None |
USB3_3 | 0x2 | 0x13 | U2 only | For mouse or keyboard
USB3_4 | 0x3 | 0x12 | U2 only | For mouse or keyboard
USB31_TA_1 | 0x7 | 0x17 | All
USB31_TC_1 | 0x6 | 0x16 | All
USB3_1 | 0x5 | 0x15 | All | ACPI wake-up function is not supported
USB3_2 | 0x4 | 0x14 | All | ACPI wake-up function is not supported

![Motherboard USB Ports](./assets/usb_ports_mb.png)
![Rear Panel USB Ports](./assets/usb_ports_panel.png)

Full usb ports list is defined at [here](./usb_ports.plist).  The 15 actived usb ports is defined in  `Info.plist` of `USBPorts.kext`.

## Benchmarks

![Geekbench](./assets/geekbench.png)

![Geekbench](./assets/geekbench_gpu.png)

![Cinebench](./assets/cinebench_r23.png)
