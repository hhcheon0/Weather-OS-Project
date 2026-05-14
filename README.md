#Status: In Progress

# Weather-OS-Project
 - 2026 대구대학교 오픈소스소프트웨어 팀 프로젝트 19조

# 1. 프로젝트 목적: "오픈소스 데이터를 활용한 직관적인 날씨 웹 서비스"
 - GitHub Flow 방식으로 진행

### 🛠 GitHub Flow 워크플로우 (6단계)

### 1. 브랜치 생성
항상 최신 main에서 분기합니다.

의미 있는 브랜치 이름 사용

기능(feature) 단위 격리

Bash
git switch -c feature/add-auth

### 2. 작업 및 커밋
로컬 작업 후 원격에 Push합니다.

작은 단위로 자주 커밋

Push로 원격 백업 및 공유

Bash
git push origin feature/add-auth

### 3. PR 생성 (개설)
도움 요청 또는 병합 준비가 완료된 상태입니다.

💬 "코드에 대한 대화의 시작점"

### 4. 리뷰 & CI 통과
코드 품질 검증 단계입니다.

✅ Tests Passing

✅ Review Approved

### 5. 병합 (Merge)
검증된 코드를 main에 반영합니다.

즉시 배포 가능 상태 유지

자동 배포(CD) 트리거됨

### 6. 브랜치 삭제
역할이 끝난 브랜치는 정리합니다.

Bash
git branch -d feature/add-auth

# 2. 역할 분담

## 🏗️ 추천 역할 분담 (3인 체제)
## 1. UI/UX 디자인 및 프론트엔드 (Visual Lead)
가장 눈에 보이는 부분인 'OS 인터페이스'를 담당합니다.

주요 임무: 데스크탑 배경화면, 아이콘 배치, 작업 표시줄(Taskbar), 윈도우 창 열기/닫기 애니메이션 구현.

기술 포인트: CSS Grid/Flexbox를 활용한 레이아웃 구성, 반응형 디자인, UI 테마(다크/라이트 모드) 설정.

Git 브랜치 추천: feature/ui-layout, feature/os-animations

## 2. 코어 시스템 로직 개발 (Core Logic Engineer)
OS의 핵심 기능인 '상태 관리 및 창 제어'를 담당합니다.

주요 임무: 여러 개의 창이 뜰 때 우선순위(Z-index) 관리, 드래그 앤 드롭 기능, 시스템 시간/날짜 로직, 파일 탐색기 구조 설계.

기술 포인트: JavaScript 객체 지향 프로그래밍, 전역 상태 관리, 이벤트 핸들링 최적화.

Git 브랜치 추천: feature/window-manager, feature/system-logic

## 3. 데이터 엔진 및 API 연동 (Data & Integration)
'날씨 정보 처리 및 외부 기능'을 담당합니다.

주요 임무: Weather API(OpenWeatherMap 등) 연동, 지역별 날씨 검색 로직, 기상 데이터 파싱 및 시각화(차트 등), 위치 정보 처리.

기술 포인트: 비동기 통신(Fetch/Axios), JSON 데이터 가공, 에러 핸들링(네트워크 오류 대응).

Git 브랜치 추천: feature/weather-api, feature/search-engine
