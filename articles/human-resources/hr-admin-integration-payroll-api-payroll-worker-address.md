---
title: 給与作業者の住所
description: このトピックでは、Dynamics 365 Human Resources における給与作業者の住所エンティティに対するクエリの詳細および例を示します。
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882022"
---
# <a name="payroll-worker-address"></a>給与作業者の住所

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources における給与作業者の住所エンティティに対するクエリの詳細および例を示します。

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **市町村**<br>mshr_city<br>*文字列* | 読み取り専用<br>必須 | 住所に定義されている市町村。   |
| **個人番号**<br>mshr_personnelnumber<br>*文字列* | 読み取り専用<br>必須 | 従業員の一意の職員番号。  |
| **国地域**<br>mshr_countryregionid<br>*文字列* | 読み取り専用<br>必須 | 住所に定義されている国の地域  |
| **発効日**<br>mshr_postaladdressvalidfrom<br>*日時オフセット* | 読み取り専用 <br>必須 | 住所が有効な日付。 |
| **住所で作業**<br>mshr_isworkedinaddressbr>*Int32* | 読み取り専用<br>必須 | 住所が従業員の勤務地であるかどうかを表します。 |
| **郡**<br>mshr_county<br>*文字列* | 読み取り専用<br>必須 | 住所に定義されている国。  |
| **給与作業者の住所 ID**<br>mshr_payrollworkeraddressentityid<br>*GUID* | 必須<br>システム生成 | 住所を一意に識別するためのシステム生成の GUID 値。  |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 |  |
| **住所**<br>mshr_street<br>*文字列* | 読み取り専用<br>必須 | 住所に定義されている番地。 |
| **失効日**<br>mshr_postaladdressvalidto<br>*日時オフセット* | 読み取り専用 <br>必須 | 住所が有効な日付。  |
| **場所 ID**<br>mshr_locationidbr>*文字列* | 読み取り専用 <br>必須 | 住所の ID。  |
| **郵便番号**<br>mshr_zipcode<br>*文字列* | 読み取り専用 <br>必須 |従業員に対して定義される ID 番号。  |
| **住所に住んでいた**<br>mshr_islivedinaddressbr>*文字列* | 読み取り専用<br>必須 | 住所が従業員の居住地であるかどうかを表します。 |
| **行政単位 (区画)**<br>mshr_state<br>*文字列* | 読み取り専用<br>必須 | 住所に定義されている状態。  |

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
