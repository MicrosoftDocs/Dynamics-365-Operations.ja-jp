---
title: 人物の識別番号
description: このトピックでは、Dynamics 365 Human Resources の人物の識別番号エンティティについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0991f5b2e17e64e23f78b346c451f7c43bc20378
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067154"
---
# <a name="person-identification-number"></a>人物の識別番号


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物の識別番号エンティティについて説明します。

物理名 : mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>説明

このエンティティは、候補者の識別番号について説明します。 これにより、API の使用者は社会保障番号やパスポート番号のような識別番号を候補者レコードに書き込む必要があります。 ID番号は従業員レコードに表示されますが、候補者レコードには表示されません。 統合されたアプリケーションで Human Resources データベースに値を書き込むできますが、Human Resources には候補者の作業者レコードが作成されるまでその番号は表示されません。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **個人識別番号 エンティティID**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | 読み取り専用<br>必須<br>システム生成 | 人物の識別番号レコードの一意の基本識別子です。 |
| **エントリ タイプ**<br>mshr_entrytype<br>*文字列* | 読み取り/書き込み<br>オプション | 識別番号のエントリ タイプを参照する自由形式の値です。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>オプション | ID 番号の説明。 |
| **有効期限**<br>mshr_expirationdate<br>*Datetime* | 読み取り/書き込み<br>オプション | 識別番号または関連するドキュメントの期限が切れる日付です。 |
| **基本**<br>mshr_isprimary<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | 識別番号が、この識別タイプの人物の基本レコードであるかどうかを定義します。 |
| **ID 番号**<br>mshr_identificationnumber<br>*文字列* | 読み取り/書き込み<br>必須 | ID 番号。 |
| **当事者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 | 識別番号を所有する当事者 (人物) の識別子です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity エンティティの mshr_dirpersonentityid | 当事者 (人物) の一意識別子です。 |
| **識別タイプ ID**<br>mshr_identificationtypeid<br>*文字列* | 読み取り/書き込み<br>必須 | 識別番号のタイプです。 |
| **識別タイプ ID 値**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmidentificationtypeentity エンティティの mshr_hcmidentificationtypeentityid | システムが生成する識別タイプの一意識別子です。 |
| **発行機関 ID**<br>mshr_issuingagencyid<br>*文字列* | 読み取り/書き込み<br>オプション | 識別番号を発行する機関または組織です。 |
| **発行機関 ID 値**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | 読み取り専用<br>オプション<br>外部キー : mshr_hcmissuingagencyentity エンティティの mshr_hcmissuingagencyentityid | システムが生成する 識別番号を発行する機関の一意の識別子です。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | エンティティ レコードの識別子として使用されるフィールドです。 関係者番号、識別タイプ ID、識別番号の組み合わせです。 |
| **発行日**<br>mshr_issuedate<br>*日* | 読み取り/書き込み<br>オプション | 識別番号が発行された日付です。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
