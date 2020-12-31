---
title: リースの調整
description: このトピックでは、リースを調整する方法について説明します。 リースの条件が変更された場合、リースが拡張された場合、またはその他の状況が変化した場合は、調整が必要になることがあります。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445399"
---
# <a name="adjust-leases"></a><span data-ttu-id="7f340-104">リースの調整</span><span class="sxs-lookup"><span data-stu-id="7f340-104">Adjust leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f340-105">このトピックでは、リースを調整する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f340-105">The topic explains how to adjust a lease.</span></span> <span data-ttu-id="7f340-106">リースの条件が変更された場合、リースが拡張された場合、またはその他の状況が変化した場合は、調整が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="7f340-106">Adjustment might be required if the lease terms are modified, the lease is extended, or other circumstances change.</span></span> <span data-ttu-id="7f340-107">資産リースは、リースの変更に関する Accounting Standards Codification Topic 842 (ASC 842) および International Financial Reporting Standard 16 (IFRS 16) のガイダンスに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="7f340-107">Asset leasing complies with the guidance that Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16) provide about lease modifications.</span></span> <span data-ttu-id="7f340-108">ASC 842-20-15-1 では、リースの変更を、リースの範囲や対価に変更を生じさせる契約条件の変更と定義しています。</span><span class="sxs-lookup"><span data-stu-id="7f340-108">ASC 842-20-15-1 defines a lease modification as any change to the terms and conditions of a contract that causes a change in the scope of, or the consideration for, a lease.</span></span> <span data-ttu-id="7f340-109">IFRS 16 の パラグラフ 39 では、 賃借人はリース支払の変動を反映するようにリース負債を再評価する必要があることが示されています。</span><span class="sxs-lookup"><span data-stu-id="7f340-109">Paragraph 39 of IFRS 16 states that a lessee must revalue the lease liability so that it reflects changes to the lease payments.</span></span>

<span data-ttu-id="7f340-110">ASC 842 または IFRS 16 に準拠している組織については、リースは、将来のリース支払 (PVFMLP) の現在価値の変化を反映して再測定されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-110">For organizations that adhere to ASC 842 or IFRS 16, a lease is remeasured to reflect a change in the present value of the future minimum lease payments (PVFMLP).</span></span> <span data-ttu-id="7f340-111">PVFMLP が増加した場合、作成される仕訳入力は、使用権 (ROU) 資産の借方と、新規 PVFMLP と前の PVFMLP の差額に対するリース負債の貸方になります。</span><span class="sxs-lookup"><span data-stu-id="7f340-111">If the PVFMLP increases, the journal entry that is created will be a debit to the right-of-use (ROU) asset and a credit to the lease liability for the difference between the new PVFMLP and the previous PVFMLP.</span></span> <span data-ttu-id="7f340-112">PVFMLP が減少した場合、仕訳入力はリースの負債の借方になり、使用権資産に対する貸方となります。</span><span class="sxs-lookup"><span data-stu-id="7f340-112">If the PVFMLP decreases, the journal entry will be a debit to the lease liability and a credit to the ROU asset for the difference.</span></span>

<span data-ttu-id="7f340-113">調整で使用権資産の数が0 (ゼロ) を超えると、**リース転記勘定** ページで指定されている [リース変更の転記] 勘定の貸方に転記され ます。</span><span class="sxs-lookup"><span data-stu-id="7f340-113">If the adjustment decreases the ROU asset past 0 (zero), the remainder will be credited to the gain on lease modification posting account that is specified on the **Lease posting accounts** page.</span></span> <span data-ttu-id="7f340-114">このシステムでは、これら取引や、分類変更、初期直接原価、リースインセンティブ、前払い、リース変更に伴う解体費用などの調整項目を会計処理しています。</span><span class="sxs-lookup"><span data-stu-id="7f340-114">The system accounts for these transactions and other adjustment entries, such as classification changes, initial direct costs, lease incentives, prepayments, and dismantling costs that arise from lease modifications.</span></span>

<span data-ttu-id="7f340-115">リース調整トランザクションに関する具体的なガイダンスについては、IFRS 16 および ASC 842 を参照することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7f340-115">For specific guidance about lease adjustment transactions, we recommend that you see IFRS 16 and ASC 842.</span></span>

<span data-ttu-id="7f340-116">リースを調整するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7f340-116">To adjust a lease, follow these steps.</span></span> <span data-ttu-id="7f340-117">変更されたデータは、作成スケジュール プロセスの実行後にリース スケジュールを更新します。</span><span class="sxs-lookup"><span data-stu-id="7f340-117">The modified data will update lease schedules after the Create schedule process is run.</span></span>

1. <span data-ttu-id="7f340-118">**資産リース \> リース \> リース概要** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f340-118">Go to **Asset leasing \> Leases \> Lease summary**.</span></span>
2. <span data-ttu-id="7f340-119">**リースの概要** ページで、調整するリースを選択し、 **リースの調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f340-119">On the **Lease summary** page, select the lease to adjust, and then select **Adjust lease**.</span></span>
3. <span data-ttu-id="7f340-120">**リースの調整** ページで、調整されたリースの新しい情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f340-120">On the **Adjust lease** page, enter the new information for the adjusted lease.</span></span>

    <span data-ttu-id="7f340-121">リースの **調整** ページは **リースの追加** ページに似ている点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="7f340-121">Notice that the **Adjust lease** page resembles the **Add lease** page.</span></span> <span data-ttu-id="7f340-122">さらに、リースを追加するときに指定した開始日によって、新しいリースの開始時期が決まります。リースの調整を開始するタイミングは、**リースの調整** ページの **修正日** フィールドによって決まります。</span><span class="sxs-lookup"><span data-stu-id="7f340-122">Additionally, just as the commencement date that you specify when you add a lease determines when the new lease starts, the **Modification date** field on the **Adjust lease** page determines when the modified lease starts.</span></span> <span data-ttu-id="7f340-123">この日付は、支払スケジュール明細行の開始日より後の日付にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7f340-123">This date can't be after the start date on the payment schedule lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f340-124">**ROU 注意事項** のフィールドは、リースの調整に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-124">The **ROU considerations** fields apply to the lease adjustment.</span></span> <span data-ttu-id="7f340-125">リースの初期直接原価、リースのインセンティブ、前払、または解体費用の原価が、変更されたリースに関連付けられていない場合は、これらのフィールドを空白のままにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f340-125">If no initial direct costs, lease incentives, prepayments, or dismantling costs are associated with the modified lease, you should leave these fields blank.</span></span> <span data-ttu-id="7f340-126">元の金額は、更新されたリースには適用されません。</span><span class="sxs-lookup"><span data-stu-id="7f340-126">The original amounts won't apply to the updated lease.</span></span> <span data-ttu-id="7f340-127">リースを変更したときに発生する追加の費用は、**リースの調整** ページで入力する必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="7f340-127">Any additional costs that are incurred when the lease is modified should be entered on the **Adjust lease** page.</span></span>
    > 
    > <span data-ttu-id="7f340-128">たとえば、賃貸人は、リース拡張に同意する $1,000インセンティブを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f340-128">For example, a lessor provides a $1,000 incentive for agreeing to a lease extension.</span></span> <span data-ttu-id="7f340-129">拡張を考慮してリースを調整する場合は、 **リース インセンティブ** フィールドに **1,000** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f340-129">In this case, when you adjust the lease to account for the extension, you enter **1,000** in the **Lease incentives** field.</span></span> <span data-ttu-id="7f340-130">リースの調整に報奨が関連付けられていない場合は、このフィールドに以前に入力されたすべての値をクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f340-130">If no incentives are associated with the lease adjustment, you should clear any value that was previously entered in this field.</span></span> <span data-ttu-id="7f340-131">同じロジックが、他の使用権の考慮事項にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-131">The same logic is applied to other ROU considerations.</span></span>

    <span data-ttu-id="7f340-132">調整されたリースの支払スケジュール行は、見込みベースで作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f340-132">The payment schedule lines of the adjusted lease should be created on a prospective basis.</span></span> <span data-ttu-id="7f340-133">見込みに基づいて作成された支払スケジュール明細行は、リースの変更を有効にする前に開始できません。</span><span class="sxs-lookup"><span data-stu-id="7f340-133">Payment schedule lines that are created on a prospective basis can't start before the lease modifications take effect.</span></span>

    <span data-ttu-id="7f340-134">次の手順は、リースを当初認識する手順とほとんど同じです。</span><span class="sxs-lookup"><span data-stu-id="7f340-134">The following steps are almost identical to the steps for initially recognizing a lease.</span></span>

4. <span data-ttu-id="7f340-135">**スケジュール作成** を選択し、調整された支払スケジュールを生成します。</span><span class="sxs-lookup"><span data-stu-id="7f340-135">Select **Create schedules** to generate the adjusted payment schedule.</span></span> <span data-ttu-id="7f340-136">リースに対する支払スケジュールが作成されたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-136">You receive a message that states that the payment schedule has been created for the lease.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7f340-137">**スケジュールの作成** を選択する前に 、変更日と支払スケジュールの明細行が正確であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7f340-137">Before you select **Create schedules**, make sure that the modification date and payment schedule lines are accurate.</span></span> <span data-ttu-id="7f340-138">また、初期直接原価、リースインセンティブ、前払い、解体費用はすべて、調整から発生する費用のみに対応していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7f340-138">Also make sure that all initial direct costs, lease incentives, prepayments, or dismantling costs correspond only to those costs that arise from the adjustment.</span></span>

5. <span data-ttu-id="7f340-139">新たに作成された支払スケジュールを表示するには、**帳簿** を選択し、**支払スケジュール** ページを開き ます。</span><span class="sxs-lookup"><span data-stu-id="7f340-139">To view the newly created payment schedule, select **Books**, and open the **Payment schedule** page.</span></span>
6. <span data-ttu-id="7f340-140">**支払スケジュール** ページで、支払スケジュールを確認する前に、調整された支払金額を編集できます。</span><span class="sxs-lookup"><span data-stu-id="7f340-140">On the **Payment schedule** page, you can edit the adjusted payment amounts before you confirm the payment schedule.</span></span> <span data-ttu-id="7f340-141">スケジュールを確認するには、**スケジュールの確認** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="7f340-141">To confirm the schedule, select **Confirm schedule**.</span></span>

    <span data-ttu-id="7f340-142">支払スケジュールが確定すると、新たな資産減価償却スケジュールと新たなリース債務スケジュールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-142">When the payment schedule is confirmed, the new asset depreciation and new lease liability schedules are created.</span></span>

7. <span data-ttu-id="7f340-143">新しい入力から生成された新しいリース負債の償却スケジュールを表示するには、**支払スケジュール** ページを閉じ、**負債償却スケジュール** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f340-143">To view the new lease liability amortization schedule that is generated from the new inputs, close the **Payment schedule** page, and open the **Liability amortization schedule** page.</span></span>
8. <span data-ttu-id="7f340-144">新たに生成された資産の減価償却スケジュールを表示するには、**帳簿の詳細** ページから **資産減価償却スケジュール**  ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f340-144">To view the newly generated asset depreciation schedule, open the **Asset depreciation schedule** page from the **Book details** page.</span></span>
9. <span data-ttu-id="7f340-145">調整仕訳入力を生成するには、**機能 \> リースの調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f340-145">To generate the adjustment journal entry, select **Function \> Lease adjustment**.</span></span> <span data-ttu-id="7f340-146">調整仕訳入力が作成されたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-146">You receive a message that states that the adjustment journal entry has been created.</span></span> 
10. <span data-ttu-id="7f340-147">仕訳入力を表示するには、**仕訳帳 \> 資産リース仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f340-147">To view the journal entry, select **Journals \> Asset leasing journal**.</span></span>
11. <span data-ttu-id="7f340-148">仕訳帳入力を転記するには、明細行を選択し、**転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f340-148">To post the journal entry, select the line, and then select **Post**.</span></span>

## <a name="view-lease-versions"></a><span data-ttu-id="7f340-149">リース バージョンの表示</span><span class="sxs-lookup"><span data-stu-id="7f340-149">View lease versions</span></span>

<span data-ttu-id="7f340-150">リースが変更されている場合は、異なるバージョンを表示できます。</span><span class="sxs-lookup"><span data-stu-id="7f340-150">If a lease has been modified, you can view the different versions of it.</span></span> <span data-ttu-id="7f340-151">履歴スケジュールと過去のリースの詳細を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="7f340-151">You can also view the historical schedules and past lease details.</span></span>

1. <span data-ttu-id="7f340-152">**リースの概要** ページで、コピーするリースを選択し、[アクション] ウィンドウで **リースのバージョン履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f340-152">On the **Lease summary** page, select the lease, and then, on the Action Pane, select **Lease version history**.</span></span>

    <span data-ttu-id="7f340-153">選択したリースが調整されている場合、**リースのバージョン履歴** ページには、それと異なるバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-153">If the selected lease has been adjusted, the **Lease version history** page shows the different versions of it.</span></span> <span data-ttu-id="7f340-154">元のリースには **1** というラベルが付けられ、後続のバージョンに連番が付番されます。</span><span class="sxs-lookup"><span data-stu-id="7f340-154">The original lease is labeled **1**, and subsequent versions have ascending numerical order.</span></span>

    <span data-ttu-id="7f340-155">選択したリース バージョンに対して、財務分析コード、契約の詳細、場所、および支払スケジュール明細行を表示できます。</span><span class="sxs-lookup"><span data-stu-id="7f340-155">For a selected lease version, you can view the financial dimensions, contract details, location, and payment schedule lines.</span></span>

2. <span data-ttu-id="7f340-156">履歴スケジュールを表示するには、**リースの概要** ページで変更したリースを開き 、目的の帳簿を選択して、アクション ウィンドウで **帳簿バージョン履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f340-156">To view historical schedules, open the modified lease from the **Lease summary** page, select the desired book, and then, on the Action Pane, select **Book version history**.</span></span>
3. <span data-ttu-id="7f340-157">**帳簿バージョン** ページで、目的のバージョンと表示する必要なスケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f340-157">On the **Book version** page, select the desired version and the desired schedule to view.</span></span>
