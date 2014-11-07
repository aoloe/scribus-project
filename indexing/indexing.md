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

## john phase2 proposal, 2.7.2014 on the scribus mailing list

### ale says:

if i understand you correctly, you're suggesting that we should use the
tex/latex indexing system from scribus.

personally, i'd prefer a solution that -- while possibly using external
libraries -- does not pull in a huge package like latex...
but for the time being, going through latex could also be a way of
doing (in the future we could have a simpler internal index or an
external one through latex)

so, back to your proposal!

while i'm comfortable with latex, i must admit that i have never used
its indexing system... so, i might not understand some details...

let's try to split the proposal in three phases:

- marking the words that are to be indexed

- creating an idx file that can be fed into makeindex

- getting the result into scribus and format it as wished by the user.



a. marking the words to be indexed

as i understand it, if the user wants to add a word to the index -- the
"dog" appearing on page 32 -- he has to get scribus to change "dog"
into "\indexentry{dog}{32}"

we probably don't want to put the code as is in the text frame
(scribus being strongly wysiwyg...) but there are a few a ways to
achieve that!
as an example, we could have a "show fields" mode or could be showing
the codes in a separate window.

we certainly want scribus to automatically fill and update the page
number.

and we will have to store each index in the .sla.


b. creating an idx file

you seem to suggest that scribus should keep an idx file in sync with
the .sla.

i don't think that tex/latex is doing it, and i don't think that
scribus should, either.
the idx file should be created on the fly when the index is created or
updated.

it will probably be slow, but does it really matter?
for sure, if we use latex, we probably will not want to update the
index each time a page is refreshed!

concerning the creation of the idx itself, we will have to check a way
that makes sure that the page breaks are the same in the file fed into
makeindex and in the .sla... but this should not be way too complicated
to achieve.

c. getting the index into scribus

i have not looked into the output of makeindex but i expect a well
structured file that is fairly easy to parse.
i'm not too worried about that...

so, using manual edited marks and latex's makeindex for indexing looks
like something doable, but not trivial...

in my eyes the biggest issue being the way we can mark the entries.

 ### andreas says
 
 You can use makeindex without LaTeX. It just converts a raw index file to a
formatted index.
Using a style file it's possible to change the input and output formats.

I'd prefer to use its successor Xindy, though. Xindy supports international
languages (incl. Klingon)
and is more flexible.

The interesting part is how to get the raw index from Scribus. We could use
something like characters styles
or we could use escape chars like {thingy} and {dog|pets|animals} or
>thingy< and  >dog|pets|animals<.  
It might also be interesting to combine it with a word frequency counting
tool for identifying possible index terms and uses.

Reading the formatted index shouldn't be more difficult than importing text.

### ale again

on debian i don't think i can install makeindex without installing the
full latex.
i don't think that you can download it for windows or os x, either

but having had a look at the makeindex project page, it seems indeed
possible to use it as a standalone software... i guess that we would
have to add it to the scribus sources, then...

or expect the user to install the full latex package...

### craig

I'm sure we can write our own indexing code, but using the idea from latex.

## lászló, 30.7.2014 on the scribus mailing list

1. So please if anyone works on this project, use xindy for the external 
indexer, not makeindex. The only disadvantage of using xindy, that it 
seems to be a very niche product, it is usually not included in major 
linux distros, and there seems to be no windows or osx port yet. And 
their website (http://xindy.sourceforge.net) is actually misleading you 
if you want to download it, you should go here:
https://github.com/jschrod/xindy.ctan

A few more notes to the above document: phase2.pdf

2. I don't think it is a good idea to keep an .idx file open all the 
time. The index items have to be stored in the scribus document file 
itself anyway, so the .idx file can be generated on demand any time it 
becomes necessary. It means it can be a temporary file. That also means 
the developers can change the .idx file format if they want to switch to 
another indexer. Or even better, you could support more than one indexer 
program.

3. I also don't think the output of the indexer program should be as 
plain as it is suggested. The indexer program (xindy) can distinguish 
between different classes of index items (e.g. it is customary to use 
boldface for those page numbers where the topic is described in detail 
in a book). So the indexer can indicate which page numbers should be 
bold, which shouldn't. Since the output of xindy is extremely 
customisable, you could use e.g. xml structures to pass this info to 
scribus rather than just the plain strings. Or you could use some other 
markup.

## louis, 4.7.2014 on the scribus-dev mailing list

1. Create from scratch a *concordance file* (a list of the words you want
to have indexed in your document)
The indexing program compares the list against the document and tags the
words to produce the index. Notably, we can expand the program’s
capapilities to co-occurrences and not only single words. Example: "open
source software" and not only "open" or "source" or "software"... or others
like "tar sands"... etc.

2. Create the concordance file using the program’s capabilities to
initially propose a list of potential candidates to be indexed, using
various parameters (minimum length of word, number of occurrences, among
other things). This list must then be thoroughly checked by a human being.
Once that person is satisfied with the result, the file becomes a
concordance file that can be used as in 1). Not an easy task.

3. Manually tag the words to be indexed while creating the content. The
tagging can be done using a specific character style than can then we used
by the program to locate the words (or expressions) and create the index.
Another method can be used to manually tag words in a more complex way as
to produce multiple levels index (you’d need to make multiple tagging with
categories). But this can become a very long and demanding task.

4. Yet another way would be to read the document once layed-out and
"extract" the index that way but this seems to me a horrible way to
accomplish an index!

