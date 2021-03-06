---
title: MyLeaveRequests の概要
description: Microsoft Dynamics 365 Human Resourcesの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054959"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests の概要

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]