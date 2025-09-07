# Pāli Platform: The Official Manual

This user's manual marks the end of the testing phase of `Pāli Platform 3` because during the revision the program has been substantially tested, fixed, and enhanced. What is said in the manual is guaranteed to work as expected.

Unlike other Pāli books by the author, this book uses a simpler technique for entering Pāli characters. This can lessen the headaches of subsequent editors.

The manual has a lot of pictures, mostly screenshots taken from a Linux environment (see Colophon). These images reside in the corresponding directory. Moreover, additional icon fonts other than those provided by the TeX program has to be present in their directory.

## How to build the book

All you need is TeX Live and the skill of using it. To install the program, consult the [quick installation guide](https://tug.org/texlive/quickinstall.html). The full installation is huge (7GB+). To minimize it, documentation and source files can be excluded, as well as languages other than English. Many packages are not really used such as additional fonts, but it is too nitpicky to microselect them. If space is not a problem, it is better to install most of them.

At least, these fonts are used in the book: TeX Gyre Schola, TeX Gyre Heros, and DejaVu Sans Mono. Make sure they are installed properly. Or you can change these to your favorite ones by changing the `fontspec` commands in `preamble.tex`.

Typesetting in LaTeX is definitely difficult, even by competent programmers. You have to learn new language syntax and several conventions. I suppose that you have already passed this requirement.

To build the whole book, follow these steps:
1. Comment out `includeonly` in `preamble.tex` (see toward the end), if it has not yet been done.
2. Open a terminal console at the book's folder and type these (normally you need to process more than once, and sometimes twice is not enough):
    ```
    $ lualatex ppman
    $ lualatex ppman
    (or maybe another one for sure)
    $ lualatex ppman
    ```
3. If `ppman.pdf` is produced, the build is successful. Otherwise, you have to fix errors, possibly by installing missing packages in case you have an insufficient installation. If any syntax errors occur, you have to fix those too.
4. If only some chapters are needed, edit and uncomment `includeonly` in `preamble.tex`, and rebuild it again. You can see the sequence of files in `ppman-base.tex`.

