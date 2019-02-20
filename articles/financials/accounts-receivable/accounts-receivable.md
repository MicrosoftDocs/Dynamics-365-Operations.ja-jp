---
title: 売掛金勘定ホーム ページ
description: 顧客請求書および入金される支払を追跡するには、売掛金勘定を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/18/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerInvoiceWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 20671
ms.assetid: 1040678e-ffcb-47fb-a1bc-626db8046504
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 303d67c0b662e6c21cebb5aa10ed28555459522e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "302549"
---
# <a name="accounts-receivable-home-page"></a>売掛金勘定ホーム ページ

[!include [banner](../includes/banner.md)]

顧客請求書および入金される支払を追跡するには、売掛金勘定を使用します。 

販売注文や梱包明細に基づいて顧客請求書を作成できます。 また、販売注文に関連付けられていない自由書式の請求書を入力することもできます。 複数の異なる支払タイプを使用して、支払を受け取ることができます。 これには、受取手形、現金、小切手、クレジット カード、電子支払が含まれます。 組織に複数の法人が含まれている場合、集中支払を使用して、その他の法人に代わって 1 つの法人で支払を記録することができます。


**業務プロセス**

[![業務プロセス](./media/AR-process.PNG)](./media/AR-process.PNG)

## <a name="set-up-accounts-receivable"></a>売掛金勘定の設定

顧客請求書および顧客から受け取る支払を追跡するには、売掛金勘定を使用します。 顧客グループ、顧客、転記プロファイル、利子計算書、督促状、コミッションのほか、顧客、請求金額、出荷と出荷先、受取手形、および他のタイプの売掛金勘定情報に関するパラメーターを設定できます。 

:::row:::
    :::column:::
        - [自由書式の請求書の勘定配布と補助元帳仕訳](accounting-distributions-subledger-journal-entries-free-text-invoices.md)
        - [顧客転記プロファイル](customer-posting-profiles.md)
        - [クレジット カードの設定、認証、および取得](credit-card-authorizations.md)
        - [顧客請求書の作成](configure-customer-invoices.md)
        - [定期請求書の設定と処理](set-up-process-recurring-invoices.md)
        - [自由書式の請求書の訂正](correct-free-text-invoice.md)
    :::column-end:::
    :::column:::
        - [受取手形の設定](set-up-bills-exchange.md)
        - [利息コードに対する金利の設定](set-up-interest-rates-interest-code.md)
        - [利息手数料の免除、再開、または取り消し](waive-reinstate-reverse-interest-fees.md)
        - [単一ユーロ支払地域 (SEPA) 口座引落の概要](sepa-direct-debit-overview.md)
        - [SEPA の口座引落の委任状の設定](sepa-direct-debit-mandate.md)
        - [売掛金勘定の決算](close-accounts-receivable.md)
    :::column-end:::
:::row-end:::


## <a name="set-up-credit-and-collections"></a>与信および回収の設定

売掛金勘定回収情報は、一元化されたビューである [回収] ページで集中管理します。 貸方および取立マネージャが回収を管理するには、この一元化されたビューを使用します。 回収代行業者は、定義済の回収基準を使用して生成された顧客リスト、または [顧客] ページから回収プロセスを開始できます。

[売掛金勘定の貸方転記および取立](collections-credit-accounts-receivable.md)

[売掛金勘定、貸方転記および取立のコンフィギュレーション](accounts-receivables-set-up-overview.md)

[与信および回収の設定](set-up-collections.md)

## <a name="set-up-payments-and-settlements"></a>支払と決済の設定

受取手形、現金、小切手、クレジット カード、電子支払などの複数の異なる支払タイプの使用を許可します。 

:::row:::
    :::column:::
        - [複数の割引期間にまたがる複数の請求書を決済するための顧客支払の使用](customer-payment-settle-multiple-invoices-multiple-discount-periods.md)
        - [売掛金勘定の集中支払](centralized-payments-accounts-receivable.md)
        - [一部の顧客支払の決済、および割引日より前の全額最終支払](../accounts-payable/settle-partial-customer-payment-or-final-payment-before-discount.md)
        - [割引日後の最終支払での割引日よりも前の一部の顧客支払の決済](settle-partial-customer-payment-before-discount-or-final-payment-after.md)
    :::column-end:::
    :::column:::
        - [訂正票で割引がある一部の顧客支払の決済](settle-partial-customer-payment-discounts-credit-notes.md)
        - [複数の割引期間を持つ一部の仕入先支払の決済](settle-partial-customer-payment-multiple-discount-periods.md)
        - [顧客への払戻し](reimburse-customers.md)
        - [一部金額の顧客支払](customer-payments-partial-amount.md)
    :::column-end:::
:::row-end:::


### <a name="additional-resources"></a>追加リソース

#### <a name="whats-new-and-in-development"></a>新機能および開発中の機能

リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/)を参照してください。 

#### <a name="blogs"></a>ブログ

売掛金勘定およびその他のソリューションに関する意見、ニュース、その他の情報については、[Microsoft Dynamics365 blog (Microsoft Dynamics 365 ブログ)](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise)を参照してください。

[Microsoft Dynamics AX product team blog (Microsoft Dynamics AX 製品チームのブログ)](https://blogs.msdn.microsoft.com/dax/) には、売掛金勘定に関する多くの投稿があります。 これらの投稿の一部は、以前のバージョンの売掛金勘定用に書かれたものですが、同じ概念が適用されます。 手順も、現在のバージョンと似ています。

[Microsoft Dynamics Operations Partner Community Blog (Microsoft Dynamics Operations パートナー コミュニティのブログ)](https://community.dynamics.com/partner/b/operationspartnercommunityblog) では、MBS Operations に関する最新情報とトレンドを知るための単一のリソースが Microsoft Dynamics パートナー向けに提供されています。

#### <a name="task-guides"></a>タスク ガイド
Finance and Operations には、タスク ガイドとして使用できる追加のヘルプが用意されています。 タスク ガイドにアクセスするには、ページの [ヘルプ] ボタンをクリックします。

#### <a name="videos"></a>ビデオ

[Microsoft Dynamics 365 YouTube チャンネル](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) のハウツー ビデオをご覧ください。







