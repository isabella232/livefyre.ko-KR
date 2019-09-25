---
description: 기능 API를 사용하여 프로세스 자동화
seo-description: 기능 API를 사용하여 프로세스 자동화
seo-title: 기능 API
title: 기능 API
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 기능 API{#feature-apis}

기능 API를 사용하여 프로세스 자동화

Feature API를 사용하여 컨텐츠가 특징에 맞게 프로세스를 자동화할 수 있습니다. 예를 들어 라이브 블로그 또는 댓글 앱을 만들 때 선택한 중재자가 게시한 모든 컨텐츠를 제공하여 대화를 조정하고 스트림 내에서 일관성을 유지할 수 있습니다.

Livefyre는 기능 및 기능 해제 API를 모두 제공합니다.

## 기능 {#section_jpw_nqw_xz}

**리소스**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

선택한 중재자의 사용자 토큰을 &#x200B; 입력합니다.

**게시물 데이터**

```
{value: <number>} 
```

이 값은 주요 컨텐츠를 정렬하는 데 사용됩니다. 가장 큰 콘텐츠에서 가장 작은 콘텐츠(주요 콘텐트 목록에서 1 앞에 10개가 표시됨) 이 값의 기본값은 **현재** epoch 시간으로 설정되므로 특집 주석은 일반적으로 가장 최근에서 가장 오래된 주석으로 정렬됩니다.

**응답 예**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>데이터 필드가 아직 사용 중이 아닙니다.

## 기능 해제 {#section_knh_mqw_xz}

**리소스**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

선택한 중재자의 사용자 토큰을 입력합니다.

**응답 예**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>데이터 필드가 아직 사용 중이 아닙니다.

