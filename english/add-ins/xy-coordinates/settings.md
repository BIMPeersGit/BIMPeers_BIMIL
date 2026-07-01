---
hidden: true
---

# Settings

Open the settings window with the **Settings** ribbon button (or the `XYCoordinatesSettings` / `XYS` command), adjust the options, and click **Apply** — the values are saved for the AutoCAD session and used the next time you pick coordinates. The window is grouped into **TEXT**, **FORMAT**, and **ANNOTATION**.

### TEXT

| Option                          | Description                                                  | Default   |
| ------------------------------- | ------------------------------------------------------------ | --------- |
| **Height**                      | Text height of the coordinate label.                         | 100       |
| **Decimals**                    | Number of decimal places shown for the X and Y values.       | 0.000 (3) |
| **Put X / Y on separate lines** | On writes X and Y on two lines; off writes them on one line. | On        |

### FORMAT

| Option               | Description                                                                                                                       | Default     |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| **Delimiter (X, Y)** | The symbol between each axis letter and its value — `=`, `.`, or `:`. Same for X and Y.                                           | `=`         |
| **Separator**        | The divider between X and Y when they are on one line — Comma, Space, or Slash. Ignored when _Put X / Y on separate lines_ is on. | Comma ( , ) |

### ANNOTATION

| Option                  | Description                                                                                                                                                             | Default |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| **Size**                | Size of the base-point marker, as a ratio of the text height.                                                                                                           | 0.6     |
| **End mark**            | Marker drawn at the base point — **None**, **Arrow**, **Dot** (filled), or **Circle** (empty). Drawn whether or not the leader is on; the arrow points toward the text. | None    |
| **Line under text**     | Draws an underline beneath the coordinate text.                                                                                                                         | On      |
| **Leader line**         | Draws a leader from the base point to the text.                                                                                                                         | On      |
| **Group line and text** | Groups the coordinate text with its leader/underline/marker so they select and move together.                                                                           | Off     |

### Label format

The label is built as `X<delimiter><value><separator>Y<delimiter><value>`:

- One line: `X=10.500, Y=20.300`
- Two lines: `X=10.500` / `Y=20.300`
