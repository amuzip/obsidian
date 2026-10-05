---
# === 템플릿 메타데이터 ===
type: template
target: permanent
status: approved
version: 1.2.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter ===
type: permanent
status: active
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
tags: []
related: []
---

# <% tp.file.title %>

## 주장 (One Idea per Note)
<!-- 하나의 명확한 주장만. 제목이 곧 주장이 되도록 -->
<% tp.file.cursor(1) %>

## 근거 / 전개
<!-- 내 언어로 재구성. 저자 요약이 아님 -->

## 연결 (최소 2개 이상)
<!-- related[] 필드와 본문 링크를 함께 유지 -->
- [[]]
- [[]]

## 발전 방향
<!-- 시간을 두고 정제. 내용적 변화 시에만 updated 갱신 -->
