[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# Mes notes pour les cours [Theoretical Minimum](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 Vue d'ensemble

Ce dépôt est avant tout un projet de notes de physique orienté documentation, construit autour de manuscrits LaTeX (`*.tex`) et d'une bibliographie partagée (`tm.bib`), avec des scripts Python et des notebooks Jupyter pour les figures et les vérifications symboliques.

## 🎓 Notes de cours de Leonard Susskind sur [Theoretical Minimum](http://theoreticalminimum.com/home)

**Avertissement** J'ai créé ces notes comme aide-mémoire pour mon usage personnel ; si elles vous sont utiles, vous êtes les bienvenu(e)s, mais j'apprécierais que vous m'en informiez. Elles ne sont _pas_ destinées à remplacer l'écoute des cours. La propriété intellectuelle de tout matériel issu des cours appartient bien entendu au professeur Susskind ; les éventuelles erreurs sont cependant les miennes.

Les notes ont été créées avec [TexStudio](https://www.texstudio.org/), et la bibliographie avec [JabRef](https://www.jabref.org/).

## ✨ Fonctionnalités

- 📚 Manuscrits LaTeX organisés par cours pour les sujets principaux du Theoretical Minimum.
- 📖 Bibliographie centrale (`tm.bib`) partagée entre les documents.
- 🖼️ Grande bibliothèque de figures réutilisables dans `figs/`.
- 🧰 Utilitaires pour l'hygiène des figures et la génération de figures (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Suppléments de calcul dans des notebooks Jupyter utilisant `pytearcat`.
- 🧪 Modèle NetLogo (`Ising.nlogo`) pour la visualisation de parois de domaine.

## 🗂️ Structure du projet

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── .auto-readme-work/
├── notebooks/
├── *.tex                 # Notes de cours, exercices, glossaire, compléments QFT
├── *.py                  # Utilitaires et scripts de tracé
├── notebooks/*.ipynb      # Notebooks de calcul
├── Ising.nlogo
└── tm.wpr
```

## 🚀 Démarrage rapide

| Objectif | Commande(s) |
|---|---|
| Compiler un manuscrit | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Régénérer les graphiques de cosmologie | `python plot_scale.py` |
| Auditer les figures non référencées | `python audit-images.py --figs ./figs` |
| Ouvrir les notebooks | `jupyter notebook` |

## 📚 Index des notes de cours

| Fichier | Description |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Cours divers |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Bibliographie du Theoretical Minimum |

## 🧪 Exercices

| Fichier | Description |
|---|---|
| `gr-exercises.tex` | Exemples corrigés de [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Utilise [pytearcat](https://arxiv.org/abs/2106.15016) pour calculer le tenseur d'Einstein pour la métrique de Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | Utilise pytearcat pour calculer le tenseur d'Einstein pour la métrique de Schwarzschild |

Remarque : le texte README précédent faisait référence à `schwartzchild.ipnb` ; le fichier du dépôt est `schwartzchild.ipynb`.

## 🧰 Programmes utilitaires

| Fichier | Description |
|---|---|
| `audit-images.py` | Utilisé pour identifier les fichiers images non référencés et générer `rm.sh` avec des commandes `git rm` |
| `ising1.py` | Explorer la rupture de symétrie à partir du cours 7, avec un modèle d'Ising unidimensionnel |
| `Ising.nlogo` | Démonstration de parois de domaine |
| `plot-quartic.py` | Utilisé pour tracer le chapeau mexicain du boson de Higgs |
| `plot_scale.py` | Utilisé pour tracer les courbes du paramètre d'échelle cosmologique |
| `plot1.py` | Utilitaire de visualisation de type surface de Riemann (adapté du gist lié à la source) |
| `plot2.py` | Version alternative de l'utilitaire de visualisation `plot1.py` |
| `template.py` | Modèle pour les programmes Python |
| `tm.wpr` | Projet Wing IDE pour les fichiers utilitaires |

## 🧠 Suppléments de démonstrations de *QFT in a Nutshell*

| Fichier | Description |
|---|---|
| `qft1.tex` | Motivation et fondation |
| `qft2.tex` | Dirac et le spineur |

## ✅ Prérequis

- Une distribution LaTeX avec `lualatex` et les outils BibTeX.
- `makeglossaries` pour les documents qui utilisent des entrées de glossaire.
- Python 3 avec `numpy` et `matplotlib` pour les scripts utilitaires.
- Jupyter Notebook/Lab pour les fichiers `.ipynb`.
- `pytearcat` pour les flux de travail des notebooks cosmologie/Schwarzschild.
- Optionnel : [TexStudio](https://www.texstudio.org/) et [JabRef](https://www.jabref.org/).

## 🧱 Installation

Aucun fichier de gestion de paquets n'est actuellement fourni (`requirements.txt`, `pyproject.toml`, etc. sont absents), donc l'installation est manuelle.

```bash
# 1) Clone

git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Si votre distribution LaTeX manque de composants, installez les paquets :

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 Utilisation

### 🧪 Compiler les notes de cours (LaTeX)

De nombreuses sources précisent explicitement LuaLaTeX (`% !TeX program = lualatex`). Une séquence de compilation générale :

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Pour les fichiers qui n'utilisent pas de glossaires, omettez `makeglossaries`.

### 🧬 Exécuter les scripts utilitaires

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

### 📓 Utiliser les notebooks

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ Configuration

Ce dépôt est volontairement léger et majoritairement piloté par les fichiers.

- Les conventions de chemins des figures sont basées sur `figs/` et `\graphicspath{{figs/}}` dans les fichiers TeX.
- Valeurs par défaut des scripts :
  - `audit-images.py` : `--figs ./figs`
  - `ising1.py` : inclut des options de simulation configurables (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Aucun fichier de configuration centralisé n'existe actuellement.

## 🧭 Exemples

### 🪐 Exemple 1 : Régénérer les tracés du facteur d'échelle cosmologique

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 Exemple 2 : Auditer et nettoyer les images non référencées

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 Exemple 3 : Construire les notes d'Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 Notes de développement

- Portée : notes de cours personnelles, évolutives, et compléments de calcul.
- L'automatisation de compilation est volontairement minimale ; les commandes sont lancées manuellement.
- `.gitignore` est centré sur LaTeX et exclut les artefacts de build typiques.
- `figs/` est volumineux ; `audit-images.py` est utile pour maintenir proprement les références aux figures.

## 🛠️ Dépannage

- Erreurs `tikz-feynman` : compiler avec `lualatex` (recommandé par les fichiers source).
- Entrées/sorties de glossaire manquantes : exécuter `makeglossaries <basename>` entre les passes LaTeX.
- Références bibliographiques manquantes : assurez-vous d'exécuter `bibtex <basename>` et que `tm.bib` est présent.
- Erreurs d'import Python (`numpy`, `matplotlib`, `pytearcat`) : installez les paquets requis dans votre environnement actif.
- Incompatibilité de kernel de notebook : sélectionnez l'environnement où les dépendances sont installées.

## 🗺️ Feuille de route

- Ajouter une automatisation de build reproductible (par exemple : wrappers `latexmk`/Makefile par manuscrit).
- Ajouter des métadonnées de dépendances Python figées.
- Peupler `i18n/` avec des variantes README traduites.
- Préciser quels manuscrits sont considérés comme stables ou snapshots finaux.

## 🤝 Contribuer

Les contributions sont bienvenues, en particulier :

- Corrections de fautes de frappe et d'équations/symboles.
- Nettoyage des liens cassés et des références.
- Améliorations de la documentation et de la compilation.
- Améliorations de reproductibilité des figures/scripts.

Workflow suggéré :

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 Remerciements

- Leonard Susskind et ses collaborateurs pour les cours *Theoretical Minimum*.
- Les outils utilisés dans ce projet incluent [TexStudio](https://www.texstudio.org/) et [JabRef](https://www.jabref.org/).

## ⚖️ Licence

Ce dépôt est publié sous la licence `CC0-1.0`. Voir [`LICENSE`](../LICENSE).

- Leonard Susskind et ses collaborateurs pour les cours *Theoretical Minimum*.
- Les outils utilisés dans ce projet incluent [TexStudio](https://www.texstudio.org/) et [JabRef](https://www.jabref.org/).

## ⚖️ Licence

Le texte de licence de niveau dépôt est fourni dans [LICENSE](../LICENSE), actuellement **CC0 1.0 Universal**.

Remarque : certains fichiers source individuels incluent leurs propres en-têtes de copyright/licence. Conservez ces mentions si vous réutilisez le code.


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
