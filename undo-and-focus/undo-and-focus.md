#undo and focus

how should scribus behave when undoing?

four years ago i created a ticket for it

http://bugs.scribus.net/view.php?id=8745

and two years ago chelen uploaded a patch.

now, craig brought up some cases where the patch is not working as the
user would expect (... personally, i don't really understand what's the
matter is in those cases, but i assume that they are legit) and the
ticket has been closed as "won't fix".



personally, i had a bad feeling about it and just did a short test.
there is indeed at least one case where, scribus does
not behave as i would expect:

- create a two pages document
- if you're monitor is somehow like mine, you will see only one page on
  it.
- scroll down to the second page.
- add a text frame.
- scroll up to the first page
- undo.

the frame on the second page is removed without the user having a
chance to see what happened.

in my eyes a dangerous behavior.

and there are other cases, where i think scribus is not helping me
enough, understanding what the undo is doing.

looking for how others are doing it. i've tried to create two pages in
a libreoffice write document, inserted a frame in the second one,
scrolled up and undo.
after deleting the frame, libreoffice "jumps" down to the second page
and the cursor is placed where the frame was anchored.
much better.

now, scribus does not have anchoring points so our case is a bit more
complicated.

but it should be possible to achieve a better behavior than the current
one!



so the question to you: does anybody want to spend some time on this
and write down a proposal defining how scribus should behave?

you don't need to be able to code for it, but you need some experience
with DTP tools and good UI/UX skills :-)

## Notes

- Sveinn suggests: I'm wondering if the problem (if there is a problem) is maybe more general; should the view go automatically to cursor location in case of any kind of edit? 
- Greg says: It might be good to first consider what actions are undoable. Some may be relatively invisible, and others may be pageless -- changes to a style for example.
