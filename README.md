# The rigidnotation LaTeX package
This package provides LaTeX macros to easily and concisely typeset vectors and matrices in a flexible way such as to follow the RIGID notation convention. The package enables the user to define custom commands that can then be used in any math-mode environment to efficiently and rigorously typeset the notational elements commonly used in robotics research (and many other fields) for position vectors, rotation matrices, pose matrices, etc.

## Documentation
This package is [available on CTAN](https://ctan.org/pkg/rigidnotation), and a PDF manual is accessible here.

## Local Installation
If you want to install the package manually on your local computer, you can follow the steps outlined below.
1. Run `kpsewhich -var-value TEXMFHOME` to get the path to your TeX package home.
Assuming that your TeX package home is `$TEXHOME`,
2. Run `mkdir -p $TEXHOME/tex/latex/rigidnotation/` to create a directory for this package.
3. Run `tex rigidnotation.ins` to generate the `rigidnotation.sty` macro file.
3. Run `cp rigidnotation.sty $TEXHOME/tex/latex/rigidnotation/` to install the package.
3. Run `pdflatex -interaction=nonstopmode rigidnotation.dtx` to build the documentation.
5. Run `texhash $TEXHOME` to update the LaTeX package tree.

## Requirements
This package depends on [mathtools](https://ctan.org/pkg/mathtools) and [xparse](https://ctan.org/pkg/xparse) packages, both of which are widely used.

## License
Copyright (C) 2024 Philippe Nadeau

This file may be distributed and/or modified under the
conditions of the LaTeX Project Public License, either version 1.3
of this license or (at your option) any later version.
The latest version of this license is in:

http://www.latex-project.org/lppl.txt

and version 1.3c or later is part of all distributions of LaTeX
version 2008-05-04 or later.