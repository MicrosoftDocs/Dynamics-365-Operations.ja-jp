---
title: MyLeaveRequests の概要
description: Microsoft Dynamics 365 Human Resources の MyLeaveRequests エンティティは、休暇申請の一覧を提供します。
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717058"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests の概要


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
