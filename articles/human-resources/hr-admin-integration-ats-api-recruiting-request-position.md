---
title: 採用要求職位
description: このトピックでは、Dynamics 365 Human Resources の採用要求職位のエンティティについて説明します。
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
ms.openlocfilehash: 4892dc0801a47ab7c219df00b997fa469f56b7fc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464697"
---
# <a name="recruiting-request-position"></a>採用要求職位

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の採用要求職位のエンティティについて説明します。

物理名 : mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>説明

採用要求に対応する職位についての説明です。 採用要求への職位の追加はオプションです。 職位のプロパティは、職位マスター レコード上のものとは異なり、採用要求上では異なってはいけないため、職位のプロパティは読み取り専用です。 プロパティを変更する必要がある場合は、採用要求に職位を追加する前に、職位マスターレコード上で行う必要があります。

### <a name="json-representation"></a>JSON 表記
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **採用で要求する職位のエンティティ ID**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | 読み取り専用<br>必須 |    システムが生成する、採用で要求する職位レコードの識別子です。 |
| **採用要求 ID**<br>mshr_recruitingrequestid<br>*文字列* | 1回書き込み<br>必須 | 読み取り可能な、採用要求の一意識別子です。 |
| **採用要求 ID 値**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmrecruitingrequestentity エンティの mshr_hcmrecruitingrequestentityid | システムが生成する、職位が割り当てられている採用要求の識別子です。 |
| **職位 ID**<br>mshr_positionid<br>*文字列* | 1回書き込み<br>必須 | 読み取り可能な、職位の一意識別子です。 |
| **ポジション ID の値**<br>_mshr_fk_position_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmpositionv2entity エンティティの mshr_hcmpositionv2entityid | システムが生成する職位の識別子です。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り専用<br>必須 | 職位の説明です。 |
| **職位タイプ ID**<br>mshr_positiontypeid<br>*文字列* | 読み取り専用<br>オプション | 読み取り可能な、この職位タイプの一意識別子です。 |
| **職位タイプ ID 値**<br>_mshr_fk_positiontype_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmpositiontypeentity エンティティの mshr_hcmpositiontypeentityid | システムが生成する、この職位タイプの一意識別子です。 |
| **状態**<br>mshr_status<br>*RecruitingRequestPositionStatus* オプション セット | 読み取り/書き込み<br>必須 | 採用要求の職位の状態を示します。 |
| **部門番号**<br>mshr_departmentnumber<br>*文字列* | 読み取り専用<br>オプション<br> | 職位の部門番号です。 |
| **部門 ID 値**<br>_mshr_fk_department_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_omdepartmententity entity の mshr_omdepartmententityid | システムが生成する、職位が属する部門の一意識別子です。 |
| **報告先の職位 ID**<br>mshr_reportstopositionid<br>*文字列* | 読み取り専用<br>必須 | ユーザーが読み取り可能な、組織階層の中で、採用された職位が所属する職位の ID です。 |
| **所属する職位 ID の値**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmpositionv2entity エンティティの mshr_hcmpositionv2entityid | システムが生成する、採用されたポジションが属する職位の ID です。 |
| **個人番号に属する**<br>mshr_reportstopersonnelnumber<br>*文字列* | 読み取り専用<br>必須 | 採用された候補者が属する従業員の従業員 ID です。 |
| **所属する従業員 ID の値**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmworkerbaseentity entity の mshr_hcmworkerbaseentityid | システムが生成する、採用された候補者が属する従業員の ID です。 |
| **財務分析コード**<br>mshr_financialdimension<br>*文字列* | 読み取り専用<br>オプション | 職位に割り当てられている財務分析コード (原価センターなど)。 財務分析コードは、法人ごとの各職位に割り当てられます。 分析コードで定義された原価センターには、mshr_dimattributeomcostcenterentity エンティティからアクセス可能です。 |
| **データ領域 ID**<br>mshr_dataareaid<br>*文字列* | 読み取り/書き込み<br>オプション | 採用要求職位の法人 (会社) を指定します。 |
| **データ領域 ID 値**<br>_mshr_dataareaid_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : cdm_companyid of cdm_company エンティティ | システムが生成する、要求された職位の採用を行う法人 (会社) を識別する GUID 値です。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | レコードを一意に識別する別の方法としての採用要求値、職位 ID の連結です。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]