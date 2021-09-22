---
title: 調達に関するよく寄せられる質問
description: このトピックでは、Supply Chain Management の調達機能に関するよく寄せられる質問 (FAQ) への回答を提供します
author: kamaybac
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 09c99b88bc47609158805cdba1291ae462cda178
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476825"
---
# <a name="procurement-faq"></a>調達に関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

このトピックでは、Supply Chain Management の調達機能に関するよく寄せられる質問 (FAQ) への回答を提供します。

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

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>発注書をキャンセルしたユーザーを見つけることができますか ?

この情報は、発注書が変更管理の対象となる場合にのみ追跡されます。 変更管理を使用すると、変更 (キャンセル) を送信したユーザーと、変更を承認したユーザーを確認できます。

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>購買契約書を既存の発注書にリンクできないのはなぜですか?

購買契約書は、発注書が作成された後、発注書に関連付ける必要があります。 それ以外の場合、発注書の明細行を購買契約書の明細行に関連付けることはできません。

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>「手動または外部ドキュメントで入力した価格と割引を更新します」というメッセージが表示されるのは、どのチェックがトリガーになっていますか?

出荷日を変更すると、「手動または外部ドキュメントで入力した価格と割引を更新します」 というメッセージが表示される場合があります。 このメッセージは、出荷日が変更された場合、別の取引または販売契約が発生し、価格が変更される可能性があるために表示されます。 出荷日を変更は、倉庫のスケジュールやその他の関連情報にも影響を与える可能性があります。

このメッセージは、日付またはその他のパラメーターが変更されるたびに発生します。 メッセージの目的は、これらの変更によって発生する可能性がある価格の変更を確実に把握することです。

メッセージは、売買契約評価 (TAE) プロンプトです。 詳細な詳細については、[売買契約評価ポリシー](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) を参照してください。

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>カテゴリ ベースの品目を持つ購買注文明細行に対して複数の請求書を転記することはできないのはなぜですか?

請求書を転記する場合は、数量が必須です。 したがって、明細行の全数量が一部の金額でしか請求されていない場合は、別の請求書で残額を請求することはできません。
