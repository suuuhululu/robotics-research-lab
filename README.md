# Robotics Research Lab

Independent robotics R&D through focused experiments, quantitative evaluation, and reproducible research.

기존 프로젝트에서 경험한 기술적 문제를 독립적인 실험으로 분리하여
재구현·비교·개선하고, 그 과정과 결과를 기록하는 개인 로보틱스 연구 저장소입니다.

## Purpose

취업 포트폴리오와 장기적인 로보틱스 연구 역량을 50:50의 목표로 발전시킵니다.

각 연구는 다음 흐름을 추적할 수 있도록 기록합니다.

문제와 배경 → 연구 질문 → 검증 방법 → 비교 결과 → 해석과 한계 → 재현 정보

기존 프로젝트 전체의 복제보다 범위가 명확한 실험을 우선합니다.
기존 경험과 구현은 참여 범위와 근거를 정리하여 기록하며,
새로운 연구 질문이 있을 때 재구현·비교·개선 실험으로 연결합니다.

## Current Status

현재는 Phase 0 — Research Foundation 단계입니다.

- 저장소 소개, 연구 로드맵, 개인 기여도 원장, 연구 방법론을 정리합니다.
- R01~R09는 연구 백로그입니다.
- 개별 주제의 실험 완료나 성능·재현 검증 결과는 아직 등록하지 않았습니다.
- 기존 프로젝트 경험과 이 저장소에서 새롭게 수행한 연구를 구분합니다.

문서 기반 정리는 [Issue #1](https://github.com/suuuhululu/robotics-research-lab/issues/1)과
[Phase 0 Milestone](https://github.com/suuuhululu/robotics-research-lab/milestone/1)에서 추적합니다.

## Research Areas

| 우선순위 | 분야 | 연구 백로그 |
|---|---|---|
| P1 | Robot Manipulation & Perception | R01 RGB-D 오차 보정, R02 MoveIt 2 장애물 회피, R03 LEGO 조립 상태 역산, R04 Contact-rich Manipulation |
| P2 | Motion Planning, Navigation & Simulation | R05 곡면 경로 생성, R06 Nav2·Localization 비교, R07 Isaac Sim·Sim2Real |
| P3 | Predictive Control & Robot Learning | R08 추적·예측, R09 Human Demonstration·Robot Learning |

세부 질문, 방법 후보, 평가 항목은
[연구 로드맵](docs/RESEARCH_ROADMAP.md)에서 관리합니다.

## Working Principles

- 초기에는 활성 실험을 1개로 제한합니다.
- 첫 착수 후보는 R01 Depth 기반 위치·기울기 보정입니다.
- 카메라나 실제 로봇을 사용할 수 없으면 R05의 순수 기하 알고리즘을 먼저 검토합니다.
- 연구 순서는 장비 접근성, 포트폴리오 가치, 구현 난이도에 따라 조정합니다.
- 실험별 독립 실행을 우선하며, 공통 모듈은 필요할 때 추출합니다.
- 기존 경험을 기록하기 위해 모든 기술을 다시 구현하도록 요구하지 않습니다.
- 실험 완료, 목표 성능 달성, 재현 성공, 실물 검증을 각각 기록합니다.

## Documentation

| 문서 | 내용 |
|---|---|
| [Research Roadmap](docs/RESEARCH_ROADMAP.md) | 연구 질문, 우선순위, 진행 단계, 평가 항목 |
| [Contributions](docs/CONTRIBUTIONS.md) | 기존 프로젝트의 개인 참여 범위와 근거 |
| [Research Method](docs/RESEARCH_METHOD.md) | 실험 설계, 환경, 결과 기록, 재현 및 GitHub 운영 규칙 |

현재 문서와 GitHub 템플릿 구조:

```text
.
├── README.md
├── docs/
│   ├── RESEARCH_ROADMAP.md
│   ├── CONTRIBUTIONS.md
│   └── RESEARCH_METHOD.md
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── research.md
    │   └── experiment.md
    └── pull_request_template.md
```

구현·데이터·결과 경로는 해당 실험을 시작할 때 추가합니다.

## Research Records

- [Issues](https://github.com/suuuhululu/robotics-research-lab/issues): 연구 질문, 범위, 완료 기준, 진행 중 판단.
- [Milestones](https://github.com/suuuhululu/robotics-research-lab/milestones): 관련 작업의 묶음과 산출물.
- [Pull Requests](https://github.com/suuuhululu/robotics-research-lab/pulls): 문서·구현·설정·결과의 변경 및 검증 이력.
- 실험 결과 문서: 실행 조건, 정량 결과, 해석, 한계, 재현 정보.

개인 기여는 사용자 진술과 확인된 자료를 구분하여 기록합니다.
팀 산출물의 존재나 Git 커밋 작성자만으로 개인 기여 범위를 확정하지 않습니다.

## Language

README는 영어 제목·소개와 한국어 설명을 병행합니다.
연구 문서는 한국어 중심으로 작성하고 논문명·알고리즘명은 원문을 유지합니다.

코드·함수·변수명은 영어를 사용합니다.
Issue·PR 제목은 영어 기술 키워드와 필요한 한국어 설명을 조합합니다.
핵심 실험에는 추후 영어 요약을 추가할 수 있습니다.
