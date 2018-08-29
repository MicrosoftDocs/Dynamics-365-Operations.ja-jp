---
title: "Finance and Operations, Enterprise Edition (2017 年 7 月) の拡張機能の変更"
description: "これは、(2017 年 7 月) に実装された拡張機能の一覧です。"
author: FrankDahl
manager: AnnBe
ms.date: 11/08/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: d29dda71a2785a35ab12297b5b57695053457291
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="extensibility-changes-in-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="24890-103">Finance and Operations, Enterprise Edition (2017 年 7 月) の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="24890-103">Extensibility changes in Finance and Operations, Enterprise edition (July 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24890-104">これは、Dynamics 365 for Finance and Operations, Enterprise Edition (2017 年 7 月) に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="24890-104">This is a list of extensibility features that were implemented in the Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span> <span data-ttu-id="24890-105">このバージョンは 2017 年 7 月にリリースされ、ビルド番号は 7.2.11792.56024 です。</span><span class="sxs-lookup"><span data-stu-id="24890-105">This version was released in July 2017 and has a build number of 7.2.11792.56024.</span></span> <span data-ttu-id="24890-106">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24890-106">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="soft-sealed-application-models"></a><span data-ttu-id="24890-107">ソフト シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="24890-107">Soft-sealed application models</span></span>

<span data-ttu-id="24890-108">以下のアプリケーション中間層モデルは、今回のリリースでソフト シールされました。</span><span class="sxs-lookup"><span data-stu-id="24890-108">The following application middle-tier models were soft-sealed in this release.</span></span> <span data-ttu-id="24890-109">これらのモデルのオーバーレイ コードは、コンパイル時に警告を生成します。</span><span class="sxs-lookup"><span data-stu-id="24890-109">Overlayered code in these models will generate warnings on compilation.</span></span>

| <span data-ttu-id="24890-110">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="24890-110">Category</span></span>       | <span data-ttu-id="24890-111">モデル</span><span class="sxs-lookup"><span data-stu-id="24890-111">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="24890-112">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="24890-112">Application Frameworks</span></span> | <span data-ttu-id="24890-113">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="24890-113">CaseManagement</span></span> |
| <span data-ttu-id="24890-114">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="24890-114">Application Frameworks</span></span> | <span data-ttu-id="24890-115">Dimensions</span><span class="sxs-lookup"><span data-stu-id="24890-115">Dimensions</span></span> |
| <span data-ttu-id="24890-116">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="24890-116">Application Frameworks</span></span> | <span data-ttu-id="24890-117">Directory</span><span class="sxs-lookup"><span data-stu-id="24890-117">Directory</span></span> |
| <span data-ttu-id="24890-118">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="24890-118">Application Frameworks</span></span> | <span data-ttu-id="24890-119">Organization</span><span class="sxs-lookup"><span data-stu-id="24890-119">Organization</span></span> |
| <span data-ttu-id="24890-120">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="24890-120">Application Frameworks</span></span> | <span data-ttu-id="24890-121">Currency</span><span class="sxs-lookup"><span data-stu-id="24890-121">Currency</span></span>|
| <span data-ttu-id="24890-122">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="24890-122">Application Frameworks</span></span> | <span data-ttu-id="24890-123">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="24890-123">ApplicationCommon</span></span>|
| <span data-ttu-id="24890-124">HCM コア モデル</span><span class="sxs-lookup"><span data-stu-id="24890-124">HCM Core Models</span></span>| <span data-ttu-id="24890-125">3817938</span><span class="sxs-lookup"><span data-stu-id="24890-125">3817938</span></span>
|<span data-ttu-id="24890-126">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-126">Tax Models</span></span> |<span data-ttu-id="24890-127">Tax</span><span class="sxs-lookup"><span data-stu-id="24890-127">Tax</span></span> |
|<span data-ttu-id="24890-128">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-128">Tax Models</span></span> |<span data-ttu-id="24890-129">Tax Books</span><span class="sxs-lookup"><span data-stu-id="24890-129">Tax Books</span></span> |
|<span data-ttu-id="24890-130">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-130">Tax Models</span></span> |<span data-ttu-id="24890-131">Tax Books Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="24890-131">Tax Books Application Suite Integration</span></span> |
|<span data-ttu-id="24890-132">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-132">Tax Models</span></span> |<span data-ttu-id="24890-133">Tax Engine Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="24890-133">Tax Engine Application Suite Integration</span></span> |
|<span data-ttu-id="24890-134">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-134">Tax Models</span></span> |<span data-ttu-id="24890-135">Tax Engine Configuration</span><span class="sxs-lookup"><span data-stu-id="24890-135">Tax Engine Configuration</span></span> |
|<span data-ttu-id="24890-136">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-136">Tax Models</span></span> |<span data-ttu-id="24890-137">Tax Engine Interface</span><span class="sxs-lookup"><span data-stu-id="24890-137">Tax Engine Interface</span></span> |
|<span data-ttu-id="24890-138">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-138">Tax Models</span></span> |<span data-ttu-id="24890-139">Tax Engine Runtime Generation</span><span class="sxs-lookup"><span data-stu-id="24890-139">Tax Engine Runtime Generation</span></span> |
|<span data-ttu-id="24890-140">税モデル</span><span class="sxs-lookup"><span data-stu-id="24890-140">Tax Models</span></span> |<span data-ttu-id="24890-141">TaxEngine</span><span class="sxs-lookup"><span data-stu-id="24890-141">TaxEngine</span></span> |
| <span data-ttu-id="24890-142">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="24890-142">Source Document Models</span></span> |<span data-ttu-id="24890-143">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="24890-143">SourceDocumentation</span></span> |
| <span data-ttu-id="24890-144">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="24890-144">Source Document Models</span></span> |<span data-ttu-id="24890-145">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="24890-145">SourceDocumentationTypes</span></span> |
| <span data-ttu-id="24890-146">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="24890-146">Ledger Models</span></span> |<span data-ttu-id="24890-147">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="24890-147">GeneralLedger</span></span> |
| <span data-ttu-id="24890-148">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="24890-148">Ledger Models</span></span> |<span data-ttu-id="24890-149">Ledger</span><span class="sxs-lookup"><span data-stu-id="24890-149">Ledger</span></span> |
| <span data-ttu-id="24890-150">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="24890-150">Ledger Models</span></span> |<span data-ttu-id="24890-151">Subledger</span><span class="sxs-lookup"><span data-stu-id="24890-151">Subledger</span></span> |
| <span data-ttu-id="24890-152">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="24890-152">Middle Tier SCM Models</span></span> | <span data-ttu-id="24890-153">CostAccounting</span><span class="sxs-lookup"><span data-stu-id="24890-153">CostAccounting</span></span> |
| <span data-ttu-id="24890-154">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="24890-154">Middle Tier SCM Models</span></span> | <span data-ttu-id="24890-155">CostAccountingAX</span><span class="sxs-lookup"><span data-stu-id="24890-155">CostAccountingAX</span></span> |
| <span data-ttu-id="24890-156">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="24890-156">Middle Tier SCM Models</span></span> | <span data-ttu-id="24890-157">SCMControls</span><span class="sxs-lookup"><span data-stu-id="24890-157">SCMControls</span></span> |
| <span data-ttu-id="24890-158">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="24890-158">Middle Tier SCM Models</span></span> | <span data-ttu-id="24890-159">SCMMobile</span><span class="sxs-lookup"><span data-stu-id="24890-159">SCMMobile</span></span> |
| <span data-ttu-id="24890-160">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="24890-160">Middle Tier SCM Models</span></span> | <span data-ttu-id="24890-161">UnitOfMeasure</span><span class="sxs-lookup"><span data-stu-id="24890-161">UnitOfMeasure</span></span> |
| <span data-ttu-id="24890-162">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="24890-162">Middle Tier SCM Models</span></span> | <span data-ttu-id="24890-163">WMSAdvancedMigration</span><span class="sxs-lookup"><span data-stu-id="24890-163">WMSAdvancedMigration</span></span>|
| <span data-ttu-id="24890-164">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="24890-164">Middle Tier SCM Models</span></span> | <span data-ttu-id="24890-165">InventoryDimensionConversion</span><span class="sxs-lookup"><span data-stu-id="24890-165">InventoryDimensionConversion</span></span>|
| <span data-ttu-id="24890-166">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="24890-166">Workspaces</span></span>| <span data-ttu-id="24890-167">ApplicationWorkspaces</span><span class="sxs-lookup"><span data-stu-id="24890-167">ApplicationWorkspaces</span></span> |
| <span data-ttu-id="24890-168">財務</span><span class="sxs-lookup"><span data-stu-id="24890-168">Finance</span></span>| <span data-ttu-id="24890-169">Fiscalbooks</span><span class="sxs-lookup"><span data-stu-id="24890-169">Fiscalbooks</span></span> |
| <span data-ttu-id="24890-170">管理ツール</span><span class="sxs-lookup"><span data-stu-id="24890-170">Management tools</span></span> | <span data-ttu-id="24890-171">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="24890-171">DataUpgrade</span></span> |

## <a name="hard-sealed-application-models"></a><span data-ttu-id="24890-172">ハード シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="24890-172">Hard-sealed application models</span></span>

<span data-ttu-id="24890-173">以下のアプリケーション中間層モデルは、今回のリリースでハード シールされました。</span><span class="sxs-lookup"><span data-stu-id="24890-173">The following application middle-tier models were hard-sealed in this release.</span></span> <span data-ttu-id="24890-174">これらのモデルのオーバーレイ コードは、コンパイル時にエラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="24890-174">Overlayered code in these models will generate errors on compilation.</span></span>

| <span data-ttu-id="24890-175">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="24890-175">Category</span></span>       | <span data-ttu-id="24890-176">モデル</span><span class="sxs-lookup"><span data-stu-id="24890-176">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="24890-177">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="24890-177">Accounts Payable</span></span> | <span data-ttu-id="24890-178">AccountsPayableMobile</span><span class="sxs-lookup"><span data-stu-id="24890-178">AccountsPayableMobile</span></span> |
| <span data-ttu-id="24890-179">財務</span><span class="sxs-lookup"><span data-stu-id="24890-179">Finance</span></span> | <span data-ttu-id="24890-180">FinancialReportingEntityStore</span><span class="sxs-lookup"><span data-stu-id="24890-180">FinancialReportingEntityStore</span></span>|
| <span data-ttu-id="24890-181">ツール</span><span class="sxs-lookup"><span data-stu-id="24890-181">Tools</span></span> | <span data-ttu-id="24890-182">PerformanceTool</span><span class="sxs-lookup"><span data-stu-id="24890-182">PerformanceTool</span></span> |
| <span data-ttu-id="24890-183">経費</span><span class="sxs-lookup"><span data-stu-id="24890-183">Expenses</span></span> | <span data-ttu-id="24890-184">ExpenseMobile</span><span class="sxs-lookup"><span data-stu-id="24890-184">ExpenseMobile</span></span> |
| <span data-ttu-id="24890-185">GER</span><span class="sxs-lookup"><span data-stu-id="24890-185">GER</span></span> | <span data-ttu-id="24890-186">ElectronicReporting</span><span class="sxs-lookup"><span data-stu-id="24890-186">ElectronicReporting</span></span>|
|<span data-ttu-id="24890-187">GER</span><span class="sxs-lookup"><span data-stu-id="24890-187">GER</span></span> | <span data-ttu-id="24890-188">ElectronicReportingCore</span><span class="sxs-lookup"><span data-stu-id="24890-188">ElectronicReportingCore</span></span>|
|<span data-ttu-id="24890-189">GER</span><span class="sxs-lookup"><span data-stu-id="24890-189">GER</span></span> | <span data-ttu-id="24890-190">Electronic Reporting Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="24890-190">Electronic Reporting Application Suite Integration</span></span>|

## <a name="enumerations-that-are-now-extensible"></a><span data-ttu-id="24890-191">拡張可能になった列挙型</span><span class="sxs-lookup"><span data-stu-id="24890-191">Enumerations that are now extensible</span></span>

<span data-ttu-id="24890-192">列挙の拡張をサポートするために以下の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="24890-192">The following changes were made to support extending enumerations:</span></span>
- <span data-ttu-id="24890-193">標準アプリケーションの多くの列挙が拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="24890-193">Many enumerations in the standard application have been made extensible.</span></span> <span data-ttu-id="24890-194">列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="24890-194">An enumeration is made extensible by setting two properties on the enumeration.</span></span> <span data-ttu-id="24890-195">**IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="24890-195">The **IsExtensible** property is set to **Yes**, and the **UseEnumValue** property is set to **No**.</span></span> 
- <span data-ttu-id="24890-196">一部の列挙型は状態を表します。</span><span class="sxs-lookup"><span data-stu-id="24890-196">Some enumerations represent state.</span></span> <span data-ttu-id="24890-197">拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="24890-197">New façade methods have been added to help enable adding enumeration values by extension.</span></span> <span data-ttu-id="24890-198">列挙型を拡張する方法については、「[列挙値の追加](add-enum-value.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24890-198">For information about how to extend an enumeration, see [Add an enum value](add-enum-value.md).</span></span>
- <span data-ttu-id="24890-199">拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。</span><span class="sxs-lookup"><span data-stu-id="24890-199">Some application code that uses enumerations was changed to support extensibility.</span></span> <span data-ttu-id="24890-200">一般的な変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="24890-200">Common changes include:</span></span>
    + <span data-ttu-id="24890-201">ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。</span><span class="sxs-lookup"><span data-stu-id="24890-201">Removing **throw** exception statements in the default case of a switch to allow post-event subscription.</span></span>
    + <span data-ttu-id="24890-202">拡張機能の **SysExtension** サポートの追加。</span><span class="sxs-lookup"><span data-stu-id="24890-202">Adding **SysExtension** support for extension.</span></span>
    + <span data-ttu-id="24890-203">明示的なデリゲートの追加。</span><span class="sxs-lookup"><span data-stu-id="24890-203">Adding explicit delegates.</span></span>


| <span data-ttu-id="24890-204">列挙型</span><span class="sxs-lookup"><span data-stu-id="24890-204">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="24890-205">AgreementState</span><span class="sxs-lookup"><span data-stu-id="24890-205">AgreementState</span></span>|
|<span data-ttu-id="24890-206">AssetAccountType</span><span class="sxs-lookup"><span data-stu-id="24890-206">AssetAccountType</span></span>|
|<span data-ttu-id="24890-207">AssetTransTypeJournal</span><span class="sxs-lookup"><span data-stu-id="24890-207">AssetTransTypeJournal</span></span>|
|<span data-ttu-id="24890-208">BankAccountType</span><span class="sxs-lookup"><span data-stu-id="24890-208">BankAccountType</span></span>|
|<span data-ttu-id="24890-209">BankFormat</span><span class="sxs-lookup"><span data-stu-id="24890-209">BankFormat</span></span>|
|<span data-ttu-id="24890-210">BarcodeContentType</span><span class="sxs-lookup"><span data-stu-id="24890-210">BarcodeContentType</span></span>|
|<span data-ttu-id="24890-211">BarcodeCoverPageEntityType</span><span class="sxs-lookup"><span data-stu-id="24890-211">BarcodeCoverPageEntityType</span></span>|
|<span data-ttu-id="24890-212">BarcodeType</span><span class="sxs-lookup"><span data-stu-id="24890-212">BarcodeType</span></span>|
|<span data-ttu-id="24890-213">BOMCalcCostingVersionUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-213">BOMCalcCostingVersionUpdate</span></span>|
|<span data-ttu-id="24890-214">BOMCalcCostPriceUsed</span><span class="sxs-lookup"><span data-stu-id="24890-214">BOMCalcCostPriceUsed</span></span>|
|<span data-ttu-id="24890-215">BOMCalcSalesPriceUsed</span><span class="sxs-lookup"><span data-stu-id="24890-215">BOMCalcSalesPriceUsed</span></span>|
|<span data-ttu-id="24890-216">BOMCalcType</span><span class="sxs-lookup"><span data-stu-id="24890-216">BOMCalcType</span></span>|
|<span data-ttu-id="24890-217">BOMCheckLevel</span><span class="sxs-lookup"><span data-stu-id="24890-217">BOMCheckLevel</span></span>|
|<span data-ttu-id="24890-218">BOMCopyContext</span><span class="sxs-lookup"><span data-stu-id="24890-218">BOMCopyContext</span></span>|
|<span data-ttu-id="24890-219">BOMCopyMethod</span><span class="sxs-lookup"><span data-stu-id="24890-219">BOMCopyMethod</span></span>|
|<span data-ttu-id="24890-220">BOMCopyType</span><span class="sxs-lookup"><span data-stu-id="24890-220">BOMCopyType</span></span>|
|<span data-ttu-id="24890-221">BOMCostCalculationMethod</span><span class="sxs-lookup"><span data-stu-id="24890-221">BOMCostCalculationMethod</span></span>|
|<span data-ttu-id="24890-222">BOMExplode</span><span class="sxs-lookup"><span data-stu-id="24890-222">BOMExplode</span></span>|
|<span data-ttu-id="24890-223">BOMRouteCopyDataType</span><span class="sxs-lookup"><span data-stu-id="24890-223">BOMRouteCopyDataType</span></span>|
|<span data-ttu-id="24890-224">BOMVersionFilter</span><span class="sxs-lookup"><span data-stu-id="24890-224">BOMVersionFilter</span></span>|
|<span data-ttu-id="24890-225">BudgetReservation_BusinessEvent_PSN</span><span class="sxs-lookup"><span data-stu-id="24890-225">BudgetReservation_BusinessEvent_PSN</span></span>|
|<span data-ttu-id="24890-226">BudgetReservation_SourceDocument_PSN</span><span class="sxs-lookup"><span data-stu-id="24890-226">BudgetReservation_SourceDocument_PSN</span></span>|
|<span data-ttu-id="24890-227">BudgetReservation_SourceDocumentLine_PSN</span><span class="sxs-lookup"><span data-stu-id="24890-227">BudgetReservation_SourceDocumentLine_PSN</span></span>|
|<span data-ttu-id="24890-228">CatCallMethod</span><span class="sxs-lookup"><span data-stu-id="24890-228">CatCallMethod</span></span>|
|<span data-ttu-id="24890-229">CatContentType</span><span class="sxs-lookup"><span data-stu-id="24890-229">CatContentType</span></span>|
|<span data-ttu-id="24890-230">CatImportStatus</span><span class="sxs-lookup"><span data-stu-id="24890-230">CatImportStatus</span></span>|
|<span data-ttu-id="24890-231">CatMaintenanceRequestWfStatus</span><span class="sxs-lookup"><span data-stu-id="24890-231">CatMaintenanceRequestWfStatus</span></span>|
|<span data-ttu-id="24890-232">CatProcurementErrorCode</span><span class="sxs-lookup"><span data-stu-id="24890-232">CatProcurementErrorCode</span></span>|
|<span data-ttu-id="24890-233">CatPurchaseStatus</span><span class="sxs-lookup"><span data-stu-id="24890-233">CatPurchaseStatus</span></span>|
|<span data-ttu-id="24890-234">CatUserReviewApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="24890-234">CatUserReviewApprovalStatus</span></span>|
|<span data-ttu-id="24890-235">CatVendorCatalogFileUploadType</span><span class="sxs-lookup"><span data-stu-id="24890-235">CatVendorCatalogFileUploadType</span></span>|
|<span data-ttu-id="24890-236">CatVendorCatalogTemplateCategory</span><span class="sxs-lookup"><span data-stu-id="24890-236">CatVendorCatalogTemplateCategory</span></span>|
|<span data-ttu-id="24890-237">CatVendorCategoryHierarchyType</span><span class="sxs-lookup"><span data-stu-id="24890-237">CatVendorCategoryHierarchyType</span></span>|
|<span data-ttu-id="24890-238">CatVendorConfigurationForImport</span><span class="sxs-lookup"><span data-stu-id="24890-238">CatVendorConfigurationForImport</span></span>|
|<span data-ttu-id="24890-239">CatVendorLegalEntityStatus</span><span class="sxs-lookup"><span data-stu-id="24890-239">CatVendorLegalEntityStatus</span></span>|
|<span data-ttu-id="24890-240">CatVendorSiteType</span><span class="sxs-lookup"><span data-stu-id="24890-240">CatVendorSiteType</span></span>|
|<span data-ttu-id="24890-241">ConsignmentReplenishmentOrderLineStatus</span><span class="sxs-lookup"><span data-stu-id="24890-241">ConsignmentReplenishmentOrderLineStatus</span></span>|
|<span data-ttu-id="24890-242">ConsignmentReplenishmentOrderStatus</span><span class="sxs-lookup"><span data-stu-id="24890-242">ConsignmentReplenishmentOrderStatus</span></span>|
|<span data-ttu-id="24890-243">CostBreakdown</span><span class="sxs-lookup"><span data-stu-id="24890-243">CostBreakdown</span></span>|
|<span data-ttu-id="24890-244">CostCalculationCompareProductType</span><span class="sxs-lookup"><span data-stu-id="24890-244">CostCalculationCompareProductType</span></span>|
|<span data-ttu-id="24890-245">CostCalculationRole</span><span class="sxs-lookup"><span data-stu-id="24890-245">CostCalculationRole</span></span>|
|<span data-ttu-id="24890-246">CostCalculationState</span><span class="sxs-lookup"><span data-stu-id="24890-246">CostCalculationState</span></span>|
|<span data-ttu-id="24890-247">CostCalculationSurchargeSubtype</span><span class="sxs-lookup"><span data-stu-id="24890-247">CostCalculationSurchargeSubtype</span></span>|
|<span data-ttu-id="24890-248">CostingActivationType</span><span class="sxs-lookup"><span data-stu-id="24890-248">CostingActivationType</span></span>|
|<span data-ttu-id="24890-249">CostingVersionCompareTo</span><span class="sxs-lookup"><span data-stu-id="24890-249">CostingVersionCompareTo</span></span>|
|<span data-ttu-id="24890-250">CostingVersionPriceType</span><span class="sxs-lookup"><span data-stu-id="24890-250">CostingVersionPriceType</span></span>|
|<span data-ttu-id="24890-251">CostPriceBase</span><span class="sxs-lookup"><span data-stu-id="24890-251">CostPriceBase</span></span>|
|<span data-ttu-id="24890-252">CostProfitSet</span><span class="sxs-lookup"><span data-stu-id="24890-252">CostProfitSet</span></span>|
|<span data-ttu-id="24890-253">CostSalesPriceDisplay</span><span class="sxs-lookup"><span data-stu-id="24890-253">CostSalesPriceDisplay</span></span>|
|<span data-ttu-id="24890-254">CostSheetNodeListType</span><span class="sxs-lookup"><span data-stu-id="24890-254">CostSheetNodeListType</span></span>|
|<span data-ttu-id="24890-255">CostSheetPanelView</span><span class="sxs-lookup"><span data-stu-id="24890-255">CostSheetPanelView</span></span>|
|<span data-ttu-id="24890-256">CostSheetProdFlowMode</span><span class="sxs-lookup"><span data-stu-id="24890-256">CostSheetProdFlowMode</span></span>|
|<span data-ttu-id="24890-257">CostStatementCacheAggregationAfter</span><span class="sxs-lookup"><span data-stu-id="24890-257">CostStatementCacheAggregationAfter</span></span>|
|<span data-ttu-id="24890-258">CostWIPStatementCategory</span><span class="sxs-lookup"><span data-stu-id="24890-258">CostWIPStatementCategory</span></span>|
|<span data-ttu-id="24890-259">CustPaymentValidate</span><span class="sxs-lookup"><span data-stu-id="24890-259">CustPaymentValidate</span></span>|
|<span data-ttu-id="24890-260">CustSpecTransOverviewFormMode</span><span class="sxs-lookup"><span data-stu-id="24890-260">CustSpecTransOverviewFormMode</span></span>|
|<span data-ttu-id="24890-261">CustTransRefType</span><span class="sxs-lookup"><span data-stu-id="24890-261">CustTransRefType</span></span>|
|<span data-ttu-id="24890-262">CustVendPaymentStatus</span><span class="sxs-lookup"><span data-stu-id="24890-262">CustVendPaymentStatus</span></span>|
|<span data-ttu-id="24890-263">CustVendTransportPointTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="24890-263">CustVendTransportPointTypeTransfer</span></span>|
|<span data-ttu-id="24890-264">DlvScheduleMarkupConversionMode</span><span class="sxs-lookup"><span data-stu-id="24890-264">DlvScheduleMarkupConversionMode</span></span>|
|<span data-ttu-id="24890-265">EcoResAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="24890-265">EcoResAttributeModifier</span></span>|
|<span data-ttu-id="24890-266">EcoResCategoryAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="24890-266">EcoResCategoryAttributeModifier</span></span>|
|<span data-ttu-id="24890-267">EcoResCategoryChangeStatus</span><span class="sxs-lookup"><span data-stu-id="24890-267">EcoResCategoryChangeStatus</span></span>|
|<span data-ttu-id="24890-268">EcoResCategoryHierarchyModifier</span><span class="sxs-lookup"><span data-stu-id="24890-268">EcoResCategoryHierarchyModifier</span></span>|
|<span data-ttu-id="24890-269">EcoResCategoryNamedHierarchyRole</span><span class="sxs-lookup"><span data-stu-id="24890-269">EcoResCategoryNamedHierarchyRole</span></span>|
|<span data-ttu-id="24890-270">EcoResProductImageUsage</span><span class="sxs-lookup"><span data-stu-id="24890-270">EcoResProductImageUsage</span></span>|
|<span data-ttu-id="24890-271">EcoResProductListPage</span><span class="sxs-lookup"><span data-stu-id="24890-271">EcoResProductListPage</span></span>|
|<span data-ttu-id="24890-272">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="24890-272">EcoResProductPerCompanyListPageType</span></span>|
|<span data-ttu-id="24890-273">EcoResProductTemplateType</span><span class="sxs-lookup"><span data-stu-id="24890-273">EcoResProductTemplateType</span></span>|
|<span data-ttu-id="24890-274">EcoResReleaseProductToCompany</span><span class="sxs-lookup"><span data-stu-id="24890-274">EcoResReleaseProductToCompany</span></span>|
|<span data-ttu-id="24890-275">EcoResVariantConfigurationTechnologyType</span><span class="sxs-lookup"><span data-stu-id="24890-275">EcoResVariantConfigurationTechnologyType</span></span>|
|<span data-ttu-id="24890-276">ECPsalesOrdersViewType</span><span class="sxs-lookup"><span data-stu-id="24890-276">ECPsalesOrdersViewType</span></span>|
|<span data-ttu-id="24890-277">EPCSSProductViewType</span><span class="sxs-lookup"><span data-stu-id="24890-277">EPCSSProductViewType</span></span>|
|<span data-ttu-id="24890-278">EUSalesTransMethod</span><span class="sxs-lookup"><span data-stu-id="24890-278">EUSalesTransMethod</span></span>|
|<span data-ttu-id="24890-279">FormLetterType</span><span class="sxs-lookup"><span data-stu-id="24890-279">FormLetterType</span></span>|
|<span data-ttu-id="24890-280">GanttCallerWrkCtr</span><span class="sxs-lookup"><span data-stu-id="24890-280">GanttCallerWrkCtr</span></span>|
|<span data-ttu-id="24890-281">GanttSetupType</span><span class="sxs-lookup"><span data-stu-id="24890-281">GanttSetupType</span></span>|
|<span data-ttu-id="24890-282">GanttTimeUnit</span><span class="sxs-lookup"><span data-stu-id="24890-282">GanttTimeUnit</span></span>|
|<span data-ttu-id="24890-283">GanttWrkCtrDisplayColumnsType</span><span class="sxs-lookup"><span data-stu-id="24890-283">GanttWrkCtrDisplayColumnsType</span></span>|
|<span data-ttu-id="24890-284">IntercompanyGoodsInTransitLineType</span><span class="sxs-lookup"><span data-stu-id="24890-284">IntercompanyGoodsInTransitLineType</span></span>|
|<span data-ttu-id="24890-285">InterCompanyGoodsInTransitOrigin</span><span class="sxs-lookup"><span data-stu-id="24890-285">InterCompanyGoodsInTransitOrigin</span></span>|
|<span data-ttu-id="24890-286">InventAccountType</span><span class="sxs-lookup"><span data-stu-id="24890-286">InventAccountType</span></span>|
|<span data-ttu-id="24890-287">InventAccountTypeStdCostVariance</span><span class="sxs-lookup"><span data-stu-id="24890-287">InventAccountTypeStdCostVariance</span></span>|
|<span data-ttu-id="24890-288">InventAdjustmentBy</span><span class="sxs-lookup"><span data-stu-id="24890-288">InventAdjustmentBy</span></span>|
|<span data-ttu-id="24890-289">InventAgingView</span><span class="sxs-lookup"><span data-stu-id="24890-289">InventAgingView</span></span>|
|<span data-ttu-id="24890-290">InventBatchJournalType</span><span class="sxs-lookup"><span data-stu-id="24890-290">InventBatchJournalType</span></span>|
|<span data-ttu-id="24890-291">InventCostBundleState</span><span class="sxs-lookup"><span data-stu-id="24890-291">InventCostBundleState</span></span>|
|<span data-ttu-id="24890-292">InventCostCostDistribution</span><span class="sxs-lookup"><span data-stu-id="24890-292">InventCostCostDistribution</span></span>|
|<span data-ttu-id="24890-293">InventCostTransactionCategory</span><span class="sxs-lookup"><span data-stu-id="24890-293">InventCostTransactionCategory</span></span>|
|<span data-ttu-id="24890-294">InventCostTransRefType</span><span class="sxs-lookup"><span data-stu-id="24890-294">InventCostTransRefType</span></span>|
|<span data-ttu-id="24890-295">InventCountCode</span><span class="sxs-lookup"><span data-stu-id="24890-295">InventCountCode</span></span>|
|<span data-ttu-id="24890-296">InventItemCostingType</span><span class="sxs-lookup"><span data-stu-id="24890-296">InventItemCostingType</span></span>|
|<span data-ttu-id="24890-297">InventItemLookupDefaultTab</span><span class="sxs-lookup"><span data-stu-id="24890-297">InventItemLookupDefaultTab</span></span>|
|<span data-ttu-id="24890-298">InventItemOrderSetupCallerType</span><span class="sxs-lookup"><span data-stu-id="24890-298">InventItemOrderSetupCallerType</span></span>|
|<span data-ttu-id="24890-299">InventItemOrderSetupType</span><span class="sxs-lookup"><span data-stu-id="24890-299">InventItemOrderSetupType</span></span>|
|<span data-ttu-id="24890-300">InventItemPriceCompareLevel</span><span class="sxs-lookup"><span data-stu-id="24890-300">InventItemPriceCompareLevel</span></span>|
|<span data-ttu-id="24890-301">InventItemPriceFilterType</span><span class="sxs-lookup"><span data-stu-id="24890-301">InventItemPriceFilterType</span></span>|
|<span data-ttu-id="24890-302">InventItemPriceType</span><span class="sxs-lookup"><span data-stu-id="24890-302">InventItemPriceType</span></span>|
|<span data-ttu-id="24890-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span><span class="sxs-lookup"><span data-stu-id="24890-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span></span>|
|<span data-ttu-id="24890-304">InventJournalType</span><span class="sxs-lookup"><span data-stu-id="24890-304">InventJournalType</span></span>|
|<span data-ttu-id="24890-305">InventLedgerConflictModule</span><span class="sxs-lookup"><span data-stu-id="24890-305">InventLedgerConflictModule</span></span>|
|<span data-ttu-id="24890-306">InventLocationType</span><span class="sxs-lookup"><span data-stu-id="24890-306">InventLocationType</span></span>|
|<span data-ttu-id="24890-307">InventMovSubType</span><span class="sxs-lookup"><span data-stu-id="24890-307">InventMovSubType</span></span>|
|<span data-ttu-id="24890-308">InventNonConformanceApproval</span><span class="sxs-lookup"><span data-stu-id="24890-308">InventNonConformanceApproval</span></span>|
|<span data-ttu-id="24890-309">InventNonConformanceHistoryType</span><span class="sxs-lookup"><span data-stu-id="24890-309">InventNonConformanceHistoryType</span></span>|
|<span data-ttu-id="24890-310">InventNonConformanceType</span><span class="sxs-lookup"><span data-stu-id="24890-310">InventNonConformanceType</span></span>|
|<span data-ttu-id="24890-311">InventParameters</span><span class="sxs-lookup"><span data-stu-id="24890-311">InventParameters</span></span>|
|<span data-ttu-id="24890-312">InventPhysicalReduction</span><span class="sxs-lookup"><span data-stu-id="24890-312">InventPhysicalReduction</span></span>|
|<span data-ttu-id="24890-313">InventRefType</span><span class="sxs-lookup"><span data-stu-id="24890-313">InventRefType</span></span>|
|<span data-ttu-id="24890-314">InventReleaseOrderPickingType</span><span class="sxs-lookup"><span data-stu-id="24890-314">InventReleaseOrderPickingType</span></span>|
|<span data-ttu-id="24890-315">InventReportDimHistoryLogType</span><span class="sxs-lookup"><span data-stu-id="24890-315">InventReportDimHistoryLogType</span></span>|
|<span data-ttu-id="24890-316">InventStdCostConvItemStatus</span><span class="sxs-lookup"><span data-stu-id="24890-316">InventStdCostConvItemStatus</span></span>|
|<span data-ttu-id="24890-317">InventStdCostPeriodType</span><span class="sxs-lookup"><span data-stu-id="24890-317">InventStdCostPeriodType</span></span>|
|<span data-ttu-id="24890-318">InventSumFields</span><span class="sxs-lookup"><span data-stu-id="24890-318">InventSumFields</span></span>|
|<span data-ttu-id="24890-319">InventSupplyDlvModeSelectCust</span><span class="sxs-lookup"><span data-stu-id="24890-319">InventSupplyDlvModeSelectCust</span></span>|
|<span data-ttu-id="24890-320">InventSupplyDlvModeSelectSupply</span><span class="sxs-lookup"><span data-stu-id="24890-320">InventSupplyDlvModeSelectSupply</span></span>|
|<span data-ttu-id="24890-321">InventSupplyLeadTimeSource</span><span class="sxs-lookup"><span data-stu-id="24890-321">InventSupplyLeadTimeSource</span></span>|
|<span data-ttu-id="24890-322">InventSupplyTmpLeadtimeType</span><span class="sxs-lookup"><span data-stu-id="24890-322">InventSupplyTmpLeadtimeType</span></span>|
|<span data-ttu-id="24890-323">InventTestActionOnFailure</span><span class="sxs-lookup"><span data-stu-id="24890-323">InventTestActionOnFailure</span></span>|
|<span data-ttu-id="24890-324">InventTestBlockProcess</span><span class="sxs-lookup"><span data-stu-id="24890-324">InventTestBlockProcess</span></span>|
|<span data-ttu-id="24890-325">InventTestCorrectionPriority</span><span class="sxs-lookup"><span data-stu-id="24890-325">InventTestCorrectionPriority</span></span>|
|<span data-ttu-id="24890-326">InventTestCorrectionStatus</span><span class="sxs-lookup"><span data-stu-id="24890-326">InventTestCorrectionStatus</span></span>|
|<span data-ttu-id="24890-327">InventTestDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="24890-327">InventTestDocumentStatus</span></span>|
|<span data-ttu-id="24890-328">InventTestOrderStatusDisplay</span><span class="sxs-lookup"><span data-stu-id="24890-328">InventTestOrderStatusDisplay</span></span>|
|<span data-ttu-id="24890-329">InventTestOutcomeStatus</span><span class="sxs-lookup"><span data-stu-id="24890-329">InventTestOutcomeStatus</span></span>|
|<span data-ttu-id="24890-330">InventTestQtySpecification</span><span class="sxs-lookup"><span data-stu-id="24890-330">InventTestQtySpecification</span></span>|
|<span data-ttu-id="24890-331">InventTestQuarantineType</span><span class="sxs-lookup"><span data-stu-id="24890-331">InventTestQuarantineType</span></span>|
|<span data-ttu-id="24890-332">InventTestReferenceType</span><span class="sxs-lookup"><span data-stu-id="24890-332">InventTestReferenceType</span></span>|
|<span data-ttu-id="24890-333">InventTestReport</span><span class="sxs-lookup"><span data-stu-id="24890-333">InventTestReport</span></span>|
|<span data-ttu-id="24890-334">InventTestType</span><span class="sxs-lookup"><span data-stu-id="24890-334">InventTestType</span></span>|
|<span data-ttu-id="24890-335">InventTrackingDimNodeType</span><span class="sxs-lookup"><span data-stu-id="24890-335">InventTrackingDimNodeType</span></span>|
|<span data-ttu-id="24890-336">InventTrackingProductType</span><span class="sxs-lookup"><span data-stu-id="24890-336">InventTrackingProductType</span></span>|
|<span data-ttu-id="24890-337">InventTrackingRegisterTransRegStatus</span><span class="sxs-lookup"><span data-stu-id="24890-337">InventTrackingRegisterTransRegStatus</span></span>|
|<span data-ttu-id="24890-338">InventTransChildType</span><span class="sxs-lookup"><span data-stu-id="24890-338">InventTransChildType</span></span>|
|<span data-ttu-id="24890-339">InventTransferRemainStatus</span><span class="sxs-lookup"><span data-stu-id="24890-339">InventTransferRemainStatus</span></span>|
|<span data-ttu-id="24890-340">InventTransferStatus</span><span class="sxs-lookup"><span data-stu-id="24890-340">InventTransferStatus</span></span>|
|<span data-ttu-id="24890-341">InventTransferUpdateType</span><span class="sxs-lookup"><span data-stu-id="24890-341">InventTransferUpdateType</span></span>|
|<span data-ttu-id="24890-342">InventTransPickRegisterLineStatus</span><span class="sxs-lookup"><span data-stu-id="24890-342">InventTransPickRegisterLineStatus</span></span>|
|<span data-ttu-id="24890-343">InventTransType</span><span class="sxs-lookup"><span data-stu-id="24890-343">InventTransType</span></span>|
|<span data-ttu-id="24890-344">InventUpdType</span><span class="sxs-lookup"><span data-stu-id="24890-344">InventUpdType</span></span>|
|<span data-ttu-id="24890-345">InventValueReportLedgerAccountCategory</span><span class="sxs-lookup"><span data-stu-id="24890-345">InventValueReportLedgerAccountCategory</span></span>|
|<span data-ttu-id="24890-346">InventValueReportLedgerLineType</span><span class="sxs-lookup"><span data-stu-id="24890-346">InventValueReportLedgerLineType</span></span>|
|<span data-ttu-id="24890-347">InventValueReportResourceType</span><span class="sxs-lookup"><span data-stu-id="24890-347">InventValueReportResourceType</span></span>|
|<span data-ttu-id="24890-348">ItemGroupLedgerDimensionGroup</span><span class="sxs-lookup"><span data-stu-id="24890-348">ItemGroupLedgerDimensionGroup</span></span>|
|<span data-ttu-id="24890-349">ItemReservation</span><span class="sxs-lookup"><span data-stu-id="24890-349">ItemReservation</span></span>|
|<span data-ttu-id="24890-350">JmgAbsenceColumnLayout</span><span class="sxs-lookup"><span data-stu-id="24890-350">JmgAbsenceColumnLayout</span></span>|
|<span data-ttu-id="24890-351">JmgAbsenceMethodEnum</span><span class="sxs-lookup"><span data-stu-id="24890-351">JmgAbsenceMethodEnum</span></span>|
|<span data-ttu-id="24890-352">JmgAttendanceRegistrationType</span><span class="sxs-lookup"><span data-stu-id="24890-352">JmgAttendanceRegistrationType</span></span>|
|<span data-ttu-id="24890-353">JmgAttendanceReportType</span><span class="sxs-lookup"><span data-stu-id="24890-353">JmgAttendanceReportType</span></span>|
|<span data-ttu-id="24890-354">JmgBarCodeType</span><span class="sxs-lookup"><span data-stu-id="24890-354">JmgBarCodeType</span></span>|
|<span data-ttu-id="24890-355">JmgBreakDropEnum</span><span class="sxs-lookup"><span data-stu-id="24890-355">JmgBreakDropEnum</span></span>|
|<span data-ttu-id="24890-356">JmgClockStyle</span><span class="sxs-lookup"><span data-stu-id="24890-356">JmgClockStyle</span></span>|
|<span data-ttu-id="24890-357">JmgControlType</span><span class="sxs-lookup"><span data-stu-id="24890-357">JmgControlType</span></span>|
|<span data-ttu-id="24890-358">JmgDaysTotalWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="24890-358">JmgDaysTotalWorkflowStatus</span></span>|
|<span data-ttu-id="24890-359">JmgEmployeeSignInStatus</span><span class="sxs-lookup"><span data-stu-id="24890-359">JmgEmployeeSignInStatus</span></span>|
|<span data-ttu-id="24890-360">JmgFeedbackButtonFunction</span><span class="sxs-lookup"><span data-stu-id="24890-360">JmgFeedbackButtonFunction</span></span>|
|<span data-ttu-id="24890-361">JmgFeedbackStyle</span><span class="sxs-lookup"><span data-stu-id="24890-361">JmgFeedbackStyle</span></span>|
|<span data-ttu-id="24890-362">JmgFieldName</span><span class="sxs-lookup"><span data-stu-id="24890-362">JmgFieldName</span></span>|
|<span data-ttu-id="24890-363">JmgGetRegistrationTimeFrom</span><span class="sxs-lookup"><span data-stu-id="24890-363">JmgGetRegistrationTimeFrom</span></span>|
|<span data-ttu-id="24890-364">JmgGridAppearance</span><span class="sxs-lookup"><span data-stu-id="24890-364">JmgGridAppearance</span></span>|
|<span data-ttu-id="24890-365">JmgJobTableSynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="24890-365">JmgJobTableSynchronizationMode</span></span>|
|<span data-ttu-id="24890-366">JmgJournalRegWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="24890-366">JmgJournalRegWorkflowStatus</span></span>|
|<span data-ttu-id="24890-367">JmgMark</span><span class="sxs-lookup"><span data-stu-id="24890-367">JmgMark</span></span>|
|<span data-ttu-id="24890-368">JmgMessageType</span><span class="sxs-lookup"><span data-stu-id="24890-368">JmgMessageType</span></span>|
|<span data-ttu-id="24890-369">JmgPayAdjustType</span><span class="sxs-lookup"><span data-stu-id="24890-369">JmgPayAdjustType</span></span>|
|<span data-ttu-id="24890-370">JmgPayEventsExportType</span><span class="sxs-lookup"><span data-stu-id="24890-370">JmgPayEventsExportType</span></span>|
|<span data-ttu-id="24890-371">JmgPaySpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="24890-371">JmgPaySpecTypeEnum</span></span>|
|<span data-ttu-id="24890-372">JmgPaySpecTypeEnumPick</span><span class="sxs-lookup"><span data-stu-id="24890-372">JmgPaySpecTypeEnumPick</span></span>|
|<span data-ttu-id="24890-373">JmgPostAutomatically</span><span class="sxs-lookup"><span data-stu-id="24890-373">JmgPostAutomatically</span></span>|
|<span data-ttu-id="24890-374">JmgProdStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-374">JmgProdStatusUpdate</span></span>|
|<span data-ttu-id="24890-375">JmgProdStatusUpdateReportFinished</span><span class="sxs-lookup"><span data-stu-id="24890-375">JmgProdStatusUpdateReportFinished</span></span>|
|<span data-ttu-id="24890-376">JmgProfileSpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="24890-376">JmgProfileSpecTypeEnum</span></span>|
|<span data-ttu-id="24890-377">JmgProfileStartCodeBlankPrev</span><span class="sxs-lookup"><span data-stu-id="24890-377">JmgProfileStartCodeBlankPrev</span></span>|
|<span data-ttu-id="24890-378">JmgProjStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-378">JmgProjStatusUpdate</span></span>|
|<span data-ttu-id="24890-379">JmgRegistrationTouchJobStatus</span><span class="sxs-lookup"><span data-stu-id="24890-379">JmgRegistrationTouchJobStatus</span></span>|
|<span data-ttu-id="24890-380">JmgSecondPresentationEnum</span><span class="sxs-lookup"><span data-stu-id="24890-380">JmgSecondPresentationEnum</span></span>|
|<span data-ttu-id="24890-381">JmgShopFloorServiceStatus</span><span class="sxs-lookup"><span data-stu-id="24890-381">JmgShopFloorServiceStatus</span></span>|
|<span data-ttu-id="24890-382">JmgSignInButtonFunction</span><span class="sxs-lookup"><span data-stu-id="24890-382">JmgSignInButtonFunction</span></span>|
|<span data-ttu-id="24890-383">JmgStoppedCompletedStatus</span><span class="sxs-lookup"><span data-stu-id="24890-383">JmgStoppedCompletedStatus</span></span>|
|<span data-ttu-id="24890-384">JmgTermBaudeRate</span><span class="sxs-lookup"><span data-stu-id="24890-384">JmgTermBaudeRate</span></span>|
|<span data-ttu-id="24890-385">JmgTermComPort</span><span class="sxs-lookup"><span data-stu-id="24890-385">JmgTermComPort</span></span>|
|<span data-ttu-id="24890-386">JmgTermDataBit</span><span class="sxs-lookup"><span data-stu-id="24890-386">JmgTermDataBit</span></span>|
|<span data-ttu-id="24890-387">JmgTerminalInsertMode</span><span class="sxs-lookup"><span data-stu-id="24890-387">JmgTerminalInsertMode</span></span>|
|<span data-ttu-id="24890-388">JmgTermStopBit</span><span class="sxs-lookup"><span data-stu-id="24890-388">JmgTermStopBit</span></span>|
|<span data-ttu-id="24890-389">KanbanBoardRefreshCycle</span><span class="sxs-lookup"><span data-stu-id="24890-389">KanbanBoardRefreshCycle</span></span>|
|<span data-ttu-id="24890-390">KanbanBoardType</span><span class="sxs-lookup"><span data-stu-id="24890-390">KanbanBoardType</span></span>|
|<span data-ttu-id="24890-391">KanbanCardAssignmentType</span><span class="sxs-lookup"><span data-stu-id="24890-391">KanbanCardAssignmentType</span></span>|
|<span data-ttu-id="24890-392">KanbanControlActionState</span><span class="sxs-lookup"><span data-stu-id="24890-392">KanbanControlActionState</span></span>|
|<span data-ttu-id="24890-393">KanbanControlLegendFormat</span><span class="sxs-lookup"><span data-stu-id="24890-393">KanbanControlLegendFormat</span></span>|
|<span data-ttu-id="24890-394">KanbanControlSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="24890-394">KanbanControlSelectionChanged</span></span>|
|<span data-ttu-id="24890-395">KanbanDemandOriginType</span><span class="sxs-lookup"><span data-stu-id="24890-395">KanbanDemandOriginType</span></span>|
|<span data-ttu-id="24890-396">KanbanJobPeggingType</span><span class="sxs-lookup"><span data-stu-id="24890-396">KanbanJobPeggingType</span></span>|
|<span data-ttu-id="24890-397">KanbanJobPickingListLineType</span><span class="sxs-lookup"><span data-stu-id="24890-397">KanbanJobPickingListLineType</span></span>|
|<span data-ttu-id="24890-398">KanbanLineEventType</span><span class="sxs-lookup"><span data-stu-id="24890-398">KanbanLineEventType</span></span>|
|<span data-ttu-id="24890-399">KanbanMultiMode</span><span class="sxs-lookup"><span data-stu-id="24890-399">KanbanMultiMode</span></span>|
|<span data-ttu-id="24890-400">KanbanPrintInstructions</span><span class="sxs-lookup"><span data-stu-id="24890-400">KanbanPrintInstructions</span></span>|
|<span data-ttu-id="24890-401">KanbanProdBOMLineEventType</span><span class="sxs-lookup"><span data-stu-id="24890-401">KanbanProdBOMLineEventType</span></span>|
|<span data-ttu-id="24890-402">KanbanQuantityCalculationStatus</span><span class="sxs-lookup"><span data-stu-id="24890-402">KanbanQuantityCalculationStatus</span></span>|
|<span data-ttu-id="24890-403">KanbanSalesLineEventType</span><span class="sxs-lookup"><span data-stu-id="24890-403">KanbanSalesLineEventType</span></span>|
|<span data-ttu-id="24890-404">KanbanStockReplenishmentEventType</span><span class="sxs-lookup"><span data-stu-id="24890-404">KanbanStockReplenishmentEventType</span></span>|
|<span data-ttu-id="24890-405">LeanBOMLineReservationMethod</span><span class="sxs-lookup"><span data-stu-id="24890-405">LeanBOMLineReservationMethod</span></span>|
|<span data-ttu-id="24890-406">LeanCostingUnusedQtyType</span><span class="sxs-lookup"><span data-stu-id="24890-406">LeanCostingUnusedQtyType</span></span>|
|<span data-ttu-id="24890-407">LeanHandlingUnitEmptyPolicy</span><span class="sxs-lookup"><span data-stu-id="24890-407">LeanHandlingUnitEmptyPolicy</span></span>|
|<span data-ttu-id="24890-408">LeanInventoryControl</span><span class="sxs-lookup"><span data-stu-id="24890-408">LeanInventoryControl</span></span>|
|<span data-ttu-id="24890-409">LeanPeggedEventType</span><span class="sxs-lookup"><span data-stu-id="24890-409">LeanPeggedEventType</span></span>|
|<span data-ttu-id="24890-410">LeanPlanJobReferenceTypes</span><span class="sxs-lookup"><span data-stu-id="24890-410">LeanPlanJobReferenceTypes</span></span>|
|<span data-ttu-id="24890-411">LeanProductionFlowCostingStatus</span><span class="sxs-lookup"><span data-stu-id="24890-411">LeanProductionFlowCostingStatus</span></span>|
|<span data-ttu-id="24890-412">LeanProductionFlowVisualizationViewMode</span><span class="sxs-lookup"><span data-stu-id="24890-412">LeanProductionFlowVisualizationViewMode</span></span>|
|<span data-ttu-id="24890-413">LeanProductTypes</span><span class="sxs-lookup"><span data-stu-id="24890-413">LeanProductTypes</span></span>|
|<span data-ttu-id="24890-414">LeanTaktStatus</span><span class="sxs-lookup"><span data-stu-id="24890-414">LeanTaktStatus</span></span>|
|<span data-ttu-id="24890-415">LedgerPostingType</span><span class="sxs-lookup"><span data-stu-id="24890-415">LedgerPostingType</span></span>|
|<span data-ttu-id="24890-416">LedgerTransTxt</span><span class="sxs-lookup"><span data-stu-id="24890-416">LedgerTransTxt</span></span>|
|<span data-ttu-id="24890-417">MarkupAllocateAfter</span><span class="sxs-lookup"><span data-stu-id="24890-417">MarkupAllocateAfter</span></span>|
|<span data-ttu-id="24890-418">MarkupCategory</span><span class="sxs-lookup"><span data-stu-id="24890-418">MarkupCategory</span></span>|
|<span data-ttu-id="24890-419">MCRBrokerContractStatus</span><span class="sxs-lookup"><span data-stu-id="24890-419">MCRBrokerContractStatus</span></span>|
|<span data-ttu-id="24890-420">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="24890-420">MCRCustSearchType</span></span>|
|<span data-ttu-id="24890-421">MCRFullTextSearchType</span><span class="sxs-lookup"><span data-stu-id="24890-421">MCRFullTextSearchType</span></span>|
|<span data-ttu-id="24890-422">MCRInstallPlanApplyMiscCharge</span><span class="sxs-lookup"><span data-stu-id="24890-422">MCRInstallPlanApplyMiscCharge</span></span>|
|<span data-ttu-id="24890-423">MCRItemListGenerationType</span><span class="sxs-lookup"><span data-stu-id="24890-423">MCRItemListGenerationType</span></span>|
|<span data-ttu-id="24890-424">MCRPickingPrompt</span><span class="sxs-lookup"><span data-stu-id="24890-424">MCRPickingPrompt</span></span>|
|<span data-ttu-id="24890-425">MCRPickingSessionStatus</span><span class="sxs-lookup"><span data-stu-id="24890-425">MCRPickingSessionStatus</span></span>|
|<span data-ttu-id="24890-426">MCRPickingWaveStatus</span><span class="sxs-lookup"><span data-stu-id="24890-426">MCRPickingWaveStatus</span></span>|
|<span data-ttu-id="24890-427">MCRPriceHistoryType</span><span class="sxs-lookup"><span data-stu-id="24890-427">MCRPriceHistoryType</span></span>|
|<span data-ttu-id="24890-428">MCRRoyaltyLineBreakType</span><span class="sxs-lookup"><span data-stu-id="24890-428">MCRRoyaltyLineBreakType</span></span>|
|<span data-ttu-id="24890-429">MCRRoyaltyTakenFrom</span><span class="sxs-lookup"><span data-stu-id="24890-429">MCRRoyaltyTakenFrom</span></span>|
|<span data-ttu-id="24890-430">MCRRoyaltyTransactionType</span><span class="sxs-lookup"><span data-stu-id="24890-430">MCRRoyaltyTransactionType</span></span>|
|<span data-ttu-id="24890-431">MCRRoyaltyUnitType</span><span class="sxs-lookup"><span data-stu-id="24890-431">MCRRoyaltyUnitType</span></span>|
|<span data-ttu-id="24890-432">MCRRoyaltyUOMOption</span><span class="sxs-lookup"><span data-stu-id="24890-432">MCRRoyaltyUOMOption</span></span>|
|<span data-ttu-id="24890-433">MCRSalesOrderDetailStatus</span><span class="sxs-lookup"><span data-stu-id="24890-433">MCRSalesOrderDetailStatus</span></span>|
|<span data-ttu-id="24890-434">ModuleInventCustVend</span><span class="sxs-lookup"><span data-stu-id="24890-434">ModuleInventCustVend</span></span>|
|<span data-ttu-id="24890-435">ModuleInventPurchSales</span><span class="sxs-lookup"><span data-stu-id="24890-435">ModuleInventPurchSales</span></span>|
|<span data-ttu-id="24890-436">OriginalDocument</span><span class="sxs-lookup"><span data-stu-id="24890-436">OriginalDocument</span></span>|
|<span data-ttu-id="24890-437">PaymDocumentType</span><span class="sxs-lookup"><span data-stu-id="24890-437">PaymDocumentType</span></span>|
|<span data-ttu-id="24890-438">PCExpressionEditorSymbolType</span><span class="sxs-lookup"><span data-stu-id="24890-438">PCExpressionEditorSymbolType</span></span>|
|<span data-ttu-id="24890-439">PCLookupMethod</span><span class="sxs-lookup"><span data-stu-id="24890-439">PCLookupMethod</span></span>|
|<span data-ttu-id="24890-440">PCNewSelectComponent</span><span class="sxs-lookup"><span data-stu-id="24890-440">PCNewSelectComponent</span></span>|
|<span data-ttu-id="24890-441">PCRequirement</span><span class="sxs-lookup"><span data-stu-id="24890-441">PCRequirement</span></span>|
|<span data-ttu-id="24890-442">PCTableConstraintType</span><span class="sxs-lookup"><span data-stu-id="24890-442">PCTableConstraintType</span></span>|
|<span data-ttu-id="24890-443">PDSAdjustmentPrinciple</span><span class="sxs-lookup"><span data-stu-id="24890-443">PDSAdjustmentPrinciple</span></span>|
|<span data-ttu-id="24890-444">PdsBatchAttribToleranceAction</span><span class="sxs-lookup"><span data-stu-id="24890-444">PdsBatchAttribToleranceAction</span></span>|
|<span data-ttu-id="24890-445">PdsBatchAttribUpdateType</span><span class="sxs-lookup"><span data-stu-id="24890-445">PdsBatchAttribUpdateType</span></span>|
|<span data-ttu-id="24890-446">PDSCalcElementBase</span><span class="sxs-lookup"><span data-stu-id="24890-446">PDSCalcElementBase</span></span>|
|<span data-ttu-id="24890-447">PDSCompensationPrincipleEnum</span><span class="sxs-lookup"><span data-stu-id="24890-447">PDSCompensationPrincipleEnum</span></span>|
|<span data-ttu-id="24890-448">PDSElementTypeEnum</span><span class="sxs-lookup"><span data-stu-id="24890-448">PDSElementTypeEnum</span></span>|
|<span data-ttu-id="24890-449">PDSIngredientTypeEnum</span><span class="sxs-lookup"><span data-stu-id="24890-449">PDSIngredientTypeEnum</span></span>|
|<span data-ttu-id="24890-450">PdsMRCDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="24890-450">PdsMRCDocumentStatus</span></span>|
|<span data-ttu-id="24890-451">PdsMRCEffectiveDateBasis</span><span class="sxs-lookup"><span data-stu-id="24890-451">PdsMRCEffectiveDateBasis</span></span>|
|<span data-ttu-id="24890-452">PdsMRCEventModule</span><span class="sxs-lookup"><span data-stu-id="24890-452">PdsMRCEventModule</span></span>|
|<span data-ttu-id="24890-453">PdsMRCEventType</span><span class="sxs-lookup"><span data-stu-id="24890-453">PdsMRCEventType</span></span>|
|<span data-ttu-id="24890-454">PdsMRCListType</span><span class="sxs-lookup"><span data-stu-id="24890-454">PdsMRCListType</span></span>|
|<span data-ttu-id="24890-455">PdsPaymtType</span><span class="sxs-lookup"><span data-stu-id="24890-455">PdsPaymtType</span></span>|
|<span data-ttu-id="24890-456">PDSPotencyAttribRecordingEnum</span><span class="sxs-lookup"><span data-stu-id="24890-456">PDSPotencyAttribRecordingEnum</span></span>|
|<span data-ttu-id="24890-457">PdsRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="24890-457">PdsRebateCalcDateType</span></span>|
|<span data-ttu-id="24890-458">PdsRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="24890-458">PdsRebateTakenFrom</span></span>|
|<span data-ttu-id="24890-459">PdsRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="24890-459">PdsRebateUOMOption</span></span>|
|<span data-ttu-id="24890-460">PdsSameLotError</span><span class="sxs-lookup"><span data-stu-id="24890-460">PdsSameLotError</span></span>|
|<span data-ttu-id="24890-461">pdsTMAJournalPosting</span><span class="sxs-lookup"><span data-stu-id="24890-461">pdsTMAJournalPosting</span></span>|
|<span data-ttu-id="24890-462">PdsUpdateBatchDate</span><span class="sxs-lookup"><span data-stu-id="24890-462">PdsUpdateBatchDate</span></span>|
|<span data-ttu-id="24890-463">PdsUpdateDispositionStatus_Quality</span><span class="sxs-lookup"><span data-stu-id="24890-463">PdsUpdateDispositionStatus_Quality</span></span>|
|<span data-ttu-id="24890-464">PlanActivityCreateRelationType</span><span class="sxs-lookup"><span data-stu-id="24890-464">PlanActivityCreateRelationType</span></span>|
|<span data-ttu-id="24890-465">PlanActivityProductionFlowActivityType</span><span class="sxs-lookup"><span data-stu-id="24890-465">PlanActivityProductionFlowActivityType</span></span>|
|<span data-ttu-id="24890-466">PlanTypes</span><span class="sxs-lookup"><span data-stu-id="24890-466">PlanTypes</span></span>|
|<span data-ttu-id="24890-467">PmfCostAllocationMethod</span><span class="sxs-lookup"><span data-stu-id="24890-467">PmfCostAllocationMethod</span></span>|
|<span data-ttu-id="24890-468">PmfOrderType</span><span class="sxs-lookup"><span data-stu-id="24890-468">PmfOrderType</span></span>|
|<span data-ttu-id="24890-469">PmfOrderTypeFilter</span><span class="sxs-lookup"><span data-stu-id="24890-469">PmfOrderTypeFilter</span></span>|
|<span data-ttu-id="24890-470">PmfProdType</span><span class="sxs-lookup"><span data-stu-id="24890-470">PmfProdType</span></span>|
|<span data-ttu-id="24890-471">PMFSeqCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="24890-471">PMFSeqCalendarPeriod</span></span>|
|<span data-ttu-id="24890-472">PriceBase</span><span class="sxs-lookup"><span data-stu-id="24890-472">PriceBase</span></span>|
|<span data-ttu-id="24890-473">PriceDiscPurchasePromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="24890-473">PriceDiscPurchasePromptSystemSource</span></span>|
|<span data-ttu-id="24890-474">PriceDiscSalesPromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="24890-474">PriceDiscSalesPromptSystemSource</span></span>|
|<span data-ttu-id="24890-475">PriceGroupType</span><span class="sxs-lookup"><span data-stu-id="24890-475">PriceGroupType</span></span>|
|<span data-ttu-id="24890-476">PriceSalesPurch</span><span class="sxs-lookup"><span data-stu-id="24890-476">PriceSalesPurch</span></span>|
|<span data-ttu-id="24890-477">PriceType</span><span class="sxs-lookup"><span data-stu-id="24890-477">PriceType</span></span>|
|<span data-ttu-id="24890-478">ProcCategoryAdministrationActivity</span><span class="sxs-lookup"><span data-stu-id="24890-478">ProcCategoryAdministrationActivity</span></span>|
|<span data-ttu-id="24890-479">ProdBOMConsumpProposal</span><span class="sxs-lookup"><span data-stu-id="24890-479">ProdBOMConsumpProposal</span></span>|
|<span data-ttu-id="24890-480">ProdBOMJournalQty</span><span class="sxs-lookup"><span data-stu-id="24890-480">ProdBOMJournalQty</span></span>|
|<span data-ttu-id="24890-481">ProdBOMJournalSplit</span><span class="sxs-lookup"><span data-stu-id="24890-481">ProdBOMJournalSplit</span></span>|
|<span data-ttu-id="24890-482">ProdErrorCause</span><span class="sxs-lookup"><span data-stu-id="24890-482">ProdErrorCause</span></span>|
|<span data-ttu-id="24890-483">ProdGanttJobColorType</span><span class="sxs-lookup"><span data-stu-id="24890-483">ProdGanttJobColorType</span></span>|
|<span data-ttu-id="24890-484">ProdGanttLoad</span><span class="sxs-lookup"><span data-stu-id="24890-484">ProdGanttLoad</span></span>|
|<span data-ttu-id="24890-485">ProdGanttRouteColorType</span><span class="sxs-lookup"><span data-stu-id="24890-485">ProdGanttRouteColorType</span></span>|
|<span data-ttu-id="24890-486">ProdJournalCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="24890-486">ProdJournalCleanUpMode</span></span>|
|<span data-ttu-id="24890-487">ProdMode</span><span class="sxs-lookup"><span data-stu-id="24890-487">ProdMode</span></span>|
|<span data-ttu-id="24890-488">ProdNotificationLevel</span><span class="sxs-lookup"><span data-stu-id="24890-488">ProdNotificationLevel</span></span>|
|<span data-ttu-id="24890-489">ProdParamInventDimLookup</span><span class="sxs-lookup"><span data-stu-id="24890-489">ProdParamInventDimLookup</span></span>|
|<span data-ttu-id="24890-490">ProdParmType</span><span class="sxs-lookup"><span data-stu-id="24890-490">ProdParmType</span></span>|
|<span data-ttu-id="24890-491">ProdRefLookUp</span><span class="sxs-lookup"><span data-stu-id="24890-491">ProdRefLookUp</span></span>|
|<span data-ttu-id="24890-492">ProdRouteJobCurrentFormTabId</span><span class="sxs-lookup"><span data-stu-id="24890-492">ProdRouteJobCurrentFormTabId</span></span>|
|<span data-ttu-id="24890-493">ProdSchedDirection</span><span class="sxs-lookup"><span data-stu-id="24890-493">ProdSchedDirection</span></span>|
|<span data-ttu-id="24890-494">ProdScrapMethod</span><span class="sxs-lookup"><span data-stu-id="24890-494">ProdScrapMethod</span></span>|
|<span data-ttu-id="24890-495">ProdStandardCostVariance</span><span class="sxs-lookup"><span data-stu-id="24890-495">ProdStandardCostVariance</span></span>|
|<span data-ttu-id="24890-496">ProdStatusAll</span><span class="sxs-lookup"><span data-stu-id="24890-496">ProdStatusAll</span></span>|
|<span data-ttu-id="24890-497">ProdStatusType</span><span class="sxs-lookup"><span data-stu-id="24890-497">ProdStatusType</span></span>|
|<span data-ttu-id="24890-498">ProductionTransType</span><span class="sxs-lookup"><span data-stu-id="24890-498">ProductionTransType</span></span>|
|<span data-ttu-id="24890-499">ProdUpdateJour</span><span class="sxs-lookup"><span data-stu-id="24890-499">ProdUpdateJour</span></span>|
|<span data-ttu-id="24890-500">ProdWHSReleasePolicy</span><span class="sxs-lookup"><span data-stu-id="24890-500">ProdWHSReleasePolicy</span></span>|
|<span data-ttu-id="24890-501">ProdWIPType_NA</span><span class="sxs-lookup"><span data-stu-id="24890-501">ProdWIPType_NA</span></span>|
|<span data-ttu-id="24890-502">PurchaseOrderResponseAction</span><span class="sxs-lookup"><span data-stu-id="24890-502">PurchaseOrderResponseAction</span></span>|
|<span data-ttu-id="24890-503">PurchaseType</span><span class="sxs-lookup"><span data-stu-id="24890-503">PurchaseType</span></span>|
|<span data-ttu-id="24890-504">PurchasingTransactionType</span><span class="sxs-lookup"><span data-stu-id="24890-504">PurchasingTransactionType</span></span>|
|<span data-ttu-id="24890-505">PurchCORReceivingMethod</span><span class="sxs-lookup"><span data-stu-id="24890-505">PurchCORReceivingMethod</span></span>|
|<span data-ttu-id="24890-506">PurchCORRejectStatus</span><span class="sxs-lookup"><span data-stu-id="24890-506">PurchCORRejectStatus</span></span>|
|<span data-ttu-id="24890-507">PurchCovRef</span><span class="sxs-lookup"><span data-stu-id="24890-507">PurchCovRef</span></span>|
|<span data-ttu-id="24890-508">PurchDlvAddr</span><span class="sxs-lookup"><span data-stu-id="24890-508">PurchDlvAddr</span></span>|
|<span data-ttu-id="24890-509">PurchLineBackOrderViews</span><span class="sxs-lookup"><span data-stu-id="24890-509">PurchLineBackOrderViews</span></span>|
|<span data-ttu-id="24890-510">PurchLineDeliveryFulfillment</span><span class="sxs-lookup"><span data-stu-id="24890-510">PurchLineDeliveryFulfillment</span></span>|
|<span data-ttu-id="24890-511">PurchLineDeliveryPrecision</span><span class="sxs-lookup"><span data-stu-id="24890-511">PurchLineDeliveryPrecision</span></span>|
|<span data-ttu-id="24890-512">PurchMatchingPolicyOverrideOption</span><span class="sxs-lookup"><span data-stu-id="24890-512">PurchMatchingPolicyOverrideOption</span></span>|
|<span data-ttu-id="24890-513">PurchPrepayApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="24890-513">PurchPrepayApplicationPolicy</span></span>|
|<span data-ttu-id="24890-514">PurchPriceDateType</span><span class="sxs-lookup"><span data-stu-id="24890-514">PurchPriceDateType</span></span>|
|<span data-ttu-id="24890-515">PurchPurchaseOrderCreationMethod</span><span class="sxs-lookup"><span data-stu-id="24890-515">PurchPurchaseOrderCreationMethod</span></span>|
|<span data-ttu-id="24890-516">PurchReApprovalPolicyRuleViewType</span><span class="sxs-lookup"><span data-stu-id="24890-516">PurchReApprovalPolicyRuleViewType</span></span>|
|<span data-ttu-id="24890-517">PurchReqAuthorizationSpecificReporting</span><span class="sxs-lookup"><span data-stu-id="24890-517">PurchReqAuthorizationSpecificReporting</span></span>|
|<span data-ttu-id="24890-518">PurchReqAutoCreatePurch</span><span class="sxs-lookup"><span data-stu-id="24890-518">PurchReqAutoCreatePurch</span></span>|
|<span data-ttu-id="24890-519">PurchReqCatalogAllNon</span><span class="sxs-lookup"><span data-stu-id="24890-519">PurchReqCatalogAllNon</span></span>|
|<span data-ttu-id="24890-520">PurchReqConsolidationActiveStatus</span><span class="sxs-lookup"><span data-stu-id="24890-520">PurchReqConsolidationActiveStatus</span></span>|
|<span data-ttu-id="24890-521">PurchReqConsolidationPriority</span><span class="sxs-lookup"><span data-stu-id="24890-521">PurchReqConsolidationPriority</span></span>|
|<span data-ttu-id="24890-522">PurchReqConsolidationStatus</span><span class="sxs-lookup"><span data-stu-id="24890-522">PurchReqConsolidationStatus</span></span>|
|<span data-ttu-id="24890-523">PurchReqCreationStatus</span><span class="sxs-lookup"><span data-stu-id="24890-523">PurchReqCreationStatus</span></span>|
|<span data-ttu-id="24890-524">PurchReqItemDescriptionTransfer</span><span class="sxs-lookup"><span data-stu-id="24890-524">PurchReqItemDescriptionTransfer</span></span>|
|<span data-ttu-id="24890-525">PurchReqItemFilterType</span><span class="sxs-lookup"><span data-stu-id="24890-525">PurchReqItemFilterType</span></span>|
|<span data-ttu-id="24890-526">PurchReqOnBehalfReports</span><span class="sxs-lookup"><span data-stu-id="24890-526">PurchReqOnBehalfReports</span></span>|
|<span data-ttu-id="24890-527">PurchReqOriginationAuthorizationView</span><span class="sxs-lookup"><span data-stu-id="24890-527">PurchReqOriginationAuthorizationView</span></span>|
|<span data-ttu-id="24890-528">PurchReqProcessingState</span><span class="sxs-lookup"><span data-stu-id="24890-528">PurchReqProcessingState</span></span>|
|<span data-ttu-id="24890-529">PurchReqQuestionnaireAggregateStatus</span><span class="sxs-lookup"><span data-stu-id="24890-529">PurchReqQuestionnaireAggregateStatus</span></span>|
|<span data-ttu-id="24890-530">PurchReqQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="24890-530">PurchReqQuestionnaireStatus</span></span>|
|<span data-ttu-id="24890-531">PurchReqReportSortOrder</span><span class="sxs-lookup"><span data-stu-id="24890-531">PurchReqReportSortOrder</span></span>|
|<span data-ttu-id="24890-532">PurchReqReportStatus</span><span class="sxs-lookup"><span data-stu-id="24890-532">PurchReqReportStatus</span></span>|
|<span data-ttu-id="24890-533">PurchReqReviewStatus</span><span class="sxs-lookup"><span data-stu-id="24890-533">PurchReqReviewStatus</span></span>|
|<span data-ttu-id="24890-534">PurchReqRFQRequirement</span><span class="sxs-lookup"><span data-stu-id="24890-534">PurchReqRFQRequirement</span></span>|
|<span data-ttu-id="24890-535">PurchReqRFQType</span><span class="sxs-lookup"><span data-stu-id="24890-535">PurchReqRFQType</span></span>|
|<span data-ttu-id="24890-536">PurchReqSaveChanges</span><span class="sxs-lookup"><span data-stu-id="24890-536">PurchReqSaveChanges</span></span>|
|<span data-ttu-id="24890-537">PurchReqStatus</span><span class="sxs-lookup"><span data-stu-id="24890-537">PurchReqStatus</span></span>|
|<span data-ttu-id="24890-538">PurchReqType</span><span class="sxs-lookup"><span data-stu-id="24890-538">PurchReqType</span></span>|
|<span data-ttu-id="24890-539">PurchReqWorkflowState</span><span class="sxs-lookup"><span data-stu-id="24890-539">PurchReqWorkflowState</span></span>|
|<span data-ttu-id="24890-540">PurchRFQQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="24890-540">PurchRFQQuestionnaireStatus</span></span>|
|<span data-ttu-id="24890-541">PurchRFQStatusVendor</span><span class="sxs-lookup"><span data-stu-id="24890-541">PurchRFQStatusVendor</span></span>|
|<span data-ttu-id="24890-542">PurchRFQType</span><span class="sxs-lookup"><span data-stu-id="24890-542">PurchRFQType</span></span>|
|<span data-ttu-id="24890-543">PurchTableFormId</span><span class="sxs-lookup"><span data-stu-id="24890-543">PurchTableFormId</span></span>|
|<span data-ttu-id="24890-544">PurchTableListPage</span><span class="sxs-lookup"><span data-stu-id="24890-544">PurchTableListPage</span></span>|
|<span data-ttu-id="24890-545">PurchTableMode</span><span class="sxs-lookup"><span data-stu-id="24890-545">PurchTableMode</span></span>|
|<span data-ttu-id="24890-546">PurchTotalsCachingMethod</span><span class="sxs-lookup"><span data-stu-id="24890-546">PurchTotalsCachingMethod</span></span>|
|<span data-ttu-id="24890-547">PurchUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-547">PurchUpdate</span></span>|
|<span data-ttu-id="24890-548">PurchVendorPortalShowResponseType</span><span class="sxs-lookup"><span data-stu-id="24890-548">PurchVendorPortalShowResponseType</span></span>|
|<span data-ttu-id="24890-549">QuotationType</span><span class="sxs-lookup"><span data-stu-id="24890-549">QuotationType</span></span>|
|<span data-ttu-id="24890-550">ReqBOMRouteCreated</span><span class="sxs-lookup"><span data-stu-id="24890-550">ReqBOMRouteCreated</span></span>|
|<span data-ttu-id="24890-551">ReqCurrentDaySchedFrom</span><span class="sxs-lookup"><span data-stu-id="24890-551">ReqCurrentDaySchedFrom</span></span>|
|<span data-ttu-id="24890-552">ReqDemPlanDataSourceType</span><span class="sxs-lookup"><span data-stu-id="24890-552">ReqDemPlanDataSourceType</span></span>|
|<span data-ttu-id="24890-553">ReqDemPlanDemandCategory</span><span class="sxs-lookup"><span data-stu-id="24890-553">ReqDemPlanDemandCategory</span></span>|
|<span data-ttu-id="24890-554">ReqDemPlanForecastAttributeType</span><span class="sxs-lookup"><span data-stu-id="24890-554">ReqDemPlanForecastAttributeType</span></span>|
|<span data-ttu-id="24890-555">ReqDemPlanForecastingStrategy</span><span class="sxs-lookup"><span data-stu-id="24890-555">ReqDemPlanForecastingStrategy</span></span>|
|<span data-ttu-id="24890-556">ReqDemPlanForecastType</span><span class="sxs-lookup"><span data-stu-id="24890-556">ReqDemPlanForecastType</span></span>|
|<span data-ttu-id="24890-557">ReqDisplayDelay</span><span class="sxs-lookup"><span data-stu-id="24890-557">ReqDisplayDelay</span></span>|
|<span data-ttu-id="24890-558">ReqForecastReducedBy</span><span class="sxs-lookup"><span data-stu-id="24890-558">ReqForecastReducedBy</span></span>|
|<span data-ttu-id="24890-559">ReqGanttColorType</span><span class="sxs-lookup"><span data-stu-id="24890-559">ReqGanttColorType</span></span>|
|<span data-ttu-id="24890-560">ReqGanttShow</span><span class="sxs-lookup"><span data-stu-id="24890-560">ReqGanttShow</span></span>|
|<span data-ttu-id="24890-561">ReqItemJournalType</span><span class="sxs-lookup"><span data-stu-id="24890-561">ReqItemJournalType</span></span>|
|<span data-ttu-id="24890-562">ReqItemTableWizardPurpose</span><span class="sxs-lookup"><span data-stu-id="24890-562">ReqItemTableWizardPurpose</span></span>|
|<span data-ttu-id="24890-563">ReqMarkUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-563">ReqMarkUpdate</span></span>|
|<span data-ttu-id="24890-564">ReqPeggingAssignmentType</span><span class="sxs-lookup"><span data-stu-id="24890-564">ReqPeggingAssignmentType</span></span>|
|<span data-ttu-id="24890-565">ReqPeggingType</span><span class="sxs-lookup"><span data-stu-id="24890-565">ReqPeggingType</span></span>|
|<span data-ttu-id="24890-566">ReqPlannedOrderLeveling</span><span class="sxs-lookup"><span data-stu-id="24890-566">ReqPlannedOrderLeveling</span></span>|
|<span data-ttu-id="24890-567">ReqPlanType</span><span class="sxs-lookup"><span data-stu-id="24890-567">ReqPlanType</span></span>|
|<span data-ttu-id="24890-568">ReqPOStatus</span><span class="sxs-lookup"><span data-stu-id="24890-568">ReqPOStatus</span></span>|
|<span data-ttu-id="24890-569">ReqQtyAmount</span><span class="sxs-lookup"><span data-stu-id="24890-569">ReqQtyAmount</span></span>|
|<span data-ttu-id="24890-570">ReqRefType</span><span class="sxs-lookup"><span data-stu-id="24890-570">ReqRefType</span></span>|
|<span data-ttu-id="24890-571">ReqRefTypeShort</span><span class="sxs-lookup"><span data-stu-id="24890-571">ReqRefTypeShort</span></span>|
|<span data-ttu-id="24890-572">ReqRefTypeTrunc</span><span class="sxs-lookup"><span data-stu-id="24890-572">ReqRefTypeTrunc</span></span>|
|<span data-ttu-id="24890-573">ReqTraceMessageType</span><span class="sxs-lookup"><span data-stu-id="24890-573">ReqTraceMessageType</span></span>|
|<span data-ttu-id="24890-574">ReqTransFuturesActionPartType</span><span class="sxs-lookup"><span data-stu-id="24890-574">ReqTransFuturesActionPartType</span></span>|
|<span data-ttu-id="24890-575">ReturnCodeType</span><span class="sxs-lookup"><span data-stu-id="24890-575">ReturnCodeType</span></span>|
|<span data-ttu-id="24890-576">ReturnCycleTimeScope</span><span class="sxs-lookup"><span data-stu-id="24890-576">ReturnCycleTimeScope</span></span>|
|<span data-ttu-id="24890-577">ReturnReasonCodeDispExtended</span><span class="sxs-lookup"><span data-stu-id="24890-577">ReturnReasonCodeDispExtended</span></span>|
|<span data-ttu-id="24890-578">ReturnReasonDispCode</span><span class="sxs-lookup"><span data-stu-id="24890-578">ReturnReasonDispCode</span></span>|
|<span data-ttu-id="24890-579">ReturnUpdateAction</span><span class="sxs-lookup"><span data-stu-id="24890-579">ReturnUpdateAction</span></span>|
|<span data-ttu-id="24890-580">RouteFormula</span><span class="sxs-lookup"><span data-stu-id="24890-580">RouteFormula</span></span>|
|<span data-ttu-id="24890-581">RouteOprPriority</span><span class="sxs-lookup"><span data-stu-id="24890-581">RouteOprPriority</span></span>|
|<span data-ttu-id="24890-582">SalesBasketType</span><span class="sxs-lookup"><span data-stu-id="24890-582">SalesBasketType</span></span>|
|<span data-ttu-id="24890-583">SalesBatch</span><span class="sxs-lookup"><span data-stu-id="24890-583">SalesBatch</span></span>|
|<span data-ttu-id="24890-584">SalesCheckForPickup</span><span class="sxs-lookup"><span data-stu-id="24890-584">SalesCheckForPickup</span></span>|
|<span data-ttu-id="24890-585">SalesCheckQtyCachKey</span><span class="sxs-lookup"><span data-stu-id="24890-585">SalesCheckQtyCachKey</span></span>|
|<span data-ttu-id="24890-586">SalesDeliveryTimeState</span><span class="sxs-lookup"><span data-stu-id="24890-586">SalesDeliveryTimeState</span></span>|
|<span data-ttu-id="24890-587">SalesDocumentTimezonePreference</span><span class="sxs-lookup"><span data-stu-id="24890-587">SalesDocumentTimezonePreference</span></span>|
|<span data-ttu-id="24890-588">SalesPriceDateType</span><span class="sxs-lookup"><span data-stu-id="24890-588">SalesPriceDateType</span></span>|
|<span data-ttu-id="24890-589">SalesPriceModelBasic</span><span class="sxs-lookup"><span data-stu-id="24890-589">SalesPriceModelBasic</span></span>|
|<span data-ttu-id="24890-590">SalesPurchCopy</span><span class="sxs-lookup"><span data-stu-id="24890-590">SalesPurchCopy</span></span>|
|<span data-ttu-id="24890-591">SalesPurchCycleAction</span><span class="sxs-lookup"><span data-stu-id="24890-591">SalesPurchCycleAction</span></span>|
|<span data-ttu-id="24890-592">SalesPurchGroup</span><span class="sxs-lookup"><span data-stu-id="24890-592">SalesPurchGroup</span></span>|
|<span data-ttu-id="24890-593">SalesPurchParmCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="24890-593">SalesPurchParmCleanUpMode</span></span>|
|<span data-ttu-id="24890-594">SalesQuotationFilter</span><span class="sxs-lookup"><span data-stu-id="24890-594">SalesQuotationFilter</span></span>|
|<span data-ttu-id="24890-595">SalesQuotationLinkToProject</span><span class="sxs-lookup"><span data-stu-id="24890-595">SalesQuotationLinkToProject</span></span>|
|<span data-ttu-id="24890-596">SalesQuotationListPage</span><span class="sxs-lookup"><span data-stu-id="24890-596">SalesQuotationListPage</span></span>|
|<span data-ttu-id="24890-597">SalesQuotationPriceConversion</span><span class="sxs-lookup"><span data-stu-id="24890-597">SalesQuotationPriceConversion</span></span>|
|<span data-ttu-id="24890-598">SalesQuotationPriceSimResult</span><span class="sxs-lookup"><span data-stu-id="24890-598">SalesQuotationPriceSimResult</span></span>|
|<span data-ttu-id="24890-599">SalesQuotationTypeListPage</span><span class="sxs-lookup"><span data-stu-id="24890-599">SalesQuotationTypeListPage</span></span>|
|<span data-ttu-id="24890-600">SalesShipping</span><span class="sxs-lookup"><span data-stu-id="24890-600">SalesShipping</span></span>|
|<span data-ttu-id="24890-601">SalesSourcingOrigin</span><span class="sxs-lookup"><span data-stu-id="24890-601">SalesSourcingOrigin</span></span>|
|<span data-ttu-id="24890-602">SalesStatus</span><span class="sxs-lookup"><span data-stu-id="24890-602">SalesStatus</span></span>|
|<span data-ttu-id="24890-603">SalesTableFormId</span><span class="sxs-lookup"><span data-stu-id="24890-603">SalesTableFormId</span></span>|
|<span data-ttu-id="24890-604">SalesTableListPage</span><span class="sxs-lookup"><span data-stu-id="24890-604">SalesTableListPage</span></span>|
|<span data-ttu-id="24890-605">SalesTableMode</span><span class="sxs-lookup"><span data-stu-id="24890-605">SalesTableMode</span></span>|
|<span data-ttu-id="24890-606">SalesType</span><span class="sxs-lookup"><span data-stu-id="24890-606">SalesType</span></span>|
|<span data-ttu-id="24890-607">SalesUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-607">SalesUpdate</span></span>|
|<span data-ttu-id="24890-608">ShipCarrierDlvType</span><span class="sxs-lookup"><span data-stu-id="24890-608">ShipCarrierDlvType</span></span>|
|<span data-ttu-id="24890-609">ShipCarrierFreightApplied</span><span class="sxs-lookup"><span data-stu-id="24890-609">ShipCarrierFreightApplied</span></span>|
|<span data-ttu-id="24890-610">ShipCarrierMkUpFreight</span><span class="sxs-lookup"><span data-stu-id="24890-610">ShipCarrierMkUpFreight</span></span>|
|<span data-ttu-id="24890-611">SMAInvoiceProjectSelection</span><span class="sxs-lookup"><span data-stu-id="24890-611">SMAInvoiceProjectSelection</span></span>|
|<span data-ttu-id="24890-612">SMAItemSetupType</span><span class="sxs-lookup"><span data-stu-id="24890-612">SMAItemSetupType</span></span>|
|<span data-ttu-id="24890-613">SMAProjectSelection</span><span class="sxs-lookup"><span data-stu-id="24890-613">SMAProjectSelection</span></span>|
|<span data-ttu-id="24890-614">SMAReasonType</span><span class="sxs-lookup"><span data-stu-id="24890-614">SMAReasonType</span></span>|
|<span data-ttu-id="24890-615">SMAServiceBOMChangeAction</span><span class="sxs-lookup"><span data-stu-id="24890-615">SMAServiceBOMChangeAction</span></span>|
|<span data-ttu-id="24890-616">SMAServiceFunctionType</span><span class="sxs-lookup"><span data-stu-id="24890-616">SMAServiceFunctionType</span></span>|
|<span data-ttu-id="24890-617">SMAServiceLevelAgreementLogType</span><span class="sxs-lookup"><span data-stu-id="24890-617">SMAServiceLevelAgreementLogType</span></span>|
|<span data-ttu-id="24890-618">SMAServiceOrderActionType</span><span class="sxs-lookup"><span data-stu-id="24890-618">SMAServiceOrderActionType</span></span>|
|<span data-ttu-id="24890-619">SMAServiceOrderFilter</span><span class="sxs-lookup"><span data-stu-id="24890-619">SMAServiceOrderFilter</span></span>|
|<span data-ttu-id="24890-620">SMAServiceOrderOrigin</span><span class="sxs-lookup"><span data-stu-id="24890-620">SMAServiceOrderOrigin</span></span>|
|<span data-ttu-id="24890-621">SMAServiceOrderProgress</span><span class="sxs-lookup"><span data-stu-id="24890-621">SMAServiceOrderProgress</span></span>|
|<span data-ttu-id="24890-622">SMAServiceTaskTitleOption</span><span class="sxs-lookup"><span data-stu-id="24890-622">SMAServiceTaskTitleOption</span></span>|
|<span data-ttu-id="24890-623">SMASubscriptionPeriodType</span><span class="sxs-lookup"><span data-stu-id="24890-623">SMASubscriptionPeriodType</span></span>|
|<span data-ttu-id="24890-624">SMAWizardCreateType</span><span class="sxs-lookup"><span data-stu-id="24890-624">SMAWizardCreateType</span></span>|
|<span data-ttu-id="24890-625">smmAccountNumToCreate</span><span class="sxs-lookup"><span data-stu-id="24890-625">smmAccountNumToCreate</span></span>|
|<span data-ttu-id="24890-626">smmActivityParentType</span><span class="sxs-lookup"><span data-stu-id="24890-626">smmActivityParentType</span></span>|
|<span data-ttu-id="24890-627">smmAppointmentNThInstance</span><span class="sxs-lookup"><span data-stu-id="24890-627">smmAppointmentNThInstance</span></span>|
|<span data-ttu-id="24890-628">smmBusinessRelationsListFilter</span><span class="sxs-lookup"><span data-stu-id="24890-628">smmBusinessRelationsListFilter</span></span>|
|<span data-ttu-id="24890-629">smmBusRelTypeSourceTable</span><span class="sxs-lookup"><span data-stu-id="24890-629">smmBusRelTypeSourceTable</span></span>|
|<span data-ttu-id="24890-630">smmCampaignBroadcastType</span><span class="sxs-lookup"><span data-stu-id="24890-630">smmCampaignBroadcastType</span></span>|
|<span data-ttu-id="24890-631">smmCampaignProjectJournalType</span><span class="sxs-lookup"><span data-stu-id="24890-631">smmCampaignProjectJournalType</span></span>|
|<span data-ttu-id="24890-632">smmCampaignResponse</span><span class="sxs-lookup"><span data-stu-id="24890-632">smmCampaignResponse</span></span>|
|<span data-ttu-id="24890-633">smmCampaignsListFilter</span><span class="sxs-lookup"><span data-stu-id="24890-633">smmCampaignsListFilter</span></span>|
|<span data-ttu-id="24890-634">smmContactsListFilter</span><span class="sxs-lookup"><span data-stu-id="24890-634">smmContactsListFilter</span></span>|
|<span data-ttu-id="24890-635">smmCreateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="24890-635">smmCreateOpportunityOptions</span></span>|
|<span data-ttu-id="24890-636">smmDisplayEMailInOutlook</span><span class="sxs-lookup"><span data-stu-id="24890-636">smmDisplayEMailInOutlook</span></span>|
|<span data-ttu-id="24890-637">smmDragDropObjectType</span><span class="sxs-lookup"><span data-stu-id="24890-637">smmDragDropObjectType</span></span>|
|<span data-ttu-id="24890-638">smmDupMethods</span><span class="sxs-lookup"><span data-stu-id="24890-638">smmDupMethods</span></span>|
|<span data-ttu-id="24890-639">smmEMailSMS</span><span class="sxs-lookup"><span data-stu-id="24890-639">smmEMailSMS</span></span>|
|<span data-ttu-id="24890-640">smmEntityToCreate</span><span class="sxs-lookup"><span data-stu-id="24890-640">smmEntityToCreate</span></span>|
|<span data-ttu-id="24890-641">smmFieldDelimiters</span><span class="sxs-lookup"><span data-stu-id="24890-641">smmFieldDelimiters</span></span>|
|<span data-ttu-id="24890-642">smmLeadsListFilter</span><span class="sxs-lookup"><span data-stu-id="24890-642">smmLeadsListFilter</span></span>|
|<span data-ttu-id="24890-643">smmLogType</span><span class="sxs-lookup"><span data-stu-id="24890-643">smmLogType</span></span>|
|<span data-ttu-id="24890-644">smmOpportunitiesListFilter</span><span class="sxs-lookup"><span data-stu-id="24890-644">smmOpportunitiesListFilter</span></span>|
|<span data-ttu-id="24890-645">smmOpportunityAssociation</span><span class="sxs-lookup"><span data-stu-id="24890-645">smmOpportunityAssociation</span></span>|
|<span data-ttu-id="24890-646">smmOutlookContactDeleteAction</span><span class="sxs-lookup"><span data-stu-id="24890-646">smmOutlookContactDeleteAction</span></span>|
|<span data-ttu-id="24890-647">smmOutlookRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="24890-647">smmOutlookRecurrenceType</span></span>|
|<span data-ttu-id="24890-648">smmOutlookSyncPrinciple</span><span class="sxs-lookup"><span data-stu-id="24890-648">smmOutlookSyncPrinciple</span></span>|
|<span data-ttu-id="24890-649">smmOutlookUpdateAction</span><span class="sxs-lookup"><span data-stu-id="24890-649">smmOutlookUpdateAction</span></span>|
|<span data-ttu-id="24890-650">smmProjectNewExisting</span><span class="sxs-lookup"><span data-stu-id="24890-650">smmProjectNewExisting</span></span>|
|<span data-ttu-id="24890-651">smmQuotationAccountType</span><span class="sxs-lookup"><span data-stu-id="24890-651">smmQuotationAccountType</span></span>|
|<span data-ttu-id="24890-652">smmQuotationStatus</span><span class="sxs-lookup"><span data-stu-id="24890-652">smmQuotationStatus</span></span>|
|<span data-ttu-id="24890-653">smmRecordDelimiters</span><span class="sxs-lookup"><span data-stu-id="24890-653">smmRecordDelimiters</span></span>|
|<span data-ttu-id="24890-654">smmSalesUnitMemberRelation</span><span class="sxs-lookup"><span data-stu-id="24890-654">smmSalesUnitMemberRelation</span></span>|
|<span data-ttu-id="24890-655">SmmSourceTypeList</span><span class="sxs-lookup"><span data-stu-id="24890-655">SmmSourceTypeList</span></span>|
|<span data-ttu-id="24890-656">smmSwotType</span><span class="sxs-lookup"><span data-stu-id="24890-656">smmSwotType</span></span>|
|<span data-ttu-id="24890-657">smmTransLogUpdateAction</span><span class="sxs-lookup"><span data-stu-id="24890-657">smmTransLogUpdateAction</span></span>|
|<span data-ttu-id="24890-658">smmUpdateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="24890-658">smmUpdateOpportunityOptions</span></span>|
|<span data-ttu-id="24890-659">smmWarningError</span><span class="sxs-lookup"><span data-stu-id="24890-659">smmWarningError</span></span>|
|<span data-ttu-id="24890-660">SMAActiveAll</span><span class="sxs-lookup"><span data-stu-id="24890-660">SMAActiveAll</span></span>|
|<span data-ttu-id="24890-661">SMAAgreementFilter</span><span class="sxs-lookup"><span data-stu-id="24890-661">SMAAgreementFilter</span></span>|
|<span data-ttu-id="24890-662">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="24890-662">SMAAgreementTableListPageType</span></span>|
|<span data-ttu-id="24890-663">TAMCustRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="24890-663">TAMCustRebateApprovalStatus</span></span>|
|<span data-ttu-id="24890-664">TAMFundStatus</span><span class="sxs-lookup"><span data-stu-id="24890-664">TAMFundStatus</span></span>|
|<span data-ttu-id="24890-665">TAMFundType</span><span class="sxs-lookup"><span data-stu-id="24890-665">TAMFundType</span></span>|
|<span data-ttu-id="24890-666">TAMPromoCustomerType</span><span class="sxs-lookup"><span data-stu-id="24890-666">TAMPromoCustomerType</span></span>|
|<span data-ttu-id="24890-667">TAMPromoMerchEvent</span><span class="sxs-lookup"><span data-stu-id="24890-667">TAMPromoMerchEvent</span></span>|
|<span data-ttu-id="24890-668">TAMPromoMgmtApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="24890-668">TAMPromoMgmtApprovalStatus</span></span>|
|<span data-ttu-id="24890-669">TAMPromotionDate</span><span class="sxs-lookup"><span data-stu-id="24890-669">TAMPromotionDate</span></span>|
|<span data-ttu-id="24890-670">TAMPromotionMode</span><span class="sxs-lookup"><span data-stu-id="24890-670">TAMPromotionMode</span></span>|
|<span data-ttu-id="24890-671">TAMRebateCustInclusive</span><span class="sxs-lookup"><span data-stu-id="24890-671">TAMRebateCustInclusive</span></span>|
|<span data-ttu-id="24890-672">TAMRebateLineBreakType</span><span class="sxs-lookup"><span data-stu-id="24890-672">TAMRebateLineBreakType</span></span>|
|<span data-ttu-id="24890-673">TAMRebateStatus</span><span class="sxs-lookup"><span data-stu-id="24890-673">TAMRebateStatus</span></span>|
|<span data-ttu-id="24890-674">TAMRebateUnitType</span><span class="sxs-lookup"><span data-stu-id="24890-674">TAMRebateUnitType</span></span>|
|<span data-ttu-id="24890-675">TAMRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="24890-675">TAMRebateUOMOption</span></span>|
|<span data-ttu-id="24890-676">TAMVendRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="24890-676">TAMVendRebateApprovalStatus</span></span>|
|<span data-ttu-id="24890-677">TAMVendRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="24890-677">TAMVendRebateCalcDateType</span></span>|
|<span data-ttu-id="24890-678">TAMVendRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="24890-678">TAMVendRebateTakenFrom</span></span>|
|<span data-ttu-id="24890-679">TAMVendRebateTransactionType</span><span class="sxs-lookup"><span data-stu-id="24890-679">TAMVendRebateTransactionType</span></span>|
|<span data-ttu-id="24890-680">TaxModuleType</span><span class="sxs-lookup"><span data-stu-id="24890-680">TaxModuleType</span></span>|
|<span data-ttu-id="24890-681">TaxSourceType</span><span class="sxs-lookup"><span data-stu-id="24890-681">TaxSourceType</span></span>|
|<span data-ttu-id="24890-682">TMSAccessorialAssignmentLevel</span><span class="sxs-lookup"><span data-stu-id="24890-682">TMSAccessorialAssignmentLevel</span></span>|
|<span data-ttu-id="24890-683">TMSAccessorialAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="24890-683">TMSAccessorialAssignmentTarget</span></span>|
|<span data-ttu-id="24890-684">TMSAccessorialDeliveryType</span><span class="sxs-lookup"><span data-stu-id="24890-684">TMSAccessorialDeliveryType</span></span>|
|<span data-ttu-id="24890-685">TMSAccessorialType</span><span class="sxs-lookup"><span data-stu-id="24890-685">TMSAccessorialType</span></span>|
|<span data-ttu-id="24890-686">TMSAppointmentAlert</span><span class="sxs-lookup"><span data-stu-id="24890-686">TMSAppointmentAlert</span></span>|
|<span data-ttu-id="24890-687">TMSDiscountResultType</span><span class="sxs-lookup"><span data-stu-id="24890-687">TMSDiscountResultType</span></span>|
|<span data-ttu-id="24890-688">TMSDiscountType</span><span class="sxs-lookup"><span data-stu-id="24890-688">TMSDiscountType</span></span>|
|<span data-ttu-id="24890-689">TMSFeeType</span><span class="sxs-lookup"><span data-stu-id="24890-689">TMSFeeType</span></span>|
|<span data-ttu-id="24890-690">TMSFreightBillMatchStatus</span><span class="sxs-lookup"><span data-stu-id="24890-690">TMSFreightBillMatchStatus</span></span>|
|<span data-ttu-id="24890-691">TMSFreightBillReconcileType</span><span class="sxs-lookup"><span data-stu-id="24890-691">TMSFreightBillReconcileType</span></span>|
|<span data-ttu-id="24890-692">TMSFwkErrorType</span><span class="sxs-lookup"><span data-stu-id="24890-692">TMSFwkErrorType</span></span>|
|<span data-ttu-id="24890-693">TMSHubPosition</span><span class="sxs-lookup"><span data-stu-id="24890-693">TMSHubPosition</span></span>|
|<span data-ttu-id="24890-694">TMSInvoiceAccountType</span><span class="sxs-lookup"><span data-stu-id="24890-694">TMSInvoiceAccountType</span></span>|
|<span data-ttu-id="24890-695">TMSLineType</span><span class="sxs-lookup"><span data-stu-id="24890-695">TMSLineType</span></span>|
|<span data-ttu-id="24890-696">TMSLoadBuildSessionState</span><span class="sxs-lookup"><span data-stu-id="24890-696">TMSLoadBuildSessionState</span></span>|
|<span data-ttu-id="24890-697">TMSLoadTender</span><span class="sxs-lookup"><span data-stu-id="24890-697">TMSLoadTender</span></span>|
|<span data-ttu-id="24890-698">TMSLookupType</span><span class="sxs-lookup"><span data-stu-id="24890-698">TMSLookupType</span></span>|
|<span data-ttu-id="24890-699">TMSNumberSequenceType</span><span class="sxs-lookup"><span data-stu-id="24890-699">TMSNumberSequenceType</span></span>|
|<span data-ttu-id="24890-700">TMSOverrideLocationType</span><span class="sxs-lookup"><span data-stu-id="24890-700">TMSOverrideLocationType</span></span>|
|<span data-ttu-id="24890-701">TMSRecurrenceDays</span><span class="sxs-lookup"><span data-stu-id="24890-701">TMSRecurrenceDays</span></span>|
|<span data-ttu-id="24890-702">TMSRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="24890-702">TMSRecurrenceType</span></span>|
|<span data-ttu-id="24890-703">TMSRecurrenceWeeks</span><span class="sxs-lookup"><span data-stu-id="24890-703">TMSRecurrenceWeeks</span></span>|
|<span data-ttu-id="24890-704">TMSResponsibleForPayment</span><span class="sxs-lookup"><span data-stu-id="24890-704">TMSResponsibleForPayment</span></span>|
|<span data-ttu-id="24890-705">TMSRouteStatus</span><span class="sxs-lookup"><span data-stu-id="24890-705">TMSRouteStatus</span></span>|
|<span data-ttu-id="24890-706">TMSSalesPurchTransfer</span><span class="sxs-lookup"><span data-stu-id="24890-706">TMSSalesPurchTransfer</span></span>|
|<span data-ttu-id="24890-707">TMSTableRef</span><span class="sxs-lookup"><span data-stu-id="24890-707">TMSTableRef</span></span>|
|<span data-ttu-id="24890-708">TMSTransportationType</span><span class="sxs-lookup"><span data-stu-id="24890-708">TMSTransportationType</span></span>|
|<span data-ttu-id="24890-709">TMSTransportRefType</span><span class="sxs-lookup"><span data-stu-id="24890-709">TMSTransportRefType</span></span>|
|<span data-ttu-id="24890-710">TMSTransportTypeFilter</span><span class="sxs-lookup"><span data-stu-id="24890-710">TMSTransportTypeFilter</span></span>|
|<span data-ttu-id="24890-711">TMSUOM</span><span class="sxs-lookup"><span data-stu-id="24890-711">TMSUOM</span></span>|
|<span data-ttu-id="24890-712">TMSZoneType</span><span class="sxs-lookup"><span data-stu-id="24890-712">TMSZoneType</span></span>|
|<span data-ttu-id="24890-713">TradeCurencyConversion</span><span class="sxs-lookup"><span data-stu-id="24890-713">TradeCurencyConversion</span></span>|
|<span data-ttu-id="24890-714">TradeLineDlvType</span><span class="sxs-lookup"><span data-stu-id="24890-714">TradeLineDlvType</span></span>|
|<span data-ttu-id="24890-715">TradeNonStockedConversionChangeType</span><span class="sxs-lookup"><span data-stu-id="24890-715">TradeNonStockedConversionChangeType</span></span>|
|<span data-ttu-id="24890-716">TradeNonStockedConversionIssue</span><span class="sxs-lookup"><span data-stu-id="24890-716">TradeNonStockedConversionIssue</span></span>|
|<span data-ttu-id="24890-717">TradeNonStockedConversionResolveUndo</span><span class="sxs-lookup"><span data-stu-id="24890-717">TradeNonStockedConversionResolveUndo</span></span>|
|<span data-ttu-id="24890-718">TradePrintType</span><span class="sxs-lookup"><span data-stu-id="24890-718">TradePrintType</span></span>|
|<span data-ttu-id="24890-719">TradeTable2LineUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-719">TradeTable2LineUpdate</span></span>|
|<span data-ttu-id="24890-720">VendNotificationCategorySelection</span><span class="sxs-lookup"><span data-stu-id="24890-720">VendNotificationCategorySelection</span></span>|
|<span data-ttu-id="24890-721">VendNotificationStatus</span><span class="sxs-lookup"><span data-stu-id="24890-721">VendNotificationStatus</span></span>|
|<span data-ttu-id="24890-722">VendPackingSlipTransTimeStatus</span><span class="sxs-lookup"><span data-stu-id="24890-722">VendPackingSlipTransTimeStatus</span></span>|
|<span data-ttu-id="24890-723">VendRequestCompanyType</span><span class="sxs-lookup"><span data-stu-id="24890-723">VendRequestCompanyType</span></span>|
|<span data-ttu-id="24890-724">VendRequestOriginatedByType</span><span class="sxs-lookup"><span data-stu-id="24890-724">VendRequestOriginatedByType</span></span>|
|<span data-ttu-id="24890-725">VendRequestQuestionnairesCompleted</span><span class="sxs-lookup"><span data-stu-id="24890-725">VendRequestQuestionnairesCompleted</span></span>|
|<span data-ttu-id="24890-726">VendRequestRoleType</span><span class="sxs-lookup"><span data-stu-id="24890-726">VendRequestRoleType</span></span>|
|<span data-ttu-id="24890-727">VendReviewRatingScore</span><span class="sxs-lookup"><span data-stu-id="24890-727">VendReviewRatingScore</span></span>|
|<span data-ttu-id="24890-728">VersioningAction</span><span class="sxs-lookup"><span data-stu-id="24890-728">VersioningAction</span></span>|
|<span data-ttu-id="24890-729">WHSAllowMaterialOverPick</span><span class="sxs-lookup"><span data-stu-id="24890-729">WHSAllowMaterialOverPick</span></span>|
|<span data-ttu-id="24890-730">WHSApplicableDemand</span><span class="sxs-lookup"><span data-stu-id="24890-730">WHSApplicableDemand</span></span>|
|<span data-ttu-id="24890-731">WHSAutoReleaseContainerAtContainerClose</span><span class="sxs-lookup"><span data-stu-id="24890-731">WHSAutoReleaseContainerAtContainerClose</span></span>|
|<span data-ttu-id="24890-732">WHSAutoReleaseOrderType</span><span class="sxs-lookup"><span data-stu-id="24890-732">WHSAutoReleaseOrderType</span></span>|
|<span data-ttu-id="24890-733">WHSBreakCluster</span><span class="sxs-lookup"><span data-stu-id="24890-733">WHSBreakCluster</span></span>|
|<span data-ttu-id="24890-734">WHSContainerizationQueryType</span><span class="sxs-lookup"><span data-stu-id="24890-734">WHSContainerizationQueryType</span></span>|
|<span data-ttu-id="24890-735">WHSContainerPackingStrategy</span><span class="sxs-lookup"><span data-stu-id="24890-735">WHSContainerPackingStrategy</span></span>|
|<span data-ttu-id="24890-736">WHSContainerTableFormViewType</span><span class="sxs-lookup"><span data-stu-id="24890-736">WHSContainerTableFormViewType</span></span>|
|<span data-ttu-id="24890-737">WHSCrossDockFulfillmentStrategy</span><span class="sxs-lookup"><span data-stu-id="24890-737">WHSCrossDockFulfillmentStrategy</span></span>|
|<span data-ttu-id="24890-738">WHSCustJourType</span><span class="sxs-lookup"><span data-stu-id="24890-738">WHSCustJourType</span></span>|
|<span data-ttu-id="24890-739">WHSCycleCountPlanStatus</span><span class="sxs-lookup"><span data-stu-id="24890-739">WHSCycleCountPlanStatus</span></span>|
|<span data-ttu-id="24890-740">WHSDefaultDataField</span><span class="sxs-lookup"><span data-stu-id="24890-740">WHSDefaultDataField</span></span>|
|<span data-ttu-id="24890-741">WHSFilterModule</span><span class="sxs-lookup"><span data-stu-id="24890-741">WHSFilterModule</span></span>|
|<span data-ttu-id="24890-742">WHSHistoryEvent</span><span class="sxs-lookup"><span data-stu-id="24890-742">WHSHistoryEvent</span></span>|
|<span data-ttu-id="24890-743">WHSLoadPlanning</span><span class="sxs-lookup"><span data-stu-id="24890-743">WHSLoadPlanning</span></span>|
|<span data-ttu-id="24890-744">WHSLoadPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="24890-744">WHSLoadPostMethodsBase</span></span>|
|<span data-ttu-id="24890-745">WhsLoadReplenishment</span><span class="sxs-lookup"><span data-stu-id="24890-745">WhsLoadReplenishment</span></span>|
|<span data-ttu-id="24890-746">WHSLoadTable</span><span class="sxs-lookup"><span data-stu-id="24890-746">WHSLoadTable</span></span>|
|<span data-ttu-id="24890-747">WHSLocDirStrategy</span><span class="sxs-lookup"><span data-stu-id="24890-747">WHSLocDirStrategy</span></span>|
|<span data-ttu-id="24890-748">WHSLPAssignment</span><span class="sxs-lookup"><span data-stu-id="24890-748">WHSLPAssignment</span></span>|
|<span data-ttu-id="24890-749">WHSLPWFilterType</span><span class="sxs-lookup"><span data-stu-id="24890-749">WHSLPWFilterType</span></span>|
|<span data-ttu-id="24890-750">WHSManifestAt</span><span class="sxs-lookup"><span data-stu-id="24890-750">WHSManifestAt</span></span>|
|<span data-ttu-id="24890-751">WHSManifestRequirementContainerGroup</span><span class="sxs-lookup"><span data-stu-id="24890-751">WHSManifestRequirementContainerGroup</span></span>|
|<span data-ttu-id="24890-752">WHSMenuItemDirectedBy</span><span class="sxs-lookup"><span data-stu-id="24890-752">WHSMenuItemDirectedBy</span></span>|
|<span data-ttu-id="24890-753">WHSMixedLPReceivingMode</span><span class="sxs-lookup"><span data-stu-id="24890-753">WHSMixedLPReceivingMode</span></span>|
|<span data-ttu-id="24890-754">WHSMixingLogicTables</span><span class="sxs-lookup"><span data-stu-id="24890-754">WHSMixingLogicTables</span></span>|
|<span data-ttu-id="24890-755">WHSMobileAppPagePattern</span><span class="sxs-lookup"><span data-stu-id="24890-755">WHSMobileAppPagePattern</span></span>|
|<span data-ttu-id="24890-756">WHSOriginType</span><span class="sxs-lookup"><span data-stu-id="24890-756">WHSOriginType</span></span>|
|<span data-ttu-id="24890-757">WHSPickOldestBatch</span><span class="sxs-lookup"><span data-stu-id="24890-757">WHSPickOldestBatch</span></span>|
|<span data-ttu-id="24890-758">WHSPostMethodBaseKanban</span><span class="sxs-lookup"><span data-stu-id="24890-758">WHSPostMethodBaseKanban</span></span>|
|<span data-ttu-id="24890-759">WHSPostMethodBaseKanbanOptional</span><span class="sxs-lookup"><span data-stu-id="24890-759">WHSPostMethodBaseKanbanOptional</span></span>|
|<span data-ttu-id="24890-760">WHSPostMethodBaseOptional</span><span class="sxs-lookup"><span data-stu-id="24890-760">WHSPostMethodBaseOptional</span></span>|
|<span data-ttu-id="24890-761">WHSPostMethodBaseProd</span><span class="sxs-lookup"><span data-stu-id="24890-761">WHSPostMethodBaseProd</span></span>|
|<span data-ttu-id="24890-762">WHSPostMethodBaseProdOptional</span><span class="sxs-lookup"><span data-stu-id="24890-762">WHSPostMethodBaseProdOptional</span></span>|
|<span data-ttu-id="24890-763">WHSPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="24890-763">WHSPostMethodsBase</span></span>|
|<span data-ttu-id="24890-764">WHSQtyPct</span><span class="sxs-lookup"><span data-stu-id="24890-764">WHSQtyPct</span></span>|
|<span data-ttu-id="24890-765">WHSReleaseQuantitySpecification</span><span class="sxs-lookup"><span data-stu-id="24890-765">WHSReleaseQuantitySpecification</span></span>|
|<span data-ttu-id="24890-766">WHSReplenishmentDependentWorkBlockingPolicy</span><span class="sxs-lookup"><span data-stu-id="24890-766">WHSReplenishmentDependentWorkBlockingPolicy</span></span>|
|<span data-ttu-id="24890-767">WHSReservationHierarchyLevelStrategyType</span><span class="sxs-lookup"><span data-stu-id="24890-767">WHSReservationHierarchyLevelStrategyType</span></span>|
|<span data-ttu-id="24890-768">WHSReservationStatus</span><span class="sxs-lookup"><span data-stu-id="24890-768">WHSReservationStatus</span></span>|
|<span data-ttu-id="24890-769">WHSUseFixedLocations</span><span class="sxs-lookup"><span data-stu-id="24890-769">WHSUseFixedLocations</span></span>|
|<span data-ttu-id="24890-770">WHSWorkActivity</span><span class="sxs-lookup"><span data-stu-id="24890-770">WHSWorkActivity</span></span>|
|<span data-ttu-id="24890-771">WHSWorkClusterStatus</span><span class="sxs-lookup"><span data-stu-id="24890-771">WHSWorkClusterStatus</span></span>|
|<span data-ttu-id="24890-772">WHSWorkCreationProcess</span><span class="sxs-lookup"><span data-stu-id="24890-772">WHSWorkCreationProcess</span></span>|
|<span data-ttu-id="24890-773">WHSWorkExceptionLogStatus</span><span class="sxs-lookup"><span data-stu-id="24890-773">WHSWorkExceptionLogStatus</span></span>|
|<span data-ttu-id="24890-774">WHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="24890-774">WHSWorkExecuteMode</span></span>|
|<span data-ttu-id="24890-775">WHSWorkListPageFilter</span><span class="sxs-lookup"><span data-stu-id="24890-775">WHSWorkListPageFilter</span></span>|
|<span data-ttu-id="24890-776">WHSWorkPrintOption</span><span class="sxs-lookup"><span data-stu-id="24890-776">WHSWorkPrintOption</span></span>|
|<span data-ttu-id="24890-777">WHSWorkPutFlow</span><span class="sxs-lookup"><span data-stu-id="24890-777">WHSWorkPutFlow</span></span>|
|<span data-ttu-id="24890-778">WHSWorkTransType</span><span class="sxs-lookup"><span data-stu-id="24890-778">WHSWorkTransType</span></span>|
|<span data-ttu-id="24890-779">WHSWorkType</span><span class="sxs-lookup"><span data-stu-id="24890-779">WHSWorkType</span></span>|
|<span data-ttu-id="24890-780">WHSWorkTypePickPut</span><span class="sxs-lookup"><span data-stu-id="24890-780">WHSWorkTypePickPut</span></span>|
|<span data-ttu-id="24890-781">WMSAutoAddStop</span><span class="sxs-lookup"><span data-stu-id="24890-781">WMSAutoAddStop</span></span>|
|<span data-ttu-id="24890-782">WMSFreightChargeTerms</span><span class="sxs-lookup"><span data-stu-id="24890-782">WMSFreightChargeTerms</span></span>|
|<span data-ttu-id="24890-783">WMSFreightCounted</span><span class="sxs-lookup"><span data-stu-id="24890-783">WMSFreightCounted</span></span>|
|<span data-ttu-id="24890-784">WMSHandlingType</span><span class="sxs-lookup"><span data-stu-id="24890-784">WMSHandlingType</span></span>|
|<span data-ttu-id="24890-785">WMSLocationType</span><span class="sxs-lookup"><span data-stu-id="24890-785">WMSLocationType</span></span>|
|<span data-ttu-id="24890-786">WMSPackageType</span><span class="sxs-lookup"><span data-stu-id="24890-786">WMSPackageType</span></span>|
|<span data-ttu-id="24890-787">WMSPalletMovementProcessing</span><span class="sxs-lookup"><span data-stu-id="24890-787">WMSPalletMovementProcessing</span></span>|
|<span data-ttu-id="24890-788">WMSPhysicalUpdateStatus</span><span class="sxs-lookup"><span data-stu-id="24890-788">WMSPhysicalUpdateStatus</span></span>|
|<span data-ttu-id="24890-789">WMSReceiptStatus</span><span class="sxs-lookup"><span data-stu-id="24890-789">WMSReceiptStatus</span></span>|
|<span data-ttu-id="24890-790">WMSReservationMethod</span><span class="sxs-lookup"><span data-stu-id="24890-790">WMSReservationMethod</span></span>|
|<span data-ttu-id="24890-791">WMSReservationMethodInternal</span><span class="sxs-lookup"><span data-stu-id="24890-791">WMSReservationMethodInternal</span></span>|
|<span data-ttu-id="24890-792">WMSShipmentStatus</span><span class="sxs-lookup"><span data-stu-id="24890-792">WMSShipmentStatus</span></span>|
|<span data-ttu-id="24890-793">WMSShipmentType</span><span class="sxs-lookup"><span data-stu-id="24890-793">WMSShipmentType</span></span>|
|<span data-ttu-id="24890-794">WMSSpaceUtilInconsistencyGroup</span><span class="sxs-lookup"><span data-stu-id="24890-794">WMSSpaceUtilInconsistencyGroup</span></span>|
|<span data-ttu-id="24890-795">WMSSpaceUtilShowBy</span><span class="sxs-lookup"><span data-stu-id="24890-795">WMSSpaceUtilShowBy</span></span>|
|<span data-ttu-id="24890-796">WMSSpaceUtilStorageLoadUnitType</span><span class="sxs-lookup"><span data-stu-id="24890-796">WMSSpaceUtilStorageLoadUnitType</span></span>|
|<span data-ttu-id="24890-797">WMSStoreAreaType</span><span class="sxs-lookup"><span data-stu-id="24890-797">WMSStoreAreaType</span></span>|
|<span data-ttu-id="24890-798">WMSTrailerLoaded</span><span class="sxs-lookup"><span data-stu-id="24890-798">WMSTrailerLoaded</span></span>|
|<span data-ttu-id="24890-799">WrkCtrActivityType</span><span class="sxs-lookup"><span data-stu-id="24890-799">WrkCtrActivityType</span></span>|
|<span data-ttu-id="24890-800">WrkCtrBulkResReqSearchType</span><span class="sxs-lookup"><span data-stu-id="24890-800">WrkCtrBulkResReqSearchType</span></span>|
|<span data-ttu-id="24890-801">WrkCtrCapacityType</span><span class="sxs-lookup"><span data-stu-id="24890-801">WrkCtrCapacityType</span></span>|
|<span data-ttu-id="24890-802">WrkCtrCapRefType</span><span class="sxs-lookup"><span data-stu-id="24890-802">WrkCtrCapRefType</span></span>|
|<span data-ttu-id="24890-803">WrkCtrCommitState</span><span class="sxs-lookup"><span data-stu-id="24890-803">WrkCtrCommitState</span></span>|
|<span data-ttu-id="24890-804">WrkCtrGroupWrkCtr</span><span class="sxs-lookup"><span data-stu-id="24890-804">WrkCtrGroupWrkCtr</span></span>|
|<span data-ttu-id="24890-805">WrkCtrSchedulerCommand</span><span class="sxs-lookup"><span data-stu-id="24890-805">WrkCtrSchedulerCommand</span></span>|
|<span data-ttu-id="24890-806">WrkCtrSchedulerConstraintType</span><span class="sxs-lookup"><span data-stu-id="24890-806">WrkCtrSchedulerConstraintType</span></span>|
|<span data-ttu-id="24890-807">WrkCtrSchedulerLoggerMode</span><span class="sxs-lookup"><span data-stu-id="24890-807">WrkCtrSchedulerLoggerMode</span></span>|
|<span data-ttu-id="24890-808">WrkCtrType</span><span class="sxs-lookup"><span data-stu-id="24890-808">WrkCtrType</span></span>|
|<span data-ttu-id="24890-809">WrkCtrTypeFilter</span><span class="sxs-lookup"><span data-stu-id="24890-809">WrkCtrTypeFilter</span></span>|

<span data-ttu-id="24890-810">以下の列挙型は削除され、拡張可能になりませんでした。</span><span class="sxs-lookup"><span data-stu-id="24890-810">These enumerations were removed, and not made extensible.</span></span>

| <span data-ttu-id="24890-811">削除された列挙型</span><span class="sxs-lookup"><span data-stu-id="24890-811">Enumeration removed</span></span> |
| --------------- |
|<span data-ttu-id="24890-812">BackorderLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="24890-812">BackorderLinesListPageMode</span></span>|
|<span data-ttu-id="24890-813">BackorderPurchLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="24890-813">BackorderPurchLinesListPageMode</span></span> |
|<span data-ttu-id="24890-814">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="24890-814">EcoResProductPerCompanyListPageType</span></span> |
|<span data-ttu-id="24890-815">ReturnTableListPageType</span><span class="sxs-lookup"><span data-stu-id="24890-815">ReturnTableListPageType</span></span> |
|<span data-ttu-id="24890-816">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="24890-816">SMAAgreementTableListPageType</span></span>|

<span data-ttu-id="24890-817">拡張可能な列挙型のサポートを改善するために、Foundation の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="24890-817">Foundation changes were made to improve support for extensible enumerations.</span></span> <span data-ttu-id="24890-818">**IsExtensible** が **はい** に設定されている列挙型については、**SysPlugin** フレームワークが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="24890-818">The **SysPlugin** framework was enabled for enumerations where **IsExtensible** is set to **Yes**.</span></span> <span data-ttu-id="24890-819">列挙型の新しい名前に基づく構文で、ビューが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="24890-819">Views were enabled with new name-based syntax for enumerations.</span></span>

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a><span data-ttu-id="24890-820">DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド</span><span class="sxs-lookup"><span data-stu-id="24890-820">Data manipulation methods that do not raise DataEvents or missing insert, update, delete pre- and post-data events</span></span>

<span data-ttu-id="24890-821">一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="24890-821">As a general practice, you use data methods on tables to raise events that can be used for extending the application.</span></span> <span data-ttu-id="24890-822">コード ベースは、必ずしもこのプラクティスに従っていませんでした。</span><span class="sxs-lookup"><span data-stu-id="24890-822">The code base has not always followed this practice.</span></span> <span data-ttu-id="24890-823">たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="24890-823">For example, the **doInsert**, **doUpdate**, and **doDelete** data methods and certain table implementations did not make a call to **super()** in the data method.</span></span>

<span data-ttu-id="24890-824">タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="24890-824">The **insert**, **update**, and **delete** methods on the type classes have been refactored.</span></span> <span data-ttu-id="24890-825">データ メソッドで **super()** が確実に呼び出されるように変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="24890-825">Changes were made so that **super()** is called more consistently in data methods.</span></span> <span data-ttu-id="24890-826">これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="24890-826">These changes enable extensions to be added to these methods, so that pre- and post-events are now available for extension.</span></span> <span data-ttu-id="24890-827">次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="24890-827">The tables where the **insert**, **update**, and **delete** events were enabled for extension are listed in the following table.</span></span>

| <span data-ttu-id="24890-828">テーブル</span><span class="sxs-lookup"><span data-stu-id="24890-828">Table</span></span> |
| -------------|
| <span data-ttu-id="24890-829">InventBlocking</span><span class="sxs-lookup"><span data-stu-id="24890-829">InventBlocking</span></span>|
| <span data-ttu-id="24890-830">InventTransferLine</span><span class="sxs-lookup"><span data-stu-id="24890-830">InventTransferLine</span></span>|
| <span data-ttu-id="24890-831">Kanban</span><span class="sxs-lookup"><span data-stu-id="24890-831">Kanban</span></span>|
| <span data-ttu-id="24890-832">KanbanJob</span><span class="sxs-lookup"><span data-stu-id="24890-832">KanbanJob</span></span>|
| <span data-ttu-id="24890-833">KanbanJobPickingList</span><span class="sxs-lookup"><span data-stu-id="24890-833">KanbanJobPickingList</span></span>|
| <span data-ttu-id="24890-834">MCRRoyaltyVendTable</span><span class="sxs-lookup"><span data-stu-id="24890-834">MCRRoyaltyVendTable</span></span>|
| <span data-ttu-id="24890-835">PdsRebateTable</span><span class="sxs-lookup"><span data-stu-id="24890-835">PdsRebateTable</span></span>|
| <span data-ttu-id="24890-836">PmfProdCoBy</span><span class="sxs-lookup"><span data-stu-id="24890-836">PmfProdCoBy</span></span>|
| <span data-ttu-id="24890-837">ProdBOM</span><span class="sxs-lookup"><span data-stu-id="24890-837">ProdBOM</span></span>|
| <span data-ttu-id="24890-838">ProdRoute</span><span class="sxs-lookup"><span data-stu-id="24890-838">ProdRoute</span></span>|
| <span data-ttu-id="24890-839">ProdTable</span><span class="sxs-lookup"><span data-stu-id="24890-839">ProdTable</span></span>|
| <span data-ttu-id="24890-840">PurchLine</span><span class="sxs-lookup"><span data-stu-id="24890-840">PurchLine</span></span>|
| <span data-ttu-id="24890-841">PurchRFQCaseLine</span><span class="sxs-lookup"><span data-stu-id="24890-841">PurchRFQCaseLine</span></span>|
| <span data-ttu-id="24890-842">PurchRFQCaseTable</span><span class="sxs-lookup"><span data-stu-id="24890-842">PurchRFQCaseTable</span></span>|
| <span data-ttu-id="24890-843">PurchRFQLine</span><span class="sxs-lookup"><span data-stu-id="24890-843">PurchRFQLine</span></span>|
| <span data-ttu-id="24890-844">PurchTable</span><span class="sxs-lookup"><span data-stu-id="24890-844">PurchTable</span></span>|
| <span data-ttu-id="24890-845">SalesLine</span><span class="sxs-lookup"><span data-stu-id="24890-845">SalesLine</span></span>|
| <span data-ttu-id="24890-846">SalesQuotationLine</span><span class="sxs-lookup"><span data-stu-id="24890-846">SalesQuotationLine</span></span>|
| <span data-ttu-id="24890-847">SalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="24890-847">SalesQuotationTable</span></span>|
| <span data-ttu-id="24890-848">SalesTable</span><span class="sxs-lookup"><span data-stu-id="24890-848">SalesTable</span></span>|
| <span data-ttu-id="24890-849">TAMVendRebateTable</span><span class="sxs-lookup"><span data-stu-id="24890-849">TAMVendRebateTable</span></span>|
| <span data-ttu-id="24890-850">WMSOrder</span><span class="sxs-lookup"><span data-stu-id="24890-850">WMSOrder</span></span>|
| <span data-ttu-id="24890-851">WMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="24890-851">WMSOrderTrans</span></span>|

## <a name="exposing-class-members"></a><span data-ttu-id="24890-852">クラス メンバーの公開</span><span class="sxs-lookup"><span data-stu-id="24890-852">Exposing class members</span></span>

<span data-ttu-id="24890-853">アクセス修飾子または新しい parm メソッドの変更の結果、追加のプライベート メンバーをカスタマイズに使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="24890-853">Additional private members are now available for customization as a result of the changes to the access modifier or new parm methods.</span></span> <span data-ttu-id="24890-854">コマンド チェーン プラットフォーム機能により、保護されたメソッドとメンバーへの拡張クラスのアクセスが有効になります。</span><span class="sxs-lookup"><span data-stu-id="24890-854">The chain of command platform feature enables extension class access to protected methods and members.</span></span> <span data-ttu-id="24890-855">コマンド チェーンの詳細については、「[拡張可能な X++: コマンド チェーン](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24890-855">For more information about chain of command, see [Extensible X++: Chain of Command](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/).</span></span>

| <span data-ttu-id="24890-856">メンバー</span><span class="sxs-lookup"><span data-stu-id="24890-856">Member</span></span> |
| -------------|
|<span data-ttu-id="24890-857">AssetPost.ledgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="24890-857">AssetPost.ledgerJournalTrans</span></span>|
|<span data-ttu-id="24890-858">クラス DimensionDerivationRule.ledgerDimensionAllocationList</span><span class="sxs-lookup"><span data-stu-id="24890-858">Class DimensionDerivationRule.ledgerDimensionAllocationList</span></span>|
|<span data-ttu-id="24890-859">クラス PurchInvoiceJournalCreate.purchTable</span><span class="sxs-lookup"><span data-stu-id="24890-859">Class PurchInvoiceJournalCreate.purchTable</span></span>|
|<span data-ttu-id="24890-860">クラス PurchTableType.purchTable</span><span class="sxs-lookup"><span data-stu-id="24890-860">Class PurchTableType.purchTable</span></span>|
|<span data-ttu-id="24890-861">クラス SalesInvoiceJournalPost.salesLine</span><span class="sxs-lookup"><span data-stu-id="24890-861">Class SalesInvoiceJournalPost.salesLine</span></span>|
|<span data-ttu-id="24890-862">クラス SalesQuotationLineType</span><span class="sxs-lookup"><span data-stu-id="24890-862">Class SalesQuotationLineType</span></span>|
|<span data-ttu-id="24890-863">クラス SalesQuotationTableType</span><span class="sxs-lookup"><span data-stu-id="24890-863">Class SalesQuotationTableType</span></span>|
|<span data-ttu-id="24890-864">クラス VendorInvoiceLineSourceDocLineItem.purchLine</span><span class="sxs-lookup"><span data-stu-id="24890-864">Class VendorInvoiceLineSourceDocLineItem.purchLine</span></span>|
|<span data-ttu-id="24890-865">CustCreditLimit.balanceTotalsCalculated</span><span class="sxs-lookup"><span data-stu-id="24890-865">CustCreditLimit.balanceTotalsCalculated</span></span>|
|<span data-ttu-id="24890-866">CustCreditLimit_SalesTable.salesTable</span><span class="sxs-lookup"><span data-stu-id="24890-866">CustCreditLimit_SalesTable.salesTable</span></span>|
|<span data-ttu-id="24890-867">フォーム LedgerJournalTransCustPaym.ledgerJournalEngine</span><span class="sxs-lookup"><span data-stu-id="24890-867">Form LedgerJournalTransCustPaym.ledgerJournalEngine</span></span>|
|<span data-ttu-id="24890-868">PurchLineType.purchLine</span><span class="sxs-lookup"><span data-stu-id="24890-868">PurchLineType.purchLine</span></span>|
|<span data-ttu-id="24890-869">PurchLineType.purchLine_orig</span><span class="sxs-lookup"><span data-stu-id="24890-869">PurchLineType.purchLine_orig</span></span>|
|<span data-ttu-id="24890-870">SalesLineType.salesLine</span><span class="sxs-lookup"><span data-stu-id="24890-870">SalesLineType.salesLine</span></span>|
|<span data-ttu-id="24890-871">SalesLineType.salesLine_orig</span><span class="sxs-lookup"><span data-stu-id="24890-871">SalesLineType.salesLine_orig</span></span>|
|<span data-ttu-id="24890-872">SalesTableType.checkSalesQty</span><span class="sxs-lookup"><span data-stu-id="24890-872">SalesTableType.checkSalesQty</span></span>|
|<span data-ttu-id="24890-873">SalesTableType.SalesTable_orig</span><span class="sxs-lookup"><span data-stu-id="24890-873">SalesTableType.SalesTable_orig</span></span>|
|<span data-ttu-id="24890-874">WHSControl.data</span><span class="sxs-lookup"><span data-stu-id="24890-874">WHSControl.data</span></span>|
|<span data-ttu-id="24890-875">WHSLocationDirective.targetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="24890-875">WHSLocationDirective.targetLicensePlateId</span></span>|

## <a name="construct-methods-with-throw-statements"></a><span data-ttu-id="24890-876">throw ステートメントを使用した construct メソッド</span><span class="sxs-lookup"><span data-stu-id="24890-876">Construct methods with throw statements</span></span>

<span data-ttu-id="24890-877">特定の型の実装が欠落していた場合、いくつかの **construct** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="24890-877">Some **construct** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="24890-878">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**construct** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="24890-878">This doesn't work well with extensibility, so to mitigate this, **construct** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="24890-879">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="24890-879">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="24890-880">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="24890-880">Object</span></span> |
| -------------|
|<span data-ttu-id="24890-881">BarcodeEAN128.string()</span><span class="sxs-lookup"><span data-stu-id="24890-881">BarcodeEAN128.string()</span></span>|
|<span data-ttu-id="24890-882">CustCreditLimit.Construct</span><span class="sxs-lookup"><span data-stu-id="24890-882">CustCreditLimit.Construct</span></span>|
|<span data-ttu-id="24890-883">FormLetterReport</span><span class="sxs-lookup"><span data-stu-id="24890-883">FormLetterReport</span></span>|
|<span data-ttu-id="24890-884">JournalStatic</span><span class="sxs-lookup"><span data-stu-id="24890-884">JournalStatic</span></span>|
|<span data-ttu-id="24890-885">MarkupAllocation</span><span class="sxs-lookup"><span data-stu-id="24890-885">MarkupAllocation</span></span>|
|<span data-ttu-id="24890-886">PurchTable2LineField</span><span class="sxs-lookup"><span data-stu-id="24890-886">PurchTable2LineField</span></span>|
|<span data-ttu-id="24890-887">SalesCalcTax</span><span class="sxs-lookup"><span data-stu-id="24890-887">SalesCalcTax</span></span>|
|<span data-ttu-id="24890-888">SalesEditLinesForm</span><span class="sxs-lookup"><span data-stu-id="24890-888">SalesEditLinesForm</span></span>|
|<span data-ttu-id="24890-889">SalesFormLetter</span><span class="sxs-lookup"><span data-stu-id="24890-889">SalesFormLetter</span></span>|
|<span data-ttu-id="24890-890">SalesFormLetterContract.newFromPackedVersion</span><span class="sxs-lookup"><span data-stu-id="24890-890">SalesFormLetterContract.newFromPackedVersion</span></span>|
|<span data-ttu-id="24890-891">SalesFormletterParmData.newData</span><span class="sxs-lookup"><span data-stu-id="24890-891">SalesFormletterParmData.newData</span></span>|
|<span data-ttu-id="24890-892">SalesQuantity</span><span class="sxs-lookup"><span data-stu-id="24890-892">SalesQuantity</span></span>|
|<span data-ttu-id="24890-893">SalesQuotationEditLinesForm.construct</span><span class="sxs-lookup"><span data-stu-id="24890-893">SalesQuotationEditLinesForm.construct</span></span>|
|<span data-ttu-id="24890-894">SalesSummaryFields</span><span class="sxs-lookup"><span data-stu-id="24890-894">SalesSummaryFields</span></span>|
|<span data-ttu-id="24890-895">SalesTable2LineField</span><span class="sxs-lookup"><span data-stu-id="24890-895">SalesTable2LineField</span></span>|
|<span data-ttu-id="24890-896">VendInvoiceTableToLineUpdate</span><span class="sxs-lookup"><span data-stu-id="24890-896">VendInvoiceTableToLineUpdate</span></span>|

## <a name="find-methods-with-throw-statements"></a><span data-ttu-id="24890-897">throw ステートメントを使用した find メソッド</span><span class="sxs-lookup"><span data-stu-id="24890-897">Find methods with throw statements</span></span>

<span data-ttu-id="24890-898">特定の型の実装が欠落していた場合、いくつかの **find** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="24890-898">Some **find** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="24890-899">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**find** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="24890-899">This does not work well with extensibility, so to mitigate this, **find** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="24890-900">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="24890-900">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="24890-901">メソッド</span><span class="sxs-lookup"><span data-stu-id="24890-901">Methods</span></span> |
| -------------|
|<span data-ttu-id="24890-902">JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="24890-902">JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="24890-903">JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="24890-903">JournalStatic.findJournalTableId</span></span>|

## <a name="methods-made-hookable"></a><span data-ttu-id="24890-904">フック可能なメソッド</span><span class="sxs-lookup"><span data-stu-id="24890-904">Methods made hookable</span></span>

<span data-ttu-id="24890-905">パブリックでない一部のメソッドおよびフック可能でない一部のメソッドについて、拡張性サポートが強化されました。</span><span class="sxs-lookup"><span data-stu-id="24890-905">Extensibility support has been extended for some methods that were not public and were not hookable.</span></span> <span data-ttu-id="24890-906">以下のメソッドはフック可能な動作で明示的に修飾されています。</span><span class="sxs-lookup"><span data-stu-id="24890-906">The following methods have been explicitly decorated with hookable behavior.</span></span>

| <span data-ttu-id="24890-907">メソッド</span><span class="sxs-lookup"><span data-stu-id="24890-907">Method</span></span> |
| -------------|
|<span data-ttu-id="24890-908">クラス CustVendReversePosting.updateCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="24890-908">Class CustVendReversePosting.updateCustVendTrans</span></span>|
|<span data-ttu-id="24890-909">クラス JournalTableData.construct</span><span class="sxs-lookup"><span data-stu-id="24890-909">Class JournalTableData.construct</span></span>|
|<span data-ttu-id="24890-910">クラス PriceDisc.makeKey</span><span class="sxs-lookup"><span data-stu-id="24890-910">Class PriceDisc.makeKey</span></span>|
|<span data-ttu-id="24890-911">クラス PurchInvoiceJournalCreate.initJournalHeader</span><span class="sxs-lookup"><span data-stu-id="24890-911">Class PurchInvoiceJournalCreate.initJournalHeader</span></span>|
|<span data-ttu-id="24890-912">クラス SalesInvoiceJournalPost.checkSourceLine</span><span class="sxs-lookup"><span data-stu-id="24890-912">Class SalesInvoiceJournalPost.checkSourceLine</span></span>|
|<span data-ttu-id="24890-913">クラス SalesInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="24890-913">Class SalesInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="24890-914">フォーム LedgerTransVoucher.addDynaLink</span><span class="sxs-lookup"><span data-stu-id="24890-914">Form LedgerTransVoucher.addDynaLink</span></span>|
|<span data-ttu-id="24890-915">ReqCalc.deleteItemRequirement</span><span class="sxs-lookup"><span data-stu-id="24890-915">ReqCalc.deleteItemRequirement</span></span>|
|<span data-ttu-id="24890-916">ReqCalc.initTransFromInventTrans</span><span class="sxs-lookup"><span data-stu-id="24890-916">ReqCalc.initTransFromInventTrans</span></span>|
|<span data-ttu-id="24890-917">ReqCalcForecastItemTable.deleteRequirement</span><span class="sxs-lookup"><span data-stu-id="24890-917">ReqCalcForecastItemTable.deleteRequirement</span></span>|
|<span data-ttu-id="24890-918">テーブル TmpCustVendTrans.createLineCreditLimit</span><span class="sxs-lookup"><span data-stu-id="24890-918">Table TmpCustVendTrans.createLineCreditLimit</span></span>|
|<span data-ttu-id="24890-919">テーブル TmpCustVendTrans.createLineCreditRemain</span><span class="sxs-lookup"><span data-stu-id="24890-919">Table TmpCustVendTrans.createLineCreditRemain</span></span>|
|<span data-ttu-id="24890-920">テーブル TmpCustVendTrans.createLineOrdered</span><span class="sxs-lookup"><span data-stu-id="24890-920">Table TmpCustVendTrans.createLineOrdered</span></span>|
|<span data-ttu-id="24890-921">テーブル TmpCustVendTrans.createLinePackingSlip</span><span class="sxs-lookup"><span data-stu-id="24890-921">Table TmpCustVendTrans.createLinePackingSlip</span></span>|
|<span data-ttu-id="24890-922">WHSLocationDirective.addRangeByTransType</span><span class="sxs-lookup"><span data-stu-id="24890-922">WHSLocationDirective.addRangeByTransType</span></span>|
|<span data-ttu-id="24890-923">WhsWorkCreate.createWorkLine</span><span class="sxs-lookup"><span data-stu-id="24890-923">WhsWorkCreate.createWorkLine</span></span>|

## <a name="inline-delegates"></a><span data-ttu-id="24890-924">インライン デリゲート</span><span class="sxs-lookup"><span data-stu-id="24890-924">Inline delegates</span></span>

<span data-ttu-id="24890-925">インライン デリゲートを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="24890-925">Inline delegates are now available.</span></span> <span data-ttu-id="24890-926">インライン デリゲートの最も一般的な使用方法は、メソッドをより粒度の細かいメソッドに分割して、より小規模なメソッドで拡張イベントを使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="24890-926">The most common way to use inline delegates is to split the method into more granular methods and enable extensibility events in the smaller methods.</span></span>

|  <span data-ttu-id="24890-927">メソッド</span><span class="sxs-lookup"><span data-stu-id="24890-927">Method</span></span> |
| -------------|
|<span data-ttu-id="24890-928">AxClass - ChequeDP - Method - insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="24890-928">AxClass - ChequeDP - Method - insertChequeTmp</span></span>|
|<span data-ttu-id="24890-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="24890-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span></span>|
|<span data-ttu-id="24890-930">クラス JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="24890-930">class JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="24890-931">クラス JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="24890-931">class JournalStatic.findJournalTableId</span></span>|
|<span data-ttu-id="24890-932">クラス WhsLocationDirective.findLocationMultiSKU</span><span class="sxs-lookup"><span data-stu-id="24890-932">Class WhsLocationDirective.findLocationMultiSKU</span></span>|
|<span data-ttu-id="24890-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span><span class="sxs-lookup"><span data-stu-id="24890-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span></span>|
|<span data-ttu-id="24890-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span><span class="sxs-lookup"><span data-stu-id="24890-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span></span>|
|<span data-ttu-id="24890-935">フォーム SalesTable - メソッド updateDesign</span><span class="sxs-lookup"><span data-stu-id="24890-935">Form SalesTable - method updateDesign</span></span>|
|<span data-ttu-id="24890-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span><span class="sxs-lookup"><span data-stu-id="24890-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span></span>|
|<span data-ttu-id="24890-937">SalesLineType.insert</span><span class="sxs-lookup"><span data-stu-id="24890-937">SalesLineType.insert</span></span>|
|<span data-ttu-id="24890-938">SalesLineType.update</span><span class="sxs-lookup"><span data-stu-id="24890-938">SalesLineType.update</span></span>|
|<span data-ttu-id="24890-939">SalesTable2LineUpdatePrompt.dialog</span><span class="sxs-lookup"><span data-stu-id="24890-939">SalesTable2LineUpdatePrompt.dialog</span></span>|
|<span data-ttu-id="24890-940">テーブル ExtCodeTable</span><span class="sxs-lookup"><span data-stu-id="24890-940">table ExtCodeTable</span></span>|
|<span data-ttu-id="24890-941">テーブル InventItemGroup.getGroupForAccountType</span><span class="sxs-lookup"><span data-stu-id="24890-941">table InventItemGroup.getGroupForAccountType</span></span>|
|<span data-ttu-id="24890-942">テーブル InventItemGroup.ledgerDimensionDescription</span><span class="sxs-lookup"><span data-stu-id="24890-942">table InventItemGroup.ledgerDimensionDescription</span></span>|
|<span data-ttu-id="24890-943">テーブル InventTestAssociationTable</span><span class="sxs-lookup"><span data-stu-id="24890-943">table InventTestAssociationTable</span></span>|
|<span data-ttu-id="24890-944">テーブル LedgerJournalName - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="24890-944">Table LedgerJournalName - method validateWrite</span></span>|
|<span data-ttu-id="24890-945">テーブル PaymTerm - メソッド due</span><span class="sxs-lookup"><span data-stu-id="24890-945">Table PaymTerm - method due</span></span>|
|<span data-ttu-id="24890-946">TaxCalculation.newForSourceType</span><span class="sxs-lookup"><span data-stu-id="24890-946">TaxCalculation.newForSourceType</span></span>|
|<span data-ttu-id="24890-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span><span class="sxs-lookup"><span data-stu-id="24890-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span></span>|
|<span data-ttu-id="24890-948">WHSLoadLine.getOrderCommonFromLoadLine</span><span class="sxs-lookup"><span data-stu-id="24890-948">WHSLoadLine.getOrderCommonFromLoadLine</span></span>|
|<span data-ttu-id="24890-949">WhsLocationDirective.findLocation</span><span class="sxs-lookup"><span data-stu-id="24890-949">WhsLocationDirective.findLocation</span></span>|
|<span data-ttu-id="24890-950">WHSRFControlData.populateData</span><span class="sxs-lookup"><span data-stu-id="24890-950">WHSRFControlData.populateData</span></span>|
|<span data-ttu-id="24890-951">WHSRFControLData.processControl</span><span class="sxs-lookup"><span data-stu-id="24890-951">WHSRFControLData.processControl</span></span>|
|<span data-ttu-id="24890-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="24890-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span></span>|

## <a name="other-changes"></a><span data-ttu-id="24890-953">その他の変更</span><span class="sxs-lookup"><span data-stu-id="24890-953">Other changes</span></span>

<span data-ttu-id="24890-954">次の表に、拡張機能に対して行われた追加の変更を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="24890-954">The following table lists additional changes that have been made for extensibility.</span></span>


|                                                           <span data-ttu-id="24890-955">変更</span><span class="sxs-lookup"><span data-stu-id="24890-955">Change</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------------------|
|                                      <span data-ttu-id="24890-956">既存の製品分析コードの間接参照の追加</span><span class="sxs-lookup"><span data-stu-id="24890-956">Add indirection for existing product dimensions</span></span>                                       |
|                                  <span data-ttu-id="24890-957">クラス FormLetterParmDataOutputContract は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="24890-957">Class FormLetterParmDataOutputContract is not extensible</span></span>                                  |
|             <span data-ttu-id="24890-958">1 つ以上の引数をサポートする SysExtensionFramework のインスタンス化戦略の作成</span><span class="sxs-lookup"><span data-stu-id="24890-958">Create an instantiation strategy for the SysExtensionFramework that supports one or more arguments</span></span>             |
|                      <span data-ttu-id="24890-959">カスタマイズ: TableField: 拡張モデル: テーブル フィールドの EDT タイプの変更</span><span class="sxs-lookup"><span data-stu-id="24890-959">Customization: TableField: Extension Model: Change EDT type of on a table field</span></span>                       |
|                          <span data-ttu-id="24890-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="24890-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch statement</span></span>                           |
|                                     <span data-ttu-id="24890-961">CustVendOpenTransBalances - new() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="24890-961">CustVendOpenTransBalances - new() switch statement</span></span>                                     |
|                                  <span data-ttu-id="24890-962">CustVendOutPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="24890-962">CustVendOutPaym (Class) needs extensibility improvement</span></span>                                   |
|                        <span data-ttu-id="24890-963">CustVendPaymReconciliationSetStatus (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="24890-963">CustVendPaymReconciliationSetStatus (Class) needs extensibility improvement</span></span>                         |
|                                 <span data-ttu-id="24890-964">CustVendSumForPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="24890-964">CustVendSumForPaym (Class) needs extensibility improvement</span></span>                                 |
|                               <span data-ttu-id="24890-965">SysGroup からの AddressCountyId と AddressStateId EDT の切り離し</span><span class="sxs-lookup"><span data-stu-id="24890-965">Decouple AddressCountyId and AddressStateId EDTs from SysGroup</span></span>                               |
|                          <span data-ttu-id="24890-966">ドキュメント管理イベントの処理には拡張性サポートの改善が必要</span><span class="sxs-lookup"><span data-stu-id="24890-966">Document Management event handling needs improved extensibility support</span></span>                           |
|            <span data-ttu-id="24890-967">為替レート プロバイダー フレームワークには、通貨モデルにカスタムの組み込みプロバイダーを配置することが必要</span><span class="sxs-lookup"><span data-stu-id="24890-967">Exchange rate provider framework requires custom built providers to be placed in the Currency Model</span></span>             |
|                                                      <span data-ttu-id="24890-968">GS-128 の拡張</span><span class="sxs-lookup"><span data-stu-id="24890-968">Extending GS-128</span></span>                                                      |
|                         <span data-ttu-id="24890-969">拡張モデル: CountryRegionCodes プロパティでのカスタマイズを許可する。</span><span class="sxs-lookup"><span data-stu-id="24890-969">Extension model: Allow customizations on the CountryRegionCodes property.</span></span>                          |
|                  <span data-ttu-id="24890-970">フォーム拡張機能 - 新しいコントロールによって "拡張された" フォーム要素の拡張機能は動作しません</span><span class="sxs-lookup"><span data-stu-id="24890-970">Form extension - Extension of "extended" form elements with new controls are not working</span></span>                  |
|                                              <span data-ttu-id="24890-971">InventDim: throw 付きの条件</span><span class="sxs-lookup"><span data-stu-id="24890-971">InventDim: Condition with throw</span></span>                                               |
|                                                  <span data-ttu-id="24890-972">InventDimRenameDimValue</span><span class="sxs-lookup"><span data-stu-id="24890-972">InventDimRenameDimValue</span></span>                                                   |
|                <span data-ttu-id="24890-973">メソッドのオーバーレイ - クラス VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="24890-973">Method overlayering - Class VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span></span>                |
|                                     <span data-ttu-id="24890-974">メソッドのオーバーレイ: クラス Markup - メソッド delete</span><span class="sxs-lookup"><span data-stu-id="24890-974">Method overlayering: class Markup - method delete</span></span>                                      |
|                       <span data-ttu-id="24890-975">メソッドのオーバーレイ: クラス McrPriceHistoryForm.insertPotentialTradeAgreements</span><span class="sxs-lookup"><span data-stu-id="24890-975">Method overlayering: class McrPriceHistoryForm.insertPotentialTradeAgreements</span></span>                        |
|                             <span data-ttu-id="24890-976">メソッドのオーバーレイ: クラス OffsetVoucher - メソッド markTransaction</span><span class="sxs-lookup"><span data-stu-id="24890-976">Method overlayering: Class OffsetVoucher - method markTransaction</span></span>                              |
|                                 <span data-ttu-id="24890-977">メソッドのオーバーレイ: フォーム LedgerJournalTransDimension.init</span><span class="sxs-lookup"><span data-stu-id="24890-977">Method overlayering: Form LedgerJournalTransDimension.init</span></span>                                 |
|                                 <span data-ttu-id="24890-978">メソッドのオーバーレイ: フォーム LedgerTransVoucher - メソッド init</span><span class="sxs-lookup"><span data-stu-id="24890-978">Method overlayering: Form LedgerTransVoucher - method init</span></span>                                 |
|                             <span data-ttu-id="24890-979">メソッドのオーバーレイ: テーブル CustInvoiceTable - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="24890-979">Method overlayering: Table CustInvoiceTable - method validateWrite</span></span>                             |
|                       <span data-ttu-id="24890-980">メソッド シグネチャが変更されました: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span><span class="sxs-lookup"><span data-stu-id="24890-980">Method signature changed: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span></span>                        |
|                               <span data-ttu-id="24890-981">メソッド シグネチャが変更になりました: WHSInvent.getCommonFromWorkTransType</span><span class="sxs-lookup"><span data-stu-id="24890-981">Method signature changed: WHSInvent.getCommonFromWorkTransType</span></span>                               |
|                                  <span data-ttu-id="24890-982">メソッド シグネチャが変更されました: WHSPoolProdBom.movementBuffer</span><span class="sxs-lookup"><span data-stu-id="24890-982">Method signature changed: WHSPoolProdBom.movementBuffer</span></span>                                   |
|                          <span data-ttu-id="24890-983">construct メソッドがありません: クラス SMAServiceOrderTableButtonStateProvider</span><span class="sxs-lookup"><span data-stu-id="24890-983">Missing construct method: class SMAServiceOrderTableButtonStateProvider</span></span>                           |
|                                         <span data-ttu-id="24890-984">必要な番号順序スコープの拡張性</span><span class="sxs-lookup"><span data-stu-id="24890-984">Number sequence scope extensibility needed</span></span>                                         |
|                           <span data-ttu-id="24890-985">Runbase には、クラスの拡張機能がメンバーをパック/アンパックする方法が必要</span><span class="sxs-lookup"><span data-stu-id="24890-985">Runbase needs a way for class extensions to pack/unpack their members</span></span>                            |
|                                              <span data-ttu-id="24890-986">文字列 EDT のサイズの拡張の問題</span><span class="sxs-lookup"><span data-stu-id="24890-986">String EDT size extension issues</span></span>                                              |
|                              <span data-ttu-id="24890-987">カスタムの InventDim に基づく手持在庫フォームのオープンのサポート</span><span class="sxs-lookup"><span data-stu-id="24890-987">Support opening Inventory on-hand form based on custom InventDim</span></span>                              |
|          <span data-ttu-id="24890-988">SysExtension フレームワーク: SysExtensionIInstantiationStrategy と SysExtensionIAttribute は互換性がありません</span><span class="sxs-lookup"><span data-stu-id="24890-988">SysExtension framework: SysExtensionIInstantiationStrategy and SysExtensionIAttribute are not compatible</span></span>          |
| <span data-ttu-id="24890-989">要求/応答シナリオで使用されるデリゲートがより堅牢になるために、EventHandlerResult のバリエーションが必要</span><span class="sxs-lookup"><span data-stu-id="24890-989">Variations of EventHandlerResult are requested to ensure that delegates used in Request/response scenarios are more robust</span></span> |
|                                                <span data-ttu-id="24890-990">WHS モバイル フレームワーク: 合格</span><span class="sxs-lookup"><span data-stu-id="24890-990">WHS Mobile Framework: passes</span></span>                                                |
|                                     <span data-ttu-id="24890-991">WhsLocationDirectiveLine To/FromQty は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="24890-991">WhsLocationDirectiveLine To/FromQty not extensible</span></span>                                     |
|                                                 <span data-ttu-id="24890-992">WHSMobileApp の拡張性</span><span class="sxs-lookup"><span data-stu-id="24890-992">WHSMobileApp Extensibility</span></span>                                                 |
|         <span data-ttu-id="24890-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="24890-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|         <span data-ttu-id="24890-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="24890-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|            <span data-ttu-id="24890-995">WhsRFControlData.processControl は switch ブロック内の _data ではなく WhsControl.data を参照する必要があります</span><span class="sxs-lookup"><span data-stu-id="24890-995">WhsRFControlData.processControl must reference WhsControl.data instead of _data in the switch block</span></span>             |


