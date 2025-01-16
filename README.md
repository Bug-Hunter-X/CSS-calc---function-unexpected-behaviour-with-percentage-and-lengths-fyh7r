# CSS calc() Function Unexpected Behavior

This repository demonstrates a subtle bug related to using the `calc()` function in CSS with percentages and lengths. The bug arises from the order in which CSS properties are applied.

## The Bug

The issue occurs when attempting to calculate a width based on a percentage of the parent element's width, while also considering padding and border widths.

The provided `bug.css` file contains a CSS snippet that illustrates this. The `calc()` function is used to set the width of an inner element based on the parent's width, subtracting a fixed amount.

However, the calculation is performed *before* the padding and border are applied to the parent. This leads to an unexpected outcome where the inner element's width is smaller than intended.

## The Solution

The `bugSolution.css` file offers a corrected approach. By explicitly adding the padding and border values to the calculation within the `calc()` function, the width is accurately determined, addressing the layout inconsistency. This ensures the inner element's width is accurately calculated, considering padding and border.