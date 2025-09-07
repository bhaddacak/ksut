# Grammatical Suttas of Kaccāyana

This is the first volume of my translation project of Pāli grammatical suttas. It is a clean translation of Kaccāyana's Pāli grammar. This work focuses mainly on the formulas and descriptions. Examples are given mostly, some are left out, some are added. The discussion part of the suttas is mostly neglected.

## How to build the book

All you need is TeX Live and the skill of using it. To install the program, consult the [quick installation guide](https://tug.org/texlive/quickinstall.html). The full installation is huge (7GB+). To minimize it, documentation and source files can be excluded, as well as languages other than English. Many packages are not really used such as additional fonts, but it is too nitpicky to microselect them. If space is not a problem, it is better to install most of them.

At least, these fonts are used in the book: TeX Gyre Schola, TeX Gyre Heros, and DejaVu Sans Mono. Make sure they are installed properly. Or you can change these to your favorite ones by changing the `fontspec` commands in `preamble.tex`.

Typesetting in LaTeX is definitely difficult, even by competent programmers. You have to learn new language syntax and several conventions. I suppose that you have already passed this requirement.

To build the whole book, follow these steps:
1. Comment out `includeonly` in `preamble.tex` (see toward the end), if it has not yet been done.
2. Open a terminal console at the book's folder and type these (normally you need to process more than once, and sometimes twice is not enough):
    ```
    $ lualatex ksut
    $ biber ksut
    $ lualatex ksut
    (or maybe another one for sure)
    $ lualatex ksut
    ```
3. If `ksut.pdf` is produced, the build is successful. Otherwise, you have to fix errors, possibly by installing missing packages in case you have an insufficient installation. If any syntax errors occur, you have to fix those too.
4. If only some chapters are needed, edit and uncomment `includeonly` in `preamble.tex`, and rebuild it again. You can see the sequence of files in `ksut-base.tex`.

