# A new story editor

The current story editor has been created because Scribus was not good enough for in frame editing.

Since the in frame editing has largely improved over the years, we should define what are the new specifcations for a story editor and start from scratch a new implementation.

## Create a prototype

We should create a standalone application that could be later converted into a Scribus plugin.

- read and write html + css.
- create a table with the matching scribus and css properties.
- do not display the html and css but marks with stating what the applied format is.
- allow to create new character and paragraph styles
- allow applying character and paragraph formatting
- do not allow local standard formatting
  - font
  - font size
  - underline
  - ...
- allow local advanced typographical formatting:
  - letter distance, ...

## Notes

- should it a Scribus plugin or an external application
- Use cases:
  - showing the formatting as tags
  - editing text that is hard to edit in the frame:
    - some rotated text
