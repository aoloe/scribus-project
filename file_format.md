Create an alternative to .sla as a the Scribus file format

Currently, the .sla file format has been identified as a blocker for a few new features. We should design a new file format that avoids those problems and add it as a parallel implementention to the current one.

Once everything in place, the team can decided if it wants to switch to the proposed file format.


- what about using sqlite instead of a pure xml format?
  - performance?
  - recovering from corrupted files? can a sqlite db get corrupted?
  - or a key/value storage engine like google leveldb?
- what about using html/css for the text frames content?
