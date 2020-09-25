---
title: プロジェクト リソースを設定します
description: このトピックでは、プロジェクト リソースの設定または要求に関する情報を提供します。
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760598"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="d31e4-103">プロジェクト リソースを設定します</span><span class="sxs-lookup"><span data-stu-id="d31e4-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d31e4-104">カレンダーを設定したり、従業員または作業者に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="d31e4-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="d31e4-105">このカレンダーは、プロジェクトおよびプロジェクトに引き当てられているリソースの作業時間をスケジュールするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="d31e4-106">カレンダーの設定時に、プロジェクト マネージャはリソースの最適化の一部として、リソースを平準化できます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="d31e4-107">カレンダー スケジュールに基づいて、制限をリソースに置くことができます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="d31e4-108">**カレンダー** ページでカレンダーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="d31e4-109">プロジェクト リソースとして作業者を設定する場合は、リソースを設定している会社で勤務する作業者から選択できます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="d31e4-110">また、組織内の他の会社から作業者を選択できます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="d31e4-111">これらの作業者は、会社間リソースと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="d31e4-112">次の手順では、会社内のプロジェクト リソースとして作業を設定する方法、会社間プロジェクト リソースの設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="d31e4-113">プロジェクト リソースとして作業者を設定</span><span class="sxs-lookup"><span data-stu-id="d31e4-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="d31e4-114">**作業者**ページの**作業者**リストで、プロジェクト リソースとして追加する作業者を選択し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="d31e4-115">[アクション ウィンドウ] で、**プロジェクト** &gt; **設定** &gt; **プロジェクトの設定**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="d31e4-116">カレンダーを選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="d31e4-117">また、リソースの既定のプロジェクトを前の割り当てのタイプとして指定できます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="d31e4-118">前の割り当ては、リソース マネージャーまたはプロジェクト マネージャが、使用されるプロジェクトのリソースを事前にわかっている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="d31e4-119">前の割り当ては、プロジェクトのスポンサーまたは顧客の要求に基づくものとすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="d31e4-120">プロジェクトを前の割り当てとするには、**残りのプロジェクト**リストの、**プロジェクト**タブの、**プロジェクトの割り当て**ページで、適切なプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="d31e4-121">会社間リソースの設定</span><span class="sxs-lookup"><span data-stu-id="d31e4-121">Set up an intercompany resource</span></span>

<span data-ttu-id="d31e4-122">会社間リソースとして作業者を設定する場合、貸与の会社と借入の会社両方の設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d31e4-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="d31e4-123">貸与の会社では</span><span class="sxs-lookup"><span data-stu-id="d31e4-123">In the lending company</span></span>

1. <span data-ttu-id="d31e4-124">Finance では、貸与の会社が選択されていることを確認し、前のセクションでの手順、「プロジェクト リソースとして作業者を設定する」を完了させます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="d31e4-125">**会社間会計**ページで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="d31e4-126">**法人 ID** フィールドで、貸与の会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="d31e4-127">必要に応じて残りのフィールドに入力し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="d31e4-128">**移転価格**ページで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="d31e4-129">**借入側の法人**フィールドで、適切な会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="d31e4-130">借入の会社に、このセクションの最初に作成したリソースのみを貸与する場合は、**リソース**フィールドで、作成したリソースの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="d31e4-131">借入の会社に対して、貸与の会社でのすべてのリソースを使用できるようにするには、**リソース**フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="d31e4-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="d31e4-132">**会社間**タブの**プロジェクト管理および会計パラメータ**ページで、**会社間リソースのスケジューリングやタイムシートを有効にする**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="d31e4-133">借入の会社では</span><span class="sxs-lookup"><span data-stu-id="d31e4-133">In the borrowing company</span></span>

- <span data-ttu-id="d31e4-134">**リソース リスト**ページで、貸与会社の作成されたリソース名を検索フィルターに入力して、借入会社のリソースの一覧に名前が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="d31e4-135">プロジェクト リソースの要求</span><span class="sxs-lookup"><span data-stu-id="d31e4-135">Request project resources</span></span>
<span data-ttu-id="d31e4-136">プロジェクト リソースのスケジューリングの機能は、リソース マネージャーが、エンゲージメントまたはプロジェクトのスタッフ割り当て済リソースを配分するようにするだけです。</span><span class="sxs-lookup"><span data-stu-id="d31e4-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="d31e4-137">この機能を有効にするには、次のタスクを行うか、または完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="d31e4-138">番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-138">Set up number sequences.</span></span>
- <span data-ttu-id="d31e4-139">プロジェクト管理および会計のワークフローを設定します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="d31e4-140">リソース要求ワークフローの有効化</span><span class="sxs-lookup"><span data-stu-id="d31e4-140">Enable resource request workflows.</span></span>

<span data-ttu-id="d31e4-141">前述のタスクが完了した後、必要に応じて、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d31e4-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="d31e4-142">仮予約されたスタッフ割り当て済リソースのリソース要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="d31e4-143">リソース要求の監視</span><span class="sxs-lookup"><span data-stu-id="d31e4-143">Monitor resource requests.</span></span>
- <span data-ttu-id="d31e4-144">リソース要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="d31e4-145">WBS からスタッフ割り当て済リソースを要求します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="d31e4-146">スタッフ割り当て済のリソースの要求なしでリソースをプロジェクトに予約します。</span><span class="sxs-lookup"><span data-stu-id="d31e4-146">Book resources to a project without having a request for a staffed resource.</span></span>
