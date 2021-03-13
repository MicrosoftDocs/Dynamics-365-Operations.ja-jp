---
title: 指標金利にリンクされたリース支払の再評価
description: このトピックでは、指標金利の変更によって変動リース支払が変更された場合に、使用権 (ROU) 資産に対するリース負債の調整について説明します。
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2cbe54ad92aff2f8a85e47301635fe4b6819e9a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012064"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a><span data-ttu-id="e5fd3-103">指標金利にリンクされたリース支払の再評価</span><span class="sxs-lookup"><span data-stu-id="e5fd3-103">Revalue lease payments that are linked to an index rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5fd3-104">このトピックでは、指標金利の変更によって変動リース支払が変更された場合に、使用権 (ROU) 資産に対するリース負債の調整について説明します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-104">This topic describes the adjustment that is made to the lease liability for a right-of-use (ROU) asset when variable lease payments change because of a change in the index rate.</span></span> <span data-ttu-id="e5fd3-105">リース負債と使用権 (ROU) 資産は、新しい支払額を考慮して調整されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-105">The lease liability and ROU asset will be adjusted to account for the new payment amounts.</span></span> <span data-ttu-id="e5fd3-106">米国で一般的に認められた会計原則 (米国 GAAP) の標準である Accounting Standards Codification Topic 842 (ASC 842) に基づいて、キャッシュ フローに追加変更があった場合を除き、指標金利の変更が原因で支払が増加または減少した場合にのみ変動支払のみが変更されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-106">Under Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), only the variable payments change when payments increase or decrease because of a change in the index rate, unless there are additional changes to cash flows.</span></span> <span data-ttu-id="e5fd3-107">これらの追加変更には、金利に関連するリース期間の変更が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-107">These additional changes might include a change in lease terms that is related to interest rates.</span></span> <span data-ttu-id="e5fd3-108">詳細については、国際会計基準16 (IFRS 16) の ASC 842-10-55-225 と 42 (b) 段落を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-108">For more information, see ASC 842-10-55-225 and paragraph 42(b) of International Financial Reporting Standard 16 (IFRS 16).</span></span>

## <a name="adjust-lease-payments"></a><span data-ttu-id="e5fd3-109">リース支払の調整</span><span class="sxs-lookup"><span data-stu-id="e5fd3-109">Adjust lease payments</span></span>

<span data-ttu-id="e5fd3-110">以下の手順に従って、指標金利にリンクされたリース支払を再評価します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-110">Follow these steps to revalue lease payments that are linked to an index rate.</span></span>

1. <span data-ttu-id="e5fd3-111">リース指標の再評価プロセスを実行するには、**資産リース \> 定期 \> 指標金利の再評価** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-111">To run the lease index revaluation process, go to **Asset leasing \> Periodic \> Index rate revaluation**.</span></span>

    <span data-ttu-id="e5fd3-112">**指標金利の再評価** ページに、以前に実行されたすべてのリース指標の再評価プロセスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-112">The **Index rate revaluation** page appears and shows all previous lease index revaluation processes that have been run.</span></span> <span data-ttu-id="e5fd3-113">このページの情報には、番号順序の設定、法人、調整されたリース帳簿の数、IFRS 16 のリースに関する負債調整の合計金額、および ASC 842 リースに対して調整された変動支払の合計金額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-113">The information on this page includes the process ID that was generated from the number sequence setup, the legal entity, the number of lease books that were adjusted, the total liability adjustment for IFRS 16 leases, and the total variable payments that were adjusted for ASC 842 leases.</span></span>

2. <span data-ttu-id="e5fd3-114">再評価を実行するには、操作ウィンドウで、**リース指標の再評価** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-114">To run the revaluation, on the Action Pane, select **Lease index revaluation**.</span></span>

    <span data-ttu-id="e5fd3-115">**指標の再評価パラメーター** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-115">The **Index revaluation parameters** dialog box appears.</span></span> <span data-ttu-id="e5fd3-116">ここでは、再評価するリースを選択するときに使用するリース、リース グループ、またはその他の条件をフィルター処理し、選択することができます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-116">Here, you can filter and select which leases, lease groups, or other criteria should be used when you select the leases to revalue.</span></span> <span data-ttu-id="e5fd3-117">さらに、**バックグラウンドで実行** タブで指標の再評価プロセスを設定して、バッチで実行することができます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-117">Additionally, on the **Run in the background** tab, you can set up the index revaluation process so that it runs in a batch.</span></span>

4. <span data-ttu-id="e5fd3-118">バックグラウンド処理に含めるリースを選択するフィルターを選択してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-118">Select the filters for selecting leases that should be included in the background processing, and then select **OK**.</span></span>

    <span data-ttu-id="e5fd3-119">**指標金利の再評価プレビュー** ダイアログ ボックスが表示され、再評価されるリースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-119">The **Index Rate revaluation preview** dialog box appears and shows the leases that will be revalued.</span></span> <span data-ttu-id="e5fd3-120">また、資産および負債の調整、または変動支払の調整も表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-120">It also shows the asset and liability adjustments or the variable payment adjustments.</span></span>
    
5. <span data-ttu-id="e5fd3-121">リースが再評価されないようにするには、再評価の **必要がある** リースを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-121">To prevent leases from being revalued, select the leases that **should** be revalued.</span></span> <span data-ttu-id="e5fd3-122">リースを選択しない場合は、すべてのリースが再評価されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-122">If you don't select any leases, all leases will be revalued.</span></span> <span data-ttu-id="e5fd3-123">完了後は、**OK** を選択して、リース支払を再評価します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-123">When you've finished, select **OK** to revalue the lease payments.</span></span>
6. <span data-ttu-id="e5fd3-124">特定の指標の再評価プロセスに対して作成されたトランザクションを表示するには、プロセス ID を選択してから **トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-124">To view the transactions that were created for a specific index revaluation process, select the process ID, and then select **Transactions**.</span></span>

    <span data-ttu-id="e5fd3-125">処理中に作成されたトランザクションの詳細がダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-125">A dialog box appears and shows the details of the transactions that were created during processing.</span></span>

> [!NOTE]
> <span data-ttu-id="e5fd3-126">再評価できるのは、再評価日がシステム日付またはそれ以前のリースに限られます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-126">Only leases that have a revaluation date that is on or before the system date can be revalued.</span></span> <span data-ttu-id="e5fd3-127">再評価日がシステム日付よりも後のリースは、システムがすべて無視します。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-127">The system automatically ignores all leases that have a revaluation date that is later than the system date.</span></span>

## <a name="asc-842-leases--index-revaluation"></a><span data-ttu-id="e5fd3-128">ASC 842 リース – 指標の再評価</span><span class="sxs-lookup"><span data-stu-id="e5fd3-128">ASC 842 leases – Index revaluation</span></span>

<span data-ttu-id="e5fd3-129">ASC 842 リースに対するリース再評価プロセスの影響を表示するには、リースの支払スケジュールを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-129">To view the effects of the lease revaluation process on ASC 842 leases, open the payment schedule for a lease.</span></span> <span data-ttu-id="e5fd3-130">このページには、指標の再評価のために再評価日を変更した日またはそれ以降に処理された変動支払のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-130">The page shows only the variable payments that have been made on or after the revaluation date was changed because of the index revaluation.</span></span> <span data-ttu-id="e5fd3-131">償却と減価償却のスケジュールは変更されません。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-131">The amortization and depreciation schedules remain unchanged.</span></span> <span data-ttu-id="e5fd3-132">変動支払がある請求書を作成すると、変動支払は変動支払の転記勘定に借方転記されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-132">When you create an invoice that has a variable payment, the variable payment is debited to the Variable payment posting account.</span></span> <span data-ttu-id="e5fd3-133">また、リース帳簿の設定に応じて、仕入先に直接転記される、または支払手形勘定に転記される貸方エントリには、変動支払金額が追加されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-133">Also the variable payment amount is added to the credit entry that's posted directly to the vendor, or posted to Notes payable account, depending on the lease book setup.</span></span>

<span data-ttu-id="e5fd3-134">リースの詳細ページの支払スケジュール明細行は、新しい指標金利を示す新しい明細行で自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-134">The payment schedule lines on the lease details page are automatically updated with a new line that indicates the new index rate.</span></span> <span data-ttu-id="e5fd3-135">また、列には、明細行が手動作成されたか、指標の再評価プロセスによって作成されたかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-135">Additionally, a column shows whether the line was created manually or through the index revaluation process.</span></span>

## <a name="ifrs-16-leases--index-revaluation"></a><span data-ttu-id="e5fd3-136">IFRS 16 リース – 指標の再評価</span><span class="sxs-lookup"><span data-stu-id="e5fd3-136">IFRS 16 leases – Index revaluation</span></span>

<span data-ttu-id="e5fd3-137">IFRS 16 リースに対するリース再評価プロセスの影響を表示するには、調節済みリースの詳細を開きます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-137">To view the effects of the lease revaluation process on IFRS 16 leases, open the lease details for an adjusted lease.</span></span> <span data-ttu-id="e5fd3-138">**リース期間** および **資産の耐用年数** フィールドが更新され、開始日または更新日から再評価日までの経過時間が反映されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-138">The **Lease term** and **Asset useful life** fields have been updated to reflect the passage of time from the commencement date or modification date to the revaluation date.</span></span> <span data-ttu-id="e5fd3-139">さらに、支払スケジュール明細行が更新され、リースに対する新しい支払、新しい指標金利、および明細行の作成方法が反映されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-139">Additionally, the payment schedule lines have updated to reflect the new payments on the lease, the new index rate, and how the line was created.</span></span>

<span data-ttu-id="e5fd3-140">新たに生成された支払スケジュール (再評価日に開始) を表示したり、更新支払金額の合計を表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-140">You can view the newly generated payment schedule that starts on the revaluation date and show the total updated payment amount.</span></span> <span data-ttu-id="e5fd3-141">新しいリース負債の償却スケジュールと資産の減価償却スケジュールも作成されたため、調整済み支払スケジュールも反映されます。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-141">A new lease liability amortization schedule and an asset depreciation schedule have also been created to reflect the adjusted payment schedule.</span></span>

<span data-ttu-id="e5fd3-142">この仕訳入力は、調整済みの仕訳入力を、指標の再評価に関連するリース支払変更勘定に自動転記しています。</span><span class="sxs-lookup"><span data-stu-id="e5fd3-142">The journal entry has automatically posted the adjustment journal entry to the account for the change in lease payments that are related to the index revaluation.</span></span>
