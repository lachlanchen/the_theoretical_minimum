[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# Mis notas para [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 Visión general

Este repositorio es, sobre todo, un proyecto de apuntes de física centrado en documentos LaTeX (`*.tex`) y una bibliografía compartida (`tm.bib`), con scripts y cuadernos de Python para figuras y comprobaciones simbólicas de apoyo.

## 🎓 Apuntes de las conferencias de Leonard Susskind sobre [Theoretical Minimum](http://theoreticalminimum.com/home)

**Descargo de responsabilidad** He creado estos apuntes como recordatorio personal; si te resultan útiles, siéntete libre de usarlos, y te agradecería que me avisaras si los utilizas. **No** pretenden sustituir a la asistencia a las clases. La propiedad intelectual de todo el material derivado de las conferencias pertenece, por supuesto, al profesor Susskind; cualquier error, sin embargo, es responsabilidad mía.

Los apuntes se crearon con [TexStudio](https://www.texstudio.org/), y la bibliografía con [JabRef](https://www.jabref.org/).

## ✨ Características

- 📚 Manuscritos LaTeX organizados por curso para los temas centrales del Theoretical Minimum.
- 📖 Bibliografía central (`tm.bib`) compartida entre documentos.
- 🖼️ Amplia biblioteca de figuras reutilizables en `figs/`.
- 🧰 Utilidades para el control y la generación de figuras (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Complementos computacionales en cuadernos Jupyter usando `pytearcat`.
- 🧪 Modelo de NetLogo (`Ising.nlogo`) para visualizar paredes de dominio.

## 🗂️ Estructura del proyecto

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

## 🚀 Guía rápida

| Objetivo | Comando(s) |
|---|---|
| Compilar un manuscrito | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Regenerar gráficos de cosmología | `python plot_scale.py` |
| Auditar figuras sin referencias | `python audit-images.py --figs ./figs` |
| Abrir cuadernos | `jupyter notebook` |

## 📚 Índice de apuntes del curso

| Archivo | Descripción |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Conferencias varias |
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

## 🧪 Ejercicios

| Archivo | Descripción |
|---|---|
| `gr-exercises.tex` | Ejemplos trabajados de [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Use [pytearcat](https://arxiv.org/abs/2106.15016) para calcular el tensor de Einstein para la métrica de Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | Use pytearcat para calcular el tensor de Einstein para la métrica de Schwarzschild |

Nota: el texto anterior del README mencionaba `schwartzchild.ipnb`; el archivo del repositorio es `schwartzchild.ipynb`.

## 🧰 Programas auxiliares

| Archivo | Descripción |
|---|---|
| `audit-images.py` | Utilizado para identificar archivos de imagen sin referencias y generar `rm.sh` con comandos `git rm` |
| `ising1.py` | Exploración de simetría rota de la clase 7, usando un modelo de Ising unidimensional |
| `Ising.nlogo` | Demostración de paredes de dominio |
| `plot-quartic.py` | Utilizado para graficar el sombrero mexicano del bosón de Higgs |
| `plot_scale.py` | Utilizado para graficar curvas del parámetro de escala cosmológica |
| `plot1.py` | Auxiliar de visualización tipo superficie de Riemann (adaptado del gist enlazado en el origen) |
| `plot2.py` | Versión alternativa del auxiliar de visualización `plot1.py` |
| `template.py` | Plantilla para programas de Python |
| `tm.wpr` | Proyecto de Wing IDE para archivos auxiliares |

## 📐 Pruebas suplementarias de *QFT in a Nutshell*

| Archivo | Descripción |
|---|---|
| `qft1.tex` | Motivación y fundamentos |
| `qft2.tex` | Dirac y el espinor |

## ✅ Prerrequisitos

- Una distribución de LaTeX con `lualatex` y herramientas de BibTeX.
- `makeglossaries` para documentos que usan entradas del glosario.
- Python 3 con `numpy` y `matplotlib` para los scripts auxiliares.
- Jupyter Notebook/Lab para archivos `.ipynb`.
- `pytearcat` para los flujos de trabajo de los cuadernos de cosmología/Schwarzschild.
- Opcional: [TexStudio](https://www.texstudio.org/) y [JabRef](https://www.jabref.org/).

## 🧱 Instalación

No hay actualmente un gestor de paquetes incluido (`requirements.txt`, `pyproject.toml`, etc. no están presentes), por lo que la configuración es manual.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Si tu distribución de TeX carece de componentes, instala paquetes para:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 Uso

### 🧪 Compilar apuntes (LaTeX)

Muchas fuentes especifican explícitamente LuaLaTeX (`% !TeX program = lualatex`). Una secuencia de compilación general:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Para archivos que no usan glosarios, omite `makeglossaries`.

### 🧬 Ejecutar scripts auxiliares

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

### 📓 Usar cuadernos

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ Configuración

Este repositorio es intencionalmente ligero y se basa sobre todo en archivos.

- Las convenciones de ruta de figuras se basan en `figs/` y `\graphicspath{{figs/}}` en los archivos TeX.
- Parámetros por defecto de scripts:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: incluye opciones ajustables de simulación (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Actualmente no existe un archivo de configuración centralizado.

## 🧭 Ejemplos

### 🪐 Ejemplo 1: Regenerar gráficos del factor de escala cosmológico

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 Ejemplo 2: Auditar y limpiar imágenes sin referencias

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 Ejemplo 3: Construir apuntes de mecánica cuántica avanzada

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 Notas de desarrollo

- Alcance: apuntes de conferencias y complementos computacionales personales y en evolución.
- La automatización de compilación es intencionalmente mínima; los comandos se ejecutan manualmente.
- `.gitignore` está orientado a LaTeX y excluye artefactos de compilación habituales.
- `figs/` es grande; `audit-images.py` es útil para mantener ordenadas las referencias de imagen.

## 🛠️ Solución de problemas

- Errores de `tikz-feynman`: compila con `lualatex` (recomendado por los archivos de origen).
- Faltan entradas/salida del glosario: ejecuta `makeglossaries <basename>` entre pasadas de LaTeX.
- Faltan referencias bibliográficas: asegúrate de ejecutar `bibtex <basename>` y de que `tm.bib` esté presente.
- Errores de importación de Python (`numpy`, `matplotlib`, `pytearcat`): instala los paquetes requeridos en tu entorno activo.
- Desajuste de kernel del cuaderno: selecciona el entorno donde estén instaladas las dependencias.

## 🗺️ Hoja de ruta

- Añadir automatización de compilación reproducible (por ejemplo: wrappers `latexmk`/Makefile por manuscrito).
- Añadir metadatos de dependencias de Python fijadas.
- Rellenar `i18n/` con versiones traducidas del README.
- Aclarar qué manuscritos se consideran capturas estables/finales.

## 🤝 Colaboración

Las contribuciones son bienvenidas, especialmente:

- Errores tipográficos y correcciones de ecuaciones/símbolos.
- Enlaces rotos y limpieza de referencias.
- Mejoras en compilación/documentación.
- Mejoras de reproducibilidad de figuras/scripts.

Flujo de trabajo sugerido:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 Agradecimientos

Gracias a los creadores y mantenedores de las herramientas utilizadas aquí, en especial LaTeX, LuaLaTeX, Matplotlib, Jupyter y pytearcat.

## ⚖️ Licencia

Este repositorio se publica bajo la licencia `CC0-1.0`. Consulta [`LICENSE`](LICENSE).

- Leonard Susskind y colaboradores de las clases de *Theoretical Minimum*.
- Entre las herramientas usadas en este proyecto se incluyen [TexStudio](https://www.texstudio.org/) y [JabRef](https://www.jabref.org/).

## ⚖️ Licencia

El texto de licencia del repositorio se proporciona en [LICENSE](LICENSE), actualmente **CC0 1.0 Universal**.

Nota: algunos archivos fuente individuales incluyen sus propios encabezados de copyright/licencia. Conserva esos avisos al reutilizar código.


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
