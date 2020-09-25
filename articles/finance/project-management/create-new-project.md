---
title: 新しいプロジェクトの作成
description: このトピックでは、新規プロジェクト作成方法について説明します。
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760593"
---
# <a name="create-a-new-project"></a><span data-ttu-id="0a1cc-103">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="0a1cc-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a1cc-104">新規プロジェクトを作成するには、以下の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="0a1cc-105">**プロジェクト管理**ページで、**新規プロジェクト**を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="0a1cc-106">**プロジェクト タイプ:** 時間/実費払い</span><span class="sxs-lookup"><span data-stu-id="0a1cc-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="0a1cc-107">**プロジェクト名:** XYZ アップグレード フェーズ 2</span><span class="sxs-lookup"><span data-stu-id="0a1cc-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="0a1cc-108">**プロジェクト グループ:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="0a1cc-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="0a1cc-109">**プロジェクト契約 ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="0a1cc-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="0a1cc-110">**プロジェクトの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="0a1cc-111">プロジェクトへのリソースの割り当て</span><span class="sxs-lookup"><span data-stu-id="0a1cc-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="0a1cc-112">**作業者**ページで、**作業者**リストで、事前にコンピテンシーを設定した作業者のレコードを選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="0a1cc-113">[アクション ウィンドウ] の、**プロジェクト**タブの、**設定**グループで、**プロジェクトの割り当て**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="0a1cc-114">**プロジェクト**タブの**リソース検証プロジェクト割り当て**ページで、**選択したプロジェクトにプロジェクトを追加**フィールドで、**XYZ アップグレード フェーズ 2** プロジェクトをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="0a1cc-115">**残りのプロジェクト**ウィンドウで、プロジェクトを選択し、矢印ボタンを選択して、**選択したプロジェクト**ウィンドウに追加します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="0a1cc-116">必要に応じて、リソースのカテゴリを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="0a1cc-117">カテゴリ タイプは、**コスト**または**収益**です。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="0a1cc-118">カテゴリ タイプは、組織により決定されます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-118">The category type is determined by your organization.</span></span> <span data-ttu-id="0a1cc-119">リソースのカテゴリが割り当てられていない場合、Finance は、原価および収益の時間価格の既定のカテゴリを検索します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="0a1cc-120">プロジェクト リソースおよびロール特性の設定</span><span class="sxs-lookup"><span data-stu-id="0a1cc-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="0a1cc-121">プロジェクト マネージャは、プロジェクトに必要なロールを作成する場合、プロジェクト リソース機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="0a1cc-122">リソース引当時に確認済のリソースがまだ不明な場合、ロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="0a1cc-123">プロジェクトの計画ステージを続行できるように、ロールは計画されているリソースとして一時的に引き当てることができます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="0a1cc-124">[![ロールの例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="0a1cc-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="0a1cc-125">**シナリオ:** Contoso は承認されたプロジェクト憲章のある時間/実費払プロジェクトを完了するために採用されました。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="0a1cc-126">若手のプロジェクト マネージャは、プロジェクトの作業範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="0a1cc-127">リソース マネージャーは、新しいプロジェクトの作業に引き当てられる特定のリソースを識別します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="0a1cc-128">プロジェクトの重要な目的のために、プロジェクトのスポンサーはロールの一つとして上級プロジェクト マネージャを要求しました。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="0a1cc-129">若手のプロジェクト マネージャがプロジェクト計画時にリソース情報を必要とする場合、リソース マネージャーは新しいリソースを取得し、システムのロールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="0a1cc-130">次の手順は、リソース マネージャーが上級プロジェクト マネージャ ロールを設定し、リソースの特性を関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="0a1cc-131">後で、ロールを使用して必要なリソースのコンピテンシーに一致する利用可能なリソースを検索できます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="0a1cc-132">**セットアップ ロール**ページで、**新規**を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="0a1cc-133">**ロール ID:** 上級プロジェクト マネージャ</span><span class="sxs-lookup"><span data-stu-id="0a1cc-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="0a1cc-134">**説明:** 上級プロジェクト マネージャ</span><span class="sxs-lookup"><span data-stu-id="0a1cc-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="0a1cc-135">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-135">Select **Create**.</span></span>
3. <span data-ttu-id="0a1cc-136">**上級プロジェクト マネージャ**ロールを選択し、**特性の構成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="0a1cc-137">**特性タイプ**フィールドで、**スキル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="0a1cc-138">**使用可能特性**フィールドに、探しているスキルを入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="0a1cc-139">**特性タイプ**フィールドで、**証明書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="0a1cc-140">**使用可能特性**フィールドに、探しているスキルを入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="0a1cc-141">プロジェクトへのプロジェクト リソースの割り当て</span><span class="sxs-lookup"><span data-stu-id="0a1cc-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="0a1cc-142">**すべてのプロジェクト** ページで **XYZ アップグレード フェーズ 2** プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="0a1cc-143">**プロジェクト チームとスケジューリング**タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="0a1cc-144">**ロール**フィールドで、**チーム メンバー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="0a1cc-145">**カレンダーから予約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="0a1cc-146">**リソースの可用性**ページで、**ビュー設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="0a1cc-147">**ビュー設定の調整**ページで、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="0a1cc-148">**日付範囲ビューの形式:** 日</span><span class="sxs-lookup"><span data-stu-id="0a1cc-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="0a1cc-149">**可用性に関する説明の表示:** はい</span><span class="sxs-lookup"><span data-stu-id="0a1cc-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="0a1cc-150">**残余能力の表示:** はい</span><span class="sxs-lookup"><span data-stu-id="0a1cc-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="0a1cc-151">リソースの一覧で、リソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="0a1cc-152">**確定予約**および**全能力**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="0a1cc-153">既定のロールへのリソースの割り当て</span><span class="sxs-lookup"><span data-stu-id="0a1cc-153">Assign a resource to a default role</span></span>

<span data-ttu-id="0a1cc-154">プロジェクト マネージャーまたはリソース マネージャーが、プロジェクトに引き当てることができるリソースにさらにドリルダウンできるよう助けます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="0a1cc-155">既存のリソースまたは最近取得したリソースに、既定のロールを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="0a1cc-156">たとえば、ダニエルはビジネス アナリストのロールを果たせる経験とスキルを備え、採用されました。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="0a1cc-157">リソース マネージャはダニエルの既定のロールとしてこのロールを割り当てました。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="0a1cc-158">したがって、リソース マネージャは、プロジェクトに従事できる業務アナリストのプールにダニエルを追加しました。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="0a1cc-159">リソース引当で、プロジェクト マネージャは、プロジェクトの作業に使用できるロール リソースをフィルタリングできます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="0a1cc-160">リソースの履行中に複数の条件による決定分析を実行するとき、この情報を一つの基準として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="0a1cc-161">特定のプロジェクトで、特定のスキル、教育、および経験を持つリソースを検索する場合、フィルターに他のリソース特性を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="0a1cc-162">**シナリオ:** 承認済のプロジェクトが開始され、プロジェクト計画ステージで上級プロジェクト マネージャ ロールが計画されているリソースとして引き当てられました。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="0a1cc-163">リソース マネージャーは、上級プロジェクト マネージャ ロールを履行するためのリソースを取得しています。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="0a1cc-164">**リソース リスト**ページで、**Daniel Goldschmidt** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="0a1cc-165">**リソース ロール**ページで、**新規**を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="0a1cc-166">**有効:** 現在の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="0a1cc-167">**有効期限:** **なし**を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="0a1cc-168">**ロール:** **上級プロジェクト マネージャ**を入力します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="0a1cc-169">**保存**を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="0a1cc-170">**コンピテンシー**タブで、**ProjectMgmt** スキルおよび **PMP** 証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="0a1cc-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
