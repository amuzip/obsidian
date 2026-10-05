---
# === 템플릿 메타데이터 ===
type: template
target: doc
status: approved
version: 1.0.0
compat:
  templater: ">=1.24.0"
  obsidian: ">=1.0.0"
changelog_url: "[[Templates/CHANGELOG]]"
superseded_by: ""
# ===============================================

# === 실제 노트 Frontmatter ===
# 필수 (4개)
title: "<% tp.file.title %>"
doc_type: "policy|procedure|howto|reference|decision"
updated: '<% tp.date.now("YYYY-MM-DD") %>'
owner: "kamwoo"

# 권장 (5개) - 문맥 확보용
summary: "<1-2문장 요약>"
scope: "<적용 범위>"
audience: "본인|팀|전사"
keywords: []
related: []

# 선택 (필요시에만)
# status: "active"
# version: "1.0.0"
# notes: "<짧은 주석>"
---

# <% tp.file.title %>

## 개요
<% tp.file.cursor(1) %>

## 내용

## Changelog
<!-- 최대 5개 항목만 유지. 무엇을 + 왜를 1줄로 -->
- <% tp.date.now("YYYY-MM-DD") %>: 문서 최초 작성
