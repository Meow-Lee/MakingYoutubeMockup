# 바꿀 것
ytd-masthead   →  <header>
app-drawer     →  <nav>
#content       →  <main>
footer         →  <footer>

# YouTube 목업 DOM 트리 구조

## 전체 트리
document
└── html
    ├── head
    └── body
        ├── header
        │   ├── div.header-left (햄버거 + 로고)
        │   ├── form.search-bar (검색창)
        │   └── div.header-right (로그인)
        ├── div.container
        │   ├── nav.sidebar (홈, Shorts, 탐색, 내 페이지)
        │   └── main.content
        │       └── ul.video-list
        │           └── li.video-card x3 (썸네일 + 제목 + 채널명 + 조회수)
        └── footer