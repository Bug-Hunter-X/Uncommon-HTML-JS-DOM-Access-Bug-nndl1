# Uncommon HTML/Javascript DOM Access Bug

This repository demonstrates a subtle bug that can occur when accessing elements in the Document Object Model (DOM) before they are fully loaded. The issue is particularly relevant to scripts that run before the HTML elements are completely parsed by the browser.

## Bug Description

The primary issue lies in the timing of the Javascript execution. The script attempts to access the element with the id "myDiv" before the browser has finished rendering the HTML. This leads to the script encountering a null value, potentially resulting in a runtime error or incorrect behavior.  This problem occurs when scripts are put into the `<head>` instead of the `<body>` before the element exists.