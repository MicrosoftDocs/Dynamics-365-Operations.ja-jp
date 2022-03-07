---
title: 給与作業者の福利厚生計画
description: このトピックでは、Dynamics 365 Human Resources における給与労働者福利厚生計画エンティティに対するクエリの詳細および例を示します。
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0837d9a153aba554d0a5293d16afb309bd37963c270da5b67e691558cae63b0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758715"
---
# <a name="payroll-worker-benefit-plan"></a>給与作業者の福利厚生計画

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与労働者福利厚生計画エンティティについて説明します。

物理名 : mshr_payrollworkerbenefitplanentities。

### <a name="description"></a>説明

このエンティティは、特定の作業者の福利厚生計画に関する情報を提供します。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **個人番号**</br>mshr_personnelnumber</br>*文字列* | 読み取り専用</br>必須 | 従業員の一意の職員番号。 |
| **法人 ID**</br>mshr_legalentityID</br>*文字列* | 読み取り専用 | 法人 (会社) を指定します。 |
| **期間 ID**</br>mshr_periodid</br>*文字列* | 読み取り専用 | 期間の ID。 |
| **計画 ID**</br>mshr_planid</br>*文字列* | 読み取り専用 | 計画の ID。 |
| **補償オプション**</br>mshr_coverageoptionid</br>*文字列* | 読み取り専用 | 補充オプションの ID。 |
| **控除開始日**</br>mshr_deductionstartdatetime</br>*日時オフセット* | 読み取り専用 | 控除開始日。 |
| **控除終了日**</br>mshr_deductionenddatetime</br>*日時オフセット* | 読み取り専用 | 控除終了日。 |
| **状態**</br>mshr_status</br>*[従業員の福利厚生の状態オプション セット](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | 読み取り専用 | 福利厚生計画の状態。 |
| **発効日**</br>mshr_validfrom</br>*日時オフセット* | 読み取り専用 | このレコードの有効開始時刻です。 |
| **失効日**</br>mshr_validto</br>*日時オフセット* |  読み取り専用 | このレコードの有効終了時刻です。 |
| **計画タイプ ID**</br>mshr_plantypeid</br>*文字列* | 読み取り専用 | 計画タイプの ID。 |
| **計画タイプ コード**</br>mshr_plantypecode</br>*[福利厚生計画タイプ カバー オプション セット](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | 読み取り専用 | 計画タイプの仕様。 |
| **支払い期間数**</br>mshr_payperiod</br>*整数* | 読み取り専用 | 支払期間数は給付金プロバイダーまたは従業員に支払われる頻度を表します。 この金額は、従業員の年間給付金給与金額を計算するために使用されます。 |
| **従業員金額**</br>mshr_amountemployee</br>*小数* | 読み取り専用 | 従業員の金額またはパーセンテージ。 |
| **雇用主金額**</br>mshr_amountemployer</br>*小数* | 読み取り専用 | 従業員の金額またはパーセンテージ。 |
| **基本フィールド**</br>mshr_primaryfield</br>*文字列* | システム生成 | 基本フィールド。 |
| **作業者 ID の値** </br>_mshr_fk_worker_id_value</br>*GUID* | 外部キー : mshr_hcmworkerbaseentity entity の mshr_hcmworkerbaseentityid。 | システムが生成した、作業者の一意識別子です。 |
| **期間 ID 値**</br> _mshr_fk_period_id_value</br>*GUID* | 外部キー : mshr_benefitperiodentityid の mshr_benefitperiodentity エンティティ。 | システムが生成した、期間の一意識別子です。 |
| **計画 ID 値**</br> _mshr_fk_plan_id_value</br>*GUID* | 外部キー : mshr_benefitplanentity の mshr_benefitplanentityid エンティティ。 | システムが生成した、計画の一意識別子です。 |
| **計画タイプ ID の値**</br> _mshr_fk_plantype_id_value</br>*GUID* | 外部キー : mshr_benefitplantypeentity の mshr_benefitplantypeentityid エンティティ。 | システムが生成した、計画の一意識別子です。 |
| **補充オプション ID 値**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | 外部キー : mshr_benefitcoverageoptionentity の mshr_benefitcoverageoptionentityid エンティティ。 | システムが生成した、計画の一意識別子です。 |
| **給与労働者給付計画エンティティ ID 値**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | 読み取り専用 </br> システム生成 | システムが生成した、レコードの一意識別子です。 |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>給与作業者福利厚生計画のクエリの例

**申請**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**応答**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
