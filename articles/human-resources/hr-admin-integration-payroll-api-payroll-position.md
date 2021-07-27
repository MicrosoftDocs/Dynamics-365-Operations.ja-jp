---
title: 職位の給与詳細
description: このトピックでは、Dynamics 365 Human Resources における職位エンティティの給与詳細に対するクエリの詳細および例を示します。
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e13a6b3608802eb7bb2bc00686c2e914cc765587
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314168"
---
# <a name="payroll-position"></a>給与職位

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与職位のエンティティについて説明します。

物理名: mshr_payrollpositionentity。

### <a name="description"></a>説明

このエンティティは、特定の従業員の職位に関連する情報を提供します。

現物名。 

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **年間基本勤務時間**<br>annualregularhours<br>*実数* | 読み取り専用<br>必須 | 職位に定義されている年間基本勤務時間。  |
| **給与職位詳細エンティティ ID**<br>payrollpositiondetailsentityid<br>*Guid* | 必須<br>システム生成。 | 職位を一意に識別するためのシステム生成の GUID 値。  |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 必須<br>システム生成 |  |
| **職位職務 ID の値**<br>_mshr_fk_positionjob_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー: mshr_payrollpositionjobentity の mshr_PayrollPositionJobEntity |この職位に関連付けられているジョブの ID です。|
| **固定報酬の報酬計画 ID 値**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー: mshr_payrollfixedcompensationplanentity の mshr_FixedCompPlan_id  | この職位に関連付けられている固定報酬計画の ID です。 |
| **支払サイクル ID**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | 職位に定義された支払サイクル。 |
| **法人による支払**<br>paidbylegalentity<br>*文字列* | 読み取り専用<br>必須 | 支払の発行を担当する職位で定義されている法人。 |
| **職位 ID**<br>mshr_positionid<br>*文字列* | 読み取り専用<br>必須 | 職位の ID。 |
| **失効日**<br>validto<br>*日時オフセット* | 読み取り専用<br>必須 |職位の詳細が有効になる日付。  |
| **発効日**<br>validfrom<br>*日時オフセット* | 読み取り専用<br>必須 |職位の詳細が有効な日付。  |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**応答**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
