---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
ms.date: 08/27/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-08-31
ms.dyn365.ops.version: App 8.0.4
ms.openlocfilehash: 63ad2f14f875fedbb2c2985d4b9b766a2725a177
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866262"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-804"></a><span data-ttu-id="b8d4b-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="b8d4b-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.4</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8d4b-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.4.</span></span> <span data-ttu-id="b8d4b-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="b8d4b-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="b8d4b-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="b8d4b-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="b8d4b-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="b8d4b-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="b8d4b-109">AgreementHeader.getModuleType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-109">AgreementHeader.getModuleType</span></span>|
|<span data-ttu-id="b8d4b-110">AssetSplit.construct</span><span class="sxs-lookup"><span data-stu-id="b8d4b-110">AssetSplit.construct</span></span>|
|<span data-ttu-id="b8d4b-111">BankDepositSlipController.main</span><span class="sxs-lookup"><span data-stu-id="b8d4b-111">BankDepositSlipController.main</span></span>|
|<span data-ttu-id="b8d4b-112">BankPositivePayExport.sendFileToUser</span><span class="sxs-lookup"><span data-stu-id="b8d4b-112">BankPositivePayExport.sendFileToUser</span></span>|
|<span data-ttu-id="b8d4b-113">CaseDetailForm.getRecordsFromDataSource</span><span class="sxs-lookup"><span data-stu-id="b8d4b-113">CaseDetailForm.getRecordsFromDataSource</span></span>|
|<span data-ttu-id="b8d4b-114">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span><span class="sxs-lookup"><span data-stu-id="b8d4b-114">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span></span>|
|<span data-ttu-id="b8d4b-115">CostSheetNodeCalculation.validate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-115">CostSheetNodeCalculation.validate</span></span>|
|<span data-ttu-id="b8d4b-116">CostSheetNodeCalculationRate.calcLowestLevel</span><span class="sxs-lookup"><span data-stu-id="b8d4b-116">CostSheetNodeCalculationRate.calcLowestLevel</span></span>|
|<span data-ttu-id="b8d4b-117">CostSheetNodeCalculationSurcharge.equal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-117">CostSheetNodeCalculationSurcharge.equal</span></span>|
|<span data-ttu-id="b8d4b-118">CustAccountStatementExtController.processParty</span><span class="sxs-lookup"><span data-stu-id="b8d4b-118">CustAccountStatementExtController.processParty</span></span>|
|<span data-ttu-id="b8d4b-119">CustAccountStatementExtDP.insertNewRecords</span><span class="sxs-lookup"><span data-stu-id="b8d4b-119">CustAccountStatementExtDP.insertNewRecords</span></span>|
|<span data-ttu-id="b8d4b-120">CustAccountStatementExtDP.setSysDocuBrandDetails</span><span class="sxs-lookup"><span data-stu-id="b8d4b-120">CustAccountStatementExtDP.setSysDocuBrandDetails</span></span>|
|<span data-ttu-id="b8d4b-121">CustBillOfExchangePost.postNextStep</span><span class="sxs-lookup"><span data-stu-id="b8d4b-121">CustBillOfExchangePost.postNextStep</span></span>|
|<span data-ttu-id="b8d4b-122">CustBillOfExchangePostProtestHonored.postNextStep</span><span class="sxs-lookup"><span data-stu-id="b8d4b-122">CustBillOfExchangePostProtestHonored.postNextStep</span></span>|
|<span data-ttu-id="b8d4b-123">CustCollectionJourController.runPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="b8d4b-123">CustCollectionJourController.runPrintMgmt</span></span>|
|<span data-ttu-id="b8d4b-124">CustCollectionLetterCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-124">CustCollectionLetterCreate.createJournal</span></span>|
|<span data-ttu-id="b8d4b-125">CustCollectionLetterCreate.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-125">CustCollectionLetterCreate.run</span></span>|
|<span data-ttu-id="b8d4b-126">CustCollectionLetterNote.CustCollectionLetterJour.active</span><span class="sxs-lookup"><span data-stu-id="b8d4b-126">CustCollectionLetterNote.CustCollectionLetterJour.active</span></span>|
|<span data-ttu-id="b8d4b-127">CustCollectionLetterPost.processRow</span><span class="sxs-lookup"><span data-stu-id="b8d4b-127">CustCollectionLetterPost.processRow</span></span>|
|<span data-ttu-id="b8d4b-128">CustCollectionLetterPost.validateCollectionLetter</span><span class="sxs-lookup"><span data-stu-id="b8d4b-128">CustCollectionLetterPost.validateCollectionLetter</span></span>|
|<span data-ttu-id="b8d4b-129">CustFreeInvoiceCorrection.createInvoiceLines</span><span class="sxs-lookup"><span data-stu-id="b8d4b-129">CustFreeInvoiceCorrection.createInvoiceLines</span></span>|
|<span data-ttu-id="b8d4b-130">CustInterestPost.main</span><span class="sxs-lookup"><span data-stu-id="b8d4b-130">CustInterestPost.main</span></span>|
|<span data-ttu-id="b8d4b-131">CustInterestPost.validateInterestTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-131">CustInterestPost.validateInterestTrans</span></span>|
|<span data-ttu-id="b8d4b-132">CustInvoiceJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-132">CustInvoiceJour.printJournal</span></span>|
|<span data-ttu-id="b8d4b-133">CustInvoiceTable.calcDue</span><span class="sxs-lookup"><span data-stu-id="b8d4b-133">CustInvoiceTable.calcDue</span></span>|
|<span data-ttu-id="b8d4b-134">CustOpenBalanceCurrency.Data Sources – VendTrans – init</span><span class="sxs-lookup"><span data-stu-id="b8d4b-134">CustOpenBalanceCurrency.Data Sources – VendTrans – init</span></span>|
|<span data-ttu-id="b8d4b-135">CustOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-135">CustOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="b8d4b-136">CustPackingSlipJourFormHelper.areCancelCorrectButtonsEnabled</span><span class="sxs-lookup"><span data-stu-id="b8d4b-136">CustPackingSlipJourFormHelper.areCancelCorrectButtonsEnabled</span></span>|
|<span data-ttu-id="b8d4b-137">CustPaymEntry.editIsMarkedForSettlement</span><span class="sxs-lookup"><span data-stu-id="b8d4b-137">CustPaymEntry.editIsMarkedForSettlement</span></span>|
|<span data-ttu-id="b8d4b-138">CustPostInvoice.main</span><span class="sxs-lookup"><span data-stu-id="b8d4b-138">CustPostInvoice.main</span></span>|
|<span data-ttu-id="b8d4b-139">CustPostInvoice.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-139">CustPostInvoice.run</span></span>|
|<span data-ttu-id="b8d4b-140">CustPostInvoice.validate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-140">CustPostInvoice.validate</span></span>|
|<span data-ttu-id="b8d4b-141">CustPostInvoiceJob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-141">CustPostInvoiceJob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="b8d4b-142">CustPostInvoiceJob.initializeCustPostProcess</span><span class="sxs-lookup"><span data-stu-id="b8d4b-142">CustPostInvoiceJob.initializeCustPostProcess</span></span>|
|<span data-ttu-id="b8d4b-143">CustPostInvoiceJob.main</span><span class="sxs-lookup"><span data-stu-id="b8d4b-143">CustPostInvoiceJob.main</span></span>|
|<span data-ttu-id="b8d4b-144">CustPostInvoiceJob.processCustPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-144">CustPostInvoiceJob.processCustPostInvoiceUpdate</span></span>|
|<span data-ttu-id="b8d4b-145">CustProvisionalBalanceDP.calculateAmounts</span><span class="sxs-lookup"><span data-stu-id="b8d4b-145">CustProvisionalBalanceDP.calculateAmounts</span></span>|
|<span data-ttu-id="b8d4b-146">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="b8d4b-146">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="b8d4b-147">CustProvisionalBalanceDP.populateCustProvisionalBalanceTmpProcessing</span><span class="sxs-lookup"><span data-stu-id="b8d4b-147">CustProvisionalBalanceDP.populateCustProvisionalBalanceTmpProcessing</span></span>|
|<span data-ttu-id="b8d4b-148">CustProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="b8d4b-148">CustProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="b8d4b-149">CustProvisionalBalanceDP.translateMainAccountNamesOnCustProvisionalBalanceTmpProcessing</span><span class="sxs-lookup"><span data-stu-id="b8d4b-149">CustProvisionalBalanceDP.translateMainAccountNamesOnCustProvisionalBalanceTmpProcessing</span></span>|
|<span data-ttu-id="b8d4b-150">CustQuotationJournal.launchReport</span><span class="sxs-lookup"><span data-stu-id="b8d4b-150">CustQuotationJournal.launchReport</span></span>|
|<span data-ttu-id="b8d4b-151">CustSettlementPriorityProcessing .createTempData</span><span class="sxs-lookup"><span data-stu-id="b8d4b-151">CustSettlementPriorityProcessing .createTempData</span></span>|
|<span data-ttu-id="b8d4b-152">CustSettlementPriorityProcessing .setPaymentAmount</span><span class="sxs-lookup"><span data-stu-id="b8d4b-152">CustSettlementPriorityProcessing .setPaymentAmount</span></span>|
|<span data-ttu-id="b8d4b-153">CustSettlementPriorityProcessing .updatePartialTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-153">CustSettlementPriorityProcessing .updatePartialTrans</span></span>|
|<span data-ttu-id="b8d4b-154">CustSettlementPriorityProcessing.classDeclaration</span><span class="sxs-lookup"><span data-stu-id="b8d4b-154">CustSettlementPriorityProcessing.classDeclaration</span></span>|
|<span data-ttu-id="b8d4b-155">CustSettlementPriorityProcessing.constructCustOpenTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-155">CustSettlementPriorityProcessing.constructCustOpenTrans</span></span>|
|<span data-ttu-id="b8d4b-156">CustSettlementPriorityProcessing.constructCustPaymEntry</span><span class="sxs-lookup"><span data-stu-id="b8d4b-156">CustSettlementPriorityProcessing.constructCustPaymEntry</span></span>|
|<span data-ttu-id="b8d4b-157">CustSettlementPriorityProcessing.constructOffsetVoucherCust</span><span class="sxs-lookup"><span data-stu-id="b8d4b-157">CustSettlementPriorityProcessing.constructOffsetVoucherCust</span></span>|
|<span data-ttu-id="b8d4b-158">CustSettlementPriorityProcessing.getBillingPriorities</span><span class="sxs-lookup"><span data-stu-id="b8d4b-158">CustSettlementPriorityProcessing.getBillingPriorities</span></span>|
|<span data-ttu-id="b8d4b-159">CustSettlementPriorityProcessing.getSettlementQuery</span><span class="sxs-lookup"><span data-stu-id="b8d4b-159">CustSettlementPriorityProcessing.getSettlementQuery</span></span>|
|<span data-ttu-id="b8d4b-160">CustSettlementPriorityProcessing.initCustTransOpen</span><span class="sxs-lookup"><span data-stu-id="b8d4b-160">CustSettlementPriorityProcessing.initCustTransOpen</span></span>|
|<span data-ttu-id="b8d4b-161">CustSettlementPriorityProcessing.insertAllLinesAccrossInvoices</span><span class="sxs-lookup"><span data-stu-id="b8d4b-161">CustSettlementPriorityProcessing.insertAllLinesAccrossInvoices</span></span>|
|<span data-ttu-id="b8d4b-162">CustSettlementPriorityProcessing.markTransactions</span><span class="sxs-lookup"><span data-stu-id="b8d4b-162">CustSettlementPriorityProcessing.markTransactions</span></span>|
|<span data-ttu-id="b8d4b-163">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span><span class="sxs-lookup"><span data-stu-id="b8d4b-163">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span></span>|
|<span data-ttu-id="b8d4b-164">CustSettlementPriorityProcessing.validateMarkedTransactionOpenTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-164">CustSettlementPriorityProcessing.validateMarkedTransactionOpenTrans</span></span>|
|<span data-ttu-id="b8d4b-165">CustStatisticsUS - メソッド calcStatistics</span><span class="sxs-lookup"><span data-stu-id="b8d4b-165">CustStatisticsUS - method calcStatistics</span></span>|
|<span data-ttu-id="b8d4b-166">CustTable.validateCNPJCPF_BR</span><span class="sxs-lookup"><span data-stu-id="b8d4b-166">CustTable.validateCNPJCPF_BR</span></span>|
|<span data-ttu-id="b8d4b-167">CustTrans.checkReversal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-167">CustTrans.checkReversal</span></span>|
|<span data-ttu-id="b8d4b-168">CustVendCheque.processChequeNum</span><span class="sxs-lookup"><span data-stu-id="b8d4b-168">CustVendCheque.processChequeNum</span></span>|
|<span data-ttu-id="b8d4b-169">CustVendCreatePaymJournal_Vend.searchTransactions</span><span class="sxs-lookup"><span data-stu-id="b8d4b-169">CustVendCreatePaymJournal_Vend.searchTransactions</span></span>|
|<span data-ttu-id="b8d4b-170">CustVendExchAdjPostingEngine.addExchangeAdjustment</span><span class="sxs-lookup"><span data-stu-id="b8d4b-170">CustVendExchAdjPostingEngine.addExchangeAdjustment</span></span>|
|<span data-ttu-id="b8d4b-171">CustVendFindSettlements.getTmpTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-171">CustVendFindSettlements.getTmpTrans</span></span>|
|<span data-ttu-id="b8d4b-172">CustVendPaymProposalTransferToJournal.transferProposalLineToJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-172">CustVendPaymProposalTransferToJournal.transferProposalLineToJournal</span></span>|
|<span data-ttu-id="b8d4b-173">CustVendSettle.createSummaryAccountReliefTransactions</span><span class="sxs-lookup"><span data-stu-id="b8d4b-173">CustVendSettle.createSummaryAccountReliefTransactions</span></span>|
|<span data-ttu-id="b8d4b-174">CustVendSettle.mustOffsetOriginalSummaryDistributions</span><span class="sxs-lookup"><span data-stu-id="b8d4b-174">CustVendSettle.mustOffsetOriginalSummaryDistributions</span></span>|
|<span data-ttu-id="b8d4b-175">CustVendSettle.postingProfileSettle_CreateDistributions</span><span class="sxs-lookup"><span data-stu-id="b8d4b-175">CustVendSettle.postingProfileSettle_CreateDistributions</span></span>|
|<span data-ttu-id="b8d4b-176">CustVendSettle.settleNow</span><span class="sxs-lookup"><span data-stu-id="b8d4b-176">CustVendSettle.settleNow</span></span>|
|<span data-ttu-id="b8d4b-177">CustVendTransDistributionController.getDistributionFactorsForPostingTypes</span><span class="sxs-lookup"><span data-stu-id="b8d4b-177">CustVendTransDistributionController.getDistributionFactorsForPostingTypes</span></span>|
|<span data-ttu-id="b8d4b-178">CustVendTransExchAdjDistController.getDistributionFactorsForPostingTypes</span><span class="sxs-lookup"><span data-stu-id="b8d4b-178">CustVendTransExchAdjDistController.getDistributionFactorsForPostingTypes</span></span>|
|<span data-ttu-id="b8d4b-179">CustVendTransSettle.post</span><span class="sxs-lookup"><span data-stu-id="b8d4b-179">CustVendTransSettle.post</span></span>|
|<span data-ttu-id="b8d4b-180">CustVendVoucher.initLedgerPosting</span><span class="sxs-lookup"><span data-stu-id="b8d4b-180">CustVendVoucher.initLedgerPosting</span></span>|
|<span data-ttu-id="b8d4b-181">CustWriteOff.createInterestWriteOffJournalForInterestTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-181">CustWriteOff.createInterestWriteOffJournalForInterestTrans</span></span>|
|<span data-ttu-id="b8d4b-182">DataFileImportExportUtils.readStreamWriterAndWriteToStreamWriter</span><span class="sxs-lookup"><span data-stu-id="b8d4b-182">DataFileImportExportUtils.readStreamWriterAndWriteToStreamWriter</span></span>|
|<span data-ttu-id="b8d4b-183">EcoResProductCreate.initDefaultControlValues</span><span class="sxs-lookup"><span data-stu-id="b8d4b-183">EcoResProductCreate.initDefaultControlValues</span></span>|
|<span data-ttu-id="b8d4b-184">EcoResProductReleaseManager.releaseToLegalEntity</span><span class="sxs-lookup"><span data-stu-id="b8d4b-184">EcoResProductReleaseManager.releaseToLegalEntity</span></span>|
|<span data-ttu-id="b8d4b-185">ExchangeRateImportOperation.saveRates</span><span class="sxs-lookup"><span data-stu-id="b8d4b-185">ExchangeRateImportOperation.saveRates</span></span>|
|<span data-ttu-id="b8d4b-186">FormletterJournalCreate.newPurchJournalCreate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-186">FormletterJournalCreate.newPurchJournalCreate</span></span>|
|<span data-ttu-id="b8d4b-187">FulfillmentLineView.NewExtension</span><span class="sxs-lookup"><span data-stu-id="b8d4b-187">FulfillmentLineView.NewExtension</span></span>|
|<span data-ttu-id="b8d4b-188">InterCompanyPost.formLetterCollect</span><span class="sxs-lookup"><span data-stu-id="b8d4b-188">InterCompanyPost.formLetterCollect</span></span>|
|<span data-ttu-id="b8d4b-189">InventCostIndirectFinancial.remainingQty</span><span class="sxs-lookup"><span data-stu-id="b8d4b-189">InventCostIndirectFinancial.remainingQty</span></span>|
|<span data-ttu-id="b8d4b-190">InventCostItemDim.load</span><span class="sxs-lookup"><span data-stu-id="b8d4b-190">InventCostItemDim.load</span></span>|
|<span data-ttu-id="b8d4b-191">InventCostJournalIndirectCost > addTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-191">InventCostJournalIndirectCost > addTrans</span></span>|
|<span data-ttu-id="b8d4b-192">InventCostTrans.setRefTypeFromInventTransType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-192">InventCostTrans.setRefTypeFromInventTransType</span></span>|
|<span data-ttu-id="b8d4b-193">InventDimCtrl_Rep_Sales.initDimParmFormletter</span><span class="sxs-lookup"><span data-stu-id="b8d4b-193">InventDimCtrl_Rep_Sales.initDimParmFormletter</span></span>|
|<span data-ttu-id="b8d4b-194">InventDimCtrl_Rep_Sales.mustShowField</span><span class="sxs-lookup"><span data-stu-id="b8d4b-194">InventDimCtrl_Rep_Sales.mustShowField</span></span>|
|<span data-ttu-id="b8d4b-195">InventDimCtrl_Rep_Sales.reportStrItemId</span><span class="sxs-lookup"><span data-stu-id="b8d4b-195">InventDimCtrl_Rep_Sales.reportStrItemId</span></span>|
|<span data-ttu-id="b8d4b-196">InventDistinctProductOrderDefaultingController.construct</span><span class="sxs-lookup"><span data-stu-id="b8d4b-196">InventDistinctProductOrderDefaultingController.construct</span></span>|
|<span data-ttu-id="b8d4b-197">InventItemLocationCountingStatus.updateStopCountingJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-197">InventItemLocationCountingStatus.updateStopCountingJournal</span></span>|
|<span data-ttu-id="b8d4b-198">InventItemPriceActivationJob.activateCostSheetCalculationFactor</span><span class="sxs-lookup"><span data-stu-id="b8d4b-198">InventItemPriceActivationJob.activateCostSheetCalculationFactor</span></span>|
|<span data-ttu-id="b8d4b-199">InventJournalCheckPost_Movement.postTransLedgerMovement</span><span class="sxs-lookup"><span data-stu-id="b8d4b-199">InventJournalCheckPost_Movement.postTransLedgerMovement</span></span>|
|<span data-ttu-id="b8d4b-200">InventJournalFormTrans_Movement.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="b8d4b-200">InventJournalFormTrans_Movement.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="b8d4b-201">InventoryMainAccDimensionListProvider.ledgerPostingType2InventAccountType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-201">InventoryMainAccDimensionListProvider.ledgerPostingType2InventAccountType</span></span>|
|<span data-ttu-id="b8d4b-202">InventQualityOrderTable.setTestResult</span><span class="sxs-lookup"><span data-stu-id="b8d4b-202">InventQualityOrderTable.setTestResult</span></span>|
|<span data-ttu-id="b8d4b-203">InventSerial.init</span><span class="sxs-lookup"><span data-stu-id="b8d4b-203">InventSerial.init</span></span>|
|<span data-ttu-id="b8d4b-204">InventSumPhysicalSpec.setValueQty</span><span class="sxs-lookup"><span data-stu-id="b8d4b-204">InventSumPhysicalSpec.setValueQty</span></span>|
|<span data-ttu-id="b8d4b-205">InventTable.insertInventItemOrderSetup</span><span class="sxs-lookup"><span data-stu-id="b8d4b-205">InventTable.insertInventItemOrderSetup</span></span>|
|<span data-ttu-id="b8d4b-206">InventTrans.updateSumUp</span><span class="sxs-lookup"><span data-stu-id="b8d4b-206">InventTrans.updateSumUp</span></span>|
|<span data-ttu-id="b8d4b-207">InventTransferLine.updates</span><span class="sxs-lookup"><span data-stu-id="b8d4b-207">InventTransferLine.updates</span></span>|
|<span data-ttu-id="b8d4b-208">InventTransferUpd.beginLedger</span><span class="sxs-lookup"><span data-stu-id="b8d4b-208">InventTransferUpd.beginLedger</span></span>|
|<span data-ttu-id="b8d4b-209">InventTransIdSum.update</span><span class="sxs-lookup"><span data-stu-id="b8d4b-209">InventTransIdSum.update</span></span>|
|<span data-ttu-id="b8d4b-210">InventUpd_Estimated.updateFieldsChange</span><span class="sxs-lookup"><span data-stu-id="b8d4b-210">InventUpd_Estimated.updateFieldsChange</span></span>|
|<span data-ttu-id="b8d4b-211">InventUpd_Financial.updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="b8d4b-211">InventUpd_Financial.updateFinancialIssue</span></span>|
|<span data-ttu-id="b8d4b-212">InventUpd_Financial.updateNow</span><span class="sxs-lookup"><span data-stu-id="b8d4b-212">InventUpd_Financial.updateNow</span></span>|
|<span data-ttu-id="b8d4b-213">InventUpd_Physical.updatePhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="b8d4b-213">InventUpd_Physical.updatePhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="b8d4b-214">InventUpd_Registered.pickReleatedIssueTransMore</span><span class="sxs-lookup"><span data-stu-id="b8d4b-214">InventUpd_Registered.pickReleatedIssueTransMore</span></span>|
|<span data-ttu-id="b8d4b-215">InventUpd_Reservation.updateReserveMore</span><span class="sxs-lookup"><span data-stu-id="b8d4b-215">InventUpd_Reservation.updateReserveMore</span></span>|
|<span data-ttu-id="b8d4b-216">InventUpdateMarking.updateReservations</span><span class="sxs-lookup"><span data-stu-id="b8d4b-216">InventUpdateMarking.updateReservations</span></span>|
|<span data-ttu-id="b8d4b-217">JmgAbsenceCalendar</span><span class="sxs-lookup"><span data-stu-id="b8d4b-217">JmgAbsenceCalendar</span></span>|
|<span data-ttu-id="b8d4b-218">JmgMESSwitchCode.init</span><span class="sxs-lookup"><span data-stu-id="b8d4b-218">JmgMESSwitchCode.init</span></span>|
|<span data-ttu-id="b8d4b-219">LedgerExchAdj.postAdjustment</span><span class="sxs-lookup"><span data-stu-id="b8d4b-219">LedgerExchAdj.postAdjustment</span></span>|
|<span data-ttu-id="b8d4b-220">LedgerExchAdj.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-220">LedgerExchAdj.run</span></span>|
|<span data-ttu-id="b8d4b-221">LedgerJournalEngine.initTaxGroup</span><span class="sxs-lookup"><span data-stu-id="b8d4b-221">LedgerJournalEngine.initTaxGroup</span></span>|
|<span data-ttu-id="b8d4b-222">LedgerJournalEngine_CustBillSettle.initCustOffsetAccount</span><span class="sxs-lookup"><span data-stu-id="b8d4b-222">LedgerJournalEngine_CustBillSettle.initCustOffsetAccount</span></span>|
|<span data-ttu-id="b8d4b-223">LedgerJournalTransCustPaym.LedgerJournalTrans.CustVendBankAccountId.jumpRef</span><span class="sxs-lookup"><span data-stu-id="b8d4b-223">LedgerJournalTransCustPaym.LedgerJournalTrans.CustVendBankAccountId.jumpRef</span></span>|
|<span data-ttu-id="b8d4b-224">LedgerJournalTransUpdateCust</span><span class="sxs-lookup"><span data-stu-id="b8d4b-224">LedgerJournalTransUpdateCust</span></span>|
|<span data-ttu-id="b8d4b-225">LedgerJournalTransUpdateLedger.updateNow</span><span class="sxs-lookup"><span data-stu-id="b8d4b-225">LedgerJournalTransUpdateLedger.updateNow</span></span>|
|<span data-ttu-id="b8d4b-226">LogisticsPostalAddress.whsAddressFormatValidation</span><span class="sxs-lookup"><span data-stu-id="b8d4b-226">LogisticsPostalAddress.whsAddressFormatValidation</span></span>|
|<span data-ttu-id="b8d4b-227">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span><span class="sxs-lookup"><span data-stu-id="b8d4b-227">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span></span>|
|<span data-ttu-id="b8d4b-228">Markup.calc</span><span class="sxs-lookup"><span data-stu-id="b8d4b-228">Markup.calc</span></span>|
|<span data-ttu-id="b8d4b-229">MCRCustPaym.ValidateWrite</span><span class="sxs-lookup"><span data-stu-id="b8d4b-229">MCRCustPaym.ValidateWrite</span></span>|
|<span data-ttu-id="b8d4b-230">McrCustPaymTotals_Sales.allPaymentsSubmitted</span><span class="sxs-lookup"><span data-stu-id="b8d4b-230">McrCustPaymTotals_Sales.allPaymentsSubmitted</span></span>|
|<span data-ttu-id="b8d4b-231">OffsetVoucher.updateNow</span><span class="sxs-lookup"><span data-stu-id="b8d4b-231">OffsetVoucher.updateNow</span></span>|
|<span data-ttu-id="b8d4b-232">PmfCoByProdCalcTrans.updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="b8d4b-232">PmfCoByProdCalcTrans.updateRealCalcIndirect</span></span>|
|<span data-ttu-id="b8d4b-233">PmfCoByProdCalcTrans.updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="b8d4b-233">PmfCoByProdCalcTrans.updateRealCalcIndirect</span></span>|
|<span data-ttu-id="b8d4b-234">POSAPIdts.New トリガー</span><span class="sxs-lookup"><span data-stu-id="b8d4b-234">POSAPIdts.New Trigger</span></span>|
|<span data-ttu-id="b8d4b-235">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span><span class="sxs-lookup"><span data-stu-id="b8d4b-235">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span></span>|
|<span data-ttu-id="b8d4b-236">PriceDiscAdmTrans.canEditPriceDiscValueField</span><span class="sxs-lookup"><span data-stu-id="b8d4b-236">PriceDiscAdmTrans.canEditPriceDiscValueField</span></span>|
|<span data-ttu-id="b8d4b-237">ProcCategoryHierarchyManagement.init</span><span class="sxs-lookup"><span data-stu-id="b8d4b-237">ProcCategoryHierarchyManagement.init</span></span>|
|<span data-ttu-id="b8d4b-238">ProdCalcTrans > メソッド updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="b8d4b-238">ProdCalcTrans > method updateRealCalcIndirect</span></span>|
|<span data-ttu-id="b8d4b-239">ProdIndirectTrans > メソッド type2ItemCalcType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-239">ProdIndirectTrans > method type2ItemCalcType</span></span>|
|<span data-ttu-id="b8d4b-240">ProdJournalCheckPostProd.postTransLedger</span><span class="sxs-lookup"><span data-stu-id="b8d4b-240">ProdJournalCheckPostProd.postTransLedger</span></span>|
|<span data-ttu-id="b8d4b-241">ProdTableForm.handleProdTableCreatePreSuper</span><span class="sxs-lookup"><span data-stu-id="b8d4b-241">ProdTableForm.handleProdTableCreatePreSuper</span></span>|
|<span data-ttu-id="b8d4b-242">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="b8d4b-242">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="b8d4b-243">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="b8d4b-243">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="b8d4b-244">ProjAdjustmentUpdate.deleteJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-244">ProjAdjustmentUpdate.deleteJournal</span></span>|
|<span data-ttu-id="b8d4b-245">ProjFundingLimitTrackingManager.updateUsingSourceDocument</span><span class="sxs-lookup"><span data-stu-id="b8d4b-245">ProjFundingLimitTrackingManager.updateUsingSourceDocument</span></span>|
|<span data-ttu-id="b8d4b-246">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-246">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="b8d4b-247">ProjInvoiceTableCreate.canClose</span><span class="sxs-lookup"><span data-stu-id="b8d4b-247">ProjInvoiceTableCreate.canClose</span></span>|
|<span data-ttu-id="b8d4b-248">ProjInvoiceTableCreate.initializeValues</span><span class="sxs-lookup"><span data-stu-id="b8d4b-248">ProjInvoiceTableCreate.initializeValues</span></span>|
|<span data-ttu-id="b8d4b-249">ProjPlanVersionsManager.createTemplateHierarchy</span><span class="sxs-lookup"><span data-stu-id="b8d4b-249">ProjPlanVersionsManager.createTemplateHierarchy</span></span>|
|<span data-ttu-id="b8d4b-250">ProjPostCostJournal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-250">ProjPostCostJournal.projTransCreate</span></span>|
|<span data-ttu-id="b8d4b-251">ProjSalesItemReq.SalesLine.linkActive</span><span class="sxs-lookup"><span data-stu-id="b8d4b-251">ProjSalesItemReq.SalesLine.linkActive</span></span>|
|<span data-ttu-id="b8d4b-252">ProjTableType_TimeMaterial.validateWrite</span><span class="sxs-lookup"><span data-stu-id="b8d4b-252">ProjTableType_TimeMaterial.validateWrite</span></span>|
|<span data-ttu-id="b8d4b-253">PurchAgreement.applyQueryRanges</span><span class="sxs-lookup"><span data-stu-id="b8d4b-253">PurchAgreement.applyQueryRanges</span></span>|
|<span data-ttu-id="b8d4b-254">PurchApproveJournalPost.postPurgeLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="b8d4b-254">PurchApproveJournalPost.postPurgeLedgerAccount</span></span>|
|<span data-ttu-id="b8d4b-255">PurchaseOrderResponseService.shouldPurchaseOrderBeAutoConfirmed</span><span class="sxs-lookup"><span data-stu-id="b8d4b-255">PurchaseOrderResponseService.shouldPurchaseOrderBeAutoConfirmed</span></span>|
|<span data-ttu-id="b8d4b-256">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-256">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="b8d4b-257">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-257">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="b8d4b-258">PurchAutoCreate_Sales.createLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-258">PurchAutoCreate_Sales.createLine</span></span>|
|<span data-ttu-id="b8d4b-259">PurchCalcTax.construct</span><span class="sxs-lookup"><span data-stu-id="b8d4b-259">PurchCalcTax.construct</span></span>|
|<span data-ttu-id="b8d4b-260">PurchCancel.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-260">PurchCancel.run</span></span>|
|<span data-ttu-id="b8d4b-261">PurchCreateFromOrder.insertMinMaxQty</span><span class="sxs-lookup"><span data-stu-id="b8d4b-261">PurchCreateFromOrder.insertMinMaxQty</span></span>|
|<span data-ttu-id="b8d4b-262">PurchCreateFromSalesOrder.insertIntoTmpPurchLinePrice</span><span class="sxs-lookup"><span data-stu-id="b8d4b-262">PurchCreateFromSalesOrder.insertIntoTmpPurchLinePrice</span></span>|
|<span data-ttu-id="b8d4b-263">PurchCreateFromSalesOrder.refreshCallerDataSource</span><span class="sxs-lookup"><span data-stu-id="b8d4b-263">PurchCreateFromSalesOrder.refreshCallerDataSource</span></span>|
|<span data-ttu-id="b8d4b-264">PurchCreateFromSalesOrder.Salesline.specifyMinMaxQty</span><span class="sxs-lookup"><span data-stu-id="b8d4b-264">PurchCreateFromSalesOrder.Salesline.specifyMinMaxQty</span></span>|
|<span data-ttu-id="b8d4b-265">PurchCreateFromSalesOrder.SalesLine.specifyVendAccount</span><span class="sxs-lookup"><span data-stu-id="b8d4b-265">PurchCreateFromSalesOrder.SalesLine.specifyVendAccount</span></span>|
|<span data-ttu-id="b8d4b-266">PurchCreateFromSalesOrder.validateSalesLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-266">PurchCreateFromSalesOrder.validateSalesLine</span></span>|
|<span data-ttu-id="b8d4b-267">PurchEditLines.canClose</span><span class="sxs-lookup"><span data-stu-id="b8d4b-267">PurchEditLines.canClose</span></span>|
|<span data-ttu-id="b8d4b-268">PurchEditLinesForm.construct</span><span class="sxs-lookup"><span data-stu-id="b8d4b-268">PurchEditLinesForm.construct</span></span>|
|<span data-ttu-id="b8d4b-269">PurchFormLetter.construct</span><span class="sxs-lookup"><span data-stu-id="b8d4b-269">PurchFormLetter.construct</span></span>|
|<span data-ttu-id="b8d4b-270">PurchFormLetterContract.newFromPackedVersion</span><span class="sxs-lookup"><span data-stu-id="b8d4b-270">PurchFormLetterContract.newFromPackedVersion</span></span>|
|<span data-ttu-id="b8d4b-271">PurchFormletterParmDataInvoice.selectFromJournalLines</span><span class="sxs-lookup"><span data-stu-id="b8d4b-271">PurchFormletterParmDataInvoice.selectFromJournalLines</span></span>|
|<span data-ttu-id="b8d4b-272">PurchFormLetterProvider.checkPurchLineChanged</span><span class="sxs-lookup"><span data-stu-id="b8d4b-272">PurchFormLetterProvider.checkPurchLineChanged</span></span>|
|<span data-ttu-id="b8d4b-273">PurchInvoiceJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-273">PurchInvoiceJournalPost.updateSourceLine</span></span>|
|<span data-ttu-id="b8d4b-274">PurchLine.checkInvoiceConstraints</span><span class="sxs-lookup"><span data-stu-id="b8d4b-274">PurchLine.checkInvoiceConstraints</span></span>|
|<span data-ttu-id="b8d4b-275">PurchLine.ledgerDimensionItem</span><span class="sxs-lookup"><span data-stu-id="b8d4b-275">PurchLine.ledgerDimensionItem</span></span>|
|<span data-ttu-id="b8d4b-276">PurchLine.ledgerDimensionReceipt</span><span class="sxs-lookup"><span data-stu-id="b8d4b-276">PurchLine.ledgerDimensionReceipt</span></span>|
|<span data-ttu-id="b8d4b-277">Purchline.unLinkAgreementLinePrompt</span><span class="sxs-lookup"><span data-stu-id="b8d4b-277">Purchline.unLinkAgreementLinePrompt</span></span>|
|<span data-ttu-id="b8d4b-278">PurchLine.validateField</span><span class="sxs-lookup"><span data-stu-id="b8d4b-278">PurchLine.validateField</span></span>|
|<span data-ttu-id="b8d4b-279">PurchLine::setProjSalesPrice</span><span class="sxs-lookup"><span data-stu-id="b8d4b-279">PurchLine::setProjSalesPrice</span></span>|
|<span data-ttu-id="b8d4b-280">PurchPrepayTable.updateAdvanceApplicationRemaining</span><span class="sxs-lookup"><span data-stu-id="b8d4b-280">PurchPrepayTable.updateAdvanceApplicationRemaining</span></span>|
|<span data-ttu-id="b8d4b-281">PurchPurchOrderJournalPost.updateSourceTable</span><span class="sxs-lookup"><span data-stu-id="b8d4b-281">PurchPurchOrderJournalPost.updateSourceTable</span></span>|
|<span data-ttu-id="b8d4b-282">PurchReqCreate.init</span><span class="sxs-lookup"><span data-stu-id="b8d4b-282">PurchReqCreate.init</span></span>|
|<span data-ttu-id="b8d4b-283">PurchReqLine.setDefaultDimension</span><span class="sxs-lookup"><span data-stu-id="b8d4b-283">PurchReqLine.setDefaultDimension</span></span>|
|<span data-ttu-id="b8d4b-284">PurchReqLine.validateWrite</span><span class="sxs-lookup"><span data-stu-id="b8d4b-284">PurchReqLine.validateWrite</span></span>|
|<span data-ttu-id="b8d4b-285">PurchReqTable.init</span><span class="sxs-lookup"><span data-stu-id="b8d4b-285">PurchReqTable.init</span></span>|
|<span data-ttu-id="b8d4b-286">PurchReqTableForm.new</span><span class="sxs-lookup"><span data-stu-id="b8d4b-286">PurchReqTableForm.new</span></span>|
|<span data-ttu-id="b8d4b-287">PurchRFQCaseTable.init</span><span class="sxs-lookup"><span data-stu-id="b8d4b-287">PurchRFQCaseTable.init</span></span>|
|<span data-ttu-id="b8d4b-288">PurchTable.jumpRefIntercompanySalesOrder</span><span class="sxs-lookup"><span data-stu-id="b8d4b-288">PurchTable.jumpRefIntercompanySalesOrder</span></span>|
|<span data-ttu-id="b8d4b-289">PurchTableForm_DeliverySchedule.updatePurchLineTable</span><span class="sxs-lookup"><span data-stu-id="b8d4b-289">PurchTableForm_DeliverySchedule.updatePurchLineTable</span></span>|
|<span data-ttu-id="b8d4b-290">PurchTableInteraction.enableHeaderReceive</span><span class="sxs-lookup"><span data-stu-id="b8d4b-290">PurchTableInteraction.enableHeaderReceive</span></span>|
|<span data-ttu-id="b8d4b-291">PurchTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="b8d4b-291">PurchTableType.validateDelete</span></span>|
|<span data-ttu-id="b8d4b-292">PurchTableUpdateFromPurchReqLineMap.update</span><span class="sxs-lookup"><span data-stu-id="b8d4b-292">PurchTableUpdateFromPurchReqLineMap.update</span></span>|
|<span data-ttu-id="b8d4b-293">ReqTransPoMarkFirm.setPurchBuyerGroupId & updatePurchBuyerGroup</span><span class="sxs-lookup"><span data-stu-id="b8d4b-293">ReqTransPoMarkFirm.setPurchBuyerGroupId & updatePurchBuyerGroup</span></span>|
|<span data-ttu-id="b8d4b-294">RetailGroupMemberLineHelper.internalCreateOrUpdateOrRemoveRetailGroupMemberLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-294">RetailGroupMemberLineHelper.internalCreateOrUpdateOrRemoveRetailGroupMemberLine</span></span>|
|<span data-ttu-id="b8d4b-295">RetailLabelDP.insertTmpTable</span><span class="sxs-lookup"><span data-stu-id="b8d4b-295">RetailLabelDP.insertTmpTable</span></span>|
|<span data-ttu-id="b8d4b-296">SalesCalcAvailableDlvDates.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="b8d4b-296">SalesCalcAvailableDlvDates.mainOnServer</span></span>|
|<span data-ttu-id="b8d4b-297">SalesConfirmJournalPost.updateSourceTable</span><span class="sxs-lookup"><span data-stu-id="b8d4b-297">SalesConfirmJournalPost.updateSourceTable</span></span>|
|<span data-ttu-id="b8d4b-298">SalesCopying.editCopy</span><span class="sxs-lookup"><span data-stu-id="b8d4b-298">SalesCopying.editCopy</span></span>|
|<span data-ttu-id="b8d4b-299">SalesCopying.editMarkAll</span><span class="sxs-lookup"><span data-stu-id="b8d4b-299">SalesCopying.editMarkAll</span></span>|
|<span data-ttu-id="b8d4b-300">SalesCopying.initReturnOrderFromCustomer</span><span class="sxs-lookup"><span data-stu-id="b8d4b-300">SalesCopying.initReturnOrderFromCustomer</span></span>|
|<span data-ttu-id="b8d4b-301">SalesCreateQuotation.canClose</span><span class="sxs-lookup"><span data-stu-id="b8d4b-301">SalesCreateQuotation.canClose</span></span>|
|<span data-ttu-id="b8d4b-302">SalesDropShipmentCancel.removeMarking</span><span class="sxs-lookup"><span data-stu-id="b8d4b-302">SalesDropShipmentCancel.removeMarking</span></span>|
|<span data-ttu-id="b8d4b-303">SalesEditLines.canClose</span><span class="sxs-lookup"><span data-stu-id="b8d4b-303">SalesEditLines.canClose</span></span>|
|<span data-ttu-id="b8d4b-304">SalesFormletterParmData.reArrangeLines</span><span class="sxs-lookup"><span data-stu-id="b8d4b-304">SalesFormletterParmData.reArrangeLines</span></span>|
|<span data-ttu-id="b8d4b-305">SalesFormletterParmData.reArrangeSplit</span><span class="sxs-lookup"><span data-stu-id="b8d4b-305">SalesFormletterParmData.reArrangeSplit</span></span>|
|<span data-ttu-id="b8d4b-306">SalesFormletterParmData.reArrangeSplit</span><span class="sxs-lookup"><span data-stu-id="b8d4b-306">SalesFormletterParmData.reArrangeSplit</span></span>|
|<span data-ttu-id="b8d4b-307">SalesFormLetterProvider.checkJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-307">SalesFormLetterProvider.checkJournal</span></span>|
|<span data-ttu-id="b8d4b-308">SalesInvoiceDP.insertGiroInformation</span><span class="sxs-lookup"><span data-stu-id="b8d4b-308">SalesInvoiceDP.insertGiroInformation</span></span>|
|<span data-ttu-id="b8d4b-309">SalesInvoiceJournalCreate.checkDocumentData_PL</span><span class="sxs-lookup"><span data-stu-id="b8d4b-309">SalesInvoiceJournalCreate.checkDocumentData_PL</span></span>|
|<span data-ttu-id="b8d4b-310">SalesInvoiceJournalPostBase.postLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-310">SalesInvoiceJournalPostBase.postLine</span></span>|
|<span data-ttu-id="b8d4b-311">SalesLine.resetInvent</span><span class="sxs-lookup"><span data-stu-id="b8d4b-311">SalesLine.resetInvent</span></span>|
|<span data-ttu-id="b8d4b-312">SalesLineType.initDimensionsSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="b8d4b-312">SalesLineType.initDimensionsSpecificDefaulting</span></span>|
|<span data-ttu-id="b8d4b-313">SalesLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="b8d4b-313">SalesLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="b8d4b-314">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="b8d4b-314">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="b8d4b-315">SalesPackingSlipJournalCreate.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-315">SalesPackingSlipJournalCreate.updateJournalLine</span></span>|
|<span data-ttu-id="b8d4b-316">SalesPackingSlipJournalCreate.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-316">SalesPackingSlipJournalCreate.updateJournalLine</span></span>|
|<span data-ttu-id="b8d4b-317">SalesPackingSlipJournalPost.insertBackorderLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-317">SalesPackingSlipJournalPost.insertBackorderLine</span></span>|
|<span data-ttu-id="b8d4b-318">SalesPackingSlipJournalPost.interCompanyPost</span><span class="sxs-lookup"><span data-stu-id="b8d4b-318">SalesPackingSlipJournalPost.interCompanyPost</span></span>|
|<span data-ttu-id="b8d4b-319">SalesPackingSlipJournalPost.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-319">SalesPackingSlipJournalPost.updateJournalLine</span></span>|
|<span data-ttu-id="b8d4b-320">SalesPurchSummaryModel_Account.createNewJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-320">SalesPurchSummaryModel_Account.createNewJournal</span></span>|
|<span data-ttu-id="b8d4b-321">SalesQuotationCalcTax_Sales.construct</span><span class="sxs-lookup"><span data-stu-id="b8d4b-321">SalesQuotationCalcTax_Sales.construct</span></span>|
|<span data-ttu-id="b8d4b-322">SalesQuotationEditLinesForm.postUpdate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-322">SalesQuotationEditLinesForm.postUpdate</span></span>|
|<span data-ttu-id="b8d4b-323">SalesQuotationLineType.initFromProjTable</span><span class="sxs-lookup"><span data-stu-id="b8d4b-323">SalesQuotationLineType.initFromProjTable</span></span>|
|<span data-ttu-id="b8d4b-324">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="b8d4b-324">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="b8d4b-325">SalesQuotationTable.modifiedField</span><span class="sxs-lookup"><span data-stu-id="b8d4b-325">SalesQuotationTable.modifiedField</span></span>|
|<span data-ttu-id="b8d4b-326">SalesQuotationTableForm.createFromTemplate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-326">SalesQuotationTableForm.createFromTemplate</span></span>|
|<span data-ttu-id="b8d4b-327">SalesQuotationUpdate_Cancelled.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-327">SalesQuotationUpdate_Cancelled.run</span></span>|
|<span data-ttu-id="b8d4b-328">SalesQuotationUpdate_Lost.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-328">SalesQuotationUpdate_Lost.run</span></span>|
|<span data-ttu-id="b8d4b-329">SalesTable.initFromCustTableMandatoryFields</span><span class="sxs-lookup"><span data-stu-id="b8d4b-329">SalesTable.initFromCustTableMandatoryFields</span></span>|
|<span data-ttu-id="b8d4b-330">SalesTable.jumpRefIntercompanyPurchaseOrder</span><span class="sxs-lookup"><span data-stu-id="b8d4b-330">SalesTable.jumpRefIntercompanyPurchaseOrder</span></span>|
|<span data-ttu-id="b8d4b-331">SalesTable.setShipCarrierFromLogisticsLocation</span><span class="sxs-lookup"><span data-stu-id="b8d4b-331">SalesTable.setShipCarrierFromLogisticsLocation</span></span>|
|<span data-ttu-id="b8d4b-332">SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="b8d4b-332">SalesTable.update</span></span>|
|<span data-ttu-id="b8d4b-333">SalesTableForm.interCompanyAutoCreateOrders</span><span class="sxs-lookup"><span data-stu-id="b8d4b-333">SalesTableForm.interCompanyAutoCreateOrders</span></span>|
|<span data-ttu-id="b8d4b-334">SettlementPair.createSettlementForDebitOrCreditTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-334">SettlementPair.createSettlementForDebitOrCreditTrans</span></span>|
|<span data-ttu-id="b8d4b-335">SmaServiceFunctionLine_Transfer.createJournalLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-335">SmaServiceFunctionLine_Transfer.createJournalLine</span></span>|
|<span data-ttu-id="b8d4b-336">SmaServiceFunctionLine_Transfer.postJournalTransType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-336">SmaServiceFunctionLine_Transfer.postJournalTransType</span></span>|
|<span data-ttu-id="b8d4b-337">SmaServiceOrderCreate.createServiceOrderLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-337">SmaServiceOrderCreate.createServiceOrderLine</span></span>|
|<span data-ttu-id="b8d4b-338">SmaSubscriptionGenerator::postTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-338">SmaSubscriptionGenerator::postTrans</span></span>|
|<span data-ttu-id="b8d4b-339">smmBusRelTable.relation2Vendor</span><span class="sxs-lookup"><span data-stu-id="b8d4b-339">smmBusRelTable.relation2Vendor</span></span>|
|<span data-ttu-id="b8d4b-340">smmBusRelTable.updateQuotations</span><span class="sxs-lookup"><span data-stu-id="b8d4b-340">smmBusRelTable.updateQuotations</span></span>|
|<span data-ttu-id="b8d4b-341">SmmCampaignBroadcast::validate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-341">SmmCampaignBroadcast::validate</span></span>|
|<span data-ttu-id="b8d4b-342">SmmOpportunityStatusUpdate.updateOpportunity</span><span class="sxs-lookup"><span data-stu-id="b8d4b-342">SmmOpportunityStatusUpdate.updateOpportunity</span></span>|
|<span data-ttu-id="b8d4b-343">smmOpportunityTable\Methods\openQuotation</span><span class="sxs-lookup"><span data-stu-id="b8d4b-343">smmOpportunityTable\Methods\openQuotation</span></span>|
|<span data-ttu-id="b8d4b-344">SmmProjectCreate.createSingleProject</span><span class="sxs-lookup"><span data-stu-id="b8d4b-344">SmmProjectCreate.createSingleProject</span></span>|
|<span data-ttu-id="b8d4b-345">SmmProjectCreate.createSingleProject</span><span class="sxs-lookup"><span data-stu-id="b8d4b-345">SmmProjectCreate.createSingleProject</span></span>|
|<span data-ttu-id="b8d4b-346">SmmUpdateBusRel.updateFromVendTableSFA2</span><span class="sxs-lookup"><span data-stu-id="b8d4b-346">SmmUpdateBusRel.updateFromVendTableSFA2</span></span>|
|<span data-ttu-id="b8d4b-347">SubledgerJournalTransferController.run</span><span class="sxs-lookup"><span data-stu-id="b8d4b-347">SubledgerJournalTransferController.run</span></span>|
|<span data-ttu-id="b8d4b-348">SuppItem.calcSuppItem</span><span class="sxs-lookup"><span data-stu-id="b8d4b-348">SuppItem.calcSuppItem</span></span>|
|<span data-ttu-id="b8d4b-349">SuppItem::newSuppItem</span><span class="sxs-lookup"><span data-stu-id="b8d4b-349">SuppItem::newSuppItem</span></span>|
|<span data-ttu-id="b8d4b-350">SuppItemCreate::newSuppItemCreate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-350">SuppItemCreate::newSuppItemCreate</span></span>|
|<span data-ttu-id="b8d4b-351">Tax.post</span><span class="sxs-lookup"><span data-stu-id="b8d4b-351">Tax.post</span></span>|
|<span data-ttu-id="b8d4b-352">Tax.saveAndPost</span><span class="sxs-lookup"><span data-stu-id="b8d4b-352">Tax.saveAndPost</span></span>|
|<span data-ttu-id="b8d4b-353">TaxFreeInvoice_Invoice.updateAndPost</span><span class="sxs-lookup"><span data-stu-id="b8d4b-353">TaxFreeInvoice_Invoice.updateAndPost</span></span>|
|<span data-ttu-id="b8d4b-354">TaxPost.moveTaxLineToNewOwner</span><span class="sxs-lookup"><span data-stu-id="b8d4b-354">TaxPost.moveTaxLineToNewOwner</span></span>|
|<span data-ttu-id="b8d4b-355">TaxPost.saveAndPostFromTmpTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-355">TaxPost.saveAndPostFromTmpTaxWorkTrans</span></span>|
|<span data-ttu-id="b8d4b-356">TaxPost.saveAndPostFromTmpTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-356">TaxPost.saveAndPostFromTmpTaxWorkTrans</span></span>|
|<span data-ttu-id="b8d4b-357">TaxVoucherService.postTaxOnErrorAccount</span><span class="sxs-lookup"><span data-stu-id="b8d4b-357">TaxVoucherService.postTaxOnErrorAccount</span></span>|
|<span data-ttu-id="b8d4b-358">TradePackingSlipJourChain.createRelationship</span><span class="sxs-lookup"><span data-stu-id="b8d4b-358">TradePackingSlipJourChain.createRelationship</span></span>|
|<span data-ttu-id="b8d4b-359">TradeTotals.calc</span><span class="sxs-lookup"><span data-stu-id="b8d4b-359">TradeTotals.calc</span></span>|
|<span data-ttu-id="b8d4b-360">TradeTotals.updateOrderBalances</span><span class="sxs-lookup"><span data-stu-id="b8d4b-360">TradeTotals.updateOrderBalances</span></span>|
|<span data-ttu-id="b8d4b-361">VendAccountStatementIntDP.processReport</span><span class="sxs-lookup"><span data-stu-id="b8d4b-361">VendAccountStatementIntDP.processReport</span></span>|
|<span data-ttu-id="b8d4b-362">VendEditInvoice\DataSource\VendInvoiceInfoTable\Methods\write</span><span class="sxs-lookup"><span data-stu-id="b8d4b-362">VendEditInvoice\DataSource\VendInvoiceInfoTable\Methods\write</span></span>|
|<span data-ttu-id="b8d4b-363">VendInvoiceMatching.initExpectedValues</span><span class="sxs-lookup"><span data-stu-id="b8d4b-363">VendInvoiceMatching.initExpectedValues</span></span>|
|<span data-ttu-id="b8d4b-364">VendInvoiceWFParticipantProviderExpend.resolve</span><span class="sxs-lookup"><span data-stu-id="b8d4b-364">VendInvoiceWFParticipantProviderExpend.resolve</span></span>|
|<span data-ttu-id="b8d4b-365">VendOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-365">VendOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="b8d4b-366">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="b8d4b-366">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="b8d4b-367">VendPaymentJournalDP.insertDataFromLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-367">VendPaymentJournalDP.insertDataFromLedgerJournalTrans</span></span>|
|<span data-ttu-id="b8d4b-368">VendPaymentJournalDP.insertDataFromSpecTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-368">VendPaymentJournalDP.insertDataFromSpecTrans</span></span>|
|<span data-ttu-id="b8d4b-369">VendPromissoryNotePost.postNextStep</span><span class="sxs-lookup"><span data-stu-id="b8d4b-369">VendPromissoryNotePost.postNextStep</span></span>|
|<span data-ttu-id="b8d4b-370">VendProvisionalBalanceDP.calculateAmounts</span><span class="sxs-lookup"><span data-stu-id="b8d4b-370">VendProvisionalBalanceDP.calculateAmounts</span></span>|
|<span data-ttu-id="b8d4b-371">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="b8d4b-371">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="b8d4b-372">VendProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="b8d4b-372">VendProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="b8d4b-373">VendTransListDP.ProcessReport</span><span class="sxs-lookup"><span data-stu-id="b8d4b-373">VendTransListDP.ProcessReport</span></span>|
|<span data-ttu-id="b8d4b-374">VendVoucher.createInvoiceJournal</span><span class="sxs-lookup"><span data-stu-id="b8d4b-374">VendVoucher.createInvoiceJournal</span></span>|
|<span data-ttu-id="b8d4b-375">WHSDocumentRouting.printDocument</span><span class="sxs-lookup"><span data-stu-id="b8d4b-375">WHSDocumentRouting.printDocument</span></span>|
|<span data-ttu-id="b8d4b-376">WhsLoadLineInventTransValidator.checkLoadLineInventTransConsistencyOnInventoryUpdate</span><span class="sxs-lookup"><span data-stu-id="b8d4b-376">WhsLoadLineInventTransValidator.checkLoadLineInventTransConsistencyOnInventoryUpdate</span></span>|
|<span data-ttu-id="b8d4b-377">WHSLoadLineUpdater.initAndInsertLoadLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-377">WHSLoadLineUpdater.initAndInsertLoadLine</span></span>|
|<span data-ttu-id="b8d4b-378">WhsShipConfirm.createASNItems</span><span class="sxs-lookup"><span data-stu-id="b8d4b-378">WhsShipConfirm.createASNItems</span></span>|
|<span data-ttu-id="b8d4b-379">WhsWarehouseRelease.createLoadLines</span><span class="sxs-lookup"><span data-stu-id="b8d4b-379">WhsWarehouseRelease.createLoadLines</span></span>|
|<span data-ttu-id="b8d4b-380">WHSWorkExecute.executeShortPick</span><span class="sxs-lookup"><span data-stu-id="b8d4b-380">WHSWorkExecute.executeShortPick</span></span>|
|<span data-ttu-id="b8d4b-381">WHSWorkExecuteDisplayLPReceiving.displayForm</span><span class="sxs-lookup"><span data-stu-id="b8d4b-381">WHSWorkExecuteDisplayLPReceiving.displayForm</span></span>|
|<span data-ttu-id="b8d4b-382">WHSWorkExecuteDisplayLPReceiving.displayNextForm</span><span class="sxs-lookup"><span data-stu-id="b8d4b-382">WHSWorkExecuteDisplayLPReceiving.displayNextForm</span></span>|
|<span data-ttu-id="b8d4b-383">WHSWorkExecuteDisplayMovementByTemplate.displayForm</span><span class="sxs-lookup"><span data-stu-id="b8d4b-383">WHSWorkExecuteDisplayMovementByTemplate.displayForm</span></span>|
|<span data-ttu-id="b8d4b-384">WhsWorkExecuteForm.createLabel</span><span class="sxs-lookup"><span data-stu-id="b8d4b-384">WhsWorkExecuteForm.createLabel</span></span>|
|<span data-ttu-id="b8d4b-385">WmsJournalCheckPostReception.postTrans</span><span class="sxs-lookup"><span data-stu-id="b8d4b-385">WmsJournalCheckPostReception.postTrans</span></span>|
|<span data-ttu-id="b8d4b-386">WmsOnlineCountingServer.getMovement</span><span class="sxs-lookup"><span data-stu-id="b8d4b-386">WmsOnlineCountingServer.getMovement</span></span>|
|<span data-ttu-id="b8d4b-387">WmsOnlineCountingServer.handleLine</span><span class="sxs-lookup"><span data-stu-id="b8d4b-387">WmsOnlineCountingServer.handleLine</span></span>|
|<span data-ttu-id="b8d4b-388">WmsOrderCreate.updateCreatewmsOrder</span><span class="sxs-lookup"><span data-stu-id="b8d4b-388">WmsOrderCreate.updateCreatewmsOrder</span></span>|
|<span data-ttu-id="b8d4b-389">WrkCtrResourceAbilityMapController.loadData</span><span class="sxs-lookup"><span data-stu-id="b8d4b-389">WrkCtrResourceAbilityMapController.loadData</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="b8d4b-390">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="b8d4b-390">Enumerations made extensible</span></span>

<span data-ttu-id="b8d4b-391">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-391">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="b8d4b-392">列挙型</span><span class="sxs-lookup"><span data-stu-id="b8d4b-392">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="b8d4b-393">ABCModel</span><span class="sxs-lookup"><span data-stu-id="b8d4b-393">ABCModel</span></span>|
|<span data-ttu-id="b8d4b-394">AccountOrder</span><span class="sxs-lookup"><span data-stu-id="b8d4b-394">AccountOrder</span></span>|
|<span data-ttu-id="b8d4b-395">AmountUnit</span><span class="sxs-lookup"><span data-stu-id="b8d4b-395">AmountUnit</span></span>|
|<span data-ttu-id="b8d4b-396">CostCalculationRateSubtype</span><span class="sxs-lookup"><span data-stu-id="b8d4b-396">CostCalculationRateSubtype</span></span>|
|<span data-ttu-id="b8d4b-397">CurrencyGainLossAccountType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-397">CurrencyGainLossAccountType</span></span>|
|<span data-ttu-id="b8d4b-398">CustInterestCodeSource</span><span class="sxs-lookup"><span data-stu-id="b8d4b-398">CustInterestCodeSource</span></span>|
|<span data-ttu-id="b8d4b-399">CustPaymentType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-399">CustPaymentType</span></span>|
|<span data-ttu-id="b8d4b-400">DirViewLocationNodeType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-400">DirViewLocationNodeType</span></span>|
|<span data-ttu-id="b8d4b-401">InterestCalcAccountChoice</span><span class="sxs-lookup"><span data-stu-id="b8d4b-401">InterestCalcAccountChoice</span></span>|
|<span data-ttu-id="b8d4b-402">InventTransPostingType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-402">InventTransPostingType</span></span>|
|<span data-ttu-id="b8d4b-403">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-403">MCRCustSearchType</span></span>|
|<span data-ttu-id="b8d4b-404">PaymentStub</span><span class="sxs-lookup"><span data-stu-id="b8d4b-404">PaymentStub</span></span>|
|<span data-ttu-id="b8d4b-405">PaymentStubInclAll</span><span class="sxs-lookup"><span data-stu-id="b8d4b-405">PaymentStubInclAll</span></span>|
|<span data-ttu-id="b8d4b-406">ProjCompletePrincip</span><span class="sxs-lookup"><span data-stu-id="b8d4b-406">ProjCompletePrincip</span></span>|
|<span data-ttu-id="b8d4b-407">ProjMatchingPrincip</span><span class="sxs-lookup"><span data-stu-id="b8d4b-407">ProjMatchingPrincip</span></span>|
|<span data-ttu-id="b8d4b-408">RetailPOSSeedDataType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-408">RetailPOSSeedDataType</span></span>|
|<span data-ttu-id="b8d4b-409">SalesQuotationStatus</span><span class="sxs-lookup"><span data-stu-id="b8d4b-409">SalesQuotationStatus</span></span>|
|<span data-ttu-id="b8d4b-410">TMSApptStatus</span><span class="sxs-lookup"><span data-stu-id="b8d4b-410">TMSApptStatus</span></span>|
|<span data-ttu-id="b8d4b-411">TMSCommunicationType</span><span class="sxs-lookup"><span data-stu-id="b8d4b-411">TMSCommunicationType</span></span>|

## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="b8d4b-412">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="b8d4b-412">Additional extensibility enhancements</span></span>

<span data-ttu-id="b8d4b-413">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-413">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="b8d4b-414">CustVendSettle: 変数をプライベートではなく保護に設定します。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-414">CustVendSettle: set variables protected instead of private.</span></span>
- <span data-ttu-id="b8d4b-415">イベントを引き起こさないデータ操作メソッド: WHSLocationDirective.loopLocDirLines。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-415">Data manipulation method not raising event: WHSLocationDirective.loopLocDirLines.</span></span>
- <span data-ttu-id="b8d4b-416">イベントを引き起こさないデータ操作メソッド: WhsWorkCreate.createTempLine。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-416">Data manipulation method not raising event: WhsWorkCreate.createTempLine.</span></span>
- <span data-ttu-id="b8d4b-417">マップ拡張: LogisticsPostalAddressMap。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-417">Map extension: LogisticsPostalAddressMap.</span></span>
- <span data-ttu-id="b8d4b-418">マップ拡張: PurchReqLineMap。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-418">Map extension: PurchReqLineMap.</span></span>
- <span data-ttu-id="b8d4b-419">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Is Public = Yes。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-419">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Is Public = Yes.</span></span>
- <span data-ttu-id="b8d4b-420">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Collection Name = ProjWBSActivityEstimates。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-420">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Public Collection Name = ProjWBSActivityEstimates.</span></span>
- <span data-ttu-id="b8d4b-421">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Entity Name = ProjWBSActivityEstimates</span><span class="sxs-lookup"><span data-stu-id="b8d4b-421">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Public Entity Name = ProjWBSActivityEstimates</span></span>
- <span data-ttu-id="b8d4b-422">メタデータの変更: /Data Model/Data Entities/EcoResProductAttributeValueEntity.IsPublic = Yes。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-422">Metadata change: /Data Model/Data Entities/EcoResProductAttributeValueEntity.IsPublic = Yes.</span></span>
- <span data-ttu-id="b8d4b-423">メタデータの変更: Form/WHSLoadPlanningListPage/FormDesign/FormDesign/FormActionPaneTabControl/ActionPaneTabShipReceive.Needed permission。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-423">Metadata change: Form/WHSLoadPlanningListPage/FormDesign/FormDesign/FormActionPaneTabControl/ActionPaneTabShipReceive.Needed permission.</span></span>
- <span data-ttu-id="b8d4b-424">メタデータの変更: WHSContainerLine, Relations WHSLoadLine & WHSShipmentTable.On Delete。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-424">Metadata change: WHSContainerLine, Relations WHSLoadLine & WHSShipmentTable.On Delete.</span></span>
- <span data-ttu-id="b8d4b-425">メタデータの変更: WHSContainerTable, Relation WHSShipmentTable.On Delete。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-425">Metadata change: WHSContainerTable, Relation WHSShipmentTable.On Delete.</span></span>
- <span data-ttu-id="b8d4b-426">プロジェクトの価格決定: 新しい価格決定検索メソッドの完全な取得。</span><span class="sxs-lookup"><span data-stu-id="b8d4b-426">Project pricing: complete uptake of new pricing find methods.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]