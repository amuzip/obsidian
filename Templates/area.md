---
# === 템플릿 메타데이터 ===
type: template
target: area
status: approved
version: 1.0.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter ===
type: area
status: active
# review_cycle: monthly
# tags: [area/operations]
---

# <% tp.file.title %>

## 목적
<!-- 이 영역이 담당하는 책임과 역할 -->
<% tp.file.cursor(1) %>

## 현황
<!-- 현재 상태, 주요 지표, KPI 등 -->

## 관련 프로젝트 (자동 집계)
```dataview
table status, due
from "1. Projects"
where contains(area, this.file.name)
sort due asc
```

## 리뷰 로그
- <% tp.date.now("YYYY-MM-DD") %>:

## 참조
- [[3. Resources/관련자료]]
- [[Zettelkasten/관련노트]]
