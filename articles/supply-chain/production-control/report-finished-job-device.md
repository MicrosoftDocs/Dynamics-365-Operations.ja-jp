---
title: ジョブ カード デバイスから完了として報告する
description: このトピックでは、ジョブ カード デバイスのユーザーが製造オーダーから在庫に対して完成品を報告できるようにシステムを構成する方法について説明します。
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd21bdf532e1e607e66bb8f5ef032f0855c99612
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811633"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="64970-103">ジョブ カード デバイスから完了として報告する</span><span class="sxs-lookup"><span data-stu-id="64970-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64970-104">作業者は、ジョブ カード デバイス上の **レポートの進捗情報** ページを使って、生産ジョブで完了した数量を報告します。</span><span class="sxs-lookup"><span data-stu-id="64970-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span> <span data-ttu-id="64970-105">このトピックでは、このページを使用して作業者が完了したことを報告する方法と、その次の手順を決定するさまざまなオプションを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64970-105">This topic describes how to set up various options that establish how workers can report as finished using this page and what happens next.</span></span> <span data-ttu-id="64970-106">次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="64970-106">Options include:</span></span>

- <span data-ttu-id="64970-107">完了報告された数量を在庫に追加するかどうかとその方法を制御する。</span><span class="sxs-lookup"><span data-stu-id="64970-107">Control whether and how quantities that are reported as finished are added to inventory.</span></span>
- <span data-ttu-id="64970-108">完了報告時にバッチ番号をどのように生成して適用するかを制御する。</span><span class="sxs-lookup"><span data-stu-id="64970-108">Control whether and how batch numbers are generated and applied when reporting as finished.</span></span>
- <span data-ttu-id="64970-109">完了報告時にシリアル番号をどのように生成して適用するかを制御する。</span><span class="sxs-lookup"><span data-stu-id="64970-109">Control whether and how serial numbers are generated and applied when reporting as finished.</span></span>
- <span data-ttu-id="64970-110">ライセンス プレートに完了報告するかどうかとその方法を制御する。</span><span class="sxs-lookup"><span data-stu-id="64970-110">Control whether and how to report as finished to a license plate.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="64970-111">完了報告された数量を在庫に追加するかどうかを制御する</span><span class="sxs-lookup"><span data-stu-id="64970-111">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="64970-112">最後の工程で完了と報告された数量を在庫に追加するかどうか、および報告する方法を制御するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="64970-112">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="64970-113">**生産管理 \> 設定 \> 製造実行 \> 生産パラメータ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="64970-113">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="64970-114">**完了レポート** タブで、**完了レポートをオンラインで更新する** フィールドに次のいずれかの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-114">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="64970-115">**なし** - 最後の工程で数量が報告されたときに、在庫に数量が加算されません。</span><span class="sxs-lookup"><span data-stu-id="64970-115">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="64970-116">生産の状態は一切変更されません。</span><span class="sxs-lookup"><span data-stu-id="64970-116">The status of the production order will never change.</span></span>
    - <span data-ttu-id="64970-117">**ステータス + 数量** - 製造オーダーのステータスが *完了報告済* に変更され、数量が完了として在庫になるように報告されます。</span><span class="sxs-lookup"><span data-stu-id="64970-117">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="64970-118">**数量** – 数量が完了として在庫になるように報告されますが、製造オーダーのステータスは変更しません。</span><span class="sxs-lookup"><span data-stu-id="64970-118">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="64970-119">**ステータス** – 生産の状態のみが変更されます。</span><span class="sxs-lookup"><span data-stu-id="64970-119">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="64970-120">最後の工程で数量が報告されたときに、在庫に数量が加算されません。</span><span class="sxs-lookup"><span data-stu-id="64970-120">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="64970-121">完了済として報告された工程が最後の工程として定義されていないと、在庫の数量が追跡されません。</span><span class="sxs-lookup"><span data-stu-id="64970-121">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="64970-122">ただし、これらの数量は、進行状況を表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="64970-122">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="64970-123">また、前の工程で報告された数量の定義済のしきい値に達する前に、作業者が次の工程を開始できるかどうかを制御するルールに含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="64970-123">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="64970-124">これらのルールは、**製造オーダーの既定値** ページの **数量の検証** タブで定義できます。</span><span class="sxs-lookup"><span data-stu-id="64970-124">You can define these rules on the **Quantity validation** tab on the **Production order defaults** page.</span></span>

<span data-ttu-id="64970-125">**製造オーダーの既定値** ページの使用方法の詳細については、[製造実行の生産パラメータ](production-parameters-manufacturing-execution.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64970-125">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="64970-126">バッチ管理された品目を完了として報告する</span><span class="sxs-lookup"><span data-stu-id="64970-126">Report batch-controlled items as finished</span></span>

<span data-ttu-id="64970-127">ジョブ カード デバイスは、バッチ品目に関するレポートのための 3 つのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="64970-127">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="64970-128">これらのシナリオは、高度な倉庫プロセスで有効になっている品目と、高度な倉庫プロセスで有効になっていない品目の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="64970-128">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="64970-129">**手動で割り当て済みのバッチ番号** - 作業者はカスタムのバッチ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="64970-129">**Manually assigned batch numbers** - Workers enter a custom batch number.</span></span> <span data-ttu-id="64970-130">このバッチ番号は、システムに認識されていない外部ソースから取得された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="64970-130">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="64970-131">**定義済バッチ番号** - 作業者は、製造オーダーがジョブ カード デバイスにリリースされる前に、システムによって自動的に生成されるバッチ番号の一覧から、バッチ番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-131">**Predefined batch numbers** - Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="64970-132">**固定バッチ番号** - 作業者はバッチ番号の入力や選択をしません。</span><span class="sxs-lookup"><span data-stu-id="64970-132">**Fixed batch numbers** - Workers don't enter or select a batch number.</span></span> <span data-ttu-id="64970-133">その代わりに、システムは製造オーダーにバッチ番号を自動的に割り当ててからリリースされます。</span><span class="sxs-lookup"><span data-stu-id="64970-133">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>


### <a name="enable-the-feature-on-your-system"></a><span data-ttu-id="64970-134">システムで機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="64970-134">Enable the feature on your system</span></span>

<span data-ttu-id="64970-135">完了報告時にジョブ カード デバイスがバッチ番号を受け取ることができるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して、次の機能を (この順序で) 有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64970-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="64970-136">ジョブ カード デバイスの進捗状況のレポート ダイアログのユーザー エクスペリエンスの向上</span><span class="sxs-lookup"><span data-stu-id="64970-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="64970-137">ジョブ カード デバイスからの完了報告時に、バッチ番号とシリアル番号を入力できるようにします。</span><span class="sxs-lookup"><span data-stu-id="64970-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device</span></span>

### <a name="configure-products-that-require-batch-number-reporting"></a><span data-ttu-id="64970-138">バッチ番号の報告を必要とする製品をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="64970-138">Configure products that require batch number reporting</span></span>

<span data-ttu-id="64970-139">利用可能なバッチ管理シナリオをサポートするための製品を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64970-139">To enable a product to support any of the available batch-controlled scenarios, follow these steps:</span></span>

1. <span data-ttu-id="64970-140">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-140">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="64970-141">構成する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-141">Select the product to configure.</span></span>
1. <span data-ttu-id="64970-142">**在庫の管理** クイックタブの **バッチ番号グループ** フィールドで、シナリオをサポートするように設定されている追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-142">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="64970-143">バッチ管理された製品にバッチ番号グループが割り当てられていない場合、既定では、完了報告時にジョブ カード デバイスによってバッチ番号の手動のエントリが提供されます。</span><span class="sxs-lookup"><span data-stu-id="64970-143">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="64970-144">次のセクションでは、バッチ品目に関するレポートの 3 つのシナリオをサポートするために、番号グループの追跡を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64970-144">The following sections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="64970-145">バッチ番号を手動で割り当てることができるように、追跡番号グループを設定する</span><span class="sxs-lookup"><span data-stu-id="64970-145">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="64970-146">バッチ番号を手動で割り当てられるようにするには、これらの手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-146">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="64970-147">**在庫管理 \> 設定 \> 分析コード \> 番号グループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-147">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="64970-148">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-148">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="64970-149">**一般** クイックタブで、**手動** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-149">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="64970-150">![手動バッチ番号の追跡番号グループ](media/tracking-number-group-manual.png "手動バッチ番号の追跡番号グループ")</span><span class="sxs-lookup"><span data-stu-id="64970-150">![A tracking number group for manual batch numbers](media/tracking-number-group-manual.png "A tracking number group for manual batch numbers")</span></span>

1. <span data-ttu-id="64970-151">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のバッチ番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-151">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="64970-152">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **バッチ番号** フィールド は、作業者が任意の値を入力できるテキスト ボックスです。</span><span class="sxs-lookup"><span data-stu-id="64970-152">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="64970-153">![手動バッチ番号を含むレポートの進行状況ページ](media/job-card-device-batch-manual.png "手動バッチ番号のフィールドを含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="64970-153">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="64970-154">事前に定義されたバッチ番号の一覧を提供する追跡番号グループの設定</span><span class="sxs-lookup"><span data-stu-id="64970-154">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="64970-155">事前に定義されたバッチ番号のリストを提供するには、これらの手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-155">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="64970-156">**在庫管理 \> 設定 > 分析コード \> 番号麩ループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-156">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="64970-157">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-157">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="64970-158">**一般** クイックタブで、**在庫取引のみ** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-158">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="64970-159">**数量ごと** フィールドを使って、入力した値に基づいて、数量ごとにバッチ番号を分割します。</span><span class="sxs-lookup"><span data-stu-id="64970-159">Use the **Per qty** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="64970-160">たとえば、10 個の製造オーダーがあり、**数量ごと** フィールドが *2* に設定されているとします。</span><span class="sxs-lookup"><span data-stu-id="64970-160">For example, you have a production order for ten pieces, and the **Per qty** field is set to *2*.</span></span> <span data-ttu-id="64970-161">この場合、製造オーダーを作成すると、5 つのバッチ番号が製造オーダーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="64970-161">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="64970-162">![事前定義バッチ番号の追跡番号グループ](media/tracking-number-group-predefined.png "事前定義バッチ番号の追跡番号グループ")</span><span class="sxs-lookup"><span data-stu-id="64970-162">![A tracking number group for predefined batch numbers](media/tracking-number-group-predefined.png "A tracking number group for predefined batch numbers")</span></span>

1. <span data-ttu-id="64970-163">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のバッチ番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-163">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="64970-164">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **バッチ番号** フィールド は、作業者が任意の値を入力できるドロップダウン リストです。</span><span class="sxs-lookup"><span data-stu-id="64970-164">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="64970-165">![事前に定義されたバッチ番号を含むレポートの進行状況ページ](media/job-card-device-batch-predefined.png "事前に定義されたバッチ番号のリストを含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="64970-165">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="64970-166">バッチ番号を自動的にで割り当てることができるように、追跡番号グループを設定する</span><span class="sxs-lookup"><span data-stu-id="64970-166">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="64970-167">バッチ番号が自動的に割り当てられるようにするには、次の手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-167">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="64970-168">**在庫管理 \> 設定 \> 分析コード \> 番号グループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-168">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="64970-169">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-169">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="64970-170">**一般** クイックタブで、**在庫取引のみ** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-170">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="64970-171">**手動** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-171">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="64970-172">![固定バッチ番号の追跡番号グループ](media/tracking-number-group-fixed.png "固定バッチ番号の追跡番号グループ")</span><span class="sxs-lookup"><span data-stu-id="64970-172">![A tracking number group for fixed batch numbers](media/tracking-number-group-fixed.png "A tracking number group for fixed batch numbers")</span></span>

1. <span data-ttu-id="64970-173">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のバッチ番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-173">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="64970-174">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **バッチ番号** フィールド は、値を表示しますが作業者はそれを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="64970-174">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="64970-175">![固定バッチ番号を含むレポートの進行状況ページ](media/job-card-device-batch-fixed.png "固定バッチ番号を含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="64970-175">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-serial-controlled-items-as-finished"></a><span data-ttu-id="64970-176">シリアル管理された品目を完了として報告する</span><span class="sxs-lookup"><span data-stu-id="64970-176">Report serial-controlled items as finished</span></span>

<span data-ttu-id="64970-177">ジョブ カード デバイスは、シリアル管理された品目に関するレポートのための 3 つのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="64970-177">The job card device supports three scenarios for reporting on serial-controlled items.</span></span> <span data-ttu-id="64970-178">これらのシナリオは、高度な倉庫プロセスで有効になっている品目と、高度な倉庫プロセスで有効になっていない品目の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="64970-178">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="64970-179">**手動で割り当て済みのシリアル番号** - 作業者はカスタムのシリアル番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="64970-179">**Manually assigned serial numbers** - Workers enter a custom serial number.</span></span> <span data-ttu-id="64970-180">このシリアル番号は、システムに認識されていない外部ソースから取得された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="64970-180">This serial number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="64970-181">**定義済シリアル番号** - 作業者は、製造オーダーがジョブ カード デバイスにリリースされる前に、システムによって自動的に生成されるシリアル番号の一覧から、シリアル番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-181">**Predefined serial numbers** - Workers select a serial number in a list of serial numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="64970-182">**固定シリアル番号** - 作業者はシリアル番号の入力や選択をしません。</span><span class="sxs-lookup"><span data-stu-id="64970-182">**Fixed serial number** - Workers don't enter or select a serial number.</span></span> <span data-ttu-id="64970-183">その代わりに、システムは製造オーダーにシリアル番号を自動的に割り当ててからリリースされます。</span><span class="sxs-lookup"><span data-stu-id="64970-183">Instead, the system automatically assigns a serial number to the production order before it's released.</span></span>

### <a name="enable-the-feature-on-your-system"></a><span data-ttu-id="64970-184">システムで機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="64970-184">Enable the feature on your system</span></span>

<span data-ttu-id="64970-185">完了報告時にジョブ カード デバイスがシリアル番号を受け取ることができるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して、次の機能を (この順序で) 有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64970-185">To enable your job card devices to accept a serial number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="64970-186">ジョブ カード デバイスの進捗状況のレポート ダイアログのユーザー エクスペリエンスの向上</span><span class="sxs-lookup"><span data-stu-id="64970-186">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="64970-187">ジョブ カード デバイスからの完了報告時に、バッチ番号とシリアル番号を入力できるようにします。</span><span class="sxs-lookup"><span data-stu-id="64970-187">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device</span></span>

### <a name="configure-products-that-require-serial-number-reporting"></a><span data-ttu-id="64970-188">シリアル番号の報告を必要とする製品をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="64970-188">Configure products that require serial-number reporting</span></span>

<span data-ttu-id="64970-189">利用可能なシリアル管理シナリオをサポートするための製品を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64970-189">To enable a product to support any of the available serial-controlled scenarios, follow these steps:</span></span>

<span data-ttu-id="64970-190">各シナリオを有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="64970-190">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="64970-191">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-191">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="64970-192">構成する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-192">Select the product to configure.</span></span>
1. <span data-ttu-id="64970-193">**在庫の管理** クイックタブの **シリアル番号グループ** フィールドで、シナリオをサポートするように設定されている追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-193">On the **Manage inventory** FastTab, in the **Serial number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="64970-194">シリアル管理された製品にシリアル番号グループが割り当てられていない場合、既定では、完了報告時にジョブ カード デバイスによってシリアル番号の手動のエントリが提供されます。</span><span class="sxs-lookup"><span data-stu-id="64970-194">By default, if no serial number group is assigned to a serial-controlled product, the job card device provides manual entry for the serial number during reporting as finished.</span></span>

<span data-ttu-id="64970-195">次のセクションでは、シリアル管理された品目に関するレポートの 3 つのシナリオをサポートするために、番号グループの追跡を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64970-195">The following sections describe how to set up tracking number groups to support each of the three scenarios for reporting on serial-controlled items.</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a><span data-ttu-id="64970-196">シリアル番号を手動で割り当てることができるように、追跡番号グループを設定する</span><span class="sxs-lookup"><span data-stu-id="64970-196">Set up a tracking number group that lets workers manually assign a serial number</span></span>

<span data-ttu-id="64970-197">シリアル番号を手動で割り当てられるようにするには、これらの手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-197">To allow for manually assigned serial numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="64970-198">**在庫管理 \> 設定 \> 分析コード \> 番号グループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-198">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="64970-199">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-199">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="64970-200">**一般** クイックタブで、**手動** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-200">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="64970-201">![追跡番号グループ ページ、シリアル番号](media/tracking-number-group-manual-serial.png "追跡番号グループ ページ、シリアル番号")</span><span class="sxs-lookup"><span data-stu-id="64970-201">![Tracking number groups page, serial numbers](media/tracking-number-group-manual-serial.png "Tracking number groups page, serial numbers")</span></span>

1. <span data-ttu-id="64970-202">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のシリアル番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-202">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="64970-203">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **シリアル番号** フィールド は、作業者がシリアル番号に任意の値を入力できるテキスト ボックスです。</span><span class="sxs-lookup"><span data-stu-id="64970-203">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value for the serial number.</span></span> <span data-ttu-id="64970-204">値を入力すると、その値がシリアル番号の一覧に追加されます。</span><span class="sxs-lookup"><span data-stu-id="64970-204">On entering a value, it is added to the serial number list.</span></span> <span data-ttu-id="64970-205">この一覧で、作業者は次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="64970-205">In this list,  workers can do the following:</span></span>

- <span data-ttu-id="64970-206">シリアル番号を仕損としてマークするには、該当する行の **仕損** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-206">To mark a serial number as scrapped, select the **Scrap** button for the appropriate row.</span></span> <span data-ttu-id="64970-207">作業者は、**エラーの原因** を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="64970-207">The worker will be prompted to provide an **Error cause**.</span></span>
- <span data-ttu-id="64970-208">シリアル番号を削除するには、該当する行の **削除** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-208">To delete a serial number, select the **Delete** button for the appropriate row.</span></span>

<span data-ttu-id="64970-209">![手動シリアル番号を含むレポートの進行状況ページ](media/job-card-device-serial-manual.png "手動シリアル番号を含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="64970-209">![Report progress page with a field for manual serial numbers](media/job-card-device-serial-manual.png "Report progress page with a field for manual serial numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a><span data-ttu-id="64970-210">事前に定義されたシリアル番号の一覧を提供する追跡番号グループの設定</span><span class="sxs-lookup"><span data-stu-id="64970-210">Set up a tracking number group that provides a list of predefined serial numbers</span></span>

<span data-ttu-id="64970-211">事前に定義されたシリアル番号のリストを提供するには、これらの手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-211">To provide a list of predefined serial numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="64970-212">**在庫管理 \> 設定 \> 分析コード \> 番号グループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-212">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="64970-213">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-213">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="64970-214">**一般** クイックタブで、**在庫取引のみ** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-214">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="64970-215">1 数量あたりのシリアル番号を分割するには、**数量ごと** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="64970-215">Use the **Per qty** field to split serial numbers per quantity of one.</span></span>

    <span data-ttu-id="64970-216">![事前定義シリアル番号の追跡番号グループ](media/tracking-number-group-predefined-sn.png "事前定義シリアル番号の追跡番号グループ")</span><span class="sxs-lookup"><span data-stu-id="64970-216">![A tracking number group for predefined serial numbers](media/tracking-number-group-predefined-sn.png "A tracking number group for predefined serial numbers")</span></span>

1. <span data-ttu-id="64970-217">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のシリアル番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-217">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="64970-218">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **シリアル番号** フィールド は、作業者が任意の値を入力できるドロップダウン リストです。</span><span class="sxs-lookup"><span data-stu-id="64970-218">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="64970-219">![事前に定義されたシリアル番号を含むレポートの進行状況ページ](media/job-card-device-serial-predefined.png "事前に定義されたシリアル番号を含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="64970-219">![Report progress page with a list of predefined serial numbers](media/job-card-device-serial-predefined.png "Report progress page with a list of predefined serial numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a><span data-ttu-id="64970-220">シリアル番号を自動的にで割り当てることができるように、追跡番号グループを設定する</span><span class="sxs-lookup"><span data-stu-id="64970-220">Set up a tracking number group that automatically assigns serial numbers</span></span>

<span data-ttu-id="64970-221">シリアル番号が自動的に割り当てられるようにするには、次の手順に従って追跡番号グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-221">If a serial number should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="64970-222">**在庫管理 \> 設定 \> 分析コード \> 番号グループを追跡** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-222">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="64970-223">設定する追跡番号グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-223">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="64970-224">**一般** クイックタブで、**在庫取引のみ** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-224">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="64970-225">**手動** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-225">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="64970-226">![固定シリアル番号の追跡番号グループ](media/tracking-number-group-fixed-sn.png "固定シリアル番号の追跡番号グループ")</span><span class="sxs-lookup"><span data-stu-id="64970-226">![A tracking number group for fixed serial numbers](media/tracking-number-group-fixed-sn.png "A tracking number group for fixed serial numbers")</span></span>

1. <span data-ttu-id="64970-227">必要に応じてその他の値を設定し、このシナリオを使用するリリース済製品のシリアル番号グループとしてこの追跡番号グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="64970-227">Set other values as you require, and then select this tracking number group as the serial number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="64970-228">このシナリオを使用する場合、ジョブ カード デバイスの **レポートの進行状況** ページに表示される **シリアル番号** フィールド は、値を表示しますが作業者はそれを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="64970-228">When you use this scenario, the **Serial number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span> <span data-ttu-id="64970-229">このシナリオは、シリアル番号管理された品目のいずれか 1 つの数量に対して製造オーダーが作成されている場合にのみ関連があります。</span><span class="sxs-lookup"><span data-stu-id="64970-229">This scenario is only relevant when a production order is created for a quantity of one piece of a serial number-controlled item.</span></span>

<span data-ttu-id="64970-230">![固定シリアル番号を含むレポートの進行状況ページ](media/job-card-device-serial-fixed.png "固定シリアル番号を含むレポートの進行状況ページ")</span><span class="sxs-lookup"><span data-stu-id="64970-230">![Report progress page with a fixed serial number](media/job-card-device-serial-fixed.png "Report progress page with a fixed serial numbers")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="64970-231">ライセンス プレートに完了としてレポートする</span><span class="sxs-lookup"><span data-stu-id="64970-231">Report as finished to a license plate</span></span>

<span data-ttu-id="64970-232">高度な倉庫プロセスでは、ライセンスプレート分析コードを使用して、この目的のために設定された倉庫の場所で在庫を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="64970-232">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="64970-233">この場合、作業者が完了報告済数量を報告するときに、ライセンス プレート番号が必要になります。</span><span class="sxs-lookup"><span data-stu-id="64970-233">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="64970-234">ライセンス プレート報告とラベル印刷を有効にする</span><span class="sxs-lookup"><span data-stu-id="64970-234">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="64970-235">このセクションで説明されている機能を使用するには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して、次の機能を (この順序で) 有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64970-235">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="64970-236">完了報告用ライセンス プレートをジョブ カード デバイスに追加</span><span class="sxs-lookup"><span data-stu-id="64970-236">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="64970-237">ジョブ カード デバイスでの完了報告時に、ライセンス プレート番号の自動生成を有効にする</span><span class="sxs-lookup"><span data-stu-id="64970-237">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="64970-238">ジョブ カード デバイスからラベルを印刷</span><span class="sxs-lookup"><span data-stu-id="64970-238">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="64970-239">ライセンス プレートに完了として報告することを設定する</span><span class="sxs-lookup"><span data-stu-id="64970-239">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="64970-240">既存のライセンスプレートを再利用するか、数量が完了済と報告されたときに新しいライセンスプレートを生成するかを制御するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64970-240">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="64970-241">**生産管理 \> 設定 \> 製造実行 \> デバイスのジョブ カードの構成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-241">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="64970-242">各デバイスに対して次のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-242">Set the following options for each device:</span></span>

    - <span data-ttu-id="64970-243">**ライセンス プレートの生成** - このオプションを **はい** に設定すると、各完了報告に対して新しいライセンス プレートを生成します。</span><span class="sxs-lookup"><span data-stu-id="64970-243">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="64970-244">完了レポートごとに既存のライセンスプレートを使用する場合は、**いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-244">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="64970-245">**印刷ラベル** - 作業員が完了報告ごとにライセンス プレート ラベルを印刷する必要がある場合は、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-245">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="64970-246">ラベルを必要としない場合は、**いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="64970-246">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="64970-247">![デバイス ページのジョブ カードの構成](media/config-job-card-raf.png "デバイス ページのジョブ カードの構成")</span><span class="sxs-lookup"><span data-stu-id="64970-247">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="64970-248">ラベルを構成するには、**倉庫管理 \> 設定 \> ドキュメント回覧 \> ドキュメント回覧** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64970-248">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="64970-249">詳細については、[ライセンス プレート ラベル印刷の有効化](../warehousing/tasks/license-plate-label-printing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64970-249">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]