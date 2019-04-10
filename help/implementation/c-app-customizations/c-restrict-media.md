---
description: 앱 스트림에 들어가는 미디어 유형을 제한하십시오.
seo-description: 앱 스트림에 들어가는 미디어 유형을 제한하십시오.
seo-title: 미디어 제한
solution: Experience Manager
title: 미디어 제한
uuid: C 470 C 985-D 221-4 F 39-8 BD 4-4 E 44 EC 14 DB 95
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 미디어 제한{#restrict-media}

앱 스트림에 들어가는 미디어 유형을 제한하십시오.

기본적으로 모든 미디어 첨부 파일을 앱에 포함할 수 있습니다. Livefyre를 사용하면 사용자가 선택한 첨부 파일 유형을 앱에 게시하지 못하도록 이 옵션을 변경할 수 있습니다.

>[!NOTE]
>
>미디어 통합을 위한 Livefyre 파트너 자세한 내용은 컨텐츠 통합 > Embedly 통합을 참조하십시오. 링크 확장 또는 소스에 대한 질문은 기술 계정 관리자에게 문의하십시오.

이 예에서는 YouTube와 Vimeo가 주석 스트림에서 삽입하는 블록을 차단합니다.

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

