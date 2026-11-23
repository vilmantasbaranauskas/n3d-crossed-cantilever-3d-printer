### Crossed-Cantilever DIY 3D Printer (Public Beta)

Welcome to the official repository for the **N3D**, a Crossed-Cantilever 3D Printer originally released by [Casual CNC](https://www.youtube.com/@CasualCNC).

This repository serves as the central hub for the printer's documentation, electronics configuration, toolhead CAD customizations, and community feedback.

### Purpose of This Printer

**This is mostly a DIY playground printer, not a machine for primary printing needs.** If you need a printer for everyday work, consider other options.

**The distinctive design and look are the main draw.** Instead of a traditional frame and motion system, the N3D is built around a crossed-cantilever layout. Its gantry is carried by cantilever arms anchored on two perpendicular sides, giving the printer a visually striking, open look.

* **Built for curiosity and learning:** The project was not made to solve an engineering problem or to outperform traditional designs. It is a personal experiment to learn from and to see something unusual in motion.
* **Not a CoreXY replacement:** It is not meant to replace CoreXY or conventional Cartesian frame printers. Cantilever arms lose stiffness as they grow longer, so the current build is already close to its practical size limit, and the cantilevers add vibration and flex.
* **Open-frame access:** The open layout leaves the build area easy to reach from the front side and lets the printer sit neatly in a corner. Some describe it as "a perfect desktop corner printer."
* **Block-and-tackle Z-axis:** The Z-axis uses a dual block-and-tackle system with a GT2 timing belt for a 3:1 reduction. This approach is extremely rare in 3D printers, which surprises the author because it is simple to implement and works very well.

**Build it if** you enjoy mechanical troubleshooting, want to explore an unconventional design, and accept its rigidity limits. **Skip it if** you need a reliable, high-precision printer for regular printing.

### Project Status: Open Beta (Phase 1)

This project is currently in **Public Beta**. It is an open-ended, DIY maker project intended for experienced builders who enjoy mechanical troubleshooting, sourcing hardware, and tuning Klipper configurations. 

* **Printer Frame & Core Motion:** Distributed as **STL files only** for this initial phase.
* **Toolhead / Print Head:** Distributed with **Full CAD files (STEP)** to allow for custom community remixes and alternative hardware mounts.

👉 **[Printer Files are also available on Printables.com](https://www.printables.com/model/1892989-crossed-cantilever-3d-printer-diy)** 

🎥 **[Assembly Video Part 1 on YouTube](https://www.youtube.com/watch?v=z4k570kHDuc)**

The **Beta 2** model files include the fixed and updated parts. Follow the [Part 1 assembly guide](ASSEMBLY.md) while building; the [3D models README](3d-models/README.md) lists the filaments and print settings used in the assembly video.

### Core Architecture & Dimensions

* **Kinematics:** Cartesian crossed-cantilever
* **Build Volume:** 183.5 × 183.5 × 166 mm (X × Y × Z)
* **Linear Motion:** MGN12H Linear Rails
* **Z-Axis:** Dual Z steppers with 3:1 reduction (block-and-tackle with GT2 timing belt)
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

### Slicing Recommendations & Printing Tips

* **Build Plate Requirement:** You will need a printer with a build plate of at least **220 × 220 mm** to print most parts.
* **Gantry Minimum Size:** The minimum required bed size for printing the gantry as a single part is around **242 × 242 mm**.

### Bill of Materials (BOM) (partial)

Parts were sourced primarily from Amazon.de.

| Item                            | Quantity | Notes / Description                              | Sourcing Link                                                                                                 |
|:--------------------------------|:---------|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| **MGN12H Linear Rail (300 mm)** | 3        | 30 cm linear rail with carriage block            | -                                                                                                             |
| **MGN12H Linear Rail (250 mm)** | 4        | 25 cm linear rail with carriage block            | -                                                                                                             |
| **GT2 Timing Belt**             | 1        | 6 mm width; approximately 115 cm for each Z-axis side | -                                                                                                        |
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
| **M3 Inserts**                  | 23+      | 15 Base + 4 Adapter + 4 Tensioners               |                                                                                                               |
| **M4 Inserts**                  | 4        | 3 Base + 1 Cover                                 |                                                                                                               |
| **Square Nuts**                 | 1 pack   | M3 square nuts                                   | https://www.amazon.de/dp/B0F5WBDM3X                                                                           |
| **Fasteners**                   | Various  | M3 screws (assorted lengths)                     | -                                                                                                             |
| **Rubber Grip Tape**            | As needed| Cut to fit under the base feet for grip and damping; rubber rail stoppers are an alternative | -                                           |
| **Zip Ties**                    | 2        | Secure the power-supply cable                     | -                                                                                                             |
| **Superglue**                   | As needed| Gantry joints, printed pulleys, and grip tape     | -                                                                                                             |

### License

This project and all associated files — including 3D models, CAD designs, firmware configurations, documentation, and the Bill of Materials—are licensed under the **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)** license.

You are free to share and adapt the material for any purpose, including commercially, provided you give appropriate credit and distribute your contributions under the same license. See the [LICENSE](LICENSE) file for the full license text.
