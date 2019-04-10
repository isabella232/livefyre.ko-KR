---
description: Livefyre는 푸시 인터페이스를 사용하여 사용자 권한에 대한 변경 사항에 대한 외부 시스템 정보를 전송합니다.
seo-description: Livefyre는 푸시 인터페이스를 사용하여 사용자 권한에 대한 변경 사항에 대한 외부 시스템 정보를 전송합니다.
seo-title: 외부 시스템에 사용자 권한 게시 (선택 사항)
solution: Experience Manager
title: 외부 시스템에 사용자 권한 게시 (선택 사항)
uuid: 9 C 18 B 20 D -3 B 93-4666-B 7 DE -1 EC 60318 CF 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 외부 시스템에 사용자 권한 게시 (선택 사항){#posting-user-permissions-to-external-systems-optional}

Livefyre는 푸시 인터페이스를 사용하여 사용자 권한에 대한 변경 사항에 대한 외부 시스템 정보를 전송합니다.

## Livefyre Studio의 사용자 유형

| 사용자 유형 | 설명 |
|--- |--- |
| 소유자 | 이 사용자는 소유자이며, 컨텐츠를 중재하고 새 중재자를 지정할 수 있습니다. |
| admin | 이 사용자는 중재자이며 컨텐츠를 중재할 수 있습니다. |
| 멤버 | 이 사용자는 화이트리스트에 포함됩니다. 게시된 컨텐츠는 스팸 또는 비속어 필터를 통과하지 않으며 미리 조정된 스트림에서 승인을 필요로 하지 않습니다. |
| 없음 | 이 사용자는 표준 사용자이며 특별한 권한이 없습니다. |
| outcast | 이 사용자는 대화에 참여하지 못하게 되었습니다. |

외부 시스템에 사용자 권한을 게시하려면 권한 데이터를 게시물 요청으로 받는 URL를 등록해야 합니다.

예를 들면 다음과 같습니다.

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| 매개 변수 | 설명 |
|--- |--- |
| Networkname | Livefyre가 네트워크 이름을 제공했습니다. |
| 토큰 | 유효한 시스템 토큰. |
| URL | 등록할 URL. |

등록된 URL는 다음과 같은 데이터가 포함된 게시물을 컨텐츠 유형으로 수락해야 합니다. application/x-www-form-urlencoded.

| 매개 변수 | 설명 |
|--- |--- |
| JID | 제휴 변경이 변경된 사용자의 JID. JID는 양식의 `user_id@network`문자열입니다. |
| 제휴 | 할당된 권한의 이름 (다음 중 하나여야 함: `{admin | member | none | outcast | owner}` |

사용자 제휴 설정 업데이트에 대한 자세한 내용은 사용자 제휴 API 참조 [추가를](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)참조하십시오.
