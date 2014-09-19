Scribus cannot reliably print on every platform. Probably, it cannot even reliably print every document on most platforms.

The solution is to remove from scribus all the code relating to printing and replace it with a call to a PDF reader that gets the task to print the document (if possible with a command line argument that opens the document prints it and closes the pdf reader).

The scribus main target being he delivery of a PDF to a professional printer, removing, the printing specific code can only lead to a result that better matches what the user will get from the print shop.

- Find the command to directly print with the most common PDF readers
- Implement the code to detect the PDF readers
- Create a dialog with the options to be forwarded to the PDF reader
- Add the call to the PDF reader

Notes:

- If possible, the PDF reader should close after having printed the document.
- The user should be able to chose, if he wants to see the reader's print options.
