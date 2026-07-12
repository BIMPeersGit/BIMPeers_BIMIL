---
description: Save layers to number slots and switch, move, or copy objects between them.
---

# Quick Layer

Quick Layer lets you save the layers you use most into numbered slots (1–9) and then switch, move, or copy objects between them with short commands — no digging through the layer list every time. The slots are stored inside the drawing, so they travel with the DWG: reopen it, or hand it to a colleague, and the slots are still there.

#### Commands

| Command | Alias             | Action                                               |
| ------- | ----------------- | ---------------------------------------------------- |
| `QLS`   | `BP_QL_SETTING`   | Open the Quick Layer settings window                 |
| `QLR`   | `BP_QL_REGISTER`  | Register the selected object's layer to a slot (1–9) |
| `QLT`   | `BP_QL_TRANSFER`  | Move selected objects to a slot layer (0–9)          |
| `QLD`   | `BP_QL_DUPLICATE` | Copy selected objects to a slot layer (0–9)          |
| `QLC`   | `BP_QL_CURRENT`   | Set a slot layer (1–9) as the current layer          |

On the **BIMIL** ribbon tab, the **Layer** panel has a **Quick Layer** split button — its drop-down holds Settings, Register, Transfer, Duplicate, and Set Current. Run a command without a number and it asks for the slot number in the command line.

#### Features

* [**Settings**](settings.md)**:**\
  Assign a layer to each of slots 1–9 in the settings window, and use **Register** to capture a slot's layer straight from an object you pick. Slots are saved inside the drawing.
* [**Transfer**](transfer.md)**:**\
  Move the selected objects onto a slot's layer.
* [**Duplicate**](duplicate.md)**:**\
  Copy the selected objects onto a slot's layer, leaving the originals where they are.
* [**Set Current**](set-current.md)**:**\
  Make a slot's layer the current layer.

#### Notes

* **Slot 0** always means the **current layer**. It can be used by Transfer and Duplicate, but it is not a saved slot — Register and Set Current use slots 1–9 only.
* Slots are saved in the drawing's Named Objects Dictionary, so they stay with the DWG and are shared when you send it to someone else.
* Every command works on objects you have already selected, or prompts you to select when none are.
