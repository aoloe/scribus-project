# Vector frames

Add vector frames.

- All the shapes are contained in the frame
- Render the SVG as a bitmap or as a group on the canvas
- Color in vector drawigns inside of a frame, are not "visible" from the document.
- There should be a way to import single colors from the loaded SVG (or is the color picker enough?)
- vector frames come from an SVG/PDF or are calculated (like for render frames)
- optionally cache the transformation from SVG/PDF to SLA

## Notes

- A vector frame could have a creator, as an example the barcode generator and could be editable by "external" applications.

Well, one thing would be to import. That is, convert everything to native objects. With, finally, a possibility of opening a color&fill dialog. I hate when scribus just adds new swatches.

details to be defined:
- what happens with the colors.
- how is the color management applied...
- fonts...

- at some time scribus will have to convert the vector to internal objects in order to create the pdf. (librsvg?)

- The other is more like "smart" object feature of Adobe CS. Render as is and monitor changes of the original object
  - just convert it to an image with desired resolution and let scribus handle that from there
  - how to implement CMS?
  - could be done with a new item in the render frame. (can we mak it look like regular image frame for the user?)

- editing:
  - in scribus by doing a "real" import (you get a group of items, and lose the link)
  - in an external editor (like it's done for bitmap images)
  - could eventually support more svg effects than scribus can
