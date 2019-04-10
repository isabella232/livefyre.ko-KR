---
description: 2018 년 11 월 15 일 릴리스에 대한 릴리스 노트.
seo-description: 2018 년 11 월 15 일 릴리스에 대한 릴리스 노트.
seo-title: 릴리스 노트
solution: Experience Manager
title: 릴리스 노트
uuid: 34 E 64943-DEA 6-46 AC -9 FCC -8 FEBEAB 6 AA 42
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 릴리스 노트{#release-notes}

2018 년 11 월 15 일 릴리스에 대한 릴리스 노트.

## 새로운 기능 {#section_syx_mdt_wcb}

이 릴리스의 프로덕션 버전에서 다음과 같은 새로운 기능이 출시되었습니다.

* **Instagram 검색 및 스트림 업데이트***Instagram 비즈니스 계정을* 사용하여 다음을 수행할 수 있습니다.

   * 사용자별 Instagram 소셜 검색을 수행합니다 (사용자는 Instagram 비즈니스 계정이어야 함).

   * 고유한 Instagram 사용자 계정 (계정은 비즈니스 계정이어야 함) 에서 Instagram 스트림을 직접 만듭니다.

   * 부분적으로 자동화된 워크플로우를 사용하여 Instagram의 자산에 대한 권한을 요청합니다.

   * Instagram에서 권한을 설정하고 요청하는 데 필요한 Instagram 계정 유형에 대한 자세한 내용은 Instagram 계정 [정보를 참조하십시오](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **비즈니스 계정 기반 검색을 위한 사용 권한 요청 응답의 자동 모니터링** 비즈니스 계정 기반 검색에만 해당—Livefyre에서 권한 요청에 대한 응답을 자동으로 모니터링하고 활동 내역을 업데이트할 수 있습니다.

Instagram 계정에 대한 권한을 요청하는 방법에 대한 자세한 내용은 Instagram [권한 요청 수동](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) 전송을 [참조하고 부분적으로 자동화된 Instagram 권한 요청을](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)보내십시오.

* **Adobe Target 통합.** Adobe Target 과의 통합을 추가하여 Livefyre 앱을 Adobe Target 오퍼 라이브러리에 바로 공유할 수 있게 되었습니다. Adobe Target에서 Livefyre를 사용하는 방법에 대한 자세한 내용은 [대상 설명서를](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html)참조하십시오.

## 문제 {#section_ehw_ndt_wcb}

다음 표의 문제가 이번 릴리스에서 해결되었습니다.

### 프로덕션 릴리스

| 문제 유형 | 구성 요소 | 릴리스 노트 |
|--- |--- |--- |
| 문제 | Appservice: Livefyre Identity | [클릭되는 문제가 해결되었습니다. Uicontrol를 기본값으로] 재설정해도 Studio > 통합 설정 > Livefyre ID의 로그인 모형이 기본 이미지에 재설정되지 않았습니다. |
| 문제 | 라이브러리 | 라이브러리에 업로드한 다음 자산 세부 사항에서 본 비디오가 올바르게 표시되지 않았던 문제를 수정했습니다. |
| 문제 | 스트림 | 스트림 규칙에 제품이 표시되지 않는 문제를 해결했습니다. |
| 문제 | 스트림 | 스트림 규칙에 제품 태그를 사용할 수 없던 문제를 수정했습니다. |
| 개선 사항 | Studio | Livefyre 스튜디오에 제품 ID가 표시되지 않는 문제가 해결되었습니다. |
| 문제 | Studio: MODQ | 삭제된 컨텐츠가 삭제된 후 modq에 여전히 표시되던 문제를 수정했습니다. |

### UAT 릴리스

| **문제 유형** | **구성 요소** | **릴리스 노트** |
|---|---|---|
| 문제 | 소셜 구성 요소: 회전판 | IE 11 및 Mozilla Firefox에서 공유 링크가 응답하지 않고 URL를 예상대로 복사하던 문제가 해결되었습니다. |