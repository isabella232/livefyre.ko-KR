---
description: Javascript 이벤트를 사용하여 미디어 담벼락에서 발생하는 이벤트를 수신하고 원하는 분석 툴로 전송할 수 있습니다.
title: 미디어 담벼락에 대한 Javascript 이벤트
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# 미디어 담벼락에 대한 Javascript 이벤트{#javascript-events-for-media-wall}

Javascript 이벤트를 사용하여 미디어 담벼락에서 발생하는 이벤트를 수신하고 원하는 분석 툴로 전송할 수 있습니다.

Livefyre는 Livefyre 앱의 사용자 활동을 추적하는 JavaScript 이벤트를 제공합니다. 예를 들어 사용자가 Twitter 또는 Facebook에 컨텐츠를 좋아하거나 공유할 때 또는 새 컨텐츠가 게시될 때 페이지를 업데이트할 수 있습니다.

다음은 이벤트를 수신하는 방법의 예입니다. 이벤트를 매핑하고 분석 통합으로 보낼 코드를 `console.log`으로 바꿉니다(다이내믹 태그 관리, Adobe Analytics JS, Google Analytics 등).

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

지원되는 미디어 담벼락 이벤트 목록:

## 미디어 담벼락 이벤트

| 이벤트 | 정의 |
|---|---|
| `Init` | 페이지에 미디어 벽이 포함되는 경우 |
| `Load` | 위치에 관계없이 페이지에 미디어 월을 로드할 때 |
| `PostButtonClick` | 사용자가 미디어 담벼락의 업로드 단추를 클릭하면 |
| `RequestMore` | 사용자가 미디어 담벼락에 더 많은 컨텐츠를 로드할 때. |
| `TwitterReplyClick` | 사용자가 미디어 담벼락에서 Twitter 응답 단추를 클릭하면 |
| `TwitterRetweetClick` | 사용자가 미디어 담벼락에서 Twitter 리트윗 버튼을 클릭하면 |
| `TwitterLikeClick` | 사용자가 미디어 담벼락에서 Twitter 좋아요/즐겨찾기 단추를 클릭하면 |
| `ModalView` | 사용자가 클릭하면 더 큰 모달 창에서 미디어 담벼락 컨텐츠를 볼 수 있습니다. |
| `Like` | 사용자가 미디어 담벼락에서 좋아요 단추를 클릭하면 |
| `ShareButtonClick` | 사용자가 미디어 담벼락 카드에서 공유 버튼을 클릭할 때마다 언제든지 |
| `ShareURL` | [URL로 공유] 텍스트 영역이 선택된 경우 미디어 담벼락에서 복사됩니다. |
| `ShareFacebook` | 미디어 담벼락에서 Facebook으로 공유를 클릭하면 |
| `ShareTwitter` | 미디어 담벼락에서 Twitter에 공유를 클릭할 때 |
