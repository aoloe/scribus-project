# Rotate the image in the frame

Make it possible to rotate an image inside of an image frame.

In 1.5svn there is a basic implementation of this feature (cf. the "Rotation" field in the "Image" tab of the Properties Palette.

There are a few improvements that can be done:

- adding a visual way of rotating the image (eventually by also enhancing the frame rotation itself)
- use the base point of the frame for the rotation (or, eventually, define an own base point, taking the frame's one as the default)
- add the command to the scripter API
- add a setting (or a way) to rotate the frame without rotating the image inside of it
