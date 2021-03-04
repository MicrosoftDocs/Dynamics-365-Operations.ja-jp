---
title: BOM 明細行イベントかんばんルールの作成
description: このタスクは、古典的な実稼働環境と混合リーン内の生産 BOM 明細行の供給を確認するイベントかんばんルールを作成するのに必要な設定を対象としています。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 698b7af3bc8e2146aaf86fb5e04dd123ea6d5153
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431687"
---
# <a name="create-a-bom-line-event-kanban-rule"></a>BOM 明細行イベントかんばんルールの作成

[!include [banner](../../includes/banner.md)]

このタスクは、古典的な実稼働環境と混合リーン内の生産 BOM 明細行の供給を確認するイベントかんばんルールを作成するのに必要な設定を対象としています。 このタスクの作成に使用するデモ データの会社は USMF です。 このタスクは、新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリーム マネージャーを対象としています。


## <a name="create-a-new-kanban-rule"></a>新しいかんばんルールの作成
1. [生産管理] > [定期処理のタスク] > [かんばん数量計算] > [かんばんルール] の順に移動します。
2. [新規] をクリックします。
3. [タイプ] フィールドで、「引き取り」を選択します。
    * 引き取りタイプが転送かんばんの作成に使用されます。  
4. [補充方法] フィールドで、「イベント」を選択します。
    * イベント戦略は、イベントに基づくかんばんの転送を作成するために選択されます。 後にタスク ガイドで、製造オーダーの見積が発生します。  
5. [最初の計画活動] フィールドで、値を入力または選択します。
    * ReplenishSpeakerComponents を入力または選択します。 この転送活動は入庫 (出荷) 倉庫と場所 12 にあるので、材料が 12 倉庫の場所 12 に移動されます。  
6. [詳細] セクションを展開します。
7. [製品] フィールドで、M0001 を入力または選択します。
8. [イベント] セクションを展開します。
9. [BOM 明細行イベント] フィールドで、「自動」を選択します。
    * [自動] を設定した [BOM 明細行イベント] フィールドで、製造オーダー BOM 明細行の材料ニーズを満たすためのかんばんが作成されます。  
10. ページを閉じます。

## <a name="create-and-modify-a-new-production-order"></a>新しい製造オーダーを作成および変更します。
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
2. [新しい製造オーダー] をクリックします。
3. [品目番号] フィールドで、値を入力または選択します。
    * 「L0001」を選択または入力します。 ただし、品目 M0001 が品目 L0001 の BOM に含まれるため、品目 L0001 を使用します。  
4. [作成] をクリックします。
5. リストで、L 0001 行のリンクをクリックします。
6. BOM をクリックします。
7. 一覧で、選択された行のリンクをクリックします。
8. [編集] をクリックします。
9. [行タイプ]フィールドで、「ペギングされた供給」を選択します。
    * ペギングされた供給は、かんばんの供給の作成を発生するために選択されます。  
10. [リソース消費]フィールドで、「いいえ」を選択します。
    * リソース消費のチェック ボックスをオフにすると、倉庫を変更することができます。  
11. [在庫分析コード] セクションを展開します。
12. [倉庫] フィールドに、「12」と入力します。
    * 倉庫は、引き取り活動の出荷倉庫である 12 に設定されます。  
13. [場所] フィールドに、「12」と入力します。
    * 場所は、引き取り活動の出荷場所である 12 に設定されます。  
14. ページを閉じます。
15. ページを閉じます。

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>製造オーダーの見積もりを行なって、作成するかんばんを表示します。
1. [見積] をクリックします。
    * 製造オーダーの見積時には、品目 M0001 を供給する関連のかんばんの作成が発生します。  
2. [OK] をクリックします。
3. ページを閉じます。
4. ページを閉じます。
5. [製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。
6. 一覧で、選択された行のリンクをクリックします。
    * 品目 M0001 用に作成したイベントかんばんルールを選択します。  
7. [かんばん] セクションを展開します。
8. 一覧で、選択された行をマークします。
    * 見積もりを行った製造オーダーの M0001 を供給するために作成されたかんばんを確認します。  
    * これは最後のステップです!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]