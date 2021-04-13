---
title: Dynamics 365 for Finance and Operations バージョン 10.0 の拡張機能の変更
description: これのトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0 に実装された拡張機能を一覧します。
author: FrankDahl
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-02-11
ms.dyn365.ops.version: App 10.0
ms.openlocfilehash: c72ca1e19250321a7bbc6cc168a317b56bee0312
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749638"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-100"></a><span data-ttu-id="22acf-103">Dynamics 365 for Finance and Operations バージョン 10.0 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="22acf-103">Extensibility changes in Dynamics 365 for Finance and Operations version 10.0</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="22acf-104">これは、Dynamics 365 for Finance and Operations バージョン 10.0 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="22acf-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations version 10.0.</span></span> <span data-ttu-id="22acf-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="22acf-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="enumerations-made-extensible"></a><span data-ttu-id="22acf-106">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="22acf-106">Enumerations made extensible</span></span>

<span data-ttu-id="22acf-107">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="22acf-107">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="22acf-108">列挙型</span><span class="sxs-lookup"><span data-stu-id="22acf-108">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="22acf-109">AssetAccrualCalendar</span><span class="sxs-lookup"><span data-stu-id="22acf-109">AssetAccrualCalendar</span></span>|
|<span data-ttu-id="22acf-110">AssetYear</span><span class="sxs-lookup"><span data-stu-id="22acf-110">AssetYear</span></span>|
|<span data-ttu-id="22acf-111">BankReconciliationReportType</span><span class="sxs-lookup"><span data-stu-id="22acf-111">BankReconciliationReportType</span></span>|
|<span data-ttu-id="22acf-112">BudgetPlanColumnPeriodLength</span><span class="sxs-lookup"><span data-stu-id="22acf-112">BudgetPlanColumnPeriodLength</span></span>|
|<span data-ttu-id="22acf-113">BudgetPlanHCMReportGroupOption</span><span class="sxs-lookup"><span data-stu-id="22acf-113">BudgetPlanHCMReportGroupOption</span></span>|
|<span data-ttu-id="22acf-114">CurrencyTypeBrief_RU</span><span class="sxs-lookup"><span data-stu-id="22acf-114">CurrencyTypeBrief_RU</span></span>|
|<span data-ttu-id="22acf-115">EInvoiceStatus_IT</span><span class="sxs-lookup"><span data-stu-id="22acf-115">EInvoiceStatus_IT</span></span>|
|<span data-ttu-id="22acf-116">EInvoiceStatus_IT</span><span class="sxs-lookup"><span data-stu-id="22acf-116">EInvoiceStatus_IT</span></span>|
|<span data-ttu-id="22acf-117">HRPAuthorityBasis</span><span class="sxs-lookup"><span data-stu-id="22acf-117">HRPAuthorityBasis</span></span>|
|<span data-ttu-id="22acf-118">HuExchOutflowType</span><span class="sxs-lookup"><span data-stu-id="22acf-118">HuExchOutflowType</span></span>|
|<span data-ttu-id="22acf-119">InventJournalTagStatus</span><span class="sxs-lookup"><span data-stu-id="22acf-119">InventJournalTagStatus</span></span>|
|<span data-ttu-id="22acf-120">InvoiceAssociationType</span><span class="sxs-lookup"><span data-stu-id="22acf-120">InvoiceAssociationType</span></span>|
|<span data-ttu-id="22acf-121">MCRClaimType</span><span class="sxs-lookup"><span data-stu-id="22acf-121">MCRClaimType</span></span>|
|<span data-ttu-id="22acf-122">MCRMerchandisingEventCategory</span><span class="sxs-lookup"><span data-stu-id="22acf-122">MCRMerchandisingEventCategory</span></span>|
|<span data-ttu-id="22acf-123">PaymAttribute</span><span class="sxs-lookup"><span data-stu-id="22acf-123">PaymAttribute</span></span>|
|<span data-ttu-id="22acf-124">PaymProposalReportedBy</span><span class="sxs-lookup"><span data-stu-id="22acf-124">PaymProposalReportedBy</span></span>|
|<span data-ttu-id="22acf-125">PayrollCategory</span><span class="sxs-lookup"><span data-stu-id="22acf-125">PayrollCategory</span></span>|
|<span data-ttu-id="22acf-126">projActualVsBudget</span><span class="sxs-lookup"><span data-stu-id="22acf-126">projActualVsBudget</span></span>|
|<span data-ttu-id="22acf-127">ProjListStateId</span><span class="sxs-lookup"><span data-stu-id="22acf-127">ProjListStateId</span></span>|
|<span data-ttu-id="22acf-128">ProjTransLayout</span><span class="sxs-lookup"><span data-stu-id="22acf-128">ProjTransLayout</span></span>|
|<span data-ttu-id="22acf-129">ProjType</span><span class="sxs-lookup"><span data-stu-id="22acf-129">ProjType</span></span>|
|<span data-ttu-id="22acf-130">RCashCheckContract</span><span class="sxs-lookup"><span data-stu-id="22acf-130">RCashCheckContract</span></span>|
|<span data-ttu-id="22acf-131">RCashDocRepresType</span><span class="sxs-lookup"><span data-stu-id="22acf-131">RCashDocRepresType</span></span>|
|<span data-ttu-id="22acf-132">RCashDocType</span><span class="sxs-lookup"><span data-stu-id="22acf-132">RCashDocType</span></span>|
|<span data-ttu-id="22acf-133">RCashRemainLimitType</span><span class="sxs-lookup"><span data-stu-id="22acf-133">RCashRemainLimitType</span></span>|
|<span data-ttu-id="22acf-134">RCashTableAll</span><span class="sxs-lookup"><span data-stu-id="22acf-134">RCashTableAll</span></span>|
|<span data-ttu-id="22acf-135">RCashTransStatus</span><span class="sxs-lookup"><span data-stu-id="22acf-135">RCashTransStatus</span></span>|
|<span data-ttu-id="22acf-136">SMARelationType</span><span class="sxs-lookup"><span data-stu-id="22acf-136">SMARelationType</span></span>|
|<span data-ttu-id="22acf-137">smmActivityTaskTimeType</span><span class="sxs-lookup"><span data-stu-id="22acf-137">smmActivityTaskTimeType</span></span>|
|<span data-ttu-id="22acf-138">TaxIdType</span><span class="sxs-lookup"><span data-stu-id="22acf-138">TaxIdType</span></span>|
|<span data-ttu-id="22acf-139">TrvAirlineServiceClassEnum</span><span class="sxs-lookup"><span data-stu-id="22acf-139">TrvAirlineServiceClassEnum</span></span>|
|<span data-ttu-id="22acf-140">TrvFieldVisibility</span><span class="sxs-lookup"><span data-stu-id="22acf-140">TrvFieldVisibility</span></span>|
|<span data-ttu-id="22acf-141">TSPeriodFrequency</span><span class="sxs-lookup"><span data-stu-id="22acf-141">TSPeriodFrequency</span></span>|
|<span data-ttu-id="22acf-142">TSPerWeekMth</span><span class="sxs-lookup"><span data-stu-id="22acf-142">TSPerWeekMth</span></span>|
|<span data-ttu-id="22acf-143">VendPaymentValidate</span><span class="sxs-lookup"><span data-stu-id="22acf-143">VendPaymentValidate</span></span>|

## <a name="sql-operations-made-extensible"></a><span data-ttu-id="22acf-144">拡張可能になった SQL 操作</span><span class="sxs-lookup"><span data-stu-id="22acf-144">SQL operations made extensible</span></span>

<span data-ttu-id="22acf-145">これらの SQL 操作は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="22acf-145">These SQL operations have been made extensible in this update.</span></span>

| <span data-ttu-id="22acf-146">操作</span><span class="sxs-lookup"><span data-stu-id="22acf-146">Operation</span></span>|
| --------------- |
|<span data-ttu-id="22acf-147">JmgStampJournalTable.makeLines</span><span class="sxs-lookup"><span data-stu-id="22acf-147">JmgStampJournalTable.makeLines</span></span>|
|<span data-ttu-id="22acf-148">MCRDropShipStatusUpdate_PurchLine.updatePurchDropShipStatusOnRecord</span><span class="sxs-lookup"><span data-stu-id="22acf-148">MCRDropShipStatusUpdate_PurchLine.updatePurchDropShipStatusOnRecord</span></span>|
|<span data-ttu-id="22acf-149">MCRDropShipStatusUpdate_PurchTable.updatePurchDropShipStatusOnRecord</span><span class="sxs-lookup"><span data-stu-id="22acf-149">MCRDropShipStatusUpdate_PurchTable.updatePurchDropShipStatusOnRecord</span></span>|
|<span data-ttu-id="22acf-150">SalesInvoiceJournalCreate.checkDocumentData_PL</span><span class="sxs-lookup"><span data-stu-id="22acf-150">SalesInvoiceJournalCreate.checkDocumentData_PL</span></span>|
|<span data-ttu-id="22acf-151">SalesInvoiceJournalPost.postFailed</span><span class="sxs-lookup"><span data-stu-id="22acf-151">SalesInvoiceJournalPost.postFailed</span></span>|

## <a name="metadata-changes"></a><span data-ttu-id="22acf-152">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="22acf-152">Metadata changes</span></span>

<span data-ttu-id="22acf-153">これらのメタデータの変更は、このアップデートで行われました。</span><span class="sxs-lookup"><span data-stu-id="22acf-153">These metadata changes have been made in this update.</span></span>

| <span data-ttu-id="22acf-154">操作</span><span class="sxs-lookup"><span data-stu-id="22acf-154">Operation</span></span> |
| --------------- |
|<span data-ttu-id="22acf-155">/Data Model/Data Entities/BOMBillOfMaterialsVersionV2Entity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-155">/Data Model/Data Entities/BOMBillOfMaterialsVersionV2Entity.IsPublic</span></span>|
|<span data-ttu-id="22acf-156">/Data Model/Data Entities/InventItemBatchEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-156">/Data Model/Data Entities/InventItemBatchEntity.IsPublic</span></span>|
|<span data-ttu-id="22acf-157">/Data Model/Data Entities/InventProductSpecificOrderSettingsV2Entity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-157">/Data Model/Data Entities/InventProductSpecificOrderSettingsV2Entity.IsPublic</span></span>|
|<span data-ttu-id="22acf-158">/Data Model/Data Entities/InventQualityGroupItemAssignmentEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-158">/Data Model/Data Entities/InventQualityGroupItemAssignmentEntity.IsPublic</span></span>|
|<span data-ttu-id="22acf-159">/Data Model/Data Entities/InventQualityTestGroupEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-159">/Data Model/Data Entities/InventQualityTestGroupEntity.IsPublic</span></span>|
|<span data-ttu-id="22acf-160">/Data Model/Data Entities/ProductionPoolEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-160">/Data Model/Data Entities/ProductionPoolEntity.IsPublic</span></span>|
|<span data-ttu-id="22acf-161">/Data Model/Data Entities/WMSItemArrivalJournalHeaderEntity.IsPublic, PublicCollectionName, PublicEntityName</span><span class="sxs-lookup"><span data-stu-id="22acf-161">/Data Model/Data Entities/WMSItemArrivalJournalHeaderEntity.IsPublic, PublicCollectionName, PublicEntityName</span></span>|
|<span data-ttu-id="22acf-162">/DataModel/Tables/WMSStorageLoadUnitReqTrans.WMSStorageLoadUnitReqTran</span><span class="sxs-lookup"><span data-stu-id="22acf-162">/DataModel/Tables/WMSStorageLoadUnitReqTrans.WMSStorageLoadUnitReqTran</span></span>|
|<span data-ttu-id="22acf-163">DimensionHierarchyType/EnumValue/RDeferrals</span><span class="sxs-lookup"><span data-stu-id="22acf-163">DimensionHierarchyType/EnumValue/RDeferrals</span></span>|
|<span data-ttu-id="22acf-164">AOT/Data Model/Tables/CategoryTable.Create RecId インデックス</span><span class="sxs-lookup"><span data-stu-id="22acf-164">AOT/Data Model/Tables/CategoryTable.Create RecId Index</span></span>|
|<span data-ttu-id="22acf-165">EcoResProductCategoryHierarchyEntity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-165">EcoResProductCategoryHierarchyEntity.Property.IsPublic</span></span>|
|<span data-ttu-id="22acf-166">EcoResProductSpecificUnitOfMeasureConversionEntity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-166">EcoResProductSpecificUnitOfMeasureConversionEntity.Property.IsPublic</span></span>|
|<span data-ttu-id="22acf-167">EcoResReleasedProductVariantExternalCodeEntity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-167">EcoResReleasedProductVariantExternalCodeEntity.Property.IsPublic</span></span>|
|<span data-ttu-id="22acf-168">InventProductSpecificOrderSettingsV2Entity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="22acf-168">InventProductSpecificOrderSettingsV2Entity.Property.IsPublic</span></span>|
|<span data-ttu-id="22acf-169">複数の EDT に "小数点以下の桁数は拡張可能" プロパティ</span><span class="sxs-lookup"><span data-stu-id="22acf-169">"No of Decimals is Extensible" property on several EDTs</span></span>|
|<span data-ttu-id="22acf-170">RetailLoyaltyRewardPoint.Replacement キー</span><span class="sxs-lookup"><span data-stu-id="22acf-170">RetailLoyaltyRewardPoint.Replacement Key</span></span>|
|<span data-ttu-id="22acf-171">Tables/CustTrans/Relations/ThirdPartyBankAccountId.Validate</span><span class="sxs-lookup"><span data-stu-id="22acf-171">Tables/CustTrans/Relations/ThirdPartyBankAccountId.Validate</span></span>|
|<span data-ttu-id="22acf-172">Tables/EInvoicePropertyTable/Relations/EInvoicePropertyTypeTable.RelationshipType</span><span class="sxs-lookup"><span data-stu-id="22acf-172">Tables/EInvoicePropertyTable/Relations/EInvoicePropertyTypeTable.RelationshipType</span></span>|
|<span data-ttu-id="22acf-173">Tables/ResourceSetup.FormRef</span><span class="sxs-lookup"><span data-stu-id="22acf-173">Tables/ResourceSetup.FormRef</span></span>|
|<span data-ttu-id="22acf-174">Tables/WHSTmpWorkExecuteListBoxItems/Fields/Elements.EDT</span><span class="sxs-lookup"><span data-stu-id="22acf-174">Tables/WHSTmpWorkExecuteListBoxItems/Fields/Elements.EDT</span></span>|

## <a name="refactored-methods"></a><span data-ttu-id="22acf-175">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="22acf-175">Refactored methods</span></span>

<span data-ttu-id="22acf-176">これらのメソッドは、拡張性をサポートするためにリファクターされています。</span><span class="sxs-lookup"><span data-stu-id="22acf-176">These methods have been refactored to support extensibility.</span></span>

| <span data-ttu-id="22acf-177">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="22acf-177">Refactored methods</span></span>                                                                             |
|------------------------------------------------------------------------------------------------|
|<span data-ttu-id="22acf-178">AdvancedLedgerEntryLine.setProjInvoiceLineLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="22acf-178">AdvancedLedgerEntryLine.setProjInvoiceLineLedgerDimension</span></span>|
|<span data-ttu-id="22acf-179">AgreementConfirmationDP.getSalesAgreementHeader</span><span class="sxs-lookup"><span data-stu-id="22acf-179">AgreementConfirmationDP.getSalesAgreementHeader</span></span>|
|<span data-ttu-id="22acf-180">AgreementConfirmationDP.getSalesAgreementHeaderHistory</span><span class="sxs-lookup"><span data-stu-id="22acf-180">AgreementConfirmationDP.getSalesAgreementHeaderHistory</span></span>|
|<span data-ttu-id="22acf-181">PurchAutoCreate_Sales.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="22acf-181">PurchAutoCreate_Sales.createPurchLine</span></span>|
|<span data-ttu-id="22acf-182">PurchCreateFromSalesOrder.run</span><span class="sxs-lookup"><span data-stu-id="22acf-182">PurchCreateFromSalesOrder.run</span></span>|
|<span data-ttu-id="22acf-183">InventItemPrice.insert</span><span class="sxs-lookup"><span data-stu-id="22acf-183">InventItemPrice.insert</span></span>|
|<span data-ttu-id="22acf-184">InventJournalTrans.setCostPrice</span><span class="sxs-lookup"><span data-stu-id="22acf-184">InventJournalTrans.setCostPrice</span></span>|
|<span data-ttu-id="22acf-185">PurchLine.initFromReqPO</span><span class="sxs-lookup"><span data-stu-id="22acf-185">PurchLine.initFromReqPO</span></span>|
|<span data-ttu-id="22acf-186">AssetBook.initDepreciationProfile</span><span class="sxs-lookup"><span data-stu-id="22acf-186">AssetBook.initDepreciationProfile</span></span>|
|<span data-ttu-id="22acf-187">AssetDepreciationProfile.validateStraightLine</span><span class="sxs-lookup"><span data-stu-id="22acf-187">AssetDepreciationProfile.validateStraightLine</span></span>|
|<span data-ttu-id="22acf-188">AssetProposalDepreciation.run</span><span class="sxs-lookup"><span data-stu-id="22acf-188">AssetProposalDepreciation.run</span></span>|
|<span data-ttu-id="22acf-189">BankPaymAdvicePrint.BankPaymAdvicePrint (変数)</span><span class="sxs-lookup"><span data-stu-id="22acf-189">BankPaymAdvicePrint.BankPaymAdvicePrint (variable)</span></span>|
|<span data-ttu-id="22acf-190">BankReconciliationMatchingMatchProcessor.constructMatch</span><span class="sxs-lookup"><span data-stu-id="22acf-190">BankReconciliationMatchingMatchProcessor.constructMatch</span></span>|
|<span data-ttu-id="22acf-191">BankReconMatchingMatchStmtReversalDoc.Multiple</span><span class="sxs-lookup"><span data-stu-id="22acf-191">BankReconMatchingMatchStmtReversalDoc.Multiple</span></span>|
|<span data-ttu-id="22acf-192">BankStatementDocumentEntity.postGetStagingData</span><span class="sxs-lookup"><span data-stu-id="22acf-192">BankStatementDocumentEntity.postGetStagingData</span></span>|
|<span data-ttu-id="22acf-193">BankVoucher.post</span><span class="sxs-lookup"><span data-stu-id="22acf-193">BankVoucher.post</span></span>|
|<span data-ttu-id="22acf-194">BomCalcItemLine.mustExplodePrice</span><span class="sxs-lookup"><span data-stu-id="22acf-194">BomCalcItemLine.mustExplodePrice</span></span>|
|<span data-ttu-id="22acf-195">BOMCopyToProd.delete</span><span class="sxs-lookup"><span data-stu-id="22acf-195">BOMCopyToProd.delete</span></span>|
|<span data-ttu-id="22acf-196">BOMCreateDialog.promptCreateBOMDialog</span><span class="sxs-lookup"><span data-stu-id="22acf-196">BOMCreateDialog.promptCreateBOMDialog</span></span>|
|<span data-ttu-id="22acf-197">BomRouteCopyJob.initFromItemId</span><span class="sxs-lookup"><span data-stu-id="22acf-197">BomRouteCopyJob.initFromItemId</span></span>|
|<span data-ttu-id="22acf-198">BudgetPlanningConfiguration.displayYearOffset</span><span class="sxs-lookup"><span data-stu-id="22acf-198">BudgetPlanningConfiguration.displayYearOffset</span></span>|
|<span data-ttu-id="22acf-199">BudgetPlanningConfiguration.updateColumnPeriodLengthValueLabel</span><span class="sxs-lookup"><span data-stu-id="22acf-199">BudgetPlanningConfiguration.updateColumnPeriodLengthValueLabel</span></span>|
|<span data-ttu-id="22acf-200">CatVendorCatalogProductApproval.getApprovedProductForRetail</span><span class="sxs-lookup"><span data-stu-id="22acf-200">CatVendorCatalogProductApproval.getApprovedProductForRetail</span></span>|
|<span data-ttu-id="22acf-201">LedgerJournalTransType.validateAccountType</span><span class="sxs-lookup"><span data-stu-id="22acf-201">LedgerJournalTransType.validateAccountType</span></span>|
|<span data-ttu-id="22acf-202">LedgerTransferOpening.processQuery</span><span class="sxs-lookup"><span data-stu-id="22acf-202">LedgerTransferOpening.processQuery</span></span>|
|<span data-ttu-id="22acf-203">BankPositivePayExport.generatePositivePayFile</span><span class="sxs-lookup"><span data-stu-id="22acf-203">BankPositivePayExport.generatePositivePayFile</span></span>|
|<span data-ttu-id="22acf-204">BankPositivePayExport.updateBankPositivePay</span><span class="sxs-lookup"><span data-stu-id="22acf-204">BankPositivePayExport.updateBankPositivePay</span></span>|
|<span data-ttu-id="22acf-205">CaseSendEmail.getEmailMessage</span><span class="sxs-lookup"><span data-stu-id="22acf-205">CaseSendEmail.getEmailMessage</span></span>|
|<span data-ttu-id="22acf-206">ContactPerson.insert</span><span class="sxs-lookup"><span data-stu-id="22acf-206">ContactPerson.insert</span></span>|
|<span data-ttu-id="22acf-207">CostSheetModeStrategyStaging.createCostSheetNodes</span><span class="sxs-lookup"><span data-stu-id="22acf-207">CostSheetModeStrategyStaging.createCostSheetNodes</span></span>|
|<span data-ttu-id="22acf-208">CreditCard.recordAuthorization</span><span class="sxs-lookup"><span data-stu-id="22acf-208">CreditCard.recordAuthorization</span></span>|
|<span data-ttu-id="22acf-209">CreditCard.recordCapture</span><span class="sxs-lookup"><span data-stu-id="22acf-209">CreditCard.recordCapture</span></span>|
|<span data-ttu-id="22acf-210">CreditCardPaymentJournal.createJournal</span><span class="sxs-lookup"><span data-stu-id="22acf-210">CreditCardPaymentJournal.createJournal</span></span>|
|<span data-ttu-id="22acf-211">CreditCardPaymentJournal.Init</span><span class="sxs-lookup"><span data-stu-id="22acf-211">CreditCardPaymentJournal.Init</span></span>|
|<span data-ttu-id="22acf-212">CreditCardPaymentJournal.run</span><span class="sxs-lookup"><span data-stu-id="22acf-212">CreditCardPaymentJournal.run</span></span>|
|<span data-ttu-id="22acf-213">CustAgingReportContract.Validate</span><span class="sxs-lookup"><span data-stu-id="22acf-213">CustAgingReportContract.Validate</span></span>|
|<span data-ttu-id="22acf-214">CustAgingReportDP.CustAgingReportTmp</span><span class="sxs-lookup"><span data-stu-id="22acf-214">CustAgingReportDP.CustAgingReportTmp</span></span>|
|<span data-ttu-id="22acf-215">CustAgingReportDPclass.insertCustAgingReportTmp</span><span class="sxs-lookup"><span data-stu-id="22acf-215">CustAgingReportDPclass.insertCustAgingReportTmp</span></span>|
|<span data-ttu-id="22acf-216">CustAgingReportDPclass.setCustAgingReportTmpInReverse</span><span class="sxs-lookup"><span data-stu-id="22acf-216">CustAgingReportDPclass.setCustAgingReportTmpInReverse</span></span>|
|<span data-ttu-id="22acf-217">CustBalanceList.insertIntoTmpAccountSumV2</span><span class="sxs-lookup"><span data-stu-id="22acf-217">CustBalanceList.insertIntoTmpAccountSumV2</span></span>|
|<span data-ttu-id="22acf-218">CustBillOfExchangePostRemit.postSettlingStep</span><span class="sxs-lookup"><span data-stu-id="22acf-218">CustBillOfExchangePostRemit.postSettlingStep</span></span>|
|<span data-ttu-id="22acf-219">CustCollectionsSetTransactionStatusHelper.createActions</span><span class="sxs-lookup"><span data-stu-id="22acf-219">CustCollectionsSetTransactionStatusHelper.createActions</span></span>|
|<span data-ttu-id="22acf-220">CustCustomerBaseEntity/CustCustomerEntity/CustCustomerV2Entity/CustCustomerV3Entity.processChangesForApproval</span><span class="sxs-lookup"><span data-stu-id="22acf-220">CustCustomerBaseEntity/CustCustomerEntity/CustCustomerV2Entity/CustCustomerV3Entity.processChangesForApproval</span></span>|
|<span data-ttu-id="22acf-221">CustCustomerDetailEntity/CustCustomerDetailV2Entity.processChangesForApproval</span><span class="sxs-lookup"><span data-stu-id="22acf-221">CustCustomerDetailEntity/CustCustomerDetailV2Entity.processChangesForApproval</span></span>|
|<span data-ttu-id="22acf-222">CustInvoiceJour.setInvoiceAddress</span><span class="sxs-lookup"><span data-stu-id="22acf-222">CustInvoiceJour.setInvoiceAddress</span></span>|
|<span data-ttu-id="22acf-223">CustInvoiceLine.getCustBillingCodeLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="22acf-223">CustInvoiceLine.getCustBillingCodeLedgerAccount</span></span>|
|<span data-ttu-id="22acf-224">CustInvoiceLine.setProjInvoiceLineLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="22acf-224">CustInvoiceLine.setProjInvoiceLineLedgerDimension</span></span>|
|<span data-ttu-id="22acf-225">CustInvoiceLine.setProjInvoiceLineLedgerDimensionBase</span><span class="sxs-lookup"><span data-stu-id="22acf-225">CustInvoiceLine.setProjInvoiceLineLedgerDimensionBase</span></span>|
|<span data-ttu-id="22acf-226">CustInvoiceLine.shouldDefaultLedgerDimensionFromProject</span><span class="sxs-lookup"><span data-stu-id="22acf-226">CustInvoiceLine.shouldDefaultLedgerDimensionFromProject</span></span>|
|<span data-ttu-id="22acf-227">CustOutPaymRecord_Cheque.checkValues</span><span class="sxs-lookup"><span data-stu-id="22acf-227">CustOutPaymRecord_Cheque.checkValues</span></span>|
|<span data-ttu-id="22acf-228">CustPostInvoiceJob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="22acf-228">CustPostInvoiceJob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="22acf-229">CustVendAgingCalculation.process</span><span class="sxs-lookup"><span data-stu-id="22acf-229">CustVendAgingCalculation.process</span></span>|
|<span data-ttu-id="22acf-230">CustVendChequeSlipTextCalculator.getChequeDocLength</span><span class="sxs-lookup"><span data-stu-id="22acf-230">CustVendChequeSlipTextCalculator.getChequeDocLength</span></span>|
|<span data-ttu-id="22acf-231">CustVendChequeSlipTextCalculator.getMinimumSlipLines</span><span class="sxs-lookup"><span data-stu-id="22acf-231">CustVendChequeSlipTextCalculator.getMinimumSlipLines</span></span>|
|<span data-ttu-id="22acf-232">CustVendChequeSlipTextCalculator.fillSlipText</span><span class="sxs-lookup"><span data-stu-id="22acf-232">CustVendChequeSlipTextCalculator.fillSlipText</span></span>|
|<span data-ttu-id="22acf-233">CustVendChequeSlipTextCalculator.Property</span><span class="sxs-lookup"><span data-stu-id="22acf-233">CustVendChequeSlipTextCalculator.Property</span></span> |
|<span data-ttu-id="22acf-234">CustVendEditTaxBranch_TH.init</span><span class="sxs-lookup"><span data-stu-id="22acf-234">CustVendEditTaxBranch_TH.init</span></span>|
|<span data-ttu-id="22acf-235">CustVendOutPaym.getSumByCurrency</span><span class="sxs-lookup"><span data-stu-id="22acf-235">CustVendOutPaym.getSumByCurrency</span></span>|
|<span data-ttu-id="22acf-236">CustVendPaymInvoiceWithJournal.createJournal</span><span class="sxs-lookup"><span data-stu-id="22acf-236">CustVendPaymInvoiceWithJournal.createJournal</span></span>|
|<span data-ttu-id="22acf-237">CustVendPaymInvoiceWithJournal.createPayment</span><span class="sxs-lookup"><span data-stu-id="22acf-237">CustVendPaymInvoiceWithJournal.createPayment</span></span>|
|<span data-ttu-id="22acf-238">CustVendPaymProposal.resolvePaymAccountAndType</span><span class="sxs-lookup"><span data-stu-id="22acf-238">CustVendPaymProposal.resolvePaymAccountAndType</span></span>|
|<span data-ttu-id="22acf-239">CustVendPaymProposalLine.paymTransactionAmountMST</span><span class="sxs-lookup"><span data-stu-id="22acf-239">CustVendPaymProposalLine.paymTransactionAmountMST</span></span>|
|<span data-ttu-id="22acf-240">CustVendPaymProposalTransferToJournal.getVoucherNum</span><span class="sxs-lookup"><span data-stu-id="22acf-240">CustVendPaymProposalTransferToJournal.getVoucherNum</span></span>|
|<span data-ttu-id="22acf-241">CustVendReversePosting.restoreCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="22acf-241">CustVendReversePosting.restoreCustVendTransOpen</span></span>|
|<span data-ttu-id="22acf-242">CustVendSettle.postDueToAndFromCreateTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-242">CustVendSettle.postDueToAndFromCreateTrans</span></span>|
|<span data-ttu-id="22acf-243">CustVendSettle.postExchRateLedgerTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-243">CustVendSettle.postExchRateLedgerTrans</span></span>|
|<span data-ttu-id="22acf-244">CustVendSettle.settleNow</span><span class="sxs-lookup"><span data-stu-id="22acf-244">CustVendSettle.settleNow</span></span>|
|<span data-ttu-id="22acf-245">CustVendSettle.updateCustTaxInvoice_TH</span><span class="sxs-lookup"><span data-stu-id="22acf-245">CustVendSettle.updateCustTaxInvoice_TH</span></span>|
|<span data-ttu-id="22acf-246">CustVendSumUpJournal.createTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-246">CustVendSumUpJournal.createTrans</span></span>|
|<span data-ttu-id="22acf-247">CustVendSumUpJournal.createVoucher</span><span class="sxs-lookup"><span data-stu-id="22acf-247">CustVendSumUpJournal.createVoucher</span></span>|
|<span data-ttu-id="22acf-248">CustVendTransreorg.end</span><span class="sxs-lookup"><span data-stu-id="22acf-248">CustVendTransreorg.end</span></span>|
|<span data-ttu-id="22acf-249">CustVoucher.updateProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="22acf-249">CustVoucher.updateProjTransPosting</span></span>|
|<span data-ttu-id="22acf-250">DimDerDistRuleProjectRevenueExt.processRegularTransactions</span><span class="sxs-lookup"><span data-stu-id="22acf-250">DimDerDistRuleProjectRevenueExt.processRegularTransactions</span></span>|
|<span data-ttu-id="22acf-251">DimDerDistRuleProjectRevenueExt.processIntercompanyTransCustInvoice</span><span class="sxs-lookup"><span data-stu-id="22acf-251">DimDerDistRuleProjectRevenueExt.processIntercompanyTransCustInvoice</span></span>|
|<span data-ttu-id="22acf-252">DimDerDistRuleProjectRevenueExt.processIntercompanyTransExpense</span><span class="sxs-lookup"><span data-stu-id="22acf-252">DimDerDistRuleProjectRevenueExt.processIntercompanyTransExpense</span></span>|
|<span data-ttu-id="22acf-253">DimDerDistRuleProjectRevenueExt.processIntercompanyTransTimesheet</span><span class="sxs-lookup"><span data-stu-id="22acf-253">DimDerDistRuleProjectRevenueExt.processIntercompanyTransTimesheet</span></span>|
|<span data-ttu-id="22acf-254">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span><span class="sxs-lookup"><span data-stu-id="22acf-254">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span></span>|
|<span data-ttu-id="22acf-255">EcoResEnumerationAttributeTypeValue.createAttributeValuesFromEnum</span><span class="sxs-lookup"><span data-stu-id="22acf-255">EcoResEnumerationAttributeTypeValue.createAttributeValuesFromEnum</span></span>|
|<span data-ttu-id="22acf-256">EcoResProductReleaseForm.addProductsToRelease</span><span class="sxs-lookup"><span data-stu-id="22acf-256">EcoResProductReleaseForm.addProductsToRelease</span></span>|
|<span data-ttu-id="22acf-257">EInvoice_IT.newCustInvoice</span><span class="sxs-lookup"><span data-stu-id="22acf-257">EInvoice_IT.newCustInvoice</span></span>|
|<span data-ttu-id="22acf-258">EInvoice_IT.newProjInvoice</span><span class="sxs-lookup"><span data-stu-id="22acf-258">EInvoice_IT.newProjInvoice</span></span>|
|<span data-ttu-id="22acf-259">EUSalesListReportingEngine.Construct</span><span class="sxs-lookup"><span data-stu-id="22acf-259">EUSalesListReportingEngine.Construct</span></span>|
|<span data-ttu-id="22acf-260">FiscalDocument_BR.lastIssueDateForSeries</span><span class="sxs-lookup"><span data-stu-id="22acf-260">FiscalDocument_BR.lastIssueDateForSeries</span></span>|
|<span data-ttu-id="22acf-261">FormletterJournalPost.docuRefCopyByRecId</span><span class="sxs-lookup"><span data-stu-id="22acf-261">FormletterJournalPost.docuRefCopyByRecId</span></span>|
|<span data-ttu-id="22acf-262">ForecastSales.Update</span><span class="sxs-lookup"><span data-stu-id="22acf-262">ForecastSales.Update</span></span>|
|<span data-ttu-id="22acf-263">HcmActionState.lookupReferenceActionTypeSetup</span><span class="sxs-lookup"><span data-stu-id="22acf-263">HcmActionState.lookupReferenceActionTypeSetup</span></span>|
|<span data-ttu-id="22acf-264">HcmWorker.init</span><span class="sxs-lookup"><span data-stu-id="22acf-264">HcmWorker.init</span></span>|
|<span data-ttu-id="22acf-265">HcmWorker.updateEmploymentControls</span><span class="sxs-lookup"><span data-stu-id="22acf-265">HcmWorker.updateEmploymentControls</span></span>|
|<span data-ttu-id="22acf-266">HcmWorkerActionHireCompletion.getHrmApplication</span><span class="sxs-lookup"><span data-stu-id="22acf-266">HcmWorkerActionHireCompletion.getHrmApplication</span></span>|
|<span data-ttu-id="22acf-267">HcmWorkerTransition.createHcmEmployment</span><span class="sxs-lookup"><span data-stu-id="22acf-267">HcmWorkerTransition.createHcmEmployment</span></span>|
|<span data-ttu-id="22acf-268">HRCCompGridView.initCompRecord</span><span class="sxs-lookup"><span data-stu-id="22acf-268">HRCCompGridView.initCompRecord</span></span>|
|<span data-ttu-id="22acf-269">HRMCompFixedEmpl.enforcePayRateTolerance</span><span class="sxs-lookup"><span data-stu-id="22acf-269">HRMCompFixedEmpl.enforcePayRateTolerance</span></span>|
|<span data-ttu-id="22acf-270">HRPDefaultSigningLimitRule.insertFormDataSourceJobDetail</span><span class="sxs-lookup"><span data-stu-id="22acf-270">HRPDefaultSigningLimitRule.insertFormDataSourceJobDetail</span></span>|
|<span data-ttu-id="22acf-271">HRPDefaultSigningLimitRule.populateDetailGrid</span><span class="sxs-lookup"><span data-stu-id="22acf-271">HRPDefaultSigningLimitRule.populateDetailGrid</span></span>|
|<span data-ttu-id="22acf-272">HRPDefaultSigningLimitRule.SaveValidation</span><span class="sxs-lookup"><span data-stu-id="22acf-272">HRPDefaultSigningLimitRule.SaveValidation</span></span>|
|<span data-ttu-id="22acf-273">HRPDefaultSigningLimitRule.insertOrUpdateFormDataSource</span><span class="sxs-lookup"><span data-stu-id="22acf-273">HRPDefaultSigningLimitRule.insertOrUpdateFormDataSource</span></span>|
|<span data-ttu-id="22acf-274">HRPDefaultSigningLimitRuleCompensation.getSelectedCompensation</span><span class="sxs-lookup"><span data-stu-id="22acf-274">HRPDefaultSigningLimitRuleCompensation.getSelectedCompensation</span></span>|
|<span data-ttu-id="22acf-275">HRPDefaultSigningLimitRuleCompensation.getAvailableCompensation</span><span class="sxs-lookup"><span data-stu-id="22acf-275">HRPDefaultSigningLimitRuleCompensation.getAvailableCompensation</span></span>|
|<span data-ttu-id="22acf-276">HRPDefaultSigningLimitRuleCompensation.selectRecords</span><span class="sxs-lookup"><span data-stu-id="22acf-276">HRPDefaultSigningLimitRuleCompensation.selectRecords</span></span>|
|<span data-ttu-id="22acf-277">HRPDefaultSigningLimitRuleCompensation.unselectRecords</span><span class="sxs-lookup"><span data-stu-id="22acf-277">HRPDefaultSigningLimitRuleCompensation.unselectRecords</span></span>|
|<span data-ttu-id="22acf-278">HrpWorkerLimit.getActiveDefaultSLRule,</span><span class="sxs-lookup"><span data-stu-id="22acf-278">HrpWorkerLimit.getActiveDefaultSLRule,</span></span> |
|<span data-ttu-id="22acf-279">HrpWorkerLimit.getDefaultSigningLimits</span><span class="sxs-lookup"><span data-stu-id="22acf-279">HrpWorkerLimit.getDefaultSigningLimits</span></span>|
|<span data-ttu-id="22acf-280">HrpWorkerLimit.getWorkerSigningLimit</span><span class="sxs-lookup"><span data-stu-id="22acf-280">HrpWorkerLimit.getWorkerSigningLimit</span></span>|
|<span data-ttu-id="22acf-281">HrpWorkerLimitr.getSigningLimitsIfRequestNotRequired</span><span class="sxs-lookup"><span data-stu-id="22acf-281">HrpWorkerLimitr.getSigningLimitsIfRequestNotRequired</span></span>|
|<span data-ttu-id="22acf-282">InterCompanyTransferInventDim.Entire クラス</span><span class="sxs-lookup"><span data-stu-id="22acf-282">InterCompanyTransferInventDim.Entire class</span></span>|
|<span data-ttu-id="22acf-283">InterCompanyTransferInventDim.transfer</span><span class="sxs-lookup"><span data-stu-id="22acf-283">InterCompanyTransferInventDim.transfer</span></span>|
|<span data-ttu-id="22acf-284">InventBatch.update</span><span class="sxs-lookup"><span data-stu-id="22acf-284">InventBatch.update</span></span>|
|<span data-ttu-id="22acf-285">InventCountCreate_Base.createInventJournalTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-285">InventCountCreate_Base.createInventJournalTrans</span></span>|
|<span data-ttu-id="22acf-286">InventInventoryDimensionEntityFieldsMapping.resolveInventDim</span><span class="sxs-lookup"><span data-stu-id="22acf-286">InventInventoryDimensionEntityFieldsMapping.resolveInventDim</span></span>|
|<span data-ttu-id="22acf-287">InventMov_Jour_BOM.journalCheckTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-287">InventMov_Jour_BOM.journalCheckTrans</span></span>|
|<span data-ttu-id="22acf-288">InventMov_Jour_Loss_Project.checkAccountOperations</span><span class="sxs-lookup"><span data-stu-id="22acf-288">InventMov_Jour_Loss_Project.checkAccountOperations</span></span>|
|<span data-ttu-id="22acf-289">InventMov_Journal.journalSetItemId</span><span class="sxs-lookup"><span data-stu-id="22acf-289">InventMov_Journal.journalSetItemId</span></span>|
|<span data-ttu-id="22acf-290">InventMov_Statement.pdsCWRemainPhysical</span><span class="sxs-lookup"><span data-stu-id="22acf-290">InventMov_Statement.pdsCWRemainPhysical</span></span>|
|<span data-ttu-id="22acf-291">InventMovement.performFinancialLedgerUpdate</span><span class="sxs-lookup"><span data-stu-id="22acf-291">InventMovement.performFinancialLedgerUpdate</span></span>|
|<span data-ttu-id="22acf-292">InventProcessGuideAdjustInController.initialStepName</span><span class="sxs-lookup"><span data-stu-id="22acf-292">InventProcessGuideAdjustInController.initialStepName</span></span>|
|<span data-ttu-id="22acf-293">InventQualityManagementBlock.run</span><span class="sxs-lookup"><span data-stu-id="22acf-293">InventQualityManagementBlock.run</span></span>|
|<span data-ttu-id="22acf-294">InventQualityManagementCreateHandler.purchFormLetterBeforeHelper</span><span class="sxs-lookup"><span data-stu-id="22acf-294">InventQualityManagementCreateHandler.purchFormLetterBeforeHelper</span></span>|
|<span data-ttu-id="22acf-295">InventQualityOrderTableValidator.checkQty</span><span class="sxs-lookup"><span data-stu-id="22acf-295">InventQualityOrderTableValidator.checkQty</span></span>|
|<span data-ttu-id="22acf-296">InventSum.retrieveMatchingInventSumDeltaForTTSId()</span><span class="sxs-lookup"><span data-stu-id="22acf-296">InventSum.retrieveMatchingInventSumDeltaForTTSId()</span></span>|
|<span data-ttu-id="22acf-297">InventTrackingRegisterTransForm.construct</span><span class="sxs-lookup"><span data-stu-id="22acf-297">InventTrackingRegisterTransForm.construct</span></span>|
|<span data-ttu-id="22acf-298">InventTransAdjust.updateNow</span><span class="sxs-lookup"><span data-stu-id="22acf-298">InventTransAdjust.updateNow</span></span>|
|<span data-ttu-id="22acf-299">InventTransferUpdReceive.updateInventTransferLine</span><span class="sxs-lookup"><span data-stu-id="22acf-299">InventTransferUpdReceive.updateInventTransferLine</span></span>|
|<span data-ttu-id="22acf-300">InventTransWms_Register.updateInventFromMovementServer</span><span class="sxs-lookup"><span data-stu-id="22acf-300">InventTransWms_Register.updateInventFromMovementServer</span></span>|
|<span data-ttu-id="22acf-301">InventUpd_ChildReference updateLess\* メソッド</span><span class="sxs-lookup"><span data-stu-id="22acf-301">InventUpd_ChildReference updateLess\* methods</span></span>|
|<span data-ttu-id="22acf-302">InventUpd_ChildReference.updateMoreIssue</span><span class="sxs-lookup"><span data-stu-id="22acf-302">InventUpd_ChildReference.updateMoreIssue</span></span>|
|<span data-ttu-id="22acf-303">InventUpd_Estimated.updateAutoDimMovement</span><span class="sxs-lookup"><span data-stu-id="22acf-303">InventUpd_Estimated.updateAutoDimMovement</span></span>|
|<span data-ttu-id="22acf-304">InventUpd_Physical.UpdatePhysicalReturnedIssue</span><span class="sxs-lookup"><span data-stu-id="22acf-304">InventUpd_Physical.UpdatePhysicalReturnedIssue</span></span>|
|<span data-ttu-id="22acf-305">InventUpd_Physical.updatePhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="22acf-305">InventUpd_Physical.updatePhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="22acf-306">InventUpd_WHSReservation.continueInventTransUpdateReserveMoveLoop</span><span class="sxs-lookup"><span data-stu-id="22acf-306">InventUpd_WHSReservation.continueInventTransUpdateReserveMoveLoop</span></span>|
|<span data-ttu-id="22acf-307">InventUpdateOnhand.checkOnhand()</span><span class="sxs-lookup"><span data-stu-id="22acf-307">InventUpdateOnhand.checkOnhand()</span></span>|
|<span data-ttu-id="22acf-308">InventUpdateReserveMore.buildQueries</span><span class="sxs-lookup"><span data-stu-id="22acf-308">InventUpdateReserveMore.buildQueries</span></span>|
|<span data-ttu-id="22acf-309">JmgMESDocuHandling.openFile</span><span class="sxs-lookup"><span data-stu-id="22acf-309">JmgMESDocuHandling.openFile</span></span>|
|<span data-ttu-id="22acf-310">JmgProfiles.insertTimeGapsPlannedAbs</span><span class="sxs-lookup"><span data-stu-id="22acf-310">JmgProfiles.insertTimeGapsPlannedAbs</span></span>|
|<span data-ttu-id="22acf-311">JmgStampJournalCalculate.run</span><span class="sxs-lookup"><span data-stu-id="22acf-311">JmgStampJournalCalculate.run</span></span>|
|<span data-ttu-id="22acf-312">JmgStampJournalTransfer.cancelExecute</span><span class="sxs-lookup"><span data-stu-id="22acf-312">JmgStampJournalTransfer.cancelExecute</span></span>|
|<span data-ttu-id="22acf-313">JmgStampJournalTransfer.cancelExecute</span><span class="sxs-lookup"><span data-stu-id="22acf-313">JmgStampJournalTransfer.cancelExecute</span></span>|
|<span data-ttu-id="22acf-314">LeanCost_Init.execute</span><span class="sxs-lookup"><span data-stu-id="22acf-314">LeanCost_Init.execute</span></span>|
|<span data-ttu-id="22acf-315">LedgerAllocationController.allocateAmounts</span><span class="sxs-lookup"><span data-stu-id="22acf-315">LedgerAllocationController.allocateAmounts</span></span>|
|<span data-ttu-id="22acf-316">LedgerAllocationProcessRequest.createVoucherDestinations</span><span class="sxs-lookup"><span data-stu-id="22acf-316">LedgerAllocationProcessRequest.createVoucherDestinations</span></span>|
|<span data-ttu-id="22acf-317">LedgerJournalCheckPost.replaceTmpVoucher</span><span class="sxs-lookup"><span data-stu-id="22acf-317">LedgerJournalCheckPost.replaceTmpVoucher</span></span>|
|<span data-ttu-id="22acf-318">LedgerJournalDeleteTransaction.deleteLedgerJournalTransRelated</span><span class="sxs-lookup"><span data-stu-id="22acf-318">LedgerJournalDeleteTransaction.deleteLedgerJournalTransRelated</span></span>|
|<span data-ttu-id="22acf-319">LedgerJournalEngine.currencyModified</span><span class="sxs-lookup"><span data-stu-id="22acf-319">LedgerJournalEngine.currencyModified</span></span>|
|<span data-ttu-id="22acf-320">LedgerJournalPeriodicCopy.journalVoucherCopy</span><span class="sxs-lookup"><span data-stu-id="22acf-320">LedgerJournalPeriodicCopy.journalVoucherCopy</span></span>|
|<span data-ttu-id="22acf-321">LedgerJournalTrans.initForCurrency</span><span class="sxs-lookup"><span data-stu-id="22acf-321">LedgerJournalTrans.initForCurrency</span></span>|
|<span data-ttu-id="22acf-322">LedgerJournalTrans.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="22acf-322">LedgerJournalTrans.validateWrite_Server</span></span>|
|<span data-ttu-id="22acf-323">LedgerTransModule.insertTransactionList</span><span class="sxs-lookup"><span data-stu-id="22acf-323">LedgerTransModule.insertTransactionList</span></span>|
|<span data-ttu-id="22acf-324">LedgerTrialBalanceContract.DataMemberAttribute</span><span class="sxs-lookup"><span data-stu-id="22acf-324">LedgerTrialBalanceContract.DataMemberAttribute</span></span>|
|<span data-ttu-id="22acf-325">LedgerVoucherObject.allocateTransaction</span><span class="sxs-lookup"><span data-stu-id="22acf-325">LedgerVoucherObject.allocateTransaction</span></span>|
|<span data-ttu-id="22acf-326">LedgerAllocationController.allocateRecursive</span><span class="sxs-lookup"><span data-stu-id="22acf-326">LedgerAllocationController.allocateRecursive</span></span>|
|<span data-ttu-id="22acf-327">MCRCheckHoldWB\Release.clicked</span><span class="sxs-lookup"><span data-stu-id="22acf-327">MCRCheckHoldWB\Release.clicked</span></span>|
|<span data-ttu-id="22acf-328">MCROrderEventSetup.find</span><span class="sxs-lookup"><span data-stu-id="22acf-328">MCROrderEventSetup.find</span></span>|
|<span data-ttu-id="22acf-329">MCRSalesOrderRecap.Control:SubmitButton.clicked</span><span class="sxs-lookup"><span data-stu-id="22acf-329">MCRSalesOrderRecap.Control:SubmitButton.clicked</span></span>|
|<span data-ttu-id="22acf-330">MCRSalesQuickQuote.Modified</span><span class="sxs-lookup"><span data-stu-id="22acf-330">MCRSalesQuickQuote.Modified</span></span>|
|<span data-ttu-id="22acf-331">MCRTmpPickingWorkbenchTrans.initFromSessionCriteria</span><span class="sxs-lookup"><span data-stu-id="22acf-331">MCRTmpPickingWorkbenchTrans.initFromSessionCriteria</span></span>|
|<span data-ttu-id="22acf-332">MultilineString.POSDeveloperSupport</span><span class="sxs-lookup"><span data-stu-id="22acf-332">MultilineString.POSDeveloperSupport</span></span>|
|<span data-ttu-id="22acf-333">OriginalDocuments.insertDocument</span><span class="sxs-lookup"><span data-stu-id="22acf-333">OriginalDocuments.insertDocument</span></span>|
|<span data-ttu-id="22acf-334">PaymSchedCalc_Amount.createTransaction</span><span class="sxs-lookup"><span data-stu-id="22acf-334">PaymSchedCalc_Amount.createTransaction</span></span>|
|<span data-ttu-id="22acf-335">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim</span><span class="sxs-lookup"><span data-stu-id="22acf-335">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim</span></span>|
|<span data-ttu-id="22acf-336">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim()</span><span class="sxs-lookup"><span data-stu-id="22acf-336">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim()</span></span>|
|<span data-ttu-id="22acf-337">PdsRebatePaymentPost.insertRebateEntryForGrouping</span><span class="sxs-lookup"><span data-stu-id="22acf-337">PdsRebatePaymentPost.insertRebateEntryForGrouping</span></span>|
|<span data-ttu-id="22acf-338">PmfFormCtrl_BOM_BOMVersion.modifiedFormulaSize</span><span class="sxs-lookup"><span data-stu-id="22acf-338">PmfFormCtrl_BOM_BOMVersion.modifiedFormulaSize</span></span>|
|<span data-ttu-id="22acf-339">PriceDiscAdmCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="22acf-339">PriceDiscAdmCheckPost.postJournal</span></span>|
|<span data-ttu-id="22acf-340">ProdJournalCheckPostProd.postTransLedger</span><span class="sxs-lookup"><span data-stu-id="22acf-340">ProdJournalCheckPostProd.postTransLedger</span></span>|
|<span data-ttu-id="22acf-341">ProdJournalTransBOM.inventBatchId.validate</span><span class="sxs-lookup"><span data-stu-id="22acf-341">ProdJournalTransBOM.inventBatchId.validate</span></span>|
|<span data-ttu-id="22acf-342">ProdMultiReportFinished.insert</span><span class="sxs-lookup"><span data-stu-id="22acf-342">ProdMultiReportFinished.insert</span></span>|
|<span data-ttu-id="22acf-343">ProdUPDCostEstimation.CreateProdBOM</span><span class="sxs-lookup"><span data-stu-id="22acf-343">ProdUPDCostEstimation.CreateProdBOM</span></span>|
|<span data-ttu-id="22acf-344">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="22acf-344">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="22acf-345">ProdUpdStartUp.createJournals</span><span class="sxs-lookup"><span data-stu-id="22acf-345">ProdUpdStartUp.createJournals</span></span>|
|<span data-ttu-id="22acf-346">ProjBegBalJournalTrans_CostSales.validateField, validateWrite</span><span class="sxs-lookup"><span data-stu-id="22acf-346">ProjBegBalJournalTrans_CostSales.validateField, validateWrite</span></span>|
|<span data-ttu-id="22acf-347">ProjBudgetManager.deleteBudgetLinesBeforeImportForRevs</span><span class="sxs-lookup"><span data-stu-id="22acf-347">ProjBudgetManager.deleteBudgetLinesBeforeImportForRevs</span></span>|
|<span data-ttu-id="22acf-348">ProjBudgetManager.getQuery</span><span class="sxs-lookup"><span data-stu-id="22acf-348">ProjBudgetManager.getQuery</span></span>|
|<span data-ttu-id="22acf-349">ProjBudgetRevisionManager.createBudgetLines</span><span class="sxs-lookup"><span data-stu-id="22acf-349">ProjBudgetRevisionManager.createBudgetLines</span></span>|
|<span data-ttu-id="22acf-350">ProjBudgetTransactionManager.isOverrunAllowed</span><span class="sxs-lookup"><span data-stu-id="22acf-350">ProjBudgetTransactionManager.isOverrunAllowed</span></span>|
|<span data-ttu-id="22acf-351">ProjectCommitmentFacade.updateProjectCommitmentsMap</span><span class="sxs-lookup"><span data-stu-id="22acf-351">ProjectCommitmentFacade.updateProjectCommitmentsMap</span></span>|
|<span data-ttu-id="22acf-352">ProjectMainAccDimensionListProvider.populateMainAccountDimensionList</span><span class="sxs-lookup"><span data-stu-id="22acf-352">ProjectMainAccDimensionListProvider.populateMainAccountDimensionList</span></span>|
|<span data-ttu-id="22acf-353">ProjForecastBudgetCopy.do_Cost</span><span class="sxs-lookup"><span data-stu-id="22acf-353">ProjForecastBudgetCopy.do_Cost</span></span>|
|<span data-ttu-id="22acf-354">ProjForecastBudgetCopy.do_empl</span><span class="sxs-lookup"><span data-stu-id="22acf-354">ProjForecastBudgetCopy.do_empl</span></span>|
|<span data-ttu-id="22acf-355">ProjForecastBudgetCopy.do_onAcc</span><span class="sxs-lookup"><span data-stu-id="22acf-355">ProjForecastBudgetCopy.do_onAcc</span></span>|
|<span data-ttu-id="22acf-356">ProjForecastBudgetCopy.do_sales</span><span class="sxs-lookup"><span data-stu-id="22acf-356">ProjForecastBudgetCopy.do_sales</span></span>|
|<span data-ttu-id="22acf-357">ProjGroupChange.checkPostedTrxAccounts</span><span class="sxs-lookup"><span data-stu-id="22acf-357">ProjGroupChange.checkPostedTrxAccounts</span></span>|
|<span data-ttu-id="22acf-358">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="22acf-358">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span></span>|
|<span data-ttu-id="22acf-359">ProjInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="22acf-359">ProjInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="22acf-360">ProjInvoiceJournalPost.validateNoTax</span><span class="sxs-lookup"><span data-stu-id="22acf-360">ProjInvoiceJournalPost.validateNoTax</span></span>|
|<span data-ttu-id="22acf-361">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="22acf-361">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="22acf-362">ProjJournalTrans.validateWrite</span><span class="sxs-lookup"><span data-stu-id="22acf-362">ProjJournalTrans.validateWrite</span></span>|
|<span data-ttu-id="22acf-363">ProjPlanVersionCopyHierarchy.addProjPlanVersionFields</span><span class="sxs-lookup"><span data-stu-id="22acf-363">ProjPlanVersionCopyHierarchy.addProjPlanVersionFields</span></span>|
|<span data-ttu-id="22acf-364">ProjPlanVersionCopyHierarchy.insertProjPlanVersionRecords</span><span class="sxs-lookup"><span data-stu-id="22acf-364">ProjPlanVersionCopyHierarchy.insertProjPlanVersionRecords</span></span>|
|<span data-ttu-id="22acf-365">ProjPlanVersionCopyHierarchy.ProjPlanVersionCopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="22acf-365">ProjPlanVersionCopyHierarchy.ProjPlanVersionCopyHierarchy</span></span>|
|<span data-ttu-id="22acf-366">ProjPlanVersionsManager.importProjPlanVersionRecords</span><span class="sxs-lookup"><span data-stu-id="22acf-366">ProjPlanVersionsManager.importProjPlanVersionRecords</span></span>|
|<span data-ttu-id="22acf-367">ProjPost.PostNeverLedger</span><span class="sxs-lookup"><span data-stu-id="22acf-367">ProjPost.PostNeverLedger</span></span>|
|<span data-ttu-id="22acf-368">ProjPost.PostTurnover</span><span class="sxs-lookup"><span data-stu-id="22acf-368">ProjPost.PostTurnover</span></span>|
|<span data-ttu-id="22acf-369">ProjPosting.updateDatasourceRanges</span><span class="sxs-lookup"><span data-stu-id="22acf-369">ProjPosting.updateDatasourceRanges</span></span>|
|<span data-ttu-id="22acf-370">ProjTable.validateWrite</span><span class="sxs-lookup"><span data-stu-id="22acf-370">ProjTable.validateWrite</span></span>|
|<span data-ttu-id="22acf-371">ProjTable.validateWriteServer</span><span class="sxs-lookup"><span data-stu-id="22acf-371">ProjTable.validateWriteServer</span></span>|
|<span data-ttu-id="22acf-372">ProjTask.addTask</span><span class="sxs-lookup"><span data-stu-id="22acf-372">ProjTask.addTask</span></span>|
|<span data-ttu-id="22acf-373">ProjValSetupEmplProj.ProjValSetupEmplProj.AddResourceButton.Click</span><span class="sxs-lookup"><span data-stu-id="22acf-373">ProjValSetupEmplProj.ProjValSetupEmplProj.AddResourceButton.Click</span></span>|
|<span data-ttu-id="22acf-374">ProjWBSDataEntityHelper.postInsertOperation</span><span class="sxs-lookup"><span data-stu-id="22acf-374">ProjWBSDataEntityHelper.postInsertOperation</span></span>|
|<span data-ttu-id="22acf-375">PurchAutoCreate_ReleaseFromAgreement.createLines</span><span class="sxs-lookup"><span data-stu-id="22acf-375">PurchAutoCreate_ReleaseFromAgreement.createLines</span></span>|
|<span data-ttu-id="22acf-376">PurchInvoiceJournalPost.calcLastPurchPrice</span><span class="sxs-lookup"><span data-stu-id="22acf-376">PurchInvoiceJournalPost.calcLastPurchPrice</span></span>|
|<span data-ttu-id="22acf-377">PurchPackingSlipJournalPost.updateSourceLineBeforePosting</span><span class="sxs-lookup"><span data-stu-id="22acf-377">PurchPackingSlipJournalPost.updateSourceLineBeforePosting</span></span>|
|<span data-ttu-id="22acf-378">PurchReqLine.defaultBuyingLegalEntity</span><span class="sxs-lookup"><span data-stu-id="22acf-378">PurchReqLine.defaultBuyingLegalEntity</span></span>|
|<span data-ttu-id="22acf-379">PurchRFQCaseAutoCreate_PurchReq.calcRFQHeaderValues</span><span class="sxs-lookup"><span data-stu-id="22acf-379">PurchRFQCaseAutoCreate_PurchReq.calcRFQHeaderValues</span></span>|
|<span data-ttu-id="22acf-380">PurchTable/InventDim/InventBatchId.modified</span><span class="sxs-lookup"><span data-stu-id="22acf-380">PurchTable/InventDim/InventBatchId.modified</span></span>|
|<span data-ttu-id="22acf-381">ReqTransPoMarkFirm.executeAction</span><span class="sxs-lookup"><span data-stu-id="22acf-381">ReqTransPoMarkFirm.executeAction</span></span>|
|<span data-ttu-id="22acf-382">ReqTransPOMarkFirm.CreateProdBOM</span><span class="sxs-lookup"><span data-stu-id="22acf-382">ReqTransPOMarkFirm.CreateProdBOM</span></span>|
|<span data-ttu-id="22acf-383">ReqTransPoMarkFirm.purchTablePostProcessing</span><span class="sxs-lookup"><span data-stu-id="22acf-383">ReqTransPoMarkFirm.purchTablePostProcessing</span></span>|
|<span data-ttu-id="22acf-384">ReqTransPoMarkFirm.setDeliveryDateAndPriceDisc</span><span class="sxs-lookup"><span data-stu-id="22acf-384">ReqTransPoMarkFirm.setDeliveryDateAndPriceDisc</span></span>|
|<span data-ttu-id="22acf-385">ReqTransPoMarkFirm.setGroupingIndicators</span><span class="sxs-lookup"><span data-stu-id="22acf-385">ReqTransPoMarkFirm.setGroupingIndicators</span></span>|
|<span data-ttu-id="22acf-386">RequisitionPurchaseOrderGeneration.Create</span><span class="sxs-lookup"><span data-stu-id="22acf-386">RequisitionPurchaseOrderGeneration.Create</span></span>|
|<span data-ttu-id="22acf-387">RequisitionPurchaseOrderGeneration.createPurch</span><span class="sxs-lookup"><span data-stu-id="22acf-387">RequisitionPurchaseOrderGeneration.createPurch</span></span>|
|<span data-ttu-id="22acf-388">RequisitionPurchaseOrderGeneration.getVendors</span><span class="sxs-lookup"><span data-stu-id="22acf-388">RequisitionPurchaseOrderGeneration.getVendors</span></span>|
|<span data-ttu-id="22acf-389">ResReserveCapacity.getCapacityPercentage</span><span class="sxs-lookup"><span data-stu-id="22acf-389">ResReserveCapacity.getCapacityPercentage</span></span>|
|<span data-ttu-id="22acf-390">RetailCreateLinesFromProductsToAdd.loadDiscountLines</span><span class="sxs-lookup"><span data-stu-id="22acf-390">RetailCreateLinesFromProductsToAdd.loadDiscountLines</span></span>|
|<span data-ttu-id="22acf-391">RetailMassUpdateValidator.validateWriteOnInventModelGroupItem</span><span class="sxs-lookup"><span data-stu-id="22acf-391">RetailMassUpdateValidator.validateWriteOnInventModelGroupItem</span></span>|
|<span data-ttu-id="22acf-392">RetailMediaAssociationHelper.populateMediaAssociationTable</span><span class="sxs-lookup"><span data-stu-id="22acf-392">RetailMediaAssociationHelper.populateMediaAssociationTable</span></span>|
|<span data-ttu-id="22acf-393">RetailOENInfo.parseEmailTemplate</span><span class="sxs-lookup"><span data-stu-id="22acf-393">RetailOENInfo.parseEmailTemplate</span></span>|
|<span data-ttu-id="22acf-394">RetailPrintLabels.loadFromArgs</span><span class="sxs-lookup"><span data-stu-id="22acf-394">RetailPrintLabels.loadFromArgs</span></span>|
|<span data-ttu-id="22acf-395">RetailPrintLabels.loadLines</span><span class="sxs-lookup"><span data-stu-id="22acf-395">RetailPrintLabels.loadLines</span></span>|
|<span data-ttu-id="22acf-396">RetailTransactionServiceOrders.createOrUpdateRetailOrderHeader</span><span class="sxs-lookup"><span data-stu-id="22acf-396">RetailTransactionServiceOrders.createOrUpdateRetailOrderHeader</span></span>|
|<span data-ttu-id="22acf-397">RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span><span class="sxs-lookup"><span data-stu-id="22acf-397">RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span></span>|
|<span data-ttu-id="22acf-398">SalesConfirmJournalPost.createReportData</span><span class="sxs-lookup"><span data-stu-id="22acf-398">SalesConfirmJournalPost.createReportData</span></span>|
|<span data-ttu-id="22acf-399">SalesFormLetter_Invoice.checkInvoicePrices</span><span class="sxs-lookup"><span data-stu-id="22acf-399">SalesFormLetter_Invoice.checkInvoicePrices</span></span>|
|<span data-ttu-id="22acf-400">SalesInvoiceDP.setPackingSlipDetails</span><span class="sxs-lookup"><span data-stu-id="22acf-400">SalesInvoiceDP.setPackingSlipDetails</span></span>|
|<span data-ttu-id="22acf-401">SalesInvoiceJournalPostBase.updateInventory</span><span class="sxs-lookup"><span data-stu-id="22acf-401">SalesInvoiceJournalPostBase.updateInventory</span></span>|
|<span data-ttu-id="22acf-402">SalesInvoiceJournalPostBase.updateInventoryFinancialForSalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="22acf-402">SalesInvoiceJournalPostBase.updateInventoryFinancialForSalesInvoiceLine</span></span>|
|<span data-ttu-id="22acf-403">SalesLine.CheckItemId</span><span class="sxs-lookup"><span data-stu-id="22acf-403">SalesLine.CheckItemId</span></span>|
|<span data-ttu-id="22acf-404">SalesLine.getInventQtyFromCWUnit</span><span class="sxs-lookup"><span data-stu-id="22acf-404">SalesLine.getInventQtyFromCWUnit</span></span>|
|<span data-ttu-id="22acf-405">SalesLine.setInventDeliverNow</span><span class="sxs-lookup"><span data-stu-id="22acf-405">SalesLine.setInventDeliverNow</span></span>|
|<span data-ttu-id="22acf-406">SalesLineType.validateWrite</span><span class="sxs-lookup"><span data-stu-id="22acf-406">SalesLineType.validateWrite</span></span>|
|<span data-ttu-id="22acf-407">SalesQuotationDP.createTaxLines</span><span class="sxs-lookup"><span data-stu-id="22acf-407">SalesQuotationDP.createTaxLines</span></span>|
|<span data-ttu-id="22acf-408">SalesQuotationDP.itemId</span><span class="sxs-lookup"><span data-stu-id="22acf-408">SalesQuotationDP.itemId</span></span>|
|<span data-ttu-id="22acf-409">SalesQuotationLine.PriceDate</span><span class="sxs-lookup"><span data-stu-id="22acf-409">SalesQuotationLine.PriceDate</span></span>|
|<span data-ttu-id="22acf-410">SalesQuotationTable.active</span><span class="sxs-lookup"><span data-stu-id="22acf-410">SalesQuotationTable.active</span></span>|
|<span data-ttu-id="22acf-411">SalesTable-DataSource_mcrSalesTable-DataField_SourceId.modified</span><span class="sxs-lookup"><span data-stu-id="22acf-411">SalesTable-DataSource_mcrSalesTable-DataField_SourceId.modified</span></span>|
|<span data-ttu-id="22acf-412">ShipOrderForm.POS.ChangeOriginOnShipOrders</span><span class="sxs-lookup"><span data-stu-id="22acf-412">ShipOrderForm.POS.ChangeOriginOnShipOrders</span></span>|
|<span data-ttu-id="22acf-413">SmabomDesignerCtrl.listInsertHistory</span><span class="sxs-lookup"><span data-stu-id="22acf-413">SmabomDesignerCtrl.listInsertHistory</span></span>|
|<span data-ttu-id="22acf-414">SmabomDesignerCtrl.treeSubstituteBOMonNode, treeDeleteNode, treeDeleteChildrenCollect</span><span class="sxs-lookup"><span data-stu-id="22acf-414">SmabomDesignerCtrl.treeSubstituteBOMonNode, treeDeleteNode, treeDeleteChildrenCollect</span></span>|
|<span data-ttu-id="22acf-415">SMAServiceObjectrelation.jumpRefBOMTable</span><span class="sxs-lookup"><span data-stu-id="22acf-415">SMAServiceObjectrelation.jumpRefBOMTable</span></span>|
|<span data-ttu-id="22acf-416">SubledgerJournalizerProjectExtension.createProjectActualCostDetail</span><span class="sxs-lookup"><span data-stu-id="22acf-416">SubledgerJournalizerProjectExtension.createProjectActualCostDetail</span></span>|
|<span data-ttu-id="22acf-417">SubledgerJournalizerProjectExtension.createProjectActualSalesDetail</span><span class="sxs-lookup"><span data-stu-id="22acf-417">SubledgerJournalizerProjectExtension.createProjectActualSalesDetail</span></span>|
|<span data-ttu-id="22acf-418">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelated</span><span class="sxs-lookup"><span data-stu-id="22acf-418">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelated</span></span>|
|<span data-ttu-id="22acf-419">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span><span class="sxs-lookup"><span data-stu-id="22acf-419">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span></span>|
|<span data-ttu-id="22acf-420">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span><span class="sxs-lookup"><span data-stu-id="22acf-420">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span></span>|
|<span data-ttu-id="22acf-421">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span><span class="sxs-lookup"><span data-stu-id="22acf-421">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span></span>|
|<span data-ttu-id="22acf-422">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span><span class="sxs-lookup"><span data-stu-id="22acf-422">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span></span>|
|<span data-ttu-id="22acf-423">SubledgerJournalTransferCommand.insertGeneralJournalEntryRelated</span><span class="sxs-lookup"><span data-stu-id="22acf-423">SubledgerJournalTransferCommand.insertGeneralJournalEntryRelated</span></span>|
|<span data-ttu-id="22acf-424">SuppItem.calcSuppItem</span><span class="sxs-lookup"><span data-stu-id="22acf-424">SuppItem.calcSuppItem</span></span>|
|<span data-ttu-id="22acf-425">TaxProformaSpec.parmTaxSpec</span><span class="sxs-lookup"><span data-stu-id="22acf-425">TaxProformaSpec.parmTaxSpec</span></span>|
|<span data-ttu-id="22acf-426">TaxWithhold.postTaxWithhold</span><span class="sxs-lookup"><span data-stu-id="22acf-426">TaxWithhold.postTaxWithhold</span></span>|
|<span data-ttu-id="22acf-427">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span><span class="sxs-lookup"><span data-stu-id="22acf-427">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span></span>|
|<span data-ttu-id="22acf-428">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span><span class="sxs-lookup"><span data-stu-id="22acf-428">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span></span>|
|<span data-ttu-id="22acf-429">TmsProcessXML_Base.readRateShipment</span><span class="sxs-lookup"><span data-stu-id="22acf-429">TmsProcessXML_Base.readRateShipment</span></span>|
|<span data-ttu-id="22acf-430">TMSRouteHelper.getShipDates</span><span class="sxs-lookup"><span data-stu-id="22acf-430">TMSRouteHelper.getShipDates</span></span>|
|<span data-ttu-id="22acf-431">TradeLineNumberManager.checkLineNumber</span><span class="sxs-lookup"><span data-stu-id="22acf-431">TradeLineNumberManager.checkLineNumber</span></span>|
|<span data-ttu-id="22acf-432">TrvCreditCardReminder.mail</span><span class="sxs-lookup"><span data-stu-id="22acf-432">TrvCreditCardReminder.mail</span></span> |
|<span data-ttu-id="22acf-433">TrvCreditCardReminder.runQT</span><span class="sxs-lookup"><span data-stu-id="22acf-433">TrvCreditCardReminder.runQT</span></span>|
|<span data-ttu-id="22acf-434">TrvExpenditureParticipantProvider.resolveFromDimensions</span><span class="sxs-lookup"><span data-stu-id="22acf-434">TrvExpenditureParticipantProvider.resolveFromDimensions</span></span>|
|<span data-ttu-id="22acf-435">TrvExpenditureParticipantProvider.resolve</span><span class="sxs-lookup"><span data-stu-id="22acf-435">TrvExpenditureParticipantProvider.resolve</span></span>|
|<span data-ttu-id="22acf-436">TrvExpenditureParticipantProvider.resolveProjectAuthorities</span><span class="sxs-lookup"><span data-stu-id="22acf-436">TrvExpenditureParticipantProvider.resolveProjectAuthorities</span></span>|
|<span data-ttu-id="22acf-437">TrvExpenses.openSplitDetailsForm</span><span class="sxs-lookup"><span data-stu-id="22acf-437">TrvExpenses.openSplitDetailsForm</span></span>|
|<span data-ttu-id="22acf-438">TrvExpTable.validateSubmit</span><span class="sxs-lookup"><span data-stu-id="22acf-438">TrvExpTable.validateSubmit</span></span>|
|<span data-ttu-id="22acf-439">VendAgingReportController.getReportName</span><span class="sxs-lookup"><span data-stu-id="22acf-439">VendAgingReportController.getReportName</span></span>|
|<span data-ttu-id="22acf-440">VendBalanceList.insertIntoTmpAccountSum</span><span class="sxs-lookup"><span data-stu-id="22acf-440">VendBalanceList.insertIntoTmpAccountSum</span></span>|
|<span data-ttu-id="22acf-441">VendInvoiceInfoListPage.postInvoice</span><span class="sxs-lookup"><span data-stu-id="22acf-441">VendInvoiceInfoListPage.postInvoice</span></span>|
|<span data-ttu-id="22acf-442">VendOutPaymRecord_Cheque.checkValues</span><span class="sxs-lookup"><span data-stu-id="22acf-442">VendOutPaymRecord_Cheque.checkValues</span></span>|
|<span data-ttu-id="22acf-443">VendVendorEntity/VendVendorV2Entity.processChangesForApproval</span><span class="sxs-lookup"><span data-stu-id="22acf-443">VendVendorEntity/VendVendorV2Entity.processChangesForApproval</span></span>|
|<span data-ttu-id="22acf-444">VestingID.Table: HRMCompVarAward</span><span class="sxs-lookup"><span data-stu-id="22acf-444">VestingID.Table: HRMCompVarAward</span></span>|
|<span data-ttu-id="22acf-445">WhsContainerization.packTmpWorkLine</span><span class="sxs-lookup"><span data-stu-id="22acf-445">WhsContainerization.packTmpWorkLine</span></span>|
|<span data-ttu-id="22acf-446">WhsControlBatchId.process</span><span class="sxs-lookup"><span data-stu-id="22acf-446">WhsControlBatchId.process</span></span>|
|<span data-ttu-id="22acf-447">WHSPostPackingSlip.canShipConfirm</span><span class="sxs-lookup"><span data-stu-id="22acf-447">WHSPostPackingSlip.canShipConfirm</span></span>|
|<span data-ttu-id="22acf-448">WHSPostPackingSlip.shipConfirmLoad</span><span class="sxs-lookup"><span data-stu-id="22acf-448">WHSPostPackingSlip.shipConfirmLoad</span></span>|
|<span data-ttu-id="22acf-449">WHSProcessGuideStartChangeWarehouseStep.doExecute</span><span class="sxs-lookup"><span data-stu-id="22acf-449">WHSProcessGuideStartChangeWarehouseStep.doExecute</span></span>|
|<span data-ttu-id="22acf-450">WhsrfControlData.batchExistInLocation</span><span class="sxs-lookup"><span data-stu-id="22acf-450">WhsrfControlData.batchExistInLocation</span></span>|
|<span data-ttu-id="22acf-451">WhsShipConfirm.tmsMultiLoadShipConfirm</span><span class="sxs-lookup"><span data-stu-id="22acf-451">WhsShipConfirm.tmsMultiLoadShipConfirm</span></span>|
|<span data-ttu-id="22acf-452">WHSSplitWork.handleOrignalWorkLine</span><span class="sxs-lookup"><span data-stu-id="22acf-452">WHSSplitWork.handleOrignalWorkLine</span></span>|
|<span data-ttu-id="22acf-453">WHSSplitWork.handleRemainingPickTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-453">WHSSplitWork.handleRemainingPickTrans</span></span>|
|<span data-ttu-id="22acf-454">WHSSplitWork.processRemainingTransaction</span><span class="sxs-lookup"><span data-stu-id="22acf-454">WHSSplitWork.processRemainingTransaction</span></span>|
|<span data-ttu-id="22acf-455">WHSSplitWork.updateClosedPickTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-455">WHSSplitWork.updateClosedPickTrans</span></span>|
|<span data-ttu-id="22acf-456">WhsUnShip.cleanUpTOInventTransDims</span><span class="sxs-lookup"><span data-stu-id="22acf-456">WhsUnShip.cleanUpTOInventTransDims</span></span>|
|<span data-ttu-id="22acf-457">WhsWarehouseRelease.createShipmentsForTransferOrders</span><span class="sxs-lookup"><span data-stu-id="22acf-457">WhsWarehouseRelease.createShipmentsForTransferOrders</span></span>|
|<span data-ttu-id="22acf-458">WHSWorkCreate.createWorkInventTrans</span><span class="sxs-lookup"><span data-stu-id="22acf-458">WHSWorkCreate.createWorkInventTrans</span></span>|
|<span data-ttu-id="22acf-459">WHSWorkCreate.createWorkTable</span><span class="sxs-lookup"><span data-stu-id="22acf-459">WHSWorkCreate.createWorkTable</span></span>|
|<span data-ttu-id="22acf-460">WhsWorkCreateProdPut.createReportFinished</span><span class="sxs-lookup"><span data-stu-id="22acf-460">WhsWorkCreateProdPut.createReportFinished</span></span>|
|<span data-ttu-id="22acf-461">WhsWorkCreateReceiving.createBatch</span><span class="sxs-lookup"><span data-stu-id="22acf-461">WhsWorkCreateReceiving.createBatch</span></span>|
|<span data-ttu-id="22acf-462">WHSWorkExecute.putAwayToLocation()</span><span class="sxs-lookup"><span data-stu-id="22acf-462">WHSWorkExecute.putAwayToLocation()</span></span>|
|<span data-ttu-id="22acf-463">WHSWorkExecuteDisplay.buildInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="22acf-463">WHSWorkExecuteDisplay.buildInventoryStatus</span></span>|
|<span data-ttu-id="22acf-464">WhsWorkExecuteDisplay.getNextFormState</span><span class="sxs-lookup"><span data-stu-id="22acf-464">WhsWorkExecuteDisplay.getNextFormState</span></span>|
|<span data-ttu-id="22acf-465">WhsWorkExecuteDisplay.processTrackingDimDetails</span><span class="sxs-lookup"><span data-stu-id="22acf-465">WhsWorkExecuteDisplay.processTrackingDimDetails</span></span>|
|<span data-ttu-id="22acf-466">WhsWorkExecuteDisplay.processVendorBatchDetails</span><span class="sxs-lookup"><span data-stu-id="22acf-466">WhsWorkExecuteDisplay.processVendorBatchDetails</span></span>|
|<span data-ttu-id="22acf-467">WhsWorkExecuteDisplay.processWorkLine</span><span class="sxs-lookup"><span data-stu-id="22acf-467">WhsWorkExecuteDisplay.processWorkLine</span></span>|
|<span data-ttu-id="22acf-468">WHSWorkExecuteDisplay.setBatchDetails</span><span class="sxs-lookup"><span data-stu-id="22acf-468">WHSWorkExecuteDisplay.setBatchDetails</span></span>|
|<span data-ttu-id="22acf-469">WhsWorkExecuteDisplayLoadItemReceiving.buildPOReceiving</span><span class="sxs-lookup"><span data-stu-id="22acf-469">WhsWorkExecuteDisplayLoadItemReceiving.buildPOReceiving</span></span>|
|<span data-ttu-id="22acf-470">WHSWorkExecuteDisplayLPReceiving.generateItemInfoForReceiving</span><span class="sxs-lookup"><span data-stu-id="22acf-470">WHSWorkExecuteDisplayLPReceiving.generateItemInfoForReceiving</span></span>|
|<span data-ttu-id="22acf-471">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span><span class="sxs-lookup"><span data-stu-id="22acf-471">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span></span>|
|<span data-ttu-id="22acf-472">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span><span class="sxs-lookup"><span data-stu-id="22acf-472">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span></span>|
|<span data-ttu-id="22acf-473">WhsWorkExecuteDisplayReportAsFinished.displayForm</span><span class="sxs-lookup"><span data-stu-id="22acf-473">WhsWorkExecuteDisplayReportAsFinished.displayForm</span></span>|
|<span data-ttu-id="22acf-474">WHSWorkTable.satisfyDemandWorkLine</span><span class="sxs-lookup"><span data-stu-id="22acf-474">WHSWorkTable.satisfyDemandWorkLine</span></span>|
|<span data-ttu-id="22acf-475">WmsArrivalCreateJournal.createWMSJournalTransFromArrivalDetails</span><span class="sxs-lookup"><span data-stu-id="22acf-475">WmsArrivalCreateJournal.createWMSJournalTransFromArrivalDetails</span></span>|
|<span data-ttu-id="22acf-476">WmsJournalCheckPostReception.returnOrderUpdate</span><span class="sxs-lookup"><span data-stu-id="22acf-476">WmsJournalCheckPostReception.returnOrderUpdate</span></span>|
|<span data-ttu-id="22acf-477">WmsOrderCreate.updateCreatewmsOrder</span><span class="sxs-lookup"><span data-stu-id="22acf-477">WmsOrderCreate.updateCreatewmsOrder</span></span>|
|<span data-ttu-id="22acf-478">WorkflowHierarchyProviderHelperEventHandler.addDataSourceFieldsDelegate</span><span class="sxs-lookup"><span data-stu-id="22acf-478">WorkflowHierarchyProviderHelperEventHandler.addDataSourceFieldsDelegate</span></span>|
|<span data-ttu-id="22acf-479">WorkflowHierarchyProviderHelperEventHandler.loadLimits</span><span class="sxs-lookup"><span data-stu-id="22acf-479">WorkflowHierarchyProviderHelperEventHandler.loadLimits</span></span>|
|<span data-ttu-id="22acf-480">WrkCtrScheduler_Prod.saveOperation</span><span class="sxs-lookup"><span data-stu-id="22acf-480">WrkCtrScheduler_Prod.saveOperation</span></span>|

## <a name="other-changes"></a><span data-ttu-id="22acf-481">その他の変更</span><span class="sxs-lookup"><span data-stu-id="22acf-481">Other changes</span></span>

<span data-ttu-id="22acf-482">次の追加の変更が、拡張機能に対して行われました。</span><span class="sxs-lookup"><span data-stu-id="22acf-482">The following additional changes have been made for extensibility.</span></span>

- <span data-ttu-id="22acf-483">InventSumFields が使用されているクエリを SysDa に変換します。</span><span class="sxs-lookup"><span data-stu-id="22acf-483">Convert queries where InventSumFields is used to SysDa.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]