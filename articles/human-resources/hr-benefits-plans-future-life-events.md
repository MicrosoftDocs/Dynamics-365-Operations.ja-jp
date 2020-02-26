---
title: 将来のライフ イベントのコンフィギュレーション
description: Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009689"
---
# <a name="configure-future-life-events"></a>将来のライフ イベントのコンフィギュレーション

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。

1. **給付金管理**ワーク スペースの**設定**で、**将来のライフ イベント**を選択します。

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
