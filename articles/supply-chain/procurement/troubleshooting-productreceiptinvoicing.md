---
title: 製品受領書と請求書に関するトラブルシューティング
description: このトピックでは、製品受領書と請求の処理中に発生する可能性がある問題を修正する方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834388"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>製品受領書と請求書に関するトラブルシューティング

このトピックでは、製品受領書と請求の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>カテゴリ ベースの品目を持つ購買注文明細行に対して複数の請求書を転記することはできません。

請求書を転記する場合は、数量が必須です。 したがって、明細行の全数量が一部の金額でしか請求されていない場合は、別の請求書で残額を請求することはできません。

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>発注書の確認に "オブジェクト参照が設定されていません" というエラーが表示されるか、仕入先請求書の転記中に "呼び出しのターゲットが例外をスローしました" という例外が発生します。

この問題は、発注書の配分に不整合があるために発生することがあります。

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>複数の製品受領書を 1 つの発注書にまとめることはできません。

複数の製品受領書を 1 つの発注書にまとめることはできません。異なる製品受領書明細行の会計日付が異なる場合に使用します。

Microsoft Dynamics 365 Supply Chain Management の以前のバージョンでは、このような場合に懸念許されていました。 ただし、このプラクティスではエラーが発生しやすくなります。 作成された発注書明細行の会計日と、その発注書明細行の作成元である製品受領書明細行の会計日とは異なるものにする必要があります。 (発注書明細行の会計日は、発注書ヘッダーの会計日と一致します。) したがって、複数の製品受領書を1つの発注書に連結することはできなくなります。

たとえば、予算引当や債務など、会計日が使用されます。 したがって、この品目は、製品受領書から発注書への移行時に保持する必要があります。

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>製品受領書がキャンセルされると、トランザクションを中断された勘定科目に転記できます。

### <a name="issue-description"></a>問題の説明

製品受領書がキャンセルされると、主勘定が中断された場合でも、保留中の勘定科目にトランザクションを転記することができます。

### <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. **買掛金勘定パラメーター** ページの **一般** タブで、**元帳の製品受領書の転記** オプションが *はい* に設定されていることを確認します。
1. 発注書を作成し、製品に対して *1000* の数量を持つ注文明細行を追加します。
1. 発注書を確認します。
1. 製品受領書を転記し、伝票を確認します。
1. 関連する主勘定 *200140* と *140200* を中断します。
1. 転記された製品受領書をキャンセルします。
1. トランザクションが保留中の勘定に転記される可能性があることに注意してください。

### <a name="issue-resolution"></a>問題の解決

製品受領書がキャンセルされると、トランザクションが保留中の勘定に転記される場合があります。なぜなら、この動作では、正しい転記が許可されるからです。

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>製品受領書で財務伝票が生成されていない場合でも、製品受領伝票番号が消費されます。

品目モデルグループで **製品受領書の未収負債** オプションが *いいえ* に設定されている場合、一般会計への転記は行われません。 ただし、補助元帳で会計を目的として現物イベントが記録され、そのイベントに伝票番号が必要な場合があります。 この伝票番号は、在庫トランザクションで参照される伝票番号です。

[製品受領時に雑費を転記する](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/) のブログ記事に説明されている通り、**製品受領時に負債を見越計上** オプションを *はい* に設定することを推奨します。

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>元帳設定の [勘定への転記] の設定が有効になっていません。

### <a name="issue-description"></a>問題の説明

この問題は、**買掛金勘定パラメータ** ページの **請求書** タブで、**元帳の掛売勘定に転記** オプションを *はい* に設定された時に発注書が請求されるときに発生します。

### <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. **買掛金勘定 \> 設定 \> 買掛金勘定パラメーター**の順に移動します。
1. **請求書** タブで、**元帳の掛売勘定に転記** オプションを *はい* に設定します。
1. **在庫管理 \> 設定 \> 転記 \> 転記** に移動します。
1. **発注書** タブで、製品の購買経費のすべての明細行が削除されていることを確認します。
1. **買掛金勘定 \> 発注書 \> すべての発注書**に移動します。
1. 発注書を作成します。 **仕入先勘定** フィールドで、*1001 Acme 事務用品* を選択します。
1. 以下の設定で注文書明細行を追加します。

    - **品目番号:** *D0011 レーザー プロジェクター*
    - **サイト:** *1*
    - **倉庫:** *11*
    - **数量:** *4*

1. アクション ペインで、**購入** タブの **アクション** グループで、**確認** を選択します。
1. アクション ペインの、**受領** タブの **一般** グループで、**製品受領書** を選択します。
1. **製品受領書の転記** ダイアログボックスの **製品受領書** フィールドに任意の番号を入力し、**OK** を選択します。
1. アクション ペインの、**請求書** タブで、**生成** グループから **請求書** を選択します。
1. **番号** フィールドに、請求書番号として任意の数を入力します。
1. 照合状態を更新して、転記します。
1. 発注書から請求書を生成すると、"製品タイプの取引タイプに対する仕入先の勘定番号が存在しません。" というエラーが表示されることに注意してください。

### <a name="issue-resolution"></a>問題の解決

これは、請求書および請求書グループのパラメータ設定によって異なります。 詳細については、[発注書と在庫の変動に関する会計転記](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/) を参照してください。
