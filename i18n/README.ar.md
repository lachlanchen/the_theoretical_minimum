[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# ملاحظاتي لدورات [Theoretical Minimum](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 نظرة عامة

هذا المستودع هو في المقام الأول مشروع ملاحظات فيزياء يعتمد على نهج "الوثيقة أولاً" ومبني حول مخطوطات LaTeX (`*.tex`) ومكتبة مرجع مشتركة (`tm.bib`)، مع سكربتات Python ودفاتر Jupyter المساعدة في الرسوم البيانية والتحقق الرمزي.

## 🎓 ملاحظات المحاضرات من سلسلة [Theoretical Minimum](http://theoreticalminimum.com/home) لليونارد ساسكيند

**إخلاء مسؤولية** أنشأت هذه الملاحظات كمذكرة مساعدة للاستخدام الشخصي؛ إذا كانت مفيدة لك فأهلاً بك، وسأكون ممتنًا إذا أخبرتني بأنك تستخدمها. وهي ليست بديلاً عن الاستماع إلى المحاضرات. الملكية الفكرية لكل مادة مشتقة من المحاضرات تعود بالطبع للبروفيسور ساسكيند؛ أي أخطاء إن وُجدت فهي من عندي.

تم إنشاء الملاحظات باستخدام [TexStudio](https://www.texstudio.org/)، وإعداد الببليوغرافيا باستخدام [JabRef](https://www.jabref.org/).

## ✨ المزايا

- 📚 مخطوطات LaTeX منظمة حسب المقرر لموضوعات Theoretical Minimum الأساسية.
- 📖 مرجع ببليوغرافي مركزي (`tm.bib`) يُشارك بين المستندات.
- 🖼️ مكتبة كبيرة للرسوميات قابلة لإعادة الاستخدام في `figs/`.
- 🧰 أدوات لتنظيف الرسوميات وتوليدها (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 ملحقات حسابية في دفاتر Jupyter باستخدام `pytearcat`.
- 🧪 نموذج NetLogo (`Ising.nlogo`) لتصور جدران المجال.

## 🗂️ هيكل المشروع

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

## 🚀 البداية السريعة

| الهدف | الأوامر |
|---|---|
| ترجمة مخطوطة واحدة | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| إعادة توليد رسوم علم الكونيات | `python plot_scale.py` |
| تدقيق الرسوم غير المرجعية | `python audit-images.py --figs ./figs` |
| فتح دفاتر Jupyter | `jupyter notebook` |

## 📚 فهرس ملاحظات المقررات

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

## 🧪 التمارين

| الملف | الوصف |
|---|---|
| `gr-exercises.tex` | أمثلة محلولة من [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | استخدام [pytearcat](https://arxiv.org/abs/2106.15016) لحساب موتر أينشتاين لمقياس Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | استخدام pytearcat لحساب موتر أينشتاين لمقياس Schwarzschild |

ملاحظة: النص السابق في README أشار إلى `schwartzchild.ipnb`؛ الملف الفعلي في المستودع هو `schwartzchild.ipynb`.

## 🧰 البرامج المساعدة

| الملف | الوصف |
|---|---|
| `audit-images.py` | يُستخدم لتحديد ملفات الصور غير المرجعية وإنشاء `rm.sh` يتضمن أوامر `git rm` |
| `ising1.py` | استكشاف كسر التناظر من المحاضرة السابعة باستخدام نموذج Ising أحادي البعد |
| `Ising.nlogo` | عرض توضيحي لجدران المجال |
| `plot-quartic.py` | يستخدم لرسم شكل "القبعة المكسيكية" لهiggs boson |
| `plot_scale.py` | يستخدم لرسم منحنيات معامل التوسع في علم الكونيات |
| `plot1.py` | أداة مساعدة للتصور بنمط سطح ريمان (مستوحاة من gist في المصدر) |
| `plot2.py` | نسخة بديلة لأداة التصور `plot1.py` |
| `template.py` | قالب لبرامج Python |
| `tm.wpr` | مشروع Wing IDE لملفات المساعدة |

## 📐 براهين مكمّلة لكتاب *QFT in a Nutshell*

| الملف | الوصف |
|---|---|
| `qft1.tex` | الدافع والأساسيات |
| `qft2.tex` | Dirac والـ Spinor |

## ✅ المتطلبات المسبقة

- توزيعة LaTeX تتضمن `lualatex` وأدوات BibTeX.
- `makeglossaries` للمستندات التي تستخدم مدخلات مسرد.
- Python 3 مع `numpy` و`matplotlib` للسكربتات المساعدة.
- Jupyter Notebook/Lab لملفات `.ipynb`.
- `pytearcat` لسير عمل دفاتر علم الكونيات/Schwarzschild.
- اختياري: [TexStudio](https://www.texstudio.org/) و[JabRef](https://www.jabref.org/).

## 🧱 التثبيت

لا يوجد ملف مدير حزم حاليًا (`requirements.txt` و`pyproject.toml` وغير ذلك غير موجودة)، لذلك يتم الإعداد يدويًا.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

إذا كانت توزيعة TeX لديك تفتقد مكونات معيّنة، ثبّت الحزم:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 الاستخدام

### 🧪 ترجمة ملاحظات المحاضرات (LaTeX)

تحدد العديد من الملفات المصدر LuaLaTeX صراحةً (`% !TeX program = lualatex`). تسلسل بناء عام هو:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

بالنسبة للملفات التي لا تستخدم المسارد، احذف خطوة `makeglossaries`.

### 🧬 تشغيل السكربتات المساعدة

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

### 📓 استخدام دفاتر Jupyter

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ الإعداد

هذا المستودع خفيف الوزن عمدًا ومعتمد أساسًا على الملفات.

- تتبع مسارات الرسوميات يعتمد على `figs/` وعلى `\graphicspath{{figs/}}` في ملفات TeX.
- إعدادات افتراضية للسكربتات:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: تشمل خيارات ضبط للمحاكاة (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- لا يوجد حتى الآن ملف إعداد مركزي.

## 🧭 أمثلة

### 🪐 المثال 1: إعادة توليد رسوم عامل المقياس في علم الكونيات

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 المثال 2: فحص وتنظيف الصور غير المرجعية

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 المثال 3: بناء ملاحظات Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 ملاحظات التطوير

- النطاق: ملاحظات محاضرات شخصية تتطور باستمرار.
- أتمتة البناء مقصودة لتكون بسيطة؛ تُشغَّل الأوامر يدويًا.
- ملف `.gitignore` موجه إلى LaTeX ويستبعد مخلفات البناء الشائعة.
- مجلد `figs/` كبير؛ ولذلك يكون `audit-images.py` مفيدًا لتنظيف مراجع الصور.

## 🛠️ استكشاف الأخطاء وإصلاحها

- أخطاء `tikz-feynman`: اجعل الترجمة باستخدام `lualatex` (موصى به في ملفات المصدر).
- نقص مداخل/مخرجات المسرد: شغّل `makeglossaries <basename>` بين تمريرتي LaTeX.
- مراجع ببليوغرافية مفقودة: تأكد من تشغيل `bibtex <basename>` وتواجد `tm.bib`.
- أخطاء استيراد Python (`numpy`, `matplotlib`, `pytearcat`): ثبّت الحزم المطلوبة في البيئة النشطة.
- عدم تطابق نواة الدفتر: اختر البيئة التي ثُبّتت فيها الاعتماديات.

## 🗺️ خارطة الطريق

- إضافة أتمتة بناء قابلة لإعادة الإنتاج (على سبيل المثال: أغلفة `latexmk`/Makefile لكل مخطوطة).
- إضافة بيانات اعتماديات Python مثبتة النسخ.
- ملء `i18n/` بنسخ README مترجمة.
- توضيح أي المخطوطات تُعتبر لقطات مستقرة/نهائية.

## 🤝 المساهمة

المساهمات مرحب بها، خصوصًا:

- تصحيحات مطبعية وأخطاء المعادلات/الترميز.
- إصلاح الروابط المكسورة وتنظيف المراجع.
- تحسينات البناء/التوثيق.
- تحسينات قابلية إعادة إنتاج الرسوم/السكربتات.

النهج المقترح:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 الشكر والتقدير

- أستاذ ليونارد ساسكيند والمتعاونون على محاضرات *Theoretical Minimum*.
- الأدوات المستخدمة في هذا المشروع تشمل [TexStudio](https://www.texstudio.org/) و[JabRef](https://www.jabref.org/).

## ⚖️ الترخيص

هذا المستودع مرخّص تحت رخصة `CC0-1.0`. راجع [LICENSE](../LICENSE).

- أستاذ ليونارد ساسكيند والمتعاونون على محاضرات *Theoretical Minimum*.
- الأدوات المستخدمة في هذا المشروع تشمل [TexStudio](https://www.texstudio.org/) و[JabRef](https://www.jabref.org/).

## ⚖️ الترخيص

نص الترخيص على مستوى المستودع موجود في [LICENSE](../LICENSE)، وهو حاليًا **CC0 1.0 Universal**.

ملاحظة: تتضمن بعض ملفات المصدر الفردية ترويسات حقوق نشر/ترخيص خاصة بها. احتفظ بهذه الإشعارات عند إعادة استخدام الكود.


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
