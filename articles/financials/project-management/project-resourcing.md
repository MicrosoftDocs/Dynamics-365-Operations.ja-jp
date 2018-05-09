---
title: "プロジェクト リソース"
description: "このトピックは、プロジェクト リソースに関する情報を提供します。"
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6d5d21cebc42cb044172d61916f26b815bb96737
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="project-resourcing"></a><span data-ttu-id="53ec4-103">プロジェクト リソース</span><span class="sxs-lookup"><span data-stu-id="53ec4-103">Project resourcing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53ec4-104">このトピックは、プロジェクト リソースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="53ec4-105">プロジェクト計画ステージでのプロジェクト マネージャーとリソース マネージャーの 1 つの課題は、プロジェクトの作業に適切なリソースを指定し引き当てる、リソース割り当てです。</span><span class="sxs-lookup"><span data-stu-id="53ec4-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="53ec4-106">Microsoft Dynamics 365 for Finance and Operations では、プロジェクトのリソース機能で、特定のエンゲージメントまたはエンゲージメントの一部に割り当てることができる、一時リソースとして処理されるロールを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-106">In Microsoft Dynamics 365 for Finance and Operations, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement or part of an engagement.</span></span> <span data-ttu-id="53ec4-107">プロジェクト マネージャとリソース マネージャーは、このタイプのリソースを使用して、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

- <span data-ttu-id="53ec4-108">リソースの照合を容易にするため、必要なコンピテンシーを持つロールを定義します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-108">Define a role that has the required competencies, so that it's easy to match resources.</span></span>
- <span data-ttu-id="53ec4-109">引当済のリソースをベースにした最初のエンゲージメント スケジュールを定義するためにロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
- <span data-ttu-id="53ec4-110">プロジェクトの割り当てロールとリソースに基づいて、原価を見積もり、最初の予算を決定します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
- <span data-ttu-id="53ec4-111">各エンゲージメントに必要な引き当てるリソースの数を見積もるためにロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
- <span data-ttu-id="53ec4-112">プロジェクトのライフ サイクル全体に必要なリソースの数を見積もります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-112">Estimate the number of resources that are required for the whole life cycle of a project.</span></span>
- <span data-ttu-id="53ec4-113">最初のリソース割り当てを使用して、作業分解構造 (WBS) を起草します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="53ec4-114">[![プロジェクトのライフ サイクル](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="53ec4-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span>

<span data-ttu-id="53ec4-115">プロジェクト計画が進行すると、計画されたリソースをスタッフが割り当てられたリソースと置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="53ec4-116">プロジェクト マネージャーは、どのプロジェクト ステージにおいても、リソース引当を戻したり、更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-116">The project manager can also go back and update the resourcing reservations during any project stage.</span></span>

## <a name="set-up-project-resources"></a><span data-ttu-id="53ec4-117">プロジェクト リソースを設定します</span><span class="sxs-lookup"><span data-stu-id="53ec4-117">Set up project resources</span></span>
<span data-ttu-id="53ec4-118">カレンダーを設定したり、従業員または作業者に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-118">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="53ec4-119">このカレンダーは、プロジェクトおよびプロジェクトに引き当てられているリソースの作業時間をスケジュールするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-119">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="53ec4-120">カレンダーの設定時に、プロジェクト マネージャはリソースの最適化の一部として、リソースを平準化できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-120">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="53ec4-121">カレンダー スケジュールに基づいて、制限をリソースに置くことができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-121">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="53ec4-122">**カレンダー** ページでカレンダーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-122">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="53ec4-123">プロジェクト リソースとして作業者を設定する場合は、リソースを設定している会社で勤務する作業者から選択できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-123">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="53ec4-124">また、組織内の他の会社から作業者を選択できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-124">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="53ec4-125">これらの作業者は、会社間リソースと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-125">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="53ec4-126">次の手順では、会社内のプロジェクト リソースとして作業を設定する方法、会社間プロジェクト リソースの設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-126">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

### <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="53ec4-127">プロジェクト リソースとして作業者を設定</span><span class="sxs-lookup"><span data-stu-id="53ec4-127">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="53ec4-128">[作業者] ページの [作業者] リストで、プロジェクト リソースとして追加する作業者を選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-128">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="53ec4-129">[アクション ウィンドウ] で、[プロジェクト] &gt; [設定] &gt; [プロジェクトの設定] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-129">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="53ec4-130">カレンダーを選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-130">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="53ec4-131">また、リソースの既定のプロジェクトを前の割り当てのタイプとして指定できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-131">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="53ec4-132">前の割り当ては、リソース マネージャーまたはプロジェクト マネージャが、使用されるプロジェクトのリソースを事前にわかっている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-132">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="53ec4-133">前の割り当ては、プロジェクトのスポンサーまたは顧客の要求に基づくものとすることもできます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-133">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="53ec4-134">プロジェクトを前の割り当てとするには、[残りのプロジェクト] リストの、[プロジェクト] タブの、[プロジェクトの割り当て] ページで、適切なプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-134">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

### <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="53ec4-135">会社間リソースの設定</span><span class="sxs-lookup"><span data-stu-id="53ec4-135">Set up an intercompany resource</span></span>

<span data-ttu-id="53ec4-136">会社間リソースとして作業者を設定する場合、貸与の会社と借入の会社両方の設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-136">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

<span data-ttu-id="53ec4-137">**貸与の会社では**</span><span class="sxs-lookup"><span data-stu-id="53ec4-137">**In the lending company**</span></span>

1. <span data-ttu-id="53ec4-138">Finance and Operations では、貸与の会社が選択されていることを確認し、前のセクションでの手順、「プロジェクト リソースとして作業者を設定する」を完了させます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-138">In Finance and Operations, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="53ec4-139">[会社間会計] ページで、[新規] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-139">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="53ec4-140">[法人 ID] フィールドで、貸与の会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-140">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="53ec4-141">必要に応じて残りのフィールドに入力し、[保存] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-141">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="53ec4-142">[移転価格] ページで、[新規] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-142">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="53ec4-143">[借入側の法人] フィールドで、適切な会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-143">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="53ec4-144">借入の会社に、このセクションの最初に作成したリソースのみを貸与する場合は、[リソース] フィールドで、作成したリソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-144">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="53ec4-145">借入の会社に対して、貸与の会社でのすべてのリソースを使用できるようにするには、 [リソース] フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="53ec4-145">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="53ec4-146">[会社間] タブの [プロジェクト管理および会計パラメータ] ページで、[会社間リソースのスケジューリングやタイムシートを有効にする] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-146">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

<span data-ttu-id="53ec4-147">**借入の会社では**</span><span class="sxs-lookup"><span data-stu-id="53ec4-147">**In the borrowing company**</span></span>

- <span data-ttu-id="53ec4-148">[リソース リスト] ページで、貸与会社の作成されたリソース名を検索フィルターに入力して、借入会社のリソースの一覧に名前が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-148">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="manage-resource-competencies"></a><span data-ttu-id="53ec4-149">リソースのコンピテンシーの管理</span><span class="sxs-lookup"><span data-stu-id="53ec4-149">Manage resource competencies</span></span>
<span data-ttu-id="53ec4-150">リソースのコンピテンシーは、リソース管理の重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="53ec4-150">Resource competencies are an essential part of resource management.</span></span> <span data-ttu-id="53ec4-151">コンピテンシーを、適切なバランスのスキル、教育、証明書、およびプロジェクト経験のあるリソースを決定するためのベースラインとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-151">Competencies can be used as a baseline to determine resources that have the correct balance of skills, education, certification, and project experience.</span></span> <span data-ttu-id="53ec4-152">各リソースに対してこの情報を設定し、定期的に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-152">You should set up this information for each resource and update it on a regular basis.</span></span> <span data-ttu-id="53ec4-153">このようにして、プロジェクトのリソース割り当て時に特定のリソースのコンピテンシーを合わせると、機能を最大化できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-153">In this way, you can maximize capabilities when specific resource competencies are matched during project resource assignment.</span></span>

<span data-ttu-id="53ec4-154">[![スキル、証明書、教育、およびプロジェクト経験の例](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span><span class="sxs-lookup"><span data-stu-id="53ec4-154">[![Examples of skills, certifications, education, and project experience](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span></span>

<span data-ttu-id="53ec4-155">次の手順では、リソースのコンピテンシーを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-155">The following procedures explain how to set up some of the competencies for a resource.</span></span>

<span data-ttu-id="53ec4-156">作業者のコンピテンシーを設定するには、[人事管理] の [作業者] リスト ページ、または [プロジェクト管理および会計] で [リソース] リスト ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-156">To set up competencies for a worker, you can use either the **Workers** list page in Human resources or the **Resources** list page in Project management and accounting.</span></span> <span data-ttu-id="53ec4-157">次の手順で、[人事管理] の [作業者] リスト ページが使用されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-157">For the following procedures, the **Workers** list page in Human resources is used.</span></span>

### <a name="set-up-competencies-certificates"></a><span data-ttu-id="53ec4-158">コンピテンシーの設定: 証明書</span><span class="sxs-lookup"><span data-stu-id="53ec4-158">Set up competencies: Certificates</span></span>

1. <span data-ttu-id="53ec4-159">[作業者] リスト ページで、証明書情報を追加する作業者用の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-159">On the **Workers** list page, select the line for the worker to add certificate information for.</span></span>
2. <span data-ttu-id="53ec4-160">[アクション ウィンドウ] の、[作業者] タブの、[コンピテンシー] グループで、[証明書] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-160">On the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Certificates**.</span></span>
3. <span data-ttu-id="53ec4-161">[新規] を選択し、それから [証明書タイプ] フィールドで、[PMP] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-161">Select **New**, and then, in the **Certificate type** field, select **PMP**.</span></span>
4. <span data-ttu-id="53ec4-162">[開始日] フィールドで、[10/1/2015] を選択し、[保存] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-162">In the **Start date** field, select **10/1/2015**, and select **Save**.</span></span>

### <a name="set-up-competencies-skills"></a><span data-ttu-id="53ec4-163">コンピテンシーの設定: スキル</span><span class="sxs-lookup"><span data-stu-id="53ec4-163">Set up competencies: Skills</span></span>

1. <span data-ttu-id="53ec4-164">[作業者] リスト ページで、前の手順で使用した作業者がまだ選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-164">On the **Workers** list page, make sure that the worker that you used in the previous procedure is still selected.</span></span> <span data-ttu-id="53ec4-165">次に、[アクション ウィンドウ] の、[作業者] タブの、[コンピテンシー] グループで、[スキル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-165">Then, on the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Skills**.</span></span>
2. <span data-ttu-id="53ec4-166">[新規] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-166">Select **New**.</span></span>
3. <span data-ttu-id="53ec4-167">[スキル] フィールドで、[プロジェクト管理] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-167">In the **Skill** field, select **Project management**.</span></span>
4. <span data-ttu-id="53ec4-168">[レベル] フィールドで、[5 専門家] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-168">In the **Level** field, select **5 Expert**.</span></span>
5. <span data-ttu-id="53ec4-169">[取得日] フィールドで、[1-/14/2014] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-169">In the **Level date** field, select **1-/14/2014**.</span></span>
6. <span data-ttu-id="53ec4-170">[経験年数] フィールドに、[10] と入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-170">In the **Years of experience** field, enter **10**.</span></span>
7. <span data-ttu-id="53ec4-171">[保存] を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-new-project"></a><span data-ttu-id="53ec4-172">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="53ec4-172">Create a new project</span></span>
1. <span data-ttu-id="53ec4-173">[プロジェクト管理] ページで、[新規プロジェクト] を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-173">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="53ec4-174">**プロジェクト タイプ:** 時間/実費払い</span><span class="sxs-lookup"><span data-stu-id="53ec4-174">**Project type:** Time and material</span></span>
    - <span data-ttu-id="53ec4-175">**プロジェクト名:** XYZ アップグレード フェーズ 2</span><span class="sxs-lookup"><span data-stu-id="53ec4-175">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="53ec4-176">**プロジェクト グループ:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="53ec4-176">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="53ec4-177">**プロジェクト契約 ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="53ec4-177">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="53ec4-178">[プロジェクトの作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-178">Select **Create project**.</span></span>

### <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="53ec4-179">プロジェクトへのリソースの割り当て</span><span class="sxs-lookup"><span data-stu-id="53ec4-179">Assign a resource to a project</span></span>

1. <span data-ttu-id="53ec4-180">[作業者] ページで、[作業者] リストで、事前にコンピテンシーを設定した作業者のレコードを選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-180">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="53ec4-181">[アクション ウィンドウ] の、[プロジェクト] タブの、[設定] グループで、[プロジェクトの割り当て] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-181">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="53ec4-182">[プロジェクト] タブの [リソース検証プロジェクト割り当て] ページで、[選択したプロジェクトにプロジェクトを追加] フィールドで、[XYZ アップグレード フェーズ 2] プロジェクトをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-182">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="53ec4-183">[残りのプロジェクト] ウィンドウで、プロジェクトを選択し、矢印ボタンを選択して、[選択したプロジェクト] ウィンドウに追加します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-183">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="53ec4-184">必要に応じて、リソースのカテゴリを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-184">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="53ec4-185">カテゴリ タイプは、[コスト] または [収益] です。</span><span class="sxs-lookup"><span data-stu-id="53ec4-185">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="53ec4-186">カテゴリ タイプは、組織により決定されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-186">The category type is determined by your organization.</span></span> <span data-ttu-id="53ec4-187">リソースのカテゴリが割り当てられていない場合、Finance and Operations は、原価および収益の時間価格の既定のカテゴリを検索します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-187">If no categories are assigned for a resource, Finance and Operations looks up the default category on hour prices for cost and revenue.</span></span>

### <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="53ec4-188">プロジェクト リソースおよびロール特性の設定</span><span class="sxs-lookup"><span data-stu-id="53ec4-188">Set up project resource and role characteristics</span></span>

<span data-ttu-id="53ec4-189">プロジェクト マネージャは、プロジェクトに必要なロールを作成する場合、プロジェクト リソース機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-189">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="53ec4-190">リソース引当時に確認済のリソースがまだ不明な場合、ロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-190">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="53ec4-191">プロジェクトの計画ステージを続行できるように、ロールは計画されているリソースとして一時的に引き当てることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-191">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="53ec4-192">[![ロールの例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="53ec4-192">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="53ec4-193">**シナリオ:** Contoso は承認されたプロジェクト憲章のある時間/実費払プロジェクトを完了するために採用されました。</span><span class="sxs-lookup"><span data-stu-id="53ec4-193">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="53ec4-194">若手のプロジェクト マネージャは、プロジェクトの作業範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-194">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="53ec4-195">リソース マネージャーは、新しいプロジェクトの作業に引き当てられる特定のリソースを識別します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-195">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="53ec4-196">プロジェクトの重要な目的のために、プロジェクトのスポンサーはロールの一つとして上級プロジェクト マネージャを要求しました。</span><span class="sxs-lookup"><span data-stu-id="53ec4-196">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="53ec4-197">若手のプロジェクト マネージャがプロジェクト計画時にリソース情報を必要とする場合、リソース マネージャーは新しいリソースを取得し、システムのロールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-197">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="53ec4-198">次の手順は、リソース マネージャーが上級プロジェクト マネージャ ロールを設定し、リソースの特性を関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-198">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="53ec4-199">後で、ロールを使用して必要なリソースのコンピテンシーに一致する利用可能なリソースを検索できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-199">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="53ec4-200">[セットアップ ロール] ページで、[新規] を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-200">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="53ec4-201">**ロール ID:** 上級プロジェクト マネージャ</span><span class="sxs-lookup"><span data-stu-id="53ec4-201">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="53ec4-202">**説明:** 上級プロジェクト マネージャ</span><span class="sxs-lookup"><span data-stu-id="53ec4-202">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="53ec4-203">[作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-203">Select **Create**.</span></span>
3. <span data-ttu-id="53ec4-204">[上級プロジェクト マネージャ] ロールを選択し、[特性の構成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-204">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="53ec4-205">[特性タイプ] フィールドで、[スキル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-205">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="53ec4-206">[使用可能特性] フィールドに、探しているスキルを入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-206">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="53ec4-207">[特性タイプ] フィールドで、[証明書] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-207">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="53ec4-208">[使用可能特性] フィールドに、探しているスキルを入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-208">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

### <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="53ec4-209">プロジェクトへのプロジェクト リソースの割り当て</span><span class="sxs-lookup"><span data-stu-id="53ec4-209">Assign a project resource to a project</span></span>

1. <span data-ttu-id="53ec4-210">[**すべてのプロジェクト**] ページで [**XYZ アップグレード フェーズ 2**] プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-210">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="53ec4-211">[プロジェクト チームとスケジューリング] タブで、[追加] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-211">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="53ec4-212">[ロール] フィールドで、[チーム メンバー] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-212">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="53ec4-213">[カレンダーから予約] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-213">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="53ec4-214">[リソースの可用性] ページで、[ビュー設定] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-214">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="53ec4-215">[ビュー設定の調整] ページで、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-215">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="53ec4-216">**日付範囲ビューの形式:** 日</span><span class="sxs-lookup"><span data-stu-id="53ec4-216">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="53ec4-217">**可用性に関する説明の表示:** はい</span><span class="sxs-lookup"><span data-stu-id="53ec4-217">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="53ec4-218">**残余能力の表示:** はい</span><span class="sxs-lookup"><span data-stu-id="53ec4-218">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="53ec4-219">リソースの一覧で、リソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-219">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="53ec4-220">[確定予約] および [全能力] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-220">Select **Hard book** and **Full capacity**.</span></span>


### <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="53ec4-221">既定のロールへのリソースの割り当て</span><span class="sxs-lookup"><span data-stu-id="53ec4-221">Assign a resource to a default role</span></span>

<span data-ttu-id="53ec4-222">プロジェクト マネージャーまたはリソース マネージャーが、プロジェクトに引き当てることができるリソースにさらにドリルダウンできるよう助けます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-222">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="53ec4-223">既存のリソースまたは最近取得したリソースに、既定のロールを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-223">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="53ec4-224">たとえば、ダニエルはビジネス アナリストのロールを果たせる経験とスキルを備え、採用されました。</span><span class="sxs-lookup"><span data-stu-id="53ec4-224">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="53ec4-225">リソース マネージャはダニエルの既定のロールとしてこのロールを割り当てました。</span><span class="sxs-lookup"><span data-stu-id="53ec4-225">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="53ec4-226">したがって、リソース マネージャは、プロジェクトに従事できる業務アナリストのプールにダニエルを追加しました。</span><span class="sxs-lookup"><span data-stu-id="53ec4-226">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="53ec4-227">リソース引当で、プロジェクト マネージャは、プロジェクトの作業に使用できるロール リソースをフィルタリングできます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-227">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="53ec4-228">リソースの履行中に複数の条件による決定分析を実行するとき、この情報を一つの基準として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-228">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="53ec4-229">特定のプロジェクトで、特定のスキル、教育、および経験を持つリソースを検索する場合、フィルターに他のリソース特性を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-229">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="53ec4-230">**シナリオ:** 承認済のプロジェクトが開始され、プロジェクト計画ステージで上級プロジェクト マネージャ ロールが計画されているリソースとして引き当てられました。</span><span class="sxs-lookup"><span data-stu-id="53ec4-230">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="53ec4-231">リソース マネージャーは、上級プロジェクト マネージャ ロールを履行するためのリソースを取得しています。</span><span class="sxs-lookup"><span data-stu-id="53ec4-231">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="53ec4-232">[リソース リスト] ページで、[Daniel Goldschmidt] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-232">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="53ec4-233">[リソース ロール] ページで、[新規] を選択し、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-233">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="53ec4-234">[有効:] 現在の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-234">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="53ec4-235">[有効期限:] [なし] を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-235">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="53ec4-236">[ロール:] [上級プロジェクト マネージャ] を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-236">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="53ec4-237">[保存] を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-237">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="53ec4-238">[コンピテンシー] タブで、[ProjectMgmt] スキルおよび [PMP] 証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-238">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>

## <a name="set-up-role-based-pricing"></a><span data-ttu-id="53ec4-239">ロール ベースの価格の設定</span><span class="sxs-lookup"><span data-stu-id="53ec4-239">Set up role-based pricing</span></span>
<span data-ttu-id="53ec4-240">すべての原価、販売、および移転価格をロールに設定できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-240">All cost, sales, and transfer prices can be set up for roles.</span></span>

1. <span data-ttu-id="53ec4-241">[販売価格 (時間)] ページで、[新規] を選択し、有効日を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-241">On the **Sales price (hour)** page, select **New**, and enter an effective date.</span></span>
2. <span data-ttu-id="53ec4-242">[ロール] 列で、ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-242">In the **Role** column, select a role.</span></span>
3. <span data-ttu-id="53ec4-243">[価格決定] 列で、選択したリソース ロールの価格を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-243">In the **Pricing** column, enter a price for the selected resource role.</span></span>

## <a name="form-a-project-team"></a><span data-ttu-id="53ec4-244">プロジェクト チームの形成</span><span class="sxs-lookup"><span data-stu-id="53ec4-244">Form a project team</span></span>
<span data-ttu-id="53ec4-245">プロジェクトで事前に設定されているロールを使用するには、プロジェクト マネージャは、プロジェクトにロールを関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-245">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="53ec4-246">プロジェクトに対して複数のロールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-246">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="53ec4-247">混乱を回避するために、Finance and Operations は引当中にこれらのロールを自動的にラベル張りします。</span><span class="sxs-lookup"><span data-stu-id="53ec4-247">To prevent confusion, Finance and Operations automatically labels these roles during reservation.</span></span> <span data-ttu-id="53ec4-248">たとえば、プロジェクト マネージャが 3 人のソフトウェア エンジニアを必要とする場合、[ソフトウェア エンジニア 1]、[ソフトウェア エンジニア 2]、および [ソフトウェア エンジニア 3] のラベルがある 3 つのソフトウェア エンジニア ロールが自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-248">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="53ec4-249">ロール特性がロールに既に設定されている場合は、リソースの検索時に、それらがフィルタとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-249">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="53ec4-250">さらに絞り込んで検索するために、追加の特性を必要に応じて追加できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-250">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="53ec4-251">リソースの可用性の表示を向上させるために、ビュー設定をカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-251">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="53ec4-252">時間、日、週、月、四半期、および年次可用性を表示するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-252">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="53ec4-253">リソースの使用可能な能力および残余能力を表示するオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-253">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="53ec4-254">このオプションは、活動またはリソースの可用性に使用可能な時間を予測する際の時間管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-254">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="53ec4-255">プロジェクト マネージャはページでロールを選択でき、要件を満たす使用可能リソースがある場合は、ロールに対応するリソースを引き当てるために選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-255">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="53ec4-256">計画ステージの、この時点でリソースを引き当てる必要がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="53ec4-256">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="53ec4-257">WBS を作成すると、プロジェクトに対してスタッフ割り当て済リソースにロールを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-257">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="53ec4-258">WBS でロールがスタッフ割り当て済リソースに置き換えられた場合、プロジェクト チームのリスト、およびスケジューリングはリソース設定により自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-258">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="53ec4-259">[![ロールと実際のリソースの両方を含むプロジェクト チームのリスト](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="53ec4-259">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="53ec4-260">プロジェクト マネージャーには、[残余能力]、[全能力]、[能力の割合]、および [時間数の指定] など、プロジェクトのリソースを予約するさまざまなオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-260">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="53ec4-261">リソース割り当てを変更した場合、これらの予約オプションはいつでもキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-261">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="53ec4-262">2 つのタイプのスケジューリングがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="53ec4-262">Two types of booking are supported:</span></span>

- <span data-ttu-id="53ec4-263">[確定予約] – 特定期間のエンゲージメント作業にリソース引当を承認および確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-263">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="53ec4-264">[仮予約] – 特定期間のエンゲージメント作業にリソース引当を一時的に設定します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-264">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="53ec4-265">次の手順では、プロジェクト チームの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-265">The following procedure explains how to create a project team.</span></span>

### <a name="create-a-project-team"></a><span data-ttu-id="53ec4-266">プロジェクト チームの作成</span><span class="sxs-lookup"><span data-stu-id="53ec4-266">Create a project team</span></span>

1. <span data-ttu-id="53ec4-267">[すべてのプロジェクト] リストページで、プロジェクトを選択し、[編集] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-267">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="53ec4-268">[プロジェクト チームとスケジューリング] タブの [スケジュールの終了日] フィールドに、スケジュールの開始日に 1 ヶ月を加えて入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-268">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="53ec4-269">たとえば、スケジュールの開始日が 2017 年 6 月 24 日 (24/06/2017) の場合、**24/07/2017** と入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-269">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="53ec4-270">[追加] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-270">Select **Add**.</span></span>
4. <span data-ttu-id="53ec4-271">[プロジェクトへのロールの追加] ウィンドウの、[ロール] フィールドで、[上級プロジェクト マネージャ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-271">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="53ec4-272">[必要なコンピテンシー] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-272">Select **Required competencies**.</span></span>
6. <span data-ttu-id="53ec4-273">[特性の選択] ページで、上級プロジェクト マネージャ ロールとして事前に設定した特性が既定で選択されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-273">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="53ec4-274">[OK] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-274">Select **OK**.</span></span>
7. <span data-ttu-id="53ec4-275">[プロジェクトへのロールの追加] ページの [リソースの数] フィールドで、 **1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-275">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="53ec4-276">[リソース] フィールドで、ルックアップが、必要なコンピテンシーのあるすべてのリソースを示します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-276">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="53ec4-277">[Daniel Goldschmidt] を選択し、[作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-277">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="53ec4-278">[プロジェクト] ページで、[追加] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-278">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="53ec4-279">[プロジェクトへのロールの追加] ウィンドウの、[ロール] フィールドで、[チーム メンバー] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-279">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="53ec4-280">[リソースの数] フィールドで、**5** を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-280">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="53ec4-281">[作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-281">Select **Create**.</span></span>
12. <span data-ttu-id="53ec4-282">[プロジェクト] ページで、[リソースの履行] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-282">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="resource-capacity-synchronization"></a><span data-ttu-id="53ec4-283">リソース能力同期</span><span class="sxs-lookup"><span data-stu-id="53ec4-283">Resource capacity synchronization</span></span>
<span data-ttu-id="53ec4-284">リソース同期のプロセスは、カレンダーの情報および基準カレンダーがプロジェクトのリソース スケジューリングにトリクルダウンするのを保証するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-284">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="53ec4-285">カレンダーが変更される場合、プロセスはプロジェクト リソースのスケジューリングに必要な更新を行います。</span><span class="sxs-lookup"><span data-stu-id="53ec4-285">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="53ec4-286">カレンダーのリソースの情報が事前に同期化されているため、プロセスもパフォーマンスを向上させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-286">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="53ec4-287">したがって、リソースのスケジューリング情報の更新がより迅速に行われます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-287">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="53ec4-288">一つずつ作成する代わりに、バッチとしてプロセスをスケジューリングすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="53ec4-288">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="53ec4-289">それ以外の場合は、情報が最後に同期された包含日付を忘れるリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-289">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="53ec4-290">包含日付を使用しない場合、日付の同期時にギャップが発生します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-290">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![カレンダーの同期](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="53ec4-292">リソース能力のロールアップを同期</span><span class="sxs-lookup"><span data-stu-id="53ec4-292">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="53ec4-293">同期プロセスは、すべてのリソース カレンダー情報と同期するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="53ec4-293">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="53ec4-294">この情報には、プロジェクトのリソース カレンダー能力テーブルの変更についての基準カレンダーの情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-294">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="53ec4-295">新しいリソースがプロジェクトに追加されると、同期により、更新されたカレンダー情報が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-295">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="53ec4-296">この同期はいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-296">This synchronization can be done at any time.</span></span>

<span data-ttu-id="53ec4-297">バッチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="53ec4-297">We recommend that you use a batch.</span></span> <span data-ttu-id="53ec4-298">確保済能力の同期中に、このオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-298">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="53ec4-299">[プロジェクト管理および会計] &gt; [定期処理] &gt; [能力の同期] &gt; [リソース能力のロールアップを同期] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-299">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="53ec4-300">次の表でオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-300">Set the options in the following table.</span></span>

    | <span data-ttu-id="53ec4-301">オプション</span><span class="sxs-lookup"><span data-stu-id="53ec4-301">Option</span></span>      | <span data-ttu-id="53ec4-302">説明</span><span class="sxs-lookup"><span data-stu-id="53ec4-302">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="53ec4-303">期間コード</span><span class="sxs-lookup"><span data-stu-id="53ec4-303">Period code</span></span> | <span data-ttu-id="53ec4-304">必要に応じて、リソース能力のロールアップの同期プロセス用に開始日と終了日を設定する、一般会計の日付間隔コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-304">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="53ec4-305">入社日</span><span class="sxs-lookup"><span data-stu-id="53ec4-305">Start date</span></span>  | <span data-ttu-id="53ec4-306">リソース能力のロールアップの同期プロセスの開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-306">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="53ec4-307">終了日</span><span class="sxs-lookup"><span data-stu-id="53ec4-307">End date</span></span>    | <span data-ttu-id="53ec4-308">リソース能力のロールアップの同期プロセスの終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-308">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="53ec4-309">[![同期プロセス](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="53ec4-309">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>

## <a name="set-up-roles-on-wbs-templates"></a><span data-ttu-id="53ec4-310">WBS テンプレートでのロールの設定</span><span class="sxs-lookup"><span data-stu-id="53ec4-310">Set up roles on WBS templates</span></span>
<span data-ttu-id="53ec4-311">プロジェクト マネージャは、新しいプロジェクトの WBS を作成するときに適用できる WBS テンプレートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-311">Project managers can set up WBS templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="53ec4-312">プロジェクト マネージャはテンプレートを作成すると、ロールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-312">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="53ec4-313">WBS テンプレートにロールを割り当てるには、次の手順に従います。 </span><span class="sxs-lookup"><span data-stu-id="53ec4-313">Use the following procedure to assign a role to a WBS template.</span></span>

1. <span data-ttu-id="53ec4-314">[プロジェクト管理および会計] &gt; [設定] &gt; [プロジェクト] &gt; [作業分解構造テンプレート] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-314">Select **Project management and accounting** &gt; **Setup** &gt; **Projects** &gt; **Work breakdown structure templates**.</span></span>
2. <span data-ttu-id="53ec4-315">選択した WBS テンプレートの [詳細] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-315">Select **Details** for a selected WBS template.</span></span>
3. <span data-ttu-id="53ec4-316">リストでタスクを選択し、[ロール] フィールドで、タスクに割り当てるロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-316">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

### <a name="work-with-a-wbs"></a><span data-ttu-id="53ec4-317">WBS の使用</span><span class="sxs-lookup"><span data-stu-id="53ec4-317">Work with a WBS</span></span>

<span data-ttu-id="53ec4-318">新しい WBS を作成できます、または既存の WBS テンプレートから WBS をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-318">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="53ec4-319">プロジェクト マネージャは WBS の新しいタスクにロールを割り当てることにより簡単にリソースを管理できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-319">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="53ec4-320">ロールは、リソースが取得されるか、またはタスクの作業の確認されたリソースが識別された後のいずれかに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-320">Roles can be replaced either after a resource is acquired or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="53ec4-321">この柔軟性により、プロジェクト マネージャーが実行できるタスクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="53ec4-321">This flexibility lets project managers perform the following tasks:</span></span>

- <span data-ttu-id="53ec4-322">WBS 作業パッケージに必要なリソース数を識別します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-322">Identify the number of resources that are required for WBS work packages.</span></span>
- <span data-ttu-id="53ec4-323">プロジェクト原価を見積もります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-323">Estimate project costs.</span></span>
- <span data-ttu-id="53ec4-324">暫定予算を確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-324">Determine a preliminary budget.</span></span>
- <span data-ttu-id="53ec4-325">ロールとリソースに基づいて、活動の期間を見積もります。</span><span class="sxs-lookup"><span data-stu-id="53ec4-325">Estimate activity duration, based on roles and resources.</span></span>
- <span data-ttu-id="53ec4-326">利用可能なプロジェクト情報に基づいて、プロジェクト管理計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-326">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="53ec4-327">リソース機能を有効に利用するために WBS に追加のオプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="53ec4-327">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53ec4-328">オプション</span><span class="sxs-lookup"><span data-stu-id="53ec4-328">Option</span></span></th>
<th><span data-ttu-id="53ec4-329">説明</span><span class="sxs-lookup"><span data-stu-id="53ec4-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53ec4-330">リソース割り当て</span><span class="sxs-lookup"><span data-stu-id="53ec4-330">Resource assignments</span></span></td>
<td><span data-ttu-id="53ec4-331">WBS の割り当てられたリソース、日付、時間数、およびタスクの予約タイプを表示します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-331">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53ec4-332">チームの自動生成</span><span class="sxs-lookup"><span data-stu-id="53ec4-332">Auto generate team</span></span></td>
<td><span data-ttu-id="53ec4-333">タスクに関連付けられるロールを使用して、計画されているリソースを自動的に追加します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-333">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="53ec4-334">Finance and Operations では、ロールに基づいた複数の条件による決定分析を使用して、計画されているリソースが自動的に提案されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-334">Finance and Operations automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="53ec4-335">WBS でタスクにロールおよび工数 (時間) を設定し、構造をリリースした後、[<strong>チームの自動生成</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-335">After the roles and effort (hours) have been set for the tasks in a WBS, and after the structure has been released, select <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="53ec4-336">計画されているリソースの必要数が、WBS と [<strong>プロジェクトとチームのスケジューリング</strong>] タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-336">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53ec4-337">リソース (ドロップダウン リスト)</span><span class="sxs-lookup"><span data-stu-id="53ec4-337">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="53ec4-338">[<strong>リソース割り当ての起動</strong>] ページで、特定期間に基づいて、確定予約または仮予約にリソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-338">On the <strong>Launch resource assignment</strong> page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="53ec4-339">ビュー設定を調整して、リソース活動の期間を表示および設定できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-339">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="53ec4-340">次のオプションを使用して、作業パッケージ レベルでリソースを選択して割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-340">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="53ec4-341">[<strong>承認</strong>] – タスクに割り当てられるリソースの変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-341"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="53ec4-342">[<strong>キャンセル</strong>] – タスクに割り当てられるリソースの変更をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="53ec4-342"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="53ec4-343"><strong>自動的に割り当て</strong> – 一致するロールが選択したタスクに自動的に選択され割り当てられる、使用できるスタッフ割り当て済リソースです。</span><span class="sxs-lookup"><span data-stu-id="53ec4-343"><strong>Assign automatically</strong> – An available staffed resource that has a matching role is automatically selected and assigned to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1. <span data-ttu-id="53ec4-344">[すべてのプロジェクト] ページで [XYZ アップグレード フェーズ 2] プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-344">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="53ec4-345">[計画] &gt; [活動] &gt; [作業分解構造] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-345">Select **Plan** &gt; **Activities** &gt; **Work breakdown structure**.</span></span>
3. <span data-ttu-id="53ec4-346">WBS に次のレベル 1 の活動を追加するには、[新規] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-346">Select **New** to add the following level-one activities to the WBS:</span></span>

    - <span data-ttu-id="53ec4-347">開始</span><span class="sxs-lookup"><span data-stu-id="53ec4-347">Initiating</span></span>
    - <span data-ttu-id="53ec4-348">計画</span><span class="sxs-lookup"><span data-stu-id="53ec4-348">Planning</span></span>
    - <span data-ttu-id="53ec4-349">実行中</span><span class="sxs-lookup"><span data-stu-id="53ec4-349">Executing</span></span>
    - <span data-ttu-id="53ec4-350">監視とコントロール</span><span class="sxs-lookup"><span data-stu-id="53ec4-350">Monitoring and Control</span></span>
    - <span data-ttu-id="53ec4-351">終了</span><span class="sxs-lookup"><span data-stu-id="53ec4-351">Close</span></span>

4. <span data-ttu-id="53ec4-352">次の図に示すように、日付と工数 (時間) を設定します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-352">Set the dates and effort (hours), as shown in the following illustration.</span></span>

    <span data-ttu-id="53ec4-353">[![日付と工数の設定](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="53ec4-353">[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>

5. <span data-ttu-id="53ec4-354">[開始] タスク明細行を選択し、[ロール] フィールドで、[上級プロジェクト マネージャ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-354">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
6. <span data-ttu-id="53ec4-355">[公開] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-355">Select **Publish**.</span></span>
7. <span data-ttu-id="53ec4-356">[リソース] フィールドの、同じ明細行で、[Daniel Goldschmidt] を選択し、それから [承認] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-356">On the same line, in the **Resource** field, select **Daniel Goldschmidt**, and then select **Accept**.</span></span>
8. <span data-ttu-id="53ec4-357">[計画] タスク明細行を選択し、次に、[ロール] フィールドで、[ビジネス アナリスト] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-357">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
9. <span data-ttu-id="53ec4-358">[公開] を選択し、[チームの自動生成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-358">Select **Publish**, and then select **Auto generate team**.</span></span>
10. <span data-ttu-id="53ec4-359">表示されるメッセージ ボックスで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-359">In the message box that appears, select **Yes**.</span></span>
11. <span data-ttu-id="53ec4-360">[リソース] フィールドで、値が [ビジネス アナリスト 1] であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-360">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
12. <span data-ttu-id="53ec4-361">[ビジネス アナリスト 1] リソースに、ルックアップを開き、[リソース割り当てフォームの起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-361">For the **Business analyst 1** resource, open the lookup, and select **Launch resource assignments**.</span></span> <span data-ttu-id="53ec4-362">次にタスクの作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-362">Then select a worker for the task.</span></span>
13. <span data-ttu-id="53ec4-363">[仮割り当て] &gt; [全能力] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-363">Select **Soft assign** &gt; **Full capacity**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="53ec4-364">指定されたリソースが現在 2 の場合、リソース数が 1 のままのため、警告は表示されません。</span><span class="sxs-lookup"><span data-stu-id="53ec4-364">You don't receive a warning that the specified resource is now 2, because the number of resources remains 1.</span></span>

14. <span data-ttu-id="53ec4-365">[作業分解構造] ページで、WBS のリソース割り当てを検証し、[保存] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-365">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then select **Save**.</span></span>

## <a name="resource-fulfillment-for-planned-resources"></a><span data-ttu-id="53ec4-366">計画されているリソースのリソースの履行</span><span class="sxs-lookup"><span data-stu-id="53ec4-366">Resource fulfillment for planned resources</span></span>
<span data-ttu-id="53ec4-367">プロジェクト マネージャは、プロジェクトの必要なリソース ロールを計画できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-367">A project manager can plan required resource roles for a project.</span></span> <span data-ttu-id="53ec4-368">リソース マネージャーは、[リソースの履行] ページで、これらの計画されているリソースを要求として参照し、実際のリソースを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-368">The resource manager will see these planned resources as requests on the **Resource fulfillment** page and can assign actual resources.</span></span>

1. <span data-ttu-id="53ec4-369">[すべてのプロジェクト] ページで [XYZ アップグレード フェーズ 2] プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-369">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="53ec4-370">[プロジェクト] を選択し、次に [編集] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-370">Select **Project**, and then select **Edit**.</span></span>
3. <span data-ttu-id="53ec4-371">[プロジェクト チームとスケジューリング] タブで、[追加] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-371">On the **Project team and scheduling** tab, select **Add**.</span></span>
4. <span data-ttu-id="53ec4-372">[ロールの追加] ダイアログ ボックスで、[ソフトウェア開発者] ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-372">In the **Add roles** dialog box, select the **Software developer** role.</span></span>
5. <span data-ttu-id="53ec4-373">[保存] を選択し、プロジェクト ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-373">Select **Create**, and then close the project page.</span></span>
6. <span data-ttu-id="53ec4-374">[リソースの履行] ページで、[XYZ アップグレード プロジェクト フェーズ 2] プロジェクトの [ソフトウェア開発者 1] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-374">On the **Resource fulfillment** page, select **Software developer 1** for the **XYZ Upgrade project Phase 2** project.</span></span>
7. <span data-ttu-id="53ec4-375">作業者を選択し、[割り当て] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-375">Select a worker, and then select **Assign**.</span></span>
8. <span data-ttu-id="53ec4-376">[ソフトウェア開発者 1] の明細行が、[XYZ アップグレード プロジェクト フェーズ 2] プロジェクトに対して削除されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-376">Verify that the line for **Software developer 1** has been removed for the **XYZ Upgrade project Phase 2** project.</span></span>
9. <span data-ttu-id="53ec4-377">[プロジェクト チームとスケジューリング] タブで、[XYZ アップグレード フェーズ 2] プロジェクトに対して、以前のステップで選択した作業者が、[ソフトウェア開発者] として追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-377">On the **Project team and scheduling** tab, for the **XYZ Upgrade Phase 2** project, verify that the worker that you selected in the previous step has been added as **Software developer**.</span></span>

## <a name="requests-for-project-resources"></a><span data-ttu-id="53ec4-378">プロジェクト リソースの依頼</span><span class="sxs-lookup"><span data-stu-id="53ec4-378">Requests for project resources</span></span>
<span data-ttu-id="53ec4-379">プロジェクト リソースのスケジューリングの機能は、リソース マネージャーが、エンゲージメントまたはプロジェクトのスタッフ割り当て済リソースを配分するようにするだけです。</span><span class="sxs-lookup"><span data-stu-id="53ec4-379">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="53ec4-380">この機能を有効にするには、次のタスクを行うか、または完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-380">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="53ec4-381">番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-381">Set up number sequences.</span></span>
- <span data-ttu-id="53ec4-382">プロジェクト管理および会計のワークフローを設定します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-382">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="53ec4-383">リソース要求ワークフローの有効化</span><span class="sxs-lookup"><span data-stu-id="53ec4-383">Enable resource request workflows.</span></span>

<span data-ttu-id="53ec4-384">前述のタスクが完了した後、必要に応じて、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="53ec4-384">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="53ec4-385">仮予約されたスタッフ割り当て済リソースのリソース要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-385">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="53ec4-386">リソース要求の監視</span><span class="sxs-lookup"><span data-stu-id="53ec4-386">Monitor resource requests.</span></span>
- <span data-ttu-id="53ec4-387">リソース要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-387">Fulfill resource requests.</span></span>
- <span data-ttu-id="53ec4-388">WBS からスタッフ割り当て済リソースを要求します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-388">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="53ec4-389">スタッフ割り当て済のリソースの要求なしでリソースをプロジェクトに予約します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-389">Book resources to a project without having a request for a staffed resource.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="53ec4-390">プロジェクト チームの監視</span><span class="sxs-lookup"><span data-stu-id="53ec4-390">Monitor project teams</span></span>
1. <span data-ttu-id="53ec4-391">[すべてのプロジェクト] ページで、[XYZ アップグレード フェーズ 2] プロジェクトに対し [プロジェクト ID] リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-391">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="53ec4-392">[プロジェクト チームとスケジューリング] クイック タブで、一覧表示されたプロジェクト リソースが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ec4-392">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>

