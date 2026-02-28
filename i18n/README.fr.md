[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="Bannière LazyingArt" />
</p>

# Mes notes pour les cours [Theoretical Minimum](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## Vue d'ensemble

Ce dépôt est avant tout un projet de notes de physique orienté documentation, construit autour de manuscrits LaTeX (`*.tex`) et d'une bibliographie partagée (`tm.bib`), avec des scripts Python et des notebooks en soutien pour les figures et les vérifications symboliques.

## Notes de cours basées sur [Theoretical Minimum](http://theoreticalminimum.com/home) de Leonard Susskind

**Avertissement** J'ai rédigé ces notes comme aide-mémoire pour mon usage personnel ; si elles vous sont utiles, vous êtes les bienvenu(e)s, mais j'apprécierais que vous me le signaliez si vous les utilisez. Elles ne sont _pas_ destinées à remplacer l'écoute des cours. La propriété intellectuelle de tout contenu dérivé des cours appartient, bien entendu, au Professeur Susskind ; les erreurs éventuelles, en revanche, sont de ma responsabilité.

Les notes ont été créées avec [TexStudio](https://www.texstudio.org/), et la bibliographie avec [JabRef](https://www.jabref.org/).

## Fonctionnalités

- 📚 Manuscrits LaTeX organisés par cours pour les thèmes centraux de Theoretical Minimum.
- 📖 Bibliographie centrale (`tm.bib`) partagée entre les documents.
- 🖼️ Grande bibliothèque de figures réutilisables dans `figs/`.
- 🧰 Utilitaires pour l'hygiène et la génération de figures (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Compléments de calcul dans des notebooks Jupyter utilisant `pytearcat`.
- 🧪 Modèle NetLogo (`Ising.nlogo`) pour la visualisation des parois de domaine.

## Structure du projet

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── *.tex                 # Notes de cours, exercices, glossaire, compléments QFT
├── *.py                  # Utilitaires d'aide et scripts de tracé
├── *.ipynb               # Notebooks de calcul
├── Ising.nlogo
└── tm.wpr
```

## Démarrage rapide

| Objectif | Commande(s) |
|---|---|
| Compiler un manuscrit | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Régénérer les tracés de cosmologie | `python plot_scale.py` |
| Auditer les figures non référencées | `python audit-images.py --figs ./figs` |
| Ouvrir les notebooks | `jupyter notebook` |

## Index des notes de cours

| Fichier | Description |
|---|---|
| `aqm.tex` | [Mécanique quantique avancée](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Intrication quantique](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmologie](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [Relativité générale](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Cours divers |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Démystifier le boson de Higgs](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Physique des particules 1 : concepts de base](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Physique des particules 2 : modèle standard](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Physique des particules 3 : supersymétrie et grande unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Mécanique statistique](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Bibliographie de Theoretical Minimum |

## Exercices

| Fichier | Description |
|---|---|
| `gr-exercises.tex` | Exemples résolus de [Relativité générale](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Utilise [pytearcat](https://arxiv.org/abs/2106.15016) pour calculer le tenseur d'Einstein pour la métrique de Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | Utilise pytearcat pour calculer le tenseur d'Einstein pour la métrique de Schwarzschild |

Remarque : une version antérieure du README faisait référence à `schwartzchild.ipnb` ; le fichier présent dans le dépôt est `schwartzchild.ipynb`.

## Programmes utilitaires

| Fichier | Description |
|---|---|
| `audit-images.py` | Sert à identifier les fichiers image non référencés et à générer `rm.sh` avec des commandes `git rm` |
| `ising1.py` | Explore la brisure de symétrie du cours 7, à l'aide d'un modèle d'Ising unidimensionnel |
| `Ising.nlogo` | Démonstration des parois de domaine |
| `plot-quartic.py` | Sert à tracer le « chapeau mexicain » pour le boson de Higgs |
| `plot_scale.py` | Sert à tracer les courbes du paramètre d'échelle en cosmologie |
| `plot1.py` | Outil de visualisation de type surface de Riemann (adapté du gist lié dans la source) |
| `plot2.py` | Version alternative de l'outil de visualisation `plot1.py` |
| `template.py` | Gabarit pour les programmes Python |
| `tm.wpr` | Projet Wing IDE pour les fichiers utilitaires |

## Preuves en complément de *QFT in a Nutshell*

| Fichier | Description |
|---|---|
| `qft1.tex` | Motivation et fondements |
| `qft2.tex` | Dirac et le spineur |

## Prérequis

- Une distribution LaTeX avec l'outillage `lualatex` et BibTeX.
- `makeglossaries` pour les documents qui utilisent des entrées de glossaire.
- Python 3 avec `numpy` et `matplotlib` pour les scripts utilitaires.
- Jupyter Notebook/Lab pour les fichiers `.ipynb`.
- `pytearcat` pour les workflows des notebooks cosmologie/Schwarzschild.
- Optionnel : [TexStudio](https://www.texstudio.org/) et [JabRef](https://www.jabref.org/).

## Installation

Aucun fichier de gestion de paquets n'est actuellement fourni (`requirements.txt`, `pyproject.toml`, etc. sont absents), la configuration est donc manuelle.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Si des composants manquent dans votre distribution TeX, installez les paquets pour :

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## Utilisation

### Compiler les notes de cours (LaTeX)

De nombreuses sources spécifient explicitement LuaLaTeX (`% !TeX program = lualatex`). Séquence de compilation générale :

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Pour les fichiers qui n'utilisent pas de glossaire, omettez `makeglossaries`.

### Exécuter les scripts utilitaires

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

### Utiliser les notebooks

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## Configuration

Ce dépôt est volontairement léger et principalement piloté par les fichiers.

- Les conventions de chemins pour les figures reposent sur `figs/` et `\graphicspath{{figs/}}` dans les fichiers TeX.
- Valeurs par défaut des scripts :
  - `audit-images.py` : `--figs ./figs`
  - `ising1.py` : inclut des options de simulation ajustables (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Aucun fichier de configuration centralisé n'existe actuellement.

## Exemples

### Exemple 1 : régénérer les tracés du facteur d'échelle cosmologique

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### Exemple 2 : auditer et nettoyer les images non référencées

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### Exemple 3 : compiler les notes d'Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## Notes de développement

- Portée : notes de cours personnelles, évolutives, et compléments de calcul.
- L'automatisation de compilation est volontairement minimale ; les commandes sont lancées manuellement.
- `.gitignore` est orienté LaTeX et exclut les artefacts de compilation habituels.
- `figs/` est volumineux ; `audit-images.py` est utile pour garder des références de figures propres.

## Dépannage

- Erreurs `tikz-feynman` : compilez avec `lualatex` (recommandé par les fichiers source).
- Entrées/sorties de glossaire manquantes : exécutez `makeglossaries <basename>` entre les passes LaTeX.
- Références bibliographiques manquantes : assurez-vous que `bibtex <basename>` est exécuté et que `tm.bib` est présent.
- Erreurs d'import Python (`numpy`, `matplotlib`, `pytearcat`) : installez les paquets requis dans votre environnement actif.
- Incohérence de noyau notebook : sélectionnez l'environnement où les dépendances sont installées.

## Feuille de route

- Ajouter une automatisation de build reproductible (par exemple : wrappers `latexmk`/Makefile par manuscrit).
- Ajouter des métadonnées de dépendances Python épinglées.
- Remplir `i18n/` avec les variantes traduites du README.
- Clarifier quels manuscrits sont considérés comme des instantanés stables/finaux.

## Contributions

Les contributions sont bienvenues, en particulier :

- Corrections de coquilles et de notations/équations.
- Correction des liens brisés et nettoyage des références.
- Améliorations de la documentation et de la compilation.
- Améliorations de la reproductibilité des figures/scripts.

Workflow suggéré :

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## Remerciements

- Leonard Susskind et ses collaborateurs pour les cours *Theoretical Minimum*.
- Les outils utilisés dans ce projet incluent [TexStudio](https://www.texstudio.org/) et [JabRef](https://www.jabref.org/).

## Licence

Le texte de la licence au niveau du dépôt est fourni dans [LICENSE](../LICENSE), actuellement sous **CC0 1.0 Universal**.

Remarque : certains fichiers source individuels incluent leurs propres en-têtes de copyright/licence. Conservez ces mentions lors de la réutilisation de code.
