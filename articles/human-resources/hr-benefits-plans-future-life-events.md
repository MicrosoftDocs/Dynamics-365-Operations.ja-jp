---
title: 将来のライフ イベントのコンフィギュレーション
description: この記事では、Dynamics 365 Human Resources で将来のライフ イベントをスケジュールする方法について説明します。
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
ms.openlocfilehash: 2cb3ca03e0d9d7e5423a405f1eb0372e1c19588d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227988"
---
# <a name="configure-future-life-events"></a>将来のライフ イベントのコンフィギュレーション

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

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
   | Status | ライフ イベント処理されているかどうか。 |
   | 明細行 | 将来のライフ イベントの行番号。 |

4. **保存** を選択します。 

将来のライフ イベントを削除できます。 処理された将来のライフ イベントが削除された場合は、将来のレコードも削除されます。 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
