---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 08/27/2018
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
ms.search.validFrom: 2018-08-31
ms.dyn365.ops.version: App 8.0.4
ms.openlocfilehash: 662796b34ee05bf72b4198bb976ea275c3d554a7
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833448"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-804"></a><span data-ttu-id="eb8a2-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="eb8a2-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.4</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb8a2-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.4.</span></span> <span data-ttu-id="eb8a2-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="eb8a2-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="eb8a2-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="eb8a2-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="eb8a2-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="eb8a2-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="eb8a2-109">AgreementHeader.getModuleType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-109">AgreementHeader.getModuleType</span></span>|
|<span data-ttu-id="eb8a2-110">AssetSplit.construct</span><span class="sxs-lookup"><span data-stu-id="eb8a2-110">AssetSplit.construct</span></span>|
|<span data-ttu-id="eb8a2-111">BankDepositSlipController.main</span><span class="sxs-lookup"><span data-stu-id="eb8a2-111">BankDepositSlipController.main</span></span>|
|<span data-ttu-id="eb8a2-112">BankPositivePayExport.sendFileToUser</span><span class="sxs-lookup"><span data-stu-id="eb8a2-112">BankPositivePayExport.sendFileToUser</span></span>|
|<span data-ttu-id="eb8a2-113">CaseDetailForm.getRecordsFromDataSource</span><span class="sxs-lookup"><span data-stu-id="eb8a2-113">CaseDetailForm.getRecordsFromDataSource</span></span>|
|<span data-ttu-id="eb8a2-114">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span><span class="sxs-lookup"><span data-stu-id="eb8a2-114">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span></span>|
|<span data-ttu-id="eb8a2-115">CostSheetNodeCalculation.validate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-115">CostSheetNodeCalculation.validate</span></span>|
|<span data-ttu-id="eb8a2-116">CostSheetNodeCalculationRate.calcLowestLevel</span><span class="sxs-lookup"><span data-stu-id="eb8a2-116">CostSheetNodeCalculationRate.calcLowestLevel</span></span>|
|<span data-ttu-id="eb8a2-117">CostSheetNodeCalculationSurcharge.equal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-117">CostSheetNodeCalculationSurcharge.equal</span></span>|
|<span data-ttu-id="eb8a2-118">CustAccountStatementExtController.processParty</span><span class="sxs-lookup"><span data-stu-id="eb8a2-118">CustAccountStatementExtController.processParty</span></span>|
|<span data-ttu-id="eb8a2-119">CustAccountStatementExtDP.insertNewRecords</span><span class="sxs-lookup"><span data-stu-id="eb8a2-119">CustAccountStatementExtDP.insertNewRecords</span></span>|
|<span data-ttu-id="eb8a2-120">CustAccountStatementExtDP.setSysDocuBrandDetails</span><span class="sxs-lookup"><span data-stu-id="eb8a2-120">CustAccountStatementExtDP.setSysDocuBrandDetails</span></span>|
|<span data-ttu-id="eb8a2-121">CustBillOfExchangePost.postNextStep</span><span class="sxs-lookup"><span data-stu-id="eb8a2-121">CustBillOfExchangePost.postNextStep</span></span>|
|<span data-ttu-id="eb8a2-122">CustBillOfExchangePostProtestHonored.postNextStep</span><span class="sxs-lookup"><span data-stu-id="eb8a2-122">CustBillOfExchangePostProtestHonored.postNextStep</span></span>|
|<span data-ttu-id="eb8a2-123">CustCollectionJourController.runPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="eb8a2-123">CustCollectionJourController.runPrintMgmt</span></span>|
|<span data-ttu-id="eb8a2-124">CustCollectionLetterCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-124">CustCollectionLetterCreate.createJournal</span></span>|
|<span data-ttu-id="eb8a2-125">CustCollectionLetterCreate.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-125">CustCollectionLetterCreate.run</span></span>|
|<span data-ttu-id="eb8a2-126">CustCollectionLetterNote.CustCollectionLetterJour.active</span><span class="sxs-lookup"><span data-stu-id="eb8a2-126">CustCollectionLetterNote.CustCollectionLetterJour.active</span></span>|
|<span data-ttu-id="eb8a2-127">CustCollectionLetterPost.processRow</span><span class="sxs-lookup"><span data-stu-id="eb8a2-127">CustCollectionLetterPost.processRow</span></span>|
|<span data-ttu-id="eb8a2-128">CustCollectionLetterPost.validateCollectionLetter</span><span class="sxs-lookup"><span data-stu-id="eb8a2-128">CustCollectionLetterPost.validateCollectionLetter</span></span>|
|<span data-ttu-id="eb8a2-129">CustFreeInvoiceCorrection.createInvoiceLines</span><span class="sxs-lookup"><span data-stu-id="eb8a2-129">CustFreeInvoiceCorrection.createInvoiceLines</span></span>|
|<span data-ttu-id="eb8a2-130">CustInterestPost.main</span><span class="sxs-lookup"><span data-stu-id="eb8a2-130">CustInterestPost.main</span></span>|
|<span data-ttu-id="eb8a2-131">CustInterestPost.validateInterestTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-131">CustInterestPost.validateInterestTrans</span></span>|
|<span data-ttu-id="eb8a2-132">CustInvoiceJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-132">CustInvoiceJour.printJournal</span></span>|
|<span data-ttu-id="eb8a2-133">CustInvoiceTable.calcDue</span><span class="sxs-lookup"><span data-stu-id="eb8a2-133">CustInvoiceTable.calcDue</span></span>|
|<span data-ttu-id="eb8a2-134">CustOpenBalanceCurrency.Data Sources – VendTrans – init</span><span class="sxs-lookup"><span data-stu-id="eb8a2-134">CustOpenBalanceCurrency.Data Sources – VendTrans – init</span></span>|
|<span data-ttu-id="eb8a2-135">CustOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-135">CustOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="eb8a2-136">CustPackingSlipJourFormHelper.areCancelCorrectButtonsEnabled</span><span class="sxs-lookup"><span data-stu-id="eb8a2-136">CustPackingSlipJourFormHelper.areCancelCorrectButtonsEnabled</span></span>|
|<span data-ttu-id="eb8a2-137">CustPaymEntry.editIsMarkedForSettlement</span><span class="sxs-lookup"><span data-stu-id="eb8a2-137">CustPaymEntry.editIsMarkedForSettlement</span></span>|
|<span data-ttu-id="eb8a2-138">CustPostInvoice.main</span><span class="sxs-lookup"><span data-stu-id="eb8a2-138">CustPostInvoice.main</span></span>|
|<span data-ttu-id="eb8a2-139">CustPostInvoice.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-139">CustPostInvoice.run</span></span>|
|<span data-ttu-id="eb8a2-140">CustPostInvoice.validate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-140">CustPostInvoice.validate</span></span>|
|<span data-ttu-id="eb8a2-141">CustPostInvoiceJob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-141">CustPostInvoiceJob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="eb8a2-142">CustPostInvoiceJob.initializeCustPostProcess</span><span class="sxs-lookup"><span data-stu-id="eb8a2-142">CustPostInvoiceJob.initializeCustPostProcess</span></span>|
|<span data-ttu-id="eb8a2-143">CustPostInvoiceJob.main</span><span class="sxs-lookup"><span data-stu-id="eb8a2-143">CustPostInvoiceJob.main</span></span>|
|<span data-ttu-id="eb8a2-144">CustPostInvoiceJob.processCustPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-144">CustPostInvoiceJob.processCustPostInvoiceUpdate</span></span>|
|<span data-ttu-id="eb8a2-145">CustProvisionalBalanceDP.calculateAmounts</span><span class="sxs-lookup"><span data-stu-id="eb8a2-145">CustProvisionalBalanceDP.calculateAmounts</span></span>|
|<span data-ttu-id="eb8a2-146">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="eb8a2-146">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="eb8a2-147">CustProvisionalBalanceDP.populateCustProvisionalBalanceTmpProcessing</span><span class="sxs-lookup"><span data-stu-id="eb8a2-147">CustProvisionalBalanceDP.populateCustProvisionalBalanceTmpProcessing</span></span>|
|<span data-ttu-id="eb8a2-148">CustProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="eb8a2-148">CustProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="eb8a2-149">CustProvisionalBalanceDP.translateMainAccountNamesOnCustProvisionalBalanceTmpProcessing</span><span class="sxs-lookup"><span data-stu-id="eb8a2-149">CustProvisionalBalanceDP.translateMainAccountNamesOnCustProvisionalBalanceTmpProcessing</span></span>|
|<span data-ttu-id="eb8a2-150">CustQuotationJournal.launchReport</span><span class="sxs-lookup"><span data-stu-id="eb8a2-150">CustQuotationJournal.launchReport</span></span>|
|<span data-ttu-id="eb8a2-151">CustSettlementPriorityProcessing .createTempData</span><span class="sxs-lookup"><span data-stu-id="eb8a2-151">CustSettlementPriorityProcessing .createTempData</span></span>|
|<span data-ttu-id="eb8a2-152">CustSettlementPriorityProcessing .setPaymentAmount</span><span class="sxs-lookup"><span data-stu-id="eb8a2-152">CustSettlementPriorityProcessing .setPaymentAmount</span></span>|
|<span data-ttu-id="eb8a2-153">CustSettlementPriorityProcessing .updatePartialTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-153">CustSettlementPriorityProcessing .updatePartialTrans</span></span>|
|<span data-ttu-id="eb8a2-154">CustSettlementPriorityProcessing.classDeclaration</span><span class="sxs-lookup"><span data-stu-id="eb8a2-154">CustSettlementPriorityProcessing.classDeclaration</span></span>|
|<span data-ttu-id="eb8a2-155">CustSettlementPriorityProcessing.constructCustOpenTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-155">CustSettlementPriorityProcessing.constructCustOpenTrans</span></span>|
|<span data-ttu-id="eb8a2-156">CustSettlementPriorityProcessing.constructCustPaymEntry</span><span class="sxs-lookup"><span data-stu-id="eb8a2-156">CustSettlementPriorityProcessing.constructCustPaymEntry</span></span>|
|<span data-ttu-id="eb8a2-157">CustSettlementPriorityProcessing.constructOffsetVoucherCust</span><span class="sxs-lookup"><span data-stu-id="eb8a2-157">CustSettlementPriorityProcessing.constructOffsetVoucherCust</span></span>|
|<span data-ttu-id="eb8a2-158">CustSettlementPriorityProcessing.getBillingPriorities</span><span class="sxs-lookup"><span data-stu-id="eb8a2-158">CustSettlementPriorityProcessing.getBillingPriorities</span></span>|
|<span data-ttu-id="eb8a2-159">CustSettlementPriorityProcessing.getSettlementQuery</span><span class="sxs-lookup"><span data-stu-id="eb8a2-159">CustSettlementPriorityProcessing.getSettlementQuery</span></span>|
|<span data-ttu-id="eb8a2-160">CustSettlementPriorityProcessing.initCustTransOpen</span><span class="sxs-lookup"><span data-stu-id="eb8a2-160">CustSettlementPriorityProcessing.initCustTransOpen</span></span>|
|<span data-ttu-id="eb8a2-161">CustSettlementPriorityProcessing.insertAllLinesAccrossInvoices</span><span class="sxs-lookup"><span data-stu-id="eb8a2-161">CustSettlementPriorityProcessing.insertAllLinesAccrossInvoices</span></span>|
|<span data-ttu-id="eb8a2-162">CustSettlementPriorityProcessing.markTransactions</span><span class="sxs-lookup"><span data-stu-id="eb8a2-162">CustSettlementPriorityProcessing.markTransactions</span></span>|
|<span data-ttu-id="eb8a2-163">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span><span class="sxs-lookup"><span data-stu-id="eb8a2-163">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span></span>|
|<span data-ttu-id="eb8a2-164">CustSettlementPriorityProcessing.validateMarkedTransactionOpenTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-164">CustSettlementPriorityProcessing.validateMarkedTransactionOpenTrans</span></span>|
|<span data-ttu-id="eb8a2-165">CustStatisticsUS - メソッド calcStatistics</span><span class="sxs-lookup"><span data-stu-id="eb8a2-165">CustStatisticsUS - method calcStatistics</span></span>|
|<span data-ttu-id="eb8a2-166">CustTable.validateCNPJCPF_BR</span><span class="sxs-lookup"><span data-stu-id="eb8a2-166">CustTable.validateCNPJCPF_BR</span></span>|
|<span data-ttu-id="eb8a2-167">CustTrans.checkReversal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-167">CustTrans.checkReversal</span></span>|
|<span data-ttu-id="eb8a2-168">CustVendCheque.processChequeNum</span><span class="sxs-lookup"><span data-stu-id="eb8a2-168">CustVendCheque.processChequeNum</span></span>|
|<span data-ttu-id="eb8a2-169">CustVendCreatePaymJournal_Vend.searchTransactions</span><span class="sxs-lookup"><span data-stu-id="eb8a2-169">CustVendCreatePaymJournal_Vend.searchTransactions</span></span>|
|<span data-ttu-id="eb8a2-170">CustVendExchAdjPostingEngine.addExchangeAdjustment</span><span class="sxs-lookup"><span data-stu-id="eb8a2-170">CustVendExchAdjPostingEngine.addExchangeAdjustment</span></span>|
|<span data-ttu-id="eb8a2-171">CustVendFindSettlements.getTmpTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-171">CustVendFindSettlements.getTmpTrans</span></span>|
|<span data-ttu-id="eb8a2-172">CustVendPaymProposalTransferToJournal.transferProposalLineToJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-172">CustVendPaymProposalTransferToJournal.transferProposalLineToJournal</span></span>|
|<span data-ttu-id="eb8a2-173">CustVendSettle.createSummaryAccountReliefTransactions</span><span class="sxs-lookup"><span data-stu-id="eb8a2-173">CustVendSettle.createSummaryAccountReliefTransactions</span></span>|
|<span data-ttu-id="eb8a2-174">CustVendSettle.mustOffsetOriginalSummaryDistributions</span><span class="sxs-lookup"><span data-stu-id="eb8a2-174">CustVendSettle.mustOffsetOriginalSummaryDistributions</span></span>|
|<span data-ttu-id="eb8a2-175">CustVendSettle.postingProfileSettle_CreateDistributions</span><span class="sxs-lookup"><span data-stu-id="eb8a2-175">CustVendSettle.postingProfileSettle_CreateDistributions</span></span>|
|<span data-ttu-id="eb8a2-176">CustVendSettle.settleNow</span><span class="sxs-lookup"><span data-stu-id="eb8a2-176">CustVendSettle.settleNow</span></span>|
|<span data-ttu-id="eb8a2-177">CustVendTransDistributionController.getDistributionFactorsForPostingTypes</span><span class="sxs-lookup"><span data-stu-id="eb8a2-177">CustVendTransDistributionController.getDistributionFactorsForPostingTypes</span></span>|
|<span data-ttu-id="eb8a2-178">CustVendTransExchAdjDistController.getDistributionFactorsForPostingTypes</span><span class="sxs-lookup"><span data-stu-id="eb8a2-178">CustVendTransExchAdjDistController.getDistributionFactorsForPostingTypes</span></span>|
|<span data-ttu-id="eb8a2-179">CustVendTransSettle.post</span><span class="sxs-lookup"><span data-stu-id="eb8a2-179">CustVendTransSettle.post</span></span>|
|<span data-ttu-id="eb8a2-180">CustVendVoucher.initLedgerPosting</span><span class="sxs-lookup"><span data-stu-id="eb8a2-180">CustVendVoucher.initLedgerPosting</span></span>|
|<span data-ttu-id="eb8a2-181">CustWriteOff.createInterestWriteOffJournalForInterestTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-181">CustWriteOff.createInterestWriteOffJournalForInterestTrans</span></span>|
|<span data-ttu-id="eb8a2-182">DataFileImportExportUtils.readStreamWriterAndWriteToStreamWriter</span><span class="sxs-lookup"><span data-stu-id="eb8a2-182">DataFileImportExportUtils.readStreamWriterAndWriteToStreamWriter</span></span>|
|<span data-ttu-id="eb8a2-183">EcoResProductCreate.initDefaultControlValues</span><span class="sxs-lookup"><span data-stu-id="eb8a2-183">EcoResProductCreate.initDefaultControlValues</span></span>|
|<span data-ttu-id="eb8a2-184">EcoResProductReleaseManager.releaseToLegalEntity</span><span class="sxs-lookup"><span data-stu-id="eb8a2-184">EcoResProductReleaseManager.releaseToLegalEntity</span></span>|
|<span data-ttu-id="eb8a2-185">ExchangeRateImportOperation.saveRates</span><span class="sxs-lookup"><span data-stu-id="eb8a2-185">ExchangeRateImportOperation.saveRates</span></span>|
|<span data-ttu-id="eb8a2-186">FormletterJournalCreate.newPurchJournalCreate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-186">FormletterJournalCreate.newPurchJournalCreate</span></span>|
|<span data-ttu-id="eb8a2-187">FulfillmentLineView.NewExtension</span><span class="sxs-lookup"><span data-stu-id="eb8a2-187">FulfillmentLineView.NewExtension</span></span>|
|<span data-ttu-id="eb8a2-188">InterCompanyPost.formLetterCollect</span><span class="sxs-lookup"><span data-stu-id="eb8a2-188">InterCompanyPost.formLetterCollect</span></span>|
|<span data-ttu-id="eb8a2-189">InventCostIndirectFinancial.remainingQty</span><span class="sxs-lookup"><span data-stu-id="eb8a2-189">InventCostIndirectFinancial.remainingQty</span></span>|
|<span data-ttu-id="eb8a2-190">InventCostItemDim.load</span><span class="sxs-lookup"><span data-stu-id="eb8a2-190">InventCostItemDim.load</span></span>|
|<span data-ttu-id="eb8a2-191">InventCostJournalIndirectCost > addTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-191">InventCostJournalIndirectCost > addTrans</span></span>|
|<span data-ttu-id="eb8a2-192">InventCostTrans.setRefTypeFromInventTransType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-192">InventCostTrans.setRefTypeFromInventTransType</span></span>|
|<span data-ttu-id="eb8a2-193">InventDimCtrl_Rep_Sales.initDimParmFormletter</span><span class="sxs-lookup"><span data-stu-id="eb8a2-193">InventDimCtrl_Rep_Sales.initDimParmFormletter</span></span>|
|<span data-ttu-id="eb8a2-194">InventDimCtrl_Rep_Sales.mustShowField</span><span class="sxs-lookup"><span data-stu-id="eb8a2-194">InventDimCtrl_Rep_Sales.mustShowField</span></span>|
|<span data-ttu-id="eb8a2-195">InventDimCtrl_Rep_Sales.reportStrItemId</span><span class="sxs-lookup"><span data-stu-id="eb8a2-195">InventDimCtrl_Rep_Sales.reportStrItemId</span></span>|
|<span data-ttu-id="eb8a2-196">InventDistinctProductOrderDefaultingController.construct</span><span class="sxs-lookup"><span data-stu-id="eb8a2-196">InventDistinctProductOrderDefaultingController.construct</span></span>|
|<span data-ttu-id="eb8a2-197">InventItemLocationCountingStatus.updateStopCountingJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-197">InventItemLocationCountingStatus.updateStopCountingJournal</span></span>|
|<span data-ttu-id="eb8a2-198">InventItemPriceActivationJob.activateCostSheetCalculationFactor</span><span class="sxs-lookup"><span data-stu-id="eb8a2-198">InventItemPriceActivationJob.activateCostSheetCalculationFactor</span></span>|
|<span data-ttu-id="eb8a2-199">InventJournalCheckPost_Movement.postTransLedgerMovement</span><span class="sxs-lookup"><span data-stu-id="eb8a2-199">InventJournalCheckPost_Movement.postTransLedgerMovement</span></span>|
|<span data-ttu-id="eb8a2-200">InventJournalFormTrans_Movement.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="eb8a2-200">InventJournalFormTrans_Movement.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="eb8a2-201">InventoryMainAccDimensionListProvider.ledgerPostingType2InventAccountType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-201">InventoryMainAccDimensionListProvider.ledgerPostingType2InventAccountType</span></span>|
|<span data-ttu-id="eb8a2-202">InventQualityOrderTable.setTestResult</span><span class="sxs-lookup"><span data-stu-id="eb8a2-202">InventQualityOrderTable.setTestResult</span></span>|
|<span data-ttu-id="eb8a2-203">InventSerial.init</span><span class="sxs-lookup"><span data-stu-id="eb8a2-203">InventSerial.init</span></span>|
|<span data-ttu-id="eb8a2-204">InventSumPhysicalSpec.setValueQty</span><span class="sxs-lookup"><span data-stu-id="eb8a2-204">InventSumPhysicalSpec.setValueQty</span></span>|
|<span data-ttu-id="eb8a2-205">InventTable.insertInventItemOrderSetup</span><span class="sxs-lookup"><span data-stu-id="eb8a2-205">InventTable.insertInventItemOrderSetup</span></span>|
|<span data-ttu-id="eb8a2-206">InventTrans.updateSumUp</span><span class="sxs-lookup"><span data-stu-id="eb8a2-206">InventTrans.updateSumUp</span></span>|
|<span data-ttu-id="eb8a2-207">InventTransferLine.updates</span><span class="sxs-lookup"><span data-stu-id="eb8a2-207">InventTransferLine.updates</span></span>|
|<span data-ttu-id="eb8a2-208">InventTransferUpd.beginLedger</span><span class="sxs-lookup"><span data-stu-id="eb8a2-208">InventTransferUpd.beginLedger</span></span>|
|<span data-ttu-id="eb8a2-209">InventTransIdSum.update</span><span class="sxs-lookup"><span data-stu-id="eb8a2-209">InventTransIdSum.update</span></span>|
|<span data-ttu-id="eb8a2-210">InventUpd_Estimated.updateFieldsChange</span><span class="sxs-lookup"><span data-stu-id="eb8a2-210">InventUpd_Estimated.updateFieldsChange</span></span>|
|<span data-ttu-id="eb8a2-211">InventUpd_Financial.updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="eb8a2-211">InventUpd_Financial.updateFinancialIssue</span></span>|
|<span data-ttu-id="eb8a2-212">InventUpd_Financial.updateNow</span><span class="sxs-lookup"><span data-stu-id="eb8a2-212">InventUpd_Financial.updateNow</span></span>|
|<span data-ttu-id="eb8a2-213">InventUpd_Physical.updatePhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="eb8a2-213">InventUpd_Physical.updatePhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="eb8a2-214">InventUpd_Registered.pickReleatedIssueTransMore</span><span class="sxs-lookup"><span data-stu-id="eb8a2-214">InventUpd_Registered.pickReleatedIssueTransMore</span></span>|
|<span data-ttu-id="eb8a2-215">InventUpd_Reservation.updateReserveMore</span><span class="sxs-lookup"><span data-stu-id="eb8a2-215">InventUpd_Reservation.updateReserveMore</span></span>|
|<span data-ttu-id="eb8a2-216">InventUpdateMarking.updateReservations</span><span class="sxs-lookup"><span data-stu-id="eb8a2-216">InventUpdateMarking.updateReservations</span></span>|
|<span data-ttu-id="eb8a2-217">JmgAbsenceCalendar</span><span class="sxs-lookup"><span data-stu-id="eb8a2-217">JmgAbsenceCalendar</span></span>|
|<span data-ttu-id="eb8a2-218">JmgMESSwitchCode.init</span><span class="sxs-lookup"><span data-stu-id="eb8a2-218">JmgMESSwitchCode.init</span></span>|
|<span data-ttu-id="eb8a2-219">LedgerExchAdj.postAdjustment</span><span class="sxs-lookup"><span data-stu-id="eb8a2-219">LedgerExchAdj.postAdjustment</span></span>|
|<span data-ttu-id="eb8a2-220">LedgerExchAdj.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-220">LedgerExchAdj.run</span></span>|
|<span data-ttu-id="eb8a2-221">LedgerJournalEngine.initTaxGroup</span><span class="sxs-lookup"><span data-stu-id="eb8a2-221">LedgerJournalEngine.initTaxGroup</span></span>|
|<span data-ttu-id="eb8a2-222">LedgerJournalEngine_CustBillSettle.initCustOffsetAccount</span><span class="sxs-lookup"><span data-stu-id="eb8a2-222">LedgerJournalEngine_CustBillSettle.initCustOffsetAccount</span></span>|
|<span data-ttu-id="eb8a2-223">LedgerJournalTransCustPaym.LedgerJournalTrans.CustVendBankAccountId.jumpRef</span><span class="sxs-lookup"><span data-stu-id="eb8a2-223">LedgerJournalTransCustPaym.LedgerJournalTrans.CustVendBankAccountId.jumpRef</span></span>|
|<span data-ttu-id="eb8a2-224">LedgerJournalTransUpdateCust</span><span class="sxs-lookup"><span data-stu-id="eb8a2-224">LedgerJournalTransUpdateCust</span></span>|
|<span data-ttu-id="eb8a2-225">LedgerJournalTransUpdateLedger.updateNow</span><span class="sxs-lookup"><span data-stu-id="eb8a2-225">LedgerJournalTransUpdateLedger.updateNow</span></span>|
|<span data-ttu-id="eb8a2-226">LogisticsPostalAddress.whsAddressFormatValidation</span><span class="sxs-lookup"><span data-stu-id="eb8a2-226">LogisticsPostalAddress.whsAddressFormatValidation</span></span>|
|<span data-ttu-id="eb8a2-227">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span><span class="sxs-lookup"><span data-stu-id="eb8a2-227">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span></span>|
|<span data-ttu-id="eb8a2-228">Markup.calc</span><span class="sxs-lookup"><span data-stu-id="eb8a2-228">Markup.calc</span></span>|
|<span data-ttu-id="eb8a2-229">MCRCustPaym.ValidateWrite</span><span class="sxs-lookup"><span data-stu-id="eb8a2-229">MCRCustPaym.ValidateWrite</span></span>|
|<span data-ttu-id="eb8a2-230">McrCustPaymTotals_Sales.allPaymentsSubmitted</span><span class="sxs-lookup"><span data-stu-id="eb8a2-230">McrCustPaymTotals_Sales.allPaymentsSubmitted</span></span>|
|<span data-ttu-id="eb8a2-231">OffsetVoucher.updateNow</span><span class="sxs-lookup"><span data-stu-id="eb8a2-231">OffsetVoucher.updateNow</span></span>|
|<span data-ttu-id="eb8a2-232">PmfCoByProdCalcTrans.updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="eb8a2-232">PmfCoByProdCalcTrans.updateRealCalcIndirect</span></span>|
|<span data-ttu-id="eb8a2-233">PmfCoByProdCalcTrans.updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="eb8a2-233">PmfCoByProdCalcTrans.updateRealCalcIndirect</span></span>|
|<span data-ttu-id="eb8a2-234">POSAPIdts.New トリガー</span><span class="sxs-lookup"><span data-stu-id="eb8a2-234">POSAPIdts.New Trigger</span></span>|
|<span data-ttu-id="eb8a2-235">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span><span class="sxs-lookup"><span data-stu-id="eb8a2-235">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span></span>|
|<span data-ttu-id="eb8a2-236">PriceDiscAdmTrans.canEditPriceDiscValueField</span><span class="sxs-lookup"><span data-stu-id="eb8a2-236">PriceDiscAdmTrans.canEditPriceDiscValueField</span></span>|
|<span data-ttu-id="eb8a2-237">ProcCategoryHierarchyManagement.init</span><span class="sxs-lookup"><span data-stu-id="eb8a2-237">ProcCategoryHierarchyManagement.init</span></span>|
|<span data-ttu-id="eb8a2-238">ProdCalcTrans > メソッド updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="eb8a2-238">ProdCalcTrans > method updateRealCalcIndirect</span></span>|
|<span data-ttu-id="eb8a2-239">ProdIndirectTrans > メソッド type2ItemCalcType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-239">ProdIndirectTrans > method type2ItemCalcType</span></span>|
|<span data-ttu-id="eb8a2-240">ProdJournalCheckPostProd.postTransLedger</span><span class="sxs-lookup"><span data-stu-id="eb8a2-240">ProdJournalCheckPostProd.postTransLedger</span></span>|
|<span data-ttu-id="eb8a2-241">ProdTableForm.handleProdTableCreatePreSuper</span><span class="sxs-lookup"><span data-stu-id="eb8a2-241">ProdTableForm.handleProdTableCreatePreSuper</span></span>|
|<span data-ttu-id="eb8a2-242">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="eb8a2-242">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="eb8a2-243">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="eb8a2-243">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="eb8a2-244">ProjAdjustmentUpdate.deleteJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-244">ProjAdjustmentUpdate.deleteJournal</span></span>|
|<span data-ttu-id="eb8a2-245">ProjFundingLimitTrackingManager.updateUsingSourceDocument</span><span class="sxs-lookup"><span data-stu-id="eb8a2-245">ProjFundingLimitTrackingManager.updateUsingSourceDocument</span></span>|
|<span data-ttu-id="eb8a2-246">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-246">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="eb8a2-247">ProjInvoiceTableCreate.canClose</span><span class="sxs-lookup"><span data-stu-id="eb8a2-247">ProjInvoiceTableCreate.canClose</span></span>|
|<span data-ttu-id="eb8a2-248">ProjInvoiceTableCreate.initializeValues</span><span class="sxs-lookup"><span data-stu-id="eb8a2-248">ProjInvoiceTableCreate.initializeValues</span></span>|
|<span data-ttu-id="eb8a2-249">ProjPlanVersionsManager.createTemplateHierarchy</span><span class="sxs-lookup"><span data-stu-id="eb8a2-249">ProjPlanVersionsManager.createTemplateHierarchy</span></span>|
|<span data-ttu-id="eb8a2-250">ProjPostCostJournal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-250">ProjPostCostJournal.projTransCreate</span></span>|
|<span data-ttu-id="eb8a2-251">ProjSalesItemReq.SalesLine.linkActive</span><span class="sxs-lookup"><span data-stu-id="eb8a2-251">ProjSalesItemReq.SalesLine.linkActive</span></span>|
|<span data-ttu-id="eb8a2-252">ProjTableType_TimeMaterial.validateWrite</span><span class="sxs-lookup"><span data-stu-id="eb8a2-252">ProjTableType_TimeMaterial.validateWrite</span></span>|
|<span data-ttu-id="eb8a2-253">PurchAgreement.applyQueryRanges</span><span class="sxs-lookup"><span data-stu-id="eb8a2-253">PurchAgreement.applyQueryRanges</span></span>|
|<span data-ttu-id="eb8a2-254">PurchApproveJournalPost.postPurgeLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="eb8a2-254">PurchApproveJournalPost.postPurgeLedgerAccount</span></span>|
|<span data-ttu-id="eb8a2-255">PurchaseOrderResponseService.shouldPurchaseOrderBeAutoConfirmed</span><span class="sxs-lookup"><span data-stu-id="eb8a2-255">PurchaseOrderResponseService.shouldPurchaseOrderBeAutoConfirmed</span></span>|
|<span data-ttu-id="eb8a2-256">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-256">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="eb8a2-257">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-257">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="eb8a2-258">PurchAutoCreate_Sales.createLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-258">PurchAutoCreate_Sales.createLine</span></span>|
|<span data-ttu-id="eb8a2-259">PurchCalcTax.construct</span><span class="sxs-lookup"><span data-stu-id="eb8a2-259">PurchCalcTax.construct</span></span>|
|<span data-ttu-id="eb8a2-260">PurchCancel.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-260">PurchCancel.run</span></span>|
|<span data-ttu-id="eb8a2-261">PurchCreateFromOrder.insertMinMaxQty</span><span class="sxs-lookup"><span data-stu-id="eb8a2-261">PurchCreateFromOrder.insertMinMaxQty</span></span>|
|<span data-ttu-id="eb8a2-262">PurchCreateFromSalesOrder.insertIntoTmpPurchLinePrice</span><span class="sxs-lookup"><span data-stu-id="eb8a2-262">PurchCreateFromSalesOrder.insertIntoTmpPurchLinePrice</span></span>|
|<span data-ttu-id="eb8a2-263">PurchCreateFromSalesOrder.refreshCallerDataSource</span><span class="sxs-lookup"><span data-stu-id="eb8a2-263">PurchCreateFromSalesOrder.refreshCallerDataSource</span></span>|
|<span data-ttu-id="eb8a2-264">PurchCreateFromSalesOrder.Salesline.specifyMinMaxQty</span><span class="sxs-lookup"><span data-stu-id="eb8a2-264">PurchCreateFromSalesOrder.Salesline.specifyMinMaxQty</span></span>|
|<span data-ttu-id="eb8a2-265">PurchCreateFromSalesOrder.SalesLine.specifyVendAccount</span><span class="sxs-lookup"><span data-stu-id="eb8a2-265">PurchCreateFromSalesOrder.SalesLine.specifyVendAccount</span></span>|
|<span data-ttu-id="eb8a2-266">PurchCreateFromSalesOrder.validateSalesLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-266">PurchCreateFromSalesOrder.validateSalesLine</span></span>|
|<span data-ttu-id="eb8a2-267">PurchEditLines.canClose</span><span class="sxs-lookup"><span data-stu-id="eb8a2-267">PurchEditLines.canClose</span></span>|
|<span data-ttu-id="eb8a2-268">PurchEditLinesForm.construct</span><span class="sxs-lookup"><span data-stu-id="eb8a2-268">PurchEditLinesForm.construct</span></span>|
|<span data-ttu-id="eb8a2-269">PurchFormLetter.construct</span><span class="sxs-lookup"><span data-stu-id="eb8a2-269">PurchFormLetter.construct</span></span>|
|<span data-ttu-id="eb8a2-270">PurchFormLetterContract.newFromPackedVersion</span><span class="sxs-lookup"><span data-stu-id="eb8a2-270">PurchFormLetterContract.newFromPackedVersion</span></span>|
|<span data-ttu-id="eb8a2-271">PurchFormletterParmDataInvoice.selectFromJournalLines</span><span class="sxs-lookup"><span data-stu-id="eb8a2-271">PurchFormletterParmDataInvoice.selectFromJournalLines</span></span>|
|<span data-ttu-id="eb8a2-272">PurchFormLetterProvider.checkPurchLineChanged</span><span class="sxs-lookup"><span data-stu-id="eb8a2-272">PurchFormLetterProvider.checkPurchLineChanged</span></span>|
|<span data-ttu-id="eb8a2-273">PurchInvoiceJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-273">PurchInvoiceJournalPost.updateSourceLine</span></span>|
|<span data-ttu-id="eb8a2-274">PurchLine.checkInvoiceConstraints</span><span class="sxs-lookup"><span data-stu-id="eb8a2-274">PurchLine.checkInvoiceConstraints</span></span>|
|<span data-ttu-id="eb8a2-275">PurchLine.ledgerDimensionItem</span><span class="sxs-lookup"><span data-stu-id="eb8a2-275">PurchLine.ledgerDimensionItem</span></span>|
|<span data-ttu-id="eb8a2-276">PurchLine.ledgerDimensionReceipt</span><span class="sxs-lookup"><span data-stu-id="eb8a2-276">PurchLine.ledgerDimensionReceipt</span></span>|
|<span data-ttu-id="eb8a2-277">Purchline.unLinkAgreementLinePrompt</span><span class="sxs-lookup"><span data-stu-id="eb8a2-277">Purchline.unLinkAgreementLinePrompt</span></span>|
|<span data-ttu-id="eb8a2-278">PurchLine.validateField</span><span class="sxs-lookup"><span data-stu-id="eb8a2-278">PurchLine.validateField</span></span>|
|<span data-ttu-id="eb8a2-279">PurchLine::setProjSalesPrice</span><span class="sxs-lookup"><span data-stu-id="eb8a2-279">PurchLine::setProjSalesPrice</span></span>|
|<span data-ttu-id="eb8a2-280">PurchPrepayTable.updateAdvanceApplicationRemaining</span><span class="sxs-lookup"><span data-stu-id="eb8a2-280">PurchPrepayTable.updateAdvanceApplicationRemaining</span></span>|
|<span data-ttu-id="eb8a2-281">PurchPurchOrderJournalPost.updateSourceTable</span><span class="sxs-lookup"><span data-stu-id="eb8a2-281">PurchPurchOrderJournalPost.updateSourceTable</span></span>|
|<span data-ttu-id="eb8a2-282">PurchReqCreate.init</span><span class="sxs-lookup"><span data-stu-id="eb8a2-282">PurchReqCreate.init</span></span>|
|<span data-ttu-id="eb8a2-283">PurchReqLine.setDefaultDimension</span><span class="sxs-lookup"><span data-stu-id="eb8a2-283">PurchReqLine.setDefaultDimension</span></span>|
|<span data-ttu-id="eb8a2-284">PurchReqLine.validateWrite</span><span class="sxs-lookup"><span data-stu-id="eb8a2-284">PurchReqLine.validateWrite</span></span>|
|<span data-ttu-id="eb8a2-285">PurchReqTable.init</span><span class="sxs-lookup"><span data-stu-id="eb8a2-285">PurchReqTable.init</span></span>|
|<span data-ttu-id="eb8a2-286">PurchReqTableForm.new</span><span class="sxs-lookup"><span data-stu-id="eb8a2-286">PurchReqTableForm.new</span></span>|
|<span data-ttu-id="eb8a2-287">PurchRFQCaseTable.init</span><span class="sxs-lookup"><span data-stu-id="eb8a2-287">PurchRFQCaseTable.init</span></span>|
|<span data-ttu-id="eb8a2-288">PurchTable.jumpRefIntercompanySalesOrder</span><span class="sxs-lookup"><span data-stu-id="eb8a2-288">PurchTable.jumpRefIntercompanySalesOrder</span></span>|
|<span data-ttu-id="eb8a2-289">PurchTableForm_DeliverySchedule.updatePurchLineTable</span><span class="sxs-lookup"><span data-stu-id="eb8a2-289">PurchTableForm_DeliverySchedule.updatePurchLineTable</span></span>|
|<span data-ttu-id="eb8a2-290">PurchTableInteraction.enableHeaderReceive</span><span class="sxs-lookup"><span data-stu-id="eb8a2-290">PurchTableInteraction.enableHeaderReceive</span></span>|
|<span data-ttu-id="eb8a2-291">PurchTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="eb8a2-291">PurchTableType.validateDelete</span></span>|
|<span data-ttu-id="eb8a2-292">PurchTableUpdateFromPurchReqLineMap.update</span><span class="sxs-lookup"><span data-stu-id="eb8a2-292">PurchTableUpdateFromPurchReqLineMap.update</span></span>|
|<span data-ttu-id="eb8a2-293">ReqTransPoMarkFirm.setPurchBuyerGroupId & updatePurchBuyerGroup</span><span class="sxs-lookup"><span data-stu-id="eb8a2-293">ReqTransPoMarkFirm.setPurchBuyerGroupId & updatePurchBuyerGroup</span></span>|
|<span data-ttu-id="eb8a2-294">RetailGroupMemberLineHelper.internalCreateOrUpdateOrRemoveRetailGroupMemberLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-294">RetailGroupMemberLineHelper.internalCreateOrUpdateOrRemoveRetailGroupMemberLine</span></span>|
|<span data-ttu-id="eb8a2-295">RetailLabelDP.insertTmpTable</span><span class="sxs-lookup"><span data-stu-id="eb8a2-295">RetailLabelDP.insertTmpTable</span></span>|
|<span data-ttu-id="eb8a2-296">SalesCalcAvailableDlvDates.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="eb8a2-296">SalesCalcAvailableDlvDates.mainOnServer</span></span>|
|<span data-ttu-id="eb8a2-297">SalesConfirmJournalPost.updateSourceTable</span><span class="sxs-lookup"><span data-stu-id="eb8a2-297">SalesConfirmJournalPost.updateSourceTable</span></span>|
|<span data-ttu-id="eb8a2-298">SalesCopying.editCopy</span><span class="sxs-lookup"><span data-stu-id="eb8a2-298">SalesCopying.editCopy</span></span>|
|<span data-ttu-id="eb8a2-299">SalesCopying.editMarkAll</span><span class="sxs-lookup"><span data-stu-id="eb8a2-299">SalesCopying.editMarkAll</span></span>|
|<span data-ttu-id="eb8a2-300">SalesCopying.initReturnOrderFromCustomer</span><span class="sxs-lookup"><span data-stu-id="eb8a2-300">SalesCopying.initReturnOrderFromCustomer</span></span>|
|<span data-ttu-id="eb8a2-301">SalesCreateQuotation.canClose</span><span class="sxs-lookup"><span data-stu-id="eb8a2-301">SalesCreateQuotation.canClose</span></span>|
|<span data-ttu-id="eb8a2-302">SalesDropShipmentCancel.removeMarking</span><span class="sxs-lookup"><span data-stu-id="eb8a2-302">SalesDropShipmentCancel.removeMarking</span></span>|
|<span data-ttu-id="eb8a2-303">SalesEditLines.canClose</span><span class="sxs-lookup"><span data-stu-id="eb8a2-303">SalesEditLines.canClose</span></span>|
|<span data-ttu-id="eb8a2-304">SalesFormletterParmData.reArrangeLines</span><span class="sxs-lookup"><span data-stu-id="eb8a2-304">SalesFormletterParmData.reArrangeLines</span></span>|
|<span data-ttu-id="eb8a2-305">SalesFormletterParmData.reArrangeSplit</span><span class="sxs-lookup"><span data-stu-id="eb8a2-305">SalesFormletterParmData.reArrangeSplit</span></span>|
|<span data-ttu-id="eb8a2-306">SalesFormletterParmData.reArrangeSplit</span><span class="sxs-lookup"><span data-stu-id="eb8a2-306">SalesFormletterParmData.reArrangeSplit</span></span>|
|<span data-ttu-id="eb8a2-307">SalesFormLetterProvider.checkJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-307">SalesFormLetterProvider.checkJournal</span></span>|
|<span data-ttu-id="eb8a2-308">SalesInvoiceDP.insertGiroInformation</span><span class="sxs-lookup"><span data-stu-id="eb8a2-308">SalesInvoiceDP.insertGiroInformation</span></span>|
|<span data-ttu-id="eb8a2-309">SalesInvoiceJournalCreate.checkDocumentData_PL</span><span class="sxs-lookup"><span data-stu-id="eb8a2-309">SalesInvoiceJournalCreate.checkDocumentData_PL</span></span>|
|<span data-ttu-id="eb8a2-310">SalesInvoiceJournalPostBase.postLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-310">SalesInvoiceJournalPostBase.postLine</span></span>|
|<span data-ttu-id="eb8a2-311">SalesLine.resetInvent</span><span class="sxs-lookup"><span data-stu-id="eb8a2-311">SalesLine.resetInvent</span></span>|
|<span data-ttu-id="eb8a2-312">SalesLineType.initDimensionsSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="eb8a2-312">SalesLineType.initDimensionsSpecificDefaulting</span></span>|
|<span data-ttu-id="eb8a2-313">SalesLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="eb8a2-313">SalesLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="eb8a2-314">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="eb8a2-314">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="eb8a2-315">SalesPackingSlipJournalCreate.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-315">SalesPackingSlipJournalCreate.updateJournalLine</span></span>|
|<span data-ttu-id="eb8a2-316">SalesPackingSlipJournalCreate.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-316">SalesPackingSlipJournalCreate.updateJournalLine</span></span>|
|<span data-ttu-id="eb8a2-317">SalesPackingSlipJournalPost.insertBackorderLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-317">SalesPackingSlipJournalPost.insertBackorderLine</span></span>|
|<span data-ttu-id="eb8a2-318">SalesPackingSlipJournalPost.interCompanyPost</span><span class="sxs-lookup"><span data-stu-id="eb8a2-318">SalesPackingSlipJournalPost.interCompanyPost</span></span>|
|<span data-ttu-id="eb8a2-319">SalesPackingSlipJournalPost.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-319">SalesPackingSlipJournalPost.updateJournalLine</span></span>|
|<span data-ttu-id="eb8a2-320">SalesPurchSummaryModel_Account.createNewJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-320">SalesPurchSummaryModel_Account.createNewJournal</span></span>|
|<span data-ttu-id="eb8a2-321">SalesQuotationCalcTax_Sales.construct</span><span class="sxs-lookup"><span data-stu-id="eb8a2-321">SalesQuotationCalcTax_Sales.construct</span></span>|
|<span data-ttu-id="eb8a2-322">SalesQuotationEditLinesForm.postUpdate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-322">SalesQuotationEditLinesForm.postUpdate</span></span>|
|<span data-ttu-id="eb8a2-323">SalesQuotationLineType.initFromProjTable</span><span class="sxs-lookup"><span data-stu-id="eb8a2-323">SalesQuotationLineType.initFromProjTable</span></span>|
|<span data-ttu-id="eb8a2-324">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="eb8a2-324">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="eb8a2-325">SalesQuotationTable.modifiedField</span><span class="sxs-lookup"><span data-stu-id="eb8a2-325">SalesQuotationTable.modifiedField</span></span>|
|<span data-ttu-id="eb8a2-326">SalesQuotationTableForm.createFromTemplate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-326">SalesQuotationTableForm.createFromTemplate</span></span>|
|<span data-ttu-id="eb8a2-327">SalesQuotationUpdate_Cancelled.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-327">SalesQuotationUpdate_Cancelled.run</span></span>|
|<span data-ttu-id="eb8a2-328">SalesQuotationUpdate_Lost.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-328">SalesQuotationUpdate_Lost.run</span></span>|
|<span data-ttu-id="eb8a2-329">SalesTable.initFromCustTableMandatoryFields</span><span class="sxs-lookup"><span data-stu-id="eb8a2-329">SalesTable.initFromCustTableMandatoryFields</span></span>|
|<span data-ttu-id="eb8a2-330">SalesTable.jumpRefIntercompanyPurchaseOrder</span><span class="sxs-lookup"><span data-stu-id="eb8a2-330">SalesTable.jumpRefIntercompanyPurchaseOrder</span></span>|
|<span data-ttu-id="eb8a2-331">SalesTable.setShipCarrierFromLogisticsLocation</span><span class="sxs-lookup"><span data-stu-id="eb8a2-331">SalesTable.setShipCarrierFromLogisticsLocation</span></span>|
|<span data-ttu-id="eb8a2-332">SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="eb8a2-332">SalesTable.update</span></span>|
|<span data-ttu-id="eb8a2-333">SalesTableForm.interCompanyAutoCreateOrders</span><span class="sxs-lookup"><span data-stu-id="eb8a2-333">SalesTableForm.interCompanyAutoCreateOrders</span></span>|
|<span data-ttu-id="eb8a2-334">SettlementPair.createSettlementForDebitOrCreditTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-334">SettlementPair.createSettlementForDebitOrCreditTrans</span></span>|
|<span data-ttu-id="eb8a2-335">SmaServiceFunctionLine_Transfer.createJournalLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-335">SmaServiceFunctionLine_Transfer.createJournalLine</span></span>|
|<span data-ttu-id="eb8a2-336">SmaServiceFunctionLine_Transfer.postJournalTransType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-336">SmaServiceFunctionLine_Transfer.postJournalTransType</span></span>|
|<span data-ttu-id="eb8a2-337">SmaServiceOrderCreate.createServiceOrderLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-337">SmaServiceOrderCreate.createServiceOrderLine</span></span>|
|<span data-ttu-id="eb8a2-338">SmaSubscriptionGenerator::postTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-338">SmaSubscriptionGenerator::postTrans</span></span>|
|<span data-ttu-id="eb8a2-339">smmBusRelTable.relation2Vendor</span><span class="sxs-lookup"><span data-stu-id="eb8a2-339">smmBusRelTable.relation2Vendor</span></span>|
|<span data-ttu-id="eb8a2-340">smmBusRelTable.updateQuotations</span><span class="sxs-lookup"><span data-stu-id="eb8a2-340">smmBusRelTable.updateQuotations</span></span>|
|<span data-ttu-id="eb8a2-341">SmmCampaignBroadcast::validate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-341">SmmCampaignBroadcast::validate</span></span>|
|<span data-ttu-id="eb8a2-342">SmmOpportunityStatusUpdate.updateOpportunity</span><span class="sxs-lookup"><span data-stu-id="eb8a2-342">SmmOpportunityStatusUpdate.updateOpportunity</span></span>|
|<span data-ttu-id="eb8a2-343">smmOpportunityTable\Methods\openQuotation</span><span class="sxs-lookup"><span data-stu-id="eb8a2-343">smmOpportunityTable\Methods\openQuotation</span></span>|
|<span data-ttu-id="eb8a2-344">SmmProjectCreate.createSingleProject</span><span class="sxs-lookup"><span data-stu-id="eb8a2-344">SmmProjectCreate.createSingleProject</span></span>|
|<span data-ttu-id="eb8a2-345">SmmProjectCreate.createSingleProject</span><span class="sxs-lookup"><span data-stu-id="eb8a2-345">SmmProjectCreate.createSingleProject</span></span>|
|<span data-ttu-id="eb8a2-346">SmmUpdateBusRel.updateFromVendTableSFA2</span><span class="sxs-lookup"><span data-stu-id="eb8a2-346">SmmUpdateBusRel.updateFromVendTableSFA2</span></span>|
|<span data-ttu-id="eb8a2-347">SubledgerJournalTransferController.run</span><span class="sxs-lookup"><span data-stu-id="eb8a2-347">SubledgerJournalTransferController.run</span></span>|
|<span data-ttu-id="eb8a2-348">SuppItem.calcSuppItem</span><span class="sxs-lookup"><span data-stu-id="eb8a2-348">SuppItem.calcSuppItem</span></span>|
|<span data-ttu-id="eb8a2-349">SuppItem::newSuppItem</span><span class="sxs-lookup"><span data-stu-id="eb8a2-349">SuppItem::newSuppItem</span></span>|
|<span data-ttu-id="eb8a2-350">SuppItemCreate::newSuppItemCreate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-350">SuppItemCreate::newSuppItemCreate</span></span>|
|<span data-ttu-id="eb8a2-351">Tax.post</span><span class="sxs-lookup"><span data-stu-id="eb8a2-351">Tax.post</span></span>|
|<span data-ttu-id="eb8a2-352">Tax.saveAndPost</span><span class="sxs-lookup"><span data-stu-id="eb8a2-352">Tax.saveAndPost</span></span>|
|<span data-ttu-id="eb8a2-353">TaxFreeInvoice_Invoice.updateAndPost</span><span class="sxs-lookup"><span data-stu-id="eb8a2-353">TaxFreeInvoice_Invoice.updateAndPost</span></span>|
|<span data-ttu-id="eb8a2-354">TaxPost.moveTaxLineToNewOwner</span><span class="sxs-lookup"><span data-stu-id="eb8a2-354">TaxPost.moveTaxLineToNewOwner</span></span>|
|<span data-ttu-id="eb8a2-355">TaxPost.saveAndPostFromTmpTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-355">TaxPost.saveAndPostFromTmpTaxWorkTrans</span></span>|
|<span data-ttu-id="eb8a2-356">TaxPost.saveAndPostFromTmpTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-356">TaxPost.saveAndPostFromTmpTaxWorkTrans</span></span>|
|<span data-ttu-id="eb8a2-357">TaxVoucherService.postTaxOnErrorAccount</span><span class="sxs-lookup"><span data-stu-id="eb8a2-357">TaxVoucherService.postTaxOnErrorAccount</span></span>|
|<span data-ttu-id="eb8a2-358">TradePackingSlipJourChain.createRelationship</span><span class="sxs-lookup"><span data-stu-id="eb8a2-358">TradePackingSlipJourChain.createRelationship</span></span>|
|<span data-ttu-id="eb8a2-359">TradeTotals.calc</span><span class="sxs-lookup"><span data-stu-id="eb8a2-359">TradeTotals.calc</span></span>|
|<span data-ttu-id="eb8a2-360">TradeTotals.updateOrderBalances</span><span class="sxs-lookup"><span data-stu-id="eb8a2-360">TradeTotals.updateOrderBalances</span></span>|
|<span data-ttu-id="eb8a2-361">VendAccountStatementIntDP.processReport</span><span class="sxs-lookup"><span data-stu-id="eb8a2-361">VendAccountStatementIntDP.processReport</span></span>|
|<span data-ttu-id="eb8a2-362">VendEditInvoice\DataSource\VendInvoiceInfoTable\Methods\write</span><span class="sxs-lookup"><span data-stu-id="eb8a2-362">VendEditInvoice\DataSource\VendInvoiceInfoTable\Methods\write</span></span>|
|<span data-ttu-id="eb8a2-363">VendInvoiceMatching.initExpectedValues</span><span class="sxs-lookup"><span data-stu-id="eb8a2-363">VendInvoiceMatching.initExpectedValues</span></span>|
|<span data-ttu-id="eb8a2-364">VendInvoiceWFParticipantProviderExpend.resolve</span><span class="sxs-lookup"><span data-stu-id="eb8a2-364">VendInvoiceWFParticipantProviderExpend.resolve</span></span>|
|<span data-ttu-id="eb8a2-365">VendOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-365">VendOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="eb8a2-366">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="eb8a2-366">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="eb8a2-367">VendPaymentJournalDP.insertDataFromLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-367">VendPaymentJournalDP.insertDataFromLedgerJournalTrans</span></span>|
|<span data-ttu-id="eb8a2-368">VendPaymentJournalDP.insertDataFromSpecTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-368">VendPaymentJournalDP.insertDataFromSpecTrans</span></span>|
|<span data-ttu-id="eb8a2-369">VendPromissoryNotePost.postNextStep</span><span class="sxs-lookup"><span data-stu-id="eb8a2-369">VendPromissoryNotePost.postNextStep</span></span>|
|<span data-ttu-id="eb8a2-370">VendProvisionalBalanceDP.calculateAmounts</span><span class="sxs-lookup"><span data-stu-id="eb8a2-370">VendProvisionalBalanceDP.calculateAmounts</span></span>|
|<span data-ttu-id="eb8a2-371">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="eb8a2-371">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="eb8a2-372">VendProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="eb8a2-372">VendProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="eb8a2-373">VendTransListDP.ProcessReport</span><span class="sxs-lookup"><span data-stu-id="eb8a2-373">VendTransListDP.ProcessReport</span></span>|
|<span data-ttu-id="eb8a2-374">VendVoucher.createInvoiceJournal</span><span class="sxs-lookup"><span data-stu-id="eb8a2-374">VendVoucher.createInvoiceJournal</span></span>|
|<span data-ttu-id="eb8a2-375">WHSDocumentRouting.printDocument</span><span class="sxs-lookup"><span data-stu-id="eb8a2-375">WHSDocumentRouting.printDocument</span></span>|
|<span data-ttu-id="eb8a2-376">WhsLoadLineInventTransValidator.checkLoadLineInventTransConsistencyOnInventoryUpdate</span><span class="sxs-lookup"><span data-stu-id="eb8a2-376">WhsLoadLineInventTransValidator.checkLoadLineInventTransConsistencyOnInventoryUpdate</span></span>|
|<span data-ttu-id="eb8a2-377">WHSLoadLineUpdater.initAndInsertLoadLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-377">WHSLoadLineUpdater.initAndInsertLoadLine</span></span>|
|<span data-ttu-id="eb8a2-378">WhsShipConfirm.createASNItems</span><span class="sxs-lookup"><span data-stu-id="eb8a2-378">WhsShipConfirm.createASNItems</span></span>|
|<span data-ttu-id="eb8a2-379">WhsWarehouseRelease.createLoadLines</span><span class="sxs-lookup"><span data-stu-id="eb8a2-379">WhsWarehouseRelease.createLoadLines</span></span>|
|<span data-ttu-id="eb8a2-380">WHSWorkExecute.executeShortPick</span><span class="sxs-lookup"><span data-stu-id="eb8a2-380">WHSWorkExecute.executeShortPick</span></span>|
|<span data-ttu-id="eb8a2-381">WHSWorkExecuteDisplayLPReceiving.displayForm</span><span class="sxs-lookup"><span data-stu-id="eb8a2-381">WHSWorkExecuteDisplayLPReceiving.displayForm</span></span>|
|<span data-ttu-id="eb8a2-382">WHSWorkExecuteDisplayLPReceiving.displayNextForm</span><span class="sxs-lookup"><span data-stu-id="eb8a2-382">WHSWorkExecuteDisplayLPReceiving.displayNextForm</span></span>|
|<span data-ttu-id="eb8a2-383">WHSWorkExecuteDisplayMovementByTemplate.displayForm</span><span class="sxs-lookup"><span data-stu-id="eb8a2-383">WHSWorkExecuteDisplayMovementByTemplate.displayForm</span></span>|
|<span data-ttu-id="eb8a2-384">WhsWorkExecuteForm.createLabel</span><span class="sxs-lookup"><span data-stu-id="eb8a2-384">WhsWorkExecuteForm.createLabel</span></span>|
|<span data-ttu-id="eb8a2-385">WmsJournalCheckPostReception.postTrans</span><span class="sxs-lookup"><span data-stu-id="eb8a2-385">WmsJournalCheckPostReception.postTrans</span></span>|
|<span data-ttu-id="eb8a2-386">WmsOnlineCountingServer.getMovement</span><span class="sxs-lookup"><span data-stu-id="eb8a2-386">WmsOnlineCountingServer.getMovement</span></span>|
|<span data-ttu-id="eb8a2-387">WmsOnlineCountingServer.handleLine</span><span class="sxs-lookup"><span data-stu-id="eb8a2-387">WmsOnlineCountingServer.handleLine</span></span>|
|<span data-ttu-id="eb8a2-388">WmsOrderCreate.updateCreatewmsOrder</span><span class="sxs-lookup"><span data-stu-id="eb8a2-388">WmsOrderCreate.updateCreatewmsOrder</span></span>|
|<span data-ttu-id="eb8a2-389">WrkCtrResourceAbilityMapController.loadData</span><span class="sxs-lookup"><span data-stu-id="eb8a2-389">WrkCtrResourceAbilityMapController.loadData</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="eb8a2-390">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="eb8a2-390">Enumerations made extensible</span></span>

<span data-ttu-id="eb8a2-391">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-391">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="eb8a2-392">列挙型</span><span class="sxs-lookup"><span data-stu-id="eb8a2-392">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="eb8a2-393">ABCModel</span><span class="sxs-lookup"><span data-stu-id="eb8a2-393">ABCModel</span></span>|
|<span data-ttu-id="eb8a2-394">AccountOrder</span><span class="sxs-lookup"><span data-stu-id="eb8a2-394">AccountOrder</span></span>|
|<span data-ttu-id="eb8a2-395">AmountUnit</span><span class="sxs-lookup"><span data-stu-id="eb8a2-395">AmountUnit</span></span>|
|<span data-ttu-id="eb8a2-396">CostCalculationRateSubtype</span><span class="sxs-lookup"><span data-stu-id="eb8a2-396">CostCalculationRateSubtype</span></span>|
|<span data-ttu-id="eb8a2-397">CurrencyGainLossAccountType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-397">CurrencyGainLossAccountType</span></span>|
|<span data-ttu-id="eb8a2-398">CustInterestCodeSource</span><span class="sxs-lookup"><span data-stu-id="eb8a2-398">CustInterestCodeSource</span></span>|
|<span data-ttu-id="eb8a2-399">CustPaymentType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-399">CustPaymentType</span></span>|
|<span data-ttu-id="eb8a2-400">DirViewLocationNodeType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-400">DirViewLocationNodeType</span></span>|
|<span data-ttu-id="eb8a2-401">InterestCalcAccountChoice</span><span class="sxs-lookup"><span data-stu-id="eb8a2-401">InterestCalcAccountChoice</span></span>|
|<span data-ttu-id="eb8a2-402">InventTransPostingType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-402">InventTransPostingType</span></span>|
|<span data-ttu-id="eb8a2-403">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-403">MCRCustSearchType</span></span>|
|<span data-ttu-id="eb8a2-404">PaymentStub</span><span class="sxs-lookup"><span data-stu-id="eb8a2-404">PaymentStub</span></span>|
|<span data-ttu-id="eb8a2-405">PaymentStubInclAll</span><span class="sxs-lookup"><span data-stu-id="eb8a2-405">PaymentStubInclAll</span></span>|
|<span data-ttu-id="eb8a2-406">ProjCompletePrincip</span><span class="sxs-lookup"><span data-stu-id="eb8a2-406">ProjCompletePrincip</span></span>|
|<span data-ttu-id="eb8a2-407">ProjMatchingPrincip</span><span class="sxs-lookup"><span data-stu-id="eb8a2-407">ProjMatchingPrincip</span></span>|
|<span data-ttu-id="eb8a2-408">RetailPOSSeedDataType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-408">RetailPOSSeedDataType</span></span>|
|<span data-ttu-id="eb8a2-409">SalesQuotationStatus</span><span class="sxs-lookup"><span data-stu-id="eb8a2-409">SalesQuotationStatus</span></span>|
|<span data-ttu-id="eb8a2-410">TMSApptStatus</span><span class="sxs-lookup"><span data-stu-id="eb8a2-410">TMSApptStatus</span></span>|
|<span data-ttu-id="eb8a2-411">TMSCommunicationType</span><span class="sxs-lookup"><span data-stu-id="eb8a2-411">TMSCommunicationType</span></span>|

## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="eb8a2-412">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="eb8a2-412">Additional extensibility enhancements</span></span>

<span data-ttu-id="eb8a2-413">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-413">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="eb8a2-414">CustVendSettle: 変数をプライベートではなく保護に設定します。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-414">CustVendSettle: set variables protected instead of private.</span></span>
- <span data-ttu-id="eb8a2-415">イベントを引き起こさないデータ操作メソッド: WHSLocationDirective.loopLocDirLines。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-415">Data manipulation method not raising event: WHSLocationDirective.loopLocDirLines.</span></span>
- <span data-ttu-id="eb8a2-416">イベントを引き起こさないデータ操作メソッド: WhsWorkCreate.createTempLine。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-416">Data manipulation method not raising event: WhsWorkCreate.createTempLine.</span></span>
- <span data-ttu-id="eb8a2-417">マップ拡張: LogisticsPostalAddressMap。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-417">Map extension: LogisticsPostalAddressMap.</span></span>
- <span data-ttu-id="eb8a2-418">マップ拡張: PurchReqLineMap。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-418">Map extension: PurchReqLineMap.</span></span>
- <span data-ttu-id="eb8a2-419">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Is Public = Yes。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-419">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Is Public = Yes.</span></span>
- <span data-ttu-id="eb8a2-420">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Collection Name = ProjWBSActivityEstimates。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-420">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Public Collection Name = ProjWBSActivityEstimates.</span></span>
- <span data-ttu-id="eb8a2-421">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Entity Name = ProjWBSActivityEstimates</span><span class="sxs-lookup"><span data-stu-id="eb8a2-421">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Public Entity Name = ProjWBSActivityEstimates</span></span>
- <span data-ttu-id="eb8a2-422">メタデータの変更: /Data Model/Data Entities/EcoResProductAttributeValueEntity.IsPublic = Yes。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-422">Metadata change: /Data Model/Data Entities/EcoResProductAttributeValueEntity.IsPublic = Yes.</span></span>
- <span data-ttu-id="eb8a2-423">メタデータの変更: Form/WHSLoadPlanningListPage/FormDesign/FormDesign/FormActionPaneTabControl/ActionPaneTabShipReceive.Needed permission。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-423">Metadata change: Form/WHSLoadPlanningListPage/FormDesign/FormDesign/FormActionPaneTabControl/ActionPaneTabShipReceive.Needed permission.</span></span>
- <span data-ttu-id="eb8a2-424">メタデータの変更: WHSContainerLine, Relations WHSLoadLine & WHSShipmentTable.On Delete。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-424">Metadata change: WHSContainerLine, Relations WHSLoadLine & WHSShipmentTable.On Delete.</span></span>
- <span data-ttu-id="eb8a2-425">メタデータの変更: WHSContainerTable, Relation WHSShipmentTable.On Delete。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-425">Metadata change: WHSContainerTable, Relation WHSShipmentTable.On Delete.</span></span>
- <span data-ttu-id="eb8a2-426">プロジェクトの価格決定: 新しい価格決定検索メソッドの完全な取得。</span><span class="sxs-lookup"><span data-stu-id="eb8a2-426">Project pricing: complete uptake of new pricing find methods.</span></span>
