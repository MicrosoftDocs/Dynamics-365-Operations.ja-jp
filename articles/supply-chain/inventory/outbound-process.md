---
title: 出荷プロセスの概要
description: このトピックでは、在庫管理の出荷プロセスの概要を示します。
author: perlynne
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 2f6638b3e79be5a2ebdbf6e5773285406239a080
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865451"
---
# <a name="outbound-process-overview"></a>出荷プロセスの概要

[!include [banner](../includes/banner.md)]

このトピックでは、在庫管理の出荷プロセスの概要を示します。

## <a name="output-orders"></a>出荷注文

出荷注文は、販売注文明細行をリンクしたり、ピッキング リストを使用する出荷ピッキング プロセスの注文明細行を転送するのに使用されます。

ピッキング リストは、販売注文または移動オーダーのいずれかから生成され、出荷注文と出荷が自動的に作成されます。 ピッキング リストには、出荷で 1 対 1 の関係があります。 移動オーダー出荷または販売注文の梱包明細票は、出荷から処理することができます。 

次の図に、出荷注文のプロセスの概要を示します。 

[![出荷注文プロセスの概要](./media/outbound-order.png)](./media/outbound-order.png)

出荷ルールを設定することにより、プログラムでの出荷処理方法を定義できます。 これらのルールを使用し、出荷プロセスを制御できます。 特に、出荷を送信するプロセスのどのステージを制御するかで、ルールを使用できます。 次の設定では、出荷プロセスの処理方法を定義します。

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>販売および移動オーダーのピッキング ルートのステータス 

**売掛金勘定** \> **設定** \> **売掛金勘定パラメーター** の順に移動し、**更新** タブで、**ピッキング ルートのステータス** フィールドの値を選択します。

[![販売注文のピッキング ルート ステータス フィールド](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

**ピッキング ルートのステータス** フィールドが **完了** 設定されると、ピッキング リストを生成するプロセスの一部として、ピッキング プロセスが自動的に行われます。 このフィールドが **有効化** に設定されている場合、ピッキング リスト明細行は手動で更新する必要があります。

同じ設定が移動オーダーに適用されます。 **在庫管理** \> **設定** \> **在庫および倉庫管理パラメーター** の順に移動し、**配送** タブで、**ピッキング ルートのステータス** フィールドで値を選択します。

[![移動オーダーのピッキング ルート ステータス フィールド](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>在庫出荷注文の終了

**在庫管理** \> **設定** \> **在庫および倉庫管理パラメーター** の順に移動し、**一般** タブで、**在庫出荷注文の終了** オプションを設定します。

[![在庫出荷注文の終了オプション](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

倉庫作業員が、ピッキング リスト数量を削減するときに、対応する在庫注文数量は出荷から削除されます。 ピッキング リストがある時点で更新されると、**在庫出荷注文の終了**オプションが**はい**に設定されている場合、残りの数量は注文に戻ります。 **在庫出荷注文の終了**オプションが**いいえ**に設定されている場合、残りの数量は出荷注文の数量として維持され、**出荷注文を開く**機能の一部として新しいピッキング リストに追加する必要があります。 

[![[機能] メニューで [出荷注文を開く] コマンド](./media/open-output-order.png)](./media/open-output-order.png)

[![[出荷注文を開く] ページの [機能] メニュー](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>数量の削減

ピッキング リストを生成するプロセスの一部として使用できる 3 番目のパラメーターは、**数量の削減** パラメーターです。 このパラメーターの設定は、**引当** 設定と強調し、引当プロセスを倉庫へのリリースの一部としてトリガーします。

[![数量の削減パラメーター](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>販売注文の出荷プロセスの例

この例では、2 つの品目の販売注文があります。 ピッキング リストの生成時に、**数量の削減** パラメーターを選択します。 したがって、使用可能な手持在庫に対してのみ、ピッキング明細行をリリースおよび作成します。 ピッキング リストの登録プロセスを介したピッキングを報告する必要があります (**ピッキング ルートのステータス** = **有効化**)。

まだ引当されていない在庫は、ピッキング リストの生成時に引当されます。 在庫がピッキング可能な場合、使用できない在庫は販売注文から削除されるか、または後で発信処理として倉庫へのリリースされるかのいずれかです。

[![ピッキング リストの更新](./media/update-picking-list.png)](./media/update-picking-list.png)

**ピッキング リスト登録** ページですべてのピッキング ラインがピッキングされるとすぐに、関連付けられている出荷が完了します。 販売注文の梱包明細のプロセスは、ピッキング済の在庫に基づいて初期化されます。

[![出荷配送の更新](./media/outbound-shipments.png)](./media/outbound-shipments.png)
