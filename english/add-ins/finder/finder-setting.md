# Finder Setting

The Snap View settings panel allows you to fully customize how your view captures behave — from copying and saving to previewing and image quality.

<figure><img src="../../.gitbook/assets/Finder Setting.png" alt="" width="375"><figcaption><p>Finder  Setting</p></figcaption></figure>

## ✅ Settings Overview&#x20;

The Report Setting section allows you to configure **which location information is included in the result.**\
When a checkbox is selected, the corresponding data will be **displayed in the result window and included in the report.**

<table><thead><tr><th width="56.29632568359375" data-type="number">Num</th><th width="128.28582763671875">ITEM</th><th>DESCRIPTION</th></tr></thead><tbody><tr><td>1</td><td><strong>Grid</strong></td><td><p>Returns the name of the <strong>grid line closest to the element’s center point</strong>. Supports vertical, horizontal, and diagonal grids.</p><p><br>Example based on <strong>vertical Grid X1</strong> and <strong>horizontal Grid Y1:</strong></p><table><thead><tr><th>X Direction (Vertical Grid)</th><th>Y Direction (Horizontal Grid)</th></tr></thead><tbody><tr><td>~X1  (left of X1)</td><td>~Y1  (above Y1)</td></tr><tr><td>X1~  (right of  X1)</td><td>Y1~  (below Y1)</td></tr><tr><td>~X1~ (crossing X1)</td><td>~Y1~ (crossing Y1)</td></tr><tr><td>X1~X3 (between X1 and X3)</td><td>Y1~Y3 (between X1 and X3)</td></tr></tbody></table></td></tr><tr><td>2</td><td><strong>Level</strong></td><td><p>Returns the name of the <strong>level that the element belongs to</strong>, based on its elevation.<br></p><p>In Revit, an element’s level information may be interpreted in <strong>two different ways</strong>:</p><ul><li><strong>Level (ref.):</strong> The level explicitly referenced by the element</li><li><strong>Level (geo.):</strong> The level determined by the element’s actual Z-coordinate (geometry-based)</li></ul></td></tr><tr><td>3</td><td><strong>Room</strong></td><td>Provides information about the <strong>architectural room that contains the element</strong>, including room name and number.<br><br>Example : Stock 3, Workshop 4</td></tr><tr><td>4</td><td><strong>Space</strong></td><td>Returns the <strong>MEP space</strong> the element is located in. This is typically used in mechanical, electrical, and plumbing design.<br><br>Example : Elevator Machine Space 12</td></tr><tr><td>5</td><td><strong>Zone</strong></td><td>Returns the <strong>logical MEP zone</strong> that groups multiple spaces for system-level organization (e.g., HVAC zones).<br><br>Example : 6, Zone B, Exhaust Zone</td></tr><tr><td>6</td><td><strong>Area</strong></td><td>Returns the <strong>name or number of the area</strong> that contains the element.<br><br>Example : Service Area 4</td></tr></tbody></table>



