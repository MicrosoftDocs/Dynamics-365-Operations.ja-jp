---
title: 作業セルで材料が利用可能な場合にプロセスかんばん作業を準備
description: このタスクでは、作業セルですべての材料が利用可能な場合にプロセスかんばん作業を準備することに焦点をあてます。
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 011c542d360309fdeb539c85a68f2a5691022e37
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836160"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a>作業セルで材料が利用可能な場合にプロセスかんばん作業を準備

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

