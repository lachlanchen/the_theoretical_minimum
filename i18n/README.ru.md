[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# Мои заметки по [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 Обзор

Этот репозиторий в первую очередь представляет собой проект заметок по физике, ориентированный на документы, построенный вокруг LaTeX-манифестов (`*.tex`) и общей библиографии (`tm.bib`) с дополнительными скриптами на Python и блокнотами для построения графиков и символических проверок.

## 🎓 Конспекты лекций Леонарда Сусскинда [Theoretical Minimum](http://theoreticalminimum.com/home)

**Отказ от ответственности** Эти заметки я сделал как aide-mémoire для личного использования; если они оказались полезны, вы можете ими пользоваться, но, пожалуйста, дайте мне знать, если это так. Они **не** предназначены для замены прослушивания самих лекций. Все права на материалы, взятые из лекций, безусловно, принадлежат профессору Сусскинду; все ошибки, однако, мои.

Заметки создавались с помощью [TexStudio](https://www.texstudio.org/), а библиография — в [JabRef](https://www.jabref.org/).

## ✨ Возможности

- 📚 Рукописи LaTeX по ключевым темам Theoretical Minimum, разбитые по курсам.
- 📖 Единая библиография (`tm.bib`) для всех документов.
- 🖼️ Большая переиспользуемая библиотека рисунков в `figs/`.
- 🧰 Утилиты для обслуживания и генерации рисунков (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Вычислительные дополнения в Jupyter-ноутбуках с использованием `pytearcat`.
- 🧪 Модель NetLogo (`Ising.nlogo`) для визуализации доменных стенок.

## 🗂️ Структура проекта

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

## 🚀 Быстрый старт

| Цель | Команда(ы) |
|---|---|
| Скомпилировать один документ | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Пересоздать космологические графики | `python plot_scale.py` |
| Проверить неиспользуемые рисунки | `python audit-images.py --figs ./figs` |
| Открыть ноутбуки | `jupyter notebook` |

## 📚 Индекс конспектов курсов

| Файл | Описание |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Разные лекции |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Библиография Theoretical Minimum |

## 🧪 Упражнения

| Файл | Описание |
|---|---|
| `gr-exercises.tex` | Разбор примеров по [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Использование [pytearcat](https://arxiv.org/abs/2106.15016) для вычисления тензора Эйнштейна для метрики Фридмана-Леметра-Робертсона-Уокера |
| `schwartzchild.ipynb` | Использование pytearcat для вычисления тензора Эйнштейна для метрики Шварцшильда |

Примечание: в более ранней версии README упоминался `schwartzchild.ipnb`; в репозитории файл называется `schwartzchild.ipynb`.

## 🧰 Вспомогательные программы

| Файл | Описание |
|---|---|
| `audit-images.py` | Используется для поиска неиспользуемых файлов изображений и создания `rm.sh` с командами `git rm` |
| `ising1.py` | Исследование нарушения симметрии по лекции 7 с использованием одномерной модели Изинга |
| `Ising.nlogo` | Демонстрация доменных стенок |
| `plot-quartic.py` | Используется для построения «мексиканской шляпы» бозона Хиггса |
| `plot_scale.py` | Используется для построения кривых масштаба вселенной в космологии |
| `plot1.py` | Вспомогательный скрипт визуализации в стиле римановой поверхности (адаптирован из связанного `gist` в исходниках) |
| `plot2.py` | Альтернативная версия скрипта визуализации `plot1.py` |
| `template.py` | Шаблон для Python-программ |
| `tm.wpr` | Проект Wing IDE для вспомогательных файлов |

## 📐 Дополнения к *QFT in a Nutshell*

| Файл | Описание |
|---|---|
| `qft1.tex` | Мотивация и основы |
| `qft2.tex` | Дирак и спиноры |

## ✅ Предварительные требования

- Дистрибутив LaTeX с `lualatex` и инструментами BibTeX.
- `makeglossaries` для документов, использующих глоссарий.
- Python 3 с `numpy` и `matplotlib` для вспомогательных скриптов.
- Jupyter Notebook/Lab для файлов `.ipynb`.
- `pytearcat` для потоков в ноутбуках по космологии и метрике Шварцшильда.
- По желанию: [TexStudio](https://www.texstudio.org/) и [JabRef](https://www.jabref.org/).

## 🧱 Установка

На данный момент файл менеджера пакетов отсутствует (`requirements.txt`, `pyproject.toml` и т.д. не предоставляются), поэтому настройка выполняется вручную.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Если в вашем TeX-дистрибутиве отсутствуют компоненты, установите пакеты для:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 Использование

### 🧪 Компиляция конспектов лекций (LaTeX)

Многие исходники явно указывают LuaLaTeX (`% !TeX program = lualatex`). Общая последовательность сборки:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Для файлов без глоссария можно опустить `makeglossaries`.

### 🧬 Запуск вспомогательных скриптов

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

### 📓 Работа с ноутбуками

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ Конфигурация

Репозиторий намеренно минималистичен и в основном управляется файлами.

- Конвенции путей к рисункам основаны на `figs/` и `\graphicspath{{figs/}}` в файлах TeX.
- Параметры по умолчанию скриптов:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: включает настраиваемые флаги симуляции (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- На данный момент централизованного конфигурационного файла нет.

## 🧭 Примеры

### 🪐 Пример 1: Пересоздание космологических графиков масштаба

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 Пример 2: Проверка и очистка неиспользуемых изображений

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 Пример 3: Сборка заметок Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 Заметки по разработке

- Область: личные, развивающиеся конспекты лекций и вычислительные дополнения.
- Автоматизация сборки намеренно минимальна; команды запускаются вручную.
- `.gitignore` ориентирован на LaTeX и исключает типичные артефакты сборки.
- `figs/` большой; `audit-images.py` полезен для поддержания порядка ссылок на изображения.

## 🛠️ Устранение неполадок

- Ошибки `tikz-feynman`: компилируйте с `lualatex` (рекомендуется в исходниках).
- Отсутствующие элементы/вывод глоссария: запустите `makeglossaries <basename>` между проходами LaTeX.
- Отсутствующие библиографические ссылки: убедитесь, что выполнен `bibtex <basename>` и что `tm.bib` присутствует.
- Ошибки импорта Python (`numpy`, `matplotlib`, `pytearcat`): установите нужные пакеты в активной среде.
- Несоответствие ядра ноутбука: выберите среду, где установлены зависимости.

## 🗺️ Дорожная карта

- Добавить воспроизводимую автоматизацию сборки (например, обёртки `latexmk`/Makefile для каждого документа).
- Добавить зафиксированные метаданные зависимостей Python.
- Заполнить `i18n/` вариантами README на разных языках.
- Уточнить, какие рукописи считаются стабильными/финальными версиями.

## 🤝 Участие

Приветствуются вклады, особенно:

- Исправления опечаток и правок уравнений/обозначений.
- Исправление битых ссылок и чистка ссылок.
- Улучшения сборки и документации.
- Улучшения воспроизводимости рисунков/скриптов.

Предлагаемый рабочий процесс:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 Благодарности

- Леонарду Сусскинду и его коллегам — за лекции *Theoretical Minimum*.
- Среди инструментов, использованных в этом проекте, [TexStudio](https://www.texstudio.org/) и [JabRef](https://www.jabref.org/).

## ⚖️ Лицензия

Этот репозиторий распространяется по лицензии `CC0-1.0`. См. [`LICENSE`](../LICENSE).

- Леонард Сасскинд и соавторы по лекциям *Theoretical Minimum*.
- Инструменты, используемые в этом проекте: [TexStudio](https://www.texstudio.org/) и [JabRef](https://www.jabref.org/).

## ⚖️ Лицензия

Текст лицензии на уровне репозитория приведён в [LICENSE](../LICENSE), в настоящее время это **CC0 1.0 Universal**.

Примечание: в некоторых отдельных исходных файлах содержатся собственные уведомления об авторских правах/лицензиях. Сохраняйте их при повторном использовании кода.


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
