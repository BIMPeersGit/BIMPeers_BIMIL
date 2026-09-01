---
hidden: true
---

# Paste Workflow

Table Paste separates setup from placement. The window reads the clipboard first, then the AutoCAD command line asks for the exact insertion point with a live preview attached to the cursor.

### How to use

1. Copy the table range from the source application.
2. Run **Table Paste** from the BIMIL ribbon, or type `BP_TBP`, `BP_TABLE_PASTE`, `TBP`, or `TABLEPASTE`.
3. Review the detected rows, columns, merged regions, and preview size.
4. Adjust the scale, text style, layer, and anchor corner.
5. Click **OK**.
6. Move the cursor in Model Space and click the insertion point when the preview is in the right place.

### Live preview

The preview uses the same layout measurement as the final table insertion. It shows the table outline, cell divisions, merged-cell footprint, and visible cell text where possible. Very dense tables show their overall footprint only, so large pastes remain responsive while still showing the space they will occupy.

### Clipboard detection

When one copy operation provides more than one table format, Table Paste compares the available formats and uses the richest one. Excel XML has the highest priority when it is available, because it carries the most precise worksheet sizing and style data. HTML and RTF are also parsed so tables copied from web pages, Google Sheets, Word, HWP, and similar applications can still be pasted with structure intact.

### Notes

* If no table data is found in the clipboard, Table Paste shows a warning and does not change the drawing.
* If the Table Paste window is already open, running the command again refreshes it with the latest clipboard data.
* The command writes a result message after insertion, including the pasted row and column count and the number of merged regions when merges exist.
* Rollover tips are disabled during placement by default to keep the insertion preview clear.
