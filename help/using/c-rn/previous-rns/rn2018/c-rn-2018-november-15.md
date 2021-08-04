---
description: 2018년 11월 15일 릴리스의 릴리스 노트.
title: 릴리스 정보
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 6%

---

# 릴리스 정보{#release-notes}

2018년 11월 15일 릴리스의 릴리스 노트.

## 새로운 기능 {#section_syx_mdt_wcb}

이 릴리스의 프로덕션 버전에서 다음과 같은 새로운 기능이 릴리스되었습니다.

* **instagram 검색 및 스트림에 대한 업데이트입니다.**  *Instagram 비즈니스 계정을 사용하여 다음을 수행할 수* 있습니다.

   * 사용자별로 Instagram 소셜 검색을 수행합니다(사용자는 Instagram 비즈니스 계정이어야 함).

   * 사용자를 포함하여 특정 Instagram 사용자 계정(계정도 비즈니스 계정이어야 함)에서 Instagram 스트림을 만듭니다.

   * 부분적으로 자동화된 워크플로우를 사용하여 Instagram에서 자산에 대한 권한을 요청합니다.

   * instagram에서 권한을 설정 및 요청하는 데 필요한 Instagram 계정 유형에 대한 자세한 내용은 [Instagram 계정 정보](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)를 참조하십시오.

* **비즈니스 계정 기반 검색에 대한 사용 권한 요청 응답 자동 모니터링** 비즈니스 계정 기반 검색만 해당—권한 요청에 대한 응답을 자동으로 모니터링하고 Livefyre의 활동 내역을 업데이트하는 기능을 사용할 수 있습니다.

instagram 계정에 대한 권한을 요청하는 방법에 대한 자세한 내용은 [Instagram 권한 요청을 수동으로 보내기](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) 및 [부분적으로 자동화된 Instagram 권한 요청 보내기](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)를 참조하십시오.

* **Adobe Target 통합.** Livefyre 앱을 Adobe Target 오퍼 라이브러리에 직접 공유할 수 있는 Adobe Target와의 통합을 추가했습니다. Adobe Target과 함께 Livefyre를 사용하는 방법에 대한 자세한 내용은 [Target 설명서](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html)를 참조하십시오.

## 문제 {#section_ehw_ndt_wcb}

다음 테이블의 문제는 이 릴리스에서 해결되었습니다.

### 프로덕션 릴리스

| 문제 유형 | 구성 요소 | 릴리스 노트 |
|--- |--- |--- |
| 문제 | 앱 서비스: Livefyre Identity | [!UICONTROL Reset to Default]을 클릭해도 Studio > Integration Settings > Livefyre Identity의 로그인 모달 아래에 있는 로고가 기본 이미지로 재설정되지 않는 문제가 해결되었습니다. |
| 문제 | 라이브러리 | 라이브러리에 업로드한 다음 자산 세부 사항으로 본 비디오가 올바르게 표시되지 않는 문제가 해결되었습니다. |
| 문제 | 스트림 | 스트림 규칙에 제품이 표시되지 않는 문제를 해결했습니다. |
| 문제 | 스트림 | 스트림 규칙에 제품 태그를 사용할 수 없던 문제를 수정했습니다. |
| 개선 사항 | Studio | 제품 ID가 Livefyre Studio에 표시되지 않는 문제가 수정되었습니다. |
| 문제 | 스튜디오: ModQ | 삭제된 콘텐츠가 삭제된 후에도 ModQ에 계속 표시되는 문제를 해결했습니다. |

### UAT 릴리스

| **문제 유형** | **구성 요소** | **릴리스 노트** |
|---|---|---|
| 문제 | 소셜 구성 요소: 회전판 | 공유 링크가 IE11 및 Mozilla Firefox에서 예상대로 URL을 응답하지 않고 복사하던 문제가 수정되었습니다. |
