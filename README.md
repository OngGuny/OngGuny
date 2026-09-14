## 손용균 (OngGuny)

백엔드 엔지니어입니다. LLM 플랫폼, RAG 파이프라인, 데이터 수집·추천 시스템을 설계부터 배포까지 만들어 왔습니다.
Python/FastAPI가 주력이고, 필요하면 프론트엔드와 인프라까지 직접 맡습니다.

- 메가존(주) Tech Platform, 2023.06 ~
- 관심사: LLM 운영 통제(거버넌스·감사), RAG 품질, 폐쇄망 환경 설계
- 고객사 프로젝트 소스는 보안 정책상 비공개입니다. 아래는 설계 경험 요약입니다.

---

### 기술 스택

| 분류 | 내용 |
|---|---|
| Backend | Python 3.13, FastAPI, Pydantic v2, SQLAlchemy 2.0 (Async), Alembic, Celery, WebSocket, Java 17, Spring Boot |
| Frontend | React 19, TypeScript (strict), Ant Design, Vite, React Hook Form + Zod |
| Database | PostgreSQL, Aurora PostgreSQL, pgvector, Redis (ElastiCache), MySQL, Oracle |
| AI / LLM | AWS Bedrock, Azure OpenAI, OpenAI API, Google Gemini, Anthropic Claude, LangChain, Ollama, RAG, 벡터 검색 |
| Cloud / Infra | AWS (Lambda, API Gateway, Secrets Manager, CloudWatch, S3, SSM, IAM), Azure, Docker, nginx, systemd, Jenkins, GitLab CI |
| AI 코딩 | Claude Code (에이전틱 코딩, CLAUDE.md 컨텍스트 관리, Custom Skill · Slash Command 설계) |

---

### 설계 경험

**생성형 AI 거버넌스 플랫폼** — 금융권, 폐쇄망

사내 AI 서비스와 LLM 사이의 보안 관문과, 이를 통제·감사하는 관리자 콘솔.
2인 팀에서 관리자 콘솔을 요구사항 해석부터 설계·백엔드·프론트엔드·배포까지 단독으로 맡았습니다.

- PII 탐지·차단·마스킹 정책 설계. 입력과 출력 방향을 나눈 이벤트 코드 체계, 로깅 전용 유형의 마스킹 면제 처리
- 서비스·모델·이용자·전역 4개 축 킬스위치, 토큰·호출 한도 집행
- 한도 확인은 매 요청 DB를 조회하면 I/O 부하가 커져 Redis 캐시로 설계하고, Redis 장애 시 DB 폴백으로 가용성을 확보
- 자체 JWT 인증(계정 잠금, IP allowlist, OTP), 역할 기반 RBAC, API Key 라이프사이클, 관리자 활동 전수 감사
- 인터넷이 차단된 폐쇄망의 반입·배포를 단독 수행. 오프라인 wheelhouse 빌드, lock 파일 기반 빌드, 회차별 팩·zip SHA256 매니페스트 자동 생성
- 정적분석(SAST) 통과가 배포 게이트인 환경에서 SQL 전량 ORM·바인드 파라미터 처리, 보안 응답 헤더·CORS 화이트리스트 적용
- 아키텍처 의사결정을 ADR로 문서화해 감리·심의 대응 근거 확보

**글로벌 산업 뉴스 수집 및 추천 시스템** — PoC부터 납품까지

4개 언어 뉴스와 경쟁사·리서치 기관 리포트를 매일 수집해 중복을 제거하고 중요 기사를 추천.

- GPU가 없고 외부 API 비용 제약이 있어 Ollama 로컬 다국어 임베딩(1024차원)을 쓰고 pgvector(HNSW)로 유사도 검색
- 중복 제거는 제목 임베딩으로 후보를 좁힌 뒤 본문 길이 비율과 본문 유사도로 확정하고, 언론사 신뢰도로 대표 기사를 선정
- 3축 기준 임베딩과의 유사도 분류에 Random Forest 품질 점수를 결합해 중요도 산출
- 추천 품질을 눈으로 확인하려고 평가·피드백 API와 Precision@K 집계를 붙이고, 검수용 대시보드를 프론트엔드까지 직접 구현
- Playwright 동적 수집, 리다이렉트 원본 URL 보존, 수집 이전 단계의 실시간 중복 검사

**RAG 기반 지식관리 시스템** — 문서 검색·질의응답

- 답변 생성 후 LLM 구조화 출력으로 실제 참조한 페이지를 판별해 출처로 저장. WebSocket으로 출처를 내려주고 원문 조회 API 제공
- 인제스트 결과를 사용자가 페이지·표 단위로 고치면 임베딩을 재생성하고 원본 복원도 가능하게 설계
- PPTX는 headless LibreOffice로 PDF 변환 후 인제스트. 이미지 업로드·요약 추가
- 사용자별 LLM API 키 관리와 Redis 기반 모델 캐시, 멀티 LLM(GPT·Gemini·Claude) 확장

---

### AI를 개발에 쓰는 방식

Claude Code 기반 에이전틱 코딩을 전 프로젝트에 상시 적용합니다. 코드를 대신 써주는 도구가 아니라, 맥락을 공유하는 작업 상대로 씁니다.

- `CLAUDE.md`에 프로젝트 구조·컨벤션·의사결정 맥락을 적어 세션이 바뀌어도 같은 기준으로 작업하게 합니다
- 보안 컨벤션(KISA 시큐어코딩 기준, 비밀값 하드코딩 금지)을 먼저 명문화해 코드 생성 단계부터 심의 기준을 반영합니다
- 추측 금지 규칙을 두고, 동작 테스트로 검증한 것만 받아들입니다
- 의사결정·작업완료·문제해결·설계변경 4개 트리거로 작업 로그를 자동 기록하는 Custom Skill을 직접 설계했고, Slash Command로 취합해 일일 보고서를 만듭니다. 7일 경과 로그 압축과 월간 요약까지 라이프사이클을 관리합니다

---

### 개인 프로젝트

- **greedy_T_bot** — 국내 주식 자동매매 봇
- **copy_voca** — Flutter 단어장 앱
- **Vue-ShoppingMall** — Vue.js 학습용 쇼핑몰

---

<sub>고객사명과 구체적인 수치는 보안상 생략했습니다. 상세 이력은 이력서로 전달드립니다.</sub>
