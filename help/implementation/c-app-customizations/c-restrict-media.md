---
description: 앱 스트림에 들어오는 미디어 유형을 제한합니다.
seo-description: 앱 스트림에 들어오는 미디어 유형을 제한합니다.
seo-title: 미디어 제한
solution: Experience Manager
title: 미디어 제한
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 미디어 제한{#restrict-media}

앱 스트림에 들어오는 미디어 유형을 제한합니다.

기본적으로 모든 미디어 첨부 파일을 앱에 포함할 수 있습니다. Livefyre를 사용하면 사용자가 선택한 첨부 파일 유형을 앱에 게시하지 못하도록 이 옵션을 변경할 수 있습니다.

>[!NOTE]
>
>Livefyre와 Embeddly를 함께 사용하여 미디어 통합 자세한 내용은 컨텐츠 통합 &gt; 내장 통합을 참조하십시오. 링크 확장 또는 출처에 대한 질문은 기술 계정 관리자에게 문의하십시오.

이 예제에서는 YouTube 및 Vimeo가 댓글 스트림에서 포함된 내용을 차단합니다.

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

대화를 로드할 때:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

