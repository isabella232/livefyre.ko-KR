---
description: 색인 페이지에 표시할 특정 컬렉션에 대한 게시물 및 댓글 카운트를 확인합니다.
seo-description: 색인 페이지에 표시할 특정 컬렉션에 대한 게시물 및 댓글 카운트를 확인합니다.
seo-title: 주석 수 표시
solution: Experience Manager
title: 주석 수 표시
uuid: 0 F 39 B 25 E -11 E 0-4945-BE 71-55 FB 4798 B 6 C 7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# 주석 수 표시{#display-comment-count}

색인 페이지에 표시할 특정 컬렉션에 대한 게시물 및 댓글 카운트를 확인합니다.

Livefyre `CommentCount.js` 를 사용하면 사이트에서 컬렉션의 콘텐츠 카운트를 가져올 수 있습니다. 앱은 현재 컬렉션에 대한 댓글 카운트를 표시하지만 사이트에서 이러한 카운트를 제공하는 것이 유용할 수 있습니다. 이 기능은 특히 데이터베이스의 컨텐츠를 지속하지 않거나 CMS 데이터베이스가 Livefyre와 동기화되지 않은 경우에 유용합니다.

1. JavaScript를 로드합니다.

   사용하려면 `CommentCount.js`먼저 JavaScript 파일을 사용하려는 페이지 또는 템플릿의 `<head>` 섹션에 포함시켜야 합니다.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. HTML 요소를 바인딩합니다.

   스크립트가 로드되면 페이지에서 클래스 이름이 `livefyre-commentcount`있는 다른 요소를 찾으려고 시도합니다. 이러한 각 요소에 대해 스크립트는 `data-lf-site-id` 검색과 `data-lf-article-id` HTML 속성을 찾고 이를 사용하여 Livefyre의 컨텐츠를 가져오고 최신 값으로 각 요소를 업데이트합니다.

   예를 들어 다음 요소가 업데이트됩니다.

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {importance = "high"}
   >
   >코드는 `CommentCount.js` 실제 카운트로 업데이트할 숫자 값을 확인합니다. 태그 사이에 숫자 값을 포함해야 합니다.

   **예제 1** (URL를 아티클 ID로 사용):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **예제 2** (번호가 매겨진 시스템을 아티클 ID로 사용):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 옵션 구성을 참조하십시오.

   컨텐츠 카운트가 바뀌는 방식을 보다 정확하게 제어하려면 구성 `LF.CommentCount()` 옵션이 들어 있는 개체를 호출하고 전달합니다. 대체해야 하는 요소가 DOM에 모두 포함되면 함수를 호출해야 합니다. 이 메서드를 호출할 가장 좋은 위치는 바닥글에 있으므로 DOM 이 로드될 때, Document 및 Window Ready 이벤트보다 앞서 발생합니다.

   다음 구성 옵션을 사용할 수 있습니다.

* **대체자:** 각 컨텐츠 수의 텍스트를 대체하는 데 사용되는 함수나 regex 입니다.

* **함수:** 각 요소를 대체하는 데 사용됩니다. 함수의 인수는 다음과 같습니다.

   **요소:** 업데이트할 HTML 요소입니다.
   **카운트:** 이 요소에 대한 컨텐츠 수입니다.

* **regex:** 요소의 텍스트 중 어떤 부분을 카운트로 대체할지를 결정하는 데 사용됩니다.

   **예**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >교체 도구를 사용하여 주석 수 메시지를 사용자 정의하거나 국제화할 수 있습니다.
