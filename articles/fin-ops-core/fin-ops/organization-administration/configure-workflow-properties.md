---
title: ワークフロー プロパティのコンフィギュレーション
description: このトピックでは、ワークフローの各種プロパティをコンフィギュレーションする方法について説明します。
author: sericks007
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268448049955170b8eb9e64cbd50416565a041b1
ms.sourcegitcommit: 561d06c2a74602dfaa40334d8afac5053aebc055
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2020
ms.locfileid: "3541112"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="8fd3a-103">ワークフロー プロパティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8fd3a-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fd3a-104">このトピックでは、ワークフローの各種プロパティをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="8fd3a-105">ワークフローのプロパティをコンフィギュレーションするには、ワークフロー エディターでワークフローを開きます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="8fd3a-106">ワークフロー エディターのキャンバスをクリックし、**プロパティ**をクリックして、**プロパティ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="8fd3a-107">ワークフローの各種プロパティをコンフィギュレーションするには、次の手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="8fd3a-108">ワークフローに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="8fd3a-108">Name the workflow</span></span>

<span data-ttu-id="8fd3a-109">次の手順でワークフローの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="8fd3a-110">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8fd3a-111">**名前**フィールドに、ワークフローの固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="8fd3a-112">たとえば、事業を行っている国または地域ごとに購買要求ワークフローを作成する場合には、購買要求ワークフローの名前を**購買要求 (デンマーク)**、または**購買要求 (スペイン)** のようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="8fd3a-113">ワークフローの所有者の指定</span><span class="sxs-lookup"><span data-stu-id="8fd3a-113">Specify the workflow owner</span></span>

<span data-ttu-id="8fd3a-114">ワークフローの所有者とは、そのワークフローの管理と保守を行う人のことです。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="8fd3a-115">次の手順でワークフローの所有者を指定します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="8fd3a-116">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8fd3a-117">**所有者**一覧で、ワークフローの管理を行う人の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="8fd3a-118">電子メール テンプレートの選択</span><span class="sxs-lookup"><span data-stu-id="8fd3a-118">Select an email template</span></span>

<span data-ttu-id="8fd3a-119">このワークフローに関する通知メッセージを生成するのに使用する電子メール テンプレートを選択するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="8fd3a-120">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8fd3a-121">**ワークフロー通知の電子メール テンプレート**一覧で、テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="8fd3a-122">ユーザーに対する指示の入力</span><span class="sxs-lookup"><span data-stu-id="8fd3a-122">Enter instructions for users</span></span>

<span data-ttu-id="8fd3a-123">処理と承認を求めてドキュメントを送信するユーザーに指示を入力できます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="8fd3a-124">これらのユーザーは、*作成者* とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="8fd3a-125">たとえば、購買要求ワークフローを作成しており、指示を入力するとします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="8fd3a-126">これらの指示は、**購買要求**ページで、購買要求を入力するユーザーに対して表示できます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="8fd3a-127">指示を表示するには、作成者がワークフロー メッセージ バーのアイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="8fd3a-128">次の手順に従って、ユーザーに対する指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="8fd3a-129">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8fd3a-130">**送信指示**フィールドで、指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="8fd3a-131">指示を個人向けのものにするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="8fd3a-132">プレースホルダーは、指示行がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="8fd3a-133">プレースホルダーを挿入するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="8fd3a-134">**送信指示**フィールドをクリックして、プレースホルダを表示する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8fd3a-135">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8fd3a-136">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8fd3a-137">**挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-137">Click **Insert**.</span></span>

4. <span data-ttu-id="8fd3a-138">指示行の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="8fd3a-139">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="8fd3a-140">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8fd3a-141">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="8fd3a-142">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8fd3a-143">テキストをカスタマイズするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8fd3a-144">プレースホルダーを入力する方法については、ステップ 3 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="8fd3a-145">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="8fd3a-146">有効化条件を使用してこのワークフローがをいつ使用するかを指定する</span><span class="sxs-lookup"><span data-stu-id="8fd3a-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="8fd3a-147">同じワークフロー タイプに基づく複数のワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="8fd3a-148">同じタイプに基づくワークフローが複数ある場合は、有効化条件を使用して各ワークフローをいつ使用するかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="8fd3a-149">有効化条件が満たされていない場合は、既定のワークフローが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="8fd3a-150">同様に、ワークフロー タイプに定義されているワークフロー コンフィギュレーションが 1 つだけの場合、有効化条件に関係なく、そのワークフロー コンフィギュレーションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="8fd3a-151">たとえば、以下の条件で、購買要求 (デンマーク) と 購買要求 (スペイン) など事業を行っている国/地域ごとに、購買要求ワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="8fd3a-152">購買要求 (デンマーク) は、国/地域 = DK の場合に使用する</span><span class="sxs-lookup"><span data-stu-id="8fd3a-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="8fd3a-153">購買要求 (スペイン) は、国/地域 = ES の場合に使用する</span><span class="sxs-lookup"><span data-stu-id="8fd3a-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="8fd3a-154">次の手順を実行して、コンフィギュレーション内のワークフローをいつ使用するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="8fd3a-155">左ウィンドウで、**有効化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="8fd3a-156">**このワークフローを実行する条件を設定する**のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="8fd3a-157">**条件の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="8fd3a-158">条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-158">Enter a condition.</span></span>
5. <span data-ttu-id="8fd3a-159">必要に応じて、追加条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="8fd3a-160">一部のターゲット レコードでワークフローを実行して、レコードが条件に正しく含まれていること、およびレコードが除外されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="8fd3a-161">いつ通知を送信するかを指定する</span><span class="sxs-lookup"><span data-stu-id="8fd3a-161">Specify when notifications are sent</span></span>

<span data-ttu-id="8fd3a-162">処理のためにドキュメントが送信されると、ワークフロー インスタンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="8fd3a-163">このワークフローに基づくワークフロー インスタンスが開始、完了、打ち切り、またはエラーによって停止されたときに、ユーザーに通知を送信できます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="8fd3a-164">いつ通知を送信するかを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="8fd3a-165">左ウィンドウで、**通知**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="8fd3a-166">通知をトリガーする各イベントのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="8fd3a-167">**開始済** – ワークフロー インスタンスが開始されたときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="8fd3a-168">**停止済** – ワークフロー インスタンスがエラーで停止したときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="8fd3a-169">**完了** – ワークフロー インスタンスが完了したときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="8fd3a-170">**修復不可能** – ワークフロー インスタンスが、修復不可能なエラーで停止したときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="8fd3a-171">**終了** – ワークフロー インスタンスが打ち切られたときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="8fd3a-172">ステップ 2 で選択したイベントの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="8fd3a-173">**通知テキスト**タブで、通知のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="8fd3a-174">テキストをカスタマイズするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8fd3a-175">プレースホルダーは、テキストがユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="8fd3a-176">プレースホルダーを挿入するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="8fd3a-177">フィールド内でクリックして、プレースホルダーを表示する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8fd3a-178">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8fd3a-179">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8fd3a-180">**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="8fd3a-181">対象に含める共通の**通知テキスト**プレースホルダーは、前の手順からのすべてのコメントを表示する「前回のメモ: %Workflow.Last note%」です。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="8fd3a-182">テキストの翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="8fd3a-183">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="8fd3a-184">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="8fd3a-185">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="8fd3a-186">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8fd3a-187">テキストをカスタマイズするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="8fd3a-188">プレースホルダーを入力する方法の指示については、ステップ 5 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="8fd3a-189">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-189">Click **Close**.</span></span>

7. <span data-ttu-id="8fd3a-190">**受信者**タブで、次のオプションを使用して、通知の受信者を指定します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8fd3a-191">オプション</span><span class="sxs-lookup"><span data-stu-id="8fd3a-191">Option</span></span></th>
    <th><span data-ttu-id="8fd3a-192">通知はこれらのユーザーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="8fd3a-193">通知を送信するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8fd3a-194">参加者</span><span class="sxs-lookup"><span data-stu-id="8fd3a-194">Participant</span></span></td>
    <td><span data-ttu-id="8fd3a-195">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="8fd3a-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8fd3a-196"><strong>受信者</strong> タブで <strong>参加者</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="8fd3a-197"><strong>参加者のタイプ</strong> 一覧の、<strong>ロール ベース</strong> タブで、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="8fd3a-198"><strong>参加者</strong> の一覧で、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8fd3a-199">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="8fd3a-199">Workflow user</span></span></td>
    <td><span data-ttu-id="8fd3a-200">このワークフローの参加者であるユーザー</span><span class="sxs-lookup"><span data-stu-id="8fd3a-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8fd3a-201"><strong>受信者</strong> タブの、<strong>ワークフロー ユーザー</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="8fd3a-202"><strong>ワークフロー ユーザー</strong> の一覧の、<strong>ワークフロー ユーザー</strong> タブで、このワークフローの参加者を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8fd3a-203">ユーザー</span><span class="sxs-lookup"><span data-stu-id="8fd3a-203">User</span></span></td>
    <td><span data-ttu-id="8fd3a-204">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="8fd3a-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8fd3a-205"><strong>受信者</strong> タブの、<strong>ユーザー</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="8fd3a-206"><strong>ユーザー</strong>タブの<strong>利用可能なユーザー</strong>一覧には、すべての Dynamics AX ユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8fd3a-207">通知の送信先のユーザーを選択して、それらのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="8fd3a-208">ステップ 2 で選択したイベントごとに、ステップ 3～7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="8fd3a-209">ワークフローに加えた変更に関するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="8fd3a-210">このワークフローに加えた変更に関するコメントを入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="8fd3a-211">左ウィンドウで、**メモ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="8fd3a-212">**ワークフローに関するコメントの入力**フィールドにコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="8fd3a-213">入力したコメントを確認します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-213">Review your comments.</span></span> <span data-ttu-id="8fd3a-214">追加したコメントは変更できません。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="8fd3a-215">**追加**をクリックして、**コメントの履歴**領域にコメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="8fd3a-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
