The Komi-Permyak morphology and tools
==========================================

[![GitHub issues](https://img.shields.io/github/issues-raw/giellalt/lang-koi)](https://github.com/giellalt/lang-koi/issues)
[![Build Status](https://divvun-tc.thetc.se/api/github/v1/repository/giellalt/lang-koi/main/badge.svg)](https://github.com/giellalt/lang-koi/actions)
[![License](https://img.shields.io/github/license/giellalt/lang-koi)](https://github.com/giellalt/lang-koi/blob/main/LICENSE)
[![Desktop speller download](https://img.shields.io/badge/download%40latest-desktop--bhfst-brightgreen)](https://pahkat.uit.no/main/download/speller-koi?platform=desktop&channel=nightly)
[![Mobile speller download](https://img.shields.io/badge/download%40latest-mobile--bhfst-brightgreen)](https://pahkat.uit.no/main/download/speller-koi?platform=mbile&channel=nightly)

This repository contains finite state source files for the Komi-Permyak language,
for building morphological analysers, proofing tools
and dictionaries. The data and implementation are licenced under __LICENSE__
licence, also detailed in the
[LICENSE](https://github.com/giellalt/lang-koi/blob/main/LICENSE). The
authors named in the AUTHORS file are available to grant other licencing
choices.

Install proofing tools and [keyboards](https://github.com/giellalt/keyboard-koi)
for the Komi-Permyak language by using the [Divvun Installer](http://divvun.no)
(some languages are only available via the nightly channel).

Download and test speller files
-------------------------------

The speller files downloadable at the top of this page (the `*.bhfst` files) can
be used with [divvunspell](https://github.com/divvun/divvunspell), to test their
performance. These files are the exact same ones as installed on users' computers
and mobile phones. Desktop and mobile speller files differ from each other in the
error model and should be tested separately — thus also two different downloads.

Documentation
-------------

Documentation can be found at:

- [Language specific documentation](https://giellalt.github.io/lang-koi/)
- [General documentation](https://giellalt.github.io/)

Core dependencies
-----------------

In order to compile and use Komi-Permyak language morphology and
dictionaries, you need:

- an FST compiler: [HFST](https://github.com/hfst/hfst), [Foma](https://github.com/mhulden/foma) or [Xerox Xfst](https://web.stanford.edu/~laurik/fsmbook/home.html)
- [VislCG3](https://visl.sdu.dk/svn/visl/tools/vislcg3/trunk) Constraint Grammar tools

To install VislCG3 and HFST, just copy/paste this into your Terminal on **Mac OS X**:

```
curl https://apertium.projectjj.com/osx/install-nightly.sh | sudo bash
```

or terminal on **Ubuntu, Debian or Windows Subsystem for Linux**:

```
wget https://apertium.projectjj.com/apt/install-nightly.sh -O - | sudo bash
sudo apt-get install cg3 hfst
```

or terminal on **RedHat, Fedora, CentOS or Windows Subsystem for Linux**:

```
wget https://apertium.projectjj.com/rpm/install-nightly.sh -O - | sudo bash
sudo dnf install cg3 hfst
```

Alternatively, the Apertium wiki has good instructions on how to [install the dependencies for Mac
OS X](https://wiki.apertium.org/wiki/Apertium_on_Mac_OS_X) and how to [install
the dependencies on
linux](https://wiki.apertium.org/wiki/Installation_of_grammar_libraries)

Further details and dependencies are described on the GiellaLT [Getting Started](https://giellalt.uit.no/infra/GettingStarted.html) pages.

Downloading
-----------

Using Git:
```
git clone https://github.com/giellalt/lang-koi
```

Using Subversion:
```
svn checkout https://github.com/giellalt/lang-koi.git/trunk lang-koi
```

Building and installation
-------------------------

[INSTALL](https://github.com/giellalt/lang-koi/blob/main/INSTALL)
describes the GNU build system in detail, but for most users it is the usual:

```sh
./autogen.sh # This will automatically clone or check out other GiellaLT dependencies
./configure
make
(as root) make install
```

Citing
------

<!-- Add language specific citation stuff here and to the CITATION.cff -->

> Jack Rueter, Niko Partanen, and Larisa Ponomareva. 2020.
  On the questions in developing computational infrastructure
  for Komi-Permyak. In Proceedings of the Sixth International
  Workshop on Computational Linguistics of Uralic Languages,
  pages 15–25, Wien, Austria. Association for Computational Linguistics.

```bibtex
@inproceedings{rueter-etal-2020-questions,
    title = "On the questions in developing computational infrastructure for {K}omi-Permyak",
    author = "Rueter, Jack  and
      Partanen, Niko  and
      Ponomareva, Larisa",
    booktitle = "Proceedings of the Sixth International Workshop on Computational Linguistics of {U}ralic Languages",
    month = jan,
    year = "2020",
    address = "Wien, Austria",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2020.iwclul-1.3",
    doi = "10.18653/v1/2020.iwclul-1.3",
    pages = "15--25",
}

```

If you use language data from more than one GiellaLT language, consider citing
[our LREC 2022 article on whole
infra](https://aclanthology.org/2022.lrec-1.125/):

> Linda Wiechetek, Katri Hiovain-Asikainen, Inga Lill Sigga Mikkelsen,
  Sjur Moshagen, Flammie Pirinen, Trond Trosterud, and Børre Gaup. 2022.
  *Unmasking the Myth of Effortless Big Data - Making an Open Source
  Multi-lingual Infrastructure and Building Language Resources from Scratch*.
  In Proceedings of the Thirteenth Language Resources and Evaluation Conference,
  pages 1167–1177, Marseille, France. European Language Resources Association.

If you use bibtex, following is as it is on ACL anthology:

```bibtex
@inproceedings{wiechetek-etal-2022-unmasking,
    title = "Unmasking the Myth of Effortless Big Data - Making an Open Source
    Multi-lingual Infrastructure and Building Language Resources from Scratch",
    author = "Wiechetek, Linda  and
      Hiovain-Asikainen, Katri  and
      Mikkelsen, Inga Lill Sigga  and
      Moshagen, Sjur  and
      Pirinen, Flammie  and
      Trosterud, Trond  and
      Gaup, B{\o}rre",
    booktitle = "Proceedings of the Thirteenth Language Resources and Evaluation
    Conference",
    month = jun,
    year = "2022",
    address = "Marseille, France",
    publisher = "European Language Resources Association",
    url = "https://aclanthology.org/2022.lrec-1.125",
    pages = "1167--1177"
}
```
