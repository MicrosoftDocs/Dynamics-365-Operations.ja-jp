--- 
title: "工程とジョブのスケジューリングによる製造オーダーのスケジュール"
description: "この手順では、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>工程とジョブのスケジューリングによる製造オーダーのスケジュール

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。 ジョブは、ジョブのスケジューリングで作成されますが、工程のスケジューリングでは作成されません。 このタスクの作成に使用するデモ データの会社は USMF です。 この手順は、個別の製造環境で作業をしている生産マネージャ、生産計画担当者、または作業現場の監督を対象としています。


## <a name="create-a-production-order"></a>製造オーダーの作成
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
2. [新しい製造オーダー] をクリックします。
3. [品目番号] フィールドで、値を入力または選択します。
    * 品目番号 D0001 を選択します。  
4. [作成] をクリックします。

## <a name="schedule-operations-for-the-production-order"></a>製造オーダの工程のスケジュール
1. 一覧で、選択された行をマークします。
    * 作成した製造オーダーを選択します。 一覧の先頭に表示されます。      
2. [アクション ペイン] で、[スケジュール] をクリックします。
3. 工程スケジュールをクリックします。
4. [スケジューリング指示] フィールドで、[スケジューリングの日付からフォワード] を選択します。
5. [スケジューリングの日付] フィールドに日付を入力します。
    * 将来期日、たとえば、今日とさらに 1 週間を選択します。 選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。  
6. [OK] をクリックします。
7. 一覧で、選択された行をマークします。
    * ステータスが "スケジュール済" に変わることに注意してください。  
8. 一覧で、選択された行のリンクをクリックします。
9. [すべてのジョブ] をクリックします。
    * ジョブは、工程のスケジューリングで作成されないことに注意してください。  
10. ページを閉じます。

## <a name="schedule-jobs-for-the-production-order"></a>製造オーダのジョブのスケジュール
1. [アクション ペイン] で、[スケジュール] をクリックします。
2. [ジョブのスケジュール設定] をクリックします。
3. [スケジューリング指示] フィールドで、[スケジューリングの日付からフォワード] を選択します。
4. [スケジューリングの日付] フィールドに日付を入力します。
    * 将来の日付、たとえば、今日とさらに 1 週間を選択します。 選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。  
5. [OK] をクリックします。
6. アクション ウィンドウで、[製造オーダー] をクリックします。
7. [すべてのジョブ] をクリックします。
    * 有効な工順に基づいて、ジョブ スケジューリングで5 つのジョブが作成されることに注意してください。  


