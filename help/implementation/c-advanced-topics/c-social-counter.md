---
description: 선별된 소셜 항목의 수를 카운트합니다.
seo-description: 선별된 소셜 항목의 수를 카운트합니다.
seo-title: 소셜 카운터
solution: Experience Manager
title: 소셜 카운터
uuid: fa 9 aa 1 a 8-6 a 04-4 bc 1-9 bfe-e 42 c 1250 fd 48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 소셜 카운터{#social-counter}

선별된 소셜 항목의 수를 카운트합니다. 사용 가능한 끝점에 대한 전체 목록은 Livefyre [API 참조](https://api.livefyre.com/docs) 섹션을 참조하십시오.

Social 카운터 API는 일정 기간 동안 주어진 컬렉션에서 일치하는 조정 규칙에 대한 카운트를 반환합니다.

>[!NOTE]
>
>이 API는 Twitter 해시 태그에만 사용할 수 있습니다.

소셜 카운터 API:

* 리소스
* 규칙 유형
* response

## 리소스 {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **Networkname:** Livefyre가 네트워크 이름을 제공했습니다. 예를 들면 다음과 같습니다. *Labs* `labs.fyre.co`의
* **쿼리:** URL-safe base 64의 모든 사이트 해시 해시, 집필 ID, 개수 정보를 가져와야 하는 규칙 유형 (사전 인코딩됨)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >Query is limited to 10 site, article ID, rule-type tuples. 이전 예에는 3 개의 자습서가 포함되어 있습니다.

* **From**`(optional)` 는 그래프에 상대적 또는 절대 기간을 지정합니다. [시작] 는 [시작] 를 지정하고, [생략] 는 24 시간 전에 지정합니다.
* **그래프에 상대적 또는 절대 기간을** `(optional)` 지정할 때까지, [시작] 를 지정하고 [현재 시간] (현재) 이 생략된 경우 기본값을 지정합니다.

### 상대적 시간

| 약어 | unit |
|---|---|
| s | 초 |
| min | minutes |
| h | hours |
| d | 일 수 |
| w | 주 |
| mon | 30 일 (월) |
| y | 365 일 (연도) |

예:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## 절대 시간 {#section_xqr_jgc_11b}

형식: hh: mm_ yyyymmdd

| 약어 | 의미 |
|---|---|
| HH | 시간 (24 시간 형식) |
| MM | minutes |
| YYYY | 4 자리 연도 |
| MM | 월 |
| DD | day |

예:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## 규칙 유형 {#section_v53_xqb_11b}

| value | type |
|---|---|
| 2 | Twitter |

예:

For obtain counts over the last minute for site `123456` and article ID `some-article-id` and rule-type `2`, for example: `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

답변 예:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
