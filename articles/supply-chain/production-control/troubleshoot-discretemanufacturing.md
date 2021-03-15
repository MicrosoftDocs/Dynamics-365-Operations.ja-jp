---
title: 個別製造のトラブルシューティング
description: このトピックでは、個別製造を操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b0073cb2c3e3d6b9218caf20c394c8c0ca67b796
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966208"
---
# <a name="troubleshoot-discrete-manufacturing"></a>個別製造のトラブルシューティング

このトピックでは、個別製造を操作する際に発生する可能性がある問題の修正方法について説明します。

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>エラー メッセージ "倉庫管理プロセスは現在使用中です。 作業明細行がまだ登録されていない場合は、作成した作業をキャンセルし、すべての貨物または出荷明細行をキャンセルして、ピッキングまたは出荷プロセスを続行することができます" が表示されます。

### <a name="issue-description"></a>問題の説明

この問題は、明細行の引当またはリリースを実行しようとしたときに、在庫トランザクションのステータスが *ピッキング済* になっている (材料がピッキングされていることを示す) 場合に発生します。

### <a name="issue-resolution"></a>問題の解決

この問題を解決するには、次のいずれかの手順に従います。

- 製造オーダーのステータスを *見積済* または *リリース済* に変更します。
- 関連する製造オーダーの詳細ページを開きます。 アクション ウィンドウの **倉庫** タブの **停止** グループで、**停止してピッキング解除** を選択し、ピッキング済トランザクションをすべてピッキング解除します。 次に、**停止の削除** を選択して、製造オーダーを処理します。

*ピッキング解除* と *停止* の機能について、次で説明します。

- **ピッキング解除**: この機能は、部品表 (BOM) 明細行と、ステータスが *ピッキング済* から *注文中* になっているフォーミュラ明細行の在庫トランザクション ステータスを反転します。 未処理の材料ピッキングの作業が完了すると、明細行のステータスが *ピッキング済* に設定されます。 このステータスにより、製造オーダーが *作成済* ステータスにリセットされなくなります。 この場合、*ピッキング解除* 機能を使用して、トランザクションを *ピッキング済* ステータスから元に戻してから、製造オーダーを *作成済* ステータスにリセットすることができます。
- **停止**: この機能は、注文のステータスが更新されないようにするために製造オーダーに **停止済み** フラグを設定します。 **停止済み** フラグは、製造オーダーの詳細ページの **倉庫** クイックタブにあります。

> [!NOTE]
>
> - このボタンは、倉庫プロセスに対して有効になっている品目に対して製造オーダーが作成された場合にのみ表示されます。
> - **停止** グループは、製造オーダーの詳細ページのアクション ウィンドウの **倉庫** タブにのみ表示されます。 **製造オーダー** リスト ページの **倉庫** クイックタブには表示されません。

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>グローバル アドレス帳で作業者名を変更しても、一致するリソース名が更新されません。

### <a name="issue-description"></a>問題の説明

グローバル アドレス帳の作業者の名前を変更した場合、リソース グループ マスター内の一致するリソース名は更新されません。

### <a name="issue-resolution"></a>問題の解決

このシナリオは、現在サポートされていません。 問題を修正するには、リソース名を手動で更新する必要があります。

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>新しい製造オーダーを作成すると、"部品表と工順の有効なバージョンを挿入しますか?" というメッセージが表示されません。

### <a name="issue-description"></a>問題の説明

新しい製造オーダーを作成する場合は、品目番号を入力すると、**サイト** および **倉庫** フィールドが、完成品目の **既定の注文設定** ページで定義されている既定のサイトと倉庫に自動的に設定されます。 さらに、有効な BOM 番号と工順番号が自動的に入力されます。 これらの値の入力を求める次のメッセージは表示されません。

> 部品表および工順の有効なバージョンを挿入しますか?

### <a name="issue-resolution"></a>問題の解決

**既定の注文設定** ページでサイトと倉庫が定義されている製品を選択した場合、BOM と工順の番号を挿入するように求められることはありません。 選択した製品に対してこれらの値が定義されていない場合にのみ、プロンプトが表示されます。

## <a name="production-orders-arent-shown-on-the-marking-page"></a>[マーキング] ページに製造オーダーは表示されません。

### <a name="issue-description"></a>問題の説明

**マーキング** ページには、一部の製造オーダーが表示されません。

### <a name="issue-resolution"></a>問題の解決

次の構成を持つ製品をマーキングに使用することはできません。 したがって、これらは **マーキング** ページに表示されません。

- 製品は、*CW* タイプの製品として定義されます。
- これらは、高度な倉庫プロセスに対して有効になっています。
- これらは、*標準原価* 原則によって制御されるように構成されています。

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>製造オーダーを終了しようとすると、エラー メッセージ " BOM consumptionCost 値の計算は、在庫からの払出時には負である必要があります" が表示されます。

この問題は、リリース 10.0.15 で修正されました。

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>製造オーダーのステータスが "完了報告済" から "終了" に変更された場合、エラー メッセージ "更新が競合しています。 更新後に、標準原価が資産在庫金額と一致していません" および "関数 InventCostMovement.checkVariance で重大なエラーが発生しました" が表示されます。

この問題は、基になるデータが別のプロセスによって変更されたために発生します。 このプロセスでは、最大 5 回までデータを更新しようとします。 5 回試行しても競合が発生する場合は、次のエラー メッセージが表示されます。

> 更新が競合しています。 更新後の標準原価が資産在庫金額と一致しません。

> 関数 InventCostMovement.checkVariance で重大なエラーが発生しました。

この動作は仕様です。 この問題を回避するには、バッチ ジョブを再開します。 実行が完了する必要があります。

バッチ ジョブが再開後に一貫して失敗する場合は、元帳の既定の通貨の丸め精度が、InventSum テーブルの値に適用される丸めに準拠していることを確認してください。 丸めの精度が準拠していない値に変更された場合は、通常、それを対応する値に変更する必要があります。 **ModifiedDateTime** を探します。 この場合、値は、通常、丸めの精度が最近変更されたことを示しています。

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>倉庫にリリースすると、エラー メッセージ "品目 RM を完全に引当できませんでした。 数量がすべて使用可能であることを確認するか、BOM 明細行の [引当] フィールドが [手動] または [開始] に設定されている場合は、品目を手動で引当します。 一部の材料を引き当てることができないため、注文を倉庫にリリースできませんでした" が表示されます。 ただし、ステータスは [リリース済] に更新されます。

### <a name="issue-description"></a>問題の説明

製造オーダーがリリースされるときに、すべての BOM 明細行品目が物理的に使用可能ではない場合、**倉庫にリリース** ポリシーが製造オーダーで *完全引当を要求* に設定されていると、次のエラー メッセージが表示されます。

> 品目 RM を完全に引当することはできません。 数量がすべて使用可能であることを確認するか、BOM 明細行の [引当] フィールドが [手動] または [開始] に設定されている場合は、品目を手動で引当します。 注文を倉庫にリリースできませんでした。一部の材料を引き当てることができませんでした。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様であり、期待どおりに機能しています。

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>製造オーダーを終了して完了と報告しようとすると、エラー メッセージ "生産に対して完了報告済みの適正数量の合計は %1 です。 最後の工程に対するフィードバックは合計で 0.00 です" が表示されます。

### <a name="issue-description"></a>問題の説明

レポートを完了仕訳帳として製造オーダーに転記しようとすると、次のエラー メッセージが表示されます。

> 生産完了が報告された良品数量の合計が %1 になります。 最後の工程に対するフィードバックは合計で 0.00 です。

### <a name="possible-cause"></a>考えられる原因

この問題は、前回の工程で転記された数量が正しくなかった場合に発生します。 たとえば、生産が開始されているが、開始する必要のある数量が割り当てられていない場合、工順カード仕訳帳は明細行なしで転記されます。 状況を確認するには、製造オーダーを開き、アクション ウィンドウの **表示** タブで、**工順カード** を選択します。

### <a name="workaround"></a>回避策

仕訳帳が正しく転記されなかった工程に対して追加の仕訳帳を転記することにより、この問題を解決できます。 製造オーダーを再開し、追加の仕訳帳を転記する場合に選択します。 このアクションでは製造オーダーは開始されませんが、仕訳帳は転記されます。 その後、工順カードに転記済の数量が表示され、製造オーダーを正常に終了することができます。

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>エラーの数量を報告しているが、時間または材料の数量を報告していないときに、製造オーダーを完了として報告することはできますか。

正常数量も報告しなければ、製造オーダーのエラー数量を報告することはできません。 このシナリオはサポートされ **ません**。 製造オーダーを終了しようとすると、完了レポートの更新が最終的に失敗し、次のエラー メッセージが表示されます。

> 完了レポートの数量がありません。

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>消費された商品のシリアル番号に対して、完成品のシリアル番号を追跡できますか。

完成品のシリアル番号を、製造オーダーが完成品を作成するために消費する材料のシリアル番号に対して追跡することはできません。 このシナリオは、現在サポートされていません。 この回避策として、数量 1 の製造オーダーを作成できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]