# Testing

Currently Scribus has little or no automatic testing.

Since we now can run Scribus from the terminal, it's now easier to get Scribus to run a test suite.

We should:

- Define what kind of testing is useful.
- Create a repository with SLAs that show edge cases.
- Create PDFs that we "manually" check for validity.
- Create a script that launches Scribus and creates PDFs that are converted to an image and diffed with the reference PDF (also converted to images)
- Report if there are any changes.

Options: 
* Regressions testing: https://github.com/scribusproject/scribus/issues/18 using SikuliX. It has Jython support which we could use to automate testing as well. 
