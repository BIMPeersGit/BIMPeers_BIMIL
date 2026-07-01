---
hidden: true
---

# Apply Last

Apply Last repeats your most recent Dimension Generator settings on a new selection — the exact mode, options, offsets, style, and layer from the last time you clicked **Apply** — without opening the window. It is meant for dimensioning many similar objects in a row.

Run it from the **Apply Last** ribbon button (or the `DIMFAST` / `BP_DIM_FAST` command).

### How to use

1. **Apply once** — open the **Dimension Generator** window, configure it, and click **Apply**. This stores the settings for the session.
2. **Select the objects** you want to dimension. (You can select them before running the command, or the command will ask you to select.)
3. **Run Apply Last** — click **Apply Last** on the BIMIL ribbon tab, or type `DIMFAST`. The dimensions are placed immediately with the stored settings.

### Notes

* If you have not applied anything yet in the current AutoCAD session, Apply Last opens the **Dimension Generator** window instead of running blind.
* If no objects are selected, the command prompts you to select some before dimensioning.
* The stored settings last for the AutoCAD session and are updated every time you click **Apply** in the window.
