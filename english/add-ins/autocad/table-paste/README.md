---
description: >-
  Paste copied spreadsheet or document tables into AutoCAD as editable table
  objects.
hidden: true
---

# Table Paste

Table Paste reads table data from the clipboard and places it in Model Space as a native AutoCAD table object. Copy cells from a source such as Excel, a web table, Word, or HWP, then use one compact window to check the detected row and column count, set the drawing scale, choose the text style and layer, and place the table with a live insertion preview.

#### Commands

| Command          | Alias        | Action                      |
| ---------------- | ------------ | --------------------------- |
| `BP_TBP`         | `TBP`        | Open the Table Paste window |
| `BP_TABLE_PASTE` | `TABLEPASTE` | Open the Table Paste window |

The same action is available from the **Table Paste** button on the **BIMIL** ribbon tab.

#### How to use

1. Copy a table or cell range from the source application.
2. Run **Table Paste** from the BIMIL ribbon, or type `TBP`.
3. Check the detected table size and preview size in the **Clipboard** summary.
4. Choose the **Table scale**, **Text style**, **Table layer**, and **Anchor corner**.
5. Click **OK**, then move the cursor in Model Space and pick the insertion point when the preview is in the right place.

#### Paste window

| Option            | Description                                                                                           | Default       |
| ----------------- | ----------------------------------------------------------------------------------------------------- | ------------- |
| **Table scale**   | Multiplies the source table size before insertion. Use the plotted drawing scale, such as `100` for 1:100. | `1`           |
| **Text style**    | Use **Source fonts** or force every cell to an existing AutoCAD text style from the active drawing.    | Source fonts  |
| **Table layer**   | Place the table on the current layer or another existing drawing layer.                               | Current Layer |
| **Anchor corner** | Controls which point of the table stays on the location you pick in Model Space.                      | Center        |

#### Live preview

The preview uses the same layout measurement as the final table insertion. It shows the table outline, cell divisions, merged-cell footprint, and visible cell text where possible. Very dense tables show their overall footprint only, so large pastes remain responsive while still showing the space they will occupy.

#### Clipboard data

| Source format | Behavior                                                                                                  |
| ------------- | --------------------------------------------------------------------------------------------------------- |
| **Excel XML** | Preserves Excel row and column sizes, merged cells, fonts, colors, fills, borders, and alignment.         |
| **HTML**      | Reads copied web or spreadsheet tables, including nested table handling, CSS styling, spans, and padding. |
| **RTF**       | Reads table structure from Word and HWP-style clipboard data, including row heights and merged regions.   |

#### Notes

* Table Paste chooses the richest clipboard table it can find. If several formats are available, it prefers the version with the most actual table content.
* The inserted result is a single AutoCAD table, so it can be moved, edited, styled, or scheduled like other AutoCAD table objects.
* Source colors, source fonts, row heights, column widths, padding, borders, and merges are applied when the clipboard provides them.
* If no table data is found in the clipboard, Table Paste shows a warning and does not change the drawing.
* If the Table Paste window is already open, running the command again refreshes it with the latest clipboard data.
* Settings are saved locally and restored after AutoCAD restarts.
