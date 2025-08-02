[![Formatting](https://github.com/ricarvid1/dsj-thesis/actions/workflows/format-latex.yml/badge.svg)](https://github.com/ricarvid1/dsj-thesis/actions/workflows/format-latex.yml)
[![Build latest](https://github.com/ricarvid1/dsj-thesis/actions/workflows/build_latest.yml/badge.svg)](https://github.com/ricarvid1/dsj-thesis/actions/workflows/build_latest.yml)
[![Publish release](https://github.com/ricarvid1/dsj-thesis/actions/workflows/release.yml/badge.svg)](https://github.com/ricarvid1/dsj-thesis/actions/workflows/release.yml)

# dsj-thesis

Title: "Programming Methodologies and Applications on a Multipurpose Reconfigurable Photonic Integrated Platform"

This repo contains the files, figures, references, etc. needed to compile my thesis manuscript for the degree of Ph.D. in Telecommunications at the [Universitat Politècnica de València](https://www.upv.es/index-en.html).

## License

This work is licensed under a Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License.

[![CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

## Citation

If you reference this thesis or the text/figures in it, please cite:

David Sanchez-Jacome. "Programming Methodologies and Applications on a Multipurpose Reconfigurable Photonic Integrated Platform." Universitat Politècnica de València, 2025.

## The running platform

This manuscript was written in [LaTeX](https://en.wikipedia.org/wiki/LaTeX) using [TeX Live 2025](https://www.tug.org/texlive/) packages on a GNU/Linux machine running [Pop!\_OS 22.04 LTS](https://system76.com/pop/download/).
The LaTeX code was compiled with [latexmk v4.86a](https://mgeier.github.io/latexmk.html) using the [luaTEX](https://www.luatex.org/) engine.
The text editor I have used is [Neovim v1.11.1](https://neovim.io/) in which the [VimTeX](https://github.com/lervag/vimtex) plugin has been instrumental providing linting, syntax checking, templates and useful snippets to navigate a LaTeX codebase project.
Writing LaTeX using Neovim was inspired and heavily influenced by [this great seven-series guide](https://ejmastnak.com/tutorials/vim-latex/intro/) as a way to achieve fast and powerful mathematical typesetting.

## Compiling the manuscript

To compile the manuscipt you need to have [TeX Live](https://www.tug.org/texlive/) installed.
The easiest way to do this is to install the full [TeX Live](https://www.tug.org/texlive/) distribution.
If you want to install only the packages needed to compile this manuscript, I recommend using the [texliveonthefly script](https://ctan.org/pkg/texliveonfly?lang=en) to download and install any missing packages.
Remember to use the [luaTEX](https://www.luatex.org/) engine.
After installing all needed packages, run the following commands to compile the manuscript:

```bash
git clone git@github.com:ricarvid1/dsj-thesis.git
cd dsj-thesis
latexmk -lualatex main.tex
# The output will be in the `main.pdf` file
latexmk -c  # Clean auxiliary files (optional)
```

## LSPs and formatting

For [language server protocol (LSP)](https://microsoft.github.io/language-server-protocol/) tooling [texlab v.5.22.1](https://github.com/latex-lsp/texlab) and [LTeX+](https://github.com/ltex-plus/ltex-ls-plus) have served as great complements for VimTeX.
The latter has turned out to be a great tool for enhancing the limited native spelling features of Neovim.

Automatic formatting has been performed by [bibytex-tidy v1.14.0](https://github.com/FlamingTempura/bibtex-tidy) and the great [latexindent.pl v3.24.5](https://github.com/cmhughes/latexindent.pl) Perl script.
The latter has provided me with the very useful feature of one-line-per-sentence wrapping which has not only made my LaTeX code/text more readable but also has helped me to organize and synthesize my ideas when writing them down.
The formatting rules can be found in the `format-latex.yml` file located in the `.github/` directory.

## CI

For continuous integration (CI), GitHub actions checking the formatting rules in `format-latex.yml` have been employed on each pull request and push.

## Template and figures

The template used for this manuscript was the [MIT thesis template in LaTeX](https://web.mit.edu/thesis/tex/) which provided most of the classes, packages, fonts and file structure needed during the writing process.
The figures in this manuscript have mostly been created/edited using [Inkscape v1.1](https://inkscape.org/) and [Google Slides](https://workspace.google.com/products/slides/).

## Why GitHub?

Since I have been actively working in collaborative software development for the last 4 years I decided to host this project on a [Github repo](https://github.com/ricarvid1/dsj-thesis) instead of [Overleaf](https://www.overleaf.com/).
In my humble opinion, and based on this experience, if a text editor/[IDE](https://medium.com/@rcpassos/writing-latex-documents-in-visual-studio-code-with-latex-workshop-d9af6a6b2815) is provisioned with the right plugins for LaTeX editing, the collaborative features of GitHub far outpace the ones offered by Overleaf.
This [thesis GitHub repo](https://github.com/ricarvid1/dsj-thesis) will be open-sourced after it has been accepted by the UPV library.
For questions and content discussion please raise an issue in this repo.
