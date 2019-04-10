---
description: 기능 API를 사용하여 프로세스 자동화
seo-description: 기능 API를 사용하여 프로세스 자동화
seo-title: 기능 API
title: 기능 API
uuid: EAC 3 A 156-0 B 60-4 FFA -8 B 6 F-E 451 EB 03 DA 77
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 기능 API{#feature-apis}

기능 API를 사용하여 프로세스 자동화

기능 API를 사용하여 컨텐츠가 특징인 프로세스를 자동화할 수 있습니다. 예를 들어, 라이브 블로그 또는 댓글 앱을 만들 때 선택한 중재자가 게시한 모든 컨텐트를 포함하여 대화를 유도하고 스트림 내에 일관성을 설정합니다.

Livefyre는 기능 및 기능 API를 모두 제공합니다.

## 기능 {#section_jpw_nqw_xz}

**리소스**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

선택한 중재자에 대한 사용자 토큰을 입력합니다.

**게시물 데이터**

```
{value: <number>} 
```

이 값은 주요 컨텐트를 가장 큰 것부터 가장 작은 값으로 정렬하는 데 사용됩니다 (특별 컨텐츠 목록에 1 이전 표시). 이 값은 기본적으로 Epoch **시간으로** 지정되므로 주요 댓글은 일반적으로 최신 항목순으로 정렬됩니다.

**예제 응답**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>데이터 필드는 아직 사용되지 않습니다.

## Unfunctionality {#section_knh_mqw_xz}

**리소스**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

선택한 중재자에 대한 사용자 토큰을 입력합니다.

**예제 응답**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>데이터 필드는 아직 사용되지 않습니다.

