[English](README.md) · [العربية](i18n/README.ar.md) · [Español](i18n/README.es.md) · [Français](i18n/README.fr.md) · [日本語](i18n/README.ja.md) · [한국어](i18n/README.ko.md) · [Tiếng Việt](i18n/README.vi.md) · [中文 (简体)](i18n/README.zh-Hans.md) · [中文（繁體）](i18n/README.zh-Hant.md) · [Deutsch](i18n/README.de.md) · [Русский](i18n/README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# My Notes for [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 Overview

This repository is primarily a document-first physics notes project built around LaTeX manuscripts (`*.tex`) and a shared bibliography (`tm.bib`), with supporting Python scripts and notebooks for figures and symbolic checks.

## 🎓 Lecture Notes from Leonard Susskind's [Theoretical Minimum](http://theoreticalminimum.com/home)

**Disclaimer** I have created these notes as an aide-mémoire for my own use; if you find them useful, you are welcome, but I'd appreciate it if you'd let me know if you are using them. They are _not_ intended as a substitute for listening to the lectures. The intellectual property for all material derived from the lectures belongs, of course, to Professor Susskind; any mistakes, however, are my own.

The notes were created using [TexStudio](https://www.texstudio.org/), and the bibliography by [JabRef](https://www.jabref.org/).

## ✨ Features

- 📚 Course-organized LaTeX manuscripts for core Theoretical Minimum topics.
- 📖 Central bibliography (`tm.bib`) shared across documents.
- 🖼️ Large reusable figure library in `figs/`.
- 🧰 Utilities for figure hygiene and figure generation (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Computational supplements in Jupyter notebooks using `pytearcat`.
- 🧪 NetLogo model (`Ising.nlogo`) for domain wall visualization.

## 🗂️ Project Structure

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── .auto-readme-work/
├── notebooks/
├── *.tex                 # Lecture notes, exercises, glossary, QFT supplements
├── *.py                  # Helper utilities and plotting scripts
├── notebooks/*.ipynb      # Computational notebooks
├── Ising.nlogo
└── tm.wpr
```

## 🚀 Quick Start

| Goal | Command(s) |
|---|---|
| Compile one manuscript | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Regenerate cosmology plots | `python plot_scale.py` |
| Audit unreferenced figures | `python audit-images.py --figs ./figs` |
| Open notebooks | `jupyter notebook` |

## 📚 Course Notes Index

| File | Description |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Miscellaneous lectures |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Bibliography for Theoretical Minimum |

## 🧪 Exercises

| File | Description |
|---|---|
| `gr-exercises.tex` | Worked examples from [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Use [pytearcat](https://arxiv.org/abs/2106.15016) to calculate Einstein tensor for Friedmann-Lemaître-Robertson-Walker metric |
| `schwartzchild.ipynb` | Use pytearcat to calculate Einstein tensor for Schwarzschild metric |

Note: earlier README text referenced `schwartzchild.ipnb`; the repository file is `schwartzchild.ipynb`.

## 🧰 Helper Programs

| File | Description |
|---|---|
| `audit-images.py` | Used to identify unreferenced image files and emit `rm.sh` with `git rm` commands |
| `ising1.py` | Explore broken symmetry from lecture 7, using a 1 dimensional Ising model |
| `Ising.nlogo` | Demonstration of domain walls |
| `plot-quartic.py` | Used to plot Mexican hat for Higgs boson |
| `plot_scale.py` | Used to plot cosmology scale-parameter curves |
| `plot1.py` | Riemann-surface style visualization helper (adapted from linked gist in source) |
| `plot2.py` | Alternate version of `plot1.py` visualization helper |
| `template.py` | Template for Python programs |
| `tm.wpr` | Wing IDE project for helper files |

## 📐 Proofs to Supplement *QFT in a Nutshell*

| File | Description |
|---|---|
| `qft1.tex` | Motivation and Foundation |
| `qft2.tex` | Dirac and the Spinor |

## ✅ Prerequisites

- A LaTeX distribution with `lualatex` and BibTeX tooling.
- `makeglossaries` for documents that use glossary entries.
- Python 3 with `numpy` and `matplotlib` for helper scripts.
- Jupyter Notebook/Lab for `.ipynb` files.
- `pytearcat` for cosmology/Schwarzschild notebook workflows.
- Optional: [TexStudio](https://www.texstudio.org/) and [JabRef](https://www.jabref.org/).

## 🧱 Installation

No package manager file is currently provided (`requirements.txt`, `pyproject.toml`, etc. are not present), so setup is manual.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

If your TeX distribution is missing components, install packages for:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 Usage

### 🧪 Compile lecture notes (LaTeX)

Many sources specify LuaLaTeX explicitly (`% !TeX program = lualatex`). A general build sequence:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

For files that do not use glossaries, omit `makeglossaries`.

### 🧬 Run helper scripts

```bash
# Find unreferenced images in ./figs and generate rm.sh
python audit-images.py --figs ./figs

# 1D Ising simulation (outputs figure in ./figs)
python ising1.py --m 100 --n 1000 --N 25 --T 0.001 --cool 0.01 --figs ./figs

# Plot helpers
python plot-quartic.py
python plot_scale.py
python plot1.py
python plot2.py
```

### 📓 Use notebooks

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ Configuration

This repository is intentionally lightweight and mostly file-driven.

- Figure path conventions are based on `figs/` and `\graphicspath{{figs/}}` in TeX files.
- Script defaults:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: includes tunable simulation flags (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- No centralized config file currently exists.

## 🧭 Examples

### 🪐 Example 1: Regenerate cosmology scale-factor plots

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 Example 2: Audit and clean unreferenced images

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 Example 3: Build Advanced Quantum Mechanics notes

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 Development Notes

- Scope: personal, evolving lecture notes and computational supplements.
- Build automation is intentionally minimal; commands are run manually.
- `.gitignore` is LaTeX-focused and excludes typical build artifacts.
- `figs/` is large; `audit-images.py` is useful for keeping image references tidy.

## 🛠️ Troubleshooting

- `tikz-feynman` errors: compile with `lualatex` (recommended by source files).
- Missing glossary entries/output: run `makeglossaries <basename>` between LaTeX passes.
- Missing bibliography references: ensure `bibtex <basename>` is run and `tm.bib` is present.
- Python import errors (`numpy`, `matplotlib`, `pytearcat`): install required packages in your active environment.
- Notebook kernel mismatch: select the environment where dependencies are installed.

## 🗺️ Roadmap

- Add reproducible build automation (for example: `latexmk`/Makefile wrappers per manuscript).
- Add pinned Python dependency metadata.
- Populate `i18n/` with translated README variants.
- Clarify which manuscripts are considered stable/final snapshots.

## 🤝 Contributing

Contributions are welcome, especially:

- Typos and equation/notation fixes.
- Broken links and reference cleanups.
- Build/documentation improvements.
- Figure/script reproducibility improvements.

Suggested workflow:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 Acknowledgements

Thank you to the creators and maintainers of the tools used here, especially LaTeX, LuaLaTeX, Matplotlib, Jupyter, and pytearcat.

## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |

## ⚖️ License

This repository is released under the `CC0-1.0` license. See [`LICENSE`](LICENSE).

- Leonard Susskind and collaborators for *Theoretical Minimum* lectures.
- Tools used in this project include [TexStudio](https://www.texstudio.org/) and [JabRef](https://www.jabref.org/).

## ⚖️ License

Repository-level license text is provided in [LICENSE](LICENSE), currently **CC0 1.0 Universal**.

Note: some individual source files include their own copyright/license headers. Preserve those notices when reusing code.
