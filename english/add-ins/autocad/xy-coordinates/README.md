---
description: >-
  Extract the X·Y coordinates of a clicked point and annotate them on the
  drawing.
---

# XY Coordinates

XY Coordinates reads the X and Y of any point you click and writes it into the drawing as a coordinate label. Click the point, drag the label to where you want it — a live preview shows the leader and text as you move — and it drops an MText label with the leader, base-point marker, and underline you set up. Keep clicking to annotate point after point until you press ESC.

#### Commands

| Command                 | Alias                  | Action                                    |
| ----------------------- | ---------------------- | ----------------------------------------- |
| `XYCoordinates`         | `XY`, `BP_XY`          | Pick a point and annotate its coordinates |
| `XYCoordinatesSettings` | `XYS`, `BP_XY_SETTING` | Open the settings window                  |

The same actions are on the **BIMIL** ribbon tab as the **XY Coordinates** and **Settings** buttons.

#### How to use

1. **Set it up** — open **Settings**, choose how the label should look, and click **Save**. See [Settings](settings.md) for each option.
2. **Click a base point** — its X and Y are read (based on the current UCS) and remembered.
3. **Place the label** — drag to position it. A gray preview of the text and leader follows the cursor, and the label automatically unfolds away from the base point.
4. **Click to drop it** — the coordinate text plus any leader, base-point marker, and underline are placed on the current layer.
5. **Repeat** for more points; press **ESC** to finish.

#### Notes

* The coordinate text is fixed at the moment you place it — moving the leader or marker afterward does not change the value.
* Labels are drawn on the current layer with BYLAYER color.
* With **Group line and text** enabled, the text and its lines/marker are grouped so they select and move together.
* Settings are saved to file, so they are restored the next time you use the add-in — even after restarting AutoCAD. If you have never saved any, the command runs with the default settings.

