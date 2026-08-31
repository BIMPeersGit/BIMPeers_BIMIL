---
description: Label selected AutoCAD geometry with area, length, and radius measurements.
hidden: true
---

# Auto Label

Auto Label reads selected boundaries and curves and places measurement labels directly in Model Space. Use one window to label the **area** of closed objects, the **length** of curves or boundary edges, and the **radius** of arcs and circles. Each output can be formatted and positioned independently, and the saved setup can be reused without reopening the window.

#### Commands

| Command       | Alias | Action                                                     |
| ------------- | ----- | ---------------------------------------------------------- |
| `BP_ALG`      | `ALG` | Open the Auto Label window                                 |
| `BP_ALG_LAST` | `ALGL` | Generate labels immediately with the last-saved settings  |

The same actions are available from the **Auto Label** split button on the **BIMIL** ribbon tab: choose **Auto Label** to configure the labels, or **Generate Last** to reuse the saved setup.

#### How to use

1. **Select objects** before opening Auto Label, or click **Select Objects** in the window and pick boundaries or curves in the drawing.
2. Under **Output**, enable at least one property: **Area**, **Length**, or **Radius**.
3. Click each enabled property to configure its value grouping, placement, unit, precision, and label format. See [Settings](settings.md).
4. Choose the common **Text Style**, **Color**, **Layer**, and **Alignment**.
5. Click **Generate**. If manual placement is enabled, click a label location or radius direction when prompted.

#### Supported geometry

| Output     | Supported geometry and behavior                                                                                       |
| ---------- | --------------------------------------------------------------------------------------------------------------------- |
| **Area**   | Closed curves, regions, and hatches. A label can be created for each object or as one sum for multiple valid objects. |
| **Length** | Lines, arcs, circles, and polylines. Label each edge/segment or create a summed perimeter/path-length value.           |
| **Radius** | Arcs and circles. A radial line and radius text are placed for each valid object.                                     |

#### Notes

* Area values use the drawing insertion units (`INSUNITS`) when available. Length and radius defaults follow the drawing's BIMIL model-unit setting; you can change the displayed unit in the window.
* Unsupported or zero-size objects are skipped and reported in the status line.
* Re-running on the same source does not stack stale labels: unchanged area labels are skipped, while changed area labels and existing length/radius measurements are updated.
* Settings are saved locally and restored after AutoCAD restarts.
