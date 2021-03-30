---
title: 税金の二重通貨サポート
description: このトピックでは、税務ドメインでの二重通貨会計機能の拡張方法と、税金の計算および転記に対する影響について説明します
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3f7ca56fef636431e152b2db424f1f972a507721
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212208"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="505d3-103">消費税の二重通貨サポート</span><span class="sxs-lookup"><span data-stu-id="505d3-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="505d3-104">このトピックでは、消費税の二重通貨会計の拡張方法と、消費税の計算、転記および決済に対する影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="505d3-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="505d3-105">Dynamics 365 Finance 用の二重通貨機能は、バージョン 8.1 (2018 年 10 月) で導入されました。</span><span class="sxs-lookup"><span data-stu-id="505d3-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="505d3-106">これにより、レポートの通貨での会計項目の計算方法が変更されます。</span><span class="sxs-lookup"><span data-stu-id="505d3-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="505d3-107">以前のバージョンでは、トランザクションは次の順序でレポート通貨に変換されました。</span><span class="sxs-lookup"><span data-stu-id="505d3-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="505d3-108">トランザクションの合計がトランザクション通貨で計算 > トランザクション金額が会計通貨に換算 > 会計通貨金額がレポート通貨に変換</span><span class="sxs-lookup"><span data-stu-id="505d3-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="505d3-109">二重通貨機能を有効にすると、トランザクションは次の順序でレポート通貨に変換されます。</span><span class="sxs-lookup"><span data-stu-id="505d3-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="505d3-110">トランザクション通貨金額 > レポート通貨金額</span><span class="sxs-lookup"><span data-stu-id="505d3-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="505d3-111">二重通貨の詳細については、[二重通貨](dual-currency.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="505d3-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="505d3-112">二重通貨のサポートにより、機能管理には次の 2 つの新機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="505d3-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="505d3-113">消費税変換 (バージョン 10.0.13 での新機能)</span><span class="sxs-lookup"><span data-stu-id="505d3-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="505d3-114">消費税の二重通貨サポートにより、税の通貨での税額が正確に計算され、会計通貨とレポートの通貨の両方で消費税精算残高が正確に計算されるようになります。</span><span class="sxs-lookup"><span data-stu-id="505d3-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="505d3-115">消費税の換算</span><span class="sxs-lookup"><span data-stu-id="505d3-115">Sales tax conversion</span></span>

<span data-ttu-id="505d3-116">**消費税変換** パラメータには、トランザクション通貨から税通貨に税金額を換算するためのオプションが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="505d3-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="505d3-117">会計通貨: パスは "トランザクション通貨での金額 > 会計通貨での金額 > 税通貨での金額"となります。</span><span class="sxs-lookup"><span data-stu-id="505d3-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="505d3-118">通貨換算では、会計通貨為替レートタイプ (元帳の設定で構成したもの) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="505d3-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="505d3-119">レポート通貨: パスは "トランザクション通貨での金額 > レポート通貨での金額 > 税通貨での金額" となります。</span><span class="sxs-lookup"><span data-stu-id="505d3-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="505d3-120">通貨換算では、レポート通貨為替レートタイプ (元帳の設定で構成したもの) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="505d3-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="505d3-121">例</span><span class="sxs-lookup"><span data-stu-id="505d3-121">Example</span></span>

<span data-ttu-id="505d3-122">この機能を実際に示す簡単な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="505d3-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="505d3-123">元帳および税の通貨の設定</span><span class="sxs-lookup"><span data-stu-id="505d3-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="505d3-124">トランザクション通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-124">Transaction currency</span></span> | <span data-ttu-id="505d3-125">会計通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-125">Accounting currency</span></span> | <span data-ttu-id="505d3-126">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-126">Reporting currency</span></span> | <span data-ttu-id="505d3-127">税通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="505d3-128">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="505d3-128">EUR</span></span>                  | <span data-ttu-id="505d3-129">USD</span><span class="sxs-lookup"><span data-stu-id="505d3-129">USD</span></span>                 | <span data-ttu-id="505d3-130">GBP</span><span class="sxs-lookup"><span data-stu-id="505d3-130">GBP</span></span>                | <span data-ttu-id="505d3-131">GBP</span><span class="sxs-lookup"><span data-stu-id="505d3-131">GBP</span></span>          |

<span data-ttu-id="505d3-132">為替レート</span><span class="sxs-lookup"><span data-stu-id="505d3-132">Exchange rate</span></span>

| <span data-ttu-id="505d3-133">交換前通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-133">From currency</span></span> | <span data-ttu-id="505d3-134">交換後通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-134">To currency</span></span> | <span data-ttu-id="505d3-135">係数</span><span class="sxs-lookup"><span data-stu-id="505d3-135">Factor</span></span> | <span data-ttu-id="505d3-136">為替レート</span><span class="sxs-lookup"><span data-stu-id="505d3-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="505d3-137">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="505d3-137">EUR</span></span>           | <span data-ttu-id="505d3-138">USD</span><span class="sxs-lookup"><span data-stu-id="505d3-138">USD</span></span>         | <span data-ttu-id="505d3-139">1</span><span class="sxs-lookup"><span data-stu-id="505d3-139">1</span></span>      | <span data-ttu-id="505d3-140">1.11</span><span class="sxs-lookup"><span data-stu-id="505d3-140">1.11</span></span>          |
| <span data-ttu-id="505d3-141">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="505d3-141">EUR</span></span>           | <span data-ttu-id="505d3-142">GBP</span><span class="sxs-lookup"><span data-stu-id="505d3-142">GBP</span></span>         | <span data-ttu-id="505d3-143">1</span><span class="sxs-lookup"><span data-stu-id="505d3-143">1</span></span>      | <span data-ttu-id="505d3-144">0.83</span><span class="sxs-lookup"><span data-stu-id="505d3-144">0.83</span></span>          |
| <span data-ttu-id="505d3-145">USD</span><span class="sxs-lookup"><span data-stu-id="505d3-145">USD</span></span>           | <span data-ttu-id="505d3-146">GBP</span><span class="sxs-lookup"><span data-stu-id="505d3-146">GBP</span></span>         | <span data-ttu-id="505d3-147">1</span><span class="sxs-lookup"><span data-stu-id="505d3-147">1</span></span>      | <span data-ttu-id="505d3-148">0.75</span><span class="sxs-lookup"><span data-stu-id="505d3-148">0.75</span></span>          |

<span data-ttu-id="505d3-149">さまざまなパラメーター オプションにおける税額計算</span><span class="sxs-lookup"><span data-stu-id="505d3-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="505d3-150">税額 = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="505d3-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="505d3-151">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="505d3-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="505d3-152">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="505d3-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="505d3-153">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="505d3-153">Accounting currency (USD)</span></span> | <span data-ttu-id="505d3-154">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="505d3-155">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="505d3-156">会計通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-156">Accounting currency</span></span>             | <span data-ttu-id="505d3-157">100</span><span class="sxs-lookup"><span data-stu-id="505d3-157">100</span></span>                        | <span data-ttu-id="505d3-158">111</span><span class="sxs-lookup"><span data-stu-id="505d3-158">111</span></span>                       | <span data-ttu-id="505d3-159">83</span><span class="sxs-lookup"><span data-stu-id="505d3-159">83</span></span>                       | <span data-ttu-id="505d3-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="505d3-160">**83.25**</span></span>          |
| <span data-ttu-id="505d3-161">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-161">Reporting currency</span></span>              | <span data-ttu-id="505d3-162">100</span><span class="sxs-lookup"><span data-stu-id="505d3-162">100</span></span>                        | <span data-ttu-id="505d3-163">111</span><span class="sxs-lookup"><span data-stu-id="505d3-163">111</span></span>                       | <span data-ttu-id="505d3-164">83</span><span class="sxs-lookup"><span data-stu-id="505d3-164">83</span></span>                       | <span data-ttu-id="505d3-165">**83**</span><span class="sxs-lookup"><span data-stu-id="505d3-165">**83**</span></span>             |

<span data-ttu-id="505d3-166">このパラメーターは、税務当局が満たすコンプライアンス要件に基づいてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="505d3-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="505d3-167">アップグレードの考慮事項</span><span class="sxs-lookup"><span data-stu-id="505d3-167">Upgrade Consideration</span></span>

<span data-ttu-id="505d3-168">この機能は、新しいトランザクションに対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="505d3-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="505d3-169">TAXTRANS テーブルに既に保存されているが決済されていない税トランザクションの場合、売上税転記の時点での為替レートが既に存在しないため、税額は再計算されません。</span><span class="sxs-lookup"><span data-stu-id="505d3-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="505d3-170">上記のシナリオを回避するには、未決済の税トランザクションが含まれない新しい (クリーンな) 税決済期間でこのパラメーター値を変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="505d3-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="505d3-171">税決済期間の途中でこの値を変更するには、このパラメーター値を変更する前に、現在の税決済期間に対して、"決済および転記" プログラムを実行してください。</span><span class="sxs-lookup"><span data-stu-id="505d3-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="505d3-172">レポート通貨の税額の追跡</span><span class="sxs-lookup"><span data-stu-id="505d3-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="505d3-173">税関連のテーブルに 3 つの新しいフィールドが追加され、レポート通貨での金額を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="505d3-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="505d3-174">これらのフィールドは、TAXUNCOMMITTED テーブルと TAXTRANS テーブルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="505d3-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="505d3-175">TaxAmountRep: レポート通貨による税額</span><span class="sxs-lookup"><span data-stu-id="505d3-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="505d3-176">TaxBaseAmountRep: レポート通貨による税基準額</span><span class="sxs-lookup"><span data-stu-id="505d3-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="505d3-177">TaxInCostPriceRep: レポート通貨による非課税金額</span><span class="sxs-lookup"><span data-stu-id="505d3-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="505d3-178">TAXUNCOMMITTED テーブルにのみ保存されているがまだ転記されていない税の場合、TAXTRANS テーブルに転記および保存する時点でレポート通貨の税額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="505d3-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="505d3-179">このリリースには、レポート通貨で税額を示すレポートおよびフォームに対する変更は含まれません。</span><span class="sxs-lookup"><span data-stu-id="505d3-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="505d3-180">レポートおよびフォームに対する変更は、将来のリリースで提供されます。</span><span class="sxs-lookup"><span data-stu-id="505d3-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="505d3-181">レポート通貨での税決済の自動残高 </span><span class="sxs-lookup"><span data-stu-id="505d3-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="505d3-182">消費税の換算パスが "会計通貨" になっていたり、ひとつの税決済期間での為替レートの変更など、特定の理由で税決済がレポート通貨に分散されていない場合、自動的に会計入力を生成して税額差異を調整し、元帳設定で設定した為替決済の損益勘定と相殺します。</span><span class="sxs-lookup"><span data-stu-id="505d3-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="505d3-183">前の例を使用して、この機能を実際に確認するには、転記時の TAXTRANS テーブルのデータが次のようになっているものとします。</span><span class="sxs-lookup"><span data-stu-id="505d3-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="505d3-184">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="505d3-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="505d3-185">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="505d3-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="505d3-186">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="505d3-186">Accounting currency (USD)</span></span> | <span data-ttu-id="505d3-187">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="505d3-188">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="505d3-189">会計通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-189">Accounting currency</span></span>             | <span data-ttu-id="505d3-190">100</span><span class="sxs-lookup"><span data-stu-id="505d3-190">100</span></span>                        | <span data-ttu-id="505d3-191">111</span><span class="sxs-lookup"><span data-stu-id="505d3-191">111</span></span>                       | <span data-ttu-id="505d3-192">83</span><span class="sxs-lookup"><span data-stu-id="505d3-192">83</span></span>                       | <span data-ttu-id="505d3-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="505d3-193">**83.25**</span></span>          |
| <span data-ttu-id="505d3-194">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-194">Reporting currency</span></span>              | <span data-ttu-id="505d3-195">100</span><span class="sxs-lookup"><span data-stu-id="505d3-195">100</span></span>                        | <span data-ttu-id="505d3-196">111</span><span class="sxs-lookup"><span data-stu-id="505d3-196">111</span></span>                       | <span data-ttu-id="505d3-197">83</span><span class="sxs-lookup"><span data-stu-id="505d3-197">83</span></span>                       | <span data-ttu-id="505d3-198">**83**</span><span class="sxs-lookup"><span data-stu-id="505d3-198">**83**</span></span>             |

<span data-ttu-id="505d3-199">月末に消費税決済プログラムを実行する場合、勘定項目は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="505d3-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="505d3-200">シナリオ: 消費税換算 = "会計通貨"</span><span class="sxs-lookup"><span data-stu-id="505d3-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="505d3-201">主勘定</span><span class="sxs-lookup"><span data-stu-id="505d3-201">Main account</span></span>           | <span data-ttu-id="505d3-202">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="505d3-203">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="505d3-203">Accounting currency (USD)</span></span> | <span data-ttu-id="505d3-204">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="505d3-205">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="505d3-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="505d3-206">-83.25</span><span class="sxs-lookup"><span data-stu-id="505d3-206">-83.25</span></span>                     | <span data-ttu-id="505d3-207">-111</span><span class="sxs-lookup"><span data-stu-id="505d3-207">-111</span></span>                      | <span data-ttu-id="505d3-208">-83.25</span><span class="sxs-lookup"><span data-stu-id="505d3-208">-83.25</span></span>                   |
| <span data-ttu-id="505d3-209">税決済</span><span class="sxs-lookup"><span data-stu-id="505d3-209">Tax Settlement</span></span>         | <span data-ttu-id="505d3-210">83.25</span><span class="sxs-lookup"><span data-stu-id="505d3-210">83.25</span></span>                      | <span data-ttu-id="505d3-211">111</span><span class="sxs-lookup"><span data-stu-id="505d3-211">111</span></span>                       | <span data-ttu-id="505d3-212">83.25</span><span class="sxs-lookup"><span data-stu-id="505d3-212">83.25</span></span>                    |
| <span data-ttu-id="505d3-213">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="505d3-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="505d3-214">0</span><span class="sxs-lookup"><span data-stu-id="505d3-214">0</span></span>                          | <span data-ttu-id="505d3-215">0</span><span class="sxs-lookup"><span data-stu-id="505d3-215">0</span></span>                         | <span data-ttu-id="505d3-216">-0.25</span><span class="sxs-lookup"><span data-stu-id="505d3-216">-0.25</span></span>                    |
| <span data-ttu-id="505d3-217">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="505d3-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="505d3-218">0</span><span class="sxs-lookup"><span data-stu-id="505d3-218">0</span></span>                          | <span data-ttu-id="505d3-219">0</span><span class="sxs-lookup"><span data-stu-id="505d3-219">0</span></span>                         | <span data-ttu-id="505d3-220">0.25</span><span class="sxs-lookup"><span data-stu-id="505d3-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="505d3-221">シナリオ: 消費税換算 = "レポート通貨"</span><span class="sxs-lookup"><span data-stu-id="505d3-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="505d3-222">主勘定</span><span class="sxs-lookup"><span data-stu-id="505d3-222">Main account</span></span>           | <span data-ttu-id="505d3-223">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="505d3-224">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="505d3-224">Accounting currency (USD)</span></span> | <span data-ttu-id="505d3-225">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="505d3-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="505d3-226">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="505d3-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="505d3-227">-83</span><span class="sxs-lookup"><span data-stu-id="505d3-227">-83</span></span>                        | <span data-ttu-id="505d3-228">-110.67</span><span class="sxs-lookup"><span data-stu-id="505d3-228">-110.67</span></span>                   | <span data-ttu-id="505d3-229">-83</span><span class="sxs-lookup"><span data-stu-id="505d3-229">-83</span></span>                      |
| <span data-ttu-id="505d3-230">税決済</span><span class="sxs-lookup"><span data-stu-id="505d3-230">Tax Settlement</span></span>         | <span data-ttu-id="505d3-231">83</span><span class="sxs-lookup"><span data-stu-id="505d3-231">83</span></span>                         | <span data-ttu-id="505d3-232">110.67</span><span class="sxs-lookup"><span data-stu-id="505d3-232">110.67</span></span>                    | <span data-ttu-id="505d3-233">83</span><span class="sxs-lookup"><span data-stu-id="505d3-233">83</span></span>                       |
| <span data-ttu-id="505d3-234">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="505d3-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="505d3-235">0</span><span class="sxs-lookup"><span data-stu-id="505d3-235">0</span></span>                          | <span data-ttu-id="505d3-236">0.33</span><span class="sxs-lookup"><span data-stu-id="505d3-236">0.33</span></span>                      | <span data-ttu-id="505d3-237">0</span><span class="sxs-lookup"><span data-stu-id="505d3-237">0</span></span>                        |
| <span data-ttu-id="505d3-238">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="505d3-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="505d3-239">0</span><span class="sxs-lookup"><span data-stu-id="505d3-239">0</span></span>                          | <span data-ttu-id="505d3-240">-0.33</span><span class="sxs-lookup"><span data-stu-id="505d3-240">-0.33</span></span>                     | <span data-ttu-id="505d3-241">0</span><span class="sxs-lookup"><span data-stu-id="505d3-241">0</span></span>                        |



<span data-ttu-id="505d3-242">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="505d3-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="505d3-243">二重通貨</span><span class="sxs-lookup"><span data-stu-id="505d3-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="505d3-244">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="505d3-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]