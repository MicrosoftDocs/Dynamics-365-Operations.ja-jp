---
title: 固定報酬の報酬計画
description: このトピックでは、Dynamics 365 Human Resources における固定報酬の報酬計画エンティティに対するクエリの詳細および例を示します。
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: a3cc431307d840d393a454e91f202c07c38d2512
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559342"
---
# <a name="payroll-fixed-compensation-plan"></a>固定報酬の報酬計画

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の固定報酬の報酬計画のエンティティについて説明します。

### <a name="description"></a>説明

このエンティティは、従業員の特定の職位に割り当てられた固定報酬プランを提供します。

物理名: mshr_payrollfixedcompensationplanentity。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **計画 ID**</br>mshr_planid</br>*文字列* | 読み取り専用 | 報酬計画を指定します。  |
| **個人番号**</br>mshr_personnelnumber</br>*文字列* | 読み取り専用 | 従業員の一意の職員番号。 |
| **支払レート**</br>mshr_payrate</br>*小数* | 読み取り専用 | 固定報酬計画で定義された支払レート。 |
| **職位 ID**</br>mshr_positionid</br>*文字列* | 読み取り専用 | 従業員および固定報酬計画の登録に関連付けられた職位 ID。 |
| **発効日**</br>mshr_validfrom</br>*日時オフセット* |  読み取り専用 | 従業員の固定報酬が有効になる日付。  |
| **失効日**</br>mshr_validto</br>*日時オフセット* | 読み取り専用 | 従業員の固定報酬が有効な日付。 |
| **支払頻度**</br>mshr_payfrequency</br>*文字列* | 読み取り専用 | 指定された支払レートに対する[報酬支払周期](hr-admin-integration-payroll-api-compensation-pay-frequency.md)の ID です。 |
| **通貨**</br>mshr_currency</br>*文字列* | 読み取り専用 | 固定報酬計画に定義されている通貨。 |
| **固定報酬の報酬計画エンティティ**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | システム生成 | システムで生成する、報酬計画を一意に識別する GUID 値です。 |

## <a name="relations"></a>リレーション

|プロパティ値 | 関連するエンティティ | ナビゲーション プロパティ | コレクション タイプ |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

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
