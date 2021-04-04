---
title: 採用する採用候補者に対するクエリの例
description: このトピックでは、Dynamics 365 Human Resources における採用候補者エンティティに対するクエリの例を示します。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2fc08586914fd3815b0da062f24d83ac550302f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467628"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="f9ddc-103">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="f9ddc-103">Example query for Candidate to hire</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f9ddc-104">このトピックでは、Dynamics 365 Human Resources における採用候補者エンティティに対するクエリの例を示します。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f9ddc-105">このトピックでは、*ディープ インサート* を使用して、ひとつの API 操作で新しい候補レコードのすべての詳細を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="f9ddc-106">ディープ インサートの詳細については、 [関連するエンティティ レコードを一度の操作で作成する](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-106">For more information about deep inserts, see [Create related entity records in one operation](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="f9ddc-107">**mshr_hcmcandidatetohireentity** エンティティ は、**mshr_dirpersonentity** エンティティとの関係性から一意となります。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="f9ddc-108">**mshr_hcmcandidatetohireentity** のプロパティの多く (**mshr_firstname**、**mshr_lastname**、**mshr_birthdate** など) は **mshr_dirpersonentity** レコードから派生しています。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="f9ddc-109">ディープインサートを使用せずに **mshr_hcmcandidatetohireentity** に新しい候補レコードを投稿する場合、これらのプロパティの値を **mshr_hcmcandidatetohireentity** レコードに直接定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="f9ddc-110">関連付けられている **mshr_dirpersonentity** レコードは、プロパティに定義された値で暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="f9ddc-111">その後、個別の API 呼び出しとして、その他すべての関連エンティティ レコード (スキルや学歴など) を作成できます。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="f9ddc-112">しかし、ディープインサートを使用して一度の操作ですべての関連エンティティを作成する場合は、**mshr_dirpersonentity** エンティティに固有のプロパティを操作のネストしたレベルで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="f9ddc-113">この例では、一度のの API 操作でディープインサートを使用して、候補者レコード、関連する人物レコード、人物のスキルと学歴を 3 つのネストされたレベルで作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="f9ddc-114">この例では、各 API エンティティのすべてのプロパティが含まれているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="f9ddc-115">デモ用に簡略化しています。</span><span class="sxs-lookup"><span data-stu-id="f9ddc-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="f9ddc-116">**申請**</span><span class="sxs-lookup"><span data-stu-id="f9ddc-116">**Request**</span></span>

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

<span data-ttu-id="f9ddc-117">**応答**</span><span class="sxs-lookup"><span data-stu-id="f9ddc-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="f9ddc-118">参照</span><span class="sxs-lookup"><span data-stu-id="f9ddc-118">See also</span></span>

[<span data-ttu-id="f9ddc-119">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="f9ddc-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]