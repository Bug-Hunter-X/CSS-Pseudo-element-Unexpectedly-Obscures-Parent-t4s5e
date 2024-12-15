# CSS Pseudo-element Covering Parent Element

This repository demonstrates a CSS issue where a pseudo-element (:before) unexpectedly covers its parent element, even without any explicit positioning properties set on either the parent or the pseudo-element.

## Bug Description

A simple div with a :before pseudo-element is used. The pseudo-element, despite having no positioning properties, covers the entire parent div. This behavior is counterintuitive, as one would expect the pseudo-element to be contained within the parent element's bounds.

## Reproduction

1. Clone the repository.
2. Open `bug.css` and `bugSolution.css` to see the issue and its solution, respectively.
3. Load `bug.css` or `bugSolution.css` in a browser and observe the results.

## Solution

The solution involves explicitly setting the `position` property of the parent element to `relative`. This forces the parent element to act as a containing block for the pseudo-element.