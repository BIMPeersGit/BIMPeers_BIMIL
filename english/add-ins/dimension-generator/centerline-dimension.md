---
hidden: true
---

# Centerline Dimension

Centerline Dimension reads the grid lines you select and places two tiers of dimensions in one pass: the spacing between adjacent centerlines (**Detail**) and the overall span across them (**Overall**). Horizontal, vertical, and diagonal centerlines are all handled — parallel diagonals are grouped and measured with rotated dimensions.

Run it from the **Dimension Generator** ribbon button (or the `DIMGEN` / `BP_DIM` command) and choose **Centerline Dimension** in the window.

### How to use

1. **Open the window** — click **Dimension Generator** on the BIMIL ribbon tab, or type `DIMGEN`.
2. **Choose the mode** — under **Target**, select **Centerline Dimension**.
3. **Pick the targets** — under **Select**, choose one:
   * **Select objects** — pick the centerlines (lines or open polylines) in the drawing.
   * **Select layer** — search for a layer to dimension every line and polyline on it.
4. **Set the offsets** — under **Offsets**:

   | Field                 | Meaning                                                                 |
   | --------------------- | ----------------------------------------------------------------------- |
   | **Detail Dimension**  | Distance from the centerlines to the first (detail) dimension line.     |
   | **Overall Dimension** | Distance from the detail dimension line out to the overall dimension line. |
5. **Set the style & layer** — under **Settings**, choose the **Dimension Style** (use **Edit** to open the style manager) and the **Dimension Layer** the dimensions are placed on.
6. **Apply** — the dimensions are placed and the result is shown in the status line.

### Notes

* At least **two** valid centerlines are required.
* Only lines and open polylines are dimensioned. Closed polylines and unsupported objects in the selection are skipped, and the skipped count is reported.
* Dimensions identical to ones already at the same spot are skipped, so re-running never creates duplicates.
