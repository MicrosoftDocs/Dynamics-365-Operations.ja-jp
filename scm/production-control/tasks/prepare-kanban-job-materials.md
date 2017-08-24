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
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4c52a2f226b079b404eab53e01b3025647633d04
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

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


