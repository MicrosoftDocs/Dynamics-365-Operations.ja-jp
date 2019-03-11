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
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-08-31
ms.dyn365.ops.version: App 8.0.4
ms.openlocfilehash: 906fac352834648508e8bb3fc2b7b076cca7c4b8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368931"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-804"></a><span data-ttu-id="025f7-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="025f7-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.4</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="025f7-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="025f7-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.4.</span></span> <span data-ttu-id="025f7-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025f7-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="025f7-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="025f7-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="025f7-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="025f7-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="025f7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="025f7-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="025f7-109">AgreementHeader.getModuleType</span><span class="sxs-lookup"><span data-stu-id="025f7-109">AgreementHeader.getModuleType</span></span>|
|<span data-ttu-id="025f7-110">AssetSplit.construct</span><span class="sxs-lookup"><span data-stu-id="025f7-110">AssetSplit.construct</span></span>|
|<span data-ttu-id="025f7-111">BankDepositSlipController.main</span><span class="sxs-lookup"><span data-stu-id="025f7-111">BankDepositSlipController.main</span></span>|
|<span data-ttu-id="025f7-112">BankPositivePayExport.sendFileToUser</span><span class="sxs-lookup"><span data-stu-id="025f7-112">BankPositivePayExport.sendFileToUser</span></span>|
|<span data-ttu-id="025f7-113">CaseDetailForm.getRecordsFromDataSource</span><span class="sxs-lookup"><span data-stu-id="025f7-113">CaseDetailForm.getRecordsFromDataSource</span></span>|
|<span data-ttu-id="025f7-114">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span><span class="sxs-lookup"><span data-stu-id="025f7-114">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span></span>|
|<span data-ttu-id="025f7-115">CostSheetNodeCalculation.validate</span><span class="sxs-lookup"><span data-stu-id="025f7-115">CostSheetNodeCalculation.validate</span></span>|
|<span data-ttu-id="025f7-116">CostSheetNodeCalculationRate.calcLowestLevel</span><span class="sxs-lookup"><span data-stu-id="025f7-116">CostSheetNodeCalculationRate.calcLowestLevel</span></span>|
|<span data-ttu-id="025f7-117">CostSheetNodeCalculationSurcharge.equal</span><span class="sxs-lookup"><span data-stu-id="025f7-117">CostSheetNodeCalculationSurcharge.equal</span></span>|
|<span data-ttu-id="025f7-118">CustAccountStatementExtController.processParty</span><span class="sxs-lookup"><span data-stu-id="025f7-118">CustAccountStatementExtController.processParty</span></span>|
|<span data-ttu-id="025f7-119">CustAccountStatementExtDP.insertNewRecords</span><span class="sxs-lookup"><span data-stu-id="025f7-119">CustAccountStatementExtDP.insertNewRecords</span></span>|
|<span data-ttu-id="025f7-120">CustAccountStatementExtDP.setSysDocuBrandDetails</span><span class="sxs-lookup"><span data-stu-id="025f7-120">CustAccountStatementExtDP.setSysDocuBrandDetails</span></span>|
|<span data-ttu-id="025f7-121">CustBillOfExchangePost.postNextStep</span><span class="sxs-lookup"><span data-stu-id="025f7-121">CustBillOfExchangePost.postNextStep</span></span>|
|<span data-ttu-id="025f7-122">CustBillOfExchangePostProtestHonored.postNextStep</span><span class="sxs-lookup"><span data-stu-id="025f7-122">CustBillOfExchangePostProtestHonored.postNextStep</span></span>|
|<span data-ttu-id="025f7-123">CustCollectionJourController.runPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="025f7-123">CustCollectionJourController.runPrintMgmt</span></span>|
|<span data-ttu-id="025f7-124">CustCollectionLetterCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-124">CustCollectionLetterCreate.createJournal</span></span>|
|<span data-ttu-id="025f7-125">CustCollectionLetterCreate.run</span><span class="sxs-lookup"><span data-stu-id="025f7-125">CustCollectionLetterCreate.run</span></span>|
|<span data-ttu-id="025f7-126">CustCollectionLetterNote.CustCollectionLetterJour.active</span><span class="sxs-lookup"><span data-stu-id="025f7-126">CustCollectionLetterNote.CustCollectionLetterJour.active</span></span>|
|<span data-ttu-id="025f7-127">CustCollectionLetterPost.processRow</span><span class="sxs-lookup"><span data-stu-id="025f7-127">CustCollectionLetterPost.processRow</span></span>|
|<span data-ttu-id="025f7-128">CustCollectionLetterPost.validateCollectionLetter</span><span class="sxs-lookup"><span data-stu-id="025f7-128">CustCollectionLetterPost.validateCollectionLetter</span></span>|
|<span data-ttu-id="025f7-129">CustFreeInvoiceCorrection.createInvoiceLines</span><span class="sxs-lookup"><span data-stu-id="025f7-129">CustFreeInvoiceCorrection.createInvoiceLines</span></span>|
|<span data-ttu-id="025f7-130">CustInterestPost.main</span><span class="sxs-lookup"><span data-stu-id="025f7-130">CustInterestPost.main</span></span>|
|<span data-ttu-id="025f7-131">CustInterestPost.validateInterestTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-131">CustInterestPost.validateInterestTrans</span></span>|
|<span data-ttu-id="025f7-132">CustInvoiceJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-132">CustInvoiceJour.printJournal</span></span>|
|<span data-ttu-id="025f7-133">CustInvoiceTable.calcDue</span><span class="sxs-lookup"><span data-stu-id="025f7-133">CustInvoiceTable.calcDue</span></span>|
|<span data-ttu-id="025f7-134">CustOpenBalanceCurrency.Data Sources – VendTrans – init</span><span class="sxs-lookup"><span data-stu-id="025f7-134">CustOpenBalanceCurrency.Data Sources – VendTrans – init</span></span>|
|<span data-ttu-id="025f7-135">CustOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-135">CustOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="025f7-136">CustPackingSlipJourFormHelper.areCancelCorrectButtonsEnabled</span><span class="sxs-lookup"><span data-stu-id="025f7-136">CustPackingSlipJourFormHelper.areCancelCorrectButtonsEnabled</span></span>|
|<span data-ttu-id="025f7-137">CustPaymEntry.editIsMarkedForSettlement</span><span class="sxs-lookup"><span data-stu-id="025f7-137">CustPaymEntry.editIsMarkedForSettlement</span></span>|
|<span data-ttu-id="025f7-138">CustPostInvoice.main</span><span class="sxs-lookup"><span data-stu-id="025f7-138">CustPostInvoice.main</span></span>|
|<span data-ttu-id="025f7-139">CustPostInvoice.run</span><span class="sxs-lookup"><span data-stu-id="025f7-139">CustPostInvoice.run</span></span>|
|<span data-ttu-id="025f7-140">CustPostInvoice.validate</span><span class="sxs-lookup"><span data-stu-id="025f7-140">CustPostInvoice.validate</span></span>|
|<span data-ttu-id="025f7-141">CustPostInvoiceJob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="025f7-141">CustPostInvoiceJob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="025f7-142">CustPostInvoiceJob.initializeCustPostProcess</span><span class="sxs-lookup"><span data-stu-id="025f7-142">CustPostInvoiceJob.initializeCustPostProcess</span></span>|
|<span data-ttu-id="025f7-143">CustPostInvoiceJob.main</span><span class="sxs-lookup"><span data-stu-id="025f7-143">CustPostInvoiceJob.main</span></span>|
|<span data-ttu-id="025f7-144">CustPostInvoiceJob.processCustPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="025f7-144">CustPostInvoiceJob.processCustPostInvoiceUpdate</span></span>|
|<span data-ttu-id="025f7-145">CustProvisionalBalanceDP.calculateAmounts</span><span class="sxs-lookup"><span data-stu-id="025f7-145">CustProvisionalBalanceDP.calculateAmounts</span></span>|
|<span data-ttu-id="025f7-146">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="025f7-146">CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="025f7-147">CustProvisionalBalanceDP.populateCustProvisionalBalanceTmpProcessing</span><span class="sxs-lookup"><span data-stu-id="025f7-147">CustProvisionalBalanceDP.populateCustProvisionalBalanceTmpProcessing</span></span>|
|<span data-ttu-id="025f7-148">CustProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="025f7-148">CustProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="025f7-149">CustProvisionalBalanceDP.translateMainAccountNamesOnCustProvisionalBalanceTmpProcessing</span><span class="sxs-lookup"><span data-stu-id="025f7-149">CustProvisionalBalanceDP.translateMainAccountNamesOnCustProvisionalBalanceTmpProcessing</span></span>|
|<span data-ttu-id="025f7-150">CustQuotationJournal.launchReport</span><span class="sxs-lookup"><span data-stu-id="025f7-150">CustQuotationJournal.launchReport</span></span>|
|<span data-ttu-id="025f7-151">CustSettlementPriorityProcessing .createTempData</span><span class="sxs-lookup"><span data-stu-id="025f7-151">CustSettlementPriorityProcessing .createTempData</span></span>|
|<span data-ttu-id="025f7-152">CustSettlementPriorityProcessing .setPaymentAmount</span><span class="sxs-lookup"><span data-stu-id="025f7-152">CustSettlementPriorityProcessing .setPaymentAmount</span></span>|
|<span data-ttu-id="025f7-153">CustSettlementPriorityProcessing .updatePartialTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-153">CustSettlementPriorityProcessing .updatePartialTrans</span></span>|
|<span data-ttu-id="025f7-154">CustSettlementPriorityProcessing.classDeclaration</span><span class="sxs-lookup"><span data-stu-id="025f7-154">CustSettlementPriorityProcessing.classDeclaration</span></span>|
|<span data-ttu-id="025f7-155">CustSettlementPriorityProcessing.constructCustOpenTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-155">CustSettlementPriorityProcessing.constructCustOpenTrans</span></span>|
|<span data-ttu-id="025f7-156">CustSettlementPriorityProcessing.constructCustPaymEntry</span><span class="sxs-lookup"><span data-stu-id="025f7-156">CustSettlementPriorityProcessing.constructCustPaymEntry</span></span>|
|<span data-ttu-id="025f7-157">CustSettlementPriorityProcessing.constructOffsetVoucherCust</span><span class="sxs-lookup"><span data-stu-id="025f7-157">CustSettlementPriorityProcessing.constructOffsetVoucherCust</span></span>|
|<span data-ttu-id="025f7-158">CustSettlementPriorityProcessing.getBillingPriorities</span><span class="sxs-lookup"><span data-stu-id="025f7-158">CustSettlementPriorityProcessing.getBillingPriorities</span></span>|
|<span data-ttu-id="025f7-159">CustSettlementPriorityProcessing.getSettlementQuery</span><span class="sxs-lookup"><span data-stu-id="025f7-159">CustSettlementPriorityProcessing.getSettlementQuery</span></span>|
|<span data-ttu-id="025f7-160">CustSettlementPriorityProcessing.initCustTransOpen</span><span class="sxs-lookup"><span data-stu-id="025f7-160">CustSettlementPriorityProcessing.initCustTransOpen</span></span>|
|<span data-ttu-id="025f7-161">CustSettlementPriorityProcessing.insertAllLinesAccrossInvoices</span><span class="sxs-lookup"><span data-stu-id="025f7-161">CustSettlementPriorityProcessing.insertAllLinesAccrossInvoices</span></span>|
|<span data-ttu-id="025f7-162">CustSettlementPriorityProcessing.markTransactions</span><span class="sxs-lookup"><span data-stu-id="025f7-162">CustSettlementPriorityProcessing.markTransactions</span></span>|
|<span data-ttu-id="025f7-163">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span><span class="sxs-lookup"><span data-stu-id="025f7-163">CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses</span></span>|
|<span data-ttu-id="025f7-164">CustSettlementPriorityProcessing.validateMarkedTransactionOpenTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-164">CustSettlementPriorityProcessing.validateMarkedTransactionOpenTrans</span></span>|
|<span data-ttu-id="025f7-165">CustStatisticsUS - メソッド calcStatistics</span><span class="sxs-lookup"><span data-stu-id="025f7-165">CustStatisticsUS - method calcStatistics</span></span>|
|<span data-ttu-id="025f7-166">CustTable.validateCNPJCPF_BR</span><span class="sxs-lookup"><span data-stu-id="025f7-166">CustTable.validateCNPJCPF_BR</span></span>|
|<span data-ttu-id="025f7-167">CustTrans.checkReversal</span><span class="sxs-lookup"><span data-stu-id="025f7-167">CustTrans.checkReversal</span></span>|
|<span data-ttu-id="025f7-168">CustVendCheque.processChequeNum</span><span class="sxs-lookup"><span data-stu-id="025f7-168">CustVendCheque.processChequeNum</span></span>|
|<span data-ttu-id="025f7-169">CustVendCreatePaymJournal_Vend.searchTransactions</span><span class="sxs-lookup"><span data-stu-id="025f7-169">CustVendCreatePaymJournal_Vend.searchTransactions</span></span>|
|<span data-ttu-id="025f7-170">CustVendExchAdjPostingEngine.addExchangeAdjustment</span><span class="sxs-lookup"><span data-stu-id="025f7-170">CustVendExchAdjPostingEngine.addExchangeAdjustment</span></span>|
|<span data-ttu-id="025f7-171">CustVendFindSettlements.getTmpTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-171">CustVendFindSettlements.getTmpTrans</span></span>|
|<span data-ttu-id="025f7-172">CustVendPaymProposalTransferToJournal.transferProposalLineToJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-172">CustVendPaymProposalTransferToJournal.transferProposalLineToJournal</span></span>|
|<span data-ttu-id="025f7-173">CustVendSettle.createSummaryAccountReliefTransactions</span><span class="sxs-lookup"><span data-stu-id="025f7-173">CustVendSettle.createSummaryAccountReliefTransactions</span></span>|
|<span data-ttu-id="025f7-174">CustVendSettle.mustOffsetOriginalSummaryDistributions</span><span class="sxs-lookup"><span data-stu-id="025f7-174">CustVendSettle.mustOffsetOriginalSummaryDistributions</span></span>|
|<span data-ttu-id="025f7-175">CustVendSettle.postingProfileSettle_CreateDistributions</span><span class="sxs-lookup"><span data-stu-id="025f7-175">CustVendSettle.postingProfileSettle_CreateDistributions</span></span>|
|<span data-ttu-id="025f7-176">CustVendSettle.settleNow</span><span class="sxs-lookup"><span data-stu-id="025f7-176">CustVendSettle.settleNow</span></span>|
|<span data-ttu-id="025f7-177">CustVendTransDistributionController.getDistributionFactorsForPostingTypes</span><span class="sxs-lookup"><span data-stu-id="025f7-177">CustVendTransDistributionController.getDistributionFactorsForPostingTypes</span></span>|
|<span data-ttu-id="025f7-178">CustVendTransExchAdjDistController.getDistributionFactorsForPostingTypes</span><span class="sxs-lookup"><span data-stu-id="025f7-178">CustVendTransExchAdjDistController.getDistributionFactorsForPostingTypes</span></span>|
|<span data-ttu-id="025f7-179">CustVendTransSettle.post</span><span class="sxs-lookup"><span data-stu-id="025f7-179">CustVendTransSettle.post</span></span>|
|<span data-ttu-id="025f7-180">CustVendVoucher.initLedgerPosting</span><span class="sxs-lookup"><span data-stu-id="025f7-180">CustVendVoucher.initLedgerPosting</span></span>|
|<span data-ttu-id="025f7-181">CustWriteOff.createInterestWriteOffJournalForInterestTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-181">CustWriteOff.createInterestWriteOffJournalForInterestTrans</span></span>|
|<span data-ttu-id="025f7-182">DataFileImportExportUtils.readStreamWriterAndWriteToStreamWriter</span><span class="sxs-lookup"><span data-stu-id="025f7-182">DataFileImportExportUtils.readStreamWriterAndWriteToStreamWriter</span></span>|
|<span data-ttu-id="025f7-183">EcoResProductCreate.initDefaultControlValues</span><span class="sxs-lookup"><span data-stu-id="025f7-183">EcoResProductCreate.initDefaultControlValues</span></span>|
|<span data-ttu-id="025f7-184">EcoResProductReleaseManager.releaseToLegalEntity</span><span class="sxs-lookup"><span data-stu-id="025f7-184">EcoResProductReleaseManager.releaseToLegalEntity</span></span>|
|<span data-ttu-id="025f7-185">ExchangeRateImportOperation.saveRates</span><span class="sxs-lookup"><span data-stu-id="025f7-185">ExchangeRateImportOperation.saveRates</span></span>|
|<span data-ttu-id="025f7-186">FormletterJournalCreate.newPurchJournalCreate</span><span class="sxs-lookup"><span data-stu-id="025f7-186">FormletterJournalCreate.newPurchJournalCreate</span></span>|
|<span data-ttu-id="025f7-187">FulfillmentLineView.NewExtension</span><span class="sxs-lookup"><span data-stu-id="025f7-187">FulfillmentLineView.NewExtension</span></span>|
|<span data-ttu-id="025f7-188">InterCompanyPost.formLetterCollect</span><span class="sxs-lookup"><span data-stu-id="025f7-188">InterCompanyPost.formLetterCollect</span></span>|
|<span data-ttu-id="025f7-189">InventCostIndirectFinancial.remainingQty</span><span class="sxs-lookup"><span data-stu-id="025f7-189">InventCostIndirectFinancial.remainingQty</span></span>|
|<span data-ttu-id="025f7-190">InventCostItemDim.load</span><span class="sxs-lookup"><span data-stu-id="025f7-190">InventCostItemDim.load</span></span>|
|<span data-ttu-id="025f7-191">InventCostJournalIndirectCost > addTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-191">InventCostJournalIndirectCost > addTrans</span></span>|
|<span data-ttu-id="025f7-192">InventCostTrans.setRefTypeFromInventTransType</span><span class="sxs-lookup"><span data-stu-id="025f7-192">InventCostTrans.setRefTypeFromInventTransType</span></span>|
|<span data-ttu-id="025f7-193">InventDimCtrl_Rep_Sales.initDimParmFormletter</span><span class="sxs-lookup"><span data-stu-id="025f7-193">InventDimCtrl_Rep_Sales.initDimParmFormletter</span></span>|
|<span data-ttu-id="025f7-194">InventDimCtrl_Rep_Sales.mustShowField</span><span class="sxs-lookup"><span data-stu-id="025f7-194">InventDimCtrl_Rep_Sales.mustShowField</span></span>|
|<span data-ttu-id="025f7-195">InventDimCtrl_Rep_Sales.reportStrItemId</span><span class="sxs-lookup"><span data-stu-id="025f7-195">InventDimCtrl_Rep_Sales.reportStrItemId</span></span>|
|<span data-ttu-id="025f7-196">InventDistinctProductOrderDefaultingController.construct</span><span class="sxs-lookup"><span data-stu-id="025f7-196">InventDistinctProductOrderDefaultingController.construct</span></span>|
|<span data-ttu-id="025f7-197">InventItemLocationCountingStatus.updateStopCountingJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-197">InventItemLocationCountingStatus.updateStopCountingJournal</span></span>|
|<span data-ttu-id="025f7-198">InventItemPriceActivationJob.activateCostSheetCalculationFactor</span><span class="sxs-lookup"><span data-stu-id="025f7-198">InventItemPriceActivationJob.activateCostSheetCalculationFactor</span></span>|
|<span data-ttu-id="025f7-199">InventJournalCheckPost_Movement.postTransLedgerMovement</span><span class="sxs-lookup"><span data-stu-id="025f7-199">InventJournalCheckPost_Movement.postTransLedgerMovement</span></span>|
|<span data-ttu-id="025f7-200">InventJournalFormTrans_Movement.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="025f7-200">InventJournalFormTrans_Movement.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="025f7-201">InventoryMainAccDimensionListProvider.ledgerPostingType2InventAccountType</span><span class="sxs-lookup"><span data-stu-id="025f7-201">InventoryMainAccDimensionListProvider.ledgerPostingType2InventAccountType</span></span>|
|<span data-ttu-id="025f7-202">InventQualityOrderTable.setTestResult</span><span class="sxs-lookup"><span data-stu-id="025f7-202">InventQualityOrderTable.setTestResult</span></span>|
|<span data-ttu-id="025f7-203">InventSerial.init</span><span class="sxs-lookup"><span data-stu-id="025f7-203">InventSerial.init</span></span>|
|<span data-ttu-id="025f7-204">InventSumPhysicalSpec.setValueQty</span><span class="sxs-lookup"><span data-stu-id="025f7-204">InventSumPhysicalSpec.setValueQty</span></span>|
|<span data-ttu-id="025f7-205">InventTable.insertInventItemOrderSetup</span><span class="sxs-lookup"><span data-stu-id="025f7-205">InventTable.insertInventItemOrderSetup</span></span>|
|<span data-ttu-id="025f7-206">InventTrans.updateSumUp</span><span class="sxs-lookup"><span data-stu-id="025f7-206">InventTrans.updateSumUp</span></span>|
|<span data-ttu-id="025f7-207">InventTransferLine.updates</span><span class="sxs-lookup"><span data-stu-id="025f7-207">InventTransferLine.updates</span></span>|
|<span data-ttu-id="025f7-208">InventTransferUpd.beginLedger</span><span class="sxs-lookup"><span data-stu-id="025f7-208">InventTransferUpd.beginLedger</span></span>|
|<span data-ttu-id="025f7-209">InventTransIdSum.update</span><span class="sxs-lookup"><span data-stu-id="025f7-209">InventTransIdSum.update</span></span>|
|<span data-ttu-id="025f7-210">InventUpd_Estimated.updateFieldsChange</span><span class="sxs-lookup"><span data-stu-id="025f7-210">InventUpd_Estimated.updateFieldsChange</span></span>|
|<span data-ttu-id="025f7-211">InventUpd_Financial.updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="025f7-211">InventUpd_Financial.updateFinancialIssue</span></span>|
|<span data-ttu-id="025f7-212">InventUpd_Financial.updateNow</span><span class="sxs-lookup"><span data-stu-id="025f7-212">InventUpd_Financial.updateNow</span></span>|
|<span data-ttu-id="025f7-213">InventUpd_Physical.updatePhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="025f7-213">InventUpd_Physical.updatePhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="025f7-214">InventUpd_Registered.pickReleatedIssueTransMore</span><span class="sxs-lookup"><span data-stu-id="025f7-214">InventUpd_Registered.pickReleatedIssueTransMore</span></span>|
|<span data-ttu-id="025f7-215">InventUpd_Reservation.updateReserveMore</span><span class="sxs-lookup"><span data-stu-id="025f7-215">InventUpd_Reservation.updateReserveMore</span></span>|
|<span data-ttu-id="025f7-216">InventUpdateMarking.updateReservations</span><span class="sxs-lookup"><span data-stu-id="025f7-216">InventUpdateMarking.updateReservations</span></span>|
|<span data-ttu-id="025f7-217">JmgAbsenceCalendar</span><span class="sxs-lookup"><span data-stu-id="025f7-217">JmgAbsenceCalendar</span></span>|
|<span data-ttu-id="025f7-218">JmgMESSwitchCode.init</span><span class="sxs-lookup"><span data-stu-id="025f7-218">JmgMESSwitchCode.init</span></span>|
|<span data-ttu-id="025f7-219">LedgerExchAdj.postAdjustment</span><span class="sxs-lookup"><span data-stu-id="025f7-219">LedgerExchAdj.postAdjustment</span></span>|
|<span data-ttu-id="025f7-220">LedgerExchAdj.run</span><span class="sxs-lookup"><span data-stu-id="025f7-220">LedgerExchAdj.run</span></span>|
|<span data-ttu-id="025f7-221">LedgerJournalEngine.initTaxGroup</span><span class="sxs-lookup"><span data-stu-id="025f7-221">LedgerJournalEngine.initTaxGroup</span></span>|
|<span data-ttu-id="025f7-222">LedgerJournalEngine_CustBillSettle.initCustOffsetAccount</span><span class="sxs-lookup"><span data-stu-id="025f7-222">LedgerJournalEngine_CustBillSettle.initCustOffsetAccount</span></span>|
|<span data-ttu-id="025f7-223">LedgerJournalTransCustPaym.LedgerJournalTrans.CustVendBankAccountId.jumpRef</span><span class="sxs-lookup"><span data-stu-id="025f7-223">LedgerJournalTransCustPaym.LedgerJournalTrans.CustVendBankAccountId.jumpRef</span></span>|
|<span data-ttu-id="025f7-224">LedgerJournalTransUpdateCust</span><span class="sxs-lookup"><span data-stu-id="025f7-224">LedgerJournalTransUpdateCust</span></span>|
|<span data-ttu-id="025f7-225">LedgerJournalTransUpdateLedger.updateNow</span><span class="sxs-lookup"><span data-stu-id="025f7-225">LedgerJournalTransUpdateLedger.updateNow</span></span>|
|<span data-ttu-id="025f7-226">LogisticsPostalAddress.whsAddressFormatValidation</span><span class="sxs-lookup"><span data-stu-id="025f7-226">LogisticsPostalAddress.whsAddressFormatValidation</span></span>|
|<span data-ttu-id="025f7-227">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span><span class="sxs-lookup"><span data-stu-id="025f7-227">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span></span>|
|<span data-ttu-id="025f7-228">Markup.calc</span><span class="sxs-lookup"><span data-stu-id="025f7-228">Markup.calc</span></span>|
|<span data-ttu-id="025f7-229">MCRCustPaym.ValidateWrite</span><span class="sxs-lookup"><span data-stu-id="025f7-229">MCRCustPaym.ValidateWrite</span></span>|
|<span data-ttu-id="025f7-230">McrCustPaymTotals_Sales.allPaymentsSubmitted</span><span class="sxs-lookup"><span data-stu-id="025f7-230">McrCustPaymTotals_Sales.allPaymentsSubmitted</span></span>|
|<span data-ttu-id="025f7-231">OffsetVoucher.updateNow</span><span class="sxs-lookup"><span data-stu-id="025f7-231">OffsetVoucher.updateNow</span></span>|
|<span data-ttu-id="025f7-232">PmfCoByProdCalcTrans.updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="025f7-232">PmfCoByProdCalcTrans.updateRealCalcIndirect</span></span>|
|<span data-ttu-id="025f7-233">PmfCoByProdCalcTrans.updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="025f7-233">PmfCoByProdCalcTrans.updateRealCalcIndirect</span></span>|
|<span data-ttu-id="025f7-234">POSAPIdts.New トリガー</span><span class="sxs-lookup"><span data-stu-id="025f7-234">POSAPIdts.New Trigger</span></span>|
|<span data-ttu-id="025f7-235">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span><span class="sxs-lookup"><span data-stu-id="025f7-235">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span></span>|
|<span data-ttu-id="025f7-236">PriceDiscAdmTrans.canEditPriceDiscValueField</span><span class="sxs-lookup"><span data-stu-id="025f7-236">PriceDiscAdmTrans.canEditPriceDiscValueField</span></span>|
|<span data-ttu-id="025f7-237">ProcCategoryHierarchyManagement.init</span><span class="sxs-lookup"><span data-stu-id="025f7-237">ProcCategoryHierarchyManagement.init</span></span>|
|<span data-ttu-id="025f7-238">ProdCalcTrans > メソッド updateRealCalcIndirect</span><span class="sxs-lookup"><span data-stu-id="025f7-238">ProdCalcTrans > method updateRealCalcIndirect</span></span>|
|<span data-ttu-id="025f7-239">ProdIndirectTrans > メソッド type2ItemCalcType</span><span class="sxs-lookup"><span data-stu-id="025f7-239">ProdIndirectTrans > method type2ItemCalcType</span></span>|
|<span data-ttu-id="025f7-240">ProdJournalCheckPostProd.postTransLedger</span><span class="sxs-lookup"><span data-stu-id="025f7-240">ProdJournalCheckPostProd.postTransLedger</span></span>|
|<span data-ttu-id="025f7-241">ProdTableForm.handleProdTableCreatePreSuper</span><span class="sxs-lookup"><span data-stu-id="025f7-241">ProdTableForm.handleProdTableCreatePreSuper</span></span>|
|<span data-ttu-id="025f7-242">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="025f7-242">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="025f7-243">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="025f7-243">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="025f7-244">ProjAdjustmentUpdate.deleteJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-244">ProjAdjustmentUpdate.deleteJournal</span></span>|
|<span data-ttu-id="025f7-245">ProjFundingLimitTrackingManager.updateUsingSourceDocument</span><span class="sxs-lookup"><span data-stu-id="025f7-245">ProjFundingLimitTrackingManager.updateUsingSourceDocument</span></span>|
|<span data-ttu-id="025f7-246">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="025f7-246">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="025f7-247">ProjInvoiceTableCreate.canClose</span><span class="sxs-lookup"><span data-stu-id="025f7-247">ProjInvoiceTableCreate.canClose</span></span>|
|<span data-ttu-id="025f7-248">ProjInvoiceTableCreate.initializeValues</span><span class="sxs-lookup"><span data-stu-id="025f7-248">ProjInvoiceTableCreate.initializeValues</span></span>|
|<span data-ttu-id="025f7-249">ProjPlanVersionsManager.createTemplateHierarchy</span><span class="sxs-lookup"><span data-stu-id="025f7-249">ProjPlanVersionsManager.createTemplateHierarchy</span></span>|
|<span data-ttu-id="025f7-250">ProjPostCostJournal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="025f7-250">ProjPostCostJournal.projTransCreate</span></span>|
|<span data-ttu-id="025f7-251">ProjSalesItemReq.SalesLine.linkActive</span><span class="sxs-lookup"><span data-stu-id="025f7-251">ProjSalesItemReq.SalesLine.linkActive</span></span>|
|<span data-ttu-id="025f7-252">ProjTableType_TimeMaterial.validateWrite</span><span class="sxs-lookup"><span data-stu-id="025f7-252">ProjTableType_TimeMaterial.validateWrite</span></span>|
|<span data-ttu-id="025f7-253">PurchAgreement.applyQueryRanges</span><span class="sxs-lookup"><span data-stu-id="025f7-253">PurchAgreement.applyQueryRanges</span></span>|
|<span data-ttu-id="025f7-254">PurchApproveJournalPost.postPurgeLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="025f7-254">PurchApproveJournalPost.postPurgeLedgerAccount</span></span>|
|<span data-ttu-id="025f7-255">PurchaseOrderResponseService.shouldPurchaseOrderBeAutoConfirmed</span><span class="sxs-lookup"><span data-stu-id="025f7-255">PurchaseOrderResponseService.shouldPurchaseOrderBeAutoConfirmed</span></span>|
|<span data-ttu-id="025f7-256">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="025f7-256">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="025f7-257">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="025f7-257">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="025f7-258">PurchAutoCreate_Sales.createLine</span><span class="sxs-lookup"><span data-stu-id="025f7-258">PurchAutoCreate_Sales.createLine</span></span>|
|<span data-ttu-id="025f7-259">PurchCalcTax.construct</span><span class="sxs-lookup"><span data-stu-id="025f7-259">PurchCalcTax.construct</span></span>|
|<span data-ttu-id="025f7-260">PurchCancel.run</span><span class="sxs-lookup"><span data-stu-id="025f7-260">PurchCancel.run</span></span>|
|<span data-ttu-id="025f7-261">PurchCreateFromOrder.insertMinMaxQty</span><span class="sxs-lookup"><span data-stu-id="025f7-261">PurchCreateFromOrder.insertMinMaxQty</span></span>|
|<span data-ttu-id="025f7-262">PurchCreateFromSalesOrder.insertIntoTmpPurchLinePrice</span><span class="sxs-lookup"><span data-stu-id="025f7-262">PurchCreateFromSalesOrder.insertIntoTmpPurchLinePrice</span></span>|
|<span data-ttu-id="025f7-263">PurchCreateFromSalesOrder.refreshCallerDataSource</span><span class="sxs-lookup"><span data-stu-id="025f7-263">PurchCreateFromSalesOrder.refreshCallerDataSource</span></span>|
|<span data-ttu-id="025f7-264">PurchCreateFromSalesOrder.Salesline.specifyMinMaxQty</span><span class="sxs-lookup"><span data-stu-id="025f7-264">PurchCreateFromSalesOrder.Salesline.specifyMinMaxQty</span></span>|
|<span data-ttu-id="025f7-265">PurchCreateFromSalesOrder.SalesLine.specifyVendAccount</span><span class="sxs-lookup"><span data-stu-id="025f7-265">PurchCreateFromSalesOrder.SalesLine.specifyVendAccount</span></span>|
|<span data-ttu-id="025f7-266">PurchCreateFromSalesOrder.validateSalesLine</span><span class="sxs-lookup"><span data-stu-id="025f7-266">PurchCreateFromSalesOrder.validateSalesLine</span></span>|
|<span data-ttu-id="025f7-267">PurchEditLines.canClose</span><span class="sxs-lookup"><span data-stu-id="025f7-267">PurchEditLines.canClose</span></span>|
|<span data-ttu-id="025f7-268">PurchEditLinesForm.construct</span><span class="sxs-lookup"><span data-stu-id="025f7-268">PurchEditLinesForm.construct</span></span>|
|<span data-ttu-id="025f7-269">PurchFormLetter.construct</span><span class="sxs-lookup"><span data-stu-id="025f7-269">PurchFormLetter.construct</span></span>|
|<span data-ttu-id="025f7-270">PurchFormLetterContract.newFromPackedVersion</span><span class="sxs-lookup"><span data-stu-id="025f7-270">PurchFormLetterContract.newFromPackedVersion</span></span>|
|<span data-ttu-id="025f7-271">PurchFormletterParmDataInvoice.selectFromJournalLines</span><span class="sxs-lookup"><span data-stu-id="025f7-271">PurchFormletterParmDataInvoice.selectFromJournalLines</span></span>|
|<span data-ttu-id="025f7-272">PurchFormLetterProvider.checkPurchLineChanged</span><span class="sxs-lookup"><span data-stu-id="025f7-272">PurchFormLetterProvider.checkPurchLineChanged</span></span>|
|<span data-ttu-id="025f7-273">PurchInvoiceJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="025f7-273">PurchInvoiceJournalPost.updateSourceLine</span></span>|
|<span data-ttu-id="025f7-274">PurchLine.checkInvoiceConstraints</span><span class="sxs-lookup"><span data-stu-id="025f7-274">PurchLine.checkInvoiceConstraints</span></span>|
|<span data-ttu-id="025f7-275">PurchLine.ledgerDimensionItem</span><span class="sxs-lookup"><span data-stu-id="025f7-275">PurchLine.ledgerDimensionItem</span></span>|
|<span data-ttu-id="025f7-276">PurchLine.ledgerDimensionReceipt</span><span class="sxs-lookup"><span data-stu-id="025f7-276">PurchLine.ledgerDimensionReceipt</span></span>|
|<span data-ttu-id="025f7-277">Purchline.unLinkAgreementLinePrompt</span><span class="sxs-lookup"><span data-stu-id="025f7-277">Purchline.unLinkAgreementLinePrompt</span></span>|
|<span data-ttu-id="025f7-278">PurchLine.validateField</span><span class="sxs-lookup"><span data-stu-id="025f7-278">PurchLine.validateField</span></span>|
|<span data-ttu-id="025f7-279">PurchLine::setProjSalesPrice</span><span class="sxs-lookup"><span data-stu-id="025f7-279">PurchLine::setProjSalesPrice</span></span>|
|<span data-ttu-id="025f7-280">PurchPrepayTable.updateAdvanceApplicationRemaining</span><span class="sxs-lookup"><span data-stu-id="025f7-280">PurchPrepayTable.updateAdvanceApplicationRemaining</span></span>|
|<span data-ttu-id="025f7-281">PurchPurchOrderJournalPost.updateSourceTable</span><span class="sxs-lookup"><span data-stu-id="025f7-281">PurchPurchOrderJournalPost.updateSourceTable</span></span>|
|<span data-ttu-id="025f7-282">PurchReqCreate.init</span><span class="sxs-lookup"><span data-stu-id="025f7-282">PurchReqCreate.init</span></span>|
|<span data-ttu-id="025f7-283">PurchReqLine.setDefaultDimension</span><span class="sxs-lookup"><span data-stu-id="025f7-283">PurchReqLine.setDefaultDimension</span></span>|
|<span data-ttu-id="025f7-284">PurchReqLine.validateWrite</span><span class="sxs-lookup"><span data-stu-id="025f7-284">PurchReqLine.validateWrite</span></span>|
|<span data-ttu-id="025f7-285">PurchReqTable.init</span><span class="sxs-lookup"><span data-stu-id="025f7-285">PurchReqTable.init</span></span>|
|<span data-ttu-id="025f7-286">PurchReqTableForm.new</span><span class="sxs-lookup"><span data-stu-id="025f7-286">PurchReqTableForm.new</span></span>|
|<span data-ttu-id="025f7-287">PurchRFQCaseTable.init</span><span class="sxs-lookup"><span data-stu-id="025f7-287">PurchRFQCaseTable.init</span></span>|
|<span data-ttu-id="025f7-288">PurchTable.jumpRefIntercompanySalesOrder</span><span class="sxs-lookup"><span data-stu-id="025f7-288">PurchTable.jumpRefIntercompanySalesOrder</span></span>|
|<span data-ttu-id="025f7-289">PurchTableForm_DeliverySchedule.updatePurchLineTable</span><span class="sxs-lookup"><span data-stu-id="025f7-289">PurchTableForm_DeliverySchedule.updatePurchLineTable</span></span>|
|<span data-ttu-id="025f7-290">PurchTableInteraction.enableHeaderReceive</span><span class="sxs-lookup"><span data-stu-id="025f7-290">PurchTableInteraction.enableHeaderReceive</span></span>|
|<span data-ttu-id="025f7-291">PurchTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="025f7-291">PurchTableType.validateDelete</span></span>|
|<span data-ttu-id="025f7-292">PurchTableUpdateFromPurchReqLineMap.update</span><span class="sxs-lookup"><span data-stu-id="025f7-292">PurchTableUpdateFromPurchReqLineMap.update</span></span>|
|<span data-ttu-id="025f7-293">ReqTransPoMarkFirm.setPurchBuyerGroupId & updatePurchBuyerGroup</span><span class="sxs-lookup"><span data-stu-id="025f7-293">ReqTransPoMarkFirm.setPurchBuyerGroupId & updatePurchBuyerGroup</span></span>|
|<span data-ttu-id="025f7-294">RetailGroupMemberLineHelper.internalCreateOrUpdateOrRemoveRetailGroupMemberLine</span><span class="sxs-lookup"><span data-stu-id="025f7-294">RetailGroupMemberLineHelper.internalCreateOrUpdateOrRemoveRetailGroupMemberLine</span></span>|
|<span data-ttu-id="025f7-295">RetailLabelDP.insertTmpTable</span><span class="sxs-lookup"><span data-stu-id="025f7-295">RetailLabelDP.insertTmpTable</span></span>|
|<span data-ttu-id="025f7-296">SalesCalcAvailableDlvDates.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="025f7-296">SalesCalcAvailableDlvDates.mainOnServer</span></span>|
|<span data-ttu-id="025f7-297">SalesConfirmJournalPost.updateSourceTable</span><span class="sxs-lookup"><span data-stu-id="025f7-297">SalesConfirmJournalPost.updateSourceTable</span></span>|
|<span data-ttu-id="025f7-298">SalesCopying.editCopy</span><span class="sxs-lookup"><span data-stu-id="025f7-298">SalesCopying.editCopy</span></span>|
|<span data-ttu-id="025f7-299">SalesCopying.editMarkAll</span><span class="sxs-lookup"><span data-stu-id="025f7-299">SalesCopying.editMarkAll</span></span>|
|<span data-ttu-id="025f7-300">SalesCopying.initReturnOrderFromCustomer</span><span class="sxs-lookup"><span data-stu-id="025f7-300">SalesCopying.initReturnOrderFromCustomer</span></span>|
|<span data-ttu-id="025f7-301">SalesCreateQuotation.canClose</span><span class="sxs-lookup"><span data-stu-id="025f7-301">SalesCreateQuotation.canClose</span></span>|
|<span data-ttu-id="025f7-302">SalesDropShipmentCancel.removeMarking</span><span class="sxs-lookup"><span data-stu-id="025f7-302">SalesDropShipmentCancel.removeMarking</span></span>|
|<span data-ttu-id="025f7-303">SalesEditLines.canClose</span><span class="sxs-lookup"><span data-stu-id="025f7-303">SalesEditLines.canClose</span></span>|
|<span data-ttu-id="025f7-304">SalesFormletterParmData.reArrangeLines</span><span class="sxs-lookup"><span data-stu-id="025f7-304">SalesFormletterParmData.reArrangeLines</span></span>|
|<span data-ttu-id="025f7-305">SalesFormletterParmData.reArrangeSplit</span><span class="sxs-lookup"><span data-stu-id="025f7-305">SalesFormletterParmData.reArrangeSplit</span></span>|
|<span data-ttu-id="025f7-306">SalesFormletterParmData.reArrangeSplit</span><span class="sxs-lookup"><span data-stu-id="025f7-306">SalesFormletterParmData.reArrangeSplit</span></span>|
|<span data-ttu-id="025f7-307">SalesFormLetterProvider.checkJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-307">SalesFormLetterProvider.checkJournal</span></span>|
|<span data-ttu-id="025f7-308">SalesInvoiceDP.insertGiroInformation</span><span class="sxs-lookup"><span data-stu-id="025f7-308">SalesInvoiceDP.insertGiroInformation</span></span>|
|<span data-ttu-id="025f7-309">SalesInvoiceJournalCreate.checkDocumentData_PL</span><span class="sxs-lookup"><span data-stu-id="025f7-309">SalesInvoiceJournalCreate.checkDocumentData_PL</span></span>|
|<span data-ttu-id="025f7-310">SalesInvoiceJournalPostBase.postLine</span><span class="sxs-lookup"><span data-stu-id="025f7-310">SalesInvoiceJournalPostBase.postLine</span></span>|
|<span data-ttu-id="025f7-311">SalesLine.resetInvent</span><span class="sxs-lookup"><span data-stu-id="025f7-311">SalesLine.resetInvent</span></span>|
|<span data-ttu-id="025f7-312">SalesLineType.initDimensionsSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="025f7-312">SalesLineType.initDimensionsSpecificDefaulting</span></span>|
|<span data-ttu-id="025f7-313">SalesLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="025f7-313">SalesLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="025f7-314">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="025f7-314">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="025f7-315">SalesPackingSlipJournalCreate.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="025f7-315">SalesPackingSlipJournalCreate.updateJournalLine</span></span>|
|<span data-ttu-id="025f7-316">SalesPackingSlipJournalCreate.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="025f7-316">SalesPackingSlipJournalCreate.updateJournalLine</span></span>|
|<span data-ttu-id="025f7-317">SalesPackingSlipJournalPost.insertBackorderLine</span><span class="sxs-lookup"><span data-stu-id="025f7-317">SalesPackingSlipJournalPost.insertBackorderLine</span></span>|
|<span data-ttu-id="025f7-318">SalesPackingSlipJournalPost.interCompanyPost</span><span class="sxs-lookup"><span data-stu-id="025f7-318">SalesPackingSlipJournalPost.interCompanyPost</span></span>|
|<span data-ttu-id="025f7-319">SalesPackingSlipJournalPost.updateJournalLine</span><span class="sxs-lookup"><span data-stu-id="025f7-319">SalesPackingSlipJournalPost.updateJournalLine</span></span>|
|<span data-ttu-id="025f7-320">SalesPurchSummaryModel_Account.createNewJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-320">SalesPurchSummaryModel_Account.createNewJournal</span></span>|
|<span data-ttu-id="025f7-321">SalesQuotationCalcTax_Sales.construct</span><span class="sxs-lookup"><span data-stu-id="025f7-321">SalesQuotationCalcTax_Sales.construct</span></span>|
|<span data-ttu-id="025f7-322">SalesQuotationEditLinesForm.postUpdate</span><span class="sxs-lookup"><span data-stu-id="025f7-322">SalesQuotationEditLinesForm.postUpdate</span></span>|
|<span data-ttu-id="025f7-323">SalesQuotationLineType.initFromProjTable</span><span class="sxs-lookup"><span data-stu-id="025f7-323">SalesQuotationLineType.initFromProjTable</span></span>|
|<span data-ttu-id="025f7-324">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span><span class="sxs-lookup"><span data-stu-id="025f7-324">SalesQuotationLineType.initReleasedProductSpecificDefaulting</span></span>|
|<span data-ttu-id="025f7-325">SalesQuotationTable.modifiedField</span><span class="sxs-lookup"><span data-stu-id="025f7-325">SalesQuotationTable.modifiedField</span></span>|
|<span data-ttu-id="025f7-326">SalesQuotationTableForm.createFromTemplate</span><span class="sxs-lookup"><span data-stu-id="025f7-326">SalesQuotationTableForm.createFromTemplate</span></span>|
|<span data-ttu-id="025f7-327">SalesQuotationUpdate_Cancelled.run</span><span class="sxs-lookup"><span data-stu-id="025f7-327">SalesQuotationUpdate_Cancelled.run</span></span>|
|<span data-ttu-id="025f7-328">SalesQuotationUpdate_Lost.run</span><span class="sxs-lookup"><span data-stu-id="025f7-328">SalesQuotationUpdate_Lost.run</span></span>|
|<span data-ttu-id="025f7-329">SalesTable.initFromCustTableMandatoryFields</span><span class="sxs-lookup"><span data-stu-id="025f7-329">SalesTable.initFromCustTableMandatoryFields</span></span>|
|<span data-ttu-id="025f7-330">SalesTable.jumpRefIntercompanyPurchaseOrder</span><span class="sxs-lookup"><span data-stu-id="025f7-330">SalesTable.jumpRefIntercompanyPurchaseOrder</span></span>|
|<span data-ttu-id="025f7-331">SalesTable.setShipCarrierFromLogisticsLocation</span><span class="sxs-lookup"><span data-stu-id="025f7-331">SalesTable.setShipCarrierFromLogisticsLocation</span></span>|
|<span data-ttu-id="025f7-332">SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="025f7-332">SalesTable.update</span></span>|
|<span data-ttu-id="025f7-333">SalesTableForm.interCompanyAutoCreateOrders</span><span class="sxs-lookup"><span data-stu-id="025f7-333">SalesTableForm.interCompanyAutoCreateOrders</span></span>|
|<span data-ttu-id="025f7-334">SettlementPair.createSettlementForDebitOrCreditTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-334">SettlementPair.createSettlementForDebitOrCreditTrans</span></span>|
|<span data-ttu-id="025f7-335">SmaServiceFunctionLine_Transfer.createJournalLine</span><span class="sxs-lookup"><span data-stu-id="025f7-335">SmaServiceFunctionLine_Transfer.createJournalLine</span></span>|
|<span data-ttu-id="025f7-336">SmaServiceFunctionLine_Transfer.postJournalTransType</span><span class="sxs-lookup"><span data-stu-id="025f7-336">SmaServiceFunctionLine_Transfer.postJournalTransType</span></span>|
|<span data-ttu-id="025f7-337">SmaServiceOrderCreate.createServiceOrderLine</span><span class="sxs-lookup"><span data-stu-id="025f7-337">SmaServiceOrderCreate.createServiceOrderLine</span></span>|
|<span data-ttu-id="025f7-338">SmaSubscriptionGenerator::postTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-338">SmaSubscriptionGenerator::postTrans</span></span>|
|<span data-ttu-id="025f7-339">smmBusRelTable.relation2Vendor</span><span class="sxs-lookup"><span data-stu-id="025f7-339">smmBusRelTable.relation2Vendor</span></span>|
|<span data-ttu-id="025f7-340">smmBusRelTable.updateQuotations</span><span class="sxs-lookup"><span data-stu-id="025f7-340">smmBusRelTable.updateQuotations</span></span>|
|<span data-ttu-id="025f7-341">SmmCampaignBroadcast::validate</span><span class="sxs-lookup"><span data-stu-id="025f7-341">SmmCampaignBroadcast::validate</span></span>|
|<span data-ttu-id="025f7-342">SmmOpportunityStatusUpdate.updateOpportunity</span><span class="sxs-lookup"><span data-stu-id="025f7-342">SmmOpportunityStatusUpdate.updateOpportunity</span></span>|
|<span data-ttu-id="025f7-343">smmOpportunityTable\Methods\openQuotation</span><span class="sxs-lookup"><span data-stu-id="025f7-343">smmOpportunityTable\Methods\openQuotation</span></span>|
|<span data-ttu-id="025f7-344">SmmProjectCreate.createSingleProject</span><span class="sxs-lookup"><span data-stu-id="025f7-344">SmmProjectCreate.createSingleProject</span></span>|
|<span data-ttu-id="025f7-345">SmmProjectCreate.createSingleProject</span><span class="sxs-lookup"><span data-stu-id="025f7-345">SmmProjectCreate.createSingleProject</span></span>|
|<span data-ttu-id="025f7-346">SmmUpdateBusRel.updateFromVendTableSFA2</span><span class="sxs-lookup"><span data-stu-id="025f7-346">SmmUpdateBusRel.updateFromVendTableSFA2</span></span>|
|<span data-ttu-id="025f7-347">SubledgerJournalTransferController.run</span><span class="sxs-lookup"><span data-stu-id="025f7-347">SubledgerJournalTransferController.run</span></span>|
|<span data-ttu-id="025f7-348">SuppItem.calcSuppItem</span><span class="sxs-lookup"><span data-stu-id="025f7-348">SuppItem.calcSuppItem</span></span>|
|<span data-ttu-id="025f7-349">SuppItem::newSuppItem</span><span class="sxs-lookup"><span data-stu-id="025f7-349">SuppItem::newSuppItem</span></span>|
|<span data-ttu-id="025f7-350">SuppItemCreate::newSuppItemCreate</span><span class="sxs-lookup"><span data-stu-id="025f7-350">SuppItemCreate::newSuppItemCreate</span></span>|
|<span data-ttu-id="025f7-351">Tax.post</span><span class="sxs-lookup"><span data-stu-id="025f7-351">Tax.post</span></span>|
|<span data-ttu-id="025f7-352">Tax.saveAndPost</span><span class="sxs-lookup"><span data-stu-id="025f7-352">Tax.saveAndPost</span></span>|
|<span data-ttu-id="025f7-353">TaxFreeInvoice_Invoice.updateAndPost</span><span class="sxs-lookup"><span data-stu-id="025f7-353">TaxFreeInvoice_Invoice.updateAndPost</span></span>|
|<span data-ttu-id="025f7-354">TaxPost.moveTaxLineToNewOwner</span><span class="sxs-lookup"><span data-stu-id="025f7-354">TaxPost.moveTaxLineToNewOwner</span></span>|
|<span data-ttu-id="025f7-355">TaxPost.saveAndPostFromTmpTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-355">TaxPost.saveAndPostFromTmpTaxWorkTrans</span></span>|
|<span data-ttu-id="025f7-356">TaxPost.saveAndPostFromTmpTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-356">TaxPost.saveAndPostFromTmpTaxWorkTrans</span></span>|
|<span data-ttu-id="025f7-357">TaxVoucherService.postTaxOnErrorAccount</span><span class="sxs-lookup"><span data-stu-id="025f7-357">TaxVoucherService.postTaxOnErrorAccount</span></span>|
|<span data-ttu-id="025f7-358">TradePackingSlipJourChain.createRelationship</span><span class="sxs-lookup"><span data-stu-id="025f7-358">TradePackingSlipJourChain.createRelationship</span></span>|
|<span data-ttu-id="025f7-359">TradeTotals.calc</span><span class="sxs-lookup"><span data-stu-id="025f7-359">TradeTotals.calc</span></span>|
|<span data-ttu-id="025f7-360">TradeTotals.updateOrderBalances</span><span class="sxs-lookup"><span data-stu-id="025f7-360">TradeTotals.updateOrderBalances</span></span>|
|<span data-ttu-id="025f7-361">VendAccountStatementIntDP.processReport</span><span class="sxs-lookup"><span data-stu-id="025f7-361">VendAccountStatementIntDP.processReport</span></span>|
|<span data-ttu-id="025f7-362">VendEditInvoice\DataSource\VendInvoiceInfoTable\Methods\write</span><span class="sxs-lookup"><span data-stu-id="025f7-362">VendEditInvoice\DataSource\VendInvoiceInfoTable\Methods\write</span></span>|
|<span data-ttu-id="025f7-363">VendInvoiceMatching.initExpectedValues</span><span class="sxs-lookup"><span data-stu-id="025f7-363">VendInvoiceMatching.initExpectedValues</span></span>|
|<span data-ttu-id="025f7-364">VendInvoiceWFParticipantProviderExpend.resolve</span><span class="sxs-lookup"><span data-stu-id="025f7-364">VendInvoiceWFParticipantProviderExpend.resolve</span></span>|
|<span data-ttu-id="025f7-365">VendOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-365">VendOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="025f7-366">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="025f7-366">VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="025f7-367">VendPaymentJournalDP.insertDataFromLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-367">VendPaymentJournalDP.insertDataFromLedgerJournalTrans</span></span>|
|<span data-ttu-id="025f7-368">VendPaymentJournalDP.insertDataFromSpecTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-368">VendPaymentJournalDP.insertDataFromSpecTrans</span></span>|
|<span data-ttu-id="025f7-369">VendPromissoryNotePost.postNextStep</span><span class="sxs-lookup"><span data-stu-id="025f7-369">VendPromissoryNotePost.postNextStep</span></span>|
|<span data-ttu-id="025f7-370">VendProvisionalBalanceDP.calculateAmounts</span><span class="sxs-lookup"><span data-stu-id="025f7-370">VendProvisionalBalanceDP.calculateAmounts</span></span>|
|<span data-ttu-id="025f7-371">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span><span class="sxs-lookup"><span data-stu-id="025f7-371">VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp</span></span>|
|<span data-ttu-id="025f7-372">VendProvisionalBalanceDP.processReport</span><span class="sxs-lookup"><span data-stu-id="025f7-372">VendProvisionalBalanceDP.processReport</span></span>|
|<span data-ttu-id="025f7-373">VendTransListDP.ProcessReport</span><span class="sxs-lookup"><span data-stu-id="025f7-373">VendTransListDP.ProcessReport</span></span>|
|<span data-ttu-id="025f7-374">VendVoucher.createInvoiceJournal</span><span class="sxs-lookup"><span data-stu-id="025f7-374">VendVoucher.createInvoiceJournal</span></span>|
|<span data-ttu-id="025f7-375">WHSDocumentRouting.printDocument</span><span class="sxs-lookup"><span data-stu-id="025f7-375">WHSDocumentRouting.printDocument</span></span>|
|<span data-ttu-id="025f7-376">WhsLoadLineInventTransValidator.checkLoadLineInventTransConsistencyOnInventoryUpdate</span><span class="sxs-lookup"><span data-stu-id="025f7-376">WhsLoadLineInventTransValidator.checkLoadLineInventTransConsistencyOnInventoryUpdate</span></span>|
|<span data-ttu-id="025f7-377">WHSLoadLineUpdater.initAndInsertLoadLine</span><span class="sxs-lookup"><span data-stu-id="025f7-377">WHSLoadLineUpdater.initAndInsertLoadLine</span></span>|
|<span data-ttu-id="025f7-378">WhsShipConfirm.createASNItems</span><span class="sxs-lookup"><span data-stu-id="025f7-378">WhsShipConfirm.createASNItems</span></span>|
|<span data-ttu-id="025f7-379">WhsWarehouseRelease.createLoadLines</span><span class="sxs-lookup"><span data-stu-id="025f7-379">WhsWarehouseRelease.createLoadLines</span></span>|
|<span data-ttu-id="025f7-380">WHSWorkExecute.executeShortPick</span><span class="sxs-lookup"><span data-stu-id="025f7-380">WHSWorkExecute.executeShortPick</span></span>|
|<span data-ttu-id="025f7-381">WHSWorkExecuteDisplayLPReceiving.displayForm</span><span class="sxs-lookup"><span data-stu-id="025f7-381">WHSWorkExecuteDisplayLPReceiving.displayForm</span></span>|
|<span data-ttu-id="025f7-382">WHSWorkExecuteDisplayLPReceiving.displayNextForm</span><span class="sxs-lookup"><span data-stu-id="025f7-382">WHSWorkExecuteDisplayLPReceiving.displayNextForm</span></span>|
|<span data-ttu-id="025f7-383">WHSWorkExecuteDisplayMovementByTemplate.displayForm</span><span class="sxs-lookup"><span data-stu-id="025f7-383">WHSWorkExecuteDisplayMovementByTemplate.displayForm</span></span>|
|<span data-ttu-id="025f7-384">WhsWorkExecuteForm.createLabel</span><span class="sxs-lookup"><span data-stu-id="025f7-384">WhsWorkExecuteForm.createLabel</span></span>|
|<span data-ttu-id="025f7-385">WmsJournalCheckPostReception.postTrans</span><span class="sxs-lookup"><span data-stu-id="025f7-385">WmsJournalCheckPostReception.postTrans</span></span>|
|<span data-ttu-id="025f7-386">WmsOnlineCountingServer.getMovement</span><span class="sxs-lookup"><span data-stu-id="025f7-386">WmsOnlineCountingServer.getMovement</span></span>|
|<span data-ttu-id="025f7-387">WmsOnlineCountingServer.handleLine</span><span class="sxs-lookup"><span data-stu-id="025f7-387">WmsOnlineCountingServer.handleLine</span></span>|
|<span data-ttu-id="025f7-388">WmsOrderCreate.updateCreatewmsOrder</span><span class="sxs-lookup"><span data-stu-id="025f7-388">WmsOrderCreate.updateCreatewmsOrder</span></span>|
|<span data-ttu-id="025f7-389">WrkCtrResourceAbilityMapController.loadData</span><span class="sxs-lookup"><span data-stu-id="025f7-389">WrkCtrResourceAbilityMapController.loadData</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="025f7-390">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="025f7-390">Enumerations made extensible</span></span>

<span data-ttu-id="025f7-391">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="025f7-391">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="025f7-392">列挙型</span><span class="sxs-lookup"><span data-stu-id="025f7-392">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="025f7-393">ABCModel</span><span class="sxs-lookup"><span data-stu-id="025f7-393">ABCModel</span></span>|
|<span data-ttu-id="025f7-394">AccountOrder</span><span class="sxs-lookup"><span data-stu-id="025f7-394">AccountOrder</span></span>|
|<span data-ttu-id="025f7-395">AmountUnit</span><span class="sxs-lookup"><span data-stu-id="025f7-395">AmountUnit</span></span>|
|<span data-ttu-id="025f7-396">CostCalculationRateSubtype</span><span class="sxs-lookup"><span data-stu-id="025f7-396">CostCalculationRateSubtype</span></span>|
|<span data-ttu-id="025f7-397">CurrencyGainLossAccountType</span><span class="sxs-lookup"><span data-stu-id="025f7-397">CurrencyGainLossAccountType</span></span>|
|<span data-ttu-id="025f7-398">CustInterestCodeSource</span><span class="sxs-lookup"><span data-stu-id="025f7-398">CustInterestCodeSource</span></span>|
|<span data-ttu-id="025f7-399">CustPaymentType</span><span class="sxs-lookup"><span data-stu-id="025f7-399">CustPaymentType</span></span>|
|<span data-ttu-id="025f7-400">DirViewLocationNodeType</span><span class="sxs-lookup"><span data-stu-id="025f7-400">DirViewLocationNodeType</span></span>|
|<span data-ttu-id="025f7-401">InterestCalcAccountChoice</span><span class="sxs-lookup"><span data-stu-id="025f7-401">InterestCalcAccountChoice</span></span>|
|<span data-ttu-id="025f7-402">InventTransPostingType</span><span class="sxs-lookup"><span data-stu-id="025f7-402">InventTransPostingType</span></span>|
|<span data-ttu-id="025f7-403">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="025f7-403">MCRCustSearchType</span></span>|
|<span data-ttu-id="025f7-404">PaymentStub</span><span class="sxs-lookup"><span data-stu-id="025f7-404">PaymentStub</span></span>|
|<span data-ttu-id="025f7-405">PaymentStubInclAll</span><span class="sxs-lookup"><span data-stu-id="025f7-405">PaymentStubInclAll</span></span>|
|<span data-ttu-id="025f7-406">ProjCompletePrincip</span><span class="sxs-lookup"><span data-stu-id="025f7-406">ProjCompletePrincip</span></span>|
|<span data-ttu-id="025f7-407">ProjMatchingPrincip</span><span class="sxs-lookup"><span data-stu-id="025f7-407">ProjMatchingPrincip</span></span>|
|<span data-ttu-id="025f7-408">RetailPOSSeedDataType</span><span class="sxs-lookup"><span data-stu-id="025f7-408">RetailPOSSeedDataType</span></span>|
|<span data-ttu-id="025f7-409">SalesQuotationStatus</span><span class="sxs-lookup"><span data-stu-id="025f7-409">SalesQuotationStatus</span></span>|
|<span data-ttu-id="025f7-410">TMSApptStatus</span><span class="sxs-lookup"><span data-stu-id="025f7-410">TMSApptStatus</span></span>|
|<span data-ttu-id="025f7-411">TMSCommunicationType</span><span class="sxs-lookup"><span data-stu-id="025f7-411">TMSCommunicationType</span></span>|

## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="025f7-412">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="025f7-412">Additional extensibility enhancements</span></span>

<span data-ttu-id="025f7-413">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="025f7-413">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="025f7-414">CustVendSettle: 変数をプライベートではなく保護に設定します。</span><span class="sxs-lookup"><span data-stu-id="025f7-414">CustVendSettle: set variables protected instead of private.</span></span>
- <span data-ttu-id="025f7-415">イベントを引き起こさないデータ操作メソッド: WHSLocationDirective.loopLocDirLines。</span><span class="sxs-lookup"><span data-stu-id="025f7-415">Data manipulation method not raising event: WHSLocationDirective.loopLocDirLines.</span></span>
- <span data-ttu-id="025f7-416">イベントを引き起こさないデータ操作メソッド: WhsWorkCreate.createTempLine。</span><span class="sxs-lookup"><span data-stu-id="025f7-416">Data manipulation method not raising event: WhsWorkCreate.createTempLine.</span></span>
- <span data-ttu-id="025f7-417">マップ拡張: LogisticsPostalAddressMap。</span><span class="sxs-lookup"><span data-stu-id="025f7-417">Map extension: LogisticsPostalAddressMap.</span></span>
- <span data-ttu-id="025f7-418">マップ拡張: PurchReqLineMap。</span><span class="sxs-lookup"><span data-stu-id="025f7-418">Map extension: PurchReqLineMap.</span></span>
- <span data-ttu-id="025f7-419">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Is Public = Yes。</span><span class="sxs-lookup"><span data-stu-id="025f7-419">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Is Public = Yes.</span></span>
- <span data-ttu-id="025f7-420">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Collection Name = ProjWBSActivityEstimates。</span><span class="sxs-lookup"><span data-stu-id="025f7-420">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Public Collection Name = ProjWBSActivityEstimates.</span></span>
- <span data-ttu-id="025f7-421">メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Entity Name = ProjWBSActivityEstimates</span><span class="sxs-lookup"><span data-stu-id="025f7-421">Metadata change: DataEntityView/ProjWBSActivityEstimatesEntity.Public Entity Name = ProjWBSActivityEstimates</span></span>
- <span data-ttu-id="025f7-422">メタデータの変更: /Data Model/Data Entities/EcoResProductAttributeValueEntity.IsPublic = Yes。</span><span class="sxs-lookup"><span data-stu-id="025f7-422">Metadata change: /Data Model/Data Entities/EcoResProductAttributeValueEntity.IsPublic = Yes.</span></span>
- <span data-ttu-id="025f7-423">メタデータの変更: Form/WHSLoadPlanningListPage/FormDesign/FormDesign/FormActionPaneTabControl/ActionPaneTabShipReceive.Needed permission。</span><span class="sxs-lookup"><span data-stu-id="025f7-423">Metadata change: Form/WHSLoadPlanningListPage/FormDesign/FormDesign/FormActionPaneTabControl/ActionPaneTabShipReceive.Needed permission.</span></span>
- <span data-ttu-id="025f7-424">メタデータの変更: WHSContainerLine, Relations WHSLoadLine & WHSShipmentTable.On Delete。</span><span class="sxs-lookup"><span data-stu-id="025f7-424">Metadata change: WHSContainerLine, Relations WHSLoadLine & WHSShipmentTable.On Delete.</span></span>
- <span data-ttu-id="025f7-425">メタデータの変更: WHSContainerTable, Relation WHSShipmentTable.On Delete。</span><span class="sxs-lookup"><span data-stu-id="025f7-425">Metadata change: WHSContainerTable, Relation WHSShipmentTable.On Delete.</span></span>
- <span data-ttu-id="025f7-426">プロジェクトの価格決定: 新しい価格決定検索メソッドの完全な取得。</span><span class="sxs-lookup"><span data-stu-id="025f7-426">Project pricing: complete uptake of new pricing find methods.</span></span>
