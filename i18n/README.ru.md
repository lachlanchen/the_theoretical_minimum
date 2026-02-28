[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# Мои заметки по [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## Обзор

Этот репозиторий в первую очередь представляет собой документо-ориентированный проект с конспектами по физике, построенный вокруг рукописей LaTeX (`*.tex`) и общей библиографии (`tm.bib`), с дополнительными Python-скриптами и ноутбуками для построения графики и символических проверок.

## Конспекты лекций по [Theoretical Minimum](http://theoreticalminimum.com/home) Леонарда Сасскинда

**Отказ от ответственности** Я сделал эти заметки как aide-mémoire для собственного использования; если они окажутся вам полезны, я буду рад, но прошу сообщить мне, если вы ими пользуетесь. Они _не_ предназначены как замена прослушиванию лекций. Интеллектуальные права на все материалы, производные от лекций, разумеется, принадлежат профессору Сасскинду; любые ошибки, однако, мои.

Заметки были подготовлены в [TexStudio](https://www.texstudio.org/), а библиография — в [JabRef](https://www.jabref.org/).

## Возможности

- 📚 Рукописи LaTeX, организованные по курсам для ключевых тем Theoretical Minimum.
- 📖 Центральная библиография (`tm.bib`), общая для нескольких документов.
- 🖼️ Большая переиспользуемая библиотека рисунков в `figs/`.
- 🧰 Утилиты для поддержания порядка в рисунках и их генерации (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Вычислительные дополнения в Jupyter-ноутбуках с использованием `pytearcat`.
- 🧪 Модель NetLogo (`Ising.nlogo`) для визуализации доменных стенок.

## Структура проекта

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

## Быстрый старт

| Цель | Команда(ы) |
|---|---|
| Скомпилировать один документ | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Перегенерировать графики по космологии | `python plot_scale.py` |
| Проверить неиспользуемые рисунки | `python audit-images.py --figs ./figs` |
| Открыть ноутбуки | `jupyter notebook` |

## Индекс конспектов курсов

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

## Упражнения

| Файл | Описание |
|---|---|
| `gr-exercises.tex` | Разобранные примеры из [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Использование [pytearcat](https://arxiv.org/abs/2106.15016) для вычисления тензора Эйнштейна для метрики Фридмана-Леметра-Робертсона-Уокера |
| `schwartzchild.ipynb` | Использование pytearcat для вычисления тензора Эйнштейна для метрики Шварцшильда |

Примечание: в более раннем тексте README упоминалось `schwartzchild.ipnb`; в репозитории файл называется `schwartzchild.ipynb`.

## Вспомогательные программы

| Файл | Описание |
|---|---|
| `audit-images.py` | Используется для поиска неиспользуемых файлов изображений и генерации `rm.sh` с командами `git rm` |
| `ising1.py` | Исследование нарушенной симметрии из лекции 7 с использованием одномерной модели Изинга |
| `Ising.nlogo` | Демонстрация доменных стенок |
| `plot-quartic.py` | Используется для построения «мексиканской шляпы» для бозона Хиггса |
| `plot_scale.py` | Используется для построения кривых параметра масштаба в космологии |
| `plot1.py` | Вспомогательный скрипт визуализации в стиле римановой поверхности (адаптирован из связанного gist в исходнике) |
| `plot2.py` | Альтернативная версия визуализации `plot1.py` |
| `template.py` | Шаблон для Python-программ |
| `tm.wpr` | Проект Wing IDE для вспомогательных файлов |

## Доказательства в дополнение к *QFT in a Nutshell*

| Файл | Описание |
|---|---|
| `qft1.tex` | Мотивация и основы |
| `qft2.tex` | Дирак и спинор |

## Предварительные требования

- Дистрибутив LaTeX с инструментами `lualatex` и BibTeX.
- `makeglossaries` для документов, использующих записи глоссария.
- Python 3 с `numpy` и `matplotlib` для вспомогательных скриптов.
- Jupyter Notebook/Lab для файлов `.ipynb`.
- `pytearcat` для рабочих процессов в ноутбуках по космологии/Шварцшильду.
- Опционально: [TexStudio](https://www.texstudio.org/) и [JabRef](https://www.jabref.org/).

## Установка

На данный момент не предоставлен файл менеджера пакетов (`requirements.txt`, `pyproject.toml` и т. п. отсутствуют), поэтому настройка выполняется вручную.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Если в вашем TeX-дистрибутиве отсутствуют нужные компоненты, установите пакеты для:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## Использование

### Компиляция конспектов лекций (LaTeX)

Во многих исходниках явно указан LuaLaTeX (`% !TeX program = lualatex`). Общая последовательность сборки:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Для файлов, не использующих глоссарии, пропустите `makeglossaries`.

### Запуск вспомогательных скриптов

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

### Использование ноутбуков

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## Конфигурация

Этот репозиторий намеренно остаётся лёгким и в основном управляется файлами.

- Соглашения о путях к рисункам основаны на `figs/` и `\graphicspath{{figs/}}` в TeX-файлах.
- Значения по умолчанию для скриптов:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: включает настраиваемые флаги симуляции (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Централизованного конфигурационного файла пока нет.

## Примеры

### Пример 1: перегенерация графиков масштабного фактора в космологии

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### Пример 2: аудит и очистка неиспользуемых изображений

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### Пример 3: сборка конспекта Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## Заметки по разработке

- Область проекта: личные, развивающиеся конспекты лекций и вычислительные дополнения.
- Автоматизация сборки намеренно минимальна; команды запускаются вручную.
- `.gitignore` ориентирован на LaTeX и исключает типичные артефакты сборки.
- `figs/` содержит много данных; `audit-images.py` полезен для поддержания порядка в ссылках на изображения.

## Устранение неполадок

- Ошибки `tikz-feynman`: компилируйте с `lualatex` (рекомендуется исходными файлами).
- Отсутствуют элементы/вывод глоссария: запускайте `makeglossaries <basename>` между проходами LaTeX.
- Отсутствуют ссылки на библиографию: убедитесь, что выполнен `bibtex <basename>` и присутствует `tm.bib`.
- Ошибки импорта Python (`numpy`, `matplotlib`, `pytearcat`): установите нужные пакеты в активное окружение.
- Несовпадение ядра ноутбука: выберите окружение, где установлены зависимости.

## План развития

- Добавить воспроизводимую автоматизацию сборки (например, обёртки `latexmk`/Makefile для каждого документа).
- Добавить фиксированные метаданные зависимостей Python.
- Заполнить `i18n/` переведёнными вариантами README.
- Уточнить, какие рукописи считаются стабильными/финальными снимками.

## Вклад

Вклады приветствуются, особенно:

- Исправления опечаток и поправки в уравнениях/обозначениях.
- Исправление битых ссылок и очистка ссылок на источники.
- Улучшения сборки/документации.
- Улучшения воспроизводимости для рисунков/скриптов.

Рекомендуемый рабочий процесс:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## Благодарности

- Леонарду Сасскинду и его соавторам — за лекции *Theoretical Minimum*.
- Среди инструментов, использованных в этом проекте: [TexStudio](https://www.texstudio.org/) и [JabRef](https://www.jabref.org/).

## Лицензия

Текст лицензии на уровне репозитория приведён в [LICENSE](../LICENSE), сейчас это **CC0 1.0 Universal**.

Примечание: некоторые отдельные исходные файлы содержат собственные заголовки об авторских правах/лицензировании. Сохраняйте эти уведомления при повторном использовании кода.
