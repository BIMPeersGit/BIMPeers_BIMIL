---
hidden: true
---

# Generate Last

Generate Last applies the most recently saved Auto Label setup to a new selection without opening the settings window. Run it from the **Generate Last** item in the Auto Label split button, or type `BP_ALG_LAST` / `ALGL`.

### How to use

1. Open **Auto Label**, configure the outputs and label style, and click **Generate** once to save the setup.
2. Select the new boundaries or curves in the drawing.<br>
3. Run **Generate Last**. If nothing is preselected, AutoCAD prompts you to select objects.
4. Complete any manual placement prompts enabled in the saved settings.

### Notes

* The command restores settings from the local settings file, so it keeps working after AutoCAD restarts.
* If no saved settings exist, the built-in defaults are used: area labels only, one label per object, automatic placement, `m²`, two decimal places, Standard text style, BYLAYER color, and the current layer.
* Unsupported objects are skipped. If the selection contains no valid boundary or curve, no labels are created and a message is written to the command line.
* Running the command again on the same source updates or skips its existing Auto Label measurements instead of layering duplicate labels.
