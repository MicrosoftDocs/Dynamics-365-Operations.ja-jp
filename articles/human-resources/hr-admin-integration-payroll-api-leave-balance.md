---
title: 休暇残高
description: このトピックでは、Dynamics 365 Human Resources における休暇残高エンティティに対するクエリの詳細および例を示します。
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab136e9b40de280387dc3c5207a08a6bb357941feb3a8c736d9671f7850f2bf8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782686"
---
# <a name="leave-balance"></a>休暇残高

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の休暇残高エンティティについて説明します。

### <a name="description"></a>説明

このエンティティは、指定された従業員の休暇タイプごとの休暇残高を提供します。

物理名 : mshr_essleavebalanceentities。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **個人番号**</br>mshr_personnelnumber</br>*文字列* | 読み取り専用 | 従業員の一意の職員番号。 |
| **現在の残日数**</br>mshr_balanceavailable</br>*実数* | 読み取り専用 | 従業員の現在の残高です。 |
| **種類**</br>mshr_balanceavailable</br>*文字列* | 読み取り専用 | 休暇タイプ ID です。 |
| **見越計上率**</br>mshr_accrualratedescription</br> | 読み取り専用 | 見越計上レートです。 |
| **最新の繰越残日数**</br>mshr_lastcarryforwardamount</br>*実数* | 読み取り専用 | 前回の繰越量です。 |
| **今年度に取得**</br>mshr_takenthisyear</br>*実数* | 読み取り専用 | 今年度取得した休暇の量です。 |
| **今年度の合計休暇日数**</br>mshr_totalthisyear</br>*実数* | 読み取り専用 | 今年度の総計です。 |
| **データ領域 ID**</br>mshr_dataareaid_id</br>*文字列* | 読み取り専用 | 法人 (会社) を指定します。 |
| **基本フィールド**</br>mshr_primaryfield</br>*GUID* | 読み取り専用</br>システム生成 | |
| **休暇タイプ ID**</br>_mshr_fk_leavetype_id_value</br>*GUID* | 読み取り専用</br>外部キー : mshr_essleavetypeentity エンティティの mshr_essleavetypeentityid  | 休暇タイプ ID |
| **休暇残高エンティティ**</br>mshr_essleavebalanceentityid</br>*GUID* | システム生成 | 残高を一意に識別するためのシステム生成の GUID 値です。 |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**応答**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
