# ESP32 IoT Smart Control Board

[![Hardware License](https://img.shields.io/badge/License-CERN--OHL--W--v2-green.svg)](https://ohwr.org/cern_ohl_w_v2.txt)
[![KiCad Version](https://img.shields.io/badge/KiCad-v10.0-blue.svg)](https://kicad.org/)
[![Status](https://img.shields.io/badge/Status-Design_Completed-success.svg)]()

A compact, high-performance, **4-layer IoT Control Board** powered by the Espressif ESP32 microcontroller. This board is designed for smart automation, edge computing, and wireless sensor networking, combining robust electrical design with modern PCB engineering practices.

---

## 🚀 Features & Specifications

- **Core Microcontroller:** Espressif ESP32 (Wi-Fi & Bluetooth LE connectivity).
- **PCB Architecture:** Advanced **4-layer stackup** for superior EMI/EMC shielding, high signal integrity, and dedicated power/ground planes.
- **Power Delivery:** High-efficiency voltage regulation network with robust input shielding (`Net-(J1-SHIELD)`).
- **Peripherals & I/O:**
  - Integrated status and debugging LEDs (0603 metric footprints).
  - External expansion headers (I2C/SPI/UART accessible via standard 01x04 pin headers).
  - Robust USB/Power connector integration with chassis grounding.
- **Form Factor:** Optimized compact footprint, built using precise 1.6mm standard thickness standards.

---

## 🛠️ Hardware Design Details

### PCB Stackup Configuration
The board utilizes a 4-layer stackup to optimize ground referencing and minimize high-frequency return path loops from the ESP32 RF circuits:
1. **Top Layer (`F.Cu`):** High-speed signal routing and component placement.
2. **Inner Layer 1 (`In1.Cu`):** Dedicated Solid Ground Plane (GND) for noise suppression.
3. **Inner Layer 2 (`In2.Cu`):** Power Routing / Secondary Signal Plane.
4. **Bottom Layer (`B.Cu`):** Auxiliary routing and ground fill.

### Manufacturing Specifications
| Parameter | Value |
|--- |--- |
| **Board Thickness** | 1.60 mm |
| **Copper Layers** | 4 Layers |
| **Minimum Trace / Space** | 0.2 mm / 0.2 mm |
| **Component Finishes** | SMD 0603 (1608 Metric) standard optimization |
| **Design Software** | KiCad v10.0 |

---

## 📂 Repository Structure

```text
├── ESP32_IoT_Board_Design.kicad_pro   # KiCad Project configuration file
├── ESP32_IoT_Board_Design.kicad_sch   # Main Schematic design file
├── ESP32_IoT_Board_Design.kicad_pcb   # 4-Layer PCB Layout file
├── ESP32_IoT_Board_Design.kicad_prl   # Local project workspace preferences
└── README.md                          # Project documentation
```

## 🖼️ Gallery & Previews

### 3D Render (Top & Bottom)

| Top View | Bottom View |
|----------|-------------|
| ![Top View](pictures/3d_top.png) | ![Bottom View](pictures/3d_bottom.png) |

### Schematic Preview

![Schematic Preview](pictures/schematic.png)

---

## 💻 Getting Started / How to Open

To view, edit, or generate manufacturing files (Gerbers) for this project:

1. Download and install **[KiCad EDA v10.0](https://www.kicad.org/)** or higher.
2. Clone this repository to your local directory:

```bash
git clone https://github.com/perfectreda/ESP32_IoT_Smart_Control_Board.git
```

3. Open KiCad, select **Open Project**, and navigate to `ESP32_IoT_Board_Design.kicad_pro`.

---

## 📜 Metadata & License

| Field | Details |
|-------|---------|
| **Designer** | Larbi Moamed Redha |
| **Revision** | Rev 0 |
| **Date** | June 20, 2026 |
| **License** | CERN-OHL-W-v2 |

Distributed under the **[CERN Open Hardware License v2 - Weakly Reciprocal (CERN-OHL-W-v2)](https://ohwr.org/cern_ohl_w_v2.txt)**.  
Feel free to use, modify, and distribute this hardware design with proper attribution.
