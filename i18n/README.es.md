[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# Mis notas de [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## Resumen

Este repositorio es, principalmente, un proyecto de notas de física orientado a documentos, construido alrededor de manuscritos en LaTeX (`*.tex`) y una bibliografía compartida (`tm.bib`), con scripts de Python y notebooks como soporte para figuras y comprobaciones simbólicas.

## Notas de clase basadas en [Theoretical Minimum](http://theoreticalminimum.com/home) de Leonard Susskind

**Descargo de responsabilidad** He creado estas notas como aide-mémoire para mi propio uso; si te resultan útiles, eres bienvenido/a, pero agradecería que me avises si las estás usando. _No_ están pensadas como sustituto de escuchar las clases. La propiedad intelectual de todo el material derivado de las clases pertenece, por supuesto, al profesor Susskind; cualquier error, sin embargo, es mío.

Las notas se crearon con [TexStudio](https://www.texstudio.org/) y la bibliografía con [JabRef](https://www.jabref.org/).

## Características

- 📚 Manuscritos en LaTeX organizados por curso para temas centrales de Theoretical Minimum.
- 📖 Bibliografía central (`tm.bib`) compartida entre documentos.
- 🖼️ Gran biblioteca reutilizable de figuras en `figs/`.
- 🧰 Utilidades para higiene y generación de figuras (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Suplementos computacionales en notebooks de Jupyter usando `pytearcat`.
- 🧪 Modelo de NetLogo (`Ising.nlogo`) para visualizar paredes de dominio.

## Estructura del proyecto

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

## Inicio rápido

| Objetivo | Comando(s) |
|---|---|
| Compilar un manuscrito | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Regenerar gráficas de cosmología | `python plot_scale.py` |
| Auditar figuras no referenciadas | `python audit-images.py --figs ./figs` |
| Abrir notebooks | `jupyter notebook` |

## Índice de notas de curso

| Archivo | Descripción |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Clases misceláneas |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Bibliografía de Theoretical Minimum |

## Ejercicios

| Archivo | Descripción |
|---|---|
| `gr-exercises.tex` | Ejemplos resueltos de [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Usar [pytearcat](https://arxiv.org/abs/2106.15016) para calcular el tensor de Einstein para la métrica de Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | Usar pytearcat para calcular el tensor de Einstein para la métrica de Schwarzschild |

Nota: un texto anterior del README hacía referencia a `schwartzchild.ipnb`; el archivo en el repositorio es `schwartzchild.ipynb`.

## Programas auxiliares

| Archivo | Descripción |
|---|---|
| `audit-images.py` | Se usa para identificar archivos de imagen no referenciados y generar `rm.sh` con comandos `git rm` |
| `ising1.py` | Explora la ruptura de simetría de la clase 7, usando un modelo de Ising unidimensional |
| `Ising.nlogo` | Demostración de paredes de dominio |
| `plot-quartic.py` | Se usa para graficar el sombrero mexicano del bosón de Higgs |
| `plot_scale.py` | Se usa para graficar curvas del parámetro de escala cosmológico |
| `plot1.py` | Helper de visualización tipo superficie de Riemann (adaptado del gist enlazado en la fuente) |
| `plot2.py` | Versión alternativa del helper de visualización `plot1.py` |
| `template.py` | Plantilla para programas en Python |
| `tm.wpr` | Proyecto de Wing IDE para archivos auxiliares |

## Demostraciones para complementar *QFT in a Nutshell*

| Archivo | Descripción |
|---|---|
| `qft1.tex` | Motivación y fundamentos |
| `qft2.tex` | Dirac y el espinor |

## Requisitos previos

- Una distribución de LaTeX con `lualatex` y herramientas de BibTeX.
- `makeglossaries` para documentos que usan entradas de glosario.
- Python 3 con `numpy` y `matplotlib` para scripts auxiliares.
- Jupyter Notebook/Lab para archivos `.ipynb`.
- `pytearcat` para flujos de trabajo de notebooks de cosmología/Schwarzschild.
- Opcional: [TexStudio](https://www.texstudio.org/) y [JabRef](https://www.jabref.org/).

## Instalación

Actualmente no se proporciona archivo de gestor de paquetes (`requirements.txt`, `pyproject.toml`, etc.), por lo que la configuración es manual.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Si a tu distribución de TeX le faltan componentes, instala paquetes para:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## Uso

### Compilar notas de clase (LaTeX)

Muchos fuentes especifican LuaLaTeX explícitamente (`% !TeX program = lualatex`). Secuencia general de compilación:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Para archivos que no usan glosarios, omite `makeglossaries`.

### Ejecutar scripts auxiliares

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

### Usar notebooks

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## Configuración

Este repositorio es intencionalmente ligero y está impulsado, sobre todo, por archivos.

- Las convenciones de rutas de figuras se basan en `figs/` y `\graphicspath{{figs/}}` en archivos TeX.
- Valores predeterminados de scripts:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: incluye flags ajustables de simulación (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Actualmente no existe un archivo de configuración centralizado.

## Ejemplos

### Ejemplo 1: regenerar gráficas del factor de escala cosmológico

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### Ejemplo 2: auditar y limpiar imágenes no referenciadas

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### Ejemplo 3: compilar notas de Mecánica Cuántica Avanzada

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## Notas de desarrollo

- Alcance: notas de clase personales en evolución y suplementos computacionales.
- La automatización de compilación es intencionalmente mínima; los comandos se ejecutan manualmente.
- `.gitignore` está enfocado en LaTeX y excluye artefactos típicos de compilación.
- `figs/` es grande; `audit-images.py` es útil para mantener ordenadas las referencias de imágenes.

## Solución de problemas

- Errores de `tikz-feynman`: compila con `lualatex` (recomendado por los archivos fuente).
- Salida/entradas de glosario faltantes: ejecuta `makeglossaries <basename>` entre pasadas de LaTeX.
- Referencias bibliográficas faltantes: asegúrate de ejecutar `bibtex <basename>` y de que `tm.bib` esté presente.
- Errores de importación en Python (`numpy`, `matplotlib`, `pytearcat`): instala los paquetes requeridos en tu entorno activo.
- Incompatibilidad del kernel de notebook: selecciona el entorno donde estén instaladas las dependencias.

## Hoja de ruta

- Añadir automatización de compilación reproducible (por ejemplo: wrappers de `latexmk`/Makefile por manuscrito).
- Añadir metadatos de dependencias de Python con versiones fijadas.
- Completar `i18n/` con variantes traducidas del README.
- Aclarar qué manuscritos se consideran instantáneas estables/finales.

## Contribuir

Las contribuciones son bienvenidas, especialmente:

- Correcciones de typos y de ecuaciones/notación.
- Enlaces rotos y limpieza de referencias.
- Mejoras de compilación/documentación.
- Mejoras de reproducibilidad de figuras/scripts.

Flujo sugerido:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## Agradecimientos

- Leonard Susskind y colaboradores por las clases de *Theoretical Minimum*.
- Las herramientas usadas en este proyecto incluyen [TexStudio](https://www.texstudio.org/) y [JabRef](https://www.jabref.org/).

## Licencia

El texto de licencia a nivel de repositorio se encuentra en [LICENSE](../LICENSE), actualmente **CC0 1.0 Universal**.

Nota: algunos archivos fuente individuales incluyen sus propias cabeceras de copyright/licencia. Conserva esos avisos al reutilizar código.
