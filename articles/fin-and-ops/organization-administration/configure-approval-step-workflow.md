---
title: "ワークフローでの承認ステップのコンフィギュレーション"
description: "このトピックでは、承認ステップのプロパティをコンフィギュレーションする方法について説明します。"
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 8f52b6ffed7c1edb97c7a673cefbc8bf486ba831
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="38757-103">ワークフローでの承認ステップのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="38757-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38757-104">このトピックでは、承認ステップのプロパティをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="38757-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="38757-105">ワークフロー エディターで承認ステップを設定するには、承認ステップを右クリックし、**プロパティ**をクリックして、**プロパティ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="38757-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="38757-106">それから承認ステップのプロパティをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="38757-107">ステップに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="38757-107">Name the step</span></span>
<span data-ttu-id="38757-108">承認ステップの名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="38757-109">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="38757-110">**名前**フィールドに、承認ステップの固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="38757-111">件名行と指示を入力する</span><span class="sxs-lookup"><span data-stu-id="38757-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="38757-112">この承認ステップに割り当てられるユーザーに対して件名行と指示を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38757-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="38757-113">たとえば、購買要求の承認ステップをコンフィギュレーションする場合には、そのステップに割り当てられるユーザーに対して、**購買要求**ページの件名行と指示が表示されます。</span><span class="sxs-lookup"><span data-stu-id="38757-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="38757-114">件名行はページのメッセージ バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="38757-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="38757-115">ユーザーはメッセージ バーのアイコンをクリックすることで、指示を表示できます。</span><span class="sxs-lookup"><span data-stu-id="38757-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="38757-116">次に手順に従って、件名行と指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="38757-117">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="38757-118">**作業項目の件名**フィールドで、件名行を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="38757-119">件名行をカスタマイズするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="38757-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="38757-120">プレースホルダーは、件名行がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="38757-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="38757-121">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="38757-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="38757-122">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="38757-123">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="38757-124">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="38757-125">**挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-125">Click **Insert**.</span></span>

4. <span data-ttu-id="38757-126">件名行の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="38757-127">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="38757-128">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="38757-129">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="38757-130">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="38757-131">テキストをカスタマイズする場合は、ステップ 3 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="38757-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="38757-132">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-132">Click **Close**.</span></span>

5. <span data-ttu-id="38757-133">**作業項目の指示**フィールドで、指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="38757-134">指示を個人向けのものにするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="38757-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="38757-135">プレースホルダーは、指示行がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="38757-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="38757-136">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="38757-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="38757-137">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="38757-138">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="38757-139">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="38757-140">**挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-140">Click **Insert**.</span></span>

7. <span data-ttu-id="38757-141">指示行の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="38757-142">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="38757-143">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="38757-144">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="38757-145">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="38757-146">テキストをカスタマイズする場合は、ステップ 6 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="38757-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="38757-147">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="38757-148">承認ステップを割り当てる</span><span class="sxs-lookup"><span data-stu-id="38757-148">Assign the approval step</span></span>

<span data-ttu-id="38757-149">承認ステップの割り当て先のユーザーを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="38757-150">左ウィンドウで、**割り当て**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="38757-151">**割り当てタイプ**タブで、次の表のいずれかのオプションを選択し、オプションの追加手順を実行してから、手順 3 に進みます。</span><span class="sxs-lookup"><span data-stu-id="38757-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="38757-152">オプション</span><span class="sxs-lookup"><span data-stu-id="38757-152">Option</span></span></th>
    <th><span data-ttu-id="38757-153">承認ステップが割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="38757-154">追加手順</span><span class="sxs-lookup"><span data-stu-id="38757-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="38757-155">参加者</span><span class="sxs-lookup"><span data-stu-id="38757-155">Participant</span></span></td>
    <td><span data-ttu-id="38757-156">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38757-157"><strong>参加者のタイプ</strong> 一覧の <strong>ロール ベース</strong> タブの、<strong>参加者</strong> を選択したのち、ステップの割り当て先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="38757-158"><strong>参加者</strong> の一覧で、ステップを割り当てる先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38757-159">階層</span><span class="sxs-lookup"><span data-stu-id="38757-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="38757-160">特定の組織階層内のユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38757-161"><strong>階層タイプ</strong> 一覧の <strong>階層選択</strong> タブの、<strong>階層</strong> を選択したのち、ステップの割り当て先の階層グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="38757-162">システムは、一定範囲のユーザー名を階層から取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38757-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="38757-163">これらの名前は、ステップを割り当てることができるユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="38757-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="38757-164">システムで取得するユーザー名の範囲について、その開始点と終了点を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="38757-165">開始点を指定するには、<strong>開始</strong> 一覧から人物を選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="38757-166">終了点を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="38757-167">次に、階層のどこで名前の取得を止めるかを示す条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="38757-168"><strong>階層オプション</strong> で、ステップを割り当てる範囲内のユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="38757-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="38757-169"><strong>取得したすべてのユーザーに割り当てる</strong> – ステップは範囲内のすべてのユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="38757-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="38757-170"><strong>取得した最後のユーザーのみに割り当てる</strong> – ステップは、範囲内の最後のユーザーのみに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="38757-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="38757-171"><strong>次の条件のユーザーを除外します</strong> – ステップは、特定の条件に該当する範囲内のどのユーザーにも割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="38757-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="38757-172">条件を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38757-173">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-173">Workflow user</span></span></td>
    <td><span data-ttu-id="38757-174">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="38757-175"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38757-176">ユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-176">User</span></span></td>
    <td><span data-ttu-id="38757-177">特定の Microsoft Dynamics 365 for Finance and Operations ユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38757-178"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="38757-179"><strong>利用可能なユーザー</strong> 一覧には、すべての Finance and Operations ユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="38757-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="38757-180">ステップを割り当てるユーザーを選択し、そのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="38757-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="38757-181">**期限**タブの、**期間**フィールドで、この承認ステップに到達したドキュメントに対して、ユーザーが処理または対応しなければならない期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="38757-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="38757-182">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-182">Select one of the following options:</span></span>

    - <span data-ttu-id="38757-183">**時間** – ユーザーが対応しなければならない期限を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="38757-184">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38757-185">**日数** – ユーザーが対応しなければならない期限を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="38757-186">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38757-187">**週** – ユーザーが対応しなければならない期限を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="38757-188">**月** – ユーザーの対応期限の曜日、週で選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="38757-189">たとえば、その月の第 3 週の金曜日までに対応するよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="38757-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="38757-190">**年** – ユーザーの対応期限の曜日、週、月で選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="38757-191">たとえば、12 月の第 3 週の金曜日までに対応するよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="38757-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="38757-192">割り当てられている時間内にユーザーがドキュメントを処理しなかった場合、そのドキュメントは期限超過になります。</span><span class="sxs-lookup"><span data-stu-id="38757-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="38757-193">期限超過のドキュメントは、このページの**エスカレーション**領域で選択したオプションに基づいて、エスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="38757-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="38757-194">承認ステップを複数のユーザーまたはユーザー グループに割り当てる場合は、**完了ポリシー**タブで、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="38757-195">**1 人の承認者** – ドキュメントに適用されるアクションは、最初に対応した人物によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="38757-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="38757-196">たとえば、康介は USD 15,000 の経費精算書を送信済です。</span><span class="sxs-lookup"><span data-stu-id="38757-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38757-197">その経費精算書は、現在は政美、健一郎、および隆志に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="38757-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="38757-198">このドキュメントに最初に対応するのが政美の場合は、彼女が行うアクションがドキュメントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="38757-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="38757-199">たとえば、政美が経費報告書を却下した場合、ドキュメントは却下され、康介に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="38757-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="38757-200">政美が経費精算書を承認した場合、ドキュメントは承認を受けるために綾に送信されます。</span><span class="sxs-lookup"><span data-stu-id="38757-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![承認プロセスのあるワークフロー](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="38757-202">**過半数の承認者** – ドキュメントに適用されるアクションは、過半数の承認者が対応したときに決定されます。</span><span class="sxs-lookup"><span data-stu-id="38757-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="38757-203">たとえば、康介は USD 15,000 の経費精算書を送信済です。</span><span class="sxs-lookup"><span data-stu-id="38757-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38757-204">その経費精算書は、現在は政美、健一郎、および隆志に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="38757-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="38757-205">最初に対応する 2 人の承認者が政美と健一郎であれば、その 2 人の取るアクションがドキュメントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="38757-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="38757-206">政美がドキュメントを承認しても、健一郎がドキュメントを却下した場合、ドキュメントは却下され、康介に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="38757-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="38757-207">政美と健一郎の両方がドキュメントを承認した場合、ドキュメントは承認を受けるために綾に送信されます。</span><span class="sxs-lookup"><span data-stu-id="38757-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="38757-208">**承認者の割合** – ドキュメントに適用されるアクションは、特定の割合の承認者が対応したときに決定されます。</span><span class="sxs-lookup"><span data-stu-id="38757-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="38757-209">たとえば、康介は USD 15,000 の経費精算書を送信済です。</span><span class="sxs-lookup"><span data-stu-id="38757-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38757-210">経費精算書は、現在は政美、健一郎、および隆志に割り当てられていて、割合として **50** が入力済だとします。</span><span class="sxs-lookup"><span data-stu-id="38757-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="38757-211">最初に対応する 2 人の承認者が政美と健一郎であれば、その 2 人の取るアクションがドキュメントに適用されます。それは、承認者の 50% という条件を満たしているためです。</span><span class="sxs-lookup"><span data-stu-id="38757-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="38757-212">政美がドキュメントを承認しても、健一郎がドキュメントを却下した場合、ドキュメントは却下され、康介に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="38757-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="38757-213">政美と健一郎の両方がドキュメントを承認した場合、ドキュメントは承認を受けるために綾に送信されます。</span><span class="sxs-lookup"><span data-stu-id="38757-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="38757-214">**すべての承認者** – すべての承認者がドキュメントを承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38757-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="38757-215">それ以外の場合、ワークフローは続行できません。</span><span class="sxs-lookup"><span data-stu-id="38757-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="38757-216">たとえば、康介は USD 15,000 の経費精算書を送信済です。</span><span class="sxs-lookup"><span data-stu-id="38757-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38757-217">その経費精算書は、現在は政美、健一郎、および隆志に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="38757-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="38757-218">政美と健一郎がドキュメントを承認しても、隆志がドキュメントを却下した場合、ドキュメントは却下され、康介に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="38757-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="38757-219">承認者全員 (政美、健一郎、および隆志) がドキュメントを承認した場合、ドキュメントは承認を受けるために綾に送信されます。</span><span class="sxs-lookup"><span data-stu-id="38757-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="38757-220">承認ステップがいつ必要になるかを指定する</span><span class="sxs-lookup"><span data-stu-id="38757-220">Specify when the approval step is required</span></span>

<span data-ttu-id="38757-221">承認ステップがいつ必要になるかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="38757-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="38757-222">承認ステップは、常に必要とすることも、指定条件を満たす場合にのみ必要とすることもできます。</span><span class="sxs-lookup"><span data-stu-id="38757-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="38757-223">承認ステップを常に必要とする場合</span><span class="sxs-lookup"><span data-stu-id="38757-223">The approval step is always required</span></span>

<span data-ttu-id="38757-224">承認ステップが常に必要な場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="38757-225">左ウィンドウで、**条件**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="38757-226">**このステップを常に実行**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="38757-227">承認ステップを特定の条件下で必要とする場合</span><span class="sxs-lookup"><span data-stu-id="38757-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="38757-228">特定の条件を満たす場合にのみ必要になる承認プロセスをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="38757-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="38757-229">たとえば、購買要求ワークフローの承認ステップをコンフィギュレーションする場合は、購買要求の合計金額が USD 10,000 を超える場合にのみ承認ステップを発生させると都合がよいこともあります。</span><span class="sxs-lookup"><span data-stu-id="38757-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="38757-230">承認ステップがどのような場合になるかを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="38757-231">左ウィンドウで、**条件**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="38757-232">**次の条件が満たされた場合にのみこのステップを実行**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="38757-233">条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-233">Enter a condition.</span></span>
4. <span data-ttu-id="38757-234">必要に応じて、追加条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="38757-235">入力した条件が正しくコンフィギュレーションされていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="38757-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="38757-236">**テスト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-236">Click **Test**.</span></span>
    2. <span data-ttu-id="38757-237">**ワークフロー条件のテスト**ページで、**条件の検証**領域で、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="38757-238">**テスト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-238">Click **Test**.</span></span> <span data-ttu-id="38757-239">システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。</span><span class="sxs-lookup"><span data-stu-id="38757-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="38757-240">**OK**、または**キャンセル**をクリックして、**プロパティ**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="38757-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="38757-241">ドキュメントが期限超過の場合の処置を指定する</span><span class="sxs-lookup"><span data-stu-id="38757-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="38757-242">割り当てられている時間内にユーザーがドキュメントを処理しなかった場合、そのドキュメントは期限超過になります。</span><span class="sxs-lookup"><span data-stu-id="38757-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="38757-243">期限超過したドキュメントは、承認を受けるために別のユーザーにエスカレートする (自動的に割り当てる) ことができます。</span><span class="sxs-lookup"><span data-stu-id="38757-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="38757-244">期限超過したドキュメントをエスカレートするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="38757-245">左ウィンドウで、**エスカレーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="38757-246">**エスカレーション パスを使用**チェック ボックスをオンにし、エスカレーション パスを作成します。</span><span class="sxs-lookup"><span data-stu-id="38757-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="38757-247">ドキュメントは、エスカレーション パスにリストされるユーザーに自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="38757-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="38757-248">たとえば、次の表に、エスカレーション パスを示します。</span><span class="sxs-lookup"><span data-stu-id="38757-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="38757-249">順番</span><span class="sxs-lookup"><span data-stu-id="38757-249">Sequence</span></span> | <span data-ttu-id="38757-250">エスカレーション パス</span><span class="sxs-lookup"><span data-stu-id="38757-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="38757-251">1</span><span class="sxs-lookup"><span data-stu-id="38757-251">1</span></span>        | <span data-ttu-id="38757-252">割り当て先: 奈緒美</span><span class="sxs-lookup"><span data-stu-id="38757-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="38757-253">2</span><span class="sxs-lookup"><span data-stu-id="38757-253">2</span></span>        | <span data-ttu-id="38757-254">割り当て先: 悦子</span><span class="sxs-lookup"><span data-stu-id="38757-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="38757-255">3</span><span class="sxs-lookup"><span data-stu-id="38757-255">3</span></span>        | <span data-ttu-id="38757-256">最終アクション: 拒否</span><span class="sxs-lookup"><span data-stu-id="38757-256">Final action: Reject</span></span> |

    <span data-ttu-id="38757-257">この例では、奈緒美に、期限超過のドキュメントが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="38757-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="38757-258">割り当てられている時間内に奈緒美が対応しない場合は、悦子にドキュメントが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="38757-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="38757-259">割り当てられている時間内に悦子が対応しない場合は、システムによりドキュメントが却下されます。</span><span class="sxs-lookup"><span data-stu-id="38757-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="38757-260">エスカレーション パスにユーザーを追加するには、**エスカレーションの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="38757-261">**割り当てタイプ**タブで、次の表のいずれかのオプションを選択し、オプションの追加手順を実行してから、ステップ 4 に進みます。</span><span class="sxs-lookup"><span data-stu-id="38757-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="38757-262">オプション</span><span class="sxs-lookup"><span data-stu-id="38757-262">Option</span></span></th>
    <th><span data-ttu-id="38757-263">ドキュメントのエスカレート先のユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="38757-264">追加手順</span><span class="sxs-lookup"><span data-stu-id="38757-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="38757-265">階層</span><span class="sxs-lookup"><span data-stu-id="38757-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="38757-266">特定の組織階層内のユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38757-267"><strong>階層タイプ</strong> 一覧の <strong>階層選択</strong> タブの、<strong>階層</strong> を選択したのち、ドキュメントをエスカレートする先の階層グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="38757-268">システムは、一定範囲のユーザー名を階層から取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38757-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="38757-269">これらの名前は、ドキュメントのエスカレート先に指定できるユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="38757-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="38757-270">システムで取得するユーザー名の範囲について、その開始点と終了点を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38757-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="38757-271">開始点を指定するには、<strong>開始</strong> 一覧から人物を選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="38757-272">終了点を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="38757-273">次に、階層のどこで名前の取得を止めるかを示す条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="38757-274"><strong>階層オプション</strong> で、ドキュメントをエスカレートできる範囲内のユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="38757-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="38757-275"><strong>取得したすべてのユーザーに割り当てる</strong> – ドキュメントは範囲内のすべてのユーザーにエスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="38757-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="38757-276"><strong>取得した最後のユーザーのみに割り当てる</strong> – ドキュメントは、範囲内の最後のユーザーのみにエスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="38757-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="38757-277"><strong>次の条件のユーザーを除外します</strong> – ドキュメントは、特定の条件に該当する範囲内のどのユーザーにもエスカレートされません。</span><span class="sxs-lookup"><span data-stu-id="38757-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="38757-278">条件を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38757-279">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-279">Workflow user</span></span></td>
    <td><span data-ttu-id="38757-280">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="38757-281"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38757-282">ユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-282">User</span></span></td>
    <td><span data-ttu-id="38757-283">特定の Finance and Operations ユーザー</span><span class="sxs-lookup"><span data-stu-id="38757-283">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38757-284"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="38757-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="38757-285"><strong>利用可能なユーザー</strong> 一覧には、すべての Finance and Operations ユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="38757-285">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="38757-286">ドキュメントをエスカレートするユーザーを選択し、そのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="38757-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="38757-287">**期限**タブの、**期間**フィールドで、ドキュメントに対して、ユーザーが処理または対応しなければならない期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="38757-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="38757-288">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-288">Select one of the following options:</span></span>

    - <span data-ttu-id="38757-289">**時間** – ユーザーが対応しなければならない期限を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="38757-290">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38757-291">**日数** – ユーザーが対応しなければならない期限を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="38757-292">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38757-293">**週** – ユーザーが対応しなければならない期限を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="38757-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="38757-294">**月** – ユーザーの対応期限の曜日、週で選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="38757-295">たとえば、その月の第 3 週の金曜日までに対応するよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="38757-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="38757-296">**年** – ユーザーの対応期限の曜日、週、月で選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="38757-297">たとえば、12 月の第 3 週の金曜日までに対応するよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="38757-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="38757-298">エスカレーション パスに追加するユーザーごとに、ステップ 3～4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="38757-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="38757-299">ユーザーの順序は、変更できます。</span><span class="sxs-lookup"><span data-stu-id="38757-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="38757-300">エスカレーション パスに含まれるユーザーが、割り当てられた時間内に対応しない場合、システムによってドキュメントが自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="38757-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="38757-301">システムによる処理を指定するには、**アクション**行を選択し、**アクションの終了**タブでアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="38757-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

