---
title: Teams における人事管理アプリ
description: このトピックでは、Microsoft Teams における Microsoft Dynamics 365 Human Resources について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776311"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="5a1a8-103">Teams における人事管理アプリ</span><span class="sxs-lookup"><span data-stu-id="5a1a8-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5a1a8-104">Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用すると、従業員は簡単に休暇を申請することができ、Microsoft Teams にて休暇の残日数情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="5a1a8-105">従業員は bot と対話して情報を要求できます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="5a1a8-106">**休暇** タブには、より詳細な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-106">The **Time off** tab provides more detailed information.</span></span>

![Teams Human Resources の休暇アプリ ボット](./media/hr-admin-teams-leave-app-bot.png)

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="5a1a8-109">インストールと設定</span><span class="sxs-lookup"><span data-stu-id="5a1a8-109">Install and setup</span></span>

<span data-ttu-id="5a1a8-110">Human Resources アプリは、Teams ストアにあります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="5a1a8-111">Teams アプリのインストールについては、[Teams で休暇申請を管理する](hr-teams-leave-app.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="5a1a8-112">Teams におけるアプリのアクセス許可の管理については、[Microsoft Teams におけるアプリのアクセス許可ポリシーを管理する](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="5a1a8-113">Teams の Human Resources アプリの通知を有効にする</span><span class="sxs-lookup"><span data-stu-id="5a1a8-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="5a1a8-114">ユーザーが Teams アプリで休暇申請通知を受け取るようにするには、Human Resources で通知を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="5a1a8-115">Teams にサインインしていて、Teams の Human Resources アプリを使用しているユーザーだけが、通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="5a1a8-116">人事管理では、**システム管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="5a1a8-117">**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-117">Select **Links**.</span></span>

3. <span data-ttu-id="5a1a8-118">**設定** で **システム パラメータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="5a1a8-119">**一般** タブで **Teams アプリの通知を有効にする** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![システム パラメータで Teams アプリの通知を有効にする](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="5a1a8-121">すべてのユーザーに対して Teams の通知をオンにするには、プロンプトで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![すべてのユーザーに対して Teams の通知を有効にする](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="5a1a8-123">個々のユーザーの Teams の通知をオンまたはオフにする</span><span class="sxs-lookup"><span data-stu-id="5a1a8-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="5a1a8-124">Teams の Human Resources アプリの通知を有効にした後、ユーザーごとに通知をオンまたはオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="5a1a8-125">人事管理では、**システム管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="5a1a8-126">**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-126">Select **Links**.</span></span>

3. <span data-ttu-id="5a1a8-127">**ユーザー** で **ユーザー オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="5a1a8-128">**ワークフロー** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="5a1a8-129">**Teams アプリの通知を有効にする** を **はい** に設定するとユーザーへの通知が有効になり、**いいえ** に設定するとユーザーへの通知が無効になります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![ユーザー オプションのワークフロー タブで Teams アプリの通知を有効にする](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="5a1a8-131">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="5a1a8-132">既知の問題</span><span class="sxs-lookup"><span data-stu-id="5a1a8-132">Known issues</span></span>

| <span data-ttu-id="5a1a8-133">出庫</span><span class="sxs-lookup"><span data-stu-id="5a1a8-133">Issue</span></span> | <span data-ttu-id="5a1a8-134">ステータス</span><span class="sxs-lookup"><span data-stu-id="5a1a8-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="5a1a8-135">Android フォンで水平スクロールが機能しない</span><span class="sxs-lookup"><span data-stu-id="5a1a8-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="5a1a8-136">水平スクロールは iOS または デスクトップ デバイスでは問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="5a1a8-137">Android の修正プログラムに取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="5a1a8-138">エラー: 接続する環境の検索に問題があります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="5a1a8-139">このエラーは、ユーザーが 1 つ以上の Human Resources 環境にアクセスできることを確認した場合でも、表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="5a1a8-140">また、予期するすべての環境が表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="5a1a8-141">この問題を修正するまでは、ユーザーを削除してから再度インポートして問題を解決してください。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="5a1a8-142">未来日付の休暇を送信する場合に、残日数に誤りがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="5a1a8-143">予測機能は未実装です。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="5a1a8-144">現在日付の残日数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="5a1a8-145">**レビュー中**の申請をキャンセルできない 。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="5a1a8-146">この機能には現在対応していないため、今後のリリースで対応予定です。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="5a1a8-147">残日数情報が、現日付の時点に基づいて算出される。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="5a1a8-148">現在のシステムでは、休暇と欠勤のパラメータで構成されている場合であっても、見越計上期間の残日数は表示されません。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="5a1a8-149">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="5a1a8-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="5a1a8-150">Microsoft Language Understanding インテリジェント サービス (LUIS)</span><span class="sxs-lookup"><span data-stu-id="5a1a8-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="5a1a8-151">Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="5a1a8-152">ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="5a1a8-153">LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="5a1a8-154">LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="5a1a8-155">この情報は、Microsoft の  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="5a1a8-156">ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="5a1a8-157">LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5a1a8-158">LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="5a1a8-159">ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="5a1a8-160">認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="5a1a8-161">Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="5a1a8-162">Microsoft Azure Event Grid と Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5a1a8-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="5a1a8-163">Teams 内で Dynamics 365 Human Resources アプリの通知機能を使用する場合、特定の顧客データは、テナントの Human Resources サービスが展開される地域外に流出します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="5a1a8-164">Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="5a1a8-165">このデータは、最大 24 時間保存され、米国で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="5a1a8-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a1a8-166">参照</span><span class="sxs-lookup"><span data-stu-id="5a1a8-166">See also</span></span> 

[<span data-ttu-id="5a1a8-167">Microsoft Teams のダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="5a1a8-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="5a1a8-168">Microsoft Teams ヘルプ センター</span><span class="sxs-lookup"><span data-stu-id="5a1a8-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="5a1a8-169">Teams での休暇要求の管理</span><span class="sxs-lookup"><span data-stu-id="5a1a8-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

