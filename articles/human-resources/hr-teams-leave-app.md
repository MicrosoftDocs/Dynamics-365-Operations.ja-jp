---
title: Teams での休暇要求の管理
description: このトピックでは、Microsoft Teams で Dynamics 365 Human Resources アプリを使用して休暇を申請する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766763"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="a5681-103">Teams での休暇要求の管理</span><span class="sxs-lookup"><span data-stu-id="a5681-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a5681-104">Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用することで、簡単に休暇を申請することができ、Microsoft Teams で休暇の残日数情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a5681-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="a5681-105">ユーザーはボットと対話して情報を要求できます。</span><span class="sxs-lookup"><span data-stu-id="a5681-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="a5681-106">**休暇** タブには、より詳細な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5681-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="a5681-107">アプリのインストール</span><span class="sxs-lookup"><span data-stu-id="a5681-107">Install the app</span></span>

<span data-ttu-id="a5681-108">Human Resources アプリは、Teams ストアにあります。</span><span class="sxs-lookup"><span data-stu-id="a5681-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="a5681-109">Microsoft Teams で省略記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5681-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Teams Human Resources の休暇アプリの省略記号](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="a5681-111">Dynamics 365 Human Resources を検索し、**Human Resources**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5681-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Teams Human Resources の休暇アプリの HR タイル](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="a5681-113">**追加** ボタンを選択してアプリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a5681-113">Select the **Add** button to install the app.</span></span>

   ![Teams Human Resources の休暇アプリのインストール](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="a5681-115">アプリで自動的にサインインされなかった場合は、**設定** タブを選択してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="a5681-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Teams Human Resources 休暇アプリの設定タブ](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="a5681-117">[サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a5681-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="a5681-118">複数の Human Resources インスタンスへのアクセス許可がある場合は、 **設定** タブで接続先の環境を選択でき ます。</span><span class="sxs-lookup"><span data-stu-id="a5681-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="a5681-119">現在、このアプリはシステム管理者のセキュリティ ロールに対応していません。システム管理者アカウントでログインすると、エラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5681-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="a5681-120">別のアカウントでログインするには、**設定** タブで **アカウントの切り替え** ボタンを選択し、システム管理者権限のないユーザー アカウントでログインします。</span><span class="sxs-lookup"><span data-stu-id="a5681-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="a5681-121">ボットの使用</span><span class="sxs-lookup"><span data-stu-id="a5681-121">Use the bot</span></span>

<span data-ttu-id="a5681-122">アプリをインストールすると、ボットが代理で実行できるアクションの種類を通知するウェルカム メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5681-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams 休暇アプリがウェルカム メッセージを表示します](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="a5681-124">初めてボットと通信する際には、サイン インする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5681-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="a5681-125">[サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a5681-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="a5681-126">ボットには次の依頼ができます:</span><span class="sxs-lookup"><span data-stu-id="a5681-126">You can ask the bot to:</span></span>

- <span data-ttu-id="a5681-127">登録されている休暇タイプごとに、休暇残数情報を表示する。</span><span class="sxs-lookup"><span data-stu-id="a5681-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Teams Human Resources 休暇アプリが残日数を表示します](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="a5681-129">特定の休暇タイプに関する追加情報を表示する。</span><span class="sxs-lookup"><span data-stu-id="a5681-129">Show additional details about a specific leave type.</span></span>

   ![Teams Human Resources 休暇アプリが詳細情報を表示します](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="a5681-131">休暇申請を開始する。</span><span class="sxs-lookup"><span data-stu-id="a5681-131">Start a leave request for you.</span></span>

   ![Teams Human Resources 休暇アプリが休暇を申請します](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="a5681-133">休暇申請を開始した後、カード内で日数を調整できます。</span><span class="sxs-lookup"><span data-stu-id="a5681-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Teams Human Resources 休暇アプリが申請を編集します](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="a5681-135">情報の入力が完了したら、**送信** を選択して、承認のために送信します。</span><span class="sxs-lookup"><span data-stu-id="a5681-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="a5681-136">また、**下書きとして保存**を選択すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="a5681-136">You can also select **Save as draft** to come back to it later.</span></span>

![Teams Human Resources 休暇アプリが申請を送信します](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="a5681-138">Teams で休暇を管理する</span><span class="sxs-lookup"><span data-stu-id="a5681-138">Manage your leave in Teams</span></span>

<span data-ttu-id="a5681-139">**休暇** タブでは、次の情報を表示できます:</span><span class="sxs-lookup"><span data-stu-id="a5681-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="a5681-140">登録されている休暇タイプごとに、休暇残数の情報を表示する</span><span class="sxs-lookup"><span data-stu-id="a5681-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="a5681-141">今後の休暇依頼</span><span class="sxs-lookup"><span data-stu-id="a5681-141">Upcoming leave requests</span></span>

- <span data-ttu-id="a5681-142">休暇申請</span><span class="sxs-lookup"><span data-stu-id="a5681-142">Time-off requests</span></span>

- <span data-ttu-id="a5681-143">休暇申請の下書き</span><span class="sxs-lookup"><span data-stu-id="a5681-143">Draft leave requests</span></span>

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="a5681-145">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="a5681-145">Create a new request</span></span>

1. <span data-ttu-id="a5681-146">**新規作成** を選択して、新しい休暇申請を作成する。</span><span class="sxs-lookup"><span data-stu-id="a5681-146">To create a new leave request, select **New request**.</span></span>

   ![Teams Human Resources 休暇アプリの新規申請](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="a5681-148">休暇の日付または日数を入力し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5681-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Teams Human Resources 休暇アプリが休暇を追加します](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="a5681-150">必要に応じて、理由コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="a5681-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="a5681-151">また、コメントを入力して添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="a5681-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="a5681-152">情報の入力が完了後は、**提出**と入力して承認を依頼します。</span><span class="sxs-lookup"><span data-stu-id="a5681-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a5681-153">また、**下書きとして保存**と入力すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="a5681-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="a5681-154">申請の下書きを管理する</span><span class="sxs-lookup"><span data-stu-id="a5681-154">Manage draft requests</span></span>

1. <span data-ttu-id="a5681-155">**下書き**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5681-155">Select the **Drafts** tab.</span></span>

   ![Teams Human Resources 休暇アプリの下書きタブ](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="a5681-157">申請を編集するには鉛筆アイコンを選択するか、[ごみ箱] を選択することで申請を削除できます。</span><span class="sxs-lookup"><span data-stu-id="a5681-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="a5681-158">必要な変更を行います。</span><span class="sxs-lookup"><span data-stu-id="a5681-158">Make any necessary changes.</span></span> <span data-ttu-id="a5681-159">情報の入力が完了後は、**提出**と入力して承認を依頼します。</span><span class="sxs-lookup"><span data-stu-id="a5681-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a5681-160">また、**下書きとして保存**を選択すると、後で処理の続きを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="a5681-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Teams Human Resources 休暇アプリが下書きを編集します](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="a5681-162">Teams の通知</span><span class="sxs-lookup"><span data-stu-id="a5681-162">Teams notifications</span></span>

<span data-ttu-id="a5681-163">自分または自分が承認者である作業者が休暇申請を送信すると、Teams の Human Resources アプリで通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a5681-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="a5681-164">通知を選択して表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a5681-164">You can select the notification to view it.</span></span> <span data-ttu-id="a5681-165">通知は、**チャット** 領域にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5681-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="a5681-166">承認者の場合は、通知で **承認** または **拒否** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="a5681-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="a5681-167">オプション メッセージを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a5681-167">You can also provide an optional message.</span></span>

![Teams の Human Resources アプリの休暇申請通知](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="a5681-169">チームの休暇カレンダーの表示</span><span class="sxs-lookup"><span data-stu-id="a5681-169">View your team's leave calendar</span></span>

<span data-ttu-id="a5681-170">直属の部下を持つマネージャーの場合は、チームの承認済みおよび保留中の休暇を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a5681-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="a5681-171">Teams の Human Resources アプリで、**休暇** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5681-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="a5681-172">**チーム カレンダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5681-172">Select **Team calendar**.</span></span>

   ![Teams の Human Resources アプリでカレンダーを表示](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="a5681-174">カレンダーには、直属の部下の承認済と保留中の休暇が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5681-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Teams の Human Resources アプリの休暇カレンダー](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="a5681-176">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="a5681-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a5681-177">Microsoft Language Understanding インテリジェント サービス (LUIS)</span><span class="sxs-lookup"><span data-stu-id="a5681-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a5681-178">Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。</span><span class="sxs-lookup"><span data-stu-id="a5681-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a5681-179">ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="a5681-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a5681-180">LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5681-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a5681-181">LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。</span><span class="sxs-lookup"><span data-stu-id="a5681-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a5681-182">この情報は、Microsoft の  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a5681-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a5681-183">ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="a5681-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a5681-184">LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a5681-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a5681-185">LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a5681-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a5681-186">ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。</span><span class="sxs-lookup"><span data-stu-id="a5681-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a5681-187">認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5681-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a5681-188">Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。</span><span class="sxs-lookup"><span data-stu-id="a5681-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="a5681-189">Microsoft Azure Event Grid と Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a5681-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="a5681-190">Teams 内で Dynamics 365 Human Resources アプリの通知機能を使用する場合、特定の顧客データは、テナントの Human Resources サービスが展開される地域外に流出します。</span><span class="sxs-lookup"><span data-stu-id="a5681-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="a5681-191">Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。</span><span class="sxs-lookup"><span data-stu-id="a5681-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a5681-192">このデータは、最大 24 時間保存され、米国で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="a5681-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5681-193">参照</span><span class="sxs-lookup"><span data-stu-id="a5681-193">See also</span></span>

[<span data-ttu-id="a5681-194">Microsoft Teams のダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="a5681-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a5681-195">Microsoft Teams ヘルプ センター</span><span class="sxs-lookup"><span data-stu-id="a5681-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a5681-196">Teams の Human Resources アプリ</span><span class="sxs-lookup"><span data-stu-id="a5681-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
