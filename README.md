# 통합과학 World

직접 탐구하고 체험하는 통합과학 인터랙티브 수업 자료실입니다. GitHub Pages용 정적 웹사이트입니다.
자매 사이트: 지구과학 World (https://rockgyu-lab.github.io/Earth-Science-World/)

## 폴더 구성
- `index.html`: 통합과학 World 메인 화면 (단원별 학습실 목록)
- `작업기록.md`: 날짜별 작업 기록과 남은 일 (사이트 화면에는 나오지 않음)
- `copyright.js`: 모든 페이지 오른쪽 아래에 작게 표시하는 저작권 문구 (지구과학 World와 같은 파일)
- `ENSO/`: 엘니뇨와 라니냐 학습실
  - `ENSO_index.html`: 학습실 메뉴
  - `elnino.html`: 탐구 01 · 엘니뇨와 라니냐 (평상시, 엘니뇨, 라니냐, 엘니뇨 vs. 라니냐 탭). 해수면 온도 지도는 NOAA ERSST v5 실제 자료(퍼블릭 도메인)를 파일 안에 넣어 인터넷이 없어도 동작합니다.

## 페이지 연결
- 메인 화면 → 학습실 메뉴(`ENSO/ENSO_index.html`)
- 학습실 메뉴 → 각 자료, 상단의 "← 통합과학 World"로 메인 화면 복귀
- 각 자료 → 상단의 "메뉴로 돌아가기"로 해당 학습실 메뉴 복귀

## GitHub Pages 게시
1. GitHub에서 `RockGyu-Lab/Integrated-Science` 저장소를 만듭니다.
2. 이 폴더의 **내용물**(`index.html`, `copyright.js`, `ENSO/` 등)을 저장소 루트에 올립니다.
3. 저장소의 Settings → Pages로 이동합니다.
4. Build and deployment에서 `Deploy from a branch`를 선택합니다.
5. Branch는 `main`, 폴더는 `/(root)`로 선택하고 Save를 누릅니다.
6. 게시된 주소(https://rockgyu-lab.github.io/Integrated-Science/)를 열어 메인 화면에서 학습실과 자료가 차례로 열리는지 확인합니다.

## 주의할 점
- GitHub Pages는 파일·폴더 이름의 **대소문자를 구분**합니다. `ENSO`와 학습실 메뉴 파일의 이름을 바꾸면 링크도 함께 고쳐야 합니다.
- 글꼴(Pretendard)은 인터넷(CDN)에서 불러오므로, 오프라인에서는 컴퓨터의 기본 글꼴로 표시됩니다(기능에는 영향 없음).

## 새 자료 추가
1. 해당 학습실 폴더에 HTML 파일을 넣습니다.
2. 자료 상단에 학습실 메뉴로 돌아가는 링크를 둡니다. 예: `<a class="back" href="./ENSO_index.html">← [엘니뇨와 라니냐] 메뉴로 돌아가기</a>`
3. 학습실 메뉴 파일에 카드(`<a class="card" href="./새파일.html">…</a>`)를 추가합니다.
4. `</body>` 바로 앞에 저작권 표시를 넣습니다: `<script src="../copyright.js"></script>`

새 학습실을 만들 때는 폴더와 메뉴 파일(`<폴더>/<폴더>_index.html`)을 만들고, 루트 `index.html`의 `subject-list`에 카드를 추가합니다.

## 제목 수정
- 메인 페이지 제목과 학습실 카드: 루트 `index.html`
- 학습실 제목과 자료 카드: 각 폴더의 `<폴더>_index.html`
- 개별 자료의 제목: 각 자료 HTML 안의 `<title>` 또는 `<h1>`
