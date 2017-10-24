--- 
title: "作業セルで材料が利用可能な場合にプロセスかんばん作業を準備"
description: "このタスクでは、作業セルですべての材料が利用可能な場合にプロセスかんばん作業を準備することに焦点をあてます。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62f3f71cc5e47f0fb027211a911e61673ca2e375
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a>作業セルで材料が利用可能な場合にプロセスかんばん作業を準備

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、作業セルですべての材料が利用可能な場合にプロセスかんばん作業を準備することに焦点をあてます。 このタスクの作成に使用するデモ データの会社は USMF です。 このタスクは、機械オペレーターを対象としています。

1. [プロセス ジョブのかんばんボード] に移動します。
2. [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
    * 作業セル 1250 を選択し、[OK] をクリックします  
4. 一覧で行 4 を選択します。
    * クリーンなデモ会社では、4 行目のかんばん「000329」はまだ完了していない最初のジョブです。  
5. [ピッキング リスト] セクションの展開を切り替えます。
    * 供給のステータスがピッキング リストのすべての品目に対して使用できることを確認します。  
    * 複数のジョブが選択されている場合、ピッキング リストには、選択したジョブに必要なすべての品目の合計が表示されます。  
6. [準備] をクリックします。
    * 準備プロセスは完了です。 ピッキング リストのすべての行に関連する選択済みのチェック ボックスは、供給のステータスがピッキングされていることを示します。  


