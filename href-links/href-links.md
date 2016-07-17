# Href links

Currently, you have to use the tool from the pdf toolbar to create a link frame that is placed on top of the area to be linked.

This projects aims at making every frame, shape and text selection clickable.

Two ways of implementing it:

- adding the links settings to the / an extended references manager
- adding the links to (a new tab of) the properties palette.


## Notes

- A text frame cannot have its own link, if it contains links (and you cannot add links if the text frames is already a link)
- The current link item will be removed and conversion from old files will conver them in rectangular shapes. 
- A first step could be to implement the links for the table of contents first (no UI needed).
