[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# 我的 [Theoretical Minimum Courses](http://theoreticalminimum.com/) 学习笔记

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 概览

本仓库以文档优先为核心，围绕 LaTeX 手稿（`*.tex`）和共享参考文献库（`tm.bib`）构建，并配合用于图形和符号校验的 Python 脚本与 notebook。

## 🎓 Leonard Susskind 的 [Theoretical Minimum](http://theoreticalminimum.com/home) 课程讲义

**免责声明** 这些笔记主要是我为个人学习整理的备忘资料；如果你觉得有帮助，欢迎使用，但我也希望你告知我是否正在使用。它们**不应**替代课程本身的学习。课程素材的知识产权当然归 Susskind 教授所有；任何错误则由我本人承担。

这些笔记使用 [TexStudio](https://www.texstudio.org/) 编写，参考文献由 [JabRef](https://www.jabref.org/) 管理。

## ✨ 特性

- 📚 按课程主题组织的 LaTeX 手稿，覆盖 Theoretical Minimum 关键内容。
- 📖 跨文档共享的中心参考文献库（`tm.bib`）。
- 🖼️ 在 `figs/` 中包含的大型可复用图像库。
- 🧰 用于图像清理与图形生成的实用工具（`audit-images.py`、`plot_*.py`、`ising1.py`）。
- 🧮 基于 `pytearcat` 的 Jupyter notebook 计算补充材料。
- 🧪 用于畴壁可视化的 NetLogo 模型（`Ising.nlogo`）。

## 🗂️ 项目结构

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── .auto-readme-work/
├── notebooks/
├── *.tex                 # 讲义、习题、术语表、QFT 补充
├── *.py                  # 辅助工具与绘图脚本
├── notebooks/*.ipynb      # 计算型 notebooks
├── Ising.nlogo
└── tm.wpr
```

## 🚀 快速开始

| 目标 | 命令 |
|---|---|
| 编译单个手稿 | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 重新生成宇宙学图像 | `python plot_scale.py` |
| 审核未引用图像 | `python audit-images.py --figs ./figs` |
| 打开 notebook | `jupyter notebook` |

## 📚 课程笔记索引

| 文件 | 说明 |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | 课外/补充讲座 |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Theoretical Minimum 参考文献 |

## 🧪 习题

| 文件 | 说明 |
|---|---|
| `gr-exercises.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) 练习示例 |
| `cosmo.ipynb` | 使用 [pytearcat](https://arxiv.org/abs/2106.15016) 计算 Friedmann-Lemaître-Robertson-Walker 度规下的爱因斯坦张量 |
| `schwartzchild.ipynb` | 使用 pytearcat 计算 Schwarzschild 度规下的爱因斯坦张量 |

注：早期 README 中引用了 `schwartzchild.ipnb`，仓库实际文件为 `schwartzchild.ipynb`。

## 🧰 辅助程序

| 文件 | 说明 |
|---|---|
| `audit-images.py` | 用于识别未引用图像文件并生成带 `git rm` 命令的 `rm.sh` |
| `ising1.py` | 使用一维 Ising 模型探索第 7 讲中的对称性自发破缺 |
| `Ising.nlogo` | 畴壁示例模型 |
| `plot-quartic.py` | 用于绘制 Higgs 玻色子的 Mexican hat 势 |
| `plot_scale.py` | 用于绘制宇宙学尺度因子曲线 |
| `plot1.py` | Riemann 曲面风格可视化工具（改编自源码链接的 gist） |
| `plot2.py` | `plot1.py` 的替代可视化实现 |
| `template.py` | Python 程序模板 |
| `tm.wpr` | 辅助文件的 Wing IDE 项目 |

## 📐 *QFT in a Nutshell* 的补充证明

| 文件 | 说明 |
|---|---|
| `qft1.tex` | 动机与基础 |
| `qft2.tex` | Dirac 与旋量 |

## ✅ 先决条件

- 拥有带有 `lualatex` 与 BibTeX 工具链的 LaTeX 发行版。
- 含术语表条目的文档需 `makeglossaries`。
- Python 3，并已安装 `numpy` 与 `matplotlib`（用于辅助脚本）。
- 运行 `.ipynb` 文件所需的 Jupyter Notebook/Lab。
- 用于宇宙学 / Schwarzschild notebook 工作流的 `pytearcat`。
- 可选：[TexStudio](https://www.texstudio.org/) 与 [JabRef](https://www.jabref.org/)。

## 🧱 安装

当前未提供包管理文件（仓库内无 `requirements.txt`、`pyproject.toml` 等），因此请按需手动设置。

```bash
# 1) 克隆

git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) 可选：Python 环境
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

如果你的 TeX 发行版缺少某些组件，请补装：

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 使用

### 🧪 编译课程讲义（LaTeX）

许多源文件明确指定 LuaLaTeX（`% !TeX program = lualatex`）。通用构建流程如下：

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

对于不使用术语表的文件，可省略 `makeglossaries`。

### 🧬 运行辅助脚本

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

## 🛠️ 配置

本仓库刻意保持轻量，主要以文件约定驱动。

- 图像路径约定基于 `figs/` 和 TeX 文件中的 `\\graphicspath{{figs/}}`。
- 脚本默认参数：
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: 包含可调参数（`--m`、`--n`、`--N`、`--T`、`--cool`、`--clamped`、`--seed`、`--figs`、`--show`）
- 目前尚无统一的配置文件。

## 🧭 示例

### 🪐 示例 1：重建宇宙学尺度因子图

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 示例 2：审计并清理未引用的图像

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 示例 3：构建 Advanced Quantum Mechanics 讲义

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 开发说明

- 范围：个人持续维护的课程讲义与计算补充。
- 构建自动化故意保持最低限度；命令通常手动执行。
- `.gitignore` 偏向 LaTeX 工作流，并排除常见构建产物。
- `figs/` 体量较大；`audit-images.py` 有助于保持图像引用整洁。

## 🛠️ 故障排查

- `tikz-feynman` 错误：请使用 `lualatex` 编译（源码文件同样推荐该命令）。
- 术语表条目或输出缺失：在 LaTeX 多次编译之间执行 `makeglossaries <basename>`。
- 参考文献缺失：确认执行了 `bibtex <basename>`，并且 `tm.bib` 存在。
- Python 导入错误（`numpy`、`matplotlib`、`pytearcat`）：请在当前环境中安装必需依赖。
- Notebook 内核不匹配：切换到安装了依赖的环境。

## 🗺️ 路线图

- 增加可复现的构建自动化（例如：按手稿拆分的 `latexmk`/Makefile 封装）。
- 增补 Python 依赖元数据并锁定版本。
- 完善 `i18n/` 下的 README 多语言版本。
- 明确哪些手稿可视为稳定/最终快照。

## 🤝 贡献

欢迎提交贡献，尤其包括：

- 更正错字及公式/符号。
- 修复失效链接和参考文献清理。
- 改进构建和文档。
- 提升图像与脚本的可复现性。

推荐流程：

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 🙏 致谢

感谢本项目所用工具的创建者和维护者，尤其是 LaTeX、LuaLaTeX、Matplotlib、Jupyter 与 pytearcat。

## ⚖️ 许可证

本仓库采用 `CC0-1.0` 许可证。详见 [`LICENSE`](../LICENSE)。

- Leonard Susskind 与其合作者的 *Theoretical Minimum* 课程。
- 本项目使用的工具包括 [TexStudio](https://www.texstudio.org/) 与 [JabRef](https://www.jabref.org/)。

## ⚖️ 许可证

仓库级许可证文本见 [LICENSE](../LICENSE)，目前为 **CC0 1.0 Universal**。

注：部分单独源文件包含各自的版权/许可证说明。复用代码时请保留这些说明。


## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
