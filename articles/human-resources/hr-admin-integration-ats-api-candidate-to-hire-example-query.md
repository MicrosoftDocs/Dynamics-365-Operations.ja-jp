---
title: 採用する採用候補者に対するクエリの例
description: この記事では、Dynamics 365 Human Resources における採用候補者エンティティに対するクエリの例を示します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2dd744665d4f0b6c64f4ee45a01c237081018514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848345"
---
# <a name="example-query-for-candidate-to-hire"></a>採用する採用候補者に対するクエリの例


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources における採用候補者エンティティに対するクエリの例を示します。

この記事では、*ディープ インサート* を使用して、ひとつの API 操作で新しい候補レコードのすべての詳細を作成する方法について説明します。 ディープ インサートの詳細については、 [関連するエンティティ レコードを一度の操作で作成する](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation)を参照してください。

**mshr_hcmcandidatetohireentity** エンティティ は、**mshr_dirpersonentity** エンティティとの関係性から一意となります。 **mshr_hcmcandidatetohireentity** のプロパティの多く (**mshr_firstname**、**mshr_lastname**、**mshr_birthdate** など) は **mshr_dirpersonentity** レコードから派生しています。 ディープインサートを使用せずに **mshr_hcmcandidatetohireentity** に新しい候補レコードを投稿する場合、これらのプロパティの値を **mshr_hcmcandidatetohireentity** レコードに直接定義することができます。 関連付けられている **mshr_dirpersonentity** レコードは、プロパティに定義された値で暗黙的に作成されます。 その後、個別の API 呼び出しとして、その他すべての関連エンティティ レコード (スキルや学歴など) を作成できます。

しかし、ディープインサートを使用して一度の操作ですべての関連エンティティを作成する場合は、**mshr_dirpersonentity** エンティティに固有のプロパティを操作のネストしたレベルで定義する必要があります。

この例では、一度のの API 操作でディープインサートを使用して、候補者レコード、関連する人物レコード、人物のスキルと学歴を 3 つのネストされたレベルで作成する方法を示しています。

> [!NOTE]
> この例では、各 API エンティティのすべてのプロパティが含まれているわけではありません。 デモ用に簡略化しています。

**申請**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**応答**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
