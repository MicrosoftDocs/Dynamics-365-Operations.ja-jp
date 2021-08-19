---
title: 固定報酬の報酬計画
description: このトピックでは、Dynamics 365 Human Resources における固定報酬の報酬計画エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: f1e5345d9f27106bdf3a3a60cb0480a9b072e340c01236e4d48c5e2ae592ddbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738394"
---
# <a name="payroll-fixed-compensation-plan"></a>固定報酬の報酬計画

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の固定報酬の報酬計画のエンティティについて説明します。

### <a name="description"></a>説明

このエンティティは、従業員の特定の職位に割り当てられた固定報酬プランを提供します。

物理名: mshr_payrollfixedcompensationplanentity。

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **従業員 ID**<br>mshr_fk_employee_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー: mshr_payrollemployeeentity エンティティの mshr_Employee_id  | 従業員 ID |
| **支払レート**<br>mshr_payrate<br>*実数* | 読み取り専用<br>必須 | 固定報酬計画で定義された支払レート。 |
| **計画 ID**<br>mshr_planid<br>*文字列* | 読み取り専用<br>必須 |報酬計画を指定します。  |
| **発効日**<br>mshr_validfrom<br>*日時オフセット* |  読み取り専用<br>必須 |従業員の固定報酬が有効になる日付。  |
| **固定報酬の報酬計画エンティティ**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | 必須<br>システム生成 | システムで生成する、報酬計画を一意に識別する GUID 値です。 |
| **支払頻度**<br>mshr_payfrequency<br>*文字列* | 読み取り専用<br>必須 |従業員に支払われる頻度。  |
| **失効日**<br>mshr_validto<br>*日時オフセット* | 読み取り専用 <br>必須 | 従業員の固定報酬が有効な日付。 |
| **職位 ID**<br>mshr_positionid<br>*文字列* | 読み取り専用 <br>必須 | 従業員および固定報酬計画の登録に関連付けられた職位 ID。 |
| **通貨**<br>mshr_currency<br>*文字列* | 読み取り専用 <br>必須 |固定報酬計画に定義されている通貨   |
| **個人番号**<br>mshr_personnelnumber<br>*文字列* | 読み取り専用<br>必須 |従業員の一意の職員番号。  |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**応答**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
