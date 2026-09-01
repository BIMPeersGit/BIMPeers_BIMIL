---
hidden: true
---

# Settings

Open **Auto Label** from the BIMIL ribbon (or run `BP_ALG` / `ALG`). The window has a selection area, three independent output-property pages, and one shared **Label Style** section.

### Output properties

Use the checkbox beside **Area**, **Length**, or **Radius** to enable that output. Click the property name to show its settings. More than one output can be generated in the same run.

#### Area

<figure><img src="../../../.gitbook/assets/image (102).png" alt="" width="458"><figcaption></figcaption></figure>

| Option        | Description                                                                           | Default              |
| ------------- | ------------------------------------------------------------------------------------- | -------------------- |
| **Values**    | **Each** creates one value per valid object; **Sum** creates one combined area label. | Each                 |
| **Placement** | Place the label automatically at the object center, or pick its location manually.    | Center automatically |
| **Unit**      | Display the result as `m²`, `ft²`, or `ha`.                                           | `m²`                 |
| **Decimals**  | Show 0–7 decimal places.                                                              | 2                    |
| **Separator** | Add comma thousands separators.                                                       | On                   |
| **Label**     | Use **Value + unit**, **Area = value + unit**, or a custom template.                  | Value + unit         |

#### Length

<figure><img src="../../../.gitbook/assets/image (106).png" alt="" width="458"><figcaption></figcaption></figure>

| Option        | Description                                                                                                                      | Default                |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| **Values**    | **Each** labels individual polyline segments or curves; **Sum** creates a perimeter/path-length summary for the selected object. | Each                   |
| **Placement** | Place the label automatically at the midpoint, or pick its location manually.                                                    | Midpoint automatically |
| **Unit**      | Display the value in `mm`, `m`, `in`, or `ft`.                                                                                   | Drawing model unit     |
| **Decimals**  | Show 0–7 decimal places.                                                                                                         | 0                      |
| **Separator** | Add comma thousands separators.                                                                                                  | On                     |
| **Label**     | Use **Value + unit**, **Length = value + unit**, or a custom template.                                                           | Value + unit           |

For a closed boundary, **Sum** represents its perimeter. For an open curve, it represents the full path length. If multiple areas are combined with **Area > Sum**, **Length > Sum** combines the perimeters of those same area objects.

#### Radius

<figure><img src="../../../.gitbook/assets/image (113).png" alt="" width="458"><figcaption></figcaption></figure>

| Option        | Description                                                                   | Default              |
| ------------- | ----------------------------------------------------------------------------- | -------------------- |
| **Placement** | Use the automatic direction, or pick the radius-dimension direction manually. | Center automatically |
| **Unit**      | Display the value in `mm`, `m`, `in`, or `ft`.                                | Drawing model unit   |
| **Decimals**  | Show 0–7 decimal places.                                                      | 0                    |
| **Separator** | Add comma thousands separators.                                               | On                   |
| **Label**     | Use **R + value**, **Value + unit**, or a custom template.                    | R + value            |

### Custom labels

Choose **Custom...** to edit the label template. The preview updates as you type. Use these placeholders:

| Placeholder      | Inserts                                |
| ---------------- | -------------------------------------- |
| `{value}`        | The converted and formatted number     |
| `{unit}`         | The selected display unit              |
| `{value + unit}` | The formatted number and unit together |

The default custom templates are `A = {value} {unit}`, `L = {value} {unit}`, and `R = {value} {unit}`. Click **Reset** to restore the relevant template.

### Label Style

| Option         | Description                                                                                                                |
| -------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Text Style** | Apply an existing drawing text style. A fixed height in that style is used; otherwise Auto Label uses its fallback height. |
| **Color**      | Choose BYLAYER, BYBLOCK, an AutoCAD index color, or a true color.                                                          |
| **Layer**      | Place labels on the current layer, the source object's layer, or another existing drawing layer.                           |
| **Alignment**  | Choose one of nine MText attachment positions, from Top Left through Bottom Right.                                         |

Clicking **Generate** validates the output selection, text style, and selected objects, then saves the settings for the next run.
