.. image:: https://img.shields.io/badge/dmtn--288-lsst.io-brightgreen.svg
   :target: https://dmtn-288.lsst.io
.. image:: https://github.com/lsst-dm/dmtn-288/workflows/CI/badge.svg
   :target: https://github.com/lsst-dm/dmtn-288/actions/

##########################################################################
Converting Rubin Observatory's Data Butler to a client/server architecture
##########################################################################

DMTN-288
========

The Rubin Observatory’s Data Butler provides a way for science users to retrieve data without knowing where or how it is stored. In order to support the 10,000 science users in a hybrid cloud environment, we have to modify the Data Butler to use a client/server architecture such that we can share authentication and authorization controls with the Rubin Science Platform and more easily support standard tooling for scaling up backend services. In this talk we describe the changes that had to be made to support this and some of the difficulties that were encountered.

Links
=====

- Live drafts: https://dmtn-288.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-288

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-288

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
