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
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-06-30
ms.dyn365.ops.version: App 8.0.2
ms.openlocfilehash: 7d036a4df8401565876ff2a4305ff1b513dd0f68
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183325"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-802"></a><span data-ttu-id="07f25-103">Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="07f25-103">Extensibility changes in Dynamics 365 for Finance and Operations update 8.0.2</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07f25-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="07f25-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.2.</span></span> <span data-ttu-id="07f25-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07f25-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="07f25-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="07f25-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="07f25-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="07f25-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="07f25-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="07f25-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="07f25-109">AccDistProcessorProjectExtension.allocateExistingDistribution</span><span class="sxs-lookup"><span data-stu-id="07f25-109">AccDistProcessorProjectExtension.allocateExistingDistribution</span></span>|
|<span data-ttu-id="07f25-110">AccDistProcessorProjectExtension.createDistributionLists</span><span class="sxs-lookup"><span data-stu-id="07f25-110">AccDistProcessorProjectExtension.createDistributionLists</span></span>|
|<span data-ttu-id="07f25-111">AccDistProcessorProjectExtension.ledgerDimensionAllocationList</span><span class="sxs-lookup"><span data-stu-id="07f25-111">AccDistProcessorProjectExtension.ledgerDimensionAllocationList</span></span>|
|<span data-ttu-id="07f25-112">AgreementConfirmationDP.processReport</span><span class="sxs-lookup"><span data-stu-id="07f25-112">AgreementConfirmationDP.processReport</span></span>|
|<span data-ttu-id="07f25-113">Bank_FR.checkControlText</span><span class="sxs-lookup"><span data-stu-id="07f25-113">Bank_FR.checkControlText</span></span>|
|<span data-ttu-id="07f25-114">Bank_IT.checkCIN</span><span class="sxs-lookup"><span data-stu-id="07f25-114">Bank_IT.checkCIN</span></span>|
|<span data-ttu-id="07f25-115">Bank_IT.checkRegistrationNum</span><span class="sxs-lookup"><span data-stu-id="07f25-115">Bank_IT.checkRegistrationNum</span></span>|
|<span data-ttu-id="07f25-116">CustVendCheque.initTmpChequePrintout</span><span class="sxs-lookup"><span data-stu-id="07f25-116">CustVendCheque.initTmpChequePrintout</span></span>|
|<span data-ttu-id="07f25-117">FBSpedFileCreator_Contabil_BR.createRecordI052</span><span class="sxs-lookup"><span data-stu-id="07f25-117">FBSpedFileCreator_Contabil_BR.createRecordI052</span></span>|
|<span data-ttu-id="07f25-118">HierarchyTemplateCopying_proj.createFromHierarchySource</span><span class="sxs-lookup"><span data-stu-id="07f25-118">HierarchyTemplateCopying_proj.createFromHierarchySource</span></span>|
|<span data-ttu-id="07f25-119">HierarchyTreeLookup.datasource smmActivities.init</span><span class="sxs-lookup"><span data-stu-id="07f25-119">HierarchyTreeLookup.datasource smmActivities.init</span></span>|
|<span data-ttu-id="07f25-120">InventDim.validateFieldCombination</span><span class="sxs-lookup"><span data-stu-id="07f25-120">InventDim.validateFieldCombination</span></span>|
|<span data-ttu-id="07f25-121">InventTransWMS_Register</span><span class="sxs-lookup"><span data-stu-id="07f25-121">InventTransWMS_Register</span></span>|
|<span data-ttu-id="07f25-122">InventUpd_Financial.updateFinancialIssue</span><span class="sxs-lookup"><span data-stu-id="07f25-122">InventUpd_Financial.updateFinancialIssue</span></span>|
|<span data-ttu-id="07f25-123">InventUpd_Registered</span><span class="sxs-lookup"><span data-stu-id="07f25-123">InventUpd_Registered</span></span>|
|<span data-ttu-id="07f25-124">JmgPostStandardSystem.PostProjTime</span><span class="sxs-lookup"><span data-stu-id="07f25-124">JmgPostStandardSystem.PostProjTime</span></span>|
|<span data-ttu-id="07f25-125">MarkupAllocation.run</span><span class="sxs-lookup"><span data-stu-id="07f25-125">MarkupAllocation.run</span></span>|
|<span data-ttu-id="07f25-126">MarkupTrans。</span><span class="sxs-lookup"><span data-stu-id="07f25-126">MarkupTrans.</span></span> <span data-ttu-id="07f25-127">MarkupTrans(datasource).active</span><span class="sxs-lookup"><span data-stu-id="07f25-127">MarkupTrans(datasource).active</span></span>|
|<span data-ttu-id="07f25-128">PdsBatchAttribByItem.checkDuplicateAttributes</span><span class="sxs-lookup"><span data-stu-id="07f25-128">PdsBatchAttribByItem.checkDuplicateAttributes</span></span>|
|<span data-ttu-id="07f25-129">PdsBatchAttribByItem.validateFieldValue</span><span class="sxs-lookup"><span data-stu-id="07f25-129">PdsBatchAttribByItem.validateFieldValue</span></span>|
|<span data-ttu-id="07f25-130">PdsBatchAttribReserve.linkActive</span><span class="sxs-lookup"><span data-stu-id="07f25-130">PdsBatchAttribReserve.linkActive</span></span>|
|<span data-ttu-id="07f25-131">PdsBatchAttributes.Datasource.PdsBatchAttributes.linkactive</span><span class="sxs-lookup"><span data-stu-id="07f25-131">PdsBatchAttributes.Datasource.PdsBatchAttributes.linkactive</span></span>|
|<span data-ttu-id="07f25-132">ProjInvoiceProposalCreateLines.closeOK</span><span class="sxs-lookup"><span data-stu-id="07f25-132">ProjInvoiceProposalCreateLines.closeOK</span></span>|
|<span data-ttu-id="07f25-133">ProjInvoiceProposalInsertLines.doCost</span><span class="sxs-lookup"><span data-stu-id="07f25-133">ProjInvoiceProposalInsertLines.doCost</span></span>|
|<span data-ttu-id="07f25-134">ProjInvoiceProposalInsertLines.doEmpl</span><span class="sxs-lookup"><span data-stu-id="07f25-134">ProjInvoiceProposalInsertLines.doEmpl</span></span>|
|<span data-ttu-id="07f25-135">ProjInvoiceProposalInsertLines.doItem</span><span class="sxs-lookup"><span data-stu-id="07f25-135">ProjInvoiceProposalInsertLines.doItem</span></span>|
|<span data-ttu-id="07f25-136">ProjInvoiceProposalInsertLines.doOnAccount</span><span class="sxs-lookup"><span data-stu-id="07f25-136">ProjInvoiceProposalInsertLines.doOnAccount</span></span>|
|<span data-ttu-id="07f25-137">ProjPeriodPostingLedgerSales.enteItem</span><span class="sxs-lookup"><span data-stu-id="07f25-137">ProjPeriodPostingLedgerSales.enteItem</span></span>|
|<span data-ttu-id="07f25-138">ProjPeriodPostingLedgerSales.enterCost</span><span class="sxs-lookup"><span data-stu-id="07f25-138">ProjPeriodPostingLedgerSales.enterCost</span></span>|
|<span data-ttu-id="07f25-139">ProjPeriodPostingLedgerSales.enterEmpl</span><span class="sxs-lookup"><span data-stu-id="07f25-139">ProjPeriodPostingLedgerSales.enterEmpl</span></span>|
|<span data-ttu-id="07f25-140">ProjPeriodPostingLedgerSales.enterRevenue</span><span class="sxs-lookup"><span data-stu-id="07f25-140">ProjPeriodPostingLedgerSales.enterRevenue</span></span>|
|<span data-ttu-id="07f25-141">ProjPeriodPostingLedgerSales.run</span><span class="sxs-lookup"><span data-stu-id="07f25-141">ProjPeriodPostingLedgerSales.run</span></span>|
|<span data-ttu-id="07f25-142">ProjPlanVersionsManager.CopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="07f25-142">ProjPlanVersionsManager.CopyHierarchy</span></span>|
|<span data-ttu-id="07f25-143">ProjPlanVersionsManager::CopyHierarchy</span><span class="sxs-lookup"><span data-stu-id="07f25-143">ProjPlanVersionsManager::copyHierarchy</span></span>|
|<span data-ttu-id="07f25-144">ProjPlanVersionsManager::createDraftVersion</span><span class="sxs-lookup"><span data-stu-id="07f25-144">ProjPlanVersionsManager::createDraftVersion</span></span>|
|<span data-ttu-id="07f25-145">ProjPlanVersionsManager::createTemplateHierarchy</span><span class="sxs-lookup"><span data-stu-id="07f25-145">ProjPlanVersionsManager::createTemplateHierarchy</span></span>|
|<span data-ttu-id="07f25-146">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span><span class="sxs-lookup"><span data-stu-id="07f25-146">PurchAutoCreate_PurchReq.initializeAndCreatePurchLine</span></span>|
|<span data-ttu-id="07f25-147">PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span><span class="sxs-lookup"><span data-stu-id="07f25-147">PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap</span></span>|
|<span data-ttu-id="07f25-148">PurchRFQPriceDiscAdmCreate.createPriceDiscAdmTrans</span><span class="sxs-lookup"><span data-stu-id="07f25-148">PurchRFQPriceDiscAdmCreate.createPriceDiscAdmTrans</span></span>|
|<span data-ttu-id="07f25-149">SalesFormLetter.validate</span><span class="sxs-lookup"><span data-stu-id="07f25-149">SalesFormLetter.validate</span></span>|
|<span data-ttu-id="07f25-150">SalesTable2LineUpdatePrompt.salesTableFieldModifiedHandler</span><span class="sxs-lookup"><span data-stu-id="07f25-150">SalesTable2LineUpdatePrompt.salesTableFieldModifiedHandler</span></span>|
|<span data-ttu-id="07f25-151">SalesUpdateRemain.cancelOpenOrderLinesDeliveryRemainder</span><span class="sxs-lookup"><span data-stu-id="07f25-151">SalesUpdateRemain.cancelOpenOrderLinesDeliveryRemainder</span></span>|
|<span data-ttu-id="07f25-152">WHSShipmentTable.createShipmentNotes</span><span class="sxs-lookup"><span data-stu-id="07f25-152">WHSShipmentTable.createShipmentNotes</span></span>|
|<span data-ttu-id="07f25-153">WHSUnShipLoadLineTmpDataCreator.createTmpLoadLineInventoryFromContainerLines</span><span class="sxs-lookup"><span data-stu-id="07f25-153">WHSUnShipLoadLineTmpDataCreator.createTmpLoadLineInventoryFromContainerLines</span></span>|

## <a name="additional-extensibility-enhancements"></a><span data-ttu-id="07f25-154">追加の拡張性強化</span><span class="sxs-lookup"><span data-stu-id="07f25-154">Additional extensibility enhancements</span></span>

<span data-ttu-id="07f25-155">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="07f25-155">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="07f25-156">拡張子からマップのサポート: CustVendTrans</span><span class="sxs-lookup"><span data-stu-id="07f25-156">Support for extensions to map: CustVendTrans</span></span>
- <span data-ttu-id="07f25-157">拡張子からマップのサポート: CustVendTransOpen</span><span class="sxs-lookup"><span data-stu-id="07f25-157">Support for extensions to map: CustVendTransOpen</span></span>
- <span data-ttu-id="07f25-158">SQL 明細書の機能拡張をサポート: PriceDiscAdmCheckPost.postJournal</span><span class="sxs-lookup"><span data-stu-id="07f25-158">Support extensibility for SQL statement:  PriceDiscAdmCheckPost.postJournal</span></span>
