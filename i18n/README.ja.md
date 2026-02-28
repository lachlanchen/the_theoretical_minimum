[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# [Theoretical Minimum Courses](http://theoreticalminimum.com/) のための私のノート

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 概要

このリポジトリは、主に LaTeX 原稿（`*.tex`）と共通参考文献（`tm.bib`）を中心に構成した、ドキュメントファーストの物理ノートプロジェクトです。図の作成や記号計算の確認を補助するために、Python スクリプトとノートブックも含まれています。

## Leonard Susskind の [Theoretical Minimum](http://theoreticalminimum.com/home) に基づく講義ノート

**免責事項** これらのノートは、私自身の備忘録として作成したものです。役に立った場合は自由に使っていただいて構いませんが、利用していることを知らせてもらえると嬉しいです。これらは講義視聴の代替を意図したものではありません。講義由来の内容に関する知的財産は当然ながら Susskind 教授に帰属します。一方、誤りがあればそれは私の責任です。

ノートの作成には [TexStudio](https://www.texstudio.org/) を、参考文献管理には [JabRef](https://www.jabref.org/) を使用しています。

## 特徴

- 📚 Theoretical Minimum の主要トピックをコース単位で整理した LaTeX 原稿。
- 📖 文書間で共有する中央参考文献ファイル（`tm.bib`）。
- 🖼️ `figs/` にある再利用可能な大規模図版ライブラリ。
- 🧰 図の整理・生成ユーティリティ（`audit-images.py`, `plot_*.py`, `ising1.py`）。
- 🧮 `pytearcat` を使った Jupyter ノートブックによる計算補助。
- 🧪 ドメインウォール可視化のための NetLogo モデル（`Ising.nlogo`）。

## プロジェクト構成

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

## クイックスタート

| 目的 | コマンド |
|---|---|
| 原稿を 1 つコンパイル | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 宇宙論プロットを再生成 | `python plot_scale.py` |
| 未参照の図を監査 | `python audit-images.py --figs ./figs` |
| ノートブックを開く | `jupyter notebook` |

## コースノート一覧

| ファイル | 説明 |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | その他の講義 |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Theoretical Minimum の参考文献 |

## 演習

| ファイル | 説明 |
|---|---|
| `gr-exercises.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) の解法付き例題 |
| `cosmo.ipynb` | [pytearcat](https://arxiv.org/abs/2106.15016) を使って Friedmann-Lemaître-Robertson-Walker 計量の Einstein テンソルを計算 |
| `schwartzchild.ipynb` | pytearcat を使って Schwarzschild 計量の Einstein テンソルを計算 |

注記: 以前の README では `schwartzchild.ipnb` と記載していましたが、リポジトリ内の実ファイルは `schwartzchild.ipynb` です。

## 補助プログラム

| ファイル | 説明 |
|---|---|
| `audit-images.py` | 未参照の画像ファイルを検出し、`git rm` コマンドを含む `rm.sh` を生成 |
| `ising1.py` | 1 次元 Ising モデルで講義 7 の対称性の破れを探索 |
| `Ising.nlogo` | ドメインウォールのデモ |
| `plot-quartic.py` | Higgs boson のメキシカンハットポテンシャルを描画 |
| `plot_scale.py` | 宇宙論のスケールパラメータ曲線を描画 |
| `plot1.py` | リーマン面風可視化の補助スクリプト（ソース内リンク先 gist をもとに調整） |
| `plot2.py` | `plot1.py` 可視化補助の別バージョン |
| `template.py` | Python プログラム用テンプレート |
| `tm.wpr` | 補助ファイル向けの Wing IDE プロジェクト |

## *QFT in a Nutshell* を補う証明

| ファイル | 説明 |
|---|---|
| `qft1.tex` | 動機と基礎 |
| `qft2.tex` | Dirac とスピノル |

## 前提条件

- `lualatex` と BibTeX ツールを含む LaTeX ディストリビューション。
- 用語集エントリを使う文書向けの `makeglossaries`。
- 補助スクリプト用に `numpy` と `matplotlib` を含む Python 3。
- `.ipynb` 用の Jupyter Notebook/Lab。
- 宇宙論 / Schwarzschild ノートブック運用向けの `pytearcat`。
- 任意: [TexStudio](https://www.texstudio.org/) と [JabRef](https://www.jabref.org/)。

## インストール

現時点ではパッケージマネージャ用ファイル（`requirements.txt`, `pyproject.toml` など）がないため、セットアップは手動です。

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

TeX ディストリビューションに不足がある場合は、次のパッケージを追加してください。

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 使い方

### 講義ノートをコンパイルする（LaTeX）

多くのソースで LuaLaTeX が明示されています（`% !TeX program = lualatex`）。一般的なビルド手順は次のとおりです。

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

用語集を使わないファイルでは `makeglossaries` を省略してください。

### 補助スクリプトを実行する

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

### ノートブックを使う

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## 設定

このリポジトリは意図的に軽量で、主にファイルベースで運用されます。

- 図のパス規約は `figs/` と TeX ファイル中の `\graphicspath{{figs/}}` に基づきます。
- スクリプトのデフォルト:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: 調整可能なシミュレーションフラグを含む（`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`）
- 現時点では集中管理された設定ファイルはありません。

## 例

### 例 1: 宇宙論のスケール因子プロットを再生成

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 例 2: 未参照画像を監査して整理

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 例 3: Advanced Quantum Mechanics ノートをビルド

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 開発メモ

- スコープ: 個人的で継続的に更新される講義ノートと計算補助。
- ビルド自動化は意図的に最小限で、コマンドは手動実行。
- `.gitignore` は LaTeX 中心で、一般的なビルド成果物を除外。
- `figs/` は大きいため、画像参照の整理には `audit-images.py` が有用。

## トラブルシューティング

- `tikz-feynman` のエラー: `lualatex` でコンパイル（ソースファイル推奨）。
- 用語集の項目/出力が欠ける: LaTeX の複数回実行の間に `makeglossaries <basename>` を実行。
- 参考文献参照が欠ける: `bibtex <basename>` の実行と `tm.bib` の存在を確認。
- Python の import エラー（`numpy`, `matplotlib`, `pytearcat`）: 使用中の環境に必要パッケージをインストール。
- ノートブックのカーネル不一致: 依存関係を入れた環境をカーネルとして選択。

## ロードマップ

- 再現可能なビルド自動化を追加（例: 各原稿向け `latexmk` / Makefile ラッパー）。
- Python 依存関係のバージョン固定メタデータを追加。
- 翻訳版 README を `i18n/` に拡充。
- どの原稿を安定版 / 最終版とみなすかを明確化。

## コントリビュート

次のような貢献を歓迎します。

- 誤字や数式・記法の修正。
- リンク切れや参考文献整備。
- ビルド/ドキュメントの改善。
- 図やスクリプトの再現性向上。

推奨ワークフロー:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 謝辞

- *Theoretical Minimum* 講義を提供する Leonard Susskind 氏と協力者の方々。
- 本プロジェクトで使用しているツールには [TexStudio](https://www.texstudio.org/) と [JabRef](https://www.jabref.org/) があります。

## ライセンス

リポジトリ全体のライセンステキストは [LICENSE](../LICENSE) にあり、現在は **CC0 1.0 Universal** です。

注記: 個別ソースファイルには独自の著作権/ライセンスヘッダが含まれる場合があります。コード再利用時はそれらの表記を保持してください。
