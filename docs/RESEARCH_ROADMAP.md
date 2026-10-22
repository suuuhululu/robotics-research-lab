# Research Roadmap

## 1. 운영 원칙

이 문서는 기존 경험에서 출발한 연구 질문과 향후 습득할 기술을 연결합니다.

R01~R09는 모두 연구 백로그입니다.
기존 프로젝트의 사용 기술이나 참여 경험을 이 저장소의 연구 완료로 표시하지 않습니다.

- 초기 활성 실험 수는 1개로 제한합니다.
- 첫 착수 후보는 R01입니다.
- 카메라나 실제 로봇을 사용할 수 없으면 R05의 순수 기하 알고리즘을 먼저 검토합니다.
- 장비 접근성, 포트폴리오 가치, 구현 난이도에 따라 순서를 변경할 수 있습니다.
- 주제별 폴더와 Issue를 한꺼번에 생성하지 않습니다.
- Baseline, 허용 오차, 합격 기준은 각 실험 착수 전에 정합니다.

## 2. 우선순위와 진행 단계

P1~P3는 연구 분야의 우선순위를 나타냅니다.
Phase는 연구 방향과 선행관계를 나타내며, 모든 주제를 순서대로 완료하는 관문은 아닙니다.

| Phase | 방향 | 예정 범위 |
|---|---|---|
| Phase 0 — Research Foundation | 연구 기반 정리 | 네 문서, 프로젝트 기여도 원장, Issue·PR 운영 방식 |
| Phase 1 — Practical Robotics Experiments | 실용적인 독립 실험 | R01, R05, R02 |
| Phase 2 — System & Algorithm Evaluation | 시스템·알고리즘 비교 | R06, R07, R03 |
| Phase 3 — Advanced Robot Intelligence | 예측·학습 및 제어 연결 | R08, R09 |

R04는 P1 연구 주제이며, Phase 배치는 아직 지정하지 않았습니다.

| ID | 연구 주제 | 우선순위 | Phase | 상태 |
|---|---|---|---|---|
| R01 | RGB-D 기반 위치·기울기 오차 보정 | P1 | 1 | 백로그 |
| R02 | MoveIt 2 기반 장애물 회피 | P1 | 1 | 백로그 |
| R03 | LEGO 조립 상태 역산 | P1 | 2 | 백로그 |
| R04 | Contact-rich Manipulation | P1 | 미지정 | 백로그 |
| R05 | 2D 이미지 기반 3D 곡면 경로 생성 | P2 | 1 | 백로그 |
| R06 | Nav2 Controller 및 Localization 비교 | P2 | 2 | 백로그 |
| R07 | Isaac Sim 실행 및 Sim2Real 연구 | P2 | 2 | 백로그 |
| R08 | 움직이는 목표 추적과 예측 | P3 | 3 | 백로그 |
| R09 | Human Demonstration & Robot Learning | P3 | 3 | 백로그 |

## 3. P1 — Robot Manipulation & Perception

Co-Assembly에서 경험한 LEGO 조립의 정밀도와 실행 안정성 문제를 출발점으로 삼습니다.

### R01. RGB-D 기반 위치·기울기 오차 보정

- 연구 질문: 깊이·자세 추정과 좌표 변환 방법에 따라 로봇 작업 목표의 오차가 어떻게 달라지는가?
- 검증 범위: Depth 기반 깊이·자세 추정, 기하학적 기울기 추정, 평면 피팅, YOLO Segmentation 기반 ROI 비교.
- 연결 과정: 픽셀 좌표에서 로봇 좌표계로 변환하고 캘리브레이션 오차를 평가.
- 평가 항목: 위치 오차(mm), 각도 오차(°), 처리 지연(ms).
- 착수 전 결정: 정답값 취득 방법, 비교 조건, 입력 데이터, 허용 오차, 필요한 장비.

### R02. MoveIt 2 기반 장애물 회피

- 연구 질문: 장애물 표현과 배치 조건이 충돌 없는 경로계획에 어떤 영향을 주는가?
- 검증 범위: Point Cloud 기반 장애물 표현, Planning Scene 연결, 충돌 검사, OMPL 기반 경로계획.
- 비교 조건: 장애물 배치별 계획 결과.
- 평가 항목: 계획 성공률, 계산 시간, 최소 장애물 거리.

### R03. LEGO 조립 상태 역산

- 연구 질문: 관측한 블록 배치에서 조립 제약을 만족하는 설계를 얼마나 복원할 수 있는가?
- 검증 범위: 블록 종류·색상·위치·층별 상태와 연결 제약의 구조화.
- 방법 후보: 정수계획법(ILP), 제약충족 기법.
- 평가 항목: 설계 복원 정확도, 계산 시간, 모호한 관측 처리 능력.

### R04. Contact-rich Manipulation

- 연구 질문: 접촉 힘과 위치 오차가 정렬·결착의 안정성과 성공 여부에 어떤 영향을 주는가?
- 검증 범위: Cartesian Motion, Compliance Control, Force Control의 원리 재구현 및 검증.
- 비교 조건: 접촉 힘·위치 오차 조건별 정렬 및 결착 결과.
- 평가 항목: 접촉 안정성, 결착 성공률, 과도한 힘 발생 여부.
- 착수 전 결정: Phase 배치, 장비, 허용 힘·동작 범위, 중단 조건과 합격 기준.

## 4. P2 — Motion Planning, Navigation & Simulation

NetClean, AMR Patrol, Surface Carving에서 경험한 기술을 독립적인 실험으로 분리합니다.

### R05. 2D 이미지 기반 3D 곡면 경로 생성

- 연구 질문: 이미지 경로의 근사·샘플링 방식에 따라 곡면 경로의 정확도와 계산량이 어떻게 달라지는가?
- 검증 범위: Otsu 이진화, Skeletonization, Bézier 근사, 원통 매개변수 기반 2D→3D 매핑.
- 비교 조건: Fixed Sampling과 Adaptive Sampling.
- 평가 항목: 경로 근사 오차, Waypoint 수, 계산 시간.
- 실행 후보: 소프트웨어만으로 재현 가능한 순수 기하 실험.

### R06. Nav2 Controller 및 Localization 비교

- 연구 질문: Controller, 위치추정 파라미터, Costmap 설정이 주행 성능에 어떤 영향을 주는가?
- 검증 범위: DWB·MPPI 비교, AMCL 파라미터 변화, Inflation·Obstacle Layer·Keepout Filter 비교.
- 실험 분리: Controller, Localization, Costmap의 영향을 구분할 수 있도록 비교 단위를 정의.
- 평가 항목: 주행 성공률, 경로 길이, 주행 시간, 위치추정 오차.

### R07. Isaac Sim 실행 및 Sim2Real 연구

- 연구 질문: 실행 방식과 로봇·센서 설정이 재현성 및 시뮬레이션 동작에 어떤 영향을 주는가?
- 검증 범위: GUI·Python Standalone 비교, ROS 2 Bridge 연결, 물리·센서·좌표계 설정 검증.
- 평가 항목: 재현성, 시뮬레이션 성능, 메모리 사용량, 실물 동작과의 차이.
- 실험 분리: 실행 방식 비교와 실물 비교의 환경·결과·검증 상태를 구분.

## 5. P3 — Predictive Control & Robot Learning

중장기 독립 연구 분야입니다.

### R08. 움직이는 목표 추적과 예측

- 연구 질문: 관측 지연이 변할 때 움직이는 목표의 상태 추정과 미래 위치 예측이 얼마나 안정적인가?
- 검증 범위: Kalman Filter·EKF 기반 상태 추정, 컨베이어 물체의 위치·속도 예측.
- 평가 항목: 추적 오차, 미래 위치 예측 오차, 지연 변화에 대한 안정성.

### R09. Human Demonstration & Robot Learning

- 연구 질문: 인간 작업 시연을 로봇 학습과 제어에 연결하려면 어떤 데이터 구조와 인터페이스가 필요한가?
- 검증 범위: 카메라 기반 시연 데이터 구조화, Imitation Learning·Reinforcement Learning 적용 가능성 비교.
- 연결 연구: VLA 정책과 기존 로봇 제어 시스템의 인터페이스.
- 예정 산출물: 시연 데이터 구조, 시뮬레이션 검증, 향후 실물 적용을 위한 연결 방식.
- 착수 전 결정: 작업 범위, Baseline, 데이터, 정량 지표 및 합격 기준.

## 6. 착수 및 진행 기록

주제를 활성화할 때 하나의 구체적인 실험으로 범위를 줄입니다.

필수 기록:

- 주제 ID와 실험 ID
- 연구 질문·가설·범위
- Baseline 또는 기준 조건
- 입력 데이터와 실행 환경
- 평가 지표·허용 오차·완료 기준
- 관련 Issue·Milestone
- 구현·결과 PR 및 실행 결과 경로

작업 상태는 백로그 / 계획 / 진행 / 보류 / 완료로 관리합니다.
실험 완료, 목표 성능 달성, 재현 성공, 실물 검증은 별도 항목으로 기록합니다.

세부 완료·재현 기준은 [Research Method](RESEARCH_METHOD.md)를 따릅니다.

## 7. 변경 이력

우선순위·범위·평가 기준을 변경하면 날짜, 변경 내용, 이유, 관련 Issue를 기록합니다.

결과를 확인한 뒤 평가 기준을 변경한 경우에는 변경 전 기준과 변경 이유도 보존합니다.

| 날짜 | 변경 내용·이유 | 관련 기록 |
|---|---|---|
| 2026-10-22 | 사용자 확정 요구사항을 초기 문서에 반영. R01~R09는 백로그로 유지하고 R04의 Phase는 미지정으로 기록. | [Foundation Issue #1](https://github.com/suuuhululu/robotics-research-lab/issues/1) |
