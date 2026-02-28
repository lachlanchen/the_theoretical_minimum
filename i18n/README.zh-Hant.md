[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# 我為 [Theoretical Minimum Courses](http://theoreticalminimum.com/) 所寫的筆記

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 概覽

此專案主要是以文件為優先的物理筆記專案，核心為 LaTeX 手稿（`*.tex`）與共用書目資料庫（`tm.bib`），並輔以用於繪圖與符號檢查的 Python 腳本與 notebooks。

## 🎓 來自 Leonard Susskind 的 [Theoretical Minimum](http://theoreticalminimum.com/home) 課程筆記

**免責聲明**：我建立這些筆記是為了個人使用的備忘；若你覺得有幫助，歡迎使用，但若你確實使用，請讓我知道。這些筆記**不**作為聆聽課程的替代教材。從課程內容衍生的智慧財產權當然歸 Susskind 教授所有；然而任何錯誤都由我本人負責。

這些筆記使用 [TexStudio](https://www.texstudio.org/) 製作，書目則由 [JabRef](https://www.jabref.org/) 管理。

## ✨ 功能

- 📚 以課程主題組織的 LaTeX 手稿，涵蓋 Theoretical Minimum 的核心主題。
- 📖 全域共用的中心書目（`tm.bib`），跨文件使用。
- 🖼️ `figs/` 目錄中的大型可重複使用圖庫。
- 🧰 圖片清理與圖形生成工具（`audit-images.py`、`plot_*.py`、`ising1.py`）。
- 🧮 使用 `pytearcat` 的 Jupyter notebook 計算補充資料。
- 🧪 用於磁區牆可視化的 NetLogo 模型（`Ising.nlogo`）。

## 🗂️ 專案結構

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

## 🚀 快速上手

| 目標 | 命令 |
|---|---|
| 編譯單一手稿 | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 重新生成宇宙學圖表 | `python plot_scale.py` |
| 審查未被參照的圖檔 | `python audit-images.py --figs ./figs` |
| 開啟 notebooks | `jupyter notebook` |

## 📚 課程筆記索引

| 檔案 | 說明 |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | 補充講座 |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Theoretical Minimum 書目 |

## 🧪 練習題

| 檔案 | 說明 |
|---|---|
| `gr-exercises.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) 的習題示例 |
| `cosmo.ipynb` | 使用 [pytearcat](https://arxiv.org/abs/2106.15016) 為 Friedmann-Lemaître-Robertson-Walker 度規計算愛因斯坦張量 |
| `schwartzchild.ipynb` | 使用 pytearcat 為 Schwarzschild 度規計算愛因斯坦張量 |

註：較早期的 README 文字提及 `schwartzchild.ipnb`；本專案實際檔案為 `schwartzchild.ipynb`。

## 🧰 輔助程式

| 檔案 | 說明 |
|---|---|
| `audit-images.py` | 用來找出未被引用的圖片，並產生含 `git rm` 指令的 `rm.sh` |
| `ising1.py` | 使用一維 Ising 模型，從第 7 講探索自發對稱性破缺 |
| `Ising.nlogo` | 磁區壁展示 |
| `plot-quartic.py` | 用於繪製 Higgs 玻色子 Mexican hat 势阱 |
| `plot_scale.py` | 用於繪製宇宙學尺度因子曲線 |
| `plot1.py` | Riemann 曲面風格可視化輔助工具（改編自原始碼連結中的 gist） |
| `plot2.py` | `plot1.py` 視覺化輔助工具的替代版本 |
| `template.py` | Python 程式模板 |
| `tm.wpr` | 輔助檔案的 Wing IDE 專案 |

## 📐 補充 *QFT in a Nutshell* 的證明

| 檔案 | 說明 |
|---|---|
| `qft1.tex` | 動機與基礎 |
| `qft2.tex` | Dirac 與旋量 |

## ✅ 前置條件

- 具備包含 `lualatex` 與 BibTeX 工具鏈的 LaTeX 發行版。
- 需要術語表條目的文件，請安裝 `makeglossaries`。
- Python 3，需安裝 `numpy` 與 `matplotlib` 以供輔助腳本使用。
- Jupyter Notebook/Lab 可開啟 `.ipynb` 檔案。
- 用於宇宙學 / Schwarzschild notebooks 流程的 `pytearcat`。
- 可選： [TexStudio](https://www.texstudio.org/) 與 [JabRef](https://www.jabref.org/)。

## 🧱 安裝

目前未提供套件管理檔（`requirements.txt`、`pyproject.toml` 等皆未提供），因此請採用手動設定。

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

如果你的 TeX 發行版缺少元件，請安裝以下套件：

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 使用方式

### 🧪 編譯講義（LaTeX）

許多原始檔明確指定 LuaLaTeX（`% !TeX program = lualatex`）。一般建置流程如下：

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

若檔案未使用術語表，請省略 `makeglossaries`。

### 🧬 執行輔助腳本

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

### 📓 使用 notebooks

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ 設定

此專案有意維持輕量，主要採文件驅動方式。

- 圖片路徑約定基於 `figs/` 與 TeX 檔案中的 `\\graphicspath{{figs/}}`。
- 腳本預設參數：
  - `audit-images.py`：`--figs ./figs`
  - `ising1.py`：可調參數包括（`--m`、`--n`、`--N`、`--T`、`--cool`、`--clamped`、`--seed`、`--figs`、`--show`）
- 目前仍沒有集中式設定檔。

## 🧭 範例

### 🪐 範例 1：重新生成宇宙學尺度因子圖

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 範例 2：盤點並清理未被參照的圖片

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 範例 3：建立 Advanced Quantum Mechanics 講義

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 開發說明

- 範圍：個人的、持續演化的講義與計算補充內容。
- 建置自動化刻意保持極簡，指令通常以手動執行為主。
- `.gitignore` 偏向 LaTeX 用途，並排除常見建置產物。
- `figs/` 較大，`audit-images.py` 有助於維持圖片參照整理。

## 🛠️ 疑難排解

- `tikz-feynman` 錯誤：請以 `lualatex` 重新編譯（由原始檔建議）。
- 術語表條目或輸出遺失：在兩次 LaTeX 編譯間執行 `makeglossaries <basename>`。
- 參考文獻缺漏：確認已執行 `bibtex <basename>` 並且存在 `tm.bib`。
- Python 匯入錯誤（`numpy`、`matplotlib`、`pytearcat`）：請在啟用的環境中安裝必要套件。
- Notebook 核心不一致：請切換到已安裝相依套件的環境。

## 🗺️ 路線圖

- 新增可重現的建置自動化（例如：每份手稿一組 `latexmk`/Makefile 包裝）。
- 補齊並鎖定 Python 相依性版本資訊。
- 充實 `i18n/` 的 README 語言版本。
- 說明哪些手稿可視為穩定／最終快照版本。

## 🤝 貢獻

歡迎提交貢獻，特別是：

- 拼字修正與公式/符號修正。
- 斷鏈接修復與參考資料清理。
- 建置與文件改進。
- 提升圖像與腳本的可重現性。

建議流程如下：

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 感謝

感謝本專案所使用工具的作者與維護者，特別是 LaTeX、LuaLaTeX、Matplotlib、Jupyter 與 pytearcat。

## ⚖️ 授權

本專案採用 `CC0-1.0` 授權條款，詳見 [`LICENSE`](../LICENSE)。

- Leonard Susskind 與其合作者的 *Theoretical Minimum* 課程。
- 本專案使用的工具包括 [TexStudio](https://www.texstudio.org/) 與 [JabRef](https://www.jabref.org/)。

## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |

## ⚖️ License

Repository-level license text is provided in [LICENSE](../LICENSE), currently **CC0 1.0 Universal**.

Note: some individual source files include their own copyright/license headers. Preserve those notices when reusing code.
