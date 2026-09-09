# 🎓 2026 캡스톤 디자인: 사내 지식 통합 RAG 및 업무 자동화 어시스턴트

> **프로젝트 한 줄 소개:** 사내 문서 기반의 신뢰성 있는 지능형 검색(RAG) 및 회의 음성 기반 액션아이템 자동 도출 에이전트

## 1. 프로젝트 개요 (Introduction)
* **개발 배경:** 기업 내 분산된 문서로 인한 정보 탐색 비용을 줄이고, 범용 LLM 도입 시 발생하는 환각 현상(Hallucination)을 방지하기 위해 기획되었습니다. 또한 수기 회의록 작성으로 인한 리소스 낭비와 업무 누락을 해결하고자 합니다.
* **목표:** 
  1. 사내 지식 자산을 통합한 **RAG(Retrieval-Augmented Generation) 어시스턴트** 구축
  2. 회의 음성(STT) 기반 **액션아이템 자동 추출 및 Slack 알림 에이전트** 개발
* **개발 기간:** 2026.03 ~ 2026.06 (예정)

## 2. 팀원 소개 (Team Members)
| 이름 | 담당 | 수행 역할 | GitHub |
|---|---|---|---|
| 여태인 (팀장) | 아키텍처·RAG | 아키텍처 설계, 사내 문서 RAG 파이프라인 및 백엔드 API 개발 | [@github-id](링크) |
| 예성호 (팀원) | 회의록 AI·파이프라인 | AI·파이프라인 Whisper STT 연동, 액션아이템(JSON) 추출 및 Slack 알림 구현 | [@github-id](링크) |
| 김동현 (팀원) | UI/UX·프론트엔드 | 선행 도구 UI 조사, React 기반 대시보드 및 출처 뷰어 개발 | [@donghyun3471](https://github.com/donghyun3471) |
| 허지량 (멘토) | 실무 검증·멘토링 | 프로젝트 실무 검증 및 기술 멘토링 지원 | - |

## 3. 기술 스택 (Tech Stack)
### AI / Data Pipeline
* LLM & STT: GPT-4o, Whisper
* Vector DB: ChromaDB
### Backend
* (Python / FastAPI / Spring Boot 등 실제 사용할 백엔드 스택 기입)
### Frontend
* React
### Infra & Integration
* Slack API

## 4. 주요 기능 (Key Features)
* **지능형 사내 문서 검색 (RAG):**
  * 규정집, 매뉴얼, 기획서 등 다양한 비정형 문서(PDF, DOCX)의 벡터화 및 보관
  * 자연어 질의에 대한 신뢰성 있는 답변 및 명확한 출처(페이지 번호 등) 실시간 제공
* **회의 액션아이템 추출 및 알림 자동화:**
  * 회의 음성을 STT(Speech-to-Text)로 텍스트화 및 핵심 내용 요약
  * 담당자 및 기한이 명시된 액션아이템(Action Item) 자동 도출
  * Slack API와 연동하여 담당자에게 엔드투엔드(End-to-End) 자동 알림 전송

## 5. 설치 및 실행 방법 (Getting Started)
```bash
# 1. 저장소 클론
$ git clone [https://github.com/donghyun3471/2026_capstonedesign_sssoft.git](https://github.com/donghyun3471/2026_capstonedesign_sssoft.git)

# 2. 디렉토리 이동
$ cd 2026_capstonedesign_sssoft

# 3. 환경 변수 설정 (.env)
# OPENAI_API_KEY, SLACK_BOT_TOKEN 등 설정 필요

# 4. 프론트엔드 패키지 설치 및 실행 (예시)
$npm install
$npm start
```
