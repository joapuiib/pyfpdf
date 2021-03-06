# Development #

[TOC]

## Introduction ##

This page has summary information about developing the PyPDF library.

This project, fpdf2 is a [FORK] of the PyFPDF project, which can be found
[here](https://github.com/reingart/pyfpdf). It is made in order to keep the
library updated and fulfill the goals of its
[Roadmap](https://github.com/reingart/pyfpdf/wiki/Roadmap) and a general overhaul of
the codebase because there was technical debt keeping features from being
created and bugs from being eradicated.

More on pyfpdf:

> This project started as Python fork of the [FPDF](http://fpdf.org/) PHP library. 
> Later, code for native reading TTF fonts was added. FPDF has not been updated since
> 2011. See also the [TCPDF](http://www.tcpdf.org/) library.
> 
> Until 2015 the code was developed at [Google Code](https://code.google.com/p/pyfpdf/).
> Now the main repository is at [Github](https://github.com/reingart/pyfpdf).
> 
> You can also view the
> [old repository](https://github.com/reingart/pyfpdf_googlecode),
> [old issues](https://github.com/reingart/pyfpdf_googlecode/issues), and 
> [old wiki](https://github.com/reingart/pyfpdf_googlecode/tree/wiki).
> 
> After being committed to the master branch, code documentation is automatically uploaded to 
> the [Read the Docs](http://pyfpdf.rtfd.org/) site.

## Repository structure ##

  * `[attic]` - folder with old code and useful, but unsupported things
  * `[docs]` - viewable documenation folder
  * `[mkdocs_docs]` - viewable documenation source folder
  * `[fpdf]` - library source
  * `[scripts]` - manipulate this repository
  * `[test]` - tests
  * `[tutorial]` - tutorials (see also [Tutorial](Tutorial.md))
  * `README.md`, `PyPIReadme.rst` - Github and PyPI Readme's.
  * `LICENSE` - license information
  * `setup.cfg`, `setup.py`, `MANIFEST.in` - setup configuration
  * `mkdocs.yml` - config for [MkDocs](https://www.mkdocs.org/)
  * `tox.ini` - config for [Tox](https://tox.readthedocs.io/en/latest/)

## Testing ##

Testing is done with [Tox](https://tox.readthedocs.io/en/latest/), and is
self-documented in the `tox.ini` file in the repository. To run tests, cd into
the cloned repository and run `tox`.

If you do not want to run tests for all versions of python, run `tox -e py27`
(or your version of python). To install all versions of python that are
supported on Ubuntu, see the instructions on the Github Repository home page
of this project.

Be sure to see the example tests in the `test` folder & `test\utilities.py`
and explore that folder in general.

## Documentation ##

To build docs, cd into repository and `tox -e docs`.

This Standalone documentation is in the `mkdocs_docs` subfolder in 
[Markdown](https://daringfireball.net/projects/markdown/) format. Building
instructions are contained in the configuration file `mkdocs.yml` and also in
the docs script in the `tox.ini` file.

Additional documentation is generated from inline comments, and is available
in the project [home page](https://alexanderankin.github.io/pyfpdf/).

## See also ##
[Project Home](index.md), [Frequently asked questions](FAQ.md), 
[Unicode](Unicode.md).
