---
title: MyLeaveRequests の概要
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009671"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests の概要

Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。

## <a name="key"></a>キー

  | プロパティ名 | データ タイプ |
  |---------------|-----------|
  | dataAreaId    | 文字列    |
  | RequestId     | 文字列    |
  | LeaveType     | 文字列    |
  | LeaveDate     | 日      |
  
## <a name="properties"></a>プロパティ

  | プロパティ名     | データ タイプ | 必須 |
  |-------------------|-----------|----------|
  | dataAreaId        | 文字列    | x        |
  | RequestId         | 文字列    | x        |
  | LeaveType         | 文字列    | x        |
  | LeaveDate         | 日      | x        |
  | ReasonCodeId      | 文字列    |          |
  | PersonnelNumber   | 文字列    | x        |
  | RequestDate       | 日      | x        |
  | コメント           | 文字列    |          |
  | ステータス            | 列挙      | x        |
  | 量            | 実績      |          |
  | HalfDayDefinition | 列挙      |          |

## <a name="actions"></a>アクション

 | アクション名                               | 説明                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [送信](hr-developer-api-myleaverequests-submit.md)   | ワークフローで処理される要求を送信します。 |

## <a name="see-also"></a>参照

- [休暇申請をワークフローに送信する](hr-developer-api-myleaverequests-submit.md)
- [認証](hr-developer-api-authentication.md)