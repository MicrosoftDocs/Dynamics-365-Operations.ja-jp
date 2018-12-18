---
title: "警告ルールの作成"
description: "このトピックでは、警告に関する情報を提供し、警告ルールを作成して到着日や発生する特定の変更などのイベントについて通知する方法について説明します。"
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: cbf4917424e72a70a6d513b5daf45f6bf9cd57c7
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="create-alert-rules"></a><span data-ttu-id="21186-103">警告ルールの作成</span><span class="sxs-lookup"><span data-stu-id="21186-103">Create alert rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a><span data-ttu-id="21186-104">はじめに</span><span class="sxs-lookup"><span data-stu-id="21186-104">Getting started</span></span>

<span data-ttu-id="21186-105">警告ルールを設定するには、その前に、いつどのような状況の場合に警告を受信するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="21186-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="21186-106">通知が必要なイベントがわかっているときは、Microsoft Dynamics 365 for Finance and Operations で、そのイベントを表示するデータのページを見つけます。</span><span class="sxs-lookup"><span data-stu-id="21186-106">When you know which event you want to be notified about, in Microsoft Dynamics 365 for Finance and Operations find the page where the data that causes that event appears.</span></span> <span data-ttu-id="21186-107">イベントは、到来した日付か、または発生した特定の変更のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="21186-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="21186-108">したがって、日付が指定されたページ、あるいは、変更されるフィールドまたは新しく作成されたレコードを表示するページを見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="21186-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="21186-109">この情報が用意されたら、警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="21186-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="21186-110">警告ルールの作成時に、警告が発生する前に満たす必要のある基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="21186-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="21186-111">この基準とは、イベントが発生した際に特定の条件に適合しているかどうかの照合であると考えることができます。</span><span class="sxs-lookup"><span data-stu-id="21186-111">You can think of criteria as a match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="21186-112">イベントが発生すると、Finance and Operations で設定されている条件に従って確認が開始されます。</span><span class="sxs-lookup"><span data-stu-id="21186-112">When an event occurs, the system starts to perform a check according to the conditions that are set up in Finance and Operations.</span></span>

## <a name="events"></a><span data-ttu-id="21186-113">イベント</span><span class="sxs-lookup"><span data-stu-id="21186-113">Events</span></span>

<span data-ttu-id="21186-114">警告ルールを発生するイベントは、到来した日付かまたは発生した特定の変更のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="21186-114">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="21186-115">イベントのトリガーは**警告ルールの作成**ダイアログ ボックスの**警告する時期**クイック タブで定義されています。</span><span class="sxs-lookup"><span data-stu-id="21186-115">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="21186-116">特定のフィールドで使用できるイベントは選択したトリガーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="21186-116">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="21186-117">たとえば**開始日**フィールドの警告ルールを設定する場合は、期日イベントが適切です。</span><span class="sxs-lookup"><span data-stu-id="21186-117">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="21186-118">したがって、**の期限です**イベント タイプは、このフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="21186-118">Therefore, the **is due in** event type is available for that field.</span></span> <span data-ttu-id="21186-119">ただし、**原価部門**などのフィールドでは、期日イベントは適切ではありません。</span><span class="sxs-lookup"><span data-stu-id="21186-119">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="21186-120">したがって、**の期限です**イベント タイプは使用できません。</span><span class="sxs-lookup"><span data-stu-id="21186-120">Therefore, the **is due in** event type isn't available.</span></span> <span data-ttu-id="21186-121">代わりに、**変更済**イベント タイプが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="21186-121">Instead, the **has changed** event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="21186-122">イベントのタイプ</span><span class="sxs-lookup"><span data-stu-id="21186-122">Event types</span></span>

<span data-ttu-id="21186-123">次の 3 つのイベント タイプが存在します。</span><span class="sxs-lookup"><span data-stu-id="21186-123">Three types of events can occur:</span></span>

- <span data-ttu-id="21186-124">**作成タイプのイベントと削除タイプのイベント** – これらのイベントは、レコードが作成または削除されたときに警告を発生します。</span><span class="sxs-lookup"><span data-stu-id="21186-124">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="21186-125">**更新タイプのイベント** – これらのイベントは、特定のフィールドのデータが変更されると警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="21186-125">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="21186-126">**期日タイプのイベント** – これらのイベントは、日付が到来したときに警告を発生します。</span><span class="sxs-lookup"><span data-stu-id="21186-126">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="21186-127">変更はユーザーによって引き起こされることがあります。</span><span class="sxs-lookup"><span data-stu-id="21186-127">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="21186-128">たとえば、ユーザーは発注書の配送日を変更します。</span><span class="sxs-lookup"><span data-stu-id="21186-128">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="21186-129">また、変更は、プロセスの一部として発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="21186-129">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="21186-130">たとえば、システム内のさまざまなプロセスのライフ サイクルを反映するために、ページの**ステータス**フィールドが変更されます。</span><span class="sxs-lookup"><span data-stu-id="21186-130">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="21186-131">条件</span><span class="sxs-lookup"><span data-stu-id="21186-131">Conditions</span></span>

<span data-ttu-id="21186-132">**警告ルールの作成**ダイアログ ボックスの**表示する警告**クイック タブで、イベントについての警告をいつ受けるかを制御する条件を使用できます。</span><span class="sxs-lookup"><span data-stu-id="21186-132">On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="21186-133">たとえば、発注書のステータスが変更されたとき、そのステータスが特定の条件セットを満たす場合にのみ、システムが警告するように指定できます。</span><span class="sxs-lookup"><span data-stu-id="21186-133">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="21186-134">特に、発注書のステータスが **受入済** に設定されている場合に警告する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21186-134">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="21186-135">このステータスの変更が警告を発生するイベントとなります。</span><span class="sxs-lookup"><span data-stu-id="21186-135">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="21186-136">次に、警告の対象となる発注書を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21186-136">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="21186-137">たとえば、次のいずれかのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="21186-137">For example, you can select one of the following options.</span></span> <span data-ttu-id="21186-138">これらのオプションは、警告ルールの条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="21186-138">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="21186-139">**現在の選択したレコード** – 特定の発注書のステータスが **Received** に変更すると警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="21186-139">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="21186-140">**すべてのレコード** – 有効なページ ビューで品目の発注書のステータスが変更されたときに警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="21186-140">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="21186-141">ページに表示される高度なフィルタ処理を使用し、特定のレコードのセットに対するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="21186-141">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="21186-142">たとえば、特定の顧客グループ内の顧客のすべての発注書に対して発生した警告を作成できます。</span><span class="sxs-lookup"><span data-stu-id="21186-142">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="21186-143">ルールの有効期限</span><span class="sxs-lookup"><span data-stu-id="21186-143">Expiry of rule</span></span>

<span data-ttu-id="21186-144">**警告ルールの作成**ダイアログ ボックスの**表示する警告**クイック タブで、警告ルールを有効にする期間を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="21186-144">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="21186-145">警告の内容</span><span class="sxs-lookup"><span data-stu-id="21186-145">Alert contents</span></span>

<span data-ttu-id="21186-146">**警告ルールの作成**ダイアログ ボックスの**警告の対象**クイック タブで、警告メッセージで使用する件名テキストとメッセージ テキストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="21186-146">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="21186-147">ユーザー ID</span><span class="sxs-lookup"><span data-stu-id="21186-147">User ID</span></span>

<span data-ttu-id="21186-148">**警告ルールの作成**ダイアログ ボックスの**警告の対象**クイック タブで、ユーザーが警告メッセージを受け取る必要があるかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="21186-148">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="21186-149">既定では、自身のユーザー ID が選択されます。</span><span class="sxs-lookup"><span data-stu-id="21186-149">By default, your user ID is selected.</span></span> <span data-ttu-id="21186-150">このオプションは、組織の管理者に制限されています。</span><span class="sxs-lookup"><span data-stu-id="21186-150">This option is restricted to organization administrators.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="21186-151">警告ルールを作成</span><span class="sxs-lookup"><span data-stu-id="21186-151">Create an alert rule</span></span>

1. <span data-ttu-id="21186-152">監視するデータが含まれているページを開きます。</span><span class="sxs-lookup"><span data-stu-id="21186-152">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="21186-153">**オプション**タブのアクション ウィンドウの、**共有**グループで、**カスタムルールの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="21186-153">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="21186-154">**警告ルールの作成**ダイアログ ボックスの**フィールド**フィールドで、監視するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="21186-154">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="21186-155">**イベント**フィールドで、イベントのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="21186-155">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="21186-156">**表示する警告**クイック タブで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="21186-156">On the **Alert me for** FastTab, select an option.</span></span>
6. <span data-ttu-id="21186-157">特定の日付で警告ルールを無効にする必要がある場合、**警告の表示期限**クイック タブで終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="21186-157">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="21186-158">**件名**フィールドの**警告の対象**クイック タブで、電子メール メッセージの既定の件名ヘッダー情報を受け入れるか、新しい件名を入力します。</span><span class="sxs-lookup"><span data-stu-id="21186-158">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="21186-159">テキストは、警告が発生したときに受信する電子メール メッセージの件名のヘッダーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="21186-159">The text is used as the subject heading for the email message that you receive when an alert is triggered.</span></span>
8. <span data-ttu-id="21186-160">**メッセージ**フィールドにオプションのメッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="21186-160">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="21186-161">テキストは、警告の発生時に受信するメッセージとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="21186-161">The text is used as the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="21186-162">**OK** を選択して、設定を保存し、警告ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="21186-162">Select **OK** to save the settings and create the alert rule.</span></span>

