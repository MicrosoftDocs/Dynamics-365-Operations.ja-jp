---
title: Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations バージョン 8.1 に実装された拡張機能を一覧表示します。
author: FrankDahl
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: App 8.1
ms.openlocfilehash: 578f54f49751590de38e688ecc7e60d6932cbd1c
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866260"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-81"></a><span data-ttu-id="d55af-103">Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="d55af-103">Extensibility changes in Dynamics 365 for Finance and Operations version 8.1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d55af-104">これは、Dynamics 365 for Finance and Operations バージョン 8.1 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="d55af-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations version 8.1.</span></span> <span data-ttu-id="d55af-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d55af-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="d55af-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="d55af-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="d55af-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d55af-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="d55af-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="d55af-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="d55af-109">AssetPost.createTrueUpDepreciation</span><span class="sxs-lookup"><span data-stu-id="d55af-109">AssetPost.createTrueUpDepreciation</span></span>|
|<span data-ttu-id="d55af-110">AssetPost.createTrueUpDepreciation</span><span class="sxs-lookup"><span data-stu-id="d55af-110">AssetPost.createTrueUpDepreciation</span></span>|
|<span data-ttu-id="d55af-111">AssetPostDisposal.post</span><span class="sxs-lookup"><span data-stu-id="d55af-111">AssetPostDisposal.post</span></span>|
|<span data-ttu-id="d55af-112">AssetPostDisposal.postVoucherTransactions</span><span class="sxs-lookup"><span data-stu-id="d55af-112">AssetPostDisposal.postVoucherTransactions</span></span>|
|<span data-ttu-id="d55af-113">AssetPostDisposal.postVoucherTransactions</span><span class="sxs-lookup"><span data-stu-id="d55af-113">AssetPostDisposal.postVoucherTransactions</span></span>|
|<span data-ttu-id="d55af-114">AssetTable.buildComposedOf</span><span class="sxs-lookup"><span data-stu-id="d55af-114">AssetTable.buildComposedOf</span></span>|
|<span data-ttu-id="d55af-115">AssetTable.createStruct</span><span class="sxs-lookup"><span data-stu-id="d55af-115">AssetTable.createStruct</span></span>|
|<span data-ttu-id="d55af-116">AxInventDim_SalesLine.setInventSiteId</span><span class="sxs-lookup"><span data-stu-id="d55af-116">AxInventDim_SalesLine.setInventSiteId</span></span>|
|<span data-ttu-id="d55af-117">BankChequePrint.printDocument</span><span class="sxs-lookup"><span data-stu-id="d55af-117">BankChequePrint.printDocument</span></span>|
|<span data-ttu-id="d55af-118">BankCodaProcessing.custSettlement</span><span class="sxs-lookup"><span data-stu-id="d55af-118">BankCodaProcessing.custSettlement</span></span>|
|<span data-ttu-id="d55af-119">BankDeposit.InitFromLedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-119">BankDeposit.InitFromLedgerJournalTrans</span></span>|
|<span data-ttu-id="d55af-120">BankExchAdj_RU.calcAndPostCurrency</span><span class="sxs-lookup"><span data-stu-id="d55af-120">BankExchAdj_RU.calcAndPostCurrency</span></span>|
|<span data-ttu-id="d55af-121">BankExchAdj_RU.calcAndPostCurrency</span><span class="sxs-lookup"><span data-stu-id="d55af-121">BankExchAdj_RU.calcAndPostCurrency</span></span>|
|<span data-ttu-id="d55af-122">BankExchAdj_RU.calcBalance</span><span class="sxs-lookup"><span data-stu-id="d55af-122">BankExchAdj_RU.calcBalance</span></span>|
|<span data-ttu-id="d55af-123">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="d55af-123">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="d55af-124">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="d55af-124">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="d55af-125">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="d55af-125">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="d55af-126">BankPrintTestCheque.printCheque</span><span class="sxs-lookup"><span data-stu-id="d55af-126">BankPrintTestCheque.printCheque</span></span>|
|<span data-ttu-id="d55af-127">BlindCloseView.MPOS_ExtensibleViews</span><span class="sxs-lookup"><span data-stu-id="d55af-127">BlindCloseView.MPOS_ExtensibleViews</span></span>|
|<span data-ttu-id="d55af-128">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span><span class="sxs-lookup"><span data-stu-id="d55af-128">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span></span>|
|<span data-ttu-id="d55af-129">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span><span class="sxs-lookup"><span data-stu-id="d55af-129">BudgetAnalysisInquiryHelper_PSN.insertTreeNodes</span></span>|
|<span data-ttu-id="d55af-130">BudgetAnalysisInquiryProcessor_PSN.getBudgetAnalysisLedgerDimensions</span><span class="sxs-lookup"><span data-stu-id="d55af-130">BudgetAnalysisInquiryProcessor_PSN.getBudgetAnalysisLedgerDimensions</span></span>|
|<span data-ttu-id="d55af-131">CAMStatisticalEntryTransferJournalEntryDataMapper.newFromParameters</span><span class="sxs-lookup"><span data-stu-id="d55af-131">CAMStatisticalEntryTransferJournalEntryDataMapper.newFromParameters</span></span>|
|<span data-ttu-id="d55af-132">CaseUpdateStatus_Close.changeStatus</span><span class="sxs-lookup"><span data-stu-id="d55af-132">CaseUpdateStatus_Close.changeStatus</span></span>|
|<span data-ttu-id="d55af-133">CashManagementView.NewExtension</span><span class="sxs-lookup"><span data-stu-id="d55af-133">CashManagementView.NewExtension</span></span>|
|<span data-ttu-id="d55af-134">ChequeController.init</span><span class="sxs-lookup"><span data-stu-id="d55af-134">ChequeController.init</span></span>|
|<span data-ttu-id="d55af-135">ChequeDP.insertChequeTmp</span><span class="sxs-lookup"><span data-stu-id="d55af-135">ChequeDP.insertChequeTmp</span></span>|
|<span data-ttu-id="d55af-136">クラス InventTransferEstimation.updateEstimatedPre</span><span class="sxs-lookup"><span data-stu-id="d55af-136">Class InventTransferEstimation.updateEstimatedPre</span></span>|
|<span data-ttu-id="d55af-137">クラス Markup.insertReturnMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-137">class Markup.insertReturnMarkupTrans</span></span>|
|<span data-ttu-id="d55af-138">クラス MarkupTransInsert.insertForCodes</span><span class="sxs-lookup"><span data-stu-id="d55af-138">class MarkupTransInsert.insertForCodes</span></span>|
|<span data-ttu-id="d55af-139">クラス PurchLineType.updateSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-139">Class PurchLineType.updateSalesLine</span></span>|
|<span data-ttu-id="d55af-140">クラス PurchPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="d55af-140">class PurchPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="d55af-141">クラス SalesQuantity_PackingSlip.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="d55af-141">Class SalesQuantity_PackingSlip.calcQtyInvent</span></span>|
|<span data-ttu-id="d55af-142">クラス SalesQuantity_PackingSlip.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="d55af-142">Class SalesQuantity_PackingSlip.calcQtySales</span></span>|
|<span data-ttu-id="d55af-143">Class/AssetPost.post</span><span class="sxs-lookup"><span data-stu-id="d55af-143">Class/AssetPost.post</span></span>|
|<span data-ttu-id="d55af-144">Class/FormLetterJournalPost.post</span><span class="sxs-lookup"><span data-stu-id="d55af-144">Class/FormLetterJournalPost.post</span></span>|
|<span data-ttu-id="d55af-145">Class/PurchReqTableListPageInteraction.applyFilter</span><span class="sxs-lookup"><span data-stu-id="d55af-145">Class/PurchReqTableListPageInteraction.applyFilter</span></span>|
|<span data-ttu-id="d55af-146">Class\PurchFormLetter_PackingSlip.checkFormLetterId</span><span class="sxs-lookup"><span data-stu-id="d55af-146">Class\PurchFormLetter_PackingSlip.checkFormLetterId</span></span>|
|<span data-ttu-id="d55af-147">Class\PurchFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="d55af-147">Class\PurchFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="d55af-148">Class\TaxCalculationAdjustment.calcManualInserted</span><span class="sxs-lookup"><span data-stu-id="d55af-148">Class\TaxCalculationAdjustment.calcManualInserted</span></span>|
|<span data-ttu-id="d55af-149">CompanyInfoHelper.onValidateField</span><span class="sxs-lookup"><span data-stu-id="d55af-149">CompanyInfoHelper.onValidateField</span></span>|
|<span data-ttu-id="d55af-150">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span><span class="sxs-lookup"><span data-stu-id="d55af-150">CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite</span></span>|
|<span data-ttu-id="d55af-151">CustAccountStatementExtController.initAgingBalances</span><span class="sxs-lookup"><span data-stu-id="d55af-151">CustAccountStatementExtController.initAgingBalances</span></span>|
|<span data-ttu-id="d55af-152">CustAccountStatementExtController.preprocessParty</span><span class="sxs-lookup"><span data-stu-id="d55af-152">CustAccountStatementExtController.preprocessParty</span></span>|
|<span data-ttu-id="d55af-153">CustAccountStatementExtController.processParty</span><span class="sxs-lookup"><span data-stu-id="d55af-153">CustAccountStatementExtController.processParty</span></span>|
|<span data-ttu-id="d55af-154">CustAccountStatementExtController.processTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-154">CustAccountStatementExtController.processTrans</span></span>|
|<span data-ttu-id="d55af-155">CustAccountStatementExtController.runPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="d55af-155">CustAccountStatementExtController.runPrintMgmt</span></span>|
|<span data-ttu-id="d55af-156">CustCollectionLetterCreate.run</span><span class="sxs-lookup"><span data-stu-id="d55af-156">CustCollectionLetterCreate.run</span></span>|
|<span data-ttu-id="d55af-157">CustCollectionLetterPost.RUN</span><span class="sxs-lookup"><span data-stu-id="d55af-157">CustCollectionLetterPost.RUN</span></span>|
|<span data-ttu-id="d55af-158">CustInterestAdjust.createCustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="d55af-158">CustInterestAdjust.createCustInvoiceTable</span></span>|
|<span data-ttu-id="d55af-159">CustInterestCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-159">CustInterestCreate.createJournal</span></span>|
|<span data-ttu-id="d55af-160">CustInterestCreate.logDateRecordError</span><span class="sxs-lookup"><span data-stu-id="d55af-160">CustInterestCreate.logDateRecordError</span></span>|
|<span data-ttu-id="d55af-161">CustInterestCreate.newAccount</span><span class="sxs-lookup"><span data-stu-id="d55af-161">CustInterestCreate.newAccount</span></span>|
|<span data-ttu-id="d55af-162">CustInterestCreate.resetCustInterest</span><span class="sxs-lookup"><span data-stu-id="d55af-162">CustInterestCreate.resetCustInterest</span></span>|
|<span data-ttu-id="d55af-163">CustInterestCreate.runOnce</span><span class="sxs-lookup"><span data-stu-id="d55af-163">CustInterestCreate.runOnce</span></span>|
|<span data-ttu-id="d55af-164">CustInvoiceCalcTax_Invoice.updateTaxWriteCode</span><span class="sxs-lookup"><span data-stu-id="d55af-164">CustInvoiceCalcTax_Invoice.updateTaxWriteCode</span></span>|
|<span data-ttu-id="d55af-165">CustInvoiceLine.Insert</span><span class="sxs-lookup"><span data-stu-id="d55af-165">CustInvoiceLine.Insert</span></span>|
|<span data-ttu-id="d55af-166">CustOutPaym.generatePaymentLines</span><span class="sxs-lookup"><span data-stu-id="d55af-166">CustOutPaym.generatePaymentLines</span></span>|
|<span data-ttu-id="d55af-167">CustQuotationJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-167">CustQuotationJour.printJournal</span></span>|
|<span data-ttu-id="d55af-168">CustTable.CanSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="d55af-168">CustTable.CanSubmitToWorkflow</span></span>|
|<span data-ttu-id="d55af-169">CustTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="d55af-169">CustTrans.documentDateModified</span></span>|
|<span data-ttu-id="d55af-170">CustTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="d55af-170">CustTrans.documentDateModified</span></span>|
|<span data-ttu-id="d55af-171">CustTransSettlement.insertSettlementLines</span><span class="sxs-lookup"><span data-stu-id="d55af-171">CustTransSettlement.insertSettlementLines</span></span>|
|<span data-ttu-id="d55af-172">CustVendCheque.createBankChequePaymentTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-172">CustVendCheque.createBankChequePaymentTrans</span></span>|
|<span data-ttu-id="d55af-173">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="d55af-173">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="d55af-174">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="d55af-174">CustVendCheque.output</span></span>|
|<span data-ttu-id="d55af-175">CustVendChequeSlipTextCalculator.seebelow</span><span class="sxs-lookup"><span data-stu-id="d55af-175">CustVendChequeSlipTextCalculator.seebelow</span></span>|
|<span data-ttu-id="d55af-176">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="d55af-176">CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen</span></span>|
|<span data-ttu-id="d55af-177">CustVendPaymProposalTransferToJournal.transferProposal</span><span class="sxs-lookup"><span data-stu-id="d55af-177">CustVendPaymProposalTransferToJournal.transferProposal</span></span>|
|<span data-ttu-id="d55af-178">CustVendPaymSched.construct</span><span class="sxs-lookup"><span data-stu-id="d55af-178">CustVendPaymSched.construct</span></span>|
|<span data-ttu-id="d55af-179">CustVendPaymSched.initCalcPaymSched</span><span class="sxs-lookup"><span data-stu-id="d55af-179">CustVendPaymSched.initCalcPaymSched</span></span>|
|<span data-ttu-id="d55af-180">CustVendReversePosting.restoreCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="d55af-180">CustVendReversePosting.restoreCustVendTransOpen</span></span>|
|<span data-ttu-id="d55af-181">CustVendVoucher.post</span><span class="sxs-lookup"><span data-stu-id="d55af-181">CustVendVoucher.post</span></span>|
|<span data-ttu-id="d55af-182">DataEntityView/SalesOrderLineEntity/Method/validateWrite</span><span class="sxs-lookup"><span data-stu-id="d55af-182">DataEntityView/SalesOrderLineEntity/Method/validateWrite</span></span>|
|<span data-ttu-id="d55af-183">DataEntityView/SalesQuotationLineEntity/Method/validateWrite</span><span class="sxs-lookup"><span data-stu-id="d55af-183">DataEntityView/SalesQuotationLineEntity/Method/validateWrite</span></span>|
|<span data-ttu-id="d55af-184">EFDocEmailProcessor_BR.saveReceivedXmlData</span><span class="sxs-lookup"><span data-stu-id="d55af-184">EFDocEmailProcessor_BR.saveReceivedXmlData</span></span>|
|<span data-ttu-id="d55af-185">EFDocMsgFormat_XmlBase_BR.createElementWithValue</span><span class="sxs-lookup"><span data-stu-id="d55af-185">EFDocMsgFormat_XmlBase_BR.createElementWithValue</span></span>|
|<span data-ttu-id="d55af-186">メソッドに抽出: SalesParmTable.GetPaymentSched</span><span class="sxs-lookup"><span data-stu-id="d55af-186">Extract into method: SalesParmTable.GetPaymentSched</span></span>|
|<span data-ttu-id="d55af-187">フォーム InventJournalAsset\Methods\init</span><span class="sxs-lookup"><span data-stu-id="d55af-187">Form InventJournalAsset\Methods\init</span></span>|
|<span data-ttu-id="d55af-188">フォーム InventJournalCount\Methods\init</span><span class="sxs-lookup"><span data-stu-id="d55af-188">Form InventJournalCount\Methods\init</span></span>|
|<span data-ttu-id="d55af-189">フォーム InventJournalMovement.init</span><span class="sxs-lookup"><span data-stu-id="d55af-189">Form InventJournalMovement.init</span></span>|
|<span data-ttu-id="d55af-190">フォーム TrvExpenses.confirmCategoryChange</span><span class="sxs-lookup"><span data-stu-id="d55af-190">Form TrvExpenses.confirmCategoryChange</span></span>|
|<span data-ttu-id="d55af-191">Form\SalesEditLines.closeOk</span><span class="sxs-lookup"><span data-stu-id="d55af-191">Form\SalesEditLines.closeOk</span></span>|
|<span data-ttu-id="d55af-192">FormletterJournalPost.newPostPurch</span><span class="sxs-lookup"><span data-stu-id="d55af-192">FormletterJournalPost.newPostPurch</span></span>|
|<span data-ttu-id="d55af-193">FreeTextInvoiceDP.Variable 宣言</span><span class="sxs-lookup"><span data-stu-id="d55af-193">FreeTextInvoiceDP.Variable declaration</span></span>|
|<span data-ttu-id="d55af-194">HcmActionTypeSetup.lookupWorkflowTable</span><span class="sxs-lookup"><span data-stu-id="d55af-194">HcmActionTypeSetup.lookupWorkflowTable</span></span>|
|<span data-ttu-id="d55af-195">HcmPosition_HcmPositionDefaultDimension_formDatasource.selectionChanged</span><span class="sxs-lookup"><span data-stu-id="d55af-195">HcmPosition_HcmPositionDefaultDimension_formDatasource.selectionChanged</span></span>|
|<span data-ttu-id="d55af-196">HcmPositionTransition:: createHcmPositionWorkerAssignment</span><span class="sxs-lookup"><span data-stu-id="d55af-196">HcmPositionTransition:: createHcmPositionWorkerAssignment</span></span>|
|<span data-ttu-id="d55af-197">HcmPositionWorkerAssignmentDialog:: createWorkerActionOk</span><span class="sxs-lookup"><span data-stu-id="d55af-197">HcmPositionWorkerAssignmentDialog:: createWorkerActionOk</span></span>|
|<span data-ttu-id="d55af-198">HRMCompFixedPlanTable::enforcePayRateTolerance</span><span class="sxs-lookup"><span data-stu-id="d55af-198">HRMCompFixedPlanTable::enforcePayRateTolerance</span></span> |
|<span data-ttu-id="d55af-199">InterCompanyPostPurch.construct</span><span class="sxs-lookup"><span data-stu-id="d55af-199">InterCompanyPostPurch.construct</span></span>|
|<span data-ttu-id="d55af-200">InterCompanyPostPurch.formLetterUpdate</span><span class="sxs-lookup"><span data-stu-id="d55af-200">InterCompanyPostPurch.formLetterUpdate</span></span>|
|<span data-ttu-id="d55af-201">InterCompanyPostSales.formLetterUpdate</span><span class="sxs-lookup"><span data-stu-id="d55af-201">InterCompanyPostSales.formLetterUpdate</span></span>|
|<span data-ttu-id="d55af-202">InterCompanySyncPurchTableType.setSalesTableData</span><span class="sxs-lookup"><span data-stu-id="d55af-202">InterCompanySyncPurchTableType.setSalesTableData</span></span>|
|<span data-ttu-id="d55af-203">IntrastatCheck.Run</span><span class="sxs-lookup"><span data-stu-id="d55af-203">IntrastatCheck.Run</span></span>|
|<span data-ttu-id="d55af-204">IntrastatTransfer.calcAmountsAndMarkups</span><span class="sxs-lookup"><span data-stu-id="d55af-204">IntrastatTransfer.calcAmountsAndMarkups</span></span>|
|<span data-ttu-id="d55af-205">IntrastatTransfer.calcValuesSign</span><span class="sxs-lookup"><span data-stu-id="d55af-205">IntrastatTransfer.calcValuesSign</span></span>|
|<span data-ttu-id="d55af-206">IntrastatTransfer.distributeIntrastatAddValueLV</span><span class="sxs-lookup"><span data-stu-id="d55af-206">IntrastatTransfer.distributeIntrastatAddValueLV</span></span>|
|<span data-ttu-id="d55af-207">IntrastatTransfer.run</span><span class="sxs-lookup"><span data-stu-id="d55af-207">IntrastatTransfer.run</span></span>|
|<span data-ttu-id="d55af-208">IntrastatTransferIT.calcCounty</span><span class="sxs-lookup"><span data-stu-id="d55af-208">IntrastatTransferIT.calcCounty</span></span>|
|<span data-ttu-id="d55af-209">IntrastatTransferIT.updateTransactionCurrencyAmount</span><span class="sxs-lookup"><span data-stu-id="d55af-209">IntrastatTransferIT.updateTransactionCurrencyAmount</span></span>|
|<span data-ttu-id="d55af-210">InventAdj_Transact.run</span><span class="sxs-lookup"><span data-stu-id="d55af-210">InventAdj_Transact.run</span></span>|
|<span data-ttu-id="d55af-211">InventCostPost.postInventCostTransVariance</span><span class="sxs-lookup"><span data-stu-id="d55af-211">InventCostPost.postInventCostTransVariance</span></span>|
|<span data-ttu-id="d55af-212">InventMov_Purch.updateAutoLossProfit</span><span class="sxs-lookup"><span data-stu-id="d55af-212">InventMov_Purch.updateAutoLossProfit</span></span>|
|<span data-ttu-id="d55af-213">InventMov_Purch.updateBuffer</span><span class="sxs-lookup"><span data-stu-id="d55af-213">InventMov_Purch.updateBuffer</span></span>|
|<span data-ttu-id="d55af-214">InventMovement.checkUpdatePhysical</span><span class="sxs-lookup"><span data-stu-id="d55af-214">InventMovement.checkUpdatePhysical</span></span>|
|<span data-ttu-id="d55af-215">InventoryLookupMatrixView.ExtensibleViews</span><span class="sxs-lookup"><span data-stu-id="d55af-215">InventoryLookupMatrixView.ExtensibleViews</span></span>|
|<span data-ttu-id="d55af-216">InventTable.pdsValidateBestBeforeDays</span><span class="sxs-lookup"><span data-stu-id="d55af-216">InventTable.pdsValidateBestBeforeDays</span></span>|
|<span data-ttu-id="d55af-217">InventTransWMS_Register.updateInventFromMovementServer</span><span class="sxs-lookup"><span data-stu-id="d55af-217">InventTransWMS_Register.updateInventFromMovementServer</span></span>|
|<span data-ttu-id="d55af-218">InventUpd_ChildReference.updateLessIssue</span><span class="sxs-lookup"><span data-stu-id="d55af-218">InventUpd_ChildReference.updateLessIssue</span></span>|
|<span data-ttu-id="d55af-219">InventUpd_ChildReference.updateLessReceipt</span><span class="sxs-lookup"><span data-stu-id="d55af-219">InventUpd_ChildReference.updateLessReceipt</span></span>|
|<span data-ttu-id="d55af-220">InventUpd_ChildReference.updateMoreIssue</span><span class="sxs-lookup"><span data-stu-id="d55af-220">InventUpd_ChildReference.updateMoreIssue</span></span>|
|<span data-ttu-id="d55af-221">InventUpd_ChildReference.updateMoreReceipt</span><span class="sxs-lookup"><span data-stu-id="d55af-221">InventUpd_ChildReference.updateMoreReceipt</span></span>|
|<span data-ttu-id="d55af-222">InventUpd_Financial.newSalesInvoice</span><span class="sxs-lookup"><span data-stu-id="d55af-222">InventUpd_Financial.newSalesInvoice</span></span>|
|<span data-ttu-id="d55af-223">InventUpd_Physical.updatePhysicalIssue</span><span class="sxs-lookup"><span data-stu-id="d55af-223">InventUpd_Physical.updatePhysicalIssue</span></span>|
|<span data-ttu-id="d55af-224">InventUpd_Physical.updateTransPhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="d55af-224">InventUpd_Physical.updateTransPhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="d55af-225">InventUpd_Physical::newSalesPackingSlip</span><span class="sxs-lookup"><span data-stu-id="d55af-225">InventUpd_Physical::newSalesPackingSlip</span></span>|
|<span data-ttu-id="d55af-226">InventUpd_Reservation.updateNow</span><span class="sxs-lookup"><span data-stu-id="d55af-226">InventUpd_Reservation.updateNow</span></span>|
|<span data-ttu-id="d55af-227">InventUpd_Reservation.updateReserveMore</span><span class="sxs-lookup"><span data-stu-id="d55af-227">InventUpd_Reservation.updateReserveMore</span></span>|
|<span data-ttu-id="d55af-228">InventUpdate.updateInventTransPosting</span><span class="sxs-lookup"><span data-stu-id="d55af-228">InventUpdate.updateInventTransPosting</span></span>|
|<span data-ttu-id="d55af-229">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-229">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="d55af-230">InventUpdate.writeInventTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-230">InventUpdate.writeInventTrans</span></span>|
|<span data-ttu-id="d55af-231">InventUpdateMarking.addMarking</span><span class="sxs-lookup"><span data-stu-id="d55af-231">InventUpdateMarking.addMarking</span></span>|
|<span data-ttu-id="d55af-232">InventUpdateMarking.removeMarking</span><span class="sxs-lookup"><span data-stu-id="d55af-232">InventUpdateMarking.removeMarking</span></span>|
|<span data-ttu-id="d55af-233">InventUpdateReserveMore.createQueryRuns</span><span class="sxs-lookup"><span data-stu-id="d55af-233">InventUpdateReserveMore.createQueryRuns</span></span>|
|<span data-ttu-id="d55af-234">JmgCalcApprovePickDialog.closeOk</span><span class="sxs-lookup"><span data-stu-id="d55af-234">JmgCalcApprovePickDialog.closeOk</span></span>|
|<span data-ttu-id="d55af-235">JmgJobBundle.postTime</span><span class="sxs-lookup"><span data-stu-id="d55af-235">JmgJobBundle.postTime</span></span>|
|<span data-ttu-id="d55af-236">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span><span class="sxs-lookup"><span data-stu-id="d55af-236">JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback</span></span>|
|<span data-ttu-id="d55af-237">JournalStaticDataModel.initializeJournalTableFields</span><span class="sxs-lookup"><span data-stu-id="d55af-237">JournalStaticDataModel.initializeJournalTableFields</span></span>|
|<span data-ttu-id="d55af-238">Ledger.populateTmpTable</span><span class="sxs-lookup"><span data-stu-id="d55af-238">Ledger.populateTmpTable</span></span>|
|<span data-ttu-id="d55af-239">Ledger::populateTmpTable</span><span class="sxs-lookup"><span data-stu-id="d55af-239">Ledger::populateTmpTable</span></span>|
|<span data-ttu-id="d55af-240">LedgerAccrualTrans_Calendar.allocate</span><span class="sxs-lookup"><span data-stu-id="d55af-240">LedgerAccrualTrans_Calendar.allocate</span></span>|
|<span data-ttu-id="d55af-241">LedgerAccrualTrans_Calendar.allocate</span><span class="sxs-lookup"><span data-stu-id="d55af-241">LedgerAccrualTrans_Calendar.allocate</span></span>|
|<span data-ttu-id="d55af-242">LedgerAccrualTrans_Fiscal.allocate</span><span class="sxs-lookup"><span data-stu-id="d55af-242">LedgerAccrualTrans_Fiscal.allocate</span></span>|
|<span data-ttu-id="d55af-243">LedgerAccrualTrans_Fiscal.allocate</span><span class="sxs-lookup"><span data-stu-id="d55af-243">LedgerAccrualTrans_Fiscal.allocate</span></span>|
|<span data-ttu-id="d55af-244">LedgerAutomaticTransactionAccountEntity</span><span class="sxs-lookup"><span data-stu-id="d55af-244">LedgerAutomaticTransactionAccountEntity</span></span>|
|<span data-ttu-id="d55af-245">LedgerCreatePeriodBalances.createPeriodBalancesMainAccount</span><span class="sxs-lookup"><span data-stu-id="d55af-245">LedgerCreatePeriodBalances.createPeriodBalancesMainAccount</span></span>|
|<span data-ttu-id="d55af-246">LedgerExchAdj.postAdjustment</span><span class="sxs-lookup"><span data-stu-id="d55af-246">LedgerExchAdj.postAdjustment</span></span>|
|<span data-ttu-id="d55af-247">LedgerExchAdj.run</span><span class="sxs-lookup"><span data-stu-id="d55af-247">LedgerExchAdj.run</span></span>|
|<span data-ttu-id="d55af-248">LedgerFiscalJournalDP_IT.getDisplaySequenceNumber</span><span class="sxs-lookup"><span data-stu-id="d55af-248">LedgerFiscalJournalDP_IT.getDisplaySequenceNumber</span></span>|
|<span data-ttu-id="d55af-249">LedgerJournalCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-249">LedgerJournalCheckPost.checkJournal</span></span>|
|<span data-ttu-id="d55af-250">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-250">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="d55af-251">LedgerJournalCheckPost.runInternal</span><span class="sxs-lookup"><span data-stu-id="d55af-251">LedgerJournalCheckPost.runInternal</span></span>|
|<span data-ttu-id="d55af-252">LedgerJournalEngine.accountModified</span><span class="sxs-lookup"><span data-stu-id="d55af-252">LedgerJournalEngine.accountModified</span></span>|
|<span data-ttu-id="d55af-253">LedgerJournalEngine.calculateTaxForCompleteJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-253">LedgerJournalEngine.calculateTaxForCompleteJournal</span></span>|
|<span data-ttu-id="d55af-254">LedgerJournalEngine.findSettledAmount</span><span class="sxs-lookup"><span data-stu-id="d55af-254">LedgerJournalEngine.findSettledAmount</span></span>|
|<span data-ttu-id="d55af-255">LedgerJournalEngine.formSettlement</span><span class="sxs-lookup"><span data-stu-id="d55af-255">LedgerJournalEngine.formSettlement</span></span>|
|<span data-ttu-id="d55af-256">LedgerJournalEngine.newVoucher</span><span class="sxs-lookup"><span data-stu-id="d55af-256">LedgerJournalEngine.newVoucher</span></span>|
|<span data-ttu-id="d55af-257">LedgerJournalPeriodicCopy.journalTransCopy</span><span class="sxs-lookup"><span data-stu-id="d55af-257">LedgerJournalPeriodicCopy.journalTransCopy</span></span>|
|<span data-ttu-id="d55af-258">LedgerJournalTrans.checkVATTransaction</span><span class="sxs-lookup"><span data-stu-id="d55af-258">LedgerJournalTrans.checkVATTransaction</span></span>|
|<span data-ttu-id="d55af-259">LedgerJournalTrans.checkVatTransaction</span><span class="sxs-lookup"><span data-stu-id="d55af-259">LedgerJournalTrans.checkVatTransaction</span></span>|
|<span data-ttu-id="d55af-260">LedgerJournalTrans.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="d55af-260">LedgerJournalTrans.validateWrite_Server</span></span>|
|<span data-ttu-id="d55af-261">LedgerJournalTrans_Project.checkCategoryId</span><span class="sxs-lookup"><span data-stu-id="d55af-261">LedgerJournalTrans_Project.checkCategoryId</span></span>|
|<span data-ttu-id="d55af-262">LedgerJournalTransUpdateAsset</span><span class="sxs-lookup"><span data-stu-id="d55af-262">LedgerJournalTransUpdateAsset</span></span>|
|<span data-ttu-id="d55af-263">LedgerJournalTransUpdateLedger.updateNow</span><span class="sxs-lookup"><span data-stu-id="d55af-263">LedgerJournalTransUpdateLedger.updateNow</span></span>|
|<span data-ttu-id="d55af-264">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-264">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span></span>|
|<span data-ttu-id="d55af-265">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-265">LedgerJournalTransVoucherTemplates.createVoucherTemplate</span></span>|
|<span data-ttu-id="d55af-266">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-266">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span></span>|
|<span data-ttu-id="d55af-267">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-267">LedgerJournalTransVoucherTemplates.saveVoucherTemplate</span></span>|
|<span data-ttu-id="d55af-268">LedgerJournalTransVoucherTemplates.SaveVoucherTemplate、CreateVoucherTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-268">LedgerJournalTransVoucherTemplates.SaveVoucherTemplate, CreateVoucherTemplate</span></span>|
|<span data-ttu-id="d55af-269">LedgerPostingGeneralJournalController.addLine</span><span class="sxs-lookup"><span data-stu-id="d55af-269">LedgerPostingGeneralJournalController.addLine</span></span>|
|<span data-ttu-id="d55af-270">LedgerPostingGeneralJournalController.getLineValues</span><span class="sxs-lookup"><span data-stu-id="d55af-270">LedgerPostingGeneralJournalController.getLineValues</span></span>|
|<span data-ttu-id="d55af-271">LedgerTransferOpening.getMainAccountStorageSegment</span><span class="sxs-lookup"><span data-stu-id="d55af-271">LedgerTransferOpening.getMainAccountStorageSegment</span></span>|
|<span data-ttu-id="d55af-272">LedgerTransferOpening.processNewClosingRecordsForOpening</span><span class="sxs-lookup"><span data-stu-id="d55af-272">LedgerTransferOpening.processNewClosingRecordsForOpening</span></span>|
|<span data-ttu-id="d55af-273">LedgerTransferOpening.processQueryForPublicSector</span><span class="sxs-lookup"><span data-stu-id="d55af-273">LedgerTransferOpening.processQueryForPublicSector</span></span>|
|<span data-ttu-id="d55af-274">LedgerTransModule.tax</span><span class="sxs-lookup"><span data-stu-id="d55af-274">LedgerTransModule.tax</span></span>|
|<span data-ttu-id="d55af-275">LedgerVoucherObject.allocateTransaction</span><span class="sxs-lookup"><span data-stu-id="d55af-275">LedgerVoucherObject.allocateTransaction</span></span>|
|<span data-ttu-id="d55af-276">LedgerVoucherObject.updateLedgerPostingJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-276">LedgerVoucherObject.updateLedgerPostingJournal</span></span>|
|<span data-ttu-id="d55af-277">LogisticsEntityLocationFormHandler.manageControls</span><span class="sxs-lookup"><span data-stu-id="d55af-277">LogisticsEntityLocationFormHandler.manageControls</span></span>|
|<span data-ttu-id="d55af-278">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span><span class="sxs-lookup"><span data-stu-id="d55af-278">LogisticsPostalAddressFormEventHandler.updatePrimaryControl</span></span>|
|<span data-ttu-id="d55af-279">MainAccount.canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="d55af-279">MainAccount.canSubmitToWorkflow</span></span>|
|<span data-ttu-id="d55af-280">可能であれば変数宣言を最初の割り当てに移動</span><span class="sxs-lookup"><span data-stu-id="d55af-280">Move variable declaration to first assignment when possible</span></span>|
|<span data-ttu-id="d55af-281">NewElement.NewMethod</span><span class="sxs-lookup"><span data-stu-id="d55af-281">NewElement.NewMethod</span></span>|
|<span data-ttu-id="d55af-282">OmOperatingUnit.getDimensionViewId</span><span class="sxs-lookup"><span data-stu-id="d55af-282">OmOperatingUnit.getDimensionViewId</span></span>|
|<span data-ttu-id="d55af-283">Originaldocuments.findFromCustTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-283">Originaldocuments.findFromCustTrans</span></span>|
|<span data-ttu-id="d55af-284">Originaldocuments.findFromGeneralJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-284">Originaldocuments.findFromGeneralJournal</span></span>|
|<span data-ttu-id="d55af-285">PaymSchedCalc.createCustVendTransaction</span><span class="sxs-lookup"><span data-stu-id="d55af-285">PaymSchedCalc.createCustVendTransaction</span></span>|
|<span data-ttu-id="d55af-286">PaymSchedCalc.initFromPurchTotals</span><span class="sxs-lookup"><span data-stu-id="d55af-286">PaymSchedCalc.initFromPurchTotals</span></span>|
|<span data-ttu-id="d55af-287">PaymSchedCalc.initFromSalesTotals</span><span class="sxs-lookup"><span data-stu-id="d55af-287">PaymSchedCalc.initFromSalesTotals</span></span>|
|<span data-ttu-id="d55af-288">POSApidts.NewTrigger</span><span class="sxs-lookup"><span data-stu-id="d55af-288">POSApidts.NewTrigger</span></span>|
|<span data-ttu-id="d55af-289">PosAPidts.NewTrigger</span><span class="sxs-lookup"><span data-stu-id="d55af-289">PosAPidts.NewTrigger</span></span>|
|<span data-ttu-id="d55af-290">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span><span class="sxs-lookup"><span data-stu-id="d55af-290">PriceDiscAdmCheckPost.checkForOverlapsAndGaps</span></span>|
|<span data-ttu-id="d55af-291">PriceDiscAdmCheckPost.runFromContract</span><span class="sxs-lookup"><span data-stu-id="d55af-291">PriceDiscAdmCheckPost.runFromContract</span></span>|
|<span data-ttu-id="d55af-292">PriceDiscTable.buildSearchFilter</span><span class="sxs-lookup"><span data-stu-id="d55af-292">PriceDiscTable.buildSearchFilter</span></span>|
|<span data-ttu-id="d55af-293">PrintableReceipt</span><span class="sxs-lookup"><span data-stu-id="d55af-293">PrintableReceipt</span></span>|
|<span data-ttu-id="d55af-294">ProjAdjustmentUpdate.newPostAdjustment</span><span class="sxs-lookup"><span data-stu-id="d55af-294">ProjAdjustmentUpdate.newPostAdjustment</span></span>|
|<span data-ttu-id="d55af-295">ProjAdjustmentUpdate.projTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-295">ProjAdjustmentUpdate.projTrans</span></span>|
|<span data-ttu-id="d55af-296">ProjAdjustmentUpdate.transEmplNew</span><span class="sxs-lookup"><span data-stu-id="d55af-296">ProjAdjustmentUpdate.transEmplNew</span></span>|
|<span data-ttu-id="d55af-297">ProjAdjustmentUpdate_Post.Post</span><span class="sxs-lookup"><span data-stu-id="d55af-297">ProjAdjustmentUpdate_Post.Post</span></span>|
|<span data-ttu-id="d55af-298">ProjAdjustmentUpdate_Post.update</span><span class="sxs-lookup"><span data-stu-id="d55af-298">ProjAdjustmentUpdate_Post.update</span></span>|
|<span data-ttu-id="d55af-299">ProjBudgetManager.createBudgetRevenueForecast、createBudgetSalesForecast</span><span class="sxs-lookup"><span data-stu-id="d55af-299">ProjBudgetManager.createBudgetRevenueForecast, createBudgetSalesForecast</span></span>|
|<span data-ttu-id="d55af-300">ProjBudgetManager.insertProjBudgetLine</span><span class="sxs-lookup"><span data-stu-id="d55af-300">ProjBudgetManager.insertProjBudgetLine</span></span>|
|<span data-ttu-id="d55af-301">ProjBudgetManager.insertProjBudgetLine</span><span class="sxs-lookup"><span data-stu-id="d55af-301">ProjBudgetManager.insertProjBudgetLine</span></span>|
|<span data-ttu-id="d55af-302">ProjBudgetManager.updateProjBudgetLinesWithAmt</span><span class="sxs-lookup"><span data-stu-id="d55af-302">ProjBudgetManager.updateProjBudgetLinesWithAmt</span></span>|
|<span data-ttu-id="d55af-303">ProjCategory.categoryType2CategoryEmplOption</span><span class="sxs-lookup"><span data-stu-id="d55af-303">ProjCategory.categoryType2CategoryEmplOption</span></span>|
|<span data-ttu-id="d55af-304">ProjCategory.categoryType2CategoryEmplOption</span><span class="sxs-lookup"><span data-stu-id="d55af-304">ProjCategory.categoryType2CategoryEmplOption</span></span>|
|<span data-ttu-id="d55af-305">ProjCategory.categoryType2TransType</span><span class="sxs-lookup"><span data-stu-id="d55af-305">ProjCategory.categoryType2TransType</span></span>|
|<span data-ttu-id="d55af-306">Projcategory.transType2CategoryType</span><span class="sxs-lookup"><span data-stu-id="d55af-306">Projcategory.transType2CategoryType</span></span>|
|<span data-ttu-id="d55af-307">Projcontrol.categoryType2CostType</span><span class="sxs-lookup"><span data-stu-id="d55af-307">Projcontrol.categoryType2CostType</span></span>|
|<span data-ttu-id="d55af-308">Projcontrol.costType2CategoryType</span><span class="sxs-lookup"><span data-stu-id="d55af-308">Projcontrol.costType2CategoryType</span></span>|
|<span data-ttu-id="d55af-309">ProjControlPosting.insertControlTrans、processSalesValue</span><span class="sxs-lookup"><span data-stu-id="d55af-309">ProjControlPosting.insertControlTrans, processSalesValue</span></span>|
|<span data-ttu-id="d55af-310">ProjectSourceDocumentLineItemHelper.projOrigin および projTransType</span><span class="sxs-lookup"><span data-stu-id="d55af-310">ProjectSourceDocumentLineItemHelper.projOrigin and projTransType</span></span>|
|<span data-ttu-id="d55af-311">ProjForecastListPageInteraction.runForcastFormBasedOnForecastUnion</span><span class="sxs-lookup"><span data-stu-id="d55af-311">ProjForecastListPageInteraction.runForcastFormBasedOnForecastUnion</span></span>|
|<span data-ttu-id="d55af-312">ProjForecastReduce.newProjPost</span><span class="sxs-lookup"><span data-stu-id="d55af-312">ProjForecastReduce.newProjPost</span></span>|
|<span data-ttu-id="d55af-313">ProjFormLetter メソッド main/mainOnServer</span><span class="sxs-lookup"><span data-stu-id="d55af-313">ProjFormLetter method main/mainOnServer</span></span>|
|<span data-ttu-id="d55af-314">ProjInvoiceCancel.cancelProposal</span><span class="sxs-lookup"><span data-stu-id="d55af-314">ProjInvoiceCancel.cancelProposal</span></span>|
|<span data-ttu-id="d55af-315">ProjInvoiceChoose.run</span><span class="sxs-lookup"><span data-stu-id="d55af-315">ProjInvoiceChoose.run</span></span>|
|<span data-ttu-id="d55af-316">ProjInvoiceJournalCreate.createJournalHeader</span><span class="sxs-lookup"><span data-stu-id="d55af-316">ProjInvoiceJournalCreate.createJournalHeader</span></span>|
|<span data-ttu-id="d55af-317">ProjInvoiceLines.run</span><span class="sxs-lookup"><span data-stu-id="d55af-317">ProjInvoiceLines.run</span></span>|
|<span data-ttu-id="d55af-318">ProjInvoiceProposalCreateLines.loadLastValue</span><span class="sxs-lookup"><span data-stu-id="d55af-318">ProjInvoiceProposalCreateLines.loadLastValue</span></span>|
|<span data-ttu-id="d55af-319">ProjInvoiceProposalCreateLines.runItemQuery</span><span class="sxs-lookup"><span data-stu-id="d55af-319">ProjInvoiceProposalCreateLines.runItemQuery</span></span>|
|<span data-ttu-id="d55af-320">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="d55af-320">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="d55af-321">ProjInvoiceProposalInsertLines.setProjProposalJour</span><span class="sxs-lookup"><span data-stu-id="d55af-321">ProjInvoiceProposalInsertLines.setProjProposalJour</span></span>|
|<span data-ttu-id="d55af-322">ProjInvoiceProposalInsertLines.setProjProposalJour</span><span class="sxs-lookup"><span data-stu-id="d55af-322">ProjInvoiceProposalInsertLines.setProjProposalJour</span></span>|
|<span data-ttu-id="d55af-323">ProjInvoiceProposalInsertLines.setProjProposalTotals</span><span class="sxs-lookup"><span data-stu-id="d55af-323">ProjInvoiceProposalInsertLines.setProjProposalTotals</span></span>|
|<span data-ttu-id="d55af-324">ProjInvoiceTableCreate.initializeValues</span><span class="sxs-lookup"><span data-stu-id="d55af-324">ProjInvoiceTableCreate.initializeValues</span></span>|
|<span data-ttu-id="d55af-325">Projparameters.defaultProjCategory</span><span class="sxs-lookup"><span data-stu-id="d55af-325">Projparameters.defaultProjCategory</span></span>|
|<span data-ttu-id="d55af-326">ProjPeriodPostingLedgerCost.updateTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-326">ProjPeriodPostingLedgerCost.updateTrans</span></span>|
|<span data-ttu-id="d55af-327">ProjPost.newCheckTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-327">ProjPost.newCheckTrans</span></span>|
|<span data-ttu-id="d55af-328">Projpost.newCreateProjTransAndLedger</span><span class="sxs-lookup"><span data-stu-id="d55af-328">Projpost.newCreateProjTransAndLedger</span></span>|
|<span data-ttu-id="d55af-329">Projpost.newCreateProjTransAndLedgerAdj</span><span class="sxs-lookup"><span data-stu-id="d55af-329">Projpost.newCreateProjTransAndLedgerAdj</span></span>|
|<span data-ttu-id="d55af-330">Projpost.newTransAdjNegativeJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-330">Projpost.newTransAdjNegativeJournal</span></span>|
|<span data-ttu-id="d55af-331">Projpost.postcost</span><span class="sxs-lookup"><span data-stu-id="d55af-331">Projpost.postcost</span></span>|
|<span data-ttu-id="d55af-332">ProjSalesItemReq.modified</span><span class="sxs-lookup"><span data-stu-id="d55af-332">ProjSalesItemReq.modified</span></span>|
|<span data-ttu-id="d55af-333">ProjSplitBill.transType</span><span class="sxs-lookup"><span data-stu-id="d55af-333">ProjSplitBill.transType</span></span>|
|<span data-ttu-id="d55af-334">ProjSplitBill.transType</span><span class="sxs-lookup"><span data-stu-id="d55af-334">ProjSplitBill.transType</span></span>|
|<span data-ttu-id="d55af-335">ProjTable.generateNextSubProjectId</span><span class="sxs-lookup"><span data-stu-id="d55af-335">ProjTable.generateNextSubProjectId</span></span>|
|<span data-ttu-id="d55af-336">ProjTableCreate.canClose</span><span class="sxs-lookup"><span data-stu-id="d55af-336">ProjTableCreate.canClose</span></span>|
|<span data-ttu-id="d55af-337">ProjTableLookup.isJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-337">ProjTableLookup.isJournal</span></span>|
|<span data-ttu-id="d55af-338">ProjTableWizardCtrl.createProject</span><span class="sxs-lookup"><span data-stu-id="d55af-338">ProjTableWizardCtrl.createProject</span></span>|
|<span data-ttu-id="d55af-339">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="d55af-339">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="d55af-340">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="d55af-340">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="d55af-341">PsaProjAndContractInvoiceController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="d55af-341">PsaProjAndContractInvoiceController.getReportTitle</span></span>|
|<span data-ttu-id="d55af-342">PSAProjRetainerInvoicing.run</span><span class="sxs-lookup"><span data-stu-id="d55af-342">PSAProjRetainerInvoicing.run</span></span>|
|<span data-ttu-id="d55af-343">PsaQuotationsController.getReportTitle</span><span class="sxs-lookup"><span data-stu-id="d55af-343">PsaQuotationsController.getReportTitle</span></span>|
|<span data-ttu-id="d55af-344">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="d55af-344">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="d55af-345">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="d55af-345">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="d55af-346">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span><span class="sxs-lookup"><span data-stu-id="d55af-346">PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState</span></span>|
|<span data-ttu-id="d55af-347">PurchAutoCreate_Sales.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="d55af-347">PurchAutoCreate_Sales.createPurchTable</span></span>|
|<span data-ttu-id="d55af-348">PurchAutoCreate_Sales.setPurchTable</span><span class="sxs-lookup"><span data-stu-id="d55af-348">PurchAutoCreate_Sales.setPurchTable</span></span>|
|<span data-ttu-id="d55af-349">PurchCalcTax_Invoice.updateTaxWriteCode</span><span class="sxs-lookup"><span data-stu-id="d55af-349">PurchCalcTax_Invoice.updateTaxWriteCode</span></span>|
|<span data-ttu-id="d55af-350">PurchCopying.copyLine</span><span class="sxs-lookup"><span data-stu-id="d55af-350">PurchCopying.copyLine</span></span>|
|<span data-ttu-id="d55af-351">PurchCreateFromSalesOrder.autoCreatePurchOrder</span><span class="sxs-lookup"><span data-stu-id="d55af-351">PurchCreateFromSalesOrder.autoCreatePurchOrder</span></span>|
|<span data-ttu-id="d55af-352">PurchFormletter_Invoice.newinvoice</span><span class="sxs-lookup"><span data-stu-id="d55af-352">PurchFormletter_Invoice.newinvoice</span></span>|
|<span data-ttu-id="d55af-353">PurchFormletter_Packingslip.runProjectPostings</span><span class="sxs-lookup"><span data-stu-id="d55af-353">PurchFormletter_Packingslip.runProjectPostings</span></span>|
|<span data-ttu-id="d55af-354">PurchFormletterParmData.createParmLine</span><span class="sxs-lookup"><span data-stu-id="d55af-354">PurchFormletterParmData.createParmLine</span></span>|
|<span data-ttu-id="d55af-355">PurchFormletterParmData.newData</span><span class="sxs-lookup"><span data-stu-id="d55af-355">PurchFormletterParmData.newData</span></span>|
|<span data-ttu-id="d55af-356">PurchFormLetterParmData.reSelectLines</span><span class="sxs-lookup"><span data-stu-id="d55af-356">PurchFormLetterParmData.reSelectLines</span></span>|
|<span data-ttu-id="d55af-357">PurchFormletterParmDataInvoice.chooseLinesNext</span><span class="sxs-lookup"><span data-stu-id="d55af-357">PurchFormletterParmDataInvoice.chooseLinesNext</span></span>|
|<span data-ttu-id="d55af-358">PurchFormletterParmDataInvoice.cleanupChooseLines</span><span class="sxs-lookup"><span data-stu-id="d55af-358">PurchFormletterParmDataInvoice.cleanupChooseLines</span></span>|
|<span data-ttu-id="d55af-359">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span><span class="sxs-lookup"><span data-stu-id="d55af-359">PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder</span></span>|
|<span data-ttu-id="d55af-360">PurchFormletterParmDataInvoice.processAdditional</span><span class="sxs-lookup"><span data-stu-id="d55af-360">PurchFormletterParmDataInvoice.processAdditional</span></span>|
|<span data-ttu-id="d55af-361">PurchFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="d55af-361">PurchFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="d55af-362">PurchInvoiceJournalCreate.checkInvoice</span><span class="sxs-lookup"><span data-stu-id="d55af-362">PurchInvoiceJournalCreate.checkInvoice</span></span>|
|<span data-ttu-id="d55af-363">PurchInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="d55af-363">PurchInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="d55af-364">PurchLine.delete</span><span class="sxs-lookup"><span data-stu-id="d55af-364">PurchLine.delete</span></span>|
|<span data-ttu-id="d55af-365">PurchLine.setProjSalesPrice</span><span class="sxs-lookup"><span data-stu-id="d55af-365">PurchLine.setProjSalesPrice</span></span>|
|<span data-ttu-id="d55af-366">PurchLine.update</span><span class="sxs-lookup"><span data-stu-id="d55af-366">PurchLine.update</span></span>|
|<span data-ttu-id="d55af-367">PurchLine.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="d55af-367">PurchLine.validateWrite_Server</span></span>|
|<span data-ttu-id="d55af-368">PurchLineCopy.canClose</span><span class="sxs-lookup"><span data-stu-id="d55af-368">PurchLineCopy.canClose</span></span>|
|<span data-ttu-id="d55af-369">PurchLineType.syncSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-369">PurchLineType.syncSalesLine</span></span>|
|<span data-ttu-id="d55af-370">PurchLineType.updateInventory</span><span class="sxs-lookup"><span data-stu-id="d55af-370">PurchLineType.updateInventory</span></span>|
|<span data-ttu-id="d55af-371">PurchLineType.updatePurchStatus</span><span class="sxs-lookup"><span data-stu-id="d55af-371">PurchLineType.updatePurchStatus</span></span>|
|<span data-ttu-id="d55af-372">PurchLineType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="d55af-372">PurchLineType.validateDelete</span></span>|
|<span data-ttu-id="d55af-373">PurchPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="d55af-373">PurchPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="d55af-374">PurchPackingSlipJournalPost.updateSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-374">PurchPackingSlipJournalPost.updateSalesLine</span></span>|
|<span data-ttu-id="d55af-375">PurchPackingSlipJournalPost.updateSalesTable</span><span class="sxs-lookup"><span data-stu-id="d55af-375">PurchPackingSlipJournalPost.updateSalesTable</span></span>|
|<span data-ttu-id="d55af-376">PurchPackingSlipJournalPost.updateSourceLine</span><span class="sxs-lookup"><span data-stu-id="d55af-376">PurchPackingSlipJournalPost.updateSourceLine</span></span>|
|<span data-ttu-id="d55af-377">PurchQuantity_PackingSlip.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="d55af-377">PurchQuantity_PackingSlip.calcQtyInvent</span></span>|
|<span data-ttu-id="d55af-378">PurchQuantity_PackingSlip.calcQtyPurch</span><span class="sxs-lookup"><span data-stu-id="d55af-378">PurchQuantity_PackingSlip.calcQtyPurch</span></span>|
|<span data-ttu-id="d55af-379">PurchReqAddItems.init</span><span class="sxs-lookup"><span data-stu-id="d55af-379">PurchReqAddItems.init</span></span>|
|<span data-ttu-id="d55af-380">PurchReqTable.init</span><span class="sxs-lookup"><span data-stu-id="d55af-380">PurchReqTable.init</span></span>|
|<span data-ttu-id="d55af-381">PurchReqWFExpendiParticipantProvider.resolve</span><span class="sxs-lookup"><span data-stu-id="d55af-381">PurchReqWFExpendiParticipantProvider.resolve</span></span>|
|<span data-ttu-id="d55af-382">PurchSelectLinesManager.mark</span><span class="sxs-lookup"><span data-stu-id="d55af-382">PurchSelectLinesManager.mark</span></span>|
|<span data-ttu-id="d55af-383">PurchTableForm.purchLine_WritePreSuper</span><span class="sxs-lookup"><span data-stu-id="d55af-383">PurchTableForm.purchLine_WritePreSuper</span></span>|
|<span data-ttu-id="d55af-384">PurchTableInteractionHelper.getDeliveryScheduleEnabled</span><span class="sxs-lookup"><span data-stu-id="d55af-384">PurchTableInteractionHelper.getDeliveryScheduleEnabled</span></span>|
|<span data-ttu-id="d55af-385">PurchTableInteractionHelper.getHasMultipleDeliveries</span><span class="sxs-lookup"><span data-stu-id="d55af-385">PurchTableInteractionHelper.getHasMultipleDeliveries</span></span>|
|<span data-ttu-id="d55af-386">PurchUpdateRemain.updateRemainPhysical</span><span class="sxs-lookup"><span data-stu-id="d55af-386">PurchUpdateRemain.updateRemainPhysical</span></span>|
|<span data-ttu-id="d55af-387">ReqCalc.insertItemInventSum</span><span class="sxs-lookup"><span data-stu-id="d55af-387">ReqCalc.insertItemInventSum</span></span>|
|<span data-ttu-id="d55af-388">ReqTransPlanIdFilter.setPlanIdOnQueryRange</span><span class="sxs-lookup"><span data-stu-id="d55af-388">ReqTransPlanIdFilter.setPlanIdOnQueryRange</span></span>|
|<span data-ttu-id="d55af-389">ReqTransPoMarkFirm.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="d55af-389">ReqTransPoMarkFirm.createPurchLine</span></span>|
|<span data-ttu-id="d55af-390">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="d55af-390">ReqTransPoMarkFirm.createPurchTable</span></span>|
|<span data-ttu-id="d55af-391">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="d55af-391">ReqTransPoMarkFirm.createPurchTable</span></span>|
|<span data-ttu-id="d55af-392">ReqTransPoMarkFirm.dialog</span><span class="sxs-lookup"><span data-stu-id="d55af-392">ReqTransPoMarkFirm.dialog</span></span>|
|<span data-ttu-id="d55af-393">RetailAssortmentLookupTask.CreateChannelGroups</span><span class="sxs-lookup"><span data-stu-id="d55af-393">RetailAssortmentLookupTask.CreateChannelGroups</span></span>|
|<span data-ttu-id="d55af-394">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span><span class="sxs-lookup"><span data-stu-id="d55af-394">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span></span>|
|<span data-ttu-id="d55af-395">RetailPackage.close</span><span class="sxs-lookup"><span data-stu-id="d55af-395">RetailPackage.close</span></span>|
|<span data-ttu-id="d55af-396">RetailProductPropertyManager.saveProductDimensions</span><span class="sxs-lookup"><span data-stu-id="d55af-396">RetailProductPropertyManager.saveProductDimensions</span></span>|
|<span data-ttu-id="d55af-397">RetailStatementPostChecker::checkStatement</span><span class="sxs-lookup"><span data-stu-id="d55af-397">RetailStatementPostChecker::checkStatement</span></span>|
|<span data-ttu-id="d55af-398">ReturnTable.isDispositionCodeValid</span><span class="sxs-lookup"><span data-stu-id="d55af-398">ReturnTable.isDispositionCodeValid</span></span>|
|<span data-ttu-id="d55af-399">RouteCopyToRoute</span><span class="sxs-lookup"><span data-stu-id="d55af-399">RouteCopyToRoute</span></span>|
|<span data-ttu-id="d55af-400">SalesCalcAvailableDlvDates.newCommonSalesDlvDateType</span><span class="sxs-lookup"><span data-stu-id="d55af-400">SalesCalcAvailableDlvDates.newCommonSalesDlvDateType</span></span>|
|<span data-ttu-id="d55af-401">SalesCalcAvailableDlvDates.newCommonSalesDlvDateTypeByEntity</span><span class="sxs-lookup"><span data-stu-id="d55af-401">SalesCalcAvailableDlvDates.newCommonSalesDlvDateTypeByEntity</span></span>|
|<span data-ttu-id="d55af-402">SalesCopying.copyLines</span><span class="sxs-lookup"><span data-stu-id="d55af-402">SalesCopying.copyLines</span></span>|
|<span data-ttu-id="d55af-403">SalesEditLines.FormDesign/FormMenuFunctionButtonControl/ButtonPaymentSched/Method/clicked</span><span class="sxs-lookup"><span data-stu-id="d55af-403">SalesEditLines.FormDesign/FormMenuFunctionButtonControl/ButtonPaymentSched/Method/clicked</span></span>|
|<span data-ttu-id="d55af-404">SalesFormLetter.onCreatePaymSched</span><span class="sxs-lookup"><span data-stu-id="d55af-404">SalesFormLetter.onCreatePaymSched</span></span>|
|<span data-ttu-id="d55af-405">SalesFormLetterParmDataPackingSlip.selectChooseLines</span><span class="sxs-lookup"><span data-stu-id="d55af-405">SalesFormLetterParmDataPackingSlip.selectChooseLines</span></span>|
|<span data-ttu-id="d55af-406">SalesFormletterProvider.checkLines</span><span class="sxs-lookup"><span data-stu-id="d55af-406">SalesFormletterProvider.checkLines</span></span>|
|<span data-ttu-id="d55af-407">SalesFormletterProvider.checkSalesLineChanged</span><span class="sxs-lookup"><span data-stu-id="d55af-407">SalesFormletterProvider.checkSalesLineChanged</span></span>|
|<span data-ttu-id="d55af-408">SalesInvoiceController.initFormLetterReport</span><span class="sxs-lookup"><span data-stu-id="d55af-408">SalesInvoiceController.initFormLetterReport</span></span>|
|<span data-ttu-id="d55af-409">SalesInvoiceJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="d55af-409">SalesInvoiceJournalPost.postInventory</span></span>|
|<span data-ttu-id="d55af-410">SalesInvoiceJournalPostProj.updateInventory</span><span class="sxs-lookup"><span data-stu-id="d55af-410">SalesInvoiceJournalPostProj.updateInventory</span></span>|
|<span data-ttu-id="d55af-411">SalesLine.createAlternativeItem</span><span class="sxs-lookup"><span data-stu-id="d55af-411">SalesLine.createAlternativeItem</span></span>|
|<span data-ttu-id="d55af-412">SalesLine.delete</span><span class="sxs-lookup"><span data-stu-id="d55af-412">SalesLine.delete</span></span>|
|<span data-ttu-id="d55af-413">SalesLine.returnLineUpdate</span><span class="sxs-lookup"><span data-stu-id="d55af-413">SalesLine.returnLineUpdate</span></span>|
|<span data-ttu-id="d55af-414">SalesLineCopy.canClose</span><span class="sxs-lookup"><span data-stu-id="d55af-414">SalesLineCopy.canClose</span></span>|
|<span data-ttu-id="d55af-415">SalesLineType.initFromCustInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="d55af-415">SalesLineType.initFromCustInvoiceTrans</span></span>|
|<span data-ttu-id="d55af-416">SalesOrderEntryStatistics.createOrderEntry</span><span class="sxs-lookup"><span data-stu-id="d55af-416">SalesOrderEntryStatistics.createOrderEntry</span></span>|
|<span data-ttu-id="d55af-417">SalesOrderEntryStatistics.deleteOrderEntry</span><span class="sxs-lookup"><span data-stu-id="d55af-417">SalesOrderEntryStatistics.deleteOrderEntry</span></span>|
|<span data-ttu-id="d55af-418">SalesPackingSlipDP.itemId</span><span class="sxs-lookup"><span data-stu-id="d55af-418">SalesPackingSlipDP.itemId</span></span>|
|<span data-ttu-id="d55af-419">SalesPackingSlipJournalPost.postInventory</span><span class="sxs-lookup"><span data-stu-id="d55af-419">SalesPackingSlipJournalPost.postInventory</span></span>|
|<span data-ttu-id="d55af-420">SalesParmLine.setQty</span><span class="sxs-lookup"><span data-stu-id="d55af-420">SalesParmLine.setQty</span></span>|
|<span data-ttu-id="d55af-421">SalesQuantity_Invoice.calcQtyInvent</span><span class="sxs-lookup"><span data-stu-id="d55af-421">SalesQuantity_Invoice.calcQtyInvent</span></span>|
|<span data-ttu-id="d55af-422">SalesQuantity_Invoice.calcQtySales</span><span class="sxs-lookup"><span data-stu-id="d55af-422">SalesQuantity_Invoice.calcQtySales</span></span>|
|<span data-ttu-id="d55af-423">SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesLines</span><span class="sxs-lookup"><span data-stu-id="d55af-423">SalesQuotationEditLinesForm_Sales_Confir method createSalesLines</span></span>|
|<span data-ttu-id="d55af-424">SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesTable</span><span class="sxs-lookup"><span data-stu-id="d55af-424">SalesQuotationEditLinesForm_Sales_Confir method createSalesTable</span></span>|
|<span data-ttu-id="d55af-425">SalesQuotationEditLinesForm_Sales_Confir.createSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-425">SalesQuotationEditLinesForm_Sales_Confir.createSalesLine</span></span>|
|<span data-ttu-id="d55af-426">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span><span class="sxs-lookup"><span data-stu-id="d55af-426">SalesQuotationEditLinesForm_Sales_Confir.createSalesLines</span></span>|
|<span data-ttu-id="d55af-427">SalesQuotationLine.createLine</span><span class="sxs-lookup"><span data-stu-id="d55af-427">SalesQuotationLine.createLine</span></span>|
|<span data-ttu-id="d55af-428">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-428">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="d55af-429">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-429">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="d55af-430">SalesQuotationLine.createQuotationLineFromTemplate</span><span class="sxs-lookup"><span data-stu-id="d55af-430">SalesQuotationLine.createQuotationLineFromTemplate</span></span>|
|<span data-ttu-id="d55af-431">SalesQuotationLine.delete</span><span class="sxs-lookup"><span data-stu-id="d55af-431">SalesQuotationLine.delete</span></span>|
|<span data-ttu-id="d55af-432">SalesQuotationLine.setCostSalesPrice</span><span class="sxs-lookup"><span data-stu-id="d55af-432">SalesQuotationLine.setCostSalesPrice</span></span>|
|<span data-ttu-id="d55af-433">SalesQuotationLine.updateSalesQuotationTable</span><span class="sxs-lookup"><span data-stu-id="d55af-433">SalesQuotationLine.updateSalesQuotationTable</span></span>|
|<span data-ttu-id="d55af-434">SalesQuotationListPageInteraction.initIsSalesQuotation</span><span class="sxs-lookup"><span data-stu-id="d55af-434">SalesQuotationListPageInteraction.initIsSalesQuotation</span></span>|
|<span data-ttu-id="d55af-435">SalesQuotationListPageInteraction.setButtonFollowup</span><span class="sxs-lookup"><span data-stu-id="d55af-435">SalesQuotationListPageInteraction.setButtonFollowup</span></span>|
|<span data-ttu-id="d55af-436">SalesQuotationListPageInteraction.setButtonQuotation</span><span class="sxs-lookup"><span data-stu-id="d55af-436">SalesQuotationListPageInteraction.setButtonQuotation</span></span>|
|<span data-ttu-id="d55af-437">SalesQuotationTableForm_DlvSchedule.updateSalesQuotationLineTable</span><span class="sxs-lookup"><span data-stu-id="d55af-437">SalesQuotationTableForm_DlvSchedule.updateSalesQuotationLineTable</span></span>|
|<span data-ttu-id="d55af-438">SalesQuotationTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="d55af-438">SalesQuotationTableType.validateDelete</span></span>|
|<span data-ttu-id="d55af-439">SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="d55af-439">SalesTable.update</span></span>|
|<span data-ttu-id="d55af-440">SalesTableForm_DeliverySchedule.updateSalesLineTable</span><span class="sxs-lookup"><span data-stu-id="d55af-440">SalesTableForm_DeliverySchedule.updateSalesLineTable</span></span>|
|<span data-ttu-id="d55af-441">SalesTableForm_ProjectSalesItem.resetSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-441">SalesTableForm_ProjectSalesItem.resetSalesLine</span></span>|
|<span data-ttu-id="d55af-442">SalesTableInteractionHelper.isOpenOrderNotReturnNotProjectRelatedSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-442">SalesTableInteractionHelper.isOpenOrderNotReturnNotProjectRelatedSalesLine</span></span>|
|<span data-ttu-id="d55af-443">SalesTableInteractionHelper.notPartiallyPickedPackedOrInvoiced</span><span class="sxs-lookup"><span data-stu-id="d55af-443">SalesTableInteractionHelper.notPartiallyPickedPackedOrInvoiced</span></span>|
|<span data-ttu-id="d55af-444">SalesTableInteractionHelper.notReservedOrderedNorPhysical</span><span class="sxs-lookup"><span data-stu-id="d55af-444">SalesTableInteractionHelper.notReservedOrderedNorPhysical</span></span>|
|<span data-ttu-id="d55af-445">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="d55af-445">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="d55af-446">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="d55af-446">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="d55af-447">SalesTableType.checkUpdate</span><span class="sxs-lookup"><span data-stu-id="d55af-447">SalesTableType.checkUpdate</span></span>|
|<span data-ttu-id="d55af-448">SalesTaxDeclarationInformationReportService.processReport</span><span class="sxs-lookup"><span data-stu-id="d55af-448">SalesTaxDeclarationInformationReportService.processReport</span></span>|
|<span data-ttu-id="d55af-449">SettlementPair_Vend.fetchPayment</span><span class="sxs-lookup"><span data-stu-id="d55af-449">SettlementPair_Vend.fetchPayment</span></span>|
|<span data-ttu-id="d55af-450">smmActivityParentLinkTable.insert</span><span class="sxs-lookup"><span data-stu-id="d55af-450">smmActivityParentLinkTable.insert</span></span>|
|<span data-ttu-id="d55af-451">smmBusRelTable.convert2Customer</span><span class="sxs-lookup"><span data-stu-id="d55af-451">smmBusRelTable.convert2Customer</span></span>|
|<span data-ttu-id="d55af-452">smmBusRelTable.convert2Customer</span><span class="sxs-lookup"><span data-stu-id="d55af-452">smmBusRelTable.convert2Customer</span></span>|
|<span data-ttu-id="d55af-453">SmmBusRelTable.convert2Vendor</span><span class="sxs-lookup"><span data-stu-id="d55af-453">SmmBusRelTable.convert2Vendor</span></span>|
|<span data-ttu-id="d55af-454">SmmBusRelTable.convert2Vendor</span><span class="sxs-lookup"><span data-stu-id="d55af-454">SmmBusRelTable.convert2Vendor</span></span>|
|<span data-ttu-id="d55af-455">smmBusRelTable.createConvertedBusRel</span><span class="sxs-lookup"><span data-stu-id="d55af-455">smmBusRelTable.createConvertedBusRel</span></span>|
|<span data-ttu-id="d55af-456">smmLeadTable.createBusRelRecord</span><span class="sxs-lookup"><span data-stu-id="d55af-456">smmLeadTable.createBusRelRecord</span></span>|
|<span data-ttu-id="d55af-457">SmmProjectCreate.createProjectGroup</span><span class="sxs-lookup"><span data-stu-id="d55af-457">SmmProjectCreate.createProjectGroup</span></span>|
|<span data-ttu-id="d55af-458">SpecTransInsertSetManager.insertDatabase</span><span class="sxs-lookup"><span data-stu-id="d55af-458">SpecTransInsertSetManager.insertDatabase</span></span>|
|<span data-ttu-id="d55af-459">SubledgerJournalizerProjectExtension.createProjectActualCostDetail、createProjectActualHeader</span><span class="sxs-lookup"><span data-stu-id="d55af-459">SubledgerJournalizerProjectExtension.createProjectActualCostDetail, createProjectActualHeader</span></span>|
|<span data-ttu-id="d55af-460">SubledgerJournalizerProjectExtension.getProjectActualMap</span><span class="sxs-lookup"><span data-stu-id="d55af-460">SubledgerJournalizerProjectExtension.getProjectActualMap</span></span>|
|<span data-ttu-id="d55af-461">SuppItemSales.initSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-461">SuppItemSales.initSalesLine</span></span>|
|<span data-ttu-id="d55af-462">テーブル PurchLine.insert</span><span class="sxs-lookup"><span data-stu-id="d55af-462">Table PurchLine.insert</span></span>|
|<span data-ttu-id="d55af-463">テーブル PurchLine.insert</span><span class="sxs-lookup"><span data-stu-id="d55af-463">Table PurchLine.insert</span></span>|
|<span data-ttu-id="d55af-464">テーブル PurchLine.update</span><span class="sxs-lookup"><span data-stu-id="d55af-464">Table PurchLine.update</span></span>|
|<span data-ttu-id="d55af-465">テーブル PurchTable.update</span><span class="sxs-lookup"><span data-stu-id="d55af-465">Table PurchTable.update</span></span>|
|<span data-ttu-id="d55af-466">テーブル PurchTable.update</span><span class="sxs-lookup"><span data-stu-id="d55af-466">Table PurchTable.update</span></span>|
|<span data-ttu-id="d55af-467">テーブル SalesLine.insert</span><span class="sxs-lookup"><span data-stu-id="d55af-467">Table SalesLine.insert</span></span>|
|<span data-ttu-id="d55af-468">テーブル SalesLine.projIdModified</span><span class="sxs-lookup"><span data-stu-id="d55af-468">table SalesLine.projIdModified</span></span>|
|<span data-ttu-id="d55af-469">テーブル SalesLine.salesQtyModifiedInteraction</span><span class="sxs-lookup"><span data-stu-id="d55af-469">table SalesLine.salesQtyModifiedInteraction</span></span>|
|<span data-ttu-id="d55af-470">テーブル SalesLine.update</span><span class="sxs-lookup"><span data-stu-id="d55af-470">Table SalesLine.update</span></span>|
|<span data-ttu-id="d55af-471">テーブル SalesQuotationLine.insert</span><span class="sxs-lookup"><span data-stu-id="d55af-471">Table SalesQuotationLine.insert</span></span>|
|<span data-ttu-id="d55af-472">テーブル SalesQuotationLine.update</span><span class="sxs-lookup"><span data-stu-id="d55af-472">Table SalesQuotationLine.update</span></span>|
|<span data-ttu-id="d55af-473">テーブル SalesQuotationTable.update</span><span class="sxs-lookup"><span data-stu-id="d55af-473">Table SalesQuotationTable.update</span></span>|
|<span data-ttu-id="d55af-474">テーブル SalesQuotationTable.update</span><span class="sxs-lookup"><span data-stu-id="d55af-474">Table SalesQuotationTable.update</span></span>|
|<span data-ttu-id="d55af-475">テーブル SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="d55af-475">Table SalesTable.update</span></span>|
|<span data-ttu-id="d55af-476">テーブル SalesTable.update</span><span class="sxs-lookup"><span data-stu-id="d55af-476">Table SalesTable.update</span></span>|
|<span data-ttu-id="d55af-477">Table\VendTable.name</span><span class="sxs-lookup"><span data-stu-id="d55af-477">Table\VendTable.name</span></span>|
|<span data-ttu-id="d55af-478">Table\VendTable.updateOnHold</span><span class="sxs-lookup"><span data-stu-id="d55af-478">Table\VendTable.updateOnHold</span></span>|
|<span data-ttu-id="d55af-479">Tax.createOrphanLinkInsteadPost_RU</span><span class="sxs-lookup"><span data-stu-id="d55af-479">Tax.createOrphanLinkInsteadPost_RU</span></span>|
|<span data-ttu-id="d55af-480">Tax.distributeTotalTax</span><span class="sxs-lookup"><span data-stu-id="d55af-480">Tax.distributeTotalTax</span></span>|
|<span data-ttu-id="d55af-481">Tax.distributeTotalTax</span><span class="sxs-lookup"><span data-stu-id="d55af-481">Tax.distributeTotalTax</span></span>|
|<span data-ttu-id="d55af-482">Tax.InsertIntersection</span><span class="sxs-lookup"><span data-stu-id="d55af-482">Tax.InsertIntersection</span></span>|
|<span data-ttu-id="d55af-483">Tax.insertIntersection</span><span class="sxs-lookup"><span data-stu-id="d55af-483">Tax.insertIntersection</span></span>|
|<span data-ttu-id="d55af-484">Tax.post</span><span class="sxs-lookup"><span data-stu-id="d55af-484">Tax.post</span></span>|
|<span data-ttu-id="d55af-485">Tax.Post</span><span class="sxs-lookup"><span data-stu-id="d55af-485">Tax.Post</span></span>|
|<span data-ttu-id="d55af-486">Tax.postCharge</span><span class="sxs-lookup"><span data-stu-id="d55af-486">Tax.postCharge</span></span>|
|<span data-ttu-id="d55af-487">Tax.postTaxProjInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="d55af-487">Tax.postTaxProjInvoice_IN</span></span>|
|<span data-ttu-id="d55af-488">Tax.postTaxPurchInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="d55af-488">Tax.postTaxPurchInvoice_IN</span></span>|
|<span data-ttu-id="d55af-489">Tax.postTaxSalesInvoice_IN</span><span class="sxs-lookup"><span data-stu-id="d55af-489">Tax.postTaxSalesInvoice_IN</span></span>|
|<span data-ttu-id="d55af-490">Tax.saveAndPost</span><span class="sxs-lookup"><span data-stu-id="d55af-490">Tax.saveAndPost</span></span>|
|<span data-ttu-id="d55af-491">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="d55af-491">Tax.taxTotals</span></span>|
|<span data-ttu-id="d55af-492">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="d55af-492">Tax.taxTotals</span></span>|
|<span data-ttu-id="d55af-493">Tax.taxTotals</span><span class="sxs-lookup"><span data-stu-id="d55af-493">Tax.taxTotals</span></span>|
|<span data-ttu-id="d55af-494">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="d55af-494">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="d55af-495">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="d55af-495">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="d55af-496">Tax.taxTotalsPosted</span><span class="sxs-lookup"><span data-stu-id="d55af-496">Tax.taxTotalsPosted</span></span>|
|<span data-ttu-id="d55af-497">TaxBookSection.checkTaxBookSection</span><span class="sxs-lookup"><span data-stu-id="d55af-497">TaxBookSection.checkTaxBookSection</span></span>|
|<span data-ttu-id="d55af-498">TaxCalculationAdjustment.calcManualInserted</span><span class="sxs-lookup"><span data-stu-id="d55af-498">TaxCalculationAdjustment.calcManualInserted</span></span>|
|<span data-ttu-id="d55af-499">TaxCalculationJournal.saveTaxTransfers</span><span class="sxs-lookup"><span data-stu-id="d55af-499">TaxCalculationJournal.saveTaxTransfers</span></span>|
|<span data-ttu-id="d55af-500">TaxFreeInvoice_Invoice.updateAndPost</span><span class="sxs-lookup"><span data-stu-id="d55af-500">TaxFreeInvoice_Invoice.updateAndPost</span></span>|
|<span data-ttu-id="d55af-501">TaxInvoiceSpec.parmTaxSpec</span><span class="sxs-lookup"><span data-stu-id="d55af-501">TaxInvoiceSpec.parmTaxSpec</span></span>|
|<span data-ttu-id="d55af-502">TaxListDP.insertTaxListTaxTmpData</span><span class="sxs-lookup"><span data-stu-id="d55af-502">TaxListDP.insertTaxListTaxTmpData</span></span>|
|<span data-ttu-id="d55af-503">TaxListDP.updateTaxListTaxTmpData</span><span class="sxs-lookup"><span data-stu-id="d55af-503">TaxListDP.updateTaxListTaxTmpData</span></span>|
|<span data-ttu-id="d55af-504">TaxMainAccDimensionListProvider.populateMainAccountDimensionList</span><span class="sxs-lookup"><span data-stu-id="d55af-504">TaxMainAccDimensionListProvider.populateMainAccountDimensionList</span></span>|
|<span data-ttu-id="d55af-505">TaxPost.postToLedger</span><span class="sxs-lookup"><span data-stu-id="d55af-505">TaxPost.postToLedger</span></span>|
|<span data-ttu-id="d55af-506">TaxReportController_US.init</span><span class="sxs-lookup"><span data-stu-id="d55af-506">TaxReportController_US.init</span></span>|
|<span data-ttu-id="d55af-507">TaxReportInclAdjustmentDP.insertTaxReportInclAdjustmentTmp</span><span class="sxs-lookup"><span data-stu-id="d55af-507">TaxReportInclAdjustmentDP.insertTaxReportInclAdjustmentTmp</span></span>|
|<span data-ttu-id="d55af-508">TaxReportingDP.insertTaxReportingTmp</span><span class="sxs-lookup"><span data-stu-id="d55af-508">TaxReportingDP.insertTaxReportingTmp</span></span>|
|<span data-ttu-id="d55af-509">TaxReverse.adjustTaxTransDueToExchangeRateGainLoss</span><span class="sxs-lookup"><span data-stu-id="d55af-509">TaxReverse.adjustTaxTransDueToExchangeRateGainLoss</span></span>|
|<span data-ttu-id="d55af-510">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="d55af-510">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="d55af-511">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="d55af-511">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="d55af-512">TaxReverse.postAccountingCurrency</span><span class="sxs-lookup"><span data-stu-id="d55af-512">TaxReverse.postAccountingCurrency</span></span>|
|<span data-ttu-id="d55af-513">TaxReverse.postCharge</span><span class="sxs-lookup"><span data-stu-id="d55af-513">TaxReverse.postCharge</span></span>|
|<span data-ttu-id="d55af-514">TaxReverse.postGainLossInReportingCurrency</span><span class="sxs-lookup"><span data-stu-id="d55af-514">TaxReverse.postGainLossInReportingCurrency</span></span>|
|<span data-ttu-id="d55af-515">TaxSales.calc</span><span class="sxs-lookup"><span data-stu-id="d55af-515">TaxSales.calc</span></span>|
|<span data-ttu-id="d55af-516">TaxSales.calc</span><span class="sxs-lookup"><span data-stu-id="d55af-516">TaxSales.calc</span></span>|
|<span data-ttu-id="d55af-517">TaxSales.calcMarkup</span><span class="sxs-lookup"><span data-stu-id="d55af-517">TaxSales.calcMarkup</span></span>|
|<span data-ttu-id="d55af-518">TaxSales.configureTaxForSalesLine</span><span class="sxs-lookup"><span data-stu-id="d55af-518">TaxSales.configureTaxForSalesLine</span></span>|
|<span data-ttu-id="d55af-519">TaxVoucherService.taxAmountForLedgerType</span><span class="sxs-lookup"><span data-stu-id="d55af-519">TaxVoucherService.taxAmountForLedgerType</span></span>|
|<span data-ttu-id="d55af-520">TmpCustVendTrans.CustTransBalanceCurrency</span><span class="sxs-lookup"><span data-stu-id="d55af-520">TmpCustVendTrans.CustTransBalanceCurrency</span></span>|
|<span data-ttu-id="d55af-521">TmpProjAdjustment.adjustmentType2JournalType</span><span class="sxs-lookup"><span data-stu-id="d55af-521">TmpProjAdjustment.adjustmentType2JournalType</span></span>|
|<span data-ttu-id="d55af-522">TmpProjAdjustment.adjustmentType2TransType</span><span class="sxs-lookup"><span data-stu-id="d55af-522">TmpProjAdjustment.adjustmentType2TransType</span></span>|
|<span data-ttu-id="d55af-523">TmpProjAdjustment.updateFundingLimits</span><span class="sxs-lookup"><span data-stu-id="d55af-523">TmpProjAdjustment.updateFundingLimits</span></span>|
|<span data-ttu-id="d55af-524">TmpProjAdjustmentCreate.salesPrice</span><span class="sxs-lookup"><span data-stu-id="d55af-524">TmpProjAdjustmentCreate.salesPrice</span></span>|
|<span data-ttu-id="d55af-525">TrvExpenseLinesVisibilityController.isVisibilityResetRequired</span><span class="sxs-lookup"><span data-stu-id="d55af-525">TrvExpenseLinesVisibilityController.isVisibilityResetRequired</span></span>|
|<span data-ttu-id="d55af-526">TrvExpenses.updateFormVisibilityOnCategoryChange</span><span class="sxs-lookup"><span data-stu-id="d55af-526">TrvExpenses.updateFormVisibilityOnCategoryChange</span></span>|
|<span data-ttu-id="d55af-527">TrvExpTrans.calcTaxAmount</span><span class="sxs-lookup"><span data-stu-id="d55af-527">TrvExpTrans.calcTaxAmount</span></span>|
|<span data-ttu-id="d55af-528">TrvTaxExpense.calculateTax</span><span class="sxs-lookup"><span data-stu-id="d55af-528">TrvTaxExpense.calculateTax</span></span>|
|<span data-ttu-id="d55af-529">TSTimesheetEntry.init、initFields、setHeaderObjects、validateWrit、lookup</span><span class="sxs-lookup"><span data-stu-id="d55af-529">TSTimesheetEntry.init, initFields, setHeaderObjects, validateWrit, lookup</span></span>|
|<span data-ttu-id="d55af-530">UnitOfMeasureConverter.Convert</span><span class="sxs-lookup"><span data-stu-id="d55af-530">UnitOfMeasureConverter.Convert</span></span>|
|<span data-ttu-id="d55af-531">VendInvoicePaymentAuthorizationTask.postSavedInvoice</span><span class="sxs-lookup"><span data-stu-id="d55af-531">VendInvoicePaymentAuthorizationTask.postSavedInvoice</span></span>|
|<span data-ttu-id="d55af-532">VendPackingSlipTrans.unpostedInvoicePurchQtyServer および VendPackingSlipTrans.unpostedInvoiceInventQtyServer</span><span class="sxs-lookup"><span data-stu-id="d55af-532">VendPackingSlipTrans.unpostedInvoicePurchQtyServer and VendPackingSlipTrans.unpostedInvoiceInventQtyServer</span></span>|
|<span data-ttu-id="d55af-533">VendTable.checkVATNumUsed</span><span class="sxs-lookup"><span data-stu-id="d55af-533">VendTable.checkVATNumUsed</span></span>|
|<span data-ttu-id="d55af-534">VendTax1099Update.calcMiscChargeAmountTax</span><span class="sxs-lookup"><span data-stu-id="d55af-534">VendTax1099Update.calcMiscChargeAmountTax</span></span>|
|<span data-ttu-id="d55af-535">VendTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="d55af-535">VendTrans.documentDateModified</span></span>|
|<span data-ttu-id="d55af-536">VendTrans.documentDateModified</span><span class="sxs-lookup"><span data-stu-id="d55af-536">VendTrans.documentDateModified</span></span>|
|<span data-ttu-id="d55af-537">VendVoucher.createTransOpen</span><span class="sxs-lookup"><span data-stu-id="d55af-537">VendVoucher.createTransOpen</span></span>|
|<span data-ttu-id="d55af-538">VendVoucher.createTransOpen</span><span class="sxs-lookup"><span data-stu-id="d55af-538">VendVoucher.createTransOpen</span></span>|
|<span data-ttu-id="d55af-539">WHSContainerTable.closeContainer</span><span class="sxs-lookup"><span data-stu-id="d55af-539">WHSContainerTable.closeContainer</span></span>|
|<span data-ttu-id="d55af-540">WHSDocumentRouting.translate</span><span class="sxs-lookup"><span data-stu-id="d55af-540">WHSDocumentRouting.translate</span></span>|
|<span data-ttu-id="d55af-541">WHSLoadLine.orderHeader</span><span class="sxs-lookup"><span data-stu-id="d55af-541">WHSLoadLine.orderHeader</span></span>|
|<span data-ttu-id="d55af-542">WHSLoadTable.validateInventTransTypeMatches</span><span class="sxs-lookup"><span data-stu-id="d55af-542">WHSLoadTable.validateInventTransTypeMatches</span></span>|
|<span data-ttu-id="d55af-543">WHSLoadTableAssignOriginInfo.classDeclaration</span><span class="sxs-lookup"><span data-stu-id="d55af-543">WHSLoadTableAssignOriginInfo.classDeclaration</span></span>|
|<span data-ttu-id="d55af-544">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span><span class="sxs-lookup"><span data-stu-id="d55af-544">WmsArrivalCreateJournal.createWMSJournalTransFromTmp</span></span>|
|<span data-ttu-id="d55af-545">WMSOrderTrans.split</span><span class="sxs-lookup"><span data-stu-id="d55af-545">WMSOrderTrans.split</span></span>|
|<span data-ttu-id="d55af-546">WmsOrderTransType_Output.updateReservations</span><span class="sxs-lookup"><span data-stu-id="d55af-546">WmsOrderTransType_Output.updateReservations</span></span>|
|<span data-ttu-id="d55af-547">WorkflowHierarchyProviderHelperEventHandler::getPersonnelNumberIdBySysDictTypeDelegate</span><span class="sxs-lookup"><span data-stu-id="d55af-547">WorkflowHierarchyProviderHelperEventHandler::getPersonnelNumberIdBySysDictTypeDelegate</span></span>|
|<span data-ttu-id="d55af-548">WorkTimeTable.removeDisplayCache</span><span class="sxs-lookup"><span data-stu-id="d55af-548">WorkTimeTable.removeDisplayCache</span></span>|
|<span data-ttu-id="d55af-549">WrkCtrResourceAbilityMapController.insertData</span><span class="sxs-lookup"><span data-stu-id="d55af-549">WrkCtrResourceAbilityMapController.insertData</span></span>|
|<span data-ttu-id="d55af-550">数量の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="d55af-550">Enable increase of decimal precision through extensiblity for quantities</span></span>|

## <a name="enumerations-made-extensible"></a><span data-ttu-id="d55af-551">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="d55af-551">Enumerations made extensible</span></span>

<span data-ttu-id="d55af-552">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="d55af-552">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="d55af-553">列挙型</span><span class="sxs-lookup"><span data-stu-id="d55af-553">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="d55af-554">AssetPostValue</span><span class="sxs-lookup"><span data-stu-id="d55af-554">AssetPostValue</span></span>|
|<span data-ttu-id="d55af-555">AssetPropertyType</span><span class="sxs-lookup"><span data-stu-id="d55af-555">AssetPropertyType</span></span>|
|<span data-ttu-id="d55af-556">AssetStatus</span><span class="sxs-lookup"><span data-stu-id="d55af-556">AssetStatus</span></span>|
|<span data-ttu-id="d55af-557">CaseStatus</span><span class="sxs-lookup"><span data-stu-id="d55af-557">CaseStatus</span></span>|
|<span data-ttu-id="d55af-558">CommissionSalesRepCode</span><span class="sxs-lookup"><span data-stu-id="d55af-558">CommissionSalesRepCode</span></span>|
|<span data-ttu-id="d55af-559">DirSubNameSequenceType</span><span class="sxs-lookup"><span data-stu-id="d55af-559">DirSubNameSequenceType</span></span>|
|<span data-ttu-id="d55af-560">FreightSlipType</span><span class="sxs-lookup"><span data-stu-id="d55af-560">FreightSlipType</span></span>|
|<span data-ttu-id="d55af-561">HRPLimitDocumentType</span><span class="sxs-lookup"><span data-stu-id="d55af-561">HRPLimitDocumentType</span></span>|
|<span data-ttu-id="d55af-562">IntrastatPaymentMethod_IT</span><span class="sxs-lookup"><span data-stu-id="d55af-562">IntrastatPaymentMethod_IT</span></span>|
|<span data-ttu-id="d55af-563">InventBlockingType</span><span class="sxs-lookup"><span data-stu-id="d55af-563">InventBlockingType</span></span>|
|<span data-ttu-id="d55af-564">JmgPaySpecTypeEnumPick</span><span class="sxs-lookup"><span data-stu-id="d55af-564">JmgPaySpecTypeEnumPick</span></span>|
|<span data-ttu-id="d55af-565">KMQuestionAnswerInputType</span><span class="sxs-lookup"><span data-stu-id="d55af-565">KMQuestionAnswerInputType</span></span>|
|<span data-ttu-id="d55af-566">LedgerJournalType</span><span class="sxs-lookup"><span data-stu-id="d55af-566">LedgerJournalType</span></span>|
|<span data-ttu-id="d55af-567">LogisticsAddrZipCodeImportCountryRegion</span><span class="sxs-lookup"><span data-stu-id="d55af-567">LogisticsAddrZipCodeImportCountryRegion</span></span>|
|<span data-ttu-id="d55af-568">LogType</span><span class="sxs-lookup"><span data-stu-id="d55af-568">LogType</span></span>|
|<span data-ttu-id="d55af-569">MarkupModuleType</span><span class="sxs-lookup"><span data-stu-id="d55af-569">MarkupModuleType</span></span>|
|<span data-ttu-id="d55af-570">MarkupModuleType</span><span class="sxs-lookup"><span data-stu-id="d55af-570">MarkupModuleType</span></span>|
|<span data-ttu-id="d55af-571">MCRBrokerValueType</span><span class="sxs-lookup"><span data-stu-id="d55af-571">MCRBrokerValueType</span></span>|
|<span data-ttu-id="d55af-572">PaymentType</span><span class="sxs-lookup"><span data-stu-id="d55af-572">PaymentType</span></span>|
|<span data-ttu-id="d55af-573">PDSCalcElementTypeBase</span><span class="sxs-lookup"><span data-stu-id="d55af-573">PDSCalcElementTypeBase</span></span>|
|<span data-ttu-id="d55af-574">PdsStatus</span><span class="sxs-lookup"><span data-stu-id="d55af-574">PdsStatus</span></span>|
|<span data-ttu-id="d55af-575">PdsVendorCheckItem</span><span class="sxs-lookup"><span data-stu-id="d55af-575">PdsVendorCheckItem</span></span>|
|<span data-ttu-id="d55af-576">ProdStatus</span><span class="sxs-lookup"><span data-stu-id="d55af-576">ProdStatus</span></span>|
|<span data-ttu-id="d55af-577">ProjActiveAll</span><span class="sxs-lookup"><span data-stu-id="d55af-577">ProjActiveAll</span></span>|
|<span data-ttu-id="d55af-578">ProjAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="d55af-578">ProjAdjustmentType</span></span>|
|<span data-ttu-id="d55af-579">ProjAllTrxType</span><span class="sxs-lookup"><span data-stu-id="d55af-579">ProjAllTrxType</span></span>|
|<span data-ttu-id="d55af-580">ProjBudgetAction</span><span class="sxs-lookup"><span data-stu-id="d55af-580">ProjBudgetAction</span></span>|
|<span data-ttu-id="d55af-581">ProjCostType</span><span class="sxs-lookup"><span data-stu-id="d55af-581">ProjCostType</span></span>|
|<span data-ttu-id="d55af-582">ProjForecastInvoiceFrequency</span><span class="sxs-lookup"><span data-stu-id="d55af-582">ProjForecastInvoiceFrequency</span></span>|
|<span data-ttu-id="d55af-583">ProjLinePropertySearch</span><span class="sxs-lookup"><span data-stu-id="d55af-583">ProjLinePropertySearch</span></span>|
|<span data-ttu-id="d55af-584">ProjSalesPriceMarkup</span><span class="sxs-lookup"><span data-stu-id="d55af-584">ProjSalesPriceMarkup</span></span>|
|<span data-ttu-id="d55af-585">ProjSortValue</span><span class="sxs-lookup"><span data-stu-id="d55af-585">ProjSortValue</span></span>|
|<span data-ttu-id="d55af-586">ProjTableEditSubProj</span><span class="sxs-lookup"><span data-stu-id="d55af-586">ProjTableEditSubProj</span></span>|
|<span data-ttu-id="d55af-587">ReqCovType</span><span class="sxs-lookup"><span data-stu-id="d55af-587">ReqCovType</span></span>|
|<span data-ttu-id="d55af-588">ResCharacteristicSetEnum</span><span class="sxs-lookup"><span data-stu-id="d55af-588">ResCharacteristicSetEnum</span></span>|
|<span data-ttu-id="d55af-589">SettlementType</span><span class="sxs-lookup"><span data-stu-id="d55af-589">SettlementType</span></span>|
|<span data-ttu-id="d55af-590">smmShowTimeAs</span><span class="sxs-lookup"><span data-stu-id="d55af-590">smmShowTimeAs</span></span>|
|<span data-ttu-id="d55af-591">SourceDocumentRelationType</span><span class="sxs-lookup"><span data-stu-id="d55af-591">SourceDocumentRelationType</span></span>|
|<span data-ttu-id="d55af-592">TaxRegistrationTypesList</span><span class="sxs-lookup"><span data-stu-id="d55af-592">TaxRegistrationTypesList</span></span>|
|<span data-ttu-id="d55af-593">TaxReportLayout</span><span class="sxs-lookup"><span data-stu-id="d55af-593">TaxReportLayout</span></span>|
|<span data-ttu-id="d55af-594">TradeWorkflowState</span><span class="sxs-lookup"><span data-stu-id="d55af-594">TradeWorkflowState</span></span>|
|<span data-ttu-id="d55af-595">WMSExpeditionStatus</span><span class="sxs-lookup"><span data-stu-id="d55af-595">WMSExpeditionStatus</span></span>|


## <a name="extensible-sql-operations"></a><span data-ttu-id="d55af-596">拡張可能な SQL 操作</span><span class="sxs-lookup"><span data-stu-id="d55af-596">Extensible SQL Operations</span></span>

<span data-ttu-id="d55af-597">これらの SQL 操作は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="d55af-597">These SQL operations have been made extensible in this update.</span></span>

| <span data-ttu-id="d55af-598">工程</span><span class="sxs-lookup"><span data-stu-id="d55af-598">Operation</span></span> |
| --------------- |
|<span data-ttu-id="d55af-599">CustInterestPost.postVoucherPerTransaction</span><span class="sxs-lookup"><span data-stu-id="d55af-599">CustInterestPost.postVoucherPerTransaction</span></span>|
|<span data-ttu-id="d55af-600">InventMov_ProdLine_JournalBom.insertChildBuffer</span><span class="sxs-lookup"><span data-stu-id="d55af-600">InventMov_ProdLine_JournalBom.insertChildBuffer</span></span>|
|<span data-ttu-id="d55af-601">InventUpdate.initInventTransToReceiveList</span><span class="sxs-lookup"><span data-stu-id="d55af-601">InventUpdate.initInventTransToReceiveList</span></span>|
|<span data-ttu-id="d55af-602">ProjAdjustmentUpdate_PostAsync.postAsync</span><span class="sxs-lookup"><span data-stu-id="d55af-602">ProjAdjustmentUpdate_PostAsync.postAsync</span></span>|
|<span data-ttu-id="d55af-603">ProjBudgetManager.createBudgetCostForecast</span><span class="sxs-lookup"><span data-stu-id="d55af-603">ProjBudgetManager.createBudgetCostForecast</span></span>|
|<span data-ttu-id="d55af-604">ProjBudgetManager.createBudgetEmplForecast</span><span class="sxs-lookup"><span data-stu-id="d55af-604">ProjBudgetManager.createBudgetEmplForecast</span></span>|
|<span data-ttu-id="d55af-605">ProjBudgetManager.createBudgetRevenueForecast</span><span class="sxs-lookup"><span data-stu-id="d55af-605">ProjBudgetManager.createBudgetRevenueForecast</span></span>|
|<span data-ttu-id="d55af-606">ProjBudgetManager.createBudgetSalesForecast</span><span class="sxs-lookup"><span data-stu-id="d55af-606">ProjBudgetManager.createBudgetSalesForecast</span></span>|


## <a name="metadata-changes"></a><span data-ttu-id="d55af-607">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="d55af-607">Metadata changes</span></span>

<span data-ttu-id="d55af-608">これらのメタデータの変更は、このアップデートで行われました。</span><span class="sxs-lookup"><span data-stu-id="d55af-608">These metadata changes have been made in this update.</span></span>

| <span data-ttu-id="d55af-609">工程</span><span class="sxs-lookup"><span data-stu-id="d55af-609">Operation</span></span> |
| --------------- |
|<span data-ttu-id="d55af-610">/Data entities/ReqPlannedOrderEntity.Is Public</span><span class="sxs-lookup"><span data-stu-id="d55af-610">/Data entities/ReqPlannedOrderEntity.Is Public</span></span>|
|<span data-ttu-id="d55af-611">/DataTypes/Extended Data Types/AmountQty.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-611">/DataTypes/Extended Data Types/AmountQty.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-612">/DataTypes/Extended Data Types/AssetDepreciationAmountUnitReportingCurrency.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-612">/DataTypes/Extended Data Types/AssetDepreciationAmountUnitReportingCurrency.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-613">/DataTypes/Extended Data Types/BOMProductQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-613">/DataTypes/Extended Data Types/BOMProductQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-614">/DataTypes/Extended Data Types/CostPriceNonMonetary.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-614">/DataTypes/Extended Data Types/CostPriceNonMonetary.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-615">/DataTypes/Extended Data Types/CostQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-615">/DataTypes/Extended Data Types/CostQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-616">/DataTypes/Extended Data Types/MCRRoyaltyValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-616">/DataTypes/Extended Data Types/MCRRoyaltyValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-617">/DataTypes/Extended Data Types/PdsRebateValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-617">/DataTypes/Extended Data Types/PdsRebateValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-618">/DataTypes/Extended Data Types/PriceDiscAmount.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-618">/DataTypes/Extended Data Types/PriceDiscAmount.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-619">/DataTypes/Extended Data Types/PriceQty.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-619">/DataTypes/Extended Data Types/PriceQty.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-620">/DataTypes/Extended Data Types/PriceUnit.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-620">/DataTypes/Extended Data Types/PriceUnit.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-621">/DataTypes/Extended Data Types/PriceUnit.Scale</span><span class="sxs-lookup"><span data-stu-id="d55af-621">/DataTypes/Extended Data Types/PriceUnit.Scale</span></span>|
|<span data-ttu-id="d55af-622">/DataTypes/Extended Data Types/ProductQuantity.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-622">/DataTypes/Extended Data Types/ProductQuantity.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-623">/DataTypes/Extended Data Types/ProductQuantityHourValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-623">/DataTypes/Extended Data Types/ProductQuantityHourValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-624">/DataTypes/Extended Data Types/ProjName.Extends</span><span class="sxs-lookup"><span data-stu-id="d55af-624">/DataTypes/Extended Data Types/ProjName.Extends</span></span>|
|<span data-ttu-id="d55af-625">/DataTypes/Extended Data Types/TAMRebateValue.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-625">/DataTypes/Extended Data Types/TAMRebateValue.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-626">/DataTypes/Extended Data Types/UnitAmountCur.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-626">/DataTypes/Extended Data Types/UnitAmountCur.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-627">/DataTypes/Extended Data Types/UnitAmountMST.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-627">/DataTypes/Extended Data Types/UnitAmountMST.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-628">/DataTypes/Extended Data Types/WeightBase.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="d55af-628">/DataTypes/Extended Data Types/WeightBase.NoOfDecimalsIsExtensible</span></span>|
|<span data-ttu-id="d55af-629">/Tables/LedgerJournalTrans_Project/Relations/LedgerJournalTrans.createNavigationPropertyMethod</span><span class="sxs-lookup"><span data-stu-id="d55af-629">/Tables/LedgerJournalTrans_Project/Relations/LedgerJournalTrans.createNavigationPropertyMethod</span></span>|
|<span data-ttu-id="d55af-630">/Tables/PriceDiscGroup.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="d55af-630">/Tables/PriceDiscGroup.Cache Lookup</span></span>|
|<span data-ttu-id="d55af-631">/Tables/VendInvoiceJour/Fields/DefaultDimension.Visible</span><span class="sxs-lookup"><span data-stu-id="d55af-631">/Tables/VendInvoiceJour/Fields/DefaultDimension.Visible</span></span>|
|<span data-ttu-id="d55af-632">/Tables/VendInvoiceTrans/Fields/DefaultDimension.Visible</span><span class="sxs-lookup"><span data-stu-id="d55af-632">/Tables/VendInvoiceTrans/Fields/DefaultDimension.Visible</span></span>|
|<span data-ttu-id="d55af-633">/Tables/WMSAisle.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="d55af-633">/Tables/WMSAisle.Cache Lookup</span></span>|
|<span data-ttu-id="d55af-634">/Tables/WorkCalendarTable.Create Rec Id Index</span><span class="sxs-lookup"><span data-stu-id="d55af-634">/Tables/WorkCalendarTable.Create Rec Id Index</span></span>|
|<span data-ttu-id="d55af-635">/Tables/WorkTimeLine.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="d55af-635">/Tables/WorkTimeLine.Cache Lookup</span></span>|
|<span data-ttu-id="d55af-636">/Tables/WorkTimeTable.Cache Lookup</span><span class="sxs-lookup"><span data-stu-id="d55af-636">/Tables/WorkTimeTable.Cache Lookup</span></span>|


## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="d55af-637">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="d55af-637">Additional extensibility enhancements</span></span>

<span data-ttu-id="d55af-638">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="d55af-638">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="d55af-639">バグ リクエスト: "CustCollectionLetterTrans -> CollectionLetterNum" 関係プロパティ</span><span class="sxs-lookup"><span data-stu-id="d55af-639">Bug request: "CustCollectionLetterTrans -> CollectionLetterNum" Relation properties</span></span>
- <span data-ttu-id="d55af-640">価格の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="d55af-640">Enable increase of decimal precision through extensiblity for prices</span></span>
- <span data-ttu-id="d55af-641">重量の拡張による小数点以下の精度の増加を有効にする</span><span class="sxs-lookup"><span data-stu-id="d55af-641">Enable increase of decimal precision through extensiblity for weights</span></span>
- <span data-ttu-id="d55af-642">マップ拡張: LogisticsEntityLocationMap</span><span class="sxs-lookup"><span data-stu-id="d55af-642">Map Extension: LogisticsEntityLocationMap</span></span>
- <span data-ttu-id="d55af-643">OMOperatingUnit は、DimAttributeOMDepartment.Value のユーザー フレンドリおよび定義済の値を指定する必要がある</span><span class="sxs-lookup"><span data-stu-id="d55af-643">OMOperatingUnit should provide user friendly and defined value for DimAttributeOMDepartment.Value</span></span>
- <span data-ttu-id="d55af-644">InventPosting が LedgerDimension を検索する方法を再設計</span><span class="sxs-lookup"><span data-stu-id="d55af-644">Redesign how InventPosting finds LedgerDimension</span></span>
- <span data-ttu-id="d55af-645">WhsWorkExecuteDisplayAdjustIn を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="d55af-645">Refactor WhsWorkExecuteDisplayAdjustIn to ProcessGuide framework</span></span>
- <span data-ttu-id="d55af-646">WHSWorkExecuteDisplayChangeWarehouse を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="d55af-646">Refactor WHSWorkExecuteDisplayChangeWarehouse to ProcessGuide framework</span></span>
- <span data-ttu-id="d55af-647">WhsWorkExecuteDisplayInquiryItem を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="d55af-647">Refactor WhsWorkExecuteDisplayInquiryItem to ProcessGuide framework</span></span>
- <span data-ttu-id="d55af-648">WhsWorkExecuteDisplayInquiryLocation を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="d55af-648">Refactor WhsWorkExecuteDisplayInquiryLocation to ProcessGuide framework</span></span>
- <span data-ttu-id="d55af-649">WhsWorkExecuteDisplayInquiryLP を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="d55af-649">Refactor WhsWorkExecuteDisplayInquiryLP to ProcessGuide framework</span></span>
- <span data-ttu-id="d55af-650">whsWorkExecuteDisplayReprintLabel を ProcessGuide フレームワークにリファクター</span><span class="sxs-lookup"><span data-stu-id="d55af-650">Refactor whsWorkExecuteDisplayReprintLabel to ProcessGuide framework</span></span>
- <span data-ttu-id="d55af-651">小売チャネル: サポート BankDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="d55af-651">Retail channel: Support BankDropOperationRequest</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]