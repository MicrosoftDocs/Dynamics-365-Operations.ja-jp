---
title: Dynamics 365 for Finance and Operations バージョン 10.0 の拡張機能の変更
description: これのトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0 に実装された拡張機能を一覧します。
author: FrankDahl
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-02-11
ms.dyn365.ops.version: App 10.0
ms.openlocfilehash: d76074fafc9caab119055193618ee7a220a43e37
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537501"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-100"></a><span data-ttu-id="6f271-103">Dynamics 365 for Finance and Operations バージョン 10.0 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="6f271-103">Extensibility changes in Dynamics 365 for Finance and Operations version 10.0</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6f271-104">これは、Dynamics 365 for Finance and Operations バージョン 10.0 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6f271-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations version 10.0.</span></span> <span data-ttu-id="6f271-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f271-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="enumerations-made-extensible"></a><span data-ttu-id="6f271-106">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="6f271-106">Enumerations made extensible</span></span>

<span data-ttu-id="6f271-107">これらの列挙は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="6f271-107">These enumerations have been made extensible in this update.</span></span>

| <span data-ttu-id="6f271-108">列挙型</span><span class="sxs-lookup"><span data-stu-id="6f271-108">Enumeration</span></span>|
| --------------- |
|<span data-ttu-id="6f271-109">AssetAccrualCalendar</span><span class="sxs-lookup"><span data-stu-id="6f271-109">AssetAccrualCalendar</span></span>|
|<span data-ttu-id="6f271-110">AssetYear</span><span class="sxs-lookup"><span data-stu-id="6f271-110">AssetYear</span></span>|
|<span data-ttu-id="6f271-111">BankReconciliationReportType</span><span class="sxs-lookup"><span data-stu-id="6f271-111">BankReconciliationReportType</span></span>|
|<span data-ttu-id="6f271-112">BudgetPlanColumnPeriodLength</span><span class="sxs-lookup"><span data-stu-id="6f271-112">BudgetPlanColumnPeriodLength</span></span>|
|<span data-ttu-id="6f271-113">BudgetPlanHCMReportGroupOption</span><span class="sxs-lookup"><span data-stu-id="6f271-113">BudgetPlanHCMReportGroupOption</span></span>|
|<span data-ttu-id="6f271-114">CurrencyTypeBrief_RU</span><span class="sxs-lookup"><span data-stu-id="6f271-114">CurrencyTypeBrief_RU</span></span>|
|<span data-ttu-id="6f271-115">EInvoiceStatus_IT</span><span class="sxs-lookup"><span data-stu-id="6f271-115">EInvoiceStatus_IT</span></span>|
|<span data-ttu-id="6f271-116">EInvoiceStatus_IT</span><span class="sxs-lookup"><span data-stu-id="6f271-116">EInvoiceStatus_IT</span></span>|
|<span data-ttu-id="6f271-117">HRPAuthorityBasis</span><span class="sxs-lookup"><span data-stu-id="6f271-117">HRPAuthorityBasis</span></span>|
|<span data-ttu-id="6f271-118">HuExchOutflowType</span><span class="sxs-lookup"><span data-stu-id="6f271-118">HuExchOutflowType</span></span>|
|<span data-ttu-id="6f271-119">InventJournalTagStatus</span><span class="sxs-lookup"><span data-stu-id="6f271-119">InventJournalTagStatus</span></span>|
|<span data-ttu-id="6f271-120">InvoiceAssociationType</span><span class="sxs-lookup"><span data-stu-id="6f271-120">InvoiceAssociationType</span></span>|
|<span data-ttu-id="6f271-121">MCRClaimType</span><span class="sxs-lookup"><span data-stu-id="6f271-121">MCRClaimType</span></span>|
|<span data-ttu-id="6f271-122">MCRMerchandisingEventCategory</span><span class="sxs-lookup"><span data-stu-id="6f271-122">MCRMerchandisingEventCategory</span></span>|
|<span data-ttu-id="6f271-123">PaymAttribute</span><span class="sxs-lookup"><span data-stu-id="6f271-123">PaymAttribute</span></span>|
|<span data-ttu-id="6f271-124">PaymProposalReportedBy</span><span class="sxs-lookup"><span data-stu-id="6f271-124">PaymProposalReportedBy</span></span>|
|<span data-ttu-id="6f271-125">PayrollCategory</span><span class="sxs-lookup"><span data-stu-id="6f271-125">PayrollCategory</span></span>|
|<span data-ttu-id="6f271-126">projActualVsBudget</span><span class="sxs-lookup"><span data-stu-id="6f271-126">projActualVsBudget</span></span>|
|<span data-ttu-id="6f271-127">ProjListStateId</span><span class="sxs-lookup"><span data-stu-id="6f271-127">ProjListStateId</span></span>|
|<span data-ttu-id="6f271-128">ProjTransLayout</span><span class="sxs-lookup"><span data-stu-id="6f271-128">ProjTransLayout</span></span>|
|<span data-ttu-id="6f271-129">ProjType</span><span class="sxs-lookup"><span data-stu-id="6f271-129">ProjType</span></span>|
|<span data-ttu-id="6f271-130">RCashCheckContract</span><span class="sxs-lookup"><span data-stu-id="6f271-130">RCashCheckContract</span></span>|
|<span data-ttu-id="6f271-131">RCashDocRepresType</span><span class="sxs-lookup"><span data-stu-id="6f271-131">RCashDocRepresType</span></span>|
|<span data-ttu-id="6f271-132">RCashDocType</span><span class="sxs-lookup"><span data-stu-id="6f271-132">RCashDocType</span></span>|
|<span data-ttu-id="6f271-133">RCashRemainLimitType</span><span class="sxs-lookup"><span data-stu-id="6f271-133">RCashRemainLimitType</span></span>|
|<span data-ttu-id="6f271-134">RCashTableAll</span><span class="sxs-lookup"><span data-stu-id="6f271-134">RCashTableAll</span></span>|
|<span data-ttu-id="6f271-135">RCashTransStatus</span><span class="sxs-lookup"><span data-stu-id="6f271-135">RCashTransStatus</span></span>|
|<span data-ttu-id="6f271-136">SMARelationType</span><span class="sxs-lookup"><span data-stu-id="6f271-136">SMARelationType</span></span>|
|<span data-ttu-id="6f271-137">smmActivityTaskTimeType</span><span class="sxs-lookup"><span data-stu-id="6f271-137">smmActivityTaskTimeType</span></span>|
|<span data-ttu-id="6f271-138">TaxIdType</span><span class="sxs-lookup"><span data-stu-id="6f271-138">TaxIdType</span></span>|
|<span data-ttu-id="6f271-139">TrvAirlineServiceClassEnum</span><span class="sxs-lookup"><span data-stu-id="6f271-139">TrvAirlineServiceClassEnum</span></span>|
|<span data-ttu-id="6f271-140">TrvFieldVisibility</span><span class="sxs-lookup"><span data-stu-id="6f271-140">TrvFieldVisibility</span></span>|
|<span data-ttu-id="6f271-141">TSPeriodFrequency</span><span class="sxs-lookup"><span data-stu-id="6f271-141">TSPeriodFrequency</span></span>|
|<span data-ttu-id="6f271-142">TSPerWeekMth</span><span class="sxs-lookup"><span data-stu-id="6f271-142">TSPerWeekMth</span></span>|
|<span data-ttu-id="6f271-143">VendPaymentValidate</span><span class="sxs-lookup"><span data-stu-id="6f271-143">VendPaymentValidate</span></span>|

## <a name="sql-operations-made-extensible"></a><span data-ttu-id="6f271-144">拡張可能になった SQL 操作</span><span class="sxs-lookup"><span data-stu-id="6f271-144">SQL operations made extensible</span></span>

<span data-ttu-id="6f271-145">これらの SQL 操作は、このアップデートで拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="6f271-145">These SQL operations have been made extensible in this update.</span></span>

| <span data-ttu-id="6f271-146">操作</span><span class="sxs-lookup"><span data-stu-id="6f271-146">Operation</span></span>|
| --------------- |
|<span data-ttu-id="6f271-147">JmgStampJournalTable.makeLines</span><span class="sxs-lookup"><span data-stu-id="6f271-147">JmgStampJournalTable.makeLines</span></span>|
|<span data-ttu-id="6f271-148">MCRDropShipStatusUpdate_PurchLine.updatePurchDropShipStatusOnRecord</span><span class="sxs-lookup"><span data-stu-id="6f271-148">MCRDropShipStatusUpdate_PurchLine.updatePurchDropShipStatusOnRecord</span></span>|
|<span data-ttu-id="6f271-149">MCRDropShipStatusUpdate_PurchTable.updatePurchDropShipStatusOnRecord</span><span class="sxs-lookup"><span data-stu-id="6f271-149">MCRDropShipStatusUpdate_PurchTable.updatePurchDropShipStatusOnRecord</span></span>|
|<span data-ttu-id="6f271-150">SalesInvoiceJournalCreate.checkDocumentData_PL</span><span class="sxs-lookup"><span data-stu-id="6f271-150">SalesInvoiceJournalCreate.checkDocumentData_PL</span></span>|
|<span data-ttu-id="6f271-151">SalesInvoiceJournalPost.postFailed</span><span class="sxs-lookup"><span data-stu-id="6f271-151">SalesInvoiceJournalPost.postFailed</span></span>|

## <a name="metadata-changes"></a><span data-ttu-id="6f271-152">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="6f271-152">Metadata changes</span></span>

<span data-ttu-id="6f271-153">これらのメタデータの変更は、このアップデートで行われました。</span><span class="sxs-lookup"><span data-stu-id="6f271-153">These metadata changes have been made in this update.</span></span>

| <span data-ttu-id="6f271-154">操作</span><span class="sxs-lookup"><span data-stu-id="6f271-154">Operation</span></span> |
| --------------- |
|<span data-ttu-id="6f271-155">/Data Model/Data Entities/BOMBillOfMaterialsVersionV2Entity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-155">/Data Model/Data Entities/BOMBillOfMaterialsVersionV2Entity.IsPublic</span></span>|
|<span data-ttu-id="6f271-156">/Data Model/Data Entities/InventItemBatchEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-156">/Data Model/Data Entities/InventItemBatchEntity.IsPublic</span></span>|
|<span data-ttu-id="6f271-157">/Data Model/Data Entities/InventProductSpecificOrderSettingsV2Entity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-157">/Data Model/Data Entities/InventProductSpecificOrderSettingsV2Entity.IsPublic</span></span>|
|<span data-ttu-id="6f271-158">/Data Model/Data Entities/InventQualityGroupItemAssignmentEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-158">/Data Model/Data Entities/InventQualityGroupItemAssignmentEntity.IsPublic</span></span>|
|<span data-ttu-id="6f271-159">/Data Model/Data Entities/InventQualityTestGroupEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-159">/Data Model/Data Entities/InventQualityTestGroupEntity.IsPublic</span></span>|
|<span data-ttu-id="6f271-160">/Data Model/Data Entities/ProductionPoolEntity.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-160">/Data Model/Data Entities/ProductionPoolEntity.IsPublic</span></span>|
|<span data-ttu-id="6f271-161">/Data Model/Data Entities/WMSItemArrivalJournalHeaderEntity.IsPublic, PublicCollectionName, PublicEntityName</span><span class="sxs-lookup"><span data-stu-id="6f271-161">/Data Model/Data Entities/WMSItemArrivalJournalHeaderEntity.IsPublic, PublicCollectionName, PublicEntityName</span></span>|
|<span data-ttu-id="6f271-162">/DataModel/Tables/WMSStorageLoadUnitReqTrans.WMSStorageLoadUnitReqTran</span><span class="sxs-lookup"><span data-stu-id="6f271-162">/DataModel/Tables/WMSStorageLoadUnitReqTrans.WMSStorageLoadUnitReqTran</span></span>|
|<span data-ttu-id="6f271-163">DimensionHierarchyType/EnumValue/RDeferrals</span><span class="sxs-lookup"><span data-stu-id="6f271-163">DimensionHierarchyType/EnumValue/RDeferrals</span></span>|
|<span data-ttu-id="6f271-164">AOT/Data Model/Tables/CategoryTable.Create RecId インデックス</span><span class="sxs-lookup"><span data-stu-id="6f271-164">AOT/Data Model/Tables/CategoryTable.Create RecId Index</span></span>|
|<span data-ttu-id="6f271-165">EcoResProductCategoryHierarchyEntity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-165">EcoResProductCategoryHierarchyEntity.Property.IsPublic</span></span>|
|<span data-ttu-id="6f271-166">EcoResProductSpecificUnitOfMeasureConversionEntity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-166">EcoResProductSpecificUnitOfMeasureConversionEntity.Property.IsPublic</span></span>|
|<span data-ttu-id="6f271-167">EcoResReleasedProductVariantExternalCodeEntity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-167">EcoResReleasedProductVariantExternalCodeEntity.Property.IsPublic</span></span>|
|<span data-ttu-id="6f271-168">InventProductSpecificOrderSettingsV2Entity.Property.IsPublic</span><span class="sxs-lookup"><span data-stu-id="6f271-168">InventProductSpecificOrderSettingsV2Entity.Property.IsPublic</span></span>|
|<span data-ttu-id="6f271-169">複数の EDT に "小数点以下の桁数は拡張可能" プロパティ</span><span class="sxs-lookup"><span data-stu-id="6f271-169">"No of Decimals is Extensible" property on several EDTs</span></span>|
|<span data-ttu-id="6f271-170">RetailLoyaltyRewardPoint.Replacement キー</span><span class="sxs-lookup"><span data-stu-id="6f271-170">RetailLoyaltyRewardPoint.Replacement Key</span></span>|
|<span data-ttu-id="6f271-171">Tables/CustTrans/Relations/ThirdPartyBankAccountId.Validate</span><span class="sxs-lookup"><span data-stu-id="6f271-171">Tables/CustTrans/Relations/ThirdPartyBankAccountId.Validate</span></span>|
|<span data-ttu-id="6f271-172">Tables/EInvoicePropertyTable/Relations/EInvoicePropertyTypeTable.RelationshipType</span><span class="sxs-lookup"><span data-stu-id="6f271-172">Tables/EInvoicePropertyTable/Relations/EInvoicePropertyTypeTable.RelationshipType</span></span>|
|<span data-ttu-id="6f271-173">Tables/ResourceSetup.FormRef</span><span class="sxs-lookup"><span data-stu-id="6f271-173">Tables/ResourceSetup.FormRef</span></span>|
|<span data-ttu-id="6f271-174">Tables/WHSTmpWorkExecuteListBoxItems/Fields/Elements.EDT</span><span class="sxs-lookup"><span data-stu-id="6f271-174">Tables/WHSTmpWorkExecuteListBoxItems/Fields/Elements.EDT</span></span>|

## <a name="refactored-methods"></a><span data-ttu-id="6f271-175">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="6f271-175">Refactored methods</span></span>

<span data-ttu-id="6f271-176">これらのメソッドは、拡張性をサポートするためにリファクターされています。</span><span class="sxs-lookup"><span data-stu-id="6f271-176">These methods have been refactored to support extensibility.</span></span>

| <span data-ttu-id="6f271-177">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="6f271-177">Refactored methods</span></span>                                                                             |
|------------------------------------------------------------------------------------------------|
|<span data-ttu-id="6f271-178">AdvancedLedgerEntryLine.setProjInvoiceLineLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="6f271-178">AdvancedLedgerEntryLine.setProjInvoiceLineLedgerDimension</span></span>|
|<span data-ttu-id="6f271-179">AgreementConfirmationDP.getSalesAgreementHeader</span><span class="sxs-lookup"><span data-stu-id="6f271-179">AgreementConfirmationDP.getSalesAgreementHeader</span></span>|
|<span data-ttu-id="6f271-180">AgreementConfirmationDP.getSalesAgreementHeaderHistory</span><span class="sxs-lookup"><span data-stu-id="6f271-180">AgreementConfirmationDP.getSalesAgreementHeaderHistory</span></span>|
|<span data-ttu-id="6f271-181">PurchAutoCreate_Sales.createPurchLine</span><span class="sxs-lookup"><span data-stu-id="6f271-181">PurchAutoCreate_Sales.createPurchLine</span></span>|
|<span data-ttu-id="6f271-182">PurchCreateFromSalesOrder.run</span><span class="sxs-lookup"><span data-stu-id="6f271-182">PurchCreateFromSalesOrder.run</span></span>|
|<span data-ttu-id="6f271-183">InventItemPrice.insert</span><span class="sxs-lookup"><span data-stu-id="6f271-183">InventItemPrice.insert</span></span>|
|<span data-ttu-id="6f271-184">InventJournalTrans.setCostPrice</span><span class="sxs-lookup"><span data-stu-id="6f271-184">InventJournalTrans.setCostPrice</span></span>|
|<span data-ttu-id="6f271-185">PurchLine.initFromReqPO</span><span class="sxs-lookup"><span data-stu-id="6f271-185">PurchLine.initFromReqPO</span></span>|
|<span data-ttu-id="6f271-186">AssetBook.initDepreciationProfile</span><span class="sxs-lookup"><span data-stu-id="6f271-186">AssetBook.initDepreciationProfile</span></span>|
|<span data-ttu-id="6f271-187">AssetDepreciationProfile.validateStraightLine</span><span class="sxs-lookup"><span data-stu-id="6f271-187">AssetDepreciationProfile.validateStraightLine</span></span>|
|<span data-ttu-id="6f271-188">AssetProposalDepreciation.run</span><span class="sxs-lookup"><span data-stu-id="6f271-188">AssetProposalDepreciation.run</span></span>|
|<span data-ttu-id="6f271-189">BankPaymAdvicePrint.BankPaymAdvicePrint (変数)</span><span class="sxs-lookup"><span data-stu-id="6f271-189">BankPaymAdvicePrint.BankPaymAdvicePrint (variable)</span></span>|
|<span data-ttu-id="6f271-190">BankReconciliationMatchingMatchProcessor.constructMatch</span><span class="sxs-lookup"><span data-stu-id="6f271-190">BankReconciliationMatchingMatchProcessor.constructMatch</span></span>|
|<span data-ttu-id="6f271-191">BankReconMatchingMatchStmtReversalDoc.Multiple</span><span class="sxs-lookup"><span data-stu-id="6f271-191">BankReconMatchingMatchStmtReversalDoc.Multiple</span></span>|
|<span data-ttu-id="6f271-192">BankStatementDocumentEntity.postGetStagingData</span><span class="sxs-lookup"><span data-stu-id="6f271-192">BankStatementDocumentEntity.postGetStagingData</span></span>|
|<span data-ttu-id="6f271-193">BankVoucher.post</span><span class="sxs-lookup"><span data-stu-id="6f271-193">BankVoucher.post</span></span>|
|<span data-ttu-id="6f271-194">BomCalcItemLine.mustExplodePrice</span><span class="sxs-lookup"><span data-stu-id="6f271-194">BomCalcItemLine.mustExplodePrice</span></span>|
|<span data-ttu-id="6f271-195">BOMCopyToProd.delete</span><span class="sxs-lookup"><span data-stu-id="6f271-195">BOMCopyToProd.delete</span></span>|
|<span data-ttu-id="6f271-196">BOMCreateDialog.promptCreateBOMDialog</span><span class="sxs-lookup"><span data-stu-id="6f271-196">BOMCreateDialog.promptCreateBOMDialog</span></span>|
|<span data-ttu-id="6f271-197">BomRouteCopyJob.initFromItemId</span><span class="sxs-lookup"><span data-stu-id="6f271-197">BomRouteCopyJob.initFromItemId</span></span>|
|<span data-ttu-id="6f271-198">BudgetPlanningConfiguration.displayYearOffset</span><span class="sxs-lookup"><span data-stu-id="6f271-198">BudgetPlanningConfiguration.displayYearOffset</span></span>|
|<span data-ttu-id="6f271-199">BudgetPlanningConfiguration.updateColumnPeriodLengthValueLabel</span><span class="sxs-lookup"><span data-stu-id="6f271-199">BudgetPlanningConfiguration.updateColumnPeriodLengthValueLabel</span></span>|
|<span data-ttu-id="6f271-200">CatVendorCatalogProductApproval.getApprovedProductForRetail</span><span class="sxs-lookup"><span data-stu-id="6f271-200">CatVendorCatalogProductApproval.getApprovedProductForRetail</span></span>|
|<span data-ttu-id="6f271-201">LedgerJournalTransType.validateAccountType</span><span class="sxs-lookup"><span data-stu-id="6f271-201">LedgerJournalTransType.validateAccountType</span></span>|
|<span data-ttu-id="6f271-202">LedgerTransferOpening.processQuery</span><span class="sxs-lookup"><span data-stu-id="6f271-202">LedgerTransferOpening.processQuery</span></span>|
|<span data-ttu-id="6f271-203">BankPositivePayExport.generatePositivePayFile</span><span class="sxs-lookup"><span data-stu-id="6f271-203">BankPositivePayExport.generatePositivePayFile</span></span>|
|<span data-ttu-id="6f271-204">BankPositivePayExport.updateBankPositivePay</span><span class="sxs-lookup"><span data-stu-id="6f271-204">BankPositivePayExport.updateBankPositivePay</span></span>|
|<span data-ttu-id="6f271-205">CaseSendEmail.getEmailMessage</span><span class="sxs-lookup"><span data-stu-id="6f271-205">CaseSendEmail.getEmailMessage</span></span>|
|<span data-ttu-id="6f271-206">ContactPerson.insert</span><span class="sxs-lookup"><span data-stu-id="6f271-206">ContactPerson.insert</span></span>|
|<span data-ttu-id="6f271-207">CostSheetModeStrategyStaging.createCostSheetNodes</span><span class="sxs-lookup"><span data-stu-id="6f271-207">CostSheetModeStrategyStaging.createCostSheetNodes</span></span>|
|<span data-ttu-id="6f271-208">CreditCard.recordAuthorization</span><span class="sxs-lookup"><span data-stu-id="6f271-208">CreditCard.recordAuthorization</span></span>|
|<span data-ttu-id="6f271-209">CreditCard.recordCapture</span><span class="sxs-lookup"><span data-stu-id="6f271-209">CreditCard.recordCapture</span></span>|
|<span data-ttu-id="6f271-210">CreditCardPaymentJournal.createJournal</span><span class="sxs-lookup"><span data-stu-id="6f271-210">CreditCardPaymentJournal.createJournal</span></span>|
|<span data-ttu-id="6f271-211">CreditCardPaymentJournal.Init</span><span class="sxs-lookup"><span data-stu-id="6f271-211">CreditCardPaymentJournal.Init</span></span>|
|<span data-ttu-id="6f271-212">CreditCardPaymentJournal.run</span><span class="sxs-lookup"><span data-stu-id="6f271-212">CreditCardPaymentJournal.run</span></span>|
|<span data-ttu-id="6f271-213">CustAgingReportContract.Validate</span><span class="sxs-lookup"><span data-stu-id="6f271-213">CustAgingReportContract.Validate</span></span>|
|<span data-ttu-id="6f271-214">CustAgingReportDP.CustAgingReportTmp</span><span class="sxs-lookup"><span data-stu-id="6f271-214">CustAgingReportDP.CustAgingReportTmp</span></span>|
|<span data-ttu-id="6f271-215">CustAgingReportDPclass.insertCustAgingReportTmp</span><span class="sxs-lookup"><span data-stu-id="6f271-215">CustAgingReportDPclass.insertCustAgingReportTmp</span></span>|
|<span data-ttu-id="6f271-216">CustAgingReportDPclass.setCustAgingReportTmpInReverse</span><span class="sxs-lookup"><span data-stu-id="6f271-216">CustAgingReportDPclass.setCustAgingReportTmpInReverse</span></span>|
|<span data-ttu-id="6f271-217">CustBalanceList.insertIntoTmpAccountSumV2</span><span class="sxs-lookup"><span data-stu-id="6f271-217">CustBalanceList.insertIntoTmpAccountSumV2</span></span>|
|<span data-ttu-id="6f271-218">CustBillOfExchangePostRemit.postSettlingStep</span><span class="sxs-lookup"><span data-stu-id="6f271-218">CustBillOfExchangePostRemit.postSettlingStep</span></span>|
|<span data-ttu-id="6f271-219">CustCollectionsSetTransactionStatusHelper.createActions</span><span class="sxs-lookup"><span data-stu-id="6f271-219">CustCollectionsSetTransactionStatusHelper.createActions</span></span>|
|<span data-ttu-id="6f271-220">CustCustomerBaseEntity/CustCustomerEntity/CustCustomerV2Entity/CustCustomerV3Entity.processChangesForApproval</span><span class="sxs-lookup"><span data-stu-id="6f271-220">CustCustomerBaseEntity/CustCustomerEntity/CustCustomerV2Entity/CustCustomerV3Entity.processChangesForApproval</span></span>|
|<span data-ttu-id="6f271-221">CustCustomerDetailEntity/CustCustomerDetailV2Entity.processChangesForApproval</span><span class="sxs-lookup"><span data-stu-id="6f271-221">CustCustomerDetailEntity/CustCustomerDetailV2Entity.processChangesForApproval</span></span>|
|<span data-ttu-id="6f271-222">CustInvoiceJour.setInvoiceAddress</span><span class="sxs-lookup"><span data-stu-id="6f271-222">CustInvoiceJour.setInvoiceAddress</span></span>|
|<span data-ttu-id="6f271-223">CustInvoiceLine.getCustBillingCodeLedgerAccount</span><span class="sxs-lookup"><span data-stu-id="6f271-223">CustInvoiceLine.getCustBillingCodeLedgerAccount</span></span>|
|<span data-ttu-id="6f271-224">CustInvoiceLine.setProjInvoiceLineLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="6f271-224">CustInvoiceLine.setProjInvoiceLineLedgerDimension</span></span>|
|<span data-ttu-id="6f271-225">CustInvoiceLine.setProjInvoiceLineLedgerDimensionBase</span><span class="sxs-lookup"><span data-stu-id="6f271-225">CustInvoiceLine.setProjInvoiceLineLedgerDimensionBase</span></span>|
|<span data-ttu-id="6f271-226">CustInvoiceLine.shouldDefaultLedgerDimensionFromProject</span><span class="sxs-lookup"><span data-stu-id="6f271-226">CustInvoiceLine.shouldDefaultLedgerDimensionFromProject</span></span>|
|<span data-ttu-id="6f271-227">CustOutPaymRecord_Cheque.checkValues</span><span class="sxs-lookup"><span data-stu-id="6f271-227">CustOutPaymRecord_Cheque.checkValues</span></span>|
|<span data-ttu-id="6f271-228">CustPostInvoiceJob.custPostInvoiceUpdate</span><span class="sxs-lookup"><span data-stu-id="6f271-228">CustPostInvoiceJob.custPostInvoiceUpdate</span></span>|
|<span data-ttu-id="6f271-229">CustVendAgingCalculation.process</span><span class="sxs-lookup"><span data-stu-id="6f271-229">CustVendAgingCalculation.process</span></span>|
|<span data-ttu-id="6f271-230">CustVendChequeSlipTextCalculator.getChequeDocLength</span><span class="sxs-lookup"><span data-stu-id="6f271-230">CustVendChequeSlipTextCalculator.getChequeDocLength</span></span>|
|<span data-ttu-id="6f271-231">CustVendChequeSlipTextCalculator.getMinimumSlipLines</span><span class="sxs-lookup"><span data-stu-id="6f271-231">CustVendChequeSlipTextCalculator.getMinimumSlipLines</span></span>|
|<span data-ttu-id="6f271-232">CustVendChequeSlipTextCalculator.fillSlipText</span><span class="sxs-lookup"><span data-stu-id="6f271-232">CustVendChequeSlipTextCalculator.fillSlipText</span></span>|
|<span data-ttu-id="6f271-233">CustVendChequeSlipTextCalculator.Property</span><span class="sxs-lookup"><span data-stu-id="6f271-233">CustVendChequeSlipTextCalculator.Property</span></span> |
|<span data-ttu-id="6f271-234">CustVendEditTaxBranch_TH.init</span><span class="sxs-lookup"><span data-stu-id="6f271-234">CustVendEditTaxBranch_TH.init</span></span>|
|<span data-ttu-id="6f271-235">CustVendOutPaym.getSumByCurrency</span><span class="sxs-lookup"><span data-stu-id="6f271-235">CustVendOutPaym.getSumByCurrency</span></span>|
|<span data-ttu-id="6f271-236">CustVendPaymInvoiceWithJournal.createJournal</span><span class="sxs-lookup"><span data-stu-id="6f271-236">CustVendPaymInvoiceWithJournal.createJournal</span></span>|
|<span data-ttu-id="6f271-237">CustVendPaymInvoiceWithJournal.createPayment</span><span class="sxs-lookup"><span data-stu-id="6f271-237">CustVendPaymInvoiceWithJournal.createPayment</span></span>|
|<span data-ttu-id="6f271-238">CustVendPaymProposal.resolvePaymAccountAndType</span><span class="sxs-lookup"><span data-stu-id="6f271-238">CustVendPaymProposal.resolvePaymAccountAndType</span></span>|
|<span data-ttu-id="6f271-239">CustVendPaymProposalLine.paymTransactionAmountMST</span><span class="sxs-lookup"><span data-stu-id="6f271-239">CustVendPaymProposalLine.paymTransactionAmountMST</span></span>|
|<span data-ttu-id="6f271-240">CustVendPaymProposalTransferToJournal.getVoucherNum</span><span class="sxs-lookup"><span data-stu-id="6f271-240">CustVendPaymProposalTransferToJournal.getVoucherNum</span></span>|
|<span data-ttu-id="6f271-241">CustVendReversePosting.restoreCustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="6f271-241">CustVendReversePosting.restoreCustVendTransOpen</span></span>|
|<span data-ttu-id="6f271-242">CustVendSettle.postDueToAndFromCreateTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-242">CustVendSettle.postDueToAndFromCreateTrans</span></span>|
|<span data-ttu-id="6f271-243">CustVendSettle.postExchRateLedgerTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-243">CustVendSettle.postExchRateLedgerTrans</span></span>|
|<span data-ttu-id="6f271-244">CustVendSettle.settleNow</span><span class="sxs-lookup"><span data-stu-id="6f271-244">CustVendSettle.settleNow</span></span>|
|<span data-ttu-id="6f271-245">CustVendSettle.updateCustTaxInvoice_TH</span><span class="sxs-lookup"><span data-stu-id="6f271-245">CustVendSettle.updateCustTaxInvoice_TH</span></span>|
|<span data-ttu-id="6f271-246">CustVendSumUpJournal.createTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-246">CustVendSumUpJournal.createTrans</span></span>|
|<span data-ttu-id="6f271-247">CustVendSumUpJournal.createVoucher</span><span class="sxs-lookup"><span data-stu-id="6f271-247">CustVendSumUpJournal.createVoucher</span></span>|
|<span data-ttu-id="6f271-248">CustVendTransreorg.end</span><span class="sxs-lookup"><span data-stu-id="6f271-248">CustVendTransreorg.end</span></span>|
|<span data-ttu-id="6f271-249">CustVoucher.updateProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="6f271-249">CustVoucher.updateProjTransPosting</span></span>|
|<span data-ttu-id="6f271-250">DimDerDistRuleProjectRevenueExt.processRegularTransactions</span><span class="sxs-lookup"><span data-stu-id="6f271-250">DimDerDistRuleProjectRevenueExt.processRegularTransactions</span></span>|
|<span data-ttu-id="6f271-251">DimDerDistRuleProjectRevenueExt.processIntercompanyTransCustInvoice</span><span class="sxs-lookup"><span data-stu-id="6f271-251">DimDerDistRuleProjectRevenueExt.processIntercompanyTransCustInvoice</span></span>|
|<span data-ttu-id="6f271-252">DimDerDistRuleProjectRevenueExt.processIntercompanyTransExpense</span><span class="sxs-lookup"><span data-stu-id="6f271-252">DimDerDistRuleProjectRevenueExt.processIntercompanyTransExpense</span></span>|
|<span data-ttu-id="6f271-253">DimDerDistRuleProjectRevenueExt.processIntercompanyTransTimesheet</span><span class="sxs-lookup"><span data-stu-id="6f271-253">DimDerDistRuleProjectRevenueExt.processIntercompanyTransTimesheet</span></span>|
|<span data-ttu-id="6f271-254">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span><span class="sxs-lookup"><span data-stu-id="6f271-254">DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation</span></span>|
|<span data-ttu-id="6f271-255">EcoResEnumerationAttributeTypeValue.createAttributeValuesFromEnum</span><span class="sxs-lookup"><span data-stu-id="6f271-255">EcoResEnumerationAttributeTypeValue.createAttributeValuesFromEnum</span></span>|
|<span data-ttu-id="6f271-256">EcoResProductReleaseForm.addProductsToRelease</span><span class="sxs-lookup"><span data-stu-id="6f271-256">EcoResProductReleaseForm.addProductsToRelease</span></span>|
|<span data-ttu-id="6f271-257">EInvoice_IT.newCustInvoice</span><span class="sxs-lookup"><span data-stu-id="6f271-257">EInvoice_IT.newCustInvoice</span></span>|
|<span data-ttu-id="6f271-258">EInvoice_IT.newProjInvoice</span><span class="sxs-lookup"><span data-stu-id="6f271-258">EInvoice_IT.newProjInvoice</span></span>|
|<span data-ttu-id="6f271-259">EUSalesListReportingEngine.Construct</span><span class="sxs-lookup"><span data-stu-id="6f271-259">EUSalesListReportingEngine.Construct</span></span>|
|<span data-ttu-id="6f271-260">FiscalDocument_BR.lastIssueDateForSeries</span><span class="sxs-lookup"><span data-stu-id="6f271-260">FiscalDocument_BR.lastIssueDateForSeries</span></span>|
|<span data-ttu-id="6f271-261">FormletterJournalPost.docuRefCopyByRecId</span><span class="sxs-lookup"><span data-stu-id="6f271-261">FormletterJournalPost.docuRefCopyByRecId</span></span>|
|<span data-ttu-id="6f271-262">ForecastSales.Update</span><span class="sxs-lookup"><span data-stu-id="6f271-262">ForecastSales.Update</span></span>|
|<span data-ttu-id="6f271-263">HcmActionState.lookupReferenceActionTypeSetup</span><span class="sxs-lookup"><span data-stu-id="6f271-263">HcmActionState.lookupReferenceActionTypeSetup</span></span>|
|<span data-ttu-id="6f271-264">HcmWorker.init</span><span class="sxs-lookup"><span data-stu-id="6f271-264">HcmWorker.init</span></span>|
|<span data-ttu-id="6f271-265">HcmWorker.updateEmploymentControls</span><span class="sxs-lookup"><span data-stu-id="6f271-265">HcmWorker.updateEmploymentControls</span></span>|
|<span data-ttu-id="6f271-266">HcmWorkerActionHireCompletion.getHrmApplication</span><span class="sxs-lookup"><span data-stu-id="6f271-266">HcmWorkerActionHireCompletion.getHrmApplication</span></span>|
|<span data-ttu-id="6f271-267">HcmWorkerTransition.createHcmEmployment</span><span class="sxs-lookup"><span data-stu-id="6f271-267">HcmWorkerTransition.createHcmEmployment</span></span>|
|<span data-ttu-id="6f271-268">HRCCompGridView.initCompRecord</span><span class="sxs-lookup"><span data-stu-id="6f271-268">HRCCompGridView.initCompRecord</span></span>|
|<span data-ttu-id="6f271-269">HRMCompFixedEmpl.enforcePayRateTolerance</span><span class="sxs-lookup"><span data-stu-id="6f271-269">HRMCompFixedEmpl.enforcePayRateTolerance</span></span>|
|<span data-ttu-id="6f271-270">HRPDefaultSigningLimitRule.insertFormDataSourceJobDetail</span><span class="sxs-lookup"><span data-stu-id="6f271-270">HRPDefaultSigningLimitRule.insertFormDataSourceJobDetail</span></span>|
|<span data-ttu-id="6f271-271">HRPDefaultSigningLimitRule.populateDetailGrid</span><span class="sxs-lookup"><span data-stu-id="6f271-271">HRPDefaultSigningLimitRule.populateDetailGrid</span></span>|
|<span data-ttu-id="6f271-272">HRPDefaultSigningLimitRule.SaveValidation</span><span class="sxs-lookup"><span data-stu-id="6f271-272">HRPDefaultSigningLimitRule.SaveValidation</span></span>|
|<span data-ttu-id="6f271-273">HRPDefaultSigningLimitRule.insertOrUpdateFormDataSource</span><span class="sxs-lookup"><span data-stu-id="6f271-273">HRPDefaultSigningLimitRule.insertOrUpdateFormDataSource</span></span>|
|<span data-ttu-id="6f271-274">HRPDefaultSigningLimitRuleCompensation.getSelectedCompensation</span><span class="sxs-lookup"><span data-stu-id="6f271-274">HRPDefaultSigningLimitRuleCompensation.getSelectedCompensation</span></span>|
|<span data-ttu-id="6f271-275">HRPDefaultSigningLimitRuleCompensation.getAvailableCompensation</span><span class="sxs-lookup"><span data-stu-id="6f271-275">HRPDefaultSigningLimitRuleCompensation.getAvailableCompensation</span></span>|
|<span data-ttu-id="6f271-276">HRPDefaultSigningLimitRuleCompensation.selectRecords</span><span class="sxs-lookup"><span data-stu-id="6f271-276">HRPDefaultSigningLimitRuleCompensation.selectRecords</span></span>|
|<span data-ttu-id="6f271-277">HRPDefaultSigningLimitRuleCompensation.unselectRecords</span><span class="sxs-lookup"><span data-stu-id="6f271-277">HRPDefaultSigningLimitRuleCompensation.unselectRecords</span></span>|
|<span data-ttu-id="6f271-278">HrpWorkerLimit.getActiveDefaultSLRule,</span><span class="sxs-lookup"><span data-stu-id="6f271-278">HrpWorkerLimit.getActiveDefaultSLRule,</span></span> |
|<span data-ttu-id="6f271-279">HrpWorkerLimit.getDefaultSigningLimits</span><span class="sxs-lookup"><span data-stu-id="6f271-279">HrpWorkerLimit.getDefaultSigningLimits</span></span>|
|<span data-ttu-id="6f271-280">HrpWorkerLimit.getWorkerSigningLimit</span><span class="sxs-lookup"><span data-stu-id="6f271-280">HrpWorkerLimit.getWorkerSigningLimit</span></span>|
|<span data-ttu-id="6f271-281">HrpWorkerLimitr.getSigningLimitsIfRequestNotRequired</span><span class="sxs-lookup"><span data-stu-id="6f271-281">HrpWorkerLimitr.getSigningLimitsIfRequestNotRequired</span></span>|
|<span data-ttu-id="6f271-282">InterCompanyTransferInventDim.Entire クラス</span><span class="sxs-lookup"><span data-stu-id="6f271-282">InterCompanyTransferInventDim.Entire class</span></span>|
|<span data-ttu-id="6f271-283">InterCompanyTransferInventDim.transfer</span><span class="sxs-lookup"><span data-stu-id="6f271-283">InterCompanyTransferInventDim.transfer</span></span>|
|<span data-ttu-id="6f271-284">InventBatch.update</span><span class="sxs-lookup"><span data-stu-id="6f271-284">InventBatch.update</span></span>|
|<span data-ttu-id="6f271-285">InventCountCreate_Base.createInventJournalTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-285">InventCountCreate_Base.createInventJournalTrans</span></span>|
|<span data-ttu-id="6f271-286">InventInventoryDimensionEntityFieldsMapping.resolveInventDim</span><span class="sxs-lookup"><span data-stu-id="6f271-286">InventInventoryDimensionEntityFieldsMapping.resolveInventDim</span></span>|
|<span data-ttu-id="6f271-287">InventMov_Jour_BOM.journalCheckTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-287">InventMov_Jour_BOM.journalCheckTrans</span></span>|
|<span data-ttu-id="6f271-288">InventMov_Jour_Loss_Project.checkAccountOperations</span><span class="sxs-lookup"><span data-stu-id="6f271-288">InventMov_Jour_Loss_Project.checkAccountOperations</span></span>|
|<span data-ttu-id="6f271-289">InventMov_Journal.journalSetItemId</span><span class="sxs-lookup"><span data-stu-id="6f271-289">InventMov_Journal.journalSetItemId</span></span>|
|<span data-ttu-id="6f271-290">InventMov_Statement.pdsCWRemainPhysical</span><span class="sxs-lookup"><span data-stu-id="6f271-290">InventMov_Statement.pdsCWRemainPhysical</span></span>|
|<span data-ttu-id="6f271-291">InventMovement.performFinancialLedgerUpdate</span><span class="sxs-lookup"><span data-stu-id="6f271-291">InventMovement.performFinancialLedgerUpdate</span></span>|
|<span data-ttu-id="6f271-292">InventProcessGuideAdjustInController.initialStepName</span><span class="sxs-lookup"><span data-stu-id="6f271-292">InventProcessGuideAdjustInController.initialStepName</span></span>|
|<span data-ttu-id="6f271-293">InventQualityManagementBlock.run</span><span class="sxs-lookup"><span data-stu-id="6f271-293">InventQualityManagementBlock.run</span></span>|
|<span data-ttu-id="6f271-294">InventQualityManagementCreateHandler.purchFormLetterBeforeHelper</span><span class="sxs-lookup"><span data-stu-id="6f271-294">InventQualityManagementCreateHandler.purchFormLetterBeforeHelper</span></span>|
|<span data-ttu-id="6f271-295">InventQualityOrderTableValidator.checkQty</span><span class="sxs-lookup"><span data-stu-id="6f271-295">InventQualityOrderTableValidator.checkQty</span></span>|
|<span data-ttu-id="6f271-296">InventSum.retrieveMatchingInventSumDeltaForTTSId()</span><span class="sxs-lookup"><span data-stu-id="6f271-296">InventSum.retrieveMatchingInventSumDeltaForTTSId()</span></span>|
|<span data-ttu-id="6f271-297">InventTrackingRegisterTransForm.construct</span><span class="sxs-lookup"><span data-stu-id="6f271-297">InventTrackingRegisterTransForm.construct</span></span>|
|<span data-ttu-id="6f271-298">InventTransAdjust.updateNow</span><span class="sxs-lookup"><span data-stu-id="6f271-298">InventTransAdjust.updateNow</span></span>|
|<span data-ttu-id="6f271-299">InventTransferUpdReceive.updateInventTransferLine</span><span class="sxs-lookup"><span data-stu-id="6f271-299">InventTransferUpdReceive.updateInventTransferLine</span></span>|
|<span data-ttu-id="6f271-300">InventTransWms_Register.updateInventFromMovementServer</span><span class="sxs-lookup"><span data-stu-id="6f271-300">InventTransWms_Register.updateInventFromMovementServer</span></span>|
|<span data-ttu-id="6f271-301">InventUpd_ChildReference updateLess\* メソッド</span><span class="sxs-lookup"><span data-stu-id="6f271-301">InventUpd_ChildReference updateLess\* methods</span></span>|
|<span data-ttu-id="6f271-302">InventUpd_ChildReference.updateMoreIssue</span><span class="sxs-lookup"><span data-stu-id="6f271-302">InventUpd_ChildReference.updateMoreIssue</span></span>|
|<span data-ttu-id="6f271-303">InventUpd_Estimated.updateAutoDimMovement</span><span class="sxs-lookup"><span data-stu-id="6f271-303">InventUpd_Estimated.updateAutoDimMovement</span></span>|
|<span data-ttu-id="6f271-304">InventUpd_Physical.UpdatePhysicalReturnedIssue</span><span class="sxs-lookup"><span data-stu-id="6f271-304">InventUpd_Physical.UpdatePhysicalReturnedIssue</span></span>|
|<span data-ttu-id="6f271-305">InventUpd_Physical.updatePhysicalReturnedReceipt</span><span class="sxs-lookup"><span data-stu-id="6f271-305">InventUpd_Physical.updatePhysicalReturnedReceipt</span></span>|
|<span data-ttu-id="6f271-306">InventUpd_WHSReservation.continueInventTransUpdateReserveMoveLoop</span><span class="sxs-lookup"><span data-stu-id="6f271-306">InventUpd_WHSReservation.continueInventTransUpdateReserveMoveLoop</span></span>|
|<span data-ttu-id="6f271-307">InventUpdateOnhand.checkOnhand()</span><span class="sxs-lookup"><span data-stu-id="6f271-307">InventUpdateOnhand.checkOnhand()</span></span>|
|<span data-ttu-id="6f271-308">InventUpdateReserveMore.buildQueries</span><span class="sxs-lookup"><span data-stu-id="6f271-308">InventUpdateReserveMore.buildQueries</span></span>|
|<span data-ttu-id="6f271-309">JmgMESDocuHandling.openFile</span><span class="sxs-lookup"><span data-stu-id="6f271-309">JmgMESDocuHandling.openFile</span></span>|
|<span data-ttu-id="6f271-310">JmgProfiles.insertTimeGapsPlannedAbs</span><span class="sxs-lookup"><span data-stu-id="6f271-310">JmgProfiles.insertTimeGapsPlannedAbs</span></span>|
|<span data-ttu-id="6f271-311">JmgStampJournalCalculate.run</span><span class="sxs-lookup"><span data-stu-id="6f271-311">JmgStampJournalCalculate.run</span></span>|
|<span data-ttu-id="6f271-312">JmgStampJournalTransfer.cancelExecute</span><span class="sxs-lookup"><span data-stu-id="6f271-312">JmgStampJournalTransfer.cancelExecute</span></span>|
|<span data-ttu-id="6f271-313">JmgStampJournalTransfer.cancelExecute</span><span class="sxs-lookup"><span data-stu-id="6f271-313">JmgStampJournalTransfer.cancelExecute</span></span>|
|<span data-ttu-id="6f271-314">LeanCost_Init.execute</span><span class="sxs-lookup"><span data-stu-id="6f271-314">LeanCost_Init.execute</span></span>|
|<span data-ttu-id="6f271-315">LedgerAllocationController.allocateAmounts</span><span class="sxs-lookup"><span data-stu-id="6f271-315">LedgerAllocationController.allocateAmounts</span></span>|
|<span data-ttu-id="6f271-316">LedgerAllocationProcessRequest.createVoucherDestinations</span><span class="sxs-lookup"><span data-stu-id="6f271-316">LedgerAllocationProcessRequest.createVoucherDestinations</span></span>|
|<span data-ttu-id="6f271-317">LedgerJournalCheckPost.replaceTmpVoucher</span><span class="sxs-lookup"><span data-stu-id="6f271-317">LedgerJournalCheckPost.replaceTmpVoucher</span></span>|
|<span data-ttu-id="6f271-318">LedgerJournalDeleteTransaction.deleteLedgerJournalTransRelated</span><span class="sxs-lookup"><span data-stu-id="6f271-318">LedgerJournalDeleteTransaction.deleteLedgerJournalTransRelated</span></span>|
|<span data-ttu-id="6f271-319">LedgerJournalEngine.currencyModified</span><span class="sxs-lookup"><span data-stu-id="6f271-319">LedgerJournalEngine.currencyModified</span></span>|
|<span data-ttu-id="6f271-320">LedgerJournalPeriodicCopy.journalVoucherCopy</span><span class="sxs-lookup"><span data-stu-id="6f271-320">LedgerJournalPeriodicCopy.journalVoucherCopy</span></span>|
|<span data-ttu-id="6f271-321">LedgerJournalTrans.initForCurrency</span><span class="sxs-lookup"><span data-stu-id="6f271-321">LedgerJournalTrans.initForCurrency</span></span>|
|<span data-ttu-id="6f271-322">LedgerJournalTrans.validateWrite_Server</span><span class="sxs-lookup"><span data-stu-id="6f271-322">LedgerJournalTrans.validateWrite_Server</span></span>|
|<span data-ttu-id="6f271-323">LedgerTransModule.insertTransactionList</span><span class="sxs-lookup"><span data-stu-id="6f271-323">LedgerTransModule.insertTransactionList</span></span>|
|<span data-ttu-id="6f271-324">LedgerTrialBalanceContract.DataMemberAttribute</span><span class="sxs-lookup"><span data-stu-id="6f271-324">LedgerTrialBalanceContract.DataMemberAttribute</span></span>|
|<span data-ttu-id="6f271-325">LedgerVoucherObject.allocateTransaction</span><span class="sxs-lookup"><span data-stu-id="6f271-325">LedgerVoucherObject.allocateTransaction</span></span>|
|<span data-ttu-id="6f271-326">LedgerAllocationController.allocateRecursive</span><span class="sxs-lookup"><span data-stu-id="6f271-326">LedgerAllocationController.allocateRecursive</span></span>|
|<span data-ttu-id="6f271-327">MCRCheckHoldWB\Release.clicked</span><span class="sxs-lookup"><span data-stu-id="6f271-327">MCRCheckHoldWB\Release.clicked</span></span>|
|<span data-ttu-id="6f271-328">MCROrderEventSetup.find</span><span class="sxs-lookup"><span data-stu-id="6f271-328">MCROrderEventSetup.find</span></span>|
|<span data-ttu-id="6f271-329">MCRSalesOrderRecap.Control:SubmitButton.clicked</span><span class="sxs-lookup"><span data-stu-id="6f271-329">MCRSalesOrderRecap.Control:SubmitButton.clicked</span></span>|
|<span data-ttu-id="6f271-330">MCRSalesQuickQuote.Modified</span><span class="sxs-lookup"><span data-stu-id="6f271-330">MCRSalesQuickQuote.Modified</span></span>|
|<span data-ttu-id="6f271-331">MCRTmpPickingWorkbenchTrans.initFromSessionCriteria</span><span class="sxs-lookup"><span data-stu-id="6f271-331">MCRTmpPickingWorkbenchTrans.initFromSessionCriteria</span></span>|
|<span data-ttu-id="6f271-332">MultilineString.POSDeveloperSupport</span><span class="sxs-lookup"><span data-stu-id="6f271-332">MultilineString.POSDeveloperSupport</span></span>|
|<span data-ttu-id="6f271-333">OriginalDocuments.insertDocument</span><span class="sxs-lookup"><span data-stu-id="6f271-333">OriginalDocuments.insertDocument</span></span>|
|<span data-ttu-id="6f271-334">PaymSchedCalc_Amount.createTransaction</span><span class="sxs-lookup"><span data-stu-id="6f271-334">PaymSchedCalc_Amount.createTransaction</span></span>|
|<span data-ttu-id="6f271-335">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim</span><span class="sxs-lookup"><span data-stu-id="6f271-335">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim</span></span>|
|<span data-ttu-id="6f271-336">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim()</span><span class="sxs-lookup"><span data-stu-id="6f271-336">PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim()</span></span>|
|<span data-ttu-id="6f271-337">PdsRebatePaymentPost.insertRebateEntryForGrouping</span><span class="sxs-lookup"><span data-stu-id="6f271-337">PdsRebatePaymentPost.insertRebateEntryForGrouping</span></span>|
|<span data-ttu-id="6f271-338">PmfFormCtrl_BOM_BOMVersion.modifiedFormulaSize</span><span class="sxs-lookup"><span data-stu-id="6f271-338">PmfFormCtrl_BOM_BOMVersion.modifiedFormulaSize</span></span>|
|<span data-ttu-id="6f271-339">PriceDiscAdmCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="6f271-339">PriceDiscAdmCheckPost.postJournal</span></span>|
|<span data-ttu-id="6f271-340">ProdJournalCheckPostProd.postTransLedger</span><span class="sxs-lookup"><span data-stu-id="6f271-340">ProdJournalCheckPostProd.postTransLedger</span></span>|
|<span data-ttu-id="6f271-341">ProdJournalTransBOM.inventBatchId.validate</span><span class="sxs-lookup"><span data-stu-id="6f271-341">ProdJournalTransBOM.inventBatchId.validate</span></span>|
|<span data-ttu-id="6f271-342">ProdMultiReportFinished.insert</span><span class="sxs-lookup"><span data-stu-id="6f271-342">ProdMultiReportFinished.insert</span></span>|
|<span data-ttu-id="6f271-343">ProdUPDCostEstimation.CreateProdBOM</span><span class="sxs-lookup"><span data-stu-id="6f271-343">ProdUPDCostEstimation.CreateProdBOM</span></span>|
|<span data-ttu-id="6f271-344">ProdUpdReportFinished.updateBOMConsumption</span><span class="sxs-lookup"><span data-stu-id="6f271-344">ProdUpdReportFinished.updateBOMConsumption</span></span>|
|<span data-ttu-id="6f271-345">ProdUpdStartUp.createJournals</span><span class="sxs-lookup"><span data-stu-id="6f271-345">ProdUpdStartUp.createJournals</span></span>|
|<span data-ttu-id="6f271-346">ProjBegBalJournalTrans_CostSales.validateField, validateWrite</span><span class="sxs-lookup"><span data-stu-id="6f271-346">ProjBegBalJournalTrans_CostSales.validateField, validateWrite</span></span>|
|<span data-ttu-id="6f271-347">ProjBudgetManager.deleteBudgetLinesBeforeImportForRevs</span><span class="sxs-lookup"><span data-stu-id="6f271-347">ProjBudgetManager.deleteBudgetLinesBeforeImportForRevs</span></span>|
|<span data-ttu-id="6f271-348">ProjBudgetManager.getQuery</span><span class="sxs-lookup"><span data-stu-id="6f271-348">ProjBudgetManager.getQuery</span></span>|
|<span data-ttu-id="6f271-349">ProjBudgetRevisionManager.createBudgetLines</span><span class="sxs-lookup"><span data-stu-id="6f271-349">ProjBudgetRevisionManager.createBudgetLines</span></span>|
|<span data-ttu-id="6f271-350">ProjBudgetTransactionManager.isOverrunAllowed</span><span class="sxs-lookup"><span data-stu-id="6f271-350">ProjBudgetTransactionManager.isOverrunAllowed</span></span>|
|<span data-ttu-id="6f271-351">ProjectCommitmentFacade.updateProjectCommitmentsMap</span><span class="sxs-lookup"><span data-stu-id="6f271-351">ProjectCommitmentFacade.updateProjectCommitmentsMap</span></span>|
|<span data-ttu-id="6f271-352">ProjectMainAccDimensionListProvider.populateMainAccountDimensionList</span><span class="sxs-lookup"><span data-stu-id="6f271-352">ProjectMainAccDimensionListProvider.populateMainAccountDimensionList</span></span>|
|<span data-ttu-id="6f271-353">ProjForecastBudgetCopy.do_Cost</span><span class="sxs-lookup"><span data-stu-id="6f271-353">ProjForecastBudgetCopy.do_Cost</span></span>|
|<span data-ttu-id="6f271-354">ProjForecastBudgetCopy.do_empl</span><span class="sxs-lookup"><span data-stu-id="6f271-354">ProjForecastBudgetCopy.do_empl</span></span>|
|<span data-ttu-id="6f271-355">ProjForecastBudgetCopy.do_onAcc</span><span class="sxs-lookup"><span data-stu-id="6f271-355">ProjForecastBudgetCopy.do_onAcc</span></span>|
|<span data-ttu-id="6f271-356">ProjForecastBudgetCopy.do_sales</span><span class="sxs-lookup"><span data-stu-id="6f271-356">ProjForecastBudgetCopy.do_sales</span></span>|
|<span data-ttu-id="6f271-357">ProjGroupChange.checkPostedTrxAccounts</span><span class="sxs-lookup"><span data-stu-id="6f271-357">ProjGroupChange.checkPostedTrxAccounts</span></span>|
|<span data-ttu-id="6f271-358">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="6f271-358">ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine</span></span>|
|<span data-ttu-id="6f271-359">ProjInvoiceJournalPost.postCustVend</span><span class="sxs-lookup"><span data-stu-id="6f271-359">ProjInvoiceJournalPost.postCustVend</span></span>|
|<span data-ttu-id="6f271-360">ProjInvoiceJournalPost.validateNoTax</span><span class="sxs-lookup"><span data-stu-id="6f271-360">ProjInvoiceJournalPost.validateNoTax</span></span>|
|<span data-ttu-id="6f271-361">ProjInvoiceProposalInsertLines.run</span><span class="sxs-lookup"><span data-stu-id="6f271-361">ProjInvoiceProposalInsertLines.run</span></span>|
|<span data-ttu-id="6f271-362">ProjJournalTrans.validateWrite</span><span class="sxs-lookup"><span data-stu-id="6f271-362">ProjJournalTrans.validateWrite</span></span>|
|<span data-ttu-id="6f271-363">ProjPlanVersionCopyHierarchy.addProjPlanVersionFields</span><span class="sxs-lookup"><span data-stu-id="6f271-363">ProjPlanVersionCopyHierarchy.addProjPlanVersionFields</span></span>|
|<span data-ttu-id="6f271-364">ProjPlanVersionCopyHierarchy.insertProjPlanVersionRecords</span><span class="sxs-lookup"><span data-stu-id="6f271-364">ProjPlanVersionCopyHierarchy.insertProjPlanVersionRecords</span></span>|
|<span data-ttu-id="6f271-365">ProjPlanVersionCopyHierarchy.ProjPlanVersionCopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="6f271-365">ProjPlanVersionCopyHierarchy.ProjPlanVersionCopyHierarchy</span></span>|
|<span data-ttu-id="6f271-366">ProjPlanVersionsManager.importProjPlanVersionRecords</span><span class="sxs-lookup"><span data-stu-id="6f271-366">ProjPlanVersionsManager.importProjPlanVersionRecords</span></span>|
|<span data-ttu-id="6f271-367">ProjPost.PostNeverLedger</span><span class="sxs-lookup"><span data-stu-id="6f271-367">ProjPost.PostNeverLedger</span></span>|
|<span data-ttu-id="6f271-368">ProjPost.PostTurnover</span><span class="sxs-lookup"><span data-stu-id="6f271-368">ProjPost.PostTurnover</span></span>|
|<span data-ttu-id="6f271-369">ProjPosting.updateDatasourceRanges</span><span class="sxs-lookup"><span data-stu-id="6f271-369">ProjPosting.updateDatasourceRanges</span></span>|
|<span data-ttu-id="6f271-370">ProjTable.validateWrite</span><span class="sxs-lookup"><span data-stu-id="6f271-370">ProjTable.validateWrite</span></span>|
|<span data-ttu-id="6f271-371">ProjTable.validateWriteServer</span><span class="sxs-lookup"><span data-stu-id="6f271-371">ProjTable.validateWriteServer</span></span>|
|<span data-ttu-id="6f271-372">ProjTask.addTask</span><span class="sxs-lookup"><span data-stu-id="6f271-372">ProjTask.addTask</span></span>|
|<span data-ttu-id="6f271-373">ProjValSetupEmplProj.ProjValSetupEmplProj.AddResourceButton.Click</span><span class="sxs-lookup"><span data-stu-id="6f271-373">ProjValSetupEmplProj.ProjValSetupEmplProj.AddResourceButton.Click</span></span>|
|<span data-ttu-id="6f271-374">ProjWBSDataEntityHelper.postInsertOperation</span><span class="sxs-lookup"><span data-stu-id="6f271-374">ProjWBSDataEntityHelper.postInsertOperation</span></span>|
|<span data-ttu-id="6f271-375">PurchAutoCreate_ReleaseFromAgreement.createLines</span><span class="sxs-lookup"><span data-stu-id="6f271-375">PurchAutoCreate_ReleaseFromAgreement.createLines</span></span>|
|<span data-ttu-id="6f271-376">PurchInvoiceJournalPost.calcLastPurchPrice</span><span class="sxs-lookup"><span data-stu-id="6f271-376">PurchInvoiceJournalPost.calcLastPurchPrice</span></span>|
|<span data-ttu-id="6f271-377">PurchPackingSlipJournalPost.updateSourceLineBeforePosting</span><span class="sxs-lookup"><span data-stu-id="6f271-377">PurchPackingSlipJournalPost.updateSourceLineBeforePosting</span></span>|
|<span data-ttu-id="6f271-378">PurchReqLine.defaultBuyingLegalEntity</span><span class="sxs-lookup"><span data-stu-id="6f271-378">PurchReqLine.defaultBuyingLegalEntity</span></span>|
|<span data-ttu-id="6f271-379">PurchRFQCaseAutoCreate_PurchReq.calcRFQHeaderValues</span><span class="sxs-lookup"><span data-stu-id="6f271-379">PurchRFQCaseAutoCreate_PurchReq.calcRFQHeaderValues</span></span>|
|<span data-ttu-id="6f271-380">PurchTable/InventDim/InventBatchId.modified</span><span class="sxs-lookup"><span data-stu-id="6f271-380">PurchTable/InventDim/InventBatchId.modified</span></span>|
|<span data-ttu-id="6f271-381">ReqTransPoMarkFirm.executeAction</span><span class="sxs-lookup"><span data-stu-id="6f271-381">ReqTransPoMarkFirm.executeAction</span></span>|
|<span data-ttu-id="6f271-382">ReqTransPOMarkFirm.CreateProdBOM</span><span class="sxs-lookup"><span data-stu-id="6f271-382">ReqTransPOMarkFirm.CreateProdBOM</span></span>|
|<span data-ttu-id="6f271-383">ReqTransPoMarkFirm.purchTablePostProcessing</span><span class="sxs-lookup"><span data-stu-id="6f271-383">ReqTransPoMarkFirm.purchTablePostProcessing</span></span>|
|<span data-ttu-id="6f271-384">ReqTransPoMarkFirm.setDeliveryDateAndPriceDisc</span><span class="sxs-lookup"><span data-stu-id="6f271-384">ReqTransPoMarkFirm.setDeliveryDateAndPriceDisc</span></span>|
|<span data-ttu-id="6f271-385">ReqTransPoMarkFirm.setGroupingIndicators</span><span class="sxs-lookup"><span data-stu-id="6f271-385">ReqTransPoMarkFirm.setGroupingIndicators</span></span>|
|<span data-ttu-id="6f271-386">RequisitionPurchaseOrderGeneration.Create</span><span class="sxs-lookup"><span data-stu-id="6f271-386">RequisitionPurchaseOrderGeneration.Create</span></span>|
|<span data-ttu-id="6f271-387">RequisitionPurchaseOrderGeneration.createPurch</span><span class="sxs-lookup"><span data-stu-id="6f271-387">RequisitionPurchaseOrderGeneration.createPurch</span></span>|
|<span data-ttu-id="6f271-388">RequisitionPurchaseOrderGeneration.getVendors</span><span class="sxs-lookup"><span data-stu-id="6f271-388">RequisitionPurchaseOrderGeneration.getVendors</span></span>|
|<span data-ttu-id="6f271-389">ResReserveCapacity.getCapacityPercentage</span><span class="sxs-lookup"><span data-stu-id="6f271-389">ResReserveCapacity.getCapacityPercentage</span></span>|
|<span data-ttu-id="6f271-390">RetailCreateLinesFromProductsToAdd.loadDiscountLines</span><span class="sxs-lookup"><span data-stu-id="6f271-390">RetailCreateLinesFromProductsToAdd.loadDiscountLines</span></span>|
|<span data-ttu-id="6f271-391">RetailMassUpdateValidator.validateWriteOnInventModelGroupItem</span><span class="sxs-lookup"><span data-stu-id="6f271-391">RetailMassUpdateValidator.validateWriteOnInventModelGroupItem</span></span>|
|<span data-ttu-id="6f271-392">RetailMediaAssociationHelper.populateMediaAssociationTable</span><span class="sxs-lookup"><span data-stu-id="6f271-392">RetailMediaAssociationHelper.populateMediaAssociationTable</span></span>|
|<span data-ttu-id="6f271-393">RetailOENInfo.parseEmailTemplate</span><span class="sxs-lookup"><span data-stu-id="6f271-393">RetailOENInfo.parseEmailTemplate</span></span>|
|<span data-ttu-id="6f271-394">RetailPrintLabels.loadFromArgs</span><span class="sxs-lookup"><span data-stu-id="6f271-394">RetailPrintLabels.loadFromArgs</span></span>|
|<span data-ttu-id="6f271-395">RetailPrintLabels.loadLines</span><span class="sxs-lookup"><span data-stu-id="6f271-395">RetailPrintLabels.loadLines</span></span>|
|<span data-ttu-id="6f271-396">RetailTransactionServiceOrders.createOrUpdateRetailOrderHeader</span><span class="sxs-lookup"><span data-stu-id="6f271-396">RetailTransactionServiceOrders.createOrUpdateRetailOrderHeader</span></span>|
|<span data-ttu-id="6f271-397">RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span><span class="sxs-lookup"><span data-stu-id="6f271-397">RetailTransactionServiceOrders.createOrUpdateRetailOrderLines</span></span>|
|<span data-ttu-id="6f271-398">SalesConfirmJournalPost.createReportData</span><span class="sxs-lookup"><span data-stu-id="6f271-398">SalesConfirmJournalPost.createReportData</span></span>|
|<span data-ttu-id="6f271-399">SalesFormLetter_Invoice.checkInvoicePrices</span><span class="sxs-lookup"><span data-stu-id="6f271-399">SalesFormLetter_Invoice.checkInvoicePrices</span></span>|
|<span data-ttu-id="6f271-400">SalesInvoiceDP.setPackingSlipDetails</span><span class="sxs-lookup"><span data-stu-id="6f271-400">SalesInvoiceDP.setPackingSlipDetails</span></span>|
|<span data-ttu-id="6f271-401">SalesInvoiceJournalPostBase.updateInventory</span><span class="sxs-lookup"><span data-stu-id="6f271-401">SalesInvoiceJournalPostBase.updateInventory</span></span>|
|<span data-ttu-id="6f271-402">SalesInvoiceJournalPostBase.updateInventoryFinancialForSalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="6f271-402">SalesInvoiceJournalPostBase.updateInventoryFinancialForSalesInvoiceLine</span></span>|
|<span data-ttu-id="6f271-403">SalesLine.CheckItemId</span><span class="sxs-lookup"><span data-stu-id="6f271-403">SalesLine.CheckItemId</span></span>|
|<span data-ttu-id="6f271-404">SalesLine.getInventQtyFromCWUnit</span><span class="sxs-lookup"><span data-stu-id="6f271-404">SalesLine.getInventQtyFromCWUnit</span></span>|
|<span data-ttu-id="6f271-405">SalesLine.setInventDeliverNow</span><span class="sxs-lookup"><span data-stu-id="6f271-405">SalesLine.setInventDeliverNow</span></span>|
|<span data-ttu-id="6f271-406">SalesLineType.validateWrite</span><span class="sxs-lookup"><span data-stu-id="6f271-406">SalesLineType.validateWrite</span></span>|
|<span data-ttu-id="6f271-407">SalesQuotationDP.createTaxLines</span><span class="sxs-lookup"><span data-stu-id="6f271-407">SalesQuotationDP.createTaxLines</span></span>|
|<span data-ttu-id="6f271-408">SalesQuotationDP.itemId</span><span class="sxs-lookup"><span data-stu-id="6f271-408">SalesQuotationDP.itemId</span></span>|
|<span data-ttu-id="6f271-409">SalesQuotationLine.PriceDate</span><span class="sxs-lookup"><span data-stu-id="6f271-409">SalesQuotationLine.PriceDate</span></span>|
|<span data-ttu-id="6f271-410">SalesQuotationTable.active</span><span class="sxs-lookup"><span data-stu-id="6f271-410">SalesQuotationTable.active</span></span>|
|<span data-ttu-id="6f271-411">SalesTable-DataSource_mcrSalesTable-DataField_SourceId.modified</span><span class="sxs-lookup"><span data-stu-id="6f271-411">SalesTable-DataSource_mcrSalesTable-DataField_SourceId.modified</span></span>|
|<span data-ttu-id="6f271-412">ShipOrderForm.POS.ChangeOriginOnShipOrders</span><span class="sxs-lookup"><span data-stu-id="6f271-412">ShipOrderForm.POS.ChangeOriginOnShipOrders</span></span>|
|<span data-ttu-id="6f271-413">SmabomDesignerCtrl.listInsertHistory</span><span class="sxs-lookup"><span data-stu-id="6f271-413">SmabomDesignerCtrl.listInsertHistory</span></span>|
|<span data-ttu-id="6f271-414">SmabomDesignerCtrl.treeSubstituteBOMonNode, treeDeleteNode, treeDeleteChildrenCollect</span><span class="sxs-lookup"><span data-stu-id="6f271-414">SmabomDesignerCtrl.treeSubstituteBOMonNode, treeDeleteNode, treeDeleteChildrenCollect</span></span>|
|<span data-ttu-id="6f271-415">SMAServiceObjectrelation.jumpRefBOMTable</span><span class="sxs-lookup"><span data-stu-id="6f271-415">SMAServiceObjectrelation.jumpRefBOMTable</span></span>|
|<span data-ttu-id="6f271-416">SubledgerJournalizerProjectExtension.createProjectActualCostDetail</span><span class="sxs-lookup"><span data-stu-id="6f271-416">SubledgerJournalizerProjectExtension.createProjectActualCostDetail</span></span>|
|<span data-ttu-id="6f271-417">SubledgerJournalizerProjectExtension.createProjectActualSalesDetail</span><span class="sxs-lookup"><span data-stu-id="6f271-417">SubledgerJournalizerProjectExtension.createProjectActualSalesDetail</span></span>|
|<span data-ttu-id="6f271-418">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelated</span><span class="sxs-lookup"><span data-stu-id="6f271-418">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelated</span></span>|
|<span data-ttu-id="6f271-419">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span><span class="sxs-lookup"><span data-stu-id="6f271-419">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span></span>|
|<span data-ttu-id="6f271-420">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span><span class="sxs-lookup"><span data-stu-id="6f271-420">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail</span></span>|
|<span data-ttu-id="6f271-421">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span><span class="sxs-lookup"><span data-stu-id="6f271-421">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span></span>|
|<span data-ttu-id="6f271-422">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span><span class="sxs-lookup"><span data-stu-id="6f271-422">SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedSummarized</span></span>|
|<span data-ttu-id="6f271-423">SubledgerJournalTransferCommand.insertGeneralJournalEntryRelated</span><span class="sxs-lookup"><span data-stu-id="6f271-423">SubledgerJournalTransferCommand.insertGeneralJournalEntryRelated</span></span>|
|<span data-ttu-id="6f271-424">SuppItem.calcSuppItem</span><span class="sxs-lookup"><span data-stu-id="6f271-424">SuppItem.calcSuppItem</span></span>|
|<span data-ttu-id="6f271-425">TaxProformaSpec.parmTaxSpec</span><span class="sxs-lookup"><span data-stu-id="6f271-425">TaxProformaSpec.parmTaxSpec</span></span>|
|<span data-ttu-id="6f271-426">TaxWithhold.postTaxWithhold</span><span class="sxs-lookup"><span data-stu-id="6f271-426">TaxWithhold.postTaxWithhold</span></span>|
|<span data-ttu-id="6f271-427">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span><span class="sxs-lookup"><span data-stu-id="6f271-427">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span></span>|
|<span data-ttu-id="6f271-428">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span><span class="sxs-lookup"><span data-stu-id="6f271-428">TaxWithholdSlipDP_TH.createTaxWithholdSlipTmp</span></span>|
|<span data-ttu-id="6f271-429">TmsProcessXML_Base.readRateShipment</span><span class="sxs-lookup"><span data-stu-id="6f271-429">TmsProcessXML_Base.readRateShipment</span></span>|
|<span data-ttu-id="6f271-430">TMSRouteHelper.getShipDates</span><span class="sxs-lookup"><span data-stu-id="6f271-430">TMSRouteHelper.getShipDates</span></span>|
|<span data-ttu-id="6f271-431">TradeLineNumberManager.checkLineNumber</span><span class="sxs-lookup"><span data-stu-id="6f271-431">TradeLineNumberManager.checkLineNumber</span></span>|
|<span data-ttu-id="6f271-432">TrvCreditCardReminder.mail</span><span class="sxs-lookup"><span data-stu-id="6f271-432">TrvCreditCardReminder.mail</span></span> |
|<span data-ttu-id="6f271-433">TrvCreditCardReminder.runQT</span><span class="sxs-lookup"><span data-stu-id="6f271-433">TrvCreditCardReminder.runQT</span></span>|
|<span data-ttu-id="6f271-434">TrvExpenditureParticipantProvider.resolveFromDimensions</span><span class="sxs-lookup"><span data-stu-id="6f271-434">TrvExpenditureParticipantProvider.resolveFromDimensions</span></span>|
|<span data-ttu-id="6f271-435">TrvExpenditureParticipantProvider.resolve</span><span class="sxs-lookup"><span data-stu-id="6f271-435">TrvExpenditureParticipantProvider.resolve</span></span>|
|<span data-ttu-id="6f271-436">TrvExpenditureParticipantProvider.resolveProjectAuthorities</span><span class="sxs-lookup"><span data-stu-id="6f271-436">TrvExpenditureParticipantProvider.resolveProjectAuthorities</span></span>|
|<span data-ttu-id="6f271-437">TrvExpenses.openSplitDetailsForm</span><span class="sxs-lookup"><span data-stu-id="6f271-437">TrvExpenses.openSplitDetailsForm</span></span>|
|<span data-ttu-id="6f271-438">TrvExpTable.validateSubmit</span><span class="sxs-lookup"><span data-stu-id="6f271-438">TrvExpTable.validateSubmit</span></span>|
|<span data-ttu-id="6f271-439">VendAgingReportController.getReportName</span><span class="sxs-lookup"><span data-stu-id="6f271-439">VendAgingReportController.getReportName</span></span>|
|<span data-ttu-id="6f271-440">VendBalanceList.insertIntoTmpAccountSum</span><span class="sxs-lookup"><span data-stu-id="6f271-440">VendBalanceList.insertIntoTmpAccountSum</span></span>|
|<span data-ttu-id="6f271-441">VendInvoiceInfoListPage.postInvoice</span><span class="sxs-lookup"><span data-stu-id="6f271-441">VendInvoiceInfoListPage.postInvoice</span></span>|
|<span data-ttu-id="6f271-442">VendOutPaymRecord_Cheque.checkValues</span><span class="sxs-lookup"><span data-stu-id="6f271-442">VendOutPaymRecord_Cheque.checkValues</span></span>|
|<span data-ttu-id="6f271-443">VendVendorEntity/VendVendorV2Entity.processChangesForApproval</span><span class="sxs-lookup"><span data-stu-id="6f271-443">VendVendorEntity/VendVendorV2Entity.processChangesForApproval</span></span>|
|<span data-ttu-id="6f271-444">VestingID.Table: HRMCompVarAward</span><span class="sxs-lookup"><span data-stu-id="6f271-444">VestingID.Table: HRMCompVarAward</span></span>|
|<span data-ttu-id="6f271-445">WhsContainerization.packTmpWorkLine</span><span class="sxs-lookup"><span data-stu-id="6f271-445">WhsContainerization.packTmpWorkLine</span></span>|
|<span data-ttu-id="6f271-446">WhsControlBatchId.process</span><span class="sxs-lookup"><span data-stu-id="6f271-446">WhsControlBatchId.process</span></span>|
|<span data-ttu-id="6f271-447">WHSPostPackingSlip.canShipConfirm</span><span class="sxs-lookup"><span data-stu-id="6f271-447">WHSPostPackingSlip.canShipConfirm</span></span>|
|<span data-ttu-id="6f271-448">WHSPostPackingSlip.shipConfirmLoad</span><span class="sxs-lookup"><span data-stu-id="6f271-448">WHSPostPackingSlip.shipConfirmLoad</span></span>|
|<span data-ttu-id="6f271-449">WHSProcessGuideStartChangeWarehouseStep.doExecute</span><span class="sxs-lookup"><span data-stu-id="6f271-449">WHSProcessGuideStartChangeWarehouseStep.doExecute</span></span>|
|<span data-ttu-id="6f271-450">WhsrfControlData.batchExistInLocation</span><span class="sxs-lookup"><span data-stu-id="6f271-450">WhsrfControlData.batchExistInLocation</span></span>|
|<span data-ttu-id="6f271-451">WhsShipConfirm.tmsMultiLoadShipConfirm</span><span class="sxs-lookup"><span data-stu-id="6f271-451">WhsShipConfirm.tmsMultiLoadShipConfirm</span></span>|
|<span data-ttu-id="6f271-452">WHSSplitWork.handleOrignalWorkLine</span><span class="sxs-lookup"><span data-stu-id="6f271-452">WHSSplitWork.handleOrignalWorkLine</span></span>|
|<span data-ttu-id="6f271-453">WHSSplitWork.handleRemainingPickTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-453">WHSSplitWork.handleRemainingPickTrans</span></span>|
|<span data-ttu-id="6f271-454">WHSSplitWork.processRemainingTransaction</span><span class="sxs-lookup"><span data-stu-id="6f271-454">WHSSplitWork.processRemainingTransaction</span></span>|
|<span data-ttu-id="6f271-455">WHSSplitWork.updateClosedPickTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-455">WHSSplitWork.updateClosedPickTrans</span></span>|
|<span data-ttu-id="6f271-456">WhsUnShip.cleanUpTOInventTransDims</span><span class="sxs-lookup"><span data-stu-id="6f271-456">WhsUnShip.cleanUpTOInventTransDims</span></span>|
|<span data-ttu-id="6f271-457">WhsWarehouseRelease.createShipmentsForTransferOrders</span><span class="sxs-lookup"><span data-stu-id="6f271-457">WhsWarehouseRelease.createShipmentsForTransferOrders</span></span>|
|<span data-ttu-id="6f271-458">WHSWorkCreate.createWorkInventTrans</span><span class="sxs-lookup"><span data-stu-id="6f271-458">WHSWorkCreate.createWorkInventTrans</span></span>|
|<span data-ttu-id="6f271-459">WHSWorkCreate.createWorkTable</span><span class="sxs-lookup"><span data-stu-id="6f271-459">WHSWorkCreate.createWorkTable</span></span>|
|<span data-ttu-id="6f271-460">WhsWorkCreateProdPut.createReportFinished</span><span class="sxs-lookup"><span data-stu-id="6f271-460">WhsWorkCreateProdPut.createReportFinished</span></span>|
|<span data-ttu-id="6f271-461">WhsWorkCreateReceiving.createBatch</span><span class="sxs-lookup"><span data-stu-id="6f271-461">WhsWorkCreateReceiving.createBatch</span></span>|
|<span data-ttu-id="6f271-462">WHSWorkExecute.putAwayToLocation()</span><span class="sxs-lookup"><span data-stu-id="6f271-462">WHSWorkExecute.putAwayToLocation()</span></span>|
|<span data-ttu-id="6f271-463">WHSWorkExecuteDisplay.buildInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="6f271-463">WHSWorkExecuteDisplay.buildInventoryStatus</span></span>|
|<span data-ttu-id="6f271-464">WhsWorkExecuteDisplay.getNextFormState</span><span class="sxs-lookup"><span data-stu-id="6f271-464">WhsWorkExecuteDisplay.getNextFormState</span></span>|
|<span data-ttu-id="6f271-465">WhsWorkExecuteDisplay.processTrackingDimDetails</span><span class="sxs-lookup"><span data-stu-id="6f271-465">WhsWorkExecuteDisplay.processTrackingDimDetails</span></span>|
|<span data-ttu-id="6f271-466">WhsWorkExecuteDisplay.processVendorBatchDetails</span><span class="sxs-lookup"><span data-stu-id="6f271-466">WhsWorkExecuteDisplay.processVendorBatchDetails</span></span>|
|<span data-ttu-id="6f271-467">WhsWorkExecuteDisplay.processWorkLine</span><span class="sxs-lookup"><span data-stu-id="6f271-467">WhsWorkExecuteDisplay.processWorkLine</span></span>|
|<span data-ttu-id="6f271-468">WHSWorkExecuteDisplay.setBatchDetails</span><span class="sxs-lookup"><span data-stu-id="6f271-468">WHSWorkExecuteDisplay.setBatchDetails</span></span>|
|<span data-ttu-id="6f271-469">WhsWorkExecuteDisplayLoadItemReceiving.buildPOReceiving</span><span class="sxs-lookup"><span data-stu-id="6f271-469">WhsWorkExecuteDisplayLoadItemReceiving.buildPOReceiving</span></span>|
|<span data-ttu-id="6f271-470">WHSWorkExecuteDisplayLPReceiving.generateItemInfoForReceiving</span><span class="sxs-lookup"><span data-stu-id="6f271-470">WHSWorkExecuteDisplayLPReceiving.generateItemInfoForReceiving</span></span>|
|<span data-ttu-id="6f271-471">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span><span class="sxs-lookup"><span data-stu-id="6f271-471">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span></span>|
|<span data-ttu-id="6f271-472">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span><span class="sxs-lookup"><span data-stu-id="6f271-472">WhsWorkExecuteDisplayPOLineReceiving.buildPOReceiving</span></span>|
|<span data-ttu-id="6f271-473">WhsWorkExecuteDisplayReportAsFinished.displayForm</span><span class="sxs-lookup"><span data-stu-id="6f271-473">WhsWorkExecuteDisplayReportAsFinished.displayForm</span></span>|
|<span data-ttu-id="6f271-474">WHSWorkTable.satisfyDemandWorkLine</span><span class="sxs-lookup"><span data-stu-id="6f271-474">WHSWorkTable.satisfyDemandWorkLine</span></span>|
|<span data-ttu-id="6f271-475">WmsArrivalCreateJournal.createWMSJournalTransFromArrivalDetails</span><span class="sxs-lookup"><span data-stu-id="6f271-475">WmsArrivalCreateJournal.createWMSJournalTransFromArrivalDetails</span></span>|
|<span data-ttu-id="6f271-476">WmsJournalCheckPostReception.returnOrderUpdate</span><span class="sxs-lookup"><span data-stu-id="6f271-476">WmsJournalCheckPostReception.returnOrderUpdate</span></span>|
|<span data-ttu-id="6f271-477">WmsOrderCreate.updateCreatewmsOrder</span><span class="sxs-lookup"><span data-stu-id="6f271-477">WmsOrderCreate.updateCreatewmsOrder</span></span>|
|<span data-ttu-id="6f271-478">WorkflowHierarchyProviderHelperEventHandler.addDataSourceFieldsDelegate</span><span class="sxs-lookup"><span data-stu-id="6f271-478">WorkflowHierarchyProviderHelperEventHandler.addDataSourceFieldsDelegate</span></span>|
|<span data-ttu-id="6f271-479">WorkflowHierarchyProviderHelperEventHandler.loadLimits</span><span class="sxs-lookup"><span data-stu-id="6f271-479">WorkflowHierarchyProviderHelperEventHandler.loadLimits</span></span>|
|<span data-ttu-id="6f271-480">WrkCtrScheduler_Prod.saveOperation</span><span class="sxs-lookup"><span data-stu-id="6f271-480">WrkCtrScheduler_Prod.saveOperation</span></span>|

## <a name="other-changes"></a><span data-ttu-id="6f271-481">その他の変更</span><span class="sxs-lookup"><span data-stu-id="6f271-481">Other changes</span></span>

<span data-ttu-id="6f271-482">次の追加の変更が、拡張機能に対して行われました。</span><span class="sxs-lookup"><span data-stu-id="6f271-482">The following additional changes have been made for extensibility.</span></span>

- <span data-ttu-id="6f271-483">InventSumFields が使用されているクエリを SysDa に変換します。</span><span class="sxs-lookup"><span data-stu-id="6f271-483">Convert queries where InventSumFields is used to SysDa.</span></span>

