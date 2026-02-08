대표님의 연구 분야(해양천연물 화학, 신약개발, 생물정보학)와 현재 워크플로우(Obsidian, 데이터 분석, 보고서 생성)를 기반으로 MCP 서버를 추천함.

---

## Tier 1 — 즉시 연결 권장 (핵심 생산성)

|순위|MCP 서버명|활용법|대표님 업무 연관성|
|---|---|---|---|
|1|**Obsidian MCP**|Obsidian 볼트 직접 읽기/쓰기, 노트 검색, 태그 관리, PARA 폴더 자동 분류|현재 PARA 기반 지식관리 시스템의 핵심 연동|
|2|**GitHub MCP**|코드 저장소 관리, 이슈 트래킹, 코드 검색, PR 관리|분석 스크립트/대시보드 코드 버전 관리|
|3|**Google Drive MCP**|이미 연결됨 ✅ — Google Docs/Sheets 검색 및 문서 접근|공동연구 문서, 보고서 공유|
|4|**Slack MCP**|채널 메시지 검색, 알림, 팀 커뮤니케이션 자동화|연구팀/사업개발팀 소통 (사용 중인 경우)|

## Tier 2 — 연구 효율 극대화

|순위|MCP 서버명|활용법|대표님 업무 연관성|
|---|---|---|---|
|5|**Puppeteer MCP**|헤드리스 브라우저 자동화, 웹 스크래핑, 자동 로그인 후 데이터 수집|PubChem, ChEMBL, KEGG 등 화학DB 자동 크롤링|
|6|**PostgreSQL/SQLite MCP**|로컬 DB 직접 쿼리, 데이터 삽입/조회/분석|245개 화합물 데이터, 194,143 생물활성 데이터 DB화|
|7|**Notion MCP**|Notion 페이지/DB 읽기쓰기, 프로젝트 관리|Obsidian 대체 또는 병행 시 활용|
|8|**Memory MCP (Anthropic 공식)**|대화 간 장기 메모리 저장, 엔티티 기반 지식 그래프 구축|화합물-타겟-질환 관계 맵 누적 저장|

## Tier 3 — 전문 분석 확장

|순위|MCP 서버명|활용법|대표님 업무 연관성|
|---|---|---|---|
|9|**Brave Search MCP**|웹 검색 API 직접 호출, 논문/특허 검색 자동화|경쟁사 특허, 최신 논문 자동 모니터링|
|10|**Exa MCP**|시맨틱 검색 — 의미 기반으로 논문/웹페이지 검색|"사르코페니아 해양유래 치료제" 같은 복합 검색에 강점|
|11|**Arxiv/PubMed MCP**|논문 검색, 초록 추출, 인용 관리|해양천연물 신약개발 문헌 조사 자동화|
|12|**Docker MCP**|컨테이너 기반 분석 환경 관리, 재현 가능한 파이프라인|RDKit, PASS 예측 도구 등 분석환경 격리 실행|

## Tier 4 — 사업개발(BD) 지원

|순위|MCP 서버명|활용법|대표님 업무 연관성|
|---|---|---|---|
|13|**Google Sheets MCP**|스프레드시트 직접 읽기/쓰기, 재무모델 자동 업데이트|바이오텍 기업분석, 재무 시뮬레이션|
|14|**Gmail MCP**|이메일 검색, 자동 분류, 드래프트 작성|BD 파트너십 커뮤니케이션 관리|
|15|**Calendar MCP**|일정 조회/생성, 미팅 관리|연구 마일스톤, BD 미팅 관리|

---

## 설치 우선순위 로드맵

**Phase 1 (이번 주)** — Obsidian MCP + GitHub MCP

- 즉시 체감 효과가 가장 큼. Obsidian 볼트를 Claude가 직접 읽고 쓰면서 PARA 자동 분류 가능

**Phase 2 (1~2주 내)** — SQLite MCP + Puppeteer MCP

- 화합물 데이터를 로컬 DB로 구조화하고, 화학DB 자동 크롤링 파이프라인 구축

**Phase 3 (한 달 내)** — Exa MCP + Memory MCP + Brave Search MCP

- 시맨틱 검색 기반 문헌조사 자동화, 장기 지식 그래프 구축

**Phase 4 (필요 시)** — Gmail/Calendar/Sheets MCP

- BD 업무량이 증가할 때 도입

---

## 설치 방법 참고

대부분의 MCP 서버는 Claude Desktop 앱의 `claude_desktop_config.json` 파일에 설정을 추가하는 방식으로 연결함. 예시:

json

```json
{
  "mcpServers": {
    "obsidian": {
      "command": "npx",
      "args": ["-y", "obsidian-mcp"],
      "env": {
        "OBSIDIAN_VAULT_PATH": "C:/Users/대표/ObsidianVault"
      }
    }
  }
}
```

특정 MCP 설치를 진행하고 싶으면 바로 가이드 가능함.

---

**B-Q1.** Obsidian MCP 연결 후 PARA 폴더 자동 분류 규칙을 설계하고 즉시 구현하는 작업을 진행할까요?

**B-Q2.** SQLite MCP를 활용하여 245개 해양 화합물 데이터를 관계형 DB로 구조화하는 스키마 설계를 수행할까요?

**B-Q3.** Puppeteer MCP 기반 PubChem/ChEMBL 자동 크롤링 파이프라인의 기술적 타당성을 검토할까요?

**B-Q4.** Exa MCP의 시맨틱 검색을 활용한 사르코페니아 해양천연물 문헌조사 자동화 워크플로우를 설계할까요?

**B-Q5.** 현재 연결된 MCP(Desktop Commander, Filesystem, Chrome, Google Drive)의 통합 활용 시나리오를 수립할까요?
