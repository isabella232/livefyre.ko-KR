---
description: 2018년 3월 23일 릴리스에 대한 릴리스 노트입니다.
seo-description: 2018년 3월 23일 릴리스에 대한 릴리스 노트입니다.
seo-title: 2018년 3월 23일
solution: Experience Manager
title: 2018년 3월 23일
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 23, 2018{#march}

2018년 3월 23일 릴리스에 대한 릴리스 노트입니다.

## 새로운 기능 {#section_syx_mdt_wcb}

이 릴리스의 프로덕션 버전에서는 다음 기능이 새롭게 추가되었습니다.

* **** 프로덕션의 새로운 기능:Facebook에서 Facebook 로그인에 대한 보안 업데이트를 만들면 고객의 Facebook 로그인이 제대로 작동하지 않습니다. 이 문제를 해결하려면 다음을 수행해야 합니다.

   1. 클라이언트 OAuth 설정의 필드에 다음 URL을 **[!UICONTROL Valid OAuth redirect URIs]** 추가합니다. 올바른 네트워크 `<networkname>` 이름으로 바꾸기:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. 로 **[!UICONTROL Use Strict Mode for Redirect URI]** 전환합니다 **[!UICONTROL Yes]**.

* **** UAT의 새로운 기능:이제 스트림의 스마트 태그에 대한 신뢰 임계값을 선택할 수 있습니다. 태그에 대한 정밀도 점수(0-100)를 설정하면 검색하는 자산의 정확도를 제어할 수 있습니다.

## 문제 {#section_ehw_ndt_wcb}

다음 표의 문제가 이번 릴리스에서 해결되었습니다.

## 프로덕션 릴리스

| **문제 유형** | **구성 요소** | **릴리스 노트** |
|---|---|---|
| 버그 | Media Wall | 스트림 규칙에서 Instagram 게시물이 추가될 때 태그를 클릭할 수 없는 미디어 담벼락 문제를 해결했습니다. |
| 버그 | ModQ | ModQ가 제대로 로드되지 않는 문제를 해결했습니다. |
| 버그 | ModQ | 오디오 임베딩으로 인해 ModQ의 작동이 중단되던 문제가 수정되었습니다. |

## UAT 릴리스

| **문제 유형** | **구성 요소** | **릴리스 노트** |
|---|---|---|
| 개선 사항 | 필름스트립 | 필름스트립에 보다 쉽게 액세스할 수 있도록 하는 몇 가지 문제가 해결되었습니다. |
| 개선 사항 | Studio | 이제 IMS 로그인을 사용하여 Livefyre에 로그인할 수 있습니다. |

