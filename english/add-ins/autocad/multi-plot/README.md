---
description: Plot matching drawing frames from one or more DWG files with one setup.
hidden: true
---

# Multi Plot

Multi Plot plots drawing frames from multiple DWG files using a single reference frame and AutoCAD page setup. Choose a frame shape, add the DWG files to process, confirm how many matching frames were found, then start the batch plot from one window.

#### Commands

* `BP_MTP` / `MTP`: Open the Multi Plot window.

The same action is available from the **Multi Plot** button on the **BIMIL** ribbon tab.

#### How to use

1. Run **Multi Plot** from the BIMIL ribbon, or type `MTP`.
2. Choose a **Plot Setup** from the current drawing, or click **Edit** to open AutoCAD Page Setup.
3. Register a **Reference Frame** by selecting an object in the current drawing or choosing a reference DWG.
4. Click **Add DWG** and add the drawings you want to plot.
5. Check the **Frames** and **Status** columns to confirm that each DWG contains matching frames.
6. Set the copy count for each DWG as needed.
7. Choose an output folder when the selected plot device creates files.
8. Click **Start Plot**.

#### Frame detection

Multi Plot uses the reference frame to find matching frames in each target DWG. Supported frame objects include block references, curves, and regions with valid geometric extents.

When a reference object is selected from the current drawing, Multi Plot stores its object type, layer, size, and block name when available. When a reference DWG is selected, the largest usable frame in that file is used, and the file must contain exactly one matching frame.

#### Output

Multi Plot uses the selected AutoCAD Model page setup for device, media, rotation, plot style, lineweight, plot style, and transparency settings. File output devices such as PDF, DWF, JPG, PNG, and XPS use the selected output folder. Non-file devices print directly through the selected plot device.

#### Notes

* Multi Plot scans each target DWG before plotting and skips files that do not contain matching frames.
* Matching frames are ordered from top to bottom and left to right.
* Duplicate or nested frames are filtered so the same sheet is not plotted repeatedly.
* The first and last pages are not selected manually; each matching frame becomes a plot window.
* AutoCAD background plotting is temporarily disabled during the batch and restored after plotting finishes.
