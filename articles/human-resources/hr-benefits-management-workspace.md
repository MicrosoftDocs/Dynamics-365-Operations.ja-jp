---
title: 給付金管理ワークスペース
description: このトピックでは、Dynamics 365 Human Resources の給付金管理ワークスペースについて説明します。
author: andreabichsel
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a2325da54b8d47ef39d0aacb5dac87107ebdd5bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019566"
---
# <a name="benefits-management-workspace"></a><span data-ttu-id="24529-103">給付金管理ワークスペース</span><span class="sxs-lookup"><span data-stu-id="24529-103">Benefits management workspace</span></span>

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="24529-104">このトピックでは、Dynamics 365 Human Resources の **給付金管理** ワークスペースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="24529-104">This topic describes the **Benefits management** workspace in Dynamics 365 Human Resources.</span></span>

> [!NOTE]
> <span data-ttu-id="24529-105">**給付金管理** ワークスペースを表示するには、まず機能管理の **(プレビュー) 給付金管理ワークスペース** 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="24529-105">To view the **Benefits management** workspace, you must first enable the **(Preview) Benefits management workspace** feature in Feature management.</span></span> <span data-ttu-id="24529-106">プレビュー機能を有効にする方法については、[機能の管理](../hr-admin-manage-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24529-106">For more information about enabling preview features, see [Manage features](../hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="24529-107">![給付金管理ワークスペースを有効にする](./media/hr-benefits-management-workspace-enable.png)</span><span class="sxs-lookup"><span data-stu-id="24529-107">![Enable Benefits management workspace](./media/hr-benefits-management-workspace-enable.png)</span></span>

<span data-ttu-id="24529-108">**給付金管理** ワークスペースを使用すると、確認が必要な福利厚生項目をすばやく表示できます。</span><span class="sxs-lookup"><span data-stu-id="24529-108">The **Benefits management** workspace gives you a quick view of benefits items that require your attention.</span></span> <span data-ttu-id="24529-109">このページでは、次のものを確認できます。</span><span class="sxs-lookup"><span data-stu-id="24529-109">On this page, you can see:</span></span>

- <span data-ttu-id="24529-110">アクションを待っている品目の合計</span><span class="sxs-lookup"><span data-stu-id="24529-110">Totals for items awaiting action</span></span>
- <span data-ttu-id="24529-111">選択が未確認の作業者</span><span class="sxs-lookup"><span data-stu-id="24529-111">Workers with unconfirmed selections</span></span>
- <span data-ttu-id="24529-112">最近福利厚生に加入した作業者</span><span class="sxs-lookup"><span data-stu-id="24529-112">Workers who recently enrolled in benefits</span></span>
- <span data-ttu-id="24529-113">将来のライフ イベントを持つ作業者</span><span class="sxs-lookup"><span data-stu-id="24529-113">Workers with future life events</span></span>
- <span data-ttu-id="24529-114">登録されていない新規採用</span><span class="sxs-lookup"><span data-stu-id="24529-114">New hires who aren't enrolled</span></span>
- <span data-ttu-id="24529-115">有効なライフ イベントを持つ作業者</span><span class="sxs-lookup"><span data-stu-id="24529-115">Workers with active life events</span></span>
- <span data-ttu-id="24529-116">プランが未選択で、オープン登録を行っている作業者</span><span class="sxs-lookup"><span data-stu-id="24529-116">Workers with open enrollments who haven't opted for any plans</span></span>

![給付金管理ワークスペース](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a><span data-ttu-id="24529-118">アクション項目の表示</span><span class="sxs-lookup"><span data-stu-id="24529-118">View action items</span></span>

<span data-ttu-id="24529-119">タイルまたはタブを選択して、アクション項目を表示できます。タブを選択すると、ワークスペース ページの右側で作業者を表示および選択できます。</span><span class="sxs-lookup"><span data-stu-id="24529-119">You can view your action items by either selecting a tile or a tab. If you select a tab, you can view and select workers right on the workspace page.</span></span>

![アクション項目](./media/hr-benefits-management-workspace-action-items.png)

<span data-ttu-id="24529-121">タイルを選択した場合は、その領域のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="24529-121">If you select a tile, you go to the page for that area.</span></span> <span data-ttu-id="24529-122">たとえば、これらのタイルのいずれかを選択すると、**作業者の給付金プラン** ページが表示され、次の操作を実行する必要がある従業員に対してフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="24529-122">For example, selecting any of these tiles displays the **Worker benefits plans** page, filtered for employees you need to take action on:</span></span>

- <span data-ttu-id="24529-123">**未確認の選択**</span><span class="sxs-lookup"><span data-stu-id="24529-123">**Unconfirmed selections**</span></span>
- <span data-ttu-id="24529-124">**計画がチェック アウトされていない登録を開く**</span><span class="sxs-lookup"><span data-stu-id="24529-124">**Open enrollments with no checked out plans**</span></span>
- <span data-ttu-id="24529-125">**給付金に登録済み**</span><span class="sxs-lookup"><span data-stu-id="24529-125">**Enrolled in benefits**</span></span>
- <span data-ttu-id="24529-126">**新規採用が未登録**</span><span class="sxs-lookup"><span data-stu-id="24529-126">**New hire not enrolled**</span></span>

![作業者給付金計画](./media/hr-benefits-management-workspace-plans.png)

<span data-ttu-id="24529-128">**有効なライフ イベント** または **将来のライフ イベント** タイルを選択すると、有効なライフ イベントまたは将来のライフ イベントのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="24529-128">Selecting the **Active life events** or **Future life events** tiles takes you to a list of active or future life events.</span></span>

![ライフ イベント](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a><span data-ttu-id="24529-130">処理中</span><span class="sxs-lookup"><span data-stu-id="24529-130">Processing</span></span>

<span data-ttu-id="24529-131">登録の適格性、ライフ イベント、またはレート変更の更新を処理するには、ナビゲーション バーで適切な項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="24529-131">To process enrollment eligibility, life events, or rate change updates, select the appropriate item on the navigation bar.</span></span>

![処理中](./media/hr-benefits-management-workspace-processing.png)

<span data-ttu-id="24529-133">プロセス結果を表示するには、ページで **プロセス結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24529-133">To view process results, select **Process results** on the page.</span></span>

![プロセス結果](./media/hr-benefits-management-workspace-process-results.png)

<span data-ttu-id="24529-135">給付金処理の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24529-135">For more information about benefits processing, see:</span></span>

- [<span data-ttu-id="24529-136">登録適格性の処理</span><span class="sxs-lookup"><span data-stu-id="24529-136">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="24529-137">ライフ イベントの変更の処理</span><span class="sxs-lookup"><span data-stu-id="24529-137">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="24529-138">ライフ イベントの適格性の処理</span><span class="sxs-lookup"><span data-stu-id="24529-138">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="24529-139">ライフ イベントの処理</span><span class="sxs-lookup"><span data-stu-id="24529-139">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="24529-140">レート変更の処理</span><span class="sxs-lookup"><span data-stu-id="24529-140">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a><span data-ttu-id="24529-141">期間の変更</span><span class="sxs-lookup"><span data-stu-id="24529-141">Change period</span></span>

<span data-ttu-id="24529-142">異なる給付金の期間を表示するには、**期間** ドロップダウンから選択します。</span><span class="sxs-lookup"><span data-stu-id="24529-142">To view a different benefits period, select it from the **Period** dropdown.</span></span>

![期間の変更](./media/hr-benefits-management-workspace-period.png)

## <a name="view-more-options"></a><span data-ttu-id="24529-144">その他のオプションの表示</span><span class="sxs-lookup"><span data-stu-id="24529-144">View more options</span></span>

<span data-ttu-id="24529-145">詳細情報および実行できるアクションを表示するには、**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24529-145">To view more information and actions you can take, select **Links**.</span></span>

![リンク](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a><span data-ttu-id="24529-147">参照</span><span class="sxs-lookup"><span data-stu-id="24529-147">See also</span></span>

[<span data-ttu-id="24529-148">福利厚生の管理の概要</span><span class="sxs-lookup"><span data-stu-id="24529-148">Benefits management overview</span></span>](hr-benefits-management-overview.md)