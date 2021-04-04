---
title: リーン生産のプロセス活動の作成
description: リーン生産のプロセス活動を作成します。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ef63faaf836c1ac929324d2b3cd4aaaee9b1352
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255112"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>リーン生産のプロセス活動の作成

[!include [banner](../../includes/banner.md)]

リーン生産のプロセス活動を作成します。 

前提条件: 

1. 有効ではない生産フローおよびバージョンを作成する必要があります。

2. 作業セルを作成する必要があります。


## <a name="find-the-production-flow-version"></a>生産フロー バージョンの検索
1. [生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。

## <a name="create-a-new-activity"></a>新しい活動の作成
1. [活動] をクリックします。
    * 選択した生産フローに、ドラフト バージョンがあることを確認し、そのバージョンを選択します。  
2. [新しい計画活動の作成] をクリックします。
3. [次へ] をクリックします。
4. [名前] フィールドに値を入力します。
5. [名前] フィールドに値を入力します。
    * すべてのバージョンにおいて、指定された生産フローに対する名前は一意にする必要があることに注意してください。  
6. [処理数量] フィールドで、数値を入力します。
    * 処理される作業数量にかかわらず、これが人件費を計算する作業ごとの最小数量であることに注意してください。 作業の数量がこの数量から逸脱すると、人件費の差異が作成されます。  
7. [次へ] をクリックします。

## <a name="select-the-work-cell"></a>作業セルの選択
1. [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
2. 一覧で、選択された行のリンクをクリックします。

## <a name="define-the-inventory-updates"></a>在庫更新の定義
1. [入庫時に手持在庫を更新] チェック ボックスをオンまたはオフにします。
    * [手持在庫の更新] = [いいえ] である場合、半完成品の製品を入庫する活動を定義できます (その活動は次の BOM レベルには達しません)。    半完成の製品の消費も選択できます。  

## <a name="define-the-picking-activities"></a>ピッキング活動の定義
1. [次へ] をクリックします。
2. 一覧で、選択された行をマークします。
    * 既定のピッキング活動は、選択された作業セルの入庫場所に対して作成されます。  
3. [追加] をクリックします。
    * 作業セルの入力活動がステージ完了になっていない、特定の製品の追加のピッキング活動を作成できます。  
4. 一覧で、目的のレコードを見つけ、選択します。
5. [品目番号] フィールドに値を入力します。
6. [倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * この定義により、活動で消費されたすべての材料は、既定の入庫場所、および 2 番目のピッキング活動で定義された品目を除外する場所からピッキングされます。 この品目は、別の倉庫および場所からピッキングされます。  
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. [仕損の登録] チェック ボックスをオンまたはオフにします。
10. [次へ] をクリックします。

## <a name="define-the-activity-times"></a>活動時間の定義
1. 一覧で、目的のレコードを見つけ、選択します。
    * ランタイムの定義が必要です。 ランタイムは、かんばん作業の原価およびスループットの時間の計算に使用されます。 ランタイムは最大能力負荷および消費の計算には使用されていません。これは生産フロー バージョンのタスクから導かれるサイクル時間で計算されます。  
2. [時刻] フィールドで、数値を入力します。
3. [単位] フィールドに値を入力します。
4. [時間単位] を選択します。
5. [数量ごと] フィールドで、数値を入力します。
6. 一覧で、目的のレコードを見つけ、選択します。
    * 待ち時間はオプションです。  
7. [時刻] フィールドで、数値を入力します。
8. [単位] フィールドに値を入力します。
9. [時間単位] を選択します。
10. [数量ごと] フィールドで、数値を入力します。
11. [次へ] をクリックします。
12. [完了] をクリックします。
13. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]