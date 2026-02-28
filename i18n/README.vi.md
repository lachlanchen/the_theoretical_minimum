[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# Ghi chú của tôi cho [Theoretical Minimum Courses](http://theoreticalminimum.com/)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## Tổng quan

Repository này chủ yếu là một dự án ghi chú vật lý theo hướng tài liệu, được xây dựng xoay quanh các bản thảo LaTeX (`*.tex`) và một thư mục tài liệu tham khảo dùng chung (`tm.bib`), kèm các script Python và notebook để hỗ trợ hình vẽ và kiểm tra ký hiệu.

## Ghi chú bài giảng dựa trên [Theoretical Minimum](http://theoreticalminimum.com/home) của Leonard Susskind

**Lưu ý** Tôi tạo các ghi chú này như một aide-mémoire cho mục đích cá nhân; nếu bạn thấy hữu ích thì cứ sử dụng, nhưng tôi sẽ rất cảm kích nếu bạn cho tôi biết bạn đang dùng chúng. Chúng _không_ nhằm thay thế việc theo dõi bài giảng. Quyền sở hữu trí tuệ đối với toàn bộ nội dung bắt nguồn từ các bài giảng dĩ nhiên thuộc về Giáo sư Susskind; còn mọi sai sót thì là của tôi.

Các ghi chú được tạo bằng [TexStudio](https://www.texstudio.org/), và thư mục tài liệu tham khảo bằng [JabRef](https://www.jabref.org/).

## Tính năng

- 📚 Bản thảo LaTeX được tổ chức theo khóa học cho các chủ đề cốt lõi của Theoretical Minimum.
- 📖 Thư mục tài liệu tham khảo trung tâm (`tm.bib`) dùng chung giữa các tài liệu.
- 🖼️ Thư viện hình lớn có thể tái sử dụng trong `figs/`.
- 🧰 Tiện ích dọn dẹp và tạo hình (`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Phần bổ trợ tính toán trong notebook Jupyter dùng `pytearcat`.
- 🧪 Mô hình NetLogo (`Ising.nlogo`) để trực quan hóa domain wall.

## Cấu trúc dự án

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

## Bắt đầu nhanh

| Mục tiêu | Lệnh |
|---|---|
| Biên dịch một bản thảo | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| Tạo lại đồ thị vũ trụ học | `python plot_scale.py` |
| Kiểm tra hình không được tham chiếu | `python audit-images.py --figs ./figs` |
| Mở notebook | `jupyter notebook` |

## Chỉ mục ghi chú khóa học

| Tệp | Mô tả |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | Bài giảng tạp |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Tài liệu tham khảo cho Theoretical Minimum |

## Bài tập

| Tệp | Mô tả |
|---|---|
| `gr-exercises.tex` | Ví dụ đã giải từ [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `cosmo.ipynb` | Dùng [pytearcat](https://arxiv.org/abs/2106.15016) để tính tensor Einstein cho metric Friedmann-Lemaître-Robertson-Walker |
| `schwartzchild.ipynb` | Dùng pytearcat để tính tensor Einstein cho metric Schwarzschild |

Lưu ý: văn bản README trước đây có nhắc tới `schwartzchild.ipnb`; tệp trong repository là `schwartzchild.ipynb`.

## Chương trình hỗ trợ

| Tệp | Mô tả |
|---|---|
| `audit-images.py` | Dùng để xác định tệp hình không được tham chiếu và tạo `rm.sh` với các lệnh `git rm` |
| `ising1.py` | Khảo sát phá vỡ đối xứng từ bài giảng 7, dùng mô hình Ising 1 chiều |
| `Ising.nlogo` | Minh họa domain wall |
| `plot-quartic.py` | Dùng để vẽ thế Mexican hat cho boson Higgs |
| `plot_scale.py` | Dùng để vẽ các đường cong tham số tỉ lệ trong vũ trụ học |
| `plot1.py` | Trợ giúp trực quan kiểu Riemann surface (điều chỉnh từ gist được liên kết trong mã nguồn) |
| `plot2.py` | Phiên bản thay thế của trợ giúp trực quan `plot1.py` |
| `template.py` | Mẫu cho chương trình Python |
| `tm.wpr` | Dự án Wing IDE cho các tệp hỗ trợ |

## Các chứng minh bổ sung cho *QFT in a Nutshell*

| Tệp | Mô tả |
|---|---|
| `qft1.tex` | Động cơ và nền tảng |
| `qft2.tex` | Dirac và spinor |

## Điều kiện tiên quyết

- Một bản phân phối LaTeX có `lualatex` và bộ công cụ BibTeX.
- `makeglossaries` cho các tài liệu có dùng mục glossary.
- Python 3 với `numpy` và `matplotlib` cho các script hỗ trợ.
- Jupyter Notebook/Lab cho các tệp `.ipynb`.
- `pytearcat` cho luồng làm việc notebook cosmology/Schwarzschild.
- Tùy chọn: [TexStudio](https://www.texstudio.org/) và [JabRef](https://www.jabref.org/).

## Cài đặt

Hiện chưa có tệp quản lý gói (`requirements.txt`, `pyproject.toml`, v.v.), nên thiết lập là thủ công.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

Nếu bản phân phối TeX của bạn thiếu thành phần, hãy cài các gói cho:

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## Cách sử dụng

### Biên dịch ghi chú bài giảng (LaTeX)

Nhiều tệp nguồn chỉ định rõ LuaLaTeX (`% !TeX program = lualatex`). Một chuỗi build tổng quát:

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

Với các tệp không dùng glossary, bỏ `makeglossaries`.

### Chạy script hỗ trợ

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

### Dùng notebook

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## Cấu hình

Repository này được giữ gọn nhẹ có chủ đích và chủ yếu vận hành theo tệp.

- Quy ước đường dẫn hình dựa trên `figs/` và `\graphicspath{{figs/}}` trong các tệp TeX.
- Giá trị mặc định của script:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: bao gồm các cờ mô phỏng có thể tinh chỉnh (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- Hiện không có tệp cấu hình tập trung.

## Ví dụ

### Ví dụ 1: tạo lại đồ thị hệ số tỉ lệ vũ trụ học

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### Ví dụ 2: kiểm tra và dọn hình không được tham chiếu

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### Ví dụ 3: build ghi chú Advanced Quantum Mechanics

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## Ghi chú phát triển

- Phạm vi: ghi chú bài giảng cá nhân đang được cập nhật và các phần bổ trợ tính toán.
- Tự động hóa build được giữ tối giản có chủ đích; các lệnh được chạy thủ công.
- `.gitignore` tập trung cho LaTeX và loại trừ các tạo phẩm build phổ biến.
- `figs/` khá lớn; `audit-images.py` hữu ích để giữ tham chiếu hình gọn gàng.

## Khắc phục sự cố

- Lỗi `tikz-feynman`: biên dịch bằng `lualatex` (được các tệp nguồn khuyến nghị).
- Thiếu mục/kết quả glossary: chạy `makeglossaries <basename>` giữa các lượt LaTeX.
- Thiếu tham chiếu tài liệu: đảm bảo đã chạy `bibtex <basename>` và có `tm.bib`.
- Lỗi import Python (`numpy`, `matplotlib`, `pytearcat`): cài các gói cần thiết trong môi trường đang kích hoạt.
- Kernel notebook không khớp: chọn môi trường nơi các phụ thuộc đã được cài.

## Lộ trình

- Thêm tự động hóa build có thể tái lập (ví dụ: wrapper `latexmk`/Makefile theo từng bản thảo).
- Thêm metadata phụ thuộc Python được ghim phiên bản.
- Điền đầy `i18n/` với các biến thể README đã dịch.
- Làm rõ bản thảo nào được xem là ổn định/phiên bản cuối.

## Đóng góp

Rất hoan nghênh đóng góp, đặc biệt là:

- Sửa lỗi chính tả và lỗi phương trình/ký hiệu.
- Sửa liên kết hỏng và dọn tài liệu tham khảo.
- Cải thiện build/tài liệu.
- Cải thiện khả năng tái lập cho hình và script.

Quy trình đề xuất:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## Lời cảm ơn

- Leonard Susskind và các cộng tác viên cho loạt bài giảng *Theoretical Minimum*.
- Các công cụ dùng trong dự án gồm [TexStudio](https://www.texstudio.org/) và [JabRef](https://www.jabref.org/).

## Giấy phép

Văn bản giấy phép ở cấp repository nằm trong [LICENSE](../LICENSE), hiện là **CC0 1.0 Universal**.

Lưu ý: một số tệp nguồn riêng lẻ có tiêu đề copyright/giấy phép riêng. Hãy giữ nguyên các thông báo đó khi tái sử dụng mã.
