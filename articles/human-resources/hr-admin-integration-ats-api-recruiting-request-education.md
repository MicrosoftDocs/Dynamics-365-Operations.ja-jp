---
title: 採用で要求する教育
description: この記事では、Dynamics 365 Human Resources の採用要求教育エンティティについて説明します。
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
ms.openlocfilehash: bcdb5e2cc61ce551af21401ea34d8e85bc21fc6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893848"
---
# <a name="recruiting-request-education"></a>採用で要求する教育


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の採用要求教育エンティティについて説明します。

物理名 : mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>説明

RecruitingRequest の教育要件について説明します。

### <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **採用で要求する教育エンティティ ID**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | 読み取り専用<br>必須 | システムが生成した、採用で要求する教育レコードの一意識別子です。 |
| **採用要求 ID**<br>mshr_recruitingrequestid<br>*文字列* | 1回書き込み<br>必須 | 読み取り可能な、関連する採用要求の一意識別子です。 |
| **採用要求 ID 値**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmrecruitingrequestentity の mshr_hcmrecruitingrequestentityid | システムが生成する、関連する採用要求の一意識別子です。 |
| **教育レベル ID**<br>mshr_educationlevelid<br>*文字列* | 1回書き込み<br>必須 | 要求される教育のレベルです。 |
| **教育レベル ID 値**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmeducationlevelentity の mshr_hcmeducationlevelentityid | システムが生成した、要求される教育のレベルの一意識別子です。 |
| **教育レベルの説明**<br>mshr_educationleveldescription<br>*文字列* | 読み取り専用<br>必須 | スキルに要求されるレベルの説明です。 |
| **教育の分野 ID**<br>mshr_educationdisciplinedescription<br>*文字列* | 1回書き込み<br>必須 | 教育の分野です。 |
| **教育の分野 ID の値**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmeducationdisciplineentity の mshr_hcmeducationdisciplineentityid | システムが生成した、教育分野の一意識別子です。 |
| **教育分野の説明**<br>mshr_educationdisciplinedescription<br>文字列 | 読み取り専用<br>必須 | 教育分野の説明です。 |
| **データ領域 ID**<br>mshr_dataareaid<br>*文字列* | 読み取り/書き込み<br>オプション | 法人 (会社) を指定します。|
| **データ領域 ID 値**<br>_mshr_dataareaid_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : cdm_companyid of cdm_company エンティティ | システムが生成する、法人 (会社) を識別する GUID 値です。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | レコードを一意に識別する別の方法としての採用要求値、教育レベルID、教育分野 ID の連結です。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
