---
description: Quickly filter and select elements using customizable criteria.
---

# Filter+ Basic

**Filter+ Basic** is a Revit add-in that allows users to efficiently filter and select elements. The process involves three steps: selecting the search scope, defining the filter criteria, and choosing the desired elements from the results table.

## Features

* **Select Search Scope:**\
  Choose from All, Active View, or Selected Elements to define the search range. If there are changes in the model while the add-in is active, click the refresh button to update the data.
* **Results Table:**\
  The results table displays filtered elements using columns for Category, Family, Type, and Element ID. Use the eye icon on the right to focus on a specific element in the current view. You can group elements by dragging columns to the top. Select elements by checking their checkboxes and clicking the Select button to select them in Revit.
* **Set Filter Criteria:** \
  Criteria are set through the following filter types:
  1. Category Filter:\
     Quickly view all elements within the search scope without specifying additional criteria.
  2. Material Filter:\
     Displays a list of all materials used by elements within the specified search scope. Select the desired material to filter the results to show only elements using that material.
  3. Parameter Filter:\
     After adding a condition and clicking Apply, only elements that meet the specified condition will be displayed. You can select parameters available in the current search scope, and only elements that have the parameters added to the conditions will be filtered.

## Notes

* If a parameter not present in the current search scope is selected or an invalid value for the parameter type is entered, the condition will be ignored and highlighted in red.
* Revit may contain multiple parameters with the same name. Selecting the desired category first will help ensure the correct parameter is chosen.
* When filtering by numeric parameters, the search will match values based on the rounded values according to the project units. If the units cannot be rounded to a decimal, the search will use the original values.
* Only instance parameters can be filtered; type parameters are not included in the parameter filter.

{% embed url="https://www.youtube.com/watch?t=5s&v=2a1BU3-44rI" %}
