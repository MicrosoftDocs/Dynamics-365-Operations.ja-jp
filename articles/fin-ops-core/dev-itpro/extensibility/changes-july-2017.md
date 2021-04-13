---
title: Finance and Operations、Enterprise edition (2017 年 7 月) の拡張機能の変更
description: これは、(2017 年 7 月) に実装された拡張機能の一覧です。
author: FrankDahl
ms.date: 11/08/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 03105f0ea2c1f23e9579aca293e24a432d508ac0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748787"
---
# <a name="extensibility-changes-in-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="51025-103">Finance and Operations、Enterprise edition (2017 年 7 月) の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="51025-103">Extensibility changes in Finance and Operations, Enterprise edition (July 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51025-104">これは、Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="51025-104">This is a list of extensibility features that were implemented in the Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span> <span data-ttu-id="51025-105">このバージョンは 2017 年 7 月にリリースされ、ビルド番号は 7.2.11792.56024 です。</span><span class="sxs-lookup"><span data-stu-id="51025-105">This version was released in July 2017 and has a build number of 7.2.11792.56024.</span></span> <span data-ttu-id="51025-106">拡張性をサポートする変更スケジュールの詳細については、 [アプリケーション機能拡張ロードマップ](extensibility-roadmap.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="51025-106">For more information about the schedule of changes that support extensibility, see [Application extensibility roadmap](extensibility-roadmap.md).</span></span>

## <a name="soft-sealed-application-models"></a><span data-ttu-id="51025-107">ソフト シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="51025-107">Soft-sealed application models</span></span>

<span data-ttu-id="51025-108">以下のアプリケーション中間層モデルは、今回のリリースでソフト シールされました。</span><span class="sxs-lookup"><span data-stu-id="51025-108">The following application middle-tier models were soft-sealed in this release.</span></span> <span data-ttu-id="51025-109">これらのモデルのオーバーレイ コードは、コンパイル時に警告を生成します。</span><span class="sxs-lookup"><span data-stu-id="51025-109">Overlayered code in these models will generate warnings on compilation.</span></span>

| <span data-ttu-id="51025-110">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="51025-110">Category</span></span>       | <span data-ttu-id="51025-111">モデル</span><span class="sxs-lookup"><span data-stu-id="51025-111">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="51025-112">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="51025-112">Application Frameworks</span></span> | <span data-ttu-id="51025-113">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="51025-113">CaseManagement</span></span> |
| <span data-ttu-id="51025-114">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="51025-114">Application Frameworks</span></span> | <span data-ttu-id="51025-115">Dimensions</span><span class="sxs-lookup"><span data-stu-id="51025-115">Dimensions</span></span> |
| <span data-ttu-id="51025-116">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="51025-116">Application Frameworks</span></span> | <span data-ttu-id="51025-117">Directory</span><span class="sxs-lookup"><span data-stu-id="51025-117">Directory</span></span> |
| <span data-ttu-id="51025-118">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="51025-118">Application Frameworks</span></span> | <span data-ttu-id="51025-119">Organization</span><span class="sxs-lookup"><span data-stu-id="51025-119">Organization</span></span> |
| <span data-ttu-id="51025-120">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="51025-120">Application Frameworks</span></span> | <span data-ttu-id="51025-121">Currency</span><span class="sxs-lookup"><span data-stu-id="51025-121">Currency</span></span>|
| <span data-ttu-id="51025-122">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="51025-122">Application Frameworks</span></span> | <span data-ttu-id="51025-123">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="51025-123">ApplicationCommon</span></span>|
| <span data-ttu-id="51025-124">HCM コア モデル</span><span class="sxs-lookup"><span data-stu-id="51025-124">HCM Core Models</span></span>| <span data-ttu-id="51025-125">3817938</span><span class="sxs-lookup"><span data-stu-id="51025-125">3817938</span></span>
|<span data-ttu-id="51025-126">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-126">Tax Models</span></span> |<span data-ttu-id="51025-127">Tax</span><span class="sxs-lookup"><span data-stu-id="51025-127">Tax</span></span> |
|<span data-ttu-id="51025-128">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-128">Tax Models</span></span> |<span data-ttu-id="51025-129">Tax Books</span><span class="sxs-lookup"><span data-stu-id="51025-129">Tax Books</span></span> |
|<span data-ttu-id="51025-130">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-130">Tax Models</span></span> |<span data-ttu-id="51025-131">Tax Books Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="51025-131">Tax Books Application Suite Integration</span></span> |
|<span data-ttu-id="51025-132">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-132">Tax Models</span></span> |<span data-ttu-id="51025-133">Tax Engine Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="51025-133">Tax Engine Application Suite Integration</span></span> |
|<span data-ttu-id="51025-134">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-134">Tax Models</span></span> |<span data-ttu-id="51025-135">Tax Engine Configuration</span><span class="sxs-lookup"><span data-stu-id="51025-135">Tax Engine Configuration</span></span> |
|<span data-ttu-id="51025-136">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-136">Tax Models</span></span> |<span data-ttu-id="51025-137">Tax Engine Interface</span><span class="sxs-lookup"><span data-stu-id="51025-137">Tax Engine Interface</span></span> |
|<span data-ttu-id="51025-138">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-138">Tax Models</span></span> |<span data-ttu-id="51025-139">Tax Engine Runtime Generation</span><span class="sxs-lookup"><span data-stu-id="51025-139">Tax Engine Runtime Generation</span></span> |
|<span data-ttu-id="51025-140">税モデル</span><span class="sxs-lookup"><span data-stu-id="51025-140">Tax Models</span></span> |<span data-ttu-id="51025-141">TaxEngine</span><span class="sxs-lookup"><span data-stu-id="51025-141">TaxEngine</span></span> |
| <span data-ttu-id="51025-142">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="51025-142">Source Document Models</span></span> |<span data-ttu-id="51025-143">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="51025-143">SourceDocumentation</span></span> |
| <span data-ttu-id="51025-144">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="51025-144">Source Document Models</span></span> |<span data-ttu-id="51025-145">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="51025-145">SourceDocumentationTypes</span></span> |
| <span data-ttu-id="51025-146">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="51025-146">Ledger Models</span></span> |<span data-ttu-id="51025-147">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="51025-147">GeneralLedger</span></span> |
| <span data-ttu-id="51025-148">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="51025-148">Ledger Models</span></span> |<span data-ttu-id="51025-149">Ledger</span><span class="sxs-lookup"><span data-stu-id="51025-149">Ledger</span></span> |
| <span data-ttu-id="51025-150">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="51025-150">Ledger Models</span></span> |<span data-ttu-id="51025-151">Subledger</span><span class="sxs-lookup"><span data-stu-id="51025-151">Subledger</span></span> |
| <span data-ttu-id="51025-152">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="51025-152">Middle Tier SCM Models</span></span> | <span data-ttu-id="51025-153">CostAccounting</span><span class="sxs-lookup"><span data-stu-id="51025-153">CostAccounting</span></span> |
| <span data-ttu-id="51025-154">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="51025-154">Middle Tier SCM Models</span></span> | <span data-ttu-id="51025-155">CostAccountingAX</span><span class="sxs-lookup"><span data-stu-id="51025-155">CostAccountingAX</span></span> |
| <span data-ttu-id="51025-156">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="51025-156">Middle Tier SCM Models</span></span> | <span data-ttu-id="51025-157">SCMControls</span><span class="sxs-lookup"><span data-stu-id="51025-157">SCMControls</span></span> |
| <span data-ttu-id="51025-158">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="51025-158">Middle Tier SCM Models</span></span> | <span data-ttu-id="51025-159">SCMMobile</span><span class="sxs-lookup"><span data-stu-id="51025-159">SCMMobile</span></span> |
| <span data-ttu-id="51025-160">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="51025-160">Middle Tier SCM Models</span></span> | <span data-ttu-id="51025-161">UnitOfMeasure</span><span class="sxs-lookup"><span data-stu-id="51025-161">UnitOfMeasure</span></span> |
| <span data-ttu-id="51025-162">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="51025-162">Middle Tier SCM Models</span></span> | <span data-ttu-id="51025-163">WMSAdvancedMigration</span><span class="sxs-lookup"><span data-stu-id="51025-163">WMSAdvancedMigration</span></span>|
| <span data-ttu-id="51025-164">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="51025-164">Middle Tier SCM Models</span></span> | <span data-ttu-id="51025-165">InventoryDimensionConversion</span><span class="sxs-lookup"><span data-stu-id="51025-165">InventoryDimensionConversion</span></span>|
| <span data-ttu-id="51025-166">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="51025-166">Workspaces</span></span>| <span data-ttu-id="51025-167">ApplicationWorkspaces</span><span class="sxs-lookup"><span data-stu-id="51025-167">ApplicationWorkspaces</span></span> |
| <span data-ttu-id="51025-168">財務</span><span class="sxs-lookup"><span data-stu-id="51025-168">Finance</span></span>| <span data-ttu-id="51025-169">Fiscalbooks</span><span class="sxs-lookup"><span data-stu-id="51025-169">Fiscalbooks</span></span> |
| <span data-ttu-id="51025-170">管理ツール</span><span class="sxs-lookup"><span data-stu-id="51025-170">Management tools</span></span> | <span data-ttu-id="51025-171">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="51025-171">DataUpgrade</span></span> |

## <a name="hard-sealed-application-models"></a><span data-ttu-id="51025-172">ハード シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="51025-172">Hard-sealed application models</span></span>

<span data-ttu-id="51025-173">以下のアプリケーション中間層モデルは、今回のリリースでハード シールされました。</span><span class="sxs-lookup"><span data-stu-id="51025-173">The following application middle-tier models were hard-sealed in this release.</span></span> <span data-ttu-id="51025-174">これらのモデルのオーバーレイ コードは、コンパイル時にエラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="51025-174">Overlayered code in these models will generate errors on compilation.</span></span>

| <span data-ttu-id="51025-175">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="51025-175">Category</span></span>       | <span data-ttu-id="51025-176">モデル</span><span class="sxs-lookup"><span data-stu-id="51025-176">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="51025-177">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="51025-177">Accounts Payable</span></span> | <span data-ttu-id="51025-178">AccountsPayableMobile</span><span class="sxs-lookup"><span data-stu-id="51025-178">AccountsPayableMobile</span></span> |
| <span data-ttu-id="51025-179">財務</span><span class="sxs-lookup"><span data-stu-id="51025-179">Finance</span></span> | <span data-ttu-id="51025-180">FinancialReportingEntityStore</span><span class="sxs-lookup"><span data-stu-id="51025-180">FinancialReportingEntityStore</span></span>|
| <span data-ttu-id="51025-181">ツール</span><span class="sxs-lookup"><span data-stu-id="51025-181">Tools</span></span> | <span data-ttu-id="51025-182">PerformanceTool</span><span class="sxs-lookup"><span data-stu-id="51025-182">PerformanceTool</span></span> |
| <span data-ttu-id="51025-183">経費</span><span class="sxs-lookup"><span data-stu-id="51025-183">Expenses</span></span> | <span data-ttu-id="51025-184">ExpenseMobile</span><span class="sxs-lookup"><span data-stu-id="51025-184">ExpenseMobile</span></span> |
| <span data-ttu-id="51025-185">GER</span><span class="sxs-lookup"><span data-stu-id="51025-185">GER</span></span> | <span data-ttu-id="51025-186">ElectronicReporting</span><span class="sxs-lookup"><span data-stu-id="51025-186">ElectronicReporting</span></span>|
|<span data-ttu-id="51025-187">GER</span><span class="sxs-lookup"><span data-stu-id="51025-187">GER</span></span> | <span data-ttu-id="51025-188">ElectronicReportingCore</span><span class="sxs-lookup"><span data-stu-id="51025-188">ElectronicReportingCore</span></span>|
|<span data-ttu-id="51025-189">GER</span><span class="sxs-lookup"><span data-stu-id="51025-189">GER</span></span> | <span data-ttu-id="51025-190">Electronic Reporting Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="51025-190">Electronic Reporting Application Suite Integration</span></span>|

## <a name="enumerations-that-are-now-extensible"></a><span data-ttu-id="51025-191">拡張可能になった列挙型</span><span class="sxs-lookup"><span data-stu-id="51025-191">Enumerations that are now extensible</span></span>

<span data-ttu-id="51025-192">列挙の拡張をサポートするために以下の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="51025-192">The following changes were made to support extending enumerations:</span></span>
- <span data-ttu-id="51025-193">標準アプリケーションの多くの列挙が拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="51025-193">Many enumerations in the standard application have been made extensible.</span></span> <span data-ttu-id="51025-194">列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="51025-194">An enumeration is made extensible by setting two properties on the enumeration.</span></span> <span data-ttu-id="51025-195">**IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="51025-195">The **IsExtensible** property is set to **Yes**, and the **UseEnumValue** property is set to **No**.</span></span> 
- <span data-ttu-id="51025-196">一部の列挙型は状態を表します。</span><span class="sxs-lookup"><span data-stu-id="51025-196">Some enumerations represent state.</span></span> <span data-ttu-id="51025-197">拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="51025-197">New façade methods have been added to help enable adding enumeration values by extension.</span></span> <span data-ttu-id="51025-198">列挙型を拡張する方法については、 [拡張機能を使用した列挙値の追加](add-enum-value.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="51025-198">For information about how to extend an enumeration, see [Add values to enums through extension](add-enum-value.md).</span></span>
- <span data-ttu-id="51025-199">拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。</span><span class="sxs-lookup"><span data-stu-id="51025-199">Some application code that uses enumerations was changed to support extensibility.</span></span> <span data-ttu-id="51025-200">一般的な変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="51025-200">Common changes include:</span></span>
    + <span data-ttu-id="51025-201">ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。</span><span class="sxs-lookup"><span data-stu-id="51025-201">Removing **throw** exception statements in the default case of a switch to allow post-event subscription.</span></span>
    + <span data-ttu-id="51025-202">拡張機能の **SysExtension** サポートの追加。</span><span class="sxs-lookup"><span data-stu-id="51025-202">Adding **SysExtension** support for extension.</span></span>
    + <span data-ttu-id="51025-203">明示的なデリゲートの追加。</span><span class="sxs-lookup"><span data-stu-id="51025-203">Adding explicit delegates.</span></span>


| <span data-ttu-id="51025-204">列挙型</span><span class="sxs-lookup"><span data-stu-id="51025-204">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="51025-205">AgreementState</span><span class="sxs-lookup"><span data-stu-id="51025-205">AgreementState</span></span>|
|<span data-ttu-id="51025-206">AssetAccountType</span><span class="sxs-lookup"><span data-stu-id="51025-206">AssetAccountType</span></span>|
|<span data-ttu-id="51025-207">AssetTransTypeJournal</span><span class="sxs-lookup"><span data-stu-id="51025-207">AssetTransTypeJournal</span></span>|
|<span data-ttu-id="51025-208">BankAccountType</span><span class="sxs-lookup"><span data-stu-id="51025-208">BankAccountType</span></span>|
|<span data-ttu-id="51025-209">BankFormat</span><span class="sxs-lookup"><span data-stu-id="51025-209">BankFormat</span></span>|
|<span data-ttu-id="51025-210">BarcodeContentType</span><span class="sxs-lookup"><span data-stu-id="51025-210">BarcodeContentType</span></span>|
|<span data-ttu-id="51025-211">BarcodeCoverPageEntityType</span><span class="sxs-lookup"><span data-stu-id="51025-211">BarcodeCoverPageEntityType</span></span>|
|<span data-ttu-id="51025-212">BarcodeType</span><span class="sxs-lookup"><span data-stu-id="51025-212">BarcodeType</span></span>|
|<span data-ttu-id="51025-213">BOMCalcCostingVersionUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-213">BOMCalcCostingVersionUpdate</span></span>|
|<span data-ttu-id="51025-214">BOMCalcCostPriceUsed</span><span class="sxs-lookup"><span data-stu-id="51025-214">BOMCalcCostPriceUsed</span></span>|
|<span data-ttu-id="51025-215">BOMCalcSalesPriceUsed</span><span class="sxs-lookup"><span data-stu-id="51025-215">BOMCalcSalesPriceUsed</span></span>|
|<span data-ttu-id="51025-216">BOMCalcType</span><span class="sxs-lookup"><span data-stu-id="51025-216">BOMCalcType</span></span>|
|<span data-ttu-id="51025-217">BOMCheckLevel</span><span class="sxs-lookup"><span data-stu-id="51025-217">BOMCheckLevel</span></span>|
|<span data-ttu-id="51025-218">BOMCopyContext</span><span class="sxs-lookup"><span data-stu-id="51025-218">BOMCopyContext</span></span>|
|<span data-ttu-id="51025-219">BOMCopyMethod</span><span class="sxs-lookup"><span data-stu-id="51025-219">BOMCopyMethod</span></span>|
|<span data-ttu-id="51025-220">BOMCopyType</span><span class="sxs-lookup"><span data-stu-id="51025-220">BOMCopyType</span></span>|
|<span data-ttu-id="51025-221">BOMCostCalculationMethod</span><span class="sxs-lookup"><span data-stu-id="51025-221">BOMCostCalculationMethod</span></span>|
|<span data-ttu-id="51025-222">BOMExplode</span><span class="sxs-lookup"><span data-stu-id="51025-222">BOMExplode</span></span>|
|<span data-ttu-id="51025-223">BOMRouteCopyDataType</span><span class="sxs-lookup"><span data-stu-id="51025-223">BOMRouteCopyDataType</span></span>|
|<span data-ttu-id="51025-224">BOMVersionFilter</span><span class="sxs-lookup"><span data-stu-id="51025-224">BOMVersionFilter</span></span>|
|<span data-ttu-id="51025-225">BudgetReservation_BusinessEvent_PSN</span><span class="sxs-lookup"><span data-stu-id="51025-225">BudgetReservation_BusinessEvent_PSN</span></span>|
|<span data-ttu-id="51025-226">BudgetReservation_SourceDocument_PSN</span><span class="sxs-lookup"><span data-stu-id="51025-226">BudgetReservation_SourceDocument_PSN</span></span>|
|<span data-ttu-id="51025-227">BudgetReservation_SourceDocumentLine_PSN</span><span class="sxs-lookup"><span data-stu-id="51025-227">BudgetReservation_SourceDocumentLine_PSN</span></span>|
|<span data-ttu-id="51025-228">CatCallMethod</span><span class="sxs-lookup"><span data-stu-id="51025-228">CatCallMethod</span></span>|
|<span data-ttu-id="51025-229">CatContentType</span><span class="sxs-lookup"><span data-stu-id="51025-229">CatContentType</span></span>|
|<span data-ttu-id="51025-230">CatImportStatus</span><span class="sxs-lookup"><span data-stu-id="51025-230">CatImportStatus</span></span>|
|<span data-ttu-id="51025-231">CatMaintenanceRequestWfStatus</span><span class="sxs-lookup"><span data-stu-id="51025-231">CatMaintenanceRequestWfStatus</span></span>|
|<span data-ttu-id="51025-232">CatProcurementErrorCode</span><span class="sxs-lookup"><span data-stu-id="51025-232">CatProcurementErrorCode</span></span>|
|<span data-ttu-id="51025-233">CatPurchaseStatus</span><span class="sxs-lookup"><span data-stu-id="51025-233">CatPurchaseStatus</span></span>|
|<span data-ttu-id="51025-234">CatUserReviewApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="51025-234">CatUserReviewApprovalStatus</span></span>|
|<span data-ttu-id="51025-235">CatVendorCatalogFileUploadType</span><span class="sxs-lookup"><span data-stu-id="51025-235">CatVendorCatalogFileUploadType</span></span>|
|<span data-ttu-id="51025-236">CatVendorCatalogTemplateCategory</span><span class="sxs-lookup"><span data-stu-id="51025-236">CatVendorCatalogTemplateCategory</span></span>|
|<span data-ttu-id="51025-237">CatVendorCategoryHierarchyType</span><span class="sxs-lookup"><span data-stu-id="51025-237">CatVendorCategoryHierarchyType</span></span>|
|<span data-ttu-id="51025-238">CatVendorConfigurationForImport</span><span class="sxs-lookup"><span data-stu-id="51025-238">CatVendorConfigurationForImport</span></span>|
|<span data-ttu-id="51025-239">CatVendorLegalEntityStatus</span><span class="sxs-lookup"><span data-stu-id="51025-239">CatVendorLegalEntityStatus</span></span>|
|<span data-ttu-id="51025-240">CatVendorSiteType</span><span class="sxs-lookup"><span data-stu-id="51025-240">CatVendorSiteType</span></span>|
|<span data-ttu-id="51025-241">ConsignmentReplenishmentOrderLineStatus</span><span class="sxs-lookup"><span data-stu-id="51025-241">ConsignmentReplenishmentOrderLineStatus</span></span>|
|<span data-ttu-id="51025-242">ConsignmentReplenishmentOrderStatus</span><span class="sxs-lookup"><span data-stu-id="51025-242">ConsignmentReplenishmentOrderStatus</span></span>|
|<span data-ttu-id="51025-243">CostBreakdown</span><span class="sxs-lookup"><span data-stu-id="51025-243">CostBreakdown</span></span>|
|<span data-ttu-id="51025-244">CostCalculationCompareProductType</span><span class="sxs-lookup"><span data-stu-id="51025-244">CostCalculationCompareProductType</span></span>|
|<span data-ttu-id="51025-245">CostCalculationRole</span><span class="sxs-lookup"><span data-stu-id="51025-245">CostCalculationRole</span></span>|
|<span data-ttu-id="51025-246">CostCalculationState</span><span class="sxs-lookup"><span data-stu-id="51025-246">CostCalculationState</span></span>|
|<span data-ttu-id="51025-247">CostCalculationSurchargeSubtype</span><span class="sxs-lookup"><span data-stu-id="51025-247">CostCalculationSurchargeSubtype</span></span>|
|<span data-ttu-id="51025-248">CostingActivationType</span><span class="sxs-lookup"><span data-stu-id="51025-248">CostingActivationType</span></span>|
|<span data-ttu-id="51025-249">CostingVersionCompareTo</span><span class="sxs-lookup"><span data-stu-id="51025-249">CostingVersionCompareTo</span></span>|
|<span data-ttu-id="51025-250">CostingVersionPriceType</span><span class="sxs-lookup"><span data-stu-id="51025-250">CostingVersionPriceType</span></span>|
|<span data-ttu-id="51025-251">CostPriceBase</span><span class="sxs-lookup"><span data-stu-id="51025-251">CostPriceBase</span></span>|
|<span data-ttu-id="51025-252">CostProfitSet</span><span class="sxs-lookup"><span data-stu-id="51025-252">CostProfitSet</span></span>|
|<span data-ttu-id="51025-253">CostSalesPriceDisplay</span><span class="sxs-lookup"><span data-stu-id="51025-253">CostSalesPriceDisplay</span></span>|
|<span data-ttu-id="51025-254">CostSheetNodeListType</span><span class="sxs-lookup"><span data-stu-id="51025-254">CostSheetNodeListType</span></span>|
|<span data-ttu-id="51025-255">CostSheetPanelView</span><span class="sxs-lookup"><span data-stu-id="51025-255">CostSheetPanelView</span></span>|
|<span data-ttu-id="51025-256">CostSheetProdFlowMode</span><span class="sxs-lookup"><span data-stu-id="51025-256">CostSheetProdFlowMode</span></span>|
|<span data-ttu-id="51025-257">CostStatementCacheAggregationAfter</span><span class="sxs-lookup"><span data-stu-id="51025-257">CostStatementCacheAggregationAfter</span></span>|
|<span data-ttu-id="51025-258">CostWIPStatementCategory</span><span class="sxs-lookup"><span data-stu-id="51025-258">CostWIPStatementCategory</span></span>|
|<span data-ttu-id="51025-259">CustPaymentValidate</span><span class="sxs-lookup"><span data-stu-id="51025-259">CustPaymentValidate</span></span>|
|<span data-ttu-id="51025-260">CustSpecTransOverviewFormMode</span><span class="sxs-lookup"><span data-stu-id="51025-260">CustSpecTransOverviewFormMode</span></span>|
|<span data-ttu-id="51025-261">CustTransRefType</span><span class="sxs-lookup"><span data-stu-id="51025-261">CustTransRefType</span></span>|
|<span data-ttu-id="51025-262">CustVendPaymentStatus</span><span class="sxs-lookup"><span data-stu-id="51025-262">CustVendPaymentStatus</span></span>|
|<span data-ttu-id="51025-263">CustVendTransportPointTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="51025-263">CustVendTransportPointTypeTransfer</span></span>|
|<span data-ttu-id="51025-264">DlvScheduleMarkupConversionMode</span><span class="sxs-lookup"><span data-stu-id="51025-264">DlvScheduleMarkupConversionMode</span></span>|
|<span data-ttu-id="51025-265">EcoResAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="51025-265">EcoResAttributeModifier</span></span>|
|<span data-ttu-id="51025-266">EcoResCategoryAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="51025-266">EcoResCategoryAttributeModifier</span></span>|
|<span data-ttu-id="51025-267">EcoResCategoryChangeStatus</span><span class="sxs-lookup"><span data-stu-id="51025-267">EcoResCategoryChangeStatus</span></span>|
|<span data-ttu-id="51025-268">EcoResCategoryHierarchyModifier</span><span class="sxs-lookup"><span data-stu-id="51025-268">EcoResCategoryHierarchyModifier</span></span>|
|<span data-ttu-id="51025-269">EcoResCategoryNamedHierarchyRole</span><span class="sxs-lookup"><span data-stu-id="51025-269">EcoResCategoryNamedHierarchyRole</span></span>|
|<span data-ttu-id="51025-270">EcoResProductImageUsage</span><span class="sxs-lookup"><span data-stu-id="51025-270">EcoResProductImageUsage</span></span>|
|<span data-ttu-id="51025-271">EcoResProductListPage</span><span class="sxs-lookup"><span data-stu-id="51025-271">EcoResProductListPage</span></span>|
|<span data-ttu-id="51025-272">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="51025-272">EcoResProductPerCompanyListPageType</span></span>|
|<span data-ttu-id="51025-273">EcoResProductTemplateType</span><span class="sxs-lookup"><span data-stu-id="51025-273">EcoResProductTemplateType</span></span>|
|<span data-ttu-id="51025-274">EcoResReleaseProductToCompany</span><span class="sxs-lookup"><span data-stu-id="51025-274">EcoResReleaseProductToCompany</span></span>|
|<span data-ttu-id="51025-275">EcoResVariantConfigurationTechnologyType</span><span class="sxs-lookup"><span data-stu-id="51025-275">EcoResVariantConfigurationTechnologyType</span></span>|
|<span data-ttu-id="51025-276">ECPsalesOrdersViewType</span><span class="sxs-lookup"><span data-stu-id="51025-276">ECPsalesOrdersViewType</span></span>|
|<span data-ttu-id="51025-277">EPCSSProductViewType</span><span class="sxs-lookup"><span data-stu-id="51025-277">EPCSSProductViewType</span></span>|
|<span data-ttu-id="51025-278">EUSalesTransMethod</span><span class="sxs-lookup"><span data-stu-id="51025-278">EUSalesTransMethod</span></span>|
|<span data-ttu-id="51025-279">FormLetterType</span><span class="sxs-lookup"><span data-stu-id="51025-279">FormLetterType</span></span>|
|<span data-ttu-id="51025-280">GanttCallerWrkCtr</span><span class="sxs-lookup"><span data-stu-id="51025-280">GanttCallerWrkCtr</span></span>|
|<span data-ttu-id="51025-281">GanttSetupType</span><span class="sxs-lookup"><span data-stu-id="51025-281">GanttSetupType</span></span>|
|<span data-ttu-id="51025-282">GanttTimeUnit</span><span class="sxs-lookup"><span data-stu-id="51025-282">GanttTimeUnit</span></span>|
|<span data-ttu-id="51025-283">GanttWrkCtrDisplayColumnsType</span><span class="sxs-lookup"><span data-stu-id="51025-283">GanttWrkCtrDisplayColumnsType</span></span>|
|<span data-ttu-id="51025-284">IntercompanyGoodsInTransitLineType</span><span class="sxs-lookup"><span data-stu-id="51025-284">IntercompanyGoodsInTransitLineType</span></span>|
|<span data-ttu-id="51025-285">InterCompanyGoodsInTransitOrigin</span><span class="sxs-lookup"><span data-stu-id="51025-285">InterCompanyGoodsInTransitOrigin</span></span>|
|<span data-ttu-id="51025-286">InventAccountType</span><span class="sxs-lookup"><span data-stu-id="51025-286">InventAccountType</span></span>|
|<span data-ttu-id="51025-287">InventAccountTypeStdCostVariance</span><span class="sxs-lookup"><span data-stu-id="51025-287">InventAccountTypeStdCostVariance</span></span>|
|<span data-ttu-id="51025-288">InventAdjustmentBy</span><span class="sxs-lookup"><span data-stu-id="51025-288">InventAdjustmentBy</span></span>|
|<span data-ttu-id="51025-289">InventAgingView</span><span class="sxs-lookup"><span data-stu-id="51025-289">InventAgingView</span></span>|
|<span data-ttu-id="51025-290">InventBatchJournalType</span><span class="sxs-lookup"><span data-stu-id="51025-290">InventBatchJournalType</span></span>|
|<span data-ttu-id="51025-291">InventCostBundleState</span><span class="sxs-lookup"><span data-stu-id="51025-291">InventCostBundleState</span></span>|
|<span data-ttu-id="51025-292">InventCostCostDistribution</span><span class="sxs-lookup"><span data-stu-id="51025-292">InventCostCostDistribution</span></span>|
|<span data-ttu-id="51025-293">InventCostTransactionCategory</span><span class="sxs-lookup"><span data-stu-id="51025-293">InventCostTransactionCategory</span></span>|
|<span data-ttu-id="51025-294">InventCostTransRefType</span><span class="sxs-lookup"><span data-stu-id="51025-294">InventCostTransRefType</span></span>|
|<span data-ttu-id="51025-295">InventCountCode</span><span class="sxs-lookup"><span data-stu-id="51025-295">InventCountCode</span></span>|
|<span data-ttu-id="51025-296">InventItemCostingType</span><span class="sxs-lookup"><span data-stu-id="51025-296">InventItemCostingType</span></span>|
|<span data-ttu-id="51025-297">InventItemLookupDefaultTab</span><span class="sxs-lookup"><span data-stu-id="51025-297">InventItemLookupDefaultTab</span></span>|
|<span data-ttu-id="51025-298">InventItemOrderSetupCallerType</span><span class="sxs-lookup"><span data-stu-id="51025-298">InventItemOrderSetupCallerType</span></span>|
|<span data-ttu-id="51025-299">InventItemOrderSetupType</span><span class="sxs-lookup"><span data-stu-id="51025-299">InventItemOrderSetupType</span></span>|
|<span data-ttu-id="51025-300">InventItemPriceCompareLevel</span><span class="sxs-lookup"><span data-stu-id="51025-300">InventItemPriceCompareLevel</span></span>|
|<span data-ttu-id="51025-301">InventItemPriceFilterType</span><span class="sxs-lookup"><span data-stu-id="51025-301">InventItemPriceFilterType</span></span>|
|<span data-ttu-id="51025-302">InventItemPriceType</span><span class="sxs-lookup"><span data-stu-id="51025-302">InventItemPriceType</span></span>|
|<span data-ttu-id="51025-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span><span class="sxs-lookup"><span data-stu-id="51025-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span></span>|
|<span data-ttu-id="51025-304">InventJournalType</span><span class="sxs-lookup"><span data-stu-id="51025-304">InventJournalType</span></span>|
|<span data-ttu-id="51025-305">InventLedgerConflictModule</span><span class="sxs-lookup"><span data-stu-id="51025-305">InventLedgerConflictModule</span></span>|
|<span data-ttu-id="51025-306">InventLocationType</span><span class="sxs-lookup"><span data-stu-id="51025-306">InventLocationType</span></span>|
|<span data-ttu-id="51025-307">InventMovSubType</span><span class="sxs-lookup"><span data-stu-id="51025-307">InventMovSubType</span></span>|
|<span data-ttu-id="51025-308">InventNonConformanceApproval</span><span class="sxs-lookup"><span data-stu-id="51025-308">InventNonConformanceApproval</span></span>|
|<span data-ttu-id="51025-309">InventNonConformanceHistoryType</span><span class="sxs-lookup"><span data-stu-id="51025-309">InventNonConformanceHistoryType</span></span>|
|<span data-ttu-id="51025-310">InventNonConformanceType</span><span class="sxs-lookup"><span data-stu-id="51025-310">InventNonConformanceType</span></span>|
|<span data-ttu-id="51025-311">InventParameters</span><span class="sxs-lookup"><span data-stu-id="51025-311">InventParameters</span></span>|
|<span data-ttu-id="51025-312">InventPhysicalReduction</span><span class="sxs-lookup"><span data-stu-id="51025-312">InventPhysicalReduction</span></span>|
|<span data-ttu-id="51025-313">InventRefType</span><span class="sxs-lookup"><span data-stu-id="51025-313">InventRefType</span></span>|
|<span data-ttu-id="51025-314">InventReleaseOrderPickingType</span><span class="sxs-lookup"><span data-stu-id="51025-314">InventReleaseOrderPickingType</span></span>|
|<span data-ttu-id="51025-315">InventReportDimHistoryLogType</span><span class="sxs-lookup"><span data-stu-id="51025-315">InventReportDimHistoryLogType</span></span>|
|<span data-ttu-id="51025-316">InventStdCostConvItemStatus</span><span class="sxs-lookup"><span data-stu-id="51025-316">InventStdCostConvItemStatus</span></span>|
|<span data-ttu-id="51025-317">InventStdCostPeriodType</span><span class="sxs-lookup"><span data-stu-id="51025-317">InventStdCostPeriodType</span></span>|
|<span data-ttu-id="51025-318">InventSumFields</span><span class="sxs-lookup"><span data-stu-id="51025-318">InventSumFields</span></span>|
|<span data-ttu-id="51025-319">InventSupplyDlvModeSelectCust</span><span class="sxs-lookup"><span data-stu-id="51025-319">InventSupplyDlvModeSelectCust</span></span>|
|<span data-ttu-id="51025-320">InventSupplyDlvModeSelectSupply</span><span class="sxs-lookup"><span data-stu-id="51025-320">InventSupplyDlvModeSelectSupply</span></span>|
|<span data-ttu-id="51025-321">InventSupplyLeadTimeSource</span><span class="sxs-lookup"><span data-stu-id="51025-321">InventSupplyLeadTimeSource</span></span>|
|<span data-ttu-id="51025-322">InventSupplyTmpLeadtimeType</span><span class="sxs-lookup"><span data-stu-id="51025-322">InventSupplyTmpLeadtimeType</span></span>|
|<span data-ttu-id="51025-323">InventTestActionOnFailure</span><span class="sxs-lookup"><span data-stu-id="51025-323">InventTestActionOnFailure</span></span>|
|<span data-ttu-id="51025-324">InventTestBlockProcess</span><span class="sxs-lookup"><span data-stu-id="51025-324">InventTestBlockProcess</span></span>|
|<span data-ttu-id="51025-325">InventTestCorrectionPriority</span><span class="sxs-lookup"><span data-stu-id="51025-325">InventTestCorrectionPriority</span></span>|
|<span data-ttu-id="51025-326">InventTestCorrectionStatus</span><span class="sxs-lookup"><span data-stu-id="51025-326">InventTestCorrectionStatus</span></span>|
|<span data-ttu-id="51025-327">InventTestDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="51025-327">InventTestDocumentStatus</span></span>|
|<span data-ttu-id="51025-328">InventTestOrderStatusDisplay</span><span class="sxs-lookup"><span data-stu-id="51025-328">InventTestOrderStatusDisplay</span></span>|
|<span data-ttu-id="51025-329">InventTestOutcomeStatus</span><span class="sxs-lookup"><span data-stu-id="51025-329">InventTestOutcomeStatus</span></span>|
|<span data-ttu-id="51025-330">InventTestQtySpecification</span><span class="sxs-lookup"><span data-stu-id="51025-330">InventTestQtySpecification</span></span>|
|<span data-ttu-id="51025-331">InventTestQuarantineType</span><span class="sxs-lookup"><span data-stu-id="51025-331">InventTestQuarantineType</span></span>|
|<span data-ttu-id="51025-332">InventTestReferenceType</span><span class="sxs-lookup"><span data-stu-id="51025-332">InventTestReferenceType</span></span>|
|<span data-ttu-id="51025-333">InventTestReport</span><span class="sxs-lookup"><span data-stu-id="51025-333">InventTestReport</span></span>|
|<span data-ttu-id="51025-334">InventTestType</span><span class="sxs-lookup"><span data-stu-id="51025-334">InventTestType</span></span>|
|<span data-ttu-id="51025-335">InventTrackingDimNodeType</span><span class="sxs-lookup"><span data-stu-id="51025-335">InventTrackingDimNodeType</span></span>|
|<span data-ttu-id="51025-336">InventTrackingProductType</span><span class="sxs-lookup"><span data-stu-id="51025-336">InventTrackingProductType</span></span>|
|<span data-ttu-id="51025-337">InventTrackingRegisterTransRegStatus</span><span class="sxs-lookup"><span data-stu-id="51025-337">InventTrackingRegisterTransRegStatus</span></span>|
|<span data-ttu-id="51025-338">InventTransChildType</span><span class="sxs-lookup"><span data-stu-id="51025-338">InventTransChildType</span></span>|
|<span data-ttu-id="51025-339">InventTransferRemainStatus</span><span class="sxs-lookup"><span data-stu-id="51025-339">InventTransferRemainStatus</span></span>|
|<span data-ttu-id="51025-340">InventTransferStatus</span><span class="sxs-lookup"><span data-stu-id="51025-340">InventTransferStatus</span></span>|
|<span data-ttu-id="51025-341">InventTransferUpdateType</span><span class="sxs-lookup"><span data-stu-id="51025-341">InventTransferUpdateType</span></span>|
|<span data-ttu-id="51025-342">InventTransPickRegisterLineStatus</span><span class="sxs-lookup"><span data-stu-id="51025-342">InventTransPickRegisterLineStatus</span></span>|
|<span data-ttu-id="51025-343">InventTransType</span><span class="sxs-lookup"><span data-stu-id="51025-343">InventTransType</span></span>|
|<span data-ttu-id="51025-344">InventUpdType</span><span class="sxs-lookup"><span data-stu-id="51025-344">InventUpdType</span></span>|
|<span data-ttu-id="51025-345">InventValueReportLedgerAccountCategory</span><span class="sxs-lookup"><span data-stu-id="51025-345">InventValueReportLedgerAccountCategory</span></span>|
|<span data-ttu-id="51025-346">InventValueReportLedgerLineType</span><span class="sxs-lookup"><span data-stu-id="51025-346">InventValueReportLedgerLineType</span></span>|
|<span data-ttu-id="51025-347">InventValueReportResourceType</span><span class="sxs-lookup"><span data-stu-id="51025-347">InventValueReportResourceType</span></span>|
|<span data-ttu-id="51025-348">ItemGroupLedgerDimensionGroup</span><span class="sxs-lookup"><span data-stu-id="51025-348">ItemGroupLedgerDimensionGroup</span></span>|
|<span data-ttu-id="51025-349">ItemReservation</span><span class="sxs-lookup"><span data-stu-id="51025-349">ItemReservation</span></span>|
|<span data-ttu-id="51025-350">JmgAbsenceColumnLayout</span><span class="sxs-lookup"><span data-stu-id="51025-350">JmgAbsenceColumnLayout</span></span>|
|<span data-ttu-id="51025-351">JmgAbsenceMethodEnum</span><span class="sxs-lookup"><span data-stu-id="51025-351">JmgAbsenceMethodEnum</span></span>|
|<span data-ttu-id="51025-352">JmgAttendanceRegistrationType</span><span class="sxs-lookup"><span data-stu-id="51025-352">JmgAttendanceRegistrationType</span></span>|
|<span data-ttu-id="51025-353">JmgAttendanceReportType</span><span class="sxs-lookup"><span data-stu-id="51025-353">JmgAttendanceReportType</span></span>|
|<span data-ttu-id="51025-354">JmgBarCodeType</span><span class="sxs-lookup"><span data-stu-id="51025-354">JmgBarCodeType</span></span>|
|<span data-ttu-id="51025-355">JmgBreakDropEnum</span><span class="sxs-lookup"><span data-stu-id="51025-355">JmgBreakDropEnum</span></span>|
|<span data-ttu-id="51025-356">JmgClockStyle</span><span class="sxs-lookup"><span data-stu-id="51025-356">JmgClockStyle</span></span>|
|<span data-ttu-id="51025-357">JmgControlType</span><span class="sxs-lookup"><span data-stu-id="51025-357">JmgControlType</span></span>|
|<span data-ttu-id="51025-358">JmgDaysTotalWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="51025-358">JmgDaysTotalWorkflowStatus</span></span>|
|<span data-ttu-id="51025-359">JmgEmployeeSignInStatus</span><span class="sxs-lookup"><span data-stu-id="51025-359">JmgEmployeeSignInStatus</span></span>|
|<span data-ttu-id="51025-360">JmgFeedbackButtonFunction</span><span class="sxs-lookup"><span data-stu-id="51025-360">JmgFeedbackButtonFunction</span></span>|
|<span data-ttu-id="51025-361">JmgFeedbackStyle</span><span class="sxs-lookup"><span data-stu-id="51025-361">JmgFeedbackStyle</span></span>|
|<span data-ttu-id="51025-362">JmgFieldName</span><span class="sxs-lookup"><span data-stu-id="51025-362">JmgFieldName</span></span>|
|<span data-ttu-id="51025-363">JmgGetRegistrationTimeFrom</span><span class="sxs-lookup"><span data-stu-id="51025-363">JmgGetRegistrationTimeFrom</span></span>|
|<span data-ttu-id="51025-364">JmgGridAppearance</span><span class="sxs-lookup"><span data-stu-id="51025-364">JmgGridAppearance</span></span>|
|<span data-ttu-id="51025-365">JmgJobTableSynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="51025-365">JmgJobTableSynchronizationMode</span></span>|
|<span data-ttu-id="51025-366">JmgJournalRegWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="51025-366">JmgJournalRegWorkflowStatus</span></span>|
|<span data-ttu-id="51025-367">JmgMark</span><span class="sxs-lookup"><span data-stu-id="51025-367">JmgMark</span></span>|
|<span data-ttu-id="51025-368">JmgMessageType</span><span class="sxs-lookup"><span data-stu-id="51025-368">JmgMessageType</span></span>|
|<span data-ttu-id="51025-369">JmgPayAdjustType</span><span class="sxs-lookup"><span data-stu-id="51025-369">JmgPayAdjustType</span></span>|
|<span data-ttu-id="51025-370">JmgPayEventsExportType</span><span class="sxs-lookup"><span data-stu-id="51025-370">JmgPayEventsExportType</span></span>|
|<span data-ttu-id="51025-371">JmgPaySpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="51025-371">JmgPaySpecTypeEnum</span></span>|
|<span data-ttu-id="51025-372">JmgPaySpecTypeEnumPick</span><span class="sxs-lookup"><span data-stu-id="51025-372">JmgPaySpecTypeEnumPick</span></span>|
|<span data-ttu-id="51025-373">JmgPostAutomatically</span><span class="sxs-lookup"><span data-stu-id="51025-373">JmgPostAutomatically</span></span>|
|<span data-ttu-id="51025-374">JmgProdStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-374">JmgProdStatusUpdate</span></span>|
|<span data-ttu-id="51025-375">JmgProdStatusUpdateReportFinished</span><span class="sxs-lookup"><span data-stu-id="51025-375">JmgProdStatusUpdateReportFinished</span></span>|
|<span data-ttu-id="51025-376">JmgProfileSpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="51025-376">JmgProfileSpecTypeEnum</span></span>|
|<span data-ttu-id="51025-377">JmgProfileStartCodeBlankPrev</span><span class="sxs-lookup"><span data-stu-id="51025-377">JmgProfileStartCodeBlankPrev</span></span>|
|<span data-ttu-id="51025-378">JmgProjStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-378">JmgProjStatusUpdate</span></span>|
|<span data-ttu-id="51025-379">JmgRegistrationTouchJobStatus</span><span class="sxs-lookup"><span data-stu-id="51025-379">JmgRegistrationTouchJobStatus</span></span>|
|<span data-ttu-id="51025-380">JmgSecondPresentationEnum</span><span class="sxs-lookup"><span data-stu-id="51025-380">JmgSecondPresentationEnum</span></span>|
|<span data-ttu-id="51025-381">JmgShopFloorServiceStatus</span><span class="sxs-lookup"><span data-stu-id="51025-381">JmgShopFloorServiceStatus</span></span>|
|<span data-ttu-id="51025-382">JmgSignInButtonFunction</span><span class="sxs-lookup"><span data-stu-id="51025-382">JmgSignInButtonFunction</span></span>|
|<span data-ttu-id="51025-383">JmgStoppedCompletedStatus</span><span class="sxs-lookup"><span data-stu-id="51025-383">JmgStoppedCompletedStatus</span></span>|
|<span data-ttu-id="51025-384">JmgTermBaudeRate</span><span class="sxs-lookup"><span data-stu-id="51025-384">JmgTermBaudeRate</span></span>|
|<span data-ttu-id="51025-385">JmgTermComPort</span><span class="sxs-lookup"><span data-stu-id="51025-385">JmgTermComPort</span></span>|
|<span data-ttu-id="51025-386">JmgTermDataBit</span><span class="sxs-lookup"><span data-stu-id="51025-386">JmgTermDataBit</span></span>|
|<span data-ttu-id="51025-387">JmgTerminalInsertMode</span><span class="sxs-lookup"><span data-stu-id="51025-387">JmgTerminalInsertMode</span></span>|
|<span data-ttu-id="51025-388">JmgTermStopBit</span><span class="sxs-lookup"><span data-stu-id="51025-388">JmgTermStopBit</span></span>|
|<span data-ttu-id="51025-389">KanbanBoardRefreshCycle</span><span class="sxs-lookup"><span data-stu-id="51025-389">KanbanBoardRefreshCycle</span></span>|
|<span data-ttu-id="51025-390">KanbanBoardType</span><span class="sxs-lookup"><span data-stu-id="51025-390">KanbanBoardType</span></span>|
|<span data-ttu-id="51025-391">KanbanCardAssignmentType</span><span class="sxs-lookup"><span data-stu-id="51025-391">KanbanCardAssignmentType</span></span>|
|<span data-ttu-id="51025-392">KanbanControlActionState</span><span class="sxs-lookup"><span data-stu-id="51025-392">KanbanControlActionState</span></span>|
|<span data-ttu-id="51025-393">KanbanControlLegendFormat</span><span class="sxs-lookup"><span data-stu-id="51025-393">KanbanControlLegendFormat</span></span>|
|<span data-ttu-id="51025-394">KanbanControlSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="51025-394">KanbanControlSelectionChanged</span></span>|
|<span data-ttu-id="51025-395">KanbanDemandOriginType</span><span class="sxs-lookup"><span data-stu-id="51025-395">KanbanDemandOriginType</span></span>|
|<span data-ttu-id="51025-396">KanbanJobPeggingType</span><span class="sxs-lookup"><span data-stu-id="51025-396">KanbanJobPeggingType</span></span>|
|<span data-ttu-id="51025-397">KanbanJobPickingListLineType</span><span class="sxs-lookup"><span data-stu-id="51025-397">KanbanJobPickingListLineType</span></span>|
|<span data-ttu-id="51025-398">KanbanLineEventType</span><span class="sxs-lookup"><span data-stu-id="51025-398">KanbanLineEventType</span></span>|
|<span data-ttu-id="51025-399">KanbanMultiMode</span><span class="sxs-lookup"><span data-stu-id="51025-399">KanbanMultiMode</span></span>|
|<span data-ttu-id="51025-400">KanbanPrintInstructions</span><span class="sxs-lookup"><span data-stu-id="51025-400">KanbanPrintInstructions</span></span>|
|<span data-ttu-id="51025-401">KanbanProdBOMLineEventType</span><span class="sxs-lookup"><span data-stu-id="51025-401">KanbanProdBOMLineEventType</span></span>|
|<span data-ttu-id="51025-402">KanbanQuantityCalculationStatus</span><span class="sxs-lookup"><span data-stu-id="51025-402">KanbanQuantityCalculationStatus</span></span>|
|<span data-ttu-id="51025-403">KanbanSalesLineEventType</span><span class="sxs-lookup"><span data-stu-id="51025-403">KanbanSalesLineEventType</span></span>|
|<span data-ttu-id="51025-404">KanbanStockReplenishmentEventType</span><span class="sxs-lookup"><span data-stu-id="51025-404">KanbanStockReplenishmentEventType</span></span>|
|<span data-ttu-id="51025-405">LeanBOMLineReservationMethod</span><span class="sxs-lookup"><span data-stu-id="51025-405">LeanBOMLineReservationMethod</span></span>|
|<span data-ttu-id="51025-406">LeanCostingUnusedQtyType</span><span class="sxs-lookup"><span data-stu-id="51025-406">LeanCostingUnusedQtyType</span></span>|
|<span data-ttu-id="51025-407">LeanHandlingUnitEmptyPolicy</span><span class="sxs-lookup"><span data-stu-id="51025-407">LeanHandlingUnitEmptyPolicy</span></span>|
|<span data-ttu-id="51025-408">LeanInventoryControl</span><span class="sxs-lookup"><span data-stu-id="51025-408">LeanInventoryControl</span></span>|
|<span data-ttu-id="51025-409">LeanPeggedEventType</span><span class="sxs-lookup"><span data-stu-id="51025-409">LeanPeggedEventType</span></span>|
|<span data-ttu-id="51025-410">LeanPlanJobReferenceTypes</span><span class="sxs-lookup"><span data-stu-id="51025-410">LeanPlanJobReferenceTypes</span></span>|
|<span data-ttu-id="51025-411">LeanProductionFlowCostingStatus</span><span class="sxs-lookup"><span data-stu-id="51025-411">LeanProductionFlowCostingStatus</span></span>|
|<span data-ttu-id="51025-412">LeanProductionFlowVisualizationViewMode</span><span class="sxs-lookup"><span data-stu-id="51025-412">LeanProductionFlowVisualizationViewMode</span></span>|
|<span data-ttu-id="51025-413">LeanProductTypes</span><span class="sxs-lookup"><span data-stu-id="51025-413">LeanProductTypes</span></span>|
|<span data-ttu-id="51025-414">LeanTaktStatus</span><span class="sxs-lookup"><span data-stu-id="51025-414">LeanTaktStatus</span></span>|
|<span data-ttu-id="51025-415">LedgerPostingType</span><span class="sxs-lookup"><span data-stu-id="51025-415">LedgerPostingType</span></span>|
|<span data-ttu-id="51025-416">LedgerTransTxt</span><span class="sxs-lookup"><span data-stu-id="51025-416">LedgerTransTxt</span></span>|
|<span data-ttu-id="51025-417">MarkupAllocateAfter</span><span class="sxs-lookup"><span data-stu-id="51025-417">MarkupAllocateAfter</span></span>|
|<span data-ttu-id="51025-418">MarkupCategory</span><span class="sxs-lookup"><span data-stu-id="51025-418">MarkupCategory</span></span>|
|<span data-ttu-id="51025-419">MCRBrokerContractStatus</span><span class="sxs-lookup"><span data-stu-id="51025-419">MCRBrokerContractStatus</span></span>|
|<span data-ttu-id="51025-420">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="51025-420">MCRCustSearchType</span></span>|
|<span data-ttu-id="51025-421">MCRFullTextSearchType</span><span class="sxs-lookup"><span data-stu-id="51025-421">MCRFullTextSearchType</span></span>|
|<span data-ttu-id="51025-422">MCRInstallPlanApplyMiscCharge</span><span class="sxs-lookup"><span data-stu-id="51025-422">MCRInstallPlanApplyMiscCharge</span></span>|
|<span data-ttu-id="51025-423">MCRItemListGenerationType</span><span class="sxs-lookup"><span data-stu-id="51025-423">MCRItemListGenerationType</span></span>|
|<span data-ttu-id="51025-424">MCRPickingPrompt</span><span class="sxs-lookup"><span data-stu-id="51025-424">MCRPickingPrompt</span></span>|
|<span data-ttu-id="51025-425">MCRPickingSessionStatus</span><span class="sxs-lookup"><span data-stu-id="51025-425">MCRPickingSessionStatus</span></span>|
|<span data-ttu-id="51025-426">MCRPickingWaveStatus</span><span class="sxs-lookup"><span data-stu-id="51025-426">MCRPickingWaveStatus</span></span>|
|<span data-ttu-id="51025-427">MCRPriceHistoryType</span><span class="sxs-lookup"><span data-stu-id="51025-427">MCRPriceHistoryType</span></span>|
|<span data-ttu-id="51025-428">MCRRoyaltyLineBreakType</span><span class="sxs-lookup"><span data-stu-id="51025-428">MCRRoyaltyLineBreakType</span></span>|
|<span data-ttu-id="51025-429">MCRRoyaltyTakenFrom</span><span class="sxs-lookup"><span data-stu-id="51025-429">MCRRoyaltyTakenFrom</span></span>|
|<span data-ttu-id="51025-430">MCRRoyaltyTransactionType</span><span class="sxs-lookup"><span data-stu-id="51025-430">MCRRoyaltyTransactionType</span></span>|
|<span data-ttu-id="51025-431">MCRRoyaltyUnitType</span><span class="sxs-lookup"><span data-stu-id="51025-431">MCRRoyaltyUnitType</span></span>|
|<span data-ttu-id="51025-432">MCRRoyaltyUOMOption</span><span class="sxs-lookup"><span data-stu-id="51025-432">MCRRoyaltyUOMOption</span></span>|
|<span data-ttu-id="51025-433">MCRSalesOrderDetailStatus</span><span class="sxs-lookup"><span data-stu-id="51025-433">MCRSalesOrderDetailStatus</span></span>|
|<span data-ttu-id="51025-434">ModuleInventCustVend</span><span class="sxs-lookup"><span data-stu-id="51025-434">ModuleInventCustVend</span></span>|
|<span data-ttu-id="51025-435">ModuleInventPurchSales</span><span class="sxs-lookup"><span data-stu-id="51025-435">ModuleInventPurchSales</span></span>|
|<span data-ttu-id="51025-436">OriginalDocument</span><span class="sxs-lookup"><span data-stu-id="51025-436">OriginalDocument</span></span>|
|<span data-ttu-id="51025-437">PaymDocumentType</span><span class="sxs-lookup"><span data-stu-id="51025-437">PaymDocumentType</span></span>|
|<span data-ttu-id="51025-438">PCExpressionEditorSymbolType</span><span class="sxs-lookup"><span data-stu-id="51025-438">PCExpressionEditorSymbolType</span></span>|
|<span data-ttu-id="51025-439">PCLookupMethod</span><span class="sxs-lookup"><span data-stu-id="51025-439">PCLookupMethod</span></span>|
|<span data-ttu-id="51025-440">PCNewSelectComponent</span><span class="sxs-lookup"><span data-stu-id="51025-440">PCNewSelectComponent</span></span>|
|<span data-ttu-id="51025-441">PCRequirement</span><span class="sxs-lookup"><span data-stu-id="51025-441">PCRequirement</span></span>|
|<span data-ttu-id="51025-442">PCTableConstraintType</span><span class="sxs-lookup"><span data-stu-id="51025-442">PCTableConstraintType</span></span>|
|<span data-ttu-id="51025-443">PDSAdjustmentPrinciple</span><span class="sxs-lookup"><span data-stu-id="51025-443">PDSAdjustmentPrinciple</span></span>|
|<span data-ttu-id="51025-444">PdsBatchAttribToleranceAction</span><span class="sxs-lookup"><span data-stu-id="51025-444">PdsBatchAttribToleranceAction</span></span>|
|<span data-ttu-id="51025-445">PdsBatchAttribUpdateType</span><span class="sxs-lookup"><span data-stu-id="51025-445">PdsBatchAttribUpdateType</span></span>|
|<span data-ttu-id="51025-446">PDSCalcElementBase</span><span class="sxs-lookup"><span data-stu-id="51025-446">PDSCalcElementBase</span></span>|
|<span data-ttu-id="51025-447">PDSCompensationPrincipleEnum</span><span class="sxs-lookup"><span data-stu-id="51025-447">PDSCompensationPrincipleEnum</span></span>|
|<span data-ttu-id="51025-448">PDSElementTypeEnum</span><span class="sxs-lookup"><span data-stu-id="51025-448">PDSElementTypeEnum</span></span>|
|<span data-ttu-id="51025-449">PDSIngredientTypeEnum</span><span class="sxs-lookup"><span data-stu-id="51025-449">PDSIngredientTypeEnum</span></span>|
|<span data-ttu-id="51025-450">PdsMRCDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="51025-450">PdsMRCDocumentStatus</span></span>|
|<span data-ttu-id="51025-451">PdsMRCEffectiveDateBasis</span><span class="sxs-lookup"><span data-stu-id="51025-451">PdsMRCEffectiveDateBasis</span></span>|
|<span data-ttu-id="51025-452">PdsMRCEventModule</span><span class="sxs-lookup"><span data-stu-id="51025-452">PdsMRCEventModule</span></span>|
|<span data-ttu-id="51025-453">PdsMRCEventType</span><span class="sxs-lookup"><span data-stu-id="51025-453">PdsMRCEventType</span></span>|
|<span data-ttu-id="51025-454">PdsMRCListType</span><span class="sxs-lookup"><span data-stu-id="51025-454">PdsMRCListType</span></span>|
|<span data-ttu-id="51025-455">PdsPaymtType</span><span class="sxs-lookup"><span data-stu-id="51025-455">PdsPaymtType</span></span>|
|<span data-ttu-id="51025-456">PDSPotencyAttribRecordingEnum</span><span class="sxs-lookup"><span data-stu-id="51025-456">PDSPotencyAttribRecordingEnum</span></span>|
|<span data-ttu-id="51025-457">PdsRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="51025-457">PdsRebateCalcDateType</span></span>|
|<span data-ttu-id="51025-458">PdsRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="51025-458">PdsRebateTakenFrom</span></span>|
|<span data-ttu-id="51025-459">PdsRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="51025-459">PdsRebateUOMOption</span></span>|
|<span data-ttu-id="51025-460">PdsSameLotError</span><span class="sxs-lookup"><span data-stu-id="51025-460">PdsSameLotError</span></span>|
|<span data-ttu-id="51025-461">pdsTMAJournalPosting</span><span class="sxs-lookup"><span data-stu-id="51025-461">pdsTMAJournalPosting</span></span>|
|<span data-ttu-id="51025-462">PdsUpdateBatchDate</span><span class="sxs-lookup"><span data-stu-id="51025-462">PdsUpdateBatchDate</span></span>|
|<span data-ttu-id="51025-463">PdsUpdateDispositionStatus_Quality</span><span class="sxs-lookup"><span data-stu-id="51025-463">PdsUpdateDispositionStatus_Quality</span></span>|
|<span data-ttu-id="51025-464">PlanActivityCreateRelationType</span><span class="sxs-lookup"><span data-stu-id="51025-464">PlanActivityCreateRelationType</span></span>|
|<span data-ttu-id="51025-465">PlanActivityProductionFlowActivityType</span><span class="sxs-lookup"><span data-stu-id="51025-465">PlanActivityProductionFlowActivityType</span></span>|
|<span data-ttu-id="51025-466">PlanTypes</span><span class="sxs-lookup"><span data-stu-id="51025-466">PlanTypes</span></span>|
|<span data-ttu-id="51025-467">PmfCostAllocationMethod</span><span class="sxs-lookup"><span data-stu-id="51025-467">PmfCostAllocationMethod</span></span>|
|<span data-ttu-id="51025-468">PmfOrderType</span><span class="sxs-lookup"><span data-stu-id="51025-468">PmfOrderType</span></span>|
|<span data-ttu-id="51025-469">PmfOrderTypeFilter</span><span class="sxs-lookup"><span data-stu-id="51025-469">PmfOrderTypeFilter</span></span>|
|<span data-ttu-id="51025-470">PmfProdType</span><span class="sxs-lookup"><span data-stu-id="51025-470">PmfProdType</span></span>|
|<span data-ttu-id="51025-471">PMFSeqCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="51025-471">PMFSeqCalendarPeriod</span></span>|
|<span data-ttu-id="51025-472">PriceBase</span><span class="sxs-lookup"><span data-stu-id="51025-472">PriceBase</span></span>|
|<span data-ttu-id="51025-473">PriceDiscPurchasePromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="51025-473">PriceDiscPurchasePromptSystemSource</span></span>|
|<span data-ttu-id="51025-474">PriceDiscSalesPromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="51025-474">PriceDiscSalesPromptSystemSource</span></span>|
|<span data-ttu-id="51025-475">PriceGroupType</span><span class="sxs-lookup"><span data-stu-id="51025-475">PriceGroupType</span></span>|
|<span data-ttu-id="51025-476">PriceSalesPurch</span><span class="sxs-lookup"><span data-stu-id="51025-476">PriceSalesPurch</span></span>|
|<span data-ttu-id="51025-477">PriceType</span><span class="sxs-lookup"><span data-stu-id="51025-477">PriceType</span></span>|
|<span data-ttu-id="51025-478">ProcCategoryAdministrationActivity</span><span class="sxs-lookup"><span data-stu-id="51025-478">ProcCategoryAdministrationActivity</span></span>|
|<span data-ttu-id="51025-479">ProdBOMConsumpProposal</span><span class="sxs-lookup"><span data-stu-id="51025-479">ProdBOMConsumpProposal</span></span>|
|<span data-ttu-id="51025-480">ProdBOMJournalQty</span><span class="sxs-lookup"><span data-stu-id="51025-480">ProdBOMJournalQty</span></span>|
|<span data-ttu-id="51025-481">ProdBOMJournalSplit</span><span class="sxs-lookup"><span data-stu-id="51025-481">ProdBOMJournalSplit</span></span>|
|<span data-ttu-id="51025-482">ProdErrorCause</span><span class="sxs-lookup"><span data-stu-id="51025-482">ProdErrorCause</span></span>|
|<span data-ttu-id="51025-483">ProdGanttJobColorType</span><span class="sxs-lookup"><span data-stu-id="51025-483">ProdGanttJobColorType</span></span>|
|<span data-ttu-id="51025-484">ProdGanttLoad</span><span class="sxs-lookup"><span data-stu-id="51025-484">ProdGanttLoad</span></span>|
|<span data-ttu-id="51025-485">ProdGanttRouteColorType</span><span class="sxs-lookup"><span data-stu-id="51025-485">ProdGanttRouteColorType</span></span>|
|<span data-ttu-id="51025-486">ProdJournalCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="51025-486">ProdJournalCleanUpMode</span></span>|
|<span data-ttu-id="51025-487">ProdMode</span><span class="sxs-lookup"><span data-stu-id="51025-487">ProdMode</span></span>|
|<span data-ttu-id="51025-488">ProdNotificationLevel</span><span class="sxs-lookup"><span data-stu-id="51025-488">ProdNotificationLevel</span></span>|
|<span data-ttu-id="51025-489">ProdParamInventDimLookup</span><span class="sxs-lookup"><span data-stu-id="51025-489">ProdParamInventDimLookup</span></span>|
|<span data-ttu-id="51025-490">ProdParmType</span><span class="sxs-lookup"><span data-stu-id="51025-490">ProdParmType</span></span>|
|<span data-ttu-id="51025-491">ProdRefLookUp</span><span class="sxs-lookup"><span data-stu-id="51025-491">ProdRefLookUp</span></span>|
|<span data-ttu-id="51025-492">ProdRouteJobCurrentFormTabId</span><span class="sxs-lookup"><span data-stu-id="51025-492">ProdRouteJobCurrentFormTabId</span></span>|
|<span data-ttu-id="51025-493">ProdSchedDirection</span><span class="sxs-lookup"><span data-stu-id="51025-493">ProdSchedDirection</span></span>|
|<span data-ttu-id="51025-494">ProdScrapMethod</span><span class="sxs-lookup"><span data-stu-id="51025-494">ProdScrapMethod</span></span>|
|<span data-ttu-id="51025-495">ProdStandardCostVariance</span><span class="sxs-lookup"><span data-stu-id="51025-495">ProdStandardCostVariance</span></span>|
|<span data-ttu-id="51025-496">ProdStatusAll</span><span class="sxs-lookup"><span data-stu-id="51025-496">ProdStatusAll</span></span>|
|<span data-ttu-id="51025-497">ProdStatusType</span><span class="sxs-lookup"><span data-stu-id="51025-497">ProdStatusType</span></span>|
|<span data-ttu-id="51025-498">ProductionTransType</span><span class="sxs-lookup"><span data-stu-id="51025-498">ProductionTransType</span></span>|
|<span data-ttu-id="51025-499">ProdUpdateJour</span><span class="sxs-lookup"><span data-stu-id="51025-499">ProdUpdateJour</span></span>|
|<span data-ttu-id="51025-500">ProdWHSReleasePolicy</span><span class="sxs-lookup"><span data-stu-id="51025-500">ProdWHSReleasePolicy</span></span>|
|<span data-ttu-id="51025-501">ProdWIPType_NA</span><span class="sxs-lookup"><span data-stu-id="51025-501">ProdWIPType_NA</span></span>|
|<span data-ttu-id="51025-502">PurchaseOrderResponseAction</span><span class="sxs-lookup"><span data-stu-id="51025-502">PurchaseOrderResponseAction</span></span>|
|<span data-ttu-id="51025-503">PurchaseType</span><span class="sxs-lookup"><span data-stu-id="51025-503">PurchaseType</span></span>|
|<span data-ttu-id="51025-504">PurchasingTransactionType</span><span class="sxs-lookup"><span data-stu-id="51025-504">PurchasingTransactionType</span></span>|
|<span data-ttu-id="51025-505">PurchCORReceivingMethod</span><span class="sxs-lookup"><span data-stu-id="51025-505">PurchCORReceivingMethod</span></span>|
|<span data-ttu-id="51025-506">PurchCORRejectStatus</span><span class="sxs-lookup"><span data-stu-id="51025-506">PurchCORRejectStatus</span></span>|
|<span data-ttu-id="51025-507">PurchCovRef</span><span class="sxs-lookup"><span data-stu-id="51025-507">PurchCovRef</span></span>|
|<span data-ttu-id="51025-508">PurchDlvAddr</span><span class="sxs-lookup"><span data-stu-id="51025-508">PurchDlvAddr</span></span>|
|<span data-ttu-id="51025-509">PurchLineBackOrderViews</span><span class="sxs-lookup"><span data-stu-id="51025-509">PurchLineBackOrderViews</span></span>|
|<span data-ttu-id="51025-510">PurchLineDeliveryFulfillment</span><span class="sxs-lookup"><span data-stu-id="51025-510">PurchLineDeliveryFulfillment</span></span>|
|<span data-ttu-id="51025-511">PurchLineDeliveryPrecision</span><span class="sxs-lookup"><span data-stu-id="51025-511">PurchLineDeliveryPrecision</span></span>|
|<span data-ttu-id="51025-512">PurchMatchingPolicyOverrideOption</span><span class="sxs-lookup"><span data-stu-id="51025-512">PurchMatchingPolicyOverrideOption</span></span>|
|<span data-ttu-id="51025-513">PurchPrepayApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="51025-513">PurchPrepayApplicationPolicy</span></span>|
|<span data-ttu-id="51025-514">PurchPriceDateType</span><span class="sxs-lookup"><span data-stu-id="51025-514">PurchPriceDateType</span></span>|
|<span data-ttu-id="51025-515">PurchPurchaseOrderCreationMethod</span><span class="sxs-lookup"><span data-stu-id="51025-515">PurchPurchaseOrderCreationMethod</span></span>|
|<span data-ttu-id="51025-516">PurchReApprovalPolicyRuleViewType</span><span class="sxs-lookup"><span data-stu-id="51025-516">PurchReApprovalPolicyRuleViewType</span></span>|
|<span data-ttu-id="51025-517">PurchReqAuthorizationSpecificReporting</span><span class="sxs-lookup"><span data-stu-id="51025-517">PurchReqAuthorizationSpecificReporting</span></span>|
|<span data-ttu-id="51025-518">PurchReqAutoCreatePurch</span><span class="sxs-lookup"><span data-stu-id="51025-518">PurchReqAutoCreatePurch</span></span>|
|<span data-ttu-id="51025-519">PurchReqCatalogAllNon</span><span class="sxs-lookup"><span data-stu-id="51025-519">PurchReqCatalogAllNon</span></span>|
|<span data-ttu-id="51025-520">PurchReqConsolidationActiveStatus</span><span class="sxs-lookup"><span data-stu-id="51025-520">PurchReqConsolidationActiveStatus</span></span>|
|<span data-ttu-id="51025-521">PurchReqConsolidationPriority</span><span class="sxs-lookup"><span data-stu-id="51025-521">PurchReqConsolidationPriority</span></span>|
|<span data-ttu-id="51025-522">PurchReqConsolidationStatus</span><span class="sxs-lookup"><span data-stu-id="51025-522">PurchReqConsolidationStatus</span></span>|
|<span data-ttu-id="51025-523">PurchReqCreationStatus</span><span class="sxs-lookup"><span data-stu-id="51025-523">PurchReqCreationStatus</span></span>|
|<span data-ttu-id="51025-524">PurchReqItemDescriptionTransfer</span><span class="sxs-lookup"><span data-stu-id="51025-524">PurchReqItemDescriptionTransfer</span></span>|
|<span data-ttu-id="51025-525">PurchReqItemFilterType</span><span class="sxs-lookup"><span data-stu-id="51025-525">PurchReqItemFilterType</span></span>|
|<span data-ttu-id="51025-526">PurchReqOnBehalfReports</span><span class="sxs-lookup"><span data-stu-id="51025-526">PurchReqOnBehalfReports</span></span>|
|<span data-ttu-id="51025-527">PurchReqOriginationAuthorizationView</span><span class="sxs-lookup"><span data-stu-id="51025-527">PurchReqOriginationAuthorizationView</span></span>|
|<span data-ttu-id="51025-528">PurchReqProcessingState</span><span class="sxs-lookup"><span data-stu-id="51025-528">PurchReqProcessingState</span></span>|
|<span data-ttu-id="51025-529">PurchReqQuestionnaireAggregateStatus</span><span class="sxs-lookup"><span data-stu-id="51025-529">PurchReqQuestionnaireAggregateStatus</span></span>|
|<span data-ttu-id="51025-530">PurchReqQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="51025-530">PurchReqQuestionnaireStatus</span></span>|
|<span data-ttu-id="51025-531">PurchReqReportSortOrder</span><span class="sxs-lookup"><span data-stu-id="51025-531">PurchReqReportSortOrder</span></span>|
|<span data-ttu-id="51025-532">PurchReqReportStatus</span><span class="sxs-lookup"><span data-stu-id="51025-532">PurchReqReportStatus</span></span>|
|<span data-ttu-id="51025-533">PurchReqReviewStatus</span><span class="sxs-lookup"><span data-stu-id="51025-533">PurchReqReviewStatus</span></span>|
|<span data-ttu-id="51025-534">PurchReqRFQRequirement</span><span class="sxs-lookup"><span data-stu-id="51025-534">PurchReqRFQRequirement</span></span>|
|<span data-ttu-id="51025-535">PurchReqRFQType</span><span class="sxs-lookup"><span data-stu-id="51025-535">PurchReqRFQType</span></span>|
|<span data-ttu-id="51025-536">PurchReqSaveChanges</span><span class="sxs-lookup"><span data-stu-id="51025-536">PurchReqSaveChanges</span></span>|
|<span data-ttu-id="51025-537">PurchReqStatus</span><span class="sxs-lookup"><span data-stu-id="51025-537">PurchReqStatus</span></span>|
|<span data-ttu-id="51025-538">PurchReqType</span><span class="sxs-lookup"><span data-stu-id="51025-538">PurchReqType</span></span>|
|<span data-ttu-id="51025-539">PurchReqWorkflowState</span><span class="sxs-lookup"><span data-stu-id="51025-539">PurchReqWorkflowState</span></span>|
|<span data-ttu-id="51025-540">PurchRFQQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="51025-540">PurchRFQQuestionnaireStatus</span></span>|
|<span data-ttu-id="51025-541">PurchRFQStatusVendor</span><span class="sxs-lookup"><span data-stu-id="51025-541">PurchRFQStatusVendor</span></span>|
|<span data-ttu-id="51025-542">PurchRFQType</span><span class="sxs-lookup"><span data-stu-id="51025-542">PurchRFQType</span></span>|
|<span data-ttu-id="51025-543">PurchTableFormId</span><span class="sxs-lookup"><span data-stu-id="51025-543">PurchTableFormId</span></span>|
|<span data-ttu-id="51025-544">PurchTableListPage</span><span class="sxs-lookup"><span data-stu-id="51025-544">PurchTableListPage</span></span>|
|<span data-ttu-id="51025-545">PurchTableMode</span><span class="sxs-lookup"><span data-stu-id="51025-545">PurchTableMode</span></span>|
|<span data-ttu-id="51025-546">PurchTotalsCachingMethod</span><span class="sxs-lookup"><span data-stu-id="51025-546">PurchTotalsCachingMethod</span></span>|
|<span data-ttu-id="51025-547">PurchUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-547">PurchUpdate</span></span>|
|<span data-ttu-id="51025-548">PurchVendorPortalShowResponseType</span><span class="sxs-lookup"><span data-stu-id="51025-548">PurchVendorPortalShowResponseType</span></span>|
|<span data-ttu-id="51025-549">QuotationType</span><span class="sxs-lookup"><span data-stu-id="51025-549">QuotationType</span></span>|
|<span data-ttu-id="51025-550">ReqBOMRouteCreated</span><span class="sxs-lookup"><span data-stu-id="51025-550">ReqBOMRouteCreated</span></span>|
|<span data-ttu-id="51025-551">ReqCurrentDaySchedFrom</span><span class="sxs-lookup"><span data-stu-id="51025-551">ReqCurrentDaySchedFrom</span></span>|
|<span data-ttu-id="51025-552">ReqDemPlanDataSourceType</span><span class="sxs-lookup"><span data-stu-id="51025-552">ReqDemPlanDataSourceType</span></span>|
|<span data-ttu-id="51025-553">ReqDemPlanDemandCategory</span><span class="sxs-lookup"><span data-stu-id="51025-553">ReqDemPlanDemandCategory</span></span>|
|<span data-ttu-id="51025-554">ReqDemPlanForecastAttributeType</span><span class="sxs-lookup"><span data-stu-id="51025-554">ReqDemPlanForecastAttributeType</span></span>|
|<span data-ttu-id="51025-555">ReqDemPlanForecastingStrategy</span><span class="sxs-lookup"><span data-stu-id="51025-555">ReqDemPlanForecastingStrategy</span></span>|
|<span data-ttu-id="51025-556">ReqDemPlanForecastType</span><span class="sxs-lookup"><span data-stu-id="51025-556">ReqDemPlanForecastType</span></span>|
|<span data-ttu-id="51025-557">ReqDisplayDelay</span><span class="sxs-lookup"><span data-stu-id="51025-557">ReqDisplayDelay</span></span>|
|<span data-ttu-id="51025-558">ReqForecastReducedBy</span><span class="sxs-lookup"><span data-stu-id="51025-558">ReqForecastReducedBy</span></span>|
|<span data-ttu-id="51025-559">ReqGanttColorType</span><span class="sxs-lookup"><span data-stu-id="51025-559">ReqGanttColorType</span></span>|
|<span data-ttu-id="51025-560">ReqGanttShow</span><span class="sxs-lookup"><span data-stu-id="51025-560">ReqGanttShow</span></span>|
|<span data-ttu-id="51025-561">ReqItemJournalType</span><span class="sxs-lookup"><span data-stu-id="51025-561">ReqItemJournalType</span></span>|
|<span data-ttu-id="51025-562">ReqItemTableWizardPurpose</span><span class="sxs-lookup"><span data-stu-id="51025-562">ReqItemTableWizardPurpose</span></span>|
|<span data-ttu-id="51025-563">ReqMarkUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-563">ReqMarkUpdate</span></span>|
|<span data-ttu-id="51025-564">ReqPeggingAssignmentType</span><span class="sxs-lookup"><span data-stu-id="51025-564">ReqPeggingAssignmentType</span></span>|
|<span data-ttu-id="51025-565">ReqPeggingType</span><span class="sxs-lookup"><span data-stu-id="51025-565">ReqPeggingType</span></span>|
|<span data-ttu-id="51025-566">ReqPlannedOrderLeveling</span><span class="sxs-lookup"><span data-stu-id="51025-566">ReqPlannedOrderLeveling</span></span>|
|<span data-ttu-id="51025-567">ReqPlanType</span><span class="sxs-lookup"><span data-stu-id="51025-567">ReqPlanType</span></span>|
|<span data-ttu-id="51025-568">ReqPOStatus</span><span class="sxs-lookup"><span data-stu-id="51025-568">ReqPOStatus</span></span>|
|<span data-ttu-id="51025-569">ReqQtyAmount</span><span class="sxs-lookup"><span data-stu-id="51025-569">ReqQtyAmount</span></span>|
|<span data-ttu-id="51025-570">ReqRefType</span><span class="sxs-lookup"><span data-stu-id="51025-570">ReqRefType</span></span>|
|<span data-ttu-id="51025-571">ReqRefTypeShort</span><span class="sxs-lookup"><span data-stu-id="51025-571">ReqRefTypeShort</span></span>|
|<span data-ttu-id="51025-572">ReqRefTypeTrunc</span><span class="sxs-lookup"><span data-stu-id="51025-572">ReqRefTypeTrunc</span></span>|
|<span data-ttu-id="51025-573">ReqTraceMessageType</span><span class="sxs-lookup"><span data-stu-id="51025-573">ReqTraceMessageType</span></span>|
|<span data-ttu-id="51025-574">ReqTransFuturesActionPartType</span><span class="sxs-lookup"><span data-stu-id="51025-574">ReqTransFuturesActionPartType</span></span>|
|<span data-ttu-id="51025-575">ReturnCodeType</span><span class="sxs-lookup"><span data-stu-id="51025-575">ReturnCodeType</span></span>|
|<span data-ttu-id="51025-576">ReturnCycleTimeScope</span><span class="sxs-lookup"><span data-stu-id="51025-576">ReturnCycleTimeScope</span></span>|
|<span data-ttu-id="51025-577">ReturnReasonCodeDispExtended</span><span class="sxs-lookup"><span data-stu-id="51025-577">ReturnReasonCodeDispExtended</span></span>|
|<span data-ttu-id="51025-578">ReturnReasonDispCode</span><span class="sxs-lookup"><span data-stu-id="51025-578">ReturnReasonDispCode</span></span>|
|<span data-ttu-id="51025-579">ReturnUpdateAction</span><span class="sxs-lookup"><span data-stu-id="51025-579">ReturnUpdateAction</span></span>|
|<span data-ttu-id="51025-580">RouteFormula</span><span class="sxs-lookup"><span data-stu-id="51025-580">RouteFormula</span></span>|
|<span data-ttu-id="51025-581">RouteOprPriority</span><span class="sxs-lookup"><span data-stu-id="51025-581">RouteOprPriority</span></span>|
|<span data-ttu-id="51025-582">SalesBasketType</span><span class="sxs-lookup"><span data-stu-id="51025-582">SalesBasketType</span></span>|
|<span data-ttu-id="51025-583">SalesBatch</span><span class="sxs-lookup"><span data-stu-id="51025-583">SalesBatch</span></span>|
|<span data-ttu-id="51025-584">SalesCheckForPickup</span><span class="sxs-lookup"><span data-stu-id="51025-584">SalesCheckForPickup</span></span>|
|<span data-ttu-id="51025-585">SalesCheckQtyCachKey</span><span class="sxs-lookup"><span data-stu-id="51025-585">SalesCheckQtyCachKey</span></span>|
|<span data-ttu-id="51025-586">SalesDeliveryTimeState</span><span class="sxs-lookup"><span data-stu-id="51025-586">SalesDeliveryTimeState</span></span>|
|<span data-ttu-id="51025-587">SalesDocumentTimezonePreference</span><span class="sxs-lookup"><span data-stu-id="51025-587">SalesDocumentTimezonePreference</span></span>|
|<span data-ttu-id="51025-588">SalesPriceDateType</span><span class="sxs-lookup"><span data-stu-id="51025-588">SalesPriceDateType</span></span>|
|<span data-ttu-id="51025-589">SalesPriceModelBasic</span><span class="sxs-lookup"><span data-stu-id="51025-589">SalesPriceModelBasic</span></span>|
|<span data-ttu-id="51025-590">SalesPurchCopy</span><span class="sxs-lookup"><span data-stu-id="51025-590">SalesPurchCopy</span></span>|
|<span data-ttu-id="51025-591">SalesPurchCycleAction</span><span class="sxs-lookup"><span data-stu-id="51025-591">SalesPurchCycleAction</span></span>|
|<span data-ttu-id="51025-592">SalesPurchGroup</span><span class="sxs-lookup"><span data-stu-id="51025-592">SalesPurchGroup</span></span>|
|<span data-ttu-id="51025-593">SalesPurchParmCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="51025-593">SalesPurchParmCleanUpMode</span></span>|
|<span data-ttu-id="51025-594">SalesQuotationFilter</span><span class="sxs-lookup"><span data-stu-id="51025-594">SalesQuotationFilter</span></span>|
|<span data-ttu-id="51025-595">SalesQuotationLinkToProject</span><span class="sxs-lookup"><span data-stu-id="51025-595">SalesQuotationLinkToProject</span></span>|
|<span data-ttu-id="51025-596">SalesQuotationListPage</span><span class="sxs-lookup"><span data-stu-id="51025-596">SalesQuotationListPage</span></span>|
|<span data-ttu-id="51025-597">SalesQuotationPriceConversion</span><span class="sxs-lookup"><span data-stu-id="51025-597">SalesQuotationPriceConversion</span></span>|
|<span data-ttu-id="51025-598">SalesQuotationPriceSimResult</span><span class="sxs-lookup"><span data-stu-id="51025-598">SalesQuotationPriceSimResult</span></span>|
|<span data-ttu-id="51025-599">SalesQuotationTypeListPage</span><span class="sxs-lookup"><span data-stu-id="51025-599">SalesQuotationTypeListPage</span></span>|
|<span data-ttu-id="51025-600">SalesShipping</span><span class="sxs-lookup"><span data-stu-id="51025-600">SalesShipping</span></span>|
|<span data-ttu-id="51025-601">SalesSourcingOrigin</span><span class="sxs-lookup"><span data-stu-id="51025-601">SalesSourcingOrigin</span></span>|
|<span data-ttu-id="51025-602">SalesStatus</span><span class="sxs-lookup"><span data-stu-id="51025-602">SalesStatus</span></span>|
|<span data-ttu-id="51025-603">SalesTableFormId</span><span class="sxs-lookup"><span data-stu-id="51025-603">SalesTableFormId</span></span>|
|<span data-ttu-id="51025-604">SalesTableListPage</span><span class="sxs-lookup"><span data-stu-id="51025-604">SalesTableListPage</span></span>|
|<span data-ttu-id="51025-605">SalesTableMode</span><span class="sxs-lookup"><span data-stu-id="51025-605">SalesTableMode</span></span>|
|<span data-ttu-id="51025-606">SalesType</span><span class="sxs-lookup"><span data-stu-id="51025-606">SalesType</span></span>|
|<span data-ttu-id="51025-607">SalesUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-607">SalesUpdate</span></span>|
|<span data-ttu-id="51025-608">ShipCarrierDlvType</span><span class="sxs-lookup"><span data-stu-id="51025-608">ShipCarrierDlvType</span></span>|
|<span data-ttu-id="51025-609">ShipCarrierFreightApplied</span><span class="sxs-lookup"><span data-stu-id="51025-609">ShipCarrierFreightApplied</span></span>|
|<span data-ttu-id="51025-610">ShipCarrierMkUpFreight</span><span class="sxs-lookup"><span data-stu-id="51025-610">ShipCarrierMkUpFreight</span></span>|
|<span data-ttu-id="51025-611">SMAInvoiceProjectSelection</span><span class="sxs-lookup"><span data-stu-id="51025-611">SMAInvoiceProjectSelection</span></span>|
|<span data-ttu-id="51025-612">SMAItemSetupType</span><span class="sxs-lookup"><span data-stu-id="51025-612">SMAItemSetupType</span></span>|
|<span data-ttu-id="51025-613">SMAProjectSelection</span><span class="sxs-lookup"><span data-stu-id="51025-613">SMAProjectSelection</span></span>|
|<span data-ttu-id="51025-614">SMAReasonType</span><span class="sxs-lookup"><span data-stu-id="51025-614">SMAReasonType</span></span>|
|<span data-ttu-id="51025-615">SMAServiceBOMChangeAction</span><span class="sxs-lookup"><span data-stu-id="51025-615">SMAServiceBOMChangeAction</span></span>|
|<span data-ttu-id="51025-616">SMAServiceFunctionType</span><span class="sxs-lookup"><span data-stu-id="51025-616">SMAServiceFunctionType</span></span>|
|<span data-ttu-id="51025-617">SMAServiceLevelAgreementLogType</span><span class="sxs-lookup"><span data-stu-id="51025-617">SMAServiceLevelAgreementLogType</span></span>|
|<span data-ttu-id="51025-618">SMAServiceOrderActionType</span><span class="sxs-lookup"><span data-stu-id="51025-618">SMAServiceOrderActionType</span></span>|
|<span data-ttu-id="51025-619">SMAServiceOrderFilter</span><span class="sxs-lookup"><span data-stu-id="51025-619">SMAServiceOrderFilter</span></span>|
|<span data-ttu-id="51025-620">SMAServiceOrderOrigin</span><span class="sxs-lookup"><span data-stu-id="51025-620">SMAServiceOrderOrigin</span></span>|
|<span data-ttu-id="51025-621">SMAServiceOrderProgress</span><span class="sxs-lookup"><span data-stu-id="51025-621">SMAServiceOrderProgress</span></span>|
|<span data-ttu-id="51025-622">SMAServiceTaskTitleOption</span><span class="sxs-lookup"><span data-stu-id="51025-622">SMAServiceTaskTitleOption</span></span>|
|<span data-ttu-id="51025-623">SMASubscriptionPeriodType</span><span class="sxs-lookup"><span data-stu-id="51025-623">SMASubscriptionPeriodType</span></span>|
|<span data-ttu-id="51025-624">SMAWizardCreateType</span><span class="sxs-lookup"><span data-stu-id="51025-624">SMAWizardCreateType</span></span>|
|<span data-ttu-id="51025-625">smmAccountNumToCreate</span><span class="sxs-lookup"><span data-stu-id="51025-625">smmAccountNumToCreate</span></span>|
|<span data-ttu-id="51025-626">smmActivityParentType</span><span class="sxs-lookup"><span data-stu-id="51025-626">smmActivityParentType</span></span>|
|<span data-ttu-id="51025-627">smmAppointmentNThInstance</span><span class="sxs-lookup"><span data-stu-id="51025-627">smmAppointmentNThInstance</span></span>|
|<span data-ttu-id="51025-628">smmBusinessRelationsListFilter</span><span class="sxs-lookup"><span data-stu-id="51025-628">smmBusinessRelationsListFilter</span></span>|
|<span data-ttu-id="51025-629">smmBusRelTypeSourceTable</span><span class="sxs-lookup"><span data-stu-id="51025-629">smmBusRelTypeSourceTable</span></span>|
|<span data-ttu-id="51025-630">smmCampaignBroadcastType</span><span class="sxs-lookup"><span data-stu-id="51025-630">smmCampaignBroadcastType</span></span>|
|<span data-ttu-id="51025-631">smmCampaignProjectJournalType</span><span class="sxs-lookup"><span data-stu-id="51025-631">smmCampaignProjectJournalType</span></span>|
|<span data-ttu-id="51025-632">smmCampaignResponse</span><span class="sxs-lookup"><span data-stu-id="51025-632">smmCampaignResponse</span></span>|
|<span data-ttu-id="51025-633">smmCampaignsListFilter</span><span class="sxs-lookup"><span data-stu-id="51025-633">smmCampaignsListFilter</span></span>|
|<span data-ttu-id="51025-634">smmContactsListFilter</span><span class="sxs-lookup"><span data-stu-id="51025-634">smmContactsListFilter</span></span>|
|<span data-ttu-id="51025-635">smmCreateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="51025-635">smmCreateOpportunityOptions</span></span>|
|<span data-ttu-id="51025-636">smmDisplayEMailInOutlook</span><span class="sxs-lookup"><span data-stu-id="51025-636">smmDisplayEMailInOutlook</span></span>|
|<span data-ttu-id="51025-637">smmDragDropObjectType</span><span class="sxs-lookup"><span data-stu-id="51025-637">smmDragDropObjectType</span></span>|
|<span data-ttu-id="51025-638">smmDupMethods</span><span class="sxs-lookup"><span data-stu-id="51025-638">smmDupMethods</span></span>|
|<span data-ttu-id="51025-639">smmEMailSMS</span><span class="sxs-lookup"><span data-stu-id="51025-639">smmEMailSMS</span></span>|
|<span data-ttu-id="51025-640">smmEntityToCreate</span><span class="sxs-lookup"><span data-stu-id="51025-640">smmEntityToCreate</span></span>|
|<span data-ttu-id="51025-641">smmFieldDelimiters</span><span class="sxs-lookup"><span data-stu-id="51025-641">smmFieldDelimiters</span></span>|
|<span data-ttu-id="51025-642">smmLeadsListFilter</span><span class="sxs-lookup"><span data-stu-id="51025-642">smmLeadsListFilter</span></span>|
|<span data-ttu-id="51025-643">smmLogType</span><span class="sxs-lookup"><span data-stu-id="51025-643">smmLogType</span></span>|
|<span data-ttu-id="51025-644">smmOpportunitiesListFilter</span><span class="sxs-lookup"><span data-stu-id="51025-644">smmOpportunitiesListFilter</span></span>|
|<span data-ttu-id="51025-645">smmOpportunityAssociation</span><span class="sxs-lookup"><span data-stu-id="51025-645">smmOpportunityAssociation</span></span>|
|<span data-ttu-id="51025-646">smmOutlookContactDeleteAction</span><span class="sxs-lookup"><span data-stu-id="51025-646">smmOutlookContactDeleteAction</span></span>|
|<span data-ttu-id="51025-647">smmOutlookRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="51025-647">smmOutlookRecurrenceType</span></span>|
|<span data-ttu-id="51025-648">smmOutlookSyncPrinciple</span><span class="sxs-lookup"><span data-stu-id="51025-648">smmOutlookSyncPrinciple</span></span>|
|<span data-ttu-id="51025-649">smmOutlookUpdateAction</span><span class="sxs-lookup"><span data-stu-id="51025-649">smmOutlookUpdateAction</span></span>|
|<span data-ttu-id="51025-650">smmProjectNewExisting</span><span class="sxs-lookup"><span data-stu-id="51025-650">smmProjectNewExisting</span></span>|
|<span data-ttu-id="51025-651">smmQuotationAccountType</span><span class="sxs-lookup"><span data-stu-id="51025-651">smmQuotationAccountType</span></span>|
|<span data-ttu-id="51025-652">smmQuotationStatus</span><span class="sxs-lookup"><span data-stu-id="51025-652">smmQuotationStatus</span></span>|
|<span data-ttu-id="51025-653">smmRecordDelimiters</span><span class="sxs-lookup"><span data-stu-id="51025-653">smmRecordDelimiters</span></span>|
|<span data-ttu-id="51025-654">smmSalesUnitMemberRelation</span><span class="sxs-lookup"><span data-stu-id="51025-654">smmSalesUnitMemberRelation</span></span>|
|<span data-ttu-id="51025-655">SmmSourceTypeList</span><span class="sxs-lookup"><span data-stu-id="51025-655">SmmSourceTypeList</span></span>|
|<span data-ttu-id="51025-656">smmSwotType</span><span class="sxs-lookup"><span data-stu-id="51025-656">smmSwotType</span></span>|
|<span data-ttu-id="51025-657">smmTransLogUpdateAction</span><span class="sxs-lookup"><span data-stu-id="51025-657">smmTransLogUpdateAction</span></span>|
|<span data-ttu-id="51025-658">smmUpdateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="51025-658">smmUpdateOpportunityOptions</span></span>|
|<span data-ttu-id="51025-659">smmWarningError</span><span class="sxs-lookup"><span data-stu-id="51025-659">smmWarningError</span></span>|
|<span data-ttu-id="51025-660">SMAActiveAll</span><span class="sxs-lookup"><span data-stu-id="51025-660">SMAActiveAll</span></span>|
|<span data-ttu-id="51025-661">SMAAgreementFilter</span><span class="sxs-lookup"><span data-stu-id="51025-661">SMAAgreementFilter</span></span>|
|<span data-ttu-id="51025-662">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="51025-662">SMAAgreementTableListPageType</span></span>|
|<span data-ttu-id="51025-663">TAMCustRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="51025-663">TAMCustRebateApprovalStatus</span></span>|
|<span data-ttu-id="51025-664">TAMFundStatus</span><span class="sxs-lookup"><span data-stu-id="51025-664">TAMFundStatus</span></span>|
|<span data-ttu-id="51025-665">TAMFundType</span><span class="sxs-lookup"><span data-stu-id="51025-665">TAMFundType</span></span>|
|<span data-ttu-id="51025-666">TAMPromoCustomerType</span><span class="sxs-lookup"><span data-stu-id="51025-666">TAMPromoCustomerType</span></span>|
|<span data-ttu-id="51025-667">TAMPromoMerchEvent</span><span class="sxs-lookup"><span data-stu-id="51025-667">TAMPromoMerchEvent</span></span>|
|<span data-ttu-id="51025-668">TAMPromoMgmtApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="51025-668">TAMPromoMgmtApprovalStatus</span></span>|
|<span data-ttu-id="51025-669">TAMPromotionDate</span><span class="sxs-lookup"><span data-stu-id="51025-669">TAMPromotionDate</span></span>|
|<span data-ttu-id="51025-670">TAMPromotionMode</span><span class="sxs-lookup"><span data-stu-id="51025-670">TAMPromotionMode</span></span>|
|<span data-ttu-id="51025-671">TAMRebateCustInclusive</span><span class="sxs-lookup"><span data-stu-id="51025-671">TAMRebateCustInclusive</span></span>|
|<span data-ttu-id="51025-672">TAMRebateLineBreakType</span><span class="sxs-lookup"><span data-stu-id="51025-672">TAMRebateLineBreakType</span></span>|
|<span data-ttu-id="51025-673">TAMRebateStatus</span><span class="sxs-lookup"><span data-stu-id="51025-673">TAMRebateStatus</span></span>|
|<span data-ttu-id="51025-674">TAMRebateUnitType</span><span class="sxs-lookup"><span data-stu-id="51025-674">TAMRebateUnitType</span></span>|
|<span data-ttu-id="51025-675">TAMRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="51025-675">TAMRebateUOMOption</span></span>|
|<span data-ttu-id="51025-676">TAMVendRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="51025-676">TAMVendRebateApprovalStatus</span></span>|
|<span data-ttu-id="51025-677">TAMVendRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="51025-677">TAMVendRebateCalcDateType</span></span>|
|<span data-ttu-id="51025-678">TAMVendRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="51025-678">TAMVendRebateTakenFrom</span></span>|
|<span data-ttu-id="51025-679">TAMVendRebateTransactionType</span><span class="sxs-lookup"><span data-stu-id="51025-679">TAMVendRebateTransactionType</span></span>|
|<span data-ttu-id="51025-680">TaxModuleType</span><span class="sxs-lookup"><span data-stu-id="51025-680">TaxModuleType</span></span>|
|<span data-ttu-id="51025-681">TaxSourceType</span><span class="sxs-lookup"><span data-stu-id="51025-681">TaxSourceType</span></span>|
|<span data-ttu-id="51025-682">TMSAccessorialAssignmentLevel</span><span class="sxs-lookup"><span data-stu-id="51025-682">TMSAccessorialAssignmentLevel</span></span>|
|<span data-ttu-id="51025-683">TMSAccessorialAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="51025-683">TMSAccessorialAssignmentTarget</span></span>|
|<span data-ttu-id="51025-684">TMSAccessorialDeliveryType</span><span class="sxs-lookup"><span data-stu-id="51025-684">TMSAccessorialDeliveryType</span></span>|
|<span data-ttu-id="51025-685">TMSAccessorialType</span><span class="sxs-lookup"><span data-stu-id="51025-685">TMSAccessorialType</span></span>|
|<span data-ttu-id="51025-686">TMSAppointmentAlert</span><span class="sxs-lookup"><span data-stu-id="51025-686">TMSAppointmentAlert</span></span>|
|<span data-ttu-id="51025-687">TMSDiscountResultType</span><span class="sxs-lookup"><span data-stu-id="51025-687">TMSDiscountResultType</span></span>|
|<span data-ttu-id="51025-688">TMSDiscountType</span><span class="sxs-lookup"><span data-stu-id="51025-688">TMSDiscountType</span></span>|
|<span data-ttu-id="51025-689">TMSFeeType</span><span class="sxs-lookup"><span data-stu-id="51025-689">TMSFeeType</span></span>|
|<span data-ttu-id="51025-690">TMSFreightBillMatchStatus</span><span class="sxs-lookup"><span data-stu-id="51025-690">TMSFreightBillMatchStatus</span></span>|
|<span data-ttu-id="51025-691">TMSFreightBillReconcileType</span><span class="sxs-lookup"><span data-stu-id="51025-691">TMSFreightBillReconcileType</span></span>|
|<span data-ttu-id="51025-692">TMSFwkErrorType</span><span class="sxs-lookup"><span data-stu-id="51025-692">TMSFwkErrorType</span></span>|
|<span data-ttu-id="51025-693">TMSHubPosition</span><span class="sxs-lookup"><span data-stu-id="51025-693">TMSHubPosition</span></span>|
|<span data-ttu-id="51025-694">TMSInvoiceAccountType</span><span class="sxs-lookup"><span data-stu-id="51025-694">TMSInvoiceAccountType</span></span>|
|<span data-ttu-id="51025-695">TMSLineType</span><span class="sxs-lookup"><span data-stu-id="51025-695">TMSLineType</span></span>|
|<span data-ttu-id="51025-696">TMSLoadBuildSessionState</span><span class="sxs-lookup"><span data-stu-id="51025-696">TMSLoadBuildSessionState</span></span>|
|<span data-ttu-id="51025-697">TMSLoadTender</span><span class="sxs-lookup"><span data-stu-id="51025-697">TMSLoadTender</span></span>|
|<span data-ttu-id="51025-698">TMSLookupType</span><span class="sxs-lookup"><span data-stu-id="51025-698">TMSLookupType</span></span>|
|<span data-ttu-id="51025-699">TMSNumberSequenceType</span><span class="sxs-lookup"><span data-stu-id="51025-699">TMSNumberSequenceType</span></span>|
|<span data-ttu-id="51025-700">TMSOverrideLocationType</span><span class="sxs-lookup"><span data-stu-id="51025-700">TMSOverrideLocationType</span></span>|
|<span data-ttu-id="51025-701">TMSRecurrenceDays</span><span class="sxs-lookup"><span data-stu-id="51025-701">TMSRecurrenceDays</span></span>|
|<span data-ttu-id="51025-702">TMSRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="51025-702">TMSRecurrenceType</span></span>|
|<span data-ttu-id="51025-703">TMSRecurrenceWeeks</span><span class="sxs-lookup"><span data-stu-id="51025-703">TMSRecurrenceWeeks</span></span>|
|<span data-ttu-id="51025-704">TMSResponsibleForPayment</span><span class="sxs-lookup"><span data-stu-id="51025-704">TMSResponsibleForPayment</span></span>|
|<span data-ttu-id="51025-705">TMSRouteStatus</span><span class="sxs-lookup"><span data-stu-id="51025-705">TMSRouteStatus</span></span>|
|<span data-ttu-id="51025-706">TMSSalesPurchTransfer</span><span class="sxs-lookup"><span data-stu-id="51025-706">TMSSalesPurchTransfer</span></span>|
|<span data-ttu-id="51025-707">TMSTableRef</span><span class="sxs-lookup"><span data-stu-id="51025-707">TMSTableRef</span></span>|
|<span data-ttu-id="51025-708">TMSTransportationType</span><span class="sxs-lookup"><span data-stu-id="51025-708">TMSTransportationType</span></span>|
|<span data-ttu-id="51025-709">TMSTransportRefType</span><span class="sxs-lookup"><span data-stu-id="51025-709">TMSTransportRefType</span></span>|
|<span data-ttu-id="51025-710">TMSTransportTypeFilter</span><span class="sxs-lookup"><span data-stu-id="51025-710">TMSTransportTypeFilter</span></span>|
|<span data-ttu-id="51025-711">TMSUOM</span><span class="sxs-lookup"><span data-stu-id="51025-711">TMSUOM</span></span>|
|<span data-ttu-id="51025-712">TMSZoneType</span><span class="sxs-lookup"><span data-stu-id="51025-712">TMSZoneType</span></span>|
|<span data-ttu-id="51025-713">TradeCurencyConversion</span><span class="sxs-lookup"><span data-stu-id="51025-713">TradeCurencyConversion</span></span>|
|<span data-ttu-id="51025-714">TradeLineDlvType</span><span class="sxs-lookup"><span data-stu-id="51025-714">TradeLineDlvType</span></span>|
|<span data-ttu-id="51025-715">TradeNonStockedConversionChangeType</span><span class="sxs-lookup"><span data-stu-id="51025-715">TradeNonStockedConversionChangeType</span></span>|
|<span data-ttu-id="51025-716">TradeNonStockedConversionIssue</span><span class="sxs-lookup"><span data-stu-id="51025-716">TradeNonStockedConversionIssue</span></span>|
|<span data-ttu-id="51025-717">TradeNonStockedConversionResolveUndo</span><span class="sxs-lookup"><span data-stu-id="51025-717">TradeNonStockedConversionResolveUndo</span></span>|
|<span data-ttu-id="51025-718">TradePrintType</span><span class="sxs-lookup"><span data-stu-id="51025-718">TradePrintType</span></span>|
|<span data-ttu-id="51025-719">TradeTable2LineUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-719">TradeTable2LineUpdate</span></span>|
|<span data-ttu-id="51025-720">VendNotificationCategorySelection</span><span class="sxs-lookup"><span data-stu-id="51025-720">VendNotificationCategorySelection</span></span>|
|<span data-ttu-id="51025-721">VendNotificationStatus</span><span class="sxs-lookup"><span data-stu-id="51025-721">VendNotificationStatus</span></span>|
|<span data-ttu-id="51025-722">VendPackingSlipTransTimeStatus</span><span class="sxs-lookup"><span data-stu-id="51025-722">VendPackingSlipTransTimeStatus</span></span>|
|<span data-ttu-id="51025-723">VendRequestCompanyType</span><span class="sxs-lookup"><span data-stu-id="51025-723">VendRequestCompanyType</span></span>|
|<span data-ttu-id="51025-724">VendRequestOriginatedByType</span><span class="sxs-lookup"><span data-stu-id="51025-724">VendRequestOriginatedByType</span></span>|
|<span data-ttu-id="51025-725">VendRequestQuestionnairesCompleted</span><span class="sxs-lookup"><span data-stu-id="51025-725">VendRequestQuestionnairesCompleted</span></span>|
|<span data-ttu-id="51025-726">VendRequestRoleType</span><span class="sxs-lookup"><span data-stu-id="51025-726">VendRequestRoleType</span></span>|
|<span data-ttu-id="51025-727">VendReviewRatingScore</span><span class="sxs-lookup"><span data-stu-id="51025-727">VendReviewRatingScore</span></span>|
|<span data-ttu-id="51025-728">VersioningAction</span><span class="sxs-lookup"><span data-stu-id="51025-728">VersioningAction</span></span>|
|<span data-ttu-id="51025-729">WHSAllowMaterialOverPick</span><span class="sxs-lookup"><span data-stu-id="51025-729">WHSAllowMaterialOverPick</span></span>|
|<span data-ttu-id="51025-730">WHSApplicableDemand</span><span class="sxs-lookup"><span data-stu-id="51025-730">WHSApplicableDemand</span></span>|
|<span data-ttu-id="51025-731">WHSAutoReleaseContainerAtContainerClose</span><span class="sxs-lookup"><span data-stu-id="51025-731">WHSAutoReleaseContainerAtContainerClose</span></span>|
|<span data-ttu-id="51025-732">WHSAutoReleaseOrderType</span><span class="sxs-lookup"><span data-stu-id="51025-732">WHSAutoReleaseOrderType</span></span>|
|<span data-ttu-id="51025-733">WHSBreakCluster</span><span class="sxs-lookup"><span data-stu-id="51025-733">WHSBreakCluster</span></span>|
|<span data-ttu-id="51025-734">WHSContainerizationQueryType</span><span class="sxs-lookup"><span data-stu-id="51025-734">WHSContainerizationQueryType</span></span>|
|<span data-ttu-id="51025-735">WHSContainerPackingStrategy</span><span class="sxs-lookup"><span data-stu-id="51025-735">WHSContainerPackingStrategy</span></span>|
|<span data-ttu-id="51025-736">WHSContainerTableFormViewType</span><span class="sxs-lookup"><span data-stu-id="51025-736">WHSContainerTableFormViewType</span></span>|
|<span data-ttu-id="51025-737">WHSCrossDockFulfillmentStrategy</span><span class="sxs-lookup"><span data-stu-id="51025-737">WHSCrossDockFulfillmentStrategy</span></span>|
|<span data-ttu-id="51025-738">WHSCustJourType</span><span class="sxs-lookup"><span data-stu-id="51025-738">WHSCustJourType</span></span>|
|<span data-ttu-id="51025-739">WHSCycleCountPlanStatus</span><span class="sxs-lookup"><span data-stu-id="51025-739">WHSCycleCountPlanStatus</span></span>|
|<span data-ttu-id="51025-740">WHSDefaultDataField</span><span class="sxs-lookup"><span data-stu-id="51025-740">WHSDefaultDataField</span></span>|
|<span data-ttu-id="51025-741">WHSFilterModule</span><span class="sxs-lookup"><span data-stu-id="51025-741">WHSFilterModule</span></span>|
|<span data-ttu-id="51025-742">WHSHistoryEvent</span><span class="sxs-lookup"><span data-stu-id="51025-742">WHSHistoryEvent</span></span>|
|<span data-ttu-id="51025-743">WHSLoadPlanning</span><span class="sxs-lookup"><span data-stu-id="51025-743">WHSLoadPlanning</span></span>|
|<span data-ttu-id="51025-744">WHSLoadPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="51025-744">WHSLoadPostMethodsBase</span></span>|
|<span data-ttu-id="51025-745">WhsLoadReplenishment</span><span class="sxs-lookup"><span data-stu-id="51025-745">WhsLoadReplenishment</span></span>|
|<span data-ttu-id="51025-746">WHSLoadTable</span><span class="sxs-lookup"><span data-stu-id="51025-746">WHSLoadTable</span></span>|
|<span data-ttu-id="51025-747">WHSLocDirStrategy</span><span class="sxs-lookup"><span data-stu-id="51025-747">WHSLocDirStrategy</span></span>|
|<span data-ttu-id="51025-748">WHSLPAssignment</span><span class="sxs-lookup"><span data-stu-id="51025-748">WHSLPAssignment</span></span>|
|<span data-ttu-id="51025-749">WHSLPWFilterType</span><span class="sxs-lookup"><span data-stu-id="51025-749">WHSLPWFilterType</span></span>|
|<span data-ttu-id="51025-750">WHSManifestAt</span><span class="sxs-lookup"><span data-stu-id="51025-750">WHSManifestAt</span></span>|
|<span data-ttu-id="51025-751">WHSManifestRequirementContainerGroup</span><span class="sxs-lookup"><span data-stu-id="51025-751">WHSManifestRequirementContainerGroup</span></span>|
|<span data-ttu-id="51025-752">WHSMenuItemDirectedBy</span><span class="sxs-lookup"><span data-stu-id="51025-752">WHSMenuItemDirectedBy</span></span>|
|<span data-ttu-id="51025-753">WHSMixedLPReceivingMode</span><span class="sxs-lookup"><span data-stu-id="51025-753">WHSMixedLPReceivingMode</span></span>|
|<span data-ttu-id="51025-754">WHSMixingLogicTables</span><span class="sxs-lookup"><span data-stu-id="51025-754">WHSMixingLogicTables</span></span>|
|<span data-ttu-id="51025-755">WHSMobileAppPagePattern</span><span class="sxs-lookup"><span data-stu-id="51025-755">WHSMobileAppPagePattern</span></span>|
|<span data-ttu-id="51025-756">WHSOriginType</span><span class="sxs-lookup"><span data-stu-id="51025-756">WHSOriginType</span></span>|
|<span data-ttu-id="51025-757">WHSPickOldestBatch</span><span class="sxs-lookup"><span data-stu-id="51025-757">WHSPickOldestBatch</span></span>|
|<span data-ttu-id="51025-758">WHSPostMethodBaseKanban</span><span class="sxs-lookup"><span data-stu-id="51025-758">WHSPostMethodBaseKanban</span></span>|
|<span data-ttu-id="51025-759">WHSPostMethodBaseKanbanOptional</span><span class="sxs-lookup"><span data-stu-id="51025-759">WHSPostMethodBaseKanbanOptional</span></span>|
|<span data-ttu-id="51025-760">WHSPostMethodBaseOptional</span><span class="sxs-lookup"><span data-stu-id="51025-760">WHSPostMethodBaseOptional</span></span>|
|<span data-ttu-id="51025-761">WHSPostMethodBaseProd</span><span class="sxs-lookup"><span data-stu-id="51025-761">WHSPostMethodBaseProd</span></span>|
|<span data-ttu-id="51025-762">WHSPostMethodBaseProdOptional</span><span class="sxs-lookup"><span data-stu-id="51025-762">WHSPostMethodBaseProdOptional</span></span>|
|<span data-ttu-id="51025-763">WHSPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="51025-763">WHSPostMethodsBase</span></span>|
|<span data-ttu-id="51025-764">WHSQtyPct</span><span class="sxs-lookup"><span data-stu-id="51025-764">WHSQtyPct</span></span>|
|<span data-ttu-id="51025-765">WHSReleaseQuantitySpecification</span><span class="sxs-lookup"><span data-stu-id="51025-765">WHSReleaseQuantitySpecification</span></span>|
|<span data-ttu-id="51025-766">WHSReplenishmentDependentWorkBlockingPolicy</span><span class="sxs-lookup"><span data-stu-id="51025-766">WHSReplenishmentDependentWorkBlockingPolicy</span></span>|
|<span data-ttu-id="51025-767">WHSReservationHierarchyLevelStrategyType</span><span class="sxs-lookup"><span data-stu-id="51025-767">WHSReservationHierarchyLevelStrategyType</span></span>|
|<span data-ttu-id="51025-768">WHSReservationStatus</span><span class="sxs-lookup"><span data-stu-id="51025-768">WHSReservationStatus</span></span>|
|<span data-ttu-id="51025-769">WHSUseFixedLocations</span><span class="sxs-lookup"><span data-stu-id="51025-769">WHSUseFixedLocations</span></span>|
|<span data-ttu-id="51025-770">WHSWorkActivity</span><span class="sxs-lookup"><span data-stu-id="51025-770">WHSWorkActivity</span></span>|
|<span data-ttu-id="51025-771">WHSWorkClusterStatus</span><span class="sxs-lookup"><span data-stu-id="51025-771">WHSWorkClusterStatus</span></span>|
|<span data-ttu-id="51025-772">WHSWorkCreationProcess</span><span class="sxs-lookup"><span data-stu-id="51025-772">WHSWorkCreationProcess</span></span>|
|<span data-ttu-id="51025-773">WHSWorkExceptionLogStatus</span><span class="sxs-lookup"><span data-stu-id="51025-773">WHSWorkExceptionLogStatus</span></span>|
|<span data-ttu-id="51025-774">WHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="51025-774">WHSWorkExecuteMode</span></span>|
|<span data-ttu-id="51025-775">WHSWorkListPageFilter</span><span class="sxs-lookup"><span data-stu-id="51025-775">WHSWorkListPageFilter</span></span>|
|<span data-ttu-id="51025-776">WHSWorkPrintOption</span><span class="sxs-lookup"><span data-stu-id="51025-776">WHSWorkPrintOption</span></span>|
|<span data-ttu-id="51025-777">WHSWorkPutFlow</span><span class="sxs-lookup"><span data-stu-id="51025-777">WHSWorkPutFlow</span></span>|
|<span data-ttu-id="51025-778">WHSWorkTransType</span><span class="sxs-lookup"><span data-stu-id="51025-778">WHSWorkTransType</span></span>|
|<span data-ttu-id="51025-779">WHSWorkType</span><span class="sxs-lookup"><span data-stu-id="51025-779">WHSWorkType</span></span>|
|<span data-ttu-id="51025-780">WHSWorkTypePickPut</span><span class="sxs-lookup"><span data-stu-id="51025-780">WHSWorkTypePickPut</span></span>|
|<span data-ttu-id="51025-781">WMSAutoAddStop</span><span class="sxs-lookup"><span data-stu-id="51025-781">WMSAutoAddStop</span></span>|
|<span data-ttu-id="51025-782">WMSFreightChargeTerms</span><span class="sxs-lookup"><span data-stu-id="51025-782">WMSFreightChargeTerms</span></span>|
|<span data-ttu-id="51025-783">WMSFreightCounted</span><span class="sxs-lookup"><span data-stu-id="51025-783">WMSFreightCounted</span></span>|
|<span data-ttu-id="51025-784">WMSHandlingType</span><span class="sxs-lookup"><span data-stu-id="51025-784">WMSHandlingType</span></span>|
|<span data-ttu-id="51025-785">WMSLocationType</span><span class="sxs-lookup"><span data-stu-id="51025-785">WMSLocationType</span></span>|
|<span data-ttu-id="51025-786">WMSPackageType</span><span class="sxs-lookup"><span data-stu-id="51025-786">WMSPackageType</span></span>|
|<span data-ttu-id="51025-787">WMSPalletMovementProcessing</span><span class="sxs-lookup"><span data-stu-id="51025-787">WMSPalletMovementProcessing</span></span>|
|<span data-ttu-id="51025-788">WMSPhysicalUpdateStatus</span><span class="sxs-lookup"><span data-stu-id="51025-788">WMSPhysicalUpdateStatus</span></span>|
|<span data-ttu-id="51025-789">WMSReceiptStatus</span><span class="sxs-lookup"><span data-stu-id="51025-789">WMSReceiptStatus</span></span>|
|<span data-ttu-id="51025-790">WMSReservationMethod</span><span class="sxs-lookup"><span data-stu-id="51025-790">WMSReservationMethod</span></span>|
|<span data-ttu-id="51025-791">WMSReservationMethodInternal</span><span class="sxs-lookup"><span data-stu-id="51025-791">WMSReservationMethodInternal</span></span>|
|<span data-ttu-id="51025-792">WMSShipmentStatus</span><span class="sxs-lookup"><span data-stu-id="51025-792">WMSShipmentStatus</span></span>|
|<span data-ttu-id="51025-793">WMSShipmentType</span><span class="sxs-lookup"><span data-stu-id="51025-793">WMSShipmentType</span></span>|
|<span data-ttu-id="51025-794">WMSSpaceUtilInconsistencyGroup</span><span class="sxs-lookup"><span data-stu-id="51025-794">WMSSpaceUtilInconsistencyGroup</span></span>|
|<span data-ttu-id="51025-795">WMSSpaceUtilShowBy</span><span class="sxs-lookup"><span data-stu-id="51025-795">WMSSpaceUtilShowBy</span></span>|
|<span data-ttu-id="51025-796">WMSSpaceUtilStorageLoadUnitType</span><span class="sxs-lookup"><span data-stu-id="51025-796">WMSSpaceUtilStorageLoadUnitType</span></span>|
|<span data-ttu-id="51025-797">WMSStoreAreaType</span><span class="sxs-lookup"><span data-stu-id="51025-797">WMSStoreAreaType</span></span>|
|<span data-ttu-id="51025-798">WMSTrailerLoaded</span><span class="sxs-lookup"><span data-stu-id="51025-798">WMSTrailerLoaded</span></span>|
|<span data-ttu-id="51025-799">WrkCtrActivityType</span><span class="sxs-lookup"><span data-stu-id="51025-799">WrkCtrActivityType</span></span>|
|<span data-ttu-id="51025-800">WrkCtrBulkResReqSearchType</span><span class="sxs-lookup"><span data-stu-id="51025-800">WrkCtrBulkResReqSearchType</span></span>|
|<span data-ttu-id="51025-801">WrkCtrCapacityType</span><span class="sxs-lookup"><span data-stu-id="51025-801">WrkCtrCapacityType</span></span>|
|<span data-ttu-id="51025-802">WrkCtrCapRefType</span><span class="sxs-lookup"><span data-stu-id="51025-802">WrkCtrCapRefType</span></span>|
|<span data-ttu-id="51025-803">WrkCtrCommitState</span><span class="sxs-lookup"><span data-stu-id="51025-803">WrkCtrCommitState</span></span>|
|<span data-ttu-id="51025-804">WrkCtrGroupWrkCtr</span><span class="sxs-lookup"><span data-stu-id="51025-804">WrkCtrGroupWrkCtr</span></span>|
|<span data-ttu-id="51025-805">WrkCtrSchedulerCommand</span><span class="sxs-lookup"><span data-stu-id="51025-805">WrkCtrSchedulerCommand</span></span>|
|<span data-ttu-id="51025-806">WrkCtrSchedulerConstraintType</span><span class="sxs-lookup"><span data-stu-id="51025-806">WrkCtrSchedulerConstraintType</span></span>|
|<span data-ttu-id="51025-807">WrkCtrSchedulerLoggerMode</span><span class="sxs-lookup"><span data-stu-id="51025-807">WrkCtrSchedulerLoggerMode</span></span>|
|<span data-ttu-id="51025-808">WrkCtrType</span><span class="sxs-lookup"><span data-stu-id="51025-808">WrkCtrType</span></span>|
|<span data-ttu-id="51025-809">WrkCtrTypeFilter</span><span class="sxs-lookup"><span data-stu-id="51025-809">WrkCtrTypeFilter</span></span>|

<span data-ttu-id="51025-810">以下の列挙型は削除され、拡張可能になりませんでした。</span><span class="sxs-lookup"><span data-stu-id="51025-810">These enumerations were removed, and not made extensible.</span></span>

| <span data-ttu-id="51025-811">削除された列挙型</span><span class="sxs-lookup"><span data-stu-id="51025-811">Enumeration removed</span></span> |
| --------------- |
|<span data-ttu-id="51025-812">BackorderLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="51025-812">BackorderLinesListPageMode</span></span>|
|<span data-ttu-id="51025-813">BackorderPurchLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="51025-813">BackorderPurchLinesListPageMode</span></span> |
|<span data-ttu-id="51025-814">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="51025-814">EcoResProductPerCompanyListPageType</span></span> |
|<span data-ttu-id="51025-815">ReturnTableListPageType</span><span class="sxs-lookup"><span data-stu-id="51025-815">ReturnTableListPageType</span></span> |
|<span data-ttu-id="51025-816">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="51025-816">SMAAgreementTableListPageType</span></span>|

<span data-ttu-id="51025-817">拡張可能な列挙型のサポートを改善するために、Foundation の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="51025-817">Foundation changes were made to improve support for extensible enumerations.</span></span> <span data-ttu-id="51025-818">**IsExtensible** が **はい** に設定されている列挙型については、**SysPlugin** フレームワークが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="51025-818">The **SysPlugin** framework was enabled for enumerations where **IsExtensible** is set to **Yes**.</span></span> <span data-ttu-id="51025-819">列挙型の新しい名前に基づく構文で、ビューが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="51025-819">Views were enabled with new name-based syntax for enumerations.</span></span>

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a><span data-ttu-id="51025-820">DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド</span><span class="sxs-lookup"><span data-stu-id="51025-820">Data manipulation methods that do not raise DataEvents or missing insert, update, delete pre- and post-data events</span></span>

<span data-ttu-id="51025-821">一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="51025-821">As a general practice, you use data methods on tables to raise events that can be used for extending the application.</span></span> <span data-ttu-id="51025-822">コード ベースは、必ずしもこのプラクティスに従っていませんでした。</span><span class="sxs-lookup"><span data-stu-id="51025-822">The code base has not always followed this practice.</span></span> <span data-ttu-id="51025-823">たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="51025-823">For example, the **doInsert**, **doUpdate**, and **doDelete** data methods and certain table implementations did not make a call to **super()** in the data method.</span></span>

<span data-ttu-id="51025-824">タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="51025-824">The **insert**, **update**, and **delete** methods on the type classes have been refactored.</span></span> <span data-ttu-id="51025-825">データ メソッドで **super()** が確実に呼び出されるように変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="51025-825">Changes were made so that **super()** is called more consistently in data methods.</span></span> <span data-ttu-id="51025-826">これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="51025-826">These changes enable extensions to be added to these methods, so that pre- and post-events are now available for extension.</span></span> <span data-ttu-id="51025-827">次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="51025-827">The tables where the **insert**, **update**, and **delete** events were enabled for extension are listed in the following table.</span></span>

| <span data-ttu-id="51025-828">テーブル</span><span class="sxs-lookup"><span data-stu-id="51025-828">Table</span></span> |
| -------------|
| <span data-ttu-id="51025-829">InventBlocking</span><span class="sxs-lookup"><span data-stu-id="51025-829">InventBlocking</span></span>|
| <span data-ttu-id="51025-830">InventTransferLine</span><span class="sxs-lookup"><span data-stu-id="51025-830">InventTransferLine</span></span>|
| <span data-ttu-id="51025-831">Kanban</span><span class="sxs-lookup"><span data-stu-id="51025-831">Kanban</span></span>|
| <span data-ttu-id="51025-832">KanbanJob</span><span class="sxs-lookup"><span data-stu-id="51025-832">KanbanJob</span></span>|
| <span data-ttu-id="51025-833">KanbanJobPickingList</span><span class="sxs-lookup"><span data-stu-id="51025-833">KanbanJobPickingList</span></span>|
| <span data-ttu-id="51025-834">MCRRoyaltyVendTable</span><span class="sxs-lookup"><span data-stu-id="51025-834">MCRRoyaltyVendTable</span></span>|
| <span data-ttu-id="51025-835">PdsRebateTable</span><span class="sxs-lookup"><span data-stu-id="51025-835">PdsRebateTable</span></span>|
| <span data-ttu-id="51025-836">PmfProdCoBy</span><span class="sxs-lookup"><span data-stu-id="51025-836">PmfProdCoBy</span></span>|
| <span data-ttu-id="51025-837">ProdBOM</span><span class="sxs-lookup"><span data-stu-id="51025-837">ProdBOM</span></span>|
| <span data-ttu-id="51025-838">ProdRoute</span><span class="sxs-lookup"><span data-stu-id="51025-838">ProdRoute</span></span>|
| <span data-ttu-id="51025-839">ProdTable</span><span class="sxs-lookup"><span data-stu-id="51025-839">ProdTable</span></span>|
| <span data-ttu-id="51025-840">PurchLine</span><span class="sxs-lookup"><span data-stu-id="51025-840">PurchLine</span></span>|
| <span data-ttu-id="51025-841">PurchRFQCaseLine</span><span class="sxs-lookup"><span data-stu-id="51025-841">PurchRFQCaseLine</span></span>|
| <span data-ttu-id="51025-842">PurchRFQCaseTable</span><span class="sxs-lookup"><span data-stu-id="51025-842">PurchRFQCaseTable</span></span>|
| <span data-ttu-id="51025-843">PurchRFQLine</span><span class="sxs-lookup"><span data-stu-id="51025-843">PurchRFQLine</span></span>|
| <span data-ttu-id="51025-844">PurchTable</span><span class="sxs-lookup"><span data-stu-id="51025-844">PurchTable</span></span>|
| <span data-ttu-id="51025-845">SalesLine</span><span class="sxs-lookup"><span data-stu-id="51025-845">SalesLine</span></span>|
| <span data-ttu-id="51025-846">SalesQuotationLine</span><span class="sxs-lookup"><span data-stu-id="51025-846">SalesQuotationLine</span></span>|
| <span data-ttu-id="51025-847">SalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="51025-847">SalesQuotationTable</span></span>|
| <span data-ttu-id="51025-848">SalesTable</span><span class="sxs-lookup"><span data-stu-id="51025-848">SalesTable</span></span>|
| <span data-ttu-id="51025-849">TAMVendRebateTable</span><span class="sxs-lookup"><span data-stu-id="51025-849">TAMVendRebateTable</span></span>|
| <span data-ttu-id="51025-850">WMSOrder</span><span class="sxs-lookup"><span data-stu-id="51025-850">WMSOrder</span></span>|
| <span data-ttu-id="51025-851">WMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="51025-851">WMSOrderTrans</span></span>|

## <a name="exposing-class-members"></a><span data-ttu-id="51025-852">クラス メンバーの公開</span><span class="sxs-lookup"><span data-stu-id="51025-852">Exposing class members</span></span>

<span data-ttu-id="51025-853">アクセス修飾子または新しい parm メソッドの変更の結果、追加のプライベート メンバーをカスタマイズに使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="51025-853">Additional private members are now available for customization as a result of the changes to the access modifier or new parm methods.</span></span> <span data-ttu-id="51025-854">コマンド チェーン プラットフォーム機能により、保護されたメソッドとメンバーへの拡張クラスのアクセスが有効になります。</span><span class="sxs-lookup"><span data-stu-id="51025-854">The chain of command platform feature enables extension class access to protected methods and members.</span></span> <span data-ttu-id="51025-855">コマンド チェーンの詳細については、「[拡張可能な X++: コマンド チェーン](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extensible-x-chain-of-command)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="51025-855">For more information about chain of command, see [Extensible X++: Chain of Command](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extensible-x-chain-of-command).</span></span>

| <span data-ttu-id="51025-856">メンバー</span><span class="sxs-lookup"><span data-stu-id="51025-856">Member</span></span> |
| -------------|
|<span data-ttu-id="51025-857">AssetPost.ledgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="51025-857">AssetPost.ledgerJournalTrans</span></span>|
|<span data-ttu-id="51025-858">クラス DimensionDerivationRule.ledgerDimensionAllocationList</span><span class="sxs-lookup"><span data-stu-id="51025-858">Class DimensionDerivationRule.ledgerDimensionAllocationList</span></span>|
|<span data-ttu-id="51025-859">クラス PurchInvoiceJournalCreate.purchTable</span><span class="sxs-lookup"><span data-stu-id="51025-859">Class PurchInvoiceJournalCreate.purchTable</span></span>|
|<span data-ttu-id="51025-860">クラス PurchTableType.purchTable</span><span class="sxs-lookup"><span data-stu-id="51025-860">Class PurchTableType.purchTable</span></span>|
|<span data-ttu-id="51025-861">クラス SalesInvoiceJournalPost.salesLine</span><span class="sxs-lookup"><span data-stu-id="51025-861">Class SalesInvoiceJournalPost.salesLine</span></span>|
|<span data-ttu-id="51025-862">クラス SalesQuotationLineType</span><span class="sxs-lookup"><span data-stu-id="51025-862">Class SalesQuotationLineType</span></span>|
|<span data-ttu-id="51025-863">クラス SalesQuotationTableType</span><span class="sxs-lookup"><span data-stu-id="51025-863">Class SalesQuotationTableType</span></span>|
|<span data-ttu-id="51025-864">クラス VendorInvoiceLineSourceDocLineItem.purchLine</span><span class="sxs-lookup"><span data-stu-id="51025-864">Class VendorInvoiceLineSourceDocLineItem.purchLine</span></span>|
|<span data-ttu-id="51025-865">CustCreditLimit.balanceTotalsCalculated</span><span class="sxs-lookup"><span data-stu-id="51025-865">CustCreditLimit.balanceTotalsCalculated</span></span>|
|<span data-ttu-id="51025-866">CustCreditLimit_SalesTable.salesTable</span><span class="sxs-lookup"><span data-stu-id="51025-866">CustCreditLimit_SalesTable.salesTable</span></span>|
|<span data-ttu-id="51025-867">フォーム LedgerJournalTransCustPaym.ledgerJournalEngine</span><span class="sxs-lookup"><span data-stu-id="51025-867">Form LedgerJournalTransCustPaym.ledgerJournalEngine</span></span>|
|<span data-ttu-id="51025-868">PurchLineType.purchLine</span><span class="sxs-lookup"><span data-stu-id="51025-868">PurchLineType.purchLine</span></span>|
|<span data-ttu-id="51025-869">PurchLineType.purchLine_orig</span><span class="sxs-lookup"><span data-stu-id="51025-869">PurchLineType.purchLine_orig</span></span>|
|<span data-ttu-id="51025-870">SalesLineType.salesLine</span><span class="sxs-lookup"><span data-stu-id="51025-870">SalesLineType.salesLine</span></span>|
|<span data-ttu-id="51025-871">SalesLineType.salesLine_orig</span><span class="sxs-lookup"><span data-stu-id="51025-871">SalesLineType.salesLine_orig</span></span>|
|<span data-ttu-id="51025-872">SalesTableType.checkSalesQty</span><span class="sxs-lookup"><span data-stu-id="51025-872">SalesTableType.checkSalesQty</span></span>|
|<span data-ttu-id="51025-873">SalesTableType.SalesTable_orig</span><span class="sxs-lookup"><span data-stu-id="51025-873">SalesTableType.SalesTable_orig</span></span>|
|<span data-ttu-id="51025-874">WHSControl.data</span><span class="sxs-lookup"><span data-stu-id="51025-874">WHSControl.data</span></span>|
|<span data-ttu-id="51025-875">WHSLocationDirective.targetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="51025-875">WHSLocationDirective.targetLicensePlateId</span></span>|

## <a name="construct-methods-with-throw-statements"></a><span data-ttu-id="51025-876">throw ステートメントを使用した construct メソッド</span><span class="sxs-lookup"><span data-stu-id="51025-876">Construct methods with throw statements</span></span>

<span data-ttu-id="51025-877">特定の型の実装が欠落していた場合、いくつかの **construct** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="51025-877">Some **construct** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="51025-878">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**construct** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="51025-878">This doesn't work well with extensibility, so to mitigate this, **construct** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="51025-879">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="51025-879">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="51025-880">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="51025-880">Object</span></span> |
| -------------|
|<span data-ttu-id="51025-881">BarcodeEAN128.string()</span><span class="sxs-lookup"><span data-stu-id="51025-881">BarcodeEAN128.string()</span></span>|
|<span data-ttu-id="51025-882">CustCreditLimit.Construct</span><span class="sxs-lookup"><span data-stu-id="51025-882">CustCreditLimit.Construct</span></span>|
|<span data-ttu-id="51025-883">FormLetterReport</span><span class="sxs-lookup"><span data-stu-id="51025-883">FormLetterReport</span></span>|
|<span data-ttu-id="51025-884">JournalStatic</span><span class="sxs-lookup"><span data-stu-id="51025-884">JournalStatic</span></span>|
|<span data-ttu-id="51025-885">MarkupAllocation</span><span class="sxs-lookup"><span data-stu-id="51025-885">MarkupAllocation</span></span>|
|<span data-ttu-id="51025-886">PurchTable2LineField</span><span class="sxs-lookup"><span data-stu-id="51025-886">PurchTable2LineField</span></span>|
|<span data-ttu-id="51025-887">SalesCalcTax</span><span class="sxs-lookup"><span data-stu-id="51025-887">SalesCalcTax</span></span>|
|<span data-ttu-id="51025-888">SalesEditLinesForm</span><span class="sxs-lookup"><span data-stu-id="51025-888">SalesEditLinesForm</span></span>|
|<span data-ttu-id="51025-889">SalesFormLetter</span><span class="sxs-lookup"><span data-stu-id="51025-889">SalesFormLetter</span></span>|
|<span data-ttu-id="51025-890">SalesFormLetterContract.newFromPackedVersion</span><span class="sxs-lookup"><span data-stu-id="51025-890">SalesFormLetterContract.newFromPackedVersion</span></span>|
|<span data-ttu-id="51025-891">SalesFormletterParmData.newData</span><span class="sxs-lookup"><span data-stu-id="51025-891">SalesFormletterParmData.newData</span></span>|
|<span data-ttu-id="51025-892">SalesQuantity</span><span class="sxs-lookup"><span data-stu-id="51025-892">SalesQuantity</span></span>|
|<span data-ttu-id="51025-893">SalesQuotationEditLinesForm.construct</span><span class="sxs-lookup"><span data-stu-id="51025-893">SalesQuotationEditLinesForm.construct</span></span>|
|<span data-ttu-id="51025-894">SalesSummaryFields</span><span class="sxs-lookup"><span data-stu-id="51025-894">SalesSummaryFields</span></span>|
|<span data-ttu-id="51025-895">SalesTable2LineField</span><span class="sxs-lookup"><span data-stu-id="51025-895">SalesTable2LineField</span></span>|
|<span data-ttu-id="51025-896">VendInvoiceTableToLineUpdate</span><span class="sxs-lookup"><span data-stu-id="51025-896">VendInvoiceTableToLineUpdate</span></span>|

## <a name="find-methods-with-throw-statements"></a><span data-ttu-id="51025-897">throw ステートメントを使用した find メソッド</span><span class="sxs-lookup"><span data-stu-id="51025-897">Find methods with throw statements</span></span>

<span data-ttu-id="51025-898">特定の型の実装が欠落していた場合、いくつかの **find** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="51025-898">Some **find** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="51025-899">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**find** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="51025-899">This does not work well with extensibility, so to mitigate this, **find** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="51025-900">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="51025-900">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="51025-901">メソッド</span><span class="sxs-lookup"><span data-stu-id="51025-901">Methods</span></span> |
| -------------|
|<span data-ttu-id="51025-902">JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="51025-902">JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="51025-903">JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="51025-903">JournalStatic.findJournalTableId</span></span>|

## <a name="methods-made-hookable"></a><span data-ttu-id="51025-904">フック可能なメソッド</span><span class="sxs-lookup"><span data-stu-id="51025-904">Methods made hookable</span></span>

<span data-ttu-id="51025-905">パブリックでない一部のメソッドおよびフック可能でない一部のメソッドについて、拡張性サポートが強化されました。</span><span class="sxs-lookup"><span data-stu-id="51025-905">Extensibility support has been extended for some methods that were not public and were not hookable.</span></span> <span data-ttu-id="51025-906">以下のメソッドはフック可能な動作で明示的に修飾されています。</span><span class="sxs-lookup"><span data-stu-id="51025-906">The following methods have been explicitly decorated with hookable behavior.</span></span>

| <span data-ttu-id="51025-907">メソッド</span><span class="sxs-lookup"><span data-stu-id="51025-907">Method</span></span> |
| -------------|
|<span data-ttu-id="51025-908">クラス CustVendReversePosting.updateCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="51025-908">Class CustVendReversePosting.updateCustVendTrans</span></span>|
|<span data-ttu-id="51025-909">クラス JournalTableData.construct</span><span class="sxs-lookup"><span data-stu-id="51025-909">Class JournalTableData.construct</span></span>|
|<span data-ttu-id="51025-910">クラス PriceDisc.makeKey</span><span class="sxs-lookup"><span data-stu-id="51025-910">Class PriceDisc.makeKey</span></span>|
|<span data-ttu-id="51025-911">クラス PurchInvoiceJournalCreate.initJournalHeader</span><span class="sxs-lookup"><span data-stu-id="51025-911">Class PurchInvoiceJournalCreate.initJournalHeader</span></span>|
|<span data-ttu-id="51025-912">クラス SalesInvoiceJournalPost.checkSourceLine</span><span class="sxs-lookup"><span data-stu-id="51025-912">Class SalesInvoiceJournalPost.checkSourceLine</span></span>|
|<span data-ttu-id="51025-913">クラス SalesInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="51025-913">Class SalesInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="51025-914">フォーム LedgerTransVoucher.addDynaLink</span><span class="sxs-lookup"><span data-stu-id="51025-914">Form LedgerTransVoucher.addDynaLink</span></span>|
|<span data-ttu-id="51025-915">ReqCalc.deleteItemRequirement</span><span class="sxs-lookup"><span data-stu-id="51025-915">ReqCalc.deleteItemRequirement</span></span>|
|<span data-ttu-id="51025-916">ReqCalc.initTransFromInventTrans</span><span class="sxs-lookup"><span data-stu-id="51025-916">ReqCalc.initTransFromInventTrans</span></span>|
|<span data-ttu-id="51025-917">ReqCalcForecastItemTable.deleteRequirement</span><span class="sxs-lookup"><span data-stu-id="51025-917">ReqCalcForecastItemTable.deleteRequirement</span></span>|
|<span data-ttu-id="51025-918">テーブル TmpCustVendTrans.createLineCreditLimit</span><span class="sxs-lookup"><span data-stu-id="51025-918">Table TmpCustVendTrans.createLineCreditLimit</span></span>|
|<span data-ttu-id="51025-919">テーブル TmpCustVendTrans.createLineCreditRemain</span><span class="sxs-lookup"><span data-stu-id="51025-919">Table TmpCustVendTrans.createLineCreditRemain</span></span>|
|<span data-ttu-id="51025-920">テーブル TmpCustVendTrans.createLineOrdered</span><span class="sxs-lookup"><span data-stu-id="51025-920">Table TmpCustVendTrans.createLineOrdered</span></span>|
|<span data-ttu-id="51025-921">テーブル TmpCustVendTrans.createLinePackingSlip</span><span class="sxs-lookup"><span data-stu-id="51025-921">Table TmpCustVendTrans.createLinePackingSlip</span></span>|
|<span data-ttu-id="51025-922">WHSLocationDirective.addRangeByTransType</span><span class="sxs-lookup"><span data-stu-id="51025-922">WHSLocationDirective.addRangeByTransType</span></span>|
|<span data-ttu-id="51025-923">WhsWorkCreate.createWorkLine</span><span class="sxs-lookup"><span data-stu-id="51025-923">WhsWorkCreate.createWorkLine</span></span>|

## <a name="inline-delegates"></a><span data-ttu-id="51025-924">インライン デリゲート</span><span class="sxs-lookup"><span data-stu-id="51025-924">Inline delegates</span></span>

<span data-ttu-id="51025-925">インライン デリゲートを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="51025-925">Inline delegates are now available.</span></span> <span data-ttu-id="51025-926">インライン デリゲートの最も一般的な使用方法は、メソッドをより粒度の細かいメソッドに分割して、より小規模なメソッドで拡張イベントを使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="51025-926">The most common way to use inline delegates is to split the method into more granular methods and enable extensibility events in the smaller methods.</span></span>

|  <span data-ttu-id="51025-927">メソッド</span><span class="sxs-lookup"><span data-stu-id="51025-927">Method</span></span> |
| -------------|
|<span data-ttu-id="51025-928">AxClass - ChequeDP - Method - insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="51025-928">AxClass - ChequeDP - Method - insertChequeTmp</span></span>|
|<span data-ttu-id="51025-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="51025-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span></span>|
|<span data-ttu-id="51025-930">クラス JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="51025-930">class JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="51025-931">クラス JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="51025-931">class JournalStatic.findJournalTableId</span></span>|
|<span data-ttu-id="51025-932">クラス WhsLocationDirective.findLocationMultiSKU</span><span class="sxs-lookup"><span data-stu-id="51025-932">Class WhsLocationDirective.findLocationMultiSKU</span></span>|
|<span data-ttu-id="51025-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span><span class="sxs-lookup"><span data-stu-id="51025-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span></span>|
|<span data-ttu-id="51025-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span><span class="sxs-lookup"><span data-stu-id="51025-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span></span>|
|<span data-ttu-id="51025-935">フォーム SalesTable - メソッド updateDesign</span><span class="sxs-lookup"><span data-stu-id="51025-935">Form SalesTable - method updateDesign</span></span>|
|<span data-ttu-id="51025-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span><span class="sxs-lookup"><span data-stu-id="51025-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span></span>|
|<span data-ttu-id="51025-937">SalesLineType.insert</span><span class="sxs-lookup"><span data-stu-id="51025-937">SalesLineType.insert</span></span>|
|<span data-ttu-id="51025-938">SalesLineType.update</span><span class="sxs-lookup"><span data-stu-id="51025-938">SalesLineType.update</span></span>|
|<span data-ttu-id="51025-939">SalesTable2LineUpdatePrompt.dialog</span><span class="sxs-lookup"><span data-stu-id="51025-939">SalesTable2LineUpdatePrompt.dialog</span></span>|
|<span data-ttu-id="51025-940">テーブル ExtCodeTable</span><span class="sxs-lookup"><span data-stu-id="51025-940">table ExtCodeTable</span></span>|
|<span data-ttu-id="51025-941">テーブル InventItemGroup.getGroupForAccountType</span><span class="sxs-lookup"><span data-stu-id="51025-941">table InventItemGroup.getGroupForAccountType</span></span>|
|<span data-ttu-id="51025-942">テーブル InventItemGroup.ledgerDimensionDescription</span><span class="sxs-lookup"><span data-stu-id="51025-942">table InventItemGroup.ledgerDimensionDescription</span></span>|
|<span data-ttu-id="51025-943">テーブル InventTestAssociationTable</span><span class="sxs-lookup"><span data-stu-id="51025-943">table InventTestAssociationTable</span></span>|
|<span data-ttu-id="51025-944">テーブル LedgerJournalName - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="51025-944">Table LedgerJournalName - method validateWrite</span></span>|
|<span data-ttu-id="51025-945">テーブル PaymTerm - メソッド due</span><span class="sxs-lookup"><span data-stu-id="51025-945">Table PaymTerm - method due</span></span>|
|<span data-ttu-id="51025-946">TaxCalculation.newForSourceType</span><span class="sxs-lookup"><span data-stu-id="51025-946">TaxCalculation.newForSourceType</span></span>|
|<span data-ttu-id="51025-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span><span class="sxs-lookup"><span data-stu-id="51025-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span></span>|
|<span data-ttu-id="51025-948">WHSLoadLine.getOrderCommonFromLoadLine</span><span class="sxs-lookup"><span data-stu-id="51025-948">WHSLoadLine.getOrderCommonFromLoadLine</span></span>|
|<span data-ttu-id="51025-949">WhsLocationDirective.findLocation</span><span class="sxs-lookup"><span data-stu-id="51025-949">WhsLocationDirective.findLocation</span></span>|
|<span data-ttu-id="51025-950">WHSRFControlData.populateData</span><span class="sxs-lookup"><span data-stu-id="51025-950">WHSRFControlData.populateData</span></span>|
|<span data-ttu-id="51025-951">WHSRFControLData.processControl</span><span class="sxs-lookup"><span data-stu-id="51025-951">WHSRFControLData.processControl</span></span>|
|<span data-ttu-id="51025-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="51025-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span></span>|

## <a name="other-changes"></a><span data-ttu-id="51025-953">その他の変更</span><span class="sxs-lookup"><span data-stu-id="51025-953">Other changes</span></span>

<span data-ttu-id="51025-954">次の表に、拡張機能に対して行われた追加の変更を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="51025-954">The following table lists additional changes that have been made for extensibility.</span></span>


|                                                           <span data-ttu-id="51025-955">変更</span><span class="sxs-lookup"><span data-stu-id="51025-955">Change</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------------------|
|                                      <span data-ttu-id="51025-956">既存の製品分析コードの間接参照の追加</span><span class="sxs-lookup"><span data-stu-id="51025-956">Add indirection for existing product dimensions</span></span>                                       |
|                                  <span data-ttu-id="51025-957">クラス FormLetterParmDataOutputContract は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="51025-957">Class FormLetterParmDataOutputContract is not extensible</span></span>                                  |
|             <span data-ttu-id="51025-958">1 つ以上の引数をサポートする SysExtensionFramework のインスタンス化戦略の作成</span><span class="sxs-lookup"><span data-stu-id="51025-958">Create an instantiation strategy for the SysExtensionFramework that supports one or more arguments</span></span>             |
|                      <span data-ttu-id="51025-959">カスタマイズ: TableField: 拡張モデル: テーブル フィールドの EDT タイプの変更</span><span class="sxs-lookup"><span data-stu-id="51025-959">Customization: TableField: Extension Model: Change EDT type of on a table field</span></span>                       |
|                          <span data-ttu-id="51025-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="51025-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch statement</span></span>                           |
|                                     <span data-ttu-id="51025-961">CustVendOpenTransBalances - new() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="51025-961">CustVendOpenTransBalances - new() switch statement</span></span>                                     |
|                                  <span data-ttu-id="51025-962">CustVendOutPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="51025-962">CustVendOutPaym (Class) needs extensibility improvement</span></span>                                   |
|                        <span data-ttu-id="51025-963">CustVendPaymReconciliationSetStatus (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="51025-963">CustVendPaymReconciliationSetStatus (Class) needs extensibility improvement</span></span>                         |
|                                 <span data-ttu-id="51025-964">CustVendSumForPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="51025-964">CustVendSumForPaym (Class) needs extensibility improvement</span></span>                                 |
|                               <span data-ttu-id="51025-965">SysGroup からの AddressCountyId と AddressStateId EDT の切り離し</span><span class="sxs-lookup"><span data-stu-id="51025-965">Decouple AddressCountyId and AddressStateId EDTs from SysGroup</span></span>                               |
|                          <span data-ttu-id="51025-966">ドキュメント管理イベントの処理には拡張性サポートの改善が必要</span><span class="sxs-lookup"><span data-stu-id="51025-966">Document Management event handling needs improved extensibility support</span></span>                           |
|            <span data-ttu-id="51025-967">為替レート プロバイダー フレームワークには、通貨モデルにカスタムの組み込みプロバイダーを配置することが必要</span><span class="sxs-lookup"><span data-stu-id="51025-967">Exchange rate provider framework requires custom built providers to be placed in the Currency Model</span></span>             |
|                                                      <span data-ttu-id="51025-968">GS-128 の拡張</span><span class="sxs-lookup"><span data-stu-id="51025-968">Extending GS-128</span></span>                                                      |
|                         <span data-ttu-id="51025-969">拡張モデル: CountryRegionCodes プロパティでのカスタマイズを許可する。</span><span class="sxs-lookup"><span data-stu-id="51025-969">Extension model: Allow customizations on the CountryRegionCodes property.</span></span>                          |
|                  <span data-ttu-id="51025-970">フォーム拡張機能 - 新しいコントロールによって "拡張された" フォーム要素の拡張機能は動作しません</span><span class="sxs-lookup"><span data-stu-id="51025-970">Form extension - Extension of "extended" form elements with new controls are not working</span></span>                  |
|                                              <span data-ttu-id="51025-971">InventDim: throw 付きの条件</span><span class="sxs-lookup"><span data-stu-id="51025-971">InventDim: Condition with throw</span></span>                                               |
|                                                  <span data-ttu-id="51025-972">InventDimRenameDimValue</span><span class="sxs-lookup"><span data-stu-id="51025-972">InventDimRenameDimValue</span></span>                                                   |
|                <span data-ttu-id="51025-973">メソッドのオーバーレイ - クラス VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="51025-973">Method overlayering - Class VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span></span>                |
|                                     <span data-ttu-id="51025-974">メソッドのオーバーレイ: クラス Markup - メソッド delete</span><span class="sxs-lookup"><span data-stu-id="51025-974">Method overlayering: class Markup - method delete</span></span>                                      |
|                       <span data-ttu-id="51025-975">メソッドのオーバーレイ: クラス McrPriceHistoryForm.insertPotentialTradeAgreements</span><span class="sxs-lookup"><span data-stu-id="51025-975">Method overlayering: class McrPriceHistoryForm.insertPotentialTradeAgreements</span></span>                        |
|                             <span data-ttu-id="51025-976">メソッドのオーバーレイ: クラス OffsetVoucher - メソッド markTransaction</span><span class="sxs-lookup"><span data-stu-id="51025-976">Method overlayering: Class OffsetVoucher - method markTransaction</span></span>                              |
|                                 <span data-ttu-id="51025-977">メソッドのオーバーレイ: フォーム LedgerJournalTransDimension.init</span><span class="sxs-lookup"><span data-stu-id="51025-977">Method overlayering: Form LedgerJournalTransDimension.init</span></span>                                 |
|                                 <span data-ttu-id="51025-978">メソッドのオーバーレイ: フォーム LedgerTransVoucher - メソッド init</span><span class="sxs-lookup"><span data-stu-id="51025-978">Method overlayering: Form LedgerTransVoucher - method init</span></span>                                 |
|                             <span data-ttu-id="51025-979">メソッドのオーバーレイ: テーブル CustInvoiceTable - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="51025-979">Method overlayering: Table CustInvoiceTable - method validateWrite</span></span>                             |
|                       <span data-ttu-id="51025-980">メソッド シグネチャが変更されました: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span><span class="sxs-lookup"><span data-stu-id="51025-980">Method signature changed: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span></span>                        |
|                               <span data-ttu-id="51025-981">メソッド シグネチャが変更になりました: WHSInvent.getCommonFromWorkTransType</span><span class="sxs-lookup"><span data-stu-id="51025-981">Method signature changed: WHSInvent.getCommonFromWorkTransType</span></span>                               |
|                                  <span data-ttu-id="51025-982">メソッド シグネチャが変更されました: WHSPoolProdBom.movementBuffer</span><span class="sxs-lookup"><span data-stu-id="51025-982">Method signature changed: WHSPoolProdBom.movementBuffer</span></span>                                   |
|                          <span data-ttu-id="51025-983">construct メソッドがありません: クラス SMAServiceOrderTableButtonStateProvider</span><span class="sxs-lookup"><span data-stu-id="51025-983">Missing construct method: class SMAServiceOrderTableButtonStateProvider</span></span>                           |
|                                         <span data-ttu-id="51025-984">必要な番号順序スコープの拡張性</span><span class="sxs-lookup"><span data-stu-id="51025-984">Number sequence scope extensibility needed</span></span>                                         |
|                           <span data-ttu-id="51025-985">Runbase には、クラスの拡張機能がメンバーをパック/アンパックする方法が必要</span><span class="sxs-lookup"><span data-stu-id="51025-985">Runbase needs a way for class extensions to pack/unpack their members</span></span>                            |
|                                              <span data-ttu-id="51025-986">文字列 EDT のサイズの拡張の問題</span><span class="sxs-lookup"><span data-stu-id="51025-986">String EDT size extension issues</span></span>                                              |
|                              <span data-ttu-id="51025-987">カスタムの InventDim に基づく手持在庫フォームのオープンのサポート</span><span class="sxs-lookup"><span data-stu-id="51025-987">Support opening Inventory on-hand form based on custom InventDim</span></span>                              |
|          <span data-ttu-id="51025-988">SysExtension フレームワーク: SysExtensionIInstantiationStrategy と SysExtensionIAttribute は互換性がありません</span><span class="sxs-lookup"><span data-stu-id="51025-988">SysExtension framework: SysExtensionIInstantiationStrategy and SysExtensionIAttribute are not compatible</span></span>          |
| <span data-ttu-id="51025-989">要求/応答シナリオで使用されるデリゲートがより堅牢になるために、EventHandlerResult のバリエーションが必要</span><span class="sxs-lookup"><span data-stu-id="51025-989">Variations of EventHandlerResult are requested to ensure that delegates used in Request/response scenarios are more robust</span></span> |
|                                                <span data-ttu-id="51025-990">WHS モバイル フレームワーク: 合格</span><span class="sxs-lookup"><span data-stu-id="51025-990">WHS Mobile Framework: passes</span></span>                                                |
|                                     <span data-ttu-id="51025-991">WhsLocationDirectiveLine To/FromQty は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="51025-991">WhsLocationDirectiveLine To/FromQty not extensible</span></span>                                     |
|                                                 <span data-ttu-id="51025-992">WHSMobileApp の拡張性</span><span class="sxs-lookup"><span data-stu-id="51025-992">WHSMobileApp Extensibility</span></span>                                                 |
|         <span data-ttu-id="51025-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="51025-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|         <span data-ttu-id="51025-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="51025-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|            <span data-ttu-id="51025-995">WhsRFControlData.processControl は switch ブロック内の _data ではなく WhsControl.data を参照する必要があります</span><span class="sxs-lookup"><span data-stu-id="51025-995">WhsRFControlData.processControl must reference WhsControl.data instead of _data in the switch block</span></span>             |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]