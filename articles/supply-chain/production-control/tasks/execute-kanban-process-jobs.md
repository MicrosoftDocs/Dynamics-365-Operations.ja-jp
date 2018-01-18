--- 
title: "かんばんプロセス ジョブの実行"
description: "この手順は、かんばんプロセス ジョブの実行を対象としています。"
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 752eab976f740606154d416678ba2381641697df
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="execute-kanban-process-jobs"></a>かんばんプロセス ジョブの実行

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


