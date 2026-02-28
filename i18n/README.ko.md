[English](../README.md) · [العربية](README.ar.md) · [Español](README.es.md) · [Français](README.fr.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Tiếng Việt](README.vi.md) · [中文 (简体)](README.zh-Hans.md) · [中文（繁體）](README.zh-Hant.md) · [Deutsch](README.de.md) · [Русский](README.ru.md)


<p align="center">
  <img src="https://raw.githubusercontent.com/lachlanchen/lachlanchen/main/logos/banner.png" alt="LazyingArt banner" />
</p>

# [Theoretical Minimum Courses](http://theoreticalminimum.com/)를 위한 내 노트

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](../LICENSE)
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080)
![Python](https://img.shields.io/badge/Python-3.x-3776AB)
![Notebooks](https://img.shields.io/badge/Jupyter-Notebooks-F37626)
![Status](https://img.shields.io/badge/Project-Document--first-0A7E8C)

## 개요

이 저장소는 주로 LaTeX 원고(`*.tex`)와 공용 참고문헌(`tm.bib`)을 중심으로 구성된 문서 중심 물리학 노트 프로젝트이며, 그림 생성과 기호 계산 검증을 위한 Python 스크립트와 노트북을 함께 제공합니다.

## Leonard Susskind의 [Theoretical Minimum](http://theoreticalminimum.com/home) 강의를 바탕으로 한 강의 노트

**면책 고지** 이 노트는 개인 용도의 기억 보조(aide-mémoire)로 작성했습니다. 도움이 된다면 자유롭게 활용하셔도 좋지만, 사용 중이라면 알려주시면 감사하겠습니다. 이 문서는 강의를 직접 듣는 것을 대체하기 위한 목적이 아닙니다. 강의에서 파생된 모든 자료의 지적 재산권은 당연히 Susskind 교수에게 있으며, 포함된 오류는 전적으로 제 책임입니다.

노트 작성에는 [TexStudio](https://www.texstudio.org/), 참고문헌 관리는 [JabRef](https://www.jabref.org/)를 사용했습니다.

## 특징

- 📚 핵심 Theoretical Minimum 주제를 과정별로 정리한 LaTeX 원고.
- 📖 문서 전반에서 공유하는 중앙 참고문헌 파일(`tm.bib`).
- 🖼️ `figs/`에 있는 대규모 재사용 가능 그림 라이브러리.
- 🧰 그림 정리 및 생성 유틸리티(`audit-images.py`, `plot_*.py`, `ising1.py`).
- 🧮 `pytearcat` 기반 Jupyter 노트북 계산 보조 자료.
- 🧪 도메인 월 시각화를 위한 NetLogo 모델(`Ising.nlogo`).

## 프로젝트 구조

```text
.
├── README.md
├── LICENSE
├── tm.bib
├── figs/
├── i18n/
├── *.tex                 # 강의 노트, 연습문제, 용어집, QFT 보충
├── *.py                  # 보조 유틸리티 및 플로팅 스크립트
├── *.ipynb               # 계산 노트북
├── Ising.nlogo
└── tm.wpr
```

## 빠른 시작

| 목표 | 명령어 |
|---|---|
| 원고 하나 컴파일 | `lualatex gr.tex && bibtex gr && makeglossaries gr && lualatex gr.tex && lualatex gr.tex` |
| 우주론 플롯 재생성 | `python plot_scale.py` |
| 참조되지 않은 그림 점검 | `python audit-images.py --figs ./figs` |
| 노트북 열기 | `jupyter notebook` |

## 강의 노트 인덱스

| 파일 | 설명 |
|---|---|
| `aqm.tex` | [고급 양자역학 (Advanced Quantum Mechanics)](http://theoreticalminimum.com/courses/advanced-quantum-mechanics/2013/fall) |
| `entanglement.tex` | [양자 얽힘 (Quantum Entanglement)](http://theoreticalminimum.com/courses/quantum-entanglement/2006/fall) |
| `cosmology.tex` | [우주론 (Cosmology)](http://theoreticalminimum.com/courses/cosmology/2013/winter) |
| `gr.tex` | [일반상대성이론 (General Relativity)](http://theoreticalminimum.com/courses/general-relativity/2012/fall) |
| `gr-misc.tex` | 기타 강의 |
| `-` | [블랙홀 내부 (Inside Black Holes)](https://www.youtube.com/watch?v=yMRYZMv0jRE) |
| `-` | [홀로그램으로서의 세계 (The World as Hologram)](https://www.youtube.com/watch?v=2DIl3Hfh9tY) |
| `-` | [복잡성과 중력 (Complexity and Gravity)](https://youtu.be/6OXdhV5BOcY?t=797) |
| `-` | [왜 시간은 한 방향으로 흐르는가? (Why is Time a One-Way Street?)](https://www.youtube.com/watch?v=jhnKBKZvb_U) |
| `higgs.tex` | [힉스 보손 해설 (Demystifying the Higgs Boson)](http://theoreticalminimum.com/courses/higgs-boson/2012/summer/lecture-1) |
| `particles1.tex` | [입자물리학 1: 기본 개념 (Particle Physics 1: Basic Concepts)](http://theoreticalminimum.com/courses/particle-physics-1-basic-concepts/2009/fall) |
| `particles2.tex` | [입자물리학 2: 표준모형 (Particle Physics 2: Standard Model)](http://theoreticalminimum.com/courses/particle-physics-2-standard-model/2010/winter) |
| `particles3.tex` | [입자물리학 3: 초대칭과 대통일 (Particle Physics 3: Supersymmetry and Grand Unification)](http://theoreticalminimum.com/courses/particle-physics-3-supersymmetry-and-grand-unification/2010/spring/lecture-1) |
| `sm.tex` | [통계역학 (Statistical Mechanics)](http://theoreticalminimum.com/courses/statistical-mechanics/2013/spring) |
| `tm.bib` | Theoretical Minimum 참고문헌 |

## 연습문제

| 파일 | 설명 |
|---|---|
| `gr-exercises.tex` | [일반상대성이론 (General Relativity)](http://theoreticalminimum.com/courses/general-relativity/2012/fall)의 풀이 예제 |
| `cosmo.ipynb` | [pytearcat](https://arxiv.org/abs/2106.15016)로 Friedmann-Lemaître-Robertson-Walker metric의 아인슈타인 텐서 계산 |
| `schwartzchild.ipynb` | pytearcat로 Schwarzschild metric의 아인슈타인 텐서 계산 |

참고: 이전 README 텍스트에는 `schwartzchild.ipnb`가 언급되어 있었지만, 저장소 내 실제 파일은 `schwartzchild.ipynb`입니다.

## 보조 프로그램

| 파일 | 설명 |
|---|---|
| `audit-images.py` | 참조되지 않은 이미지 파일을 찾아 `git rm` 명령이 담긴 `rm.sh`를 생성 |
| `ising1.py` | 강의 7의 대칭 깨짐을 1차원 Ising 모델로 탐색 |
| `Ising.nlogo` | 도메인 월 시연 |
| `plot-quartic.py` | 힉스 보손의 멕시칸 햇 포텐셜 플롯 생성 |
| `plot_scale.py` | 우주론 scale-parameter 곡선 플롯 생성 |
| `plot1.py` | 리만 곡면 스타일 시각화 보조(소스에 연결된 gist 기반 변형) |
| `plot2.py` | `plot1.py` 시각화 보조의 대체 버전 |
| `template.py` | Python 프로그램 템플릿 |
| `tm.wpr` | 보조 파일용 Wing IDE 프로젝트 |

## *QFT in a Nutshell* 보충 증명

| 파일 | 설명 |
|---|---|
| `qft1.tex` | 동기와 기초 |
| `qft2.tex` | 디랙과 스피너 |

## 사전 요구사항

- `lualatex`와 BibTeX 도구를 포함한 LaTeX 배포판.
- 용어집을 사용하는 문서를 위한 `makeglossaries`.
- 보조 스크립트를 위한 `numpy`, `matplotlib`가 포함된 Python 3.
- `.ipynb` 파일 실행을 위한 Jupyter Notebook/Lab.
- 우주론/Schwarzschild 노트북 워크플로를 위한 `pytearcat`.
- 선택 사항: [TexStudio](https://www.texstudio.org/) 및 [JabRef](https://www.jabref.org/).

## 설치

현재 패키지 매니저 파일(`requirements.txt`, `pyproject.toml` 등)이 제공되지 않으므로 수동으로 환경을 설정해야 합니다.

```bash
# 1) Clone
git clone <your-fork-or-origin-url>
cd the_theoretical_minimum

# 2) Optional Python environment
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib jupyter pytearcat
```

TeX 배포판에 구성 요소가 누락되어 있다면 다음 패키지를 설치하세요.

- `tikz-feynman`
- `glossaries` / `glossaries-extra`
- `thmtools`
- `pgfplots`

## 사용법

### 강의 노트 컴파일 (LaTeX)

많은 소스 파일이 LuaLaTeX를 명시적으로 지정합니다(`% !TeX program = lualatex`). 일반적인 빌드 순서는 다음과 같습니다.

```bash
# Example: General Relativity notes
lualatex gr.tex
bibtex gr
makeglossaries gr   # if glossary is enabled for the file
lualatex gr.tex
lualatex gr.tex
```

용어집을 사용하지 않는 파일이라면 `makeglossaries`를 생략하세요.

### 보조 스크립트 실행

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

### 노트북 사용

```bash
jupyter notebook
# Open cosmo.ipynb or schwartzchild.ipynb
```

## 설정

이 저장소는 의도적으로 가볍게 유지되며, 대부분 파일 기반으로 동작합니다.

- 그림 경로 규칙은 TeX 파일의 `figs/` 및 `\graphicspath{{figs/}}`를 기준으로 합니다.
- 스크립트 기본값:
  - `audit-images.py`: `--figs ./figs`
  - `ising1.py`: 조정 가능한 시뮬레이션 플래그 포함 (`--m`, `--n`, `--N`, `--T`, `--cool`, `--clamped`, `--seed`, `--figs`, `--show`)
- 현재 중앙 설정 파일은 존재하지 않습니다.

## 예시

### 예시 1: 우주론 scale-factor 플롯 재생성

```bash
python plot_scale.py
# writes figs/cosmo-2-a-t and figs/cosmo-2-a-r
```

### 예시 2: 참조되지 않은 이미지 점검 및 정리

```bash
python audit-images.py --verbose --figs ./figs
# inspect generated rm.sh before executing
bash rm.sh
```

### 예시 3: Advanced Quantum Mechanics 노트 빌드

```bash
lualatex aqm.tex
bibtex aqm
makeglossaries aqm
lualatex aqm.tex
lualatex aqm.tex
```

## 개발 노트

- 범위: 개인용으로 계속 확장되는 강의 노트와 계산 보조 자료.
- 빌드 자동화는 의도적으로 최소화되어 있으며, 명령은 수동 실행을 전제로 합니다.
- `.gitignore`는 LaTeX 중심이며 일반적인 빌드 산출물을 제외합니다.
- `figs/` 디렉터리는 크기가 크므로 이미지 참조 정리에 `audit-images.py`가 유용합니다.

## 문제 해결

- `tikz-feynman` 오류: 소스 파일 권장 사항에 따라 `lualatex`로 컴파일하세요.
- 용어집 항목/출력이 누락됨: LaTeX 실행 사이에 `makeglossaries <basename>`을 실행하세요.
- 참고문헌 참조 누락: `bibtex <basename>`이 실행되었고 `tm.bib`가 존재하는지 확인하세요.
- Python import 오류 (`numpy`, `matplotlib`, `pytearcat`): 현재 활성 환경에 필요한 패키지를 설치하세요.
- 노트북 커널 불일치: 의존성이 설치된 환경의 커널을 선택하세요.

## 로드맵

- 재현 가능한 빌드 자동화 추가(예: 원고별 `latexmk`/Makefile 래퍼).
- 버전 고정된 Python 의존성 메타데이터 추가.
- `i18n/`에 번역 README 변형 채우기.
- 어떤 원고를 안정/최종 스냅샷으로 간주하는지 명확화.

## 기여

다음과 같은 기여를 환영합니다.

- 오탈자 및 수식/표기법 수정.
- 깨진 링크 및 참고문헌 정리.
- 빌드/문서화 개선.
- 그림/스크립트 재현성 개선.

권장 워크플로:

```bash
git checkout -b docs/<topic>
# make edits
git commit -m "docs: improve <topic>"
git push
# open a pull request
```

## 감사의 말

- *Theoretical Minimum* 강의를 제공한 Leonard Susskind와 협력자들.
- 이 프로젝트에서 사용한 도구: [TexStudio](https://www.texstudio.org/), [JabRef](https://www.jabref.org/).

## 라이선스

저장소 수준의 라이선스 텍스트는 [LICENSE](../LICENSE)에 있으며, 현재 **CC0 1.0 Universal**입니다.

참고: 일부 개별 소스 파일에는 자체 저작권/라이선스 헤더가 포함되어 있습니다. 코드를 재사용할 때 해당 고지는 유지하세요.
