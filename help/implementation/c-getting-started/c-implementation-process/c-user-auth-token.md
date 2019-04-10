---
description: 이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 생성하는 Userauth JSON 개체를 생성하는 방법에
  대해 설명합니다.
seo-description: 이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 생성하는 Userauth JSON 개체를 생성하는
  방법에 대해 설명합니다.
seo-title: 사용자 인증 토큰
solution: Experience Manager
title: 사용자 인증 토큰
uuid: 6483 DEBD -453 C -4780-B 19 C -1 D 8041693617
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 사용자 인증 토큰{#user-auth-token}

이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 생성하는 Userauth JSON 개체를 생성하는 방법에 대해 설명합니다.

이 섹션에서는 사용자를 앱에 로그인하는 데 필요한 사용자 인증 토큰을 생성하는 Userauth JSON 개체를 생성하는 방법에 대해 설명합니다.

토큰을 만들려면 원하는 언어 라이브러리를 사용하여 다음 매개 변수를 전달합니다.

| 매개 변수 | type | 설명 |
|---|---|---|
| Networkname | 문자열 *필요* | Livefyre 네트워크 이름 (Livefyre 제공). |
| Networkkey | 문자열 *필요* | 이 특정 네트워크의 비밀 키 (Livefyre 제공). |
| userid | 문자열 *필요* | 사용자 관리 시스템에 저장된 대로 로그인하는 사용자의 ID (영숫자, 대시, 밑줄 및 점문자만 허용: [a-za-z 0-9_-.]). **참고:** Userid는 고유해야 합니다. |
| 만료됨 | 정수 *필요* | 토큰이 지금부터 만료되는 시기 (초). **참고:** 이 값을 부동 항목으로 전달할 수도 있습니다. 생성된 JSON 웹 토큰은 UNIX Epoch 시간에 이 값을 저장합니다. |
| Displayname | 문자열 *필요* | UI에서 이 사용자를 식별하는 텍스트입니다. (최대 문자 수: 50) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## Nodejs {#section_c42_mjz_1cb}

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
>Livefyre 인구 통계 계정에는 네트워크 키가 공유되지 않습니다. Livefyre가 환경을 프로비저닝하면 네트워크 키가 전송됩니다. 이 키는 비공개로 유지해야 합니다.

