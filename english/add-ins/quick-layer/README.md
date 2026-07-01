---
description: Save frequently used layers to number slots and switch, move, or copy objects between them in a click.
hidden: true
---

# Quick Layer

Quick Layer is a BIMIL AutoCAD add-in that stores the layers you use most in slots 1–9, then lets you quickly change the layer of a selected object, copy it onto a slot layer, or set a slot layer as the current layer using simple number-based commands. Slot data is saved inside the drawing file (Named Objects Dictionary), so the configuration is preserved whenever the same DWG is reopened. It appears in the **BIMIL** ribbon tab under the **Layer** panel as a Quick Layer split button; pressing the button body opens the settings window (`QLS`), and the drop-down exposes each function.

#### Commands

| Ribbon item                                 | Command | Internal alias    | Slot input | Action                                                             |
| ------------------------------------------- | ------- | ----------------- | ---------- | ------------------------------------------------------------------ |
| **Quick Layer** (button body) / **Setting** | `QLS`   | `BP_QL_SETTING`   | —          | Open the slot settings window                                      |
| **Register**                                | `QLR`   | `BP_QL_REGISTER`  | 1–9        | Register the selected object's layer into one of slots 1–9         |
| **Transfer**                                | `QLT`   | `BP_QL_TRANSFER`  | 0–9        | Move the selected objects onto a slot 0–9 layer                    |
| **Duplicate**                               | `QLD`   | `BP_QL_DUPLICATE` | 0–9        | Copy the selected objects and place the copies on a slot 0–9 layer |
| **Set Current**                             | `QLC`   | `BP_QL_CURRENT`   | 1–9        | Set a slot 1–9 layer as the current layer (`CLAYER`)               |

Slot `0` is not a saved slot — it always means the **current layer**. It can therefore be entered only in `Transfer` / `Duplicate`, while `Register` / `Set Current` accept 1–9 only.

#### Features

- **Save layer slots 1–9:** Assign frequently used layers to number slots. In the settings window you can pick a layer per slot from a combo box, type it directly, or click **Select** to pick an object on the drawing and capture its layer into that slot (saved immediately).
- **Register (`QLR`):** Reads the layer of the first selected object and stores it in the chosen slot. If objects are pre-selected they are used; otherwise AutoCAD prompts for a selection.
- **Transfer (`QLT`):** Changes the `Layer` of the selected objects to the target slot layer. Slot `0` is the current layer.
- **Duplicate (`QLD`):** Copies the selected objects in the current space with `DeepClone`, then changes the copies' `Layer` to the target slot layer. The original objects are left unchanged. Slot `0` is the current layer.
- **Set Current (`QLC`):** Sets the target slot (1–9) layer as the AutoCAD current layer (`CLAYER`). If the slot is empty or the layer does not exist in the drawing, a warning is printed and the command ends.
- **Live settings window:** A modeless window that reads the current drawing's layer list into per-slot combo boxes. It updates automatically when layers are added or removed (database events + a debounce timer), so there is no separate refresh button. Running `QLS` again while it is open brings the existing window to the front (restoring it if minimized).
- **Theme-aware UI:** Button icons and panel title color follow the AutoCAD `COLORTHEME` (light / dark) automatically.

#### Notes

- Slot values are stored in the current DWG's Named Objects Dictionary — dictionary `BIMIL_QuickLayer`, Xrecord key `Slots`, holding the layer-name strings for slots 1–9 in order. Because the data lives inside the drawing rather than on the user's PC, sharing the drawing shares the Quick Layer slots too. Slot `0` (current layer) is not saved.
- When the modeless window writes to the database, the document is accessed via `Document.LockDocument()` before saving to avoid an `eLockViolation`.
- Commands also work when typed directly in the command line, and each is registered under both its short command and a `BP_` internal alias.
- Supported on AutoCAD 2023–2027; the .NET Framework and .NET projects share the same `QuickLayer` source (2023/2024 on .NET Framework 4.8, 2025/2026 on net8.0-windows, 2027 on net10.0-windows). Local builds deploy automatically to `%AppData%\Autodesk\ApplicationPlugins\BIMPeers_QuickLayer.bundle\`.
