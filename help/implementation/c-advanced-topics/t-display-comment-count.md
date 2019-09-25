---
description: 색인 페이지에 표시할 특정 컬렉션의 게시물 및 댓글 수를 선택합니다.
seo-description: 색인 페이지에 표시할 특정 컬렉션의 게시물 및 댓글 수를 선택합니다.
seo-title: 댓글 수 표시
solution: Experience Manager
title: 댓글 수 표시
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# 댓글 수 표시{#display-comment-count}

색인 페이지에 표시할 특정 컬렉션의 게시물 및 댓글 수를 선택합니다.

Livefyre를 `CommentCount.js` 사용하면 사이트에서 컬렉션의 콘텐츠 수를 가져올 수 있습니다. 앱은 현재 컬렉션에 대한 댓글 수를 표시하지만 사이트 전체에 이러한 카운트를 적용하는 것이 유용할 수 있습니다. 이 기능은 특히 데이터베이스의 컨텐츠를 유지하지 않거나 CMS 데이터베이스가 Livefyre와 동기화되지 않은 경우에 유용합니다.

1. JavaScript를 로드합니다.

   사용하려면 `CommentCount.js`먼저 JavaScript 파일을 사용하려는 페이지 또는 템플릿의 `<head>` 섹션에 포함합니다.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. HTML 요소를 바인딩합니다.

   스크립트가 로드되면 이 스크립트는 클래스 이름이 인 페이지에서 다른 요소를 찾으려고 시도합니다. `livefyre-commentcount` 이러한 각 요소에 대해 스크립트는 `data-lf-site-id` `data-lf-article-id` 및 HTML 속성을 찾고 이를 사용하여 Livefyre에서 컨텐츠를 가져오고 각 요소를 최신 값으로 업데이트합니다.

   예를 들어 다음 요소가 업데이트됩니다.

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {importance="high"}
   >
   >이 `CommentCount.js` 코드는 실제 수로 업데이트할 숫자 값을 확인합니다. 태그 사이에 숫자 값을 포함해야 합니다.

   **예 1** (URL을 아티클 ID로 사용):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **예 2** (번호가 매겨진 시스템을 아티클 ID로 사용):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 옵션 구성을 참조하십시오.

   콘텐트 카운트의 대체 방법을 더 잘 제어하려면 구성 옵션이 포함된 개체를 호출하고 `LF.CommentCount()` 전달합니다. 교체가 필요한 모든 요소가 DOM에 있으면 함수를 호출해야 합니다. 이 메서드를 호출하는 데 가장 적합한 위치는 바닥글이므로 DOM이 로드될 때, 문서 및 창 준비 이벤트 전에 발생합니다.

   다음 구성 옵션을 허용합니다.

* **** 교체:각 컨텐츠 카운트의 텍스트를 바꾸는 데 사용되는 함수 또는 Regex입니다.

* **** function:각 요소에서 대체 작업을 수행하는 데 사용됩니다. 함수의 인수는 다음과 같습니다.

   **element:** The HTML element that is being updated.
   **** count:이 요소의 콘텐츠 카운트입니다.

* **** regex: Used to determine which part of the element’s text should be replaced by the count.

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
   >Use the replacer to customize or internationalize the comment count message.
