---
title: "モバイル デバイスを使用して材料消費を登録する"
description: "このトピックでは、ハンドヘルド デバイスを使用して生産における原材料消費の登録を可能にするワークフローについて説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 525b5a21047f0f39b9cd15448c4096d17c0e2dbd
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="1ba96-103">モバイル デバイスを使用して材料消費を登録する</span><span class="sxs-lookup"><span data-stu-id="1ba96-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="1ba96-104">このトピックでは、ハンドヘルド デバイスを使用して生産における原材料消費の登録を可能にするワークフローについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="1ba96-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="1ba96-105">Introduction</span></span>
------------

<span data-ttu-id="1ba96-106">このワークフローは、材料の追跡に厳密な要件がある場合に有効です。</span><span class="sxs-lookup"><span data-stu-id="1ba96-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="1ba96-107">その場合、材料の追跡を管理するために、消費に関する正確な時間と数量を報告する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ba96-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="1ba96-108">このプロセスはプレフラッシュまたはバックフラッシュの工程とは異なって見ることができ、登録の時間と実際の消費が行われる時期の間にオフセットが存在します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="1ba96-109">これが、追跡の要件を持つ一部の材料に対して自動消費する方法を使用できない理由です。</span><span class="sxs-lookup"><span data-stu-id="1ba96-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="1ba96-110">ハンドヘルド デバイスを使用して生産における原材料消費の登録を可能にするワークフローの設定方法を説明する簡単なシナリオを見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="1ba96-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="1ba96-111">[![ハンドヘルド デバイスを使用して原材料消費の登録を有効にするワークフローの設定](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="1ba96-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="1ba96-112">シナリオの詳細</span><span class="sxs-lookup"><span data-stu-id="1ba96-112">Scenario details</span></span>

<span data-ttu-id="1ba96-113">継続的な生産プロセス (5) では、バッチ管理されている原材料 RM-100 が消費されます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="1ba96-114">材料が、それぞれ 100 ポンドの 2 つのバッチ B1 および B2 でライセンス プレート PL-1 の場所 Bulk-001 (1) に手持在庫であります。</span><span class="sxs-lookup"><span data-stu-id="1ba96-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="1ba96-115">倉庫作業 (2) がリリースされ、RM-100 が処理され、Bulk-001 からライセンス プレートにより制御されていないものと定義される生産入庫の場所 PIL-01 (3) にピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="1ba96-116">機械オペレーターは生産入庫の場所 (3) の材料の重さを計測し、その重量とバッチ番号を消費済 (4) として登録します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="1ba96-117">生産入庫の場所から、定義済の時間間隔で材料の一部が手動で生産プロセスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="1ba96-118">機械オペレーターが材料を追加すると、スケールで計量され、バッチ番号が登録されます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="1ba96-119">ハンドヘルド デバイスを使用して消費を登録するワークフローの設定</span><span class="sxs-lookup"><span data-stu-id="1ba96-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="1ba96-120">バッチ管理されている原材料 RM-100 がある部品表で、完成品 FG-100 を作成します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="1ba96-121">RM-100 の 2 つのバッチ B1 および B2 を、100 の数量で場所 Bulk-001 にライセンス プレート PL-1 で追加します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="1ba96-122">RM-100 の部品表の部品消費ルールが [**手動**] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="1ba96-123">生産入庫の場所を PIL-01 に設定します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="1ba96-124">倉庫 51 でこの場所を既定の生産入庫の場所として選択することでこの操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="1ba96-125">新しいモバイル デバイス メニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="1ba96-126">**メニュー項目名** - 材料消費を登録します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="1ba96-127">**タイトル** - 材料消費を登録します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="1ba96-128">**モード** - 間接。</span><span class="sxs-lookup"><span data-stu-id="1ba96-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="1ba96-129">**活動コード** - 材料消費を登録します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="1ba96-130">メニュー項目を [**製造モバイル**] デバイス メニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="1ba96-131">完成品の製造オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="1ba96-132">**品目番号** - FG-100</span><span class="sxs-lookup"><span data-stu-id="1ba96-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="1ba96-133">**サイト** - 5</span><span class="sxs-lookup"><span data-stu-id="1ba96-133">**Site** - 5</span></span> 
-    <span data-ttu-id="1ba96-134">**倉庫** - 51</span><span class="sxs-lookup"><span data-stu-id="1ba96-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="1ba96-135">**数量** - 150</span><span class="sxs-lookup"><span data-stu-id="1ba96-135">**Quantity** - 150</span></span>

<span data-ttu-id="1ba96-136">製造オーダーが [**見積済**] および [**リリース済**] になり、倉庫作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="1ba96-137">ハンドヘルド デバイスの原材料ピッキングのワークフローを使用して作業を完了します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="1ba96-138">これでバルク場所から生産入庫の場所 PIL-01 に材料が移ります。</span><span class="sxs-lookup"><span data-stu-id="1ba96-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="1ba96-139">作業が完了した後、材料のステータスが [**生産入庫の場所でピッキング済み**] になります。</span><span class="sxs-lookup"><span data-stu-id="1ba96-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="1ba96-140">作業が処理された後のステータスは、[**ピッキング済**] または [**引当済現物**] のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="1ba96-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="1ba96-141">これは、パラメーター [**倉庫フォームで配置後にステータスを発行**] でコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="1ba96-142">[**生産開始**] のメニュー項目を使用して、クライアントまたはハンドヘルド デバイスのいずれかから製造オーダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="1ba96-143">製造オーダーが開始された後は、ハンドヘルド デバイスのワークフローで材料消費を登録できます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="1ba96-144">まず、バッチ B1 の 25 ポンドの消費を登録します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="1ba96-145">ハンドヘルド デバイスのメニューの [**材料消費の****登録**] のメニュー項目を選択して、次の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="1ba96-146">製造オーダー番号。</span><span class="sxs-lookup"><span data-stu-id="1ba96-146">The production order number.</span></span> 
-    <span data-ttu-id="1ba96-147">このケース PIL-01 で材料が消費される場所。</span><span class="sxs-lookup"><span data-stu-id="1ba96-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="1ba96-148">品目番号 RM-100。</span><span class="sxs-lookup"><span data-stu-id="1ba96-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="1ba96-149">バッチ番号 B1。</span><span class="sxs-lookup"><span data-stu-id="1ba96-149">Batch number B1.</span></span> 
-    <span data-ttu-id="1ba96-150">25 の数量。</span><span class="sxs-lookup"><span data-stu-id="1ba96-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="1ba96-151">[**OK**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-151">Select **OK**.</span></span>

<span data-ttu-id="1ba96-152">ディスプレイに「仕訳帳明細行が作成されました」というメッセージが表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1ba96-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="1ba96-153">製造オーダーに、品目番号 RM-100 およびバッチ番号 B1 のタイプ [**生産ピッキング リスト**] の未処理の仕訳帳があります。</span><span class="sxs-lookup"><span data-stu-id="1ba96-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="1ba96-154">バッチ番号 B2 など、登録を選択して続行できるようになり、[**OK**] を選択するたびに、新しい仕訳帳明細行が未処理の仕訳帳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="1ba96-155">登録が完了したら、[**実行**] を選択して仕訳帳に転記し、ワークフローを終了します。</span><span class="sxs-lookup"><span data-stu-id="1ba96-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="1ba96-156">追加コメント</span><span class="sxs-lookup"><span data-stu-id="1ba96-156">Additional comments</span></span> 

-   <span data-ttu-id="1ba96-157">ユーザーが仕訳帳が作成された後にワークフローをキャンセルする場合、仕訳帳は未転記の状態になりますが、後から同じ製造オーダーのワークフローを使用する場合、明細行は新しい仕訳帳ではなく未処理の仕訳帳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="1ba96-158">新しいワークフローは、シリアル番号の登録もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1ba96-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="1ba96-159">部品表または選択した製造オーダーやバッチ オーダーのフォーミュラで定義された品目番号のみ登録することができます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="1ba96-160">材料は超過消費することができます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-160">Material can be overconsumed.</span></span> <span data-ttu-id="1ba96-161">たとえば、材料が 100 ポンドの数量で消費される見積の場合、105 ポンドといった数量で超過消費することができます。</span><span class="sxs-lookup"><span data-stu-id="1ba96-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>


