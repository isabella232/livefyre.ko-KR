---
description: collectionMeta 및 auth 토큰 작성을 위한 가이드입니다.
seo-description: collectionMeta 및 auth 토큰 작성을 위한 가이드입니다.
seo-title: 서버 측 토큰 작성
solution: Experience Manager
title: 서버 측 토큰 작성
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# 서버 측 토큰 작성{#build-server-side-tokens}

collectionMeta 및 auth 토큰 작성을 위한 가이드입니다.

Livefyre가 요청의 유효성을 검사하는 데 사용하는 토큰을 빌드하면 본인만 Livefyre 네트워크를 업데이트할 수 있습니다.

## CollectionMeta 토큰

토큰을 만들어 새 대화를 만들고 기존 대화를 표시하는 방법을 알아봅니다.

## 인증 토큰

사용자 관리에 Janrain Capture를 사용하지 않는 경우 통합 프로세스에서 필요한 단계인 사용자 인증을 위한 토큰을 만드는 방법을 알아봅니다.

## 사용자 인증 토큰 {#section_l5l_hwt_bbb}

이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 만드는 UserAuth JSON 개체를 생성하는 방법에 대해 설명합니다.

토큰을 만들려면 기본 언어 라이브러리를 사용하여 다음 매개 변수를 전달합니다.

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| networkName | 문자열 *필요* | Livefyre 네트워크 이름(Livefyre에서 제공). |
| networkKey | 문자열 *필요* | 이 특정 네트워크의 비밀 키(Livefyre에서 제공)입니다. |
| userId | 문자열 *필요* | 사용자 관리 시스템에 저장된 대로 로그인하는 사용자의 ID(영숫자, 대시, 밑줄 및 도트 문자만 허용됩니다. `[a-zA-Z0-9_-.]`). **** 참고:userId는 고유해야 합니다. |
| expire | 정수 *필요* | 토큰 만료 시기(초) **** 참고:이 값은 부동 으로도 전달할 수 있습니다. 생성된 JSON 웹 토큰은 이 값을 UNIX epoch 시간에 저장합니다. |
| displayName | 문자열 *필요* | UI 및 주석에서 이 사용자를 식별하는 텍스트입니다. (최대 문자 수:50) |

