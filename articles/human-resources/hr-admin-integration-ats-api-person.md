---
title: 名前
description: このトピックでは、Dynamics 365 Human Resources の人物エンティティについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 448be7ada2825d3cdd846650821579d1d6797d00
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800360"
---
# <a name="person"></a>名前

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物エンティティについて説明します。

物理名 : mshr_dirpersonentity

### <a name="description"></a>説明

このエンティティは、候補者である人物の個人情報を提供します。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **人物のエンティティ ID**<br>mshr_dirpersonentityid<br>*GUID* | 読み取り専用<br>必須<br>システム生成 | システムが生成した、エンティティ レコードの一意識別子です。 |
| **当事者番号**<br>mshr_partynumber<br>*文字列* | 読み取り専用<br>必須<br>システム生成 | ユーザーが可読な、当該人物のシステムが生成する一意識別子です。  |
| **氏名**<br>mshr_name<br>*文字列* | 読み取り専用<br>必須 | このフィールド値は、**名前順序の表示方法** フィールドで定義された順序の、<姓、ミドルネーム、敬称、名>を連結したものです。 |
| **名前のエイリアス**<br>mshr_namealias<br>*文字列* | 読み取り/書き込み<br>オプション | 人物に指定できる名前のエイリアスです。 |
| **呼称**<br>mshr_knownas<br>*文字列* | 読み取り/書き込み<br>オプション | 別の名前で認知されている場合に、使用される可能性があります。 |
| **言語 ID**<br>mshr_languageid<br>*文字列* | 読み取り/書き込み<br>オプション | ISO 639-1 形式で定義された、人物の第一言語の言語 ID です。 |
| **アドレス帳**<br>mshr_addressbooks<br>*文字列* | 読み取り/書き込み<br>オプション | この人物が割り当てられるアドレス帳です。 組織で設定されているアドレス帳は、mshr_diraddressbooksentity エンティティに一覧表示されます。 |
| **記念日**<br>mshr_anniversaryday<br>*Int* | 読み取り/書き込み<br>オプション | 人物の記念日の日付です。 |
| **記念日 (月)**<br>mshr_anniversarymonth<br>*mshr_monthsofyear オプション セット* | 読み取り/書き込み<br>オプション | 人物の記念日が属する月です。 |
| **記念日 (年)**<br>mshr_anniversaryyear<br>*Int* | 読み取り/書き込み<br>オプション | 人物の記念日の年です。 |
| **生年月日**<br>mshr_birthday<br>*Int* | 読み取り/書き込み<br>オプション | 人物の生年月日です。 |
| **生年月日 (月)**<br>mshr_birthmonth<br>*mshr_monthsofyear オプション セット* | 読み取り/書き込み<br>オプション | 人物の生年月日の月です。 |
| **生年月日 (年)**<br>mshr_birthyear<br>*Int* | 読み取り/書き込み<br>オプション | 人物の生年月日の年です。 |
| **子の名前**<br>mshr_childrennames<br>*文字列* | 読み取り/書き込み<br>オプション | ユーザーのコドモの名前の文字列です。 区切りは必要ありません。 |
| **種類**<br>mshr_gender<br>*mshr_hcmpersongender オプション セット* | 読み取り/書き込み<br>オプション | 人物の性別です。 |
| **趣味**<br>mshr_hobbies<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の趣味です。 |
| **イニシャル**<br>mshr_initials<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の名前のイニシャルです。 |
| **配偶者の有無**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus オプション セット* | 読み取り/書き込み<br>オプション | 個人の婚姻状態です。 |
| **名のふりがな**<br>mshr_phoneticfirstname<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の名のふりがなです。 |
| **姓のふりがな**<br>mshr_phoneticlastname<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の姓のふりがなです。 |
| **ミドルネームのふりがな**<br>mshr_phoneticmiddlename<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の姓のふりがなです。 |
| **個人の敬称**<br>mshr_personalsuffix<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の敬称です。 mshr_type が Suffix (200000001) となっている mshr_dirnameaffixentity エンティティで有効な値です。 |
| **個人の肩書き**<br>mshr_personaltitle<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の肩書きです。 mshr_type が Title (200000000) となっている mshr_dirnameaffixentity エンティティで有効な値です。
| **職務の接尾辞**<br>mshr_professionalsuffix<br>*文字列* | 読み取り/書き込み<br>オプション | 職務の接尾辞です。 |
| **職務の肩書き**<br>mshr_professionaltitle<br>*文字列* | 読み取り/書き込み<br>オプション | 職務の肩書きです。 |
| **完全な基本住所**<br>mshr_fullprimaryaddress<br>*文字列* | 読み取り/書き込み<br>オプション | 担当者の完全な基本住所、基本住所フィールドの連結です。 |
| **住所 (市区町村)**<br>mshr_addresscity<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の市区町です。 mshr_logisticsaddresscityentity エンティティで設定します。 |
| **住所 国 地域**<br>mshr_addresscountryregionid<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の国/地域です。 mshr_logisticsaddresscountryregionentity エンティティ内の有効な値です。 |
| **住所 国 地域 ISO コード**<br>mshr_addresscountryregionisocode<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の国の ISO コードです。 |
| **住所 国**<br>mshr_addresscounty<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の国です。 mshr_logisticsaddresscountyentity エンティティで設定します。 |
| **住所 地域 名称**<br>mshr_addressdistrictname<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の地域です。 mshr_logisticsaddressdistrictentity エンティティで設定します。 |
| **住所の緯度**<br>mshr_addresslatitude<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の緯度です。 |
| **住所 場所 ID**<br>mshr_addresslocationid<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の場所の一意識別子です。 mshr_logisticspostaladdresslocationcdsentity エンティティ内の有効な値です。 |
| **住所の場所ロール**<br>mshr_addresslocationroles<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の場所ロールです。 mshr_logisticslocationrolecdsentity エンティティで設定します。 |
| **住所の経度**<br>mshr_addresslongitude<br>*文字列* |  読み取り/書き込み<br>オプション | 人物の基本住所の経度です。 |
| **住所の都道府県州**<br>mshr_addressstate<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の住所の都道府県州です。 mshr_logisticsaddressstateentity エンティティで設定します。 |
| **住所の番地**<br>mshr_addressstreet<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の番地です。 |
| **住所の有効なフォーム**<br>mshr_addressvalidfrom<br>*日* | 読み取り/書き込み<br>オプション | 本人の基本住所が有効な日付です。 |
| **住所の有効期限**<br>mshr_addressvalidto<br>*日* | 読み取り/書き込み<br>オプション | 本人の基本住所の有効期限日です。 |
| **住所の郵便番号**<br>mshr_addresszipcode<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所の郵便番号です。 mshr_logisticsaddresspostalcodeentity エンティティで設定します。 |
| **住所は非公開です**<br>mshr_addressisprivate<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | ユーザーの基本住所を組織内の他のユーザーと共有するかどうかを決定します。 |
| **住所の説明**<br>mshr_addressdescription<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本住所に対する説明です。 |
| **基本連絡先のメールアドレス**<br>mshr_primarycontactemail<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本電子メール アドレスです。 |
| **基本連絡先のメールアドレスの説明**<br>mshr_primarycontactemaildescription<br>*文字列* | 読み取り/書き込み<br>オプション | 基本メール アドレスについての説明です。 |
| **基本連絡先のメールアドレスが IM である**<br>mshr_primarycontactemailisim<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | 基本メール アドレスをインスタント メッセージに使用できるかどうかを指定します。 |
| **基本連絡先メールアドレスの用途**<br>mshr_primarycontactemailpurpose<br>*文字列* | 読み取り/書き込み<br>オプション | 基本メール アドレスの目的です。 mshr_logisticslocationroleentity エンティティで設定します。 |
| **基本連絡先の Fax**<br>mshr_primarycontactfax<br>*文字列* | 読み取り/書き込み<br>オプション | 基本 FAX 番号です。 |
| **基本連絡先の Fax の説明**<br>mshr_primarycontactfaxdescription<br>*文字列* | 読み取り/書き込み<br>オプション | 基本 Fax 番号についての説明です。 |
| **基本連絡先の Fax の内線番号**<br>mshr_primarycontactfaxextension<br>*文字列* | 読み取り/書き込み<br>オプション | 基本FAX番号の内線番号です。 |
| **基本連絡先 FAX の用途**<br>mshr_primarycontactfaxpurpose<br>*文字列* | 読み取り/書き込み<br>オプション | 基本FAX番号の内線番号の使用目的です。 mshr_logisticslocationroleentity エンティティで設定します。
| **基本連絡先の電話番号**<br>mshr_primarycontactphone<br>*文字列* | 読み取り/書き込み<br>オプション | 代表電話番号です。 |
| **基本連絡先の電話についての説明**<br>mshr_primarycontactphonedescription<br>*文字列* | 読み取り/書き込み<br>オプション | 基本電話番号についての説明です。 |
| **基本連絡先電話番号の内線番号**<br>mshr_primarycontactphoneextension<br>*文字列* | 読み取り/書き込み<br>オプション | 基本電話番号の内線番号です。 |
| **基本連絡先の電話が携帯電話**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | 基本の電話番号が携帯電話番号かどうかを指定します。 |
| **基本連絡先電話の用途**<br>mshr_primarycontactphonepurpose<br>*文字列* | 読み取り/書き込み<br>オプション | 基本電話番号の内線番号の使用目的です。 mshr_logisticslocationroleentity エンティティで設定します。 |
| **基本連絡先のテレックス**<br>mshr_primarycontacttelex<br>*文字列* | 読み取り/書き込み<br>オプション | 基本テレックス番号です。 |
| **基本連絡先のテレックスの説明**<br>mshr_primarycontacttelexdescription<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本テレックス番号についての説明です。 |
| **基本連絡先テレックスの用途**<br>mshr_primarycontacttelexpurpose<br>*文字列* | 読み取り/書き込み<br>オプション | その人物の基本テレックス番号の目的です。 mshr_logisticslocationroleentity エンティティで設定します。 |
| **基本連絡先 URL**<br>mshr_primarycontacturl<br>*文字列* | 読み取り/書き込み<br>オプション | 基本 URL です。 |
| **基本連絡先の URL の説明**<br>mshr_primarycontacturldescription<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 URL に対する説明です。 |
| **基本連絡先 URL の用途**<br>mshr_primarycontacturldescription<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 URL の使用目的です。 mshr_logisticslocationroleentity エンティティで設定します。 |
| **基本連絡先の Facebook**<br>mshr_primarycontactfacebook<br>*文字列* | 読み取り/書き込み<br>オプション | 基本 Facebook アカウントです。 ユーザー ID で識別します。 |
| **基本連絡先の Facebook の説明**<br>mshr_primarycontactfacebookdescription<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 Facebook アカウントに対する説明です。 |
| **基本連絡先 Facebookが非公開である**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | 基本 Facebook アカウントを他のユーザーが表示できるかどうかを指定します。 |
| **基本連絡先 Facebook の用途**<br>mshr_primarycontactfacebookpurpose<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 Facebook アカウントの使用目的です。 mshr_logisticslocationroleentity エンティティで設定します。 |
| **基本連絡先 LinkedIn**<br>mshr_primarycontactlinkedin<br>*文字列* | 読み取り/書き込み<br>オプション | 基本 LinkedIn アカウント。 ユーザー名 で識別します。 |
| **、基本連絡先 LinkedIn についての説明**<br>mshr_primarycontactlinkedindescription<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 LinkedIn アカウントに対する説明です。 |
| **基本連絡先の LinkedIn は非公開です**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | 人物の基本 LinkedIn アカウントを他のユーザーと共有するかどうかを決定します。 |
| **基本連絡先 LinkedIn の用途**<br>mshr_primarycontactlinkedinpurpose<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 LinkedIn アカウントの使用目的です。 mshr_logisticslocationroleentity エンティティで設定します。 |
| **基本連絡先 Twitter**<br>mshr_primarycontacttwitter<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 Twitter アカウントです。 @username で識別します。 |
| **基本連絡先 Twitter についての説明**<br>mshr_primarycontacttwitterdescription<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 Twitter アカウントに対する説明です。 |
| **基本連絡先の Twitter は非公開です**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | 人物の基本 Twitter アカウントを他のユーザーと共有するかどうかを決定します。 |
| **基本連絡先 Twitter の用途**<br>mshr_primarycontacttwitterpurpose<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の基本 Twitter アカウントの使用目的です。 mshr_logisticslocationroleentity エンティティで設定します。 |
| **当事者 タイプ**<br>mshr_partytype<br>*文字列* | 読み取り/書き込み<br>オプション | 人物のの関係者タイプです。 常に候補者の **人物** が選び出されます。 |
| **名前シーケンスの表示順序**<br>mshr_namesequencedisplayas<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の名前プロパティを連結して Name (mshr_name) プロパティ値を形成する順序です。 |
| **名**<br>mshr_firstname<br>*文字列* | 読み取り/書き込み<br>必須 | 人物の名です。 |
| **ミドル ネーム**<br>mshr_middlename<br>*文字列* | 読み取り/書き込み<br>オプション | 人物のミドルネームです。 |
| **姓の接頭辞**<br>mshr_lastnameprefix<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の姓の敬称です。 |
| **姓**<br>mshr_lastname<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の姓です。 |
| **電子場所 ID**<br>mshr_electroniclocationid<br>*文字列* | 読み取り/書き込み<br>オプション | 人物の電子的な場所の ID です。 |
| **住所のタイム ゾーン**<br>mshr_addresstimezone<br>*Int* | 読み取り/書き込み<br>オプション | 人物の基本住所のタイムゾーンです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]