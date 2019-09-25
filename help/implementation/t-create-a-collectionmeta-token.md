---
description: Livefyre로 전달되는 collectionMeta 토큰을 만들어 새 컬렉션을 만듭니다.
seo-description: Livefyre로 전달되는 collectionMeta 토큰을 만들어 새 컬렉션을 만듭니다.
seo-title: CollectionMeta 토큰을 사용하여 컬렉션 만들기
solution: Experience Manager
title: CollectionMeta 토큰을 사용하여 컬렉션 만들기
uuid: 5a3e18e8-8568-4 파섹
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# CollectionMeta 토큰을 사용하여 컬렉션 만들기{#create-a-collection-using-the-collectionmeta-token}

Livefyre로 전달되는 collectionMeta 토큰을 만들어 새 컬렉션을 만듭니다.

1. collectionMeta 토큰을 만듭니다.
1. 체크섬을 만듭니다.

   Livefyre에 컬렉션에 수행한 변경 사항을 알리려면 체크섬이 필요합니다. 제공된 체크섬이 이전에 전송된 체크섬과 다른 경우에만 Livefyre가 컬렉션을 업데이트합니다. 체크섬을 만드는 것은 `collectionMeta` 토큰을 만드는 것과 비슷하지만 `buildCollectionMetaToken` 호출하는 대신 `buildChecksum`호출합니다.

Livefyre에 인증하기 위한 사용자 토큰을 만듭니다.