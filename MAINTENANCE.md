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
