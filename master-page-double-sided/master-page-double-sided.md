# Double sided master pages

For double sided document, it should not be possible to edit Master pages in a single sided way.

The master pages should be shown in the same way as on the normal canvas and a left and right version of the master page should be autoamtically created from what is layouted.

Ideas:
- Scribus could allow two master pages to have the same name, if they are of different type (left, right)

Tasks:
- Implement the new view
- Tweak the "apply" and "edit" master pages dialogs to reflect the changes
- Make sure that old documents can still correctly be used and are automatically converted to the new schema
