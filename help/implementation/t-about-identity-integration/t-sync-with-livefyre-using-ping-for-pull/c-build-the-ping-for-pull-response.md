---
description: 풀 응답에 대한 Ping를 빌드하여 업데이트된 사용자 정보를 Livefyre로 전송합니다.
seo-description: 풀 응답에 대한 Ping를 빌드하여 업데이트된 사용자 정보를 Livefyre로 전송합니다.
seo-title: 풀 응답에 대한 Ping 만들기
solution: Experience Manager
title: 풀 응답에 대한 Ping 만들기
uuid: f 90871 d 5-601 f -40 dc-b 3 d 2-ab 78635 e 4 a 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 풀 응답에 대한 Ping 만들기{#build-the-ping-for-pull-response}

풀 응답에 대한 Ping를 빌드하여 업데이트된 사용자 정보를 Livefyre로 전송합니다.

| type | property | 설명 |
|--- |--- |--- |
| 문자열 *필요* | ID | 프로필 시스템에서 사용자의 사용자 ID 입니다. 이 기능은 네트워크의 모든 사용자에 대해 고유해야 하며 절대 변경되지 않아야 합니다. |
| 문자열 *필요* | display_ name | 사용자의 표시 이름입니다. 이는 사용자가 게시한 Livefyre 컨텐츠로 렌더링됩니다. |
| 개체 *선택 사항이지만 권장* | name | 문자열을 사용하여 사용자의 형식, 처음, 중간 및 성을 정의합니다. |
| 문자열 *선택 사항이지만 권장* | 이메일 | 사용자의 이메일 주소입니다. 이메일 알림을 보내는 데 사용됩니다. |
| 문자열 *선택 사항이지만 권장* | image_ url | 사용자에 대해 표시할 아바타에 대한 URL 입니다. Livefyre는 업로드한 이미지의 크기를 100 × 100, 75 × 75 또는 50 × 50 픽셀로 조정합니다. 최상의 결과를 얻으려면 100 × 100 픽셀에서 정사각형 이미지를 업로드해야 합니다. Livefyre에서 아바타 이미지가 업데이트되도록 하려면 각 이미지 업데이트에 대한 image_ url를 수정하여 풀링에 대한 ping 이 이미지가 변경되었음을 감지합니다. 예를 들어 타임스탬프를 파일 이름에 첨부하거나 이미지를 증가시킵니다. 참고: 모든 URL는 완벽하게 유효하고 액세스 가능해야 합니다. |
| 문자열 *선택 사항이지만 권장* | profile_ url | 사이트의 프로필 페이지에 대한 URL 입니다. |
| 문자열 *선택 사항이지만 권장* | settings_ url | 사용자가 사이트에 대한 사용자의 프로필 설정을 구성할 수 있는 페이지에 대한 URL. |
| Array *optional, but recommended* | 태그 | 사용자 그룹에 사용자를 할당하는 데 사용됩니다. 태그에는 1-63 개의 영숫자 및 밑줄 문자가 포함될 수 있습니다. |
| 부울 *선택 사항이지만 권장됨* | autofollow_ conversations | 사용자가 게시물을 게시한 후 자동으로 팔로우할지 여부를 정의합니다. 컬렉션을 팔로우하면 다른 사용자가 참여할 때 이메일 알림을 받게 됩니다. true 또는 false 일 수 있습니다. 기본값은 true 입니다. |
| 개체 *선택 사항이지만 권장* | email_ notifications | 사용 가능한 Livefyre 이메일 알림 빈도를 정의합니다. 각 알림 유형에 대해 서로 다른 주파수가 설정될 수 있습니다. 기본적으로 알림이 전송되지 않습니다. <br><ul><li> 나열된 이벤트 즉시 즉시 알림을 발행합니다. </li><li>종종 알림을 일괄적으로 발행합니다. </li><li> 활동에 대한 이메일 알림을 보내지 않습니다. </li><li>*댓글*: 다른 사용자가 이 사용자가 팔로우하는 컬렉션에 컨텐츠를 게시할 때 알림이 전송되는 시기를 정의합니다. </li><li>*답글*: 다른 사용자가 이 사용자의 컨텐트에 답글을 달 때 알림이 전송될 시기를 정의합니다.</li><li>*좋아요*: 다른 사용자가 이 사용자의 콘텐트를 좋아하면 알림이 전송될 시기를 정의합니다.</li><li>*moderator_ comments*: 사용자가 네트워크에서 임의의 컬렉션에 컨텐츠를 게시할 때 알림이 중재자에게 전송되는 시기를 정의합니다.</li><li>*moderator_ flags*: 다른 사용자가 네트워크에서 컬렉션의 콘텐츠를 플래그로 지정하면 알림이 중재자에게 전송될 시기를 정의합니다.</li></ul> |
| 문자열 *선택 사항* | 위치 | 사용자가 제출한 위치입니다. |
| 문자열 *선택 사항* | 소개 | 사용자가 제출한 자서전 |
| Array *optional* | 웹 사이트 | 사용자가 제출한 다양한 사이트 max = 2. |
| 개체 *선택 사항* | display_ rules | 다른 사용자에게 공개적으로 표시되는 프로필 속성을 정의합니다. 사용 가능한 각 매개 변수는 부울 입력 true 또는 false를 사용합니다. 사용 가능한 매개 변수: <br><ul><li>소개 </li><li> 위치</li><li>  성별 </li><li>Nameimage </li><li> REMOTE_ PROFILE_ URL</li></ul> |
| 부울 *선택 사항* | 중재자 | 사용자가 네트워크를 통해 중재자 권한을 가지고 있는지 여부를 정의합니다. |
| 부울 *선택 사항* | gravatar_ disabled | image_ url 이 제공되지 않을 경우 Livefyre의 Gravatar 사용을 비활성화할지 여부를 정의합니다. |

## 예제 응답 {#section_uxt_3dd_mz}

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
