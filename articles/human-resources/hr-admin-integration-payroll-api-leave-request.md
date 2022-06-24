---
title: 休暇申請
description: この記事では、Dynamics 365 Human Resources における休暇申請エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899675"
---
# <a name="leave-request"></a>休暇申請


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の休暇申請エンティティについて説明します。

### <a name="description"></a>Description

このエンティティは、休暇申請の情報を提供します。

物理名 : mshr_essleaverequestentity。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **申請 ID**</br>mshr_requestid</br>*文字列* | 読み取り専用 | 申請 ID です。 |
| **休暇タイプ ID**</br>mshr_leavetypeid</br>*文字列* | 読み取り専用 | 休暇タイプ ID です。 |
| **日**</br>mshr_leavedate</br>*日時オフセット* | 読み取り専用 | 休暇申請の日付です。 |
| **金額**</br>mshr_amount</br>*実数* | 読み取り専用 | 休暇申請の量です。 |
| **半日タイプ**</br>mshr_halfdaydefinition</br>*mshr_LeaveHalfDayDefinition オプション セット* | 読み取り専用 | 半日休暇のタイプです。 |
| **コメント**</br>mshr_comment</br>*文字列* | 読み取り専用 | 申請のコメントです。 |
| **状態**</br>mshr_status</br>*mshr_status オプション セット* | 読み取り専用 | 要求のステータス。 |
| **日**</br>mshr_requestdate</br>*日時オフセット* | 読み取り専用 | 申請の日付です。 |
| **個人番号**</br>mshr_personnelnumber</br>*文字列* | 読み取り専用 | 従業員の一意の職員番号。 |
| **理由コード ID**</br>mshr_reasoncodeid</br>*文字列* | 読み取り専用 | 理由コード ID です。 |
| **データ領域 ID**</br>mshr_dataareaid</br>*文字列* | 読み取り専用 | 法人 (会社) を指定します。 |
| **基本フィールド**</br>mshr_primaryfield</br>*GUID* | 読み取り専用</br>システム生成 | |
| **休暇タイプ エンティティ**</br>mshr_essleaverequestentityid</br>*GUID* | システム生成 | システムで生成する、休暇申請を一意に識別する GUID 値です。 |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**応答**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
