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
ms.openlocfilehash: 2bbb234d2f51391ea65e3d6153d6cee250f3c6dc
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069810"
---
# <a name="payroll-position"></a>給与職位


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与職位のエンティティについて説明します。

物理名: mshr_payrollpositionentity。

### <a name="description"></a>説明

このエンティティは、特定の従業員の職位に関連する情報を提供します。

物理名: mshr_payrollpositionentity。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **職位 ID**</br>mshr_positionid</br>*文字列* | 読み取り専用 | 職位の ID。 |
| **支払サイクル ID**</br>mshr_paycycleid</br>*文字列* | 読み取り専用 | 職位に定義されている支払サイクル。 |
| **年間基本勤務時間**</br>annualregularhours</br>*小数* | 読み取り専用 | 職位に定義されている年間の基本勤務時間。 |
| **法人による支払**</br>paidbylegalentity</br>*文字列* | 読み取り専用 | 職位に定義されている、支払いを発行する責任を負う法人。 |
| **失効日**</br>validto</br>*日時オフセット* | 読み取り専用 | 職位の詳細が有効となる期限の日付。 |
| **発効日**</br>validfrom</br>*日時オフセット* | 読み取り専用 | 職位の詳細が有効となる開始日付。 |
| **基本フィールド**</br>mshr_primaryfield</br>*文字列* | システム生成 | プライマリ フィールド。 |
| **給与職位詳細エンティティ ID**</br>payrollpositiondetailsentityid</br>*Guid* | 必須</br>システム生成。 | 職位を一意に識別するための、システムが生成したグローバルに一意な識別子 (GUID) の値です。 |

## <a name="relations"></a>リレーション

| プロパティ値 | 関連するエンティティ | ナビゲーション プロパティ | コレクション タイプ |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | 該当なし |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | 該当なし |

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
