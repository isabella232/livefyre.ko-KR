---
description: 고객은 제품 제공을 평가하고 검토할 수 있습니다.
seo-description: 고객은 제품 제공을 평가하고 검토할 수 있습니다.
seo-title: 평가
solution: Experience Manager
title: 평가
uuid: b 740 ee 28-f 6 f 9-4 ae 7-9 fe 7-61 a 5 cde 97 bbb
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 평가 {#reviews}

고객은 제품 제공을 평가하고 검토할 수 있습니다.

리뷰를 통해 커뮤니티 구성원은 제품 또는 서비스에 대한 스타 등급 및 질적 평가를 제공할 수 있습니다.

## 통합 {#section_kk5_15b_c1b}

검토 앱을 통합하려면 대화 앱 통합에 대한 절차를 따르십시오. 앱 [포함을 참조하십시오](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). 다음은 포함된 검토 앱의 예입니다.

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

작성 `CollectionMeta` 섹션에 명시된 대로 `CollectionMeta` 인코딩된 JSON 개체입니다. 위의 예에서 JSON 개체는 JWT 인코딩하기 전에 다음 형식을 사용합니다.

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Convconfig 오브젝트 {#section_pzv_ytb_c1b}

시작 섹션을 이미 완료한 경우 Convconfig 개체에 익숙해야 합니다. 검토를 활성화하려면 다음 필드로 Convconfig를 업데이트합니다.

* **Alwaysshoweditor** *선택적* 부울: 기본적으로 검토 편집기는 사용자가 "검토 작성" 단추를 누른 후에만 나타납니다. 항상 편집기를 표시하려면 이 매개 변수를 true로 설정합니다.

* **앱** *필수* 문자열: 검토할 앱 이름. " 검토 "여야 합니다.

* **Defaultsort** *선택적* 문자열: 기본 정렬 옵션을 선택하여 검토할 수 있습니다. 가능한 값은 다음과 같습니다. Mosthelpful, highestrated, lowestrated, LATEST 및 DEST.

* **Disabletitle** *optional* boolean: 기본적으로 필수 및 표시되는 검토 편집기에서 제목 필드를 비활성화하고 숨깁니다. 기본값은 true 입니다.

* **Enablehalfrating** *optional* Boolean: 기본 스타 선택 모듈에서 반 등급을 활성화하는 데 사용됩니다. 기본값은 true 입니다.

* **Hideshowreviewbutton** *optional* boolean: [!UICONTROL Show My Review] 단추가 표시될지 여부를 제어합니다. 사용자가 자신의 평가를 표시할지 여부를 선택할 수 있도록 하려면 true로 설정합니다.

* **Maxrating** *선택* 사항 기본 스타 선택 모듈에 표시되는 별의 수를 설정하는 데 사용되는 선택적 정수입니다. 기본값은 5 입니다. 최대 100 개까지 구성할 수 있습니다.

* **Ratingsummaryenabled** *선택적* 부울: 평가 앱 위에 등급 요약 보기를 표시하는 데 사용됩니다. Ratingsummarydelegate를 사용하려면 활성화해야 합니다. 기본값은 true 입니다.

## 컬렉션 메타데이터 검토 {#section_k1s_sqb_c1b}

* **유형:***필수* 문자열: 컬렉션 유형을 정의합니다. `reviews`되어야 합니다.

* **Ratingdimensions** *선택적* 배열: 이 컬렉션에 사용할 각 차원 유형에 대한 문자열 배열. 이 값을 지정하지 않으면 1 차원만 허용됩니다.

   예를 들어 사용자가'design ',' features'및'performance'에서 제품을 평가할 수 있도록 하려면 Array를 다음과 같이 설정합니다. `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **Ratingsubparts** *선택적* 정수: 검토 텍스트 상자에 표시할 파티션의 수입니다. 하위 파트 레이블은 아래와 같이 매개 변수와 함께 전달됩니다.

   >[!NOTE]
   >각 하위 부분에 대한 레이블을 정의해야 합니다.

* **Ratingsubpartsids** *Optional* Array: CSS 및 JavaScript에서 이러한 하위 요소 요소를 타깃팅하는 데 사용할 수 있는 등급 컬렉션의 각 하위 부분에 대한 ID를 정의할 수 있습니다. 사용자가 게시물을 게시하면 각 `ratingSubpart` 사용자가 이 ID로 채워진 " `data-lf-subpart-id`" 속성을 갖게 됩니다.

>[!NOTE]
>
>To use `ratingSubpartsIds`, the `ratingSubparts` param must also be defined, and the length of the two array must match.

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
>사용 `ratingDimensions`중인 경우 `ratingSelectionDelegate`, `ratingDisplayDelegate`및 `ratingSummaryDelegate` (등급 요약을 표시하려면) 를 사용해야 합니다.

## 사용자 정의 검토 {#section_khz_xmb_c1b}

### 별 이미지 구성

전체 별의 이미지를 변경하려면 이 클래스가 `goog-ratings-star`있습니다. 배경 이미지를 원하는 이미지로 변경할 수 있습니다. 기본적으로 별은 28 x 28 픽셀입니다.

### 별별 이미지로 별 이미지 구성

별의 경우 별의 양쪽에 두 개의 클래스가 있습니다. Half Star의 왼쪽은 오른쪽이고 `fyre-rating-half-odd` 오른쪽은 `fyre-rating-half-even`입니다. 기본적으로 절반의 별은 28 x 14 픽셀입니다.

### 별표에 대한 도구 설명 값 구성

별의 도구 설명 값을 구성하려면 문자열 사용자 정의에 설명된 사용자 지정 텍스트를 따릅니다. 설정한 후에는 키와 `ratingValues` 값을 사용하여 도구 설명 문자열이 포함된 배열을 사용합니다. 절반의 별이 비활성화되어 있는 경우 배열의 요소 수는 (위) 와 `maxRating` 같아야 합니다. 별표가 활성화되어 있으면 요소의 수는 2 x `maxRating`이어야 합니다. 배열의 첫 번째 요소는 맨 왼쪽 별 (또는 절반 별) 요소에 해당하고 왼쪽에서 오른쪽으로 계속됩니다.

### 내 검토 표시'옵션 전환

[!UICONTROL Show My Review] 옵션을 켜거나 끄려면 앱 구성에서 `hideShowReviewButton` 매개 변수를 타깃팅합니다.

### 기본적으로 텍스트 편집기 표시

검토 편집기는 [!UICONTROL write review] 사용자가 단추를 누른 후에만 나타납니다. 이 양식을 기본적으로 표시하려면 앱 구성에서 `alwaysShowEditor` 매개 변수를 타깃팅하십시오.
