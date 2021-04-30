---
title: Microsoft Teams と Dynamics 365 Commerce POS 間でタスク管理を同期させる
description: このトピックでは、Microsoft Teams と Dynamics 365 Commerce の販売時点管理 (POS) の間で同期する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b4a9ad561e3bff67720a08d6e4184a81e01f734
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908272"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="9b8cb-103">Microsoft Teams と Dynamics 365 Commerce POS 間でタスク管理を同期させる</span><span class="sxs-lookup"><span data-stu-id="9b8cb-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9b8cb-104">このトピックでは、Microsoft Teams と Dynamics 365 Commerce の販売時点管理 (POS) の間で同期する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="9b8cb-105">Teams 統合の主な目的の1つは、POS アプリケーションとチーム間でのタスク管理の同期を有効に行う目的の1つです。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="9b8cb-106">店舗の従業員は、POS アプリケーションまたはチームを使用してタスクを管理し、アプリケーションを切り替える必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="9b8cb-107">Planner はチームのタスクのリポジトリとして使用されるので、Teams と Dynamics 365 Commerce の間にリンクがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="9b8cb-108">このリンクは、特定の店舗チームの特定の計画 ID を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="9b8cb-109">次の手順では、POS アプリケーションと Teams アプリケーション間のタスク管理同期を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="9b8cb-110">Teams でのテストタスク リストの公開</span><span class="sxs-lookup"><span data-stu-id="9b8cb-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="9b8cb-111">次の手順は、店舗チームが初めて Commerce と Microsoft Teams タスク管理統合を使用している場合と仮定しています。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="9b8cb-112">Teams でテスト タスク リストを公開するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="9b8cb-113">Teams は通信マネージャーとしてサインインします。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="9b8cb-114">通常、通信マネージャは、Commerce で **地域マネージャー** ロールを持つユーザーです。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="9b8cb-115">左のナビゲーション ペインで、**Planner によるタスク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="9b8cb-116">**発行済みリスト** タブで、左下の **新規リスト** を選択し、新しいリストに **テスト タスク リスト** と指定します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="9b8cb-117">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-117">Select **Create**.</span></span> <span data-ttu-id="9b8cb-118">新しいリストは **ドラフト** の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="9b8cb-119">**タスク タイトル** で、最初のタスクに **Teams 統合のテスト** というタイトルを付けます。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="9b8cb-120">**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="9b8cb-121">**ドラフト** リストで、タスク リストを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="9b8cb-122">次に右上隅で  **発行**   を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="9b8cb-123">**発行先の選択** ダイアログ ボックス で、テストタスク リストを受け取るチームを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="9b8cb-124">**次へ** を選択すると、出版物計画が確認されます。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="9b8cb-125">変更する必要がある場合は、 **戻る** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="9b8cb-126">**確認を選択して続行** を選択して、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="9b8cb-127">発行が完了した後に、**発行済リスト** タブの上部に表示されるメッセージに、タスク リストが正常に 配信されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="9b8cb-128">詳細については、[組織の作業を作成および追跡するためのタスク リストの公開](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="9b8cb-129">POS とタスク管理のための Teams のリンク</span><span class="sxs-lookup"><span data-stu-id="9b8cb-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="9b8cb-130">Commerce Headquarters でタスク管理用の POS と Microsoft Teams アプリケーションをリンクするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9b8cb-131">**Commerce \> タスク管理 \> Microsoft Teams とのタスク統合** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="9b8cb-132">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9b8cb-133">**タスク管理統合の有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="9b8cb-134">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9b8cb-135">アクション ペインで、**タスク管理の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="9b8cb-136">**Teams のプロビジョニング** という名前のバッチ ジョブが作成中であることを示す通知 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="9b8cb-137">**システム管理 \> 照会 \> バッチジョブ** に移動し、**Teams のプロビジョニング** の説明がある最新のジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="9b8cb-138">このジョブの実行が終了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="9b8cb-139">**CDX ジョブ 1070** を実行して、計画 ID と Retail Server への店舗参照を公開します。</span><span class="sxs-lookup"><span data-stu-id="9b8cb-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b8cb-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9b8cb-140">Additional resources</span></span>

[<span data-ttu-id="9b8cb-141">Dynamics 365 Commerce と Microsoft Teams データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="9b8cb-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="9b8cb-142">Dynamics 365 Commerce と Microsoft Teams の統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="9b8cb-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="9b8cb-143">Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="9b8cb-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="9b8cb-144">Microsoft Teams でユーザーとロールを管理する</span><span class="sxs-lookup"><span data-stu-id="9b8cb-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="9b8cb-145">Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします</span><span class="sxs-lookup"><span data-stu-id="9b8cb-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="9b8cb-146">Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="9b8cb-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
