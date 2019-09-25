---
description: Livefyre에 네트워크의 사용자 동기화 URL을 제공된 URL로 업데이트하라는 메시지가 표시됩니다. 부울 값을 반환합니다.
seo-description: Livefyre에 네트워크의 사용자 동기화 URL을 제공된 URL로 업데이트하라는 메시지가 표시됩니다. 부울 값을 반환합니다.
seo-title: setUserSyncUrl 네트워크 메서드
solution: Experience Manager
title: setUserSyncUrl 네트워크 메서드
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncUrl 네트워크 메서드{#setusersyncurl-network-method}

Livefyre에 네트워크의 사용자 동기화 URL을 제공된 URL로 업데이트하라는 메시지가 표시됩니다. 부울 값을 반환합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| urlTemplate | 문자열 | 사용자 ID를 동기화하기 위해 Livefyre에 등록할 URL입니다. "`{id}`"가 제공된 URL 문자열의 일부가 되어야 합니다. |

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

## Ruby 예 {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

샘플 출력:

```
True
```
