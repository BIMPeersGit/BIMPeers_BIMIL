# How to Use

### 1. Start Family Exporter

* Open the **BIMIL** tab in Revit and click **Family Exporter**.
* The add-in loads families from the active project and displays the project path under **Target Project**.

{% hint style="info" %}
If the project has not been saved yet, the target project is shown as `New Project (Project Name)`.
{% endhint %}

### 2. Review Project Families

The left panel, **Project Families**, shows loaded families grouped by category. Each category group displays the number of families it contains.

* Use **Search** to filter families by name.
* Use the expand/collapse button to open or close all category groups.
* Click the refresh button to reload the family list from the active project.

### 3. Select Families

Select the families or category groups you want to export.

* Click a single family to select it.
* Use `Ctrl + Click` to select multiple individual items.
* Use `Shift + Click` to select a range.
* Use `Ctrl + A` to select all visible items in the focused list.

### 4. Move Families to Selected Families

Move items from **Project Families** to **Selected Families** using one of the following methods:

* Click the add button between the two panels.
* Drag selected items from the left panel to the right panel.
* Press `Enter` or `Right Arrow` while the left panel is focused.

To remove items from **Selected Families**:

* Click the remove button.
* Drag selected items back to the left panel.
* Press `Delete` or `Left Arrow` while the right panel is focused.

### 5. Choose a Save Folder

Click **Browse** and select the folder where the exported RFA files will be saved.

The default save folder is:

```text
Desktop\Family Exporter
```

### 6. Export Families

Click **Export** to save the selected families as `.rfa` files.

Family Exporter creates category folders automatically inside the selected save folder.

```text
Save Folder
+-- Doors
|   `-- FamilyName.rfa
+-- Furniture
|   `-- FamilyName.rfa
`-- Windows
    `-- FamilyName.rfa
```

Enable **Open folder after export** if you want the output folder to open automatically after the export is complete.

### 7. Check Export Results

When export is complete, Family Exporter shows a result message.

* If all selected families are exported successfully, the message shows the number of exported families.
* If some families cannot be exported, the message lists the failed families.
* Successfully exported families are removed from the **Selected Families** list.

{% hint style="warning" %}
Before exporting, keep Revit focused on the same project that was loaded in Family Exporter. If you switch to another project, return to the target project or refresh the list before exporting.
{% endhint %}
