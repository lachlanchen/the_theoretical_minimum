[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)

<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>


# 我的 [Theoretical Minimum Courses](http://theoreticalminimum.com/) 学习笔记

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 概览

本仓库是一个以文档为核心的物理学习笔记项目，围绕 LaTeX 手稿（`*.tex`）和共享参考文献库（`tm.bib`）构建，并配有用于图像生成与符号校验的 Python 脚本与 notebooks。

## 基于 Leonard Susskind [Theoretical Minimum](http://theoreticalminimum.com/home) 课程的讲义笔记

**免责声明** 这些笔记主要是我为自己整理的备忘资料；如果你觉得有帮助，欢迎使用，也希望你能告知我。它们 _并不_ 旨在替代课程视频本身。所有源自课程内容的知识产权当然归 Susskind 教授所有；其中任何错误均由我个人负责。

这些笔记使用 [TexStudio](https://www.texstudio.org/) 编写，参考文献由 [JabRef](https://www.jabref.org/) 管理。

## 特性

- 📚 按课程主题组织的 LaTeX 手稿，覆盖 Theoretical Minimum 核心内容。
- 📖 跨文档共享的中心参考文献库（`tm.bib`）。
- 🖼️ 位于 `figs/` 的大型可复用图像资源库。
- 🧰 用于图像清理和图表生成的实用工具（`audit-images.py`, `plot_*.py`, `ising1.py`）。
- 🧮 基于 `pytearcat` 的 Jupyter notebook 计算补充材料。
- 🧪 用于畴壁可视化的 NetLogo 模型（`Ising.nlogo`）。

## 项目结构

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── *.tex                 # 讲义、习题、术语表、QFT 补充
├── *.py                  # 辅助工具与绘图脚本
├── *.ipynb               # 计算型 notebooks
├── Ising.nlogo
└── tm.wpr
```

## 快速开始

| 目标 | 命令 |
|---|---|
| 编译单个手稿 | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 重新生成宇宙学图像 | `python plot_scale.py` |
| 审计未被引用的图像 | `python audit-images.py --figs ./figs` |
| 打开 notebooks | `jupyter notebook` |

## 课程笔记索引

| 文件 | 说明 |
|---|---|
| `aqm.tex` | [Advanced Quantum Mechanics](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [Quantum Entanglement](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [Cosmology](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | 杂项讲座 |
| `-` | [Inside Black Holes](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [The World as Hologram](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [Complexity and Gravity](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [Why is Time a One-Way Street?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [Demystifying the Higgs Boson](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [Particle Physics 1: Basic Concepts](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [Particle Physics 2: Standard Model](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [Particle Physics 3: Supersymmetry and Grand Unification](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [Statistical Mechanics](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Theoretical Minimum 参考文献库 |

## 习题

| 文件 | 说明 |
|---|---|
| `gr-exercises.tex` | [General Relativity](http://theoreticalminimum.com/courses/general-relativity/2012/fall) 的例题讲解 |
| `cosmo.ipynb` | 使用 [pytearcat](https://arxiv.org/abs/2106.15016) 计算 Friedmann-Lemaître-Robertson-Walker 度规下的 Einstein 张量 |
| `schwartzchild.ipynb` | 使用 pytearcat 计算 Schwarzschild 度规下的 Einstein 张量 |

注：早期 README 文本中引用了 `schwartzchild.ipnb`；仓库中的实际文件为 `schwartzchild.ipynb`。

## 辅助程序

| 文件 | 说明 |
|---|---|
| `audit-images.py` | 用于识别未被引用的图片文件，并生成带 `git rm` 命令的 `rm.sh` |
| `ising1.py` | 基于一维 Ising 模型探索第 7 讲中的对称性破缺 |
| `Ising.nlogo` | 畴壁演示模型 |
| `plot-quartic.py` | 用于绘制 Higgs 玻色子的 Mexican hat 势 |
| `plot_scale.py` | 用于绘制宇宙学尺度因子曲线 |
| `plot1.py` | Riemann 曲面风格可视化辅助脚本（改编自源码中链接的 gist） |
| `plot2.py` | `plot1.py` 可视化辅助脚本的另一版本 |
| `template.py` | Python 程序模板 |
| `tm.wpr` | 用于辅助文件的 Wing IDE 项目 |

## 对 *QFT in a Nutshell* 的补充推导

| 文件 | 说明 |
|---|---|
| `qft1.tex` | 动机与基础 |
| `qft2.tex` | Dirac 与旋量 |

## 先决条件

- 包含 `lualatex` 与 BibTeX 工具链的 LaTeX 发行版。
- 对使用术语表的文档，需要 `makeglossaries`。
- Python 3，且安装 `numpy` 与 `matplotlib`（用于辅助脚本）。
- 用于运行 `.ipynb` 文件的 Jupyter Notebook/Lab。
- 用于宇宙学/Schwarzschild notebook 工作流的 `pytearcat`。
- 可选：[TexStudio](https://www.texstudio.org/) 与 [JabRef](https://www.jabref.org/)。

## 安装

当前未提供包管理文件（仓库中不存在 `requirements.txt`、`pyproject.toml` 等），因此需要手动配置。

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

如果你的 TeX 发行版缺少组件，请安装以下包：

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 使用方法

### 编译课程讲义（LaTeX）

许多源文件显式指定了 LuaLaTeX（`% !TeX program = lualatex`）。通用构建流程如下：

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

对于不使用术语表的文件，可省略 `makeglossaries`。

### 运行辅助脚本

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

### 使用 notebooks

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## 配置

本仓库刻意保持轻量，整体以文件约定为驱动。

- 图像路径约定基于 `figs/` 以及 TeX 文件中的 `\graphicspath{{figs/}}`。
- 脚本默认值：
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: 包含可调模拟参数（`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`）
- 目前不存在集中式配置文件。

## 示例

### 示例 1：重新生成宇宙学尺度因子图

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 示例 2：审计并清理未引用图像

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 示例 3：构建 Advanced Quantum Mechanics 讲义

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 开发说明

- 范围：个人持续整理的课程笔记与计算补充内容。
- 构建自动化刻意保持最小化；命令通常手动执行。
- `.gitignore` 偏向 LaTeX 工作流，排除了常见构建产物。
- `figs/` 体量较大；`audit-images.py` 有助于保持图像引用整洁。

## 故障排查

- `tikz-feynman` 报错：请使用 `lualatex` 编译（源码文件也推荐此方式）。
- 术语表条目或输出缺失：在 LaTeX 多次编译之间运行 `makeglossaries <basename>`。
- 参考文献引用缺失：确认已运行 `bibtex <basename>` 且 `tm.bib` 存在。
- Python 导入错误（`numpy`, `matplotlib`, `pytearcat`）：在当前环境中安装所需依赖。
- Notebook 内核不匹配：选择已安装依赖的运行环境。

## 路线图

- 增加可复现的构建自动化（例如：按手稿划分的 `latexmk`/Makefile 封装）。
- 增加带版本锁定的 Python 依赖元数据。
- 在 `i18n/` 中补全 README 的多语言版本。
- 明确哪些手稿已被视为稳定/最终快照。

## 贡献

欢迎贡献，尤其包括：

- 拼写错误与公式/符号修正。
- 失效链接与参考文献整理。
- 构建/文档改进。
- 图像与脚本可复现性改进。

建议流程：

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 致谢

- 感谢 Leonard Susskind 及其合作团队提供 *Theoretical Minimum* 课程。
- 本项目使用的工具包括 [TexStudio](https://www.texstudio.org/) 与 [JabRef](https://www.jabref.org/)。

## 许可证

仓库级许可证见 [LICENSE](../LICENSE)，当前为 **CC0 1.0 Universal**。

注：部分单独源文件包含其各自的版权/许可证声明。复用代码时请保留这些声明。
