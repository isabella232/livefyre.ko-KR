---
description: 호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.
seo-description: 호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.
seo-title: buildLivefyreToken 네트워크 메서드
solution: Experience Manager
title: buildLivefyreToken 네트워크 메서드
uuid: 7c72a05f-669b-4df3-8117-aa4af2f7a179
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# buildLivefyreToken 네트워크 메서드{#buildlivefyretoken-network-method}

호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.

호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.

기본적으로 이 토큰은 만들어진 후 24시간 후에 만료되도록 설정됩니다.

## Java 예 {#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## NodeJS 예 {#section_xkd_gds_rz}

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

## Python 예 {#section_dwg_gds_rz}

```
network.build_livefyre_token() 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## 루비의 예 {#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

샘플 출력:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

