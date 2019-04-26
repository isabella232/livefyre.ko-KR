---
description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-title: 대화 앱에 대한 Javascript 이벤트
solution: Experience Manager
title: 대화 앱에 대한 Javascript 이벤트
uuid: CCE 112 B 5-7 C 3 A -4721-9854-FC 8471 F 3 D 5 D 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 대화 앱에 대한 Javascript 이벤트{#javascript-events-for-conversation-apps}

대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.

## 대화 앱 및 이벤트 매트릭스 {#section_y4j_x4m_ybb}

다음은 대화 앱에서 사용할 수 있는 이벤트의 행렬입니다. X는 이벤트가 앱에 대해 사용 가능하다는 것을 나타내고, N/A는 해당 이벤트가 앱에는 적용되지 않음을 나타내고, 표시는 해당 앱에 대해 이벤트를 사용할 수 없음을 의미합니다.

### 대화 앱 이벤트

| 이벤트 | 댓글 | 채팅 | Liveblog | 평가 | Sidenotes | 투표 | 트렌딩 |
|---|---|---|---|---|---|---|---|
| init | x | x | x | x | x |  |  |
| load | x | x | x | x |  |  |  |
| view | x | x | x | x |  |  |  |
| POST | x | x | x | x |  | N/A | N/A |
| 게시됨 | x | x | x | x | x | N/A | N/A |
| Twitter 답글 | x | x | x | N/A | N/A | N/A | N/A |
| Twitter 좋아요 | x | x | x | N/A | N/A | N/A | N/A |
| LF like | x | x | x | x | N/A | N/A | N/A |
| LF와 달리 | x | x | x | x | N/A | N/A | N/A |
| 게시물 공유 | x | x |  | x | N/A | N/A | N/A |
| 공유 단추 | x | x | x | x |  | N/A | N/A |
| Twitter 공유 | x | x | x | x | x | N/A | N/A |
| Facebook 공유 | x | x | x | x | x | N/A | N/A |
| 공유 URL | x | x | x | x |  | N/A | N/A |
| Expandreplies | x | N/A | x | x | N/A | N/A | N/A |
| 답글 축소 | x | N/A | x | x | N/A | N/A | N/A |
| 플래그 단추 | x | x | x | x | N/A | N/A | N/A |
| flag | x | x | x | x | x | N/A | N/A |
| 플래그 취소 | x | x | x | x | N/A | N/A | N/A |
| 팔로우 | x | N/A | x | x | N/A | N/A | N/A |
| Unfollow | x | N/A | x | x | N/A | N/A | N/A |
| 요청자세한 내용 | x | x | x | x | N/A | N/A | N/A |
| Modalview |  | N/A | N/A | N/A | N/A | N/A | N/A |
| Twitter 리트윗 | x | x | x | N/A | N/A | N/A | N/A |
| 게시물 단추 클릭 | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| 댓글 수 업데이트 | x | x | x | x | N/A | N/A | N/A |
| 사용자 로그인 |  |  |  |  |  | N/A | N/A |
| 사용자가 로그아웃함 |  |  |  |  |  | N/A | N/A |
| 주석 기능 특집 |  | N/A |  |  | N/A | N/A | N/A |
| 주석 없는 주석 |  | N/A |  |  | N/A | N/A | N/A |
| 투표 투표 | N/A | N/A | N/A | x | x | N/A | N/A |
| 투표 선택 | N/A | N/A | N/A | N/A | N/A |  | N/A |
| 트렌드 항목 선택 | n/. a | N/A | N/A | N/A | N/A | N/A |  |
| 네트워크 ID |  |  |  |  |  |  |  |
| 앱 ID | x | x | x | x |  |  |  |
| 컨텍스트 ID | x | x | x | x |  |  |  |
| 앱 유형 | x | x | x | x |  |  |  |
| 컨텐츠 유형 | x | x | x | x |  |  |  |
| 앱에 게시된 날짜 |  |  |  |  |  |  |  |
| 최종 사용자 앱에 로그인됨 |  |  |  |  |  |  |  |

