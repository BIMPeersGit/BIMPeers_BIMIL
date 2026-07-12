# Array (Grid)

Array (Grid) takes a single base frame and repeats it into a regular grid of viewports, so you can lay out many equally spaced sheets from one source without drawing every frame by hand.

Open the window with the **Viewport Generator** ribbon button (or the `VPG` command) and set **Generation Method** to **Array (Grid)**.

### How to use

1. **Open the window** and select **Array (Grid)**.
2. **Pick the base frame** — click **Select Base Frame** and pick one polyline. Its size is shown as _Base Width_ / _Base Height_.
3.  **Set the grid:**

    | Field           | Meaning                                                                                                  |
    | --------------- | -------------------------------------------------------------------------------------------------------- |
    | **Rows / Cols** | The number of viewports down and across.                                                                 |
    | **X Offset**    | Horizontal spacing between frames. Use the 📍 button to measure it between two points instead of typing. |
    | **Y Offset**    | Vertical spacing between frames, measurable the same way with 📍.                                        |
4. **Set the output** — **Sorting Direction**, **Viewport Scale**, **Source Layout**, and **Sheet Prefix / Start** (see the [overview](./) for these shared settings).
5. **Generate Layouts** — the base frame is copied across the grid and a sheet is created for each copy.

### Notes

* When you pick the offset with the 📍 button, the sign (+ / −) is set automatically from the direction you measure in.
* The offsets are the spacing between frames — set them larger than the base width/height to leave a gap between copies.
