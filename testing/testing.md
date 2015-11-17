# Testing

Currently Scribus has little or no automatic testing.

Since we now can run Scribus from the terminal, it's now easier to get Scribus to run a test suite.

We should:
- Testing the PDF export
  - Define what kind of testing is useful.
  - Create a repository with SLAs that show edge cases.
  - Create PDFs that we "manually" check for validity.
  - Create a script that launches Scribus and creates PDFs that are converted to an image and diffed with the reference PDF (also converted to images)
  - Report if there are any changes.
- Testing the Canvas rendering (through PNG export... not sure if the PNG export matches the canvas rendering, thgough)
- Testing the user interface:
  - Regressions testing: https://github.com/scribusproject/scribus/issues/18 using SikuliX. It has Jython support which we could use to automate testing as well. 

## Notes

- mapreri could help integrate them in the packaging (so they get run in ci.debian.net / http://autopkgtest.ubuntu.com/ ) once they are available.
