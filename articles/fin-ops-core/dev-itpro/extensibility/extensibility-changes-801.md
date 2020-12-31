---
title: Finance and Operations 更新プログラム 8.0.1 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.1 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 05/17/2018
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
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: App 8.0.1
ms.openlocfilehash: 6c06e76c1a20547219ecc0106f340e154e5d611b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409342"
---
# <a name="extensibility-changes-in-finance-and-operations-update-801"></a><span data-ttu-id="77b01-103">Finance and Operations 更新プログラム 8.0.1 の拡張機能の変更</span><span class="sxs-lookup"><span data-stu-id="77b01-103">Extensibility changes in Finance and Operations update 8.0.1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77b01-104">これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.1 に実装された拡張機能の一覧です。</span><span class="sxs-lookup"><span data-stu-id="77b01-104">This is a list of extensibility features that were implemented in Dynamics 365 for Finance and Operations update 8.0.1.</span></span> <span data-ttu-id="77b01-105">拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="77b01-105">For more information about the schedule of changes that support extensibility, see [Application extensibility plans](extensibility-roadmap.md).</span></span>

## <a name="refactored-methods-to-support-extensibility"></a><span data-ttu-id="77b01-106">拡張性をサポートするためにリファクターされたメソッド</span><span class="sxs-lookup"><span data-stu-id="77b01-106">Refactored methods to support extensibility</span></span>

<span data-ttu-id="77b01-107">これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="77b01-107">These methods have been refactored to support extensibility through chain of command, delegates, or by providing access to members.</span></span>

| <span data-ttu-id="77b01-108">方法</span><span class="sxs-lookup"><span data-stu-id="77b01-108">Method</span></span>|
| --------------- |
|<span data-ttu-id="77b01-109">クラス ProjControlPeriod::PeriodInsert</span><span class="sxs-lookup"><span data-stu-id="77b01-109">Class ProjControlPeriod::PeriodInsert</span></span>|
|<span data-ttu-id="77b01-110">クラス ProjInvoiceChoose::doSalesLine</span><span class="sxs-lookup"><span data-stu-id="77b01-110">Class ProjInvoiceChoose::doSalesLine</span></span>|
|<span data-ttu-id="77b01-111">クラス CustInvoiceJour::printFreeTextJournal</span><span class="sxs-lookup"><span data-stu-id="77b01-111">Class CustInvoiceJour::printFreeTextJournal</span></span>|
|<span data-ttu-id="77b01-112">クラス ProjCostControl.createEmptyTransactionType</span><span class="sxs-lookup"><span data-stu-id="77b01-112">Class ProjCostControl.createEmptyTransactionType</span></span>|
|<span data-ttu-id="77b01-113">クラス ProjEstimate::autoGenerateEstimateLinesFromTask</span><span class="sxs-lookup"><span data-stu-id="77b01-113">Class ProjEstimate::autoGenerateEstimateLinesFromTask</span></span>|
|<span data-ttu-id="77b01-114">クラス ProjEstimateDataContract.updateEstimates</span><span class="sxs-lookup"><span data-stu-id="77b01-114">Class ProjEstimateDataContract.updateEstimates</span></span>|
|<span data-ttu-id="77b01-115">クラス ProjForecastBudget.Run</span><span class="sxs-lookup"><span data-stu-id="77b01-115">Class ProjForecastBudget.Run</span></span>|
|<span data-ttu-id="77b01-116">クラス ProjHierarchyProvider.preDeleteHierarchy</span><span class="sxs-lookup"><span data-stu-id="77b01-116">Class ProjHierarchyProvider.preDeleteHierarchy</span></span>|
|<span data-ttu-id="77b01-117">クラス ProjPlanVersionsManager::CopyTasks</span><span class="sxs-lookup"><span data-stu-id="77b01-117">Class ProjPlanVersionsManager::CopyTasks</span></span>|
|<span data-ttu-id="77b01-118">クラス ProjPlanVersionsManager.createDraftFromPublishedVersion</span><span class="sxs-lookup"><span data-stu-id="77b01-118">Class ProjPlanVersionsManager.createDraftFromPublishedVersion</span></span>|
|<span data-ttu-id="77b01-119">クラス ProjPlanVersionsManager.PublishQuotationSubHierarchy</span><span class="sxs-lookup"><span data-stu-id="77b01-119">Class ProjPlanVersionsManager.PublishQuotationSubHierarchy</span></span>|
|<span data-ttu-id="77b01-120">クラス ProjPlanVersionsManager.CreateDraftVersion</span><span class="sxs-lookup"><span data-stu-id="77b01-120">Class ProjPlanVersionsManager.CreateDraftVersion</span></span>|
|<span data-ttu-id="77b01-121">クラス ProjTask.addTask</span><span class="sxs-lookup"><span data-stu-id="77b01-121">Class ProjTask.addTask</span></span>|
|<span data-ttu-id="77b01-122">クラス ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span><span class="sxs-lookup"><span data-stu-id="77b01-122">Class ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span></span>|
|<span data-ttu-id="77b01-123">クラス VendOpenTrans.editMarkTrans</span><span class="sxs-lookup"><span data-stu-id="77b01-123">Class VendOpenTrans.editMarkTrans</span></span>|
|<span data-ttu-id="77b01-124">クラス CustVendReversePosting.reverseTaxWithholdTrans</span><span class="sxs-lookup"><span data-stu-id="77b01-124">Class CustVendReversePosting.reverseTaxWithholdTrans</span></span>|
|<span data-ttu-id="77b01-125">クラス CustVendSettle.postPennyDiff</span><span class="sxs-lookup"><span data-stu-id="77b01-125">Class CustVendSettle.postPennyDiff</span></span>|
|<span data-ttu-id="77b01-126">クラス CustVendSettle.processStillOpenTransactions</span><span class="sxs-lookup"><span data-stu-id="77b01-126">Class CustVendSettle.processStillOpenTransactions</span></span>|
|<span data-ttu-id="77b01-127">クラス InventTransferOrderOverviewDP.insertTmp</span><span class="sxs-lookup"><span data-stu-id="77b01-127">Class InventTransferOrderOverviewDP.insertTmp</span></span>|
|<span data-ttu-id="77b01-128">クラス LedgerJournalTransCost.LedgerJournalTrans.Create</span><span class="sxs-lookup"><span data-stu-id="77b01-128">Class LedgerJournalTransCost.LedgerJournalTrans.Create</span></span>|
|<span data-ttu-id="77b01-129">クラス ProjAdjustmentSelect.dialog</span><span class="sxs-lookup"><span data-stu-id="77b01-129">Class ProjAdjustmentSelect.dialog</span></span>|
|<span data-ttu-id="77b01-130">クラス ProjEstimate.syncEstimateLinesFromTask</span><span class="sxs-lookup"><span data-stu-id="77b01-130">Class ProjEstimate.syncEstimateLinesFromTask</span></span>|
|<span data-ttu-id="77b01-131">クラス ProjEstimateDataContract.UpdateEstimates</span><span class="sxs-lookup"><span data-stu-id="77b01-131">Class ProjEstimateDataContract.UpdateEstimates</span></span>|
|<span data-ttu-id="77b01-132">クラス ProjForecastTransferFromWbs.transferToForecast</span><span class="sxs-lookup"><span data-stu-id="77b01-132">Class ProjForecastTransferFromWbs.transferToForecast</span></span>|
|<span data-ttu-id="77b01-133">クラス ProjWizardActivityCtrl.insertDBOnServer</span><span class="sxs-lookup"><span data-stu-id="77b01-133">Class ProjWizardActivityCtrl.insertDBOnServer</span></span>|
|<span data-ttu-id="77b01-134">クラス ProjTaskEstimatesSynchronizer.calcTotalEstimateLineHours</span><span class="sxs-lookup"><span data-stu-id="77b01-134">Class ProjTaskEstimatesSynchronizer.calcTotalEstimateLineHours</span></span>|
|<span data-ttu-id="77b01-135">クラス ProjTaskEstimatesSynchronizer.countNumberOfHourEstimateLines</span><span class="sxs-lookup"><span data-stu-id="77b01-135">Class ProjTaskEstimatesSynchronizer.countNumberOfHourEstimateLines</span></span>|
|<span data-ttu-id="77b01-136">クラス ProjTaskEstimatesSynchronizer.syncExistingHourEstimatesWithTask</span><span class="sxs-lookup"><span data-stu-id="77b01-136">Class ProjTaskEstimatesSynchronizer.syncExistingHourEstimatesWithTask</span></span>|
|<span data-ttu-id="77b01-137">クラス ProjTaskEstimatesSynchronizer.syncHourEstimatesWithTaskEffort</span><span class="sxs-lookup"><span data-stu-id="77b01-137">Class ProjTaskEstimatesSynchronizer.syncHourEstimatesWithTaskEffort</span></span>|
|<span data-ttu-id="77b01-138">クラス ProjWbsCostPlanningServerActions.executeDataRetrievalAction</span><span class="sxs-lookup"><span data-stu-id="77b01-138">Class ProjWbsCostPlanningServerActions.executeDataRetrievalAction</span></span>|
|<span data-ttu-id="77b01-139">クラス ProjWbsCostPlanningServerActions.getProjectCategoryTypes</span><span class="sxs-lookup"><span data-stu-id="77b01-139">Class ProjWbsCostPlanningServerActions.getProjectCategoryTypes</span></span>|
|<span data-ttu-id="77b01-140">クラス ProjWbsSchedulePlanningServerActions.executeAction</span><span class="sxs-lookup"><span data-stu-id="77b01-140">Class ProjWbsSchedulePlanningServerActions.executeAction</span></span>|
|<span data-ttu-id="77b01-141">クラス ProjWbsSchedulePlanningServerActions.executeDataRetrievalAction</span><span class="sxs-lookup"><span data-stu-id="77b01-141">Class ProjWbsSchedulePlanningServerActions.executeDataRetrievalAction</span></span>|
|<span data-ttu-id="77b01-142">クラス ProjStatisticCalc.validate</span><span class="sxs-lookup"><span data-stu-id="77b01-142">Class ProjStatisticCalc.validate</span></span>|
|<span data-ttu-id="77b01-143">クラス WHSInventReserve.insert</span><span class="sxs-lookup"><span data-stu-id="77b01-143">Class WHSInventReserve.insert</span></span>|
|<span data-ttu-id="77b01-144">クラス WHSInventReserveDelta.insert</span><span class="sxs-lookup"><span data-stu-id="77b01-144">Class WHSInventReserveDelta.insert</span></span>|
|<span data-ttu-id="77b01-145">クラス ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span><span class="sxs-lookup"><span data-stu-id="77b01-145">Class ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span></span>|
|<span data-ttu-id="77b01-146">クラス ProjJournalTransEmpl - Datasource: ProjJournalTrans.Validate</span><span class="sxs-lookup"><span data-stu-id="77b01-146">Class ProjJournalTransEmpl - Datasource: ProjJournalTrans.Validate</span></span>|
|<span data-ttu-id="77b01-147">クラス LedgerJournalEngine.initTaxItemGroup</span><span class="sxs-lookup"><span data-stu-id="77b01-147">Class LedgerJournalEngine.initTaxItemGroup</span></span>|
|<span data-ttu-id="77b01-148">クラス LedgerJournalEngine.initValue</span><span class="sxs-lookup"><span data-stu-id="77b01-148">Class LedgerJournalEngine.initValue</span></span>|
|<span data-ttu-id="77b01-149">クラス ProjJournalTrans.mergeResourceDimensionDefault</span><span class="sxs-lookup"><span data-stu-id="77b01-149">Class ProjJournalTrans.mergeResourceDimensionDefault</span></span>|
|<span data-ttu-id="77b01-150">クラス ProjTask.setTaskinfo</span><span class="sxs-lookup"><span data-stu-id="77b01-150">Class ProjTask.setTaskinfo</span></span>|
|<span data-ttu-id="77b01-151">クラス ProjJournalName.standardJournalName</span><span class="sxs-lookup"><span data-stu-id="77b01-151">Class ProjJournalName.standardJournalName</span></span>|
|<span data-ttu-id="77b01-152">フォーム ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span><span class="sxs-lookup"><span data-stu-id="77b01-152">Form ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup</span></span>|

## <a name="other-extensibility-enhancements"></a><span data-ttu-id="77b01-153">その他の拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="77b01-153">Other extensibility enhancements</span></span>

<span data-ttu-id="77b01-154">リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。</span><span class="sxs-lookup"><span data-stu-id="77b01-154">In addition to the refactored methods, the following extensibility enhancements have been made.</span></span>

- <span data-ttu-id="77b01-155">小数点以下の変数番号のサポート - InventTestLowerLimit</span><span class="sxs-lookup"><span data-stu-id="77b01-155">Support variable number of decimals - InventTestLowerLimit</span></span>
- <span data-ttu-id="77b01-156">小数点以下の変数番号のサポート - InventTestLowerTolerance</span><span class="sxs-lookup"><span data-stu-id="77b01-156">Support variable number of decimals -  InventTestLowerTolerance</span></span>
- <span data-ttu-id="77b01-157">小数点以下の変数番号のサポート - InventTestStandardValue</span><span class="sxs-lookup"><span data-stu-id="77b01-157">Support variable number of decimals -  InventTestStandardValue</span></span> 
- <span data-ttu-id="77b01-158">小数点以下の変数番号のサポート - InventTestUpperLimit</span><span class="sxs-lookup"><span data-stu-id="77b01-158">Support variable number of decimals -  InventTestUpperLimit</span></span>
- <span data-ttu-id="77b01-159">小数点以下の変数番号のサポート - InventTestUpperTolerance</span><span class="sxs-lookup"><span data-stu-id="77b01-159">Support variable number of decimals - InventTestUpperTolerance</span></span>
- <span data-ttu-id="77b01-160">トランザクションの取消でスキップ確認をサポートします。</span><span class="sxs-lookup"><span data-stu-id="77b01-160">Support to skip prompt on transaction reversal</span></span>
- <span data-ttu-id="77b01-161">PSAProjQuotationApproval ワークフローの拡張機能の有効化</span><span class="sxs-lookup"><span data-stu-id="77b01-161">Enable extension of PSAProjQuotationApproval workflow</span></span>
