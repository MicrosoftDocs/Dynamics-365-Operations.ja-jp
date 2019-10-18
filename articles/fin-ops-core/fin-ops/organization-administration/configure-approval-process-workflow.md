---
title: ワークフローでの承認プロセスのコンフィギュレーション
description: 承認プロセスのプロパティをコンフィギュレーションするには、次の手順に従います。
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09d09464eae932bf9caf4f2ea38cbbb3b4f0162
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190215"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="4e302-103">ワークフローでの承認プロセスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4e302-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e302-104">承認プロセスのプロパティをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="4e302-105">承認プロセスを設定するには、ワークフロー エディターで承認要素を右クリックし、**プロパティ**をクリックして、**プロパティ**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="4e302-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="4e302-106">承認プロセスに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="4e302-106">Name the approval process</span></span>

<span data-ttu-id="4e302-107">次の手順に従って承認プロセスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="4e302-108">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="4e302-109">**名前**フィールドに、承認プロセスの固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="4e302-110">ドキュメントをシステムで自動的に処理する条件を指定する</span><span class="sxs-lookup"><span data-stu-id="4e302-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="4e302-111">特定の条件が満たされる場合にドキュメントを自動的に処理するようにシステムをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="4e302-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="4e302-112">たとえば、合計金額が USD 100 未満の経費精算書は、システムによって承認することができます。</span><span class="sxs-lookup"><span data-stu-id="4e302-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="4e302-113">ドキュメントをシステムによって処理する条件を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="4e302-114">左ウィンドウで、**自動アクション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="4e302-115">**自動アクションの有効化**を選択し、チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="4e302-116">**条件の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="4e302-117">条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-117">Enter a condition.</span></span>
5. <span data-ttu-id="4e302-118">必要に応じて追加条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="4e302-119">入力した条件が正しくコンフィギュレーションされていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4e302-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="4e302-120">**テスト**をクリックして、**ワークフロー条件のテスト**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="4e302-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="4e302-121">フォームの**条件の検証**領域でレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="4e302-122">**テスト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-122">Click **Test**.</span></span> <span data-ttu-id="4e302-123">システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。</span><span class="sxs-lookup"><span data-stu-id="4e302-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="4e302-124">**OK** または**キャンセル**をクリックして、**プロパティ**フォームに戻ります。</span><span class="sxs-lookup"><span data-stu-id="4e302-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="4e302-125">**自動完了アクション**一覧で、ドキュメントに対してシステムが実行するアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="4e302-126">いつ通知を送信するかを指定する</span><span class="sxs-lookup"><span data-stu-id="4e302-126">Specify when notifications are sent</span></span>

<span data-ttu-id="4e302-127">ドキュメントが承認、否認、委任、またはエスカレートされたときや、変更が依頼されたときに、ユーザーに通知を送信できます。</span><span class="sxs-lookup"><span data-stu-id="4e302-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="4e302-128">通知の送信条件と、通知の送信先のユーザーを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="4e302-129">左ウィンドウで、**通知**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="4e302-130">通知の送信するイベントの横にあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="4e302-131">**委任** – 承認対象のドキュメントが別のユーザーに割り当てられたとき。</span><span class="sxs-lookup"><span data-stu-id="4e302-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="4e302-132">**エスカレート** – 割り当てられたユーザーが割り当て時間内にドキュメントを処理しなかったとき。</span><span class="sxs-lookup"><span data-stu-id="4e302-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="4e302-133">**承認** – ドキュメントが承認されたとき。</span><span class="sxs-lookup"><span data-stu-id="4e302-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="4e302-134">**拒否** – ドキュメントが否認されたとき。</span><span class="sxs-lookup"><span data-stu-id="4e302-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="4e302-135">**変更依頼** – 割り当てられたユーザーが、提出されたドキュメントに対する変更を依頼したとき。</span><span class="sxs-lookup"><span data-stu-id="4e302-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="4e302-136">手順 2. で選択したイベントの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="4e302-137">**通知テキスト**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="4e302-138">テキスト ボックスに、通知のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="4e302-139">テキストをカスタマイズするには、プレースホルダーを挿入します。プレースホルダーは、ユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="4e302-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="4e302-140">プレースホルダーを挿入するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="4e302-141">メッセージ ボックス内で、プレースホルダーを表示する位置をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="4e302-142">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="4e302-143">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="4e302-144">**挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-144">Click **Insert**.</span></span>

7. <span data-ttu-id="4e302-145">通知の翻訳を追加するには、**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="4e302-146">表示されるフォームで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="4e302-147">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-147">Click **Add**.</span></span>
    2. <span data-ttu-id="4e302-148">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="4e302-149">**翻訳テキスト**テキスト ボックスで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="4e302-150">テキストをカスタマイズするためには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="4e302-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="4e302-151">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-151">Click **Close**.</span></span>

8. <span data-ttu-id="4e302-152">**受取人**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="4e302-153">通知の送信先ユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e302-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="4e302-154">次の表のいずれかのオプションを選択し、オプションの追加手順を実行してから、手順 10 に進みます。</span><span class="sxs-lookup"><span data-stu-id="4e302-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="4e302-155">オプション</span><span class="sxs-lookup"><span data-stu-id="4e302-155">Option</span></span></th>
    <th><span data-ttu-id="4e302-156">通知の受信者</span><span class="sxs-lookup"><span data-stu-id="4e302-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="4e302-157">追加手順</span><span class="sxs-lookup"><span data-stu-id="4e302-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="4e302-158"><strong>参加者</strong></span><span class="sxs-lookup"><span data-stu-id="4e302-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="4e302-159">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="4e302-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4e302-160"><strong>参加者</strong> を選択した後、<strong>ロール ベース</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="4e302-161"><strong>参加者のタイプ</strong> の一覧で、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="4e302-162"><strong>参加者</strong> の一覧で、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="4e302-163"><strong>ワークフロー ユーザー</strong></span><span class="sxs-lookup"><span data-stu-id="4e302-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="4e302-164">現在のワークフローに参加しているユーザー</span><span class="sxs-lookup"><span data-stu-id="4e302-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4e302-165"><strong>ワークフロー ユーザー</strong> を選択したのち、<strong>ワークフロー ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="4e302-166"><strong>ワークフロー ユーザー</strong> の一覧で、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="4e302-167"><strong>ユーザー</strong></span><span class="sxs-lookup"><span data-stu-id="4e302-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="4e302-168">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="4e302-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="4e302-169"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="4e302-170">通知の送信先のユーザーを選択して、これらのユーザーを<strong>選択されたユーザー</strong>リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="4e302-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="4e302-171">手順 2. で選択したイベントごとに手順 3 ～ 9 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="4e302-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="4e302-172">最終承認者を指定する</span><span class="sxs-lookup"><span data-stu-id="4e302-172">Specify a final approver</span></span>

<span data-ttu-id="4e302-173">承認のためにドキュメントを送信した人物が承認者であるような場合は、最終承認者を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="4e302-173">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="4e302-174">最終承認者を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="4e302-175">左ウィンドウで**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-175">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="4e302-176">**最終承認者の使用**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-176">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="4e302-177">最終承認者とするユーザーを一覧から選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-177">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="4e302-178">期限の設定</span><span class="sxs-lookup"><span data-stu-id="4e302-178">Set a time limit</span></span>

<span data-ttu-id="4e302-179">承認プロセスを特定の時間内に完了する必要がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-179">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="4e302-180">これらのステップで選択するオプションは、個々の承認ステップの**割り当て**および**エスカレーション**領域で選択したオプションに上書きされます。</span><span class="sxs-lookup"><span data-stu-id="4e302-180">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="4e302-181">左ウィンドウで**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-181">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="4e302-182">**ワークフローの期限の設定** **要素**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-182">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="4e302-183">**期間**フィールドで、承認プロセスをいつまでに完了する必要があるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e302-183">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="4e302-184">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-184">Select one of the following options:</span></span>

    - <span data-ttu-id="4e302-185">**時間** – 承認プロセスの完了期限を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-185">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="4e302-186">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="4e302-187">**日数** – 承認プロセスの完了期限を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-187">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="4e302-188">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="4e302-189">**週** – 承認プロセスの完了期限を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="4e302-189">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="4e302-190">**月** – 承認プロセスの完了期限を曜日または週で選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-190">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="4e302-191">たとえば、承認プロセスを当月の第 3 週の金曜日までに完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="4e302-191">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="4e302-192">**年** – 承認プロセスの完了期限を曜日、週、および月で選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-192">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="4e302-193">たとえば、承認プロセスを 12 月の第 3 週の金曜日までに完了する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="4e302-193">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="4e302-194">時間制限を超過した場合は、システムによってドキュメントが処理されます。</span><span class="sxs-lookup"><span data-stu-id="4e302-194">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="4e302-195">**アクション**の一覧で、システムで実行するアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e302-195">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="4e302-196">ユーザーが実行可能なアクションを指定する</span><span class="sxs-lookup"><span data-stu-id="4e302-196">Specify which actions are available to the user</span></span>

<span data-ttu-id="4e302-197">承認対象のドキュメントがユーザーに割り当てられた場合、そのユーザーはドキュメントを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e302-197">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="4e302-198">提出されたドキュメントに対してユーザーがどのアクションを実行できるかを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4e302-198">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="4e302-199">左ウィンドウで**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-199">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="4e302-200">ユーザーがドキュメントを承認できる場合は、**承認**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-200">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="4e302-201">ユーザーがドキュメントを否認できる場合は、**拒否**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-201">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="4e302-202">ユーザーがドキュメントに対する変更を依頼できる場合は、**変更依頼**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-202">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="4e302-203">ユーザーが承認対象のドキュメントを別のユーザーに割り当てることができる場合は、**委任**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4e302-203">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="4e302-204">**エンタープライズ ポータルの作業一覧からのアクションの有効化**チェック ボックスは使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="4e302-204">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="4e302-205">承認ステップをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="4e302-205">Configure the approval steps</span></span>

<span data-ttu-id="4e302-206">承認プロセスは、承認ステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="4e302-206">An approval process consists of approval steps.</span></span> <span data-ttu-id="4e302-207">承認プロセスにステップを追加し、そのステップをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4e302-207">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="4e302-208">ワークフロー エディターで、承認プロセスをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e302-208">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="4e302-209">ワークフロー エディターに承認プロセスのステップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4e302-209">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="4e302-210">承認ステップを追加するには、**ワークフロー要素**領域からキャンバスにステップをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="4e302-210">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="4e302-211">承認ステップをコンフィギュレーションするには、[承認ステップのコンフィギュレーション](configure-approval-step-workflow.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e302-211">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>
