---
title: 給与職位職務
description: この記事では、Dynamics 365 Human Resources における給与職位職務エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: fa347f4b99adc7c29d69daf62ad2bbfc14726a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864086"
---
# <a name="payroll-position-job"></a>給与職位職務


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の給与職位職務のエンティティについて説明します。

### <a name="description"></a>Description

このエンティティは、特定の固定報酬プランの職位と職務の関係を提供します。

物理名: mshr_payrollpositionjobentity。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **職位 ID**</br>mshr_positionid</br>*文字列* | 読み取り専用 | 職位の ID。 |
| **発効日**</br>mshr_validto</br>*日時オフセット* | 読み取り専用 | 役職や職務関係が有効となる日付。 |
| **失効日**</br>mshr_validto</br>*日時オフセット* | 読み取り専用 | 職位とジョブの関係が有効な日付。 |
| **ジョブ ID**</br>mshr_jobid</br>*文字列* | 読み取り専用 | ジョブの ID。 |
| **基本フィールド**</br>mshr_primaryfield</br>*文字列* | システム生成 | プライマリ フィールド。 |
| **給与職位職務エンティティ ID**</br>mshr_payrollpositionjobentityid</br>*Guid* | システム生成。 | 職務を一意に識別するための、システムが生成したグローバルに一意な識別子 (GUID) の値です。 |

## <a name="relations"></a>リレーション

| プロパティ値 | 関連するエンティティ | ナビゲーション プロパティ | コレクション タイプ |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | 該当なし |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

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
