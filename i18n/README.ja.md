[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# [Theoretical Minimum Courses](http://theoreticalminimum.com/) のための私のノート

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 概要

このリポジトリは、LaTeX 原稿（`*.tex`）と共通の参考文献データベース（`tm.bib`）を中心に構築された、ドキュメント主導の物理学ノート集です。図生成と記号計算チェックを補助する Python スクリプトやノートブックも併用しています。

## 🎓 レナード・サスキンド（Leonard Susskind）《[Theoretical Minimum](http://theoreticalminimum.com/home)》の講義ノート

**免責事項** これらのノートは私自身の補助メモとして作成したものです。役に立つと感じていただけるなら歓迎しますが、使用する場合は知らせていただけると助かります。これらは講義を聞くことの代替になることを意図していません。すべての講義由来の知的財産権はもちろん Susskind 教授に帰属しますが、誤りは私の責任です。

このノートは [TexStudio](https://www.texstudio.org/) で作成され、参考文献管理は [JabRef](https://www.jabref.org/) で行いました。

## ✨ 特徴

- 📚 コアとなる Theoretical Minimum 各テーマの、講義ごとに整理された LaTeX 原稿。
- 📖 文書間で共有される `tm.bib` という一元化された参考文献。
- 🖼️ `figs/` にまとめた、再利用可能な大規模な図ライブラリ。
- 🧰 図の整備と生成のための補助ツール群（`audit-images.py`、`plot_*.py`、`ising1.py`）。
- 🧮 Jupyter ノートブックで `pytearcat` を用いた計算補助。
- 🧪 ドメイン壁の可視化を行う NetLogo モデル（`Ising.nlogo`）。

## 🗂️ プロジェクト構成

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── .auto-readme-work/
├── notebooks/
├── *.tex                 # 講義ノート、演習、用語集、QFT 補遺
├── *.py                  # 補助ユーティリティと描画スクリプト
├── notebooks/*.ipynb      # 計算ノートブック
├── Ising.nlogo
└── tm.wpr
```

## 🚀 クイックスタート

| 目的 | コマンド |
|---|---|
| 1 つの原稿をコンパイル | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 宇宙論プロットを再作成 | `python plot_scale.py` |
| 参照されない図を監査 | `python audit-images.py --figs ./figs` |
| ノートブックを開く | `jupyter notebook` |

## 📚 講義ノート一覧

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

## 🧪 演習

| ファイル | 説明 |
|---|---|
| `gr-exercises.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) の演習解答 |
| `cosmo.ipynb` | [pytearcat](https://arxiv.org/abs/2106.15016) を用いて、Friedmann-Lemaître-Robertson-Walker 計量に対する Einstein tensor を計算 |
| `schwartzchild.ipynb` | pytearcat を用いて Schwarzschild 計量の Einstein tensor を計算 |

注記: 以前の README では `schwartzchild.ipnb` と記載されていましたが、実際のファイルは `schwartzchild.ipynb` です。

## 🧰 補助プログラム

| ファイル | 説明 |
|---|---|
| `audit-images.py` | 未参照画像ファイルを特定し、`rm.sh` として `git rm` コマンドを出力 |
| `ising1.py` | 1 次元 Ising モデルを用いて、第7講義の対称性の破れを可視化 |
| `Ising.nlogo` | ドメイン壁のデモ |
| `plot-quartic.py` | ヒッグスボゾンのメキシカンハット曲線を描画 |
| `plot_scale.py` | 宇宙論のスケール係数曲線を描画 |
| `plot1.py` | リーマン曲面スタイルの可視化ヘルパー（ソースのリンク付き gist から改変） |
| `plot2.py` | `plot1.py` の代替可視化ヘルパー |
| `template.py` | Python プログラムのテンプレート |
| `tm.wpr` | 補助ファイル群用の Wing IDE プロジェクト |

## 📐 *QFT in a Nutshell* の補完証明

| ファイル | 説明 |
|---|---|
| `qft1.tex` | 動機付けと基礎 |
| `qft2.tex` | Dirac とスピノル |

## ✅ 事前準備

- `lualatex` と BibTeX ツールを含む LaTeX 配布版。
- 用語集付き文書では `makeglossaries` が必要。
- 補助スクリプトの実行には Python 3 と `numpy`、`matplotlib`。
- `.ipynb` ファイルを扱うには Jupyter Notebook/Lab。
- 宇宙論・Schwarzschild ノートブックのワークフローには `pytearcat`。
- 任意: [TexStudio](https://www.texstudio.org/) と [JabRef](https://www.jabref.org/)。

## 🧱 インストール

現在、パッケージ管理ファイルはありません（`requirements.txt`、`pyproject.toml` など未配置）。そのためセットアップは手動です。

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

TeX 配布環境に必要なコンポーネントが不足している場合は、次を導入してください。

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 使用方法

### 🧪 講義ノートをコンパイルする（LaTeX）

多くのソースでは LuaLaTeX が明示されています（`% !TeX program = lualatex`）。一般的なビルド順は次のとおりです。

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

用語集を使用していないファイルでは `makeglossaries` は省略します。

### 🧬 補助スクリプトを実行する

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

### 📓 ノートブックを使う

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ 設定

このリポジトリは意図的に軽量で、ほぼファイル駆動です。

- 図のパス規約は TeX ファイル内の `figs/` と `\graphicspath{{figs/}}` に基づいています。
- スクリプトの既定値:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: 調整可能なシミュレーション引数（`--m`、`--n`、`--N`、`--T`、`--cool`、`--clamped`、`--seed`、`--figs`、`--show`）
- 現在、集中管理の設定ファイルは存在しません。

## 🧭 例

### 🪐 例 1: 宇宙論スケールファクターのプロットを再生成

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 例 2: 未参照画像を監査して整理

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 例 3: Advanced Quantum Mechanics ノートをビルド

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 開発メモ

- 対象: 個人的に継続的に更新される講義ノートと計算補助資料。
- ビルド自動化は意図的に最小限で、コマンドは手動実行。
- `.gitignore` は LaTeX 向けに設計され、一般的なビルド成果物を除外。
- `figs/` は規模が大きいため、`audit-images.py` が参照整合を保つのに役立ちます。

## 🛠️ トラブルシューティング

- `tikz-feynman` 関連エラー: `lualatex` で再コンパイルします（ソースファイルでも推奨）。
- 用語集エントリまたは出力の欠落: LaTeX 実行間で `makeglossaries <basename>` を実行。
- 参考文献参照の欠落: `bibtex <basename>` が実行され、`tm.bib` が存在することを確認。
- Python のインポートエラー（`numpy`、`matplotlib`、`pytearcat`）: アクティブな環境に必要パッケージをインストール。
- ノートブックのカーネル不一致: 依存ライブラリが入った環境を選択。

## 🗺️ ロードマップ

- 再現可能なビルド自動化の追加（例: 原稿ごとの `latexmk` / Makefile ラッパー）。
- Python の固定依存情報を追加。
- `i18n/` に翻訳済み README バリアントを追加。
- どの原稿が安定版・完成版に該当するかを明確化。

## 🤝 貢献

ご意見・修正は歓迎します。特に次の内容。

- タイポや式・記法の修正。
- 破損リンクの修正と参照のクリーンアップ。
- ビルド・ドキュメント改善。
- 図・スクリプトの再現性向上。

推奨ワークフロー:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
