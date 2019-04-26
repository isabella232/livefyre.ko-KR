---
description: 코어 애플리케이션과 유사한 프로세스를 수행하여 Sidenotes 앱을 통합합니다.
seo-description: 코어 애플리케이션과 유사한 프로세스를 수행하여 Sidenotes 앱을 통합합니다.
seo-title: Sidenotes 통합
solution: Experience Manager
title: Sidenotes 통합
uuid: 4 AA 14 ADA -402 A -482 D-B 43 E -96 F 37 AFA 6 C 53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Sidenotes 통합{#sidenotes-integration}

코어 애플리케이션과 유사한 프로세스를 수행하여 Sidenotes 앱을 통합합니다.

일반적인 규칙으로, 핵심 애플리케이션 통합이 완료된 경우 `collectionMeta` , 개체를 생성하기 위해 작성된 코드는 Sidenotes에 재사용할 수 있습니다.

(선택 사항) 필드에 Sidenotes로 작성된 대리자를 제공하여 기존 `auth``auth``fyre.conv` 대리자를 재활용할 `authDelegate` 수도 있습니다.

>[!NOTE]
>
>Sidenotes를 사용하면 생성자의 다른 부분에서 별도로 전달하는 것이 아니라, 단일 개체에 `network`포함 `siteId``articleId` 및 포함할 수 있습니다.

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

작성 `collectionMeta` 섹션에 명시된 대로 `collectionMeta` 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT 인코딩하기 전에 다음 형식을 사용합니다.

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

Sidenotes는 모바일 장치에서 사용하도록 최적화되었습니다. Livefyre 앱의 모바일 버전에서 최상의 결과를 얻으려면 [사용자 확장 가능] 옵션을 [아니요] 로 설정하십시오. 예를 들면 다음과 같습니다.

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
