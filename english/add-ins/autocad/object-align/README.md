---
description: Align selected AutoCAD objects by edge or center and distribute equal gaps.
hidden: true
---

# Object Align

Object Align arranges selected AutoCAD objects by their geometric extents in the current UCS. Use the Align panel on the BIMIL ribbon to line up object edges or centers, or distribute objects with equal horizontal or vertical gaps.

#### Commands

<table><thead><tr><th>Command</th><th>Alias</th><th width="246">Action</th></tr></thead><tbody><tr><td><code>BP_AGL</code></td><td><code>AGL</code></td><td>Align selected objects to the left edge</td></tr><tr><td><code>BP_AGC</code></td><td><code>AGC</code></td><td>Align selected objects to the center line</td></tr><tr><td><code>BP_AGR</code></td><td><code>AGR</code></td><td>Align selected objects to the right edge</td></tr><tr><td><code>BP_AGT</code></td><td><code>AGT</code></td><td>Align selected objects to the top edge</td></tr><tr><td><code>BP_AGM</code></td><td><code>AGM</code></td><td>Align selected objects to the middle line</td></tr><tr><td><code>BP_AGB</code></td><td><code>AGB</code></td><td>Align selected objects to the bottom edge</td></tr><tr><td><code>BP_AGH</code></td><td><code>AGH</code></td><td>Distribute selected objects horizontally</td></tr><tr><td><code>BP_AGV</code></td><td><code>AGV</code></td><td>Distribute selected objects vertically</td></tr><tr><td><code>BP_DSH</code></td><td><code>DSH</code></td><td>Distribute selected objects horizontally</td></tr><tr><td><code>BP_DSV</code></td><td><code>DSV</code></td><td>Distribute selected objects vertically</td></tr></tbody></table>

The same actions are available from the **Align** panel on the **BIMIL** ribbon tab.

#### How to use

1. Select the objects to arrange, or run an Object Align command and select objects when prompted.
2. Choose one of the align or distribute buttons from the **Align** panel, or type its command alias.
3. For align commands, select at least two objects.
4. For distribute commands, select at least three objects.
5. Object Align moves the selected objects and keeps them selected after the operation finishes.

#### Align operations

| Operation        | Behavior                                                                           |
| ---------------- | ---------------------------------------------------------------------------------- |
| **Align Left**   | Moves objects so their left extents share the same X position.                     |
| **Align Center** | Moves objects so their horizontal centers share the selection's center X position. |
| **Align Right**  | Moves objects so their right extents share the same X position.                    |
| **Align Top**    | Moves objects so their top extents share the same Y position.                      |
| **Align Middle** | Moves objects so their vertical centers share the selection's center Y position.   |
| **Align Bottom** | Moves objects so their bottom extents share the same Y position.                   |

#### Distribute operations

| Operation                   | Behavior                                                                              |
| --------------------------- | ------------------------------------------------------------------------------------- |
| **Distribute Horizontally** | Keeps the leftmost and rightmost objects fixed, then makes the horizontal gaps equal. |
| **Distribute Vertically**   | Keeps the lowest and highest objects fixed, then makes the vertical gaps equal.       |

#### Notes

* Object Align calculates positions in the current UCS, so the result follows the active drawing coordinate orientation.
* The command uses each object's geometric extents. If any selected object does not provide valid extents, no objects are moved.
* Distribution is based on the gaps between object extents, not the distance between insertion points.
* Objects on locked layers or unsupported objects may prevent the move; AutoCAD reports the reason in the command line.
