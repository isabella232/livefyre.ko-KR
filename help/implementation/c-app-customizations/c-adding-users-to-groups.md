---
description: 그룹에 사용자 태그를 추가하여 그룹에 사용자를 추가합니다.
seo-description: 그룹에 사용자 태그를 추가하여 그룹에 사용자를 추가합니다.
seo-title: 그룹에 사용자 추가
solution: Experience Manager
title: 그룹에 사용자 추가
uuid: 3633 f 2 df -8 d 60-4 cdd-b 9 a 2-3807218 c 74 a 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 그룹에 사용자 추가{#adding-users-to-groups}

그룹에 사용자 태그를 추가하여 그룹에 사용자를 추가합니다.

사용자 태그는 독점적 및 엔터프라이즈 프로필 시스템 모두에 대해 구현될 수 있으며, 몇 가지 방법을 통해 계정에 추가될 수 있습니다.

* Studio를 통해 소유자 및 중재자를 만들면'중재자'사용자 태그가 계정에 할당됩니다.
* 사용자 그룹을 만들고 Studio를 통해 사용자를 추가하면 선택한 사용자에게 그룹 이름이 있는 사용자 태그가 자동으로 적용됩니다.
* 사용자 태그는 사용자 태그 [추가 HTTP](https://api.livefyre.com/docs#add-user-tag) 호출 또는 풀링을 위한 Ping를 사용하여 계정에 직접 적용될 수도 있습니다.

>[!NOTE]
>
>API 메서드, HTTP 사용자 태그 호출 및 풀 방법에 대한 ping 메서드 모두 다른 방법을 통해 계정에 이전에 할당된 태그를 덮어씁니다. 따라서 한 방법을 선택하고 전체 프로세스에서 일관성 있게 사용하십시오.

## Studio의 사용자 페이지에서 그룹에 사용자 추가 {#section_qgq_nbw_xz}

* 사용자 이름 아래의 그룹 레이블을 클릭하거나 **[!UICONTROL Add Group]** 그룹 레이블을 클릭하여 그룹 메뉴를 엽니다.
* 목록을 스크롤하고 사용자를 추가할 그룹을 찾습니다. 드롭다운의 상단에 **[!UICONTROL Search]** 있는 상자에 그룹 이름을 입력할 수 있습니다.
* 사용자를 추가할 그룹 옆의 확인란을 클릭하고 Return 키를 누릅니다.

사용자의 프로필에는 그룹 이름 (사용자가 그룹에만 있는 경우) 이나 사용자가 속한 그룹 수가 표시됩니다.

## 사용자 태그 추가 호출을 사용하여 그룹에 사용자 추가 {#section_kn3_gbw_xz}

사용자의 lftoken 및 선택한 태그 이름을 post 요청으로 전달합니다.

예를 들면 다음과 같습니다.

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


자세한 내용은 API Reference > [Add User Tag](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)를 참조하십시오.

## 가져오기에 Ping를 사용하여 그룹에 사용자 추가 {#section_kyj_11w_xz}

태그 배열을 사용하여 사용자 그룹에 사용자를 할당합니다. (태그에는 영숫자 및 밑줄 문자가 1-63 개 포함될 수 있습니다.)

예를 들면 다음과 같습니다.

```
"tags": ["moderator", "brand_advocate"],
```

## 원격 프로필을 사용하여 그룹에 사용자 추가 {#section_uyn_scv_xz}

특정 사용자에 대해 사용자 지정 프로필 시스템과 Livefyre 간에 사용자 데이터를 동기화하는 데 사용되는 원격 프로필에 사용자 태그를 추가합니다.
