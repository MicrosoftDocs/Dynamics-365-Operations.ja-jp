---
title: Dynamics 365 for Finance and Operations バージョン 8.1.2 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations バージョン 8.1.2 で実装された拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: App 8.1.2
ms.openlocfilehash: 6550f8858a2973256d75679b4bd7a71887ca12a0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409335"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-812"></a><span data-ttu-id="ce8e9-103">Dynamics 365 for Finance and Operations バージョン 8.1.2 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="ce8e9-103">Extensibility changes in Dynamics 365 for Finance and Operations version 8.1.2</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce8e9-104">これは、Dynamics 365 for Finance and Operations バージョン 8.1.2 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations version 8.1.2.</span></span> <span data-ttu-id="ce8e9-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="enumerations-made-extensible"></a><span data-ttu-id="ce8e9-106">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="ce8e9-106">Enumerations made extensible</span></span>

<span data-ttu-id="ce8e9-107">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-107">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="ce8e9-108">列挙型</span><span class="sxs-lookup"><span data-stu-id="ce8e9-108">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="ce8e9-109">DimensionHierarchyType</span><span class="sxs-lookup"><span data-stu-id="ce8e9-109">DimensionHierarchyType</span></span>|
|<span data-ttu-id="ce8e9-110">DirPartyType</span><span class="sxs-lookup"><span data-stu-id="ce8e9-110">DirPartyType</span></span>|
|<span data-ttu-id="ce8e9-111">DirPersonMaritalStatus</span><span class="sxs-lookup"><span data-stu-id="ce8e9-111">DirPersonMaritalStatus</span></span>|
|<span data-ttu-id="ce8e9-112">PrintPostCancel</span><span class="sxs-lookup"><span data-stu-id="ce8e9-112">PrintPostCancel</span></span>|
|<span data-ttu-id="ce8e9-113">INSAffiliate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-113">INSAffiliate</span></span>|
|<span data-ttu-id="ce8e9-114">LedgerJournalLinesDisplayOption</span><span class="sxs-lookup"><span data-stu-id="ce8e9-114">LedgerJournalLinesDisplayOption</span></span>|
|<span data-ttu-id="ce8e9-115">LedgerTransPerJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-115">LedgerTransPerJournal</span></span>|
|<span data-ttu-id="ce8e9-116">ProjDortValue</span><span class="sxs-lookup"><span data-stu-id="ce8e9-116">ProjDortValue</span></span>|
|<span data-ttu-id="ce8e9-117">ProjPaymentStatus</span><span class="sxs-lookup"><span data-stu-id="ce8e9-117">ProjPaymentStatus</span></span>|
|<span data-ttu-id="ce8e9-118">RequisitionReleaseType</span><span class="sxs-lookup"><span data-stu-id="ce8e9-118">RequisitionReleaseType</span></span>|
|<span data-ttu-id="ce8e9-119">RetailPOSSeedDataType</span><span class="sxs-lookup"><span data-stu-id="ce8e9-119">RetailPOSSeedDataType</span></span>|
|<span data-ttu-id="ce8e9-120">SysDimension</span><span class="sxs-lookup"><span data-stu-id="ce8e9-120">SysDimension</span></span>|
|<span data-ttu-id="ce8e9-121">TrvExpType</span><span class="sxs-lookup"><span data-stu-id="ce8e9-121">TrvExpType</span></span>|
|<span data-ttu-id="ce8e9-122">TSTimesheetEntryGridView</span><span class="sxs-lookup"><span data-stu-id="ce8e9-122">TSTimesheetEntryGridView</span></span>|
|<span data-ttu-id="ce8e9-123">VendProspectiveVendorRegistrationWizardTab</span><span class="sxs-lookup"><span data-stu-id="ce8e9-123">VendProspectiveVendorRegistrationWizardTab</span></span>

## <a name="metadata-changes"></a><span data-ttu-id="ce8e9-124">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="ce8e9-124">Metadata changes</span></span>

<span data-ttu-id="ce8e9-125">これらのメタデータの変更は、このアップデートで行われました。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-125">These metadata changes have been made in this update.</span></span>

| <span data-ttu-id="ce8e9-126">工程</span><span class="sxs-lookup"><span data-stu-id="ce8e9-126">Operation</span></span> |
| --------------- |
|<span data-ttu-id="ce8e9-127">DataEntities/LedgerJournalNameEntity/Fields/DeleteLinesAfterPosting.Allow Edit</span><span class="sxs-lookup"><span data-stu-id="ce8e9-127">DataEntities/LedgerJournalNameEntity/Fields/DeleteLinesAfterPosting.Allow Edit</span></span>|
|<span data-ttu-id="ce8e9-128">DataEntities/LedgerJournalNameEntity/Fields/DeleteLinesAfterPosting.AllowEditOnCreate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-128">DataEntities/LedgerJournalNameEntity/Fields/DeleteLinesAfterPosting.AllowEditOnCreate</span></span>|
|<span data-ttu-id="ce8e9-129">Forms/AssetProposalDepreciation/Design/Tab/ParametersTabPage/ParametersGroup/SummarizedDepreciationControl.Value</span><span class="sxs-lookup"><span data-stu-id="ce8e9-129">Forms/AssetProposalDepreciation/Design/Tab/ParametersTabPage/ParametersGroup/SummarizedDepreciationControl.Value</span></span>|
|<span data-ttu-id="ce8e9-130">Data manipulation method not raising event: PriceDiscAdmDeleteTradeAgreements.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-130">Data manipulation method not raising event: PriceDiscAdmDeleteTradeAgreements.run</span></span>|
|<span data-ttu-id="ce8e9-131">Data Types/Base Enums/WHSReverseWorkMode.Label</span><span class="sxs-lookup"><span data-stu-id="ce8e9-131">Data Types/Base Enums/WHSReverseWorkMode.Label</span></span>|
|<span data-ttu-id="ce8e9-132">DataEntity smmProspectEntity はパブリックではありません</span><span class="sxs-lookup"><span data-stu-id="ce8e9-132">DataEntity smmProspectEntity is not public</span></span>|
|<span data-ttu-id="ce8e9-133">DataEntityView/GeneralJournalAccountEntryEntity.PublicCollectionName、PublicEntityName および IsPublic</span><span class="sxs-lookup"><span data-stu-id="ce8e9-133">DataEntityView/GeneralJournalAccountEntryEntity.PublicCollectionName, PublicEntityName and IsPublic</span></span>|
|<span data-ttu-id="ce8e9-134">Enum/HcmPersonGender/EnumValue/NonSpecific.Label</span><span class="sxs-lookup"><span data-stu-id="ce8e9-134">Enum/HcmPersonGender/EnumValue/NonSpecific.Label</span></span>|
|<span data-ttu-id="ce8e9-135">LedgerJournalEngine.shouldOverwriteAmountWithSettledAmount</span><span class="sxs-lookup"><span data-stu-id="ce8e9-135">LedgerJournalEngine.shouldOverwriteAmountWithSettledAmount</span></span>|
|<span data-ttu-id="ce8e9-136">Query/LedgerDerivedFinHierarchy/EcoResCategoryHierarchyRole_1/Ranges/NamedCategoryHierarchyRole.Range/Value</span><span class="sxs-lookup"><span data-stu-id="ce8e9-136">Query/LedgerDerivedFinHierarchy/EcoResCategoryHierarchyRole_1/Ranges/NamedCategoryHierarchyRole.Range/Value</span></span>|
|<span data-ttu-id="ce8e9-137">Table/TSTimesheetLine/TableFieldEnum</span><span class="sxs-lookup"><span data-stu-id="ce8e9-137">Table/TSTimesheetLine/TableFieldEnum</span></span>|
|<span data-ttu-id="ce8e9-138">Tables/InventTransPosting.DateVoucherTransIdx</span><span class="sxs-lookup"><span data-stu-id="ce8e9-138">Tables/InventTransPosting.DateVoucherTransIdx</span></span>|
|<span data-ttu-id="ce8e9-139">プロジェクトの価格決定テーブル内の固有のインデックスを更新します</span><span class="sxs-lookup"><span data-stu-id="ce8e9-139">Update unique indexes in pricing tables for project</span></span>|

## <a name="refactored-methods"></a><span data-ttu-id="ce8e9-140">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="ce8e9-140">Refactored methods</span></span>

<span data-ttu-id="ce8e9-141">これらのメソッドは、拡張性をサポートするためにリファクターされています。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-141">These methods have been refactored to support extensibility.</span></span>

| <span data-ttu-id="ce8e9-142">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="ce8e9-142">Refactored methods</span></span>                                                                             |
|------------------------------------------------------------------------------------------------|
|<span data-ttu-id="ce8e9-143">AgreementConfirmationDP.getAgreementLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-143">AgreementConfirmationDP.getAgreementLine</span></span>|
|<span data-ttu-id="ce8e9-144">AgreementConfirmationDP.getAgreementLineHistory</span><span class="sxs-lookup"><span data-stu-id="ce8e9-144">AgreementConfirmationDP.getAgreementLineHistory</span></span>|
|<span data-ttu-id="ce8e9-145">AssetBook.initDepreciationProfile</span><span class="sxs-lookup"><span data-stu-id="ce8e9-145">AssetBook.initDepreciationProfile</span></span>|
|<span data-ttu-id="ce8e9-146">AssetPost.createTrueUpDepreciation</span><span class="sxs-lookup"><span data-stu-id="ce8e9-146">AssetPost.createTrueUpDepreciation</span></span>|
|<span data-ttu-id="ce8e9-147">AssetPost.reduceLastDepreciation</span><span class="sxs-lookup"><span data-stu-id="ce8e9-147">AssetPost.reduceLastDepreciation</span></span>|
|<span data-ttu-id="ce8e9-148">Bank_CA.checkBankAccount</span><span class="sxs-lookup"><span data-stu-id="ce8e9-148">Bank_CA.checkBankAccount</span></span>|
|<span data-ttu-id="ce8e9-149">Bank_CA.checkBankRegNum</span><span class="sxs-lookup"><span data-stu-id="ce8e9-149">Bank_CA.checkBankRegNum</span></span>|
|<span data-ttu-id="ce8e9-150">BankReconMatchingRuleAutoProcessor.doProcessMatchRule</span><span class="sxs-lookup"><span data-stu-id="ce8e9-150">BankReconMatchingRuleAutoProcessor.doProcessMatchRule</span></span>|
|<span data-ttu-id="ce8e9-151">BankReconMatchingRuleAutoProcessor.performMatchAction</span><span class="sxs-lookup"><span data-stu-id="ce8e9-151">BankReconMatchingRuleAutoProcessor.performMatchAction</span></span>|
|<span data-ttu-id="ce8e9-152">BomCalcItem.calcCostSheet</span><span class="sxs-lookup"><span data-stu-id="ce8e9-152">BomCalcItem.calcCostSheet</span></span>|
|<span data-ttu-id="ce8e9-153">ChequeCopy.printCheque</span><span class="sxs-lookup"><span data-stu-id="ce8e9-153">ChequeCopy.printCheque</span></span>|
|<span data-ttu-id="ce8e9-154">ChequeDP.fetch</span><span class="sxs-lookup"><span data-stu-id="ce8e9-154">ChequeDP.fetch</span></span>|
|<span data-ttu-id="ce8e9-155">Coupons.AddCouponTrigger</span><span class="sxs-lookup"><span data-stu-id="ce8e9-155">Coupons.AddCouponTrigger</span></span>|
|<span data-ttu-id="ce8e9-156">Cust.initLedgerVoucher</span><span class="sxs-lookup"><span data-stu-id="ce8e9-156">Cust.initLedgerVoucher</span></span>|
|<span data-ttu-id="ce8e9-157">CustAgingReportDP.heading</span><span class="sxs-lookup"><span data-stu-id="ce8e9-157">CustAgingReportDP.heading</span></span>|
|<span data-ttu-id="ce8e9-158">CustBalanceList.constructAgingCalculation</span><span class="sxs-lookup"><span data-stu-id="ce8e9-158">CustBalanceList.constructAgingCalculation</span></span>|
|<span data-ttu-id="ce8e9-159">CustCollectionLetterCreate.createJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-159">CustCollectionLetterCreate.createJournal</span></span>|
|<span data-ttu-id="ce8e9-160">CustCollectionLetterCreate.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-160">CustCollectionLetterCreate.run</span></span>|
|<span data-ttu-id="ce8e9-161">CustCollectionLetterPost.updateQuery</span><span class="sxs-lookup"><span data-stu-id="ce8e9-161">CustCollectionLetterPost.updateQuery</span></span>|
|<span data-ttu-id="ce8e9-162">CustCollections.showAgingIndicator</span><span class="sxs-lookup"><span data-stu-id="ce8e9-162">CustCollections.showAgingIndicator</span></span>|
|<span data-ttu-id="ce8e9-163">CustCollectionsExcelStatement.setTransactionWorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="ce8e9-163">CustCollectionsExcelStatement.setTransactionWorksheetHeader</span></span>|
|<span data-ttu-id="ce8e9-164">CustDirectDebitMandate.lookupReference</span><span class="sxs-lookup"><span data-stu-id="ce8e9-164">CustDirectDebitMandate.lookupReference</span></span>|
|<span data-ttu-id="ce8e9-165">CustDirectDebitMandate.validateMandate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-165">CustDirectDebitMandate.validateMandate</span></span>|
|<span data-ttu-id="ce8e9-166">CustDirectDebitMandate.validateMandate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-166">CustDirectDebitMandate.validateMandate</span></span>|
|<span data-ttu-id="ce8e9-167">CustFreeInvoiceCorrection.createAdjustingCorrectedInvoice</span><span class="sxs-lookup"><span data-stu-id="ce8e9-167">CustFreeInvoiceCorrection.createAdjustingCorrectedInvoice</span></span>|
|<span data-ttu-id="ce8e9-168">CustFreeInvoiceCorrection.createTaxes</span><span class="sxs-lookup"><span data-stu-id="ce8e9-168">CustFreeInvoiceCorrection.createTaxes</span></span>|
|<span data-ttu-id="ce8e9-169">CustFreeInvoiceCorrectionPost.postAdjustingInvoice</span><span class="sxs-lookup"><span data-stu-id="ce8e9-169">CustFreeInvoiceCorrectionPost.postAdjustingInvoice</span></span>|
|<span data-ttu-id="ce8e9-170">CustFreeInvoiceCorrectionPost.validate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-170">CustFreeInvoiceCorrectionPost.validate</span></span>|
|<span data-ttu-id="ce8e9-171">CustinvoiceLine.insert</span><span class="sxs-lookup"><span data-stu-id="ce8e9-171">CustinvoiceLine.insert</span></span>|
|<span data-ttu-id="ce8e9-172">CustInvoicePrintJob.buildQueryForFreeText</span><span class="sxs-lookup"><span data-stu-id="ce8e9-172">CustInvoicePrintJob.buildQueryForFreeText</span></span>|
|<span data-ttu-id="ce8e9-173">CustInvoicePrintJob.processFreeText</span><span class="sxs-lookup"><span data-stu-id="ce8e9-173">CustInvoicePrintJob.processFreeText</span></span>|
|<span data-ttu-id="ce8e9-174">CustOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-174">CustOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="ce8e9-175">CustOpenTransReverse.markTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-175">CustOpenTransReverse.markTrans</span></span>|
|<span data-ttu-id="ce8e9-176">CustOverPaym.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-176">CustOverPaym.run</span></span>|
|<span data-ttu-id="ce8e9-177">CustPackingSlipJour.printJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-177">CustPackingSlipJour.printJournal</span></span>|
|<span data-ttu-id="ce8e9-178">CustPaymEntry.hasMultipleOpenTransReferences</span><span class="sxs-lookup"><span data-stu-id="ce8e9-178">CustPaymEntry.hasMultipleOpenTransReferences</span></span>|
|<span data-ttu-id="ce8e9-179">CustPaymEntry.isInvalidOpenTransReference</span><span class="sxs-lookup"><span data-stu-id="ce8e9-179">CustPaymEntry.isInvalidOpenTransReference</span></span>|
|<span data-ttu-id="ce8e9-180">CustPostInvoice.allocateNumAndVoucher</span><span class="sxs-lookup"><span data-stu-id="ce8e9-180">CustPostInvoice.allocateNumAndVoucher</span></span>|
|<span data-ttu-id="ce8e9-181">CustPostInvoice.createJournalHeader</span><span class="sxs-lookup"><span data-stu-id="ce8e9-181">CustPostInvoice.createJournalHeader</span></span>|
|<span data-ttu-id="ce8e9-182">CustRecurrenceInvoicePostService.postRecurrenceInvoice</span><span class="sxs-lookup"><span data-stu-id="ce8e9-182">CustRecurrenceInvoicePostService.postRecurrenceInvoice</span></span>|
|<span data-ttu-id="ce8e9-183">CustSettlementPriorityProcessing.initCustTransOpen</span><span class="sxs-lookup"><span data-stu-id="ce8e9-183">CustSettlementPriorityProcessing.initCustTransOpen</span></span>|
|<span data-ttu-id="ce8e9-184">CustStatistics.TmpStatPer.linkActive</span><span class="sxs-lookup"><span data-stu-id="ce8e9-184">CustStatistics.TmpStatPer.linkActive</span></span>|
|<span data-ttu-id="ce8e9-185">CustTable.createRecord</span><span class="sxs-lookup"><span data-stu-id="ce8e9-185">CustTable.createRecord</span></span>|
|<span data-ttu-id="ce8e9-186">CustTable.CustTable_DS/fields/CustGroup/modified</span><span class="sxs-lookup"><span data-stu-id="ce8e9-186">CustTable.CustTable_DS/fields/CustGroup/modified</span></span>|
|<span data-ttu-id="ce8e9-187">CustVendCheque.checkDataOk</span><span class="sxs-lookup"><span data-stu-id="ce8e9-187">CustVendCheque.checkDataOk</span></span>|
|<span data-ttu-id="ce8e9-188">CustVendCheque.output</span><span class="sxs-lookup"><span data-stu-id="ce8e9-188">CustVendCheque.output</span></span>|
|<span data-ttu-id="ce8e9-189">CustVendChequeSlipTextCalculator.getMaxSlipLines</span><span class="sxs-lookup"><span data-stu-id="ce8e9-189">CustVendChequeSlipTextCalculator.getMaxSlipLines</span></span>|
|<span data-ttu-id="ce8e9-190">CustVendChequeSlipTextCalculator.getUnprintableReportArea</span><span class="sxs-lookup"><span data-stu-id="ce8e9-190">CustVendChequeSlipTextCalculator.getUnprintableReportArea</span></span>|
|<span data-ttu-id="ce8e9-191">CustVendCreatePaymJournal.runPaymentProposalGenerationProcess</span><span class="sxs-lookup"><span data-stu-id="ce8e9-191">CustVendCreatePaymJournal.runPaymentProposalGenerationProcess</span></span>|
|<span data-ttu-id="ce8e9-192">CustVendCreatePaymJournal.runPaymentProposalGenerationProcess</span><span class="sxs-lookup"><span data-stu-id="ce8e9-192">CustVendCreatePaymJournal.runPaymentProposalGenerationProcess</span></span>|
|<span data-ttu-id="ce8e9-193">CustVendOpenTransManager.createTaxWithholding</span><span class="sxs-lookup"><span data-stu-id="ce8e9-193">CustVendOpenTransManager.createTaxWithholding</span></span>|
|<span data-ttu-id="ce8e9-194">CustVendPaymProposal.addCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="ce8e9-194">CustVendPaymProposal.addCustVendTransOpen</span></span>|
|<span data-ttu-id="ce8e9-195">CustVendReversePosting.restoreCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="ce8e9-195">CustVendReversePosting.restoreCustVendTransOpen</span></span>|
|<span data-ttu-id="ce8e9-196">CustWriteOff.calcSalesTaxOnOpenTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-196">CustWriteOff.calcSalesTaxOnOpenTrans</span></span>|
|<span data-ttu-id="ce8e9-197">CustWriteOff.generateSummarizedTmpTaxTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-197">CustWriteOff.generateSummarizedTmpTaxTrans</span></span>|
|<span data-ttu-id="ce8e9-198">DataEntityView/ExpenseJournalLineEntity.DataEntityView/ExpenseJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="ce8e9-198">DataEntityView/ExpenseJournalLineEntity.DataEntityView/ExpenseJournalLineEntity</span></span>|
|<span data-ttu-id="ce8e9-199">DirPartyPostalAddressFormHandlerExt.onUpdateTransactionCaller_delegate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-199">DirPartyPostalAddressFormHandlerExt.onUpdateTransactionCaller_delegate</span></span>|
|<span data-ttu-id="ce8e9-200">拡張可能クラス メソッド: PriceDisc.mcrPriceDiscTableFound</span><span class="sxs-lookup"><span data-stu-id="ce8e9-200">Extensible class method: PriceDisc.mcrPriceDiscTableFound</span></span>|
|<span data-ttu-id="ce8e9-201">FBSpedFileCreator_Contabil_BR.createRecordI052</span><span class="sxs-lookup"><span data-stu-id="ce8e9-201">FBSpedFileCreator_Contabil_BR.createRecordI052</span></span>|
|<span data-ttu-id="ce8e9-202">FiscalDocumentDate_BR.lastIssueDateForSeries</span><span class="sxs-lookup"><span data-stu-id="ce8e9-202">FiscalDocumentDate_BR.lastIssueDateForSeries</span></span>|
|<span data-ttu-id="ce8e9-203">HrpSigningLimitPolicyUtil.createDefaultLimit</span><span class="sxs-lookup"><span data-stu-id="ce8e9-203">HrpSigningLimitPolicyUtil.createDefaultLimit</span></span>|
|<span data-ttu-id="ce8e9-204">HrpSigningLimitPolicyUtil.insertJobOrCompensationRule</span><span class="sxs-lookup"><span data-stu-id="ce8e9-204">HrpSigningLimitPolicyUtil.insertJobOrCompensationRule</span></span>|
|<span data-ttu-id="ce8e9-205">HrpSigningLimitPolicyUtil.private RefRecId checkLimitAgreementDetail(HRPTmpLimitAgreementRule _tmpLimitAgreementRule,HRPAuthorityBasis _authorityBasis)</span><span class="sxs-lookup"><span data-stu-id="ce8e9-205">HrpSigningLimitPolicyUtil.private RefRecId checkLimitAgreementDetail(HRPTmpLimitAgreementRule _tmpLimitAgreementRule,HRPAuthorityBasis _authorityBasis)</span></span>|
|<span data-ttu-id="ce8e9-206">HrpWorkerLimit.private recId getAuthBaseRecId(HRPAuthorityBasis _authBasis, RefRecId _positionId)</span><span class="sxs-lookup"><span data-stu-id="ce8e9-206">HrpWorkerLimit.private recId getAuthBaseRecId(HRPAuthorityBasis _authBasis, RefRecId _positionId)</span></span>|
|<span data-ttu-id="ce8e9-207">InterCompanySyncPurchTableType.setSalesTableData</span><span class="sxs-lookup"><span data-stu-id="ce8e9-207">InterCompanySyncPurchTableType.setSalesTableData</span></span>|
|<span data-ttu-id="ce8e9-208">InventCountCreate_Base.doCountingBasedOnCountCode</span><span class="sxs-lookup"><span data-stu-id="ce8e9-208">InventCountCreate_Base.doCountingBasedOnCountCode</span></span>|
|<span data-ttu-id="ce8e9-209">InventMov_Purch.updateAutoLossProfit</span><span class="sxs-lookup"><span data-stu-id="ce8e9-209">InventMov_Purch.updateAutoLossProfit</span></span>|
|<span data-ttu-id="ce8e9-210">InventMov_Purch.updateLedgerFinancial</span><span class="sxs-lookup"><span data-stu-id="ce8e9-210">InventMov_Purch.updateLedgerFinancial</span></span>|
|<span data-ttu-id="ce8e9-211">InventMovement.addLedgerPhysicalAmounts</span><span class="sxs-lookup"><span data-stu-id="ce8e9-211">InventMovement.addLedgerPhysicalAmounts</span></span>|
|<span data-ttu-id="ce8e9-212">InventMovement.addLedgerVoucherRevenueTransactionAmountsForFinancialUpdate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-212">InventMovement.addLedgerVoucherRevenueTransactionAmountsForFinancialUpdate</span></span>|
|<span data-ttu-id="ce8e9-213">InventMovement.addLedgerVoucherRevenueTransactionAmountsForPhysicalUpdate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-213">InventMovement.addLedgerVoucherRevenueTransactionAmountsForPhysicalUpdate</span></span>|
|<span data-ttu-id="ce8e9-214">InventMovement.addLedgerVoucherTransactionAmountsForFinancialUpdate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-214">InventMovement.addLedgerVoucherTransactionAmountsForFinancialUpdate</span></span>|
|<span data-ttu-id="ce8e9-215">InventMovement.addLedgerVoucherTransactionAmountsForPhysicalUpdate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-215">InventMovement.addLedgerVoucherTransactionAmountsForPhysicalUpdate</span></span>|
|<span data-ttu-id="ce8e9-216">InventMovement.checkUpdatePhysical</span><span class="sxs-lookup"><span data-stu-id="ce8e9-216">InventMovement.checkUpdatePhysical</span></span>|
|<span data-ttu-id="ce8e9-217">InventMovement.processLedgerPhysicalAmountList</span><span class="sxs-lookup"><span data-stu-id="ce8e9-217">InventMovement.processLedgerPhysicalAmountList</span></span>|
|<span data-ttu-id="ce8e9-218">InventMovement.setAutoReserving</span><span class="sxs-lookup"><span data-stu-id="ce8e9-218">InventMovement.setAutoReserving</span></span>|
|<span data-ttu-id="ce8e9-219">InventMovement.setCostAmountPhysical</span><span class="sxs-lookup"><span data-stu-id="ce8e9-219">InventMovement.setCostAmountPhysical</span></span>|
|<span data-ttu-id="ce8e9-220">InventMovement.updateLedgerAdjust</span><span class="sxs-lookup"><span data-stu-id="ce8e9-220">InventMovement.updateLedgerAdjust</span></span>|
|<span data-ttu-id="ce8e9-221">InventMovement.updateLedgerFinancial</span><span class="sxs-lookup"><span data-stu-id="ce8e9-221">InventMovement.updateLedgerFinancial</span></span>|
|<span data-ttu-id="ce8e9-222">InventOnhandReserve.updateReserveLot</span><span class="sxs-lookup"><span data-stu-id="ce8e9-222">InventOnhandReserve.updateReserveLot</span></span>|
|<span data-ttu-id="ce8e9-223">InventUpd_Estimated</span><span class="sxs-lookup"><span data-stu-id="ce8e9-223">InventUpd_Estimated</span></span>|
|<span data-ttu-id="ce8e9-224">InventUpd_Estimated.updateFieldsChange</span><span class="sxs-lookup"><span data-stu-id="ce8e9-224">InventUpd_Estimated.updateFieldsChange</span></span>|
|<span data-ttu-id="ce8e9-225">JmgPayEventsExport_Std.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-225">JmgPayEventsExport_Std.run</span></span>|
|<span data-ttu-id="ce8e9-226">JmgStampJournalTable.approve</span><span class="sxs-lookup"><span data-stu-id="ce8e9-226">JmgStampJournalTable.approve</span></span>|
|<span data-ttu-id="ce8e9-227">JmgStampJournalTable.transfer</span><span class="sxs-lookup"><span data-stu-id="ce8e9-227">JmgStampJournalTable.transfer</span></span>|
|<span data-ttu-id="ce8e9-228">LedgerAccrualTrans.post</span><span class="sxs-lookup"><span data-stu-id="ce8e9-228">LedgerAccrualTrans.post</span></span>|
|<span data-ttu-id="ce8e9-229">LedgerAllocationBasisRules.createGeneralJournalAccountEntrySumQuery</span><span class="sxs-lookup"><span data-stu-id="ce8e9-229">LedgerAllocationBasisRules.createGeneralJournalAccountEntrySumQuery</span></span>|
|<span data-ttu-id="ce8e9-230">LedgerAllocationController.allocateAmounts</span><span class="sxs-lookup"><span data-stu-id="ce8e9-230">LedgerAllocationController.allocateAmounts</span></span>|
|<span data-ttu-id="ce8e9-231">LedgerAllocationProcessRequest.allocate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-231">LedgerAllocationProcessRequest.allocate</span></span>|
|<span data-ttu-id="ce8e9-232">LedgerJournalCheckPost.checkJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-232">LedgerJournalCheckPost.checkJournal</span></span>|
|<span data-ttu-id="ce8e9-233">LedgerJournalCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-233">LedgerJournalCheckPost.postJournal</span></span>|
|<span data-ttu-id="ce8e9-234">LedgerJournalDistribute.createNewJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-234">LedgerJournalDistribute.createNewJournal</span></span>|
|<span data-ttu-id="ce8e9-235">LedgerJournalEngine.calculateTaxForCompleteJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-235">LedgerJournalEngine.calculateTaxForCompleteJournal</span></span>|
|<span data-ttu-id="ce8e9-236">LedgerJournalEngine.initValue</span><span class="sxs-lookup"><span data-stu-id="ce8e9-236">LedgerJournalEngine.initValue</span></span>|
|<span data-ttu-id="ce8e9-237">LedgerJournalTable.deleteAllLines</span><span class="sxs-lookup"><span data-stu-id="ce8e9-237">LedgerJournalTable.deleteAllLines</span></span>|
|<span data-ttu-id="ce8e9-238">LedgerJournalTrans.deleteTaxUncommitted</span><span class="sxs-lookup"><span data-stu-id="ce8e9-238">LedgerJournalTrans.deleteTaxUncommitted</span></span>|
|<span data-ttu-id="ce8e9-239">LedgerJournalTransDaily.LedgerJournalTrans.AmountCurCredit.validate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-239">LedgerJournalTransDaily.LedgerJournalTrans.AmountCurCredit.validate</span></span>|
|<span data-ttu-id="ce8e9-240">LedgerJournalTransDaily.LedgerJournalTrans.AmountCurDebit.validate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-240">LedgerJournalTransDaily.LedgerJournalTrans.AmountCurDebit.validate</span></span>|
|<span data-ttu-id="ce8e9-241">LedgerJournalTransType.validateVoucher</span><span class="sxs-lookup"><span data-stu-id="ce8e9-241">LedgerJournalTransType.validateVoucher</span></span>|
|<span data-ttu-id="ce8e9-242">LedgerJournalTransUpdate.updateIntercompany</span><span class="sxs-lookup"><span data-stu-id="ce8e9-242">LedgerJournalTransUpdate.updateIntercompany</span></span>|
|<span data-ttu-id="ce8e9-243">LedgerJournalTransVendPaym./Forms/LedgerJournalTransVendPaym/Design/ActionPane(ActionPane)/ButtonGroup(ButtonGroup)/buttonCreatePayment(MenuFunctionButton)/Clicked</span><span class="sxs-lookup"><span data-stu-id="ce8e9-243">LedgerJournalTransVendPaym./Forms/LedgerJournalTransVendPaym/Design/ActionPane(ActionPane)/ButtonGroup(ButtonGroup)/buttonCreatePayment(MenuFunctionButton)/Clicked</span></span>|
|<span data-ttu-id="ce8e9-244">LedgerTransListReportHelper.buildFieldMap</span><span class="sxs-lookup"><span data-stu-id="ce8e9-244">LedgerTransListReportHelper.buildFieldMap</span></span>|
|<span data-ttu-id="ce8e9-245">LedgerTransPerJournalDP.insertForLedgerBase</span><span class="sxs-lookup"><span data-stu-id="ce8e9-245">LedgerTransPerJournalDP.insertForLedgerBase</span></span>|
|<span data-ttu-id="ce8e9-246">LedgerVoucherObject.checkBalance</span><span class="sxs-lookup"><span data-stu-id="ce8e9-246">LedgerVoucherObject.checkBalance</span></span>|
|<span data-ttu-id="ce8e9-247">LedgerVoucherObject.checkBalanceRound</span><span class="sxs-lookup"><span data-stu-id="ce8e9-247">LedgerVoucherObject.checkBalanceRound</span></span>|
|<span data-ttu-id="ce8e9-248">LogisticsLocationFormHandler.callerResearch</span><span class="sxs-lookup"><span data-stu-id="ce8e9-248">LogisticsLocationFormHandler.callerResearch</span></span>|
|<span data-ttu-id="ce8e9-249">LoyaltyCardBlance.MPOS_ExtensibleViews</span><span class="sxs-lookup"><span data-stu-id="ce8e9-249">LoyaltyCardBlance.MPOS_ExtensibleViews</span></span>|
|<span data-ttu-id="ce8e9-250">Macros.InventSumFields</span><span class="sxs-lookup"><span data-stu-id="ce8e9-250">Macros.InventSumFields</span></span>|
|<span data-ttu-id="ce8e9-251">MainAccount.DimensionAttributeValue_ds/dimensionAttributeValueIsSuspended</span><span class="sxs-lookup"><span data-stu-id="ce8e9-251">MainAccount.DimensionAttributeValue_ds/dimensionAttributeValueIsSuspended</span></span>|
|<span data-ttu-id="ce8e9-252">NumberSeqModuleProject.loadModule</span><span class="sxs-lookup"><span data-stu-id="ce8e9-252">NumberSeqModuleProject.loadModule</span></span>|
|<span data-ttu-id="ce8e9-253">PcSourceDocumentLineUtility.initialize</span><span class="sxs-lookup"><span data-stu-id="ce8e9-253">PcSourceDocumentLineUtility.initialize</span></span>|
|<span data-ttu-id="ce8e9-254">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim + run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-254">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim + run</span></span>|
|<span data-ttu-id="ce8e9-255">PriceDisc.findPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="ce8e9-255">PriceDisc.findPriceAgreement</span></span>|
|<span data-ttu-id="ce8e9-256">PriceDisc.FindPriceAgreement.mcrPriceDiscTablefound</span><span class="sxs-lookup"><span data-stu-id="ce8e9-256">PriceDisc.FindPriceAgreement.mcrPriceDiscTablefound</span></span>|
|<span data-ttu-id="ce8e9-257">PriceDiscResultFields.NA</span><span class="sxs-lookup"><span data-stu-id="ce8e9-257">PriceDiscResultFields.NA</span></span>|
|<span data-ttu-id="ce8e9-258">ProdJournalBOM.insertJournalCreate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-258">ProdJournalBOM.insertJournalCreate</span></span>|
|<span data-ttu-id="ce8e9-259">ProjAdjustment.splitLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-259">ProjAdjustment.splitLine</span></span>|
|<span data-ttu-id="ce8e9-260">ProjAdjustmentSplit.calculateQty</span><span class="sxs-lookup"><span data-stu-id="ce8e9-260">ProjAdjustmentSplit.calculateQty</span></span>|
|<span data-ttu-id="ce8e9-261">ProjAdjustmentSplit.getNewTotalSaleAmount</span><span class="sxs-lookup"><span data-stu-id="ce8e9-261">ProjAdjustmentSplit.getNewTotalSaleAmount</span></span>|
|<span data-ttu-id="ce8e9-262">ProjAdjustmentUpdate.newPostAdjustment</span><span class="sxs-lookup"><span data-stu-id="ce8e9-262">ProjAdjustmentUpdate.newPostAdjustment</span></span>|
|<span data-ttu-id="ce8e9-263">ProjAdjustmentUpdate.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-263">ProjAdjustmentUpdate.run</span></span>|
|<span data-ttu-id="ce8e9-264">ProjAdjustmentUpdate.transCostNew / transEmplNew / transItemNew メソッド</span><span class="sxs-lookup"><span data-stu-id="ce8e9-264">ProjAdjustmentUpdate.transCostNew / transEmplNew / transItemNew methods</span></span>|
|<span data-ttu-id="ce8e9-265">ProjAdjustmentUpdate.transItemNew</span><span class="sxs-lookup"><span data-stu-id="ce8e9-265">ProjAdjustmentUpdate.transItemNew</span></span>|
|<span data-ttu-id="ce8e9-266">ProjAdjustmentUpdate.updateAdjusted</span><span class="sxs-lookup"><span data-stu-id="ce8e9-266">ProjAdjustmentUpdate.updateAdjusted</span></span>|
|<span data-ttu-id="ce8e9-267">ProjBudgetImport.SourceType - 変更済み</span><span class="sxs-lookup"><span data-stu-id="ce8e9-267">ProjBudgetImport.SourceType - modified</span></span>|
|<span data-ttu-id="ce8e9-268">ProjBudgetRevision.updateGridHelper</span><span class="sxs-lookup"><span data-stu-id="ce8e9-268">ProjBudgetRevision.updateGridHelper</span></span>|
|<span data-ttu-id="ce8e9-269">ProjectPosting.getProjectLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="ce8e9-269">ProjectPosting.getProjectLedgerDimension</span></span>|
|<span data-ttu-id="ce8e9-270">ProjForecastEmpl.initValue</span><span class="sxs-lookup"><span data-stu-id="ce8e9-270">ProjForecastEmpl.initValue</span></span>|
|<span data-ttu-id="ce8e9-271">ProjFormletterParmData.updateQueryBuild</span><span class="sxs-lookup"><span data-stu-id="ce8e9-271">ProjFormletterParmData.updateQueryBuild</span></span>|
|<span data-ttu-id="ce8e9-272">ProjGrant.canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="ce8e9-272">ProjGrant.canSubmitToWorkflow</span></span>|
|<span data-ttu-id="ce8e9-273">ProjInvoiceChoose.doCost</span><span class="sxs-lookup"><span data-stu-id="ce8e9-273">ProjInvoiceChoose.doCost</span></span>|
|<span data-ttu-id="ce8e9-274">ProjInvoiceChoose.doEmpl</span><span class="sxs-lookup"><span data-stu-id="ce8e9-274">ProjInvoiceChoose.doEmpl</span></span>|
|<span data-ttu-id="ce8e9-275">ProjInvoiceChoose.doItem</span><span class="sxs-lookup"><span data-stu-id="ce8e9-275">ProjInvoiceChoose.doItem</span></span>|
|<span data-ttu-id="ce8e9-276">ProjInvoiceChoose.doOnAccount</span><span class="sxs-lookup"><span data-stu-id="ce8e9-276">ProjInvoiceChoose.doOnAccount</span></span>|
|<span data-ttu-id="ce8e9-277">ProjInvoiceChoose.doRevenue</span><span class="sxs-lookup"><span data-stu-id="ce8e9-277">ProjInvoiceChoose.doRevenue</span></span>|
|<span data-ttu-id="ce8e9-278">ProjInvoiceChoose.doSalesLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-278">ProjInvoiceChoose.doSalesLine</span></span>|
|<span data-ttu-id="ce8e9-279">ProjInvoiceChoose.psaAddEndDateToProposalJour</span><span class="sxs-lookup"><span data-stu-id="ce8e9-279">ProjInvoiceChoose.psaAddEndDateToProposalJour</span></span>|
|<span data-ttu-id="ce8e9-280">ProjInvoiceEditLines.Choose.clicked</span><span class="sxs-lookup"><span data-stu-id="ce8e9-280">ProjInvoiceEditLines.Choose.clicked</span></span>|
|<span data-ttu-id="ce8e9-281">ProjInvoiceEditLines.closeOk</span><span class="sxs-lookup"><span data-stu-id="ce8e9-281">ProjInvoiceEditLines.closeOk</span></span>|
|<span data-ttu-id="ce8e9-282">ProjInvoiceProposalCreateLines.modifiedTransFilter</span><span class="sxs-lookup"><span data-stu-id="ce8e9-282">ProjInvoiceProposalCreateLines.modifiedTransFilter</span></span>|
|<span data-ttu-id="ce8e9-283">ProjInvoiceProposalCreateLines.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-283">ProjInvoiceProposalCreateLines.run</span></span>|
|<span data-ttu-id="ce8e9-284">ProjInvoiceProposalCreateLines.runSalesLineQuery</span><span class="sxs-lookup"><span data-stu-id="ce8e9-284">ProjInvoiceProposalCreateLines.runSalesLineQuery</span></span>|
|<span data-ttu-id="ce8e9-285">ProjInvoiceProposalInsertLines.doSalesLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-285">ProjInvoiceProposalInsertLines.doSalesLine</span></span>|
|<span data-ttu-id="ce8e9-286">ProjInvoiceProposalInsertLines.setProjProposalJour</span><span class="sxs-lookup"><span data-stu-id="ce8e9-286">ProjInvoiceProposalInsertLines.setProjProposalJour</span></span>|
|<span data-ttu-id="ce8e9-287">ProjInvoiceTable.createProposalJour</span><span class="sxs-lookup"><span data-stu-id="ce8e9-287">ProjInvoiceTable.createProposalJour</span></span>|
|<span data-ttu-id="ce8e9-288">ProjLedgerUpdate.insert</span><span class="sxs-lookup"><span data-stu-id="ce8e9-288">ProjLedgerUpdate.insert</span></span>|
|<span data-ttu-id="ce8e9-289">ProjListTransDP.insertTmpTable</span><span class="sxs-lookup"><span data-stu-id="ce8e9-289">ProjListTransDP.insertTmpTable</span></span>|
|<span data-ttu-id="ce8e9-290">ProjPostItemPackingSlip .projTransCreate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-290">ProjPostItemPackingSlip .projTransCreate</span></span>|
|<span data-ttu-id="ce8e9-291">ProjPostItemTransCost_Adj.projTransUpdate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-291">ProjPostItemTransCost_Adj.projTransUpdate</span></span>|
|<span data-ttu-id="ce8e9-292">ProjSplitBill.maxAllowedByLimits</span><span class="sxs-lookup"><span data-stu-id="ce8e9-292">ProjSplitBill.maxAllowedByLimits</span></span>|
|<span data-ttu-id="ce8e9-293">ProjStatusTypeRule.enableRule</span><span class="sxs-lookup"><span data-stu-id="ce8e9-293">ProjStatusTypeRule.enableRule</span></span>|
|<span data-ttu-id="ce8e9-294">ProjTable.isCustomerTransferNeeded</span><span class="sxs-lookup"><span data-stu-id="ce8e9-294">ProjTable.isCustomerTransferNeeded</span></span>|
|<span data-ttu-id="ce8e9-295">ProjTableType.validateWrite</span><span class="sxs-lookup"><span data-stu-id="ce8e9-295">ProjTableType.validateWrite</span></span>|
|<span data-ttu-id="ce8e9-296">ProjValCheckTrans.validateMandatory</span><span class="sxs-lookup"><span data-stu-id="ce8e9-296">ProjValCheckTrans.validateMandatory</span></span>|
|<span data-ttu-id="ce8e9-297">PsaProjAndContractInvoiceController.runPrintMgmt</span><span class="sxs-lookup"><span data-stu-id="ce8e9-297">PsaProjAndContractInvoiceController.runPrintMgmt</span></span>|
|<span data-ttu-id="ce8e9-298">PSAProjRetainerInvoicing.createTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-298">PSAProjRetainerInvoicing.createTrans</span></span>|
|<span data-ttu-id="ce8e9-299">PSAProjRetainerInvoicing.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-299">PSAProjRetainerInvoicing.run</span></span>|
|<span data-ttu-id="ce8e9-300">PurchAutoCreate_PurchReq.getPurchLineName</span><span class="sxs-lookup"><span data-stu-id="ce8e9-300">PurchAutoCreate_PurchReq.getPurchLineName</span></span>|
|<span data-ttu-id="ce8e9-301">PurchAutoCreate_Sales.createLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-301">PurchAutoCreate_Sales.createLine</span></span>|
|<span data-ttu-id="ce8e9-302">PurchCopying.updatePriceDiscLineChangePolicy</span><span class="sxs-lookup"><span data-stu-id="ce8e9-302">PurchCopying.updatePriceDiscLineChangePolicy</span></span>|
|<span data-ttu-id="ce8e9-303">PurchCreateFromSalesOrder.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-303">PurchCreateFromSalesOrder.run</span></span>|
|<span data-ttu-id="ce8e9-304">PurchCreateOrder.PurchTable.write</span><span class="sxs-lookup"><span data-stu-id="ce8e9-304">PurchCreateOrder.PurchTable.write</span></span>|
|<span data-ttu-id="ce8e9-305">PurchEditLines.Choose_Button.clicked</span><span class="sxs-lookup"><span data-stu-id="ce8e9-305">PurchEditLines.Choose_Button.clicked</span></span>|
|<span data-ttu-id="ce8e9-306">PurchEditLines.run</span><span class="sxs-lookup"><span data-stu-id="ce8e9-306">PurchEditLines.run</span></span>|
|<span data-ttu-id="ce8e9-307">PurchFormLetter.prePromptInit</span><span class="sxs-lookup"><span data-stu-id="ce8e9-307">PurchFormLetter.prePromptInit</span></span>|
|<span data-ttu-id="ce8e9-308">PurchFormLetter.reSelect</span><span class="sxs-lookup"><span data-stu-id="ce8e9-308">PurchFormLetter.reSelect</span></span>|
|<span data-ttu-id="ce8e9-309">PurchFormLetter::main</span><span class="sxs-lookup"><span data-stu-id="ce8e9-309">PurchFormLetter::main</span></span>|
|<span data-ttu-id="ce8e9-310">PurchFormletterParmDataInvoice.reSelectLines</span><span class="sxs-lookup"><span data-stu-id="ce8e9-310">PurchFormletterParmDataInvoice.reSelectLines</span></span>|
|<span data-ttu-id="ce8e9-311">PurchInvoiceJournalCreate.allocateNumAndVoucher</span><span class="sxs-lookup"><span data-stu-id="ce8e9-311">PurchInvoiceJournalCreate.allocateNumAndVoucher</span></span>|
|<span data-ttu-id="ce8e9-312">PurchReqAddItem.N/A: 変数の変更 (メソッドではなく)</span><span class="sxs-lookup"><span data-stu-id="ce8e9-312">PurchReqAddItem.N/A: Variable Change, not Method</span></span>|
|<span data-ttu-id="ce8e9-313">PurchRFQCaseTable.isCalledFromPurchRFQCTListPageProject</span><span class="sxs-lookup"><span data-stu-id="ce8e9-313">PurchRFQCaseTable.isCalledFromPurchRFQCTListPageProject</span></span>|
|<span data-ttu-id="ce8e9-314">PurchTable.ConvertCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="ce8e9-314">PurchTable.ConvertCurrencyCode</span></span>|
|<span data-ttu-id="ce8e9-315">PurchTable.create</span><span class="sxs-lookup"><span data-stu-id="ce8e9-315">PurchTable.create</span></span>|
|<span data-ttu-id="ce8e9-316">PurchTable.create (PurchTable データ ソース)</span><span class="sxs-lookup"><span data-stu-id="ce8e9-316">PurchTable.create (PurchTable datasource)</span></span>|
|<span data-ttu-id="ce8e9-317">PurchTableType.validateDelete</span><span class="sxs-lookup"><span data-stu-id="ce8e9-317">PurchTableType.validateDelete</span></span>|
|<span data-ttu-id="ce8e9-318">ReqCalc.actionCalcItem</span><span class="sxs-lookup"><span data-stu-id="ce8e9-318">ReqCalc.actionCalcItem</span></span>|
|<span data-ttu-id="ce8e9-319">ReqCalc.covCalcDim</span><span class="sxs-lookup"><span data-stu-id="ce8e9-319">ReqCalc.covCalcDim</span></span>|
|<span data-ttu-id="ce8e9-320">ReqCalc.covCodeQtyMinMax</span><span class="sxs-lookup"><span data-stu-id="ce8e9-320">ReqCalc.covCodeQtyMinMax</span></span>|
|<span data-ttu-id="ce8e9-321">ReqCalc.covCreatePlannedOrder</span><span class="sxs-lookup"><span data-stu-id="ce8e9-321">ReqCalc.covCreatePlannedOrder</span></span>|
|<span data-ttu-id="ce8e9-322">ReqCalc.covCreateSafetyInvent</span><span class="sxs-lookup"><span data-stu-id="ce8e9-322">ReqCalc.covCreateSafetyInvent</span></span>|
|<span data-ttu-id="ce8e9-323">ReqCalc.createSafetyInvent</span><span class="sxs-lookup"><span data-stu-id="ce8e9-323">ReqCalc.createSafetyInvent</span></span>|
|<span data-ttu-id="ce8e9-324">ReqCalc.createSafetyInventKey</span><span class="sxs-lookup"><span data-stu-id="ce8e9-324">ReqCalc.createSafetyInventKey</span></span>|
|<span data-ttu-id="ce8e9-325">ReqCalc.deleteTransactionAndCoverage</span><span class="sxs-lookup"><span data-stu-id="ce8e9-325">ReqCalc.deleteTransactionAndCoverage</span></span>|
|<span data-ttu-id="ce8e9-326">ReqCalc.setParameters</span><span class="sxs-lookup"><span data-stu-id="ce8e9-326">ReqCalc.setParameters</span></span>|
|<span data-ttu-id="ce8e9-327">ReqCalc.writeInventSum</span><span class="sxs-lookup"><span data-stu-id="ce8e9-327">ReqCalc.writeInventSum</span></span>|
|<span data-ttu-id="ce8e9-328">ReqTransCache.listCovDimSorted</span><span class="sxs-lookup"><span data-stu-id="ce8e9-328">ReqTransCache.listCovDimSorted</span></span>|
|<span data-ttu-id="ce8e9-329">ReqTransPoMarkFirm.create</span><span class="sxs-lookup"><span data-stu-id="ce8e9-329">ReqTransPoMarkFirm.create</span></span>|
|<span data-ttu-id="ce8e9-330">RequisitionPurchaseOrderGeneration.updateEmptyVendAccountsForManualCreation</span><span class="sxs-lookup"><span data-stu-id="ce8e9-330">RequisitionPurchaseOrderGeneration.updateEmptyVendAccountsForManualCreation</span></span>|
|<span data-ttu-id="ce8e9-331">RequisitionPurchaseOrderGeneration.validatePurchReqLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-331">RequisitionPurchaseOrderGeneration.validatePurchReqLine</span></span>|
|<span data-ttu-id="ce8e9-332">RetailInternalOrganization.insert</span><span class="sxs-lookup"><span data-stu-id="ce8e9-332">RetailInternalOrganization.insert</span></span>|
|<span data-ttu-id="ce8e9-333">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-333">RetailKitAssemblyOrder.createOrUpdateBOMJournal</span></span>|
|<span data-ttu-id="ce8e9-334">RetailKitAssemblyOrder.createOrUpdateBOMJournalLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-334">RetailKitAssemblyOrder.createOrUpdateBOMJournalLine</span></span>|
|<span data-ttu-id="ce8e9-335">RetailStatementPost.postRetailSpecific</span><span class="sxs-lookup"><span data-stu-id="ce8e9-335">RetailStatementPost.postRetailSpecific</span></span>|
|<span data-ttu-id="ce8e9-336">RetailStoresToDeploy.setAllowEditTrue</span><span class="sxs-lookup"><span data-stu-id="ce8e9-336">RetailStoresToDeploy.setAllowEditTrue</span></span>|
|<span data-ttu-id="ce8e9-337">RetailTransactionSalesTransMark.findInventDimIdFromWorkingTable</span><span class="sxs-lookup"><span data-stu-id="ce8e9-337">RetailTransactionSalesTransMark.findInventDimIdFromWorkingTable</span></span>|
|<span data-ttu-id="ce8e9-338">RetailTransactionSalesTransMark.populateTransactionSalesLineWorkingTable</span><span class="sxs-lookup"><span data-stu-id="ce8e9-338">RetailTransactionSalesTransMark.populateTransactionSalesLineWorkingTable</span></span>|
|<span data-ttu-id="ce8e9-339">RetailTransactionServiceOrders.cancelCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="ce8e9-339">RetailTransactionServiceOrders.cancelCustomerOrder</span></span>|
|<span data-ttu-id="ce8e9-340">RetailTransactionServiceOrders.createCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="ce8e9-340">RetailTransactionServiceOrders.createCustomerOrder</span></span>|
|<span data-ttu-id="ce8e9-341">RetailTransactionServiceOrders.createLedgerJournalTransForPayment</span><span class="sxs-lookup"><span data-stu-id="ce8e9-341">RetailTransactionServiceOrders.createLedgerJournalTransForPayment</span></span>|
|<span data-ttu-id="ce8e9-342">RetailTransactionServiceOrders.createRetailOrderPayment</span><span class="sxs-lookup"><span data-stu-id="ce8e9-342">RetailTransactionServiceOrders.createRetailOrderPayment</span></span>|
|<span data-ttu-id="ce8e9-343">RetailTransactionServiceOrders.invoiceSalesOrder</span><span class="sxs-lookup"><span data-stu-id="ce8e9-343">RetailTransactionServiceOrders.invoiceSalesOrder</span></span>|
|<span data-ttu-id="ce8e9-344">RetailTransactionServiceOrders.settleCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="ce8e9-344">RetailTransactionServiceOrders.settleCustomerOrder</span></span>|
|<span data-ttu-id="ce8e9-345">SalesCopying.canClose</span><span class="sxs-lookup"><span data-stu-id="ce8e9-345">SalesCopying.canClose</span></span>|
|<span data-ttu-id="ce8e9-346">SalesCreateOrder.updateDeliveryAddress</span><span class="sxs-lookup"><span data-stu-id="ce8e9-346">SalesCreateOrder.updateDeliveryAddress</span></span>|
|<span data-ttu-id="ce8e9-347">SalesFormLetter.main</span><span class="sxs-lookup"><span data-stu-id="ce8e9-347">SalesFormLetter.main</span></span>|
|<span data-ttu-id="ce8e9-348">SalesFormLetter.mainOnServer</span><span class="sxs-lookup"><span data-stu-id="ce8e9-348">SalesFormLetter.mainOnServer</span></span>|
|<span data-ttu-id="ce8e9-349">SalesFormLetter.reSelect</span><span class="sxs-lookup"><span data-stu-id="ce8e9-349">SalesFormLetter.reSelect</span></span>|
|<span data-ttu-id="ce8e9-350">SalesInvoiceJournalCreateBase.createJournalHeader</span><span class="sxs-lookup"><span data-stu-id="ce8e9-350">SalesInvoiceJournalCreateBase.createJournalHeader</span></span>|
|<span data-ttu-id="ce8e9-351">SalesInvoiceJournalPostBase.postLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-351">SalesInvoiceJournalPostBase.postLine</span></span>|
|<span data-ttu-id="ce8e9-352">SalesInvoiceJournalPostBase.updateInventory</span><span class="sxs-lookup"><span data-stu-id="ce8e9-352">SalesInvoiceJournalPostBase.updateInventory</span></span>|
|<span data-ttu-id="ce8e9-353">SalesLine.createLinesFromTmpFrmVirtual</span><span class="sxs-lookup"><span data-stu-id="ce8e9-353">SalesLine.createLinesFromTmpFrmVirtual</span></span>|
|<span data-ttu-id="ce8e9-354">SalesLine.runPriceDiscPolicyDialog</span><span class="sxs-lookup"><span data-stu-id="ce8e9-354">SalesLine.runPriceDiscPolicyDialog</span></span>|
|<span data-ttu-id="ce8e9-355">SalesLineType_ProjectSales.canBeInvoiced</span><span class="sxs-lookup"><span data-stu-id="ce8e9-355">SalesLineType_ProjectSales.canBeInvoiced</span></span>|
|<span data-ttu-id="ce8e9-356">SalesPurchLine.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="ce8e9-356">SalesPurchLine.setPriceAgreement</span></span>|
|<span data-ttu-id="ce8e9-357">SalesPurchLineInterface.setPriceAgreement</span><span class="sxs-lookup"><span data-stu-id="ce8e9-357">SalesPurchLineInterface.setPriceAgreement</span></span>|
|<span data-ttu-id="ce8e9-358">SalesPurchLineInterface.setPriceDisc</span><span class="sxs-lookup"><span data-stu-id="ce8e9-358">SalesPurchLineInterface.setPriceDisc</span></span>|
|<span data-ttu-id="ce8e9-359">SalesQuotationEditLinesForm メソッド createParmLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-359">SalesQuotationEditLinesForm method createParmLine</span></span>|
|<span data-ttu-id="ce8e9-360">SalesQuotationListPageInteraction.linkActive</span><span class="sxs-lookup"><span data-stu-id="ce8e9-360">SalesQuotationListPageInteraction.linkActive</span></span>|
|<span data-ttu-id="ce8e9-361">SalesQuotationProjLinkWizard.endUpdate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-361">SalesQuotationProjLinkWizard.endUpdate</span></span>|
|<span data-ttu-id="ce8e9-362">SalesQuotationTable.convertCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="ce8e9-362">SalesQuotationTable.convertCurrencyCode</span></span>|
|<span data-ttu-id="ce8e9-363">SalesQuotationTable.modified (SalesQuotationLine_ItemId フォーム コントロール)</span><span class="sxs-lookup"><span data-stu-id="ce8e9-363">SalesQuotationTable.modified (SalesQuotationLine_ItemId form control)</span></span>|
|<span data-ttu-id="ce8e9-364">SalesQuotationTableType.numberSeqFormHandlerQuotationId</span><span class="sxs-lookup"><span data-stu-id="ce8e9-364">SalesQuotationTableType.numberSeqFormHandlerQuotationId</span></span>|
|<span data-ttu-id="ce8e9-365">SalesQuotationTransferToProject.createForecastOnAcc</span><span class="sxs-lookup"><span data-stu-id="ce8e9-365">SalesQuotationTransferToProject.createForecastOnAcc</span></span>|
|<span data-ttu-id="ce8e9-366">SalesQuotationTransferToProject.createProject</span><span class="sxs-lookup"><span data-stu-id="ce8e9-366">SalesQuotationTransferToProject.createProject</span></span>|
|<span data-ttu-id="ce8e9-367">SalesTable.convertCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="ce8e9-367">SalesTable.convertCurrencyCode</span></span>|
|<span data-ttu-id="ce8e9-368">SalesTable.modified</span><span class="sxs-lookup"><span data-stu-id="ce8e9-368">SalesTable.modified</span></span>|
|<span data-ttu-id="ce8e9-369">SalesTable.updateDeliveryAddress</span><span class="sxs-lookup"><span data-stu-id="ce8e9-369">SalesTable.updateDeliveryAddress</span></span>|
|<span data-ttu-id="ce8e9-370">SmaServiceFunctionLine.getFromDialog</span><span class="sxs-lookup"><span data-stu-id="ce8e9-370">SmaServiceFunctionLine.getFromDialog</span></span>|
|<span data-ttu-id="ce8e9-371">smmBusRelTable.updateCustTable</span><span class="sxs-lookup"><span data-stu-id="ce8e9-371">smmBusRelTable.updateCustTable</span></span>|
|<span data-ttu-id="ce8e9-372">smmBusRelTable.updateVendTable</span><span class="sxs-lookup"><span data-stu-id="ce8e9-372">smmBusRelTable.updateVendTable</span></span>|
|<span data-ttu-id="ce8e9-373">SourceDocumentBalanceProvider.calculateEncumberedAmount</span><span class="sxs-lookup"><span data-stu-id="ce8e9-373">SourceDocumentBalanceProvider.calculateEncumberedAmount</span></span>|
|<span data-ttu-id="ce8e9-374">Table/MyAddressBook.xds</span><span class="sxs-lookup"><span data-stu-id="ce8e9-374">Table/MyAddressBook.xds</span></span>|
|<span data-ttu-id="ce8e9-375">Table/TrvExpTrans.update</span><span class="sxs-lookup"><span data-stu-id="ce8e9-375">Table/TrvExpTrans.update</span></span>|
|<span data-ttu-id="ce8e9-376">Tax.allocateInTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-376">Tax.allocateInTaxWorkTrans</span></span>|
|<span data-ttu-id="ce8e9-377">TaxCalculationJournal.saveTaxTransfer</span><span class="sxs-lookup"><span data-stu-id="ce8e9-377">TaxCalculationJournal.saveTaxTransfer</span></span>|
|<span data-ttu-id="ce8e9-378">TaxCashDisc.calcAndInsertTaxes</span><span class="sxs-lookup"><span data-stu-id="ce8e9-378">TaxCashDisc.calcAndInsertTaxes</span></span>|
|<span data-ttu-id="ce8e9-379">TaxData.find</span><span class="sxs-lookup"><span data-stu-id="ce8e9-379">TaxData.find</span></span>|
|<span data-ttu-id="ce8e9-380">TaxInventTransferInvoice_BR.post</span><span class="sxs-lookup"><span data-stu-id="ce8e9-380">TaxInventTransferInvoice_BR.post</span></span>|
|<span data-ttu-id="ce8e9-381">TaxReversePrePayment.calcPostAndInsertTaxes</span><span class="sxs-lookup"><span data-stu-id="ce8e9-381">TaxReversePrePayment.calcPostAndInsertTaxes</span></span>|
|<span data-ttu-id="ce8e9-382">TaxReverseTax.insertTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-382">TaxReverseTax.insertTaxWorkTrans</span></span>|
|<span data-ttu-id="ce8e9-383">TaxReverseTax.newTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-383">TaxReverseTax.newTrans</span></span>|
|<span data-ttu-id="ce8e9-384">TaxSettlement.retailCalcAndInsertTaxes</span><span class="sxs-lookup"><span data-stu-id="ce8e9-384">TaxSettlement.retailCalcAndInsertTaxes</span></span>|
|<span data-ttu-id="ce8e9-385">TaxWithHold.createTaxWithholdTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-385">TaxWithHold.createTaxWithholdTrans</span></span>|
|<span data-ttu-id="ce8e9-386">TaxWithhold.postTaxWithhold</span><span class="sxs-lookup"><span data-stu-id="ce8e9-386">TaxWithhold.postTaxWithhold</span></span>|
|<span data-ttu-id="ce8e9-387">TransactionReversal.updateTaxTrans</span><span class="sxs-lookup"><span data-stu-id="ce8e9-387">TransactionReversal.updateTaxTrans</span></span>|
|<span data-ttu-id="ce8e9-388">TransactionReversal_Vend.reversal</span><span class="sxs-lookup"><span data-stu-id="ce8e9-388">TransactionReversal_Vend.reversal</span></span>|
|<span data-ttu-id="ce8e9-389">TransactionTxt.setKey1</span><span class="sxs-lookup"><span data-stu-id="ce8e9-389">TransactionTxt.setKey1</span></span>|
|<span data-ttu-id="ce8e9-390">TransactionTxt.setKey2</span><span class="sxs-lookup"><span data-stu-id="ce8e9-390">TransactionTxt.setKey2</span></span>|
|<span data-ttu-id="ce8e9-391">TransactionTxt.setKey3</span><span class="sxs-lookup"><span data-stu-id="ce8e9-391">TransactionTxt.setKey3</span></span>|
|<span data-ttu-id="ce8e9-392">TrvExpTrans.insertPerDiemDataLines</span><span class="sxs-lookup"><span data-stu-id="ce8e9-392">TrvExpTrans.insertPerDiemDataLines</span></span>|
|<span data-ttu-id="ce8e9-393">TrvPbsMainDataLines.clicked</span><span class="sxs-lookup"><span data-stu-id="ce8e9-393">TrvPbsMainDataLines.clicked</span></span>|
|<span data-ttu-id="ce8e9-394">TrvPostExpenseHeader.postCustVendTransactions</span><span class="sxs-lookup"><span data-stu-id="ce8e9-394">TrvPostExpenseHeader.postCustVendTransactions</span></span>|
|<span data-ttu-id="ce8e9-395">TSTimesheetTrans.getCostPrice</span><span class="sxs-lookup"><span data-stu-id="ce8e9-395">TSTimesheetTrans.getCostPrice</span></span>|
|<span data-ttu-id="ce8e9-396">VendOutPaym_Cheque.generatePaymentLines</span><span class="sxs-lookup"><span data-stu-id="ce8e9-396">VendOutPaym_Cheque.generatePaymentLines</span></span>|
|<span data-ttu-id="ce8e9-397">VendOutPaym_RBC.generatePaymentLines</span><span class="sxs-lookup"><span data-stu-id="ce8e9-397">VendOutPaym_RBC.generatePaymentLines</span></span>|
|<span data-ttu-id="ce8e9-398">VendOutPaymRecord_RBC_Credit.fillField03</span><span class="sxs-lookup"><span data-stu-id="ce8e9-398">VendOutPaymRecord_RBC_Credit.fillField03</span></span>|
|<span data-ttu-id="ce8e9-399">VendOutPaymRecord_RBC_Credit.fillField07</span><span class="sxs-lookup"><span data-stu-id="ce8e9-399">VendOutPaymRecord_RBC_Credit.fillField07</span></span>|
|<span data-ttu-id="ce8e9-400">WhsControlItemId.populate</span><span class="sxs-lookup"><span data-stu-id="ce8e9-400">WhsControlItemId.populate</span></span>|
|<span data-ttu-id="ce8e9-401">WHSCycleCountCreatePlan.insertWorkLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-401">WHSCycleCountCreatePlan.insertWorkLine</span></span>|
|<span data-ttu-id="ce8e9-402">WHSLoadLineAllocationProcessor.validateBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ce8e9-402">WHSLoadLineAllocationProcessor.validateBatchDisposition</span></span>|
|<span data-ttu-id="ce8e9-403">WhsLoadLineUpdater.initLoadLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-403">WhsLoadLineUpdater.initLoadLine</span></span>|
|<span data-ttu-id="ce8e9-404">WHSMobileAppServiceXMLTranslator.createXML</span><span class="sxs-lookup"><span data-stu-id="ce8e9-404">WHSMobileAppServiceXMLTranslator.createXML</span></span>|
|<span data-ttu-id="ce8e9-405">WHSPack.packFromScanningFields</span><span class="sxs-lookup"><span data-stu-id="ce8e9-405">WHSPack.packFromScanningFields</span></span>|
|<span data-ttu-id="ce8e9-406">WhsrfControlData.allowMixedBatch</span><span class="sxs-lookup"><span data-stu-id="ce8e9-406">WhsrfControlData.allowMixedBatch</span></span>|
|<span data-ttu-id="ce8e9-407">WhsrfControlData.allowMixedItem</span><span class="sxs-lookup"><span data-stu-id="ce8e9-407">WhsrfControlData.allowMixedItem</span></span>|
|<span data-ttu-id="ce8e9-408">WHSRFControlData.processLegacyControl</span><span class="sxs-lookup"><span data-stu-id="ce8e9-408">WHSRFControlData.processLegacyControl</span></span>|
|<span data-ttu-id="ce8e9-409">WhsWorkExecuteDisplay.buildGetVendBatchDetails</span><span class="sxs-lookup"><span data-stu-id="ce8e9-409">WhsWorkExecuteDisplay.buildGetVendBatchDetails</span></span>|
|<span data-ttu-id="ce8e9-410">WHSWorkExecuteDisplay.buildLPControlFromPass</span><span class="sxs-lookup"><span data-stu-id="ce8e9-410">WHSWorkExecuteDisplay.buildLPControlFromPass</span></span>|
|<span data-ttu-id="ce8e9-411">WHSWorkExecuteDisplay.buildPORecTrackingDimensions</span><span class="sxs-lookup"><span data-stu-id="ce8e9-411">WHSWorkExecuteDisplay.buildPORecTrackingDimensions</span></span>|
|<span data-ttu-id="ce8e9-412">WHSWorkExecuteDisplay.buildRemainingReceiptQtyCurrentLPLabel</span><span class="sxs-lookup"><span data-stu-id="ce8e9-412">WHSWorkExecuteDisplay.buildRemainingReceiptQtyCurrentLPLabel</span></span>|
|<span data-ttu-id="ce8e9-413">WHSWorkExecuteDisplay.buildTrackingDimensions</span><span class="sxs-lookup"><span data-stu-id="ce8e9-413">WHSWorkExecuteDisplay.buildTrackingDimensions</span></span>|
|<span data-ttu-id="ce8e9-414">WHSWorkExecuteDisplay.processWorkLine</span><span class="sxs-lookup"><span data-stu-id="ce8e9-414">WHSWorkExecuteDisplay.processWorkLine</span></span>|
|<span data-ttu-id="ce8e9-415">WHSWorkExecuteDisplay.setBatchDetails</span><span class="sxs-lookup"><span data-stu-id="ce8e9-415">WHSWorkExecuteDisplay.setBatchDetails</span></span>|
|<span data-ttu-id="ce8e9-416">WhsWorkExecuteDisplayClusterPicking.clusterCompleted</span><span class="sxs-lookup"><span data-stu-id="ce8e9-416">WhsWorkExecuteDisplayClusterPicking.clusterCompleted</span></span>|
|<span data-ttu-id="ce8e9-417">WhsWorkExecuteDisplayMenu.buildMenu</span><span class="sxs-lookup"><span data-stu-id="ce8e9-417">WhsWorkExecuteDisplayMenu.buildMenu</span></span>|
|<span data-ttu-id="ce8e9-418">WHSWorkExecuteDisplayPOReceiving.displayForm</span><span class="sxs-lookup"><span data-stu-id="ce8e9-418">WHSWorkExecuteDisplayPOReceiving.displayForm</span></span>|
|<span data-ttu-id="ce8e9-419">WHSWorkExecuteDisplayUserDirected.displayForm</span><span class="sxs-lookup"><span data-stu-id="ce8e9-419">WHSWorkExecuteDisplayUserDirected.displayForm</span></span>|
|<span data-ttu-id="ce8e9-420">WhsWorkExecuteDisplayWarehouseTransfer.displayForm</span><span class="sxs-lookup"><span data-stu-id="ce8e9-420">WhsWorkExecuteDisplayWarehouseTransfer.displayForm</span></span>|
|<span data-ttu-id="ce8e9-421">WrkCtrScheduler_Proj.insertOrder</span><span class="sxs-lookup"><span data-stu-id="ce8e9-421">WrkCtrScheduler_Proj.insertOrder</span></span>|


## <a name="other-changes"></a><span data-ttu-id="ce8e9-422">その他の変更</span><span class="sxs-lookup"><span data-stu-id="ce8e9-422">Other changes</span></span>

<span data-ttu-id="ce8e9-423">次の表に、拡張機能に対して行われた追加の変更を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-423">The following table lists additional changes that have been made for extensibility.</span></span>

| <span data-ttu-id="ce8e9-424">計上額</span><span class="sxs-lookup"><span data-stu-id="ce8e9-424">Change</span></span> |
| -------------|
- <span data-ttu-id="ce8e9-425">AppCommon に SysQueryUpdateRecordSet クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-425">Create a SysQueryUpdateRecordSet class in AppCommon.</span></span>
- <span data-ttu-id="ce8e9-426">CW 品目の割合管理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ce8e9-426">Enable percent controlled for a catch weight item.</span></span>


