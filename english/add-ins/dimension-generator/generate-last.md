---
hidden: true
---

# Generate Last

Generate Last repeats your most recent Dimension Generator settings on a new selection — the exact mode, options, offsets, style, and layer from the last time you clicked **Generate** — without opening the window. It is meant for dimensioning many similar objects in a row.

Run it from the **Generate Last** ribbon button (or the `DIMFAST` / `BP_DIM_FAST` command).

### How to use

1. **Generate once** — open the **Dimension Generator** window, configure it, and click **Generate**. This stores the settings.
2. **Select the objects** you want to dimension. (You can select them before running the command, or the command will ask you to select.)
3. **Run Generate Last** — click **Generate Last** on the BIMIL ribbon tab, or type `DIMFAST`. The dimensions are placed immediately with the stored settings.

### Notes

* If you have never generated dimensions before, Generate Last opens the **Dimension Generator** window instead of running blind.
* If no objects are selected, the command prompts you to select some before dimensioning.
* Settings are saved to file, so Generate Last keeps working with your last configuration even after restarting AutoCAD.
