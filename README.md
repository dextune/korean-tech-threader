# Korean Tech Threader

> 당신도 테크 스레드가 되고 싶은가요?

좋은 테크 스레드는
그냥 정보를 요약하지 않습니다.

첫 줄에서 멈추게 만들고,
중간에서 고개를 끄덕이게 만들고,
마지막 줄에서 저장하게 만듭니다.

Korean Tech Threader는 그런 글을 쓰기 위한 스킬입니다.

AI, IT, 개발, 스타트업, 인프라, 자동화, 생산성 이야기를
그럴듯한 뉴스 요약이 아니라
실무자가 읽고 "이거 맞지" 하게 되는 한국어 테크 스레드로 바꿉니다.

긴 원문을 짧게 자르고,
뻔한 주장을 한 번 꺾고,
비용, 장애, 실패, 운영 리스크 같은 진짜 이야기를 앞으로 끌어냅니다.

말은 가볍게.
내용은 얕지 않게.
끝은 기억나게.

## What It Does

- 긴 원문을 모바일에서 읽기 쉬운 한국어 스레드로 변환합니다.
- 반말 기반의 캐주얼한 실무자 톤을 유지합니다.
- 비용, 장애, 실패, 운영 리스크 같은 현실적인 포인트를 강조합니다.
- 사실 검증이 필요한 내용은 리서치와 신뢰도 확인을 우선합니다.
- 근거가 부족한 수치, 모델명, 기업명, 보고서명은 임의로 만들어내지 않도록 안내합니다.
- 현재 기본 말투와 스타일을 `sharp-practitioner` 페르소나 모듈로 불러옵니다.

## Skill Name

```text
korean-tech-threader
```

Display name:

```text
Korean Tech Threader
```

## Repository Structure

```text
.
|-- SKILL.md
|-- references/
|   `-- personas.md
`-- README.md
```

## Installation

### Codex

Copy this skill folder into one of Codex's skill locations, for example:

```text
~/.agents/skills/korean-tech-threader
```

For a repository-local install, place it under:

```text
.agents/skills/korean-tech-threader
```

Then restart Codex if the skill does not appear automatically.

### Claude Code

Copy this skill folder into:

```text
~/.claude/skills/korean-tech-threader
```

Or install it as a project skill under:

```text
.claude/skills/korean-tech-threader
```

## Usage

Invoke the skill and provide source material:

```text
Use $korean-tech-threader to turn the following notes into a Korean tech thread:

[paste source text here]
```

You can also ask for a specific angle:

```text
Use $korean-tech-threader. Make this about the hidden operating cost of AI automation.
```

## Persona Modules

The default persona is:

```text
sharp-practitioner
```

It writes like a Korean tech practitioner who has shipped real systems, seen production failures, and prefers operational reality over shallow hype.

Use it explicitly like this:

```text
Use $korean-tech-threader with persona sharp-practitioner.

[paste source text here]
```

More personas can be added later in:

```text
references/personas.md
```

## Output Style

The generated thread should feel:

- short
- readable
- practical
- slightly sharp
- grounded in facts
- memorable at the end

It should avoid sounding like:

- a news article
- an academic summary
- a corporate blog post
- an exaggerated advertisement

## License

Add your preferred license before publishing.
