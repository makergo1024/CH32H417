# CH32H417

English overview for the CH32H417 embedded microcontroller example repository.

## Overview

The CH32H417 is a connected general-purpose microcontroller from WCH. It uses a dual-core QingKe RISC-V design:

- RISC-V5F core up to 400 MHz
- RISC-V3F core up to 144 MHz
- 960 KB Flash and 896 KB SRAM
- 3.3 V nominal system supply

The device integrates high-speed interfaces, connectivity peripherals, analog functions, timers, and display-related hardware. This repository includes WCH EVT example projects for the supported peripherals.

## Notable peripherals

- USB 3.2 Gen 1 controller and PHY
- USB 2.0 high-speed and full-speed controllers
- 10/100 Mbps Ethernet MAC and PHY
- Type-C and USB Power Delivery controller/PHY
- SerDes high-speed isolated transceiver
- SD/EMMC controller, DVP camera interface, UHSIF, FMC, and PIOC
- Up to 8 USARTs, I3C, 4 I2C buses, 4 SPI buses, 2 QSPI buses, 2 I2S interfaces, and 3 CAN controllers
- Two 12-bit ADC units (up to 5 Msps), one 10-bit HSADC (up to 20 Msps), DACs, op amps, comparators, and TouchKey inputs

Refer to the included datasheet in `docs/` and the official WCH documentation for electrical limits, pin assignments, and the full peripheral specification.

## Repository layout

| Path | Contents |
| --- | --- |
| `EVT/` | WCH evaluation and peripheral example projects |
| `EVT/EXAM/` | Examples grouped by peripheral, including ADC, CAN, Ethernet, timers, USART, USB, USB PD, and more |
| `docs/` | Device documentation, including the CH32H417 datasheet |
| `LICENSE` | MIT license |

Many examples provide separate `V3F` and `V5F` project directories for the two cores. Project and workspace files use the MounRiver Studio formats (`.wvproj` and `.wvsln`).

## Getting started

1. Install [MounRiver Studio](http://www.mounriver.com/download) and the WCH tooling appropriate for your operating system.
2. Select an example under `EVT/EXAM/` for the peripheral and core you want to evaluate.
3. Open the corresponding `.wvsln` workspace or `.wvproj` project in MounRiver Studio.
4. Confirm the target board, clock configuration, debugger connection, and pin configuration against the datasheet and board schematic before programming hardware.
5. Build, flash, and validate the example with the relevant WCH tools.

Examples are vendor reference material. Review clock, GPIO, power, and board-specific configuration before reusing them in a product.

## Related resources

- [CH32H417 product page](https://www.wch.cn/products/CH32H417.html)
- [CH32H417 EVT package](https://www.wch.cn/downloads/CH32H417EVT_ZIP.html)
- [WCHISPTool](https://www.wch.cn/downloads/WCHISPTool_Setup_exe.html)
- [MounRiver Studio](http://www.mounriver.com/download)

## License

This repository is distributed under the [MIT License](LICENSE). Keep the included copyright and license notices when copying or redistributing the material.

