---
title: 税金の二重通貨サポート
description: このトピックでは、税務ドメインでの二重通貨会計機能の拡張方法と、税金の計算および転記に対する影響について説明します
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3673642729aa41fa3c00a09fe8fe205edd0624c7
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088468"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="444e8-103">消費税の二重通貨サポート</span><span class="sxs-lookup"><span data-stu-id="444e8-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="444e8-104">このトピックでは、消費税の二重通貨会計の拡張方法と、消費税の計算、転記および決済に対する影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="444e8-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="444e8-105">Dynamics 365 Finance 用の二重通貨機能は、バージョン 8.1 (2018 年 10 月) で導入されました。</span><span class="sxs-lookup"><span data-stu-id="444e8-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="444e8-106">これにより、レポートの通貨での会計項目の計算方法が変更されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="444e8-107">以前のバージョンでは、トランザクションは次の順序でレポート通貨に変換されました。</span><span class="sxs-lookup"><span data-stu-id="444e8-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="444e8-108">トランザクションの合計がトランザクション通貨で計算 > トランザクション金額が会計通貨に換算 > 会計通貨金額がレポート通貨に変換</span><span class="sxs-lookup"><span data-stu-id="444e8-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="444e8-109">二重通貨機能を有効にすると、トランザクションは次の順序でレポート通貨に変換されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="444e8-110">トランザクション通貨金額 > レポート通貨金額</span><span class="sxs-lookup"><span data-stu-id="444e8-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="444e8-111">二重通貨の詳細については、[二重通貨](dual-currency.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="444e8-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="444e8-112">二重通貨のサポートにより、機能管理には次の 2 つの新機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="444e8-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="444e8-113">消費税変換 (バージョン 10.0.13 での新機能)</span><span class="sxs-lookup"><span data-stu-id="444e8-113">Sales tax conversion (new in version 10.0.13)</span></span>
- <span data-ttu-id="444e8-114">消費税精算のための実現通貨調整損益勘定の分析コードの入力 (バージョン10.0.17の新機能)</span><span class="sxs-lookup"><span data-stu-id="444e8-114">Enter financial dimensions in the realized currency adjustment profit/loss accounts for sales tax settlement (new in version 10.0.17)</span></span>

<span data-ttu-id="444e8-115">消費税の二重通貨サポートにより、税の通貨での税額が正確に計算され、会計通貨とレポートの通貨の両方で消費税精算残高が正確に計算されるようになります。</span><span class="sxs-lookup"><span data-stu-id="444e8-115">Dual currency support for sales taxes ensures that taxes are accurately calculated in the tax currency, and that the sales tax settlement balance is accurately calculated in both the accounting currency and the reporting currency.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="444e8-116">消費税の換算</span><span class="sxs-lookup"><span data-stu-id="444e8-116">Sales tax conversion</span></span>

<span data-ttu-id="444e8-117">**消費税変換** パラメータには、トランザクション通貨から税通貨に税金額を換算するためのオプションが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="444e8-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="444e8-118">会計通貨: パスは "トランザクション通貨での金額 > 会計通貨での金額 > 税通貨での金額"となります。</span><span class="sxs-lookup"><span data-stu-id="444e8-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="444e8-119">通貨換算では、会計通貨為替レートタイプ (元帳の設定で構成したもの) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-119">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="444e8-120">レポート通貨: パスは "トランザクション通貨での金額 > レポート通貨での金額 > 税通貨での金額" となります。</span><span class="sxs-lookup"><span data-stu-id="444e8-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="444e8-121">通貨換算では、レポート通貨為替レートタイプ (元帳の設定で構成したもの) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-121">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="444e8-122">例</span><span class="sxs-lookup"><span data-stu-id="444e8-122">Example</span></span>

<span data-ttu-id="444e8-123">この機能を実際に示す簡単な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="444e8-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="444e8-124">元帳および税の通貨の設定</span><span class="sxs-lookup"><span data-stu-id="444e8-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="444e8-125">トランザクション通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-125">Transaction currency</span></span> | <span data-ttu-id="444e8-126">会計通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-126">Accounting currency</span></span> | <span data-ttu-id="444e8-127">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-127">Reporting currency</span></span> | <span data-ttu-id="444e8-128">税通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="444e8-129">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="444e8-129">EUR</span></span>                  | <span data-ttu-id="444e8-130">USD</span><span class="sxs-lookup"><span data-stu-id="444e8-130">USD</span></span>                 | <span data-ttu-id="444e8-131">GBP</span><span class="sxs-lookup"><span data-stu-id="444e8-131">GBP</span></span>                | <span data-ttu-id="444e8-132">GBP</span><span class="sxs-lookup"><span data-stu-id="444e8-132">GBP</span></span>          |

<span data-ttu-id="444e8-133">為替レート</span><span class="sxs-lookup"><span data-stu-id="444e8-133">Exchange rate</span></span>

| <span data-ttu-id="444e8-134">交換前通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-134">From currency</span></span> | <span data-ttu-id="444e8-135">交換後通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-135">To currency</span></span> | <span data-ttu-id="444e8-136">係数</span><span class="sxs-lookup"><span data-stu-id="444e8-136">Factor</span></span> | <span data-ttu-id="444e8-137">為替レート</span><span class="sxs-lookup"><span data-stu-id="444e8-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="444e8-138">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="444e8-138">EUR</span></span>           | <span data-ttu-id="444e8-139">USD</span><span class="sxs-lookup"><span data-stu-id="444e8-139">USD</span></span>         | <span data-ttu-id="444e8-140">1</span><span class="sxs-lookup"><span data-stu-id="444e8-140">1</span></span>      | <span data-ttu-id="444e8-141">1.11</span><span class="sxs-lookup"><span data-stu-id="444e8-141">1.11</span></span>          |
| <span data-ttu-id="444e8-142">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="444e8-142">EUR</span></span>           | <span data-ttu-id="444e8-143">GBP</span><span class="sxs-lookup"><span data-stu-id="444e8-143">GBP</span></span>         | <span data-ttu-id="444e8-144">1</span><span class="sxs-lookup"><span data-stu-id="444e8-144">1</span></span>      | <span data-ttu-id="444e8-145">0.83</span><span class="sxs-lookup"><span data-stu-id="444e8-145">0.83</span></span>          |
| <span data-ttu-id="444e8-146">USD</span><span class="sxs-lookup"><span data-stu-id="444e8-146">USD</span></span>           | <span data-ttu-id="444e8-147">GBP</span><span class="sxs-lookup"><span data-stu-id="444e8-147">GBP</span></span>         | <span data-ttu-id="444e8-148">1</span><span class="sxs-lookup"><span data-stu-id="444e8-148">1</span></span>      | <span data-ttu-id="444e8-149">0.75</span><span class="sxs-lookup"><span data-stu-id="444e8-149">0.75</span></span>          |

<span data-ttu-id="444e8-150">さまざまなパラメーター オプションにおける税額計算</span><span class="sxs-lookup"><span data-stu-id="444e8-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="444e8-151">税額 = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="444e8-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="444e8-152">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="444e8-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="444e8-153">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="444e8-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="444e8-154">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="444e8-154">Accounting currency (USD)</span></span> | <span data-ttu-id="444e8-155">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="444e8-156">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="444e8-157">会計通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-157">Accounting currency</span></span>             | <span data-ttu-id="444e8-158">100</span><span class="sxs-lookup"><span data-stu-id="444e8-158">100</span></span>                        | <span data-ttu-id="444e8-159">111</span><span class="sxs-lookup"><span data-stu-id="444e8-159">111</span></span>                       | <span data-ttu-id="444e8-160">83</span><span class="sxs-lookup"><span data-stu-id="444e8-160">83</span></span>                       | <span data-ttu-id="444e8-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="444e8-161">**83.25**</span></span>          |
| <span data-ttu-id="444e8-162">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-162">Reporting currency</span></span>              | <span data-ttu-id="444e8-163">100</span><span class="sxs-lookup"><span data-stu-id="444e8-163">100</span></span>                        | <span data-ttu-id="444e8-164">111</span><span class="sxs-lookup"><span data-stu-id="444e8-164">111</span></span>                       | <span data-ttu-id="444e8-165">83</span><span class="sxs-lookup"><span data-stu-id="444e8-165">83</span></span>                       | <span data-ttu-id="444e8-166">**83**</span><span class="sxs-lookup"><span data-stu-id="444e8-166">**83**</span></span>             |

<span data-ttu-id="444e8-167">このパラメーターは、税務当局が満たすコンプライアンス要件に基づいてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="444e8-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="444e8-168">アップグレードの考慮事項</span><span class="sxs-lookup"><span data-stu-id="444e8-168">Upgrade Consideration</span></span>

<span data-ttu-id="444e8-169">この機能は、新しいトランザクションに対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="444e8-170">TAXTRANS テーブルに既に保存されているが決済されていない税トランザクションの場合、売上税転記の時点での為替レートが既に存在しないため、税額は再計算されません。</span><span class="sxs-lookup"><span data-stu-id="444e8-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="444e8-171">上記のシナリオを回避するには、未決済の税トランザクションが含まれない新しい (クリーンな) 税決済期間でこのパラメーター値を変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="444e8-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="444e8-172">税決済期間の途中でこの値を変更するには、このパラメーター値を変更する前に、現在の税決済期間に対して、"決済および転記" プログラムを実行してください。</span><span class="sxs-lookup"><span data-stu-id="444e8-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>

<span data-ttu-id="444e8-173">この機能により、通貨交換による損益を明確にする会計項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-173">This feature will add accounting entries that clarify gains and losses from currency exchanges.</span></span> <span data-ttu-id="444e8-174">消費税の精算時に再評価を行う際には、実現通貨調整の損益勘定で入力します。</span><span class="sxs-lookup"><span data-stu-id="444e8-174">The entries will be made in the realized currency adjustment profit and loss accounts when revaluation is done during sales tax settlement.</span></span> <span data-ttu-id="444e8-175">詳細については、このトピックの後半の [レポート通貨での税決済の自動残高](#tax-settlement-auto-balance-in-reporting-currency)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="444e8-175">For more information, see the [Tax settlement auto-balance in reporting currency](#tax-settlement-auto-balance-in-reporting-currency) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="444e8-176">決済時には、貸借対照表の勘定科目である売上税勘定から財務分析コードの情報を取得し、損益計算書の勘定科目である通貨調整損益勘定に入力されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-176">During settlement, information for financial dimensions is taken from sales tax accounts, which are balance sheet accounts, and entered in currency adjustment profit and loss accounts, which are profit and loss statement accounts.</span></span> <span data-ttu-id="444e8-177">貸借対照表の勘定科目と損益計算書の勘定科目では、財務分析コードの値の制限が異なるため、決済や消費税の後処理の際にエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="444e8-177">Because restrictions on the value of financial dimensions differ between balance sheet accounts and profit and loss statement accounts, an error can occur during the Settle and post sales tax process.</span></span> <span data-ttu-id="444e8-178">勘定構造を変更する必要が生じしないように、「消費税決済の実現通貨調整損益勘定に財務分析コードを設定する」機能をオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="444e8-178">To avoid having to modify account structures, you can turn on the "Populate financial dimensions to the realized currency adjustment profits/loss accounts for sales tax settlement" feature.</span></span> <span data-ttu-id="444e8-179">この機能により、通貨調整損益勘定への財務分析コードの派生が強制的に行われます。</span><span class="sxs-lookup"><span data-stu-id="444e8-179">This feature will force the derivation of financial dimensions to currency adjustment profits/loss accounts.</span></span> 

## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="444e8-180">レポート通貨の税額の追跡</span><span class="sxs-lookup"><span data-stu-id="444e8-180">Track reporting currency tax amount</span></span>

<span data-ttu-id="444e8-181">税関連のテーブルに 3 つの新しいフィールドが追加され、レポート通貨での金額を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="444e8-181">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="444e8-182">これらのフィールドは、TAXUNCOMMITTED テーブルと TAXTRANS テーブルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="444e8-182">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="444e8-183">TaxAmountRep: レポート通貨による税額</span><span class="sxs-lookup"><span data-stu-id="444e8-183">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="444e8-184">TaxBaseAmountRep: レポート通貨による税基準額</span><span class="sxs-lookup"><span data-stu-id="444e8-184">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="444e8-185">TaxInCostPriceRep: レポート通貨による非課税金額</span><span class="sxs-lookup"><span data-stu-id="444e8-185">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="444e8-186">TAXUNCOMMITTED テーブルにのみ保存されているがまだ転記されていない税の場合、TAXTRANS テーブルに転記および保存する時点でレポート通貨の税額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-186">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="444e8-187">このリリースには、レポート通貨で税額を示すレポートおよびフォームに対する変更は含まれません。</span><span class="sxs-lookup"><span data-stu-id="444e8-187">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="444e8-188">レポートおよびフォームに対する変更は、将来のリリースで提供されます。</span><span class="sxs-lookup"><span data-stu-id="444e8-188">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="444e8-189">レポート通貨での税決済の自動残高 </span><span class="sxs-lookup"><span data-stu-id="444e8-189">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="444e8-190">消費税の換算パスが "会計通貨" になっていたり、ひとつの税決済期間での為替レートの変更など、特定の理由で税決済がレポート通貨に分散されていない場合、自動的に会計入力を生成して税額差異を調整し、元帳設定で設定した為替決済の損益勘定と相殺します。</span><span class="sxs-lookup"><span data-stu-id="444e8-190">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="444e8-191">前述の例を使用して、この機能を実際に確認するには、転記時の TAXTRANS テーブルのデータが次のようになっているものとします。</span><span class="sxs-lookup"><span data-stu-id="444e8-191">Using the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="444e8-192">消費税変換パラメーター</span><span class="sxs-lookup"><span data-stu-id="444e8-192">Sales tax conversion parameters</span></span> | <span data-ttu-id="444e8-193">トランザクション通貨 (EUR)</span><span class="sxs-lookup"><span data-stu-id="444e8-193">Transaction currency (EUR)</span></span> | <span data-ttu-id="444e8-194">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="444e8-194">Accounting currency (USD)</span></span> | <span data-ttu-id="444e8-195">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-195">Reporting currency (GBP)</span></span> | <span data-ttu-id="444e8-196">税通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-196">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="444e8-197">会計通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-197">Accounting currency</span></span>             | <span data-ttu-id="444e8-198">100</span><span class="sxs-lookup"><span data-stu-id="444e8-198">100</span></span>                        | <span data-ttu-id="444e8-199">111</span><span class="sxs-lookup"><span data-stu-id="444e8-199">111</span></span>                       | <span data-ttu-id="444e8-200">83</span><span class="sxs-lookup"><span data-stu-id="444e8-200">83</span></span>                       | <span data-ttu-id="444e8-201">**83.25**</span><span class="sxs-lookup"><span data-stu-id="444e8-201">**83.25**</span></span>          |
| <span data-ttu-id="444e8-202">レポート通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-202">Reporting currency</span></span>              | <span data-ttu-id="444e8-203">100</span><span class="sxs-lookup"><span data-stu-id="444e8-203">100</span></span>                        | <span data-ttu-id="444e8-204">111</span><span class="sxs-lookup"><span data-stu-id="444e8-204">111</span></span>                       | <span data-ttu-id="444e8-205">83</span><span class="sxs-lookup"><span data-stu-id="444e8-205">83</span></span>                       | <span data-ttu-id="444e8-206">**83**</span><span class="sxs-lookup"><span data-stu-id="444e8-206">**83**</span></span>             |

<span data-ttu-id="444e8-207">月末に消費税決済プログラムを実行する場合、勘定項目は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="444e8-207">When you run the sales tax settlement program at month-end, the accounting entry will be as follows.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="444e8-208">シナリオ: 消費税換算 = "会計通貨"</span><span class="sxs-lookup"><span data-stu-id="444e8-208">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="444e8-209">主勘定</span><span class="sxs-lookup"><span data-stu-id="444e8-209">Main account</span></span>           | <span data-ttu-id="444e8-210">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-210">Transaction currency (GBP)</span></span> | <span data-ttu-id="444e8-211">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="444e8-211">Accounting currency (USD)</span></span> | <span data-ttu-id="444e8-212">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-212">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="444e8-213">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="444e8-213">Tax Payable/Receivable</span></span> | <span data-ttu-id="444e8-214">-83.25</span><span class="sxs-lookup"><span data-stu-id="444e8-214">-83.25</span></span>                     | <span data-ttu-id="444e8-215">-111</span><span class="sxs-lookup"><span data-stu-id="444e8-215">-111</span></span>                      | <span data-ttu-id="444e8-216">-83.25</span><span class="sxs-lookup"><span data-stu-id="444e8-216">-83.25</span></span>                   |
| <span data-ttu-id="444e8-217">税決済</span><span class="sxs-lookup"><span data-stu-id="444e8-217">Tax Settlement</span></span>         | <span data-ttu-id="444e8-218">83.25</span><span class="sxs-lookup"><span data-stu-id="444e8-218">83.25</span></span>                      | <span data-ttu-id="444e8-219">111</span><span class="sxs-lookup"><span data-stu-id="444e8-219">111</span></span>                       | <span data-ttu-id="444e8-220">83.25</span><span class="sxs-lookup"><span data-stu-id="444e8-220">83.25</span></span>                    |
| <span data-ttu-id="444e8-221">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="444e8-221">Realized Gain/Loss</span></span>     | <span data-ttu-id="444e8-222">0</span><span class="sxs-lookup"><span data-stu-id="444e8-222">0</span></span>                          | <span data-ttu-id="444e8-223">0</span><span class="sxs-lookup"><span data-stu-id="444e8-223">0</span></span>                         | <span data-ttu-id="444e8-224">-0.25</span><span class="sxs-lookup"><span data-stu-id="444e8-224">-0.25</span></span>                    |
| <span data-ttu-id="444e8-225">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="444e8-225">Tax Payable/Receivable</span></span> | <span data-ttu-id="444e8-226">0</span><span class="sxs-lookup"><span data-stu-id="444e8-226">0</span></span>                          | <span data-ttu-id="444e8-227">0</span><span class="sxs-lookup"><span data-stu-id="444e8-227">0</span></span>                         | <span data-ttu-id="444e8-228">0.25</span><span class="sxs-lookup"><span data-stu-id="444e8-228">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="444e8-229">シナリオ: 消費税換算 = "レポート通貨"</span><span class="sxs-lookup"><span data-stu-id="444e8-229">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="444e8-230">主勘定</span><span class="sxs-lookup"><span data-stu-id="444e8-230">Main account</span></span>           | <span data-ttu-id="444e8-231">トランザクション通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-231">Transaction currency (GBP)</span></span> | <span data-ttu-id="444e8-232">会計通貨 (USD)</span><span class="sxs-lookup"><span data-stu-id="444e8-232">Accounting currency (USD)</span></span> | <span data-ttu-id="444e8-233">レポート通貨 (GBP)</span><span class="sxs-lookup"><span data-stu-id="444e8-233">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="444e8-234">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="444e8-234">Tax Payable/Receivable</span></span> | <span data-ttu-id="444e8-235">-83</span><span class="sxs-lookup"><span data-stu-id="444e8-235">-83</span></span>                        | <span data-ttu-id="444e8-236">-110.67</span><span class="sxs-lookup"><span data-stu-id="444e8-236">-110.67</span></span>                   | <span data-ttu-id="444e8-237">-83</span><span class="sxs-lookup"><span data-stu-id="444e8-237">-83</span></span>                      |
| <span data-ttu-id="444e8-238">税決済</span><span class="sxs-lookup"><span data-stu-id="444e8-238">Tax Settlement</span></span>         | <span data-ttu-id="444e8-239">83</span><span class="sxs-lookup"><span data-stu-id="444e8-239">83</span></span>                         | <span data-ttu-id="444e8-240">110.67</span><span class="sxs-lookup"><span data-stu-id="444e8-240">110.67</span></span>                    | <span data-ttu-id="444e8-241">83</span><span class="sxs-lookup"><span data-stu-id="444e8-241">83</span></span>                       |
| <span data-ttu-id="444e8-242">実現利益/損失</span><span class="sxs-lookup"><span data-stu-id="444e8-242">Realized Gain/Loss</span></span>     | <span data-ttu-id="444e8-243">0</span><span class="sxs-lookup"><span data-stu-id="444e8-243">0</span></span>                          | <span data-ttu-id="444e8-244">0.33</span><span class="sxs-lookup"><span data-stu-id="444e8-244">0.33</span></span>                      | <span data-ttu-id="444e8-245">0</span><span class="sxs-lookup"><span data-stu-id="444e8-245">0</span></span>                        |
| <span data-ttu-id="444e8-246">税支払/収入</span><span class="sxs-lookup"><span data-stu-id="444e8-246">Tax Payable/Receivable</span></span> | <span data-ttu-id="444e8-247">0</span><span class="sxs-lookup"><span data-stu-id="444e8-247">0</span></span>                          | <span data-ttu-id="444e8-248">-0.33</span><span class="sxs-lookup"><span data-stu-id="444e8-248">-0.33</span></span>                     | <span data-ttu-id="444e8-249">0</span><span class="sxs-lookup"><span data-stu-id="444e8-249">0</span></span>                        |



<span data-ttu-id="444e8-250">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="444e8-250">For more information, see the following topics:</span></span>

- [<span data-ttu-id="444e8-251">二重通貨</span><span class="sxs-lookup"><span data-stu-id="444e8-251">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="444e8-252">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="444e8-252">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
