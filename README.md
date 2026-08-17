# 기자를 위한 바이브 코딩 가이드

기획 · 취재 · 보도 세 막을 AI 에이전트로 잇는 취재보도 실습 자료입니다.

**→ [학습 허브 열기](https://jonghhhh.github.io/newsroom_agent/)**

> ℹ️ 이 저장소 이름(`newsroom_agent`)은 실습에서 만드는 **작업 폴더 이름과 같습니다.**
> 저장소 = 강의 자료, 작업 폴더 = 각자의 실습 프로젝트로 구분해 주세요.

---

## 수강생이라면 여기부터

| | 문서 | 내용 |
|---|---|---|
| **먼저** | [강의 전 사전 준비](https://jonghhhh.github.io/newsroom_agent/prep.html) | 파이썬 · 네이버 API 키 · 스타터 세팅 (20분) |
| **받기** | [starter-claude.zip](starter/starter-claude.zip) | Claude Code를 쓰는 경우 |
| **받기** | [starter-codex.zip](starter/starter-codex.zip) | OpenAI Codex를 쓰는 경우 |

압축을 풀면 `newsroom_agent/` 폴더가 나옵니다. 설정 파일이 모두 들어 있어 바로 시작할 수 있습니다.

---

## 전체 자료

### 1차 · 도구 익히기

| 문서 | 내용 |
|---|---|
| [입문 가이드](https://jonghhhh.github.io/newsroom_agent/vibecoding_basic.html) | 파이썬 설치 · **가상환경(.venv)과 pip** · Claude Code · Codex · Antigravity CLI |
| [심화 가이드](https://jonghhhh.github.io/newsroom_agent/vibecoding_advanced.html) | 메모리 파일 · 스킬 · 서브에이전트 · 훅 · MCP · 병렬/반복/예약/대량 처리 |

### 2차 · 취재보도 실습 (세 막)

| 막 | 문서 | 산출물 |
|---|---|---|
| 1막 · 기획 | [plan.html](https://jonghhhh.github.io/newsroom_agent/plan.html) | 배경 브리프 + **질문 목록 Q1·Q2·Q3…** |
| 2막 · 취재 | [reporting.html](https://jonghhhh.github.io/newsroom_agent/reporting.html) | 수집 원문 + 개체 대장 + **사실 대장 F1·F2…** |
| 3막 · 보도 | [writing.html](https://jonghhhh.github.io/newsroom_agent/writing.html) | 기사 초고 + 문장별 팩트체크 |

### 부록

| 문서 | 내용 |
|---|---|
| [주제 바꾸기](https://jonghhhh.github.io/newsroom_agent/topic_switch.html) | 새 주제를 세 막 전체에 적용하는 법 (배달앱 수수료 사례) |
| [사전 준비 안내](https://jonghhhh.github.io/newsroom_agent/prep.html) | 수강생 발송용 |

<details>
<summary>보관본 (현행 커리큘럼에 미포함)</summary>

- [collector.html](https://jonghhhh.github.io/newsroom_agent/collector.html) — 자료 수집 파이프라인. 현재는 2막에 통합됨
- [investigation.html](https://jonghhhh.github.io/newsroom_agent/investigation.html) — 문서 더미에서 단서 찾기. 현재는 2막에 통합됨

</details>

---

## 이 실습의 핵심

세 막을 잇는 것은 설명이 아니라 **파일**입니다.

```
1막  질문 Q2  "특별법 전후로 수주가 늘었나?"
      ↓
2막  사실 F17 "A사가 2026-03-11 계약을 공시했다"  (근거: DART 공시 4쪽)
      ↓
3막  기사 문장 "…계약을 공시했다 [F17]"
```

기사의 한 문장에서 출발해 **원본 문서 몇 쪽까지 되짚을 수 있습니다.**
이 사슬이 있으면 "AI가 지어낸 것"과 "자료에 근거한 것"이 문장 단위로 구분됩니다.

---

## 준비물

- 노트북 (Windows / macOS), 인터넷
- 파이썬 3.11 이상
- VS Code
- **Claude Code 또는 OpenAI Codex** 중 하나 (문서에 양쪽 안내 모두 포함)
- API 키 — 1막은 **네이버 검색 API 하나만** 필요. DART·국회 키는 2막부터

---

## 원칙

- AI는 단서를 모아 주는 도구입니다. **확인과 게재의 책임은 사람 기자에게 있습니다.**
- 공개기록과 이용약관 안에서만. 로그인 우회 없이.
- 기사 전문은 복제하지 않고 링크와 짧은 인용으로.
- 사실 대장에 없는 문장은 기사에 쓰지 않습니다.

---

<sub>도구 버전 · 모델명 · API 사양은 2026년 8월 기준이며 자주 바뀝니다. 각 문서 하단의 참고문헌에서 최신 정보를 확인하세요.</sub>
