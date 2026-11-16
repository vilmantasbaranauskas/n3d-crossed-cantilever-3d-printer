### 3D Printable Models

This directory contains the 3D model files (`.3mf`) required to assemble the N3D Crossed-Cantilever 3D printer.

You will need a printer with a build plate of at least **220 × 220 mm** to print the parts.

### Gantry Configuration Options

The gantry component is provided in two options to accommodate different printer build volumes and user preferences. The minimum required bed size for printing the gantry as a single part is around **242 × 242 mm**.

* **Single Part:** `gantry-as-one-part.3mf`
* **As 3 Parts:** `gantry-left.3mf`, `gantry-center.3mf` and `gantry-right.3mf`

### Filaments Used For Assembly Video

🎥 **[Assembly Video Part 1 on YouTube](https://www.youtube.com/watch?v=z4k570kHDuc)**

#### PLA-FR (Spectrum FlameGuard PLA)

- base (`base.3mf`)
- 1 + 1 mirror timing-belt-holder-bottom (`timing-belt-holder-bottom.3mf`)
- 2x transformer-holder (`transformer-holder.3mf`)
- manta-m5p-adapter-left / manta-m5p-adapter-right (`manta-m5p-adapter-left.3mf`, `manta-m5p-adapter-right.3mf`)
- gantry-left / gantry-center / gantry-right (`gantry-left.3mf`, `gantry-center.3mf`, `gantry-right.3mf`)
  or alternatively gantry as a single part (`gantry-as-one-part.3mf`)
- belt-tensioner (`belt-tensioner.3mf`)
- belt-tensioner-plug (`belt-tensioner-plug.3mf`)
- belt-holder-top (`belt-holder-top.3mf`)
- top-frame (`top-frame.3mf`)
- cover (`cover.3mf`)
- fan-duct-simple (`fan-duct-simple.3mf`)

#### ABS-FR (Sunlu)

- heated bed adapter (`hotbed-adapter.3mf`)
- print-block-for-e3d-revo-voron (`print-block-for-e3d-revo-voron.3mf`)
- print-block-front-for-e3d-revo-voron (`print-block-front-for-e3d-revo-voron.3mf`)

#### PETG-CF (Tinmorry)

- 2x gt2-15t (`gt2-15t.3mf`)
- 2x gt2-16t (`gt2-16t.3mf`)
- 2x gantry-xy-lr-0 (`gantry-xy-lr-0.3mf`)
- timing-belt-holder-xy (`timing-belt-holder-xy.3mf`)
- timing-belt-holder-xy-tentioner (`timing-belt-holder-xy-tentioner.3mf`)
- gt2-plug (`gt2-plug.3mf`)

#### TPU (Overture)

- 2x timing-belt-holder-bottom-damper (`timing-belt-holder-bottom-damper.3mf`)
- 4x nema17-damper-2.8-1.8mm (`nema17-damper-2.8-1.8mm.3mf`)
- fan-damper (`fan-damper.3mf`)
- 6x m3-damper (`m3-damper.3mf`)

### Changelog

All notable changes, model fixes, and revisions for the printable 3D models are documented in this section.

#### Beta 2 - 2026-11-15
- **Fixed**: Length of `gt2-15t.3mf` and `gt2-16t.3mf`.
- **Fixed**: Height of `m3-damper.3mf`.
- **Added**: Power supply cover for safety (`power-supply-cover.3mf`).
- **Added**: Adapter-based mainboard mounting, allowing boards other than the Manta M5P to be used. Two new parts: `manta-m5p-adapter-left.3mf` and `manta-m5p-adapter-right.3mf`.
- **Added**: Two new parts for warp correction of the base corners: `warp-correction-1.3mf` and `warp-correction-2.3mf` (3 for the front and side corners and 1 for the back).
- **Changed**: `base.3mf` now uses the Manta M5P adapters for mainboard mounting.
- **Removed**: Technical text imprint on `gantry-xy-lr-0.3mf`.

#### Hotfix - 2026-11-01
- **Fixed**: `timing-belt-holder-bottom.3mf` broken model issue in Beta 1.

#### Beta 1 - 2026-10-27
- Initial release of Beta 1 printable 3D models.
