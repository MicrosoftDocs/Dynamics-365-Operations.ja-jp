---
title: "Finance and Operations 更新プログラム 8.0.1 の拡張機能の変更"
description: "このトピックでは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.1 でリリースされた拡張機能を一覧表示します。"
author: FrankDahl
manager: AnnBe
ms.date: 05/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: App 8.0.1
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: e1e1b716a0bd15cc4a1ef47d8b8e741bce38a040
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="extensibility-changes-in-finance-and-operations-update-801"></a><span data-ttu-id="19c7a-103">Finance and Operations 更新プログラム 8.0.1 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="19c7a-103">Extensibility changes in Finance and Operations update 8.0.1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19c7a-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.1 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="19c7a-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.1.</span></span> <span data-ttu-id="19c7a-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19c7a-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="19c7a-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="19c7a-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="19c7a-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="19c7a-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="19c7a-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="19c7a-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="19c7a-109">クラス ProjControlPeriod::PeriodInsert</span><span class="sxs-lookup"><span data-stu-id="19c7a-109">Class ProjControlPeriod::PeriodInsert</span></span>|
|<span data-ttu-id="19c7a-110">クラス ProjInvoiceChoose::doSalesLine</span><span class="sxs-lookup"><span data-stu-id="19c7a-110">Class ProjInvoiceChoose::doSalesLine</span></span>|
|<span data-ttu-id="19c7a-111">クラス CustInvoiceJour::printFreeTextJournal</span><span class="sxs-lookup"><span data-stu-id="19c7a-111">Class CustInvoiceJour::printFreeTextJournal</span></span>|
|<span data-ttu-id="19c7a-112">クラス ProjCostControl.createEmptyTransactionType</span><span class="sxs-lookup"><span data-stu-id="19c7a-112">Class ProjCostControl.createEmptyTransactionType</span></span>|
|<span data-ttu-id="19c7a-113">クラス ProjEstimate::autoGenerateEstimateLinesFromTask</span><span class="sxs-lookup"><span data-stu-id="19c7a-113">Class ProjEstimate::autoGenerateEstimateLinesFromTask</span></span>|
|<span data-ttu-id="19c7a-114">クラス ProjEstimateDataContract.updateEstimates</span><span class="sxs-lookup"><span data-stu-id="19c7a-114">Class ProjEstimateDataContract.updateEstimates</span></span>|
|<span data-ttu-id="19c7a-115">クラス ProjForecastBudget.Run</span><span class="sxs-lookup"><span data-stu-id="19c7a-115">Class ProjForecastBudget.Run</span></span>|
|<span data-ttu-id="19c7a-116">クラス ProjHierarchyProvider.preDeleteHierarchy</span><span class="sxs-lookup"><span data-stu-id="19c7a-116">Class ProjHierarchyProvider.preDeleteHierarchy</span></span>|
|<span data-ttu-id="19c7a-117">クラス ProjPlanVersionsManager::CopyTasks</span><span class="sxs-lookup"><span data-stu-id="19c7a-117">Class ProjPlanVersionsManager::CopyTasks</span></span>|
|<span data-ttu-id="19c7a-118">クラス ProjPlanVersionsManager.createDraftFromPublishedVersion</span><span class="sxs-lookup"><span data-stu-id="19c7a-118">Class ProjPlanVersionsManager.createDraftFromPublishedVersion</span></span>|
|<span data-ttu-id="19c7a-119">クラス ProjPlanVersionsManager.PublishQuotationSubHierarchy</span><span class="sxs-lookup"><span data-stu-id="19c7a-119">Class ProjPlanVersionsManager.PublishQuotationSubHierarchy</span></span>|
|<span data-ttu-id="19c7a-120">クラス ProjPlanVersionsManager.CreateDraftVersion</span><span class="sxs-lookup"><span data-stu-id="19c7a-120">Class ProjPlanVersionsManager.CreateDraftVersion</span></span>|
|<span data-ttu-id="19c7a-121">クラス ProjTask.addTask</span><span class="sxs-lookup"><span data-stu-id="19c7a-121">Class ProjTask.addTask</span></span>|
|<span data-ttu-id="19c7a-122">クラス ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span><span class="sxs-lookup"><span data-stu-id="19c7a-122">Class ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span></span>|
|<span data-ttu-id="19c7a-123">クラス VendOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="19c7a-123">Class VendOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="19c7a-124">クラス CustVendReversePosting.reverseTaxWithholdTrans</span><span class="sxs-lookup"><span data-stu-id="19c7a-124">Class CustVendReversePosting.reverseTaxWithholdTrans</span></span>|
|<span data-ttu-id="19c7a-125">クラス CustVendSettle.postPennyDiff</span><span class="sxs-lookup"><span data-stu-id="19c7a-125">Class CustVendSettle.postPennyDiff</span></span>|
|<span data-ttu-id="19c7a-126">クラス CustVendSettle.processStillOpenTransactions</span><span class="sxs-lookup"><span data-stu-id="19c7a-126">Class CustVendSettle.processStillOpenTransactions</span></span>|
|<span data-ttu-id="19c7a-127">クラス InventTransferOrderOverviewDP.insertTmp</span><span class="sxs-lookup"><span data-stu-id="19c7a-127">Class InventTransferOrderOverviewDP.insertTmp</span></span>|
|<span data-ttu-id="19c7a-128">クラス LedgerJournalTransCost.LedgerJournalTrans.Create</span><span class="sxs-lookup"><span data-stu-id="19c7a-128">Class LedgerJournalTransCost.LedgerJournalTrans.Create</span></span>|
|<span data-ttu-id="19c7a-129">クラス ProjAdjustmentSelect.dialog</span><span class="sxs-lookup"><span data-stu-id="19c7a-129">Class ProjAdjustmentSelect.dialog</span></span>|
|<span data-ttu-id="19c7a-130">クラス ProjEstimate.syncEstimateLinesFromTask</span><span class="sxs-lookup"><span data-stu-id="19c7a-130">Class ProjEstimate.syncEstimateLinesFromTask</span></span>|
|<span data-ttu-id="19c7a-131">クラス ProjEstimateDataContract.UpdateEstimates</span><span class="sxs-lookup"><span data-stu-id="19c7a-131">Class ProjEstimateDataContract.UpdateEstimates</span></span>|
|<span data-ttu-id="19c7a-132">クラス ProjForecastTransferFromWbs.transferToForecast</span><span class="sxs-lookup"><span data-stu-id="19c7a-132">Class ProjForecastTransferFromWbs.transferToForecast</span></span>|
|<span data-ttu-id="19c7a-133">クラス ProjWizardActivityCtrl.insertDBOnServer</span><span class="sxs-lookup"><span data-stu-id="19c7a-133">Class ProjWizardActivityCtrl.insertDBOnServer</span></span>|
|<span data-ttu-id="19c7a-134">クラス ProjTaskEstimatesSynchronizer.calcTotalEstimateLineHours</span><span class="sxs-lookup"><span data-stu-id="19c7a-134">Class ProjTaskEstimatesSynchronizer.calcTotalEstimateLineHours</span></span>|
|<span data-ttu-id="19c7a-135">クラス ProjTaskEstimatesSynchronizer.countNumberOfHourEstimateLines</span><span class="sxs-lookup"><span data-stu-id="19c7a-135">Class ProjTaskEstimatesSynchronizer.countNumberOfHourEstimateLines</span></span>|
|<span data-ttu-id="19c7a-136">クラス ProjTaskEstimatesSynchronizer.syncExistingHourEstimatesWithTask</span><span class="sxs-lookup"><span data-stu-id="19c7a-136">Class ProjTaskEstimatesSynchronizer.syncExistingHourEstimatesWithTask</span></span>|
|<span data-ttu-id="19c7a-137">クラス ProjTaskEstimatesSynchronizer.syncHourEstimatesWithTaskEffort</span><span class="sxs-lookup"><span data-stu-id="19c7a-137">Class ProjTaskEstimatesSynchronizer.syncHourEstimatesWithTaskEffort</span></span>|
|<span data-ttu-id="19c7a-138">クラス ProjWbsCostPlanningServerActions.executeDataRetrievalAction</span><span class="sxs-lookup"><span data-stu-id="19c7a-138">Class ProjWbsCostPlanningServerActions.executeDataRetrievalAction</span></span>|
|<span data-ttu-id="19c7a-139">クラス ProjWbsCostPlanningServerActions.getProjectCategoryTypes</span><span class="sxs-lookup"><span data-stu-id="19c7a-139">Class ProjWbsCostPlanningServerActions.getProjectCategoryTypes</span></span>|
|<span data-ttu-id="19c7a-140">クラス ProjWbsSchedulePlanningServerActions.executeAction</span><span class="sxs-lookup"><span data-stu-id="19c7a-140">Class ProjWbsSchedulePlanningServerActions.executeAction</span></span>|
|<span data-ttu-id="19c7a-141">クラス ProjWbsSchedulePlanningServerActions.executeDataRetrievalAction</span><span class="sxs-lookup"><span data-stu-id="19c7a-141">Class ProjWbsSchedulePlanningServerActions.executeDataRetrievalAction</span></span>|
|<span data-ttu-id="19c7a-142">クラス ProjStatisticCalc.validate</span><span class="sxs-lookup"><span data-stu-id="19c7a-142">Class ProjStatisticCalc.validate</span></span>|
|<span data-ttu-id="19c7a-143">クラス WHSInventReserve.insert</span><span class="sxs-lookup"><span data-stu-id="19c7a-143">Class WHSInventReserve.insert</span></span>|
|<span data-ttu-id="19c7a-144">クラス WHSInventReserveDelta.insert</span><span class="sxs-lookup"><span data-stu-id="19c7a-144">Class WHSInventReserveDelta.insert</span></span>|
|<span data-ttu-id="19c7a-145">クラス ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span><span class="sxs-lookup"><span data-stu-id="19c7a-145">Class ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span></span>|
|<span data-ttu-id="19c7a-146">クラス ProjJournalTransEmpl - Datasource: ProjJournalTrans.Validate</span><span class="sxs-lookup"><span data-stu-id="19c7a-146">Class ProjJournalTransEmpl - Datasource: ProjJournalTrans.Validate</span></span>|
|<span data-ttu-id="19c7a-147">クラス LedgerJournalEngine.initTaxItemGroup</span><span class="sxs-lookup"><span data-stu-id="19c7a-147">Class LedgerJournalEngine.initTaxItemGroup</span></span>|
|<span data-ttu-id="19c7a-148">クラス LedgerJournalEngine.initValue</span><span class="sxs-lookup"><span data-stu-id="19c7a-148">Class LedgerJournalEngine.initValue</span></span>|
|<span data-ttu-id="19c7a-149">クラス ProjJournalTrans.mergeResourceDimensionDefault</span><span class="sxs-lookup"><span data-stu-id="19c7a-149">Class ProjJournalTrans.mergeResourceDimensionDefault</span></span>|
|<span data-ttu-id="19c7a-150">クラス ProjTask.setTaskinfo</span><span class="sxs-lookup"><span data-stu-id="19c7a-150">Class ProjTask.setTaskinfo</span></span>|
|<span data-ttu-id="19c7a-151">クラス ProjJournalName.standardJournalName</span><span class="sxs-lookup"><span data-stu-id="19c7a-151">Class ProjJournalName.standardJournalName</span></span>|
|<span data-ttu-id="19c7a-152">フォーム ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span><span class="sxs-lookup"><span data-stu-id="19c7a-152">Form ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span></span>|

## <a name="other-extensibility-enhancements"></a><span data-ttu-id="19c7a-153">その他の拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="19c7a-153">Other extensibility enhancements</span></span>

<span data-ttu-id="19c7a-154">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="19c7a-154">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="19c7a-155">小数点以下の変数番号のサポート - InventTestLowerLimit</span><span class="sxs-lookup"><span data-stu-id="19c7a-155">Support variable number of decimals - InventTestLowerLimit</span></span>
- <span data-ttu-id="19c7a-156">小数点以下の変数番号のサポート - InventTestLowerTolerance</span><span class="sxs-lookup"><span data-stu-id="19c7a-156">Support variable number of decimals -  InventTestLowerTolerance</span></span>
- <span data-ttu-id="19c7a-157">小数点以下の変数番号のサポート - InventTestStandardValue</span><span class="sxs-lookup"><span data-stu-id="19c7a-157">Support variable number of decimals -  InventTestStandardValue</span></span> 
- <span data-ttu-id="19c7a-158">小数点以下の変数番号のサポート - InventTestUpperLimit</span><span class="sxs-lookup"><span data-stu-id="19c7a-158">Support variable number of decimals -  InventTestUpperLimit</span></span>
- <span data-ttu-id="19c7a-159">小数点以下の変数番号のサポート - InventTestUpperTolerance</span><span class="sxs-lookup"><span data-stu-id="19c7a-159">Support variable number of decimals - InventTestUpperTolerance</span></span>
- <span data-ttu-id="19c7a-160">トランザクションの取消でスキップ確認をサポートします。</span><span class="sxs-lookup"><span data-stu-id="19c7a-160">Support to skip prompt on transaction reversal</span></span>
- <span data-ttu-id="19c7a-161">PSAProjQuotationApproval ワークフローの拡張機能の有効化</span><span class="sxs-lookup"><span data-stu-id="19c7a-161">Enable extension of PSAProjQuotationApproval workflow</span></span>

