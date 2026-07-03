---
description: Auto-generate layouts and viewports from polyline frames in AutoCAD Model Space.
hidden: true
---

# Viewport Generator

Viewport Generator is an AutoCAD add-in that turns the polyline frames in your Model Space into finished layout tabs and viewports. Point it at your frames, choose a source layout to copy the title block and settings from, set the scale and sheet names, and it builds every sheet for you — following the true shape of each frame, rectangular or not. It offers three ways to generate, so you can dimension existing frames directly, fan a single frame out into a grid, or drop viewports by hand.

#### Commands

| Command | Alias                  | Action                             |
| ------- | ---------------------- | ---------------------------------- |
| `VPG`   | `BP_VPG`, `VIEWPORTGEN`| Open the Viewport Generator window |

#### Features

* [**Plan Frames**](plan-frames.md)**:**\
  The default mode — creates viewports in one pass from pre-drawn polyline frames, pick them directly or by layer. Follows irregular shapes (L-shapes, stairs, etc.) exactly.
* [**Array (Grid)**](array-grid.md)**:**\
  Copies a single base frame into a grid of viewports by row/column count and spacing.
* [**Interactive**](interactive.md)**:**\
  Places viewports by clicking in Model Space, one after another, like stamping.
* **Common Output Settings:** Applied to every mode.
  * **Sorting Direction:** The order in which sheets are created when frames are scattered across the drawing (Z, N, Reverse N, Reverse Z patterns).
  * **Viewport Scale (1:X):** The drawing scale of the generated viewports (e.g. 1:50, 1:100, 1:200).
  * **Source Layout:** The existing layout tab — with its title block and viewport settings — that each new sheet is based on.
  * **Sheet Prefix / Start:** The naming rule for new sheets (e.g. prefix `Plan_` and start `1` produces `Plan_1`, `Plan_2`, …).

#### Notes

* Every mode builds on a **Source Layout**, so set up one template sheet (title block, viewport scale) before running.
* Irregular polygon frames are reproduced exactly — stars, stairs, and other non-rectangular shapes included.
* Your settings are saved to file, so the window reopens with your last configuration — even after restarting AutoCAD.
