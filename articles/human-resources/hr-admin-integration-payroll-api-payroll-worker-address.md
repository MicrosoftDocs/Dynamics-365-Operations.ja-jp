---
title: 給与作業者の住所
description: このトピックでは、Dynamics 365 Human Resources における給与作業者の住所エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 70e42cbf657a28327699d927731edd36de7c4a64
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069760"
---
# <a name="payroll-worker-address"></a>給与作業者の住所


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の給与作業者の住所のエンティティについて説明します。

物理名: mshr_payrollworkeraddressentity。

### <a name="description"></a>説明

このエンティティは、特定の従業員の給与居住の場所と給与作業の場所を提供します。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **個人番号**</br>mshr_personnelnumber</br>*文字列* | 読み取り専用 | 従業員の一意の職員番号。 |
| **場所 ID**</br>mshr_locationidbr>*文字列* | 読み取り専用 | 住所の ID。 |
| **住所に住んでいた**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes オプション セット](hr-admin-integration-payroll-api-no-yes.md)* | 読み取り専用 | 住所が従業員の居住地であるかどうかを示す値。 |
| **住所で作業** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes オプション セット](hr-admin-integration-payroll-api-no-yes.md)* | 読み取り専用 | 住所が従業員の勤務地であるかどうかを示す値。 |
| **国地域**</br>mshr_countryregionid</br>*文字列* | 読み取り専用</br>必須 | 住所に定義されている国や地域。 |
| **郵便番号**</br>mshr_zipcode<br>*文字列* | 読み取り専用 | 従業員に対して定義されている ID 番号。 |
| **住所**</br>mshr_street</br>*文字列* | 読み取り専用 | 住所に定義されている番地。 |
| **市区町村**</br>mshr_city</br>*文字列* | 読み取り専用 | 住所に定義されている市区町村。 |
| **行政単位 (区画)**</br>mshr_state</br>*文字列* | 読み取り専用 | 住所に定義されている都道府県。 |
| **郡**</br>mshr_county</br>*文字列* | 読み取り専用 | 住所に定義されている国。 |
| **発効日**</br>mshr_postaladdressvalidfrom</br>*日時オフセット* | 読み取り専用 | 住所が有効となる開始日付。 |
| **失効日**</br>mshr_postaladdressvalidto</br>*日時オフセット* | 読み取り専用 | 住所が有効な日付の期限。 |
| **基本フィールド**</br>mshr_primaryfield</br>*文字列* | 読み取り専用 | プライマリ フィールド。 |
| **給与作業者の住所 ID**</br>mshr_payrollworkeraddressentityid</br>*GUID* | システム生成 | 住所を一意に識別するための、システムが生成したグローバルに一意な識別子 (GUID) の値です。 |

## <a name="relations"></a>リレーション

| プロパティ値 | 関連するエンティティ | ナビゲーション プロパティ | コレクション タイプ |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**応答**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
