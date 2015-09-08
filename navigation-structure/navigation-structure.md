# Improving the navigation structure

There are several issues in the navigation that should be improved:

- Too many sub menus.
- Too small difference between "Scribus preferences" and "Document settings".
- No way to discover the formatting options in the properties palette.
- Too many commands in the tree menus with no or little semantics: "edit", "extras", "windows".
- "Table" has its own menu entry (and it's the only item type having it!) but it's a very secondary content item type.

We probably first need a concept that can be applied to the navigation and then propose incremental changes to achieve the goal.

## Notes

### Ale

Personally, i still like the way staroffice did (iirc) and, sadly, libreoffice does not anymore: file/Scribus > settings && format > document.  
I just rediscovered that scribus does not have a "format" menu... and i wonder if there shouldn't be one.
as usual, i have the feeling that there should not be a "table" menu and split its entries between "insert > table" and "format > table".

The "format" menu could contain commands that make the properties palette visible and selects the matching tab; and the styles editor. (and probably some other entries that are currently placed in a very "technical" (and not semantic) way under "edit", "extras" and "windows".

