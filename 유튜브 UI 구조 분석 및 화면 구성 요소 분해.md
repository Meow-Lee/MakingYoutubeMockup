## 1. 전체 구조 개요
- HTML은 head / body 두 영역으로 구성
- YouTube는 Google의 Polymer 프레임워크 기반 Web Components를 사용
- `ytd-*`, `yt-*` prefix가 붙은 커스텀 엘리먼트들로 화면을 구성함
- 커스텀 엘리먼트들은 각자 Shadow DOM을 가지며, 외부에서 내부 구조가 캡슐화됨

## 2. head 영역
- JS 번들 파일 (동작 로직)
- CSS 파일 (스타일 정의)
- 아이콘, 파비콘 등 리소스

## 3. body 영역 - DOM 트리 구조

### 루트: ytd-app
모든 YouTube UI 컴포넌트의 최상위 커스텀 엘리먼트

### 3-1. ytd-masthead (헤더 영역)
- 로고, 검색바, 로그인/업로드 아이콘 포함

### 3-2. app-drawer (사이드바)
- ytd-guide-renderer를 자식으로 가짐
- 홈, 구독, 보관함 등 네비게이션 메뉴

### 3-3. #content (메인 콘텐츠 컨테이너)
- ytd-page-manager가 현재 라우팅된 페이지를 렌더링
  - ytd-browse: 홈, 채널 페이지
  - ytd-watch: 영상 시청 페이지
  - ytd-search: 검색 결과 페이지

### 3-4. 부가 기능 컴포넌트
- ytd-popup-container: 팝업, 컨텍스트 메뉴
- ytd-miniplayer: 미니 플레이어
- yt-tooltip: 툴팁