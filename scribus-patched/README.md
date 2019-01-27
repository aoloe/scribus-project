# A patched version of Scribus

The official bug tracker is full of patches that have not (yet) been applied to the Scribus trunk.

Publishing a patched version of Scribus, can give the users a chance to try new features and for the developers to easily see how the patches affect Scribus.

https://github.com/impagina/scribus

## Applied patches

## Patches to be applied

- snap to item on shift
  - https://bugs.scribus.net/view.php?id=15228
- mulitple duplicate on pages
  - https://bugs.scribus.net/view.php?id=15438
- styles apply
  - needs the scripter API
- action search
  - https://bugs.scribus.net/view.php?id=15552
- content panel
- store the expand status from the text palette
  - https://bugs.scribus.net/view.php?id=15553
- do not reset the image position when loading an image over an existing one
  - https://bugs.scribus.net/view.php?id=12253
- do not overflow images that are set to fit the frame
  - https://bugs.scribus.net/view.php?id=15448

## Existing possible patches

## Patches that would be easy to create

### Toolbars and palettes

- by default show the properties palette docked to the right
  - https://bugs.scribus.net/view_all_bug_page.php?page_number=3
- by default shoe the tools toolbar on the left and hide the other ones
- remove some tools from the toolbar (only reachable from the insert menu; eventually add a draw toolbar)
  - hand drawing
  - callygraphy
  - polygon
  - arc
  - spyral
  - barcode
  - remove the pull down on the shape button

### Guides and snapping

- snap to items should only snap to visible items
- remove snap to item modus
  - https://bugs.scribus.net/view.php?id=15230
- guides snap to item on shift
  - https://bugs.scribus.net/view.php?id=10988
- while dragging a guide, pressing ESC should cancel the action
  - https://bugs.scribus.net/bug_update_page.php
- axis snap to margin, guides and items
  - https://bugs.scribus.net/view.php?id=15268
- add a key for a temporary enabling / disabling of all snapping
  - https://bugs.scribus.net/view.php?id=15442

### Duplicating and autotext

- remove the automatic text frames from the UI
- remove "insert > frames" from the UI

### Preview, print and export

- remove "file > print" from the UI
- create a "file > print" that launches a pdf viewer in the background to do the printing
- move the export to pdf outside of the file > export menu and rename it "create pdf"
  - https://bugs.scribus.net/view.php?id=15396
- by default allow editing in preview mode
  - https://bugs.scribus.net/view.php?id=12464
- remove "file > print preview"
  - eventually use the code to create a separate tool with the same features

### Image frames

- a button for resetting the the image position and size in the frame
- when an image is set to fit the frame, it should just fit it
  - https://bugs.scribus.net/view.php?id=15448
- add a fill frame option in the image frame scaling
  - it should only be possible to move the image inside of the frame in one direction and no padding can appear.
  - https://bugs.scribus.net/view.php?id=15437
  - create three horizontal buttons for the three fitting options (instead of three radio buttons)
- fit to content for both text and image frames
  - https://bugs.scribus.net/view.php?id=15240
- context menu: move the content of "image" into "content"
  - https://bugs.scribus.net/view.php?id=15197
- adjust image to frame should not activate "scale to frame size"
  - https://bugs.scribus.net/view.php?id=14780

### Text frames

- add a "edit" entry before the "edit with story editor"

### Tools and items

- Experimental features must be invididually enabled before they show up in the UI
  - Tables
  - Export of image PDFs as vectors
- Remove every reference to the free hand line tool (imported free hand lines can be deleted but not edited)
### Other

- inspect, not outline
  - https://bugs.scribus.net/view.php?id=15196
- simplify the context menu
- rename the "background" layer to something else
  - default
  - https://bugs.scribus.net/view.php?id=14607
- Enable click and drag when importing a vector file (+ ability to set a specific size)
  - https://bugs.scribus.net/view.php?id=10995

## Patches that we dream of

- a clippy
  - show possible modifier
  - a picker / inspector to get help on UI items
  - a "short help" browser
  - http://doc.qt.io/qt-5/qwhatsthis.html
- a flatplan to replace arrange pages
  - vertical and horizontal layout
- allow relative paths for images (and fonts)
  - https://bugs.scribus.net/view.php?id=9056
- search and replace the whole document
- unify the bezier and line tool

## Patches that are hard to create / maintain
