# Text formatting and frames

having formatting attached to a (non empty) frame is the source of several bugs in scribus.

frames should not have text formatting. the formatting should only apply to the text inside of it.
the only case when a frame should have formatting, it's when it's empty.

if you change the formatting when you are not in edit mode, scribus should be behave as if you were in edit mode and had the whole text selected. the same applies to the values shown in the PP in that case.

the same applies to the end of paragraph mark: it should only have character formatting, if the paragraph is otherwise empty.

