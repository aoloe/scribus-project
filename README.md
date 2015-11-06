# Projects for Scribus

## The plan

List of projects for scribus:

- create a php interface to browse this list ("static" from the github repository; with comments from an external service)
- should each project be in its own directory? (images, properties?)
- how to sort the the projects? how to add properties (json? yaml?)
- also show all the bugs marked with the "easyhack" tag

## Creating a project

- Each project has its own directory in the `content/` directory.
- The name of the directory should identify the content of the project.
- If possible, the name of the directory should start with a word that projects that cover a similar topic are listed one after the other (i.e. `master-page-double-sided/` and `master-page-dynamic`).
- Put a markdown file into the directory, with the same name as the directory (i.e. `master-apge-double-sided.md`).
- If possible start the file with a YAML description of the preject (see the section below)
- If no YAML description is given or no title is defined in there, if the first markdown line is a title, it is used athe title of the project. If no "description" is defined, the second line, is used as the "description" field.

## Creating the YAML description

## The Markdown syntax

A pretty standard markdown syntax is in use, with a few restrictions and a few extensions:

- A comment is used at the beginning of the file to define the YAML description of the project.
- Please use the `#` character for the titles.

## Todo

- rename the projects as "topic-name-of-project" where topic is one of
  - text
  - script
  - image
  - ...
  or is it overingeneering?
- comments: is there a way to add the comments from my site by js to the tickets? if not, send me an email with the comment and i'll click on the link to accept it and add it in my name to the ticket's comments

## Commenting

Use `hashover`, a php based commenting system.

## Tasks

- finish `php-deploy-git`
- create a site on impagina with aoloe's hand made cms or with picocms showing a list of projects and linking to the them
- complete the comments part to know which one are / have easy hacks
- add search functions
