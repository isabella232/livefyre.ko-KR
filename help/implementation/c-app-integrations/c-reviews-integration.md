---
description: 고객은 제품 오퍼링을 평가하고 검토할 수 있습니다.
seo-description: 고객은 제품 오퍼링을 평가하고 검토할 수 있습니다.
seo-title: 평가
solution: Experience Manager
title: 평가
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 0%

---


# 평가 {#reviews}

고객은 제품 오퍼링을 평가하고 검토할 수 있습니다.

검토를 통해 커뮤니티 구성원은 모든 제품 또는 서비스에 대한 스타 등급과 질적 평가를 제공할 수 있습니다.

## 통합 {#section_kk5_15b_c1b}

검토 앱을 통합하려면 대화 앱 통합 절차를 따르십시오. [앱](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md) 포함을 참조하십시오. 다음은 포함된 검토 앱의 예입니다.

### 예

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

`CollectionMeta` 빌드 섹션에 설명된 대로 `CollectionMeta`은(는) 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT로 인코딩되기 전에 다음 형식을 사용합니다.

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig 개체 {#section_pzv_ytb_c1b}

시작하기 섹션을 이미 완료한 경우 convConfig 객체에 대해 잘 알고 있어야 합니다. 검토를 활성화하려면 다음 필드로 convConfig를 업데이트합니다.

* **** ** alwaysShowEditoroptionalboolean:기본적으로 검토 편집기는 사용자가 &quot;검토 쓰기&quot; 단추를 누른 후에만 나타납니다. 편집기를 항상 표시하려면 이 매개 변수를 true로 설정합니다.

* **** ** improquedstring:검토에 사용할 앱 이름입니다. &quot;검토&quot;여야 합니다.

* **default** ** sortoptionalstring:검토에 대한 기본 정렬 옵션을 선택할 수 있습니다. 가능한 값은 다음과 같습니다.mostHelper, highestRated, lowerRated, 최신 항목 및 가장 오래된 항목.

* **disable** ** Titleotionalboolean:검토 편집기에서 제목 필드를 비활성화하거나 숨깁니다. 이 필드는 기본적으로 필수이며 표시됩니다. 기본값은 true입니다.

* **enableHalfRatingoptions** ** 부울:기본 별 선택 모듈에서 반등을 활성화하는 데 사용됩니다. 기본값은 true입니다.

* **** ** hideShowReviewButtonoptionsalboolean:단추를  [!UICONTROL Show My Review] 표시할지 여부를 제어합니다. 사용자가 자신의 검토를 표시할지 또는 표시할지를 선택할 수 있도록 하려면 true로 설정합니다.

* **** ** maxRatingoptionsalinteger 기본 별 선택 모듈에 표시되는 별 수를 설정하는 데 사용됩니다. 기본값은 5입니다. 최대 100개까지 구성할 수 있습니다.

* **** ** 등급 요약 활성화옵션 부울:평가 앱 위의 등급 요약 보기를 표시하는 데 사용됩니다. ratingSummaryDelegate를 사용하려면 이 기능을 활성화해야 합니다. 기본값은 true입니다.

## 컬렉션 메타데이터 검토 {#section_k1s_sqb_c1b}

* **type:** ** requiremdstring:컬렉션 유형을 정의합니다. `reviews`이어야 합니다.

* **등급** ** 분류 배열:이 컬렉션에서 사용할 각 차원 유형에 대한 문자열 배열입니다. 이 값을 지정하지 않으면 1개의 차원만 허용됩니다.

   예를 들어 사용자가 &#39;design&#39;, &#39;features&#39; 및 &#39;performance&#39;를 통해 제품을 평가할 수 있도록 하려면 배열을 다음과 같이 설정합니다.`ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** 등급 하위 파트너_정수:검토 텍스트 상자에 표시할 파티션 수입니다. 하위 부품 레이블은 아래 그림과 같이 매개 변수와 함께 전달됩니다.

   >[!NOTE]
   >각 하위 부품에 대한 레이블을 정의해야 합니다.

* **등급** ** 하위 부분표시 배열:등급 컬렉션의 각 하위 부분에 대한 ID를 정의할 수 있습니다. 이 ID는 CSS 및 JavaScript에서 이러한 하위 부분 요소를 대상으로 하는 데 사용할 수 있습니다. 사용자가 검토를 게시하면 각 `ratingSubpart`에 이 ID로 채워진 &quot;`data-lf-subpart-id`&quot; 속성이 포함됩니다.

>[!NOTE]
>
>`ratingSubpartsIds`을 사용하려면 `ratingSubparts` 매개 변수도 정의해야 하며 두 배열의 길이는 일치해야 합니다.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>`ratingDimensions`을 사용하는 경우 `ratingSelectionDelegate`, `ratingDisplayDelegate` 및 `ratingSummaryDelegate`(등급 요약을 표시하려면)을 사용해야 합니다.

## 사용자 정의 검토 {#section_khz_xmb_c1b}

### 별 이미지 구성

전체 별에 대한 이미지를 변경하려면 클래스는 `goog-ratings-star`입니다. 배경 이미지를 원하는 이미지로 변경합니다. 기본적으로 별은 28 x 28 픽셀입니다.

### 반점이 있는 별 이미지 구성

반별과 함께, 별들의 각 면에 대해 각각 하나의 2개의 수업이 있습니다. 반성의 왼쪽은 `fyre-rating-half-odd`이고 오른쪽은 `fyre-rating-half-even`입니다. 기본적으로 반점은 28 x 14픽셀입니다.

### 별 도구 설명 값 구성

별에 대한 도구 설명 값을 구성하려면 [문자열 사용자 지정]에 설명된 사용자 정의 텍스트를 따릅니다. 이 설정을 완료하면 `ratingValues` 키와 도구 설명 문자열이 포함된 배열의 값을 사용합니다. 반점이 비활성화된 경우 배열의 요소 수는 `maxRating`(위)과 같아야 합니다. 반점이 활성화된 경우 요소 수는 2x `maxRating`이어야 합니다. 배열의 첫 번째 요소는 맨 왼쪽 별(또는 반별) 요소에 해당하고 왼쪽에서 오른쪽으로 계속됩니다.

### &#39;내 검토 표시&#39; 옵션 켜기/끄기

[!UICONTROL Show My Review] 옵션을 켜거나 끄려면 앱 구성에서 `hideShowReviewButton` 매개 변수를 타깃팅하십시오.

### 기본적으로 텍스트 편집기 표시

검토 편집기는 사용자가 [!UICONTROL write review] 단추를 누른 후에만 나타납니다. 기본적으로 이 양식을 표시하려면 앱 구성에서 `alwaysShowEditor` 매개 변수를 타깃팅합니다.
