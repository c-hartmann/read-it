# Read-It

Convert scanned documents with a single right click in KDE Dolphin to plain text or a (searchable) "sandwich" PDF.

## tl;dr;

Creates SCAN-0001.png.txt (or SCAN-0001.png.pdf) from SCAN-0001.png

## Dependency

Read-It utilizes (and checks) tesseract(1). Pleas use your package management system to install.
(the required package might be named 'tesseract-ocr')

If tesseract is not installed, Read-It will either not show up at all or show an error message.

## Limitations

Read-It is restricted to reading text from images only. Currently no plans to read from PDF as well.

Read-It uses a very rough method to determine the default language to use with tesseract:

    _tesseract_lang_code="$(tesseract --list-langs | grep ${LANG:0:2})"

(This works fine for a variety of languages such as englisch, italian, german, but not for spanish.)

It also roughly overwrites existing extraction files of the same name.

## Ideas

Create one PDF with multiple pages from a list of image files.
