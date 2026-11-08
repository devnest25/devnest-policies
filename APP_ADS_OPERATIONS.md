# 개발자 웹사이트·app-ads.txt 관리

2026-11-08 확인. 정책 main `fc4fafb`, 게임 main `bfe3222` 기준.

- Play Console 웹사이트: `https://devnest-studio.devnest25.chatgpt.site/`
- 인증 파일: `https://devnest-studio.devnest25.chatgpt.site/app-ads.txt`
- 관리 위치: Sites의 공개 DevNest 사이트, project `appgprj_6ad4309fb308819186a94db7d456392b`, 현재 게시 버전 5. 소유자 접근 확인. 정책 저장소의 하위 경로에 복사하지 않는다.
- 기존 개인정보처리방침 및 공지·패치노트·운영 JSON의 URL은 유지한다. 이 파일은 AAB에 포함하는 파일이 아니다.

## 파일과 탐색 근거

```text
google.com, pub-2745926655781274, DIRECT, f08c47fec0942fa0
```

일반 요청과 `Google-adstxt` User-Agent 요청 모두 로그인·쿠키 제공 없이 HTTP 200, `Content-Type: text/plain`, 중간 리디렉션 없이 위 한 항목을 반환했다. 기존 항목이 정확하여 재게시하지 않았다. 게시자 번호는 사용자 제공 값과 게임의 광고 설정을 대조하며, AdMob 계정 화면의 실제 번호는 운영자가 최종 대조한다.

[Google 탐색 규칙](https://support.google.com/admob/answer/9363762?hl=en)은 등록 도메인의 1단계 하위 도메인까지 확인한다. [Public Suffix List](https://publicsuffix.org/list/public_suffix_list.dat)의 `chatgpt.site` 항목에 따르면 등록 가능한 도메인은 `devnest25.chatgpt.site`, 사이트는 그 아래 1단계인 `devnest-studio`다. 따라서 현재 파일이 탐색 대상에 해당한다는 판단이다. 브라우저 표시만을 근거로 인증 성공을 선언하지 않는다. 부모 호스트의 파일은 404지만 현재 사이트 파일은 200이다. `/robots.txt`는 사이트 HTML을 반환하며 명시적인 Disallow 규칙은 없었다. 플랫폼의 향후 봇 판정과 Google의 실제 크롤링 성공은 별도다.

사용자 사이트 저장소 `devnest25/devnest25.github.io`는 GitHub API와 gh 조회에서 404였다. 현재 GPT 사이트의 파일을 활용할 근거가 있어 새 저장소나 대체 사이트는 만들지 않았다. 기존 공개 URL은 모두 보존했다.

## 사용자가 진행할 Console·AdMob 작업

1. Play Console → 사용자 늘리기 → 스토어 정보 → 스토어 설정 → 스토어 등록정보 연락처의 웹사이트에 위 루트 주소를 입력하고 변경을 반영한다. 공개 Play 페이지의 앱 지원 웹사이트 링크까지 확인한다.
2. AdMob의 해당 앱과 올바른 Play 스토어 항목 연결, 계정의 맞춤 app-ads.txt 게시자 ID가 `pub-2745926655781274`인지 확인한다.
3. AdMob → 앱 → 대상 앱 → 앱 설정 → **앱 인증(Verify app)** → **업데이트 확인(Check for updates)**. 또는 앱 개요/모든 앱의 인증 요청 안내에서 진입한다.
4. 모든 앱 → app-ads.txt → 대상 앱 상세에서도 조회 URL·마지막 크롤링·인증 상태를 확인한다. 변경 감지/크롤링에는 최대 24시간이 걸릴 수 있으므로 즉시 미반영을 실패로 단정하지 않는다.
5. 미인증이면 AdMob이 표시하는 실제 조회 URL·오류·게시자 ID를 확인한다. 파일 게시, 파일 인증, 앱 인증, 광고 게재 준비 심사는 각각 구분한다.

[앱 인증 공식 절차](https://support.google.com/admob/answer/14538460?hl=en). 이번 작업은 Console 입력이나 AdMob 인증을 수행한 것이 아니다.

## 변경 시

같은 Sites 프로젝트의 소스를 열어 루트 정적 파일을 관리하고 기존 유효 판매자 항목은 보존하며 중복만 제거한다. 게시 후 익명 GET·Google-adstxt GET의 상태/내용/리디렉션, robots 응답과 공개 Play 링크를 재검증한다. 플랫폼 도메인 또는 PSL이 바뀌면 탐색 경계를 다시 대조한다.
