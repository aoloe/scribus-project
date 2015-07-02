# Printing through PDF

Scribus cannot reliably print on every platform. Probably, it cannot even reliably print every document on most platforms.

## On removing printing code from Scribus

The solution is to remove from Scribus all the code relating to printing and replace it with a call to a PDF reader that gets the task to print the document (if possible with a command line argument that opens the document prints it and closes the pdf reader).

The scribus main target being he delivery of a PDF to a professional printer, removing, the printing specific code will probably lead to a result that better matches what the user will get from the print shop.

## Optionally print through PDF

- find out the command to directly print with the most common PDF readers
- implement the code to detect the PDF readers
- add a choice in the preferences to use the internal print engine or print through pdf.
- for printing through pdf one has to choose one of the predefined PDF viewers and, eventually, set its path.
- when printing, scribus will
  - show the preflight verifier
  - show the pdf export dialog
  - create a temporary pdf
  - use the pdf viewer to print the pdf unatended (it should be possible with (adobe reader)!
  - delete the temporary pdf

Notes:

- If possible, the PDF reader should close after having printed the document or run without GUI.
- The user should be able to chose, if he wants to see the reader's print options.

# Related tickets

- [Does not print in landscape](http://bugs.scribus.net/view.php?id=5708)
- [Page becomes rotated 90 degrees clockwise when printing to postscript level 3](http://bugs.scribus.net/view.php?id=8254)
