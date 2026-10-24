# Post · 네이티브처럼 보이고 팔리는 공유 이미지

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | 한국어 | [Tiếng Việt](README.vi.md) | [हिन्दी](README.hi.md)

<p align="center"><img src="docs/share.png" alt="Post: a day of notes into a native-looking carousel" width="100%"></p>
<p align="center"><sub><a href="https://github.com/jack-reson8/copy-that"><b>Copy That</b></a> 시리즈 · 한 줄로 전체 설치</sub></p>

**오늘의 사실만 Claude에게 주세요. 진짜 앱 화면처럼 보이고, 유머 있는 사람 말투로 읽히며, 제품과 시리즈를 함께 밀어 주는 샤오훙수(Xiaohongshu) / X용 이미지 세트가 나옵니다.**

<table><tr>
<td><img src="docs/frame-1.jpg" width="170"></td>
<td><img src="docs/frame-2.jpg" width="170"></td>
<td><img src="docs/frame-3.jpg" width="170"></td>
<td><img src="docs/frame-4.jpg" width="170"></td>
<td><img src="docs/frame-5.jpg" width="170"></td>
</tr></table>
<sub>빌드 인 퍼블릭 시리즈("Claude가 월 $200 구독료를 직접 벌어오게 하기")의 1일차. 이 스킬로 제작.</sub>

AI가 만든 게시물 이미지는 대부분 같은 이유로 실패합니다. 그라데이션 카드, 이모지 목록, 템플릿 티가 팍 나는 "디자인된" 장면. 이 스킬은 실제로 7번 퇴짜를 맞고("못생겼다", "AI가 만든 티 난다", "Claude 같지 않다", "너무 진지하다") 마침내 통과된 과정에서 나왔고, 그때 문제를 고친 방법을 그대로 담았습니다.

| 단계 | Claude가 하는 일 |
|---|---|
| 1 · 브리프 | `brief.md`: 게시물의 GTM 역할, 시리즈 정체성, 출처가 있는 사실 목록. 이미지에는 이 목록에 있는 내용만 들어갈 수 있음 |
| 2 · 레퍼런스 | 플랫폼에서 좋아요 많은 커버를 그리드로 모으고, 감각 좋은 앱의 App Store 스크린샷 세트를 분석해 핵심 3가지를 정리(게이트) |
| 3 · 스토리보드 | 프레임당 한 줄: 헤드라인, 근거, 떠 있는 카드, 개그, GTM 역할. 필수: 시리즈 로고가 들어간 커버, 실제 결과물과 가격을 보여주는 제품 프레임, 숫자 전면 페이지, 팔로우 유도 |
| 4 · 카피 | 먼저 담백하게 쓰고, 개그 라이브러리에서 1~3개를 더함(질문형 제목, 한 줄 펀치, 무표정 개그, 콜백, 반전 마무리) |
| 5 · 제작 | 실제 모바일 스크린샷, 픽셀 단위로 재현한 UI 목업(X, Claude, iOS 잠금 화면, Google, Stripe), 표가 아닌 도표, App Store 포스터 템플릿 |
| 6 · 검수 | 썸네일 크기의 컨택트 시트를 체크리스트로 점검 |
| 7 · 전달 | 컨택트 시트 + 제목 후보 2~3개. 게시는 항상 직접 결정 |

## 설치

**Claude Code 플러그인으로 (권장)**

```bash
claude plugin marketplace add jack-reson8/post-skill
claude plugin install post@post-skill
```

**일반 스킬로**

```bash
git clone https://github.com/jack-reson8/post-skill
cp -R post-skill/plugins/post/skills/post ~/.claude/skills/
```
헤드리스 렌더링용 Google Chrome과, 컨택트 시트용 Pillow가 설치된 Python 3이 필요합니다.

**Codex (CLI 또는 ChatGPT 데스크톱 앱):**

```bash
codex plugin marketplace add jack-reson8/post-skill
codex plugin add post@post-skill
```

`plugins/post/skills/post`를 `~/.codex/skills/`에 복사해도 됩니다. 이 스킬은 오픈 [Agent Skills](https://agentskills.io) 표준을 따르므로 Claude Code, Codex, 그리고 SKILL.md를 읽는 모든 에이전트에서 동작합니다.

**기타 에이전트 (Cursor, Gemini CLI, GitHub Copilot 등 skills CLI가 지원하는 에이전트):**

```bash
npx skills add jack-reson8/post-skill
```

## 내장된 정직 규칙
사실만 사용합니다. 대화 목업은 실제 대화를 재구성한 것이며, 타인의 메시지, 결제, 좋아요, 조회수를 절대 위조하지 않습니다.

## 라이선스
MIT. UI 목업은 논평 성격의 게시물을 위해 서드파티 앱을 모방한 것이며, 이름과 상표는 각 소유자에게 있습니다.

만든 사람 [@jack-reson8](https://github.com/jack-reson8) · 자매 스킬: [pro-motion](https://github.com/jack-reson8/pro-motion), [skill-skill](https://github.com/jack-reson8/skill-skill)
