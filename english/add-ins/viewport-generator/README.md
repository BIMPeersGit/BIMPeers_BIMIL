---
description: Auto-generate layouts and viewports from polyline frames in AutoCAD Model Space.
hidden: true
---

# Viewport Generator

Viewport Generator is an AutoCAD plug-in that automatically creates layout tabs and viewports from polygon (polyline) frames drawn in Model Space, using a chosen template. It runs from the `VPG` (or `BP_VPG`) command, which opens the main window, and supports three generation methods so frames can be turned into viewports directly, arrayed into a grid, or placed interactively on screen.

#### Commands

- **`VPG`** (or **`BP_VPG`**): Opens the main Viewport Generator window.

#### Features

- **Plan Frames (direct frame mode):**\
  The default mode that creates viewports in one pass from pre-drawn polyline frames. It faithfully follows not only rectangles but also irregular polygons such as star or stair shapes.
  - **Directly Select:** Click `[Select]` and drag on the drawing to pick the polygon objects to turn into viewports.
  - **Select by Layer:** Type part of a layer name into `Target Layer` to filter, then load all polygons on the matching layers at once.
  - **Snap to Orthogonal:** For rotated frames, rotates the viewport in 90° steps so the drawing inside faces upright.
  - **Use Bounding Box:** Ignores the frame's rotation and creates the viewport from the smallest axis-aligned rectangle that fully contains the polygon.
- **Array (Grid) mode:**\
  Copies a single source frame into a grid of viewports by count and spacing. Click `[Select Base Frame]` and pick one source polyline, then enter `Rows` and `Cols` for the desired viewport counts and `X Offset` / `Y Offset` for the spacing between objects. When spacing is hard to type, click the ruler button to measure the gap between two points on the drawing — the sign (+ / −) is applied automatically based on the measurement direction (up/down/left/right).
- **Interactive mode:**\
  Places viewports freely by clicking on screen, like stamping. On start you are moved to the source layout tab; click a source viewport border (or polyline) once to copy its size, then move the mouse in Model Space and click each target center in turn. Command-line options let you keep the frame in the mouse direction (`K`) or rotate it (`R`); press `ESC` or `Enter` to finish.
- **Common Output Settings:** Criteria applied whenever viewports are generated, in every mode.
  - **Sorting Direction:** Determines the order in which layout tabs are created when frames are scattered across the drawing (e.g. Z, N, Reverse N, Reverse Z).
  - **Viewport Scale (1:X):** Sets the drawing scale of the generated viewports (e.g. 1/50, 1/100, 1/200).
  - **Source Layout:** Selects the source layout template (containing the title block, etc.) to base new layout tabs on.
  - **Sheet Prefix / Start:** Naming rule for the newly created layout tabs (e.g. prefix `Plan_` and start `1` produces `Plan_1`, `Plan_2`, …).

#### Notes

- Plan Frames handles arbitrary polygon shapes, so star, stair, and other non-rectangular frames are reproduced exactly.
- In Interactive mode the source viewport size is copied from the layout tab you set before running, and viewports are created sequentially at each clicked center.
- Supported on AutoCAD 2023–2027.
