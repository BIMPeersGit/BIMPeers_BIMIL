---
hidden: true
---

# Export to Excel

### 1. Start Family Type Manager

Open the **BIMIL** tab in Revit and click **Family Type Manager**. The window loads families from the active project.

### 2. Choose a category group and scope

Use the tabs to browse **Model**, **Annotation**, or **Analytical Model** types. Then choose which part of the project supplies the family list:

| Scope                 | Families shown                                                                 |
| --------------------- | ------------------------------------------------------------------------------ |
| **All**               | All supported types loaded in the active project                               |
| **Active View**       | Families used by elements visible in the active view                           |
| **Selected Elements** | Families used by the elements currently selected in Revit                      |

Changing the category tab clears the current **Selected Families** list, so finish one group before switching tabs.

### 3. Select families

Search the **Families** list by category or family name. Select the required families or category groups and use the right-arrow button to add them to **Selected Families**.

In the selected list, you can:

* Search the current selection.
* Remove families with the left-arrow button.
* Move selected families to the top, up, down, or bottom.
* Clear the complete selection.

The selected order is also used for the exported family worksheets.

### 4. Export the workbook

Click **Export**, choose a location, and save the `.xlsx` file. The suggested filename is based on the project title and export time.

Family Type Manager creates one visible worksheet per selected family. Each worksheet contains:

| Column                            | Purpose                                                        |
| --------------------------------- | -------------------------------------------------------------- |
| **ElementId**                     | Identifies an existing Revit type; do not edit                  |
| **Category**                      | Identifies the Revit category; do not edit                      |
| **Family**                        | Identifies the family; do not edit                              |
| **Type**                          | Existing or new type name; editable                             |
| **Parameter columns**             | Editable type-parameter values                                 |

### 5. Edit in Excel

* Edit a type name or parameter value in an existing row to update that type.
* Add a new row with a type name and parameter values to create a type. Leave the identity cells used for existing types blank.
* Use the provided drop-down list for Yes/No, ElementId, and other parameters with known choices.
* You may reorder parameter columns or delete parameter columns you do not want to import.

{% hint style="warning" %}
Do not delete or replace the hidden BIMIL row/column identifiers or internal worksheets. Do not edit the locked identity columns. Without that data, Family Type Manager cannot safely match the workbook to Revit.
{% endhint %}

Deleted parameter columns are ignored during import. When creating a type, an omitted parameter keeps the value inherited from the chosen **Duplicate from** type.

