---
title: 人物のスキル
description: このトピックでは、Dynamics 365 Human Resources の人物のスキル エンティティについて説明します。
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
ms.openlocfilehash: 03181d6377fdacee0faa600551e8b7ad7c68a76d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059235"
---
# <a name="person-skill"></a>人物のスキル

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物のスキル エンティティについて説明します。

物理名 : mshr_hcmpersonskillentity

## <a name="description"></a>説明

このエンティティは、候補者のスキルを表します。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **人物のスキル ID**<br>mshr_hcmpersonskillentityid<br>*GUID* | 読み取り専用<br>必須 | システムが生成した、エンティティ レコードの一意識別子です。 |
| **関係者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 |   関連付けられている当事者 (人物) レコードの ID です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity の mshr_dirpersonentityid | システムが生成する、当事者 (個人) エンティティ レコードの識別子です。 |
| **証明者**<br>mshr_certifier<br>*文字列* | 読み取り/書き込み<br>オプション | このスキルを認定した従業員の職員番号です。 |
| **証明者 ID の値**<br>_mshr_fk_certifier_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmworkerentity の mshr_hcmworkerentityid | システムが生成したスキルを認定した従業員の従業員レコードの一意の識別子です。 |
| **スキル ID**<br>mshr_skillid<br>*文字列* | 読み取り/書き込み<br>必須 | Human Resources で定義されているスキルの識別子です。 |
| **スキル ID の値**<br>_mshr_fk_skill_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmskillentity の mshr_hcmskillentityid | システムが生成した選択されたスキルの識別子です。 |
| **経験年数**<br>mshr_yearsofexperience<br>*実数* | 読み取り/書き込み<br>オプション | このスキルについて候補者が経験した年数です。 |
| **評価 ID**<br>mshr_ratingid<br>*文字列* | 読み取り/書き込み<br>必須 | 評価スケールのタイプです。 このエンティティの値は **スキル** です。 |
| **レベルのタイプ**<br>mshr_leveltype<br>*mshr_hrmskillleveltype オプション セット* | 読み取り/書き込み<br>必須 | スキルに割り当てられたレベルの分類タイプです。 |
| **レベル ID**<br>mshr_levelid<br>*文字列* | 読み取り/書き込み<br>必須 | このスキルに対する候補者の評価レベル ID です。 |
| **評価レベル ID 値**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmratinglevelentity の mshr_hcmratinglevelentityid | システムが生成した評価レベルの識別子です。 |
| **レベルの日付**<br>mshr_leveldate<br>*Datetime* | 読み取り/書き込み<br>必須 | 候補者のスキルが評価された日付です。 |
| **評価レベル検証者**<br>mshr_ratinglevelexaminer<br>*文字列* | 読み取り/書き込み<br>オプション | この候補者を評価した従業員の職員番号です。 |
| **評価レベル検証者 ID 値**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmworkerentity の mshr_hcmworkerentityid | システムが生成する、候補者のスキルレベルを審査した従業員の識別子です。 |
| **検証済**<br>mshr_verified<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>必須 | 評価されたスキルレベルが検証されたかどうかを示します。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | エンティティ レコードの識別子として使用されるフィールドです。 関係者番号、レベルのタイプ、スキル ID、レベルの日付けの組み合わせです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]