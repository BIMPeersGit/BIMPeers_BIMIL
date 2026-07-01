---
description: One-click, accurate dimensioning for AutoCAD Model Space
hidden: true
---

# Dimension Generator

Dimension Generator is an AutoCAD plug-in that quickly and accurately places dimensions based on the centerlines and closed polylines (outlines) in Model Space. With a single click on the whole drawing or on a selected set of objects, it generates a consistent set of 1st-tier (outer) and 2nd-tier (overall) dimensions. It runs from the `DimensionGenerator` window or, without a window, directly on the current selection with `DimensionGeneratorLast`, and is also available from the **BIMIL** ribbon tab through the Dimension Generator panel (`Open Window` / `Apply Last`).

#### Commands

- **`DimensionGenerator`:** Opens the main Dimension Generator window.
- **`DimensionGeneratorLast`:** Skips the window and immediately dimensions the selected objects using the exact settings from the last Apply.
- **Ribbon menu:** Launch from the **BIMIL** tab → **Dimension Generator** panel using the `Open Window` / `Apply Last` buttons.

#### Features

- **Centerline Dimension:**\
  Recognizes pre-drawn lines and open polylines as centerlines and dimensions them in one pass. Centerlines are automatically classified into vertical / horizontal axes to dimension the spacing between adjacent centerlines (1st tier), and collinear centerlines are grouped so a rotated dimension measures the perpendicular spacing.
- **Outer Dimension:**\
  Dimensions the outer edges of a closed polyline (outline), handling not only rectangles but also irregular polygons with diagonal edges.
  - **Placement (Inside / Outside):** Place dimensions either outside or inside the polyline.
  - **Per-edge style (Aligned / Linear):** Dimension each edge with an Aligned dimension parallel to the edge, or decompose it into horizontal / vertical components as separate X/Y dimensions.
  - **Multi dimension:** Consecutive outer dimensions that touch each other are grouped and an additional summed dimension is added above them; empty gaps are split automatically.
  - **Polyline width dimension:** Places a length dimension for each polyline.
- **Common Settings:** Criteria applied whenever dimensions are created, in every mode.
  - **Target selection:** _Directly Select_ to click and drag objects on the drawing (pickfirst selections made before running are also recognized), or _Select by Layer_ to filter by layer name and load all matching objects at once.
  - **Offset:** Distance from the object to the first (1st-tier) dimension line.
  - **Dimension Style:** Choose which dimension style defined in the current drawing to apply.
  - **Output Layer:** Choose the layer the generated dimensions are placed on; defaults to the current layer if left unset.
- **Preview tooltip:** Hover over the `?` button at the bottom of the window to preview the dimensioning result for the current mode and option combination. The preview updates as you change options, so the output shape can be confirmed before Apply.
- **Apply Last:** Settings are remembered after one Apply, so you can reapply the same settings to a new selection without opening the window, via the ribbon `Apply Last` button or the `DimensionGeneratorLast` command.

#### Notes

- At least 2 centerlines are required to place a Centerline dimension; closed polylines and unsupported objects are skipped automatically, and the skipped count is reported in the status message.
- Even if an outline is not perfectly closed, a gap within tolerance (0.01) is treated as a closed polyline.
- If an identical dimension already exists at the same location, it is skipped to prevent duplicates.
- If the output layer is frozen or locked, it is temporarily released before dimensioning and restored afterward; a turned-off layer triggers a warning that dimensions may not be visible.
- The output layer and dimension style are validated before dimensioning — if there is a problem the process stops without modifying the drawing.
- The last input values are restored when the window is reopened within the same AutoCAD session.
- The execution result is shown with a status icon at the bottom of the window: Success, Partial success (warning), or Failure.
- Supported on AutoCAD 2023–2027 (2023/2024 on .NET Framework 4.8, 2025/2026 on .NET 8.0, 2027 on .NET 10.0), deployed as an Autodesk bundle under `%APPDATA%\Autodesk\ApplicationPlugins\`.
