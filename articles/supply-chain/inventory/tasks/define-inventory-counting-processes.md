---
title: 在庫棚卸プロセスの定義
description: このトピックでは、棚卸グループおよび棚卸仕訳帳を作成することによって、基本的な在庫棚卸処理のコンフィギュレーションについて説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df5db0e71f550e82820e15b1597d9e287071f83
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214001"
---
# <a name="define-inventory-counting-processes"></a><span data-ttu-id="e6d04-103">在庫棚卸プロセスの定義</span><span class="sxs-lookup"><span data-stu-id="e6d04-103">Define inventory counting processes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6d04-104">このトピックでは、棚卸グループおよび棚卸仕訳帳を作成することによって、基本的な在庫棚卸処理のコンフィギュレーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-104">This topic describes the configuration of basic inventory counting processes by creating a counting group and a counting journal.</span></span> <span data-ttu-id="e6d04-105">また、倉庫と品目レベルにおける棚卸ポリシーを有効にする方法も説明します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-105">It also shows you how to enable counting policies on a warehouse and item level.</span></span> <span data-ttu-id="e6d04-106">通常、これらのタスクを実施するのは、倉庫の監督です。</span><span class="sxs-lookup"><span data-stu-id="e6d04-106">These tasks would typically be carried out by a warehouse supervisor.</span></span> <span data-ttu-id="e6d04-107">これは、現在リリースされている一部の製品および倉庫を所有する前提条件となっています。</span><span class="sxs-lookup"><span data-stu-id="e6d04-107">It is a prerequisite to have some existing released products and warehouses.</span></span> <span data-ttu-id="e6d04-108">デモ データの会社を使用すると、いずれの在庫品目を使用しても、USMF 会社でこの手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-108">If you're using a demo data company, you can run this procedure in the USMF company with any stocked item.</span></span>


## <a name="create-a-counting-group"></a><span data-ttu-id="e6d04-109">棚卸グループの作成</span><span class="sxs-lookup"><span data-stu-id="e6d04-109">Create a counting group</span></span>
1. <span data-ttu-id="e6d04-110">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫 > 棚卸グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-110">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory > Counting groups**.</span></span>
2. <span data-ttu-id="e6d04-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-111">Select **New**.</span></span>
3. <span data-ttu-id="e6d04-112">新しい行の**棚卸グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-112">In the **Counting group** field of the new row, type a value.</span></span>
4. <span data-ttu-id="e6d04-113">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-113">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="e6d04-114">**棚卸コード** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-114">In the **Counting code** field, select an option.</span></span>

    - <span data-ttu-id="e6d04-115">**手動** – ジョブを実行するたびに明細行を含めます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-115">**Manual** – Includes lines every time you run the job.</span></span> <span data-ttu-id="e6d04-116">つまり、棚卸グループの棚卸の間隔を自分で決定します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-116">In other words, you decide the counting interval for the counting group.</span></span>  
    - <span data-ttu-id="e6d04-117">**期間** – 期間間隔の期限が切れたときに、棚卸仕訳帳に期間の明細行を含めます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-117">**Period** – Includes lines for the period in the counting journal when the period interval has expired.</span></span>  
    - <span data-ttu-id="e6d04-118">**在庫なし** – 手持在庫がゼロ (0) になった場合は、ジョブが実行されたときに棚卸仕訳帳に明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-118">**Zero in stock** – If on-hand inventory reaches zero (0), lines are generated in the counting journal when the job is run.</span></span> <span data-ttu-id="e6d04-119">棚卸後に手持ち在庫が 0 になった場合は、次に棚卸を実行したときに明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-119">If the on-hand inventory reaches 0 after a count, lines are generated the next time that you start the count.</span></span>  
    - <span data-ttu-id="e6d04-120">**最小** – 手持在庫が指定された最小値以下である場合は、棚卸仕訳帳に明細行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-120">**Minimum** – Inserts lines in the counting journal if the on-hand inventory is equal to or less than the minimum that is specified.</span></span>  
    - <span data-ttu-id="e6d04-121">オプション: **棚卸コード** フィールドで特定**期間**を指定した場合、**棚卸期間**フィールドに期間の範囲を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6d04-121">Optional: If you have specified **Period** in the **Counting code** field, you must type the interval for the period in the **Counting period** field.</span></span> <span data-ttu-id="e6d04-122">間隔の単位に日を使用します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-122">The unit for intervals is days.</span></span>  
    - <span data-ttu-id="e6d04-123">棚卸仕訳帳に新しい行を作成するジョブを実行すると、同じジョブを実行する頻度に関係なく、このフィールドに指定した間隔で新しい行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-123">When you run the job for creating new lines in the counting journal, new lines are created at the interval specified in this field, regardless of how often you run the same job.</span></span> <span data-ttu-id="e6d04-124">たとえば、**棚卸期間**を 7 と設定し、1 月 1 日に仕訳帳明細行が生成され、別のジョブが 1 月 5 日に開始される場合、7 日間経過しないとその期間中に明細行は仕訳帳に生成されません。</span><span class="sxs-lookup"><span data-stu-id="e6d04-124">For example, if **Counting period** is set to 7, and journal lines were last generated for a count on January 1, if another job is started on January 5, seven days have not passed and so no lines are generated in the journal for that period interval.</span></span> <span data-ttu-id="e6d04-125">ジョブを 1 月 8 日に再度開始した場合、経過日数は 7 日を超えているので、棚卸仕訳帳にその期間の明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-125">If you start the job again on January 8, lines are generated for the period in the counting journal, because 7 days have passed.</span></span>  

6. <span data-ttu-id="e6d04-126">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-126">Select **Save**.</span></span>

## <a name="create-a-counting-journal-name"></a><span data-ttu-id="e6d04-127">棚卸仕訳帳名の作成</span><span class="sxs-lookup"><span data-stu-id="e6d04-127">Create a counting journal name</span></span>
1. <span data-ttu-id="e6d04-128">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 仕訳帳名 > 在庫**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-128">In the navigation pane, go to **Modules > Inventory management > Setup > Journal names > Inventory**.</span></span>
2. <span data-ttu-id="e6d04-129">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-129">Select **New**.</span></span>
3. <span data-ttu-id="e6d04-130">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-130">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="e6d04-131">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e6d04-132">**仕訳帳タイプ** フィールドで、**棚卸**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-132">In the **Journal type** field, select **Counting**.</span></span> <span data-ttu-id="e6d04-133">オプション: 棚卸仕訳帳を作成するときに生成される伝票 ID の固有の番号順序を入手する場合、別の伝票シリーズの ID を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-133">Optional: you can select a different voucher series ID if you want a specific number sequence for the voucher IDs generated when creating counting journals.</span></span> <span data-ttu-id="e6d04-134">伝票シリーズは、**番号順序**ページで作成します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-134">Voucher series are created in the **Number sequences** page.</span></span>  
6. <span data-ttu-id="e6d04-135">**詳細レベル** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-135">In the **Detail level** field, select an option.</span></span>  

    - <span data-ttu-id="e6d04-136">これは仕訳帳が転記されるときに適用される詳細レベルです。</span><span class="sxs-lookup"><span data-stu-id="e6d04-136">This is the level of detail that is applied when the journal is posted.</span></span>  
    - <span data-ttu-id="e6d04-137">オプション: [引当] フィールドの値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-137">Optional: you can change the value in the Reservation field.</span></span> <span data-ttu-id="e6d04-138">これは、棚卸中の品目を引当てるために使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="e6d04-138">This is the method used to reserve items during counting.</span></span>   
    - <span data-ttu-id="e6d04-139">**手動** – 引当フォームで品目が手動で引当られます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-139">**Manual** – The items are reserved manually in the Reservation form.</span></span>  
    - <span data-ttu-id="e6d04-140">**自動** – 注文数量は、利用可能な品目の手持在庫から引当られます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-140">**Automatic** – The order quantity is reserved from the available, on-hand inventory for the item.</span></span>   
    - <span data-ttu-id="e6d04-141">**展開** – 引当は、トランザクションのマスター プランの一部です。</span><span class="sxs-lookup"><span data-stu-id="e6d04-141">**Explosion** – The reservation is part of the master planning of the transaction.</span></span>  

7. <span data-ttu-id="e6d04-142">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-142">Select **Save**.</span></span>

## <a name="set-standard-counting-journal-name"></a><span data-ttu-id="e6d04-143">標準棚卸仕訳帳名の設定</span><span class="sxs-lookup"><span data-stu-id="e6d04-143">Set standard counting journal name</span></span>
1. <span data-ttu-id="e6d04-144">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫および倉庫管理パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-144">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="e6d04-145">**仕訳帳**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-145">Select the **Journals** tab.</span></span>
3. <span data-ttu-id="e6d04-146">**棚卸**フィールドのドロップダウン メニューで、以前に作成した仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-146">In the drop down menu of the **Counting** field, select the journal you previously created.</span></span> <span data-ttu-id="e6d04-147">この仕訳帳は、**棚卸**タイプにおける在庫仕訳帳の既定仕訳帳名となります。</span><span class="sxs-lookup"><span data-stu-id="e6d04-147">This journal will then be the default journal name for inventory journals of the **Counting** type.</span></span>  
4. <span data-ttu-id="e6d04-148">**一般**タブを選択します。オプション: 梱包明細票、ピッキング リスト、またはピッキング リスト登録が更新されないように、棚卸処理中に品目をロックするため、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-148">Select the **General** tab. Optional: Select this option to lock an item during the counting process to prevent updates for packing slips, picking lists, or picking list registrations.</span></span>  

## <a name="set-the-counting-policy-for-an-item"></a><span data-ttu-id="e6d04-149">品目棚仕訳帳卸の設定</span><span class="sxs-lookup"><span data-stu-id="e6d04-149">Set the counting policy for an item</span></span>
1. <span data-ttu-id="e6d04-150">ナビゲーション ウィンドウで、**モジュール > 製品情報管理 > 製品 > リリース済製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-150">In the navigation pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="e6d04-151">一覧で、棚卸ポリシーを設定する製品の品目番号のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-151">In the list, select the link for the Item number of the product that you want to set counting policies on.</span></span> <span data-ttu-id="e6d04-152">追跡される在庫から品目を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6d04-152">You must select an item that is inventory tracked.</span></span> <span data-ttu-id="e6d04-153">非在庫製品はカウントできません。</span><span class="sxs-lookup"><span data-stu-id="e6d04-153">A non-stocked product can't be counted.</span></span> <span data-ttu-id="e6d04-154">デモ データの会社 USMF を使用する場合は、品目「A0001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-154">If you are using USMF demo data you can select item A0001.</span></span>  
3. <span data-ttu-id="e6d04-155">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-155">Select **Edit**.</span></span>
4. <span data-ttu-id="e6d04-156">**在庫の管理**セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-156">Toggle the expansion of the **Manage inventory** section.</span></span>
5. <span data-ttu-id="e6d04-157">**棚卸グループ** フィールドのドロップダウン メニューで、以前に作成した棚卸グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-157">In the drop-down menu of the **Counting group** field, select the counting group you previously created.</span></span> <span data-ttu-id="e6d04-158">この製品は、棚卸グループを使用して在庫仕訳帳明細行が作成されるときに含まれます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-158">This product will now be included when inventory counting journal lines are created using this counting group.</span></span>  
6. <span data-ttu-id="e6d04-159">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-159">Select **Save**.</span></span>

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a><span data-ttu-id="e6d04-160">倉庫品目の棚卸ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="e6d04-160">Set the counting policy for an item in a specific warehouse</span></span>
1. <span data-ttu-id="e6d04-161">アクション ウィンドウで、**在庫の管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-161">On the Action Pane, select **Manage inventory**.</span></span>
2. <span data-ttu-id="e6d04-162">**在庫品**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-162">Select **Warehouse items**.</span></span>
3. <span data-ttu-id="e6d04-163">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-163">Select **New**.</span></span>
4. <span data-ttu-id="e6d04-164">**倉庫**フィールドのドロップダウン メニューで、特定の棚卸ポリシーを設定する倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-164">In the drop-down menu of the **Warehouse** field, select the warehouse you want to set up specific counting policies for.</span></span>
5. <span data-ttu-id="e6d04-165">**棚卸グループ** フィールドのドロップダウン メニューで、棚卸グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-165">In the drop-down menu of the **Counting group** field, select a counting group.</span></span> <span data-ttu-id="e6d04-166">選択した特定倉庫の品目に適用される特定棚卸グループを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-166">You can select a specific counting group that should apply to the item in the specific warehouse you have selected.</span></span> <span data-ttu-id="e6d04-167">その倉庫で棚卸が実行される場合、この棚卸ポリシーによって、品目における一般的な棚卸ポリシーは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="e6d04-167">When counting is performed in that warehouse, this counting policy will override the general counting policy for the item.</span></span>  
6. <span data-ttu-id="e6d04-168">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6d04-168">Select **Save**.</span></span>

