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
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-08-31
ms.dyn365.ops.version: App 8.0.3
ms.openlocfilehash: c272aede83056d61c28e514332aabde7d501a94f
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833452"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-803"></a><span data-ttu-id="f68d7-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="f68d7-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.3</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f68d7-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="f68d7-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.3.</span></span> <span data-ttu-id="f68d7-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f68d7-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="f68d7-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="f68d7-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="f68d7-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f68d7-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="f68d7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f68d7-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="f68d7-109">AccountingSourceExplorerProcessor.filterEntries</span><span class="sxs-lookup"><span data-stu-id="f68d7-109">AccountingSourceExplorerProcessor.filterEntries</span></span>|
|<span data-ttu-id="f68d7-110">AgreementClassification.init</span><span class="sxs-lookup"><span data-stu-id="f68d7-110">AgreementClassification.init</span></span>|
|<span data-ttu-id="f68d7-111">AgreementConfirm.createLineVolumeCommittmentHistory</span><span class="sxs-lookup"><span data-stu-id="f68d7-111">AgreementConfirm.createLineVolumeCommittmentHistory</span></span>|
|<span data-ttu-id="f68d7-112">AgreementConfirm.newAgreementConfirm</span><span class="sxs-lookup"><span data-stu-id="f68d7-112">AgreementConfirm.newAgreementConfirm</span></span>|
|<span data-ttu-id="f68d7-113">Agreementline.findLineForAutoMatch</span><span class="sxs-lookup"><span data-stu-id="f68d7-113">Agreementline.findLineForAutoMatch</span></span>|
|<span data-ttu-id="f68d7-114">Agreementline.getAgreementLinesForOrderLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-114">Agreementline.getAgreementLinesForOrderLine</span></span>|
|<span data-ttu-id="f68d7-115">AgreementLine.getAgreementLinesForPurchReqLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-115">AgreementLine.getAgreementLinesForPurchReqLine</span></span>|
|<span data-ttu-id="f68d7-116">Agreementline.getAgreementLinesList</span><span class="sxs-lookup"><span data-stu-id="f68d7-116">Agreementline.getAgreementLinesList</span></span>|
|<span data-ttu-id="f68d7-117">Bank_FR.checkControlText</span><span class="sxs-lookup"><span data-stu-id="f68d7-117">Bank_FR.checkControlText</span></span>|
|<span data-ttu-id="f68d7-118">Bank_IT.checkCIN</span><span class="sxs-lookup"><span data-stu-id="f68d7-118">Bank_IT.checkCIN</span></span>|
|<span data-ttu-id="f68d7-119">Bank_IT.checkRegistrationNum</span><span class="sxs-lookup"><span data-stu-id="f68d7-119">Bank_IT.checkRegistrationNum</span></span>|
|<span data-ttu-id="f68d7-120">BankAccountTrans.insert</span><span class="sxs-lookup"><span data-stu-id="f68d7-120">BankAccountTrans.insert</span></span>|
|<span data-ttu-id="f68d7-121">BankAccountTrans.update</span><span class="sxs-lookup"><span data-stu-id="f68d7-121">BankAccountTrans.update</span></span>|
|<span data-ttu-id="f68d7-122">BankChequeCopy.fillTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="f68d7-122">BankChequeCopy.fillTmpChequePrintout</span></span>|
|<span data-ttu-id="f68d7-123">BankChequePrint.printDocument</span><span class="sxs-lookup"><span data-stu-id="f68d7-123">BankChequePrint.printDocument</span></span>|
|<span data-ttu-id="f68d7-124">BankPaymAdviceReportGeneratorVend</span><span class="sxs-lookup"><span data-stu-id="f68d7-124">BankPaymAdviceReportGeneratorVend</span></span>|
|<span data-ttu-id="f68d7-125">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span><span class="sxs-lookup"><span data-stu-id="f68d7-125">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span></span>|
|<span data-ttu-id="f68d7-126">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span><span class="sxs-lookup"><span data-stu-id="f68d7-126">BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc</span></span>|
|<span data-ttu-id="f68d7-127">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span><span class="sxs-lookup"><span data-stu-id="f68d7-127">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span></span>|
|<span data-ttu-id="f68d7-128">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span><span class="sxs-lookup"><span data-stu-id="f68d7-128">BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList</span></span>|
|<span data-ttu-id="f68d7-129">BankVoucher.createBankAccountTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-129">BankVoucher.createBankAccountTrans</span></span>|
|<span data-ttu-id="f68d7-130">BankVoucher.createBankAccountTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-130">BankVoucher.createBankAccountTrans</span></span>|
|<span data-ttu-id="f68d7-131">BomCopyToProd.copyTo</span><span class="sxs-lookup"><span data-stu-id="f68d7-131">BomCopyToProd.copyTo</span></span>|
|<span data-ttu-id="f68d7-132">BudgetPlanLineFieldActiveViewMapping.getBudgetPlanLineFieldName</span><span class="sxs-lookup"><span data-stu-id="f68d7-132">BudgetPlanLineFieldActiveViewMapping.getBudgetPlanLineFieldName</span></span>|
|<span data-ttu-id="f68d7-133">BudgetTransaction.openLinesInExcel</span><span class="sxs-lookup"><span data-stu-id="f68d7-133">BudgetTransaction.openLinesInExcel</span></span>|
|<span data-ttu-id="f68d7-134">ChequeController.init</span><span class="sxs-lookup"><span data-stu-id="f68d7-134">ChequeController.init</span></span>|
|<span data-ttu-id="f68d7-135">CustAccountStatementExt.main</span><span class="sxs-lookup"><span data-stu-id="f68d7-135">CustAccountStatementExt.main</span></span>|
|<span data-ttu-id="f68d7-136">CustAccountStatementExtController.includeOnStatement</span><span class="sxs-lookup"><span data-stu-id="f68d7-136">CustAccountStatementExtController.includeOnStatement</span></span>|
|<span data-ttu-id="f68d7-137">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-137">CustAccountStatementExtController.insertCustAccountStatementExtTmp</span></span>|
|<span data-ttu-id="f68d7-138">CustAccountStatementExtController.setCommonData</span><span class="sxs-lookup"><span data-stu-id="f68d7-138">CustAccountStatementExtController.setCommonData</span></span>|
|<span data-ttu-id="f68d7-139">CustAccountStatementExtController.tmpCustVendTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-139">CustAccountStatementExtController.tmpCustVendTrans</span></span>|
|<span data-ttu-id="f68d7-140">CustAccountStatementExtUIBuilder.build</span><span class="sxs-lookup"><span data-stu-id="f68d7-140">CustAccountStatementExtUIBuilder.build</span></span>|
|<span data-ttu-id="f68d7-141">CustAuditorDP.setCustAuditorTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-141">CustAuditorDP.setCustAuditorTmp</span></span>|
|<span data-ttu-id="f68d7-142">CustCollectionJourDP.insertCustCollectionJourDP</span><span class="sxs-lookup"><span data-stu-id="f68d7-142">CustCollectionJourDP.insertCustCollectionJourDP</span></span>|
|<span data-ttu-id="f68d7-143">CustCreditLimit.Balance</span><span class="sxs-lookup"><span data-stu-id="f68d7-143">CustCreditLimit.Balance</span></span>|
|<span data-ttu-id="f68d7-144">CustInterestNoteDp.processReport</span><span class="sxs-lookup"><span data-stu-id="f68d7-144">CustInterestNoteDp.processReport</span></span>|
|<span data-ttu-id="f68d7-145">CustInvoiceJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="f68d7-145">CustInvoiceJour.printJournal</span></span>|
|<span data-ttu-id="f68d7-146">CustInvoiceTable.checkCreditLimit</span><span class="sxs-lookup"><span data-stu-id="f68d7-146">CustInvoiceTable.checkCreditLimit</span></span>|
|<span data-ttu-id="f68d7-147">CustPackingSlipJour.interCompanyUpdate</span><span class="sxs-lookup"><span data-stu-id="f68d7-147">CustPackingSlipJour.interCompanyUpdate</span></span>|
|<span data-ttu-id="f68d7-148">CustPaymEntry.updateConditionalControls</span><span class="sxs-lookup"><span data-stu-id="f68d7-148">CustPaymEntry.updateConditionalControls</span></span>|
|<span data-ttu-id="f68d7-149">custPostInvoicejob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="f68d7-149">custPostInvoicejob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="f68d7-150">CustTrans.reverseTransact</span><span class="sxs-lookup"><span data-stu-id="f68d7-150">CustTrans.reverseTransact</span></span>|
|<span data-ttu-id="f68d7-151">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-151">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="f68d7-152">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-152">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="f68d7-153">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="f68d7-153">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="f68d7-154">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="f68d7-154">CustVendCheque.output</span></span>|
|<span data-ttu-id="f68d7-155">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="f68d7-155">CustVendCheque.output</span></span>|
|<span data-ttu-id="f68d7-156">CustVendChequeSlipTextCalculator.getChequeDocLength</span><span class="sxs-lookup"><span data-stu-id="f68d7-156">CustVendChequeSlipTextCalculator.getChequeDocLength</span></span>|
|<span data-ttu-id="f68d7-157">CustVendSumForPaym.validateSEPATransaction</span><span class="sxs-lookup"><span data-stu-id="f68d7-157">CustVendSumForPaym.validateSEPATransaction</span></span>|
|<span data-ttu-id="f68d7-158">CustVendSumUpJournal.createTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-158">CustVendSumUpJournal.createTrans</span></span>|
|<span data-ttu-id="f68d7-159">CustVendVoucher.post</span><span class="sxs-lookup"><span data-stu-id="f68d7-159">CustVendVoucher.post</span></span>|
|<span data-ttu-id="f68d7-160">DimDerDistRuleProjectTimesheetsExt.populateDimAllocListIntercompany</span><span class="sxs-lookup"><span data-stu-id="f68d7-160">DimDerDistRuleProjectTimesheetsExt.populateDimAllocListIntercompany</span></span>|
|<span data-ttu-id="f68d7-161">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span><span class="sxs-lookup"><span data-stu-id="f68d7-161">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span></span>|
|<span data-ttu-id="f68d7-162">DirPartyVerification.selectionChanged</span><span class="sxs-lookup"><span data-stu-id="f68d7-162">DirPartyVerification.selectionChanged</span></span>|
|<span data-ttu-id="f68d7-163">EcoResCategoryTreeDatasource.initializeAvailableCategoriesMap</span><span class="sxs-lookup"><span data-stu-id="f68d7-163">EcoResCategoryTreeDatasource.initializeAvailableCategoriesMap</span></span>|
|<span data-ttu-id="f68d7-164">EcoResProductCreate.writeMoreFields</span><span class="sxs-lookup"><span data-stu-id="f68d7-164">EcoResProductCreate.writeMoreFields</span></span>|
|<span data-ttu-id="f68d7-165">EcoResProductDetailsExtended.initInventDimensionsMetadataEntries</span><span class="sxs-lookup"><span data-stu-id="f68d7-165">EcoResProductDetailsExtended.initInventDimensionsMetadataEntries</span></span>|
|<span data-ttu-id="f68d7-166">ElectronicPaymentRemitExport_BR.construct</span><span class="sxs-lookup"><span data-stu-id="f68d7-166">ElectronicPaymentRemitExport_BR.construct</span></span>|
|<span data-ttu-id="f68d7-167">ForecastPuch</span><span class="sxs-lookup"><span data-stu-id="f68d7-167">ForecastPuch</span></span>|
|<span data-ttu-id="f68d7-168">ForecastSales.accountConsumption</span><span class="sxs-lookup"><span data-stu-id="f68d7-168">ForecastSales.accountConsumption</span></span>|
|<span data-ttu-id="f68d7-169">ForecastSales.accountDisc</span><span class="sxs-lookup"><span data-stu-id="f68d7-169">ForecastSales.accountDisc</span></span>|
|<span data-ttu-id="f68d7-170">ForecastSales.accountIssue</span><span class="sxs-lookup"><span data-stu-id="f68d7-170">ForecastSales.accountIssue</span></span>|
|<span data-ttu-id="f68d7-171">ForecastSales.accountSales</span><span class="sxs-lookup"><span data-stu-id="f68d7-171">ForecastSales.accountSales</span></span>|
|<span data-ttu-id="f68d7-172">InventPosting.accountItemLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="f68d7-172">InventPosting.accountItemLedgerDimension</span></span>|
|<span data-ttu-id="f68d7-173">InventSupply.init</span><span class="sxs-lookup"><span data-stu-id="f68d7-173">InventSupply.init</span></span>|
|<span data-ttu-id="f68d7-174">InventTrans.insertReturnTransOrigin</span><span class="sxs-lookup"><span data-stu-id="f68d7-174">InventTrans.insertReturnTransOrigin</span></span>|
|<span data-ttu-id="f68d7-175">InventTransferParmLine - いくつかの方法</span><span class="sxs-lookup"><span data-stu-id="f68d7-175">InventTransferParmLine - several methods</span></span>|
|<span data-ttu-id="f68d7-176">InventTransferUpd::updateLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-176">InventTransferUpd::updateLines</span></span>|
|<span data-ttu-id="f68d7-177">InventTransFormHelper.formQueryAddDynalink</span><span class="sxs-lookup"><span data-stu-id="f68d7-177">InventTransFormHelper.formQueryAddDynalink</span></span>|
|<span data-ttu-id="f68d7-178">InventTransWMS_Pick::updateInventServer</span><span class="sxs-lookup"><span data-stu-id="f68d7-178">InventTransWMS_Pick::updateInventServer</span></span>|
|<span data-ttu-id="f68d7-179">InventUpd_Physical::updatePhysicalReceiptTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-179">InventUpd_Physical::updatePhysicalReceiptTrans</span></span>|
|<span data-ttu-id="f68d7-180">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-180">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="f68d7-181">InventUpdate::createInventTransOriginAndReferences</span><span class="sxs-lookup"><span data-stu-id="f68d7-181">InventUpdate::createInventTransOriginAndReferences</span></span>|
|<span data-ttu-id="f68d7-182">InventValueReportPopulateItem::findReportLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-182">InventValueReportPopulateItem::findReportLine</span></span>|
|<span data-ttu-id="f68d7-183">JmgRegistration.JmgJobTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-183">JmgRegistration.JmgJobTable</span></span>|
|<span data-ttu-id="f68d7-184">JournalizingDefinitionManager.newJournalizingDefinitionManagerPurch</span><span class="sxs-lookup"><span data-stu-id="f68d7-184">JournalizingDefinitionManager.newJournalizingDefinitionManagerPurch</span></span>|
|<span data-ttu-id="f68d7-185">JournalStatic.initializeDataModel</span><span class="sxs-lookup"><span data-stu-id="f68d7-185">JournalStatic.initializeDataModel</span></span>|
|<span data-ttu-id="f68d7-186">LedgerFinancialJournalReportDPBE.calcDebCredTotals</span><span class="sxs-lookup"><span data-stu-id="f68d7-186">LedgerFinancialJournalReportDPBE.calcDebCredTotals</span></span>|
|<span data-ttu-id="f68d7-187">LedgerFinancialJournalReportDPBE.processReport</span><span class="sxs-lookup"><span data-stu-id="f68d7-187">LedgerFinancialJournalReportDPBE.processReport</span></span>|
|<span data-ttu-id="f68d7-188">LedgerJournalDP.insertJournalTransForLedgerJournalTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-188">LedgerJournalDP.insertJournalTransForLedgerJournalTable</span></span>|
|<span data-ttu-id="f68d7-189">LedgerJournalDP.insertLedgerJournalTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-189">LedgerJournalDP.insertLedgerJournalTmp</span></span>|
|<span data-ttu-id="f68d7-190">LedgerJournalEngine.newJournalActive</span><span class="sxs-lookup"><span data-stu-id="f68d7-190">LedgerJournalEngine.newJournalActive</span></span>|
|<span data-ttu-id="f68d7-191">LedgerJournalTrans checkAllowPosting</span><span class="sxs-lookup"><span data-stu-id="f68d7-191">LedgerJournalTrans checkAllowPosting</span></span>|
|<span data-ttu-id="f68d7-192">LedgerJournalTransUpdateBank.setBankVoucherSource</span><span class="sxs-lookup"><span data-stu-id="f68d7-192">LedgerJournalTransUpdateBank.setBankVoucherSource</span></span>|
|<span data-ttu-id="f68d7-193">LedgerJournalTransUpdateBank.updateNow</span><span class="sxs-lookup"><span data-stu-id="f68d7-193">LedgerJournalTransUpdateBank.updateNow</span></span>|
|<span data-ttu-id="f68d7-194">LedgerJournalTransUpdateBankLC.addBankVoucher</span><span class="sxs-lookup"><span data-stu-id="f68d7-194">LedgerJournalTransUpdateBankLC.addBankVoucher</span></span>|
|<span data-ttu-id="f68d7-195">LedgerPostingGeneralJournalController.transferLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-195">LedgerPostingGeneralJournalController.transferLines</span></span>|
|<span data-ttu-id="f68d7-196">LedgerPurchaseJournalReportDPBE.insertIntoTempTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-196">LedgerPurchaseJournalReportDPBE.insertIntoTempTable</span></span>|
|<span data-ttu-id="f68d7-197">LedgerSalesJournalReportDPBE.processReport</span><span class="sxs-lookup"><span data-stu-id="f68d7-197">LedgerSalesJournalReportDPBE.processReport</span></span>|
|<span data-ttu-id="f68d7-198">LedgerTransFurtherPosting.createLedgerJournalTransFromGenJour</span><span class="sxs-lookup"><span data-stu-id="f68d7-198">LedgerTransFurtherPosting.createLedgerJournalTransFromGenJour</span></span>|
|<span data-ttu-id="f68d7-199">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span><span class="sxs-lookup"><span data-stu-id="f68d7-199">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span></span>|
|<span data-ttu-id="f68d7-200">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span><span class="sxs-lookup"><span data-stu-id="f68d7-200">LedgerTransVoucher.getSubledgerVoucherLinkDataSource</span></span>|
|<span data-ttu-id="f68d7-201">LedgerTransVoucher.getVoucherDateRange</span><span class="sxs-lookup"><span data-stu-id="f68d7-201">LedgerTransVoucher.getVoucherDateRange</span></span>|
|<span data-ttu-id="f68d7-202">LedgerVoucherObject.updateLedgerPostingJournal</span><span class="sxs-lookup"><span data-stu-id="f68d7-202">LedgerVoucherObject.updateLedgerPostingJournal</span></span>|
|<span data-ttu-id="f68d7-203">LedgerVoucherTransObject.checkRounding</span><span class="sxs-lookup"><span data-stu-id="f68d7-203">LedgerVoucherTransObject.checkRounding</span></span>|
|<span data-ttu-id="f68d7-204">Markup.insertMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-204">Markup.insertMarkupTrans</span></span>|
|<span data-ttu-id="f68d7-205">MarkupTrans.MarkupTable.MarkupCode.Lookup</span><span class="sxs-lookup"><span data-stu-id="f68d7-205">MarkupTrans.MarkupTable.MarkupCode.Lookup</span></span>|
|<span data-ttu-id="f68d7-206">PaymSchedCalc::init\*</span><span class="sxs-lookup"><span data-stu-id="f68d7-206">PaymSchedCalc::init\*</span></span>|
|<span data-ttu-id="f68d7-207">PaymSchedCalc_Line::createTransaction</span><span class="sxs-lookup"><span data-stu-id="f68d7-207">PaymSchedCalc_Line::createTransaction</span></span>|
|<span data-ttu-id="f68d7-208">PdsApprovedVendorListCheck.newBasedOnTableType</span><span class="sxs-lookup"><span data-stu-id="f68d7-208">PdsApprovedVendorListCheck.newBasedOnTableType</span></span>|
|<span data-ttu-id="f68d7-209">PmfFormulaCoBy.run</span><span class="sxs-lookup"><span data-stu-id="f68d7-209">PmfFormulaCoBy.run</span></span>|
|<span data-ttu-id="f68d7-210">PmfFormulaCoBy.ValidateField</span><span class="sxs-lookup"><span data-stu-id="f68d7-210">PmfFormulaCoBy.ValidateField</span></span>|
|<span data-ttu-id="f68d7-211">PmfProdCoBy.ValidateField</span><span class="sxs-lookup"><span data-stu-id="f68d7-211">PmfProdCoBy.ValidateField</span></span>|
|<span data-ttu-id="f68d7-212">PmfProdCoBy.ValidateWrite</span><span class="sxs-lookup"><span data-stu-id="f68d7-212">PmfProdCoBy.ValidateWrite</span></span>|
|<span data-ttu-id="f68d7-213">PriceDiscAdmSearch</span><span class="sxs-lookup"><span data-stu-id="f68d7-213">PriceDiscAdmSearch</span></span>|
|<span data-ttu-id="f68d7-214">PriceDiscPolicyDialog.runPolicyDialog</span><span class="sxs-lookup"><span data-stu-id="f68d7-214">PriceDiscPolicyDialog.runPolicyDialog</span></span>|
|<span data-ttu-id="f68d7-215">ProdBOM.checkIsItemsReleased</span><span class="sxs-lookup"><span data-stu-id="f68d7-215">ProdBOM.checkIsItemsReleased</span></span>|
|<span data-ttu-id="f68d7-216">ProdBOM::update</span><span class="sxs-lookup"><span data-stu-id="f68d7-216">ProdBOM::update</span></span>|
|<span data-ttu-id="f68d7-217">ProdJournalProd.Insert</span><span class="sxs-lookup"><span data-stu-id="f68d7-217">ProdJournalProd.Insert</span></span>|
|<span data-ttu-id="f68d7-218">ProdPurch.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-218">ProdPurch.createPurchTable</span></span>|
|<span data-ttu-id="f68d7-219">ProdUpdHistoricalCost_Process.checkValidCoBy</span><span class="sxs-lookup"><span data-stu-id="f68d7-219">ProdUpdHistoricalCost_Process.checkValidCoBy</span></span>|
|<span data-ttu-id="f68d7-220">ProdUpdReportFinished::updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="f68d7-220">ProdUpdReportFinished::updateBOMConsumption</span></span>|
|<span data-ttu-id="f68d7-221">ProdUpdStartUp,getListOfBOMJournals</span><span class="sxs-lookup"><span data-stu-id="f68d7-221">ProdUpdStartUp,getListOfBOMJournals</span></span>|
|<span data-ttu-id="f68d7-222">ProdUpdStatusDecrease_StartUp.reverseBOMStartUp</span><span class="sxs-lookup"><span data-stu-id="f68d7-222">ProdUpdStatusDecrease_StartUp.reverseBOMStartUp</span></span>|
|<span data-ttu-id="f68d7-223">ProjBudgetParticipantProvider.resolveByProject</span><span class="sxs-lookup"><span data-stu-id="f68d7-223">ProjBudgetParticipantProvider.resolveByProject</span></span>|
|<span data-ttu-id="f68d7-224">ProjBudgetParticipantProvider.resolveByProjectHierarchy</span><span class="sxs-lookup"><span data-stu-id="f68d7-224">ProjBudgetParticipantProvider.resolveByProjectHierarchy</span></span>|
|<span data-ttu-id="f68d7-225">ProjBudgetParticipantProvider.resolveByRootProject</span><span class="sxs-lookup"><span data-stu-id="f68d7-225">ProjBudgetParticipantProvider.resolveByRootProject</span></span>|
|<span data-ttu-id="f68d7-226">ProjCaseActivitiesHandler.smmActivities_onValidatedDelete</span><span class="sxs-lookup"><span data-stu-id="f68d7-226">ProjCaseActivitiesHandler.smmActivities_onValidatedDelete</span></span>|
|<span data-ttu-id="f68d7-227">ProjControlPeriod.forecast</span><span class="sxs-lookup"><span data-stu-id="f68d7-227">ProjControlPeriod.forecast</span></span>|
|<span data-ttu-id="f68d7-228">ProjControlPeriod.forecast</span><span class="sxs-lookup"><span data-stu-id="f68d7-228">ProjControlPeriod.forecast</span></span>|
|<span data-ttu-id="f68d7-229">ProjControlPeriodCostGroup.totalBudgetMinusActual</span><span class="sxs-lookup"><span data-stu-id="f68d7-229">ProjControlPeriodCostGroup.totalBudgetMinusActual</span></span>|
|<span data-ttu-id="f68d7-230">ProjControlPeriodCostGroup.totalBudgetMinusActual</span><span class="sxs-lookup"><span data-stu-id="f68d7-230">ProjControlPeriodCostGroup.totalBudgetMinusActual</span></span>|
|<span data-ttu-id="f68d7-231">ProjectPosting.costLedgerDimension.</span><span class="sxs-lookup"><span data-stu-id="f68d7-231">ProjectPosting.costLedgerDimension.</span></span>|
|<span data-ttu-id="f68d7-232">ProjectPosting.getProjectLedgerDimension.</span><span class="sxs-lookup"><span data-stu-id="f68d7-232">ProjectPosting.getProjectLedgerDimension.</span></span>|
|<span data-ttu-id="f68d7-233">ProjForecastEmpl.initValue</span><span class="sxs-lookup"><span data-stu-id="f68d7-233">ProjForecastEmpl.initValue</span></span>|
|<span data-ttu-id="f68d7-234">ProjForecastReduceHour.constructQuery</span><span class="sxs-lookup"><span data-stu-id="f68d7-234">ProjForecastReduceHour.constructQuery</span></span>|
|<span data-ttu-id="f68d7-235">ProjFundingSource.setInvoiceLocation</span><span class="sxs-lookup"><span data-stu-id="f68d7-235">ProjFundingSource.setInvoiceLocation</span></span>|
|<span data-ttu-id="f68d7-236">ProjGroup.initFromProjType</span><span class="sxs-lookup"><span data-stu-id="f68d7-236">ProjGroup.initFromProjType</span></span>|
|<span data-ttu-id="f68d7-237">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-237">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span></span>|
|<span data-ttu-id="f68d7-238">ProjIntercompanyTransactionSelection.runQuery</span><span class="sxs-lookup"><span data-stu-id="f68d7-238">ProjIntercompanyTransactionSelection.runQuery</span></span>|
|<span data-ttu-id="f68d7-239">ProjIntercompanyTransQuery.buildExpenseQuery</span><span class="sxs-lookup"><span data-stu-id="f68d7-239">ProjIntercompanyTransQuery.buildExpenseQuery</span></span>|
|<span data-ttu-id="f68d7-240">ProjIntercompanyTransQuery.buildHoursQuery</span><span class="sxs-lookup"><span data-stu-id="f68d7-240">ProjIntercompanyTransQuery.buildHoursQuery</span></span>|
|<span data-ttu-id="f68d7-241">ProjIntercompanyTransQuery.buildVendorInvoiceLinesQuery</span><span class="sxs-lookup"><span data-stu-id="f68d7-241">ProjIntercompanyTransQuery.buildVendorInvoiceLinesQuery</span></span>|
|<span data-ttu-id="f68d7-242">ProjInventJournalTransMapForm.checkActivity</span><span class="sxs-lookup"><span data-stu-id="f68d7-242">ProjInventJournalTransMapForm.checkActivity</span></span>||
|<span data-ttu-id="f68d7-243">projInvoiceChooose.setProposalJour</span><span class="sxs-lookup"><span data-stu-id="f68d7-243">projInvoiceChooose.setProposalJour</span></span>|
|<span data-ttu-id="f68d7-244">ProjInvoiceChoose.doRevenue</span><span class="sxs-lookup"><span data-stu-id="f68d7-244">ProjInvoiceChoose.doRevenue</span></span>|
|<span data-ttu-id="f68d7-245">ProjInvoiceChoose.updateInvoiceTotal</span><span class="sxs-lookup"><span data-stu-id="f68d7-245">ProjInvoiceChoose.updateInvoiceTotal</span></span>|
|<span data-ttu-id="f68d7-246">ProjInvoiceProposalCreateLines.isRevenueTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-246">ProjInvoiceProposalCreateLines.isRevenueTrans</span></span>|
|<span data-ttu-id="f68d7-247">ProjInvoiceProposalCreateLinesBase.createProposalTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-247">ProjInvoiceProposalCreateLinesBase.createProposalTrans</span></span>|
|<span data-ttu-id="f68d7-248">ProjInvoiceProposalCreateLinesBase.doOnAccount</span><span class="sxs-lookup"><span data-stu-id="f68d7-248">ProjInvoiceProposalCreateLinesBase.doOnAccount</span></span>|
|<span data-ttu-id="f68d7-249">ProjInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-249">ProjInvoiceTable</span></span>|
|<span data-ttu-id="f68d7-250">ProjLedger.classdeclaration</span><span class="sxs-lookup"><span data-stu-id="f68d7-250">ProjLedger.classdeclaration</span></span>|
|<span data-ttu-id="f68d7-251">ProjPostItemJournal.projTransCreate</span><span class="sxs-lookup"><span data-stu-id="f68d7-251">ProjPostItemJournal.projTransCreate</span></span>|
|<span data-ttu-id="f68d7-252">ProjProjectsListPage.CtrlStages</span><span class="sxs-lookup"><span data-stu-id="f68d7-252">ProjProjectsListPage.CtrlStages</span></span>|
|<span data-ttu-id="f68d7-253">ProjProjectsListPageInteraction.enableButton</span><span class="sxs-lookup"><span data-stu-id="f68d7-253">ProjProjectsListPageInteraction.enableButton</span></span>|
|<span data-ttu-id="f68d7-254">ProjProjectsListPageInteraction.showButton</span><span class="sxs-lookup"><span data-stu-id="f68d7-254">ProjProjectsListPageInteraction.showButton</span></span>|
|<span data-ttu-id="f68d7-255">ProjStatusUpd.main</span><span class="sxs-lookup"><span data-stu-id="f68d7-255">ProjStatusUpd.main</span></span>|
|<span data-ttu-id="f68d7-256">ProjStatusUpd.new</span><span class="sxs-lookup"><span data-stu-id="f68d7-256">ProjStatusUpd.new</span></span>|
|<span data-ttu-id="f68d7-257">ProjTable - ProjTable datasource.write</span><span class="sxs-lookup"><span data-stu-id="f68d7-257">ProjTable - ProjTable datasource.write</span></span>|
|<span data-ttu-id="f68d7-258">ProjTable.clicked</span><span class="sxs-lookup"><span data-stu-id="f68d7-258">ProjTable.clicked</span></span>|
|<span data-ttu-id="f68d7-259">ProjTable.editSubProj</span><span class="sxs-lookup"><span data-stu-id="f68d7-259">ProjTable.editSubProj</span></span>|
|<span data-ttu-id="f68d7-260">ProjTable.editSubProj</span><span class="sxs-lookup"><span data-stu-id="f68d7-260">ProjTable.editSubProj</span></span>|
|<span data-ttu-id="f68d7-261">ProjTableCreate.close</span><span class="sxs-lookup"><span data-stu-id="f68d7-261">ProjTableCreate.close</span></span>|
|<span data-ttu-id="f68d7-262">ProjTableCreate.run</span><span class="sxs-lookup"><span data-stu-id="f68d7-262">ProjTableCreate.run</span></span>|
|<span data-ttu-id="f68d7-263">ProjTableCreate.write</span><span class="sxs-lookup"><span data-stu-id="f68d7-263">ProjTableCreate.write</span></span>|
|<span data-ttu-id="f68d7-264">ProjTableCreate.write</span><span class="sxs-lookup"><span data-stu-id="f68d7-264">ProjTableCreate.write</span></span>|
|<span data-ttu-id="f68d7-265">ProjTableLookup.ProjProjectLookup.init</span><span class="sxs-lookup"><span data-stu-id="f68d7-265">ProjTableLookup.ProjProjectLookup.init</span></span>|
|<span data-ttu-id="f68d7-266">PSAProjInvoiceDP.insertPSAProjInvoiceHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-266">PSAProjInvoiceDP.insertPSAProjInvoiceHeaderTmp</span></span>|
|<span data-ttu-id="f68d7-267">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span><span class="sxs-lookup"><span data-stu-id="f68d7-267">PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax</span></span>|
|<span data-ttu-id="f68d7-268">PsaProjProposalSelection</span><span class="sxs-lookup"><span data-stu-id="f68d7-268">PsaProjProposalSelection</span></span>|
|<span data-ttu-id="f68d7-269">PurchAgreementAutoCreate::construct</span><span class="sxs-lookup"><span data-stu-id="f68d7-269">PurchAgreementAutoCreate::construct</span></span>|
|<span data-ttu-id="f68d7-270">PurchAutoCreate.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-270">PurchAutoCreate.setPurchTable</span></span>|
|<span data-ttu-id="f68d7-271">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-271">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="f68d7-272">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-272">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="f68d7-273">PurchAutoCreate_ReleaseFromAgreement.updateFinDimFromAgreemHeader</span><span class="sxs-lookup"><span data-stu-id="f68d7-273">PurchAutoCreate_ReleaseFromAgreement.updateFinDimFromAgreemHeader</span></span>|
|<span data-ttu-id="f68d7-274">PurchCreateFromSalesOrder.shouldCreatePurchOrder</span><span class="sxs-lookup"><span data-stu-id="f68d7-274">PurchCreateFromSalesOrder.shouldCreatePurchOrder</span></span>|
|<span data-ttu-id="f68d7-275">PurchFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="f68d7-275">PurchFormLetter::main</span></span>|
|<span data-ttu-id="f68d7-276">PurchFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="f68d7-276">PurchFormLetter::main</span></span>|
|<span data-ttu-id="f68d7-277">PurchFormletterParmDataPackingSlip::reSelectLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-277">PurchFormletterParmDataPackingSlip::reSelectLines</span></span>|
|<span data-ttu-id="f68d7-278">PurchFormletterParmDataPackingSlip::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-278">PurchFormletterParmDataPackingSlip::selectChooseLines</span></span>|
|<span data-ttu-id="f68d7-279">PurchFormletterParmDataPurchOrder::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-279">PurchFormletterParmDataPurchOrder::selectChooseLines</span></span>|
|<span data-ttu-id="f68d7-280">PurchInvoiceJournalPost.checkBeforePostingLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-280">PurchInvoiceJournalPost.checkBeforePostingLine</span></span> |
|<span data-ttu-id="f68d7-281">PurchInvoiceJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-281">PurchInvoiceJournalPost.updateSourceLine</span></span> |
|<span data-ttu-id="f68d7-282">Purchline.createline</span><span class="sxs-lookup"><span data-stu-id="f68d7-282">Purchline.createline</span></span>|
|<span data-ttu-id="f68d7-283">PurchOrderLineBudgetControlPolicy.canCheckBudget</span><span class="sxs-lookup"><span data-stu-id="f68d7-283">PurchOrderLineBudgetControlPolicy.canCheckBudget</span></span>|
|<span data-ttu-id="f68d7-284">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-284">PurchReceiptsListDP.setPurchReceiptsListDetailsTmp</span></span>|
|<span data-ttu-id="f68d7-285">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-285">PurchReceiptsListDP.setPurchReceiptsListHeaderTmp</span></span>|
|<span data-ttu-id="f68d7-286">PurchRFQAcceptJournalPost.updatePurchReq</span><span class="sxs-lookup"><span data-stu-id="f68d7-286">PurchRFQAcceptJournalPost.updatePurchReq</span></span>|
|<span data-ttu-id="f68d7-287">ReqCalc.covCalcDim</span><span class="sxs-lookup"><span data-stu-id="f68d7-287">ReqCalc.covCalcDim</span></span>|
|<span data-ttu-id="f68d7-288">ReqTrans.createTransferDemand</span><span class="sxs-lookup"><span data-stu-id="f68d7-288">ReqTrans.createTransferDemand</span></span>|
|<span data-ttu-id="f68d7-289">ReqTransPoMarkFirm.createProdRoute</span><span class="sxs-lookup"><span data-stu-id="f68d7-289">ReqTransPoMarkFirm.createProdRoute</span></span>|
|<span data-ttu-id="f68d7-290">RetailPeriodicDiscount.ClassDeclaration</span><span class="sxs-lookup"><span data-stu-id="f68d7-290">RetailPeriodicDiscount.ClassDeclaration</span></span>|
|<span data-ttu-id="f68d7-291">RetailTransactionServiceOrders.cancelCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="f68d7-291">RetailTransactionServiceOrders.cancelCustomerOrder</span></span>|
|<span data-ttu-id="f68d7-292">Return.ReturnDispositionCodeId::validate</span><span class="sxs-lookup"><span data-stu-id="f68d7-292">Return.ReturnDispositionCodeId::validate</span></span>|
|<span data-ttu-id="f68d7-293">SalesAutoCreate::construct</span><span class="sxs-lookup"><span data-stu-id="f68d7-293">SalesAutoCreate::construct</span></span>|
|<span data-ttu-id="f68d7-294">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="f68d7-294">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="f68d7-295">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="f68d7-295">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="f68d7-296">SalesFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="f68d7-296">SalesFormLetter::main</span></span>|
|<span data-ttu-id="f68d7-297">SalesFormletterParmDataConfirm::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-297">SalesFormletterParmDataConfirm::selectChooseLines</span></span>|
|<span data-ttu-id="f68d7-298">SalesFormletterParmDataInvoice::mayJournalTransBePosted</span><span class="sxs-lookup"><span data-stu-id="f68d7-298">SalesFormletterParmDataInvoice::mayJournalTransBePosted</span></span>|
|<span data-ttu-id="f68d7-299">SalesFormletterParmDataInvoice::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-299">SalesFormletterParmDataInvoice::selectChooseLines</span></span>|
|<span data-ttu-id="f68d7-300">SalesFormLetterParmDataPackingSlip::selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-300">SalesFormletterParmDataPackingslip::selectChooseLines</span></span>|
|<span data-ttu-id="f68d7-301">SalesInvoiceDP.insertIntoSalesInvoiceTmp,insertIntoSalesInvoiceHeaderFooterTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-301">SalesInvoiceDP.insertIntoSalesInvoiceTmp,insertIntoSalesInvoiceHeaderFooterTmp</span></span>|
|<span data-ttu-id="f68d7-302">SalesInvoiceJournalCreate.createJournalLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-302">SalesInvoiceJournalCreate.createJournalLine</span></span>|
|<span data-ttu-id="f68d7-303">SalesLine.CheckItemId</span><span class="sxs-lookup"><span data-stu-id="f68d7-303">SalesLine.CheckItemId</span></span>|
|<span data-ttu-id="f68d7-304">SalesLine.ValidateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="f68d7-304">SalesLine.ValidateWrite_Server</span></span>|
|<span data-ttu-id="f68d7-305">SalesLine::calcLineAvailQty</span><span class="sxs-lookup"><span data-stu-id="f68d7-305">SalesLine::calcLineAvailQty</span></span>|
|<span data-ttu-id="f68d7-306">SalesLine::createFromTmpFrmVirtualIL</span><span class="sxs-lookup"><span data-stu-id="f68d7-306">SalesLine::createFromTmpFrmVirtualIL</span></span>|
|<span data-ttu-id="f68d7-307">SalesLineType.SalesLineType</span><span class="sxs-lookup"><span data-stu-id="f68d7-307">SalesLineType.SalesLineType</span></span>|
|<span data-ttu-id="f68d7-308">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-308">SalesPackingSlipDP.setSalesPackingSlipDetailsTmp</span></span>|
|<span data-ttu-id="f68d7-309">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-309">SalesPackingSlipDP.setSalesPackingSlipHeaderTmp</span></span>|
|<span data-ttu-id="f68d7-310">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span><span class="sxs-lookup"><span data-stu-id="f68d7-310">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span></span>|
|<span data-ttu-id="f68d7-311">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span><span class="sxs-lookup"><span data-stu-id="f68d7-311">SalesPackingSlipDP.setSysDocuBrandDetailsRegular</span></span>|
|<span data-ttu-id="f68d7-312">SalesPackingSlipJournalPost.updateInventory</span><span class="sxs-lookup"><span data-stu-id="f68d7-312">SalesPackingSlipJournalPost.updateInventory</span></span>|
|<span data-ttu-id="f68d7-313">SalesQuotationLineType_Proj.validateProjTransTypeItem</span><span class="sxs-lookup"><span data-stu-id="f68d7-313">SalesQuotationLineType_Proj.validateProjTransTypeItem</span></span>|
|<span data-ttu-id="f68d7-314">SalesQuotationProjTable データ ソース SalesQuotationline</span><span class="sxs-lookup"><span data-stu-id="f68d7-314">SalesQuotationProjTable data source SalesQuotationline</span></span>|
|<span data-ttu-id="f68d7-315">SalesQuotationTableForm.createABSFromTemplate</span><span class="sxs-lookup"><span data-stu-id="f68d7-315">SalesQuotationTableForm.createABSFromTemplate</span></span>|
|<span data-ttu-id="f68d7-316">SalesTable.setLocation</span><span class="sxs-lookup"><span data-stu-id="f68d7-316">SalesTable.setLocation</span></span>|
|<span data-ttu-id="f68d7-317">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="f68d7-317">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="f68d7-318">SalesTable2LineUpdate.update</span><span class="sxs-lookup"><span data-stu-id="f68d7-318">SalesTable2LineUpdate.update</span></span>|
|<span data-ttu-id="f68d7-319">SalesTable2LineUpdatePrompt.initpriceDiscUpdateTriggers</span><span class="sxs-lookup"><span data-stu-id="f68d7-319">SalesTable2LineUpdatePrompt.initpriceDiscUpdateTriggers</span></span>|
|<span data-ttu-id="f68d7-320">smmActivitiesEventHandler</span><span class="sxs-lookup"><span data-stu-id="f68d7-320">smmActivitiesEventHandler</span></span>|
|<span data-ttu-id="f68d7-321">SuppitemTable Table Cache Lookup プロパティ</span><span class="sxs-lookup"><span data-stu-id="f68d7-321">SuppitemTable Table Cache Lookup property</span></span>|
|<span data-ttu-id="f68d7-322">テーブル PurchPrepayTable.updateAdvanceApplicationRemaining</span><span class="sxs-lookup"><span data-stu-id="f68d7-322">Table PurchPrepayTable.updateAdvanceApplicationRemaining</span></span>|
|<span data-ttu-id="f68d7-323">TransactionReversal_Cust.reversal</span><span class="sxs-lookup"><span data-stu-id="f68d7-323">TransactionReversal_Cust.reversal</span></span>|
|<span data-ttu-id="f68d7-324">TransactionReversal_Cust.reversal</span><span class="sxs-lookup"><span data-stu-id="f68d7-324">TransactionReversal_Cust.reversal</span></span>|
|<span data-ttu-id="f68d7-325">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="f68d7-325">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="f68d7-326">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="f68d7-326">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="f68d7-327">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="f68d7-327">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="f68d7-328">TsTimesheetAddFavorites.addToFavorites</span><span class="sxs-lookup"><span data-stu-id="f68d7-328">TsTimesheetAddFavorites.addToFavorites</span></span>|
|<span data-ttu-id="f68d7-329">TsTimesheetCreate.createTimesheetLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-329">TsTimesheetCreate.createTimesheetLine</span></span>|
|<span data-ttu-id="f68d7-330">TSTimesheetEntry.initFields</span><span class="sxs-lookup"><span data-stu-id="f68d7-330">TSTimesheetEntry.initFields</span></span>|
|<span data-ttu-id="f68d7-331">TSTimesheetFavorites.createTimesheetLines</span><span class="sxs-lookup"><span data-stu-id="f68d7-331">TSTimesheetFavorites.createTimesheetLines</span></span>|
|<span data-ttu-id="f68d7-332">TSTimesheetLine.setCategoryIdFromActivity</span><span class="sxs-lookup"><span data-stu-id="f68d7-332">TSTimesheetLine.setCategoryIdFromActivity</span></span>|
|<span data-ttu-id="f68d7-333">VendInvoiceDocumentDP.insertVendInvoiceDocumentTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-333">VendInvoiceDocumentDP.insertVendInvoiceDocumentTmp</span></span>|
|<span data-ttu-id="f68d7-334">WHSLoadLine.validateStatus</span><span class="sxs-lookup"><span data-stu-id="f68d7-334">WHSLoadLine.validateStatus</span></span>|
|<span data-ttu-id="f68d7-335">WHSLoadLineAllocationProcessor.allocateLoadLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-335">WHSLoadLineAllocationProcessor.allocateLoadLine</span></span>|
|<span data-ttu-id="f68d7-336">WHSPostEngine.validateAnyDimAboveLocationMissing</span><span class="sxs-lookup"><span data-stu-id="f68d7-336">WHSPostEngine.validateAnyDimAboveLocationMissing</span></span>|
|<span data-ttu-id="f68d7-337">WhsWarehouseRelease.createShipmentsForAllSalesOrders</span><span class="sxs-lookup"><span data-stu-id="f68d7-337">WhsWarehouseRelease.createShipmentsForAllSalesOrders</span></span>|
|<span data-ttu-id="f68d7-338">WhsWarehouseRelease.createShipmentsForTransferOrders</span><span class="sxs-lookup"><span data-stu-id="f68d7-338">WhsWarehouseRelease.createShipmentsForTransferOrders</span></span>|
|<span data-ttu-id="f68d7-339">WhsWorkCreateLP.createTempTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-339">WhsWorkCreateLP.createTempTable</span></span>|
|<span data-ttu-id="f68d7-340">WHSWorkCreateProdPut.createTempTable</span><span class="sxs-lookup"><span data-stu-id="f68d7-340">WHSWorkCreateProdPut.createTempTable</span></span>|
|<span data-ttu-id="f68d7-341">WHSWorkExecuteDisplay.buildNextDimensionCaptureControl</span><span class="sxs-lookup"><span data-stu-id="f68d7-341">WHSWorkExecuteDisplay.buildNextDimensionCaptureControl</span></span>|
|<span data-ttu-id="f68d7-342">WHSWorkLine::cancelLine</span><span class="sxs-lookup"><span data-stu-id="f68d7-342">WHSWorkLine::cancelLine</span></span>|
|<span data-ttu-id="f68d7-343">WmsArrivalCreateJournal::createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="f68d7-343">WmsArrivalCreateJournal::createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="f68d7-344">WmsArrivalOverviewGeneration::updateOverviewInformation</span><span class="sxs-lookup"><span data-stu-id="f68d7-344">WmsArrivalOverviewGeneration::updateOverviewInformation</span></span>|
|<span data-ttu-id="f68d7-345">WmsJournalCheckPostReception::initJournal</span><span class="sxs-lookup"><span data-stu-id="f68d7-345">WmsJournalCheckPostReception::initJournal</span></span>|
|<span data-ttu-id="f68d7-346">WMSOrderTrans::adjustQtyWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-346">WMSOrderTrans::adjustQtyWMSOrderTrans</span></span>|
|<span data-ttu-id="f68d7-347">WMSOrderTrans::createNewWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-347">WMSOrderTrans::createNewWMSOrderTrans</span></span>|
|<span data-ttu-id="f68d7-348">WMSOrderTrans::insertOrUpdate</span><span class="sxs-lookup"><span data-stu-id="f68d7-348">WMSOrderTrans::insertOrUpdate</span></span>|
|<span data-ttu-id="f68d7-349">WMSOrderTrans::updateWMSOrderTrans</span><span class="sxs-lookup"><span data-stu-id="f68d7-349">WMSOrderTrans::updateWMSOrderTrans</span></span>|
|<span data-ttu-id="f68d7-350">WmsPickingList_OrderPickDP.insertIntoTempTable,setWMSPickingList_OrderPickTmpTemplate</span><span class="sxs-lookup"><span data-stu-id="f68d7-350">WmsPickingList_OrderPickDP.insertIntoTempTable,setWMSPickingList_OrderPickTmpTemplate</span></span>|
|<span data-ttu-id="f68d7-351">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span><span class="sxs-lookup"><span data-stu-id="f68d7-351">WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate</span></span>|
|<span data-ttu-id="f68d7-352">WrkCtrlScheduler_Proj.loadJob</span><span class="sxs-lookup"><span data-stu-id="f68d7-352">WrkCtrlScheduler_Proj.loadJob</span></span>|
|<span data-ttu-id="f68d7-353">WrkCtrScheduler_Prod.saveOperation</span><span class="sxs-lookup"><span data-stu-id="f68d7-353">WrkCtrScheduler_Prod.saveOperation</span></span>|
|<span data-ttu-id="f68d7-354">WrkCtrScheduler_Prod.saveOrder</span><span class="sxs-lookup"><span data-stu-id="f68d7-354">WrkCtrScheduler_Prod.saveOrder</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="f68d7-355">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="f68d7-355">Enumerations made extensible</span></span>

<span data-ttu-id="f68d7-356">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="f68d7-356">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="f68d7-357">列挙型</span><span class="sxs-lookup"><span data-stu-id="f68d7-357">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="f68d7-358">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="f68d7-358">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="f68d7-359">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="f68d7-359">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="f68d7-360">BankReconMatchRuleLineSysGeneratedType</span><span class="sxs-lookup"><span data-stu-id="f68d7-360">BankReconMatchRuleLineSysGeneratedType</span></span>|
|<span data-ttu-id="f68d7-361">ItemNumAlternative</span><span class="sxs-lookup"><span data-stu-id="f68d7-361">ItemNumAlternative</span></span>|
|<span data-ttu-id="f68d7-362">JmgRegistrationErrorMode</span><span class="sxs-lookup"><span data-stu-id="f68d7-362">JmgRegistrationErrorMode</span></span>|
|<span data-ttu-id="f68d7-363">MCRCustSearchType</span><span class="sxs-lookup"><span data-stu-id="f68d7-363">MCRCustSearchType</span></span>|
|<span data-ttu-id="f68d7-364">ModuleSalesPurch</span><span class="sxs-lookup"><span data-stu-id="f68d7-364">ModuleSalesPurch</span></span>|
|<span data-ttu-id="f68d7-365">ModuleSalesPurch</span><span class="sxs-lookup"><span data-stu-id="f68d7-365">ModuleSalesPurch</span></span>|
|<span data-ttu-id="f68d7-366">ProjStatusRule</span><span class="sxs-lookup"><span data-stu-id="f68d7-366">ProjStatusRule</span></span>|
|<span data-ttu-id="f68d7-367">PurchRFQUpdateType</span><span class="sxs-lookup"><span data-stu-id="f68d7-367">PurchRFQUpdateType</span></span>|
|<span data-ttu-id="f68d7-368">TAMVendRebateItemCode</span><span class="sxs-lookup"><span data-stu-id="f68d7-368">TAMVendRebateItemCode</span></span>|
|<span data-ttu-id="f68d7-369">TMSLoadBuildSupplyDemandType</span><span class="sxs-lookup"><span data-stu-id="f68d7-369">TMSLoadBuildSupplyDemandType</span></span>|


## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="f68d7-370">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="f68d7-370">Additional extensibility enhancements</span></span>

<span data-ttu-id="f68d7-371">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="f68d7-371">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="f68d7-372">EcoResProductSearchName の EDT の文字列のサイズを増加</span><span class="sxs-lookup"><span data-stu-id="f68d7-372">Increase EDT string size for EcoResProductSearchName</span></span>
- <span data-ttu-id="f68d7-373">AssetLedgerAccounts の CacheLookup プロパティを NotInTTS に変更します。</span><span class="sxs-lookup"><span data-stu-id="f68d7-373">Change CacheLookup property to NotInTTS for AssetLedgerAccounts</span></span>
- <span data-ttu-id="f68d7-374">TaxOnItem、TaxJurisdiction、TaxGroupData、TaxData、およびAssetLedgerAcounts で CacheLookup プロパティを検出に変更します。</span><span class="sxs-lookup"><span data-stu-id="f68d7-374">Change CacheLookup property to Found on TaxOnItem, TaxJurisdiction, TaxGroupData, and TaxData, and AssetLedgerAcounts</span></span>
