---
hidden: true
---

# Settings

The settings window is where you fill your nine layer slots. **Register** (`QLR`) is the quick companion to it — it drops a picked object's layer straight into a slot without opening the window.

Open the window with the **Quick Layer** ribbon button (or the `QLS` command).

### The settings window

| Item                       | What it does                                                                                     |
| -------------------------- | ------------------------------------------------------------------------------------------------ |
| **CURRENT LAYER (SLOT 0)** | Shows the current layer. It is read-only and is what *Transfer* / *Duplicate* use as slot 0.      |
| **SHORTCUT SLOTS (1–9)**   | One row per slot. Choose or type a layer name, or click **Select** to pick an object in the drawing and use its layer. |
| **Save**                   | Writes the slots into the current drawing.                                                        |
| **Close**                  | Closes the window.                                                                                |

### Register (`QLR`)

Register fills a slot without opening the window:

1. **Select** the object whose layer you want to save (or pre-select it before running).
2. Run **Register** from the ribbon drop-down, or type `QLR`.
3. **Enter the slot number** (1–9) when prompted.

The first selected object's layer is stored in that slot.

### Notes

* Slots are saved in the drawing's Named Objects Dictionary, so they stay with the DWG and travel to anyone you share it with.
* Slot 0 (current layer) is never saved — only slots 1–9 hold assigned layers.
