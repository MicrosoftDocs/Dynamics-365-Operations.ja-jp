---
title: 将来のライフ イベントのコンフィギュレーション
description: Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d52e91e7b050027485b3536f40f6ad80afd90de8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056735"
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