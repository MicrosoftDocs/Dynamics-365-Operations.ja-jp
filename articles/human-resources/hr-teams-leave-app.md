---
title: Teams での休暇要求の管理
description: このトピックでは、Microsoft Teams で Dynamics 365 Human Resources アプリを使用して休暇を申請する方法について説明します。
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097262"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="0b5bf-103">Teams での休暇要求の管理</span><span class="sxs-lookup"><span data-stu-id="0b5bf-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0b5bf-104">Microsoft Teams の Dynamics 365 Human Resources アプリを使用することで、簡単に休暇を申請することができ、Microsoft Teams で休暇の残日数情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="0b5bf-105">ボットと対話して情報を要求し、休暇申請を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="0b5bf-106">**休暇** タブには、より詳細な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="0b5bf-107">さらに、Human Resources アプリ外部の Teams やチャットで今後の休暇についての情報を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="0b5bf-108">アプリのインストール</span><span class="sxs-lookup"><span data-stu-id="0b5bf-108">Install the app</span></span>

<span data-ttu-id="0b5bf-109">Dynamics 365 Human Resources アプリは、Teams ストアにあります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="0b5bf-110">Microsoft Teams で、アプリケーションの一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="0b5bf-111">Dynamics 365 Human Resources を検索し、**Human Resources** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="0b5bf-112">**追加** ボタンを選択してアプリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="0b5bf-113">アプリで自動的にサインインされなかった場合は、**設定** タブを選択してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="0b5bf-114">[サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="0b5bf-115">複数の Human Resources インスタンスへのアクセス許可がある場合は、 **設定** タブで接続先の環境を選択でき ます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="0b5bf-116">アプリはシステム管理者セキュリティ ロールをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="0b5bf-117">ボットの使用</span><span class="sxs-lookup"><span data-stu-id="0b5bf-117">Use the bot</span></span>

<span data-ttu-id="0b5bf-118">アプリをインストールすると、ボットが代理で実行できるアクションの種類を通知するウェルカム メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="0b5bf-119">初めてボットと通信する際には、サイン インする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="0b5bf-120">[サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="0b5bf-121">ボットには次の依頼ができます:</span><span class="sxs-lookup"><span data-stu-id="0b5bf-121">You can ask the bot to:</span></span>

- <span data-ttu-id="0b5bf-122">現在の休暇残数を表示します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-122">View your current leave balances.</span></span> <span data-ttu-id="0b5bf-123">たとえば、「休暇残数を表示する」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="0b5bf-124">休暇申請を開始する。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-124">Start a leave request for you.</span></span> <span data-ttu-id="0b5bf-125">たとえば、「休暇を取ってください」や「来週の木曜と金曜に休暇を取りたいのですが」というメッセージを送信すると、休暇の種類に応じた休暇申請がより具体的にできます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Teams チャットでの休暇申請の開始](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="0b5bf-127">チャット ボットでユーザーの休暇申請を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="0b5bf-128">**休暇申請** を選択し、申請の詳細を編集します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="0b5bf-129">同じ日に複数の休暇タイプの休暇申請を行いたい場合は、**その他オプション** メニューから **日の分割** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="0b5bf-130">休暇申請の単位が日数の場合に半日休暇を選択した場合は、**その他のオプション** メニューから **半日の定義** を選択することで、最初の半日と後半の半日のどちらに休暇を申請するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![半日の定義](./media/HalfDayDefinitions.png)

- <span data-ttu-id="0b5bf-132">休暇申請詳細情報の編集が完了したら、**送信** を選択して、承認を依頼します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![休暇申請の送信](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="0b5bf-134">Teams で休暇を管理する</span><span class="sxs-lookup"><span data-stu-id="0b5bf-134">Manage your leave in Teams</span></span>

<span data-ttu-id="0b5bf-135">**休暇** タブでは、次の情報を表示できます:</span><span class="sxs-lookup"><span data-stu-id="0b5bf-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="0b5bf-136">登録されている休暇タイプごとに、休暇残数の情報を表示する</span><span class="sxs-lookup"><span data-stu-id="0b5bf-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="0b5bf-137">今後の休暇依頼</span><span class="sxs-lookup"><span data-stu-id="0b5bf-137">Upcoming leave requests</span></span>

- <span data-ttu-id="0b5bf-138">休暇申請</span><span class="sxs-lookup"><span data-stu-id="0b5bf-138">Time-off requests</span></span>

- <span data-ttu-id="0b5bf-139">休暇申請の下書き</span><span class="sxs-lookup"><span data-stu-id="0b5bf-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="0b5bf-140">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="0b5bf-140">Create a new request</span></span>

1. <span data-ttu-id="0b5bf-141">**新規作成** を選択して、新しい休暇申請を作成する。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="0b5bf-142">休暇の日付または日数を入力し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Teams Human Resources 休暇アプリが休暇を追加します](./media/TimeOffHours.png)

3. <span data-ttu-id="0b5bf-144">必要に応じて、理由コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="0b5bf-145">また、コメントを入力して添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="0b5bf-146">異なる休暇タイプで同じ日に複数の休暇申請を行う場合は、**その他のオプション** メニューから **日の分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="0b5bf-147">**半日の定義** オプションを選択して、最初の半日の休みを要求するか、後半の半日の休みを要求するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="0b5bf-148">このオプションは、休暇要求単位が日数で、要求量が 0.5 日の場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="0b5bf-149">情報の入力が完了したら、**送信** を選択して、承認をリクエストします。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="0b5bf-150">また、**下書きとして保存** と入力すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="0b5bf-151">申請の下書きを管理する</span><span class="sxs-lookup"><span data-stu-id="0b5bf-151">Manage draft requests</span></span>

1. <span data-ttu-id="0b5bf-152">**下書き** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="0b5bf-153">申請を編集するには鉛筆アイコンを選択するか、[ごみ箱] を選択することで申請を削除できます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="0b5bf-154">必要な変更を行います。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-154">Make any necessary changes.</span></span> <span data-ttu-id="0b5bf-155">情報の入力が完了後は、**提出** と入力して承認を依頼します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="0b5bf-156">また、**下書きとして保存** を選択すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="0b5bf-157">Teams 通知への対応</span><span class="sxs-lookup"><span data-stu-id="0b5bf-157">Respond to Teams notifications</span></span>

<span data-ttu-id="0b5bf-158">自分または自分が承認者である作業者が休暇申請を送信すると、Teams の Human Resources アプリで通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="0b5bf-159">通知を選択して表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-159">You can select the notification to view it.</span></span> <span data-ttu-id="0b5bf-160">通知は、**チャット** 領域にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="0b5bf-161">承認者の場合は、通知で **承認** または **拒否** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="0b5bf-162">オプション メッセージを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="0b5bf-163">同僚に次の休暇情報を送信する</span><span class="sxs-lookup"><span data-stu-id="0b5bf-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="0b5bf-164">Teams 向けの Human Resources アプリをインストールすると、チームやチャットで今後の休暇の情報を同僚に簡単に送信できます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="0b5bf-165">チームまたは Teams のチャットで、チャット ウィンドウの下にある人事管理ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![チャット ウィンドウの下の人事管理ボタン](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="0b5bf-167">共有する休暇申請を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-167">Select the leave request you want to share.</span></span> <span data-ttu-id="0b5bf-168">休暇申請の下書きを共有する場合は、まず **下書き** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="0b5bf-169">休暇申請がチャットに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="0b5bf-170">申請の下書きを共有すると、下書きとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="0b5bf-171">チームの休暇カレンダーの表示</span><span class="sxs-lookup"><span data-stu-id="0b5bf-171">View your team's leave calendar</span></span>

<span data-ttu-id="0b5bf-172">直属の部下を持つマネージャーの場合は、チームの承認済みおよび保留中の休暇を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="0b5bf-173">Teams の Human Resources アプリで、**休暇** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="0b5bf-174">**チーム カレンダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-174">Select **Team calendar**.</span></span> <span data-ttu-id="0b5bf-175">カレンダーには、直属の部下の承認済と保留中の休暇が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0b5bf-176">チーム カレンダーが表示できない場合は、有効にできるよう管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="0b5bf-177">詳細については、[インストールと設定](hr-admin-teams-leave-app.md#install-and-setup)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="0b5bf-178">対応している言語</span><span class="sxs-lookup"><span data-stu-id="0b5bf-178">Supported languages</span></span>

<span data-ttu-id="0b5bf-179">Teams の Dynamics 365 Human Resources アプリでは、次の言語がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="0b5bf-180">ロケール ID</span><span class="sxs-lookup"><span data-stu-id="0b5bf-180">Locale ID</span></span> | <span data-ttu-id="0b5bf-181">言語</span><span class="sxs-lookup"><span data-stu-id="0b5bf-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="0b5bf-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="0b5bf-182">de-DE</span></span> | <span data-ttu-id="0b5bf-183">ドイツ語 (ドイツ)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-183">German (Germany)</span></span> |
| <span data-ttu-id="0b5bf-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="0b5bf-184">es-ES</span></span> | <span data-ttu-id="0b5bf-185">スペイン語 (スペイン)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="0b5bf-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="0b5bf-186">es-MX</span></span> | <span data-ttu-id="0b5bf-187">スペイン語 (メキシコ)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="0b5bf-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="0b5bf-188">fr-CA</span></span> | <span data-ttu-id="0b5bf-189">フランス語 (カナダ)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-189">French (Canada)</span></span> |
| <span data-ttu-id="0b5bf-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="0b5bf-190">fr-FR</span></span> | <span data-ttu-id="0b5bf-191">フランス語 (フランス)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-191">French (France)</span></span> |
| <span data-ttu-id="0b5bf-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="0b5bf-192">it-IT</span></span> | <span data-ttu-id="0b5bf-193">イタリア語 (イタリア)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-193">Italian (Italy)</span></span> |
| <span data-ttu-id="0b5bf-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="0b5bf-194">nl-NL</span></span> | <span data-ttu-id="0b5bf-195">オランダ語 (オランダ)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="0b5bf-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="0b5bf-196">pt-BR</span></span> | <span data-ttu-id="0b5bf-197">ポルトガル語 (ブラジル)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="0b5bf-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="0b5bf-198">tr-TR</span></span> | <span data-ttu-id="0b5bf-199">トルコ語 (トルコ)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="0b5bf-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="0b5bf-200">zh-CN</span></span> | <span data-ttu-id="0b5bf-201">中国語 (簡体)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="0b5bf-202">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="0b5bf-202">Troubleshooting</span></span>

<span data-ttu-id="0b5bf-203">Dynamics 365 Human Resources Teams アプリへのサインインまたは使用で問題が発生した場合は、次のトラブルシューティングの手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="0b5bf-204">トラブルシューティング後も問題が解決しない場合は、サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="0b5bf-205">詳細については、[サポート](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="0b5bf-206">Teams の Human Resources アプリにサインインできない</span><span class="sxs-lookup"><span data-stu-id="0b5bf-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="0b5bf-207">アプリにサインインできない場合は、Microsoft Teams へのサインインに使用しているアカウントが Dynamics 365 Human Resources の従業員レコードに関連付けられていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0b5bf-208">システム管理者に連絡して、従業員レコードが正しく関連付けられていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="0b5bf-209">翻訳が正しく表示されない</span><span class="sxs-lookup"><span data-stu-id="0b5bf-209">Translations don't display correctly</span></span>

<span data-ttu-id="0b5bf-210">翻訳が期待した通りに表示されない場合は、Teams で選択する言語が Human Resources **ユーザー オプション** で選択された言語と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="0b5bf-211">Teams で、**設定** の **アプリ言語** を確認します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-211">In Teams, look at **App language** in **Settings**.</span></span>

![Teams の設定](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="0b5bf-213">Human Resources で、**設定** を選択してから、**ユーザー オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="0b5bf-214">**言語** フィールドが Teams の **アプリ言語** フィールドと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Human Resources ユーザー オプション](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="0b5bf-216">それでも翻訳の問題が発生する場合は、お知らせください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="0b5bf-217">詳細については、[Finance and Operations アプリまたは Lifecycle Services (LCS) のサポートを得る](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="0b5bf-218">Teams の Human Resources アプリで休暇申請を承認する際のエラー</span><span class="sxs-lookup"><span data-stu-id="0b5bf-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="0b5bf-219">Teams アプリで休暇申請を承認しようとしたときにエラーが発生した場合は、次のトラブルシューティングの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="0b5bf-220">Microsoft Teams へのサインインに使用しているアカウントが、Dynamics 365 Human Resources にアクセスに使用しているアカウントと同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="0b5bf-221">休暇承認のワークフロー設定を確認して、要求の有効な承認者であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="0b5bf-222">休暇申請ワークフローの詳細については、[休暇申請ワークフローの作成](hr-leave-and-absence-workflow.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="0b5bf-223">休暇承認者が休暇申請を承認するための Teams のチャット メッセージを受信しない</span><span class="sxs-lookup"><span data-stu-id="0b5bf-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="0b5bf-224">通知が環境およびユーザーに対して有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="0b5bf-225">詳細については、[Teams の Human Resources アプリで通知を有効にする](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) および[個々のユーザーの Teams の通知をオンまたはオフにする](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="0b5bf-226">ユーザーが休暇申請を承認するために使用するのと同じ資格情報で **チャット** タブにログインしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="0b5bf-227">"サインアウト" というメッセージを使用してから "サインイン" を使用して正しい資格情報でサインインします。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="0b5bf-228">それでも問題が解消しない場合は、システム管理者としてビジネス イベント システム バッチ ジョブのステータスを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="0b5bf-229">待機中または実行中のステージにある場合は、数分後にもう一度戻って確認します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="0b5bf-230">ステータスが変わらない場合は、弊社のチームで問題を解決することができるように、サポート チケットを記録します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="0b5bf-231">既知のアクセシビリティの問題</span><span class="sxs-lookup"><span data-stu-id="0b5bf-231">Known accessibility issues</span></span>

<span data-ttu-id="0b5bf-232">Teams の Human Resources アプリには、今後のリリースに向けて修正を行っている次のようなアクセシビリティ上の問題があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="0b5bf-233">出庫</span><span class="sxs-lookup"><span data-stu-id="0b5bf-233">Issue</span></span> | <span data-ttu-id="0b5bf-234">回避策または説明</span><span class="sxs-lookup"><span data-stu-id="0b5bf-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="0b5bf-235">デスクトップで 400% に拡大すると、一部のアクション ボタンが表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="0b5bf-236">この拡大のレベルがサポートされるまで、代わりに拡大鏡を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="0b5bf-237">**休暇** タブで、VoiceOver が、タイムアウト グリッドのヘッダーを読みながら、ボタンのアクションを読み上げます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="0b5bf-238">グリッド内のヘッダーと要素は年によってグループ化され、折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="0b5bf-239">VoiceOver は、これをアクション可能な項目として解釈しますが、アクション可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="0b5bf-240">**休暇** タブで、新しい要求の **理由コード** へ移動する際に追加のスワイプ ジェスチャがあります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="0b5bf-241">スワイプ ナビゲーションがアクセスしようとしている非表示のコントロールはありません。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="0b5bf-242">**休暇** タブで、カレンダーが開いている状態でスワイプすると、新しい要求の上部または要求の編集中に移動するのではなく、コントロールの外部に出てしまいます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="0b5bf-243">**今日に移動** が表示された場合、コントロールの最後で逆方向にスワイプして一番上に戻ることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="0b5bf-244">**チャット** タブで、支援ツールまたはキーボードのナビゲーションを使用して日付を入力すると、フォーカスが上に戻ってきます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="0b5bf-245">入力領域に戻るまでタブを押し続けます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="0b5bf-246">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="0b5bf-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="0b5bf-247">Microsoft Language Understanding インテリジェント サービス (LUIS)</span><span class="sxs-lookup"><span data-stu-id="0b5bf-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="0b5bf-248">Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="0b5bf-249">ユーザーが入力した 「顧客 Contoso を検索」は、Language Understanding インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="0b5bf-250">LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="0b5bf-251">LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="0b5bf-252">この情報は、Microsoft の  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="0b5bf-253">ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="0b5bf-254">LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0b5bf-255">LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="0b5bf-256">ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="0b5bf-257">認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="0b5bf-258">Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="0b5bf-259">Microsoft Teams、Azure Event Grid、Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0b5bf-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="0b5bf-260">Microsoft Teams 内で Dynamics 365 Human Resources アプリを使用する場合、特定の顧客データが、テナントの Human Resources サービスが展開されている地域外に流出する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="0b5bf-261">Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="0b5bf-262">このデータは、Microsoft Azure Event Grid に最大 24 時間保存でき、米国内で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0b5bf-263">データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="0b5bf-264">Human Resources アプリでチャット ボットと会話しながら、会話の内容を Azure Cosmos DB に保存し、Microsoft Teams に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="0b5bf-265">このデータは Azure Cosmos DB に最大24時間格納され、テナントの Human Resources サービスが展開されている地域外で処理される可能性があり、転送中および保存中に暗号化され、トレーニングやサービス改善のために Microsoft またはそのサブプロセッサが使用することはありません。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="0b5bf-266">データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="0b5bf-267">組織または組織内のユーザーの Microsoft Teams の Human Resources アプリへのアクセスを制限するには、[Microsoft Teams におけるアプリのアクセス許可ポリシーの管理](/MicrosoftTeams/teams-app-permission-policies) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b5bf-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="0b5bf-268">参照</span><span class="sxs-lookup"><span data-stu-id="0b5bf-268">See also</span></span>

[<span data-ttu-id="0b5bf-269">Microsoft Teams のダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="0b5bf-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="0b5bf-270">Microsoft Teams ヘルプ センター</span><span class="sxs-lookup"><span data-stu-id="0b5bf-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="0b5bf-271">Teams の Human Resources アプリ</span><span class="sxs-lookup"><span data-stu-id="0b5bf-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
