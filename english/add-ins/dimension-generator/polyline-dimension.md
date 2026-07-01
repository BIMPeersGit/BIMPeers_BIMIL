---
hidden: true
---

# Polyline Dimension

Polyline Dimension measures each edge of a closed polyline outline and places one dimension per segment. It follows the true shape, so rectangles and irregular polygons — including diagonal edges and concave corners — are all dimensioned correctly.

Run it from the **Dimension Generator** ribbon button (or the `DIMGEN` / `BP_DIM` command) and choose **Polyline Dimension** in the window.

### Options

When **Polyline Dimension** is selected, two extra choices appear:

| Option        | Choice      | Result                                                                        |
| ------------- | ----------- | ----------------------------------------------------------------------------- |
| **Method**    | **Aligned** | Dimensions each segment along its true length, parallel to the edge.          |
|               | **Linear**  | Splits diagonal segments into separate horizontal (X) and vertical (Y) lengths. |
| **Direction** | **Outside** | Places the dimensions outside the outline.                                    |
|               | **Inside**  | Places the dimensions inside the outline.                                     |

Hover the **?** preview to see how the current Method / Direction combination will look before you Apply.

### How to use

1. **Open the window** — click **Dimension Generator** on the BIMIL ribbon tab, or type `DIMGEN`.
2. **Choose the mode** — under **Target**, select **Polyline Dimension**.
3. **Set Method and Direction** — Aligned vs. Linear, and Outside vs. Inside.
4. **Pick the targets** — under **Select**, choose one:
   * **Select objects** — pick the closed polylines in the drawing.
   * **Select layer** — search for a layer to dimension every closed polyline on it.
5. **Set the offset** — under **Offsets**, set **Detail Dimension** (the distance from each edge to its dimension line).
6. **Set the style & layer** — under **Settings**, choose the **Dimension Style** (use **Edit** to open the style manager) and the **Dimension Layer** the dimensions are placed on.
7. **Apply** — the dimensions are placed and the result is shown in the status line.

### Notes

* A **closed** outline is required. An outline whose endpoints are within the drawing tolerance is still treated as closed; open polylines in the selection are skipped and their count is reported.
* Concave (inward-cornered) outlines are handled — each dimension is pushed to the correct outside or inside face.
* Dimensions identical to ones already at the same spot are skipped, so re-running never creates duplicates.
