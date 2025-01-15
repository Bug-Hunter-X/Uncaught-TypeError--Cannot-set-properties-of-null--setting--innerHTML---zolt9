# Uncommon HTML Error: Accessing Non-Existent Element

This repository demonstrates a common yet subtle error in HTML/JavaScript: attempting to manipulate a DOM element before it's fully loaded.  The error manifests as `Uncaught TypeError: Cannot set properties of null (setting 'innerHTML')`.

## The Bug

The `bug.html` file contains the problematic code.  The script attempts to access and modify the `myDiv` element before the HTML parser has completed adding it to the Document Object Model (DOM).

## The Solution

The solution, in `bugSolution.html`, uses the `DOMContentLoaded` event listener to ensure that the script executes only after the entire HTML document is parsed and the DOM is ready.  This prevents the `null` reference error.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in your web browser.  You'll see the error in your browser's developer console.
3. Open `bugSolution.html`. This version works correctly.