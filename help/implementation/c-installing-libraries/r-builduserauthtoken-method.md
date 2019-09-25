---
description: 호출된 네트워크에 대해 암호화된 사용자 인증 토큰을 반환합니다.
seo-description: 호출된 네트워크에 대해 암호화된 사용자 인증 토큰을 반환합니다.
seo-title: buildUserAuthToken 네트워크 메서드
solution: Experience Manager
title: buildUserAuthToken 네트워크 메서드
uuid: 8828d356-c3c6-46a6-91bf-83bd59e35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildUserAuthToken 네트워크 메서드{#builduserauthtoken-network-method}

호출된 네트워크에 대해 암호화된 사용자 인증 토큰을 반환합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| userId | 문자열 | 이 토큰이 속한 사용자의 사용자 ID입니다. |
| displayName | 문자열 | 사용자의 표시 이름입니다. |
| expire | 이중 | 토큰 만료 시간(초)입니다. |

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

## Ruby 예 {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
