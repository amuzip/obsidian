---
type: doc
status: approved
tags: [policy, templates]
---

# Templates CHANGELOG

> 템플릿 변경 이력 통합 관리. 레지스트리는 [[Templates/CLAUDE.md]] 참조.
> 버전 규칙: PATCH(오타/주석) · MINOR(섹션/선택 필드 추가) · MAJOR(필드 삭제/구조 변경 → 신규 템플릿 생성)

---

## 2026-10-05 - 템플릿 파일 실체화 (project/area/resource/literature/permanent/archive/docs)

### 변경 사항
- 레지스트리에 등재되어 있었으나 파일이 존재하지 않던 템플릿 7종을 생성
  - `project.md` v1.2.0 — `Templates/CLAUDE.md` §예시 템플릿 구조 사양 그대로 적용
  - `area.md` v1.0.0 — `2. Areas/CLAUDE.md` 프론트매터 및 본문 구조 사양 적용
  - `resource.md` v1.0.0 — `3. Resources/CLAUDE.md` 프론트매터 사양 적용 (Templater 미사용)
  - `literature.md` v1.2.0 — `Zettelkasten/CLAUDE.md` Literature 스키마 적용
  - `permanent.md` v1.2.0 — `Zettelkasten/CLAUDE.md` Permanent 스키마 적용
  - `archive.md` v1.0.0 — `4. Archive/CLAUDE.md` 사양 및 표준 ENUM 적용
  - `docs.md` v1.0.0 — `0. Docs/CLAUDE.md` 프론트매터 규칙 적용
- `CHANGELOG.md` 신규 생성

### 마이그레이션 가이드
- 기존 노트: 영향 없음 (신규 파일 추가만)
- 신규 노트: Templates 플러그인/Templater에서 해당 템플릿 사용 가능

### Breaking Changes
- 없음

### 미해결 (후속 과제)
- `project-hub.md` v1.1.0 — 레지스트리에 등재되어 있으나 본문 사양이 어느 지침에도 정의되지 않아 생성하지 않음
- 지침 문서의 `5. Zettelkasten/`, `6. Templates/`, `7. Attachments/` 경로 표기가 실제 폴더명(`Zettelkasten/`, `Templates/`, `Attachments/`)과 불일치 — 수정 보류 상태
- 템플릿 메타데이터와 실제 노트 Frontmatter가 단일 YAML 블록에 공존하는 사양상 `type` 키 중복 문제 (아래 주의 참조)

---

## 주의: `type` 키 중복

`Templates/CLAUDE.md` §예시 템플릿 구조 사양은 하나의 YAML 블록 안에
`type: template`(템플릿 메타데이터)과 `type: project`(실제 노트) 를 함께 두도록 정의한다.
YAML 중복 키는 파서에 따라 마지막 값이 채택되므로:

- `Templates/CLAUDE.md` 의 Dataview 검증 대시보드(`WHERE type = "template"`)가 템플릿을 집계하지 못할 수 있음
- Templater 삽입 시 템플릿 메타데이터가 생성된 노트에 그대로 복사됨

현재 파일들은 **사양에 충실하게** 작성되어 있다. 해소 방안(택1, 미결정):
1. 템플릿 메타데이터를 YAML 주석 또는 본문 하단 섹션으로 이동
2. 템플릿 파일을 `tpl-{target}.md` 로 분리하고 메타데이터만 보유, 삽입 본문은 별도 블록으로 관리
