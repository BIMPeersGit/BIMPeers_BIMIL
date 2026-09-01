---
description: Align selected AutoCAD objects by edge or center and distribute equal gaps.
hidden: true
---

# Object Align

Object Align arranges selected AutoCAD objects by their geometric extents in the current UCS. Use the Align panel on the BIMIL ribbon to line up object edges or centers, or distribute objects with equal horizontal or vertical gaps.

#### Commands

| Command  | Alias | Action                                      |
| -------- | ----- | ------------------------------------------- |
| `BP_AGL` | `AGL` | Align selected objects to the left edge     |
| `BP_AGC` | `AGC` | Align selected objects to the center line   |
| `BP_AGR` | `AGR` | Align selected objects to the right edge    |
| `BP_AGT` | `AGT` | Align selected objects to the top edge      |
| `BP_AGM` | `AGM` | Align selected objects to the middle line   |
| `BP_AGB` | `AGB` | Align selected objects to the bottom edge   |
| `BP_AGH` | `AGH` | Distribute selected objects horizontally    |
| `BP_AGV` | `AGV` | Distribute selected objects vertically      |
| `BP_DSH` | `DSH` | Distribute selected objects horizontally    |
| `BP_DSV` | `DSV` | Distribute selected objects vertically      |

The same actions are available from the **Align** panel on the **BIMIL** ribbon tab.

#### How to use

1. Select the objects to arrange, or run an Object Align command and select objects when prompted.
2. Choose one of the align or distribute buttons from the **Align** panel, or type its command alias.
3. For align commands, select at least two objects.
4. For distribute commands, select at least three objects.
5. Object Align moves the selected objects and keeps them selected after the operation finishes.

#### Align operations

| Operation            | Behavior                                                                            |
| -------------------- | ----------------------------------------------------------------------------------- |
| **Align Left**       | Moves objects so their left extents share the same X position.                      |
| **Align Center**     | Moves objects so their horizontal centers share the selection's center X position.  |
| **Align Right**      | Moves objects so their right extents share the same X position.                     |
| **Align Top**        | Moves objects so their top extents share the same Y position.                       |
| **Align Middle**     | Moves objects so their vertical centers share the selection's center Y position.    |
| **Align Bottom**     | Moves objects so their bottom extents share the same Y position.                    |

#### Distribute operations

| Operation                     | Behavior                                                                                  |
| ----------------------------- | ----------------------------------------------------------------------------------------- |
| **Distribute Horizontally**   | Keeps the leftmost and rightmost objects fixed, then makes the horizontal gaps equal.      |
| **Distribute Vertically**     | Keeps the lowest and highest objects fixed, then makes the vertical gaps equal.            |

#### Notes

* Object Align calculates positions in the current UCS, so the result follows the active drawing coordinate orientation.
* The command uses each object's geometric extents. If any selected object does not provide valid extents, no objects are moved.
* Distribution is based on the gaps between object extents, not the distance between insertion points.
* Objects on locked layers or unsupported objects may prevent the move; AutoCAD reports the reason in the command line.
