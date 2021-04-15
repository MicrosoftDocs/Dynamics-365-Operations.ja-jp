---
title: 価格、割引、契約、リベートのトラブルシューティング
description: このトピックでは、価格、割引、契約、およびリベートの処理中に発生する可能性がある問題を修正する方法について説明します。
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 12bc3cbccb1577c278489f640299510b3ced17e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811089"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>価格、割引、契約、リベートのトラブルシューティング

このトピックでは、価格、割引、契約、およびリベートの処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>発注書が作成された後、購買契約書を発注書の明細行にリンクできません。

購買契約書は、発注書が作成された後、発注書に関連付ける必要があります。 それ以外の場合、発注書の明細行を購買契約書の明細行に関連付けることはできません。

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>「手動または外部ドキュメントで入力した価格と割引を更新します」というメッセージが表示されるのは、どのチェックがトリガーになっていますか?

出荷日を変更すると、「手動または外部ドキュメントで入力した価格と割引を更新します」 というメッセージが表示される場合があります。 このメッセージは、出荷日が変更された場合、別の取引または販売契約が発生し、価格が変更される可能性があるために表示されます。 出荷日を変更は、倉庫のスケジュールやその他の関連情報にも影響を与える可能性があります。

このメッセージは、日付またはその他のパラメーターが変更されるたびに発生します。 メッセージの目的は、これらの変更によって発生する可能性がある価格の変更を確実に把握することです。

メッセージは、売買契約評価 (TAE) プロンプトです。 詳細な詳細については、[売買契約評価ポリシー](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) を参照してください。

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>発注受入には、すべての費用は含まれません。

### <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. **調達パラメーター** ページの **配送** タブで、**製品受領時に費用を生成** オプションが *はい* に設定されていることを確認します。
1. 費用を含む発注書を作成します。
1. 発注書を確認します。
1. 発注書を受け取ります。
1. 受入合計を確認し、予想される合計と比較します。
1. すべての費用が発注受入に含まれているわけではないことに注意してください。

### <a name="issue-resolution"></a>問題の解決

解決策は、雑費が設定されている方法によって異なります。 要件に合わせて雑費を設定する方法については、次のブログ記事を参照してください: [製品受領時に雑費を計上する](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>売買契約価格および割引は、データ管理を介してインポートされた販売注文または発注書の明細行には適用されません。

### <a name="issue-description"></a>問題の説明

販売注文または発注書の明細行に適用可能な売買契約は、データ管理を介してインポートされた明細行には適用されません。 ただし、手動で作成された販売注文または発注書の明細行には、同じ売買契約が適用されます。

### <a name="reason-for-the-issue"></a>問題の理由

データ管理を介してインポートされた発注書の明細行に価格情報が既に含まれている場合、それらの明細行に対する売買契約は再評価されません。 たとえば、**行割引の割合** または価格と割引のいずれかの値が、明細行に設定されている場合、その明細行に対して売買契約は検索されません。

### <a name="issue-workaround"></a>問題の回避策

この動作は予期されるものであり、販売注文と発注書の両方で類似しています。

回避策として、価格情報を設定せずに発注書の明細行をインポートします。 その結果、売買契約が適用され、定義された売買契約に基づいて発注書の明細行が更新されます。

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>仕入先リベートは、請求書に基づいて累計されません。

### <a name="issue-description"></a>問題の説明

転記された請求書の支払期日が異なる場合、それらの請求書は、それらから生成される仕入先リベートには反映されません。

### <a name="issue-resolution"></a>問題の解決

仕様では、仕入先リベートの計算時に期日が考慮されません。 実際の仕入先リベートに関して、期日と請求書との関係がより明確になるようにシステムをカスタマイズすることを検討してください。

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>発注書の単価は、単位換算に基づいて計算されません。

### <a name="issue-description"></a>問題の説明

発注書の単位が変更された場合、売買契約価格は単位換算定義に従って再計算されません。

### <a name="issue-resolution"></a>問題の解決

価格は常に売買契約 (または販売契約書や品目価格などのシステム内のその他の価格設定) から取得され、単位に対して設定されます。

注文明細行で単位が変更されると、システムは新しい単位の価格を検索し、その価格を適用します。 単位の価格が見つからない場合は、システムは価格を適用しません。 単位換算を使用して、価格を別の単位に再計算することはできません。 理論的には、10 個入りの 1 箱の価格は、1 箱の価格の 10 倍と等しくない場合があります。

### <a name="issue-workaround"></a>問題の回避策

この問題を回避する 1 つの方法は、品目の注文明細行で使用されると予想される単位の売買契約があることを確認することです。

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>通貨換算の問題は、売買契約で発生します。

通貨が発注書で異なる場合、売買契約価格が通貨に従って再計算されません。

*一般通貨* 機能を使用すると、価格と割引を 1 つの通貨でのみ定義できます。 その後、必要に応じて、他の通貨に換算できます。 さらに、換算が完了すると、機能によって自動的にスマート丸めが適用されます。

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>行ビュー モードで購買契約ページを開くと、明細行の概要に価格単位フィールドを追加してページをカスタマイズできません。

契約フレームワーク内の一部の共有フィールドは、個人用設定に含めることはできません。 この制限は、実装されるデータ モデルが原因で発生します。 したがって、**価格単位** フィールドをカスタマイズすることはできません。

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>購買契約書の上限は、購買要求に対して有効ではありません。

### <a name="issue-description"></a>問題の説明

購買要求が購買契約書にリンクされている場合、購買要求に対して購買契約書の上限は有効ではありません。 既定の価格情報は正しく入力されていますが、購買要求で購買契約書の上限を超えて注文することができます。

### <a name="issue-resolution"></a>問題の解決

この動作は予期されています。 要求が常に承認されるとは限らないため、購買契約書に数量または金額を予約しないでください。 したがって、購買契約書の上限には達しません。

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>売買契約は、却下された RFQ から作成できます。 したがって、RFQ 明細行が受理されていない場合でも、システムは売買契約仕訳帳の作成を妨げません。

承認されたかまたは却下されたかに関係なく、見積依頼 (RFQ) に対するすべての返信は、売買契約を作成できます。 詳細については、[見積依頼 (RFQ) の概要](request-quotations.md) を参照してください。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]