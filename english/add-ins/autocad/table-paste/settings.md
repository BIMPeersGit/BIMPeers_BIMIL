---
hidden: true
---

# Settings

Open **Table Paste** from the BIMIL ribbon, or run `BP_TBP` / `TBP`, after copying a table. The window reads the clipboard first, shows the detected table size, and lets you choose how the native AutoCAD table will be placed.

### Clipboard summary

| Field       | Description                                                                                       |
| ----------- | ------------------------------------------------------------------------------------------------- |
| **Table**   | Shows the detected row and column count. If merged cells are present, the merge count appears too. |
| **Preview** | Shows the estimated table width and height in the current drawing unit after scale is applied.     |

The preview size updates when the scale or anchor settings change, so you can confirm the table footprint before choosing the insertion point.

### Placement settings

| Option            | Description                                                                                           | Default       |
| ----------------- | ----------------------------------------------------------------------------------------------------- | ------------- |
| **Table scale**   | Multiplies the source table size before insertion. Use the plotted drawing scale, such as `100` for 1:100. | `1`           |
| **Text style**    | Use **Source fonts** or force every cell to an existing AutoCAD text style from the active drawing.    | Source fonts  |
| **Table layer**   | Place the table on the current layer or another existing drawing layer.                               | Current Layer |
| **Anchor corner** | Controls which point of the table stays on the location you pick in Model Space.                      | Center        |

### Anchor corner

| Anchor           | Placement behavior                                      |
| ---------------- | ------------------------------------------------------- |
| **Center**       | The picked point becomes the center of the pasted table. |
| **Top left**     | The table grows right and downward from the picked point. |
| **Top right**    | The table grows left and downward from the picked point.  |
| **Bottom left**  | The table grows right and upward from the picked point.   |
| **Bottom right** | The table grows left and upward from the picked point.    |

Use a corner anchor when the table needs to start from a title block, grid intersection, or known drawing reference. Use **Center** when you want to position the table by its overall footprint.

### Live preview

After you click **OK**, Table Paste asks for the insertion point in Model Space. A live preview follows the cursor and shows the table outline, cell divisions, merged-cell footprint, and visible cell text where possible. Very dense tables show their overall footprint only, so large pastes remain responsive while still showing the space they will occupy.

### Source appearance

Table Paste keeps source formatting enabled while it builds the AutoCAD table.

| Source property         | Result in AutoCAD                                                            |
| ----------------------- | ---------------------------------------------------------------------------- |
| **Column width**        | Converted from source size and multiplied by **Table scale**.                 |
| **Row height**          | Converted from source size and multiplied by **Table scale**.                 |
| **Font family**         | Converted to generated `TP_*` text styles when matching fonts are installed.  |
| **Font size**           | Converted from source points to drawing units.                                |
| **Bold / italic**       | Used when creating source-font text styles.                                   |
| **Text and fill color** | Applied from source colors when available.                                    |
| **Borders**             | Applied per edge, including source border weight and color when available.    |
| **Padding**             | Used as AutoCAD cell margins when the source reports cell padding.            |
| **Merged cells**        | Recreated as AutoCAD merged cell ranges.                                      |
| **Alignment**           | Horizontal and vertical alignment are preserved; general numeric values align right. |

Clicking **OK** validates the scale, text style, and layer, saves the settings, and then asks for the insertion point.
