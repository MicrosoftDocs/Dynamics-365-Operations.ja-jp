---
title: 発注書のトラブルシューティング
description: このトピックでは、発注書と作業する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 7b65c23fc7ac04fc30c0001bee9541a475026018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007494"
---
# <a name="troubleshoot-purchase-orders"></a>発注書のトラブルシューティング

このトピックでは、発注書と作業する際に発生する可能性がある問題の修正方法について説明します。

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>行番号が完全に配布された後にのみアクションを完了できます。

この問題は、発注書の配分に不整合があるために発生することがあります。

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>データ管理を通して発注書をインポートした場合、発注書明細行番号は、システム パラメータで定義されている増分に従いません。

### <a name="issue-description"></a>問題の説明

既定では、*発注書明細行 V2*  データ エンティティを通じてインポートされた発注書明細行の自動生成された行番号は、システム パラメータで指定されたシステム行番号の増分を使用しません。 ユーザー インターフェイス (UI) を通じて発注書を手動で作成し、明細行を追加すると、行番号が正しく増加します。 ただし、データ管理フレームワーク (DMF) を使用すると、正しく増加しません。

この問題が発生するのは、DMF で明細行をインポートしたときに、インポートされたエンティティで行番号が割り当てられていない場合に、DMF メソッドを使用してそれを割り当てるためです。 このメソッドでは、常に行番号が 1 ずつ増加します。

### <a name="issue-workaround"></a>問題の回避策

発注書明細行をインポートするときに、目的の行番号が [データエンティティの行番号] フィールドに既に設定されていることを確認します。 この場合、DMF は行番号を上書きしません。

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>既定の税グループと既定の現金割引が請求元仕入先に入力されていません。

顧客 ID とは異なる請求元仕入先を使用している場合、既定の税グループと既定の現金割引は、発注書が作成されるときに請求先/元 ID から入力されません。

この動作は仕様です。 税グループ、現金割引、およびその他の価格情報の既定値は、請求先/元 ID ではなく顧客 ID に基づいています。

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>発注書の確認に "オブジェクト参照が設定されていません" というエラーが表示されるか、仕入先請求書の転記中に "呼び出しのターゲットが例外をスローしました" という例外が発生します。

この問題は、発注書の配分に不整合があるために発生することがあります。

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>1 つ以上の勘定配布が、過剰配布されているか、配布中であるかのいずれかです。

### <a name="issue-description"></a>問題の説明

"1 つ以上の勘定配布が過剰配分されているか、配分中である" というエラーが表示されます。

### <a name="issue-resolution"></a>問題の解決

この問題は、発注書の配分に不整合があるために発生することがあります。

この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。 詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>自分が作成した発注書のみを表示できますか?

この機能は現在使用できません。

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>発注書の登録済在庫に対して、在庫を予約したりトランザクションを作成したりすることはできますか ?

### <a name="issue-description"></a>問題の説明

品目が発注書の *登録済* 状態にある場合でも 、在庫を引当てることができます。 つまり、登録済みの在庫に対してトランザクションを作成できます。

### <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. 発注書を作成します。
2. 発注書明細行を登録します。
3. 登録済みの在庫に対して引当またはトランザクションを生成できることに注意してください。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。 これは、登録された品目が倉庫または在庫に現物到着しており、引当に使用できるようになっていることを前提としています。

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>購買注文には、法人の言語設定は反映されません。

### <a name="issue-description"></a>問題の説明

発注書上の製品名は、発注書が作成された法人に対して設定されている言語ではなく、システム言語で表示されます。

### <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. システム言語を *EN-US* (米国英語) に設定します。
1. 製品名の翻訳に、*EN-US* と *DE* (ドイツ語) 言語が維持される製品があることを確認してください。
1. 法人の言語を *"DE"* に変更します。
1. 言語として *DE* が設定されている法人では、製品を含む発注書を作成します。
1. 製品名が米国英語 (システム言語) で表示されたままになっていることに注意してください。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。 発注書では、製品は常にシステム言語で表示されます。 発注書の言語は、確認仕訳帳が作成されたときに使用されます。

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>製品エンティティ別の承認済仕入先リストでは、有効日を変更することはできません。

### <a name="issue-description"></a>問題の説明

たとえば、ある製品には承認済仕入先があり、有効日は 2018 年 1 月 11 日 (*01/11/2018*)、有効期限は *なし* となっています。 有効日を 2018 年 1 月 10 日 (*01/10/2018*) または 2018 年 1 月 12 日 (*01/12/2018*) に変更しようとすると、次のエラーが表示されます。

> 承認済サプライヤー リスト (PdsApproveVendorList) にレコードを作成することはできません。 '有効期限' の値は、'有効' 値以上である必要があります。

### <a name="issue-resolution"></a>問題の解決

仕入先の承認期間のみ延長できます。 次のルールが適用されます。

- 有効日を、品目の仕入先の既存のレコード (期間) よりも前に変更するには、新しい期間の有効期限を既存のレコードの有効期限のすべての日付より前にする必要があります。
- 既存の期間より後の日付に有効期限を変更するには、既存のレコードの有効日が最新の有効期限の後にする必要があります。
- 仕入先が承認する合計期間を減らすには、既存のレコードを削除または変更する必要があります。 または、インポート中に **切り捨て** スイッチを使用することもできます。 このスイッチは、品目ごとに承認済仕入先のテーブル内の既存のレコードをすべて削除します。

レコードに有効日が *01/11/2018*、有効期限が *なし* となっている問題の説明で説明されているシナリオでは、有効期限が常にあるという、問題の説明で説明されているシナリオについては、有効日が *01/10/2018* で有効期限が *なし* となっている新規レコードをインポートできます。 ただし、データ管理を通じて有効日が *01/12/2018* に更新されるように期間を短縮することはできません。 この変更は UI を通じて行なわなければなりません。

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a>発注書ヘッダーの配送先住所を変更した後、配送先名は同期されません。

### <a name="issue-description"></a>問題の説明

発注書のヘッダーの住所が配送先住所ではない住所に更新されます。 住所は発注書上で更新されますが、更新された住所に基づいて配送先名が更新されることはありません。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。 選択された住所は配送先住所として分類される必要があります。 それ以外の場合、選択した住所に基づいて配送先名が更新されることはありません。

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>発注書をキャンセルしたユーザーを見つけることができますか ?

この情報は、発注書が変更管理の対象となる場合にのみ追跡されます。 変更管理を使用すると、変更 (キャンセル) を送信したユーザーと、変更を承認したユーザーを確認できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]