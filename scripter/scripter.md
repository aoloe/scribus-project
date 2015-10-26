# The Scripter

For many years, a new scripter has been in the workings.

The characteristics of the new scripter are:

- almost completely implemented in Python
- easier to add new API commands and bind them to the Scribus code
- scripts can be attached to the navigation
- scripts can be attached to keyboard shortcuts
- script can create PyQt dialogs
- a new saner API
- a better model for documenting the API (readthedocs)

While in the past it used to be incomplete but somehow work, due to the move to Qt5 it is currently simply broken:

The status at the time of writing is:

- Needs Python 3
- Mostly ported to Python 3 (no error know, but since it does not run, the port cannot be tested)
- Compiles correctly
- Does not load because of an error in the way Signal and Slots cross the boundaries between C++/Qt5 and Python/PyQt5

The current version can be found here: <https://github.com/aoloe/scribus-plugin-scripter>  
The README.md file contains the instruction for building the new scripter.
