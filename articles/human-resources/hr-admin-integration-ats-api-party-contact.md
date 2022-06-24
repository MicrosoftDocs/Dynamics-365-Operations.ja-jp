---
title: 関係者の連絡先
description: この記事では、Dynamics 365 Human Resources の関係者の連絡先エンティティについて説明します。
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
ms.openlocfilehash: f10bb89757419bcb29bfa5a4f44d30a38f41dfb0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909878"
---
# <a name="party-contact"></a>関係者の連絡先


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の関係者の連絡先エンティティについて説明します。

物理名 : mshr_dirpartycontactentities

## <a name="description"></a>説明

このエンティティは、電話、電子メール、ソーシャル メディア アカウントなど、候補者の連絡先情報を表します。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **当事者連絡先エンティティ ID**<br>mshr_dirpartycontactentityid<br>*文字列* | 読み取り専用<br>必須 | システムが生成した、エンティティ レコードの一意識別子です。 |
| **関係者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 | 関連付けられている当事者 (人物) レコードの ID です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity の mshr_dirpersonentityid | システムが生成する、当事者 (個人) エンティティ レコードの識別子です。 |
| **場所 ID**<br>mshr_locationid<br>*文字列* | 読み取り/書き込み<br>必須 | 住所レコードの場所 ID です。 mshr_logisticspostaladdresslocationcdsentity エンティティ内の設定をします。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>必須 | 連絡先の詳細についての説明です。 |
| **種類**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype オプション セット* | 読み取り/書き込み<br>必須 | 連絡先の詳細タイプです。 |
| **国/地域コード**<br>mshr_countryregioncode<br>*文字列* | 読み取り/書き込み<br>オプション | 住所の国または地域。 |
| **ロケーター**<br>mshr_locator<br>*文字列* | 読み取り/書き込み<br>オプション | 連絡先の詳細です。 たとえば、タイプが **メール アドレス** の場合 、このフィールドには候補者のメール アドレスが表示されます。 |
| **ロケーターの拡張機能**<br>mshr_locatorextension<br>*文字列* | 読み取り/書き込み<br>オプション | ロケーターの拡張機能です。 たとえば、タイプが **電話** の 場合 、このプロパティには内線電話番号が含まれます。 |
| **はモバイルです**<br>mshr_ismobile<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>必須 | 電話が携帯電話番号かどうかを指定します。 |
| **はインスタント メッセージです**<br>mshr_isinstantmessage<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>必須 | 電話でインスタント メッセージが有効かどうかを指定します。 |
| **基本**<br>mshr_isprimary<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>必須 | 連絡先タイプの基本連絡先を決定します。 連絡先タイプごとに基本レコードを1件だけ作成する必要があります。 |
| **は非公開です**<br>mshr_isprivate<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>必須 | この住所が個人のプライベート アドレスかどうかを識別します。 |
| **使用方法**<br>mshr_purpose<br>*文字列* | 読み取り/書き込み<br>オプション | 連絡先詳細の連絡先/ロールについての説明です。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | エンティティ レコードの基本識別子として使用されるフィールドです。 関係者番号、タイプ、説明、ロケーターの組み合わせ。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
