# How to Use

### 1️⃣ Select a Box

* **Requirement**: In the 3D view, select **exactly one** Section box or Scope box.

### 2️⃣ Display UI & Configure Options

When you run the Add-in, the following panel appears—configure as needed:

<figure><img src="../../.gitbook/assets/Box To View UI (1).png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="40" align="center">Callout</th><th width="168.48486328125">UI Element</th><th>Description</th></tr></thead><tbody><tr><td align="center"><strong>1</strong></td><td><strong>Direction</strong></td><td>Lists all six faces (Top, Bottom, Front, Back, Left, Right).</td></tr><tr><td align="center"><strong>2</strong></td><td><strong>Locate (Show)</strong></td><td>Click to preview that face—the face surface is highlighted in <strong>red</strong> in the current 3D view.</td></tr><tr><td align="center"><strong>3</strong></td><td><strong>Generate toggle</strong></td><td>Turn on (blue) or off (grey) to include or exclude each face from view generation.</td></tr><tr><td align="center"><strong>4</strong></td><td><strong>View Type</strong></td><td>Choose the view style for each face: <br>• <strong>Top</strong> → Floor Plan, Structural Plan, Section<br>• <strong>Bottom</strong> → Ceiling Plan, Section<br>• <strong>Front / Back / Left / Right</strong> → Section, Elevation, Detail View</td></tr><tr><td align="center"><strong>5</strong></td><td><strong>View Template</strong></td><td><p>Choose its View Template.</p><p>(only shows templates for the selected View Type)</p></td></tr><tr><td align="center"><strong>6</strong></td><td><strong>View Name Prefix</strong></td><td>Enter a prefix for all generated views (e.g. <code>Box To View_Top</code>).</td></tr></tbody></table>

### 3️⃣ Generate Your Views

Click **Generate** to create one view per selected face. \
Names follow `<Prefix>_<Direction>`, with `_1`, `_2` added for duplicates.\
(e.g. `Box To View_Top, Box To View_Right, Box`)&#x20;
