---
title: 製造オーダー状態を逆行させる
description: この記事では、製造オーダーのステータスを取り消す方法について説明します。
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmStatusDecrease, ProdSetupStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d50cbcb4031d5c9f2c814883afd1fb38777d2ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903959"
---
# <a name="reverse-the-production-order-status"></a>製造オーダー状態を逆行させる

[!include [banner](../includes/banner.md)]

この記事では、製造オーダーのステータスを取り消す方法について説明します。 

製造オーダーのステータスを戻すと、注文および工順に関連付けられているすべての工程が、生産ライフ サイクルの前のステップに戻されます。 たとえば、製造オーダーのステータスが **スケジュール済** で、ステータスを **作成済** に戻します。 この場合、システムによって最初にステータスを **見積済**、つまり **スケジュール済** の直前のステータスに変更します。 その後、ステータスを目的の **作成済** ステータスに変更できます。 **注記:** 注文が **完了レポート** ステータスに到達していても、これを前のステータスに戻すことができます。 ただし、見積および工程のスケジューリングまたはジョブのスケジューリング、あるいはその両方のスケジューリングを実行して、再度注文の情報を更新する必要があります。 このステップは、残余品目消費および運営リソース消費の引当もリセットする必要があるため必須のステップです。 この記事の残りの部分では、次のように、製造オーダーのステータスを戻す場合に実行される内容を説明します。

-   **見積済** から **作成済** へ
-   **スケジュール済** から **見積済** へ
-   **リリース済** から **スケジュール済** へ
-   **開始済** から **リリース済** へ

## <a name="from-estimated-to-created"></a>[見積済] から [作成済] へ
製造オーダーのステータスを **見積済** から **作成済** に戻す場合、部品表 (BOM) の品目に対して計算された品目消費は削除されます。 生産ラインの在庫トランザクションは削除され、生産の BOM 明細行の **残余のステータス** フィールドは **終了済** にリセットされます。 **派生購買** と **派生生産** オプションが選択されている場合、基になる発注書または製造オーダーが削除されます。 製造オーダー原価を見積もる場合、または生産で使用するために品目を手動で引当されている場合、これらのトランザクションが削除されます。

## <a name="from-scheduled-to-estimated"></a>[スケジュール済] から [見積済] へ
ステータスを **スケジュール済** から **見積済** に戻す場合、スケジュールされた開始日と終了日および時刻が削除されます。 スケジュール中に作成された確保済能力は削除され、ジョブ スケジュール中に作成されたジョブも削除されます。 **製造オーダーの詳細** ページで記録される、工程スケジューリングとジョブ スケジューリングについてのすべての情報は、リセットされます。

## <a name="from-released-to-scheduled"></a>[リリース済] から [スケジュール済] へ
製造オーダーのステータスを **リリース済** から **スケジュール済** に戻した場合、変化するのはステータスのフィールドの値のみです。

## <a name="from-started-to-released"></a>[開始済] から [リリース済] へ
製造オーダーのステータスを **開始済** から **リリース済** に戻すと、完了したとして報告されたすべての品目の設定は戻されます。 材料がピッキング済であるか、入庫および出荷の配送が生産に対して行われていた場合は、これらの設定は戻されます。 製造オーダーの BOM 明細行の **残余のステータス** フィールドは、**終了済** から **材料消費量** に変更されます。 時間が登録済または数量が生産工順の工程で完了と報告される場合、これらの設定は取り消されます。 生産工順における **残余のステータス** フィールドは、**終了済** から **工順消費** に変更されます。 プロセス中またはプロセスの作業としてと転記されたすべての品目の設定は戻されます。 **製造オーダーの詳細** ページで、開始または完了報告された数量を示すフィールドはリセットされます。 これらのトランザクションの日付も、リセットされます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]