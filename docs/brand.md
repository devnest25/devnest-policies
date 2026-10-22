---
layout: default
title: DevNest 브랜드·CI 기준
lang: ko
---
# DevNest 브랜드·CI 기준

확정일: 2026-10-22 (KST) · CI 버전: 1.0

## 확정 방향
- 5개 시안 중 **2안 DN 결합형** 채택. D와 N을 결합한 심볼과 `DevNest` 워드마크를 사용한다.
- 브랜드 표기는 **DevNest**로 통일한다. 소개에 “1인 개발자” 문구를 사용하지 않는다.
- 네온 퍼플과 어두운 배경을 기본으로 한다. 로고 자체는 단색 면으로 표현하고 과도한 발광·왜곡을 추가하지 않는다.
- 가치관: 꾸준한 업데이트, 사용자 편의성, 방치형의 재미는 보는 맛.

## 색상
| 용도 | HEX |
| --- | --- |
| 대표 퍼플 | `#9B5CFF` |
| 어두운 배경·본문 | `#100D1B` |
| 밝은 글자·배경 | `#F5F1FF` |
| 보조 라벤더 | `#C4A9FF` |

## 원본과 적용
CI 벡터 원본의 SSOT는 이 저장소의 `docs/assets/brand/`이다.
소개 사이트는 원본을 복사하여 `dist/assets/brand/`에 사용한다. 변경 시 이 문서와 원본을 먼저 갱신한 뒤 사이트에 동기화한다.

- [밝은 배경용 가로 로고](assets/brand/logo-horizontal-color-light.svg)
- [어두운 배경용 가로 로고](assets/brand/logo-horizontal-color-dark.svg)
- [퍼플 심볼](assets/brand/symbol-color-light.svg)
- [검정 로고](assets/brand/logo-horizontal-black.svg) / [흰색 로고](assets/brand/logo-horizontal-white.svg)
- [정사각형 아이콘](assets/brand/app-icon.svg)

SVG는 이미지 생성 정리 시안의 윤곽을 벡터 경로로 변환한 파일이다. 워드마크도 경로이며 별도 폰트가 필요 없다.
아이콘 PNG는 동일 SVG에서 32·64·192·512·1024px로 출력한다.

## 사용 기준
- 가로·세로 비율을 유지한다. 임의 늘이기, 기울이기, 글자 재조합을 금지한다.
- 심볼 높이의 1/4 이상을 주변 여백으로 권장한다.
- 가로형 폭 180px 이상, 심볼 폭 32px 이상을 권장한다. 작은 영역에는 심볼만 사용한다.
- 밝은 배경에는 color-light, 어두운 배경에는 color-dark 버전을 사용한다.
- 정책 문서는 본문 가독성을 위해 밝은 배경을 유지하며 로고·링크 색상에 CI를 적용한다.
- 사이트 헤더·푸터에는 가로 로고, 브라우저 탭에는 정사각형 아이콘을 적용한다.
- 게임 내 로고 적용은 별도 요청 범위다. 이번 CI 확정으로 게임 로딩 화면에 DevNest를 추가하지 않는다.

## 적용 위치
- [DevNest 소개 사이트](https://devnest-studio.devnest25.chatgpt.site)
- [정책 문서](https://devnest25.github.io/devnest-policies/)
