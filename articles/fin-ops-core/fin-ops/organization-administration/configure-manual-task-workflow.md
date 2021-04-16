---
title: ワークフローでの手動タスクのコンフィギュレーション
description: このトピックでは、手動タスクのプロパティをコンフィギュレーションする方法について説明します。
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4be7f0ee5e487185033b7ccb9a2b0a91eb4a36c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747858"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="2c602-103">ワークフローでの手動タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2c602-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c602-104">このトピックでは、手動タスクのプロパティをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c602-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="2c602-105">ワークフロー エディターで手動タスクをコンフィギュレーションするには、タスクを右クリックし、**プロパティ** をクリックして、**プロパティ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="2c602-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2c602-106">それから次の手順に従って、手動タスクのプロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2c602-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="2c602-107">タスクに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="2c602-107">Name the task</span></span>

<span data-ttu-id="2c602-108">手動タスクの名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="2c602-109">左ウィンドウで **基本設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2c602-110">**名前** フィールドに、タスクの固有名を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="2c602-111">件名行と指示を入力する</span><span class="sxs-lookup"><span data-stu-id="2c602-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="2c602-112">タスクに割り当てられるユーザーに対して件名行と指示を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c602-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="2c602-113">たとえば、購買要求のタスクをコンフィギュレーションする場合には、そのタスクに割り当てられるユーザーに対して、**購買要求** ページの件名行と指示が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2c602-114">件名行はページのメッセージ バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="2c602-115">ユーザーは、その後、メッセージ バーのアイコンをクリックして、指示を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="2c602-116">次に手順に従って、件名行と指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="2c602-117">左ウィンドウで **基本設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2c602-118">**作業項目の件名** フィールドで、件名行を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="2c602-119">件名行をカスタマイズするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="2c602-120">プレースホルダーは、件名行がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="2c602-121">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2c602-122">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2c602-123">**プレースホルダーの挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2c602-124">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2c602-125">**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-125">Click **Insert**.</span></span>

4. <span data-ttu-id="2c602-126">件名行の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="2c602-127">**翻訳** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="2c602-128">表示されるページで、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2c602-129">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2c602-130">**翻訳テキスト** フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2c602-131">テキストをカスタマイズする場合は、ステップ 3 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="2c602-132">**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-132">Click **Close**.</span></span>

5. <span data-ttu-id="2c602-133">**作業項目の指示** フィールドで、指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="2c602-134">指示を個人向けのものにするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2c602-135">プレースホルダーは、指示行がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2c602-136">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2c602-137">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2c602-138">**プレースホルダーの挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2c602-139">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2c602-140">**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-140">Click **Insert**.</span></span>

7. <span data-ttu-id="2c602-141">指示行の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="2c602-142">**翻訳** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="2c602-143">表示されるページで、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2c602-144">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2c602-145">**翻訳テキスト** フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2c602-146">テキストをカスタマイズする場合は、ステップ 6 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="2c602-147">**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="2c602-148">タスクを割り当てる</span><span class="sxs-lookup"><span data-stu-id="2c602-148">Assign the task</span></span>

<span data-ttu-id="2c602-149">手動タスクの割り当て先のユーザーを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="2c602-150">左ウィンドウで、**割り当て** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="2c602-151">**割り当てタイプ** タブで、次の表のいずれかのオプションを選択し、オプションの追加手順を実行してから、手順 3 に進みます。</span><span class="sxs-lookup"><span data-stu-id="2c602-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2c602-152">オプション</span><span class="sxs-lookup"><span data-stu-id="2c602-152">Option</span></span></th>
    <th><span data-ttu-id="2c602-153">タスクの割り当て先のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="2c602-154">追加手順</span><span class="sxs-lookup"><span data-stu-id="2c602-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2c602-155">参加者</span><span class="sxs-lookup"><span data-stu-id="2c602-155">Participant</span></span></td>
    <td><span data-ttu-id="2c602-156">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-157"><strong>参加者のタイプ</strong> 一覧の <strong>ロール ベース</strong> タブの、<strong>参加者</strong> を選択したのち、タスクの割り当て先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="2c602-158"><strong>参加者</strong> の一覧で、タスクの割り当て先のグループまたはロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-159">階層</span><span class="sxs-lookup"><span data-stu-id="2c602-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="2c602-160">特定の組織階層内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-161"><strong>階層タイプ</strong> 一覧の <strong>階層選択</strong> タブの、<strong>階層</strong> を選択したのち、タスクの割り当て先の階層タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="2c602-162">システムは、一定範囲のユーザー名を階層から取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c602-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2c602-163">これらの名前は、タスクを割り当てることができるユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="2c602-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="2c602-164">システムで取得するユーザー名の範囲について、その開始点と終了点を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2c602-165">開始点を指定するには、<strong>開始</strong> 一覧から人物を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2c602-166">終了点を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2c602-167">次に、階層のどこで名前の取得を止めるかを示す条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2c602-168"><strong>階層オプション</strong> で、タスクを割り当てる範囲内のユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c602-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="2c602-169"><strong>取得したすべてのユーザーに割り当てる</strong> – タスクは範囲内のすべてのユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="2c602-170"><strong>取得した最後のユーザーのみに割り当てる</strong> – タスクは、範囲内の最後のユーザーのみに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2c602-171"><strong>次の条件のユーザーを除外します</strong> – タスクは、特定の条件に該当する範囲内のユーザーには割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="2c602-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="2c602-172">条件を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-173">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-173">Workflow user</span></span></td>
    <td><span data-ttu-id="2c602-174">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2c602-175"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-176">ユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-176">User</span></span></td>
    <td><span data-ttu-id="2c602-177">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-178"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2c602-179"><strong>利用可能なユーザー</strong>の一覧には、すべてのユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2c602-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2c602-180">タスクを割り当てるユーザーを選択し、そのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="2c602-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-181">キュー</span><span class="sxs-lookup"><span data-stu-id="2c602-181">Queue</span></span></td>
    <td><span data-ttu-id="2c602-182">作業項目キュー</span><span class="sxs-lookup"><span data-stu-id="2c602-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-183"><strong>キュー</strong> を選択した後、<strong>キュー ベース</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="2c602-184">タスクを特定のキューに割り当てるには、次の手順に従います。:</span><span class="sxs-lookup"><span data-stu-id="2c602-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2c602-185"><strong>キュー タイプ</strong> 一覧で、<strong>作業項目キュー</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2c602-186"><strong>キュー名</strong> の一覧でキューを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2c602-187">タスクを割り当てるキューを特定の条件で決定する場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="2c602-188"><strong>キュー タイプ</strong> 一覧で、<strong>条件付き作業項目キュー</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="2c602-189"><strong>キュー名</strong> の一覧で、<strong>条件付きキュー</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="2c602-190">このオプションは、ケース管理などのいくつかのワークフローのみで使用されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="2c602-191">**期限** タブの、**期間** フィールドで、ユーザーがタスクを完了するのに必要とする期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c602-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="2c602-192">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-192">Select one of the following options:</span></span>

    - <span data-ttu-id="2c602-193">**時間** – ユーザーがタスクを完了するのに必要とする期間を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="2c602-194">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2c602-195">**日** – ユーザーがタスクを完了するのに必要とする期間を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="2c602-196">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2c602-197">**週** – ユーザーがタスクを完了するのに必要とする期間を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="2c602-198">**月** – ユーザーがタスクを完了する必要のある期限を、曜日、週で選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="2c602-199">たとえば、当月の第 3 週の金曜日までにタスクを完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2c602-200">**年** – ユーザーがタスクを完了する必要のある期限を、曜日、週、月で選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="2c602-201">たとえば、12 月の第 3 週の金曜日までにタスクを完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="2c602-202">割り当てられている時間内にユーザーがタスクを完了しなかった場合、タスクは期限超過になります。</span><span class="sxs-lookup"><span data-stu-id="2c602-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="2c602-203">期限超過のタスクは、このページの **エスカレーション** 領域で選択したオプションに基づいて、エスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="2c602-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="2c602-204">タスクが期限超過の場合の処置を指定する</span><span class="sxs-lookup"><span data-stu-id="2c602-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="2c602-205">割り当てられている時間内にユーザーが手動タスクを完了しなかった場合、タスクは期限超過になります。</span><span class="sxs-lookup"><span data-stu-id="2c602-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="2c602-206">期限超過したタスクは、別のユーザーにエスカレートする (自動的に割り当てる) ことができます。</span><span class="sxs-lookup"><span data-stu-id="2c602-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="2c602-207">期限超過したタスクをエスカレートするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="2c602-208">左ウィンドウで、**エスカレーション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="2c602-209">**エスカレーション パスを使用** チェック ボックスをオンにし、エスカレーション パスを作成します。</span><span class="sxs-lookup"><span data-stu-id="2c602-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="2c602-210">タスクは、エスカレーション パスにリストされるユーザーに自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="2c602-211">たとえば、次の表に、エスカレーション パスを示します。</span><span class="sxs-lookup"><span data-stu-id="2c602-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="2c602-212">順番</span><span class="sxs-lookup"><span data-stu-id="2c602-212">Sequence</span></span> | <span data-ttu-id="2c602-213">エスカレーション パス</span><span class="sxs-lookup"><span data-stu-id="2c602-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="2c602-214">1</span><span class="sxs-lookup"><span data-stu-id="2c602-214">1</span></span>        | <span data-ttu-id="2c602-215">割り当て先: 奈緒美</span><span class="sxs-lookup"><span data-stu-id="2c602-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="2c602-216">2</span><span class="sxs-lookup"><span data-stu-id="2c602-216">2</span></span>        | <span data-ttu-id="2c602-217">割り当て先: 悦子</span><span class="sxs-lookup"><span data-stu-id="2c602-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="2c602-218">3</span><span class="sxs-lookup"><span data-stu-id="2c602-218">3</span></span>        | <span data-ttu-id="2c602-219">最終アクション: 拒否</span><span class="sxs-lookup"><span data-stu-id="2c602-219">Final action: Reject</span></span> |

    <span data-ttu-id="2c602-220">この例では、奈緒美に、期限超過のタスクが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="2c602-221">割り当てられた時間内に奈緒美がタスクを実行しない場合は、悦子にタスクが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="2c602-222">割り当て時間内に悦子がタスクを実行しない場合、処理のために送信されたドキュメントがシステムによって却下されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="2c602-223">エスカレーション パスにユーザーを追加するには、**エスカレーションの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="2c602-224">**割り当てタイプ** タブで、次の表のいずれかのオプションを選択し、オプションの追加手順を実行してから、ステップ 4 に進みます。</span><span class="sxs-lookup"><span data-stu-id="2c602-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2c602-225">オプション</span><span class="sxs-lookup"><span data-stu-id="2c602-225">Option</span></span></th>
    <th><span data-ttu-id="2c602-226">タスクのエスカレート先のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="2c602-227">追加手順</span><span class="sxs-lookup"><span data-stu-id="2c602-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2c602-228">階層</span><span class="sxs-lookup"><span data-stu-id="2c602-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="2c602-229">特定の組織階層内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-230"><strong>階層タイプ</strong> 一覧の <strong>階層選択</strong> タブの、<strong>階層</strong> を選択したのち、タスクのエスカレート先の階層タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="2c602-231">システムは、一定範囲のユーザー名を階層から取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c602-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2c602-232">これらの名前は、タスクをエスカレートできるユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="2c602-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="2c602-233">システムで取得するユーザー名の範囲について、その開始点と終了点を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2c602-234">開始点を指定するには、<strong>開始</strong> 一覧から人物を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2c602-235">終了点を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2c602-236">次に、階層のどこで名前の取得を止めるかを示す条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2c602-237"><strong>階層オプション</strong> で、タスクをエスカレートできる範囲内のユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c602-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="2c602-238"><strong>取得したすべてのユーザーに割り当てる</strong> – タスクは範囲内のすべてのユーザーにエスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="2c602-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="2c602-239"><strong>取得した最後のユーザーのみに割り当てる</strong> – タスクは、範囲内の最後のユーザーのみにエスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="2c602-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2c602-240"><strong>次の条件のユーザーを除外します</strong> – タスクは、特定の条件に該当する範囲内のユーザーにはエスカレートされません。</span><span class="sxs-lookup"><span data-stu-id="2c602-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="2c602-241">条件を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-242">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-242">Workflow user</span></span></td>
    <td><span data-ttu-id="2c602-243">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2c602-244"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-245">ユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-245">User</span></span></td>
    <td><span data-ttu-id="2c602-246">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-247"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2c602-248"><strong>利用可能なユーザー</strong>の一覧には、すべてのユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2c602-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2c602-249">タスクをエスカレートするユーザーを選択し、そのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="2c602-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="2c602-250">**期限** タブの、**期間** フィールドで、ユーザーがタスクを完了するのに必要とする期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c602-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="2c602-251">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-251">Select one of the following options:</span></span>

    - <span data-ttu-id="2c602-252">**時間** – ユーザーがタスクを完了するのに必要とする期間を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="2c602-253">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2c602-254">**日** – ユーザーがタスクを完了するのに必要とする期間を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="2c602-255">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2c602-256">**週** – ユーザーがタスクを完了するのに必要とする期間を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="2c602-257">**月** – ユーザーがタスクを完了する必要のある期限を、曜日、週で選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="2c602-258">たとえば、当月の第 3 週の金曜日までにタスクを完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2c602-259">**年** – ユーザーがタスクを完了する必要のある期限を、曜日、週、月で選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="2c602-260">たとえば、12 月の第 3 週の金曜日までにタスクを完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="2c602-261">エスカレーション パスに追加するユーザーごとに、ステップ 3～4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="2c602-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="2c602-262">ユーザーの順序は、変更できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="2c602-263">エスカレーション パスに含まれるユーザーが、割り当てられた時間内にタスクを完了しない場合、システムによってタスクが処理されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="2c602-264">システムによる処理を指定するには、**アクション** 行を選択し、**アクションの終了** タブでアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="2c602-265">タスクをシステムで自動的に処理する条件を指定する</span><span class="sxs-lookup"><span data-stu-id="2c602-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="2c602-266">特定の条件が満たされたときに、手動タスクをシステムで処理するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="2c602-267">たとえば、あるタスクでは、経費精算書と共に提出された領収書を経費精算書部門のメンバーが確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c602-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="2c602-268">会社のポリシーに従うと、このタスクは、経費精算書の合計金額が USD 100 を超える場合に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c602-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="2c602-269">このシナリオでは、合計金額 < 100 の場合に、**完了** のマークを自動的にタスクに付けるよう、システムをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="2c602-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="2c602-270">手動タスクをシステムによって処理する条件を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="2c602-271">左ウィンドウで、**自動アクション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="2c602-272">**自動アクションの有効化** を選択し、チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="2c602-273">**条件の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="2c602-274">条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-274">Enter a condition.</span></span>
5. <span data-ttu-id="2c602-275">必要に応じて、追加条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="2c602-276">入力した条件が正しくコンフィギュレーションされていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2c602-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="2c602-277">**テスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-277">Click **Test**.</span></span>
    2. <span data-ttu-id="2c602-278">**ワークフロー条件のテスト** ページで、**条件の検証** 領域で、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="2c602-279">**テスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-279">Click **Test**.</span></span> <span data-ttu-id="2c602-280">システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="2c602-281">**OK**、または **キャンセル** をクリックして、**プロパティ** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="2c602-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="2c602-282">**自動完了アクション** 一覧で、タスクに対してシステムが実行するアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="2c602-283">いつ通知を送信するかを指定する</span><span class="sxs-lookup"><span data-stu-id="2c602-283">Specify when notifications are sent</span></span>

<span data-ttu-id="2c602-284">手動タスクが委任、エスカレート、完了、否認されたとき、または変更が依頼されたときに、ユーザーに通知を送信できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="2c602-285">通知の送信条件と、通知の送信先のユーザーを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="2c602-286">左ウィンドウで、**通知** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="2c602-287">通知を送信するイベントの横にあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="2c602-288">**委任** – タスクは他のユーザーに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="2c602-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="2c602-289">**エスカレート** – 割り当てられたユーザーは、割り当て時間内にタスクを完了していません。</span><span class="sxs-lookup"><span data-stu-id="2c602-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="2c602-290">**完了** – 割り当てられたユーザーがタスクを完了しました。</span><span class="sxs-lookup"><span data-stu-id="2c602-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="2c602-291">**拒否** – 割り当てられたユーザーが提出されたドキュメントを否認しました。</span><span class="sxs-lookup"><span data-stu-id="2c602-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="2c602-292">**変更依頼** – 割り当てられたユーザーが、提出されたドキュメントの変更を依頼しました。</span><span class="sxs-lookup"><span data-stu-id="2c602-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="2c602-293">手順 2. で選択したイベントの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="2c602-294">**通知テキスト** タブのテキスト ボックス内で、通知のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="2c602-295">通知を個人向けのものにするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="2c602-296">プレースホルダーは、通知がユーザーに表示されるときに、適切な情報に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2c602-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="2c602-297">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2c602-298">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2c602-299">**プレースホルダーの挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2c602-300">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2c602-301">**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-301">Click **Insert**.</span></span>

6. <span data-ttu-id="2c602-302">通知の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="2c602-303">**翻訳** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="2c602-304">表示されるページで、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2c602-305">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2c602-306">**翻訳テキスト** フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2c602-307">テキストをカスタマイズする場合は、ステップ 5 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2c602-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="2c602-308">**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-308">Click **Close**.</span></span>

7. <span data-ttu-id="2c602-309">**受信者** タブで、通知の送信先ユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c602-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="2c602-310">次の表のいずれかのオプションを選択し、オプションの追加ステップを実行してから、ステップ 8 に進みます。</span><span class="sxs-lookup"><span data-stu-id="2c602-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2c602-311">オプション</span><span class="sxs-lookup"><span data-stu-id="2c602-311">Option</span></span></th>
    <th><span data-ttu-id="2c602-312">通知の受信者</span><span class="sxs-lookup"><span data-stu-id="2c602-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="2c602-313">追加手順</span><span class="sxs-lookup"><span data-stu-id="2c602-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2c602-314">参加者</span><span class="sxs-lookup"><span data-stu-id="2c602-314">Participant</span></span></td>
    <td><span data-ttu-id="2c602-315">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-316"><strong>参加者のタイプ</strong> 一覧の <strong>ロール ベース</strong> タブの、<strong>参加者</strong> を選択したのち、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="2c602-317"><strong>参加者</strong> の一覧で、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-318">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-318">Workflow user</span></span></td>
    <td><span data-ttu-id="2c602-319">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2c602-320"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2c602-321">ユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-321">User</span></span></td>
    <td><span data-ttu-id="2c602-322">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="2c602-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2c602-323"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2c602-324"><strong>利用可能なユーザー</strong>の一覧には、すべてのユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2c602-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2c602-325">通知の送信先のユーザーを選択して、それらのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="2c602-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="2c602-326">ステップ 2 で選択したイベントごとに、ステップ 3～7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="2c602-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="2c602-327">期限の設定</span><span class="sxs-lookup"><span data-stu-id="2c602-327">Set a time limit</span></span>

<span data-ttu-id="2c602-328">手動タスクを特定の時間内に完了する必要がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="2c602-329">この手順で選択するオプションは、このページの **割り当て**、および **エスカレーション** 領域で選択されたオプションよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="2c602-330">左ウィンドウで **詳細設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="2c602-331">**ワークフロー要素の期限の設定** を選択し、チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="2c602-332">**期間** フィールドで、このタスクをいつまでに完了する必要があるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c602-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="2c602-333">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-333">Select one of the following options:</span></span>

    - <span data-ttu-id="2c602-334">**時間** – タスクの完了期限を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="2c602-335">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2c602-336">**日数** – このタスクの完了期限を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="2c602-337">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2c602-338">**週** – タスクの完了期限を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2c602-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="2c602-339">**月** – タスクの完了期限を曜日、週で選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="2c602-340">たとえば、当月の第 3 週の金曜日までにタスクを完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2c602-341">**年** – タスクの完了期限を曜日、週、月で選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="2c602-342">たとえば、12 月の第 3 週の金曜日までにタスクを完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="2c602-343">時間制限を超過した場合は、システムによってタスクが処理されます。</span><span class="sxs-lookup"><span data-stu-id="2c602-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="2c602-344">**アクション** の一覧で、システムで実行するアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c602-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="2c602-345">ユーザーが実行可能なアクションを指定する</span><span class="sxs-lookup"><span data-stu-id="2c602-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="2c602-346">手動タスクがあるユーザーに割り当てられた場合、そのユーザーはタスクを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c602-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="2c602-347">タスクに対してユーザーが実行できるアクションを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c602-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="2c602-348">実行可能なアクションは、タスクの設計方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2c602-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="2c602-349">左ウィンドウで **詳細設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c602-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="2c602-350">ユーザーが **完了** マークをタスクに付けられるようにするには、**完了** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="2c602-351">ユーザーが提出されたドキュメントを否認できるようにするには、**拒否** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="2c602-352">ユーザーが提出されたドキュメントに対して変更を依頼できるようにするには、**変更依頼** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="2c602-353">ユーザーがタスクを別のユーザーに割り当てることができるようにするには、**委任** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="2c602-354">ユーザーが作業項目キューの他のユーザーにタスクを割り当て直すことができるようにするには、**再割り当て** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="2c602-355">ユーザーが作業項目キューにタスクを割り当て直すことができるようにするには、**リリース** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2c602-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="2c602-356">すると、別のユーザーがタスクを完了できます。</span><span class="sxs-lookup"><span data-stu-id="2c602-356">Another user can then complete the task.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]