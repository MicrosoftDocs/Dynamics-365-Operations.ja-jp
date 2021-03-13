---
title: 審査タイプ
description: このトピックでは、Dynamics 365 Human Resources の選考タイプ エンティティについて説明します。
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126173"
---
# <a name="screening-types"></a>審査タイプ

このトピックでは、Dynamics 365 Human Resources の選考タイプ エンティティについて説明します。

物理名 : mshr_hcmscreeningtypeentity

## <a name="description"></a>説明

このエンティティには、雇用前および継続的な従業員の選考プロセスに会社が設定した選考の種類が記載されています。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **選考タイプ エンティティ ID**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | 読み取り専用<br>必須<br>システム生成 | 人物の選考タイプ レコードの一意の基本識別子です。 |
| **選考タイプ ID**<br>mshr_screeningtypeid<br>*文字列* | 読み取り/書き込み<br>必須 | ユーザー定義の選考タイプ レコードの一意識別子です。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>必須 | 選考タイプの説明です。 |
| **頻度の単位**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit オプション セット* | 読み取り/書き込み<br>必須 | 割り当てられた人物に対して審査を完了しなければならない頻度を表します。 |
| **生成元**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom オプション セット* | 読み取り/書き込み<br>必須 | 頻度の値が [一時のみ] 以外の値である場合は、GenerateFrom 値により、次の選考イベントを計算する開始日が決定されます。 |
| **頻度の間隔**<br>mshr_frequencyinterval<br>*整数* | 読み取り/書き込み<br>必須 | 頻度の値が [一時のみ] 以外の値である場合は、各選考イベントの間隔を定義する必要があります。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
