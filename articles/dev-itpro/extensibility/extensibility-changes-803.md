---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 08/03/2018
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
ms.dyn365.ops.version: App 8.0.3
ms.openlocfilehash: e665277f718c5302618393b080d989fe05888966
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544116"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-803"></a><span data-ttu-id="05f16-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="05f16-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.3</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05f16-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="05f16-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.3.</span></span> <span data-ttu-id="05f16-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05f16-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="05f16-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="05f16-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="05f16-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="05f16-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="05f16-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="05f16-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="05f16-109">AccountingSourceExplorerProcessor.filterEntries</span><span class="sxs-lookup"><span data-stu-id="05f16-109">AccountingSourceExplorerProcessor.filterEntries</span></span>|
|<span data-ttu-id="05f16-110">AgreementClassification.init</span><span class="sxs-lookup"><span data-stu-id="05f16-110">AgreementClassification.init</span></span>|
|<span data-ttu-id="05f16-111">AgreementConfirm.createLineVolumeCommittmentHistory</span><span class="sxs-lookup"><span data-stu-id="05f16-111">AgreementConfirm.createLineVolumeCommittmentHistory</span></span>|
|<span data-ttu-id="05f16-112">AgreementConfirm.newAgreementConfirm</span><span class="sxs-lookup"><span data-stu-id="05f16-112">AgreementConfirm.newAgreementConfirm</span></span>|
|<span data-ttu-id="05f16-113">Agreementline.findLineForAutoMatch</span><span class="sxs-lookup"><span data-stu-id="05f16-113">Agreementline.findLineForAutoMatch</span></span>|
|<span data-ttu-id="05f16-114">Agreementline.getAgreementLinesForOrderLine</span><span class="sxs-lookup"><span data-stu-id="05f16-114">Agreementline.getAgreementLinesForOrderLine</span></span>|
|<span data-ttu-id="05f16-115">AgreementLine.getAgreementLinesForPurchReqLine</span><span class="sxs-lookup"><span data-stu-id="05f16-115">AgreementLine.getAgreementLinesForPurchReqLine</span></span>|
|<span data-ttu-id="05f16-116">Agreementline.getAgreementLinesList</span><span class="sxs-lookup"><span data-stu-id="05f16-116">Agreementline.getAgreementLinesList</span></span>|
|<span data-ttu-id="05f16-117">Bank_FR.checkControlText</span><span class="sxs-lookup"><span data-stu-id="05f16-117">Bank_FR.checkControlText</span></span>|
|<span data-ttu-id="05f16-118">Bank_IT.checkCIN</span><span class="sxs-lookup"><span data-stu-id="05f16-118">Bank_IT.checkCIN</span></span>|
|<span data-ttu-id="05f16-119">Bank_IT.checkRegistrationNum</span><span class="sxs-lookup"><span data-stu-id="05f16-119">Bank_IT.checkRegistrationNum</span></span>|
|<span data-ttu-id="05f16-120">BankAccountTrans.insert</span><span class="sxs-lookup"><span data-stu-id="05f16-120">BankAccountTrans.insert</span></span>|
|<span data-ttu-id="05f16-121">BankAccountTrans.update</span><span class="sxs-lookup"><span data-stu-id="05f16-121">BankAccountTrans.update</span></span>|
|<span data-ttu-id="05f16-122">BankChequeCopy.fillTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="05f16-122">BankChequeCopy.fillTmpChequePrintout</span></span>|
|<span data-ttu-id="05f16-123">BankChequePrint.printDocument</span><span class="sxs-lookup"><span data-stu-id="05f16-123">BankChequePrint.printDocument</span></span>|
|<span data-ttu-id="05f16-124">BankPaymAdviceReportGeneratorVend</span><span class="sxs-lookup"><span data-stu-id="05f16-124">BankPaymAdviceReportGeneratorVend</span></span>|
|<span data-ttu-id="05f16-125">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span><span class="sxs-lookup"><span data-stu-id="05f16-125">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span></span>|
|<span data-ttu-id="05f16-126">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span><span class="sxs-lookup"><span data-stu-id="05f16-126">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span></span>|
|<span data-ttu-id="05f16-127">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span><span class="sxs-lookup"><span data-stu-id="05f16-127">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span></span>|
|<span data-ttu-id="05f16-128">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span><span class="sxs-lookup"><span data-stu-id="05f16-128">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span></span>|
|<span data-ttu-id="05f16-129">BankVoucher.createBankAccountTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-129">BankVoucher.createBankAccountTrans</span></span>|
|<span data-ttu-id="05f16-130">BankVoucher.createBankAccountTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-130">BankVoucher.createBankAccountTrans</span></span>|
|<span data-ttu-id="05f16-131">BomCopyToProd.copyTo</span><span class="sxs-lookup"><span data-stu-id="05f16-131">BomCopyToProd.copyTo</span></span>|
|<span data-ttu-id="05f16-132">BudgetPlanLineFieldActiveViewMapping.getBudgetPlanLineFieldName</span><span class="sxs-lookup"><span data-stu-id="05f16-132">BudgetPlanLineFieldActiveViewMapping.getBudgetPlanLineFieldName</span></span>|
|<span data-ttu-id="05f16-133">BudgetTransaction.openLinesInExcel</span><span class="sxs-lookup"><span data-stu-id="05f16-133">BudgetTransaction.openLinesInExcel</span></span>|
|<span data-ttu-id="05f16-134">ChequeController.init</span><span class="sxs-lookup"><span data-stu-id="05f16-134">ChequeController.init</span></span>|
|<span data-ttu-id="05f16-135">CustAccountStatementExt.main</span><span class="sxs-lookup"><span data-stu-id="05f16-135">CustAccountStatementExt.main</span></span>|
|<span data-ttu-id="05f16-136">CustAccountStatementExtController.includeOnStatement</span><span class="sxs-lookup"><span data-stu-id="05f16-136">CustAccountStatementExtController.includeOnStatement</span></span>|
|<span data-ttu-id="05f16-137">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-137">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span></span>|
|<span data-ttu-id="05f16-138">CustAccountStatementExtController.setCommonData</span><span class="sxs-lookup"><span data-stu-id="05f16-138">CustAccountStatementExtController.setCommonData</span></span>|
|<span data-ttu-id="05f16-139">CustAccountStatementExtController.tmpCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-139">CustAccountStatementExtController.tmpCustVendTrans</span></span>|
|<span data-ttu-id="05f16-140">CustAccountStatementExtUIBuilder.build</span><span class="sxs-lookup"><span data-stu-id="05f16-140">CustAccountStatementExtUIBuilder.build</span></span>|
|<span data-ttu-id="05f16-141">CustAuditorDP.setCustAuditorTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-141">CustAuditorDP.setCustAuditorTmp</span></span>|
|<span data-ttu-id="05f16-142">CustCollectionJourDP.insertCustCollectionJourDP</span><span class="sxs-lookup"><span data-stu-id="05f16-142">CustCollectionJourDP.insertCustCollectionJourDP</span></span>|
|<span data-ttu-id="05f16-143">CustCreditLimit.Balance</span><span class="sxs-lookup"><span data-stu-id="05f16-143">CustCreditLimit.Balance</span></span>|
|<span data-ttu-id="05f16-144">CustInterestNoteDp.processReport</span><span class="sxs-lookup"><span data-stu-id="05f16-144">CustInterestNoteDp.processReport</span></span>|
|<span data-ttu-id="05f16-145">CustInvoiceJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="05f16-145">CustInvoiceJour.printJournal</span></span>|
|<span data-ttu-id="05f16-146">CustInvoiceTable.checkCreditLimit</span><span class="sxs-lookup"><span data-stu-id="05f16-146">CustInvoiceTable.checkCreditLimit</span></span>|
|<span data-ttu-id="05f16-147">CustPackingSlipJour.interCompanyUpdate</span><span class="sxs-lookup"><span data-stu-id="05f16-147">CustPackingSlipJour.interCompanyUpdate</span></span>|
|<span data-ttu-id="05f16-148">CustPaymEntry.updateConditionalControls</span><span class="sxs-lookup"><span data-stu-id="05f16-148">CustPaymEntry.updateConditionalControls</span></span>|
|<span data-ttu-id="05f16-149">custPostInvoicejob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="05f16-149">custPostInvoicejob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="05f16-150">CustTrans.reverseTransact</span><span class="sxs-lookup"><span data-stu-id="05f16-150">CustTrans.reverseTransact</span></span>|
|<span data-ttu-id="05f16-151">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-151">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="05f16-152">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-152">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="05f16-153">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="05f16-153">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="05f16-154">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="05f16-154">CustVendCheque.output</span></span>|
|<span data-ttu-id="05f16-155">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="05f16-155">CustVendCheque.output</span></span>|
|<span data-ttu-id="05f16-156">CustVendChequeSlipTextCalculator.getChequeDocLength</span><span class="sxs-lookup"><span data-stu-id="05f16-156">CustVendChequeSlipTextCalculator.getChequeDocLength</span></span>|
|<span data-ttu-id="05f16-157">CustVendSumForPaym.validateSEPATransaction</span><span class="sxs-lookup"><span data-stu-id="05f16-157">CustVendSumForPaym.validateSEPATransaction</span></span>|
|<span data-ttu-id="05f16-158">CustVendSumUpJournal.createTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-158">CustVendSumUpJournal.createTrans</span></span>|
|<span data-ttu-id="05f16-159">CustVendVoucher.post</span><span class="sxs-lookup"><span data-stu-id="05f16-159">CustVendVoucher.post</span></span>|
|<span data-ttu-id="05f16-160">DimDerDistRuleProjectTimesheetsExt.populateDimAllocListIntercompany</span><span class="sxs-lookup"><span data-stu-id="05f16-160">DimDerDistRuleProjectTimesheetsExt.populateDimAllocListIntercompany</span></span>|
|<span data-ttu-id="05f16-161">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span><span class="sxs-lookup"><span data-stu-id="05f16-161">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span></span>|
|<span data-ttu-id="05f16-162">DirPartyVerification.selectionChanged</span><span class="sxs-lookup"><span data-stu-id="05f16-162">DirPartyVerification.selectionChanged</span></span>|
|<span data-ttu-id="05f16-163">EcoResCategoryTreeDatasource.initializeAvailableCategoriesMap</span><span class="sxs-lookup"><span data-stu-id="05f16-163">EcoResCategoryTreeDatasource.initializeAvailableCategoriesMap</span></span>|
|<span data-ttu-id="05f16-164">EcoResProductCreate.writeMoreFields</span><span class="sxs-lookup"><span data-stu-id="05f16-164">EcoResProductCreate.writeMoreFields</span></span>|
|<span data-ttu-id="05f16-165">EcoResProductDetailsExtended.initInventDimensionsMetadataEntries</span><span class="sxs-lookup"><span data-stu-id="05f16-165">EcoResProductDetailsExtended.initInventDimensionsMetadataEntries</span></span>|
|<span data-ttu-id="05f16-166">ElectronicPaymentRemitExport_BR.construct</span><span class="sxs-lookup"><span data-stu-id="05f16-166">ElectronicPaymentRemitExport_BR.construct</span></span>|
|<span data-ttu-id="05f16-167">ForecastPuch</span><span class="sxs-lookup"><span data-stu-id="05f16-167">ForecastPuch</span></span>|
|<span data-ttu-id="05f16-168">ForecastSales.accountConsumption</span><span class="sxs-lookup"><span data-stu-id="05f16-168">ForecastSales.accountConsumption</span></span>|
|<span data-ttu-id="05f16-169">ForecastSales.accountDisc</span><span class="sxs-lookup"><span data-stu-id="05f16-169">ForecastSales.accountDisc</span></span>|
|<span data-ttu-id="05f16-170">ForecastSales.accountIssue</span><span class="sxs-lookup"><span data-stu-id="05f16-170">ForecastSales.accountIssue</span></span>|
|<span data-ttu-id="05f16-171">ForecastSales.accountSales</span><span class="sxs-lookup"><span data-stu-id="05f16-171">ForecastSales.accountSales</span></span>|
|<span data-ttu-id="05f16-172">InventPosting.accountItemLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="05f16-172">InventPosting.accountItemLedgerDimension</span></span>|
|<span data-ttu-id="05f16-173">InventSupply.init</span><span class="sxs-lookup"><span data-stu-id="05f16-173">InventSupply.init</span></span>|
|<span data-ttu-id="05f16-174">InventTrans.insertReturnTransOrigin</span><span class="sxs-lookup"><span data-stu-id="05f16-174">InventTrans.insertReturnTransOrigin</span></span>|
|<span data-ttu-id="05f16-175">InventTransferParmLine - いくつかの方法</span><span class="sxs-lookup"><span data-stu-id="05f16-175">InventTransferParmLine - several methods</span></span>|
|<span data-ttu-id="05f16-176">InventTransferUpd::updateLines</span><span class="sxs-lookup"><span data-stu-id="05f16-176">InventTransferUpd::updateLines</span></span>|
|<span data-ttu-id="05f16-177">InventTransFormHelper.formQueryAddDynalink</span><span class="sxs-lookup"><span data-stu-id="05f16-177">InventTransFormHelper.formQueryAddDynalink</span></span>|
|<span data-ttu-id="05f16-178">InventTransWMS_Pick::updateInventServer</span><span class="sxs-lookup"><span data-stu-id="05f16-178">InventTransWMS_Pick::updateInventServer</span></span>|
|<span data-ttu-id="05f16-179">InventUpd_Physical::updatePhysicalReceiptTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-179">InventUpd_Physical::updatePhysicalReceiptTrans</span></span>|
|<span data-ttu-id="05f16-180">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-180">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="05f16-181">InventUpdate::createInventTransOriginAndReferences</span><span class="sxs-lookup"><span data-stu-id="05f16-181">InventUpdate::createInventTransOriginAndReferences</span></span>|
|<span data-ttu-id="05f16-182">InventValueReportPopulateItem::findReportLine</span><span class="sxs-lookup"><span data-stu-id="05f16-182">InventValueReportPopulateItem::findReportLine</span></span>|
|<span data-ttu-id="05f16-183">JmgRegistration.JmgJobTable</span><span class="sxs-lookup"><span data-stu-id="05f16-183">JmgRegistration.JmgJobTable</span></span>|
|<span data-ttu-id="05f16-184">JournalizingDefinitionManager.newJournalizingDefinitionManagerPurch</span><span class="sxs-lookup"><span data-stu-id="05f16-184">JournalizingDefinitionManager.newJournalizingDefinitionManagerPurch</span></span>|
|<span data-ttu-id="05f16-185">JournalStatic.initializeDataModel</span><span class="sxs-lookup"><span data-stu-id="05f16-185">JournalStatic.initializeDataModel</span></span>|
|<span data-ttu-id="05f16-186">LedgerFinancialJournalReportDPBE.calcDebCredTotals</span><span class="sxs-lookup"><span data-stu-id="05f16-186">LedgerFinancialJournalReportDPBE.calcDebCredTotals</span></span>|
|<span data-ttu-id="05f16-187">LedgerFinancialJournalReportDPBE.processReport</span><span class="sxs-lookup"><span data-stu-id="05f16-187">LedgerFinancialJournalReportDPBE.processReport</span></span>|
|<span data-ttu-id="05f16-188">LedgerJournalDP.insertJournalTransForLedgerJournalTable</span><span class="sxs-lookup"><span data-stu-id="05f16-188">LedgerJournalDP.insertJournalTransForLedgerJournalTable</span></span>|
|<span data-ttu-id="05f16-189">LedgerJournalDP.insertLedgerJournalTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-189">LedgerJournalDP.insertLedgerJournalTmp</span></span>|
|<span data-ttu-id="05f16-190">LedgerJournalEngine.newJournalActive</span><span class="sxs-lookup"><span data-stu-id="05f16-190">LedgerJournalEngine.newJournalActive</span></span>|
|<span data-ttu-id="05f16-191">LedgerJournalTrans checkAllowPosting</span><span class="sxs-lookup"><span data-stu-id="05f16-191">LedgerJournalTrans checkAllowPosting</span></span>|
|<span data-ttu-id="05f16-192">LedgerJournalTransUpdateBank.setBankVoucherSource</span><span class="sxs-lookup"><span data-stu-id="05f16-192">LedgerJournalTransUpdateBank.setBankVoucherSource</span></span>|
|<span data-ttu-id="05f16-193">LedgerJournalTransUpdateBank.updateNow</span><span class="sxs-lookup"><span data-stu-id="05f16-193">LedgerJournalTransUpdateBank.updateNow</span></span>|
|<span data-ttu-id="05f16-194">LedgerJournalTransUpdateBankLC.addBankVoucher</span><span class="sxs-lookup"><span data-stu-id="05f16-194">LedgerJournalTransUpdateBankLC.addBankVoucher</span></span>|
|<span data-ttu-id="05f16-195">LedgerPostingGeneralJournalController.transferLines</span><span class="sxs-lookup"><span data-stu-id="05f16-195">LedgerPostingGeneralJournalController.transferLines</span></span>|
|<span data-ttu-id="05f16-196">LedgerPurchaseJournalReportDPBE.insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="05f16-196">LedgerPurchaseJournalReportDPBE.insertIntoTempTable</span></span>|
|<span data-ttu-id="05f16-197">LedgerSalesJournalReportDPBE.processReport</span><span class="sxs-lookup"><span data-stu-id="05f16-197">LedgerSalesJournalReportDPBE.processReport</span></span>|
|<span data-ttu-id="05f16-198">LedgerTransFurtherPosting.createLedgerJournalTransFromGenJour</span><span class="sxs-lookup"><span data-stu-id="05f16-198">LedgerTransFurtherPosting.createLedgerJournalTransFromGenJour</span></span>|
|<span data-ttu-id="05f16-199">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span><span class="sxs-lookup"><span data-stu-id="05f16-199">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span></span>|
|<span data-ttu-id="05f16-200">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span><span class="sxs-lookup"><span data-stu-id="05f16-200">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span></span>|
|<span data-ttu-id="05f16-201">LedgerTransVoucher.getVoucherDateRange</span><span class="sxs-lookup"><span data-stu-id="05f16-201">LedgerTransVoucher.getVoucherDateRange</span></span>|
|<span data-ttu-id="05f16-202">LedgerVoucherObject.updateLedgerPostingJournal</span><span class="sxs-lookup"><span data-stu-id="05f16-202">LedgerVoucherObject.updateLedgerPostingJournal</span></span>|
|<span data-ttu-id="05f16-203">LedgerVoucherTransObject.checkRounding</span><span class="sxs-lookup"><span data-stu-id="05f16-203">LedgerVoucherTransObject.checkRounding</span></span>|
|<span data-ttu-id="05f16-204">Markup.insertMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-204">Markup.insertMarkupTrans</span></span>|
|<span data-ttu-id="05f16-205">MarkupTrans.MarkupTable.MarkupCode.Lookup</span><span class="sxs-lookup"><span data-stu-id="05f16-205">MarkupTrans.MarkupTable.MarkupCode.Lookup</span></span>|
|<span data-ttu-id="05f16-206">PaymSchedCalc::init\*</span><span class="sxs-lookup"><span data-stu-id="05f16-206">PaymSchedCalc::init\*</span></span>|
|<span data-ttu-id="05f16-207">PaymSchedCalc_Line::createTransaction</span><span class="sxs-lookup"><span data-stu-id="05f16-207">PaymSchedCalc_Line::createTransaction</span></span>|
|<span data-ttu-id="05f16-208">PdsApprovedVendorListCheck.newBasedOnTableType</span><span class="sxs-lookup"><span data-stu-id="05f16-208">PdsApprovedVendorListCheck.newBasedOnTableType</span></span>|
|<span data-ttu-id="05f16-209">PmfFormulaCoBy.run</span><span class="sxs-lookup"><span data-stu-id="05f16-209">PmfFormulaCoBy.run</span></span>|
|<span data-ttu-id="05f16-210">PmfFormulaCoBy.ValidateField</span><span class="sxs-lookup"><span data-stu-id="05f16-210">PmfFormulaCoBy.ValidateField</span></span>|
|<span data-ttu-id="05f16-211">PmfProdCoBy.ValidateField</span><span class="sxs-lookup"><span data-stu-id="05f16-211">PmfProdCoBy.ValidateField</span></span>|
|<span data-ttu-id="05f16-212">PmfProdCoBy.ValidateWrite</span><span class="sxs-lookup"><span data-stu-id="05f16-212">PmfProdCoBy.ValidateWrite</span></span>|
|<span data-ttu-id="05f16-213">PriceDiscAdmSearch</span><span class="sxs-lookup"><span data-stu-id="05f16-213">PriceDiscAdmSearch</span></span>|
|<span data-ttu-id="05f16-214">PriceDiscPolicyDialog.runPolicyDialog</span><span class="sxs-lookup"><span data-stu-id="05f16-214">PriceDiscPolicyDialog.runPolicyDialog</span></span>|
|<span data-ttu-id="05f16-215">ProdBOM.checkIsItemsReleased</span><span class="sxs-lookup"><span data-stu-id="05f16-215">ProdBOM.checkIsItemsReleased</span></span>|
|<span data-ttu-id="05f16-216">ProdBOM::update</span><span class="sxs-lookup"><span data-stu-id="05f16-216">ProdBOM::update</span></span>|
|<span data-ttu-id="05f16-217">ProdJournalProd.Insert</span><span class="sxs-lookup"><span data-stu-id="05f16-217">ProdJournalProd.Insert</span></span>|
|<span data-ttu-id="05f16-218">ProdPurch.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="05f16-218">ProdPurch.createPurchTable</span></span>|
|<span data-ttu-id="05f16-219">ProdUpdHistoricalCost_Process.checkValidCoBy</span><span class="sxs-lookup"><span data-stu-id="05f16-219">ProdUpdHistoricalCost_Process.checkValidCoBy</span></span>|
|<span data-ttu-id="05f16-220">ProdUpdReportFinished::updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="05f16-220">ProdUpdReportFinished::updateBOMConsumption</span></span>|
|<span data-ttu-id="05f16-221">ProdUpdStartUp,getListOfBOMJournals</span><span class="sxs-lookup"><span data-stu-id="05f16-221">ProdUpdStartUp,getListOfBOMJournals</span></span>|
|<span data-ttu-id="05f16-222">ProdUpdStatusDecrease_StartUp.reverseBOMStartUp</span><span class="sxs-lookup"><span data-stu-id="05f16-222">ProdUpdStatusDecrease_StartUp.reverseBOMStartUp</span></span>|
|<span data-ttu-id="05f16-223">ProjBudgetParticipantProvider.resolveByProject</span><span class="sxs-lookup"><span data-stu-id="05f16-223">ProjBudgetParticipantProvider.resolveByProject</span></span>|
|<span data-ttu-id="05f16-224">ProjBudgetParticipantProvider.resolveByProjectHierarchy</span><span class="sxs-lookup"><span data-stu-id="05f16-224">ProjBudgetParticipantProvider.resolveByProjectHierarchy</span></span>|
|<span data-ttu-id="05f16-225">ProjBudgetParticipantProvider.resolveByRootProject</span><span class="sxs-lookup"><span data-stu-id="05f16-225">ProjBudgetParticipantProvider.resolveByRootProject</span></span>|
|<span data-ttu-id="05f16-226">ProjCaseActivitiesHandler.smmActivities_onValidatedDelete</span><span class="sxs-lookup"><span data-stu-id="05f16-226">ProjCaseActivitiesHandler.smmActivities_onValidatedDelete</span></span>|
|<span data-ttu-id="05f16-227">ProjControlPeriod.forecast</span><span class="sxs-lookup"><span data-stu-id="05f16-227">ProjControlPeriod.forecast</span></span>|
|<span data-ttu-id="05f16-228">ProjControlPeriod.forecast</span><span class="sxs-lookup"><span data-stu-id="05f16-228">ProjControlPeriod.forecast</span></span>|
|<span data-ttu-id="05f16-229">ProjControlPeriodCostGroup.totalBudgetMinusActual</span><span class="sxs-lookup"><span data-stu-id="05f16-229">ProjControlPeriodCostGroup.totalBudgetMinusActual</span></span>|
|<span data-ttu-id="05f16-230">ProjControlPeriodCostGroup.totalBudgetMinusActual</span><span class="sxs-lookup"><span data-stu-id="05f16-230">ProjControlPeriodCostGroup.totalBudgetMinusActual</span></span>|
|<span data-ttu-id="05f16-231">ProjectPosting.costLedgerDimension.</span><span class="sxs-lookup"><span data-stu-id="05f16-231">ProjectPosting.costLedgerDimension.</span></span>|
|<span data-ttu-id="05f16-232">ProjectPosting.getProjectLedgerDimension.</span><span class="sxs-lookup"><span data-stu-id="05f16-232">ProjectPosting.getProjectLedgerDimension.</span></span>|
|<span data-ttu-id="05f16-233">ProjForecastEmpl.initValue</span><span class="sxs-lookup"><span data-stu-id="05f16-233">ProjForecastEmpl.initValue</span></span>|
|<span data-ttu-id="05f16-234">ProjForecastReduceHour.constructQuery</span><span class="sxs-lookup"><span data-stu-id="05f16-234">ProjForecastReduceHour.constructQuery</span></span>|
|<span data-ttu-id="05f16-235">ProjFundingSource.setInvoiceLocation</span><span class="sxs-lookup"><span data-stu-id="05f16-235">ProjFundingSource.setInvoiceLocation</span></span>|
|<span data-ttu-id="05f16-236">ProjGroup.initFromProjType</span><span class="sxs-lookup"><span data-stu-id="05f16-236">ProjGroup.initFromProjType</span></span>|
|<span data-ttu-id="05f16-237">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="05f16-237">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span></span>|
|<span data-ttu-id="05f16-238">ProjIntercompanyTransactionSelection.runQuery</span><span class="sxs-lookup"><span data-stu-id="05f16-238">ProjIntercompanyTransactionSelection.runQuery</span></span>|
|<span data-ttu-id="05f16-239">ProjIntercompanyTransQuery.buildExpenseQuery</span><span class="sxs-lookup"><span data-stu-id="05f16-239">ProjIntercompanyTransQuery.buildExpenseQuery</span></span>|
|<span data-ttu-id="05f16-240">ProjIntercompanyTransQuery.buildHoursQuery</span><span class="sxs-lookup"><span data-stu-id="05f16-240">ProjIntercompanyTransQuery.buildHoursQuery</span></span>|
|<span data-ttu-id="05f16-241">ProjIntercompanyTransQuery.buildVendorInvoiceLinesQuery</span><span class="sxs-lookup"><span data-stu-id="05f16-241">ProjIntercompanyTransQuery.buildVendorInvoiceLinesQuery</span></span>|
|<span data-ttu-id="05f16-242">ProjInventJournalTransMapForm.checkActivity</span><span class="sxs-lookup"><span data-stu-id="05f16-242">ProjInventJournalTransMapForm.checkActivity</span></span>||
|<span data-ttu-id="05f16-243">projInvoiceChooose.setProposalJour</span><span class="sxs-lookup"><span data-stu-id="05f16-243">projInvoiceChooose.setProposalJour</span></span>|
|<span data-ttu-id="05f16-244">ProjInvoiceChoose.doRevenue</span><span class="sxs-lookup"><span data-stu-id="05f16-244">ProjInvoiceChoose.doRevenue</span></span>|
|<span data-ttu-id="05f16-245">ProjInvoiceChoose.updateInvoiceTotal</span><span class="sxs-lookup"><span data-stu-id="05f16-245">ProjInvoiceChoose.updateInvoiceTotal</span></span>|
|<span data-ttu-id="05f16-246">ProjInvoiceProposalCreateLines.isRevenueTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-246">ProjInvoiceProposalCreateLines.isRevenueTrans</span></span>|
|<span data-ttu-id="05f16-247">ProjInvoiceProposalCreateLinesBase.createProposalTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-247">ProjInvoiceProposalCreateLinesBase.createProposalTrans</span></span>|
|<span data-ttu-id="05f16-248">ProjInvoiceProposalCreateLinesBase.doOnAccount</span><span class="sxs-lookup"><span data-stu-id="05f16-248">ProjInvoiceProposalCreateLinesBase.doOnAccount</span></span>|
|<span data-ttu-id="05f16-249">ProjInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="05f16-249">ProjInvoiceTable</span></span>|
|<span data-ttu-id="05f16-250">ProjLedger.classdeclaration</span><span class="sxs-lookup"><span data-stu-id="05f16-250">ProjLedger.classdeclaration</span></span>|
|<span data-ttu-id="05f16-251">ProjPostItemJournal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="05f16-251">ProjPostItemJournal.projTransCreate</span></span>|
|<span data-ttu-id="05f16-252">ProjProjectsListPage.CtrlStages</span><span class="sxs-lookup"><span data-stu-id="05f16-252">ProjProjectsListPage.CtrlStages</span></span>|
|<span data-ttu-id="05f16-253">ProjProjectsListPageInteraction.enableButton</span><span class="sxs-lookup"><span data-stu-id="05f16-253">ProjProjectsListPageInteraction.enableButton</span></span>|
|<span data-ttu-id="05f16-254">ProjProjectsListPageInteraction.showButton</span><span class="sxs-lookup"><span data-stu-id="05f16-254">ProjProjectsListPageInteraction.showButton</span></span>|
|<span data-ttu-id="05f16-255">ProjStatusUpd.main</span><span class="sxs-lookup"><span data-stu-id="05f16-255">ProjStatusUpd.main</span></span>|
|<span data-ttu-id="05f16-256">ProjStatusUpd.new</span><span class="sxs-lookup"><span data-stu-id="05f16-256">ProjStatusUpd.new</span></span>|
|<span data-ttu-id="05f16-257">ProjTable - ProjTable datasource.write</span><span class="sxs-lookup"><span data-stu-id="05f16-257">ProjTable - ProjTable datasource.write</span></span>|
|<span data-ttu-id="05f16-258">ProjTable.clicked</span><span class="sxs-lookup"><span data-stu-id="05f16-258">ProjTable.clicked</span></span>|
|<span data-ttu-id="05f16-259">ProjTable.editSubProj</span><span class="sxs-lookup"><span data-stu-id="05f16-259">ProjTable.editSubProj</span></span>|
|<span data-ttu-id="05f16-260">ProjTable.editSubProj</span><span class="sxs-lookup"><span data-stu-id="05f16-260">ProjTable.editSubProj</span></span>|
|<span data-ttu-id="05f16-261">ProjTableCreate.close</span><span class="sxs-lookup"><span data-stu-id="05f16-261">ProjTableCreate.close</span></span>|
|<span data-ttu-id="05f16-262">ProjTableCreate.run</span><span class="sxs-lookup"><span data-stu-id="05f16-262">ProjTableCreate.run</span></span>|
|<span data-ttu-id="05f16-263">ProjTableCreate.write</span><span class="sxs-lookup"><span data-stu-id="05f16-263">ProjTableCreate.write</span></span>|
|<span data-ttu-id="05f16-264">ProjTableCreate.write</span><span class="sxs-lookup"><span data-stu-id="05f16-264">ProjTableCreate.write</span></span>|
|<span data-ttu-id="05f16-265">ProjTableLookup.ProjProjectLookup.init</span><span class="sxs-lookup"><span data-stu-id="05f16-265">ProjTableLookup.ProjProjectLookup.init</span></span>|
|<span data-ttu-id="05f16-266">PSAProjInvoiceDP.insertPSAProjInvoiceHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-266">PSAProjInvoiceDP.insertPSAProjInvoiceHeaderTmp</span></span>|
|<span data-ttu-id="05f16-267">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span><span class="sxs-lookup"><span data-stu-id="05f16-267">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span></span>|
|<span data-ttu-id="05f16-268">PsaProjProposalSelection</span><span class="sxs-lookup"><span data-stu-id="05f16-268">PsaProjProposalSelection</span></span>|
|<span data-ttu-id="05f16-269">PurchAgreementAutoCreate::construct</span><span class="sxs-lookup"><span data-stu-id="05f16-269">PurchAgreementAutoCreate::construct</span></span>|
|<span data-ttu-id="05f16-270">PurchAutoCreate.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="05f16-270">PurchAutoCreate.setPurchTable</span></span>|
|<span data-ttu-id="05f16-271">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="05f16-271">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="05f16-272">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="05f16-272">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="05f16-273">PurchAutoCreate_ReleaseFromAgreement.updateFinDimFromAgreemHeader</span><span class="sxs-lookup"><span data-stu-id="05f16-273">PurchAutoCreate_ReleaseFromAgreement.updateFinDimFromAgreemHeader</span></span>|
|<span data-ttu-id="05f16-274">PurchCreateFromSalesOrder.shouldCreatePurchOrder</span><span class="sxs-lookup"><span data-stu-id="05f16-274">PurchCreateFromSalesOrder.shouldCreatePurchOrder</span></span>|
|<span data-ttu-id="05f16-275">PurchFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="05f16-275">PurchFormLetter::main</span></span>|
|<span data-ttu-id="05f16-276">PurchFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="05f16-276">PurchFormLetter::main</span></span>|
|<span data-ttu-id="05f16-277">PurchFormletterParmDataPackingSlip::reSelectLines</span><span class="sxs-lookup"><span data-stu-id="05f16-277">PurchFormletterParmDataPackingSlip::reSelectLines</span></span>|
|<span data-ttu-id="05f16-278">PurchFormletterParmDataPackingSlip::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="05f16-278">PurchFormletterParmDataPackingSlip::selectChooseLines</span></span>|
|<span data-ttu-id="05f16-279">PurchFormletterParmDataPurchOrder::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="05f16-279">PurchFormletterParmDataPurchOrder::selectChooseLines</span></span>|
|<span data-ttu-id="05f16-280">PurchInvoiceJournalPost.checkBeforePostingLine</span><span class="sxs-lookup"><span data-stu-id="05f16-280">PurchInvoiceJournalPost.checkBeforePostingLine</span></span> |
|<span data-ttu-id="05f16-281">PurchInvoiceJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="05f16-281">PurchInvoiceJournalPost.updateSourceLine</span></span> |
|<span data-ttu-id="05f16-282">Purchline.createline</span><span class="sxs-lookup"><span data-stu-id="05f16-282">Purchline.createline</span></span>|
|<span data-ttu-id="05f16-283">PurchOrderLineBudgetControlPolicy.canCheckBudget</span><span class="sxs-lookup"><span data-stu-id="05f16-283">PurchOrderLineBudgetControlPolicy.canCheckBudget</span></span>|
|<span data-ttu-id="05f16-284">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-284">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span></span>|
|<span data-ttu-id="05f16-285">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-285">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span></span>|
|<span data-ttu-id="05f16-286">PurchRFQAcceptJournalPost.updatePurchReq</span><span class="sxs-lookup"><span data-stu-id="05f16-286">PurchRFQAcceptJournalPost.updatePurchReq</span></span>|
|<span data-ttu-id="05f16-287">ReqCalc.covCalcDim</span><span class="sxs-lookup"><span data-stu-id="05f16-287">ReqCalc.covCalcDim</span></span>|
|<span data-ttu-id="05f16-288">ReqTrans.createTransferDemand</span><span class="sxs-lookup"><span data-stu-id="05f16-288">ReqTrans.createTransferDemand</span></span>|
|<span data-ttu-id="05f16-289">ReqTransPoMarkFirm.createProdRoute</span><span class="sxs-lookup"><span data-stu-id="05f16-289">ReqTransPoMarkFirm.createProdRoute</span></span>|
|<span data-ttu-id="05f16-290">RetailPeriodicDiscount.ClassDeclaration</span><span class="sxs-lookup"><span data-stu-id="05f16-290">RetailPeriodicDiscount.ClassDeclaration</span></span>|
|<span data-ttu-id="05f16-291">RetailTransactionServiceOrders.cancelCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="05f16-291">RetailTransactionServiceOrders.cancelCustomerOrder</span></span>|
|<span data-ttu-id="05f16-292">Return.ReturnDispositionCodeId::validate</span><span class="sxs-lookup"><span data-stu-id="05f16-292">Return.ReturnDispositionCodeId::validate</span></span>|
|<span data-ttu-id="05f16-293">SalesAutoCreate::construct</span><span class="sxs-lookup"><span data-stu-id="05f16-293">SalesAutoCreate::construct</span></span>|
|<span data-ttu-id="05f16-294">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="05f16-294">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="05f16-295">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="05f16-295">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="05f16-296">SalesFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="05f16-296">SalesFormLetter::main</span></span>|
|<span data-ttu-id="05f16-297">SalesFormletterParmDataConfirm::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="05f16-297">SalesFormletterParmDataConfirm::selectChooseLines</span></span>|
|<span data-ttu-id="05f16-298">SalesFormletterParmDataInvoice::mayJournalTransBePosted</span><span class="sxs-lookup"><span data-stu-id="05f16-298">SalesFormletterParmDataInvoice::mayJournalTransBePosted</span></span>|
|<span data-ttu-id="05f16-299">SalesFormletterParmDataInvoice::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="05f16-299">SalesFormletterParmDataInvoice::selectChooseLines</span></span>|
|<span data-ttu-id="05f16-300">SalesFormLetterParmDataPackingSlip::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="05f16-300">SalesFormletterParmDataPackingslip::selectChooseLines</span></span>|
|<span data-ttu-id="05f16-301">SalesInvoiceDP.insertIntoSalesInvoiceTmp,insertIntoSalesInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-301">SalesInvoiceDP.insertIntoSalesInvoiceTmp,insertIntoSalesInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="05f16-302">SalesInvoiceJournalCreate.createJournalLine</span><span class="sxs-lookup"><span data-stu-id="05f16-302">SalesInvoiceJournalCreate.createJournalLine</span></span>|
|<span data-ttu-id="05f16-303">SalesLine.CheckItemId</span><span class="sxs-lookup"><span data-stu-id="05f16-303">SalesLine.CheckItemId</span></span>|
|<span data-ttu-id="05f16-304">SalesLine.ValidateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="05f16-304">SalesLine.ValidateWrite_Server</span></span>|
|<span data-ttu-id="05f16-305">SalesLine::calcLineAvailQty</span><span class="sxs-lookup"><span data-stu-id="05f16-305">SalesLine::calcLineAvailQty</span></span>|
|<span data-ttu-id="05f16-306">SalesLine::createFromTmpFrmVirtualIL</span><span class="sxs-lookup"><span data-stu-id="05f16-306">SalesLine::createFromTmpFrmVirtualIL</span></span>|
|<span data-ttu-id="05f16-307">SalesLineType.SalesLineType</span><span class="sxs-lookup"><span data-stu-id="05f16-307">SalesLineType.SalesLineType</span></span>|
|<span data-ttu-id="05f16-308">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-308">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="05f16-309">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-309">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span></span>|
|<span data-ttu-id="05f16-310">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span><span class="sxs-lookup"><span data-stu-id="05f16-310">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span></span>|
|<span data-ttu-id="05f16-311">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span><span class="sxs-lookup"><span data-stu-id="05f16-311">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span></span>|
|<span data-ttu-id="05f16-312">SalesPackingSlipJournalPost.updateInventory</span><span class="sxs-lookup"><span data-stu-id="05f16-312">SalesPackingSlipJournalPost.updateInventory</span></span>|
|<span data-ttu-id="05f16-313">SalesQuotationLineType_Proj.validateProjTransTypeItem</span><span class="sxs-lookup"><span data-stu-id="05f16-313">SalesQuotationLineType_Proj.validateProjTransTypeItem</span></span>|
|<span data-ttu-id="05f16-314">SalesQuotationProjTable データ ソース SalesQuotationline</span><span class="sxs-lookup"><span data-stu-id="05f16-314">SalesQuotationProjTable data source SalesQuotationline</span></span>|
|<span data-ttu-id="05f16-315">SalesQuotationTableForm.createABSFromTemplate</span><span class="sxs-lookup"><span data-stu-id="05f16-315">SalesQuotationTableForm.createABSFromTemplate</span></span>|
|<span data-ttu-id="05f16-316">SalesTable.setLocation</span><span class="sxs-lookup"><span data-stu-id="05f16-316">SalesTable.setLocation</span></span>|
|<span data-ttu-id="05f16-317">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="05f16-317">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="05f16-318">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="05f16-318">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="05f16-319">SalesTable2LineUpdatePrompt.initpriceDiscUpdateTriggers</span><span class="sxs-lookup"><span data-stu-id="05f16-319">SalesTable2LineUpdatePrompt.initpriceDiscUpdateTriggers</span></span>|
|<span data-ttu-id="05f16-320">smmActivitiesEventHandler</span><span class="sxs-lookup"><span data-stu-id="05f16-320">smmActivitiesEventHandler</span></span>|
|<span data-ttu-id="05f16-321">SuppitemTable Table Cache Lookup プロパティ</span><span class="sxs-lookup"><span data-stu-id="05f16-321">SuppitemTable Table Cache Lookup property</span></span>|
|<span data-ttu-id="05f16-322">テーブル PurchPrepayTable.updateAdvanceApplicationRemaining</span><span class="sxs-lookup"><span data-stu-id="05f16-322">Table PurchPrepayTable.updateAdvanceApplicationRemaining</span></span>|
|<span data-ttu-id="05f16-323">TransactionReversal_Cust.reversal</span><span class="sxs-lookup"><span data-stu-id="05f16-323">TransactionReversal_Cust.reversal</span></span>|
|<span data-ttu-id="05f16-324">TransactionReversal_Cust.reversal</span><span class="sxs-lookup"><span data-stu-id="05f16-324">TransactionReversal_Cust.reversal</span></span>|
|<span data-ttu-id="05f16-325">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="05f16-325">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="05f16-326">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="05f16-326">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="05f16-327">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="05f16-327">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="05f16-328">TsTimesheetAddFavorites.addToFavorites</span><span class="sxs-lookup"><span data-stu-id="05f16-328">TsTimesheetAddFavorites.addToFavorites</span></span>|
|<span data-ttu-id="05f16-329">TsTimesheetCreate.createTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="05f16-329">TsTimesheetCreate.createTimesheetLine</span></span>|
|<span data-ttu-id="05f16-330">TSTimesheetEntry.initFields</span><span class="sxs-lookup"><span data-stu-id="05f16-330">TSTimesheetEntry.initFields</span></span>|
|<span data-ttu-id="05f16-331">TSTimesheetFavorites.createTimesheetLines</span><span class="sxs-lookup"><span data-stu-id="05f16-331">TSTimesheetFavorites.createTimesheetLines</span></span>|
|<span data-ttu-id="05f16-332">TSTimesheetLine.setCategoryIdFromActivity</span><span class="sxs-lookup"><span data-stu-id="05f16-332">TSTimesheetLine.setCategoryIdFromActivity</span></span>|
|<span data-ttu-id="05f16-333">VendInvoiceDocumentDP.insertVendInvoiceDocumentTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-333">VendInvoiceDocumentDP.insertVendInvoiceDocumentTmp</span></span>|
|<span data-ttu-id="05f16-334">WHSLoadLine.validateStatus</span><span class="sxs-lookup"><span data-stu-id="05f16-334">WHSLoadLine.validateStatus</span></span>|
|<span data-ttu-id="05f16-335">WHSLoadLineAllocationProcessor.allocateLoadLine</span><span class="sxs-lookup"><span data-stu-id="05f16-335">WHSLoadLineAllocationProcessor.allocateLoadLine</span></span>|
|<span data-ttu-id="05f16-336">WHSPostEngine.validateAnyDimAboveLocationMissing</span><span class="sxs-lookup"><span data-stu-id="05f16-336">WHSPostEngine.validateAnyDimAboveLocationMissing</span></span>|
|<span data-ttu-id="05f16-337">WhsWarehouseRelease.createShipmentsForAllSalesOrders</span><span class="sxs-lookup"><span data-stu-id="05f16-337">WhsWarehouseRelease.createShipmentsForAllSalesOrders</span></span>|
|<span data-ttu-id="05f16-338">WhsWarehouseRelease.createShipmentsForTransferOrders</span><span class="sxs-lookup"><span data-stu-id="05f16-338">WhsWarehouseRelease.createShipmentsForTransferOrders</span></span>|
|<span data-ttu-id="05f16-339">WhsWorkCreateLP.createTempTable</span><span class="sxs-lookup"><span data-stu-id="05f16-339">WhsWorkCreateLP.createTempTable</span></span>|
|<span data-ttu-id="05f16-340">WHSWorkCreateProdPut.createTempTable</span><span class="sxs-lookup"><span data-stu-id="05f16-340">WHSWorkCreateProdPut.createTempTable</span></span>|
|<span data-ttu-id="05f16-341">WHSWorkExecuteDisplay.buildNextDimensionCaptureControl</span><span class="sxs-lookup"><span data-stu-id="05f16-341">WHSWorkExecuteDisplay.buildNextDimensionCaptureControl</span></span>|
|<span data-ttu-id="05f16-342">WHSWorkLine::cancelLine</span><span class="sxs-lookup"><span data-stu-id="05f16-342">WHSWorkLine::cancelLine</span></span>|
|<span data-ttu-id="05f16-343">WmsArrivalCreateJournal::createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="05f16-343">WmsArrivalCreateJournal::createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="05f16-344">WmsArrivalOverviewGeneration::updateOverviewInformation</span><span class="sxs-lookup"><span data-stu-id="05f16-344">WmsArrivalOverviewGeneration::updateOverviewInformation</span></span>|
|<span data-ttu-id="05f16-345">WmsJournalCheckPostReception::initJournal</span><span class="sxs-lookup"><span data-stu-id="05f16-345">WmsJournalCheckPostReception::initJournal</span></span>|
|<span data-ttu-id="05f16-346">WMSOrderTrans::adjustQtyWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-346">WMSOrderTrans::adjustQtyWMSOrderTrans</span></span>|
|<span data-ttu-id="05f16-347">WMSOrderTrans::createNewWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-347">WMSOrderTrans::createNewWMSOrderTrans</span></span>|
|<span data-ttu-id="05f16-348">WMSOrderTrans::insertOrUpdate</span><span class="sxs-lookup"><span data-stu-id="05f16-348">WMSOrderTrans::insertOrUpdate</span></span>|
|<span data-ttu-id="05f16-349">WMSOrderTrans::updateWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="05f16-349">WMSOrderTrans::updateWMSOrderTrans</span></span>|
|<span data-ttu-id="05f16-350">WmsPickingList_OrderPickDP.insertIntoTempTable,setWMSPickingList_OrderPickTmpTemplate</span><span class="sxs-lookup"><span data-stu-id="05f16-350">WmsPickingList_OrderPickDP.insertIntoTempTable,setWMSPickingList_OrderPickTmpTemplate</span></span>|
|<span data-ttu-id="05f16-351">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span><span class="sxs-lookup"><span data-stu-id="05f16-351">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span></span>|
|<span data-ttu-id="05f16-352">WrkCtrlScheduler_Proj.loadJob</span><span class="sxs-lookup"><span data-stu-id="05f16-352">WrkCtrlScheduler_Proj.loadJob</span></span>|
|<span data-ttu-id="05f16-353">WrkCtrScheduler_Prod.saveOperation</span><span class="sxs-lookup"><span data-stu-id="05f16-353">WrkCtrScheduler_Prod.saveOperation</span></span>|
|<span data-ttu-id="05f16-354">WrkCtrScheduler_Prod.saveOrder</span><span class="sxs-lookup"><span data-stu-id="05f16-354">WrkCtrScheduler_Prod.saveOrder</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="05f16-355">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="05f16-355">Enumerations made extensible</span></span>

<span data-ttu-id="05f16-356">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="05f16-356">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="05f16-357">列挙型</span><span class="sxs-lookup"><span data-stu-id="05f16-357">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="05f16-358">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="05f16-358">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="05f16-359">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="05f16-359">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="05f16-360">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="05f16-360">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="05f16-361">ItemNumAlternative</span><span class="sxs-lookup"><span data-stu-id="05f16-361">ItemNumAlternative</span></span>|
|<span data-ttu-id="05f16-362">JmgRegistrationErrorMode</span><span class="sxs-lookup"><span data-stu-id="05f16-362">JmgRegistrationErrorMode</span></span>|
|<span data-ttu-id="05f16-363">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="05f16-363">MCRCustSearchType</span></span>|
|<span data-ttu-id="05f16-364">ModuleSalesPurch</span><span class="sxs-lookup"><span data-stu-id="05f16-364">ModuleSalesPurch</span></span>|
|<span data-ttu-id="05f16-365">ModuleSalesPurch</span><span class="sxs-lookup"><span data-stu-id="05f16-365">ModuleSalesPurch</span></span>|
|<span data-ttu-id="05f16-366">ProjStatusRule</span><span class="sxs-lookup"><span data-stu-id="05f16-366">ProjStatusRule</span></span>|
|<span data-ttu-id="05f16-367">PurchRFQUpdateType</span><span class="sxs-lookup"><span data-stu-id="05f16-367">PurchRFQUpdateType</span></span>|
|<span data-ttu-id="05f16-368">TAMVendRebateItemCode</span><span class="sxs-lookup"><span data-stu-id="05f16-368">TAMVendRebateItemCode</span></span>|
|<span data-ttu-id="05f16-369">TMSLoadBuildSupplyDemandType</span><span class="sxs-lookup"><span data-stu-id="05f16-369">TMSLoadBuildSupplyDemandType</span></span>|


## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="05f16-370">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="05f16-370">Additional extensibility enhancements</span></span>

<span data-ttu-id="05f16-371">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="05f16-371">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="05f16-372">EcoResProductSearchName の EDT の文字列のサイズを増加</span><span class="sxs-lookup"><span data-stu-id="05f16-372">Increase EDT string size for EcoResProductSearchName</span></span>
- <span data-ttu-id="05f16-373">AssetLedgerAccounts の CacheLookup プロパティを NotInTTS に変更します。</span><span class="sxs-lookup"><span data-stu-id="05f16-373">Change CacheLookup property to NotInTTS for AssetLedgerAccounts</span></span>
- <span data-ttu-id="05f16-374">TaxOnItem、TaxJurisdiction、TaxGroupData、TaxData、およびAssetLedgerAcounts で CacheLookup プロパティを検出に変更します。</span><span class="sxs-lookup"><span data-stu-id="05f16-374">Change CacheLookup property to Found on TaxOnItem, TaxJurisdiction, TaxGroupData, and TaxData, and AssetLedgerAcounts</span></span>
