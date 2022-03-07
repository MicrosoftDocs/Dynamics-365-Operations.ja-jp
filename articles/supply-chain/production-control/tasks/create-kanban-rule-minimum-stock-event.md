---
title: 最小の在庫イベントを使用したかんばんルールの作成
description: この手順では、特定の製品が特定の場所で常に使用できるようにするために、最小在庫のイベントを使用してかんばんルールを作成するのに必要な設定を中心に説明します。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19b4f80c6afa2634c469a23dfcd8dd8f151dd6cc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998706"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>最小の在庫イベントを使用したかんばんルールの作成

[!include [banner](../../includes/banner.md)]

この手順では、特定の製品が特定の場所で常に使用できるようにするために、最小在庫のイベントを使用してかんばんルールを作成するのに必要な設定を中心に説明します。 かんばんルールは、在庫レベルが 200 個を下回ったときに材料をその場所に転送するために作成されます。 ペギング イベント処理を実行することによって、必要なかんばんが作成されます。 このタスクの作成に使用するデモ データの会社は USMF です。 このタスクは、リーン環境で新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。


## <a name="create-a-new-kanban-rule"></a>新しいかんばんルールの作成
1. [製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。
2. [新規] をクリックします。
3. [タイプ] フィールドで、「引き取り」を選択します。
    * このタイプは転送かんばんの作成に使用されます。  
4. [補充方法] フィールドで、「イベント」を選択します。
    * イベント戦略は、イベントに基づくかんばんの転送を作成するために使用されます。 後の手順で、在庫補充を使用して転送かんばんをトリガーします。  
5. [最初の計画活動] フィールドで、値を入力または選択します。
    * ReplenishSpeakerComponents を入力または選択します。 この転送活動には入庫 (出荷) 倉庫と場所 12 があるので、材料は倉庫 12 のロケーション 12 に移動されます。  
6. [詳細] セクションを展開します。
7. [製品] フィールドで、値を入力または選択します。
    * M0007 を選択します。  
8. [イベント] セクションを展開します。
9. [在庫補充イベント] フィールドで、「バッチ」を選択します。
    * これにより、ペギング イベント処理中に関連する場所へ材料ニーズを満たすかんばんを作成します。  

## <a name="set-the-minimum-quantity-for-the-item"></a>品目の最小数量の設定
1. クリックして、[製品] フィールドのリンク先を表示します。
2. クリックして、[品目番号] フィールドのリンク先を表示します。
3. 製品画像の情報ボックスを展開します。
4. アクション ウィンドウで、[計画] をクリックします。
5. [品目補充] をクリックします。
6. [新規] をクリックします。
7. 一覧で、選択された行をマークします。
8. [倉庫] フィールドで、値を入力または選択します。
    * [倉庫] を 12 に設定します。  
9. 最小を「200」に設定します。

## <a name="run-the-batch-event-creation-job"></a>バッチ イベント作成ジョブの実行
1. [生産管理] > [定期処理のタスク] > [かんばん作業のバッチ処理] > [ペギング イベント処理] の順に移動します。
2. [OK] をクリックします。
3. [製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。
4. 一覧で、選択された行のリンクをクリックします。
    * 先に作成されたかんばんルールを選択します。  
5. [かんばん] セクションを展開します。
    * 必要な材料を倉庫 12 に転送するためにかんばんが作成されたことを確認します。  

