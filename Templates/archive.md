---
# === 템플릿 메타데이터 ===
type: template
target: archive
status: approved
version: 1.0.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter ===
type: archive
status: archived
original_folder: "1. Projects"
archived_date: <% tp.date.now("YYYY-MM-DD") %>
# completed_date:

# 복귀(회귀) 범위
return_candidates: ["1. Projects", "2. Areas", "3. Resources", "5. Zettelkasten"]
return_target: "1. Projects"
recyclable: yes
tags: [archive/project]
---

# <% tp.file.title %>

## 보관 사유
<!-- 왜 Archive로 이동했는가? -->
<% tp.file.cursor(1) %>

## 원본 정보
- Original folder: [[1. Projects/]]
- Archived: <% tp.date.now("YYYY-MM-DD") %>

## 복귀 계획
- 복귀 대상:
- 재활용 가능 여부:
- 복귀 시점:
