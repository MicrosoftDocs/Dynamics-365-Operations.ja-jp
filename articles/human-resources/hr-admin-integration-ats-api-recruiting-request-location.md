---
title: 採用要求場所
description: この記事では、Dynamics 365 Human Resources の採用要求場所エンティティについて説明します。
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
ms.openlocfilehash: d31af9ab62db310b89fbc7a2d7099621b59a356d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893819"
---
# <a name="recruiting-request-location"></a>採用要求場所


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の採用要求場所エンティティについて説明します。

物理名 : mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>説明

採用した社員が採用時に働く場所として定義されている場所の一覧です。 これらは、法人間で作成された場所です。

### <a name="json-representation"></a>JSON 表記

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **場所 ID**<br>mshr_locationid<br>*文字列* | 1回書き込み<br>必須 | システムが生成する、ユーザーが可読な、採用場所の一意識別子です。 |
| **採用要求場所**<br>mshr_recruitingrequestlocationid<br>*文字列* | 1回書き込み<br>必須 | ユーザー定義の採用場所の一意識別子です。 |
| **採用で要求する場所エンティティ ID**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | 読み取り専用<br>必須 | システムが生成した、採用で要求する場所レコードの一意識別子です。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>必須 | 場所の説明です。 |
| **国/地域 ID**<br>mshr_countryregionid<br>*文字列* | 読み取り専用<br>オプション | 候補者が市民権を有する国、または地域を指定します。 |
| **国/地域 ID 値**<br>_mshr_fk_countriregion_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_logisticsaddresscountryregionentity の mshr_logisticaddresscountryregionentityid | システムが生成する国/地域の住所の一意識別子です。 |
| **ZipCode**<br>mshr_zipcode<br>*文字列* | 読み取り専用<br>オプション | 郵便番号です。 |
| **住所**<br>mshr_street<br>*文字列* | 読み取り専用<br>オプション | 住所の番地です。 |
| **市町村**<br>mshr_city<br>*文字列* | 読み取り専用<br>オプション | 市町村です。 |
| **行政単位 (区画)**<br>mshr_state<br>*文字列* | 読み取り専用<br>オプション | 都道府県です。 |
| **郡**<br>mshr_county<br>*文字列* | 読み取り専用<br>オプション | 郡です。 |
| **電話**<br>mshr_telephone<br>*文字列* | 読み取り/書き込み<br>オプション | 当該場所の電話番号です。 |
| **メール**<br>mshr_email<br>*文字列* | 読み取り/書き込み<br>オプション | メール アドレスです。 |
| **InternetAddress**<br>mshr_internetaddress<br>*文字列* | 読み取り/書き込み<br>オプション | 当該場所の Web サイトの URL です。 |
| **データ領域 ID**<br>mshr_dataareaid<br>*文字列* | 読み取り/書き込み<br>オプション | 法人 (会社) を指定します。 |
| **データ領域 ID 値**<br>_mshr_dataareaid_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : cdm_companyid of cdm_company エンティティ | システムが生成する、法人 (会社) を識別する GUID 値です。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
