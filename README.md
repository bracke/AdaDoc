# AdaDoc
AdaDoc consists of a commandline program 'AdaDoc' by Julien Burdy &
Vincent Decorges and a frontend (this).

To read more about the backend (AdaDoc) go to:
http://adadoc.sourceforge.net/

NOTE: This is a RISC OS app and will not run on other platforms.

# Frontend use

1. Double click on the !AdaDoc icon - this will place an icon on the
   iconbar.
2. SELECT clicking on the iconbar icon will open a setup window.
3. Fill in the information needed. Use the interactive help to
   get information about what to fill in where.
4. Set the work directory to the source directory ('*dir <source
   directory>')
5. SELECT click on 'Run'

This will start the AdaDoc command line program and open a window
showing the status.

AdaDoc generates a file from an Ada 95 specification package
for documentation purpose.

The format is either HTML,XML,LaTeX or StrongHelp. Multiple formats can
be selected and created in one go.

AdaDoc puts the files into subdirectories (html,xml,tex,sh) according to
their type.

For HTML output AdaDoc will accept a stylesheet. An example stylesheet
(style) is supplied in the !Adadoc directory.

Command line use
================
### Use 
adadoc option File_Name 

### Options

  Arg 		  | Description
  ----		  |------
  -x          | don't delete XML file after generating output.
  -c          | don't try to extract comments from the specification.
  -Hstylsheet | generate HTML file. stylsheet is optional
  -L          | generate LaTeX file.
  -S          | generate StrongHelp file.

### Example 
adadoc -x -Hfid spec.ads spec2.ads ..