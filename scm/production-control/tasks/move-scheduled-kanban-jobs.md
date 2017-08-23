--- 
title: "スケジュール済みかんばん作業の移動"
description: "この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。"
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5f101a097643fa027a667b9d6577fbe5d24ecd27
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="move-scheduled-kanban-jobs"></a>スケジュール済みかんばん作業の移動

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、かんばんを処理する作業現場の監督または生産計画担当者を対象としています。


## <a name="select-scheduled-kanban-jobs"></a>スケジュール済みかんばんジョブを選択する
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. !MtCMR! [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。 áçêìõý !
3. Markér den valgte række på listen.
    * 作業セル 1250 を選択します。  
4. Klik på Select.
5. Vælg 'Planlagt' i feltet Display job status.
    * これは、スケジュール済のかんばんジョブのみを表示するジョブ一覧をフィルタ処理します。  

## <a name="move-kanban-jobs-to-a-different-period"></a>別の期間へのジョブの移動
1. Find og vælg den ønskede post på listen.
    * たとえば、[計画期間] フィールドにある 2012 年 12 月 20 日にスケジュールされたジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。 その後、ジョブを以前の期間に移動します。  
2. Klik på Previous period.
3. Klik på End.
    * これにより、前の期間内にある最後のジョブとしてジョブ リストの最後にジョブが移動されます。  
4. Find og vælg den ønskede post på listen.
    * たとえば、[計画期間] フィールドにある 2012 年 12 月 18 日にスケジュールされたジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。 その後、ジョブを次の期間に移動します。  
5. Klik på Next period.
6. Klik på Start.
    * これにより、前の期間内にある最初のジョブとしてジョブ リストの最初にジョブが移動されます。  

## <a name="task-move-a-job-within-a-period"></a>タスク: 期間内へのジョブの移動
1. Find og vælg den ønskede post på listen.
    * たとえば、[計画期間] フィールドにある 2012 年 12 月 19 日にスケジュールされた 2 番目のジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。 その後、計画期間内にジョブを移動します。  
2. Klik på Forward.
    * 一覧でジョブが 1 行下へ移動することを確認します。  
3. Klik på Backward.
    * 一覧でジョブが 1 行上へ移動することを確認します。  


