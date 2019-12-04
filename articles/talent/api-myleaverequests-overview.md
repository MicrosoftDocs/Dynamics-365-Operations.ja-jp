---
title: MyLeaveRequests の概要
description: この記事では、MyLeaveRequests エンティティの参照資料を提供します。
author: gboyko
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: gboyko
ms.search.validFrom: 2019-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3bf2aa784d85882d657c1d0f00f1417534a89dc3
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833197"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests の概要

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talentの MyLeaveRequests エンティティは、現在のユーザーがエンティティを照会するときにアクセスできる要求にスコープされた (制限された)、システム内の休暇要求のリストを提供します。

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
 | [送信](api-myleaverequests-submit.md)   | ワークフローで処理される要求を送信します。 |

## <a name="see-also"></a>参照

[ワークフローへの休暇要求の送信](api-myleaverequests-submit.md)