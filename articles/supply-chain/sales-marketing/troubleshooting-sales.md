---
title: 販売注文に関するトラブルシューティング
description: このトピックでは、販売注文と作業する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 346ebee598e282abfe01a399793cc259aff3c22d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232233"
---
# <a name="troubleshoot-sales-orders"></a>販売注文に関するトラブルシューティング

このトピックでは、販売注文と作業する際に発生する可能性がある問題の修正方法について説明します。

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>販売注文ヘッダーの場所を変更しても、税金情報は更新されません。

### <a name="issue-description"></a>問題の説明

販売注文ヘッダーまたは明細行レベルで、サイト、倉庫、または配送先の住所が変更された場合、明細行のケースの税金情報は自動的に更新されません。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。 この問題が発生するのは、明細行レベルで配送先住所、サイト、および倉庫が自動的に変更されないためです。 手動でそれらをを更新する必要があります。

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>同じ期間または重複する期間に対して 2 つの売買契約がある場合は、常に同じ契約明細行が選択されます。

### <a name="issue-description"></a>問題の説明

2 つの売買契約が同じ期間または重複する期間に対して定義されている場合は、それらの品目を含む販売注文明細行を作成するたびに同じ売買契約が選択されるように見えます。

### <a name="issue-resolution"></a>問題の解決

特定の日付に対して複数の売買契約がある場合は、最低価格の売買契約が常に選択されます。 詳細については、[Microsoft Dynamics AX 2012 の売買契約](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90) のホワイトペーパーをダウンロードしてください。

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>需要を満たすために注文書を販売注文にリンクすることはできますか。

販売注文からの発注書を作成することができます。 詳細については、[販売注文から発注書を作成する](tasks/create-purchase-order-sales-order.md) をご覧ください。

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>返品注文または販売注文をキャンセルまたは削除できません。

*作成済* 状態の販売注文および返品注文のみをキャンセルできます。 詳細については、[返品注文のキャンセル](../service-management/cancel-return-order.md) を参照してください。

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>販売注文をキャンセルしようとすると、"予約に依存する作業が作成されているため、"引当を削除できません" というエラーを受信します。

エラーコード: WAX4661

作業が販売注文に関連付けられている場合、その作業がキャンセルされて取り消されるまで、販売注文をキャンセルすることはできません。 この要件は、販売注文に関連付けられている作業が終了されている場合にも適用されます。

この問題を解決するには、次の手順に従います。

1. 作業をキャンセルし、在庫を目的の場所に戻します。 販売注文の該当する負荷に移動し、読み込み行の **ピッキング済数量の削減** またはアクション ペインでの **作業の取消し** を選択します。

    この時点で、職場のステータスは *キャンセル済* になり、新しい在庫移動作業が自動的に作成および処理されて、在庫が取消時点で説明した保管場所に戻されます。

2. 負荷を削除します。 また、出荷も削除されます。
3. これで、販売注文に移動してキャンセルすることができます。

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>販売注文にリンクされている会社間発注書をキャンセルできません。

### <a name="issue-description"></a>問題の説明

販売注文にリンクされている会社間発注書をキャンセルしようとすると、"残余更新数量が変更されたため、数量を減らすことができません。" というエラーメッセージが表示される場合があります。

### <a name="issue-resolution"></a>問題の解決

この問題は、Microsoft Dynamics 365 Supply Chain Management バージョン10.0.13 で修正されました。 このバージョン以降のバージョンでは、販売注文にリンクされている会社間発注書をキャンセルできるようになりました。

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>削除された請求済販売注文を元に戻すことはできますか ?

### <a name="issue-description"></a>問題の説明

請求済の販売注文が誤って削除されました。これを復元するか、その詳細を表示する必要があります。

### <a name="issue-resolution"></a>問題の解決

削除された販売注文が既に請求されている場合は、**顧客アカウント \> トランザクション \> 元のドキュメント \> 詳細の表示** に移動します。 目的の請求書を検索し、その詳細を表示するために選択します。 この詳細には、販売注文の参照が含まれます。 また、このページから販売注文の詳細にアクセスできるようにする必要があります。

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>販売注文ヘッダーの期限が SalesOrderHeaderV2Entity データ エンティティに見つかりません。

[期日] フィールドは、*SalesOrderHeaderV2Entity* エンティティに存在しません。

## <a name="i-must-delete-orphaned-sales-order-records"></a>孤立した販売注文レコードを削除する必要があります。

孤立した販売注文レコードをクリーンアップするには、次のいずれかの場所に移動して、*販売注文の削除* の定期処理ジョブを実行します。

- 販売とマーケティング \> 定期的なタスク \> クリーンアップ \> 半日注文の削除
- 小売りおよびコマース \>小売業およびコマース IT \> クリーンアップ \> 販売注文の削除

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>既に転記されている請求書のコミッションを計算する方法はありますか。

Supply Chain Management は、転記された請求書のコミッションの計算は現在サポートしていません。

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>バンドル品目は、会社間プロセスではサポートされていません。

このバンドル品目は、発注書に対しては使用できません。なぜなら、このバンドル品目の販売注文明細行を確認すると、数量が *0* (ゼロ) になり、ステータスが *キャンセル済* であることがわかります。 この動作は仕様です。 この販売注文では、バンドル品目のコンポーネントのみが購入されます。 バンドル品目自体は購入されません。

バンドルを購入する必要がある場合、この機能は実際には収益認識シナリオのために設計されているため、バンドル品目としてマークする必要があるかどうかを検討します。 バンドル品目についての詳細情報は、[バンドル](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]