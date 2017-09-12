---
title: "在庫棚卸プロセスの定義"
description: "この手順は、棚卸グループおよび棚卸仕訳帳を作成することによって、基本的な在庫棚卸処理のコンフィギュレーションについて説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: c14c846c55a3d821945160835817cd4f467deda9
ms.contentlocale: ja-jp
ms.lasthandoff: 09/12/2017

---
# <a name="define-inventory-counting-processes"></a><span data-ttu-id="16bd5-103">在庫棚卸プロセスの定義</span><span class="sxs-lookup"><span data-stu-id="16bd5-103">Define inventory counting processes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16bd5-104">この手順は、棚卸グループおよび棚卸仕訳帳を作成することによって、基本的な在庫棚卸処理のコンフィギュレーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-104">This procedure walks you through the configuration of basic inventory counting processes by creating a counting group and a counting journal.</span></span> <span data-ttu-id="16bd5-105">また、倉庫と品目レベルにおける棚卸ポリシーを有効にする方法も説明します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-105">It also shows you how to enable counting policies on a warehouse and item level.</span></span> <span data-ttu-id="16bd5-106">通常、これらのタスクを実施するのは、倉庫の監督です。</span><span class="sxs-lookup"><span data-stu-id="16bd5-106">These tasks would typically be carried out by a warehouse supervisor.</span></span> <span data-ttu-id="16bd5-107">これは、現在リリースされている一部の製品および倉庫を所有する前提条件となっています。</span><span class="sxs-lookup"><span data-stu-id="16bd5-107">It is a prerequisite to have some existing released products and warehouses.</span></span> <span data-ttu-id="16bd5-108">デモ データの会社を使用すると、いずれの在庫品目を使用しても、USMF 会社でこの手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-108">If you're using a demo data company, you can run this procedure in the USMF company with any stocked item.</span></span>


## <a name="create-a-counting-group"></a><span data-ttu-id="16bd5-109">棚卸グループの作成</span><span class="sxs-lookup"><span data-stu-id="16bd5-109">Create a counting group</span></span>
1. <span data-ttu-id="16bd5-110">[在庫管理] > [設定] > [在庫] > [棚卸グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-110">Go to Inventory management > Setup > Inventory > Counting groups.</span></span>
2. <span data-ttu-id="16bd5-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-111">Click New.</span></span>
3. <span data-ttu-id="16bd5-112">[棚卸グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-112">In the Counting group field, type a value.</span></span>
4. <span data-ttu-id="16bd5-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="16bd5-114">[棚卸コード] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-114">In the Counting code field, select an option.</span></span>
    * <span data-ttu-id="16bd5-115">手動 - ジョブを実行するたびに明細行を含めます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-115">Manual – Includes lines every time you run the job.</span></span> <span data-ttu-id="16bd5-116">つまり、棚卸グループの棚卸の間隔を自分で決定します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-116">In other words, you decide the counting interval for the counting group.</span></span>  <span data-ttu-id="16bd5-117">期間 – 期間間隔の期限が切れたときに、棚卸仕訳帳に期間の明細行を含めます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-117">Period – Includes lines for the period in the counting journal when the period interval has expired.</span></span>   <span data-ttu-id="16bd5-118">在庫なし – 手持在庫がゼロ (0) になった場合は、ジョブが実行されたときに棚卸仕訳帳に明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-118">Zero in stock – If on-hand inventory reaches zero (0), lines are generated in the counting journal when the job is run.</span></span> <span data-ttu-id="16bd5-119">棚卸後に手持ち在庫が 0 になった場合は、次に棚卸を実行したときに明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-119">If the on-hand inventory reaches 0 after a count, lines are generated the next time that you start the count.</span></span>   <span data-ttu-id="16bd5-120">最小 - 手持在庫が指定された最小値以下である場合は、棚卸仕訳帳に明細行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-120">Minimum – Inserts lines in the counting journal if the on-hand inventory is equal to or less than the minimum that is specified.</span></span>  
    * <span data-ttu-id="16bd5-121">オプション: [棚卸コード] フィールドで特定「期間」を指定した場合、[棚卸期間] フィールドに期間の範囲を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16bd5-121">Optional: If you have specified Period in the Counting code field, you must type the interval for the period in the Counting period field.</span></span> <span data-ttu-id="16bd5-122">間隔の単位に日を使用します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-122">The unit for intervals is days.</span></span>  
    * <span data-ttu-id="16bd5-123">棚卸仕訳帳に新しい行を作成するジョブを実行すると、同じジョブを実行する頻度に関係なく、このフィールドに指定した間隔で新しい行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-123">When you run the job for creating new lines in the counting journal, new lines are created at the interval specified in this field, regardless of how often you run the same job.</span></span> <span data-ttu-id="16bd5-124">たとえば、「棚卸期間」を 7 と設定し、1 月 1 日に仕訳帳明細行が生成され、別のジョブが 1 月 5 日に開始される場合、7 日間経過しないとその期間中に明細行は仕訳帳に生成されません。</span><span class="sxs-lookup"><span data-stu-id="16bd5-124">For example, if Counting period is set to 7, and journal lines were last generated for a count on January 1, if another job is started on January 5, seven days have not passed and so no lines are generated in the journal for that period interval.</span></span> <span data-ttu-id="16bd5-125">ジョブを 1 月 8 日に再度開始した場合、経過日数は 7 日を超えているので、棚卸仕訳帳にその期間の明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-125">If you start the job again on January 8, lines are generated for the period in the counting journal, because 7 days have passed.</span></span>  
6. <span data-ttu-id="16bd5-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-126">Click Save.</span></span>

## <a name="create-a-counting-journal-name"></a><span data-ttu-id="16bd5-127">棚卸仕訳帳名の作成</span><span class="sxs-lookup"><span data-stu-id="16bd5-127">Create a counting journal name</span></span>
1. <span data-ttu-id="16bd5-128">[在庫管理] > [設定] > [仕訳帳名] > [在庫] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-128">Go to Inventory management > Setup > Journal names > Inventory.</span></span>
2. <span data-ttu-id="16bd5-129">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-129">Click New.</span></span>
3. <span data-ttu-id="16bd5-130">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-130">In the Name field, type a value.</span></span>
4. <span data-ttu-id="16bd5-131">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-131">In the Description field, type a value.</span></span>
5. <span data-ttu-id="16bd5-132">[仕訳帳タイプ] フィールドで、「棚卸」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-132">In the Journal type field, select 'Counting'.</span></span>
    * <span data-ttu-id="16bd5-133">オプション: 棚卸仕訳帳を作成するときに生成される伝票 ID の固有の番号順序を入手する場合、別の伝票シリーズの ID を選択できます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-133">Optional: you can select a different voucher series ID if you want a specific number sequence for the voucher IDs generated when creating counting journals.</span></span> <span data-ttu-id="16bd5-134">伝票シリーズは、[番号順序] ページで作成します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-134">Voucher series are created in the Number sequences page.</span></span>  
6. <span data-ttu-id="16bd5-135">[詳細レベル] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-135">In the Detail level field, select an option.</span></span>
    * <span data-ttu-id="16bd5-136">これは仕訳帳が転記されるときに適用される詳細レベルです。</span><span class="sxs-lookup"><span data-stu-id="16bd5-136">This is the level of detail that is applied when the journal is posted.</span></span>  
    * <span data-ttu-id="16bd5-137">オプション: [引当] フィールドの値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-137">Optional: you can change the value in the Reservation field.</span></span> <span data-ttu-id="16bd5-138">これは、棚卸中の品目を引当てるために使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="16bd5-138">This is the method used to reserve items during counting.</span></span>   
    * <span data-ttu-id="16bd5-139">手動 – [引当] フォームで品目が手動で引当られます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-139">Manual – The items are reserved manually in the Reservation form.</span></span>   <span data-ttu-id="16bd5-140">自動 – 注文数量は、利用可能な品目の手持在庫から引当られます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-140">Automatic – The order quantity is reserved from the available, on-hand inventory for the item.</span></span>   <span data-ttu-id="16bd5-141">展開 – 引当は、トランザクションのマスター プランの一部です。</span><span class="sxs-lookup"><span data-stu-id="16bd5-141">Explosion – The reservation is part of the master planning of the transaction.</span></span>  
7. <span data-ttu-id="16bd5-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-142">Click Save.</span></span>

## <a name="set-standard-counting-journal-name"></a><span data-ttu-id="16bd5-143">標準棚卸仕訳帳名の設定</span><span class="sxs-lookup"><span data-stu-id="16bd5-143">Set standard counting journal name</span></span>
1. <span data-ttu-id="16bd5-144">[在庫管理] > [設定] > [在庫および倉庫管理パラメーター] を表示します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-144">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="16bd5-145">[仕訳帳] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-145">Click the Journals tab.</span></span>
3. <span data-ttu-id="16bd5-146">[棚卸] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-146">In the Counting field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="16bd5-147">以前に作成した仕訳を選択します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-147">Select the journal you previously created.</span></span>
    * <span data-ttu-id="16bd5-148">この仕訳帳は、棚卸タイプにおける在庫仕訳帳の既定仕訳帳名となります。</span><span class="sxs-lookup"><span data-stu-id="16bd5-148">This journal will then be the default journal name for inventory journals of the Counting type.</span></span>  
5. <span data-ttu-id="16bd5-149">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-149">Click the General tab.</span></span>
    * <span data-ttu-id="16bd5-150">オプション: 梱包明細票、ピッキング リスト、またはピッキング リスト登録が更新されないように、棚卸処理中に品目をロックするため、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-150">Optional: Select this option to lock an item during the counting process to prevent updates for packing slips, picking lists, or picking list registrations.</span></span>  

## <a name="set-the-counting-policy-for-an-item"></a><span data-ttu-id="16bd5-151">品目棚仕訳帳卸の設定</span><span class="sxs-lookup"><span data-stu-id="16bd5-151">Set the counting policy for an item</span></span>
1. <span data-ttu-id="16bd5-152">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-152">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="16bd5-153">一覧で、棚卸ポリシーを設定する製品の品目番号のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-153">In the list, click on the link for the Item number of the product that you want to set counting policies on.</span></span>
    * <span data-ttu-id="16bd5-154">追跡される在庫から品目を選択する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="16bd5-154">Note that you need to select an item that is inventory tracked.</span></span> <span data-ttu-id="16bd5-155">非在庫製品はカウントできません。</span><span class="sxs-lookup"><span data-stu-id="16bd5-155">A non-stocked product can't be counted.</span></span> <span data-ttu-id="16bd5-156">デモ データの会社 USMF を使用する場合は、品目「A0001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-156">If you are using USMF demo data you can select item A0001.</span></span>  
3. <span data-ttu-id="16bd5-157">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-157">Click Edit.</span></span>
4. <span data-ttu-id="16bd5-158">[在庫の管理] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-158">Toggle the expansion of the Manage inventory section.</span></span>
5. <span data-ttu-id="16bd5-159">[棚卸グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-159">In the Counting group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="16bd5-160">一覧で、以前に作成した棚卸グループをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-160">In the list, click on the counting group you previously created.</span></span>
    * <span data-ttu-id="16bd5-161">この製品は、棚卸グループを使用して在庫仕訳帳明細行が作成されるときに含まれます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-161">This product will now be included when inventory counting journal lines are created using this counting group.</span></span>  
7. <span data-ttu-id="16bd5-162">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-162">Click Save.</span></span>

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a><span data-ttu-id="16bd5-163">倉庫品目の棚卸ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="16bd5-163">Set the counting policy for an item in a specific warehouse</span></span>
1. <span data-ttu-id="16bd5-164">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-164">On the Action Pane, click Manage inventory.</span></span>
2. <span data-ttu-id="16bd5-165">[倉庫品] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-165">Click Warehouse items.</span></span>
3. <span data-ttu-id="16bd5-166">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-166">Click New.</span></span>
4. <span data-ttu-id="16bd5-167">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-167">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="16bd5-168">一覧で、特定の棚卸ポリシーを設定する倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="16bd5-168">In the list, select the warehouse you want set up specific counting policies for.</span></span>
6. <span data-ttu-id="16bd5-169">[棚卸グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-169">In the Counting group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="16bd5-170">一覧で棚卸グループの選択</span><span class="sxs-lookup"><span data-stu-id="16bd5-170">In the list, select a counting group</span></span>
    * <span data-ttu-id="16bd5-171">選択した特定倉庫の品目に適用される特定棚卸グループをここで選択できます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-171">Here you can select a specific counting group that should apply to the item in the specific warehouse you have selected.</span></span> <span data-ttu-id="16bd5-172">その倉庫で棚卸が実行される場合、この棚卸ポリシーによって、品目における一般的な棚卸ポリシーは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="16bd5-172">When counting is performed in that warehouse, this counting policy will override the general counting policy for the item.</span></span>  
8. <span data-ttu-id="16bd5-173">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16bd5-173">Click Save.</span></span>

