---
title: かんばん作業のスケジューリング
description: この手順は、特定の作業セルに対してプロセスかんばん作業をスケジュールすることに焦点を当てています。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97b88a2637e661146e8150cd6535ff32745227a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996804"
---
# <a name="schedule-kanban-jobs"></a>かんばん作業のスケジューリング

[!include [banner](../../includes/banner.md)]

この手順は、特定の作業セルに対してプロセスかんばん作業をスケジュールすることに焦点を当てています。 「材料が利用可能な場合にプロセスかんばん作業を準備する」という手順は、この手順を作成するための前提条件です。 この手順の作成に使用するデモ データの会社は USMF です。 このタスクは、かんばんを処理する作業現場の監督と生産計画担当者を対象としています。


## <a name="select-kanban-jobs-for-a-work-cell"></a>作業セルにかんばん作業を選択する
1. [生産管理] > [かんばん] > [かんばん作業スケジューリング] の順に移動します。
2. [期間能力ファクト ボックス] の展開
    * 「かんばん情報ボックス」を展開します。  
3. [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行をマークします。
    * 作業セル 1250 を選択します。 これによって、作業セル 1250 のジョブのみを表示するビューをフィルタ処理します。  
5. 一覧で、選択された行のリンクをクリックします。
6. [選択] をクリックします。

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>最初に作業可能な期間内にかんばん作業をスケジュールする
1. 一覧で、選択された行をマークします。
    * ステータスが [未計画] になっている一覧の最初の行を選択します。 [ジョブ ステータス] フィールドにある点を打たれたアイコンは、未計画を示します。  
2. [スケジュール] をクリックします。
    * これにより、最初に作業可能な期間内にかんばん作業をスケジュールします。  
    * かんばん作業は今日から開始期間に追加されたため、かんばん作業をリストの最後に移動するように注意します。  
    * 今日の日付を起点として開始した期間が完全に予約されると、ジョブは最初に作業可能な期間に移動します。  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>特定の日に 2 つのかんばん作業をスケジュールする
1. 一覧で行 1 を選択します。
    * 最初の行の [ジョブ ステータス] フィールドが [未計画] ステータスになっていることを確認する必要があります。  
2. 一覧で行 2 を選択します。
    * 2 番目の行の [ジョブ ステータス] フィールドが [未計画] ステータスになっていることを確認する必要があります。 ここで、最初の 2 つのジョブを選択しています。  
3. [スケジュール開始日] をクリックして、ドロップ ダイアログを開きます。
4. [書きの能力不足の反応] チェック ボックスをオンまたはオフにします。
    * このオプションでは、既定能力不足に対する反応を上書きすることができます。  
5. [能力不足に対する反応] フィールドで、[要求された期間設定に追加] を選択します。
    * このオプションによって、作業セルが過負荷状態になっているかに関係なく、ジョブが要求された期間に追加されるようにします。  
6. [スケジュール] をクリックします。
    * 両方のジョブが目的としている期間に追加されていることを確認します。  
    * [期間能力] セクションで、各期間の負荷を確認できます。 [消費] フィールドにはこの期間にスケジューリングされた消費が表示されます。 スケジュールされた消費がこの期間に使用可能な能力よりも高い場合、負荷状態にある消費が選択されます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]