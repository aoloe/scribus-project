# Fix the behavior of the first line offset

Currently the first line offset is a frame property set that one can only set on a per frame base from the properties palette.

There are multiple issues:

- The first thing is that nobody knows that it's there.
- The second is that the default value is probably wrong (it should be "line height"... or even better match the current line height setting).
- The third is that it might be better to have (also) automatically change when changing / setting paragraph line height
- The forth being that there is no way to set it to for multiple frames
- The fifth is that there is no way to change the default value.
- Sixth: very likely, it looks like it's implemented as a frame property... In theory it's the right thing to do, but in practice it might be much more intuitive (and easy to implement) to have it as a paragraph setting...  
  In most cases it will have the same effect. In some cases it will be the wrong value or it will be a bit more difficult to set the value. But in the normal case it would just do the right thing and it will be much easier to understand / set.
