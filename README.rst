Tampere University Beamer Theme
===============================

This repository contains a LaTeX Beamer class theme for Tampere University -themed presentation slides.
There are two versions available, in two different aspect ratios: ``4:3`` and ``16:9``.
These are located in the folders ``4-3`` and ``16-9``, respectively.

How-to
------

Depending on the expected display size, one should choose either
the ``4:3`` or ``16:9`` version of the slide set.
The actual contents of the slides should be written in
either ``4-3/main.tex`` or ``16-9/main.tex``,
depending on which version one wants to use.

Author and document information should be set by modifying
the values inside the braces ``{..}``, defined at the beginning of ``main.tex``::

  % Author and document information.
  % Change these to suit your needs.
  \def\myauthor{Santtu Söderholm}
  \def\mytitle{An Example Presentation}
  \def\mysubject{This is the subject}
  \def\mykeywords{latex, beamer, presentation}
  \def\myproducer{LaTeX with hyperref}
  \def\mycreator{pdflatex or lualatex}

This data will be used to generate the front page and document metadata.
Therefore these lines should not be removed.

Once the document metadata has been entered and your content is in place,
the presentation can be compiled by navigating to the folder that contains your ``main.tex`` file
and typing

  $ <compiler> main.tex

Here ``<compiler>`` is either ``pdflatex`` or ``lualatex``.

Possible issues
---------------

The relative TAU logo paths defined in ::

 {4-3,16-9}/beamerinnerthemetaupresentation.sty

might not work as intended on Windows.
If ``pdflatex`` or ``lualatex`` complains about the images not being found,
a possible workaround is to copy the images from ``tau-logo``
to the same folder with ``main.tex`` and remove the prefixes ``../tau-logo/``
from the image paths.
