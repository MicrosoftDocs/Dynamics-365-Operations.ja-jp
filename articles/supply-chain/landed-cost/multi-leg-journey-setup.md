---
title: マルチレッグ行程の設定
description: このトピックでは、陸揚原価モジュールのマルチレッグ行程を設定する方法について説明します。
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e1377b7453622e5bed711753fc2d99258d3c5951
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833764"
---
# <a name="multi-leg-journey-setup"></a><span data-ttu-id="4d01a-103">マルチレッグ行程の設定</span><span class="sxs-lookup"><span data-stu-id="4d01a-103">Multi-leg journey setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d01a-104">このトピックでは、**陸揚原価** モジュールのマルチレッグ行程を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-104">This topic describes how to set up multi-leg journeys for the **Landed cost** module.</span></span>

## <a name="legs"></a><span data-ttu-id="4d01a-105">区間</span><span class="sxs-lookup"><span data-stu-id="4d01a-105">Legs</span></span>

<span data-ttu-id="4d01a-106">区間は行程の異なる部分を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-106">Legs are used to identify separate parts of a journey.</span></span> <span data-ttu-id="4d01a-107">各区間は、「出荷先」および「出荷元」の出荷港 を選択し、その区間に使用する輸送方法を選択して作成されます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-107">Each leg is built by selecting the "to" and "from" shipping ports, and the transportation method that is used for that leg.</span></span> <span data-ttu-id="4d01a-108">リード タイムは各区画に関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-108">Lead times can be associated with each leg.</span></span> <span data-ttu-id="4d01a-109">リード タイムは、出荷の追跡に役立ち、航海中の商品の配送予定日を計算するためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-109">Lead times can help track a shipment and can also be used to calculate the estimated delivery date of the goods on a voyage.</span></span> <span data-ttu-id="4d01a-110">また、行程の区間が完成すると、追跡コントロールの設定を使用して、航海、出荷コンテナー、および関連する発注書明細行のステータスを更新できます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-110">Additionally, when a leg of a journey is completed, the status of the voyage, shipping container, and associated purchase order lines can be updated through the tracking control setup.</span></span> <span data-ttu-id="4d01a-111">区間は、単一の行程テンプレートで使用することも、複数の行程テンプレートで再利用することもできます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-111">Legs can be used by a single journey template, or they can be reused by multiple journey templates.</span></span> <span data-ttu-id="4d01a-112">コンテナの積み込み、関税、および現地ローカル輸送は通常、区間として設定され、非特定の出荷ポートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-112">Container loading, customs, and local transport are generally set up as legs, and a non-specific shipping port is used for them.</span></span>

<span data-ttu-id="4d01a-113">区間を使用するには、**陸揚原価 \> マルチレッグ行程の設定 \> 区間** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-113">To work with legs, go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="4d01a-114">そこで、区間のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-114">There, you can view, open, create, and delete records for legs.</span></span> <span data-ttu-id="4d01a-115">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-115">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="4d01a-116">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d01a-116">Field</span></span> | <span data-ttu-id="4d01a-117">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-117">Description</span></span> |
|---|---|
| <span data-ttu-id="4d01a-118">区間</span><span class="sxs-lookup"><span data-stu-id="4d01a-118">Leg</span></span> | <span data-ttu-id="4d01a-119">行程区間の固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-119">Enter a unique identification name/number for the journey leg.</span></span> |
| <span data-ttu-id="4d01a-120">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-120">Description</span></span> | <span data-ttu-id="4d01a-121">行程区間の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-121">Enter a description of the journey leg.</span></span> <span data-ttu-id="4d01a-122">通常、この説明は、「出荷先」および「出荷元」の港、または行程のステップを識別します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-122">Typically, this description identifies the "to" and "from" ports, or the step of the journey.</span></span> |
| <span data-ttu-id="4d01a-123">出荷元港</span><span class="sxs-lookup"><span data-stu-id="4d01a-123">From port</span></span> | <span data-ttu-id="4d01a-124">区間に商品の原産地を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-124">Enter the point of origin of the goods on the leg.</span></span> |
| <span data-ttu-id="4d01a-125">出荷先港</span><span class="sxs-lookup"><span data-stu-id="4d01a-125">To port</span></span> | <span data-ttu-id="4d01a-126">区間に商品の行先を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-126">Enter the point of destination of the goods on the leg.</span></span> |
| <span data-ttu-id="4d01a-127">配送方法</span><span class="sxs-lookup"><span data-stu-id="4d01a-127">Delivery method</span></span> | <span data-ttu-id="4d01a-128">区間の輸送方法を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-128">Enter the method of transport for the leg.</span></span> |

## <a name="journey-templates"></a><span data-ttu-id="4d01a-129">輸送テンプレート</span><span class="sxs-lookup"><span data-stu-id="4d01a-129">Journey templates</span></span>

<span data-ttu-id="4d01a-130">行程テンプレートは、商品が航海中に移動する 2 つのポート間のマルチレッグ行程を定義します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-130">A journey template defines the multi-leg journey between two ports that goods travel during a voyage.</span></span> <span data-ttu-id="4d01a-131">行程の区間を組み合わせて、商品が仕入先の原産地から最後の倉庫の行先まで移動するのに必要な時間を識別します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-131">The legs of the journey are combined to identify the amount of time that will be required for goods to travel from the vendor's point of origin to the final warehouse destination.</span></span> <span data-ttu-id="4d01a-132">区間が特定の順序で行程テンプレートに配置されると、リード タイムによって各区間の日付と、航海、コンテナー、および航海の購買注文明細行のステータスを識別します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-132">When the legs are put on the journey template in a specific order, the lead times will identify the date of each leg and status of the voyage, container, and purchase lines for the voyage.</span></span> <span data-ttu-id="4d01a-133">[追跡コントロール センター](delivery-information-setup.md) を使用して、行程テンプレートを構成する各区間に関連付けられたリード タイムを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-133">You use the [Tracking control center](delivery-information-setup.md) to set up the lead times that are associated with each leg that makes up the journey template.</span></span> <span data-ttu-id="4d01a-134">行程テンプレートは、航海の自動原価を設定するときにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-134">The journey template is also used when the automatic costs of a voyage are set up.</span></span> <span data-ttu-id="4d01a-135">行程を定義した場合、商品の輸送に関連するコストを自動原価ページで定義できます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-135">When a journey is defined, the cost that is associated with the transport of the goods can be defined on the auto costs page.</span></span>

<span data-ttu-id="4d01a-136">行程テンプレートを使用するには、**陸揚原価 \> マルチレッグ行程の設定 \> 行程テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-136">To work with journey templates, go to **Landed cost \> Multi-leg journey setup \> Journey templates**.</span></span> <span data-ttu-id="4d01a-137">そこで、行程のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-137">There, you can view, open, create, and delete journey templates.</span></span>

<span data-ttu-id="4d01a-138">各行程テンプレートについて、ヘッダーの次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-138">For each journey template, set the following fields on the header.</span></span>

| <span data-ttu-id="4d01a-139">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d01a-139">Field</span></span> | <span data-ttu-id="4d01a-140">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-140">Description</span></span> |
|---|---|
| <span data-ttu-id="4d01a-141">輸送テンプレート</span><span class="sxs-lookup"><span data-stu-id="4d01a-141">Journey template</span></span> | <span data-ttu-id="4d01a-142">行程テンプレートの固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-142">Enter a unique identification name/number for the journey template.</span></span> <span data-ttu-id="4d01a-143">通常、行程テンプレートは、元の場所と原産地および行先を説明します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-143">The journey template typically describes the point of origin and point of destination for the journey.</span></span> |
| <span data-ttu-id="4d01a-144">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-144">Description</span></span> | <span data-ttu-id="4d01a-145">行程テンプレートの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-145">Enter a description of the journey template.</span></span> <span data-ttu-id="4d01a-146">説明は通常、「出荷先」および「出荷元」の港、および移動のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-146">The description typically indicates the "to" and "from" ports, and the type of travel.</span></span> |

<span data-ttu-id="4d01a-147">**明細行** セクションで、行程の各区間に明細行を追加し、明細行を順序に並べます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-147">In the **Lines** section, add a line for each leg of the journey, and put the lines in order.</span></span> <span data-ttu-id="4d01a-148">明細行の順序を変更するには、ツール バーの **上** および **下** 矢印を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-148">Use the **Up** and **Down** arrows on the toolbar to change the order of the lines.</span></span> <span data-ttu-id="4d01a-149">次の表は、各明細行に使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-149">The following table describes the fields that are available for each line.</span></span>

| <span data-ttu-id="4d01a-150">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d01a-150">Field</span></span> | <span data-ttu-id="4d01a-151">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-151">Description</span></span> |
|---|---|
| <span data-ttu-id="4d01a-152">区間</span><span class="sxs-lookup"><span data-stu-id="4d01a-152">Leg</span></span> | <span data-ttu-id="4d01a-153">行程に追加する区間を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-153">Select a leg to add to the journey.</span></span> |
| <span data-ttu-id="4d01a-154">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-154">Description</span></span> | <span data-ttu-id="4d01a-155">区間の説明。</span><span class="sxs-lookup"><span data-stu-id="4d01a-155">The description of the leg.</span></span> |
| <span data-ttu-id="4d01a-156">出荷元港</span><span class="sxs-lookup"><span data-stu-id="4d01a-156">From port</span></span> | <span data-ttu-id="4d01a-157">区間の商品の原産地となる港。</span><span class="sxs-lookup"><span data-stu-id="4d01a-157">The port that is the point of origin of the goods on the leg.</span></span> <span data-ttu-id="4d01a-158">この港は、航海の自動原価を決定するために使用される「出荷先」港です。</span><span class="sxs-lookup"><span data-stu-id="4d01a-158">This port is the "to" port that is used to determine the auto costs for a voyage.</span></span> |
| <span data-ttu-id="4d01a-159">出荷先港</span><span class="sxs-lookup"><span data-stu-id="4d01a-159">To port</span></span> | <span data-ttu-id="4d01a-160">区間の商品の最終目的地の港。</span><span class="sxs-lookup"><span data-stu-id="4d01a-160">The final destination port of the goods on the leg.</span></span> |
| <span data-ttu-id="4d01a-161">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="4d01a-161">Mode of delivery</span></span> | <span data-ttu-id="4d01a-162">区間に使用される配送モード。</span><span class="sxs-lookup"><span data-stu-id="4d01a-162">The mode of delivery that is used for the leg.</span></span> |
| <span data-ttu-id="4d01a-163">輸送出荷元港</span><span class="sxs-lookup"><span data-stu-id="4d01a-163">Journey from port</span></span> | <span data-ttu-id="4d01a-164">区間に指定された港を使用して自動原価を決定する場合は、このチェック ボックスをオンにして、「輸送出荷元」港として識別します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-164">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey from" port.</span></span> <span data-ttu-id="4d01a-165">この港は、航海ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-165">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="4d01a-166">輸送出荷先港</span><span class="sxs-lookup"><span data-stu-id="4d01a-166">Journey to port</span></span> | <span data-ttu-id="4d01a-167">区間に指定された港を使用して自動原価を決定する場合は、このチェック ボックスをオンにして、「輸送出荷先」港として識別します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-167">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey to" port.</span></span> <span data-ttu-id="4d01a-168">この港は、航海ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-168">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="4d01a-169">出荷会社</span><span class="sxs-lookup"><span data-stu-id="4d01a-169">Shipping company</span></span> | <span data-ttu-id="4d01a-170">区間に使用する出荷会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-170">Select the shipping company that is used for the leg.</span></span> |

## <a name="activities"></a><span data-ttu-id="4d01a-171">活動</span><span class="sxs-lookup"><span data-stu-id="4d01a-171">Activities</span></span>

<span data-ttu-id="4d01a-172">**活動** ページの設定は、区間の目的地の港で発生する活動のタイプを確立します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-172">The settings on the **Activities** page establish the types of activities that can occur at the destination port of a leg.</span></span> <span data-ttu-id="4d01a-173">**すべての出荷コンテナー** ページで作業するユーザーは、各活動の期間を見積もり、比較のために実際の期間を記録するときに、これらの値から選択できます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-173">Users who work on the **All shipping containers** page can select among these values when they estimate the duration of each activity and record the actual duration for comparison purposes.</span></span>

<span data-ttu-id="4d01a-174">活動を設定するには、**陸揚原価 \> マルチレッグ行程の設定 \> 活動** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-174">To set up your activities, go to **Landed cost \> Multi-leg journeys setup \> Activities**.</span></span> <span data-ttu-id="4d01a-175">そこで、アクション ウィンドウのボタンを使用して、活動を追加、削除、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="4d01a-175">There, you can add, remove, and edit activities by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="4d01a-176">次の表に、グリッドで各活動に使用できるフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="4d01a-176">The following table describes the fields that are available for each activity in the grid.</span></span>

| <span data-ttu-id="4d01a-177">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d01a-177">Field</span></span> | <span data-ttu-id="4d01a-178">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-178">Description</span></span> |
|---|---|
| <span data-ttu-id="4d01a-179">活動</span><span class="sxs-lookup"><span data-stu-id="4d01a-179">Activity</span></span> | <span data-ttu-id="4d01a-180">活動の名前。</span><span class="sxs-lookup"><span data-stu-id="4d01a-180">The name of the activity.</span></span> |
| <span data-ttu-id="4d01a-181">説明</span><span class="sxs-lookup"><span data-stu-id="4d01a-181">Description</span></span> | <span data-ttu-id="4d01a-182">活動の説明。</span><span class="sxs-lookup"><span data-stu-id="4d01a-182">A description of the activity.</span></span> |
| <span data-ttu-id="4d01a-183">出荷会社</span><span class="sxs-lookup"><span data-stu-id="4d01a-183">Shipping company</span></span> | <span data-ttu-id="4d01a-184">活動に関連付けられている出荷会社の仕入先口座。</span><span class="sxs-lookup"><span data-stu-id="4d01a-184">The vendor account of the shipping company that is associated with the activity.</span></span> |
