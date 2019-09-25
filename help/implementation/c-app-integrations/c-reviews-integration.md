---
description: 고객은 제품 오퍼링을 평가하고 검토할 수 있습니다.
seo-description: 고객은 제품 오퍼링을 평가하고 검토할 수 있습니다.
seo-title: 평가
solution: Experience Manager
title: 평가
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# 평가 {#reviews}

고객은 제품 오퍼링을 평가하고 검토할 수 있습니다.

검토를 통해 커뮤니티 구성원은 모든 제품 또는 서비스에 대한 스타 등급과 질적 평가를 제공할 수 있습니다.

## 통합 {#section_kk5_15b_c1b}

검토 앱을 통합하려면 대화 앱 통합 절차를 따르십시오. 앱 [포함을 참조하십시오](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). 다음은 포함된 검토 앱의 예입니다.

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

빌드 `CollectionMeta` 섹션에 명시된 대로 `CollectionMeta` 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT로 인코딩되기 전에 다음 형식을 사용합니다.

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

시작하기 섹션을 이미 완료한 경우 convConfig 개체에 익숙해야 합니다. 검토를 활성화하려면 다음 필드로 convConfig를 업데이트합니다.

* **alwaysShowEditor** 옵션 *부울* :기본적으로 검토 편집기는 사용자가 "쓰기 검토" 단추를 누른 후에만 나타납니다. 편집기를 항상 표시하려면 이 매개 변수를 true로 설정합니다.

* **app** required ** 문자열:검토에 사용할 앱 이름. "평가"여야 합니다.

* **defaultSort** 선택 *문자열* :검토에 대한 기본 정렬 옵션을 선택할 수 있습니다. 가능한 값은 다음과 같습니다.mostHelpful, highestRated, lowerRated, 최신 및 가장 오래된

* **disableTitle** 선택 *사항* 부울:검토 편집기에서 제목 필드를 비활성화하고 숨깁니다. 이 필드는 기본적으로 필요하며 표시됩니다. 기본값은 true입니다.

* **enableHalfRating** 옵션 *부울* :기본 별 선택 모듈에서 절반 등급을 활성화하는 데 사용됩니다. 기본값은 true입니다.

* **hideShowReviewButton** 선택 *사항* 부울단추를 표시할지 여부를 [!UICONTROL Show My Review] 제어합니다. 사용자가 자신의 평가를 표시할지 또는 표시할지 선택할 수 있도록 하려면 true로 설정합니다.

* **maxRating** *선택적* 정수 기본 별 선택 모듈에 표시되는 별 수를 설정하는 데 사용됩니다. 기본값은 5입니다. 최대 100개까지 구성할 수 있습니다.

* **ratingSummaryEnabled** 옵션 *부울* :평가 앱 위의 등급 요약 보기를 표시하는 데 사용됩니다. ratingSummaryDelegate를 사용하려면 이 옵션을 활성화해야 합니다. 기본값은 true입니다.

## 컬렉션 메타데이터 검토 {#section_k1s_sqb_c1b}

* **** type: *필수* 문자열:컬렉션 유형을 정의합니다. 틀림없이 `reviews`그렇습니다.

* **ratingDimensions** 선택 *배열* :이 컬렉션에서 사용할 각 차원 유형에 대한 문자열 배열입니다. 이 값을 지정하지 않으면 1개의 차원만 허용됩니다.

   예를 들어 사용자가 'design', 'features' 및 'performance'에 대해 제품을 평가할 수 있도록 하려면 배열을 다음과 같이 설정합니다. `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **ratingSubparts** 선택 *사항* 정수:검토 텍스트 상자에 표시할 파티션 수입니다. 하위 부품 레이블은 아래 그림과 같이 매개 변수와 함께 전달됩니다.

   >[!NOTE]
   >각 하위 부품에 대한 레이블을 정의해야 합니다.

* **ratingSubpartsIds** 선택 *배열* :등급 컬렉션의 각 하위 부분에 대한 ID를 정의할 수 있습니다. 이 ID는 CSS 및 JavaScript에서 이러한 하위 파트 요소를 타깃팅하는 데 사용할 수 있습니다. 사용자가 검토를 게시하면 각 `ratingSubpart` 사용자에게 " `data-lf-subpart-id`" 속성이 이 ID로 채워집니다.

>[!NOTE]
>
>사용하려면 `ratingSubpartsIds`매개 변수도 `ratingSubparts` 정의해야 하며 두 배열의 길이가 일치해야 합니다.

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
>사용 중인 `ratingDimensions`경우, `ratingSelectionDelegate`, `ratingDisplayDelegate`및 `ratingSummaryDelegate` (등급 요약을 표시하려면) 을 사용해야 합니다.

## 사용자 정의 검토 {#section_khz_xmb_c1b}

### 별 이미지 구성

별 모양을 변경하려면 클래스가 `goog-ratings-star`필요합니다. 배경 이미지를 원하는 이미지로 변경합니다. 기본적으로 별은 28 x 28 픽셀입니다.

### 별 모양 구성

반별이 있으면 별들의 각 면에 각각 하나씩, 두 개의 수업이 있다. 반성의 왼쪽은 `fyre-rating-half-odd` 오른쪽이고 오른쪽은 `fyre-rating-half-even`오른쪽이다. 기본적으로 반점은 28 x 14 픽셀입니다.

### 별에 대한 도구 설명 값 구성

별에 대한 도구 설명 값을 구성하려면 문자열 사용자 정의에 설명된 사용자 지정 텍스트를 따릅니다. 설정을 완료하면 키와 도구 설명 문자열이 포함된 `ratingValues` 배열의 값을 사용합니다. 반점이 비활성화된 경우 배열의 요소 수는 `maxRating` (위)와 같아야 합니다. 반점이 활성화된 경우 요소 수는 2x이어야 합니다 `maxRating`. 배열의 첫 번째 요소는 맨 왼쪽 별(또는 절반 별) 요소에 해당하며 왼쪽에서 오른쪽으로 계속됩니다.

### '내 검토 표시' 옵션 전환

이 [!UICONTROL Show My Review] 옵션을 켜거나 끄려면 앱 구성에서 `hideShowReviewButton` 매개 변수를 타게팅합니다.

### 기본적으로 텍스트 편집기 표시

검토 편집기는 사용자가 [!UICONTROL write review] 단추를 누른 후에만 나타납니다. 이 양식을 기본적으로 표시하려면 앱 구성에서 `alwaysShowEditor` 매개 변수를 타게팅하십시오.
