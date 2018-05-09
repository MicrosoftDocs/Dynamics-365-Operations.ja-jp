---
title: "Dynamics 365 for Finance and Operations バージョン 8.0 の拡張機能の変更"
description: "これは、Dynamics 365 for Finance and Operations バージョン 8.0 に実装された拡張機能の一覧です。"
author: FrankDahl
manager: AnnBe
ms.date: 04/13/2018
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
ms.search.validFrom: 2018-04-04
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 47a4a2e60ef2bcc0d2edf065d63c34cddc0a1325
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-80"></a><span data-ttu-id="e2cf7-103">Dynamics 365 for Finance and Operations バージョン 8.0 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="e2cf7-103">Extensibility changes in Dynamics 365 for Finance and Operations version 8.0</span></span>

[!include[banner](../includes/banner.md)]

## <a name="hard-sealed-application-models"></a><span data-ttu-id="e2cf7-104">ハード シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="e2cf7-104">Hard-sealed application models</span></span>

<span data-ttu-id="e2cf7-105">Dynamics 365 for Finance and Operations バージョン 8.0 では、Microsoft のアプリケーション モデルはすべてハード シールされています。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-105">In Dynamics 365 for Finance and Operations version 8.0, all of Microsoft's application models have been hard-sealed.</span></span> <span data-ttu-id="e2cf7-106">これらのモデルのオーバーレイ コードは、現在コンパイル エラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-106">Overlayered code in these models will now produce compilation errors.</span></span> <span data-ttu-id="e2cf7-107">カスタマイズ モデルは拡張機能によってのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-107">The only supported customization model is through extensions.</span></span> <span data-ttu-id="e2cf7-108">拡張機能によってこれらのモデルをカスタマイズできない場合は、標準のアプリケーションを変更して拡張機能を有効にするよう、Microsoft に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-108">If you cannot customize these models through extension, then you will have to make a request to Microsoft to enable extensibility by changing the standard application.</span></span>

<span data-ttu-id="e2cf7-109">次の表に、今回のリリースで現在ハード シールされているモデルの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-109">The following table includes a list of models that are now hard-sealed with this release.</span></span>

| <span data-ttu-id="e2cf7-110">モジュール</span><span class="sxs-lookup"><span data-stu-id="e2cf7-110">Module</span></span> | <span data-ttu-id="e2cf7-111">モデル</span><span class="sxs-lookup"><span data-stu-id="e2cf7-111">Model</span></span>         |
| --------------- |-------------|
|<span data-ttu-id="e2cf7-112">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="e2cf7-112">ApplicationCommon</span></span> | <span data-ttu-id="e2cf7-113">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="e2cf7-113">ApplicationCommon</span></span> |
|<span data-ttu-id="e2cf7-114">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-114">ApplicationSuite</span></span> | <span data-ttu-id="e2cf7-115">Electronic Reporting Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="e2cf7-115">Electronic Reporting Application Suite Integration</span></span> |
|<span data-ttu-id="e2cf7-116">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-116">ApplicationSuite</span></span> | <span data-ttu-id="e2cf7-117">Foundation Upgrade</span><span class="sxs-lookup"><span data-stu-id="e2cf7-117">Foundation Upgrade</span></span> |
|<span data-ttu-id="e2cf7-118">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-118">ApplicationSuite</span></span> | <span data-ttu-id="e2cf7-119">Foundation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-119">Foundation</span></span> |
|<span data-ttu-id="e2cf7-120">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-120">ApplicationSuite</span></span> | <span data-ttu-id="e2cf7-121">SCMControls</span><span class="sxs-lookup"><span data-stu-id="e2cf7-121">SCMControls</span></span> |
|<span data-ttu-id="e2cf7-122">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-122">ApplicationSuite</span></span> | <span data-ttu-id="e2cf7-123">Tax Books Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="e2cf7-123">Tax Books Application Suite Integration</span></span> |
|<span data-ttu-id="e2cf7-124">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-124">ApplicationSuite</span></span> | <span data-ttu-id="e2cf7-125">Tax Engine Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="e2cf7-125">Tax Engine Application Suite Integration</span></span> |
|<span data-ttu-id="e2cf7-126">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-126">CaseManagement</span></span> | <span data-ttu-id="e2cf7-127">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-127">CaseManagement</span></span> |
|<span data-ttu-id="e2cf7-128">Currency</span><span class="sxs-lookup"><span data-stu-id="e2cf7-128">Currency</span></span> | <span data-ttu-id="e2cf7-129">Currency</span><span class="sxs-lookup"><span data-stu-id="e2cf7-129">Currency</span></span> |
|<span data-ttu-id="e2cf7-130">DataImpExpApplication</span><span class="sxs-lookup"><span data-stu-id="e2cf7-130">DataImpExpApplication</span></span> | <span data-ttu-id="e2cf7-131">DataImpExpApplication</span><span class="sxs-lookup"><span data-stu-id="e2cf7-131">DataImpExpApplication</span></span> |
|<span data-ttu-id="e2cf7-132">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="e2cf7-132">DataUpgrade</span></span> | <span data-ttu-id="e2cf7-133">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="e2cf7-133">DataUpgrade</span></span> |
|<span data-ttu-id="e2cf7-134">Directory</span><span class="sxs-lookup"><span data-stu-id="e2cf7-134">Directory</span></span> | <span data-ttu-id="e2cf7-135">Directory</span><span class="sxs-lookup"><span data-stu-id="e2cf7-135">Directory</span></span> |
|<span data-ttu-id="e2cf7-136">Directory</span><span class="sxs-lookup"><span data-stu-id="e2cf7-136">Directory</span></span> | <span data-ttu-id="e2cf7-137">SecurityReports</span><span class="sxs-lookup"><span data-stu-id="e2cf7-137">SecurityReports</span></span> |
|<span data-ttu-id="e2cf7-138">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="e2cf7-138">GeneralLedger</span></span> | <span data-ttu-id="e2cf7-139">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="e2cf7-139">GeneralLedger</span></span> |
|<span data-ttu-id="e2cf7-140">Ledger</span><span class="sxs-lookup"><span data-stu-id="e2cf7-140">Ledger</span></span> | <span data-ttu-id="e2cf7-141">Ledger</span><span class="sxs-lookup"><span data-stu-id="e2cf7-141">Ledger</span></span> |
|<span data-ttu-id="e2cf7-142">PersonnelManagement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-142">PersonnelManagement</span></span> | <span data-ttu-id="e2cf7-143">PersonnelManagement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-143">PersonnelManagement</span></span> |
|<span data-ttu-id="e2cf7-144">ProcessGuide</span><span class="sxs-lookup"><span data-stu-id="e2cf7-144">ProcessGuide</span></span> | <span data-ttu-id="e2cf7-145">ProcessGuide</span><span class="sxs-lookup"><span data-stu-id="e2cf7-145">ProcessGuide</span></span> |
|<span data-ttu-id="e2cf7-146">Retail</span><span class="sxs-lookup"><span data-stu-id="e2cf7-146">Retail</span></span> | <span data-ttu-id="e2cf7-147">Retail</span><span class="sxs-lookup"><span data-stu-id="e2cf7-147">Retail</span></span> |
|<span data-ttu-id="e2cf7-148">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-148">SourceDocumentation</span></span> | <span data-ttu-id="e2cf7-149">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-149">SourceDocumentation</span></span> |
|<span data-ttu-id="e2cf7-150">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="e2cf7-150">SourceDocumentationTypes</span></span> | <span data-ttu-id="e2cf7-151">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="e2cf7-151">SourceDocumentationTypes</span></span> |
|<span data-ttu-id="e2cf7-152">Subledger</span><span class="sxs-lookup"><span data-stu-id="e2cf7-152">Subledger</span></span> | <span data-ttu-id="e2cf7-153">Subledger</span><span class="sxs-lookup"><span data-stu-id="e2cf7-153">Subledger</span></span> |
|<span data-ttu-id="e2cf7-154">Tax</span><span class="sxs-lookup"><span data-stu-id="e2cf7-154">Tax</span></span> | <span data-ttu-id="e2cf7-155">Tax</span><span class="sxs-lookup"><span data-stu-id="e2cf7-155">Tax</span></span> |

## <a name="enumerations-that-have-been-made-extensible"></a><span data-ttu-id="e2cf7-156">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="e2cf7-156">Enumerations that have been made extensible</span></span>

<span data-ttu-id="e2cf7-157">列挙の拡張をサポートするために以下の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-157">The following changes were made to support extending enumerations:</span></span>
- <span data-ttu-id="e2cf7-158">標準アプリケーションの多くの列挙が拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-158">Many enumerations in the standard application have been made extensible.</span></span> <span data-ttu-id="e2cf7-159">列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-159">An enumeration is made extensible by setting two properties on the enumeration.</span></span> <span data-ttu-id="e2cf7-160">**IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-160">The **IsExtensible** property is set to **Yes**, and the **UseEnumValue** property is set to **No**.</span></span> 
- <span data-ttu-id="e2cf7-161">一部の列挙型は状態を表します。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-161">Some enumerations represent state.</span></span> <span data-ttu-id="e2cf7-162">拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-162">New façade methods have been added to help enable adding enumeration values by extension.</span></span> <span data-ttu-id="e2cf7-163">列挙型を拡張する方法については、「[列挙値の追加](add-enum-value.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-163">For information about how to extend an enumeration, see [Add an enum value](add-enum-value.md).</span></span>
- <span data-ttu-id="e2cf7-164">拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-164">Some application code that uses enumerations was changed to support extensibility.</span></span> <span data-ttu-id="e2cf7-165">一般的な変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-165">Common changes include:</span></span>
    + <span data-ttu-id="e2cf7-166">ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-166">Removing **throw** exception statements in the default case of a switch to allow post-event subscription.</span></span>
    + <span data-ttu-id="e2cf7-167">拡張機能の **SysExtension** サポートの追加。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-167">Adding **SysExtension** support for extension.</span></span>
    + <span data-ttu-id="e2cf7-168">明示的なデリゲートの追加。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-168">Adding explicit delegates.</span></span>

| <span data-ttu-id="e2cf7-169">列挙型</span><span class="sxs-lookup"><span data-stu-id="e2cf7-169">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="e2cf7-170">BOMConsumpType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-170">BOMConsumpType</span></span>|
|<span data-ttu-id="e2cf7-171">BOMFormula</span><span class="sxs-lookup"><span data-stu-id="e2cf7-171">BOMFormula</span></span>|
|<span data-ttu-id="e2cf7-172">BOMType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-172">BOMType</span></span>|
|<span data-ttu-id="e2cf7-173">ChequeFormType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-173">ChequeFormType</span></span>|
|<span data-ttu-id="e2cf7-174">CostGroupType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-174">CostGroupType</span></span>|
|<span data-ttu-id="e2cf7-175">CustAccountStatement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-175">CustAccountStatement</span></span>|
|<span data-ttu-id="e2cf7-176">CustMandateScheme</span><span class="sxs-lookup"><span data-stu-id="e2cf7-176">CustMandateScheme</span></span>|
|<span data-ttu-id="e2cf7-177">CustVendDisputeStatus</span><span class="sxs-lookup"><span data-stu-id="e2cf7-177">CustVendDisputeStatus</span></span>|
|<span data-ttu-id="e2cf7-178">DispositionAction</span><span class="sxs-lookup"><span data-stu-id="e2cf7-178">DispositionAction</span></span>|
|<span data-ttu-id="e2cf7-179">ItemCalcType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-179">ItemCalcType</span></span>|
|<span data-ttu-id="e2cf7-180">KMCollectionAnswerStatus</span><span class="sxs-lookup"><span data-stu-id="e2cf7-180">KMCollectionAnswerStatus</span></span>|
|<span data-ttu-id="e2cf7-181">KanbanEventType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-181">KanbanEventType</span></span>|
|<span data-ttu-id="e2cf7-182">LedgerAccrualPeriod</span><span class="sxs-lookup"><span data-stu-id="e2cf7-182">LedgerAccrualPeriod</span></span>|
|<span data-ttu-id="e2cf7-183">LogisticsAddressElement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-183">LogisticsAddressElement</span></span>|
|<span data-ttu-id="e2cf7-184">LogisticsLocationEntityType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-184">LogisticsLocationEntityType</span></span>|
|<span data-ttu-id="e2cf7-185">NoneBeginTransEnd</span><span class="sxs-lookup"><span data-stu-id="e2cf7-185">NoneBeginTransEnd</span></span>|
|<span data-ttu-id="e2cf7-186">PSAInvoiceFormats</span><span class="sxs-lookup"><span data-stu-id="e2cf7-186">PSAInvoiceFormats</span></span>|
|<span data-ttu-id="e2cf7-187">PdsCumulationPeriod</span><span class="sxs-lookup"><span data-stu-id="e2cf7-187">PdsCumulationPeriod</span></span>|
|<span data-ttu-id="e2cf7-188">PdsRebateProgramType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-188">PdsRebateProgramType</span></span>|
|<span data-ttu-id="e2cf7-189">PdsRebateTransaction</span><span class="sxs-lookup"><span data-stu-id="e2cf7-189">PdsRebateTransaction</span></span>|
|<span data-ttu-id="e2cf7-190">PdsUnitType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-190">PdsUnitType</span></span>|
|<span data-ttu-id="e2cf7-191">PriceDiscSystemSource</span><span class="sxs-lookup"><span data-stu-id="e2cf7-191">PriceDiscSystemSource</span></span>|
|<span data-ttu-id="e2cf7-192">ProdFlushingPrincipBOM</span><span class="sxs-lookup"><span data-stu-id="e2cf7-192">ProdFlushingPrincipBOM</span></span>|
|<span data-ttu-id="e2cf7-193">ProdFlushingPrincipItem</span><span class="sxs-lookup"><span data-stu-id="e2cf7-193">ProdFlushingPrincipItem</span></span>|
|<span data-ttu-id="e2cf7-194">ProdReservation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-194">ProdReservation</span></span>|
|<span data-ttu-id="e2cf7-195">ProjAccountTypeCost</span><span class="sxs-lookup"><span data-stu-id="e2cf7-195">ProjAccountTypeCost</span></span>|
|<span data-ttu-id="e2cf7-196">ProjAccountTypeSales</span><span class="sxs-lookup"><span data-stu-id="e2cf7-196">ProjAccountTypeSales</span></span>|
|<span data-ttu-id="e2cf7-197">ProjAccountType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-197">ProjAccountType</span></span>|
|<span data-ttu-id="e2cf7-198">ProjJournalType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-198">ProjJournalType</span></span>|
|<span data-ttu-id="e2cf7-199">RevenueContributionMargin</span><span class="sxs-lookup"><span data-stu-id="e2cf7-199">RevenueContributionMargin</span></span>|
|<span data-ttu-id="e2cf7-200">SMATransactionType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-200">SMATransactionType</span></span>|
|<span data-ttu-id="e2cf7-201">SysPolicyRuleEnum</span><span class="sxs-lookup"><span data-stu-id="e2cf7-201">SysPolicyRuleEnum</span></span>|
|<span data-ttu-id="e2cf7-202">SysPolicyRuleTypeEnum</span><span class="sxs-lookup"><span data-stu-id="e2cf7-202">SysPolicyRuleTypeEnum</span></span>|
|<span data-ttu-id="e2cf7-203">SysPolicyTypeEnum</span><span class="sxs-lookup"><span data-stu-id="e2cf7-203">SysPolicyTypeEnum</span></span>|
|<span data-ttu-id="e2cf7-204">TAMRebateAmtType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-204">TAMRebateAmtType</span></span>|
|<span data-ttu-id="e2cf7-205">TAMVendRebateStatus</span><span class="sxs-lookup"><span data-stu-id="e2cf7-205">TAMVendRebateStatus</span></span>|
|<span data-ttu-id="e2cf7-206">TMSRecordType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-206">TMSRecordType</span></span>|
|<span data-ttu-id="e2cf7-207">Voided</span><span class="sxs-lookup"><span data-stu-id="e2cf7-207">Voided</span></span>|
|<span data-ttu-id="e2cf7-208">WMSJointShippingType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-208">WMSJointShippingType</span></span>|
|<span data-ttu-id="e2cf7-209">WMSReferenceType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-209">WMSReferenceType</span></span>|

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a><span data-ttu-id="e2cf7-210">DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド</span><span class="sxs-lookup"><span data-stu-id="e2cf7-210">Data manipulation methods that do not raise DataEvents or missing insert, update, delete pre- and post-data events</span></span>

<span data-ttu-id="e2cf7-211">一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-211">As a general practice, you use data methods on tables to raise events that can be used for extending the application.</span></span> <span data-ttu-id="e2cf7-212">コード ベースは、必ずしもこのプラクティスに従っていませんでした。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-212">The code base has not always followed this practice.</span></span> <span data-ttu-id="e2cf7-213">たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-213">For example, the **doInsert**, **doUpdate**, and **doDelete** data methods and certain table implementations did not make a call to **super()** in the data method.</span></span>

<span data-ttu-id="e2cf7-214">タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-214">The **insert**, **update**, and **delete** methods on the type classes have been refactored.</span></span> <span data-ttu-id="e2cf7-215">データ メソッドで **super()** が確実に呼び出されるように変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-215">Changes were made so that **super()** is called more consistently in data methods.</span></span> <span data-ttu-id="e2cf7-216">これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-216">These changes enable extensions to be added to these methods, so that pre- and post-events are now available for extension.</span></span> <span data-ttu-id="e2cf7-217">次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-217">The tables where the **insert**, **update**, and **delete** events were enabled for extension are listed in the following table.</span></span>

| <span data-ttu-id="e2cf7-218">タイプ、名前、データ ソース、およびメソッド</span><span class="sxs-lookup"><span data-stu-id="e2cf7-218">Type, name, data source, and method</span></span> |
| ----------------------|
|<span data-ttu-id="e2cf7-219">フォーム ProjTableCreate.ProjTable.write</span><span class="sxs-lookup"><span data-stu-id="e2cf7-219">Form ProjTableCreate.ProjTable.write</span></span>|
|<span data-ttu-id="e2cf7-220">フォーム ReturnTable.ReturnTable.leaveRecord</span><span class="sxs-lookup"><span data-stu-id="e2cf7-220">Form ReturnTable.ReturnTable.leaveRecord</span></span>|
|<span data-ttu-id="e2cf7-221">フォーム SalesQuotationProjTable.SalesQuotationTable.leaveRecord</span><span class="sxs-lookup"><span data-stu-id="e2cf7-221">Form SalesQuotationProjTable.SalesQuotationTable.leaveRecord</span></span>|
|<span data-ttu-id="e2cf7-222">フォーム SalesQuotationTable.SalesQuotationTable.leaveRecord</span><span class="sxs-lookup"><span data-stu-id="e2cf7-222">Form SalesQuotationTable.SalesQuotationTable.leaveRecord</span></span>|
|<span data-ttu-id="e2cf7-223">フォーム SalesTable.SalesTable.leaveRecord</span><span class="sxs-lookup"><span data-stu-id="e2cf7-223">Form SalesTable.SalesTable.leaveRecord</span></span>|

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="e2cf7-224">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="e2cf7-224">Refactored methods to support extensibility</span></span>

<span data-ttu-id="e2cf7-225">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-225">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="e2cf7-226">タイプ、名前、およびメソッド</span><span class="sxs-lookup"><span data-stu-id="e2cf7-226">Type, name, and method</span></span> |
| ----------------------|
|<span data-ttu-id="e2cf7-227">クラス AgreementConfirm_Sales.startConfirm</span><span class="sxs-lookup"><span data-stu-id="e2cf7-227">Class AgreementConfirm_Sales.startConfirm</span></span>|
|<span data-ttu-id="e2cf7-228">クラス AssetChangeGroup.updateAssetGroupInfo</span><span class="sxs-lookup"><span data-stu-id="e2cf7-228">Class AssetChangeGroup.updateAssetGroupInfo</span></span>|
|<span data-ttu-id="e2cf7-229">クラス AssetPost.createAssetTransForPost</span><span class="sxs-lookup"><span data-stu-id="e2cf7-229">Class AssetPost.createAssetTransForPost</span></span>|
|<span data-ttu-id="e2cf7-230">クラス AssetSplit.getUpdatedSplitValueModel</span><span class="sxs-lookup"><span data-stu-id="e2cf7-230">Class AssetSplit.getUpdatedSplitValueModel</span></span>|
|<span data-ttu-id="e2cf7-231">クラス AssetTableMethod.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-231">Class AssetTableMethod.init</span></span>|
|<span data-ttu-id="e2cf7-232">クラス AssetTableMethod_SL.calc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-232">Class AssetTableMethod_SL.calc</span></span>|
|<span data-ttu-id="e2cf7-233">クラス AxSalesLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-233">Class AxSalesLine</span></span>|
|<span data-ttu-id="e2cf7-234">クラス BankPaymCancel.serverRun</span><span class="sxs-lookup"><span data-stu-id="e2cf7-234">Class BankPaymCancel.serverRun</span></span>|
|<span data-ttu-id="e2cf7-235">クラス BomSearch.New</span><span class="sxs-lookup"><span data-stu-id="e2cf7-235">Class BomSearch.New</span></span>|
|<span data-ttu-id="e2cf7-236">クラス BomSearch_BOMCopyType.New</span><span class="sxs-lookup"><span data-stu-id="e2cf7-236">Class BomSearch_BOMCopyType.New</span></span>|
|<span data-ttu-id="e2cf7-237">クラス Commission.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-237">Class Commission.run</span></span>|
|<span data-ttu-id="e2cf7-238">クラス CostSheetPanel.build</span><span class="sxs-lookup"><span data-stu-id="e2cf7-238">Class CostSheetPanel.build</span></span>|
|<span data-ttu-id="e2cf7-239">クラス CreateInvoiceJournalPost.createFixedAsset</span><span class="sxs-lookup"><span data-stu-id="e2cf7-239">Class CreateInvoiceJournalPost.createFixedAsset</span></span>|
|<span data-ttu-id="e2cf7-240">クラス CustAccountStatementIntDP.printingAmountMST</span><span class="sxs-lookup"><span data-stu-id="e2cf7-240">Class CustAccountStatementIntDP.printingAmountMST</span></span>|
|<span data-ttu-id="e2cf7-241">クラス CustCreditLimit.balanceEstimate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-241">Class CustCreditLimit.balanceEstimate</span></span>|
|<span data-ttu-id="e2cf7-242">クラス CustCreditLimit.calculateBalance</span><span class="sxs-lookup"><span data-stu-id="e2cf7-242">Class CustCreditLimit.calculateBalance</span></span>|
|<span data-ttu-id="e2cf7-243">クラス CustCreditLimit_SalesTable.New</span><span class="sxs-lookup"><span data-stu-id="e2cf7-243">Class CustCreditLimit_SalesTable.New</span></span>|
|<span data-ttu-id="e2cf7-244">クラス CustInterestCreate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-244">Class CustInterestCreate</span></span>|
|<span data-ttu-id="e2cf7-245">クラス CustVoucher.post</span><span class="sxs-lookup"><span data-stu-id="e2cf7-245">Class CustVoucher.post</span></span>|
|<span data-ttu-id="e2cf7-246">クラス DimensionDerivationRule.buildDimensionCombination</span><span class="sxs-lookup"><span data-stu-id="e2cf7-246">Class DimensionDerivationRule.buildDimensionCombination</span></span>|
|<span data-ttu-id="e2cf7-247">クラス EcoResProductInformation.main</span><span class="sxs-lookup"><span data-stu-id="e2cf7-247">Class EcoResProductInformation.main</span></span>|
|<span data-ttu-id="e2cf7-248">クラス EcoResProductReleaseManager.setAndSaveRetailProductProperties</span><span class="sxs-lookup"><span data-stu-id="e2cf7-248">Class EcoResProductReleaseManager.setAndSaveRetailProductProperties</span></span>|
|<span data-ttu-id="e2cf7-249">クラス EcoResProductValidator.isEssentialFieldValuesSet</span><span class="sxs-lookup"><span data-stu-id="e2cf7-249">Class EcoResProductValidator.isEssentialFieldValuesSet</span></span>|
|<span data-ttu-id="e2cf7-250">クラス FormLetterServiceController.newFromContract</span><span class="sxs-lookup"><span data-stu-id="e2cf7-250">Class FormLetterServiceController.newFromContract</span></span>|
|<span data-ttu-id="e2cf7-251">クラス FormletterJournalPost.postLineDiscount</span><span class="sxs-lookup"><span data-stu-id="e2cf7-251">Class FormletterJournalPost.postLineDiscount</span></span>|
|<span data-ttu-id="e2cf7-252">クラス Graphics_WrkCtrCapBooking.insertLoad</span><span class="sxs-lookup"><span data-stu-id="e2cf7-252">Class Graphics_WrkCtrCapBooking.insertLoad</span></span>|
|<span data-ttu-id="e2cf7-253">クラス Graphics_WrkCtrCapBooking.loadGroupReservations</span><span class="sxs-lookup"><span data-stu-id="e2cf7-253">Class Graphics_WrkCtrCapBooking.loadGroupReservations</span></span>|
|<span data-ttu-id="e2cf7-254">クラス Graphics_WrkCtrCapBooking.loadNumReservations</span><span class="sxs-lookup"><span data-stu-id="e2cf7-254">Class Graphics_WrkCtrCapBooking.loadNumReservations</span></span>|
|<span data-ttu-id="e2cf7-255">クラス InterCompanyPostPurch.construct</span><span class="sxs-lookup"><span data-stu-id="e2cf7-255">Class InterCompanyPostPurch.construct</span></span>|
|<span data-ttu-id="e2cf7-256">クラス InterCompanySyncPurchLineType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-256">Class InterCompanySyncPurchLineType</span></span>|
|<span data-ttu-id="e2cf7-257">クラス InterCompanySyncPurchTableType.setSalesTableData</span><span class="sxs-lookup"><span data-stu-id="e2cf7-257">Class InterCompanySyncPurchTableType.setSalesTableData</span></span>|
|<span data-ttu-id="e2cf7-258">クラス InterCompanySyncPurchTableType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-258">Class InterCompanySyncPurchTableType</span></span>|
|<span data-ttu-id="e2cf7-259">クラス InventAgeDimDP.createOrMergeInventAgeDimTmp</span><span class="sxs-lookup"><span data-stu-id="e2cf7-259">Class InventAgeDimDP.createOrMergeInventAgeDimTmp</span></span>|
|<span data-ttu-id="e2cf7-260">クラス InventAgeDimDP.insertOrMergeInventAgeDimTmp</span><span class="sxs-lookup"><span data-stu-id="e2cf7-260">Class InventAgeDimDP.insertOrMergeInventAgeDimTmp</span></span>|
|<span data-ttu-id="e2cf7-261">クラス InventAgingCmdAggregateSelected.execute</span><span class="sxs-lookup"><span data-stu-id="e2cf7-261">Class InventAgingCmdAggregateSelected.execute</span></span>|
|<span data-ttu-id="e2cf7-262">クラス InventCostItemDim.initInventSettlement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-262">Class InventCostItemDim.initInventSettlement</span></span>|
|<span data-ttu-id="e2cf7-263">クラス InventCostReport.newInventCostReport_CostBaseType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-263">Class InventCostReport.newInventCostReport_CostBaseType</span></span>|
|<span data-ttu-id="e2cf7-264">クラス InventCountCreateItems.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-264">Class InventCountCreateItems.run</span></span>|
|<span data-ttu-id="e2cf7-265">クラス InventDimCtrl_Frm.clearInvisibleRanges</span><span class="sxs-lookup"><span data-stu-id="e2cf7-265">Class InventDimCtrl_Frm.clearInvisibleRanges</span></span>|
|<span data-ttu-id="e2cf7-266">クラス InventItemPriceActivationTaskActivateSim.activateOneInventItemPriceSim</span><span class="sxs-lookup"><span data-stu-id="e2cf7-266">Class InventItemPriceActivationTaskActivateSim.activateOneInventItemPriceSim</span></span>|
|<span data-ttu-id="e2cf7-267">クラス InventItemPriceSim.moveSimulatedToCurrent</span><span class="sxs-lookup"><span data-stu-id="e2cf7-267">Class InventItemPriceSim.moveSimulatedToCurrent</span></span>|
|<span data-ttu-id="e2cf7-268">クラス InventLedgerPostingDefinitionEntityHelper.inventAccountTypeX2InventAccountType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-268">Class InventLedgerPostingDefinitionEntityHelper.inventAccountTypeX2InventAccountType</span></span>|
|<span data-ttu-id="e2cf7-269">クラス InventMov_SalesQuotation.isQuotationQtyEditable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-269">Class InventMov_SalesQuotation.isQuotationQtyEditable</span></span>|
|<span data-ttu-id="e2cf7-270">クラス InventProductDimensionLookup.dimEDT2FieldId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-270">Class InventProductDimensionLookup.dimEDT2FieldId</span></span>|
|<span data-ttu-id="e2cf7-271">クラス InventProductDimension</span><span class="sxs-lookup"><span data-stu-id="e2cf7-271">Class InventProductDimension</span></span>|
|<span data-ttu-id="e2cf7-272">クラス InventQualityManagementBlock.actOnAssociations</span><span class="sxs-lookup"><span data-stu-id="e2cf7-272">Class InventQualityManagementBlock.actOnAssociations</span></span>|
|<span data-ttu-id="e2cf7-273">クラス InventQualityManagementCreate.createOnRegistration</span><span class="sxs-lookup"><span data-stu-id="e2cf7-273">Class InventQualityManagementCreate.createOnRegistration</span></span>|
|<span data-ttu-id="e2cf7-274">クラス InventQualityManagementCreate.createQualityOrder</span><span class="sxs-lookup"><span data-stu-id="e2cf7-274">Class InventQualityManagementCreate.createQualityOrder</span></span>|
|<span data-ttu-id="e2cf7-275">クラス InventQualityManagementCreate.generateQualityOrders</span><span class="sxs-lookup"><span data-stu-id="e2cf7-275">Class InventQualityManagementCreate.generateQualityOrders</span></span>|
|<span data-ttu-id="e2cf7-276">クラス InventQualityManagementCreateInvent.generateQualityOrdersWithDiscrimination</span><span class="sxs-lookup"><span data-stu-id="e2cf7-276">Class InventQualityManagementCreateInvent.generateQualityOrdersWithDiscrimination</span></span>|
|<span data-ttu-id="e2cf7-277">クラス InventQualityMgmtCreateNonInvent.generateQualityOrdersWithDiscrimination</span><span class="sxs-lookup"><span data-stu-id="e2cf7-277">Class InventQualityMgmtCreateNonInvent.generateQualityOrdersWithDiscrimination</span></span>|
|<span data-ttu-id="e2cf7-278">クラス InventQualityOrderReopen.main</span><span class="sxs-lookup"><span data-stu-id="e2cf7-278">Class InventQualityOrderReopen.main</span></span>|
|<span data-ttu-id="e2cf7-279">クラス InventQualityOrderReopen.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-279">Class InventQualityOrderReopen.run</span></span>|
|<span data-ttu-id="e2cf7-280">クラス InventQualityOrderValidate.main</span><span class="sxs-lookup"><span data-stu-id="e2cf7-280">Class InventQualityOrderValidate.main</span></span>|
|<span data-ttu-id="e2cf7-281">クラス InventQualityOrderValidate.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-281">Class InventQualityOrderValidate.run</span></span>|
|<span data-ttu-id="e2cf7-282">クラス InventQualityReferenceTypeSales.isEligibleForQualityManagement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-282">Class InventQualityReferenceTypeSales.isEligibleForQualityManagement</span></span>|
|<span data-ttu-id="e2cf7-283">クラス InventQualityReferenceTypeSales.supportsInventoryBlocking</span><span class="sxs-lookup"><span data-stu-id="e2cf7-283">Class InventQualityReferenceTypeSales.supportsInventoryBlocking</span></span>|
|<span data-ttu-id="e2cf7-284">クラス InventQualitymanagementCreate.createPerQualityAssociations</span><span class="sxs-lookup"><span data-stu-id="e2cf7-284">Class InventQualitymanagementCreate.createPerQualityAssociations</span></span>|
|<span data-ttu-id="e2cf7-285">クラス InventSumReCalcItem.updateActualInventSum</span><span class="sxs-lookup"><span data-stu-id="e2cf7-285">Class InventSumReCalcItem.updateActualInventSum</span></span>|
|<span data-ttu-id="e2cf7-286">クラス InventTestAssociationTable.checkAccountRelation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-286">Class InventTestAssociationTable.checkAccountRelation</span></span>|
|<span data-ttu-id="e2cf7-287">クラス InventTestAssociationTable.initRecord</span><span class="sxs-lookup"><span data-stu-id="e2cf7-287">Class InventTestAssociationTable.initRecord</span></span>|
|<span data-ttu-id="e2cf7-288">クラス InventTrackingDimTracingCriteria.initFromArgs</span><span class="sxs-lookup"><span data-stu-id="e2cf7-288">Class InventTrackingDimTracingCriteria.initFromArgs</span></span>|
|<span data-ttu-id="e2cf7-289">クラス InventTransLine.insert</span><span class="sxs-lookup"><span data-stu-id="e2cf7-289">Class InventTransLine.insert</span></span>|
|<span data-ttu-id="e2cf7-290">クラス InventTransferMulti.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-290">Class InventTransferMulti.run</span></span>|
|<span data-ttu-id="e2cf7-291">クラス InventTransferMultiReceive::main</span><span class="sxs-lookup"><span data-stu-id="e2cf7-291">Class InventTransferMultiReceive::main</span></span>|
|<span data-ttu-id="e2cf7-292">クラス InventTransferMultiShip.buildParmFromWMSShipment</span><span class="sxs-lookup"><span data-stu-id="e2cf7-292">Class InventTransferMultiShip.buildParmFromWMSShipment</span></span>|
|<span data-ttu-id="e2cf7-293">クラス InventTransferMultiShip.runUpdate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-293">Class InventTransferMultiShip.runUpdate</span></span>|
|<span data-ttu-id="e2cf7-294">クラス InventTransferOrderOverviewDP.insertTmpTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-294">Class InventTransferOrderOverviewDP.insertTmpTable</span></span>|
|<span data-ttu-id="e2cf7-295">クラス InventTransferUpdShip.updateInventTransferLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-295">Class InventTransferUpdShip.updateInventTransferLine</span></span>|
|<span data-ttu-id="e2cf7-296">クラス InventUpd_Physical.updatePhysicalIssue</span><span class="sxs-lookup"><span data-stu-id="e2cf7-296">Class InventUpd_Physical.updatePhysicalIssue</span></span>|
|<span data-ttu-id="e2cf7-297">クラス InventUpd_Physical.updatePhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="e2cf7-297">Class InventUpd_Physical.updatePhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="e2cf7-298">クラス InventUpd_Picked.updatePickInventTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-298">Class InventUpd_Picked.updatePickInventTrans</span></span>|
|<span data-ttu-id="e2cf7-299">クラス InventUpd_Reservation.whsUpdateReserveMore</span><span class="sxs-lookup"><span data-stu-id="e2cf7-299">Class InventUpd_Reservation.whsUpdateReserveMore</span></span>|
|<span data-ttu-id="e2cf7-300">クラス InventUpdate.raiseOnHandChangingOnPhysicalStatusUpd</span><span class="sxs-lookup"><span data-stu-id="e2cf7-300">Class InventUpdate.raiseOnHandChangingOnPhysicalStatusUpd</span></span>|
|<span data-ttu-id="e2cf7-301">クラス InventUpdate.updateDimReservePhysical</span><span class="sxs-lookup"><span data-stu-id="e2cf7-301">Class InventUpdate.updateDimReservePhysical</span></span>|
|<span data-ttu-id="e2cf7-302">クラス InventUpdate.updateTransDimTransferReceipt</span><span class="sxs-lookup"><span data-stu-id="e2cf7-302">Class InventUpdate.updateTransDimTransferReceipt</span></span>|
|<span data-ttu-id="e2cf7-303">クラス InventUpdate.writeInventTransAutoDim</span><span class="sxs-lookup"><span data-stu-id="e2cf7-303">Class InventUpdate.writeInventTransAutoDim</span></span>|
|<span data-ttu-id="e2cf7-304">クラス InventValueReportDP.processInventValueReportTmpLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-304">Class InventValueReportDP.processInventValueReportTmpLine</span></span>|
|<span data-ttu-id="e2cf7-305">クラス InventoryMainAccDimensionListProvider.populateMainAccountDimensionList</span><span class="sxs-lookup"><span data-stu-id="e2cf7-305">Class InventoryMainAccDimensionListProvider.populateMainAccountDimensionList</span></span>|
|<span data-ttu-id="e2cf7-306">クラス LedgerBalanceQueryGeneralJournal.addToBalanceTotals</span><span class="sxs-lookup"><span data-stu-id="e2cf7-306">Class LedgerBalanceQueryGeneralJournal.addToBalanceTotals</span></span>|
|<span data-ttu-id="e2cf7-307">クラス LedgerBalanceQueryGeneralJournal.createQuery</span><span class="sxs-lookup"><span data-stu-id="e2cf7-307">Class LedgerBalanceQueryGeneralJournal.createQuery</span></span>|
|<span data-ttu-id="e2cf7-308">クラス LedgerJournalCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="e2cf7-308">Class LedgerJournalCheckPost.checkJournal</span></span>|
|<span data-ttu-id="e2cf7-309">クラス LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="e2cf7-309">Class LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="e2cf7-310">クラス LedgerJournalDP.insertJournalTransForLedgerJournalTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-310">Class LedgerJournalDP.insertJournalTransForLedgerJournalTable</span></span>|
|<span data-ttu-id="e2cf7-311">クラス LedgerJournalDP.insertLedgerJournalTmp</span><span class="sxs-lookup"><span data-stu-id="e2cf7-311">Class LedgerJournalDP.insertLedgerJournalTmp</span></span>|
|<span data-ttu-id="e2cf7-312">クラス LedgerJournalGetTrans.createLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-312">Class LedgerJournalGetTrans.createLedgerJournalTrans</span></span>|
|<span data-ttu-id="e2cf7-313">クラス LedgerVoucherObject.addTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-313">Class LedgerVoucherObject.addTrans</span></span>|
|<span data-ttu-id="e2cf7-314">クラス LedgerVoucherTransObject.check</span><span class="sxs-lookup"><span data-stu-id="e2cf7-314">Class LedgerVoucherTransObject.check</span></span>|
|<span data-ttu-id="e2cf7-315">クラス LogisticsLocationSelectForm.construct</span><span class="sxs-lookup"><span data-stu-id="e2cf7-315">Class LogisticsLocationSelectForm.construct</span></span>|
|<span data-ttu-id="e2cf7-316">クラス LogisticsLocationSelectForm.main</span><span class="sxs-lookup"><span data-stu-id="e2cf7-316">Class LogisticsLocationSelectForm.main</span></span>|
|<span data-ttu-id="e2cf7-317">クラス LogisticsPostalAddressFormHandlerExt.onNewParameters_delegate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-317">Class LogisticsPostalAddressFormHandlerExt.onNewParameters_delegate</span></span>|
|<span data-ttu-id="e2cf7-318">クラス MCRItemListGeneration.generateItemListLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-318">Class MCRItemListGeneration.generateItemListLines</span></span>|
|<span data-ttu-id="e2cf7-319">クラス MCRItemListGeneration.generateItemListLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-319">Class MCRItemListGeneration.generateItemListLines</span></span>|
|<span data-ttu-id="e2cf7-320">クラス MCRMarginAlert.skipMarginCalc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-320">Class MCRMarginAlert.skipMarginCalc</span></span>|
|<span data-ttu-id="e2cf7-321">クラス Markup.mcrDeleteNonUser</span><span class="sxs-lookup"><span data-stu-id="e2cf7-321">Class Markup.mcrDeleteNonUser</span></span>|
|<span data-ttu-id="e2cf7-322">クラス MarkupAllocationSelectionManager.setQueryRanges</span><span class="sxs-lookup"><span data-stu-id="e2cf7-322">Class MarkupAllocationSelectionManager.setQueryRanges</span></span>|
|<span data-ttu-id="e2cf7-323">クラス PSAProjInvoiceDP.insertPSAProjInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="e2cf7-323">Class PSAProjInvoiceDP.insertPSAProjInvoiceTmp</span></span>|
|<span data-ttu-id="e2cf7-324">クラス PSAProjInvoiceDP.insertProformaPSAProjInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="e2cf7-324">Class PSAProjInvoiceDP.insertProformaPSAProjInvoiceTmp</span></span> |
|<span data-ttu-id="e2cf7-325">クラス PdsApprovedVendorListCheck.newBasedOnTableType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-325">Class PdsApprovedVendorListCheck.newBasedOnTableType</span></span>|
|<span data-ttu-id="e2cf7-326">クラス PlanActivityTimeCalculation.calculatePlanActivityTime</span><span class="sxs-lookup"><span data-stu-id="e2cf7-326">Class PlanActivityTimeCalculation.calculatePlanActivityTime</span></span>|
|<span data-ttu-id="e2cf7-327">クラス PordJournalCreateBOM.createLinesProdBOM</span><span class="sxs-lookup"><span data-stu-id="e2cf7-327">Class PordJournalCreateBOM.createLinesProdBOM</span></span>|
|<span data-ttu-id="e2cf7-328">クラス PriceDisc.accountRelation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-328">Class PriceDisc.accountRelation</span></span>|
|<span data-ttu-id="e2cf7-329">クラス PriceDisc.findDiscAgreement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-329">Class PriceDisc.findDiscAgreement</span></span>|
|<span data-ttu-id="e2cf7-330">クラス PriceDisc.findDisc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-330">Class PriceDisc.findDisc</span></span>|
|<span data-ttu-id="e2cf7-331">クラス PriceDisc.findPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-331">Class PriceDisc.findPriceAgreement</span></span>|
|<span data-ttu-id="e2cf7-332">クラス PriceTypeConverter.priceTypeToPriceGroupType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-332">Class PriceTypeConverter.priceTypeToPriceGroupType</span></span>|
|<span data-ttu-id="e2cf7-333">クラス PrintMgmtReportFormatSubscriber.add</span><span class="sxs-lookup"><span data-stu-id="e2cf7-333">Class PrintMgmtReportFormatSubscriber.add</span></span>|
|<span data-ttu-id="e2cf7-334">クラス PrintMgmtReportFormatSubscriber.populate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-334">Class PrintMgmtReportFormatSubscriber.populate</span></span>|
|<span data-ttu-id="e2cf7-335">クラス ProdBOM.prodFlushingPrincipItem2BOM</span><span class="sxs-lookup"><span data-stu-id="e2cf7-335">Class ProdBOM.prodFlushingPrincipItem2BOM</span></span>|
|<span data-ttu-id="e2cf7-336">クラス ProdJournalCreateBOM.createLinesInventTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-336">Class ProdJournalCreateBOM.createLinesInventTrans</span></span>|
|<span data-ttu-id="e2cf7-337">クラス ProdJournalCreateBOM.createLinesInventTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-337">Class ProdJournalCreateBOM.createLinesInventTrans</span></span>|
|<span data-ttu-id="e2cf7-338">クラス ProdJournalCreateBOM.createLinesProdBOM</span><span class="sxs-lookup"><span data-stu-id="e2cf7-338">Class ProdJournalCreateBOM.createLinesProdBOM</span></span>|
|<span data-ttu-id="e2cf7-339">クラス ProdJournalCreateBOM.dialog</span><span class="sxs-lookup"><span data-stu-id="e2cf7-339">Class ProdJournalCreateBOM.dialog</span></span>|
|<span data-ttu-id="e2cf7-340">クラス ProdJournalCreateBOM.validate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-340">Class ProdJournalCreateBOM.validate</span></span>|
|<span data-ttu-id="e2cf7-341">クラス ProdJournalFormTransBOM.setupCWFormControl</span><span class="sxs-lookup"><span data-stu-id="e2cf7-341">Class ProdJournalFormTransBOM.setupCWFormControl</span></span>|
|<span data-ttu-id="e2cf7-342">クラス ProdPickListController.prePromptModifyContract</span><span class="sxs-lookup"><span data-stu-id="e2cf7-342">Class ProdPickListController.prePromptModifyContract</span></span>|
|<span data-ttu-id="e2cf7-343">クラス ProdPicklistDP.insertValues</span><span class="sxs-lookup"><span data-stu-id="e2cf7-343">Class ProdPicklistDP.insertValues</span></span>|
|<span data-ttu-id="e2cf7-344">クラス ProdStatusType_Released.checkPostJournal</span><span class="sxs-lookup"><span data-stu-id="e2cf7-344">Class ProdStatusType_Released.checkPostJournal</span></span>|
|<span data-ttu-id="e2cf7-345">クラス ProdTableListPageInteraction.getEnabledControls</span><span class="sxs-lookup"><span data-stu-id="e2cf7-345">Class ProdTableListPageInteraction.getEnabledControls</span></span>|
|<span data-ttu-id="e2cf7-346">クラス ProdUpdReportFinished.updateBomConsumption</span><span class="sxs-lookup"><span data-stu-id="e2cf7-346">Class ProdUpdReportFinished.updateBomConsumption</span></span>|
|<span data-ttu-id="e2cf7-347">クラス ProdUpdReportFinished.updateRouteConsumption</span><span class="sxs-lookup"><span data-stu-id="e2cf7-347">Class ProdUpdReportFinished.updateRouteConsumption</span></span>|
|<span data-ttu-id="e2cf7-348">クラス ProdUpdSplit.createSplitToProduction</span><span class="sxs-lookup"><span data-stu-id="e2cf7-348">Class ProdUpdSplit.createSplitToProduction</span></span>|
|<span data-ttu-id="e2cf7-349">クラス ProdUpdStartUp.getListOfBOMJournals</span><span class="sxs-lookup"><span data-stu-id="e2cf7-349">Class ProdUpdStartUp.getListOfBOMJournals</span></span>|
|<span data-ttu-id="e2cf7-350">クラス ProdUpdStartUp.updateBOMConsmption</span><span class="sxs-lookup"><span data-stu-id="e2cf7-350">Class ProdUpdStartUp.updateBOMConsmption</span></span>|
|<span data-ttu-id="e2cf7-351">クラス ProjInvoiceDP.insertIntoProjInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="e2cf7-351">Class ProjInvoiceDP.insertIntoProjInvoiceTmp</span></span>|
|<span data-ttu-id="e2cf7-352">クラス ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-352">Class ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="e2cf7-353">クラス ProjInvoiceProposalInsertLines::run()</span><span class="sxs-lookup"><span data-stu-id="e2cf7-353">Class ProjInvoiceProposalInsertLines::run()</span></span>|
|<span data-ttu-id="e2cf7-354">クラス ProjPlanVersionsManager</span><span class="sxs-lookup"><span data-stu-id="e2cf7-354">Class ProjPlanVersionsManager</span></span>|
|<span data-ttu-id="e2cf7-355">クラス ProjPostItemJournal::projTransCreate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-355">Class ProjPostItemJournal::projTransCreate</span></span>|
|<span data-ttu-id="e2cf7-356">クラス ProjProposalTotals.calc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-356">Class ProjProposalTotals.calc</span></span>|
|<span data-ttu-id="e2cf7-357">クラス PsaProjInvoiceDP::insertProformaPSAProjInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="e2cf7-357">Class PsaProjInvoiceDP::insertProformaPSAProjInvoiceTmp</span></span>|
|<span data-ttu-id="e2cf7-358">クラス PsacustomerRetention.createFeeTransactionForProposal</span><span class="sxs-lookup"><span data-stu-id="e2cf7-358">Class PsacustomerRetention.createFeeTransactionForProposal</span></span>|
|<span data-ttu-id="e2cf7-359">クラス PurchAgreementGenerateReleaseOrder.check</span><span class="sxs-lookup"><span data-stu-id="e2cf7-359">Class PurchAgreementGenerateReleaseOrder.check</span></span>|
|<span data-ttu-id="e2cf7-360">クラス PurchAgreementGenerateReleaseOrder.validatePurchLinesWithPurchQty</span><span class="sxs-lookup"><span data-stu-id="e2cf7-360">Class PurchAgreementGenerateReleaseOrder.validatePurchLinesWithPurchQty</span></span>|
|<span data-ttu-id="e2cf7-361">クラス PurchAutoCreate.construct</span><span class="sxs-lookup"><span data-stu-id="e2cf7-361">Class PurchAutoCreate.construct</span></span>|
|<span data-ttu-id="e2cf7-362">クラス PurchAutoCreate.construct</span><span class="sxs-lookup"><span data-stu-id="e2cf7-362">Class PurchAutoCreate.construct</span></span>|
|<span data-ttu-id="e2cf7-363">クラス PurchAutoCreate_RFQ.construct</span><span class="sxs-lookup"><span data-stu-id="e2cf7-363">Class PurchAutoCreate_RFQ.construct</span></span>|
|<span data-ttu-id="e2cf7-364">クラス PurchAutoCreate_SalesProjectItemReq.createLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-364">Class PurchAutoCreate_SalesProjectItemReq.createLine</span></span>|
|<span data-ttu-id="e2cf7-365">クラス PurchAutoCreate_SalesProjectItemReq.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-365">Class PurchAutoCreate_SalesProjectItemReq.createPurchLine</span></span>|
|<span data-ttu-id="e2cf7-366">クラス PurchCancel.parmPurchTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-366">Class PurchCancel.parmPurchTable</span></span>|
|<span data-ttu-id="e2cf7-367">クラス PurchCancel.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-367">Class PurchCancel.run</span></span>|
|<span data-ttu-id="e2cf7-368">クラス PurchCopying.deleteLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-368">Class PurchCopying.deleteLines</span></span>|
|<span data-ttu-id="e2cf7-369">クラス PurchCreateFromSalesOrder</span><span class="sxs-lookup"><span data-stu-id="e2cf7-369">Class PurchCreateFromSalesOrder</span></span>|
|<span data-ttu-id="e2cf7-370">クラス PurchFormLetterParmData.createParmLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-370">Class PurchFormLetterParmData.createParmLine</span></span>|
|<span data-ttu-id="e2cf7-371">クラス PurchFormLetterParmDataInvoice.createParmLineAndSubLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-371">Class PurchFormLetterParmDataInvoice.createParmLineAndSubLines</span></span>|
|<span data-ttu-id="e2cf7-372">クラス PurchFormletterParmData.reSelectLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-372">Class PurchFormletterParmData.reSelectLines</span></span>|
|<span data-ttu-id="e2cf7-373">クラス PurchFormletterParmDataApproveJournal.updateQueryBuild</span><span class="sxs-lookup"><span data-stu-id="e2cf7-373">Class PurchFormletterParmDataApproveJournal.updateQueryBuild</span></span>|
|<span data-ttu-id="e2cf7-374">クラス PurchFormletterParmDataInvoice</span><span class="sxs-lookup"><span data-stu-id="e2cf7-374">Class PurchFormletterParmDataInvoice</span></span>|
|<span data-ttu-id="e2cf7-375">クラス PurchInvoiceCreate.createJournalLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-375">Class PurchInvoiceCreate.createJournalLine</span></span>|
|<span data-ttu-id="e2cf7-376">クラス PurchInvoiceJournalCreate.checkInvoicePolicies</span><span class="sxs-lookup"><span data-stu-id="e2cf7-376">Class PurchInvoiceJournalCreate.checkInvoicePolicies</span></span>|
|<span data-ttu-id="e2cf7-377">クラス PurchInvoiceJournalCreate.checkMatching</span><span class="sxs-lookup"><span data-stu-id="e2cf7-377">Class PurchInvoiceJournalCreate.checkMatching</span></span>|
|<span data-ttu-id="e2cf7-378">クラス PurchInvoiceJournalPost.createFixedAsset</span><span class="sxs-lookup"><span data-stu-id="e2cf7-378">Class PurchInvoiceJournalPost.createFixedAsset</span></span>|
|<span data-ttu-id="e2cf7-379">クラス PurchInvoiceJournalPost.lateMatchPackingSlip</span><span class="sxs-lookup"><span data-stu-id="e2cf7-379">Class PurchInvoiceJournalPost.lateMatchPackingSlip</span></span>|
|<span data-ttu-id="e2cf7-380">クラス PurchLineType.validateWrite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-380">Class PurchLineType.validateWrite</span></span>|
|<span data-ttu-id="e2cf7-381">クラス PurchLineVersioningFieldSet.isChangeConfirmationRequired</span><span class="sxs-lookup"><span data-stu-id="e2cf7-381">Class PurchLineVersioningFieldSet.isChangeConfirmationRequired</span></span>|
|<span data-ttu-id="e2cf7-382">クラス PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="e2cf7-382">Class PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="e2cf7-383">クラス PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="e2cf7-383">Class PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="e2cf7-384">クラス PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="e2cf7-384">Class PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="e2cf7-385">クラス PurchPackingSlipDP.createProductReceiptLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-385">Class PurchPackingSlipDP.createProductReceiptLines</span></span>|
|<span data-ttu-id="e2cf7-386">クラス PurchPackingSlipJournalPost.selectFormletterJournalTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-386">Class PurchPackingSlipJournalPost.selectFormletterJournalTrans</span></span>|
|<span data-ttu-id="e2cf7-387">クラス PurchRFQCaseAutoCreate.newAutoCreate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-387">Class PurchRFQCaseAutoCreate.newAutoCreate</span></span>|
|<span data-ttu-id="e2cf7-388">クラス PurchReApprovalPolicyRuleFieldList.addTable2Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e2cf7-388">Class PurchReApprovalPolicyRuleFieldList.addTable2Hierarchy</span></span>|
|<span data-ttu-id="e2cf7-389">クラス PurchReApprovalPolicyRuleFieldList.addTable2Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e2cf7-389">Class PurchReApprovalPolicyRuleFieldList.addTable2Hierarchy</span></span>|
|<span data-ttu-id="e2cf7-390">クラス PurchSelectLinesManager.passSets</span><span class="sxs-lookup"><span data-stu-id="e2cf7-390">Class PurchSelectLinesManager.passSets</span></span>|
|<span data-ttu-id="e2cf7-391">クラス PurchTableInteraction.enableHeaderPurchase</span><span class="sxs-lookup"><span data-stu-id="e2cf7-391">Class PurchTableInteraction.enableHeaderPurchase</span></span>|
|<span data-ttu-id="e2cf7-392">クラス PurchTableInteractionHelper.getJournalEnquiryButtons</span><span class="sxs-lookup"><span data-stu-id="e2cf7-392">Class PurchTableInteractionHelper.getJournalEnquiryButtons</span></span>|
|<span data-ttu-id="e2cf7-393">クラス PurchTableInteractionHelper.getUpdateJournalButtons</span><span class="sxs-lookup"><span data-stu-id="e2cf7-393">Class PurchTableInteractionHelper.getUpdateJournalButtons</span></span>|
|<span data-ttu-id="e2cf7-394">クラス PurchaseOrderResponseConsume.checkIfPurchLinesRequireUpdate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-394">Class PurchaseOrderResponseConsume.checkIfPurchLinesRequireUpdate</span></span>|
|<span data-ttu-id="e2cf7-395">クラス PurchaseOrderResponseConsume.checkIfResponseLineCannotBeConsumedAndUpdateConsumptionState</span><span class="sxs-lookup"><span data-stu-id="e2cf7-395">Class PurchaseOrderResponseConsume.checkIfResponseLineCannotBeConsumedAndUpdateConsumptionState</span></span>|
|<span data-ttu-id="e2cf7-396">クラス PurchaseOrderResponseConsume.consumeFirstPurchaseOrderResponeLineAndInitiateArchivingOnPurchLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-396">Class PurchaseOrderResponseConsume.consumeFirstPurchaseOrderResponeLineAndInitiateArchivingOnPurchLine</span></span>|
|<span data-ttu-id="e2cf7-397">クラス PurchaseOrderResponseConsume.consumeRemainingPurchaseOrderResponseLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-397">Class PurchaseOrderResponseConsume.consumeRemainingPurchaseOrderResponseLines</span></span>|
|<span data-ttu-id="e2cf7-398">クラス PurchaseOrderResponseConsumeLine.checkIfSelectedPurchLinesRequireUpdate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-398">Class PurchaseOrderResponseConsumeLine.checkIfSelectedPurchLinesRequireUpdate</span></span>|
|<span data-ttu-id="e2cf7-399">クラス ReqCalc.covCodeQty</span><span class="sxs-lookup"><span data-stu-id="e2cf7-399">Class ReqCalc.covCodeQty</span></span>|
|<span data-ttu-id="e2cf7-400">クラス ReqCalc.insertItemInventSum</span><span class="sxs-lookup"><span data-stu-id="e2cf7-400">Class ReqCalc.insertItemInventSum</span></span>|
|<span data-ttu-id="e2cf7-401">クラス ReqCalc.insertItemInventTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-401">Class ReqCalc.insertItemInventTrans</span></span>|
|<span data-ttu-id="e2cf7-402">クラス ReqTransFormPo.validateFromInventLocationId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-402">Class ReqTransFormPo.validateFromInventLocationId</span></span>|
|<span data-ttu-id="e2cf7-403">クラス ReqTransPoMarkChangeToRFQ.DialogPostRun</span><span class="sxs-lookup"><span data-stu-id="e2cf7-403">Class ReqTransPoMarkChangeToRFQ.DialogPostRun</span></span>|
|<span data-ttu-id="e2cf7-404">クラス ReqTransPoMarkFirm.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-404">Class ReqTransPoMarkFirm.createPurchLine</span></span>|
|<span data-ttu-id="e2cf7-405">クラス ReqTransPoMarkFirm.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-405">Class ReqTransPoMarkFirm.setPurchTable</span></span>|
|<span data-ttu-id="e2cf7-406">クラス RetailAssortmentLookupTask.explodeAssortments</span><span class="sxs-lookup"><span data-stu-id="e2cf7-406">Class RetailAssortmentLookupTask.explodeAssortments</span></span>|
|<span data-ttu-id="e2cf7-407">クラス RetailCreateLinesFromProductsToAdd.createPeriodicDiscount</span><span class="sxs-lookup"><span data-stu-id="e2cf7-407">Class RetailCreateLinesFromProductsToAdd.createPeriodicDiscount</span></span>|
|<span data-ttu-id="e2cf7-408">クラス RetailCreateLinesFromProductsToAdd.loadLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-408">Class RetailCreateLinesFromProductsToAdd.loadLines</span></span>|
|<span data-ttu-id="e2cf7-409">クラス RetailPackagePurchManagement.createLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-409">Class RetailPackagePurchManagement.createLines</span></span>|
|<span data-ttu-id="e2cf7-410">クラス RetailProductPropertyManager.saveInventTableAndRelated</span><span class="sxs-lookup"><span data-stu-id="e2cf7-410">Class RetailProductPropertyManager.saveInventTableAndRelated</span></span>|
|<span data-ttu-id="e2cf7-411">クラス RetailProductPropertyManager.validateWriteOnInventTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-411">Class RetailProductPropertyManager.validateWriteOnInventTable</span></span>|
|<span data-ttu-id="e2cf7-412">クラス RetailSalesOrderCalculator.saveSalesOrder</span><span class="sxs-lookup"><span data-stu-id="e2cf7-412">Class RetailSalesOrderCalculator.saveSalesOrder</span></span>|
|<span data-ttu-id="e2cf7-413">クラス RetailSalesOrderCalculator.setPriceOnCurrentLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-413">Class RetailSalesOrderCalculator.setPriceOnCurrentLine</span></span>|
|<span data-ttu-id="e2cf7-414">クラス RetailSalesQuotationCalculator.saveSalesQuote</span><span class="sxs-lookup"><span data-stu-id="e2cf7-414">Class RetailSalesQuotationCalculator.saveSalesQuote</span></span>|
|<span data-ttu-id="e2cf7-415">クラス RetailSalesQuotationCalculator.setPricesOnCurrentLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-415">Class RetailSalesQuotationCalculator.setPricesOnCurrentLine</span></span>|
|<span data-ttu-id="e2cf7-416">クラス ReturnTableInteraction.enableControl</span><span class="sxs-lookup"><span data-stu-id="e2cf7-416">Class ReturnTableInteraction.enableControl</span></span>|
|<span data-ttu-id="e2cf7-417">クラス RouteCopyToRoute.insertRouteOpr</span><span class="sxs-lookup"><span data-stu-id="e2cf7-417">Class RouteCopyToRoute.insertRouteOpr</span></span>|
|<span data-ttu-id="e2cf7-418">クラス SMAServiceFunctionLine_Transfer.checkJournalType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-418">Class SMAServiceFunctionLine_Transfer.checkJournalType</span></span>|
|<span data-ttu-id="e2cf7-419">クラス SMAServiceFunctionLine_Transfer.postJournalType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-419">Class SMAServiceFunctionLine_Transfer.postJournalType</span></span>|
|<span data-ttu-id="e2cf7-420">クラス SMAServiceFunctionLine_Transfer.sumjournals</span><span class="sxs-lookup"><span data-stu-id="e2cf7-420">Class SMAServiceFunctionLine_Transfer.sumjournals</span></span>|
|<span data-ttu-id="e2cf7-421">クラス SMAServiceOrderCreate.createServiceOrderLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-421">Class SMAServiceOrderCreate.createServiceOrderLine</span></span>|
|<span data-ttu-id="e2cf7-422">クラス SalesAutoCreate_ReleaseFromAgreement.createSalesTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-422">Class SalesAutoCreate_ReleaseFromAgreement.createSalesTable</span></span>|
|<span data-ttu-id="e2cf7-423">クラス SalesCancelOrder.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-423">Class SalesCancelOrder.run</span></span>|
|<span data-ttu-id="e2cf7-424">クラス SalesCopying.copy</span><span class="sxs-lookup"><span data-stu-id="e2cf7-424">Class SalesCopying.copy</span></span>|
|<span data-ttu-id="e2cf7-425">クラス SalesCreateOrderFromCutomer.main</span><span class="sxs-lookup"><span data-stu-id="e2cf7-425">Class SalesCreateOrderFromCutomer.main</span></span>|
|<span data-ttu-id="e2cf7-426">クラス SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="e2cf7-426">Class SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="e2cf7-427">クラス SalesFormLetterParmData.createParmLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-427">Class SalesFormLetterParmData.createParmLine</span></span>|
|<span data-ttu-id="e2cf7-428">クラス SalesFormLetterReport.construct</span><span class="sxs-lookup"><span data-stu-id="e2cf7-428">Class SalesFormLetterReport.construct</span></span>|
|<span data-ttu-id="e2cf7-429">クラス SalesFormletterParmData.reSelectLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-429">Class SalesFormletterParmData.reSelectLines</span></span>|
|<span data-ttu-id="e2cf7-430">クラス SalesFormletterParmDataInvoice.reSelectInit</span><span class="sxs-lookup"><span data-stu-id="e2cf7-430">Class SalesFormletterParmDataInvoice.reSelectInit</span></span>|
|<span data-ttu-id="e2cf7-431">クラス SalesInvoiceDP.invoiceTxt</span><span class="sxs-lookup"><span data-stu-id="e2cf7-431">Class SalesInvoiceDP.invoiceTxt</span></span>|
|<span data-ttu-id="e2cf7-432">クラス SalesInvoiceDP.itemId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-432">Class SalesInvoiceDP.itemId</span></span>|
|<span data-ttu-id="e2cf7-433">クラス SalesLineCopyFromSource.updateCopiedLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-433">Class SalesLineCopyFromSource.updateCopiedLine</span></span>|
|<span data-ttu-id="e2cf7-434">クラス SalesLineType.setReservation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-434">Class SalesLineType.setReservation</span></span>|
|<span data-ttu-id="e2cf7-435">クラス SalesLineType.setSalesStatus</span><span class="sxs-lookup"><span data-stu-id="e2cf7-435">Class SalesLineType.setSalesStatus</span></span>|
|<span data-ttu-id="e2cf7-436">クラス SalesLineType.syncPurchLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-436">Class SalesLineType.syncPurchLine</span></span>|
|<span data-ttu-id="e2cf7-437">クラス SalesPackingSlipDP.createSalesPackingSlipLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-437">Class SalesPackingSlipDP.createSalesPackingSlipLines</span></span>|
|<span data-ttu-id="e2cf7-438">クラス SalesPackingSlipJournalPost.addToInventReportDimHistory</span><span class="sxs-lookup"><span data-stu-id="e2cf7-438">Class SalesPackingSlipJournalPost.addToInventReportDimHistory</span></span>|
|<span data-ttu-id="e2cf7-439">クラス SalesPurchLineInterface.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-439">Class SalesPurchLineInterface.setPriceAgreement</span></span>|
|<span data-ttu-id="e2cf7-440">クラス SalesQuotationCopying.copyHeader</span><span class="sxs-lookup"><span data-stu-id="e2cf7-440">Class SalesQuotationCopying.copyHeader</span></span>|
|<span data-ttu-id="e2cf7-441">クラス SalesQuotationEditLinesForm_Sales_Confir.createSalesTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-441">Class SalesQuotationEditLinesForm_Sales_Confir.createSalesTable</span></span>|
|<span data-ttu-id="e2cf7-442">クラス SalesQuotationEditLinesForm</span><span class="sxs-lookup"><span data-stu-id="e2cf7-442">Class SalesQuotationEditLinesForm</span></span>|
|<span data-ttu-id="e2cf7-443">クラス SalesQuotationLineType_Sales.validateWrite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-443">Class SalesQuotationLineType_Sales.validateWrite</span></span>|
|<span data-ttu-id="e2cf7-444">クラス SalesTableListPageInteraction.setButtonInterCompany</span><span class="sxs-lookup"><span data-stu-id="e2cf7-444">Class SalesTableListPageInteraction.setButtonInterCompany</span></span>|
|<span data-ttu-id="e2cf7-445">クラス SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-445">Class SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="e2cf7-446">クラス SalesTableType.interCompanyMirror</span><span class="sxs-lookup"><span data-stu-id="e2cf7-446">Class SalesTableType.interCompanyMirror</span></span>|
|<span data-ttu-id="e2cf7-447">クラス SmmCampaignQueries</span><span class="sxs-lookup"><span data-stu-id="e2cf7-447">Class SmmCampaignQueries</span></span>|
|<span data-ttu-id="e2cf7-448">クラス SmmLeadUpdate</span><span class="sxs-lookup"><span data-stu-id="e2cf7-448">Class SmmLeadUpdate</span></span>|
|<span data-ttu-id="e2cf7-449">クラス SmmOpportunityLink</span><span class="sxs-lookup"><span data-stu-id="e2cf7-449">Class SmmOpportunityLink</span></span>|
|<span data-ttu-id="e2cf7-450">クラス SmmUpdateBusRel.updateFromCustTableSFA2</span><span class="sxs-lookup"><span data-stu-id="e2cf7-450">Class SmmUpdateBusRel.updateFromCustTableSFA2</span></span>|
|<span data-ttu-id="e2cf7-451">クラス TradeCurrencyConversionPrompt.construct</span><span class="sxs-lookup"><span data-stu-id="e2cf7-451">Class TradeCurrencyConversionPrompt.construct</span></span>|
|<span data-ttu-id="e2cf7-452">クラス TradeLineRenumbering.renumber</span><span class="sxs-lookup"><span data-stu-id="e2cf7-452">Class TradeLineRenumbering.renumber</span></span>|
|<span data-ttu-id="e2cf7-453">クラス TradeTotals.calc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-453">Class TradeTotals.calc</span></span>|
|<span data-ttu-id="e2cf7-454">クラス VendDocumentLineInterface.setPurchaseQty</span><span class="sxs-lookup"><span data-stu-id="e2cf7-454">Class VendDocumentLineInterface.setPurchaseQty</span></span>|
|<span data-ttu-id="e2cf7-455">クラス VendInvoicePolicyValidation.policyViolationMessage</span><span class="sxs-lookup"><span data-stu-id="e2cf7-455">Class VendInvoicePolicyValidation.policyViolationMessage</span></span>|
|<span data-ttu-id="e2cf7-456">クラス VendProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="e2cf7-456">Class VendProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="e2cf7-457">クラス WHSPool.pickFromWorkCenter</span><span class="sxs-lookup"><span data-stu-id="e2cf7-457">Class WHSPool.pickFromWorkCenter</span></span>|
|<span data-ttu-id="e2cf7-458">クラス WHSShipConfirm.createUOMStructure</span><span class="sxs-lookup"><span data-stu-id="e2cf7-458">Class WHSShipConfirm.createUOMStructure</span></span>|
|<span data-ttu-id="e2cf7-459">クラス WHSWorkExecute.pickLicensePlateHandledByLP</span><span class="sxs-lookup"><span data-stu-id="e2cf7-459">Class WHSWorkExecute.pickLicensePlateHandledByLP</span></span>|
|<span data-ttu-id="e2cf7-460">クラス WhsInventOnHandReserve.changeReservation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-460">Class WhsInventOnHandReserve.changeReservation</span></span>|
|<span data-ttu-id="e2cf7-461">クラス WhsInventOnHandReserve.setMovement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-461">Class WhsInventOnHandReserve.setMovement</span></span>|
|<span data-ttu-id="e2cf7-462">クラス WhsPackForm.buttonPack_clicked</span><span class="sxs-lookup"><span data-stu-id="e2cf7-462">Class WhsPackForm.buttonPack_clicked</span></span>|
|<span data-ttu-id="e2cf7-463">クラス WhsPostEngineBase.createLoadFromShipment</span><span class="sxs-lookup"><span data-stu-id="e2cf7-463">Class WhsPostEngineBase.createLoadFromShipment</span></span>|
|<span data-ttu-id="e2cf7-464">クラス WhsShipConfirm.createInventTransferParmLineTMS</span><span class="sxs-lookup"><span data-stu-id="e2cf7-464">Class WhsShipConfirm.createInventTransferParmLineTMS</span></span>|
|<span data-ttu-id="e2cf7-465">クラス WhsShipConfirm.createInventTransferParmLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-465">Class WhsShipConfirm.createInventTransferParmLine</span></span>|
|<span data-ttu-id="e2cf7-466">クラス WhsWorkExecute</span><span class="sxs-lookup"><span data-stu-id="e2cf7-466">Class WhsWorkExecute</span></span>|
|<span data-ttu-id="e2cf7-467">クラス WmsBillOfLadingDP::insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-467">Class WmsBillOfLadingDP::insertIntoTempTable</span></span>|
|<span data-ttu-id="e2cf7-468">クラス WmsOrderTransType_OutputDontPostTransfer.updateParentMovement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-468">Class WmsOrderTransType_OutputDontPostTransfer.updateParentMovement</span></span>|
|<span data-ttu-id="e2cf7-469">クラス WrkCtrCapResHandler.hasNewCapacityReservation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-469">Class WrkCtrCapResHandler.hasNewCapacityReservation</span></span>|
|<span data-ttu-id="e2cf7-470">クラス WrkCtrCapResHandler.loadCapacityReservations</span><span class="sxs-lookup"><span data-stu-id="e2cf7-470">Class WrkCtrCapResHandler.loadCapacityReservations</span></span>|
|<span data-ttu-id="e2cf7-471">クラス WrkCtrReservedSum.calcReservationSumGroupId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-471">Class WrkCtrReservedSum.calcReservationSumGroupId</span></span>|
|<span data-ttu-id="e2cf7-472">クラス WrkCtrReservedSum.calcReservationSumGroupId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-472">Class WrkCtrReservedSum.calcReservationSumGroupId</span></span>|
|<span data-ttu-id="e2cf7-473">クラス WrkCtrReservedSum.calcReservationSumWrkCtrId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-473">Class WrkCtrReservedSum.calcReservationSumWrkCtrId</span></span>|
|<span data-ttu-id="e2cf7-474">クラス WrkCtrReservedSum.calcReservationSumWrkCtrId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-474">Class WrkCtrReservedSum.calcReservationSumWrkCtrId</span></span>|
|<span data-ttu-id="e2cf7-475">クラス WrkCtrScheduler_Prod.saveOperation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-475">Class WrkCtrScheduler_Prod.saveOperation</span></span>|
|<span data-ttu-id="e2cf7-476">クラス createParmLinesFromTransferLinesOnLoad</span><span class="sxs-lookup"><span data-stu-id="e2cf7-476">Class createParmLinesFromTransferLinesOnLoad</span></span>|
|<span data-ttu-id="e2cf7-477">クラス smmCampaignQueries.lookupClass</span><span class="sxs-lookup"><span data-stu-id="e2cf7-477">Class smmCampaignQueries.lookupClass</span></span>|
|<span data-ttu-id="e2cf7-478">エンティティ EcoResProductDimensionGroupEntity.dataSourceDimensionFieldId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-478">Entity EcoResProductDimensionGroupEntity.dataSourceDimensionFieldId</span></span>|
|<span data-ttu-id="e2cf7-479">エンティティ InventProductDefaultOrderSettingsEntity.insertEntityDataSource</span><span class="sxs-lookup"><span data-stu-id="e2cf7-479">Entity InventProductDefaultOrderSettingsEntity.insertEntityDataSource</span></span>|
|<span data-ttu-id="e2cf7-480">エンティティ InventProductSiteSpecificOrderSettingsEntity.insertEntityDataSource</span><span class="sxs-lookup"><span data-stu-id="e2cf7-480">Entity InventProductSiteSpecificOrderSettingsEntity.insertEntityDataSource</span></span>|
|<span data-ttu-id="e2cf7-481">エンティティ PSAActualEntity.createQuery_LaborConsumptionQty</span><span class="sxs-lookup"><span data-stu-id="e2cf7-481">Entity PSAActualEntity.createQuery_LaborConsumptionQty</span></span>|
|<span data-ttu-id="e2cf7-482">エンティティ PSAActualEntity.createQuery_LaborConsumption</span><span class="sxs-lookup"><span data-stu-id="e2cf7-482">Entity PSAActualEntity.createQuery_LaborConsumption</span></span>|
|<span data-ttu-id="e2cf7-483">エンティティ PSAActualEntity.createQuery_PlLaborCost</span><span class="sxs-lookup"><span data-stu-id="e2cf7-483">Entity PSAActualEntity.createQuery_PlLaborCost</span></span>|
|<span data-ttu-id="e2cf7-484">エンティティ PSAActualEntity.createQuery_PlLaborQty</span><span class="sxs-lookup"><span data-stu-id="e2cf7-484">Entity PSAActualEntity.createQuery_PlLaborQty</span></span>|
|<span data-ttu-id="e2cf7-485">エンティティ PSAForecastEntity.createQuery_LaborConsumptionForecastQty</span><span class="sxs-lookup"><span data-stu-id="e2cf7-485">Entity PSAForecastEntity.createQuery_LaborConsumptionForecastQty</span></span>|
|<span data-ttu-id="e2cf7-486">エンティティ PSAForecastEntity.createQuery_LaborConsumptionForecast</span><span class="sxs-lookup"><span data-stu-id="e2cf7-486">Entity PSAForecastEntity.createQuery_LaborConsumptionForecast</span></span>|
|<span data-ttu-id="e2cf7-487">エンティティ PSAForecastEntity.createQuery_PlLaborForecastCost</span><span class="sxs-lookup"><span data-stu-id="e2cf7-487">Entity PSAForecastEntity.createQuery_PlLaborForecastCost</span></span>|
|<span data-ttu-id="e2cf7-488">エンティティ PSAForecastEntity.createQuery_PlLaborForecastQty</span><span class="sxs-lookup"><span data-stu-id="e2cf7-488">Entity PSAForecastEntity.createQuery_PlLaborForecastQty</span></span>|
|<span data-ttu-id="e2cf7-489">フォーム BOMCalcDialog.updateDesign</span><span class="sxs-lookup"><span data-stu-id="e2cf7-489">Form BOMCalcDialog.updateDesign</span></span>|
|<span data-ttu-id="e2cf7-490">フォーム EcoResProductCreate.releaseProductToCompany</span><span class="sxs-lookup"><span data-stu-id="e2cf7-490">Form EcoResProductCreate.releaseProductToCompany</span></span>|
|<span data-ttu-id="e2cf7-491">フォーム InventItemOrderSetup.InventItemSetupSupplyType.editOrderType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-491">Form InventItemOrderSetup.InventItemSetupSupplyType.editOrderType</span></span>|
|<span data-ttu-id="e2cf7-492">フォーム InventLocationIdLookup.InventDim_DS.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-492">Form InventLocationIdLookup.InventDim_DS.init</span></span>|
|<span data-ttu-id="e2cf7-493">フォーム InventLocationIdLookup.InventLocation_DS.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-493">Form InventLocationIdLookup.InventLocation_DS.init</span></span>|
|<span data-ttu-id="e2cf7-494">フォーム InventNonConformanceTable.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-494">Form InventNonConformanceTable.init</span></span>|
|<span data-ttu-id="e2cf7-495">フォーム InventNonConformanceTableCreate.InventNonConformanceTable.write</span><span class="sxs-lookup"><span data-stu-id="e2cf7-495">Form InventNonConformanceTableCreate.InventNonConformanceTable.write</span></span>|
|<span data-ttu-id="e2cf7-496">フォーム InventQualityOrderTableCreate.allowEdit</span><span class="sxs-lookup"><span data-stu-id="e2cf7-496">Form InventQualityOrderTableCreate.allowEdit</span></span>|
|<span data-ttu-id="e2cf7-497">フォーム InventQualityOrderTableCreate.refreshCaller</span><span class="sxs-lookup"><span data-stu-id="e2cf7-497">Form InventQualityOrderTableCreate.refreshCaller</span></span>|
|<span data-ttu-id="e2cf7-498">フォーム InventTestAssociationTable.initRecord</span><span class="sxs-lookup"><span data-stu-id="e2cf7-498">Form InventTestAssociationTable.initRecord</span></span>|
|<span data-ttu-id="e2cf7-499">フォーム InventTransPick\TmpInventTransWMS.validateWrite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-499">Form InventTransPick\TmpInventTransWMS.validateWrite</span></span>|
|<span data-ttu-id="e2cf7-500">フォーム LedgerTransVoucher.updateQueryForProject</span><span class="sxs-lookup"><span data-stu-id="e2cf7-500">Form LedgerTransVoucher.updateQueryForProject</span></span>|
|<span data-ttu-id="e2cf7-501">フォーム MarkupAllocation.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-501">Form MarkupAllocation.init</span></span>|
|<span data-ttu-id="e2cf7-502">フォーム MarkupAllocation_VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-502">Form MarkupAllocation_VendInvoiceTrans</span></span>|
|<span data-ttu-id="e2cf7-503">フォーム PdsBatchAttributes.PdsBatchAttributes.linkActive</span><span class="sxs-lookup"><span data-stu-id="e2cf7-503">Form PdsBatchAttributes.PdsBatchAttributes.linkActive</span></span>|
|<span data-ttu-id="e2cf7-504">フォーム PriceDiscAdmTable.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-504">Form PriceDiscAdmTable.init</span></span>|
|<span data-ttu-id="e2cf7-505">フォーム PriceDiscTable.appendInventCriteria</span><span class="sxs-lookup"><span data-stu-id="e2cf7-505">Form PriceDiscTable.appendInventCriteria</span></span>|
|<span data-ttu-id="e2cf7-506">フォーム PriceDiscTable.buildOrderLineFilter</span><span class="sxs-lookup"><span data-stu-id="e2cf7-506">Form PriceDiscTable.buildOrderLineFilter</span></span>|
|<span data-ttu-id="e2cf7-507">フォーム PriceDiscTable.buildSearchFilter</span><span class="sxs-lookup"><span data-stu-id="e2cf7-507">Form PriceDiscTable.buildSearchFilter</span></span>|
|<span data-ttu-id="e2cf7-508">フォーム PriceDiscTable.isLineFilterEnabled</span><span class="sxs-lookup"><span data-stu-id="e2cf7-508">Form PriceDiscTable.isLineFilterEnabled</span></span>|
|<span data-ttu-id="e2cf7-509">フォーム PriceDiscTable.retrieveRelationType</span><span class="sxs-lookup"><span data-stu-id="e2cf7-509">Form PriceDiscTable.retrieveRelationType</span></span>|
|<span data-ttu-id="e2cf7-510">フォーム ProdParmStartUp.ProdParmStartUp.active</span><span class="sxs-lookup"><span data-stu-id="e2cf7-510">Form ProdParmStartUp.ProdParmStartUp.active</span></span>|
|<span data-ttu-id="e2cf7-511">フォーム ProjCreditNoteSelect.editMark</span><span class="sxs-lookup"><span data-stu-id="e2cf7-511">Form ProjCreditNoteSelect.editMark</span></span>|
|<span data-ttu-id="e2cf7-512">フォーム ProjTableCreate.ProjTable.write</span><span class="sxs-lookup"><span data-stu-id="e2cf7-512">Form ProjTableCreate.ProjTable.write</span></span>|
|<span data-ttu-id="e2cf7-513">フォーム PurchCreateFromSalesOrder.initFields</span><span class="sxs-lookup"><span data-stu-id="e2cf7-513">Form PurchCreateFromSalesOrder.initFields</span></span>|
|<span data-ttu-id="e2cf7-514">フォーム PurchUpdateRemain.closeOk</span><span class="sxs-lookup"><span data-stu-id="e2cf7-514">Form PurchUpdateRemain.closeOk</span></span>|
|<span data-ttu-id="e2cf7-515">フォーム ReqTransPoMarkFirm.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-515">Form ReqTransPoMarkFirm.init</span></span>|
|<span data-ttu-id="e2cf7-516">フォーム RetailAddItems.closeOk</span><span class="sxs-lookup"><span data-stu-id="e2cf7-516">Form RetailAddItems.closeOk</span></span>|
|<span data-ttu-id="e2cf7-517">フォーム RetailColorGroupTable.RetailColorGroupTrans.recordHasChanges</span><span class="sxs-lookup"><span data-stu-id="e2cf7-517">Form RetailColorGroupTable.RetailColorGroupTrans.recordHasChanges</span></span>|
|<span data-ttu-id="e2cf7-518">フォーム RouteLookupOprNum.init</span><span class="sxs-lookup"><span data-stu-id="e2cf7-518">Form RouteLookupOprNum.init</span></span>|
|<span data-ttu-id="e2cf7-519">フォーム VendEditInvoice.invoiceAccountModified</span><span class="sxs-lookup"><span data-stu-id="e2cf7-519">Form VendEditInvoice.invoiceAccountModified</span></span>|
|<span data-ttu-id="e2cf7-520">フォーム VendEditInvoice.run</span><span class="sxs-lookup"><span data-stu-id="e2cf7-520">Form VendEditInvoice.run</span></span>|
|<span data-ttu-id="e2cf7-521">フォーム VendOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-521">Form VendOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="e2cf7-522">フォーム WrkCtrCapResGraphDialog.setParm</span><span class="sxs-lookup"><span data-stu-id="e2cf7-522">Form WrkCtrCapResGraphDialog.setParm</span></span>|
|<span data-ttu-id="e2cf7-523">マップ BomCalcTransMap.displayUnitId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-523">Map BomCalcTransMap.displayUnitId</span></span>|
|<span data-ttu-id="e2cf7-524">テーブル AssetTable.lookupAccountNum</span><span class="sxs-lookup"><span data-stu-id="e2cf7-524">Table AssetTable.lookupAccountNum</span></span>|
|<span data-ttu-id="e2cf7-525">テーブル AssetTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-525">Table AssetTrans</span></span>|
|<span data-ttu-id="e2cf7-526">テーブル CaseDetailBase.validateWrite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-526">Table CaseDetailBase.validateWrite</span></span>|
|<span data-ttu-id="e2cf7-527">テーブル EcoResProductMasterConfiguration.existWithSameConfigUnit</span><span class="sxs-lookup"><span data-stu-id="e2cf7-527">Table EcoResProductMasterConfiguration.existWithSameConfigUnit</span></span>|
|<span data-ttu-id="e2cf7-528">テーブル FormletterJournalTrans.getLinePrefix</span><span class="sxs-lookup"><span data-stu-id="e2cf7-528">Table FormletterJournalTrans.getLinePrefix</span></span>|
|<span data-ttu-id="e2cf7-529">テーブル InventItemPriceSim.autoSalesPrice</span><span class="sxs-lookup"><span data-stu-id="e2cf7-529">Table InventItemPriceSim.autoSalesPrice</span></span>|
|<span data-ttu-id="e2cf7-530">テーブル InventQualityOrderLine.adjustInt</span><span class="sxs-lookup"><span data-stu-id="e2cf7-530">Table InventQualityOrderLine.adjustInt</span></span>|
|<span data-ttu-id="e2cf7-531">テーブル InventQualityOrderTable.createInventQualityOrderLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-531">Table InventQualityOrderTable.createInventQualityOrderLines</span></span>|
|<span data-ttu-id="e2cf7-532">テーブル InventQualityOrderTable.initFromReference</span><span class="sxs-lookup"><span data-stu-id="e2cf7-532">Table InventQualityOrderTable.initFromReference</span></span>|
|<span data-ttu-id="e2cf7-533">テーブル InventQualityOrderTable.initQtyFromAssocation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-533">Table InventQualityOrderTable.initQtyFromAssocation</span></span>|
|<span data-ttu-id="e2cf7-534">テーブル InventTestAssocationTable.checkAccountRelation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-534">Table InventTestAssocationTable.checkAccountRelation</span></span>|
|<span data-ttu-id="e2cf7-535">テーブル InventTestAssocationTable.validateWrite</span><span class="sxs-lookup"><span data-stu-id="e2cf7-535">Table InventTestAssocationTable.validateWrite</span></span>|
|<span data-ttu-id="e2cf7-536">テーブル InventTrans.insertReturnTransOrigin</span><span class="sxs-lookup"><span data-stu-id="e2cf7-536">Table InventTrans.insertReturnTransOrigin</span></span>|
|<span data-ttu-id="e2cf7-537">テーブル InventTransOrigin.createOrigin</span><span class="sxs-lookup"><span data-stu-id="e2cf7-537">Table InventTransOrigin.createOrigin</span></span>|
|<span data-ttu-id="e2cf7-538">テーブル InventTransferParmLine.createPickLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-538">Table InventTransferParmLine.createPickLines</span></span>|
|<span data-ttu-id="e2cf7-539">テーブル InventTransferParmLine.createReceiveLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-539">Table InventTransferParmLine.createReceiveLines</span></span>|
|<span data-ttu-id="e2cf7-540">テーブル InventTransferParmLine.createShipLines</span><span class="sxs-lookup"><span data-stu-id="e2cf7-540">Table InventTransferParmLine.createShipLines</span></span>|
|<span data-ttu-id="e2cf7-541">テーブル JmgStampjournalTrans</span><span class="sxs-lookup"><span data-stu-id="e2cf7-541">Table JmgStampjournalTrans</span></span>|
|<span data-ttu-id="e2cf7-542">テーブル JmgTermReg.createJournalSignIn</span><span class="sxs-lookup"><span data-stu-id="e2cf7-542">Table JmgTermReg.createJournalSignIn</span></span>|
|<span data-ttu-id="e2cf7-543">テーブル JmgTermReg.update</span><span class="sxs-lookup"><span data-stu-id="e2cf7-543">Table JmgTermReg.update</span></span>|
|<span data-ttu-id="e2cf7-544">テーブル LedgerJournalTrans.delete</span><span class="sxs-lookup"><span data-stu-id="e2cf7-544">Table LedgerJournalTrans.delete</span></span>|
|<span data-ttu-id="e2cf7-545">テーブル LedgerJournalTrans.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="e2cf7-545">Table LedgerJournalTrans.validateWrite_Server</span></span>|
|<span data-ttu-id="e2cf7-546">テーブル PriceDiscAdm.getEntityAutoReportFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="e2cf7-546">Table PriceDiscAdm.getEntityAutoReportFieldGroupName</span></span>|
|<span data-ttu-id="e2cf7-547">テーブル PriceDiscAdm.getEntityJournalNumberFieldName</span><span class="sxs-lookup"><span data-stu-id="e2cf7-547">Table PriceDiscAdm.getEntityJournalNumberFieldName</span></span>|
|<span data-ttu-id="e2cf7-548">テーブル PriceDiscAdmTrans.CheckAccountRelation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-548">Table PriceDiscAdmTrans.CheckAccountRelation</span></span>|
|<span data-ttu-id="e2cf7-549">テーブル PriceDiscAdmTrans.checkItemRelation</span><span class="sxs-lookup"><span data-stu-id="e2cf7-549">Table PriceDiscAdmTrans.checkItemRelation</span></span>|
|<span data-ttu-id="e2cf7-550">テーブル PurchLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-550">Table PurchLine.setPriceDisc</span></span>|
|<span data-ttu-id="e2cf7-551">テーブル RouteVersion.selectRouteVersion</span><span class="sxs-lookup"><span data-stu-id="e2cf7-551">Table RouteVersion.selectRouteVersion</span></span>|
|<span data-ttu-id="e2cf7-552">テーブル SalesLine.checkItemId</span><span class="sxs-lookup"><span data-stu-id="e2cf7-552">Table SalesLine.checkItemId</span></span>|
|<span data-ttu-id="e2cf7-553">テーブル SalesLine.getSourcingFields</span><span class="sxs-lookup"><span data-stu-id="e2cf7-553">Table SalesLine.getSourcingFields</span></span>|
|<span data-ttu-id="e2cf7-554">テーブル SalesLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-554">Table SalesLine.setPriceAgreement</span></span>|
|<span data-ttu-id="e2cf7-555">テーブル SalesLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-555">Table SalesLine.setPriceDisc</span></span>|
|<span data-ttu-id="e2cf7-556">テーブル SalesLine.setSourcingFields</span><span class="sxs-lookup"><span data-stu-id="e2cf7-556">Table SalesLine.setSourcingFields</span></span>|
|<span data-ttu-id="e2cf7-557">テーブル SalesQuotationLine.IsCategoryBased</span><span class="sxs-lookup"><span data-stu-id="e2cf7-557">Table SalesQuotationLine.IsCategoryBased</span></span>|
|<span data-ttu-id="e2cf7-558">テーブル SalesQuotationLine.mcrCreateFromTmpFrmVirtualFromContract</span><span class="sxs-lookup"><span data-stu-id="e2cf7-558">Table SalesQuotationLine.mcrCreateFromTmpFrmVirtualFromContract</span></span>|
|<span data-ttu-id="e2cf7-559">テーブル SalesQuotationLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-559">Table SalesQuotationLine.setPriceAgreement</span></span>|
|<span data-ttu-id="e2cf7-560">テーブル SalesQuotationLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="e2cf7-560">Table SalesQuotationLine.setPriceDisc</span></span>|
|<span data-ttu-id="e2cf7-561">テーブル Salesline.splitReturnLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-561">Table Salesline.splitReturnLine</span></span>|
|<span data-ttu-id="e2cf7-562">テーブル SuppItemCreate.createLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-562">Table SuppItemCreate.createLine</span></span>|
|<span data-ttu-id="e2cf7-563">テーブル TmpInventTransMark.packTmpMark</span><span class="sxs-lookup"><span data-stu-id="e2cf7-563">Table TmpInventTransMark.packTmpMark</span></span>|
|<span data-ttu-id="e2cf7-564">テーブル VendInvoiceMatchingLine.initFromPurchLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-564">Table VendInvoiceMatchingLine.initFromPurchLine</span></span>|
|<span data-ttu-id="e2cf7-565">テーブル VendTable.updateOnHold</span><span class="sxs-lookup"><span data-stu-id="e2cf7-565">Table VendTable.updateOnHold</span></span>|
|<span data-ttu-id="e2cf7-566">テーブル WHSInvent.checkNonPhysicalDims</span><span class="sxs-lookup"><span data-stu-id="e2cf7-566">Table WHSInvent.checkNonPhysicalDims</span></span>|
|<span data-ttu-id="e2cf7-567">テーブル WHSShipmentTable.consolidateShipments</span><span class="sxs-lookup"><span data-stu-id="e2cf7-567">Table WHSShipmentTable.consolidateShipments</span></span>|
|<span data-ttu-id="e2cf7-568">テーブル WHSShipmentTable.transferShipment</span><span class="sxs-lookup"><span data-stu-id="e2cf7-568">Table WHSShipmentTable.transferShipment</span></span>|
|<span data-ttu-id="e2cf7-569">テーブル WHSTmpPackingLine.addTmpPackLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-569">Table WHSTmpPackingLine.addTmpPackLine</span></span>|
|<span data-ttu-id="e2cf7-570">テーブル salesLine.initFromProjTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-570">Table salesLine.initFromProjTable</span></span>|
|<span data-ttu-id="e2cf7-571">テーブル smmBusRelTable.updateReferences</span><span class="sxs-lookup"><span data-stu-id="e2cf7-571">Table smmBusRelTable.updateReferences</span></span>|
|<span data-ttu-id="e2cf7-572">テーブル smmLeadTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-572">Table smmLeadTable</span></span>|
|<span data-ttu-id="e2cf7-573">テーブル smmOpportunityTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-573">Table smmOpportunityTable</span></span>|


## <a name="maps-enabled-for-extensibility"></a><span data-ttu-id="e2cf7-574">拡張性に対して使用可能なマップ</span><span class="sxs-lookup"><span data-stu-id="e2cf7-574">Maps enabled for extensibility</span></span>

<span data-ttu-id="e2cf7-575">拡張機能によるフィールドとメソッドの追加を可能にするマップ実装に対して、新しいパターンが導入されました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-575">New patterns have been introduced for maps implementation that will allow you to add fields and methods by extensions.</span></span> <span data-ttu-id="e2cf7-576">これの実行方法の詳細は、インターフェイスとして使用されるマップが含まれるドキュメントとバージョン管理実装のためのドキュメントの両方にあります。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-576">Details on how this is done is available in the documentation both with maps that are used as interfaces and for versioning implementations.</span></span>

<span data-ttu-id="e2cf7-577">次の表に、拡張性を有効にするために変更が適用されたマップとその関連テーブルを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-577">The following table lists the maps and related tables where changes have been applied for enabling extensibility.</span></span>

| <span data-ttu-id="e2cf7-578">マップ</span><span class="sxs-lookup"><span data-stu-id="e2cf7-578">Maps</span></span> |
| -------------------|
|<span data-ttu-id="e2cf7-579">CustVendSettlement</span><span class="sxs-lookup"><span data-stu-id="e2cf7-579">CustVendSettlement</span></span>|
|<span data-ttu-id="e2cf7-580">JmgStampTransMap</span><span class="sxs-lookup"><span data-stu-id="e2cf7-580">JmgStampTransMap</span></span>|
|<span data-ttu-id="e2cf7-581">PriceDiscResultFields</span><span class="sxs-lookup"><span data-stu-id="e2cf7-581">PriceDiscResultFields</span></span>|
|<span data-ttu-id="e2cf7-582">SalesPurchLine</span><span class="sxs-lookup"><span data-stu-id="e2cf7-582">SalesPurchLine</span></span>|

## <a name="inventory-dimensions"></a><span data-ttu-id="e2cf7-583">在庫分析コード</span><span class="sxs-lookup"><span data-stu-id="e2cf7-583">Inventory dimensions</span></span>

<span data-ttu-id="e2cf7-584">今回のリリースでは、拡張機能による複数のシナリオのサポートをすべて対象とする在庫分析コードの追加のために、新しいモデルにマイナーな改良を加えました。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-584">This release made minor improvements to the new model for adding inventory dimensions, all targeted at supporting more scenarios through extensions.</span></span> 

| <span data-ttu-id="e2cf7-585">変更</span><span class="sxs-lookup"><span data-stu-id="e2cf7-585">Change</span></span> |
| -------------|
|<span data-ttu-id="e2cf7-586">BOM 階層はコンフィギュレーション分析コードとのみ連携します</span><span class="sxs-lookup"><span data-stu-id="e2cf7-586">BOM hierarchy works only with the config dimension</span></span>|
|<span data-ttu-id="e2cf7-587">フォーム BOMDesigner は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-587">Form BOMDesigner should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-588">フォーム EcoResProductSearchLookup は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-588">Form EcoResProductSearchLookup should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-589">フォーム FactureJournal_RU は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-589">Form FactureJournal_RU should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-590">フォーム InventDimParmFixed.InventDimensionXXFlag.Style は正しくありません</span><span class="sxs-lookup"><span data-stu-id="e2cf7-590">Form InventDimParmFixed.InventDimensionXXFlag.Style is incorrect</span></span>|
|<span data-ttu-id="e2cf7-591">フォーム InventItemOrderSetup は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-591">Form InventItemOrderSetup should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-592">フォーム InventTransferParmPick は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-592">Form InventTransferParmPick should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-593">フォーム InventTransferReleaseOrderPicking は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-593">Form InventTransferReleaseOrderPicking should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-594">フォーム KanbanCreateScheduled は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-594">Form KanbanCreateScheduled should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-595">フォーム KanbanJobPickingListPart は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-595">Form KanbanJobPickingListPart should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-596">フォーム KanbanRules は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-596">Form KanbanRules should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-597">フォーム LeanPeggingTree は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-597">Form LeanPeggingTree should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-598">フォーム MCRItemDisplay は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-598">Form MCRItemDisplay should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-599">フォーム MCRPriceDiscGroupItem は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-599">Form MCRPriceDiscGroupItem should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-600">フォーム PlanActivityServiceWizard は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-600">Form PlanActivityServiceWizard should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-601">フォーム ProdBOMVendor は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-601">Form ProdBOMVendor should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-602">フォーム PurchAgreementGenerateReleaseOrder は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-602">Form PurchAgreementGenerateReleaseOrder should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-603">フォーム PurchAgreementHistory は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-603">Form PurchAgreementHistory should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-604">フォーム PurchComplementaryInvoice は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-604">Form PurchComplementaryInvoice should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-605">フォーム PurchRFQCompareLineDimensions は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-605">Form PurchRFQCompareLineDimensions should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-606">フォーム PurchTable.TrackingDimesions のスペルが正しくありません</span><span class="sxs-lookup"><span data-stu-id="e2cf7-606">Form PurchTable.TrackingDimesions has incorrect spelling</span></span>|
|<span data-ttu-id="e2cf7-607">フォーム PurchVendorPortalAllResponse は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-607">Form PurchVendorPortalAllResponse should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-608">フォーム PurchVendorPortalConfirmedOrders は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-608">Form PurchVendorPortalConfirmedOrders should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-609">フォーム PurchVendorPortalOriginalOrder は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-609">Form PurchVendorPortalOriginalOrder should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-610">フォーム PurchVendorPortalRequests は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-610">Form PurchVendorPortalRequests should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-611">フォーム PurchVendorPortalResponses は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-611">Form PurchVendorPortalResponses should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-612">フォーム ReqDemPlanEasyItemAllocator は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-612">Form ReqDemPlanEasyItemAllocator should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-613">フォーム ReqOutboundIntercompanyDemand は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-613">Form ReqOutboundIntercompanyDemand should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-614">フォーム ReqSupplyDemandScheduleFilters は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-614">Form ReqSupplyDemandScheduleFilters should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-615">フォーム RetailVariantLookup は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-615">Form RetailVariantLookup should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-616">フォーム RouteVersionFeasibility は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-616">Form RouteVersionFeasibility should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-617">フォーム SMAAgreementTable は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-617">Form SMAAgreementTable should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-618">フォーム SalesAgreementGenerateReleaseOrder は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-618">Form SalesAgreementGenerateReleaseOrder should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-619">フォーム SalesAgreementHistory は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-619">Form SalesAgreementHistory should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-620">フォーム SalesComplementaryInvoice は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-620">Form SalesComplementaryInvoice should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-621">フォーム SalesLineDeliveryDetails は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-621">Form SalesLineDeliveryDetails should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-622">フォーム SalesQuotationProjTable は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-622">Form SalesQuotationProjTable should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-623">フォーム SalesQuotationTable は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-623">Form SalesQuotationTable should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-624">フォーム SalesTable は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-624">Form SalesTable should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-625">フォーム TAMFundManagement は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-625">Form TAMFundManagement should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-626">フォーム TAMTradePromotions は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-626">Form TAMTradePromotions should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-627">フォーム VendEditInvoice は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-627">Form VendEditInvoice should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-628">フォーム VendJournalMatch_PackingSlip は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-628">Form VendJournalMatch_PackingSlip should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-629">フォーム WHSLoadPlanningWorkBench は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-629">Form WHSLoadPlanningWorkBench should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-630">フォーム WHSLoadPlanningWorkbench は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-630">Form WHSLoadPlanningWorkbench should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-631">フォーム WHSLoadTable は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-631">Form WHSLoadTable should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-632">フォーム WHSLoadTable は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-632">Form WHSLoadTable should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-633">フォーム WHSProdWaveTableManageBOMPool は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-633">Form WHSProdWaveTableManageBOMPool should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-634">フォーム WHSWorkTable は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-634">Form WHSWorkTable should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-635">フォーム WMSOrderTransUnPick は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-635">Form WMSOrderTransUnPick should use field group for showing dimensions</span></span>|
|<span data-ttu-id="e2cf7-636">フォーム WMSPickingRegistration は、分析コードの表示にフィールド グループを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="e2cf7-636">Form WMSPickingRegistration should use field group for showing dimensions</span></span> |
|<span data-ttu-id="e2cf7-637">レポート InventAging は追加の分析コードをサポートしません</span><span class="sxs-lookup"><span data-stu-id="e2cf7-637">Report InventAging does not support extra dimensions</span></span>|
|<span data-ttu-id="e2cf7-638">テーブル EcoResProductVariantStaging.StagingIdx は、追加の分析コード フィールドを必要とします</span><span class="sxs-lookup"><span data-stu-id="e2cf7-638">Table EcoResProductVariantStaging.StagingIdx need extra dimension fields</span></span>|

## <a name="other-changes"></a><span data-ttu-id="e2cf7-639">その他の変更</span><span class="sxs-lookup"><span data-stu-id="e2cf7-639">Other changes</span></span>

<span data-ttu-id="e2cf7-640">次の表に、拡張機能に対して行われた追加の変更を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="e2cf7-640">The following table lists additional changes that have been made for extensibility.</span></span>

| <span data-ttu-id="e2cf7-641">変更</span><span class="sxs-lookup"><span data-stu-id="e2cf7-641">Change</span></span> |
| -------------|
|<span data-ttu-id="e2cf7-642">フィルター インターフェイスの追加: form InventQualityOrderTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-642">Add filter interface: form InventQualityOrderTable</span></span>|
|<span data-ttu-id="e2cf7-643">住所管理: 新しい住所フィールドの追加</span><span class="sxs-lookup"><span data-stu-id="e2cf7-643">Address management: Adding new address fields</span></span>|
|<span data-ttu-id="e2cf7-644">AxMaps - TradePostalAddress - partyTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-644">AxMaps - TradePostalAddress - partyTable</span></span>|
|<span data-ttu-id="e2cf7-645">銀行トランザクション コメント - BankReconciliationDataInitializer</span><span class="sxs-lookup"><span data-stu-id="e2cf7-645">Bank Trans Comments - BankReconciliationDataInitializer</span></span>|
|<span data-ttu-id="e2cf7-646">取消ログ要件 - 販売配送残量の更新</span><span class="sxs-lookup"><span data-stu-id="e2cf7-646">Cancellation Log Requirements - Update Sales Deliver Remainder</span></span>|
|<span data-ttu-id="e2cf7-647">購買要求明細行から購買明細行にグループ分けするメカニズムの拡張</span><span class="sxs-lookup"><span data-stu-id="e2cf7-647">Extend the grouping mechanisme from purch req line to purch line</span></span>|
|<span data-ttu-id="e2cf7-648">購買要求明細行から購買明細行に分割するメカニズムの拡張</span><span class="sxs-lookup"><span data-stu-id="e2cf7-648">Extend the splitting mechanisme from purch req line to purch line</span></span>|
|<span data-ttu-id="e2cf7-649">在庫品目要求と共に複数の資金調達ソースを許可</span><span class="sxs-lookup"><span data-stu-id="e2cf7-649">Allow multiple funding sources in conjunction with item requirements</span></span>|
|<span data-ttu-id="e2cf7-650">為替レート プロバイダー フレームワークの実装</span><span class="sxs-lookup"><span data-stu-id="e2cf7-650">Implementing exchange rate provider framework</span></span>|
|<span data-ttu-id="e2cf7-651">すべての使用で PriceDiscPartyCodeType を拡張可能にする</span><span class="sxs-lookup"><span data-stu-id="e2cf7-651">Make the PriceDiscPartyCodeType extensible in all usages</span></span>|
|<span data-ttu-id="e2cf7-652">すべての使用で PriceDiscProductCodeType を拡張可能にする</span><span class="sxs-lookup"><span data-stu-id="e2cf7-652">Make the PriceDiscProductCodeType extensible in all usages</span></span>|
|<span data-ttu-id="e2cf7-653">テーブル RetailChannelTable には ReplacementKey がありません</span><span class="sxs-lookup"><span data-stu-id="e2cf7-653">Table RetailChannelTable does not have ReplacementKey</span></span>|
|<span data-ttu-id="e2cf7-654">テーブル RetailSeasonTable CreateRecIdIndex True</span><span class="sxs-lookup"><span data-stu-id="e2cf7-654">Table RetailSeasonTable CreateRecIdIndex True</span></span>|
|<span data-ttu-id="e2cf7-655">インデックスの変更: テーブル InventTestAssociationTable</span><span class="sxs-lookup"><span data-stu-id="e2cf7-655">Modify index: table InventTestAssociationTable</span></span>|
|<span data-ttu-id="e2cf7-656">パブリックに切り替えられたエンティティ UnitOfMeasureEntity</span><span class="sxs-lookup"><span data-stu-id="e2cf7-656">Entity UnitOfMeasureEntity switched to public</span></span>|
|<span data-ttu-id="e2cf7-657">パブリックに切り替えられたエンティティ UnitOfMeasureTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="e2cf7-657">Entity UnitOfMeasureTranslationEntity switched to public</span></span>|

