[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# 我的 [Theoretical Minimum Courses](http://theoreticalminimum.com/) 筆記

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 概覽

這個儲存庫主要是一個以文件為核心（document-first）的物理學筆記專案，圍繞 LaTeX 手稿（`*.tex`）與共用參考文獻庫（`tm.bib`）建構，並搭配 Python 腳本與筆記本用於繪圖與符號檢查。

## 基於 Leonard Susskind [Theoretical Minimum](http://theoreticalminimum.com/home) 的課程筆記

**聲明**：這些筆記是我為了自己使用而整理的備忘；如果你覺得有幫助，歡迎使用，但若能告知我你正在使用會很感謝。這些筆記_不_是用來取代實際聽課。凡由課程衍生的內容，其智慧財產權當然屬於 Susskind 教授；其中若有錯誤，則由我自行負責。

筆記使用 [TexStudio](https://www.texstudio.org/) 撰寫，文獻庫使用 [JabRef](https://www.jabref.org/) 管理。

## 特色

- 📚 依課程主題組織的 LaTeX 手稿，涵蓋 Theoretical Minimum 核心內容。
- 📖 跨文件共用的中心文獻庫（`tm.bib`）。
- 🖼️ 位於 `figs/` 的大型可重用圖庫。
- 🧰 圖像整理與生成工具（`audit-images.py`, `plot_*.py`, `ising1.py`）。
- 🧮 使用 `pytearcat` 的 Jupyter 筆記本作為計算補充。
- 🧪 用於領域壁（domain wall）可視化的 NetLogo 模型（`Ising.nlogo`）。

## 專案結構

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

## 快速開始

| 目標 | 指令 |
|---|---|
| 編譯單一手稿 | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 重新產生宇宙學圖表 | `python plot_scale.py` |
| 稽核未被引用的圖片 | `python audit-images.py --figs ./figs` |
| 開啟筆記本 | `jupyter notebook` |

## 課程筆記索引

| 檔案 | 說明 |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | 雜項講次 |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Theoretical Minimum 的文獻庫 |

## 練習

| 檔案 | 說明 |
|---|---|
| `gr-exercises.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) 的範例解題 |
| `cosmo.ipynb` | 使用 [pytearcat](https://arxiv.org/abs/2106.15016) 計算 Friedmann-Lemaître-Robertson-Walker 度規的 Einstein tensor |
| `schwartzchild.ipynb` | 使用 pytearcat 計算 Schwarzschild 度規的 Einstein tensor |

注意：較早版本的 README 曾寫成 `schwartzchild.ipnb`；儲存庫中的檔案為 `schwartzchild.ipynb`。

## 輔助程式

| 檔案 | 說明 |
|---|---|
| `audit-images.py` | 用於找出未被引用的圖片檔，並輸出含 `git rm` 指令的 `rm.sh` |
| `ising1.py` | 使用一維 Ising 模型探索第 7 講中的對稱性破缺 |
| `Ising.nlogo` | 領域壁示範 |
| `plot-quartic.py` | 用於繪製 Higgs boson 的 Mexican hat |
| `plot_scale.py` | 用於繪製宇宙學尺度參數曲線 |
| `plot1.py` | Riemann 曲面風格視覺化輔助（改寫自原始碼中連結的 gist） |
| `plot2.py` | `plot1.py` 視覺化輔助的另一版本 |
| `template.py` | Python 程式範本 |
| `tm.wpr` | 輔助檔案使用的 Wing IDE 專案 |

## 補充 *QFT in a Nutshell* 的證明

| 檔案 | 說明 |
|---|---|
| `qft1.tex` | Motivation and Foundation |
| `qft2.tex` | Dirac and the Spinor |

## 先備需求

- 具備 `lualatex` 與 BibTeX 工具鏈的 LaTeX 發行版。
- 對使用術語表的文件，需要 `makeglossaries`。
- Python 3，以及供輔助腳本使用的 `numpy`、`matplotlib`。
- 用於 `.ipynb` 檔案的 Jupyter Notebook/Lab。
- 用於宇宙學/Schwarzschild 筆記本流程的 `pytearcat`。
- 選配：[TexStudio](https://www.texstudio.org/) 與 [JabRef](https://www.jabref.org/)。

## 安裝

目前沒有提供套件管理檔（`requirements.txt`、`pyproject.toml` 等不存在），因此需手動設定。

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

若你的 TeX 發行版缺少元件，請安裝以下套件：

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 使用方式

### 編譯課程筆記（LaTeX）

許多來源檔明確指定 LuaLaTeX（`% !TeX program = lualatex`）。一般建置流程如下：

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

對不使用術語表的檔案，可省略 `makeglossaries`。

### 執行輔助腳本

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

### 使用筆記本

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## 設定

本儲存庫刻意維持輕量，且主要由檔案驅動。

- 圖片路徑慣例基於 `figs/`，以及 TeX 檔中的 `\graphicspath{{figs/}}`。
- 腳本預設值：
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: 包含可調整的模擬旗標（`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`）
- 目前沒有集中式設定檔。

## 範例

### 範例 1：重新產生宇宙學尺度因子圖

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 範例 2：稽核並清理未引用圖片

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 範例 3：建置 Advanced Quantum Mechanics 筆記

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 開發備註

- 範圍：個人使用、持續演進的課程筆記與計算補充內容。
- 建置自動化刻意維持最小化；指令以手動執行為主。
- `.gitignore` 以 LaTeX 為主，排除常見建置產物。
- `figs/` 體積較大；`audit-images.py` 有助於維持圖片引用整潔。

## 疑難排解

- `tikz-feynman` 錯誤：請用 `lualatex` 編譯（來源檔也建議如此）。
- 缺少術語表條目/輸出：在 LaTeX 多輪編譯間執行 `makeglossaries <basename>`。
- 缺少參考文獻引用：確認已執行 `bibtex <basename>` 且 `tm.bib` 存在。
- Python 匯入錯誤（`numpy`, `matplotlib`, `pytearcat`）：在目前啟用環境安裝所需套件。
- 筆記本 kernel 不一致：選擇已安裝相依套件的環境。

## 路線圖

- 加入可重現建置自動化（例如各手稿的 `latexmk`/Makefile 包裝）。
- 加入已固定版本的 Python 相依資訊。
- 在 `i18n/` 補齊 README 各語言翻譯版本。
- 釐清哪些手稿屬於穩定/最終快照。

## 貢獻

歡迎貢獻，特別是：

- 錯字與公式/記號修正。
- 失效連結與參考清理。
- 建置/文件改進。
- 圖片/腳本可重現性改進。

建議流程：

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 致謝

- Leonard Susskind 與其合作者提供 *Theoretical Minimum* 系列課程。
- 本專案使用的工具包括 [TexStudio](https://www.texstudio.org/) 與 [JabRef](https://www.jabref.org/)。

## 授權

儲存庫層級授權條文位於 [LICENSE](LICENSE)，目前為 **CC0 1.0 Universal**。

注意：部分個別原始檔包含其自身的版權/授權標頭。重用程式碼時請保留這些聲明。
