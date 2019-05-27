---
title: Finance and Operations, Enterprise Edition 7.3 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations、Enterprise edition 7.3 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: c88d18538f9c92fd55af4f772fe26fe13ac7a04b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537498"
---
# <a name="extensibility-changes-in-finance-and-operations-enterprise-edition-73"></a><span data-ttu-id="0bbb6-103">Finance and Operations, Enterprise Edition 7.3 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="0bbb6-103">Extensibility changes in Finance and Operations, Enterprise edition 7.3</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bbb6-104">このトピックは、Dynamics 365 for Finance and Operations、Enterprise edition 7.3 でリリースされた拡張機能を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-104">This topic lists the extensibility features that were released in Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span> <span data-ttu-id="0bbb6-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="soft-sealed-application-models"></a><span data-ttu-id="0bbb6-106">ソフト シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="0bbb6-106">Soft-sealed application models</span></span>

<span data-ttu-id="0bbb6-107">このリリースは、すべてのモデルがハードシールになる前の最後のリリースとなり、このためのすべてのアプリケーション モデルはソフトシールされています。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-107">This release marks the last release before all models will become hard-sealed, and as a step toward this all application models are now soft-sealed.</span></span> <span data-ttu-id="0bbb6-108">ソフト シールされたモデルでもオーバーレイヤーされたコードを作成できますが、オーバーレイヤーされたコードをコンパイルするときに警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-108">Soft-sealed models still allow for making overlayered code, but warnings will be generated when you compile the overlayered code.</span></span> 

> [!NOTE]
> <span data-ttu-id="0bbb6-109">コードはオーバーレイすることができますが、推奨される方法は拡張です。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-109">You can still overlayer code, but extension is the recommended approach.</span></span>

<span data-ttu-id="0bbb6-110">次のテーブルに、今回のリリースで現在ソフト シールされているモデルの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-110">The following table includes a list of the models that are soft-sealed with this release.</span></span>

| <span data-ttu-id="0bbb6-111">モジュール</span><span class="sxs-lookup"><span data-stu-id="0bbb6-111">Module</span></span> | <span data-ttu-id="0bbb6-112">モデル</span><span class="sxs-lookup"><span data-stu-id="0bbb6-112">Model</span></span>         |
| --------------- |-------------|
|<span data-ttu-id="0bbb6-113">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="0bbb6-113">ApplicationCommon</span></span> | <span data-ttu-id="0bbb6-114">ApplicationCommon</span><span class="sxs-lookup"><span data-stu-id="0bbb6-114">ApplicationCommon</span></span> |
|<span data-ttu-id="0bbb6-115">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-115">ApplicationSuite</span></span> | <span data-ttu-id="0bbb6-116">Electronic Reporting Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-116">Electronic Reporting Application Suite Integration</span></span> |
|<span data-ttu-id="0bbb6-117">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-117">ApplicationSuite</span></span> | <span data-ttu-id="0bbb6-118">Foundation Upgrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-118">Foundation Upgrade</span></span> |
|<span data-ttu-id="0bbb6-119">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-119">ApplicationSuite</span></span> | <span data-ttu-id="0bbb6-120">Foundation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-120">Foundation</span></span> |
|<span data-ttu-id="0bbb6-121">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-121">ApplicationSuite</span></span> | <span data-ttu-id="0bbb6-122">SCMControls</span><span class="sxs-lookup"><span data-stu-id="0bbb6-122">SCMControls</span></span> |
|<span data-ttu-id="0bbb6-123">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-123">ApplicationSuite</span></span> | <span data-ttu-id="0bbb6-124">Tax Books Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-124">Tax Books Application Suite Integration</span></span> |
|<span data-ttu-id="0bbb6-125">ApplicationSuite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-125">ApplicationSuite</span></span> | <span data-ttu-id="0bbb6-126">Tax Engine Application Suite Integration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-126">Tax Engine Application Suite Integration</span></span> |
|<span data-ttu-id="0bbb6-127">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-127">CaseManagement</span></span> | <span data-ttu-id="0bbb6-128">CaseManagement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-128">CaseManagement</span></span> |
|<span data-ttu-id="0bbb6-129">Currency</span><span class="sxs-lookup"><span data-stu-id="0bbb6-129">Currency</span></span> | <span data-ttu-id="0bbb6-130">Currency</span><span class="sxs-lookup"><span data-stu-id="0bbb6-130">Currency</span></span> |
|<span data-ttu-id="0bbb6-131">DataImpExpApplication</span><span class="sxs-lookup"><span data-stu-id="0bbb6-131">DataImpExpApplication</span></span> | <span data-ttu-id="0bbb6-132">DataImpExpApplication</span><span class="sxs-lookup"><span data-stu-id="0bbb6-132">DataImpExpApplication</span></span> |
|<span data-ttu-id="0bbb6-133">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-133">DataUpgrade</span></span> | <span data-ttu-id="0bbb6-134">DataUpgrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-134">DataUpgrade</span></span> |
|<span data-ttu-id="0bbb6-135">Directory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-135">Directory</span></span> | <span data-ttu-id="0bbb6-136">Directory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-136">Directory</span></span> |
|<span data-ttu-id="0bbb6-137">Directory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-137">Directory</span></span> | <span data-ttu-id="0bbb6-138">SecurityReports</span><span class="sxs-lookup"><span data-stu-id="0bbb6-138">SecurityReports</span></span> |
|<span data-ttu-id="0bbb6-139">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="0bbb6-139">GeneralLedger</span></span> | <span data-ttu-id="0bbb6-140">GeneralLedger</span><span class="sxs-lookup"><span data-stu-id="0bbb6-140">GeneralLedger</span></span> |
|<span data-ttu-id="0bbb6-141">Ledger</span><span class="sxs-lookup"><span data-stu-id="0bbb6-141">Ledger</span></span> | <span data-ttu-id="0bbb6-142">Ledger</span><span class="sxs-lookup"><span data-stu-id="0bbb6-142">Ledger</span></span> |
|<span data-ttu-id="0bbb6-143">PersonnelManagement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-143">PersonnelManagement</span></span> | <span data-ttu-id="0bbb6-144">PersonnelManagement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-144">PersonnelManagement</span></span> |
|<span data-ttu-id="0bbb6-145">Retail</span><span class="sxs-lookup"><span data-stu-id="0bbb6-145">Retail</span></span> | <span data-ttu-id="0bbb6-146">Retail</span><span class="sxs-lookup"><span data-stu-id="0bbb6-146">Retail</span></span> |
|<span data-ttu-id="0bbb6-147">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-147">SourceDocumentation</span></span> | <span data-ttu-id="0bbb6-148">SourceDocumentation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-148">SourceDocumentation</span></span> |
|<span data-ttu-id="0bbb6-149">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-149">SourceDocumentationTypes</span></span> | <span data-ttu-id="0bbb6-150">SourceDocumentationTypes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-150">SourceDocumentationTypes</span></span> |
|<span data-ttu-id="0bbb6-151">補助元帳</span><span class="sxs-lookup"><span data-stu-id="0bbb6-151">Subledger</span></span> | <span data-ttu-id="0bbb6-152">補助元帳</span><span class="sxs-lookup"><span data-stu-id="0bbb6-152">Subledger</span></span> |
|<span data-ttu-id="0bbb6-153">税申告</span><span class="sxs-lookup"><span data-stu-id="0bbb6-153">Tax</span></span> | <span data-ttu-id="0bbb6-154">税申告</span><span class="sxs-lookup"><span data-stu-id="0bbb6-154">Tax</span></span> |

## <a name="hard-sealed-application-models"></a><span data-ttu-id="0bbb6-155">ハード シールされたアプリケーション モデル</span><span class="sxs-lookup"><span data-stu-id="0bbb6-155">Hard-sealed application models</span></span>

<span data-ttu-id="0bbb6-156">このリリースでは、ほとんどすべてのアプリケーションの主要なモデルはハード シールされています。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-156">With this release, almost all application core models have been hard-sealed.</span></span> <span data-ttu-id="0bbb6-157">これらのモデルのオーバーレイ コードは、現在コンパイル エラーを発生します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-157">Overlayered code in these models will now produce compilation errors.</span></span> <span data-ttu-id="0bbb6-158">カスタマイズ モデルは拡張機能によってのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-158">The only supported customization model is through extensions.</span></span> <span data-ttu-id="0bbb6-159">拡張機能によってこれらのモデルをカスタマイズできない場合は、標準のアプリケーションを変更して拡張機能を有効にするよう、Microsoft に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-159">If you cannot customize these models through extension, then you will have to make a request to Microsoft to enable extensibility by changing the standard application.</span></span>

<span data-ttu-id="0bbb6-160">次の表に、今回のリリースで現在ハード シールされているモデルの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-160">TThe following table includes a list of models that are now hard-sealed with this release.</span></span>

| <span data-ttu-id="0bbb6-161">モジュール</span><span class="sxs-lookup"><span data-stu-id="0bbb6-161">Module</span></span>| <span data-ttu-id="0bbb6-162">モデル</span><span class="sxs-lookup"><span data-stu-id="0bbb6-162">Model</span></span>         |
| --------------- |-------------|
| <span data-ttu-id="0bbb6-163">AccountsPayableMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-163">AccountsPayableMobile</span></span> | <span data-ttu-id="0bbb6-164">AccountsPayableMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-164">AccountsPayableMobile</span></span> |
| <span data-ttu-id="0bbb6-165">ApplicationWorkspaces</span><span class="sxs-lookup"><span data-stu-id="0bbb6-165">ApplicationWorkspaces</span></span> | <span data-ttu-id="0bbb6-166">ApplicationWorkspaces</span><span class="sxs-lookup"><span data-stu-id="0bbb6-166">ApplicationWorkspaces</span></span> |
| <span data-ttu-id="0bbb6-167">BankTypes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-167">BankTypes</span></span> | <span data-ttu-id="0bbb6-168">BankTypes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-168">BankTypes</span></span> |
| <span data-ttu-id="0bbb6-169">BusinessProcess</span><span class="sxs-lookup"><span data-stu-id="0bbb6-169">BusinessProcess</span></span> | <span data-ttu-id="0bbb6-170">BusinessProcess</span><span class="sxs-lookup"><span data-stu-id="0bbb6-170">BusinessProcess</span></span> |
| <span data-ttu-id="0bbb6-171">カレンダー</span><span class="sxs-lookup"><span data-stu-id="0bbb6-171">Calendar</span></span> | <span data-ttu-id="0bbb6-172">カレンダー</span><span class="sxs-lookup"><span data-stu-id="0bbb6-172">Calendar</span></span> |
| <span data-ttu-id="0bbb6-173">ContactPerson</span><span class="sxs-lookup"><span data-stu-id="0bbb6-173">ContactPerson</span></span> | <span data-ttu-id="0bbb6-174">ContactPerson</span><span class="sxs-lookup"><span data-stu-id="0bbb6-174">ContactPerson</span></span> |
| <span data-ttu-id="0bbb6-175">CostAccounting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-175">CostAccounting</span></span> | <span data-ttu-id="0bbb6-176">CostAccounting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-176">CostAccounting</span></span> |
| <span data-ttu-id="0bbb6-177">CostAccountingAX</span><span class="sxs-lookup"><span data-stu-id="0bbb6-177">CostAccountingAX</span></span> | <span data-ttu-id="0bbb6-178">CostAccountingAX</span><span class="sxs-lookup"><span data-stu-id="0bbb6-178">CostAccountingAX</span></span> |
| <span data-ttu-id="0bbb6-179">分析コード</span><span class="sxs-lookup"><span data-stu-id="0bbb6-179">Dimensions</span></span> | <span data-ttu-id="0bbb6-180">分析コード</span><span class="sxs-lookup"><span data-stu-id="0bbb6-180">Dimensions</span></span> |
| <span data-ttu-id="0bbb6-181">DirectoryUpgrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-181">DirectoryUpgrade</span></span> | <span data-ttu-id="0bbb6-182">DirectoryUpgrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-182">DirectoryUpgrade</span></span> |
| <span data-ttu-id="0bbb6-183">DOM</span><span class="sxs-lookup"><span data-stu-id="0bbb6-183">DOM</span></span> | <span data-ttu-id="0bbb6-184">DOM</span><span class="sxs-lookup"><span data-stu-id="0bbb6-184">DOM</span></span> |
| <span data-ttu-id="0bbb6-185">ElectronicReporting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-185">ElectronicReporting</span></span> | <span data-ttu-id="0bbb6-186">ElectronicReporting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-186">ElectronicReporting</span></span> |
| <span data-ttu-id="0bbb6-187">ElectronicReportingAppSuiteIntegration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-187">ElectronicReportingAppSuiteIntegration</span></span> | <span data-ttu-id="0bbb6-188">ElectronicReportingAppSuiteIntegration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-188">ElectronicReportingAppSuiteIntegration</span></span> |
| <span data-ttu-id="0bbb6-189">ElectronicReportingCore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-189">ElectronicReportingCore</span></span> | <span data-ttu-id="0bbb6-190">ElectronicReportingCore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-190">ElectronicReportingCore</span></span> |
| <span data-ttu-id="0bbb6-191">ElectronicReportingDotNetUtils</span><span class="sxs-lookup"><span data-stu-id="0bbb6-191">ElectronicReportingDotNetUtils</span></span> | <span data-ttu-id="0bbb6-192">ElectronicReportingDotNetUtils</span><span class="sxs-lookup"><span data-stu-id="0bbb6-192">ElectronicReportingDotNetUtils</span></span> |
| <span data-ttu-id="0bbb6-193">ElectronicReportingForAx</span><span class="sxs-lookup"><span data-stu-id="0bbb6-193">ElectronicReportingForAx</span></span> | <span data-ttu-id="0bbb6-194">ElectronicReportingForAx</span><span class="sxs-lookup"><span data-stu-id="0bbb6-194">ElectronicReportingForAx</span></span> |
| <span data-ttu-id="0bbb6-195">ElectronicReportingMapping</span><span class="sxs-lookup"><span data-stu-id="0bbb6-195">ElectronicReportingMapping</span></span> | <span data-ttu-id="0bbb6-196">ElectronicReportingMapping</span><span class="sxs-lookup"><span data-stu-id="0bbb6-196">ElectronicReportingMapping</span></span> |
| <span data-ttu-id="0bbb6-197">ExpenseMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-197">ExpenseMobile</span></span> | <span data-ttu-id="0bbb6-198">ExpenseMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-198">ExpenseMobile</span></span> |
| <span data-ttu-id="0bbb6-199">FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-199">FinancialReporting</span></span> | <span data-ttu-id="0bbb6-200">FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-200">FinancialReporting</span></span> |
| <span data-ttu-id="0bbb6-201">FinancialReportingEntityStore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-201">FinancialReportingEntityStore</span></span> | <span data-ttu-id="0bbb6-202">FinancialReportingEntityStore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-202">FinancialReportingEntityStore</span></span> |
| <span data-ttu-id="0bbb6-203">FiscalBooks</span><span class="sxs-lookup"><span data-stu-id="0bbb6-203">FiscalBooks</span></span> | <span data-ttu-id="0bbb6-204">FiscalBooks</span><span class="sxs-lookup"><span data-stu-id="0bbb6-204">FiscalBooks</span></span> |
| <span data-ttu-id="0bbb6-205">InventoryDimensionConversion</span><span class="sxs-lookup"><span data-stu-id="0bbb6-205">InventoryDimensionConversion</span></span> | <span data-ttu-id="0bbb6-206">InventoryDimensionConversion</span><span class="sxs-lookup"><span data-stu-id="0bbb6-206">InventoryDimensionConversion</span></span> |
| <span data-ttu-id="0bbb6-207">測定</span><span class="sxs-lookup"><span data-stu-id="0bbb6-207">Measurement</span></span> | <span data-ttu-id="0bbb6-208">測定</span><span class="sxs-lookup"><span data-stu-id="0bbb6-208">Measurement</span></span> |
| <span data-ttu-id="0bbb6-209">PaymentPredictor</span><span class="sxs-lookup"><span data-stu-id="0bbb6-209">PaymentPredictor</span></span> | <span data-ttu-id="0bbb6-210">PaymentPredictor</span><span class="sxs-lookup"><span data-stu-id="0bbb6-210">PaymentPredictor</span></span> |
| <span data-ttu-id="0bbb6-211">PerformanceTool</span><span class="sxs-lookup"><span data-stu-id="0bbb6-211">PerformanceTool</span></span> | <span data-ttu-id="0bbb6-212">PerformanceTool</span><span class="sxs-lookup"><span data-stu-id="0bbb6-212">PerformanceTool</span></span> |
| <span data-ttu-id="0bbb6-213">担当者</span><span class="sxs-lookup"><span data-stu-id="0bbb6-213">Personnel</span></span> | <span data-ttu-id="0bbb6-214">担当者</span><span class="sxs-lookup"><span data-stu-id="0bbb6-214">Personnel</span></span> |
| <span data-ttu-id="0bbb6-215">PersonnelCore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-215">PersonnelCore</span></span> | <span data-ttu-id="0bbb6-216">PersonnelCore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-216">PersonnelCore</span></span> |
| <span data-ttu-id="0bbb6-217">PersonnelMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-217">PersonnelMobile</span></span> | <span data-ttu-id="0bbb6-218">PersonnelMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-218">PersonnelMobile</span></span> |
| <span data-ttu-id="0bbb6-219">PersonnelUpgrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-219">PersonnelUpgrade</span></span> | <span data-ttu-id="0bbb6-220">PersonnelUpgrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-220">PersonnelUpgrade</span></span> |
| <span data-ttu-id="0bbb6-221">保険証書</span><span class="sxs-lookup"><span data-stu-id="0bbb6-221">Policy</span></span> | <span data-ttu-id="0bbb6-222">保険証書</span><span class="sxs-lookup"><span data-stu-id="0bbb6-222">Policy</span></span> |
| <span data-ttu-id="0bbb6-223">Project</span><span class="sxs-lookup"><span data-stu-id="0bbb6-223">Project</span></span> | <span data-ttu-id="0bbb6-224">Project</span><span class="sxs-lookup"><span data-stu-id="0bbb6-224">Project</span></span> |
| <span data-ttu-id="0bbb6-225">ProjectMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-225">ProjectMobile</span></span> | <span data-ttu-id="0bbb6-226">ProjectMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-226">ProjectMobile</span></span> |
| <span data-ttu-id="0bbb6-227">RegulatoryServices</span><span class="sxs-lookup"><span data-stu-id="0bbb6-227">RegulatoryServices</span></span> | <span data-ttu-id="0bbb6-228">RegulatoryServices</span><span class="sxs-lookup"><span data-stu-id="0bbb6-228">RegulatoryServices</span></span> |
| <span data-ttu-id="0bbb6-229">SCMMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-229">SCMMobile</span></span> | <span data-ttu-id="0bbb6-230">SCMMobile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-230">SCMMobile</span></span> |
| <span data-ttu-id="0bbb6-231">SelfHealing</span><span class="sxs-lookup"><span data-stu-id="0bbb6-231">SelfHealing</span></span> | <span data-ttu-id="0bbb6-232">SelfHealing</span><span class="sxs-lookup"><span data-stu-id="0bbb6-232">SelfHealing</span></span> |
| <span data-ttu-id="0bbb6-233">SelfHealingRules</span><span class="sxs-lookup"><span data-stu-id="0bbb6-233">SelfHealingRules</span></span> | <span data-ttu-id="0bbb6-234">SelfHealingRules</span><span class="sxs-lookup"><span data-stu-id="0bbb6-234">SelfHealingRules</span></span> |
| <span data-ttu-id="0bbb6-235">SystemHealth</span><span class="sxs-lookup"><span data-stu-id="0bbb6-235">SystemHealth</span></span> | <span data-ttu-id="0bbb6-236">SystemHealth</span><span class="sxs-lookup"><span data-stu-id="0bbb6-236">SystemHealth</span></span> |
| <span data-ttu-id="0bbb6-237">TaxEngine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-237">TaxEngine</span></span> | <span data-ttu-id="0bbb6-238">TaxEngine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-238">TaxEngine</span></span> |
| <span data-ttu-id="0bbb6-239">UnitOfMeasure</span><span class="sxs-lookup"><span data-stu-id="0bbb6-239">UnitOfMeasure</span></span> | <span data-ttu-id="0bbb6-240">UnitOfMeasure</span><span class="sxs-lookup"><span data-stu-id="0bbb6-240">UnitOfMeasure</span></span> |
| <span data-ttu-id="0bbb6-241">WMSAdvancedMigration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-241">WMSAdvancedMigration</span></span> | <span data-ttu-id="0bbb6-242">WMSAdvancedMigration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-242">WMSAdvancedMigration</span></span> |

## <a name="enumerations-that-have-been-made-extensible"></a><span data-ttu-id="0bbb6-243">拡張可能になった列挙型</span><span class="sxs-lookup"><span data-stu-id="0bbb6-243">Enumerations that have been made extensible</span></span>

<span data-ttu-id="0bbb6-244">列挙の拡張をサポートするために以下の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-244">The following changes were made to support extending enumerations:</span></span>
- <span data-ttu-id="0bbb6-245">標準アプリケーションの多くの列挙が拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-245">Many enumerations in the standard application have been made extensible.</span></span> <span data-ttu-id="0bbb6-246">列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-246">An enumeration is made extensible by setting two properties on the enumeration.</span></span> <span data-ttu-id="0bbb6-247">**IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-247">The **IsExtensible** property is set to **Yes**, and the **UseEnumValue** property is set to **No**.</span></span> 
- <span data-ttu-id="0bbb6-248">一部の列挙型は状態を表します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-248">Some enumerations represent state.</span></span> <span data-ttu-id="0bbb6-249">拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-249">New façade methods have been added to help enable adding enumeration values by extension.</span></span> <span data-ttu-id="0bbb6-250">列挙型を拡張する方法については、「[列挙値の追加](add-enum-value.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-250">For information about how to extend an enumeration, see [Add an enum value](add-enum-value.md).</span></span>
- <span data-ttu-id="0bbb6-251">拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-251">Some application code that uses enumerations was changed to support extensibility.</span></span> <span data-ttu-id="0bbb6-252">一般的な変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-252">Common changes include:</span></span>
    + <span data-ttu-id="0bbb6-253">ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-253">Removing **throw** exception statements in the default case of a switch to allow post-event subscription.</span></span>
    + <span data-ttu-id="0bbb6-254">拡張機能の **SysExtension** サポートの追加。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-254">Adding **SysExtension** support for extension.</span></span>
    + <span data-ttu-id="0bbb6-255">明示的なデリゲートを追加します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-255">Adding explicit delegates.</span></span>

| <span data-ttu-id="0bbb6-256">列挙</span><span class="sxs-lookup"><span data-stu-id="0bbb6-256">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="0bbb6-257">AssetCalendarYearType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-257">AssetCalendarYearType</span></span>|
|<span data-ttu-id="0bbb6-258">AssetDepreciationConvention</span><span class="sxs-lookup"><span data-stu-id="0bbb6-258">AssetDepreciationConvention</span></span>|
|<span data-ttu-id="0bbb6-259">AssetDepreciationMethod</span><span class="sxs-lookup"><span data-stu-id="0bbb6-259">AssetDepreciationMethod</span></span>|
|<span data-ttu-id="0bbb6-260">AssetPeriodMonth</span><span class="sxs-lookup"><span data-stu-id="0bbb6-260">AssetPeriodMonth</span></span>|
|<span data-ttu-id="0bbb6-261">AssetSoldScrap</span><span class="sxs-lookup"><span data-stu-id="0bbb6-261">AssetSoldScrap</span></span>|
|<span data-ttu-id="0bbb6-262">AssetStatusLVPFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-262">AssetStatusLVPFilter</span></span>|
|<span data-ttu-id="0bbb6-263">AssetTransType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-263">AssetTransType</span></span>|
|<span data-ttu-id="0bbb6-264">BaseDataProd</span><span class="sxs-lookup"><span data-stu-id="0bbb6-264">BaseDataProd</span></span>|
|<span data-ttu-id="0bbb6-265">BOMRouteVersionSelect</span><span class="sxs-lookup"><span data-stu-id="0bbb6-265">BOMRouteVersionSelect</span></span>|
|<span data-ttu-id="0bbb6-266">BudgetPlanGenerateSource</span><span class="sxs-lookup"><span data-stu-id="0bbb6-266">BudgetPlanGenerateSource</span></span>|
|<span data-ttu-id="0bbb6-267">BudgetPlanScenarioAccessLevel</span><span class="sxs-lookup"><span data-stu-id="0bbb6-267">BudgetPlanScenarioAccessLevel</span></span>|
|<span data-ttu-id="0bbb6-268">BudgetPlanScenarioAttribute</span><span class="sxs-lookup"><span data-stu-id="0bbb6-268">BudgetPlanScenarioAttribute</span></span>|
|<span data-ttu-id="0bbb6-269">BudgetTransactionColumnType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-269">BudgetTransactionColumnType</span></span>|
|<span data-ttu-id="0bbb6-270">BusinessEvent_ActivityJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-270">BusinessEvent_ActivityJournal</span></span>|
|<span data-ttu-id="0bbb6-271">BusinessEvent_CustomerInvoice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-271">BusinessEvent_CustomerInvoice</span></span>|
|<span data-ttu-id="0bbb6-272">BusinessEventRelievingMethod</span><span class="sxs-lookup"><span data-stu-id="0bbb6-272">BusinessEventRelievingMethod</span></span>|
|<span data-ttu-id="0bbb6-273">CollabSiteEntityType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-273">CollabSiteEntityType</span></span>|
|<span data-ttu-id="0bbb6-274">CollabSiteSharePointType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-274">CollabSiteSharePointType</span></span>|
|<span data-ttu-id="0bbb6-275">CostSheetNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-275">CostSheetNodeType</span></span>|
|<span data-ttu-id="0bbb6-276">CreditCardAddEdit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-276">CreditCardAddEdit</span></span>|
|<span data-ttu-id="0bbb6-277">CreditCardApprovalType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-277">CreditCardApprovalType</span></span>|
|<span data-ttu-id="0bbb6-278">CreditCardDupCheckResult</span><span class="sxs-lookup"><span data-stu-id="0bbb6-278">CreditCardDupCheckResult</span></span>|
|<span data-ttu-id="0bbb6-279">CreditCardPaymType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-279">CreditCardPaymType</span></span>|
|<span data-ttu-id="0bbb6-280">CustAssessment</span><span class="sxs-lookup"><span data-stu-id="0bbb6-280">CustAssessment</span></span>|
|<span data-ttu-id="0bbb6-281">CustCollectionLetterCode</span><span class="sxs-lookup"><span data-stu-id="0bbb6-281">CustCollectionLetterCode</span></span>|
|<span data-ttu-id="0bbb6-282">CustInterestFeeType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-282">CustInterestFeeType</span></span>|
|<span data-ttu-id="0bbb6-283">CustomerTransactionType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-283">CustomerTransactionType</span></span>|
|<span data-ttu-id="0bbb6-284">CustSettlementPriorityAttribute</span><span class="sxs-lookup"><span data-stu-id="0bbb6-284">CustSettlementPriorityAttribute</span></span>|
|<span data-ttu-id="0bbb6-285">CustSettlementTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-285">CustSettlementTrans</span></span>|
|<span data-ttu-id="0bbb6-286">CustTransRefType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-286">CustTransRefType</span></span>|
|<span data-ttu-id="0bbb6-287">CustVendDisputeStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-287">CustVendDisputeStatus</span></span>|
|<span data-ttu-id="0bbb6-288">CustVendForeignExchRefIndicator_US</span><span class="sxs-lookup"><span data-stu-id="0bbb6-288">CustVendForeignExchRefIndicator_US</span></span>|
|<span data-ttu-id="0bbb6-289">CustVendGatewayOperatorOFACIndicator_US</span><span class="sxs-lookup"><span data-stu-id="0bbb6-289">CustVendGatewayOperatorOFACIndicator_US</span></span>|
|<span data-ttu-id="0bbb6-290">CustVendorBlocked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-290">CustVendorBlocked</span></span>|
|<span data-ttu-id="0bbb6-291">CustVendOutPaymTrade</span><span class="sxs-lookup"><span data-stu-id="0bbb6-291">CustVendOutPaymTrade</span></span>|
|<span data-ttu-id="0bbb6-292">CustVendPaymStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-292">CustVendPaymStatus</span></span>|
|<span data-ttu-id="0bbb6-293">CustVendSecondaryOFACIndicator_US</span><span class="sxs-lookup"><span data-stu-id="0bbb6-293">CustVendSecondaryOFACIndicator_US</span></span>|
|<span data-ttu-id="0bbb6-294">DimensionCacheScope</span><span class="sxs-lookup"><span data-stu-id="0bbb6-294">DimensionCacheScope</span></span>|
|<span data-ttu-id="0bbb6-295">DirPartyRoleType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-295">DirPartyRoleType</span></span>|
|<span data-ttu-id="0bbb6-296">DirPartyRoleView</span><span class="sxs-lookup"><span data-stu-id="0bbb6-296">DirPartyRoleView</span></span>|
|<span data-ttu-id="0bbb6-297">DistributionProcess</span><span class="sxs-lookup"><span data-stu-id="0bbb6-297">DistributionProcess</span></span>|
|<span data-ttu-id="0bbb6-298">DistributionProcessingState</span><span class="sxs-lookup"><span data-stu-id="0bbb6-298">DistributionProcessingState</span></span>|
|<span data-ttu-id="0bbb6-299">DistributionStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-299">DistributionStatus</span></span>|
|<span data-ttu-id="0bbb6-300">EPProjUpdateSubProjStage</span><span class="sxs-lookup"><span data-stu-id="0bbb6-300">EPProjUpdateSubProjStage</span></span>|
|<span data-ttu-id="0bbb6-301">HcmPositionForecastStatusSelection</span><span class="sxs-lookup"><span data-stu-id="0bbb6-301">HcmPositionForecastStatusSelection</span></span>|
|<span data-ttu-id="0bbb6-302">JournalizingDefinitionLedgerEntryTypeId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-302">JournalizingDefinitionLedgerEntryTypeId</span></span>|
|<span data-ttu-id="0bbb6-303">LedgerBalanceExportFieldSeparator</span><span class="sxs-lookup"><span data-stu-id="0bbb6-303">LedgerBalanceExportFieldSeparator</span></span>|
|<span data-ttu-id="0bbb6-304">LedgerBalanceExportHeaders</span><span class="sxs-lookup"><span data-stu-id="0bbb6-304">LedgerBalanceExportHeaders</span></span>|
|<span data-ttu-id="0bbb6-305">LedgerBalanceExportHiddenFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-305">LedgerBalanceExportHiddenFields</span></span>|
|<span data-ttu-id="0bbb6-306">LedgerBalanceExportInvertSign</span><span class="sxs-lookup"><span data-stu-id="0bbb6-306">LedgerBalanceExportInvertSign</span></span>|
|<span data-ttu-id="0bbb6-307">LedgerBalanceExportSubcomponents</span><span class="sxs-lookup"><span data-stu-id="0bbb6-307">LedgerBalanceExportSubcomponents</span></span>|
|<span data-ttu-id="0bbb6-308">LedgerBalanceExportSubtotals</span><span class="sxs-lookup"><span data-stu-id="0bbb6-308">LedgerBalanceExportSubtotals</span></span>|
|<span data-ttu-id="0bbb6-309">LedgerColumnType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-309">LedgerColumnType</span></span>|
|<span data-ttu-id="0bbb6-310">LedgerConsDim</span><span class="sxs-lookup"><span data-stu-id="0bbb6-310">LedgerConsDim</span></span>|
|<span data-ttu-id="0bbb6-311">LedgerConsolidateAccountSource</span><span class="sxs-lookup"><span data-stu-id="0bbb6-311">LedgerConsolidateAccountSource</span></span>|
|<span data-ttu-id="0bbb6-312">LedgerDataExportFormat</span><span class="sxs-lookup"><span data-stu-id="0bbb6-312">LedgerDataExportFormat</span></span>|
|<span data-ttu-id="0bbb6-313">LedgerReconciliationStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-313">LedgerReconciliationStatus</span></span>|
|<span data-ttu-id="0bbb6-314">LedgerShowCurrency</span><span class="sxs-lookup"><span data-stu-id="0bbb6-314">LedgerShowCurrency</span></span>|
|<span data-ttu-id="0bbb6-315">LedgerSIEFileType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-315">LedgerSIEFileType</span></span>|
|<span data-ttu-id="0bbb6-316">LedgerTransactionType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-316">LedgerTransactionType</span></span>|
|<span data-ttu-id="0bbb6-317">LedgerTransEnigneBuildQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-317">LedgerTransEnigneBuildQuery</span></span>|
|<span data-ttu-id="0bbb6-318">LogisticsAddressElement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-318">LogisticsAddressElement</span></span>|
|<span data-ttu-id="0bbb6-319">LogisticsAddrZipCodeImportCountryRegion</span><span class="sxs-lookup"><span data-stu-id="0bbb6-319">LogisticsAddrZipCodeImportCountryRegion</span></span>|
|<span data-ttu-id="0bbb6-320">LogisticsLocationEntityType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-320">LogisticsLocationEntityType</span></span>|
|<span data-ttu-id="0bbb6-321">LogisticsLocationSelectSourceType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-321">LogisticsLocationSelectSourceType</span></span>|
|<span data-ttu-id="0bbb6-322">MCROrderEventType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-322">MCROrderEventType</span></span>|
|<span data-ttu-id="0bbb6-323">PaymManDocType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-323">PaymManDocType</span></span>|
|<span data-ttu-id="0bbb6-324">ProjAccountType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-324">ProjAccountType</span></span>|
|<span data-ttu-id="0bbb6-325">ProjAccountTypeCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-325">ProjAccountTypeCost</span></span>|
|<span data-ttu-id="0bbb6-326">ProjAccountTypeSales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-326">ProjAccountTypeSales</span></span>|
|<span data-ttu-id="0bbb6-327">ProjActualVsForecastCategory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-327">ProjActualVsForecastCategory</span></span>|
|<span data-ttu-id="0bbb6-328">ProjActualVsForecastValue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-328">ProjActualVsForecastValue</span></span>|
|<span data-ttu-id="0bbb6-329">ProjAlertType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-329">ProjAlertType</span></span>|
|<span data-ttu-id="0bbb6-330">ProjAssignConflictStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-330">ProjAssignConflictStatus</span></span>|
|<span data-ttu-id="0bbb6-331">ProjCategoryType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-331">ProjCategoryType</span></span>|
|<span data-ttu-id="0bbb6-332">ProjChoose</span><span class="sxs-lookup"><span data-stu-id="0bbb6-332">ProjChoose</span></span>|
|<span data-ttu-id="0bbb6-333">ProjContractType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-333">ProjContractType</span></span>|
|<span data-ttu-id="0bbb6-334">ProjCostSales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-334">ProjCostSales</span></span>|
|<span data-ttu-id="0bbb6-335">ProjDimensionStrType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-335">ProjDimensionStrType</span></span>|
|<span data-ttu-id="0bbb6-336">ProjectReportingAnalyticsWorkspaces</span><span class="sxs-lookup"><span data-stu-id="0bbb6-336">ProjectReportingAnalyticsWorkspaces</span></span>|
|<span data-ttu-id="0bbb6-337">ProjEstimateMethod</span><span class="sxs-lookup"><span data-stu-id="0bbb6-337">ProjEstimateMethod</span></span>|
|<span data-ttu-id="0bbb6-338">ProjExportToExcelDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-338">ProjExportToExcelDimension</span></span>|
|<span data-ttu-id="0bbb6-339">ProjFoundMethod</span><span class="sxs-lookup"><span data-stu-id="0bbb6-339">ProjFoundMethod</span></span>|
|<span data-ttu-id="0bbb6-340">ProjFunctionType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-340">ProjFunctionType</span></span>|
|<span data-ttu-id="0bbb6-341">ProjFundingRuleType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-341">ProjFundingRuleType</span></span>|
|<span data-ttu-id="0bbb6-342">ProjInvoiceFrequency</span><span class="sxs-lookup"><span data-stu-id="0bbb6-342">ProjInvoiceFrequency</span></span>|
|<span data-ttu-id="0bbb6-343">ProjInvoiceProposalsTransSelectionTypes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-343">ProjInvoiceProposalsTransSelectionTypes</span></span>|
|<span data-ttu-id="0bbb6-344">ProjLevelFilterOption</span><span class="sxs-lookup"><span data-stu-id="0bbb6-344">ProjLevelFilterOption</span></span>|
|<span data-ttu-id="0bbb6-345">ProjListLedgerTransType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-345">ProjListLedgerTransType</span></span>|
|<span data-ttu-id="0bbb6-346">ProjOrigin</span><span class="sxs-lookup"><span data-stu-id="0bbb6-346">ProjOrigin</span></span>|
|<span data-ttu-id="0bbb6-347">ProjOriginOnAcc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-347">ProjOriginOnAcc</span></span>|
|<span data-ttu-id="0bbb6-348">projPostedProjectTransactionsListFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-348">projPostedProjectTransactionsListFilter</span></span>|
|<span data-ttu-id="0bbb6-349">ProjProdTableListPageFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-349">ProjProdTableListPageFilter</span></span>|
|<span data-ttu-id="0bbb6-350">projProjectsListFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-350">projProjectsListFilter</span></span>|
|<span data-ttu-id="0bbb6-351">ProjQuotationTransTypeFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-351">ProjQuotationTransTypeFilter</span></span>|
|<span data-ttu-id="0bbb6-352">ProjResourceCapacityBooking</span><span class="sxs-lookup"><span data-stu-id="0bbb6-352">ProjResourceCapacityBooking</span></span>|
|<span data-ttu-id="0bbb6-353">ProjResourceViewType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-353">ProjResourceViewType</span></span>|
|<span data-ttu-id="0bbb6-354">ProjSelectTransOnAcc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-354">ProjSelectTransOnAcc</span></span>|
|<span data-ttu-id="0bbb6-355">ProjServerProcessStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-355">ProjServerProcessStatus</span></span>|
|<span data-ttu-id="0bbb6-356">ProjStatementTypeSub</span><span class="sxs-lookup"><span data-stu-id="0bbb6-356">ProjStatementTypeSub</span></span>|
|<span data-ttu-id="0bbb6-357">ProjStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-357">ProjStatus</span></span>|
|<span data-ttu-id="0bbb6-358">ProjTransType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-358">ProjTransType</span></span>|
|<span data-ttu-id="0bbb6-359">ProjValConnection</span><span class="sxs-lookup"><span data-stu-id="0bbb6-359">ProjValConnection</span></span>|
|<span data-ttu-id="0bbb6-360">ProjValidateType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-360">ProjValidateType</span></span>|
|<span data-ttu-id="0bbb6-361">ProjViewSubProjects</span><span class="sxs-lookup"><span data-stu-id="0bbb6-361">ProjViewSubProjects</span></span>|
|<span data-ttu-id="0bbb6-362">ProjYearEndOptions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-362">ProjYearEndOptions</span></span>|
|<span data-ttu-id="0bbb6-363">PSAActivityDisplayDefault</span><span class="sxs-lookup"><span data-stu-id="0bbb6-363">PSAActivityDisplayDefault</span></span>|
|<span data-ttu-id="0bbb6-364">PSAActivityParent</span><span class="sxs-lookup"><span data-stu-id="0bbb6-364">PSAActivityParent</span></span>|
|<span data-ttu-id="0bbb6-365">PSADetailLevel</span><span class="sxs-lookup"><span data-stu-id="0bbb6-365">PSADetailLevel</span></span>|
|<span data-ttu-id="0bbb6-366">PSAExpenseProjValCategoryType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-366">PSAExpenseProjValCategoryType</span></span>|
|<span data-ttu-id="0bbb6-367">PSAInvoiceFormats</span><span class="sxs-lookup"><span data-stu-id="0bbb6-367">PSAInvoiceFormats</span></span>|
|<span data-ttu-id="0bbb6-368">PSAProjInvoiceDetailGrouping</span><span class="sxs-lookup"><span data-stu-id="0bbb6-368">PSAProjInvoiceDetailGrouping</span></span>|
|<span data-ttu-id="0bbb6-369">PSAProjInvoiceDetailSortBy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-369">PSAProjInvoiceDetailSortBy</span></span>|
|<span data-ttu-id="0bbb6-370">PSAProjOriginakVsCurrent</span><span class="sxs-lookup"><span data-stu-id="0bbb6-370">PSAProjOriginakVsCurrent</span></span>|
|<span data-ttu-id="0bbb6-371">PSAPWPAssessment</span><span class="sxs-lookup"><span data-stu-id="0bbb6-371">PSAPWPAssessment</span></span>|
|<span data-ttu-id="0bbb6-372">PSAResAssignView</span><span class="sxs-lookup"><span data-stu-id="0bbb6-372">PSAResAssignView</span></span>|
|<span data-ttu-id="0bbb6-373">PSAResSchedStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-373">PSAResSchedStatus</span></span>|
|<span data-ttu-id="0bbb6-374">PurchStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-374">PurchStatus</span></span>|
|<span data-ttu-id="0bbb6-375">QuotationProjTransType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-375">QuotationProjTransType</span></span>|
|<span data-ttu-id="0bbb6-376">ReasonCodeAccountType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-376">ReasonCodeAccountType</span></span>|
|<span data-ttu-id="0bbb6-377">ResBasicSearchType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-377">ResBasicSearchType</span></span>|
|<span data-ttu-id="0bbb6-378">ResRollUpResourceType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-378">ResRollUpResourceType</span></span>|
|<span data-ttu-id="0bbb6-379">ResTransferType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-379">ResTransferType</span></span>|
|<span data-ttu-id="0bbb6-380">ResUtilizationCategoryEnum</span><span class="sxs-lookup"><span data-stu-id="0bbb6-380">ResUtilizationCategoryEnum</span></span>|
|<span data-ttu-id="0bbb6-381">RetailEventNotificationType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-381">RetailEventNotificationType</span></span>|
|<span data-ttu-id="0bbb6-382">SourceDocument_ActivityJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-382">SourceDocument_ActivityJournal</span></span>|
|<span data-ttu-id="0bbb6-383">SourceDocumentLine_ActivityJournalLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-383">SourceDocumentLine_ActivityJournalLine</span></span>|
|<span data-ttu-id="0bbb6-384">SpecType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-384">SpecType</span></span>|
|<span data-ttu-id="0bbb6-385">SyncProjTableAddSubProj</span><span class="sxs-lookup"><span data-stu-id="0bbb6-385">SyncProjTableAddSubProj</span></span>|
|<span data-ttu-id="0bbb6-386">SyncProjTableDeleteSubProj</span><span class="sxs-lookup"><span data-stu-id="0bbb6-386">SyncProjTableDeleteSubProj</span></span>|
|<span data-ttu-id="0bbb6-387">TrvCarRentalChargeType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-387">TrvCarRentalChargeType</span></span>|
|<span data-ttu-id="0bbb6-388">TrvExpenseFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-388">TrvExpenseFilter</span></span>|
|<span data-ttu-id="0bbb6-389">TrvExpenseReportGroupBy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-389">TrvExpenseReportGroupBy</span></span>|
|<span data-ttu-id="0bbb6-390">TrvIntermediatePageOnCreateExpenseReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-390">TrvIntermediatePageOnCreateExpenseReport</span></span>|
|<span data-ttu-id="0bbb6-391">TrvPayrollQtyOrDayes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-391">TrvPayrollQtyOrDayes</span></span>|
|<span data-ttu-id="0bbb6-392">TrvPBSTxtType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-392">TrvPBSTxtType</span></span>|
|<span data-ttu-id="0bbb6-393">TrvPolicyViolationAction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-393">TrvPolicyViolationAction</span></span>|
|<span data-ttu-id="0bbb6-394">TrvPosting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-394">TrvPosting</span></span>|
|<span data-ttu-id="0bbb6-395">TrvPostStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-395">TrvPostStatus</span></span>|
|<span data-ttu-id="0bbb6-396">TrvTaxType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-396">TrvTaxType</span></span>|
|<span data-ttu-id="0bbb6-397">TrvUDFDisplayOption</span><span class="sxs-lookup"><span data-stu-id="0bbb6-397">TrvUDFDisplayOption</span></span>|
|<span data-ttu-id="0bbb6-398">TSApprovalLevel</span><span class="sxs-lookup"><span data-stu-id="0bbb6-398">TSApprovalLevel</span></span>|
|<span data-ttu-id="0bbb6-399">TSDocumentStatusReset</span><span class="sxs-lookup"><span data-stu-id="0bbb6-399">TSDocumentStatusReset</span></span>|
|<span data-ttu-id="0bbb6-400">TSTimesheetFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-400">TSTimesheetFilter</span></span>|
|<span data-ttu-id="0bbb6-401">TSTimesheetLineFilterType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-401">TSTimesheetLineFilterType</span></span>|
|<span data-ttu-id="0bbb6-402">TSTimesheetListPageFilters</span><span class="sxs-lookup"><span data-stu-id="0bbb6-402">TSTimesheetListPageFilters</span></span>|
|<span data-ttu-id="0bbb6-403">TSVendorPerformanceThreshold</span><span class="sxs-lookup"><span data-stu-id="0bbb6-403">TSVendorPerformanceThreshold</span></span>|
|<span data-ttu-id="0bbb6-404">TypeOfCreditmaxCheck</span><span class="sxs-lookup"><span data-stu-id="0bbb6-404">TypeOfCreditmaxCheck</span></span>|
|<span data-ttu-id="0bbb6-405">VendInvoiceCloseCommand</span><span class="sxs-lookup"><span data-stu-id="0bbb6-405">VendInvoiceCloseCommand</span></span>|
|<span data-ttu-id="0bbb6-406">VendorInvoiceSearchOptions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-406">VendorInvoiceSearchOptions</span></span>|
|<span data-ttu-id="0bbb6-407">VendOutPaymFeeDistribution</span><span class="sxs-lookup"><span data-stu-id="0bbb6-407">VendOutPaymFeeDistribution</span></span>|

<span data-ttu-id="0bbb6-408">拡張可能な列挙型のサポートを改善するために、Foundation の変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-408">Foundation changes were made to improve support for extensible enumerations.</span></span> <span data-ttu-id="0bbb6-409">**IsExtensible** が **はい** に設定されている列挙型については、**SysPlugin** フレームワークが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-409">The **SysPlugin** framework was enabled for enumerations where **IsExtensible** is set to **Yes**.</span></span> <span data-ttu-id="0bbb6-410">列挙型の新しい名前に基づく構文で、ビューが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-410">Views were enabled with new name-based syntax for enumerations.</span></span>

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a><span data-ttu-id="0bbb6-411">DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド</span><span class="sxs-lookup"><span data-stu-id="0bbb6-411">Data manipulation methods that do not raise DataEvents or missing insert, update, delete pre- and post-data events</span></span>

<span data-ttu-id="0bbb6-412">一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-412">As a general practice, you use data methods on tables to raise events that can be used for extending the application.</span></span> <span data-ttu-id="0bbb6-413">コード ベースは、必ずしもこのプラクティスに従っていませんでした。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-413">The code base has not always followed this practice.</span></span> <span data-ttu-id="0bbb6-414">たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-414">For example, the **doInsert**, **doUpdate**, and **doDelete** data methods and certain table implementations did not make a call to **super()** in the data method.</span></span>

<span data-ttu-id="0bbb6-415">タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-415">The **insert**, **update**, and **delete** methods on the type classes have been refactored.</span></span> <span data-ttu-id="0bbb6-416">データ メソッドで **super()** が確実に呼び出されるように変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-416">Changes were made so that **super()** is called more consistently in data methods.</span></span> <span data-ttu-id="0bbb6-417">これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-417">These changes enable extensions to be added to these methods, so that pre- and post-events are now available for extension.</span></span> <span data-ttu-id="0bbb6-418">次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-418">The tables where the **insert**, **update**, and **delete** events were enabled for extension are listed in the following table.</span></span>

| <span data-ttu-id="0bbb6-419">テーブルとメソッド</span><span class="sxs-lookup"><span data-stu-id="0bbb6-419">Table and method</span></span> |
| ----------------------|
|<span data-ttu-id="0bbb6-420">BOM</span><span class="sxs-lookup"><span data-stu-id="0bbb6-420">BOM</span></span>|
|<span data-ttu-id="0bbb6-421">BOMTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-421">BOMTable</span></span>|
|<span data-ttu-id="0bbb6-422">BOMVersion</span><span class="sxs-lookup"><span data-stu-id="0bbb6-422">BOMVersion</span></span>|
|<span data-ttu-id="0bbb6-423">ProjTableType.delete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-423">ProjTableType.delete</span></span>|
|<span data-ttu-id="0bbb6-424">ProjTableType.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-424">ProjTableType.update</span></span>|
|<span data-ttu-id="0bbb6-425">工順</span><span class="sxs-lookup"><span data-stu-id="0bbb6-425">Route</span></span>|
|<span data-ttu-id="0bbb6-426">RouteOpr</span><span class="sxs-lookup"><span data-stu-id="0bbb6-426">RouteOpr</span></span>|
|<span data-ttu-id="0bbb6-427">RouteTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-427">RouteTable</span></span>|
|<span data-ttu-id="0bbb6-428">RouteVersion</span><span class="sxs-lookup"><span data-stu-id="0bbb6-428">RouteVersion</span></span>|
|<span data-ttu-id="0bbb6-429">SalesLineType::interCompanyResetDeliverNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-429">SalesLineType::interCompanyResetDeliverNow</span></span>|
|<span data-ttu-id="0bbb6-430">テーブル ForecastSales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-430">Table ForecastSales</span></span>|

## <a name="exposing-class-members"></a><span data-ttu-id="0bbb6-431">クラス メンバーの公開</span><span class="sxs-lookup"><span data-stu-id="0bbb6-431">Exposing class members</span></span>

<span data-ttu-id="0bbb6-432">アクセス修飾子と新しい parm メソッドの変更の結果、追加のプライベート メンバーをカスタマイズに使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-432">Additional private members are now available for customization as a result of changes to access modifiers and parm methods.</span></span> <span data-ttu-id="0bbb6-433">コマンド プラットフォームのチェーン機能により、保護されたメソッドやメンバーへの拡張クラスのアクセスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-433">The chain of command platform feature enables extension class access to protected methods and members.</span></span> <span data-ttu-id="0bbb6-434">コマンド チェーンの詳細については、「[拡張可能な X++: コマンド チェーン](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-434">For more information about chain of command, see [Extensible X++: Chain of Command](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/).</span></span>

| <span data-ttu-id="0bbb6-435">メンバー</span><span class="sxs-lookup"><span data-stu-id="0bbb6-435">Member</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-436">BankPaymCancel.custTransToCancel</span><span class="sxs-lookup"><span data-stu-id="0bbb6-436">BankPaymCancel.custTransToCancel</span></span>|
|<span data-ttu-id="0bbb6-437">CustCollectionLetterCancel - メソッド queryBuildUpdate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-437">CustCollectionLetterCancel - method queryBuildUpdate</span></span>|
|<span data-ttu-id="0bbb6-438">CustCollectionLetterPost - メソッド queryBuildUpdate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-438">CustCollectionLetterPost - method queryBuildUpdate</span></span>|
|<span data-ttu-id="0bbb6-439">CustCollectionLetterPost - メソッド updateFee</span><span class="sxs-lookup"><span data-stu-id="0bbb6-439">CustCollectionLetterPost - method updateFee</span></span>|
|<span data-ttu-id="0bbb6-440">CustCollectionLetterPost - メソッド validateCollectionLetter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-440">CustCollectionLetterPost - method validateCollectionLetter</span></span>|
|<span data-ttu-id="0bbb6-441">CustInterestCancel - メソッド updateQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-441">CustInterestCancel - method updateQuery</span></span>|
|<span data-ttu-id="0bbb6-442">CustInterestHelper - メソッド getFeeLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-442">CustInterestHelper - method getFeeLedgerAccount</span></span>|
|<span data-ttu-id="0bbb6-443">CustInterestHelper - メソッド getInterestRecord</span><span class="sxs-lookup"><span data-stu-id="0bbb6-443">CustInterestHelper - method getInterestRecord</span></span>|
|<span data-ttu-id="0bbb6-444">CustInterestHelper - メソッド getPostingProfile</span><span class="sxs-lookup"><span data-stu-id="0bbb6-444">CustInterestHelper - method getPostingProfile</span></span>|
|<span data-ttu-id="0bbb6-445">CustInterestHelper - メソッド getTransLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-445">CustInterestHelper - method getTransLedgerAccount</span></span>|
|<span data-ttu-id="0bbb6-446">CustInterestHelper - メソッド getTransLineLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-446">CustInterestHelper - method getTransLineLedgerAccount</span></span>|
|<span data-ttu-id="0bbb6-447">CustInterestHelper - メソッド getVerDetailLedgerDimensionByIntTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-447">CustInterestHelper - method getVerDetailLedgerDimensionByIntTrans</span></span>|
|<span data-ttu-id="0bbb6-448">CustInterestPost - メソッド postVoucher</span><span class="sxs-lookup"><span data-stu-id="0bbb6-448">CustInterestPost - method postVoucher</span></span>|
|<span data-ttu-id="0bbb6-449">CustOutPaymControlController</span><span class="sxs-lookup"><span data-stu-id="0bbb6-449">CustOutPaymControlController</span></span>|
|<span data-ttu-id="0bbb6-450">CustVendCreatePaymJournal - メソッド dialogAddInvoiceSelectionCriteriaFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-450">CustVendCreatePaymJournal - method dialogAddInvoiceSelectionCriteriaFields</span></span>|
|<span data-ttu-id="0bbb6-451">CustVendPaymProposal - メソッド createProposalLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-451">CustVendPaymProposal - method createProposalLine</span></span>|
|<span data-ttu-id="0bbb6-452">CustVendPaymProposal - メソッド parmLedgerJournalId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-452">CustVendPaymProposal - method parmLedgerJournalId</span></span>|
|<span data-ttu-id="0bbb6-453">CustVendPaymProposalLineInsertSetManager - 変数</span><span class="sxs-lookup"><span data-stu-id="0bbb6-453">CustVendPaymProposalLineInsertSetManager - variables</span></span>|
|<span data-ttu-id="0bbb6-454">CustVendPaymProposalOrg - 変数</span><span class="sxs-lookup"><span data-stu-id="0bbb6-454">CustVendPaymProposalOrg - variables</span></span>|
|<span data-ttu-id="0bbb6-455">CustVendPaymProposalTransferToJournal - メソッド trackSpecTransForUpdate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-455">CustVendPaymProposalTransferToJournal - method trackSpecTransForUpdate</span></span>|
|<span data-ttu-id="0bbb6-456">CustVendPaymProposalTransferToJournal - 変数</span><span class="sxs-lookup"><span data-stu-id="0bbb6-456">CustVendPaymProposalTransferToJournal - variables</span></span>|
|<span data-ttu-id="0bbb6-457">フォーム ProjWorkBreakdownStructure</span><span class="sxs-lookup"><span data-stu-id="0bbb6-457">Form ProjWorkBreakdownStructure</span></span>|
|<span data-ttu-id="0bbb6-458">フォーム/クラス CustPaymModeSpec</span><span class="sxs-lookup"><span data-stu-id="0bbb6-458">Form/Class CustPaymModeSpec</span></span>|
|<span data-ttu-id="0bbb6-459">フォーム/クラス VendPaymModeSpec</span><span class="sxs-lookup"><span data-stu-id="0bbb6-459">Form/Class VendPaymModeSpec</span></span>|
|<span data-ttu-id="0bbb6-460">InventUpd_ChildReference.initUpdate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-460">InventUpd_ChildReference.initUpdate</span></span>|
|<span data-ttu-id="0bbb6-461">InventUpd_ChildReference.parmInventDimId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-461">InventUpd_ChildReference.parmInventDimId</span></span>|
|<span data-ttu-id="0bbb6-462">LogisticsLocationFormHandler.callerGetAddressRecord</span><span class="sxs-lookup"><span data-stu-id="0bbb6-462">LogisticsLocationFormHandler.callerGetAddressRecord</span></span>|
|<span data-ttu-id="0bbb6-463">ProjAdjustmentSelect.newQuery.addAdditionalHeaderRange</span><span class="sxs-lookup"><span data-stu-id="0bbb6-463">ProjAdjustmentSelect.newQuery.addAdditionalHeaderRange</span></span>|
|<span data-ttu-id="0bbb6-464">ProjAdjustmentSelect.processProjCostTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-464">ProjAdjustmentSelect.processProjCostTrans</span></span>|
|<span data-ttu-id="0bbb6-465">ProjAdjustmentSplit.deleteTransaction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-465">ProjAdjustmentSplit.deleteTransaction</span></span>|
|<span data-ttu-id="0bbb6-466">ProjAdjustmentSplit.splitTransaction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-466">ProjAdjustmentSplit.splitTransaction</span></span>|
|<span data-ttu-id="0bbb6-467">ProjInvoiceChoose.parmprojInvoiceProjId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-467">ProjInvoiceChoose.parmprojInvoiceProjId</span></span>|
|<span data-ttu-id="0bbb6-468">ProjProposalTotals.projInvoiceExchRate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-468">ProjProposalTotals.projInvoiceExchRate</span></span>|
|<span data-ttu-id="0bbb6-469">SalesInvoiceJournalCreateBase</span><span class="sxs-lookup"><span data-stu-id="0bbb6-469">SalesInvoiceJournalCreateBase</span></span>|
|<span data-ttu-id="0bbb6-470">smmActivityCreate.createOrPrompt</span><span class="sxs-lookup"><span data-stu-id="0bbb6-470">smmActivityCreate.createOrPrompt</span></span>|
|<span data-ttu-id="0bbb6-471">テーブル SalesQuotationTable.canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-471">Table SalesQuotationTable.canSubmitToWorkflow</span></span>|
|<span data-ttu-id="0bbb6-472">VendorInvoiceLineSourceDocLineItem.initializeProjectFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-472">VendorInvoiceLineSourceDocLineItem.initializeProjectFields</span></span>|
|<span data-ttu-id="0bbb6-473">WHSWorkUserSession.WorkExecuteMode</span><span class="sxs-lookup"><span data-stu-id="0bbb6-473">WHSWorkUserSession.WorkExecuteMode</span></span>|

## <a name="construct-methods-with-throw-statements"></a><span data-ttu-id="0bbb6-474">throw ステートメントを使用した construct メソッド</span><span class="sxs-lookup"><span data-stu-id="0bbb6-474">Construct methods with throw statements</span></span>

<span data-ttu-id="0bbb6-475">特定の型の実装が欠落していた場合、いくつかの **construct** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-475">Some **construct** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="0bbb6-476">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**construct** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-476">This doesn't work well with extensibility, so to mitigate this, **construct** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="0bbb6-477">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-477">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="0bbb6-478">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0bbb6-478">Object</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-479">AddressZipCodeImport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-479">AddressZipCodeImport</span></span>|
|<span data-ttu-id="0bbb6-480">CaseCategoryHierarchyTree</span><span class="sxs-lookup"><span data-stu-id="0bbb6-480">CaseCategoryHierarchyTree</span></span>|
|<span data-ttu-id="0bbb6-481">CustInterestCancel</span><span class="sxs-lookup"><span data-stu-id="0bbb6-481">CustInterestCancel</span></span>|
|<span data-ttu-id="0bbb6-482">CustInterestHelper</span><span class="sxs-lookup"><span data-stu-id="0bbb6-482">CustInterestHelper</span></span>|
|<span data-ttu-id="0bbb6-483">CustInterestPost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-483">CustInterestPost</span></span>|
|<span data-ttu-id="0bbb6-484">CustOutPaymControlController</span><span class="sxs-lookup"><span data-stu-id="0bbb6-484">CustOutPaymControlController</span></span>|
|<span data-ttu-id="0bbb6-485">CustTransQueryBuild</span><span class="sxs-lookup"><span data-stu-id="0bbb6-485">CustTransQueryBuild</span></span>|
|<span data-ttu-id="0bbb6-486">CustVendCreatePaymJournal_Cust</span><span class="sxs-lookup"><span data-stu-id="0bbb6-486">CustVendCreatePaymJournal_Cust</span></span>|
|<span data-ttu-id="0bbb6-487">CustVendFindSettlements</span><span class="sxs-lookup"><span data-stu-id="0bbb6-487">CustVendFindSettlements</span></span>|
|<span data-ttu-id="0bbb6-488">CustVendOpenTransBalances.new</span><span class="sxs-lookup"><span data-stu-id="0bbb6-488">CustVendOpenTransBalances.new</span></span>|
|<span data-ttu-id="0bbb6-489">CustVendOpenTransManager.initFromCaller</span><span class="sxs-lookup"><span data-stu-id="0bbb6-489">CustVendOpenTransManager.initFromCaller</span></span>|
|<span data-ttu-id="0bbb6-490">CustVendPaymProposalTransferToJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-490">CustVendPaymProposalTransferToJournal</span></span>|
|<span data-ttu-id="0bbb6-491">CustVendTransQueryBuild</span><span class="sxs-lookup"><span data-stu-id="0bbb6-491">CustVendTransQueryBuild</span></span>|
|<span data-ttu-id="0bbb6-492">フォーム PdsApprovedVendorList</span><span class="sxs-lookup"><span data-stu-id="0bbb6-492">Form PdsApprovedVendorList</span></span>|
|<span data-ttu-id="0bbb6-493">フォーム WhsContainerTable.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-493">Form WhsContainerTable.init</span></span>|
|<span data-ttu-id="0bbb6-494">FormletterJournalCreate.newSalesJournalCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-494">FormletterJournalCreate.newSalesJournalCreate</span></span>|
|<span data-ttu-id="0bbb6-495">FormLetterJournalPost.newPostSales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-495">FormLetterJournalPost.newPostSales</span></span>|
|<span data-ttu-id="0bbb6-496">InventUpd_Physical::newInventMovement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-496">InventUpd_Physical::newInventMovement</span></span>|
|<span data-ttu-id="0bbb6-497">InventUpd_Physical::newProdReleaseLossProfit_RU</span><span class="sxs-lookup"><span data-stu-id="0bbb6-497">InventUpd_Physical::newProdReleaseLossProfit_RU</span></span>|
|<span data-ttu-id="0bbb6-498">LogisticsLocationSelectForm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-498">LogisticsLocationSelectForm</span></span>|
|<span data-ttu-id="0bbb6-499">PdsApprovedVendorListCheck.newBasedOnTableType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-499">PdsApprovedVendorListCheck.newBasedOnTableType</span></span>|
|<span data-ttu-id="0bbb6-500">ProjInvoiceChoose</span><span class="sxs-lookup"><span data-stu-id="0bbb6-500">ProjInvoiceChoose</span></span>|
|<span data-ttu-id="0bbb6-501">ProjTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-501">ProjTrans</span></span>|
|<span data-ttu-id="0bbb6-502">PurchReqAutoCreate.newAutoCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-502">PurchReqAutoCreate.newAutoCreate</span></span>|
|<span data-ttu-id="0bbb6-503">PurchTableForm_Project</span><span class="sxs-lookup"><span data-stu-id="0bbb6-503">PurchTableForm_Project</span></span>|
|<span data-ttu-id="0bbb6-504">SalesQuantity</span><span class="sxs-lookup"><span data-stu-id="0bbb6-504">SalesQuantity</span></span>|
|<span data-ttu-id="0bbb6-505">SalesTotals</span><span class="sxs-lookup"><span data-stu-id="0bbb6-505">SalesTotals</span></span>|
|<span data-ttu-id="0bbb6-506">WHSReservation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-506">WHSReservation</span></span>|

## <a name="find-methods-with-throw-statements"></a><span data-ttu-id="0bbb6-507">throw ステートメントのメソッドを検索します</span><span class="sxs-lookup"><span data-stu-id="0bbb6-507">Find methods with throw statements</span></span>

<span data-ttu-id="0bbb6-508">特定の型の実装が欠落していた場合、いくつかの **find** メソッドが **throw** ステートメントで実装されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-508">Some **find** methods were implemented with **throw** statements if there was a missing implementation for a given type.</span></span> <span data-ttu-id="0bbb6-509">これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**find** メソッドが変更されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-509">This does not work well with extensibility, so to mitigate this, **find** methods were changed so that they do not throw exceptions.</span></span> <span data-ttu-id="0bbb6-510">以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-510">These methods are now to open for extensibility through class augmentation or by post-event subscription.</span></span>

| <span data-ttu-id="0bbb6-511">メソッド</span><span class="sxs-lookup"><span data-stu-id="0bbb6-511">Methods</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-512">TradePostalAddress.partyTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-512">TradePostalAddress.partyTable</span></span>|

## <a name="extracted-method-to-open-for-class-extensions"></a><span data-ttu-id="0bbb6-513">クラス拡張子を開くための抽出されたメソッド</span><span class="sxs-lookup"><span data-stu-id="0bbb6-513">Extracted method to open for class extensions</span></span>

<span data-ttu-id="0bbb6-514">**コマンドのチェーン**機能では、拡張クラスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-514">The **Chain of Command** feature lets you create extension classes.</span></span> <span data-ttu-id="0bbb6-515">拡張子クラスは、保護されたメソッドとパブリック メソッドおよびメンバーの両方にアクセスできるため、他のオプションよりも強力な拡張方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-515">Extensions classes offer a stronger way of extending than other options because they allow access to both protected and public methods and members.</span></span> <span data-ttu-id="0bbb6-516">これにより、デリゲートやプレイベントまたはポスト イベントによって拡張するよりも柔軟性が向上します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-516">This provides more flexibility than extending through delegates or by pre or post event.</span></span>

<span data-ttu-id="0bbb6-517">変更のこのグループでは、長いメソッドが小さいメソッドに抽出されます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-517">Within this group of changes, longer methods are extracted into smaller methods.</span></span> <span data-ttu-id="0bbb6-518">新しいメソッドには、より具体的なフォーカスがあり、拡張機能の範囲をより詳細に制御できます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-518">The new methods have a more specific focus and you have more control over the scope of your extensions.</span></span>

<span data-ttu-id="0bbb6-519">**指揮命令系統**機能が導入された後、デリゲートを追加する代わりにメソッドを抽出して拡張性を使用することをお勧めします。このアプローチにより、より柔軟なソリューションを提供する事ができるからです。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-519">After the introduction of the **Chain of Command** feature, we suggest using extensibility by extracting methods instead of adding delegates because this approach provides a more versatile solution.</span></span>

<span data-ttu-id="0bbb6-520">次のテーブルに、拡張クラスをビルドするために抽出されて開かれた新しいメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-520">The following table lists the new methods that have been extracted and opened for building extension classes.</span></span>

| <span data-ttu-id="0bbb6-521">方法</span><span class="sxs-lookup"><span data-stu-id="0bbb6-521">Method</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-522">AssetPost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-522">AssetPost</span></span>|
|<span data-ttu-id="0bbb6-523">BankPrintTestCheque</span><span class="sxs-lookup"><span data-stu-id="0bbb6-523">BankPrintTestCheque</span></span>|
|<span data-ttu-id="0bbb6-524">CustCreditLimit.showErrorMsg</span><span class="sxs-lookup"><span data-stu-id="0bbb6-524">CustCreditLimit.showErrorMsg</span></span>|
|<span data-ttu-id="0bbb6-525">CustVendCheque</span><span class="sxs-lookup"><span data-stu-id="0bbb6-525">CustVendCheque</span></span>|
|<span data-ttu-id="0bbb6-526">CustVendChequeSlipTextCalculator</span><span class="sxs-lookup"><span data-stu-id="0bbb6-526">CustVendChequeSlipTextCalculator</span></span>|
|<span data-ttu-id="0bbb6-527">フォーム CustBankAccounts</span><span class="sxs-lookup"><span data-stu-id="0bbb6-527">Form CustBankAccounts</span></span>|
|<span data-ttu-id="0bbb6-528">フォーム DirPartyQuickCreateForm.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-528">Form DirPartyQuickCreateForm.init</span></span>|
|<span data-ttu-id="0bbb6-529">フォーム HierarchyDetail.contextChanged</span><span class="sxs-lookup"><span data-stu-id="0bbb6-529">Form HierarchyDetail.contextChanged</span></span>|
|<span data-ttu-id="0bbb6-530">フォーム HierarchyDetail: smmActiviate: initValue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-530">Form HierarchyDetail: smmActiviate:  initValue</span></span>|
|<span data-ttu-id="0bbb6-531">フォーム HierarchyNameLookoup: 階層: init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-531">Form HierarchyNameLookoup: Hierarchy: init</span></span>|
|<span data-ttu-id="0bbb6-532">フォーム LedgerJournalTransDimension.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-532">Form LedgerJournalTransDimension.init</span></span>|
|<span data-ttu-id="0bbb6-533">フォーム ProjInvoiceProposalDetail.editInvoiceFormat</span><span class="sxs-lookup"><span data-stu-id="0bbb6-533">Form ProjInvoiceProposalDetail.editInvoiceFormat</span></span>|
|<span data-ttu-id="0bbb6-534">フォーム SalesCopying.upDateRemainderCache</span><span class="sxs-lookup"><span data-stu-id="0bbb6-534">Form SalesCopying.upDateRemainderCache</span></span>|
|<span data-ttu-id="0bbb6-535">フォーム SalesQuotationProjLinkWizard-> changeType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-535">Form SalesQuotationProjLinkWizard-> changeType</span></span>|
|<span data-ttu-id="0bbb6-536">フォーム smmActivities: ResponsibleWorker_Overview: lookupReference</span><span class="sxs-lookup"><span data-stu-id="0bbb6-536">Form smmActivities: ResponsibleWorker_Overview: lookupReference</span></span>|
|<span data-ttu-id="0bbb6-537">フォーム smmActivities: smmActivities::initValue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-537">Form smmActivities: smmActivities::initValue</span></span>|
|<span data-ttu-id="0bbb6-538">FormletterJournalPrint</span><span class="sxs-lookup"><span data-stu-id="0bbb6-538">FormletterJournalPrint</span></span>|
|<span data-ttu-id="0bbb6-539">HierarchyTemplateCopying.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-539">HierarchyTemplateCopying.run</span></span>|
|<span data-ttu-id="0bbb6-540">HierarchyTemplateCopying_CRM.copyActivity</span><span class="sxs-lookup"><span data-stu-id="0bbb6-540">HierarchyTemplateCopying_CRM.copyActivity</span></span>|
|<span data-ttu-id="0bbb6-541">HierarchyTemplateCopyingDialog.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-541">HierarchyTemplateCopyingDialog.main</span></span>|
|<span data-ttu-id="0bbb6-542">HierarchyTree</span><span class="sxs-lookup"><span data-stu-id="0bbb6-542">HierarchyTree</span></span>|
|<span data-ttu-id="0bbb6-543">HierarchyTree.buildSubTree</span><span class="sxs-lookup"><span data-stu-id="0bbb6-543">HierarchyTree.buildSubTree</span></span>|
|<span data-ttu-id="0bbb6-544">InventDimCtrl_Frm_Mov_QualityOrder.mustEnableField</span><span class="sxs-lookup"><span data-stu-id="0bbb6-544">InventDimCtrl_Frm_Mov_QualityOrder.mustEnableField</span></span>|
|<span data-ttu-id="0bbb6-545">InventDistinctProductValidator.checkProductNotStopped</span><span class="sxs-lookup"><span data-stu-id="0bbb6-545">InventDistinctProductValidator.checkProductNotStopped</span></span>|
|<span data-ttu-id="0bbb6-546">InventMovement.createProjLedgerForUpdateLedgerAdjust</span><span class="sxs-lookup"><span data-stu-id="0bbb6-546">InventMovement.createProjLedgerForUpdateLedgerAdjust</span></span>|
|<span data-ttu-id="0bbb6-547">InventTransferUpdShip::populateIssueReceiptDimensions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-547">InventTransferUpdShip::populateIssueReceiptDimensions</span></span>|
|<span data-ttu-id="0bbb6-548">JournalFormTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-548">JournalFormTable</span></span>|
|<span data-ttu-id="0bbb6-549">JournalizingDefinitionManager.newJournalizingDefinitionManagerCustomer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-549">JournalizingDefinitionManager.newJournalizingDefinitionManagerCustomer</span></span>|
|<span data-ttu-id="0bbb6-550">LedgerJournalCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-550">LedgerJournalCheckPost.checkJournal</span></span>|
|<span data-ttu-id="0bbb6-551">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-551">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="0bbb6-552">LedgerJournalEngine.parmLedgerJournalTrans_Project</span><span class="sxs-lookup"><span data-stu-id="0bbb6-552">LedgerJournalEngine.parmLedgerJournalTrans_Project</span></span>|
|<span data-ttu-id="0bbb6-553">LedgerJournalEngine_Server.addVoucher</span><span class="sxs-lookup"><span data-stu-id="0bbb6-553">LedgerJournalEngine_Server.addVoucher</span></span>|
|<span data-ttu-id="0bbb6-554">LedgerJournalEngine_VendApprove.cancelVoucher</span><span class="sxs-lookup"><span data-stu-id="0bbb6-554">LedgerJournalEngine_VendApprove.cancelVoucher</span></span>|
|<span data-ttu-id="0bbb6-555">LedgerJournalizeReportDP_DE.processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-555">LedgerJournalizeReportDP_DE.processReport</span></span>|
|<span data-ttu-id="0bbb6-556">LedgerJournalTransUpdateCust.checkAccountBlocked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-556">LedgerJournalTransUpdateCust.checkAccountBlocked</span></span>|
|<span data-ttu-id="0bbb6-557">LedgerJournalTransUpdateVend.checkVendorBlocked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-557">LedgerJournalTransUpdateVend.checkVendorBlocked</span></span>|
|<span data-ttu-id="0bbb6-558">LogisticsAddressFormatProcess.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-558">LogisticsAddressFormatProcess.run</span></span>|
|<span data-ttu-id="0bbb6-559">ProjAdjustmentUpdate.journalTableInsert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-559">ProjAdjustmentUpdate.journalTableInsert</span></span>|
|<span data-ttu-id="0bbb6-560">ProjAdjustmentUpdate_Post</span><span class="sxs-lookup"><span data-stu-id="0bbb6-560">ProjAdjustmentUpdate_Post</span></span>|
|<span data-ttu-id="0bbb6-561">projCategoryLookup.buildQuery_PSA_impl</span><span class="sxs-lookup"><span data-stu-id="0bbb6-561">projCategoryLookup.buildQuery_PSA_impl</span></span>|
|<span data-ttu-id="0bbb6-562">ProjEstimate.add</span><span class="sxs-lookup"><span data-stu-id="0bbb6-562">ProjEstimate.add</span></span>|
|<span data-ttu-id="0bbb6-563">ProjFormLetter_invoice.projPrintFormLetter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-563">ProjFormLetter_invoice.projPrintFormLetter</span></span>|
|<span data-ttu-id="0bbb6-564">ProjIntercompanyVendorInvoiceCreator.createVendorInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-564">ProjIntercompanyVendorInvoiceCreator.createVendorInvoiceLine</span></span>|
|<span data-ttu-id="0bbb6-565">ProjListTransDP.insertTmpProjTransList</span><span class="sxs-lookup"><span data-stu-id="0bbb6-565">ProjListTransDP.insertTmpProjTransList</span></span>|
|<span data-ttu-id="0bbb6-566">ProjPostRevenueProposal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-566">ProjPostRevenueProposal.projTransCreate</span></span>|
|<span data-ttu-id="0bbb6-567">projUnpostedTransactionsListPage.populateMenuFunction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-567">projUnpostedTransactionsListPage.populateMenuFunction</span></span>|
|<span data-ttu-id="0bbb6-568">PSAProjAndContractInvoiceController.preRunModifyContract</span><span class="sxs-lookup"><span data-stu-id="0bbb6-568">PSAProjAndContractInvoiceController.preRunModifyContract</span></span>|
|<span data-ttu-id="0bbb6-569">PSARetenetionRelease.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-569">PSARetenetionRelease.run</span></span>|
|<span data-ttu-id="0bbb6-570">PurchAutoCreate_SalesLine.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-570">PurchAutoCreate_SalesLine.setPurchTable</span></span>|
|<span data-ttu-id="0bbb6-571">PurchCreateFromSalesOrder.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-571">PurchCreateFromSalesOrder.run</span></span>|
|<span data-ttu-id="0bbb6-572">PurchFormletterParmDataInvoice.createParmLinesAndTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-572">PurchFormletterParmDataInvoice.createParmLinesAndTable</span></span>|
|<span data-ttu-id="0bbb6-573">PurchTableForm_DlvScheduleSyncEnabled.syncDeliveryScheduleCommercialAttributes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-573">PurchTableForm_DlvScheduleSyncEnabled.syncDeliveryScheduleCommercialAttributes</span></span>|
|<span data-ttu-id="0bbb6-574">ReqCalc.deleteItemRequirement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-574">ReqCalc.deleteItemRequirement</span></span>|
|<span data-ttu-id="0bbb6-575">ReturnAcknowledgmentAndDocumentDP.insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-575">ReturnAcknowledgmentAndDocumentDP.insertIntoTempTable</span></span>|
|<span data-ttu-id="0bbb6-576">ReturnAcknowledgmentAndDocumentDP.setReturnAckAndDocumentTemplate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-576">ReturnAcknowledgmentAndDocumentDP.setReturnAckAndDocumentTemplate</span></span>|
|<span data-ttu-id="0bbb6-577">SalesAgreementFormDatasourceManager.transferCustAccount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-577">SalesAgreementFormDatasourceManager.transferCustAccount</span></span>|
|<span data-ttu-id="0bbb6-578">SalesCopying.copy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-578">SalesCopying.copy</span></span>|
|<span data-ttu-id="0bbb6-579">SalesFormLetterParmData.createParmSubTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-579">SalesFormLetterParmData.createParmSubTable</span></span>|
|<span data-ttu-id="0bbb6-580">SalesFormLetterParmDataInvoice.reSelectInit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-580">SalesFormLetterParmDataInvoice.reSelectInit</span></span>|
|<span data-ttu-id="0bbb6-581">SalesQuotationConfirmationDP.processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-581">SalesQuotationConfirmationDP.processReport</span></span>|
|<span data-ttu-id="0bbb6-582">SalesQuotationConfirmationDP.setSalesQuotationDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-582">SalesQuotationConfirmationDP.setSalesQuotationDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-583">SalesQuotationEditLinesForm.createParmLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-583">SalesQuotationEditLinesForm.createParmLine</span></span>|
|<span data-ttu-id="0bbb6-584">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-584">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span></span>|
|<span data-ttu-id="0bbb6-585">SalesQuotationTableForm_Sales.syncDeliveryScheduleCommercialAttributes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-585">SalesQuotationTableForm_Sales.syncDeliveryScheduleCommercialAttributes</span></span>|
|<span data-ttu-id="0bbb6-586">SalesQuotationTableType.validateField</span><span class="sxs-lookup"><span data-stu-id="0bbb6-586">SalesQuotationTableType.validateField</span></span>|
|<span data-ttu-id="0bbb6-587">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-587">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="0bbb6-588">SalesTableForm.interCompanySetLineAccess</span><span class="sxs-lookup"><span data-stu-id="0bbb6-588">SalesTableForm.interCompanySetLineAccess</span></span>|
|<span data-ttu-id="0bbb6-589">SalesTableForm_DlvScheduleSyncEnabled.syncDeliveryScheduleCommercialAttributes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-589">SalesTableForm_DlvScheduleSyncEnabled.syncDeliveryScheduleCommercialAttributes</span></span>|
|<span data-ttu-id="0bbb6-590">SalesUpdateRemain.updateICDeliverRemainder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-590">SalesUpdateRemain.updateICDeliverRemainder</span></span>|
|<span data-ttu-id="0bbb6-591">SmmProcessInstance.openForm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-591">SmmProcessInstance.openForm</span></span>|
|<span data-ttu-id="0bbb6-592">SubledgerJournalizerProjectExtension.createProjectActualHeader</span><span class="sxs-lookup"><span data-stu-id="0bbb6-592">SubledgerJournalizerProjectExtension.createProjectActualHeader</span></span>|
|<span data-ttu-id="0bbb6-593">テーブル CustTable.createOneTimeAccount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-593">Table CustTable.createOneTimeAccount</span></span>|
|<span data-ttu-id="0bbb6-594">テーブル CustTable.lookupCustomer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-594">Table CustTable.lookupCustomer</span></span>|
|<span data-ttu-id="0bbb6-595">テーブル InventPosting.salesAccount2AccountType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-595">Table InventPosting.salesAccount2AccountType</span></span>|
|<span data-ttu-id="0bbb6-596">テーブル InventTable.lookupItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-596">Table InventTable.lookupItem</span></span>|
|<span data-ttu-id="0bbb6-597">テーブル ReqPO.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-597">Table ReqPO.update</span></span>|
|<span data-ttu-id="0bbb6-598">テーブル SalesLine -> createFromSalesQuotationLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-598">Table SalesLine -> createFromSalesQuotationLine</span></span>|
|<span data-ttu-id="0bbb6-599">テーブル SalesTable::initFromCustTableIL</span><span class="sxs-lookup"><span data-stu-id="0bbb6-599">Table SalesTable::initFromCustTableIL</span></span>|
|<span data-ttu-id="0bbb6-600">テーブル smmBusRelTable.relation2Customer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-600">Table smmBusRelTable.relation2Customer</span></span>|
|<span data-ttu-id="0bbb6-601">テーブル smmBusRelTable.updateCustTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-601">Table smmBusRelTable.updateCustTable</span></span>|
|<span data-ttu-id="0bbb6-602">テーブル TSTimesheetTrans.updateCommentsFromLineWeekUpdateTSTimesheetTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-602">Table TSTimesheetTrans.updateCommentsFromLineWeekUpdateTSTimesheetTrans</span></span>|
|<span data-ttu-id="0bbb6-603">テーブル TSTimesheetTrans.updateFromTimesheetLineWeekUpdateTSTimesheetTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-603">Table TSTimesheetTrans.updateFromTimesheetLineWeekUpdateTSTimesheetTrans</span></span>|
|<span data-ttu-id="0bbb6-604">テーブル VendTable.lookupVendor</span><span class="sxs-lookup"><span data-stu-id="0bbb6-604">Table VendTable.lookupVendor</span></span>|
|<span data-ttu-id="0bbb6-605">テーブル WHSWorkTable ->deleteAndCleanupWorkLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-605">Table WHSWorkTable ->deleteAndCleanupWorkLines</span></span>|
|<span data-ttu-id="0bbb6-606">テーブル WHSWorkTable ->SetBlankFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-606">Table WHSWorkTable ->SetBlankFields</span></span>|
|<span data-ttu-id="0bbb6-607">テーブル WHSWorkTable ->SetFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-607">Table WHSWorkTable ->SetFields</span></span>|
|<span data-ttu-id="0bbb6-608">テーブル WrkCtrActivity.getCompanyContext</span><span class="sxs-lookup"><span data-stu-id="0bbb6-608">Table WrkCtrActivity.getCompanyContext</span></span>|
|<span data-ttu-id="0bbb6-609">Tax.insertLineInInternal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-609">Tax.insertLineInInternal</span></span>|
|<span data-ttu-id="0bbb6-610">TransactionReversal_Cust.fld900_1_modified</span><span class="sxs-lookup"><span data-stu-id="0bbb6-610">TransactionReversal_Cust.fld900_1_modified</span></span>|
|<span data-ttu-id="0bbb6-611">whsLoadTemplateAssignmentForm: WHSLoadTable::clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-611">whsLoadTemplateAssignmentForm: WHSLoadTable::clicked</span></span>|
|<span data-ttu-id="0bbb6-612">WhsWorkExecuteDisplay.getNextFormState</span><span class="sxs-lookup"><span data-stu-id="0bbb6-612">WhsWorkExecuteDisplay.getNextFormState</span></span>|
|<span data-ttu-id="0bbb6-613">WHSWorkExecuteDisplay.setBatchDetails</span><span class="sxs-lookup"><span data-stu-id="0bbb6-613">WHSWorkExecuteDisplay.setBatchDetails</span></span>|
|<span data-ttu-id="0bbb6-614">WhsWorkExecuteDisplayReturnOrder.buildReturnOrder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-614">WhsWorkExecuteDisplayReturnOrder.buildReturnOrder</span></span>|
|<span data-ttu-id="0bbb6-615">WhsWorkExecuteDisplayReturnOrder.displayForm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-615">WhsWorkExecuteDisplayReturnOrder.displayForm</span></span>|

## <a name="changes-using-other-methods-to-support-extensibility"></a><span data-ttu-id="0bbb6-616">拡張性をサポートするための他の方法を使用した変更</span><span class="sxs-lookup"><span data-stu-id="0bbb6-616">Changes using other methods to support extensibility</span></span>

<span data-ttu-id="0bbb6-617">このセクションの変更のグループには、いくつかの異なる拡張機能のアプローチが含まれており、**コマンド チェーン** が導入される前の行われた拡張機能の変更を表しています。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-617">The group of changes in this section includes several different approaches to extensibility and represents the extensibilty changes made before **Chain of Command** was introduced.</span></span> <span data-ttu-id="0bbb6-618">使用されるアプローチの一部は、メソッドの抽出、"スタブ" メソッドの追加、デリゲートの追加、メソッドでのアクセス修飾子の変更、SysExtension フレームワークの使用を行います。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-618">Some of the approaches used are extracting methods, adding "stub" methods, adding delegates, changing access modifiers on methods, and using the SysExtension framework.</span></span> <span data-ttu-id="0bbb6-619">実行したアプローチがカスタマイズで機能するかどうかを判断するには、カスタマイズに必要な所定の場所の実装を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-619">Please consult the implementation in places required for your customization to determine if the approach taken will work for your customization.</span></span> <span data-ttu-id="0bbb6-620">今後のリリースで、主に**コマンド チェーン**を使用するため、このグループは小さくなります。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-620">In future releases, this group will be small, because we will primarily be using **Chain of Command**.</span></span>

| <span data-ttu-id="0bbb6-621">方法</span><span class="sxs-lookup"><span data-stu-id="0bbb6-621">Method</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-622">AccDistRuleSaleOfProductExtendedPrice.parmLedgerDimensionAllocList</span><span class="sxs-lookup"><span data-stu-id="0bbb6-622">AccDistRuleSaleOfProductExtendedPrice.parmLedgerDimensionAllocList</span></span>|
|<span data-ttu-id="0bbb6-623">AssetPost.createInventorySoldTransaction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-623">AssetPost.createInventorySoldTransaction</span></span>|
|<span data-ttu-id="0bbb6-624">AssetSplit.validate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-624">AssetSplit.validate</span></span>|
|<span data-ttu-id="0bbb6-625">AxSalesLine.doSave</span><span class="sxs-lookup"><span data-stu-id="0bbb6-625">AxSalesLine.doSave</span></span>|
|<span data-ttu-id="0bbb6-626">AxSalesLine.setLineAmount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-626">AxSalesLine.setLineAmount</span></span>|
|<span data-ttu-id="0bbb6-627">AxSalesQuotationLine.setLineAmount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-627">AxSalesQuotationLine.setLineAmount</span></span>|
|<span data-ttu-id="0bbb6-628">BankPaymCancel.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-628">BankPaymCancel.main</span></span>|
|<span data-ttu-id="0bbb6-629">BankPaymCancel.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-629">BankPaymCancel.run</span></span>|
|<span data-ttu-id="0bbb6-630">BankPaymCancel.serverRun</span><span class="sxs-lookup"><span data-stu-id="0bbb6-630">BankPaymCancel.serverRun</span></span>|
|<span data-ttu-id="0bbb6-631">BomCalcJob.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-631">BomCalcJob.main</span></span>|
|<span data-ttu-id="0bbb6-632">CustCollectionLetterCancel.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-632">CustCollectionLetterCancel.main</span></span>|
|<span data-ttu-id="0bbb6-633">CustCollectionLetterCancel.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-633">CustCollectionLetterCancel.run</span></span>|
|<span data-ttu-id="0bbb6-634">CustCollectionLetterCreate.checkCustTransOpen</span><span class="sxs-lookup"><span data-stu-id="0bbb6-634">CustCollectionLetterCreate.checkCustTransOpen</span></span>|
|<span data-ttu-id="0bbb6-635">CustCollectionLetterCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-635">CustCollectionLetterCreate.createJournal</span></span>|
|<span data-ttu-id="0bbb6-636">CustCollectionLetterPost.updateFee</span><span class="sxs-lookup"><span data-stu-id="0bbb6-636">CustCollectionLetterPost.updateFee</span></span>|
|<span data-ttu-id="0bbb6-637">CustCollectionLetterPost.validate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-637">CustCollectionLetterPost.validate</span></span>|
|<span data-ttu-id="0bbb6-638">CustCollectionsExcelStatement.setTransactionWorksheetRow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-638">CustCollectionsExcelStatement.setTransactionWorksheetRow</span></span>|
|<span data-ttu-id="0bbb6-639">CustInterestCancel.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-639">CustInterestCancel.run</span></span>|
|<span data-ttu-id="0bbb6-640">CustInterestCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-640">CustInterestCreate</span></span>|
|<span data-ttu-id="0bbb6-641">CustInterestCreate.dialog</span><span class="sxs-lookup"><span data-stu-id="0bbb6-641">CustInterestCreate.dialog</span></span>|
|<span data-ttu-id="0bbb6-642">CustInterestCreate.runOnce</span><span class="sxs-lookup"><span data-stu-id="0bbb6-642">CustInterestCreate.runOnce</span></span>|
|<span data-ttu-id="0bbb6-643">CustInterestHelper.getFeeLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-643">CustInterestHelper.getFeeLedgerAccount</span></span>|
|<span data-ttu-id="0bbb6-644">CustInterestHelper.getVerDetailLedgerDimensionByIntTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-644">CustInterestHelper.getVerDetailLedgerDimensionByIntTrans</span></span>|
|<span data-ttu-id="0bbb6-645">CustInterestPost.postVoucher</span><span class="sxs-lookup"><span data-stu-id="0bbb6-645">CustInterestPost.postVoucher</span></span>|
|<span data-ttu-id="0bbb6-646">CustInterestPost.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-646">CustInterestPost.run</span></span>|
|<span data-ttu-id="0bbb6-647">CustInterestPost.updateFee</span><span class="sxs-lookup"><span data-stu-id="0bbb6-647">CustInterestPost.updateFee</span></span>|
|<span data-ttu-id="0bbb6-648">CustInterestPost.validateInterestTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-648">CustInterestPost.validateInterestTrans</span></span>|
|<span data-ttu-id="0bbb6-649">CustInvoiceSpecDP::insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-649">CustInvoiceSpecDP::insertIntoTempTable</span></span>|
|<span data-ttu-id="0bbb6-650">CustOutPaymControlController.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-650">CustOutPaymControlController.init</span></span>|
|<span data-ttu-id="0bbb6-651">CustPostInvoiceJob.custPostInvoiceUpdate()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-651">CustPostInvoiceJob.custPostInvoiceUpdate()</span></span>|
|<span data-ttu-id="0bbb6-652">CustSettlementPriorityProcessing</span><span class="sxs-lookup"><span data-stu-id="0bbb6-652">CustSettlementPriorityProcessing</span></span>|
|<span data-ttu-id="0bbb6-653">CustSettlementPriorityProcessing.markAllSelected</span><span class="sxs-lookup"><span data-stu-id="0bbb6-653">CustSettlementPriorityProcessing.markAllSelected</span></span>|
|<span data-ttu-id="0bbb6-654">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span><span class="sxs-lookup"><span data-stu-id="0bbb6-654">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span></span>|
|<span data-ttu-id="0bbb6-655">CustVendCreatePaymJournal.initBalances</span><span class="sxs-lookup"><span data-stu-id="0bbb6-655">CustVendCreatePaymJournal.initBalances</span></span>|
|<span data-ttu-id="0bbb6-656">CustVendOpenTransManager::updateOriginatorForMarkedTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-656">CustVendOpenTransManager::updateOriginatorForMarkedTrans</span></span>|
|<span data-ttu-id="0bbb6-657">CustVendPaymProposalCalcPaym.calcPaymDueDate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-657">CustVendPaymProposalCalcPaym.calcPaymDueDate</span></span>|
|<span data-ttu-id="0bbb6-658">CustVendReversePosting.updateNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-658">CustVendReversePosting.updateNow</span></span>|
|<span data-ttu-id="0bbb6-659">CustVendSettle.mustOffsetOriginalSummaryDistributions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-659">CustVendSettle.mustOffsetOriginalSummaryDistributions</span></span>|
|<span data-ttu-id="0bbb6-660">CustVendVoucher.initLedgerPosting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-660">CustVendVoucher.initLedgerPosting</span></span>|
|<span data-ttu-id="0bbb6-661">DimensionDerivationRule.buildDimensionCombination</span><span class="sxs-lookup"><span data-stu-id="0bbb6-661">DimensionDerivationRule.buildDimensionCombination</span></span>|
|<span data-ttu-id="0bbb6-662">DimensionDerivationRule.initialize</span><span class="sxs-lookup"><span data-stu-id="0bbb6-662">DimensionDerivationRule.initialize</span></span>|
|<span data-ttu-id="0bbb6-663">EcoResProductReleaseManager.release</span><span class="sxs-lookup"><span data-stu-id="0bbb6-663">EcoResProductReleaseManager.release</span></span>|
|<span data-ttu-id="0bbb6-664">EcoResProductReleaseSessionBatch.runJob</span><span class="sxs-lookup"><span data-stu-id="0bbb6-664">EcoResProductReleaseSessionBatch.runJob</span></span>|
|<span data-ttu-id="0bbb6-665">EcoResProductReleaseSessionManager.executeOnServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-665">EcoResProductReleaseSessionManager.executeOnServer</span></span>|
|<span data-ttu-id="0bbb6-666">EcoResProductVariantCreationMgr.buildVariantSuggestions()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-666">EcoResProductVariantCreationMgr.buildVariantSuggestions()</span></span>|
|<span data-ttu-id="0bbb6-667">フォーム BankPaymCancel.closeOK</span><span class="sxs-lookup"><span data-stu-id="0bbb6-667">Form BankPaymCancel.closeOK</span></span>|
|<span data-ttu-id="0bbb6-668">フォーム BOMChangeLine.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-668">Form BOMChangeLine.init</span></span>|
|<span data-ttu-id="0bbb6-669">フォーム BOMConsistOf: BOMCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-669">Form BOMConsistOf: BOMCreate</span></span>|
|<span data-ttu-id="0bbb6-670">フォーム ConfigPartOf: EcoResConfiguration</span><span class="sxs-lookup"><span data-stu-id="0bbb6-670">Form ConfigPartOf: EcoResConfiguration</span></span>|
|<span data-ttu-id="0bbb6-671">フォーム CustBankAccounts.write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-671">Form CustBankAccounts.write</span></span>|
|<span data-ttu-id="0bbb6-672">フォーム CustCollections.showAgingIndicator</span><span class="sxs-lookup"><span data-stu-id="0bbb6-672">Form CustCollections.showAgingIndicator</span></span>|
|<span data-ttu-id="0bbb6-673">フォーム CustOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-673">Form CustOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="0bbb6-674">フォーム CustOpenTrans.updateDesignStatic</span><span class="sxs-lookup"><span data-stu-id="0bbb6-674">Form CustOpenTrans.updateDesignStatic</span></span>|
|<span data-ttu-id="0bbb6-675">フォーム CustPaymEntry.editIsMarkedForSettlement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-675">Form CustPaymEntry.editIsMarkedForSettlement</span></span>|
|<span data-ttu-id="0bbb6-676">フォーム CustPaymEntry.write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-676">Form CustPaymEntry.write</span></span>|
|<span data-ttu-id="0bbb6-677">フォーム CustSettlementPrioritySetup.active</span><span class="sxs-lookup"><span data-stu-id="0bbb6-677">Form CustSettlementPrioritySetup.active</span></span>|
|<span data-ttu-id="0bbb6-678">フォーム CustTable.PrintManagement.clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-678">Form CustTable.PrintManagement.clicked</span></span>|
|<span data-ttu-id="0bbb6-679">フォーム EcoResProductImage.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-679">Form EcoResProductImage.init</span></span>|
|<span data-ttu-id="0bbb6-680">フォーム EcoResProductImage.setProductRecId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-680">Form EcoResProductImage.setProductRecId</span></span>|
|<span data-ttu-id="0bbb6-681">フォーム HRMAbsenceRequest.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-681">Form HRMAbsenceRequest.init</span></span>|
|<span data-ttu-id="0bbb6-682">フォーム LedgerJournalTransAccrual.enableFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-682">Form LedgerJournalTransAccrual.enableFields</span></span>|
|<span data-ttu-id="0bbb6-683">フォーム LedgerJournalTransAccrual.LedgerJournalTransAccrual.clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-683">Form LedgerJournalTransAccrual.LedgerJournalTransAccrual.clicked</span></span>|
|<span data-ttu-id="0bbb6-684">フォーム LedgerJournalTransCustPaym: LedgerJournalTrans.active</span><span class="sxs-lookup"><span data-stu-id="0bbb6-684">Form LedgerJournalTransCustPaym: LedgerJournalTrans.active</span></span>|
|<span data-ttu-id="0bbb6-685">フォーム LedgerJournalTransDaily: SettlementButton.clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-685">Form LedgerJournalTransDaily: SettlementButton.clicked</span></span>|
|<span data-ttu-id="0bbb6-686">フォーム LedgerJournalTransDimension.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-686">Form LedgerJournalTransDimension.init</span></span>|
|<span data-ttu-id="0bbb6-687">フォーム MarkupTable.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-687">Form MarkupTable.init</span></span>|
|<span data-ttu-id="0bbb6-688">フォーム MCRItemListCopying.copyLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-688">Form MCRItemListCopying.copyLines</span></span>|
|<span data-ttu-id="0bbb6-689">フォーム PCProductModelVersion</span><span class="sxs-lookup"><span data-stu-id="0bbb6-689">Form PCProductModelVersion</span></span>|
|<span data-ttu-id="0bbb6-690">フォーム ProjInvoiceProposalCreateLines.modifiedTransFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-690">Form ProjInvoiceProposalCreateLines.modifiedTransFilter</span></span>|
|<span data-ttu-id="0bbb6-691">フォーム ProjTransItem: ProjItemTrans.salesAmount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-691">Form ProjTransItem: ProjItemTrans.salesAmount</span></span>|
|<span data-ttu-id="0bbb6-692">フォーム PurchCreateFromSalesOrder.SalesLine.included</span><span class="sxs-lookup"><span data-stu-id="0bbb6-692">Form PurchCreateFromSalesOrder.SalesLine.included</span></span>|
|<span data-ttu-id="0bbb6-693">フォーム ReqItemTable.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-693">Form ReqItemTable.init</span></span>|
|<span data-ttu-id="0bbb6-694">フォーム SalesCopying.canClose</span><span class="sxs-lookup"><span data-stu-id="0bbb6-694">Form SalesCopying.canClose</span></span>|
|<span data-ttu-id="0bbb6-695">フォーム SalesCreateQuotation.setFieldsActive</span><span class="sxs-lookup"><span data-stu-id="0bbb6-695">Form SalesCreateQuotation.setFieldsActive</span></span>|
|<span data-ttu-id="0bbb6-696">フォーム SalesQuotationTable.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-696">Form SalesQuotationTable.init</span></span>|
|<span data-ttu-id="0bbb6-697">フォーム SalesTable: SalesLine.write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-697">Form SalesTable: SalesLine.write</span></span>|
|<span data-ttu-id="0bbb6-698">フォーム SalesTable: SalesLine_DS.ItemId.lookup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-698">Form SalesTable: SalesLine_DS.ItemId.lookup</span></span>|
|<span data-ttu-id="0bbb6-699">フォーム: VendEditInvoice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-699">Form: VendEditInvoice</span></span>|
|<span data-ttu-id="0bbb6-700">FormletterJournalPos::newPostSales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-700">FormletterJournalPos::newPostSales</span></span>|
|<span data-ttu-id="0bbb6-701">FormLetterJournalPost.post</span><span class="sxs-lookup"><span data-stu-id="0bbb6-701">FormLetterJournalPost.post</span></span>|
|<span data-ttu-id="0bbb6-702">FormletterService.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-702">FormletterService.run</span></span>|
|<span data-ttu-id="0bbb6-703">ProjTable.init から</span><span class="sxs-lookup"><span data-stu-id="0bbb6-703">From ProjTable.init</span></span>|
|<span data-ttu-id="0bbb6-704">HierarchyTemplateCopying.copyHierachy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-704">HierarchyTemplateCopying.copyHierarchy</span></span>|
|<span data-ttu-id="0bbb6-705">HrmAbsenceRequestAction.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-705">HrmAbsenceRequestAction.run</span></span>|
|<span data-ttu-id="0bbb6-706">InterCompanyUpdateRemPhys_PurchLine::synchronizeExternal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-706">InterCompanyUpdateRemPhys_PurchLine::synchronizeExternal</span></span>|
|<span data-ttu-id="0bbb6-707">InterCompanyUpdateRemPhys_PurchLine::synchronizeInternal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-707">InterCompanyUpdateRemPhys_PurchLine::synchronizeInternal</span></span>|
|<span data-ttu-id="0bbb6-708">InterCompanyUpdateStatus_PurchLine::synchronizeExternal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-708">InterCompanyUpdateStatus_PurchLine::synchronizeExternal</span></span>|
|<span data-ttu-id="0bbb6-709">InterCompanyUpdateStatus_PurchLine::synchronizeInternal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-709">InterCompanyUpdateStatus_PurchLine::synchronizeInternal</span></span>|
|<span data-ttu-id="0bbb6-710">IntrastatTransfer::calcCustVendInvoiceTransQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-710">IntrastatTransfer::calcCustVendInvoiceTransQty</span></span>|
|<span data-ttu-id="0bbb6-711">InventDim::dimReportStr</span><span class="sxs-lookup"><span data-stu-id="0bbb6-711">InventDim::dimReportStr</span></span>|
|<span data-ttu-id="0bbb6-712">InventMov_Transfer::checkUpdateEstimated</span><span class="sxs-lookup"><span data-stu-id="0bbb6-712">InventMov_Transfer::checkUpdateEstimated</span></span>|
|<span data-ttu-id="0bbb6-713">InventMov_Transfer::defaultDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-713">InventMov_Transfer::defaultDimension</span></span>|
|<span data-ttu-id="0bbb6-714">InventMovement::checkNotSubDelivery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-714">InventMovement::checkNotSubDelivery</span></span>|
|<span data-ttu-id="0bbb6-715">InventQualityManagementCreate.createQualityOrder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-715">InventQualityManagementCreate.createQualityOrder</span></span>|
|<span data-ttu-id="0bbb6-716">InventTransferParmLine::createShipLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-716">InventTransferParmLine::createShipLines</span></span>|
|<span data-ttu-id="0bbb6-717">InventTransferParmLine::initFromInventTransferParmTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-717">InventTransferParmLine::initFromInventTransferParmTable</span></span>|
|<span data-ttu-id="0bbb6-718">InventTransferUpdShi::updateInventTransferLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-718">InventTransferUpdShip::updateInventTransferLine</span></span>|
|<span data-ttu-id="0bbb6-719">InventUpd_Estimated::createEstimatedInventTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-719">InventUpd_Estimated::createEstimatedInventTrans</span></span>|
|<span data-ttu-id="0bbb6-720">InventUpd_Financial::newInventTransferLineReceive</span><span class="sxs-lookup"><span data-stu-id="0bbb6-720">InventUpd_Financial::newInventTransferLineReceive</span></span>|
|<span data-ttu-id="0bbb6-721">InventUpd_Financial::newInventTransferLineShip</span><span class="sxs-lookup"><span data-stu-id="0bbb6-721">InventUpd_Financial::newInventTransferLineShip</span></span>|
|<span data-ttu-id="0bbb6-722">InventUpd_Financia::updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-722">InventUpd_Financial::updateFinancialIssue</span></span>|
|<span data-ttu-id="0bbb6-723">InventUpd_Financial::updateFinancialReceipt</span><span class="sxs-lookup"><span data-stu-id="0bbb6-723">InventUpd_Financial::updateFinancialReceipt</span></span>|
|<span data-ttu-id="0bbb6-724">InventUpd_Physical::newInventMovement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-724">InventUpd_Physical::newInventMovement</span></span>|
|<span data-ttu-id="0bbb6-725">InventUpd_Reservation::updateReserveBuffer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-725">InventUpd_Reservation::updateReserveBuffer</span></span>|
|<span data-ttu-id="0bbb6-726">InventUpd_Reservation::updateReserveFromForm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-726">InventUpd_Reservation::updateReserveFromForm</span></span>|
|<span data-ttu-id="0bbb6-727">InventUpdate::whsUpdateDimReservePhysical</span><span class="sxs-lookup"><span data-stu-id="0bbb6-727">InventUpdate::whsUpdateDimReservePhysical</span></span>|
|<span data-ttu-id="0bbb6-728">InventUpdate::whsUpdateWorkTransDimIssue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-728">InventUpdate::whsUpdateWorkTransDimIssue</span></span>|
|<span data-ttu-id="0bbb6-729">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-729">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="0bbb6-730">LedgerJournalEngine - メソッド preDelete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-730">LedgerJournalEngine - method preDelete</span></span>|
|<span data-ttu-id="0bbb6-731">LedgerJournalEngin::findSettledAmount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-731">LedgerJournalEngine::findSettledAmount</span></span>|
|<span data-ttu-id="0bbb6-732">LedgerJournalEngine_CustPayment.allowEditTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-732">LedgerJournalEngine_CustPayment.allowEditTrans</span></span>|
|<span data-ttu-id="0bbb6-733">LedgerJournalEngine_CustPayment.initDefaultDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-733">LedgerJournalEngine_CustPayment.initDefaultDimension</span></span>|
|<span data-ttu-id="0bbb6-734">LedgerJournalEngine_CustPayment.write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-734">LedgerJournalEngine_CustPayment.write</span></span>|
|<span data-ttu-id="0bbb6-735">LedgerJournalFormTable.verifyCanDelete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-735">LedgerJournalFormTable.verifyCanDelete</span></span>|
|<span data-ttu-id="0bbb6-736">LedgerVoucherTransObject.newTransLedgerJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-736">LedgerVoucherTransObject.newTransLedgerJournal</span></span>|
|<span data-ttu-id="0bbb6-737">LogisticsPostalAddressFormHandler.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-737">LogisticsPostalAddressFormHandler.main</span></span>|
|<span data-ttu-id="0bbb6-738">マップ SalesPurchLine.calcPrice2LineAmount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-738">Map SalesPurchLine.calcPrice2LineAmount</span></span>|
|<span data-ttu-id="0bbb6-739">マップ SalesPurchLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-739">Map SalesPurchLine.setPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-740">Markup.calc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-740">Markup.calc</span></span>|
|<span data-ttu-id="0bbb6-741">MarkupAdjustment::main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-741">MarkupAdjustment::main</span></span>|
|<span data-ttu-id="0bbb6-742">McrPriceHistoryForm.insertPotentialTradeAgreements</span><span class="sxs-lookup"><span data-stu-id="0bbb6-742">McrPriceHistoryForm.insertPotentialTradeAgreements</span></span>|
|<span data-ttu-id="0bbb6-743">OffsetVoucherCust.updateNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-743">OffsetVoucherCust.updateNow</span></span>|
|<span data-ttu-id="0bbb6-744">PcGenerateBOMTableAndVersion.generate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-744">PcGenerateBOMTableAndVersion.generate</span></span>|
|<span data-ttu-id="0bbb6-745">PriceDisc.findDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-745">PriceDisc.findDisc</span></span>|
|<span data-ttu-id="0bbb6-746">PriceDisc::findItemLineDiscAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-746">PriceDisc::findItemLineDiscAgreement</span></span>|
|<span data-ttu-id="0bbb6-747">PriceDisc::findItemPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-747">PriceDisc::findItemPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-748">PriceDisc::findMultiLineDiscServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-748">PriceDisc::findMultiLineDiscServer</span></span>|
|<span data-ttu-id="0bbb6-749">PriceDisc::newFromPriceDiscHeading</span><span class="sxs-lookup"><span data-stu-id="0bbb6-749">PriceDisc::newFromPriceDiscHeading</span></span>|
|<span data-ttu-id="0bbb6-750">PriceDisc_LineDisc::findLineDiscAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-750">PriceDisc_LineDisc::findLineDiscAgreement</span></span>|
|<span data-ttu-id="0bbb6-751">PriceDisc_Price::findPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-751">PriceDisc_Price::findPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-752">PriceDiscAdmCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-752">PriceDiscAdmCheckPost.checkJournal</span></span>|
|<span data-ttu-id="0bbb6-753">PrintMgmtHierarchy_Project.getParentImplementation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-753">PrintMgmtHierarchy_Project.getParentImplementation</span></span>|
|<span data-ttu-id="0bbb6-754">ProjAdjustmentSplit.createNewTrans.getNewTotalCostAmount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-754">ProjAdjustmentSplit.createNewTrans.getNewTotalCostAmount</span></span>|
|<span data-ttu-id="0bbb6-755">ProjInvoiceJournalPost.createProjInvoiceRevenue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-755">ProjInvoiceJournalPost.createProjInvoiceRevenue</span></span>|
|<span data-ttu-id="0bbb6-756">ProjInvoiceProposalInsertLines.doSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-756">ProjInvoiceProposalInsertLines.doSalesLine</span></span>|
|<span data-ttu-id="0bbb6-757">ProjPost.postCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-757">ProjPost.postCost</span></span>|
|<span data-ttu-id="0bbb6-758">ProjPostCostJournal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-758">ProjPostCostJournal.projTransCreate</span></span>|
|<span data-ttu-id="0bbb6-759">ProjPostCostTrans_AdjNeg.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-759">ProjPostCostTrans_AdjNeg.projTransCreate</span></span>|
|<span data-ttu-id="0bbb6-760">PurchAutoCreate_PurchReq.prepareSort</span><span class="sxs-lookup"><span data-stu-id="0bbb6-760">PurchAutoCreate_PurchReq.prepareSort</span></span>|
|<span data-ttu-id="0bbb6-761">PurchCalcItem.initListBOM</span><span class="sxs-lookup"><span data-stu-id="0bbb6-761">PurchCalcItem.initListBOM</span></span>|
|<span data-ttu-id="0bbb6-762">PurchFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-762">PurchFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="0bbb6-763">PurchFormLetterParmData::newChooseLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-763">PurchFormLetterParmData::newChooseLines</span></span>|
|<span data-ttu-id="0bbb6-764">PurchFormletterParmDataInvoice.createParmLineAndSubLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-764">PurchFormletterParmDataInvoice.createParmLineAndSubLines</span></span>|
|<span data-ttu-id="0bbb6-765">PurchInvoiceJournalPost.checkSourceLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-765">PurchInvoiceJournalPost.checkSourceLine</span></span>|
|<span data-ttu-id="0bbb6-766">PurchInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="0bbb6-766">PurchInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="0bbb6-767">PurchInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-767">PurchInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="0bbb6-768">PurchLineType.initDimensionsSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-768">PurchLineType.initDimensionsSpecificDefaulting</span></span>|
|<span data-ttu-id="0bbb6-769">PurchLineType.interCompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-769">PurchLineType.interCompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-770">ReqCalcExplodeSales.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-770">ReqCalcExplodeSales.run</span></span>|
|<span data-ttu-id="0bbb6-771">SalesAutoCreate_ReleaseOrder.createSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-771">SalesAutoCreate_ReleaseOrder.createSalesLine</span></span>|
|<span data-ttu-id="0bbb6-772">SalesConfirmDP::createData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-772">SalesConfirmDP::createData</span></span>|
|<span data-ttu-id="0bbb6-773">SalesConfirmDP::printDimHistory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-773">SalesConfirmDP::printDimHistory</span></span>|
|<span data-ttu-id="0bbb6-774">SalesConfirmDP::setSalesConfirmDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-774">SalesConfirmDP::setSalesConfirmDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-775">SalesCopying.copy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-775">SalesCopying.copy</span></span>|
|<span data-ttu-id="0bbb6-776">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-776">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="0bbb6-777">SalesFormletterParmData.calcAutomaticTotalDiscount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-777">SalesFormletterParmData.calcAutomaticTotalDiscount</span></span>|
|<span data-ttu-id="0bbb6-778">SalesFormletterParmDataPickingList.insertParmLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-778">SalesFormletterParmDataPickingList.insertParmLine</span></span>|
|<span data-ttu-id="0bbb6-779">SalesInvoiceController::main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-779">SalesInvoiceController::main</span></span>|
|<span data-ttu-id="0bbb6-780">SalesInvoiceDP.insertIntoSalesInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-780">SalesInvoiceDP.insertIntoSalesInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-781">SalesInvoiceD::PinsertIntoSalesInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-781">SalesInvoiceDP::insertIntoSalesInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-782">SalesInvoiceDP::loadCustPackingSlipTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-782">SalesInvoiceDP::loadCustPackingSlipTrans</span></span>|
|<span data-ttu-id="0bbb6-783">SalesInvoiceDPBase::createData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-783">SalesInvoiceDPBase::createData</span></span>|
|<span data-ttu-id="0bbb6-784">SalesInvoiceJournalCreate::initInvoiceLineFromSourceLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-784">SalesInvoiceJournalCreate::initInvoiceLineFromSourceLine</span></span>|
|<span data-ttu-id="0bbb6-785">SalesInvoiceJournalPost::postCustVend</span><span class="sxs-lookup"><span data-stu-id="0bbb6-785">SalesInvoiceJournalPost::postCustVend</span></span>|
|<span data-ttu-id="0bbb6-786">SalesLine::initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-786">SalesLine::initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="0bbb6-787">SalesLineType.initDimensionsSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-787">SalesLineType.initDimensionsSpecificDefaulting</span></span>|
|<span data-ttu-id="0bbb6-788">SalesLineType.interCompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-788">SalesLineType.interCompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-789">SalesLineType::checkDelete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-789">SalesLineType::checkDelete</span></span>|
|<span data-ttu-id="0bbb6-790">SalesLineType::delete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-790">SalesLineType::delete</span></span>|
|<span data-ttu-id="0bbb6-791">SalesLineType::insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-791">SalesLineType::insert</span></span>|
|<span data-ttu-id="0bbb6-792">SalesLineType::interCompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-792">SalesLineType::interCompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-793">SalesLineType::setSalesStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-793">SalesLineType::setSalesStatus</span></span>|
|<span data-ttu-id="0bbb6-794">SalesLineType::update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-794">SalesLineType::update</span></span>|
|<span data-ttu-id="0bbb6-795">SalesLineType::validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-795">SalesLineType::validateWrite</span></span>|
|<span data-ttu-id="0bbb6-796">SalesPickingListJournalCreate::createJournalLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-796">SalesPickingListJournalCreate::createJournalLine</span></span>|
|<span data-ttu-id="0bbb6-797">SalesQuotationConfirmationDP::processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-797">SalesQuotationConfirmationDP::processReport</span></span>|
|<span data-ttu-id="0bbb6-798">SalesQuotationCopying.copy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-798">SalesQuotationCopying.copy</span></span>|
|<span data-ttu-id="0bbb6-799">SalesQuotationDP::processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-799">SalesQuotationDP::processReport</span></span>|
|<span data-ttu-id="0bbb6-800">SalesQuotationLine.modifySalesQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-800">SalesQuotationLine.modifySalesQty</span></span>|
|<span data-ttu-id="0bbb6-801">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-801">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="0bbb6-802">SalesQuotationToLineField.getFieldDescription</span><span class="sxs-lookup"><span data-stu-id="0bbb6-802">SalesQuotationToLineField.getFieldDescription</span></span>|
|<span data-ttu-id="0bbb6-803">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-803">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="0bbb6-804">SalesTableListPageInteraction.setButtonInterCompany</span><span class="sxs-lookup"><span data-stu-id="0bbb6-804">SalesTableListPageInteraction.setButtonInterCompany</span></span>|
|<span data-ttu-id="0bbb6-805">SalesTableListPageInteraction.setButtonInvoice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-805">SalesTableListPageInteraction.setButtonInvoice</span></span>|
|<span data-ttu-id="0bbb6-806">SalesTableListPageInteraction.setButtonPickAndPack</span><span class="sxs-lookup"><span data-stu-id="0bbb6-806">SalesTableListPageInteraction.setButtonPickAndPack</span></span>|
|<span data-ttu-id="0bbb6-807">SalesUpdateRemain</span><span class="sxs-lookup"><span data-stu-id="0bbb6-807">SalesUpdateRemain</span></span>|
|<span data-ttu-id="0bbb6-808">SalesUpdateRemain::updateDeliveryRemainder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-808">SalesUpdateRemain::updateDeliveryRemainder</span></span>|
|<span data-ttu-id="0bbb6-809">smmActivityCreate.setup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-809">smmActivityCreate.setup</span></span>|
|<span data-ttu-id="0bbb6-810">smmAttendeeTable.insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-810">smmAttendeeTable.insert</span></span>|
|<span data-ttu-id="0bbb6-811">smmSalesCustItemStatisticsDP::processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-811">smmSalesCustItemStatisticsDP::processReport</span></span>|
|<span data-ttu-id="0bbb6-812">SpecTransManager.updateFullSettlement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-812">SpecTransManager.updateFullSettlement</span></span>|
|<span data-ttu-id="0bbb6-813">SubledgerJournalizer.loadAccDistTmpRelieveAccrual</span><span class="sxs-lookup"><span data-stu-id="0bbb6-813">SubledgerJournalizer.loadAccDistTmpRelieveAccrual</span></span>|
|<span data-ttu-id="0bbb6-814">SubledgerJournalizer.loadaccountingDistributionTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-814">SubledgerJournalizer.loadaccountingDistributionTmp</span></span>|
|<span data-ttu-id="0bbb6-815">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span><span class="sxs-lookup"><span data-stu-id="0bbb6-815">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span></span>|
|<span data-ttu-id="0bbb6-816">SubledgerJournalizer.recordSubledgerJournalAccountEntries</span><span class="sxs-lookup"><span data-stu-id="0bbb6-816">SubledgerJournalizer.recordSubledgerJournalAccountEntries</span></span>|
|<span data-ttu-id="0bbb6-817">SubLedgerJournalTransferUIBuilder::build</span><span class="sxs-lookup"><span data-stu-id="0bbb6-817">SubLedgerJournalTransferUIBuilder::build</span></span>|
|<span data-ttu-id="0bbb6-818">SuppItemCreate_SalesQuotation::createLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-818">SuppItemCreate_SalesQuotation::createLine</span></span>|
|<span data-ttu-id="0bbb6-819">テーブル - PurchLine.Insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-819">Table - PurchLine.Insert</span></span>|
|<span data-ttu-id="0bbb6-820">テーブル - PurchLine.Update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-820">Table - PurchLine.Update</span></span>|
|<span data-ttu-id="0bbb6-821">テーブル CostingVersion.validateField</span><span class="sxs-lookup"><span data-stu-id="0bbb6-821">Table CostingVersion.validateField</span></span>|
|<span data-ttu-id="0bbb6-822">テーブル CustBankAccount.lookupBankAccount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-822">Table CustBankAccount.lookupBankAccount</span></span>|
|<span data-ttu-id="0bbb6-823">テーブル CustCollectionLetterJour.cancelCollectionLetterCodeCustTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-823">Table CustCollectionLetterJour.cancelCollectionLetterCodeCustTrans</span></span>|
|<span data-ttu-id="0bbb6-824">テーブル CustInterestJour.feeLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-824">Table CustInterestJour.feeLedgerDimension</span></span>|
|<span data-ttu-id="0bbb6-825">テーブル CustInvoiceTable - メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-825">Table CustInvoiceTable - method validateWrite</span></span>|
|<span data-ttu-id="0bbb6-826">テーブル CustTable.blocked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-826">Table CustTable.blocked</span></span>|
|<span data-ttu-id="0bbb6-827">テーブル CustTrans.reverseTransact</span><span class="sxs-lookup"><span data-stu-id="0bbb6-827">Table CustTrans.reverseTransact</span></span>|
|<span data-ttu-id="0bbb6-828">テーブル InventNonConformanceTable.setEditableFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-828">Table InventNonConformanceTable.setEditableFields</span></span>|
|<span data-ttu-id="0bbb6-829">テーブル InventPosting.accountItemLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-829">Table InventPosting.accountItemLedgerDimension</span></span>|
|<span data-ttu-id="0bbb6-830">テーブル InventTable.updateAutoSalesPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-830">Table InventTable.updateAutoSalesPrice</span></span>|
|<span data-ttu-id="0bbb6-831">テーブル InventTestAssociationTable.checkDocumentType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-831">Table InventTestAssociationTable.checkDocumentType</span></span>|
|<span data-ttu-id="0bbb6-832">テーブル InventTrans.accountLossProfitLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-832">Table InventTrans.accountLossProfitLedgerDimension</span></span>|
|<span data-ttu-id="0bbb6-833">テーブル LedgerJournalTrans.checkVATNumJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-833">Table LedgerJournalTrans.checkVATNumJournal</span></span>|
|<span data-ttu-id="0bbb6-834">テーブル MarkupTrans.checkMarkCode</span><span class="sxs-lookup"><span data-stu-id="0bbb6-834">Table MarkupTrans.checkMarkCode</span></span>|
|<span data-ttu-id="0bbb6-835">テーブル PurchLine.convertCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="0bbb6-835">Table PurchLine.convertCurrencyCode</span></span>|
|<span data-ttu-id="0bbb6-836">テーブル ReqPO.validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-836">Table ReqPO.validateWrite</span></span>|
|<span data-ttu-id="0bbb6-837">テーブル SalesLine.checkAndUpdateLoadLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-837">Table SalesLine.checkAndUpdateLoadLines</span></span>|
|<span data-ttu-id="0bbb6-838">テーブル SalesLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-838">Table SalesLine.setPriceDisc</span></span>|
|<span data-ttu-id="0bbb6-839">テーブル SalesQuotationLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-839">Table SalesQuotationLine.setPriceDisc</span></span>|
|<span data-ttu-id="0bbb6-840">テーブル SalesTable.createMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-840">Table SalesTable.createMarkupTrans</span></span>|
|<span data-ttu-id="0bbb6-841">テーブル TmpInventTransMark.updateTmpMark</span><span class="sxs-lookup"><span data-stu-id="0bbb6-841">Table TmpInventTransMark.updateTmpMark</span></span>|
|<span data-ttu-id="0bbb6-842">テーブル TMSAppointment.validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-842">Table TMSAppointment.validateWrite</span></span>|
|<span data-ttu-id="0bbb6-843">テーブル WHSLoadLine::inventTransferLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-843">Table WHSLoadLine::inventTransferLine</span></span>|
|<span data-ttu-id="0bbb6-844">テーブル WHSLoadLine::purchLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-844">Table WHSLoadLine::purchLine</span></span>|
|<span data-ttu-id="0bbb6-845">テーブル WHSLoadLine::salesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-845">Table WHSLoadLine::salesLine</span></span>|
|<span data-ttu-id="0bbb6-846">テーブル WHSRFMenuItemTable.validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-846">Table WHSRFMenuItemTable.validateWrite</span></span>|
|<span data-ttu-id="0bbb6-847">Tax.distributeTotalTax</span><span class="sxs-lookup"><span data-stu-id="0bbb6-847">Tax.distributeTotalTax</span></span>|
|<span data-ttu-id="0bbb6-848">TradeInterCompany::insertInterCompanyInventDim</span><span class="sxs-lookup"><span data-stu-id="0bbb6-848">TradeInterCompany::insertInterCompanyInventDim</span></span>|
|<span data-ttu-id="0bbb6-849">TransactionReversal_Asset.checkStatusApplicable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-849">TransactionReversal_Asset.checkStatusApplicable</span></span>|
|<span data-ttu-id="0bbb6-850">TransactionReversal_Cust.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-850">TransactionReversal_Cust.main</span></span>|
|<span data-ttu-id="0bbb6-851">TransactionReversal_Cust.reversal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-851">TransactionReversal_Cust.reversal</span></span>|
|<span data-ttu-id="0bbb6-852">TransactionReversal_CustVend.createCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-852">TransactionReversal_CustVend.createCustVendTrans</span></span>|
|<span data-ttu-id="0bbb6-853">TSTimesheetLineWeek.loadFromLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-853">TSTimesheetLineWeek.loadFromLine</span></span>|
|<span data-ttu-id="0bbb6-854">VendInvoiceInfoListPageMultiSelect.determineSelectState</span><span class="sxs-lookup"><span data-stu-id="0bbb6-854">VendInvoiceInfoListPageMultiSelect.determineSelectState</span></span>|
|<span data-ttu-id="0bbb6-855">WHSInventReserveDeltaLevelsEnumerator::moveNext</span><span class="sxs-lookup"><span data-stu-id="0bbb6-855">WHSInventReserveDeltaLevelsEnumerator::moveNext</span></span>|
|<span data-ttu-id="0bbb6-856">WhsPostEngineBase::createLoadFromShipment</span><span class="sxs-lookup"><span data-stu-id="0bbb6-856">WhsPostEngineBase::createLoadFromShipment</span></span>|
|<span data-ttu-id="0bbb6-857">WHSWorkCreateProdPut.insertProdParmforProdItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-857">WHSWorkCreateProdPut.insertProdParmforProdItem</span></span>|
|<span data-ttu-id="0bbb6-858">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-858">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="0bbb6-859">WMSPickingList_OrderPick.RunPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="0bbb6-859">WMSPickingList_OrderPick.RunPrintMgmt</span></span>|
|<span data-ttu-id="0bbb6-860">WrkCtrlScheduler_Prod.loadJobsDetail</span><span class="sxs-lookup"><span data-stu-id="0bbb6-860">WrkCtrlScheduler_Prod.loadJobsDetail</span></span>|

## <a name="methods-made-hookable"></a><span data-ttu-id="0bbb6-861">フック可能なメソッド</span><span class="sxs-lookup"><span data-stu-id="0bbb6-861">Methods made hookable</span></span>

<span data-ttu-id="0bbb6-862">公開されずフック不可能な一部のメソッドでは、拡張性サポートが強化されています。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-862">Extensibility support has been extended for some methods that were not public and were not hookable.</span></span> <span data-ttu-id="0bbb6-863">以下のメソッドはフック可能な動作で明示的に修飾されています。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-863">The following methods have been explicitly decorated with hookable behavior.</span></span>

| <span data-ttu-id="0bbb6-864">方法</span><span class="sxs-lookup"><span data-stu-id="0bbb6-864">Method</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-865">Bank.checkBankIBAN</span><span class="sxs-lookup"><span data-stu-id="0bbb6-865">Bank.checkBankIBAN</span></span>|
|<span data-ttu-id="0bbb6-866">BankDepositCreateCancelJour.initValues</span><span class="sxs-lookup"><span data-stu-id="0bbb6-866">BankDepositCreateCancelJour.initValues</span></span>|
|<span data-ttu-id="0bbb6-867">BankDepositCreateCancelJour.newDepositCreateCancelJour</span><span class="sxs-lookup"><span data-stu-id="0bbb6-867">BankDepositCreateCancelJour.newDepositCreateCancelJour</span></span>|
|<span data-ttu-id="0bbb6-868">BankPaymCancel.initParms</span><span class="sxs-lookup"><span data-stu-id="0bbb6-868">BankPaymCancel.initParms</span></span>|
|<span data-ttu-id="0bbb6-869">BankPaymCancel.updateCollectionsStatusAutomation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-869">BankPaymCancel.updateCollectionsStatusAutomation</span></span>|
|<span data-ttu-id="0bbb6-870">CustAccountStatementExtController</span><span class="sxs-lookup"><span data-stu-id="0bbb6-870">CustAccountStatementExtController</span></span>|
|<span data-ttu-id="0bbb6-871">CustAccountStatementIntDP.insertCustAccountStatementIntTmp()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-871">CustAccountStatementIntDP.insertCustAccountStatementIntTmp()</span></span>|
|<span data-ttu-id="0bbb6-872">CustCollectionLetterPost.updateFee</span><span class="sxs-lookup"><span data-stu-id="0bbb6-872">CustCollectionLetterPost.updateFee</span></span>|
|<span data-ttu-id="0bbb6-873">CustInterestCreate.construct</span><span class="sxs-lookup"><span data-stu-id="0bbb6-873">CustInterestCreate.construct</span></span>|
|<span data-ttu-id="0bbb6-874">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-874">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp()</span></span>|
|<span data-ttu-id="0bbb6-875">CustSettlementPriorityProcessing</span><span class="sxs-lookup"><span data-stu-id="0bbb6-875">CustSettlementPriorityProcessing</span></span>|
|<span data-ttu-id="0bbb6-876">CustVendCreatePaymJournal.dialogAddDateSelectionFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-876">CustVendCreatePaymJournal.dialogAddDateSelectionFields</span></span>|
|<span data-ttu-id="0bbb6-877">CustVendPaymReconciliationSetStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-877">CustVendPaymReconciliationSetStatus</span></span>|
|<span data-ttu-id="0bbb6-878">CustVendReversePosting.updateCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-878">CustVendReversePosting.updateCustVendTrans</span></span>|
|<span data-ttu-id="0bbb6-879">DataEntity EcoResTrackingDimensionGroupEntity.dataSourceDimensionFieldId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-879">DataEntity EcoResTrackingDimensionGroupEntity.dataSourceDimensionFieldId</span></span>|
|<span data-ttu-id="0bbb6-880">EcoResProductCrossTableManager.saveValuesToProduct</span><span class="sxs-lookup"><span data-stu-id="0bbb6-880">EcoResProductCrossTableManager.saveValuesToProduct</span></span>|
|<span data-ttu-id="0bbb6-881">EcoResProductImage.getImageFrom2Records</span><span class="sxs-lookup"><span data-stu-id="0bbb6-881">EcoResProductImage.getImageFrom2Records</span></span>|
|<span data-ttu-id="0bbb6-882">EUSalesListTransfer - 3 つの方法</span><span class="sxs-lookup"><span data-stu-id="0bbb6-882">EUSalesListTransfer - 3 methods</span></span>|
|<span data-ttu-id="0bbb6-883">フォーム EcoResProductCreate.applyTemplate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-883">Form EcoResProductCreate.applyTemplate</span></span>|
|<span data-ttu-id="0bbb6-884">フォーム EcoResProductCreate.createData2Controls</span><span class="sxs-lookup"><span data-stu-id="0bbb6-884">Form EcoResProductCreate.createData2Controls</span></span>|
|<span data-ttu-id="0bbb6-885">フォーム PriceDiscTable.initFromCallerTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-885">Form PriceDiscTable.initFromCallerTable</span></span>|
|<span data-ttu-id="0bbb6-886">フォーム ProjCostControl.setButtonVisibility</span><span class="sxs-lookup"><span data-stu-id="0bbb6-886">Form ProjCostControl.setButtonVisibility</span></span>|
|<span data-ttu-id="0bbb6-887">フォーム projPostedTransRelInfoFormPart: ProjPostTransView: costPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-887">Form projPostedTransRelInfoFormPart: ProjPostTransView:  costPrice</span></span>|
|<span data-ttu-id="0bbb6-888">フォーム ProjTable.lookup 参照</span><span class="sxs-lookup"><span data-stu-id="0bbb6-888">Form ProjTable.lookup Reference</span></span>|
|<span data-ttu-id="0bbb6-889">フォーム ProjWorkBreakdownStructure</span><span class="sxs-lookup"><span data-stu-id="0bbb6-889">Form ProjWorkBreakdownStructure</span></span>|
|<span data-ttu-id="0bbb6-890">フォーム WHSPack.updateSummaryFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-890">Form WHSPack.updateSummaryFields</span></span>|
|<span data-ttu-id="0bbb6-891">FormletterJournalPost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-891">FormletterJournalPost</span></span>|
|<span data-ttu-id="0bbb6-892">FreeTextInvoiceDP.bankGroupIdName_CH</span><span class="sxs-lookup"><span data-stu-id="0bbb6-892">FreeTextInvoiceDP.bankGroupIdName_CH</span></span>|
|<span data-ttu-id="0bbb6-893">FreeTextInvoiceDP.bankZipCode_CH</span><span class="sxs-lookup"><span data-stu-id="0bbb6-893">FreeTextInvoiceDP.bankZipCode_CH</span></span>|
|<span data-ttu-id="0bbb6-894">FreeTextInvoiceDP.insertGiroInformation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-894">FreeTextInvoiceDP.insertGiroInformation</span></span>|
|<span data-ttu-id="0bbb6-895">FreeTextInvoiceDP.insertIntoFreeTextInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-895">FreeTextInvoiceDP.insertIntoFreeTextInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="0bbb6-896">FreeTextInvoiceDP.insertIntoFreeTextInvoiceLocalizationTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-896">FreeTextInvoiceDP.insertIntoFreeTextInvoiceLocalizationTmp</span></span>|
|<span data-ttu-id="0bbb6-897">FreeTextInvoiceDP.insertIntoFreeTextInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-897">FreeTextInvoiceDP.insertIntoFreeTextInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-898">HierarchyCreate_CRM.initHierarchy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-898">HierarchyCreate_CRM.initHierarchy</span></span>|
|<span data-ttu-id="0bbb6-899">HierarchyTemplateCopying_Proj.copyEstimates</span><span class="sxs-lookup"><span data-stu-id="0bbb6-899">HierarchyTemplateCopying_Proj.copyEstimates</span></span>|
|<span data-ttu-id="0bbb6-900">InventDimGroupSetup.combineInventDimParms</span><span class="sxs-lookup"><span data-stu-id="0bbb6-900">InventDimGroupSetup.combineInventDimParms</span></span>|
|<span data-ttu-id="0bbb6-901">InventLookupItemIdByDefaultOrder.initializeQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-901">InventLookupItemIdByDefaultOrder.initializeQuery</span></span>|
|<span data-ttu-id="0bbb6-902">InventStorageDimMap.modifiedInventSiteFromParent</span><span class="sxs-lookup"><span data-stu-id="0bbb6-902">InventStorageDimMap.modifiedInventSiteFromParent</span></span>|
|<span data-ttu-id="0bbb6-903">InventUpd_Physical.updatePhysicalReceiptTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-903">InventUpd_Physical.updatePhysicalReceiptTrans</span></span>|
|<span data-ttu-id="0bbb6-904">JournalFormTable.initJournalTypeFromCaller</span><span class="sxs-lookup"><span data-stu-id="0bbb6-904">JournalFormTable.initJournalTypeFromCaller</span></span>|
|<span data-ttu-id="0bbb6-905">LedgerJournalCheckPost.runInternal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-905">LedgerJournalCheckPost.runInternal</span></span>|
|<span data-ttu-id="0bbb6-906">マップ SalesPurchLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-906">Map SalesPurchLine.setPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-907">マップ VendDocumentLineMap.setPurchaseInventReceiveNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-907">Maps VendDocumentLineMap.setPurchaseInventReceiveNow</span></span>|
|<span data-ttu-id="0bbb6-908">OffsetVoucherCust.getAutoSettlementQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-908">OffsetVoucherCust.getAutoSettlementQuery</span></span>|
|<span data-ttu-id="0bbb6-909">ProjAdjustmentSelect.doTransCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-909">ProjAdjustmentSelect.doTransCost</span></span>|
|<span data-ttu-id="0bbb6-910">ProjAdjustmentSelect.doTransSale</span><span class="sxs-lookup"><span data-stu-id="0bbb6-910">ProjAdjustmentSelect.doTransSale</span></span>|
|<span data-ttu-id="0bbb6-911">ProjAdjustmentSelect.processProjEmplTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-911">ProjAdjustmentSelect.processProjEmplTrans</span></span>|
|<span data-ttu-id="0bbb6-912">ProjAdjustmentSelect.validate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-912">ProjAdjustmentSelect.validate</span></span>|
|<span data-ttu-id="0bbb6-913">ProjAdjustmentSplit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-913">ProjAdjustmentSplit</span></span>|
|<span data-ttu-id="0bbb6-914">ProjAdjustmentSplit.createNewTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-914">ProjAdjustmentSplit.createNewTrans</span></span>|
|<span data-ttu-id="0bbb6-915">ProjAdjustmentSplit.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-915">ProjAdjustmentSplit.run</span></span>|
|<span data-ttu-id="0bbb6-916">ProjAdjustmentUpdate.newPostAdjustment</span><span class="sxs-lookup"><span data-stu-id="0bbb6-916">ProjAdjustmentUpdate.newPostAdjustment</span></span>|
|<span data-ttu-id="0bbb6-917">ProjBegBalJournalTrans_CostSales.createProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-917">ProjBegBalJournalTrans_CostSales.createProjTransPosting</span></span>|
|<span data-ttu-id="0bbb6-918">ProjBegBalJournalTrans_Fee.createProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-918">ProjBegBalJournalTrans_Fee.createProjTransPosting</span></span>|
|<span data-ttu-id="0bbb6-919">ProjBegBalJournalTrans_OnAcc.createProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-919">ProjBegBalJournalTrans_OnAcc.createProjTransPosting</span></span>|
|<span data-ttu-id="0bbb6-920">projCostControl.progressUpdate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-920">projCostControl.progressUpdate</span></span>|
|<span data-ttu-id="0bbb6-921">ProjEstimatesDataContract.setRevenueSalesPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-921">ProjEstimatesDataContract.setRevenueSalesPrice</span></span>|
|<span data-ttu-id="0bbb6-922">ProjForecastBudget.forecastCopy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-922">ProjForecastBudget.forecastCopy</span></span>|
|<span data-ttu-id="0bbb6-923">ProjForecastBudget.forecastDelete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-923">ProjForecastBudget.forecastDelete</span></span>|
|<span data-ttu-id="0bbb6-924">ProjForecastPostItemFixedInvest.checkEnterCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-924">ProjForecastPostItemFixedInvest.checkEnterCost</span></span>|
|<span data-ttu-id="0bbb6-925">ProjForecastTransferFromWBS.transferToForecast</span><span class="sxs-lookup"><span data-stu-id="0bbb6-925">ProjForecastTransferFromWBS.transferToForecast</span></span>|
|<span data-ttu-id="0bbb6-926">ProjFormLetter。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-926">ProjFormLetter.</span></span> <span data-ttu-id="0bbb6-927">mainOnServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-927">mainOnServer</span></span>|
|<span data-ttu-id="0bbb6-928">ProjFormLetter.printPreview</span><span class="sxs-lookup"><span data-stu-id="0bbb6-928">ProjFormLetter.printPreview</span></span>|
|<span data-ttu-id="0bbb6-929">ProjInvoiceDP.insertIntoProjInvoiceLocalizationTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-929">ProjInvoiceDP.insertIntoProjInvoiceLocalizationTmp</span></span>|
|<span data-ttu-id="0bbb6-930">ProjInvoiceDP.insertIntoProjInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-930">ProjInvoiceDP.insertIntoProjInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-931">ProjInvoiceJournalCreate.creditMaxOk</span><span class="sxs-lookup"><span data-stu-id="0bbb6-931">ProjInvoiceJournalCreate.creditMaxOk</span></span>|
|<span data-ttu-id="0bbb6-932">ProjInvoiceJournalPost.initProposalUpdate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-932">ProjInvoiceJournalPost.initProposalUpdate</span></span>|
|<span data-ttu-id="0bbb6-933">ProjLedger.newInventCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-933">ProjLedger.newInventCost</span></span>|
|<span data-ttu-id="0bbb6-934">ProjPlanVersionManager.copyActivityData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-934">ProjPlanVersionManager.copyActivityData</span></span>|
|<span data-ttu-id="0bbb6-935">ProjPlanVersionsMananger.createDraftVersion</span><span class="sxs-lookup"><span data-stu-id="0bbb6-935">ProjPlanVersionsMananger.createDraftVersion</span></span>|
|<span data-ttu-id="0bbb6-936">ProjProjectTransListPageInteraction.linkActive</span><span class="sxs-lookup"><span data-stu-id="0bbb6-936">ProjProjectTransListPageInteraction.linkActive</span></span>|
|<span data-ttu-id="0bbb6-937">Projtask.getCorrespondingTaskElementNumber</span><span class="sxs-lookup"><span data-stu-id="0bbb6-937">Projtask.getCorrespondingTaskElementNumber</span></span>|
|<span data-ttu-id="0bbb6-938">ProjValCheckTrans.validateMandatory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-938">ProjValCheckTrans.validateMandatory</span></span>|
|<span data-ttu-id="0bbb6-939">projWbsUpdateController.getNodesMapSortedByPath</span><span class="sxs-lookup"><span data-stu-id="0bbb6-939">projWbsUpdateController.getNodesMapSortedByPath</span></span>|
|<span data-ttu-id="0bbb6-940">PSAProjInvoiceDP.processLinesFromInvoiceJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-940">PSAProjInvoiceDP.processLinesFromInvoiceJournal</span></span>|
|<span data-ttu-id="0bbb6-941">psaProjQuotationSubmitSend.validateProjectDates</span><span class="sxs-lookup"><span data-stu-id="0bbb6-941">psaProjQuotationSubmitSend.validateProjectDates</span></span>|
|<span data-ttu-id="0bbb6-942">PSAQuotationsDP.insertPSAQuotationsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-942">PSAQuotationsDP.insertPSAQuotationsTmp</span></span>|
|<span data-ttu-id="0bbb6-943">PurchaseOrderResponseCreate.createPurchaseOrderResponseLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-943">PurchaseOrderResponseCreate.createPurchaseOrderResponseLines</span></span>|
|<span data-ttu-id="0bbb6-944">PurchCancel.cancelMarkup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-944">PurchCancel.cancelMarkup</span></span>|
|<span data-ttu-id="0bbb6-945">PurchCreateFromSalesOrder.preMatchIncludedLinesWithAgreements</span><span class="sxs-lookup"><span data-stu-id="0bbb6-945">PurchCreateFromSalesOrder.preMatchIncludedLinesWithAgreements</span></span>|
|<span data-ttu-id="0bbb6-946">PurchPackingSlipDP.setPurchPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-946">PurchPackingSlipDP.setPurchPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-947">PurchPackingSlipDP.setPurchPackingSlipHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-947">PurchPackingSlipDP.setPurchPackingSlipHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-948">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-948">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-949">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-949">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-950">PurchSummary.checkFormLetterId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-950">PurchSummary.checkFormLetterId</span></span>|
|<span data-ttu-id="0bbb6-951">ReqPlanCopy.insertLog</span><span class="sxs-lookup"><span data-stu-id="0bbb6-951">ReqPlanCopy.insertLog</span></span>|
|<span data-ttu-id="0bbb6-952">ResRollupActivityWriter::updateRollupTableWithLockedCapacityForActivityResource()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-952">ResRollupActivityWriter::updateRollupTableWithLockedCapacityForActivityResource()</span></span>|
|<span data-ttu-id="0bbb6-953">ResRollupAvailabilityWriter.updateRollupTableWithLockedCapacityForNamedResource()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-953">ResRollupAvailabilityWriter.updateRollupTableWithLockedCapacityForNamedResource()</span></span>|
|<span data-ttu-id="0bbb6-954">SalesConfirmDP.setSalesConfirmDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-954">SalesConfirmDP.setSalesConfirmDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-955">SalesConfirmDP.setSalesConfirmHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-955">SalesConfirmDP.setSalesConfirmHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-956">SalesInvoiceController::main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-956">SalesInvoiceController::main</span></span>|
|<span data-ttu-id="0bbb6-957">SalesInvoiceDP.bankGroupIdName_CH</span><span class="sxs-lookup"><span data-stu-id="0bbb6-957">SalesInvoiceDP.bankGroupIdName_CH</span></span>|
|<span data-ttu-id="0bbb6-958">SalesInvoiceDP.bankZipCode_CH</span><span class="sxs-lookup"><span data-stu-id="0bbb6-958">SalesInvoiceDP.bankZipCode_CH</span></span>|
|<span data-ttu-id="0bbb6-959">SalesInvoiceDP.insertIntoSalesInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-959">SalesInvoiceDP.insertIntoSalesInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="0bbb6-960">SalesInvoiceDP.insertIntoSalesInvoiceLocalizationTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-960">SalesInvoiceDP.insertIntoSalesInvoiceLocalizationTmp</span></span>|
|<span data-ttu-id="0bbb6-961">SalesInvoiceDP.insertIntoSalesInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-961">SalesInvoiceDP.insertIntoSalesInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-962">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-962">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-963">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-963">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-964">SalesQuotationLineType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-964">SalesQuotationLineType.validateDelete</span></span>|
|<span data-ttu-id="0bbb6-965">SalesQuotationLineType.validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-965">SalesQuotationLineType.validateWrite</span></span>|
|<span data-ttu-id="0bbb6-966">SalesQuotationTableForm.CreateABSFromTemplate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-966">SalesQuotationTableForm.CreateABSFromTemplate</span></span>|
|<span data-ttu-id="0bbb6-967">salesQuotationTransferToProject.initParameters</span><span class="sxs-lookup"><span data-stu-id="0bbb6-967">salesQuotationTransferToProject.initParameters</span></span>|
|<span data-ttu-id="0bbb6-968">SalesTable.initFromCustTableMandatoryFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-968">SalesTable.initFromCustTableMandatoryFields</span></span>|
|<span data-ttu-id="0bbb6-969">SalesTableListPageInteraction.setButtonSell</span><span class="sxs-lookup"><span data-stu-id="0bbb6-969">SalesTableListPageInteraction.setButtonSell</span></span>|
|<span data-ttu-id="0bbb6-970">smmActivityCreate.createActivity</span><span class="sxs-lookup"><span data-stu-id="0bbb6-970">smmActivityCreate.createActivity</span></span>|
|<span data-ttu-id="0bbb6-971">smmActivityCreate.new</span><span class="sxs-lookup"><span data-stu-id="0bbb6-971">smmActivityCreate.new</span></span>|
|<span data-ttu-id="0bbb6-972">smmActivityParentLinkTablee.insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-972">smmActivityParentLinkTablee.insert</span></span>|
|<span data-ttu-id="0bbb6-973">SubledgerJournalizerProjectExtension.createLedgerUpdate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-973">SubledgerJournalizerProjectExtension.createLedgerUpdate</span></span>|
|<span data-ttu-id="0bbb6-974">テーブル CustBankAccount.validatePreNote</span><span class="sxs-lookup"><span data-stu-id="0bbb6-974">Table CustBankAccount.validatePreNote</span></span>|
|<span data-ttu-id="0bbb6-975">テーブル InventItemGTIN.formatGTIN</span><span class="sxs-lookup"><span data-stu-id="0bbb6-975">Table InventItemGTIN.formatGTIN</span></span>|
|<span data-ttu-id="0bbb6-976">テーブル PriceDiscAdmTrans.checkItemRelation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-976">Table PriceDiscAdmTrans.checkItemRelation</span></span>|
|<span data-ttu-id="0bbb6-977">テーブル PriceDiscAdmTrans.checkproductDimensions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-977">Table PriceDiscAdmTrans.checkproductDimensions</span></span>|
|<span data-ttu-id="0bbb6-978">テーブル ProjCategory.lookupProjCategoryType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-978">Table ProjCategory.lookupProjCategoryType</span></span>|
|<span data-ttu-id="0bbb6-979">テーブル ProjTable.validateWriteServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-979">Table ProjTable.validateWriteServer</span></span>|
|<span data-ttu-id="0bbb6-980">テーブル PSAActivityEstimates.checkUpdateQuotationLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-980">Table PSAActivityEstimates.checkUpdateQuotationLine</span></span>|
|<span data-ttu-id="0bbb6-981">テーブル PSAActivityEstimates.setSalesPriceFromCostPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-981">Table PSAActivityEstimates.setSalesPriceFromCostPrice</span></span>|
|<span data-ttu-id="0bbb6-982">テーブル PurchLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-982">Table PurchLine.setPriceDisc</span></span>|
|<span data-ttu-id="0bbb6-983">テーブル PurchTable.internalTableIdToTableId_W</span><span class="sxs-lookup"><span data-stu-id="0bbb6-983">Table PurchTable.internalTableIdToTableId_W</span></span>|
|<span data-ttu-id="0bbb6-984">テーブル SalesLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-984">Table SalesLine.setPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-985">テーブル Salesline.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-985">Table Salesline.setPriceDisc</span></span>|
|<span data-ttu-id="0bbb6-986">テーブル SalesQuotationLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-986">Table SalesQuotationLine.setPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-987">テーブル SalesQuotationLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-987">Table SalesQuotationLine.setPriceDisc</span></span>|
|<span data-ttu-id="0bbb6-988">テーブル SalesTable.setSalesOrderReleaseStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-988">Table SalesTable.setSalesOrderReleaseStatus</span></span>|
|<span data-ttu-id="0bbb6-989">テーブル TmpCustVendTrans.createLineCreditLimit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-989">Table TmpCustVendTrans.createLineCreditLimit</span></span>|
|<span data-ttu-id="0bbb6-990">テーブル TmpCustVendTrans.createLineCreditRemain</span><span class="sxs-lookup"><span data-stu-id="0bbb6-990">Table TmpCustVendTrans.createLineCreditRemain</span></span>|
|<span data-ttu-id="0bbb6-991">テーブル TmpCustVendTrans.createLineOrdered</span><span class="sxs-lookup"><span data-stu-id="0bbb6-991">Table TmpCustVendTrans.createLineOrdered</span></span>|
|<span data-ttu-id="0bbb6-992">テーブル TmpCustVendTrans.createLinePackingSlip</span><span class="sxs-lookup"><span data-stu-id="0bbb6-992">Table TmpCustVendTrans.createLinePackingSlip</span></span>|
|<span data-ttu-id="0bbb6-993">テーブル TmpCustVendTrans.createLineTotal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-993">Table TmpCustVendTrans.createLineTotal</span></span>|
|<span data-ttu-id="0bbb6-994">テーブル TmpCustVendTrans.insertTmpCustVendTransForCustBalance</span><span class="sxs-lookup"><span data-stu-id="0bbb6-994">Table TmpCustVendTrans.insertTmpCustVendTransForCustBalance</span></span>|
|<span data-ttu-id="0bbb6-995">テーブル TSTimeSheetLine.checkActivity</span><span class="sxs-lookup"><span data-stu-id="0bbb6-995">Table TSTimeSheetLine.checkActivity</span></span>|
|<span data-ttu-id="0bbb6-996">TSTimesheetLine::buildQuerySmmActivities</span><span class="sxs-lookup"><span data-stu-id="0bbb6-996">TSTimesheetLine::buildQuerySmmActivities</span></span>|
|<span data-ttu-id="0bbb6-997">TsTimesheetPost.validatePost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-997">TsTimesheetPost.validatePost</span></span>|
|<span data-ttu-id="0bbb6-998">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-998">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp()</span></span>|
|<span data-ttu-id="0bbb6-999">VendTransQueryBuild::construct</span><span class="sxs-lookup"><span data-stu-id="0bbb6-999">VendTransQueryBuild::construct</span></span>|
|<span data-ttu-id="0bbb6-1000">VersioningPurchaseOrderResponse.archiveResponseLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1000">VersioningPurchaseOrderResponse.archiveResponseLines</span></span>|
|<span data-ttu-id="0bbb6-1001">VersioningPurchaseOrderResponse.restoreLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1001">VersioningPurchaseOrderResponse.restoreLines</span></span>|
|<span data-ttu-id="0bbb6-1002">WhsCycleCountCreateLocation.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1002">WhsCycleCountCreateLocation.run</span></span>|
|<span data-ttu-id="0bbb6-1003">WhsLoadReplenishment.calculateReplenishQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1003">WhsLoadReplenishment.calculateReplenishQty</span></span>|
|<span data-ttu-id="0bbb6-1004">WHSLoadTable::initPurchOriginDestination</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1004">WHSLoadTable::initPurchOriginDestination</span></span>|
|<span data-ttu-id="0bbb6-1005">WhsReplenishment.calculateReplenishQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1005">WhsReplenishment.calculateReplenishQty</span></span>|
|<span data-ttu-id="0bbb6-1006">WhsRFControlData.validateAndUpdateWorkClusterLPScan</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1006">WhsRFControlData.validateAndUpdateWorkClusterLPScan</span></span>|
|<span data-ttu-id="0bbb6-1007">WhsShipConfirm.tmsRouteConfirmation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1007">WhsShipConfirm.tmsRouteConfirmation</span></span>|
|<span data-ttu-id="0bbb6-1008">WhsWarehouseRelease.buildReleaseQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1008">WhsWarehouseRelease.buildReleaseQuery</span></span>|
|<span data-ttu-id="0bbb6-1009">WhsWarehouseRelease.createLoadLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1009">WhsWarehouseRelease.createLoadLines</span></span>|
|<span data-ttu-id="0bbb6-1010">WHSWaveTable.createWaveTableFromTemplate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1010">WHSWaveTable.createWaveTableFromTemplate</span></span>|
|<span data-ttu-id="0bbb6-1011">WHSWorkExecute.createAdjustmentWork</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1011">WHSWorkExecute.createAdjustmentWork</span></span>|
|<span data-ttu-id="0bbb6-1012">WHSWorkExecute.createCountingJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1012">WHSWorkExecute.createCountingJournal</span></span>|
|<span data-ttu-id="0bbb6-1013">WHSWorkExecute.createInventLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1013">WHSWorkExecute.createInventLine</span></span>|
|<span data-ttu-id="0bbb6-1014">WHSWorkExecute.executeShortPick</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1014">WHSWorkExecute.executeShortPick</span></span>|
|<span data-ttu-id="0bbb6-1015">WHSWorkExecute.shortPickAdjustOut</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1015">WHSWorkExecute.shortPickAdjustOut</span></span>|
|<span data-ttu-id="0bbb6-1016">WHSWorkExecuteDisplayPOReceiving.createWork</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1016">WHSWorkExecuteDisplayPOReceiving.createWork</span></span>|
|<span data-ttu-id="0bbb6-1017">WorkTimeTable.lookupTime</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1017">WorkTimeTable.lookupTime</span></span>|

## <a name="inline-delegates"></a><span data-ttu-id="0bbb6-1018">インライン デリゲート</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1018">Inline delegates</span></span>

<span data-ttu-id="0bbb6-1019">インライン デリゲートを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1019">Inline delegates are now available.</span></span> <span data-ttu-id="0bbb6-1020">インライン デリゲートの最も一般的な使用方法は、メソッドをより粒度の細かいメソッドに分割して、より小規模なメソッドで拡張イベントを使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1020">The most common way to use inline delegates is to split the method into more granular methods and enable extensibility events in the smaller methods.</span></span>

|  <span data-ttu-id="0bbb6-1021">方法</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1021">Method</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-1022">AssetCopy.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1022">AssetCopy.run</span></span>|
|<span data-ttu-id="0bbb6-1023">AssetPost.post</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1023">AssetPost.post</span></span>|
|<span data-ttu-id="0bbb6-1024">AssetSplit.createTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1024">AssetSplit.createTrans</span></span>|
|<span data-ttu-id="0bbb6-1025">AssetSplit.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1025">AssetSplit.run</span></span>|
|<span data-ttu-id="0bbb6-1026">BankDepositCreateCancelJour.createDepositCancelJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1026">BankDepositCreateCancelJour.createDepositCancelJournal</span></span>|
|<span data-ttu-id="0bbb6-1027">BankPaymCancel.createCancellingCustTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1027">BankPaymCancel.createCancellingCustTrans</span></span>|
|<span data-ttu-id="0bbb6-1028">BankPaymCancel.reverseSettlement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1028">BankPaymCancel.reverseSettlement</span></span>|
|<span data-ttu-id="0bbb6-1029">BankPaymCancel.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1029">BankPaymCancel.run</span></span>|
|<span data-ttu-id="0bbb6-1030">BankPositivePayExport.initPositivePayQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1030">BankPositivePayExport.initPositivePayQuery</span></span>|
|<span data-ttu-id="0bbb6-1031">BankPrintTestCheque.createTestCheque</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1031">BankPrintTestCheque.createTestCheque</span></span>|
|<span data-ttu-id="0bbb6-1032">BOMCalcItem.initListBOM</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1032">BOMCalcItem.initListBOM</span></span>|
|<span data-ttu-id="0bbb6-1033">BOMCalcJob.runBOMCalculation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1033">BOMCalcJob.runBOMCalculation</span></span>|
|<span data-ttu-id="0bbb6-1034">BOMRouteCopyJob.checkTo</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1034">BOMRouteCopyJob.checkTo</span></span>|
|<span data-ttu-id="0bbb6-1035">BOMRouteCopyJob.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1035">BOMRouteCopyJob.main</span></span>|
|<span data-ttu-id="0bbb6-1036">BomRouteCopyJob::main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1036">BomRouteCopyJob::main</span></span>|
|<span data-ttu-id="0bbb6-1037">BomSearch.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1037">BomSearch.init</span></span>|
|<span data-ttu-id="0bbb6-1038">bomVersionActivate.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1038">bomVersionActivate.run</span></span>|
|<span data-ttu-id="0bbb6-1039">CaseDetailForm.lookupParentCase</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1039">CaseDetailForm.lookupParentCase</span></span>|
|<span data-ttu-id="0bbb6-1040">CaseDetailFormCreate.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1040">CaseDetailFormCreate.main</span></span>|
|<span data-ttu-id="0bbb6-1041">CaseUpdateStatus.changeStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1041">CaseUpdateStatus.changeStatus</span></span>|
|<span data-ttu-id="0bbb6-1042">CaseUpdateStatus_Close.updateStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1042">CaseUpdateStatus_Close.updateStatus</span></span>|
|<span data-ttu-id="0bbb6-1043">ChequeDP.insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1043">ChequeDP.insertChequeTmp</span></span>|
|<span data-ttu-id="0bbb6-1044">クラス SalesLineType.intercompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1044">Class SalesLineType.intercompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-1045">Commission.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1045">Commission.run</span></span>|
|<span data-ttu-id="0bbb6-1046">CostControlPostingSourceDocumentLine.createCommittedCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1046">CostControlPostingSourceDocumentLine.createCommittedCost</span></span>|
|<span data-ttu-id="0bbb6-1047">CostSheetPanel.build</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1047">CostSheetPanel.build</span></span>|
|<span data-ttu-id="0bbb6-1048">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1048">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span></span>|
|<span data-ttu-id="0bbb6-1049">CustAgingReportController.getReportName</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1049">CustAgingReportController.getReportName</span></span>|
|<span data-ttu-id="0bbb6-1050">CustAgingReportDP.insertCustAgingReportTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1050">CustAgingReportDP.insertCustAgingReportTmp</span></span>|
|<span data-ttu-id="0bbb6-1051">CustCollectionJourDP.collectionLetterTitle</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1051">CustCollectionJourDP.collectionLetterTitle</span></span>|
|<span data-ttu-id="0bbb6-1052">CustCollectionJourDP.insertCustCollectionJourTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1052">CustCollectionJourDP.insertCustCollectionJourTmp</span></span>|
|<span data-ttu-id="0bbb6-1053">CustCollectionLetterCancel.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1053">CustCollectionLetterCancel.main</span></span>|
|<span data-ttu-id="0bbb6-1054">CustCollectionLetterCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1054">CustCollectionLetterCreate.createJournal</span></span>|
|<span data-ttu-id="0bbb6-1055">CustCollectionLetterCreate.updateCreatedCollectionLetter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1055">CustCollectionLetterCreate.updateCreatedCollectionLetter</span></span>|
|<span data-ttu-id="0bbb6-1056">CustCollectionLetterPost.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1056">CustCollectionLetterPost.run</span></span>|
|<span data-ttu-id="0bbb6-1057">CustCollectionLetterPost.updateFee</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1057">CustCollectionLetterPost.updateFee</span></span>|
|<span data-ttu-id="0bbb6-1058">CustInterestCancel.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1058">CustInterestCancel.run</span></span>|
|<span data-ttu-id="0bbb6-1059">CustInterestCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1059">CustInterestCreate.createJournal</span></span>|
|<span data-ttu-id="0bbb6-1060">CustInterestCreate.insertCustInterestTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1060">CustInterestCreate.insertCustInterestTrans</span></span>|
|<span data-ttu-id="0bbb6-1061">CustInterestCreate.insertCustInterestTransLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1061">CustInterestCreate.insertCustInterestTransLine</span></span>|
|<span data-ttu-id="0bbb6-1062">CustInterestPost.updateCustInterestTransVoucherRef</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1062">CustInterestPost.updateCustInterestTransVoucherRef</span></span>|
|<span data-ttu-id="0bbb6-1063">CustInterestPost.updateFee</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1063">CustInterestPost.updateFee</span></span>|
|<span data-ttu-id="0bbb6-1064">CustInvoiceDP::insertCustInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1064">CustInvoiceDP::insertCustInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-1065">CustInvoiceSpecDP::insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1065">CustInvoiceSpecDP::insertIntoTempTable</span></span>|
|<span data-ttu-id="0bbb6-1066">CustNsf.createFeeJournalTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1066">CustNsf.createFeeJournalTrans</span></span>|
|<span data-ttu-id="0bbb6-1067">CustOutPaymControlController.insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1067">CustOutPaymControlController.insert</span></span>|
|<span data-ttu-id="0bbb6-1068">CustPostInvoice.createJournalHeader</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1068">CustPostInvoice.createJournalHeader</span></span>|
|<span data-ttu-id="0bbb6-1069">CustPostInvoice::createJournalHeader</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1069">CustPostInvoice::createJournalHeader</span></span>|
|<span data-ttu-id="0bbb6-1070">CustSettlementPriorityProcessing.createTempData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1070">CustSettlementPriorityProcessing.createTempData</span></span>|
|<span data-ttu-id="0bbb6-1071">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1071">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span></span>|
|<span data-ttu-id="0bbb6-1072">CustTransOpenPerDateDP.insertCustTransOpenPerDateTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1072">CustTransOpenPerDateDP.insertCustTransOpenPerDateTmp</span></span>|
|<span data-ttu-id="0bbb6-1073">CustVendCreatePaymJournal.checkBlocked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1073">CustVendCreatePaymJournal.checkBlocked</span></span>|
|<span data-ttu-id="0bbb6-1074">CustVendCreatePaymJournal.dialogAddInvoiceSelectionCriteriaFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1074">CustVendCreatePaymJournal.dialogAddInvoiceSelectionCriteriaFields</span></span>|
|<span data-ttu-id="0bbb6-1075">CustVendCreatePaymJournal.runPaymentProposalGenerationProcess</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1075">CustVendCreatePaymJournal.runPaymentProposalGenerationProcess</span></span>|
|<span data-ttu-id="0bbb6-1076">CustVendCreatePaymJournal_Vend.UpdateQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1076">CustVendCreatePaymJournal_Vend.UpdateQuery</span></span>|
|<span data-ttu-id="0bbb6-1077">CustVendFindSettlements.findSettledSettlements</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1077">CustVendFindSettlements.findSettledSettlements</span></span>|
|<span data-ttu-id="0bbb6-1078">CustVendOpenTransBalances.initAccountNumCurrencies</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1078">CustVendOpenTransBalances.initAccountNumCurrencies</span></span>|
|<span data-ttu-id="0bbb6-1079">CustVendOpenTransBalances.new</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1079">CustVendOpenTransBalances.new</span></span>|
|<span data-ttu-id="0bbb6-1080">CustVendOpenTransManager.initFromCaller</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1080">CustVendOpenTransManager.initFromCaller</span></span>|
|<span data-ttu-id="0bbb6-1081">CustVendOpenTransManager.updateOriginatorForMarkedTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1081">CustVendOpenTransManager.updateOriginatorForMarkedTrans</span></span>|
|<span data-ttu-id="0bbb6-1082">CustVendPaymProposal.createProposalLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1082">CustVendPaymProposal.createProposalLine</span></span>|
|<span data-ttu-id="0bbb6-1083">CustVendPaymProposalTransferToJournal.initLedgerJournalTransFromPaymLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1083">CustVendPaymProposalTransferToJournal.initLedgerJournalTransFromPaymLine</span></span>|
|<span data-ttu-id="0bbb6-1084">CustVendPaymProposalTransferToJournal.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1084">CustVendPaymProposalTransferToJournal.run</span></span>|
|<span data-ttu-id="0bbb6-1085">CustVendPaymProposalTransferToJournal.transferProposal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1085">CustVendPaymProposalTransferToJournal.transferProposal</span></span>|
|<span data-ttu-id="0bbb6-1086">CustVendReversePosting.updateCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1086">CustVendReversePosting.updateCustVendTrans</span></span>|
|<span data-ttu-id="0bbb6-1087">CustVendSettle.createSettlementForDebitOrCreditTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1087">CustVendSettle.createSettlementForDebitOrCreditTrans</span></span>|
|<span data-ttu-id="0bbb6-1088">CustVendSumForPaym::Validate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1088">CustVendSumForPaym::Validate</span></span>|
|<span data-ttu-id="0bbb6-1089">CustVendVoucher.post</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1089">CustVendVoucher.post</span></span>|
|<span data-ttu-id="0bbb6-1090">CustVoucher.createInvoiceJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1090">CustVoucher.createInvoiceJournal</span></span>|
|<span data-ttu-id="0bbb6-1091">DataEntityView FreeTextInvoiceEntity.insertFreeTextInvoiceLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1091">DataEntityView FreeTextInvoiceEntity.insertFreeTextInvoiceLines</span></span>|
|<span data-ttu-id="0bbb6-1092">DataEntityView FreeTextInvoiceEntity.preTargetProcessSetBased</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1092">DataEntityView FreeTextInvoiceEntity.preTargetProcessSetBased</span></span>|
|<span data-ttu-id="0bbb6-1093">DimensionHierarchyHelper::getHierarchyTypeByAccountType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1093">DimensionHierarchyHelper::getHierarchyTypeByAccountType</span></span>|
|<span data-ttu-id="0bbb6-1094">EcoResProductMasterManager.addProductDimensionValue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1094">EcoResProductMasterManager.addProductDimensionValue</span></span>|
|<span data-ttu-id="0bbb6-1095">EcoResProductReleaseManager.createInventITable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1095">EcoResProductReleaseManager.createInventITable</span></span>|
|<span data-ttu-id="0bbb6-1096">EcoResProductReleaseManager.createInventItemSetupSupplyType</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1096">EcoResProductReleaseManager.createInventItemSetupSupplyType</span></span>|
|<span data-ttu-id="0bbb6-1097">EcoResProductReleaseManager.setInventTableFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1097">EcoResProductReleaseManager.setInventTableFields</span></span>|
|<span data-ttu-id="0bbb6-1098">EcoResProductTemplateManager.getBufferByDataSourceName</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1098">EcoResProductTemplateManager.getBufferByDataSourceName</span></span>|
|<span data-ttu-id="0bbb6-1099">EcoResProductVariantManager.createProductVariant</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1099">EcoResProductVariantManager.createProductVariant</span></span>|
|<span data-ttu-id="0bbb6-1100">デリゲートを拡張 (DirPartyPostalAddressFormHandler、defaultLocationRoles_delegate)</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1100">Extend delegatestr(DirPartyPostalAddressFormHandler, defaultLocationRoles_delegate)</span></span>|
|<span data-ttu-id="0bbb6-1101">フォーム BankReconciliation: BankAccountReconcile::clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1101">Form BankReconciliation: BankAccountReconcile::clicked</span></span>|
|<span data-ttu-id="0bbb6-1102">フォーム CustCreditLimitCreditPart.totalAgingByCompany</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1102">Form CustCreditLimitCreditPart.totalAgingByCompany</span></span>|
|<span data-ttu-id="0bbb6-1103">フォーム CustDirectDebitMandate.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1103">Form CustDirectDebitMandate.run</span></span>|
|<span data-ttu-id="0bbb6-1104">フォーム CustFormletterParameters.PrintMgMt.clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1104">Form CustFormletterParameters.PrintMgMt.clicked</span></span>|
|<span data-ttu-id="0bbb6-1105">フォーム CustOpenTrans.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1105">Form CustOpenTrans.init</span></span>|
|<span data-ttu-id="0bbb6-1106">フォーム CustOpenTrans.updateDesignStatic</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1106">Form CustOpenTrans.updateDesignStatic</span></span>|
|<span data-ttu-id="0bbb6-1107">フォーム CustOpenTrans: ボタン UpdateNow::clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1107">Form CustOpenTrans: Button UpdateNow::clicked</span></span>|
|<span data-ttu-id="0bbb6-1108">フォーム CustOpenTrans::doesCallerAllowEdit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1108">Form CustOpenTrans::doesCallerAllowEdit</span></span>|
|<span data-ttu-id="0bbb6-1109">フォーム CustTable: CustTable::write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1109">Form CustTable: CustTable::write</span></span>|
|<span data-ttu-id="0bbb6-1110">フォーム EcoResProductCreate.writeMoreFields</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1110">Form EcoResProductCreate.writeMoreFields</span></span>|
|<span data-ttu-id="0bbb6-1111">フォーム EcoResProductVariantsPerCompany: InventDimCombination::write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1111">Form EcoResProductVariantsPerCompany: InventDimCombination::write</span></span>|
|<span data-ttu-id="0bbb6-1112">フォーム HierarchyTemplateCopying_Proj.copyEstimates</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1112">Form HierarchyTemplateCopying_Proj.copyEstimates</span></span>|
|<span data-ttu-id="0bbb6-1113">フォーム InventDimParmFixed: InventDimParm::create</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1113">Form InventDimParmFixed: InventDimParm::create</span></span>|
|<span data-ttu-id="0bbb6-1114">フォーム InventOnhandReserve: InventSum::reserveNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1114">Form InventOnhandReserve: InventSum::reserveNow</span></span>|
|<span data-ttu-id="0bbb6-1115">フォーム InventOnhandReserve: InventTransOriginMovement::movementOnOrderUnit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1115">Form InventOnhandReserve: InventTransOriginMovement::movementOnOrderUnit</span></span>|
|<span data-ttu-id="0bbb6-1116">フォーム InventOnhandReserve: InventTransOriginMovement::movementReservOrderedUnit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1116">Form InventOnhandReserve: InventTransOriginMovement::movementReservOrderedUnit</span></span>|
|<span data-ttu-id="0bbb6-1117">フォーム InventOnhandReserve: InventTransOriginMovement::movementReservPhysicalUnit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1117">Form InventOnhandReserve: InventTransOriginMovement::movementReservPhysicalUnit</span></span>|
|<span data-ttu-id="0bbb6-1118">フォーム InventTransRegister: TmpInventTransWMS::setEnabled</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1118">Form InventTransRegister: TmpInventTransWMS::setEnabled</span></span>|
|<span data-ttu-id="0bbb6-1119">フォーム LedgerJournalTransCustPaym.accountNumModifiedPost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1119">Form LedgerJournalTransCustPaym.accountNumModifiedPost</span></span>|
|<span data-ttu-id="0bbb6-1120">フォーム LedgerJournalTransCustPaym: ボタン ButtonSettlement::clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1120">Form LedgerJournalTransCustPaym: Button ButtonSettlement::clicked</span></span>|
|<span data-ttu-id="0bbb6-1121">フォーム LedgerJournalTransVendPaym: buttonPaymReconciliation::Clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1121">Form LedgerJournalTransVendPaym: buttonPaymReconciliation::Clicked</span></span>|
|<span data-ttu-id="0bbb6-1122">フォーム LedgerJournalTransVendPaym: PaymReconciliationReject::Clicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1122">Form LedgerJournalTransVendPaym: PaymReconciliationReject::Clicked</span></span>|
|<span data-ttu-id="0bbb6-1123">フォーム MarkupTrans.MarkupTrans_DS.active()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1123">Form MarkupTrans.MarkupTrans_DS.active()</span></span>|
|<span data-ttu-id="0bbb6-1124">フォーム MCRSalesQuickQuote.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1124">Form MCRSalesQuickQuote.init</span></span>|
|<span data-ttu-id="0bbb6-1125">フォーム MCRSalesQuickQuote.prepareSearch</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1125">Form MCRSalesQuickQuote.prepareSearch</span></span>|
|<span data-ttu-id="0bbb6-1126">フォーム MCRSalesQuickQuote.tmpFrmVirtualInventDimId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1126">Form MCRSalesQuickQuote.tmpFrmVirtualInventDimId</span></span>|
|<span data-ttu-id="0bbb6-1127">フォーム MRCSalesQuickQuote.createLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1127">Form MRCSalesQuickQuote.createLines</span></span>|
|<span data-ttu-id="0bbb6-1128">フォーム PriceDiscActual::init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1128">Form PriceDiscActual::init</span></span>|
|<span data-ttu-id="0bbb6-1129">フォーム ProcCategoryHierarchyManagement.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1129">Form ProcCategoryHierarchyManagement.init</span></span>|
|<span data-ttu-id="0bbb6-1130">フォーム ProjAdjustment.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1130">Form ProjAdjustment.init</span></span>|
|<span data-ttu-id="0bbb6-1131">フォーム ProjAdjustment.selectAdjRecords</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1131">Form ProjAdjustment.selectAdjRecords</span></span>|
|<span data-ttu-id="0bbb6-1132">フォーム ProjCreditNoteSelect.canClose</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1132">Form ProjCreditNoteSelect.canClose</span></span>|
|<span data-ttu-id="0bbb6-1133">フォーム ProjCreditNoteSelect.writeTmpFrmVirtual</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1133">Form ProjCreditNoteSelect.writeTmpFrmVirtual</span></span>|
|<span data-ttu-id="0bbb6-1134">フォーム ProjInvoiceProposalCreateLines.TransTypeSelectionCtrl.lookup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1134">Form ProjInvoiceProposalCreateLines.TransTypeSelectionCtrl.lookup</span></span>|
|<span data-ttu-id="0bbb6-1135">フォーム PurchTable: PurchTable::enableJournalButtons</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1135">Form PurchTable: PurchTable::enableJournalButtons</span></span>|
|<span data-ttu-id="0bbb6-1136">フォーム SalesATP.SalesATP</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1136">Form SalesATP.SalesATP</span></span>|
|<span data-ttu-id="0bbb6-1137">フォーム SalesQuickQuote: InventDimCombination::getSetQuantyties</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1137">Form SalesQuickQuote: InventDimCombination::getSetQuantyties</span></span>|
|<span data-ttu-id="0bbb6-1138">フォーム SalesQuickQuote: InventDimCombination::salesQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1138">Form SalesQuickQuote: InventDimCombination::salesQty</span></span>|
|<span data-ttu-id="0bbb6-1139">フォーム SalesQuotationProjTable::SalesQuotationLine::ItemId::modified</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1139">Form SalesQuotationProjTable::SalesQuotationLine::ItemId::modified</span></span>|
|<span data-ttu-id="0bbb6-1140">フォーム SalesQuotationTable: SalesQuotationTable::write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1140">Form SalesQuotationTable: SalesQuotationTable::write</span></span>|
|<span data-ttu-id="0bbb6-1141">フォーム SalesTable.modified</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1141">Form SalesTable.modified</span></span>|
|<span data-ttu-id="0bbb6-1142">フォーム SalesTable.SalesTable_DS.linkActive</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1142">Form SalesTable.SalesTable_DS.linkActive</span></span>|
|<span data-ttu-id="0bbb6-1143">フォーム SalesTable.write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1143">Form SalesTable.write</span></span>|
|<span data-ttu-id="0bbb6-1144">フォーム SalesTable: SalesLine::write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1144">Form SalesTable: SalesLine::write</span></span>|
|<span data-ttu-id="0bbb6-1145">フォーム SalesTable: SalesTable::write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1145">Form SalesTable: SalesTable::write</span></span>|
|<span data-ttu-id="0bbb6-1146">フォーム TMSRateRouteWorkbench.updateRoutes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1146">Form TMSRateRouteWorkbench.updateRoutes</span></span>|
|<span data-ttu-id="0bbb6-1147">フォーム VendEditInvoice: VendInvoiceInfoTable.write</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1147">Form VendEditInvoice: VendInvoiceInfoTable.write</span></span>|
|<span data-ttu-id="0bbb6-1148">フォーム WhsWorkTable.setFilter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1148">Form WhsWorkTable.setFilter</span></span>|
|<span data-ttu-id="0bbb6-1149">FormLetterJournalPost.post</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1149">FormLetterJournalPost.post</span></span>|
|<span data-ttu-id="0bbb6-1150">FormLetterService.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1150">FormLetterService.run</span></span>|
|<span data-ttu-id="0bbb6-1151">フォーム WHSLoadPlanningWorkbench.init</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1151">Forms WHSLoadPlanningWorkbench.init</span></span>|
|<span data-ttu-id="0bbb6-1152">フォーム WHSLoadPlanningWorkbench.restoreQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1152">Forms WHSLoadPlanningWorkbench.restoreQuery</span></span>|
|<span data-ttu-id="0bbb6-1153">FreeTextInvoiceDP::insertIntoFreeTextInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1153">FreeTextInvoiceDP::insertIntoFreeTextInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="0bbb6-1154">ProjTableCreate.init から</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1154">From ProjTableCreate.init</span></span>|
|<span data-ttu-id="0bbb6-1155">HierarchyCreate.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1155">HierarchyCreate.run</span></span>|
|<span data-ttu-id="0bbb6-1156">HierarchyTemplateCopyingDialog_proj.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1156">HierarchyTemplateCopyingDialog_proj.main</span></span>|
|<span data-ttu-id="0bbb6-1157">InterCompanyPost.formLetterCollect</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1157">InterCompanyPost.formLetterCollect</span></span>|
|<span data-ttu-id="0bbb6-1158">InventAgeDimDP.calcAllDim</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1158">InventAgeDimDP.calcAllDim</span></span>|
|<span data-ttu-id="0bbb6-1159">InventAgeDimDP.insertInventAgeDimTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1159">InventAgeDimDP.insertInventAgeDimTmp</span></span>|
|<span data-ttu-id="0bbb6-1160">InventAgeDimDP.insertOrMergeInventAgeDimTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1160">InventAgeDimDP.insertOrMergeInventAgeDimTmp</span></span>|
|<span data-ttu-id="0bbb6-1161">InventCountCreate.dialog</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1161">InventCountCreate.dialog</span></span>|
|<span data-ttu-id="0bbb6-1162">InventDimCtrl_Frm_Lookup.initDisplayOrderDataSource</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1162">InventDimCtrl_Frm_Lookup.initDisplayOrderDataSource</span></span>|
|<span data-ttu-id="0bbb6-1163">InventDimPhysDP.processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1163">InventDimPhysDP.processReport</span></span>|
|<span data-ttu-id="0bbb6-1164">InventDimViewContract</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1164">InventDimViewContract</span></span>|
|<span data-ttu-id="0bbb6-1165">InventMovement.updateSerialNumIssue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1165">InventMovement.updateSerialNumIssue</span></span>|
|<span data-ttu-id="0bbb6-1166">InventMovement.updateSerialNumReceipt</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1166">InventMovement.updateSerialNumReceipt</span></span>|
|<span data-ttu-id="0bbb6-1167">InventMovement::updateLedgerPhysical</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1167">InventMovement::updateLedgerPhysical</span></span>|
|<span data-ttu-id="0bbb6-1168">InventOnhandReserve.updateReserveNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1168">InventOnhandReserve.updateReserveNow</span></span>|
|<span data-ttu-id="0bbb6-1169">InventSumDateEngine.clearNotSelectedDimensions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1169">InventSumDateEngine.clearNotSelectedDimensions</span></span>|
|<span data-ttu-id="0bbb6-1170">InventTransferMulti.insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1170">InventTransferMulti.insert</span></span>|
|<span data-ttu-id="0bbb6-1171">InventUpd_Picked.updatePickMore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1171">InventUpd_Picked.updatePickMore</span></span>|
|<span data-ttu-id="0bbb6-1172">InventUpd_Reservation.updateReserveLess</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1172">InventUpd_Reservation.updateReserveLess</span></span>|
|<span data-ttu-id="0bbb6-1173">InventUpdateOnhand.checkOnHand</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1173">InventUpdateOnhand.checkOnHand</span></span>|
|<span data-ttu-id="0bbb6-1174">InventValueReportContract</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1174">InventValueReportContract</span></span>|
|<span data-ttu-id="0bbb6-1175">InventValueReportController</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1175">InventValueReportController</span></span>|
|<span data-ttu-id="0bbb6-1176">InventValueReportPopulateResource.initReportLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1176">InventValueReportPopulateResource.initReportLines</span></span>|
|<span data-ttu-id="0bbb6-1177">JmgPostStandardSystem.postProjTime</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1177">JmgPostStandardSystem.postProjTime</span></span>|
|<span data-ttu-id="0bbb6-1178">JournalFormTable.designLookupJournalName</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1178">JournalFormTable.designLookupJournalName</span></span>|
|<span data-ttu-id="0bbb6-1179">JournalFormTable.initAllOpenPostedFromCaller</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1179">JournalFormTable.initAllOpenPostedFromCaller</span></span>|
|<span data-ttu-id="0bbb6-1180">LedgerBalancesBase.CalculateBalance</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1180">LedgerBalancesBase.CalculateBalance</span></span>|
|<span data-ttu-id="0bbb6-1181">LedgerInAccountStatement.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1181">LedgerInAccountStatement.main</span></span>|
|<span data-ttu-id="0bbb6-1182">LedgerJournalCheckPost.createReverseEntryJournalLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1182">LedgerJournalCheckPost.createReverseEntryJournalLine</span></span>|
|<span data-ttu-id="0bbb6-1183">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1183">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="0bbb6-1184">LedgerJournalCheckPost.runInternal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1184">LedgerJournalCheckPost.runInternal</span></span>|
|<span data-ttu-id="0bbb6-1185">LedgerJournalCheckPost::updateSystemBlockCheckedPostedJournal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1185">LedgerJournalCheckPost::updateSystemBlockCheckedPostedJournal</span></span>|
|<span data-ttu-id="0bbb6-1186">LedgerJournalMultiPost.multiSelectPost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1186">LedgerJournalMultiPost.multiSelectPost</span></span>|
|<span data-ttu-id="0bbb6-1187">LedgerJournalTrans table.checkBankAccounts</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1187">LedgerJournalTrans table.checkBankAccounts</span></span>|
|<span data-ttu-id="0bbb6-1188">LedgerJournalTransUpdateVend::postNewVendorVoucher</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1188">LedgerJournalTransUpdateVend::postNewVendorVoucher</span></span>|
|<span data-ttu-id="0bbb6-1189">マップ ProjTableWizardCtrl::insertDB</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1189">Map ProjTableWizardCtrl::insertDB</span></span>|
|<span data-ttu-id="0bbb6-1190">マップ SalesPurchLine.calcPrice2LineAmount</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1190">Map SalesPurchLine.calcPrice2LineAmount</span></span>|
|<span data-ttu-id="0bbb6-1191">マップ SalesPurchLine.resetPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1191">Map SalesPurchLine.resetPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-1192">マップ SalesPurchLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1192">Map SalesPurchLine.setPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-1193">MarkupAllocation.sumValue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1193">MarkupAllocation.sumValue</span></span>|
|<span data-ttu-id="0bbb6-1194">MCRInventSearch.executeSearch</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1194">MCRInventSearch.executeSearch</span></span>|
|<span data-ttu-id="0bbb6-1195">MCROrderEventTable.Insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1195">MCROrderEventTable.Insert</span></span>|
|<span data-ttu-id="0bbb6-1196">McrPriceHistoryForm.insertPriceHistory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1196">McrPriceHistoryForm.insertPriceHistory</span></span>|
|<span data-ttu-id="0bbb6-1197">PmfFormCtrl.initPost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1197">PmfFormCtrl.initPost</span></span>|
|<span data-ttu-id="0bbb6-1198">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1198">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span></span>|
|<span data-ttu-id="0bbb6-1199">PriceDiscAdmCopy.updateNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1199">PriceDiscAdmCopy.updateNow</span></span>|
|<span data-ttu-id="0bbb6-1200">ProdJournalCheckPostProd::checkTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1200">ProdJournalCheckPostProd::checkTrans</span></span>|
|<span data-ttu-id="0bbb6-1201">ProdJournalCheckPostProd::postTransLedger</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1201">ProdJournalCheckPostProd::postTransLedger</span></span>|
|<span data-ttu-id="0bbb6-1202">ProdJournalCheckPostProd::postVoucher</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1202">ProdJournalCheckPostProd::postVoucher</span></span>|
|<span data-ttu-id="0bbb6-1203">ProdJournalCheckPostRoute.updateProdRouteScheduling</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1203">ProdJournalCheckPostRoute.updateProdRouteScheduling</span></span>|
|<span data-ttu-id="0bbb6-1204">ProdJournalCreateProd.createLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1204">ProdJournalCreateProd.createLines</span></span>|
|<span data-ttu-id="0bbb6-1205">ProdJournalCreateRoute.createLinesProdRoute</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1205">ProdJournalCreateRoute.createLinesProdRoute</span></span>|
|<span data-ttu-id="0bbb6-1206">ProdJournalFormTable.datasourceExecuteQueryPre</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1206">ProdJournalFormTable.datasourceExecuteQueryPre</span></span>|
|<span data-ttu-id="0bbb6-1207">ProdMultiBOMCalc.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1207">ProdMultiBOMCalc.run</span></span>|
|<span data-ttu-id="0bbb6-1208">ProdMultiCostEstimation.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1208">ProdMultiCostEstimation.run</span></span>|
|<span data-ttu-id="0bbb6-1209">ProdMultiHistoricalCost.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1209">ProdMultiHistoricalCost.run</span></span>|
|<span data-ttu-id="0bbb6-1210">ProdMultiRelease.insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1210">ProdMultiRelease.insert</span></span>|
|<span data-ttu-id="0bbb6-1211">ProdMultiRelease.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1211">ProdMultiRelease.run</span></span>|
|<span data-ttu-id="0bbb6-1212">ProdMultiReportFinished.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1212">ProdMultiReportFinished.main</span></span>|
|<span data-ttu-id="0bbb6-1213">ProdMultiReportFinished.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1213">ProdMultiReportFinished.run</span></span>|
|<span data-ttu-id="0bbb6-1214">ProdMultiSchedulingJob.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1214">ProdMultiSchedulingJob.run</span></span>|
|<span data-ttu-id="0bbb6-1215">ProdMultiSchedulingOperation.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1215">ProdMultiSchedulingOperation.run</span></span>|
|<span data-ttu-id="0bbb6-1216">ProdMultiStartUp.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1216">ProdMultiStartUp.run</span></span>|
|<span data-ttu-id="0bbb6-1217">ProdPurch.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1217">ProdPurch.createPurchTable</span></span>|
|<span data-ttu-id="0bbb6-1218">prodTableChangeQtySched.performActionFromDefaultValues</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1218">prodTableChangeQtySched.performActionFromDefaultValues</span></span>|
|<span data-ttu-id="0bbb6-1219">prodTableChangeQtySched.performActionFromPrompt</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1219">prodTableChangeQtySched.performActionFromPrompt</span></span>|
|<span data-ttu-id="0bbb6-1220">ProdUpdCostEstimation.costEstimateOperations</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1220">ProdUpdCostEstimation.costEstimateOperations</span></span>|
|<span data-ttu-id="0bbb6-1221">ProdUpdCostEstimation.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1221">ProdUpdCostEstimation.createPurchLine</span></span>|
|<span data-ttu-id="0bbb6-1222">ProdUpdReportFinished.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1222">ProdUpdReportFinished.run</span></span>|
|<span data-ttu-id="0bbb6-1223">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1223">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="0bbb6-1224">ProdUpdStartUp.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1224">ProdUpdStartUp.updateBOMConsumption</span></span>|
|<span data-ttu-id="0bbb6-1225">ProdUpdStartUp.updateRouteConsumption</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1225">ProdUpdStartUp.updateRouteConsumption</span></span>|
|<span data-ttu-id="0bbb6-1226">ProjAdjustmentSelect.doTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1226">ProjAdjustmentSelect.doTrans</span></span>|
|<span data-ttu-id="0bbb6-1227">ProjAdjustmentSelect.newQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1227">ProjAdjustmentSelect.newQuery</span></span>|
|<span data-ttu-id="0bbb6-1228">ProjAdjustmentSelect.Run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1228">ProjAdjustmentSelect.Run</span></span>|
|<span data-ttu-id="0bbb6-1229">ProjAdjustmentUpdate.checkTransChanged</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1229">ProjAdjustmentUpdate.checkTransChanged</span></span>|
|<span data-ttu-id="0bbb6-1230">ProjBudgetTransactionsManager.adjustBudget</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1230">ProjBudgetTransactionsManager.adjustBudget</span></span>|
|<span data-ttu-id="0bbb6-1231">ProjCopyForecastItem.copyToSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1231">ProjCopyForecastItem.copyToSalesLine</span></span>|
|<span data-ttu-id="0bbb6-1232">ProjCOstControl.createActualCosts</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1232">ProjCOstControl.createActualCosts</span></span>|
|<span data-ttu-id="0bbb6-1233">ProjCOstControl.createActuals</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1233">ProjCOstControl.createActuals</span></span>|
|<span data-ttu-id="0bbb6-1234">ProjCostControl.createAverageForRemaining</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1234">ProjCostControl.createAverageForRemaining</span></span>|
|<span data-ttu-id="0bbb6-1235">ProjCostControl.createCommittedCosts</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1235">ProjCostControl.createCommittedCosts</span></span>|
|<span data-ttu-id="0bbb6-1236">ProjCostControl.createForecastCosts</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1236">ProjCostControl.createForecastCosts</span></span>|
|<span data-ttu-id="0bbb6-1237">ProjCostControl.queryCommittedCosts</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1237">ProjCostControl.queryCommittedCosts</span></span>|
|<span data-ttu-id="0bbb6-1238">ProjCostControl.queryProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1238">ProjCostControl.queryProjTransPosting</span></span>|
|<span data-ttu-id="0bbb6-1239">ProjCostControl.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1239">ProjCostControl.run</span></span>|
|<span data-ttu-id="0bbb6-1240">ProjCostControl.validate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1240">ProjCostControl.validate</span></span>|
|<span data-ttu-id="0bbb6-1241">ProjForecastBudgetCopy.do_cost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1241">ProjForecastBudgetCopy.do_cost</span></span>|
|<span data-ttu-id="0bbb6-1242">ProjForecastBudgetCopy.do_empl</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1242">ProjForecastBudgetCopy.do_empl</span></span>|
|<span data-ttu-id="0bbb6-1243">ProjForecastBudgetCopy.do_OnaCC</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1243">ProjForecastBudgetCopy.do_OnaCC</span></span>|
|<span data-ttu-id="0bbb6-1244">ProjForecastBudgetCopy.do_Revenue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1244">ProjForecastBudgetCopy.do_Revenue</span></span>|
|<span data-ttu-id="0bbb6-1245">ProjForecastBudgetCopy.do_Sales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1245">ProjForecastBudgetCopy.do_Sales</span></span>|
|<span data-ttu-id="0bbb6-1246">ProjForecastBudgetCopy.initQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1246">ProjForecastBudgetCopy.initQuery</span></span>|
|<span data-ttu-id="0bbb6-1247">ProjForecastBudgetCopy.validate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1247">ProjForecastBudgetCopy.validate</span></span>|
|<span data-ttu-id="0bbb6-1248">ProjForecastBudgetDelete.initQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1248">ProjForecastBudgetDelete.initQuery</span></span>|
|<span data-ttu-id="0bbb6-1249">ProjForecastTransferFromWbs.</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1249">ProjForecastTransferFromWbs.</span></span> <span data-ttu-id="0bbb6-1250">transferItemToForecast</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1250">transferItemToForecast</span></span>|
|<span data-ttu-id="0bbb6-1251">ProjFundingEngine.allocate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1251">ProjFundingEngine.allocate</span></span>|
|<span data-ttu-id="0bbb6-1252">ProjFundingEngine.isAmountWithinFundingLimits</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1252">ProjFundingEngine.isAmountWithinFundingLimits</span></span>|
|<span data-ttu-id="0bbb6-1253">ProjFundingEngine.updateFundingLimits</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1253">ProjFundingEngine.updateFundingLimits</span></span>|
|<span data-ttu-id="0bbb6-1254">ProjInvoiceChooseNormal.dialog</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1254">ProjInvoiceChooseNormal.dialog</span></span>|
|<span data-ttu-id="0bbb6-1255">ProjInvoiceJournalCreate.initTotals</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1255">ProjInvoiceJournalCreate.initTotals</span></span>|
|<span data-ttu-id="0bbb6-1256">ProjInvoiceJournalPost.createProjInvoiceCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1256">ProjInvoiceJournalPost.createProjInvoiceCost</span></span>|
|<span data-ttu-id="0bbb6-1257">ProjInvoiceJournalPost.createProjInvoiceEmpl</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1257">ProjInvoiceJournalPost.createProjInvoiceEmpl</span></span>|
|<span data-ttu-id="0bbb6-1258">ProjInvoiceJournalPost.createProjInvoiceItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1258">ProjInvoiceJournalPost.createProjInvoiceItem</span></span>|
|<span data-ttu-id="0bbb6-1259">ProjInvoiceJournalPost.createProjInvoiceOnAcc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1259">ProjInvoiceJournalPost.createProjInvoiceOnAcc</span></span>|
|<span data-ttu-id="0bbb6-1260">ProjInvoiceJournalPost.createProjInvoiceRevenue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1260">ProjInvoiceJournalPost.createProjInvoiceRevenue</span></span>|
|<span data-ttu-id="0bbb6-1261">ProjInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1261">ProjInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="0bbb6-1262">ProjInvoiceProposalCreateLines.runSalesLineQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1262">ProjInvoiceProposalCreateLines.runSalesLineQuery</span></span>|
|<span data-ttu-id="0bbb6-1263">ProjInvoiceProposalCreateLines.runTransactions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1263">ProjInvoiceProposalCreateLines.runTransactions</span></span>|
|<span data-ttu-id="0bbb6-1264">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1264">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="0bbb6-1265">ProjInvoiceProposalNormalPeriodic.createParameters</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1265">ProjInvoiceProposalNormalPeriodic.createParameters</span></span>|
|<span data-ttu-id="0bbb6-1266">ProjInvoiceProposalPeriodic.dialog</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1266">ProjInvoiceProposalPeriodic.dialog</span></span>|
|<span data-ttu-id="0bbb6-1267">ProjJournalCheckPost.processHourJournalResourceRateCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1267">ProjJournalCheckPost.processHourJournalResourceRateCost</span></span>|
|<span data-ttu-id="0bbb6-1268">ProjLedger.initFromProjectPostingTransaction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1268">ProjLedger.initFromProjectPostingTransaction</span></span>|
|<span data-ttu-id="0bbb6-1269">ProjLedgerUpdate.insert</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1269">ProjLedgerUpdate.insert</span></span>|
|<span data-ttu-id="0bbb6-1270">ProjPlanVersionsManager.copyTasks</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1270">ProjPlanVersionsManager.copyTasks</span></span>|
|<span data-ttu-id="0bbb6-1271">ProjProposalTotals.calc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1271">ProjProposalTotals.calc</span></span>|
|<span data-ttu-id="0bbb6-1272">ProjSplitBill.buildRuleQR</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1272">ProjSplitBill.buildRuleQR</span></span>|
|<span data-ttu-id="0bbb6-1273">ProjSplitBill.split</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1273">ProjSplitBill.split</span></span>|
|<span data-ttu-id="0bbb6-1274">ProjStatisticCalc.mapPSAEntityToTmpProjStatistic</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1274">ProjStatisticCalc.mapPSAEntityToTmpProjStatistic</span></span>|
|<span data-ttu-id="0bbb6-1275">ProjValCheckTrans.setVariablesFromBuffer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1275">ProjValCheckTrans.setVariablesFromBuffer</span></span>|
|<span data-ttu-id="0bbb6-1276">PsaCustomerRetention.createFeeTransaction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1276">PsaCustomerRetention.createFeeTransaction</span></span>|
|<span data-ttu-id="0bbb6-1277">PsaGenerateQuotationLines.createSalesQuotationLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1277">PsaGenerateQuotationLines.createSalesQuotationLines</span></span>|
|<span data-ttu-id="0bbb6-1278">PSAProjInvoiceDP::insertPSAProjInvoiceHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1278">PsaProjInvoiceDP::insertPSAProjInvoiceHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1279">PsaProjInvoiceDP::insertPSAProjInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1279">PsaProjInvoiceDP::insertPSAProjInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-1280">PSARetentionRelease.insertLineRecords</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1280">PSARetentionRelease.insertLineRecords</span></span>|
|<span data-ttu-id="0bbb6-1281">PurchAgreementGenerateReleaseOrder.check</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1281">PurchAgreementGenerateReleaseOrder.check</span></span>|
|<span data-ttu-id="0bbb6-1282">PurchAutoCreate_RFQ.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1282">PurchAutoCreate_RFQ.createPurchLine</span></span>|
|<span data-ttu-id="0bbb6-1283">PurchAutoCreate_Sales.createLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1283">PurchAutoCreate_Sales.createLine</span></span>|
|<span data-ttu-id="0bbb6-1284">PurchCancel.cancelMarkup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1284">PurchCancel.cancelMarkup</span></span>|
|<span data-ttu-id="0bbb6-1285">PurchCancel.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1285">PurchCancel.run</span></span>|
|<span data-ttu-id="0bbb6-1286">PurchCopying.copyLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1286">PurchCopying.copyLine</span></span>|
|<span data-ttu-id="0bbb6-1287">PurchCreateFromSalesOrder.mcrDropChipCreateTmpFrmVirtual</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1287">PurchCreateFromSalesOrder.mcrDropChipCreateTmpFrmVirtual</span></span>|
|<span data-ttu-id="0bbb6-1288">PurchCreateFromSalesOrder.preMatchIncludedLinesWithAgreements</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1288">PurchCreateFromSalesOrder.preMatchIncludedLinesWithAgreements</span></span>|
|<span data-ttu-id="0bbb6-1289">PurchFormLetter.PrePromptInit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1289">PurchFormLetter.PrePromptInit</span></span>|
|<span data-ttu-id="0bbb6-1290">PurchformLetter::Main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1290">PurchformLetter::Main</span></span>|
|<span data-ttu-id="0bbb6-1291">PurchFormLetter::MainOnServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1291">PurchFormLetter::MainOnServer</span></span>|
|<span data-ttu-id="0bbb6-1292">PurchFormletterParmData.createParmTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1292">PurchFormletterParmData.createParmTable</span></span>|
|<span data-ttu-id="0bbb6-1293">PurchFormletterParmDataInvoice.chooseLinesFromPurchSelectLinesManager</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1293">PurchFormletterParmDataInvoice.chooseLinesFromPurchSelectLinesManager</span></span>|
|<span data-ttu-id="0bbb6-1294">PurchLineType.intercompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1294">PurchLineType.intercompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-1295">PurchLineType_Project.initFromInventTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1295">PurchLineType_Project.initFromInventTable</span></span>|
|<span data-ttu-id="0bbb6-1296">PurchLineType_WithMultipleDeliveries.recalculateDeliveryScheduleOrderLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1296">PurchLineType_WithMultipleDeliveries.recalculateDeliveryScheduleOrderLine</span></span>|
|<span data-ttu-id="0bbb6-1297">PurchPackingSlipDP::setPurchPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1297">PurchPackingSlipDP::setPurchPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-1298">PurchPackingSlipDP::setPurchPackingSlipHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1298">PurchPackingSlipDP::setPurchPackingSlipHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1299">PurchPurchaseOrderDP.createData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1299">PurchPurchaseOrderDP.createData</span></span>|
|<span data-ttu-id="0bbb6-1300">PurchPurchaseOrderDP.initializePurchPurchaseOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1300">PurchPurchaseOrderDP.initializePurchPurchaseOrderHeader</span></span>|
|<span data-ttu-id="0bbb6-1301">PurchPurchaseOrderDP.processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1301">PurchPurchaseOrderDP.processReport</span></span>|
|<span data-ttu-id="0bbb6-1302">PurchPurchaseOrderDP.setPurchPurchaseOrderDetails</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1302">PurchPurchaseOrderDP.setPurchPurchaseOrderDetails</span></span>|
|<span data-ttu-id="0bbb6-1303">PurchPurchaseOrderDP::setPurchPurchaseOrderDetails</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1303">PurchPurchaseOrderDP::setPurchPurchaseOrderDetails</span></span>|
|<span data-ttu-id="0bbb6-1304">PurchPurchaseOrderDP::setPurchPurchaseOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1304">PurchPurchaseOrderDP::setPurchPurchaseOrderHeader</span></span>|
|<span data-ttu-id="0bbb6-1305">PurchReceiptsListDP::setPurchReceiptsListDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1305">PurchReceiptsListDP::setPurchReceiptsListDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-1306">PurchReceiptsListDP::setPurchReceiptsListHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1306">PurchReceiptsListDP::setPurchReceiptsListHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1307">PurchReqTable2LineField.lineUpdateDescription</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1307">PurchReqTable2LineField.lineUpdateDescription</span></span>|
|<span data-ttu-id="0bbb6-1308">PurchRFQCaseAutoCreate.newAutoCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1308">PurchRFQCaseAutoCreate.newAutoCreate</span></span>|
|<span data-ttu-id="0bbb6-1309">PurchRFQCompare.BuildReplyLineList</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1309">PurchRFQCompare.BuildReplyLineList</span></span>|
|<span data-ttu-id="0bbb6-1310">PurchRFQSendDP::processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1310">PurchRFQSendDP::processReport</span></span>|
|<span data-ttu-id="0bbb6-1311">PurchRFQSendJournalCreate.createOrUpdateRFQ</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1311">PurchRFQSendJournalCreate.createOrUpdateRFQ</span></span>|
|<span data-ttu-id="0bbb6-1312">PurchTable2LineField.getFieldDescription</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1312">PurchTable2LineField.getFieldDescription</span></span>|
|<span data-ttu-id="0bbb6-1313">PurchTableType.intercompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1313">PurchTableType.intercompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-1314">ReqActionApplyPurchaseOrder.applyActionToReferencedOrder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1314">ReqActionApplyPurchaseOrder.applyActionToReferencedOrder</span></span>|
|<span data-ttu-id="0bbb6-1315">ReqBOMCreate.createBOM</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1315">ReqBOMCreate.createBOM</span></span>|
|<span data-ttu-id="0bbb6-1316">ReqCalc.mcrInsertItemContinuitySales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1316">ReqCalc.mcrInsertItemContinuitySales</span></span>|
|<span data-ttu-id="0bbb6-1317">ReqCalcScheduleItemTable.run</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1317">ReqCalcScheduleItemTable.run</span></span>|
|<span data-ttu-id="0bbb6-1318">ReqSetupDim.setReqItemTableGrouped</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1318">ReqSetupDim.setReqItemTableGrouped</span></span>|
|<span data-ttu-id="0bbb6-1319">ReqSupplyDemandScheduleModel.executeQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1319">ReqSupplyDemandScheduleModel.executeQuery</span></span>|
|<span data-ttu-id="0bbb6-1320">ReqSupplyDemandScheduleModel.insertPeriodValue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1320">ReqSupplyDemandScheduleModel.insertPeriodValue</span></span>|
|<span data-ttu-id="0bbb6-1321">ReqTransPoMarkChangeToRFQ.change2RFQ</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1321">ReqTransPoMarkChangeToRFQ.change2RFQ</span></span>|
|<span data-ttu-id="0bbb6-1322">ReqTransPoMarkFirm.create</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1322">ReqTransPoMarkFirm.create</span></span>|
|<span data-ttu-id="0bbb6-1323">ReqTransPoMarkFirm.createInventTransferLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1323">ReqTransPoMarkFirm.createInventTransferLine</span></span>|
|<span data-ttu-id="0bbb6-1324">ReqTransPoMarkFirm.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1324">ReqTransPoMarkFirm.createPurchLine</span></span>|
|<span data-ttu-id="0bbb6-1325">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1325">ReqTransPoMarkFirm.createPurchTable</span></span>|
|<span data-ttu-id="0bbb6-1326">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1326">ReqTransPoMarkFirm.firmSelectedPlannedOrders</span></span>|
|<span data-ttu-id="0bbb6-1327">RouteCopyToProd.copyTo</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1327">RouteCopyToProd.copyTo</span></span>|
|<span data-ttu-id="0bbb6-1328">SalesAgreementGenerateReleaseOrder.check</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1328">SalesAgreementGenerateReleaseOrder.check</span></span>|
|<span data-ttu-id="0bbb6-1329">SalesAgreementGenerateReleaseOrder.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1329">SalesAgreementGenerateReleaseOrder.main</span></span>|
|<span data-ttu-id="0bbb6-1330">SalesAutoCreate_ReleaseFromAgreement.createSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1330">SalesAutoCreate_ReleaseFromAgreement.createSalesLine</span></span>|
|<span data-ttu-id="0bbb6-1331">SalesAutoCreate_ReleaseFromAgreement.createSalesTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1331">SalesAutoCreate_ReleaseFromAgreement.createSalesTable</span></span>|
|<span data-ttu-id="0bbb6-1332">SalesAutoCreate_ReleaseOrder.createSalesTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1332">SalesAutoCreate_ReleaseOrder.createSalesTable</span></span>|
|<span data-ttu-id="0bbb6-1333">SalesConfirmDP.setSalesConfirmDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1333">SalesConfirmDP.setSalesConfirmDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-1334">SalesConfirmDP.setSalesConfirmHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1334">SalesConfirmDP.setSalesConfirmHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1335">SalesConfirmDP::setSalesConfirmDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1335">SalesConfirmDP::setSalesConfirmDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-1336">SalesConfirmDP::setSalesConfirmHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1336">SalesConfirmDP::setSalesConfirmHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1337">SalesCopying.copy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1337">SalesCopying.copy</span></span>|
|<span data-ttu-id="0bbb6-1338">SalesCopying.copyHeader</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1338">SalesCopying.copyHeader</span></span>|
|<span data-ttu-id="0bbb6-1339">SalesCopying.deleteLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1339">SalesCopying.deleteLines</span></span>|
|<span data-ttu-id="0bbb6-1340">SalesCopying_CreditNote.copy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1340">SalesCopying_CreditNote.copy</span></span>|
|<span data-ttu-id="0bbb6-1341">SalesCopying_CreditNote.copyHeader</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1341">SalesCopying_CreditNote.copyHeader</span></span>|
|<span data-ttu-id="0bbb6-1342">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1342">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="0bbb6-1343">SalesFormLetter.reselect</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1343">SalesFormLetter.reselect</span></span>|
|<span data-ttu-id="0bbb6-1344">SalesFormletterParmData.createParmLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1344">SalesFormletterParmData.createParmLine</span></span>|
|<span data-ttu-id="0bbb6-1345">SalesFormletterParmData::createParmTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1345">SalesFormletterParmData::createParmTable</span></span>|
|<span data-ttu-id="0bbb6-1346">SalesInvoiceController::outputReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1346">SalesInvoiceController::outputReport</span></span>|
|<span data-ttu-id="0bbb6-1347">SalesInvoiceDP.useExistingReportData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1347">SalesInvoiceDP.useExistingReportData</span></span>|
|<span data-ttu-id="0bbb6-1348">SalesInvoiceDP::insertIntoSalesInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1348">SalesInvoiceDP::insertIntoSalesInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="0bbb6-1349">SalesInvoiceDP::insertIntoSalesInvoiceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1349">SalesInvoiceDP::insertIntoSalesInvoiceTmp</span></span>|
|<span data-ttu-id="0bbb6-1350">SalesLineExplodeBOM.explode</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1350">SalesLineExplodeBOM.explode</span></span>|
|<span data-ttu-id="0bbb6-1351">SalesLineType.canPickingListBeRegistered</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1351">SalesLineType.canPickingListBeRegistered</span></span>|
|<span data-ttu-id="0bbb6-1352">SalesLineType.delete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1352">SalesLineType.delete</span></span>|
|<span data-ttu-id="0bbb6-1353">SalesLineType.initDimensionsSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1353">SalesLineType.initDimensionsSpecificDefaulting</span></span>|
|<span data-ttu-id="0bbb6-1354">SalesLineType.initFromSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1354">SalesLineType.initFromSalesLine</span></span>|
|<span data-ttu-id="0bbb6-1355">SalesLineType.interCompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1355">SalesLineType.interCompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-1356">SalesLineType.setSalesStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1356">SalesLineType.setSalesStatus</span></span>|
|<span data-ttu-id="0bbb6-1357">SalesLineType.validateField フィールド ShippingDateRequested および ShippingDateConfirmed</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1357">SalesLineType.validateField field  ShippingDateRequested and ShippingDateConfirmed</span></span>|
|<span data-ttu-id="0bbb6-1358">SalesPackingSlipDP.printDimHistory</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1358">SalesPackingSlipDP.printDimHistory</span></span>|
|<span data-ttu-id="0bbb6-1359">SalesPackingSlipDP::setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1359">SalesPackingSlipDP::setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-1360">SalesPackingSlipDP::setSalesPackingSlipHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1360">SalesPackingSlipDP::setSalesPackingSlipHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1361">SalesPurchTableToLineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1361">SalesPurchTableToLineUpdate.update</span></span>|
|<span data-ttu-id="0bbb6-1362">SalesQuantity_PackingSlip.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1362">SalesQuantity_PackingSlip.calcQtySales</span></span>|
|<span data-ttu-id="0bbb6-1363">SalesQuantity_PickingList.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1363">SalesQuantity_PickingList.calcQtySales</span></span>|
|<span data-ttu-id="0bbb6-1364">SalesQuotationConfirmationDP::setSalesQuotationDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1364">SalesQuotationConfirmationDP::setSalesQuotationDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-1365">SalesQuotationConfirmationDP::setSalesQuotationHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1365">SalesQuotationConfirmationDP::setSalesQuotationHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1366">SalesQuotationCopying.buildTreeControl</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1366">SalesQuotationCopying.buildTreeControl</span></span>|
|<span data-ttu-id="0bbb6-1367">SalesQuotationCopying.Copy</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1367">SalesQuotationCopying.Copy</span></span>|
|<span data-ttu-id="0bbb6-1368">SalesQuotationDP::setSalesQuotationDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1368">SalesQuotationDP::setSalesQuotationDetailsTmp</span></span>|
|<span data-ttu-id="0bbb6-1369">SalesQuotationDP::setSalesQuotationHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1369">SalesQuotationDP::setSalesQuotationHeaderTmp</span></span>|
|<span data-ttu-id="0bbb6-1370">SalesQuotationEditLinesForm.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1370">SalesQuotationEditLinesForm.mainOnServer</span></span>|
|<span data-ttu-id="0bbb6-1371">SalesQuotationEditLinesForm_Proj_Confirm.queryBuildSalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1371">SalesQuotationEditLinesForm_Proj_Confirm.queryBuildSalesQuotationTable</span></span>|
|<span data-ttu-id="0bbb6-1372">SalesQuotationEditLinesForm_Proj_Send.queryBuildSalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1372">SalesQuotationEditLinesForm_Proj_Send.queryBuildSalesQuotationTable</span></span>|
|<span data-ttu-id="0bbb6-1373">SalesQuotationEditLinesForm_Sales_Confir.updateNow</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1373">SalesQuotationEditLinesForm_Sales_Confir.updateNow</span></span>|
|<span data-ttu-id="0bbb6-1374">SalesQuotationEditLinesForm_Sales_Confirm.createSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1374">SalesQuotationEditLinesForm_Sales_Confirm.createSalesLine</span></span>|
|<span data-ttu-id="0bbb6-1375">SalesQuotationEditLinesForm_Sales_Send.checkLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1375">SalesQuotationEditLinesForm_Sales_Send.checkLines</span></span>|
|<span data-ttu-id="0bbb6-1376">SalesQuotationJumpRef.main</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1376">SalesQuotationJumpRef.main</span></span>|
|<span data-ttu-id="0bbb6-1377">SalesQuotationLineType.initFromSalesQuotationLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1377">SalesQuotationLineType.initFromSalesQuotationLine</span></span>|
|<span data-ttu-id="0bbb6-1378">SalesQuotationLineType_Proj.validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1378">SalesQuotationLineType_Proj.validateWrite</span></span>|
|<span data-ttu-id="0bbb6-1379">SalesQuotationProjLinkWizard.transferForecastToProject</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1379">SalesQuotationProjLinkWizard.transferForecastToProject</span></span>|
|<span data-ttu-id="0bbb6-1380">SalesQuotationProjLinkWizard.transferItemReq</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1380">SalesQuotationProjLinkWizard.transferItemReq</span></span>|
|<span data-ttu-id="0bbb6-1381">SalesQuotationTransferToProject.transferItemsToForecast</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1381">SalesQuotationTransferToProject.transferItemsToForecast</span></span>|
|<span data-ttu-id="0bbb6-1382">SalesQuotationTransferToProject.transferItemsToItemReq</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1382">SalesQuotationTransferToProject.transferItemsToItemReq</span></span>|
|<span data-ttu-id="0bbb6-1383">SalesQuotationUpdate.getCallerModuleFromParm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1383">SalesQuotationUpdate.getCallerModuleFromParm</span></span>|
|<span data-ttu-id="0bbb6-1384">SalesTableForm.initValues</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1384">SalesTableForm.initValues</span></span>|
|<span data-ttu-id="0bbb6-1385">SalesTableForm_DeliverySchedule.updateSalesLineTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1385">SalesTableForm_DeliverySchedule.updateSalesLineTable</span></span>|
|<span data-ttu-id="0bbb6-1386">SalesTableType.intercompanyMirror</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1386">SalesTableType.intercompanyMirror</span></span>|
|<span data-ttu-id="0bbb6-1387">SalesTableType.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1387">SalesTableType.update</span></span>|
|<span data-ttu-id="0bbb6-1388">SalesTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1388">SalesTableType.validateDelete</span></span>|
|<span data-ttu-id="0bbb6-1389">smmSalesCustItemStatisticsDP::processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1389">smmSalesCustItemStatisticsDP::processReport</span></span>|
|<span data-ttu-id="0bbb6-1390">テーブル CaseDetailBase.validateWrite</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1390">Table CaseDetailBase.validateWrite</span></span>|
|<span data-ttu-id="0bbb6-1391">テーブル CustCollectionLetterJour.updateCollectionLetterCodeCustTrans()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1391">Table CustCollectionLetterJour.updateCollectionLetterCodeCustTrans()</span></span>|
|<span data-ttu-id="0bbb6-1392">テーブル EcoResProductTranslation.queryAddCompanyLanguage</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1392">Table EcoResProductTranslation.queryAddCompanyLanguage</span></span>|
|<span data-ttu-id="0bbb6-1393">テーブル InventLocation::lookupBySiteIdAllTypes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1393">Table InventLocation::lookupBySiteIdAllTypes</span></span>|
|<span data-ttu-id="0bbb6-1394">テーブル InventPosting.accountGroup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1394">Table InventPosting.accountGroup</span></span>|
|<span data-ttu-id="0bbb6-1395">テーブル InventPosting.accountItemLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1395">Table InventPosting.accountItemLedgerDimension</span></span>|
|<span data-ttu-id="0bbb6-1396">テーブル InventPosting.deleteFromCust</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1396">Table InventPosting.deleteFromCust</span></span>|
|<span data-ttu-id="0bbb6-1397">テーブル InventPosting.deleteFromVend</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1397">Table InventPosting.deleteFromVend</span></span>|
|<span data-ttu-id="0bbb6-1398">テーブル InventTable.defaultProductDescription</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1398">Table InventTable.defaultProductDescription</span></span>|
|<span data-ttu-id="0bbb6-1399">テーブル InventTable.defaultProductName</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1399">Table InventTable.defaultProductName</span></span>|
|<span data-ttu-id="0bbb6-1400">テーブル InventTable.lookupBOMId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1400">Table InventTable.lookupBOMId</span></span>|
|<span data-ttu-id="0bbb6-1401">テーブル InventTrans.updateMarkReqTransCov</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1401">Table InventTrans.updateMarkReqTransCov</span></span>|
|<span data-ttu-id="0bbb6-1402">テーブル PaymTerm.due</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1402">Table PaymTerm.due</span></span>|
|<span data-ttu-id="0bbb6-1403">テーブル ProdBOM.updateStartUp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1403">Table ProdBOM.updateStartUp</span></span>|
|<span data-ttu-id="0bbb6-1404">テーブル ProdBOM.updateSubPurch</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1404">Table ProdBOM.updateSubPurch</span></span>|
|<span data-ttu-id="0bbb6-1405">テーブル ProdJournalBOM.insertJournalCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1405">Table ProdJournalBOM.insertJournalCreate</span></span>|
|<span data-ttu-id="0bbb6-1406">テーブル ProdJournalBOM.lookupTransId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1406">Table ProdJournalBOM.lookupTransId</span></span>|
|<span data-ttu-id="0bbb6-1407">テーブル ProdTable.validateRouteId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1407">Table ProdTable.validateRouteId</span></span>|
|<span data-ttu-id="0bbb6-1408">テーブル ProjBegBalJournalTrans_CostSales.postProjTransactionCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1408">Table ProjBegBalJournalTrans_CostSales.postProjTransactionCost</span></span>|
|<span data-ttu-id="0bbb6-1409">テーブル ProjBegBalJournalTrans_CostSales.postProjTransactionHour</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1409">Table ProjBegBalJournalTrans_CostSales.postProjTransactionHour</span></span>|
|<span data-ttu-id="0bbb6-1410">テーブル ProjBegBalJournalTrans_CostSales.postProjTransactionItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1410">Table ProjBegBalJournalTrans_CostSales.postProjTransactionItem</span></span>|
|<span data-ttu-id="0bbb6-1411">テーブル ProjBegBalJournalTrans_Fee.postProjTransaction</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1411">Table ProjBegBalJournalTrans_Fee.postProjTransaction</span></span>|
|<span data-ttu-id="0bbb6-1412">テーブル ProjBegBalJournalTrans_OnAcc.postProjTransactionCost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1412">Table ProjBegBalJournalTrans_OnAcc.postProjTransactionCost</span></span>|
|<span data-ttu-id="0bbb6-1413">テーブル PurchLine.initBarCode</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1413">Table PurchLine.initBarCode</span></span>|
|<span data-ttu-id="0bbb6-1414">テーブル PurchLine.priceDateDelegate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1414">Table PurchLine.priceDateDelegate</span></span>|
|<span data-ttu-id="0bbb6-1415">テーブル PurchLine.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1415">Table PurchLine.setPriceDisc</span></span>|
|<span data-ttu-id="0bbb6-1416">テーブル PurchTable.updateFromPurchReqLineMap</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1416">Table PurchTable.updateFromPurchReqLineMap</span></span>|
|<span data-ttu-id="0bbb6-1417">テーブル ReqPO.updateBOMRoute</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1417">Table ReqPO.updateBOMRoute</span></span>|
|<span data-ttu-id="0bbb6-1418">テーブル ReqTrans.bulkInitFromInventTransOrigin</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1418">Table ReqTrans.bulkInitFromInventTransOrigin</span></span>|
|<span data-ttu-id="0bbb6-1419">テーブル RouteOpr.validateFieldValue</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1419">Table RouteOpr.validateFieldValue</span></span>|
|<span data-ttu-id="0bbb6-1420">テーブル RouteVersion.checkExistInventSiteId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1420">Table RouteVersion.checkExistInventSiteId</span></span>|
|<span data-ttu-id="0bbb6-1421">テーブル SalesLine.checkPriceDate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1421">Table SalesLine.checkPriceDate</span></span>|
|<span data-ttu-id="0bbb6-1422">テーブル Salesline.convertCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1422">Table Salesline.convertCurrencyCode</span></span>|
|<span data-ttu-id="0bbb6-1423">テーブル SalesLine.convertToDeliverySchedule</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1423">Table SalesLine.convertToDeliverySchedule</span></span>|
|<span data-ttu-id="0bbb6-1424">テーブル SalesLine.createFromTmpFrmVirtualIL</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1424">Table SalesLine.createFromTmpFrmVirtualIL</span></span>|
|<span data-ttu-id="0bbb6-1425">テーブル SalesLine.createReplacement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1425">Table SalesLine.createReplacement</span></span>|
|<span data-ttu-id="0bbb6-1426">テーブル SalesLine.createSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1426">Table SalesLine.createSalesLine</span></span>|
|<span data-ttu-id="0bbb6-1427">テーブル SalesLine.expandBOM</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1427">Table SalesLine.expandBOM</span></span>|
|<span data-ttu-id="0bbb6-1428">テーブル Salesline.modifyInventDimSet</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1428">Table Salesline.modifyInventDimSet</span></span>|
|<span data-ttu-id="0bbb6-1429">テーブル SalesLine.priceDateDelegate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1429">Table SalesLine.priceDateDelegate</span></span>|
|<span data-ttu-id="0bbb6-1430">テーブル salesLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1430">Table salesLine.setPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-1431">テーブル Salesline.splitReturnLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1431">Table Salesline.splitReturnLine</span></span>|
|<span data-ttu-id="0bbb6-1432">テーブル SalesLine::createFromSalesQuotationLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1432">Table SalesLine::createFromSalesQuotationLine</span></span>|
|<span data-ttu-id="0bbb6-1433">テーブル SalesQuotationLine.createFromTmpFrmVirtual</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1433">Table SalesQuotationLine.createFromTmpFrmVirtual</span></span>|
|<span data-ttu-id="0bbb6-1434">テーブル SalesQuotationLine.modifiedField</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1434">Table SalesQuotationLine.modifiedField</span></span>|
|<span data-ttu-id="0bbb6-1435">テーブル SalesQuotationLine.modifyInventDim</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1435">Table SalesQuotationLine.modifyInventDim</span></span>|
|<span data-ttu-id="0bbb6-1436">テーブル SalesQuotationTable.copyAddressToLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1436">Table SalesQuotationTable.copyAddressToLine</span></span>|
|<span data-ttu-id="0bbb6-1437">テーブル SalesQuotationTable.lookupTemplateName</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1437">Table SalesQuotationTable.lookupTemplateName</span></span>|
|<span data-ttu-id="0bbb6-1438">テーブル SalesTable.copyAddressToLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1438">Table SalesTable.copyAddressToLine</span></span>|
|<span data-ttu-id="0bbb6-1439">テーブル SalesTable.copyRMALines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1439">Table SalesTable.copyRMALines</span></span>|
|<span data-ttu-id="0bbb6-1440">テーブル SalesTable.copyThirdPartyBillingAddressToLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1440">Table SalesTable.copyThirdPartyBillingAddressToLine</span></span>|
|<span data-ttu-id="0bbb6-1441">テーブル SalesTable.existingJournals</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1441">Table SalesTable.existingJournals</span></span>|
|<span data-ttu-id="0bbb6-1442">テーブル SalesTable.initFromCustTableIL</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1442">Table SalesTable.initFromCustTableIL</span></span>|
|<span data-ttu-id="0bbb6-1443">テーブル SalesTable.initFromProjTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1443">Table SalesTable.initFromProjTable</span></span>|
|<span data-ttu-id="0bbb6-1444">テーブル SalesTable.initFromSalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1444">Table SalesTable.initFromSalesQuotationTable</span></span>|
|<span data-ttu-id="0bbb6-1445">テーブル SalesTable.unlinkAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1445">Table SalesTable.unlinkAgreement</span></span>|
|<span data-ttu-id="0bbb6-1446">テーブル WHSAccountItemStatusDefault.checkModuleAccountNum</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1446">Table WHSAccountItemStatusDefault.checkModuleAccountNum</span></span>|
|<span data-ttu-id="0bbb6-1447">テーブル WHSLoadLine.delete</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1447">Table WHSLoadLine.delete</span></span>|
|<span data-ttu-id="0bbb6-1448">テーブル WHSLoadLine.updateReleaseQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1448">Table WHSLoadLine.updateReleaseQty</span></span>|
|<span data-ttu-id="0bbb6-1449">テーブル WhsLoadLine.validateQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1449">Table WhsLoadLine.validateQty</span></span>|
|<span data-ttu-id="0bbb6-1450">テーブル WHSLoadTable.assignOriginInfo</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1450">Table WHSLoadTable.assignOriginInfo</span></span>|
|<span data-ttu-id="0bbb6-1451">テーブル WHSProdTable.pickMore</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1451">Table WHSProdTable.pickMore</span></span>|
|<span data-ttu-id="0bbb6-1452">テーブル WhsWorkTabke.lockUnLockWork</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1452">Table WhsWorkTabke.lockUnLockWork</span></span>|
|<span data-ttu-id="0bbb6-1453">テーブル WMSBillOfLading.constructFromInvoice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1453">Table WMSBillOfLading.constructFromInvoice</span></span>|
|<span data-ttu-id="0bbb6-1454">テーブル WMSBillOfLading.constructFromPackingSlip</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1454">Table WMSBillOfLading.constructFromPackingSlip</span></span>|
|<span data-ttu-id="0bbb6-1455">テーブル WMSBillOfLading.constructFromShipment</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1455">Table WMSBillOfLading.constructFromShipment</span></span>|
|<span data-ttu-id="0bbb6-1456">テーブル WMSOrderTrans.loopWMSOrderTransMulti</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1456">Table WMSOrderTrans.loopWMSOrderTransMulti</span></span>|
|<span data-ttu-id="0bbb6-1457">テーブル WrkCtrActivityRequirementSet.copyRequirements</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1457">Table WrkCtrActivityRequirementSet.copyRequirements</span></span>|
|<span data-ttu-id="0bbb6-1458">テーブル WrkCtrActivityRequirementSet.schedulingProperties</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1458">Table WrkCtrActivityRequirementSet.schedulingProperties</span></span>|
|<span data-ttu-id="0bbb6-1459">テーブル SalesLine/Methods/setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1459">Tables SalesLine/Methods/setPriceDisc</span></span>|
|<span data-ttu-id="0bbb6-1460">TamDeductionUpdate_Deny.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1460">TamDeductionUpdate_Deny.update</span></span>|
|<span data-ttu-id="0bbb6-1461">TmsProcessXML_Container.readShipContainer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1461">TmsProcessXML_Container.readShipContainer</span></span>|
|<span data-ttu-id="0bbb6-1462">TmsProcessXML_Shipment.readShipContainer</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1462">TmsProcessXML_Shipment.readShipContainer</span></span>|
|<span data-ttu-id="0bbb6-1463">TradeInterCompany.insertInterCompanyInventDim</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1463">TradeInterCompany.insertInterCompanyInventDim</span></span>|
|<span data-ttu-id="0bbb6-1464">TradeInterCompanyConv.axPurchItemId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1464">TradeInterCompanyConv.axPurchItemId</span></span>|
|<span data-ttu-id="0bbb6-1465">TradeInterCompanyConv.axSalesItemId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1465">TradeInterCompanyConv.axSalesItemId</span></span>|
|<span data-ttu-id="0bbb6-1466">TransactionReversal_Asset.reversalBook</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1466">TransactionReversal_Asset.reversalBook</span></span>|
|<span data-ttu-id="0bbb6-1467">TransactionReversal_Cust::reversal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1467">TransactionReversal_Cust::reversal</span></span>|
|<span data-ttu-id="0bbb6-1468">TransactionReversal_CustVend.createCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1468">TransactionReversal_CustVend.createCustVendTrans</span></span>|
|<span data-ttu-id="0bbb6-1469">VendInvoiceDocumentDP::insertVendInvoiceDocumentTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1469">VendInvoiceDocumentDP::insertVendInvoiceDocumentTmp</span></span>|
|<span data-ttu-id="0bbb6-1470">VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1470">VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice</span></span>|
|<span data-ttu-id="0bbb6-1471">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1471">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="0bbb6-1472">VersioningDocument.change</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1472">VersioningDocument.change</span></span>|
|<span data-ttu-id="0bbb6-1473">VersioningPurchaseOrder.createChangeRequest</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1473">VersioningPurchaseOrder.createChangeRequest</span></span>|
|<span data-ttu-id="0bbb6-1474">WhsCycleCountCreateThreshold.processCycleCountThresholdItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1474">WhsCycleCountCreateThreshold.processCycleCountThresholdItem</span></span>|
|<span data-ttu-id="0bbb6-1475">WHSInventOnHandReserve.changeReservation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1475">WHSInventOnHandReserve.changeReservation</span></span>|
|<span data-ttu-id="0bbb6-1476">WHSLaborStandards.findLaborStandardByItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1476">WHSLaborStandards.findLaborStandardByItem</span></span>|
|<span data-ttu-id="0bbb6-1477">WHSLoadLine.update</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1477">WHSLoadLine.update</span></span>|
|<span data-ttu-id="0bbb6-1478">WHSLoadTable.tmsLoadConfirmation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1478">WHSLoadTable.tmsLoadConfirmation</span></span>|
|<span data-ttu-id="0bbb6-1479">WHSLocationBuild</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1479">WHSLocationBuild</span></span>|
|<span data-ttu-id="0bbb6-1480">WHSLocationDirective.findLocation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1480">WHSLocationDirective.findLocation</span></span>|
|<span data-ttu-id="0bbb6-1481">WHSLocationDirective.findPickPutLocation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1481">WHSLocationDirective.findPickPutLocation</span></span>|
|<span data-ttu-id="0bbb6-1482">WHSLocationDirectiveActionQuery.modifyPickLocDirActionQuery</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1482">WHSLocationDirectiveActionQuery.modifyPickLocDirActionQuery</span></span>|
|<span data-ttu-id="0bbb6-1483">WHSPool.pickFromWorkCenter</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1483">WHSPool.pickFromWorkCenter</span></span>|
|<span data-ttu-id="0bbb6-1484">WHSPostEngineBase.prodCreateWork</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1484">WHSPostEngineBase.prodCreateWork</span></span>|
|<span data-ttu-id="0bbb6-1485">WHSPostEngineBase.prodPickQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1485">WHSPostEngineBase.prodPickQty</span></span>|
|<span data-ttu-id="0bbb6-1486">WhsRfControlData.getClusterPickQty</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1486">WhsRfControlData.getClusterPickQty</span></span>|
|<span data-ttu-id="0bbb6-1487">WHSRFControlData.processControl</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1487">WHSRFControlData.processControl</span></span>|
|<span data-ttu-id="0bbb6-1488">WhsShipConfirm.canShipConfirm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1488">WhsShipConfirm.canShipConfirm</span></span>|
|<span data-ttu-id="0bbb6-1489">WHSShipConfirm.createInventTransferParmLineFromContainerTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1489">WHSShipConfirm.createInventTransferParmLineFromContainerTable</span></span>|
|<span data-ttu-id="0bbb6-1490">WHSShipConfirm.runTransferShip</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1490">WHSShipConfirm.runTransferShip</span></span>|
|<span data-ttu-id="0bbb6-1491">WhsShipConfirn.validateAllAllowedForOverOrUnderdeliveryWorkQtyHasBeenPicked</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1491">WhsShipConfirn.validateAllAllowedForOverOrUnderdeliveryWorkQtyHasBeenPicked</span></span>|
|<span data-ttu-id="0bbb6-1492">WHSSplitWork.splitWork</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1492">WHSSplitWork.splitWork</span></span>|
|<span data-ttu-id="0bbb6-1493">WHSWorkClusterTable.cleanupCluster</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1493">WHSWorkClusterTable.cleanupCluster</span></span>|
|<span data-ttu-id="0bbb6-1494">WHSWorkCreateProdPut.insertProdParmforCoByProduct</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1494">WHSWorkCreateProdPut.insertProdParmforCoByProduct</span></span>|
|<span data-ttu-id="0bbb6-1495">WHSWorkCreateProdPut.insertProdParmforProdItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1495">WHSWorkCreateProdPut.insertProdParmforProdItem</span></span>|
|<span data-ttu-id="0bbb6-1496">WhsWorkExecute.getFirstOpenLineSystemDirected</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1496">WhsWorkExecute.getFirstOpenLineSystemDirected</span></span>|
|<span data-ttu-id="0bbb6-1497">WHSWorkExecute.overPickByItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1497">WHSWorkExecute.overPickByItem</span></span>|
|<span data-ttu-id="0bbb6-1498">WHSWorkExecute.putAwayToLocation</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1498">WHSWorkExecute.putAwayToLocation</span></span>|
|<span data-ttu-id="0bbb6-1499">WHSWorkExecute.scanLicensePlate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1499">WHSWorkExecute.scanLicensePlate</span></span>|
|<span data-ttu-id="0bbb6-1500">WHSWorkExecuteDisplay.buildPORecTrackingDimensions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1500">WHSWorkExecuteDisplay.buildPORecTrackingDimensions</span></span>|
|<span data-ttu-id="0bbb6-1501">WhsWorkExecuteDisplayCycleCount.findOrCreateCycleCountWorkLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1501">WhsWorkExecuteDisplayCycleCount.findOrCreateCycleCountWorkLines</span></span>|
|<span data-ttu-id="0bbb6-1502">WhsWorkExecuteDisplayLPReceiving.displayForm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1502">WhsWorkExecuteDisplayLPReceiving.displayForm</span></span>|
|<span data-ttu-id="0bbb6-1503">WHSWorkExecuteDisplayMixedLPReceiving.displayForm</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1503">WHSWorkExecuteDisplayMixedLPReceiving.displayForm</span></span>|
|<span data-ttu-id="0bbb6-1504">WHSWorkLine.cancelLineMultiPick</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1504">WHSWorkLine.cancelLineMultiPick</span></span>|
|<span data-ttu-id="0bbb6-1505">WHSWorkLine.cancelLinePartial</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1505">WHSWorkLine.cancelLinePartial</span></span>|
|<span data-ttu-id="0bbb6-1506">WMSArrivalCreateJournal.createWMSJournalTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1506">WMSArrivalCreateJournal.createWMSJournalTrans</span></span>|
|<span data-ttu-id="0bbb6-1507">WMSArrivalCreateJournal.createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1507">WMSArrivalCreateJournal.createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="0bbb6-1508">WMSArrivalOverviewGeneration.buildReturnOrderFromSalesLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1508">WMSArrivalOverviewGeneration.buildReturnOrderFromSalesLine</span></span>|
|<span data-ttu-id="0bbb6-1509">WMSJournalCheckPostReception.checkReference</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1509">WMSJournalCheckPostReception.checkReference</span></span>|
|<span data-ttu-id="0bbb6-1510">WMSJournalTransUpdateSerialId.dialog</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1510">WMSJournalTransUpdateSerialId.dialog</span></span>|
|<span data-ttu-id="0bbb6-1511">WmsPickingList_OrderPickDP::insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1511">WmsPickingList_OrderPickDP::insertIntoTempTable</span></span>|
|<span data-ttu-id="0bbb6-1512">WrkCrtScheduler.writeJobCapacityReservations</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1512">WrkCrtScheduler.writeJobCapacityReservations</span></span>|
|<span data-ttu-id="0bbb6-1513">WrkCtrApplicableResourceQuery.query</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1513">WrkCtrApplicableResourceQuery.query</span></span>|
|<span data-ttu-id="0bbb6-1514">WrkCtrlScheduler_Prod.loadJobsDetail</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1514">WrkCtrlScheduler_Prod.loadJobsDetail</span></span>|
|<span data-ttu-id="0bbb6-1515">WrkCtrlScheduler_Prod.saveOrder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1515">WrkCtrlScheduler_Prod.saveOrder</span></span>|
|<span data-ttu-id="0bbb6-1516">WrkCtrlScheduler_Proj.saveOrder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1516">WrkCtrlScheduler_Proj.saveOrder</span></span>|
|<span data-ttu-id="0bbb6-1517">WrkCtrlScheduler_Proj.writeJobData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1517">WrkCtrlScheduler_Proj.writeJobData</span></span>|
|<span data-ttu-id="0bbb6-1518">WrkCtrReservedSum.find</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1518">WrkCtrReservedSum.find</span></span>|
|<span data-ttu-id="0bbb6-1519">WrkCtrScheduler.computeJobTimes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1519">WrkCtrScheduler.computeJobTimes</span></span>|
|<span data-ttu-id="0bbb6-1520">WrkCtrScheduler.insertWrkCtrCapResUsingInsertList</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1520">WrkCtrScheduler.insertWrkCtrCapResUsingInsertList</span></span>|
|<span data-ttu-id="0bbb6-1521">WrkCtrScheduler.writeJobCapacityReservations</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1521">WrkCtrScheduler.writeJobCapacityReservations</span></span>|
|<span data-ttu-id="0bbb6-1522">WrkCtrScheduler.writeJobData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1522">WrkCtrScheduler.writeJobData</span></span>|

## <a name="sql-operations-made-extensible"></a><span data-ttu-id="0bbb6-1523">拡張可能になった SQL 操作</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1523">SQL operations made extensible</span></span>

<span data-ttu-id="0bbb6-1524">埋め込み SQL ステートメントを使用するアプリケーション コードは拡張機能を通じて変更できません。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1524">Application code with embedded SQL statements cannot be modified through extensions.</span></span> <span data-ttu-id="0bbb6-1525">次の表に示す方法で拡張性を有効にするために、標準のアプリケーションに変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1525">Changes have been made to the standard application to enable extensibility in the methods listed in the folllowing table.</span></span> <span data-ttu-id="0bbb6-1526">これは、一般に、埋め込み SQL ステートメントを、これらのメソッドで SQL ステートメントの構築方法を拡張をサポートするクエリ オブジェクトに変換すると有効になります。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1526">This has commonly been enabled by transforming embedded SQL statements into query objects that support extending how SQL statements are built in these methods.</span></span>

|  <span data-ttu-id="0bbb6-1527">方法</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1527">Method</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-1528">CustCollectionLetterCreate.updateAllExisting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1528">CustCollectionLetterCreate.updateAllExisting</span></span>|
|<span data-ttu-id="0bbb6-1529">CustCollectionLetterCreate.updateExisting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1529">CustCollectionLetterCreate.updateExisting</span></span>|
|<span data-ttu-id="0bbb6-1530">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1530">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="0bbb6-1531">CustProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1531">CustProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="0bbb6-1532">CustSettlementPriorityProcessing.createTempData</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1532">CustSettlementPriorityProcessing.createTempData</span></span>|
|<span data-ttu-id="0bbb6-1533">DirPartyTable.getLocationFromRole</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1533">DirPartyTable.getLocationFromRole</span></span>|
|<span data-ttu-id="0bbb6-1534">InventQualityOrderTable.createInventQualityOrderLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1534">InventQualityOrderTable.createInventQualityOrderLines</span></span>|
|<span data-ttu-id="0bbb6-1535">InventTransIdSum::calcSum</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1535">InventTransIdSum::calcSum</span></span>|
|<span data-ttu-id="0bbb6-1536">InventTransIdSum_InventLocation::calcSum</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1536">InventTransIdSum_InventLocation::calcSum</span></span>|
|<span data-ttu-id="0bbb6-1537">InventTransReference::setRefTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1537">InventTransReference::setRefTrans</span></span>|
|<span data-ttu-id="0bbb6-1538">Markup.insertMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1538">Markup.insertMarkupTrans</span></span>|
|<span data-ttu-id="0bbb6-1539">Markup.mcrCopyForReturn</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1539">Markup.mcrCopyForReturn</span></span>|
|<span data-ttu-id="0bbb6-1540">PriceDisc.findDisc</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1540">PriceDisc.findDisc</span></span>|
|<span data-ttu-id="0bbb6-1541">PriceDisc.findPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1541">PriceDisc.findPriceAgreement</span></span>|
|<span data-ttu-id="0bbb6-1542">PurchFormLetterParmDataInvoice.createLineProject</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1542">PurchFormLetterParmDataInvoice.createLineProject</span></span>|
|<span data-ttu-id="0bbb6-1543">ReqPlanCopy.copyReqTransAndReqTransCov</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1543">ReqPlanCopy.copyReqTransAndReqTransCov</span></span>|
|<span data-ttu-id="0bbb6-1544">ReqPlanCopy.copyReqTransKeep</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1544">ReqPlanCopy.copyReqTransKeep</span></span>|
|<span data-ttu-id="0bbb6-1545">ReqPlanCopy.copyWrkCtrCapRes</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1545">ReqPlanCopy.copyWrkCtrCapRes</span></span>|
|<span data-ttu-id="0bbb6-1546">ReqPlanCopy.copyWrkCtrCapResForReqPO</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1546">ReqPlanCopy.copyWrkCtrCapResForReqPO</span></span>|
|<span data-ttu-id="0bbb6-1547">SalesCopying.deleteLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1547">SalesCopying.deleteLines</span></span>|
|<span data-ttu-id="0bbb6-1548">SalesLineType::deliveredInTotal</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1548">SalesLineType::deliveredInTotal</span></span>|
|<span data-ttu-id="0bbb6-1549">SalesTableType.parmPickingListRegistrationEnumerable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1549">SalesTableType.parmPickingListRegistrationEnumerable</span></span>|
|<span data-ttu-id="0bbb6-1550">SalesTableType_Sales.canPickingListBeUpdated</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1550">SalesTableType_Sales.canPickingListBeUpdated</span></span>|
|<span data-ttu-id="0bbb6-1551">SalesUpdateRemain.canclRemainderOnOpenSalesLines</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1551">SalesUpdateRemain.canclRemainderOnOpenSalesLines</span></span>|
|<span data-ttu-id="0bbb6-1552">SubledgerJournalizer.createSummaryFromJournalAccountEntry</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1552">SubledgerJournalizer.createSummaryFromJournalAccountEntry</span></span>|
|<span data-ttu-id="0bbb6-1553">SubledgerJournalizer.loadAccountingDistributionTmpJournalize</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1553">SubledgerJournalizer.loadAccountingDistributionTmpJournalize</span></span>|
|<span data-ttu-id="0bbb6-1554">SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1554">SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="0bbb6-1555">SubledgerJournalizer.loadStandardSubledgerLedgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1555">SubledgerJournalizer.loadStandardSubledgerLedgerJournalTmpDetail</span></span>|
|<span data-ttu-id="0bbb6-1556">SubledgerJournalizer.loadSubledgerJourTmpDetailWithRelieving</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1556">SubledgerJournalizer.loadSubledgerJourTmpDetailWithRelieving</span></span>|
|<span data-ttu-id="0bbb6-1557">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1557">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span></span>|
|<span data-ttu-id="0bbb6-1558">SubledgerJournalizer.summarizeJourAccountEntryDetailForRound</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1558">SubledgerJournalizer.summarizeJourAccountEntryDetailForRound</span></span>|
|<span data-ttu-id="0bbb6-1559">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1559">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span></span>|
|<span data-ttu-id="0bbb6-1560">TmsProcessXML_Base.writeShipDeliveryAccessorials</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1560">TmsProcessXML_Base.writeShipDeliveryAccessorials</span></span>|
|<span data-ttu-id="0bbb6-1561">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1561">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="0bbb6-1562">VersioningPurchaseOrder.archivePurchLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1562">VersioningPurchaseOrder.archivePurchLine</span></span>|
|<span data-ttu-id="0bbb6-1563">WhsLoadPostEngineBase::createShipments</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1563">WhsLoadPostEngineBase::createShipments</span></span>|
|<span data-ttu-id="0bbb6-1564">WHSPackForm.getShipmentId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1564">WHSPackForm.getShipmentId</span></span>|
|<span data-ttu-id="0bbb6-1565">WHSPostEngineBase.executeWaveSteps</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1565">WHSPostEngineBase.executeWaveSteps</span></span>|
|<span data-ttu-id="0bbb6-1566">WhsPostPackingSlip.preparePackingSlipPosting</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1566">WhsPostPackingSlip.preparePackingSlipPosting</span></span>|
|<span data-ttu-id="0bbb6-1567">WhsWarehouseRelease.createShipments</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1567">WhsWarehouseRelease.createShipments</span></span>|
|<span data-ttu-id="0bbb6-1568">WhsWarehouseRelease::createOrConsolidateShipmentForSalesOrder</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1568">WhsWarehouseRelease::createOrConsolidateShipmentForSalesOrder</span></span>|

## <a name="maps-enabled-for-extensibility"></a><span data-ttu-id="0bbb6-1569">拡張性に対して使用可能なマップ</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1569">Maps enabled for extensibility</span></span>

<span data-ttu-id="0bbb6-1570">拡張機能によるフィールドとメソッドの追加を可能にするマップ実装に対して、新しいパターンが導入されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1570">New patterns have been introduced for maps implementation that will allow you to add field and methods by extensions.</span></span> <span data-ttu-id="0bbb6-1571">これの実行方法の詳細は、インターフェイスとして使用されるマップが含まれるドキュメントとバージョン管理実装のためのドキュメントの両方にあります。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1571">Details on how this is done is available in the documentation both with maps that are used as interfaces and for versioning implementations.</span></span>

<span data-ttu-id="0bbb6-1572">次のテーブルに、拡張性を有効にするために変更が適用されたマップとその関連テーブルを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1572">The following table lists the maps and related tables where changes have been applied for enabling extensibility.</span></span>

| <span data-ttu-id="0bbb6-1573">マップおよびテーブル</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1573">Maps and tables</span></span>|
| -------------------|
|<span data-ttu-id="0bbb6-1574">マップ CustVendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1574">Map CustVendInvoiceTrans</span></span>|
|<span data-ttu-id="0bbb6-1575">マップ SalesPurchLine の拡張機能または継承</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1575">Map SalesPurchLine extensions or inheritance</span></span>|
|<span data-ttu-id="0bbb6-1576">マップ SalesPurchTable</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1576">Map SalesPurchTable</span></span>|
|<span data-ttu-id="0bbb6-1577">マップ VendDocumentLineMap</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1577">Map VendDocumentLineMap</span></span>|
|<span data-ttu-id="0bbb6-1578">テーブル PurchLine マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1578">Table PurchLine mappings</span></span>|
|<span data-ttu-id="0bbb6-1579">テーブル PurchLineHistory マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1579">Table PurchLineHistory mappings</span></span>|

## <a name="inventory-dimensions"></a><span data-ttu-id="0bbb6-1580">在庫分析コード</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1580">Inventory dimensions</span></span>

<span data-ttu-id="0bbb6-1581">このリリースでは、在庫分析コードを追加するための新しいモデルが導入されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1581">This release introduces a new model for adding inventory dimensions.</span></span> <span data-ttu-id="0bbb6-1582">以前のリリースでは、在庫分析コードが含まれているすべての SQL ステートメントの拡張が必要な場合、新しい在庫分析コードのカスタマイズをサポートすることは実用的ではありませんでした。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1582">In previous releases it was not practical to support customization for new inventory dimensions if that required extending every SQL statement that included inventory dimensions.</span></span> <span data-ttu-id="0bbb6-1583">代わりに、特定の指定された用途のない 10 個の在庫分析コードを追加しました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1583">Instead, we have added 10 inventory dimensions without any specific designated usage.</span></span> <span data-ttu-id="0bbb6-1584">パートナー ソリューションは、そのコードを保持している間接モデルを通じてコード化し、パートナー ソリューションでの使用に向けた作成済みの在庫分析コード 1 つ以上を配置する個々の実装プロジェクトのために他のモデルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1584">Partner solutions will code through indirection models that hold their code, and other models are made for individual implementation projects that deploy one or more of the prefabricated inventory dimensions toward use in a partner solution.</span></span> <span data-ttu-id="0bbb6-1585">このモデルで在庫分析コードを実装する方法および新しいモデルについて学ぶのに役立つフレーバーの分析コード アプリをリリースする方法については、ドキュメントを利用できます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1585">Documentation will be available on how to implement with inventory dimensions under this model, and release of a sample app with a Flavor dimension will help you learn about the new model.</span></span> <span data-ttu-id="0bbb6-1586">新しい在庫分析コードは、製品分析コードまたは追跡用分析コードとして自由に配置して使用できます。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1586">The new inventory dimension can be freely deployed and used as either product dimensions or tracking dimensions.</span></span>

<span data-ttu-id="0bbb6-1587">この変更により、アプリケーション全体で、次のリストに示されている内容を含む複数の場所が変更されました。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1587">The changes have led to changing multiple places across the application, including what is shown in the following list.</span></span>

| <span data-ttu-id="0bbb6-1588">計上額</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1588">Change</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-1589">拡張可能な製品分析コード</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1589">Extensible Product Dimensions</span></span>|
|<span data-ttu-id="0bbb6-1590">フォーム WHSInventOnHandReserve.updateInventDimFixedControls</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1590">Form WHSInventOnHandReserve.updateInventDimFixedControls</span></span>|
|<span data-ttu-id="0bbb6-1591">InterCompanyInventDim: スロー付きの条件</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1591">InterCompanyInventDim: Condition with throw</span></span>|
|<span data-ttu-id="0bbb6-1592">InventDimFieldsMap - 追加されたフィールド</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1592">InventDimFieldsMap - Added field</span></span>|
|<span data-ttu-id="0bbb6-1593">在庫分析コード InventUpdateOnhand::checkOnHand</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1593">Inventory dimension InventUpdateOnhand::checkOnHand</span></span>|
|<span data-ttu-id="0bbb6-1594">在庫分析コード - テーブル InventDim.create</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1594">Inventory Dimensions - Table InventDim.create</span></span>|
|<span data-ttu-id="0bbb6-1595">InventTransferUpdShip.populateIssueReceiptDimensions</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1595">InventTransferUpdShip.populateIssueReceiptDimensions</span></span>|
|<span data-ttu-id="0bbb6-1596">マップ InventInventoryDimensionEntityFieldsMapping::resolveInventDim()</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1596">Map InventInventoryDimensionEntityFieldsMapping::resolveInventDim()</span></span>|
|<span data-ttu-id="0bbb6-1597">InventDimFieldsMap::getFieldIdForDimensionOnMappedTable の名前を inventoryDimensionFieldIdOnMappedTable() に変更</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1597">Rename InventDimFieldsMap::getFieldIdForDimensionOnMappedTable to inventoryDimensionFieldIdOnMappedTable()</span></span>|
|<span data-ttu-id="0bbb6-1598">テーブル BOMConsistOfTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1598">Table BOMConsistOfTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1599">テーブル BOMPartOfTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1599">Table BOMPartOfTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1600">テーブル EcoResTrackingDimensionGroup.isDimFieldTrackingDimension</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1600">Table EcoResTrackingDimensionGroup.isDimFieldTrackingDimension</span></span>|
|<span data-ttu-id="0bbb6-1601">テーブル InterCompanyInventDim マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1601">Table InterCompanyInventDim mappings</span></span>|
|<span data-ttu-id="0bbb6-1602">テーブル InventAgeGroupDimTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1602">Table InventAgeGroupDimTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1603">テーブル InventCheckRecieptCostPricePcsTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1603">Table InventCheckRecieptCostPricePcsTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1604">テーブル InventCostTmpTransBreakdown マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1604">Table InventCostTmpTransBreakdown mappings</span></span>|
|<span data-ttu-id="0bbb6-1605">テーブル InventCountStatisticsTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1605">Table InventCountStatisticsTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1606">テーブル InventDim マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1606">Table InventDim mappings</span></span>|
|<span data-ttu-id="0bbb6-1607">テーブル InventOnhandTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1607">Table InventOnhandTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1608">テーブル InventPhysicalPerWarehouseTransTmp_IT マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1608">Table InventPhysicalPerWarehouseTransTmp_IT mappings</span></span>|
|<span data-ttu-id="0bbb6-1609">テーブル InventPriceOverviewTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1609">Table InventPriceOverviewTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1610">テーブル InventSumCriticalTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1610">Table InventSumCriticalTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1611">テーブル InventSumDateTransReport マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1611">Table InventSumDateTransReport mappings</span></span>|
|<span data-ttu-id="0bbb6-1612">テーブル InventSumDeltaDim マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1612">Table InventSumDeltaDim mappings</span></span>|
|<span data-ttu-id="0bbb6-1613">テーブル InventTable マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1613">Table InventTable mappings</span></span>|
|<span data-ttu-id="0bbb6-1614">テーブル InventTransferOrderOverviewTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1614">Table InventTransferOrderOverviewTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1615">テーブル InventValueReportTmpLine マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1615">Table InventValueReportTmpLine mappings</span></span>|
|<span data-ttu-id="0bbb6-1616">テーブル ProdPickList マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1616">Table ProdPickList mappings</span></span>|
|<span data-ttu-id="0bbb6-1617">テーブル SalesInvoiceTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1617">Table SalesInvoiceTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1618">テーブル WHSPurchLine.registerPurchaseLine</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1618">Table WHSPurchLine.registerPurchaseLine</span></span>|
|<span data-ttu-id="0bbb6-1619">テーブル WHSTmpCompleteWorkLine.lookupBatch</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1619">Table WHSTmpCompleteWorkLine.lookupBatch</span></span>|
|<span data-ttu-id="0bbb6-1620">テーブル WHSTmpCompleteWorkLine.lookupTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1620">Table WHSTmpCompleteWorkLine.lookupTargetLicensePlateId</span></span>|
|<span data-ttu-id="0bbb6-1621">テーブル WMSCheckABCZonesTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1621">Table WMSCheckABCZonesTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1622">テーブル WMSPickingList_OrderPickTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1622">Table WMSPickingList_OrderPickTmp mappings</span></span>|
|<span data-ttu-id="0bbb6-1623">テーブル WMSPickingListReportTmp マッピング</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1623">Table WMSPickingListReportTmp mappings</span></span>|

## <a name="metadata-changes-to-enable-extensibility"></a><span data-ttu-id="0bbb6-1624">拡張機能を有効にするメタデータの変更</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1624">Metadata changes to enable extensibility</span></span>

<span data-ttu-id="0bbb6-1625">次のテーブルに、これらのオブジェクトの特定のメタデータの拡張機能を有効にするために加えられた変更を示します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1625">The following table lists changes made for enabling extensibility for specific metadata on these objects.</span></span> <span data-ttu-id="0bbb6-1626">これらの変更はインスタンスごとに異なります。変更を確認するには、特定の実装を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1626">These changes vary from instance to instance, you can consult the specific implementation to review the changes.</span></span>

| <span data-ttu-id="0bbb6-1627">計上額</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1627">Change</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-1628">CountryRegionCodes プロパティ</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1628">CountryRegionCodes property</span></span>|
|<span data-ttu-id="0bbb6-1629">CustCustomerEntity</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1629">CustCustomerEntity</span></span>|
|<span data-ttu-id="0bbb6-1630">EcoResProductCategoryAssignmentEntity が公開</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1630">EcoResProductCategoryAssignmentEntity made public</span></span>|
|<span data-ttu-id="0bbb6-1631">フォーム AssetSplit : FormControls</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1631">Form AssetSplit : FormControls</span></span>|
|<span data-ttu-id="0bbb6-1632">フォーム CustCollections.Cases</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1632">Form CustCollections.Cases</span></span>|
|<span data-ttu-id="0bbb6-1633">フォーム CustGroup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1633">Form CustGroup</span></span>|
|<span data-ttu-id="0bbb6-1634">フォーム LedgerJournalTransCustPaym - メニュー項目ボタン自動申告</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1634">Form LedgerJournalTransCustPaym - menu item button auto declaration</span></span>|
|<span data-ttu-id="0bbb6-1635">フォーム LedgerJournalTransVendPaym - メニュー項目ボタン自動申告</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1635">Form LedgerJournalTransVendPaym - menu item button auto declaration</span></span>|
|<span data-ttu-id="0bbb6-1636">テーブル DimensionAttributeValueSetItem</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1636">Table DimensionAttributeValueSetItem</span></span>|
|<span data-ttu-id="0bbb6-1637">他のステージング テーブルと同様、ReplacementKey がないテーブル EcoResReleasedProductCreationStaging。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1637">Table EcoResReleasedProductCreationStaging missing ReplacementKey like other staging tables.</span></span>|
|<span data-ttu-id="0bbb6-1638">テーブル SubledgerJournalAccountEntry(Tmp...)</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1638">Tables SubledgerJournalAccountEntry(Tmp...)</span></span>|
|<span data-ttu-id="0bbb6-1639">SubLedgerJournalAccountEntryView の表示</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1639">View SubLedgerJournalAccountEntryView</span></span>|

## <a name="other-changes"></a><span data-ttu-id="0bbb6-1640">その他の変更</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1640">Other changes</span></span>

<span data-ttu-id="0bbb6-1641">次のテーブルに、拡張機能に対して行われた追加の変更を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1641">The following table lists additional changes that have been made for extensibility.</span></span>

| <span data-ttu-id="0bbb6-1642">計上額</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1642">Change</span></span> |
| -------------|
|<span data-ttu-id="0bbb6-1643">CustCollectionLetterCreate</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1643">CustCollectionLetterCreate</span></span>|
|<span data-ttu-id="0bbb6-1644">CustCollectionLetterPost</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1644">CustCollectionLetterPost</span></span>|
|<span data-ttu-id="0bbb6-1645">通貨の小数点以下桁数に対する拡張性アプローチ</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1645">Extensibility approach for number of decimal places for currency</span></span>|
|<span data-ttu-id="0bbb6-1646">拡張可能な EDT 小数点以下桁数: AssetDepreciationAmountUnit</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1646">Extensible edt decimal places:  AssetDepreciationAmountUnit</span></span>|
|<span data-ttu-id="0bbb6-1647">フォーム拡張機能 - DirPartyTable - registerOverrideMethod jumpRef</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1647">Form Extension - DirPartyTable - registerOverrideMethod jumpRef</span></span>|
|<span data-ttu-id="0bbb6-1648">フォーム ProjCategoryLookup</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1648">Form ProjCategoryLookup</span></span>|
|<span data-ttu-id="0bbb6-1649">メソッド シグネチャが変更されました: InventPostingSetupCache</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1649">Method signature changed: InventPostingSetupCache</span></span>|
|<span data-ttu-id="0bbb6-1650">メソッド シグネチャが変更されました: テーブル ProjCostPriceExpense.find</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1650">Method signature changed: Table ProjCostPriceExpense.find</span></span>|
|<span data-ttu-id="0bbb6-1651">メソッド シグネチャが変更されました: テーブル ProjCostPriceExpense.findCostPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1651">Method signature changed: Table ProjCostPriceExpense.findCostPrice</span></span>|
|<span data-ttu-id="0bbb6-1652">メソッド シグネチャが変更されました: テーブル ProjCostSalesPrice.find</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1652">Method signature changed: Table ProjCostSalesPrice.find</span></span>|
|<span data-ttu-id="0bbb6-1653">メソッド シグネチャが変更されました: テーブル ProjCostSalesPrice.findCostSalesPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1653">Method signature changed: Table ProjCostSalesPrice.findCostSalesPrice</span></span>|
|<span data-ttu-id="0bbb6-1654">メソッド シグネチャが変更されました: テーブル ProjHourCostPrice.Find</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1654">Method signature changed: Table ProjHourCostPrice.Find</span></span>|
|<span data-ttu-id="0bbb6-1655">メソッド シグネチャが変更されました: テーブル ProjHourCostPrice.FindCostPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1655">Method signature changed: Table ProjHourCostPrice.FindCostPrice</span></span>|
|<span data-ttu-id="0bbb6-1656">メソッド シグネチャが変更されました: テーブル ProjHourSalesPrice.find</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1656">Method signature changed: Table ProjHourSalesPrice.find</span></span>|
|<span data-ttu-id="0bbb6-1657">メソッド シグネチャが変更されました: テーブル ProjHourSalesPrice.findHourSalesPrice</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1657">Method signature changed: Table ProjHourSalesPrice.findHourSalesPrice</span></span>|
|<span data-ttu-id="0bbb6-1658">ApplicationCommon に追加される新しい数量 EDT</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1658">New Quantity EDT added to ApplicationCommon</span></span>|
|<span data-ttu-id="0bbb6-1659">その他: 価格と割引のフレームワークの新しい基本列挙型</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1659">Other: New base enum for Price & Discount framework</span></span>|
|<span data-ttu-id="0bbb6-1660">Alternative Key = Yes に設定し、参照グループ ルックアップを有効にする</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1660">Set Alternative Key = Yes to enable reference group lookups</span></span>|
|<span data-ttu-id="0bbb6-1661">EcoResIProductCrossTableData インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1661">Use of interface EcoResIProductCrossTableData</span></span>|

## <a name="bugs"></a><span data-ttu-id="0bbb6-1662">バグ</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1662">Bugs</span></span>

<span data-ttu-id="0bbb6-1663">次のテーブルは、拡張機能のために要求されたが、バグとして認識され、標準アプリケーションで修正された変更を一覧表示したものです。</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1663">The following table lists changes that were requested for extensibility but were acknowledged as bugs and fixed in the standard application.</span></span>


|                                   <span data-ttu-id="0bbb6-1664">計上額</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1664">Change</span></span>                                   |
|----------------------------------------------------------------------------|
|             <span data-ttu-id="0bbb6-1665">class CaseUpdateStatus_Close, method changeStatus</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1665">class CaseUpdateStatus_Close, method changeStatus</span></span>              |
|               <span data-ttu-id="0bbb6-1666">CustCollectionLetterJour での誤った関係</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1666">Incorrect relation on CustCollectionLetterJour</span></span>               |
|            <span data-ttu-id="0bbb6-1667">その他: CompanyHelper.testCreateParameter のバグ修正</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1667">Other: Bug fix on CompanyHelper.testCreateParameter</span></span>             |
| <span data-ttu-id="0bbb6-1668">テーブル CustCollectionLetterJour - クラス cancelCollectionLetterCodeCustTrans</span><span class="sxs-lookup"><span data-stu-id="0bbb6-1668">Table CustCollectionLetterJour - class cancelCollectionLetterCodeCustTrans</span></span> |

