---
description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-description: 대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.
seo-title: 대화 앱에 대한 Javascript 이벤트
solution: Experience Manager
title: 대화 앱에 대한 Javascript 이벤트
uuid: cce112b5-7c3a-4721-9854-fc8471f3d5d0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 대화 앱에 대한 Javascript 이벤트{#javascript-events-for-conversation-apps}

대화 앱(예를 들어 댓글, 채팅, 라이브 블로그, 검토 및 방주)에 JavaScript를 바인딩할 수 있는 이벤트.

## 대화 앱 및 이벤트 매트릭스 {#section_y4j_x4m_ybb}

다음은 대화 앱에 사용할 수 있는 이벤트 매트릭스입니다. X는 이벤트가 앱에 대해 사용 가능하다는 것을 의미하고, N/A는 이벤트가 앱에 적용되지 않음을 의미하며, 표시가 없으면 해당 앱에서 이벤트를 사용할 수 없음을 의미합니다.

### 대화 앱 이벤트

| 이벤트 | 설명 | 대화 | Liveblog | 평가 | 사이드노트 | 투표 | 트렌딩 |
|---|---|---|---|---|---|---|---|
| 초기화 | X | X | X | X | X |  |  |
| 로드 | X | X | X | X |  |  |  |
| 보기 | X | X | X | X |  |  |  |
| 게시물 | X | X | X | X |  | N/A | N/A |
| 게시됨 | X | X | X | X | X | N/A | N/A |
| Twitter 답글 | X | X | X | N/A | N/A | N/A | N/A |
| Twitter 좋아요 | X | X | X | N/A | N/A | N/A | N/A |
| 좋아요 LF | X | X | X | X | N/A | N/A | N/A |
| LF Unlike | X | X | X | X | N/A | N/A | N/A |
| 게시물 공유 | X | X |  | X | N/A | N/A | N/A |
| 공유 단추 | X | X | X | X |  | N/A | N/A |
| Twitter 공유 | X | X | X | X | X | N/A | N/A |
| Facebook 공유 | X | X | X | X | X | N/A | N/A |
| URL 공유 | X | X | X | X |  | N/A | N/A |
| 답글 확장 | X | 해당 없음 | X | X | N/A | N/A | N/A |
| 답글 축소 | X | 해당 없음 | X | X | N/A | N/A | N/A |
| 플래그 단추 | X | X | X | X | N/A | N/A | N/A |
| 플래그 | X | X | X | X | X | N/A | N/A |
| 플래그 취소 | X | X | X | X | N/A | N/A | N/A |
| 팔로우 | X | 해당 없음 | X | X | N/A | N/A | N/A |
| 팔로우 취소 | X | 해당 없음 | X | X | N/A | N/A | N/A |
| 요청더 보기 | X | X | X | X | N/A | N/A | N/A |
| ModalView |  | N/A | N/A | N/A | N/A | N/A | N/A |
| Twitter 리트윗 | X | X | X | N/A | N/A | N/A | N/A |
| 게시물 단추 클릭 | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| 댓글 수 업데이트됨 | X | X | X | X | N/A | N/A | N/A |
| 사용자 로그인 |  |  |  |  |  | N/A | N/A |
| 사용자 로그아웃 |  |  |  |  |  | N/A | N/A |
| 주요 의견 |  | N/A |  |  | N/A | N/A | N/A |
| 특집 없는 주석 |  | N/A |  |  | N/A | N/A | N/A |
| 댓글 투표 | N/A | N/A | N/A | X | X | N/A | N/A |
| 투표 선택 | N/A | N/A | N/A | N/A | N/A |  | N/A |
| 트렌드 항목 선택 | N/.A | N/A | N/A | N/A | N/A | N/A |  |
| 네트워크 ID |  |  |  |  |  |  |  |
| 앱 ID | X | X | X | X |  |  |  |
| 컨텍스트 ID | X | X | X | X |  |  |  |
| 앱 유형 | X | X | X | X |  |  |  |
| 컨텐츠 유형 | X | X | X | X |  |  |  |
| 앱에 게시된 날짜 |  |  |  |  |  |  |  |
| 최종 사용자 앱에 로그인 |  |  |  |  |  |  |  |

