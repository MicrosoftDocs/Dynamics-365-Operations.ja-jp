---
title: 人物の住所
description: このトピックでは、Dynamics 365 Human Resources の人物の住所エンティティについて説明します。
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
ms.openlocfilehash: 9911362ff8260860864cfe24f0b60f59adb77186
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125885"
---
# <a name="person-address"></a>人物の住所

このトピックでは、Dynamics 365 Human Resources の人物の住所エンティティについて説明します。

物理名 : mshr_hcmpersonaddressentities

## <a name="description"></a>説明

このエンティティには、候補者レコードの郵便番号の一覧が含まれます。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **人物の住所のエンティティ ID**<br>mshr_hcmpersonaddressentityid<br>*文字列* | 読み取り専用<br>必須 | システムが生成した、エンティティ レコードの一意識別子です。 |
| **当事者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 | 関連付けられている当事者 (人物) レコードの ID です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity の mshr_dirpersonentityid | システムが生成する、当事者 (個人) エンティティ レコードの識別子です。 |
| **場所 ID**<br>mshr_locationid<br>*文字列* | 読み取り/書き込み<br>必須 | 住所レコードの場所 ID です。 mshr_logisticspostaladdresslocationcdsentity エンティティ内の設定をします。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>必須 | 候補者の住所の説明です。 |
| **ロール**<br>mshr_roles<br>*文字列* | 読み取り/書き込み<br>必須 | この住所に割り当てられたロールです。 複数のロールを割り当てることができます。 各ロールは、セミコロンで区切る必要があります。 有効な値は mshr_logisticslocationroleentity エンティティに含まれています。 |
| **住所**<br>mshr_street<br>*文字列* | 読み取り/書き込み<br>オプション | 番地です。 |
| **市町村**<br>mshr_city<br>*文字列* | 読み取り/書き込み<br>オプション | 住所の市町村。 mshr_logisticsaddresscityentity エンティティで設定します。 |
| **行政単位 (区画)**<br>mshr_state<br>*文字列* | 読み取り/書き込み<br>オプション | 住所の都道府県です。 mshr_logisticsaddressstateentity エンティティで設定します。 |
| **郡**<br>mshr_county<br>*文字列* | 読み取り/書き込み<br>オプション | 住所の市区郡。 mshr_logisticsaddresscountyentity エンティティで設定します。 |
| **郵便番号**<br>mshr_zipcode<br>*文字列* | 読み取り/書き込み<br>オプション | 住所の郵便番号です。 mshr_logisticsaddresspostalcodeentity エンティティで設定します。 |
| **国/地域 ID**<br>mshr_countryregionid<br>*文字列* | 読み取り/書き込み<br>オプション | 住所の国または地域。 |
| **国/地域 ID 値**<br>_mshr_fk_countriregion_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_logisticsaddresscountryregionentity の mshr_logisticaddresscountryregionentityid | システムが生成する国/地域の住所の一意識別子です。 |
| **基本**<br>mshr_isprimary<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>必須 | この住所が、定義されたロールの人物の基本住所であるかどうかを識別します。 |
| **は非公開です**<br>mshr_isprivate<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>必須 | この住所が個人のプライベート アドレスかどうかを識別します。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | エンティティ レコードの基本識別子として使用されるフィールドです。 関係者番号と場所 ID の組み合わせです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]