# Create a notification palette

From the code we should be able to add notifications to a list.

They are non blocking, the user sees them and can act upon.

Notifications can have:

- a message
- a button applying a specific change
- a button launching a dialog
- a "Hide" button
- a "Delete" button
- a decay time, after which they are hidden
- an importance (making sure that important messages are shown on top of less important ones

The notification would be implemented as a plugin.

It can be implemented:
- as a palette
- as stackable notification bubbles shown on top of the Scribus window.

There could be preferences for:
- how long the list can become (LIFO)
- how long items are kept in the list
- manually clear the list

## Notes

- http://qt-project.org/doc/qt-4.7/qsystemtrayicon.html
- http://stackoverflow.com/questions/9818014/show-ubuntu-linux-notifications-with-qt
- http://stackoverflow.com/questions/11450528/qt-notifications-without-tray-icon-possible
