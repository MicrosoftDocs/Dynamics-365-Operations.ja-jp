---
title: かんばんプロセス ジョブの実行
description: この手順は、かんばんプロセス ジョブの実行を対象としています。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9da49ae17d6c25166f6b0e05e3c45fc991c9a54d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994157"
---
# <a name="execute-kanban-process-jobs"></a>かんばんプロセス ジョブの実行

[!include [banner](../../includes/banner.md)]

この手順は、かんばんプロセス ジョブの実行を対象としています。 最初のジョブでは、予定数量が完了されずエラーはありません。 2 番目のジョブはエラーで完了されます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、機械オペレーターを対象としています。


## <a name="select-a-kanban-job"></a>かんばん作業を選択
1. [生産管理] > [かんばん] > [プロセス ジョブのかんばんボード] の順に移動します。
2. [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. リソース グループ 1250 を含む行をクリックします。 これによって、作業セル 1250 のジョブのみを表示するジョブ リストをフィルター処理します。
    * 計画済みのジョブ ステータスがある行をマークします。  

## <a name="complete-a-job-with-expected-quantity"></a>予定数量のジョブを完了します。
1. [詳細] セクションを展開または折りたたみます。
    * このセクションでは、カード番号、品目番号、注文済の数量、および活動名に関する重要な情報を表示します。  
2. [生産指示] セクションを展開または折りたたみます。
    * このセクションでは、活動の生産指示を表示します。 その手順は、テキスト、写真、図面、またはその他のドキュメントのいずれかです。  
3. [開始] をクリックします。
    * 完了していないジョブを選択します。 ジョブ ステータスを表示している [ジョブ ステータス] フィールドでステータスのアイコンを使用します。      
4. [完了] をクリックします。
    * ジョブは、期待品質で完了しています。  

## <a name="complete-a-job-with-errors"></a>エラーのジョブを完了します。
1. [開始] をクリックします。
    * ジョブが完了すると、リストの次のジョブが自動的に選択されます。 [開始] をクリックする前にジョブを選択する必要はありません。  
2. [アクション ペイン] 上で、[製造] をクリックします。
3. \[完了\] (詳細) をクリックします。
4. 一覧で、選択された行をマークします。
5. [エラー数量] フィールドに番号を入力します。
6. [適正数量] フィールドに番号を入力します。
7. [OK] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]