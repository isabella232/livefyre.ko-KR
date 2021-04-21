---
description: 호출된 네트워크의 다른 Livefyre API와 상호 작용하는 데 사용할 수 있는 암호화된 유효한 Livefyre 토큰을 반환합니다.
title: buildLivefyreToken 네트워크 메서드
exl-id: 2b303606-e8de-41e5-9c01-b41cc7bd8437
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '111'
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
