---
title: 採用で要求するスキル
description: このトピックでは、Dynamics 365 Human Resources の人物の採用スキルエンティティについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e464ced904eb4358ba5d4e1c6c2c36089bfa0d8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801314"
---
# <a name="recruiting-request-skill"></a>採用で要求するスキル

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物の採用スキルエンティティについて説明します。

物理名 : mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>説明

RecruitingRequest のスキル要件について説明します。

### <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **採用で要求するスキルのエンティティ ID**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | 読み取り専用<br>必須 | システムが生成した、**採用で要求するスキル** レコードの一意識別子です。 |
| **採用要求 ID**<br>mshr_recruitingrequestid<br>*文字列* | 1回書き込み<br>必須 | 読み取り可能な、関連する採用要求の一意識別子です。 |
| **採用要求 ID 値**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | 読み取り専用<br>必須<br> 外部キー : mshr_hcmrecruitingrequestentity エンティの mshr_hcmrecruitingrequestentityid | システムが生成する、関連する採用要求の一意識別子です。 |
| **スキル ID**<br>mshr_skillid<br>*文字列*<br> | 1回書き込み<br>必須 | 読み取り可能な、要求されるスキルの一意識別子です。 |
| **スキル ID の値**<br>_mshr_fk_skill_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmskillentity エンティティの mshr_hcmskillentityid | システムが生成した、要求されるスキルの一意識別子です。 |
| **評価レベル ID**<br>mshr_ratinglevelid<br>*文字列* | 1回書き込み<br>オプション | スキルに割り当てられている評価モデルに基づいて、職務に選択された必要なスキル レベルの値です。 |
| **評価レベル ID 値**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmratinglevelentity エンティティの mshr_hcmratinglevelentityid | システムが生成した、レベルの一意識別子です。 |
| **スキルの説明**<br>mshr_skilldescription<br>*文字列* | 読み取り専用<br>必須 | スキルの説明です。 |
| **評価レベルの説明**<br>mshr_ratingleveldescription<br>*文字列* | 読み取り専用<br>オプション | 選択したスキルレベルの説明です。 |
| **データ領域 ID**<br>mshr_dataareaid<br>*文字列* | 読み取り/書き込み<br>オプション | 法人 (会社) を指定します。 |
| **データ領域 ID 値**<br>_mshr_dataareaid_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : cdm_companyid of cdm_company エンティティ | システムが生成する、法人 (会社) を識別する GUID 値です。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | レコードを一意に識別する別の方法としての採用要求値、スキル ID の連結です。 |
| **評価モデル ID**<br>mshr_ratingmodelid<br>*文字列* | 読み取り/書き込み<br>必須 | スキルの評価に使用される評価モデルです。 |
| **評価モデル ID の値**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmratingmodelentity エンティティ の mshr_hcmratingmodelentityid | システムが生成する、スキルの評価に使用される評価モデルの一意識別子です。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]