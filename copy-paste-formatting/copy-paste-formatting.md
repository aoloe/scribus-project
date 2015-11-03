# Copy paste and formatting

- see <http://bugs.scribus.net/view.php?id=11574>

here are a few "simple" edge cases:

- if noting is said, the formatting surrounding the cursor at the target place is applied to the pasted text.
- surrounding needs to be defined (character before, character after, both of them; what happens when one of both do not exist?)
- copy pasting a single word should not apply a paragraph style (except if it is a full paragraph).
- copy pasting a full paragraph in the middle of more text should probably by default use the original paragraph style.
- the local formatting and character styles that are applied to a selection bigger than what is copy-pasted should probably not be kept in the pasted text.
- the local formatting and character styles that are applied to a subset of the selection should by default be reproduced in the pasted text.
- we must define what happens if the subset starts or ends with the selection.
- the condition before might be different than the case where the subset start inside of the selection and ends outside of it (not at its boundaries)
- the local formatting and character that are applied to the exact same selection as the one copied might or not by default be copied (a decision must be taken)
- we should not over engineer the "keeping" of the paragraph formatting, since it's easy to reaply the paragraph style.
- we might want a new command "edit > paste without formatting"
- you need to define which is information is to be collected at the time you copy the text and which one at paste time.
