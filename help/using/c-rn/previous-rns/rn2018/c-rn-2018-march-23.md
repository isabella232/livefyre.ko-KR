---
description: 2018 년 3 월 23 일 릴리스 릴리스 노트.
seo-description: 2018 년 3 월 23 일 릴리스 릴리스 노트.
seo-title: 2018년 3월 23일
solution: Experience Manager
title: 2018년 3월 23일
uuid: b 69 b 8715-ace 4-48 e 0-8 f 54-ce 4 e 12170 ef 3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 2018 년 3 월 23 일{#march}

2018 년 3 월 23 일 릴리스 릴리스 노트.

## 새로운 기능 {#section_syx_mdt_wcb}

이번 릴리스 프로덕션 버전의 새로운 기능은 다음과 같습니다.

* **제작 과정 새로운 기능:** Facebook 로그인 시 고객의 Facebook 로그인이 제대로 작동하지 않는 Facebook 로그인에 대한 보안 업데이트를 만들었습니다. 이 문제를 해결하려면 다음을 수행해야 합니다.

   1. 클라이언트 OAuth 설정의 **[!UICONTROL Valid OAuth redirect URIs]** 필드에 다음 URL를 추가합니다. 올바른 `<networkname>` 네트워크 이름으로 바꾸기:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. 으로 전환합니다 **[!UICONTROL Use Strict Mode for Redirect URI]****[!UICONTROL Yes]**.

* **UAT의 새로운 기능:** 이제 스트림에서 스마트 태그에 대한 신뢰 임계값을 선택할 수 있습니다. 태그에 대한 정밀도 점수 (0-100) 를 설정하면 검색하는 자산의 정확도를 제어할 수 있습니다.

## 문제 {#section_ehw_ndt_wcb}

다음 표의 문제가 이번 릴리스에서 해결되었습니다.

## 프로덕션 릴리스

| **문제 유형** | **구성 요소** | **릴리스 노트** |
|---|---|---|
| 버그 | 미디어 담벼락 | 스트림 규칙에서 Instagram 게시물을 추가할 때 태그를 클릭할 수 없는 미디어 담벼락 문제를 해결했습니다. |
| 버그 | MODQ | MODQ가 제대로 로드되지 않는 문제가 해결되었습니다. |
| 버그 | MODQ | 오디오를 임베드하여 MODQ가 작동되지 않는 문제가 해결되었습니다. |

## UAT 릴리스

| **문제 유형** | **구성 요소** | **릴리스 노트** |
|---|---|---|
| 개선 사항 | 필름스트립 | 필름 스트립을 더 쉽게 액세스할 수 있도록 하는 문제가 해결되었습니다. |
| 개선 사항 | Studio | 이제 IMS 로그인을 사용하여 Livefyre에 로그인할 수 있습니다. |

