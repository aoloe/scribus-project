We should provide a way for scribus to index the content or a way to interface with existing external tools.

# Existing tools

- Xindy (but is not simple to setup)

# Notes

## john jason, 20.6.2014, scribus mailing list

Having written and published numerous textbooks, and having been a
student where I needed to use an index, let me point out that a good
index is not a mere afterthought. Here are some things to consider:

1) Nesting. This means making subtopics under a larger topic. If you do
want nesting, then each subtopic needs to have its own individual
entry, with a reference to the larger topic, e.g., "see <larger
topic>."  

2) Main entries. Sometimes a term will appear in numerous places in the
book, but there is one place where the term is first defined for the
reader, or where the discussion is the most complete. I used to bold
the page number(s) for the main entry, but you could do italics or some
other scheme instead. And if you do this, tell the user what the bold,
etc. means with a comment at the start of the index.

3) Cross references. These are entries that say "See also."

4) With indexes, more is better. Nothing is more frustrating to the
reader than trying to find something in a book and the term is not
listed in the index. This means not only should you make an entry for
everything that you think a reader might need to look up, but you also
need to duplicate the entry under other terms that the user might use. 

5) I have never found an indexing tool that did not require at least
a little manual cleanup after the index was created. 

The last time I needed to create an index for a book laid out with
Scribus I was fortunate in that almost all the text was in one story. I
copied the text in that story and pasted it into LibreOffice Writer,
then manually went through the Writer document and forced page breaks
at exactly the same places as the pages broke in Scribus. Having done
this I could use the LibreOffice indexing function, which offered me
most of the above features. When I finished the index (which Writer
places at the end of the text) I made some manual edits, then copied
and pasted it into Scribus as a separate story at the end of the book.

If you want a rudimentary indexing tool for Scribus it might be possible
with a script. I can envision a script that copies a selected word in
a text frame, pastes it into another text frame at the top of the frame
(so you can see it easily, bearing in mind that the index text will
quickly overflow its frame). Then the script can add a tab at the end of
the pasted entry, insert the page number, then move to the beginning of
the entry and enter a line feed and move up to the new blank line so
you'll be ready for the next entry. When finished you can copy and paste
the entire index into a Writer document and sort it, plus make other
manual edits as desired. Writer can sort text by line, so it is not
necessary to use Calc or a Writer table for the sorting. 

If someone wants to embellish the script it could have an option to
bold or italicize the page number for main entries and an option to add
"see also" instead of a page number. Nesting might be more difficult to
script. 

Another script could sort a story on a line by line basis, eliminating
the need for a LibreOffice detour.

A script such as I envision above should not be difficult to implement,
but a true indexing tool would have the ability to change the page
numbers if the entry moves to a different page. In other words, you'd
have to be sure you used the script only after you were sure that there
were going to be no further edits to the book that might alter the
pagination..

It might also be possible to create a script that would generate an
index by searching for a specific character style. For example, I could
create a character style called Index_entry, then go through the book
and apply it to every term that I want in the index. When I have
finished I can use the script, which would search the entire work and
generate the index in a separate frame. If you want the capability of
having main entries you could create two character styles; one for
regular entries and one for main entries, so the script would bold or
italicize the page number when it finds a main entry character style.
An advantage of this approach is that if the page numbers change you
can just regenerate the index, although you'd lose any manual edits to
the index.

Yet another option might be to create a separate indexing program that
would work on a PDF file. I dont know if such programs currently exist,
but if so they are probably not free and open source. Note, however,
that if you index based on a PDF you'd have to be sure that you didn't
outline any fonts when exporting from Scribus. An advantage of a
separate PDF indexer is that it could be used on any PDF file, not just
PDFs created from Scribus. This would increase its popularity, and
concomitantly the number of potential developers.

I offer the above just as thoughts for further discussion. It would be
cool to have an indexing tool for Scribus, even if it is not as fully
capable as we might wish.

## john, 21.6.2014 on the scribus mailing list

1.  Most professional indexers use a
totally non-integrated approach. they receive a
final and paginated pdf from the publisher, print
it out, mark up the index items on the paper pages
and then enter the information using a separate
commercial program. The separate program 
generates a file that can be added to
the book by the publisher or author. 

2. The next level is semi-integration, or a tagged
index. TeX uses this technique. TeX is a
compilative system. The author works on a source
file with the suffix .tex. When a term is
encountered that needs indexing a tag is entered
at that spot. When the source file is compiled in
TeX a separate file of tagged indexed items with
the the suffix .idx is generated. This is run
through a separate program (usually makeindex)  
and a file resembling the final index is created
with the suffix .ind. A command is placed at the
end of the original tex file that imports the
index and typesets it. Typically I set up a
script that runs TeX, runs makeindex, and then
runs TeX again to import the index into the pdf
document.

3. The third version used in programs such as
InDesign and Libre office, where the indexing
function is fully integrated into the main
program. Here is how Libre Office help describbes
the process:

   Click in a word, or select the words in your
    document that you want to use as an index
    entry. Choose Insert - Indexes and Tables -
    Entry, and do one of the following:

    To change the text that appears in the index,
    type the text that you want in the Entry box.
    The text that you type here does not replace
    the selected text in the document. To add an
    index mark to similar words in your document,
    select Apply to all similar texts. To add the
    entries to a custom index, click the New
    User-defined Index icon, enter the name of
    the index, and then click OK.

There is a separate command that places the index
at the end of the document.

The third level is perhaps the most desirable but
is the hardest to implement. So I propose a
gradual approach. First, use my stand alone
program tyro.tcl This separate program actually
uses the makeindex program to generate the index,
but as you enter items the current version of
the index appears in a tk window. 

I should mention that makeindex is not the only
TeX game in town. There is another indexing
program in the TeX suite called Xindy. It is
little used. It adds additional capabilities not
found in makeindex, principally foreign alphabet
sorting. It uses style files for various
languages. I can be used with TeX (usually LaTeX),
the nroff family, and even sgm/html systems. It
is a very geeky approach to the indexing task.
But where non-romance languages are involved its
feature set is worth inspecting.
