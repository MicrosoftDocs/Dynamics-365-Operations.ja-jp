---
title: Dynamics 365 for Finance and Operations バージョン 10.0.2 の拡張機能の変更
description: これのトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.2 に実装された拡張機能を一覧します。
author: FrankDahl
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-05-10
ms.dyn365.ops.version: App 10.0
ms.openlocfilehash: c35dc457d0b06474d43a75610f7c1087e5ca456b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749642"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-1002"></a><span data-ttu-id="23e4e-103">Dynamics 365 for Finance and Operations バージョン 10.0.2 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="23e4e-103">Extensibility changes in Dynamics 365 for Finance and Operations version 10.0.2</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23e4e-104">これのトピックでは、 Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.2 にて実装された拡張機能を記載しています。</span><span class="sxs-lookup"><span data-stu-id="23e4e-104">This topic lists the extensibility features that were implemented in Microsoft Dynamics 365 for Finance and Operations version 10.0.2.</span></span> <span data-ttu-id="23e4e-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23e4e-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="enumerations-made-extensible"></a><span data-ttu-id="23e4e-106">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="23e4e-106">Enumerations made extensible</span></span>

<span data-ttu-id="23e4e-107">今回のアップデートで実装された拡張を以下に記載します。</span><span class="sxs-lookup"><span data-stu-id="23e4e-107">The following enumerations have been made extensible in this update:</span></span>

- <span data-ttu-id="23e4e-108">MarkupModuleType</span><span class="sxs-lookup"><span data-stu-id="23e4e-108">MarkupModuleType</span></span>
- <span data-ttu-id="23e4e-109">MCRCustPaymType</span><span class="sxs-lookup"><span data-stu-id="23e4e-109">MCRCustPaymType</span></span>
- <span data-ttu-id="23e4e-110">PaymSchedBy</span><span class="sxs-lookup"><span data-stu-id="23e4e-110">PaymSchedBy</span></span>

## <a name="sql-operations-made-extensible"></a><span data-ttu-id="23e4e-111">拡張可能になった SQL 操作</span><span class="sxs-lookup"><span data-stu-id="23e4e-111">SQL operations made extensible</span></span>

<span data-ttu-id="23e4e-112">今回のアップデートでは、以下のSQL操作が拡張されました。</span><span class="sxs-lookup"><span data-stu-id="23e4e-112">The following SQL operations have been made extensible in this update:</span></span>

- <span data-ttu-id="23e4e-113">JmgPayAdjustment.payAdjustLoop</span><span class="sxs-lookup"><span data-stu-id="23e4e-113">JmgPayAdjustment.payAdjustLoop</span></span>
- <span data-ttu-id="23e4e-114">ProjPosting.ExtensionHash.New field</span><span class="sxs-lookup"><span data-stu-id="23e4e-114">ProjPosting.ExtensionHash.New field</span></span>
- <span data-ttu-id="23e4e-115">WmsArrivalOverviewGeneration.buildPurch</span><span class="sxs-lookup"><span data-stu-id="23e4e-115">WmsArrivalOverviewGeneration.buildPurch</span></span>
- <span data-ttu-id="23e4e-116">WmsArrivalOverviewGeneration.buildTransferOrder</span><span class="sxs-lookup"><span data-stu-id="23e4e-116">WmsArrivalOverviewGeneration.buildTransferOrder</span></span>

## <a name="metadata-changes"></a><span data-ttu-id="23e4e-117">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="23e4e-117">Metadata changes</span></span>

<span data-ttu-id="23e4e-118">今回のアップデートで以下のメタデータが更新されました。</span><span class="sxs-lookup"><span data-stu-id="23e4e-118">The following metadata changes have been made in this update:</span></span>

- <span data-ttu-id="23e4e-119">CostSheetPercent.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="23e4e-119">CostSheetPercent.NoOfDecimalsIsExtensible</span></span>
- <span data-ttu-id="23e4e-120">WHSCycleCountingWarehouseWorkLineEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="23e4e-120">WHSCycleCountingWarehouseWorkLineEntity.IsPublic</span></span>

## <a name="refactored-methods"></a><span data-ttu-id="23e4e-121">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="23e4e-121">Refactored methods</span></span>

<span data-ttu-id="23e4e-122">拡張性をサポートするために、以下のメソッドがリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="23e4e-122">The following methods have been refactored to support extensibility:</span></span>

- <span data-ttu-id="23e4e-123">/Forms/ProjJournalTable/datasource/ProjJournalTable.initValue</span><span class="sxs-lookup"><span data-stu-id="23e4e-123">/Forms/ProjJournalTable/datasource/ProjJournalTable.initValue</span></span>
- <span data-ttu-id="23e4e-124">/Forms/PurchReqTable.instantiatePurchReqTableForm</span><span class="sxs-lookup"><span data-stu-id="23e4e-124">/Forms/PurchReqTable.instantiatePurchReqTableForm</span></span>
- <span data-ttu-id="23e4e-125">/Forms/PurchReqTable/DataSource/PurchReqTable.init</span><span class="sxs-lookup"><span data-stu-id="23e4e-125">/Forms/PurchReqTable/DataSource/PurchReqTable.init</span></span>
- <span data-ttu-id="23e4e-126">/Forms/SalesQuotationProjLinkWizard/Controls/ProjInvoiceId.lookup</span><span class="sxs-lookup"><span data-stu-id="23e4e-126">/Forms/SalesQuotationProjLinkWizard/Controls/ProjInvoiceId.lookup</span></span>
- <span data-ttu-id="23e4e-127">/Tables/SalesTable.lastQuotation</span><span class="sxs-lookup"><span data-stu-id="23e4e-127">/Tables/SalesTable.lastQuotation</span></span>
- <span data-ttu-id="23e4e-128">AccPolicyProductReceipt.isAccountingRequiredForSourceDocLine</span><span class="sxs-lookup"><span data-stu-id="23e4e-128">AccPolicyProductReceipt.isAccountingRequiredForSourceDocLine</span></span>
- <span data-ttu-id="23e4e-129">AssetFixedAssetEntity.overrideDataSource</span><span class="sxs-lookup"><span data-stu-id="23e4e-129">AssetFixedAssetEntity.overrideDataSource</span></span>
- <span data-ttu-id="23e4e-130">AssetProposalDepreciation.run</span><span class="sxs-lookup"><span data-stu-id="23e4e-130">AssetProposalDepreciation.run</span></span>
- <span data-ttu-id="23e4e-131">AssetTableMethod.init</span><span class="sxs-lookup"><span data-stu-id="23e4e-131">AssetTableMethod.init</span></span>
- <span data-ttu-id="23e4e-132">BankAccountReconcile.validate</span><span class="sxs-lookup"><span data-stu-id="23e4e-132">BankAccountReconcile.validate</span></span>
- <span data-ttu-id="23e4e-133">Class\\BomCalcCost.calcCostModel</span><span class="sxs-lookup"><span data-stu-id="23e4e-133">Class\\BomCalcCost.calcCostModel</span></span>
- <span data-ttu-id="23e4e-134">Class\\MCRLoadContinuityCustInfo.insertLineData</span><span class="sxs-lookup"><span data-stu-id="23e4e-134">Class\\MCRLoadContinuityCustInfo.insertLineData</span></span>
- <span data-ttu-id="23e4e-135">Class\\McrPriceHistoryUpdate.insertNewlyFoundReferences</span><span class="sxs-lookup"><span data-stu-id="23e4e-135">Class\\McrPriceHistoryUpdate.insertNewlyFoundReferences</span></span>
- <span data-ttu-id="23e4e-136">Class\\McrPriceHistoryUpdate.update</span><span class="sxs-lookup"><span data-stu-id="23e4e-136">Class\\McrPriceHistoryUpdate.update</span></span>
- <span data-ttu-id="23e4e-137">Class\\McrPriceHistoryUpdate.updatePriceHistoryLineReferences</span><span class="sxs-lookup"><span data-stu-id="23e4e-137">Class\\McrPriceHistoryUpdate.updatePriceHistoryLineReferences</span></span>
- <span data-ttu-id="23e4e-138">Class\\ProjCopyItemEstimates.copyToItemRequirment</span><span class="sxs-lookup"><span data-stu-id="23e4e-138">Class\\ProjCopyItemEstimates.copyToItemRequirment</span></span>
- <span data-ttu-id="23e4e-139">Class\\PurchAutoCreate\_RFQ.createPurchOrderRFQLineReference</span><span class="sxs-lookup"><span data-stu-id="23e4e-139">Class\\PurchAutoCreate\_RFQ.createPurchOrderRFQLineReference</span></span>
- <span data-ttu-id="23e4e-140">Class\\ReqEventProcessDeleteUnusedKanban.deleteUnusedKanban</span><span class="sxs-lookup"><span data-stu-id="23e4e-140">Class\\ReqEventProcessDeleteUnusedKanban.deleteUnusedKanban</span></span>
- <span data-ttu-id="23e4e-141">Class\\ReqEventProcessDeleteUnusedKanban.run</span><span class="sxs-lookup"><span data-stu-id="23e4e-141">Class\\ReqEventProcessDeleteUnusedKanban.run</span></span>
- <span data-ttu-id="23e4e-142">Class\\ReqTransUpdate.updateLogAddQty</span><span class="sxs-lookup"><span data-stu-id="23e4e-142">Class\\ReqTransUpdate.updateLogAddQty</span></span>
- <span data-ttu-id="23e4e-143">Class\\SalesCancelOrder.run</span><span class="sxs-lookup"><span data-stu-id="23e4e-143">Class\\SalesCancelOrder.run</span></span>
- <span data-ttu-id="23e4e-144">Class\\SalesCreateOrderFromCustomer.main</span><span class="sxs-lookup"><span data-stu-id="23e4e-144">Class\\SalesCreateOrderFromCustomer.main</span></span>
- <span data-ttu-id="23e4e-145">Class\\TAMVendRebateCorrectClaims.rebateAlreadyGiven</span><span class="sxs-lookup"><span data-stu-id="23e4e-145">Class\\TAMVendRebateCorrectClaims.rebateAlreadyGiven</span></span>
- <span data-ttu-id="23e4e-146">Class\\tamVendRebateTableStatusType\_Approved.runPayment</span><span class="sxs-lookup"><span data-stu-id="23e4e-146">Class\\tamVendRebateTableStatusType\_Approved.runPayment</span></span>
- <span data-ttu-id="23e4e-147">Class\\TamVendRebateTableStatusType\_Calculated.inserted</span><span class="sxs-lookup"><span data-stu-id="23e4e-147">Class\\TamVendRebateTableStatusType\_Calculated.inserted</span></span>
- <span data-ttu-id="23e4e-148">Class\\TamVendRebateTableStatusType\_Calculated.runPayment</span><span class="sxs-lookup"><span data-stu-id="23e4e-148">Class\\TamVendRebateTableStatusType\_Calculated.runPayment</span></span>
- <span data-ttu-id="23e4e-149">Classes\\TaxWithhold.createAllTaxWithholdTrans</span><span class="sxs-lookup"><span data-stu-id="23e4e-149">Classes\\TaxWithhold.createAllTaxWithholdTrans</span></span>
- <span data-ttu-id="23e4e-150">Classes\\TaxWithhold.isCalculateTaxWithholdingNeeded\_TH</span><span class="sxs-lookup"><span data-stu-id="23e4e-150">Classes\\TaxWithhold.isCalculateTaxWithholdingNeeded\_TH</span></span>
- <span data-ttu-id="23e4e-151">Classes\\TaxWithhold.postTaxWithhold</span><span class="sxs-lookup"><span data-stu-id="23e4e-151">Classes\\TaxWithhold.postTaxWithhold</span></span>
- <span data-ttu-id="23e4e-152">Classes\\TaxWithhold.totalInvoiceLineAmountSettled\_TH</span><span class="sxs-lookup"><span data-stu-id="23e4e-152">Classes\\TaxWithhold.totalInvoiceLineAmountSettled\_TH</span></span>
- <span data-ttu-id="23e4e-153">CustDirectDebitMandate.setDefaultMandate</span><span class="sxs-lookup"><span data-stu-id="23e4e-153">CustDirectDebitMandate.setDefaultMandate</span></span>
- <span data-ttu-id="23e4e-154">CustDueReportDetailDP.class declaration</span><span class="sxs-lookup"><span data-stu-id="23e4e-154">CustDueReportDetailDP.class declaration</span></span>
- <span data-ttu-id="23e4e-155">CustDueReportDetailDP.insertCustDueReportDetailTmp</span><span class="sxs-lookup"><span data-stu-id="23e4e-155">CustDueReportDetailDP.insertCustDueReportDetailTmp</span></span>
- <span data-ttu-id="23e4e-156">CustQuotationConfirmJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="23e4e-156">CustQuotationConfirmJour.printJournal</span></span>
- <span data-ttu-id="23e4e-157">CustVendCreatePaymJournal.pack</span><span class="sxs-lookup"><span data-stu-id="23e4e-157">CustVendCreatePaymJournal.pack</span></span>
- <span data-ttu-id="23e4e-158">CustVendCreatePaymJournal.parmHasBatchBeenSplit</span><span class="sxs-lookup"><span data-stu-id="23e4e-158">CustVendCreatePaymJournal.parmHasBatchBeenSplit</span></span>
- <span data-ttu-id="23e4e-159">CustVendEditTaxBranch\_TH.init</span><span class="sxs-lookup"><span data-stu-id="23e4e-159">CustVendEditTaxBranch\_TH.init</span></span>
- <span data-ttu-id="23e4e-160">CustVendSumForPaym.run</span><span class="sxs-lookup"><span data-stu-id="23e4e-160">CustVendSumForPaym.run</span></span>
- <span data-ttu-id="23e4e-161">CustVendTransSettlement.post</span><span class="sxs-lookup"><span data-stu-id="23e4e-161">CustVendTransSettlement.post</span></span>
- <span data-ttu-id="23e4e-162">DimDerDistRuleSalesComplInvoice\_BR.createDimAllocForProjRevenue</span><span class="sxs-lookup"><span data-stu-id="23e4e-162">DimDerDistRuleSalesComplInvoice\_BR.createDimAllocForProjRevenue</span></span>
- <span data-ttu-id="23e4e-163">EcoResProductCreateExtended.SetAllowEditField</span><span class="sxs-lookup"><span data-stu-id="23e4e-163">EcoResProductCreateExtended.SetAllowEditField</span></span>
- <span data-ttu-id="23e4e-164">EcoResProductVariantEntity.findDataSource</span><span class="sxs-lookup"><span data-stu-id="23e4e-164">EcoResProductVariantEntity.findDataSource</span></span>
- <span data-ttu-id="23e4e-165">FBSpedFileCreator\_Fiscal\_BR.createRecordC195</span><span class="sxs-lookup"><span data-stu-id="23e4e-165">FBSpedFileCreator\_Fiscal\_BR.createRecordC195</span></span>
- <span data-ttu-id="23e4e-166">Form\\ProdTableCreate.canContinueWithEmptyDim</span><span class="sxs-lookup"><span data-stu-id="23e4e-166">Form\\ProdTableCreate.canContinueWithEmptyDim</span></span>
- <span data-ttu-id="23e4e-167">Form\\PurchCreateFromSalesOrder\\DataSource\\SalesLine.included</span><span class="sxs-lookup"><span data-stu-id="23e4e-167">Form\\PurchCreateFromSalesOrder\\DataSource\\SalesLine.included</span></span>
- <span data-ttu-id="23e4e-168">Form\\PurchCreateFromSalesOrder\\DataSource\\SalesLine.specifyVendAccount</span><span class="sxs-lookup"><span data-stu-id="23e4e-168">Form\\PurchCreateFromSalesOrder\\DataSource\\SalesLine.specifyVendAccount</span></span>
- <span data-ttu-id="23e4e-169">Forms\\TaxWithholdTable.init</span><span class="sxs-lookup"><span data-stu-id="23e4e-169">Forms\\TaxWithholdTable.init</span></span>
- <span data-ttu-id="23e4e-170">FreeTextInvoiceDP.setSysDocuBrandDetails</span><span class="sxs-lookup"><span data-stu-id="23e4e-170">FreeTextInvoiceDP.setSysDocuBrandDetails</span></span>
- <span data-ttu-id="23e4e-171">InventItemOrderSetupMap.checkNotStopped</span><span class="sxs-lookup"><span data-stu-id="23e4e-171">InventItemOrderSetupMap.checkNotStopped</span></span>
- <span data-ttu-id="23e4e-172">InventNonConformanceTable.InventNonConformanceTable.Create</span><span class="sxs-lookup"><span data-stu-id="23e4e-172">InventNonConformanceTable.InventNonConformanceTable.Create</span></span>
- <span data-ttu-id="23e4e-173">InventUpd\_Estimated.updateAutoDimBatchId</span><span class="sxs-lookup"><span data-stu-id="23e4e-173">InventUpd\_Estimated.updateAutoDimBatchId</span></span>
- <span data-ttu-id="23e4e-174">InventUpdateReserveMore.InventUpdateReserveMore</span><span class="sxs-lookup"><span data-stu-id="23e4e-174">InventUpdateReserveMore.InventUpdateReserveMore</span></span>
- <span data-ttu-id="23e4e-175">InventValueReportPopulateItem.updateReportLinePL</span><span class="sxs-lookup"><span data-stu-id="23e4e-175">InventValueReportPopulateItem.updateReportLinePL</span></span>
- <span data-ttu-id="23e4e-176">JmgCalcApproveDateView.viewDate member</span><span class="sxs-lookup"><span data-stu-id="23e4e-176">JmgCalcApproveDateView.viewDate member</span></span>
- <span data-ttu-id="23e4e-177">JmgCalcApproveWeekView.viewDate member</span><span class="sxs-lookup"><span data-stu-id="23e4e-177">JmgCalcApproveWeekView.viewDate member</span></span>
- <span data-ttu-id="23e4e-178">JmgPayAdjustment.payAdjustLoop</span><span class="sxs-lookup"><span data-stu-id="23e4e-178">JmgPayAdjustment.payAdjustLoop</span></span>
- <span data-ttu-id="23e4e-179">LedgerJournalPeriodicCopy.journalTransCopy</span><span class="sxs-lookup"><span data-stu-id="23e4e-179">LedgerJournalPeriodicCopy.journalTransCopy</span></span>
- <span data-ttu-id="23e4e-180">LedgerTransStatementDP.populateTempTableLedgerInStaging</span><span class="sxs-lookup"><span data-stu-id="23e4e-180">LedgerTransStatementDP.populateTempTableLedgerInStaging</span></span>
- <span data-ttu-id="23e4e-181">MCRCustpaym.validateWrite</span><span class="sxs-lookup"><span data-stu-id="23e4e-181">MCRCustpaym.validateWrite</span></span>
- <span data-ttu-id="23e4e-182">MCRFullTextSearch.buildSearchText</span><span class="sxs-lookup"><span data-stu-id="23e4e-182">MCRFullTextSearch.buildSearchText</span></span>
- <span data-ttu-id="23e4e-183">MCRFullTextSearch.truncate</span><span class="sxs-lookup"><span data-stu-id="23e4e-183">MCRFullTextSearch.truncate</span></span>
- <span data-ttu-id="23e4e-184">MCRHoldCodeTrans.insert</span><span class="sxs-lookup"><span data-stu-id="23e4e-184">MCRHoldCodeTrans.insert</span></span>
- <span data-ttu-id="23e4e-185">MCRHoldCodeTrans.setOrderStoppedFlag</span><span class="sxs-lookup"><span data-stu-id="23e4e-185">MCRHoldCodeTrans.setOrderStoppedFlag</span></span>
- <span data-ttu-id="23e4e-186">MCRHoldCodeTrans.unreserve</span><span class="sxs-lookup"><span data-stu-id="23e4e-186">MCRHoldCodeTrans.unreserve</span></span>
- <span data-ttu-id="23e4e-187">McrPriceHistoryForm.calcPotential</span><span class="sxs-lookup"><span data-stu-id="23e4e-187">McrPriceHistoryForm.calcPotential</span></span>
- <span data-ttu-id="23e4e-188">McrPriceHistoryForm.insertPotentialTradeAgreements</span><span class="sxs-lookup"><span data-stu-id="23e4e-188">McrPriceHistoryForm.insertPotentialTradeAgreements</span></span>
- <span data-ttu-id="23e4e-189">PaymTerm.validateWrite</span><span class="sxs-lookup"><span data-stu-id="23e4e-189">PaymTerm.validateWrite</span></span>
- <span data-ttu-id="23e4e-190">PdsRebateAgreement.checkLineBreaks</span><span class="sxs-lookup"><span data-stu-id="23e4e-190">PdsRebateAgreement.checkLineBreaks</span></span>
- <span data-ttu-id="23e4e-191">PdsRebateAgreement.groupChangeCheckValid</span><span class="sxs-lookup"><span data-stu-id="23e4e-191">PdsRebateAgreement.groupChangeCheckValid</span></span>
- <span data-ttu-id="23e4e-192">PdsRebateAgreement.lineAmountHasGapOrOverlap</span><span class="sxs-lookup"><span data-stu-id="23e4e-192">PdsRebateAgreement.lineAmountHasGapOrOverlap</span></span>
- <span data-ttu-id="23e4e-193">PdsRebateAgreement.lineQuantityHasGapOrOverlap</span><span class="sxs-lookup"><span data-stu-id="23e4e-193">PdsRebateAgreement.lineQuantityHasGapOrOverlap</span></span>
- <span data-ttu-id="23e4e-194">PdsRebateAgreementLine.selectRebateAgreementLineMax</span><span class="sxs-lookup"><span data-stu-id="23e4e-194">PdsRebateAgreementLine.selectRebateAgreementLineMax</span></span>
- <span data-ttu-id="23e4e-195">PriceDisc.mcrCalcPostageDisc</span><span class="sxs-lookup"><span data-stu-id="23e4e-195">PriceDisc.mcrCalcPostageDisc</span></span>
- <span data-ttu-id="23e4e-196">PriceDiscLinePolicyRule.retrieveSystemPolicyFieldList</span><span class="sxs-lookup"><span data-stu-id="23e4e-196">PriceDiscLinePolicyRule.retrieveSystemPolicyFieldList</span></span>
- <span data-ttu-id="23e4e-197">ProdUpdCostEstimation.updateSubPurchLine</span><span class="sxs-lookup"><span data-stu-id="23e4e-197">ProdUpdCostEstimation.updateSubPurchLine</span></span>
- <span data-ttu-id="23e4e-198">ProjBudgetManager.createBudgetLineDetail</span><span class="sxs-lookup"><span data-stu-id="23e4e-198">ProjBudgetManager.createBudgetLineDetail</span></span>
- <span data-ttu-id="23e4e-199">ProjBudgetManager.getQuery</span><span class="sxs-lookup"><span data-stu-id="23e4e-199">ProjBudgetManager.getQuery</span></span>
- <span data-ttu-id="23e4e-200">ProjForecastCost.validateWrite</span><span class="sxs-lookup"><span data-stu-id="23e4e-200">ProjForecastCost.validateWrite</span></span>
- <span data-ttu-id="23e4e-201">ProjForecastEmpl.validateWrite</span><span class="sxs-lookup"><span data-stu-id="23e4e-201">ProjForecastEmpl.validateWrite</span></span>
- <span data-ttu-id="23e4e-202">ProjForecastRevenue.validateWrite</span><span class="sxs-lookup"><span data-stu-id="23e4e-202">ProjForecastRevenue.validateWrite</span></span>
- <span data-ttu-id="23e4e-203">ProjLedgerUpdate.insert</span><span class="sxs-lookup"><span data-stu-id="23e4e-203">ProjLedgerUpdate.insert</span></span>
- <span data-ttu-id="23e4e-204">ProjPlanVersionsManager.importHierarchy</span><span class="sxs-lookup"><span data-stu-id="23e4e-204">ProjPlanVersionsManager.importHierarchy</span></span>
- <span data-ttu-id="23e4e-205">ProjPlanVersionsManager.importProjPlanVersionRecords</span><span class="sxs-lookup"><span data-stu-id="23e4e-205">ProjPlanVersionsManager.importProjPlanVersionRecords</span></span>
- <span data-ttu-id="23e4e-206">ProjPost.PostCost</span><span class="sxs-lookup"><span data-stu-id="23e4e-206">ProjPost.PostCost</span></span>
- <span data-ttu-id="23e4e-207">ProjPost.PostCost</span><span class="sxs-lookup"><span data-stu-id="23e4e-207">ProjPost.PostCost</span></span>
- <span data-ttu-id="23e4e-208">ProjWorkBreakdownStructureHelper.addQuotationRelatedRecordsForTask</span><span class="sxs-lookup"><span data-stu-id="23e4e-208">ProjWorkBreakdownStructureHelper.addQuotationRelatedRecordsForTask</span></span>
- <span data-ttu-id="23e4e-209">ProjWorkBreakdownStructureHelper.Addtask</span><span class="sxs-lookup"><span data-stu-id="23e4e-209">ProjWorkBreakdownStructureHelper.Addtask</span></span>
- <span data-ttu-id="23e4e-210">ProjWorkBreakdownStructureHelper.Addtask</span><span class="sxs-lookup"><span data-stu-id="23e4e-210">ProjWorkBreakdownStructureHelper.Addtask</span></span>
- <span data-ttu-id="23e4e-211">ProjWorkBreakdownStructureHelper.Addtask</span><span class="sxs-lookup"><span data-stu-id="23e4e-211">ProjWorkBreakdownStructureHelper.Addtask</span></span>
- <span data-ttu-id="23e4e-212">ProjWorkBreakdownStructureV2FormHelper.IndentTaskV2</span><span class="sxs-lookup"><span data-stu-id="23e4e-212">ProjWorkBreakdownStructureV2FormHelper.IndentTaskV2</span></span>
- <span data-ttu-id="23e4e-213">ProjWorkBreakdownStructureV2FormHelper.MoveTasks</span><span class="sxs-lookup"><span data-stu-id="23e4e-213">ProjWorkBreakdownStructureV2FormHelper.MoveTasks</span></span>
- <span data-ttu-id="23e4e-214">PurchFormletterParmDataInvoice.createParmLinesAndTable</span><span class="sxs-lookup"><span data-stu-id="23e4e-214">PurchFormletterParmDataInvoice.createParmLinesAndTable</span></span>
- <span data-ttu-id="23e4e-215">PurchLine.delete</span><span class="sxs-lookup"><span data-stu-id="23e4e-215">PurchLine.delete</span></span>
- <span data-ttu-id="23e4e-216">PurchLine.distributionUpdateNeeded</span><span class="sxs-lookup"><span data-stu-id="23e4e-216">PurchLine.distributionUpdateNeeded</span></span>
- <span data-ttu-id="23e4e-217">PurchLine.initFromPriceDisc</span><span class="sxs-lookup"><span data-stu-id="23e4e-217">PurchLine.initFromPriceDisc</span></span>
- <span data-ttu-id="23e4e-218">PurchLine.insert</span><span class="sxs-lookup"><span data-stu-id="23e4e-218">PurchLine.insert</span></span>
- <span data-ttu-id="23e4e-219">PurchLine.update</span><span class="sxs-lookup"><span data-stu-id="23e4e-219">PurchLine.update</span></span>
- <span data-ttu-id="23e4e-220">PurchLineType.statusChangeAllowed</span><span class="sxs-lookup"><span data-stu-id="23e4e-220">PurchLineType.statusChangeAllowed</span></span>
- <span data-ttu-id="23e4e-221">ReqEventProcessKanban.newStandard</span><span class="sxs-lookup"><span data-stu-id="23e4e-221">ReqEventProcessKanban.newStandard</span></span>
- <span data-ttu-id="23e4e-222">ReqTransNeutralTracker.trackReqTrans</span><span class="sxs-lookup"><span data-stu-id="23e4e-222">ReqTransNeutralTracker.trackReqTrans</span></span>
- <span data-ttu-id="23e4e-223">ReqTransPoMarkFirm.create</span><span class="sxs-lookup"><span data-stu-id="23e4e-223">ReqTransPoMarkFirm.create</span></span>
- <span data-ttu-id="23e4e-224">小売チャンネル: CartWorkflowHelper.AllowAggregation</span><span class="sxs-lookup"><span data-stu-id="23e4e-224">Retail channel: CartWorkflowHelper.AllowAggregation</span></span>
- <span data-ttu-id="23e4e-225">RetailEcoResProductReleaseManager\_Extension.setAndSaveRetailProductProperties</span><span class="sxs-lookup"><span data-stu-id="23e4e-225">RetailEcoResProductReleaseManager\_Extension.setAndSaveRetailProductProperties</span></span>
- <span data-ttu-id="23e4e-226">RetailMassUpdateUploadDBManager.insertIntoProductProperty</span><span class="sxs-lookup"><span data-stu-id="23e4e-226">RetailMassUpdateUploadDBManager.insertIntoProductProperty</span></span>
- <span data-ttu-id="23e4e-227">RetailPeriodicDiscount.validatePriceGroup</span><span class="sxs-lookup"><span data-stu-id="23e4e-227">RetailPeriodicDiscount.validatePriceGroup</span></span>
- <span data-ttu-id="23e4e-228">RetailTransactionServiceCustomer.newCustomer</span><span class="sxs-lookup"><span data-stu-id="23e4e-228">RetailTransactionServiceCustomer.newCustomer</span></span>
- <span data-ttu-id="23e4e-229">RetailTransactionTransformer.ReadDiscountLines</span><span class="sxs-lookup"><span data-stu-id="23e4e-229">RetailTransactionTransformer.ReadDiscountLines</span></span>
- <span data-ttu-id="23e4e-230">SalesInvoiceDP.setSysDocuBrandDetails</span><span class="sxs-lookup"><span data-stu-id="23e4e-230">SalesInvoiceDP.setSysDocuBrandDetails</span></span>
- <span data-ttu-id="23e4e-231">SalesInvoiceJournalPost.run</span><span class="sxs-lookup"><span data-stu-id="23e4e-231">SalesInvoiceJournalPost.run</span></span>
- <span data-ttu-id="23e4e-232">SalesInvoiceJournalPostBase.run</span><span class="sxs-lookup"><span data-stu-id="23e4e-232">SalesInvoiceJournalPostBase.run</span></span>
- <span data-ttu-id="23e4e-233">SalesLine.CheckItemId</span><span class="sxs-lookup"><span data-stu-id="23e4e-233">SalesLine.CheckItemId</span></span>
- <span data-ttu-id="23e4e-234">Table\\InventTable.purchPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="23e4e-234">Table\\InventTable.purchPriceAgreement</span></span>
- <span data-ttu-id="23e4e-235">Tables\\TaxWithholdTrans.copyTaxWithholdTrans, initFromTaxWithholdTable, insert, validateWrite, amountTotalWHT, existPeriod\_TH</span><span class="sxs-lookup"><span data-stu-id="23e4e-235">Tables\\TaxWithholdTrans.copyTaxWithholdTrans, initFromTaxWithholdTable, insert, validateWrite, amountTotalWHT, existPeriod\_TH</span></span>
- <span data-ttu-id="23e4e-236">TAMVendRebatePaymentPost.main</span><span class="sxs-lookup"><span data-stu-id="23e4e-236">TAMVendRebatePaymentPost.main</span></span>
- <span data-ttu-id="23e4e-237">TAMVendRebateTableProcess.runProcess</span><span class="sxs-lookup"><span data-stu-id="23e4e-237">TAMVendRebateTableProcess.runProcess</span></span>
- <span data-ttu-id="23e4e-238">TrvPostExpenseHeader.postCustVendTransactions</span><span class="sxs-lookup"><span data-stu-id="23e4e-238">TrvPostExpenseHeader.postCustVendTransactions</span></span>
- <span data-ttu-id="23e4e-239">TrvPostExpenseHeader.postCustVendTransactions</span><span class="sxs-lookup"><span data-stu-id="23e4e-239">TrvPostExpenseHeader.postCustVendTransactions</span></span>
- <span data-ttu-id="23e4e-240">WhsControlLicensePlateId.process</span><span class="sxs-lookup"><span data-stu-id="23e4e-240">WhsControlLicensePlateId.process</span></span>
- <span data-ttu-id="23e4e-241">WhsLicensePlateLabelBuild.insertSingleLabelMenuItem</span><span class="sxs-lookup"><span data-stu-id="23e4e-241">WhsLicensePlateLabelBuild.insertSingleLabelMenuItem</span></span>
- <span data-ttu-id="23e4e-242">WhsLicensePlateLabelBuild.insertSingleLabelPrintLine</span><span class="sxs-lookup"><span data-stu-id="23e4e-242">WhsLicensePlateLabelBuild.insertSingleLabelPrintLine</span></span>
- <span data-ttu-id="23e4e-243">WhsrfControlData.processLegacyControl</span><span class="sxs-lookup"><span data-stu-id="23e4e-243">WhsrfControlData.processLegacyControl</span></span>
- <span data-ttu-id="23e4e-244">WhsWorkCreateProdPut.createReportFinishedParameters</span><span class="sxs-lookup"><span data-stu-id="23e4e-244">WhsWorkCreateProdPut.createReportFinishedParameters</span></span>
- <span data-ttu-id="23e4e-245">WhsWorkCreateProdPut.insertProdParmforCoByProduct</span><span class="sxs-lookup"><span data-stu-id="23e4e-245">WhsWorkCreateProdPut.insertProdParmforCoByProduct</span></span>
- <span data-ttu-id="23e4e-246">WhsWorkCreateProdPut.insertProdParmForProdItem</span><span class="sxs-lookup"><span data-stu-id="23e4e-246">WhsWorkCreateProdPut.insertProdParmForProdItem</span></span>
- <span data-ttu-id="23e4e-247">WhsWorkCreateProdPut.setAcceptError</span><span class="sxs-lookup"><span data-stu-id="23e4e-247">WhsWorkCreateProdPut.setAcceptError</span></span>
- <span data-ttu-id="23e4e-248">WHSWorkCreateReplenishment.checkExistingReplenWork</span><span class="sxs-lookup"><span data-stu-id="23e4e-248">WHSWorkCreateReplenishment.checkExistingReplenWork</span></span>
- <span data-ttu-id="23e4e-249">WhsWorkExecuteDisplay.buildPick</span><span class="sxs-lookup"><span data-stu-id="23e4e-249">WhsWorkExecuteDisplay.buildPick</span></span>
- <span data-ttu-id="23e4e-250">whsWorkExecuteDisplayInquiryLocation.buildLocationInquiry</span><span class="sxs-lookup"><span data-stu-id="23e4e-250">whsWorkExecuteDisplayInquiryLocation.buildLocationInquiry</span></span>
- <span data-ttu-id="23e4e-251">WmsArrivalOverviewGeneration.buildInventTransId</span><span class="sxs-lookup"><span data-stu-id="23e4e-251">WmsArrivalOverviewGeneration.buildInventTransId</span></span>
- <span data-ttu-id="23e4e-252">WmsOrderTransType\_OutputDontPostTransfer.decreaseQty</span><span class="sxs-lookup"><span data-stu-id="23e4e-252">WmsOrderTransType\_OutputDontPostTransfer.decreaseQty</span></span>
- <span data-ttu-id="23e4e-253">WmsOrderTransType\_OutputDontPostTransfer.increaseQtyOverdelivery</span><span class="sxs-lookup"><span data-stu-id="23e4e-253">WmsOrderTransType\_OutputDontPostTransfer.increaseQtyOverdelivery</span></span>

## <a name="other-extensibility-enhancements"></a><span data-ttu-id="23e4e-254">その他の拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="23e4e-254">Other extensibility enhancements</span></span>

- <span data-ttu-id="23e4e-255">Classes\\BankPositivePayExport の accessmodifier が private から protected に変更されました。</span><span class="sxs-lookup"><span data-stu-id="23e4e-255">The accessModifier of Classes\\BankPositivePayExport.Class changed from private to protected.</span></span>
- <span data-ttu-id="23e4e-256">InventItemOrderSetupMap が拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="23e4e-256">The InventItemOrderSetupMap map was made extensible.</span></span>
- <span data-ttu-id="23e4e-257">**小売チャンネル:** RetailTransactionViewのカスタムカラム。</span><span class="sxs-lookup"><span data-stu-id="23e4e-257">**Retail channel:** Custom columns in RetailTransactionView.</span></span>
- <span data-ttu-id="23e4e-258">**小売チャンネル:** :サインイン要求の無効化ができます。</span><span class="sxs-lookup"><span data-stu-id="23e4e-258">**Retail channel:** The sign-in request can be overridden.</span></span>
- <span data-ttu-id="23e4e-259">**小売チャンネル:** 出荷ビュー拡張コントローラクラス。</span><span class="sxs-lookup"><span data-stu-id="23e4e-259">**Retail channel:** Shipping view extension controller class.</span></span>
- <span data-ttu-id="23e4e-260">**小売チャンネル:** AddressAddEditView の [App Bar] ボタンの実装。</span><span class="sxs-lookup"><span data-stu-id="23e4e-260">**Retail channel:** Support for the AppBar button in AddressAddEditView.</span></span>
- <span data-ttu-id="23e4e-261">**小売チャンネル:** ダイアログボックスで銀行預金額キーの無効化に対応。</span><span class="sxs-lookup"><span data-stu-id="23e4e-261">**Retail channel:** Support for overriding the Bank deposit amount key in the dialog box.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]