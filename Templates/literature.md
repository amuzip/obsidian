---
# === 템플릿 메타데이터 ===
type: template
target: literature
status: approved
version: 1.2.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter ===
type: literature
status: active
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
source: ""
author: ""
# tags: [literature]
---

# <% tp.file.title %>

## 저자의 주장
<!-- 객관적 요약. 내 해석은 금지 (해석은 Permanent 노트에서) -->
<% tp.file.cursor(1) %>

## 인용 (필수)
<!-- 원문 그대로. 페이지/타임스탬프 명시 -->
>

## 출처
- Source:
- Author:

## 관련 노트
<!-- Literature는 관계를 frontmatter(related)로 정의하지 않음. 본문 링크만 사용 -->
- [[]]
