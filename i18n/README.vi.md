[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# Ghi chú của tôi cho [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## Tổng quan

Kho lưu trữ này chủ yếu là một dự án ghi chú vật lý theo hướng tài liệu trước tiên, được xây dựng quanh các bản thảo LaTeX (`*.tex`) và một kho tài liệu tham khảo dùng chung (`tm.bib`), với các script Python và notebook hỗ trợ tạo hình và kiểm tra ký hiệu.

## 🎓 Ghi chú bài giảng từ [Theoretical Minimum](http://theoreticalminimum.com/home) của Leonard Susskind

**Lưu ý** Tôi đã tạo các ghi chú này như một tài liệu nhắc lại cho riêng tôi; nếu bạn thấy hữu ích thì mừng lắm, và tôi rất trân trọng nếu bạn cho tôi biết khi bạn sử dụng chúng. Chúng không được thiết kế để thay thế cho việc theo dõi trực tiếp các bài giảng. Quyền sở hữu trí tuệ cho mọi nội dung lấy từ các bài giảng thuộc về Giáo sư Susskind; mọi lỗi sót, nếu có, là trách nhiệm của tôi.

Các ghi chú này được tạo bằng [TexStudio](https://www.texstudio.org/), và thư mục tham khảo bởi [JabRef](https://www.jabref.org/).

## ✨ Tính năng

- 📚 Các bản thảo LaTeX theo từng khóa học cho các chủ đề cốt lõi của Theoretical Minimum.
- 📖 Kho tài liệu tham khảo trung tâm (`tm.bib`) được dùng chung giữa các tài liệu.
- 🖼️ Thư viện hình minh họa lớn có thể tái sử dụng trong `figs/`.
- 🧰 Tiện ích chăm sóc và tạo hình ảnh (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Tài liệu bổ trợ tính toán trong các notebook Jupyter dùng `pytearcat`.
- 🧪 Mô hình NetLogo (`Ising.nlogo`) để trực quan hóa domain wall.

## 🗂️ Cấu trúc dự án

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

## 🚀 Bắt đầu nhanh

| Mục tiêu | Lệnh |
|---|---|
| Biên dịch một bản thảo | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Tạo lại đồ thị vũ trụ học | `python plot_scale.py` |
| Kiểm tra hình không được tham chiếu | `python audit-images.py --figs ./figs` |
| Mở notebook | `jupyter notebook` |

## 📚 Chỉ mục ghi chú theo khóa học

| Tệp | Mô tả |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Các bài giảng bổ sung |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Tài liệu tham khảo của Theoretical Minimum |

## 🧪 Bài tập

| Tệp | Mô tả |
|---|---|
| `gr-exercises.tex` | Bài tập có lời giải từ [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Dùng [pytearcat](https://arxiv.org/abs/2106.15016) để tính tensor Einstein cho metric Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | Dùng pytearcat để tính tensor Einstein cho metric Schwarzschild |

Lưu ý: bản README trước đây đề cập `schwartzchild.ipnb`; tệp trong repository là `schwartzchild.ipynb`.

## 🧰 Chương trình hỗ trợ

| Tệp | Mô tả |
|---|---|
| `audit-images.py` | Dùng để nhận diện các tệp hình chưa được tham chiếu và sinh `rm.sh` với lệnh `git rm` |
| `ising1.py` | Khám phá sự vỡ đối xứng từ bài giảng 7, dùng mô hình Ising một chiều |
| `Ising.nlogo` | Minh họa domain walls |
| `plot-quartic.py` | Dùng để vẽ Mexican hat cho boson Higgs |
| `plot_scale.py` | Dùng để vẽ các đường cong tham số tỉ lệ vũ trụ học |
| `plot1.py` | Trợ giúp trực quan hóa kiểu Riemann surface (được điều chỉnh từ gist liên kết trong mã nguồn) |
| `plot2.py` | Phiên bản thay thế của trình trực quan `plot1.py` |
| `template.py` | Mẫu cho các chương trình Python |
| `tm.wpr` | Dự án Wing IDE cho các tệp hỗ trợ |

## 🧪 Chứng minh bổ sung cho *QFT in a Nutshell*

| Tệp | Mô tả |
|---|---|
| `qft1.tex` | Động lực và nền tảng |
| `qft2.tex` | Dirac và Spinor |

## ✅ Điều kiện tiên quyết

- Một bản phân phối LaTeX có `lualatex` và các công cụ BibTeX.
- `makeglossaries` cho các tài liệu sử dụng mục glossary.
- Python 3 cùng `numpy` và `matplotlib` cho script hỗ trợ.
- Jupyter Notebook/Lab cho các tệp `.ipynb`.
- `pytearcat` cho các notebook cosmology/Schwarzschild.
- Tùy chọn: [TexStudio](https://www.texstudio.org/) và [JabRef](https://www.jabref.org/).

## 🧱 Cài đặt

Hiện chưa có file quản lý gói nào được cung cấp (`requirements.txt`, `pyproject.toml`, ...), nên việc cài đặt được thực hiện thủ công.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Tùy chọn môi trường Python
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Nếu bản phân phối TeX của bạn thiếu thành phần, cài thêm các gói:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 Cách sử dụng

### 🧪 Biên dịch ghi chú bài giảng (LaTeX)

Nhiều nguồn chỉ định rõ LuaLaTeX (`% !TeX program = lualatex`). Một quy trình build tổng quát:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # nếu tệp có bật glossary
lualatex gr.tex
lualatex gr.tex
```

Với các tệp không dùng glossaries, bỏ `makeglossaries` đi.

### 🧬 Chạy các script hỗ trợ

```bash
# Kiểm tra các hình chưa được tham chiếu trong ./figs và sinh rm.sh
python audit-images.py --figs ./figs

# Mô phỏng Ising 1 chiều (tạo hình trong ./figs)
python ising1.py --m 100 --n 1000 --N 25 --T 0.001 --cool 0.01 --figs ./figs

# Các script vẽ hình
python plot-quartic.py
python plot_scale.py
python plot1.py
python plot2.py
```

### 📓 Dùng notebook

```bash
jupyter notebook
# Mở notebooks/cosmo.ipynb hoặc notebooks/schwartzchild.ipynb
```

## 🛠️ Cấu hình

Kho lưu trữ này được giữ gọn nhẹ có chủ đích và chủ yếu điều khiển theo tệp.

- Quy ước đường dẫn hình dựa trên `figs/` và `\graphicspath{{figs/}}` trong các tệp TeX.
- Mặc định script:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: gồm các cờ mô phỏng có thể chỉnh (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Hiện chưa có file cấu hình trung tâm.

## 🧭 Ví dụ

### 🪐 Ví dụ 1: Tạo lại đồ thị scale-factor của vũ trụ

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 Ví dụ 2: Kiểm tra và dọn dẹp hình chưa được tham chiếu

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 Ví dụ 3: Biên dịch ghi chú Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 Ghi chú phát triển

- Phạm vi: ghi chú bài giảng cá nhân, liên tục cập nhật và tài liệu tính toán bổ sung.
- Tự động hóa build được giữ tối giản có chủ ý; các lệnh thường chạy thủ công.
- `.gitignore` tập trung cho LaTeX và loại trừ các artefact build thông thường.
- `figs/` khá lớn; `audit-images.py` hữu ích để giữ tham chiếu hình ảnh gọn gàng.

## 🛠️ Khắc phục sự cố

- Lỗi `tikz-feynman`: biên dịch bằng `lualatex` (khuyến nghị trong các tệp nguồn).
- Thiếu mục/đầu ra glossary: chạy `makeglossaries <basename>` giữa các lượt LaTeX.
- Thiếu tham chiếu tài liệu: chắc chắn đã chạy `bibtex <basename>` và có `tm.bib`.
- Lỗi import Python (`numpy`, `matplotlib`, `pytearcat`): cài gói cần thiết trong môi trường đang hoạt động.
- Kernel notebook không khớp: chọn đúng môi trường đã cài đủ dependency.

## 🗺️ Lộ trình

- Thêm tự động hóa build có thể tái lập (ví dụ: wrapper `latexmk`/Makefile riêng cho từng bản thảo).
- Thêm metadata phụ thuộc Python có phiên bản cố định.
- Bổ sung đầy đủ `i18n/` với các bản README đã dịch.
- Làm rõ bản thảo nào được xem là bản ổn định/hữu dụng cuối cùng.

## 🤝 Đóng góp

Đóng góp rất được hoan nghênh, đặc biệt:

- Sửa lỗi chính tả và lỗi phương trình/ký hiệu.
- Sửa đường dẫn hỏng và làm sạch tham chiếu.
- Cải tiến build và tài liệu.
- Cải thiện khả năng tái lập cho hình và script.

Quy trình gợi ý:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 Lời cảm ơn

Cảm ơn các nhà sáng tạo và bảo trì các công cụ được dùng tại đây, đặc biệt là LaTeX, LuaLaTeX, Matplotlib, Jupyter và pytearcat.

## ⚖️ Giấy phép

Repository này phát hành theo giấy phép `CC0-1.0`. Xem [`LICENSE`](../LICENSE).

- Leonard Susskind và cộng sự cho loạt bài giảng *Theoretical Minimum*.
- Các công cụ dùng trong dự án bao gồm [TexStudio](https://www.texstudio.org/) và [JabRef](https://www.jabref.org/).

## ⚖️ Giấy phép

Văn bản giấy phép cấp repository nằm trong [LICENSE](../LICENSE), hiện là **CC0 1.0 Universal**.

Lưu ý: một số tệp nguồn riêng lẻ có tiêu đề bản quyền/giấy phép riêng. Hãy giữ nguyên các thông báo đó khi tái sử dụng mã.


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
