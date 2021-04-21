---
description: 호출된 네트워크의 암호화된 사용자 인증 토큰을 반환합니다.
title: buildUserAuthToken 네트워크 메서드
exl-id: dcc61c4b-90d9-42a0-9f46-73a843a4ad78
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 8%

---

# buildUserAuthToken 네트워크 메서드{#builduserauthtoken-network-method}

호출된 네트워크의 암호화된 사용자 인증 토큰을 반환합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| userId | 문자열 | 이 토큰이 속한 사용자의 사용자 ID. |
| displayName | 문자열 | 사용자의 표시 이름입니다. |
| expected | 이중 | 토큰이 몇 초 후에 만료됩니다. |

## Java 예 {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP 예 {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Python 예 {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## 루비의 예 {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
