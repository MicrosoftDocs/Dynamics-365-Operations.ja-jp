---
title: 個人の審査
description: このトピックでは、Dynamics 365 Human Resources の人物の選考エンティティについて説明します。
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125380"
---
# <a name="person-screening"></a>個人の審査

このトピックでは、Dynamics 365 Human Resources の人物の選考エンティティについて説明します。

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

