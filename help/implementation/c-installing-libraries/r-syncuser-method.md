---
description: Livefyre가 이전에 설정된 사용자 동기화 URL에서 사용자 정보를 가져오도록 알려줍니다. 부울 값을 반환합니다.
seo-description: Livefyre가 이전에 설정된 사용자 동기화 URL에서 사용자 정보를 가져오도록 알려줍니다. 부울 값을 반환합니다.
seo-title: Syncuser 네트워크 방법
solution: Experience Manager
title: Syncuser 네트워크 방법
uuid: 2 AFFB 03 D -3907-4 B 01-9 A 64-02 BA 1 B 06 DA 14
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Syncuser 네트워크 방법{#syncuser-network-method}

Livefyre가 이전에 설정된 사용자 동기화 URL에서 사용자 정보를 가져오도록 알려줍니다. 부울 값을 반환합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| userid | 문자열 | Livefyre와 동기화할 사용자 ID. 이 메서드를 호출하기 전에 Livefyre와 동기화된 URL 이 설정되어 있어야 합니다. |

## Java 예제 {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

샘플 출력:

```
true
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

샘플 출력:

```
true
```

## PHP 예 {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

샘플 출력:

```
true
```

## Python 예제 {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

샘플 출력:

```
True
```

## Ruby 예 {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

샘플 출력:

```
True
```
