---
title: Dynamics 365 for Finance and Operations バージョン 10.0.3 の拡張機能の変更
description: これのトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 に実装された拡張機能を一覧します。
author: FrankDahl
manager: AnnBe
ms.date: 06/14/2019
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
ms.search.validFrom: 2019-05-10
ms.dyn365.ops.version: App 10.0
ms.openlocfilehash: 8520b31123425afde0876d2de2b06852c377e6be
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409346"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-1003"></a><span data-ttu-id="6bb3d-103">Dynamics 365 for Finance and Operations バージョン 10.0.3 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="6bb3d-103">Extensibility changes in Dynamics 365 for Finance and Operations version 10.0.3</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bb3d-104">これのトピックでは、 Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 にて実装された拡張機能を記載しています。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-104">This topic lists the extensibility features that were implemented in Microsoft Dynamics 365 for Finance and Operations version 10.0.3.</span></span> <span data-ttu-id="6bb3d-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="enumerations-made-extensible"></a><span data-ttu-id="6bb3d-106">拡張可能になった列挙</span><span class="sxs-lookup"><span data-stu-id="6bb3d-106">Enumerations made extensible</span></span>

<span data-ttu-id="6bb3d-107">今回のアップデートで実装された拡張を以下に記載します。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-107">The following enumerations have been made extensible in this update:</span></span>

- <span data-ttu-id="6bb3d-108">LedgerJournalWFApprovalModule</span><span class="sxs-lookup"><span data-stu-id="6bb3d-108">LedgerJournalWFApprovalModule</span></span>
- <span data-ttu-id="6bb3d-109">RetailReceiptTransaction</span><span class="sxs-lookup"><span data-stu-id="6bb3d-109">RetailReceiptTransaction</span></span>

## <a name="sql-operations-made-extensible"></a><span data-ttu-id="6bb3d-110">拡張可能になった SQL 操作</span><span class="sxs-lookup"><span data-stu-id="6bb3d-110">SQL operations made extensible</span></span>

<span data-ttu-id="6bb3d-111">今回のアップデートでは、以下のSQL操作が拡張されました。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-111">The following SQL operations have been made extensible in this update:</span></span>

- <span data-ttu-id="6bb3d-112">拡張可能マップパターンにむけた CustVendTrans の実装</span><span class="sxs-lookup"><span data-stu-id="6bb3d-112">CustVendTrans support for an extensible map pattern</span></span>

## <a name="metadata-changes"></a><span data-ttu-id="6bb3d-113">メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="6bb3d-113">Metadata changes</span></span>

<span data-ttu-id="6bb3d-114">今回のアップデートで以下のメタデータが更新されました。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-114">The following metadata changes have been made in this update:</span></span>

- <span data-ttu-id="6bb3d-115">CostSheetAmount.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="6bb3d-115">CostSheetAmount.NoOfDecimalsIsExtensible</span></span>
- <span data-ttu-id="6bb3d-116">SalesLinePercent.NoOfDecimalsIsExtensible</span><span class="sxs-lookup"><span data-stu-id="6bb3d-116">SalesLinePercent.NoOfDecimalsIsExtensible</span></span>

## <a name="refactored-methods"></a><span data-ttu-id="6bb3d-117">リファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="6bb3d-117">Refactored methods</span></span>

<span data-ttu-id="6bb3d-118">拡張性をサポートするために、以下のメソッドがリファクターされました。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-118">The following methods have been refactored to support extensibility:</span></span>

- <span data-ttu-id="6bb3d-119">BankReconciliationDataInitializer.initDocumentOpenTmp</span><span class="sxs-lookup"><span data-stu-id="6bb3d-119">BankReconciliationDataInitializer.initDocumentOpenTmp</span></span>
- <span data-ttu-id="6bb3d-120">BankReconciliationDataInitializer.initStatementOpenTmp</span><span class="sxs-lookup"><span data-stu-id="6bb3d-120">BankReconciliationDataInitializer.initStatementOpenTmp</span></span>
- <span data-ttu-id="6bb3d-121">Class\\BomCalcJob\_All.processSingleTask</span><span class="sxs-lookup"><span data-stu-id="6bb3d-121">Class\\BomCalcJob\_All.processSingleTask</span></span>
- <span data-ttu-id="6bb3d-122">Class\\KanbanEventQuantityMap.newStandard</span><span class="sxs-lookup"><span data-stu-id="6bb3d-122">Class\\KanbanEventQuantityMap.newStandard</span></span>
- <span data-ttu-id="6bb3d-123">Class\\MCRFullTextSearchRefresh.run</span><span class="sxs-lookup"><span data-stu-id="6bb3d-123">Class\\MCRFullTextSearchRefresh.run</span></span>
- <span data-ttu-id="6bb3d-124">Class\\PdsRebateAgreementValidate.validate</span><span class="sxs-lookup"><span data-stu-id="6bb3d-124">Class\\PdsRebateAgreementValidate.validate</span></span>
- <span data-ttu-id="6bb3d-125">Class\\PurchRFQFormLetter.main</span><span class="sxs-lookup"><span data-stu-id="6bb3d-125">Class\\PurchRFQFormLetter.main</span></span>
- <span data-ttu-id="6bb3d-126">Class\\ReqTransPoMarkFirm.getPurchIdSingleThread</span><span class="sxs-lookup"><span data-stu-id="6bb3d-126">Class\\ReqTransPoMarkFirm.getPurchIdSingleThread</span></span>
- <span data-ttu-id="6bb3d-127">Class\\TAMVendRebateCorrectClaims.correctClaims</span><span class="sxs-lookup"><span data-stu-id="6bb3d-127">Class\\TAMVendRebateCorrectClaims.correctClaims</span></span>
- <span data-ttu-id="6bb3d-128">Class\\TAMVendRebateCorrectClaims.createClaimCorrection</span><span class="sxs-lookup"><span data-stu-id="6bb3d-128">Class\\TAMVendRebateCorrectClaims.createClaimCorrection</span></span>
- <span data-ttu-id="6bb3d-129">Class\\TAMVendRebateCorrectClaims.rebateAmountPerUnit</span><span class="sxs-lookup"><span data-stu-id="6bb3d-129">Class\\TAMVendRebateCorrectClaims.rebateAmountPerUnit</span></span>
- <span data-ttu-id="6bb3d-130">Class\\WhsReleaseToWarehouseForm.buttonRelease\_clicked</span><span class="sxs-lookup"><span data-stu-id="6bb3d-130">Class\\WhsReleaseToWarehouseForm.buttonRelease\_clicked</span></span>
- <span data-ttu-id="6bb3d-131">Classes\\LedgerAllocationRules.ValidateDimension</span><span class="sxs-lookup"><span data-stu-id="6bb3d-131">Classes\\LedgerAllocationRules.ValidateDimension</span></span>
- <span data-ttu-id="6bb3d-132">Classes\\ProjJournalCheckPost.checkFeeJournalDimensions</span><span class="sxs-lookup"><span data-stu-id="6bb3d-132">Classes\\ProjJournalCheckPost.checkFeeJournalDimensions</span></span>
- <span data-ttu-id="6bb3d-133">Commission\_Sales.run</span><span class="sxs-lookup"><span data-stu-id="6bb3d-133">Commission\_Sales.run</span></span>
- <span data-ttu-id="6bb3d-134">CreditcardPaymentCardTokenize.getFromDialog</span><span class="sxs-lookup"><span data-stu-id="6bb3d-134">CreditcardPaymentCardTokenize.getFromDialog</span></span>
- <span data-ttu-id="6bb3d-135">CustInPaymDialog.openDialog</span><span class="sxs-lookup"><span data-stu-id="6bb3d-135">CustInPaymDialog.openDialog</span></span>
- <span data-ttu-id="6bb3d-136">CustVendDisputeHelper.canDeleteDispute</span><span class="sxs-lookup"><span data-stu-id="6bb3d-136">CustVendDisputeHelper.canDeleteDispute</span></span>
- <span data-ttu-id="6bb3d-137">EcoResCategoryTreeDatasource.new</span><span class="sxs-lookup"><span data-stu-id="6bb3d-137">EcoResCategoryTreeDatasource.new</span></span>
- <span data-ttu-id="6bb3d-138">EcoResProductRelationtable.validateWrite</span><span class="sxs-lookup"><span data-stu-id="6bb3d-138">EcoResProductRelationtable.validateWrite</span></span>
- <span data-ttu-id="6bb3d-139">Form\\EcoResProductCreate.updateCallers</span><span class="sxs-lookup"><span data-stu-id="6bb3d-139">Form\\EcoResProductCreate.updateCallers</span></span>
- <span data-ttu-id="6bb3d-140">Form\\InventOnhandReserve\\DataSource\\InventSum.reserveNow</span><span class="sxs-lookup"><span data-stu-id="6bb3d-140">Form\\InventOnhandReserve\\DataSource\\InventSum.reserveNow</span></span>
- <span data-ttu-id="6bb3d-141">Form\\PdsRebateAgreement\\DataSource\\PdsRebateAgreement.executeQuery</span><span class="sxs-lookup"><span data-stu-id="6bb3d-141">Form\\PdsRebateAgreement\\DataSource\\PdsRebateAgreement.executeQuery</span></span>
- <span data-ttu-id="6bb3d-142">Form\\ProcCategoryHierarchyManagement\\FormDesign\\CategoryTreeGroup\\CategoryTreeCtrl.selection</span><span class="sxs-lookup"><span data-stu-id="6bb3d-142">Form\\ProcCategoryHierarchyManagement\\FormDesign\\CategoryTreeGroup\\CategoryTreeCtrl.selection</span></span>
- <span data-ttu-id="6bb3d-143">Form\\ReqSupplyDemandSchedule.updateDesign</span><span class="sxs-lookup"><span data-stu-id="6bb3d-143">Form\\ReqSupplyDemandSchedule.updateDesign</span></span>
- <span data-ttu-id="6bb3d-144">Form\\SalesTable\\DataSource\\MCRSalesLineDropShipment\\field\\DropShipment.modified</span><span class="sxs-lookup"><span data-stu-id="6bb3d-144">Form\\SalesTable\\DataSource\\MCRSalesLineDropShipment\\field\\DropShipment.modified</span></span>
- <span data-ttu-id="6bb3d-145">Form\\SalesTable\\DataSource\\SalesTable.create</span><span class="sxs-lookup"><span data-stu-id="6bb3d-145">Form\\SalesTable\\DataSource\\SalesTable.create</span></span>
- <span data-ttu-id="6bb3d-146">FormletterService.removeProforma</span><span class="sxs-lookup"><span data-stu-id="6bb3d-146">FormletterService.removeProforma</span></span>
- <span data-ttu-id="6bb3d-147">InventJournalTrans.validateWrite</span><span class="sxs-lookup"><span data-stu-id="6bb3d-147">InventJournalTrans.validateWrite</span></span>
- <span data-ttu-id="6bb3d-148">InventJournalTrans\_Tag.validateWrite</span><span class="sxs-lookup"><span data-stu-id="6bb3d-148">InventJournalTrans\_Tag.validateWrite</span></span>
- <span data-ttu-id="6bb3d-149">InventMovement.addLedgerPhysicalAmount</span><span class="sxs-lookup"><span data-stu-id="6bb3d-149">InventMovement.addLedgerPhysicalAmount</span></span>
- <span data-ttu-id="6bb3d-150">InventMovement.canAutoReserveQuantity</span><span class="sxs-lookup"><span data-stu-id="6bb3d-150">InventMovement.canAutoReserveQuantity</span></span>
- <span data-ttu-id="6bb3d-151">InventTransSerialNumberCreate.checkFormat</span><span class="sxs-lookup"><span data-stu-id="6bb3d-151">InventTransSerialNumberCreate.checkFormat</span></span>
- <span data-ttu-id="6bb3d-152">InventUpd\_Reservation.updateReserveLess</span><span class="sxs-lookup"><span data-stu-id="6bb3d-152">InventUpd\_Reservation.updateReserveLess</span></span>
- <span data-ttu-id="6bb3d-153">LedgerJournalEngine.onSegmentChangedForPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="6bb3d-153">LedgerJournalEngine.onSegmentChangedForPrimaryAccount</span></span>
- <span data-ttu-id="6bb3d-154">LedgerJournalTransCustPaym.enableDisableMandate</span><span class="sxs-lookup"><span data-stu-id="6bb3d-154">LedgerJournalTransCustPaym.enableDisableMandate</span></span>
- <span data-ttu-id="6bb3d-155">LedgerTransStatementDP.processOffsetAccountInStaging</span><span class="sxs-lookup"><span data-stu-id="6bb3d-155">LedgerTransStatementDP.processOffsetAccountInStaging</span></span>
- <span data-ttu-id="6bb3d-156">PdsBatchAttribReserveForm.checkReserveLine</span><span class="sxs-lookup"><span data-stu-id="6bb3d-156">PdsBatchAttribReserveForm.checkReserveLine</span></span>
- <span data-ttu-id="6bb3d-157">PriceDisc.findDiscAgreement</span><span class="sxs-lookup"><span data-stu-id="6bb3d-157">PriceDisc.findDiscAgreement</span></span>
- <span data-ttu-id="6bb3d-158">PriceDiscAdmCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="6bb3d-158">PriceDiscAdmCheckPost.postJournal</span></span>
- <span data-ttu-id="6bb3d-159">PriceDiscHeading.updateDiscQty</span><span class="sxs-lookup"><span data-stu-id="6bb3d-159">PriceDiscHeading.updateDiscQty</span></span>
- <span data-ttu-id="6bb3d-160">PriceDiscHeading.updateMultiLineDiscTmp</span><span class="sxs-lookup"><span data-stu-id="6bb3d-160">PriceDiscHeading.updateMultiLineDiscTmp</span></span>
- <span data-ttu-id="6bb3d-161">PriceDiscPolicyFindOrCreate.run</span><span class="sxs-lookup"><span data-stu-id="6bb3d-161">PriceDiscPolicyFindOrCreate.run</span></span>
- <span data-ttu-id="6bb3d-162">ProjInvoiceControl.projInvoiceControl</span><span class="sxs-lookup"><span data-stu-id="6bb3d-162">ProjInvoiceControl.projInvoiceControl</span></span>
- <span data-ttu-id="6bb3d-163">ProjPostCostJournal.new</span><span class="sxs-lookup"><span data-stu-id="6bb3d-163">ProjPostCostJournal.new</span></span>
- <span data-ttu-id="6bb3d-164">PurchLineType.validateWrite</span><span class="sxs-lookup"><span data-stu-id="6bb3d-164">PurchLineType.validateWrite</span></span>
- <span data-ttu-id="6bb3d-165">ReqTransFormExplosion.tmpReqExplosionOnhandBuildServer</span><span class="sxs-lookup"><span data-stu-id="6bb3d-165">ReqTransFormExplosion.tmpReqExplosionOnhandBuildServer</span></span>
- <span data-ttu-id="6bb3d-166">ReqTransPoMarkFirm.createPurchTable</span><span class="sxs-lookup"><span data-stu-id="6bb3d-166">ReqTransPoMarkFirm.createPurchTable</span></span>
- <span data-ttu-id="6bb3d-167">ReqTransPoMarkFirm.updatePurchBuyerGroup</span><span class="sxs-lookup"><span data-stu-id="6bb3d-167">ReqTransPoMarkFirm.updatePurchBuyerGroup</span></span>
- <span data-ttu-id="6bb3d-168">RequisitionPurchaseOrderGeneration.createPurchaseOrder</span><span class="sxs-lookup"><span data-stu-id="6bb3d-168">RequisitionPurchaseOrderGeneration.createPurchaseOrder</span></span>
- <span data-ttu-id="6bb3d-169">RetailBarCodeManagement.CreateBarCodeNoDim</span><span class="sxs-lookup"><span data-stu-id="6bb3d-169">RetailBarCodeManagement.CreateBarCodeNoDim</span></span>
- <span data-ttu-id="6bb3d-170">RetailTransactionServiceOrders.createCustomerOrder</span><span class="sxs-lookup"><span data-stu-id="6bb3d-170">RetailTransactionServiceOrders.createCustomerOrder</span></span>
- <span data-ttu-id="6bb3d-171">RetailTransactionTransformer.readTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="6bb3d-171">RetailTransactionTransformer.readTransactionSalesTrans</span></span>
- <span data-ttu-id="6bb3d-172">SalesLine.createLine</span><span class="sxs-lookup"><span data-stu-id="6bb3d-172">SalesLine.createLine</span></span>
- <span data-ttu-id="6bb3d-173">SalesLine.initFromPriceDisc</span><span class="sxs-lookup"><span data-stu-id="6bb3d-173">SalesLine.initFromPriceDisc</span></span>
- <span data-ttu-id="6bb3d-174">SalesLine.insert</span><span class="sxs-lookup"><span data-stu-id="6bb3d-174">SalesLine.insert</span></span>
- <span data-ttu-id="6bb3d-175">SalesLine.update</span><span class="sxs-lookup"><span data-stu-id="6bb3d-175">SalesLine.update</span></span>
- <span data-ttu-id="6bb3d-176">SalesLine.validateDelete</span><span class="sxs-lookup"><span data-stu-id="6bb3d-176">SalesLine.validateDelete</span></span>
- <span data-ttu-id="6bb3d-177">SalesLine.writeRetailSalesLine</span><span class="sxs-lookup"><span data-stu-id="6bb3d-177">SalesLine.writeRetailSalesLine</span></span>
- <span data-ttu-id="6bb3d-178">SalesTable.updateMultiLineDisc</span><span class="sxs-lookup"><span data-stu-id="6bb3d-178">SalesTable.updateMultiLineDisc</span></span>
- <span data-ttu-id="6bb3d-179">SmaServiceFunctionLine\_transfer.Run</span><span class="sxs-lookup"><span data-stu-id="6bb3d-179">SmaServiceFunctionLine\_transfer.Run</span></span>
- <span data-ttu-id="6bb3d-180">SmmOpportunityStatusUpdate.updateFromQuote</span><span class="sxs-lookup"><span data-stu-id="6bb3d-180">SmmOpportunityStatusUpdate.updateFromQuote</span></span>
- <span data-ttu-id="6bb3d-181">Table\\MCRCustpaymTable.salesTableByPassCreditLimit, displayOrderID, getCurrency, and mcrCustPaym\\getCustomerPostingProfile</span><span class="sxs-lookup"><span data-stu-id="6bb3d-181">Table\\MCRCustpaymTable.salesTableByPassCreditLimit, displayOrderID, getCurrency, and mcrCustPaym\\getCustomerPostingProfile</span></span>
- <span data-ttu-id="6bb3d-182">Table\\ReqPO.findAnySalesLineForReqPO</span><span class="sxs-lookup"><span data-stu-id="6bb3d-182">Table\\ReqPO.findAnySalesLineForReqPO</span></span>
- <span data-ttu-id="6bb3d-183">TaxUncommitted.createTaxUncommitted, added local method createTaxUncommittedFromTmpTaxWorkTrans</span><span class="sxs-lookup"><span data-stu-id="6bb3d-183">TaxUncommitted.createTaxUncommitted, added local method createTaxUncommittedFromTmpTaxWorkTrans</span></span>
- <span data-ttu-id="6bb3d-184">TmpTaxReport\_IT.create</span><span class="sxs-lookup"><span data-stu-id="6bb3d-184">TmpTaxReport\_IT.create</span></span>
- <span data-ttu-id="6bb3d-185">TrvExpTrans.defaultTaxGroupFromWorker</span><span class="sxs-lookup"><span data-stu-id="6bb3d-185">TrvExpTrans.defaultTaxGroupFromWorker</span></span>
- <span data-ttu-id="6bb3d-186">WHSBillOfLadingDP.insertWHSBillOfLadingTmp</span><span class="sxs-lookup"><span data-stu-id="6bb3d-186">WHSBillOfLadingDP.insertWHSBillOfLadingTmp</span></span>
- <span data-ttu-id="6bb3d-187">WHSControlItemId.populate</span><span class="sxs-lookup"><span data-stu-id="6bb3d-187">WHSControlItemId.populate</span></span>
- <span data-ttu-id="6bb3d-188">WhsWarehouseRelease.creditLimitCheck</span><span class="sxs-lookup"><span data-stu-id="6bb3d-188">WhsWarehouseRelease.creditLimitCheck</span></span>
- <span data-ttu-id="6bb3d-189">WhsWorkCreate.addRangesToWorkTemplateQuery</span><span class="sxs-lookup"><span data-stu-id="6bb3d-189">WhsWorkCreate.addRangesToWorkTemplateQuery</span></span>
- <span data-ttu-id="6bb3d-190">WHSWorkExecute.CreateTransferJournalLine</span><span class="sxs-lookup"><span data-stu-id="6bb3d-190">WHSWorkExecute.CreateTransferJournalLine</span></span>
- <span data-ttu-id="6bb3d-191">WhsWorkTypePrintHandler.buildLabelAndConfirm</span><span class="sxs-lookup"><span data-stu-id="6bb3d-191">WhsWorkTypePrintHandler.buildLabelAndConfirm</span></span>

## <a name="other-extensibility-enhancements"></a><span data-ttu-id="6bb3d-192">その他の拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="6bb3d-192">Other extensibility enhancements</span></span>

- <span data-ttu-id="6bb3d-193">The PriceDiscHeading マップが拡張可能になりました。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-193">The PriceDiscHeading map was made extensible.</span></span>
- <span data-ttu-id="6bb3d-194">**小売チャンネル:** Shipped、PackingSlip、MarkAsPacked に対してプレトリガーが追加されました。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-194">**Retail channel:** Pre-triggers were added for Shipped, PackingSlip, and MarkAsPacked.</span></span>
- <span data-ttu-id="6bb3d-195">**小売チャンネル:** キャンセル費用のダイアログボックスを無効化することができます。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-195">**Retail channel:** The Cancellation charge dialog box can be overridden.</span></span>
- <span data-ttu-id="6bb3d-196">**小売チャンネル:** オーダー検索のダイアログボックスに、オーダー取消のデフォルト パラメータ値が拡張されました。</span><span class="sxs-lookup"><span data-stu-id="6bb3d-196">**Retail channel:** Recall order default parameter value extension for the search order dialog box.</span></span>
