---
description: 호출된 네트워크에 대한 암호화된 사용자 인증 토큰을 반환합니다.
seo-description: 호출된 네트워크에 대한 암호화된 사용자 인증 토큰을 반환합니다.
seo-title: Builduserauthtoken 네트워크 방법
solution: Experience Manager
title: Builduserauthtoken 네트워크 방법
uuid: 8828 D 356-C 3 C 6-46 A 6-91 BF -83 BD 59 E 35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Builduserauthtoken 네트워크 방법{#builduserauthtoken-network-method}

호출된 네트워크에 대한 암호화된 사용자 인증 토큰을 반환합니다.

| 변수 | type | 설명 |
|--- |--- |--- |
| userid | 문자열 | 이 토큰이 속한 사용자의 사용자 ID 입니다. |
| Displayname | 문자열 | 사용자의 표시 이름입니다. |
| 만료됨 | double | 토큰이 초 단위로 만료되는 경우. |

## Java 예제 {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Nodejs 예제 {#section_xkd_gds_rz}

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

## Python 예제 {#section_dwg_gds_rz}

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
