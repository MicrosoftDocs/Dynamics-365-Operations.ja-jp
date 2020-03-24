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
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 1ba4d09240888f0c533fb07614e75ffecea0742c
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124096"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="71948-103">消費税の二重通貨サポート</span><span class="sxs-lookup"><span data-stu-id="71948-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="71948-104">このトピックでは、消費税の二重通貨会計の拡張方法と、消費税の計算、転記および決済に対する影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="71948-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="71948-105">Dynamics 365 Finance 用の二重通貨機能は、バージョン 8.1 (2018 年 10 月) で導入されました。</span><span class="sxs-lookup"><span data-stu-id="71948-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="71948-106">これにより、レポートの通貨での会計項目の計算方法が変更されます。</span><span class="sxs-lookup"><span data-stu-id="71948-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="71948-107">以前のバージョンでは、トランザクションは次の順序でレポート通貨に変換されました。</span><span class="sxs-lookup"><span data-stu-id="71948-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="71948-108">トランザクションの合計がトランザクション通貨で計算 > トランザクション金額が会計通貨に換算 > 会計通貨金額がレポート通貨に変換</span><span class="sxs-lookup"><span data-stu-id="71948-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="71948-109">二重通貨機能を有効にすると、トランザクションは次の順序でレポート通貨に変換されます。</span><span class="sxs-lookup"><span data-stu-id="71948-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="71948-110">トランザクション通貨金額 > レポート通貨金額</span><span class="sxs-lookup"><span data-stu-id="71948-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="71948-111">二重通貨の詳細については、[二重通貨](dual-currency.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71948-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="71948-112">二重通貨のサポートにより、機能管理には次の 2 つの新機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="71948-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="71948-113">消費税変換 (バージョン 10.0.9 のリリース)</span><span class="sxs-lookup"><span data-stu-id="71948-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="71948-114">レポート通貨での税決済の自動残高 (バージョン 10.0.11 のリリース)</span><span class="sxs-lookup"><span data-stu-id="71948-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="71948-115">消費税の二重通貨サポートにより、税の通貨での税額が正確に計算され、会計通貨とレポートの通貨の両方で消費税精算残高が正確に計算されるようになります。</span><span class="sxs-lookup"><span data-stu-id="71948-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="71948-116">新しい機能は、プライベート プレビューの顧客で現在有効になっています。</span><span class="sxs-lookup"><span data-stu-id="71948-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="71948-117">機能を有効にするには、対応するチャネルを通じて Microsoft にサービス要求を生成します。</span><span class="sxs-lookup"><span data-stu-id="71948-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="71948-118">消費税の換算</span><span class="sxs-lookup"><span data-stu-id="71948-118">Sales tax conversion</span></span>

<span data-ttu-id="71948-119">**消費税変換**パラメータには、トランザクション通貨から税通貨に税金額を換算するためのオプションが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="71948-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="71948-120">会計通貨: パスは "トランザクション通貨での金額 > 会計通貨での金額 > 税通貨での金額"となります。</span><span class="sxs-lookup"><span data-stu-id="71948-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="71948-121">通貨換算では、会計通貨為替レートタイプ (元帳の設定で構成) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="71948-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="71948-122">レポート通貨: パスは "トランザクション通貨での金額 > レポート通貨での金額 > 税通貨での金額" となります。</span><span class="sxs-lookup"><span data-stu-id="71948-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="71948-123">通貨換算では、レポート通貨為替レートタイプ (元帳の設定で構成) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="71948-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="71948-124">例</span><span class="sxs-lookup"><span data-stu-id="71948-124">Example</span></span>

<span data-ttu-id="71948-125">この機能を実際に示す簡単な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="71948-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="71948-126">元帳および税の通貨の設定</span><span class="sxs-lookup"><span data-stu-id="71948-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="71948-127">トランザクション通貨</span><span class="sxs-lookup"><span data-stu-id="71948-127">Transaction currency</span></span> | <span data-ttu-id="71948-128">会計通貨</span><span class="sxs-lookup"><span data-stu-id="71948-128">Accounting currency</span></span> | <span data-ttu-id="71948-129">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="71948-129">Reporting currency</span></span> | <span data-ttu-id="71948-130">税通貨</span><span class="sxs-lookup"><span data-stu-id="71948-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="71948-131">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="71948-131">EUR</span></span>                  | <span data-ttu-id="71948-132">USD</span><span class="sxs-lookup"><span data-stu-id="71948-132">USD</span></span>                 | <span data-ttu-id="71948-133">GBP</span><span class="sxs-lookup"><span data-stu-id="71948-133">GBP</span></span>                | <span data-ttu-id="71948-134">GBP</span><span class="sxs-lookup"><span data-stu-id="71948-134">GBP</span></span>          |

<span data-ttu-id="71948-135">為替レート</span><span class="sxs-lookup"><span data-stu-id="71948-135">Exchange rate</span></span>

| <span data-ttu-id="71948-136">交換前通貨</span><span class="sxs-lookup"><span data-stu-id="71948-136">From currency</span></span> | <span data-ttu-id="71948-137">交換後通貨</span><span class="sxs-lookup"><span data-stu-id="71948-137">To currency</span></span> | <span data-ttu-id="71948-138">係数</span><span class="sxs-lookup"><span data-stu-id="71948-138">Factor</span></span> | <span data-ttu-id="71948-139">為替レート</span><span class="sxs-lookup"><span data-stu-id="71948-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="71948-140">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="71948-140">EUR</span></span>           | <span data-ttu-id="71948-141">USD</span><span class="sxs-lookup"><span data-stu-id="71948-141">USD</span></span>         | <span data-ttu-id="71948-142">1</span><span class="sxs-lookup"><span data-stu-id="71948-142">1</span></span>      | <span data-ttu-id="71948-143">1.11</span><span class="sxs-lookup"><span data-stu-id="71948-143">1.11</span></span>          |
| <span data-ttu-id="71948-144">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="71948-144">EUR</span></span>           | <span data-ttu-id="71948-145">GBP</span><span class="sxs-lookup"><span data-stu-id="71948-145">GBP</span></span>         | <span data-ttu-id="71948-146">1</span><span class="sxs-lookup"><span data-stu-id="71948-146">1</span></span>      | <span data-ttu-id="71948-147">0.83</span><span class="sxs-lookup"><span data-stu-id="71948-147">0.83</span></span>          |
| <span data-ttu-id="71948-148">USD</span><span class="sxs-lookup"><span data-stu-id="71948-148">USD</span></span>           | <span data-ttu-id="71948-149">GBP</span><span class="sxs-lookup"><span data-stu-id="71948-149">GBP</span></span>         | <span data-ttu-id="71948-150">1</span><span class="sxs-lookup"><span data-stu-id="71948-150">1</span></span>      | <span data-ttu-id="71948-151">0.75</span><span class="sxs-lookup"><span data-stu-id="71948-151">0.75</span></span>          |

<span data-ttu-id="71948-152">さまざまなパラメーター オプションにおける税額計算</span><span class="sxs-lookup"><span data-stu-id="71948-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="71948-153">税額 = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="71948-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="71948-154">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="71948-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="71948-155">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="71948-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="71948-156">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="71948-156">Accounting currency (USD)</span></span> | <span data-ttu-id="71948-157">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="71948-158">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="71948-159">会計通貨</span><span class="sxs-lookup"><span data-stu-id="71948-159">Accounting currency</span></span>             | <span data-ttu-id="71948-160">100</span><span class="sxs-lookup"><span data-stu-id="71948-160">100</span></span>                        | <span data-ttu-id="71948-161">111</span><span class="sxs-lookup"><span data-stu-id="71948-161">111</span></span>                       | <span data-ttu-id="71948-162">83</span><span class="sxs-lookup"><span data-stu-id="71948-162">83</span></span>                       | <span data-ttu-id="71948-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="71948-163">**83.25**</span></span>          |
| <span data-ttu-id="71948-164">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="71948-164">Reporting currency</span></span>              | <span data-ttu-id="71948-165">100</span><span class="sxs-lookup"><span data-stu-id="71948-165">100</span></span>                        | <span data-ttu-id="71948-166">111</span><span class="sxs-lookup"><span data-stu-id="71948-166">111</span></span>                       | <span data-ttu-id="71948-167">83</span><span class="sxs-lookup"><span data-stu-id="71948-167">83</span></span>                       | <span data-ttu-id="71948-168">**83**</span><span class="sxs-lookup"><span data-stu-id="71948-168">**83**</span></span>             |

<span data-ttu-id="71948-169">このパラメーターは、税務当局が満たすコンプライアンス要件に基づいてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="71948-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="71948-170">アップグレードの考慮事項</span><span class="sxs-lookup"><span data-stu-id="71948-170">Upgrade Consideration</span></span>

<span data-ttu-id="71948-171">この機能は、新しいトランザクションに対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="71948-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="71948-172">TAXTRANS テーブルに既に保存されているが決済されていない税トランザクションの場合、売上税転記の時点での為替レートが既に存在しないため、税額は再計算されません。</span><span class="sxs-lookup"><span data-stu-id="71948-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="71948-173">上記のシナリオを回避するには、未決済の税トランザクションが含まれない新しい (クリーンな) 税決済期間でこのパラメーター値を変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="71948-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="71948-174">税決済期間の途中でこの値を変更するには、このパラメーター値を変更する前に、現在の税決済期間に対して、"決済および転記" プログラムを実行してください。</span><span class="sxs-lookup"><span data-stu-id="71948-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="71948-175">レポート通貨の税額の追跡</span><span class="sxs-lookup"><span data-stu-id="71948-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="71948-176">税関連のテーブルに 3 つの新しいフィールドが追加され、レポート通貨での金額を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="71948-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="71948-177">これらのフィールドは、TAXUNCOMMITTED テーブルと TAXTRANS テーブルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71948-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="71948-178">TaxAmountRep: レポート通貨による税額</span><span class="sxs-lookup"><span data-stu-id="71948-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="71948-179">TaxBaseAmountRep: レポート通貨による税基準額</span><span class="sxs-lookup"><span data-stu-id="71948-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="71948-180">TaxInCostPriceRep: レポート通貨による非課税金額</span><span class="sxs-lookup"><span data-stu-id="71948-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="71948-181">TAXUNCOMMITTED テーブルにのみ保存されているがまだ転記されていない税の場合、TAXTRANS テーブルに転記および保存する時点でレポート通貨の税額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="71948-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="71948-182">このリリースには、レポート通貨で税額を示すレポートおよびフォームに対する変更は含まれません。</span><span class="sxs-lookup"><span data-stu-id="71948-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="71948-183">レポートおよびフォームに対する変更は、将来のリリースで提供されます。</span><span class="sxs-lookup"><span data-stu-id="71948-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="71948-184">レポート通貨での税決済の自動残高 </span><span class="sxs-lookup"><span data-stu-id="71948-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="71948-185">消費税の換算パスが "会計通貨" になっていたり、1 つの税決済期間での為替レートの変更など、特定の理由で税決済がレポート通貨に分散されていない場合、元帳の設定で税額の差異を調整し、コンフィギュレーションされた実現利益/損失の会計に相殺するために、自動的に勘定項目を生成します。</span><span class="sxs-lookup"><span data-stu-id="71948-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="71948-186">前の例を使用して、この機能を実際に確認するには、転記時の TAXTRANS テーブルのデータが次のようになっているものとします。</span><span class="sxs-lookup"><span data-stu-id="71948-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="71948-187">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="71948-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="71948-188">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="71948-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="71948-189">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="71948-189">Accounting currency (USD)</span></span> | <span data-ttu-id="71948-190">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="71948-191">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="71948-192">会計通貨</span><span class="sxs-lookup"><span data-stu-id="71948-192">Accounting currency</span></span>             | <span data-ttu-id="71948-193">100</span><span class="sxs-lookup"><span data-stu-id="71948-193">100</span></span>                        | <span data-ttu-id="71948-194">111</span><span class="sxs-lookup"><span data-stu-id="71948-194">111</span></span>                       | <span data-ttu-id="71948-195">83</span><span class="sxs-lookup"><span data-stu-id="71948-195">83</span></span>                       | <span data-ttu-id="71948-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="71948-196">**83.25**</span></span>          |
| <span data-ttu-id="71948-197">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="71948-197">Reporting currency</span></span>              | <span data-ttu-id="71948-198">100</span><span class="sxs-lookup"><span data-stu-id="71948-198">100</span></span>                        | <span data-ttu-id="71948-199">111</span><span class="sxs-lookup"><span data-stu-id="71948-199">111</span></span>                       | <span data-ttu-id="71948-200">83</span><span class="sxs-lookup"><span data-stu-id="71948-200">83</span></span>                       | <span data-ttu-id="71948-201">**83**</span><span class="sxs-lookup"><span data-stu-id="71948-201">**83**</span></span>             |

<span data-ttu-id="71948-202">月末に消費税決済プログラムを実行する場合、勘定項目は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="71948-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="71948-203">シナリオ: 消費税換算 = "会計通貨"</span><span class="sxs-lookup"><span data-stu-id="71948-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="71948-204">主勘定</span><span class="sxs-lookup"><span data-stu-id="71948-204">Main account</span></span>           | <span data-ttu-id="71948-205">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="71948-206">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="71948-206">Accounting currency (USD)</span></span> | <span data-ttu-id="71948-207">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="71948-208">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="71948-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="71948-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="71948-209">-83.25</span></span>                     | <span data-ttu-id="71948-210">-111</span><span class="sxs-lookup"><span data-stu-id="71948-210">-111</span></span>                      | <span data-ttu-id="71948-211">-83.25</span><span class="sxs-lookup"><span data-stu-id="71948-211">-83.25</span></span>                   |
| <span data-ttu-id="71948-212">税決済</span><span class="sxs-lookup"><span data-stu-id="71948-212">Tax Settlement</span></span>         | <span data-ttu-id="71948-213">83.25</span><span class="sxs-lookup"><span data-stu-id="71948-213">83.25</span></span>                      | <span data-ttu-id="71948-214">111</span><span class="sxs-lookup"><span data-stu-id="71948-214">111</span></span>                       | <span data-ttu-id="71948-215">83.25</span><span class="sxs-lookup"><span data-stu-id="71948-215">83.25</span></span>                    |
| <span data-ttu-id="71948-216">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="71948-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="71948-217">0</span><span class="sxs-lookup"><span data-stu-id="71948-217">0</span></span>                          | <span data-ttu-id="71948-218">0</span><span class="sxs-lookup"><span data-stu-id="71948-218">0</span></span>                         | <span data-ttu-id="71948-219">-0.25</span><span class="sxs-lookup"><span data-stu-id="71948-219">-0.25</span></span>                    |
| <span data-ttu-id="71948-220">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="71948-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="71948-221">0</span><span class="sxs-lookup"><span data-stu-id="71948-221">0</span></span>                          | <span data-ttu-id="71948-222">0</span><span class="sxs-lookup"><span data-stu-id="71948-222">0</span></span>                         | <span data-ttu-id="71948-223">0.25</span><span class="sxs-lookup"><span data-stu-id="71948-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="71948-224">シナリオ: 消費税換算 = "レポート通貨"</span><span class="sxs-lookup"><span data-stu-id="71948-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="71948-225">主勘定</span><span class="sxs-lookup"><span data-stu-id="71948-225">Main account</span></span>           | <span data-ttu-id="71948-226">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="71948-227">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="71948-227">Accounting currency (USD)</span></span> | <span data-ttu-id="71948-228">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="71948-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="71948-229">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="71948-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="71948-230">-83</span><span class="sxs-lookup"><span data-stu-id="71948-230">-83</span></span>                        | <span data-ttu-id="71948-231">-110.67</span><span class="sxs-lookup"><span data-stu-id="71948-231">-110.67</span></span>                   | <span data-ttu-id="71948-232">-83</span><span class="sxs-lookup"><span data-stu-id="71948-232">-83</span></span>                      |
| <span data-ttu-id="71948-233">税決済</span><span class="sxs-lookup"><span data-stu-id="71948-233">Tax Settlement</span></span>         | <span data-ttu-id="71948-234">83</span><span class="sxs-lookup"><span data-stu-id="71948-234">83</span></span>                         | <span data-ttu-id="71948-235">110.67</span><span class="sxs-lookup"><span data-stu-id="71948-235">110.67</span></span>                    | <span data-ttu-id="71948-236">83</span><span class="sxs-lookup"><span data-stu-id="71948-236">83</span></span>                       |
| <span data-ttu-id="71948-237">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="71948-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="71948-238">0</span><span class="sxs-lookup"><span data-stu-id="71948-238">0</span></span>                          | <span data-ttu-id="71948-239">0.33</span><span class="sxs-lookup"><span data-stu-id="71948-239">0.33</span></span>                      | <span data-ttu-id="71948-240">0</span><span class="sxs-lookup"><span data-stu-id="71948-240">0</span></span>                        |
| <span data-ttu-id="71948-241">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="71948-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="71948-242">0</span><span class="sxs-lookup"><span data-stu-id="71948-242">0</span></span>                          | <span data-ttu-id="71948-243">-0.33</span><span class="sxs-lookup"><span data-stu-id="71948-243">-0.33</span></span>                     | <span data-ttu-id="71948-244">0</span><span class="sxs-lookup"><span data-stu-id="71948-244">0</span></span>                        |



<span data-ttu-id="71948-245">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="71948-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="71948-246">二重通貨</span><span class="sxs-lookup"><span data-stu-id="71948-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="71948-247">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="71948-247">Sales tax overview</span></span>](indirect-taxes-overview.md)

