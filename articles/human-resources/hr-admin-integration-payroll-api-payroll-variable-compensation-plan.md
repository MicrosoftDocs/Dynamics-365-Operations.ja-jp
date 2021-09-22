---
title: 給与の変動報酬計画
description: このトピックでは、Dynamics 365 Human Resources における給与の変動報酬計画エンティティに対するクエリの詳細および例を示します。
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c30df23debed9e2ab90745e6ea9d0e6b8a05b6d5
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429270"
---
# <a name="payroll-variable-compensation-plan"></a>給与の変動報酬計画

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与の変動報酬計画エンティティについて説明します。

### <a name="description"></a>説明

このエンティティは、従業員の特定の職位に割り当てられた変動報酬計画を提供します。

物理名 : mshr_payrollvariablecompensationawardentity。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **個人番号**</br>mshr_personnelnumber</br>*文字列* | 読み取り専用 | 従業員の一意の職員番号。  |
| **報酬日**</br>mshr_awarddate</br>*日時オフセット* | 読み取り専用 | 報奨の日付です。 |
| **報奨タイプ**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType オプション セット](hr-admin-integration-payroll-api-award-type.md)* | 読み取り専用 | 変動報酬計画で定義されている報奨タイプです。 |
| **通貨**</br>mshr_unitcurrencycode</br>*文字列* | 読み取り専用 |変動報酬計画で定義されている通貨です。   |
| **固定報酬計画 ID**</br>mshr_fixedplanid</br>*文字列* | 読み取り専用 | 報奨の計算の規準として使用される固定報酬計画です。 |
| **単位値**</br>mshr_awardamount</br>*実数* | 読み取り専用 | 単位の値 |
| **プロセスのタイプ**</br>mshr_processtype</br>*[mshr_hrmCompProcessType オプション セット](hr-admin-integration-payroll-api-process-type.md)* | 読み取り専用 | プロセスのタイプです。 |
| **変動報酬計画タイプ**</br>文字列</br>*mshr_typeid* | 読み取り専用 | 変動報酬計画のタイプです。 |
| **変動報酬計画 ID**</br>文字列</br>*mshr_planid* | 読み取り専用 | 変動報酬計画の ID です。 |
| **単位数**</br>小数</br>*mshr_numberofunits* | 読み取り専用 | 報酬の単位数を入力します。 |
| **基本フィールド**</br>mshr_primaryfield</br>*GUID* | 読み取り専用</br>システム生成。 | |
| **給与の変動報酬計画エンティティ**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | システム生成 | システムで生成する、報酬計画を一意に識別する GUID 値です。 |

## <a name="relations"></a>リレーション 

|プロパティ値 | 関連するエンティティ | ナビゲーション プロパティ | コレクション タイプ |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**応答**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
