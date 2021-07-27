---
title: 給与職位職務
description: このトピックでは、Dynamics 365 Human Resources における給与職位職務エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 842c459acd8b5e1a8b6074243b3afa18dc6a13c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314240"
---
# <a name="payroll-position-job"></a>給与職位職務

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与職位職務のエンティティについて説明します。

### <a name="description"></a>説明

このエンティティは、特定の固定報酬プランの職位と職務の関係を提供します。

物理名: mshr_payrollpositionjobentity。

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **ジョブ ID**<br>mshr_jobid<br>*文字列* | 読み取り専用<br>必須 |ジョブの ID。 |
| **発効日**<br>mshr_validto<br>*日時オフセット* | 読み取り専用 <br>必須 | 職位と職務の関係が有効になる日付。 |
| **失効日**<br>mshr_validto<br>*日時オフセット* | 読み取り専用 <br>必須 | 職位とジョブの関係が有効である日付。  |
| **職位 ID**<br>mshr_positionid<br>*文字列* | 読み取り専用<br>必須 | 職位の ID。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 必須<br>システム生成 |  |
| **職位職務 ID の値**<br>_mshr_fk_positionjob_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー: mshr_payrollpositionjobentity の mshr_PayrollPositionJobEntity |この職位に関連付けられているジョブの ID です。|
| **固定報酬の報酬計画 ID 値**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー: mshr_payrollfixedcompensationplanentity の mshr_FixedCompPlan_id  | この職位に関連付けられている固定報酬計画の ID です。 |
| **給与職位職務エンティティ ID**<br>mshr_payrollpositionjobentityid<br>*Guid* | 必須<br>システム生成。 | システムで生成する、ジョブを一意に識別する GUID 値です。  |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**応答**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
