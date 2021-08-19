---
title: 人物の証明書
description: このトピックでは、Dynamics 365 Human Resources の人物の証明書エンティティについて説明します。
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
ms.openlocfilehash: f74691d4f6593dc02931a037ecacb6314e28ea6d9ea5ab494581453bf8dfb31c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733567"
---
# <a name="person-certificate"></a>人物の証明書

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の人物の証明書エンティティについて説明します。

物理名 : mshr_hcmpersoncertificateentity

## <a name="description"></a>説明

このエンティティは、候補者の職業証明書を表します。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **人物の証明書エンティティ ID**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | 読み取り専用<br>必須 | システムが生成した、人物の証明書エンティティ レコードの一意識別子です。 |
| **当事者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 | 候補者の関係者 (人物) ID です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity の mshr_dirpersonentityid | システムが生成する、当事者 (個人) エンティティ レコードの識別子です。 |
| **証明書タイプ ID**<br>mshr_certificatetypeid<br>*文字列* | 読み取り/書き込み<br>必須 |  Human Resources で定義されている証明書タイプの ID です。 |
| **証明書タイプ ID 値**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmcertificatetypeentity の mshr_hcmcertificatetypeentityid | システムが生成する関連エンティティの証明書タイプの一意識別子です。 |
| **開始日**<br>mshr_startdate<br>*Datetime* | 読み取り/書き込み<br>必須 | 証明書が発行された日付です。 |
| **終了日**<br>mshr_enddate<br>*Datetime* | 読み取り/書き込み<br>オプション | 証明書が失効する日付です。 |
| **摘要**<br>mshr_notes<br>*文字列* | 読み取り/書き込み<br>オプション | 採用担当者や採用マネージャーが使用するメモです。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 |  エンティティ レコードの識別子として使用されるフィールドです。 関係者番号、証明書タイプ ID、開始日の組み合わせです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]