---
title: "ワークフローの自動化タスクのコンフィギュレーション"
description: "このトピックでは、自動化タスクのプロパティをコンフィギュレーションする方法について説明します。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 56e29bd2e875b8bb729e5dfe0c5ac03fc997ecbe
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a><span data-ttu-id="ee2e9-103">ワークフローの自動化タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ee2e9-103">Configure an automated task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ee2e9-104">このトピックでは、自動化タスクのプロパティをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="ee2e9-105">ワークフロー エディターで自動化タスクをコンフィギュレーションするには、タスクを右クリックし、[**プロパティ**] をクリックして、[**プロパティ**] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="ee2e9-106">それから次の手順に従って、自動化タスクのプロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="ee2e9-107">タスクに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="ee2e9-107">Name the task</span></span>
<span data-ttu-id="ee2e9-108">自動化タスクの名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-108">Follow these steps to enter a name for the automated task.</span></span>

1.  <span data-ttu-id="ee2e9-109">左ウィンドウで [**基本設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="ee2e9-110">[**名前**] フィールドに、タスクの固有名を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="ee2e9-111">いつ通知を送信するかを指定する</span><span class="sxs-lookup"><span data-stu-id="ee2e9-111">Specify when notifications are sent</span></span>
<span data-ttu-id="ee2e9-112">自動化タスクが実行されたときまたはキャンセルされたときに、ユーザーに通知を送信できます。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="ee2e9-113">通知の送信条件と送信先のユーザーを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1.  <span data-ttu-id="ee2e9-114">左ウィンドウで、[**通知**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-114">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="ee2e9-115">通知の送信するイベントの横にあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-115">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="ee2e9-116">[**実行**] – タスクが実行されたときに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    -   <span data-ttu-id="ee2e9-117">[**キャンセル済**] – タスクがキャンセルされたときに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3.  <span data-ttu-id="ee2e9-118">ステップ 2 で選択したイベントの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-118">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="ee2e9-119">[**通知テキスト**] タブのテキスト ボックス内で、通知のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="ee2e9-120">通知を個人向けのものにするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="ee2e9-121">プレースホルダーは、通知がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="ee2e9-122">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-122">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="ee2e9-123">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-123">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="ee2e9-124">[**プレースホルダーの挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-124">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="ee2e9-125">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-125">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="ee2e9-126">[**挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-126">Click **Insert**.</span></span>

6.  <span data-ttu-id="ee2e9-127">通知の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-127">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="ee2e9-128">[**翻訳**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-128">Click **Translations**.</span></span>
    2.  <span data-ttu-id="ee2e9-129">表示されるページで、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-129">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="ee2e9-130">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="ee2e9-131">[**翻訳テキスト**] フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-131">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="ee2e9-132">テキストをカスタマイズする場合は、ステップ 5 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="ee2e9-133">[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-133">Click **Close**.</span></span>

7.  <span data-ttu-id="ee2e9-134">[**受信者**] タブで、通知の送信先ユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="ee2e9-135">次の表のいずれかのオプションを選択し、オプションの追加ステップを実行してから、ステップ 8 に進みます。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="ee2e9-136">オプション</span><span class="sxs-lookup"><span data-stu-id="ee2e9-136">Option</span></span></th>
    <th><span data-ttu-id="ee2e9-137">通知の受信者</span><span class="sxs-lookup"><span data-stu-id="ee2e9-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="ee2e9-138">追加手順</span><span class="sxs-lookup"><span data-stu-id="ee2e9-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="ee2e9-139">参加者</span><span class="sxs-lookup"><span data-stu-id="ee2e9-139">Participant</span></span></td>
    <td><span data-ttu-id="ee2e9-140">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="ee2e9-140">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="ee2e9-141">[<strong>参加者のタイプ</strong>] 一覧の [<strong>ロール ベース</strong>] タブの、[<strong>参加者</strong>] を選択したのち、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="ee2e9-142">[<strong>参加者</strong>] の一覧で、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ee2e9-143">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="ee2e9-143">Workflow user</span></span></td>
    <td><span data-ttu-id="ee2e9-144">現在のワークフローに参加しているユーザー</span><span class="sxs-lookup"><span data-stu-id="ee2e9-144">Users who participate in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="ee2e9-145">[<strong>ワークフロー ユーザー</strong>] 一覧の、[<strong>ワークフロー ユーザー</strong>] タブの、[<strong>ワークフロー ユーザー</strong>] を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="ee2e9-146">ユーザー</span><span class="sxs-lookup"><span data-stu-id="ee2e9-146">User</span></span></td>
    <td><span data-ttu-id="ee2e9-147">特定の Microsoft Dynamics 365 for Finance and Operations ユーザー</span><span class="sxs-lookup"><span data-stu-id="ee2e9-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="ee2e9-148">[<strong>ユーザー</strong>] を選択したのち、[<strong>ユーザー</strong>] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ee2e9-149">[<strong>利用可能なユーザー</strong>] 一覧には、すべての Finance and Operations ユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="ee2e9-150">通知の送信先のユーザーを選択して、それらのユーザーを [<strong>選択されたユーザー</strong>] リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="ee2e9-151">ステップ 2 で選択したイベントごとに、ステップ 3～7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="ee2e9-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>





