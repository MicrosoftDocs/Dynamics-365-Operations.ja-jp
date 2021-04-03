---
title: 人物の学歴
description: このトピックでは、Dynamics 365 Human Resources の人物の学歴エンティティについて説明します。
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
ms.openlocfilehash: cfa05fe6816c6b24034f8f015bf6e42d665ef1dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466499"
---
# <a name="person-education"></a>人物の学歴

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物の学歴エンティティについて説明します。

物理名 : mshr_hcmpersoneducationentity

## <a name="description"></a>説明

このエンティティには、候補者の学歴が含まれています。 学歴は人物のレコードにリンクされており、候補者のレコードに加えて、作成された他のロール (労働者、請負業者など) を関連付けることができます。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **人物の学歴エンティティ ID**<br>mshr_hcmpersoneducationentityid<br>*GUID* | 読み取り専用<br>必須 | システムが生成した、人物の学歴エンティティ レコードの一意識別子です。 |
| **当事者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 | システムが生成する、候補者の当事者 (個人) レコードの一意識別子です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity の mshr_dirpersonentityid | システムが生成する、候補者の個人レコードの一意識別子です。 |
| **クレジットの基準**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis オプション セット* | 読み取り/書き込み<br>オプション | 教育学位の履修証明の基準です。 |
| **完了した履修証明**<br>mshr_creditscompleted<br>*実数* | 読み取り/書き込み<br>オプション | 学歴の履修証明数です。 |
| **取得した履修証明**<br>mshr_creditsearned<br>*実数* | 読み取り/書き込み<br>オプション | 学位取得のために取得した単位数です。 |
| **必要な履修単位**<br>mshr_creditsneeded<br>*実数* | 読み取り/書き込み<br>オプション | 学位の取得に必要な単位数です。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>オプション | 候補者の学位の説明です。 |
| **教育レベル ID**<br>mshr_educationlevelid<br>*文字列* | 読み取り/書き込み<br>オプション | 教育レベルの ID です。 | 
| **教育レベル ID 値**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmeducationdegreeentity entity の mshr_hcmeducationdegreeentityid | システムが生成した、履修証明レコードの識別子です。 この識別子は、組織で定義された教育および教育レベルを提供します。 |
| **教育の分野 ID**<br>mshr_educationdisciplineid<br>*文字列* | 読み取り/書き込み<br>必須<br>外部キー : EducationDiscipline | 教育分野の ID です。 |
| **教育の分野 ID の値**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmeducationdisciplineentity の mshr_hcmeducationdisciplineentityid | システムが生成する、学歴レコードの教育分野の一意識別子です。 |
| **第二専攻**<br>mshr_secondaryemphasis<br>*文字列* | 読み取り/書き込み<br>オプション | 第二専攻で獲得した学位です。 |
| **教育機関 ID**<br>mshr_educationinstitutionid<br>*文字列* | 読み取り/書き込み<br>オプション | 通学した教育機関の ID です。 |
| **教育機関 ID 値**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmeducationinstitutionentity の mshr_hcmeducationinstitutionentityid | システムが生成された教育機関の ID です。 |
| **開始日**<br>mshr_startdate<br>*Datetime* | 読み取り/書き込み<br>オプション | 取得した学位に関する教育の開始日です。 |
| **終了日**<br>mshr_enddate<br>*Datetime* | 読み取り/書き込み<br>必須 | 資格情報が発行された日付です。 |
| **期間**<br>mshr_duration<br>*実数* | 読み取り/書き込み<br>オプション | 学歴レコードの期間です。 |
| **期間の単位**<br>mshr_durationunit<br>*mshr_periodunit オプション セット* | 読み取り/書き込み<br>オプション | 学歴レコードの期間に関連付けられた期間の単位です。 |
| **成績平均点**<br>mshr_gradepointaverage<br>*実数* | 読み取り/書き込み<br>オプション | 学位で取得した成績平均点です。 |
| **成績評価**<br>mshr_gradescale<br>*文字列* | 読み取り/書き込み<br>オプション | 成績平均点に対する評価です。 |
| **摘要**<br>mshr_notes<br>*文字列* | 読み取り/書き込み<br>オプション | 採用担当者や採用マネージャーが使用するメモです。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | エンティティ レコードのその他基本識別子として使用されるフィールドです。 当事者番号、教育分野 ID、教育機関 ID、教育レベル ID の組み合わせです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]