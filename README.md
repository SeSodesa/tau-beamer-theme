# Tampere University Beamer Theme

This repository contains a LaTeX Beamer class theme for Tampere University
-themed presentation slides. There are two versions available, in two
different aspect ratios: `4:3` and `16:9`. These are located in the folders
[`4-3/`](./4-3/) and [`16-9/`](./16-9/), respectively.

## How-to

The files the user of these templates needs to modify are found in the folder
[`content/`](./content/). The file
[`content/presentation-metadata.tex`](./content/presentation-metadata.tex)
needs to be filled in between the braces `{..}` with author and presentation
information, in the format

    \def\myauthor{Santtu Söderholm}
    \def\mytitle{An Example Presentation}
    \def\mysubject{This is the subject}
    \def\mykeywords{latex, beamer, presentation}
    \def\myproducer{LaTeX with hyperref}
    \def\mycreator{pdflatex or lualatex}

The actual subject matter or presentation is added to the file
[`content/subject-matter.tex`](./content/subject-matter.tex), in standard
LaTeΧ syntax.

### Local use

Depending on the expected display size, one should choose either the
[`4:3`](./4-3/) or [`16:9`](./16-9/) version of the slide set for compilation.
Once the document metadata has been entered and your content is in place, the
presentation can be compiled by navigating to the folder that contains the
desired `main.tex` file with

    cd [folder]

where `[folder]` ∈ {`4-3`, `16-9`}, and entering the command

    $ [compiler] main.tex

Here `[compiler]` is either `pdflatex` or `lualatex`.

**Note:** remember that LaTeΧ compilers always look for files such as images
in relation to the used `main.tex` file or the so-called compilation context.
If you place your image file `image.pdf` into the [`content/`](./content)
folder, you must then include the image with
```latex
\includegraphics{../content/image.pdf}
```
or your chosen LaTeΧ compiler will not find it. To make image inclusion
easier, the folder [`content/images/`](./content/images/) can be used to store
images, in which case only
```latex
\includegraphics{image.pdf}
```
should be enough to include an image into a presentation.

### Using the project with Overleaf

Using the project with Overleaf is as simple as downloading the latest
Git-tagged version of the project as a ZIP file, uploading it to Overleaf as a
new project and choosing which main file one wants to use. The downloading of
the ZIP can be done on the Tags-page of this repository. Then on Overleaf, on
the page that contains your projects ([link](https://www.overleaf.com/project)),
press <kbd>New Project</kbd> → <kbd>Upload Project</kbd> → <kbd>Select a .zip
file</kbd>. Then on the generated project page, choose the desired aspect
ratio for the presentation, by selecting <kbd>Menu</kbd> → <kbd>Main
document</kbd> → <kbd>4-3/main.tex</kbd> or <kbd>16-9/main.tex</kbd>.

## Possible issues

The relative TAU logo paths defined in

    {4-3, 16-9}/beamerinnerthemetaupresentation.sty

might not work as intended on Windows, as at a certain point in time LaTeΧ
compilers still had issues with relative paths on the operating system. If
`pdflatex` or `lualatex` complains about the images not being found, a possible
workaround is to copy the images from `tau-logo` to the same folder with
`main.tex` and remove the prefixes `../tau-logo/` from the image paths.

## Future additions

A cross-platform build script that compiles the authored presentation in both
aspect ratios might be concocted later. For now, one has to manually compile
both versions as the instructions above indicate.
