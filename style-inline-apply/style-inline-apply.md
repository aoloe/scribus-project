# Apply styles inline

Show a popup that with a fast way for applying paragraph and character styles

## Implementation

Create a plugin that

- shows a popup above (or below if too close to the window border?) cursor position,
- gets the focus in a combobox with filtering and
- lets the user type a part of a style name that is matched with the existing paragraph and character styles;
- ok applies the style to the selection / paragraph, esc cancels.
- It should work in text edit mode and when a text frame is selected.

Challenges:

- add a shortcut in text edit mode, that fires up a dialog.
- place the popup somewhere near the cursor / selection without covering it.

## Notes

- The dialog should be really minimalistic
- Pressing the down arrow on an empty search box should show all options.
- The same mechanisme can be used for applying the advanced text properties.
- No mouse click should be necessary
- <http://stackoverflow.com/questions/1613245/can-i-make-qcompleter-complete-inline-and-show-a-popup>
- <https://github.com/scribusproject/scribus/issues/56>
