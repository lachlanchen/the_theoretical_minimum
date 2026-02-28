[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# Meine Notizen für [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 Überblick

Dieses Repository ist in erster Linie ein dokumentenorientiertes Physik-Notizprojekt, das auf LaTeX-Manuskripten (`*.tex`) und einer gemeinsamen Bibliografie (`tm.bib`) basiert, mit unterstützenden Python-Skripten und Notebooks für Figuren und symbolische Prüfungen.

## 🎓 Vorlesungsnotizen von Leonard Susskinds [Theoretical Minimum](http://theoreticalminimum.com/home)

**Haftungsausschluss** Ich habe diese Notizen als Gedächtnisstütze für meinen eigenen Gebrauch erstellt; wenn Sie sie nützlich finden, ist das willkommen, ich wäre aber dankbar, wenn Sie mir sagen würden, dass Sie sie verwenden. Sie sind _nicht_ als Ersatz für das Mitverfolgen der Vorlesungen gedacht. Das geistige Eigentum für alle aus den Vorlesungen abgeleiteten Inhalte liegt selbstverständlich bei Professor Susskind; eventuelle Fehler sind jedoch meine eigenen.

Die Notizen wurden mit [TexStudio](https://www.texstudio.org/) erstellt, und die Bibliografie mit [JabRef](https://www.jabref.org/).

## ✨ Funktionen

- 📚 Kursorganisierte LaTeX-Manuskripte für Kerninhalte der Theoretical-Minimum-Themen.
- 📖 Zentrale Bibliografie (`tm.bib`), die über mehrere Dokumente hinweg geteilt wird.
- 🖼️ Große, wiederverwendbare Figure-Bibliothek in `figs/`.
- 🧰 Werkzeuge zur Bildpflege und Figuren-Erstellung (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Rechnerische Ergänzungen in Jupyter-Notebooks mit `pytearcat`.
- 🧪 NetLogo-Modell (`Ising.nlogo`) für die Visualisierung von Domänenwänden.

## 🗂️ Projektstruktur

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── .auto-readme-work/
├── notebooks/
├── *.tex                 # Vorlesungsnotizen, Übungen, Glossar, QFT-Ergänzungen
├── *.py                  # Hilfsprogramme und Plot-Skripte
├── notebooks/*.ipynb      # Rechnerische Notebooks
├── Ising.nlogo
└── tm.wpr
```

## 🚀 Schnellstart

| Ziel | Befehl(e) |
|---|---|
| Ein Manuskript kompilieren | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Kosmologie-Plots neu erzeugen | `python plot_scale.py` |
| Nicht referenzierte Figuren prüfen | `python audit-images.py --figs ./figs` |
| Notebooks öffnen | `jupyter notebook` |

## 📚 Kursnotizen-Index

| Datei | Beschreibung |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Sonstige Vorlesungen |
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

## 🧪 Übungen

| Datei | Beschreibung |
|---|---|
| `gr-exercises.tex` | Ausgeführte Beispiele aus [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Mithilfe von [pytearcat](https://arxiv.org/abs/2106.15016) den Einstein-Tensor für die Friedmann-Lemaître-Robertson-Walker-Metrik berechnen |
| `schwartzchild.ipynb` | Mit pytearcat den Einstein-Tensor für die Schwarzschild-Metrik berechnen |

Hinweis: In einer früheren README war `schwartzchild.ipnb` erwähnt; die Datei im Repository heißt `schwartzchild.ipynb`.

## 🧰 Hilfsprogramme

| Datei | Beschreibung |
|---|---|
| `audit-images.py` | Verwendet zur Ermittlung nicht referenzierter Bilddateien und zum Erzeugen von `rm.sh` mit `git rm`-Befehlen |
| `ising1.py` | Erforschung von Symmetriebrechung aus Vorlesung 7 anhand eines eindimensionalen Ising-Modells |
| `Ising.nlogo` | Demonstration von Domänenwänden |
| `plot-quartic.py` | Verwendet, um den "mexikanischen Hut" für das Higgs-Boson zu plotten |
| `plot_scale.py` | Verwendet, um Skalierungsparameter-Kurven für die Kosmologie zu plotten |
| `plot1.py` | Visualisierungs-Helfer im Stil einer Riemann-Fläche (adaptiert aus dem verlinkten Gist im Quelltext) |
| `plot2.py` | Alternative Version des Visualisierungs-Helfers `plot1.py` |
| `template.py` | Vorlage für Python-Programme |
| `tm.wpr` | Wing-IDE-Projekt für Hilfsdateien |

## 🧮 Beweise zur Ergänzung von *QFT in a Nutshell*

| Datei | Beschreibung |
|---|---|
| `qft1.tex` | Motivation und Grundlagen |
| `qft2.tex` | Dirac und der Spinor |

## ✅ Voraussetzungen

- Eine LaTeX-Distribution mit `lualatex` und BibTeX-Werkzeugen.
- `makeglossaries` für Dokumente mit Glossareinträgen.
- Python 3 mit `numpy` und `matplotlib` für Hilfsskripte.
- Jupyter Notebook/Lab für `.ipynb`-Dateien.
- `pytearcat` für Kosmologie-/Schwarzschild-Notebook-Workflows.
- Optional: [TexStudio](https://www.texstudio.org/) und [JabRef](https://www.jabref.org/).

## 🧱 Installation

Aktuell ist keine Paketmanager-Datei vorhanden (`requirements.txt`, `pyproject.toml` usw. werden nicht bereitgestellt), daher erfolgt das Setup manuell.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Falls Ihrer TeX-Distribution Komponenten fehlen, installieren Sie diese Pakete:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 Verwendung

### 🧪 Vorlesungsnotizen kompilieren (LaTeX)

Viele Quellen geben LuaLaTeX explizit an (`% !TeX program = lualatex`). Eine allgemeine Build-Folge:

```bash
# Beispiel: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Für Dateien ohne Glossar verwenden Sie `makeglossaries` nicht.

### 🧬 Hilfsskripte ausführen

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

### 📓 Notebooks verwenden

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ Konfiguration

Dieses Repository ist absichtlich leichtgewichtig und größtenteils dateibasiert.

- Bildpfadkonventionen beruhen auf `figs/` und `\graphicspath{{figs/}}` in den TeX-Dateien.
- Standardwerte der Skripte:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: enthält einstellbare Simulations-Flags (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Momentan gibt es keine zentrale Konfigurationsdatei.

## 🧭 Beispiele

### 🪐 Beispiel 1: Kosmologische Skalenfaktor-Plots neu erzeugen

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 Beispiel 2: Nichtreferenzierte Bilder prüfen und bereinigen

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 Beispiel 3: Notizen zu Advanced Quantum Mechanics erstellen

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 Entwicklungsnotizen

- Umfang: persönliche, weiterentwickelte Vorlesungsnotizen und rechnerische Ergänzungen.
- Die Build-Automatisierung ist bewusst minimal gehalten; die Befehle werden manuell ausgeführt.
- `.gitignore` ist LaTeX-fokussiert und schließt typische Build-Artefakte aus.
- `figs/` ist groß; `audit-images.py` ist hilfreich, um Bildreferenzen sauber zu halten.

## 🛠️ Fehlerbehebung

- `tikz-feynman`-Fehler: Mit `lualatex` kompilieren (von den Quelltexten empfohlen).
- Fehlende Glossareinträge/Ausgaben: `makeglossaries <basename>` zwischen LaTeX-Durchläufen ausführen.
- Fehlende Literaturverweise: Sicherstellen, dass `bibtex <basename>` ausgeführt wird und `tm.bib` vorhanden ist.
- Python-Importfehler (`numpy`, `matplotlib`, `pytearcat`): Benötigte Pakete in Ihrem aktiven Environment installieren.
- Notebook-Kernel-Mismatch: Wählen Sie die Umgebung, in der die Abhängigkeiten installiert sind.

## 🗺️ Roadmap

- Reproduzierbare Build-Automatisierung ergänzen (zum Beispiel: `latexmk`/Makefile-Wrapper pro Manuskript).
- Gesperrte Python-Abhängigkeitsmetadaten ergänzen.
- `i18n/` mit übersetzten README-Varianten füllen.
- Festlegen, welche Manuskripte als stabile/finale Schnappschüsse gelten.

## 🤝 Mitwirken

Beiträge sind willkommen, insbesondere:

- Tippfehler sowie Rechen-/Notation-korrekturen.
- Bereinigung kaputter Links und Referenzen.
- Verbesserungen an Build und Dokumentation.
- Reproduzierbarkeit von Figuren/Skripten verbessern.

Vorgeschlagener Ablauf:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 Danksagungen

Danke an die Entwickler und Maintainer der hier eingesetzten Werkzeuge, insbesondere an LaTeX, LuaLaTeX, Matplotlib, Jupyter und pytearcat.

## ⚖️ Lizenz

Dieses Repository wird unter der Lizenz `CC0-1.0` veröffentlicht. Siehe [`LICENSE`](../LICENSE).

- Leonard Susskind und Mitwirkende für die *Theoretical Minimum*-Vorlesungen.
- Zu den in diesem Projekt verwendeten Werkzeugen gehören [TexStudio](https://www.texstudio.org/) und [JabRef](https://www.jabref.org/).

## ⚖️ Lizenz

Der repositoryweite Lizenztext liegt in [LICENSE](../LICENSE) vor und lautet aktuell **CC0 1.0 Universal**.

Hinweis: Einige einzelne Quelldateien enthalten eigene Copyright-/Lizenzheader. Bitte bewahren Sie diese Hinweise bei Wiederverwendung von Code auf.


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
