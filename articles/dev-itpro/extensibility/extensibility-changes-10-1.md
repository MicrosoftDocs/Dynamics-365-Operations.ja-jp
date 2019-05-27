---
title: Dynamics 365 for Finance and Operations バージョン 10.0.1 の拡張機能の変更
description: これのトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 に実装された拡張機能を一覧します。
author: FrankDahl
manager: AnnBe
ms.date: 05/10/2019
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
ms.search.validFrom: 2019-05-10
ms.dyn365.ops.version: App 10.0
ms.openlocfilehash: 23466970ae2c8fd55c77e77d580173feeac1d11a
ms.sourcegitcommit: 3d1b0e7d0f165fbcbec9c92783e5e936b282d757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2019
ms.locfileid: "1540155"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-1001"></a><span data-ttu-id="0061e-103">Dynamics 365 for Finance and Operations バージョン 10.0.1 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="0061e-103">Extensibility changes in Dynamics 365 for Finance and Operations version 10.0.1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0061e-104">これのトピックでは、 Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 にて実装された拡張機能を記載しています。</span><span class="sxs-lookup"><span data-stu-id="0061e-104">This topic lists the extensibility features that were implemented in Microsoft Dynamics 365 for Finance and Operations version 10.0.1.</span></span> <span data-ttu-id="0061e-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0061e-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="enumerations-made-extensible"></a><span data-ttu-id="0061e-106">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="0061e-106">Enumerations made extensible</span></span>

<span data-ttu-id="0061e-107">今回のアップデートで実装された拡張を以下に記載します。</span><span class="sxs-lookup"><span data-stu-id="0061e-107">The following enumerations have been made extensible in this update:</span></span>

- <span data-ttu-id="0061e-108">ACOCostStatus\_BR</span><span class="sxs-lookup"><span data-stu-id="0061e-108">ACOCostStatus\_BR</span></span>
- <span data-ttu-id="0061e-109">ACOCostType\_BR</span><span class="sxs-lookup"><span data-stu-id="0061e-109">ACOCostType\_BR</span></span>
- <span data-ttu-id="0061e-110">ACOJournalType\_BR</span><span class="sxs-lookup"><span data-stu-id="0061e-110">ACOJournalType\_BR</span></span>
- <span data-ttu-id="0061e-111">BankModuloCheck\_NO</span><span class="sxs-lookup"><span data-stu-id="0061e-111">BankModuloCheck\_NO</span></span>
- <span data-ttu-id="0061e-112">InventTransferOrderType\_BR</span><span class="sxs-lookup"><span data-stu-id="0061e-112">InventTransferOrderType\_BR</span></span>
- <span data-ttu-id="0061e-113">ProdJourType</span><span class="sxs-lookup"><span data-stu-id="0061e-113">ProdJourType</span></span>
- <span data-ttu-id="0061e-114">ProjTransStatus</span><span class="sxs-lookup"><span data-stu-id="0061e-114">ProjTransStatus</span></span>
- <span data-ttu-id="0061e-115">RetailLabelTypeBase</span><span class="sxs-lookup"><span data-stu-id="0061e-115">RetailLabelTypeBase</span></span>
- <span data-ttu-id="0061e-116">RetailLedgerBank</span><span class="sxs-lookup"><span data-stu-id="0061e-116">RetailLedgerBank</span></span>
- <span data-ttu-id="0061e-117">RetailTenderFunction</span><span class="sxs-lookup"><span data-stu-id="0061e-117">RetailTenderFunction</span></span>
- <span data-ttu-id="0061e-118">SalesPurchTrntype\_BR</span><span class="sxs-lookup"><span data-stu-id="0061e-118">SalesPurchTrntype\_BR</span></span>
- <span data-ttu-id="0061e-119">SMAGetPriceFrom</span><span class="sxs-lookup"><span data-stu-id="0061e-119">SMAGetPriceFrom</span></span>
- <span data-ttu-id="0061e-120">SMASubscriptionIndexChange</span><span class="sxs-lookup"><span data-stu-id="0061e-120">SMASubscriptionIndexChange</span></span>

## <a name="sql-operations-made-extensible"></a><span data-ttu-id="0061e-121">拡張可能になった SQL 操作</span><span class="sxs-lookup"><span data-stu-id="0061e-121">SQL operations made extensible</span></span>

<span data-ttu-id="0061e-122">今回のアップデートでは、以下のSQL操作が拡張されました。</span><span class="sxs-lookup"><span data-stu-id="0061e-122">The following SQL operations have been made extensible in this update:</span></span>

- <span data-ttu-id="0061e-123">InventSumDelta.findInventSumDeltaInventSumFieldsAll.</span><span class="sxs-lookup"><span data-stu-id="0061e-123">InventSumDelta.findInventSumDeltaInventSumFieldsAll.</span></span>
- <span data-ttu-id="0061e-124">LedgerFiscalJournal は、QueryObject を使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="0061e-124">LedgerFiscalJournal was changed so that it uses QueryObject.</span></span>
- <span data-ttu-id="0061e-125">TaxTransDP.</span><span class="sxs-lookup"><span data-stu-id="0061e-125">TaxTransDP.</span></span>

## <a name="metadata-changes"></a><span data-ttu-id="0061e-126">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="0061e-126">Metadata changes</span></span>

<span data-ttu-id="0061e-127">今回のアップデートで以下のメタデータが更新されました。</span><span class="sxs-lookup"><span data-stu-id="0061e-127">The following metadata changes have been made in this update:</span></span>

- <span data-ttu-id="0061e-128">Data Entities/WMSItemArrivalJournalLineEntity.IsPublic, PublicCollectionName, PublicEntityName</span><span class="sxs-lookup"><span data-stu-id="0061e-128">Data Entities/WMSItemArrivalJournalLineEntity.IsPublic, PublicCollectionName, PublicEntityName.</span></span>
- <span data-ttu-id="0061e-129">DataEntities/LedgerJournalNameEntity/Fields/voucherSeriesCode 作成時に編集することが可能となりました。</span><span class="sxs-lookup"><span data-stu-id="0061e-129">DataEntities/LedgerJournalNameEntity/Fields/voucherSeriesCode.Allow Edit, Allow Edit on Create.</span></span>
- <span data-ttu-id="0061e-130">DataEntities/LedgerJournalNameEntity/Fields/VoucherSeriesCompanyId.AllowEdit.</span><span class="sxs-lookup"><span data-stu-id="0061e-130">DataEntities/LedgerJournalNameEntity/Fields/VoucherSeriesCompanyId.AllowEdit.</span></span>
- <span data-ttu-id="0061e-131">Enums\\SalesStatus::Backorder, Delivered.Label.</span><span class="sxs-lookup"><span data-stu-id="0061e-131">Enums\\SalesStatus::Backorder, Delivered.Label.</span></span>
- <span data-ttu-id="0061e-132">Types/WeightBase.Scale におけるデータの拡張。</span><span class="sxs-lookup"><span data-stu-id="0061e-132">Extended Data Types/WeightBase.Scale.</span></span>
- <span data-ttu-id="0061e-133">InventTransferOrders は、フォームコントロールグループをグリッドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="0061e-133">InventTransferOrders added a form control group in the grid.</span></span>

## <a name="refactored-methods"></a><span data-ttu-id="0061e-134">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="0061e-134">Refactored methods</span></span>

<span data-ttu-id="0061e-135">拡張性をサポートするために、以下のメソッドがリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="0061e-135">The following methods have been refactored to support extensibility:</span></span>

- <span data-ttu-id="0061e-136">AssetProposalDepreciation.run</span><span class="sxs-lookup"><span data-stu-id="0061e-136">AssetProposalDepreciation.run</span></span>
- <span data-ttu-id="0061e-137">BankStatementValidate.validateDate</span><span class="sxs-lookup"><span data-stu-id="0061e-137">BankStatementValidate.validateDate</span></span>
- <span data-ttu-id="0061e-138">Class\\BankDocumentBankAccountTrans.loadSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="0061e-138">Class\\BankDocumentBankAccountTrans.loadSourceBuffer</span></span>
- <span data-ttu-id="0061e-139">Class\\BankReconMatchingRuleAutoProcessor.doProcessMatchRule</span><span class="sxs-lookup"><span data-stu-id="0061e-139">Class\\BankReconMatchingRuleAutoProcessor.doProcessMatchRule</span></span>
- <span data-ttu-id="0061e-140">Class\\ProjJournalTransMapForm.initFromProjTable</span><span class="sxs-lookup"><span data-stu-id="0061e-140">Class\\ProjJournalTransMapForm.initFromProjTable</span></span>
- <span data-ttu-id="0061e-141">Class\\RetailEodStatementPaymentJournal.createPaymentJournalLine</span><span class="sxs-lookup"><span data-stu-id="0061e-141">Class\\RetailEodStatementPaymentJournal.createPaymentJournalLine</span></span>
- <span data-ttu-id="0061e-142">Class\\RetailKitAssemblyOrder.CreateOrUpdateBOMJournal</span><span class="sxs-lookup"><span data-stu-id="0061e-142">Class\\RetailKitAssemblyOrder.CreateOrUpdateBOMJournal</span></span>
- <span data-ttu-id="0061e-143">Class\\RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span><span class="sxs-lookup"><span data-stu-id="0061e-143">Class\\RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span></span>
- <span data-ttu-id="0061e-144">Class\\SalesInvoiceController.initReportName\_IN</span><span class="sxs-lookup"><span data-stu-id="0061e-144">Class\\SalesInvoiceController.initReportName\_IN</span></span>
- <span data-ttu-id="0061e-145">Class\\SalesInvoiceJournalPost.endUpdate</span><span class="sxs-lookup"><span data-stu-id="0061e-145">Class\\SalesInvoiceJournalPost.endUpdate</span></span>
- <span data-ttu-id="0061e-146">Class\\WrkCtrScheduler.loadRoute</span><span class="sxs-lookup"><span data-stu-id="0061e-146">Class\\WrkCtrScheduler.loadRoute</span></span>
- <span data-ttu-id="0061e-147">CreditCard.mcrInitFromCustPaymTable</span><span class="sxs-lookup"><span data-stu-id="0061e-147">CreditCard.mcrInitFromCustPaymTable</span></span>
- <span data-ttu-id="0061e-148">CreditcardProcess.mcrDoCapture</span><span class="sxs-lookup"><span data-stu-id="0061e-148">CreditcardProcess.mcrDoCapture</span></span>
- <span data-ttu-id="0061e-149">CreditCardProcess.mcrDoRefund</span><span class="sxs-lookup"><span data-stu-id="0061e-149">CreditCardProcess.mcrDoRefund</span></span>
- <span data-ttu-id="0061e-150">CreditCardProviderProcess.Submit</span><span class="sxs-lookup"><span data-stu-id="0061e-150">CreditCardProviderProcess.Submit</span></span>
- <span data-ttu-id="0061e-151">CustCollectionLetterCreate.skipCustomer</span><span class="sxs-lookup"><span data-stu-id="0061e-151">CustCollectionLetterCreate.skipCustomer</span></span>
- <span data-ttu-id="0061e-152">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="0061e-152">CustVendCheque.output</span></span>
- <span data-ttu-id="0061e-153">CustVendSumForPaym.run</span><span class="sxs-lookup"><span data-stu-id="0061e-153">CustVendSumForPaym.run</span></span>
- <span data-ttu-id="0061e-154">EFDOCDanfe\_BR.additionalInformationPageBreak</span><span class="sxs-lookup"><span data-stu-id="0061e-154">EFDOCDanfe\_BR.additionalInformationPageBreak</span></span>
- <span data-ttu-id="0061e-155">EfDocDANFEDP\_BR.additionalInformationBox</span><span class="sxs-lookup"><span data-stu-id="0061e-155">EfDocDANFEDP\_BR.additionalInformationBox</span></span>
- <span data-ttu-id="0061e-156">ERDocuManagement.insertFile</span><span class="sxs-lookup"><span data-stu-id="0061e-156">ERDocuManagement.insertFile</span></span>
- <span data-ttu-id="0061e-157">ERFileDestinationAttachment.saveFile</span><span class="sxs-lookup"><span data-stu-id="0061e-157">ERFileDestinationAttachment.saveFile</span></span>
- <span data-ttu-id="0061e-158">ERFileDestinationBrowser.saveFile</span><span class="sxs-lookup"><span data-stu-id="0061e-158">ERFileDestinationBrowser.saveFile</span></span>
- <span data-ttu-id="0061e-159">Form\\BankReconciliationWorksheet.Init</span><span class="sxs-lookup"><span data-stu-id="0061e-159">Form\\BankReconciliationWorksheet.Init</span></span>
- <span data-ttu-id="0061e-160">FreeTextInvoiceController.initReportName\_IN</span><span class="sxs-lookup"><span data-stu-id="0061e-160">FreeTextInvoiceController.initReportName\_IN</span></span>
- <span data-ttu-id="0061e-161">HcmWorkerTransition.createHcmWorker</span><span class="sxs-lookup"><span data-stu-id="0061e-161">HcmWorkerTransition.createHcmWorker</span></span>
- <span data-ttu-id="0061e-162">InventCostClosingCancel\_Init.createTasks</span><span class="sxs-lookup"><span data-stu-id="0061e-162">InventCostClosingCancel\_Init.createTasks</span></span>
- <span data-ttu-id="0061e-163">InventDimCtrl\_Frm\_OnHand.initFromCaller</span><span class="sxs-lookup"><span data-stu-id="0061e-163">InventDimCtrl\_Frm\_OnHand.initFromCaller</span></span>
- <span data-ttu-id="0061e-164">InventMov\_Jour\_BOM.journalPostTrans</span><span class="sxs-lookup"><span data-stu-id="0061e-164">InventMov\_Jour\_BOM.journalPostTrans</span></span>
- <span data-ttu-id="0061e-165">InventProcessGuideDisplayLicensePlateDetailsPageBuilder.generateItemInfoForLicensePlate</span><span class="sxs-lookup"><span data-stu-id="0061e-165">InventProcessGuideDisplayLicensePlateDetailsPageBuilder.generateItemInfoForLicensePlate</span></span>
- <span data-ttu-id="0061e-166">InventProcessGuideDisplayLocationDetailsPageBuilder.generateItemInfoForLocation</span><span class="sxs-lookup"><span data-stu-id="0061e-166">InventProcessGuideDisplayLocationDetailsPageBuilder.generateItemInfoForLocation</span></span>
- <span data-ttu-id="0061e-167">InventStockCardDP.createInventStockCardTmpLineDetail</span><span class="sxs-lookup"><span data-stu-id="0061e-167">InventStockCardDP.createInventStockCardTmpLineDetail</span></span>
- <span data-ttu-id="0061e-168">InventTable.checkProjCategoryId</span><span class="sxs-lookup"><span data-stu-id="0061e-168">InventTable.checkProjCategoryId</span></span>
- <span data-ttu-id="0061e-169">InventUpd\_WHSReservation.updateReserveMore</span><span class="sxs-lookup"><span data-stu-id="0061e-169">InventUpd\_WHSReservation.updateReserveMore</span></span>
- <span data-ttu-id="0061e-170">JmgCalcApproveWeekView.initializeData</span><span class="sxs-lookup"><span data-stu-id="0061e-170">JmgCalcApproveWeekView.initializeData</span></span>
- <span data-ttu-id="0061e-171">LedgerConsolidate.Run and getSelectedDimensionAttributes</span><span class="sxs-lookup"><span data-stu-id="0061e-171">LedgerConsolidate.Run and getSelectedDimensionAttributes</span></span>
- <span data-ttu-id="0061e-172">LedgerFiscalJournalDP\_IT.addStarsToTmpTable</span><span class="sxs-lookup"><span data-stu-id="0061e-172">LedgerFiscalJournalDP\_IT.addStarsToTmpTable</span></span>
- <span data-ttu-id="0061e-173">LedgerFiscalJournalDP\_IT.insertLedgerFiscalJournalTmp\_IT</span><span class="sxs-lookup"><span data-stu-id="0061e-173">LedgerFiscalJournalDP\_IT.insertLedgerFiscalJournalTmp\_IT</span></span>
- <span data-ttu-id="0061e-174">LedgerFiscalJournalDP\_IT.insertLedgerFiscalJournalTmp\_IT</span><span class="sxs-lookup"><span data-stu-id="0061e-174">LedgerFiscalJournalDP\_IT.insertLedgerFiscalJournalTmp\_IT</span></span>
- <span data-ttu-id="0061e-175">LedgerFiscalJournalDP\_IT.processReport</span><span class="sxs-lookup"><span data-stu-id="0061e-175">LedgerFiscalJournalDP\_IT.processReport</span></span>
- <span data-ttu-id="0061e-176">LedgerJournalTrans.checkAllowEditWhenCheckPrinted</span><span class="sxs-lookup"><span data-stu-id="0061e-176">LedgerJournalTrans.checkAllowEditWhenCheckPrinted</span></span>
- <span data-ttu-id="0061e-177">LedgerJournalTransUpdateVend.pdateNow</span><span class="sxs-lookup"><span data-stu-id="0061e-177">LedgerJournalTransUpdateVend.pdateNow</span></span>
- <span data-ttu-id="0061e-178">LedgerVoucherTransList.First</span><span class="sxs-lookup"><span data-stu-id="0061e-178">LedgerVoucherTransList.First</span></span>
- <span data-ttu-id="0061e-179">LedgerVoucherTransList.next</span><span class="sxs-lookup"><span data-stu-id="0061e-179">LedgerVoucherTransList.next</span></span>
- <span data-ttu-id="0061e-180">MCRFullTextIndexField.tableIdFromEnum</span><span class="sxs-lookup"><span data-stu-id="0061e-180">MCRFullTextIndexField.tableIdFromEnum</span></span>
- <span data-ttu-id="0061e-181">MCRFullTextIndexField.viewFromTable</span><span class="sxs-lookup"><span data-stu-id="0061e-181">MCRFullTextIndexField.viewFromTable</span></span>
- <span data-ttu-id="0061e-182">MCRInventSearch.searchProduct</span><span class="sxs-lookup"><span data-stu-id="0061e-182">MCRInventSearch.searchProduct</span></span>
- <span data-ttu-id="0061e-183">McrPriceHistoryLine\_Purch.initAndInsertRebate</span><span class="sxs-lookup"><span data-stu-id="0061e-183">McrPriceHistoryLine\_Purch.initAndInsertRebate</span></span>
- <span data-ttu-id="0061e-184">PartyProvider.operatingUnitTypeToName</span><span class="sxs-lookup"><span data-stu-id="0061e-184">PartyProvider.operatingUnitTypeToName</span></span>
- <span data-ttu-id="0061e-185">PdsRebateAgreementValidate.construct</span><span class="sxs-lookup"><span data-stu-id="0061e-185">PdsRebateAgreementValidate.construct</span></span>
- <span data-ttu-id="0061e-186">POS\_IssueLoyaltyCardView.NA</span><span class="sxs-lookup"><span data-stu-id="0061e-186">POS\_IssueLoyaltyCardView.NA</span></span>
- <span data-ttu-id="0061e-187">PriceDiscAdmCheckPostPriceDiscTableUpdater.formattedQueryValue</span><span class="sxs-lookup"><span data-stu-id="0061e-187">PriceDiscAdmCheckPostPriceDiscTableUpdater.formattedQueryValue</span></span>
- <span data-ttu-id="0061e-188">PriceDiscAdmTrans.checkItemRelation</span><span class="sxs-lookup"><span data-stu-id="0061e-188">PriceDiscAdmTrans.checkItemRelation</span></span>
- <span data-ttu-id="0061e-189">ProjBudgetManager.deleteProjBudgetLinesWhenZeroAmount</span><span class="sxs-lookup"><span data-stu-id="0061e-189">ProjBudgetManager.deleteProjBudgetLinesWhenZeroAmount</span></span>
- <span data-ttu-id="0061e-190">ProjBudgetManager.updateProjBudgetLinesWithAmt</span><span class="sxs-lookup"><span data-stu-id="0061e-190">ProjBudgetManager.updateProjBudgetLinesWithAmt</span></span>
- <span data-ttu-id="0061e-191">ProjHourCostPrice.psaFindCostPrice</span><span class="sxs-lookup"><span data-stu-id="0061e-191">ProjHourCostPrice.psaFindCostPrice</span></span>
- <span data-ttu-id="0061e-192">ProjInvoiceProposalListPageInteraction.initializeQuery</span><span class="sxs-lookup"><span data-stu-id="0061e-192">ProjInvoiceProposalListPageInteraction.initializeQuery</span></span>
- <span data-ttu-id="0061e-193">ProjPostEmplProposalSale.new</span><span class="sxs-lookup"><span data-stu-id="0061e-193">ProjPostEmplProposalSale.new</span></span>
- <span data-ttu-id="0061e-194">ProjPostRevenueProposalSale.new</span><span class="sxs-lookup"><span data-stu-id="0061e-194">ProjPostRevenueProposalSale.new</span></span>
- <span data-ttu-id="0061e-195">ProjTable.initProjectFromCustomerAndInvoice</span><span class="sxs-lookup"><span data-stu-id="0061e-195">ProjTable.initProjectFromCustomerAndInvoice</span></span>
- <span data-ttu-id="0061e-196">ProjTransferPrice.findByContractResourceCategory, findTransferPrice, find</span><span class="sxs-lookup"><span data-stu-id="0061e-196">ProjTransferPrice.findByContractResourceCategory, findTransferPrice, find</span></span>
- <span data-ttu-id="0061e-197">ProjValElementServer.addProjToResource</span><span class="sxs-lookup"><span data-stu-id="0061e-197">ProjValElementServer.addProjToResource</span></span>
- <span data-ttu-id="0061e-198">ProjValElementServer.deleteProjFromResource</span><span class="sxs-lookup"><span data-stu-id="0061e-198">ProjValElementServer.deleteProjFromResource</span></span>
- <span data-ttu-id="0061e-199">PurchPackingSlipJournalPost.postMarkupOnTrans</span><span class="sxs-lookup"><span data-stu-id="0061e-199">PurchPackingSlipJournalPost.postMarkupOnTrans</span></span>
- <span data-ttu-id="0061e-200">PurchReqLine.setProjSalesPrice</span><span class="sxs-lookup"><span data-stu-id="0061e-200">PurchReqLine.setProjSalesPrice</span></span>
- <span data-ttu-id="0061e-201">PurchRFQSendJournalCreate.createOrUpdateRFQLine</span><span class="sxs-lookup"><span data-stu-id="0061e-201">PurchRFQSendJournalCreate.createOrUpdateRFQLine</span></span>
- <span data-ttu-id="0061e-202">ReqCalc.covCalcDim</span><span class="sxs-lookup"><span data-stu-id="0061e-202">ReqCalc.covCalcDim</span></span>
- <span data-ttu-id="0061e-203">ReqCalc.covCalcDim</span><span class="sxs-lookup"><span data-stu-id="0061e-203">ReqCalc.covCalcDim</span></span>
- <span data-ttu-id="0061e-204">ReqCalc.covCalcDim</span><span class="sxs-lookup"><span data-stu-id="0061e-204">ReqCalc.covCalcDim</span></span>
- <span data-ttu-id="0061e-205">RequisitionPurchaseOrderGeneration.create</span><span class="sxs-lookup"><span data-stu-id="0061e-205">RequisitionPurchaseOrderGeneration.create</span></span>
- <span data-ttu-id="0061e-206">RequisitionPurchaseOrderGeneration.create</span><span class="sxs-lookup"><span data-stu-id="0061e-206">RequisitionPurchaseOrderGeneration.create</span></span>
- <span data-ttu-id="0061e-207">Commerce runtime (CRT) のRetail extension point は ValidateCartLineQuantityAndPriceSymbol メソッドを無効にします。</span><span class="sxs-lookup"><span data-stu-id="0061e-207">Retail extension point in the Commerce runtime (CRT) to override the ValidateCartLineQuantityAndPriceSymbol method</span></span>
- <span data-ttu-id="0061e-208">RetailCatalogProductAttributeFormHelper.addProductAttributeControls</span><span class="sxs-lookup"><span data-stu-id="0061e-208">RetailCatalogProductAttributeFormHelper.addProductAttributeControls</span></span>
- <span data-ttu-id="0061e-209">RetailCreateSpecificLabel.makeLabel</span><span class="sxs-lookup"><span data-stu-id="0061e-209">RetailCreateSpecificLabel.makeLabel</span></span>
- <span data-ttu-id="0061e-210">RetailEodStatementCustomerOrderInvoiceController.run</span><span class="sxs-lookup"><span data-stu-id="0061e-210">RetailEodStatementCustomerOrderInvoiceController.run</span></span>
- <span data-ttu-id="0061e-211">RetailEodStatementPaymentJournal.ledgerBank2LedgerJournalACType</span><span class="sxs-lookup"><span data-stu-id="0061e-211">RetailEodStatementPaymentJournal.ledgerBank2LedgerJournalACType</span></span>
- <span data-ttu-id="0061e-212">RetailEodStatementPaymentJournal.postPaymentJournalForOthers, postPaymentJournalForSales, createTenderedPaymentLines, createPaymentJournalLine</span><span class="sxs-lookup"><span data-stu-id="0061e-212">RetailEodStatementPaymentJournal.postPaymentJournalForOthers, postPaymentJournalForSales, createTenderedPaymentLines, createPaymentJournalLine</span></span>
- <span data-ttu-id="0061e-213">RetailEodTransactionTransformer.ReadTransactionHeader</span><span class="sxs-lookup"><span data-stu-id="0061e-213">RetailEodTransactionTransformer.ReadTransactionHeader</span></span>
- <span data-ttu-id="0061e-214">RetailEodTransactionTransformer.setExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="0061e-214">RetailEodTransactionTransformer.setExtensionProperty</span></span>
- <span data-ttu-id="0061e-215">RetailEventNotificationAction.packingSlipCompletion</span><span class="sxs-lookup"><span data-stu-id="0061e-215">RetailEventNotificationAction.packingSlipCompletion</span></span>
- <span data-ttu-id="0061e-216">RetailMediaAssociationHelper.associateProduct</span><span class="sxs-lookup"><span data-stu-id="0061e-216">RetailMediaAssociationHelper.associateProduct</span></span>
- <span data-ttu-id="0061e-217">RetailProductPropertyManager.validateWriteOnInventModelGroupItem</span><span class="sxs-lookup"><span data-stu-id="0061e-217">RetailProductPropertyManager.validateWriteOnInventModelGroupItem</span></span>
- <span data-ttu-id="0061e-218">RetailSMBSeedGenerator.AccountReceivable</span><span class="sxs-lookup"><span data-stu-id="0061e-218">RetailSMBSeedGenerator.AccountReceivable</span></span>
- <span data-ttu-id="0061e-219">RetailStatementPost.createPaymentLedgerTrans</span><span class="sxs-lookup"><span data-stu-id="0061e-219">RetailStatementPost.createPaymentLedgerTrans</span></span>
- <span data-ttu-id="0061e-220">RetailTransactionSalesTransMark.MarkTransactions</span><span class="sxs-lookup"><span data-stu-id="0061e-220">RetailTransactionSalesTransMark.MarkTransactions</span></span>
- <span data-ttu-id="0061e-221">RetailTransactionServiceOrder.settleCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="0061e-221">RetailTransactionServiceOrder.settleCustomerOrder</span></span>
- <span data-ttu-id="0061e-222">RetailTransactionServiceOrders.cancelCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="0061e-222">RetailTransactionServiceOrders.cancelCustomerOrder</span></span>
- <span data-ttu-id="0061e-223">RetailTransactionServiceOrders.createCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="0061e-223">RetailTransactionServiceOrders.createCustomerOrder</span></span>
- <span data-ttu-id="0061e-224">RetailTransactionServiceOrders.createLedgerJournalForStore</span><span class="sxs-lookup"><span data-stu-id="0061e-224">RetailTransactionServiceOrders.createLedgerJournalForStore</span></span>
- <span data-ttu-id="0061e-225">RetailTransactionServiceOrders.createOrUpdateRetailOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0061e-225">RetailTransactionServiceOrders.createOrUpdateRetailOrderHeader</span></span>
- <span data-ttu-id="0061e-226">RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span><span class="sxs-lookup"><span data-stu-id="0061e-226">RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span></span>
- <span data-ttu-id="0061e-227">RetailTransactionServiceTransactions.fillPaymentTransDetails</span><span class="sxs-lookup"><span data-stu-id="0061e-227">RetailTransactionServiceTransactions.fillPaymentTransDetails</span></span>
- <span data-ttu-id="0061e-228">RetailTransactionServiceTransactions.fillRetailTransactionDetails</span><span class="sxs-lookup"><span data-stu-id="0061e-228">RetailTransactionServiceTransactions.fillRetailTransactionDetails</span></span>
- <span data-ttu-id="0061e-229">RetailTransactionServiceTransactions.fillSalesTransDetails</span><span class="sxs-lookup"><span data-stu-id="0061e-229">RetailTransactionServiceTransactions.fillSalesTransDetails</span></span>
- <span data-ttu-id="0061e-230">RetailTransactionServiceTransactions.getJournalListQuery</span><span class="sxs-lookup"><span data-stu-id="0061e-230">RetailTransactionServiceTransactions.getJournalListQuery</span></span>
- <span data-ttu-id="0061e-231">SalesCreateOrder.updateDeliveryAddress</span><span class="sxs-lookup"><span data-stu-id="0061e-231">SalesCreateOrder.updateDeliveryAddress</span></span>
- <span data-ttu-id="0061e-232">SubledgerJournalizer.loadAccountingdistributionTmp</span><span class="sxs-lookup"><span data-stu-id="0061e-232">SubledgerJournalizer.loadAccountingdistributionTmp</span></span>
- <span data-ttu-id="0061e-233">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span><span class="sxs-lookup"><span data-stu-id="0061e-233">SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding</span></span>
- <span data-ttu-id="0061e-234">SubledgerJournalizer.recordSubledgerJournalAccountEntries</span><span class="sxs-lookup"><span data-stu-id="0061e-234">SubledgerJournalizer.recordSubledgerJournalAccountEntries</span></span>
- <span data-ttu-id="0061e-235">Table\\MCRContinuityScheduleLine.UpdateOtherLines</span><span class="sxs-lookup"><span data-stu-id="0061e-235">Table\\MCRContinuityScheduleLine.UpdateOtherLines</span></span>
- <span data-ttu-id="0061e-236">Tax1099SummaryHelper.populateTaxSummaryFromVendSettlementTax</span><span class="sxs-lookup"><span data-stu-id="0061e-236">Tax1099SummaryHelper.populateTaxSummaryFromVendSettlementTax</span></span>
- <span data-ttu-id="0061e-237">TrvCreditCardTransactionEntity.validateWrite</span><span class="sxs-lookup"><span data-stu-id="0061e-237">TrvCreditCardTransactionEntity.validateWrite</span></span>
- <span data-ttu-id="0061e-238">TrvExpenses.initializePersonalAmount</span><span class="sxs-lookup"><span data-stu-id="0061e-238">TrvExpenses.initializePersonalAmount</span></span>
- <span data-ttu-id="0061e-239">TrvExpenses.updateFormVisibilityOnCategoryChange</span><span class="sxs-lookup"><span data-stu-id="0061e-239">TrvExpenses.updateFormVisibilityOnCategoryChange</span></span>
- <span data-ttu-id="0061e-240">TrvExpenses.updateItemizationControls</span><span class="sxs-lookup"><span data-stu-id="0061e-240">TrvExpenses.updateItemizationControls</span></span>
- <span data-ttu-id="0061e-241">TrvExpTrans.copyValueToChildLines</span><span class="sxs-lookup"><span data-stu-id="0061e-241">TrvExpTrans.copyValueToChildLines</span></span>
- <span data-ttu-id="0061e-242">TrvExpTrans.defaultTaxGroupFromWorker</span><span class="sxs-lookup"><span data-stu-id="0061e-242">TrvExpTrans.defaultTaxGroupFromWorker</span></span>
- <span data-ttu-id="0061e-243">TrvExpTrans.modifiedField</span><span class="sxs-lookup"><span data-stu-id="0061e-243">TrvExpTrans.modifiedField</span></span>
- <span data-ttu-id="0061e-244">TsTimesheetSignOffDP.insertTmpTSTimesheetSignOff</span><span class="sxs-lookup"><span data-stu-id="0061e-244">TsTimesheetSignOffDP.insertTmpTSTimesheetSignOff</span></span>
- <span data-ttu-id="0061e-245">WHSBillOfLadingDataUtil.populateCarrierInformation</span><span class="sxs-lookup"><span data-stu-id="0061e-245">WHSBillOfLadingDataUtil.populateCarrierInformation</span></span>
- <span data-ttu-id="0061e-246">WHSBillOfLadingDataUtil.populateCustomerOrderInfo</span><span class="sxs-lookup"><span data-stu-id="0061e-246">WHSBillOfLadingDataUtil.populateCustomerOrderInfo</span></span>
- <span data-ttu-id="0061e-247">WHSLoadPlanningWorkbenchServerForm.addLoadLinesToLoad</span><span class="sxs-lookup"><span data-stu-id="0061e-247">WHSLoadPlanningWorkbenchServerForm.addLoadLinesToLoad</span></span>
- <span data-ttu-id="0061e-248">WHSLocationDirective.getValidSellableDaysQty</span><span class="sxs-lookup"><span data-stu-id="0061e-248">WHSLocationDirective.getValidSellableDaysQty</span></span>
- <span data-ttu-id="0061e-249">WHSMobileAppAttachedImageDetails.getImageTypeFromSymbol</span><span class="sxs-lookup"><span data-stu-id="0061e-249">WHSMobileAppAttachedImageDetails.getImageTypeFromSymbol</span></span>
- <span data-ttu-id="0061e-250">WhsPostPackingSlip.updatePurchaseLoadLines</span><span class="sxs-lookup"><span data-stu-id="0061e-250">WhsPostPackingSlip.updatePurchaseLoadLines</span></span>
- <span data-ttu-id="0061e-251">WhsPostPackingSlip.updatePurchParmLineQuantityData</span><span class="sxs-lookup"><span data-stu-id="0061e-251">WhsPostPackingSlip.updatePurchParmLineQuantityData</span></span>
- <span data-ttu-id="0061e-252">WhsWarehouseRelease.main</span><span class="sxs-lookup"><span data-stu-id="0061e-252">WhsWarehouseRelease.main</span></span>
- <span data-ttu-id="0061e-253">WhsWorkManualComplete.executeWorkLines</span><span class="sxs-lookup"><span data-stu-id="0061e-253">WhsWorkManualComplete.executeWorkLines</span></span>
- <span data-ttu-id="0061e-254">WhsWorkManualComplete.performValidation</span><span class="sxs-lookup"><span data-stu-id="0061e-254">WhsWorkManualComplete.performValidation</span></span>
- <span data-ttu-id="0061e-255">WorkTimeCheckClassWorkCalendarDateLineTableWorkTimeLineTable class, validateWrite()</span><span class="sxs-lookup"><span data-stu-id="0061e-255">WorkTimeCheckClassWorkCalendarDateLineTableWorkTimeLineTable class, validateWrite()</span></span>
- <span data-ttu-id="0061e-256">WorkTimeLine.createWorkTimeCheck</span><span class="sxs-lookup"><span data-stu-id="0061e-256">WorkTimeLine.createWorkTimeCheck</span></span>

## <a name="other-extensibility-enhancements"></a><span data-ttu-id="0061e-257">その他の拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="0061e-257">Other extensibility enhancements</span></span>

- <span data-ttu-id="0061e-258">**小売チャンネル:** OrderFulfillmentViewにおける機能拡張、 [すべて選択] と [すべてクリア] が利用可能となります。</span><span class="sxs-lookup"><span data-stu-id="0061e-258">**Retail channel:** Allow for extensions to support Select all and Clear all in OrderFulfillmentView.</span></span>
- <span data-ttu-id="0061e-259">**小売チャンネル** : トランザクションアプリケーションプログラミングインターフェイス (API) から行IDごとに、戻り行をカートに表示します。</span><span class="sxs-lookup"><span data-stu-id="0061e-259">**Retail channel:** Expose Add return line to cart from the transaction application programming interface (API) by line ID.</span></span>
- <span data-ttu-id="0061e-260">**小売チャンネル** : OrderFulfillmentViewにてラインアイテムの場所を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0061e-260">**Retail channel:** Line item locations can be viewed in OrderFulfillmentView.</span></span>
- <span data-ttu-id="0061e-261">**小売チャンネル:** OrderFulfillmentView に ICustomListColumn が追加され、詳細情報を参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0061e-261">**Retail channel:** OrderFulfillmentView adds ICustomListColumn to allow for more information.</span></span>
- <span data-ttu-id="0061e-262">Retail ステートメントのポスティングメソッドは、RetailTransactionAggregationFieldListテーブルを使用して、別の集計ビューを追加します。</span><span class="sxs-lookup"><span data-stu-id="0061e-262">Retail statement posting method adds another aggregation view by using the new RetailTransactionAggregationFieldList table that adds additional fields.</span></span>
