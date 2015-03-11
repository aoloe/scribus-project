# Text formatting and frames

having formatting attached to a (non empty) frame is the source of several bugs in scribus.

frames should not have text formatting. the formatting should only apply to the text inside of it.
the only case when a frame should have formatting, it's when it's empty.

if you change the formatting when you are not in edit mode, scribus should be behave as if you were in edit mode and had the whole text selected. the same applies to the values shown in the PP in that case.

the same applies to the end of paragraph mark: it should only have character formatting, if the paragraph is otherwise empty.

## nermander says: 

i think the major problem with the frame formatting is the strange use of both No style and Default style.

I think the Default styles (paragraph and character) should be removed.

A created frame ALWAYS have settings for the text (the ones set in Preferences), this means a frame ALWAYS have it's own default text settings. For example you can not create a frame that has no font selected!

Text in the frame that is set to No style inherits the settings from the frame.

There is no need for a default style, because the default style in any case needs to be assigned explicitly (text inserted into a frame as No style if not changed). And if it has to be assigned explicitly, it is not a default style.

## a.l.e says

i would go the other way round: no more settings in the text tool except being able to choose a style. the "Default style" being the default.
