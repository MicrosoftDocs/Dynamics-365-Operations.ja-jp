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
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: App 8.1
ms.openlocfilehash: bea74016ef6ea5c683c302dc7aa038932296dc4e
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833450"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-81"></a><span data-ttu-id="52a2c-103">Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="52a2c-103">Extensibility changes in Dynamics 365 for Finance and Operations version 8.1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52a2c-104">これは、Dynamics 365 for Finance and Operations バージョン 8.1 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="52a2c-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations version 8.1.</span></span> <span data-ttu-id="52a2c-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52a2c-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="52a2c-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="52a2c-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="52a2c-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="52a2c-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="52a2c-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="52a2c-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="52a2c-109">AssetPost.createTrueUpDepreciation</span><span class="sxs-lookup"><span data-stu-id="52a2c-109">AssetPost.createTrueUpDepreciation</span></span>|
|<span data-ttu-id="52a2c-110">AssetPost.createTrueUpDepreciation</span><span class="sxs-lookup"><span data-stu-id="52a2c-110">AssetPost.createTrueUpDepreciation</span></span>|
|<span data-ttu-id="52a2c-111">AssetPostDisposal.post</span><span class="sxs-lookup"><span data-stu-id="52a2c-111">AssetPostDisposal.post</span></span>|
|<span data-ttu-id="52a2c-112">AssetPostDisposal.postVoucherTransactions</span><span class="sxs-lookup"><span data-stu-id="52a2c-112">AssetPostDisposal.postVoucherTransactions</span></span>|
|<span data-ttu-id="52a2c-113">AssetPostDisposal.postVoucherTransactions</span><span class="sxs-lookup"><span data-stu-id="52a2c-113">AssetPostDisposal.postVoucherTransactions</span></span>|
|<span data-ttu-id="52a2c-114">AssetTable.buildComposedOf</span><span class="sxs-lookup"><span data-stu-id="52a2c-114">AssetTable.buildComposedOf</span></span>|
|<span data-ttu-id="52a2c-115">AssetTable.createStruct</span><span class="sxs-lookup"><span data-stu-id="52a2c-115">AssetTable.createStruct</span></span>|
|<span data-ttu-id="52a2c-116">AxInventDim_SalesLine.setInventSiteId</span><span class="sxs-lookup"><span data-stu-id="52a2c-116">AxInventDim_SalesLine.setInventSiteId</span></span>|
|<span data-ttu-id="52a2c-117">BankChequePrint.printDocument</span><span class="sxs-lookup"><span data-stu-id="52a2c-117">BankChequePrint.printDocument</span></span>|
|<span data-ttu-id="52a2c-118">BankCodaProcessing.custSettlement</span><span class="sxs-lookup"><span data-stu-id="52a2c-118">BankCodaProcessing.custSettlement</span></span>|
|<span data-ttu-id="52a2c-119">BankDeposit.InitFromLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-119">BankDeposit.InitFromLedgerJournalTrans</span></span>|
|<span data-ttu-id="52a2c-120">BankExchAdj_RU.calcAndPostCurrency</span><span class="sxs-lookup"><span data-stu-id="52a2c-120">BankExchAdj_RU.calcAndPostCurrency</span></span>|
|<span data-ttu-id="52a2c-121">BankExchAdj_RU.calcAndPostCurrency</span><span class="sxs-lookup"><span data-stu-id="52a2c-121">BankExchAdj_RU.calcAndPostCurrency</span></span>|
|<span data-ttu-id="52a2c-122">BankExchAdj_RU.calcBalance</span><span class="sxs-lookup"><span data-stu-id="52a2c-122">BankExchAdj_RU.calcBalance</span></span>|
|<span data-ttu-id="52a2c-123">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="52a2c-123">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="52a2c-124">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="52a2c-124">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="52a2c-125">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="52a2c-125">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="52a2c-126">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="52a2c-126">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="52a2c-127">BlindCloseView.MPOS_ExtensibleViews</span><span class="sxs-lookup"><span data-stu-id="52a2c-127">BlindCloseView.MPOS_ExtensibleViews</span></span>|
|<span data-ttu-id="52a2c-128">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span><span class="sxs-lookup"><span data-stu-id="52a2c-128">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span></span>|
|<span data-ttu-id="52a2c-129">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span><span class="sxs-lookup"><span data-stu-id="52a2c-129">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span></span>|
|<span data-ttu-id="52a2c-130">BudgetAnalysisInquiryProcessor_PSN.getBudgetAnalysisLedgerDimensions</span><span class="sxs-lookup"><span data-stu-id="52a2c-130">BudgetAnalysisInquiryProcessor_PSN.getBudgetAnalysisLedgerDimensions</span></span>|
|<span data-ttu-id="52a2c-131">CAMStatisticalEntryTransferJournalEntryDataMapper.newFromParameters</span><span class="sxs-lookup"><span data-stu-id="52a2c-131">CAMStatisticalEntryTransferJournalEntryDataMapper.newFromParameters</span></span>|
|<span data-ttu-id="52a2c-132">CaseUpdateStatus_Close.changeStatus</span><span class="sxs-lookup"><span data-stu-id="52a2c-132">CaseUpdateStatus_Close.changeStatus</span></span>|
|<span data-ttu-id="52a2c-133">CashManagementView.NewExtension</span><span class="sxs-lookup"><span data-stu-id="52a2c-133">CashManagementView.NewExtension</span></span>|
|<span data-ttu-id="52a2c-134">ChequeController.init</span><span class="sxs-lookup"><span data-stu-id="52a2c-134">ChequeController.init</span></span>|
|<span data-ttu-id="52a2c-135">ChequeDP.insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="52a2c-135">ChequeDP.insertChequeTmp</span></span>|
|<span data-ttu-id="52a2c-136">クラス InventTransferEstimation.updateEstimatedPre</span><span class="sxs-lookup"><span data-stu-id="52a2c-136">Class InventTransferEstimation.updateEstimatedPre</span></span>|
|<span data-ttu-id="52a2c-137">クラス Markup.insertReturnMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-137">class Markup.insertReturnMarkupTrans</span></span>|
|<span data-ttu-id="52a2c-138">クラス MarkupTransInsert.insertForCodes</span><span class="sxs-lookup"><span data-stu-id="52a2c-138">class MarkupTransInsert.insertForCodes</span></span>|
|<span data-ttu-id="52a2c-139">クラス PurchLineType.updateSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-139">Class PurchLineType.updateSalesLine</span></span>|
|<span data-ttu-id="52a2c-140">クラス PurchPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="52a2c-140">class PurchPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="52a2c-141">クラス SalesQuantity_PackingSlip.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="52a2c-141">Class SalesQuantity_PackingSlip.calcQtyInvent</span></span>|
|<span data-ttu-id="52a2c-142">クラス SalesQuantity_PackingSlip.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="52a2c-142">Class SalesQuantity_PackingSlip.calcQtySales</span></span>|
|<span data-ttu-id="52a2c-143">Class/AssetPost.post</span><span class="sxs-lookup"><span data-stu-id="52a2c-143">Class/AssetPost.post</span></span>|
|<span data-ttu-id="52a2c-144">Class/FormLetterJournalPost.post</span><span class="sxs-lookup"><span data-stu-id="52a2c-144">Class/FormLetterJournalPost.post</span></span>|
|<span data-ttu-id="52a2c-145">Class/PurchReqTableListPageInteraction.applyFilter</span><span class="sxs-lookup"><span data-stu-id="52a2c-145">Class/PurchReqTableListPageInteraction.applyFilter</span></span>|
|<span data-ttu-id="52a2c-146">Class\PurchFormLetter_PackingSlip.checkFormLetterId</span><span class="sxs-lookup"><span data-stu-id="52a2c-146">Class\PurchFormLetter_PackingSlip.checkFormLetterId</span></span>|
|<span data-ttu-id="52a2c-147">Class\PurchFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-147">Class\PurchFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="52a2c-148">Class\TaxCalculationAdjustment.calcManualInserted</span><span class="sxs-lookup"><span data-stu-id="52a2c-148">Class\TaxCalculationAdjustment.calcManualInserted</span></span>|
|<span data-ttu-id="52a2c-149">CompanyInfoHelper.onValidateField</span><span class="sxs-lookup"><span data-stu-id="52a2c-149">CompanyInfoHelper.onValidateField</span></span>|
|<span data-ttu-id="52a2c-150">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span><span class="sxs-lookup"><span data-stu-id="52a2c-150">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span></span>|
|<span data-ttu-id="52a2c-151">CustAccountStatementExtController.initAgingBalances</span><span class="sxs-lookup"><span data-stu-id="52a2c-151">CustAccountStatementExtController.initAgingBalances</span></span>|
|<span data-ttu-id="52a2c-152">CustAccountStatementExtController.preprocessParty</span><span class="sxs-lookup"><span data-stu-id="52a2c-152">CustAccountStatementExtController.preprocessParty</span></span>|
|<span data-ttu-id="52a2c-153">CustAccountStatementExtController.processParty</span><span class="sxs-lookup"><span data-stu-id="52a2c-153">CustAccountStatementExtController.processParty</span></span>|
|<span data-ttu-id="52a2c-154">CustAccountStatementExtController.processTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-154">CustAccountStatementExtController.processTrans</span></span>|
|<span data-ttu-id="52a2c-155">CustAccountStatementExtController.runPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="52a2c-155">CustAccountStatementExtController.runPrintMgmt</span></span>|
|<span data-ttu-id="52a2c-156">CustCollectionLetterCreate.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-156">CustCollectionLetterCreate.run</span></span>|
|<span data-ttu-id="52a2c-157">CustCollectionLetterPost.RUN</span><span class="sxs-lookup"><span data-stu-id="52a2c-157">CustCollectionLetterPost.RUN</span></span>|
|<span data-ttu-id="52a2c-158">CustInterestAdjust.createCustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-158">CustInterestAdjust.createCustInvoiceTable</span></span>|
|<span data-ttu-id="52a2c-159">CustInterestCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-159">CustInterestCreate.createJournal</span></span>|
|<span data-ttu-id="52a2c-160">CustInterestCreate.logDateRecordError</span><span class="sxs-lookup"><span data-stu-id="52a2c-160">CustInterestCreate.logDateRecordError</span></span>|
|<span data-ttu-id="52a2c-161">CustInterestCreate.newAccount</span><span class="sxs-lookup"><span data-stu-id="52a2c-161">CustInterestCreate.newAccount</span></span>|
|<span data-ttu-id="52a2c-162">CustInterestCreate.resetCustInterest</span><span class="sxs-lookup"><span data-stu-id="52a2c-162">CustInterestCreate.resetCustInterest</span></span>|
|<span data-ttu-id="52a2c-163">CustInterestCreate.runOnce</span><span class="sxs-lookup"><span data-stu-id="52a2c-163">CustInterestCreate.runOnce</span></span>|
|<span data-ttu-id="52a2c-164">CustInvoiceCalcTax_Invoice.updateTaxWriteCode</span><span class="sxs-lookup"><span data-stu-id="52a2c-164">CustInvoiceCalcTax_Invoice.updateTaxWriteCode</span></span>|
|<span data-ttu-id="52a2c-165">CustInvoiceLine.Insert</span><span class="sxs-lookup"><span data-stu-id="52a2c-165">CustInvoiceLine.Insert</span></span>|
|<span data-ttu-id="52a2c-166">CustOutPaym.generatePaymentLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-166">CustOutPaym.generatePaymentLines</span></span>|
|<span data-ttu-id="52a2c-167">CustQuotationJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-167">CustQuotationJour.printJournal</span></span>|
|<span data-ttu-id="52a2c-168">CustTable.CanSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="52a2c-168">CustTable.CanSubmitToWorkflow</span></span>|
|<span data-ttu-id="52a2c-169">CustTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="52a2c-169">CustTrans.documentDateModified</span></span>|
|<span data-ttu-id="52a2c-170">CustTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="52a2c-170">CustTrans.documentDateModified</span></span>|
|<span data-ttu-id="52a2c-171">CustTransSettlement.insertSettlementLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-171">CustTransSettlement.insertSettlementLines</span></span>|
|<span data-ttu-id="52a2c-172">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-172">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="52a2c-173">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="52a2c-173">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="52a2c-174">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="52a2c-174">CustVendCheque.output</span></span>|
|<span data-ttu-id="52a2c-175">CustVendChequeSlipTextCalculator.seebelow</span><span class="sxs-lookup"><span data-stu-id="52a2c-175">CustVendChequeSlipTextCalculator.seebelow</span></span>|
|<span data-ttu-id="52a2c-176">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="52a2c-176">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span></span>|
|<span data-ttu-id="52a2c-177">CustVendPaymProposalTransferToJournal.transferProposal</span><span class="sxs-lookup"><span data-stu-id="52a2c-177">CustVendPaymProposalTransferToJournal.transferProposal</span></span>|
|<span data-ttu-id="52a2c-178">CustVendPaymSched.construct</span><span class="sxs-lookup"><span data-stu-id="52a2c-178">CustVendPaymSched.construct</span></span>|
|<span data-ttu-id="52a2c-179">CustVendPaymSched.initCalcPaymSched</span><span class="sxs-lookup"><span data-stu-id="52a2c-179">CustVendPaymSched.initCalcPaymSched</span></span>|
|<span data-ttu-id="52a2c-180">CustVendReversePosting.restoreCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="52a2c-180">CustVendReversePosting.restoreCustVendTransOpen</span></span>|
|<span data-ttu-id="52a2c-181">CustVendVoucher.post</span><span class="sxs-lookup"><span data-stu-id="52a2c-181">CustVendVoucher.post</span></span>|
|<span data-ttu-id="52a2c-182">DataEntityView/SalesOrderLineEntity/Method/validateWrite</span><span class="sxs-lookup"><span data-stu-id="52a2c-182">DataEntityView/SalesOrderLineEntity/Method/validateWrite</span></span>|
|<span data-ttu-id="52a2c-183">DataEntityView/SalesQuotationLineEntity/Method/validateWrite</span><span class="sxs-lookup"><span data-stu-id="52a2c-183">DataEntityView/SalesQuotationLineEntity/Method/validateWrite</span></span>|
|<span data-ttu-id="52a2c-184">EFDocEmailProcessor_BR.saveReceivedXmlData</span><span class="sxs-lookup"><span data-stu-id="52a2c-184">EFDocEmailProcessor_BR.saveReceivedXmlData</span></span>|
|<span data-ttu-id="52a2c-185">EFDocMsgFormat_XmlBase_BR.createElementWithValue</span><span class="sxs-lookup"><span data-stu-id="52a2c-185">EFDocMsgFormat_XmlBase_BR.createElementWithValue</span></span>|
|<span data-ttu-id="52a2c-186">メソッドに抽出: SalesParmTable.GetPaymentSched</span><span class="sxs-lookup"><span data-stu-id="52a2c-186">Extract into method: SalesParmTable.GetPaymentSched</span></span>|
|<span data-ttu-id="52a2c-187">フォーム InventJournalAsset\Methods\init</span><span class="sxs-lookup"><span data-stu-id="52a2c-187">Form InventJournalAsset\Methods\init</span></span>|
|<span data-ttu-id="52a2c-188">フォーム InventJournalCount\Methods\init</span><span class="sxs-lookup"><span data-stu-id="52a2c-188">Form InventJournalCount\Methods\init</span></span>|
|<span data-ttu-id="52a2c-189">フォーム InventJournalMovement.init</span><span class="sxs-lookup"><span data-stu-id="52a2c-189">Form InventJournalMovement.init</span></span>|
|<span data-ttu-id="52a2c-190">フォーム TrvExpenses.confirmCategoryChange</span><span class="sxs-lookup"><span data-stu-id="52a2c-190">Form TrvExpenses.confirmCategoryChange</span></span>|
|<span data-ttu-id="52a2c-191">Form\SalesEditLines.closeOk</span><span class="sxs-lookup"><span data-stu-id="52a2c-191">Form\SalesEditLines.closeOk</span></span>|
|<span data-ttu-id="52a2c-192">FormletterJournalPost.newPostPurch</span><span class="sxs-lookup"><span data-stu-id="52a2c-192">FormletterJournalPost.newPostPurch</span></span>|
|<span data-ttu-id="52a2c-193">FreeTextInvoiceDP.Variable 宣言</span><span class="sxs-lookup"><span data-stu-id="52a2c-193">FreeTextInvoiceDP.Variable declaration</span></span>|
|<span data-ttu-id="52a2c-194">HcmActionTypeSetup.lookupWorkflowTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-194">HcmActionTypeSetup.lookupWorkflowTable</span></span>|
|<span data-ttu-id="52a2c-195">HcmPosition_HcmPositionDefaultDimension_formDatasource.selectionChanged</span><span class="sxs-lookup"><span data-stu-id="52a2c-195">HcmPosition_HcmPositionDefaultDimension_formDatasource.selectionChanged</span></span>|
|<span data-ttu-id="52a2c-196">HcmPositionTransition:: createHcmPositionWorkerAssignment</span><span class="sxs-lookup"><span data-stu-id="52a2c-196">HcmPositionTransition:: createHcmPositionWorkerAssignment</span></span>|
|<span data-ttu-id="52a2c-197">HcmPositionWorkerAssignmentDialog:: createWorkerActionOk</span><span class="sxs-lookup"><span data-stu-id="52a2c-197">HcmPositionWorkerAssignmentDialog:: createWorkerActionOk</span></span>|
|<span data-ttu-id="52a2c-198">HRMCompFixedPlanTable::enforcePayRateTolerance</span><span class="sxs-lookup"><span data-stu-id="52a2c-198">HRMCompFixedPlanTable::enforcePayRateTolerance</span></span> |
|<span data-ttu-id="52a2c-199">InterCompanyPostPurch.construct</span><span class="sxs-lookup"><span data-stu-id="52a2c-199">InterCompanyPostPurch.construct</span></span>|
|<span data-ttu-id="52a2c-200">InterCompanyPostPurch.formLetterUpdate</span><span class="sxs-lookup"><span data-stu-id="52a2c-200">InterCompanyPostPurch.formLetterUpdate</span></span>|
|<span data-ttu-id="52a2c-201">InterCompanyPostSales.formLetterUpdate</span><span class="sxs-lookup"><span data-stu-id="52a2c-201">InterCompanyPostSales.formLetterUpdate</span></span>|
|<span data-ttu-id="52a2c-202">InterCompanySyncPurchTableType.setSalesTableData</span><span class="sxs-lookup"><span data-stu-id="52a2c-202">InterCompanySyncPurchTableType.setSalesTableData</span></span>|
|<span data-ttu-id="52a2c-203">IntrastatCheck.Run</span><span class="sxs-lookup"><span data-stu-id="52a2c-203">IntrastatCheck.Run</span></span>|
|<span data-ttu-id="52a2c-204">IntrastatTransfer.calcAmountsAndMarkups</span><span class="sxs-lookup"><span data-stu-id="52a2c-204">IntrastatTransfer.calcAmountsAndMarkups</span></span>|
|<span data-ttu-id="52a2c-205">IntrastatTransfer.calcValuesSign</span><span class="sxs-lookup"><span data-stu-id="52a2c-205">IntrastatTransfer.calcValuesSign</span></span>|
|<span data-ttu-id="52a2c-206">IntrastatTransfer.distributeIntrastatAddValueLV</span><span class="sxs-lookup"><span data-stu-id="52a2c-206">IntrastatTransfer.distributeIntrastatAddValueLV</span></span>|
|<span data-ttu-id="52a2c-207">IntrastatTransfer.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-207">IntrastatTransfer.run</span></span>|
|<span data-ttu-id="52a2c-208">IntrastatTransferIT.calcCounty</span><span class="sxs-lookup"><span data-stu-id="52a2c-208">IntrastatTransferIT.calcCounty</span></span>|
|<span data-ttu-id="52a2c-209">IntrastatTransferIT.updateTransactionCurrencyAmount</span><span class="sxs-lookup"><span data-stu-id="52a2c-209">IntrastatTransferIT.updateTransactionCurrencyAmount</span></span>|
|<span data-ttu-id="52a2c-210">InventAdj_Transact.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-210">InventAdj_Transact.run</span></span>|
|<span data-ttu-id="52a2c-211">InventCostPost.postInventCostTransVariance</span><span class="sxs-lookup"><span data-stu-id="52a2c-211">InventCostPost.postInventCostTransVariance</span></span>|
|<span data-ttu-id="52a2c-212">InventMov_Purch.updateAutoLossProfit</span><span class="sxs-lookup"><span data-stu-id="52a2c-212">InventMov_Purch.updateAutoLossProfit</span></span>|
|<span data-ttu-id="52a2c-213">InventMov_Purch.updateBuffer</span><span class="sxs-lookup"><span data-stu-id="52a2c-213">InventMov_Purch.updateBuffer</span></span>|
|<span data-ttu-id="52a2c-214">InventMovement.checkUpdatePhysical</span><span class="sxs-lookup"><span data-stu-id="52a2c-214">InventMovement.checkUpdatePhysical</span></span>|
|<span data-ttu-id="52a2c-215">InventoryLookupMatrixView.ExtensibleViews</span><span class="sxs-lookup"><span data-stu-id="52a2c-215">InventoryLookupMatrixView.ExtensibleViews</span></span>|
|<span data-ttu-id="52a2c-216">InventTable.pdsValidateBestBeforeDays</span><span class="sxs-lookup"><span data-stu-id="52a2c-216">InventTable.pdsValidateBestBeforeDays</span></span>|
|<span data-ttu-id="52a2c-217">InventTransWMS_Register.updateInventFromMovementServer</span><span class="sxs-lookup"><span data-stu-id="52a2c-217">InventTransWMS_Register.updateInventFromMovementServer</span></span>|
|<span data-ttu-id="52a2c-218">InventUpd_ChildReference.updateLessIssue</span><span class="sxs-lookup"><span data-stu-id="52a2c-218">InventUpd_ChildReference.updateLessIssue</span></span>|
|<span data-ttu-id="52a2c-219">InventUpd_ChildReference.updateLessReceipt</span><span class="sxs-lookup"><span data-stu-id="52a2c-219">InventUpd_ChildReference.updateLessReceipt</span></span>|
|<span data-ttu-id="52a2c-220">InventUpd_ChildReference.updateMoreIssue</span><span class="sxs-lookup"><span data-stu-id="52a2c-220">InventUpd_ChildReference.updateMoreIssue</span></span>|
|<span data-ttu-id="52a2c-221">InventUpd_ChildReference.updateMoreReceipt</span><span class="sxs-lookup"><span data-stu-id="52a2c-221">InventUpd_ChildReference.updateMoreReceipt</span></span>|
|<span data-ttu-id="52a2c-222">InventUpd_Financial.newSalesInvoice</span><span class="sxs-lookup"><span data-stu-id="52a2c-222">InventUpd_Financial.newSalesInvoice</span></span>|
|<span data-ttu-id="52a2c-223">InventUpd_Physical.updatePhysicalIssue</span><span class="sxs-lookup"><span data-stu-id="52a2c-223">InventUpd_Physical.updatePhysicalIssue</span></span>|
|<span data-ttu-id="52a2c-224">InventUpd_Physical.updateTransPhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="52a2c-224">InventUpd_Physical.updateTransPhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="52a2c-225">InventUpd_Physical::newSalesPackingSlip</span><span class="sxs-lookup"><span data-stu-id="52a2c-225">InventUpd_Physical::newSalesPackingSlip</span></span>|
|<span data-ttu-id="52a2c-226">InventUpd_Reservation.updateNow</span><span class="sxs-lookup"><span data-stu-id="52a2c-226">InventUpd_Reservation.updateNow</span></span>|
|<span data-ttu-id="52a2c-227">InventUpd_Reservation.updateReserveMore</span><span class="sxs-lookup"><span data-stu-id="52a2c-227">InventUpd_Reservation.updateReserveMore</span></span>|
|<span data-ttu-id="52a2c-228">InventUpdate.updateInventTransPosting</span><span class="sxs-lookup"><span data-stu-id="52a2c-228">InventUpdate.updateInventTransPosting</span></span>|
|<span data-ttu-id="52a2c-229">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-229">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="52a2c-230">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-230">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="52a2c-231">InventUpdateMarking.addMarking</span><span class="sxs-lookup"><span data-stu-id="52a2c-231">InventUpdateMarking.addMarking</span></span>|
|<span data-ttu-id="52a2c-232">InventUpdateMarking.removeMarking</span><span class="sxs-lookup"><span data-stu-id="52a2c-232">InventUpdateMarking.removeMarking</span></span>|
|<span data-ttu-id="52a2c-233">InventUpdateReserveMore.createQueryRuns</span><span class="sxs-lookup"><span data-stu-id="52a2c-233">InventUpdateReserveMore.createQueryRuns</span></span>|
|<span data-ttu-id="52a2c-234">JmgCalcApprovePickDialog.closeOk</span><span class="sxs-lookup"><span data-stu-id="52a2c-234">JmgCalcApprovePickDialog.closeOk</span></span>|
|<span data-ttu-id="52a2c-235">JmgJobBundle.postTime</span><span class="sxs-lookup"><span data-stu-id="52a2c-235">JmgJobBundle.postTime</span></span>|
|<span data-ttu-id="52a2c-236">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span><span class="sxs-lookup"><span data-stu-id="52a2c-236">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span></span>|
|<span data-ttu-id="52a2c-237">JournalStaticDataModel.initializeJournalTableFields</span><span class="sxs-lookup"><span data-stu-id="52a2c-237">JournalStaticDataModel.initializeJournalTableFields</span></span>|
|<span data-ttu-id="52a2c-238">Ledger.populateTmpTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-238">Ledger.populateTmpTable</span></span>|
|<span data-ttu-id="52a2c-239">Ledger::populateTmpTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-239">Ledger::populateTmpTable</span></span>|
|<span data-ttu-id="52a2c-240">LedgerAccrualTrans_Calendar.allocate</span><span class="sxs-lookup"><span data-stu-id="52a2c-240">LedgerAccrualTrans_Calendar.allocate</span></span>|
|<span data-ttu-id="52a2c-241">LedgerAccrualTrans_Calendar.allocate</span><span class="sxs-lookup"><span data-stu-id="52a2c-241">LedgerAccrualTrans_Calendar.allocate</span></span>|
|<span data-ttu-id="52a2c-242">LedgerAccrualTrans_Fiscal.allocate</span><span class="sxs-lookup"><span data-stu-id="52a2c-242">LedgerAccrualTrans_Fiscal.allocate</span></span>|
|<span data-ttu-id="52a2c-243">LedgerAccrualTrans_Fiscal.allocate</span><span class="sxs-lookup"><span data-stu-id="52a2c-243">LedgerAccrualTrans_Fiscal.allocate</span></span>|
|<span data-ttu-id="52a2c-244">LedgerAutomaticTransactionAccountEntity</span><span class="sxs-lookup"><span data-stu-id="52a2c-244">LedgerAutomaticTransactionAccountEntity</span></span>|
|<span data-ttu-id="52a2c-245">LedgerCreatePeriodBalances.createPeriodBalancesMainAccount</span><span class="sxs-lookup"><span data-stu-id="52a2c-245">LedgerCreatePeriodBalances.createPeriodBalancesMainAccount</span></span>|
|<span data-ttu-id="52a2c-246">LedgerExchAdj.postAdjustment</span><span class="sxs-lookup"><span data-stu-id="52a2c-246">LedgerExchAdj.postAdjustment</span></span>|
|<span data-ttu-id="52a2c-247">LedgerExchAdj.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-247">LedgerExchAdj.run</span></span>|
|<span data-ttu-id="52a2c-248">LedgerFiscalJournalDP_IT.getDisplaySequenceNumber</span><span class="sxs-lookup"><span data-stu-id="52a2c-248">LedgerFiscalJournalDP_IT.getDisplaySequenceNumber</span></span>|
|<span data-ttu-id="52a2c-249">LedgerJournalCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-249">LedgerJournalCheckPost.checkJournal</span></span>|
|<span data-ttu-id="52a2c-250">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-250">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="52a2c-251">LedgerJournalCheckPost.runInternal</span><span class="sxs-lookup"><span data-stu-id="52a2c-251">LedgerJournalCheckPost.runInternal</span></span>|
|<span data-ttu-id="52a2c-252">LedgerJournalEngine.accountModified</span><span class="sxs-lookup"><span data-stu-id="52a2c-252">LedgerJournalEngine.accountModified</span></span>|
|<span data-ttu-id="52a2c-253">LedgerJournalEngine.calculateTaxForCompleteJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-253">LedgerJournalEngine.calculateTaxForCompleteJournal</span></span>|
|<span data-ttu-id="52a2c-254">LedgerJournalEngine.findSettledAmount</span><span class="sxs-lookup"><span data-stu-id="52a2c-254">LedgerJournalEngine.findSettledAmount</span></span>|
|<span data-ttu-id="52a2c-255">LedgerJournalEngine.formSettlement</span><span class="sxs-lookup"><span data-stu-id="52a2c-255">LedgerJournalEngine.formSettlement</span></span>|
|<span data-ttu-id="52a2c-256">LedgerJournalEngine.newVoucher</span><span class="sxs-lookup"><span data-stu-id="52a2c-256">LedgerJournalEngine.newVoucher</span></span>|
|<span data-ttu-id="52a2c-257">LedgerJournalPeriodicCopy.journalTransCopy</span><span class="sxs-lookup"><span data-stu-id="52a2c-257">LedgerJournalPeriodicCopy.journalTransCopy</span></span>|
|<span data-ttu-id="52a2c-258">LedgerJournalTrans.checkVATTransaction</span><span class="sxs-lookup"><span data-stu-id="52a2c-258">LedgerJournalTrans.checkVATTransaction</span></span>|
|<span data-ttu-id="52a2c-259">LedgerJournalTrans.checkVatTransaction</span><span class="sxs-lookup"><span data-stu-id="52a2c-259">LedgerJournalTrans.checkVatTransaction</span></span>|
|<span data-ttu-id="52a2c-260">LedgerJournalTrans.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="52a2c-260">LedgerJournalTrans.validateWrite_Server</span></span>|
|<span data-ttu-id="52a2c-261">LedgerJournalTrans_Project.checkCategoryId</span><span class="sxs-lookup"><span data-stu-id="52a2c-261">LedgerJournalTrans_Project.checkCategoryId</span></span>|
|<span data-ttu-id="52a2c-262">LedgerJournalTransUpdateAsset</span><span class="sxs-lookup"><span data-stu-id="52a2c-262">LedgerJournalTransUpdateAsset</span></span>|
|<span data-ttu-id="52a2c-263">LedgerJournalTransUpdateLedger.updateNow</span><span class="sxs-lookup"><span data-stu-id="52a2c-263">LedgerJournalTransUpdateLedger.updateNow</span></span>|
|<span data-ttu-id="52a2c-264">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-264">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span></span>|
|<span data-ttu-id="52a2c-265">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-265">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span></span>|
|<span data-ttu-id="52a2c-266">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-266">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span></span>|
|<span data-ttu-id="52a2c-267">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-267">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span></span>|
|<span data-ttu-id="52a2c-268">LedgerJournalTransVoucherTemplates.SaveVoucherTemplate、CreateVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-268">LedgerJournalTransVoucherTemplates.SaveVoucherTemplate, CreateVoucherTemplate</span></span>|
|<span data-ttu-id="52a2c-269">LedgerPostingGeneralJournalController.addLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-269">LedgerPostingGeneralJournalController.addLine</span></span>|
|<span data-ttu-id="52a2c-270">LedgerPostingGeneralJournalController.getLineValues</span><span class="sxs-lookup"><span data-stu-id="52a2c-270">LedgerPostingGeneralJournalController.getLineValues</span></span>|
|<span data-ttu-id="52a2c-271">LedgerTransferOpening.getMainAccountStorageSegment</span><span class="sxs-lookup"><span data-stu-id="52a2c-271">LedgerTransferOpening.getMainAccountStorageSegment</span></span>|
|<span data-ttu-id="52a2c-272">LedgerTransferOpening.processNewClosingRecordsForOpening</span><span class="sxs-lookup"><span data-stu-id="52a2c-272">LedgerTransferOpening.processNewClosingRecordsForOpening</span></span>|
|<span data-ttu-id="52a2c-273">LedgerTransferOpening.processQueryForPublicSector</span><span class="sxs-lookup"><span data-stu-id="52a2c-273">LedgerTransferOpening.processQueryForPublicSector</span></span>|
|<span data-ttu-id="52a2c-274">LedgerTransModule.tax</span><span class="sxs-lookup"><span data-stu-id="52a2c-274">LedgerTransModule.tax</span></span>|
|<span data-ttu-id="52a2c-275">LedgerVoucherObject.allocateTransaction</span><span class="sxs-lookup"><span data-stu-id="52a2c-275">LedgerVoucherObject.allocateTransaction</span></span>|
|<span data-ttu-id="52a2c-276">LedgerVoucherObject.updateLedgerPostingJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-276">LedgerVoucherObject.updateLedgerPostingJournal</span></span>|
|<span data-ttu-id="52a2c-277">LogisticsEntityLocationFormHandler.manageControls</span><span class="sxs-lookup"><span data-stu-id="52a2c-277">LogisticsEntityLocationFormHandler.manageControls</span></span>|
|<span data-ttu-id="52a2c-278">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span><span class="sxs-lookup"><span data-stu-id="52a2c-278">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span></span>|
|<span data-ttu-id="52a2c-279">MainAccount.canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="52a2c-279">MainAccount.canSubmitToWorkflow</span></span>|
|<span data-ttu-id="52a2c-280">可能であれば変数宣言を最初の割り当てに移動</span><span class="sxs-lookup"><span data-stu-id="52a2c-280">Move variable declaration to first assignment when possible</span></span>|
|<span data-ttu-id="52a2c-281">NewElement.NewMethod</span><span class="sxs-lookup"><span data-stu-id="52a2c-281">NewElement.NewMethod</span></span>|
|<span data-ttu-id="52a2c-282">OmOperatingUnit.getDimensionViewId</span><span class="sxs-lookup"><span data-stu-id="52a2c-282">OmOperatingUnit.getDimensionViewId</span></span>|
|<span data-ttu-id="52a2c-283">Originaldocuments.findFromCustTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-283">Originaldocuments.findFromCustTrans</span></span>|
|<span data-ttu-id="52a2c-284">Originaldocuments.findFromGeneralJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-284">Originaldocuments.findFromGeneralJournal</span></span>|
|<span data-ttu-id="52a2c-285">PaymSchedCalc.createCustVendTransaction</span><span class="sxs-lookup"><span data-stu-id="52a2c-285">PaymSchedCalc.createCustVendTransaction</span></span>|
|<span data-ttu-id="52a2c-286">PaymSchedCalc.initFromPurchTotals</span><span class="sxs-lookup"><span data-stu-id="52a2c-286">PaymSchedCalc.initFromPurchTotals</span></span>|
|<span data-ttu-id="52a2c-287">PaymSchedCalc.initFromSalesTotals</span><span class="sxs-lookup"><span data-stu-id="52a2c-287">PaymSchedCalc.initFromSalesTotals</span></span>|
|<span data-ttu-id="52a2c-288">POSApidts.NewTrigger</span><span class="sxs-lookup"><span data-stu-id="52a2c-288">POSApidts.NewTrigger</span></span>|
|<span data-ttu-id="52a2c-289">PosAPidts.NewTrigger</span><span class="sxs-lookup"><span data-stu-id="52a2c-289">PosAPidts.NewTrigger</span></span>|
|<span data-ttu-id="52a2c-290">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span><span class="sxs-lookup"><span data-stu-id="52a2c-290">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span></span>|
|<span data-ttu-id="52a2c-291">PriceDiscAdmCheckPost.runFromContract</span><span class="sxs-lookup"><span data-stu-id="52a2c-291">PriceDiscAdmCheckPost.runFromContract</span></span>|
|<span data-ttu-id="52a2c-292">PriceDiscTable.buildSearchFilter</span><span class="sxs-lookup"><span data-stu-id="52a2c-292">PriceDiscTable.buildSearchFilter</span></span>|
|<span data-ttu-id="52a2c-293">PrintableReceipt</span><span class="sxs-lookup"><span data-stu-id="52a2c-293">PrintableReceipt</span></span>|
|<span data-ttu-id="52a2c-294">ProjAdjustmentUpdate.newPostAdjustment</span><span class="sxs-lookup"><span data-stu-id="52a2c-294">ProjAdjustmentUpdate.newPostAdjustment</span></span>|
|<span data-ttu-id="52a2c-295">ProjAdjustmentUpdate.projTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-295">ProjAdjustmentUpdate.projTrans</span></span>|
|<span data-ttu-id="52a2c-296">ProjAdjustmentUpdate.transEmplNew</span><span class="sxs-lookup"><span data-stu-id="52a2c-296">ProjAdjustmentUpdate.transEmplNew</span></span>|
|<span data-ttu-id="52a2c-297">ProjAdjustmentUpdate_Post.Post</span><span class="sxs-lookup"><span data-stu-id="52a2c-297">ProjAdjustmentUpdate_Post.Post</span></span>|
|<span data-ttu-id="52a2c-298">ProjAdjustmentUpdate_Post.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-298">ProjAdjustmentUpdate_Post.update</span></span>|
|<span data-ttu-id="52a2c-299">ProjBudgetManager.createBudgetRevenueForecast、createBudgetSalesForecast</span><span class="sxs-lookup"><span data-stu-id="52a2c-299">ProjBudgetManager.createBudgetRevenueForecast, createBudgetSalesForecast</span></span>|
|<span data-ttu-id="52a2c-300">ProjBudgetManager.insertProjBudgetLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-300">ProjBudgetManager.insertProjBudgetLine</span></span>|
|<span data-ttu-id="52a2c-301">ProjBudgetManager.insertProjBudgetLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-301">ProjBudgetManager.insertProjBudgetLine</span></span>|
|<span data-ttu-id="52a2c-302">ProjBudgetManager.updateProjBudgetLinesWithAmt</span><span class="sxs-lookup"><span data-stu-id="52a2c-302">ProjBudgetManager.updateProjBudgetLinesWithAmt</span></span>|
|<span data-ttu-id="52a2c-303">ProjCategory.categoryType2CategoryEmplOption</span><span class="sxs-lookup"><span data-stu-id="52a2c-303">ProjCategory.categoryType2CategoryEmplOption</span></span>|
|<span data-ttu-id="52a2c-304">ProjCategory.categoryType2CategoryEmplOption</span><span class="sxs-lookup"><span data-stu-id="52a2c-304">ProjCategory.categoryType2CategoryEmplOption</span></span>|
|<span data-ttu-id="52a2c-305">ProjCategory.categoryType2TransType</span><span class="sxs-lookup"><span data-stu-id="52a2c-305">ProjCategory.categoryType2TransType</span></span>|
|<span data-ttu-id="52a2c-306">Projcategory.transType2CategoryType</span><span class="sxs-lookup"><span data-stu-id="52a2c-306">Projcategory.transType2CategoryType</span></span>|
|<span data-ttu-id="52a2c-307">Projcontrol.categoryType2CostType</span><span class="sxs-lookup"><span data-stu-id="52a2c-307">Projcontrol.categoryType2CostType</span></span>|
|<span data-ttu-id="52a2c-308">Projcontrol.costType2CategoryType</span><span class="sxs-lookup"><span data-stu-id="52a2c-308">Projcontrol.costType2CategoryType</span></span>|
|<span data-ttu-id="52a2c-309">ProjControlPosting.insertControlTrans、processSalesValue</span><span class="sxs-lookup"><span data-stu-id="52a2c-309">ProjControlPosting.insertControlTrans, processSalesValue</span></span>|
|<span data-ttu-id="52a2c-310">ProjectSourceDocumentLineItemHelper.projOrigin および projTransType</span><span class="sxs-lookup"><span data-stu-id="52a2c-310">ProjectSourceDocumentLineItemHelper.projOrigin and projTransType</span></span>|
|<span data-ttu-id="52a2c-311">ProjForecastListPageInteraction.runForcastFormBasedOnForecastUnion</span><span class="sxs-lookup"><span data-stu-id="52a2c-311">ProjForecastListPageInteraction.runForcastFormBasedOnForecastUnion</span></span>|
|<span data-ttu-id="52a2c-312">ProjForecastReduce.newProjPost</span><span class="sxs-lookup"><span data-stu-id="52a2c-312">ProjForecastReduce.newProjPost</span></span>|
|<span data-ttu-id="52a2c-313">ProjFormLetter メソッド main/mainOnServer</span><span class="sxs-lookup"><span data-stu-id="52a2c-313">ProjFormLetter method main/mainOnServer</span></span>|
|<span data-ttu-id="52a2c-314">ProjInvoiceCancel.cancelProposal</span><span class="sxs-lookup"><span data-stu-id="52a2c-314">ProjInvoiceCancel.cancelProposal</span></span>|
|<span data-ttu-id="52a2c-315">ProjInvoiceChoose.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-315">ProjInvoiceChoose.run</span></span>|
|<span data-ttu-id="52a2c-316">ProjInvoiceJournalCreate.createJournalHeader</span><span class="sxs-lookup"><span data-stu-id="52a2c-316">ProjInvoiceJournalCreate.createJournalHeader</span></span>|
|<span data-ttu-id="52a2c-317">ProjInvoiceLines.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-317">ProjInvoiceLines.run</span></span>|
|<span data-ttu-id="52a2c-318">ProjInvoiceProposalCreateLines.loadLastValue</span><span class="sxs-lookup"><span data-stu-id="52a2c-318">ProjInvoiceProposalCreateLines.loadLastValue</span></span>|
|<span data-ttu-id="52a2c-319">ProjInvoiceProposalCreateLines.runItemQuery</span><span class="sxs-lookup"><span data-stu-id="52a2c-319">ProjInvoiceProposalCreateLines.runItemQuery</span></span>|
|<span data-ttu-id="52a2c-320">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-320">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="52a2c-321">ProjInvoiceProposalInsertLines.setProjProposalJour</span><span class="sxs-lookup"><span data-stu-id="52a2c-321">ProjInvoiceProposalInsertLines.setProjProposalJour</span></span>|
|<span data-ttu-id="52a2c-322">ProjInvoiceProposalInsertLines.setProjProposalJour</span><span class="sxs-lookup"><span data-stu-id="52a2c-322">ProjInvoiceProposalInsertLines.setProjProposalJour</span></span>|
|<span data-ttu-id="52a2c-323">ProjInvoiceProposalInsertLines.setProjProposalTotals</span><span class="sxs-lookup"><span data-stu-id="52a2c-323">ProjInvoiceProposalInsertLines.setProjProposalTotals</span></span>|
|<span data-ttu-id="52a2c-324">ProjInvoiceTableCreate.initializeValues</span><span class="sxs-lookup"><span data-stu-id="52a2c-324">ProjInvoiceTableCreate.initializeValues</span></span>|
|<span data-ttu-id="52a2c-325">Projparameters.defaultProjCategory</span><span class="sxs-lookup"><span data-stu-id="52a2c-325">Projparameters.defaultProjCategory</span></span>|
|<span data-ttu-id="52a2c-326">ProjPeriodPostingLedgerCost.updateTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-326">ProjPeriodPostingLedgerCost.updateTrans</span></span>|
|<span data-ttu-id="52a2c-327">ProjPost.newCheckTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-327">ProjPost.newCheckTrans</span></span>|
|<span data-ttu-id="52a2c-328">Projpost.newCreateProjTransAndLedger</span><span class="sxs-lookup"><span data-stu-id="52a2c-328">Projpost.newCreateProjTransAndLedger</span></span>|
|<span data-ttu-id="52a2c-329">Projpost.newCreateProjTransAndLedgerAdj</span><span class="sxs-lookup"><span data-stu-id="52a2c-329">Projpost.newCreateProjTransAndLedgerAdj</span></span>|
|<span data-ttu-id="52a2c-330">Projpost.newTransAdjNegativeJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-330">Projpost.newTransAdjNegativeJournal</span></span>|
|<span data-ttu-id="52a2c-331">Projpost.postcost</span><span class="sxs-lookup"><span data-stu-id="52a2c-331">Projpost.postcost</span></span>|
|<span data-ttu-id="52a2c-332">ProjSalesItemReq.modified</span><span class="sxs-lookup"><span data-stu-id="52a2c-332">ProjSalesItemReq.modified</span></span>|
|<span data-ttu-id="52a2c-333">ProjSplitBill.transType</span><span class="sxs-lookup"><span data-stu-id="52a2c-333">ProjSplitBill.transType</span></span>|
|<span data-ttu-id="52a2c-334">ProjSplitBill.transType</span><span class="sxs-lookup"><span data-stu-id="52a2c-334">ProjSplitBill.transType</span></span>|
|<span data-ttu-id="52a2c-335">ProjTable.generateNextSubProjectId</span><span class="sxs-lookup"><span data-stu-id="52a2c-335">ProjTable.generateNextSubProjectId</span></span>|
|<span data-ttu-id="52a2c-336">ProjTableCreate.canClose</span><span class="sxs-lookup"><span data-stu-id="52a2c-336">ProjTableCreate.canClose</span></span>|
|<span data-ttu-id="52a2c-337">ProjTableLookup.isJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-337">ProjTableLookup.isJournal</span></span>|
|<span data-ttu-id="52a2c-338">ProjTableWizardCtrl.createProject</span><span class="sxs-lookup"><span data-stu-id="52a2c-338">ProjTableWizardCtrl.createProject</span></span>|
|<span data-ttu-id="52a2c-339">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="52a2c-339">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="52a2c-340">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="52a2c-340">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="52a2c-341">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="52a2c-341">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="52a2c-342">PSAProjRetainerInvoicing.run</span><span class="sxs-lookup"><span data-stu-id="52a2c-342">PSAProjRetainerInvoicing.run</span></span>|
|<span data-ttu-id="52a2c-343">PsaQuotationsController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="52a2c-343">PsaQuotationsController.getReportTitle</span></span>|
|<span data-ttu-id="52a2c-344">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="52a2c-344">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="52a2c-345">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="52a2c-345">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="52a2c-346">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="52a2c-346">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="52a2c-347">PurchAutoCreate_Sales.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-347">PurchAutoCreate_Sales.createPurchTable</span></span>|
|<span data-ttu-id="52a2c-348">PurchAutoCreate_Sales.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-348">PurchAutoCreate_Sales.setPurchTable</span></span>|
|<span data-ttu-id="52a2c-349">PurchCalcTax_Invoice.updateTaxWriteCode</span><span class="sxs-lookup"><span data-stu-id="52a2c-349">PurchCalcTax_Invoice.updateTaxWriteCode</span></span>|
|<span data-ttu-id="52a2c-350">PurchCopying.copyLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-350">PurchCopying.copyLine</span></span>|
|<span data-ttu-id="52a2c-351">PurchCreateFromSalesOrder.autoCreatePurchOrder</span><span class="sxs-lookup"><span data-stu-id="52a2c-351">PurchCreateFromSalesOrder.autoCreatePurchOrder</span></span>|
|<span data-ttu-id="52a2c-352">PurchFormletter_Invoice.newinvoice</span><span class="sxs-lookup"><span data-stu-id="52a2c-352">PurchFormletter_Invoice.newinvoice</span></span>|
|<span data-ttu-id="52a2c-353">PurchFormletter_Packingslip.runProjectPostings</span><span class="sxs-lookup"><span data-stu-id="52a2c-353">PurchFormletter_Packingslip.runProjectPostings</span></span>|
|<span data-ttu-id="52a2c-354">PurchFormletterParmData.createParmLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-354">PurchFormletterParmData.createParmLine</span></span>|
|<span data-ttu-id="52a2c-355">PurchFormletterParmData.newData</span><span class="sxs-lookup"><span data-stu-id="52a2c-355">PurchFormletterParmData.newData</span></span>|
|<span data-ttu-id="52a2c-356">PurchFormLetterParmData.reSelectLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-356">PurchFormLetterParmData.reSelectLines</span></span>|
|<span data-ttu-id="52a2c-357">PurchFormletterParmDataInvoice.chooseLinesNext</span><span class="sxs-lookup"><span data-stu-id="52a2c-357">PurchFormletterParmDataInvoice.chooseLinesNext</span></span>|
|<span data-ttu-id="52a2c-358">PurchFormletterParmDataInvoice.cleanupChooseLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-358">PurchFormletterParmDataInvoice.cleanupChooseLines</span></span>|
|<span data-ttu-id="52a2c-359">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span><span class="sxs-lookup"><span data-stu-id="52a2c-359">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span></span>|
|<span data-ttu-id="52a2c-360">PurchFormletterParmDataInvoice.processAdditional</span><span class="sxs-lookup"><span data-stu-id="52a2c-360">PurchFormletterParmDataInvoice.processAdditional</span></span>|
|<span data-ttu-id="52a2c-361">PurchFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-361">PurchFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="52a2c-362">PurchInvoiceJournalCreate.checkInvoice</span><span class="sxs-lookup"><span data-stu-id="52a2c-362">PurchInvoiceJournalCreate.checkInvoice</span></span>|
|<span data-ttu-id="52a2c-363">PurchInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="52a2c-363">PurchInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="52a2c-364">PurchLine.delete</span><span class="sxs-lookup"><span data-stu-id="52a2c-364">PurchLine.delete</span></span>|
|<span data-ttu-id="52a2c-365">PurchLine.setProjSalesPrice</span><span class="sxs-lookup"><span data-stu-id="52a2c-365">PurchLine.setProjSalesPrice</span></span>|
|<span data-ttu-id="52a2c-366">PurchLine.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-366">PurchLine.update</span></span>|
|<span data-ttu-id="52a2c-367">PurchLine.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="52a2c-367">PurchLine.validateWrite_Server</span></span>|
|<span data-ttu-id="52a2c-368">PurchLineCopy.canClose</span><span class="sxs-lookup"><span data-stu-id="52a2c-368">PurchLineCopy.canClose</span></span>|
|<span data-ttu-id="52a2c-369">PurchLineType.syncSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-369">PurchLineType.syncSalesLine</span></span>|
|<span data-ttu-id="52a2c-370">PurchLineType.updateInventory</span><span class="sxs-lookup"><span data-stu-id="52a2c-370">PurchLineType.updateInventory</span></span>|
|<span data-ttu-id="52a2c-371">PurchLineType.updatePurchStatus</span><span class="sxs-lookup"><span data-stu-id="52a2c-371">PurchLineType.updatePurchStatus</span></span>|
|<span data-ttu-id="52a2c-372">PurchLineType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="52a2c-372">PurchLineType.validateDelete</span></span>|
|<span data-ttu-id="52a2c-373">PurchPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="52a2c-373">PurchPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="52a2c-374">PurchPackingSlipJournalPost.updateSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-374">PurchPackingSlipJournalPost.updateSalesLine</span></span>|
|<span data-ttu-id="52a2c-375">PurchPackingSlipJournalPost.updateSalesTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-375">PurchPackingSlipJournalPost.updateSalesTable</span></span>|
|<span data-ttu-id="52a2c-376">PurchPackingSlipJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-376">PurchPackingSlipJournalPost.updateSourceLine</span></span>|
|<span data-ttu-id="52a2c-377">PurchQuantity_PackingSlip.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="52a2c-377">PurchQuantity_PackingSlip.calcQtyInvent</span></span>|
|<span data-ttu-id="52a2c-378">PurchQuantity_PackingSlip.calcQtyPurch</span><span class="sxs-lookup"><span data-stu-id="52a2c-378">PurchQuantity_PackingSlip.calcQtyPurch</span></span>|
|<span data-ttu-id="52a2c-379">PurchReqAddItems.init</span><span class="sxs-lookup"><span data-stu-id="52a2c-379">PurchReqAddItems.init</span></span>|
|<span data-ttu-id="52a2c-380">PurchReqTable.init</span><span class="sxs-lookup"><span data-stu-id="52a2c-380">PurchReqTable.init</span></span>|
|<span data-ttu-id="52a2c-381">PurchReqWFExpendiParticipantProvider.resolve</span><span class="sxs-lookup"><span data-stu-id="52a2c-381">PurchReqWFExpendiParticipantProvider.resolve</span></span>|
|<span data-ttu-id="52a2c-382">PurchSelectLinesManager.mark</span><span class="sxs-lookup"><span data-stu-id="52a2c-382">PurchSelectLinesManager.mark</span></span>|
|<span data-ttu-id="52a2c-383">PurchTableForm.purchLine_WritePreSuper</span><span class="sxs-lookup"><span data-stu-id="52a2c-383">PurchTableForm.purchLine_WritePreSuper</span></span>|
|<span data-ttu-id="52a2c-384">PurchTableInteractionHelper.getDeliveryScheduleEnabled</span><span class="sxs-lookup"><span data-stu-id="52a2c-384">PurchTableInteractionHelper.getDeliveryScheduleEnabled</span></span>|
|<span data-ttu-id="52a2c-385">PurchTableInteractionHelper.getHasMultipleDeliveries</span><span class="sxs-lookup"><span data-stu-id="52a2c-385">PurchTableInteractionHelper.getHasMultipleDeliveries</span></span>|
|<span data-ttu-id="52a2c-386">PurchUpdateRemain.updateRemainPhysical</span><span class="sxs-lookup"><span data-stu-id="52a2c-386">PurchUpdateRemain.updateRemainPhysical</span></span>|
|<span data-ttu-id="52a2c-387">ReqCalc.insertItemInventSum</span><span class="sxs-lookup"><span data-stu-id="52a2c-387">ReqCalc.insertItemInventSum</span></span>|
|<span data-ttu-id="52a2c-388">ReqTransPlanIdFilter.setPlanIdOnQueryRange</span><span class="sxs-lookup"><span data-stu-id="52a2c-388">ReqTransPlanIdFilter.setPlanIdOnQueryRange</span></span>|
|<span data-ttu-id="52a2c-389">ReqTransPoMarkFirm.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-389">ReqTransPoMarkFirm.createPurchLine</span></span>|
|<span data-ttu-id="52a2c-390">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-390">ReqTransPoMarkFirm.createPurchTable</span></span>|
|<span data-ttu-id="52a2c-391">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-391">ReqTransPoMarkFirm.createPurchTable</span></span>|
|<span data-ttu-id="52a2c-392">ReqTransPoMarkFirm.dialog</span><span class="sxs-lookup"><span data-stu-id="52a2c-392">ReqTransPoMarkFirm.dialog</span></span>|
|<span data-ttu-id="52a2c-393">RetailAssortmentLookupTask.CreateChannelGroups</span><span class="sxs-lookup"><span data-stu-id="52a2c-393">RetailAssortmentLookupTask.CreateChannelGroups</span></span>|
|<span data-ttu-id="52a2c-394">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span><span class="sxs-lookup"><span data-stu-id="52a2c-394">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span></span>|
|<span data-ttu-id="52a2c-395">RetailPackage.close</span><span class="sxs-lookup"><span data-stu-id="52a2c-395">RetailPackage.close</span></span>|
|<span data-ttu-id="52a2c-396">RetailProductPropertyManager.saveProductDimensions</span><span class="sxs-lookup"><span data-stu-id="52a2c-396">RetailProductPropertyManager.saveProductDimensions</span></span>|
|<span data-ttu-id="52a2c-397">RetailStatementPostChecker::checkStatement</span><span class="sxs-lookup"><span data-stu-id="52a2c-397">RetailStatementPostChecker::checkStatement</span></span>|
|<span data-ttu-id="52a2c-398">ReturnTable.isDispositionCodeValid</span><span class="sxs-lookup"><span data-stu-id="52a2c-398">ReturnTable.isDispositionCodeValid</span></span>|
|<span data-ttu-id="52a2c-399">RouteCopyToRoute</span><span class="sxs-lookup"><span data-stu-id="52a2c-399">RouteCopyToRoute</span></span>|
|<span data-ttu-id="52a2c-400">SalesCalcAvailableDlvDates.newCommonSalesDlvDateType</span><span class="sxs-lookup"><span data-stu-id="52a2c-400">SalesCalcAvailableDlvDates.newCommonSalesDlvDateType</span></span>|
|<span data-ttu-id="52a2c-401">SalesCalcAvailableDlvDates.newCommonSalesDlvDateTypeByEntity</span><span class="sxs-lookup"><span data-stu-id="52a2c-401">SalesCalcAvailableDlvDates.newCommonSalesDlvDateTypeByEntity</span></span>|
|<span data-ttu-id="52a2c-402">SalesCopying.copyLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-402">SalesCopying.copyLines</span></span>|
|<span data-ttu-id="52a2c-403">SalesEditLines.FormDesign/FormMenuFunctionButtonControl/ButtonPaymentSched/Method/clicked</span><span class="sxs-lookup"><span data-stu-id="52a2c-403">SalesEditLines.FormDesign/FormMenuFunctionButtonControl/ButtonPaymentSched/Method/clicked</span></span>|
|<span data-ttu-id="52a2c-404">SalesFormLetter.onCreatePaymSched</span><span class="sxs-lookup"><span data-stu-id="52a2c-404">SalesFormLetter.onCreatePaymSched</span></span>|
|<span data-ttu-id="52a2c-405">SalesFormLetterParmDataPackingSlip.selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-405">SalesFormLetterParmDataPackingSlip.selectChooseLines</span></span>|
|<span data-ttu-id="52a2c-406">SalesFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-406">SalesFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="52a2c-407">SalesFormletterProvider.checkSalesLineChanged</span><span class="sxs-lookup"><span data-stu-id="52a2c-407">SalesFormletterProvider.checkSalesLineChanged</span></span>|
|<span data-ttu-id="52a2c-408">SalesInvoiceController.initFormLetterReport</span><span class="sxs-lookup"><span data-stu-id="52a2c-408">SalesInvoiceController.initFormLetterReport</span></span>|
|<span data-ttu-id="52a2c-409">SalesInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="52a2c-409">SalesInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="52a2c-410">SalesInvoiceJournalPostProj.updateInventory</span><span class="sxs-lookup"><span data-stu-id="52a2c-410">SalesInvoiceJournalPostProj.updateInventory</span></span>|
|<span data-ttu-id="52a2c-411">SalesLine.createAlternativeItem</span><span class="sxs-lookup"><span data-stu-id="52a2c-411">SalesLine.createAlternativeItem</span></span>|
|<span data-ttu-id="52a2c-412">SalesLine.delete</span><span class="sxs-lookup"><span data-stu-id="52a2c-412">SalesLine.delete</span></span>|
|<span data-ttu-id="52a2c-413">SalesLine.returnLineUpdate</span><span class="sxs-lookup"><span data-stu-id="52a2c-413">SalesLine.returnLineUpdate</span></span>|
|<span data-ttu-id="52a2c-414">SalesLineCopy.canClose</span><span class="sxs-lookup"><span data-stu-id="52a2c-414">SalesLineCopy.canClose</span></span>|
|<span data-ttu-id="52a2c-415">SalesLineType.initFromCustInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="52a2c-415">SalesLineType.initFromCustInvoiceTrans</span></span>|
|<span data-ttu-id="52a2c-416">SalesOrderEntryStatistics.createOrderEntry</span><span class="sxs-lookup"><span data-stu-id="52a2c-416">SalesOrderEntryStatistics.createOrderEntry</span></span>|
|<span data-ttu-id="52a2c-417">SalesOrderEntryStatistics.deleteOrderEntry</span><span class="sxs-lookup"><span data-stu-id="52a2c-417">SalesOrderEntryStatistics.deleteOrderEntry</span></span>|
|<span data-ttu-id="52a2c-418">SalesPackingSlipDP.itemId</span><span class="sxs-lookup"><span data-stu-id="52a2c-418">SalesPackingSlipDP.itemId</span></span>|
|<span data-ttu-id="52a2c-419">SalesPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="52a2c-419">SalesPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="52a2c-420">SalesParmLine.setQty</span><span class="sxs-lookup"><span data-stu-id="52a2c-420">SalesParmLine.setQty</span></span>|
|<span data-ttu-id="52a2c-421">SalesQuantity_Invoice.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="52a2c-421">SalesQuantity_Invoice.calcQtyInvent</span></span>|
|<span data-ttu-id="52a2c-422">SalesQuantity_Invoice.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="52a2c-422">SalesQuantity_Invoice.calcQtySales</span></span>|
|<span data-ttu-id="52a2c-423">SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-423">SalesQuotationEditLinesForm_Sales_Confir method createSalesLines</span></span>|
|<span data-ttu-id="52a2c-424">SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-424">SalesQuotationEditLinesForm_Sales_Confir method createSalesTable</span></span>|
|<span data-ttu-id="52a2c-425">SalesQuotationEditLinesForm_Sales_Confir.createSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-425">SalesQuotationEditLinesForm_Sales_Confir.createSalesLine</span></span>|
|<span data-ttu-id="52a2c-426">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span><span class="sxs-lookup"><span data-stu-id="52a2c-426">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span></span>|
|<span data-ttu-id="52a2c-427">SalesQuotationLine.createLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-427">SalesQuotationLine.createLine</span></span>|
|<span data-ttu-id="52a2c-428">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-428">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="52a2c-429">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-429">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="52a2c-430">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="52a2c-430">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="52a2c-431">SalesQuotationLine.delete</span><span class="sxs-lookup"><span data-stu-id="52a2c-431">SalesQuotationLine.delete</span></span>|
|<span data-ttu-id="52a2c-432">SalesQuotationLine.setCostSalesPrice</span><span class="sxs-lookup"><span data-stu-id="52a2c-432">SalesQuotationLine.setCostSalesPrice</span></span>|
|<span data-ttu-id="52a2c-433">SalesQuotationLine.updateSalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-433">SalesQuotationLine.updateSalesQuotationTable</span></span>|
|<span data-ttu-id="52a2c-434">SalesQuotationListPageInteraction.initIsSalesQuotation</span><span class="sxs-lookup"><span data-stu-id="52a2c-434">SalesQuotationListPageInteraction.initIsSalesQuotation</span></span>|
|<span data-ttu-id="52a2c-435">SalesQuotationListPageInteraction.setButtonFollowup</span><span class="sxs-lookup"><span data-stu-id="52a2c-435">SalesQuotationListPageInteraction.setButtonFollowup</span></span>|
|<span data-ttu-id="52a2c-436">SalesQuotationListPageInteraction.setButtonQuotation</span><span class="sxs-lookup"><span data-stu-id="52a2c-436">SalesQuotationListPageInteraction.setButtonQuotation</span></span>|
|<span data-ttu-id="52a2c-437">SalesQuotationTableForm_DlvSchedule.updateSalesQuotationLineTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-437">SalesQuotationTableForm_DlvSchedule.updateSalesQuotationLineTable</span></span>|
|<span data-ttu-id="52a2c-438">SalesQuotationTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="52a2c-438">SalesQuotationTableType.validateDelete</span></span>|
|<span data-ttu-id="52a2c-439">SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-439">SalesTable.update</span></span>|
|<span data-ttu-id="52a2c-440">SalesTableForm_DeliverySchedule.updateSalesLineTable</span><span class="sxs-lookup"><span data-stu-id="52a2c-440">SalesTableForm_DeliverySchedule.updateSalesLineTable</span></span>|
|<span data-ttu-id="52a2c-441">SalesTableForm_ProjectSalesItem.resetSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-441">SalesTableForm_ProjectSalesItem.resetSalesLine</span></span>|
|<span data-ttu-id="52a2c-442">SalesTableInteractionHelper.isOpenOrderNotReturnNotProjectRelatedSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-442">SalesTableInteractionHelper.isOpenOrderNotReturnNotProjectRelatedSalesLine</span></span>|
|<span data-ttu-id="52a2c-443">SalesTableInteractionHelper.notPartiallyPickedPackedOrInvoiced</span><span class="sxs-lookup"><span data-stu-id="52a2c-443">SalesTableInteractionHelper.notPartiallyPickedPackedOrInvoiced</span></span>|
|<span data-ttu-id="52a2c-444">SalesTableInteractionHelper.notReservedOrderedNorPhysical</span><span class="sxs-lookup"><span data-stu-id="52a2c-444">SalesTableInteractionHelper.notReservedOrderedNorPhysical</span></span>|
|<span data-ttu-id="52a2c-445">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="52a2c-445">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="52a2c-446">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="52a2c-446">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="52a2c-447">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="52a2c-447">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="52a2c-448">SalesTaxDeclarationInformationReportService.processReport</span><span class="sxs-lookup"><span data-stu-id="52a2c-448">SalesTaxDeclarationInformationReportService.processReport</span></span>|
|<span data-ttu-id="52a2c-449">SettlementPair_Vend.fetchPayment</span><span class="sxs-lookup"><span data-stu-id="52a2c-449">SettlementPair_Vend.fetchPayment</span></span>|
|<span data-ttu-id="52a2c-450">smmActivityParentLinkTable.insert</span><span class="sxs-lookup"><span data-stu-id="52a2c-450">smmActivityParentLinkTable.insert</span></span>|
|<span data-ttu-id="52a2c-451">smmBusRelTable.convert2Customer</span><span class="sxs-lookup"><span data-stu-id="52a2c-451">smmBusRelTable.convert2Customer</span></span>|
|<span data-ttu-id="52a2c-452">smmBusRelTable.convert2Customer</span><span class="sxs-lookup"><span data-stu-id="52a2c-452">smmBusRelTable.convert2Customer</span></span>|
|<span data-ttu-id="52a2c-453">SmmBusRelTable.convert2Vendor</span><span class="sxs-lookup"><span data-stu-id="52a2c-453">SmmBusRelTable.convert2Vendor</span></span>|
|<span data-ttu-id="52a2c-454">SmmBusRelTable.convert2Vendor</span><span class="sxs-lookup"><span data-stu-id="52a2c-454">SmmBusRelTable.convert2Vendor</span></span>|
|<span data-ttu-id="52a2c-455">smmBusRelTable.createConvertedBusRel</span><span class="sxs-lookup"><span data-stu-id="52a2c-455">smmBusRelTable.createConvertedBusRel</span></span>|
|<span data-ttu-id="52a2c-456">smmLeadTable.createBusRelRecord</span><span class="sxs-lookup"><span data-stu-id="52a2c-456">smmLeadTable.createBusRelRecord</span></span>|
|<span data-ttu-id="52a2c-457">SmmProjectCreate.createProjectGroup</span><span class="sxs-lookup"><span data-stu-id="52a2c-457">SmmProjectCreate.createProjectGroup</span></span>|
|<span data-ttu-id="52a2c-458">SpecTransInsertSetManager.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="52a2c-458">SpecTransInsertSetManager.insertDatabase</span></span>|
|<span data-ttu-id="52a2c-459">SubledgerJournalizerProjectExtension.createProjectActualCostDetail、createProjectActualHeader</span><span class="sxs-lookup"><span data-stu-id="52a2c-459">SubledgerJournalizerProjectExtension.createProjectActualCostDetail, createProjectActualHeader</span></span>|
|<span data-ttu-id="52a2c-460">SubledgerJournalizerProjectExtension.getProjectActualMap</span><span class="sxs-lookup"><span data-stu-id="52a2c-460">SubledgerJournalizerProjectExtension.getProjectActualMap</span></span>|
|<span data-ttu-id="52a2c-461">SuppItemSales.initSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-461">SuppItemSales.initSalesLine</span></span>|
|<span data-ttu-id="52a2c-462">テーブル PurchLine.insert</span><span class="sxs-lookup"><span data-stu-id="52a2c-462">Table PurchLine.insert</span></span>|
|<span data-ttu-id="52a2c-463">テーブル PurchLine.insert</span><span class="sxs-lookup"><span data-stu-id="52a2c-463">Table PurchLine.insert</span></span>|
|<span data-ttu-id="52a2c-464">テーブル PurchLine.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-464">Table PurchLine.update</span></span>|
|<span data-ttu-id="52a2c-465">テーブル PurchTable.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-465">Table PurchTable.update</span></span>|
|<span data-ttu-id="52a2c-466">テーブル PurchTable.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-466">Table PurchTable.update</span></span>|
|<span data-ttu-id="52a2c-467">テーブル SalesLine.insert</span><span class="sxs-lookup"><span data-stu-id="52a2c-467">Table SalesLine.insert</span></span>|
|<span data-ttu-id="52a2c-468">テーブル SalesLine.projIdModified</span><span class="sxs-lookup"><span data-stu-id="52a2c-468">table SalesLine.projIdModified</span></span>|
|<span data-ttu-id="52a2c-469">テーブル SalesLine.salesQtyModifiedInteraction</span><span class="sxs-lookup"><span data-stu-id="52a2c-469">table SalesLine.salesQtyModifiedInteraction</span></span>|
|<span data-ttu-id="52a2c-470">テーブル SalesLine.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-470">Table SalesLine.update</span></span>|
|<span data-ttu-id="52a2c-471">テーブル SalesQuotationLine.insert</span><span class="sxs-lookup"><span data-stu-id="52a2c-471">Table SalesQuotationLine.insert</span></span>|
|<span data-ttu-id="52a2c-472">テーブル SalesQuotationLine.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-472">Table SalesQuotationLine.update</span></span>|
|<span data-ttu-id="52a2c-473">テーブル SalesQuotationTable.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-473">Table SalesQuotationTable.update</span></span>|
|<span data-ttu-id="52a2c-474">テーブル SalesQuotationTable.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-474">Table SalesQuotationTable.update</span></span>|
|<span data-ttu-id="52a2c-475">テーブル SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-475">Table SalesTable.update</span></span>|
|<span data-ttu-id="52a2c-476">テーブル SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="52a2c-476">Table SalesTable.update</span></span>|
|<span data-ttu-id="52a2c-477">Table\VendTable.name</span><span class="sxs-lookup"><span data-stu-id="52a2c-477">Table\VendTable.name</span></span>|
|<span data-ttu-id="52a2c-478">Table\VendTable.updateOnHold</span><span class="sxs-lookup"><span data-stu-id="52a2c-478">Table\VendTable.updateOnHold</span></span>|
|<span data-ttu-id="52a2c-479">Tax.createOrphanLinkInsteadPost_RU</span><span class="sxs-lookup"><span data-stu-id="52a2c-479">Tax.createOrphanLinkInsteadPost_RU</span></span>|
|<span data-ttu-id="52a2c-480">Tax.distributeTotalTax</span><span class="sxs-lookup"><span data-stu-id="52a2c-480">Tax.distributeTotalTax</span></span>|
|<span data-ttu-id="52a2c-481">Tax.distributeTotalTax</span><span class="sxs-lookup"><span data-stu-id="52a2c-481">Tax.distributeTotalTax</span></span>|
|<span data-ttu-id="52a2c-482">Tax.InsertIntersection</span><span class="sxs-lookup"><span data-stu-id="52a2c-482">Tax.InsertIntersection</span></span>|
|<span data-ttu-id="52a2c-483">Tax.insertIntersection</span><span class="sxs-lookup"><span data-stu-id="52a2c-483">Tax.insertIntersection</span></span>|
|<span data-ttu-id="52a2c-484">Tax.post</span><span class="sxs-lookup"><span data-stu-id="52a2c-484">Tax.post</span></span>|
|<span data-ttu-id="52a2c-485">Tax.Post</span><span class="sxs-lookup"><span data-stu-id="52a2c-485">Tax.Post</span></span>|
|<span data-ttu-id="52a2c-486">Tax.postCharge</span><span class="sxs-lookup"><span data-stu-id="52a2c-486">Tax.postCharge</span></span>|
|<span data-ttu-id="52a2c-487">Tax.postTaxProjInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="52a2c-487">Tax.postTaxProjInvoice_IN</span></span>|
|<span data-ttu-id="52a2c-488">Tax.postTaxPurchInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="52a2c-488">Tax.postTaxPurchInvoice_IN</span></span>|
|<span data-ttu-id="52a2c-489">Tax.postTaxSalesInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="52a2c-489">Tax.postTaxSalesInvoice_IN</span></span>|
|<span data-ttu-id="52a2c-490">Tax.saveAndPost</span><span class="sxs-lookup"><span data-stu-id="52a2c-490">Tax.saveAndPost</span></span>|
|<span data-ttu-id="52a2c-491">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="52a2c-491">Tax.taxTotals</span></span>|
|<span data-ttu-id="52a2c-492">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="52a2c-492">Tax.taxTotals</span></span>|
|<span data-ttu-id="52a2c-493">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="52a2c-493">Tax.taxTotals</span></span>|
|<span data-ttu-id="52a2c-494">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="52a2c-494">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="52a2c-495">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="52a2c-495">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="52a2c-496">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="52a2c-496">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="52a2c-497">TaxBookSection.checkTaxBookSection</span><span class="sxs-lookup"><span data-stu-id="52a2c-497">TaxBookSection.checkTaxBookSection</span></span>|
|<span data-ttu-id="52a2c-498">TaxCalculationAdjustment.calcManualInserted</span><span class="sxs-lookup"><span data-stu-id="52a2c-498">TaxCalculationAdjustment.calcManualInserted</span></span>|
|<span data-ttu-id="52a2c-499">TaxCalculationJournal.saveTaxTransfers</span><span class="sxs-lookup"><span data-stu-id="52a2c-499">TaxCalculationJournal.saveTaxTransfers</span></span>|
|<span data-ttu-id="52a2c-500">TaxFreeInvoice_Invoice.updateAndPost</span><span class="sxs-lookup"><span data-stu-id="52a2c-500">TaxFreeInvoice_Invoice.updateAndPost</span></span>|
|<span data-ttu-id="52a2c-501">TaxInvoiceSpec.parmTaxSpec</span><span class="sxs-lookup"><span data-stu-id="52a2c-501">TaxInvoiceSpec.parmTaxSpec</span></span>|
|<span data-ttu-id="52a2c-502">TaxListDP.insertTaxListTaxTmpData</span><span class="sxs-lookup"><span data-stu-id="52a2c-502">TaxListDP.insertTaxListTaxTmpData</span></span>|
|<span data-ttu-id="52a2c-503">TaxListDP.updateTaxListTaxTmpData</span><span class="sxs-lookup"><span data-stu-id="52a2c-503">TaxListDP.updateTaxListTaxTmpData</span></span>|
|<span data-ttu-id="52a2c-504">TaxMainAccDimensionListProvider.populateMainAccountDimensionList</span><span class="sxs-lookup"><span data-stu-id="52a2c-504">TaxMainAccDimensionListProvider.populateMainAccountDimensionList</span></span>|
|<span data-ttu-id="52a2c-505">TaxPost.postToLedger</span><span class="sxs-lookup"><span data-stu-id="52a2c-505">TaxPost.postToLedger</span></span>|
|<span data-ttu-id="52a2c-506">TaxReportController_US.init</span><span class="sxs-lookup"><span data-stu-id="52a2c-506">TaxReportController_US.init</span></span>|
|<span data-ttu-id="52a2c-507">TaxReportInclAdjustmentDP.insertTaxReportInclAdjustmentTmp</span><span class="sxs-lookup"><span data-stu-id="52a2c-507">TaxReportInclAdjustmentDP.insertTaxReportInclAdjustmentTmp</span></span>|
|<span data-ttu-id="52a2c-508">TaxReportingDP.insertTaxReportingTmp</span><span class="sxs-lookup"><span data-stu-id="52a2c-508">TaxReportingDP.insertTaxReportingTmp</span></span>|
|<span data-ttu-id="52a2c-509">TaxReverse.adjustTaxTransDueToExchangeRateGainLoss</span><span class="sxs-lookup"><span data-stu-id="52a2c-509">TaxReverse.adjustTaxTransDueToExchangeRateGainLoss</span></span>|
|<span data-ttu-id="52a2c-510">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="52a2c-510">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="52a2c-511">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="52a2c-511">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="52a2c-512">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="52a2c-512">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="52a2c-513">TaxReverse.postCharge</span><span class="sxs-lookup"><span data-stu-id="52a2c-513">TaxReverse.postCharge</span></span>|
|<span data-ttu-id="52a2c-514">TaxReverse.postGainLossInReportingCurrency</span><span class="sxs-lookup"><span data-stu-id="52a2c-514">TaxReverse.postGainLossInReportingCurrency</span></span>|
|<span data-ttu-id="52a2c-515">TaxSales.calc</span><span class="sxs-lookup"><span data-stu-id="52a2c-515">TaxSales.calc</span></span>|
|<span data-ttu-id="52a2c-516">TaxSales.calc</span><span class="sxs-lookup"><span data-stu-id="52a2c-516">TaxSales.calc</span></span>|
|<span data-ttu-id="52a2c-517">TaxSales.calcMarkup</span><span class="sxs-lookup"><span data-stu-id="52a2c-517">TaxSales.calcMarkup</span></span>|
|<span data-ttu-id="52a2c-518">TaxSales.configureTaxForSalesLine</span><span class="sxs-lookup"><span data-stu-id="52a2c-518">TaxSales.configureTaxForSalesLine</span></span>|
|<span data-ttu-id="52a2c-519">TaxVoucherService.taxAmountForLedgerType</span><span class="sxs-lookup"><span data-stu-id="52a2c-519">TaxVoucherService.taxAmountForLedgerType</span></span>|
|<span data-ttu-id="52a2c-520">TmpCustVendTrans.CustTransBalanceCurrency</span><span class="sxs-lookup"><span data-stu-id="52a2c-520">TmpCustVendTrans.CustTransBalanceCurrency</span></span>|
|<span data-ttu-id="52a2c-521">TmpProjAdjustment.adjustmentType2JournalType</span><span class="sxs-lookup"><span data-stu-id="52a2c-521">TmpProjAdjustment.adjustmentType2JournalType</span></span>|
|<span data-ttu-id="52a2c-522">TmpProjAdjustment.adjustmentType2TransType</span><span class="sxs-lookup"><span data-stu-id="52a2c-522">TmpProjAdjustment.adjustmentType2TransType</span></span>|
|<span data-ttu-id="52a2c-523">TmpProjAdjustment.updateFundingLimits</span><span class="sxs-lookup"><span data-stu-id="52a2c-523">TmpProjAdjustment.updateFundingLimits</span></span>|
|<span data-ttu-id="52a2c-524">TmpProjAdjustmentCreate.salesPrice</span><span class="sxs-lookup"><span data-stu-id="52a2c-524">TmpProjAdjustmentCreate.salesPrice</span></span>|
|<span data-ttu-id="52a2c-525">TrvExpenseLinesVisibilityController.isVisibilityResetRequired</span><span class="sxs-lookup"><span data-stu-id="52a2c-525">TrvExpenseLinesVisibilityController.isVisibilityResetRequired</span></span>|
|<span data-ttu-id="52a2c-526">TrvExpenses.updateFormVisibilityOnCategoryChange</span><span class="sxs-lookup"><span data-stu-id="52a2c-526">TrvExpenses.updateFormVisibilityOnCategoryChange</span></span>|
|<span data-ttu-id="52a2c-527">TrvExpTrans.calcTaxAmount</span><span class="sxs-lookup"><span data-stu-id="52a2c-527">TrvExpTrans.calcTaxAmount</span></span>|
|<span data-ttu-id="52a2c-528">TrvTaxExpense.calculateTax</span><span class="sxs-lookup"><span data-stu-id="52a2c-528">TrvTaxExpense.calculateTax</span></span>|
|<span data-ttu-id="52a2c-529">TSTimesheetEntry.init、initFields、setHeaderObjects、validateWrit、lookup</span><span class="sxs-lookup"><span data-stu-id="52a2c-529">TSTimesheetEntry.init, initFields, setHeaderObjects, validateWrit, lookup</span></span>|
|<span data-ttu-id="52a2c-530">UnitOfMeasureConverter.Convert</span><span class="sxs-lookup"><span data-stu-id="52a2c-530">UnitOfMeasureConverter.Convert</span></span>|
|<span data-ttu-id="52a2c-531">VendInvoicePaymentAuthorizationTask.postSavedInvoice</span><span class="sxs-lookup"><span data-stu-id="52a2c-531">VendInvoicePaymentAuthorizationTask.postSavedInvoice</span></span>|
|<span data-ttu-id="52a2c-532">VendPackingSlipTrans.unpostedInvoicePurchQtyServer および VendPackingSlipTrans.unpostedInvoiceInventQtyServer</span><span class="sxs-lookup"><span data-stu-id="52a2c-532">VendPackingSlipTrans.unpostedInvoicePurchQtyServer and VendPackingSlipTrans.unpostedInvoiceInventQtyServer</span></span>|
|<span data-ttu-id="52a2c-533">VendTable.checkVATNumUsed</span><span class="sxs-lookup"><span data-stu-id="52a2c-533">VendTable.checkVATNumUsed</span></span>|
|<span data-ttu-id="52a2c-534">VendTax1099Update.calcMiscChargeAmountTax</span><span class="sxs-lookup"><span data-stu-id="52a2c-534">VendTax1099Update.calcMiscChargeAmountTax</span></span>|
|<span data-ttu-id="52a2c-535">VendTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="52a2c-535">VendTrans.documentDateModified</span></span>|
|<span data-ttu-id="52a2c-536">VendTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="52a2c-536">VendTrans.documentDateModified</span></span>|
|<span data-ttu-id="52a2c-537">VendVoucher.createTransOpen</span><span class="sxs-lookup"><span data-stu-id="52a2c-537">VendVoucher.createTransOpen</span></span>|
|<span data-ttu-id="52a2c-538">VendVoucher.createTransOpen</span><span class="sxs-lookup"><span data-stu-id="52a2c-538">VendVoucher.createTransOpen</span></span>|
|<span data-ttu-id="52a2c-539">WHSContainerTable.closeContainer</span><span class="sxs-lookup"><span data-stu-id="52a2c-539">WHSContainerTable.closeContainer</span></span>|
|<span data-ttu-id="52a2c-540">WHSDocumentRouting.translate</span><span class="sxs-lookup"><span data-stu-id="52a2c-540">WHSDocumentRouting.translate</span></span>|
|<span data-ttu-id="52a2c-541">WHSLoadLine.orderHeader</span><span class="sxs-lookup"><span data-stu-id="52a2c-541">WHSLoadLine.orderHeader</span></span>|
|<span data-ttu-id="52a2c-542">WHSLoadTable.validateInventTransTypeMatches</span><span class="sxs-lookup"><span data-stu-id="52a2c-542">WHSLoadTable.validateInventTransTypeMatches</span></span>|
|<span data-ttu-id="52a2c-543">WHSLoadTableAssignOriginInfo.classDeclaration</span><span class="sxs-lookup"><span data-stu-id="52a2c-543">WHSLoadTableAssignOriginInfo.classDeclaration</span></span>|
|<span data-ttu-id="52a2c-544">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="52a2c-544">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="52a2c-545">WMSOrderTrans.split</span><span class="sxs-lookup"><span data-stu-id="52a2c-545">WMSOrderTrans.split</span></span>|
|<span data-ttu-id="52a2c-546">WmsOrderTransType_Output.updateReservations</span><span class="sxs-lookup"><span data-stu-id="52a2c-546">WmsOrderTransType_Output.updateReservations</span></span>|
|<span data-ttu-id="52a2c-547">WorkflowHierarchyProviderHelperEventHandler::getPersonnelNumberIdBySysDictTypeDelegate</span><span class="sxs-lookup"><span data-stu-id="52a2c-547">WorkflowHierarchyProviderHelperEventHandler::getPersonnelNumberIdBySysDictTypeDelegate</span></span>|
|<span data-ttu-id="52a2c-548">WorkTimeTable.removeDisplayCache</span><span class="sxs-lookup"><span data-stu-id="52a2c-548">WorkTimeTable.removeDisplayCache</span></span>|
|<span data-ttu-id="52a2c-549">WrkCtrResourceAbilityMapController.insertData</span><span class="sxs-lookup"><span data-stu-id="52a2c-549">WrkCtrResourceAbilityMapController.insertData</span></span>|
|<span data-ttu-id="52a2c-550">数量の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="52a2c-550">Enable increase of decimal precision through extensiblity for quantities</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="52a2c-551">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="52a2c-551">Enumerations made extensible</span></span>

<span data-ttu-id="52a2c-552">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="52a2c-552">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="52a2c-553">列挙型</span><span class="sxs-lookup"><span data-stu-id="52a2c-553">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="52a2c-554">AssetPostValue</span><span class="sxs-lookup"><span data-stu-id="52a2c-554">AssetPostValue</span></span>|
|<span data-ttu-id="52a2c-555">AssetPropertyType</span><span class="sxs-lookup"><span data-stu-id="52a2c-555">AssetPropertyType</span></span>|
|<span data-ttu-id="52a2c-556">AssetStatus</span><span class="sxs-lookup"><span data-stu-id="52a2c-556">AssetStatus</span></span>|
|<span data-ttu-id="52a2c-557">CaseStatus</span><span class="sxs-lookup"><span data-stu-id="52a2c-557">CaseStatus</span></span>|
|<span data-ttu-id="52a2c-558">CommissionSalesRepCode</span><span class="sxs-lookup"><span data-stu-id="52a2c-558">CommissionSalesRepCode</span></span>|
|<span data-ttu-id="52a2c-559">DirSubNameSequenceType</span><span class="sxs-lookup"><span data-stu-id="52a2c-559">DirSubNameSequenceType</span></span>|
|<span data-ttu-id="52a2c-560">FreightSlipType</span><span class="sxs-lookup"><span data-stu-id="52a2c-560">FreightSlipType</span></span>|
|<span data-ttu-id="52a2c-561">HRPLimitDocumentType</span><span class="sxs-lookup"><span data-stu-id="52a2c-561">HRPLimitDocumentType</span></span>|
|<span data-ttu-id="52a2c-562">IntrastatPaymentMethod_IT</span><span class="sxs-lookup"><span data-stu-id="52a2c-562">IntrastatPaymentMethod_IT</span></span>|
|<span data-ttu-id="52a2c-563">InventBlockingType</span><span class="sxs-lookup"><span data-stu-id="52a2c-563">InventBlockingType</span></span>|
|<span data-ttu-id="52a2c-564">JmgPaySpecTypeEnumPick</span><span class="sxs-lookup"><span data-stu-id="52a2c-564">JmgPaySpecTypeEnumPick</span></span>|
|<span data-ttu-id="52a2c-565">KMQuestionAnswerInputType</span><span class="sxs-lookup"><span data-stu-id="52a2c-565">KMQuestionAnswerInputType</span></span>|
|<span data-ttu-id="52a2c-566">LedgerJournalType</span><span class="sxs-lookup"><span data-stu-id="52a2c-566">LedgerJournalType</span></span>|
|<span data-ttu-id="52a2c-567">LogisticsAddrZipCodeImportCountryRegion</span><span class="sxs-lookup"><span data-stu-id="52a2c-567">LogisticsAddrZipCodeImportCountryRegion</span></span>|
|<span data-ttu-id="52a2c-568">LogType</span><span class="sxs-lookup"><span data-stu-id="52a2c-568">LogType</span></span>|
|<span data-ttu-id="52a2c-569">MarkupModuleType</span><span class="sxs-lookup"><span data-stu-id="52a2c-569">MarkupModuleType</span></span>|
|<span data-ttu-id="52a2c-570">MarkupModuleType</span><span class="sxs-lookup"><span data-stu-id="52a2c-570">MarkupModuleType</span></span>|
|<span data-ttu-id="52a2c-571">MCRBrokerValueType</span><span class="sxs-lookup"><span data-stu-id="52a2c-571">MCRBrokerValueType</span></span>|
|<span data-ttu-id="52a2c-572">PaymentType</span><span class="sxs-lookup"><span data-stu-id="52a2c-572">PaymentType</span></span>|
|<span data-ttu-id="52a2c-573">PDSCalcElementTypeBase</span><span class="sxs-lookup"><span data-stu-id="52a2c-573">PDSCalcElementTypeBase</span></span>|
|<span data-ttu-id="52a2c-574">PdsStatus</span><span class="sxs-lookup"><span data-stu-id="52a2c-574">PdsStatus</span></span>|
|<span data-ttu-id="52a2c-575">PdsVendorCheckItem</span><span class="sxs-lookup"><span data-stu-id="52a2c-575">PdsVendorCheckItem</span></span>|
|<span data-ttu-id="52a2c-576">ProdStatus</span><span class="sxs-lookup"><span data-stu-id="52a2c-576">ProdStatus</span></span>|
|<span data-ttu-id="52a2c-577">ProjActiveAll</span><span class="sxs-lookup"><span data-stu-id="52a2c-577">ProjActiveAll</span></span>|
|<span data-ttu-id="52a2c-578">ProjAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="52a2c-578">ProjAdjustmentType</span></span>|
|<span data-ttu-id="52a2c-579">ProjAllTrxType</span><span class="sxs-lookup"><span data-stu-id="52a2c-579">ProjAllTrxType</span></span>|
|<span data-ttu-id="52a2c-580">ProjBudgetAction</span><span class="sxs-lookup"><span data-stu-id="52a2c-580">ProjBudgetAction</span></span>|
|<span data-ttu-id="52a2c-581">ProjCostType</span><span class="sxs-lookup"><span data-stu-id="52a2c-581">ProjCostType</span></span>|
|<span data-ttu-id="52a2c-582">ProjForecastInvoiceFrequency</span><span class="sxs-lookup"><span data-stu-id="52a2c-582">ProjForecastInvoiceFrequency</span></span>|
|<span data-ttu-id="52a2c-583">ProjLinePropertySearch</span><span class="sxs-lookup"><span data-stu-id="52a2c-583">ProjLinePropertySearch</span></span>|
|<span data-ttu-id="52a2c-584">ProjSalesPriceMarkup</span><span class="sxs-lookup"><span data-stu-id="52a2c-584">ProjSalesPriceMarkup</span></span>|
|<span data-ttu-id="52a2c-585">ProjSortValue</span><span class="sxs-lookup"><span data-stu-id="52a2c-585">ProjSortValue</span></span>|
|<span data-ttu-id="52a2c-586">ProjTableEditSubProj</span><span class="sxs-lookup"><span data-stu-id="52a2c-586">ProjTableEditSubProj</span></span>|
|<span data-ttu-id="52a2c-587">ReqCovType</span><span class="sxs-lookup"><span data-stu-id="52a2c-587">ReqCovType</span></span>|
|<span data-ttu-id="52a2c-588">ResCharacteristicSetEnum</span><span class="sxs-lookup"><span data-stu-id="52a2c-588">ResCharacteristicSetEnum</span></span>|
|<span data-ttu-id="52a2c-589">SettlementType</span><span class="sxs-lookup"><span data-stu-id="52a2c-589">SettlementType</span></span>|
|<span data-ttu-id="52a2c-590">smmShowTimeAs</span><span class="sxs-lookup"><span data-stu-id="52a2c-590">smmShowTimeAs</span></span>|
|<span data-ttu-id="52a2c-591">SourceDocumentRelationType</span><span class="sxs-lookup"><span data-stu-id="52a2c-591">SourceDocumentRelationType</span></span>|
|<span data-ttu-id="52a2c-592">TaxRegistrationTypesList</span><span class="sxs-lookup"><span data-stu-id="52a2c-592">TaxRegistrationTypesList</span></span>|
|<span data-ttu-id="52a2c-593">TaxReportLayout</span><span class="sxs-lookup"><span data-stu-id="52a2c-593">TaxReportLayout</span></span>|
|<span data-ttu-id="52a2c-594">TradeWorkflowState</span><span class="sxs-lookup"><span data-stu-id="52a2c-594">TradeWorkflowState</span></span>|
|<span data-ttu-id="52a2c-595">WMSExpeditionStatus</span><span class="sxs-lookup"><span data-stu-id="52a2c-595">WMSExpeditionStatus</span></span>|


## <a name="extensible-sql-operations"></a><span data-ttu-id="52a2c-596">拡張可能な SQL 操作</span><span class="sxs-lookup"><span data-stu-id="52a2c-596">Extensible SQL Operations</span></span>

<span data-ttu-id="52a2c-597">これらの SQL 操作は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="52a2c-597">These SQL operations have been made extensible in this update.</span></span>

| <span data-ttu-id="52a2c-598">工程</span><span class="sxs-lookup"><span data-stu-id="52a2c-598">Operation</span></span> |
| --------------- |
|<span data-ttu-id="52a2c-599">CustInterestPost.postVoucherPerTransaction</span><span class="sxs-lookup"><span data-stu-id="52a2c-599">CustInterestPost.postVoucherPerTransaction</span></span>|
|<span data-ttu-id="52a2c-600">InventMov_ProdLine_JournalBom.insertChildBuffer</span><span class="sxs-lookup"><span data-stu-id="52a2c-600">InventMov_ProdLine_JournalBom.insertChildBuffer</span></span>|
|<span data-ttu-id="52a2c-601">InventUpdate.initInventTransToReceiveList</span><span class="sxs-lookup"><span data-stu-id="52a2c-601">InventUpdate.initInventTransToReceiveList</span></span>|
|<span data-ttu-id="52a2c-602">ProjAdjustmentUpdate_PostAsync.postAsync</span><span class="sxs-lookup"><span data-stu-id="52a2c-602">ProjAdjustmentUpdate_PostAsync.postAsync</span></span>|
|<span data-ttu-id="52a2c-603">ProjBudgetManager.createBudgetCostForecast</span><span class="sxs-lookup"><span data-stu-id="52a2c-603">ProjBudgetManager.createBudgetCostForecast</span></span>|
|<span data-ttu-id="52a2c-604">ProjBudgetManager.createBudgetEmplForecast</span><span class="sxs-lookup"><span data-stu-id="52a2c-604">ProjBudgetManager.createBudgetEmplForecast</span></span>|
|<span data-ttu-id="52a2c-605">ProjBudgetManager.createBudgetRevenueForecast</span><span class="sxs-lookup"><span data-stu-id="52a2c-605">ProjBudgetManager.createBudgetRevenueForecast</span></span>|
|<span data-ttu-id="52a2c-606">ProjBudgetManager.createBudgetSalesForecast</span><span class="sxs-lookup"><span data-stu-id="52a2c-606">ProjBudgetManager.createBudgetSalesForecast</span></span>|


## <a name="metadata-changes"></a><span data-ttu-id="52a2c-607">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="52a2c-607">Metadata changes</span></span>

<span data-ttu-id="52a2c-608">これらのメタデータの変更は、このアップデートで行われました。</span><span class="sxs-lookup"><span data-stu-id="52a2c-608">These metadata changes have been made in this update.</span></span>

| <span data-ttu-id="52a2c-609">工程</span><span class="sxs-lookup"><span data-stu-id="52a2c-609">Operation</span></span> |
| --------------- |
|<span data-ttu-id="52a2c-610">/Data entities/ReqPlannedOrderEntity.Is Public</span><span class="sxs-lookup"><span data-stu-id="52a2c-610">/Data entities/ReqPlannedOrderEntity.Is Public</span></span>|
|<span data-ttu-id="52a2c-611">/DataTypes/Extended Data Types/AmountQty.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-611">/DataTypes/Extended Data Types/AmountQty.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-612">/DataTypes/Extended Data Types/AssetDepreciationAmountUnitReportingCurrency.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-612">/DataTypes/Extended Data Types/AssetDepreciationAmountUnitReportingCurrency.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-613">/DataTypes/Extended Data Types/BOMProductQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-613">/DataTypes/Extended Data Types/BOMProductQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-614">/DataTypes/Extended Data Types/CostPriceNonMonetary.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-614">/DataTypes/Extended Data Types/CostPriceNonMonetary.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-615">/DataTypes/Extended Data Types/CostQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-615">/DataTypes/Extended Data Types/CostQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-616">/DataTypes/Extended Data Types/MCRRoyaltyValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-616">/DataTypes/Extended Data Types/MCRRoyaltyValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-617">/DataTypes/Extended Data Types/PdsRebateValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-617">/DataTypes/Extended Data Types/PdsRebateValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-618">/DataTypes/Extended Data Types/PriceDiscAmount.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-618">/DataTypes/Extended Data Types/PriceDiscAmount.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-619">/DataTypes/Extended Data Types/PriceQty.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-619">/DataTypes/Extended Data Types/PriceQty.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-620">/DataTypes/Extended Data Types/PriceUnit.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-620">/DataTypes/Extended Data Types/PriceUnit.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-621">/DataTypes/Extended Data Types/PriceUnit.Scale</span><span class="sxs-lookup"><span data-stu-id="52a2c-621">/DataTypes/Extended Data Types/PriceUnit.Scale</span></span>|
|<span data-ttu-id="52a2c-622">/DataTypes/Extended Data Types/ProductQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-622">/DataTypes/Extended Data Types/ProductQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-623">/DataTypes/Extended Data Types/ProductQuantityHourValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-623">/DataTypes/Extended Data Types/ProductQuantityHourValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-624">/DataTypes/Extended Data Types/ProjName.Extends</span><span class="sxs-lookup"><span data-stu-id="52a2c-624">/DataTypes/Extended Data Types/ProjName.Extends</span></span>|
|<span data-ttu-id="52a2c-625">/DataTypes/Extended Data Types/TAMRebateValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-625">/DataTypes/Extended Data Types/TAMRebateValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-626">/DataTypes/Extended Data Types/UnitAmountCur.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-626">/DataTypes/Extended Data Types/UnitAmountCur.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-627">/DataTypes/Extended Data Types/UnitAmountMST.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-627">/DataTypes/Extended Data Types/UnitAmountMST.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-628">/DataTypes/Extended Data Types/WeightBase.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="52a2c-628">/DataTypes/Extended Data Types/WeightBase.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="52a2c-629">/Tables/LedgerJournalTrans_Project/Relations/LedgerJournalTrans.createNavigationPropertyMethod</span><span class="sxs-lookup"><span data-stu-id="52a2c-629">/Tables/LedgerJournalTrans_Project/Relations/LedgerJournalTrans.createNavigationPropertyMethod</span></span>|
|<span data-ttu-id="52a2c-630">/Tables/PriceDiscGroup.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="52a2c-630">/Tables/PriceDiscGroup.Cache Lookup</span></span>|
|<span data-ttu-id="52a2c-631">/Tables/VendInvoiceJour/Fields/DefaultDimension.Visible</span><span class="sxs-lookup"><span data-stu-id="52a2c-631">/Tables/VendInvoiceJour/Fields/DefaultDimension.Visible</span></span>|
|<span data-ttu-id="52a2c-632">/Tables/VendInvoiceTrans/Fields/DefaultDimension.Visible</span><span class="sxs-lookup"><span data-stu-id="52a2c-632">/Tables/VendInvoiceTrans/Fields/DefaultDimension.Visible</span></span>|
|<span data-ttu-id="52a2c-633">/Tables/WMSAisle.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="52a2c-633">/Tables/WMSAisle.Cache Lookup</span></span>|
|<span data-ttu-id="52a2c-634">/Tables/WorkCalendarTable.Create Rec Id Index</span><span class="sxs-lookup"><span data-stu-id="52a2c-634">/Tables/WorkCalendarTable.Create Rec Id Index</span></span>|
|<span data-ttu-id="52a2c-635">/Tables/WorkTimeLine.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="52a2c-635">/Tables/WorkTimeLine.Cache Lookup</span></span>|
|<span data-ttu-id="52a2c-636">/Tables/WorkTimeTable.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="52a2c-636">/Tables/WorkTimeTable.Cache Lookup</span></span>|


## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="52a2c-637">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="52a2c-637">Additional extensibility enhancements</span></span>

<span data-ttu-id="52a2c-638">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="52a2c-638">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="52a2c-639">バグ リクエスト: "CustCollectionLetterTrans -> CollectionLetterNum" 関係プロパティ</span><span class="sxs-lookup"><span data-stu-id="52a2c-639">Bug request: "CustCollectionLetterTrans -> CollectionLetterNum" Relation properties</span></span>
- <span data-ttu-id="52a2c-640">価格の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="52a2c-640">Enable increase of decimal precision through extensiblity for prices</span></span>
- <span data-ttu-id="52a2c-641">重量の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="52a2c-641">Enable increase of decimal precision through extensiblity for weights</span></span>
- <span data-ttu-id="52a2c-642">マップ拡張: LogisticsEntityLocationMap</span><span class="sxs-lookup"><span data-stu-id="52a2c-642">Map Extension: LogisticsEntityLocationMap</span></span>
- <span data-ttu-id="52a2c-643">OMOperatingUnit は、DimAttributeOMDepartment.Value のユーザー フレンドリおよび定義済の値を指定する必要がある</span><span class="sxs-lookup"><span data-stu-id="52a2c-643">OMOperatingUnit should provide user friendly and defined value for DimAttributeOMDepartment.Value</span></span>
- <span data-ttu-id="52a2c-644">InventPosting が LedgerDimension を検索する方法を再設計</span><span class="sxs-lookup"><span data-stu-id="52a2c-644">Redesign how InventPosting finds LedgerDimension</span></span>
- <span data-ttu-id="52a2c-645">WhsWorkExecuteDisplayAdjustIn を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="52a2c-645">Refactor WhsWorkExecuteDisplayAdjustIn to ProcessGuide framework</span></span>
- <span data-ttu-id="52a2c-646">WHSWorkExecuteDisplayChangeWarehouse を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="52a2c-646">Refactor WHSWorkExecuteDisplayChangeWarehouse to ProcessGuide framework</span></span>
- <span data-ttu-id="52a2c-647">WhsWorkExecuteDisplayInquiryItem を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="52a2c-647">Refactor WhsWorkExecuteDisplayInquiryItem to ProcessGuide framework</span></span>
- <span data-ttu-id="52a2c-648">WhsWorkExecuteDisplayInquiryLocation を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="52a2c-648">Refactor WhsWorkExecuteDisplayInquiryLocation to ProcessGuide framework</span></span>
- <span data-ttu-id="52a2c-649">WhsWorkExecuteDisplayInquiryLP を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="52a2c-649">Refactor WhsWorkExecuteDisplayInquiryLP to ProcessGuide framework</span></span>
- <span data-ttu-id="52a2c-650">whsWorkExecuteDisplayReprintLabel を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="52a2c-650">Refactor whsWorkExecuteDisplayReprintLabel to ProcessGuide framework</span></span>
- <span data-ttu-id="52a2c-651">小売チャネル: サポート BankDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="52a2c-651">Retail channel: Support BankDropOperationRequest</span></span>

