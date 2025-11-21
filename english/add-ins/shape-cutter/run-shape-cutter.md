# Run Shape Cutter

The **Shape Cutter** add-in simplifies the process of separating disjointed profiles within a single element into individual components. Here’s how the feature operates and what happens during execution:

## **How to Use**

1. **Select the Target Element**:\
   Begin by selecting one or more elements containing multiple disjointed profiles. The add-in supports batch processing of multiple elements simultaneously.
2. **Run the Add-In**:\
   Click the **Shape Cutter** button to execute the operation. The add-in will process all selected elements, separating their disjointed profiles into individual elements.
3. **Post-Execution Selection**:\
   Once the operation is complete, all newly separated elements will automatically be selected. This ensures that users can immediately review, manipulate, or apply further modifications to the newly created elements.

## **What Happens During Execution**

* **Element Analysis**:\
  The add-in identifies disjointed profiles within each selected element. Profiles that are geometrically separate are treated as individual components during processing.
*   **Separation Process**:

    Each disjointed profile is converted into a separate element. The resulting elements inherit geometry and parameter data based on the original elements, depending on the 'Shape Cutter Setting' configurations:<br>

    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

    * **Copy Parameters from the original element**: When selected, parameters (instance properties) from the original elements are applied to the newly created elements.
    * **Delete the original element**: If enabled, the original elements are removed after the separation process.


* **Compatibility and Limitations**:
  * Works only with floors, ceilings, and structural slabs.
  * Elements with slopes are not supported and cannot be processed.
