---
title: 警告ルールの作成
description: このトピックでは、警告に関する情報を提供し、警告ルールの作成方法を説明します。
author: RichdiMSFT
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 869a2f83360c1d6515bbe2868f1450f76ff3a13f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909842"
---
# <a name="create-alert-rules"></a><span data-ttu-id="b31cd-103">警告ルールの作成</span><span class="sxs-lookup"><span data-stu-id="b31cd-103">Create alert rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a><span data-ttu-id="b31cd-104">はじめに</span><span class="sxs-lookup"><span data-stu-id="b31cd-104">Getting started</span></span>

<span data-ttu-id="b31cd-105">警告ルールを設定するには、その前に、いつどのような状況の場合に警告を受信するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="b31cd-106">通知が必要なイベントがわかっているときは、そのイベントを表示するデータのページを見つけます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-106">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="b31cd-107">イベントは、到来した日付か、または発生した特定の変更のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="b31cd-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="b31cd-108">したがって、日付が指定されたページ、あるいは、変更されるフィールドまたは新しく作成されたレコードを表示するページを見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="b31cd-109">この情報が用意されたら、警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="b31cd-110">警告ルールの作成時に、警告が発生する前に満たす必要のある基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="b31cd-111">この基準とは、基本的にイベントが発生した際に特定の条件に適合しているかどうかの照合です。</span><span class="sxs-lookup"><span data-stu-id="b31cd-111">Criteria is basically the match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="b31cd-112">イベントが発生すると、設定されている条件に従って確認が開始されます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-112">When an event occurs, the system starts to perform a check according to the conditions that are set up.</span></span>

## <a name="ensure-the-alert-batch-jobs-are-running"></a><span data-ttu-id="b31cd-113">警告のバッチジョブが実行されていることの確認</span><span class="sxs-lookup"><span data-stu-id="b31cd-113">Ensure the alert batch jobs are running</span></span>

<span data-ttu-id="b31cd-114">データ変更と期日の警告に対してバッチジョブを実行して、警告条件を処理し、通知を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-114">The batch jobs for data change and due date alerts need to be running for the alert conditions to be processed and the notifications to be sent.</span></span> <span data-ttu-id="b31cd-115">バッチジョブを実行するには、**システム管理** > **定期処理タスク** > **警告** に移動し、**変更に基づく警告** または **期日の警告** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-115">To run batch jobs, go to **System administration** > **Periodic tasks** > **Alerts** and add a new batch job for **Change based alerts** and/or **Due date alerts**.</span></span> <span data-ttu-id="b31cd-116">長時間バッチジョブを頻繁に実行する必要がある場合は、**定期処理** を選択し、**終了日なし** を **分** の **定期処理パターン** と **1** の **カウント** で設定します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-116">If a long and frequently running batch job is needed, select **Recurrence** and set **No end date** with a **Recurrence pattern** of **Minutes** and a **Count** of **1**.</span></span>

## <a name="events"></a><span data-ttu-id="b31cd-117">イベント</span><span class="sxs-lookup"><span data-stu-id="b31cd-117">Events</span></span>

<span data-ttu-id="b31cd-118">警告ルールを発生するイベントは、到来した日付かまたは発生した特定の変更のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="b31cd-118">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="b31cd-119">イベントのトリガーは **警告ルールの作成** ダイアログ ボックスの **警告する時期** クイック タブで定義されています。</span><span class="sxs-lookup"><span data-stu-id="b31cd-119">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="b31cd-120">特定のフィールドで使用できるイベントは選択したトリガーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-120">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="b31cd-121">たとえば **開始日** フィールドの警告ルールを設定する場合は、期日イベントが適切です。</span><span class="sxs-lookup"><span data-stu-id="b31cd-121">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="b31cd-122">したがって、`is due in` イベント タイプは、そのフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-122">Therefore, the `is due in` event type is available for that field.</span></span> <span data-ttu-id="b31cd-123">ただし、**原価部門** などのフィールドでは、期日イベントは適切ではありません。</span><span class="sxs-lookup"><span data-stu-id="b31cd-123">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="b31cd-124">したがって、`is due in` イベント タイプは使用できません。</span><span class="sxs-lookup"><span data-stu-id="b31cd-124">Therefore, the `is due in` event type isn't available.</span></span> <span data-ttu-id="b31cd-125">代わりに、`has changed` イベント タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-125">Instead, the `has changed` event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="b31cd-126">イベントのタイプ</span><span class="sxs-lookup"><span data-stu-id="b31cd-126">Event types</span></span>

<span data-ttu-id="b31cd-127">次の 3 つのイベント タイプが存在します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-127">Three types of events can occur:</span></span>

- <span data-ttu-id="b31cd-128">**作成タイプのイベントと削除タイプのイベント** – これらのイベントは、レコードが作成または削除されたときに警告を発生します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-128">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="b31cd-129">**更新タイプのイベント** – これらのイベントは、特定のフィールドのデータが変更されると警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-129">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="b31cd-130">**期日タイプのイベント** – これらのイベントは、日付が到来したときに警告を発生します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-130">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="b31cd-131">変更はユーザーによって引き起こされることがあります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-131">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="b31cd-132">たとえば、ユーザーは発注書の配送日を変更します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-132">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="b31cd-133">また、変更は、プロセスの一部として発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-133">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="b31cd-134">たとえば、システム内のさまざまなプロセスのライフ サイクルを反映するために、ページの **ステータス** フィールドが変更されます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-134">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="b31cd-135">条件</span><span class="sxs-lookup"><span data-stu-id="b31cd-135">Conditions</span></span>

<span data-ttu-id="b31cd-136">**警告ルールの作成** ダイアログ ボックスの **表示する警告** クイック タブで、イベントについての警告をいつ受けるかを制御する条件を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-136">On the **Alert me for** FastTab in the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="b31cd-137">たとえば、発注書のステータスが変更されたとき、そのステータスが特定の条件セットを満たす場合にのみ、システムが警告するように指定できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-137">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="b31cd-138">特に、発注書のステータスが **受入済** に設定されている場合に警告する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-138">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="b31cd-139">このステータスの変更が警告を発生するイベントとなります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-139">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="b31cd-140">次に、警告の対象となる発注書を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-140">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="b31cd-141">たとえば、次のいずれかのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-141">For example, you can select one of the following options.</span></span> <span data-ttu-id="b31cd-142">これらのオプションは、警告ルールの条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-142">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="b31cd-143">**現在の選択したレコード** – 特定の発注書のステータスが **Received** に変更すると警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-143">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="b31cd-144">**すべてのレコード** – 有効なページ ビューで品目の発注書のステータスが変更されたときに警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-144">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="b31cd-145">ページに表示される高度なフィルタ処理を使用し、特定のレコードのセットに対するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-145">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="b31cd-146">たとえば、特定の顧客グループ内の顧客のすべての発注書に対して発生した警告を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-146">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="b31cd-147">ルールの有効期限</span><span class="sxs-lookup"><span data-stu-id="b31cd-147">Expiry of rule</span></span>

<span data-ttu-id="b31cd-148">**警告ルールの作成** ダイアログ ボックスの **表示する警告** クイック タブで、警告ルールを有効にする期間を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-148">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="b31cd-149">警告の内容</span><span class="sxs-lookup"><span data-stu-id="b31cd-149">Alert contents</span></span>

<span data-ttu-id="b31cd-150">**警告ルールの作成** ダイアログ ボックスの **警告の対象** クイック タブで、警告メッセージで使用する件名テキストとメッセージ テキストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-150">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="b31cd-151">ユーザー ID</span><span class="sxs-lookup"><span data-stu-id="b31cd-151">User ID</span></span>

<span data-ttu-id="b31cd-152">**警告ルールの作成** ダイアログ ボックスの **警告の対象** クイック タブで、ユーザーが警告メッセージを受け取る必要があるかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-152">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="b31cd-153">既定では、自身のユーザー ID が選択されます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-153">By default, your user ID is selected.</span></span> <span data-ttu-id="b31cd-154">警告を受信するユーザーを変更する機能は、組織管理者に制限されます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-154">The ability to change the user receiving the alert is restricted to organization administrators.</span></span>

## <a name="alerts-as-business-events"></a><span data-ttu-id="b31cd-155">ビジネス イベントとしての警告</span><span class="sxs-lookup"><span data-stu-id="b31cd-155">Alerts as business events</span></span>

<span data-ttu-id="b31cd-156">ビジネス イベント フレームワークを使用して、警告を外部に送信できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-156">You can send alerts externally using the business events framework.</span></span> <span data-ttu-id="b31cd-157">警告を作成する場合は、**組織全体** を **いいえ** に設定し、**外部への送信** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-157">When creating an alert, set **Organization-wide** to **No** and set **Send externally** to **Yes**.</span></span> <span data-ttu-id="b31cd-158">ビジネス イベントをトリガーする警告が発生したら、Finance and Operations コネクターの **ビジネス イベントが発生した場合** のトリガーを使用して Power Automate に組み込まれたフローをトリガーするか、**ビジネス イベント カタログ** を介してイベントをビジネス イベント エンドポイントに明示的に送信できます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-158">After you have the alert triggering the business event, you can trigger a flow built in Power Automate using the **When a business event occurs** trigger on the Finance and Operations connector, or explicitly send the event to a business events endpoint via the **Business events catalog**.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="b31cd-159">警告ルールを作成</span><span class="sxs-lookup"><span data-stu-id="b31cd-159">Create an alert rule</span></span>

0. <span data-ttu-id="b31cd-160">警告のバッチ ジョブが実行されていることを確認してください (上記を参照)。</span><span class="sxs-lookup"><span data-stu-id="b31cd-160">Ensure the alert batch jobs are running (see above).</span></span>
1. <span data-ttu-id="b31cd-161">監視するデータが含まれているページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-161">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="b31cd-162">**オプション** タブのアクション ウィンドウの、**共有** グループで、**カスタムルールの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-162">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="b31cd-163">**警告ルールの作成** ダイアログ ボックスの **フィールド** フィールドで、監視するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-163">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="b31cd-164">**イベント** フィールドで、イベントのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-164">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="b31cd-165">**表示する警告** クイック タブで、希望のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-165">On the **Alert me for** FastTab, select the desired option.</span></span> <span data-ttu-id="b31cd-166">警告をビジネス イベントとして送信する場合は、**組織全体** 値を **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-166">If you want to send the alert as a business event, set the **Organization-wide** value to **No**.</span></span>
6. <span data-ttu-id="b31cd-167">特定の日付で警告ルールを無効にする必要がある場合、**警告の表示期限** クイック タブで終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-167">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="b31cd-168">**件名** フィールドの **警告の対象** クイック タブで、電子メール メッセージの既定の件名ヘッダー情報を受け入れるか、新しい件名を入力します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-168">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="b31cd-169">テキストは、警告が発生したときに受信する電子メール メッセージの件名のヘッダーになります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-169">The text becomes the subject heading for the email message that you receive when an alert is triggered.</span></span> <span data-ttu-id="b31cd-170">警告をビジネスイベントとして送信する場合は、**外部に送信** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-170">If you want to send the alert as a business event, set **Send externally** to **Yes**.</span></span>
8. <span data-ttu-id="b31cd-171">**メッセージ** フィールドにオプションのメッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-171">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="b31cd-172">テキストは、警告の発生時に受信するメッセージになります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-172">The text becomes the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="b31cd-173">**OK** を選択して、設定を保存し、警告ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-173">Select **OK** to save the settings and create the alert rule.</span></span>

## <a name="limitations-and-workarounds"></a><span data-ttu-id="b31cd-174">制限事項と回避策</span><span class="sxs-lookup"><span data-stu-id="b31cd-174">Limitations and workarounds</span></span>

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a><span data-ttu-id="b31cd-175">フォームのセカンダリ データ ソースに対して警告を作成するための回避策</span><span class="sxs-lookup"><span data-stu-id="b31cd-175">Workaround for creating alerts for the secondary data sources of a form</span></span>
<span data-ttu-id="b31cd-176">フォーム上の一部のセカンダリ データ ソースに対して警告を作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="b31cd-176">You can't create alerts for some secondary data sources on forms.</span></span> <span data-ttu-id="b31cd-177">たとえば、顧客または仕入先の転記プロファイル フォームで警告を作成するときは、ヘッダー (CustLedger または VendLedger) のフィールドのみが利用可能で、分析コード勘定は利用できません。</span><span class="sxs-lookup"><span data-stu-id="b31cd-177">For example, when creating alerts on the customer or vendor posting profiles form, only the fields on the header (CustLedger or VendLedger) are available and not the dimension accounts.</span></span> <span data-ttu-id="b31cd-178">この制限の回避策は、**SysTableBrowser** を使用してそのテーブルを基本データ ソースとして開きます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-178">The workaround for this limitation is to use **SysTableBrowser** to open that table as primary data source.</span></span> 
1. <span data-ttu-id="b31cd-179">**SysTableBrowser** フォームでテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="b31cd-179">Open the table in the **SysTableBrowser** form.</span></span>
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. <span data-ttu-id="b31cd-180">SysTableBrowser フォームから警告を作成します。</span><span class="sxs-lookup"><span data-stu-id="b31cd-180">Create an alert from the SysTableBrowser form.</span></span>

### <a name="change-based-alerts-do-not-work-for-batch-status-changes"></a><span data-ttu-id="b31cd-181">変更に基づく警告がバッチ ステータスの変更に対して機能しない</span><span class="sxs-lookup"><span data-stu-id="b31cd-181">Change based alerts do not work for batch status changes</span></span>
<span data-ttu-id="b31cd-182">変更に基づく警告は、パフォーマンス上の理由からオフになっているため、バッチ ステータスの変更に対して機能しません。</span><span class="sxs-lookup"><span data-stu-id="b31cd-182">Change based Alerts does not work with batch status changes because it is turned off for performance reasons.</span></span> <span data-ttu-id="b31cd-183">代わりに、**バッチ警告** を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b31cd-183">Instead, you should set up the **Batch alerts** capability.</span></span> <span data-ttu-id="b31cd-184">詳細については、[拡張バッチ フォームに対する警告を設定](../../dev-itpro/sysadmin/alerts.md#set-up-alerts-for-batch-enhanced-forms)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b31cd-184">For more information, see [Set up alerts for batch enhanced forms](../../dev-itpro/sysadmin/alerts.md#set-up-alerts-for-batch-enhanced-forms).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]