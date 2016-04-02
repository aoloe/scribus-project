If an image overflows the frame, offer the option to crop it to the frame's size.


## Notes

- choice to use a linked image or an embedded one (default is the current setting).
- keep in the `.sla` the original link to the original image or originally embedded one.
- allow to restore the original image (by keeping the original crop and resolution).
- if an image file is created, put the size and position in its name and place it nearby to the original one or close to the `.sla` (ask to overwrite older files with the same name or fail, do not try to find alternatives).
- for jpg images, we might ask for the compression settings to be aplied (if no 1:1 crop is possible).
- the size of the image is the bounding box of the frame and the image must be correctly placed in the frame.
