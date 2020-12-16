---
description: Livefyre에 전달되는 collectionMeta 토큰을 만들어 새 컬렉션을 만듭니다.
seo-description: Livefyre에 전달되는 collectionMeta 토큰을 만들어 새 컬렉션을 만듭니다.
seo-title: CollectionMeta 토큰을 사용하여 컬렉션 만들기
solution: Experience Manager
title: CollectionMeta 토큰을 사용하여 컬렉션 만들기
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# CollectionMeta 토큰{#create-a-collection-using-the-collectionmeta-token}을 사용하여 컬렉션 만들기

Livefyre에 전달되는 collectionMeta 토큰을 만들어 새 컬렉션을 만듭니다.

1. collectionMeta 토큰을 만듭니다.
1. 체크섬을 만듭니다.

   컬렉션에 수행한 변경 사항을 Livefyre에 알리려면 checksum이 필요합니다. 제공된 체크섬이 이전에 전송된 체크섬과 다른 경우에만 Livefyre가 컬렉션을 업데이트합니다. 체크섬을 만드는 것은 `collectionMeta` 토큰을 만드는 것과 비슷하지만 `buildCollectionMetaToken`을 호출하는 대신 `buildChecksum`를 호출합니다.

Livefyre에 인증하기 위한 사용자 토큰을 만듭니다.