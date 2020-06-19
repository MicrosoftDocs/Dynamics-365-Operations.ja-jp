---
title: ジョブ カード デバイスから完了として報告する
description: このトピックでは、ジョブ カード デバイスのユーザーが製造オーダーから在庫に対して完成品を報告できるようにシステムを構成する方法について説明します。
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403265"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="9f0c3-103">ジョブ カード デバイスから完了として報告する</span><span class="sxs-lookup"><span data-stu-id="9f0c3-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f0c3-104">作業者は、ジョブ カード デバイス上の **レポートの進捗情報** ページを使って、生産ジョブで完了した数量を報告します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="9f0c3-105">完了報告された数量を在庫に追加するかどうかを制御する</span><span class="sxs-lookup"><span data-stu-id="9f0c3-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="9f0c3-106">最後の工程で完了と報告された数量を在庫に追加するかどうか、および報告する方法を制御するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="9f0c3-107">**生産管理 \> 設定 \> 製造実行 \> 生産パラメータ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="9f0c3-108">**完了レポート** タブで、**完了レポートをオンラインで更新する** フィールドに次のいずれかの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="9f0c3-109">**なし** - 最後の工程で数量が報告されたときに、在庫に数量が加算されません。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="9f0c3-110">生産の状態は一切変更されません。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="9f0c3-111">**ステータス + 数量** - 製造オーダーのステータスが *完了報告済* に変更され、数量が完了として在庫になるように報告されます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="9f0c3-112">**数量** – 数量が完了として在庫になるように報告されますが、製造オーダーのステータスは変更しません。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="9f0c3-113">**ステータス** – 生産の状態のみが変更されます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="9f0c3-114">最後の工程で数量が報告されたときに、在庫に数量が加算されません。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="9f0c3-115">完了済として報告された工程が最後の工程として定義されていないと、在庫の数量が追跡されません。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="9f0c3-116">ただし、これらの数量は、進行状況を表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="9f0c3-117">また、前の工程で報告された数量の定義済のしきい値に達する前に、作業者が次の工程を開始できるかどうかを制御するルールに含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="9f0c3-118">これらのルールは、**製造オーダーの既定値** ページの **数量の検証** タブで定義できます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="9f0c3-119">**製造オーダーの既定値** ページの使用方法の詳細については、[製造実行の生産パラメータ](production-parameters-manufacturing-execution.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="9f0c3-120">バッチ管理された品目を完了として報告する</span><span class="sxs-lookup"><span data-stu-id="9f0c3-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="9f0c3-121">ジョブ カード デバイスは、バッチ品目に関するレポートのための 3 つのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="9f0c3-122">これらのシナリオは、高度な倉庫プロセスで有効になっている品目と、高度な倉庫プロセスで有効になっていない品目の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="9f0c3-123">**手動で割り当て済みのバッチ番号:** 作業者はカスタムのバッチ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="9f0c3-124">このバッチ番号は、システムに認識されていない外部ソースから取得された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="9f0c3-125">**定義済バッチ番号:** 作業者は、製造オーダーがジョブ カード デバイスにリリースされる前に、システムによって自動的に生成されるバッチ番号の一覧から、バッチ番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="9f0c3-126">**固定バッチ番号:** 作業者はバッチ番号の入力や選択をしません。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="9f0c3-127">その代わりに、システムは製造オーダーにバッチ番号を自動的に割り当ててからリリースされます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="9f0c3-128">各シナリオを有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="9f0c3-129">**製品管理情報 \> 製品 \> リリースされた製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9f0c3-130">構成する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-130">Select the product to configure.</span></span>
1. <span data-ttu-id="9f0c3-131">**在庫の管理** クイックタブの **バッチ番号グループ** フィールドで、シナリオをサポートするように設定されている追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="9f0c3-132">バッチ管理された製品にバッチ番号グループが割り当てられていない場合、既定では、完了報告時にジョブ カード デバイスによってバッチ番号の手動のエントリが提供されます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="9f0c3-133">次のサブセクションでは、バッチ品目に関するレポートの 3 つのシナリオをサポートするために、番号グループの追跡を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="9f0c3-134">ジョブ カード デバイスのバッチ番号の報告を有効にする</span><span class="sxs-lookup"><span data-stu-id="9f0c3-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="9f0c3-135">完了報告時にジョブ カード デバイスがバッチ番号を受け取ることができるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して、次の機能を (この順序で) 有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="9f0c3-136">ジョブ カード デバイスの進捗状況のレポート ダイアログのユーザー エクスペリエンスの向上</span><span class="sxs-lookup"><span data-stu-id="9f0c3-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="9f0c3-137">ジョブ カード デバイス (プレビュー) からの完了報告時に、バッチ番号とシリアル番号を入力できるようにする</span><span class="sxs-lookup"><span data-stu-id="9f0c3-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="9f0c3-138">バッチ番号を手動で割り当てることができるように、追跡番号グループを設定する</span><span class="sxs-lookup"><span data-stu-id="9f0c3-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="9f0c3-139">バッチ番号を手動で割り当てられるようにするには、これらの手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="9f0c3-140">**在庫管理 \> 設定 \> 分析コード \> 番号グループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="9f0c3-141">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="9f0c3-142">**一般** クイックタブで、**手動** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="9f0c3-143">![追跡番号グループ ページ](media/tracking-number-group-manual.png "追跡番号グループ ページ")</span><span class="sxs-lookup"><span data-stu-id="9f0c3-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="9f0c3-144">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のバッチ番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="9f0c3-145">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **バッチ番号** フィールド は、作業者が任意の値を入力できるテキスト ボックスです。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="9f0c3-146">![手動バッチ番号を含むレポートの進行状況ページ](media/job-card-device-batch-manual.png "手動バッチ番号のフィールドを含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="9f0c3-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="9f0c3-147">事前に定義されたバッチ番号の一覧を提供する追跡番号グループの設定</span><span class="sxs-lookup"><span data-stu-id="9f0c3-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="9f0c3-148">事前に定義されたバッチ番号のリストを提供するには、これらの手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="9f0c3-149">**在庫管理 \> 設定 > 分析コード \> 番号麩ループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="9f0c3-150">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="9f0c3-151">**一般** クイックタブで、**在庫取引のみ** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="9f0c3-152">**数量ごと** フィールドを使って、入力した値に基づいて、数量ごとにバッチ番号を分割します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="9f0c3-153">たとえば、10 個の製造オーダーがあり、**数量ごと** フィールドが *2* に設定されているとします。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="9f0c3-154">この場合、製造オーダーを作成すると、5 つのバッチ番号が製造オーダーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="9f0c3-155">![追跡番号グループ ページ](media/tracking-number-group-predefined.png "追跡番号グループ ページ")</span><span class="sxs-lookup"><span data-stu-id="9f0c3-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="9f0c3-156">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のバッチ番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="9f0c3-157">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **バッチ番号** フィールド は、作業者が任意の値を入力できるドロップダウン リストです。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="9f0c3-158">![事前に定義されたバッチ番号を含むレポートの進行状況ページ](media/job-card-device-batch-predefined.png "事前に定義されたバッチ番号のリストを含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="9f0c3-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="9f0c3-159">バッチ番号を自動的にで割り当てることができるように、追跡番号グループを設定する</span><span class="sxs-lookup"><span data-stu-id="9f0c3-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="9f0c3-160">バッチ番号が自動的に割り当てられるようにするには、次の手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="9f0c3-161">**在庫管理 \> 設定 \> 分析コード \> 番号グループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="9f0c3-162">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="9f0c3-163">**一般** クイックタブで、**在庫取引のみ** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="9f0c3-164">**手動**オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="9f0c3-165">![追跡番号グループ ページ](media/tracking-number-group-fixed.png "追跡番号グループ ページ")</span><span class="sxs-lookup"><span data-stu-id="9f0c3-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="9f0c3-166">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のバッチ番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="9f0c3-167">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **バッチ番号** フィールド は、値を表示しますが作業者はそれを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="9f0c3-168">![固定バッチ番号を含むレポートの進行状況ページ](media/job-card-device-batch-fixed.png "固定バッチ番号を含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="9f0c3-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="9f0c3-169">ライセンス プレートに完了としてレポートする</span><span class="sxs-lookup"><span data-stu-id="9f0c3-169">Report as finished to a license plate</span></span>

<span data-ttu-id="9f0c3-170">高度な倉庫プロセスでは、ライセンスプレート分析コードを使用して、この目的のために設定された倉庫の場所で在庫を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="9f0c3-171">この場合、作業者が完了報告済数量を報告するときに、ライセンス プレート番号が必要になります。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="9f0c3-172">ライセンス プレート報告とラベル印刷を有効にする</span><span class="sxs-lookup"><span data-stu-id="9f0c3-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="9f0c3-173">このセクションで説明されている機能を使用するには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して、次の機能を (この順序で) 有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="9f0c3-174">完了報告用ライセンス プレートをジョブ カード デバイスに追加</span><span class="sxs-lookup"><span data-stu-id="9f0c3-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="9f0c3-175">ジョブ カード デバイスでの完了報告時に、ライセンス プレート番号の自動生成を有効にする</span><span class="sxs-lookup"><span data-stu-id="9f0c3-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="9f0c3-176">ジョブ カード デバイスからラベルを印刷</span><span class="sxs-lookup"><span data-stu-id="9f0c3-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="9f0c3-177">ライセンス プレートに完了として報告することを設定する</span><span class="sxs-lookup"><span data-stu-id="9f0c3-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="9f0c3-178">既存のライセンスプレートを再利用するか、数量が完了済と報告されたときに新しいライセンスプレートを生成するかを制御するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="9f0c3-179">**生産管理 \> 設定 \> 製造実行 \> デバイスのジョブ カードの構成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="9f0c3-180">各デバイスに対して次のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="9f0c3-181">**ライセンス プレートの生成** - このオプションを **はい** に設定すると、各完了報告に対して新しいライセンス プレートを生成します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="9f0c3-182">完了レポートごとに既存のライセンスプレートを使用する場合は、**いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="9f0c3-183">**印刷ラベル** - 作業員が完了報告ごとにライセンス プレート ラベルを印刷する必要がある場合は、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="9f0c3-184">ラベルを必要としない場合は、**いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="9f0c3-185">![デバイス ページのジョブ カードの構成](media/config-job-card-raf.png "デバイス ページのジョブ カードの構成")</span><span class="sxs-lookup"><span data-stu-id="9f0c3-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="9f0c3-186">ラベルを構成するには、**倉庫管理 \> 設定 \> ドキュメント回覧 \> ドキュメント回覧** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="9f0c3-187">詳細については、[ライセンス プレート ラベル印刷の有効化](../warehousing/tasks/license-plate-label-printing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f0c3-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
