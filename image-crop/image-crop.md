If an image overflows the frame, offer the option to crop it to the frame's size.

Exporting to pdf could have an option to crop the images to the visible part.

## Notes

- choice to use a linked image or an embedded one (default is the current setting).
- keep in the `.sla` the original link to the original image or originally embedded one.
- allow to restore the original image (by keeping the original crop and resolution).
- if an image file is created, put the size and position in its name and place it nearby to the original one or close to the `.sla` (ask to overwrite older files with the same name or fail, do not try to find alternatives).
- for jpg images, we might ask for the compression settings to be aplied (if no 1:1 crop is possible).
- the size of the image is the bounding box of the frame and the image must be correctly placed in the frame.
- Nermander says in the forum: "Lossless cropping of images in exported PDF is on the wishlist. JPEG is the major problem, but they can (if I recall correct) be losslessly cropped by allowing up to 15 or 16 pixels outside the visible part to remain."
  - http://nodivisions.com/photos/apps/lossless-cropping/
- cropping when exporting to pdf will have to make sure that images used multiple times (but only inserted once as resource in the pdf) are not crop in a way that content is lost.
- a perl script for cropping images in a sla:
  - https://photo.m-j-s.net/blog/2016/05/blurb-pdf-upload/
  - https://github.com/phtnnz/perl-scripts/blob/master/scribus-crop.pl
