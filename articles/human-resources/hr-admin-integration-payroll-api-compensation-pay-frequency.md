---
title: 報酬支払頻度
description: この記事では、Dynamics 365 Human Resources における報酬の支払い周期エンティティに対するクエリの詳細および例を示します。
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9afe27776797b2355a32226bbd7fa514b5c5d962
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894617"
---
# <a name="compensation-pay-frequency"></a>報酬支払頻度


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の報酬の支払い周期エンティティについて説明します。

物理名: mshr_hcmpayrateconversionentity。

### <a name="description"></a>説明

このエンティティは、指定された報酬の支払い周期に対する給与レートの変換に関する情報を提供します。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **年間支払レートの換算**</br>mshr_annualconversionfactor</br>*小数* | 読み取り専用 | 支払頻度の年間変換率。 |
| **説明**</br>mshr_description</br>*文字列* | 読み取り専用 | 変換レートの説明。 |
| **時間支払レートの換算**</br>mshr_hourlyconversionfactor</br>*小数* | 読み取り専用 | 支払頻度の時間ごとの変換率。 |
| **月間支払レートの換算**</br>mshr_monthlyconversionfactor</br>*小数* | 読み取り専用 | 支払頻度の毎月の変換率。 |
| **支払レートの変換**</br>mshr_payrateconversion</br>*文字列* | 読み取り専用 | 換算率を識別する一意の文字列。 |
| **期間**</br>mshr_period</br>*期間オプション セット* | 読み取り専用 | 指定された支払レート換算の主な期間。 |
| **週間支払レートの換算**</br>mshr_weeklyconversionfactor</br>*小数* | 読み取り専用 | 支払頻度の週ごとの変換率。 |
| **データ領域 id**</br>mshr_dataareaid</br>*文字列* | 読み取り専用 | 法人 (会社) です。 |
| **報酬支払頻度のエンティティ ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | システム生成 | レコードを一意に識別するための、システムが生成したグローバルに一意な識別子 (GUID) の値です。 |

## <a name="example-query-for-payroll-employee"></a>給与従業員のクエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**応答**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
