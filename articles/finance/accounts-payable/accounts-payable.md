---
title: 買掛金勘定ホーム ページ
description: このトピックでは、買掛金勘定の概要を示します。
author: ShylaThompson
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e20c26939389a72a8b3249bcb26bb3871768bbee
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820862"
---
# <a name="accounts-payable-home-page"></a>買掛金勘定ホーム ページ

[!include [banner](../includes/banner.md)]

このトピックでは、買掛金勘定の概要を示します。 

仕入先請求書を手動で入力するか、またはデータ エンティティによって電子的にそれらを受け取ることができます。 請求書の入力または入庫後、請求書承認仕訳または **仕入先請求書** ページを使用して、請求書を確認および承認できます。 確認プロセスを自動化するために請求書照合、仕入先請求書ポリシー、およびワークフローを使用すると、特定の基準を満たす請求書は自動的に承認され、残りの請求書には承認されたユーザーが確認するようにフラグが設定されます。

**業務プロセス**

[![業務プロセスのダイアグラム](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>買掛金勘定の設定

仕入先グループ、仕入先、転記プロファイル、各種の支払オプションのほか、仕入先、請求金額、出荷と出荷先、支払手形、他のタイプの買掛金勘定情報に関するパラメーターを設定します。 

[買掛金勘定のコンフィギュレーションの概要](accounts-payable-overview.md)

[仕入先請求書の勘定配布と補助元帳仕訳](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[買掛金勘定と売掛金勘定の外貨再評価](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>仕入先請求書のコンフィギュレーション

買掛金勘定を使用して、請求書および仕入先への支出を追跡します。

[買掛金勘定の請求書照合の概要](accounts-payable-invoice-matching.md)

[仕入先転記プロファイル](vendor-posting-profiles.md)

[買掛金勘定の請求書照合検証の設定](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[スリーウェイ マッチング ポリシー](three-way-matching-policies.md)

[請求書照合と会社間発注書](invoice-matching-intercompany-purchase-orders.md)

[請求書の合計価格の照合における差異の解決の概要](resolve-invoice-totals-invoice-matching-discrepancies.md)

[仕入先請求仕訳帳および請求書承認仕訳帳の既定の相手勘定](default-offset-accounts-vendor-invoice-journals.md)

[モバイルによる請求書承認](mobile-invoice-approvals.md)

[仕入先コラボレーションの請求ワークスペース](vendor-portal-invoicing-workspace.md)

[仕入先請求書の自動化](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>仕入先支払のコンフィギュレーション 

小切手、電子支払、支払手形などのシステム定義の支払タイプを、任意のユーザー定義の支払方法に割り当てます。 支払タイプはオプションですが、電子支払を検証する場合や、支払に使用する支払タイプをすぐに決定できるようにする必要がある場合に役に立ちます。 

[仕入先支払ワークスペース](vendor-payments-workspace.md)

[仕入先の支払手数料の定義](tasks/define-vendor-payment-fees.md)

[仕入先の支払条件の定義](tasks/define-vendor-payment-terms.md)

[確認後支払の概要](positive-pay-overview.md)

[確認後支払ファイルの設定と生成](set-up-generate-positive-pay-files.md)

[支払提案を使用した仕入先支払の作成](create-vendor-payments-payment-proposal.md)

[一部金額の仕入先支払](vendor-payments-partial-amount.md)

[仕入先支払の計算済割引より大幅な割引の適用](take-discount-more-calculated-discount-vendor-payment.md)

[現金割引期間外の現金割引の適用](take-cash-discount-outside-cash-discount-timeframe.md)

[仕入先小切手の電子申告サンプル](electronic-reporting-sample-vendor-checks.md)

[仕入先支払の取消](reverse-vendor-payment.md)

[前払請求書と前払](prepayments-invoices-vs-prepayments.md)

[買掛金勘定の集中支払](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>決済

この後のトピックでは、決済に関する情報を提供します。 決済は、請求書の支払を決済するプロセスです。 

[決済のコンフィギュレーション](../cash-bank-management/configure-settlement.md)

[割引日よりも前に一部仕入先支払を決済し割引日後に最終支払](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[仕入先訂正票で割引がある一部の仕入先支払の決済](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[複数の割引期間を持つ一部の仕入先支払の決済](settle-partial-vendor-payment-multiple-discount-periods.md)

[一部の仕入先支払の決済、および割引日より前の全額最終支払](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[複数の顧客または仕入先レコードを持つ単一伝票](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>追加リソース

#### <a name="whats-new-and-in-development"></a>新機能および開発中の機能

予定されている新機能を確認するには、[Microsoft Dynamics 365 リリース プラン](https://go.microsoft.com/fwlink/?linkid=2010158) を参照してください。 

#### <a name="blogs"></a>ブログ

買掛金勘定およびその他のソリューションに関する意見、ニュース、その他の情報については、[Microsoft Dynamics 365 ブログ](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)および [Microsoft Dynamics 365 Finance - Financials のブログ](https://community.dynamics.com/365/financeandoperations/b/financials)を参照してください。

[Microsoft Dynamics Operations パートナー コミュニティのブログ](https://community.dynamics.com/partner/b/operationspartnercommunityblog) では、Dynamics 365 に関する最新情報とトレンドを知るための単一のリソースが Microsoft Dynamics パートナー向けに提供されています。

#### <a name="community-blogs"></a>コミュニティのブログ

[Dynamics 365 Finance で買掛金を管理する方法](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>タスク ガイド
アプリケーションには、タスク ガイドとして使用できる追加のヘルプが用意されています。 タスク ガイドにアクセスするには、ページの [ヘルプ] ボタンをクリックします。

#### <a name="videos"></a>ビデオ

[Microsoft Dynamics 365 YouTube チャンネル](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) のハウツー ビデオをご覧ください。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]