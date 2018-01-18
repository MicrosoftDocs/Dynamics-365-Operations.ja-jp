---
title: "シフトとキャッシュ ドロワーの管理"
description: "この記事では、小売販売時点管理 (POS) シフトにおける 2 つのタイプの設定および使用方法について説明します - 共有およびスタンドアロン。 共有シフトは、複数の場所で複数のユーザーにより使用できますが、スタンドアロン シフトは、一度に 1 人の作業者しか使用できません。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 69a1032ae279dc55e0e7ee3801c1e7b97d8a2cf5
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="c5af3-104">シフトとキャッシュ ドロワーの管理</span><span class="sxs-lookup"><span data-stu-id="c5af3-104">Shift and cash drawer management</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c5af3-105">この記事では、小売販売時点管理 (POS) シフトにおける 2 つのタイプの設定および使用方法について説明します - 共有およびスタンドアロン。</span><span class="sxs-lookup"><span data-stu-id="c5af3-105">This article explains how to set up and use the two types of retail point of sale (POS) shifts -  shared and stand-alone.</span></span> <span data-ttu-id="c5af3-106">共有シフトは、複数の場所で複数のユーザーにより使用できますが、スタンドアロン シフトは、一度に 1 人の作業者しか使用できません。</span><span class="sxs-lookup"><span data-stu-id="c5af3-106">Shared shifts can be used by multiple users in multiple places, whereas stand-alone shifts can be used by only one worker at a time.</span></span>

<span data-ttu-id="c5af3-107">販売時点管理 (POS) シフトには 2 種類あります: スタンドアロンと共有です。</span><span class="sxs-lookup"><span data-stu-id="c5af3-107">There are two types of retail point of sale (POS) shifts: stand-alone and shared.</span></span> <span data-ttu-id="c5af3-108">スタンドアロンのシフトは、1 回に 1 人の作業者しか使用できません。</span><span class="sxs-lookup"><span data-stu-id="c5af3-108">Stand-alone shifts can be used by only one worker at a time.</span></span> <span data-ttu-id="c5af3-109">共有のシフトは、複数の場所で複数のユーザーによって使用可能です。</span><span class="sxs-lookup"><span data-stu-id="c5af3-109">Shared shifts can be used by multiple users in multiple places.</span></span> <span data-ttu-id="c5af3-110">したがって、店舗内の複数の作業者に 1 つのシフトを効果的に作成します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-110">Therefore, they effectively create a single shift for multiple workers in a store.</span></span>

## <a name="standalone-shifts"></a><span data-ttu-id="c5af3-111">スタンドアロン シフト</span><span class="sxs-lookup"><span data-stu-id="c5af3-111">Standalone shifts</span></span>
<span data-ttu-id="c5af3-112">スタンドアロン シフトは、POS レジスターごとに現金を個別に調整する従来の固定 POS シ ナリオにおいて使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-112">Stand-alone shifts are used in a traditional, fixed POS scenario, where cash is reconciled independently for each POS register.</span></span> <span data-ttu-id="c5af3-113">たとえば、食料品店での設定では、通常、いくつかの固定 POS レジスターがあり、レジ担当者が各レジスターに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="c5af3-113">For example, in a grocery store setting, there are typically several fixed POS registers, and a cashier is assigned to each register.</span></span> <span data-ttu-id="c5af3-114">この場合では、各レジスターはスタンドアロン シフトを使用する可能性があり、レジ担当者は、そのレジスターでレジまたは現金の取扱いを担当します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-114">In this case, each register likely uses a stand-alone shift, and the cashier is responsible for the till or physical cash at that register.</span></span> <span data-ttu-id="c5af3-115">スタンドアロン シフトには、レジ担当者の勤務シフトにおけるそのレジスターのすべてのアクティビティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c5af3-115">A stand-alone shift encompasses all the activity on that register during the cashier’s work shift.</span></span> <span data-ttu-id="c5af3-116">アクティビティには、レジに預金される開始金額、および銀行入金、釣銭入力、シフト終了時の支払/入金申告などの操作を含む現金削除および追加を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-116">Activities can include the opening amount that is deposited in the till, all removal and addition of cash through operations such as bank drops and float entry, and the tender declaration at the end of the shift.</span></span>

### <a name="set-up-a-stand-alone-shift"></a><span data-ttu-id="c5af3-117">スタンドアロン シフトの設定</span><span class="sxs-lookup"><span data-stu-id="c5af3-117">Set up a stand-alone shift</span></span>

<span data-ttu-id="c5af3-118">スタンドアロン シフトは、キャッシュ ドロワーのレベルで指定されます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-118">A stand-alone shift is designated at the cash drawer level.</span></span> <span data-ttu-id="c5af3-119">この手順では、POS レジスターのスタンドアロンのシフトを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-119">This procedure explains how to set up a stand-alone shift on a POS register.</span></span>

1.  <span data-ttu-id="c5af3-120">[**小売り**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS プロファイル**] &gt; [**ハードウェア プロファイル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-120">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="c5af3-121">スタンドアロンのシフトを使用するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-121">Select the hardware profile to use for the stand-alone shift.</span></span>
3.  <span data-ttu-id="c5af3-122">[**引き出し**] クイック タブで、[**共有シフトのドロワー**] オプションが [**いいえ**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-122">On the **Drawer** FastTab, confirm that the **Shared shift drawer** option is set to **No**.</span></span>
4.  <span data-ttu-id="c5af3-123">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-123">Click **Save**.</span></span>
5.  <span data-ttu-id="c5af3-124">[**小売**] &gt; [**チャネル設定**] &gt; [**POS 設定**] &gt; [**レジスター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-124">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="c5af3-125">スタンドアロンのシフトを必要とするレジスターを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-125">Select the register that requires a stand-alone shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="c5af3-126">[**ハードウェア プロファイル**] フィールドで、手順 2 で選択したハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-126">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="c5af3-127">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-127">Click **Save**.</span></span>
9.  <span data-ttu-id="c5af3-128">[**小売**] &gt; [**小売 IT**] &gt; [**配送スケジュール**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-128">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="c5af3-129">[**1090**] 配送スケジュールを選択して、[**今すぐ実行**] をクリックし、POS への変更を同期します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-129">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-stand-alone-shift"></a><span data-ttu-id="c5af3-130">スタンドアロン シフトの使用</span><span class="sxs-lookup"><span data-stu-id="c5af3-130">Use a stand-alone shift</span></span>

1.  <span data-ttu-id="c5af3-131">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="c5af3-131">Sign in to the POS.</span></span>
2.  <span data-ttu-id="c5af3-132">シフトが開いていない場合は、[**新しいシフトのオープン**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-132">If no shift is open, select **Open a new shift**.</span></span>
3.  <span data-ttu-id="c5af3-133">[**開始金額の申告**] 操作へ移動し、作業日を開始するのには、レジに追加されている現金の金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-133">Go to the **Declare start amount** operation, and specify the amount of cash that is being added to the till to start the work day.</span></span>
4.  <span data-ttu-id="c5af3-134">一部のトランザクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-134">Perform some transactions.</span></span>
5.  <span data-ttu-id="c5af3-135">1 日の最後に、[**支払/入金の申告**] を選択し、キャッシュ ドロワー内に残っている現金の金額を申告します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-135">At the end of the day, select **Declare tender** to declare the amount of cash that remains in the cash drawer.</span></span>
6.  <span data-ttu-id="c5af3-136">現金金額を入力した後、[**保存**] をクリックし、支払/入金申告を保存します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-136">Enter the amount of cash, and then click **Save** to save the tender declaration.</span></span>
7.  <span data-ttu-id="c5af3-137">[**シフトのクローズ**] を選択し、シフトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-137">Select **Close shift** to close the shift.</span></span>

<span data-ttu-id="c5af3-138">[**注記:**] 実行中のビジネス プロセスに応じて、他の操作はシフト中に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="c5af3-138">**Note:** Other operations are available during the shift, depending on the business processes that are in place.</span></span> <span data-ttu-id="c5af3-139">[**金庫保管**]、[**銀行入金**]、および [**支払/入金の削除**] 操作は、日中またはシフトを閉じる前に、レジからお金を削除するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-139">The **Safe drop**, **Bank drop**, and **Tender removal** operations can be used to remove money from the till during the day or before the shift is closed.</span></span> <span data-ttu-id="c5af3-140">レジの現金が不足している場合、[**釣銭入力**] 操作は、レジに現金を追加するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-140">If a till runs low on cash, the **Float entry** operation can be used to add cash to the till.</span></span>

## <a name="shared-shifts"></a><span data-ttu-id="c5af3-141">共有シフト</span><span class="sxs-lookup"><span data-stu-id="c5af3-141">Shared shifts</span></span>
<span data-ttu-id="c5af3-142">共有シフトは、複数のレジ担当者が現金の引き出しや作業日全体での現金引き出しのセットを共有する環境で使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-142">A shared shift is used in an environment where multiple cashiers share a cash drawer or a set of cash drawers throughout the work day.</span></span> <span data-ttu-id="c5af3-143">通常、共有シフトは、モバイル POS 環境で使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-143">Typically, a shared shift is used in mobile POS environments.</span></span> <span data-ttu-id="c5af3-144">モバイル環境では、各レジ担当者が、1 つの現金引き出しに割り当てられる、または担当することはありません。</span><span class="sxs-lookup"><span data-stu-id="c5af3-144">In a mobile environment, each cashier isn’t assigned to and responsible for a single cash drawer.</span></span> <span data-ttu-id="c5af3-145">代わりに、すべてのレジ担当者は、売上への支払/入金を行い、最も近いキャッシュ ドロワーに現金を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5af3-145">Instead, all cashiers must be able to tender a sale and add cash to whatever cash drawer is closest to them.</span></span> <span data-ttu-id="c5af3-146">このシナリオでは、レジ担当者間で共有されているキャッシュ ドロワーは共有シフトに含まれます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-146">In this scenario, the cash drawers that are shared among cashiers are included in a shared shift.</span></span> <span data-ttu-id="c5af3-147">共有シフトのすべてのキャッシュ ドロワーは、そのシフトの現金の管理に関連する活動の目的のために同じシフトに含まれます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-147">All the cash drawers in a shared shift are included in the same shift for the purpose of activities that are related to cash management for that shift.</span></span> <span data-ttu-id="c5af3-148">したがって、シフトの開始時の金額は、共有シフトに含まれているすべてのキャッシュ ドロワーの現金の合計に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5af3-148">Therefore, the starting amount for the shift should include the sum of all cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="c5af3-149">同様に、支払/入金申告も、共有シフトに含まれているすべてのキャッシュ ドロワーの現金の合計に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5af3-149">Likewise, the tender declaration will be the sum of all the cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="c5af3-150">**注記:** 一度に 1 つの共有シフトしか各店舗に開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="c5af3-150">**Note:** Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="c5af3-151">共有シフトとスタンドアロンのシフトは同じ店舗で使用できます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

### <a name="set-up-a-shared-shift"></a><span data-ttu-id="c5af3-152">共有シフトの設定</span><span class="sxs-lookup"><span data-stu-id="c5af3-152">Set up a shared shift</span></span>

1.  <span data-ttu-id="c5af3-153">[**小売り**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS プロファイル**] &gt; [**ハードウェア プロファイル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-153">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="c5af3-154">共有のシフトに対して使用するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-154">Select the hardware profile to use for the shared shift.</span></span>
3.  <span data-ttu-id="c5af3-155">[**ドロワー**] クイック タブで、[**共有シフトのドロワー**] オプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-155">On the **Drawer** FastTab, set the **Shared shift drawer** option to **Yes**.</span></span>
4.  <span data-ttu-id="c5af3-156">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-156">Click **Save**.</span></span>
5.  <span data-ttu-id="c5af3-157">[**小売**] &gt; [**チャネル設定**] &gt; [**POS 設定**] &gt; [**レジスター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-157">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="c5af3-158">共有のシフトを必要とするレジスターを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-158">Select the register that requires a shared shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="c5af3-159">[**ハードウェア プロファイル**] フィールドで、手順 2 で選択したハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-159">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="c5af3-160">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-160">Click **Save**.</span></span>
9.  <span data-ttu-id="c5af3-161">[**小売**] &gt; [**小売 IT**] &gt; [**配送スケジュール**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-161">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="c5af3-162">[**1090**] 配送スケジュールを選択して、[**今すぐ実行**] をクリックし、POS への変更を同期します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-162">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-shared-shift"></a><span data-ttu-id="c5af3-163">共有シフトの使用</span><span class="sxs-lookup"><span data-stu-id="c5af3-163">Use a shared shift</span></span>

1.  <span data-ttu-id="c5af3-164">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="c5af3-164">Sign in to the POS.</span></span>
2.  <span data-ttu-id="c5af3-165">POS がハードウェア ステーションにまだ接続されていない場合、[**非ドロワー操作**] を選択した後、[**ハードウェア ステーションの選択**] 操作を選択し、共有のシフトに対してハードウェア ステーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-165">If the POS isn’t yet connected to a hardware station, select **Non-drawer operation**, and then select the **Select hardware station** operation to make a hardware station active for the shared shift.</span></span> <span data-ttu-id="c5af3-166">この手順は、レジスターが共有シフト環境に初めて追加された時にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="c5af3-166">This step is required only the first time that a register is added to a shared shift environment.</span></span>
3.  <span data-ttu-id="c5af3-167">POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-167">Sign out of the POS, and then sign back in.</span></span>
4.  <span data-ttu-id="c5af3-168">[**新しいシフトの作成**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-168">Select **Create a new shift**.</span></span>
5.  <span data-ttu-id="c5af3-169">[**開始金額の申告**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-169">Select **Declare start amount**.</span></span>
6.  <span data-ttu-id="c5af3-170">共有シフトを使用している店舗のすべてのキャッシュ ドロワーの現金開始金を入力し、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-170">Enter the starting amount of all the cash drawers in the store that are part of the shared shift, and then click **Save**.</span></span>
    -   <span data-ttu-id="c5af3-171">開始金額の一部を各後続のキャッシュ ドロワー追加するには、[**ハードウェア ステーションの選択**] 操作を使用し、ハードウェア ステーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-171">To add part of the starting amount to each subsequent cash drawer, use the **Select hardware station** operation to make the hardware station active.</span></span>
    -   <span data-ttu-id="c5af3-172">レジを特定のキャッシュ ドロワーに追加するには、[**ドロワーを開く**] 操作を使用します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-172">To add a till to a specific cash drawer, use the **Open drawer** operation.</span></span>
    -   <span data-ttu-id="c5af3-173">共有シフトのすべてのキャッシュ ドロワーに開始時の金額の一部が入るまで続行します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-173">Continue until all cash drawers in the shared shift have their part of the starting amount.</span></span>

7.  <span data-ttu-id="c5af3-174">1 日の最後に、各キャッシュ ドロワーを開き、現金を削除します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-174">At the end of the day, open each cash drawer, and remove the cash.</span></span>
8.  <span data-ttu-id="c5af3-175">最後のキャッシュ ドロワーから現金を削除した後は、すべてのキャッシュ レジスターからのすべての現金をカウントします。</span><span class="sxs-lookup"><span data-stu-id="c5af3-175">After you’ve removed the cash from the last cash drawer, count all the cash from all the cash drawers.</span></span>
9.  <span data-ttu-id="c5af3-176">[**支払/入金の申告**] 操作を使用して、共有シフトに含まれるすべてのキャッシュ ドロワーの現金合計金額を申告します。</span><span class="sxs-lookup"><span data-stu-id="c5af3-176">Use the **Declare tender** operation to declare the total amount of cash from all the cash drawers that are included in the shared shift.</span></span>
10. <span data-ttu-id="c5af3-177">[**シフトのクローズ**] 操作を使用し、共有シフトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c5af3-177">Use the **Close shift** operation to close the shared shift.</span></span>





