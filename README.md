# KUIT 8기 Android 1주차

건국대학교 KUIT 8기 안드로이드 파트 1주차 미션 저장소입니다.
`main`에는 미션을 시작할 기본 프로젝트가 있습니다.

## Android Studio에서 시작하기

1. 시작 화면의 **Clone Repository / Get from VCS** 또는 프로젝트를 연 상태에서 **Git → Clone…**을 선택합니다.
2. 아래 HTTPS 주소를 입력하고 저장할 폴더를 선택한 뒤 **Clone**을 누릅니다.

   `https://github.com/Konkuk-KUIT/KUIT8_Android_week1.git`

3. 프로젝트가 열리면 Gradle 동기화가 끝날 때까지 기다립니다.
4. 현재 브랜치가 `main`인지 확인하고, 상단 브랜치 메뉴의 **New Branch…**를 선택합니다.
5. 브랜치명을 **`본인GitHub아이디/week1`**로 입력하고 **Checkout branch**를 선택해 생성합니다.

예: `honggildong/week1`. 다음 주차는 `honggildong/week2`처럼 주차 숫자를 바꿉니다.
상단에 본인 브랜치명이 표시된 상태에서 미션을 진행합니다.

## Android Studio에서 커밋·Push

1. **Git → Commit…**에서 올릴 파일을 선택하고 변경 내용을 확인합니다.
2. 메시지를 입력하고 **Commit**을 누릅니다. 예: `week1: 학생증 화면 구현`.
3. **Git → Push…**에서 대상이 `origin/본인GitHub아이디/week1`인지 확인하고 **Push**를 누릅니다.
4. GitHub 로그인을 요청하면 본인 계정으로 연결합니다.

Commit은 내 컴퓨터에 변경을 기록하고, Push는 그 커밋을 GitHub에 올립니다.

## GitHub 웹에서 미션 제출

1. 이 저장소의 **Pull requests → New pull request**를 누릅니다.
2. **base: `main` ← compare: `본인GitHub아이디/week1`**로 선택합니다.
3. 변경 파일을 확인하고 **Create pull request**를 누릅니다.
4. 제목과 본문을 작성합니다. 제목 예: `[week1] 홍길동 학생증 미션`.
5. 본문에 구현한 내용, 실행 화면 캡처, 막힌 점이나 질문을 적고 **Create pull request**로 제출합니다.

PR은 파트장이 확인합니다. **직접 Merge하지 않아도 됩니다.**
수정할 내용이 있으면 같은 브랜치에서 커밋·Push하면 기존 PR에 반영됩니다.

## 강의 예제 다시 보기

강의 참고 코드는 [lecture/examples 브랜치](https://github.com/Konkuk-KUIT/KUIT8_Android_week1/tree/lecture/examples)에 보관합니다.

## PR 자동 검사

| 이름 | 확인하는 내용 |
|---|---|
| PR Build & Test | 앱 빌드, 단위 테스트, androidTest 코드 컴파일 |
| PR Static Analysis | Android Lint |
| Leftover Marker Check | 충돌 마커 확인 — 경고용 |
| Docs Link Check | 문서 링크 확인 — 경고용 |

실패하면 PR의 **Checks**에서 오류 메시지를 확인합니다. 제공되는 리포트는 해당 검사 실행의 **Artifacts**에서 받을 수 있습니다.

관리자용 수동 검사로 **Build Cache Warm**, **Instrumented Test**, **Release Build Check**도 있습니다.
