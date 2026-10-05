---
# === 템플릿 메타데이터 ===
type: template
target: project
status: approved
version: 1.2.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter ===
type: project
status: todo
due: <% tp.date.now("YYYY-MM-DD", 7) %>
# area: <% tp.file.cursor(1) %>
# tags: []
---

# <% tp.file.title %>

## 목표(Outcome)
<!-- 이 프로젝트가 완료되면 무엇을 달성하는가? -->
<% tp.file.cursor(2) %>

## 배경
<!-- 왜 이 프로젝트를 시작했는가? -->

## 완료 기준(Definition of Done)
- [ ] <% tp.file.cursor(3) %>

## 범위/비범위
- **In scope:**
- **Out of scope:**

## 마일스톤
- <% tp.date.now("YYYY-MM-DD", 7) %>:
- <% tp.date.now("YYYY-MM-DD", 14) %>:

## 리스크 & 대응
- 리스크: ... / 대응: ...

## 진행 로그
- <% tp.date.now("YYYY-MM-DD") %>:

## 참조
- [[2. Areas/]]
- 자료: [[]] · 문헌: [[]]
