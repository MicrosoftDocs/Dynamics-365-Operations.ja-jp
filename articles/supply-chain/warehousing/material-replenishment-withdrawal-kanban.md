---
title: 引き取りかんばんを使用した補充
description: この記事では、製造活動における材料補充の引き取りかんばん使用方法を説明します。
author: perlynne
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 517b2eeb3b218fe0820ffa4e1d19b20841837b92
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863711"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>引き取りかんばんを使用した補充

[!include [banner](../includes/banner.md)]

この記事では、製造活動における材料補充の引き取りかんばん使用方法を説明します。

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>引き取りかんばんを使用する材料補充のワークフロー

引き取りかんばんは、倉庫と材料が消費される生産場所の間で、1 つの品目のかんばんを移動することに使用できます。 引き取りかんばんは、プル信号が特定の需要の供給をトリガするために必要な材料補充のプル ベースのソリューションをサポートします。 

次のシナリオでは、プル信号が生産プロセスの材料補充を行うかんばんの作成をトリガーする、プル ベース補充システムを示します。 

[![プル信号が生産プロセスの材料補充を行うかんばんの作成をトリガーします。](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  引き取りかんばん
2.  「開始」場所と倉庫作業用のプット場所のかんばん
3.  「配置」場所と生産入庫の場所のかんばん
4.  製造プロセス
5.  かんばんピッキング用の倉庫作業
6.  原材料の倉庫の場所
7.  材料倉庫
8.  製造倉庫

このシナリオでは、製造プロセス (4) が製造倉庫 (8) で、生産入庫の場所 (3) から材料を消費します。 材料 (かんばん) の取扱単位が消費されると、空として登録されます。 補充信号は元の品目に向け作られ、そして新しいかんばん (1) が作成されます。 この場合、元の品目は、材料倉庫 (7) 内の場所で構成されます。 かんばんの材料がピッキングされ、同じ倉庫内の場所 (2) に配置します。 材料がピッキングされた場合、場所 (2) から製造倉庫 (8) 内の生産入庫の場所 (3) へ転送する準備が出来ています。

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>引き取りかんばんのピッキングに向け、倉庫作業を構成

引き取りかんばんの原材料ピッキングを可能にするため、ウェーブ テンプレートや作業テンプレート、**かんばんピッキング** ワーク オーダー タイプの場所ディレクティブを構成します。 この作業の注文タイプは、引き取りかんばんのピッキング プロセスをサポートするだけではありません。 製造かんばんのピッキング プロセスもサポートします。 ただし、ウェーブ テンプレートや作業テンプレート、および場所ディレクティブを分けることで、かんばんのタイプごとに個別のピッキング プロセスを構成することができます。 ウエーブ テンプレートや作業テンプレート、および場所ディレクティブを分けるには、これらのエンティティのクエリ内の活動タイプ (**プロセス** または **転送**) に基準を設定します。

## <a name="configure-the-withdrawal-kanban"></a>引き取りかんばんを構成

引き取りかんばんに使用される転送活動は、リーン生産フローでアクティブ化された活動計画の一部として構成されます。 転送活動のコンフィギュレーションの一部として、転送の「開始」と「配置」場所を指定します。 転送活動を構成すると、**引き取り** タイプのかんばんルールに割り当てることができます。 引き取りかんばんにポリシーとコンフィギュレーションを設定し、かんばんルールとします。 かんばんの数量は、転送プロセス中で実行されるかんばんの材料取り扱い単位数を定義します。 固定補充方法を選択すると、固定かんばん数量が使用されます。 この数量は、需要のソース対して在庫を切らさないよう構築するために必要な数のかんばんを定義します。 固定数量は、実需、過去の需要、およびサービスのレベルに基づいて計算されます。 次の2つのシナリオでは、引き取りかんばんを使用する材料補充の管理方法について説明します。

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>シナリオ 1: 固定の引き取りかんばんを使用して、生産入庫の場所を補充

製造プロセスでは、製造倉庫内の生産入庫の場所から、購入済みの原材料を消費します。 原材料を仕入先から受信すると、材料倉庫内の場所に格納されます。 材料に対する需要は一定期間にわたって安定していると考えられる為、固定数量かんばんフロー内で生産を供給するよう設定されています。 生産入庫の場所でかんばんを消費すると、空シグナルが登録され、同じタイプの新しいかんばんがフローに追加されます。 

かんばんが完了すると、空シグナルは自動的に実行するようにコンフィギュレーションされています。 また、空シグナルは、かんばん転送ボードか携帯デバイス上のメニューから与えられる手動操作として設定できます。 かんばん転送ボードは、かんばんライフ サイクルのすべての活動を管理するワークスペースです。 

かんばんが作成されると、原材料のウェーブ明細行が材料倉庫のかんばんウェーブに追加されます。 かんばん転送ボードのピッキング リスト セクションでは、材料が「転送元」の場所に置かれ生産入庫の場所へ転送準備ができるまで、ウェーブ作成から作業作成において材料および関連する倉庫プロセスのステータスを監視できます。 かんばんは、かんばん転送ボードまたは携帯デバイス上のメニューから実行することができます。 

このシナリオでは、材料倉庫のピッキング作業は 1 つの活動として処理されます。 材料倉庫と生産倉庫の間の転送活動は、個別の活動として処理されます。 この方法は、たとえば、2 つの倉庫の間で大規模な物理的距離がある場合に役立ちます。 この場合、かんばん転送活動はトラック負荷を表すことができます。 

倉庫の場所と生産入力の場所の間の距離が小さい場合は、ピッキング プロセスに転送活動を加える方が効率的かもしれません。 そして、材料を選択した後、生産入庫の場所に直接配置できます。 このプロセスをサポートするためには、引き取りかんばんのピッキング作業が処理される際に自動的に完了するように転送活動を構成します。

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>シナリオ 2: かんばんピッキング作業が処理されるときは、自動的に転送活動を完了します。

次のシナリオでは、引き取りかんばんの転送活動は同じ倉庫内の 2 つの場所の間で転送するように構成されています。 引き取りかんばんの転送活動は、自動的に完了すように設定されます。 

[![かんばんピッキング作業が処理されると、転送活動は自動的に完了します。](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  原材料と生産の倉庫を共有
2.  原材料の倉庫の場所
3.  「開始」場所と倉庫作業用のプット場所のかんばん
4.  引き取りかんばん
5.  生産入庫の場所
6.  製造プロセス

生産入庫の場所でかんばんを消費すると、空と報告され、新しいかんばんがフローに追加されます。 かんばんが作成されると、ウェーブ明細行がかんばんウェーブに追加されます。 かんばんウェーブが処理されるときは、かんばんピッキング用の倉庫作業が作成されます。 倉庫作業者は、かんばんピッキングの作業を処理すると倉庫場所のかんばん用材料をピッキングする作業を行うよう指示されます。 この倉庫作業者がピッキングを確認する際、かんばんは自動的に完了し、作業者は材料を生産入庫の場所に配置するようガイドされます。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]