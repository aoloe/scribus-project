# Zoom


- when zooming with the scrollwheel, the cursor position should be used as a reference
- when zooming with the +/- shortcuts, the current behavior using the selection as a reference is ok
- when using the spinboxes in the status bar it should use the center of the viewport
- use more sane steps (<http://bugs.scribus.net/view.php?id=10171>, http://bugs.scribus.net/view.php?id=10978)

## The current situation

currently, there are lot of ways of zooming a document, and most of them do not work in a 100% satisfying way.

- navigation
- main toolbar
- status bar
- scroll wheel
- keyboard shortcuts

on the one side, we want to reduce the number of ways of doing exactly the same thing and on the other make each tool and the full zoom experience better and reliable.

## Current issues

- It's almost impossible to use ctrl-scroll on a laptop.
- The default the zoom steps are not considered as very usable.

## Whishes

## Draft proposal

### The mouse wheel

- ctrl-scroll should zoom in and out.
- if an item is selected fit to width and fit to height could be added as additional steps.
- the zoom should use the cursor position as a reference.
- we should have better zoom steps.

### Status bar

- remove the +/- lens buttons
- eventually remove the 1 lens button
- add a button to define the zommed area.
- clicking on an item will make  the zoom area fit to it.
- when the zoom tool is active, the scroll wheel should zoom in and out (without modifiers)
- get the up and down arrow keys to work in the text spinbox

The current layout can be moved to a Zoom toolbar
