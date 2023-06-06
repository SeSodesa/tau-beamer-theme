# Presentation contents

The files and folders in this directory are to be filled in by the user of
this presentation template. The intended contents of the files are as follows:

* [`presentation-metadata.tex`](./presentation-metadata.tex):
  Contains author and document information, in addition to document-wide
  settings, in the form of `\def\key{value}`.

* [`preamble.tex`](./preamble.tex):
  Own packages can be entered here with `\usepackage{package-name}`. Any LaTeΧ
  command definitions should also be entered here, unless the definitions need
  to be added or changed in the middle of the presentation.

* [`subject-matter.tex`](./subject-matter.tex):
  This is where one writes the actual contents of the presentation, in
  standard LaTeΧ syntax. This file is included by all of the `main.tex` files
  in this template, so the content only has to be written once, and it will
  still show up no matter which aspect ratio you choose to compile with.

* [`sources.bib`](./sources.bib):
  This is the database of citations. See BibLaTeΧ documentation for
  information on citation syntax.

* [`images/`](./images):
  This is where one should place any image files, if one does not wish to use
  a full relative path when including images via the `\includegraphics`
  command. In other words, if the image files are stored in this folder, one
  only has to write `\includegraphics{image.pdf}` instead of
  `\includegraphics{../path/to/image.pdf}` in relation to the files
  `main.tex`.
