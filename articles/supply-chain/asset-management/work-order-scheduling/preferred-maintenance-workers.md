---
title: 優先メンテナンス作業者の設定
description: このトピックでは、資産管理で優先メンテナンス作業者を設定する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887414"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="8b09a-103">優先メンテナンス作業者</span><span class="sxs-lookup"><span data-stu-id="8b09a-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8b09a-104">ワーク オーダーのスケジューリング中に、どのメンテナンス作業者がワーク オーダーを完了するために割り当てられるかについて、優先順位をつけることができます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="8b09a-105">この機能の使用はオプションですが、作業者のスキルと能力に基づいて、最も適格なメンテナンス作業者をジョブ完了のために選択するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="8b09a-106">したがって、ワーク オーダーのスケジューリング中に、**優先メンテナンス作業者**の設定を使用して、特定のメンテナンス作業者もしくは作業者グループをワーク オーダーにスケジュールするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8b09a-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="8b09a-107">スケジューリング時に使用可能なメンテナンス作業者のみがスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="8b09a-108">スケジューリング中に優先メンテナンス作業者の設定とワーク オーダーが一致するものの、メンテナンス作業者が他のジョブに割り当てられている場合、そのワーク オーダーは別の使用可能なメンテナンス作業者にスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="8b09a-109">メンテナンス作業者を設定する前に、選択可能なメンテナンス作業者および作業者グループを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b09a-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="8b09a-110">メンテナンス作業者および作業者グループを設定する方法については、[メンテナンス作業者および作業者グループ](../setup-for-objects/workers-and-worker-groups.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b09a-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="8b09a-111">優先作業者の設定</span><span class="sxs-lookup"><span data-stu-id="8b09a-111">Set up preferred workers</span></span>

<span data-ttu-id="8b09a-112">優先メンテナンス作業者もしくは作業者グループは、以下の特定のものと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="8b09a-113">取引</span><span class="sxs-lookup"><span data-stu-id="8b09a-113">trade</span></span>  
- <span data-ttu-id="8b09a-114">メンテナンス作業タイプのバリアント</span><span class="sxs-lookup"><span data-stu-id="8b09a-114">maintenance job type variant</span></span>  
- <span data-ttu-id="8b09a-115">メンテナンス作業タイプ</span><span class="sxs-lookup"><span data-stu-id="8b09a-115">maintenance job type</span></span>  
- <span data-ttu-id="8b09a-116">メンテナンス作業タイプのカテゴリ</span><span class="sxs-lookup"><span data-stu-id="8b09a-116">maintenance job type category</span></span>  
- <span data-ttu-id="8b09a-117">資産</span><span class="sxs-lookup"><span data-stu-id="8b09a-117">asset</span></span>  
- <span data-ttu-id="8b09a-118">資産タイプ</span><span class="sxs-lookup"><span data-stu-id="8b09a-118">asset type</span></span>  

<span data-ttu-id="8b09a-119">または、これらの選択の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="8b09a-119">or a combination of those selections.</span></span> <span data-ttu-id="8b09a-120">同じレコードに対して選択する内容が多いほど、設定はより具体的になります。</span><span class="sxs-lookup"><span data-stu-id="8b09a-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="8b09a-121">**資産管理** > **設定** > **作業者** > **優先メンテナンス作業者**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b09a-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="8b09a-122">**新規**をクリックして、新規レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b09a-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="8b09a-123">最初に、上記の箇条書きリストに示されているフィールドで選択のない「既定の」メンテナンス作業者または作業者グループの設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="8b09a-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="8b09a-124">つまり、**優先メンテナンス作業者グループ** フィールドもしくは**優先メンテナンス作業者**フィールドでのみ、選択を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="8b09a-125">次の図は、優先メンテナンス作業者グループとして「要求」が選択されている最初のレコードの例です。</span><span class="sxs-lookup"><span data-stu-id="8b09a-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="8b09a-126">この既定の設定は、ワーク オーダーの内容と他のより具体的な組み合わせが一致しない場合に、ワーク オーダーのスケジューリング中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="8b09a-127">手順 2 を繰り返して、新規レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b09a-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="8b09a-128">優先作業者または作業者グループの詳細レベルに応じて、必要な選択を行います。</span><span class="sxs-lookup"><span data-stu-id="8b09a-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="8b09a-129">*例:* 次の図では、6 番目のレコードで、メンテナンス作業者ショーン リチャードソンが優先作業者として選択されています。</span><span class="sxs-lookup"><span data-stu-id="8b09a-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="8b09a-130">資産「CH-BP1-03-02」およびメンテナンス作業タイプ「融資評価」を含むワーク オーダーのスケジュール中に、スケジュールされた時間に空きがある場合、彼は自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="8b09a-131">一般に、ワーク オーダーのスケジューリング中に優先メンテナンス作業者が選択されると、資産管理はすべての**優先メンテナンス作業者**のレコードから一致の可能性をチェックし、常に最も具体的な組み合わせを最初にチェックします。</span><span class="sxs-lookup"><span data-stu-id="8b09a-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="8b09a-132">もし一致するものが見つからない場合は、**優先メンテナンス作業者グループ** フィールドまたは **優先メンテナンス作業者**フィールドのいずれかが選択された「既定」レコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![図 1](media/02-work-order-scheduling.png)

<span data-ttu-id="8b09a-134">また、メンテナンス要求またはワーク オーダーを作成するときにメンテナンス担当作業者を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="8b09a-135">**すべてのワークオーダー**と**すべてのメンテナンス要求**では、必要に応じて選択を編集できます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="8b09a-136">詳細については、[メンテナンス担当作業者](../setup-for-maintenance-requests/responsible-workers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b09a-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="8b09a-137">ワーク オーダー スケジューリング中に、どの作業者がワーク オーダーに関連するジョブを完了する必要があるかを決定するために、異なるスコアが計算されます (これらのスコアは、**資産管理パラメーター** > **ワーク オーダー スケジューリング** リンクで設定されます)。</span><span class="sxs-lookup"><span data-stu-id="8b09a-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="8b09a-138">ワーク オーダー スケジューリング中に、2 人以上の優先メンテナンス作業者またはメンテナンス担当作業者が同じスコアを獲得した場合、1 人の作業者がランダムに選択されます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="8b09a-139">それ以外の場合は、最高のスコアを持つ作業者が常にワーク オーダーを完了するために割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8b09a-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

