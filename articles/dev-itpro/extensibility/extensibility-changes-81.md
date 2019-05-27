---
title: Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations バージョン 8.1 に実装された拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 10/01/2018
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
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: App 8.1
ms.openlocfilehash: d252a5ec5feb258f9e013cc435a54bb2fc33941a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510973"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-81"></a><span data-ttu-id="36c9b-103">Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="36c9b-103">Extensibility changes in Dynamics 365 for Finance and Operations version 8.1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36c9b-104">これは、Dynamics 365 for Finance and Operations バージョン 8.1 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="36c9b-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations version 8.1.</span></span> <span data-ttu-id="36c9b-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36c9b-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="36c9b-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="36c9b-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="36c9b-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="36c9b-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="36c9b-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="36c9b-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="36c9b-109">AssetPost.createTrueUpDepreciation</span><span class="sxs-lookup"><span data-stu-id="36c9b-109">AssetPost.createTrueUpDepreciation</span></span>|
|<span data-ttu-id="36c9b-110">AssetPost.createTrueUpDepreciation</span><span class="sxs-lookup"><span data-stu-id="36c9b-110">AssetPost.createTrueUpDepreciation</span></span>|
|<span data-ttu-id="36c9b-111">AssetPostDisposal.post</span><span class="sxs-lookup"><span data-stu-id="36c9b-111">AssetPostDisposal.post</span></span>|
|<span data-ttu-id="36c9b-112">AssetPostDisposal.postVoucherTransactions</span><span class="sxs-lookup"><span data-stu-id="36c9b-112">AssetPostDisposal.postVoucherTransactions</span></span>|
|<span data-ttu-id="36c9b-113">AssetPostDisposal.postVoucherTransactions</span><span class="sxs-lookup"><span data-stu-id="36c9b-113">AssetPostDisposal.postVoucherTransactions</span></span>|
|<span data-ttu-id="36c9b-114">AssetTable.buildComposedOf</span><span class="sxs-lookup"><span data-stu-id="36c9b-114">AssetTable.buildComposedOf</span></span>|
|<span data-ttu-id="36c9b-115">AssetTable.createStruct</span><span class="sxs-lookup"><span data-stu-id="36c9b-115">AssetTable.createStruct</span></span>|
|<span data-ttu-id="36c9b-116">AxInventDim_SalesLine.setInventSiteId</span><span class="sxs-lookup"><span data-stu-id="36c9b-116">AxInventDim_SalesLine.setInventSiteId</span></span>|
|<span data-ttu-id="36c9b-117">BankChequePrint.printDocument</span><span class="sxs-lookup"><span data-stu-id="36c9b-117">BankChequePrint.printDocument</span></span>|
|<span data-ttu-id="36c9b-118">BankCodaProcessing.custSettlement</span><span class="sxs-lookup"><span data-stu-id="36c9b-118">BankCodaProcessing.custSettlement</span></span>|
|<span data-ttu-id="36c9b-119">BankDeposit.InitFromLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-119">BankDeposit.InitFromLedgerJournalTrans</span></span>|
|<span data-ttu-id="36c9b-120">BankExchAdj_RU.calcAndPostCurrency</span><span class="sxs-lookup"><span data-stu-id="36c9b-120">BankExchAdj_RU.calcAndPostCurrency</span></span>|
|<span data-ttu-id="36c9b-121">BankExchAdj_RU.calcAndPostCurrency</span><span class="sxs-lookup"><span data-stu-id="36c9b-121">BankExchAdj_RU.calcAndPostCurrency</span></span>|
|<span data-ttu-id="36c9b-122">BankExchAdj_RU.calcBalance</span><span class="sxs-lookup"><span data-stu-id="36c9b-122">BankExchAdj_RU.calcBalance</span></span>|
|<span data-ttu-id="36c9b-123">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="36c9b-123">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="36c9b-124">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="36c9b-124">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="36c9b-125">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="36c9b-125">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="36c9b-126">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="36c9b-126">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="36c9b-127">BlindCloseView.MPOS_ExtensibleViews</span><span class="sxs-lookup"><span data-stu-id="36c9b-127">BlindCloseView.MPOS_ExtensibleViews</span></span>|
|<span data-ttu-id="36c9b-128">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span><span class="sxs-lookup"><span data-stu-id="36c9b-128">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span></span>|
|<span data-ttu-id="36c9b-129">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span><span class="sxs-lookup"><span data-stu-id="36c9b-129">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span></span>|
|<span data-ttu-id="36c9b-130">BudgetAnalysisInquiryProcessor_PSN.getBudgetAnalysisLedgerDimensions</span><span class="sxs-lookup"><span data-stu-id="36c9b-130">BudgetAnalysisInquiryProcessor_PSN.getBudgetAnalysisLedgerDimensions</span></span>|
|<span data-ttu-id="36c9b-131">CAMStatisticalEntryTransferJournalEntryDataMapper.newFromParameters</span><span class="sxs-lookup"><span data-stu-id="36c9b-131">CAMStatisticalEntryTransferJournalEntryDataMapper.newFromParameters</span></span>|
|<span data-ttu-id="36c9b-132">CaseUpdateStatus_Close.changeStatus</span><span class="sxs-lookup"><span data-stu-id="36c9b-132">CaseUpdateStatus_Close.changeStatus</span></span>|
|<span data-ttu-id="36c9b-133">CashManagementView.NewExtension</span><span class="sxs-lookup"><span data-stu-id="36c9b-133">CashManagementView.NewExtension</span></span>|
|<span data-ttu-id="36c9b-134">ChequeController.init</span><span class="sxs-lookup"><span data-stu-id="36c9b-134">ChequeController.init</span></span>|
|<span data-ttu-id="36c9b-135">ChequeDP.insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="36c9b-135">ChequeDP.insertChequeTmp</span></span>|
|<span data-ttu-id="36c9b-136">クラス InventTransferEstimation.updateEstimatedPre</span><span class="sxs-lookup"><span data-stu-id="36c9b-136">Class InventTransferEstimation.updateEstimatedPre</span></span>|
|<span data-ttu-id="36c9b-137">クラス Markup.insertReturnMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-137">class Markup.insertReturnMarkupTrans</span></span>|
|<span data-ttu-id="36c9b-138">クラス MarkupTransInsert.insertForCodes</span><span class="sxs-lookup"><span data-stu-id="36c9b-138">class MarkupTransInsert.insertForCodes</span></span>|
|<span data-ttu-id="36c9b-139">クラス PurchLineType.updateSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-139">Class PurchLineType.updateSalesLine</span></span>|
|<span data-ttu-id="36c9b-140">クラス PurchPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="36c9b-140">class PurchPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="36c9b-141">クラス SalesQuantity_PackingSlip.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="36c9b-141">Class SalesQuantity_PackingSlip.calcQtyInvent</span></span>|
|<span data-ttu-id="36c9b-142">クラス SalesQuantity_PackingSlip.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="36c9b-142">Class SalesQuantity_PackingSlip.calcQtySales</span></span>|
|<span data-ttu-id="36c9b-143">Class/AssetPost.post</span><span class="sxs-lookup"><span data-stu-id="36c9b-143">Class/AssetPost.post</span></span>|
|<span data-ttu-id="36c9b-144">Class/FormLetterJournalPost.post</span><span class="sxs-lookup"><span data-stu-id="36c9b-144">Class/FormLetterJournalPost.post</span></span>|
|<span data-ttu-id="36c9b-145">Class/PurchReqTableListPageInteraction.applyFilter</span><span class="sxs-lookup"><span data-stu-id="36c9b-145">Class/PurchReqTableListPageInteraction.applyFilter</span></span>|
|<span data-ttu-id="36c9b-146">Class\PurchFormLetter_PackingSlip.checkFormLetterId</span><span class="sxs-lookup"><span data-stu-id="36c9b-146">Class\PurchFormLetter_PackingSlip.checkFormLetterId</span></span>|
|<span data-ttu-id="36c9b-147">Class\PurchFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-147">Class\PurchFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="36c9b-148">Class\TaxCalculationAdjustment.calcManualInserted</span><span class="sxs-lookup"><span data-stu-id="36c9b-148">Class\TaxCalculationAdjustment.calcManualInserted</span></span>|
|<span data-ttu-id="36c9b-149">CompanyInfoHelper.onValidateField</span><span class="sxs-lookup"><span data-stu-id="36c9b-149">CompanyInfoHelper.onValidateField</span></span>|
|<span data-ttu-id="36c9b-150">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span><span class="sxs-lookup"><span data-stu-id="36c9b-150">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span></span>|
|<span data-ttu-id="36c9b-151">CustAccountStatementExtController.initAgingBalances</span><span class="sxs-lookup"><span data-stu-id="36c9b-151">CustAccountStatementExtController.initAgingBalances</span></span>|
|<span data-ttu-id="36c9b-152">CustAccountStatementExtController.preprocessParty</span><span class="sxs-lookup"><span data-stu-id="36c9b-152">CustAccountStatementExtController.preprocessParty</span></span>|
|<span data-ttu-id="36c9b-153">CustAccountStatementExtController.processParty</span><span class="sxs-lookup"><span data-stu-id="36c9b-153">CustAccountStatementExtController.processParty</span></span>|
|<span data-ttu-id="36c9b-154">CustAccountStatementExtController.processTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-154">CustAccountStatementExtController.processTrans</span></span>|
|<span data-ttu-id="36c9b-155">CustAccountStatementExtController.runPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="36c9b-155">CustAccountStatementExtController.runPrintMgmt</span></span>|
|<span data-ttu-id="36c9b-156">CustCollectionLetterCreate.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-156">CustCollectionLetterCreate.run</span></span>|
|<span data-ttu-id="36c9b-157">CustCollectionLetterPost.RUN</span><span class="sxs-lookup"><span data-stu-id="36c9b-157">CustCollectionLetterPost.RUN</span></span>|
|<span data-ttu-id="36c9b-158">CustInterestAdjust.createCustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-158">CustInterestAdjust.createCustInvoiceTable</span></span>|
|<span data-ttu-id="36c9b-159">CustInterestCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-159">CustInterestCreate.createJournal</span></span>|
|<span data-ttu-id="36c9b-160">CustInterestCreate.logDateRecordError</span><span class="sxs-lookup"><span data-stu-id="36c9b-160">CustInterestCreate.logDateRecordError</span></span>|
|<span data-ttu-id="36c9b-161">CustInterestCreate.newAccount</span><span class="sxs-lookup"><span data-stu-id="36c9b-161">CustInterestCreate.newAccount</span></span>|
|<span data-ttu-id="36c9b-162">CustInterestCreate.resetCustInterest</span><span class="sxs-lookup"><span data-stu-id="36c9b-162">CustInterestCreate.resetCustInterest</span></span>|
|<span data-ttu-id="36c9b-163">CustInterestCreate.runOnce</span><span class="sxs-lookup"><span data-stu-id="36c9b-163">CustInterestCreate.runOnce</span></span>|
|<span data-ttu-id="36c9b-164">CustInvoiceCalcTax_Invoice.updateTaxWriteCode</span><span class="sxs-lookup"><span data-stu-id="36c9b-164">CustInvoiceCalcTax_Invoice.updateTaxWriteCode</span></span>|
|<span data-ttu-id="36c9b-165">CustInvoiceLine.Insert</span><span class="sxs-lookup"><span data-stu-id="36c9b-165">CustInvoiceLine.Insert</span></span>|
|<span data-ttu-id="36c9b-166">CustOutPaym.generatePaymentLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-166">CustOutPaym.generatePaymentLines</span></span>|
|<span data-ttu-id="36c9b-167">CustQuotationJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-167">CustQuotationJour.printJournal</span></span>|
|<span data-ttu-id="36c9b-168">CustTable.CanSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="36c9b-168">CustTable.CanSubmitToWorkflow</span></span>|
|<span data-ttu-id="36c9b-169">CustTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="36c9b-169">CustTrans.documentDateModified</span></span>|
|<span data-ttu-id="36c9b-170">CustTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="36c9b-170">CustTrans.documentDateModified</span></span>|
|<span data-ttu-id="36c9b-171">CustTransSettlement.insertSettlementLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-171">CustTransSettlement.insertSettlementLines</span></span>|
|<span data-ttu-id="36c9b-172">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-172">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="36c9b-173">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="36c9b-173">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="36c9b-174">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="36c9b-174">CustVendCheque.output</span></span>|
|<span data-ttu-id="36c9b-175">CustVendChequeSlipTextCalculator.seebelow</span><span class="sxs-lookup"><span data-stu-id="36c9b-175">CustVendChequeSlipTextCalculator.seebelow</span></span>|
|<span data-ttu-id="36c9b-176">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="36c9b-176">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span></span>|
|<span data-ttu-id="36c9b-177">CustVendPaymProposalTransferToJournal.transferProposal</span><span class="sxs-lookup"><span data-stu-id="36c9b-177">CustVendPaymProposalTransferToJournal.transferProposal</span></span>|
|<span data-ttu-id="36c9b-178">CustVendPaymSched.construct</span><span class="sxs-lookup"><span data-stu-id="36c9b-178">CustVendPaymSched.construct</span></span>|
|<span data-ttu-id="36c9b-179">CustVendPaymSched.initCalcPaymSched</span><span class="sxs-lookup"><span data-stu-id="36c9b-179">CustVendPaymSched.initCalcPaymSched</span></span>|
|<span data-ttu-id="36c9b-180">CustVendReversePosting.restoreCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="36c9b-180">CustVendReversePosting.restoreCustVendTransOpen</span></span>|
|<span data-ttu-id="36c9b-181">CustVendVoucher.post</span><span class="sxs-lookup"><span data-stu-id="36c9b-181">CustVendVoucher.post</span></span>|
|<span data-ttu-id="36c9b-182">DataEntityView/SalesOrderLineEntity/Method/validateWrite</span><span class="sxs-lookup"><span data-stu-id="36c9b-182">DataEntityView/SalesOrderLineEntity/Method/validateWrite</span></span>|
|<span data-ttu-id="36c9b-183">DataEntityView/SalesQuotationLineEntity/Method/validateWrite</span><span class="sxs-lookup"><span data-stu-id="36c9b-183">DataEntityView/SalesQuotationLineEntity/Method/validateWrite</span></span>|
|<span data-ttu-id="36c9b-184">EFDocEmailProcessor_BR.saveReceivedXmlData</span><span class="sxs-lookup"><span data-stu-id="36c9b-184">EFDocEmailProcessor_BR.saveReceivedXmlData</span></span>|
|<span data-ttu-id="36c9b-185">EFDocMsgFormat_XmlBase_BR.createElementWithValue</span><span class="sxs-lookup"><span data-stu-id="36c9b-185">EFDocMsgFormat_XmlBase_BR.createElementWithValue</span></span>|
|<span data-ttu-id="36c9b-186">メソッドに抽出: SalesParmTable.GetPaymentSched</span><span class="sxs-lookup"><span data-stu-id="36c9b-186">Extract into method: SalesParmTable.GetPaymentSched</span></span>|
|<span data-ttu-id="36c9b-187">フォーム InventJournalAsset\Methods\init</span><span class="sxs-lookup"><span data-stu-id="36c9b-187">Form InventJournalAsset\Methods\init</span></span>|
|<span data-ttu-id="36c9b-188">フォーム InventJournalCount\Methods\init</span><span class="sxs-lookup"><span data-stu-id="36c9b-188">Form InventJournalCount\Methods\init</span></span>|
|<span data-ttu-id="36c9b-189">フォーム InventJournalMovement.init</span><span class="sxs-lookup"><span data-stu-id="36c9b-189">Form InventJournalMovement.init</span></span>|
|<span data-ttu-id="36c9b-190">フォーム TrvExpenses.confirmCategoryChange</span><span class="sxs-lookup"><span data-stu-id="36c9b-190">Form TrvExpenses.confirmCategoryChange</span></span>|
|<span data-ttu-id="36c9b-191">Form\SalesEditLines.closeOk</span><span class="sxs-lookup"><span data-stu-id="36c9b-191">Form\SalesEditLines.closeOk</span></span>|
|<span data-ttu-id="36c9b-192">FormletterJournalPost.newPostPurch</span><span class="sxs-lookup"><span data-stu-id="36c9b-192">FormletterJournalPost.newPostPurch</span></span>|
|<span data-ttu-id="36c9b-193">FreeTextInvoiceDP.Variable 宣言</span><span class="sxs-lookup"><span data-stu-id="36c9b-193">FreeTextInvoiceDP.Variable declaration</span></span>|
|<span data-ttu-id="36c9b-194">HcmActionTypeSetup.lookupWorkflowTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-194">HcmActionTypeSetup.lookupWorkflowTable</span></span>|
|<span data-ttu-id="36c9b-195">HcmPosition_HcmPositionDefaultDimension_formDatasource.selectionChanged</span><span class="sxs-lookup"><span data-stu-id="36c9b-195">HcmPosition_HcmPositionDefaultDimension_formDatasource.selectionChanged</span></span>|
|<span data-ttu-id="36c9b-196">HcmPositionTransition:: createHcmPositionWorkerAssignment</span><span class="sxs-lookup"><span data-stu-id="36c9b-196">HcmPositionTransition:: createHcmPositionWorkerAssignment</span></span>|
|<span data-ttu-id="36c9b-197">HcmPositionWorkerAssignmentDialog:: createWorkerActionOk</span><span class="sxs-lookup"><span data-stu-id="36c9b-197">HcmPositionWorkerAssignmentDialog:: createWorkerActionOk</span></span>|
|<span data-ttu-id="36c9b-198">HRMCompFixedPlanTable::enforcePayRateTolerance</span><span class="sxs-lookup"><span data-stu-id="36c9b-198">HRMCompFixedPlanTable::enforcePayRateTolerance</span></span> |
|<span data-ttu-id="36c9b-199">InterCompanyPostPurch.construct</span><span class="sxs-lookup"><span data-stu-id="36c9b-199">InterCompanyPostPurch.construct</span></span>|
|<span data-ttu-id="36c9b-200">InterCompanyPostPurch.formLetterUpdate</span><span class="sxs-lookup"><span data-stu-id="36c9b-200">InterCompanyPostPurch.formLetterUpdate</span></span>|
|<span data-ttu-id="36c9b-201">InterCompanyPostSales.formLetterUpdate</span><span class="sxs-lookup"><span data-stu-id="36c9b-201">InterCompanyPostSales.formLetterUpdate</span></span>|
|<span data-ttu-id="36c9b-202">InterCompanySyncPurchTableType.setSalesTableData</span><span class="sxs-lookup"><span data-stu-id="36c9b-202">InterCompanySyncPurchTableType.setSalesTableData</span></span>|
|<span data-ttu-id="36c9b-203">IntrastatCheck.Run</span><span class="sxs-lookup"><span data-stu-id="36c9b-203">IntrastatCheck.Run</span></span>|
|<span data-ttu-id="36c9b-204">IntrastatTransfer.calcAmountsAndMarkups</span><span class="sxs-lookup"><span data-stu-id="36c9b-204">IntrastatTransfer.calcAmountsAndMarkups</span></span>|
|<span data-ttu-id="36c9b-205">IntrastatTransfer.calcValuesSign</span><span class="sxs-lookup"><span data-stu-id="36c9b-205">IntrastatTransfer.calcValuesSign</span></span>|
|<span data-ttu-id="36c9b-206">IntrastatTransfer.distributeIntrastatAddValueLV</span><span class="sxs-lookup"><span data-stu-id="36c9b-206">IntrastatTransfer.distributeIntrastatAddValueLV</span></span>|
|<span data-ttu-id="36c9b-207">IntrastatTransfer.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-207">IntrastatTransfer.run</span></span>|
|<span data-ttu-id="36c9b-208">IntrastatTransferIT.calcCounty</span><span class="sxs-lookup"><span data-stu-id="36c9b-208">IntrastatTransferIT.calcCounty</span></span>|
|<span data-ttu-id="36c9b-209">IntrastatTransferIT.updateTransactionCurrencyAmount</span><span class="sxs-lookup"><span data-stu-id="36c9b-209">IntrastatTransferIT.updateTransactionCurrencyAmount</span></span>|
|<span data-ttu-id="36c9b-210">InventAdj_Transact.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-210">InventAdj_Transact.run</span></span>|
|<span data-ttu-id="36c9b-211">InventCostPost.postInventCostTransVariance</span><span class="sxs-lookup"><span data-stu-id="36c9b-211">InventCostPost.postInventCostTransVariance</span></span>|
|<span data-ttu-id="36c9b-212">InventMov_Purch.updateAutoLossProfit</span><span class="sxs-lookup"><span data-stu-id="36c9b-212">InventMov_Purch.updateAutoLossProfit</span></span>|
|<span data-ttu-id="36c9b-213">InventMov_Purch.updateBuffer</span><span class="sxs-lookup"><span data-stu-id="36c9b-213">InventMov_Purch.updateBuffer</span></span>|
|<span data-ttu-id="36c9b-214">InventMovement.checkUpdatePhysical</span><span class="sxs-lookup"><span data-stu-id="36c9b-214">InventMovement.checkUpdatePhysical</span></span>|
|<span data-ttu-id="36c9b-215">InventoryLookupMatrixView.ExtensibleViews</span><span class="sxs-lookup"><span data-stu-id="36c9b-215">InventoryLookupMatrixView.ExtensibleViews</span></span>|
|<span data-ttu-id="36c9b-216">InventTable.pdsValidateBestBeforeDays</span><span class="sxs-lookup"><span data-stu-id="36c9b-216">InventTable.pdsValidateBestBeforeDays</span></span>|
|<span data-ttu-id="36c9b-217">InventTransWMS_Register.updateInventFromMovementServer</span><span class="sxs-lookup"><span data-stu-id="36c9b-217">InventTransWMS_Register.updateInventFromMovementServer</span></span>|
|<span data-ttu-id="36c9b-218">InventUpd_ChildReference.updateLessIssue</span><span class="sxs-lookup"><span data-stu-id="36c9b-218">InventUpd_ChildReference.updateLessIssue</span></span>|
|<span data-ttu-id="36c9b-219">InventUpd_ChildReference.updateLessReceipt</span><span class="sxs-lookup"><span data-stu-id="36c9b-219">InventUpd_ChildReference.updateLessReceipt</span></span>|
|<span data-ttu-id="36c9b-220">InventUpd_ChildReference.updateMoreIssue</span><span class="sxs-lookup"><span data-stu-id="36c9b-220">InventUpd_ChildReference.updateMoreIssue</span></span>|
|<span data-ttu-id="36c9b-221">InventUpd_ChildReference.updateMoreReceipt</span><span class="sxs-lookup"><span data-stu-id="36c9b-221">InventUpd_ChildReference.updateMoreReceipt</span></span>|
|<span data-ttu-id="36c9b-222">InventUpd_Financial.newSalesInvoice</span><span class="sxs-lookup"><span data-stu-id="36c9b-222">InventUpd_Financial.newSalesInvoice</span></span>|
|<span data-ttu-id="36c9b-223">InventUpd_Physical.updatePhysicalIssue</span><span class="sxs-lookup"><span data-stu-id="36c9b-223">InventUpd_Physical.updatePhysicalIssue</span></span>|
|<span data-ttu-id="36c9b-224">InventUpd_Physical.updateTransPhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="36c9b-224">InventUpd_Physical.updateTransPhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="36c9b-225">InventUpd_Physical::newSalesPackingSlip</span><span class="sxs-lookup"><span data-stu-id="36c9b-225">InventUpd_Physical::newSalesPackingSlip</span></span>|
|<span data-ttu-id="36c9b-226">InventUpd_Reservation.updateNow</span><span class="sxs-lookup"><span data-stu-id="36c9b-226">InventUpd_Reservation.updateNow</span></span>|
|<span data-ttu-id="36c9b-227">InventUpd_Reservation.updateReserveMore</span><span class="sxs-lookup"><span data-stu-id="36c9b-227">InventUpd_Reservation.updateReserveMore</span></span>|
|<span data-ttu-id="36c9b-228">InventUpdate.updateInventTransPosting</span><span class="sxs-lookup"><span data-stu-id="36c9b-228">InventUpdate.updateInventTransPosting</span></span>|
|<span data-ttu-id="36c9b-229">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-229">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="36c9b-230">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-230">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="36c9b-231">InventUpdateMarking.addMarking</span><span class="sxs-lookup"><span data-stu-id="36c9b-231">InventUpdateMarking.addMarking</span></span>|
|<span data-ttu-id="36c9b-232">InventUpdateMarking.removeMarking</span><span class="sxs-lookup"><span data-stu-id="36c9b-232">InventUpdateMarking.removeMarking</span></span>|
|<span data-ttu-id="36c9b-233">InventUpdateReserveMore.createQueryRuns</span><span class="sxs-lookup"><span data-stu-id="36c9b-233">InventUpdateReserveMore.createQueryRuns</span></span>|
|<span data-ttu-id="36c9b-234">JmgCalcApprovePickDialog.closeOk</span><span class="sxs-lookup"><span data-stu-id="36c9b-234">JmgCalcApprovePickDialog.closeOk</span></span>|
|<span data-ttu-id="36c9b-235">JmgJobBundle.postTime</span><span class="sxs-lookup"><span data-stu-id="36c9b-235">JmgJobBundle.postTime</span></span>|
|<span data-ttu-id="36c9b-236">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span><span class="sxs-lookup"><span data-stu-id="36c9b-236">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span></span>|
|<span data-ttu-id="36c9b-237">JournalStaticDataModel.initializeJournalTableFields</span><span class="sxs-lookup"><span data-stu-id="36c9b-237">JournalStaticDataModel.initializeJournalTableFields</span></span>|
|<span data-ttu-id="36c9b-238">Ledger.populateTmpTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-238">Ledger.populateTmpTable</span></span>|
|<span data-ttu-id="36c9b-239">Ledger::populateTmpTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-239">Ledger::populateTmpTable</span></span>|
|<span data-ttu-id="36c9b-240">LedgerAccrualTrans_Calendar.allocate</span><span class="sxs-lookup"><span data-stu-id="36c9b-240">LedgerAccrualTrans_Calendar.allocate</span></span>|
|<span data-ttu-id="36c9b-241">LedgerAccrualTrans_Calendar.allocate</span><span class="sxs-lookup"><span data-stu-id="36c9b-241">LedgerAccrualTrans_Calendar.allocate</span></span>|
|<span data-ttu-id="36c9b-242">LedgerAccrualTrans_Fiscal.allocate</span><span class="sxs-lookup"><span data-stu-id="36c9b-242">LedgerAccrualTrans_Fiscal.allocate</span></span>|
|<span data-ttu-id="36c9b-243">LedgerAccrualTrans_Fiscal.allocate</span><span class="sxs-lookup"><span data-stu-id="36c9b-243">LedgerAccrualTrans_Fiscal.allocate</span></span>|
|<span data-ttu-id="36c9b-244">LedgerAutomaticTransactionAccountEntity</span><span class="sxs-lookup"><span data-stu-id="36c9b-244">LedgerAutomaticTransactionAccountEntity</span></span>|
|<span data-ttu-id="36c9b-245">LedgerCreatePeriodBalances.createPeriodBalancesMainAccount</span><span class="sxs-lookup"><span data-stu-id="36c9b-245">LedgerCreatePeriodBalances.createPeriodBalancesMainAccount</span></span>|
|<span data-ttu-id="36c9b-246">LedgerExchAdj.postAdjustment</span><span class="sxs-lookup"><span data-stu-id="36c9b-246">LedgerExchAdj.postAdjustment</span></span>|
|<span data-ttu-id="36c9b-247">LedgerExchAdj.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-247">LedgerExchAdj.run</span></span>|
|<span data-ttu-id="36c9b-248">LedgerFiscalJournalDP_IT.getDisplaySequenceNumber</span><span class="sxs-lookup"><span data-stu-id="36c9b-248">LedgerFiscalJournalDP_IT.getDisplaySequenceNumber</span></span>|
|<span data-ttu-id="36c9b-249">LedgerJournalCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-249">LedgerJournalCheckPost.checkJournal</span></span>|
|<span data-ttu-id="36c9b-250">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-250">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="36c9b-251">LedgerJournalCheckPost.runInternal</span><span class="sxs-lookup"><span data-stu-id="36c9b-251">LedgerJournalCheckPost.runInternal</span></span>|
|<span data-ttu-id="36c9b-252">LedgerJournalEngine.accountModified</span><span class="sxs-lookup"><span data-stu-id="36c9b-252">LedgerJournalEngine.accountModified</span></span>|
|<span data-ttu-id="36c9b-253">LedgerJournalEngine.calculateTaxForCompleteJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-253">LedgerJournalEngine.calculateTaxForCompleteJournal</span></span>|
|<span data-ttu-id="36c9b-254">LedgerJournalEngine.findSettledAmount</span><span class="sxs-lookup"><span data-stu-id="36c9b-254">LedgerJournalEngine.findSettledAmount</span></span>|
|<span data-ttu-id="36c9b-255">LedgerJournalEngine.formSettlement</span><span class="sxs-lookup"><span data-stu-id="36c9b-255">LedgerJournalEngine.formSettlement</span></span>|
|<span data-ttu-id="36c9b-256">LedgerJournalEngine.newVoucher</span><span class="sxs-lookup"><span data-stu-id="36c9b-256">LedgerJournalEngine.newVoucher</span></span>|
|<span data-ttu-id="36c9b-257">LedgerJournalPeriodicCopy.journalTransCopy</span><span class="sxs-lookup"><span data-stu-id="36c9b-257">LedgerJournalPeriodicCopy.journalTransCopy</span></span>|
|<span data-ttu-id="36c9b-258">LedgerJournalTrans.checkVATTransaction</span><span class="sxs-lookup"><span data-stu-id="36c9b-258">LedgerJournalTrans.checkVATTransaction</span></span>|
|<span data-ttu-id="36c9b-259">LedgerJournalTrans.checkVatTransaction</span><span class="sxs-lookup"><span data-stu-id="36c9b-259">LedgerJournalTrans.checkVatTransaction</span></span>|
|<span data-ttu-id="36c9b-260">LedgerJournalTrans.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="36c9b-260">LedgerJournalTrans.validateWrite_Server</span></span>|
|<span data-ttu-id="36c9b-261">LedgerJournalTrans_Project.checkCategoryId</span><span class="sxs-lookup"><span data-stu-id="36c9b-261">LedgerJournalTrans_Project.checkCategoryId</span></span>|
|<span data-ttu-id="36c9b-262">LedgerJournalTransUpdateAsset</span><span class="sxs-lookup"><span data-stu-id="36c9b-262">LedgerJournalTransUpdateAsset</span></span>|
|<span data-ttu-id="36c9b-263">LedgerJournalTransUpdateLedger.updateNow</span><span class="sxs-lookup"><span data-stu-id="36c9b-263">LedgerJournalTransUpdateLedger.updateNow</span></span>|
|<span data-ttu-id="36c9b-264">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-264">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span></span>|
|<span data-ttu-id="36c9b-265">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-265">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span></span>|
|<span data-ttu-id="36c9b-266">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-266">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span></span>|
|<span data-ttu-id="36c9b-267">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-267">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span></span>|
|<span data-ttu-id="36c9b-268">LedgerJournalTransVoucherTemplates.SaveVoucherTemplate、CreateVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-268">LedgerJournalTransVoucherTemplates.SaveVoucherTemplate, CreateVoucherTemplate</span></span>|
|<span data-ttu-id="36c9b-269">LedgerPostingGeneralJournalController.addLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-269">LedgerPostingGeneralJournalController.addLine</span></span>|
|<span data-ttu-id="36c9b-270">LedgerPostingGeneralJournalController.getLineValues</span><span class="sxs-lookup"><span data-stu-id="36c9b-270">LedgerPostingGeneralJournalController.getLineValues</span></span>|
|<span data-ttu-id="36c9b-271">LedgerTransferOpening.getMainAccountStorageSegment</span><span class="sxs-lookup"><span data-stu-id="36c9b-271">LedgerTransferOpening.getMainAccountStorageSegment</span></span>|
|<span data-ttu-id="36c9b-272">LedgerTransferOpening.processNewClosingRecordsForOpening</span><span class="sxs-lookup"><span data-stu-id="36c9b-272">LedgerTransferOpening.processNewClosingRecordsForOpening</span></span>|
|<span data-ttu-id="36c9b-273">LedgerTransferOpening.processQueryForPublicSector</span><span class="sxs-lookup"><span data-stu-id="36c9b-273">LedgerTransferOpening.processQueryForPublicSector</span></span>|
|<span data-ttu-id="36c9b-274">LedgerTransModule.tax</span><span class="sxs-lookup"><span data-stu-id="36c9b-274">LedgerTransModule.tax</span></span>|
|<span data-ttu-id="36c9b-275">LedgerVoucherObject.allocateTransaction</span><span class="sxs-lookup"><span data-stu-id="36c9b-275">LedgerVoucherObject.allocateTransaction</span></span>|
|<span data-ttu-id="36c9b-276">LedgerVoucherObject.updateLedgerPostingJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-276">LedgerVoucherObject.updateLedgerPostingJournal</span></span>|
|<span data-ttu-id="36c9b-277">LogisticsEntityLocationFormHandler.manageControls</span><span class="sxs-lookup"><span data-stu-id="36c9b-277">LogisticsEntityLocationFormHandler.manageControls</span></span>|
|<span data-ttu-id="36c9b-278">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span><span class="sxs-lookup"><span data-stu-id="36c9b-278">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span></span>|
|<span data-ttu-id="36c9b-279">MainAccount.canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="36c9b-279">MainAccount.canSubmitToWorkflow</span></span>|
|<span data-ttu-id="36c9b-280">可能であれば変数宣言を最初の割り当てに移動</span><span class="sxs-lookup"><span data-stu-id="36c9b-280">Move variable declaration to first assignment when possible</span></span>|
|<span data-ttu-id="36c9b-281">NewElement.NewMethod</span><span class="sxs-lookup"><span data-stu-id="36c9b-281">NewElement.NewMethod</span></span>|
|<span data-ttu-id="36c9b-282">OmOperatingUnit.getDimensionViewId</span><span class="sxs-lookup"><span data-stu-id="36c9b-282">OmOperatingUnit.getDimensionViewId</span></span>|
|<span data-ttu-id="36c9b-283">Originaldocuments.findFromCustTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-283">Originaldocuments.findFromCustTrans</span></span>|
|<span data-ttu-id="36c9b-284">Originaldocuments.findFromGeneralJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-284">Originaldocuments.findFromGeneralJournal</span></span>|
|<span data-ttu-id="36c9b-285">PaymSchedCalc.createCustVendTransaction</span><span class="sxs-lookup"><span data-stu-id="36c9b-285">PaymSchedCalc.createCustVendTransaction</span></span>|
|<span data-ttu-id="36c9b-286">PaymSchedCalc.initFromPurchTotals</span><span class="sxs-lookup"><span data-stu-id="36c9b-286">PaymSchedCalc.initFromPurchTotals</span></span>|
|<span data-ttu-id="36c9b-287">PaymSchedCalc.initFromSalesTotals</span><span class="sxs-lookup"><span data-stu-id="36c9b-287">PaymSchedCalc.initFromSalesTotals</span></span>|
|<span data-ttu-id="36c9b-288">POSApidts.NewTrigger</span><span class="sxs-lookup"><span data-stu-id="36c9b-288">POSApidts.NewTrigger</span></span>|
|<span data-ttu-id="36c9b-289">PosAPidts.NewTrigger</span><span class="sxs-lookup"><span data-stu-id="36c9b-289">PosAPidts.NewTrigger</span></span>|
|<span data-ttu-id="36c9b-290">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span><span class="sxs-lookup"><span data-stu-id="36c9b-290">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span></span>|
|<span data-ttu-id="36c9b-291">PriceDiscAdmCheckPost.runFromContract</span><span class="sxs-lookup"><span data-stu-id="36c9b-291">PriceDiscAdmCheckPost.runFromContract</span></span>|
|<span data-ttu-id="36c9b-292">PriceDiscTable.buildSearchFilter</span><span class="sxs-lookup"><span data-stu-id="36c9b-292">PriceDiscTable.buildSearchFilter</span></span>|
|<span data-ttu-id="36c9b-293">PrintableReceipt</span><span class="sxs-lookup"><span data-stu-id="36c9b-293">PrintableReceipt</span></span>|
|<span data-ttu-id="36c9b-294">ProjAdjustmentUpdate.newPostAdjustment</span><span class="sxs-lookup"><span data-stu-id="36c9b-294">ProjAdjustmentUpdate.newPostAdjustment</span></span>|
|<span data-ttu-id="36c9b-295">ProjAdjustmentUpdate.projTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-295">ProjAdjustmentUpdate.projTrans</span></span>|
|<span data-ttu-id="36c9b-296">ProjAdjustmentUpdate.transEmplNew</span><span class="sxs-lookup"><span data-stu-id="36c9b-296">ProjAdjustmentUpdate.transEmplNew</span></span>|
|<span data-ttu-id="36c9b-297">ProjAdjustmentUpdate_Post.Post</span><span class="sxs-lookup"><span data-stu-id="36c9b-297">ProjAdjustmentUpdate_Post.Post</span></span>|
|<span data-ttu-id="36c9b-298">ProjAdjustmentUpdate_Post.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-298">ProjAdjustmentUpdate_Post.update</span></span>|
|<span data-ttu-id="36c9b-299">ProjBudgetManager.createBudgetRevenueForecast、createBudgetSalesForecast</span><span class="sxs-lookup"><span data-stu-id="36c9b-299">ProjBudgetManager.createBudgetRevenueForecast, createBudgetSalesForecast</span></span>|
|<span data-ttu-id="36c9b-300">ProjBudgetManager.insertProjBudgetLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-300">ProjBudgetManager.insertProjBudgetLine</span></span>|
|<span data-ttu-id="36c9b-301">ProjBudgetManager.insertProjBudgetLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-301">ProjBudgetManager.insertProjBudgetLine</span></span>|
|<span data-ttu-id="36c9b-302">ProjBudgetManager.updateProjBudgetLinesWithAmt</span><span class="sxs-lookup"><span data-stu-id="36c9b-302">ProjBudgetManager.updateProjBudgetLinesWithAmt</span></span>|
|<span data-ttu-id="36c9b-303">ProjCategory.categoryType2CategoryEmplOption</span><span class="sxs-lookup"><span data-stu-id="36c9b-303">ProjCategory.categoryType2CategoryEmplOption</span></span>|
|<span data-ttu-id="36c9b-304">ProjCategory.categoryType2CategoryEmplOption</span><span class="sxs-lookup"><span data-stu-id="36c9b-304">ProjCategory.categoryType2CategoryEmplOption</span></span>|
|<span data-ttu-id="36c9b-305">ProjCategory.categoryType2TransType</span><span class="sxs-lookup"><span data-stu-id="36c9b-305">ProjCategory.categoryType2TransType</span></span>|
|<span data-ttu-id="36c9b-306">Projcategory.transType2CategoryType</span><span class="sxs-lookup"><span data-stu-id="36c9b-306">Projcategory.transType2CategoryType</span></span>|
|<span data-ttu-id="36c9b-307">Projcontrol.categoryType2CostType</span><span class="sxs-lookup"><span data-stu-id="36c9b-307">Projcontrol.categoryType2CostType</span></span>|
|<span data-ttu-id="36c9b-308">Projcontrol.costType2CategoryType</span><span class="sxs-lookup"><span data-stu-id="36c9b-308">Projcontrol.costType2CategoryType</span></span>|
|<span data-ttu-id="36c9b-309">ProjControlPosting.insertControlTrans、processSalesValue</span><span class="sxs-lookup"><span data-stu-id="36c9b-309">ProjControlPosting.insertControlTrans, processSalesValue</span></span>|
|<span data-ttu-id="36c9b-310">ProjectSourceDocumentLineItemHelper.projOrigin および projTransType</span><span class="sxs-lookup"><span data-stu-id="36c9b-310">ProjectSourceDocumentLineItemHelper.projOrigin and projTransType</span></span>|
|<span data-ttu-id="36c9b-311">ProjForecastListPageInteraction.runForcastFormBasedOnForecastUnion</span><span class="sxs-lookup"><span data-stu-id="36c9b-311">ProjForecastListPageInteraction.runForcastFormBasedOnForecastUnion</span></span>|
|<span data-ttu-id="36c9b-312">ProjForecastReduce.newProjPost</span><span class="sxs-lookup"><span data-stu-id="36c9b-312">ProjForecastReduce.newProjPost</span></span>|
|<span data-ttu-id="36c9b-313">ProjFormLetter メソッド main/mainOnServer</span><span class="sxs-lookup"><span data-stu-id="36c9b-313">ProjFormLetter method main/mainOnServer</span></span>|
|<span data-ttu-id="36c9b-314">ProjInvoiceCancel.cancelProposal</span><span class="sxs-lookup"><span data-stu-id="36c9b-314">ProjInvoiceCancel.cancelProposal</span></span>|
|<span data-ttu-id="36c9b-315">ProjInvoiceChoose.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-315">ProjInvoiceChoose.run</span></span>|
|<span data-ttu-id="36c9b-316">ProjInvoiceJournalCreate.createJournalHeader</span><span class="sxs-lookup"><span data-stu-id="36c9b-316">ProjInvoiceJournalCreate.createJournalHeader</span></span>|
|<span data-ttu-id="36c9b-317">ProjInvoiceLines.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-317">ProjInvoiceLines.run</span></span>|
|<span data-ttu-id="36c9b-318">ProjInvoiceProposalCreateLines.loadLastValue</span><span class="sxs-lookup"><span data-stu-id="36c9b-318">ProjInvoiceProposalCreateLines.loadLastValue</span></span>|
|<span data-ttu-id="36c9b-319">ProjInvoiceProposalCreateLines.runItemQuery</span><span class="sxs-lookup"><span data-stu-id="36c9b-319">ProjInvoiceProposalCreateLines.runItemQuery</span></span>|
|<span data-ttu-id="36c9b-320">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-320">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="36c9b-321">ProjInvoiceProposalInsertLines.setProjProposalJour</span><span class="sxs-lookup"><span data-stu-id="36c9b-321">ProjInvoiceProposalInsertLines.setProjProposalJour</span></span>|
|<span data-ttu-id="36c9b-322">ProjInvoiceProposalInsertLines.setProjProposalJour</span><span class="sxs-lookup"><span data-stu-id="36c9b-322">ProjInvoiceProposalInsertLines.setProjProposalJour</span></span>|
|<span data-ttu-id="36c9b-323">ProjInvoiceProposalInsertLines.setProjProposalTotals</span><span class="sxs-lookup"><span data-stu-id="36c9b-323">ProjInvoiceProposalInsertLines.setProjProposalTotals</span></span>|
|<span data-ttu-id="36c9b-324">ProjInvoiceTableCreate.initializeValues</span><span class="sxs-lookup"><span data-stu-id="36c9b-324">ProjInvoiceTableCreate.initializeValues</span></span>|
|<span data-ttu-id="36c9b-325">Projparameters.defaultProjCategory</span><span class="sxs-lookup"><span data-stu-id="36c9b-325">Projparameters.defaultProjCategory</span></span>|
|<span data-ttu-id="36c9b-326">ProjPeriodPostingLedgerCost.updateTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-326">ProjPeriodPostingLedgerCost.updateTrans</span></span>|
|<span data-ttu-id="36c9b-327">ProjPost.newCheckTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-327">ProjPost.newCheckTrans</span></span>|
|<span data-ttu-id="36c9b-328">Projpost.newCreateProjTransAndLedger</span><span class="sxs-lookup"><span data-stu-id="36c9b-328">Projpost.newCreateProjTransAndLedger</span></span>|
|<span data-ttu-id="36c9b-329">Projpost.newCreateProjTransAndLedgerAdj</span><span class="sxs-lookup"><span data-stu-id="36c9b-329">Projpost.newCreateProjTransAndLedgerAdj</span></span>|
|<span data-ttu-id="36c9b-330">Projpost.newTransAdjNegativeJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-330">Projpost.newTransAdjNegativeJournal</span></span>|
|<span data-ttu-id="36c9b-331">Projpost.postcost</span><span class="sxs-lookup"><span data-stu-id="36c9b-331">Projpost.postcost</span></span>|
|<span data-ttu-id="36c9b-332">ProjSalesItemReq.modified</span><span class="sxs-lookup"><span data-stu-id="36c9b-332">ProjSalesItemReq.modified</span></span>|
|<span data-ttu-id="36c9b-333">ProjSplitBill.transType</span><span class="sxs-lookup"><span data-stu-id="36c9b-333">ProjSplitBill.transType</span></span>|
|<span data-ttu-id="36c9b-334">ProjSplitBill.transType</span><span class="sxs-lookup"><span data-stu-id="36c9b-334">ProjSplitBill.transType</span></span>|
|<span data-ttu-id="36c9b-335">ProjTable.generateNextSubProjectId</span><span class="sxs-lookup"><span data-stu-id="36c9b-335">ProjTable.generateNextSubProjectId</span></span>|
|<span data-ttu-id="36c9b-336">ProjTableCreate.canClose</span><span class="sxs-lookup"><span data-stu-id="36c9b-336">ProjTableCreate.canClose</span></span>|
|<span data-ttu-id="36c9b-337">ProjTableLookup.isJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-337">ProjTableLookup.isJournal</span></span>|
|<span data-ttu-id="36c9b-338">ProjTableWizardCtrl.createProject</span><span class="sxs-lookup"><span data-stu-id="36c9b-338">ProjTableWizardCtrl.createProject</span></span>|
|<span data-ttu-id="36c9b-339">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="36c9b-339">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="36c9b-340">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="36c9b-340">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="36c9b-341">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="36c9b-341">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="36c9b-342">PSAProjRetainerInvoicing.run</span><span class="sxs-lookup"><span data-stu-id="36c9b-342">PSAProjRetainerInvoicing.run</span></span>|
|<span data-ttu-id="36c9b-343">PsaQuotationsController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="36c9b-343">PsaQuotationsController.getReportTitle</span></span>|
|<span data-ttu-id="36c9b-344">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="36c9b-344">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="36c9b-345">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="36c9b-345">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="36c9b-346">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="36c9b-346">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="36c9b-347">PurchAutoCreate_Sales.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-347">PurchAutoCreate_Sales.createPurchTable</span></span>|
|<span data-ttu-id="36c9b-348">PurchAutoCreate_Sales.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-348">PurchAutoCreate_Sales.setPurchTable</span></span>|
|<span data-ttu-id="36c9b-349">PurchCalcTax_Invoice.updateTaxWriteCode</span><span class="sxs-lookup"><span data-stu-id="36c9b-349">PurchCalcTax_Invoice.updateTaxWriteCode</span></span>|
|<span data-ttu-id="36c9b-350">PurchCopying.copyLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-350">PurchCopying.copyLine</span></span>|
|<span data-ttu-id="36c9b-351">PurchCreateFromSalesOrder.autoCreatePurchOrder</span><span class="sxs-lookup"><span data-stu-id="36c9b-351">PurchCreateFromSalesOrder.autoCreatePurchOrder</span></span>|
|<span data-ttu-id="36c9b-352">PurchFormletter_Invoice.newinvoice</span><span class="sxs-lookup"><span data-stu-id="36c9b-352">PurchFormletter_Invoice.newinvoice</span></span>|
|<span data-ttu-id="36c9b-353">PurchFormletter_Packingslip.runProjectPostings</span><span class="sxs-lookup"><span data-stu-id="36c9b-353">PurchFormletter_Packingslip.runProjectPostings</span></span>|
|<span data-ttu-id="36c9b-354">PurchFormletterParmData.createParmLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-354">PurchFormletterParmData.createParmLine</span></span>|
|<span data-ttu-id="36c9b-355">PurchFormletterParmData.newData</span><span class="sxs-lookup"><span data-stu-id="36c9b-355">PurchFormletterParmData.newData</span></span>|
|<span data-ttu-id="36c9b-356">PurchFormLetterParmData.reSelectLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-356">PurchFormLetterParmData.reSelectLines</span></span>|
|<span data-ttu-id="36c9b-357">PurchFormletterParmDataInvoice.chooseLinesNext</span><span class="sxs-lookup"><span data-stu-id="36c9b-357">PurchFormletterParmDataInvoice.chooseLinesNext</span></span>|
|<span data-ttu-id="36c9b-358">PurchFormletterParmDataInvoice.cleanupChooseLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-358">PurchFormletterParmDataInvoice.cleanupChooseLines</span></span>|
|<span data-ttu-id="36c9b-359">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span><span class="sxs-lookup"><span data-stu-id="36c9b-359">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span></span>|
|<span data-ttu-id="36c9b-360">PurchFormletterParmDataInvoice.processAdditional</span><span class="sxs-lookup"><span data-stu-id="36c9b-360">PurchFormletterParmDataInvoice.processAdditional</span></span>|
|<span data-ttu-id="36c9b-361">PurchFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-361">PurchFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="36c9b-362">PurchInvoiceJournalCreate.checkInvoice</span><span class="sxs-lookup"><span data-stu-id="36c9b-362">PurchInvoiceJournalCreate.checkInvoice</span></span>|
|<span data-ttu-id="36c9b-363">PurchInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="36c9b-363">PurchInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="36c9b-364">PurchLine.delete</span><span class="sxs-lookup"><span data-stu-id="36c9b-364">PurchLine.delete</span></span>|
|<span data-ttu-id="36c9b-365">PurchLine.setProjSalesPrice</span><span class="sxs-lookup"><span data-stu-id="36c9b-365">PurchLine.setProjSalesPrice</span></span>|
|<span data-ttu-id="36c9b-366">PurchLine.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-366">PurchLine.update</span></span>|
|<span data-ttu-id="36c9b-367">PurchLine.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="36c9b-367">PurchLine.validateWrite_Server</span></span>|
|<span data-ttu-id="36c9b-368">PurchLineCopy.canClose</span><span class="sxs-lookup"><span data-stu-id="36c9b-368">PurchLineCopy.canClose</span></span>|
|<span data-ttu-id="36c9b-369">PurchLineType.syncSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-369">PurchLineType.syncSalesLine</span></span>|
|<span data-ttu-id="36c9b-370">PurchLineType.updateInventory</span><span class="sxs-lookup"><span data-stu-id="36c9b-370">PurchLineType.updateInventory</span></span>|
|<span data-ttu-id="36c9b-371">PurchLineType.updatePurchStatus</span><span class="sxs-lookup"><span data-stu-id="36c9b-371">PurchLineType.updatePurchStatus</span></span>|
|<span data-ttu-id="36c9b-372">PurchLineType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="36c9b-372">PurchLineType.validateDelete</span></span>|
|<span data-ttu-id="36c9b-373">PurchPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="36c9b-373">PurchPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="36c9b-374">PurchPackingSlipJournalPost.updateSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-374">PurchPackingSlipJournalPost.updateSalesLine</span></span>|
|<span data-ttu-id="36c9b-375">PurchPackingSlipJournalPost.updateSalesTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-375">PurchPackingSlipJournalPost.updateSalesTable</span></span>|
|<span data-ttu-id="36c9b-376">PurchPackingSlipJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-376">PurchPackingSlipJournalPost.updateSourceLine</span></span>|
|<span data-ttu-id="36c9b-377">PurchQuantity_PackingSlip.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="36c9b-377">PurchQuantity_PackingSlip.calcQtyInvent</span></span>|
|<span data-ttu-id="36c9b-378">PurchQuantity_PackingSlip.calcQtyPurch</span><span class="sxs-lookup"><span data-stu-id="36c9b-378">PurchQuantity_PackingSlip.calcQtyPurch</span></span>|
|<span data-ttu-id="36c9b-379">PurchReqAddItems.init</span><span class="sxs-lookup"><span data-stu-id="36c9b-379">PurchReqAddItems.init</span></span>|
|<span data-ttu-id="36c9b-380">PurchReqTable.init</span><span class="sxs-lookup"><span data-stu-id="36c9b-380">PurchReqTable.init</span></span>|
|<span data-ttu-id="36c9b-381">PurchReqWFExpendiParticipantProvider.resolve</span><span class="sxs-lookup"><span data-stu-id="36c9b-381">PurchReqWFExpendiParticipantProvider.resolve</span></span>|
|<span data-ttu-id="36c9b-382">PurchSelectLinesManager.mark</span><span class="sxs-lookup"><span data-stu-id="36c9b-382">PurchSelectLinesManager.mark</span></span>|
|<span data-ttu-id="36c9b-383">PurchTableForm.purchLine_WritePreSuper</span><span class="sxs-lookup"><span data-stu-id="36c9b-383">PurchTableForm.purchLine_WritePreSuper</span></span>|
|<span data-ttu-id="36c9b-384">PurchTableInteractionHelper.getDeliveryScheduleEnabled</span><span class="sxs-lookup"><span data-stu-id="36c9b-384">PurchTableInteractionHelper.getDeliveryScheduleEnabled</span></span>|
|<span data-ttu-id="36c9b-385">PurchTableInteractionHelper.getHasMultipleDeliveries</span><span class="sxs-lookup"><span data-stu-id="36c9b-385">PurchTableInteractionHelper.getHasMultipleDeliveries</span></span>|
|<span data-ttu-id="36c9b-386">PurchUpdateRemain.updateRemainPhysical</span><span class="sxs-lookup"><span data-stu-id="36c9b-386">PurchUpdateRemain.updateRemainPhysical</span></span>|
|<span data-ttu-id="36c9b-387">ReqCalc.insertItemInventSum</span><span class="sxs-lookup"><span data-stu-id="36c9b-387">ReqCalc.insertItemInventSum</span></span>|
|<span data-ttu-id="36c9b-388">ReqTransPlanIdFilter.setPlanIdOnQueryRange</span><span class="sxs-lookup"><span data-stu-id="36c9b-388">ReqTransPlanIdFilter.setPlanIdOnQueryRange</span></span>|
|<span data-ttu-id="36c9b-389">ReqTransPoMarkFirm.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-389">ReqTransPoMarkFirm.createPurchLine</span></span>|
|<span data-ttu-id="36c9b-390">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-390">ReqTransPoMarkFirm.createPurchTable</span></span>|
|<span data-ttu-id="36c9b-391">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-391">ReqTransPoMarkFirm.createPurchTable</span></span>|
|<span data-ttu-id="36c9b-392">ReqTransPoMarkFirm.dialog</span><span class="sxs-lookup"><span data-stu-id="36c9b-392">ReqTransPoMarkFirm.dialog</span></span>|
|<span data-ttu-id="36c9b-393">RetailAssortmentLookupTask.CreateChannelGroups</span><span class="sxs-lookup"><span data-stu-id="36c9b-393">RetailAssortmentLookupTask.CreateChannelGroups</span></span>|
|<span data-ttu-id="36c9b-394">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span><span class="sxs-lookup"><span data-stu-id="36c9b-394">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span></span>|
|<span data-ttu-id="36c9b-395">RetailPackage.close</span><span class="sxs-lookup"><span data-stu-id="36c9b-395">RetailPackage.close</span></span>|
|<span data-ttu-id="36c9b-396">RetailProductPropertyManager.saveProductDimensions</span><span class="sxs-lookup"><span data-stu-id="36c9b-396">RetailProductPropertyManager.saveProductDimensions</span></span>|
|<span data-ttu-id="36c9b-397">RetailStatementPostChecker::checkStatement</span><span class="sxs-lookup"><span data-stu-id="36c9b-397">RetailStatementPostChecker::checkStatement</span></span>|
|<span data-ttu-id="36c9b-398">ReturnTable.isDispositionCodeValid</span><span class="sxs-lookup"><span data-stu-id="36c9b-398">ReturnTable.isDispositionCodeValid</span></span>|
|<span data-ttu-id="36c9b-399">RouteCopyToRoute</span><span class="sxs-lookup"><span data-stu-id="36c9b-399">RouteCopyToRoute</span></span>|
|<span data-ttu-id="36c9b-400">SalesCalcAvailableDlvDates.newCommonSalesDlvDateType</span><span class="sxs-lookup"><span data-stu-id="36c9b-400">SalesCalcAvailableDlvDates.newCommonSalesDlvDateType</span></span>|
|<span data-ttu-id="36c9b-401">SalesCalcAvailableDlvDates.newCommonSalesDlvDateTypeByEntity</span><span class="sxs-lookup"><span data-stu-id="36c9b-401">SalesCalcAvailableDlvDates.newCommonSalesDlvDateTypeByEntity</span></span>|
|<span data-ttu-id="36c9b-402">SalesCopying.copyLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-402">SalesCopying.copyLines</span></span>|
|<span data-ttu-id="36c9b-403">SalesEditLines.FormDesign/FormMenuFunctionButtonControl/ButtonPaymentSched/Method/clicked</span><span class="sxs-lookup"><span data-stu-id="36c9b-403">SalesEditLines.FormDesign/FormMenuFunctionButtonControl/ButtonPaymentSched/Method/clicked</span></span>|
|<span data-ttu-id="36c9b-404">SalesFormLetter.onCreatePaymSched</span><span class="sxs-lookup"><span data-stu-id="36c9b-404">SalesFormLetter.onCreatePaymSched</span></span>|
|<span data-ttu-id="36c9b-405">SalesFormLetterParmDataPackingSlip.selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-405">SalesFormLetterParmDataPackingSlip.selectChooseLines</span></span>|
|<span data-ttu-id="36c9b-406">SalesFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-406">SalesFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="36c9b-407">SalesFormletterProvider.checkSalesLineChanged</span><span class="sxs-lookup"><span data-stu-id="36c9b-407">SalesFormletterProvider.checkSalesLineChanged</span></span>|
|<span data-ttu-id="36c9b-408">SalesInvoiceController.initFormLetterReport</span><span class="sxs-lookup"><span data-stu-id="36c9b-408">SalesInvoiceController.initFormLetterReport</span></span>|
|<span data-ttu-id="36c9b-409">SalesInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="36c9b-409">SalesInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="36c9b-410">SalesInvoiceJournalPostProj.updateInventory</span><span class="sxs-lookup"><span data-stu-id="36c9b-410">SalesInvoiceJournalPostProj.updateInventory</span></span>|
|<span data-ttu-id="36c9b-411">SalesLine.createAlternativeItem</span><span class="sxs-lookup"><span data-stu-id="36c9b-411">SalesLine.createAlternativeItem</span></span>|
|<span data-ttu-id="36c9b-412">SalesLine.delete</span><span class="sxs-lookup"><span data-stu-id="36c9b-412">SalesLine.delete</span></span>|
|<span data-ttu-id="36c9b-413">SalesLine.returnLineUpdate</span><span class="sxs-lookup"><span data-stu-id="36c9b-413">SalesLine.returnLineUpdate</span></span>|
|<span data-ttu-id="36c9b-414">SalesLineCopy.canClose</span><span class="sxs-lookup"><span data-stu-id="36c9b-414">SalesLineCopy.canClose</span></span>|
|<span data-ttu-id="36c9b-415">SalesLineType.initFromCustInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="36c9b-415">SalesLineType.initFromCustInvoiceTrans</span></span>|
|<span data-ttu-id="36c9b-416">SalesOrderEntryStatistics.createOrderEntry</span><span class="sxs-lookup"><span data-stu-id="36c9b-416">SalesOrderEntryStatistics.createOrderEntry</span></span>|
|<span data-ttu-id="36c9b-417">SalesOrderEntryStatistics.deleteOrderEntry</span><span class="sxs-lookup"><span data-stu-id="36c9b-417">SalesOrderEntryStatistics.deleteOrderEntry</span></span>|
|<span data-ttu-id="36c9b-418">SalesPackingSlipDP.itemId</span><span class="sxs-lookup"><span data-stu-id="36c9b-418">SalesPackingSlipDP.itemId</span></span>|
|<span data-ttu-id="36c9b-419">SalesPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="36c9b-419">SalesPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="36c9b-420">SalesParmLine.setQty</span><span class="sxs-lookup"><span data-stu-id="36c9b-420">SalesParmLine.setQty</span></span>|
|<span data-ttu-id="36c9b-421">SalesQuantity_Invoice.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="36c9b-421">SalesQuantity_Invoice.calcQtyInvent</span></span>|
|<span data-ttu-id="36c9b-422">SalesQuantity_Invoice.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="36c9b-422">SalesQuantity_Invoice.calcQtySales</span></span>|
|<span data-ttu-id="36c9b-423">SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-423">SalesQuotationEditLinesForm_Sales_Confir method createSalesLines</span></span>|
|<span data-ttu-id="36c9b-424">SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-424">SalesQuotationEditLinesForm_Sales_Confir method createSalesTable</span></span>|
|<span data-ttu-id="36c9b-425">SalesQuotationEditLinesForm_Sales_Confir.createSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-425">SalesQuotationEditLinesForm_Sales_Confir.createSalesLine</span></span>|
|<span data-ttu-id="36c9b-426">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span><span class="sxs-lookup"><span data-stu-id="36c9b-426">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span></span>|
|<span data-ttu-id="36c9b-427">SalesQuotationLine.createLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-427">SalesQuotationLine.createLine</span></span>|
|<span data-ttu-id="36c9b-428">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-428">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="36c9b-429">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-429">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="36c9b-430">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="36c9b-430">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="36c9b-431">SalesQuotationLine.delete</span><span class="sxs-lookup"><span data-stu-id="36c9b-431">SalesQuotationLine.delete</span></span>|
|<span data-ttu-id="36c9b-432">SalesQuotationLine.setCostSalesPrice</span><span class="sxs-lookup"><span data-stu-id="36c9b-432">SalesQuotationLine.setCostSalesPrice</span></span>|
|<span data-ttu-id="36c9b-433">SalesQuotationLine.updateSalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-433">SalesQuotationLine.updateSalesQuotationTable</span></span>|
|<span data-ttu-id="36c9b-434">SalesQuotationListPageInteraction.initIsSalesQuotation</span><span class="sxs-lookup"><span data-stu-id="36c9b-434">SalesQuotationListPageInteraction.initIsSalesQuotation</span></span>|
|<span data-ttu-id="36c9b-435">SalesQuotationListPageInteraction.setButtonFollowup</span><span class="sxs-lookup"><span data-stu-id="36c9b-435">SalesQuotationListPageInteraction.setButtonFollowup</span></span>|
|<span data-ttu-id="36c9b-436">SalesQuotationListPageInteraction.setButtonQuotation</span><span class="sxs-lookup"><span data-stu-id="36c9b-436">SalesQuotationListPageInteraction.setButtonQuotation</span></span>|
|<span data-ttu-id="36c9b-437">SalesQuotationTableForm_DlvSchedule.updateSalesQuotationLineTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-437">SalesQuotationTableForm_DlvSchedule.updateSalesQuotationLineTable</span></span>|
|<span data-ttu-id="36c9b-438">SalesQuotationTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="36c9b-438">SalesQuotationTableType.validateDelete</span></span>|
|<span data-ttu-id="36c9b-439">SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-439">SalesTable.update</span></span>|
|<span data-ttu-id="36c9b-440">SalesTableForm_DeliverySchedule.updateSalesLineTable</span><span class="sxs-lookup"><span data-stu-id="36c9b-440">SalesTableForm_DeliverySchedule.updateSalesLineTable</span></span>|
|<span data-ttu-id="36c9b-441">SalesTableForm_ProjectSalesItem.resetSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-441">SalesTableForm_ProjectSalesItem.resetSalesLine</span></span>|
|<span data-ttu-id="36c9b-442">SalesTableInteractionHelper.isOpenOrderNotReturnNotProjectRelatedSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-442">SalesTableInteractionHelper.isOpenOrderNotReturnNotProjectRelatedSalesLine</span></span>|
|<span data-ttu-id="36c9b-443">SalesTableInteractionHelper.notPartiallyPickedPackedOrInvoiced</span><span class="sxs-lookup"><span data-stu-id="36c9b-443">SalesTableInteractionHelper.notPartiallyPickedPackedOrInvoiced</span></span>|
|<span data-ttu-id="36c9b-444">SalesTableInteractionHelper.notReservedOrderedNorPhysical</span><span class="sxs-lookup"><span data-stu-id="36c9b-444">SalesTableInteractionHelper.notReservedOrderedNorPhysical</span></span>|
|<span data-ttu-id="36c9b-445">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="36c9b-445">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="36c9b-446">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="36c9b-446">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="36c9b-447">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="36c9b-447">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="36c9b-448">SalesTaxDeclarationInformationReportService.processReport</span><span class="sxs-lookup"><span data-stu-id="36c9b-448">SalesTaxDeclarationInformationReportService.processReport</span></span>|
|<span data-ttu-id="36c9b-449">SettlementPair_Vend.fetchPayment</span><span class="sxs-lookup"><span data-stu-id="36c9b-449">SettlementPair_Vend.fetchPayment</span></span>|
|<span data-ttu-id="36c9b-450">smmActivityParentLinkTable.insert</span><span class="sxs-lookup"><span data-stu-id="36c9b-450">smmActivityParentLinkTable.insert</span></span>|
|<span data-ttu-id="36c9b-451">smmBusRelTable.convert2Customer</span><span class="sxs-lookup"><span data-stu-id="36c9b-451">smmBusRelTable.convert2Customer</span></span>|
|<span data-ttu-id="36c9b-452">smmBusRelTable.convert2Customer</span><span class="sxs-lookup"><span data-stu-id="36c9b-452">smmBusRelTable.convert2Customer</span></span>|
|<span data-ttu-id="36c9b-453">SmmBusRelTable.convert2Vendor</span><span class="sxs-lookup"><span data-stu-id="36c9b-453">SmmBusRelTable.convert2Vendor</span></span>|
|<span data-ttu-id="36c9b-454">SmmBusRelTable.convert2Vendor</span><span class="sxs-lookup"><span data-stu-id="36c9b-454">SmmBusRelTable.convert2Vendor</span></span>|
|<span data-ttu-id="36c9b-455">smmBusRelTable.createConvertedBusRel</span><span class="sxs-lookup"><span data-stu-id="36c9b-455">smmBusRelTable.createConvertedBusRel</span></span>|
|<span data-ttu-id="36c9b-456">smmLeadTable.createBusRelRecord</span><span class="sxs-lookup"><span data-stu-id="36c9b-456">smmLeadTable.createBusRelRecord</span></span>|
|<span data-ttu-id="36c9b-457">SmmProjectCreate.createProjectGroup</span><span class="sxs-lookup"><span data-stu-id="36c9b-457">SmmProjectCreate.createProjectGroup</span></span>|
|<span data-ttu-id="36c9b-458">SpecTransInsertSetManager.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="36c9b-458">SpecTransInsertSetManager.insertDatabase</span></span>|
|<span data-ttu-id="36c9b-459">SubledgerJournalizerProjectExtension.createProjectActualCostDetail、createProjectActualHeader</span><span class="sxs-lookup"><span data-stu-id="36c9b-459">SubledgerJournalizerProjectExtension.createProjectActualCostDetail, createProjectActualHeader</span></span>|
|<span data-ttu-id="36c9b-460">SubledgerJournalizerProjectExtension.getProjectActualMap</span><span class="sxs-lookup"><span data-stu-id="36c9b-460">SubledgerJournalizerProjectExtension.getProjectActualMap</span></span>|
|<span data-ttu-id="36c9b-461">SuppItemSales.initSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-461">SuppItemSales.initSalesLine</span></span>|
|<span data-ttu-id="36c9b-462">テーブル PurchLine.insert</span><span class="sxs-lookup"><span data-stu-id="36c9b-462">Table PurchLine.insert</span></span>|
|<span data-ttu-id="36c9b-463">テーブル PurchLine.insert</span><span class="sxs-lookup"><span data-stu-id="36c9b-463">Table PurchLine.insert</span></span>|
|<span data-ttu-id="36c9b-464">テーブル PurchLine.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-464">Table PurchLine.update</span></span>|
|<span data-ttu-id="36c9b-465">テーブル PurchTable.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-465">Table PurchTable.update</span></span>|
|<span data-ttu-id="36c9b-466">テーブル PurchTable.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-466">Table PurchTable.update</span></span>|
|<span data-ttu-id="36c9b-467">テーブル SalesLine.insert</span><span class="sxs-lookup"><span data-stu-id="36c9b-467">Table SalesLine.insert</span></span>|
|<span data-ttu-id="36c9b-468">テーブル SalesLine.projIdModified</span><span class="sxs-lookup"><span data-stu-id="36c9b-468">table SalesLine.projIdModified</span></span>|
|<span data-ttu-id="36c9b-469">テーブル SalesLine.salesQtyModifiedInteraction</span><span class="sxs-lookup"><span data-stu-id="36c9b-469">table SalesLine.salesQtyModifiedInteraction</span></span>|
|<span data-ttu-id="36c9b-470">テーブル SalesLine.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-470">Table SalesLine.update</span></span>|
|<span data-ttu-id="36c9b-471">テーブル SalesQuotationLine.insert</span><span class="sxs-lookup"><span data-stu-id="36c9b-471">Table SalesQuotationLine.insert</span></span>|
|<span data-ttu-id="36c9b-472">テーブル SalesQuotationLine.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-472">Table SalesQuotationLine.update</span></span>|
|<span data-ttu-id="36c9b-473">テーブル SalesQuotationTable.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-473">Table SalesQuotationTable.update</span></span>|
|<span data-ttu-id="36c9b-474">テーブル SalesQuotationTable.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-474">Table SalesQuotationTable.update</span></span>|
|<span data-ttu-id="36c9b-475">テーブル SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-475">Table SalesTable.update</span></span>|
|<span data-ttu-id="36c9b-476">テーブル SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="36c9b-476">Table SalesTable.update</span></span>|
|<span data-ttu-id="36c9b-477">Table\VendTable.name</span><span class="sxs-lookup"><span data-stu-id="36c9b-477">Table\VendTable.name</span></span>|
|<span data-ttu-id="36c9b-478">Table\VendTable.updateOnHold</span><span class="sxs-lookup"><span data-stu-id="36c9b-478">Table\VendTable.updateOnHold</span></span>|
|<span data-ttu-id="36c9b-479">Tax.createOrphanLinkInsteadPost_RU</span><span class="sxs-lookup"><span data-stu-id="36c9b-479">Tax.createOrphanLinkInsteadPost_RU</span></span>|
|<span data-ttu-id="36c9b-480">Tax.distributeTotalTax</span><span class="sxs-lookup"><span data-stu-id="36c9b-480">Tax.distributeTotalTax</span></span>|
|<span data-ttu-id="36c9b-481">Tax.distributeTotalTax</span><span class="sxs-lookup"><span data-stu-id="36c9b-481">Tax.distributeTotalTax</span></span>|
|<span data-ttu-id="36c9b-482">Tax.InsertIntersection</span><span class="sxs-lookup"><span data-stu-id="36c9b-482">Tax.InsertIntersection</span></span>|
|<span data-ttu-id="36c9b-483">Tax.insertIntersection</span><span class="sxs-lookup"><span data-stu-id="36c9b-483">Tax.insertIntersection</span></span>|
|<span data-ttu-id="36c9b-484">Tax.post</span><span class="sxs-lookup"><span data-stu-id="36c9b-484">Tax.post</span></span>|
|<span data-ttu-id="36c9b-485">Tax.Post</span><span class="sxs-lookup"><span data-stu-id="36c9b-485">Tax.Post</span></span>|
|<span data-ttu-id="36c9b-486">Tax.postCharge</span><span class="sxs-lookup"><span data-stu-id="36c9b-486">Tax.postCharge</span></span>|
|<span data-ttu-id="36c9b-487">Tax.postTaxProjInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="36c9b-487">Tax.postTaxProjInvoice_IN</span></span>|
|<span data-ttu-id="36c9b-488">Tax.postTaxPurchInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="36c9b-488">Tax.postTaxPurchInvoice_IN</span></span>|
|<span data-ttu-id="36c9b-489">Tax.postTaxSalesInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="36c9b-489">Tax.postTaxSalesInvoice_IN</span></span>|
|<span data-ttu-id="36c9b-490">Tax.saveAndPost</span><span class="sxs-lookup"><span data-stu-id="36c9b-490">Tax.saveAndPost</span></span>|
|<span data-ttu-id="36c9b-491">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="36c9b-491">Tax.taxTotals</span></span>|
|<span data-ttu-id="36c9b-492">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="36c9b-492">Tax.taxTotals</span></span>|
|<span data-ttu-id="36c9b-493">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="36c9b-493">Tax.taxTotals</span></span>|
|<span data-ttu-id="36c9b-494">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="36c9b-494">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="36c9b-495">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="36c9b-495">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="36c9b-496">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="36c9b-496">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="36c9b-497">TaxBookSection.checkTaxBookSection</span><span class="sxs-lookup"><span data-stu-id="36c9b-497">TaxBookSection.checkTaxBookSection</span></span>|
|<span data-ttu-id="36c9b-498">TaxCalculationAdjustment.calcManualInserted</span><span class="sxs-lookup"><span data-stu-id="36c9b-498">TaxCalculationAdjustment.calcManualInserted</span></span>|
|<span data-ttu-id="36c9b-499">TaxCalculationJournal.saveTaxTransfers</span><span class="sxs-lookup"><span data-stu-id="36c9b-499">TaxCalculationJournal.saveTaxTransfers</span></span>|
|<span data-ttu-id="36c9b-500">TaxFreeInvoice_Invoice.updateAndPost</span><span class="sxs-lookup"><span data-stu-id="36c9b-500">TaxFreeInvoice_Invoice.updateAndPost</span></span>|
|<span data-ttu-id="36c9b-501">TaxInvoiceSpec.parmTaxSpec</span><span class="sxs-lookup"><span data-stu-id="36c9b-501">TaxInvoiceSpec.parmTaxSpec</span></span>|
|<span data-ttu-id="36c9b-502">TaxListDP.insertTaxListTaxTmpData</span><span class="sxs-lookup"><span data-stu-id="36c9b-502">TaxListDP.insertTaxListTaxTmpData</span></span>|
|<span data-ttu-id="36c9b-503">TaxListDP.updateTaxListTaxTmpData</span><span class="sxs-lookup"><span data-stu-id="36c9b-503">TaxListDP.updateTaxListTaxTmpData</span></span>|
|<span data-ttu-id="36c9b-504">TaxMainAccDimensionListProvider.populateMainAccountDimensionList</span><span class="sxs-lookup"><span data-stu-id="36c9b-504">TaxMainAccDimensionListProvider.populateMainAccountDimensionList</span></span>|
|<span data-ttu-id="36c9b-505">TaxPost.postToLedger</span><span class="sxs-lookup"><span data-stu-id="36c9b-505">TaxPost.postToLedger</span></span>|
|<span data-ttu-id="36c9b-506">TaxReportController_US.init</span><span class="sxs-lookup"><span data-stu-id="36c9b-506">TaxReportController_US.init</span></span>|
|<span data-ttu-id="36c9b-507">TaxReportInclAdjustmentDP.insertTaxReportInclAdjustmentTmp</span><span class="sxs-lookup"><span data-stu-id="36c9b-507">TaxReportInclAdjustmentDP.insertTaxReportInclAdjustmentTmp</span></span>|
|<span data-ttu-id="36c9b-508">TaxReportingDP.insertTaxReportingTmp</span><span class="sxs-lookup"><span data-stu-id="36c9b-508">TaxReportingDP.insertTaxReportingTmp</span></span>|
|<span data-ttu-id="36c9b-509">TaxReverse.adjustTaxTransDueToExchangeRateGainLoss</span><span class="sxs-lookup"><span data-stu-id="36c9b-509">TaxReverse.adjustTaxTransDueToExchangeRateGainLoss</span></span>|
|<span data-ttu-id="36c9b-510">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="36c9b-510">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="36c9b-511">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="36c9b-511">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="36c9b-512">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="36c9b-512">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="36c9b-513">TaxReverse.postCharge</span><span class="sxs-lookup"><span data-stu-id="36c9b-513">TaxReverse.postCharge</span></span>|
|<span data-ttu-id="36c9b-514">TaxReverse.postGainLossInReportingCurrency</span><span class="sxs-lookup"><span data-stu-id="36c9b-514">TaxReverse.postGainLossInReportingCurrency</span></span>|
|<span data-ttu-id="36c9b-515">TaxSales.calc</span><span class="sxs-lookup"><span data-stu-id="36c9b-515">TaxSales.calc</span></span>|
|<span data-ttu-id="36c9b-516">TaxSales.calc</span><span class="sxs-lookup"><span data-stu-id="36c9b-516">TaxSales.calc</span></span>|
|<span data-ttu-id="36c9b-517">TaxSales.calcMarkup</span><span class="sxs-lookup"><span data-stu-id="36c9b-517">TaxSales.calcMarkup</span></span>|
|<span data-ttu-id="36c9b-518">TaxSales.configureTaxForSalesLine</span><span class="sxs-lookup"><span data-stu-id="36c9b-518">TaxSales.configureTaxForSalesLine</span></span>|
|<span data-ttu-id="36c9b-519">TaxVoucherService.taxAmountForLedgerType</span><span class="sxs-lookup"><span data-stu-id="36c9b-519">TaxVoucherService.taxAmountForLedgerType</span></span>|
|<span data-ttu-id="36c9b-520">TmpCustVendTrans.CustTransBalanceCurrency</span><span class="sxs-lookup"><span data-stu-id="36c9b-520">TmpCustVendTrans.CustTransBalanceCurrency</span></span>|
|<span data-ttu-id="36c9b-521">TmpProjAdjustment.adjustmentType2JournalType</span><span class="sxs-lookup"><span data-stu-id="36c9b-521">TmpProjAdjustment.adjustmentType2JournalType</span></span>|
|<span data-ttu-id="36c9b-522">TmpProjAdjustment.adjustmentType2TransType</span><span class="sxs-lookup"><span data-stu-id="36c9b-522">TmpProjAdjustment.adjustmentType2TransType</span></span>|
|<span data-ttu-id="36c9b-523">TmpProjAdjustment.updateFundingLimits</span><span class="sxs-lookup"><span data-stu-id="36c9b-523">TmpProjAdjustment.updateFundingLimits</span></span>|
|<span data-ttu-id="36c9b-524">TmpProjAdjustmentCreate.salesPrice</span><span class="sxs-lookup"><span data-stu-id="36c9b-524">TmpProjAdjustmentCreate.salesPrice</span></span>|
|<span data-ttu-id="36c9b-525">TrvExpenseLinesVisibilityController.isVisibilityResetRequired</span><span class="sxs-lookup"><span data-stu-id="36c9b-525">TrvExpenseLinesVisibilityController.isVisibilityResetRequired</span></span>|
|<span data-ttu-id="36c9b-526">TrvExpenses.updateFormVisibilityOnCategoryChange</span><span class="sxs-lookup"><span data-stu-id="36c9b-526">TrvExpenses.updateFormVisibilityOnCategoryChange</span></span>|
|<span data-ttu-id="36c9b-527">TrvExpTrans.calcTaxAmount</span><span class="sxs-lookup"><span data-stu-id="36c9b-527">TrvExpTrans.calcTaxAmount</span></span>|
|<span data-ttu-id="36c9b-528">TrvTaxExpense.calculateTax</span><span class="sxs-lookup"><span data-stu-id="36c9b-528">TrvTaxExpense.calculateTax</span></span>|
|<span data-ttu-id="36c9b-529">TSTimesheetEntry.init、initFields、setHeaderObjects、validateWrit、lookup</span><span class="sxs-lookup"><span data-stu-id="36c9b-529">TSTimesheetEntry.init, initFields, setHeaderObjects, validateWrit, lookup</span></span>|
|<span data-ttu-id="36c9b-530">UnitOfMeasureConverter.Convert</span><span class="sxs-lookup"><span data-stu-id="36c9b-530">UnitOfMeasureConverter.Convert</span></span>|
|<span data-ttu-id="36c9b-531">VendInvoicePaymentAuthorizationTask.postSavedInvoice</span><span class="sxs-lookup"><span data-stu-id="36c9b-531">VendInvoicePaymentAuthorizationTask.postSavedInvoice</span></span>|
|<span data-ttu-id="36c9b-532">VendPackingSlipTrans.unpostedInvoicePurchQtyServer および VendPackingSlipTrans.unpostedInvoiceInventQtyServer</span><span class="sxs-lookup"><span data-stu-id="36c9b-532">VendPackingSlipTrans.unpostedInvoicePurchQtyServer and VendPackingSlipTrans.unpostedInvoiceInventQtyServer</span></span>|
|<span data-ttu-id="36c9b-533">VendTable.checkVATNumUsed</span><span class="sxs-lookup"><span data-stu-id="36c9b-533">VendTable.checkVATNumUsed</span></span>|
|<span data-ttu-id="36c9b-534">VendTax1099Update.calcMiscChargeAmountTax</span><span class="sxs-lookup"><span data-stu-id="36c9b-534">VendTax1099Update.calcMiscChargeAmountTax</span></span>|
|<span data-ttu-id="36c9b-535">VendTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="36c9b-535">VendTrans.documentDateModified</span></span>|
|<span data-ttu-id="36c9b-536">VendTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="36c9b-536">VendTrans.documentDateModified</span></span>|
|<span data-ttu-id="36c9b-537">VendVoucher.createTransOpen</span><span class="sxs-lookup"><span data-stu-id="36c9b-537">VendVoucher.createTransOpen</span></span>|
|<span data-ttu-id="36c9b-538">VendVoucher.createTransOpen</span><span class="sxs-lookup"><span data-stu-id="36c9b-538">VendVoucher.createTransOpen</span></span>|
|<span data-ttu-id="36c9b-539">WHSContainerTable.closeContainer</span><span class="sxs-lookup"><span data-stu-id="36c9b-539">WHSContainerTable.closeContainer</span></span>|
|<span data-ttu-id="36c9b-540">WHSDocumentRouting.translate</span><span class="sxs-lookup"><span data-stu-id="36c9b-540">WHSDocumentRouting.translate</span></span>|
|<span data-ttu-id="36c9b-541">WHSLoadLine.orderHeader</span><span class="sxs-lookup"><span data-stu-id="36c9b-541">WHSLoadLine.orderHeader</span></span>|
|<span data-ttu-id="36c9b-542">WHSLoadTable.validateInventTransTypeMatches</span><span class="sxs-lookup"><span data-stu-id="36c9b-542">WHSLoadTable.validateInventTransTypeMatches</span></span>|
|<span data-ttu-id="36c9b-543">WHSLoadTableAssignOriginInfo.classDeclaration</span><span class="sxs-lookup"><span data-stu-id="36c9b-543">WHSLoadTableAssignOriginInfo.classDeclaration</span></span>|
|<span data-ttu-id="36c9b-544">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="36c9b-544">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="36c9b-545">WMSOrderTrans.split</span><span class="sxs-lookup"><span data-stu-id="36c9b-545">WMSOrderTrans.split</span></span>|
|<span data-ttu-id="36c9b-546">WmsOrderTransType_Output.updateReservations</span><span class="sxs-lookup"><span data-stu-id="36c9b-546">WmsOrderTransType_Output.updateReservations</span></span>|
|<span data-ttu-id="36c9b-547">WorkflowHierarchyProviderHelperEventHandler::getPersonnelNumberIdBySysDictTypeDelegate</span><span class="sxs-lookup"><span data-stu-id="36c9b-547">WorkflowHierarchyProviderHelperEventHandler::getPersonnelNumberIdBySysDictTypeDelegate</span></span>|
|<span data-ttu-id="36c9b-548">WorkTimeTable.removeDisplayCache</span><span class="sxs-lookup"><span data-stu-id="36c9b-548">WorkTimeTable.removeDisplayCache</span></span>|
|<span data-ttu-id="36c9b-549">WrkCtrResourceAbilityMapController.insertData</span><span class="sxs-lookup"><span data-stu-id="36c9b-549">WrkCtrResourceAbilityMapController.insertData</span></span>|
|<span data-ttu-id="36c9b-550">数量の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="36c9b-550">Enable increase of decimal precision through extensiblity for quantities</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="36c9b-551">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="36c9b-551">Enumerations made extensible</span></span>

<span data-ttu-id="36c9b-552">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="36c9b-552">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="36c9b-553">列挙型</span><span class="sxs-lookup"><span data-stu-id="36c9b-553">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="36c9b-554">AssetPostValue</span><span class="sxs-lookup"><span data-stu-id="36c9b-554">AssetPostValue</span></span>|
|<span data-ttu-id="36c9b-555">AssetPropertyType</span><span class="sxs-lookup"><span data-stu-id="36c9b-555">AssetPropertyType</span></span>|
|<span data-ttu-id="36c9b-556">AssetStatus</span><span class="sxs-lookup"><span data-stu-id="36c9b-556">AssetStatus</span></span>|
|<span data-ttu-id="36c9b-557">CaseStatus</span><span class="sxs-lookup"><span data-stu-id="36c9b-557">CaseStatus</span></span>|
|<span data-ttu-id="36c9b-558">CommissionSalesRepCode</span><span class="sxs-lookup"><span data-stu-id="36c9b-558">CommissionSalesRepCode</span></span>|
|<span data-ttu-id="36c9b-559">DirSubNameSequenceType</span><span class="sxs-lookup"><span data-stu-id="36c9b-559">DirSubNameSequenceType</span></span>|
|<span data-ttu-id="36c9b-560">FreightSlipType</span><span class="sxs-lookup"><span data-stu-id="36c9b-560">FreightSlipType</span></span>|
|<span data-ttu-id="36c9b-561">HRPLimitDocumentType</span><span class="sxs-lookup"><span data-stu-id="36c9b-561">HRPLimitDocumentType</span></span>|
|<span data-ttu-id="36c9b-562">IntrastatPaymentMethod_IT</span><span class="sxs-lookup"><span data-stu-id="36c9b-562">IntrastatPaymentMethod_IT</span></span>|
|<span data-ttu-id="36c9b-563">InventBlockingType</span><span class="sxs-lookup"><span data-stu-id="36c9b-563">InventBlockingType</span></span>|
|<span data-ttu-id="36c9b-564">JmgPaySpecTypeEnumPick</span><span class="sxs-lookup"><span data-stu-id="36c9b-564">JmgPaySpecTypeEnumPick</span></span>|
|<span data-ttu-id="36c9b-565">KMQuestionAnswerInputType</span><span class="sxs-lookup"><span data-stu-id="36c9b-565">KMQuestionAnswerInputType</span></span>|
|<span data-ttu-id="36c9b-566">LedgerJournalType</span><span class="sxs-lookup"><span data-stu-id="36c9b-566">LedgerJournalType</span></span>|
|<span data-ttu-id="36c9b-567">LogisticsAddrZipCodeImportCountryRegion</span><span class="sxs-lookup"><span data-stu-id="36c9b-567">LogisticsAddrZipCodeImportCountryRegion</span></span>|
|<span data-ttu-id="36c9b-568">LogType</span><span class="sxs-lookup"><span data-stu-id="36c9b-568">LogType</span></span>|
|<span data-ttu-id="36c9b-569">MarkupModuleType</span><span class="sxs-lookup"><span data-stu-id="36c9b-569">MarkupModuleType</span></span>|
|<span data-ttu-id="36c9b-570">MarkupModuleType</span><span class="sxs-lookup"><span data-stu-id="36c9b-570">MarkupModuleType</span></span>|
|<span data-ttu-id="36c9b-571">MCRBrokerValueType</span><span class="sxs-lookup"><span data-stu-id="36c9b-571">MCRBrokerValueType</span></span>|
|<span data-ttu-id="36c9b-572">PaymentType</span><span class="sxs-lookup"><span data-stu-id="36c9b-572">PaymentType</span></span>|
|<span data-ttu-id="36c9b-573">PDSCalcElementTypeBase</span><span class="sxs-lookup"><span data-stu-id="36c9b-573">PDSCalcElementTypeBase</span></span>|
|<span data-ttu-id="36c9b-574">PdsStatus</span><span class="sxs-lookup"><span data-stu-id="36c9b-574">PdsStatus</span></span>|
|<span data-ttu-id="36c9b-575">PdsVendorCheckItem</span><span class="sxs-lookup"><span data-stu-id="36c9b-575">PdsVendorCheckItem</span></span>|
|<span data-ttu-id="36c9b-576">ProdStatus</span><span class="sxs-lookup"><span data-stu-id="36c9b-576">ProdStatus</span></span>|
|<span data-ttu-id="36c9b-577">ProjActiveAll</span><span class="sxs-lookup"><span data-stu-id="36c9b-577">ProjActiveAll</span></span>|
|<span data-ttu-id="36c9b-578">ProjAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="36c9b-578">ProjAdjustmentType</span></span>|
|<span data-ttu-id="36c9b-579">ProjAllTrxType</span><span class="sxs-lookup"><span data-stu-id="36c9b-579">ProjAllTrxType</span></span>|
|<span data-ttu-id="36c9b-580">ProjBudgetAction</span><span class="sxs-lookup"><span data-stu-id="36c9b-580">ProjBudgetAction</span></span>|
|<span data-ttu-id="36c9b-581">ProjCostType</span><span class="sxs-lookup"><span data-stu-id="36c9b-581">ProjCostType</span></span>|
|<span data-ttu-id="36c9b-582">ProjForecastInvoiceFrequency</span><span class="sxs-lookup"><span data-stu-id="36c9b-582">ProjForecastInvoiceFrequency</span></span>|
|<span data-ttu-id="36c9b-583">ProjLinePropertySearch</span><span class="sxs-lookup"><span data-stu-id="36c9b-583">ProjLinePropertySearch</span></span>|
|<span data-ttu-id="36c9b-584">ProjSalesPriceMarkup</span><span class="sxs-lookup"><span data-stu-id="36c9b-584">ProjSalesPriceMarkup</span></span>|
|<span data-ttu-id="36c9b-585">ProjSortValue</span><span class="sxs-lookup"><span data-stu-id="36c9b-585">ProjSortValue</span></span>|
|<span data-ttu-id="36c9b-586">ProjTableEditSubProj</span><span class="sxs-lookup"><span data-stu-id="36c9b-586">ProjTableEditSubProj</span></span>|
|<span data-ttu-id="36c9b-587">ReqCovType</span><span class="sxs-lookup"><span data-stu-id="36c9b-587">ReqCovType</span></span>|
|<span data-ttu-id="36c9b-588">ResCharacteristicSetEnum</span><span class="sxs-lookup"><span data-stu-id="36c9b-588">ResCharacteristicSetEnum</span></span>|
|<span data-ttu-id="36c9b-589">SettlementType</span><span class="sxs-lookup"><span data-stu-id="36c9b-589">SettlementType</span></span>|
|<span data-ttu-id="36c9b-590">smmShowTimeAs</span><span class="sxs-lookup"><span data-stu-id="36c9b-590">smmShowTimeAs</span></span>|
|<span data-ttu-id="36c9b-591">SourceDocumentRelationType</span><span class="sxs-lookup"><span data-stu-id="36c9b-591">SourceDocumentRelationType</span></span>|
|<span data-ttu-id="36c9b-592">TaxRegistrationTypesList</span><span class="sxs-lookup"><span data-stu-id="36c9b-592">TaxRegistrationTypesList</span></span>|
|<span data-ttu-id="36c9b-593">TaxReportLayout</span><span class="sxs-lookup"><span data-stu-id="36c9b-593">TaxReportLayout</span></span>|
|<span data-ttu-id="36c9b-594">TradeWorkflowState</span><span class="sxs-lookup"><span data-stu-id="36c9b-594">TradeWorkflowState</span></span>|
|<span data-ttu-id="36c9b-595">WMSExpeditionStatus</span><span class="sxs-lookup"><span data-stu-id="36c9b-595">WMSExpeditionStatus</span></span>|


## <a name="extensible-sql-operations"></a><span data-ttu-id="36c9b-596">拡張可能な SQL 操作</span><span class="sxs-lookup"><span data-stu-id="36c9b-596">Extensible SQL Operations</span></span>

<span data-ttu-id="36c9b-597">これらの SQL 操作は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="36c9b-597">These SQL operations have been made extensible in this update.</span></span>

| <span data-ttu-id="36c9b-598">工程</span><span class="sxs-lookup"><span data-stu-id="36c9b-598">Operation</span></span> |
| --------------- |
|<span data-ttu-id="36c9b-599">CustInterestPost.postVoucherPerTransaction</span><span class="sxs-lookup"><span data-stu-id="36c9b-599">CustInterestPost.postVoucherPerTransaction</span></span>|
|<span data-ttu-id="36c9b-600">InventMov_ProdLine_JournalBom.insertChildBuffer</span><span class="sxs-lookup"><span data-stu-id="36c9b-600">InventMov_ProdLine_JournalBom.insertChildBuffer</span></span>|
|<span data-ttu-id="36c9b-601">InventUpdate.initInventTransToReceiveList</span><span class="sxs-lookup"><span data-stu-id="36c9b-601">InventUpdate.initInventTransToReceiveList</span></span>|
|<span data-ttu-id="36c9b-602">ProjAdjustmentUpdate_PostAsync.postAsync</span><span class="sxs-lookup"><span data-stu-id="36c9b-602">ProjAdjustmentUpdate_PostAsync.postAsync</span></span>|
|<span data-ttu-id="36c9b-603">ProjBudgetManager.createBudgetCostForecast</span><span class="sxs-lookup"><span data-stu-id="36c9b-603">ProjBudgetManager.createBudgetCostForecast</span></span>|
|<span data-ttu-id="36c9b-604">ProjBudgetManager.createBudgetEmplForecast</span><span class="sxs-lookup"><span data-stu-id="36c9b-604">ProjBudgetManager.createBudgetEmplForecast</span></span>|
|<span data-ttu-id="36c9b-605">ProjBudgetManager.createBudgetRevenueForecast</span><span class="sxs-lookup"><span data-stu-id="36c9b-605">ProjBudgetManager.createBudgetRevenueForecast</span></span>|
|<span data-ttu-id="36c9b-606">ProjBudgetManager.createBudgetSalesForecast</span><span class="sxs-lookup"><span data-stu-id="36c9b-606">ProjBudgetManager.createBudgetSalesForecast</span></span>|


## <a name="metadata-changes"></a><span data-ttu-id="36c9b-607">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="36c9b-607">Metadata changes</span></span>

<span data-ttu-id="36c9b-608">これらのメタデータの変更は、このアップデートで行われました。</span><span class="sxs-lookup"><span data-stu-id="36c9b-608">These metadata changes have been made in this update.</span></span>

| <span data-ttu-id="36c9b-609">工程</span><span class="sxs-lookup"><span data-stu-id="36c9b-609">Operation</span></span> |
| --------------- |
|<span data-ttu-id="36c9b-610">/Data entities/ReqPlannedOrderEntity.Is Public</span><span class="sxs-lookup"><span data-stu-id="36c9b-610">/Data entities/ReqPlannedOrderEntity.Is Public</span></span>|
|<span data-ttu-id="36c9b-611">/DataTypes/Extended Data Types/AmountQty.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-611">/DataTypes/Extended Data Types/AmountQty.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-612">/DataTypes/Extended Data Types/AssetDepreciationAmountUnitReportingCurrency.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-612">/DataTypes/Extended Data Types/AssetDepreciationAmountUnitReportingCurrency.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-613">/DataTypes/Extended Data Types/BOMProductQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-613">/DataTypes/Extended Data Types/BOMProductQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-614">/DataTypes/Extended Data Types/CostPriceNonMonetary.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-614">/DataTypes/Extended Data Types/CostPriceNonMonetary.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-615">/DataTypes/Extended Data Types/CostQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-615">/DataTypes/Extended Data Types/CostQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-616">/DataTypes/Extended Data Types/MCRRoyaltyValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-616">/DataTypes/Extended Data Types/MCRRoyaltyValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-617">/DataTypes/Extended Data Types/PdsRebateValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-617">/DataTypes/Extended Data Types/PdsRebateValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-618">/DataTypes/Extended Data Types/PriceDiscAmount.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-618">/DataTypes/Extended Data Types/PriceDiscAmount.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-619">/DataTypes/Extended Data Types/PriceQty.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-619">/DataTypes/Extended Data Types/PriceQty.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-620">/DataTypes/Extended Data Types/PriceUnit.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-620">/DataTypes/Extended Data Types/PriceUnit.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-621">/DataTypes/Extended Data Types/PriceUnit.Scale</span><span class="sxs-lookup"><span data-stu-id="36c9b-621">/DataTypes/Extended Data Types/PriceUnit.Scale</span></span>|
|<span data-ttu-id="36c9b-622">/DataTypes/Extended Data Types/ProductQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-622">/DataTypes/Extended Data Types/ProductQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-623">/DataTypes/Extended Data Types/ProductQuantityHourValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-623">/DataTypes/Extended Data Types/ProductQuantityHourValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-624">/DataTypes/Extended Data Types/ProjName.Extends</span><span class="sxs-lookup"><span data-stu-id="36c9b-624">/DataTypes/Extended Data Types/ProjName.Extends</span></span>|
|<span data-ttu-id="36c9b-625">/DataTypes/Extended Data Types/TAMRebateValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-625">/DataTypes/Extended Data Types/TAMRebateValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-626">/DataTypes/Extended Data Types/UnitAmountCur.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-626">/DataTypes/Extended Data Types/UnitAmountCur.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-627">/DataTypes/Extended Data Types/UnitAmountMST.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-627">/DataTypes/Extended Data Types/UnitAmountMST.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-628">/DataTypes/Extended Data Types/WeightBase.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="36c9b-628">/DataTypes/Extended Data Types/WeightBase.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="36c9b-629">/Tables/LedgerJournalTrans_Project/Relations/LedgerJournalTrans.createNavigationPropertyMethod</span><span class="sxs-lookup"><span data-stu-id="36c9b-629">/Tables/LedgerJournalTrans_Project/Relations/LedgerJournalTrans.createNavigationPropertyMethod</span></span>|
|<span data-ttu-id="36c9b-630">/Tables/PriceDiscGroup.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="36c9b-630">/Tables/PriceDiscGroup.Cache Lookup</span></span>|
|<span data-ttu-id="36c9b-631">/Tables/VendInvoiceJour/Fields/DefaultDimension.Visible</span><span class="sxs-lookup"><span data-stu-id="36c9b-631">/Tables/VendInvoiceJour/Fields/DefaultDimension.Visible</span></span>|
|<span data-ttu-id="36c9b-632">/Tables/VendInvoiceTrans/Fields/DefaultDimension.Visible</span><span class="sxs-lookup"><span data-stu-id="36c9b-632">/Tables/VendInvoiceTrans/Fields/DefaultDimension.Visible</span></span>|
|<span data-ttu-id="36c9b-633">/Tables/WMSAisle.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="36c9b-633">/Tables/WMSAisle.Cache Lookup</span></span>|
|<span data-ttu-id="36c9b-634">/Tables/WorkCalendarTable.Create Rec Id Index</span><span class="sxs-lookup"><span data-stu-id="36c9b-634">/Tables/WorkCalendarTable.Create Rec Id Index</span></span>|
|<span data-ttu-id="36c9b-635">/Tables/WorkTimeLine.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="36c9b-635">/Tables/WorkTimeLine.Cache Lookup</span></span>|
|<span data-ttu-id="36c9b-636">/Tables/WorkTimeTable.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="36c9b-636">/Tables/WorkTimeTable.Cache Lookup</span></span>|


## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="36c9b-637">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="36c9b-637">Additional extensibility enhancements</span></span>

<span data-ttu-id="36c9b-638">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="36c9b-638">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="36c9b-639">バグ リクエスト: "CustCollectionLetterTrans -> CollectionLetterNum" 関係プロパティ</span><span class="sxs-lookup"><span data-stu-id="36c9b-639">Bug request: "CustCollectionLetterTrans -> CollectionLetterNum" Relation properties</span></span>
- <span data-ttu-id="36c9b-640">価格の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="36c9b-640">Enable increase of decimal precision through extensiblity for prices</span></span>
- <span data-ttu-id="36c9b-641">重量の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="36c9b-641">Enable increase of decimal precision through extensiblity for weights</span></span>
- <span data-ttu-id="36c9b-642">マップ拡張: LogisticsEntityLocationMap</span><span class="sxs-lookup"><span data-stu-id="36c9b-642">Map Extension: LogisticsEntityLocationMap</span></span>
- <span data-ttu-id="36c9b-643">OMOperatingUnit は、DimAttributeOMDepartment.Value のユーザー フレンドリおよび定義済の値を指定する必要がある</span><span class="sxs-lookup"><span data-stu-id="36c9b-643">OMOperatingUnit should provide user friendly and defined value for DimAttributeOMDepartment.Value</span></span>
- <span data-ttu-id="36c9b-644">InventPosting が LedgerDimension を検索する方法を再設計</span><span class="sxs-lookup"><span data-stu-id="36c9b-644">Redesign how InventPosting finds LedgerDimension</span></span>
- <span data-ttu-id="36c9b-645">WhsWorkExecuteDisplayAdjustIn を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="36c9b-645">Refactor WhsWorkExecuteDisplayAdjustIn to ProcessGuide framework</span></span>
- <span data-ttu-id="36c9b-646">WHSWorkExecuteDisplayChangeWarehouse を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="36c9b-646">Refactor WHSWorkExecuteDisplayChangeWarehouse to ProcessGuide framework</span></span>
- <span data-ttu-id="36c9b-647">WhsWorkExecuteDisplayInquiryItem を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="36c9b-647">Refactor WhsWorkExecuteDisplayInquiryItem to ProcessGuide framework</span></span>
- <span data-ttu-id="36c9b-648">WhsWorkExecuteDisplayInquiryLocation を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="36c9b-648">Refactor WhsWorkExecuteDisplayInquiryLocation to ProcessGuide framework</span></span>
- <span data-ttu-id="36c9b-649">WhsWorkExecuteDisplayInquiryLP を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="36c9b-649">Refactor WhsWorkExecuteDisplayInquiryLP to ProcessGuide framework</span></span>
- <span data-ttu-id="36c9b-650">whsWorkExecuteDisplayReprintLabel を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="36c9b-650">Refactor whsWorkExecuteDisplayReprintLabel to ProcessGuide framework</span></span>
- <span data-ttu-id="36c9b-651">小売チャネル: サポート BankDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="36c9b-651">Retail channel: Support BankDropOperationRequest</span></span>

