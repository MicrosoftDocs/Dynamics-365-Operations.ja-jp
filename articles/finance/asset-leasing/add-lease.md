---
title: リースの追加またはコピー (プレビュー版)
description: このトピックでは、新しいリースを作成する方法について説明します。これにより、資産リースの情報の入力や、既存のリースから情報をコピーすることができます。
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
ms.openlocfilehash: 325a1b7948f3cb8033fa93b7c36f1f1f6b7dbb27
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220014"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="62e52-103">リースの追加またはコピー (プレビュー版)</span><span class="sxs-lookup"><span data-stu-id="62e52-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62e52-104">このトピックでは、資産リースに最初からリースを作成する方法と、既存のリースをコピーしてリースを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="62e52-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="62e52-105">最初からリースを作成するには、新しいリースの情報を入力し、リース スケジュールを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62e52-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="62e52-106">ひとつ以上のリースを設定しておくと、既存のリースから情報をコピーして、新しいリースの作成に必要な情報を簡単に編集することができます。</span><span class="sxs-lookup"><span data-stu-id="62e52-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="62e52-107">リースの作成</span><span class="sxs-lookup"><span data-stu-id="62e52-107">Create a lease</span></span>

<span data-ttu-id="62e52-108">アセット リースでリースを作成するには以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="62e52-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="62e52-109">**リースの概要** ページの、アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e52-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="62e52-110">リースの情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="62e52-110">Enter the lease information.</span></span> <span data-ttu-id="62e52-111">必須フィールドには赤い境界線が表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="62e52-112">リース スケジュールの作成</span><span class="sxs-lookup"><span data-stu-id="62e52-112">Create a lease schedule</span></span>

<span data-ttu-id="62e52-113">リースの情報を入力後、次の手順に従ってリース スケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="62e52-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="62e52-114">財務分析コードは、ユーザー定義の財務分析コードに基づいて変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="62e52-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="62e52-115">**スケジュールの作成** を選択して、リース帳簿を生成します。</span><span class="sxs-lookup"><span data-stu-id="62e52-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="62e52-116">リース帳簿には、支払、償却、減価償却、経費のスケジュールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="62e52-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="62e52-117">リース帳簿にアクセスし、新しく作成されたスケジュールを表示するには、**帳簿** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="62e52-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="62e52-118">**帳簿の詳細** ページには、割り当てられている帳簿ごとにリースがどのように計上されるかが示されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="62e52-119">ここでは、リースのスケジュールを表示できます。</span><span class="sxs-lookup"><span data-stu-id="62e52-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="62e52-120">支払スケジュールには、**リースの追加** ページの **支払スケジュール明細行** タブの入力が含まれます。</span><span class="sxs-lookup"><span data-stu-id="62e52-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="62e52-121">各支払額や変動支払を変更することも可能です。</span><span class="sxs-lookup"><span data-stu-id="62e52-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="62e52-122">リース負債は、変更された支払スケジュールに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="62e52-123">支払スケジュールの確認が完了したら、**スケジュールの確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e52-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="62e52-124">スケジュールを確認した後は、そのリースを編集できなくなります。</span><span class="sxs-lookup"><span data-stu-id="62e52-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62e52-125">**リースの追加** ページの支払スケジュール明細行から自動的にリース期間が計算され ます。</span><span class="sxs-lookup"><span data-stu-id="62e52-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="62e52-126">リース期間を月単位で計算する場合は、特定の支払スケジュール明細行の開始日と終了日の差分が検出されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="62e52-127">その後、次の支払スケジュール明細行に移動し、差分を再び検索します。</span><span class="sxs-lookup"><span data-stu-id="62e52-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="62e52-128">最後に、すべての金額を合計して、月単位でのリース期間を決定します。</span><span class="sxs-lookup"><span data-stu-id="62e52-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="62e52-129">計算された期限の経費を表示するには、**負債償却スケジュール**  ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="62e52-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="62e52-130">計算された定額減価償却を表示するには、**資産減価償却スケジュール** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="62e52-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="62e52-131">計算された金額の確認が完了したら、**当初認識** ページで当初認識の仕訳入力を作成できます。</span><span class="sxs-lookup"><span data-stu-id="62e52-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="62e52-132">仕訳帳が作成されたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62e52-133">仕訳帳エントリは、手動でエントリを転記するまで一般会計に転記されません。</span><span class="sxs-lookup"><span data-stu-id="62e52-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="62e52-134">転記前に、提案された当初認識のエントリを確認するには、**資産のリース仕訳帳を選択** します。</span><span class="sxs-lookup"><span data-stu-id="62e52-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62e52-135">資産のリース仕訳帳は手動で作成できません。</span><span class="sxs-lookup"><span data-stu-id="62e52-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="62e52-136">リースのスケジュールが作成されると、自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="62e52-137">当初認識仕訳帳エントリを確認し、転記の準備ができている場合は、**転記** を選択して、一般会計における資産の使用権 (ROU) とリース負債を認識します。</span><span class="sxs-lookup"><span data-stu-id="62e52-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="62e52-138">リースのコピー</span><span class="sxs-lookup"><span data-stu-id="62e52-138">Copy a lease</span></span>

<span data-ttu-id="62e52-139">資産のリースではリースの詳細をコピーして、同じ情報を持つ新しいリースを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="62e52-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="62e52-140">コピーしたリースのスケジュールを作成する前に、リース フィールドを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="62e52-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="62e52-141">**リースの概要** ページで、コピーするリースを選択し、[アクション] ウィンドウで **リースのコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e52-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62e52-142">リース ID の番号順に **手動** パラメーターをオフにした場合、そのシーケンスの次の番号はコピーされたリースのリース ID として自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="62e52-143">**手動** のパラメーターが有効になっている場合は、リース のコピーを続行する前に、リースIDの入力を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="62e52-144">**コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62e52-144">Select **Copy**.</span></span> <span data-ttu-id="62e52-145">選択したリースのリースの詳細が新しいリースにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="62e52-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="62e52-146">その後、保存する前に新しいリースの詳細を編集して、リース スケジュールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="62e52-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="62e52-147">資産リース仕訳帳</span><span class="sxs-lookup"><span data-stu-id="62e52-147">Asset leasing journal</span></span>

<span data-ttu-id="62e52-148">資産リースで作成されたすべての仕訳帳エントリは、資産リース仕訳帳に含まれています。</span><span class="sxs-lookup"><span data-stu-id="62e52-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="62e52-149">**資産のリース仕訳帳**  ページ (**資産のリース契約 \> 仕訳帳のエントリ \> 資産のリース仕訳帳**) では、転記ステータス別にフィルタリングし、特定の仕訳帳エントリと伝票を表示して、未転記仕訳帳エントリを転記することができます。</span><span class="sxs-lookup"><span data-stu-id="62e52-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="62e52-150">資産のリース仕訳帳は手動で作成できません。</span><span class="sxs-lookup"><span data-stu-id="62e52-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="62e52-151">リースのスケジュールが作成されると、自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="62e52-151">It's automatically created when lease schedules are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]