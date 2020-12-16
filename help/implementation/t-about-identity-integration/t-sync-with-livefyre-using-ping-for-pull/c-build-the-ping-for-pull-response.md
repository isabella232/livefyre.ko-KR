---
description: Ping for Pull 응답을 작성하여 업데이트된 사용자 정보를 Livefyre로 전송합니다.
seo-description: Ping for Pull 응답을 작성하여 업데이트된 사용자 정보를 Livefyre로 전송합니다.
seo-title: 풀링 응답에 대한 Ping 작성
solution: Experience Manager
title: 풀링 응답에 대한 Ping 작성
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 1%

---


# 풀 응답에 대한 Ping 작성{#build-the-ping-for-pull-response}

Ping for Pull 응답을 작성하여 업데이트된 사용자 정보를 Livefyre로 전송합니다.

| 유형 | 속성 | 설명 |
|--- |--- |--- |
| 문자열 *필수* | ID | 프로필 시스템에 있는 사용자의 사용자 ID. 이 값은 네트워크의 모든 사용자에 대해 고유해야 하며 절대 변경되어서는 안됩니다. |
| 문자열 *필수* | display_name | 사용자의 표시 이름입니다. 사용자가 게시한 Livefyre 콘텐츠로 렌더링됩니다. |
| 개체 *선택 사항이지만 권장* | 이름 | 사용자의 형식, 첫 번째, 중간 및 성을 정의하는 문자열입니다. |
| 문자열 *선택 사항이지만 권장* | 이메일 | 사용자의 이메일 주소입니다. 이메일 알림을 보내는 데 사용됩니다. |
| 문자열 *선택 사항이지만 권장* | image_url | 사용자를 위해 표시할 아바타의 URL. Livefyre는 업로드된 이미지의 크기를 100×100, 75×75 또는 50×50픽셀로 적절히 조정합니다. 최상의 결과를 얻으려면 100×100픽셀의 정사각형 이미지를 업로드해야 합니다. Livefyre에서 아바타 이미지를 업데이트하려면 각 이미지 업데이트에 대해 image_url을 수정하여 Pull에서 이미지가 변경되었음을 감지합니다. 예를 들어 파일 이름에 타임스탬프를 첨부하거나 이미지 변경 사항을 증가시킵니다. 참고: 모든 URL은 정규화된 URL이어야 하며 액세스 가능해야 합니다. |
| 문자열 *선택 사항이지만 권장* | profile_url | 사이트의 사용자 프로필 페이지에 대한 URL. |
| 문자열 *선택 사항이지만 권장* | settings_url | 사용자가 사이트에 대한 사용자의 프로필 설정을 구성할 수 있는 페이지의 URL. |
| 배열 *선택 사항이지만 권장* | 태그가 있는 세그먼트만 필터링할 수 있습니다 | 사용자 그룹에 사용자를 할당하는 데 사용됩니다. 태그에는 1-63개의 영숫자 및 밑줄 문자가 포함될 수 있습니다. |
| 부울 *선택 사항이지만 권장* | autofollow_conversations | 사용자가 컬렉션에 게시한 후 자동으로 컬렉션을 팔로우할지 여부를 정의합니다. 컬렉션을 팔로우하면 다른 사용자가 참가할 때 이메일 알림을 받게 됩니다. 참 또는 거짓 일 수 있습니다. 기본값은 true입니다. |
| 개체 *선택 사항이지만 권장* | email_notifications | 사용 가능한 Livefyre 이메일 알림의 빈도를 정의합니다. 각 알림 유형에 대해 서로 다른 주파수를 설정할 수 있습니다. 기본적으로 알림은 전송되지 않습니다.<br><ul><li> 나열된 이벤트 즉시 알림을 발행합니다. </li><li>종종 알림을 일괄로 발행합니다. </li><li> 활동에 대한 이메일 알림은 전송하지 않습니다. </li><li>*댓글*:다른 사용자가 이 사용자가 팔로우하는 콘텐츠를 컬렉션에 게시할 때 알림이 전송되는 시기를 정의합니다. </li><li>*답글*:다른 사용자가 이 사용자의 콘텐츠에 응답할 때 알림이 전송되는 시기를 정의합니다.</li><li>*좋아요*:다른 사용자가 이 사용자의 콘텐트를 좋아하는 경우 알림이 전송되는 시기를 정의합니다.</li><li>*consortium_comments*:사용자가 네트워크의 모든 컬렉션에 컨텐츠를 게시할 때 중재자에게 알림이 전송되는 시기를 정의합니다.</li><li>*advertiser_flags*:다른 사용자가 네트워크의 모든 컬렉션의 콘텐츠를 플래그를 지정할 때 중재자에게 알림이 전송되는 시기를 정의합니다.</li></ul> |
| 문자열 *선택적* | 위치 | 사용자가 제출한 위치입니다. |
| 문자열 *선택적* | 소개 | 사용자가 제출한 자서전. |
| 배열 *선택 사항* | 웹 사이트 | 사용자가 제출한 일련의 사이트입니다. 최대 = 2. |
| 개체 *선택적* | display_rules | 다른 사용자가 공개적으로 볼 수 있는 프로필 속성을 정의합니다. 사용할 수 있는 각 매개 변수는 부울 입력 true 또는 false를 사용합니다. 사용 가능한 매개 변수: <br><ul><li>소개 </li><li> 위치</li><li>  성별 </li><li>이름 이미지 </li><li> remote_profile_url</li></ul> |
| 부울 *선택적* | 중재자 | 사용자가 네트워크 전반에 걸쳐 중재자 권한을 가지고 있는지 여부를 정의합니다. |
| 부울 *선택적* | gravatar_disabled | image_url을 제공하지 않은 경우 Livefyre의 gravatar 사용을 비활성화할지 여부를 정의합니다. |

## 응답 예 {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
