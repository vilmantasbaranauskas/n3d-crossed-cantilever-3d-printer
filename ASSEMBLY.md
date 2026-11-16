### Part 1 Assembly Guide

This guide covers the base, gantry, top frame, and Z-axis block-and-tackle assembly shown in [Assembly Video Part 1](https://www.youtube.com/watch?v=z4k570kHDuc). Use the Beta 2 model files, which include updated and fixed parts. Print details are in the [3D models README](3d-models/README.md).

### Filaments and Preparation

The video build uses four filaments:

- **Spectrum FlameGuard PLA, Technical Red:** Base, gantry, top frame, and other frame parts. The filament is rated UL 94 V-0; it was selected in part because the base houses electrical components.
- **Sunlu ABS-FR:** Heated-bed adapter and print head. This filament is also rated UL 94 V-0.
- **Tinmorry PETG-CF:** Structural parts subject to high loads, including the printed GT2 pulleys.
- **Overture TPU 95A:** Dampers.

The prints in the video were not perfectly calibrated and showed some under-extrusion and imperfect layer adhesion. The settings are the creator's build record rather than a definitive recommendation; refer to the [print settings and observations](3d-models/README.md#print-settings-used-for-assembly-video). Superglue was used to help where needed.

### Base

#### Fit the feet and inserts

1. Start with `base.3mf`. The base can warp at the corners during printing. The Beta 2 warp-correction parts (`warp-correction-1.3mf` and `warp-correction-2.3mf`) help hide corner warping and level the printer.
2. Cut self-adhesive rubber grip tape to fit the feet and glue it in place with superglue, checking that the corners stay down. Rubber stoppers from linear rails are an alternative. Place the base firmly on the work surface.
3. Install 15 M3 threaded inserts and 3 M4 threaded inserts in the base, then install one M4 threaded insert in `cover.3mf`.

#### Install the power supply and Z-axis motors

1. Before installing the power supply, read the safety disclaimer shown in the assembly video. The power supply contains hazardous high-voltage areas. Secure its cable with two zip ties and cover the high-voltage area with `power-supply-cover.3mf`, then fasten the supply in place.
2. Attach the three vertical rails to the base.
3. Print two `gt2-15t.3mf` pulleys in PETG-CF for the Z-axis. The pulley ends are asymmetric: the side that was against the build plate faces outward when installed. Secure each pulley to its motor shaft with a small amount of superglue to prevent backlash. This makes the pulley non-reusable; it must be broken to remove. Clean excess glue from the shaft before fitting the ball bearing.
4. Prepare two `timing-belt-holder-bottom.3mf` parts by using the slicer's clone and mirror functions to create the left and right versions. Fit a 16T idler in each and secure it with an M3 screw; tighten gently to avoid over-tensioning the idler.
5. Attach a TPU damper to the inner side of each bottom timing-belt holder. Fit the NEMA 17 dampers into the base and mount the left and right Z-axis steppers.

### Gantry

#### Print and join the gantry

1. On a 220 × 220 mm bed, print `gantry-left.3mf`, `gantry-center.3mf`, and `gantry-right.3mf` separately. Use gyroid infill and 4 wall loops; add supports for the center and a brim and supports for the left and right pieces. A single-piece gantry needs a larger bed of about 242 × 242 mm.
2. Align the three pieces so the openings for the linear-rail carriages face down. Depending on printer calibration, a clamp or vise may be needed to bring the joints together.
3. Apply superglue, keep the pieces slightly separated when sliding them together so glue does not spill onto visible surfaces. Let that side dry before joining the other side. The glued fit is impossible to reverse, so align properly.

#### Fit idlers, motors, and rails

1. Install four toothless idlers in the gantry. Washers are not needed because the spacers are integrated into the printed design. Tighten the M3 screws gently.
2. Assemble the 16T pulleys and ball bearings as for the Z-axis steppers. Fit the NEMA 17 dampers and mount each motor using three dampered M3 screws.
3. Insert square nuts into the hidden linear-rail mounting locations, using the rail carriages to hold the nuts in place during installation. The left and right sides are asymmetric, so install the additional hidden nut on the right side as shown in the video. The rail mounting hole nearest each pulley is intentionally left without a screw because a screw there would collide with the motor. Square nuts are used here instead of threaded inserts, which loosened under load over time.
4. Mount the gantry onto the vertical rails. Install the third carriage on its rail and use a stopper so it cannot slide off accidentally. Bring the right side on slightly before the left, and align the back rail with the opening at the top of the gantry. Push the back-rail carriage into the gantry and secure it with a screw. The gantry should then move relatively freely on the vertical axis.

### Top Frame

1. Print `top-frame.3mf` with a brim. Placement on a 220 × 220 mm plate is tight; adjust the position manually to find the small area where it fits.
2. Install four 16T idlers in the top frame, then push it onto the rails. Check that the gantry moves smoothly.

### Block and Tackle

1. Prepare approximately 115 cm of 6 mm-wide GT2 belt for each side.
2. To feed the belt through the idlers, place a small piece of paper over its tip and push it through.
3. Attach one end of the belt to the gantry with a belt holder. Route it over and under the idlers in the up-and-down pattern shown in the video.
4. Attach the belt to the belt tensioner, secure it with the plug, and slide the assembled tensioner into the gantry. Adjust tension with the tensioner screw.
5. Repeat the routing and attachment for the other side. The video tunes belt tension by ear and does not specify a target tension value.

### End of Part 1

At this point, the base, gantry, top frame, and Z-axis belts are assembled. Beta 2 model files are available from the [project's Printables page](https://www.printables.com/model/1892989-crossed-cantilever-3d-printer-diy) and this GitHub repository.
