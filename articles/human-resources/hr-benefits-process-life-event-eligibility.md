---
title: ライフ イベントの適格性を処理
description: この記事では、ライフ イベント適格性の処理を実行する方法について説明します。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20b458e67b6504ca1c3efce6b40d1cea4faa7193
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058515"
---
# <a name="process-life-event-eligibility"></a>ライフ イベントの適格性を処理

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、ライフ イベント適格性の処理を実行する方法について説明します。

1. **給付金管理** ワークスペースにて、**処理** の下の **ライフ イベントの適格性処理** を選択します。

2. **ライフ イベントの適格性処理を実行** ダイアログ ボックスで、次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **登録期間** | ライフ イベントの適格性を処理する登録期間。 |

3. バックグラウンドで処理を実行する場合は、**バックグラウンドで実行** を選択し、次のタスクを実行します。

   1. 処理情報を入力します。

   2. 定期的なジョブを設定するには、**再実行** を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告** を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメータで処理が実行されます。

4. **OK** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]