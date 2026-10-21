---
title: Slime Miner 공지사항·패치노트 관리
lang: ko
---

# Slime Miner 공지사항·패치노트

- 공개 JSON: https://devnest25.github.io/devnest-policies/slime-miner/notices/feed.json
- 원본: `docs/slime-miner/notices/feed.json`, 이 저장소의 `main` → GitHub Pages `/docs`.
- 초기 데이터는 검증된 원고가 없어 유효한 빈 목록이다. 출시 날짜·버전·공지 내용을 추정하지 않는다.
- 기존 업데이트 안내 `updates/latest.json`과 별도이며 해당 파일을 수정하지 않는다.

## 데이터 계약

UTF-8 JSON, `schema_version: 1`, `items` 배열. 응답 최대262144바이트·100항목.
각 항목은 `id`(영문/숫자/밑줄/하이픈1~64자, 전체에서 고유), `kind`(`notice` 또는 `patch`), `published_on`(유효한 날짜 `YYYY-MM-DD`), `content`를 갖는다.
`content.ko`, `content.en`은 각각 `title`(1~160자), `body`(1~12000자)의 객체다. 언어 하나는 생략할 수 있고 제공된 다른 언어로 표시한다. 제공한 언어의 제목/본문은 모두 필수이며 공백만인 내용은 허용하지 않는다.
`patch`는 `version_code`(1~2100000000 정수), `version_name`(1~64자, 앞뒤 공백/제어문자 없음)도 필수다.
최신 날짜 먼저, 같은 날짜는 ID 오름차순. 본문은 일반 텍스트·줄바꿈이며 HTML/스크립트/URL은 실행되지 않는다.
스키마/필수 값이 잘못되거나 제한을 넘으면 전체 응답을 거부하고 기존 정상 내용을 유지한다.

## 갱신 절차

1. 실제 공개 출시가 확인된 변경만 패치노트로 작성한다. AAB 생성/전달·Debug 변경·미출시 MVP는 출시 완료 근거가 아니다. 출시일·버전·원고의 확인 근거를 PR에 남긴다. 새 대외 메시지나 이벤트 보상 공지는 별도 승인을 받는다.
2. 전용 브랜치에서 이 JSON만 편집한다. ID는 재사용하지 않는다. 두 언어를 제공할 수 없으면 빠진 언어 객체를 생략한다. 인증/토큰/개인정보/비공개 주소를 넣지 않는다.
3. JSON 문법·위 계약·앱 `NoticeFeed.from_body` 파서·diff를 검증한다. UI 확인은 앱 저장소의 PC fixture를 사용하며 fixture를 공개 운영 JSON에 올리지 않는다.
4. PR을 main에 병합하고 Pages 배포 성공을 확인한다. 공개 URL을 인증 없는 HTTPS로 요청해 HTTP200·본문·제품 파서를 확인한다. Pages 캐시(`max-age=600`)가 남으면 배포/캐시 갱신 뒤 재확인한다.
5. 게시 커밋·실제 응답 확인 시각·원고 확인 근거를 운영 기록에 남긴다. 앱 사용자는 새로고침 또는 재실행으로 조회한다. 잘못된 게시라면 PR로 마지막 정상 JSON을 복원한다.

앱은 첫 수동 진입 시 8초 제한으로 조회하고 성공 결과를 실행 중 메모리에 재사용한다. 읽음 저장·배지·자동 팝업·푸시·검색·첨부·보상은 없다.
