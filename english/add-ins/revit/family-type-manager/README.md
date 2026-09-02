---
description: Export Revit family type data to Excel and safely create or update types from an import preview.
hidden: true
---

# Family Type Manager

Family Type Manager lets you manage Revit family type data through Excel. Choose families from the active project, export their type names and editable type parameters to an `.xlsx` workbook, edit the workbook, and import it back through a change preview before anything is applied to the model.

### Features

* Browse supported families under **Model**, **Annotation**, and **Analytical Model** categories.
* Limit the family list to the whole project, the active view, or currently selected elements.
* Search by category or family name and build an ordered **Selected Families** list.
* [Export to Excel](export-to-excel.md) with one worksheet per family, editable type names and parameters, and drop-down choices where available.
* [Import from Excel](import-from-excel.md) to create, update, or overwrite family types after reviewing every detected change.
* Filter the import preview by **Create**, **Overwrite**, **Update**, **No Change**, or **Error**.
* Roll back the complete import if Revit rejects any operation.

### Supported versions

Family Type Manager supports Revit **2023–2027**. Revit 2022 is not supported.

### Notes

* Family Type Manager edits **type data**, not instance parameter values.
* Only editable type parameters are included in the workbook.
* The workbook is tied to the Revit project from which it was exported. Import it into the same active project.
* Keep the workbook's hidden BIMIL data intact. It identifies the project, families, rows, parameters, and choice values used during import.
* The project must remain the active document while an export or import request is running. If the active document changes, reload the list and start again.

