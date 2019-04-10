---
description: 호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.
seo-description: 호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을
  반환합니다.
seo-title: Buildlivefyretoken 네트워크 메서드
solution: Experience Manager
title: Buildlivefyretoken 네트워크 메서드
uuid: 7 C 72 A 05 F -669 B -4 DF 3-8117-AA 4 AF 2 F 7 A 179
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Buildlivefyretoken 네트워크 메서드{#buildlivefyretoken-network-method}

호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.

호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.

기본적으로 이 토큰은 작성 시점으로부터 24 시간 후에 만료되도록 설정됩니다.

## Java 예제 {#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Nodejs 예제 {#section_xkd_gds_rz}

```
network.buildLivefyreToken(); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## PHP 예 {#section_ghf_gds_rz}

```
network.buildLivefyreToken(); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Python 예제 {#section_dwg_gds_rz}

```
network.build_livefyre_token() 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Ruby 예 {#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

