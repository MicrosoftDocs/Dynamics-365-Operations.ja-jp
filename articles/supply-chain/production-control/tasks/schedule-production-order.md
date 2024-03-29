---
title: 製造オーダーのスケジュール
description: この手順では、製造オーダーのスケジュール方法を示します。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43d183764def1b1bea7bbe140c25e0eec0b692b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580579"
---
# <a name="schedule-a-production-order"></a>製造オーダーのスケジュール

[!include [banner](../../includes/banner.md)]

この手順では、製造オーダーのスケジュール方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 これは、製造オーダーのライフ サイクルを説明する 7 つの手順の 3 番目です。


## <a name="schedule-a-production-order"></a>製造オーダーのスケジュール
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
    * [見積済] 状態の製造オーダーを選択します。  
2. [アクション ペイン] で、[スケジュール] をクリックします。
3. [ジョブのスケジュール設定] をクリックします。
    * スケジューリングのパラメーターはこのページで設定します。 特定のユーザーまたはすべてのユーザー用のパラメータを設定できます。  
4. [スケジューリング指示] フィールドで、「今日からフォワード」 をクリックします。
5. [スケジューリングの日付] フィールドに日付を入力します。
6. [有限能力] チェック ボックスを選択またはクリアします。
7. [有限原材料] チェック ボックスをオンまたはオフにします。
8. [OK] をクリックします。

## <a name="view-the-scheduling-results"></a>スケジューリング結果の表示
1. アクション ウィンドウで、[製造オーダー] をクリックします。
2. [すべてのジョブ] をクリックします。
    * このページでは、生成したスケジュール済ジョブを表示します。  
3. [スケジューリング] セクションを展開または折りたたみます。
    * [スケジューリング クイック タブ] で、予定日時を表示できます。  
4. [照会] をクリックします。
5. [最大能力負荷] をクリックします。
    * [最大能力負荷] ページは、ジョブのスケジューリングで予約されている時間数、リソースで現在予約済の合計時間数、リソースのジョブのスケジューリングで使用できる残り時間数を表示します。  
6. ページを閉じます。
7. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]