# Interactive

Interactive mode lets you place viewports by hand, clicking one after another in Model Space like stamping. The frame size and scale are copied from your source layout's viewport, so every viewport you drop matches it.

Open the window with the **Viewport Generator** ribbon button (or the `VPG` command) and set **Generation Method** to **Interactive**.

### How to use

1. **Open the window** and select **Interactive**.
2. **Set the output** — **Viewport Scale**, **Source Layout**, and **Sheet Prefix / Start** (see the [overview](./) for these shared settings). The frame size comes from the source layout's viewport.
3. **Generate Layouts** — the drawing switches to Model space and a frame follows your cursor.
4. **Place each viewport** — click to drop a frame; repeat for as many as you need.
   * **Change the grip point** while placing by typing `1`–`5`: `1` TopLeft, `2` TopRight, `3` BotLeft, `4` BotRight, `5` Center. Your choice is remembered for the next frame.
   * After each click you can **specify a rotation angle** for that frame, or accept it as-is.
5. **Finish** — press **Enter** or **ESC** to stop. A sheet is created for each frame you placed.

### Notes

* The source layout must contain a viewport — its size and scale define the interactive frame.
* Frames are numbered in the order you click them.
