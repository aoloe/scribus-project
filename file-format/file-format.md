Create an alternative to .sla as a the Scribus file format

Currently, the .sla file format has been identified as a blocker for a few new features. We should design a new file format that avoids those problems and add it as a parallel implementention to the current one.

Once everything in place, the team can decided if it wants to switch to the proposed file format.


- what about using sqlite instead of a pure xml format?
  - performance?
  - recovering from corrupted files? can a sqlite db get corrupted?
  - or a key/value storage engine like google leveldb?
- what about using html/css for the text frames content?

# Ideas

- The paragraph styles should not have character formatting in them, but just reference a character style (the GUI might automatically link the default character style and give the option to create a character style with the same name as the paragraph style)
- We might simple use HTML5 and css in a zip file, with scribus proprietary extension for what is not supported. Scribus should be able to read and zip an unzipped directory.

# Notes:

- [In the bug tracker](http://bugs.scribus.net/view.php?id=12656) grol suggests to use QML as a description language for Scribus documents.
