---
title: 給与従業員
description: このトピックでは、Dynamics 365 Human Resources における給与従業員エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 450872a38c833de9d37e2c6224839f2bca7cb4c6
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429238"
---
# <a name="payroll-employee"></a>給与従業員

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与従業員のエンティティについて説明します。

物理名: mshr_payrollemployeeentity。

### <a name="description"></a>説明

このエンティティは、従業員に関する情報を提供します。 このエンティティを使用する前、[給与統合のパラメーター](hr-admin-integration-payroll-api-parameters.md) を設定する必要があります。

>[!IMPORTANT] 
>**FirstName**、**MiddleName**、**LastName**、**NameValidFrom**、および **NameValidTo** フィールドは、このエンティティで使用できなくなりました。 これにより、このエンティティを管理する有効日データ ソースは 1 つだけになります。
>これらのフィールドは、プラットフォーム更新プログラム 43 でリリースされた **DirPersonNameHistoricalEntity** で使用できます。 **PayrollEmployeeEntity** から **DirPersonNameHistoricalEntity** への OData リレーションシップがあります。 

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **法人 ID**</br>mshr_legalentityid</br>*文字列* | 読み取り専用 | 法人 (会社) を指定します。 |
| **個人番号**</br>mshr_personnelnumber</br>*文字列* | 読み取り専用 | 従業員の一意の職員番号。 |
| **雇用開始日**</br>mshr_employmentstartdate</br>*日時オフセット* | 読み取り専用 | 従業員の雇用開始日。 |
| **雇用終了日**</br>mshr_employmentenddate</br>*日時オフセット* | 読み取り専用 |従業員の雇用の終了。  |
| **生年月日**</br>mshr_birthdate</br>*日時オフセット* | 読み取り専用 | 従業員の生年月日。 |
| **種類**</br>mshr_gender</br>[mshr_hcmpersongender オプション セット](hr-admin-integration-payroll-api-gender.md) | 読み取り専用 | 従業員の性別。 |
| **雇用タイプ**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype オプション セット](hr-admin-integration-payroll-api-hcmemploymenttype.md) | 読み取り専用 | 雇用タイプ。 |
| **識別タイプ ID**</br>mshr_identificationtypeid</br>*文字列* |読み取り専用 | 従業員に対して定義される ID タイプ。 |
| **ID 番号**</br>mshr_identificationnumber</br>*文字列* | 読み取り専用 |従業員に対して定義される ID 番号。 |
| **支払準備完了**</br>mshr_readytopay</br>[mshr_noyes オプション セット](hr-admin-integration-payroll-api-no-yes.md) | 読み取り専用 | 従業員が支払準備完了としてマークされたかどうかを示します。 |
| **給与従業員エンティティ ID**</br>mshr_payrollemployeeentityid</br>*GUID* | 必須</br>システム生成 | 従業員を一意に識別するためのシステム生成の GUID 値。 |

## <a name="relations"></a>リレーション

|プロパティ値 | 関連するエンティティ | ナビゲーション プロパティ | コレクション タイプ |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | - |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | - |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>給与従業員のクエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**応答**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
