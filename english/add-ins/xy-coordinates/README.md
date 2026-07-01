---
description: Extract the X·Y coordinates of a clicked point and annotate them on the drawing.
hidden: true
---

# XY Coordinates

XY Coordinates is a BIMIL AutoCAD add-in for the BIMIL ecosystem. When you click a point on the drawing, it reads that point's X·Y coordinates and places a coordinate label (MText) wherever you want, dragging it into position. Optional elements such as a leader, a base-point marker, and an underline can be configured in the settings window. It runs from the **BIMIL** ribbon tab, where the **XY Coordinates** panel places two buttons side by side.

#### Commands

| Button             | Command                 | Action                                             |
| ------------------ | ----------------------- | -------------------------------------------------- |
| **XY Coordinates** | `XYCoordinates`         | Pick a point and annotate using the saved settings |
| **Settings**       | `XYCoordinatesSettings` | Open the (modeless) input settings window          |

If you run `XYCoordinates` before ever pressing **[Apply]** in the settings window (`XYSettingsStore.Last == null`), it does not draw with arbitrary defaults — a BIMIL warning appears and it exits. Apply the settings first.

#### Features

- **Coordinate pick & annotate:** Click a base point to read its X·Y value and annotate it as a label.
- **Drag preview:** While dragging the label to its target position, the base point, a leader from the cursor, and the text to be annotated are previewed in real time (`DrawJig`) in a highlight color (ACI 8).
- **Direction-aware alignment:** The MText alignment is chosen automatically so the text unfolds away from the base point depending on the drag direction.
- **Annotation customization:** Set text height, decimal places, the delimiter symbol, the separator between X and Y, and one-line vs. two-line formatting.
- **Optional elements:** A leader, a base-point marker (arrow / dot / circle), and a text underline can each be toggled independently.
- **Continuous input:** Once started, keep annotating points one after another until you press ESC.
- **BIMIL integration:** Uses the BIMIL premium window style (Controls.dll) and links automatically to the AutoCAD light / dark theme.

#### Settings (`XYSettings`)

| Property        | Description                                                         | Default |
| --------------- | ------------------------------------------------------------------- | ------- |
| `TextHeight`    | Text height (positive; blank not allowed)                           | 2.5     |
| `DecimalPlaces` | Decimal places for the X·Y values                                   | 3       |
| `Delimiter`     | Shared X·Y delimiter symbol (`=`, `.`, `:`) — same for X and Y      | `=`     |
| `Separator`     | Separator between X and Y in single-line horizontal format          | `, `    |
| `MultiLine`     | `true` = two lines (line break `\P`), `false` = one line horizontal | `false` |
| `ShowLeader`    | Draw a leader from the base point to the text                       | `false` |
| `LeaderEnd`     | Base-point marker: `None` / `Arrow` / `Dot` / `Circle`              | `None`  |
| `LeaderEndSize` | Marker size (ratio to text height)                                  | 0.6     |
| `ShowUnderline` | Draw an underline beneath the text                                  | `false` |

Label format examples via `FormatLabel(x, y)`:

- One line: `X=10.500, Y=20.300`
- Two lines: `X=10.500` / `Y=20.300` (MText line break `\P`)

#### Notes

- The coordinate text is fixed to the value at annotation time — moving the leader or marker afterward does not change the coordinate value.
- The base-point marker is drawn independently of the leader; the arrow points toward the text direction, `Dot` is filled with a SOLID hatch, and `Circle` is drawn empty.
- Settings are kept in `XYSettingsStore.Last` only for the current AutoCAD session and reset when AutoCAD restarts.
- **AutoCAD 2027 compatibility:** Setting `MText.Attachment` directly raises `eInvalidInput` for the alignment value on some versions (e.g. 2027), so alignment is kept at the default (TopLeft) and the box is moved to the bottom-left of the content to get the same result position; the preview (`WorldDraw`) and actual annotation (`PlaceLabel`) use the same calculation.
- All entities follow the current layer (CLAYER) and BYLAYER color via `SetDatabaseDefaults`. Click points are read against the current UCS and transformed to WCS (`TransformBy`) to derive the coordinate value.
- Supported on AutoCAD 2023–2027 (2023/2024 on .NET Framework 4.8, 2025/2026 on net8.0-windows, 2027 on net10.0-windows), auto-loaded via `PackageContents.xml` from the `ApplicationPlugins\XYCoordinates.bundle`.
