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
