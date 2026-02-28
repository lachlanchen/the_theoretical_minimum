[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# ملاحظاتي لدورات [Theoretical Minimum](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## نظرة عامة

هذا المستودع هو بالأساس مشروع ملاحظات فيزياء يعتمد منهج "الوثيقة أولاً"، ومبني حول مخطوطات LaTeX (`*.tex`) ومرجع ببليوغرافي مشترك (`tm.bib`)، مع سكربتات Python ودفاتر Jupyter داعمة للرسوم والتحقق الرمزي.

## ملاحظات محاضرات مبنية على [Theoretical Minimum](http://theoreticalminimum.com/home) لليونارد سسكايند

**إخلاء مسؤولية** أنشأت هذه الملاحظات لتكون تذكيراً شخصياً لنفسي؛ إذا وجدتها مفيدة فأهلاً بك، وسأقدّر أن تخبرني إذا كنت تستخدمها. وهي _ليست_ بديلاً عن متابعة المحاضرات. حقوق الملكية الفكرية لكل المواد المشتقة من المحاضرات تعود بالطبع إلى الأستاذ سسكايند؛ أما الأخطاء، فهي أخطائي أنا.

تم إعداد الملاحظات باستخدام [TexStudio](https://www.texstudio.org/)، وإدارة المراجع باستخدام [JabRef](https://www.jabref.org/).

## الميزات

- 📚 مخطوطات LaTeX منظّمة حسب المقررات لموضوعات Theoretical Minimum الأساسية.
- 📖 ببليوغرافيا مركزية (`tm.bib`) مشتركة بين المستندات.
- 🖼️ مكتبة كبيرة قابلة لإعادة الاستخدام من الأشكال في `figs/`.
- 🧰 أدوات للمحافظة على نظافة الأشكال وتوليدها (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 ملاحق حسابية في دفاتر Jupyter باستخدام `pytearcat`.
- 🧪 نموذج NetLogo (`Ising.nlogo`) لتصور الجدران المجالّية (domain walls).

## بنية المشروع

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

## بداية سريعة

| الهدف | الأمر/الأوامر |
|---|---|
| ترجمة مخطوطة واحدة | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| إعادة توليد رسوم علم الكونيات | `python plot_scale.py` |
| فحص الأشكال غير المشار إليها | `python audit-images.py --figs ./figs` |
| فتح دفاتر الملاحظات | `jupyter notebook` |

## فهرس ملاحظات المقررات

| الملف | الوصف |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | محاضرات متنوعة |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | الببليوغرافيا الخاصة بـ Theoretical Minimum |

## التمارين

| الملف | الوصف |
|---|---|
| `gr-exercises.tex` | أمثلة محلولة من [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | استخدام [pytearcat](https://arxiv.org/abs/2106.15016) لحساب موتر أينشتاين لمترية Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | استخدام pytearcat لحساب موتر أينشتاين لمترية Schwarzschild |

ملاحظة: أشار نص README سابقاً إلى `schwartzchild.ipnb`؛ الملف الموجود في المستودع هو `schwartzchild.ipynb`.

## البرامج المساعدة

| الملف | الوصف |
|---|---|
| `audit-images.py` | يُستخدم لتحديد ملفات الصور غير المشار إليها وإنشاء `rm.sh` بأوامر `git rm` |
| `ising1.py` | استكشاف كسر التناظر من المحاضرة 7 باستخدام نموذج Ising أحادي البعد |
| `Ising.nlogo` | عرض توضيحي للجدران المجالّية (domain walls) |
| `plot-quartic.py` | يُستخدم لرسم شكل Mexican hat الخاص ببوزون Higgs |
| `plot_scale.py` | يُستخدم لرسم منحنيات معامل التمدد في علم الكونيات |
| `plot1.py` | أداة مساعدة للتصور بأسلوب سطح ريمان (مقتبسة من gist مرتبط في المصدر) |
| `plot2.py` | نسخة بديلة من أداة التصور `plot1.py` |
| `template.py` | قالب لبرامج Python |
| `tm.wpr` | مشروع Wing IDE لملفات المساعدة |

## براهين مكمّلة لكتاب *QFT in a Nutshell*

| الملف | الوصف |
|---|---|
| `qft1.tex` | Motivation and Foundation |
| `qft2.tex` | Dirac and the Spinor |

## المتطلبات المسبقة

- توزيعة LaTeX تتضمن أدوات `lualatex` وBibTeX.
- أداة `makeglossaries` للمستندات التي تستخدم مدخلات المسرد.
- Python 3 مع `numpy` و`matplotlib` للسكربتات المساعدة.
- Jupyter Notebook/Lab لملفات `.ipynb`.
- `pytearcat` لسير عمل دفاتر علم الكونيات/Schwarzschild.
- اختياري: [TexStudio](https://www.texstudio.org/) و[JabRef](https://www.jabref.org/).

## التثبيت

لا يوجد حالياً ملف مدير حزم (`requirements.txt`, `pyproject.toml`, إلخ)، لذلك يتم الإعداد يدوياً.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

إذا كانت توزيعة TeX لديك تفتقد بعض المكوّنات، فقم بتثبيت الحزم الخاصة بـ:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## الاستخدام

### ترجمة ملاحظات المحاضرات (LaTeX)

تحدد العديد من الملفات المصدر LuaLaTeX صراحة (`% !TeX program = lualatex`). تسلسل بناء عام:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

بالنسبة للملفات التي لا تستخدم المسارد، احذف خطوة `makeglossaries`.

### تشغيل السكربتات المساعدة

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

### استخدام الدفاتر

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## الإعداد

هذا المستودع خفيف عمداً ويعتمد في الغالب على تنظيم الملفات.

- اصطلاحات مسار الأشكال تعتمد على `figs/` وعلى `\graphicspath{{figs/}}` داخل ملفات TeX.
- القيم الافتراضية للسكربتات:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: يتضمن خيارات محاكاة قابلة للضبط (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- لا يوجد حالياً ملف إعداد مركزي.

## أمثلة

### المثال 1: إعادة توليد رسوم معامل التمدد في علم الكونيات

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### المثال 2: فحص وتنظيف الصور غير المشار إليها

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### المثال 3: بناء ملاحظات Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## ملاحظات التطوير

- النطاق: ملاحظات محاضرات شخصية ومتطورة باستمرار مع ملاحق حسابية.
- أتمتة البناء محدودة عمداً؛ يتم تشغيل الأوامر يدوياً.
- ملف `.gitignore` يركز على LaTeX ويستثني نواتج البناء الشائعة.
- مجلد `figs/` كبير؛ أداة `audit-images.py` مفيدة للحفاظ على تنظيم مراجع الصور.

## استكشاف الأخطاء وإصلاحها

- أخطاء `tikz-feynman`: قم بالترجمة باستخدام `lualatex` (كما توصي به ملفات المصدر).
- غياب مدخلات/مخرجات المسرد: شغّل `makeglossaries <basename>` بين تمريرات LaTeX.
- غياب مراجع الببليوغرافيا: تأكد من تشغيل `bibtex <basename>` ومن وجود `tm.bib`.
- أخطاء استيراد Python (`numpy`, `matplotlib`, `pytearcat`): ثبّت الحزم المطلوبة في البيئة النشطة.
- عدم تطابق نواة الدفتر: اختر البيئة التي ثُبّتت فيها الاعتماديات.

## خارطة الطريق

- إضافة أتمتة بناء قابلة لإعادة الإنتاج (مثلاً: أغلفة `latexmk`/Makefile لكل مخطوطة).
- إضافة بيانات اعتماديات Python مُثبتة الإصدارات.
- تعبئة `i18n/` بنسخ README مترجمة.
- توضيح المخطوطات التي تُعد لقطات مستقرة/نهائية.

## المساهمة

المساهمات مرحب بها، خاصة:

- تصحيحات الأخطاء المطبعية وأخطاء المعادلات/الترميز.
- إصلاح الروابط المكسورة وتنظيف المراجع.
- تحسينات البناء/التوثيق.
- تحسين قابلية إعادة إنتاج الأشكال/السكربتات.

سير عمل مقترح:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## الشكر والتقدير

- ليونارد سسكايند والمتعاونون معه على محاضرات *Theoretical Minimum*.
- من الأدوات المستخدمة في هذا المشروع: [TexStudio](https://www.texstudio.org/) و[JabRef](https://www.jabref.org/).

## الترخيص

نص الترخيص على مستوى المستودع موجود في [LICENSE](../LICENSE)، وهو حالياً **CC0 1.0 Universal**.

ملاحظة: تتضمن بعض ملفات المصدر الفردية ترويسات حقوق نشر/ترخيص خاصة بها. حافظ على هذه الإشعارات عند إعادة استخدام الكود.
