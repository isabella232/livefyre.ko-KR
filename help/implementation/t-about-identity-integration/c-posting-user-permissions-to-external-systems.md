---
description: Livefyre는 PUSH 인터페이스를 사용하여 사용자 권한 변경 사항에 대한 외부 시스템 정보를 보냅니다.
seo-description: Livefyre는 PUSH 인터페이스를 사용하여 사용자 권한 변경 사항에 대한 외부 시스템 정보를 보냅니다.
seo-title: 외부 시스템에 사용자 권한 게시(선택 사항)
solution: Experience Manager
title: 외부 시스템에 사용자 권한 게시(선택 사항)
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---


# 외부 시스템에 사용자 권한 게시(선택 사항){#posting-user-permissions-to-external-systems-optional}

Livefyre는 PUSH 인터페이스를 사용하여 사용자 권한 변경 사항에 대한 외부 시스템 정보를 보냅니다.

## Livefyre 스튜디오의 사용자 유형

| 사용자 유형 | 설명 |
|--- |--- |
| 소유자 | 이 사용자는 소유자이며, 컨텐츠를 중재하고 새 중재자를 할당할 수 있습니다. |
| admin | 이 사용자는 중재자이며 컨텐츠를 중재할 수 있습니다. |
| 회원 | 이 사용자는 허용 목록에 표시됩니다. 게시된 컨텐츠는 스팸 또는 비속어 필터를 통과하지 않으며 중재된 전 스트림에서 승인을 필요로 하지 않습니다. |
| 없음 | 이 사용자는 표준 사용자이며 특별한 권한이 없습니다. |
| 왕따 | 이 사용자는 대화에 참여할 수 없습니다. |

외부 시스템에 사용자 권한을 게시하려면 POST 요청으로 권한 데이터를 받는 URL을 등록해야 합니다.

예:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| 매개 변수 | 설명 |
|--- |--- |
| networkName | Livefyre에서 네트워크 이름을 제공했습니다. |
| 토큰 | 유효한 시스템 토큰입니다. |
| url | 등록할 URL입니다. |

등록된 URL은 다음 데이터가 있는 POST를 컨텐츠 유형으로 허용해야 합니다.application/x-www-form-urlencoded.

| 매개 변수 | 설명 |
|--- |--- |
| jid | 가입이 변경된 사용자의 JID. JID는 `user_id@network` 형식의 문자열입니다. |
| 소속자 | 할당된 권한 이름(다음 중 하나여야 함): `{admin | member | none | outcast | owner}` |

사용자 제휴 설정 업데이트에 대한 자세한 내용은 [사용자 제휴 API 참조 추가](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)를 참조하십시오.
