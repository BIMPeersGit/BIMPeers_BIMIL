---
description: Filter elements by their parameter values.
---

# Parameter Filter

**Parameter Filter** allows users to filter elements based on their instance parameter values, offering more advanced and refined filtering options. This feature enables users to create custom conditions and search for elements that meet specific parameter criteria, enhancing control and flexibility.

## **Features**

* **Parameter-Based Search:** \
  Filter elements by instance parameter values. The filter displays a list of parameters available in the current search scope.
* **Condition-Based Filtering:** \
  Choose from 8 default conditions and 4 additional conditions for numeric parameters. Users can input values or select True/False conditions for applicable parameters.
* **Custom Logic:** \
  Use AND/OR conditions to combine parameter criteria for more refined filtering.
* 세팅 저장:\
  Parameter Filter에 작성한 조건을 Import Export 가능.&#x20;

## **Notes**

* If a parameter not found in the current scope is selected, or an invalid value (such as text for numeric parameters) is entered, the condition is ignored and highlighted in red.
* When filtering numeric parameters, results are based on project units. For non-decimal unit settings (e.g., feet-inches), the original values are used for comparison.
* Only instance parameters can be filtered, and type parameters are excluded.
