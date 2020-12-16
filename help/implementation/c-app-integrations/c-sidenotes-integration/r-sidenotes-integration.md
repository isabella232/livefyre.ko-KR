---
description: 핵심 애플리케이션과 유사한 프로세스를 수행하여 Sidecotes 앱을 통합합니다.
seo-description: 핵심 애플리케이션과 유사한 프로세스를 수행하여 Sidecotes 앱을 통합합니다.
seo-title: 사이드노트 통합
solution: Experience Manager
title: 사이드노트 통합
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---


# 사이드노트 통합{#sidenotes-integration}

핵심 애플리케이션과 유사한 프로세스를 수행하여 Sidecotes 앱을 통합합니다.

일반적으로 핵심 응용 프로그램 통합이 완료된 경우 `collectionMeta` 개체를 생성하기 위해 작성된 코드를 사이드노트에 다시 사용할 수 있습니다.

`fyre.conv`로 만든 `auth` 대리자를 (선택 사항) `authDelegate` 필드에서 사이드노트에 제공하여 기존 `auth` 대리자를 재사용할 수도 있습니다.

>[!NOTE]
>
>사이드노트는 생성자의 다른 부분에 별도로 전달하는 대신 단일 객체에 `network`, `siteId` 및 `articleId`를 포함할 수 있습니다.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

`collectionMeta` 빌드 섹션에 설명된 대로 `collectionMeta`은(는) 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT로 인코딩되기 전에 다음 형식을 취합니다.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

자세한 내용은 `collectionMeta` 토큰을 참조하십시오.

## 모바일 설정

사이드노트는 모바일 장치에서 사용하도록 최적화되었습니다. 모바일 버전의 Livefyre 앱을 사용하여 최상의 결과를 얻으려면 사용자 확장 가능 옵션을 no로 설정합니다. 예:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
