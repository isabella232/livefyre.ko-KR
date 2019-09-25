---
description: 사용자 태그를 계정에 추가하여 그룹에 사용자를 추가합니다.
seo-description: 사용자 태그를 계정에 추가하여 그룹에 사용자를 추가합니다.
seo-title: 그룹에 사용자 추가
solution: Experience Manager
title: 그룹에 사용자 추가
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Adding Users to Groups{#adding-users-to-groups}

사용자 태그를 계정에 추가하여 그룹에 사용자를 추가합니다.

사용자 태그는 전용 및 엔터프라이즈 프로파일 시스템 모두에 대해 구현될 수 있으며, 다음과 같은 여러 가지 방법으로 계정에 추가할 수 있습니다.

* Studio를 통해 소유자 및 중재자를 만들면 계정에 '중재자' 사용자 태그를 할당합니다.
* 사용자 그룹을 만들고 Studio를 통해 사용자 그룹에 사용자를 추가하면 선택한 사용자에게 그룹 이름이 있는 사용자 태그가 자동으로 적용됩니다.
* 사용자 태그는 사용자 태그 HTTP 추가 [호출 또는 풀링용](https://api.livefyre.com/docs#add-user-tag) Ping을 사용하여 계정에 직접 적용할 수도 있습니다.

>[!NOTE]
>
>API 메서드, HTTP Add User Tag 호출 및 Ping for Pull 메서드는 모두 이전에 계정에 할당된 태그를 다른 방법으로 덮어씁니다. 따라서 한 가지 방법을 선택하고 프로세스 전체에서 일관되게 사용하십시오.

## Studio의 사용자 페이지에서 그룹에 사용자 추가 {#section_qgq_nbw_xz}

* 사용자 이름 **[!UICONTROL Add Group]** 아래의 그룹 레이블을 클릭하거나 클릭하여 그룹 메뉴를 엽니다.
* 목록을 스크롤하여 사용자를 추가할 그룹을 찾습니다. 드롭다운 맨 위의 **[!UICONTROL Search]** 상자에 그룹 이름을 입력할 수 있습니다.
* 사용자를 추가할 그룹 옆의 확인란을 클릭하고 Return 키를 누릅니다.

사용자의 프로필에는 그룹 이름(사용자가 한 그룹에만 있는 경우) 또는 사용자가 속한 그룹 수가 표시됩니다.

## 사용자 태그 추가 호출을 사용하여 그룹에 사용자 추가 {#section_kn3_gbw_xz}

사용자의 LFToken 및 선택한 태그 이름을 POST 요청으로 전달합니다.

예:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


자세한 내용은 API 참조 &gt; 사용자 태그 [추가를 참조하십시오](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Pip for Pull을 사용하여 그룹에 사용자 추가 {#section_kyj_11w_xz}

태그 배열을 사용하여 사용자 그룹에 사용자를 할당합니다. (태그에는 1-63개의 영숫자 및 밑줄 문자가 포함될 수 있습니다.)

예:

```
"tags": ["moderator", "brand_advocate"],
```

## 원격 프로필을 사용하여 그룹에 사용자 추가 {#section_uyn_scv_xz}

사용자 지정 프로필 시스템과 Livefyre 간 사용자 데이터를 동기화하는 데 사용되는 사용자 태그를 원격 프로필에 추가합니다.
