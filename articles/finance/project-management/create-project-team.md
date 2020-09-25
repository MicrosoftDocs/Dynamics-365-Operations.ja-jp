---
title: プロジェクト チームを作成する
description: このトピックでは、プロジェクトの作成方法、および管理方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760594"
---
# <a name="create-a-project-team"></a><span data-ttu-id="65ff0-103">プロジェクト チームの作成</span><span class="sxs-lookup"><span data-stu-id="65ff0-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65ff0-104">プロジェクトで事前に設定されているロールを使用するには、プロジェクト マネージャは、プロジェクトにロールを関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ff0-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="65ff0-105">プロジェクトに対して複数のロールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="65ff0-106">混乱を回避するために、引当中にこれらのロールに自動的にラベル張りが行われます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="65ff0-107">たとえば、プロジェクト マネージャが 3 人のソフトウェア エンジニアを必要とする場合、**ソフトウェア エンジニア 1**、**ソフトウェア エンジニア 2**、および**ソフトウェア エンジニア 3** のラベルがある 3 つのソフトウェア エンジニア ロールが自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="65ff0-108">ロール特性がロールに既に設定されている場合は、リソースの検索時に、それらがフィルタとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="65ff0-109">さらに絞り込んで検索するために、追加の特性を必要に応じて追加できます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="65ff0-110">リソースの可用性の表示を向上させるために、ビュー設定をカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="65ff0-111">時間、日、週、月、四半期、および年次可用性を表示するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="65ff0-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="65ff0-112">リソースの使用可能な能力および残余能力を表示するオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="65ff0-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="65ff0-113">このオプションは、活動またはリソースの可用性に使用可能な時間を予測する際の時間管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="65ff0-114">プロジェクト マネージャはページでロールを選択でき、要件を満たす使用可能リソースがある場合は、ロールに対応するリソースを引き当てるために選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="65ff0-115">計画ステージの、この時点でリソースを引き当てる必要がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="65ff0-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="65ff0-116">WBS を作成すると、プロジェクトに対してスタッフ割り当て済リソースにロールを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="65ff0-117">WBS でロールがスタッフ割り当て済リソースに置き換えられた場合、プロジェクト チームのリスト、およびスケジューリングはリソース設定により自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="65ff0-118">[![ロールと実際のリソースの両方を含むプロジェクト チームのリスト](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="65ff0-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="65ff0-119">プロジェクト マネージャーには、**残余能力**、**全能力**、**能力の割合**、および**時間数の指定**など、プロジェクトのリソースを予約するさまざまなオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="65ff0-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="65ff0-120">リソース割り当てを変更した場合、これらの予約オプションはいつでもキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="65ff0-121">2 つのタイプのスケジューリングがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="65ff0-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="65ff0-122">**確定予約** – 特定期間のエンゲージメント作業にリソース引当を承認および確認します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="65ff0-123">**仮予約** – 特定期間のエンゲージメント作業にリソース引当を一時的に設定します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="65ff0-124">次の手順では、プロジェクト チームの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="65ff0-125">プロジェクト チームの作成</span><span class="sxs-lookup"><span data-stu-id="65ff0-125">Create a project team</span></span>

1. <span data-ttu-id="65ff0-126">**すべてのプロジェクト**リストページで、プロジェクトを選択し、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="65ff0-127">**プロジェクト チームとスケジューリング**タブの**スケジュールの終了日**フィールドに、スケジュールの開始日に 1 ヶ月を加えて入力します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="65ff0-128">たとえば、スケジュールの開始日が 2017 年 6 月 24 日 (24/06/2017) の場合、**24/07/2017** と入力します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="65ff0-129">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-129">Select **Add**.</span></span>
4. <span data-ttu-id="65ff0-130">**プロジェクトへのロールの追加**ウィンドウの、**ロール**フィールドで、**上級プロジェクト マネージャ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="65ff0-131">**必要なコンピテンシー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="65ff0-132">**特性の選択**ページで、上級プロジェクト マネージャ ロールとして事前に設定した特性が既定で選択されます。</span><span class="sxs-lookup"><span data-stu-id="65ff0-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="65ff0-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-133">Select **OK**.</span></span>
7. <span data-ttu-id="65ff0-134">**プロジェクトへのロールの追加**ページの**リソースの数**フィールドで、 **1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="65ff0-135">**リソース**フィールドで、ルックアップが、必要なコンピテンシーのあるすべてのリソースを示します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="65ff0-136">**Daniel Goldschmidt** を選択し、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="65ff0-137">**プロジェクト**ページで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="65ff0-138">**プロジェクトへのロールの追加**ウィンドウの、**ロール**フィールドで、**チーム メンバー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="65ff0-139">**リソースの数**フィールドで、**5** を入力します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="65ff0-140">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-140">Select **Create**.</span></span>
12. <span data-ttu-id="65ff0-141">**プロジェクト**ページで、**リソースの履行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="65ff0-142">プロジェクト チームの監視</span><span class="sxs-lookup"><span data-stu-id="65ff0-142">Monitor project teams</span></span>
1. <span data-ttu-id="65ff0-143">**すべてのプロジェクト**ページで、**XYZ アップグレード フェーズ 2** プロジェクトに対し**プロジェクト ID** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="65ff0-144">**プロジェクト チームとスケジューリング**クイック タブで、一覧表示されたプロジェクト リソースが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="65ff0-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
