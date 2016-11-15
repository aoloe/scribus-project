# Imposition

Imposition inside of Scribus is one of the most requested features.

## Inside of Scribus

Cezary has implemented some imposition features in his Scribus-ECE

## Outside of Scribus

Still, imposition is probably better done outside of Scribus.

There are several tools that allow to do imposition. But it's never clear how well they understand / keep all the PDF features (CMS, fonts, ...) that are essential in a professional workflow.

- Document the existing command line tool
- Document the existing GUI tools
- Eventually create a dumbled down tool that warranties the PDF quality but only supports a few workflows (spreads, booklets, multiple double page copies on one page)
  - Rust and libui? (<https://github.com/pcwalton/libui-rs>, <http://www.chriskrycho.com/2016/using-rust-for-scripting.html>)
  - Using Podofo / Poppler ?
  - Using gs / command line tools?
