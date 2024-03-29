---
title: リーン スケジュール グループの定義
description: リーン スケジュール グループは、かんばんスケジューリングの製品をグループ化して区別するために定義されます。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9d16c0d3192773c32c8dcc57a430607c6b60f97
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574452"
---
# <a name="define-lean-schedule-groups"></a>リーン スケジュール グループの定義

[!include [banner](../../includes/banner.md)]

リーン スケジュール グループは、かんばんスケジューリングの製品をグループ化して区別するために定義されます。 グループ化は、会社ごとの一般的な関連として、または作業セル特定としてできます。 各グループには、かんばんスケジューリング リストページでの視覚的表示のため、割り当てられた色コードがあります。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="define-lean-scheduling-group"></a>リーン スケジューリング グループの定義
1. [製品情報管理] > [リーン生産] > [リーン スケジュール グループ] に移動します。
2. [新規] をクリックします。
3. [スケジュール グループ] フィールドに値を入力します。
    * スケジュール グループは、グローバル グループとして、または作業セルを固有に定義できます。 この単純な例では、グローバル グループを定義し、作業セルは空白になります。 このグループの設定は、特定のスケジュール グループがないすべての作業セルに適用されます。  
4. 色セレクションから色を選択します。
    * かんばんスケジュールのリスト ページまたはかんばんプロセス ボードのジョブを強調表示するため、色が使用されます。  
5. 一覧で、選択された行をマークします。
6. 一覧で、選択された行のリンクをクリックします。

## <a name="associate-product"></a>製品の関連付け
1. 特定の製品を関連付けます。
    * 製品をリーン スケジュール グループに関連付けるには、特定の製品として(商品関係タイプ = 品目) または、品目配賦キーの一部として(商品関係タイプ = グループ) のいずれか 2 つの方法があります。    
2. [商品関係タイプ] フィールドで、品目を選択します。
3. [品目番号] フィールドに値を入力します。
4. [スループットの比率] フィールドに数値を入力します。
    * 既定のスループットの比率は 1 です。つまり、関連する製品は、生産フローのプロセス活動で指定されたのと同じ能力を消費することを意味します。 スループットの比率 > 1 はより高いリソース消費を定義し、スループットの比率 < 1 はより低いリソース消費を定義します。 この比率は原価計算とかんばん作業消費の計算に使用されます。  

## <a name="associate-item-allocation-key"></a>品目配賦キーの関連付け
1. 品目配賦キーの関連付け
    * [品目関係タイプ] グループを使用して、品目配賦キーにアソシエーションを追加します。   このプロセスには、データで定義された予測の品目配賦キーが必要なことに注意してください。  
2. [商品関係タイプ] フィールドで、グループを選択します。
3. [品目配賦キー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]