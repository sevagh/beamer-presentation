# beamer-presentation

This repo contains my favorite LaTeX Beamer presentation template I use in academia and industry.

## Prerequisites/dependencies

* A "full" texlive distribution, e.g., `texlive-full` on Ubuntu, `texlive-scheme-full` on Fedora
* make
* latexmk
* **[OPTIONAL]** [Pympress](https://github.com/Cimbali/pympress) for a better presentation tool including a private note display

**n.b.** I only use Linux, so I'm not sure how these instructions might work on a different OS.

## How to use this repo

* Create a new repo from the template
* Modify `presentation.tex` to include your content
* Build presenter pdf (with notes): `make presentation`
    * **[OPTIONAL]** Use `make presentation-dev` for dev mode with PDF file regeneration
    * **[OPTIONAL]** Use `make presentation-dev-pympress` to use Pympress for preview
* Build handout pdf (no notes): `make handout`

Compiled example PDFs can be seen in the [releases]() page.

## Features

* Generate two copies:
    1. Presenter copy with notes (compatible with Pympress) called `presentation.pdf`
    2. Handout copy, no notes, called `handout.pdf`
        * **n.b.** the `-jobname=handout` parameter controls both the name of the handout output file (`handout.pdf`) and is tested for `=="handout"` to disable notes in the TeX source code
* Include figures and subfigures
* Custom footnote citation commands to be displayed on the bottom of each slide
    * **n.b.** Some prefer citations at the end, but I prefer the citation shown with the content or the viewers forget about it
* Cast audio to the audience on Linux
* Two-column pros/cons slide
* Tikz timeline slides
* Code blocks slide (using Verb, verbatim, and Minted)
