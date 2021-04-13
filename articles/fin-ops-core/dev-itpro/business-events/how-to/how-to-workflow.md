---
title: ビジネス イベントおよびワークフローの承認
description: このトピックでは Microsoft Power Automate を使用して購買申請を承認するワークフロー ビジネス イベントを構成して使用する方法を説明します。
author: Sunil-Garg
ms.date: 11/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 23f27def8a59a6aaaa6fb46eebb867235a656126
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745355"
---
# <a name="business-events-and-workflow-approvals"></a><span data-ttu-id="8578d-103">ビジネス イベントおよびワークフローの承認</span><span class="sxs-lookup"><span data-stu-id="8578d-103">Business events and workflow approvals</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8578d-104">このトピックでは Microsoft Power Automate を使用して購買申請を承認するワークフロー ビジネス イベントを構成して使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8578d-104">This topic explains how to use Microsoft Power Automate to configure and consume a workflow business event for purchase requisition approval.</span></span>

<span data-ttu-id="8578d-105">このトピックを完了するには、プラットフォーム アップデート 26 以降で Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.2 (2019 年 5 月) を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8578d-105">To complete this topic, you must be running Microsoft Dynamics 365 for Finance and Operations version 10.0.2 (May 2019) with platform update 26 or later.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="8578d-106">シナリオの概要</span><span class="sxs-lookup"><span data-stu-id="8578d-106">Scenario overview</span></span>

<span data-ttu-id="8578d-107">次の図は Power Automate を使用して構成する必要がある高レベル プロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="8578d-107">The following illustration shows the high-level process that you must configure by using Power Automate.</span></span> <span data-ttu-id="8578d-108">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="8578d-108">Note the following points:</span></span>

1. <span data-ttu-id="8578d-109">アプリケーションは、新しい承認が開始するたびにビジネス イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="8578d-109">The application fires a business event whenever a new approval starts.</span></span>
2. <span data-ttu-id="8578d-110">Power Automate トリガーが開始されます。</span><span class="sxs-lookup"><span data-stu-id="8578d-110">Power Automate trigger starts.</span></span> 
3. <span data-ttu-id="8578d-111">F&O からビジネス イベント ペイロードを解析した後、次のステップは F&O から受信したワークフロー インスタンス ID がまだ有効か確認することです。</span><span class="sxs-lookup"><span data-stu-id="8578d-111">After parsing business event payload from F&O, next step is to check wheter the workflow instance ID received from F&O is still alive.</span></span> <span data-ttu-id="8578d-112">これは、承認が既に行われた場合、またはワークフローが取り消された場合のセキュリティ ステップです。</span><span class="sxs-lookup"><span data-stu-id="8578d-112">This is a security step in case approval has already taken place or workflow has been recalled.</span></span>
4. <span data-ttu-id="8578d-113">確認が失敗すると、ワークスペース内の潜在的な作業項目についてユーザーに通知する電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8578d-113">If the check is unsuccessful, an email is sent to notify the user about a potential work item in their workspace.</span></span>
4. <span data-ttu-id="8578d-114">確認が成功すると新しい Power Automate の承認が開始されます。</span><span class="sxs-lookup"><span data-stu-id="8578d-114">If the check is successful, a new Power Automate approval is started.</span></span>
5. <span data-ttu-id="8578d-115">次に、承認の結果を使用してワークフローが完了します。</span><span class="sxs-lookup"><span data-stu-id="8578d-115">Then workflow is completed by using the outcome of the approval.</span></span> <span data-ttu-id="8578d-116">結果は **承認** または **否認** のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="8578d-116">The outcome can be either **Approve** or **Reject**.</span></span>

<img alt="Scenario overview"  src="../../media/BEF-Howto-workflow-01.png" width="70%">

## <a name="exercise-1-create-a-new-flow"></a><span data-ttu-id="8578d-117">練習 1: 新しいフローの作成</span><span class="sxs-lookup"><span data-stu-id="8578d-117">Exercise 1: Create a new flow</span></span>

1. <span data-ttu-id="8578d-118">Power Automate ポータルにサインインします。</span><span class="sxs-lookup"><span data-stu-id="8578d-118">Sign in to the Power Automate portal.</span></span>
2. <span data-ttu-id="8578d-119">フロー リソースを作成する権限がある既存の環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-119">Select an existing environment where you have the right to create a flow resource.</span></span> <span data-ttu-id="8578d-120">**(既定)** 環境はすべての会社が利用できます。</span><span class="sxs-lookup"><span data-stu-id="8578d-120">The **(default)** environment is available to all companies.</span></span>
3. <span data-ttu-id="8578d-121">**空白から新規 \> を作成する** 選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-121">Select **New \> Create from blank**.</span></span>
4. <span data-ttu-id="8578d-122">**Dynamics 365 for Finance and Operations** を検索して、コネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-122">Search for **Dynamics 365 for Finance and Operations**, and select the connector.</span></span>
5. <span data-ttu-id="8578d-123">新しいトリガーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8578d-123">A new trigger is created.</span></span> <span data-ttu-id="8578d-124">このトリガーの名前は **ビジネス イベントの発生時** です。</span><span class="sxs-lookup"><span data-stu-id="8578d-124">This trigger is named **When a Business Event occurs**.</span></span> <span data-ttu-id="8578d-125">それを選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-125">Select it.</span></span>
6. <span data-ttu-id="8578d-126">次の特性を持つ環境インスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-126">Select the environment instance that has these characteristics:</span></span> 

    - <span data-ttu-id="8578d-127">カテゴリは **ワークフロー作業項目** です。</span><span class="sxs-lookup"><span data-stu-id="8578d-127">The category is **Workflow workitem**.</span></span>
    - <span data-ttu-id="8578d-128">イベント名は **購買要求の確認 (000062) – 購買要求の承認** です。</span><span class="sxs-lookup"><span data-stu-id="8578d-128">The event name is **Purchase requisition review (000062) – Approve purchase requisitions**.</span></span>
    - <span data-ttu-id="8578d-129">任意の法人が選択されます。</span><span class="sxs-lookup"><span data-stu-id="8578d-129">Any legal entity is selected.</span></span>

7. <span data-ttu-id="8578d-130">**新規ステップ** を選択して新しいアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="8578d-130">Select **New Step** to add a new action.</span></span>
8. <span data-ttu-id="8578d-131">**JSON の解析** データ処理を検索します。</span><span class="sxs-lookup"><span data-stu-id="8578d-131">Search for the **Parse Json** data operation.</span></span> <span data-ttu-id="8578d-132">このステップは、アプリケーションが提供するデータ コントラクトのスキーマを使用してメッセージを解析するために必要です。</span><span class="sxs-lookup"><span data-stu-id="8578d-132">This step is required so that the message can be parsed by using the schema of the data contract that the application provides.</span></span>
9. <span data-ttu-id="8578d-133">**Json 解析** アクションのコンテンツ フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-133">Select the content field of the **Parse Json** action.</span></span> <span data-ttu-id="8578d-134">前の手順の **本文** 出力がオプションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="8578d-134">The **Body** output from the previous step should appear as an option.</span></span> <span data-ttu-id="8578d-135">**Body** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-135">Select **Body**.</span></span>

    <span data-ttu-id="8578d-136">次に、契約のスキーマを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8578d-136">Next, you must enter the schema of the contract.</span></span> <span data-ttu-id="8578d-137">アプリケーションでは、サンプル ペイロードのみ提供します。</span><span class="sxs-lookup"><span data-stu-id="8578d-137">The application provides only a sample payload.</span></span> <span data-ttu-id="8578d-138">ただし Microsoft Flow の機能を使用してペイロードからスキーマを生成できます。</span><span class="sxs-lookup"><span data-stu-id="8578d-138">However, you can use a capability of Microsoft Flow to generate a schema from a payload.</span></span>

10. <span data-ttu-id="8578d-139">カタログの **000062** ワークフロー イベントを選択し、**スキーマのダウンロード** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-139">Select the **000062** workflow event in the catalog, and then select the **Download schema** link.</span></span> <span data-ttu-id="8578d-140">ダウンロードしたテキスト ファイルを開いて内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="8578d-140">Open the text file that is downloaded, and copy the contents.</span></span>
11. <span data-ttu-id="8578d-141">Power Automate に戻り、**サンプル ペイロードを使用してスキーマを生成** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-141">Go back to Power Automate, and select the **Use sample payload to generate schema** link.</span></span> <span data-ttu-id="8578d-142">テキスト ファイルの内容を貼り付けて **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-142">Paste the contents of the text file, and then select **Done**.</span></span>
12. <span data-ttu-id="8578d-143">新しいステップを追加して、正しいインスタンス ID を持つワークフローが実行中で承認を待っているか検証するワークフロー アクションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8578d-143">Add a new step to call a workflow action that validates whether a workflow that has the correct instance ID is running and awaiting approval.</span></span>

    <img alt="workitem validate action" src="../../media/BEF-Howto-workflow-08.png" width="70%">

13. <span data-ttu-id="8578d-144">検証アクションの結果を確認する新しい条件コントロール ステップを追加します。</span><span class="sxs-lookup"><span data-stu-id="8578d-144">Add a new condition control step to check the result of the validate action.</span></span> <span data-ttu-id="8578d-145">動的フィールドは必要な出力を提供しません。</span><span class="sxs-lookup"><span data-stu-id="8578d-145">The dynamic field won't provide the required output.</span></span> <span data-ttu-id="8578d-146">したがって、代わりに次の式を手動で入力する必要があります: **Body('Execute_action')?\['value'\]**</span><span class="sxs-lookup"><span data-stu-id="8578d-146">Therefore, you must manually enter the following expression instead: **Body('Execute_action')?\['value'\]**.</span></span> <span data-ttu-id="8578d-147">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-147">Then select **OK**.</span></span>

    <img alt="Microsoft Power Automate expression" src="../../media/BEF-Howto-workflow-09.png" width="70%">

    > [!NOTE]
    > <span data-ttu-id="8578d-148">次にワークフローを開いたときに式が更新されて **値** フィールドが表示されることがわかります。</span><span class="sxs-lookup"><span data-stu-id="8578d-148">The next time that you open the workflow, you will notice that the expression has been updated so that it shows the **value** field.</span></span> <span data-ttu-id="8578d-149">次の図に示すように、このフィールドにはアプリケーション アイコンがあります。</span><span class="sxs-lookup"><span data-stu-id="8578d-149">As the following illustration shows, this field will have an application icon.</span></span>

    <img alt="expression value" src="../../media/BEF-Howto-workflow-10.png" width="70%">

14. <span data-ttu-id="8578d-150">条件コントロールは **はい**/**いいえ** 結果の 2 つの分岐を自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="8578d-150">The condition control automatically creates two branches for **Yes**/**No** results.</span></span> <span data-ttu-id="8578d-151">検証ステップの結果が **いいえ** の場合、ユーザーに電子メールを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8578d-151">If the result of the validate step is **No**, an email must be sent to the user.</span></span> <span data-ttu-id="8578d-152">この電子メールは、新しいタスクには注意が必要であり、クライアントにサイン インする必要があることをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="8578d-152">This email notifies the user that a new task requires attention, and that the user must sign in to the client.</span></span> <span data-ttu-id="8578d-153">このステップを完了するには、**いいえ** コンテナに新しい電子メール送信アクションを作成し、前のステップ **workflowuseremail** からの承認者の電子メール、選択した件名と本文を、パラメーターに入力します。</span><span class="sxs-lookup"><span data-stu-id="8578d-153">In order to complete this step create a new send email action within the **No** container and fill in the parameter with the email of the Approver from the previous step **workflowuseremail** and a subject and body of your choice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8578d-154">ワークフロー ビジネス イベントが返す電子メール アドレスは、ワークフロー承認者の電子メール アドレスです。</span><span class="sxs-lookup"><span data-stu-id="8578d-154">The email address that the workflow business event returns is the email address of the workflow approver.</span></span> <span data-ttu-id="8578d-155">デモ環境でワークフロー承認者ユーザーが構成されていない場合、デモに自分の電子メール アドレスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8578d-155">If the workflow approver user hasn't been configured in yourdemo environment, you can use your own email address for demo purposes.</span></span>

    <img alt="approver email" src="../../media/BEF-Howto-workflow-11.png" width="70%">

15. <span data-ttu-id="8578d-156">検証ステップの結果が **はい** の場合、新しい Power Automate 承認ステップを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8578d-156">If the result of the validate step is **Yes**, you must start a new Power Automate approval step.</span></span> <span data-ttu-id="8578d-157">**はい** コンテナで **開始して承認を待つ (v2)** という名前の新しいアクションを選択し、次のように入力を選択します。承認タイプ: 承認/拒否 最初に応答するタイトル: **workflowworkitemsubject** 出力フォーム ビジネスイベントペイロード割り当て先: **workflowuseremail** 出力 その後、**workflowdocument** や **workflowstepinstruction** などの前のステップで必要な情報を詳細セクションに入力できます。</span><span class="sxs-lookup"><span data-stu-id="8578d-157">In the **Yes** container, select a new action that is named **Start and wait for an approval (v2)**, and choose inputs as follows: Approval type: Approve/reject: first to respond title: **workflowworkitemsubject** output form Business event payload Assigned to: **workflowuseremail** output Then you can fill in the details section with as much information as needed from previous step such as **workflowdocument** or **workflowstepinstruction**.</span></span> <span data-ttu-id="8578d-158">繰り返しになりますが、特にワークフロー承認者ユーザーがデモ環境で構成されていない場合は、デモ目的で **割り当て先** フィールドで自分の電子メールアドレスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8578d-158">Again, you can use your own email address in the **Assigned to** field for demo purposes especially if the workflow approver user hasn't been configured in your demo environment.</span></span>

    <img alt="Microsoft Power Automate approval" src="../../media/BEF-Howto-workflow-12.png" width="70%">

16. <span data-ttu-id="8578d-159">次に、承認ステップの結果を使用してワークフローの承認を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8578d-159">Next, you must complete the workflow approval by using the outcome of the approval step.</span></span> <span data-ttu-id="8578d-160">さらに **はい** コンテナに新しい **Finance and Operations 実行アクション** を追加し、**WorkflowWorkitem-complete** アクションと **WorkflowWorkitemInstanceID** パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-160">Still in the **Yes** container, add a new **Finance and Operations Execute Action** step, and choose the **WorkflowWorkitem-complete** action and the **WorkflowWorkitemInstanceID** parameter.</span></span> <span data-ttu-id="8578d-161">次に、承認出力から残りのパラメーターを入力します。</span><span class="sxs-lookup"><span data-stu-id="8578d-161">Then fill in the rest of the parameters from the approval outputs.</span></span> <span data-ttu-id="8578d-162">最低限の承認結果がある結果セクションと、承認者の応答があるコメント セクション。</span><span class="sxs-lookup"><span data-stu-id="8578d-162">As a minimum the outcome section with Approval outcome and the comment section with the approver's responses.</span></span> <span data-ttu-id="8578d-163">承認ステップは複数の承認者をサポートできるため、応答出力は配列です。</span><span class="sxs-lookup"><span data-stu-id="8578d-163">Because the approval step can support multiple approvers, the response output is an array.</span></span> <span data-ttu-id="8578d-164">したがって、コメント セクションの入力として出力 **応答** を選択すると、すぐに以下に示すように Power Automate はアクションを **それぞれに適用** コンテナに自動的に埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="8578d-164">Therefore, as soon as you select the output **Reponses** as an input for the comment section, Power Automate automatically embeds your action in an **Apply to each** container as shown below.</span></span>

    <img alt="workitem complete action" src="../../media/BEF-Howto-workflow-13.png" width="70%">

17. <span data-ttu-id="8578d-165">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-165">Select **Save**.</span></span>

## <a name="exercise-2-trigger-a-business-event"></a><span data-ttu-id="8578d-166">練習 2: ビジネス イベントのトリガー</span><span class="sxs-lookup"><span data-stu-id="8578d-166">Exercise 2: Trigger a business event</span></span>

<span data-ttu-id="8578d-167">Power Automate では、アプリケーションを自動的にコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="8578d-167">Power Automate can automatically configure the application for you.</span></span> <span data-ttu-id="8578d-168">フローを保存すると、Power Automate でエンドポイントが作成され、ビジネス イベントが有効となります。</span><span class="sxs-lookup"><span data-stu-id="8578d-168">After you save your flow, Power Automate creates an endpoint and activates the business event.</span></span> <span data-ttu-id="8578d-169">その他のコンフィギュレーションを完了する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8578d-169">You don't have to complete any other configurations.</span></span> <span data-ttu-id="8578d-170">エンドポイントが正しく構成されてたことを確認してからイベントをトリガーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8578d-170">You just have to verify that the endpoint has been correctly configured and then trigger an event.</span></span>

1. <span data-ttu-id="8578d-171">クライアントにサイン インします。</span><span class="sxs-lookup"><span data-stu-id="8578d-171">Sign in to the client.</span></span>
2. <span data-ttu-id="8578d-172">**システム管理 \> 設定 \> ビジネス イベント** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8578d-172">Go to **System administration \> Setup \> Business events**.</span></span>
3. <span data-ttu-id="8578d-173">**ビジネス イベント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-173">Select **Business events**.</span></span>
4. <span data-ttu-id="8578d-174">**エンドポイント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8578d-174">Select **Endpoints**.</span></span>
5. <span data-ttu-id="8578d-175">新しいエンドポイントが作成されたこと、そしてグローバル一意識別子 (GUID) が名前に追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8578d-175">Verify that a new endpoint has been created, and that a globally unique identifier (GUID) has been appended to the name.</span></span>
6. <span data-ttu-id="8578d-176">**有効なイベント** タブで、USMF 会社の **ワークフロー作業項目** がアクティブにであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8578d-176">On the **Active events** tab, verify that **Workflow workitem** is activated for the USMF company.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]