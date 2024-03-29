---
title: スケジュール済みかんばん作業の移動
description: この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。
author: johanhoffmann
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c1b6ea92a1e3b16df6678030957c3fa407c15b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568018"
---
# <a name="move-scheduled-kanban-jobs"></a>スケジュール済みかんばん作業の移動

[!include [banner](../../includes/banner.md)]

この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、かんばんを処理する作業現場の監督または生産計画担当者を対象としています。

## <a name="select-scheduled-kanban-jobs"></a>スケジュール済みかんばん作業を選択します。 

1. **生産管理 > かんばん > かんばん作業スケジューリング** の順に移動します。 

2. **作業セル** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。 

3. 一覧で、選択された行をマークします。 
   - 作業セル 1250 を選択します。 
4. **選択** をクリックします。 

5. **ジョブ ステータスの表示** フィールドでは、**スケジュール済み** を選択します。 これは、スケジュール済のかんばんジョブのみを表示するジョブ一覧をフィルタ処理します。 

## <a name="move-kanban-jobs-to-a-different-period"></a>かんばん作業を別の期間へ移動します。 

1. 一覧で、目的のレコードを見つけ、選択します。 たとえば、**計画期間** フィールドにある 2012 年 12 月 20 日にスケジュールされたジョブなど、ジョブ ステータスが **計画済み** となっているジョブを選択します。 その後、ジョブを以前の期間に移動します。 

2. **前期** をクリックします。 

3. **終了** をクリックすると、前期の最後のジョブとしてジョブ リストの最後にジョブが移動されます。 

4. 一覧で、目的のレコードを見つけ、選択します。 たとえば、**計画期間** フィールドにある 2012 年 12 月 18 日にスケジュールされたジョブなど、ジョブ ステータスが **計画済み** となっているジョブを選択します。 その後、ジョブを次の期間に移動します。 

5. **次の期間** をクリックします。 

6. **開始** をクリックすると、前期の最初のジョブとしてジョブ リストの最初にジョブが移動されます。 

## <a name="move-a-job-within-a-period"></a>期間内へジョブを移動します。 

1. 一覧で、目的のレコードを見つけ、選択します。 たとえば、**計画期間** フィールドにある 2012 年 12 月 19 日にスケジュールされた 2 番目のジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。 その後、計画期間内にジョブを移動します。 

2. **次** をクリックします。 一覧でジョブが 1 行下へ移動することを確認します。 

3. **前** をクリックします。 一覧でジョブが 1 行上へ移動することを確認します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]