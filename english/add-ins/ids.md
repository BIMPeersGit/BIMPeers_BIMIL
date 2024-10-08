---
description: Check Element IDs or select elements by entering their ID
---

# IDs

**IDs** provides an easy way to view and select element IDs within both Revit models and linked models. The add-in appears as a side panel, which can be toggled on or off using the **IDs** button. Each time an element is selected, its corresponding ID is displayed in the panel. IDs can also be manually entered into the text box for element selection, and a history feature tracks recent actions for convenient reference.

## Features

* **View Element IDs:** \
  Automatically displays the IDs of selected elements in Revit and linked models. Multiple IDs are separated by a semicolon (`;`).
* **Select by ID:** \
  Enter IDs manually (separated by space, comma, or semicolon) and select the corresponding elements by clicking the **Select** button. IDs are unified with `;` after selection.
* **Copy IDs:** \
  Copy the current list of IDs to the clipboard using the **Copy** button.
* **Element Count:** \
  Shows the count of currently selected elements each time a selection is made.
* **History Tracking:** \
  Logs up to 20 recent actions, allowing users to view and select elements from previous ID entries.
* **Linked Model Support:** \
  Displays selection of element IDs from linked models in the format \
  `(Linked Model ID) Element ID; Element ID; ...`

## Notes

* If an ID does not exist in the current model, only existing IDs will be selected.
* While the add-in displays the IDs of linked model elements when selected, users cannot select linked model elements by manually entering their IDs.
* In Revit 2022, displaying the IDs of elements within linked models is not supported.
