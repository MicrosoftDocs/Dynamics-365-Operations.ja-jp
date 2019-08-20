---
title: Dynamics 365 for Finance and Operations バージョン 8.1.3 の拡張機能の変更
description: これは、Dynamics 365 for Finance and Operations バージョン 8.1.3 に実装された拡張機能の一覧です。
author: FrankDahl
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-12-07
ms.dyn365.ops.version: App 8.1.3
ms.openlocfilehash: 3de652350ef2a010c57de32c792c986e18e74fc7
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833446"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-813"></a><span data-ttu-id="fa00f-103">Dynamics 365 for Finance and Operations バージョン 8.1.3 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="fa00f-103">Extensibility changes in Dynamics 365 for Finance and Operations version 8.1.3</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fa00f-104">これは、Dynamics 365 for Finance and Operations バージョン 8.1.3 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="fa00f-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="fa00f-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa00f-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="enumerations-made-extensible"></a><span data-ttu-id="fa00f-106">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="fa00f-106">Enumerations made extensible</span></span>

<span data-ttu-id="fa00f-107">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="fa00f-107">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="fa00f-108">列挙型</span><span class="sxs-lookup"><span data-stu-id="fa00f-108">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="fa00f-109">AttributeDataType</span><span class="sxs-lookup"><span data-stu-id="fa00f-109">AttributeDataType</span></span>|
|<span data-ttu-id="fa00f-110">BankDocumentBookType</span><span class="sxs-lookup"><span data-stu-id="fa00f-110">BankDocumentBookType</span></span>|
|<span data-ttu-id="fa00f-111">BudgetPlanHCMReportGroupOption</span><span class="sxs-lookup"><span data-stu-id="fa00f-111">BudgetPlanHCMReportGroupOption</span></span>|
|<span data-ttu-id="fa00f-112">CommitmentType</span><span class="sxs-lookup"><span data-stu-id="fa00f-112">CommitmentType</span></span>|
|<span data-ttu-id="fa00f-113">CommitmentType</span><span class="sxs-lookup"><span data-stu-id="fa00f-113">CommitmentType</span></span>|
|<span data-ttu-id="fa00f-114">CustVendNegInstStatus</span><span class="sxs-lookup"><span data-stu-id="fa00f-114">CustVendNegInstStatus</span></span>|
|<span data-ttu-id="fa00f-115">CzAdvanceInvoiceStatus</span><span class="sxs-lookup"><span data-stu-id="fa00f-115">CzAdvanceInvoiceStatus</span></span>|
|<span data-ttu-id="fa00f-116">DateTransactionDuedate</span><span class="sxs-lookup"><span data-stu-id="fa00f-116">DateTransactionDuedate</span></span>|
|<span data-ttu-id="fa00f-117">LedgerAllocationMethod</span><span class="sxs-lookup"><span data-stu-id="fa00f-117">LedgerAllocationMethod</span></span>|
|<span data-ttu-id="fa00f-118">LedgerCovDocumentType</span><span class="sxs-lookup"><span data-stu-id="fa00f-118">LedgerCovDocumentType</span></span>|
|<span data-ttu-id="fa00f-119">MCRFraudType</span><span class="sxs-lookup"><span data-stu-id="fa00f-119">MCRFraudType</span></span>|
|<span data-ttu-id="fa00f-120">PercentHours</span><span class="sxs-lookup"><span data-stu-id="fa00f-120">PercentHours</span></span>|
|<span data-ttu-id="fa00f-121">PerDayWeekMthQtYr</span><span class="sxs-lookup"><span data-stu-id="fa00f-121">PerDayWeekMthQtYr</span></span>|
|<span data-ttu-id="fa00f-122">PrepaymentHandlingLayout_W</span><span class="sxs-lookup"><span data-stu-id="fa00f-122">PrepaymentHandlingLayout_W</span></span>|
|<span data-ttu-id="fa00f-123">ProdStatusAll</span><span class="sxs-lookup"><span data-stu-id="fa00f-123">ProdStatusAll</span></span>|
|<span data-ttu-id="fa00f-124">TaxDirection</span><span class="sxs-lookup"><span data-stu-id="fa00f-124">TaxDirection</span></span>|
|<span data-ttu-id="fa00f-125">TaxType_IT</span><span class="sxs-lookup"><span data-stu-id="fa00f-125">TaxType_IT</span></span>|
|<span data-ttu-id="fa00f-126">WHSWaveTemplateType</span><span class="sxs-lookup"><span data-stu-id="fa00f-126">WHSWaveTemplateType</span></span>|

## <a name="sql-operations-made-extensible"></a><span data-ttu-id="fa00f-127">拡張可能になった SQL 操作</span><span class="sxs-lookup"><span data-stu-id="fa00f-127">SQL operations made extensible</span></span>

<span data-ttu-id="fa00f-128">これらの SQL 操作は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="fa00f-128">These SQL operations have been made extensible in this update.</span></span>

| <span data-ttu-id="fa00f-129">操作</span><span class="sxs-lookup"><span data-stu-id="fa00f-129">Operation</span></span>|
| --------------- |
|<span data-ttu-id="fa00f-130">InventTrans.deleteReturnTransOrigin</span><span class="sxs-lookup"><span data-stu-id="fa00f-130">InventTrans.deleteReturnTransOrigin</span></span>|
|<span data-ttu-id="fa00f-131">InventUpd_ChangeDimension.updateForceInventTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-131">InventUpd_ChangeDimension.updateForceInventTrans</span></span>|
|<span data-ttu-id="fa00f-132">PriceDiscAdmCheckPost.updatePriceDiscTableRecords</span><span class="sxs-lookup"><span data-stu-id="fa00f-132">PriceDiscAdmCheckPost.updatePriceDiscTableRecords</span></span>|
|<span data-ttu-id="fa00f-133">ProdJournalCleanUp.deleteJournals</span><span class="sxs-lookup"><span data-stu-id="fa00f-133">ProdJournalCleanUp.deleteJournals</span></span>|
|<span data-ttu-id="fa00f-134">ProjBudgetManager.createBudgetCostForecast</span><span class="sxs-lookup"><span data-stu-id="fa00f-134">ProjBudgetManager.createBudgetCostForecast</span></span>|
|<span data-ttu-id="fa00f-135">ProjBudgetManager.createBudgetEmplForecast</span><span class="sxs-lookup"><span data-stu-id="fa00f-135">ProjBudgetManager.createBudgetEmplForecast</span></span>|
|<span data-ttu-id="fa00f-136">ProjBudgetManager.createBudgetRevenueForecast</span><span class="sxs-lookup"><span data-stu-id="fa00f-136">ProjBudgetManager.createBudgetRevenueForecast</span></span>|
|<span data-ttu-id="fa00f-137">ProjBudgetManager.createBudgetSalesForecast</span><span class="sxs-lookup"><span data-stu-id="fa00f-137">ProjBudgetManager.createBudgetSalesForecast</span></span>|
|<span data-ttu-id="fa00f-138">SubledgerJourFinalNetAmtEntryProvider.getFinalRelievingEntriesWithNetAmounts</span><span class="sxs-lookup"><span data-stu-id="fa00f-138">SubledgerJourFinalNetAmtEntryProvider.getFinalRelievingEntriesWithNetAmounts</span></span>|
|<span data-ttu-id="fa00f-139">SubledgerJourFinalRelieveEntryProvider.populateEntriesBySide</span><span class="sxs-lookup"><span data-stu-id="fa00f-139">SubledgerJourFinalRelieveEntryProvider.populateEntriesBySide</span></span>|
|<span data-ttu-id="fa00f-140">SubledgerJournalAccountEntryRelievingTmp.mergeJournalizationEntries</span><span class="sxs-lookup"><span data-stu-id="fa00f-140">SubledgerJournalAccountEntryRelievingTmp.mergeJournalizationEntries</span></span>|
|<span data-ttu-id="fa00f-141">SubledgerJournalFinalReliever.findEntriesAlreadyRelieved</span><span class="sxs-lookup"><span data-stu-id="fa00f-141">SubledgerJournalFinalReliever.findEntriesAlreadyRelieved</span></span>|
|<span data-ttu-id="fa00f-142">SubledgerJournalFinalReliever.findEntriesToRelieve</span><span class="sxs-lookup"><span data-stu-id="fa00f-142">SubledgerJournalFinalReliever.findEntriesToRelieve</span></span>|
|<span data-ttu-id="fa00f-143">SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-143">SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-144">SubledgerJournalizer.loadInterCompanyNonOffsetSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-144">SubledgerJournalizer.loadInterCompanyNonOffsetSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-145">SubledgerJournalizer.loadInterCompanyOffsetSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-145">SubledgerJournalizer.loadInterCompanyOffsetSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-146">SubledgerJournalizer.loadRelievingSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-146">SubledgerJournalizer.loadRelievingSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-147">SubledgerJournalizer.loadReversingSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-147">SubledgerJournalizer.loadReversingSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-148">SubledgerJournalizer.loadYearEndSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-148">SubledgerJournalizer.loadYearEndSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-149">SubledgerJournalizer.summarizeJourAccountEntryDetailForRound</span><span class="sxs-lookup"><span data-stu-id="fa00f-149">SubledgerJournalizer.summarizeJourAccountEntryDetailForRound</span></span>|

## <a name="metadata-changes"></a><span data-ttu-id="fa00f-150">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="fa00f-150">Metadata changes</span></span>

<span data-ttu-id="fa00f-151">これらのメタデータの変更は、このアップデートで行われました。</span><span class="sxs-lookup"><span data-stu-id="fa00f-151">These metadata changes have been made in this update.</span></span>

| <span data-ttu-id="fa00f-152">操作</span><span class="sxs-lookup"><span data-stu-id="fa00f-152">Operation</span></span> |
| --------------- |
|<span data-ttu-id="fa00f-153">Classes/CustVendSettle/classDeclaration.field モディファイアー</span><span class="sxs-lookup"><span data-stu-id="fa00f-153">Classes/CustVendSettle/classDeclaration.field modifier</span></span>|
|<span data-ttu-id="fa00f-154">Classes/LedgerPostingGeneralJournalController/transferLines.HookableAttribute</span><span class="sxs-lookup"><span data-stu-id="fa00f-154">Classes/LedgerPostingGeneralJournalController/transferLines.HookableAttribute</span></span>|
|<span data-ttu-id="fa00f-155">Classes/VendPaymentJournalDP.none</span><span class="sxs-lookup"><span data-stu-id="fa00f-155">Classes/VendPaymentJournalDP.none</span></span>|
|<span data-ttu-id="fa00f-156">EcoResProductAttributeTranslationEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="fa00f-156">EcoResProductAttributeTranslationEntity.IsPublic</span></span>|
|<span data-ttu-id="fa00f-157">EcoResProductBarcodeEntity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="fa00f-157">EcoResProductBarcodeEntity.Property.IsPublic</span></span>|
|<span data-ttu-id="fa00f-158">Enum/RDeferralsCalculatePeriod.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-158">Enum/RDeferralsCalculatePeriod.Country region code</span></span>|
|<span data-ttu-id="fa00f-159">Enum/RDeferralsInitRetirementDate.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-159">Enum/RDeferralsInitRetirementDate.Country region codes</span></span>|
|<span data-ttu-id="fa00f-160">Enum/RDeferralsInitWriteStartDate.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-160">Enum/RDeferralsInitWriteStartDate.Country region codes</span></span>|
|<span data-ttu-id="fa00f-161">Enum/RDeferralsInitWriteStartDate/EnumValue</span><span class="sxs-lookup"><span data-stu-id="fa00f-161">Enum/RDeferralsInitWriteStartDate/EnumValue</span></span>|
|<span data-ttu-id="fa00f-162">Enum/RDeferralsInterval.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-162">Enum/RDeferralsInterval.Country region code</span></span>|
|<span data-ttu-id="fa00f-163">Enum/RDeferralsManualCalcType.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-163">Enum/RDeferralsManualCalcType.Country region codes</span></span>|
|<span data-ttu-id="fa00f-164">Enum/RDeferralsMethod.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-164">Enum/RDeferralsMethod.Country Region Codes</span></span>|
|<span data-ttu-id="fa00f-165">Enum/RDeferralsPostValue.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-165">Enum/RDeferralsPostValue.Country region codes</span></span>|
|<span data-ttu-id="fa00f-166">Enum/RDeferralsStatus.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-166">Enum/RDeferralsStatus.Country Region Code</span></span>|
|<span data-ttu-id="fa00f-167">Enum/RDeferralsTableGroupAllBook.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-167">Enum/RDeferralsTableGroupAllBook.Country Region Codes</span></span>|
|<span data-ttu-id="fa00f-168">Enum/RDeferralsTransType.Country 地域コード</span><span class="sxs-lookup"><span data-stu-id="fa00f-168">Enum/RDeferralsTransType.Country Region Codes</span></span>|
|<span data-ttu-id="fa00f-169">Extended Data Types/AttributeValueFloat.No Of Decimals は拡張可能です</span><span class="sxs-lookup"><span data-stu-id="fa00f-169">Extended Data Types/AttributeValueFloat.No Of Decimals is Extensible</span></span>|
|<span data-ttu-id="fa00f-170">OnAccount および経費の明細行タイプのプロジェクトの請求書/提案明細行の説明を増加します。</span><span class="sxs-lookup"><span data-stu-id="fa00f-170">Increase Description in Project invoices/proposal lines for OnAccount and Expense line type</span></span>|
|<span data-ttu-id="fa00f-171">InventValue レポートは、カスタムの分析コードをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="fa00f-171">InventValue report now supports custom dimensions</span></span>|
|<span data-ttu-id="fa00f-172">Maps/AccountSumMap.Balance08,Balance08Cur,Balance09,Balance09Cur</span><span class="sxs-lookup"><span data-stu-id="fa00f-172">Maps/AccountSumMap.Balance08,Balance08Cur,Balance09,Balance09Cur</span></span>|
|<span data-ttu-id="fa00f-173">Table/PurchTable.Visible = True</span><span class="sxs-lookup"><span data-stu-id="fa00f-173">Table/PurchTable.Visible = True</span></span>|
|<span data-ttu-id="fa00f-174">Table/VendUnrealizedRev/Field/ReversalDate.Allow edit.AllowEdit</span><span class="sxs-lookup"><span data-stu-id="fa00f-174">Table/VendUnrealizedRev/Field/ReversalDate.Allow edit.AllowEdit</span></span>|
|<span data-ttu-id="fa00f-175">Tables/DirPartyTable/Fields.AOS 承認</span><span class="sxs-lookup"><span data-stu-id="fa00f-175">Tables/DirPartyTable/Fields.AOS Authorization</span></span>|
|<span data-ttu-id="fa00f-176">Tables/VendSettlement/Relations/VendTrans.RelationshipType</span><span class="sxs-lookup"><span data-stu-id="fa00f-176">Tables/VendSettlement/Relations/VendTrans.RelationshipType</span></span>|
|<span data-ttu-id="fa00f-177">Tables/WHSDocumentRoutingLine/Indexes/DocumentRoutingTablePrinterNameIdx</span><span class="sxs-lookup"><span data-stu-id="fa00f-177">Tables/WHSDocumentRoutingLine/Indexes/DocumentRoutingTablePrinterNameIdx</span></span>|

## <a name="refactored-methods"></a><span data-ttu-id="fa00f-178">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="fa00f-178">Refactored methods</span></span>

<span data-ttu-id="fa00f-179">これらのメソッドは、拡張性をサポートするためにリファクターされています。</span><span class="sxs-lookup"><span data-stu-id="fa00f-179">These methods have been refactored to support extensibility.</span></span>

| <span data-ttu-id="fa00f-180">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="fa00f-180">Refactored methods</span></span>                                                                             |
|------------------------------------------------------------------------------------------------|
|<span data-ttu-id="fa00f-181">AssetJournal.populateLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-181">AssetJournal.populateLedgerJournalTrans</span></span>|
|<span data-ttu-id="fa00f-182">AssetPost.postToGeneralLedger</span><span class="sxs-lookup"><span data-stu-id="fa00f-182">AssetPost.postToGeneralLedger</span></span>|
|<span data-ttu-id="fa00f-183">AssetProposalDepreciation.run</span><span class="sxs-lookup"><span data-stu-id="fa00f-183">AssetProposalDepreciation.run</span></span>|
|<span data-ttu-id="fa00f-184">AssetTransfer.addLedgerVoucherTransObjects</span><span class="sxs-lookup"><span data-stu-id="fa00f-184">AssetTransfer.addLedgerVoucherTransObjects</span></span>|
|<span data-ttu-id="fa00f-185">AxSalesLine.setDefaultDimension</span><span class="sxs-lookup"><span data-stu-id="fa00f-185">AxSalesLine.setDefaultDimension</span></span>|
|<span data-ttu-id="fa00f-186">BankChequeCopy.fillTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="fa00f-186">BankChequeCopy.fillTmpChequePrintout</span></span>|
|<span data-ttu-id="fa00f-187">BankChequeLayout.updateDesign</span><span class="sxs-lookup"><span data-stu-id="fa00f-187">BankChequeLayout.updateDesign</span></span>|
|<span data-ttu-id="fa00f-188">BankDepositSlip.modifyBankAccountTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-188">BankDepositSlip.modifyBankAccountTrans</span></span>|
|<span data-ttu-id="fa00f-189">BankJournalHeaderEntity.ValidateField</span><span class="sxs-lookup"><span data-stu-id="fa00f-189">BankJournalHeaderEntity.ValidateField</span></span>|
|<span data-ttu-id="fa00f-190">BankPositivePayExport.sendFileToUser</span><span class="sxs-lookup"><span data-stu-id="fa00f-190">BankPositivePayExport.sendFileToUser</span></span>|
|<span data-ttu-id="fa00f-191">BankStatementValidate.validateDate</span><span class="sxs-lookup"><span data-stu-id="fa00f-191">BankStatementValidate.validateDate</span></span>|
|<span data-ttu-id="fa00f-192">BankStmtISOAccountStatement.deleteStatement</span><span class="sxs-lookup"><span data-stu-id="fa00f-192">BankStmtISOAccountStatement.deleteStatement</span></span>|
|<span data-ttu-id="fa00f-193">BOM.defaultField</span><span class="sxs-lookup"><span data-stu-id="fa00f-193">BOM.defaultField</span></span>|
|<span data-ttu-id="fa00f-194">BOM.validateField</span><span class="sxs-lookup"><span data-stu-id="fa00f-194">BOM.validateField</span></span>|
|<span data-ttu-id="fa00f-195">BOM.validateWrite</span><span class="sxs-lookup"><span data-stu-id="fa00f-195">BOM.validateWrite</span></span>|
|<span data-ttu-id="fa00f-196">BomCalcItem.insertBOMCalcTable</span><span class="sxs-lookup"><span data-stu-id="fa00f-196">BomCalcItem.insertBOMCalcTable</span></span>|
|<span data-ttu-id="fa00f-197">BomCalcItem.insertBOMCalcTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-197">BomCalcItem.insertBOMCalcTrans</span></span>|
|<span data-ttu-id="fa00f-198">BomCalcProd.calcCostSheet</span><span class="sxs-lookup"><span data-stu-id="fa00f-198">BomCalcProd.calcCostSheet</span></span>|
|<span data-ttu-id="fa00f-199">BOMReportFinishMax.retrieveInventTable</span><span class="sxs-lookup"><span data-stu-id="fa00f-199">BOMReportFinishMax.retrieveInventTable</span></span>|
|<span data-ttu-id="fa00f-200">BudgetCaculateBalance.getActualLedgerAmountsQuery</span><span class="sxs-lookup"><span data-stu-id="fa00f-200">BudgetCaculateBalance.getActualLedgerAmountsQuery</span></span>|
|<span data-ttu-id="fa00f-201">BudgetCaculateBalance.getOriginalBudgetQuery</span><span class="sxs-lookup"><span data-stu-id="fa00f-201">BudgetCaculateBalance.getOriginalBudgetQuery</span></span>|
|<span data-ttu-id="fa00f-202">BudgetCaculateBalance.getRevisedBudgetQuery</span><span class="sxs-lookup"><span data-stu-id="fa00f-202">BudgetCaculateBalance.getRevisedBudgetQuery</span></span>|
|<span data-ttu-id="fa00f-203">BudgetSourceCollectionIntegrator.newBudgetSourceCollectionIntegrator</span><span class="sxs-lookup"><span data-stu-id="fa00f-203">BudgetSourceCollectionIntegrator.newBudgetSourceCollectionIntegrator</span></span>|
|<span data-ttu-id="fa00f-204">BudgetSourceIntegrator.newBudgetSourceIntegrator</span><span class="sxs-lookup"><span data-stu-id="fa00f-204">BudgetSourceIntegrator.newBudgetSourceIntegrator</span></span>|
|<span data-ttu-id="fa00f-205">ChequeController.ClassDeclaration</span><span class="sxs-lookup"><span data-stu-id="fa00f-205">ChequeController.ClassDeclaration</span></span>|
|<span data-ttu-id="fa00f-206">ChequeController.init</span><span class="sxs-lookup"><span data-stu-id="fa00f-206">ChequeController.init</span></span>|
|<span data-ttu-id="fa00f-207">ContactPersonApplicationSuiteEventHandlers.initializedFromCommonEventHandler</span><span class="sxs-lookup"><span data-stu-id="fa00f-207">ContactPersonApplicationSuiteEventHandlers.initializedFromCommonEventHandler</span></span>|
|<span data-ttu-id="fa00f-208">CustBillOfExchangePostRemit.postSettlingStep</span><span class="sxs-lookup"><span data-stu-id="fa00f-208">CustBillOfExchangePostRemit.postSettlingStep</span></span>|
|<span data-ttu-id="fa00f-209">CustDirectDebitMandate.checkBankIBAN</span><span class="sxs-lookup"><span data-stu-id="fa00f-209">CustDirectDebitMandate.checkBankIBAN</span></span>|
|<span data-ttu-id="fa00f-210">CustDueReportDetailDP.updateCustDueReportDetailTmp</span><span class="sxs-lookup"><span data-stu-id="fa00f-210">CustDueReportDetailDP.updateCustDueReportDetailTmp</span></span>|
|<span data-ttu-id="fa00f-211">CustPostInvoiceJob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="fa00f-211">CustPostInvoiceJob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="fa00f-212">CustSettleJournalizingEntries.createGeneratedEntries</span><span class="sxs-lookup"><span data-stu-id="fa00f-212">CustSettleJournalizingEntries.createGeneratedEntries</span></span>|
|<span data-ttu-id="fa00f-213">CustSettleJournalizingEntries.getInterestOriginatingEntries</span><span class="sxs-lookup"><span data-stu-id="fa00f-213">CustSettleJournalizingEntries.getInterestOriginatingEntries</span></span>|
|<span data-ttu-id="fa00f-214">CustSettleJournalizingEntries.getOriginatingEntries</span><span class="sxs-lookup"><span data-stu-id="fa00f-214">CustSettleJournalizingEntries.getOriginatingEntries</span></span>|
|<span data-ttu-id="fa00f-215">CustTransDetails.new</span><span class="sxs-lookup"><span data-stu-id="fa00f-215">CustTransDetails.new</span></span>|
|<span data-ttu-id="fa00f-216">CustTransListDP.insertCustTransListTmp</span><span class="sxs-lookup"><span data-stu-id="fa00f-216">CustTransListDP.insertCustTransListTmp</span></span>|
|<span data-ttu-id="fa00f-217">CustTransOpenCashFlow.generateCashFlow</span><span class="sxs-lookup"><span data-stu-id="fa00f-217">CustTransOpenCashFlow.generateCashFlow</span></span>|
|<span data-ttu-id="fa00f-218">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="fa00f-218">CustVendCheque.output</span></span>|
|<span data-ttu-id="fa00f-219">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="fa00f-219">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span></span>|
|<span data-ttu-id="fa00f-220">CustVendEditTaxBranchHelper_TH.init</span><span class="sxs-lookup"><span data-stu-id="fa00f-220">CustVendEditTaxBranchHelper_TH.init</span></span>|
|<span data-ttu-id="fa00f-221">CustVendExchAdjTrans.initLedgerVoucher</span><span class="sxs-lookup"><span data-stu-id="fa00f-221">CustVendExchAdjTrans.initLedgerVoucher</span></span>|
|<span data-ttu-id="fa00f-222">CustVendSettle.reverseTax</span><span class="sxs-lookup"><span data-stu-id="fa00f-222">CustVendSettle.reverseTax</span></span>|
|<span data-ttu-id="fa00f-223">CustVendTransReorg.paymentSchedSplit</span><span class="sxs-lookup"><span data-stu-id="fa00f-223">CustVendTransReorg.paymentSchedSplit</span></span>|
|<span data-ttu-id="fa00f-224">CustVendTransReorg.post</span><span class="sxs-lookup"><span data-stu-id="fa00f-224">CustVendTransReorg.post</span></span>|
|<span data-ttu-id="fa00f-225">CustVendTransReorg.reorganize</span><span class="sxs-lookup"><span data-stu-id="fa00f-225">CustVendTransReorg.reorganize</span></span>|
|<span data-ttu-id="fa00f-226">CustVendVoucher.setTransactionTxt</span><span class="sxs-lookup"><span data-stu-id="fa00f-226">CustVendVoucher.setTransactionTxt</span></span>|
|<span data-ttu-id="fa00f-227">CustWriteOff.createTaxJournalLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-227">CustWriteOff.createTaxJournalLines</span></span>|
|<span data-ttu-id="fa00f-228">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span><span class="sxs-lookup"><span data-stu-id="fa00f-228">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span></span>|
|<span data-ttu-id="fa00f-229">DirPartyRoleIsExternallyMaintained.setFieldRestrictions</span><span class="sxs-lookup"><span data-stu-id="fa00f-229">DirPartyRoleIsExternallyMaintained.setFieldRestrictions</span></span>|
|<span data-ttu-id="fa00f-230">EcoResDocumentAttachmentEntity.insertDatasourceDocuRef</span><span class="sxs-lookup"><span data-stu-id="fa00f-230">EcoResDocumentAttachmentEntity.insertDatasourceDocuRef</span></span>|
|<span data-ttu-id="fa00f-231">EcoResProductNumberBuilderVariant.getEnumeratorForEnabledOrderedProductDimensions</span><span class="sxs-lookup"><span data-stu-id="fa00f-231">EcoResProductNumberBuilderVariant.getEnumeratorForEnabledOrderedProductDimensions</span></span>|
|<span data-ttu-id="fa00f-232">EFDocMsgFormat_XmlSubmit_BR.createXmlDocumentFromEFDocument</span><span class="sxs-lookup"><span data-stu-id="fa00f-232">EFDocMsgFormat_XmlSubmit_BR.createXmlDocumentFromEFDocument</span></span>|
|<span data-ttu-id="fa00f-233">EFDocumentXpath_BR.Not 適用</span><span class="sxs-lookup"><span data-stu-id="fa00f-233">EFDocumentXpath_BR.Not applied</span></span>|
|<span data-ttu-id="fa00f-234">ERclasses - クラス署名</span><span class="sxs-lookup"><span data-stu-id="fa00f-234">ERclasses - class signature</span></span>|
|<span data-ttu-id="fa00f-235">FiscalDocParmDataCreatorInvTransfer_BR.initHeaderParmData</span><span class="sxs-lookup"><span data-stu-id="fa00f-235">FiscalDocParmDataCreatorInvTransfer_BR.initHeaderParmData</span></span>|
|<span data-ttu-id="fa00f-236">FiscalDocParmDataCreatorInvTransfer_BR.setinventTransferTableFiscalInfo</span><span class="sxs-lookup"><span data-stu-id="fa00f-236">FiscalDocParmDataCreatorInvTransfer_BR.setinventTransferTableFiscalInfo</span></span>|
|<span data-ttu-id="fa00f-237">FiscalDocumentParmDataCreator_BR.initTaxTransParmDataFromTaxTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-237">FiscalDocumentParmDataCreator_BR.initTaxTransParmDataFromTaxTrans</span></span>|
|<span data-ttu-id="fa00f-238">FiscalDocumentParmDataCreator_BR.setAccountingAmountOnFiscalDocumentLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-238">FiscalDocumentParmDataCreator_BR.setAccountingAmountOnFiscalDocumentLines</span></span>|
|<span data-ttu-id="fa00f-239">FiscalDocumentPost_BR.initFiscalDocument</span><span class="sxs-lookup"><span data-stu-id="fa00f-239">FiscalDocumentPost_BR.initFiscalDocument</span></span>|
|<span data-ttu-id="fa00f-240">FreeTextInvoiceDP.insertIntoFreeTextInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="fa00f-240">FreeTextInvoiceDP.insertIntoFreeTextInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="fa00f-241">HcmWorkerTransition.createHcmEmployment</span><span class="sxs-lookup"><span data-stu-id="fa00f-241">HcmWorkerTransition.createHcmEmployment</span></span>|
|<span data-ttu-id="fa00f-242">HrpExpireWorkerLimits.expireLimitRequest,expireApprovedLimit,getAuthorityBasis</span><span class="sxs-lookup"><span data-stu-id="fa00f-242">HrpExpireWorkerLimits.expireLimitRequest,expireApprovedLimit,getAuthorityBasis</span></span>|
|<span data-ttu-id="fa00f-243">InventMov_Sales.accountBalanceSheet</span><span class="sxs-lookup"><span data-stu-id="fa00f-243">InventMov_Sales.accountBalanceSheet</span></span>|
|<span data-ttu-id="fa00f-244">InventReleaseOrderPickingForm_Sales.bldInventReleaseOrderPickingTmp</span><span class="sxs-lookup"><span data-stu-id="fa00f-244">InventReleaseOrderPickingForm_Sales.bldInventReleaseOrderPickingTmp</span></span>|
|<span data-ttu-id="fa00f-245">InventTestAssociationTable.checkExecutionTime</span><span class="sxs-lookup"><span data-stu-id="fa00f-245">InventTestAssociationTable.checkExecutionTime</span></span>|
|<span data-ttu-id="fa00f-246">InventTrans.insertReturnTransOrigin</span><span class="sxs-lookup"><span data-stu-id="fa00f-246">InventTrans.insertReturnTransOrigin</span></span>|
|<span data-ttu-id="fa00f-247">InventTrans.updateMarkReqTransCov</span><span class="sxs-lookup"><span data-stu-id="fa00f-247">InventTrans.updateMarkReqTransCov</span></span>|
|<span data-ttu-id="fa00f-248">InventTransferOrderCopying_BR.createTransferLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-248">InventTransferOrderCopying_BR.createTransferLines</span></span>|
|<span data-ttu-id="fa00f-249">InventTransferOrderCopying_BR.createTransferOrder</span><span class="sxs-lookup"><span data-stu-id="fa00f-249">InventTransferOrderCopying_BR.createTransferOrder</span></span>|
|<span data-ttu-id="fa00f-250">InventTransferUpdShip.updateInventTransferLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-250">InventTransferUpdShip.updateInventTransferLine</span></span>|
|<span data-ttu-id="fa00f-251">InventUnusedDimCleanup.isCandidateInventDimIdTable</span><span class="sxs-lookup"><span data-stu-id="fa00f-251">InventUnusedDimCleanup.isCandidateInventDimIdTable</span></span>|
|<span data-ttu-id="fa00f-252">InventUpd_ChangeDimension.updateTransSwitchDim</span><span class="sxs-lookup"><span data-stu-id="fa00f-252">InventUpd_ChangeDimension.updateTransSwitchDim</span></span>|
|<span data-ttu-id="fa00f-253">InventUpd_ChildReference.updateLessReceipt</span><span class="sxs-lookup"><span data-stu-id="fa00f-253">InventUpd_ChildReference.updateLessReceipt</span></span>|
|<span data-ttu-id="fa00f-254">InventUpd_ChildReference.UpdateMoreReceipt</span><span class="sxs-lookup"><span data-stu-id="fa00f-254">InventUpd_ChildReference.UpdateMoreReceipt</span></span>|
|<span data-ttu-id="fa00f-255">InventUpd_Financial.updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="fa00f-255">InventUpd_Financial.updateFinancialIssue</span></span>|
|<span data-ttu-id="fa00f-256">InventUpd_Financial.updateStdCostPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-256">InventUpd_Financial.updateStdCostPrice</span></span>|
|<span data-ttu-id="fa00f-257">InventUpd_Picked.updatePickMore</span><span class="sxs-lookup"><span data-stu-id="fa00f-257">InventUpd_Picked.updatePickMore</span></span>|
|<span data-ttu-id="fa00f-258">InventUpd_Registered.updateRegisterLess</span><span class="sxs-lookup"><span data-stu-id="fa00f-258">InventUpd_Registered.updateRegisterLess</span></span>|
|<span data-ttu-id="fa00f-259">InventUpd_Registered.updateRegisterMore</span><span class="sxs-lookup"><span data-stu-id="fa00f-259">InventUpd_Registered.updateRegisterMore</span></span>|
|<span data-ttu-id="fa00f-260">InventUpd_Reservation.updateReserveLess</span><span class="sxs-lookup"><span data-stu-id="fa00f-260">InventUpd_Reservation.updateReserveLess</span></span>|
|<span data-ttu-id="fa00f-261">InventUpdate.initializeInventTransToIssueListFromDatabase</span><span class="sxs-lookup"><span data-stu-id="fa00f-261">InventUpdate.initializeInventTransToIssueListFromDatabase</span></span>|
|<span data-ttu-id="fa00f-262">InventUpdate.initInventTransToReceiveList</span><span class="sxs-lookup"><span data-stu-id="fa00f-262">InventUpdate.initInventTransToReceiveList</span></span>|
|<span data-ttu-id="fa00f-263">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span><span class="sxs-lookup"><span data-stu-id="fa00f-263">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span></span>|
|<span data-ttu-id="fa00f-264">JmgPaySpecificationDP.Class 宣言</span><span class="sxs-lookup"><span data-stu-id="fa00f-264">JmgPaySpecificationDP.Class declaration</span></span>|
|<span data-ttu-id="fa00f-265">JmgPostStandardSystem.getProjTransCostPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-265">JmgPostStandardSystem.getProjTransCostPrice</span></span>|
|<span data-ttu-id="fa00f-266">JmgPostStandardSystem.postIPCTime</span><span class="sxs-lookup"><span data-stu-id="fa00f-266">JmgPostStandardSystem.postIPCTime</span></span>|
|<span data-ttu-id="fa00f-267">JmgPostStandardSystem.postProjTime</span><span class="sxs-lookup"><span data-stu-id="fa00f-267">JmgPostStandardSystem.postProjTime</span></span>|
|<span data-ttu-id="fa00f-268">JmgProfiles.bundleSlizeTime</span><span class="sxs-lookup"><span data-stu-id="fa00f-268">JmgProfiles.bundleSlizeTime</span></span>|
|<span data-ttu-id="fa00f-269">JmgProfiles.insertTimeGapsPlannedAbs</span><span class="sxs-lookup"><span data-stu-id="fa00f-269">JmgProfiles.insertTimeGapsPlannedAbs</span></span>|
|<span data-ttu-id="fa00f-270">JmgProfiles.sumPayEventsSec</span><span class="sxs-lookup"><span data-stu-id="fa00f-270">JmgProfiles.sumPayEventsSec</span></span>|
|<span data-ttu-id="fa00f-271">JmgStampJournalTransfer.insertStampTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-271">JmgStampJournalTransfer.insertStampTrans</span></span>|
|<span data-ttu-id="fa00f-272">JmgTransferEvents.createPayEventsArray</span><span class="sxs-lookup"><span data-stu-id="fa00f-272">JmgTransferEvents.createPayEventsArray</span></span>|
|<span data-ttu-id="fa00f-273">JmgTransferEvents.insertEvents</span><span class="sxs-lookup"><span data-stu-id="fa00f-273">JmgTransferEvents.insertEvents</span></span>|
|<span data-ttu-id="fa00f-274">JournalizingDefinitionManagerPurch.getDefaultJournalizingDefinition</span><span class="sxs-lookup"><span data-stu-id="fa00f-274">JournalizingDefinitionManagerPurch.getDefaultJournalizingDefinition</span></span>|
|<span data-ttu-id="fa00f-275">LedgerAccrualTrans.post</span><span class="sxs-lookup"><span data-stu-id="fa00f-275">LedgerAccrualTrans.post</span></span>|
|<span data-ttu-id="fa00f-276">LedgerAllocationBasisRules.getBasisAmount</span><span class="sxs-lookup"><span data-stu-id="fa00f-276">LedgerAllocationBasisRules.getBasisAmount</span></span>|
|<span data-ttu-id="fa00f-277">LedgerJournalCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="fa00f-277">LedgerJournalCheckPost.checkJournal</span></span>|
|<span data-ttu-id="fa00f-278">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="fa00f-278">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="fa00f-279">LedgerJournalCheckPost.postTransV2</span><span class="sxs-lookup"><span data-stu-id="fa00f-279">LedgerJournalCheckPost.postTransV2</span></span>|
|<span data-ttu-id="fa00f-280">LedgerJournalCheckPost.updateInterCompanyJournal</span><span class="sxs-lookup"><span data-stu-id="fa00f-280">LedgerJournalCheckPost.updateInterCompanyJournal</span></span>|
|<span data-ttu-id="fa00f-281">LedgerJournalTrans.markedForSettlementError</span><span class="sxs-lookup"><span data-stu-id="fa00f-281">LedgerJournalTrans.markedForSettlementError</span></span>|
|<span data-ttu-id="fa00f-282">LedgerJournalTrans.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="fa00f-282">LedgerJournalTrans.validateWrite_Server</span></span>|
|<span data-ttu-id="fa00f-283">LedgerJournalTransProject.checkProjId</span><span class="sxs-lookup"><span data-stu-id="fa00f-283">LedgerJournalTransProject.checkProjId</span></span>|
|<span data-ttu-id="fa00f-284">LedgerJournalTransUpdate.updateInterCompany</span><span class="sxs-lookup"><span data-stu-id="fa00f-284">LedgerJournalTransUpdate.updateInterCompany</span></span>|
|<span data-ttu-id="fa00f-285">LedgerJournalTransUpdateBank.updateNow</span><span class="sxs-lookup"><span data-stu-id="fa00f-285">LedgerJournalTransUpdateBank.updateNow</span></span>|
|<span data-ttu-id="fa00f-286">LedgerJournalTransUpdateCust.updateNow</span><span class="sxs-lookup"><span data-stu-id="fa00f-286">LedgerJournalTransUpdateCust.updateNow</span></span>|
|<span data-ttu-id="fa00f-287">LedgerJournalTransUpdateLedger.createTaxLinkForTaxTransfer</span><span class="sxs-lookup"><span data-stu-id="fa00f-287">LedgerJournalTransUpdateLedger.createTaxLinkForTaxTransfer</span></span>|
|<span data-ttu-id="fa00f-288">LedgerJournalTransUpdateLedger.updateNow</span><span class="sxs-lookup"><span data-stu-id="fa00f-288">LedgerJournalTransUpdateLedger.updateNow</span></span>|
|<span data-ttu-id="fa00f-289">LedgerJournalTransUpdateVend.updateNow</span><span class="sxs-lookup"><span data-stu-id="fa00f-289">LedgerJournalTransUpdateVend.updateNow</span></span>|
|<span data-ttu-id="fa00f-290">LedgerTransPerJournalDP.insertForLedgerBase</span><span class="sxs-lookup"><span data-stu-id="fa00f-290">LedgerTransPerJournalDP.insertForLedgerBase</span></span>|
|<span data-ttu-id="fa00f-291">LedgerTransPerJournalDP.insertVoucherDetails</span><span class="sxs-lookup"><span data-stu-id="fa00f-291">LedgerTransPerJournalDP.insertVoucherDetails</span></span>|
|<span data-ttu-id="fa00f-292">LedgerTransPerJournalDP.processReport</span><span class="sxs-lookup"><span data-stu-id="fa00f-292">LedgerTransPerJournalDP.processReport</span></span>|
|<span data-ttu-id="fa00f-293">LedgerVoucher.check</span><span class="sxs-lookup"><span data-stu-id="fa00f-293">LedgerVoucher.check</span></span>|
|<span data-ttu-id="fa00f-294">LedgerVoucherGroup.end</span><span class="sxs-lookup"><span data-stu-id="fa00f-294">LedgerVoucherGroup.end</span></span>|
|<span data-ttu-id="fa00f-295">LedgerVoucherObject.addBalanceAdjustments</span><span class="sxs-lookup"><span data-stu-id="fa00f-295">LedgerVoucherObject.addBalanceAdjustments</span></span>|
|<span data-ttu-id="fa00f-296">LedgerVoucherObject.allocateTransaction</span><span class="sxs-lookup"><span data-stu-id="fa00f-296">LedgerVoucherObject.allocateTransaction</span></span>|
|<span data-ttu-id="fa00f-297">LedgerVoucherObject.post</span><span class="sxs-lookup"><span data-stu-id="fa00f-297">LedgerVoucherObject.post</span></span>|
|<span data-ttu-id="fa00f-298">LedgerVoucherObject.updateBalances</span><span class="sxs-lookup"><span data-stu-id="fa00f-298">LedgerVoucherObject.updateBalances</span></span>|
|<span data-ttu-id="fa00f-299">LedgerVoucherTransObject.check</span><span class="sxs-lookup"><span data-stu-id="fa00f-299">LedgerVoucherTransObject.check</span></span>|
|<span data-ttu-id="fa00f-300">Markup.copy</span><span class="sxs-lookup"><span data-stu-id="fa00f-300">Markup.copy</span></span>|
|<span data-ttu-id="fa00f-301">McrPriceHistoryLine_Sales.initAndInsertRebate</span><span class="sxs-lookup"><span data-stu-id="fa00f-301">McrPriceHistoryLine_Sales.initAndInsertRebate</span></span>|
|<span data-ttu-id="fa00f-302">メソッド署名: 測定単位宣言を行う前にコンテキスト情報を追加する</span><span class="sxs-lookup"><span data-stu-id="fa00f-302">Method signature: Adding contextual information before doing Unit of Measure calculation</span></span>|
|<span data-ttu-id="fa00f-303">PdsRebateFindAndCreate.findPdsRebateAgreementLineAndCreate</span><span class="sxs-lookup"><span data-stu-id="fa00f-303">PdsRebateFindAndCreate.findPdsRebateAgreementLineAndCreate</span></span>|
|<span data-ttu-id="fa00f-304">PdsRebateFindAndCreate.tamFindBillBackAgreementAndCreateClaim</span><span class="sxs-lookup"><span data-stu-id="fa00f-304">PdsRebateFindAndCreate.tamFindBillBackAgreementAndCreateClaim</span></span>|
|<span data-ttu-id="fa00f-305">PriceDisc.findDisc</span><span class="sxs-lookup"><span data-stu-id="fa00f-305">PriceDisc.findDisc</span></span>|
|<span data-ttu-id="fa00f-306">PriceDisc.findDiscAgreement</span><span class="sxs-lookup"><span data-stu-id="fa00f-306">PriceDisc.findDiscAgreement</span></span>|
|<span data-ttu-id="fa00f-307">PriceDisc.findItemPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-307">PriceDisc.findItemPrice</span></span>|
|<span data-ttu-id="fa00f-308">PriceDisc.findPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-308">PriceDisc.findPrice</span></span>|
|<span data-ttu-id="fa00f-309">PriceDisc.findPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="fa00f-309">PriceDisc.findPriceAgreement</span></span>|
|<span data-ttu-id="fa00f-310">PriceDiscAdmCheckPost.runFromContract</span><span class="sxs-lookup"><span data-stu-id="fa00f-310">PriceDiscAdmCheckPost.runFromContract</span></span>|
|<span data-ttu-id="fa00f-311">ProdJournalCheckPost.postProdJournalTableBOM</span><span class="sxs-lookup"><span data-stu-id="fa00f-311">ProdJournalCheckPost.postProdJournalTableBOM</span></span>|
|<span data-ttu-id="fa00f-312">ProdJournalCheckPostProd.postTransLedger</span><span class="sxs-lookup"><span data-stu-id="fa00f-312">ProdJournalCheckPostProd.postTransLedger</span></span>|
|<span data-ttu-id="fa00f-313">ProdJournalCreateBom.createSingleLineProdBOM</span><span class="sxs-lookup"><span data-stu-id="fa00f-313">ProdJournalCreateBom.createSingleLineProdBOM</span></span>|
|<span data-ttu-id="fa00f-314">ProdTableCleanUp.deleteProductions</span><span class="sxs-lookup"><span data-stu-id="fa00f-314">ProdTableCleanUp.deleteProductions</span></span>|
|<span data-ttu-id="fa00f-315">ProdUpdCostEstimation.costEstimateItems</span><span class="sxs-lookup"><span data-stu-id="fa00f-315">ProdUpdCostEstimation.costEstimateItems</span></span>|
|<span data-ttu-id="fa00f-316">ProdUpdCostestimation.updateSubProdTable</span><span class="sxs-lookup"><span data-stu-id="fa00f-316">ProdUpdCostestimation.updateSubProdTable</span></span>|
|<span data-ttu-id="fa00f-317">ProdUpdReportFinished.updateBomConsumption</span><span class="sxs-lookup"><span data-stu-id="fa00f-317">ProdUpdReportFinished.updateBomConsumption</span></span>|
|<span data-ttu-id="fa00f-318">ProdUpdStartup.UpdateBomConsumption</span><span class="sxs-lookup"><span data-stu-id="fa00f-318">ProdUpdStartup.UpdateBomConsumption</span></span>|
|<span data-ttu-id="fa00f-319">ProjAdjustment.getNewTotalCostAmount</span><span class="sxs-lookup"><span data-stu-id="fa00f-319">ProjAdjustment.getNewTotalCostAmount</span></span>|
|<span data-ttu-id="fa00f-320">ProjAdjustment.setHourCostPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-320">ProjAdjustment.setHourCostPrice</span></span>|
|<span data-ttu-id="fa00f-321">ProjAdjustmentSplit.createNewTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-321">ProjAdjustmentSplit.createNewTrans</span></span>|
|<span data-ttu-id="fa00f-322">ProjAdjustmentSplit.initializeTmpProjAdjustmentCreate</span><span class="sxs-lookup"><span data-stu-id="fa00f-322">ProjAdjustmentSplit.initializeTmpProjAdjustmentCreate</span></span>|
|<span data-ttu-id="fa00f-323">ProjAdjustmentUpdate_Post.post</span><span class="sxs-lookup"><span data-stu-id="fa00f-323">ProjAdjustmentUpdate_Post.post</span></span>|
|<span data-ttu-id="fa00f-324">ProjAdjustmentUpdate_Post.postCost</span><span class="sxs-lookup"><span data-stu-id="fa00f-324">ProjAdjustmentUpdate_Post.postCost</span></span>|
|<span data-ttu-id="fa00f-325">ProjAdjustmentUpdate_Post.postItem</span><span class="sxs-lookup"><span data-stu-id="fa00f-325">ProjAdjustmentUpdate_Post.postItem</span></span>|
|<span data-ttu-id="fa00f-326">ProjBudget.queryProjBudgetLineCost / ProjBudgetLineCost(DataSource)</span><span class="sxs-lookup"><span data-stu-id="fa00f-326">ProjBudget.queryProjBudgetLineCost / ProjBudgetLineCost(DataSource)</span></span>|
|<span data-ttu-id="fa00f-327">ProjBudget.queryProjBudgetLineCost / ProjBudgetLineRevenue(DataSource)</span><span class="sxs-lookup"><span data-stu-id="fa00f-327">ProjBudget.queryProjBudgetLineCost / ProjBudgetLineRevenue(DataSource)</span></span>|
|<span data-ttu-id="fa00f-328">ProjBudgetManager.createBudgetFromForecastModel</span><span class="sxs-lookup"><span data-stu-id="fa00f-328">ProjBudgetManager.createBudgetFromForecastModel</span></span>|
|<span data-ttu-id="fa00f-329">ProjCategoryLookup.buildQueryTsTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-329">ProjCategoryLookup.buildQueryTsTimesheetLine</span></span>|
|<span data-ttu-id="fa00f-330">ProjInvoiceChoose.main</span><span class="sxs-lookup"><span data-stu-id="fa00f-330">ProjInvoiceChoose.main</span></span>|
|<span data-ttu-id="fa00f-331">ProjInvoiceJournalCreate.initJournalHeader</span><span class="sxs-lookup"><span data-stu-id="fa00f-331">ProjInvoiceJournalCreate.initJournalHeader</span></span>|
|<span data-ttu-id="fa00f-332">ProjInvoiceJournalPost.createProjInvoiceSalesLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-332">ProjInvoiceJournalPost.createProjInvoiceSalesLine</span></span>|
|<span data-ttu-id="fa00f-333">ProjInvoiceProposalInsertLines.doCost、doEmpl、doItem、doOnAccount、doRevenue、doSalesLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-333">ProjInvoiceProposalInsertLines.doCost, doEmpl, doItem, doOnAccount, doRevenue, doSalesLine</span></span>|
|<span data-ttu-id="fa00f-334">ProjInvoiceProposalPeriodic.Validate</span><span class="sxs-lookup"><span data-stu-id="fa00f-334">ProjInvoiceProposalPeriodic.Validate</span></span>|
|<span data-ttu-id="fa00f-335">ProjJournalTrans.setHourCostPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-335">ProjJournalTrans.setHourCostPrice</span></span>|
|<span data-ttu-id="fa00f-336">ProjJournalTrans.setHourPrices</span><span class="sxs-lookup"><span data-stu-id="fa00f-336">ProjJournalTrans.setHourPrices</span></span>|
|<span data-ttu-id="fa00f-337">ProjJournalTrans.setHourSalesPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-337">ProjJournalTrans.setHourSalesPrice</span></span>|
|<span data-ttu-id="fa00f-338">ProjPlanVersionsManager.CopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="fa00f-338">ProjPlanVersionsManager.CopyHierarchy</span></span>|
|<span data-ttu-id="fa00f-339">ProjPost.postCost</span><span class="sxs-lookup"><span data-stu-id="fa00f-339">ProjPost.postCost</span></span>|
|<span data-ttu-id="fa00f-340">ProjPostCostProposalSale.projTransUpdate</span><span class="sxs-lookup"><span data-stu-id="fa00f-340">ProjPostCostProposalSale.projTransUpdate</span></span>|
|<span data-ttu-id="fa00f-341">ProjPostEmplProposalSale.projTransUpdate</span><span class="sxs-lookup"><span data-stu-id="fa00f-341">ProjPostEmplProposalSale.projTransUpdate</span></span>|
|<span data-ttu-id="fa00f-342">ProjPostItemProposalSale.projTransUpdate</span><span class="sxs-lookup"><span data-stu-id="fa00f-342">ProjPostItemProposalSale.projTransUpdate</span></span>|
|<span data-ttu-id="fa00f-343">ProjPostRevenueProposalSale.projTransUpdate</span><span class="sxs-lookup"><span data-stu-id="fa00f-343">ProjPostRevenueProposalSale.projTransUpdate</span></span>|
|<span data-ttu-id="fa00f-344">ProjTable.createSalesTable_ItemReq</span><span class="sxs-lookup"><span data-stu-id="fa00f-344">ProjTable.createSalesTable_ItemReq</span></span>|
|<span data-ttu-id="fa00f-345">ProjTable.editSubProjects</span><span class="sxs-lookup"><span data-stu-id="fa00f-345">ProjTable.editSubProjects</span></span>|
|<span data-ttu-id="fa00f-346">psaContractLineInvoiceDP.insertTmpPSAContractLineInvoice</span><span class="sxs-lookup"><span data-stu-id="fa00f-346">psaContractLineInvoiceDP.insertTmpPSAContractLineInvoice</span></span>|
|<span data-ttu-id="fa00f-347">PsaGenerateQuotationLines.createSalesQuotationLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-347">PsaGenerateQuotationLines.createSalesQuotationLines</span></span>|
|<span data-ttu-id="fa00f-348">PsaManageInvoiceDP.insertTmpPSAManageInvoice</span><span class="sxs-lookup"><span data-stu-id="fa00f-348">PsaManageInvoiceDP.insertTmpPSAManageInvoice</span></span>|
|<span data-ttu-id="fa00f-349">PSAProjInvoiceDP.processLinesFromInvoiceJournal</span><span class="sxs-lookup"><span data-stu-id="fa00f-349">PSAProjInvoiceDP.processLinesFromInvoiceJournal</span></span>|
|<span data-ttu-id="fa00f-350">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span><span class="sxs-lookup"><span data-stu-id="fa00f-350">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span></span>|
|<span data-ttu-id="fa00f-351">PSAProjPostEmplIndirectProposal.indirectCreditAccountTurnover</span><span class="sxs-lookup"><span data-stu-id="fa00f-351">PSAProjPostEmplIndirectProposal.indirectCreditAccountTurnover</span></span>|
|<span data-ttu-id="fa00f-352">PurchCreateFromSalesOrder.autoCreatePurchOrder</span><span class="sxs-lookup"><span data-stu-id="fa00f-352">PurchCreateFromSalesOrder.autoCreatePurchOrder</span></span>|
|<span data-ttu-id="fa00f-353">PurchCreateFromSalesOrder.checkLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-353">PurchCreateFromSalesOrder.checkLine</span></span>|
|<span data-ttu-id="fa00f-354">PurchCreateFromSalesOrder.main</span><span class="sxs-lookup"><span data-stu-id="fa00f-354">PurchCreateFromSalesOrder.main</span></span>|
|<span data-ttu-id="fa00f-355">PurchCreateFromSalesOrder.querySalesLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-355">PurchCreateFromSalesOrder.querySalesLine</span></span>|
|<span data-ttu-id="fa00f-356">PurchCreateFromSalesOrder.run</span><span class="sxs-lookup"><span data-stu-id="fa00f-356">PurchCreateFromSalesOrder.run</span></span>|
|<span data-ttu-id="fa00f-357">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span><span class="sxs-lookup"><span data-stu-id="fa00f-357">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span></span>|
|<span data-ttu-id="fa00f-358">PurchFormletterParmDataInvoice.createInvoiceHeaderFromTempTable</span><span class="sxs-lookup"><span data-stu-id="fa00f-358">PurchFormletterParmDataInvoice.createInvoiceHeaderFromTempTable</span></span>|
|<span data-ttu-id="fa00f-359">PurchFormletterParmDataInvoice.createLineAsset</span><span class="sxs-lookup"><span data-stu-id="fa00f-359">PurchFormletterParmDataInvoice.createLineAsset</span></span>|
|<span data-ttu-id="fa00f-360">PurchFormletterParmDataInvoice.selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-360">PurchFormletterParmDataInvoice.selectChooseLines</span></span>|
|<span data-ttu-id="fa00f-361">PurchInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="fa00f-361">PurchInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="fa00f-362">PurchLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="fa00f-362">PurchLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="fa00f-363">PurchOrderLineSourceDocumentLineItem.initMonetaryAmountValue</span><span class="sxs-lookup"><span data-stu-id="fa00f-363">PurchOrderLineSourceDocumentLineItem.initMonetaryAmountValue</span></span>|
|<span data-ttu-id="fa00f-364">PurchReApprovalPolicyRule.evaluatePolicy</span><span class="sxs-lookup"><span data-stu-id="fa00f-364">PurchReApprovalPolicyRule.evaluatePolicy</span></span>|
|<span data-ttu-id="fa00f-365">PurchRFQAcceptJournalPost.updateSourceTable</span><span class="sxs-lookup"><span data-stu-id="fa00f-365">PurchRFQAcceptJournalPost.updateSourceTable</span></span>|
|<span data-ttu-id="fa00f-366">PurchRFQSendJournalCreate.createOrUpdateRFQLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-366">PurchRFQSendJournalCreate.createOrUpdateRFQLine</span></span>|
|<span data-ttu-id="fa00f-367">PurchTableForm.main</span><span class="sxs-lookup"><span data-stu-id="fa00f-367">PurchTableForm.main</span></span>|
|<span data-ttu-id="fa00f-368">rDeferralsJournal.createTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-368">rDeferralsJournal.createTrans</span></span>|
|<span data-ttu-id="fa00f-369">rDeferralsProposalReceipt.createJournalLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-369">rDeferralsProposalReceipt.createJournalLines</span></span>|
|<span data-ttu-id="fa00f-370">rDeferralsProposalRetirement.createJournalLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-370">rDeferralsProposalRetirement.createJournalLines</span></span>|
|<span data-ttu-id="fa00f-371">rDeferralsProposalWritingOff.createJournalLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-371">rDeferralsProposalWritingOff.createJournalLines</span></span>|
|<span data-ttu-id="fa00f-372">rDeferralsTableMethodIterator.new</span><span class="sxs-lookup"><span data-stu-id="fa00f-372">rDeferralsTableMethodIterator.new</span></span>|
|<span data-ttu-id="fa00f-373">ReqDemPlanForecastAggregator.deaggregate</span><span class="sxs-lookup"><span data-stu-id="fa00f-373">ReqDemPlanForecastAggregator.deaggregate</span></span>|
|<span data-ttu-id="fa00f-374">ReqDemPlanImportForecastService.insertDemandForecast</span><span class="sxs-lookup"><span data-stu-id="fa00f-374">ReqDemPlanImportForecastService.insertDemandForecast</span></span>|
|<span data-ttu-id="fa00f-375">ReqIntercompanyDemand.initReqTransFromIntercompanyReqPO</span><span class="sxs-lookup"><span data-stu-id="fa00f-375">ReqIntercompanyDemand.initReqTransFromIntercompanyReqPO</span></span>|
|<span data-ttu-id="fa00f-376">ReqPO.Update</span><span class="sxs-lookup"><span data-stu-id="fa00f-376">ReqPO.Update</span></span>|
|<span data-ttu-id="fa00f-377">ReqTrans.updateBOMQty</span><span class="sxs-lookup"><span data-stu-id="fa00f-377">ReqTrans.updateBOMQty</span></span>|
|<span data-ttu-id="fa00f-378">ReqTransPoMarkSumUp.updateSumUp</span><span class="sxs-lookup"><span data-stu-id="fa00f-378">ReqTransPoMarkSumUp.updateSumUp</span></span>|
|<span data-ttu-id="fa00f-379">RequisitionReleaseStrategy.runAutoPurchOrderGeneration</span><span class="sxs-lookup"><span data-stu-id="fa00f-379">RequisitionReleaseStrategy.runAutoPurchOrderGeneration</span></span>|
|<span data-ttu-id="fa00f-380">RetailTransactionSalesTransMark.findInventDimFromWorkingTable; など。添付ファイルを確認してください</span><span class="sxs-lookup"><span data-stu-id="fa00f-380">RetailTransactionSalesTransMark.findInventDimFromWorkingTable; and more please review attachment</span></span>|
|<span data-ttu-id="fa00f-381">RetailTransactionSalesTransMark.updateTransactionSalesLine_InventDimId</span><span class="sxs-lookup"><span data-stu-id="fa00f-381">RetailTransactionSalesTransMark.updateTransactionSalesLine_InventDimId</span></span>|
|<span data-ttu-id="fa00f-382">RetailTransactionServiceOrder.createOrUpdateRetailOrderLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-382">RetailTransactionServiceOrder.createOrUpdateRetailOrderLines</span></span>|
|<span data-ttu-id="fa00f-383">RetailTransactionServiceOrders.cancelCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="fa00f-383">RetailTransactionServiceOrders.cancelCustomerOrder</span></span>|
|<span data-ttu-id="fa00f-384">RunBaseMultiParm.initFromForm</span><span class="sxs-lookup"><span data-stu-id="fa00f-384">RunBaseMultiParm.initFromForm</span></span>|
|<span data-ttu-id="fa00f-385">SalesCopying.callerSalesTable.returnItem</span><span class="sxs-lookup"><span data-stu-id="fa00f-385">SalesCopying.callerSalesTable.returnItem</span></span>|
|<span data-ttu-id="fa00f-386">SalesFormletterParmDataInvoice.createBasedOnPackingSlip</span><span class="sxs-lookup"><span data-stu-id="fa00f-386">SalesFormletterParmDataInvoice.createBasedOnPackingSlip</span></span>|
|<span data-ttu-id="fa00f-387">SalesInvoiceController.initFormLetterReport</span><span class="sxs-lookup"><span data-stu-id="fa00f-387">SalesInvoiceController.initFormLetterReport</span></span>|
|<span data-ttu-id="fa00f-388">SalesInvoiceController.parmRunOnBlockMode_TH</span><span class="sxs-lookup"><span data-stu-id="fa00f-388">SalesInvoiceController.parmRunOnBlockMode_TH</span></span>|
|<span data-ttu-id="fa00f-389">SalesInvoiceController.PrintMgmtPrintSettingDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-389">SalesInvoiceController.PrintMgmtPrintSettingDetail</span></span>|
|<span data-ttu-id="fa00f-390">SalesInvoiceDP.addProductDimensionsToInventDim; tmpTaxWorkTrans;</span><span class="sxs-lookup"><span data-stu-id="fa00f-390">SalesInvoiceDP.addProductDimensionsToInventDim; tmpTaxWorkTrans;</span></span>|
|<span data-ttu-id="fa00f-391">SalesInvoiceDP.initInventDimData</span><span class="sxs-lookup"><span data-stu-id="fa00f-391">SalesInvoiceDP.initInventDimData</span></span>|
|<span data-ttu-id="fa00f-392">SalesInvoiceDP.populateSalesInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="fa00f-392">SalesInvoiceDP.populateSalesInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="fa00f-393">SalesInvoiceDP.printBackorders</span><span class="sxs-lookup"><span data-stu-id="fa00f-393">SalesInvoiceDP.printBackorders</span></span>|
|<span data-ttu-id="fa00f-394">SalesInvoiceDPBase.createData</span><span class="sxs-lookup"><span data-stu-id="fa00f-394">SalesInvoiceDPBase.createData</span></span>|
|<span data-ttu-id="fa00f-395">SalesInvoiceDPBase.init</span><span class="sxs-lookup"><span data-stu-id="fa00f-395">SalesInvoiceDPBase.init</span></span>|
|<span data-ttu-id="fa00f-396">SalesInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="fa00f-396">SalesInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="fa00f-397">SalesInvoiceJournalPost.postLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-397">SalesInvoiceJournalPost.postLine</span></span>|
|<span data-ttu-id="fa00f-398">SalesLineType.pmfValidateBatchId</span><span class="sxs-lookup"><span data-stu-id="fa00f-398">SalesLineType.pmfValidateBatchId</span></span>|
|<span data-ttu-id="fa00f-399">SalesLineType_ReturnItem.validateField</span><span class="sxs-lookup"><span data-stu-id="fa00f-399">SalesLineType_ReturnItem.validateField</span></span>|
|<span data-ttu-id="fa00f-400">SalesPackingSlipController.initFormLetterReport</span><span class="sxs-lookup"><span data-stu-id="fa00f-400">SalesPackingSlipController.initFormLetterReport</span></span>|
|<span data-ttu-id="fa00f-401">SalesPackingSlipController.parmRunOnBlockMode_TH</span><span class="sxs-lookup"><span data-stu-id="fa00f-401">SalesPackingSlipController.parmRunOnBlockMode_TH</span></span>|
|<span data-ttu-id="fa00f-402">SalesPackingSlipDP.checkPrintLineHeader</span><span class="sxs-lookup"><span data-stu-id="fa00f-402">SalesPackingSlipDP.checkPrintLineHeader</span></span>|
|<span data-ttu-id="fa00f-403">SalesPackingSlipDP.initializeInventDimReportSetup</span><span class="sxs-lookup"><span data-stu-id="fa00f-403">SalesPackingSlipDP.initializeInventDimReportSetup</span></span>|
|<span data-ttu-id="fa00f-404">SalesPackingSlipJournalPost.updateInventory</span><span class="sxs-lookup"><span data-stu-id="fa00f-404">SalesPackingSlipJournalPost.updateInventory</span></span>|
|<span data-ttu-id="fa00f-405">SalesParmTable.createPaymentSched</span><span class="sxs-lookup"><span data-stu-id="fa00f-405">SalesParmTable.createPaymentSched</span></span>|
|<span data-ttu-id="fa00f-406">SalesPurchOperationTypeController_BR.getReferenceLookup</span><span class="sxs-lookup"><span data-stu-id="fa00f-406">SalesPurchOperationTypeController_BR.getReferenceLookup</span></span>|
|<span data-ttu-id="fa00f-407">SalesQuotationDP.initializeInventDimReport</span><span class="sxs-lookup"><span data-stu-id="fa00f-407">SalesQuotationDP.initializeInventDimReport</span></span>|
|<span data-ttu-id="fa00f-408">SalesQuotationProjLinkWizard.endUpdate</span><span class="sxs-lookup"><span data-stu-id="fa00f-408">SalesQuotationProjLinkWizard.endUpdate</span></span>|
|<span data-ttu-id="fa00f-409">SalesQuotationTableType.disableFieldsIfCustomerAccountNotSpecified</span><span class="sxs-lookup"><span data-stu-id="fa00f-409">SalesQuotationTableType.disableFieldsIfCustomerAccountNotSpecified</span></span>|
|<span data-ttu-id="fa00f-410">SingleReturn.POSDeveloperSupport</span><span class="sxs-lookup"><span data-stu-id="fa00f-410">SingleReturn.POSDeveloperSupport</span></span>|
|<span data-ttu-id="fa00f-411">SubledgerJournalizer.addRelievingAccountingDistributions</span><span class="sxs-lookup"><span data-stu-id="fa00f-411">SubledgerJournalizer.addRelievingAccountingDistributions</span></span>|
|<span data-ttu-id="fa00f-412">SubledgerJournalizer.fillPreviewTmpSummaryWithRounding</span><span class="sxs-lookup"><span data-stu-id="fa00f-412">SubledgerJournalizer.fillPreviewTmpSummaryWithRounding</span></span>|
|<span data-ttu-id="fa00f-413">SubledgerJournalizer.loadaccountingDistributionTmp</span><span class="sxs-lookup"><span data-stu-id="fa00f-413">SubledgerJournalizer.loadaccountingDistributionTmp</span></span>|
|<span data-ttu-id="fa00f-414">SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-414">SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-415">SubledgerJournalizer.loadInterCompanyNonOffsetSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-415">SubledgerJournalizer.loadInterCompanyNonOffsetSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-416">SubledgerJournalizer.loadInterCompanyOffsetSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-416">SubledgerJournalizer.loadInterCompanyOffsetSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-417">SubledgerJournalizer.loadIntercompanySubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-417">SubledgerJournalizer.loadIntercompanySubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-418">SubledgerJournalizer.loadRelievingSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-418">SubledgerJournalizer.loadRelievingSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-419">SubledgerJournalizer.loadReversingSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-419">SubledgerJournalizer.loadReversingSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-420">SubledgerJournalizer.loadStandardSubledgerLedgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-420">SubledgerJournalizer.loadStandardSubledgerLedgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-421">SubledgerJournalizer.loadYearEndSubledgerJournalTmpDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-421">SubledgerJournalizer.loadYearEndSubledgerJournalTmpDetail</span></span>|
|<span data-ttu-id="fa00f-422">SubledgerJournalizer.previewSummarizeJournalAccEntryDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-422">SubledgerJournalizer.previewSummarizeJournalAccEntryDetail</span></span>|
|<span data-ttu-id="fa00f-423">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span><span class="sxs-lookup"><span data-stu-id="fa00f-423">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span></span>|
|<span data-ttu-id="fa00f-424">SubledgerJournalizer.recordSubledgerJournalAccountEntries</span><span class="sxs-lookup"><span data-stu-id="fa00f-424">SubledgerJournalizer.recordSubledgerJournalAccountEntries</span></span>|
|<span data-ttu-id="fa00f-425">SubledgerJournalizer.summarizeJournalAccountEntryDetail</span><span class="sxs-lookup"><span data-stu-id="fa00f-425">SubledgerJournalizer.summarizeJournalAccountEntryDetail</span></span>|
|<span data-ttu-id="fa00f-426">TAMTradePromotion.ValidateFundCostLevel</span><span class="sxs-lookup"><span data-stu-id="fa00f-426">TAMTradePromotion.ValidateFundCostLevel</span></span>|
|<span data-ttu-id="fa00f-427">taxBooksection.checkNumberSequenceSetup</span><span class="sxs-lookup"><span data-stu-id="fa00f-427">taxBooksection.checkNumberSequenceSetup</span></span>|
|<span data-ttu-id="fa00f-428">TaxCalculationAdjustment.adjustBaseForTaxIncluded</span><span class="sxs-lookup"><span data-stu-id="fa00f-428">TaxCalculationAdjustment.adjustBaseForTaxIncluded</span></span>|
|<span data-ttu-id="fa00f-429">TaxJournalSpec.parmTaxSpec</span><span class="sxs-lookup"><span data-stu-id="fa00f-429">TaxJournalSpec.parmTaxSpec</span></span>|
|<span data-ttu-id="fa00f-430">TaxProjInvoice.new</span><span class="sxs-lookup"><span data-stu-id="fa00f-430">TaxProjInvoice.new</span></span>|
|<span data-ttu-id="fa00f-431">TaxReport770TransHandler_IT.transferTaxWithholdTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-431">TaxReport770TransHandler_IT.transferTaxWithholdTrans</span></span>|
|<span data-ttu-id="fa00f-432">TaxReport770Validate_IT.validateVendors</span><span class="sxs-lookup"><span data-stu-id="fa00f-432">TaxReport770Validate_IT.validateVendors</span></span>|
|<span data-ttu-id="fa00f-433">TaxSplitPaymentPost_IT.creareReverseTaxTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-433">TaxSplitPaymentPost_IT.creareReverseTaxTrans</span></span>|
|<span data-ttu-id="fa00f-434">TaxWithhold.postTaxWithhold</span><span class="sxs-lookup"><span data-stu-id="fa00f-434">TaxWithhold.postTaxWithhold</span></span>|
|<span data-ttu-id="fa00f-435">TaxWithholdSpecialDP.createTaxWithholdSpecialTmp</span><span class="sxs-lookup"><span data-stu-id="fa00f-435">TaxWithholdSpecialDP.createTaxWithholdSpecialTmp</span></span>|
|<span data-ttu-id="fa00f-436">TmpProjAdjustmentCreate.createFromAdjustment</span><span class="sxs-lookup"><span data-stu-id="fa00f-436">TmpProjAdjustmentCreate.createFromAdjustment</span></span>|
|<span data-ttu-id="fa00f-437">TmpProjAdjustmentCreate.fieldModifiedProjId</span><span class="sxs-lookup"><span data-stu-id="fa00f-437">TmpProjAdjustmentCreate.fieldModifiedProjId</span></span>|
|<span data-ttu-id="fa00f-438">TmpProjAdjustmentCreate.setDimension</span><span class="sxs-lookup"><span data-stu-id="fa00f-438">TmpProjAdjustmentCreate.setDimension</span></span>|
|<span data-ttu-id="fa00f-439">TmpProjAdjustmentCreate.setHourCostPrice</span><span class="sxs-lookup"><span data-stu-id="fa00f-439">TmpProjAdjustmentCreate.setHourCostPrice</span></span>|
|<span data-ttu-id="fa00f-440">TransactionReversal_Asset.reversalBook</span><span class="sxs-lookup"><span data-stu-id="fa00f-440">TransactionReversal_Asset.reversalBook</span></span>|
|<span data-ttu-id="fa00f-441">TransactionReversal_Cust.createAuxiliaryCustTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-441">TransactionReversal_Cust.createAuxiliaryCustTrans</span></span>|
|<span data-ttu-id="fa00f-442">TransactionReversal_Ledger.createGeneralJournal</span><span class="sxs-lookup"><span data-stu-id="fa00f-442">TransactionReversal_Ledger.createGeneralJournal</span></span>|
|<span data-ttu-id="fa00f-443">TrvExpTrans.setTaxGroup</span><span class="sxs-lookup"><span data-stu-id="fa00f-443">TrvExpTrans.setTaxGroup</span></span>|
|<span data-ttu-id="fa00f-444">TSTimesheetEntry.setFocusOnDayIndex</span><span class="sxs-lookup"><span data-stu-id="fa00f-444">TSTimesheetEntry.setFocusOnDayIndex</span></span>|
|<span data-ttu-id="fa00f-445">TsTimesheetFavorites.createTimesheetLines</span><span class="sxs-lookup"><span data-stu-id="fa00f-445">TsTimesheetFavorites.createTimesheetLines</span></span>|
|<span data-ttu-id="fa00f-446">TsTimesheetFavorites.validateWrite</span><span class="sxs-lookup"><span data-stu-id="fa00f-446">TsTimesheetFavorites.validateWrite</span></span>|
|<span data-ttu-id="fa00f-447">TSTimesheetTable.checkHours</span><span class="sxs-lookup"><span data-stu-id="fa00f-447">TSTimesheetTable.checkHours</span></span>|
|<span data-ttu-id="fa00f-448">VendAccountStatementIntDP.insertVendAccountStatementIntTmpRil</span><span class="sxs-lookup"><span data-stu-id="fa00f-448">VendAccountStatementIntDP.insertVendAccountStatementIntTmpRil</span></span>|
|<span data-ttu-id="fa00f-449">VendOutPaymControlController.Insert</span><span class="sxs-lookup"><span data-stu-id="fa00f-449">VendOutPaymControlController.Insert</span></span>|
|<span data-ttu-id="fa00f-450">VendPaymentJournalDP.insertDataFromSpecTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-450">VendPaymentJournalDP.insertDataFromSpecTrans</span></span>|
|<span data-ttu-id="fa00f-451">VendRequestAddVendor.init</span><span class="sxs-lookup"><span data-stu-id="fa00f-451">VendRequestAddVendor.init</span></span>|
|<span data-ttu-id="fa00f-452">WhsContainerization.createNewContainer</span><span class="sxs-lookup"><span data-stu-id="fa00f-452">WhsContainerization.createNewContainer</span></span>|
|<span data-ttu-id="fa00f-453">WHSLoadLine.updateQtyLeftToLoad</span><span class="sxs-lookup"><span data-stu-id="fa00f-453">WHSLoadLine.updateQtyLeftToLoad</span></span>|
|<span data-ttu-id="fa00f-454">WHSLoadTableAssignOriginInfo.assignFromFirstLoadLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-454">WHSLoadTableAssignOriginInfo.assignFromFirstLoadLine</span></span>|
|<span data-ttu-id="fa00f-455">WHSLocationDirective.findPickPutLocation</span><span class="sxs-lookup"><span data-stu-id="fa00f-455">WHSLocationDirective.findPickPutLocation</span></span>|
|<span data-ttu-id="fa00f-456">WhsPostPackingSlip.alterLoadLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-456">WhsPostPackingSlip.alterLoadLine</span></span>|
|<span data-ttu-id="fa00f-457">WHSProdTable.pickBatchQtys</span><span class="sxs-lookup"><span data-stu-id="fa00f-457">WHSProdTable.pickBatchQtys</span></span>|
|<span data-ttu-id="fa00f-458">WhsWorkCreate.checkMaximums</span><span class="sxs-lookup"><span data-stu-id="fa00f-458">WhsWorkCreate.checkMaximums</span></span>|
|<span data-ttu-id="fa00f-459">WHSWorkCreateProdPut.insertProdParmforProdItem</span><span class="sxs-lookup"><span data-stu-id="fa00f-459">WHSWorkCreateProdPut.insertProdParmforProdItem</span></span>|
|<span data-ttu-id="fa00f-460">WhsWorkExecuteDisplay.buildAboveLocationDimensions</span><span class="sxs-lookup"><span data-stu-id="fa00f-460">WhsWorkExecuteDisplay.buildAboveLocationDimensions</span></span>|
|<span data-ttu-id="fa00f-461">WhsWorkExecuteDisplay.buildPick</span><span class="sxs-lookup"><span data-stu-id="fa00f-461">WhsWorkExecuteDisplay.buildPick</span></span>|
|<span data-ttu-id="fa00f-462">WhsWorkExecuteDisplay.getNextFormState</span><span class="sxs-lookup"><span data-stu-id="fa00f-462">WhsWorkExecuteDisplay.getNextFormState</span></span>|
|<span data-ttu-id="fa00f-463">WhsWorkExecuteDisplay.processWorkLine</span><span class="sxs-lookup"><span data-stu-id="fa00f-463">WhsWorkExecuteDisplay.processWorkLine</span></span>|
|<span data-ttu-id="fa00f-464">WHSWorkExecuteDisplayCycleCount.buildCycleCount</span><span class="sxs-lookup"><span data-stu-id="fa00f-464">WHSWorkExecuteDisplayCycleCount.buildCycleCount</span></span>|
|<span data-ttu-id="fa00f-465">WhsWorkExecuteDisplayCycleCount.buildFinish</span><span class="sxs-lookup"><span data-stu-id="fa00f-465">WhsWorkExecuteDisplayCycleCount.buildFinish</span></span>|
|<span data-ttu-id="fa00f-466">WhsWorkExecuteDisplayPOItemReceiving.buildPOReceiving</span><span class="sxs-lookup"><span data-stu-id="fa00f-466">WhsWorkExecuteDisplayPOItemReceiving.buildPOReceiving</span></span>|
|<span data-ttu-id="fa00f-467">WhsWorkExecuteDisplaySpotCycleCounting.displayForm</span><span class="sxs-lookup"><span data-stu-id="fa00f-467">WhsWorkExecuteDisplaySpotCycleCounting.displayForm</span></span>|
|<span data-ttu-id="fa00f-468">WhsWorkExecuteDisplaySystemGrouping.displayNextForm</span><span class="sxs-lookup"><span data-stu-id="fa00f-468">WhsWorkExecuteDisplaySystemGrouping.displayNextForm</span></span>|
|<span data-ttu-id="fa00f-469">WhsWorkExecuteDisplaySystemGrouping.getWorkIdFromFieldName</span><span class="sxs-lookup"><span data-stu-id="fa00f-469">WhsWorkExecuteDisplaySystemGrouping.getWorkIdFromFieldName</span></span>|
|<span data-ttu-id="fa00f-470">WhsWorkExecuteDisplayUserDirected.displayForm</span><span class="sxs-lookup"><span data-stu-id="fa00f-470">WhsWorkExecuteDisplayUserDirected.displayForm</span></span>|
|<span data-ttu-id="fa00f-471">WhsWorkExecuteDisplayUserGrouping.displayForm</span><span class="sxs-lookup"><span data-stu-id="fa00f-471">WhsWorkExecuteDisplayUserGrouping.displayForm</span></span>|
|<span data-ttu-id="fa00f-472">WhsWorkExecuteDisplayValidateUserDirect.displayForm</span><span class="sxs-lookup"><span data-stu-id="fa00f-472">WhsWorkExecuteDisplayValidateUserDirect.displayForm</span></span>|
|<span data-ttu-id="fa00f-473">WhsWorkExecuteDisplayValidateUserDirect.validateUserDirectWorkExists</span><span class="sxs-lookup"><span data-stu-id="fa00f-473">WhsWorkExecuteDisplayValidateUserDirect.validateUserDirectWorkExists</span></span>|
|<span data-ttu-id="fa00f-474">WHSWorkTable.executeWorkLinesInit</span><span class="sxs-lookup"><span data-stu-id="fa00f-474">WHSWorkTable.executeWorkLinesInit</span></span>|
|<span data-ttu-id="fa00f-475">WmsJournalCheckPostReception.returnOrderUpdate</span><span class="sxs-lookup"><span data-stu-id="fa00f-475">WmsJournalCheckPostReception.returnOrderUpdate</span></span>|
|<span data-ttu-id="fa00f-476">WmsPickingList_OrderPickDP.initQueryWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="fa00f-476">WmsPickingList_OrderPickDP.initQueryWMSOrderTrans</span></span>|
|<span data-ttu-id="fa00f-477">WmsPickingList_OrderPickDP.insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="fa00f-477">WmsPickingList_OrderPickDP.insertIntoTempTable</span></span>|
|<span data-ttu-id="fa00f-478">WmsPickingList_OrderPickDP.orderQty</span><span class="sxs-lookup"><span data-stu-id="fa00f-478">WmsPickingList_OrderPickDP.orderQty</span></span>|
|<span data-ttu-id="fa00f-479">WmsPickingList_OrderPickDP.orderUnit</span><span class="sxs-lookup"><span data-stu-id="fa00f-479">WmsPickingList_OrderPickDP.orderUnit</span></span>|
|<span data-ttu-id="fa00f-480">WmsPickingList_OrderPickDP.printDocumentHeader</span><span class="sxs-lookup"><span data-stu-id="fa00f-480">WmsPickingList_OrderPickDP.printDocumentHeader</span></span>|
|<span data-ttu-id="fa00f-481">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span><span class="sxs-lookup"><span data-stu-id="fa00f-481">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span></span>|

## <a name="other-changes"></a><span data-ttu-id="fa00f-482">その他の変更</span><span class="sxs-lookup"><span data-stu-id="fa00f-482">Other changes</span></span>

<span data-ttu-id="fa00f-483">次の追加の変更が、拡張機能に対して行われました。</span><span class="sxs-lookup"><span data-stu-id="fa00f-483">The following additional changes have been made for extensibility.</span></span>

- <span data-ttu-id="fa00f-484">計算済のエイジング バケットの数を増やすためにカスタマイズ機能をサポートする、更新されたエイジングおよび残高リスト クラスおよびフォーム。</span><span class="sxs-lookup"><span data-stu-id="fa00f-484">Updated aging and balance list classes and forms to support the ability for customizations to increase the number of calculated aging buckets.</span></span> 
