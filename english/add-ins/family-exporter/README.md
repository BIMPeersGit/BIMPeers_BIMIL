---
description: Bulk export Revit families into organized folders.
hidden: true
---

# Family Exporter

Export loaded Revit families as individual `.rfa` files in just a few steps, with category-based browsing and bulk selection built in.

## Details

Family Exporter is an add-in for Autodesk Revit that helps you export loaded project families to individual RFA files in bulk. Instead of opening and saving families one by one, you can browse families grouped by category, select the families you need, and export them to a chosen folder with a simple workflow.

### Features

- Lists loaded Revit families by category from the active project
- Allows single selection, multi-selection, Ctrl+A selection, and Shift/Ctrl click workflows
- Exports selected families as RFA files in bulk

### Notes

- Families are exported from the active target project.
- Existing RFA files with the same name in the output folder may be overwritten.
- Exported files are organized by category, for example: `Save Folder / Doors / FamilyName.rfa`.
- System families or non-editable families cannot be exported as standalone RFA files.
