---
title: Teams での休暇要求の管理
description: このトピックでは、Microsoft Teams で Dynamics 365 Human Resources アプリを使用して休暇を申請する方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 342106ad09db3a5d9c2dec8ab18e824d70e0f6bf
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128164"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="a78c2-103">Teams での休暇要求の管理</span><span class="sxs-lookup"><span data-stu-id="a78c2-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a78c2-104">Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用することで、簡単に休暇を申請することができ、Microsoft Teams で休暇の残日数情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="a78c2-105">ボットと対話して情報を要求し、休暇申請を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="a78c2-106">**休暇** タブには、より詳細な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="a78c2-107">さらに、Human Resources アプリの外で、チームやチャットで今後の休暇についての情報を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-107">You can also send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="a78c2-108">アプリのインストール</span><span class="sxs-lookup"><span data-stu-id="a78c2-108">Install the app</span></span>

<span data-ttu-id="a78c2-109">Human Resources アプリは、Teams ストアにあります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="a78c2-110">Microsoft Teams で省略記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Teams Human Resources の休暇アプリの省略記号](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="a78c2-112">Dynamics 365 Human Resources を検索し、**Human Resources** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Teams Human Resources の休暇アプリの HR タイル](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="a78c2-114">**追加** ボタンを選択してアプリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a78c2-114">Select the **Add** button to install the app.</span></span>

   ![Teams Human Resources の休暇アプリのインストール](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="a78c2-116">アプリで自動的にサインインされなかった場合は、**設定** タブを選択してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="a78c2-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Teams Human Resources 休暇アプリの設定タブ](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="a78c2-118">[サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="a78c2-119">複数の Human Resources インスタンスへのアクセス許可がある場合は、 **設定** タブで接続先の環境を選択でき ます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="a78c2-120">アプリはシステム管理者セキュリティ ロールをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="a78c2-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="a78c2-121">ボットの使用</span><span class="sxs-lookup"><span data-stu-id="a78c2-121">Use the bot</span></span>

<span data-ttu-id="a78c2-122">アプリをインストールすると、ボットが代理で実行できるアクションの種類を通知するウェルカム メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams 休暇アプリがウェルカム メッセージを表示します](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="a78c2-124">初めてボットと通信する際には、サイン インする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="a78c2-125">[サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="a78c2-126">ボットには次の依頼ができます:</span><span class="sxs-lookup"><span data-stu-id="a78c2-126">You can ask the bot to:</span></span>

- <span data-ttu-id="a78c2-127">登録されている休暇タイプごとに、休暇残数情報を表示する。</span><span class="sxs-lookup"><span data-stu-id="a78c2-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Teams Human Resources 休暇アプリが残日数を表示します](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="a78c2-129">特定の休暇タイプに関する追加情報を表示する。</span><span class="sxs-lookup"><span data-stu-id="a78c2-129">Show additional details about a specific leave type.</span></span>

   ![Teams Human Resources 休暇アプリが詳細情報を表示します](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="a78c2-131">休暇申請を開始する。</span><span class="sxs-lookup"><span data-stu-id="a78c2-131">Start a leave request for you.</span></span>

   ![Teams Human Resources 休暇アプリが休暇を申請します](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="a78c2-133">休暇申請を開始した後、カード内で日数を調整できます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Teams Human Resources 休暇アプリが申請を編集します](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="a78c2-135">情報の入力が完了したら、**送信** を選択して、承認のために送信します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="a78c2-136">また、**下書きとして保存** を選択すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-136">You can also select **Save as draft** to come back to it later.</span></span>

![Teams Human Resources 休暇アプリが申請を送信します](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="a78c2-138">Teams で休暇を管理する</span><span class="sxs-lookup"><span data-stu-id="a78c2-138">Manage your leave in Teams</span></span>

<span data-ttu-id="a78c2-139">**休暇** タブでは、次の情報を表示できます:</span><span class="sxs-lookup"><span data-stu-id="a78c2-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="a78c2-140">登録されている休暇タイプごとに、休暇残数の情報を表示する</span><span class="sxs-lookup"><span data-stu-id="a78c2-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="a78c2-141">今後の休暇依頼</span><span class="sxs-lookup"><span data-stu-id="a78c2-141">Upcoming leave requests</span></span>

- <span data-ttu-id="a78c2-142">休暇申請</span><span class="sxs-lookup"><span data-stu-id="a78c2-142">Time-off requests</span></span>

- <span data-ttu-id="a78c2-143">休暇申請の下書き</span><span class="sxs-lookup"><span data-stu-id="a78c2-143">Draft leave requests</span></span>

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="a78c2-145">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="a78c2-145">Create a new request</span></span>

1. <span data-ttu-id="a78c2-146">**新規作成** を選択して、新しい休暇申請を作成する。</span><span class="sxs-lookup"><span data-stu-id="a78c2-146">To create a new leave request, select **New request**.</span></span>

   ![Teams Human Resources 休暇アプリの新規申請](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="a78c2-148">休暇の日付または日数を入力し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Teams Human Resources 休暇アプリが休暇を追加します](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="a78c2-150">必要に応じて、理由コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="a78c2-151">また、コメントを入力して添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="a78c2-152">情報の入力が完了後は、**提出** と入力して承認を依頼します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a78c2-153">また、**下書きとして保存** と入力すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="a78c2-154">申請の下書きを管理する</span><span class="sxs-lookup"><span data-stu-id="a78c2-154">Manage draft requests</span></span>

1. <span data-ttu-id="a78c2-155">**下書き** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-155">Select the **Drafts** tab.</span></span>

   ![Teams Human Resources 休暇アプリの下書きタブ](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="a78c2-157">申請を編集するには鉛筆アイコンを選択するか、[ごみ箱] を選択することで申請を削除できます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="a78c2-158">必要な変更を行います。</span><span class="sxs-lookup"><span data-stu-id="a78c2-158">Make any necessary changes.</span></span> <span data-ttu-id="a78c2-159">情報の入力が完了後は、**提出** と入力して承認を依頼します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a78c2-160">また、**下書きとして保存** を選択すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Teams Human Resources 休暇アプリが下書きを編集します](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="a78c2-162">Teams 通知への対応</span><span class="sxs-lookup"><span data-stu-id="a78c2-162">Respond to Teams notifications</span></span>

<span data-ttu-id="a78c2-163">自分または自分が承認者である作業者が休暇申請を送信すると、Teams の Human Resources アプリで通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="a78c2-164">通知を選択して表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-164">You can select the notification to view it.</span></span> <span data-ttu-id="a78c2-165">通知は、**チャット** 領域にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="a78c2-166">承認者の場合は、通知で **承認** または **拒否** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="a78c2-167">オプション メッセージを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-167">You can also provide an optional message.</span></span>

![Teams の Human Resources アプリの休暇申請通知](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="a78c2-169">同僚に次の休暇情報を送信する</span><span class="sxs-lookup"><span data-stu-id="a78c2-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="a78c2-170">Teams 向けの Human Resources アプリをインストールすると、チームやチャットで今後の休暇の情報を同僚に簡単に送信できます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="a78c2-171">チームまたは Teams のチャットで、チャット ウィンドウの下にある人事管理ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![チャット ウィンドウの下の人事管理ボタン](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="a78c2-173">共有する休暇申請を選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-173">Select the leave request you want to share.</span></span> <span data-ttu-id="a78c2-174">休暇申請の下書きを共有する場合は、まず **下書き** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![共有する今後の休暇申請の選択](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="a78c2-176">休暇申請がチャットに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-176">Your leave request will display in the chat.</span></span>

![Human Resources の休暇申請カード](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="a78c2-178">申請の下書きを共有すると、下書きとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-178">If you shared a draft request, it will display as a draft:</span></span>

![Human Resources の休暇申請カードの下書き](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="a78c2-180">チームの休暇カレンダーの表示</span><span class="sxs-lookup"><span data-stu-id="a78c2-180">View your team's leave calendar</span></span>

<span data-ttu-id="a78c2-181">直属の部下を持つマネージャーの場合は、チームの承認済みおよび保留中の休暇を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="a78c2-182">Teams の Human Resources アプリで、**休暇** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="a78c2-183">**チーム カレンダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-183">Select **Team calendar**.</span></span>

   ![Teams の Human Resources アプリでカレンダーを表示](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="a78c2-185">カレンダーには、直属の部下の承認済と保留中の休暇が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Teams の Human Resources アプリの休暇カレンダー](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="a78c2-187">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a78c2-187">Troubleshooting</span></span>

<span data-ttu-id="a78c2-188">Teams Human Resources アプリへのサインインまたは使用で問題が発生した場合は、次のトラブルシューティングの手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="a78c2-189">トラブルシューティング後も問題が解決しない場合は、サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="a78c2-190">詳細については、[サポート](hr-admin-troubleshooting-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="a78c2-191">Teams の Human Resources アプリにサインインできない</span><span class="sxs-lookup"><span data-stu-id="a78c2-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="a78c2-192">アプリにサインインできない場合は、Microsoft Teams へのサインインに使用しているアカウントが Dynamics 365 Human Resources の従業員レコードに関連付けられていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a78c2-193">システム管理者に連絡して、従業員レコードが正しく関連付けられていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="a78c2-194">Teams の Human Resources アプリで休暇申請を承認する際のエラー</span><span class="sxs-lookup"><span data-stu-id="a78c2-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="a78c2-195">Teams アプリで休暇申請を承認しようとしたときにエラーが発生した場合は、次のトラブルシューティングの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-195">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="a78c2-196">Microsoft Teams へのサインインに使用しているアカウントが、Dynamics 365 Human Resources にアクセスに使用しているアカウントと同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="a78c2-197">休暇承認のワークフロー設定を確認して、要求の有効な承認者であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="a78c2-198">休暇申請ワークフローの詳細については、[休暇申請ワークフローの作成](hr-leave-and-absence-workflow.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="a78c2-199">既知のアクセシビリティの問題</span><span class="sxs-lookup"><span data-stu-id="a78c2-199">Known accessibility issues</span></span>

<span data-ttu-id="a78c2-200">Teams の Human Resources アプリには、今後のリリースに向けて修正を行っている次のようなアクセシビリティ上の問題があります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-200">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="a78c2-201">出庫</span><span class="sxs-lookup"><span data-stu-id="a78c2-201">Issue</span></span> | <span data-ttu-id="a78c2-202">回避策または説明</span><span class="sxs-lookup"><span data-stu-id="a78c2-202">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="a78c2-203">デスクトップで 400% に拡大すると、一部のアクション ボタンが表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-203">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="a78c2-204">この拡大のレベルがサポートされるまで、代わりに拡大鏡を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a78c2-204">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="a78c2-205">**休暇** タブで、VoiceOver が、タイムアウト グリッドのヘッダーを読みながら、ボタンのアクションを読み上げます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-205">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="a78c2-206">グリッド内のヘッダーと要素は年によってグループ化され、折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-206">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="a78c2-207">VoiceOver は、これをアクション可能な項目として解釈しますが、アクション可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="a78c2-207">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="a78c2-208">**休暇** タブで、新しい要求の **理由コード** へ移動する際に追加のスワイプ ジェスチャがあります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-208">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="a78c2-209">スワイプ ナビゲーションがアクセスしようとしている非表示のコントロールはありません。</span><span class="sxs-lookup"><span data-stu-id="a78c2-209">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="a78c2-210">**休暇** タブで、カレンダーが開いている状態でスワイプすると、新しい要求の上部または要求の編集中に移動するのではなく、コントロールの外部に出てしまいます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-210">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="a78c2-211">**今日に移動** が表示された場合、コントロールの最後で逆方向にスワイプして一番上に戻ることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-211">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="a78c2-212">VoiceOver は、日付のラベルを読み取りません。</span><span class="sxs-lookup"><span data-stu-id="a78c2-212">Voiceover doesn't read the labels for dates.</span></span> | <span data-ttu-id="a78c2-213">ペアになる日付は、常に **開始日** と **終了日** です。</span><span class="sxs-lookup"><span data-stu-id="a78c2-213">The dates encountered in pairs are always **Start date** and **End date**.</span></span> |
| <span data-ttu-id="a78c2-214">**チャット** タブで、支援ツールまたはキーボードのナビゲーションを使用して日付を入力すると、フォーカスが上に戻ってきます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-214">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="a78c2-215">入力領域に戻るまでタブを押し続けます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-215">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="a78c2-216">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="a78c2-216">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a78c2-217">Microsoft Language Understanding インテリジェント サービス (LUIS)</span><span class="sxs-lookup"><span data-stu-id="a78c2-217">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a78c2-218">Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-218">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a78c2-219">ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-219">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a78c2-220">LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-220">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a78c2-221">LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。</span><span class="sxs-lookup"><span data-stu-id="a78c2-221">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a78c2-222">この情報は、Microsoft の  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-222">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a78c2-223">ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-223">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a78c2-224">LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-224">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a78c2-225">LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-225">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a78c2-226">ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。</span><span class="sxs-lookup"><span data-stu-id="a78c2-226">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a78c2-227">認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-227">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a78c2-228">Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-228">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="a78c2-229">Microsoft Teams、Azure Event Grid、Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a78c2-229">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="a78c2-230">Microsoft Teams 内で Dynamics 365 Human Resources アプリを使用する場合、特定の顧客データが、テナントの Human Resources サービスが展開されている地域外に流出する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a78c2-230">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="a78c2-231">Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。</span><span class="sxs-lookup"><span data-stu-id="a78c2-231">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a78c2-232">このデータは、Microsoft Azure Event Grid に最大 24 時間保存でき、米国内で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="a78c2-232">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="a78c2-233">データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-233">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="a78c2-234">Human Resources アプリでチャット ボットと会話しながら、会話の内容を Azure Cosmos DB に保存し、Microsoft Teams に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="a78c2-234">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="a78c2-235">このデータは Azure Cosmos DB に最大24時間格納され、テナントの Human Resources サービスが展開されている地域外で処理される可能性があり、転送中および保存中に暗号化され、トレーニングやサービス改善のために Microsoft またはそのサブプロセッサが使用することはありません。</span><span class="sxs-lookup"><span data-stu-id="a78c2-235">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="a78c2-236">データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-236">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="a78c2-237">組織または組織内のユーザーの Microsoft Teams の Human Resources アプリへのアクセスを制限するには、[Microsoft Teams におけるアプリのアクセス許可ポリシーの管理](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a78c2-237">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="a78c2-238">参照</span><span class="sxs-lookup"><span data-stu-id="a78c2-238">See also</span></span>

[<span data-ttu-id="a78c2-239">Microsoft Teams のダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="a78c2-239">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a78c2-240">Microsoft Teams ヘルプ センター</span><span class="sxs-lookup"><span data-stu-id="a78c2-240">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a78c2-241">Teams の Human Resources アプリ</span><span class="sxs-lookup"><span data-stu-id="a78c2-241">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
