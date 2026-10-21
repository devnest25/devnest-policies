---
title: Slime Miner 업데이트 정보 관리
lang: ko
---

# Slime Miner 업데이트 정보

- 공개 JSON: <https://devnest25.github.io/devnest-policies/slime-miner/updates/latest.json>
- 원본: `docs/slime-miner/updates/latest.json`
- 호스팅: 이 공개 저장소의 `main` → GitHub Pages `/docs` (HTTPS).
- 스키마1: `schema_version`(정수1), `latest_version_code`(양의 정수), `latest_version_name`(비어 있지 않은 문자열).
- 초기 값: code10 / 1.1.0. 2026-10-21 운영자가 전체 대상 사용자에게 실제 설치 가능한 공개 versionCode10을 확인했다. 기존 code10의 versionName1.1.0을 유지했다.

## 갱신 절차

1. 대상 사용자가 실제 Google Play에서 설치 가능한 공개 출시 버전의 code/name을 확인한다. AAB 생성·전달, 내부 테스트 업로드만으로 갱신하지 않는다.
2. 전용 브랜치에서 JSON의 code/name을 해당 출시 버전으로 함께 수정한다. schema_version은 앱이 지원하는1을 유지한다. 토큰·인증 URL·사용자 정보·게임 소스를 넣지 않는다.
3. JSON 파싱과 diff를 확인하고 PR을 main에 병합한다. 앱 빌드·버전 변경 작업과 이 게시 작업은 별개다.
4. Pages 배포 완료 후 위 URL을 인증 없는 HTTPS로 요청한다. HTTP200, 필수 필드와 게시 값을 확인한다. 캐시 때문에 이전 응답이 남으면 배포/캐시 갱신을 기다려 다시 확인한다.
5. 배포 커밋과 실제 응답 확인 시각을 운영 기록에 남긴다. 잘못된 게시라면 PR로 마지막 확인 값을 복원한다. 기존 설치 앱이나 사용자 저장을 수정하지 않는다.

앱은 버전 code로 비교하고 name을 표시한다. 업데이트는 선택 사항이며 조회 실패가 플레이를 막지 않는다. 스토어 URL은 앱에 고정되고 이 JSON으로 바꿀 수 없다. Debug 앱의 운영 자동 안내는 제외한다.
