---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 06/21/2018
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
ms.search.validFrom: 2018-06-30
ms.dyn365.ops.version: App 8.0.2
ms.openlocfilehash: 31fa4ee4db4e4224698530fd48b011f72cb9a7a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409341"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-802"></a><span data-ttu-id="d907e-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="d907e-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.2</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d907e-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="d907e-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.2.</span></span> <span data-ttu-id="d907e-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d907e-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="d907e-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="d907e-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="d907e-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d907e-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="d907e-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="d907e-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="d907e-109">AccDistProcessorProjectExtension.allocateExistingDistribution</span><span class="sxs-lookup"><span data-stu-id="d907e-109">AccDistProcessorProjectExtension.allocateExistingDistribution</span></span>|
|<span data-ttu-id="d907e-110">AccDistProcessorProjectExtension.createDistributionLists</span><span class="sxs-lookup"><span data-stu-id="d907e-110">AccDistProcessorProjectExtension.createDistributionLists</span></span>|
|<span data-ttu-id="d907e-111">AccDistProcessorProjectExtension.ledgerDimensionAllocationList</span><span class="sxs-lookup"><span data-stu-id="d907e-111">AccDistProcessorProjectExtension.ledgerDimensionAllocationList</span></span>|
|<span data-ttu-id="d907e-112">AgreementConfirmationDP.processReport</span><span class="sxs-lookup"><span data-stu-id="d907e-112">AgreementConfirmationDP.processReport</span></span>|
|<span data-ttu-id="d907e-113">Bank_FR.checkControlText</span><span class="sxs-lookup"><span data-stu-id="d907e-113">Bank_FR.checkControlText</span></span>|
|<span data-ttu-id="d907e-114">Bank_IT.checkCIN</span><span class="sxs-lookup"><span data-stu-id="d907e-114">Bank_IT.checkCIN</span></span>|
|<span data-ttu-id="d907e-115">Bank_IT.checkRegistrationNum</span><span class="sxs-lookup"><span data-stu-id="d907e-115">Bank_IT.checkRegistrationNum</span></span>|
|<span data-ttu-id="d907e-116">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="d907e-116">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="d907e-117">FBSpedFileCreator_Contabil_BR.createRecordI052</span><span class="sxs-lookup"><span data-stu-id="d907e-117">FBSpedFileCreator_Contabil_BR.createRecordI052</span></span>|
|<span data-ttu-id="d907e-118">HierarchyTemplateCopying_proj.createFromHierarchySource</span><span class="sxs-lookup"><span data-stu-id="d907e-118">HierarchyTemplateCopying_proj.createFromHierarchySource</span></span>|
|<span data-ttu-id="d907e-119">HierarchyTreeLookup.datasource smmActivities.init</span><span class="sxs-lookup"><span data-stu-id="d907e-119">HierarchyTreeLookup.datasource smmActivities.init</span></span>|
|<span data-ttu-id="d907e-120">InventDim.validateFieldCombination</span><span class="sxs-lookup"><span data-stu-id="d907e-120">InventDim.validateFieldCombination</span></span>|
|<span data-ttu-id="d907e-121">InventTransWMS_Register</span><span class="sxs-lookup"><span data-stu-id="d907e-121">InventTransWMS_Register</span></span>|
|<span data-ttu-id="d907e-122">InventUpd_Financial.updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="d907e-122">InventUpd_Financial.updateFinancialIssue</span></span>|
|<span data-ttu-id="d907e-123">InventUpd_Registered</span><span class="sxs-lookup"><span data-stu-id="d907e-123">InventUpd_Registered</span></span>|
|<span data-ttu-id="d907e-124">JmgPostStandardSystem.PostProjTime</span><span class="sxs-lookup"><span data-stu-id="d907e-124">JmgPostStandardSystem.PostProjTime</span></span>|
|<span data-ttu-id="d907e-125">MarkupAllocation.run</span><span class="sxs-lookup"><span data-stu-id="d907e-125">MarkupAllocation.run</span></span>|
|<span data-ttu-id="d907e-126">MarkupTrans。</span><span class="sxs-lookup"><span data-stu-id="d907e-126">MarkupTrans.</span></span> <span data-ttu-id="d907e-127">MarkupTrans(datasource).active</span><span class="sxs-lookup"><span data-stu-id="d907e-127">MarkupTrans(datasource).active</span></span>|
|<span data-ttu-id="d907e-128">PdsBatchAttribByItem.checkDuplicateAttributes</span><span class="sxs-lookup"><span data-stu-id="d907e-128">PdsBatchAttribByItem.checkDuplicateAttributes</span></span>|
|<span data-ttu-id="d907e-129">PdsBatchAttribByItem.validateFieldValue</span><span class="sxs-lookup"><span data-stu-id="d907e-129">PdsBatchAttribByItem.validateFieldValue</span></span>|
|<span data-ttu-id="d907e-130">PdsBatchAttribReserve.linkActive</span><span class="sxs-lookup"><span data-stu-id="d907e-130">PdsBatchAttribReserve.linkActive</span></span>|
|<span data-ttu-id="d907e-131">PdsBatchAttributes.Datasource.PdsBatchAttributes.linkactive</span><span class="sxs-lookup"><span data-stu-id="d907e-131">PdsBatchAttributes.Datasource.PdsBatchAttributes.linkactive</span></span>|
|<span data-ttu-id="d907e-132">ProjInvoiceProposalCreateLines.closeOK</span><span class="sxs-lookup"><span data-stu-id="d907e-132">ProjInvoiceProposalCreateLines.closeOK</span></span>|
|<span data-ttu-id="d907e-133">ProjInvoiceProposalInsertLines.doCost</span><span class="sxs-lookup"><span data-stu-id="d907e-133">ProjInvoiceProposalInsertLines.doCost</span></span>|
|<span data-ttu-id="d907e-134">ProjInvoiceProposalInsertLines.doEmpl</span><span class="sxs-lookup"><span data-stu-id="d907e-134">ProjInvoiceProposalInsertLines.doEmpl</span></span>|
|<span data-ttu-id="d907e-135">ProjInvoiceProposalInsertLines.doItem</span><span class="sxs-lookup"><span data-stu-id="d907e-135">ProjInvoiceProposalInsertLines.doItem</span></span>|
|<span data-ttu-id="d907e-136">ProjInvoiceProposalInsertLines.doOnAccount</span><span class="sxs-lookup"><span data-stu-id="d907e-136">ProjInvoiceProposalInsertLines.doOnAccount</span></span>|
|<span data-ttu-id="d907e-137">ProjPeriodPostingLedgerSales.enteItem</span><span class="sxs-lookup"><span data-stu-id="d907e-137">ProjPeriodPostingLedgerSales.enteItem</span></span>|
|<span data-ttu-id="d907e-138">ProjPeriodPostingLedgerSales.enterCost</span><span class="sxs-lookup"><span data-stu-id="d907e-138">ProjPeriodPostingLedgerSales.enterCost</span></span>|
|<span data-ttu-id="d907e-139">ProjPeriodPostingLedgerSales.enterEmpl</span><span class="sxs-lookup"><span data-stu-id="d907e-139">ProjPeriodPostingLedgerSales.enterEmpl</span></span>|
|<span data-ttu-id="d907e-140">ProjPeriodPostingLedgerSales.enterRevenue</span><span class="sxs-lookup"><span data-stu-id="d907e-140">ProjPeriodPostingLedgerSales.enterRevenue</span></span>|
|<span data-ttu-id="d907e-141">ProjPeriodPostingLedgerSales.run</span><span class="sxs-lookup"><span data-stu-id="d907e-141">ProjPeriodPostingLedgerSales.run</span></span>|
|<span data-ttu-id="d907e-142">ProjPlanVersionsManager.CopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="d907e-142">ProjPlanVersionsManager.CopyHierarchy</span></span>|
|<span data-ttu-id="d907e-143">ProjPlanVersionsManager::CopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="d907e-143">ProjPlanVersionsManager::copyHierarchy</span></span>|
|<span data-ttu-id="d907e-144">ProjPlanVersionsManager::createDraftVersion</span><span class="sxs-lookup"><span data-stu-id="d907e-144">ProjPlanVersionsManager::createDraftVersion</span></span>|
|<span data-ttu-id="d907e-145">ProjPlanVersionsManager::createTemplateHierarchy</span><span class="sxs-lookup"><span data-stu-id="d907e-145">ProjPlanVersionsManager::createTemplateHierarchy</span></span>|
|<span data-ttu-id="d907e-146">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="d907e-146">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="d907e-147">PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="d907e-147">PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="d907e-148">PurchRFQPriceDiscAdmCreate.createPriceDiscAdmTrans</span><span class="sxs-lookup"><span data-stu-id="d907e-148">PurchRFQPriceDiscAdmCreate.createPriceDiscAdmTrans</span></span>|
|<span data-ttu-id="d907e-149">SalesFormLetter.validate</span><span class="sxs-lookup"><span data-stu-id="d907e-149">SalesFormLetter.validate</span></span>|
|<span data-ttu-id="d907e-150">SalesTable2LineUpdatePrompt.salesTableFieldModifiedHandler</span><span class="sxs-lookup"><span data-stu-id="d907e-150">SalesTable2LineUpdatePrompt.salesTableFieldModifiedHandler</span></span>|
|<span data-ttu-id="d907e-151">SalesUpdateRemain.cancelOpenOrderLinesDeliveryRemainder</span><span class="sxs-lookup"><span data-stu-id="d907e-151">SalesUpdateRemain.cancelOpenOrderLinesDeliveryRemainder</span></span>|
|<span data-ttu-id="d907e-152">WHSShipmentTable.createShipmentNotes</span><span class="sxs-lookup"><span data-stu-id="d907e-152">WHSShipmentTable.createShipmentNotes</span></span>|
|<span data-ttu-id="d907e-153">WHSUnShipLoadLineTmpDataCreator.createTmpLoadLineInventoryFromContainerLines</span><span class="sxs-lookup"><span data-stu-id="d907e-153">WHSUnShipLoadLineTmpDataCreator.createTmpLoadLineInventoryFromContainerLines</span></span>|

## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="d907e-154">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="d907e-154">Additional extensibility enhancements</span></span>

<span data-ttu-id="d907e-155">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="d907e-155">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="d907e-156">拡張子からマップのサポート: CustVendTrans</span><span class="sxs-lookup"><span data-stu-id="d907e-156">Support for extensions to map: CustVendTrans</span></span>
- <span data-ttu-id="d907e-157">拡張子からマップのサポート: CustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="d907e-157">Support for extensions to map: CustVendTransOpen</span></span>
- <span data-ttu-id="d907e-158">SQL 明細書の機能拡張をサポート: PriceDiscAdmCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="d907e-158">Support extensibility for SQL statement:  PriceDiscAdmCheckPost.postJournal</span></span>
