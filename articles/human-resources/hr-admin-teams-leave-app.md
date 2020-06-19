---
title: Teams における人事管理アプリ
description: このトピックでは、Microsoft Teams における Microsoft Dynamics 365 Human Resources について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431133"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="b77fc-103">Teams における人事管理アプリ</span><span class="sxs-lookup"><span data-stu-id="b77fc-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="b77fc-104">Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用すると、従業員は簡単に休暇を申請することができ、Microsoft Teams にて休暇の残日数情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="b77fc-105">従業員は bot と対話して情報を要求できます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="b77fc-106">**休暇** タブには、より詳細な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-106">The **Time off** tab provides more detailed information.</span></span>

![Teams Human Resources の休暇アプリ ボット](./media/hr-admin-teams-leave-app-bot.png)

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="b77fc-109">インストールと設定</span><span class="sxs-lookup"><span data-stu-id="b77fc-109">Install and setup</span></span>

<span data-ttu-id="b77fc-110">Human Resources アプリは、Teams ストアにあります。</span><span class="sxs-lookup"><span data-stu-id="b77fc-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="b77fc-111">Teams アプリのインストールについては、[Teams で休暇申請を管理する](hr-teams-leave-app.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="b77fc-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="b77fc-112">Teams におけるアプリのアクセス許可の管理については、[Microsoft Teams におけるアプリのアクセス許可ポリシーを管理する](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b77fc-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="b77fc-113">既知の問題</span><span class="sxs-lookup"><span data-stu-id="b77fc-113">Known issues</span></span>

| <span data-ttu-id="b77fc-114">問題</span><span class="sxs-lookup"><span data-stu-id="b77fc-114">Issue</span></span> | <span data-ttu-id="b77fc-115">ステータス</span><span class="sxs-lookup"><span data-stu-id="b77fc-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="b77fc-116">エラー: 接続する環境の検索に問題があります。</span><span class="sxs-lookup"><span data-stu-id="b77fc-116">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="b77fc-117">このエラーは、ユーザーが 1 つ以上の Human Resources 環境にアクセスできることを確認した場合でも、表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="b77fc-117">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="b77fc-118">また、予期するすべての環境が表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b77fc-118">In addtion, you might not see all the environments you expect.</span></span> <span data-ttu-id="b77fc-119">この問題を修正するまでは、ユーザーを削除してから再度インポートして問題を解決してください。</span><span class="sxs-lookup"><span data-stu-id="b77fc-119">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="b77fc-120">未来日付の休暇を送信する場合に、残日数に誤りがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="b77fc-120">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="b77fc-121">予測機能は未実装です。</span><span class="sxs-lookup"><span data-stu-id="b77fc-121">Forecasting isn't yet available.</span></span> <span data-ttu-id="b77fc-122">現在日付の残日数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-122">The balance displays for the current date.</span></span> |
| <span data-ttu-id="b77fc-123">既存の申請で要した時間数を減らすと、**残日数**が加算されずに減算される。</span><span class="sxs-lookup"><span data-stu-id="b77fc-123">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="b77fc-124">この既知の問題については、将来的に対応予定です。</span><span class="sxs-lookup"><span data-stu-id="b77fc-124">We'll address this known issue in the future.</span></span> <span data-ttu-id="b77fc-125">表示内容は正しくありませんが、送信時に正しい日数が調整されます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-125">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="b77fc-126">同じ日付に対して、**今後の休暇**カードが2つ表示される。</span><span class="sxs-lookup"><span data-stu-id="b77fc-126">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="b77fc-127">これらのカードはそれぞれ個別の提出を意味しています。</span><span class="sxs-lookup"><span data-stu-id="b77fc-127">The cards represent individual submissions.</span></span> <span data-ttu-id="b77fc-128">今後も継続的にフィードバックを受け、調整を行っていきます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-128">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="b77fc-129">**レビュー中**の申請をキャンセルできない 。</span><span class="sxs-lookup"><span data-stu-id="b77fc-129">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="b77fc-130">この機能には現在対応していないため、今後のリリースで対応予定です。</span><span class="sxs-lookup"><span data-stu-id="b77fc-130">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="b77fc-131">残日数情報が、現日付の時点に基づいて算出される。</span><span class="sxs-lookup"><span data-stu-id="b77fc-131">Balance information is calculated as of today.</span></span> | <span data-ttu-id="b77fc-132">現在のシステムでは、休暇と欠勤のパラメータで構成されている場合であっても、見越計上期間の残日数は表示されません。</span><span class="sxs-lookup"><span data-stu-id="b77fc-132">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="b77fc-133">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="b77fc-133">Privacy notice</span></span>

<span data-ttu-id="b77fc-134">Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-134">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="b77fc-135">ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-135">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="b77fc-136">LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b77fc-136">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="b77fc-137">LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。</span><span class="sxs-lookup"><span data-stu-id="b77fc-137">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="b77fc-138">この情報は、Microsoft の [Azure ボット フレームワーク](https://azure.microsoft.com/services/bot-service/)に渡され、 Dynamics 365 Human Resources のデータと対話し、ユーザーのクエリに必要な情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="b77fc-138">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="b77fc-139">ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="b77fc-139">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="b77fc-140">LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b77fc-140">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b77fc-141">LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b77fc-141">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="b77fc-142">ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。</span><span class="sxs-lookup"><span data-stu-id="b77fc-142">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="b77fc-143">認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b77fc-143">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="b77fc-144">Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。</span><span class="sxs-lookup"><span data-stu-id="b77fc-144">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="b77fc-145">参照</span><span class="sxs-lookup"><span data-stu-id="b77fc-145">See also</span></span> 

[<span data-ttu-id="b77fc-146">Microsoft Teams のダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="b77fc-146">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="b77fc-147">Microsoft Teams ヘルプ センター</span><span class="sxs-lookup"><span data-stu-id="b77fc-147">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="b77fc-148">Teams で休暇申請を管理する</span><span class="sxs-lookup"><span data-stu-id="b77fc-148">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

