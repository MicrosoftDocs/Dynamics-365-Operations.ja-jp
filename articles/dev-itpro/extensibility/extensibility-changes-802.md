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
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-06-30
ms.dyn365.ops.version: App 8.0.2
ms.openlocfilehash: f207323fce53e684514246c27bb159a5f48aa1eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550889"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-802"></a><span data-ttu-id="a6233-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="a6233-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.2</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6233-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="a6233-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.2.</span></span> <span data-ttu-id="a6233-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6233-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="a6233-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="a6233-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="a6233-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a6233-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="a6233-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="a6233-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="a6233-109">AccDistProcessorProjectExtension.allocateExistingDistribution</span><span class="sxs-lookup"><span data-stu-id="a6233-109">AccDistProcessorProjectExtension.allocateExistingDistribution</span></span>|
|<span data-ttu-id="a6233-110">AccDistProcessorProjectExtension.createDistributionLists</span><span class="sxs-lookup"><span data-stu-id="a6233-110">AccDistProcessorProjectExtension.createDistributionLists</span></span>|
|<span data-ttu-id="a6233-111">AccDistProcessorProjectExtension.ledgerDimensionAllocationList</span><span class="sxs-lookup"><span data-stu-id="a6233-111">AccDistProcessorProjectExtension.ledgerDimensionAllocationList</span></span>|
|<span data-ttu-id="a6233-112">AgreementConfirmationDP.processReport</span><span class="sxs-lookup"><span data-stu-id="a6233-112">AgreementConfirmationDP.processReport</span></span>|
|<span data-ttu-id="a6233-113">Bank_FR.checkControlText</span><span class="sxs-lookup"><span data-stu-id="a6233-113">Bank_FR.checkControlText</span></span>|
|<span data-ttu-id="a6233-114">Bank_IT.checkCIN</span><span class="sxs-lookup"><span data-stu-id="a6233-114">Bank_IT.checkCIN</span></span>|
|<span data-ttu-id="a6233-115">Bank_IT.checkRegistrationNum</span><span class="sxs-lookup"><span data-stu-id="a6233-115">Bank_IT.checkRegistrationNum</span></span>|
|<span data-ttu-id="a6233-116">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="a6233-116">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="a6233-117">FBSpedFileCreator_Contabil_BR.createRecordI052</span><span class="sxs-lookup"><span data-stu-id="a6233-117">FBSpedFileCreator_Contabil_BR.createRecordI052</span></span>|
|<span data-ttu-id="a6233-118">HierarchyTemplateCopying_proj.createFromHierarchySource</span><span class="sxs-lookup"><span data-stu-id="a6233-118">HierarchyTemplateCopying_proj.createFromHierarchySource</span></span>|
|<span data-ttu-id="a6233-119">HierarchyTreeLookup.datasource smmActivities.init</span><span class="sxs-lookup"><span data-stu-id="a6233-119">HierarchyTreeLookup.datasource smmActivities.init</span></span>|
|<span data-ttu-id="a6233-120">InventDim.validateFieldCombination</span><span class="sxs-lookup"><span data-stu-id="a6233-120">InventDim.validateFieldCombination</span></span>|
|<span data-ttu-id="a6233-121">InventTransWMS_Register</span><span class="sxs-lookup"><span data-stu-id="a6233-121">InventTransWMS_Register</span></span>|
|<span data-ttu-id="a6233-122">InventUpd_Financial.updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="a6233-122">InventUpd_Financial.updateFinancialIssue</span></span>|
|<span data-ttu-id="a6233-123">InventUpd_Registered</span><span class="sxs-lookup"><span data-stu-id="a6233-123">InventUpd_Registered</span></span>|
|<span data-ttu-id="a6233-124">JmgPostStandardSystem.PostProjTime</span><span class="sxs-lookup"><span data-stu-id="a6233-124">JmgPostStandardSystem.PostProjTime</span></span>|
|<span data-ttu-id="a6233-125">MarkupAllocation.run</span><span class="sxs-lookup"><span data-stu-id="a6233-125">MarkupAllocation.run</span></span>|
|<span data-ttu-id="a6233-126">MarkupTrans。</span><span class="sxs-lookup"><span data-stu-id="a6233-126">MarkupTrans.</span></span> <span data-ttu-id="a6233-127">MarkupTrans(datasource).active</span><span class="sxs-lookup"><span data-stu-id="a6233-127">MarkupTrans(datasource).active</span></span>|
|<span data-ttu-id="a6233-128">PdsBatchAttribByItem.checkDuplicateAttributes</span><span class="sxs-lookup"><span data-stu-id="a6233-128">PdsBatchAttribByItem.checkDuplicateAttributes</span></span>|
|<span data-ttu-id="a6233-129">PdsBatchAttribByItem.validateFieldValue</span><span class="sxs-lookup"><span data-stu-id="a6233-129">PdsBatchAttribByItem.validateFieldValue</span></span>|
|<span data-ttu-id="a6233-130">PdsBatchAttribReserve.linkActive</span><span class="sxs-lookup"><span data-stu-id="a6233-130">PdsBatchAttribReserve.linkActive</span></span>|
|<span data-ttu-id="a6233-131">PdsBatchAttributes.Datasource.PdsBatchAttributes.linkactive</span><span class="sxs-lookup"><span data-stu-id="a6233-131">PdsBatchAttributes.Datasource.PdsBatchAttributes.linkactive</span></span>|
|<span data-ttu-id="a6233-132">ProjInvoiceProposalCreateLines.closeOK</span><span class="sxs-lookup"><span data-stu-id="a6233-132">ProjInvoiceProposalCreateLines.closeOK</span></span>|
|<span data-ttu-id="a6233-133">ProjInvoiceProposalInsertLines.doCost</span><span class="sxs-lookup"><span data-stu-id="a6233-133">ProjInvoiceProposalInsertLines.doCost</span></span>|
|<span data-ttu-id="a6233-134">ProjInvoiceProposalInsertLines.doEmpl</span><span class="sxs-lookup"><span data-stu-id="a6233-134">ProjInvoiceProposalInsertLines.doEmpl</span></span>|
|<span data-ttu-id="a6233-135">ProjInvoiceProposalInsertLines.doItem</span><span class="sxs-lookup"><span data-stu-id="a6233-135">ProjInvoiceProposalInsertLines.doItem</span></span>|
|<span data-ttu-id="a6233-136">ProjInvoiceProposalInsertLines.doOnAccount</span><span class="sxs-lookup"><span data-stu-id="a6233-136">ProjInvoiceProposalInsertLines.doOnAccount</span></span>|
|<span data-ttu-id="a6233-137">ProjPeriodPostingLedgerSales.enteItem</span><span class="sxs-lookup"><span data-stu-id="a6233-137">ProjPeriodPostingLedgerSales.enteItem</span></span>|
|<span data-ttu-id="a6233-138">ProjPeriodPostingLedgerSales.enterCost</span><span class="sxs-lookup"><span data-stu-id="a6233-138">ProjPeriodPostingLedgerSales.enterCost</span></span>|
|<span data-ttu-id="a6233-139">ProjPeriodPostingLedgerSales.enterEmpl</span><span class="sxs-lookup"><span data-stu-id="a6233-139">ProjPeriodPostingLedgerSales.enterEmpl</span></span>|
|<span data-ttu-id="a6233-140">ProjPeriodPostingLedgerSales.enterRevenue</span><span class="sxs-lookup"><span data-stu-id="a6233-140">ProjPeriodPostingLedgerSales.enterRevenue</span></span>|
|<span data-ttu-id="a6233-141">ProjPeriodPostingLedgerSales.run</span><span class="sxs-lookup"><span data-stu-id="a6233-141">ProjPeriodPostingLedgerSales.run</span></span>|
|<span data-ttu-id="a6233-142">ProjPlanVersionsManager.CopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="a6233-142">ProjPlanVersionsManager.CopyHierarchy</span></span>|
|<span data-ttu-id="a6233-143">ProjPlanVersionsManager::CopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="a6233-143">ProjPlanVersionsManager::copyHierarchy</span></span>|
|<span data-ttu-id="a6233-144">ProjPlanVersionsManager::createDraftVersion</span><span class="sxs-lookup"><span data-stu-id="a6233-144">ProjPlanVersionsManager::createDraftVersion</span></span>|
|<span data-ttu-id="a6233-145">ProjPlanVersionsManager::createTemplateHierarchy</span><span class="sxs-lookup"><span data-stu-id="a6233-145">ProjPlanVersionsManager::createTemplateHierarchy</span></span>|
|<span data-ttu-id="a6233-146">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="a6233-146">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="a6233-147">PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="a6233-147">PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="a6233-148">PurchRFQPriceDiscAdmCreate.createPriceDiscAdmTrans</span><span class="sxs-lookup"><span data-stu-id="a6233-148">PurchRFQPriceDiscAdmCreate.createPriceDiscAdmTrans</span></span>|
|<span data-ttu-id="a6233-149">SalesFormLetter.validate</span><span class="sxs-lookup"><span data-stu-id="a6233-149">SalesFormLetter.validate</span></span>|
|<span data-ttu-id="a6233-150">SalesTable2LineUpdatePrompt.salesTableFieldModifiedHandler</span><span class="sxs-lookup"><span data-stu-id="a6233-150">SalesTable2LineUpdatePrompt.salesTableFieldModifiedHandler</span></span>|
|<span data-ttu-id="a6233-151">SalesUpdateRemain.cancelOpenOrderLinesDeliveryRemainder</span><span class="sxs-lookup"><span data-stu-id="a6233-151">SalesUpdateRemain.cancelOpenOrderLinesDeliveryRemainder</span></span>|
|<span data-ttu-id="a6233-152">WHSShipmentTable.createShipmentNotes</span><span class="sxs-lookup"><span data-stu-id="a6233-152">WHSShipmentTable.createShipmentNotes</span></span>|
|<span data-ttu-id="a6233-153">WHSUnShipLoadLineTmpDataCreator.createTmpLoadLineInventoryFromContainerLines</span><span class="sxs-lookup"><span data-stu-id="a6233-153">WHSUnShipLoadLineTmpDataCreator.createTmpLoadLineInventoryFromContainerLines</span></span>|

## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="a6233-154">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="a6233-154">Additional extensibility enhancements</span></span>

<span data-ttu-id="a6233-155">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="a6233-155">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="a6233-156">拡張子からマップのサポート: CustVendTrans</span><span class="sxs-lookup"><span data-stu-id="a6233-156">Support for extensions to map: CustVendTrans</span></span>
- <span data-ttu-id="a6233-157">拡張子からマップのサポート: CustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="a6233-157">Support for extensions to map: CustVendTransOpen</span></span>
- <span data-ttu-id="a6233-158">SQL 明細書の機能拡張をサポート: PriceDiscAdmCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="a6233-158">Support extensibility for SQL statement:  PriceDiscAdmCheckPost.postJournal</span></span>
