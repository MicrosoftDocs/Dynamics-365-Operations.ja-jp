---
title: 氏名の履歴
description: このトピックでは、Dynamics 365 Human Resources における氏名の履歴エンティティに対するクエリの詳細と例を示します。
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
ms.openlocfilehash: d87803b6ae0ada3ed2de6e4e7da5ffa57bf22eec
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064844"
---
# <a name="person-name-history"></a>氏名の履歴


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の氏名の履歴エンティティについて説明します。

物理名: mshr_dirpersonnamehistoricalentity。

### <a name="description"></a>説明

このエンティティは、特定の人物の氏名の履歴に関する情報を提供します。

> [!IMPORTANT] 
> **FirstName**、**MiddleName**、**LastName**、**NameValidFrom**、および **NameValidTo** フィールドは、給与従業員エンティティでは使用できなくなりました。 これらは、このエンティティをバックアップするデータソースが 1 つだけであることを保証する目的で削除されています。

## <a name="properties"></a>プロパティ

| プロパティ</br>**現物名**</br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **名**</br>mshr_firstname</br>*文字列* | 読み取り専用 | 名です。 |
| **姓の接頭語**</br>mshr_lastnameprefix</br>*文字列*) | 読み取り専用 | 姓の接頭辞です。 |
| **姓**</br>mshr_lastname</br>*文字列*) | 読み取り専用 | 姓です。 |
| **ミドル ネーム**</br>mshr_middlename</br>*文字列*) | 読み取り専用 | ミドル ネームです。 |
| **失効日**</br>mshr_validto</br>*文字列*) | 読み取り専用 | 名前が有効な日付の期限。 |
| **当事者番号**</br>mshr_partynumber</br>*文字列* | 読み取り専用 | ユーザーが可読な、当該人物のシステムが生成する一意識別子です。 |
| **基本フィールド**</br>mshr_primaryfield</br>*文字列* | 読み取り専用 | レコードの一意識別子です。 |
| **人物名履歴のエンティティ ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | システム生成 | レコードを一意に識別するための、システムが生成したグローバルに一意な識別子 (GUID) の値です。 |

## <a name="relations"></a>リレーション

| プロパティ値 | 関連するエンティティ | ナビゲーション プロパティ | コレクション タイプ |
| --- | --- | --- | --- |
| 該当なし | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | 該当なし | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>給与従業員のクエリの例

**申請**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**応答**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>参照

[給与統合 API の概要](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
