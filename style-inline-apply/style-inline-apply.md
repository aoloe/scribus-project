# Apply styles inline

Show a popup that with a fast way for applying paragraph and character styles

## Implementation

Create a plugin that

- shows a popup above (or below if too close to the window border?) cursor position,
- gets the focus in a combobox with filtering and
- lets the user type a part of a style name that is matched with the existing paragraph and character styles;
- ok applies the style to the selection / paragraph, esc cancels.

## Notes

- The dialog should be really minimalistic
- Pressing the down arrow on an empty search box should show all options.
- The same mechanisme can be used for applying the advanced text properties.
- No mouse click should be necessary
