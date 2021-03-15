---
title: 評価レベル
description: このトピックでは、Dynamics 365 Human Resources の評価レベルのエンティティについて説明します。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125260"
---
# <a name="rating-level"></a>評価レベル

このトピックでは、Dynamics 365 Human Resources の評価レベルのエンティティについて説明します。

物理名 : mshr_hcmratinglevelentity

## <a name="description"></a>説明

このエンティティは、スキルの評価レベルを提供します。 評価レベルは、すべての法人に適用されます。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **評価レベル エンティティ ID**<br>mshr_hcmratinglevelentityid<br>*GUID* | 読み取り専用<br>必須<br>システム生成 | システムが生成した、レベルの一意識別子です。 |
| **評価レベル ID**<br>mshr_ratinglevelid<br>*文字列* | 読み取り/書き込み<br>必須 | ユーザーが読取り可能なレベルの一意識別子です。 |
| **評価モデル ID**<br>mshr_ratingmodelid<br>*文字列* | 読み取り/書き込み<br>必須 | 評価レベルが属する評価モデルです。 |
| **評価モデル エンティティ ID**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmratingmodelentity の mshr_hcmratingmodelentityid | システムが生成する、評価レベルが属する評価モデルの識別子です。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>必須 | 評価レベルの説明です。 |
| **係数**<br>mshr_factor<br>*整数* | 読み取り/書き込み<br>必須 | 評価レベルの係数です。 評価レベルの異なる数の項目を比較する際には、スコアを正規化するためにこの係数が使用されます。 値は 0 (ゼロ) から 9 までの間の整数値である必要があります。 |
| **メモ**<br>mshr_note<br>*文字列* | 読み取り/書き込み<br>オプション | 評価レベルに関連付けられているメモです。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 読み取り専用<br>必須 | エンティティ レコードの識別子として使用されるフィールドです。 評価レベル ID と評価モデル ID の組み合わせです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]