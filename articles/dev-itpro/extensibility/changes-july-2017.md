---
title: Finance and Operations, Enterprise Edition (2017 年 7 月) の拡張機能の変更
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
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: d6834971cb50a7379a43320ac386e9294717f2f3
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833474"
---
# <a name="extensibility-changes-in-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="b918c-103">Finance and Operations, Enterprise Edition (2017 年 7 月) の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="b918c-103">Extensibility changes in Finance and Operations, Enterprise edition (July 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b918c-104">これは、Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="b918c-104">This is a list of extensibility features that were implemented in the Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span> <span data-ttu-id="b918c-105">このバージョンは 2017 年 7 月にリリースされ、ビルド番号は 7.2.11792.56024 です。</span><span class="sxs-lookup"><span data-stu-id="b918c-105">This version was released in July 2017 and has a build number of 7.2.11792.56024.</span></span> <span data-ttu-id="b918c-106">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b918c-106">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="soft-sealed-application-models"></a><span data-ttu-id="b918c-107">ソフト シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-107">Soft-sealed application models</span></span>

<span data-ttu-id="b918c-108">以下のアプリケーション中間層モデルは、今回のリリースでソフト シールされました。</span><span class="sxs-lookup"><span data-stu-id="b918c-108">The following application middle-tier models were soft-sealed in this release.</span></span> <span data-ttu-id="b918c-109">これらのモデルのオーバーレイ コードは、コンパイル時に警告を生成します。</span><span class="sxs-lookup"><span data-stu-id="b918c-109">Overlayered code in these models will generate warnings on compilation.</span></span>

| <span data-ttu-id="b918c-110">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="b918c-110">Category</span></span>       | <span data-ttu-id="b918c-111">モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-111">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="b918c-112">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b918c-112">Application Frameworks</span></span> | <span data-ttu-id="b918c-113">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="b918c-113">CaseManagement</span></span> |
| <span data-ttu-id="b918c-114">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b918c-114">Application Frameworks</span></span> | <span data-ttu-id="b918c-115">Dimensions</span><span class="sxs-lookup"><span data-stu-id="b918c-115">Dimensions</span></span> |
| <span data-ttu-id="b918c-116">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b918c-116">Application Frameworks</span></span> | <span data-ttu-id="b918c-117">Directory</span><span class="sxs-lookup"><span data-stu-id="b918c-117">Directory</span></span> |
| <span data-ttu-id="b918c-118">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b918c-118">Application Frameworks</span></span> | <span data-ttu-id="b918c-119">Organization</span><span class="sxs-lookup"><span data-stu-id="b918c-119">Organization</span></span> |
| <span data-ttu-id="b918c-120">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b918c-120">Application Frameworks</span></span> | <span data-ttu-id="b918c-121">Currency</span><span class="sxs-lookup"><span data-stu-id="b918c-121">Currency</span></span>|
| <span data-ttu-id="b918c-122">アプリケーション フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b918c-122">Application Frameworks</span></span> | <span data-ttu-id="b918c-123">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="b918c-123">ApplicationCommon</span></span>|
| <span data-ttu-id="b918c-124">HCM コア モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-124">HCM Core Models</span></span>| <span data-ttu-id="b918c-125">3817938</span><span class="sxs-lookup"><span data-stu-id="b918c-125">3817938</span></span>
|<span data-ttu-id="b918c-126">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-126">Tax Models</span></span> |<span data-ttu-id="b918c-127">Tax</span><span class="sxs-lookup"><span data-stu-id="b918c-127">Tax</span></span> |
|<span data-ttu-id="b918c-128">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-128">Tax Models</span></span> |<span data-ttu-id="b918c-129">Tax Books</span><span class="sxs-lookup"><span data-stu-id="b918c-129">Tax Books</span></span> |
|<span data-ttu-id="b918c-130">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-130">Tax Models</span></span> |<span data-ttu-id="b918c-131">Tax Books Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="b918c-131">Tax Books Application Suite Integration</span></span> |
|<span data-ttu-id="b918c-132">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-132">Tax Models</span></span> |<span data-ttu-id="b918c-133">Tax Engine Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="b918c-133">Tax Engine Application Suite Integration</span></span> |
|<span data-ttu-id="b918c-134">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-134">Tax Models</span></span> |<span data-ttu-id="b918c-135">Tax Engine Configuration</span><span class="sxs-lookup"><span data-stu-id="b918c-135">Tax Engine Configuration</span></span> |
|<span data-ttu-id="b918c-136">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-136">Tax Models</span></span> |<span data-ttu-id="b918c-137">Tax Engine Interface</span><span class="sxs-lookup"><span data-stu-id="b918c-137">Tax Engine Interface</span></span> |
|<span data-ttu-id="b918c-138">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-138">Tax Models</span></span> |<span data-ttu-id="b918c-139">Tax Engine Runtime Generation</span><span class="sxs-lookup"><span data-stu-id="b918c-139">Tax Engine Runtime Generation</span></span> |
|<span data-ttu-id="b918c-140">税モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-140">Tax Models</span></span> |<span data-ttu-id="b918c-141">TaxEngine</span><span class="sxs-lookup"><span data-stu-id="b918c-141">TaxEngine</span></span> |
| <span data-ttu-id="b918c-142">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-142">Source Document Models</span></span> |<span data-ttu-id="b918c-143">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="b918c-143">SourceDocumentation</span></span> |
| <span data-ttu-id="b918c-144">元伝票モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-144">Source Document Models</span></span> |<span data-ttu-id="b918c-145">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="b918c-145">SourceDocumentationTypes</span></span> |
| <span data-ttu-id="b918c-146">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-146">Ledger Models</span></span> |<span data-ttu-id="b918c-147">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="b918c-147">GeneralLedger</span></span> |
| <span data-ttu-id="b918c-148">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-148">Ledger Models</span></span> |<span data-ttu-id="b918c-149">Ledger</span><span class="sxs-lookup"><span data-stu-id="b918c-149">Ledger</span></span> |
| <span data-ttu-id="b918c-150">元帳モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-150">Ledger Models</span></span> |<span data-ttu-id="b918c-151">Subledger</span><span class="sxs-lookup"><span data-stu-id="b918c-151">Subledger</span></span> |
| <span data-ttu-id="b918c-152">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-152">Middle Tier SCM Models</span></span> | <span data-ttu-id="b918c-153">CostAccounting</span><span class="sxs-lookup"><span data-stu-id="b918c-153">CostAccounting</span></span> |
| <span data-ttu-id="b918c-154">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-154">Middle Tier SCM Models</span></span> | <span data-ttu-id="b918c-155">CostAccountingAX</span><span class="sxs-lookup"><span data-stu-id="b918c-155">CostAccountingAX</span></span> |
| <span data-ttu-id="b918c-156">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-156">Middle Tier SCM Models</span></span> | <span data-ttu-id="b918c-157">SCMControls</span><span class="sxs-lookup"><span data-stu-id="b918c-157">SCMControls</span></span> |
| <span data-ttu-id="b918c-158">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-158">Middle Tier SCM Models</span></span> | <span data-ttu-id="b918c-159">SCMMobile</span><span class="sxs-lookup"><span data-stu-id="b918c-159">SCMMobile</span></span> |
| <span data-ttu-id="b918c-160">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-160">Middle Tier SCM Models</span></span> | <span data-ttu-id="b918c-161">UnitOfMeasure</span><span class="sxs-lookup"><span data-stu-id="b918c-161">UnitOfMeasure</span></span> |
| <span data-ttu-id="b918c-162">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-162">Middle Tier SCM Models</span></span> | <span data-ttu-id="b918c-163">WMSAdvancedMigration</span><span class="sxs-lookup"><span data-stu-id="b918c-163">WMSAdvancedMigration</span></span>|
| <span data-ttu-id="b918c-164">中間層 SCM モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-164">Middle Tier SCM Models</span></span> | <span data-ttu-id="b918c-165">InventoryDimensionConversion</span><span class="sxs-lookup"><span data-stu-id="b918c-165">InventoryDimensionConversion</span></span>|
| <span data-ttu-id="b918c-166">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="b918c-166">Workspaces</span></span>| <span data-ttu-id="b918c-167">ApplicationWorkspaces</span><span class="sxs-lookup"><span data-stu-id="b918c-167">ApplicationWorkspaces</span></span> |
| <span data-ttu-id="b918c-168">財務</span><span class="sxs-lookup"><span data-stu-id="b918c-168">Finance</span></span>| <span data-ttu-id="b918c-169">Fiscalbooks</span><span class="sxs-lookup"><span data-stu-id="b918c-169">Fiscalbooks</span></span> |
| <span data-ttu-id="b918c-170">管理ツール</span><span class="sxs-lookup"><span data-stu-id="b918c-170">Management tools</span></span> | <span data-ttu-id="b918c-171">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="b918c-171">DataUpgrade</span></span> |

## <a name="hard-sealed-application-models"></a><span data-ttu-id="b918c-172">ハード シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-172">Hard-sealed application models</span></span>

<span data-ttu-id="b918c-173">以下のアプリケーション中間層モデルは、今回のリリースでハード シールされました。</span><span class="sxs-lookup"><span data-stu-id="b918c-173">The following application middle-tier models were hard-sealed in this release.</span></span> <span data-ttu-id="b918c-174">これらのモデルのオーバーレイ コードは、コンパイル時にエラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="b918c-174">Overlayered code in these models will generate errors on compilation.</span></span>

| <span data-ttu-id="b918c-175">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="b918c-175">Category</span></span>       | <span data-ttu-id="b918c-176">モデル</span><span class="sxs-lookup"><span data-stu-id="b918c-176">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="b918c-177">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="b918c-177">Accounts Payable</span></span> | <span data-ttu-id="b918c-178">AccountsPayableMobile</span><span class="sxs-lookup"><span data-stu-id="b918c-178">AccountsPayableMobile</span></span> |
| <span data-ttu-id="b918c-179">財務</span><span class="sxs-lookup"><span data-stu-id="b918c-179">Finance</span></span> | <span data-ttu-id="b918c-180">FinancialReportingEntityStore</span><span class="sxs-lookup"><span data-stu-id="b918c-180">FinancialReportingEntityStore</span></span>|
| <span data-ttu-id="b918c-181">ツール</span><span class="sxs-lookup"><span data-stu-id="b918c-181">Tools</span></span> | <span data-ttu-id="b918c-182">PerformanceTool</span><span class="sxs-lookup"><span data-stu-id="b918c-182">PerformanceTool</span></span> |
| <span data-ttu-id="b918c-183">経費</span><span class="sxs-lookup"><span data-stu-id="b918c-183">Expenses</span></span> | <span data-ttu-id="b918c-184">ExpenseMobile</span><span class="sxs-lookup"><span data-stu-id="b918c-184">ExpenseMobile</span></span> |
| <span data-ttu-id="b918c-185">GER</span><span class="sxs-lookup"><span data-stu-id="b918c-185">GER</span></span> | <span data-ttu-id="b918c-186">ElectronicReporting</span><span class="sxs-lookup"><span data-stu-id="b918c-186">ElectronicReporting</span></span>|
|<span data-ttu-id="b918c-187">GER</span><span class="sxs-lookup"><span data-stu-id="b918c-187">GER</span></span> | <span data-ttu-id="b918c-188">ElectronicReportingCore</span><span class="sxs-lookup"><span data-stu-id="b918c-188">ElectronicReportingCore</span></span>|
|<span data-ttu-id="b918c-189">GER</span><span class="sxs-lookup"><span data-stu-id="b918c-189">GER</span></span> | <span data-ttu-id="b918c-190">Electronic Reporting Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="b918c-190">Electronic Reporting Application Suite Integration</span></span>|

## <a name="enumerations-that-are-now-extensible"></a><span data-ttu-id="b918c-191">拡張可能になった列挙型</span><span class="sxs-lookup"><span data-stu-id="b918c-191">Enumerations that are now extensible</span></span>

<span data-ttu-id="b918c-192">列挙の拡張をサポートするために以下の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="b918c-192">The following changes were made to support extending enumerations:</span></span>
- <span data-ttu-id="b918c-193">標準アプリケーションの多くの列挙が拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-193">Many enumerations in the standard application have been made extensible.</span></span> <span data-ttu-id="b918c-194">列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b918c-194">An enumeration is made extensible by setting two properties on the enumeration.</span></span> <span data-ttu-id="b918c-195">**IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b918c-195">The **IsExtensible** property is set to **Yes**, and the **UseEnumValue** property is set to **No**.</span></span> 
- <span data-ttu-id="b918c-196">一部の列挙型は状態を表します。</span><span class="sxs-lookup"><span data-stu-id="b918c-196">Some enumerations represent state.</span></span> <span data-ttu-id="b918c-197">拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="b918c-197">New façade methods have been added to help enable adding enumeration values by extension.</span></span> <span data-ttu-id="b918c-198">列挙型を拡張する方法については、「[列挙値の追加](add-enum-value.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b918c-198">For information about how to extend an enumeration, see [Add an enum value](add-enum-value.md).</span></span>
- <span data-ttu-id="b918c-199">拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。</span><span class="sxs-lookup"><span data-stu-id="b918c-199">Some application code that uses enumerations was changed to support extensibility.</span></span> <span data-ttu-id="b918c-200">一般的な変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="b918c-200">Common changes include:</span></span>
    + <span data-ttu-id="b918c-201">ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。</span><span class="sxs-lookup"><span data-stu-id="b918c-201">Removing **throw** exception statements in the default case of a switch to allow post-event subscription.</span></span>
    + <span data-ttu-id="b918c-202">拡張機能の **SysExtension** サポートの追加。</span><span class="sxs-lookup"><span data-stu-id="b918c-202">Adding **SysExtension** support for extension.</span></span>
    + <span data-ttu-id="b918c-203">明示的なデリゲートの追加。</span><span class="sxs-lookup"><span data-stu-id="b918c-203">Adding explicit delegates.</span></span>


| <span data-ttu-id="b918c-204">列挙型</span><span class="sxs-lookup"><span data-stu-id="b918c-204">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="b918c-205">AgreementState</span><span class="sxs-lookup"><span data-stu-id="b918c-205">AgreementState</span></span>|
|<span data-ttu-id="b918c-206">AssetAccountType</span><span class="sxs-lookup"><span data-stu-id="b918c-206">AssetAccountType</span></span>|
|<span data-ttu-id="b918c-207">AssetTransTypeJournal</span><span class="sxs-lookup"><span data-stu-id="b918c-207">AssetTransTypeJournal</span></span>|
|<span data-ttu-id="b918c-208">BankAccountType</span><span class="sxs-lookup"><span data-stu-id="b918c-208">BankAccountType</span></span>|
|<span data-ttu-id="b918c-209">BankFormat</span><span class="sxs-lookup"><span data-stu-id="b918c-209">BankFormat</span></span>|
|<span data-ttu-id="b918c-210">BarcodeContentType</span><span class="sxs-lookup"><span data-stu-id="b918c-210">BarcodeContentType</span></span>|
|<span data-ttu-id="b918c-211">BarcodeCoverPageEntityType</span><span class="sxs-lookup"><span data-stu-id="b918c-211">BarcodeCoverPageEntityType</span></span>|
|<span data-ttu-id="b918c-212">BarcodeType</span><span class="sxs-lookup"><span data-stu-id="b918c-212">BarcodeType</span></span>|
|<span data-ttu-id="b918c-213">BOMCalcCostingVersionUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-213">BOMCalcCostingVersionUpdate</span></span>|
|<span data-ttu-id="b918c-214">BOMCalcCostPriceUsed</span><span class="sxs-lookup"><span data-stu-id="b918c-214">BOMCalcCostPriceUsed</span></span>|
|<span data-ttu-id="b918c-215">BOMCalcSalesPriceUsed</span><span class="sxs-lookup"><span data-stu-id="b918c-215">BOMCalcSalesPriceUsed</span></span>|
|<span data-ttu-id="b918c-216">BOMCalcType</span><span class="sxs-lookup"><span data-stu-id="b918c-216">BOMCalcType</span></span>|
|<span data-ttu-id="b918c-217">BOMCheckLevel</span><span class="sxs-lookup"><span data-stu-id="b918c-217">BOMCheckLevel</span></span>|
|<span data-ttu-id="b918c-218">BOMCopyContext</span><span class="sxs-lookup"><span data-stu-id="b918c-218">BOMCopyContext</span></span>|
|<span data-ttu-id="b918c-219">BOMCopyMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-219">BOMCopyMethod</span></span>|
|<span data-ttu-id="b918c-220">BOMCopyType</span><span class="sxs-lookup"><span data-stu-id="b918c-220">BOMCopyType</span></span>|
|<span data-ttu-id="b918c-221">BOMCostCalculationMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-221">BOMCostCalculationMethod</span></span>|
|<span data-ttu-id="b918c-222">BOMExplode</span><span class="sxs-lookup"><span data-stu-id="b918c-222">BOMExplode</span></span>|
|<span data-ttu-id="b918c-223">BOMRouteCopyDataType</span><span class="sxs-lookup"><span data-stu-id="b918c-223">BOMRouteCopyDataType</span></span>|
|<span data-ttu-id="b918c-224">BOMVersionFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-224">BOMVersionFilter</span></span>|
|<span data-ttu-id="b918c-225">BudgetReservation_BusinessEvent_PSN</span><span class="sxs-lookup"><span data-stu-id="b918c-225">BudgetReservation_BusinessEvent_PSN</span></span>|
|<span data-ttu-id="b918c-226">BudgetReservation_SourceDocument_PSN</span><span class="sxs-lookup"><span data-stu-id="b918c-226">BudgetReservation_SourceDocument_PSN</span></span>|
|<span data-ttu-id="b918c-227">BudgetReservation_SourceDocumentLine_PSN</span><span class="sxs-lookup"><span data-stu-id="b918c-227">BudgetReservation_SourceDocumentLine_PSN</span></span>|
|<span data-ttu-id="b918c-228">CatCallMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-228">CatCallMethod</span></span>|
|<span data-ttu-id="b918c-229">CatContentType</span><span class="sxs-lookup"><span data-stu-id="b918c-229">CatContentType</span></span>|
|<span data-ttu-id="b918c-230">CatImportStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-230">CatImportStatus</span></span>|
|<span data-ttu-id="b918c-231">CatMaintenanceRequestWfStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-231">CatMaintenanceRequestWfStatus</span></span>|
|<span data-ttu-id="b918c-232">CatProcurementErrorCode</span><span class="sxs-lookup"><span data-stu-id="b918c-232">CatProcurementErrorCode</span></span>|
|<span data-ttu-id="b918c-233">CatPurchaseStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-233">CatPurchaseStatus</span></span>|
|<span data-ttu-id="b918c-234">CatUserReviewApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-234">CatUserReviewApprovalStatus</span></span>|
|<span data-ttu-id="b918c-235">CatVendorCatalogFileUploadType</span><span class="sxs-lookup"><span data-stu-id="b918c-235">CatVendorCatalogFileUploadType</span></span>|
|<span data-ttu-id="b918c-236">CatVendorCatalogTemplateCategory</span><span class="sxs-lookup"><span data-stu-id="b918c-236">CatVendorCatalogTemplateCategory</span></span>|
|<span data-ttu-id="b918c-237">CatVendorCategoryHierarchyType</span><span class="sxs-lookup"><span data-stu-id="b918c-237">CatVendorCategoryHierarchyType</span></span>|
|<span data-ttu-id="b918c-238">CatVendorConfigurationForImport</span><span class="sxs-lookup"><span data-stu-id="b918c-238">CatVendorConfigurationForImport</span></span>|
|<span data-ttu-id="b918c-239">CatVendorLegalEntityStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-239">CatVendorLegalEntityStatus</span></span>|
|<span data-ttu-id="b918c-240">CatVendorSiteType</span><span class="sxs-lookup"><span data-stu-id="b918c-240">CatVendorSiteType</span></span>|
|<span data-ttu-id="b918c-241">ConsignmentReplenishmentOrderLineStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-241">ConsignmentReplenishmentOrderLineStatus</span></span>|
|<span data-ttu-id="b918c-242">ConsignmentReplenishmentOrderStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-242">ConsignmentReplenishmentOrderStatus</span></span>|
|<span data-ttu-id="b918c-243">CostBreakdown</span><span class="sxs-lookup"><span data-stu-id="b918c-243">CostBreakdown</span></span>|
|<span data-ttu-id="b918c-244">CostCalculationCompareProductType</span><span class="sxs-lookup"><span data-stu-id="b918c-244">CostCalculationCompareProductType</span></span>|
|<span data-ttu-id="b918c-245">CostCalculationRole</span><span class="sxs-lookup"><span data-stu-id="b918c-245">CostCalculationRole</span></span>|
|<span data-ttu-id="b918c-246">CostCalculationState</span><span class="sxs-lookup"><span data-stu-id="b918c-246">CostCalculationState</span></span>|
|<span data-ttu-id="b918c-247">CostCalculationSurchargeSubtype</span><span class="sxs-lookup"><span data-stu-id="b918c-247">CostCalculationSurchargeSubtype</span></span>|
|<span data-ttu-id="b918c-248">CostingActivationType</span><span class="sxs-lookup"><span data-stu-id="b918c-248">CostingActivationType</span></span>|
|<span data-ttu-id="b918c-249">CostingVersionCompareTo</span><span class="sxs-lookup"><span data-stu-id="b918c-249">CostingVersionCompareTo</span></span>|
|<span data-ttu-id="b918c-250">CostingVersionPriceType</span><span class="sxs-lookup"><span data-stu-id="b918c-250">CostingVersionPriceType</span></span>|
|<span data-ttu-id="b918c-251">CostPriceBase</span><span class="sxs-lookup"><span data-stu-id="b918c-251">CostPriceBase</span></span>|
|<span data-ttu-id="b918c-252">CostProfitSet</span><span class="sxs-lookup"><span data-stu-id="b918c-252">CostProfitSet</span></span>|
|<span data-ttu-id="b918c-253">CostSalesPriceDisplay</span><span class="sxs-lookup"><span data-stu-id="b918c-253">CostSalesPriceDisplay</span></span>|
|<span data-ttu-id="b918c-254">CostSheetNodeListType</span><span class="sxs-lookup"><span data-stu-id="b918c-254">CostSheetNodeListType</span></span>|
|<span data-ttu-id="b918c-255">CostSheetPanelView</span><span class="sxs-lookup"><span data-stu-id="b918c-255">CostSheetPanelView</span></span>|
|<span data-ttu-id="b918c-256">CostSheetProdFlowMode</span><span class="sxs-lookup"><span data-stu-id="b918c-256">CostSheetProdFlowMode</span></span>|
|<span data-ttu-id="b918c-257">CostStatementCacheAggregationAfter</span><span class="sxs-lookup"><span data-stu-id="b918c-257">CostStatementCacheAggregationAfter</span></span>|
|<span data-ttu-id="b918c-258">CostWIPStatementCategory</span><span class="sxs-lookup"><span data-stu-id="b918c-258">CostWIPStatementCategory</span></span>|
|<span data-ttu-id="b918c-259">CustPaymentValidate</span><span class="sxs-lookup"><span data-stu-id="b918c-259">CustPaymentValidate</span></span>|
|<span data-ttu-id="b918c-260">CustSpecTransOverviewFormMode</span><span class="sxs-lookup"><span data-stu-id="b918c-260">CustSpecTransOverviewFormMode</span></span>|
|<span data-ttu-id="b918c-261">CustTransRefType</span><span class="sxs-lookup"><span data-stu-id="b918c-261">CustTransRefType</span></span>|
|<span data-ttu-id="b918c-262">CustVendPaymentStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-262">CustVendPaymentStatus</span></span>|
|<span data-ttu-id="b918c-263">CustVendTransportPointTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="b918c-263">CustVendTransportPointTypeTransfer</span></span>|
|<span data-ttu-id="b918c-264">DlvScheduleMarkupConversionMode</span><span class="sxs-lookup"><span data-stu-id="b918c-264">DlvScheduleMarkupConversionMode</span></span>|
|<span data-ttu-id="b918c-265">EcoResAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="b918c-265">EcoResAttributeModifier</span></span>|
|<span data-ttu-id="b918c-266">EcoResCategoryAttributeModifier</span><span class="sxs-lookup"><span data-stu-id="b918c-266">EcoResCategoryAttributeModifier</span></span>|
|<span data-ttu-id="b918c-267">EcoResCategoryChangeStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-267">EcoResCategoryChangeStatus</span></span>|
|<span data-ttu-id="b918c-268">EcoResCategoryHierarchyModifier</span><span class="sxs-lookup"><span data-stu-id="b918c-268">EcoResCategoryHierarchyModifier</span></span>|
|<span data-ttu-id="b918c-269">EcoResCategoryNamedHierarchyRole</span><span class="sxs-lookup"><span data-stu-id="b918c-269">EcoResCategoryNamedHierarchyRole</span></span>|
|<span data-ttu-id="b918c-270">EcoResProductImageUsage</span><span class="sxs-lookup"><span data-stu-id="b918c-270">EcoResProductImageUsage</span></span>|
|<span data-ttu-id="b918c-271">EcoResProductListPage</span><span class="sxs-lookup"><span data-stu-id="b918c-271">EcoResProductListPage</span></span>|
|<span data-ttu-id="b918c-272">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="b918c-272">EcoResProductPerCompanyListPageType</span></span>|
|<span data-ttu-id="b918c-273">EcoResProductTemplateType</span><span class="sxs-lookup"><span data-stu-id="b918c-273">EcoResProductTemplateType</span></span>|
|<span data-ttu-id="b918c-274">EcoResReleaseProductToCompany</span><span class="sxs-lookup"><span data-stu-id="b918c-274">EcoResReleaseProductToCompany</span></span>|
|<span data-ttu-id="b918c-275">EcoResVariantConfigurationTechnologyType</span><span class="sxs-lookup"><span data-stu-id="b918c-275">EcoResVariantConfigurationTechnologyType</span></span>|
|<span data-ttu-id="b918c-276">ECPsalesOrdersViewType</span><span class="sxs-lookup"><span data-stu-id="b918c-276">ECPsalesOrdersViewType</span></span>|
|<span data-ttu-id="b918c-277">EPCSSProductViewType</span><span class="sxs-lookup"><span data-stu-id="b918c-277">EPCSSProductViewType</span></span>|
|<span data-ttu-id="b918c-278">EUSalesTransMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-278">EUSalesTransMethod</span></span>|
|<span data-ttu-id="b918c-279">FormLetterType</span><span class="sxs-lookup"><span data-stu-id="b918c-279">FormLetterType</span></span>|
|<span data-ttu-id="b918c-280">GanttCallerWrkCtr</span><span class="sxs-lookup"><span data-stu-id="b918c-280">GanttCallerWrkCtr</span></span>|
|<span data-ttu-id="b918c-281">GanttSetupType</span><span class="sxs-lookup"><span data-stu-id="b918c-281">GanttSetupType</span></span>|
|<span data-ttu-id="b918c-282">GanttTimeUnit</span><span class="sxs-lookup"><span data-stu-id="b918c-282">GanttTimeUnit</span></span>|
|<span data-ttu-id="b918c-283">GanttWrkCtrDisplayColumnsType</span><span class="sxs-lookup"><span data-stu-id="b918c-283">GanttWrkCtrDisplayColumnsType</span></span>|
|<span data-ttu-id="b918c-284">IntercompanyGoodsInTransitLineType</span><span class="sxs-lookup"><span data-stu-id="b918c-284">IntercompanyGoodsInTransitLineType</span></span>|
|<span data-ttu-id="b918c-285">InterCompanyGoodsInTransitOrigin</span><span class="sxs-lookup"><span data-stu-id="b918c-285">InterCompanyGoodsInTransitOrigin</span></span>|
|<span data-ttu-id="b918c-286">InventAccountType</span><span class="sxs-lookup"><span data-stu-id="b918c-286">InventAccountType</span></span>|
|<span data-ttu-id="b918c-287">InventAccountTypeStdCostVariance</span><span class="sxs-lookup"><span data-stu-id="b918c-287">InventAccountTypeStdCostVariance</span></span>|
|<span data-ttu-id="b918c-288">InventAdjustmentBy</span><span class="sxs-lookup"><span data-stu-id="b918c-288">InventAdjustmentBy</span></span>|
|<span data-ttu-id="b918c-289">InventAgingView</span><span class="sxs-lookup"><span data-stu-id="b918c-289">InventAgingView</span></span>|
|<span data-ttu-id="b918c-290">InventBatchJournalType</span><span class="sxs-lookup"><span data-stu-id="b918c-290">InventBatchJournalType</span></span>|
|<span data-ttu-id="b918c-291">InventCostBundleState</span><span class="sxs-lookup"><span data-stu-id="b918c-291">InventCostBundleState</span></span>|
|<span data-ttu-id="b918c-292">InventCostCostDistribution</span><span class="sxs-lookup"><span data-stu-id="b918c-292">InventCostCostDistribution</span></span>|
|<span data-ttu-id="b918c-293">InventCostTransactionCategory</span><span class="sxs-lookup"><span data-stu-id="b918c-293">InventCostTransactionCategory</span></span>|
|<span data-ttu-id="b918c-294">InventCostTransRefType</span><span class="sxs-lookup"><span data-stu-id="b918c-294">InventCostTransRefType</span></span>|
|<span data-ttu-id="b918c-295">InventCountCode</span><span class="sxs-lookup"><span data-stu-id="b918c-295">InventCountCode</span></span>|
|<span data-ttu-id="b918c-296">InventItemCostingType</span><span class="sxs-lookup"><span data-stu-id="b918c-296">InventItemCostingType</span></span>|
|<span data-ttu-id="b918c-297">InventItemLookupDefaultTab</span><span class="sxs-lookup"><span data-stu-id="b918c-297">InventItemLookupDefaultTab</span></span>|
|<span data-ttu-id="b918c-298">InventItemOrderSetupCallerType</span><span class="sxs-lookup"><span data-stu-id="b918c-298">InventItemOrderSetupCallerType</span></span>|
|<span data-ttu-id="b918c-299">InventItemOrderSetupType</span><span class="sxs-lookup"><span data-stu-id="b918c-299">InventItemOrderSetupType</span></span>|
|<span data-ttu-id="b918c-300">InventItemPriceCompareLevel</span><span class="sxs-lookup"><span data-stu-id="b918c-300">InventItemPriceCompareLevel</span></span>|
|<span data-ttu-id="b918c-301">InventItemPriceFilterType</span><span class="sxs-lookup"><span data-stu-id="b918c-301">InventItemPriceFilterType</span></span>|
|<span data-ttu-id="b918c-302">InventItemPriceType</span><span class="sxs-lookup"><span data-stu-id="b918c-302">InventItemPriceType</span></span>|
|<span data-ttu-id="b918c-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span><span class="sxs-lookup"><span data-stu-id="b918c-303">InventJournalOwnershipChangeLineCreateQueryStatusIssue</span></span>|
|<span data-ttu-id="b918c-304">InventJournalType</span><span class="sxs-lookup"><span data-stu-id="b918c-304">InventJournalType</span></span>|
|<span data-ttu-id="b918c-305">InventLedgerConflictModule</span><span class="sxs-lookup"><span data-stu-id="b918c-305">InventLedgerConflictModule</span></span>|
|<span data-ttu-id="b918c-306">InventLocationType</span><span class="sxs-lookup"><span data-stu-id="b918c-306">InventLocationType</span></span>|
|<span data-ttu-id="b918c-307">InventMovSubType</span><span class="sxs-lookup"><span data-stu-id="b918c-307">InventMovSubType</span></span>|
|<span data-ttu-id="b918c-308">InventNonConformanceApproval</span><span class="sxs-lookup"><span data-stu-id="b918c-308">InventNonConformanceApproval</span></span>|
|<span data-ttu-id="b918c-309">InventNonConformanceHistoryType</span><span class="sxs-lookup"><span data-stu-id="b918c-309">InventNonConformanceHistoryType</span></span>|
|<span data-ttu-id="b918c-310">InventNonConformanceType</span><span class="sxs-lookup"><span data-stu-id="b918c-310">InventNonConformanceType</span></span>|
|<span data-ttu-id="b918c-311">InventParameters</span><span class="sxs-lookup"><span data-stu-id="b918c-311">InventParameters</span></span>|
|<span data-ttu-id="b918c-312">InventPhysicalReduction</span><span class="sxs-lookup"><span data-stu-id="b918c-312">InventPhysicalReduction</span></span>|
|<span data-ttu-id="b918c-313">InventRefType</span><span class="sxs-lookup"><span data-stu-id="b918c-313">InventRefType</span></span>|
|<span data-ttu-id="b918c-314">InventReleaseOrderPickingType</span><span class="sxs-lookup"><span data-stu-id="b918c-314">InventReleaseOrderPickingType</span></span>|
|<span data-ttu-id="b918c-315">InventReportDimHistoryLogType</span><span class="sxs-lookup"><span data-stu-id="b918c-315">InventReportDimHistoryLogType</span></span>|
|<span data-ttu-id="b918c-316">InventStdCostConvItemStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-316">InventStdCostConvItemStatus</span></span>|
|<span data-ttu-id="b918c-317">InventStdCostPeriodType</span><span class="sxs-lookup"><span data-stu-id="b918c-317">InventStdCostPeriodType</span></span>|
|<span data-ttu-id="b918c-318">InventSumFields</span><span class="sxs-lookup"><span data-stu-id="b918c-318">InventSumFields</span></span>|
|<span data-ttu-id="b918c-319">InventSupplyDlvModeSelectCust</span><span class="sxs-lookup"><span data-stu-id="b918c-319">InventSupplyDlvModeSelectCust</span></span>|
|<span data-ttu-id="b918c-320">InventSupplyDlvModeSelectSupply</span><span class="sxs-lookup"><span data-stu-id="b918c-320">InventSupplyDlvModeSelectSupply</span></span>|
|<span data-ttu-id="b918c-321">InventSupplyLeadTimeSource</span><span class="sxs-lookup"><span data-stu-id="b918c-321">InventSupplyLeadTimeSource</span></span>|
|<span data-ttu-id="b918c-322">InventSupplyTmpLeadtimeType</span><span class="sxs-lookup"><span data-stu-id="b918c-322">InventSupplyTmpLeadtimeType</span></span>|
|<span data-ttu-id="b918c-323">InventTestActionOnFailure</span><span class="sxs-lookup"><span data-stu-id="b918c-323">InventTestActionOnFailure</span></span>|
|<span data-ttu-id="b918c-324">InventTestBlockProcess</span><span class="sxs-lookup"><span data-stu-id="b918c-324">InventTestBlockProcess</span></span>|
|<span data-ttu-id="b918c-325">InventTestCorrectionPriority</span><span class="sxs-lookup"><span data-stu-id="b918c-325">InventTestCorrectionPriority</span></span>|
|<span data-ttu-id="b918c-326">InventTestCorrectionStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-326">InventTestCorrectionStatus</span></span>|
|<span data-ttu-id="b918c-327">InventTestDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-327">InventTestDocumentStatus</span></span>|
|<span data-ttu-id="b918c-328">InventTestOrderStatusDisplay</span><span class="sxs-lookup"><span data-stu-id="b918c-328">InventTestOrderStatusDisplay</span></span>|
|<span data-ttu-id="b918c-329">InventTestOutcomeStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-329">InventTestOutcomeStatus</span></span>|
|<span data-ttu-id="b918c-330">InventTestQtySpecification</span><span class="sxs-lookup"><span data-stu-id="b918c-330">InventTestQtySpecification</span></span>|
|<span data-ttu-id="b918c-331">InventTestQuarantineType</span><span class="sxs-lookup"><span data-stu-id="b918c-331">InventTestQuarantineType</span></span>|
|<span data-ttu-id="b918c-332">InventTestReferenceType</span><span class="sxs-lookup"><span data-stu-id="b918c-332">InventTestReferenceType</span></span>|
|<span data-ttu-id="b918c-333">InventTestReport</span><span class="sxs-lookup"><span data-stu-id="b918c-333">InventTestReport</span></span>|
|<span data-ttu-id="b918c-334">InventTestType</span><span class="sxs-lookup"><span data-stu-id="b918c-334">InventTestType</span></span>|
|<span data-ttu-id="b918c-335">InventTrackingDimNodeType</span><span class="sxs-lookup"><span data-stu-id="b918c-335">InventTrackingDimNodeType</span></span>|
|<span data-ttu-id="b918c-336">InventTrackingProductType</span><span class="sxs-lookup"><span data-stu-id="b918c-336">InventTrackingProductType</span></span>|
|<span data-ttu-id="b918c-337">InventTrackingRegisterTransRegStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-337">InventTrackingRegisterTransRegStatus</span></span>|
|<span data-ttu-id="b918c-338">InventTransChildType</span><span class="sxs-lookup"><span data-stu-id="b918c-338">InventTransChildType</span></span>|
|<span data-ttu-id="b918c-339">InventTransferRemainStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-339">InventTransferRemainStatus</span></span>|
|<span data-ttu-id="b918c-340">InventTransferStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-340">InventTransferStatus</span></span>|
|<span data-ttu-id="b918c-341">InventTransferUpdateType</span><span class="sxs-lookup"><span data-stu-id="b918c-341">InventTransferUpdateType</span></span>|
|<span data-ttu-id="b918c-342">InventTransPickRegisterLineStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-342">InventTransPickRegisterLineStatus</span></span>|
|<span data-ttu-id="b918c-343">InventTransType</span><span class="sxs-lookup"><span data-stu-id="b918c-343">InventTransType</span></span>|
|<span data-ttu-id="b918c-344">InventUpdType</span><span class="sxs-lookup"><span data-stu-id="b918c-344">InventUpdType</span></span>|
|<span data-ttu-id="b918c-345">InventValueReportLedgerAccountCategory</span><span class="sxs-lookup"><span data-stu-id="b918c-345">InventValueReportLedgerAccountCategory</span></span>|
|<span data-ttu-id="b918c-346">InventValueReportLedgerLineType</span><span class="sxs-lookup"><span data-stu-id="b918c-346">InventValueReportLedgerLineType</span></span>|
|<span data-ttu-id="b918c-347">InventValueReportResourceType</span><span class="sxs-lookup"><span data-stu-id="b918c-347">InventValueReportResourceType</span></span>|
|<span data-ttu-id="b918c-348">ItemGroupLedgerDimensionGroup</span><span class="sxs-lookup"><span data-stu-id="b918c-348">ItemGroupLedgerDimensionGroup</span></span>|
|<span data-ttu-id="b918c-349">ItemReservation</span><span class="sxs-lookup"><span data-stu-id="b918c-349">ItemReservation</span></span>|
|<span data-ttu-id="b918c-350">JmgAbsenceColumnLayout</span><span class="sxs-lookup"><span data-stu-id="b918c-350">JmgAbsenceColumnLayout</span></span>|
|<span data-ttu-id="b918c-351">JmgAbsenceMethodEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-351">JmgAbsenceMethodEnum</span></span>|
|<span data-ttu-id="b918c-352">JmgAttendanceRegistrationType</span><span class="sxs-lookup"><span data-stu-id="b918c-352">JmgAttendanceRegistrationType</span></span>|
|<span data-ttu-id="b918c-353">JmgAttendanceReportType</span><span class="sxs-lookup"><span data-stu-id="b918c-353">JmgAttendanceReportType</span></span>|
|<span data-ttu-id="b918c-354">JmgBarCodeType</span><span class="sxs-lookup"><span data-stu-id="b918c-354">JmgBarCodeType</span></span>|
|<span data-ttu-id="b918c-355">JmgBreakDropEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-355">JmgBreakDropEnum</span></span>|
|<span data-ttu-id="b918c-356">JmgClockStyle</span><span class="sxs-lookup"><span data-stu-id="b918c-356">JmgClockStyle</span></span>|
|<span data-ttu-id="b918c-357">JmgControlType</span><span class="sxs-lookup"><span data-stu-id="b918c-357">JmgControlType</span></span>|
|<span data-ttu-id="b918c-358">JmgDaysTotalWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-358">JmgDaysTotalWorkflowStatus</span></span>|
|<span data-ttu-id="b918c-359">JmgEmployeeSignInStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-359">JmgEmployeeSignInStatus</span></span>|
|<span data-ttu-id="b918c-360">JmgFeedbackButtonFunction</span><span class="sxs-lookup"><span data-stu-id="b918c-360">JmgFeedbackButtonFunction</span></span>|
|<span data-ttu-id="b918c-361">JmgFeedbackStyle</span><span class="sxs-lookup"><span data-stu-id="b918c-361">JmgFeedbackStyle</span></span>|
|<span data-ttu-id="b918c-362">JmgFieldName</span><span class="sxs-lookup"><span data-stu-id="b918c-362">JmgFieldName</span></span>|
|<span data-ttu-id="b918c-363">JmgGetRegistrationTimeFrom</span><span class="sxs-lookup"><span data-stu-id="b918c-363">JmgGetRegistrationTimeFrom</span></span>|
|<span data-ttu-id="b918c-364">JmgGridAppearance</span><span class="sxs-lookup"><span data-stu-id="b918c-364">JmgGridAppearance</span></span>|
|<span data-ttu-id="b918c-365">JmgJobTableSynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="b918c-365">JmgJobTableSynchronizationMode</span></span>|
|<span data-ttu-id="b918c-366">JmgJournalRegWorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-366">JmgJournalRegWorkflowStatus</span></span>|
|<span data-ttu-id="b918c-367">JmgMark</span><span class="sxs-lookup"><span data-stu-id="b918c-367">JmgMark</span></span>|
|<span data-ttu-id="b918c-368">JmgMessageType</span><span class="sxs-lookup"><span data-stu-id="b918c-368">JmgMessageType</span></span>|
|<span data-ttu-id="b918c-369">JmgPayAdjustType</span><span class="sxs-lookup"><span data-stu-id="b918c-369">JmgPayAdjustType</span></span>|
|<span data-ttu-id="b918c-370">JmgPayEventsExportType</span><span class="sxs-lookup"><span data-stu-id="b918c-370">JmgPayEventsExportType</span></span>|
|<span data-ttu-id="b918c-371">JmgPaySpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-371">JmgPaySpecTypeEnum</span></span>|
|<span data-ttu-id="b918c-372">JmgPaySpecTypeEnumPick</span><span class="sxs-lookup"><span data-stu-id="b918c-372">JmgPaySpecTypeEnumPick</span></span>|
|<span data-ttu-id="b918c-373">JmgPostAutomatically</span><span class="sxs-lookup"><span data-stu-id="b918c-373">JmgPostAutomatically</span></span>|
|<span data-ttu-id="b918c-374">JmgProdStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-374">JmgProdStatusUpdate</span></span>|
|<span data-ttu-id="b918c-375">JmgProdStatusUpdateReportFinished</span><span class="sxs-lookup"><span data-stu-id="b918c-375">JmgProdStatusUpdateReportFinished</span></span>|
|<span data-ttu-id="b918c-376">JmgProfileSpecTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-376">JmgProfileSpecTypeEnum</span></span>|
|<span data-ttu-id="b918c-377">JmgProfileStartCodeBlankPrev</span><span class="sxs-lookup"><span data-stu-id="b918c-377">JmgProfileStartCodeBlankPrev</span></span>|
|<span data-ttu-id="b918c-378">JmgProjStatusUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-378">JmgProjStatusUpdate</span></span>|
|<span data-ttu-id="b918c-379">JmgRegistrationTouchJobStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-379">JmgRegistrationTouchJobStatus</span></span>|
|<span data-ttu-id="b918c-380">JmgSecondPresentationEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-380">JmgSecondPresentationEnum</span></span>|
|<span data-ttu-id="b918c-381">JmgShopFloorServiceStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-381">JmgShopFloorServiceStatus</span></span>|
|<span data-ttu-id="b918c-382">JmgSignInButtonFunction</span><span class="sxs-lookup"><span data-stu-id="b918c-382">JmgSignInButtonFunction</span></span>|
|<span data-ttu-id="b918c-383">JmgStoppedCompletedStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-383">JmgStoppedCompletedStatus</span></span>|
|<span data-ttu-id="b918c-384">JmgTermBaudeRate</span><span class="sxs-lookup"><span data-stu-id="b918c-384">JmgTermBaudeRate</span></span>|
|<span data-ttu-id="b918c-385">JmgTermComPort</span><span class="sxs-lookup"><span data-stu-id="b918c-385">JmgTermComPort</span></span>|
|<span data-ttu-id="b918c-386">JmgTermDataBit</span><span class="sxs-lookup"><span data-stu-id="b918c-386">JmgTermDataBit</span></span>|
|<span data-ttu-id="b918c-387">JmgTerminalInsertMode</span><span class="sxs-lookup"><span data-stu-id="b918c-387">JmgTerminalInsertMode</span></span>|
|<span data-ttu-id="b918c-388">JmgTermStopBit</span><span class="sxs-lookup"><span data-stu-id="b918c-388">JmgTermStopBit</span></span>|
|<span data-ttu-id="b918c-389">KanbanBoardRefreshCycle</span><span class="sxs-lookup"><span data-stu-id="b918c-389">KanbanBoardRefreshCycle</span></span>|
|<span data-ttu-id="b918c-390">KanbanBoardType</span><span class="sxs-lookup"><span data-stu-id="b918c-390">KanbanBoardType</span></span>|
|<span data-ttu-id="b918c-391">KanbanCardAssignmentType</span><span class="sxs-lookup"><span data-stu-id="b918c-391">KanbanCardAssignmentType</span></span>|
|<span data-ttu-id="b918c-392">KanbanControlActionState</span><span class="sxs-lookup"><span data-stu-id="b918c-392">KanbanControlActionState</span></span>|
|<span data-ttu-id="b918c-393">KanbanControlLegendFormat</span><span class="sxs-lookup"><span data-stu-id="b918c-393">KanbanControlLegendFormat</span></span>|
|<span data-ttu-id="b918c-394">KanbanControlSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="b918c-394">KanbanControlSelectionChanged</span></span>|
|<span data-ttu-id="b918c-395">KanbanDemandOriginType</span><span class="sxs-lookup"><span data-stu-id="b918c-395">KanbanDemandOriginType</span></span>|
|<span data-ttu-id="b918c-396">KanbanJobPeggingType</span><span class="sxs-lookup"><span data-stu-id="b918c-396">KanbanJobPeggingType</span></span>|
|<span data-ttu-id="b918c-397">KanbanJobPickingListLineType</span><span class="sxs-lookup"><span data-stu-id="b918c-397">KanbanJobPickingListLineType</span></span>|
|<span data-ttu-id="b918c-398">KanbanLineEventType</span><span class="sxs-lookup"><span data-stu-id="b918c-398">KanbanLineEventType</span></span>|
|<span data-ttu-id="b918c-399">KanbanMultiMode</span><span class="sxs-lookup"><span data-stu-id="b918c-399">KanbanMultiMode</span></span>|
|<span data-ttu-id="b918c-400">KanbanPrintInstructions</span><span class="sxs-lookup"><span data-stu-id="b918c-400">KanbanPrintInstructions</span></span>|
|<span data-ttu-id="b918c-401">KanbanProdBOMLineEventType</span><span class="sxs-lookup"><span data-stu-id="b918c-401">KanbanProdBOMLineEventType</span></span>|
|<span data-ttu-id="b918c-402">KanbanQuantityCalculationStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-402">KanbanQuantityCalculationStatus</span></span>|
|<span data-ttu-id="b918c-403">KanbanSalesLineEventType</span><span class="sxs-lookup"><span data-stu-id="b918c-403">KanbanSalesLineEventType</span></span>|
|<span data-ttu-id="b918c-404">KanbanStockReplenishmentEventType</span><span class="sxs-lookup"><span data-stu-id="b918c-404">KanbanStockReplenishmentEventType</span></span>|
|<span data-ttu-id="b918c-405">LeanBOMLineReservationMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-405">LeanBOMLineReservationMethod</span></span>|
|<span data-ttu-id="b918c-406">LeanCostingUnusedQtyType</span><span class="sxs-lookup"><span data-stu-id="b918c-406">LeanCostingUnusedQtyType</span></span>|
|<span data-ttu-id="b918c-407">LeanHandlingUnitEmptyPolicy</span><span class="sxs-lookup"><span data-stu-id="b918c-407">LeanHandlingUnitEmptyPolicy</span></span>|
|<span data-ttu-id="b918c-408">LeanInventoryControl</span><span class="sxs-lookup"><span data-stu-id="b918c-408">LeanInventoryControl</span></span>|
|<span data-ttu-id="b918c-409">LeanPeggedEventType</span><span class="sxs-lookup"><span data-stu-id="b918c-409">LeanPeggedEventType</span></span>|
|<span data-ttu-id="b918c-410">LeanPlanJobReferenceTypes</span><span class="sxs-lookup"><span data-stu-id="b918c-410">LeanPlanJobReferenceTypes</span></span>|
|<span data-ttu-id="b918c-411">LeanProductionFlowCostingStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-411">LeanProductionFlowCostingStatus</span></span>|
|<span data-ttu-id="b918c-412">LeanProductionFlowVisualizationViewMode</span><span class="sxs-lookup"><span data-stu-id="b918c-412">LeanProductionFlowVisualizationViewMode</span></span>|
|<span data-ttu-id="b918c-413">LeanProductTypes</span><span class="sxs-lookup"><span data-stu-id="b918c-413">LeanProductTypes</span></span>|
|<span data-ttu-id="b918c-414">LeanTaktStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-414">LeanTaktStatus</span></span>|
|<span data-ttu-id="b918c-415">LedgerPostingType</span><span class="sxs-lookup"><span data-stu-id="b918c-415">LedgerPostingType</span></span>|
|<span data-ttu-id="b918c-416">LedgerTransTxt</span><span class="sxs-lookup"><span data-stu-id="b918c-416">LedgerTransTxt</span></span>|
|<span data-ttu-id="b918c-417">MarkupAllocateAfter</span><span class="sxs-lookup"><span data-stu-id="b918c-417">MarkupAllocateAfter</span></span>|
|<span data-ttu-id="b918c-418">MarkupCategory</span><span class="sxs-lookup"><span data-stu-id="b918c-418">MarkupCategory</span></span>|
|<span data-ttu-id="b918c-419">MCRBrokerContractStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-419">MCRBrokerContractStatus</span></span>|
|<span data-ttu-id="b918c-420">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="b918c-420">MCRCustSearchType</span></span>|
|<span data-ttu-id="b918c-421">MCRFullTextSearchType</span><span class="sxs-lookup"><span data-stu-id="b918c-421">MCRFullTextSearchType</span></span>|
|<span data-ttu-id="b918c-422">MCRInstallPlanApplyMiscCharge</span><span class="sxs-lookup"><span data-stu-id="b918c-422">MCRInstallPlanApplyMiscCharge</span></span>|
|<span data-ttu-id="b918c-423">MCRItemListGenerationType</span><span class="sxs-lookup"><span data-stu-id="b918c-423">MCRItemListGenerationType</span></span>|
|<span data-ttu-id="b918c-424">MCRPickingPrompt</span><span class="sxs-lookup"><span data-stu-id="b918c-424">MCRPickingPrompt</span></span>|
|<span data-ttu-id="b918c-425">MCRPickingSessionStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-425">MCRPickingSessionStatus</span></span>|
|<span data-ttu-id="b918c-426">MCRPickingWaveStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-426">MCRPickingWaveStatus</span></span>|
|<span data-ttu-id="b918c-427">MCRPriceHistoryType</span><span class="sxs-lookup"><span data-stu-id="b918c-427">MCRPriceHistoryType</span></span>|
|<span data-ttu-id="b918c-428">MCRRoyaltyLineBreakType</span><span class="sxs-lookup"><span data-stu-id="b918c-428">MCRRoyaltyLineBreakType</span></span>|
|<span data-ttu-id="b918c-429">MCRRoyaltyTakenFrom</span><span class="sxs-lookup"><span data-stu-id="b918c-429">MCRRoyaltyTakenFrom</span></span>|
|<span data-ttu-id="b918c-430">MCRRoyaltyTransactionType</span><span class="sxs-lookup"><span data-stu-id="b918c-430">MCRRoyaltyTransactionType</span></span>|
|<span data-ttu-id="b918c-431">MCRRoyaltyUnitType</span><span class="sxs-lookup"><span data-stu-id="b918c-431">MCRRoyaltyUnitType</span></span>|
|<span data-ttu-id="b918c-432">MCRRoyaltyUOMOption</span><span class="sxs-lookup"><span data-stu-id="b918c-432">MCRRoyaltyUOMOption</span></span>|
|<span data-ttu-id="b918c-433">MCRSalesOrderDetailStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-433">MCRSalesOrderDetailStatus</span></span>|
|<span data-ttu-id="b918c-434">ModuleInventCustVend</span><span class="sxs-lookup"><span data-stu-id="b918c-434">ModuleInventCustVend</span></span>|
|<span data-ttu-id="b918c-435">ModuleInventPurchSales</span><span class="sxs-lookup"><span data-stu-id="b918c-435">ModuleInventPurchSales</span></span>|
|<span data-ttu-id="b918c-436">OriginalDocument</span><span class="sxs-lookup"><span data-stu-id="b918c-436">OriginalDocument</span></span>|
|<span data-ttu-id="b918c-437">PaymDocumentType</span><span class="sxs-lookup"><span data-stu-id="b918c-437">PaymDocumentType</span></span>|
|<span data-ttu-id="b918c-438">PCExpressionEditorSymbolType</span><span class="sxs-lookup"><span data-stu-id="b918c-438">PCExpressionEditorSymbolType</span></span>|
|<span data-ttu-id="b918c-439">PCLookupMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-439">PCLookupMethod</span></span>|
|<span data-ttu-id="b918c-440">PCNewSelectComponent</span><span class="sxs-lookup"><span data-stu-id="b918c-440">PCNewSelectComponent</span></span>|
|<span data-ttu-id="b918c-441">PCRequirement</span><span class="sxs-lookup"><span data-stu-id="b918c-441">PCRequirement</span></span>|
|<span data-ttu-id="b918c-442">PCTableConstraintType</span><span class="sxs-lookup"><span data-stu-id="b918c-442">PCTableConstraintType</span></span>|
|<span data-ttu-id="b918c-443">PDSAdjustmentPrinciple</span><span class="sxs-lookup"><span data-stu-id="b918c-443">PDSAdjustmentPrinciple</span></span>|
|<span data-ttu-id="b918c-444">PdsBatchAttribToleranceAction</span><span class="sxs-lookup"><span data-stu-id="b918c-444">PdsBatchAttribToleranceAction</span></span>|
|<span data-ttu-id="b918c-445">PdsBatchAttribUpdateType</span><span class="sxs-lookup"><span data-stu-id="b918c-445">PdsBatchAttribUpdateType</span></span>|
|<span data-ttu-id="b918c-446">PDSCalcElementBase</span><span class="sxs-lookup"><span data-stu-id="b918c-446">PDSCalcElementBase</span></span>|
|<span data-ttu-id="b918c-447">PDSCompensationPrincipleEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-447">PDSCompensationPrincipleEnum</span></span>|
|<span data-ttu-id="b918c-448">PDSElementTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-448">PDSElementTypeEnum</span></span>|
|<span data-ttu-id="b918c-449">PDSIngredientTypeEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-449">PDSIngredientTypeEnum</span></span>|
|<span data-ttu-id="b918c-450">PdsMRCDocumentStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-450">PdsMRCDocumentStatus</span></span>|
|<span data-ttu-id="b918c-451">PdsMRCEffectiveDateBasis</span><span class="sxs-lookup"><span data-stu-id="b918c-451">PdsMRCEffectiveDateBasis</span></span>|
|<span data-ttu-id="b918c-452">PdsMRCEventModule</span><span class="sxs-lookup"><span data-stu-id="b918c-452">PdsMRCEventModule</span></span>|
|<span data-ttu-id="b918c-453">PdsMRCEventType</span><span class="sxs-lookup"><span data-stu-id="b918c-453">PdsMRCEventType</span></span>|
|<span data-ttu-id="b918c-454">PdsMRCListType</span><span class="sxs-lookup"><span data-stu-id="b918c-454">PdsMRCListType</span></span>|
|<span data-ttu-id="b918c-455">PdsPaymtType</span><span class="sxs-lookup"><span data-stu-id="b918c-455">PdsPaymtType</span></span>|
|<span data-ttu-id="b918c-456">PDSPotencyAttribRecordingEnum</span><span class="sxs-lookup"><span data-stu-id="b918c-456">PDSPotencyAttribRecordingEnum</span></span>|
|<span data-ttu-id="b918c-457">PdsRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="b918c-457">PdsRebateCalcDateType</span></span>|
|<span data-ttu-id="b918c-458">PdsRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="b918c-458">PdsRebateTakenFrom</span></span>|
|<span data-ttu-id="b918c-459">PdsRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="b918c-459">PdsRebateUOMOption</span></span>|
|<span data-ttu-id="b918c-460">PdsSameLotError</span><span class="sxs-lookup"><span data-stu-id="b918c-460">PdsSameLotError</span></span>|
|<span data-ttu-id="b918c-461">pdsTMAJournalPosting</span><span class="sxs-lookup"><span data-stu-id="b918c-461">pdsTMAJournalPosting</span></span>|
|<span data-ttu-id="b918c-462">PdsUpdateBatchDate</span><span class="sxs-lookup"><span data-stu-id="b918c-462">PdsUpdateBatchDate</span></span>|
|<span data-ttu-id="b918c-463">PdsUpdateDispositionStatus_Quality</span><span class="sxs-lookup"><span data-stu-id="b918c-463">PdsUpdateDispositionStatus_Quality</span></span>|
|<span data-ttu-id="b918c-464">PlanActivityCreateRelationType</span><span class="sxs-lookup"><span data-stu-id="b918c-464">PlanActivityCreateRelationType</span></span>|
|<span data-ttu-id="b918c-465">PlanActivityProductionFlowActivityType</span><span class="sxs-lookup"><span data-stu-id="b918c-465">PlanActivityProductionFlowActivityType</span></span>|
|<span data-ttu-id="b918c-466">PlanTypes</span><span class="sxs-lookup"><span data-stu-id="b918c-466">PlanTypes</span></span>|
|<span data-ttu-id="b918c-467">PmfCostAllocationMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-467">PmfCostAllocationMethod</span></span>|
|<span data-ttu-id="b918c-468">PmfOrderType</span><span class="sxs-lookup"><span data-stu-id="b918c-468">PmfOrderType</span></span>|
|<span data-ttu-id="b918c-469">PmfOrderTypeFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-469">PmfOrderTypeFilter</span></span>|
|<span data-ttu-id="b918c-470">PmfProdType</span><span class="sxs-lookup"><span data-stu-id="b918c-470">PmfProdType</span></span>|
|<span data-ttu-id="b918c-471">PMFSeqCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="b918c-471">PMFSeqCalendarPeriod</span></span>|
|<span data-ttu-id="b918c-472">PriceBase</span><span class="sxs-lookup"><span data-stu-id="b918c-472">PriceBase</span></span>|
|<span data-ttu-id="b918c-473">PriceDiscPurchasePromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="b918c-473">PriceDiscPurchasePromptSystemSource</span></span>|
|<span data-ttu-id="b918c-474">PriceDiscSalesPromptSystemSource</span><span class="sxs-lookup"><span data-stu-id="b918c-474">PriceDiscSalesPromptSystemSource</span></span>|
|<span data-ttu-id="b918c-475">PriceGroupType</span><span class="sxs-lookup"><span data-stu-id="b918c-475">PriceGroupType</span></span>|
|<span data-ttu-id="b918c-476">PriceSalesPurch</span><span class="sxs-lookup"><span data-stu-id="b918c-476">PriceSalesPurch</span></span>|
|<span data-ttu-id="b918c-477">PriceType</span><span class="sxs-lookup"><span data-stu-id="b918c-477">PriceType</span></span>|
|<span data-ttu-id="b918c-478">ProcCategoryAdministrationActivity</span><span class="sxs-lookup"><span data-stu-id="b918c-478">ProcCategoryAdministrationActivity</span></span>|
|<span data-ttu-id="b918c-479">ProdBOMConsumpProposal</span><span class="sxs-lookup"><span data-stu-id="b918c-479">ProdBOMConsumpProposal</span></span>|
|<span data-ttu-id="b918c-480">ProdBOMJournalQty</span><span class="sxs-lookup"><span data-stu-id="b918c-480">ProdBOMJournalQty</span></span>|
|<span data-ttu-id="b918c-481">ProdBOMJournalSplit</span><span class="sxs-lookup"><span data-stu-id="b918c-481">ProdBOMJournalSplit</span></span>|
|<span data-ttu-id="b918c-482">ProdErrorCause</span><span class="sxs-lookup"><span data-stu-id="b918c-482">ProdErrorCause</span></span>|
|<span data-ttu-id="b918c-483">ProdGanttJobColorType</span><span class="sxs-lookup"><span data-stu-id="b918c-483">ProdGanttJobColorType</span></span>|
|<span data-ttu-id="b918c-484">ProdGanttLoad</span><span class="sxs-lookup"><span data-stu-id="b918c-484">ProdGanttLoad</span></span>|
|<span data-ttu-id="b918c-485">ProdGanttRouteColorType</span><span class="sxs-lookup"><span data-stu-id="b918c-485">ProdGanttRouteColorType</span></span>|
|<span data-ttu-id="b918c-486">ProdJournalCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="b918c-486">ProdJournalCleanUpMode</span></span>|
|<span data-ttu-id="b918c-487">ProdMode</span><span class="sxs-lookup"><span data-stu-id="b918c-487">ProdMode</span></span>|
|<span data-ttu-id="b918c-488">ProdNotificationLevel</span><span class="sxs-lookup"><span data-stu-id="b918c-488">ProdNotificationLevel</span></span>|
|<span data-ttu-id="b918c-489">ProdParamInventDimLookup</span><span class="sxs-lookup"><span data-stu-id="b918c-489">ProdParamInventDimLookup</span></span>|
|<span data-ttu-id="b918c-490">ProdParmType</span><span class="sxs-lookup"><span data-stu-id="b918c-490">ProdParmType</span></span>|
|<span data-ttu-id="b918c-491">ProdRefLookUp</span><span class="sxs-lookup"><span data-stu-id="b918c-491">ProdRefLookUp</span></span>|
|<span data-ttu-id="b918c-492">ProdRouteJobCurrentFormTabId</span><span class="sxs-lookup"><span data-stu-id="b918c-492">ProdRouteJobCurrentFormTabId</span></span>|
|<span data-ttu-id="b918c-493">ProdSchedDirection</span><span class="sxs-lookup"><span data-stu-id="b918c-493">ProdSchedDirection</span></span>|
|<span data-ttu-id="b918c-494">ProdScrapMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-494">ProdScrapMethod</span></span>|
|<span data-ttu-id="b918c-495">ProdStandardCostVariance</span><span class="sxs-lookup"><span data-stu-id="b918c-495">ProdStandardCostVariance</span></span>|
|<span data-ttu-id="b918c-496">ProdStatusAll</span><span class="sxs-lookup"><span data-stu-id="b918c-496">ProdStatusAll</span></span>|
|<span data-ttu-id="b918c-497">ProdStatusType</span><span class="sxs-lookup"><span data-stu-id="b918c-497">ProdStatusType</span></span>|
|<span data-ttu-id="b918c-498">ProductionTransType</span><span class="sxs-lookup"><span data-stu-id="b918c-498">ProductionTransType</span></span>|
|<span data-ttu-id="b918c-499">ProdUpdateJour</span><span class="sxs-lookup"><span data-stu-id="b918c-499">ProdUpdateJour</span></span>|
|<span data-ttu-id="b918c-500">ProdWHSReleasePolicy</span><span class="sxs-lookup"><span data-stu-id="b918c-500">ProdWHSReleasePolicy</span></span>|
|<span data-ttu-id="b918c-501">ProdWIPType_NA</span><span class="sxs-lookup"><span data-stu-id="b918c-501">ProdWIPType_NA</span></span>|
|<span data-ttu-id="b918c-502">PurchaseOrderResponseAction</span><span class="sxs-lookup"><span data-stu-id="b918c-502">PurchaseOrderResponseAction</span></span>|
|<span data-ttu-id="b918c-503">PurchaseType</span><span class="sxs-lookup"><span data-stu-id="b918c-503">PurchaseType</span></span>|
|<span data-ttu-id="b918c-504">PurchasingTransactionType</span><span class="sxs-lookup"><span data-stu-id="b918c-504">PurchasingTransactionType</span></span>|
|<span data-ttu-id="b918c-505">PurchCORReceivingMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-505">PurchCORReceivingMethod</span></span>|
|<span data-ttu-id="b918c-506">PurchCORRejectStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-506">PurchCORRejectStatus</span></span>|
|<span data-ttu-id="b918c-507">PurchCovRef</span><span class="sxs-lookup"><span data-stu-id="b918c-507">PurchCovRef</span></span>|
|<span data-ttu-id="b918c-508">PurchDlvAddr</span><span class="sxs-lookup"><span data-stu-id="b918c-508">PurchDlvAddr</span></span>|
|<span data-ttu-id="b918c-509">PurchLineBackOrderViews</span><span class="sxs-lookup"><span data-stu-id="b918c-509">PurchLineBackOrderViews</span></span>|
|<span data-ttu-id="b918c-510">PurchLineDeliveryFulfillment</span><span class="sxs-lookup"><span data-stu-id="b918c-510">PurchLineDeliveryFulfillment</span></span>|
|<span data-ttu-id="b918c-511">PurchLineDeliveryPrecision</span><span class="sxs-lookup"><span data-stu-id="b918c-511">PurchLineDeliveryPrecision</span></span>|
|<span data-ttu-id="b918c-512">PurchMatchingPolicyOverrideOption</span><span class="sxs-lookup"><span data-stu-id="b918c-512">PurchMatchingPolicyOverrideOption</span></span>|
|<span data-ttu-id="b918c-513">PurchPrepayApplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b918c-513">PurchPrepayApplicationPolicy</span></span>|
|<span data-ttu-id="b918c-514">PurchPriceDateType</span><span class="sxs-lookup"><span data-stu-id="b918c-514">PurchPriceDateType</span></span>|
|<span data-ttu-id="b918c-515">PurchPurchaseOrderCreationMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-515">PurchPurchaseOrderCreationMethod</span></span>|
|<span data-ttu-id="b918c-516">PurchReApprovalPolicyRuleViewType</span><span class="sxs-lookup"><span data-stu-id="b918c-516">PurchReApprovalPolicyRuleViewType</span></span>|
|<span data-ttu-id="b918c-517">PurchReqAuthorizationSpecificReporting</span><span class="sxs-lookup"><span data-stu-id="b918c-517">PurchReqAuthorizationSpecificReporting</span></span>|
|<span data-ttu-id="b918c-518">PurchReqAutoCreatePurch</span><span class="sxs-lookup"><span data-stu-id="b918c-518">PurchReqAutoCreatePurch</span></span>|
|<span data-ttu-id="b918c-519">PurchReqCatalogAllNon</span><span class="sxs-lookup"><span data-stu-id="b918c-519">PurchReqCatalogAllNon</span></span>|
|<span data-ttu-id="b918c-520">PurchReqConsolidationActiveStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-520">PurchReqConsolidationActiveStatus</span></span>|
|<span data-ttu-id="b918c-521">PurchReqConsolidationPriority</span><span class="sxs-lookup"><span data-stu-id="b918c-521">PurchReqConsolidationPriority</span></span>|
|<span data-ttu-id="b918c-522">PurchReqConsolidationStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-522">PurchReqConsolidationStatus</span></span>|
|<span data-ttu-id="b918c-523">PurchReqCreationStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-523">PurchReqCreationStatus</span></span>|
|<span data-ttu-id="b918c-524">PurchReqItemDescriptionTransfer</span><span class="sxs-lookup"><span data-stu-id="b918c-524">PurchReqItemDescriptionTransfer</span></span>|
|<span data-ttu-id="b918c-525">PurchReqItemFilterType</span><span class="sxs-lookup"><span data-stu-id="b918c-525">PurchReqItemFilterType</span></span>|
|<span data-ttu-id="b918c-526">PurchReqOnBehalfReports</span><span class="sxs-lookup"><span data-stu-id="b918c-526">PurchReqOnBehalfReports</span></span>|
|<span data-ttu-id="b918c-527">PurchReqOriginationAuthorizationView</span><span class="sxs-lookup"><span data-stu-id="b918c-527">PurchReqOriginationAuthorizationView</span></span>|
|<span data-ttu-id="b918c-528">PurchReqProcessingState</span><span class="sxs-lookup"><span data-stu-id="b918c-528">PurchReqProcessingState</span></span>|
|<span data-ttu-id="b918c-529">PurchReqQuestionnaireAggregateStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-529">PurchReqQuestionnaireAggregateStatus</span></span>|
|<span data-ttu-id="b918c-530">PurchReqQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-530">PurchReqQuestionnaireStatus</span></span>|
|<span data-ttu-id="b918c-531">PurchReqReportSortOrder</span><span class="sxs-lookup"><span data-stu-id="b918c-531">PurchReqReportSortOrder</span></span>|
|<span data-ttu-id="b918c-532">PurchReqReportStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-532">PurchReqReportStatus</span></span>|
|<span data-ttu-id="b918c-533">PurchReqReviewStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-533">PurchReqReviewStatus</span></span>|
|<span data-ttu-id="b918c-534">PurchReqRFQRequirement</span><span class="sxs-lookup"><span data-stu-id="b918c-534">PurchReqRFQRequirement</span></span>|
|<span data-ttu-id="b918c-535">PurchReqRFQType</span><span class="sxs-lookup"><span data-stu-id="b918c-535">PurchReqRFQType</span></span>|
|<span data-ttu-id="b918c-536">PurchReqSaveChanges</span><span class="sxs-lookup"><span data-stu-id="b918c-536">PurchReqSaveChanges</span></span>|
|<span data-ttu-id="b918c-537">PurchReqStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-537">PurchReqStatus</span></span>|
|<span data-ttu-id="b918c-538">PurchReqType</span><span class="sxs-lookup"><span data-stu-id="b918c-538">PurchReqType</span></span>|
|<span data-ttu-id="b918c-539">PurchReqWorkflowState</span><span class="sxs-lookup"><span data-stu-id="b918c-539">PurchReqWorkflowState</span></span>|
|<span data-ttu-id="b918c-540">PurchRFQQuestionnaireStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-540">PurchRFQQuestionnaireStatus</span></span>|
|<span data-ttu-id="b918c-541">PurchRFQStatusVendor</span><span class="sxs-lookup"><span data-stu-id="b918c-541">PurchRFQStatusVendor</span></span>|
|<span data-ttu-id="b918c-542">PurchRFQType</span><span class="sxs-lookup"><span data-stu-id="b918c-542">PurchRFQType</span></span>|
|<span data-ttu-id="b918c-543">PurchTableFormId</span><span class="sxs-lookup"><span data-stu-id="b918c-543">PurchTableFormId</span></span>|
|<span data-ttu-id="b918c-544">PurchTableListPage</span><span class="sxs-lookup"><span data-stu-id="b918c-544">PurchTableListPage</span></span>|
|<span data-ttu-id="b918c-545">PurchTableMode</span><span class="sxs-lookup"><span data-stu-id="b918c-545">PurchTableMode</span></span>|
|<span data-ttu-id="b918c-546">PurchTotalsCachingMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-546">PurchTotalsCachingMethod</span></span>|
|<span data-ttu-id="b918c-547">PurchUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-547">PurchUpdate</span></span>|
|<span data-ttu-id="b918c-548">PurchVendorPortalShowResponseType</span><span class="sxs-lookup"><span data-stu-id="b918c-548">PurchVendorPortalShowResponseType</span></span>|
|<span data-ttu-id="b918c-549">QuotationType</span><span class="sxs-lookup"><span data-stu-id="b918c-549">QuotationType</span></span>|
|<span data-ttu-id="b918c-550">ReqBOMRouteCreated</span><span class="sxs-lookup"><span data-stu-id="b918c-550">ReqBOMRouteCreated</span></span>|
|<span data-ttu-id="b918c-551">ReqCurrentDaySchedFrom</span><span class="sxs-lookup"><span data-stu-id="b918c-551">ReqCurrentDaySchedFrom</span></span>|
|<span data-ttu-id="b918c-552">ReqDemPlanDataSourceType</span><span class="sxs-lookup"><span data-stu-id="b918c-552">ReqDemPlanDataSourceType</span></span>|
|<span data-ttu-id="b918c-553">ReqDemPlanDemandCategory</span><span class="sxs-lookup"><span data-stu-id="b918c-553">ReqDemPlanDemandCategory</span></span>|
|<span data-ttu-id="b918c-554">ReqDemPlanForecastAttributeType</span><span class="sxs-lookup"><span data-stu-id="b918c-554">ReqDemPlanForecastAttributeType</span></span>|
|<span data-ttu-id="b918c-555">ReqDemPlanForecastingStrategy</span><span class="sxs-lookup"><span data-stu-id="b918c-555">ReqDemPlanForecastingStrategy</span></span>|
|<span data-ttu-id="b918c-556">ReqDemPlanForecastType</span><span class="sxs-lookup"><span data-stu-id="b918c-556">ReqDemPlanForecastType</span></span>|
|<span data-ttu-id="b918c-557">ReqDisplayDelay</span><span class="sxs-lookup"><span data-stu-id="b918c-557">ReqDisplayDelay</span></span>|
|<span data-ttu-id="b918c-558">ReqForecastReducedBy</span><span class="sxs-lookup"><span data-stu-id="b918c-558">ReqForecastReducedBy</span></span>|
|<span data-ttu-id="b918c-559">ReqGanttColorType</span><span class="sxs-lookup"><span data-stu-id="b918c-559">ReqGanttColorType</span></span>|
|<span data-ttu-id="b918c-560">ReqGanttShow</span><span class="sxs-lookup"><span data-stu-id="b918c-560">ReqGanttShow</span></span>|
|<span data-ttu-id="b918c-561">ReqItemJournalType</span><span class="sxs-lookup"><span data-stu-id="b918c-561">ReqItemJournalType</span></span>|
|<span data-ttu-id="b918c-562">ReqItemTableWizardPurpose</span><span class="sxs-lookup"><span data-stu-id="b918c-562">ReqItemTableWizardPurpose</span></span>|
|<span data-ttu-id="b918c-563">ReqMarkUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-563">ReqMarkUpdate</span></span>|
|<span data-ttu-id="b918c-564">ReqPeggingAssignmentType</span><span class="sxs-lookup"><span data-stu-id="b918c-564">ReqPeggingAssignmentType</span></span>|
|<span data-ttu-id="b918c-565">ReqPeggingType</span><span class="sxs-lookup"><span data-stu-id="b918c-565">ReqPeggingType</span></span>|
|<span data-ttu-id="b918c-566">ReqPlannedOrderLeveling</span><span class="sxs-lookup"><span data-stu-id="b918c-566">ReqPlannedOrderLeveling</span></span>|
|<span data-ttu-id="b918c-567">ReqPlanType</span><span class="sxs-lookup"><span data-stu-id="b918c-567">ReqPlanType</span></span>|
|<span data-ttu-id="b918c-568">ReqPOStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-568">ReqPOStatus</span></span>|
|<span data-ttu-id="b918c-569">ReqQtyAmount</span><span class="sxs-lookup"><span data-stu-id="b918c-569">ReqQtyAmount</span></span>|
|<span data-ttu-id="b918c-570">ReqRefType</span><span class="sxs-lookup"><span data-stu-id="b918c-570">ReqRefType</span></span>|
|<span data-ttu-id="b918c-571">ReqRefTypeShort</span><span class="sxs-lookup"><span data-stu-id="b918c-571">ReqRefTypeShort</span></span>|
|<span data-ttu-id="b918c-572">ReqRefTypeTrunc</span><span class="sxs-lookup"><span data-stu-id="b918c-572">ReqRefTypeTrunc</span></span>|
|<span data-ttu-id="b918c-573">ReqTraceMessageType</span><span class="sxs-lookup"><span data-stu-id="b918c-573">ReqTraceMessageType</span></span>|
|<span data-ttu-id="b918c-574">ReqTransFuturesActionPartType</span><span class="sxs-lookup"><span data-stu-id="b918c-574">ReqTransFuturesActionPartType</span></span>|
|<span data-ttu-id="b918c-575">ReturnCodeType</span><span class="sxs-lookup"><span data-stu-id="b918c-575">ReturnCodeType</span></span>|
|<span data-ttu-id="b918c-576">ReturnCycleTimeScope</span><span class="sxs-lookup"><span data-stu-id="b918c-576">ReturnCycleTimeScope</span></span>|
|<span data-ttu-id="b918c-577">ReturnReasonCodeDispExtended</span><span class="sxs-lookup"><span data-stu-id="b918c-577">ReturnReasonCodeDispExtended</span></span>|
|<span data-ttu-id="b918c-578">ReturnReasonDispCode</span><span class="sxs-lookup"><span data-stu-id="b918c-578">ReturnReasonDispCode</span></span>|
|<span data-ttu-id="b918c-579">ReturnUpdateAction</span><span class="sxs-lookup"><span data-stu-id="b918c-579">ReturnUpdateAction</span></span>|
|<span data-ttu-id="b918c-580">RouteFormula</span><span class="sxs-lookup"><span data-stu-id="b918c-580">RouteFormula</span></span>|
|<span data-ttu-id="b918c-581">RouteOprPriority</span><span class="sxs-lookup"><span data-stu-id="b918c-581">RouteOprPriority</span></span>|
|<span data-ttu-id="b918c-582">SalesBasketType</span><span class="sxs-lookup"><span data-stu-id="b918c-582">SalesBasketType</span></span>|
|<span data-ttu-id="b918c-583">SalesBatch</span><span class="sxs-lookup"><span data-stu-id="b918c-583">SalesBatch</span></span>|
|<span data-ttu-id="b918c-584">SalesCheckForPickup</span><span class="sxs-lookup"><span data-stu-id="b918c-584">SalesCheckForPickup</span></span>|
|<span data-ttu-id="b918c-585">SalesCheckQtyCachKey</span><span class="sxs-lookup"><span data-stu-id="b918c-585">SalesCheckQtyCachKey</span></span>|
|<span data-ttu-id="b918c-586">SalesDeliveryTimeState</span><span class="sxs-lookup"><span data-stu-id="b918c-586">SalesDeliveryTimeState</span></span>|
|<span data-ttu-id="b918c-587">SalesDocumentTimezonePreference</span><span class="sxs-lookup"><span data-stu-id="b918c-587">SalesDocumentTimezonePreference</span></span>|
|<span data-ttu-id="b918c-588">SalesPriceDateType</span><span class="sxs-lookup"><span data-stu-id="b918c-588">SalesPriceDateType</span></span>|
|<span data-ttu-id="b918c-589">SalesPriceModelBasic</span><span class="sxs-lookup"><span data-stu-id="b918c-589">SalesPriceModelBasic</span></span>|
|<span data-ttu-id="b918c-590">SalesPurchCopy</span><span class="sxs-lookup"><span data-stu-id="b918c-590">SalesPurchCopy</span></span>|
|<span data-ttu-id="b918c-591">SalesPurchCycleAction</span><span class="sxs-lookup"><span data-stu-id="b918c-591">SalesPurchCycleAction</span></span>|
|<span data-ttu-id="b918c-592">SalesPurchGroup</span><span class="sxs-lookup"><span data-stu-id="b918c-592">SalesPurchGroup</span></span>|
|<span data-ttu-id="b918c-593">SalesPurchParmCleanUpMode</span><span class="sxs-lookup"><span data-stu-id="b918c-593">SalesPurchParmCleanUpMode</span></span>|
|<span data-ttu-id="b918c-594">SalesQuotationFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-594">SalesQuotationFilter</span></span>|
|<span data-ttu-id="b918c-595">SalesQuotationLinkToProject</span><span class="sxs-lookup"><span data-stu-id="b918c-595">SalesQuotationLinkToProject</span></span>|
|<span data-ttu-id="b918c-596">SalesQuotationListPage</span><span class="sxs-lookup"><span data-stu-id="b918c-596">SalesQuotationListPage</span></span>|
|<span data-ttu-id="b918c-597">SalesQuotationPriceConversion</span><span class="sxs-lookup"><span data-stu-id="b918c-597">SalesQuotationPriceConversion</span></span>|
|<span data-ttu-id="b918c-598">SalesQuotationPriceSimResult</span><span class="sxs-lookup"><span data-stu-id="b918c-598">SalesQuotationPriceSimResult</span></span>|
|<span data-ttu-id="b918c-599">SalesQuotationTypeListPage</span><span class="sxs-lookup"><span data-stu-id="b918c-599">SalesQuotationTypeListPage</span></span>|
|<span data-ttu-id="b918c-600">SalesShipping</span><span class="sxs-lookup"><span data-stu-id="b918c-600">SalesShipping</span></span>|
|<span data-ttu-id="b918c-601">SalesSourcingOrigin</span><span class="sxs-lookup"><span data-stu-id="b918c-601">SalesSourcingOrigin</span></span>|
|<span data-ttu-id="b918c-602">SalesStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-602">SalesStatus</span></span>|
|<span data-ttu-id="b918c-603">SalesTableFormId</span><span class="sxs-lookup"><span data-stu-id="b918c-603">SalesTableFormId</span></span>|
|<span data-ttu-id="b918c-604">SalesTableListPage</span><span class="sxs-lookup"><span data-stu-id="b918c-604">SalesTableListPage</span></span>|
|<span data-ttu-id="b918c-605">SalesTableMode</span><span class="sxs-lookup"><span data-stu-id="b918c-605">SalesTableMode</span></span>|
|<span data-ttu-id="b918c-606">SalesType</span><span class="sxs-lookup"><span data-stu-id="b918c-606">SalesType</span></span>|
|<span data-ttu-id="b918c-607">SalesUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-607">SalesUpdate</span></span>|
|<span data-ttu-id="b918c-608">ShipCarrierDlvType</span><span class="sxs-lookup"><span data-stu-id="b918c-608">ShipCarrierDlvType</span></span>|
|<span data-ttu-id="b918c-609">ShipCarrierFreightApplied</span><span class="sxs-lookup"><span data-stu-id="b918c-609">ShipCarrierFreightApplied</span></span>|
|<span data-ttu-id="b918c-610">ShipCarrierMkUpFreight</span><span class="sxs-lookup"><span data-stu-id="b918c-610">ShipCarrierMkUpFreight</span></span>|
|<span data-ttu-id="b918c-611">SMAInvoiceProjectSelection</span><span class="sxs-lookup"><span data-stu-id="b918c-611">SMAInvoiceProjectSelection</span></span>|
|<span data-ttu-id="b918c-612">SMAItemSetupType</span><span class="sxs-lookup"><span data-stu-id="b918c-612">SMAItemSetupType</span></span>|
|<span data-ttu-id="b918c-613">SMAProjectSelection</span><span class="sxs-lookup"><span data-stu-id="b918c-613">SMAProjectSelection</span></span>|
|<span data-ttu-id="b918c-614">SMAReasonType</span><span class="sxs-lookup"><span data-stu-id="b918c-614">SMAReasonType</span></span>|
|<span data-ttu-id="b918c-615">SMAServiceBOMChangeAction</span><span class="sxs-lookup"><span data-stu-id="b918c-615">SMAServiceBOMChangeAction</span></span>|
|<span data-ttu-id="b918c-616">SMAServiceFunctionType</span><span class="sxs-lookup"><span data-stu-id="b918c-616">SMAServiceFunctionType</span></span>|
|<span data-ttu-id="b918c-617">SMAServiceLevelAgreementLogType</span><span class="sxs-lookup"><span data-stu-id="b918c-617">SMAServiceLevelAgreementLogType</span></span>|
|<span data-ttu-id="b918c-618">SMAServiceOrderActionType</span><span class="sxs-lookup"><span data-stu-id="b918c-618">SMAServiceOrderActionType</span></span>|
|<span data-ttu-id="b918c-619">SMAServiceOrderFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-619">SMAServiceOrderFilter</span></span>|
|<span data-ttu-id="b918c-620">SMAServiceOrderOrigin</span><span class="sxs-lookup"><span data-stu-id="b918c-620">SMAServiceOrderOrigin</span></span>|
|<span data-ttu-id="b918c-621">SMAServiceOrderProgress</span><span class="sxs-lookup"><span data-stu-id="b918c-621">SMAServiceOrderProgress</span></span>|
|<span data-ttu-id="b918c-622">SMAServiceTaskTitleOption</span><span class="sxs-lookup"><span data-stu-id="b918c-622">SMAServiceTaskTitleOption</span></span>|
|<span data-ttu-id="b918c-623">SMASubscriptionPeriodType</span><span class="sxs-lookup"><span data-stu-id="b918c-623">SMASubscriptionPeriodType</span></span>|
|<span data-ttu-id="b918c-624">SMAWizardCreateType</span><span class="sxs-lookup"><span data-stu-id="b918c-624">SMAWizardCreateType</span></span>|
|<span data-ttu-id="b918c-625">smmAccountNumToCreate</span><span class="sxs-lookup"><span data-stu-id="b918c-625">smmAccountNumToCreate</span></span>|
|<span data-ttu-id="b918c-626">smmActivityParentType</span><span class="sxs-lookup"><span data-stu-id="b918c-626">smmActivityParentType</span></span>|
|<span data-ttu-id="b918c-627">smmAppointmentNThInstance</span><span class="sxs-lookup"><span data-stu-id="b918c-627">smmAppointmentNThInstance</span></span>|
|<span data-ttu-id="b918c-628">smmBusinessRelationsListFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-628">smmBusinessRelationsListFilter</span></span>|
|<span data-ttu-id="b918c-629">smmBusRelTypeSourceTable</span><span class="sxs-lookup"><span data-stu-id="b918c-629">smmBusRelTypeSourceTable</span></span>|
|<span data-ttu-id="b918c-630">smmCampaignBroadcastType</span><span class="sxs-lookup"><span data-stu-id="b918c-630">smmCampaignBroadcastType</span></span>|
|<span data-ttu-id="b918c-631">smmCampaignProjectJournalType</span><span class="sxs-lookup"><span data-stu-id="b918c-631">smmCampaignProjectJournalType</span></span>|
|<span data-ttu-id="b918c-632">smmCampaignResponse</span><span class="sxs-lookup"><span data-stu-id="b918c-632">smmCampaignResponse</span></span>|
|<span data-ttu-id="b918c-633">smmCampaignsListFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-633">smmCampaignsListFilter</span></span>|
|<span data-ttu-id="b918c-634">smmContactsListFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-634">smmContactsListFilter</span></span>|
|<span data-ttu-id="b918c-635">smmCreateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="b918c-635">smmCreateOpportunityOptions</span></span>|
|<span data-ttu-id="b918c-636">smmDisplayEMailInOutlook</span><span class="sxs-lookup"><span data-stu-id="b918c-636">smmDisplayEMailInOutlook</span></span>|
|<span data-ttu-id="b918c-637">smmDragDropObjectType</span><span class="sxs-lookup"><span data-stu-id="b918c-637">smmDragDropObjectType</span></span>|
|<span data-ttu-id="b918c-638">smmDupMethods</span><span class="sxs-lookup"><span data-stu-id="b918c-638">smmDupMethods</span></span>|
|<span data-ttu-id="b918c-639">smmEMailSMS</span><span class="sxs-lookup"><span data-stu-id="b918c-639">smmEMailSMS</span></span>|
|<span data-ttu-id="b918c-640">smmEntityToCreate</span><span class="sxs-lookup"><span data-stu-id="b918c-640">smmEntityToCreate</span></span>|
|<span data-ttu-id="b918c-641">smmFieldDelimiters</span><span class="sxs-lookup"><span data-stu-id="b918c-641">smmFieldDelimiters</span></span>|
|<span data-ttu-id="b918c-642">smmLeadsListFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-642">smmLeadsListFilter</span></span>|
|<span data-ttu-id="b918c-643">smmLogType</span><span class="sxs-lookup"><span data-stu-id="b918c-643">smmLogType</span></span>|
|<span data-ttu-id="b918c-644">smmOpportunitiesListFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-644">smmOpportunitiesListFilter</span></span>|
|<span data-ttu-id="b918c-645">smmOpportunityAssociation</span><span class="sxs-lookup"><span data-stu-id="b918c-645">smmOpportunityAssociation</span></span>|
|<span data-ttu-id="b918c-646">smmOutlookContactDeleteAction</span><span class="sxs-lookup"><span data-stu-id="b918c-646">smmOutlookContactDeleteAction</span></span>|
|<span data-ttu-id="b918c-647">smmOutlookRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="b918c-647">smmOutlookRecurrenceType</span></span>|
|<span data-ttu-id="b918c-648">smmOutlookSyncPrinciple</span><span class="sxs-lookup"><span data-stu-id="b918c-648">smmOutlookSyncPrinciple</span></span>|
|<span data-ttu-id="b918c-649">smmOutlookUpdateAction</span><span class="sxs-lookup"><span data-stu-id="b918c-649">smmOutlookUpdateAction</span></span>|
|<span data-ttu-id="b918c-650">smmProjectNewExisting</span><span class="sxs-lookup"><span data-stu-id="b918c-650">smmProjectNewExisting</span></span>|
|<span data-ttu-id="b918c-651">smmQuotationAccountType</span><span class="sxs-lookup"><span data-stu-id="b918c-651">smmQuotationAccountType</span></span>|
|<span data-ttu-id="b918c-652">smmQuotationStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-652">smmQuotationStatus</span></span>|
|<span data-ttu-id="b918c-653">smmRecordDelimiters</span><span class="sxs-lookup"><span data-stu-id="b918c-653">smmRecordDelimiters</span></span>|
|<span data-ttu-id="b918c-654">smmSalesUnitMemberRelation</span><span class="sxs-lookup"><span data-stu-id="b918c-654">smmSalesUnitMemberRelation</span></span>|
|<span data-ttu-id="b918c-655">SmmSourceTypeList</span><span class="sxs-lookup"><span data-stu-id="b918c-655">SmmSourceTypeList</span></span>|
|<span data-ttu-id="b918c-656">smmSwotType</span><span class="sxs-lookup"><span data-stu-id="b918c-656">smmSwotType</span></span>|
|<span data-ttu-id="b918c-657">smmTransLogUpdateAction</span><span class="sxs-lookup"><span data-stu-id="b918c-657">smmTransLogUpdateAction</span></span>|
|<span data-ttu-id="b918c-658">smmUpdateOpportunityOptions</span><span class="sxs-lookup"><span data-stu-id="b918c-658">smmUpdateOpportunityOptions</span></span>|
|<span data-ttu-id="b918c-659">smmWarningError</span><span class="sxs-lookup"><span data-stu-id="b918c-659">smmWarningError</span></span>|
|<span data-ttu-id="b918c-660">SMAActiveAll</span><span class="sxs-lookup"><span data-stu-id="b918c-660">SMAActiveAll</span></span>|
|<span data-ttu-id="b918c-661">SMAAgreementFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-661">SMAAgreementFilter</span></span>|
|<span data-ttu-id="b918c-662">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="b918c-662">SMAAgreementTableListPageType</span></span>|
|<span data-ttu-id="b918c-663">TAMCustRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-663">TAMCustRebateApprovalStatus</span></span>|
|<span data-ttu-id="b918c-664">TAMFundStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-664">TAMFundStatus</span></span>|
|<span data-ttu-id="b918c-665">TAMFundType</span><span class="sxs-lookup"><span data-stu-id="b918c-665">TAMFundType</span></span>|
|<span data-ttu-id="b918c-666">TAMPromoCustomerType</span><span class="sxs-lookup"><span data-stu-id="b918c-666">TAMPromoCustomerType</span></span>|
|<span data-ttu-id="b918c-667">TAMPromoMerchEvent</span><span class="sxs-lookup"><span data-stu-id="b918c-667">TAMPromoMerchEvent</span></span>|
|<span data-ttu-id="b918c-668">TAMPromoMgmtApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-668">TAMPromoMgmtApprovalStatus</span></span>|
|<span data-ttu-id="b918c-669">TAMPromotionDate</span><span class="sxs-lookup"><span data-stu-id="b918c-669">TAMPromotionDate</span></span>|
|<span data-ttu-id="b918c-670">TAMPromotionMode</span><span class="sxs-lookup"><span data-stu-id="b918c-670">TAMPromotionMode</span></span>|
|<span data-ttu-id="b918c-671">TAMRebateCustInclusive</span><span class="sxs-lookup"><span data-stu-id="b918c-671">TAMRebateCustInclusive</span></span>|
|<span data-ttu-id="b918c-672">TAMRebateLineBreakType</span><span class="sxs-lookup"><span data-stu-id="b918c-672">TAMRebateLineBreakType</span></span>|
|<span data-ttu-id="b918c-673">TAMRebateStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-673">TAMRebateStatus</span></span>|
|<span data-ttu-id="b918c-674">TAMRebateUnitType</span><span class="sxs-lookup"><span data-stu-id="b918c-674">TAMRebateUnitType</span></span>|
|<span data-ttu-id="b918c-675">TAMRebateUOMOption</span><span class="sxs-lookup"><span data-stu-id="b918c-675">TAMRebateUOMOption</span></span>|
|<span data-ttu-id="b918c-676">TAMVendRebateApprovalStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-676">TAMVendRebateApprovalStatus</span></span>|
|<span data-ttu-id="b918c-677">TAMVendRebateCalcDateType</span><span class="sxs-lookup"><span data-stu-id="b918c-677">TAMVendRebateCalcDateType</span></span>|
|<span data-ttu-id="b918c-678">TAMVendRebateTakenFrom</span><span class="sxs-lookup"><span data-stu-id="b918c-678">TAMVendRebateTakenFrom</span></span>|
|<span data-ttu-id="b918c-679">TAMVendRebateTransactionType</span><span class="sxs-lookup"><span data-stu-id="b918c-679">TAMVendRebateTransactionType</span></span>|
|<span data-ttu-id="b918c-680">TaxModuleType</span><span class="sxs-lookup"><span data-stu-id="b918c-680">TaxModuleType</span></span>|
|<span data-ttu-id="b918c-681">TaxSourceType</span><span class="sxs-lookup"><span data-stu-id="b918c-681">TaxSourceType</span></span>|
|<span data-ttu-id="b918c-682">TMSAccessorialAssignmentLevel</span><span class="sxs-lookup"><span data-stu-id="b918c-682">TMSAccessorialAssignmentLevel</span></span>|
|<span data-ttu-id="b918c-683">TMSAccessorialAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="b918c-683">TMSAccessorialAssignmentTarget</span></span>|
|<span data-ttu-id="b918c-684">TMSAccessorialDeliveryType</span><span class="sxs-lookup"><span data-stu-id="b918c-684">TMSAccessorialDeliveryType</span></span>|
|<span data-ttu-id="b918c-685">TMSAccessorialType</span><span class="sxs-lookup"><span data-stu-id="b918c-685">TMSAccessorialType</span></span>|
|<span data-ttu-id="b918c-686">TMSAppointmentAlert</span><span class="sxs-lookup"><span data-stu-id="b918c-686">TMSAppointmentAlert</span></span>|
|<span data-ttu-id="b918c-687">TMSDiscountResultType</span><span class="sxs-lookup"><span data-stu-id="b918c-687">TMSDiscountResultType</span></span>|
|<span data-ttu-id="b918c-688">TMSDiscountType</span><span class="sxs-lookup"><span data-stu-id="b918c-688">TMSDiscountType</span></span>|
|<span data-ttu-id="b918c-689">TMSFeeType</span><span class="sxs-lookup"><span data-stu-id="b918c-689">TMSFeeType</span></span>|
|<span data-ttu-id="b918c-690">TMSFreightBillMatchStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-690">TMSFreightBillMatchStatus</span></span>|
|<span data-ttu-id="b918c-691">TMSFreightBillReconcileType</span><span class="sxs-lookup"><span data-stu-id="b918c-691">TMSFreightBillReconcileType</span></span>|
|<span data-ttu-id="b918c-692">TMSFwkErrorType</span><span class="sxs-lookup"><span data-stu-id="b918c-692">TMSFwkErrorType</span></span>|
|<span data-ttu-id="b918c-693">TMSHubPosition</span><span class="sxs-lookup"><span data-stu-id="b918c-693">TMSHubPosition</span></span>|
|<span data-ttu-id="b918c-694">TMSInvoiceAccountType</span><span class="sxs-lookup"><span data-stu-id="b918c-694">TMSInvoiceAccountType</span></span>|
|<span data-ttu-id="b918c-695">TMSLineType</span><span class="sxs-lookup"><span data-stu-id="b918c-695">TMSLineType</span></span>|
|<span data-ttu-id="b918c-696">TMSLoadBuildSessionState</span><span class="sxs-lookup"><span data-stu-id="b918c-696">TMSLoadBuildSessionState</span></span>|
|<span data-ttu-id="b918c-697">TMSLoadTender</span><span class="sxs-lookup"><span data-stu-id="b918c-697">TMSLoadTender</span></span>|
|<span data-ttu-id="b918c-698">TMSLookupType</span><span class="sxs-lookup"><span data-stu-id="b918c-698">TMSLookupType</span></span>|
|<span data-ttu-id="b918c-699">TMSNumberSequenceType</span><span class="sxs-lookup"><span data-stu-id="b918c-699">TMSNumberSequenceType</span></span>|
|<span data-ttu-id="b918c-700">TMSOverrideLocationType</span><span class="sxs-lookup"><span data-stu-id="b918c-700">TMSOverrideLocationType</span></span>|
|<span data-ttu-id="b918c-701">TMSRecurrenceDays</span><span class="sxs-lookup"><span data-stu-id="b918c-701">TMSRecurrenceDays</span></span>|
|<span data-ttu-id="b918c-702">TMSRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="b918c-702">TMSRecurrenceType</span></span>|
|<span data-ttu-id="b918c-703">TMSRecurrenceWeeks</span><span class="sxs-lookup"><span data-stu-id="b918c-703">TMSRecurrenceWeeks</span></span>|
|<span data-ttu-id="b918c-704">TMSResponsibleForPayment</span><span class="sxs-lookup"><span data-stu-id="b918c-704">TMSResponsibleForPayment</span></span>|
|<span data-ttu-id="b918c-705">TMSRouteStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-705">TMSRouteStatus</span></span>|
|<span data-ttu-id="b918c-706">TMSSalesPurchTransfer</span><span class="sxs-lookup"><span data-stu-id="b918c-706">TMSSalesPurchTransfer</span></span>|
|<span data-ttu-id="b918c-707">TMSTableRef</span><span class="sxs-lookup"><span data-stu-id="b918c-707">TMSTableRef</span></span>|
|<span data-ttu-id="b918c-708">TMSTransportationType</span><span class="sxs-lookup"><span data-stu-id="b918c-708">TMSTransportationType</span></span>|
|<span data-ttu-id="b918c-709">TMSTransportRefType</span><span class="sxs-lookup"><span data-stu-id="b918c-709">TMSTransportRefType</span></span>|
|<span data-ttu-id="b918c-710">TMSTransportTypeFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-710">TMSTransportTypeFilter</span></span>|
|<span data-ttu-id="b918c-711">TMSUOM</span><span class="sxs-lookup"><span data-stu-id="b918c-711">TMSUOM</span></span>|
|<span data-ttu-id="b918c-712">TMSZoneType</span><span class="sxs-lookup"><span data-stu-id="b918c-712">TMSZoneType</span></span>|
|<span data-ttu-id="b918c-713">TradeCurencyConversion</span><span class="sxs-lookup"><span data-stu-id="b918c-713">TradeCurencyConversion</span></span>|
|<span data-ttu-id="b918c-714">TradeLineDlvType</span><span class="sxs-lookup"><span data-stu-id="b918c-714">TradeLineDlvType</span></span>|
|<span data-ttu-id="b918c-715">TradeNonStockedConversionChangeType</span><span class="sxs-lookup"><span data-stu-id="b918c-715">TradeNonStockedConversionChangeType</span></span>|
|<span data-ttu-id="b918c-716">TradeNonStockedConversionIssue</span><span class="sxs-lookup"><span data-stu-id="b918c-716">TradeNonStockedConversionIssue</span></span>|
|<span data-ttu-id="b918c-717">TradeNonStockedConversionResolveUndo</span><span class="sxs-lookup"><span data-stu-id="b918c-717">TradeNonStockedConversionResolveUndo</span></span>|
|<span data-ttu-id="b918c-718">TradePrintType</span><span class="sxs-lookup"><span data-stu-id="b918c-718">TradePrintType</span></span>|
|<span data-ttu-id="b918c-719">TradeTable2LineUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-719">TradeTable2LineUpdate</span></span>|
|<span data-ttu-id="b918c-720">VendNotificationCategorySelection</span><span class="sxs-lookup"><span data-stu-id="b918c-720">VendNotificationCategorySelection</span></span>|
|<span data-ttu-id="b918c-721">VendNotificationStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-721">VendNotificationStatus</span></span>|
|<span data-ttu-id="b918c-722">VendPackingSlipTransTimeStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-722">VendPackingSlipTransTimeStatus</span></span>|
|<span data-ttu-id="b918c-723">VendRequestCompanyType</span><span class="sxs-lookup"><span data-stu-id="b918c-723">VendRequestCompanyType</span></span>|
|<span data-ttu-id="b918c-724">VendRequestOriginatedByType</span><span class="sxs-lookup"><span data-stu-id="b918c-724">VendRequestOriginatedByType</span></span>|
|<span data-ttu-id="b918c-725">VendRequestQuestionnairesCompleted</span><span class="sxs-lookup"><span data-stu-id="b918c-725">VendRequestQuestionnairesCompleted</span></span>|
|<span data-ttu-id="b918c-726">VendRequestRoleType</span><span class="sxs-lookup"><span data-stu-id="b918c-726">VendRequestRoleType</span></span>|
|<span data-ttu-id="b918c-727">VendReviewRatingScore</span><span class="sxs-lookup"><span data-stu-id="b918c-727">VendReviewRatingScore</span></span>|
|<span data-ttu-id="b918c-728">VersioningAction</span><span class="sxs-lookup"><span data-stu-id="b918c-728">VersioningAction</span></span>|
|<span data-ttu-id="b918c-729">WHSAllowMaterialOverPick</span><span class="sxs-lookup"><span data-stu-id="b918c-729">WHSAllowMaterialOverPick</span></span>|
|<span data-ttu-id="b918c-730">WHSApplicableDemand</span><span class="sxs-lookup"><span data-stu-id="b918c-730">WHSApplicableDemand</span></span>|
|<span data-ttu-id="b918c-731">WHSAutoReleaseContainerAtContainerClose</span><span class="sxs-lookup"><span data-stu-id="b918c-731">WHSAutoReleaseContainerAtContainerClose</span></span>|
|<span data-ttu-id="b918c-732">WHSAutoReleaseOrderType</span><span class="sxs-lookup"><span data-stu-id="b918c-732">WHSAutoReleaseOrderType</span></span>|
|<span data-ttu-id="b918c-733">WHSBreakCluster</span><span class="sxs-lookup"><span data-stu-id="b918c-733">WHSBreakCluster</span></span>|
|<span data-ttu-id="b918c-734">WHSContainerizationQueryType</span><span class="sxs-lookup"><span data-stu-id="b918c-734">WHSContainerizationQueryType</span></span>|
|<span data-ttu-id="b918c-735">WHSContainerPackingStrategy</span><span class="sxs-lookup"><span data-stu-id="b918c-735">WHSContainerPackingStrategy</span></span>|
|<span data-ttu-id="b918c-736">WHSContainerTableFormViewType</span><span class="sxs-lookup"><span data-stu-id="b918c-736">WHSContainerTableFormViewType</span></span>|
|<span data-ttu-id="b918c-737">WHSCrossDockFulfillmentStrategy</span><span class="sxs-lookup"><span data-stu-id="b918c-737">WHSCrossDockFulfillmentStrategy</span></span>|
|<span data-ttu-id="b918c-738">WHSCustJourType</span><span class="sxs-lookup"><span data-stu-id="b918c-738">WHSCustJourType</span></span>|
|<span data-ttu-id="b918c-739">WHSCycleCountPlanStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-739">WHSCycleCountPlanStatus</span></span>|
|<span data-ttu-id="b918c-740">WHSDefaultDataField</span><span class="sxs-lookup"><span data-stu-id="b918c-740">WHSDefaultDataField</span></span>|
|<span data-ttu-id="b918c-741">WHSFilterModule</span><span class="sxs-lookup"><span data-stu-id="b918c-741">WHSFilterModule</span></span>|
|<span data-ttu-id="b918c-742">WHSHistoryEvent</span><span class="sxs-lookup"><span data-stu-id="b918c-742">WHSHistoryEvent</span></span>|
|<span data-ttu-id="b918c-743">WHSLoadPlanning</span><span class="sxs-lookup"><span data-stu-id="b918c-743">WHSLoadPlanning</span></span>|
|<span data-ttu-id="b918c-744">WHSLoadPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="b918c-744">WHSLoadPostMethodsBase</span></span>|
|<span data-ttu-id="b918c-745">WhsLoadReplenishment</span><span class="sxs-lookup"><span data-stu-id="b918c-745">WhsLoadReplenishment</span></span>|
|<span data-ttu-id="b918c-746">WHSLoadTable</span><span class="sxs-lookup"><span data-stu-id="b918c-746">WHSLoadTable</span></span>|
|<span data-ttu-id="b918c-747">WHSLocDirStrategy</span><span class="sxs-lookup"><span data-stu-id="b918c-747">WHSLocDirStrategy</span></span>|
|<span data-ttu-id="b918c-748">WHSLPAssignment</span><span class="sxs-lookup"><span data-stu-id="b918c-748">WHSLPAssignment</span></span>|
|<span data-ttu-id="b918c-749">WHSLPWFilterType</span><span class="sxs-lookup"><span data-stu-id="b918c-749">WHSLPWFilterType</span></span>|
|<span data-ttu-id="b918c-750">WHSManifestAt</span><span class="sxs-lookup"><span data-stu-id="b918c-750">WHSManifestAt</span></span>|
|<span data-ttu-id="b918c-751">WHSManifestRequirementContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b918c-751">WHSManifestRequirementContainerGroup</span></span>|
|<span data-ttu-id="b918c-752">WHSMenuItemDirectedBy</span><span class="sxs-lookup"><span data-stu-id="b918c-752">WHSMenuItemDirectedBy</span></span>|
|<span data-ttu-id="b918c-753">WHSMixedLPReceivingMode</span><span class="sxs-lookup"><span data-stu-id="b918c-753">WHSMixedLPReceivingMode</span></span>|
|<span data-ttu-id="b918c-754">WHSMixingLogicTables</span><span class="sxs-lookup"><span data-stu-id="b918c-754">WHSMixingLogicTables</span></span>|
|<span data-ttu-id="b918c-755">WHSMobileAppPagePattern</span><span class="sxs-lookup"><span data-stu-id="b918c-755">WHSMobileAppPagePattern</span></span>|
|<span data-ttu-id="b918c-756">WHSOriginType</span><span class="sxs-lookup"><span data-stu-id="b918c-756">WHSOriginType</span></span>|
|<span data-ttu-id="b918c-757">WHSPickOldestBatch</span><span class="sxs-lookup"><span data-stu-id="b918c-757">WHSPickOldestBatch</span></span>|
|<span data-ttu-id="b918c-758">WHSPostMethodBaseKanban</span><span class="sxs-lookup"><span data-stu-id="b918c-758">WHSPostMethodBaseKanban</span></span>|
|<span data-ttu-id="b918c-759">WHSPostMethodBaseKanbanOptional</span><span class="sxs-lookup"><span data-stu-id="b918c-759">WHSPostMethodBaseKanbanOptional</span></span>|
|<span data-ttu-id="b918c-760">WHSPostMethodBaseOptional</span><span class="sxs-lookup"><span data-stu-id="b918c-760">WHSPostMethodBaseOptional</span></span>|
|<span data-ttu-id="b918c-761">WHSPostMethodBaseProd</span><span class="sxs-lookup"><span data-stu-id="b918c-761">WHSPostMethodBaseProd</span></span>|
|<span data-ttu-id="b918c-762">WHSPostMethodBaseProdOptional</span><span class="sxs-lookup"><span data-stu-id="b918c-762">WHSPostMethodBaseProdOptional</span></span>|
|<span data-ttu-id="b918c-763">WHSPostMethodsBase</span><span class="sxs-lookup"><span data-stu-id="b918c-763">WHSPostMethodsBase</span></span>|
|<span data-ttu-id="b918c-764">WHSQtyPct</span><span class="sxs-lookup"><span data-stu-id="b918c-764">WHSQtyPct</span></span>|
|<span data-ttu-id="b918c-765">WHSReleaseQuantitySpecification</span><span class="sxs-lookup"><span data-stu-id="b918c-765">WHSReleaseQuantitySpecification</span></span>|
|<span data-ttu-id="b918c-766">WHSReplenishmentDependentWorkBlockingPolicy</span><span class="sxs-lookup"><span data-stu-id="b918c-766">WHSReplenishmentDependentWorkBlockingPolicy</span></span>|
|<span data-ttu-id="b918c-767">WHSReservationHierarchyLevelStrategyType</span><span class="sxs-lookup"><span data-stu-id="b918c-767">WHSReservationHierarchyLevelStrategyType</span></span>|
|<span data-ttu-id="b918c-768">WHSReservationStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-768">WHSReservationStatus</span></span>|
|<span data-ttu-id="b918c-769">WHSUseFixedLocations</span><span class="sxs-lookup"><span data-stu-id="b918c-769">WHSUseFixedLocations</span></span>|
|<span data-ttu-id="b918c-770">WHSWorkActivity</span><span class="sxs-lookup"><span data-stu-id="b918c-770">WHSWorkActivity</span></span>|
|<span data-ttu-id="b918c-771">WHSWorkClusterStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-771">WHSWorkClusterStatus</span></span>|
|<span data-ttu-id="b918c-772">WHSWorkCreationProcess</span><span class="sxs-lookup"><span data-stu-id="b918c-772">WHSWorkCreationProcess</span></span>|
|<span data-ttu-id="b918c-773">WHSWorkExceptionLogStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-773">WHSWorkExceptionLogStatus</span></span>|
|<span data-ttu-id="b918c-774">WHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="b918c-774">WHSWorkExecuteMode</span></span>|
|<span data-ttu-id="b918c-775">WHSWorkListPageFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-775">WHSWorkListPageFilter</span></span>|
|<span data-ttu-id="b918c-776">WHSWorkPrintOption</span><span class="sxs-lookup"><span data-stu-id="b918c-776">WHSWorkPrintOption</span></span>|
|<span data-ttu-id="b918c-777">WHSWorkPutFlow</span><span class="sxs-lookup"><span data-stu-id="b918c-777">WHSWorkPutFlow</span></span>|
|<span data-ttu-id="b918c-778">WHSWorkTransType</span><span class="sxs-lookup"><span data-stu-id="b918c-778">WHSWorkTransType</span></span>|
|<span data-ttu-id="b918c-779">WHSWorkType</span><span class="sxs-lookup"><span data-stu-id="b918c-779">WHSWorkType</span></span>|
|<span data-ttu-id="b918c-780">WHSWorkTypePickPut</span><span class="sxs-lookup"><span data-stu-id="b918c-780">WHSWorkTypePickPut</span></span>|
|<span data-ttu-id="b918c-781">WMSAutoAddStop</span><span class="sxs-lookup"><span data-stu-id="b918c-781">WMSAutoAddStop</span></span>|
|<span data-ttu-id="b918c-782">WMSFreightChargeTerms</span><span class="sxs-lookup"><span data-stu-id="b918c-782">WMSFreightChargeTerms</span></span>|
|<span data-ttu-id="b918c-783">WMSFreightCounted</span><span class="sxs-lookup"><span data-stu-id="b918c-783">WMSFreightCounted</span></span>|
|<span data-ttu-id="b918c-784">WMSHandlingType</span><span class="sxs-lookup"><span data-stu-id="b918c-784">WMSHandlingType</span></span>|
|<span data-ttu-id="b918c-785">WMSLocationType</span><span class="sxs-lookup"><span data-stu-id="b918c-785">WMSLocationType</span></span>|
|<span data-ttu-id="b918c-786">WMSPackageType</span><span class="sxs-lookup"><span data-stu-id="b918c-786">WMSPackageType</span></span>|
|<span data-ttu-id="b918c-787">WMSPalletMovementProcessing</span><span class="sxs-lookup"><span data-stu-id="b918c-787">WMSPalletMovementProcessing</span></span>|
|<span data-ttu-id="b918c-788">WMSPhysicalUpdateStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-788">WMSPhysicalUpdateStatus</span></span>|
|<span data-ttu-id="b918c-789">WMSReceiptStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-789">WMSReceiptStatus</span></span>|
|<span data-ttu-id="b918c-790">WMSReservationMethod</span><span class="sxs-lookup"><span data-stu-id="b918c-790">WMSReservationMethod</span></span>|
|<span data-ttu-id="b918c-791">WMSReservationMethodInternal</span><span class="sxs-lookup"><span data-stu-id="b918c-791">WMSReservationMethodInternal</span></span>|
|<span data-ttu-id="b918c-792">WMSShipmentStatus</span><span class="sxs-lookup"><span data-stu-id="b918c-792">WMSShipmentStatus</span></span>|
|<span data-ttu-id="b918c-793">WMSShipmentType</span><span class="sxs-lookup"><span data-stu-id="b918c-793">WMSShipmentType</span></span>|
|<span data-ttu-id="b918c-794">WMSSpaceUtilInconsistencyGroup</span><span class="sxs-lookup"><span data-stu-id="b918c-794">WMSSpaceUtilInconsistencyGroup</span></span>|
|<span data-ttu-id="b918c-795">WMSSpaceUtilShowBy</span><span class="sxs-lookup"><span data-stu-id="b918c-795">WMSSpaceUtilShowBy</span></span>|
|<span data-ttu-id="b918c-796">WMSSpaceUtilStorageLoadUnitType</span><span class="sxs-lookup"><span data-stu-id="b918c-796">WMSSpaceUtilStorageLoadUnitType</span></span>|
|<span data-ttu-id="b918c-797">WMSStoreAreaType</span><span class="sxs-lookup"><span data-stu-id="b918c-797">WMSStoreAreaType</span></span>|
|<span data-ttu-id="b918c-798">WMSTrailerLoaded</span><span class="sxs-lookup"><span data-stu-id="b918c-798">WMSTrailerLoaded</span></span>|
|<span data-ttu-id="b918c-799">WrkCtrActivityType</span><span class="sxs-lookup"><span data-stu-id="b918c-799">WrkCtrActivityType</span></span>|
|<span data-ttu-id="b918c-800">WrkCtrBulkResReqSearchType</span><span class="sxs-lookup"><span data-stu-id="b918c-800">WrkCtrBulkResReqSearchType</span></span>|
|<span data-ttu-id="b918c-801">WrkCtrCapacityType</span><span class="sxs-lookup"><span data-stu-id="b918c-801">WrkCtrCapacityType</span></span>|
|<span data-ttu-id="b918c-802">WrkCtrCapRefType</span><span class="sxs-lookup"><span data-stu-id="b918c-802">WrkCtrCapRefType</span></span>|
|<span data-ttu-id="b918c-803">WrkCtrCommitState</span><span class="sxs-lookup"><span data-stu-id="b918c-803">WrkCtrCommitState</span></span>|
|<span data-ttu-id="b918c-804">WrkCtrGroupWrkCtr</span><span class="sxs-lookup"><span data-stu-id="b918c-804">WrkCtrGroupWrkCtr</span></span>|
|<span data-ttu-id="b918c-805">WrkCtrSchedulerCommand</span><span class="sxs-lookup"><span data-stu-id="b918c-805">WrkCtrSchedulerCommand</span></span>|
|<span data-ttu-id="b918c-806">WrkCtrSchedulerConstraintType</span><span class="sxs-lookup"><span data-stu-id="b918c-806">WrkCtrSchedulerConstraintType</span></span>|
|<span data-ttu-id="b918c-807">WrkCtrSchedulerLoggerMode</span><span class="sxs-lookup"><span data-stu-id="b918c-807">WrkCtrSchedulerLoggerMode</span></span>|
|<span data-ttu-id="b918c-808">WrkCtrType</span><span class="sxs-lookup"><span data-stu-id="b918c-808">WrkCtrType</span></span>|
|<span data-ttu-id="b918c-809">WrkCtrTypeFilter</span><span class="sxs-lookup"><span data-stu-id="b918c-809">WrkCtrTypeFilter</span></span>|

<span data-ttu-id="b918c-810">以下の列挙型は削除され、拡張可能になりませんでした。</span><span class="sxs-lookup"><span data-stu-id="b918c-810">These enumerations were removed, and not made extensible.</span></span>

| <span data-ttu-id="b918c-811">削除された列挙型</span><span class="sxs-lookup"><span data-stu-id="b918c-811">Enumeration removed</span></span> |
| --------------- |
|<span data-ttu-id="b918c-812">BackorderLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="b918c-812">BackorderLinesListPageMode</span></span>|
|<span data-ttu-id="b918c-813">BackorderPurchLinesListPageMode</span><span class="sxs-lookup"><span data-stu-id="b918c-813">BackorderPurchLinesListPageMode</span></span> |
|<span data-ttu-id="b918c-814">EcoResProductPerCompanyListPageType</span><span class="sxs-lookup"><span data-stu-id="b918c-814">EcoResProductPerCompanyListPageType</span></span> |
|<span data-ttu-id="b918c-815">ReturnTableListPageType</span><span class="sxs-lookup"><span data-stu-id="b918c-815">ReturnTableListPageType</span></span> |
|<span data-ttu-id="b918c-816">SMAAgreementTableListPageType</span><span class="sxs-lookup"><span data-stu-id="b918c-816">SMAAgreementTableListPageType</span></span>|

<span data-ttu-id="b918c-817">拡張可能な列挙型のサポートを改善するために、Foundation の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="b918c-817">Foundation changes were made to improve support for extensible enumerations.</span></span> <span data-ttu-id="b918c-818">**IsExtensible** が **はい** に設定されている列挙型については、**SysPlugin** フレームワークが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-818">The **SysPlugin** framework was enabled for enumerations where **IsExtensible** is set to **Yes**.</span></span> <span data-ttu-id="b918c-819">列挙型の新しい名前に基づく構文で、ビューが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-819">Views were enabled with new name-based syntax for enumerations.</span></span>

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a><span data-ttu-id="b918c-820">DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド</span><span class="sxs-lookup"><span data-stu-id="b918c-820">Data manipulation methods that do not raise DataEvents or missing insert, update, delete pre- and post-data events</span></span>

<span data-ttu-id="b918c-821">一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="b918c-821">As a general practice, you use data methods on tables to raise events that can be used for extending the application.</span></span> <span data-ttu-id="b918c-822">コード ベースは、必ずしもこのプラクティスに従っていませんでした。</span><span class="sxs-lookup"><span data-stu-id="b918c-822">The code base has not always followed this practice.</span></span> <span data-ttu-id="b918c-823">たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="b918c-823">For example, the **doInsert**, **doUpdate**, and **doDelete** data methods and certain table implementations did not make a call to **super()** in the data method.</span></span>

<span data-ttu-id="b918c-824">タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="b918c-824">The **insert**, **update**, and **delete** methods on the type classes have been refactored.</span></span> <span data-ttu-id="b918c-825">データ メソッドで **super()** が確実に呼び出されるように変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="b918c-825">Changes were made so that **super()** is called more consistently in data methods.</span></span> <span data-ttu-id="b918c-826">これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-826">These changes enable extensions to be added to these methods, so that pre- and post-events are now available for extension.</span></span> <span data-ttu-id="b918c-827">次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="b918c-827">The tables where the **insert**, **update**, and **delete** events were enabled for extension are listed in the following table.</span></span>

| <span data-ttu-id="b918c-828">テーブル</span><span class="sxs-lookup"><span data-stu-id="b918c-828">Table</span></span> |
| -------------|
| <span data-ttu-id="b918c-829">InventBlocking</span><span class="sxs-lookup"><span data-stu-id="b918c-829">InventBlocking</span></span>|
| <span data-ttu-id="b918c-830">InventTransferLine</span><span class="sxs-lookup"><span data-stu-id="b918c-830">InventTransferLine</span></span>|
| <span data-ttu-id="b918c-831">Kanban</span><span class="sxs-lookup"><span data-stu-id="b918c-831">Kanban</span></span>|
| <span data-ttu-id="b918c-832">KanbanJob</span><span class="sxs-lookup"><span data-stu-id="b918c-832">KanbanJob</span></span>|
| <span data-ttu-id="b918c-833">KanbanJobPickingList</span><span class="sxs-lookup"><span data-stu-id="b918c-833">KanbanJobPickingList</span></span>|
| <span data-ttu-id="b918c-834">MCRRoyaltyVendTable</span><span class="sxs-lookup"><span data-stu-id="b918c-834">MCRRoyaltyVendTable</span></span>|
| <span data-ttu-id="b918c-835">PdsRebateTable</span><span class="sxs-lookup"><span data-stu-id="b918c-835">PdsRebateTable</span></span>|
| <span data-ttu-id="b918c-836">PmfProdCoBy</span><span class="sxs-lookup"><span data-stu-id="b918c-836">PmfProdCoBy</span></span>|
| <span data-ttu-id="b918c-837">ProdBOM</span><span class="sxs-lookup"><span data-stu-id="b918c-837">ProdBOM</span></span>|
| <span data-ttu-id="b918c-838">ProdRoute</span><span class="sxs-lookup"><span data-stu-id="b918c-838">ProdRoute</span></span>|
| <span data-ttu-id="b918c-839">ProdTable</span><span class="sxs-lookup"><span data-stu-id="b918c-839">ProdTable</span></span>|
| <span data-ttu-id="b918c-840">PurchLine</span><span class="sxs-lookup"><span data-stu-id="b918c-840">PurchLine</span></span>|
| <span data-ttu-id="b918c-841">PurchRFQCaseLine</span><span class="sxs-lookup"><span data-stu-id="b918c-841">PurchRFQCaseLine</span></span>|
| <span data-ttu-id="b918c-842">PurchRFQCaseTable</span><span class="sxs-lookup"><span data-stu-id="b918c-842">PurchRFQCaseTable</span></span>|
| <span data-ttu-id="b918c-843">PurchRFQLine</span><span class="sxs-lookup"><span data-stu-id="b918c-843">PurchRFQLine</span></span>|
| <span data-ttu-id="b918c-844">PurchTable</span><span class="sxs-lookup"><span data-stu-id="b918c-844">PurchTable</span></span>|
| <span data-ttu-id="b918c-845">SalesLine</span><span class="sxs-lookup"><span data-stu-id="b918c-845">SalesLine</span></span>|
| <span data-ttu-id="b918c-846">SalesQuotationLine</span><span class="sxs-lookup"><span data-stu-id="b918c-846">SalesQuotationLine</span></span>|
| <span data-ttu-id="b918c-847">SalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="b918c-847">SalesQuotationTable</span></span>|
| <span data-ttu-id="b918c-848">SalesTable</span><span class="sxs-lookup"><span data-stu-id="b918c-848">SalesTable</span></span>|
| <span data-ttu-id="b918c-849">TAMVendRebateTable</span><span class="sxs-lookup"><span data-stu-id="b918c-849">TAMVendRebateTable</span></span>|
| <span data-ttu-id="b918c-850">WMSOrder</span><span class="sxs-lookup"><span data-stu-id="b918c-850">WMSOrder</span></span>|
| <span data-ttu-id="b918c-851">WMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="b918c-851">WMSOrderTrans</span></span>|

## <a name="exposing-class-members"></a><span data-ttu-id="b918c-852">クラス メンバーの公開</span><span class="sxs-lookup"><span data-stu-id="b918c-852">Exposing class members</span></span>

<span data-ttu-id="b918c-853">アクセス修飾子または新しい parm メソッドの変更の結果、追加のプライベート メンバーをカスタマイズに使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-853">Additional private members are now available for customization as a result of the changes to the access modifier or new parm methods.</span></span> <span data-ttu-id="b918c-854">コマンド チェーン プラットフォーム機能により、保護されたメソッドとメンバーへの拡張クラスのアクセスが有効になります。</span><span class="sxs-lookup"><span data-stu-id="b918c-854">The chain of command platform feature enables extension class access to protected methods and members.</span></span> <span data-ttu-id="b918c-855">コマンド チェーンの詳細については、「[拡張可能な X++: コマンド チェーン](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b918c-855">For more information about chain of command, see [Extensible X++: Chain of Command](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/).</span></span>

| <span data-ttu-id="b918c-856">メンバー</span><span class="sxs-lookup"><span data-stu-id="b918c-856">Member</span></span> |
| -------------|
|<span data-ttu-id="b918c-857">AssetPost.ledgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="b918c-857">AssetPost.ledgerJournalTrans</span></span>|
|<span data-ttu-id="b918c-858">クラス DimensionDerivationRule.ledgerDimensionAllocationList</span><span class="sxs-lookup"><span data-stu-id="b918c-858">Class DimensionDerivationRule.ledgerDimensionAllocationList</span></span>|
|<span data-ttu-id="b918c-859">クラス PurchInvoiceJournalCreate.purchTable</span><span class="sxs-lookup"><span data-stu-id="b918c-859">Class PurchInvoiceJournalCreate.purchTable</span></span>|
|<span data-ttu-id="b918c-860">クラス PurchTableType.purchTable</span><span class="sxs-lookup"><span data-stu-id="b918c-860">Class PurchTableType.purchTable</span></span>|
|<span data-ttu-id="b918c-861">クラス SalesInvoiceJournalPost.salesLine</span><span class="sxs-lookup"><span data-stu-id="b918c-861">Class SalesInvoiceJournalPost.salesLine</span></span>|
|<span data-ttu-id="b918c-862">クラス SalesQuotationLineType</span><span class="sxs-lookup"><span data-stu-id="b918c-862">Class SalesQuotationLineType</span></span>|
|<span data-ttu-id="b918c-863">クラス SalesQuotationTableType</span><span class="sxs-lookup"><span data-stu-id="b918c-863">Class SalesQuotationTableType</span></span>|
|<span data-ttu-id="b918c-864">クラス VendorInvoiceLineSourceDocLineItem.purchLine</span><span class="sxs-lookup"><span data-stu-id="b918c-864">Class VendorInvoiceLineSourceDocLineItem.purchLine</span></span>|
|<span data-ttu-id="b918c-865">CustCreditLimit.balanceTotalsCalculated</span><span class="sxs-lookup"><span data-stu-id="b918c-865">CustCreditLimit.balanceTotalsCalculated</span></span>|
|<span data-ttu-id="b918c-866">CustCreditLimit_SalesTable.salesTable</span><span class="sxs-lookup"><span data-stu-id="b918c-866">CustCreditLimit_SalesTable.salesTable</span></span>|
|<span data-ttu-id="b918c-867">フォーム LedgerJournalTransCustPaym.ledgerJournalEngine</span><span class="sxs-lookup"><span data-stu-id="b918c-867">Form LedgerJournalTransCustPaym.ledgerJournalEngine</span></span>|
|<span data-ttu-id="b918c-868">PurchLineType.purchLine</span><span class="sxs-lookup"><span data-stu-id="b918c-868">PurchLineType.purchLine</span></span>|
|<span data-ttu-id="b918c-869">PurchLineType.purchLine_orig</span><span class="sxs-lookup"><span data-stu-id="b918c-869">PurchLineType.purchLine_orig</span></span>|
|<span data-ttu-id="b918c-870">SalesLineType.salesLine</span><span class="sxs-lookup"><span data-stu-id="b918c-870">SalesLineType.salesLine</span></span>|
|<span data-ttu-id="b918c-871">SalesLineType.salesLine_orig</span><span class="sxs-lookup"><span data-stu-id="b918c-871">SalesLineType.salesLine_orig</span></span>|
|<span data-ttu-id="b918c-872">SalesTableType.checkSalesQty</span><span class="sxs-lookup"><span data-stu-id="b918c-872">SalesTableType.checkSalesQty</span></span>|
|<span data-ttu-id="b918c-873">SalesTableType.SalesTable_orig</span><span class="sxs-lookup"><span data-stu-id="b918c-873">SalesTableType.SalesTable_orig</span></span>|
|<span data-ttu-id="b918c-874">WHSControl.data</span><span class="sxs-lookup"><span data-stu-id="b918c-874">WHSControl.data</span></span>|
|<span data-ttu-id="b918c-875">WHSLocationDirective.targetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="b918c-875">WHSLocationDirective.targetLicensePlateId</span></span>|

## <a name="construct-methods-with-throw-statements"></a><span data-ttu-id="b918c-876">throw ステートメントを使用した construct メソッド</span><span class="sxs-lookup"><span data-stu-id="b918c-876">Construct methods with throw statements</span></span>

<span data-ttu-id="b918c-877">特定の型の実装が欠落していた場合、いくつかの **construct** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="b918c-877">Some **construct** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="b918c-878">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**construct** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="b918c-878">This doesn't work well with extensibility, so to mitigate this, **construct** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="b918c-879">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-879">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="b918c-880">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b918c-880">Object</span></span> |
| -------------|
|<span data-ttu-id="b918c-881">BarcodeEAN128.string()</span><span class="sxs-lookup"><span data-stu-id="b918c-881">BarcodeEAN128.string()</span></span>|
|<span data-ttu-id="b918c-882">CustCreditLimit.Construct</span><span class="sxs-lookup"><span data-stu-id="b918c-882">CustCreditLimit.Construct</span></span>|
|<span data-ttu-id="b918c-883">FormLetterReport</span><span class="sxs-lookup"><span data-stu-id="b918c-883">FormLetterReport</span></span>|
|<span data-ttu-id="b918c-884">JournalStatic</span><span class="sxs-lookup"><span data-stu-id="b918c-884">JournalStatic</span></span>|
|<span data-ttu-id="b918c-885">MarkupAllocation</span><span class="sxs-lookup"><span data-stu-id="b918c-885">MarkupAllocation</span></span>|
|<span data-ttu-id="b918c-886">PurchTable2LineField</span><span class="sxs-lookup"><span data-stu-id="b918c-886">PurchTable2LineField</span></span>|
|<span data-ttu-id="b918c-887">SalesCalcTax</span><span class="sxs-lookup"><span data-stu-id="b918c-887">SalesCalcTax</span></span>|
|<span data-ttu-id="b918c-888">SalesEditLinesForm</span><span class="sxs-lookup"><span data-stu-id="b918c-888">SalesEditLinesForm</span></span>|
|<span data-ttu-id="b918c-889">SalesFormLetter</span><span class="sxs-lookup"><span data-stu-id="b918c-889">SalesFormLetter</span></span>|
|<span data-ttu-id="b918c-890">SalesFormLetterContract.newFromPackedVersion</span><span class="sxs-lookup"><span data-stu-id="b918c-890">SalesFormLetterContract.newFromPackedVersion</span></span>|
|<span data-ttu-id="b918c-891">SalesFormletterParmData.newData</span><span class="sxs-lookup"><span data-stu-id="b918c-891">SalesFormletterParmData.newData</span></span>|
|<span data-ttu-id="b918c-892">SalesQuantity</span><span class="sxs-lookup"><span data-stu-id="b918c-892">SalesQuantity</span></span>|
|<span data-ttu-id="b918c-893">SalesQuotationEditLinesForm.construct</span><span class="sxs-lookup"><span data-stu-id="b918c-893">SalesQuotationEditLinesForm.construct</span></span>|
|<span data-ttu-id="b918c-894">SalesSummaryFields</span><span class="sxs-lookup"><span data-stu-id="b918c-894">SalesSummaryFields</span></span>|
|<span data-ttu-id="b918c-895">SalesTable2LineField</span><span class="sxs-lookup"><span data-stu-id="b918c-895">SalesTable2LineField</span></span>|
|<span data-ttu-id="b918c-896">VendInvoiceTableToLineUpdate</span><span class="sxs-lookup"><span data-stu-id="b918c-896">VendInvoiceTableToLineUpdate</span></span>|

## <a name="find-methods-with-throw-statements"></a><span data-ttu-id="b918c-897">throw ステートメントを使用した find メソッド</span><span class="sxs-lookup"><span data-stu-id="b918c-897">Find methods with throw statements</span></span>

<span data-ttu-id="b918c-898">特定の型の実装が欠落していた場合、いくつかの **find** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="b918c-898">Some **find** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="b918c-899">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**find** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="b918c-899">This does not work well with extensibility, so to mitigate this, **find** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="b918c-900">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-900">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="b918c-901">メソッド</span><span class="sxs-lookup"><span data-stu-id="b918c-901">Methods</span></span> |
| -------------|
|<span data-ttu-id="b918c-902">JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="b918c-902">JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="b918c-903">JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="b918c-903">JournalStatic.findJournalTableId</span></span>|

## <a name="methods-made-hookable"></a><span data-ttu-id="b918c-904">フック可能なメソッド</span><span class="sxs-lookup"><span data-stu-id="b918c-904">Methods made hookable</span></span>

<span data-ttu-id="b918c-905">パブリックでない一部のメソッドおよびフック可能でない一部のメソッドについて、拡張性サポートが強化されました。</span><span class="sxs-lookup"><span data-stu-id="b918c-905">Extensibility support has been extended for some methods that were not public and were not hookable.</span></span> <span data-ttu-id="b918c-906">以下のメソッドはフック可能な動作で明示的に修飾されています。</span><span class="sxs-lookup"><span data-stu-id="b918c-906">The following methods have been explicitly decorated with hookable behavior.</span></span>

| <span data-ttu-id="b918c-907">メソッド</span><span class="sxs-lookup"><span data-stu-id="b918c-907">Method</span></span> |
| -------------|
|<span data-ttu-id="b918c-908">クラス CustVendReversePosting.updateCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="b918c-908">Class CustVendReversePosting.updateCustVendTrans</span></span>|
|<span data-ttu-id="b918c-909">クラス JournalTableData.construct</span><span class="sxs-lookup"><span data-stu-id="b918c-909">Class JournalTableData.construct</span></span>|
|<span data-ttu-id="b918c-910">クラス PriceDisc.makeKey</span><span class="sxs-lookup"><span data-stu-id="b918c-910">Class PriceDisc.makeKey</span></span>|
|<span data-ttu-id="b918c-911">クラス PurchInvoiceJournalCreate.initJournalHeader</span><span class="sxs-lookup"><span data-stu-id="b918c-911">Class PurchInvoiceJournalCreate.initJournalHeader</span></span>|
|<span data-ttu-id="b918c-912">クラス SalesInvoiceJournalPost.checkSourceLine</span><span class="sxs-lookup"><span data-stu-id="b918c-912">Class SalesInvoiceJournalPost.checkSourceLine</span></span>|
|<span data-ttu-id="b918c-913">クラス SalesInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="b918c-913">Class SalesInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="b918c-914">フォーム LedgerTransVoucher.addDynaLink</span><span class="sxs-lookup"><span data-stu-id="b918c-914">Form LedgerTransVoucher.addDynaLink</span></span>|
|<span data-ttu-id="b918c-915">ReqCalc.deleteItemRequirement</span><span class="sxs-lookup"><span data-stu-id="b918c-915">ReqCalc.deleteItemRequirement</span></span>|
|<span data-ttu-id="b918c-916">ReqCalc.initTransFromInventTrans</span><span class="sxs-lookup"><span data-stu-id="b918c-916">ReqCalc.initTransFromInventTrans</span></span>|
|<span data-ttu-id="b918c-917">ReqCalcForecastItemTable.deleteRequirement</span><span class="sxs-lookup"><span data-stu-id="b918c-917">ReqCalcForecastItemTable.deleteRequirement</span></span>|
|<span data-ttu-id="b918c-918">テーブル TmpCustVendTrans.createLineCreditLimit</span><span class="sxs-lookup"><span data-stu-id="b918c-918">Table TmpCustVendTrans.createLineCreditLimit</span></span>|
|<span data-ttu-id="b918c-919">テーブル TmpCustVendTrans.createLineCreditRemain</span><span class="sxs-lookup"><span data-stu-id="b918c-919">Table TmpCustVendTrans.createLineCreditRemain</span></span>|
|<span data-ttu-id="b918c-920">テーブル TmpCustVendTrans.createLineOrdered</span><span class="sxs-lookup"><span data-stu-id="b918c-920">Table TmpCustVendTrans.createLineOrdered</span></span>|
|<span data-ttu-id="b918c-921">テーブル TmpCustVendTrans.createLinePackingSlip</span><span class="sxs-lookup"><span data-stu-id="b918c-921">Table TmpCustVendTrans.createLinePackingSlip</span></span>|
|<span data-ttu-id="b918c-922">WHSLocationDirective.addRangeByTransType</span><span class="sxs-lookup"><span data-stu-id="b918c-922">WHSLocationDirective.addRangeByTransType</span></span>|
|<span data-ttu-id="b918c-923">WhsWorkCreate.createWorkLine</span><span class="sxs-lookup"><span data-stu-id="b918c-923">WhsWorkCreate.createWorkLine</span></span>|

## <a name="inline-delegates"></a><span data-ttu-id="b918c-924">インライン デリゲート</span><span class="sxs-lookup"><span data-stu-id="b918c-924">Inline delegates</span></span>

<span data-ttu-id="b918c-925">インライン デリゲートを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b918c-925">Inline delegates are now available.</span></span> <span data-ttu-id="b918c-926">インライン デリゲートの最も一般的な使用方法は、メソッドをより粒度の細かいメソッドに分割して、より小規模なメソッドで拡張イベントを使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="b918c-926">The most common way to use inline delegates is to split the method into more granular methods and enable extensibility events in the smaller methods.</span></span>

|  <span data-ttu-id="b918c-927">メソッド</span><span class="sxs-lookup"><span data-stu-id="b918c-927">Method</span></span> |
| -------------|
|<span data-ttu-id="b918c-928">AxClass - ChequeDP - Method - insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="b918c-928">AxClass - ChequeDP - Method - insertChequeTmp</span></span>|
|<span data-ttu-id="b918c-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="b918c-929">AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice</span></span>|
|<span data-ttu-id="b918c-930">クラス JournalStatic.findJournalTableFromTrans</span><span class="sxs-lookup"><span data-stu-id="b918c-930">class JournalStatic.findJournalTableFromTrans</span></span>|
|<span data-ttu-id="b918c-931">クラス JournalStatic.findJournalTableId</span><span class="sxs-lookup"><span data-stu-id="b918c-931">class JournalStatic.findJournalTableId</span></span>|
|<span data-ttu-id="b918c-932">クラス WhsLocationDirective.findLocationMultiSKU</span><span class="sxs-lookup"><span data-stu-id="b918c-932">Class WhsLocationDirective.findLocationMultiSKU</span></span>|
|<span data-ttu-id="b918c-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span><span class="sxs-lookup"><span data-stu-id="b918c-933">EcoResReleasedProductVariantEntity.insertEntityDataSource</span></span>|
|<span data-ttu-id="b918c-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span><span class="sxs-lookup"><span data-stu-id="b918c-934">ForecastSales.ForecastSales_ds.updateForecastSalesFields</span></span>|
|<span data-ttu-id="b918c-935">フォーム SalesTable - メソッド updateDesign</span><span class="sxs-lookup"><span data-stu-id="b918c-935">Form SalesTable - method updateDesign</span></span>|
|<span data-ttu-id="b918c-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span><span class="sxs-lookup"><span data-stu-id="b918c-936">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span></span>|
|<span data-ttu-id="b918c-937">SalesLineType.insert</span><span class="sxs-lookup"><span data-stu-id="b918c-937">SalesLineType.insert</span></span>|
|<span data-ttu-id="b918c-938">SalesLineType.update</span><span class="sxs-lookup"><span data-stu-id="b918c-938">SalesLineType.update</span></span>|
|<span data-ttu-id="b918c-939">SalesTable2LineUpdatePrompt.dialog</span><span class="sxs-lookup"><span data-stu-id="b918c-939">SalesTable2LineUpdatePrompt.dialog</span></span>|
|<span data-ttu-id="b918c-940">テーブル ExtCodeTable</span><span class="sxs-lookup"><span data-stu-id="b918c-940">table ExtCodeTable</span></span>|
|<span data-ttu-id="b918c-941">テーブル InventItemGroup.getGroupForAccountType</span><span class="sxs-lookup"><span data-stu-id="b918c-941">table InventItemGroup.getGroupForAccountType</span></span>|
|<span data-ttu-id="b918c-942">テーブル InventItemGroup.ledgerDimensionDescription</span><span class="sxs-lookup"><span data-stu-id="b918c-942">table InventItemGroup.ledgerDimensionDescription</span></span>|
|<span data-ttu-id="b918c-943">テーブル InventTestAssociationTable</span><span class="sxs-lookup"><span data-stu-id="b918c-943">table InventTestAssociationTable</span></span>|
|<span data-ttu-id="b918c-944">テーブル LedgerJournalName - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="b918c-944">Table LedgerJournalName - method validateWrite</span></span>|
|<span data-ttu-id="b918c-945">テーブル PaymTerm - メソッド due</span><span class="sxs-lookup"><span data-stu-id="b918c-945">Table PaymTerm - method due</span></span>|
|<span data-ttu-id="b918c-946">TaxCalculation.newForSourceType</span><span class="sxs-lookup"><span data-stu-id="b918c-946">TaxCalculation.newForSourceType</span></span>|
|<span data-ttu-id="b918c-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span><span class="sxs-lookup"><span data-stu-id="b918c-947">TaxCalculation.newForSourceTypeWithTaxUncommitted</span></span>|
|<span data-ttu-id="b918c-948">WHSLoadLine.getOrderCommonFromLoadLine</span><span class="sxs-lookup"><span data-stu-id="b918c-948">WHSLoadLine.getOrderCommonFromLoadLine</span></span>|
|<span data-ttu-id="b918c-949">WhsLocationDirective.findLocation</span><span class="sxs-lookup"><span data-stu-id="b918c-949">WhsLocationDirective.findLocation</span></span>|
|<span data-ttu-id="b918c-950">WHSRFControlData.populateData</span><span class="sxs-lookup"><span data-stu-id="b918c-950">WHSRFControlData.populateData</span></span>|
|<span data-ttu-id="b918c-951">WHSRFControLData.processControl</span><span class="sxs-lookup"><span data-stu-id="b918c-951">WHSRFControLData.processControl</span></span>|
|<span data-ttu-id="b918c-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="b918c-952">WHSRFMenuItemTable.getWHSWorkExecuteMode</span></span>|

## <a name="other-changes"></a><span data-ttu-id="b918c-953">その他の変更</span><span class="sxs-lookup"><span data-stu-id="b918c-953">Other changes</span></span>

<span data-ttu-id="b918c-954">次の表に、拡張機能に対して行われた追加の変更を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b918c-954">The following table lists additional changes that have been made for extensibility.</span></span>


|                                                           <span data-ttu-id="b918c-955">変更</span><span class="sxs-lookup"><span data-stu-id="b918c-955">Change</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------------------|
|                                      <span data-ttu-id="b918c-956">既存の製品分析コードの間接参照の追加</span><span class="sxs-lookup"><span data-stu-id="b918c-956">Add indirection for existing product dimensions</span></span>                                       |
|                                  <span data-ttu-id="b918c-957">クラス FormLetterParmDataOutputContract は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="b918c-957">Class FormLetterParmDataOutputContract is not extensible</span></span>                                  |
|             <span data-ttu-id="b918c-958">1 つ以上の引数をサポートする SysExtensionFramework のインスタンス化戦略の作成</span><span class="sxs-lookup"><span data-stu-id="b918c-958">Create an instantiation strategy for the SysExtensionFramework that supports one or more arguments</span></span>             |
|                      <span data-ttu-id="b918c-959">カスタマイズ: TableField: 拡張モデル: テーブル フィールドの EDT タイプの変更</span><span class="sxs-lookup"><span data-stu-id="b918c-959">Customization: TableField: Extension Model: Change EDT type of on a table field</span></span>                       |
|                          <span data-ttu-id="b918c-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="b918c-960">CustVendOpenTransBalances - initAccountNumCurrencies() switch statement</span></span>                           |
|                                     <span data-ttu-id="b918c-961">CustVendOpenTransBalances - new() switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="b918c-961">CustVendOpenTransBalances - new() switch statement</span></span>                                     |
|                                  <span data-ttu-id="b918c-962">CustVendOutPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="b918c-962">CustVendOutPaym (Class) needs extensibility improvement</span></span>                                   |
|                        <span data-ttu-id="b918c-963">CustVendPaymReconciliationSetStatus (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="b918c-963">CustVendPaymReconciliationSetStatus (Class) needs extensibility improvement</span></span>                         |
|                                 <span data-ttu-id="b918c-964">CustVendSumForPaym (クラス) には拡張性の改善が必要</span><span class="sxs-lookup"><span data-stu-id="b918c-964">CustVendSumForPaym (Class) needs extensibility improvement</span></span>                                 |
|                               <span data-ttu-id="b918c-965">SysGroup からの AddressCountyId と AddressStateId EDT の切り離し</span><span class="sxs-lookup"><span data-stu-id="b918c-965">Decouple AddressCountyId and AddressStateId EDTs from SysGroup</span></span>                               |
|                          <span data-ttu-id="b918c-966">ドキュメント管理イベントの処理には拡張性サポートの改善が必要</span><span class="sxs-lookup"><span data-stu-id="b918c-966">Document Management event handling needs improved extensibility support</span></span>                           |
|            <span data-ttu-id="b918c-967">為替レート プロバイダー フレームワークには、通貨モデルにカスタムの組み込みプロバイダーを配置することが必要</span><span class="sxs-lookup"><span data-stu-id="b918c-967">Exchange rate provider framework requires custom built providers to be placed in the Currency Model</span></span>             |
|                                                      <span data-ttu-id="b918c-968">GS-128 の拡張</span><span class="sxs-lookup"><span data-stu-id="b918c-968">Extending GS-128</span></span>                                                      |
|                         <span data-ttu-id="b918c-969">拡張モデル: CountryRegionCodes プロパティでのカスタマイズを許可する。</span><span class="sxs-lookup"><span data-stu-id="b918c-969">Extension model: Allow customizations on the CountryRegionCodes property.</span></span>                          |
|                  <span data-ttu-id="b918c-970">フォーム拡張機能 - 新しいコントロールによって "拡張された" フォーム要素の拡張機能は動作しません</span><span class="sxs-lookup"><span data-stu-id="b918c-970">Form extension - Extension of "extended" form elements with new controls are not working</span></span>                  |
|                                              <span data-ttu-id="b918c-971">InventDim: throw 付きの条件</span><span class="sxs-lookup"><span data-stu-id="b918c-971">InventDim: Condition with throw</span></span>                                               |
|                                                  <span data-ttu-id="b918c-972">InventDimRenameDimValue</span><span class="sxs-lookup"><span data-stu-id="b918c-972">InventDimRenameDimValue</span></span>                                                   |
|                <span data-ttu-id="b918c-973">メソッドのオーバーレイ - クラス VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="b918c-973">Method overlayering - Class VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span></span>                |
|                                     <span data-ttu-id="b918c-974">メソッドのオーバーレイ: クラス Markup - メソッド delete</span><span class="sxs-lookup"><span data-stu-id="b918c-974">Method overlayering: class Markup - method delete</span></span>                                      |
|                       <span data-ttu-id="b918c-975">メソッドのオーバーレイ: クラス McrPriceHistoryForm.insertPotentialTradeAgreements</span><span class="sxs-lookup"><span data-stu-id="b918c-975">Method overlayering: class McrPriceHistoryForm.insertPotentialTradeAgreements</span></span>                        |
|                             <span data-ttu-id="b918c-976">メソッドのオーバーレイ: クラス OffsetVoucher - メソッド markTransaction</span><span class="sxs-lookup"><span data-stu-id="b918c-976">Method overlayering: Class OffsetVoucher - method markTransaction</span></span>                              |
|                                 <span data-ttu-id="b918c-977">メソッドのオーバーレイ: フォーム LedgerJournalTransDimension.init</span><span class="sxs-lookup"><span data-stu-id="b918c-977">Method overlayering: Form LedgerJournalTransDimension.init</span></span>                                 |
|                                 <span data-ttu-id="b918c-978">メソッドのオーバーレイ: フォーム LedgerTransVoucher - メソッド init</span><span class="sxs-lookup"><span data-stu-id="b918c-978">Method overlayering: Form LedgerTransVoucher - method init</span></span>                                 |
|                             <span data-ttu-id="b918c-979">メソッドのオーバーレイ: テーブル CustInvoiceTable - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="b918c-979">Method overlayering: Table CustInvoiceTable - method validateWrite</span></span>                             |
|                       <span data-ttu-id="b918c-980">メソッド シグネチャが変更されました: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span><span class="sxs-lookup"><span data-stu-id="b918c-980">Method signature changed: RetailCreateLinesFromProductsToAdd.parmCallerCommon</span></span>                        |
|                               <span data-ttu-id="b918c-981">メソッド シグネチャが変更になりました: WHSInvent.getCommonFromWorkTransType</span><span class="sxs-lookup"><span data-stu-id="b918c-981">Method signature changed: WHSInvent.getCommonFromWorkTransType</span></span>                               |
|                                  <span data-ttu-id="b918c-982">メソッド シグネチャが変更されました: WHSPoolProdBom.movementBuffer</span><span class="sxs-lookup"><span data-stu-id="b918c-982">Method signature changed: WHSPoolProdBom.movementBuffer</span></span>                                   |
|                          <span data-ttu-id="b918c-983">construct メソッドがありません: クラス SMAServiceOrderTableButtonStateProvider</span><span class="sxs-lookup"><span data-stu-id="b918c-983">Missing construct method: class SMAServiceOrderTableButtonStateProvider</span></span>                           |
|                                         <span data-ttu-id="b918c-984">必要な番号順序スコープの拡張性</span><span class="sxs-lookup"><span data-stu-id="b918c-984">Number sequence scope extensibility needed</span></span>                                         |
|                           <span data-ttu-id="b918c-985">Runbase には、クラスの拡張機能がメンバーをパック/アンパックする方法が必要</span><span class="sxs-lookup"><span data-stu-id="b918c-985">Runbase needs a way for class extensions to pack/unpack their members</span></span>                            |
|                                              <span data-ttu-id="b918c-986">文字列 EDT のサイズの拡張の問題</span><span class="sxs-lookup"><span data-stu-id="b918c-986">String EDT size extension issues</span></span>                                              |
|                              <span data-ttu-id="b918c-987">カスタムの InventDim に基づく手持在庫フォームのオープンのサポート</span><span class="sxs-lookup"><span data-stu-id="b918c-987">Support opening Inventory on-hand form based on custom InventDim</span></span>                              |
|          <span data-ttu-id="b918c-988">SysExtension フレームワーク: SysExtensionIInstantiationStrategy と SysExtensionIAttribute は互換性がありません</span><span class="sxs-lookup"><span data-stu-id="b918c-988">SysExtension framework: SysExtensionIInstantiationStrategy and SysExtensionIAttribute are not compatible</span></span>          |
| <span data-ttu-id="b918c-989">要求/応答シナリオで使用されるデリゲートがより堅牢になるために、EventHandlerResult のバリエーションが必要</span><span class="sxs-lookup"><span data-stu-id="b918c-989">Variations of EventHandlerResult are requested to ensure that delegates used in Request/response scenarios are more robust</span></span> |
|                                                <span data-ttu-id="b918c-990">WHS モバイル フレームワーク: 合格</span><span class="sxs-lookup"><span data-stu-id="b918c-990">WHS Mobile Framework: passes</span></span>                                                |
|                                     <span data-ttu-id="b918c-991">WhsLocationDirectiveLine To/FromQty は拡張可能ではありません</span><span class="sxs-lookup"><span data-stu-id="b918c-991">WhsLocationDirectiveLine To/FromQty not extensible</span></span>                                     |
|                                                 <span data-ttu-id="b918c-992">WHSMobileApp の拡張性</span><span class="sxs-lookup"><span data-stu-id="b918c-992">WHSMobileApp Extensibility</span></span>                                                 |
|         <span data-ttu-id="b918c-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="b918c-993">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|         <span data-ttu-id="b918c-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません</span><span class="sxs-lookup"><span data-stu-id="b918c-994">WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() is not generic enough about Product dimensions</span></span>          |
|            <span data-ttu-id="b918c-995">WhsRFControlData.processControl は switch ブロック内の _data ではなく WhsControl.data を参照する必要があります</span><span class="sxs-lookup"><span data-stu-id="b918c-995">WhsRFControlData.processControl must reference WhsControl.data instead of _data in the switch block</span></span>             |

