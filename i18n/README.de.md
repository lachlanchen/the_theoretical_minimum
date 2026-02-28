[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# Meine Notizen zu [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## Überblick

Dieses Repository ist in erster Linie ein dokumentenorientiertes Physik-Notizprojekt, das auf LaTeX-Manuskripten (`*.tex`) und einer gemeinsamen Bibliografie (`tm.bib`) basiert, mit unterstützenden Python-Skripten und Notebooks für Abbildungen und symbolische Prüfungen.

## Vorlesungsnotizen basierend auf Leonard Susskinds [Theoretical Minimum](http://theoreticalminimum.com/home)

**Hinweis** Ich habe diese Notizen als Gedächtnisstütze für meinen eigenen Gebrauch erstellt; wenn sie für dich nützlich sind, freut mich das, aber ich wäre dankbar, wenn du mir Bescheid gibst, dass du sie nutzt. Sie sind _nicht_ als Ersatz für das Anhören der Vorlesungen gedacht. Die geistigen Eigentumsrechte für sämtliches aus den Vorlesungen abgeleitetes Material liegen selbstverständlich bei Professor Susskind; etwaige Fehler gehen jedoch auf mein Konto.

Die Notizen wurden mit [TexStudio](https://www.texstudio.org/) erstellt und die Bibliografie mit [JabRef](https://www.jabref.org/).

## Features

- 📚 Nach Kursen organisierte LaTeX-Manuskripte zu zentralen Theoretical-Minimum-Themen.
- 📖 Zentrale Bibliografie (`tm.bib`), die von mehreren Dokumenten gemeinsam genutzt wird.
- 🖼️ Große wiederverwendbare Abbildungssammlung in `figs/`.
- 🧰 Hilfswerkzeuge für Abbildungs-Hygiene und Abbildungsgenerierung (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Rechnergestützte Ergänzungen in Jupyter-Notebooks mit `pytearcat`.
- 🧪 NetLogo-Modell (`Ising.nlogo`) zur Visualisierung von Domänenwänden.

## Projektstruktur

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── *.tex                 # Lecture notes, exercises, glossary, QFT supplements
├── *.py                  # Helper utilities and plotting scripts
├── *.ipynb               # Computational notebooks
├── Ising.nlogo
└── tm.wpr
```

## Schnellstart

| Ziel | Befehl(e) |
|---|---|
| Ein Manuskript kompilieren | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Kosmologie-Plots neu erzeugen | `python plot_scale.py` |
| Nicht referenzierte Abbildungen prüfen | `python audit-images.py --figs ./figs` |
| Notebooks öffnen | `jupyter notebook` |

## Index der Kursnotizen

| Datei | Beschreibung |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Verschiedene Vorlesungen |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Bibliografie für Theoretical Minimum |

## Übungen

| Datei | Beschreibung |
|---|---|
| `gr-exercises.tex` | Durchgerechnete Beispiele aus [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Mit [pytearcat](https://arxiv.org/abs/2106.15016) den Einstein-Tensor für die Friedmann-Lemaître-Robertson-Walker-Metrik berechnen |
| `schwartzchild.ipynb` | Mit pytearcat den Einstein-Tensor für die Schwarzschild-Metrik berechnen |

Hinweis: In einem früheren README-Text wurde `schwartzchild.ipnb` erwähnt; die Datei im Repository heißt `schwartzchild.ipynb`.

## Hilfsprogramme

| Datei | Beschreibung |
|---|---|
| `audit-images.py` | Wird verwendet, um nicht referenzierte Bilddateien zu finden und `rm.sh` mit `git rm`-Befehlen zu erzeugen |
| `ising1.py` | Untersucht Symmetriebrechung aus Vorlesung 7 mit einem eindimensionalen Ising-Modell |
| `Ising.nlogo` | Demonstration von Domänenwänden |
| `plot-quartic.py` | Wird verwendet, um den Mexican-Hat-Verlauf für das Higgs-Boson zu plotten |
| `plot_scale.py` | Wird verwendet, um kosmologische Skalenparameter-Kurven zu plotten |
| `plot1.py` | Visualisierungs-Helfer im Riemannflächen-Stil (adaptiert aus dem im Quelltext verlinkten Gist) |
| `plot2.py` | Alternative Version des Visualisierungs-Helfers `plot1.py` |
| `template.py` | Vorlage für Python-Programme |
| `tm.wpr` | Wing-IDE-Projekt für Hilfsdateien |

## Beweise als Ergänzung zu *QFT in a Nutshell*

| Datei | Beschreibung |
|---|---|
| `qft1.tex` | Motivation und Grundlagen |
| `qft2.tex` | Dirac und der Spinor |

## Voraussetzungen

- Eine LaTeX-Distribution mit `lualatex` und BibTeX-Werkzeugen.
- `makeglossaries` für Dokumente, die Glossareinträge verwenden.
- Python 3 mit `numpy` und `matplotlib` für Hilfsskripte.
- Jupyter Notebook/Lab für `.ipynb`-Dateien.
- `pytearcat` für Cosmology-/Schwarzschild-Notebook-Workflows.
- Optional: [TexStudio](https://www.texstudio.org/) und [JabRef](https://www.jabref.org/).

## Installation

Aktuell gibt es keine Paketmanager-Datei (`requirements.txt`, `pyproject.toml` usw.), daher erfolgt die Einrichtung manuell.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Wenn deiner TeX-Distribution Komponenten fehlen, installiere Pakete für:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## Verwendung

### Vorlesungsnotizen kompilieren (LaTeX)

Viele Quelldateien geben LuaLaTeX explizit an (`% !TeX program = lualatex`). Eine allgemeine Build-Sequenz:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Für Dateien ohne Glossar `makeglossaries` weglassen.

### Hilfsskripte ausführen

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

### Notebooks verwenden

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## Konfiguration

Dieses Repository ist bewusst schlank gehalten und größtenteils dateibasiert.

- Konventionen für Abbildungspfade basieren auf `figs/` und `\graphicspath{{figs/}}` in TeX-Dateien.
- Skript-Standardwerte:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: enthält anpassbare Simulations-Flags (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Es gibt derzeit keine zentrale Konfigurationsdatei.

## Beispiele

### Beispiel 1: kosmologische Skalenfaktor-Plots neu erzeugen

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### Beispiel 2: nicht referenzierte Bilder prüfen und bereinigen

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### Beispiel 3: Notizen zur Fortgeschrittenen Quantenmechanik bauen

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## Entwicklungsnotizen

- Umfang: persönliche, fortlaufend weiterentwickelte Vorlesungsnotizen und rechnergestützte Ergänzungen.
- Die Build-Automatisierung ist bewusst minimal; Befehle werden manuell ausgeführt.
- `.gitignore` ist auf LaTeX ausgerichtet und schließt typische Build-Artefakte aus.
- `figs/` ist groß; `audit-images.py` hilft, Bildreferenzen sauber zu halten.

## Fehlerbehebung

- `tikz-feynman`-Fehler: mit `lualatex` kompilieren (von den Quelldateien empfohlen).
- Fehlende Glossareinträge/-ausgabe: `makeglossaries <basename>` zwischen LaTeX-Durchläufen ausführen.
- Fehlende Literaturverweise: sicherstellen, dass `bibtex <basename>` läuft und `tm.bib` vorhanden ist.
- Python-Importfehler (`numpy`, `matplotlib`, `pytearcat`): erforderliche Pakete in der aktiven Umgebung installieren.
- Notebook-Kernel passt nicht: die Umgebung auswählen, in der die Abhängigkeiten installiert sind.

## Roadmap

- Reproduzierbare Build-Automatisierung ergänzen (z. B. `latexmk`-/Makefile-Wrapper pro Manuskript).
- Metadaten mit festgelegten Python-Abhängigkeiten ergänzen.
- `i18n/` mit übersetzten README-Varianten vervollständigen.
- Klären, welche Manuskripte als stabile/finale Snapshots gelten.

## Beitragen

Beiträge sind willkommen, insbesondere:

- Tippfehler sowie Gleichungs-/Notationskorrekturen.
- Defekte Links und Bereinigung von Referenzen.
- Verbesserungen bei Build/Dokumentation.
- Verbesserungen der Reproduzierbarkeit von Abbildungen/Skripten.

Vorgeschlagener Workflow:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## Danksagungen

- Leonard Susskind und Mitarbeitende für die *Theoretical Minimum*-Vorlesungen.
- Zu den in diesem Projekt verwendeten Tools gehören [TexStudio](https://www.texstudio.org/) und [JabRef](https://www.jabref.org/).

## Lizenz

Der Repository-weite Lizenztext befindet sich in [LICENSE](../LICENSE), aktuell **CC0 1.0 Universal**.

Hinweis: Einige einzelne Quelldateien enthalten eigene Copyright-/Lizenz-Header. Diese Hinweise beim Wiederverwenden von Code bitte beibehalten.
