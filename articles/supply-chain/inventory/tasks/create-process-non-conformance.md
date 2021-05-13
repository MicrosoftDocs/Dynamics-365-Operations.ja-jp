---
title: 不適合の作成および処理
description: このトピックでは、既存の品質指示に基づき不適合管理を実行する方法について説明します。
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956209"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="0981b-103">不適合の作成および処理</span><span class="sxs-lookup"><span data-stu-id="0981b-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0981b-104">このトピックでは、既存の品質指示に基づき不適合管理を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0981b-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="0981b-105">通常、不適合管理は品質担当者が実施します。</span><span class="sxs-lookup"><span data-stu-id="0981b-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="0981b-106">前提条件として、使用可能な品質指示が必要です。</span><span class="sxs-lookup"><span data-stu-id="0981b-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="0981b-107">(品質指示の作成方法については、[商品の品質の調査](inspect-quality-goods.md) を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="0981b-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="0981b-108">ユーザーが不適合の承認を処理するには、**ユーザー** ページの **個人** フィールドで、不適合に対する作業者を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0981b-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="0981b-109">また、ユーザーがドキュメントのメモを使用するには、ユーザー オプションで **ドキュメント処理の有効化** オプションを *はい* に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0981b-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="0981b-110">不適合の作成</span><span class="sxs-lookup"><span data-stu-id="0981b-110">Create a nonconformance</span></span>

<span data-ttu-id="0981b-111">不適合を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="0981b-112">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-113">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="0981b-114">**問題タイプ** フィールドの **不適合の作成** ダイアログ ボックスで、検査プロセス中に検出された問題を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="0981b-115">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="0981b-116">不適合の承認または否認</span><span class="sxs-lookup"><span data-stu-id="0981b-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="0981b-117">不適合を承認または否認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="0981b-118">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-119">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-120">承認されている不適合に対してのみ修正を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="0981b-121">アクション ペインで、不適合を承認する場合は **機能\>不適合の承認** を、不適合を否認する場合は **機能\>不適合の否認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="0981b-122">承認済の不適合を[関連する工程](../quality-operations.md) に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0981b-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="0981b-123">これにより、不適合処理や修正処理の一部として、処理される作業を記録することができます。</span><span class="sxs-lookup"><span data-stu-id="0981b-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="0981b-124">選択を確定するように求められます。</span><span class="sxs-lookup"><span data-stu-id="0981b-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="0981b-125">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="0981b-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="0981b-126">不適合への操作や詳細の追加</span><span class="sxs-lookup"><span data-stu-id="0981b-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="0981b-127">不適合を作成したら、関連する工程を追加し、それらの工程に関する追加情報を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="0981b-128">承認されている不適合に対してのみ関連する工程を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="0981b-129">基本的な情報に加え、次の詳細情報を操作に追加できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="0981b-130">**品目** – 修正の実行に消費される品目の一覧を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="0981b-131">たとえば、設備の修理に必要な製品や、完成品の再作業に必要な材料などが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="0981b-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="0981b-132">**品質諸費用** – 発生した費用または外部ソースに請求した金額の一覧を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="0981b-133">**タイムシート** – 各作業者が工程に費やした時間のログを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="0981b-134">残りの設定はオプションです。</span><span class="sxs-lookup"><span data-stu-id="0981b-134">The remaining settings are optional.</span></span> <span data-ttu-id="0981b-135">各品目の原価、品質諸費用、およびタイムシートが合計され、工程に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="0981b-136">工程の **原価** フィールドを直接編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="0981b-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="0981b-137">不適合の工程の作成</span><span class="sxs-lookup"><span data-stu-id="0981b-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="0981b-138">不適合の工程を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="0981b-139">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-140">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-141">承認されている不適合に対してのみ関連する工程を追加または更新できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="0981b-142">アクション ペインで、**関連する工程** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="0981b-143">アクション ペインの **関連する工程** ページで **新規** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0981b-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0981b-144">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="0981b-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="0981b-145">**工程** – 不適合に対して実行される工程のコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="0981b-146">**理由** – 工程が必要な理由を説明する詳細な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="0981b-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="0981b-147">**販売注文** – 選択した工程コードが販売注文タイプに関連する場合、工程にリンクする販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="0981b-148">**発注書** – 選択した工程コードが発注書タイプに関連する場合、工程にリンクする発注書を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="0981b-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="0981b-150">工程への品目の追加</span><span class="sxs-lookup"><span data-stu-id="0981b-150">Add items to an operation</span></span>

<span data-ttu-id="0981b-151">工程に品目を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="0981b-152">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-153">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-154">承認されている不適合に対してのみ関連する工程を追加または更新できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="0981b-155">アクション ペインで、**関連する工程** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="0981b-156">**関連する工程** ページで、品目を追加する工程を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="0981b-157">アクション ペインで、**品目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="0981b-158">アクション ペインの **関連する工程** ページで **新規** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0981b-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0981b-159">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="0981b-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="0981b-160">**品目番号** – 選択した工程の一部として消費される製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="0981b-161">**数量** – 消費される品目の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="0981b-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-162">品目の原価は、**全般** タブの **原価** フィールドに表示されます。この原価は、**リリースされた製品** ページで設定された費用を元に計算されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="0981b-163">原価は、**関連する工程の品目** ページで直接更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="0981b-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="0981b-164">**関連する工程の品目** ページで追加されたすべての品目の原価は、**関連する工程** ページの **原価** フィールドに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="0981b-165">追加する品目ごとに前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="0981b-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="0981b-166">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="0981b-167">工程への品質諸費用の追加</span><span class="sxs-lookup"><span data-stu-id="0981b-167">Add quality charges to an operation</span></span>

<span data-ttu-id="0981b-168">工程に品質諸費用を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="0981b-169">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-170">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-171">承認されている不適合に対してのみ関連する工程を追加または更新できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="0981b-172">アクション ペインで、**関連する工程** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="0981b-173">**関連する工程** ページで、品質諸費用を追加する工程を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="0981b-174">アクション ペインで、**品質諸費用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="0981b-175">アクション ペインの **関連する工程の費用** ページで **新規** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0981b-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0981b-176">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="0981b-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="0981b-177">**諸費用コード** – 追加する品質諸費用を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="0981b-178">**説明** – 費用の詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="0981b-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="0981b-179">**諸費用金額** – 費用の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="0981b-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="0981b-180">追加する費用ごとに前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="0981b-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="0981b-181">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="0981b-182">**諸費用金額** フィールドの金額は、すべての品質諸費用に対して自動的に合計され、**関連する工程** ページの **原価** フィールドで他の金額に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="0981b-183">工程のタイムシートの作成</span><span class="sxs-lookup"><span data-stu-id="0981b-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="0981b-184">工程にタイムシートを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="0981b-185">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-186">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-187">承認されている不適合に対してのみ関連する工程を追加または更新できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="0981b-188">アクション ペインで、**関連する工程** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="0981b-189">**関連する工程** ページで、タイムシートを追加する工程を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="0981b-190">アクション ペインで、**タイムシート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="0981b-191">アクション ペインの **関連する工程のタイムシート** ページで **新規** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0981b-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0981b-192">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="0981b-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="0981b-193">**日付** – 作業が行われた日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="0981b-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="0981b-194">既定では、このフィールドが現在の日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="0981b-195">**作業者** – 作業を行った作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="0981b-196">既定では、このフィールドは現在のユーザーに割り当てられている作業者に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="0981b-197">**工程時間** – 選択した工程の作業時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="0981b-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="0981b-198">**請求済** – 請求書で顧客または仕入先に時間が請求されている場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="0981b-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-199">原価は、**全般** タブの **原価** フィールドに表示されます。原価は、**在庫管理パラメーター** ページで定義したレートを使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="0981b-200">追加するタイムシート行ごとに前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="0981b-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="0981b-201">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="0981b-202">**原価** フィールドの金額は、すべてのタイムシート行に対して自動的に合計され、**関連する工程** ページの **原価** フィールドで他の金額に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0981b-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="0981b-203">不適合への修正の追加</span><span class="sxs-lookup"><span data-stu-id="0981b-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="0981b-204">不適合に修正を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="0981b-205">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-206">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-207">承認されている不適合に対してのみ修正を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="0981b-208">アクション ペインで、**修正** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="0981b-209">アクション ペインの **修正** ページで、**新規** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0981b-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0981b-210">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="0981b-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="0981b-211">**診断** – 作成する修正のタイプを識別する診断タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="0981b-212">**作業者** – 修正を担当する個人を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="0981b-213">**修正の優先順位** – 修正に優先順位付けする方法を示すオプションを選択します (*低*、*標準*、または *高*)。</span><span class="sxs-lookup"><span data-stu-id="0981b-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="0981b-214">**要求日** – 修正アクションが要求された日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0981b-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="0981b-215">**予定日** – 修正の完了予定日を入力します。</span><span class="sxs-lookup"><span data-stu-id="0981b-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="0981b-216">**短期間ソリューション** – 修正アクションによって不適合が短期間のみ修正される場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="0981b-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="0981b-217">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="0981b-218">修正を完了としてマーク</span><span class="sxs-lookup"><span data-stu-id="0981b-218">Mark a correction as completed</span></span>

<span data-ttu-id="0981b-219">不適合の修正を完了としてマークするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="0981b-220">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-221">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0981b-222">承認されている不適合に対してのみ修正を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0981b-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="0981b-223">アクション ペインで、**修正** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="0981b-224">**修正** ページのグリッドで、完了としてマークする修正を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="0981b-225">アクション ペインで、**完了としてマーク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="0981b-226">選択を確定するように求められます。</span><span class="sxs-lookup"><span data-stu-id="0981b-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="0981b-227">続行するには **OK** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="0981b-227">Select **OK** to continue.</span></span> <span data-ttu-id="0981b-228">**完了日時** フィールドが現在の日時に設定され、**完了** チェック ボックスがオンになります。</span><span class="sxs-lookup"><span data-stu-id="0981b-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="0981b-229">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="0981b-230">完了した修正の再オープン</span><span class="sxs-lookup"><span data-stu-id="0981b-230">Reopen a completed correction</span></span>

<span data-ttu-id="0981b-231">完了した修正を再オープンするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="0981b-232">**在庫管理\>定期処理のタスク\>品質管理\>不適合** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0981b-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-233">一覧で、更新する不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="0981b-234">アクション ペインで、**修正** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="0981b-235">**修正** ページのグリッドで、再オープンする修正を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="0981b-236">アクション ペインで、**再オープン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="0981b-237">選択を確定するように求められます。</span><span class="sxs-lookup"><span data-stu-id="0981b-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="0981b-238">続行するには **OK** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="0981b-238">Select **OK** to continue.</span></span> <span data-ttu-id="0981b-239">**完了日時** フィールドの値がクリアされ、**完了** チェック ボックスはオフになります。</span><span class="sxs-lookup"><span data-stu-id="0981b-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="0981b-240">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-240">Close the page.</span></span>

<span data-ttu-id="0981b-241">これで、修正に対して追加の編集または更新ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="0981b-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="0981b-242">完了したら、修正を再度完了としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="0981b-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="0981b-243">不適合のクローズ</span><span class="sxs-lookup"><span data-stu-id="0981b-243">Close a nonconformance</span></span>

<span data-ttu-id="0981b-244">不適合をクローズするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0981b-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="0981b-245">**在庫管理 \> 定期処理タスク \> 品質管理 \> 品質指示** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0981b-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="0981b-246">グリッドで品質指示を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="0981b-247">アクション ペインで、**照会\>不適合** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="0981b-248">**不適合** ページで、グリッド内のターゲット不適合を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="0981b-249">アクション ペインで、**機能\>不適合のクローズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0981b-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="0981b-250">選択を確定するように求められます。</span><span class="sxs-lookup"><span data-stu-id="0981b-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="0981b-251">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="0981b-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="0981b-252">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0981b-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0981b-253">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0981b-253">Additional resources</span></span>

- [<span data-ttu-id="0981b-254">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="0981b-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="0981b-255">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="0981b-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="0981b-256">不適合の承認を担当する作業者</span><span class="sxs-lookup"><span data-stu-id="0981b-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="0981b-257">不適合の検査ゾーン</span><span class="sxs-lookup"><span data-stu-id="0981b-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="0981b-258">不適合の診断タイプ</span><span class="sxs-lookup"><span data-stu-id="0981b-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="0981b-259">不適合の品質諸費用</span><span class="sxs-lookup"><span data-stu-id="0981b-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="0981b-260">不適合の工程</span><span class="sxs-lookup"><span data-stu-id="0981b-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="0981b-261">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="0981b-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
