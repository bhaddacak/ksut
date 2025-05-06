# Grammatical Suttas of Kaccāyana

(to be added)

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

## Notes on licensing

Form version 3.0 onward, the *GNU Free Documentation License* is applied to the work. This means the LaTeX source files will be always publicly available and amendable. Now the work belongs to the public. To help editing the book in the main branch, please use the *pull request* mechanism.

Apart from the strict license used, I also allow derivative works, possibly translations and partial compositions, to be relicensed to *Creative Commons Attribution-ShareAlike 4.0 International License* ([CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)) provided that the LaTeX source files are not used.
