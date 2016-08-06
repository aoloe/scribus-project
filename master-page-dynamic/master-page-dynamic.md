# Dynamic master pages

Currently, in Scribus master pages are a mostly static background (up to the page numbers and a few other dynamic fields).

Other packages, allow to edit on the page items that come from the master page. But they do that in a rather cumbersome way, both on the code and on the workflow side.

Scribus should increase the usefulness of the master pages by making it clear how to define editable content attached to a master page.

The problems with the way the master pages work in Scribus, already start from the fact that it's hard to understand the diffrence between the normal page editing and the master page editing. And it's not trivial to find the way to get out of it.

- a better integration with the scrapbook (creating a link between the master page and some of the scrapbook items?)
- frame styles.
- better visibility for guides, scrapbook, scrapbook linked items
- more variables fields

## Automatically add scrapbook and pattern items

- When a page with a specific master page is created, automatically add one ore more scrapbook entries.
- The template items could be on a "master page" layer that does not get printed.

Ideas:

- We could have layers that are only shown when in master page modus.

does anybody want to do a UX / UI proposal for this feature? 

## related projects:

- real double sided master pages
