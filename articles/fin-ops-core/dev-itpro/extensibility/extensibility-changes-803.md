---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
ms.date: 08/03/2018
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
ms.dyn365.ops.version: App 8.0.3
ms.openlocfilehash: 2843246e46b3c255b5ce7bd50251e34b4a6e6d1c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749630"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-803"></a><span data-ttu-id="7ace6-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="7ace6-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.3</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ace6-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="7ace6-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.3.</span></span> <span data-ttu-id="7ace6-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ace6-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="7ace6-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="7ace6-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="7ace6-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7ace6-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="7ace6-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="7ace6-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="7ace6-109">AccountingSourceExplorerProcessor.filterEntries</span><span class="sxs-lookup"><span data-stu-id="7ace6-109">AccountingSourceExplorerProcessor.filterEntries</span></span>|
|<span data-ttu-id="7ace6-110">AgreementClassification.init</span><span class="sxs-lookup"><span data-stu-id="7ace6-110">AgreementClassification.init</span></span>|
|<span data-ttu-id="7ace6-111">AgreementConfirm.createLineVolumeCommittmentHistory</span><span class="sxs-lookup"><span data-stu-id="7ace6-111">AgreementConfirm.createLineVolumeCommittmentHistory</span></span>|
|<span data-ttu-id="7ace6-112">AgreementConfirm.newAgreementConfirm</span><span class="sxs-lookup"><span data-stu-id="7ace6-112">AgreementConfirm.newAgreementConfirm</span></span>|
|<span data-ttu-id="7ace6-113">Agreementline.findLineForAutoMatch</span><span class="sxs-lookup"><span data-stu-id="7ace6-113">Agreementline.findLineForAutoMatch</span></span>|
|<span data-ttu-id="7ace6-114">Agreementline.getAgreementLinesForOrderLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-114">Agreementline.getAgreementLinesForOrderLine</span></span>|
|<span data-ttu-id="7ace6-115">AgreementLine.getAgreementLinesForPurchReqLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-115">AgreementLine.getAgreementLinesForPurchReqLine</span></span>|
|<span data-ttu-id="7ace6-116">Agreementline.getAgreementLinesList</span><span class="sxs-lookup"><span data-stu-id="7ace6-116">Agreementline.getAgreementLinesList</span></span>|
|<span data-ttu-id="7ace6-117">Bank_FR.checkControlText</span><span class="sxs-lookup"><span data-stu-id="7ace6-117">Bank_FR.checkControlText</span></span>|
|<span data-ttu-id="7ace6-118">Bank_IT.checkCIN</span><span class="sxs-lookup"><span data-stu-id="7ace6-118">Bank_IT.checkCIN</span></span>|
|<span data-ttu-id="7ace6-119">Bank_IT.checkRegistrationNum</span><span class="sxs-lookup"><span data-stu-id="7ace6-119">Bank_IT.checkRegistrationNum</span></span>|
|<span data-ttu-id="7ace6-120">BankAccountTrans.insert</span><span class="sxs-lookup"><span data-stu-id="7ace6-120">BankAccountTrans.insert</span></span>|
|<span data-ttu-id="7ace6-121">BankAccountTrans.update</span><span class="sxs-lookup"><span data-stu-id="7ace6-121">BankAccountTrans.update</span></span>|
|<span data-ttu-id="7ace6-122">BankChequeCopy.fillTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="7ace6-122">BankChequeCopy.fillTmpChequePrintout</span></span>|
|<span data-ttu-id="7ace6-123">BankChequePrint.printDocument</span><span class="sxs-lookup"><span data-stu-id="7ace6-123">BankChequePrint.printDocument</span></span>|
|<span data-ttu-id="7ace6-124">BankPaymAdviceReportGeneratorVend</span><span class="sxs-lookup"><span data-stu-id="7ace6-124">BankPaymAdviceReportGeneratorVend</span></span>|
|<span data-ttu-id="7ace6-125">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span><span class="sxs-lookup"><span data-stu-id="7ace6-125">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span></span>|
|<span data-ttu-id="7ace6-126">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span><span class="sxs-lookup"><span data-stu-id="7ace6-126">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span></span>|
|<span data-ttu-id="7ace6-127">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span><span class="sxs-lookup"><span data-stu-id="7ace6-127">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span></span>|
|<span data-ttu-id="7ace6-128">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span><span class="sxs-lookup"><span data-stu-id="7ace6-128">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span></span>|
|<span data-ttu-id="7ace6-129">BankVoucher.createBankAccountTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-129">BankVoucher.createBankAccountTrans</span></span>|
|<span data-ttu-id="7ace6-130">BankVoucher.createBankAccountTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-130">BankVoucher.createBankAccountTrans</span></span>|
|<span data-ttu-id="7ace6-131">BomCopyToProd.copyTo</span><span class="sxs-lookup"><span data-stu-id="7ace6-131">BomCopyToProd.copyTo</span></span>|
|<span data-ttu-id="7ace6-132">BudgetPlanLineFieldActiveViewMapping.getBudgetPlanLineFieldName</span><span class="sxs-lookup"><span data-stu-id="7ace6-132">BudgetPlanLineFieldActiveViewMapping.getBudgetPlanLineFieldName</span></span>|
|<span data-ttu-id="7ace6-133">BudgetTransaction.openLinesInExcel</span><span class="sxs-lookup"><span data-stu-id="7ace6-133">BudgetTransaction.openLinesInExcel</span></span>|
|<span data-ttu-id="7ace6-134">ChequeController.init</span><span class="sxs-lookup"><span data-stu-id="7ace6-134">ChequeController.init</span></span>|
|<span data-ttu-id="7ace6-135">CustAccountStatementExt.main</span><span class="sxs-lookup"><span data-stu-id="7ace6-135">CustAccountStatementExt.main</span></span>|
|<span data-ttu-id="7ace6-136">CustAccountStatementExtController.includeOnStatement</span><span class="sxs-lookup"><span data-stu-id="7ace6-136">CustAccountStatementExtController.includeOnStatement</span></span>|
|<span data-ttu-id="7ace6-137">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-137">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span></span>|
|<span data-ttu-id="7ace6-138">CustAccountStatementExtController.setCommonData</span><span class="sxs-lookup"><span data-stu-id="7ace6-138">CustAccountStatementExtController.setCommonData</span></span>|
|<span data-ttu-id="7ace6-139">CustAccountStatementExtController.tmpCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-139">CustAccountStatementExtController.tmpCustVendTrans</span></span>|
|<span data-ttu-id="7ace6-140">CustAccountStatementExtUIBuilder.build</span><span class="sxs-lookup"><span data-stu-id="7ace6-140">CustAccountStatementExtUIBuilder.build</span></span>|
|<span data-ttu-id="7ace6-141">CustAuditorDP.setCustAuditorTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-141">CustAuditorDP.setCustAuditorTmp</span></span>|
|<span data-ttu-id="7ace6-142">CustCollectionJourDP.insertCustCollectionJourDP</span><span class="sxs-lookup"><span data-stu-id="7ace6-142">CustCollectionJourDP.insertCustCollectionJourDP</span></span>|
|<span data-ttu-id="7ace6-143">CustCreditLimit.Balance</span><span class="sxs-lookup"><span data-stu-id="7ace6-143">CustCreditLimit.Balance</span></span>|
|<span data-ttu-id="7ace6-144">CustInterestNoteDp.processReport</span><span class="sxs-lookup"><span data-stu-id="7ace6-144">CustInterestNoteDp.processReport</span></span>|
|<span data-ttu-id="7ace6-145">CustInvoiceJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="7ace6-145">CustInvoiceJour.printJournal</span></span>|
|<span data-ttu-id="7ace6-146">CustInvoiceTable.checkCreditLimit</span><span class="sxs-lookup"><span data-stu-id="7ace6-146">CustInvoiceTable.checkCreditLimit</span></span>|
|<span data-ttu-id="7ace6-147">CustPackingSlipJour.interCompanyUpdate</span><span class="sxs-lookup"><span data-stu-id="7ace6-147">CustPackingSlipJour.interCompanyUpdate</span></span>|
|<span data-ttu-id="7ace6-148">CustPaymEntry.updateConditionalControls</span><span class="sxs-lookup"><span data-stu-id="7ace6-148">CustPaymEntry.updateConditionalControls</span></span>|
|<span data-ttu-id="7ace6-149">custPostInvoicejob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="7ace6-149">custPostInvoicejob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="7ace6-150">CustTrans.reverseTransact</span><span class="sxs-lookup"><span data-stu-id="7ace6-150">CustTrans.reverseTransact</span></span>|
|<span data-ttu-id="7ace6-151">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-151">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="7ace6-152">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-152">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="7ace6-153">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="7ace6-153">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="7ace6-154">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="7ace6-154">CustVendCheque.output</span></span>|
|<span data-ttu-id="7ace6-155">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="7ace6-155">CustVendCheque.output</span></span>|
|<span data-ttu-id="7ace6-156">CustVendChequeSlipTextCalculator.getChequeDocLength</span><span class="sxs-lookup"><span data-stu-id="7ace6-156">CustVendChequeSlipTextCalculator.getChequeDocLength</span></span>|
|<span data-ttu-id="7ace6-157">CustVendSumForPaym.validateSEPATransaction</span><span class="sxs-lookup"><span data-stu-id="7ace6-157">CustVendSumForPaym.validateSEPATransaction</span></span>|
|<span data-ttu-id="7ace6-158">CustVendSumUpJournal.createTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-158">CustVendSumUpJournal.createTrans</span></span>|
|<span data-ttu-id="7ace6-159">CustVendVoucher.post</span><span class="sxs-lookup"><span data-stu-id="7ace6-159">CustVendVoucher.post</span></span>|
|<span data-ttu-id="7ace6-160">DimDerDistRuleProjectTimesheetsExt.populateDimAllocListIntercompany</span><span class="sxs-lookup"><span data-stu-id="7ace6-160">DimDerDistRuleProjectTimesheetsExt.populateDimAllocListIntercompany</span></span>|
|<span data-ttu-id="7ace6-161">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span><span class="sxs-lookup"><span data-stu-id="7ace6-161">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span></span>|
|<span data-ttu-id="7ace6-162">DirPartyVerification.selectionChanged</span><span class="sxs-lookup"><span data-stu-id="7ace6-162">DirPartyVerification.selectionChanged</span></span>|
|<span data-ttu-id="7ace6-163">EcoResCategoryTreeDatasource.initializeAvailableCategoriesMap</span><span class="sxs-lookup"><span data-stu-id="7ace6-163">EcoResCategoryTreeDatasource.initializeAvailableCategoriesMap</span></span>|
|<span data-ttu-id="7ace6-164">EcoResProductCreate.writeMoreFields</span><span class="sxs-lookup"><span data-stu-id="7ace6-164">EcoResProductCreate.writeMoreFields</span></span>|
|<span data-ttu-id="7ace6-165">EcoResProductDetailsExtended.initInventDimensionsMetadataEntries</span><span class="sxs-lookup"><span data-stu-id="7ace6-165">EcoResProductDetailsExtended.initInventDimensionsMetadataEntries</span></span>|
|<span data-ttu-id="7ace6-166">ElectronicPaymentRemitExport_BR.construct</span><span class="sxs-lookup"><span data-stu-id="7ace6-166">ElectronicPaymentRemitExport_BR.construct</span></span>|
|<span data-ttu-id="7ace6-167">ForecastPuch</span><span class="sxs-lookup"><span data-stu-id="7ace6-167">ForecastPuch</span></span>|
|<span data-ttu-id="7ace6-168">ForecastSales.accountConsumption</span><span class="sxs-lookup"><span data-stu-id="7ace6-168">ForecastSales.accountConsumption</span></span>|
|<span data-ttu-id="7ace6-169">ForecastSales.accountDisc</span><span class="sxs-lookup"><span data-stu-id="7ace6-169">ForecastSales.accountDisc</span></span>|
|<span data-ttu-id="7ace6-170">ForecastSales.accountIssue</span><span class="sxs-lookup"><span data-stu-id="7ace6-170">ForecastSales.accountIssue</span></span>|
|<span data-ttu-id="7ace6-171">ForecastSales.accountSales</span><span class="sxs-lookup"><span data-stu-id="7ace6-171">ForecastSales.accountSales</span></span>|
|<span data-ttu-id="7ace6-172">InventPosting.accountItemLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="7ace6-172">InventPosting.accountItemLedgerDimension</span></span>|
|<span data-ttu-id="7ace6-173">InventSupply.init</span><span class="sxs-lookup"><span data-stu-id="7ace6-173">InventSupply.init</span></span>|
|<span data-ttu-id="7ace6-174">InventTrans.insertReturnTransOrigin</span><span class="sxs-lookup"><span data-stu-id="7ace6-174">InventTrans.insertReturnTransOrigin</span></span>|
|<span data-ttu-id="7ace6-175">InventTransferParmLine - いくつかの方法</span><span class="sxs-lookup"><span data-stu-id="7ace6-175">InventTransferParmLine - several methods</span></span>|
|<span data-ttu-id="7ace6-176">InventTransferUpd::updateLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-176">InventTransferUpd::updateLines</span></span>|
|<span data-ttu-id="7ace6-177">InventTransFormHelper.formQueryAddDynalink</span><span class="sxs-lookup"><span data-stu-id="7ace6-177">InventTransFormHelper.formQueryAddDynalink</span></span>|
|<span data-ttu-id="7ace6-178">InventTransWMS_Pick::updateInventServer</span><span class="sxs-lookup"><span data-stu-id="7ace6-178">InventTransWMS_Pick::updateInventServer</span></span>|
|<span data-ttu-id="7ace6-179">InventUpd_Physical::updatePhysicalReceiptTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-179">InventUpd_Physical::updatePhysicalReceiptTrans</span></span>|
|<span data-ttu-id="7ace6-180">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-180">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="7ace6-181">InventUpdate::createInventTransOriginAndReferences</span><span class="sxs-lookup"><span data-stu-id="7ace6-181">InventUpdate::createInventTransOriginAndReferences</span></span>|
|<span data-ttu-id="7ace6-182">InventValueReportPopulateItem::findReportLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-182">InventValueReportPopulateItem::findReportLine</span></span>|
|<span data-ttu-id="7ace6-183">JmgRegistration.JmgJobTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-183">JmgRegistration.JmgJobTable</span></span>|
|<span data-ttu-id="7ace6-184">JournalizingDefinitionManager.newJournalizingDefinitionManagerPurch</span><span class="sxs-lookup"><span data-stu-id="7ace6-184">JournalizingDefinitionManager.newJournalizingDefinitionManagerPurch</span></span>|
|<span data-ttu-id="7ace6-185">JournalStatic.initializeDataModel</span><span class="sxs-lookup"><span data-stu-id="7ace6-185">JournalStatic.initializeDataModel</span></span>|
|<span data-ttu-id="7ace6-186">LedgerFinancialJournalReportDPBE.calcDebCredTotals</span><span class="sxs-lookup"><span data-stu-id="7ace6-186">LedgerFinancialJournalReportDPBE.calcDebCredTotals</span></span>|
|<span data-ttu-id="7ace6-187">LedgerFinancialJournalReportDPBE.processReport</span><span class="sxs-lookup"><span data-stu-id="7ace6-187">LedgerFinancialJournalReportDPBE.processReport</span></span>|
|<span data-ttu-id="7ace6-188">LedgerJournalDP.insertJournalTransForLedgerJournalTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-188">LedgerJournalDP.insertJournalTransForLedgerJournalTable</span></span>|
|<span data-ttu-id="7ace6-189">LedgerJournalDP.insertLedgerJournalTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-189">LedgerJournalDP.insertLedgerJournalTmp</span></span>|
|<span data-ttu-id="7ace6-190">LedgerJournalEngine.newJournalActive</span><span class="sxs-lookup"><span data-stu-id="7ace6-190">LedgerJournalEngine.newJournalActive</span></span>|
|<span data-ttu-id="7ace6-191">LedgerJournalTrans checkAllowPosting</span><span class="sxs-lookup"><span data-stu-id="7ace6-191">LedgerJournalTrans checkAllowPosting</span></span>|
|<span data-ttu-id="7ace6-192">LedgerJournalTransUpdateBank.setBankVoucherSource</span><span class="sxs-lookup"><span data-stu-id="7ace6-192">LedgerJournalTransUpdateBank.setBankVoucherSource</span></span>|
|<span data-ttu-id="7ace6-193">LedgerJournalTransUpdateBank.updateNow</span><span class="sxs-lookup"><span data-stu-id="7ace6-193">LedgerJournalTransUpdateBank.updateNow</span></span>|
|<span data-ttu-id="7ace6-194">LedgerJournalTransUpdateBankLC.addBankVoucher</span><span class="sxs-lookup"><span data-stu-id="7ace6-194">LedgerJournalTransUpdateBankLC.addBankVoucher</span></span>|
|<span data-ttu-id="7ace6-195">LedgerPostingGeneralJournalController.transferLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-195">LedgerPostingGeneralJournalController.transferLines</span></span>|
|<span data-ttu-id="7ace6-196">LedgerPurchaseJournalReportDPBE.insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-196">LedgerPurchaseJournalReportDPBE.insertIntoTempTable</span></span>|
|<span data-ttu-id="7ace6-197">LedgerSalesJournalReportDPBE.processReport</span><span class="sxs-lookup"><span data-stu-id="7ace6-197">LedgerSalesJournalReportDPBE.processReport</span></span>|
|<span data-ttu-id="7ace6-198">LedgerTransFurtherPosting.createLedgerJournalTransFromGenJour</span><span class="sxs-lookup"><span data-stu-id="7ace6-198">LedgerTransFurtherPosting.createLedgerJournalTransFromGenJour</span></span>|
|<span data-ttu-id="7ace6-199">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span><span class="sxs-lookup"><span data-stu-id="7ace6-199">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span></span>|
|<span data-ttu-id="7ace6-200">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span><span class="sxs-lookup"><span data-stu-id="7ace6-200">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span></span>|
|<span data-ttu-id="7ace6-201">LedgerTransVoucher.getVoucherDateRange</span><span class="sxs-lookup"><span data-stu-id="7ace6-201">LedgerTransVoucher.getVoucherDateRange</span></span>|
|<span data-ttu-id="7ace6-202">LedgerVoucherObject.updateLedgerPostingJournal</span><span class="sxs-lookup"><span data-stu-id="7ace6-202">LedgerVoucherObject.updateLedgerPostingJournal</span></span>|
|<span data-ttu-id="7ace6-203">LedgerVoucherTransObject.checkRounding</span><span class="sxs-lookup"><span data-stu-id="7ace6-203">LedgerVoucherTransObject.checkRounding</span></span>|
|<span data-ttu-id="7ace6-204">Markup.insertMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-204">Markup.insertMarkupTrans</span></span>|
|<span data-ttu-id="7ace6-205">MarkupTrans.MarkupTable.MarkupCode.Lookup</span><span class="sxs-lookup"><span data-stu-id="7ace6-205">MarkupTrans.MarkupTable.MarkupCode.Lookup</span></span>|
|<span data-ttu-id="7ace6-206">PaymSchedCalc::init\*</span><span class="sxs-lookup"><span data-stu-id="7ace6-206">PaymSchedCalc::init\*</span></span>|
|<span data-ttu-id="7ace6-207">PaymSchedCalc_Line::createTransaction</span><span class="sxs-lookup"><span data-stu-id="7ace6-207">PaymSchedCalc_Line::createTransaction</span></span>|
|<span data-ttu-id="7ace6-208">PdsApprovedVendorListCheck.newBasedOnTableType</span><span class="sxs-lookup"><span data-stu-id="7ace6-208">PdsApprovedVendorListCheck.newBasedOnTableType</span></span>|
|<span data-ttu-id="7ace6-209">PmfFormulaCoBy.run</span><span class="sxs-lookup"><span data-stu-id="7ace6-209">PmfFormulaCoBy.run</span></span>|
|<span data-ttu-id="7ace6-210">PmfFormulaCoBy.ValidateField</span><span class="sxs-lookup"><span data-stu-id="7ace6-210">PmfFormulaCoBy.ValidateField</span></span>|
|<span data-ttu-id="7ace6-211">PmfProdCoBy.ValidateField</span><span class="sxs-lookup"><span data-stu-id="7ace6-211">PmfProdCoBy.ValidateField</span></span>|
|<span data-ttu-id="7ace6-212">PmfProdCoBy.ValidateWrite</span><span class="sxs-lookup"><span data-stu-id="7ace6-212">PmfProdCoBy.ValidateWrite</span></span>|
|<span data-ttu-id="7ace6-213">PriceDiscAdmSearch</span><span class="sxs-lookup"><span data-stu-id="7ace6-213">PriceDiscAdmSearch</span></span>|
|<span data-ttu-id="7ace6-214">PriceDiscPolicyDialog.runPolicyDialog</span><span class="sxs-lookup"><span data-stu-id="7ace6-214">PriceDiscPolicyDialog.runPolicyDialog</span></span>|
|<span data-ttu-id="7ace6-215">ProdBOM.checkIsItemsReleased</span><span class="sxs-lookup"><span data-stu-id="7ace6-215">ProdBOM.checkIsItemsReleased</span></span>|
|<span data-ttu-id="7ace6-216">ProdBOM::update</span><span class="sxs-lookup"><span data-stu-id="7ace6-216">ProdBOM::update</span></span>|
|<span data-ttu-id="7ace6-217">ProdJournalProd.Insert</span><span class="sxs-lookup"><span data-stu-id="7ace6-217">ProdJournalProd.Insert</span></span>|
|<span data-ttu-id="7ace6-218">ProdPurch.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-218">ProdPurch.createPurchTable</span></span>|
|<span data-ttu-id="7ace6-219">ProdUpdHistoricalCost_Process.checkValidCoBy</span><span class="sxs-lookup"><span data-stu-id="7ace6-219">ProdUpdHistoricalCost_Process.checkValidCoBy</span></span>|
|<span data-ttu-id="7ace6-220">ProdUpdReportFinished::updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="7ace6-220">ProdUpdReportFinished::updateBOMConsumption</span></span>|
|<span data-ttu-id="7ace6-221">ProdUpdStartUp,getListOfBOMJournals</span><span class="sxs-lookup"><span data-stu-id="7ace6-221">ProdUpdStartUp,getListOfBOMJournals</span></span>|
|<span data-ttu-id="7ace6-222">ProdUpdStatusDecrease_StartUp.reverseBOMStartUp</span><span class="sxs-lookup"><span data-stu-id="7ace6-222">ProdUpdStatusDecrease_StartUp.reverseBOMStartUp</span></span>|
|<span data-ttu-id="7ace6-223">ProjBudgetParticipantProvider.resolveByProject</span><span class="sxs-lookup"><span data-stu-id="7ace6-223">ProjBudgetParticipantProvider.resolveByProject</span></span>|
|<span data-ttu-id="7ace6-224">ProjBudgetParticipantProvider.resolveByProjectHierarchy</span><span class="sxs-lookup"><span data-stu-id="7ace6-224">ProjBudgetParticipantProvider.resolveByProjectHierarchy</span></span>|
|<span data-ttu-id="7ace6-225">ProjBudgetParticipantProvider.resolveByRootProject</span><span class="sxs-lookup"><span data-stu-id="7ace6-225">ProjBudgetParticipantProvider.resolveByRootProject</span></span>|
|<span data-ttu-id="7ace6-226">ProjCaseActivitiesHandler.smmActivities_onValidatedDelete</span><span class="sxs-lookup"><span data-stu-id="7ace6-226">ProjCaseActivitiesHandler.smmActivities_onValidatedDelete</span></span>|
|<span data-ttu-id="7ace6-227">ProjControlPeriod.forecast</span><span class="sxs-lookup"><span data-stu-id="7ace6-227">ProjControlPeriod.forecast</span></span>|
|<span data-ttu-id="7ace6-228">ProjControlPeriod.forecast</span><span class="sxs-lookup"><span data-stu-id="7ace6-228">ProjControlPeriod.forecast</span></span>|
|<span data-ttu-id="7ace6-229">ProjControlPeriodCostGroup.totalBudgetMinusActual</span><span class="sxs-lookup"><span data-stu-id="7ace6-229">ProjControlPeriodCostGroup.totalBudgetMinusActual</span></span>|
|<span data-ttu-id="7ace6-230">ProjControlPeriodCostGroup.totalBudgetMinusActual</span><span class="sxs-lookup"><span data-stu-id="7ace6-230">ProjControlPeriodCostGroup.totalBudgetMinusActual</span></span>|
|<span data-ttu-id="7ace6-231">ProjectPosting.costLedgerDimension.</span><span class="sxs-lookup"><span data-stu-id="7ace6-231">ProjectPosting.costLedgerDimension.</span></span>|
|<span data-ttu-id="7ace6-232">ProjectPosting.getProjectLedgerDimension.</span><span class="sxs-lookup"><span data-stu-id="7ace6-232">ProjectPosting.getProjectLedgerDimension.</span></span>|
|<span data-ttu-id="7ace6-233">ProjForecastEmpl.initValue</span><span class="sxs-lookup"><span data-stu-id="7ace6-233">ProjForecastEmpl.initValue</span></span>|
|<span data-ttu-id="7ace6-234">ProjForecastReduceHour.constructQuery</span><span class="sxs-lookup"><span data-stu-id="7ace6-234">ProjForecastReduceHour.constructQuery</span></span>|
|<span data-ttu-id="7ace6-235">ProjFundingSource.setInvoiceLocation</span><span class="sxs-lookup"><span data-stu-id="7ace6-235">ProjFundingSource.setInvoiceLocation</span></span>|
|<span data-ttu-id="7ace6-236">ProjGroup.initFromProjType</span><span class="sxs-lookup"><span data-stu-id="7ace6-236">ProjGroup.initFromProjType</span></span>|
|<span data-ttu-id="7ace6-237">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-237">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span></span>|
|<span data-ttu-id="7ace6-238">ProjIntercompanyTransactionSelection.runQuery</span><span class="sxs-lookup"><span data-stu-id="7ace6-238">ProjIntercompanyTransactionSelection.runQuery</span></span>|
|<span data-ttu-id="7ace6-239">ProjIntercompanyTransQuery.buildExpenseQuery</span><span class="sxs-lookup"><span data-stu-id="7ace6-239">ProjIntercompanyTransQuery.buildExpenseQuery</span></span>|
|<span data-ttu-id="7ace6-240">ProjIntercompanyTransQuery.buildHoursQuery</span><span class="sxs-lookup"><span data-stu-id="7ace6-240">ProjIntercompanyTransQuery.buildHoursQuery</span></span>|
|<span data-ttu-id="7ace6-241">ProjIntercompanyTransQuery.buildVendorInvoiceLinesQuery</span><span class="sxs-lookup"><span data-stu-id="7ace6-241">ProjIntercompanyTransQuery.buildVendorInvoiceLinesQuery</span></span>|
|<span data-ttu-id="7ace6-242">ProjInventJournalTransMapForm.checkActivity</span><span class="sxs-lookup"><span data-stu-id="7ace6-242">ProjInventJournalTransMapForm.checkActivity</span></span>||
|<span data-ttu-id="7ace6-243">projInvoiceChooose.setProposalJour</span><span class="sxs-lookup"><span data-stu-id="7ace6-243">projInvoiceChooose.setProposalJour</span></span>|
|<span data-ttu-id="7ace6-244">ProjInvoiceChoose.doRevenue</span><span class="sxs-lookup"><span data-stu-id="7ace6-244">ProjInvoiceChoose.doRevenue</span></span>|
|<span data-ttu-id="7ace6-245">ProjInvoiceChoose.updateInvoiceTotal</span><span class="sxs-lookup"><span data-stu-id="7ace6-245">ProjInvoiceChoose.updateInvoiceTotal</span></span>|
|<span data-ttu-id="7ace6-246">ProjInvoiceProposalCreateLines.isRevenueTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-246">ProjInvoiceProposalCreateLines.isRevenueTrans</span></span>|
|<span data-ttu-id="7ace6-247">ProjInvoiceProposalCreateLinesBase.createProposalTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-247">ProjInvoiceProposalCreateLinesBase.createProposalTrans</span></span>|
|<span data-ttu-id="7ace6-248">ProjInvoiceProposalCreateLinesBase.doOnAccount</span><span class="sxs-lookup"><span data-stu-id="7ace6-248">ProjInvoiceProposalCreateLinesBase.doOnAccount</span></span>|
|<span data-ttu-id="7ace6-249">ProjInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-249">ProjInvoiceTable</span></span>|
|<span data-ttu-id="7ace6-250">ProjLedger.classdeclaration</span><span class="sxs-lookup"><span data-stu-id="7ace6-250">ProjLedger.classdeclaration</span></span>|
|<span data-ttu-id="7ace6-251">ProjPostItemJournal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="7ace6-251">ProjPostItemJournal.projTransCreate</span></span>|
|<span data-ttu-id="7ace6-252">ProjProjectsListPage.CtrlStages</span><span class="sxs-lookup"><span data-stu-id="7ace6-252">ProjProjectsListPage.CtrlStages</span></span>|
|<span data-ttu-id="7ace6-253">ProjProjectsListPageInteraction.enableButton</span><span class="sxs-lookup"><span data-stu-id="7ace6-253">ProjProjectsListPageInteraction.enableButton</span></span>|
|<span data-ttu-id="7ace6-254">ProjProjectsListPageInteraction.showButton</span><span class="sxs-lookup"><span data-stu-id="7ace6-254">ProjProjectsListPageInteraction.showButton</span></span>|
|<span data-ttu-id="7ace6-255">ProjStatusUpd.main</span><span class="sxs-lookup"><span data-stu-id="7ace6-255">ProjStatusUpd.main</span></span>|
|<span data-ttu-id="7ace6-256">ProjStatusUpd.new</span><span class="sxs-lookup"><span data-stu-id="7ace6-256">ProjStatusUpd.new</span></span>|
|<span data-ttu-id="7ace6-257">ProjTable - ProjTable datasource.write</span><span class="sxs-lookup"><span data-stu-id="7ace6-257">ProjTable - ProjTable datasource.write</span></span>|
|<span data-ttu-id="7ace6-258">ProjTable.clicked</span><span class="sxs-lookup"><span data-stu-id="7ace6-258">ProjTable.clicked</span></span>|
|<span data-ttu-id="7ace6-259">ProjTable.editSubProj</span><span class="sxs-lookup"><span data-stu-id="7ace6-259">ProjTable.editSubProj</span></span>|
|<span data-ttu-id="7ace6-260">ProjTable.editSubProj</span><span class="sxs-lookup"><span data-stu-id="7ace6-260">ProjTable.editSubProj</span></span>|
|<span data-ttu-id="7ace6-261">ProjTableCreate.close</span><span class="sxs-lookup"><span data-stu-id="7ace6-261">ProjTableCreate.close</span></span>|
|<span data-ttu-id="7ace6-262">ProjTableCreate.run</span><span class="sxs-lookup"><span data-stu-id="7ace6-262">ProjTableCreate.run</span></span>|
|<span data-ttu-id="7ace6-263">ProjTableCreate.write</span><span class="sxs-lookup"><span data-stu-id="7ace6-263">ProjTableCreate.write</span></span>|
|<span data-ttu-id="7ace6-264">ProjTableCreate.write</span><span class="sxs-lookup"><span data-stu-id="7ace6-264">ProjTableCreate.write</span></span>|
|<span data-ttu-id="7ace6-265">ProjTableLookup.ProjProjectLookup.init</span><span class="sxs-lookup"><span data-stu-id="7ace6-265">ProjTableLookup.ProjProjectLookup.init</span></span>|
|<span data-ttu-id="7ace6-266">PSAProjInvoiceDP.insertPSAProjInvoiceHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-266">PSAProjInvoiceDP.insertPSAProjInvoiceHeaderTmp</span></span>|
|<span data-ttu-id="7ace6-267">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span><span class="sxs-lookup"><span data-stu-id="7ace6-267">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span></span>|
|<span data-ttu-id="7ace6-268">PsaProjProposalSelection</span><span class="sxs-lookup"><span data-stu-id="7ace6-268">PsaProjProposalSelection</span></span>|
|<span data-ttu-id="7ace6-269">PurchAgreementAutoCreate::construct</span><span class="sxs-lookup"><span data-stu-id="7ace6-269">PurchAgreementAutoCreate::construct</span></span>|
|<span data-ttu-id="7ace6-270">PurchAutoCreate.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-270">PurchAutoCreate.setPurchTable</span></span>|
|<span data-ttu-id="7ace6-271">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-271">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="7ace6-272">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-272">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="7ace6-273">PurchAutoCreate_ReleaseFromAgreement.updateFinDimFromAgreemHeader</span><span class="sxs-lookup"><span data-stu-id="7ace6-273">PurchAutoCreate_ReleaseFromAgreement.updateFinDimFromAgreemHeader</span></span>|
|<span data-ttu-id="7ace6-274">PurchCreateFromSalesOrder.shouldCreatePurchOrder</span><span class="sxs-lookup"><span data-stu-id="7ace6-274">PurchCreateFromSalesOrder.shouldCreatePurchOrder</span></span>|
|<span data-ttu-id="7ace6-275">PurchFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="7ace6-275">PurchFormLetter::main</span></span>|
|<span data-ttu-id="7ace6-276">PurchFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="7ace6-276">PurchFormLetter::main</span></span>|
|<span data-ttu-id="7ace6-277">PurchFormletterParmDataPackingSlip::reSelectLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-277">PurchFormletterParmDataPackingSlip::reSelectLines</span></span>|
|<span data-ttu-id="7ace6-278">PurchFormletterParmDataPackingSlip::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-278">PurchFormletterParmDataPackingSlip::selectChooseLines</span></span>|
|<span data-ttu-id="7ace6-279">PurchFormletterParmDataPurchOrder::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-279">PurchFormletterParmDataPurchOrder::selectChooseLines</span></span>|
|<span data-ttu-id="7ace6-280">PurchInvoiceJournalPost.checkBeforePostingLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-280">PurchInvoiceJournalPost.checkBeforePostingLine</span></span> |
|<span data-ttu-id="7ace6-281">PurchInvoiceJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-281">PurchInvoiceJournalPost.updateSourceLine</span></span> |
|<span data-ttu-id="7ace6-282">Purchline.createline</span><span class="sxs-lookup"><span data-stu-id="7ace6-282">Purchline.createline</span></span>|
|<span data-ttu-id="7ace6-283">PurchOrderLineBudgetControlPolicy.canCheckBudget</span><span class="sxs-lookup"><span data-stu-id="7ace6-283">PurchOrderLineBudgetControlPolicy.canCheckBudget</span></span>|
|<span data-ttu-id="7ace6-284">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-284">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span></span>|
|<span data-ttu-id="7ace6-285">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-285">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span></span>|
|<span data-ttu-id="7ace6-286">PurchRFQAcceptJournalPost.updatePurchReq</span><span class="sxs-lookup"><span data-stu-id="7ace6-286">PurchRFQAcceptJournalPost.updatePurchReq</span></span>|
|<span data-ttu-id="7ace6-287">ReqCalc.covCalcDim</span><span class="sxs-lookup"><span data-stu-id="7ace6-287">ReqCalc.covCalcDim</span></span>|
|<span data-ttu-id="7ace6-288">ReqTrans.createTransferDemand</span><span class="sxs-lookup"><span data-stu-id="7ace6-288">ReqTrans.createTransferDemand</span></span>|
|<span data-ttu-id="7ace6-289">ReqTransPoMarkFirm.createProdRoute</span><span class="sxs-lookup"><span data-stu-id="7ace6-289">ReqTransPoMarkFirm.createProdRoute</span></span>|
|<span data-ttu-id="7ace6-290">RetailPeriodicDiscount.ClassDeclaration</span><span class="sxs-lookup"><span data-stu-id="7ace6-290">RetailPeriodicDiscount.ClassDeclaration</span></span>|
|<span data-ttu-id="7ace6-291">RetailTransactionServiceOrders.cancelCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="7ace6-291">RetailTransactionServiceOrders.cancelCustomerOrder</span></span>|
|<span data-ttu-id="7ace6-292">Return.ReturnDispositionCodeId::validate</span><span class="sxs-lookup"><span data-stu-id="7ace6-292">Return.ReturnDispositionCodeId::validate</span></span>|
|<span data-ttu-id="7ace6-293">SalesAutoCreate::construct</span><span class="sxs-lookup"><span data-stu-id="7ace6-293">SalesAutoCreate::construct</span></span>|
|<span data-ttu-id="7ace6-294">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="7ace6-294">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="7ace6-295">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="7ace6-295">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="7ace6-296">SalesFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="7ace6-296">SalesFormLetter::main</span></span>|
|<span data-ttu-id="7ace6-297">SalesFormletterParmDataConfirm::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-297">SalesFormletterParmDataConfirm::selectChooseLines</span></span>|
|<span data-ttu-id="7ace6-298">SalesFormletterParmDataInvoice::mayJournalTransBePosted</span><span class="sxs-lookup"><span data-stu-id="7ace6-298">SalesFormletterParmDataInvoice::mayJournalTransBePosted</span></span>|
|<span data-ttu-id="7ace6-299">SalesFormletterParmDataInvoice::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-299">SalesFormletterParmDataInvoice::selectChooseLines</span></span>|
|<span data-ttu-id="7ace6-300">SalesFormLetterParmDataPackingSlip::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-300">SalesFormletterParmDataPackingslip::selectChooseLines</span></span>|
|<span data-ttu-id="7ace6-301">SalesInvoiceDP.insertIntoSalesInvoiceTmp,insertIntoSalesInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-301">SalesInvoiceDP.insertIntoSalesInvoiceTmp,insertIntoSalesInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="7ace6-302">SalesInvoiceJournalCreate.createJournalLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-302">SalesInvoiceJournalCreate.createJournalLine</span></span>|
|<span data-ttu-id="7ace6-303">SalesLine.CheckItemId</span><span class="sxs-lookup"><span data-stu-id="7ace6-303">SalesLine.CheckItemId</span></span>|
|<span data-ttu-id="7ace6-304">SalesLine.ValidateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="7ace6-304">SalesLine.ValidateWrite_Server</span></span>|
|<span data-ttu-id="7ace6-305">SalesLine::calcLineAvailQty</span><span class="sxs-lookup"><span data-stu-id="7ace6-305">SalesLine::calcLineAvailQty</span></span>|
|<span data-ttu-id="7ace6-306">SalesLine::createFromTmpFrmVirtualIL</span><span class="sxs-lookup"><span data-stu-id="7ace6-306">SalesLine::createFromTmpFrmVirtualIL</span></span>|
|<span data-ttu-id="7ace6-307">SalesLineType.SalesLineType</span><span class="sxs-lookup"><span data-stu-id="7ace6-307">SalesLineType.SalesLineType</span></span>|
|<span data-ttu-id="7ace6-308">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-308">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="7ace6-309">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-309">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span></span>|
|<span data-ttu-id="7ace6-310">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span><span class="sxs-lookup"><span data-stu-id="7ace6-310">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span></span>|
|<span data-ttu-id="7ace6-311">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span><span class="sxs-lookup"><span data-stu-id="7ace6-311">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span></span>|
|<span data-ttu-id="7ace6-312">SalesPackingSlipJournalPost.updateInventory</span><span class="sxs-lookup"><span data-stu-id="7ace6-312">SalesPackingSlipJournalPost.updateInventory</span></span>|
|<span data-ttu-id="7ace6-313">SalesQuotationLineType_Proj.validateProjTransTypeItem</span><span class="sxs-lookup"><span data-stu-id="7ace6-313">SalesQuotationLineType_Proj.validateProjTransTypeItem</span></span>|
|<span data-ttu-id="7ace6-314">SalesQuotationProjTable データ ソース SalesQuotationline</span><span class="sxs-lookup"><span data-stu-id="7ace6-314">SalesQuotationProjTable data source SalesQuotationline</span></span>|
|<span data-ttu-id="7ace6-315">SalesQuotationTableForm.createABSFromTemplate</span><span class="sxs-lookup"><span data-stu-id="7ace6-315">SalesQuotationTableForm.createABSFromTemplate</span></span>|
|<span data-ttu-id="7ace6-316">SalesTable.setLocation</span><span class="sxs-lookup"><span data-stu-id="7ace6-316">SalesTable.setLocation</span></span>|
|<span data-ttu-id="7ace6-317">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="7ace6-317">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="7ace6-318">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="7ace6-318">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="7ace6-319">SalesTable2LineUpdatePrompt.initpriceDiscUpdateTriggers</span><span class="sxs-lookup"><span data-stu-id="7ace6-319">SalesTable2LineUpdatePrompt.initpriceDiscUpdateTriggers</span></span>|
|<span data-ttu-id="7ace6-320">smmActivitiesEventHandler</span><span class="sxs-lookup"><span data-stu-id="7ace6-320">smmActivitiesEventHandler</span></span>|
|<span data-ttu-id="7ace6-321">SuppitemTable Table Cache Lookup プロパティ</span><span class="sxs-lookup"><span data-stu-id="7ace6-321">SuppitemTable Table Cache Lookup property</span></span>|
|<span data-ttu-id="7ace6-322">テーブル PurchPrepayTable.updateAdvanceApplicationRemaining</span><span class="sxs-lookup"><span data-stu-id="7ace6-322">Table PurchPrepayTable.updateAdvanceApplicationRemaining</span></span>|
|<span data-ttu-id="7ace6-323">TransactionReversal_Cust.reversal</span><span class="sxs-lookup"><span data-stu-id="7ace6-323">TransactionReversal_Cust.reversal</span></span>|
|<span data-ttu-id="7ace6-324">TransactionReversal_Cust.reversal</span><span class="sxs-lookup"><span data-stu-id="7ace6-324">TransactionReversal_Cust.reversal</span></span>|
|<span data-ttu-id="7ace6-325">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="7ace6-325">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="7ace6-326">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="7ace6-326">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="7ace6-327">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="7ace6-327">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="7ace6-328">TsTimesheetAddFavorites.addToFavorites</span><span class="sxs-lookup"><span data-stu-id="7ace6-328">TsTimesheetAddFavorites.addToFavorites</span></span>|
|<span data-ttu-id="7ace6-329">TsTimesheetCreate.createTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-329">TsTimesheetCreate.createTimesheetLine</span></span>|
|<span data-ttu-id="7ace6-330">TSTimesheetEntry.initFields</span><span class="sxs-lookup"><span data-stu-id="7ace6-330">TSTimesheetEntry.initFields</span></span>|
|<span data-ttu-id="7ace6-331">TSTimesheetFavorites.createTimesheetLines</span><span class="sxs-lookup"><span data-stu-id="7ace6-331">TSTimesheetFavorites.createTimesheetLines</span></span>|
|<span data-ttu-id="7ace6-332">TSTimesheetLine.setCategoryIdFromActivity</span><span class="sxs-lookup"><span data-stu-id="7ace6-332">TSTimesheetLine.setCategoryIdFromActivity</span></span>|
|<span data-ttu-id="7ace6-333">VendInvoiceDocumentDP.insertVendInvoiceDocumentTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-333">VendInvoiceDocumentDP.insertVendInvoiceDocumentTmp</span></span>|
|<span data-ttu-id="7ace6-334">WHSLoadLine.validateStatus</span><span class="sxs-lookup"><span data-stu-id="7ace6-334">WHSLoadLine.validateStatus</span></span>|
|<span data-ttu-id="7ace6-335">WHSLoadLineAllocationProcessor.allocateLoadLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-335">WHSLoadLineAllocationProcessor.allocateLoadLine</span></span>|
|<span data-ttu-id="7ace6-336">WHSPostEngine.validateAnyDimAboveLocationMissing</span><span class="sxs-lookup"><span data-stu-id="7ace6-336">WHSPostEngine.validateAnyDimAboveLocationMissing</span></span>|
|<span data-ttu-id="7ace6-337">WhsWarehouseRelease.createShipmentsForAllSalesOrders</span><span class="sxs-lookup"><span data-stu-id="7ace6-337">WhsWarehouseRelease.createShipmentsForAllSalesOrders</span></span>|
|<span data-ttu-id="7ace6-338">WhsWarehouseRelease.createShipmentsForTransferOrders</span><span class="sxs-lookup"><span data-stu-id="7ace6-338">WhsWarehouseRelease.createShipmentsForTransferOrders</span></span>|
|<span data-ttu-id="7ace6-339">WhsWorkCreateLP.createTempTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-339">WhsWorkCreateLP.createTempTable</span></span>|
|<span data-ttu-id="7ace6-340">WHSWorkCreateProdPut.createTempTable</span><span class="sxs-lookup"><span data-stu-id="7ace6-340">WHSWorkCreateProdPut.createTempTable</span></span>|
|<span data-ttu-id="7ace6-341">WHSWorkExecuteDisplay.buildNextDimensionCaptureControl</span><span class="sxs-lookup"><span data-stu-id="7ace6-341">WHSWorkExecuteDisplay.buildNextDimensionCaptureControl</span></span>|
|<span data-ttu-id="7ace6-342">WHSWorkLine::cancelLine</span><span class="sxs-lookup"><span data-stu-id="7ace6-342">WHSWorkLine::cancelLine</span></span>|
|<span data-ttu-id="7ace6-343">WmsArrivalCreateJournal::createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="7ace6-343">WmsArrivalCreateJournal::createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="7ace6-344">WmsArrivalOverviewGeneration::updateOverviewInformation</span><span class="sxs-lookup"><span data-stu-id="7ace6-344">WmsArrivalOverviewGeneration::updateOverviewInformation</span></span>|
|<span data-ttu-id="7ace6-345">WmsJournalCheckPostReception::initJournal</span><span class="sxs-lookup"><span data-stu-id="7ace6-345">WmsJournalCheckPostReception::initJournal</span></span>|
|<span data-ttu-id="7ace6-346">WMSOrderTrans::adjustQtyWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-346">WMSOrderTrans::adjustQtyWMSOrderTrans</span></span>|
|<span data-ttu-id="7ace6-347">WMSOrderTrans::createNewWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-347">WMSOrderTrans::createNewWMSOrderTrans</span></span>|
|<span data-ttu-id="7ace6-348">WMSOrderTrans::insertOrUpdate</span><span class="sxs-lookup"><span data-stu-id="7ace6-348">WMSOrderTrans::insertOrUpdate</span></span>|
|<span data-ttu-id="7ace6-349">WMSOrderTrans::updateWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="7ace6-349">WMSOrderTrans::updateWMSOrderTrans</span></span>|
|<span data-ttu-id="7ace6-350">WmsPickingList_OrderPickDP.insertIntoTempTable,setWMSPickingList_OrderPickTmpTemplate</span><span class="sxs-lookup"><span data-stu-id="7ace6-350">WmsPickingList_OrderPickDP.insertIntoTempTable,setWMSPickingList_OrderPickTmpTemplate</span></span>|
|<span data-ttu-id="7ace6-351">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span><span class="sxs-lookup"><span data-stu-id="7ace6-351">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span></span>|
|<span data-ttu-id="7ace6-352">WrkCtrlScheduler_Proj.loadJob</span><span class="sxs-lookup"><span data-stu-id="7ace6-352">WrkCtrlScheduler_Proj.loadJob</span></span>|
|<span data-ttu-id="7ace6-353">WrkCtrScheduler_Prod.saveOperation</span><span class="sxs-lookup"><span data-stu-id="7ace6-353">WrkCtrScheduler_Prod.saveOperation</span></span>|
|<span data-ttu-id="7ace6-354">WrkCtrScheduler_Prod.saveOrder</span><span class="sxs-lookup"><span data-stu-id="7ace6-354">WrkCtrScheduler_Prod.saveOrder</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="7ace6-355">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="7ace6-355">Enumerations made extensible</span></span>

<span data-ttu-id="7ace6-356">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="7ace6-356">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="7ace6-357">列挙型</span><span class="sxs-lookup"><span data-stu-id="7ace6-357">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="7ace6-358">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="7ace6-358">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="7ace6-359">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="7ace6-359">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="7ace6-360">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="7ace6-360">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="7ace6-361">ItemNumAlternative</span><span class="sxs-lookup"><span data-stu-id="7ace6-361">ItemNumAlternative</span></span>|
|<span data-ttu-id="7ace6-362">JmgRegistrationErrorMode</span><span class="sxs-lookup"><span data-stu-id="7ace6-362">JmgRegistrationErrorMode</span></span>|
|<span data-ttu-id="7ace6-363">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="7ace6-363">MCRCustSearchType</span></span>|
|<span data-ttu-id="7ace6-364">ModuleSalesPurch</span><span class="sxs-lookup"><span data-stu-id="7ace6-364">ModuleSalesPurch</span></span>|
|<span data-ttu-id="7ace6-365">ModuleSalesPurch</span><span class="sxs-lookup"><span data-stu-id="7ace6-365">ModuleSalesPurch</span></span>|
|<span data-ttu-id="7ace6-366">ProjStatusRule</span><span class="sxs-lookup"><span data-stu-id="7ace6-366">ProjStatusRule</span></span>|
|<span data-ttu-id="7ace6-367">PurchRFQUpdateType</span><span class="sxs-lookup"><span data-stu-id="7ace6-367">PurchRFQUpdateType</span></span>|
|<span data-ttu-id="7ace6-368">TAMVendRebateItemCode</span><span class="sxs-lookup"><span data-stu-id="7ace6-368">TAMVendRebateItemCode</span></span>|
|<span data-ttu-id="7ace6-369">TMSLoadBuildSupplyDemandType</span><span class="sxs-lookup"><span data-stu-id="7ace6-369">TMSLoadBuildSupplyDemandType</span></span>|


## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="7ace6-370">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="7ace6-370">Additional extensibility enhancements</span></span>

<span data-ttu-id="7ace6-371">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="7ace6-371">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="7ace6-372">EcoResProductSearchName の EDT の文字列のサイズを増加</span><span class="sxs-lookup"><span data-stu-id="7ace6-372">Increase EDT string size for EcoResProductSearchName</span></span>
- <span data-ttu-id="7ace6-373">AssetLedgerAccounts の CacheLookup プロパティを NotInTTS に変更します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-373">Change CacheLookup property to NotInTTS for AssetLedgerAccounts</span></span>
- <span data-ttu-id="7ace6-374">TaxOnItem、TaxJurisdiction、TaxGroupData、TaxData、およびAssetLedgerAcounts で CacheLookup プロパティを検出に変更します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-374">Change CacheLookup property to Found on TaxOnItem, TaxJurisdiction, TaxGroupData, and TaxData, and AssetLedgerAcounts</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]