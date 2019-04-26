---
description: Javascript 이벤트를 사용하여 미디어 담벼락에서 발생하는 이벤트를 수신하고 원하는 분석 도구로 전송합니다.
seo-description: Javascript 이벤트를 사용하여 미디어 담벼락에서 발생하는 이벤트를 수신하고 원하는 분석 도구로 전송합니다.
seo-title: 미디어 담벼락에 대한 Javascript 이벤트
solution: Experience Manager
title: 미디어 담벼락에 대한 Javascript 이벤트
uuid: 8 AFC 0529-4640-476 A-B 207-91 B 2 C 70101 F 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 미디어 담벼락에 대한 Javascript 이벤트{#javascript-events-for-media-wall}

Javascript 이벤트를 사용하여 미디어 담벼락에서 발생하는 이벤트를 수신하고 원하는 분석 도구로 전송합니다.

Livefyre는 Livefyre 앱의 사용자 활동을 추적하는 JavaScript 이벤트를 제공합니다. 예를 들어 사용자가 Twitter 또는 Facebook와 같은 또는 새 컨텐츠가 게시될 때 페이지를 업데이트하려는 경우 페이지를 업데이트할 수 있습니다.

다음은 이벤트를 받는 방법의 예입니다. 코드를 매핑하여 `console.log` 이벤트를 매핑하고 Analytics 통합 (다이내믹 태그 관리, Adobe Analytics JS, Google Analytics 등) 에 보냅니다.

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

지원되는 미디어 담벼락 이벤트 목록:

## Media Wall Events

| 이벤트 | 정의 |
|---|---|
| `Init` | 미디어 담벼락이 페이지에 포함되는 경우. |
| `Load` | 미디어 담벼락이 위치에 관계없이 페이지에 로드된 경우 |
| `PostButtonClick` | 사용자가 미디어 담벼락의 업로드 단추를 클릭할 때. |
| `RequestMore` | 사용자가 미디어 담벼락에 더 많은 컨텐츠를 로드할 때 |
| `TwitterReplyClick` | 사용자가 미디어 담벼락에서 Twitter 답글 단추를 클릭할 때. |
| `TwitterRetweetClick` | 사용자가 미디어 담벼락에서 Twitter 리트윗 단추를 클릭할 때. |
| `TwitterLikeClick` | 사용자가 미디어 담벼락에서 Twitter 좋아요/즐겨찾기 단추를 클릭할 때. |
| `ModalView` | 사용자가 클릭하여 큰 모달 창에서 미디어 담벼락 컨텐츠를 볼 때 |
| `Like` | 사용자가 미디어 담벼락에서 좋아요 단추를 클릭할 때. |
| `ShareButtonClick` | 사용자가 미디어 담벼락의 공유 단추를 클릭할 때마다 |
| `ShareURL` | 미디어 담벼락에서 URL 텍스트 영역에 공유/복사되는 경우 |
| `ShareFacebook` | 미디어 담벼락에서 Facebook에 공유를 클릭하면 |
| `ShareTwitter` | 미디어 담벼락에서 Twitter에 공유하는 경우 |
