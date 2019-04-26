---
description: Livefyre에 네트워크의 사용자 동기화 URL를 업데이트하도록 알려줍니다. 부울 값을 반환합니다.
seo-description: Livefyre에 네트워크의 사용자 동기화 URL를 업데이트하도록 알려줍니다. 부울 값을 반환합니다.
seo-title: Setusersyncurl 네트워크 메서드
solution: Experience Manager
title: Setusersyncurl 네트워크 메서드
uuid: cd 067 e 90-a 2 da -4 e 3 d -8 e 60-7 eabfd 86 fc 7 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Setusersyncurl 네트워크 메서드{#setusersyncurl-network-method}

Livefyre에 네트워크의 사용자 동기화 URL를 업데이트하도록 알려줍니다. 부울 값을 반환합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| Urltemplate | 문자열 | 사용자 ID 동기화를 위해 Livefyre에 등록할 URL 입니다. "`{id}`» 가 제공된 URL 문자열의 일부가 되어야 합니다. |

## Java 예제 {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

샘플 출력:

```
true
```

## Nodejs 예제 {#section_xkd_gds_rz}

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

## Python 예제 {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

샘플 출력:

```
True
```

## Ruby 예 {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

샘플 출력:

```
True
```
