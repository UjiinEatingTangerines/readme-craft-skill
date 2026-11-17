# README Craft

[![Claude Code 지원](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square)](#claude-code)
[![Codex 지원](https://img.shields.io/badge/Codex-14532D?style=flat-square)](#codex)
[![출력 형식 Markdown](https://img.shields.io/badge/Markdown-1864AB?style=flat-square)](SKILL.md)

**README의 구조를 정리하고 한국어 문장을 다듬습니다.**

Claude Code와 Codex에서 함께 쓰는 스킬입니다. 배지, 이모지 소제목, 바로가기, 표와 안내 상자로 읽는 순서를 잡습니다. 프로젝트의 기능, 설치 명령과 라이선스 정보는 그대로 보존합니다.

[구성 원칙](#principles) · [설치](#install) · [사용](#usage) · [파일 구성](#files) · [검증](#validation)

<a id="principles"></a>

## 🎨 구성 원칙

| 요소 | 적용 방식 |
| --- | --- |
| 배지 | 지원 도구·출력 형식 등 확인된 정보만 표시 |
| 소제목 | 의미에 맞는 이모지와 동일한 기본 글씨색 사용 |
| 구획 | 설치·사용·파일 구성·실행 조건을 구분 |
| 색상 | 브랜드 배지와 안내 상자에 사용 |
| 라이선스 | 프로젝트 자체와 외부 구성요소의 적용 범위를 구분 |
| 한국어 | 사실과 명령어를 유지하면서 반복 표현과 긴 수식을 정리 |

실제 구성은 [Sketch Flow README](https://github.com/UjiinEatingTangerines/sketch-flow-skill#readme)에서 볼 수 있습니다. 이 저장소의 README도 같은 규칙으로 작성했습니다.

<a id="install"></a>

## 📦 설치

<a id="claude-code"></a>

### 🛠️ ![Claude 로고](https://img.shields.io/badge/-D97757?style=flat-square&logo=claude&logoColor=white) Claude Code

**개인 설치** · 모든 프로젝트에서 사용합니다.

```sh
git clone https://github.com/UjiinEatingTangerines/readme-craft-skill.git ~/.claude/skills/readme-craft
```

**프로젝트 설치** · 특정 프로젝트에서만 쓰려면 프로젝트 루트에서 실행하세요. 두 방식 중 하나를 선택하면 됩니다.

```sh
git clone https://github.com/UjiinEatingTangerines/readme-craft-skill.git .claude/skills/readme-craft
```

<a id="codex"></a>

### 🛠️ ![OpenAI 로고](assets/codex-badge.svg) Codex

```sh
git clone https://github.com/UjiinEatingTangerines/readme-craft-skill.git ~/.codex/skills/readme-craft
```

`CODEX_HOME`을 따로 지정했다면 그 경로의 `skills/readme-craft`에 설치하세요. 설치 후 새 세션에서 스킬을 불러옵니다.

> [!TIP]
> 이미 설치했다면 해당 스킬 저장소에서 `git pull --ff-only`로 업데이트하세요. 직접 수정한 파일이 있다면 변경 사항을 먼저 확인하세요.

<a id="usage"></a>

## ✍️ 사용

### 💬 Claude Code에서 요청하기

```text
/readme-craft 이 저장소 README에 배지와 소제목 이모지를 넣고 구획을 정리해주세요.
소제목 글씨는 기본색으로 통일하고, 마지막에 한국어 문장을 다듬어주세요.
기존 설치 명령과 라이선스 정보는 보존해주세요.
```

### 💬 Codex에서 요청하기

```text
$readme-craft로 이 저장소 README의 가독성을 높여주세요.
배지, 표, 안내 상자를 필요한 곳에 사용하고 한국어 문장을 다듬어주세요.
```

커밋·푸시는 요청한 경우에만 수행합니다. 접기/펼치기 UI도 명시적으로 요청하지 않으면 추가하지 않습니다.

<a id="files"></a>

## 🗂️ 파일 구성

| 파일 | 용도 |
| --- | --- |
| [SKILL.md](SKILL.md) | Claude Code·Codex 공통 작업 지침 |
| [components.md](references/components.md) | 배지·소제목·표·라이선스 컴포넌트 규칙과 검증 방법 |
| [README.md](README.md) | 규칙을 적용한 문서 예제 |
| [openai.yaml](agents/openai.yaml) | Codex용 표시 메타데이터 |

<a id="validation"></a>

## ⚙️ 검증

파일을 읽고 수정할 수 있는 에이전트 환경에서 사용합니다. 특정 MCP 서버나 플러그인은 필요하지 않습니다. 링크와 이미지, 앵커, Markdown 구조를 확인하고 기존 명령어가 바뀌지 않았는지 비교합니다.

> [!NOTE]
> 브라우저 도구가 있으면 실제 화면도 확인합니다. 없으면 구조 점검과 화면 검증을 구분해 보고합니다. README 렌더링이 정상이어도 설치 명령의 실행까지 검증한 것은 아닙니다.

## 📄 외부 리소스

배지는 Shields.io에서 불러옵니다. 설치 구역의 OpenAI 문양은 [Simple Icons 11.15.0](https://cdn.jsdelivr.net/npm/simple-icons@11.15.0/icons/openai.svg)에서 가져왔으며, 출처를 [SVG 파일](assets/codex-badge.svg)에 보존했습니다. 해당 아이콘 배포물의 라이선스는 [CC0-1.0](https://github.com/simple-icons/simple-icons/blob/11.15.0/LICENSE.md)입니다. 이는 이 저장소 전체의 라이선스를 뜻하지 않습니다.
