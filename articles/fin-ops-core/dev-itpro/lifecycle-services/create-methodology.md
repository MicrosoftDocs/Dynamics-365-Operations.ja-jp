---
title: 方法の作成または更新
description: Microsoft Dynamics の Lifecycle Services (LCS) は、より反復可能で予測可能な実装プロジェクト体験を保証するために使用できる方法を提供します。 いずれかの提供された方法を使用するか、自分の方法を作成することができます。 方法を使用すると、進捗状況を容易に追跡およびレポートすることができます。
author: meeramahabala
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 266824
ms.assetid: ac723685-f87c-4854-9bb7-b92ccf1094eb
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af17a07aa5e079cc69a807a886179953d9f2afb2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687916"
---
# <a name="create-or-update-methodologies"></a><span data-ttu-id="ffe07-105">方法の作成または更新</span><span class="sxs-lookup"><span data-stu-id="ffe07-105">Create or update methodologies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffe07-106">Microsoft Dynamics の Lifecycle Services (LCS) は、より反復可能で予測可能な実装プロジェクト体験を保証するために使用できる方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-106">Lifecycle Services (LCS) for Microsoft Dynamics provides methodologies that you can use to ensure a more repeatable and predictable implementation project experience.</span></span> <span data-ttu-id="ffe07-107">いずれかの提供された方法を使用するか、自分の方法を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-107">You can use one of the provided methodologies or create your own.</span></span> <span data-ttu-id="ffe07-108">方法を使用すると、進捗状況を容易に追跡およびレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-108">With a methodology, you can easily track and report on your progress.</span></span>

<span data-ttu-id="ffe07-109">フェーズ、タスク、およびマイルストーンで構成される方法。</span><span class="sxs-lookup"><span data-stu-id="ffe07-109">A methodology consists of phases, tasks, and milestones.</span></span> <span data-ttu-id="ffe07-110">各フェーズでは、任意の数のタスクを持つことができ、そのうちのいくつかは必須です。</span><span class="sxs-lookup"><span data-stu-id="ffe07-110">Each phase can have any number of tasks, some of which are mandatory.</span></span> <span data-ttu-id="ffe07-111">フェーズにあるすべてのタスクが完了したら、そのフェーズを完了とマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-111">When all of the tasks in a phase are completed, the phase can be marked as complete.</span></span> <span data-ttu-id="ffe07-112">また、完了するフェーズを予想するときのマイルス トーンを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-112">You can also create a milestone for when you anticipate a phase to be completed.</span></span> <span data-ttu-id="ffe07-113">以下の方法が LCS プロジェクトに含まれています。</span><span class="sxs-lookup"><span data-stu-id="ffe07-113">The following methodologies are included in an LCS project:</span></span>

-   <span data-ttu-id="ffe07-114">実装</span><span class="sxs-lookup"><span data-stu-id="ffe07-114">Implementation</span></span>
-   <span data-ttu-id="ffe07-115">確認ステップ</span><span class="sxs-lookup"><span data-stu-id="ffe07-115">Sure Step</span></span>
-   <span data-ttu-id="ffe07-116">開発を学ぶ</span><span class="sxs-lookup"><span data-stu-id="ffe07-116">Learn development</span></span>
-   <span data-ttu-id="ffe07-117">ソリューションの移行および作成</span><span class="sxs-lookup"><span data-stu-id="ffe07-117">Migrate and create solutions</span></span>
-   <span data-ttu-id="ffe07-118">ソリューションの消費</span><span class="sxs-lookup"><span data-stu-id="ffe07-118">Consume solutions</span></span>

<span data-ttu-id="ffe07-119">**注記:** Microsoft Methodology に公開された新しい変更が既存のプロジェクトにプッシュされないという既知の制限があります。</span><span class="sxs-lookup"><span data-stu-id="ffe07-119">**Note:** There is a known limitation where new changes that are published to the Microsoft Methodology are not pushed to existing projects.</span></span> <span data-ttu-id="ffe07-120">新しいプロジェクトのみがこれらの変更を取得します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-120">Only new projects get these changes.</span></span>

## <a name="add-or-update-methodologies"></a><span data-ttu-id="ffe07-121">方法の追加または更新</span><span class="sxs-lookup"><span data-stu-id="ffe07-121">Add or update methodologies</span></span>

<span data-ttu-id="ffe07-122">パートナーまたはプロジェクト管理者は、新しい方法を作成するか、自身の組織または特定のプロジェクトの範囲内の既存の方法を変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-122">A partner or a project administrator can create new methodologies or make changes to an existing methodology for their organization or within the scope of a specific project.</span></span> <span data-ttu-id="ffe07-123">これらの追加および変更は、プロジェクト レベルまたは組織レベルで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-123">These additions and changes can be made at the project level or at the organization level.</span></span> <span data-ttu-id="ffe07-124">新しい方法を作成して保存し、既存の方法を更新し、必要に応じて組織レベルに新しい方法を取り入れたり方法を変更するには、次の手順を使用ます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-124">Use the following procedures to create and save a new methodology, update existing methodologies, and when appropriate, promote a new methodology or methodology changes to the organization level.</span></span>

### <a name="create-a-new-methodology"></a><span data-ttu-id="ffe07-125">新しい方法の作成</span><span class="sxs-lookup"><span data-stu-id="ffe07-125">Create a new methodology</span></span>
1.  <span data-ttu-id="ffe07-126">Lifecycle Services ダッシュ ボードで、画面の右側の、**方法の管理** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ffe07-126">On the Lifecycle Services dashboard, on the right side of the screen, click **Manage methodologies**.</span></span>
2.  <span data-ttu-id="ffe07-127">**方法の管理**ページで、プラス記号 (+) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ffe07-127">On the \*\*Manage methodologies \*\*page, click the plus sign (+).</span></span>
3.  <span data-ttu-id="ffe07-128">**新しい方法** ウィンドウに、新しい方法の名前および説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-128">In the **New methodology** pane, enter a name and description for the new methodology.</span></span> <span data-ttu-id="ffe07-129">**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ffe07-129">Click **Confirm**.</span></span>
4.  <span data-ttu-id="ffe07-130">**オプション:** 方法を確認した後、グリッド内の方法、および **昇格** を選択して、組織レベルに昇格できます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-130">**Optional:** After you have confirmed the methodology, you can promote it to the organization level by selecting the methodology in the grid, and then selecting **Promote**.</span></span> <span data-ttu-id="ffe07-131">[![promotemethodology](./media/promotemethodology-1024x506.jpg)](./media/promotemethodology.jpg)**注記:** 組織レベルに方法を昇格させるには、組織の管理者でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ffe07-131">[![promotemethodology](./media/promotemethodology-1024x506.jpg)](./media/promotemethodology.jpg) **Note:** You must be an admin in your organization to promote a methodology to the organization level.</span></span>

### <a name="change-or-update-a-methodology"></a><span data-ttu-id="ffe07-132">方法の変更または更新</span><span class="sxs-lookup"><span data-stu-id="ffe07-132">Change or update a methodology</span></span>
<span data-ttu-id="ffe07-133">方法論を変更するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="ffe07-133">There are two ways to make changes to a methodology.</span></span> <span data-ttu-id="ffe07-134">既存の方法を追加するか、プロジェクトの範囲内で方法に変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-134">You can append an existing methodology or you can make changes to a methodology in the scope of a project.</span></span> <span data-ttu-id="ffe07-135">LCSプロジェクト ダッシュ ボードから更新する方法を選択し、**方法の編集** または **方法の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-135">From the LCS project dashboard, select the methodology that you want to update, and then select **Edit methodology** or **Append methodology**.</span></span> <span data-ttu-id="ffe07-136">[![projectlevelmethodology](./media/projectlevelmethodology-1024x494.jpg)](./media/projectlevelmethodology.jpg) 方法を編集することを選択した場合は、次の変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ffe07-136">[![projectlevelmethodology](./media/projectlevelmethodology-1024x494.jpg)](./media/projectlevelmethodology.jpg) If you select to edit the methodology, you can make the following changes:</span></span>

-   <span data-ttu-id="ffe07-137">新しいフェーズを追加します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-137">Add a new phase.</span></span>
-   <span data-ttu-id="ffe07-138">新しいタスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-138">Add a new task.</span></span>
-   <span data-ttu-id="ffe07-139">フェーズまたはタスクを編集します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-139">Edit a phase or task.</span></span> <span data-ttu-id="ffe07-140">(フェーズとタスクの一部を編集することができますが、Microsoft によって適用されるため、ロックされて、編集できないものもあります。)</span><span class="sxs-lookup"><span data-stu-id="ffe07-140">(Some phases and tasks can be edited, but others are enforced by Microsoft and are therefore locked and can’t be edited.)</span></span>
-   <span data-ttu-id="ffe07-141">フェーズまたはタスクをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ffe07-141">Copy a phase or task.</span></span>
-   <span data-ttu-id="ffe07-142">フェーズおよびタスクの順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-142">Reorder phases and tasks.</span></span>
-   <span data-ttu-id="ffe07-143">フェーズまたはタスクを削除します。</span><span class="sxs-lookup"><span data-stu-id="ffe07-143">Delete a phase or task.</span></span>




