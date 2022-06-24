---
title: 休暇タイプ
description: この記事では、Dynamics 365 Human Resources における休暇タイプ エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893789"
---
# <a name="leave-type"></a>休暇タイプ


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の休暇タイプ エンティティについて説明します。

### <a name="description"></a>Description

このエンティティは、特定の休暇タイプの情報を提供します。

物理名 : mshr_essleavetypeentity。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **休暇タイプ ID**</br>mshr_leavetypeid</br>*文字列* | 読み取り専用 | 休暇タイプ ID です。 |
| **説明**</br>mshr_description</br>*文字列* | 読み取り専用 | 休暇タイプの説明です。 |
| **カテゴリ**</br>mshr_category</br>*mshr_LeaveTypeCategory オプション セット* | 読み取り専用 | 休暇タイプ カテゴリです。 |
| **理由コードが必要です**</br>mshr_isreasoncoderequired</br>*mshr_NoYes オプション セット* | 読み取り専用 | 休暇タイプに理由コードが必要な場合に定義します。 |
| **休暇単位**</br>mshr_leaveamountunit</br>*mshr_LeaveAmountUnit オプション セット* | 読み取り専用 | この休暇タイプの単位です。 |
| **半日を有効にする**</br>mshr_enablehalfdaydefinition</br>*mshr_NoYes オプション セット* | 休暇タイプに対して半日を有効にした場合に定義します。 |
| **データ領域 ID**</br>mshr_dataareaid_id</br>*文字列* | 読み取り専用 | 法人 (会社) を指定します。 |
| **休暇タイプ エンティティ**</br>mshr_essleavetypeentityid</br>*GUID* | システム生成 | システムで生成する、休暇タイプを一意に識別する GUID 値です。 |

## <a name="example-query"></a>クエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**応答**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
