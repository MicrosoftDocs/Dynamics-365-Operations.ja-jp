---
title: Warehouse Management モバイル アプリのステップ アイコンとタイトルの割り当て
description: このトピックでは、Warehouse Management モバイル アプリの新しいタスク フローまたはカスタマイズされたタスク フローに対してステップ アイコンとタイトルを割り当てる方法について説明します。
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049367"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="36802-103">Warehouse Management モバイル アプリのステップ アイコンとタイトルの割り当て</span><span class="sxs-lookup"><span data-stu-id="36802-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36802-104">このトピックでは、Warehouse Management モバイル アプリの新しいタスク フローまたはカスタマイズされたタスク フローに対してステップ アイコンとステップ タイトルを割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="36802-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="36802-105">次の図は、Warehouse Management モバイル アプリにステップ アイコンとタイトルがどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="36802-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="36802-106">![Warehouse Management モバイル アプリのステップ アイコンとステップ タイトルの例](media/step-icon-example.png "Warehouse Management モバイル アプリのステップ アイコンとステップ タイトルの例")</span><span class="sxs-lookup"><span data-stu-id="36802-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="36802-107">システムでこの機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="36802-107">Turn on this feature in your system</span></span>

<span data-ttu-id="36802-108">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="36802-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="36802-109">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="36802-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="36802-110">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="36802-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="36802-111">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="36802-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="36802-112">**機能名:** *新しい倉庫アプリのユーザー設定、アイコン、ステップ タイトル*</span><span class="sxs-lookup"><span data-stu-id="36802-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="36802-113">標準的なステップ ID、クラス、アイコン</span><span class="sxs-lookup"><span data-stu-id="36802-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="36802-114">タスク フローの各ステップはステップ ID で識別され、各ステップ ID には対応するステップ クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="36802-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="36802-115">ステップ アイコンおよびタイトルは各ステップ クラスで指定されます。</span><span class="sxs-lookup"><span data-stu-id="36802-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="36802-116">ステップ ID とステップ クラス</span><span class="sxs-lookup"><span data-stu-id="36802-116">Step IDs and step classes</span></span>

<span data-ttu-id="36802-117">次の表に、現在使用可能なすべてのステップ ID と、それに対応するステップ クラスの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="36802-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="36802-118">基本入力フィールドの制御名がステップ ID として使用されます。</span><span class="sxs-lookup"><span data-stu-id="36802-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="36802-119">これらのステップ ID およびクラスがどのように使用されるかを示す例については、このトピックで後述する [例: カスタム フローへのステップ アイコンとタイトルの割り当て](#example) セクションの `WHSMobileAppStepInfoBuilder.stepId()` メソッドの実装を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36802-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="36802-120">ステップ ID</span><span class="sxs-lookup"><span data-stu-id="36802-120">Step ID</span></span> | <span data-ttu-id="36802-121">ステップ クラス</span><span class="sxs-lookup"><span data-stu-id="36802-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="36802-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36802-122">BatchDisposition</span></span> | <span data-ttu-id="36802-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36802-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="36802-124">配送業者</span><span class="sxs-lookup"><span data-stu-id="36802-124">Carrier</span></span> | <span data-ttu-id="36802-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="36802-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="36802-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="36802-126">CatchWeight</span></span> | <span data-ttu-id="36802-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36802-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36802-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="36802-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="36802-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36802-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36802-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36802-130">CatchWeightTag</span></span> | <span data-ttu-id="36802-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36802-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="36802-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="36802-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="36802-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="36802-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="36802-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="36802-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="36802-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="36802-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="36802-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="36802-136">CheckDigit</span></span> | <span data-ttu-id="36802-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="36802-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="36802-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="36802-138">ClusterId</span></span> | <span data-ttu-id="36802-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="36802-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="36802-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36802-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="36802-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36802-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="36802-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="36802-142">ClusterPosition</span></span> | <span data-ttu-id="36802-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="36802-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="36802-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="36802-144">ConfigId</span></span> | <span data-ttu-id="36802-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="36802-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="36802-146">確認書</span><span class="sxs-lookup"><span data-stu-id="36802-146">Confirmation</span></span> | <span data-ttu-id="36802-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="36802-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="36802-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="36802-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="36802-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="36802-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="36802-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="36802-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="36802-154">ContainerType</span></span> | <span data-ttu-id="36802-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="36802-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="36802-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="36802-156">CountingReasonCode</span></span> | <span data-ttu-id="36802-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="36802-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="36802-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="36802-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="36802-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="36802-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="36802-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="36802-160">CycleCountQty1</span></span> | <span data-ttu-id="36802-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36802-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36802-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="36802-162">CycleCountQty2</span></span> | <span data-ttu-id="36802-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36802-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36802-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="36802-164">CycleCountQty3</span></span> | <span data-ttu-id="36802-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36802-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36802-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="36802-166">CycleCountQty4</span></span> | <span data-ttu-id="36802-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="36802-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="36802-168">Disposition</span><span class="sxs-lookup"><span data-stu-id="36802-168">Disposition</span></span> | <span data-ttu-id="36802-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="36802-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="36802-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="36802-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="36802-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="36802-172">DriverCheckInId</span></span> | <span data-ttu-id="36802-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="36802-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="36802-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="36802-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="36802-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="36802-176">DriverCheckOutId</span></span> | <span data-ttu-id="36802-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="36802-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="36802-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="36802-178">ExpDate</span></span> | <span data-ttu-id="36802-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="36802-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="36802-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36802-180">FromBatchDisposition</span></span> | <span data-ttu-id="36802-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36802-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="36802-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="36802-182">FromInventoryStatus</span></span> | <span data-ttu-id="36802-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="36802-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="36802-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="36802-184">FullQty</span></span> | <span data-ttu-id="36802-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="36802-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="36802-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="36802-186">InboundPut</span></span> | <span data-ttu-id="36802-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="36802-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="36802-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="36802-188">InventBatchId</span></span> | <span data-ttu-id="36802-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="36802-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="36802-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="36802-190">InventColorId</span></span> | <span data-ttu-id="36802-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="36802-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="36802-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="36802-192">InventLocation</span></span> | <span data-ttu-id="36802-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="36802-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="36802-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="36802-194">InventLocationId</span></span> | <span data-ttu-id="36802-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="36802-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="36802-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="36802-196">InventSerialId</span></span> | <span data-ttu-id="36802-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="36802-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="36802-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="36802-198">InventSizeId</span></span> | <span data-ttu-id="36802-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="36802-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="36802-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="36802-200">InventStatusId</span></span> | <span data-ttu-id="36802-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="36802-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="36802-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="36802-202">InventStyleId</span></span> | <span data-ttu-id="36802-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="36802-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="36802-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="36802-204">InventVersionId</span></span> | <span data-ttu-id="36802-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="36802-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="36802-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="36802-206">ItemId</span></span> | <span data-ttu-id="36802-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="36802-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="36802-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="36802-208">ITMContainerID</span></span> | <span data-ttu-id="36802-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="36802-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="36802-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="36802-210">ITMShipmentID</span></span> | <span data-ttu-id="36802-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="36802-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="36802-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="36802-212">KanbanCardId</span></span> | <span data-ttu-id="36802-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="36802-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="36802-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="36802-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="36802-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="36802-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="36802-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="36802-216">KanbanOrCardId</span></span> | <span data-ttu-id="36802-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="36802-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="36802-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-218">LicensePlateId</span></span> | <span data-ttu-id="36802-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="36802-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="36802-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="36802-220">LoadId</span></span> | <span data-ttu-id="36802-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="36802-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="36802-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="36802-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="36802-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="36802-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="36802-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="36802-224">LocOrLP</span></span> | <span data-ttu-id="36802-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="36802-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="36802-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="36802-226">LocOrLP_From</span></span> | <span data-ttu-id="36802-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="36802-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="36802-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="36802-228">LocOrLP_To</span></span> | <span data-ttu-id="36802-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="36802-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="36802-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="36802-230">LocOrLPCheck</span></span> | <span data-ttu-id="36802-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="36802-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="36802-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="36802-232">LocVerification</span></span> | <span data-ttu-id="36802-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="36802-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="36802-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="36802-234">LPAdjustIn</span></span> | <span data-ttu-id="36802-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="36802-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="36802-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="36802-236">LPBreakChildLP</span></span> | <span data-ttu-id="36802-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="36802-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="36802-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="36802-238">LPBreakParentLP</span></span> | <span data-ttu-id="36802-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="36802-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="36802-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="36802-240">LPBuildChildLP</span></span> | <span data-ttu-id="36802-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="36802-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="36802-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="36802-242">LPBuildParentLP</span></span> | <span data-ttu-id="36802-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="36802-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="36802-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="36802-244">LPVerification</span></span> | <span data-ttu-id="36802-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="36802-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="36802-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="36802-246">MergeContainerId</span></span> | <span data-ttu-id="36802-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="36802-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="36802-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-248">MixedLPLineNum</span></span> | <span data-ttu-id="36802-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="36802-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="36802-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="36802-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="36802-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="36802-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="36802-252">MovementConfirmCancel</span></span> | <span data-ttu-id="36802-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="36802-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="36802-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="36802-254">NewCaptureWeight</span></span> | <span data-ttu-id="36802-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36802-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36802-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="36802-256">NewQty</span></span> | <span data-ttu-id="36802-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="36802-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="36802-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36802-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="36802-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36802-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="36802-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="36802-260">OutboundPut</span></span> | <span data-ttu-id="36802-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="36802-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="36802-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="36802-262">OutboundWeight</span></span> | <span data-ttu-id="36802-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="36802-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="36802-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="36802-264">OverridePutNewLocation</span></span> | <span data-ttu-id="36802-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="36802-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="36802-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="36802-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36802-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="36802-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-268">POLineNum</span></span> | <span data-ttu-id="36802-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="36802-270">発注書番号</span><span class="sxs-lookup"><span data-stu-id="36802-270">PONum</span></span> | <span data-ttu-id="36802-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="36802-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="36802-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="36802-272">PositionFull</span></span> | <span data-ttu-id="36802-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="36802-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="36802-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="36802-274">PositionFullQty</span></span> | <span data-ttu-id="36802-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="36802-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="36802-276">ポテンシー</span><span class="sxs-lookup"><span data-stu-id="36802-276">Potency</span></span> | <span data-ttu-id="36802-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="36802-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="36802-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="36802-278">PrinterName</span></span> | <span data-ttu-id="36802-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="36802-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="36802-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="36802-280">ProdId</span></span> | <span data-ttu-id="36802-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="36802-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="36802-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="36802-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="36802-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-284">ProductConfirmation</span></span> | <span data-ttu-id="36802-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="36802-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="36802-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="36802-288">プット</span><span class="sxs-lookup"><span data-stu-id="36802-288">Put</span></span> | <span data-ttu-id="36802-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="36802-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="36802-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="36802-290">PutawayClusterId</span></span> | <span data-ttu-id="36802-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="36802-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="36802-292">数量</span><span class="sxs-lookup"><span data-stu-id="36802-292">Qty</span></span> | <span data-ttu-id="36802-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="36802-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="36802-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="36802-294">QtyAdjust</span></span> | <span data-ttu-id="36802-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="36802-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="36802-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="36802-296">QtyShort</span></span> | <span data-ttu-id="36802-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="36802-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="36802-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="36802-298">QtyToConsume</span></span> | <span data-ttu-id="36802-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="36802-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="36802-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="36802-300">QtyToPick</span></span> | <span data-ttu-id="36802-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="36802-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="36802-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="36802-302">QtyToPut</span></span> | <span data-ttu-id="36802-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="36802-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="36802-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="36802-304">QtyToScrap</span></span> | <span data-ttu-id="36802-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="36802-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="36802-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="36802-306">QtyVerification</span></span> | <span data-ttu-id="36802-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="36802-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="36802-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="36802-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="36802-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="36802-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="36802-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="36802-310">ReasonString</span></span> | <span data-ttu-id="36802-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="36802-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="36802-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="36802-312">RecvLocationId</span></span> | <span data-ttu-id="36802-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="36802-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="36802-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="36802-314">RemoveContainerId</span></span> | <span data-ttu-id="36802-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="36802-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="36802-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="36802-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="36802-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="36802-318">RMANum</span></span> | <span data-ttu-id="36802-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="36802-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="36802-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="36802-320">ShortPickReason</span></span> | <span data-ttu-id="36802-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="36802-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="36802-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="36802-322">SortConOrLP</span></span> | <span data-ttu-id="36802-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="36802-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="36802-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-324">SortLicensePlateId</span></span> | <span data-ttu-id="36802-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="36802-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="36802-326">SortPositionId</span></span> | <span data-ttu-id="36802-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="36802-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="36802-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="36802-328">SortVerification</span></span> | <span data-ttu-id="36802-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="36802-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="36802-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="36802-330">StartLocationId</span></span> | <span data-ttu-id="36802-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="36802-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="36802-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="36802-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="36802-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-334">TargetLicensePlateId</span></span> | <span data-ttu-id="36802-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="36802-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-336">TOLineNum</span></span> | <span data-ttu-id="36802-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="36802-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="36802-338">ToLocation</span></span> | <span data-ttu-id="36802-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="36802-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="36802-340">TONum</span><span class="sxs-lookup"><span data-stu-id="36802-340">TONum</span></span> | <span data-ttu-id="36802-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="36802-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="36802-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="36802-342">ToWarehouse</span></span> | <span data-ttu-id="36802-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="36802-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="36802-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="36802-344">TransportLoadId</span></span> | <span data-ttu-id="36802-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="36802-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="36802-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="36802-346">WaveLabelId</span></span> | <span data-ttu-id="36802-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="36802-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="36802-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="36802-348">WaveLblQty</span></span> | <span data-ttu-id="36802-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="36802-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="36802-350">太さ</span><span class="sxs-lookup"><span data-stu-id="36802-350">Weight</span></span> | <span data-ttu-id="36802-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="36802-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="36802-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="36802-352">WeightToConsume</span></span> | <span data-ttu-id="36802-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="36802-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="36802-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="36802-354">WHSAdjustmentType</span></span> | <span data-ttu-id="36802-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="36802-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="36802-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="36802-356">WHSReceivingException</span></span> | <span data-ttu-id="36802-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="36802-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="36802-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="36802-358">WHSWorkException</span></span> | <span data-ttu-id="36802-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="36802-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="36802-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="36802-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="36802-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="36802-362">WMSLocationId</span></span> | <span data-ttu-id="36802-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="36802-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="36802-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="36802-364">WorkId</span></span> | <span data-ttu-id="36802-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="36802-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="36802-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="36802-366">WorkIdToCancel</span></span> | <span data-ttu-id="36802-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="36802-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="36802-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="36802-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="36802-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="36802-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="36802-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="36802-370">WorkPoolId</span></span> | <span data-ttu-id="36802-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="36802-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="36802-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="36802-372">ZoneId</span></span> | <span data-ttu-id="36802-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="36802-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="36802-374">使用可能なステップ アイコン</span><span class="sxs-lookup"><span data-stu-id="36802-374">Available step icons</span></span>

<span data-ttu-id="36802-375">システムには、カスタム ステップにも使用できる標準ステップ アイコンのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="36802-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="36802-376">現在、カスタム ステップ アイコンはアップロードできません。</span><span class="sxs-lookup"><span data-stu-id="36802-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="36802-377">したがって、常に標準ステップ アイコンのいずれかを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36802-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="36802-378">次の表に、現在使用可能なすべての標準ステップ アイコンとその名前を示します。</span><span class="sxs-lookup"><span data-stu-id="36802-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="ステップ アイコンについて"><br><span data-ttu-id="36802-380">情報</span><span class="sxs-lookup"><span data-stu-id="36802-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="ライセンス プレートまたは品目ステップ アイコンの追加"><br><span data-ttu-id="36802-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="36802-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="バッチ廃棄ステップ アイコン"><br><span data-ttu-id="36802-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36802-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="通信事業者ステップ アイコン"><br><span data-ttu-id="36802-386">配送業者</span><span class="sxs-lookup"><span data-stu-id="36802-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="CW タグ ステップ アイコン"><br><span data-ttu-id="36802-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="36802-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="CW タグの重量ステップ アイコン"><br><span data-ttu-id="36802-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="36802-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="チェック ディジット ステップ アイコン"><br><span data-ttu-id="36802-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="36802-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="チェックインまたはアウト ID ステップ アイコン"><br><span data-ttu-id="36802-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="36802-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="子ライセンス プレート ステップ アイコン"><br><span data-ttu-id="36802-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="36802-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="クラスター ID ステップ アイコン"><br><span data-ttu-id="36802-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="36802-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="クラスター位置ステップ アイコン"><br><span data-ttu-id="36802-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="36802-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="コンフィギュレーション ID ステップ アイコン"><br><span data-ttu-id="36802-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="36802-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="構成済フィールド ステップ アイコン"><br><span data-ttu-id="36802-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="36802-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con または LP ステップ アイコン"><br><span data-ttu-id="36802-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="36802-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="ライセンス プレート ID から連結ステップ アイコン"><br><span data-ttu-id="36802-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="36802-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="ライセンス プレート ID に連結ステップ アイコン"><br><span data-ttu-id="36802-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="36802-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="コンテナー タイプ ステップ アイコン"><br><span data-ttu-id="36802-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="36802-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="棚卸ステップ アイコン"><br><span data-ttu-id="36802-414">棚卸</span><span class="sxs-lookup"><span data-stu-id="36802-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="棚卸理由コード ステップ アイコン"><br><span data-ttu-id="36802-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="36802-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="原産国コード ステップ アイコン"><br><span data-ttu-id="36802-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="36802-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="廃棄ステップ アイコン"><br><span data-ttu-id="36802-420">Disposition</span><span class="sxs-lookup"><span data-stu-id="36802-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="完了ステップ アイコン"><br><span data-ttu-id="36802-422">完了</span><span class="sxs-lookup"><span data-stu-id="36802-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="配送担当者のチェックイン確認ステップ アイコン"><br><span data-ttu-id="36802-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="配送担当者のチェックイン ID ステップ アイコン"><br><span data-ttu-id="36802-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="36802-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="配送担当者のチェックアウト ID ステップ アイコン"><br><span data-ttu-id="36802-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="36802-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="有効期限ステップ アイコン"><br><span data-ttu-id="36802-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="36802-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="フィールド ステップ アイコン"><br><span data-ttu-id="36802-432">フィールド</span><span class="sxs-lookup"><span data-stu-id="36802-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="バッチ廃棄からステップ アイコン"><br><span data-ttu-id="36802-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="36802-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="在庫状態からステップ アイコン"><br><span data-ttu-id="36802-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="36802-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ID 属性ステップ アイコン"><br><span data-ttu-id="36802-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="36802-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="在庫バッチ ID ステップ アイコン"><br><span data-ttu-id="36802-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="36802-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="在庫の色 ID ステップ アイコン"><br><span data-ttu-id="36802-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="36802-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="在庫場所ステップ アイコン"><br><span data-ttu-id="36802-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="36802-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="在庫のシリアル ID ステップ アイコン"><br><span data-ttu-id="36802-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="36802-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="在庫のサイズ ID ステップ アイコン"><br><span data-ttu-id="36802-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="36802-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="在庫の状態 ID ステップ アイコン"><br><span data-ttu-id="36802-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="36802-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="在庫のスタイル ID ステップ アイコン"><br><span data-ttu-id="36802-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="36802-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="在庫のバージョン ID ステップ アイコン"><br><span data-ttu-id="36802-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="36802-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="品目 ID ステップ アイコン"><br><span data-ttu-id="36802-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="36802-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM コンテナー ID ステップ アイコン"><br><span data-ttu-id="36802-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="36802-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM 出荷 ID ステップ アイコン"><br><span data-ttu-id="36802-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="36802-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="かんばんカード ID ステップ アイコン"><br><span data-ttu-id="36802-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="36802-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="かんばんまたはカード ID ステップ アイコン"><br><span data-ttu-id="36802-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="36802-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="ライセンス プレート ID ステップ アイコン"><br><span data-ttu-id="36802-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="36802-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="貨物 ID ステップ アイコン"><br><span data-ttu-id="36802-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="36802-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="場所ライセンス プレートの位置ステップ アイコン"><br><span data-ttu-id="36802-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="36802-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="場所またはライセンス プレート ステップ アイコン"><br><span data-ttu-id="36802-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="36802-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="場所またはライセンス プレート チェック ステップ アイコン"><br><span data-ttu-id="36802-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="36802-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="場所またはライセンス プレート元ステップ アイコン"><br><span data-ttu-id="36802-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="36802-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="場所またはライセンス プレート先ステップ アイコン"><br><span data-ttu-id="36802-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="36802-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="ロング プロセス完了ステップ アイコン"><br><span data-ttu-id="36802-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="36802-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP ブレーク 親 LP ステップ アイコン"><br><span data-ttu-id="36802-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="36802-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="結合コンテナー ID ステップ アイコン"><br><span data-ttu-id="36802-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="36802-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="混合ライセンス プレートの行番号ステップ アイコン"><br><span data-ttu-id="36802-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="出庫重量ステップ アイコン"><br><span data-ttu-id="36802-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="36802-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="所有者ステップ アイコン"><br><span data-ttu-id="36802-490">所有者</span><span class="sxs-lookup"><span data-stu-id="36802-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="親ライセンス プレート ステップ アイコン"><br><span data-ttu-id="36802-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="36802-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="確認ステップ アイコン"><br><span data-ttu-id="36802-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="36802-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="発注書行番号ステップ アイコン"><br><span data-ttu-id="36802-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="発注書番号ステップ アイコン"><br><span data-ttu-id="36802-498">発注書番号</span><span class="sxs-lookup"><span data-stu-id="36802-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="満杯のポジション ステップ アイコン"><br><span data-ttu-id="36802-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="36802-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="ポテンシー ステップ アイコン"><br><span data-ttu-id="36802-502">ポテンシー</span><span class="sxs-lookup"><span data-stu-id="36802-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="プリンター名ステップ アイコン"><br><span data-ttu-id="36802-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="36802-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="製品 ID ステップ アイコン"><br><span data-ttu-id="36802-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="36802-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="製品の確認ステップ アイコン"><br><span data-ttu-id="36802-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="プット ステップ アイコン"><br><span data-ttu-id="36802-510">プット</span><span class="sxs-lookup"><span data-stu-id="36802-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="プットアウェイ クラスター ID ステップ アイコン"><br><span data-ttu-id="36802-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="36802-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="数量ステップ アイコン"><br><span data-ttu-id="36802-514">数量</span><span class="sxs-lookup"><span data-stu-id="36802-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="数量調整ステップ アイコン"><br><span data-ttu-id="36802-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="36802-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="数量不足ステップ アイコン"><br><span data-ttu-id="36802-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="36802-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="消費数量ステップ アイコン"><br><span data-ttu-id="36802-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="36802-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="プット数量ステップ アイコン"><br><span data-ttu-id="36802-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="36802-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="廃棄数量ステップ アイコン"><br><span data-ttu-id="36802-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="36802-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="数量確定ステップ アイコン"><br><span data-ttu-id="36802-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="36802-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="完了ジョブとしてレポート ステップ アイコン"><br><span data-ttu-id="36802-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="36802-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="受取場所 ID ステップ アイコン"><br><span data-ttu-id="36802-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="36802-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="削除コンテナー ID ステップ アイコン"><br><span data-ttu-id="36802-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="36802-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA 番号ステップ アイコン"><br><span data-ttu-id="36802-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="36802-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="順序選択ステップ アイコン"><br><span data-ttu-id="36802-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="36802-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="ショート・ピックの理由ステップ アイコン"><br><span data-ttu-id="36802-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="36802-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="並べ替え位置 ID ステップ アイコン"><br><span data-ttu-id="36802-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="36802-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="ターゲット ライセンス プレート ID ステップ アイコン"><br><span data-ttu-id="36802-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="行番号へステップ アイコン"><br><span data-ttu-id="36802-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="36802-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="移動先ステップ アイコン"><br><span data-ttu-id="36802-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="36802-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="番号へステップ アイコン"><br><span data-ttu-id="36802-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="36802-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="移動先倉庫ステップ アイコン"><br><span data-ttu-id="36802-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="36802-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="輸送貨物 ID ステップ アイコン"><br><span data-ttu-id="36802-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="36802-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="仕入先バッチ ID ステップ アイコン"><br><span data-ttu-id="36802-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="36802-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="ウェーブ ラベル ID ステップ アイコン"><br><span data-ttu-id="36802-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="36802-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="ウェーブ ラベル数量ステップ アイコン"><br><span data-ttu-id="36802-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="36802-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="重量ステップ アイコン"><br><span data-ttu-id="36802-560">太さ</span><span class="sxs-lookup"><span data-stu-id="36802-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="消費重量ステップ アイコン"><br><span data-ttu-id="36802-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="36802-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS 調整タイプ ステップ アイコン"><br><span data-ttu-id="36802-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="36802-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS 受領例外ステップ アイコン"><br><span data-ttu-id="36802-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="36802-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS 場所 ID ステップ アイコン"><br><span data-ttu-id="36802-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="36802-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="作業 ID ステップ アイコン"><br><span data-ttu-id="36802-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="36802-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="キャンセルする作業 ID ステップ アイコン"><br><span data-ttu-id="36802-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="36802-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="作業ライセンス プレート ID ステップ アイコン"><br><span data-ttu-id="36802-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="36802-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="作業ライセンス プレート ID プットアウェイ クラスター ステップ アイコン"><br><span data-ttu-id="36802-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="36802-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="作業プール ID ステップ アイコン"><br><span data-ttu-id="36802-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="36802-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="ゾーン ID ステップ アイコン"><br><span data-ttu-id="36802-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="36802-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="36802-581">例: カスタム フローへのステップ アイコンとタイトルの割り当て</span><span class="sxs-lookup"><span data-stu-id="36802-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="36802-582">この例では、カスタム タスク フローのステップ アイコンとタイトルの設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="36802-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="36802-583">このシナリオは、次のブログ記事: [倉庫モバイル アプリのカスタマイズ](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app) で詳細に説明および検討するカスタム タスク フローの例に基づいて作成されています。</span><span class="sxs-lookup"><span data-stu-id="36802-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="36802-584">タスク フローは次のように機能します:</span><span class="sxs-lookup"><span data-stu-id="36802-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="36802-585">アプリは、作業者にコンテナー ID の入力を求めるページを表示します (例えば、バーコードをスキャンするなど)。</span><span class="sxs-lookup"><span data-stu-id="36802-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="36802-586">コンテナー ID が有効な場合、アプリは新しいページを開き、作業者に重量の入力を求めます。</span><span class="sxs-lookup"><span data-stu-id="36802-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="36802-587">(コンテナー ID が無効な場合、作業者は最初のページに戻ります。)</span><span class="sxs-lookup"><span data-stu-id="36802-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="36802-588">作業者が有効な重量を入力すると、システムは重量を格納し、作業者を最初のページに戻します。</span><span class="sxs-lookup"><span data-stu-id="36802-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="36802-589">次の図は、このタスク フローを示します。</span><span class="sxs-lookup"><span data-stu-id="36802-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="36802-590">![タスク フロー図](media/step-icons-example-task-flow.png "タスク フロー図")</span><span class="sxs-lookup"><span data-stu-id="36802-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="36802-591">コンテナー入力ページ用のステップ クラスの作成</span><span class="sxs-lookup"><span data-stu-id="36802-591">Create a step class for the container input page</span></span>

<span data-ttu-id="36802-592">コンテナー入力ページでは、作業者がコンテナー ID をスキャンまたは入力できます。</span><span class="sxs-lookup"><span data-stu-id="36802-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="36802-593">![コンテナー入力ページ](media/step-icons-example-container-input.png "コンテナー入力ページ")</span><span class="sxs-lookup"><span data-stu-id="36802-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="36802-594">コンテナー入力ページでは、入力フィールドのコントロール名は `ContainerId` です。</span><span class="sxs-lookup"><span data-stu-id="36802-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="36802-595">このコントロール名は [ステップ ID の一覧](#step-ids-classes) にないため、このコントロール名に基づく既存のステップは見つかりません。</span><span class="sxs-lookup"><span data-stu-id="36802-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="36802-596">したがって、ステップを表すステップ クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36802-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="36802-597">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="36802-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="36802-598">ステップ アイコンの識別子は `defaultStepIcon` クラス メンバーに保存され、ステップ タイトルは `defaultStepTitle` クラス メンバーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="36802-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="36802-599">ステップ アイコンを割り当てるには、`defaultStepIcon` をこのトピックで前述した [使用可能なステップ アイコン](#step-icons) セクションに一覧表示されているアイコン ID の 1 つに設定します。</span><span class="sxs-lookup"><span data-stu-id="36802-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="36802-600">重量入力に標準またはカスタムのステップ アイコンとタイトルを使用する</span><span class="sxs-lookup"><span data-stu-id="36802-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="36802-601">重量入力ページでは、作業者が重量を入力できます。</span><span class="sxs-lookup"><span data-stu-id="36802-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="36802-602">![重量入力ページ](media/step-icons-example-weight-input.png "重量入力ページ")</span><span class="sxs-lookup"><span data-stu-id="36802-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="36802-603">重量入力ページでは、入力フィールドのコントロール名は [ステップ ID の一覧](#step-ids-classes) にある `Weight` です。</span><span class="sxs-lookup"><span data-stu-id="36802-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="36802-604">したがって、`WHSMobileAppStepWeight` クラスで定義されているステップ アイコンとタイトルが適切であれば、このステップで何も変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="36802-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="36802-605">ただし、このステップで別のアイコンまたはタイトルを使用する場合は、ビルダー クラスで `stepId()` メソッドまたは `stepInfo()` メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="36802-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="36802-606">各タスク フローには、独自のステップ情報ビルダーがあります。</span><span class="sxs-lookup"><span data-stu-id="36802-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="36802-607">stepId() メソッドの上書き</span><span class="sxs-lookup"><span data-stu-id="36802-607">Override the stepId() method</span></span>

<span data-ttu-id="36802-608">次の例は、`stepId()` メソッドを上書きしてビルダー クラスを変更する方法の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="36802-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="36802-609">次に、`NewWeight` ステップのステップ クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="36802-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="36802-610">コードは、このトピックの前半で示した `ContainerId` の例のコードと似ている必要があります。</span><span class="sxs-lookup"><span data-stu-id="36802-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="36802-611">stepInfo() メソッドの上書き</span><span class="sxs-lookup"><span data-stu-id="36802-611">Override the stepInfo() method</span></span>

<span data-ttu-id="36802-612">次の例は、`stepInfo()` メソッドを上書きしてビルダー クラスを変更する方法の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="36802-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="36802-613">次に、`WHSMobileAppStepInfo` オブジェクトを作成し、アイコンやタイトルを直接設定します。</span><span class="sxs-lookup"><span data-stu-id="36802-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36802-614">追加リソース</span><span class="sxs-lookup"><span data-stu-id="36802-614">Additional resources</span></span>

- [<span data-ttu-id="36802-615">倉庫管理モバイル アプリのインストールと接続</span><span class="sxs-lookup"><span data-stu-id="36802-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="36802-616">モバイル デバイスのユーザー設定</span><span class="sxs-lookup"><span data-stu-id="36802-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
