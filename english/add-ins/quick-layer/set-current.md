---
hidden: true
---

# Set Current

Set Current makes a slot's layer the drawing's current layer (`CLAYER`), so anything you draw next lands on it — without opening the layer list to find it.

Run it from the **Set Current** ribbon drop-down item (or the `QLC` command).

### How to use

1. Run **Set Current**, or type `QLC`.
2. **Enter the slot number** (1–9) when prompted.

The slot's layer becomes the current layer.

### Notes

* Set Current uses slots 1–9 only — there is no slot 0 here, since slot 0 *is* the current layer.
* If the slot is empty or its layer no longer exists in the drawing, Set Current reports it and stops.
