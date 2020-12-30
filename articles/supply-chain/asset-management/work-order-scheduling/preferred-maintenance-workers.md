---
title: 優先メンテナンス作業者の設定
description: このトピックでは、資産管理で優先メンテナンス作業者を設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431912"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="9f483-103">優先メンテナンス作業者の設定</span><span class="sxs-lookup"><span data-stu-id="9f483-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9f483-104">作業指示書のスケジューリング中に、どちらのメンテナンス作業者または作業グループがその作業指示書を完了するために割り当てられるかについて、優先順位をつけることができます。</span><span class="sxs-lookup"><span data-stu-id="9f483-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="9f483-105">この機能の使用はオプションですが、作業者のスキルと能力に基づいて、最も適格なメンテナンス作業者をジョブ完了のために選択するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9f483-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="9f483-106">スケジューリング時に使用可能なメンテナンス作業者のみがスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="9f483-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="9f483-107">スケジューリング中に優先メンテナンス作業者の設定と作業指示書が一致するものの、メンテナンス作業者が他のジョブに割り当てられている場合、その作業指示書は別の使用可能なメンテナンス作業者にスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="9f483-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="9f483-108">推奨されるメンテナンス作業者を設定する前に、最初にメンテナンス作業者と作業者のグループを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f483-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="9f483-109">メンテナンス作業者と作業者グループの設定方法については、[メンテナンス作業者と作業者グループ](../setup-for-objects/workers-and-worker-groups.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f483-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="9f483-110">優先作業者の設定</span><span class="sxs-lookup"><span data-stu-id="9f483-110">Set up preferred workers</span></span>

<span data-ttu-id="9f483-111">優先メンテナンス作業者もしくは作業者グループは、次の 1 つ以上のものと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9f483-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="9f483-112">取引</span><span class="sxs-lookup"><span data-stu-id="9f483-112">trade</span></span>  
- <span data-ttu-id="9f483-113">メンテナンス作業タイプのバリアント</span><span class="sxs-lookup"><span data-stu-id="9f483-113">maintenance job type variant</span></span>  
- <span data-ttu-id="9f483-114">メンテナンス作業タイプ</span><span class="sxs-lookup"><span data-stu-id="9f483-114">maintenance job type</span></span>  
- <span data-ttu-id="9f483-115">メンテナンス作業タイプのカテゴリ</span><span class="sxs-lookup"><span data-stu-id="9f483-115">maintenance job type category</span></span>  
- <span data-ttu-id="9f483-116">資産</span><span class="sxs-lookup"><span data-stu-id="9f483-116">asset</span></span>  
- <span data-ttu-id="9f483-117">資産タイプ</span><span class="sxs-lookup"><span data-stu-id="9f483-117">asset type</span></span>  

<span data-ttu-id="9f483-118">同じレコードに対して選択する内容が多いほど、設定はより具体的になります。</span><span class="sxs-lookup"><span data-stu-id="9f483-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="9f483-119">**資産管理** > **設定** > **作業者** > **優先メンテナンス作業者** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f483-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="9f483-120">**新規** をクリックして、新規レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f483-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="9f483-121">最初に「既定の」メンテナンス作業者または作業者グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f483-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="9f483-122">つまり、**優先メンテナンス作業者グループ** フィールドもしくは **優先メンテナンス作業者** フィールドでのみ、選択を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9f483-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="9f483-123">次のスクリーンショットにて、**優先メンテナンス作業者グループ** として「要求」が選択されている最初のレコードの例です。</span><span class="sxs-lookup"><span data-stu-id="9f483-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="9f483-124">既定の設定では、作業指示書の内容と他のより具体的な組み合わせが一致しない場合に、作業指示書のスケジューリング中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9f483-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="9f483-125">手順 2 を繰り返して、新規レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f483-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="9f483-126">優先作業者または作業者グループの詳細レベルに応じて、必要な選択を行います。</span><span class="sxs-lookup"><span data-stu-id="9f483-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="9f483-127">*例:* 次のスクリーンショットでは、6 番目の記録で、メンテナンス作業者ショーン リチャードソンが優先作業者として選択されています。</span><span class="sxs-lookup"><span data-stu-id="9f483-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="9f483-128">資産「CH-BP1-03-02」およびメンテナンス作業タイプ「融資評価」を含むワーク オーダーのスケジュール中に、スケジュールされた時間に空きがある場合、彼は自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="9f483-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="9f483-129">一般に、ワーク オーダーのスケジューリング中に優先メンテナンス作業者が選択されると、資産管理はすべての **優先メンテナンス作業者** のレコードから一致の可能性をチェックし、常に最も具体的な組み合わせを最初にチェックします。</span><span class="sxs-lookup"><span data-stu-id="9f483-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="9f483-130">もし一致するものが見つからない場合は、**優先メンテナンス作業者グループ** フィールドまたは **優先メンテナンス作業者** フィールドのいずれかが選択された「既定」レコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9f483-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![図 1](media/02-work-order-scheduling.png)

<span data-ttu-id="9f483-132">また、メンテナンス要求または作業指示書を作成するときに、メンテナンス作業者の *責任者* を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="9f483-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="9f483-133">**すべての作業指示書** と **すべてのメンテナンス要求** にて、必要に応じて選択を編集できます。</span><span class="sxs-lookup"><span data-stu-id="9f483-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="9f483-134">詳細については、[メンテナンス作業者の責任者](../setup-for-maintenance-requests/responsible-workers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f483-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="9f483-135">ワーク オーダー スケジューリング中に、どの作業者がワーク オーダーに関連するジョブを完了する必要があるかを決定するために、異なるスコアが計算されます (これらのスコアは、**資産管理パラメーター** > **ワーク オーダー スケジューリング** リンクで設定されます)。</span><span class="sxs-lookup"><span data-stu-id="9f483-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="9f483-136">ワーク オーダー スケジューリング中に、2 人以上の優先メンテナンス作業者またはメンテナンス担当作業者が同じスコアを獲得した場合、1 人の作業者がランダムに選択されます。</span><span class="sxs-lookup"><span data-stu-id="9f483-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="9f483-137">それ以外の場合は、最高のスコアを持つ作業者が常にワーク オーダーを完了するために割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="9f483-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

