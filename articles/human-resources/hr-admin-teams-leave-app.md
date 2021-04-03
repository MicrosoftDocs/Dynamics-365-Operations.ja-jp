---
title: Teams における人事管理アプリ
description: このトピックでは、Microsoft Teams における Microsoft Dynamics 365 Human Resources について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 86abe32f76f2cc21c773727be07a44be49cdbac7
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487876"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="54fe8-103">Teams における人事管理アプリ</span><span class="sxs-lookup"><span data-stu-id="54fe8-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="54fe8-104">Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用すると、従業員は簡単に休暇を申請することができ、Microsoft Teams にて休暇の残日数情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="54fe8-105">従業員は bot と対話して情報を要求できます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="54fe8-106">**休暇** タブには、より詳細な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="54fe8-107">さらに、Human Resources アプリの外部で、チームやチャットで今後の休暇に関する情報を送信できます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Teams Human Resources の休暇アプリ ボット](./media/hr-teams-leave-app-bot.png)

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources の休暇申請カード](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="54fe8-111">インストールと設定</span><span class="sxs-lookup"><span data-stu-id="54fe8-111">Install and setup</span></span>

<span data-ttu-id="54fe8-112">Dynamics 365 Human Resources アプリは、Teams ストアにあります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="54fe8-113">Teams アプリのインストールについては、[Teams で休暇申請を管理する](hr-teams-leave-app.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="54fe8-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="54fe8-114">Teams におけるアプリのアクセス許可の管理については、[Microsoft Teams におけるアプリのアクセス許可ポリシーを管理する](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="54fe8-115">ユーザーがアプリで休暇および欠勤カレンダーを表示するには、機能管理で **Teams の休暇および欠勤カレンダー** を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="54fe8-116">機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="54fe8-117">Teams の Human Resources アプリの通知を有効にする</span><span class="sxs-lookup"><span data-stu-id="54fe8-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="54fe8-118">ユーザーが Teams アプリで休暇申請通知を受け取るようにするには、Dynamics 365 Human Resources で通知を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="54fe8-119">Teams にサインインしていて、Teams の Dynamics 365 Human Resources アプリを使用しているユーザーだけが、通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="54fe8-120">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="54fe8-121">**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-121">Select **Links**.</span></span>

3. <span data-ttu-id="54fe8-122">**設定** で **システム パラメータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="54fe8-123">**一般** タブで **Teams アプリの通知を有効にする** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![システム パラメータで Teams アプリの通知を有効にする](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="54fe8-125">すべてのユーザーに対して Teams の通知をオンにするには、プロンプトで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![すべてのユーザーに対して Teams の通知を有効にする](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="54fe8-127">個々のユーザーの Teams の通知をオンまたはオフにする</span><span class="sxs-lookup"><span data-stu-id="54fe8-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="54fe8-128">Teams の Dynamics 365 Human Resources アプリの通知を有効にした後、ユーザーごとに通知をオンまたはオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="54fe8-129">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="54fe8-130">**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-130">Select **Links**.</span></span>

3. <span data-ttu-id="54fe8-131">**ユーザー** で **ユーザー オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="54fe8-132">**ワークフロー** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="54fe8-133">**Teams アプリの通知を有効にする** を **はい** に設定するとユーザーへの通知が有効になり、**いいえ** に設定するとユーザーへの通知が無効になります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![ユーザー オプションのワークフロー タブで Teams アプリの通知を有効にする](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="54fe8-135">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="54fe8-136">対応している言語</span><span class="sxs-lookup"><span data-stu-id="54fe8-136">Supported languages</span></span>

<span data-ttu-id="54fe8-137">Teams の Dynamics 365 Human Resources アプリでは、次の言語がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="54fe8-138">ロケール ID</span><span class="sxs-lookup"><span data-stu-id="54fe8-138">Locale ID</span></span> | <span data-ttu-id="54fe8-139">言語</span><span class="sxs-lookup"><span data-stu-id="54fe8-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="54fe8-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="54fe8-140">de-DE</span></span> | <span data-ttu-id="54fe8-141">ドイツ語 (ドイツ)</span><span class="sxs-lookup"><span data-stu-id="54fe8-141">German (Germany)</span></span> |
| <span data-ttu-id="54fe8-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="54fe8-142">es-ES</span></span> | <span data-ttu-id="54fe8-143">スペイン語 (スペイン)</span><span class="sxs-lookup"><span data-stu-id="54fe8-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="54fe8-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="54fe8-144">es-MX</span></span> | <span data-ttu-id="54fe8-145">スペイン語 (メキシコ)</span><span class="sxs-lookup"><span data-stu-id="54fe8-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="54fe8-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="54fe8-146">fr-CA</span></span> | <span data-ttu-id="54fe8-147">フランス語 (カナダ)</span><span class="sxs-lookup"><span data-stu-id="54fe8-147">French (Canada)</span></span> |
| <span data-ttu-id="54fe8-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="54fe8-148">fr-FR</span></span> | <span data-ttu-id="54fe8-149">フランス語 (フランス)</span><span class="sxs-lookup"><span data-stu-id="54fe8-149">French (France)</span></span> |
| <span data-ttu-id="54fe8-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="54fe8-150">it-IT</span></span> | <span data-ttu-id="54fe8-151">イタリア語 (イタリア)</span><span class="sxs-lookup"><span data-stu-id="54fe8-151">Italian (Italy)</span></span> |
| <span data-ttu-id="54fe8-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="54fe8-152">nl-NL</span></span> | <span data-ttu-id="54fe8-153">オランダ語 (オランダ)</span><span class="sxs-lookup"><span data-stu-id="54fe8-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="54fe8-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="54fe8-154">pt-BR</span></span> | <span data-ttu-id="54fe8-155">ポルトガル語 (ブラジル)</span><span class="sxs-lookup"><span data-stu-id="54fe8-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="54fe8-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="54fe8-156">tr-TR</span></span> | <span data-ttu-id="54fe8-157">トルコ語 (トルコ)</span><span class="sxs-lookup"><span data-stu-id="54fe8-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="54fe8-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="54fe8-158">zh-CN</span></span> | <span data-ttu-id="54fe8-159">中国語 (簡体)</span><span class="sxs-lookup"><span data-stu-id="54fe8-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="54fe8-160">摘要</span><span class="sxs-lookup"><span data-stu-id="54fe8-160">Notes</span></span>

<span data-ttu-id="54fe8-161">今後のリリースでは、次の作業項目が予定されています。</span><span class="sxs-lookup"><span data-stu-id="54fe8-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="54fe8-162">作業項目</span><span class="sxs-lookup"><span data-stu-id="54fe8-162">Work item</span></span> | <span data-ttu-id="54fe8-163">状態</span><span class="sxs-lookup"><span data-stu-id="54fe8-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="54fe8-164">未来日付の休暇を送信する場合に、残日数に誤りがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="54fe8-165">予測機能は未実装です。</span><span class="sxs-lookup"><span data-stu-id="54fe8-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="54fe8-166">現在日付の残日数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="54fe8-167">**レビュー中** の申請をキャンセルできない 。</span><span class="sxs-lookup"><span data-stu-id="54fe8-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="54fe8-168">この機能には現在対応していないため、今後のリリースで対応予定です。</span><span class="sxs-lookup"><span data-stu-id="54fe8-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="54fe8-169">残日数情報が、現日付の時点に基づいて算出される。</span><span class="sxs-lookup"><span data-stu-id="54fe8-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="54fe8-170">現在のシステムでは、休暇と欠勤のパラメータで構成されている場合であっても、見越計上期間の残日数は表示されません。</span><span class="sxs-lookup"><span data-stu-id="54fe8-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="54fe8-171">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="54fe8-171">Troubleshooting</span></span>

<span data-ttu-id="54fe8-172">ユーザーが Teams の Human Resources アプリへのサインインまたは使用で問題が発生した場合は、次のトラブルシューティングの手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="54fe8-173">トラブルシューティング後も問題が解決しない場合は、サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="54fe8-174">詳細については、[サポート](hr-admin-troubleshooting-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-174">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="54fe8-175">Teams の Human Resources アプリにサインインできない</span><span class="sxs-lookup"><span data-stu-id="54fe8-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="54fe8-176">ユーザーがアプリにサインインできないために連絡した場合は、そのユーザーが Human Resources に関連付けられている従業員レコードを持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="54fe8-177">Teams の Human Resources アプリで休暇申請を承認する際のエラー</span><span class="sxs-lookup"><span data-stu-id="54fe8-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="54fe8-178">Teams アプリで休暇申請を承認しようとしたときにユーザーがエラーを受信した場合は、次のトラブルシューティングの手順を試行します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="54fe8-179">Teams のアカウントが、Human Resources へのアクセスに使用するものと同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="54fe8-180">休暇承認のワークフロー設定を確認して、要求の有効な承認者であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="54fe8-181">休暇申請ワークフローの詳細については、[休暇申請ワークフローの作成](hr-leave-and-absence-workflow.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="54fe8-182">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="54fe8-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="54fe8-183">Microsoft Language Understanding インテリジェント サービス (LUIS)</span><span class="sxs-lookup"><span data-stu-id="54fe8-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="54fe8-184">Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="54fe8-185">ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="54fe8-186">LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="54fe8-187">LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。</span><span class="sxs-lookup"><span data-stu-id="54fe8-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="54fe8-188">この情報は、Microsoft の  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="54fe8-189">ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="54fe8-190">LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="54fe8-191">LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="54fe8-192">ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。</span><span class="sxs-lookup"><span data-stu-id="54fe8-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="54fe8-193">認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="54fe8-194">Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="54fe8-195">Microsoft Teams、Azure Event Grid、Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="54fe8-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="54fe8-196">Microsoft Teams 内で Dynamics 365 Human Resources アプリを使用する場合、特定の顧客データが、テナントの Human Resources サービスが展開されている地域外に流出する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54fe8-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="54fe8-197">Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。</span><span class="sxs-lookup"><span data-stu-id="54fe8-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="54fe8-198">このデータは、Microsoft Azure Event Grid に最大 24 時間保存でき、米国内で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="54fe8-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="54fe8-199">データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="54fe8-200">Human Resources アプリでチャット ボットと会話しながら、会話の内容を Azure Cosmos DB に保存し、Microsoft Teams に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="54fe8-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="54fe8-201">このデータは Azure Cosmos DB に最大24時間格納され、テナントの Human Resources サービスが展開されている地域外で処理される可能性があり、転送中および保存中に暗号化され、トレーニングやサービス改善のために Microsoft またはそのサブプロセッサが使用することはありません。</span><span class="sxs-lookup"><span data-stu-id="54fe8-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="54fe8-202">データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="54fe8-203">組織または組織内のユーザーの Microsoft Teams の Human Resources アプリへのアクセスを制限するには、[Microsoft Teams におけるアプリのアクセス許可ポリシーの管理](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fe8-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="54fe8-204">参照</span><span class="sxs-lookup"><span data-stu-id="54fe8-204">See also</span></span> 

[<span data-ttu-id="54fe8-205">Microsoft Teams のダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="54fe8-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="54fe8-206">Microsoft Teams ヘルプ センター</span><span class="sxs-lookup"><span data-stu-id="54fe8-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="54fe8-207">Teams での休暇要求の管理</span><span class="sxs-lookup"><span data-stu-id="54fe8-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]