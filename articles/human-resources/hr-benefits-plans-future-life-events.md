---
title: 将来のライフ イベントのコンフィギュレーション
description: このトピックでは、Dynamics 365 Human Resources で将来のライフ イベントをスケジュールする方法について説明します。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 441ccc478f78f76b80ac9138dc62592634f005bd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693202"
---
# <a name="configure-future-life-events"></a>将来のライフ イベントのコンフィギュレーション

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。

1. **給付金管理** ワーク スペースの **設定** で、**将来のライフ イベント** を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | ライフ イベント日付 | システムによって登録期間中に、この日付までのすべてのイベントが処理されます。 |
   | ライフ イベントのログが記録されます | ライフ イベントが記録される日時。 |
   | ログ タイプ | アクションが次のいずれかであるかどうかを示します。</br></br>- **更新** – ライフ イベントを追跡している既存のレコードへの変更</br></br>- **挿入** – 新しいライフ イベント レコードを作成 |
   | ライフ イベント タイプ ID | ライフ イベント タイプの固有識別子。 |
   | ライフ イベント タイプ | 従業員の給付金登録を更新する触媒。 詳細については、ライフ イベント トリガーのセクションを参照してください。 |
   | ステータス | ライフ イベント処理されているかどうか。 |
   | ライン | 将来のライフ イベントの行番号。 |

4. **保存** を選択します。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
