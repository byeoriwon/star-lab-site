# 스타랩 · Star Lab 공식 웹사이트

- 사이트 주소: https://byeoriwon.github.io/star-lab-site/
- 전용 저장소: https://github.com/byeoriwon/star-lab-site

모바일 앱 및 소프트웨어 개발사 스타랩의 공개용 소개 사이트입니다. Google Play 개인 개발자 계정을 조직 계정으로 전환할 때 사용할 공식 웹사이트를 준비하는 목적으로 제작했습니다.

HTML과 CSS만 사용하는 정적 사이트입니다. 설치, 빌드, 서버, 데이터베이스, 유료 테마, 외부 폰트가 필요 없습니다. GitHub Free의 **새 공개 저장소**에서 GitHub Pages로 운영할 수 있습니다. 기존 앱 개발 저장소의 파일을 복사하거나 연결할 필요가 없습니다.

## 1. 포함된 파일

```text
star-lab-site/
├── index.html          # 소개 / 개발 분야 / Contact / 인증 메타태그 위치
├── privacy.html        # 이 웹사이트에 적용되는 개인정보처리방침
├── assets/
│   ├── styles.css      # PC·모바일 공통 스타일
│   └── favicon.svg     # 자체 제작한 별 심볼
├── .nojekyll           # Jekyll 처리 없이 정적 파일 제공
├── .gitignore
└── README.md
```

현재 공개 문의 주소는 **wonbyeori0529@gmail.com**입니다. 홈과 개인정보처리방침에 표시되며, 클릭하면 이메일 작성 프로그램이 열립니다. 이 사이트 자체에 메일함이나 문의 수신 서버가 생기는 것은 아닙니다. 메일은 해당 Gmail 계정으로 도착합니다.

집 주소, 개인 전화번호, 대표자 실명, 사업자등록번호, D-U-N-S 번호, 기존 앱 소스, API 키는 포함하지 않았습니다. Google Play 또는 사업자 관련 기관에 제출하는 정보와 이 공개 사이트에 표시하는 정보는 별도로 관리하세요.

## 2. GitHub Pages 배포 순서

1. GitHub에서 **New repository**를 선택합니다.
2. 저장소 이름을 예를 들어 `star-lab-site`로 지정하고 **Public**으로 만듭니다. 기존 저장소를 재사용하거나 fork하지 않습니다. 계정에 이미 `<계정명>.github.io` 사이트가 있어도 별도 프로젝트 사이트로 운영할 수 있습니다.
3. 이 폴더 **안의 파일과 `assets` 폴더**를 새 저장소의 최상위에 업로드합니다. `star-lab-site` 폴더 자체를 한 겹 더 올리지 마세요. `index.html`이 저장소 첫 화면에 바로 보여야 합니다.
4. `.nojekyll`과 `.gitignore`도 포함합니다. 탐색기에서 점으로 시작하는 파일이 보이지 않거나 업로드에서 빠지면 GitHub의 **Add file → Create new file**로 `.nojekyll`을 만들 수 있습니다. 비어 있는 파일로 저장이 어려우면 줄바꿈 한 줄을 넣어도 됩니다.
5. 파일을 기본 브랜치(`main`)에 커밋합니다.
6. 저장소 **Settings → Pages → Build and deployment**를 엽니다.
7. **Source: Deploy from a branch**, **Branch: main**, **Folder: /(root)**를 선택하고 **Save**를 누릅니다.
8. Pages 화면 또는 Actions에서 배포 완료를 확인합니다. Pages 화면에 표시된 실제 사이트 주소를 사용하세요. 프로젝트 사이트 주소의 형식은 다음과 같습니다.

   ```text
   https://<GitHub계정명>.github.io/star-lab-site/
   ```

9. **Enforce HTTPS**가 표시되면 활성화되어 있는지 확인합니다. 로그아웃한 브라우저에서도 홈, Contact, 개인정보처리방침이 열리는지 확인합니다.

별도의 GitHub Actions 파일이나 `npm` 명령은 필요 없습니다. 상대경로를 사용하므로 저장소 이름을 바꾸어도 내부 링크가 유지됩니다. 독립 도메인을 연결하지 않아도 GitHub에서 제공하는 주소로 사이트를 운영할 수 있습니다.

GitHub Free에서는 공개 저장소로 Pages를 운영할 수 있습니다. 공개 저장소의 파일과 커밋 기록도 공개되므로 사이트 파일만 업로드하세요. 커밋 작성자 정보와 GitHub 프로필에 이미 표시되는 개인정보는 이 사이트와 별개이며 GitHub 계정에서 확인할 수 있습니다.

## 3. Google Search Console 소유권 인증

### 사용할 속성

GitHub 제공 주소를 사용한다면 **URL 접두어(URL prefix)** 속성으로 등록합니다. `github.io` 전체를 소유한 것이 아니므로 도메인(Domain) 속성을 선택하지 않습니다.

예시 주소를 그대로 복사하지 말고, **Settings → Pages에 표시된 실제 HTTPS 주소**를 입력하세요. 프로젝트 사이트라면 저장소 경로와 마지막 `/`까지 포함합니다.

```text
https://<GitHub계정명>.github.io/star-lab-site/
```

### 메타태그를 넣을 위치

`index.html`의 `<head>` 안에서 아래 문구를 검색합니다.

```text
GOOGLE SEARCH CONSOLE
```

설명 주석이 끝나는 `-->` 바로 아래, 아이콘·스타일시트 `<link>` 위에 **Search Console에서 발급한 실제 태그 전체**를 붙여 넣습니다. 예시 형식은 다음과 같습니다.

```html
  <!-- GOOGLE SEARCH CONSOLE: ... 안내 주석 ... -->
  <meta name="google-site-verification" content="여기에_Search_Console에서_발급한_실제_값">

  <link rel="icon" href="./assets/favicon.svg" type="image/svg+xml">
```

**위 예시 값을 사용하면 인증되지 않습니다.** 기본 파일의 예시는 주석 안에 있으므로 활성화되어 있지 않습니다. 실제 태그는 반드시 주석 바깥, `<head>` 안에 넣으세요. 개인정보처리방침 페이지에는 넣을 필요가 없습니다.

### 인증 순서

1. 가능하면 Play Console 계정 소유자와 같은 Google 계정으로 [Search Console](https://search.google.com/search-console)에 로그인합니다.
2. **속성 추가 → URL 접두어**에 실제 배포 주소를 입력합니다.
3. 인증 방법에서 **HTML 태그**를 선택하고 태그 전체를 복사합니다.
4. GitHub에서 `index.html`을 편집하여 위 위치에 붙이고 커밋합니다.
5. GitHub Pages 재배포가 끝난 뒤, 공개 홈페이지의 페이지 소스에서 `google-site-verification` 태그가 주석 밖에 있는지 확인합니다.
6. Search Console로 돌아가 **확인(Verify)**을 누릅니다.
7. **인증 후에도 태그를 삭제하지 마세요.** Google은 소유권을 주기적으로 다시 확인합니다.

HTML 파일 업로드 방식이 안내되는 경우 Google에서 받은 파일을 이름과 내용 그대로 사이트 최상위에 추가하는 방법도 있습니다.

## 4. Play Console에서 웹사이트 인증 연결

Search Console 소유권 확인과 Play Console의 웹사이트 연결은 별도 단계입니다.

1. 배포한 웹사이트의 Search Console 소유권 인증을 먼저 완료합니다.
2. Play Console에서 **개발자 계정 → 내 정보(About you)**로 이동합니다.
3. 공식 조직 웹사이트에 Search Console에서 확인한 실제 사이트 주소를 입력하고 저장합니다.
4. **인증 요청 보내기(Send verification request)**를 누릅니다.
5. Search Console 소유자와 Play Console에 로그인한 Google 계정이 같으면 공식 안내상 요청이 자동 승인됩니다. 다른 계정이면 Search Console의 등록 소유자가 연결 요청을 승인해야 합니다.
6. Play Console에서 인증 완료를 확인한 다음 표시되는 계정 유형 전환 절차를 진행합니다.

이 사이트는 공식 웹사이트를 준비하는 부분을 지원합니다. 조직 계정 전환에는 조직 결제 프로필, D-U-N-S 번호 등 별도 요구사항이 있습니다. 이 템플릿이나 `github.io` 주소 사용만으로 Google의 조직 인증 승인 또는 테스트 요건 면제를 보장하지 않습니다. 최종 요구사항과 진행 상태는 Play Console의 안내를 따르세요.

## 5. 운영 시 수정할 곳

| 변경 내용 | 수정 위치 |
| --- | --- |
| 공개 문의 이메일 | `index.html`, `privacy.html`, 이 `README.md`의 `wonbyeori0529@gmail.com` 전체. HTML의 `mailto:` 주소와 표시 주소를 함께 수정 |
| Google 인증 태그 | `index.html` 상단 `<head>`의 `GOOGLE SEARCH CONSOLE` 주석 바로 아래 |
| 소개와 개발 분야 | `index.html`의 `about`, `work` 섹션 |
| 디자인·색상 | `assets/styles.css`의 `:root` 및 각 스타일 |
| 개인정보 처리 방식 | `privacy.html`의 실제 처리 내용과 시행일 |

개인정보처리방침은 **현재의 소개 웹사이트**를 기준으로 작성했습니다. 직접 수집하는 입력 폼, 자체 쿠키, 방문자 분석 도구, 광고 스크립트는 없습니다. GitHub Pages의 보안 목적 IP 기록과 Gmail을 통한 문의 정보 처리는 별도로 안내했습니다. 문의 메일을 목적 달성 후 삭제한다는 방침을 실제 운영에도 적용하세요.

앱에 광고·분석 SDK, 회원가입, 결제, 위치·사진 접근 등이 있다면 앱에서 처리하는 항목·목적·제공 및 위탁·보관 기간 등을 확인하여 **별도의 앱 개인정보처리방침**을 작성해야 합니다. 이 웹사이트용 페이지를 확인 없이 앱의 정책으로 등록하지 마세요. 공개할 앱 정보가 정해지면 공식 스토어 링크와 해당 앱의 방침을 추가할 수 있습니다.

### 배포 후 확인

- [ ] 홈에서 `스타랩`과 `Star Lab`이 정확히 표시됩니다.
- [ ] Contact의 메일 주소가 맞고, 메일 수신을 확인했습니다.
- [ ] 휴대전화 화면에서 글과 메뉴가 잘 보입니다.
- [ ] `privacy.html`이 로그인 없이 직접 열립니다.
- [ ] 등록한 사이트 주소에 저장소 경로가 빠지지 않았습니다.
- [ ] 실제 Google 인증 태그가 공개 홈페이지의 `<head>`에 유지됩니다.

## 6. 공식 참고 문서

2026년 10월 28일 확인. 서비스 메뉴 이름은 언어와 업데이트에 따라 달라질 수 있습니다.

- [GitHub Pages 소개와 데이터 수집](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
- [GitHub Pages 배포 원본 설정](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Search Console 소유권 확인](https://support.google.com/webmasters/answer/9008080?hl=ko)
- [Play Console 웹사이트 인증](https://support.google.com/googleplay/android-developer/answer/13205715?hl=ko)
- [개인 개발자 계정을 조직 계정으로 전환](https://support.google.com/googleplay/android-developer/answer/16260648?hl=ko)
