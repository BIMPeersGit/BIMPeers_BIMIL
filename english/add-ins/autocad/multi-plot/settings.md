---
hidden: true
---

# Settings

<figure><img src="../../../.gitbook/assets/image (1).png" alt="" width="510"><figcaption></figcaption></figure>

\
\
Open **Multi Plot** from the BIMIL ribbon, or run `BP_MTP` / `MTP`. The window is organized around the page setup, reference frame, DWG queue, output folder, and plot status.

### Plot Setup

Choose the AutoCAD Model page setup that Multi Plot should apply to every matching frame. The list includes **Current Model Setup** and named Model page setups from the active drawing.

* **Current Model Setup** uses the active drawing's current Model layout plot settings.
* Named setups copy the selected setup onto the Model layout before plotting.
* The summary line shows the selected plot device and media name.

Click **Edit** to open AutoCAD Page Setup for the active drawing. If a named setup is selected, Multi Plot applies that setup to the Model layout before opening Page Setup. When the AutoCAD Page Setup command finishes, Multi Plot returns to the window and refreshes the setup list.

### Reference Frame

The reference frame defines which objects will be treated as sheets in each DWG.

* **Select Object** lets you pick a frame object from the current drawing.
* **Select DWG** reads a reference drawing and uses the largest usable frame found in Model Space.
* The reference summary shows the frame type or block name, layer, frame size, and matched count.
* Supported frame sources are block references, curves, and regions with valid extents.

For block references, Multi Plot matches the same block name and a similar frame size. For other supported object types, it matches the same object type, layer, and similar frame size.

### DWG queue

Use **Add DWG** to add one or more target drawings. Duplicate files and non-DWG files are ignored.

* **DWG** shows the drawing file name.
* **Frames** shows how many matching frames were found in the file.
* **Copies** sets the number of times each matching frame should be plotted for that DWG.
* **Status** shows whether the drawing is ready, missing, has no matching frames, failed to scan, or is currently plotting.
* The delete button removes a drawing from the queue before plotting starts.

The queue can be sorted by DWG, frame count, or status.

### Output

The output folder is used when the selected plot device creates files, including PDF, DWF, JPG, JPEG, PNG, and XPS devices. If the selected device is a printer or another direct output device, the output folder is disabled and the plot is sent directly to that device.

For PDF output, Multi Plot creates a combined PDF for each DWG. For other file devices, each sheet is written as a separate numbered file.

### Start Plot

Click **Start Plot** after a page setup, reference frame, and at least one matching DWG are ready. Multi Plot opens each target drawing as needed, plots every matching frame, reports skipped sheets or files, and closes drawings it opened for the batch without saving changes.

During plotting, a progress window shows the current sheet and overall progress. The plot can be canceled from the progress window.
