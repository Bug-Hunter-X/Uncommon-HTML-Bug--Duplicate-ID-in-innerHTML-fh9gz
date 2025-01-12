# Uncommon HTML Bug: Duplicate ID in innerHTML

This repository demonstrates an uncommon bug in HTML related to the use of `innerHTML` to add elements to the DOM.  The bug arises from adding an element with an ID that already exists in the DOM, which can lead to unpredictable behavior and issues with JavaScript interactions.

## Bug Description
The bug occurs when using `innerHTML +=` to append HTML content to an existing element and you inadvertently introduce a duplicate `id` attribute. This violates the fundamental rule that IDs must be unique within an HTML document.  Browsers will handle this inconsistently.  Usually one of the elements will be accessible with `getElementById` and the other is ignored. This inconsistency can make debugging difficult.

## Solution
The solution involves avoiding the use of `innerHTML` for adding elements when possible. This ensures that you do not accidentally introduce duplicate IDs or other structural issues.  Use DOM manipulation methods like `createElement`, `appendChild`, etc for better control and reduced error risk.