---
description: Easily toggle, save, and manage section boxes for selected elements.
---

# Filter+ Section Box

Filter+ Section Box enables efficient control over section boxes, allowing users to quickly create, toggle, and manage section boxes in Revit. With a single button, users can generate a section box around selected elements or hide it if already present. Saved section boxes are stored in a list, allowing quick access, renaming, and reloading based on saved coordinates, dimensions, and orientations, streamlining complex project views.

#### Features

* [**Toggle Section Box**](toggle-section-box.md)**:**\
  Generates a section box around selected elements or toggles visibility of an existing section box in the current view. If no elements or only the section box is selected, the button simply turns the section box on or off.
* [**Box List**](manage-section-box-box-list.md)**:**\
  Displays saved section boxes in a list, allowing users to store the current view’s section box with **+Save Box**. Each box’s coordinates, size and rotation are retained, and boxes can be renamed or deleted. Selecting a saved box and clicking **Load Box** applies it to the current view.
* [**Box Settings**](manage-seciton-box-settings.md)**:**
  * **Section Box Size:** Choose between **Auto** (adjusts size to selected elements) and **Fixed** (generates a box of specified dimensions centered on the selected elements).
  * **Fixed Size:** Set specific **X, Y, and Z** dimensions for a fixed-size section box.
  * **Section Box Offset:** Adjust the section box position with positive or negative values for each axis.
  * **Auto Rotation:** Allow the section box to rotate to align horizontally with the direction of the selected element.
  * **Auto Zoom to Fit**: Automatically adjusts the camera to focus on the section box after it is created or loaded.

#### Notes

* When only the section box is selected, the toggle button functions as if no elements are selected, hiding or displaying the box as needed.
* Section boxes are saved per project, with data saved upon project or list closure.
* Each project opens with its own set of saved section boxes, clearing any previous list.

{% embed url="https://www.youtube.com/watch?ab_channel=BIMPeers&v=FpO827FNVWY" %}



