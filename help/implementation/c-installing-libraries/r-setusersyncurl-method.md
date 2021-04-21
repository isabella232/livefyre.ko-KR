---
description: Livefyre에 네트워크의 사용자 동기화 URL을 제공된 URL로 업데이트하라는 메시지가 표시됩니다. 부울 값을 반환합니다.
title: setUserSyncUrl 네트워크 메서드
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# setUserSyncUrl 네트워크 메서드{#setusersyncurl-network-method}

Livefyre에 네트워크의 사용자 동기화 URL을 제공된 URL로 업데이트하라는 메시지가 표시됩니다. 부울 값을 반환합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| urlTemplate | 문자열 | 사용자 ID를 동기화하기 위해 Livefyre에 등록할 URL입니다. 제공된 URL 문자열에 &quot;`{id}`&quot;이(가) 포함되어야 합니다. |

## Java 예 {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

샘플 출력:

```
true
```

## NodeJS 예 {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

샘플 출력:

```
true
```

## PHP 예 {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

샘플 출력:

```
true
```

## Python 예 {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

샘플 출력:

```
True
```

## 루비의 예 {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

샘플 출력:

```
True
```
