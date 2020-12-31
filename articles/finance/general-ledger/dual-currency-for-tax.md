---
title: 税金の二重通貨サポート
description: このトピックでは、税務ドメインでの二重通貨会計機能の拡張方法と、税金の計算および転記に対する影響について説明します
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 9e5db8e4bbd14aa30196e3be617cdfcb72c091fd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445144"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="38ff3-103">消費税の二重通貨サポート</span><span class="sxs-lookup"><span data-stu-id="38ff3-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="38ff3-104">このトピックでは、消費税の二重通貨会計の拡張方法と、消費税の計算、転記および決済に対する影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="38ff3-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="38ff3-105">Dynamics 365 Finance 用の二重通貨機能は、バージョン 8.1 (2018 年 10 月) で導入されました。</span><span class="sxs-lookup"><span data-stu-id="38ff3-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="38ff3-106">これにより、レポートの通貨での会計項目の計算方法が変更されます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="38ff3-107">以前のバージョンでは、トランザクションは次の順序でレポート通貨に変換されました。</span><span class="sxs-lookup"><span data-stu-id="38ff3-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="38ff3-108">トランザクションの合計がトランザクション通貨で計算 > トランザクション金額が会計通貨に換算 > 会計通貨金額がレポート通貨に変換</span><span class="sxs-lookup"><span data-stu-id="38ff3-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="38ff3-109">二重通貨機能を有効にすると、トランザクションは次の順序でレポート通貨に変換されます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="38ff3-110">トランザクション通貨金額 > レポート通貨金額</span><span class="sxs-lookup"><span data-stu-id="38ff3-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="38ff3-111">二重通貨の詳細については、[二重通貨](dual-currency.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38ff3-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="38ff3-112">二重通貨のサポートにより、機能管理には次の 2 つの新機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="38ff3-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="38ff3-113">消費税変換 (バージョン 10.0.9 のリリース)</span><span class="sxs-lookup"><span data-stu-id="38ff3-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="38ff3-114">レポート通貨での税決済の自動残高 (バージョン 10.0.11 のリリース)</span><span class="sxs-lookup"><span data-stu-id="38ff3-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="38ff3-115">消費税の二重通貨サポートにより、税の通貨での税額が正確に計算され、会計通貨とレポートの通貨の両方で消費税精算残高が正確に計算されるようになります。</span><span class="sxs-lookup"><span data-stu-id="38ff3-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="38ff3-116">消費税の換算</span><span class="sxs-lookup"><span data-stu-id="38ff3-116">Sales tax conversion</span></span>

<span data-ttu-id="38ff3-117">**消費税変換** パラメータには、トランザクション通貨から税通貨に税金額を換算するためのオプションが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="38ff3-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="38ff3-118">会計通貨: パスは "トランザクション通貨での金額 > 会計通貨での金額 > 税通貨での金額"となります。</span><span class="sxs-lookup"><span data-stu-id="38ff3-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="38ff3-119">通貨換算では、会計通貨為替レートタイプ (元帳の設定で構成) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="38ff3-120">レポート通貨: パスは "トランザクション通貨での金額 > レポート通貨での金額 > 税通貨での金額" となります。</span><span class="sxs-lookup"><span data-stu-id="38ff3-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="38ff3-121">通貨換算では、レポート通貨為替レートタイプ (元帳の設定で構成) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="38ff3-122">例</span><span class="sxs-lookup"><span data-stu-id="38ff3-122">Example</span></span>

<span data-ttu-id="38ff3-123">この機能を実際に示す簡単な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="38ff3-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="38ff3-124">元帳および税の通貨の設定</span><span class="sxs-lookup"><span data-stu-id="38ff3-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="38ff3-125">トランザクション通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-125">Transaction currency</span></span> | <span data-ttu-id="38ff3-126">会計通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-126">Accounting currency</span></span> | <span data-ttu-id="38ff3-127">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-127">Reporting currency</span></span> | <span data-ttu-id="38ff3-128">税通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="38ff3-129">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="38ff3-129">EUR</span></span>                  | <span data-ttu-id="38ff3-130">USD</span><span class="sxs-lookup"><span data-stu-id="38ff3-130">USD</span></span>                 | <span data-ttu-id="38ff3-131">GBP</span><span class="sxs-lookup"><span data-stu-id="38ff3-131">GBP</span></span>                | <span data-ttu-id="38ff3-132">GBP</span><span class="sxs-lookup"><span data-stu-id="38ff3-132">GBP</span></span>          |

<span data-ttu-id="38ff3-133">為替レート</span><span class="sxs-lookup"><span data-stu-id="38ff3-133">Exchange rate</span></span>

| <span data-ttu-id="38ff3-134">交換前通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-134">From currency</span></span> | <span data-ttu-id="38ff3-135">交換後通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-135">To currency</span></span> | <span data-ttu-id="38ff3-136">係数</span><span class="sxs-lookup"><span data-stu-id="38ff3-136">Factor</span></span> | <span data-ttu-id="38ff3-137">為替レート</span><span class="sxs-lookup"><span data-stu-id="38ff3-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="38ff3-138">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="38ff3-138">EUR</span></span>           | <span data-ttu-id="38ff3-139">USD</span><span class="sxs-lookup"><span data-stu-id="38ff3-139">USD</span></span>         | <span data-ttu-id="38ff3-140">1</span><span class="sxs-lookup"><span data-stu-id="38ff3-140">1</span></span>      | <span data-ttu-id="38ff3-141">1.11</span><span class="sxs-lookup"><span data-stu-id="38ff3-141">1.11</span></span>          |
| <span data-ttu-id="38ff3-142">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="38ff3-142">EUR</span></span>           | <span data-ttu-id="38ff3-143">GBP</span><span class="sxs-lookup"><span data-stu-id="38ff3-143">GBP</span></span>         | <span data-ttu-id="38ff3-144">1</span><span class="sxs-lookup"><span data-stu-id="38ff3-144">1</span></span>      | <span data-ttu-id="38ff3-145">0.83</span><span class="sxs-lookup"><span data-stu-id="38ff3-145">0.83</span></span>          |
| <span data-ttu-id="38ff3-146">USD</span><span class="sxs-lookup"><span data-stu-id="38ff3-146">USD</span></span>           | <span data-ttu-id="38ff3-147">GBP</span><span class="sxs-lookup"><span data-stu-id="38ff3-147">GBP</span></span>         | <span data-ttu-id="38ff3-148">1</span><span class="sxs-lookup"><span data-stu-id="38ff3-148">1</span></span>      | <span data-ttu-id="38ff3-149">0.75</span><span class="sxs-lookup"><span data-stu-id="38ff3-149">0.75</span></span>          |

<span data-ttu-id="38ff3-150">さまざまなパラメーター オプションにおける税額計算</span><span class="sxs-lookup"><span data-stu-id="38ff3-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="38ff3-151">税額 = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="38ff3-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="38ff3-152">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="38ff3-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="38ff3-153">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="38ff3-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="38ff3-154">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="38ff3-154">Accounting currency (USD)</span></span> | <span data-ttu-id="38ff3-155">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="38ff3-156">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="38ff3-157">会計通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-157">Accounting currency</span></span>             | <span data-ttu-id="38ff3-158">100</span><span class="sxs-lookup"><span data-stu-id="38ff3-158">100</span></span>                        | <span data-ttu-id="38ff3-159">111</span><span class="sxs-lookup"><span data-stu-id="38ff3-159">111</span></span>                       | <span data-ttu-id="38ff3-160">83</span><span class="sxs-lookup"><span data-stu-id="38ff3-160">83</span></span>                       | <span data-ttu-id="38ff3-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="38ff3-161">**83.25**</span></span>          |
| <span data-ttu-id="38ff3-162">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-162">Reporting currency</span></span>              | <span data-ttu-id="38ff3-163">100</span><span class="sxs-lookup"><span data-stu-id="38ff3-163">100</span></span>                        | <span data-ttu-id="38ff3-164">111</span><span class="sxs-lookup"><span data-stu-id="38ff3-164">111</span></span>                       | <span data-ttu-id="38ff3-165">83</span><span class="sxs-lookup"><span data-stu-id="38ff3-165">83</span></span>                       | <span data-ttu-id="38ff3-166">**83**</span><span class="sxs-lookup"><span data-stu-id="38ff3-166">**83**</span></span>             |

<span data-ttu-id="38ff3-167">このパラメーターは、税務当局が満たすコンプライアンス要件に基づいてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="38ff3-168">アップグレードの考慮事項</span><span class="sxs-lookup"><span data-stu-id="38ff3-168">Upgrade Consideration</span></span>

<span data-ttu-id="38ff3-169">この機能は、新しいトランザクションに対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="38ff3-170">TAXTRANS テーブルに既に保存されているが決済されていない税トランザクションの場合、売上税転記の時点での為替レートが既に存在しないため、税額は再計算されません。</span><span class="sxs-lookup"><span data-stu-id="38ff3-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="38ff3-171">上記のシナリオを回避するには、未決済の税トランザクションが含まれない新しい (クリーンな) 税決済期間でこのパラメーター値を変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="38ff3-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="38ff3-172">税決済期間の途中でこの値を変更するには、このパラメーター値を変更する前に、現在の税決済期間に対して、"決済および転記" プログラムを実行してください。</span><span class="sxs-lookup"><span data-stu-id="38ff3-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="38ff3-173">レポート通貨の税額の追跡</span><span class="sxs-lookup"><span data-stu-id="38ff3-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="38ff3-174">税関連のテーブルに 3 つの新しいフィールドが追加され、レポート通貨での金額を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="38ff3-175">これらのフィールドは、TAXUNCOMMITTED テーブルと TAXTRANS テーブルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="38ff3-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="38ff3-176">TaxAmountRep: レポート通貨による税額</span><span class="sxs-lookup"><span data-stu-id="38ff3-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="38ff3-177">TaxBaseAmountRep: レポート通貨による税基準額</span><span class="sxs-lookup"><span data-stu-id="38ff3-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="38ff3-178">TaxInCostPriceRep: レポート通貨による非課税金額</span><span class="sxs-lookup"><span data-stu-id="38ff3-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="38ff3-179">TAXUNCOMMITTED テーブルにのみ保存されているがまだ転記されていない税の場合、TAXTRANS テーブルに転記および保存する時点でレポート通貨の税額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="38ff3-180">このリリースには、レポート通貨で税額を示すレポートおよびフォームに対する変更は含まれません。</span><span class="sxs-lookup"><span data-stu-id="38ff3-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="38ff3-181">レポートおよびフォームに対する変更は、将来のリリースで提供されます。</span><span class="sxs-lookup"><span data-stu-id="38ff3-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="38ff3-182">レポート通貨での税決済の自動残高 </span><span class="sxs-lookup"><span data-stu-id="38ff3-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="38ff3-183">消費税の換算パスが "会計通貨" になっていたり、1 つの税決済期間での為替レートの変更など、特定の理由で税決済がレポート通貨に分散されていない場合、元帳の設定で税額の差異を調整し、コンフィギュレーションされた実現利益/損失の会計に相殺するために、自動的に勘定項目を生成します。</span><span class="sxs-lookup"><span data-stu-id="38ff3-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="38ff3-184">前の例を使用して、この機能を実際に確認するには、転記時の TAXTRANS テーブルのデータが次のようになっているものとします。</span><span class="sxs-lookup"><span data-stu-id="38ff3-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="38ff3-185">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="38ff3-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="38ff3-186">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="38ff3-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="38ff3-187">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="38ff3-187">Accounting currency (USD)</span></span> | <span data-ttu-id="38ff3-188">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="38ff3-189">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="38ff3-190">会計通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-190">Accounting currency</span></span>             | <span data-ttu-id="38ff3-191">100</span><span class="sxs-lookup"><span data-stu-id="38ff3-191">100</span></span>                        | <span data-ttu-id="38ff3-192">111</span><span class="sxs-lookup"><span data-stu-id="38ff3-192">111</span></span>                       | <span data-ttu-id="38ff3-193">83</span><span class="sxs-lookup"><span data-stu-id="38ff3-193">83</span></span>                       | <span data-ttu-id="38ff3-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="38ff3-194">**83.25**</span></span>          |
| <span data-ttu-id="38ff3-195">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-195">Reporting currency</span></span>              | <span data-ttu-id="38ff3-196">100</span><span class="sxs-lookup"><span data-stu-id="38ff3-196">100</span></span>                        | <span data-ttu-id="38ff3-197">111</span><span class="sxs-lookup"><span data-stu-id="38ff3-197">111</span></span>                       | <span data-ttu-id="38ff3-198">83</span><span class="sxs-lookup"><span data-stu-id="38ff3-198">83</span></span>                       | <span data-ttu-id="38ff3-199">**83**</span><span class="sxs-lookup"><span data-stu-id="38ff3-199">**83**</span></span>             |

<span data-ttu-id="38ff3-200">月末に消費税決済プログラムを実行する場合、勘定項目は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="38ff3-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="38ff3-201">シナリオ: 消費税換算 = "会計通貨"</span><span class="sxs-lookup"><span data-stu-id="38ff3-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="38ff3-202">主勘定</span><span class="sxs-lookup"><span data-stu-id="38ff3-202">Main account</span></span>           | <span data-ttu-id="38ff3-203">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="38ff3-204">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="38ff3-204">Accounting currency (USD)</span></span> | <span data-ttu-id="38ff3-205">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="38ff3-206">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="38ff3-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="38ff3-207">-83.25</span><span class="sxs-lookup"><span data-stu-id="38ff3-207">-83.25</span></span>                     | <span data-ttu-id="38ff3-208">-111</span><span class="sxs-lookup"><span data-stu-id="38ff3-208">-111</span></span>                      | <span data-ttu-id="38ff3-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="38ff3-209">-83.25</span></span>                   |
| <span data-ttu-id="38ff3-210">税決済</span><span class="sxs-lookup"><span data-stu-id="38ff3-210">Tax Settlement</span></span>         | <span data-ttu-id="38ff3-211">83.25</span><span class="sxs-lookup"><span data-stu-id="38ff3-211">83.25</span></span>                      | <span data-ttu-id="38ff3-212">111</span><span class="sxs-lookup"><span data-stu-id="38ff3-212">111</span></span>                       | <span data-ttu-id="38ff3-213">83.25</span><span class="sxs-lookup"><span data-stu-id="38ff3-213">83.25</span></span>                    |
| <span data-ttu-id="38ff3-214">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="38ff3-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="38ff3-215">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-215">0</span></span>                          | <span data-ttu-id="38ff3-216">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-216">0</span></span>                         | <span data-ttu-id="38ff3-217">-0.25</span><span class="sxs-lookup"><span data-stu-id="38ff3-217">-0.25</span></span>                    |
| <span data-ttu-id="38ff3-218">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="38ff3-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="38ff3-219">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-219">0</span></span>                          | <span data-ttu-id="38ff3-220">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-220">0</span></span>                         | <span data-ttu-id="38ff3-221">0.25</span><span class="sxs-lookup"><span data-stu-id="38ff3-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="38ff3-222">シナリオ: 消費税換算 = "レポート通貨"</span><span class="sxs-lookup"><span data-stu-id="38ff3-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="38ff3-223">主勘定</span><span class="sxs-lookup"><span data-stu-id="38ff3-223">Main account</span></span>           | <span data-ttu-id="38ff3-224">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="38ff3-225">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="38ff3-225">Accounting currency (USD)</span></span> | <span data-ttu-id="38ff3-226">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="38ff3-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="38ff3-227">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="38ff3-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="38ff3-228">-83</span><span class="sxs-lookup"><span data-stu-id="38ff3-228">-83</span></span>                        | <span data-ttu-id="38ff3-229">-110.67</span><span class="sxs-lookup"><span data-stu-id="38ff3-229">-110.67</span></span>                   | <span data-ttu-id="38ff3-230">-83</span><span class="sxs-lookup"><span data-stu-id="38ff3-230">-83</span></span>                      |
| <span data-ttu-id="38ff3-231">税決済</span><span class="sxs-lookup"><span data-stu-id="38ff3-231">Tax Settlement</span></span>         | <span data-ttu-id="38ff3-232">83</span><span class="sxs-lookup"><span data-stu-id="38ff3-232">83</span></span>                         | <span data-ttu-id="38ff3-233">110.67</span><span class="sxs-lookup"><span data-stu-id="38ff3-233">110.67</span></span>                    | <span data-ttu-id="38ff3-234">83</span><span class="sxs-lookup"><span data-stu-id="38ff3-234">83</span></span>                       |
| <span data-ttu-id="38ff3-235">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="38ff3-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="38ff3-236">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-236">0</span></span>                          | <span data-ttu-id="38ff3-237">0.33</span><span class="sxs-lookup"><span data-stu-id="38ff3-237">0.33</span></span>                      | <span data-ttu-id="38ff3-238">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-238">0</span></span>                        |
| <span data-ttu-id="38ff3-239">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="38ff3-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="38ff3-240">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-240">0</span></span>                          | <span data-ttu-id="38ff3-241">-0.33</span><span class="sxs-lookup"><span data-stu-id="38ff3-241">-0.33</span></span>                     | <span data-ttu-id="38ff3-242">0</span><span class="sxs-lookup"><span data-stu-id="38ff3-242">0</span></span>                        |



<span data-ttu-id="38ff3-243">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="38ff3-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="38ff3-244">二重通貨</span><span class="sxs-lookup"><span data-stu-id="38ff3-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="38ff3-245">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="38ff3-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

