---
description: 2018년 11월 15일 릴리스에 대한 릴리스 노트입니다.
seo-description: 2018년 11월 15일 릴리스에 대한 릴리스 노트입니다.
seo-title: 릴리스 노트
solution: Experience Manager
title: 릴리스 노트
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 릴리스 노트{#release-notes}

2018년 11월 15일 릴리스에 대한 릴리스 노트입니다.

## 새로운 기능 {#section_syx_mdt_wcb}

이번 릴리스의 프로덕션 버전에서 다음과 같은 새로운 기능이 릴리스되었습니다.

* **Instagram 검색 및 스트림 업데이트** Instagram *비즈니스 계정을* 사용하여 다음을 수행할 수 있습니다.

   * 사용자별로 Instagram 소셜 검색 수행(사용자는 Instagram 비즈니스 계정이어야 함)

   * 사용자 계정을 포함하여 특정 Instagram 사용자 계정에서 Instagram 스트림을 만듭니다(계정도 비즈니스 계정이어야 함).

   * 부분적으로 자동화된 워크플로우를 사용하여 Instagram에서 에셋에 대한 권한 요청

   * Instagram에서 권한을 설정하고 요청하는 데 필요한 Instagram 계정 유형에 대한 자세한 내용은 Instagram 계정 [정보를 참조하십시오](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **비즈니스 계정 기반 검색에 대한 사용 권한 요청 응답을 자동으로 모니터링합니다.** 비즈니스 계정 기반 검색만 해당—권한 요청에 대한 응답을 자동으로 모니터링하고 Livefyre에서 활동 내역을 업데이트하는 기능을 사용할 수 있습니다.

Instagram 계정에 대한 권한을 요청하는 방법에 대한 자세한 내용은 Instagram Rights Request 수동 [보내기 및](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) 부분적으로 자동화된 [Instagram Rights Request 보내기를 참조하십시오](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Adobe Target 통합.** Adobe Target과의 통합을 통해 Livefyre 앱을 Adobe Target 오퍼 라이브러리에 직접 공유할 수 있습니다. Adobe Target에서 Livefyre 사용에 대한 자세한 내용은 Target [설명서를](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html)참조하십시오.

## 문제 {#section_ehw_ndt_wcb}

다음 표의 문제가 이번 릴리스에서 해결되었습니다.

### 프로덕션 릴리스

| 문제 유형 | 구성 요소 | 릴리스 노트 |
|--- |--- |--- |
| 문제 | AppService:Livefyre Identity | 클릭 [시 발생하는 문제가 해결되었습니다. UICONTROL Reset to] Default가 Studio &gt; 통합 설정 &gt; Livefyre Identity의 로그인 모달 아래에 있는 로고를 기본 이미지로 재설정하지 않았습니다. |
| 문제 | 라이브러리 | 라이브러리에 업로드된 후 자산 세부 정보로 본 비디오가 제대로 표시되지 않는 문제를 해결했습니다. |
| 문제 | 스트림 | 제품이 스트림 규칙에 표시되지 않는 문제를 해결했습니다. |
| 문제 | 스트림 | 스트림 규칙에 제품 태그를 사용할 수 없던 문제를 수정했습니다. |
| 개선 사항 | Studio | Livefyre 스튜디오에서 제품 ID가 표시되지 않는 문제를 해결했습니다. |
| 문제 | 스튜디오:ModQ | 삭제된 컨텐츠가 삭제된 후에도 ModQ에 계속 표시되는 문제를 해결했습니다. |

### UAT 릴리스

| **문제 유형** | **구성 요소** | **릴리스 노트** |
|---|---|---|
| 문제 | 소셜 구성 요소:회전판 | 공유 링크가 IE11 및 Mozilla Firefox에서 예상한 대로 URL을 복사하지 않던 문제를 수정했습니다. |