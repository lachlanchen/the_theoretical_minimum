[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


[![LazyingArt banner](https://github.com/lachlanchen/lachlanchen/raw/main/figs/banner.png)](https://github.com/lachlanchen/lachlanchen/blob/main/figs/banner.png)

---

# [Theoretical Minimum Courses](http://theoreticalminimum.com/)를 위한 내 노트

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 🌟 개요

이 저장소는 주로 LaTeX 원고(`*.tex`)와 공유 참고문헌(`tm.bib`)을 중심으로 구성된 문서 우선(문서가 먼저인) 물리 노트 프로젝트로, 그림 생성 및 기호 계산 점검을 위한 Python 스크립트와 노트북이 이를 보조합니다.

## 🎓 레오나드 서스킨드의 [Theoretical Minimum](http://theoreticalminimum.com/home) 강의 노트

**면책 조항** 이 노트는 제 스스로의 복습을 위한 메모로 제작한 것입니다. 도움이 되었다면 기꺼이 사용해도 좋지만, 사용하신다면 알려주시면 감사하겠습니다. 강의를 대신해 학습하도록 만든 것은 아니며, 듣기 학습의 대체 자료가 아닙니다. 강의로부터 파생된 모든 자료의 지적 재산권은 물론 서스킨드 교수님께 있으며, 그 외의 오류는 전적으로 제 책임입니다.

원고는 [TexStudio](https://www.texstudio.org/)로, 참고문헌은 [JabRef](https://www.jabref.org/)로 작성했습니다.

## ✨ 주요 기능

- 📚 핵심 Theoretical Minimum 주제를 과정 단위로 구성한 LaTeX 원고.
- 📖 문서 전체에서 공유되는 중앙 참고문헌(`tm.bib`).
- 🖼️ `figs/` 폴더의 크고 재사용 가능한 그림 라이브러리.
- 🧰 그림 정리 및 생성 유틸리티(`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 Jupyter 노트북 기반 계산 보강(`pytearcat` 사용).
- 🧪 도메인 월 시각화용 NetLogo 모델(`Ising.nlogo`).

## 🗂️ 프로젝트 구조

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── .auto-readme-work/
├── notebooks/
├── *.tex                 # 강의 노트, 연습문제, 용어집, QFT 보강 자료
├── *.py                  # 보조 유틸리티 및 플롯 생성 스크립트
├── notebooks/*.ipynb      # 계산 노트북
├── Ising.nlogo
└── tm.wpr
```

## 🚀 빠른 시작

| 목표 | 명령어 |
|---|---|
| 원고 하나 컴파일 | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 우주론 플롯 재생성 | `python plot_scale.py` |
| 참조되지 않는 그림 감사 | `python audit-images.py --figs ./figs` |
| 노트북 열기 | `jupyter notebook` |

## 📚 강의 노트 목록

| 파일 | 설명 |
|---|---|
| `aqm.tex` | [고급 양자역학](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [양자 얽힘](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [우주론](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [일반상대성이론](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | 기타 강의 |
| `-` | [블랙홀 내부](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [세계를 홀로그램으로](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [복잡성과 중력](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [왜 시간은 일방통행일까?](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [히그스 보손 이해하기](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [입자물리학 1: 기본 개념](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [입자물리학 2: 표준 모형](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [입자물리학 3: 초대칭과 대통일](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [통계역학](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Theoretical Minimum 참고문헌 |

## 🧪 연습문제

| 파일 | 설명 |
|---|---|
| `gr-exercises.tex` | [일반상대성이론](http://theoreticalminimum.com/courses/general-relativity/2012/fall)의 풀이 예시 |
| `cosmo.ipynb` | [pytearcat](https://arxiv.org/abs/2106.15016)로 Friedmann-Lemaître-Robertson-Walker 계량에서 아인슈타인 텐서를 계산 |
| `schwartzchild.ipynb` | pytearcat로 Schwarzschild 계량의 아인슈타인 텐서를 계산 |

참고: 이전 README 텍스트에는 `schwartzchild.ipnb`가 언급되어 있었지만, 저장소 파일은 `schwartzchild.ipynb`입니다.

## 🧰 보조 프로그램

| 파일 | 설명 |
|---|---|
| `audit-images.py` | 참조되지 않는 이미지 파일을 찾아 `git rm` 명령이 들어 있는 `rm.sh`를 생성 |
| `ising1.py` | 강의 7의 대칭 깨짐을 1차원 Ising 모델로 탐색 |
| `Ising.nlogo` | 도메인 월 시각화 데모 |
| `plot-quartic.py` | 힉스 보손의 '멕시칸 햇' 곡면을 플롯 |
| `plot_scale.py` | 우주론 스케일 인자 곡선을 플롯 |
| `plot1.py` | 리만 곡면 스타일 시각화 보조 (소스에서 링크된 gist를 기반으로 변형됨) |
| `plot2.py` | `plot1.py` 시각화 보조의 대체판 |
| `template.py` | Python 프로그램 템플릿 |
| `tm.wpr` | 보조 파일용 Wing IDE 프로젝트 |

## 📐 *QFT in a Nutshell* 보강 증명

| 파일 | 설명 |
|---|---|
| `qft1.tex` | 동기와 기초 |
| `qft2.tex` | 디랙과 스피너 |

## ✅ 선수 조건

- `lualatex`와 BibTeX 도구가 포함된 LaTeX 배포판.
- 용어집 항목을 사용하는 문서를 위한 `makeglossaries`.
- 보조 스크립트를 위한 `numpy`와 `matplotlib`가 포함된 Python 3.
- `.ipynb` 파일용 Jupyter Notebook/Lab.
- 우주론/Schwarzschild 노트북 워크플로용 `pytearcat`.
- 선택 사항: [TexStudio](https://www.texstudio.org/)와 [JabRef](https://www.jabref.org/).

## 🧱 설치

별도의 패키지 관리자 파일은 현재 제공되지 않습니다(`requirements.txt`, `pyproject.toml` 등 없음). 따라서 수동으로 설정합니다.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

TeX 배포판에 누락된 구성요소가 있으면 아래 패키지를 설치하세요.

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 🧭 사용법

### 🧪 강의 노트 컴파일 (LaTeX)

많은 소스에서 LuaLaTeX를 명시적으로 지정합니다(`% !TeX program = lualatex`). 일반적인 빌드 순서는 다음과 같습니다.

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

용어집을 사용하지 않는 파일은 `makeglossaries`를 생략하세요.

### 🧬 보조 스크립트 실행

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

### 📓 노트북 사용

```bash
jupyter notebook
# Open notebooks/cosmo.ipynb or notebooks/schwartzchild.ipynb
```

## 🛠️ 설정

이 저장소는 의도적으로 가볍고 주로 파일 중심으로 구성되어 있습니다.

- 그림 경로 규칙은 TeX 파일의 `figs/`와 `\graphicspath{{figs/}}`에 기반합니다.
- 스크립트 기본값:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: 조절 가능한 시뮬레이션 플래그 포함 (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- 현재 중앙 설정 파일은 없습니다.

## 🧭 예시

### 🪐 예시 1: 우주론 스케일 인자 플롯 재생성

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 🧹 예시 2: 참조되지 않는 이미지 감사 및 정리

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 🧱 예시 3: Advanced Quantum Mechanics 노트 빌드

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 📌 개발 노트

- 범위: 개인용으로 계속 진화하는 강의 노트와 계산 보강 자료.
- 빌드 자동화는 의도적으로 최소화되어 있으며, 명령은 수동으로 실행됩니다.
- `.gitignore`는 LaTeX 중심이고, 일반적인 빌드 산출물을 제외합니다.
- `figs/` 폴더가 크므로 `audit-images.py`로 이미지 참조 정리를 유지하면 좋습니다.

## 🛠️ 문제 해결

- `tikz-feynman` 오류: 소스 파일 권장 방식대로 `lualatex`로 컴파일하세요.
- 용어집 항목/출력 누락: LaTeX 패스 사이에 `makeglossaries <basename>`를 실행하세요.
- 참고문헌 누락 참조: `bibtex <basename>` 실행 여부와 `tm.bib` 존재 여부를 확인하세요.
- Python import 오류 (`numpy`, `matplotlib`, `pytearcat`): 활성 환경에 필요한 패키지를 설치하세요.
- 노트북 커널 불일치: 의존성이 설치된 환경의 커널을 선택하세요.

## 🗺️ 로드맵

- 재현 가능한 빌드 자동화 추가(예: 원고별 `latexmk`/Makefile 래퍼).
- 버전 고정 Python 의존성 메타데이터 추가.
- `i18n/`에 번역된 README 변형을 채움.
- 어느 원고가 안정/최종 스냅샷으로 간주되는지 명확화.



## ❤️ Support

| Donate | PayPal | Stripe |
| --- | --- | --- |
| [![Donate](https://camo.githubusercontent.com/24a4914f0b42c6f435f9e101621f1e52535b02c225764b2f6cc99416926004b7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f446f6e6174652d4c617a79696e674172742d3045413545393f7374796c653d666f722d7468652d6261646765266c6f676f3d6b6f2d6669266c6f676f436f6c6f723d7768697465)](https://chat.lazying.art/donate) | [![PayPal](https://camo.githubusercontent.com/d0f57e8b016517a4b06961b24d0ca87d62fdba16e18bbdb6aba28e978dc0ea21/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617950616c2d526f6e677a686f754368656e2d3030343537433f7374796c653d666f722d7468652d6261646765266c6f676f3d70617970616c266c6f676f436f6c6f723d7768697465)](https://paypal.me/RongzhouChen) | [![Stripe](https://camo.githubusercontent.com/1152dfe04b6943afe3a8d2953676749603fb9f95e24088c92c97a01a897b4942/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5374726970652d446f6e6174652d3633354246463f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065266c6f676f436f6c6f723d7768697465)](https://buy.stripe.com/aFadR8gIaflgfQV6T4fw400) |
