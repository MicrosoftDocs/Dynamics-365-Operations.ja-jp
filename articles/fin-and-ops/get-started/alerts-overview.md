---
title: "警告の概要"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の警告に関する一般情報を提供します。 警告を使用することで、作業日に追跡したいイベントに関する情報を常に受け取ることができます。"
author: tjvass
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: ec005285eb561f77c005f8d84eeff69c37ce6833
ms.openlocfilehash: a3145cad682177ae3be2450889f788d695b25df4
ms.contentlocale: ja-jp
ms.lasthandoff: 07/16/2018

---

# <a name="alerts-overview"></a><span data-ttu-id="c5983-104">警告の概要</span><span class="sxs-lookup"><span data-stu-id="c5983-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="c5983-105">警告について</span><span class="sxs-lookup"><span data-stu-id="c5983-105">About alerts</span></span>
<span data-ttu-id="c5983-106">警告は、Microsoft Dynamics 365 for Finance and Operations の重大なイベントの通知システムを形成します。</span><span class="sxs-lookup"><span data-stu-id="c5983-106">Alerts form a notification system for critical events in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c5983-107">警告を使用することで、作業日に追跡したいイベントに関する情報を常に受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="c5983-108">延滞した出荷、削除された注文、変更された価格、またはその他対応が必要なイベントに関する警告を受け取る独自の警告ルール セットを、簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="c5983-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="c5983-109">エンタープライズ リソース プランニング (ERP) では、Finance and Operations での警告機能を使用できる、いくつかの一般的なシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="c5983-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature in Finance and Operations can be used.</span></span> <span data-ttu-id="c5983-110">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="c5983-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="c5983-111">シナリオ 1: 新しい販売注文に対する警告ルールの作成</span><span class="sxs-lookup"><span data-stu-id="c5983-111">Scenario 1: Create an alert rule for new sales orders</span></span>
1. <span data-ttu-id="c5983-112">[すべての販売注文] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c5983-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="c5983-113">[オプション] タブのアクション ウィンドウの、[共有] グループで、[カスタム警告の作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5983-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="c5983-114">[警告ルールの作成] ダイアログ ボックスの [警告する時期] クイック タブの [イベント] フィールドで、[レコードが作成されました] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5983-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="c5983-115">シナリオ 2: 出荷日の延期に対する警告ルールの作成</span><span class="sxs-lookup"><span data-stu-id="c5983-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>
1. <span data-ttu-id="c5983-116">[すべての発注書] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c5983-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="c5983-117">発注書の詳細にアクセスするには、購買注文の ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5983-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="c5983-118">[発注書ヘッダー] クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="c5983-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="c5983-119">[オプション] タブのアクション ウィンドウの、[共有] グループで、[カスタム警告の作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5983-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="c5983-120">[警告ルールの作成] ダイアログ ボックスの [警告する時期] クイック タブの [フィールド] フィールドで、[出荷日] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5983-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="c5983-121">[イベント] フィールドで、[は延期されました] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5983-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="c5983-122">[警告ルールの作成] ダイアログ ボックスを閉じた後、[警告ルールの管理] ページにルールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5983-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="c5983-123">[警告ルールの管理] ページを使用して、既存の警告ルールを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="c5983-124">たとえば、イベント トリガーを変更し、イベント通知を更新し、有効期限を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="c5983-125">[警告ルールの管理] ページを開くために、アクション ペインの [オプション] タブにある [警告] ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="c5983-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="c5983-126">警告ルール作成時の処理</span><span class="sxs-lookup"><span data-stu-id="c5983-126">What occurs when an alert rule is created?</span></span>
<span data-ttu-id="c5983-127">警告ルールを作成すると、事前に定義したイベントを特定のフィールドに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="c5983-128">たとえば、フィールドに指定された日付が来るか、またはフィールドの内容が変更されます。</span><span class="sxs-lookup"><span data-stu-id="c5983-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="c5983-129">また、イベントを特定のページのレコードに関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="c5983-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="c5983-130">たとえば、レコードが作成されるか、レコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c5983-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="c5983-131">選択したイベントがフィールドまたはページ上のレコードに対して発生すると、警告が自分自身に送信されます。</span><span class="sxs-lookup"><span data-stu-id="c5983-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="c5983-132">たとえば、特定の発注書明細行の [配送日] フィールドを、[この合計時間数より前が期限でした] イベントに関連付けるルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="c5983-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="c5983-133">期間は 5 日に設定します。</span><span class="sxs-lookup"><span data-stu-id="c5983-133">You set the time frame to five days.</span></span> <span data-ttu-id="c5983-134">この場合は、発注書明細行の配送日の 5 日後に警告が送信されます。</span><span class="sxs-lookup"><span data-stu-id="c5983-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="c5983-135">また、条件を設定して警告ルールを調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="c5983-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="c5983-136">たとえば、特定の仕入先勘定に対して作成された新しい発注書に関する警告を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="c5983-137">警告を準備する</span><span class="sxs-lookup"><span data-stu-id="c5983-137">Preparing for an alert</span></span>
<span data-ttu-id="c5983-138">警告ルールを設定するには、その前に、いつどのような状況の場合に警告を受信するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c5983-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="c5983-139">通知が必要なイベントがわかっているときは、Finance and Operations で、そのイベントを表示するデータのページを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c5983-139">When you know which event you want to be notified about, in Finance and Operations, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="c5983-140">イベントは、到来した日付か、または発生した特定の変更のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="c5983-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="c5983-141">したがって、日付が指定されたページ、あるいは、変更されるフィールドまたは新しく作成されたレコードを表示するページを見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5983-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="c5983-142">この情報が用意されたら、警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c5983-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="c5983-143">警告ルールのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="c5983-143">Components of an alert rule</span></span>
<span data-ttu-id="c5983-144">警告ルールには、5 つのコンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="c5983-144">An alert rule has five components:</span></span>

- <span data-ttu-id="c5983-145">**イベント** – 警告ルールを発生するイベントは、到来した日付かまたは発生した特定の変更のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="c5983-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="c5983-146">[警告ルールの作成] ダイアログ ボックスの [ジョブ状態変更の電子メール警告の送信] クイック タブでイベントを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="c5983-147">**条件** – [警告ルールの作成] ダイアログ ボックスの [表示する警告] クイック タブで、イベントについての警告をいつ受けるかを制御する条件の範囲を選択できます。</span><span class="sxs-lookup"><span data-stu-id="c5983-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="c5983-148">このルールは、現在のレコードのみに適用することも、ページ上に表示されるすべてのレコードに適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="c5983-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="c5983-149">法人間でルールが適用される場合は、[組織全体] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="c5983-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="c5983-150">**ルールの有効期限** – [警告ルールの作成] ダイアログ ボックスの [表示する警告] クイック タブで、警告ルールを有効にする期間を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="c5983-151">**コンテンツ** – [警告ルールの作成] ダイアログ ボックスの [表示する警告] クイック タブで、警告メッセージで使用する件名テキストとメッセージ テキストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c5983-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="c5983-152">**ユーザー** – [警告ルールの作成] ダイアログ ボックスの [警告先] クイック タブで、ユーザーが警告メッセージを受け取る必要があるかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="c5983-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="c5983-153">既定では、自身のユーザー ID が選択されます。</span><span class="sxs-lookup"><span data-stu-id="c5983-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c5983-154">このオプションは、組織の管理者に制限されています。</span><span class="sxs-lookup"><span data-stu-id="c5983-154">This option is restricted to organization administrators.</span></span>

## <a name="email-notifications-from-alerts"></a><span data-ttu-id="c5983-155">警告からの電子メール通知</span><span class="sxs-lookup"><span data-stu-id="c5983-155">Email notifications from alerts</span></span>
<span data-ttu-id="c5983-156">警告からの電子メール通知はまだ有効なっていません。</span><span class="sxs-lookup"><span data-stu-id="c5983-156">Email notifications from alerts are not yet enabled.</span></span> <span data-ttu-id="c5983-157">これは今後の更新で有効になります。</span><span class="sxs-lookup"><span data-stu-id="c5983-157">This will be enabled in a future update.</span></span>

