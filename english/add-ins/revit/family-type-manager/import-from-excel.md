---
hidden: true
---

# Import from Excel

### 1. Open the workbook

Open **Family Type Manager** in the same Revit project used for export, click **Import**, and select the edited `.xlsx` workbook. The add-in validates the workbook and opens **Import Preview**; the model is not changed yet.

### 2. Review the preview

Use the tabs and search field to review the detected rows:

| Action        | Meaning                                                                                              |
| ------------- | ---------------------------------------------------------------------------------------------------- |
| **Create**    | A new type will be duplicated from an existing type in the same family.                              |
| **Overwrite** | A new row uses an existing type name and can replace that type's values.                              |
| **Update**    | An existing type name or one or more editable parameters changed.                                    |
| **No Change** | The workbook values match the current Revit type.                                                     |
| **Error**     | The row contains invalid data or a change that cannot be applied.                                    |

Expand a row to inspect its details. Create rows show the source and new values; update and overwrite rows show the current and new values; error rows show the field, input value, and reason.

### 3. Choose Duplicate from

Every **Create** row needs a source type from the same family. Choose it in the **Duplicate from** column. Family Type Manager duplicates that Revit type and then applies the Excel values.

To assign the same source to several new types, select multiple Create rows from the same family and change **Duplicate from** on one of them.

### 4. Apply the changes

Click **Apply** when the preview is ready.

* If **Overwrite** conflicts exist, choose **Yes** to apply the Excel values to the existing types or **No** to skip those rows and continue with the remaining valid changes.
* Error rows are excluded. If valid changes remain, Family Type Manager asks whether to continue without the error rows.
* **No Change** rows are not written to the model.

After a successful import, the result reports the numbers of created, updated, overwritten, and skipped rows, and the family list is refreshed.

### Important rules

* Existing rows are checked against both their stored identity and current Revit element ID.
* A new row must not contain the identity values reserved for an existing type.
* Renaming an existing type to another existing type name is rejected. Type-name exchanges between updated rows are supported when their final names remain unique.
* If multiple workbook rows target the same existing type, the last applicable instruction in workbook order is used.
* Invalid choice values are reported as errors instead of being silently converted.
* All valid changes are applied in one Revit transaction. If any operation fails, the entire import is rolled back.

