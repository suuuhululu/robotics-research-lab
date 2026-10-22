# Contributions

## 1. 목적과 기록 범위

기존 팀 프로젝트에서의 개인 참여 범위와 근거를 기록합니다.

공식 역할 분담과 실제 참여 내용을 함께 보존합니다.
담당 범위를 넘어 참여한 구현·통합·시험도 구체적인 작업 단위로 기록합니다.

기존 경험은 재구현 여부와 별개로 기록할 수 있습니다.
이 저장소에서 새롭게 수행하는 독립 연구는 기존 프로젝트 참여 기록과 구분합니다.

## 2. 기여 유형과 근거

| 기여 유형 | 기록할 내용 |
|---|---|
| 직접 구현 | 본인이 구현한 기능·모듈과 담당 범위 |
| 공동 설계·구현 | 공동 작업 대상, 본인의 작업, 협업 범위 |
| 통합·수정·시험 | 연결하거나 수정한 모듈, 시험 조건과 결과 |
| 연구를 통한 독립 구현 | 이 저장소에서 새로 구현·비교·개선한 내용 |

한 작업에 여러 유형이 해당할 수 있습니다.
세부 경계가 명확하지 않으면 미분류로 남기고 확인할 내용을 적습니다.

각 기록에는 다음 정보를 연결합니다.

- 프로젝트·대상 기능
- 구체적인 수행 내용과 기여 유형
- 관련 버전·시기
- PR·Commit·설계 문서·시험 영상·실험 로그
- 근거 상태와 확인되지 않은 범위
- 연결되는 연구 질문 또는 실험

근거 상태는 사용자 진술 / 관련 자료 확인 / 개인 참여 범위 확인으로 구분합니다.
관련 자료가 팀 기능의 존재만 보여 주는 경우에는 개인 참여 범위 확인으로 표시하지 않습니다.

Git 커밋 작성자가 다르다는 이유만으로 공동 개발 경험을 배제하지 않습니다.
프로젝트에 코드가 존재한다는 이유만으로 개인 구현이라고 확정하지 않습니다.
기여율·단독 개발 여부·주도 여부는 근거 없이 추가하지 않습니다.

## 3. 초기 원장의 근거 상태

아래 내용은 사용자가 제공한 참여 내역입니다.

초기 원장은 개별 PR·Commit·설계 문서·영상·로그와 대조하지 않았으므로
모든 참여 내역의 근거 상태를 사용자 진술로 기록합니다.

명시된 공동 개발·통합 참여는 보존합니다.
직접 구현과 공동 구현의 경계가 명시되지 않은 작업은 추가 확인 대상으로 둡니다.

### Project A — NetClean

저장소: [isaac_ros2_waste_net_cutting2](https://github.com/suuuhululu/isaac_ros2_waste_net_cutting2)

사용자 진술에 따른 참여 범위:

- 공식 담당은 Computer Vision.
- YOLO 기반 객체 검출 및 RGB-D를 활용한 로봇 작업 목표 추정에 참여.
- Isaac Sim GUI와 Python Standalone 양쪽에서 시뮬레이션 환경과 로봇 구동 구현.
- 로봇 구동 및 시뮬레이터·ROS 2 통합 과정에 참여.

기여 분류:

- 통합 참여: 로봇 구동, 시뮬레이터, ROS 2 연결.
- 나머지 구현 작업의 직접·공동 범위: 추가 확인.

연구 연결 키워드:

RGB-D Geometry, Isaac Sim Standalone, Robot Motion & Coordinate Transformation,
Robotic Process Automation.

### Project B — AMR Patrol System

저장소: [AMR-patrol-system](https://github.com/suuuhululu/AMR-patrol-system)

사용자 진술에 따른 참여 범위:

- Nav2 Navigation과 AMCL Localization을 함께 관리.
- TurtleBot4 기반 자율주행·순찰 시스템의 구성·통합에 참여.
- 주행 경로, 위치추정, Nav2 설정 및 현장 동작 검증 경험.
- 다중 AMR 시스템의 동작과 인터페이스 연결 과정에 참여.

기여 분류:

- 공동 관리: Nav2·AMCL 설정 및 동작 관리.
- 통합·시험 참여: 순찰 시스템, 다중 AMR 인터페이스, 현장 동작 검증.
- 직접 구현·공동 개발에 해당하는 세부 변경 범위: 추가 확인.

연구 연결 키워드:

Autonomous Navigation, Localization, Nav2 Parameter Tuning,
Costmap & Keepout Filter, Multi-Robot Integration.

### Project C — Robotic Surface Carving

저장소: [robotic-curved-surface-carving](https://github.com/suuuhululu/robotic-curved-surface-carving)

사용자 진술에 따른 참여 범위:

- HMI와 백엔드 연결을 우선 구현.
- 이후 로봇 제어, 공정 실행, 경로 생성 알고리즘 개발에 공동 참여.
- 이미지 기반 경로 생성, 원통 곡면의 3D 경로 변환 및 실제 로봇 적용에 참여.
- Doosan M0609 실물 구동과 작업영역·실행 경로 검증에 참여.

기여 분류:

- 구현 진술: HMI·백엔드 연결. 직접·공동 범위는 추가 확인.
- 공동 개발: 로봇 제어, 공정 실행, 경로 생성 알고리즘.
- 통합·시험 참여: 이미지 경로의 실물 적용, 작업영역·실행 경로 검증.

연구 연결 키워드:

Robot Motion & Process Control, Image-to-Path Algorithms,
Parametric Surface Mapping, System Integration, HMI & Backend.

### Project D — Adaptive Co-Assembly

저장소: [co-human-robot-LEGO-assembly](https://github.com/suuuhululu/co-human-robot-LEGO-assembly)

사용자 진술에 따른 참여 범위:

- Doosan M0609·RG2 기반 로봇 실행 및 조립 동작 구현.
- 힘/토크 피드백과 접촉·압입 제어.
- 사람과 로봇의 작업 인계 및 제스처 기반 상호작용.
- HMI, State Manager, 작업 이력·DB·웹 연동.
- 다른 팀원의 설계·경로계획·비전 모듈과 실행 시스템 통합.

기여 분류:

- 구현·제어·연동 작업의 직접·공동 범위: 추가 확인.
- 통합 참여: 설계·경로계획·비전 모듈과 실행 시스템 연결.

연구 연결 키워드:

Contact-rich Manipulation, Human–Robot Interaction, State Management & Recovery,
Vision-based Assembly, Robot Execution Architecture.

## 4. 독립 연구 구현 기록

이 저장소의 독립 연구 구현으로 등록된 항목은 아직 없습니다.

새로운 결과가 생기면 다음 항목을 추가합니다.

- 주제·실험 ID와 연구 질문
- 새로 구현하거나 변경한 부분
- 기존 경험·외부 구현과의 관계
- 비교 결과와 한계
- 구현 Commit·PR 및 실험 결과 링크

기존 팀 프로젝트의 성과와 독립 실험의 성과를 각각 기록합니다.

## 5. 출처·공개 범위·정정

- 외부 논문·구현을 참고하면 출처와 라이선스를 기록합니다.
- 팀 코드·데이터를 재배포하기 전에 공개 권한과 라이선스를 확인합니다.
- 비공개 자료는 공개 가능한 설명과 근거 범위만 기록합니다.
- 개인 참여 범위가 확인되면 해당 작업의 근거 상태를 갱신합니다.
- 기록을 정정하면 변경 내용, 이유, 근거를 남깁니다.
