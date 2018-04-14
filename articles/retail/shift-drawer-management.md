---
title: "シフトとキャッシュ ドロワーの管理"
description: "この記事では、小売販売時点管理 (POS) シフトにおける 2 つのタイプの設定および使用方法について説明します - 共有およびスタンドアロン。 共有シフトは、複数の場所で複数のユーザーにより使用できますが、スタンドアロン シフトは、一度に 1 人の作業者しか使用できません。"
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4b39fafb7fb51ee26bd45fb28ce4b505a91de813
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="f3e4e-104">シフトとキャッシュ ドロワーの管理</span><span class="sxs-lookup"><span data-stu-id="f3e4e-104">Shift and cash drawer management</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="f3e4e-105">この記事では、小売販売時点管理 (POS) シフトにおける 2 つのタイプの設定および使用方法について説明します - 共有およびスタンドアロン。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-105">This article explains how to set up and use the two types of retail point of sale (POS) shifts -  shared and stand-alone.</span></span> <span data-ttu-id="f3e4e-106">共有シフトは、複数の場所で複数のユーザーにより使用できますが、スタンドアロン シフトは、一度に 1 人の作業者しか使用できません。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-106">Shared shifts can be used by multiple users in multiple places, whereas stand-alone shifts can be used by only one worker at a time.</span></span>

<span data-ttu-id="f3e4e-107">販売時点管理 (POS) シフトには 2 種類あります: スタンドアロンと共有です。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-107">There are two types of retail point of sale (POS) shifts: stand-alone and shared.</span></span> <span data-ttu-id="f3e4e-108">スタンドアロンのシフトは、1 回に 1 人の作業者しか使用できません。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-108">Stand-alone shifts can be used by only one worker at a time.</span></span> <span data-ttu-id="f3e4e-109">共有のシフトは、複数の場所で複数のユーザーによって使用可能です。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-109">Shared shifts can be used by multiple users in multiple places.</span></span> <span data-ttu-id="f3e4e-110">したがって、店舗内の複数の作業者に 1 つのシフトを効果的に作成します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-110">Therefore, they effectively create a single shift for multiple workers in a store.</span></span>

## <a name="standalone-shifts"></a><span data-ttu-id="f3e4e-111">スタンドアロン シフト</span><span class="sxs-lookup"><span data-stu-id="f3e4e-111">Standalone shifts</span></span>
<span data-ttu-id="f3e4e-112">スタンドアロン シフトは、POS レジスターごとに現金を個別に調整する従来の固定 POS シ ナリオにおいて使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-112">Stand-alone shifts are used in a traditional, fixed POS scenario, where cash is reconciled independently for each POS register.</span></span> <span data-ttu-id="f3e4e-113">たとえば、食料品店での設定では、通常、いくつかの固定 POS レジスターがあり、レジ担当者が各レジスターに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-113">For example, in a grocery store setting, there are typically several fixed POS registers, and a cashier is assigned to each register.</span></span> <span data-ttu-id="f3e4e-114">この場合では、各レジスターはスタンドアロン シフトを使用する可能性があり、レジ担当者は、そのレジスターでレジまたは現金の取扱いを担当します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-114">In this case, each register likely uses a stand-alone shift, and the cashier is responsible for the till or physical cash at that register.</span></span> <span data-ttu-id="f3e4e-115">スタンドアロン シフトには、レジ担当者の勤務シフトにおけるそのレジスターのすべてのアクティビティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-115">A stand-alone shift encompasses all the activity on that register during the cashier’s work shift.</span></span> <span data-ttu-id="f3e4e-116">アクティビティには、レジに預金される開始金額、および銀行入金、釣銭入力、シフト終了時の支払/入金申告などの操作を含む現金削除および追加を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-116">Activities can include the opening amount that is deposited in the till, all removal and addition of cash through operations such as bank drops and float entry, and the tender declaration at the end of the shift.</span></span>

### <a name="set-up-a-stand-alone-shift"></a><span data-ttu-id="f3e4e-117">スタンドアロン シフトの設定</span><span class="sxs-lookup"><span data-stu-id="f3e4e-117">Set up a stand-alone shift</span></span>

<span data-ttu-id="f3e4e-118">スタンドアロン シフトは、キャッシュ ドロワーのレベルで指定されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-118">A stand-alone shift is designated at the cash drawer level.</span></span> <span data-ttu-id="f3e4e-119">この手順では、POS レジスターのスタンドアロンのシフトを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-119">This procedure explains how to set up a stand-alone shift on a POS register.</span></span>

1.  <span data-ttu-id="f3e4e-120">[**小売り**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS プロファイル**] &gt; [**ハードウェア プロファイル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-120">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="f3e4e-121">スタンドアロンのシフトを使用するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-121">Select the hardware profile to use for the stand-alone shift.</span></span>
3.  <span data-ttu-id="f3e4e-122">[**引き出し**] クイック タブで、[**共有シフトのドロワー**] オプションが [**いいえ**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-122">On the **Drawer** FastTab, confirm that the **Shared shift drawer** option is set to **No**.</span></span>
4.  <span data-ttu-id="f3e4e-123">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-123">Click **Save**.</span></span>
5.  <span data-ttu-id="f3e4e-124">[**小売**] &gt; [**チャネル設定**] &gt; [**POS 設定**] &gt; [**レジスター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-124">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="f3e4e-125">スタンドアロンのシフトを必要とするレジスターを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-125">Select the register that requires a stand-alone shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="f3e4e-126">[**ハードウェア プロファイル**] フィールドで、手順 2 で選択したハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-126">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="f3e4e-127">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-127">Click **Save**.</span></span>
9.  <span data-ttu-id="f3e4e-128">[**小売**] &gt; [**小売 IT**] &gt; [**配送スケジュール**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-128">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="f3e4e-129">[**1090**] 配送スケジュールを選択して、[**今すぐ実行**] をクリックし、POS への変更を同期します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-129">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-stand-alone-shift"></a><span data-ttu-id="f3e4e-130">スタンドアロン シフトの使用</span><span class="sxs-lookup"><span data-stu-id="f3e4e-130">Use a stand-alone shift</span></span>

1.  <span data-ttu-id="f3e4e-131">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="f3e4e-131">Sign in to the POS.</span></span>
2.  <span data-ttu-id="f3e4e-132">シフトが開いていない場合は、[**新しいシフトのオープン**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-132">If no shift is open, select **Open a new shift**.</span></span>
3.  <span data-ttu-id="f3e4e-133">[**開始金額の申告**] 操作へ移動し、作業日を開始するのには、レジに追加されている現金の金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-133">Go to the **Declare start amount** operation, and specify the amount of cash that is being added to the till to start the work day.</span></span>
4.  <span data-ttu-id="f3e4e-134">一部のトランザクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-134">Perform some transactions.</span></span>
5.  <span data-ttu-id="f3e4e-135">1 日の最後に、[**支払/入金の申告**] を選択し、キャッシュ ドロワー内に残っている現金の金額を申告します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-135">At the end of the day, select **Declare tender** to declare the amount of cash that remains in the cash drawer.</span></span>
6.  <span data-ttu-id="f3e4e-136">現金金額を入力した後、[**保存**] をクリックし、支払/入金申告を保存します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-136">Enter the amount of cash, and then click **Save** to save the tender declaration.</span></span>
7.  <span data-ttu-id="f3e4e-137">[**シフトのクローズ**] を選択し、シフトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-137">Select **Close shift** to close the shift.</span></span>

<span data-ttu-id="f3e4e-138">[**注記:**] 実行中のビジネス プロセスに応じて、他の操作はシフト中に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-138">**Note:** Other operations are available during the shift, depending on the business processes that are in place.</span></span> <span data-ttu-id="f3e4e-139">[**金庫保管**]、[**銀行入金**]、および [**支払/入金の削除**] 操作は、日中またはシフトを閉じる前に、レジからお金を削除するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-139">The **Safe drop**, **Bank drop**, and **Tender removal** operations can be used to remove money from the till during the day or before the shift is closed.</span></span> <span data-ttu-id="f3e4e-140">レジの現金が不足している場合、[**釣銭入力**] 操作は、レジに現金を追加するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-140">If a till runs low on cash, the **Float entry** operation can be used to add cash to the till.</span></span>

## <a name="shared-shifts"></a><span data-ttu-id="f3e4e-141">共有シフト</span><span class="sxs-lookup"><span data-stu-id="f3e4e-141">Shared shifts</span></span>
<span data-ttu-id="f3e4e-142">共有シフトは、複数のレジ担当者が現金の引き出しや作業日全体での現金引き出しのセットを共有する環境で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-142">A shared shift is used in an environment where multiple cashiers share a cash drawer or a set of cash drawers throughout the work day.</span></span> <span data-ttu-id="f3e4e-143">通常、共有シフトは、モバイル POS 環境で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-143">Typically, a shared shift is used in mobile POS environments.</span></span> <span data-ttu-id="f3e4e-144">モバイル環境では、各レジ担当者が、1 つの現金引き出しに割り当てられる、または担当することはありません。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-144">In a mobile environment, each cashier isn’t assigned to and responsible for a single cash drawer.</span></span> <span data-ttu-id="f3e4e-145">代わりに、すべてのレジ担当者は、売上への支払/入金を行い、最も近いキャッシュ ドロワーに現金を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-145">Instead, all cashiers must be able to tender a sale and add cash to whatever cash drawer is closest to them.</span></span> <span data-ttu-id="f3e4e-146">このシナリオでは、レジ担当者間で共有されているキャッシュ ドロワーは共有シフトに含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-146">In this scenario, the cash drawers that are shared among cashiers are included in a shared shift.</span></span> <span data-ttu-id="f3e4e-147">共有シフトのすべてのキャッシュ ドロワーは、そのシフトの現金の管理に関連する活動の目的のために同じシフトに含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-147">All the cash drawers in a shared shift are included in the same shift for the purpose of activities that are related to cash management for that shift.</span></span> <span data-ttu-id="f3e4e-148">したがって、シフトの開始時の金額は、共有シフトに含まれているすべてのキャッシュ ドロワーの現金の合計に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-148">Therefore, the starting amount for the shift should include the sum of all cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="f3e4e-149">同様に、支払/入金申告も、共有シフトに含まれているすべてのキャッシュ ドロワーの現金の合計に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-149">Likewise, the tender declaration will be the sum of all the cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="f3e4e-150">**注記:** 一度に 1 つの共有シフトしか各店舗に開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-150">**Note:** Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="f3e4e-151">共有シフトとスタンドアロンのシフトは同じ店舗で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

### <a name="set-up-a-shared-shift"></a><span data-ttu-id="f3e4e-152">共有シフトの設定</span><span class="sxs-lookup"><span data-stu-id="f3e4e-152">Set up a shared shift</span></span>

1.  <span data-ttu-id="f3e4e-153">[**小売り**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS プロファイル**] &gt; [**ハードウェア プロファイル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-153">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="f3e4e-154">共有のシフトに対して使用するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-154">Select the hardware profile to use for the shared shift.</span></span>
3.  <span data-ttu-id="f3e4e-155">[**ドロワー**] クイック タブで、[**共有シフトのドロワー**] オプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-155">On the **Drawer** FastTab, set the **Shared shift drawer** option to **Yes**.</span></span>
4.  <span data-ttu-id="f3e4e-156">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-156">Click **Save**.</span></span>
5.  <span data-ttu-id="f3e4e-157">[**小売**] &gt; [**チャネル設定**] &gt; [**POS 設定**] &gt; [**レジスター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-157">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="f3e4e-158">共有のシフトを必要とするレジスターを選択し、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-158">Select the register that requires a shared shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="f3e4e-159">[**ハードウェア プロファイル**] フィールドで、手順 2 で選択したハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-159">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="f3e4e-160">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-160">Click **Save**.</span></span>
9.  <span data-ttu-id="f3e4e-161">[**小売**] &gt; [**小売 IT**] &gt; [**配送スケジュール**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-161">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="f3e4e-162">[**1090**] 配送スケジュールを選択して、[**今すぐ実行**] をクリックし、POS への変更を同期します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-162">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-shared-shift"></a><span data-ttu-id="f3e4e-163">共有シフトの使用</span><span class="sxs-lookup"><span data-stu-id="f3e4e-163">Use a shared shift</span></span>

1.  <span data-ttu-id="f3e4e-164">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="f3e4e-164">Sign in to the POS.</span></span>
2.  <span data-ttu-id="f3e4e-165">POS がハードウェア ステーションにまだ接続されていない場合、[**非ドロワー操作**] を選択した後、[**ハードウェア ステーションの選択**] 操作を選択し、共有のシフトに対してハードウェア ステーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-165">If the POS isn’t yet connected to a hardware station, select **Non-drawer operation**, and then select the **Select hardware station** operation to make a hardware station active for the shared shift.</span></span> <span data-ttu-id="f3e4e-166">この手順は、レジスターが共有シフト環境に初めて追加された時にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-166">This step is required only the first time that a register is added to a shared shift environment.</span></span>
3.  <span data-ttu-id="f3e4e-167">POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-167">Sign out of the POS, and then sign back in.</span></span>
4.  <span data-ttu-id="f3e4e-168">[**新しいシフトの作成**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-168">Select **Create a new shift**.</span></span>
5.  <span data-ttu-id="f3e4e-169">[**開始金額の申告**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-169">Select **Declare start amount**.</span></span>
6.  <span data-ttu-id="f3e4e-170">共有シフトを使用している店舗のすべてのキャッシュ ドロワーの現金開始金を入力し、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-170">Enter the starting amount of all the cash drawers in the store that are part of the shared shift, and then click **Save**.</span></span>
    -   <span data-ttu-id="f3e4e-171">開始金額の一部を各後続のキャッシュ ドロワー追加するには、[**ハードウェア ステーションの選択**] 操作を使用し、ハードウェア ステーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-171">To add part of the starting amount to each subsequent cash drawer, use the **Select hardware station** operation to make the hardware station active.</span></span>
    -   <span data-ttu-id="f3e4e-172">レジを特定のキャッシュ ドロワーに追加するには、[**ドロワーを開く**] 操作を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-172">To add a till to a specific cash drawer, use the **Open drawer** operation.</span></span>
    -   <span data-ttu-id="f3e4e-173">共有シフトのすべてのキャッシュ ドロワーに開始時の金額の一部が入るまで続行します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-173">Continue until all cash drawers in the shared shift have their part of the starting amount.</span></span>

7.  <span data-ttu-id="f3e4e-174">1 日の最後に、各キャッシュ ドロワーを開き、現金を削除します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-174">At the end of the day, open each cash drawer, and remove the cash.</span></span>
8.  <span data-ttu-id="f3e4e-175">最後のキャッシュ ドロワーから現金を削除した後は、すべてのキャッシュ レジスターからのすべての現金をカウントします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-175">After you’ve removed the cash from the last cash drawer, count all the cash from all the cash drawers.</span></span>
9.  <span data-ttu-id="f3e4e-176">[**支払/入金の申告**] 操作を使用して、共有シフトに含まれるすべてのキャッシュ ドロワーの現金合計金額を申告します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-176">Use the **Declare tender** operation to declare the total amount of cash from all the cash drawers that are included in the shared shift.</span></span>
10. <span data-ttu-id="f3e4e-177">[**シフトのクローズ**] 操作を使用し、共有シフトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-177">Use the **Close shift** operation to close the shared shift.</span></span>

## <a name="shift-operations"></a><span data-ttu-id="f3e4e-178">シフト操作</span><span class="sxs-lookup"><span data-stu-id="f3e4e-178">Shift operations</span></span>
<span data-ttu-id="f3e4e-179">さまざまなアクションによってシフトの状態を変更、またはドロワーの合計金額を増減することができます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-179">Various actions can be taken to change the state of a shift or to increase or decrease the amount of money in the drawer.</span></span> <span data-ttu-id="f3e4e-180">以下のセクションでは、Retail Modern POS およびクラウド POS に対する Dynamics 365 のこれらのシフト操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-180">The section below describes these shift operations for Dynamics 365 for Retail Modern POS and Cloud POS.</span></span>

<span data-ttu-id="f3e4e-181">**オープン シフト**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-181">**Open shift**</span></span>

<span data-ttu-id="f3e4e-182">POSでは、販売、返品、顧客注文などの財務トランザクションにつながる操作を実行するために、ユーザーが有効で開かれたシフトを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-182">POS requires that a user has an active, open shift to perform any operations that would result in a financial transaction such as a sale, return, or customer order.</span></span>  

<span data-ttu-id="f3e4e-183">POS にログインすると、システムは最初に、ユーザーが現在のレジスターに使用可能な有効なシフトを持っているかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-183">When logging into the POS, the system first checks to see if the user has an active shift available on the current register.</span></span> <span data-ttu-id="f3e4e-184">そうでない場合、システム コンフィギュレーションおよびそのアクセス許可に応じて、ユーザーは新しいシフトを開き、既存のシフトを再開し、または「ドロワー以外」モードでログインし続ける選択ができます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-184">If not, the user can then choose to open a new shift, resume an existing shift, or continue to login in “non-drawer” mode, depending on the system configuration and their permissions.</span></span>

<span data-ttu-id="f3e4e-185">**開始金額の申告**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-185">**Declare start amount**</span></span>

<span data-ttu-id="f3e4e-186">多くの場合、この操作は新しく開いたシフトを取得する最初のアクションになります。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-186">This operation is often the first action that is taken a newly opened shift.</span></span> <span data-ttu-id="f3e4e-187">ユーザは、シフトのドロワーに現金の開始金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-187">Users specify the starting cash amount in the drawer for the shift.</span></span> <span data-ttu-id="f3e4e-188">これは、シフトを終了するときに発生する超過/不足計算がこの合計量になるため重要です。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-188">This is important because the over/short calculation that occurs when closing a shift accounts for this amount.</span></span>

<span data-ttu-id="f3e4e-189">**釣銭入力**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-189">**Float entry**</span></span>

<span data-ttu-id="f3e4e-190">釣銭入力は、有効なシフトで実行される販売以外のトランザクションであり、ドロワー内の現金の金額を増やします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-190">Float entries are non-sales transactions that are performed in an active shift and they increase the amount of the cash in the drawer.</span></span> <span data-ttu-id="f3e4e-191">釣銭入力の一般的な例は、ドロワーが少ない場合にドロワーに追加の変更を加えることです。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-191">A common example of a float entry would be to add additional change to the drawer when it is running low.</span></span>

<span data-ttu-id="f3e4e-192">**支払/入金の削除**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-192">**Tender removal**</span></span>

<span data-ttu-id="f3e4e-193">支払/入金の削除は、ドロワー内の現金金額を減らすために有効なシフトで実行される販売以外のトランザクションです。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-193">Tender removals are non-sales transactions that are performed in an active shift to reduce the amount of the cash in the drawer.</span></span> <span data-ttu-id="f3e4e-194">これは、異なるシフトの釣銭入力と組み合わせて最もよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-194">This is most commonly used in conjunction with a float entry on a different shift.</span></span> <span data-ttu-id="f3e4e-195">たとえば、レジスター 1 は変化が少ないため、レジスター 2 のユーザーがドロワー金額を削減するための支払/入金の削除を実行します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-195">For example, Register 1 is running low on change, so the user on Register 2 performs a tender removal to reduce the drawer amount.</span></span> <span data-ttu-id="f3e4e-196">そして、レジスター 1 のユーザは釣銭入力を行い金額を増加させます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-196">The user on Register 1 would then perform a float entry to increase their amount.</span></span>

<span data-ttu-id="f3e4e-197">**シフトの中断**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-197">**Suspend shift**</span></span>

<span data-ttu-id="f3e4e-198">ユーザーは、有効なシフトを中断して、別のユーザーの現在の登録を解放したり、別の登録にシフトを移すことができます (これは多くの場合「フローティング レジ」と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-198">Users can suspend their active shift to free up the current register for another user, or to move their shift to a different register (this is often referred to as a “floating till”).</span></span> 

<span data-ttu-id="f3e4e-199">シフトを中断すると、再開されるまで、新しいトランザクションやシフトの変更が防止されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-199">Suspending the shift prevents any new transactions or changes to the shift until it resumed.</span></span>

<span data-ttu-id="f3e4e-200">**シフトの再開**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-200">**Resume shift**</span></span>

<span data-ttu-id="f3e4e-201">この操作により、ユーザは、有効なシフトをまだ持っていないレジスターで以前に中断したシフトを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-201">This operation allows a user to resume a previously suspended shift on a register that does not already have an active shift.</span></span>

<span data-ttu-id="f3e4e-202">**支払/入金申告**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-202">**Tender declaration**</span></span>

<span data-ttu-id="f3e4e-203">支払/入金申告は、ユーザーが現時点でドロワー内にある現金の総額を指定するための、ほとんどの場合、シフトを終了する前に行うアクションです。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-203">The tender declaration is action the user takes to specify the amount of total money currently in the drawer, most often before closing the shift.</span></span> <span data-ttu-id="f3e4e-204">これは、超過/不足金額を計算するために予想されるシフトと比較される値です。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-204">This is the value that is compared against the expected shift to calculate the over/short amount.</span></span>

<span data-ttu-id="f3e4e-205">**金庫保管**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-205">**Safe drop**</span></span>

<span data-ttu-id="f3e4e-206">金庫保管は有効なシフトでいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-206">Safe drops can be performed at any time on an active shift.</span></span> <span data-ttu-id="f3e4e-207">この操作はドロワーから金銭を取り出すので、奥の部屋の金庫など、より安全な場所に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-207">This operation removes money from the drawer, so it can be transferred to a more secure location such as a safe in the back room.</span></span> <span data-ttu-id="f3e4e-208">金庫保管に記録された合計金額は依然としてシフト合計に含まれますが、支払/入金申告の一部としてカウントする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-208">The total amount recorded for safe drops is still included in the shift totals, but doesn't need to be counted as part of the tender declaration.</span></span>

<span data-ttu-id="f3e4e-209">**銀行入金**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-209">**Bank drop**</span></span>

<span data-ttu-id="f3e4e-210">金庫保管のように、銀行入金は有効なシフトでも実行されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-210">Like safe drops, bank drops are also performed on active shifts.</span></span> <span data-ttu-id="f3e4e-211">この操作により、シフトからの金銭が取り出され、銀行預金の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-211">This operation removes money from the shift to prepare for the bank deposit.</span></span>

<span data-ttu-id="f3e4e-212">**シフトのブラインド クローズ**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-212">**Blind close shift**</span></span>

<span data-ttu-id="f3e4e-213">ブラインド クローズされたシフトは、有効ではなくなったが、完全に終了していないシフトです。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-213">A blind closed shift is a shift that is no longer active but has not been fully closed.</span></span> <span data-ttu-id="f3e4e-214">ブラインド クローズ済シフトは、中断されたシフトのように再開することはできませんが、開始金額の申告と支払/入金申告などの手順は、後で実行することも、または別のレジスターから実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-214">Blind closed shifts can't be resumed like a suspended shift, but procedures such as declare staring amounts and tender declarations can be performed at a later time or from a different register.</span></span>

<span data-ttu-id="f3e4e-215">ブラインド クローズ済シフトは、最初にこのシフトを完全にカウントし、調整し、閉じる必要がないため、新しいユーザーまたはシフトのためにレジスター解放するためによく使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-215">Blind closed shifts are often used to free up a register for a new user or shift, without having to fully count, reconcile, and close this shift first.</span></span> 

<span data-ttu-id="f3e4e-216">**シフトのクローズ**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-216">**Close shift**</span></span>

<span data-ttu-id="f3e4e-217">この操作では、シフト合計、超過/不足金額が計算され、有効またはブラインド クローズされたシフトを完了します。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-217">This operation calculates shift totals, over/short amounts, and then finalizes an active or blind closed shift.</span></span> <span data-ttu-id="f3e4e-218">クローズされたシフトを再開または変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-218">Closed shifts cannot be resumed or modified.</span></span>  

<span data-ttu-id="f3e4e-219">**シフトを管理する**</span><span class="sxs-lookup"><span data-stu-id="f3e4e-219">**Manage shifts**</span></span>

<span data-ttu-id="f3e4e-220">この操作により、ユーザーはストアのすべての有効、中断、およびブラインド クローズされたシフトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-220">This operation allows users to view all active, suspended, and blind closed shifts for the store.</span></span> <span data-ttu-id="f3e4e-221">アクセス許可に応じて、ユーザーは支払/入金申告などの最終決算手続きを実行し、ブラインド クローズ済シフトのシフトをクローズします。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-221">Depending on their permissions, users can perform their final closing procedures such as tender declaration and close shifts for blind closed shifts.</span></span> <span data-ttu-id="f3e4e-222">この操作では、オフライン モードとオンライン モードの切り替え後にシフトが不適切な状態のままになっているまれなイベントの際に、無効なシフトを表示および削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-222">This operation will also allow users to view and delete invalid shifts in the rare event that a shift is left in a bad state after switching between offline and online modes.</span></span> <span data-ttu-id="f3e4e-223">これらの無効なシフトには、調整に必要な財務情報またはトランザクション データは含まれません。</span><span class="sxs-lookup"><span data-stu-id="f3e4e-223">These invalid shifts do not contain any financial information or transactional data needed for reconciliation.</span></span> 

