# 🧰 my-skills

AI에게 **매번 반복해서 설명하던 일**을 스킬 2개로 만들었습니다.

| 스킬 | 언제 쓰나 |
|---|---|
| [`homework-submit`](.claude/skills/homework-submit/SKILL.md) | 과제를 GitHub에 올려 제출하기 직전 |
| [`ask-first-brief`](.claude/skills/ask-first-brief/SKILL.md) | "게임 만들자"처럼 요청이 모호할 때, 만들기 전에 |

## 왜 만들었나

### 1. homework-submit: 제출 점검

| 불편 | 실제로 있었던 일 |
|---|---|
| "푸시됐어? README 있어? 링크 열려?"를 과제마다 다시 시킴 | 게임 과제와 Todo 과제에서 같은 확인을 두 번 함 |
| 제출란이 받는 링크 종류를 깜빡함 | 제출란은 `github.com`만 받는데 `github.io` 주소를 내려 했음 |
| README의 "게임 열기"가 상대경로라 GitHub에서 코드만 보임 | 눌러도 게임이 안 뜰 뻔했음 |

**해결**: "제출 점검해 줘" 한마디로 순서대로 확인하고, 고치기 전에 허락을 받고, 제출할 링크 1개와 내가 직접 할 일(로그인, 휴대폰 확인, 회고)을 줍니다. 회고는 대신 쓰지 않습니다.

### 2. ask-first-brief: 먼저 묻고 시작

| 불편 | 실제로 있었던 일 |
|---|---|
| "게임 만들자"라고만 하면 AI가 추측해서 만듦 | 원하지 않은 헤어스타일 게임이 나왔음 |
| 내가 원하는 장면(누가, 무엇을, 왜)을 처음에 말하지 못함 | 다시 만드느라 시간과 토큰이 듦 |

**해결**: 모호한 요청이면 만들기 전에 주인공·목표, 방해물, 끝난 기준, 하지 말 것을 짧게 묻고, 3줄 요약을 확인받은 뒤에 시작합니다. 게임뿐 아니라 앱 수정, 문서 작성에도 씁니다.

## 설치

적용할 프로젝트 루트에서 복사합니다.

```bash
mkdir -p .claude/skills
cp -r <my-skills 경로>/.claude/skills/homework-submit .claude/skills/
cp -r <my-skills 경로>/.claude/skills/ask-first-brief .claude/skills/
```

## 호출

프로젝트를 연 상태에서 **새 대화**를 시작합니다.

- `/homework-submit` 또는 "과제 제출 점검해 줘"
- `/ask-first-brief` 또는 모호한 요청 그대로 (예: "게임 만들자")

## 확인한 결과

> ⚠️ 새 대화에서 직접 호출해 본 뒤 채웁니다. (해 보기 전에는 비워 둡니다)

- 적용 프로젝트: HOMEWORK-PROJECT
- homework-submit 결과: <나온 것을 적기>
- ask-first-brief 결과: <"게임 만들자"라고 했을 때 나온 질문을 적기>

## 참고

인증 정보와 개인 데이터는 없습니다. `homework-submit`은 읽기 점검부터 하고, README 수정·커밋·푸시는 허락을 받은 뒤에만 합니다.
