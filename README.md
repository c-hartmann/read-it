# ReMove-Ext(ension)

KDE Dolphin Servie Menu, that removes the extension from one or more filenames and renames the files accordingly. Takes no action on filenames starting with a dot.

## Dependency

Read-It utilizes (and checks) tesseract(1). Please use your package management system to install.

The required package is 'tesseract-ocr' in most common distributions.

bash


## Changelog

Read-It is restricted to reading text from images only. Currently no plans to read from PDF as well.

Read-It uses a very rough method to determine the default language to use with tesseract:

    _tesseract_lang_code="$(tesseract --list-langs | grep ${LANG:0:2})"

(This works fine for a variety of languages such as englisch, italian, german, but not for spanish.)

It also roughly overwrites existing extraction files of the same name.

## Ideas

Create one PDF with multiple pages from a list of image files.

## Changelog

* 2023-10-03: 0.2.1: removed default TryExec=, replaced by own check, being more verbose on not-install error and success on creation
* 2023-10-03: 0.3.0: added option to create a seachable "sandwich" PDF

