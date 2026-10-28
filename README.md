### Crossed-Cantilever DIY 3D Printer (Public Beta)

Welcome to the official repository for the **N3D** a Crossed-Cantilever 3D Printer originally released by [Casual CNC](https://www.youtube.com/@CasualCNC). 

This repository serves as the central hub for the printer's documentation, electronics configuration, toolhead CAD customizations, and community feedback.

### 🛠 Project Status: Open Beta (Phase 1)

This project is currently in **Public Beta**. It is an open-ended, DIY maker project intended for experienced builders who enjoy mechanical troubleshooting, sourcing hardware, and tuning Klipper configurations. 

* **Printer Frame & Core Motion:** Distributed as **STL files only** for this initial phase.
* **Toolhead / Print Head:** Distributed with **Full CAD files (STEP)** to allow for custom community remixes and alternative hardware mounts.

👉 **[Printer Files are also available on Printables.com](https://www.printables.com/model/1892989-crossed-cantilever-3d-printer-diy)** 

### 📐 Baseline Hardware Specifications

### Core Architecture & Dimensions

* **Kinematics:** Cartesian crossed-cantilever
* **Build Volume:** 183.5 × 183.5 × 166 mm (X × Y × Z)
* **Linear Motion:** MGN12H Linear Rails
* **Z-Axis:** Dual Z steppers with 3:1 gear reduction (Block & Tackle with GT2 timing belt)
* **Motion Dynamics:**
  * Max Velocity: 800 mm/s (Max Z Velocity: 150 mm/s)
  * Max Acceleration: 12,000 mm/s² (Max Z Acceleration: 2000 mm/s²)

### Electronics & Motion Control

* **Mainboard:** **BigTreeTech Manta M5P** with **CB1** compute module
* **Firmware:** **Klipper** (Baseline configuration files provided in the [klipper-manta-m5p](/klipper-manta-m5p) folder)
* **Stepper Drivers:** 5× TMC2209 running in UART mode
* **Homing:** Sensorless homing (StallGuard) on X and Y axes; Safe Z Homing via probe
* **Motors:** Standard NEMA 17 Stepper Motors (38 mm body length)
* **Host Cooling:** Temperature-controlled CB1 SoC fan

### Toolhead & Thermal Configuration

* **Hotend:** **E3D Revo Voron PZ Probe** (ATC Semitec 104NT thermistor, up to 270°C)
* **Extruder:** Ender 3 compatible direct drive extruder (1.75 mm filament, 0.40 mm nozzle)
* **Heated Bed:** Ender 3 compatible heated bed with Generic 3950 thermistor (up to 90°C)
* **Bed Leveling:** Integrated Z-probe with 7×7 bicubic mesh leveling compensation
* **Part Cooling:** Dual 4010 high-speed radial blower fans
* **Customization:** The print head STEP file: [/CAD_Toolhead/print-head.step](/CAD_Toolhead/print-head.step)

### 💬 Slicing Recommendations & Printing Tips

* **Build Plate Requirement:** You will need a printer with a build plate of at least **220 × 220 mm** to print the parts.

### Bill of Materials (BOM) (incomplete)

I've sourced my parts mostly from german amazon shop.

| Item                            | Quantity | Notes / Description                              | Sourcing Link                                                                                                 |
|:--------------------------------|:---------|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| **MGN12H Linear Rail (300 mm)** | 3        | 30 cm linear rail with carriage block            | -                                                                                                             |
| **MGN12H Linear Rail (250 mm)** | 4        | 25 cm linear rail with carriage block            | -                                                                                                             |
| **GT2 Timing Belt**             | 1        | 6 mm width belt for motion axes                  | -                                                                                                             |
| **GT2 16T Toothed Idlers**      | 8        | 16-tooth idler pulleys                           | -                                                                                                             |
| **GT2 16 Smooth Idlers**        | 4        | Toothless idler pulleys                          | -                                                                                                             |
| **Miniature Ball Bearings**     | 4        | 685-ZZ (5x11x5 mm)                               | https://www.amazon.de/dp/B092Q5M7FY                                                                           |
| **Nema 17 Stepper Motor**       | 4 + 1    | 38 mm body length                                | -                                                                                                             |
| **Extruder**                    | 1        | Ender 3 compatible extruder                      | https://www.amazon.de/dp/B09ZDQM6P6 (with stepper) <br> https://www.amazon.de/dp/B09H6T3NNT (without stepper) |
| **E3D Revo Voron PZ Probe**     | 1        | Toolhead integrated probe & hotend setup         | -                                                                                                             |
| **Cooling Fan 4010**            | 2        | 4010 axial fans                                  | -                                                                                                             |
| **High Speed 4010 Blowers**     | 2        | 4010 radial blower fans for part cooling         | https://www.amazon.de/dp/B0DMZWJJPJ                                                                           |
| **Heated Bed**                  | 1        | Ender 3 compatible heated bed assembly           | https://www.amazon.de/dp/B08DRJM9S4                                                                           |
| **Magnetic Bed Surface**        | 1        | Ender 3 compatible flexible magnetic build plate | https://www.amazon.de/dp/B07SW9BQKS                                                                           |
| **Mainboard & Compute Kit**     | 1        | BTT Manta M5P + CB1 + 5x TMC2209 stepper drivers | -                                                                                                             |
| **Power Supply**                | 1        | 300 W, 24 V *SLIM* power supply 21x6x2 cm        | https://www.amazon.de/dp/B0F7XF7X4Q                                                                           |
| **Accelerometer Board**         | 1        | BIGTREETECH ADXL345 V2.0 for input shaping       | -                                                                                                             |
| **USB Adapter / Cable**         | 1        | USB connection                                   | https://www.amazon.de/dp/B0FHZN6ZYF                                                                           |
| **Cable Sleeve**                | 1        | Cable management sleeving                        | https://www.amazon.de/dp/B07FW5H57B                                                                           |
| **Square Nuts**                 | 1 pack   | M3 square nuts                                   | https://www.amazon.de/dp/B0F5WBDM3X                                                                           |
| **Fasteners**                   | Various  | M3 screws (assorted lengths)                     | -                                                                                                             |

### 📄 License

This project and all associated files — including 3D models, CAD designs, firmware configurations, documentation, and the Bill of Materials—are licensed under the **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)** license.

You are free to share and adapt the material for any purpose, including commercially, provided you give appropriate credit and distribute your contributions under the same license. See the [LICENSE](LICENSE) file for the full license text.
