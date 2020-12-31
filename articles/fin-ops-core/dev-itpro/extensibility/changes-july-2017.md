---
title: Finance and Operations、Enterprise edition (2017 年 7 月) の拡張機能の変更
description: これは、(2017 年 7 月) に実装された拡張機能の一覧です。
author: FrankDahl
manager: AnnBe
ms.date: 11/08/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: f44ee8f345b5d0a494799bbf7b04ffda9f2c8a02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409269"
---
# <a name="extensibility-changes-in-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="95a00-103">Finance and Operations、Enterprise edition (2017 年 7 月) の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="95a00-103">Extensibility changes in Finance and Operations, Enterprise edition (July 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95a00-104">これは、Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="95a00-104">This is a list of extensibility features that were implemented in the Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span> <span data-ttu-id="95a00-105">このバージョンは 2017 年 7 月にリリースされ、ビルド番号は 7.2.11792.56024 です。</span><span class="sxs-lookup"><span data-stu-id="95a00-105">This version was released in July 2017 and has a build number of 7.2.11792.56024.</span></span> <span data-ttu-id="95a00-106">拡張性をサポートする変更スケジュールの詳細については、 [アプリケーション機能拡張ロードマップ](extensibility-roadmap.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="95a00-106">For more information about the schedule of changes that support extensibility, see [Application extensibility roadmap](extensibility-roadmap.md).</span></span>

## <a name="soft-sealed-application-models"></a><span data-ttu-id="95a00-107">ソフト シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-107">Soft-sealed application models</span></span>

<span data-ttu-id="95a00-108">以下のアプリケーション中間層モデルは、今回のリリースでソフト シールされました。</span><span class="sxs-lookup"><span data-stu-id="95a00-108">The following application middle-tier models were soft-sealed in this release.</span></span> <span data-ttu-id="95a00-109">これらのモデルのオーバーレイ コードは、コンパイル時に警告を生成します。</span><span class="sxs-lookup"><span data-stu-id="95a00-109">Overlayered code in these models will generate warnings on compilation.</span></span>

| <span data-ttu-id="95a00-110">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="95a00-110">Category</span></span>       | <span data-ttu-id="95a00-111">モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-111">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="95a00-112">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="95a00-112">Application Frameworks</span></span> | <span data-ttu-id="95a00-113">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="95a00-113">CaseManagement</span></span> |
| <span data-ttu-id="95a00-114">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="95a00-114">Application Frameworks</span></span> | <span data-ttu-id="95a00-115">Dimensions</span><span class="sxs-lookup"><span data-stu-id="95a00-115">Dimensions</span></span> |
| <span data-ttu-id="95a00-116">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="95a00-116">Application Frameworks</span></span> | <span data-ttu-id="95a00-117">Directory</span><span class="sxs-lookup"><span data-stu-id="95a00-117">Directory</span></span> |
| <span data-ttu-id="95a00-118">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="95a00-118">Application Frameworks</span></span> | <span data-ttu-id="95a00-119">Organization</span><span class="sxs-lookup"><span data-stu-id="95a00-119">Organization</span></span> |
| <span data-ttu-id="95a00-120">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="95a00-120">Application Frameworks</span></span> | <span data-ttu-id="95a00-121">Currency</span><span class="sxs-lookup"><span data-stu-id="95a00-121">Currency</span></span>|
| <span data-ttu-id="95a00-122">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="95a00-122">Application Frameworks</span></span> | <span data-ttu-id="95a00-123">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="95a00-123">ApplicationCommon</span></span>|
| <span data-ttu-id="95a00-124">HCM コア モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-124">HCM Core Models</span></span>| <span data-ttu-id="95a00-125">3817938</span><span class="sxs-lookup"><span data-stu-id="95a00-125">3817938</span></span>
|<span data-ttu-id="95a00-126">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-126">Tax Models</span></span> |<span data-ttu-id="95a00-127">Tax</span><span class="sxs-lookup"><span data-stu-id="95a00-127">Tax</span></span> |
|<span data-ttu-id="95a00-128">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-128">Tax Models</span></span> |<span data-ttu-id="95a00-129">Tax Books</span><span class="sxs-lookup"><span data-stu-id="95a00-129">Tax Books</span></span> |
|<span data-ttu-id="95a00-130">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-130">Tax Models</span></span> |<span data-ttu-id="95a00-131">Tax Books Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="95a00-131">Tax Books Application Suite Integration</span></span> |
|<span data-ttu-id="95a00-132">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-132">Tax Models</span></span> |<span data-ttu-id="95a00-133">Tax Engine Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="95a00-133">Tax Engine Application Suite Integration</span></span> |
|<span data-ttu-id="95a00-134">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-134">Tax Models</span></span> |<span data-ttu-id="95a00-135">Tax Engine Configuration</span><span class="sxs-lookup"><span data-stu-id="95a00-135">Tax Engine Configuration</span></span> |
|<span data-ttu-id="95a00-136">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-136">Tax Models</span></span> |<span data-ttu-id="95a00-137">Tax Engine Interface</span><span class="sxs-lookup"><span data-stu-id="95a00-137">Tax Engine Interface</span></span> |
|<span data-ttu-id="95a00-138">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-138">Tax Models</span></span> |<span data-ttu-id="95a00-139">Tax Engine Runtime Generation</span><span class="sxs-lookup"><span data-stu-id="95a00-139">Tax Engine Runtime Generation</span></span> |
|<span data-ttu-id="95a00-140">税モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-140">Tax Models</span></span> |<span data-ttu-id="95a00-141">TaxEngine</span><span class="sxs-lookup"><span data-stu-id="95a00-141">TaxEngine</span></span> |
| <span data-ttu-id="95a00-142">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-142">Source Document Models</span></span> |<span data-ttu-id="95a00-143">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="95a00-143">SourceDocumentation</span></span> |
| <span data-ttu-id="95a00-144">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-144">Source Document Models</span></span> |<span data-ttu-id="95a00-145">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="95a00-145">SourceDocumentationTypes</span></span> |
| <span data-ttu-id="95a00-146">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-146">Ledger Models</span></span> |<span data-ttu-id="95a00-147">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="95a00-147">GeneralLedger</span></span> |
| <span data-ttu-id="95a00-148">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-148">Ledger Models</span></span> |<span data-ttu-id="95a00-149">Ledger</span><span class="sxs-lookup"><span data-stu-id="95a00-149">Ledger</span></span> |
| <span data-ttu-id="95a00-150">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-150">Ledger Models</span></span> |<span data-ttu-id="95a00-151">Subledger</span><span class="sxs-lookup"><span data-stu-id="95a00-151">Subledger</span></span> |
| <span data-ttu-id="95a00-152">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-152">Middle Tier SCM Models</span></span> | <span data-ttu-id="95a00-153">CostAccounting</span><span class="sxs-lookup"><span data-stu-id="95a00-153">CostAccounting</span></span> |
| <span data-ttu-id="95a00-154">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-154">Middle Tier SCM Models</span></span> | <span data-ttu-id="95a00-155">CostAccountingAX</span><span class="sxs-lookup"><span data-stu-id="95a00-155">CostAccountingAX</span></span> |
| <span data-ttu-id="95a00-156">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-156">Middle Tier SCM Models</span></span> | <span data-ttu-id="95a00-157">SCMControls</span><span class="sxs-lookup"><span data-stu-id="95a00-157">SCMControls</span></span> |
| <span data-ttu-id="95a00-158">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-158">Middle Tier SCM Models</span></span> | <span data-ttu-id="95a00-159">SCMMobile</span><span class="sxs-lookup"><span data-stu-id="95a00-159">SCMMobile</span></span> |
| <span data-ttu-id="95a00-160">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-160">Middle Tier SCM Models</span></span> | <span data-ttu-id="95a00-161">UnitOfMeasure</span><span class="sxs-lookup"><span data-stu-id="95a00-161">UnitOfMeasure</span></span> |
| <span data-ttu-id="95a00-162">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-162">Middle Tier SCM Models</span></span> | <span data-ttu-id="95a00-163">WMSAdvancedMigration</span><span class="sxs-lookup"><span data-stu-id="95a00-163">WMSAdvancedMigration</span></span>|
| <span data-ttu-id="95a00-164">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-164">Middle Tier SCM Models</span></span> | <span data-ttu-id="95a00-165">InventoryDimensionConversion</span><span class="sxs-lookup"><span data-stu-id="95a00-165">InventoryDimensionConversion</span></span>|
| <span data-ttu-id="95a00-166">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="95a00-166">Workspaces</span></span>| <span data-ttu-id="95a00-167">ApplicationWorkspaces</span><span class="sxs-lookup"><span data-stu-id="95a00-167">ApplicationWorkspaces</span></span> |
| <span data-ttu-id="95a00-168">財務</span><span class="sxs-lookup"><span data-stu-id="95a00-168">Finance</span></span>| <span data-ttu-id="95a00-169">Fiscalbooks</span><span class="sxs-lookup"><span data-stu-id="95a00-169">Fiscalbooks</span></span> |
| <span data-ttu-id="95a00-170">管理ツール</span><span class="sxs-lookup"><span data-stu-id="95a00-170">Management tools</span></span> | <span data-ttu-id="95a00-171">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="95a00-171">DataUpgrade</span></span> |

## <a name="hard-sealed-application-models"></a><span data-ttu-id="95a00-172">ハード シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-172">Hard-sealed application models</span></span>

<span data-ttu-id="95a00-173">以下のアプリケーション中間層モデルは、今回のリリースでハード シールされました。</span><span class="sxs-lookup"><span data-stu-id="95a00-173">The following application middle-tier models were hard-sealed in this release.</span></span> <span data-ttu-id="95a00-174">これらのモデルのオーバーレイ コードは、コンパイル時にエラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="95a00-174">Overlayered code in these models will generate errors on compilation.</span></span>

| <span data-ttu-id="95a00-175">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="95a00-175">Category</span></span>       | <span data-ttu-id="95a00-176">モデル</span><span class="sxs-lookup"><span data-stu-id="95a00-176">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="95a00-177">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="95a00-177">Accounts Payable</span></span> | <span data-ttu-id="95a00-178">AccountsPayableMobile</span><span class="sxs-lookup"><span data-stu-id="95a00-178">AccountsPayableMobile</span></span> |
| <span data-ttu-id="95a00-179">財務</span><span class="sxs-lookup"><span data-stu-id="95a00-179">Finance</span></span> | <span data-ttu-id="95a00-180">FinancialReportingEntityStore</span><span class="sxs-lookup"><span data-stu-id="95a00-180">FinancialReportingEntityStore</span></span>|
| <span data-ttu-id="95a00-181">ツール</span><span class="sxs-lookup"><span data-stu-id="95a00-181">Tools</span></span> | <span data-ttu-id="95a00-182">PerformanceTool</span><span class="sxs-lookup"><span data-stu-id="95a00-182">PerformanceTool</span></span> |
| <span data-ttu-id="95a00-183">経費</span><span class="sxs-lookup"><span data-stu-id="95a00-183">Expenses</span></span> | <span data-ttu-id="95a00-184">ExpenseMobile</span><span class="sxs-lookup"><span data-stu-id="95a00-184">ExpenseMobile</span></span> |
| <span data-ttu-id="95a00-185">GER</span><span class="sxs-lookup"><span data-stu-id="95a00-185">GER</span></span> | <span data-ttu-id="95a00-186">ElectronicReporting</span><span class="sxs-lookup"><span data-stu-id="95a00-186">ElectronicReporting</span></span>|
|<span data-ttu-id="95a00-187">GER</span><span class="sxs-lookup"><span data-stu-id="95a00-187">GER</span></span> | <span data-ttu-id="95a00-188">ElectronicReportingCore</span><span class="sxs-lookup"><span data-stu-id="95a00-188">ElectronicReportingCore</span></span>|
|<span data-ttu-id="95a00-189">GER</span><span class="sxs-lookup"><span data-stu-id="95a00-189">GER</span></span> | <span data-ttu-id="95a00-190">Electronic Reporting Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="95a00-190">Electronic Reporting Application Suite Integration</span></span>|

## <a name="enumerations-that-are-now-extensible"></a><span data-ttu-id="95a00-191">拡張可能になった列挙型</span><span class="sxs-lookup"><span data-stu-id="95a00-191">Enumerations that are now extensible</span></span>

<span data-ttu-id="95a00-192">列挙の拡張をサポートするために以下の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="95a00-192">The following changes were made to support extending enumerations:</span></span>
- <span data-ttu-id="95a00-193">標準アプリケーションの多くの列挙が拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-193">Many enumerations in the standard application have been made extensible.</span></span> <span data-ttu-id="95a00-194">列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="95a00-194">An enumeration is made extensible by setting two properties on the enumeration.</span></span> <span data-ttu-id="95a00-195">**IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="95a00-195">The **IsExtensible** property is set to **Yes**, and the **UseEnumValue** property is set to **No**.</span></span> 
- <span data-ttu-id="95a00-196">一部の列挙型は状態を表します。</span><span class="sxs-lookup"><span data-stu-id="95a00-196">Some enumerations represent state.</span></span> <span data-ttu-id="95a00-197">拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="95a00-197">New façade methods have been added to help enable adding enumeration values by extension.</span></span> <span data-ttu-id="95a00-198">列挙型を拡張する方法については、 [拡張機能を使用した列挙値の追加](add-enum-value.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="95a00-198">For information about how to extend an enumeration, see [Add values to enums through extension](add-enum-value.md).</span></span>
- <span data-ttu-id="95a00-199">拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。</span><span class="sxs-lookup"><span data-stu-id="95a00-199">Some application code that uses enumerations was changed to support extensibility.</span></span> <span data-ttu-id="95a00-200">一般的な変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="95a00-200">Common changes include:</span></span>
    + <span data-ttu-id="95a00-201">ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。</span><span class="sxs-lookup"><span data-stu-id="95a00-201">Removing **throw** exception statements in the default case of a switch to allow post-event subscription.</span></span>
    + <span data-ttu-id="95a00-202">拡張機能の **SysExtension** サポートの追加。</span><span class="sxs-lookup"><span data-stu-id="95a00-202">Adding **SysExtension** support for extension.</span></span>
    + <span data-ttu-id="95a00-203">明示的なデリゲートの追加。</span><span class="sxs-lookup"><span data-stu-id="95a00-203">Adding explicit delegates.</span></span>


| <span data-ttu-id="95a00-204">列挙型</span><span class="sxs-lookup"><span data-stu-id="95a00-204">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="95a00-205">AgreementState</span><span class="sxs-lookup"><span data-stu-id="95a00-205">AgreementState</span></span>|
|<span data-ttu-id="95a00-206">AssetAccountType</span><span class="sxs-lookup"><span data-stu-id="95a00-206">AssetAccountType</span></span>|
|<span data-ttu-id="95a00-207">AssetTransTypeJournal</span><span class="sxs-lookup"><span data-stu-id="95a00-207">AssetTransTypeJournal</span></span>|
|<span data-ttu-id="95a00-208">BankAccountType</span><span class="sxs-lookup"><span data-stu-id="95a00-208">BankAccountType</span></span>|
|<span data-ttu-id="95a00-209">BankFormat</span><span class="sxs-lookup"><span data-stu-id="95a00-209">BankFormat</span></span>|
|<span data-ttu-id="95a00-210">BarcodeContentType</span><span class="sxs-lookup"><span data-stu-id="95a00-210">BarcodeContentType</span></span>|
|<span data-ttu-id="95a00-211">BarcodeCoverPageEntityType</span><span class="sxs-lookup"><span data-stu-id="95a00-211">BarcodeCoverPageEntityType</span></span>|
|<span data-ttu-id="95a00-212">BarcodeType</span><span class="sxs-lookup"><span data-stu-id="95a00-212">BarcodeType</span></span>|
|<span data-ttu-id="95a00-213">BOMCalcCostingVersionUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-213">BOMCalcCostingVersionUpdate</span></span>|
|<span data-ttu-id="95a00-214">BOMCalcCostPriceUsed</span><span class="sxs-lookup"><span data-stu-id="95a00-214">BOMCalcCostPriceUsed</span></span>|
|<span data-ttu-id="95a00-215">BOMCalcSalesPriceUsed</span><span class="sxs-lookup"><span data-stu-id="95a00-215">BOMCalcSalesPriceUsed</span></span>|
|<span data-ttu-id="95a00-216">BOMCalcType</span><span class="sxs-lookup"><span data-stu-id="95a00-216">BOMCalcType</span></span>|
|<span data-ttu-id="95a00-217">BOMCheckLevel</span><span class="sxs-lookup"><span data-stu-id="95a00-217">BOMCheckLevel</span></span>|
|<span data-ttu-id="95a00-218">BOMCopyContext</span><span class="sxs-lookup"><span data-stu-id="95a00-218">BOMCopyContext</span></span>|
|<span data-ttu-id="95a00-219">BOMCopyMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-219">BOMCopyMethod</span></span>|
|<span data-ttu-id="95a00-220">BOMCopyType</span><span class="sxs-lookup"><span data-stu-id="95a00-220">BOMCopyType</span></span>|
|<span data-ttu-id="95a00-221">BOMCostCalculationMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-221">BOMCostCalculationMethod</span></span>|
|<span data-ttu-id="95a00-222">BOMExplode</span><span class="sxs-lookup"><span data-stu-id="95a00-222">BOMExplode</span></span>|
|<span data-ttu-id="95a00-223">BOMRouteCopyDataType</span><span class="sxs-lookup"><span data-stu-id="95a00-223">BOMRouteCopyDataType</span></span>|
|<span data-ttu-id="95a00-224">BOMVersionFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-224">BOMVersionFilter</span></span>|
|<span data-ttu-id="95a00-225">BudgetReservation_BusinessEvent_PSN</span><span class="sxs-lookup"><span data-stu-id="95a00-225">BudgetReservation_BusinessEvent_PSN</span></span>|
|<span data-ttu-id="95a00-226">BudgetReservation_SourceDocument_PSN</span><span class="sxs-lookup"><span data-stu-id="95a00-226">BudgetReservation_SourceDocument_PSN</span></span>|
|<span data-ttu-id="95a00-227">BudgetReservation_SourceDocumentLine_PSN</span><span class="sxs-lookup"><span data-stu-id="95a00-227">BudgetReservation_SourceDocumentLine_PSN</span></span>|
|<span data-ttu-id="95a00-228">CatCallMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-228">CatCallMethod</span></span>|
|<span data-ttu-id="95a00-229">CatContentType</span><span class="sxs-lookup"><span data-stu-id="95a00-229">CatContentType</span></span>|
|<span data-ttu-id="95a00-230">CatImportStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-230">CatImportStatus</span></span>|
|<span data-ttu-id="95a00-231">CatMaintenanceRequestWfStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-231">CatMaintenanceRequestWfStatus</span></span>|
|<span data-ttu-id="95a00-232">CatProcurementErrorCode</span><span class="sxs-lookup"><span data-stu-id="95a00-232">CatProcurementErrorCode</span></span>|
|<span data-ttu-id="95a00-233">CatPurchaseStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-233">CatPurchaseStatus</span></span>|
|<span data-ttu-id="95a00-234">CatUserReviewApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-234">CatUserReviewApprovalStatus</span></span>|
|<span data-ttu-id="95a00-235">CatVendorCatalogFileUploadType</span><span class="sxs-lookup"><span data-stu-id="95a00-235">CatVendorCatalogFileUploadType</span></span>|
|<span data-ttu-id="95a00-236">CatVendorCatalogTemplateCategory</span><span class="sxs-lookup"><span data-stu-id="95a00-236">CatVendorCatalogTemplateCategory</span></span>|
|<span data-ttu-id="95a00-237">CatVendorCategoryHierarchyType</span><span class="sxs-lookup"><span data-stu-id="95a00-237">CatVendorCategoryHierarchyType</span></span>|
|<span data-ttu-id="95a00-238">CatVendorConfigurationForImport</span><span class="sxs-lookup"><span data-stu-id="95a00-238">CatVendorConfigurationForImport</span></span>|
|<span data-ttu-id="95a00-239">CatVendorLegalEntityStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-239">CatVendorLegalEntityStatus</span></span>|
|<span data-ttu-id="95a00-240">CatVendorSiteType</span><span class="sxs-lookup"><span data-stu-id="95a00-240">CatVendorSiteType</span></span>|
|<span data-ttu-id="95a00-241">ConsignmentReplenishmentOrderLineStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-241">ConsignmentReplenishmentOrderLineStatus</span></span>|
|<span data-ttu-id="95a00-242">ConsignmentReplenishmentOrderStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-242">ConsignmentReplenishmentOrderStatus</span></span>|
|<span data-ttu-id="95a00-243">CostBreakdown</span><span class="sxs-lookup"><span data-stu-id="95a00-243">CostBreakdown</span></span>|
|<span data-ttu-id="95a00-244">CostCalculationCompareProductType</span><span class="sxs-lookup"><span data-stu-id="95a00-244">CostCalculationCompareProductType</span></span>|
|<span data-ttu-id="95a00-245">CostCalculationRole</span><span class="sxs-lookup"><span data-stu-id="95a00-245">CostCalculationRole</span></span>|
|<span data-ttu-id="95a00-246">CostCalculationState</span><span class="sxs-lookup"><span data-stu-id="95a00-246">CostCalculationState</span></span>|
|<span data-ttu-id="95a00-247">CostCalculationSurchargeSubtype</span><span class="sxs-lookup"><span data-stu-id="95a00-247">CostCalculationSurchargeSubtype</span></span>|
|<span data-ttu-id="95a00-248">CostingActivationType</span><span class="sxs-lookup"><span data-stu-id="95a00-248">CostingActivationType</span></span>|
|<span data-ttu-id="95a00-249">CostingVersionCompareTo</span><span class="sxs-lookup"><span data-stu-id="95a00-249">CostingVersionCompareTo</span></span>|
|<span data-ttu-id="95a00-250">CostingVersionPriceType</span><span class="sxs-lookup"><span data-stu-id="95a00-250">CostingVersionPriceType</span></span>|
|<span data-ttu-id="95a00-251">CostPriceBase</span><span class="sxs-lookup"><span data-stu-id="95a00-251">CostPriceBase</span></span>|
|<span data-ttu-id="95a00-252">CostProfitSet</span><span class="sxs-lookup"><span data-stu-id="95a00-252">CostProfitSet</span></span>|
|<span data-ttu-id="95a00-253">CostSalesPriceDisplay</span><span class="sxs-lookup"><span data-stu-id="95a00-253">CostSalesPriceDisplay</span></span>|
|<span data-ttu-id="95a00-254">CostSheetNodeListType</span><span class="sxs-lookup"><span data-stu-id="95a00-254">CostSheetNodeListType</span></span>|
|<span data-ttu-id="95a00-255">CostSheetPanelView</span><span class="sxs-lookup"><span data-stu-id="95a00-255">CostSheetPanelView</span></span>|
|<span data-ttu-id="95a00-256">CostSheetProdFlowMode</span><span class="sxs-lookup"><span data-stu-id="95a00-256">CostSheetProdFlowMode</span></span>|
|<span data-ttu-id="95a00-257">CostStatementCacheAggregationAfter</span><span class="sxs-lookup"><span data-stu-id="95a00-257">CostStatementCacheAggregationAfter</span></span>|
|<span data-ttu-id="95a00-258">CostWIPStatementCategory</span><span class="sxs-lookup"><span data-stu-id="95a00-258">CostWIPStatementCategory</span></span>|
|<span data-ttu-id="95a00-259">CustPaymentValidate</span><span class="sxs-lookup"><span data-stu-id="95a00-259">CustPaymentValidate</span></span>|
|<span data-ttu-id="95a00-260">CustSpecTransOverviewFormMode</span><span class="sxs-lookup"><span data-stu-id="95a00-260">CustSpecTransOverviewFormMode</span></span>|
|<span data-ttu-id="95a00-261">CustTransRefType</span><span class="sxs-lookup"><span data-stu-id="95a00-261">CustTransRefType</span></span>|
|<span data-ttu-id="95a00-262">CustVendPaymentStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-262">CustVendPaymentStatus</span></span>|
|<span data-ttu-id="95a00-263">CustVendTransportPointTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="95a00-263">CustVendTransportPointTypeTransfer</span></span>|
|<span data-ttu-id="95a00-264">DlvScheduleMarkupConversionMode</span><span class="sxs-lookup"><span data-stu-id="95a00-264">DlvScheduleMarkupConversionMode</span></span>|
|<span data-ttu-id="95a00-265">EcoResAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="95a00-265">EcoResAttributeModifier</span></span>|
|<span data-ttu-id="95a00-266">EcoResCategoryAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="95a00-266">EcoResCategoryAttributeModifier</span></span>|
|<span data-ttu-id="95a00-267">EcoResCategoryChangeStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-267">EcoResCategoryChangeStatus</span></span>|
|<span data-ttu-id="95a00-268">EcoResCategoryHierarchyModifier</span><span class="sxs-lookup"><span data-stu-id="95a00-268">EcoResCategoryHierarchyModifier</span></span>|
|<span data-ttu-id="95a00-269">EcoResCategoryNamedHierarchyRole</span><span class="sxs-lookup"><span data-stu-id="95a00-269">EcoResCategoryNamedHierarchyRole</span></span>|
|<span data-ttu-id="95a00-270">EcoResProductImageUsage</span><span class="sxs-lookup"><span data-stu-id="95a00-270">EcoResProductImageUsage</span></span>|
|<span data-ttu-id="95a00-271">EcoResProductListPage</span><span class="sxs-lookup"><span data-stu-id="95a00-271">EcoResProductListPage</span></span>|
|<span data-ttu-id="95a00-272">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="95a00-272">EcoResProductPerCompanyListPageType</span></span>|
|<span data-ttu-id="95a00-273">EcoResProductTemplateType</span><span class="sxs-lookup"><span data-stu-id="95a00-273">EcoResProductTemplateType</span></span>|
|<span data-ttu-id="95a00-274">EcoResReleaseProductToCompany</span><span class="sxs-lookup"><span data-stu-id="95a00-274">EcoResReleaseProductToCompany</span></span>|
|<span data-ttu-id="95a00-275">EcoResVariantConfigurationTechnologyType</span><span class="sxs-lookup"><span data-stu-id="95a00-275">EcoResVariantConfigurationTechnologyType</span></span>|
|<span data-ttu-id="95a00-276">ECPsalesOrdersViewType</span><span class="sxs-lookup"><span data-stu-id="95a00-276">ECPsalesOrdersViewType</span></span>|
|<span data-ttu-id="95a00-277">EPCSSProductViewType</span><span class="sxs-lookup"><span data-stu-id="95a00-277">EPCSSProductViewType</span></span>|
|<span data-ttu-id="95a00-278">EUSalesTransMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-278">EUSalesTransMethod</span></span>|
|<span data-ttu-id="95a00-279">FormLetterType</span><span class="sxs-lookup"><span data-stu-id="95a00-279">FormLetterType</span></span>|
|<span data-ttu-id="95a00-280">GanttCallerWrkCtr</span><span class="sxs-lookup"><span data-stu-id="95a00-280">GanttCallerWrkCtr</span></span>|
|<span data-ttu-id="95a00-281">GanttSetupType</span><span class="sxs-lookup"><span data-stu-id="95a00-281">GanttSetupType</span></span>|
|<span data-ttu-id="95a00-282">GanttTimeUnit</span><span class="sxs-lookup"><span data-stu-id="95a00-282">GanttTimeUnit</span></span>|
|<span data-ttu-id="95a00-283">GanttWrkCtrDisplayColumnsType</span><span class="sxs-lookup"><span data-stu-id="95a00-283">GanttWrkCtrDisplayColumnsType</span></span>|
|<span data-ttu-id="95a00-284">IntercompanyGoodsInTransitLineType</span><span class="sxs-lookup"><span data-stu-id="95a00-284">IntercompanyGoodsInTransitLineType</span></span>|
|<span data-ttu-id="95a00-285">InterCompanyGoodsInTransitOrigin</span><span class="sxs-lookup"><span data-stu-id="95a00-285">InterCompanyGoodsInTransitOrigin</span></span>|
|<span data-ttu-id="95a00-286">InventAccountType</span><span class="sxs-lookup"><span data-stu-id="95a00-286">InventAccountType</span></span>|
|<span data-ttu-id="95a00-287">InventAccountTypeStdCostVariance</span><span class="sxs-lookup"><span data-stu-id="95a00-287">InventAccountTypeStdCostVariance</span></span>|
|<span data-ttu-id="95a00-288">InventAdjustmentBy</span><span class="sxs-lookup"><span data-stu-id="95a00-288">InventAdjustmentBy</span></span>|
|<span data-ttu-id="95a00-289">InventAgingView</span><span class="sxs-lookup"><span data-stu-id="95a00-289">InventAgingView</span></span>|
|<span data-ttu-id="95a00-290">InventBatchJournalType</span><span class="sxs-lookup"><span data-stu-id="95a00-290">InventBatchJournalType</span></span>|
|<span data-ttu-id="95a00-291">InventCostBundleState</span><span class="sxs-lookup"><span data-stu-id="95a00-291">InventCostBundleState</span></span>|
|<span data-ttu-id="95a00-292">InventCostCostDistribution</span><span class="sxs-lookup"><span data-stu-id="95a00-292">InventCostCostDistribution</span></span>|
|<span data-ttu-id="95a00-293">InventCostTransactionCategory</span><span class="sxs-lookup"><span data-stu-id="95a00-293">InventCostTransactionCategory</span></span>|
|<span data-ttu-id="95a00-294">InventCostTransRefType</span><span class="sxs-lookup"><span data-stu-id="95a00-294">InventCostTransRefType</span></span>|
|<span data-ttu-id="95a00-295">InventCountCode</span><span class="sxs-lookup"><span data-stu-id="95a00-295">InventCountCode</span></span>|
|<span data-ttu-id="95a00-296">InventItemCostingType</span><span class="sxs-lookup"><span data-stu-id="95a00-296">InventItemCostingType</span></span>|
|<span data-ttu-id="95a00-297">InventItemLookupDefaultTab</span><span class="sxs-lookup"><span data-stu-id="95a00-297">InventItemLookupDefaultTab</span></span>|
|<span data-ttu-id="95a00-298">InventItemOrderSetupCallerType</span><span class="sxs-lookup"><span data-stu-id="95a00-298">InventItemOrderSetupCallerType</span></span>|
|<span data-ttu-id="95a00-299">InventItemOrderSetupType</span><span class="sxs-lookup"><span data-stu-id="95a00-299">InventItemOrderSetupType</span></span>|
|<span data-ttu-id="95a00-300">InventItemPriceCompareLevel</span><span class="sxs-lookup"><span data-stu-id="95a00-300">InventItemPriceCompareLevel</span></span>|
|<span data-ttu-id="95a00-301">InventItemPriceFilterType</span><span class="sxs-lookup"><span data-stu-id="95a00-301">InventItemPriceFilterType</span></span>|
|<span data-ttu-id="95a00-302">InventItemPriceType</span><span class="sxs-lookup"><span data-stu-id="95a00-302">InventItemPriceType</span></span>|
|<span data-ttu-id="95a00-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span><span class="sxs-lookup"><span data-stu-id="95a00-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span></span>|
|<span data-ttu-id="95a00-304">InventJournalType</span><span class="sxs-lookup"><span data-stu-id="95a00-304">InventJournalType</span></span>|
|<span data-ttu-id="95a00-305">InventLedgerConflictModule</span><span class="sxs-lookup"><span data-stu-id="95a00-305">InventLedgerConflictModule</span></span>|
|<span data-ttu-id="95a00-306">InventLocationType</span><span class="sxs-lookup"><span data-stu-id="95a00-306">InventLocationType</span></span>|
|<span data-ttu-id="95a00-307">InventMovSubType</span><span class="sxs-lookup"><span data-stu-id="95a00-307">InventMovSubType</span></span>|
|<span data-ttu-id="95a00-308">InventNonConformanceApproval</span><span class="sxs-lookup"><span data-stu-id="95a00-308">InventNonConformanceApproval</span></span>|
|<span data-ttu-id="95a00-309">InventNonConformanceHistoryType</span><span class="sxs-lookup"><span data-stu-id="95a00-309">InventNonConformanceHistoryType</span></span>|
|<span data-ttu-id="95a00-310">InventNonConformanceType</span><span class="sxs-lookup"><span data-stu-id="95a00-310">InventNonConformanceType</span></span>|
|<span data-ttu-id="95a00-311">InventParameters</span><span class="sxs-lookup"><span data-stu-id="95a00-311">InventParameters</span></span>|
|<span data-ttu-id="95a00-312">InventPhysicalReduction</span><span class="sxs-lookup"><span data-stu-id="95a00-312">InventPhysicalReduction</span></span>|
|<span data-ttu-id="95a00-313">InventRefType</span><span class="sxs-lookup"><span data-stu-id="95a00-313">InventRefType</span></span>|
|<span data-ttu-id="95a00-314">InventReleaseOrderPickingType</span><span class="sxs-lookup"><span data-stu-id="95a00-314">InventReleaseOrderPickingType</span></span>|
|<span data-ttu-id="95a00-315">InventReportDimHistoryLogType</span><span class="sxs-lookup"><span data-stu-id="95a00-315">InventReportDimHistoryLogType</span></span>|
|<span data-ttu-id="95a00-316">InventStdCostConvItemStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-316">InventStdCostConvItemStatus</span></span>|
|<span data-ttu-id="95a00-317">InventStdCostPeriodType</span><span class="sxs-lookup"><span data-stu-id="95a00-317">InventStdCostPeriodType</span></span>|
|<span data-ttu-id="95a00-318">InventSumFields</span><span class="sxs-lookup"><span data-stu-id="95a00-318">InventSumFields</span></span>|
|<span data-ttu-id="95a00-319">InventSupplyDlvModeSelectCust</span><span class="sxs-lookup"><span data-stu-id="95a00-319">InventSupplyDlvModeSelectCust</span></span>|
|<span data-ttu-id="95a00-320">InventSupplyDlvModeSelectSupply</span><span class="sxs-lookup"><span data-stu-id="95a00-320">InventSupplyDlvModeSelectSupply</span></span>|
|<span data-ttu-id="95a00-321">InventSupplyLeadTimeSource</span><span class="sxs-lookup"><span data-stu-id="95a00-321">InventSupplyLeadTimeSource</span></span>|
|<span data-ttu-id="95a00-322">InventSupplyTmpLeadtimeType</span><span class="sxs-lookup"><span data-stu-id="95a00-322">InventSupplyTmpLeadtimeType</span></span>|
|<span data-ttu-id="95a00-323">InventTestActionOnFailure</span><span class="sxs-lookup"><span data-stu-id="95a00-323">InventTestActionOnFailure</span></span>|
|<span data-ttu-id="95a00-324">InventTestBlockProcess</span><span class="sxs-lookup"><span data-stu-id="95a00-324">InventTestBlockProcess</span></span>|
|<span data-ttu-id="95a00-325">InventTestCorrectionPriority</span><span class="sxs-lookup"><span data-stu-id="95a00-325">InventTestCorrectionPriority</span></span>|
|<span data-ttu-id="95a00-326">InventTestCorrectionStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-326">InventTestCorrectionStatus</span></span>|
|<span data-ttu-id="95a00-327">InventTestDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-327">InventTestDocumentStatus</span></span>|
|<span data-ttu-id="95a00-328">InventTestOrderStatusDisplay</span><span class="sxs-lookup"><span data-stu-id="95a00-328">InventTestOrderStatusDisplay</span></span>|
|<span data-ttu-id="95a00-329">InventTestOutcomeStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-329">InventTestOutcomeStatus</span></span>|
|<span data-ttu-id="95a00-330">InventTestQtySpecification</span><span class="sxs-lookup"><span data-stu-id="95a00-330">InventTestQtySpecification</span></span>|
|<span data-ttu-id="95a00-331">InventTestQuarantineType</span><span class="sxs-lookup"><span data-stu-id="95a00-331">InventTestQuarantineType</span></span>|
|<span data-ttu-id="95a00-332">InventTestReferenceType</span><span class="sxs-lookup"><span data-stu-id="95a00-332">InventTestReferenceType</span></span>|
|<span data-ttu-id="95a00-333">InventTestReport</span><span class="sxs-lookup"><span data-stu-id="95a00-333">InventTestReport</span></span>|
|<span data-ttu-id="95a00-334">InventTestType</span><span class="sxs-lookup"><span data-stu-id="95a00-334">InventTestType</span></span>|
|<span data-ttu-id="95a00-335">InventTrackingDimNodeType</span><span class="sxs-lookup"><span data-stu-id="95a00-335">InventTrackingDimNodeType</span></span>|
|<span data-ttu-id="95a00-336">InventTrackingProductType</span><span class="sxs-lookup"><span data-stu-id="95a00-336">InventTrackingProductType</span></span>|
|<span data-ttu-id="95a00-337">InventTrackingRegisterTransRegStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-337">InventTrackingRegisterTransRegStatus</span></span>|
|<span data-ttu-id="95a00-338">InventTransChildType</span><span class="sxs-lookup"><span data-stu-id="95a00-338">InventTransChildType</span></span>|
|<span data-ttu-id="95a00-339">InventTransferRemainStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-339">InventTransferRemainStatus</span></span>|
|<span data-ttu-id="95a00-340">InventTransferStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-340">InventTransferStatus</span></span>|
|<span data-ttu-id="95a00-341">InventTransferUpdateType</span><span class="sxs-lookup"><span data-stu-id="95a00-341">InventTransferUpdateType</span></span>|
|<span data-ttu-id="95a00-342">InventTransPickRegisterLineStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-342">InventTransPickRegisterLineStatus</span></span>|
|<span data-ttu-id="95a00-343">InventTransType</span><span class="sxs-lookup"><span data-stu-id="95a00-343">InventTransType</span></span>|
|<span data-ttu-id="95a00-344">InventUpdType</span><span class="sxs-lookup"><span data-stu-id="95a00-344">InventUpdType</span></span>|
|<span data-ttu-id="95a00-345">InventValueReportLedgerAccountCategory</span><span class="sxs-lookup"><span data-stu-id="95a00-345">InventValueReportLedgerAccountCategory</span></span>|
|<span data-ttu-id="95a00-346">InventValueReportLedgerLineType</span><span class="sxs-lookup"><span data-stu-id="95a00-346">InventValueReportLedgerLineType</span></span>|
|<span data-ttu-id="95a00-347">InventValueReportResourceType</span><span class="sxs-lookup"><span data-stu-id="95a00-347">InventValueReportResourceType</span></span>|
|<span data-ttu-id="95a00-348">ItemGroupLedgerDimensionGroup</span><span class="sxs-lookup"><span data-stu-id="95a00-348">ItemGroupLedgerDimensionGroup</span></span>|
|<span data-ttu-id="95a00-349">ItemReservation</span><span class="sxs-lookup"><span data-stu-id="95a00-349">ItemReservation</span></span>|
|<span data-ttu-id="95a00-350">JmgAbsenceColumnLayout</span><span class="sxs-lookup"><span data-stu-id="95a00-350">JmgAbsenceColumnLayout</span></span>|
|<span data-ttu-id="95a00-351">JmgAbsenceMethodEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-351">JmgAbsenceMethodEnum</span></span>|
|<span data-ttu-id="95a00-352">JmgAttendanceRegistrationType</span><span class="sxs-lookup"><span data-stu-id="95a00-352">JmgAttendanceRegistrationType</span></span>|
|<span data-ttu-id="95a00-353">JmgAttendanceReportType</span><span class="sxs-lookup"><span data-stu-id="95a00-353">JmgAttendanceReportType</span></span>|
|<span data-ttu-id="95a00-354">JmgBarCodeType</span><span class="sxs-lookup"><span data-stu-id="95a00-354">JmgBarCodeType</span></span>|
|<span data-ttu-id="95a00-355">JmgBreakDropEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-355">JmgBreakDropEnum</span></span>|
|<span data-ttu-id="95a00-356">JmgClockStyle</span><span class="sxs-lookup"><span data-stu-id="95a00-356">JmgClockStyle</span></span>|
|<span data-ttu-id="95a00-357">JmgControlType</span><span class="sxs-lookup"><span data-stu-id="95a00-357">JmgControlType</span></span>|
|<span data-ttu-id="95a00-358">JmgDaysTotalWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-358">JmgDaysTotalWorkflowStatus</span></span>|
|<span data-ttu-id="95a00-359">JmgEmployeeSignInStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-359">JmgEmployeeSignInStatus</span></span>|
|<span data-ttu-id="95a00-360">JmgFeedbackButtonFunction</span><span class="sxs-lookup"><span data-stu-id="95a00-360">JmgFeedbackButtonFunction</span></span>|
|<span data-ttu-id="95a00-361">JmgFeedbackStyle</span><span class="sxs-lookup"><span data-stu-id="95a00-361">JmgFeedbackStyle</span></span>|
|<span data-ttu-id="95a00-362">JmgFieldName</span><span class="sxs-lookup"><span data-stu-id="95a00-362">JmgFieldName</span></span>|
|<span data-ttu-id="95a00-363">JmgGetRegistrationTimeFrom</span><span class="sxs-lookup"><span data-stu-id="95a00-363">JmgGetRegistrationTimeFrom</span></span>|
|<span data-ttu-id="95a00-364">JmgGridAppearance</span><span class="sxs-lookup"><span data-stu-id="95a00-364">JmgGridAppearance</span></span>|
|<span data-ttu-id="95a00-365">JmgJobTableSynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="95a00-365">JmgJobTableSynchronizationMode</span></span>|
|<span data-ttu-id="95a00-366">JmgJournalRegWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-366">JmgJournalRegWorkflowStatus</span></span>|
|<span data-ttu-id="95a00-367">JmgMark</span><span class="sxs-lookup"><span data-stu-id="95a00-367">JmgMark</span></span>|
|<span data-ttu-id="95a00-368">JmgMessageType</span><span class="sxs-lookup"><span data-stu-id="95a00-368">JmgMessageType</span></span>|
|<span data-ttu-id="95a00-369">JmgPayAdjustType</span><span class="sxs-lookup"><span data-stu-id="95a00-369">JmgPayAdjustType</span></span>|
|<span data-ttu-id="95a00-370">JmgPayEventsExportType</span><span class="sxs-lookup"><span data-stu-id="95a00-370">JmgPayEventsExportType</span></span>|
|<span data-ttu-id="95a00-371">JmgPaySpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-371">JmgPaySpecTypeEnum</span></span>|
|<span data-ttu-id="95a00-372">JmgPaySpecTypeEnumPick</span><span class="sxs-lookup"><span data-stu-id="95a00-372">JmgPaySpecTypeEnumPick</span></span>|
|<span data-ttu-id="95a00-373">JmgPostAutomatically</span><span class="sxs-lookup"><span data-stu-id="95a00-373">JmgPostAutomatically</span></span>|
|<span data-ttu-id="95a00-374">JmgProdStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-374">JmgProdStatusUpdate</span></span>|
|<span data-ttu-id="95a00-375">JmgProdStatusUpdateReportFinished</span><span class="sxs-lookup"><span data-stu-id="95a00-375">JmgProdStatusUpdateReportFinished</span></span>|
|<span data-ttu-id="95a00-376">JmgProfileSpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-376">JmgProfileSpecTypeEnum</span></span>|
|<span data-ttu-id="95a00-377">JmgProfileStartCodeBlankPrev</span><span class="sxs-lookup"><span data-stu-id="95a00-377">JmgProfileStartCodeBlankPrev</span></span>|
|<span data-ttu-id="95a00-378">JmgProjStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-378">JmgProjStatusUpdate</span></span>|
|<span data-ttu-id="95a00-379">JmgRegistrationTouchJobStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-379">JmgRegistrationTouchJobStatus</span></span>|
|<span data-ttu-id="95a00-380">JmgSecondPresentationEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-380">JmgSecondPresentationEnum</span></span>|
|<span data-ttu-id="95a00-381">JmgShopFloorServiceStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-381">JmgShopFloorServiceStatus</span></span>|
|<span data-ttu-id="95a00-382">JmgSignInButtonFunction</span><span class="sxs-lookup"><span data-stu-id="95a00-382">JmgSignInButtonFunction</span></span>|
|<span data-ttu-id="95a00-383">JmgStoppedCompletedStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-383">JmgStoppedCompletedStatus</span></span>|
|<span data-ttu-id="95a00-384">JmgTermBaudeRate</span><span class="sxs-lookup"><span data-stu-id="95a00-384">JmgTermBaudeRate</span></span>|
|<span data-ttu-id="95a00-385">JmgTermComPort</span><span class="sxs-lookup"><span data-stu-id="95a00-385">JmgTermComPort</span></span>|
|<span data-ttu-id="95a00-386">JmgTermDataBit</span><span class="sxs-lookup"><span data-stu-id="95a00-386">JmgTermDataBit</span></span>|
|<span data-ttu-id="95a00-387">JmgTerminalInsertMode</span><span class="sxs-lookup"><span data-stu-id="95a00-387">JmgTerminalInsertMode</span></span>|
|<span data-ttu-id="95a00-388">JmgTermStopBit</span><span class="sxs-lookup"><span data-stu-id="95a00-388">JmgTermStopBit</span></span>|
|<span data-ttu-id="95a00-389">KanbanBoardRefreshCycle</span><span class="sxs-lookup"><span data-stu-id="95a00-389">KanbanBoardRefreshCycle</span></span>|
|<span data-ttu-id="95a00-390">KanbanBoardType</span><span class="sxs-lookup"><span data-stu-id="95a00-390">KanbanBoardType</span></span>|
|<span data-ttu-id="95a00-391">KanbanCardAssignmentType</span><span class="sxs-lookup"><span data-stu-id="95a00-391">KanbanCardAssignmentType</span></span>|
|<span data-ttu-id="95a00-392">KanbanControlActionState</span><span class="sxs-lookup"><span data-stu-id="95a00-392">KanbanControlActionState</span></span>|
|<span data-ttu-id="95a00-393">KanbanControlLegendFormat</span><span class="sxs-lookup"><span data-stu-id="95a00-393">KanbanControlLegendFormat</span></span>|
|<span data-ttu-id="95a00-394">KanbanControlSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="95a00-394">KanbanControlSelectionChanged</span></span>|
|<span data-ttu-id="95a00-395">KanbanDemandOriginType</span><span class="sxs-lookup"><span data-stu-id="95a00-395">KanbanDemandOriginType</span></span>|
|<span data-ttu-id="95a00-396">KanbanJobPeggingType</span><span class="sxs-lookup"><span data-stu-id="95a00-396">KanbanJobPeggingType</span></span>|
|<span data-ttu-id="95a00-397">KanbanJobPickingListLineType</span><span class="sxs-lookup"><span data-stu-id="95a00-397">KanbanJobPickingListLineType</span></span>|
|<span data-ttu-id="95a00-398">KanbanLineEventType</span><span class="sxs-lookup"><span data-stu-id="95a00-398">KanbanLineEventType</span></span>|
|<span data-ttu-id="95a00-399">KanbanMultiMode</span><span class="sxs-lookup"><span data-stu-id="95a00-399">KanbanMultiMode</span></span>|
|<span data-ttu-id="95a00-400">KanbanPrintInstructions</span><span class="sxs-lookup"><span data-stu-id="95a00-400">KanbanPrintInstructions</span></span>|
|<span data-ttu-id="95a00-401">KanbanProdBOMLineEventType</span><span class="sxs-lookup"><span data-stu-id="95a00-401">KanbanProdBOMLineEventType</span></span>|
|<span data-ttu-id="95a00-402">KanbanQuantityCalculationStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-402">KanbanQuantityCalculationStatus</span></span>|
|<span data-ttu-id="95a00-403">KanbanSalesLineEventType</span><span class="sxs-lookup"><span data-stu-id="95a00-403">KanbanSalesLineEventType</span></span>|
|<span data-ttu-id="95a00-404">KanbanStockReplenishmentEventType</span><span class="sxs-lookup"><span data-stu-id="95a00-404">KanbanStockReplenishmentEventType</span></span>|
|<span data-ttu-id="95a00-405">LeanBOMLineReservationMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-405">LeanBOMLineReservationMethod</span></span>|
|<span data-ttu-id="95a00-406">LeanCostingUnusedQtyType</span><span class="sxs-lookup"><span data-stu-id="95a00-406">LeanCostingUnusedQtyType</span></span>|
|<span data-ttu-id="95a00-407">LeanHandlingUnitEmptyPolicy</span><span class="sxs-lookup"><span data-stu-id="95a00-407">LeanHandlingUnitEmptyPolicy</span></span>|
|<span data-ttu-id="95a00-408">LeanInventoryControl</span><span class="sxs-lookup"><span data-stu-id="95a00-408">LeanInventoryControl</span></span>|
|<span data-ttu-id="95a00-409">LeanPeggedEventType</span><span class="sxs-lookup"><span data-stu-id="95a00-409">LeanPeggedEventType</span></span>|
|<span data-ttu-id="95a00-410">LeanPlanJobReferenceTypes</span><span class="sxs-lookup"><span data-stu-id="95a00-410">LeanPlanJobReferenceTypes</span></span>|
|<span data-ttu-id="95a00-411">LeanProductionFlowCostingStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-411">LeanProductionFlowCostingStatus</span></span>|
|<span data-ttu-id="95a00-412">LeanProductionFlowVisualizationViewMode</span><span class="sxs-lookup"><span data-stu-id="95a00-412">LeanProductionFlowVisualizationViewMode</span></span>|
|<span data-ttu-id="95a00-413">LeanProductTypes</span><span class="sxs-lookup"><span data-stu-id="95a00-413">LeanProductTypes</span></span>|
|<span data-ttu-id="95a00-414">LeanTaktStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-414">LeanTaktStatus</span></span>|
|<span data-ttu-id="95a00-415">LedgerPostingType</span><span class="sxs-lookup"><span data-stu-id="95a00-415">LedgerPostingType</span></span>|
|<span data-ttu-id="95a00-416">LedgerTransTxt</span><span class="sxs-lookup"><span data-stu-id="95a00-416">LedgerTransTxt</span></span>|
|<span data-ttu-id="95a00-417">MarkupAllocateAfter</span><span class="sxs-lookup"><span data-stu-id="95a00-417">MarkupAllocateAfter</span></span>|
|<span data-ttu-id="95a00-418">MarkupCategory</span><span class="sxs-lookup"><span data-stu-id="95a00-418">MarkupCategory</span></span>|
|<span data-ttu-id="95a00-419">MCRBrokerContractStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-419">MCRBrokerContractStatus</span></span>|
|<span data-ttu-id="95a00-420">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="95a00-420">MCRCustSearchType</span></span>|
|<span data-ttu-id="95a00-421">MCRFullTextSearchType</span><span class="sxs-lookup"><span data-stu-id="95a00-421">MCRFullTextSearchType</span></span>|
|<span data-ttu-id="95a00-422">MCRInstallPlanApplyMiscCharge</span><span class="sxs-lookup"><span data-stu-id="95a00-422">MCRInstallPlanApplyMiscCharge</span></span>|
|<span data-ttu-id="95a00-423">MCRItemListGenerationType</span><span class="sxs-lookup"><span data-stu-id="95a00-423">MCRItemListGenerationType</span></span>|
|<span data-ttu-id="95a00-424">MCRPickingPrompt</span><span class="sxs-lookup"><span data-stu-id="95a00-424">MCRPickingPrompt</span></span>|
|<span data-ttu-id="95a00-425">MCRPickingSessionStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-425">MCRPickingSessionStatus</span></span>|
|<span data-ttu-id="95a00-426">MCRPickingWaveStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-426">MCRPickingWaveStatus</span></span>|
|<span data-ttu-id="95a00-427">MCRPriceHistoryType</span><span class="sxs-lookup"><span data-stu-id="95a00-427">MCRPriceHistoryType</span></span>|
|<span data-ttu-id="95a00-428">MCRRoyaltyLineBreakType</span><span class="sxs-lookup"><span data-stu-id="95a00-428">MCRRoyaltyLineBreakType</span></span>|
|<span data-ttu-id="95a00-429">MCRRoyaltyTakenFrom</span><span class="sxs-lookup"><span data-stu-id="95a00-429">MCRRoyaltyTakenFrom</span></span>|
|<span data-ttu-id="95a00-430">MCRRoyaltyTransactionType</span><span class="sxs-lookup"><span data-stu-id="95a00-430">MCRRoyaltyTransactionType</span></span>|
|<span data-ttu-id="95a00-431">MCRRoyaltyUnitType</span><span class="sxs-lookup"><span data-stu-id="95a00-431">MCRRoyaltyUnitType</span></span>|
|<span data-ttu-id="95a00-432">MCRRoyaltyUOMOption</span><span class="sxs-lookup"><span data-stu-id="95a00-432">MCRRoyaltyUOMOption</span></span>|
|<span data-ttu-id="95a00-433">MCRSalesOrderDetailStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-433">MCRSalesOrderDetailStatus</span></span>|
|<span data-ttu-id="95a00-434">ModuleInventCustVend</span><span class="sxs-lookup"><span data-stu-id="95a00-434">ModuleInventCustVend</span></span>|
|<span data-ttu-id="95a00-435">ModuleInventPurchSales</span><span class="sxs-lookup"><span data-stu-id="95a00-435">ModuleInventPurchSales</span></span>|
|<span data-ttu-id="95a00-436">OriginalDocument</span><span class="sxs-lookup"><span data-stu-id="95a00-436">OriginalDocument</span></span>|
|<span data-ttu-id="95a00-437">PaymDocumentType</span><span class="sxs-lookup"><span data-stu-id="95a00-437">PaymDocumentType</span></span>|
|<span data-ttu-id="95a00-438">PCExpressionEditorSymbolType</span><span class="sxs-lookup"><span data-stu-id="95a00-438">PCExpressionEditorSymbolType</span></span>|
|<span data-ttu-id="95a00-439">PCLookupMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-439">PCLookupMethod</span></span>|
|<span data-ttu-id="95a00-440">PCNewSelectComponent</span><span class="sxs-lookup"><span data-stu-id="95a00-440">PCNewSelectComponent</span></span>|
|<span data-ttu-id="95a00-441">PCRequirement</span><span class="sxs-lookup"><span data-stu-id="95a00-441">PCRequirement</span></span>|
|<span data-ttu-id="95a00-442">PCTableConstraintType</span><span class="sxs-lookup"><span data-stu-id="95a00-442">PCTableConstraintType</span></span>|
|<span data-ttu-id="95a00-443">PDSAdjustmentPrinciple</span><span class="sxs-lookup"><span data-stu-id="95a00-443">PDSAdjustmentPrinciple</span></span>|
|<span data-ttu-id="95a00-444">PdsBatchAttribToleranceAction</span><span class="sxs-lookup"><span data-stu-id="95a00-444">PdsBatchAttribToleranceAction</span></span>|
|<span data-ttu-id="95a00-445">PdsBatchAttribUpdateType</span><span class="sxs-lookup"><span data-stu-id="95a00-445">PdsBatchAttribUpdateType</span></span>|
|<span data-ttu-id="95a00-446">PDSCalcElementBase</span><span class="sxs-lookup"><span data-stu-id="95a00-446">PDSCalcElementBase</span></span>|
|<span data-ttu-id="95a00-447">PDSCompensationPrincipleEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-447">PDSCompensationPrincipleEnum</span></span>|
|<span data-ttu-id="95a00-448">PDSElementTypeEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-448">PDSElementTypeEnum</span></span>|
|<span data-ttu-id="95a00-449">PDSIngredientTypeEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-449">PDSIngredientTypeEnum</span></span>|
|<span data-ttu-id="95a00-450">PdsMRCDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-450">PdsMRCDocumentStatus</span></span>|
|<span data-ttu-id="95a00-451">PdsMRCEffectiveDateBasis</span><span class="sxs-lookup"><span data-stu-id="95a00-451">PdsMRCEffectiveDateBasis</span></span>|
|<span data-ttu-id="95a00-452">PdsMRCEventModule</span><span class="sxs-lookup"><span data-stu-id="95a00-452">PdsMRCEventModule</span></span>|
|<span data-ttu-id="95a00-453">PdsMRCEventType</span><span class="sxs-lookup"><span data-stu-id="95a00-453">PdsMRCEventType</span></span>|
|<span data-ttu-id="95a00-454">PdsMRCListType</span><span class="sxs-lookup"><span data-stu-id="95a00-454">PdsMRCListType</span></span>|
|<span data-ttu-id="95a00-455">PdsPaymtType</span><span class="sxs-lookup"><span data-stu-id="95a00-455">PdsPaymtType</span></span>|
|<span data-ttu-id="95a00-456">PDSPotencyAttribRecordingEnum</span><span class="sxs-lookup"><span data-stu-id="95a00-456">PDSPotencyAttribRecordingEnum</span></span>|
|<span data-ttu-id="95a00-457">PdsRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="95a00-457">PdsRebateCalcDateType</span></span>|
|<span data-ttu-id="95a00-458">PdsRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="95a00-458">PdsRebateTakenFrom</span></span>|
|<span data-ttu-id="95a00-459">PdsRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="95a00-459">PdsRebateUOMOption</span></span>|
|<span data-ttu-id="95a00-460">PdsSameLotError</span><span class="sxs-lookup"><span data-stu-id="95a00-460">PdsSameLotError</span></span>|
|<span data-ttu-id="95a00-461">pdsTMAJournalPosting</span><span class="sxs-lookup"><span data-stu-id="95a00-461">pdsTMAJournalPosting</span></span>|
|<span data-ttu-id="95a00-462">PdsUpdateBatchDate</span><span class="sxs-lookup"><span data-stu-id="95a00-462">PdsUpdateBatchDate</span></span>|
|<span data-ttu-id="95a00-463">PdsUpdateDispositionStatus_Quality</span><span class="sxs-lookup"><span data-stu-id="95a00-463">PdsUpdateDispositionStatus_Quality</span></span>|
|<span data-ttu-id="95a00-464">PlanActivityCreateRelationType</span><span class="sxs-lookup"><span data-stu-id="95a00-464">PlanActivityCreateRelationType</span></span>|
|<span data-ttu-id="95a00-465">PlanActivityProductionFlowActivityType</span><span class="sxs-lookup"><span data-stu-id="95a00-465">PlanActivityProductionFlowActivityType</span></span>|
|<span data-ttu-id="95a00-466">PlanTypes</span><span class="sxs-lookup"><span data-stu-id="95a00-466">PlanTypes</span></span>|
|<span data-ttu-id="95a00-467">PmfCostAllocationMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-467">PmfCostAllocationMethod</span></span>|
|<span data-ttu-id="95a00-468">PmfOrderType</span><span class="sxs-lookup"><span data-stu-id="95a00-468">PmfOrderType</span></span>|
|<span data-ttu-id="95a00-469">PmfOrderTypeFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-469">PmfOrderTypeFilter</span></span>|
|<span data-ttu-id="95a00-470">PmfProdType</span><span class="sxs-lookup"><span data-stu-id="95a00-470">PmfProdType</span></span>|
|<span data-ttu-id="95a00-471">PMFSeqCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="95a00-471">PMFSeqCalendarPeriod</span></span>|
|<span data-ttu-id="95a00-472">PriceBase</span><span class="sxs-lookup"><span data-stu-id="95a00-472">PriceBase</span></span>|
|<span data-ttu-id="95a00-473">PriceDiscPurchasePromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="95a00-473">PriceDiscPurchasePromptSystemSource</span></span>|
|<span data-ttu-id="95a00-474">PriceDiscSalesPromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="95a00-474">PriceDiscSalesPromptSystemSource</span></span>|
|<span data-ttu-id="95a00-475">PriceGroupType</span><span class="sxs-lookup"><span data-stu-id="95a00-475">PriceGroupType</span></span>|
|<span data-ttu-id="95a00-476">PriceSalesPurch</span><span class="sxs-lookup"><span data-stu-id="95a00-476">PriceSalesPurch</span></span>|
|<span data-ttu-id="95a00-477">PriceType</span><span class="sxs-lookup"><span data-stu-id="95a00-477">PriceType</span></span>|
|<span data-ttu-id="95a00-478">ProcCategoryAdministrationActivity</span><span class="sxs-lookup"><span data-stu-id="95a00-478">ProcCategoryAdministrationActivity</span></span>|
|<span data-ttu-id="95a00-479">ProdBOMConsumpProposal</span><span class="sxs-lookup"><span data-stu-id="95a00-479">ProdBOMConsumpProposal</span></span>|
|<span data-ttu-id="95a00-480">ProdBOMJournalQty</span><span class="sxs-lookup"><span data-stu-id="95a00-480">ProdBOMJournalQty</span></span>|
|<span data-ttu-id="95a00-481">ProdBOMJournalSplit</span><span class="sxs-lookup"><span data-stu-id="95a00-481">ProdBOMJournalSplit</span></span>|
|<span data-ttu-id="95a00-482">ProdErrorCause</span><span class="sxs-lookup"><span data-stu-id="95a00-482">ProdErrorCause</span></span>|
|<span data-ttu-id="95a00-483">ProdGanttJobColorType</span><span class="sxs-lookup"><span data-stu-id="95a00-483">ProdGanttJobColorType</span></span>|
|<span data-ttu-id="95a00-484">ProdGanttLoad</span><span class="sxs-lookup"><span data-stu-id="95a00-484">ProdGanttLoad</span></span>|
|<span data-ttu-id="95a00-485">ProdGanttRouteColorType</span><span class="sxs-lookup"><span data-stu-id="95a00-485">ProdGanttRouteColorType</span></span>|
|<span data-ttu-id="95a00-486">ProdJournalCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="95a00-486">ProdJournalCleanUpMode</span></span>|
|<span data-ttu-id="95a00-487">ProdMode</span><span class="sxs-lookup"><span data-stu-id="95a00-487">ProdMode</span></span>|
|<span data-ttu-id="95a00-488">ProdNotificationLevel</span><span class="sxs-lookup"><span data-stu-id="95a00-488">ProdNotificationLevel</span></span>|
|<span data-ttu-id="95a00-489">ProdParamInventDimLookup</span><span class="sxs-lookup"><span data-stu-id="95a00-489">ProdParamInventDimLookup</span></span>|
|<span data-ttu-id="95a00-490">ProdParmType</span><span class="sxs-lookup"><span data-stu-id="95a00-490">ProdParmType</span></span>|
|<span data-ttu-id="95a00-491">ProdRefLookUp</span><span class="sxs-lookup"><span data-stu-id="95a00-491">ProdRefLookUp</span></span>|
|<span data-ttu-id="95a00-492">ProdRouteJobCurrentFormTabId</span><span class="sxs-lookup"><span data-stu-id="95a00-492">ProdRouteJobCurrentFormTabId</span></span>|
|<span data-ttu-id="95a00-493">ProdSchedDirection</span><span class="sxs-lookup"><span data-stu-id="95a00-493">ProdSchedDirection</span></span>|
|<span data-ttu-id="95a00-494">ProdScrapMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-494">ProdScrapMethod</span></span>|
|<span data-ttu-id="95a00-495">ProdStandardCostVariance</span><span class="sxs-lookup"><span data-stu-id="95a00-495">ProdStandardCostVariance</span></span>|
|<span data-ttu-id="95a00-496">ProdStatusAll</span><span class="sxs-lookup"><span data-stu-id="95a00-496">ProdStatusAll</span></span>|
|<span data-ttu-id="95a00-497">ProdStatusType</span><span class="sxs-lookup"><span data-stu-id="95a00-497">ProdStatusType</span></span>|
|<span data-ttu-id="95a00-498">ProductionTransType</span><span class="sxs-lookup"><span data-stu-id="95a00-498">ProductionTransType</span></span>|
|<span data-ttu-id="95a00-499">ProdUpdateJour</span><span class="sxs-lookup"><span data-stu-id="95a00-499">ProdUpdateJour</span></span>|
|<span data-ttu-id="95a00-500">ProdWHSReleasePolicy</span><span class="sxs-lookup"><span data-stu-id="95a00-500">ProdWHSReleasePolicy</span></span>|
|<span data-ttu-id="95a00-501">ProdWIPType_NA</span><span class="sxs-lookup"><span data-stu-id="95a00-501">ProdWIPType_NA</span></span>|
|<span data-ttu-id="95a00-502">PurchaseOrderResponseAction</span><span class="sxs-lookup"><span data-stu-id="95a00-502">PurchaseOrderResponseAction</span></span>|
|<span data-ttu-id="95a00-503">PurchaseType</span><span class="sxs-lookup"><span data-stu-id="95a00-503">PurchaseType</span></span>|
|<span data-ttu-id="95a00-504">PurchasingTransactionType</span><span class="sxs-lookup"><span data-stu-id="95a00-504">PurchasingTransactionType</span></span>|
|<span data-ttu-id="95a00-505">PurchCORReceivingMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-505">PurchCORReceivingMethod</span></span>|
|<span data-ttu-id="95a00-506">PurchCORRejectStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-506">PurchCORRejectStatus</span></span>|
|<span data-ttu-id="95a00-507">PurchCovRef</span><span class="sxs-lookup"><span data-stu-id="95a00-507">PurchCovRef</span></span>|
|<span data-ttu-id="95a00-508">PurchDlvAddr</span><span class="sxs-lookup"><span data-stu-id="95a00-508">PurchDlvAddr</span></span>|
|<span data-ttu-id="95a00-509">PurchLineBackOrderViews</span><span class="sxs-lookup"><span data-stu-id="95a00-509">PurchLineBackOrderViews</span></span>|
|<span data-ttu-id="95a00-510">PurchLineDeliveryFulfillment</span><span class="sxs-lookup"><span data-stu-id="95a00-510">PurchLineDeliveryFulfillment</span></span>|
|<span data-ttu-id="95a00-511">PurchLineDeliveryPrecision</span><span class="sxs-lookup"><span data-stu-id="95a00-511">PurchLineDeliveryPrecision</span></span>|
|<span data-ttu-id="95a00-512">PurchMatchingPolicyOverrideOption</span><span class="sxs-lookup"><span data-stu-id="95a00-512">PurchMatchingPolicyOverrideOption</span></span>|
|<span data-ttu-id="95a00-513">PurchPrepayApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="95a00-513">PurchPrepayApplicationPolicy</span></span>|
|<span data-ttu-id="95a00-514">PurchPriceDateType</span><span class="sxs-lookup"><span data-stu-id="95a00-514">PurchPriceDateType</span></span>|
|<span data-ttu-id="95a00-515">PurchPurchaseOrderCreationMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-515">PurchPurchaseOrderCreationMethod</span></span>|
|<span data-ttu-id="95a00-516">PurchReApprovalPolicyRuleViewType</span><span class="sxs-lookup"><span data-stu-id="95a00-516">PurchReApprovalPolicyRuleViewType</span></span>|
|<span data-ttu-id="95a00-517">PurchReqAuthorizationSpecificReporting</span><span class="sxs-lookup"><span data-stu-id="95a00-517">PurchReqAuthorizationSpecificReporting</span></span>|
|<span data-ttu-id="95a00-518">PurchReqAutoCreatePurch</span><span class="sxs-lookup"><span data-stu-id="95a00-518">PurchReqAutoCreatePurch</span></span>|
|<span data-ttu-id="95a00-519">PurchReqCatalogAllNon</span><span class="sxs-lookup"><span data-stu-id="95a00-519">PurchReqCatalogAllNon</span></span>|
|<span data-ttu-id="95a00-520">PurchReqConsolidationActiveStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-520">PurchReqConsolidationActiveStatus</span></span>|
|<span data-ttu-id="95a00-521">PurchReqConsolidationPriority</span><span class="sxs-lookup"><span data-stu-id="95a00-521">PurchReqConsolidationPriority</span></span>|
|<span data-ttu-id="95a00-522">PurchReqConsolidationStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-522">PurchReqConsolidationStatus</span></span>|
|<span data-ttu-id="95a00-523">PurchReqCreationStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-523">PurchReqCreationStatus</span></span>|
|<span data-ttu-id="95a00-524">PurchReqItemDescriptionTransfer</span><span class="sxs-lookup"><span data-stu-id="95a00-524">PurchReqItemDescriptionTransfer</span></span>|
|<span data-ttu-id="95a00-525">PurchReqItemFilterType</span><span class="sxs-lookup"><span data-stu-id="95a00-525">PurchReqItemFilterType</span></span>|
|<span data-ttu-id="95a00-526">PurchReqOnBehalfReports</span><span class="sxs-lookup"><span data-stu-id="95a00-526">PurchReqOnBehalfReports</span></span>|
|<span data-ttu-id="95a00-527">PurchReqOriginationAuthorizationView</span><span class="sxs-lookup"><span data-stu-id="95a00-527">PurchReqOriginationAuthorizationView</span></span>|
|<span data-ttu-id="95a00-528">PurchReqProcessingState</span><span class="sxs-lookup"><span data-stu-id="95a00-528">PurchReqProcessingState</span></span>|
|<span data-ttu-id="95a00-529">PurchReqQuestionnaireAggregateStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-529">PurchReqQuestionnaireAggregateStatus</span></span>|
|<span data-ttu-id="95a00-530">PurchReqQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-530">PurchReqQuestionnaireStatus</span></span>|
|<span data-ttu-id="95a00-531">PurchReqReportSortOrder</span><span class="sxs-lookup"><span data-stu-id="95a00-531">PurchReqReportSortOrder</span></span>|
|<span data-ttu-id="95a00-532">PurchReqReportStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-532">PurchReqReportStatus</span></span>|
|<span data-ttu-id="95a00-533">PurchReqReviewStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-533">PurchReqReviewStatus</span></span>|
|<span data-ttu-id="95a00-534">PurchReqRFQRequirement</span><span class="sxs-lookup"><span data-stu-id="95a00-534">PurchReqRFQRequirement</span></span>|
|<span data-ttu-id="95a00-535">PurchReqRFQType</span><span class="sxs-lookup"><span data-stu-id="95a00-535">PurchReqRFQType</span></span>|
|<span data-ttu-id="95a00-536">PurchReqSaveChanges</span><span class="sxs-lookup"><span data-stu-id="95a00-536">PurchReqSaveChanges</span></span>|
|<span data-ttu-id="95a00-537">PurchReqStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-537">PurchReqStatus</span></span>|
|<span data-ttu-id="95a00-538">PurchReqType</span><span class="sxs-lookup"><span data-stu-id="95a00-538">PurchReqType</span></span>|
|<span data-ttu-id="95a00-539">PurchReqWorkflowState</span><span class="sxs-lookup"><span data-stu-id="95a00-539">PurchReqWorkflowState</span></span>|
|<span data-ttu-id="95a00-540">PurchRFQQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-540">PurchRFQQuestionnaireStatus</span></span>|
|<span data-ttu-id="95a00-541">PurchRFQStatusVendor</span><span class="sxs-lookup"><span data-stu-id="95a00-541">PurchRFQStatusVendor</span></span>|
|<span data-ttu-id="95a00-542">PurchRFQType</span><span class="sxs-lookup"><span data-stu-id="95a00-542">PurchRFQType</span></span>|
|<span data-ttu-id="95a00-543">PurchTableFormId</span><span class="sxs-lookup"><span data-stu-id="95a00-543">PurchTableFormId</span></span>|
|<span data-ttu-id="95a00-544">PurchTableListPage</span><span class="sxs-lookup"><span data-stu-id="95a00-544">PurchTableListPage</span></span>|
|<span data-ttu-id="95a00-545">PurchTableMode</span><span class="sxs-lookup"><span data-stu-id="95a00-545">PurchTableMode</span></span>|
|<span data-ttu-id="95a00-546">PurchTotalsCachingMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-546">PurchTotalsCachingMethod</span></span>|
|<span data-ttu-id="95a00-547">PurchUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-547">PurchUpdate</span></span>|
|<span data-ttu-id="95a00-548">PurchVendorPortalShowResponseType</span><span class="sxs-lookup"><span data-stu-id="95a00-548">PurchVendorPortalShowResponseType</span></span>|
|<span data-ttu-id="95a00-549">QuotationType</span><span class="sxs-lookup"><span data-stu-id="95a00-549">QuotationType</span></span>|
|<span data-ttu-id="95a00-550">ReqBOMRouteCreated</span><span class="sxs-lookup"><span data-stu-id="95a00-550">ReqBOMRouteCreated</span></span>|
|<span data-ttu-id="95a00-551">ReqCurrentDaySchedFrom</span><span class="sxs-lookup"><span data-stu-id="95a00-551">ReqCurrentDaySchedFrom</span></span>|
|<span data-ttu-id="95a00-552">ReqDemPlanDataSourceType</span><span class="sxs-lookup"><span data-stu-id="95a00-552">ReqDemPlanDataSourceType</span></span>|
|<span data-ttu-id="95a00-553">ReqDemPlanDemandCategory</span><span class="sxs-lookup"><span data-stu-id="95a00-553">ReqDemPlanDemandCategory</span></span>|
|<span data-ttu-id="95a00-554">ReqDemPlanForecastAttributeType</span><span class="sxs-lookup"><span data-stu-id="95a00-554">ReqDemPlanForecastAttributeType</span></span>|
|<span data-ttu-id="95a00-555">ReqDemPlanForecastingStrategy</span><span class="sxs-lookup"><span data-stu-id="95a00-555">ReqDemPlanForecastingStrategy</span></span>|
|<span data-ttu-id="95a00-556">ReqDemPlanForecastType</span><span class="sxs-lookup"><span data-stu-id="95a00-556">ReqDemPlanForecastType</span></span>|
|<span data-ttu-id="95a00-557">ReqDisplayDelay</span><span class="sxs-lookup"><span data-stu-id="95a00-557">ReqDisplayDelay</span></span>|
|<span data-ttu-id="95a00-558">ReqForecastReducedBy</span><span class="sxs-lookup"><span data-stu-id="95a00-558">ReqForecastReducedBy</span></span>|
|<span data-ttu-id="95a00-559">ReqGanttColorType</span><span class="sxs-lookup"><span data-stu-id="95a00-559">ReqGanttColorType</span></span>|
|<span data-ttu-id="95a00-560">ReqGanttShow</span><span class="sxs-lookup"><span data-stu-id="95a00-560">ReqGanttShow</span></span>|
|<span data-ttu-id="95a00-561">ReqItemJournalType</span><span class="sxs-lookup"><span data-stu-id="95a00-561">ReqItemJournalType</span></span>|
|<span data-ttu-id="95a00-562">ReqItemTableWizardPurpose</span><span class="sxs-lookup"><span data-stu-id="95a00-562">ReqItemTableWizardPurpose</span></span>|
|<span data-ttu-id="95a00-563">ReqMarkUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-563">ReqMarkUpdate</span></span>|
|<span data-ttu-id="95a00-564">ReqPeggingAssignmentType</span><span class="sxs-lookup"><span data-stu-id="95a00-564">ReqPeggingAssignmentType</span></span>|
|<span data-ttu-id="95a00-565">ReqPeggingType</span><span class="sxs-lookup"><span data-stu-id="95a00-565">ReqPeggingType</span></span>|
|<span data-ttu-id="95a00-566">ReqPlannedOrderLeveling</span><span class="sxs-lookup"><span data-stu-id="95a00-566">ReqPlannedOrderLeveling</span></span>|
|<span data-ttu-id="95a00-567">ReqPlanType</span><span class="sxs-lookup"><span data-stu-id="95a00-567">ReqPlanType</span></span>|
|<span data-ttu-id="95a00-568">ReqPOStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-568">ReqPOStatus</span></span>|
|<span data-ttu-id="95a00-569">ReqQtyAmount</span><span class="sxs-lookup"><span data-stu-id="95a00-569">ReqQtyAmount</span></span>|
|<span data-ttu-id="95a00-570">ReqRefType</span><span class="sxs-lookup"><span data-stu-id="95a00-570">ReqRefType</span></span>|
|<span data-ttu-id="95a00-571">ReqRefTypeShort</span><span class="sxs-lookup"><span data-stu-id="95a00-571">ReqRefTypeShort</span></span>|
|<span data-ttu-id="95a00-572">ReqRefTypeTrunc</span><span class="sxs-lookup"><span data-stu-id="95a00-572">ReqRefTypeTrunc</span></span>|
|<span data-ttu-id="95a00-573">ReqTraceMessageType</span><span class="sxs-lookup"><span data-stu-id="95a00-573">ReqTraceMessageType</span></span>|
|<span data-ttu-id="95a00-574">ReqTransFuturesActionPartType</span><span class="sxs-lookup"><span data-stu-id="95a00-574">ReqTransFuturesActionPartType</span></span>|
|<span data-ttu-id="95a00-575">ReturnCodeType</span><span class="sxs-lookup"><span data-stu-id="95a00-575">ReturnCodeType</span></span>|
|<span data-ttu-id="95a00-576">ReturnCycleTimeScope</span><span class="sxs-lookup"><span data-stu-id="95a00-576">ReturnCycleTimeScope</span></span>|
|<span data-ttu-id="95a00-577">ReturnReasonCodeDispExtended</span><span class="sxs-lookup"><span data-stu-id="95a00-577">ReturnReasonCodeDispExtended</span></span>|
|<span data-ttu-id="95a00-578">ReturnReasonDispCode</span><span class="sxs-lookup"><span data-stu-id="95a00-578">ReturnReasonDispCode</span></span>|
|<span data-ttu-id="95a00-579">ReturnUpdateAction</span><span class="sxs-lookup"><span data-stu-id="95a00-579">ReturnUpdateAction</span></span>|
|<span data-ttu-id="95a00-580">RouteFormula</span><span class="sxs-lookup"><span data-stu-id="95a00-580">RouteFormula</span></span>|
|<span data-ttu-id="95a00-581">RouteOprPriority</span><span class="sxs-lookup"><span data-stu-id="95a00-581">RouteOprPriority</span></span>|
|<span data-ttu-id="95a00-582">SalesBasketType</span><span class="sxs-lookup"><span data-stu-id="95a00-582">SalesBasketType</span></span>|
|<span data-ttu-id="95a00-583">SalesBatch</span><span class="sxs-lookup"><span data-stu-id="95a00-583">SalesBatch</span></span>|
|<span data-ttu-id="95a00-584">SalesCheckForPickup</span><span class="sxs-lookup"><span data-stu-id="95a00-584">SalesCheckForPickup</span></span>|
|<span data-ttu-id="95a00-585">SalesCheckQtyCachKey</span><span class="sxs-lookup"><span data-stu-id="95a00-585">SalesCheckQtyCachKey</span></span>|
|<span data-ttu-id="95a00-586">SalesDeliveryTimeState</span><span class="sxs-lookup"><span data-stu-id="95a00-586">SalesDeliveryTimeState</span></span>|
|<span data-ttu-id="95a00-587">SalesDocumentTimezonePreference</span><span class="sxs-lookup"><span data-stu-id="95a00-587">SalesDocumentTimezonePreference</span></span>|
|<span data-ttu-id="95a00-588">SalesPriceDateType</span><span class="sxs-lookup"><span data-stu-id="95a00-588">SalesPriceDateType</span></span>|
|<span data-ttu-id="95a00-589">SalesPriceModelBasic</span><span class="sxs-lookup"><span data-stu-id="95a00-589">SalesPriceModelBasic</span></span>|
|<span data-ttu-id="95a00-590">SalesPurchCopy</span><span class="sxs-lookup"><span data-stu-id="95a00-590">SalesPurchCopy</span></span>|
|<span data-ttu-id="95a00-591">SalesPurchCycleAction</span><span class="sxs-lookup"><span data-stu-id="95a00-591">SalesPurchCycleAction</span></span>|
|<span data-ttu-id="95a00-592">SalesPurchGroup</span><span class="sxs-lookup"><span data-stu-id="95a00-592">SalesPurchGroup</span></span>|
|<span data-ttu-id="95a00-593">SalesPurchParmCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="95a00-593">SalesPurchParmCleanUpMode</span></span>|
|<span data-ttu-id="95a00-594">SalesQuotationFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-594">SalesQuotationFilter</span></span>|
|<span data-ttu-id="95a00-595">SalesQuotationLinkToProject</span><span class="sxs-lookup"><span data-stu-id="95a00-595">SalesQuotationLinkToProject</span></span>|
|<span data-ttu-id="95a00-596">SalesQuotationListPage</span><span class="sxs-lookup"><span data-stu-id="95a00-596">SalesQuotationListPage</span></span>|
|<span data-ttu-id="95a00-597">SalesQuotationPriceConversion</span><span class="sxs-lookup"><span data-stu-id="95a00-597">SalesQuotationPriceConversion</span></span>|
|<span data-ttu-id="95a00-598">SalesQuotationPriceSimResult</span><span class="sxs-lookup"><span data-stu-id="95a00-598">SalesQuotationPriceSimResult</span></span>|
|<span data-ttu-id="95a00-599">SalesQuotationTypeListPage</span><span class="sxs-lookup"><span data-stu-id="95a00-599">SalesQuotationTypeListPage</span></span>|
|<span data-ttu-id="95a00-600">SalesShipping</span><span class="sxs-lookup"><span data-stu-id="95a00-600">SalesShipping</span></span>|
|<span data-ttu-id="95a00-601">SalesSourcingOrigin</span><span class="sxs-lookup"><span data-stu-id="95a00-601">SalesSourcingOrigin</span></span>|
|<span data-ttu-id="95a00-602">SalesStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-602">SalesStatus</span></span>|
|<span data-ttu-id="95a00-603">SalesTableFormId</span><span class="sxs-lookup"><span data-stu-id="95a00-603">SalesTableFormId</span></span>|
|<span data-ttu-id="95a00-604">SalesTableListPage</span><span class="sxs-lookup"><span data-stu-id="95a00-604">SalesTableListPage</span></span>|
|<span data-ttu-id="95a00-605">SalesTableMode</span><span class="sxs-lookup"><span data-stu-id="95a00-605">SalesTableMode</span></span>|
|<span data-ttu-id="95a00-606">SalesType</span><span class="sxs-lookup"><span data-stu-id="95a00-606">SalesType</span></span>|
|<span data-ttu-id="95a00-607">SalesUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-607">SalesUpdate</span></span>|
|<span data-ttu-id="95a00-608">ShipCarrierDlvType</span><span class="sxs-lookup"><span data-stu-id="95a00-608">ShipCarrierDlvType</span></span>|
|<span data-ttu-id="95a00-609">ShipCarrierFreightApplied</span><span class="sxs-lookup"><span data-stu-id="95a00-609">ShipCarrierFreightApplied</span></span>|
|<span data-ttu-id="95a00-610">ShipCarrierMkUpFreight</span><span class="sxs-lookup"><span data-stu-id="95a00-610">ShipCarrierMkUpFreight</span></span>|
|<span data-ttu-id="95a00-611">SMAInvoiceProjectSelection</span><span class="sxs-lookup"><span data-stu-id="95a00-611">SMAInvoiceProjectSelection</span></span>|
|<span data-ttu-id="95a00-612">SMAItemSetupType</span><span class="sxs-lookup"><span data-stu-id="95a00-612">SMAItemSetupType</span></span>|
|<span data-ttu-id="95a00-613">SMAProjectSelection</span><span class="sxs-lookup"><span data-stu-id="95a00-613">SMAProjectSelection</span></span>|
|<span data-ttu-id="95a00-614">SMAReasonType</span><span class="sxs-lookup"><span data-stu-id="95a00-614">SMAReasonType</span></span>|
|<span data-ttu-id="95a00-615">SMAServiceBOMChangeAction</span><span class="sxs-lookup"><span data-stu-id="95a00-615">SMAServiceBOMChangeAction</span></span>|
|<span data-ttu-id="95a00-616">SMAServiceFunctionType</span><span class="sxs-lookup"><span data-stu-id="95a00-616">SMAServiceFunctionType</span></span>|
|<span data-ttu-id="95a00-617">SMAServiceLevelAgreementLogType</span><span class="sxs-lookup"><span data-stu-id="95a00-617">SMAServiceLevelAgreementLogType</span></span>|
|<span data-ttu-id="95a00-618">SMAServiceOrderActionType</span><span class="sxs-lookup"><span data-stu-id="95a00-618">SMAServiceOrderActionType</span></span>|
|<span data-ttu-id="95a00-619">SMAServiceOrderFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-619">SMAServiceOrderFilter</span></span>|
|<span data-ttu-id="95a00-620">SMAServiceOrderOrigin</span><span class="sxs-lookup"><span data-stu-id="95a00-620">SMAServiceOrderOrigin</span></span>|
|<span data-ttu-id="95a00-621">SMAServiceOrderProgress</span><span class="sxs-lookup"><span data-stu-id="95a00-621">SMAServiceOrderProgress</span></span>|
|<span data-ttu-id="95a00-622">SMAServiceTaskTitleOption</span><span class="sxs-lookup"><span data-stu-id="95a00-622">SMAServiceTaskTitleOption</span></span>|
|<span data-ttu-id="95a00-623">SMASubscriptionPeriodType</span><span class="sxs-lookup"><span data-stu-id="95a00-623">SMASubscriptionPeriodType</span></span>|
|<span data-ttu-id="95a00-624">SMAWizardCreateType</span><span class="sxs-lookup"><span data-stu-id="95a00-624">SMAWizardCreateType</span></span>|
|<span data-ttu-id="95a00-625">smmAccountNumToCreate</span><span class="sxs-lookup"><span data-stu-id="95a00-625">smmAccountNumToCreate</span></span>|
|<span data-ttu-id="95a00-626">smmActivityParentType</span><span class="sxs-lookup"><span data-stu-id="95a00-626">smmActivityParentType</span></span>|
|<span data-ttu-id="95a00-627">smmAppointmentNThInstance</span><span class="sxs-lookup"><span data-stu-id="95a00-627">smmAppointmentNThInstance</span></span>|
|<span data-ttu-id="95a00-628">smmBusinessRelationsListFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-628">smmBusinessRelationsListFilter</span></span>|
|<span data-ttu-id="95a00-629">smmBusRelTypeSourceTable</span><span class="sxs-lookup"><span data-stu-id="95a00-629">smmBusRelTypeSourceTable</span></span>|
|<span data-ttu-id="95a00-630">smmCampaignBroadcastType</span><span class="sxs-lookup"><span data-stu-id="95a00-630">smmCampaignBroadcastType</span></span>|
|<span data-ttu-id="95a00-631">smmCampaignProjectJournalType</span><span class="sxs-lookup"><span data-stu-id="95a00-631">smmCampaignProjectJournalType</span></span>|
|<span data-ttu-id="95a00-632">smmCampaignResponse</span><span class="sxs-lookup"><span data-stu-id="95a00-632">smmCampaignResponse</span></span>|
|<span data-ttu-id="95a00-633">smmCampaignsListFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-633">smmCampaignsListFilter</span></span>|
|<span data-ttu-id="95a00-634">smmContactsListFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-634">smmContactsListFilter</span></span>|
|<span data-ttu-id="95a00-635">smmCreateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="95a00-635">smmCreateOpportunityOptions</span></span>|
|<span data-ttu-id="95a00-636">smmDisplayEMailInOutlook</span><span class="sxs-lookup"><span data-stu-id="95a00-636">smmDisplayEMailInOutlook</span></span>|
|<span data-ttu-id="95a00-637">smmDragDropObjectType</span><span class="sxs-lookup"><span data-stu-id="95a00-637">smmDragDropObjectType</span></span>|
|<span data-ttu-id="95a00-638">smmDupMethods</span><span class="sxs-lookup"><span data-stu-id="95a00-638">smmDupMethods</span></span>|
|<span data-ttu-id="95a00-639">smmEMailSMS</span><span class="sxs-lookup"><span data-stu-id="95a00-639">smmEMailSMS</span></span>|
|<span data-ttu-id="95a00-640">smmEntityToCreate</span><span class="sxs-lookup"><span data-stu-id="95a00-640">smmEntityToCreate</span></span>|
|<span data-ttu-id="95a00-641">smmFieldDelimiters</span><span class="sxs-lookup"><span data-stu-id="95a00-641">smmFieldDelimiters</span></span>|
|<span data-ttu-id="95a00-642">smmLeadsListFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-642">smmLeadsListFilter</span></span>|
|<span data-ttu-id="95a00-643">smmLogType</span><span class="sxs-lookup"><span data-stu-id="95a00-643">smmLogType</span></span>|
|<span data-ttu-id="95a00-644">smmOpportunitiesListFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-644">smmOpportunitiesListFilter</span></span>|
|<span data-ttu-id="95a00-645">smmOpportunityAssociation</span><span class="sxs-lookup"><span data-stu-id="95a00-645">smmOpportunityAssociation</span></span>|
|<span data-ttu-id="95a00-646">smmOutlookContactDeleteAction</span><span class="sxs-lookup"><span data-stu-id="95a00-646">smmOutlookContactDeleteAction</span></span>|
|<span data-ttu-id="95a00-647">smmOutlookRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="95a00-647">smmOutlookRecurrenceType</span></span>|
|<span data-ttu-id="95a00-648">smmOutlookSyncPrinciple</span><span class="sxs-lookup"><span data-stu-id="95a00-648">smmOutlookSyncPrinciple</span></span>|
|<span data-ttu-id="95a00-649">smmOutlookUpdateAction</span><span class="sxs-lookup"><span data-stu-id="95a00-649">smmOutlookUpdateAction</span></span>|
|<span data-ttu-id="95a00-650">smmProjectNewExisting</span><span class="sxs-lookup"><span data-stu-id="95a00-650">smmProjectNewExisting</span></span>|
|<span data-ttu-id="95a00-651">smmQuotationAccountType</span><span class="sxs-lookup"><span data-stu-id="95a00-651">smmQuotationAccountType</span></span>|
|<span data-ttu-id="95a00-652">smmQuotationStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-652">smmQuotationStatus</span></span>|
|<span data-ttu-id="95a00-653">smmRecordDelimiters</span><span class="sxs-lookup"><span data-stu-id="95a00-653">smmRecordDelimiters</span></span>|
|<span data-ttu-id="95a00-654">smmSalesUnitMemberRelation</span><span class="sxs-lookup"><span data-stu-id="95a00-654">smmSalesUnitMemberRelation</span></span>|
|<span data-ttu-id="95a00-655">SmmSourceTypeList</span><span class="sxs-lookup"><span data-stu-id="95a00-655">SmmSourceTypeList</span></span>|
|<span data-ttu-id="95a00-656">smmSwotType</span><span class="sxs-lookup"><span data-stu-id="95a00-656">smmSwotType</span></span>|
|<span data-ttu-id="95a00-657">smmTransLogUpdateAction</span><span class="sxs-lookup"><span data-stu-id="95a00-657">smmTransLogUpdateAction</span></span>|
|<span data-ttu-id="95a00-658">smmUpdateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="95a00-658">smmUpdateOpportunityOptions</span></span>|
|<span data-ttu-id="95a00-659">smmWarningError</span><span class="sxs-lookup"><span data-stu-id="95a00-659">smmWarningError</span></span>|
|<span data-ttu-id="95a00-660">SMAActiveAll</span><span class="sxs-lookup"><span data-stu-id="95a00-660">SMAActiveAll</span></span>|
|<span data-ttu-id="95a00-661">SMAAgreementFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-661">SMAAgreementFilter</span></span>|
|<span data-ttu-id="95a00-662">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="95a00-662">SMAAgreementTableListPageType</span></span>|
|<span data-ttu-id="95a00-663">TAMCustRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-663">TAMCustRebateApprovalStatus</span></span>|
|<span data-ttu-id="95a00-664">TAMFundStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-664">TAMFundStatus</span></span>|
|<span data-ttu-id="95a00-665">TAMFundType</span><span class="sxs-lookup"><span data-stu-id="95a00-665">TAMFundType</span></span>|
|<span data-ttu-id="95a00-666">TAMPromoCustomerType</span><span class="sxs-lookup"><span data-stu-id="95a00-666">TAMPromoCustomerType</span></span>|
|<span data-ttu-id="95a00-667">TAMPromoMerchEvent</span><span class="sxs-lookup"><span data-stu-id="95a00-667">TAMPromoMerchEvent</span></span>|
|<span data-ttu-id="95a00-668">TAMPromoMgmtApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-668">TAMPromoMgmtApprovalStatus</span></span>|
|<span data-ttu-id="95a00-669">TAMPromotionDate</span><span class="sxs-lookup"><span data-stu-id="95a00-669">TAMPromotionDate</span></span>|
|<span data-ttu-id="95a00-670">TAMPromotionMode</span><span class="sxs-lookup"><span data-stu-id="95a00-670">TAMPromotionMode</span></span>|
|<span data-ttu-id="95a00-671">TAMRebateCustInclusive</span><span class="sxs-lookup"><span data-stu-id="95a00-671">TAMRebateCustInclusive</span></span>|
|<span data-ttu-id="95a00-672">TAMRebateLineBreakType</span><span class="sxs-lookup"><span data-stu-id="95a00-672">TAMRebateLineBreakType</span></span>|
|<span data-ttu-id="95a00-673">TAMRebateStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-673">TAMRebateStatus</span></span>|
|<span data-ttu-id="95a00-674">TAMRebateUnitType</span><span class="sxs-lookup"><span data-stu-id="95a00-674">TAMRebateUnitType</span></span>|
|<span data-ttu-id="95a00-675">TAMRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="95a00-675">TAMRebateUOMOption</span></span>|
|<span data-ttu-id="95a00-676">TAMVendRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-676">TAMVendRebateApprovalStatus</span></span>|
|<span data-ttu-id="95a00-677">TAMVendRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="95a00-677">TAMVendRebateCalcDateType</span></span>|
|<span data-ttu-id="95a00-678">TAMVendRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="95a00-678">TAMVendRebateTakenFrom</span></span>|
|<span data-ttu-id="95a00-679">TAMVendRebateTransactionType</span><span class="sxs-lookup"><span data-stu-id="95a00-679">TAMVendRebateTransactionType</span></span>|
|<span data-ttu-id="95a00-680">TaxModuleType</span><span class="sxs-lookup"><span data-stu-id="95a00-680">TaxModuleType</span></span>|
|<span data-ttu-id="95a00-681">TaxSourceType</span><span class="sxs-lookup"><span data-stu-id="95a00-681">TaxSourceType</span></span>|
|<span data-ttu-id="95a00-682">TMSAccessorialAssignmentLevel</span><span class="sxs-lookup"><span data-stu-id="95a00-682">TMSAccessorialAssignmentLevel</span></span>|
|<span data-ttu-id="95a00-683">TMSAccessorialAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="95a00-683">TMSAccessorialAssignmentTarget</span></span>|
|<span data-ttu-id="95a00-684">TMSAccessorialDeliveryType</span><span class="sxs-lookup"><span data-stu-id="95a00-684">TMSAccessorialDeliveryType</span></span>|
|<span data-ttu-id="95a00-685">TMSAccessorialType</span><span class="sxs-lookup"><span data-stu-id="95a00-685">TMSAccessorialType</span></span>|
|<span data-ttu-id="95a00-686">TMSAppointmentAlert</span><span class="sxs-lookup"><span data-stu-id="95a00-686">TMSAppointmentAlert</span></span>|
|<span data-ttu-id="95a00-687">TMSDiscountResultType</span><span class="sxs-lookup"><span data-stu-id="95a00-687">TMSDiscountResultType</span></span>|
|<span data-ttu-id="95a00-688">TMSDiscountType</span><span class="sxs-lookup"><span data-stu-id="95a00-688">TMSDiscountType</span></span>|
|<span data-ttu-id="95a00-689">TMSFeeType</span><span class="sxs-lookup"><span data-stu-id="95a00-689">TMSFeeType</span></span>|
|<span data-ttu-id="95a00-690">TMSFreightBillMatchStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-690">TMSFreightBillMatchStatus</span></span>|
|<span data-ttu-id="95a00-691">TMSFreightBillReconcileType</span><span class="sxs-lookup"><span data-stu-id="95a00-691">TMSFreightBillReconcileType</span></span>|
|<span data-ttu-id="95a00-692">TMSFwkErrorType</span><span class="sxs-lookup"><span data-stu-id="95a00-692">TMSFwkErrorType</span></span>|
|<span data-ttu-id="95a00-693">TMSHubPosition</span><span class="sxs-lookup"><span data-stu-id="95a00-693">TMSHubPosition</span></span>|
|<span data-ttu-id="95a00-694">TMSInvoiceAccountType</span><span class="sxs-lookup"><span data-stu-id="95a00-694">TMSInvoiceAccountType</span></span>|
|<span data-ttu-id="95a00-695">TMSLineType</span><span class="sxs-lookup"><span data-stu-id="95a00-695">TMSLineType</span></span>|
|<span data-ttu-id="95a00-696">TMSLoadBuildSessionState</span><span class="sxs-lookup"><span data-stu-id="95a00-696">TMSLoadBuildSessionState</span></span>|
|<span data-ttu-id="95a00-697">TMSLoadTender</span><span class="sxs-lookup"><span data-stu-id="95a00-697">TMSLoadTender</span></span>|
|<span data-ttu-id="95a00-698">TMSLookupType</span><span class="sxs-lookup"><span data-stu-id="95a00-698">TMSLookupType</span></span>|
|<span data-ttu-id="95a00-699">TMSNumberSequenceType</span><span class="sxs-lookup"><span data-stu-id="95a00-699">TMSNumberSequenceType</span></span>|
|<span data-ttu-id="95a00-700">TMSOverrideLocationType</span><span class="sxs-lookup"><span data-stu-id="95a00-700">TMSOverrideLocationType</span></span>|
|<span data-ttu-id="95a00-701">TMSRecurrenceDays</span><span class="sxs-lookup"><span data-stu-id="95a00-701">TMSRecurrenceDays</span></span>|
|<span data-ttu-id="95a00-702">TMSRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="95a00-702">TMSRecurrenceType</span></span>|
|<span data-ttu-id="95a00-703">TMSRecurrenceWeeks</span><span class="sxs-lookup"><span data-stu-id="95a00-703">TMSRecurrenceWeeks</span></span>|
|<span data-ttu-id="95a00-704">TMSResponsibleForPayment</span><span class="sxs-lookup"><span data-stu-id="95a00-704">TMSResponsibleForPayment</span></span>|
|<span data-ttu-id="95a00-705">TMSRouteStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-705">TMSRouteStatus</span></span>|
|<span data-ttu-id="95a00-706">TMSSalesPurchTransfer</span><span class="sxs-lookup"><span data-stu-id="95a00-706">TMSSalesPurchTransfer</span></span>|
|<span data-ttu-id="95a00-707">TMSTableRef</span><span class="sxs-lookup"><span data-stu-id="95a00-707">TMSTableRef</span></span>|
|<span data-ttu-id="95a00-708">TMSTransportationType</span><span class="sxs-lookup"><span data-stu-id="95a00-708">TMSTransportationType</span></span>|
|<span data-ttu-id="95a00-709">TMSTransportRefType</span><span class="sxs-lookup"><span data-stu-id="95a00-709">TMSTransportRefType</span></span>|
|<span data-ttu-id="95a00-710">TMSTransportTypeFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-710">TMSTransportTypeFilter</span></span>|
|<span data-ttu-id="95a00-711">TMSUOM</span><span class="sxs-lookup"><span data-stu-id="95a00-711">TMSUOM</span></span>|
|<span data-ttu-id="95a00-712">TMSZoneType</span><span class="sxs-lookup"><span data-stu-id="95a00-712">TMSZoneType</span></span>|
|<span data-ttu-id="95a00-713">TradeCurencyConversion</span><span class="sxs-lookup"><span data-stu-id="95a00-713">TradeCurencyConversion</span></span>|
|<span data-ttu-id="95a00-714">TradeLineDlvType</span><span class="sxs-lookup"><span data-stu-id="95a00-714">TradeLineDlvType</span></span>|
|<span data-ttu-id="95a00-715">TradeNonStockedConversionChangeType</span><span class="sxs-lookup"><span data-stu-id="95a00-715">TradeNonStockedConversionChangeType</span></span>|
|<span data-ttu-id="95a00-716">TradeNonStockedConversionIssue</span><span class="sxs-lookup"><span data-stu-id="95a00-716">TradeNonStockedConversionIssue</span></span>|
|<span data-ttu-id="95a00-717">TradeNonStockedConversionResolveUndo</span><span class="sxs-lookup"><span data-stu-id="95a00-717">TradeNonStockedConversionResolveUndo</span></span>|
|<span data-ttu-id="95a00-718">TradePrintType</span><span class="sxs-lookup"><span data-stu-id="95a00-718">TradePrintType</span></span>|
|<span data-ttu-id="95a00-719">TradeTable2LineUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-719">TradeTable2LineUpdate</span></span>|
|<span data-ttu-id="95a00-720">VendNotificationCategorySelection</span><span class="sxs-lookup"><span data-stu-id="95a00-720">VendNotificationCategorySelection</span></span>|
|<span data-ttu-id="95a00-721">VendNotificationStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-721">VendNotificationStatus</span></span>|
|<span data-ttu-id="95a00-722">VendPackingSlipTransTimeStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-722">VendPackingSlipTransTimeStatus</span></span>|
|<span data-ttu-id="95a00-723">VendRequestCompanyType</span><span class="sxs-lookup"><span data-stu-id="95a00-723">VendRequestCompanyType</span></span>|
|<span data-ttu-id="95a00-724">VendRequestOriginatedByType</span><span class="sxs-lookup"><span data-stu-id="95a00-724">VendRequestOriginatedByType</span></span>|
|<span data-ttu-id="95a00-725">VendRequestQuestionnairesCompleted</span><span class="sxs-lookup"><span data-stu-id="95a00-725">VendRequestQuestionnairesCompleted</span></span>|
|<span data-ttu-id="95a00-726">VendRequestRoleType</span><span class="sxs-lookup"><span data-stu-id="95a00-726">VendRequestRoleType</span></span>|
|<span data-ttu-id="95a00-727">VendReviewRatingScore</span><span class="sxs-lookup"><span data-stu-id="95a00-727">VendReviewRatingScore</span></span>|
|<span data-ttu-id="95a00-728">VersioningAction</span><span class="sxs-lookup"><span data-stu-id="95a00-728">VersioningAction</span></span>|
|<span data-ttu-id="95a00-729">WHSAllowMaterialOverPick</span><span class="sxs-lookup"><span data-stu-id="95a00-729">WHSAllowMaterialOverPick</span></span>|
|<span data-ttu-id="95a00-730">WHSApplicableDemand</span><span class="sxs-lookup"><span data-stu-id="95a00-730">WHSApplicableDemand</span></span>|
|<span data-ttu-id="95a00-731">WHSAutoReleaseContainerAtContainerClose</span><span class="sxs-lookup"><span data-stu-id="95a00-731">WHSAutoReleaseContainerAtContainerClose</span></span>|
|<span data-ttu-id="95a00-732">WHSAutoReleaseOrderType</span><span class="sxs-lookup"><span data-stu-id="95a00-732">WHSAutoReleaseOrderType</span></span>|
|<span data-ttu-id="95a00-733">WHSBreakCluster</span><span class="sxs-lookup"><span data-stu-id="95a00-733">WHSBreakCluster</span></span>|
|<span data-ttu-id="95a00-734">WHSContainerizationQueryType</span><span class="sxs-lookup"><span data-stu-id="95a00-734">WHSContainerizationQueryType</span></span>|
|<span data-ttu-id="95a00-735">WHSContainerPackingStrategy</span><span class="sxs-lookup"><span data-stu-id="95a00-735">WHSContainerPackingStrategy</span></span>|
|<span data-ttu-id="95a00-736">WHSContainerTableFormViewType</span><span class="sxs-lookup"><span data-stu-id="95a00-736">WHSContainerTableFormViewType</span></span>|
|<span data-ttu-id="95a00-737">WHSCrossDockFulfillmentStrategy</span><span class="sxs-lookup"><span data-stu-id="95a00-737">WHSCrossDockFulfillmentStrategy</span></span>|
|<span data-ttu-id="95a00-738">WHSCustJourType</span><span class="sxs-lookup"><span data-stu-id="95a00-738">WHSCustJourType</span></span>|
|<span data-ttu-id="95a00-739">WHSCycleCountPlanStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-739">WHSCycleCountPlanStatus</span></span>|
|<span data-ttu-id="95a00-740">WHSDefaultDataField</span><span class="sxs-lookup"><span data-stu-id="95a00-740">WHSDefaultDataField</span></span>|
|<span data-ttu-id="95a00-741">WHSFilterModule</span><span class="sxs-lookup"><span data-stu-id="95a00-741">WHSFilterModule</span></span>|
|<span data-ttu-id="95a00-742">WHSHistoryEvent</span><span class="sxs-lookup"><span data-stu-id="95a00-742">WHSHistoryEvent</span></span>|
|<span data-ttu-id="95a00-743">WHSLoadPlanning</span><span class="sxs-lookup"><span data-stu-id="95a00-743">WHSLoadPlanning</span></span>|
|<span data-ttu-id="95a00-744">WHSLoadPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="95a00-744">WHSLoadPostMethodsBase</span></span>|
|<span data-ttu-id="95a00-745">WhsLoadReplenishment</span><span class="sxs-lookup"><span data-stu-id="95a00-745">WhsLoadReplenishment</span></span>|
|<span data-ttu-id="95a00-746">WHSLoadTable</span><span class="sxs-lookup"><span data-stu-id="95a00-746">WHSLoadTable</span></span>|
|<span data-ttu-id="95a00-747">WHSLocDirStrategy</span><span class="sxs-lookup"><span data-stu-id="95a00-747">WHSLocDirStrategy</span></span>|
|<span data-ttu-id="95a00-748">WHSLPAssignment</span><span class="sxs-lookup"><span data-stu-id="95a00-748">WHSLPAssignment</span></span>|
|<span data-ttu-id="95a00-749">WHSLPWFilterType</span><span class="sxs-lookup"><span data-stu-id="95a00-749">WHSLPWFilterType</span></span>|
|<span data-ttu-id="95a00-750">WHSManifestAt</span><span class="sxs-lookup"><span data-stu-id="95a00-750">WHSManifestAt</span></span>|
|<span data-ttu-id="95a00-751">WHSManifestRequirementContainerGroup</span><span class="sxs-lookup"><span data-stu-id="95a00-751">WHSManifestRequirementContainerGroup</span></span>|
|<span data-ttu-id="95a00-752">WHSMenuItemDirectedBy</span><span class="sxs-lookup"><span data-stu-id="95a00-752">WHSMenuItemDirectedBy</span></span>|
|<span data-ttu-id="95a00-753">WHSMixedLPReceivingMode</span><span class="sxs-lookup"><span data-stu-id="95a00-753">WHSMixedLPReceivingMode</span></span>|
|<span data-ttu-id="95a00-754">WHSMixingLogicTables</span><span class="sxs-lookup"><span data-stu-id="95a00-754">WHSMixingLogicTables</span></span>|
|<span data-ttu-id="95a00-755">WHSMobileAppPagePattern</span><span class="sxs-lookup"><span data-stu-id="95a00-755">WHSMobileAppPagePattern</span></span>|
|<span data-ttu-id="95a00-756">WHSOriginType</span><span class="sxs-lookup"><span data-stu-id="95a00-756">WHSOriginType</span></span>|
|<span data-ttu-id="95a00-757">WHSPickOldestBatch</span><span class="sxs-lookup"><span data-stu-id="95a00-757">WHSPickOldestBatch</span></span>|
|<span data-ttu-id="95a00-758">WHSPostMethodBaseKanban</span><span class="sxs-lookup"><span data-stu-id="95a00-758">WHSPostMethodBaseKanban</span></span>|
|<span data-ttu-id="95a00-759">WHSPostMethodBaseKanbanOptional</span><span class="sxs-lookup"><span data-stu-id="95a00-759">WHSPostMethodBaseKanbanOptional</span></span>|
|<span data-ttu-id="95a00-760">WHSPostMethodBaseOptional</span><span class="sxs-lookup"><span data-stu-id="95a00-760">WHSPostMethodBaseOptional</span></span>|
|<span data-ttu-id="95a00-761">WHSPostMethodBaseProd</span><span class="sxs-lookup"><span data-stu-id="95a00-761">WHSPostMethodBaseProd</span></span>|
|<span data-ttu-id="95a00-762">WHSPostMethodBaseProdOptional</span><span class="sxs-lookup"><span data-stu-id="95a00-762">WHSPostMethodBaseProdOptional</span></span>|
|<span data-ttu-id="95a00-763">WHSPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="95a00-763">WHSPostMethodsBase</span></span>|
|<span data-ttu-id="95a00-764">WHSQtyPct</span><span class="sxs-lookup"><span data-stu-id="95a00-764">WHSQtyPct</span></span>|
|<span data-ttu-id="95a00-765">WHSReleaseQuantitySpecification</span><span class="sxs-lookup"><span data-stu-id="95a00-765">WHSReleaseQuantitySpecification</span></span>|
|<span data-ttu-id="95a00-766">WHSReplenishmentDependentWorkBlockingPolicy</span><span class="sxs-lookup"><span data-stu-id="95a00-766">WHSReplenishmentDependentWorkBlockingPolicy</span></span>|
|<span data-ttu-id="95a00-767">WHSReservationHierarchyLevelStrategyType</span><span class="sxs-lookup"><span data-stu-id="95a00-767">WHSReservationHierarchyLevelStrategyType</span></span>|
|<span data-ttu-id="95a00-768">WHSReservationStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-768">WHSReservationStatus</span></span>|
|<span data-ttu-id="95a00-769">WHSUseFixedLocations</span><span class="sxs-lookup"><span data-stu-id="95a00-769">WHSUseFixedLocations</span></span>|
|<span data-ttu-id="95a00-770">WHSWorkActivity</span><span class="sxs-lookup"><span data-stu-id="95a00-770">WHSWorkActivity</span></span>|
|<span data-ttu-id="95a00-771">WHSWorkClusterStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-771">WHSWorkClusterStatus</span></span>|
|<span data-ttu-id="95a00-772">WHSWorkCreationProcess</span><span class="sxs-lookup"><span data-stu-id="95a00-772">WHSWorkCreationProcess</span></span>|
|<span data-ttu-id="95a00-773">WHSWorkExceptionLogStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-773">WHSWorkExceptionLogStatus</span></span>|
|<span data-ttu-id="95a00-774">WHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="95a00-774">WHSWorkExecuteMode</span></span>|
|<span data-ttu-id="95a00-775">WHSWorkListPageFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-775">WHSWorkListPageFilter</span></span>|
|<span data-ttu-id="95a00-776">WHSWorkPrintOption</span><span class="sxs-lookup"><span data-stu-id="95a00-776">WHSWorkPrintOption</span></span>|
|<span data-ttu-id="95a00-777">WHSWorkPutFlow</span><span class="sxs-lookup"><span data-stu-id="95a00-777">WHSWorkPutFlow</span></span>|
|<span data-ttu-id="95a00-778">WHSWorkTransType</span><span class="sxs-lookup"><span data-stu-id="95a00-778">WHSWorkTransType</span></span>|
|<span data-ttu-id="95a00-779">WHSWorkType</span><span class="sxs-lookup"><span data-stu-id="95a00-779">WHSWorkType</span></span>|
|<span data-ttu-id="95a00-780">WHSWorkTypePickPut</span><span class="sxs-lookup"><span data-stu-id="95a00-780">WHSWorkTypePickPut</span></span>|
|<span data-ttu-id="95a00-781">WMSAutoAddStop</span><span class="sxs-lookup"><span data-stu-id="95a00-781">WMSAutoAddStop</span></span>|
|<span data-ttu-id="95a00-782">WMSFreightChargeTerms</span><span class="sxs-lookup"><span data-stu-id="95a00-782">WMSFreightChargeTerms</span></span>|
|<span data-ttu-id="95a00-783">WMSFreightCounted</span><span class="sxs-lookup"><span data-stu-id="95a00-783">WMSFreightCounted</span></span>|
|<span data-ttu-id="95a00-784">WMSHandlingType</span><span class="sxs-lookup"><span data-stu-id="95a00-784">WMSHandlingType</span></span>|
|<span data-ttu-id="95a00-785">WMSLocationType</span><span class="sxs-lookup"><span data-stu-id="95a00-785">WMSLocationType</span></span>|
|<span data-ttu-id="95a00-786">WMSPackageType</span><span class="sxs-lookup"><span data-stu-id="95a00-786">WMSPackageType</span></span>|
|<span data-ttu-id="95a00-787">WMSPalletMovementProcessing</span><span class="sxs-lookup"><span data-stu-id="95a00-787">WMSPalletMovementProcessing</span></span>|
|<span data-ttu-id="95a00-788">WMSPhysicalUpdateStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-788">WMSPhysicalUpdateStatus</span></span>|
|<span data-ttu-id="95a00-789">WMSReceiptStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-789">WMSReceiptStatus</span></span>|
|<span data-ttu-id="95a00-790">WMSReservationMethod</span><span class="sxs-lookup"><span data-stu-id="95a00-790">WMSReservationMethod</span></span>|
|<span data-ttu-id="95a00-791">WMSReservationMethodInternal</span><span class="sxs-lookup"><span data-stu-id="95a00-791">WMSReservationMethodInternal</span></span>|
|<span data-ttu-id="95a00-792">WMSShipmentStatus</span><span class="sxs-lookup"><span data-stu-id="95a00-792">WMSShipmentStatus</span></span>|
|<span data-ttu-id="95a00-793">WMSShipmentType</span><span class="sxs-lookup"><span data-stu-id="95a00-793">WMSShipmentType</span></span>|
|<span data-ttu-id="95a00-794">WMSSpaceUtilInconsistencyGroup</span><span class="sxs-lookup"><span data-stu-id="95a00-794">WMSSpaceUtilInconsistencyGroup</span></span>|
|<span data-ttu-id="95a00-795">WMSSpaceUtilShowBy</span><span class="sxs-lookup"><span data-stu-id="95a00-795">WMSSpaceUtilShowBy</span></span>|
|<span data-ttu-id="95a00-796">WMSSpaceUtilStorageLoadUnitType</span><span class="sxs-lookup"><span data-stu-id="95a00-796">WMSSpaceUtilStorageLoadUnitType</span></span>|
|<span data-ttu-id="95a00-797">WMSStoreAreaType</span><span class="sxs-lookup"><span data-stu-id="95a00-797">WMSStoreAreaType</span></span>|
|<span data-ttu-id="95a00-798">WMSTrailerLoaded</span><span class="sxs-lookup"><span data-stu-id="95a00-798">WMSTrailerLoaded</span></span>|
|<span data-ttu-id="95a00-799">WrkCtrActivityType</span><span class="sxs-lookup"><span data-stu-id="95a00-799">WrkCtrActivityType</span></span>|
|<span data-ttu-id="95a00-800">WrkCtrBulkResReqSearchType</span><span class="sxs-lookup"><span data-stu-id="95a00-800">WrkCtrBulkResReqSearchType</span></span>|
|<span data-ttu-id="95a00-801">WrkCtrCapacityType</span><span class="sxs-lookup"><span data-stu-id="95a00-801">WrkCtrCapacityType</span></span>|
|<span data-ttu-id="95a00-802">WrkCtrCapRefType</span><span class="sxs-lookup"><span data-stu-id="95a00-802">WrkCtrCapRefType</span></span>|
|<span data-ttu-id="95a00-803">WrkCtrCommitState</span><span class="sxs-lookup"><span data-stu-id="95a00-803">WrkCtrCommitState</span></span>|
|<span data-ttu-id="95a00-804">WrkCtrGroupWrkCtr</span><span class="sxs-lookup"><span data-stu-id="95a00-804">WrkCtrGroupWrkCtr</span></span>|
|<span data-ttu-id="95a00-805">WrkCtrSchedulerCommand</span><span class="sxs-lookup"><span data-stu-id="95a00-805">WrkCtrSchedulerCommand</span></span>|
|<span data-ttu-id="95a00-806">WrkCtrSchedulerConstraintType</span><span class="sxs-lookup"><span data-stu-id="95a00-806">WrkCtrSchedulerConstraintType</span></span>|
|<span data-ttu-id="95a00-807">WrkCtrSchedulerLoggerMode</span><span class="sxs-lookup"><span data-stu-id="95a00-807">WrkCtrSchedulerLoggerMode</span></span>|
|<span data-ttu-id="95a00-808">WrkCtrType</span><span class="sxs-lookup"><span data-stu-id="95a00-808">WrkCtrType</span></span>|
|<span data-ttu-id="95a00-809">WrkCtrTypeFilter</span><span class="sxs-lookup"><span data-stu-id="95a00-809">WrkCtrTypeFilter</span></span>|

<span data-ttu-id="95a00-810">以下の列挙型は削除され、拡張可能になりませんでした。</span><span class="sxs-lookup"><span data-stu-id="95a00-810">These enumerations were removed, and not made extensible.</span></span>

| <span data-ttu-id="95a00-811">削除された列挙型</span><span class="sxs-lookup"><span data-stu-id="95a00-811">Enumeration removed</span></span> |
| --------------- |
|<span data-ttu-id="95a00-812">BackorderLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="95a00-812">BackorderLinesListPageMode</span></span>|
|<span data-ttu-id="95a00-813">BackorderPurchLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="95a00-813">BackorderPurchLinesListPageMode</span></span> |
|<span data-ttu-id="95a00-814">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="95a00-814">EcoResProductPerCompanyListPageType</span></span> |
|<span data-ttu-id="95a00-815">ReturnTableListPageType</span><span class="sxs-lookup"><span data-stu-id="95a00-815">ReturnTableListPageType</span></span> |
|<span data-ttu-id="95a00-816">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="95a00-816">SMAAgreementTableListPageType</span></span>|

<span data-ttu-id="95a00-817">拡張可能な列挙型のサポートを改善するために、Foundation の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="95a00-817">Foundation changes were made to improve support for extensible enumerations.</span></span> <span data-ttu-id="95a00-818">**IsExtensible** が **はい** に設定されている列挙型については、**SysPlugin** フレームワークが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-818">The **SysPlugin** framework was enabled for enumerations where **IsExtensible** is set to **Yes**.</span></span> <span data-ttu-id="95a00-819">列挙型の新しい名前に基づく構文で、ビューが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-819">Views were enabled with new name-based syntax for enumerations.</span></span>

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a><span data-ttu-id="95a00-820">DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド</span><span class="sxs-lookup"><span data-stu-id="95a00-820">Data manipulation methods that do not raise DataEvents or missing insert, update, delete pre- and post-data events</span></span>

<span data-ttu-id="95a00-821">一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="95a00-821">As a general practice, you use data methods on tables to raise events that can be used for extending the application.</span></span> <span data-ttu-id="95a00-822">コード ベースは、必ずしもこのプラクティスに従っていませんでした。</span><span class="sxs-lookup"><span data-stu-id="95a00-822">The code base has not always followed this practice.</span></span> <span data-ttu-id="95a00-823">たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="95a00-823">For example, the **doInsert**, **doUpdate**, and **doDelete** data methods and certain table implementations did not make a call to **super()** in the data method.</span></span>

<span data-ttu-id="95a00-824">タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="95a00-824">The **insert**, **update**, and **delete** methods on the type classes have been refactored.</span></span> <span data-ttu-id="95a00-825">データ メソッドで **super()** が確実に呼び出されるように変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="95a00-825">Changes were made so that **super()** is called more consistently in data methods.</span></span> <span data-ttu-id="95a00-826">これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-826">These changes enable extensions to be added to these methods, so that pre- and post-events are now available for extension.</span></span> <span data-ttu-id="95a00-827">次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="95a00-827">The tables where the **insert**, **update**, and **delete** events were enabled for extension are listed in the following table.</span></span>

| <span data-ttu-id="95a00-828">テーブル</span><span class="sxs-lookup"><span data-stu-id="95a00-828">Table</span></span> |
| -------------|
| <span data-ttu-id="95a00-829">InventBlocking</span><span class="sxs-lookup"><span data-stu-id="95a00-829">InventBlocking</span></span>|
| <span data-ttu-id="95a00-830">InventTransferLine</span><span class="sxs-lookup"><span data-stu-id="95a00-830">InventTransferLine</span></span>|
| <span data-ttu-id="95a00-831">Kanban</span><span class="sxs-lookup"><span data-stu-id="95a00-831">Kanban</span></span>|
| <span data-ttu-id="95a00-832">KanbanJob</span><span class="sxs-lookup"><span data-stu-id="95a00-832">KanbanJob</span></span>|
| <span data-ttu-id="95a00-833">KanbanJobPickingList</span><span class="sxs-lookup"><span data-stu-id="95a00-833">KanbanJobPickingList</span></span>|
| <span data-ttu-id="95a00-834">MCRRoyaltyVendTable</span><span class="sxs-lookup"><span data-stu-id="95a00-834">MCRRoyaltyVendTable</span></span>|
| <span data-ttu-id="95a00-835">PdsRebateTable</span><span class="sxs-lookup"><span data-stu-id="95a00-835">PdsRebateTable</span></span>|
| <span data-ttu-id="95a00-836">PmfProdCoBy</span><span class="sxs-lookup"><span data-stu-id="95a00-836">PmfProdCoBy</span></span>|
| <span data-ttu-id="95a00-837">ProdBOM</span><span class="sxs-lookup"><span data-stu-id="95a00-837">ProdBOM</span></span>|
| <span data-ttu-id="95a00-838">ProdRoute</span><span class="sxs-lookup"><span data-stu-id="95a00-838">ProdRoute</span></span>|
| <span data-ttu-id="95a00-839">ProdTable</span><span class="sxs-lookup"><span data-stu-id="95a00-839">ProdTable</span></span>|
| <span data-ttu-id="95a00-840">PurchLine</span><span class="sxs-lookup"><span data-stu-id="95a00-840">PurchLine</span></span>|
| <span data-ttu-id="95a00-841">PurchRFQCaseLine</span><span class="sxs-lookup"><span data-stu-id="95a00-841">PurchRFQCaseLine</span></span>|
| <span data-ttu-id="95a00-842">PurchRFQCaseTable</span><span class="sxs-lookup"><span data-stu-id="95a00-842">PurchRFQCaseTable</span></span>|
| <span data-ttu-id="95a00-843">PurchRFQLine</span><span class="sxs-lookup"><span data-stu-id="95a00-843">PurchRFQLine</span></span>|
| <span data-ttu-id="95a00-844">PurchTable</span><span class="sxs-lookup"><span data-stu-id="95a00-844">PurchTable</span></span>|
| <span data-ttu-id="95a00-845">SalesLine</span><span class="sxs-lookup"><span data-stu-id="95a00-845">SalesLine</span></span>|
| <span data-ttu-id="95a00-846">SalesQuotationLine</span><span class="sxs-lookup"><span data-stu-id="95a00-846">SalesQuotationLine</span></span>|
| <span data-ttu-id="95a00-847">SalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="95a00-847">SalesQuotationTable</span></span>|
| <span data-ttu-id="95a00-848">SalesTable</span><span class="sxs-lookup"><span data-stu-id="95a00-848">SalesTable</span></span>|
| <span data-ttu-id="95a00-849">TAMVendRebateTable</span><span class="sxs-lookup"><span data-stu-id="95a00-849">TAMVendRebateTable</span></span>|
| <span data-ttu-id="95a00-850">WMSOrder</span><span class="sxs-lookup"><span data-stu-id="95a00-850">WMSOrder</span></span>|
| <span data-ttu-id="95a00-851">WMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="95a00-851">WMSOrderTrans</span></span>|

## <a name="exposing-class-members"></a><span data-ttu-id="95a00-852">クラス メンバーの公開</span><span class="sxs-lookup"><span data-stu-id="95a00-852">Exposing class members</span></span>

<span data-ttu-id="95a00-853">アクセス修飾子または新しい parm メソッドの変更の結果、追加のプライベート メンバーをカスタマイズに使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-853">Additional private members are now available for customization as a result of the changes to the access modifier or new parm methods.</span></span> <span data-ttu-id="95a00-854">コマンド チェーン プラットフォーム機能により、保護されたメソッドとメンバーへの拡張クラスのアクセスが有効になります。</span><span class="sxs-lookup"><span data-stu-id="95a00-854">The chain of command platform feature enables extension class access to protected methods and members.</span></span> <span data-ttu-id="95a00-855">コマンド チェーンの詳細については、「[拡張可能な X++: コマンド チェーン](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extensible-x-chain-of-command)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="95a00-855">For more information about chain of command, see [Extensible X++: Chain of Command](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extensible-x-chain-of-command).</span></span>

| <span data-ttu-id="95a00-856">メンバー</span><span class="sxs-lookup"><span data-stu-id="95a00-856">Member</span></span> |
| -------------|
|<span data-ttu-id="95a00-857">AssetPost.ledgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="95a00-857">AssetPost.ledgerJournalTrans</span></span>|
|<span data-ttu-id="95a00-858">クラス DimensionDerivationRule.ledgerDimensionAllocationList</span><span class="sxs-lookup"><span data-stu-id="95a00-858">Class DimensionDerivationRule.ledgerDimensionAllocationList</span></span>|
|<span data-ttu-id="95a00-859">クラス PurchInvoiceJournalCreate.purchTable</span><span class="sxs-lookup"><span data-stu-id="95a00-859">Class PurchInvoiceJournalCreate.purchTable</span></span>|
|<span data-ttu-id="95a00-860">クラス PurchTableType.purchTable</span><span class="sxs-lookup"><span data-stu-id="95a00-860">Class PurchTableType.purchTable</span></span>|
|<span data-ttu-id="95a00-861">クラス SalesInvoiceJournalPost.salesLine</span><span class="sxs-lookup"><span data-stu-id="95a00-861">Class SalesInvoiceJournalPost.salesLine</span></span>|
|<span data-ttu-id="95a00-862">クラス SalesQuotationLineType</span><span class="sxs-lookup"><span data-stu-id="95a00-862">Class SalesQuotationLineType</span></span>|
|<span data-ttu-id="95a00-863">クラス SalesQuotationTableType</span><span class="sxs-lookup"><span data-stu-id="95a00-863">Class SalesQuotationTableType</span></span>|
|<span data-ttu-id="95a00-864">クラス VendorInvoiceLineSourceDocLineItem.purchLine</span><span class="sxs-lookup"><span data-stu-id="95a00-864">Class VendorInvoiceLineSourceDocLineItem.purchLine</span></span>|
|<span data-ttu-id="95a00-865">CustCreditLimit.balanceTotalsCalculated</span><span class="sxs-lookup"><span data-stu-id="95a00-865">CustCreditLimit.balanceTotalsCalculated</span></span>|
|<span data-ttu-id="95a00-866">CustCreditLimit_SalesTable.salesTable</span><span class="sxs-lookup"><span data-stu-id="95a00-866">CustCreditLimit_SalesTable.salesTable</span></span>|
|<span data-ttu-id="95a00-867">フォーム LedgerJournalTransCustPaym.ledgerJournalEngine</span><span class="sxs-lookup"><span data-stu-id="95a00-867">Form LedgerJournalTransCustPaym.ledgerJournalEngine</span></span>|
|<span data-ttu-id="95a00-868">PurchLineType.purchLine</span><span class="sxs-lookup"><span data-stu-id="95a00-868">PurchLineType.purchLine</span></span>|
|<span data-ttu-id="95a00-869">PurchLineType.purchLine_orig</span><span class="sxs-lookup"><span data-stu-id="95a00-869">PurchLineType.purchLine_orig</span></span>|
|<span data-ttu-id="95a00-870">SalesLineType.salesLine</span><span class="sxs-lookup"><span data-stu-id="95a00-870">SalesLineType.salesLine</span></span>|
|<span data-ttu-id="95a00-871">SalesLineType.salesLine_orig</span><span class="sxs-lookup"><span data-stu-id="95a00-871">SalesLineType.salesLine_orig</span></span>|
|<span data-ttu-id="95a00-872">SalesTableType.checkSalesQty</span><span class="sxs-lookup"><span data-stu-id="95a00-872">SalesTableType.checkSalesQty</span></span>|
|<span data-ttu-id="95a00-873">SalesTableType.SalesTable_orig</span><span class="sxs-lookup"><span data-stu-id="95a00-873">SalesTableType.SalesTable_orig</span></span>|
|<span data-ttu-id="95a00-874">WHSControl.data</span><span class="sxs-lookup"><span data-stu-id="95a00-874">WHSControl.data</span></span>|
|<span data-ttu-id="95a00-875">WHSLocationDirective.targetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="95a00-875">WHSLocationDirective.targetLicensePlateId</span></span>|

## <a name="construct-methods-with-throw-statements"></a><span data-ttu-id="95a00-876">throw ステートメントを使用した construct メソッド</span><span class="sxs-lookup"><span data-stu-id="95a00-876">Construct methods with throw statements</span></span>

<span data-ttu-id="95a00-877">特定の型の実装が欠落していた場合、いくつかの **construct** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="95a00-877">Some **construct** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="95a00-878">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**construct** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="95a00-878">This doesn't work well with extensibility, so to mitigate this, **construct** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="95a00-879">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-879">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="95a00-880">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="95a00-880">Object</span></span> |
| -------------|
|<span data-ttu-id="95a00-881">BarcodeEAN128.string()</span><span class="sxs-lookup"><span data-stu-id="95a00-881">BarcodeEAN128.string()</span></span>|
|<span data-ttu-id="95a00-882">CustCreditLimit.Construct</span><span class="sxs-lookup"><span data-stu-id="95a00-882">CustCreditLimit.Construct</span></span>|
|<span data-ttu-id="95a00-883">FormLetterReport</span><span class="sxs-lookup"><span data-stu-id="95a00-883">FormLetterReport</span></span>|
|<span data-ttu-id="95a00-884">JournalStatic</span><span class="sxs-lookup"><span data-stu-id="95a00-884">JournalStatic</span></span>|
|<span data-ttu-id="95a00-885">MarkupAllocation</span><span class="sxs-lookup"><span data-stu-id="95a00-885">MarkupAllocation</span></span>|
|<span data-ttu-id="95a00-886">PurchTable2LineField</span><span class="sxs-lookup"><span data-stu-id="95a00-886">PurchTable2LineField</span></span>|
|<span data-ttu-id="95a00-887">SalesCalcTax</span><span class="sxs-lookup"><span data-stu-id="95a00-887">SalesCalcTax</span></span>|
|<span data-ttu-id="95a00-888">SalesEditLinesForm</span><span class="sxs-lookup"><span data-stu-id="95a00-888">SalesEditLinesForm</span></span>|
|<span data-ttu-id="95a00-889">SalesFormLetter</span><span class="sxs-lookup"><span data-stu-id="95a00-889">SalesFormLetter</span></span>|
|<span data-ttu-id="95a00-890">SalesFormLetterContract.newFromPackedVersion</span><span class="sxs-lookup"><span data-stu-id="95a00-890">SalesFormLetterContract.newFromPackedVersion</span></span>|
|<span data-ttu-id="95a00-891">SalesFormletterParmData.newData</span><span class="sxs-lookup"><span data-stu-id="95a00-891">SalesFormletterParmData.newData</span></span>|
|<span data-ttu-id="95a00-892">SalesQuantity</span><span class="sxs-lookup"><span data-stu-id="95a00-892">SalesQuantity</span></span>|
|<span data-ttu-id="95a00-893">SalesQuotationEditLinesForm.construct</span><span class="sxs-lookup"><span data-stu-id="95a00-893">SalesQuotationEditLinesForm.construct</span></span>|
|<span data-ttu-id="95a00-894">SalesSummaryFields</span><span class="sxs-lookup"><span data-stu-id="95a00-894">SalesSummaryFields</span></span>|
|<span data-ttu-id="95a00-895">SalesTable2LineField</span><span class="sxs-lookup"><span data-stu-id="95a00-895">SalesTable2LineField</span></span>|
|<span data-ttu-id="95a00-896">VendInvoiceTableToLineUpdate</span><span class="sxs-lookup"><span data-stu-id="95a00-896">VendInvoiceTableToLineUpdate</span></span>|

## <a name="find-methods-with-throw-statements"></a><span data-ttu-id="95a00-897">throw ステートメントを使用した find メソッド</span><span class="sxs-lookup"><span data-stu-id="95a00-897">Find methods with throw statements</span></span>

<span data-ttu-id="95a00-898">特定の型の実装が欠落していた場合、いくつかの **find** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="95a00-898">Some **find** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="95a00-899">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**find** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="95a00-899">This does not work well with extensibility, so to mitigate this, **find** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="95a00-900">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-900">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="95a00-901">メソッド</span><span class="sxs-lookup"><span data-stu-id="95a00-901">Methods</span></span> |
| -------------|
|<span data-ttu-id="95a00-902">JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="95a00-902">JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="95a00-903">JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="95a00-903">JournalStatic.findJournalTableId</span></span>|

## <a name="methods-made-hookable"></a><span data-ttu-id="95a00-904">フック可能なメソッド</span><span class="sxs-lookup"><span data-stu-id="95a00-904">Methods made hookable</span></span>

<span data-ttu-id="95a00-905">パブリックでない一部のメソッドおよびフック可能でない一部のメソッドについて、拡張性サポートが強化されました。</span><span class="sxs-lookup"><span data-stu-id="95a00-905">Extensibility support has been extended for some methods that were not public and were not hookable.</span></span> <span data-ttu-id="95a00-906">以下のメソッドはフック可能な動作で明示的に修飾されています。</span><span class="sxs-lookup"><span data-stu-id="95a00-906">The following methods have been explicitly decorated with hookable behavior.</span></span>

| <span data-ttu-id="95a00-907">メソッド</span><span class="sxs-lookup"><span data-stu-id="95a00-907">Method</span></span> |
| -------------|
|<span data-ttu-id="95a00-908">クラス CustVendReversePosting.updateCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="95a00-908">Class CustVendReversePosting.updateCustVendTrans</span></span>|
|<span data-ttu-id="95a00-909">クラス JournalTableData.construct</span><span class="sxs-lookup"><span data-stu-id="95a00-909">Class JournalTableData.construct</span></span>|
|<span data-ttu-id="95a00-910">クラス PriceDisc.makeKey</span><span class="sxs-lookup"><span data-stu-id="95a00-910">Class PriceDisc.makeKey</span></span>|
|<span data-ttu-id="95a00-911">クラス PurchInvoiceJournalCreate.initJournalHeader</span><span class="sxs-lookup"><span data-stu-id="95a00-911">Class PurchInvoiceJournalCreate.initJournalHeader</span></span>|
|<span data-ttu-id="95a00-912">クラス SalesInvoiceJournalPost.checkSourceLine</span><span class="sxs-lookup"><span data-stu-id="95a00-912">Class SalesInvoiceJournalPost.checkSourceLine</span></span>|
|<span data-ttu-id="95a00-913">クラス SalesInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="95a00-913">Class SalesInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="95a00-914">フォーム LedgerTransVoucher.addDynaLink</span><span class="sxs-lookup"><span data-stu-id="95a00-914">Form LedgerTransVoucher.addDynaLink</span></span>|
|<span data-ttu-id="95a00-915">ReqCalc.deleteItemRequirement</span><span class="sxs-lookup"><span data-stu-id="95a00-915">ReqCalc.deleteItemRequirement</span></span>|
|<span data-ttu-id="95a00-916">ReqCalc.initTransFromInventTrans</span><span class="sxs-lookup"><span data-stu-id="95a00-916">ReqCalc.initTransFromInventTrans</span></span>|
|<span data-ttu-id="95a00-917">ReqCalcForecastItemTable.deleteRequirement</span><span class="sxs-lookup"><span data-stu-id="95a00-917">ReqCalcForecastItemTable.deleteRequirement</span></span>|
|<span data-ttu-id="95a00-918">テーブル TmpCustVendTrans.createLineCreditLimit</span><span class="sxs-lookup"><span data-stu-id="95a00-918">Table TmpCustVendTrans.createLineCreditLimit</span></span>|
|<span data-ttu-id="95a00-919">テーブル TmpCustVendTrans.createLineCreditRemain</span><span class="sxs-lookup"><span data-stu-id="95a00-919">Table TmpCustVendTrans.createLineCreditRemain</span></span>|
|<span data-ttu-id="95a00-920">テーブル TmpCustVendTrans.createLineOrdered</span><span class="sxs-lookup"><span data-stu-id="95a00-920">Table TmpCustVendTrans.createLineOrdered</span></span>|
|<span data-ttu-id="95a00-921">テーブル TmpCustVendTrans.createLinePackingSlip</span><span class="sxs-lookup"><span data-stu-id="95a00-921">Table TmpCustVendTrans.createLinePackingSlip</span></span>|
|<span data-ttu-id="95a00-922">WHSLocationDirective.addRangeByTransType</span><span class="sxs-lookup"><span data-stu-id="95a00-922">WHSLocationDirective.addRangeByTransType</span></span>|
|<span data-ttu-id="95a00-923">WhsWorkCreate.createWorkLine</span><span class="sxs-lookup"><span data-stu-id="95a00-923">WhsWorkCreate.createWorkLine</span></span>|

## <a name="inline-delegates"></a><span data-ttu-id="95a00-924">インライン デリゲート</span><span class="sxs-lookup"><span data-stu-id="95a00-924">Inline delegates</span></span>

<span data-ttu-id="95a00-925">インライン デリゲートを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="95a00-925">Inline delegates are now available.</span></span> <span data-ttu-id="95a00-926">インライン デリゲートの最も一般的な使用方法は、メソッドをより粒度の細かいメソッドに分割して、より小規模なメソッドで拡張イベントを使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="95a00-926">The most common way to use inline delegates is to split the method into more granular methods and enable extensibility events in the smaller methods.</span></span>

|  <span data-ttu-id="95a00-927">メソッド</span><span class="sxs-lookup"><span data-stu-id="95a00-927">Method</span></span> |
| -------------|
|<span data-ttu-id="95a00-928">AxClass - ChequeDP - Method - insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="95a00-928">AxClass - ChequeDP - Method - insertChequeTmp</span></span>|
|<span data-ttu-id="95a00-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="95a00-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span></span>|
|<span data-ttu-id="95a00-930">クラス JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="95a00-930">class JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="95a00-931">クラス JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="95a00-931">class JournalStatic.findJournalTableId</span></span>|
|<span data-ttu-id="95a00-932">クラス WhsLocationDirective.findLocationMultiSKU</span><span class="sxs-lookup"><span data-stu-id="95a00-932">Class WhsLocationDirective.findLocationMultiSKU</span></span>|
|<span data-ttu-id="95a00-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span><span class="sxs-lookup"><span data-stu-id="95a00-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span></span>|
|<span data-ttu-id="95a00-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span><span class="sxs-lookup"><span data-stu-id="95a00-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span></span>|
|<span data-ttu-id="95a00-935">フォーム SalesTable - メソッド updateDesign</span><span class="sxs-lookup"><span data-stu-id="95a00-935">Form SalesTable - method updateDesign</span></span>|
|<span data-ttu-id="95a00-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span><span class="sxs-lookup"><span data-stu-id="95a00-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span></span>|
|<span data-ttu-id="95a00-937">SalesLineType.insert</span><span class="sxs-lookup"><span data-stu-id="95a00-937">SalesLineType.insert</span></span>|
|<span data-ttu-id="95a00-938">SalesLineType.update</span><span class="sxs-lookup"><span data-stu-id="95a00-938">SalesLineType.update</span></span>|
|<span data-ttu-id="95a00-939">SalesTable2LineUpdatePrompt.dialog</span><span class="sxs-lookup"><span data-stu-id="95a00-939">SalesTable2LineUpdatePrompt.dialog</span></span>|
|<span data-ttu-id="95a00-940">テーブル ExtCodeTable</span><span class="sxs-lookup"><span data-stu-id="95a00-940">table ExtCodeTable</span></span>|
|<span data-ttu-id="95a00-941">テーブル InventItemGroup.getGroupForAccountType</span><span class="sxs-lookup"><span data-stu-id="95a00-941">table InventItemGroup.getGroupForAccountType</span></span>|
|<span data-ttu-id="95a00-942">テーブル InventItemGroup.ledgerDimensionDescription</span><span class="sxs-lookup"><span data-stu-id="95a00-942">table InventItemGroup.ledgerDimensionDescription</span></span>|
|<span data-ttu-id="95a00-943">テーブル InventTestAssociationTable</span><span class="sxs-lookup"><span data-stu-id="95a00-943">table InventTestAssociationTable</span></span>|
|<span data-ttu-id="95a00-944">テーブル LedgerJournalName - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="95a00-944">Table LedgerJournalName - method validateWrite</span></span>|
|<span data-ttu-id="95a00-945">テーブル PaymTerm - メソッド due</span><span class="sxs-lookup"><span data-stu-id="95a00-945">Table PaymTerm - method due</span></span>|
|<span data-ttu-id="95a00-946">TaxCalculation.newForSourceType</span><span class="sxs-lookup"><span data-stu-id="95a00-946">TaxCalculation.newForSourceType</span></span>|
|<span data-ttu-id="95a00-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span><span class="sxs-lookup"><span data-stu-id="95a00-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span></span>|
|<span data-ttu-id="95a00-948">WHSLoadLine.getOrderCommonFromLoadLine</span><span class="sxs-lookup"><span data-stu-id="95a00-948">WHSLoadLine.getOrderCommonFromLoadLine</span></span>|
|<span data-ttu-id="95a00-949">WhsLocationDirective.findLocation</span><span class="sxs-lookup"><span data-stu-id="95a00-949">WhsLocationDirective.findLocation</span></span>|
|<span data-ttu-id="95a00-950">WHSRFControlData.populateData</span><span class="sxs-lookup"><span data-stu-id="95a00-950">WHSRFControlData.populateData</span></span>|
|<span data-ttu-id="95a00-951">WHSRFControLData.processControl</span><span class="sxs-lookup"><span data-stu-id="95a00-951">WHSRFControLData.processControl</span></span>|
|<span data-ttu-id="95a00-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="95a00-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span></span>|

## <a name="other-changes"></a><span data-ttu-id="95a00-953">その他の変更</span><span class="sxs-lookup"><span data-stu-id="95a00-953">Other changes</span></span>

<span data-ttu-id="95a00-954">次の表に、拡張機能に対して行われた追加の変更を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="95a00-954">The following table lists additional changes that have been made for extensibility.</span></span>


|                                                           <span data-ttu-id="95a00-955">変更</span><span class="sxs-lookup"><span data-stu-id="95a00-955">Change</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------------------|
|                                      <span data-ttu-id="95a00-956">既存の製品分析コードの間接参照の追加</span><span class="sxs-lookup"><span data-stu-id="95a00-956">Add indirection for existing product dimensions</span></span>                                       |
|                                  <span data-ttu-id="95a00-957">クラス FormLetterParmDataOutputContract は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="95a00-957">Class FormLetterParmDataOutputContract is not extensible</span></span>                                  |
|             <span data-ttu-id="95a00-958">1 つ以上の引数をサポートする SysExtensionFramework のインスタンス化戦略の作成</span><span class="sxs-lookup"><span data-stu-id="95a00-958">Create an instantiation strategy for the SysExtensionFramework that supports one or more arguments</span></span>             |
|                      <span data-ttu-id="95a00-959">カスタマイズ: TableField: 拡張モデル: テーブル フィールドの EDT タイプの変更</span><span class="sxs-lookup"><span data-stu-id="95a00-959">Customization: TableField: Extension Model: Change EDT type of on a table field</span></span>                       |
|                          <span data-ttu-id="95a00-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="95a00-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch statement</span></span>                           |
|                                     <span data-ttu-id="95a00-961">CustVendOpenTransBalances - new() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="95a00-961">CustVendOpenTransBalances - new() switch statement</span></span>                                     |
|                                  <span data-ttu-id="95a00-962">CustVendOutPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="95a00-962">CustVendOutPaym (Class) needs extensibility improvement</span></span>                                   |
|                        <span data-ttu-id="95a00-963">CustVendPaymReconciliationSetStatus (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="95a00-963">CustVendPaymReconciliationSetStatus (Class) needs extensibility improvement</span></span>                         |
|                                 <span data-ttu-id="95a00-964">CustVendSumForPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="95a00-964">CustVendSumForPaym (Class) needs extensibility improvement</span></span>                                 |
|                               <span data-ttu-id="95a00-965">SysGroup からの AddressCountyId と AddressStateId EDT の切り離し</span><span class="sxs-lookup"><span data-stu-id="95a00-965">Decouple AddressCountyId and AddressStateId EDTs from SysGroup</span></span>                               |
|                          <span data-ttu-id="95a00-966">ドキュメント管理イベントの処理には拡張性サポートの改善が必要</span><span class="sxs-lookup"><span data-stu-id="95a00-966">Document Management event handling needs improved extensibility support</span></span>                           |
|            <span data-ttu-id="95a00-967">為替レート プロバイダー フレームワークには、通貨モデルにカスタムの組み込みプロバイダーを配置することが必要</span><span class="sxs-lookup"><span data-stu-id="95a00-967">Exchange rate provider framework requires custom built providers to be placed in the Currency Model</span></span>             |
|                                                      <span data-ttu-id="95a00-968">GS-128 の拡張</span><span class="sxs-lookup"><span data-stu-id="95a00-968">Extending GS-128</span></span>                                                      |
|                         <span data-ttu-id="95a00-969">拡張モデル: CountryRegionCodes プロパティでのカスタマイズを許可する。</span><span class="sxs-lookup"><span data-stu-id="95a00-969">Extension model: Allow customizations on the CountryRegionCodes property.</span></span>                          |
|                  <span data-ttu-id="95a00-970">フォーム拡張機能 - 新しいコントロールによって "拡張された" フォーム要素の拡張機能は動作しません</span><span class="sxs-lookup"><span data-stu-id="95a00-970">Form extension - Extension of "extended" form elements with new controls are not working</span></span>                  |
|                                              <span data-ttu-id="95a00-971">InventDim: throw 付きの条件</span><span class="sxs-lookup"><span data-stu-id="95a00-971">InventDim: Condition with throw</span></span>                                               |
|                                                  <span data-ttu-id="95a00-972">InventDimRenameDimValue</span><span class="sxs-lookup"><span data-stu-id="95a00-972">InventDimRenameDimValue</span></span>                                                   |
|                <span data-ttu-id="95a00-973">メソッドのオーバーレイ - クラス VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="95a00-973">Method overlayering - Class VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span></span>                |
|                                     <span data-ttu-id="95a00-974">メソッドのオーバーレイ: クラス Markup - メソッド delete</span><span class="sxs-lookup"><span data-stu-id="95a00-974">Method overlayering: class Markup - method delete</span></span>                                      |
|                       <span data-ttu-id="95a00-975">メソッドのオーバーレイ: クラス McrPriceHistoryForm.insertPotentialTradeAgreements</span><span class="sxs-lookup"><span data-stu-id="95a00-975">Method overlayering: class McrPriceHistoryForm.insertPotentialTradeAgreements</span></span>                        |
|                             <span data-ttu-id="95a00-976">メソッドのオーバーレイ: クラス OffsetVoucher - メソッド markTransaction</span><span class="sxs-lookup"><span data-stu-id="95a00-976">Method overlayering: Class OffsetVoucher - method markTransaction</span></span>                              |
|                                 <span data-ttu-id="95a00-977">メソッドのオーバーレイ: フォーム LedgerJournalTransDimension.init</span><span class="sxs-lookup"><span data-stu-id="95a00-977">Method overlayering: Form LedgerJournalTransDimension.init</span></span>                                 |
|                                 <span data-ttu-id="95a00-978">メソッドのオーバーレイ: フォーム LedgerTransVoucher - メソッド init</span><span class="sxs-lookup"><span data-stu-id="95a00-978">Method overlayering: Form LedgerTransVoucher - method init</span></span>                                 |
|                             <span data-ttu-id="95a00-979">メソッドのオーバーレイ: テーブル CustInvoiceTable - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="95a00-979">Method overlayering: Table CustInvoiceTable - method validateWrite</span></span>                             |
|                       <span data-ttu-id="95a00-980">メソッド シグネチャが変更されました: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span><span class="sxs-lookup"><span data-stu-id="95a00-980">Method signature changed: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span></span>                        |
|                               <span data-ttu-id="95a00-981">メソッド シグネチャが変更になりました: WHSInvent.getCommonFromWorkTransType</span><span class="sxs-lookup"><span data-stu-id="95a00-981">Method signature changed: WHSInvent.getCommonFromWorkTransType</span></span>                               |
|                                  <span data-ttu-id="95a00-982">メソッド シグネチャが変更されました: WHSPoolProdBom.movementBuffer</span><span class="sxs-lookup"><span data-stu-id="95a00-982">Method signature changed: WHSPoolProdBom.movementBuffer</span></span>                                   |
|                          <span data-ttu-id="95a00-983">construct メソッドがありません: クラス SMAServiceOrderTableButtonStateProvider</span><span class="sxs-lookup"><span data-stu-id="95a00-983">Missing construct method: class SMAServiceOrderTableButtonStateProvider</span></span>                           |
|                                         <span data-ttu-id="95a00-984">必要な番号順序スコープの拡張性</span><span class="sxs-lookup"><span data-stu-id="95a00-984">Number sequence scope extensibility needed</span></span>                                         |
|                           <span data-ttu-id="95a00-985">Runbase には、クラスの拡張機能がメンバーをパック/アンパックする方法が必要</span><span class="sxs-lookup"><span data-stu-id="95a00-985">Runbase needs a way for class extensions to pack/unpack their members</span></span>                            |
|                                              <span data-ttu-id="95a00-986">文字列 EDT のサイズの拡張の問題</span><span class="sxs-lookup"><span data-stu-id="95a00-986">String EDT size extension issues</span></span>                                              |
|                              <span data-ttu-id="95a00-987">カスタムの InventDim に基づく手持在庫フォームのオープンのサポート</span><span class="sxs-lookup"><span data-stu-id="95a00-987">Support opening Inventory on-hand form based on custom InventDim</span></span>                              |
|          <span data-ttu-id="95a00-988">SysExtension フレームワーク: SysExtensionIInstantiationStrategy と SysExtensionIAttribute は互換性がありません</span><span class="sxs-lookup"><span data-stu-id="95a00-988">SysExtension framework: SysExtensionIInstantiationStrategy and SysExtensionIAttribute are not compatible</span></span>          |
| <span data-ttu-id="95a00-989">要求/応答シナリオで使用されるデリゲートがより堅牢になるために、EventHandlerResult のバリエーションが必要</span><span class="sxs-lookup"><span data-stu-id="95a00-989">Variations of EventHandlerResult are requested to ensure that delegates used in Request/response scenarios are more robust</span></span> |
|                                                <span data-ttu-id="95a00-990">WHS モバイル フレームワーク: 合格</span><span class="sxs-lookup"><span data-stu-id="95a00-990">WHS Mobile Framework: passes</span></span>                                                |
|                                     <span data-ttu-id="95a00-991">WhsLocationDirectiveLine To/FromQty は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="95a00-991">WhsLocationDirectiveLine To/FromQty not extensible</span></span>                                     |
|                                                 <span data-ttu-id="95a00-992">WHSMobileApp の拡張性</span><span class="sxs-lookup"><span data-stu-id="95a00-992">WHSMobileApp Extensibility</span></span>                                                 |
|         <span data-ttu-id="95a00-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="95a00-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|         <span data-ttu-id="95a00-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="95a00-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|            <span data-ttu-id="95a00-995">WhsRFControlData.processControl は switch ブロック内の _data ではなく WhsControl.data を参照する必要があります</span><span class="sxs-lookup"><span data-stu-id="95a00-995">WhsRFControlData.processControl must reference WhsControl.data instead of _data in the switch block</span></span>             |

