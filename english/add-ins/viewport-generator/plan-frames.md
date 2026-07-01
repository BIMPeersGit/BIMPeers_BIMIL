---
hidden: true
---

# Plan Frames

Plan Frames is the default mode. It turns polyline frames you have already drawn in Model Space into viewports in a single pass — one sheet per frame — following the true outline of each frame, whether it is a rectangle or an irregular shape such as an L-shape or a stair plan.

Open the window with the **Viewport Generator** ribbon button (or the `VPG` command) and keep **Generation Method** on **Plan Frames**.

### How to use

1. **Open the window** and select **Plan Frames**.
2. **Choose how to pick the frames:**
   * **Directly Select** — click **Select** and pick the polyline frames in the drawing. The count is shown as *Selected : N*.
   * **Select by Layer** — choose a **Target Layer** to use every polyline on that layer as a frame.
3. **Set the frame options** (optional):

   | Option                  | Effect                                                                                             |
   | ----------------------- | -------------------------------------------------------------------------------------------------- |
   | **Snap to Orthogonal**  | For a rotated frame, rotates the viewport in 90° steps so the drawing inside sits upright.          |
   | **Use Bounding Box**    | Ignores the frame's rotation and uses the smallest upright rectangle that fully contains the frame. |
4. **Set the output** — **Sorting Direction**, **Viewport Scale**, **Source Layout**, and **Sheet Prefix / Start** (see the [overview](README.md) for these shared settings).
5. **Generate Layouts** — one sheet is created per frame, named and ordered by your output settings.

### Notes

* You can pre-select frames before running the command; they are picked up automatically.
* Irregular and non-rectangular frames are followed exactly.
