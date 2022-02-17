---
title: 人物の職務経験
description: このトピックでは、Dynamics 365 Human Resources の人物の職務経験エンティティについて説明します。
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
ms.openlocfilehash: 38535b5dd56b3408ea582fbaf1594b7adefcd171
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068687"
---
# <a name="person-professional-experience"></a>人物の職務経験


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物の職務経験エンティティについて説明します。

物理名 : mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>説明

このエンティティは、候補者の職務経験または業務経歴を記述します。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **人物の職務経験エンティティ ID**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | 読み取り専用<br>必須 | システムが生成した、エンティティ レコードの一意識別子です。 |
| **当事者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 | 候補者の個人レコードの一意識別子です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity の mshr_dirpersonentityid | システムが生成した、人物のエンティティ レコードの一意識別子です。 |
| **雇用主の職位**<br>mshr_employerposition<br>*文字列* | 読み取り/書き込み<br>必須 | 候補者が在職中に経験した職位です。 |
| **従業員名称**<br>mshr_employername<br>*文字列* | 読み取り/書き込み<br>必須 | 従業員の名前です。 |
| **雇用主の場所**<br>mshr_employerlocation<br>*文字列* | 読み取り/書き込み<br>オプション | 雇用主の場所です。 最大の長さ : 60 。 特定の形式や定義は不要です。 |
| **電話**<br>mshr_phone<br>*文字列* | 読み取り/書き込み<br>オプション | 雇用主の電話番号です。 |
| **URL**<br>mshr_url<br>*文字列* | 読み取り/書き込み<br>オプション | 雇用主の Web サイトの URL です。 |
| **開始日**<br>mshr_startdate<br>*Datetime* | 読み取り/書き込み<br>必須 | 候補者の雇用開始日です。 |
| **終了日**<br>mshr_enddate<br>*Datetime* | 読み取り/書き込み<br>オプション | 候補者の雇用終了日です。候補者の雇用が継続している場合は、null 値となります。 |
| **雇用主への連絡を許可する**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno オプション セット* | 読み取り/書き込み<br>オプション | 候補者が前の雇用主への連絡を許可するかどうかを示します。 |
| **摘要**<br>mshr_note<br>*文字列* | 読み取り/書き込み<br>オプション | 採用担当者や採用マネージャーが使用するメモです。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | エンティティ レコードの基本識別子として使用されるフィールドです。 関係者番号、開始日、雇用主の職位、雇用主名の組み合わせです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
