---
description: 이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 만드는 UserAuth JSON 개체를 생성하는 방법에 대해 설명합니다.
seo-description: 이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 만드는 UserAuth JSON 개체를 생성하는 방법에 대해 설명합니다.
seo-title: 사용자 인증 토큰
solution: Experience Manager
title: 사용자 인증 토큰
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# 사용자 인증 토큰{#user-auth-token}

이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 만드는 UserAuth JSON 개체를 생성하는 방법에 대해 설명합니다.

이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 만드는 UserAuth JSON 개체를 생성하는 방법에 대해 설명합니다.

토큰을 만들려면 기본 언어 라이브러리를 사용하여 다음 매개 변수를 전달합니다.

| 매개 변수 | 유형 | 설명 |
|---|---|---|
| networkName | 문자열 *필수* | Livefyre 네트워크의 이름(Livefyre에서 제공). |
| networkKey | 문자열 *필수* | 이 특정 네트워크의 비밀 키(Livefyre에서 제공)입니다. |
| userId | 문자열 *필수* | 사용자 관리 시스템에 저장되어 있는 사용자 로그인 ID(영숫자, 대시, 밑줄 및 도트 문자만 허용됩니다.[a-zA-Z0-9_-.] 참조). **참고:** userId는 고유해야 합니다. |
| expected | 정수 *필수* | 토큰이 지금부터 만료될 시기(초). **참고:** 이 값은 부동 소수점 형태로 전달할 수도 있습니다. 생성된 JSON 웹 토큰은 이 값을 UNIX epoch 시간에 저장합니다. |
| displayName | 문자열 *필수* | UI 및 주석에서 이 사용자를 식별하는 텍스트입니다. (최대 문자 수:50) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>네트워크 키는 Livefyre 디모자이크 계정에 대해 공유되지 않습니다. Livefyre가 환경을 프로비저닝하면 네트워크 키를 받게 됩니다. 이 키는 비공개로 유지되어야 합니다.

