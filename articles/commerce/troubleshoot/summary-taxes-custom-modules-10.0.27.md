---
title: カスタマイズした注文集計モジュールを使用すると、注文集計の小計に請求金額に対する税金が含まれない
description: この記事では、カスタマイズした注文集計合計モジュールを使用すると、'価格に消費税が含まれる' シナリオで、注文集計の小計に請求金額の税が含まれない場合の、トラブルシューティング ガイドを定期用します。
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848840"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>カスタマイズした注文集計モジュールを使用すると、注文集計の小計に請求金額に対する税金が含まれない

この記事では、カスタマイズした注文集計合計モジュールを使用すると、'価格に消費税が含まれる' シナリオで、注文集計の小計に請求金額の税が含まれない場合の、トラブルシューティング ガイドを定期用します。

## <a name="description"></a>Description

Microsoft Dynamics 365 Commerce バージョン 10.0.27 リリースでは、'価格に消費税が含まれる' シナリオに次の変更が行われ、eコマース サイト ページ全体に、注文集計モジュールでの一貫性のあるエクスペリエンスを提供します。

- 新しいフィールドが 2 つ追加されました: **TaxOnShippingCharge** と **TaxOnNonShippingCharges**。
- **GetSalesOrderBySalesId** と **GetSalesOrderByTransactionId** アプリケーション プログラミング インターフェイス (API) は、'価格に消費税が含まれる' シナリオ次のフィールドに対する正確な値を持っています。

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

ただし、カスタマイズした注文集計モジュールを使用している場合、これらの違いは、請求金額の税を含まないことで、注文集計の小計の値に影響する可能性があります。

## <a name="resolution"></a>解決策

カスタマイズした注文集計モジュールを使用している場合、Commerce Version 10.0.27 以降の '価格に消費税が含まれる' シナリオに加えた変更を継承したくなければ、このセクションの手順に従ってください。

**salesTransaction.SubtotalAmount** および **salesTransaction.SubtotalAmountWithoutTax** フィールドの以前の (バージョン 10.0.27 より前の) 注文集計の動作に戻すと、請求税金額の合計請求税額 (**TaxOnShippingCharge** と **TaxOnNonShippingCharges**) が小計金額 (**SubtotalAmount** と **SubtotalAmountWithoutTax**) に含めて復元されます。

以前の注文集計動作に戻すには、次の手順に従います。

1. Commerce headquarters で、Commerce パラメーター ページを開きます (**Retail と Commerce \> Headquarters の設定 \> パラメーター \> Commerce パラメーター**)。
1. 左側のナビゲーション ウィンドウで、**コンフィギュレーション パラメーター** を選択します。
1. 次のコンフィギュレーション パラメータを追加し、それぞれの値を **true** に設定します。

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** コンフィギュレーション パラメータを以前使用したことがあり、**order.NetAmountWithoutTax** プロパティで同じ動作を維持する場合は、**IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** コンフィギュレーション パラメータも追加して、その値を **true** に設定する必要があります。

## <a name="additional-resources"></a>追加リソース

[注文概要で税の分割情報を非表示にする](../hide-taxes-breakup.md)
