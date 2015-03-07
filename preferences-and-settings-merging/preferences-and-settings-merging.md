# Merging the preferences and document settings dialogs

It's always hard to explain the people what's the difference between the preferences and the document settings.

This project tries to define how the two dialogs could be merged.

## Concept

- There is only one dialog for all the settings that relate to the content.
- Eventually, we still want a "Preferences" dialog for things UI tab, the shortcuts, the external tools, Scripter, and other settings that are not related to the content in any way (and that cannot be saved on a per document base). In this case it would be probably better to call the unifed dialog "Document settings".
- All sections are always shown.
- There is a place in the dialog where you can:
  - switch between the general settings and the current document's one
  - revert the current document values to the general settings or promote the current values to be the default ones.
  - on a per tab or per section basis
  - if the current section does not have general or document settings, the buttons will be replaced by a text telling it to the user.
  - if you have switched between the general and document settings, the choice will be retained when switching to another tab or section. The choice could be respected when reopening the dialog or not (or this cuold be a setting)
