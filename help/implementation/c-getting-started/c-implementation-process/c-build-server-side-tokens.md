---
description: Collectionmeta 및 auth 토큰을 빌드하는 안내서입니다.
seo-description: Collectionmeta 및 auth 토큰을 빌드하는 안내서입니다.
seo-title: 서버측 토큰 빌드
solution: Experience Manager
title: 서버측 토큰 빌드
uuid: 8313 F 26 E -5 CEB -414 E-A 61 A -480 BB 7 A 8 BA 66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# 서버측 토큰 빌드{#build-server-side-tokens}

Collectionmeta 및 auth 토큰을 빌드하는 안내서입니다.

Livefyre가 요청을 확인하는 데 사용하는 토큰을 빌드하면 Livefyre 네트워크만 업데이트할 수 있습니다.

## Collectionmeta Token

토큰을 작성하고 기존 대화를 표시하는 토큰을 만드는 방법을 알아봅니다.

## 인증 토큰

사용자 관리를 위해 Janrain Capture를 사용하지 않는 경우 통합 프로세스에서 필요한 단계를 수행하는 토큰을 작성하는 방법을 알아봅니다.

## 사용자 인증 토큰 {#section_l5l_hwt_bbb}

이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 생성하는 Userauth JSON 개체를 생성하는 방법에 대해 설명합니다.

토큰을 만들려면 원하는 언어 라이브러리를 사용하여 다음 매개 변수를 전달합니다.

| 매개 변수 | type | 설명 |
|---|---|---|
| Networkname | 문자열 *필요* | Livefyre 네트워크 이름 (Livefyre 제공). |
| Networkkey | 문자열 *필요* | 이 특정 네트워크의 비밀 키 (Livefyre 제공). |
| userid | 문자열 *필요* | 사용자 관리 시스템에 저장된 대로 로그인하는 사용자의 ID (영숫자, 대시, 밑줄 및 점문자만 허용: `[a-zA-Z0-9_-.]`). **참고:** Userid는 고유해야 합니다. |
| 만료됨 | 정수 *필요* | 토큰이 지금부터 만료되는 시기 (초). **참고:** 이 값을 부동 항목으로 전달할 수도 있습니다. 생성된 JSON 웹 토큰은 UNIX Epoch 시간에 이 값을 저장합니다. |
| Displayname | 문자열 *필요* | UI에서 이 사용자를 식별하는 텍스트입니다. (최대 문자 수: 50) |

