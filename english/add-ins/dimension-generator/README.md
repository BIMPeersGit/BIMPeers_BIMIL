---
description: One-click centerline and polyline dimensioning for AutoCAD Model Space.
hidden: true
---

# Dimension Generator

Dimension Generator is an AutoCAD add-in that reads the centerlines and closed polylines in Model Space and places clean, consistent dimensions in a single click. Pick the objects (or a whole layer), choose how the dimensions should look, and Generate — it works out the spacing, grouping, and placement for you, so you skip the repetitive manual dimensioning.

#### Commands

| Command   | Alias         | Action                                                          |
| --------- | ------------- | -------------------------------------------------------------- |
| `DIMGEN`  | `BP_DIM`      | Open the Dimension Generator window                            |
| `DIMFAST` | `BP_DIM_FAST` | Generate dimensions for the selected objects with the last-used settings |

The same actions are available on the **BIMIL** ribbon tab as the **Dimension Generator** and **Generate Last** buttons.

#### Features

* [**Centerline Dimension**](centerline-dimension.md)**:**\
  Reads the selected centerlines (lines / open polylines), automatically sorts them by axis, and dimensions the spacing between adjacent centerlines (Detail) together with the overall span (Overall). Parallel diagonal centerlines are grouped and measured with rotated dimensions.
* [**Polyline Dimension**](polyline-dimension.md)**:**\
  Dimensions each edge of a closed polyline outline — rectangles and irregular polygons alike. Choose the **Method** (Aligned vs. Linear) and **Direction** (Outside vs. Inside).
* [**Generate Last**](generate-last.md)**:**\
  Reuse your most recent settings on a new selection straight from the ribbon, without opening the window.
* **Two ways to pick targets:** *Select Objects* to dimension only the objects you pick, or *Select by Layer* to dimension every line and polyline on a chosen layer.
* **Dimension style & layer:** Choose which dimension style to apply — with a quick Edit shortcut to the style manager — and which layer the dimensions are placed on.
* **Preview help:** The **?** preview shows exactly how the current mode and option combination will look before you Generate.

#### Notes

* Centerline mode needs at least two centerlines; closed polylines and unsupported objects in the selection are skipped, and the skipped count is reported.
* Polyline mode needs a closed outline. A gap smaller than the drawing tolerance is still treated as closed, and tiny sub-tolerance segments are not dimensioned.
* Dimensions identical to ones already at the same spot are skipped, so re-running never creates duplicates.
* If the dimension layer is frozen, off, or locked, the result message tells you so you can make the new dimensions visible or editable.
* Your settings are saved to file, so your last configuration is restored the next time you open the window — even after restarting AutoCAD.
* Every run reports its outcome in the window's status line: success, partial (something was skipped), or failure.
