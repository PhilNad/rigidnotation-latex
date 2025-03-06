# The rigidnotation LaTeX package
This package provides LaTeX macros to easily and concisely typeset vectors and matrices in a flexible way such as to follow the RIGID notation convention. The package enables the user to define custom commands that can then be used in any math-mode environment to efficiently and rigorously typeset the notational elements commonly used in robotics research (and many other fields) for position vectors, rotation matrices, pose matrices, etc.

## Documentation
This package is [available on CTAN](https://ctan.org/pkg/rigidnotation), and a PDF manual is accessible in this repository.

## Installation
There are (at least) three ways you can use to install this package:
1. With MikTeX (easiest), if your system is using it
2. Integrate the package with TeX Live, if your system is using it
3. Simply copy `rigidnotation.sty` in your LaTeX project

To know if your system is relying on MikTeX or TeX Live for package installation, run
```bash
tex -version | head -n 1
```
and the output should be either something like
```
TeX 3.141592653 (TeX Live 2022/dev/Debian)
```
or something like
```
MiKTeX-TeX 4.5 (MiKTeX 23.10)
```

### As a standalone file
The fastest way to get going is to download the `rigidnotation.sty` in the root of your LaTeX project. This will not install the package onto your system but will make it available for a specific project.
```bash
wget https://raw.githubusercontent.com/PhilNad/rigidnotation-latex/refs/heads/main/rigidnotation.sty
```

### With MikTeX
This package is distributed [by the MikTeX repository](https://miktex.org/packages/rigidnotation) and can be easily installed from a working MikTeX distribution:
```bash
> miktex packages install rigidnotation
Installing package rigidnotation...
> miktex packages info rigidnotation
id: rigidnotation
title: Typeset vectors and matrices following the RIGID notation
version: 1.0.0
isInstalled: true
```

### With TeX Live
If you want to install the package manually on your local computer, you can follow the steps outlined below.
1. Run `` TEXMFHOME=`kpsewhich -var-value TEXMFHOME` `` to get the path to your TeX package home.
2. Use `echo $TEXMFHOME` to verify that the package home is defined.
3. Run `mkdir -p $TEXHOME/tex/latex/rigidnotation/` to create a directory for this package.
4. Clone this repository on your machine and `cd` into it.
5. Run `tex rigidnotation.ins` to generate the `rigidnotation.sty` macro file.
3. Run `cp rigidnotation.sty $TEXHOME/tex/latex/rigidnotation/` to install the package.
3. Run `pdflatex -interaction=nonstopmode rigidnotation.dtx` to build the documentation.
5. Run `texhash $TEXHOME` to update the LaTeX package tree.

## Requirements
This package depends on [mathtools](https://ctan.org/pkg/mathtools) and [xparse](https://ctan.org/pkg/xparse) packages, both of which are widely used.

## License
Copyright (C) 2024 Philippe Nadeau

This file may be distributed and/or modified under the
conditions of the LaTeX Project Public License, either version 1.3c
of this license or (at your option) any later version.
The latest version of this license is in:

http://www.latex-project.org/lppl.txt

and version 1.3c or later is part of all distributions of LaTeX
version 2008-05-04 or later.
