# Easy Hacks for Scribus

This is a temporary static collection of easy hacks for Scribus.

## General topics

- Bug Tracker: [DELETE key in "Edit Image" mode should empty image frame](http://bugs.scribus.net/view.php?id=11526)
  - Understand what is the edit modus for images.
  - Understand the patch.
  - Improve the patch.
- Bug Tracker: [Improve access to contour editing](http://bugs.scribus.net/view.php?id=10409)
  - Understand what the issue is with the hyphenation.
  - Understand the patch.
  - Improve the patch and make it work with the current trunk.
- Bug Tracker: [No page range check in PDF export dialog](http://bugs.scribus.net/view.php?id=11818)
  - Understand what the issue is with the range checking.
  - Understand the discussion in the ticket.
  - Understand the patch.
  - Define the behavior to be implemented.
  - Improve the patch and make it work with the current trunk .
- Bug Tracker: [Check "select all" on styles import](http://bugs.scribus.net/view.php?id=10455)
  - Understand the issue.
  - Understand the patch.
  - Make sure that the new behavior is a desired one.
  - Make sure that the patch works with the trunk.
- Bug Tracker: [Scrapbook: name of element is too much summarized](http://bugs.scribus.net/view.php?id=11624)
  - Understand the issue
  - Propose a set of solutions for discussion
  - Create a patch
- Bug Tracker [Missing error message when pasting on locked background shape](http://bugs.scribus.net/view.php?id=9588)
  - Understand the issue
  - Propose a set of solutions for discussion
  - Create a patch
- Bug Tracker: [ Adapt images to frame should reset offest](http://bugs.scribus.net/view.php?id=12980)
  - Understand the issue
  - Define the behavior to be implemented.
  - Create a patch
- Bug Tracker [Move vector dialog lacks "OK" and "Cancel" buttons](http://bugs.scribus.net/view.php?id=12761)
  - Understand the issue
  - Create a patch
- Bug Tracker [add width and height variables in the x-pos and y-pos fields of the PP](http://bugs.scribus.net/view.php?id=12683)
  - Understand the issue.
  - Understand how width and height variables are defined in Scribus.
  - List the variables that should be added to this context.
  - Create a patch.
- Bug Tracker [It’s possible to create various objects with the same name](http://bugs.scribus.net/view.php?id=11926)
  - Understand the issue.
  - Define the behavior to be implemented.
  - Create a patch.
- [Export and import the hyphenator's exceptions](https://github.com/aoloe/scribus-project/blob/master/hyphenator-export-exceptions/hyphenator-export-exceptions.md)
  - Understand the issue.
  - Create a mockup of the dialog.
  - Extend the dialog.
  - Implement the actions.
- [Print through PDF](https://github.com/aoloe/scribus-project/blob/master/print-through-pdf/print-through-pdf.md)
  - Understand the issue
  - Create a mockup of the dialog.
  - Implement the actions.
  - Add the prefences.

## Involving text rendering

- Bug Tracker: Prevent hyphenation ona per-word bases [[#4676]]() [[10517]](http://bugs.scribus.net/view.php?id=10517)
  - Understand what the issue is with the hyphenation.
  - Understand the patch.
  - Improve the patch and make it work with the current trunk.
- Bug Tracker: [Hyphenation control in the paragraph styles](http://bugs.scribus.net/view.php?id=11370).
  - Understand the patch.
  - Improve the patch and make it work with the current trunk.
- [make sure that all control characters have a (good) representation](https://github.com/aoloe/scribus-project/blob/master/control-characters/control-characters.md)
  - Understand the issue.
  - Propose a set of solutions for discussion
  - Create a patch.
- Convert column and rows guides to real guide
  - Understand the issue.
  - Create a mockup of the dialog.
  - Extend the dialog.
  - Implement the actions.
- [Replace missing glyphs with a different font](https://github.com/aoloe/scribus-project/blob/master/replace-missing-glyphs/replace-missing-glyphs.md)
  - Understand the issue.
  - Check how the preflight verifier finds the missing glyphs.
  - Create a mockup of the preferences dialog.
  - Create the dialog.
  - Implement the actions.
- [separate text and frame transparencies](https://github.com/aoloe/scribus-project/blob/master/text-transparency/text-transparency.md)
  - Understand the issue.
  - Understand how transparency is implemented.
  - Tweak the relevant dialogs.
  - Implement the actions.
- [Improve the zoom behavior](https://github.com/aoloe/scribus-project/blob/master/zoom/zoom.md)
  - Understand the issue
  - List the tasks to be done
  - Implement the actions

## Not so Hard Hacks

- [Align the image in its frame](https://github.com/aoloe/scribus-project/blob/master/align-image-in-frame/align-image-in-frame.md)
  - Understand the issue.
  - Create a mockup of the dialog.
  - Extend the dialog.
  - Implement the actions.
- [Frame styles](https://github.com/aoloe/scribus-project/blob/master/frame-styles/frame-styles.md)
  - List frame properties that could be defined in styles
  - Create a mockup of the dialog
  - Add the dialog to the styles editor
  - Implement the actions.
- [Rotate the image in the frame](https://github.com/aoloe/scribus-project/blob/master/image-rotation/image-rotation.md)
  - Understand the issue.
  - Create a mockup of the view.
  - Extend the view.
  - Implement the actions.
- [Use LanguageTool for proofreading](https://github.com/aoloe/scribus-project/blob/master/language-tool/language-tool.md)
  - Understand the issue.
  - Create a mockup of the view.
  - Understand how text is rendered.
  - Implement the actions.
- Add "+" buttons to create resources
  - Understand the issue
  - Find the cases where it should be applied (colors, styles, ...)
  - Define how the dialog can be shown.
  - Create a mockup of the views.
  - Extend the view.
  - Implement the actions.
- [Styles based table of contents](https://github.com/aoloe/scribus-project/blob/master/table-of-contents/table-of-contents.md)
  - Understand the issue
  - Understand how scribus-ece does it.
  - Define a set possible implementations.
  - Create mockups for the dialogs
  - Implement the actions and dialogs.
- [Vector frames](https://github.com/aoloe/scribus-project/blob/master/vector-frames/vector-frames.md)
  - Understand the issue
  - Understand how frames are implemented
  - Understand how vectors are imported
  - Define a set possible implementations.
  - Create mockups for the dialogs
  - Implement the actions and dialogs.