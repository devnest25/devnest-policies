# 현재 개인정보처리방침 관리 — 2026-11-03

현재 공개 원본은 `docs/slime-miner/privacy-policy.md`와 `privacy-policy-en.md`다. 한·영 시행일/수정일을 2026-11-03으로 맞췄다. 아래 과거 기록은 당시 상태이며, 현재 확인 상태는 이 절을 우선한다. 기존 공개 URL·문의 이메일·Pages 레이아웃은 유지한다.

## 이번 변경과 확인 근거

- 사용자 요청: 글로벌 출시 준비에 맞춰 현재 프로젝트 기준으로 개인정보·동의 안내를 보완.
- 게임 소스 기준: `devnest25/slime-miner` main `019f90011251f3ed381f827123d6ed1d37e529a3`. 정책 원본 기준: `c4613db35223a0de7c6f4d59d155583296f3cb45`. 실제 Play 설치본·Console 설정과 소스 확인은 구분한다.
- `ranking_service.gd`, `ranking_record.gd`, `save_snapshot.gd`, `save_system.gd`: 연결/최고 기록 갱신/재시도에 따른 랭킹 제출, 플레이어 ID를 소유 계정으로 로컬 저장하고 수동 클라우드 백업에도 포함. 기존의 “플레이어 ID는 실행 중에만 사용” 설명을 정정.
- PGS 플러그인과 `ranking_window.gd`: 공개 랭킹의 플레이어 ID·표시 이름·순위·최고 단계 조회. 다른 이용자 목록은 일반 저장본에 포함하지 않음. 수동 Saved Games 백업과 자동 랭킹 제출을 분리해 안내.
- 업데이트·공지·우편·쿠폰 클라이언트: 고정 공개 HTTPS 파일 조회. 게임즈 ID/광고 ID/구매 토큰/세이브/입력 쿠폰을 요청에 첨부하지 않음. 쿠폰 대조와 수령 내역 처리는 로컬이며, 수령 식별값은 진행 백업 대상.
- GitHub Pages 호스팅 접속 정보와 Gmail 문의 처리, 로컬/Google/GitHub 삭제 경계를 추가. 자체 서버가 없다는 설명이 외부 온라인 처리 부재로 오해되지 않도록 정정.
- AdMob/UMP: 설정의 광고 개인정보 선택 경로와 동의 변경 시 기존 광고 로드 무효화는 코드로 확인. EEA·영국·스위스 동의, 다른 지역의 조건부 권리 안내를 보완. 방침 열람·설치·계속 이용을 선택적 처리 동의로 보지 않음을 명시. 미국 메시지 게시·옵트아웃 검증 완료로 표현하지 않음.
- 광고 의존성 잠금 파일상 GMA Next-Gen `ads-mobile-sdk:1.4.0`, Godot AdMob 플러그인 5.1.0. 공식 최신 SDK 데이터 안내를 참고하되 해당 배포 바이너리·미디에이션의 검증 완료로 확대하지 않음.

## 후속 확인 — 문서 보완과 별개

- **앱 내 일반 개인정보처리방침 진입점:** 확인한 `SettingsPanel.tscn`, `settings_panel.gd`, `main.gd`, 광고 화면에는 UMP 광고 개인정보 버튼이 있지만 일반 한·영 방침 URL을 여는 연결은 확인되지 않았다. 게임 설정에 항상 접근 가능한 방침 링크를 추가/대조하는 앱 후속 작업이 필요하다. UMP 버튼은 지역에 따라 숨겨지므로 일반 방침 링크의 대체가 아니다. 이번 정책 문서 작업에서 게임 기능은 수정하지 않았다.
- **지역별 동의 실제 설정/실기기:** AdMob 유럽·미국 메시지 게시 상태와 대상 지역, 동의/거부/철회/재선택, 네트워크 오류·재실행·광고 제거 보유 시 동작, 브리지의 광고 요청 허용 판정을 확인한다. 과거 동의 메시지 정상 작동 보고를 모든 지역·선택 조합 PASS로 확대하지 않는다.
- **대상 연령·출시 국가:** Play Console 실제 설정과 아동 관련 광고/UMP 플래그를 대조한다. 특정 연령 제한이나 아동 미대상을 문서만으로 확정하지 않는다.
- **지역별 법적 고지:** 실제 배포국과 계약에 맞춰 처리 목적별 법적 근거(EEA/영국 등), 운영자 법적 신원·필요 시 대표자, 국외 이전 수령 주체·국가·항목·시점/방법·보유 기간·거부 영향·보호 근거 등 추가 고지 필요 사항을 확정한다. 미확인 계약·기간·법적 근거를 임의 작성하지 않는다. Google/GitHub 정책 링크만으로 모든 지역의 개별 고지가 충족되었다고 간주하지 않는다.
- **Play 데이터 보안:** 실제 배포본 기준으로 플레이어 ID·표시 이름·랭킹, 진행 백업, 구매 정보, 광고 SDK 및 호스팅 접속 정보의 수집/공유 분류·선택성·보안 응답을 대조한다. 자체 서버가 없다는 이유로 “수집 없음”으로 답하지 않는다.
- **삭제 결과:** Google 게임별 삭제와 랭킹·Saved Games 반영, 남은 로컬 데이터의 재제출/재백업 동작을 실제 계정으로 확인한다. 삭제 기간이나 Google 데이터 전체 삭제를 보장하지 않는다.

## 검증 및 변경 경계

- 한·영 정보 범위·날짜·상호 링크, Markdown 표/헤딩, 기존 결제·문의·삭제 안내 보존과 변경 diff 확인 완료. 두 언어 모두 9개 본문 절·7개 데이터 행이 Markdown 렌더링에 포함되며 외부 참고 링크의 언어 간 일치를 확인했다. 기존 결제 절은 그대로 보존했다.
- 로컬 브라우저 화면 검증은 실행 파일이 없어 미실행이다. 레이아웃·인덱스·사이트 설정은 변경하지 않았다. 공개 Jekyll 결과의 본문·언어·표·링크는 배포 후 확인 대상으로 구분한다.
- main 반영 후 Pages 배포 결과와 두 공개 URL의 HTTP 상태·실제 본문을 확인한다. 저장소 원본 반영과 공개 배포 확인은 최종 작업 보고에서 구분한다.
- 정책 파일·README·이 관리 문서만 변경한다. 운영 JSON, 공지/패치노트 게시, 게임 코드·버전, AAB/APK, Console/AdMob 설정은 변경하지 않는다.
- 공개 저장소에는 게임 소스·세이브·거래/계정 식별값·비밀정보·문의 원문을 올리지 않는다. 이번 변경은 정책 정확성 보완이며 모든 국가 출시 요건 충족을 의미하지 않는다.

## 공식 참고 자료 (2026-11-03 확인)

- [Google Play User Data](https://support.google.com/googleplay/android-developer/answer/10144311)
- [GMA Next-Gen 데이터 공개](https://developers.google.com/admob/android/next-gen/privacy/play-data-disclosure)
- [UMP 및 개인정보 선택 진입점](https://developers.google.com/admob/android/privacy)
- [AdMob 미국 주 메시지](https://support.google.com/admob/answer/10862202)
- [Play Games 데이터 공개](https://developer.android.com/games/pgs/data-collection), [랭킹 공개 범위](https://developer.android.com/games/pgs/leaderboards), [게임별 삭제](https://support.google.com/googleplay/answer/9130646)
- [GitHub Pages 접속 정보](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection), [GitHub 개인정보처리방침](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)
- [유럽연합 정보주체 안내](https://commission.europa.eu/law/law-topic/data-protection/information-individuals_en)
- [캘리포니아 개인정보 권리 안내](https://oag.ca.gov/privacy/ccpa)

---

# 과거 관리 이력

## Slime Miner 업데이트 버전 정보 (2026-10-21)

기존 공개 Pages에 `docs/slime-miner/updates/latest.json`을 추가했다. 운영자가 공개 설치 가능하다고 확인한 code10 / 기존 name1.1.0을 게시한다. 앱·스토어 버전은 변경하지 않는다. 갱신 절차는 [업데이트 정보 관리](docs/slime-miner/updates/README.md)를 따른다. 공개 HTTPS 응답 확인은 배포 후 별도 기록한다.

# 2026-10-19 현재 방침 갱신·영문 제공

이번 갱신은 사용자 요청에 따라 현재 구현과 불일치하던 공개 초안을 교체한다. 시행일/수정일2026-10-19, 운영자 DevNest, 기존 문의 이메일 유지. 한국어 URL 유지·영문 privacy-policy-en.html 추가·언어별 html lang·상호 링크·인덱스 보완. 별도 HTML 본문 사본은 만들지 않는다.

## 확인 근거
- 게임 최신 main의 광고105/결제97/클라우드 구현 및 기존 사용자 실기기 확인.
- scripts/save/cloud_save_controller.gd: 선택적 연결·수동 업로드/복원·로컬/클라우드 삭제 구분.
- tools/pgs_plugin/plugin/src/main/java/com/jacobibanez/plugin/android/godotplaygameservices/GodotAndroidPlugin.kt: currentPlayer.playerId 실행 중 계정 확인, Saved Games bytes/metadata, SDK 재개 계정 검증.
- scripts/billing/permanent_purchase_service.gd 및 purchase_journal.gd: 상품/토큰/서명 거래 원장·보유권 캐시/승인·조회, 로컬 저장.
- scripts/ads/admob_adapter.gd 및 ad_diagnostics.gd: AdMob/UMP, 동의 선택·설정 진입, 진단 마스킹. 광고 제거가 SDK 정보 처리 전체 중단을 보장하지 않는 실제 초기화 경로 반영.
- 사용자2026-10-19 보고: 동의 메시지 등록 후 스토어 앱 정상 작동. 개별 광고 경로·EEA 거부/재선택 전체 검증 성공으로 확대하지 않는다.
- Google 공식 GMA Next-Gen 데이터 공개, PGS 데이터 공개·게임별 삭제, Play User Data 정책을2026-10-19 확인.

## 반영
- 검토용 초안/시행일 공란 제거, 제공 중인 게임즈·인앱결제·보상 상태 처리 설명.
- 로컬/OS 백업/클라우드/Play 거래/문의 자료의 보관·삭제 분리.
- 데이터 권리·국외 처리·암호화 범위, 한국어/영어 동일 항목 제공.
- 과거 play-games-planned.md는 역사 문서로 안내하고 최신 방침으로 연결.

## 남은 확인 — 문서 수정만으로 완료 처리하지 않음
- [ ] Play Console 대상 연령/출시 국가 실제 설정과 Google 아동 관련 SDK 플래그 대조. 아동 미대상/특정 연령 기준을 임의 확정하지 않았다.
- [ ] 적용 법령에 따른 국외 이전 수령 주체·국가·항목·시점/방법·기간·거부 영향 등 구체 고지 필요 여부와 실제 계약/정보 확인. 알려지지 않은 기간·법적 근거를 만들어 넣지 않았다.
- [ ] Google이 관리하는 데이터의 실제 삭제 반영 결과/기간. 공식 사용자 절차만 안내하며 확인하지 않은 SLA를 약속하지 않았다.
- [ ] Play Console 데이터 보안 응답과 현재 AdMob/PGS/Billing의 실제 처리 범위 대조.
- [ ] 앱 설정의 개인정보처리방침 링크 존재·접근, EEA 동의/거부/재선택 검증.
- [ ] Pages 배포 완료와 한·영 공개 URL HTTP/본문 확인. 배포 결과는 실행 후 추가 기록한다.

게임 코드·SDK·Console·AdMob 설정·스토어 배포는 변경하지 않는다. 문서만으로 모든 지역 법규 준수나 Play 심사 통과를 보증하지 않는다. 한·영의 정보 범위와 날짜를 함께 갱신한다.

---

## 과거 관리 이력 (아래는 당시 상태)

# 정책 문서 관리

## 원본
- 공개 방침의 SSOT: docs/slime-miner/privacy-policy.md
- Markdown 원본을 GitHub Pages의 Jekyll이 HTML로 변환한다. 본문을 별도 HTML에 복사하지 않는다.
- 게임의 기능·데이터 처리 SSOT는 slime-miner 저장소의 최신 docs 및 소스다.
- SDK, 로그인, 서버, 분석 도구, 결제, 대상 연령, 출시 국가가 바뀌면 방침과 Play 데이터 보안 답변을 함께 재검토한다.

## 2026-10-15 확인 근거
- slime-miner main 트리: 6b60220267a8f968781899f1cc59986d32f19290
- scripts/save/save_system.gd: user://savegame.json 및 백업 저장
- scripts/ads/admob_adapter.gd: AdMob, UMP, 광고 개인정보 선택 화면
- docs/mvp/MVP_71_REWARDED_ADS.md: 계정/서버/SSV 제외, 출시 설정·실기기 검증 별도
- https://developers.google.com/admob/android/privacy/play-data-disclosure?hl=ko
- https://support.google.com/googleplay/android-developer/answer/10144311?hl=ko

## 정식 방침 전환 전 남은 항목
- [x] 운영자가 공개할 문의 이메일 확정: devnest25@gmail.com (2026-10-15)
- [ ] 출시 대상 연령·국가 확정 및 아동 관련 정책 적용 여부 검토
- [ ] 실제 배포 AAB의 SDK 버전·미디에이션·백업 설정 및 수집 항목 대조
- [ ] AdMob 동의 메시지 설정 및 실기기 동의/선택 변경 확인
- [ ] 필요한 국외 이전 고지 등 출시 지역별 추가 내용 확정
- [ ] 시행일 확정 및 초안 표시 제거
- [ ] Pages 공개 URL 정상 응답 확인
- [ ] 게임 설정에 개인정보처리방침 URL 연결
- [ ] Play Console 개인정보처리방침 URL 및 데이터 보안 응답 대조

## Pages 활성화
저장소 Settings → Pages → Build and deployment:
- Source: Deploy from a branch
- Branch: main
- Folder: /docs
- Save

연결된 GitHub 도구는 Pages 설정 변경을 제공하지 않으므로 운영자가 이 설정을 수행한다.
예정 주소: https://devnest25.github.io/devnest-policies/slime-miner/privacy-policy.html
활성화 및 실제 접근 확인 전에는 사용 가능한 공개 URL로 간주하지 않는다.

## 변경 절차
원본 수정 → diff 확인 → main 커밋 → Pages 배포 및 링크 확인.
공개 저장소에 게임 소스·세이브 파일·인증정보·사용자의 문의 원문을 올리지 않는다.

## 게임즈 백업·복원 도입 예정 (2026-10-15)
- 예정 기능 변경안의 단일 원본: docs/slime-miner/play-games-planned.md. Jekyll이 동일 Markdown에서 HTML을 생성한다.
- 현재 공개 방침 원본과 분리하며 미구현 인증/클라우드 저장을 제공 중이라고 쓰지 않는다. 현재 방침의 초안 상태·문의 이메일을 유지한다.
- 게임 SSOT: slime-miner의 docs/mvp/MVP_74_PLAY_GAMES_BACKUP_RESTORE.md. 확인한 main은 cbcc947be583cdc77d70184f16123afd32b3ff9f (Save V25 / Godot 환경 문서 4.7).
- 플러그인 인증·저장·복원 최소 검증, 실제 전송 항목·보관·삭제/연결 해제 확인 후 위 변경안의 공개 전환 체크리스트를 완료한다.
- PGS v2 자동 인증/OS 계정 관리 제약을 확인한다. 인앱 수동 연결과 SDK 인증 시점을 혼동하지 않는다.
- 출시 연령·국가는 미확정으로 보존한다. 실제 출시 전 공개 방침·시행일·Play 데이터 보안 응답·게임 내 링크를 함께 대조한다.
- 이번 반영: 문서만 수정. 게임 기능/SDK 설치·APK 생성 및 법적 최종 확정을 의미하지 않는다.

