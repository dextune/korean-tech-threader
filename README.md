<p align="center">
  <img src="assets/ktt-title.svg" alt="Korean Tech Threader" width="900">
</p>

<p align="center">
  <img src="assets/ktt-readme.jpg" alt="Korean Tech Threader preview" width="900">
</p>

<p align="center">
  <img src="assets/ktt-tagline.svg" alt="당신도 테크 스레드가 되고 싶은가요?" width="900">
</p>

<p align="center">
  <a href="#빠른-사용"><img alt="Skill" src="https://img.shields.io/badge/skill-ktt-111111"></a>
  <a href="#페르소나"><img alt="Personas" src="https://img.shields.io/badge/personas-2-3376A0"></a>
  <a href="#자세한-설명"><img alt="Guide" src="https://img.shields.io/badge/guide-short-0f172a"></a>
</p>

Korean Tech Threader는 URL, 메모, 초안, 아이디어를 짧고 강한 한국어 테크 스레드로 바꾸는 스킬입니다.

말은 가볍게.  
내용은 얕지 않게.  
끝은 저장하고 싶게.

## 설치 방법

Codex, Claude Code에서 아래와 같이 입력합니다.

> [dextune/korean-tech-threader](https://github.com/dextune/korean-tech-threader) 스킬을 설치하세요.

프로젝트 안에서만 쓰려면 아래 위치에 둡니다.

```text
.agents/skills/ktt
.claude/skills/ktt
```

스킬이 보이지 않으면 Codex 또는 Claude Code를 다시 시작합니다.

## 빠른 사용

```text
$ktt 페르소나명 URL 또는 내용
```

```text
$ktt 존문가 https://example.com/article-about-ai-tools
```

```text
$ktt 거임
배포 자동화는 버튼보다 실패 복구 설계가 더 중요하다.
```

페르소나를 생략하면 `거임`으로 작성합니다.

```text
$ktt
AI 검색에서 중요한 건 점수보다 결과를 추적할 수 있는 구조다.
```

## 페르소나

| 페르소나 | 이런 글에 좋음 |
|---|---|
| `거임` | 운영, 비용, 장애, 실패 복구, 유지보수 |
| `존문가` | 도구 조합, 자동화, 빠른 실험, 비용 절감 |

목록 보기:

```text
ktt 목록
```

<br>
<br>

---

<br>
<br>

## 자세한 설명

### 무엇을 해주나

긴 원문을 그대로 요약하지 않습니다.  
하나의 중심 주장으로 압축하고, 모바일에서 읽기 쉬운 스레드 흐름으로 다시 씁니다.

주로 다룹니다:

- AI
- 개발
- 인프라
- 자동화
- 스타트업
- 생산성

### 작성 원칙

| 원칙 | 설명 |
|---|---|
| 짧게 | 한 줄을 길게 끌지 않습니다. |
| 하나만 | 한 스레드에는 중심 주장을 하나만 둡니다. |
| 꺾기 | 중간에 관점 전환이나 반전을 넣습니다. |
| 검증 | 확인되지 않은 수치나 이름은 단정하지 않습니다. |
| 페르소나 | 말투와 관점은 선택한 페르소나를 따릅니다. |

### 모듈 구조

```text
.
|-- SKILL.md
|-- assets/
|   |-- ktt-readme.jpg
|   |-- ktt-title.svg
|   `-- ktt.png
|-- references/
|   |-- thread-common.md
|   |-- thread-guim.md
|   `-- thread-johnmunga.md
`-- README.md
```

```mermaid
flowchart LR
    A["$ktt 입력"] --> B["thread-common.md"]
    B --> C{"페르소나"}
    C --> D["thread-guim.md"]
    C --> E["thread-johnmunga.md"]
    D --> F["한국어 테크 스레드"]
    E --> F
```

| 모듈 | 역할 |
|---|---|
| `thread-common.md` | 스레드 구조, 줄바꿈, 훅, 반전, 사실 검증 |
| `thread-guim.md` | `거임` 말투 |
| `thread-johnmunga.md` | `존문가` 말투 |

새 페르소나는 영어 파일명으로 추가합니다.

```text
references/thread-module-name.md
```

사용자가 입력하는 페르소나명은 한글이어도 됩니다.

### 말투 예시

`거임`

운영은 멋진 기능보다 실패했을 때 어떻게 복구하느냐가 더 중요하다.  
그래서 버튼보다 로그, 권한, 재시도 설계를 먼저 본다.

`존문가`

핵심은 단순하다.  
작은 도구를 묶어 빨리 돌려보고, 되면 붙이고 안 되면 버리면 된다.

## 라이선스

배포 전에 원하는 라이선스를 추가하세요.
