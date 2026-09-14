<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:1F3864,50:2E5C9A,100:4A90D9&height=200&section=header&text=OngGuny&fontSize=70&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=AI%20Native%20Backend%20Engineer&descAlignY=55&descSize=20" />

<br/>

**LLM 플랫폼 · RAG 파이프라인 · 데이터 수집 시스템을 설계부터 배포까지**

<br/>

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white" />

<br/><br/>

<a href="mailto:oongguny@gmail.com"><img src="https://img.shields.io/badge/oongguny@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
<img src="https://img.shields.io/badge/Seoul,%20KR-1F3864?style=flat-square&logo=googlemaps&logoColor=white" />
<img src="https://img.shields.io/badge/AWS%20Certified%20AI%20Practitioner-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white" />

</div>

<br/>

```python
class OngGuny:
    def __init__(self):
        self.role    = "Backend Engineer"
        self.company = "메가존(주) · AI & Core Tech Lab"  # 2023.06 ~
        self.focus   = ["LLM 운영 통제 (거버넌스 · 감사)",
                        "RAG 품질",
                        "폐쇄망(air-gapped) 환경 설계"]

    def how_i_work(self):
        return "필요하면 프론트엔드와 인프라까지 직접 맡습니다"
```

<br/>

<div align="center">

## 🛠 Tech Stack

</div>

<table>
<tr>
<td valign="top" width="50%">

**Backend**

![Python](https://img.shields.io/badge/Python%203.13-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic%20v2-E92063?style=flat-square&logo=pydantic&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy%202.0%20Async-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white)
![Java](https://img.shields.io/badge/Java%2017-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React%2019-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript%20strict-3178C6?style=flat-square&logo=typescript&logoColor=white)
![AntDesign](https://img.shields.io/badge/Ant%20Design-0170FE?style=flat-square&logo=antdesign&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

</td>
<td valign="top" width="50%">

**AI / LLM**

![Bedrock](https://img.shields.io/badge/AWS%20Bedrock-232F3E?style=flat-square&logo=amazonwebservices&logoColor=FF9900)
![OpenAI](https://img.shields.io/badge/Azure%20OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)

**Data / Infra**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Lambda](https://img.shields.io/badge/AWS%20Lambda-FF9900?style=flat-square&logo=awslambda&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)

</td>
</tr>
</table>

<br/>

<div align="center">

## 🏗 Architecture Experience

<sub>고객사 프로젝트 소스는 보안 정책상 비공개입니다. 아래는 설계 경험 요약입니다.</sub>

</div>

<br/>

<details open>
<summary><b>🔐 생성형 AI 거버넌스 플랫폼</b> &nbsp;<code>금융권</code> <code>폐쇄망</code> <code>2인 팀</code></summary>

<br/>

> 사내 AI 서비스와 LLM 사이의 보안 관문, 그리고 이를 통제·감사하는 관리자 콘솔.
> **관리자 콘솔은 요구사항 해석부터 설계·백엔드·프론트엔드·배포까지 단독으로 맡았습니다.**

| 영역 | 한 일 |
|:--|:--|
| **PII 통제** | 탐지·차단·마스킹 **정책 설계**. 입력/출력 방향을 나눈 이벤트 코드 체계, 로깅 전용 유형의 마스킹 면제 처리 |
| **운영 통제** | 서비스·모델·이용자·전역 **4개 축 킬스위치**, 토큰·호출 한도 집행 |
| **성능 판단** | 한도 확인을 매 요청 DB 조회하면 I/O 부하가 커져 **Redis 캐시로 설계**, Redis 장애 시 **DB 폴백**으로 가용성 확보 |
| **인증·권한** | 자체 JWT(계정 잠금 · IP allowlist · OTP), 역할 기반 RBAC, API Key 라이프사이클, 관리자 활동 전수 감사 |
| **폐쇄망 배포** | 인터넷 차단 환경의 **반입·배포 단독 수행**. 오프라인 wheelhouse 빌드, lock 파일 기반 빌드, 회차별 팩·zip SHA256 매니페스트 자동 생성 |
| **보안 게이트** | 정적분석(SAST) 통과가 배포 조건인 환경 — SQL 전량 ORM·바인드 파라미터, 보안 응답 헤더·CORS 화이트리스트 |
| **의사결정 기록** | 아키텍처 의사결정을 **ADR로 문서화**해 감리·심의 대응 근거 확보 |

</details>

<details>
<summary><b>📰 글로벌 산업 뉴스 수집 및 추천 시스템</b> &nbsp;<code>PoC → 납품</code> <code>개발 단독</code></summary>

<br/>

> 4개 언어 뉴스와 경쟁사·리서치 기관 리포트를 매일 수집해 중복을 제거하고 중요 기사를 추천.

```
수집 (Playwright · RSS)  →  임베딩 (Ollama 로컬 · 1024d)  →  중복 제거  →  분류 · 스코어링  →  대시보드
```

- **제약이 설계를 결정했습니다.** GPU가 없고 외부 API 비용 제약이 있어 로컬 다국어 임베딩을 쓰고 `pgvector(HNSW)`로 유사도 검색
- **중복 제거 3단계** — 제목 임베딩으로 후보를 좁히고 → 본문 길이 비율·본문 유사도로 확정 → 언론사 신뢰도로 대표 기사 선정
- **추천** — 3축 기준 임베딩과의 유사도 분류에 Random Forest 품질 점수를 결합해 중요도 산출
- **품질을 눈으로 보려고** 평가·피드백 API와 Precision@K 집계를 붙이고, 검수용 대시보드를 프론트엔드까지 직접 구현
- 리다이렉트 원본 URL 보존, 수집 이전 단계의 실시간 중복 검사

</details>

<details>
<summary><b>📚 RAG 기반 지식관리 시스템</b> &nbsp;<code>문서 검색 · 질의응답</code></summary>

<br/>

> 사내 문서를 올려 RAG로 검색·질의응답하는 시스템. 백엔드 기능 개발을 맡았습니다.

- **답변 출처 추적** — 답변 생성 후 LLM 구조화 출력으로 *실제 참조한* 페이지를 판별해 출처로 저장. WebSocket으로 내려주고 원문 조회 API 제공
- **인제스트 결과 보정** — 사용자가 페이지·표 단위로 고치면 임베딩을 재생성하고 원본 복원도 가능하게 설계
- **포맷 확장** — PPTX는 headless LibreOffice로 PDF 변환 후 인제스트, 이미지 업로드·요약 추가
- **멀티 LLM** — 사용자별 LLM API 키 관리, Redis 기반 모델 캐시, GPT · Gemini · Claude 확장

</details>

<br/>

<div align="center">

## 🤖 AI Native — AI를 개발에 쓰는 방식

</div>

> **코드를 대신 써주는 도구가 아니라, 맥락을 공유하는 작업 상대로 씁니다.**

<table>
<tr><td width="50%" valign="top">

**컨텍스트를 관리합니다**

`CLAUDE.md`에 프로젝트 구조 · 컨벤션 · 의사결정 맥락을 적어 세션이 바뀌어도 같은 기준으로 작업하게 합니다.

</td><td width="50%" valign="top">

**보안을 먼저 명문화합니다**

KISA 시큐어코딩 기준과 비밀값 하드코딩 금지를 사전에 규칙으로 박아 **코드 생성 단계부터** 심의 기준을 반영합니다.

</td></tr>
<tr><td width="50%" valign="top">

**추측을 금지합니다**

추측 금지 규칙을 두고, 동작 테스트로 검증한 것만 받아들입니다.

</td><td width="50%" valign="top">

**워크플로우를 직접 설계합니다**

의사결정 · 작업완료 · 문제해결 · 설계변경 4개 트리거로 작업 로그를 자동 기록하는 **Custom Skill을 직접 만들었습니다.** Slash Command로 취합해 일일 보고서를 생성하고, 7일 경과 로그 압축과 월간 요약까지 라이프사이클을 관리합니다.

</td></tr>
</table>

<br/>

<div align="center">

## 📦 Side Projects

<table>
<tr>
<td align="center" width="33%">

**greedy_T_bot**

<sub>국내 주식 자동매매 봇</sub>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

</td>
<td align="center" width="33%">

**copy_voca**

<sub>단어장 앱</sub>

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)

</td>
<td align="center" width="33%">

**Vue-ShoppingMall**

<sub>학습용 쇼핑몰</sub>

![Vue](https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)

</td>
</tr>
</table>

<br/><br/>

<img src="https://github-readme-stats.vercel.app/api?username=OngGuny&show_icons=true&hide_border=true&title_color=1F3864&icon_color=4A90D9&bg_color=00000000" height="150" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=OngGuny&layout=compact&hide_border=true&title_color=1F3864&bg_color=00000000" height="150" />

<br/><br/>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:4A90D9,50:2E5C9A,100:1F3864&height=120&section=footer" />

</div>
