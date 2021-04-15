---
title: 採用要求
description: このトピックでは、Dynamics 365 Human Resources の人物の採用要求エンティティについて説明します。
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
ms.openlocfilehash: dd2f2fc74261c6eea3033567fe020c4e03c60637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805181"
---
# <a name="recruiting-request"></a>採用要求

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物の採用要求エンティティについて説明します。

物理名 : mshr_hcmrecruitingrequestentity

### <a name="description"></a>説明

職務の採用要求に対する説明です。

### <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **採用要求 ID**<br>mshr_recruitingrequestid<br>*文字列* | 読み取り専用<br>必須<br>システム生成 | HR アプリケーションに表示される要求に対するユーザーが読み取り可能な一意識別子です。 番号のシーケンスです。 |
| **採用要求のエンティティ ID**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | 読み取り専用<br>必須<br>システム生成 | システムで生成する、採用要求を一意に識別する GUID 値です。 |
| **データ領域 ID**<br>mshr_dataareaid<br>*文字列* | 読み取り/書き込み<br>オプション<br> | 採用要求の法人 (会社) を指定します。 |
| **データ領域 ID 値**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | 読み取り専用<br>オプション<br>外部キー : cdm_companyid of cdm_company エンティティ | システムが生成する、採用要求を行う法人 (会社) を識別する GUID 値です。 |
| **採用マネージャーの個人番号**<br>mshr_hiringmanagerpersonnelnumber<br>*文字列* | 読み取り/書き込み<br>オプション | この採用要求に関連付けられている採用マネージャの個人番号です。 |
| **採用マネージャー ID 値**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmworkerbaseentity entity の mshr_hcmworkerbaseentityid | システムが生成する、採用要求に関連付けられているマネージャーを識別する GUID 値です。 |
| **採用担当者の関係者番号**<br>mshr_recruiterpartynumber<br>*文字列* | 読み取り/書き込み<br>オプション | 要求で選択された採用担当者の人物 (関係者) 番号です。 |
| **採用担当者 ID 値**<br>_mshr_fk_recruiter_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_dirpersonentity エンティティの mshr_dirpersonentityid | システムが生成する、採用要求に関連付けられている採用担当者を識別する GUID 値です。 |
| **状態**<br>mshr_status<br>*RecruitingRequestStatus* オプション セット | 読み取り/書き込み<br>必須<br> | 採用要求の状態を示します。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>必須 | 要求を説明します。 |
| **採用要求の場所 ID**<br>mshr_recruitingrequestlocationid<br>*文字列* | 読み取り/書き込み<br>オプション | ユーザーが読み取り可能な、この要求に関連付けられているジョブの場所の一意識別子です。 |
| **採用要求の場所 ID 値**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmrecruitingrequestlocationentity entity の mshr_hcmrecruitingrequestlocationentityid | システムが生成する、要求で選択された採用要求の場所を識別する GUID 値です。 |
| **備考**<br>mshr_comments<br>*文字列* | 読み取り/書き込み<br>オプション | マネージャーおよび採用担当者の採用要求に関するコメントです。 |
| **ジョブ ID**<br>mshr_jobid<br>*文字列* | 1回書き込み<br>必須 |   ユーザーが読み取り可能な、この要求に関連するすべてのポジションで共有されている職務の一意識別子です。 |
| **職務 ID の値**<br>_mshr_fk_job_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmjobentity entity の mshr_hcmjobentityid | システムが生成する、採用要求に関連するすべてのポジションで共有されている職務の一意識別子です。 |
| **役職 ID**<br>mshr_titleid<br>*文字列* | 読み取り専用<br>必須 | ユーザーが読み取り可能な、この要求に関連付けられている役職の一意識別子です。 |
| **役職 ID 値**<br>_mshr_fk_title_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmtitleentity entity の mshr_hcmtitleid | システムが生成する、採用要求で選択された役職の一意識別子です。 |
| **職務権限 ID**<br>mshr_jobfunctionid<br>*文字列* | 読み取り専用<br>必須<br>外部キー : mshr_hcmjobfunctionentity entity の mshr_jobfunctionid | ユーザーが読み取り可能な、この要求に関連付けられている職務権限の一意識別子です。 |
| **既定のフルタイム相当値**<br>mshr_defaultfulltimeequivalency<br>*二重* | 読み取り専用<br>必須 | 職務のフルタイムの等価値 (1.0はフルタイムの従業員を表します)。 |
| **規制のジョブ カテゴリ**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory* オプション セット | 読み取り専用<br>オプション | 職務に対して選択された職務権限の EEO 職務カテゴリです。 HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) オプション セットに含まれている有効な値です。 |
| **職務タイプ ID**<br>mshr_jobtypeid<br>*文字列* | 読み取り専用<br>オプション | この職位に関連付けられているジョブのタイプです。 職務タイプはユーザー定義の値であり、mshr_hcmjobtypeentity エンティティで利用可能です。 |
| **職務タイプ ID の値**<br>_mshr_fk_jobtype_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmjobtypenentity entity の mshr_hcmjobtypeentityid | システムが生成する、 採用要求のジョブに関連付けられたジョブタイプの一意識別子です。 |
| **控除状態**<br>mshr_exemptstatus<br>*JobExemptStatus* オプション セット | 読み取り専用<br>オプション | ジョブ タイプに基づく FLSA の控除状態です。 |
| **推定開始日**<br>mshr_estimatedstartdate<br>*日* | 読み取り/書き込み<br>必須 | 候補者が業務を始める見込み開始日です。 |
| **外部説明**<br>mshr_externaldescription<br>*文字列* | 読み取り/書き込み<br>オプション | ジョブ/職位の候補者向け説明です。 | 
| **報酬の低しきい値**<br>mshr_compensationlowthreshold<br>*二重* | 読み取り/書き込み<br>オプション | 報酬レベルの下限です。 |
| **報酬のコントロール ポイント**<br>mshr_compensationcontrolpoint<br>*二重* | 読み取り/書き込み<br>オプション | 報酬レベルのコントロール ポイントです。 |
| **報酬の高しきい値**<br>mshr_compensationhighthreshold<br>*二重* | 読み取り/書き込み<br>オプション | 報酬レベルの上限です。 |
| **報酬レベル**<br>mshr_compensationlevelid<br>*文字列* | 読み取り/書き込み<br>オプション | 職務の報酬レベルです。 ひとつの職務に複数の報酬レベルで設定できます。 この属性は、この要求に対して選択された職務の報酬レベルを示します。 |
| **職務の報酬 ID**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmjobcompensationentity entity の mshr_hcmjobcompensationentityid | システムが生成する、 採用要求の職務に関連した報酬レベルの一意識別子です。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
