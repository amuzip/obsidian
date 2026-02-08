# NotebookLM MCP 사용 가이드

## 개요
NotebookLM MCP는 Claude Code에서 Google NotebookLM과 연동하여 문서 기반 질의응답을 할 수 있게 해주는 도구입니다.

## 연결 상태 확인
```
mcp__notebooklm__get_health
```
- authenticated: true 확인
- status: ok 확인

## 주요 기능

### 노트북 관리
| 기능 | 설명 |
|------|------|
| `add_notebook` | 새 노트북을 라이브러리에 추가 |
| `list_notebooks` | 저장된 노트북 목록 조회 |
| `get_notebook` | 특정 노트북 상세 정보 조회 |
| `select_notebook` | 활성 노트북 설정 |
| `update_notebook` | 노트북 메타데이터 수정 |
| `remove_notebook` | 라이브러리에서 노트북 제거 |
| `search_notebooks` | 이름/주제/태그로 노트북 검색 |

### 질의 및 연구
| 기능 | 설명 |
|------|------|
| `ask_question` | NotebookLM에 질문하고 답변 받기 |

### 세션 관리
| 기능 | 설명 |
|------|------|
| `list_sessions` | 활성 세션 목록 조회 |
| `close_session` | 세션 종료 |
| `reset_session` | 세션 히스토리 초기화 |

### 인증 및 유지보수
| 기능 | 설명 |
|------|------|
| `setup_auth` | Google 계정 인증 설정 |
| `re_auth` | 재인증 (계정 전환, 한도 초과 시) |
| `cleanup_data` | 캐시/브라우저 데이터 정리 |

## 노트북 추가 방법
1. https://notebooklm.google 에서 노트북 생성
2. 문서/자료 업로드
3. **Share** 버튼 클릭 → "Anyone with the link" 선택
4. 링크 복사 후 Claude에게 공유

## 등록된 노트북

### 테스트 노트북
- **URL**: https://notebooklm.google.com/notebook/52a00787-1672-4a56-89ab-abfcca20c9b9
- **설명**: 테스트용 노트북
- **주제**: 테스트
- **용도**: 기능 테스트
- **포함 문서**:
  - NotebookLM MCP Installation Instructions (영문)
  - NotebookLM MCP 설치 및 설정 방법 (한글)

## 제한사항
- NotebookLM 계정의 전체 노트북 목록 자동 조회 불가
- 각 노트북 URL을 수동으로 추가해야 함
- 세션 종료 시 대화 기록은 사라짐 (영구 저장 안 됨)

## 참고
- NotebookLM 무료 계정: 100개 노트북, 50개 소스/노트북, 50회 일일 쿼리
- Google AI Pro/Ultra: 5배 높은 한도

---
*작성일: 2026-02-05*
