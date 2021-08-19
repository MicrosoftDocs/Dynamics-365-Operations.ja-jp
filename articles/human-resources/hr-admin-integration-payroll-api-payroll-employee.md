---
title: 給与従業員
description: このトピックでは、Dynamics 365 Human Resources における給与従業員エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768194"
---
# <a name="payroll-employee"></a>給与従業員

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与従業員のエンティティについて説明します。

物理名: mshr_payrollemployeeentity。

### <a name="description"></a>説明

このエンティティは、従業員に関する情報を提供します。 このエンティティを使用する前、[給与統合のパラメーター](hr-admin-integration-payroll-api-parameters.md) を設定する必要があります。

>[!IMPORTANT] 
>**FirstName**、**MiddleName**、**LastName**、**NameValidFrom**、および **NameValidTo** フィールドは、このエンティティで使用できなくなりました。 これにより、このエンティティを管理する有効日データ ソースは 1 つだけになります。
>これらのフィールドは、プラットフォーム更新プログラム 43 でリリースされた **DirPersonNameHistoricalEntity** で使用できます。 **個人** フィールドに **PayrollEmployeeEntity** から **DirPersonNameHistoricalEntity** への OData リレーションシップがあります。 

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **個人番号**<br>mshr_personnelnumber<br>*文字列* | 読み取り専用 | 従業員の一意の職員番号。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>システム生成 |  |
| **法人 ID**<br>mshr_legalentityID<br>*文字列* | 読み取り専用 | 法人 (会社) を指定します。 |
| **種類**<br>mshr_gender<br>[mshr_hcmpersongender オプション セット](hr-admin-integration-payroll-api-gender.md) | 読み取り専用 | 従業員の性別。 |
| **給与従業員エンティティ ID**<br>mshr_payrollemployeeentityid<br>*GUID* | 必須<br>システム生成 | 従業員を一意に識別するためのシステム生成の GUID 値。 |
| **雇用開始日**<br>mshr_employmentstartdate<br>*日時オフセット* | 読み取り専用 | 従業員の雇用開始日。 |
| **識別タイプ ID**<br>mshr_identificationtypeid<br>*文字列* |読み取り専用 | 従業員に対して定義される ID タイプ。 |
| **雇用終了日**<br>mshr_employmentenddate<br>*日時オフセット* | 読み取り専用 |従業員の雇用の終了。  |
| **データ領域 ID**<br>mshr_dataareaid_id<br>*GUID* | 読み取り専用 <br>システム生成 | システムが生成する、法人 (会社) を識別する GUID 値です。 |
| **失効日**<br>mshr_namevalidto<br>*日時オフセット* |  読み取り専用 | 従業員情報が有効な日付。 |
| **生年月日**<br>mshr_birthdate<br>*日時オフセット* | 読み取り専用 | 従業員の生年月日 |
| **ID 番号**<br>mshr_identificationnumber<br>*文字列* | 読み取り専用 |従業員に対して定義される ID 番号。  |

## <a name="example-query-for-payroll-employee"></a>給与従業員のクエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
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
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
