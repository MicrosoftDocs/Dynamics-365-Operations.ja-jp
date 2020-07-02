---
title: ワークフローでの手動決定のコンフィギュレーション
description: このトピックでは、手動決定のプロパティをコンフィギュレーションする方法について説明します。
author: sericks007
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130cb50369c13bc3478340023c94f169ee5250cf
ms.sourcegitcommit: a5009c8958037afbaa1dd4f1469255b187ced93a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3455036"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="2ac37-103">ワークフローでの手動決定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2ac37-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ac37-104">このトピックでは、手動決定のプロパティをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="2ac37-105">ワークフロー エディターで手動決定をコンフィギュレーションするには、手動決定を右クリックし、**プロパティ**をクリックして、**プロパティ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2ac37-106">その後、手動決定のプロパティをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="2ac37-107">判断名の設定</span><span class="sxs-lookup"><span data-stu-id="2ac37-107">Name the decision</span></span>

<span data-ttu-id="2ac37-108">手動決定の名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="2ac37-109">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2ac37-110">**名前**フィールドに、手動決定の一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="2ac37-111">件名行と指示を入力する</span><span class="sxs-lookup"><span data-stu-id="2ac37-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="2ac37-112">この手動決定に割り当てられるユーザーに対して件名行と指示を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ac37-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="2ac37-113">たとえば、購買要求の決定をコンフィギュレーションする場合には、その決定に割り当てられるユーザーに対して、**購買要求**ページの件名行と指示が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2ac37-114">件名行はページのメッセージ バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="2ac37-115">ユーザーは、その後、メッセージ バーのアイコンをクリックして、指示を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="2ac37-116">次に手順に従って、件名行と指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="2ac37-117">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2ac37-118">**作業項目の件名**フィールドの**指示**タブで、件名行を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="2ac37-119">件名行をカスタマイズするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="2ac37-120">プレースホルダーは、件名行がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="2ac37-121">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2ac37-122">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2ac37-123">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2ac37-124">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2ac37-125">**挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-125">Click **Insert**.</span></span>

4. <span data-ttu-id="2ac37-126">件名行の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="2ac37-127">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="2ac37-128">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2ac37-129">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2ac37-130">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2ac37-131">テキストをカスタマイズする場合は、ステップ 3 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="2ac37-132">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-132">Click **Close**.</span></span>

5. <span data-ttu-id="2ac37-133">**作業項目の指示**フィールドで、指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="2ac37-134">指示を個人向けのものにするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2ac37-135">プレースホルダーは、指示行がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2ac37-136">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2ac37-137">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2ac37-138">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2ac37-139">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2ac37-140">**挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-140">Click **Insert**.</span></span>

7. <span data-ttu-id="2ac37-141">指示行の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="2ac37-142">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="2ac37-143">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2ac37-144">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2ac37-145">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2ac37-146">テキストをカスタマイズする場合は、ステップ 6 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="2ac37-147">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="2ac37-148">決定の可能な結果を指定する</span><span class="sxs-lookup"><span data-stu-id="2ac37-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="2ac37-149">通常、ドキュメントが意思決定者に割り当てられると、その意志決定者に質問が行われます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="2ac37-150">この質問に対する回答は、通常**はい**または**いいえ**または **True** または **False** です。</span><span class="sxs-lookup"><span data-stu-id="2ac37-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="2ac37-151">手動決定の結果の候補を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="2ac37-152">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2ac37-153">**結果 1** フィールドの**結果**タブに、結果の名前またはオプションを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="2ac37-154">結果の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="2ac37-155">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="2ac37-156">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2ac37-157">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2ac37-158">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2ac37-159">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-159">Click **Close**.</span></span>

4. <span data-ttu-id="2ac37-160">**結果 2** フィールドに、結果の名前またはオプションを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="2ac37-161">結果の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="2ac37-162">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="2ac37-163">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2ac37-164">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2ac37-165">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2ac37-166">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="2ac37-167">いつ通知を送信するかを指定する</span><span class="sxs-lookup"><span data-stu-id="2ac37-167">Specify when notifications are sent</span></span>

<span data-ttu-id="2ac37-168">決定の実行、委任、またはエスカレーションが行われたときに、ユーザーに通知を送信できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="2ac37-169">通知の送信条件と、通知の送信先のユーザーを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="2ac37-170">左ウィンドウで、**通知**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="2ac37-171">通知を送信するイベントの横にあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="2ac37-172">**\[選択 1\]** – 割り当てられたユーザーは **\[選択 1\]** を選択しました。</span><span class="sxs-lookup"><span data-stu-id="2ac37-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="2ac37-173">**\[選択 2\]** – 割り当てられたユーザーは **\[選択 2\]** を選択しました。</span><span class="sxs-lookup"><span data-stu-id="2ac37-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="2ac37-174">**委任** – 割り当てられたユーザーは別のユーザーに決定を割り当てました。</span><span class="sxs-lookup"><span data-stu-id="2ac37-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="2ac37-175">**エスカレート** – 割り当てられたユーザーは割り当てられた時間内に決定を行いませんでした。</span><span class="sxs-lookup"><span data-stu-id="2ac37-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="2ac37-176">ステップ 2 で選択したイベントの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="2ac37-177">**通知テキスト**タブのテキスト ボックス内で、通知のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="2ac37-178">通知を個人向けのものにするには、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="2ac37-179">プレースホルダーは、通知がユーザーに表示されるときに、適切なデータに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="2ac37-180">次の手順に従って、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2ac37-181">テキスト ボックス内で、プレースホルダを表示する場所をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2ac37-182">**プレースホルダーの挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2ac37-183">表示されるリストで、挿入するプレースホルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2ac37-184">**挿入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-184">Click **Insert**.</span></span>

6. <span data-ttu-id="2ac37-185">通知の翻訳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="2ac37-186">**翻訳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="2ac37-187">表示されるページで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2ac37-188">表示される一覧で、テキストを入力する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2ac37-189">**翻訳テキスト**フィールドで、テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2ac37-190">テキストをカスタマイズする場合は、ステップ 5 の説明に従い、プレースホルダーを挿入します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="2ac37-191">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-191">Click **Close**.</span></span>

7. <span data-ttu-id="2ac37-192">**受信者**タブで、通知の送信先ユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="2ac37-193">次の表のいずれかのオプションを選択し、オプションの追加ステップを実行してから、ステップ 8 に進みます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2ac37-194">オプション</span><span class="sxs-lookup"><span data-stu-id="2ac37-194">Option</span></span></th>
    <th><span data-ttu-id="2ac37-195">通知の受信者</span><span class="sxs-lookup"><span data-stu-id="2ac37-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="2ac37-196">追加手順</span><span class="sxs-lookup"><span data-stu-id="2ac37-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2ac37-197">参加者</span><span class="sxs-lookup"><span data-stu-id="2ac37-197">Participant</span></span></td>
    <td><span data-ttu-id="2ac37-198">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2ac37-199"><strong>参加者のタイプ</strong> 一覧の <strong>ロール ベース</strong> タブの、<strong>参加者</strong> を選択したのち、通知の送信先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="2ac37-200"><strong>参加者</strong> の一覧で、通知の送信先のグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2ac37-201">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-201">Workflow user</span></span></td>
    <td><span data-ttu-id="2ac37-202">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2ac37-203"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2ac37-204">ユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-204">User</span></span></td>
    <td><span data-ttu-id="2ac37-205">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2ac37-206"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2ac37-207"><strong>利用可能なユーザー</strong>の一覧には、すべてのユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2ac37-208">通知の送信先のユーザーを選択して、それらのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="2ac37-209">ステップ 2 で選択したイベントごとに、ステップ 3～7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="2ac37-210">決定の割り当て</span><span class="sxs-lookup"><span data-stu-id="2ac37-210">Assign a decision</span></span>

<span data-ttu-id="2ac37-211">手動決定の割り当て先のユーザーを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="2ac37-212">左ウィンドウで、**割り当て**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="2ac37-213">**割り当てタイプ**タブで、次の表のいずれかのオプションを選択し、オプションの追加手順を実行してから、手順 3 に進みます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2ac37-214">オプション</span><span class="sxs-lookup"><span data-stu-id="2ac37-214">Option</span></span></th>
    <th><span data-ttu-id="2ac37-215">決定の割り当て先のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="2ac37-216">追加手順</span><span class="sxs-lookup"><span data-stu-id="2ac37-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2ac37-217">参加者</span><span class="sxs-lookup"><span data-stu-id="2ac37-217">Participant</span></span></td>
    <td><span data-ttu-id="2ac37-218">特定のグループまたはロールに割り当てられたユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2ac37-219"><strong>参加者のタイプ</strong> 一覧の <strong>ロール ベース</strong> タブの、<strong>参加者</strong> を選択した後、決定の割り当て先のグループまたはロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2ac37-220"><strong>参加者</strong> の一覧で、決定の割り当て先のグループまたはロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2ac37-221">階層</span><span class="sxs-lookup"><span data-stu-id="2ac37-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="2ac37-222">特定の組織階層内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2ac37-223"><strong>階層タイプ</strong> 一覧の <strong>階層選択</strong> タブの、<strong>階層</strong> を選択したのち、決定の割り当て先の階層タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2ac37-224">システムは、一定範囲のユーザー名を階層から取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ac37-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2ac37-225">これらの名前は、決定を割り当てることができるユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="2ac37-226">システムで取得するユーザー名の範囲について、その開始点と終了点を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2ac37-227">開始点を指定するには、<strong>開始</strong> 一覧から人物を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2ac37-228">終了点を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2ac37-229">次に、階層のどこで名前の取得を止めるかを示す条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2ac37-230"><strong>階層オプション</strong> で、決定を割り当てる範囲内のユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="2ac37-231"><strong>取得したすべてのユーザーに割り当てる</strong> – 決定は範囲内のすべてのユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="2ac37-232"><strong>取得した最後のユーザーのみに割り当てる</strong> – 決定は、範囲内の最後のユーザーのみに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2ac37-233"><strong>次の条件のユーザーを除外します</strong> – 決定は、特定の条件に該当する範囲内のどのユーザーにも割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="2ac37-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2ac37-234">条件を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2ac37-235">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-235">Workflow user</span></span></td>
    <td><span data-ttu-id="2ac37-236">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2ac37-237"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2ac37-238">ユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-238">User</span></span></td>
    <td><span data-ttu-id="2ac37-239">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2ac37-240"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2ac37-241"><strong>利用可能なユーザー</strong>の一覧には、すべてのユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2ac37-242">決定を割り当てるユーザーを選択し、そのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="2ac37-243">**期限**タブの、**期間**フィールドで、ユーザーが決定をしなければならない期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2ac37-244">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-244">Select one of the following options:</span></span>

    - <span data-ttu-id="2ac37-245">**時間数** – ユーザーが決定を行わなければならない期限を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2ac37-246">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2ac37-247">**日数** – ユーザーが決定を行わなければならない期限を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2ac37-248">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2ac37-249">**週数** – ユーザーが決定を行わなければならない期限を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="2ac37-250">**月** – ユーザーが決定を行わなければならない期限を曜日および週で選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2ac37-251">たとえば、当月の第 3 週の金曜日までに決定を行うよう設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2ac37-252">**月** – ユーザーが決定を行わなければならない期限を曜日、週、および月で選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2ac37-253">たとえば、12 月の第 3 週の金曜日までに決定を行うよう設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="2ac37-254">割り当てられている時間内にユーザーが決定を行わなかった場合、その決定は期限超過になります。</span><span class="sxs-lookup"><span data-stu-id="2ac37-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2ac37-255">期限超過の決定は、このページの**エスカレーション**領域で選択したオプションに基づいて、エスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="2ac37-256">決定が期限超過の場合の処置を指定する</span><span class="sxs-lookup"><span data-stu-id="2ac37-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="2ac37-257">割り当てられている時間内にユーザーが決定を行わなかった場合、その決定は期限超過になります。</span><span class="sxs-lookup"><span data-stu-id="2ac37-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2ac37-258">期限超過した決定は、別のユーザーにエスカレートする (自動的に割り当てる) ことができます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="2ac37-259">期限超過した決定をエスカレートするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="2ac37-260">左ウィンドウで、**エスカレーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="2ac37-261">**エスカレーション パスを使用**チェック ボックスをオンにし、エスカレーション パスを作成します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="2ac37-262">決定は、エスカレーション パスにリストされるユーザーに自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="2ac37-263">たとえば、次の表に、エスカレーション パスを示します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="2ac37-264">順番</span><span class="sxs-lookup"><span data-stu-id="2ac37-264">Sequence</span></span> | <span data-ttu-id="2ac37-265">エスカレーション パス</span><span class="sxs-lookup"><span data-stu-id="2ac37-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="2ac37-266">1</span><span class="sxs-lookup"><span data-stu-id="2ac37-266">1</span></span>        | <span data-ttu-id="2ac37-267">割り当て先: 奈緒美</span><span class="sxs-lookup"><span data-stu-id="2ac37-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="2ac37-268">2</span><span class="sxs-lookup"><span data-stu-id="2ac37-268">2</span></span>        | <span data-ttu-id="2ac37-269">割り当て先: 悦子</span><span class="sxs-lookup"><span data-stu-id="2ac37-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="2ac37-270">3</span><span class="sxs-lookup"><span data-stu-id="2ac37-270">3</span></span>        | <span data-ttu-id="2ac37-271">最終アクション: \[選択 1\]</span><span class="sxs-lookup"><span data-stu-id="2ac37-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="2ac37-272">この例では、奈緒美に、期限超過の決定が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="2ac37-273">割り当てられた時間内に奈緒美が決定を行わない場合は、悦子に決定が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="2ac37-274">割り当てられた時間内に悦子が決定を行わない場合は、**\[選択 1\]** が決定として選択されます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="2ac37-275">エスカレーション パスにユーザーを追加するには、**エスカレーションの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="2ac37-276">次の表のいずれかのオプションを選択し、そのオプションの追加ステップを実行してから、ステップ 4 に進みます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2ac37-277">オプション</span><span class="sxs-lookup"><span data-stu-id="2ac37-277">Option</span></span></th>
    <th><span data-ttu-id="2ac37-278">決定のエスカレート先のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="2ac37-279">追加手順</span><span class="sxs-lookup"><span data-stu-id="2ac37-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2ac37-280">階層</span><span class="sxs-lookup"><span data-stu-id="2ac37-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="2ac37-281">特定の組織階層内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2ac37-282"><strong>階層タイプ</strong> 一覧の <strong>階層選択</strong> タブの、<strong>階層</strong> を選択したのち、決定をエスカレートする先の階層グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="2ac37-283">システムは、一定範囲のユーザー名を階層から取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ac37-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2ac37-284">これらの名前は、決定のエスカレート先にすることできるユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="2ac37-285">システムで取得するユーザー名の範囲について、その開始点と終了点を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2ac37-286">開始点を指定するには、<strong>開始</strong> 一覧から人物を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2ac37-287">終了点を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2ac37-288">次に、階層のどこで名前の取得を止めるかを示す条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2ac37-289"><strong>階層オプション</strong> で、決定をエスカレートできる範囲内のユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="2ac37-290"><strong>取得したすべてのユーザーに割り当てる</strong> – 決定は範囲内のすべてのユーザーにエスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="2ac37-291"><strong>取得した最後のユーザーのみに割り当てる</strong> – 決定は、範囲内の最後のユーザーのみにエスカレートされます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2ac37-292"><strong>次の条件のユーザーを除外します</strong> – 決定は、特定の条件に該当する範囲内のどのユーザーにもエスカレートされません。</span><span class="sxs-lookup"><span data-stu-id="2ac37-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2ac37-293">条件を指定するには、<strong>条件の追加</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2ac37-294">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-294">Workflow user</span></span></td>
    <td><span data-ttu-id="2ac37-295">現在のワークフロー内のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2ac37-296"><strong>ワークフロー ユーザー</strong> 一覧の、<strong>ワークフロー ユーザー</strong> タブの、<strong>ワークフロー ユーザー</strong> を選択したのち、ワークフローに参加するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2ac37-297">ユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-297">User</span></span></td>
    <td><span data-ttu-id="2ac37-298">特定のユーザー</span><span class="sxs-lookup"><span data-stu-id="2ac37-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2ac37-299"><strong>ユーザー</strong> を選択したのち、<strong>ユーザー</strong> タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2ac37-300"><strong>利用可能なユーザー</strong>の一覧には、すべてのユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2ac37-301">決定をエスカレートするユーザーを選択し、そのユーザーを <strong>選択されたユーザー</strong> リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="2ac37-302">**期限**タブの、**期間**フィールドで、ユーザーが決定をしなければならない期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2ac37-303">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-303">Select one of the following options:</span></span>

    - <span data-ttu-id="2ac37-304">**時間数** – ユーザーが決定を行わなければならない期限を時間数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2ac37-305">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2ac37-306">**日数** – ユーザーが決定を行わなければならない期限を日数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2ac37-307">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2ac37-308">**週数** – ユーザーが決定を行わなければならない期限を週数で入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="2ac37-309">**月** – ユーザーが決定を行わなければならない期限を曜日および週で選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2ac37-310">たとえば、当月の第 3 週の金曜日までに決定を行うよう設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2ac37-311">**月** – ユーザーが決定を行わなければならない期限を曜日、週、および月で選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2ac37-312">たとえば、12 月の第 3 週の金曜日までに決定を行うよう設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="2ac37-313">エスカレーション パスに追加するユーザーごとに、ステップ 3～4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="2ac37-314">ユーザーの順序は、変更できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="2ac37-315">エスカレーション パスに含まれるユーザーが、割り当てられた時間内に決定を行わない場合、システムによって決定が行われます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="2ac37-316">システムによるオプションを指定するには、**アクション**行を選択し、**アクションの終了**タブでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="2ac37-317">期限の設定</span><span class="sxs-lookup"><span data-stu-id="2ac37-317">Set a time limit</span></span>

<span data-ttu-id="2ac37-318">特定の時間内に決定を行わなければならないようにするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ac37-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="2ac37-319">この手順で選択するオプションは、このページの**割り当て**、および**エスカレーション**領域で選択されたオプションよりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="2ac37-320">左ウィンドウで**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="2ac37-321">**ワークフロー要素の期限の設定**を選択し、チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2ac37-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="2ac37-322">**期間**フィールドで、決定を行う必要がある期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="2ac37-323">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-323">Select one of the following options:</span></span>

    - <span data-ttu-id="2ac37-324">**時間数** – 時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="2ac37-325">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2ac37-326">**日数** – 日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="2ac37-327">続いて、組織で使用しているカレンダーを選択し、組織の週間労働時間に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2ac37-328">**週数** – 週数を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="2ac37-329">**月** – 決定の実行期限を曜日、週で選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="2ac37-330">たとえば、当月の第 3 週の金曜日までに決定を実行する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2ac37-331">**年** – 決定の実行期限を曜日、週、月で選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="2ac37-332">たとえば、12 月の第 3 週の金曜日までに決定を実行する必要があるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="2ac37-333">時間制限を超過した場合は、システムによって決定が行われます。</span><span class="sxs-lookup"><span data-stu-id="2ac37-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="2ac37-334">**アクション**の一覧から、システムで選択するオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ac37-334">In the **Action** list, select the option that the system should select.</span></span>
