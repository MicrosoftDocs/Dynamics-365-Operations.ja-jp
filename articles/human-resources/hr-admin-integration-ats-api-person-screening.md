---
title: 個人の審査
description: この記事では、Dynamics 365 Human Resources の人物の選考エンティティについて説明します。
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
ms.openlocfilehash: e9b2bbda8f8191f592462f4fbd1902e7274cf7f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907643"
---
# <a name="person-screening"></a>個人の審査


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の人物の選考エンティティについて説明します。

物理名 : mshr_hcmpersonscreeningentity

## <a name="description"></a>説明

このエンティティは、候補者が合格した、または採用に合格する必要がある選考を表します。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **人物の選考エンティティ ID**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | 読み取り専用<br>必須<br>システム生成 | 人物の選考レコードの一意の基本識別子です。 |
| **関係者番号**<br>mshr_partynumber<br>*文字列* | 読み取り/書き込み<br>必須 | 候補者に関連付けられている関係者 (人物) 番号です。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_dirpersonentity の mshr_dirpersonentityid | システムが生成する、当事者 (個人) エンティティ レコードの識別子です。 |
| **選考タイプ ID**<br>mshr_screeningtypeid<br>*文字列* | 読み取り/書き込み<br>必須<br>外部キー : 選考タイプ | Human Resources で定義されている選考タイプの ID です。 |
| **選考タイプ ID 値**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー : mshr_hcmscreeningtypeentity の mshr_hcmscreeningtypeentityid | 関連するエンティティの選考タイプ レコーに向けてシステムが生成して識別子です。 |
| **期日**<br>mshr_requiredby<br>*Datetime* | 読み取り/書き込み<br>オプション | 選考を完了する必要がある期日です。 |
| **状態**<br>mshr_status<br>*mshr_hcmcompletionstatus オプション セット*<br>読み取り/書き込み<br>必須 | 候補者の選考の状態を指定します。 |
| **完了日**<br>mshr_completeddate<br>*Datetime* | 読み取り/書き込み<br>オプション | 選考が完了した日付です。 |
| **摘要**<br>mshr_note<br>*文字列* | 読み取り/書き込み<br>オプション | 採用担当者や採用マネージャーが使用するメモです。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
