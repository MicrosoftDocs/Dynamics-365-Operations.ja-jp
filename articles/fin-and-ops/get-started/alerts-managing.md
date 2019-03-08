---
title: 警告のバッチ処理
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の警告のバッチ処理に関する情報を提供します。
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 482cf30b4f82e8801ebc12e3925c1efb09f7eb1e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "341928"
---
# <a name="batch-processing-of-alerts"></a><span data-ttu-id="ee99e-103">警告のバッチ処理</span><span class="sxs-lookup"><span data-stu-id="ee99e-103">Batch processing of alerts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee99e-104">警告は Microsoft Dynamics 365 for Finance and Operations のバッチ処理機能により処理されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-104">Alerts are processed by the batch processing functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ee99e-105">警告を通知するには、事前にバッチ処理を設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-105">You must set up batch processing before alerts can be delivered.</span></span>

<span data-ttu-id="ee99e-106">Finance and Operations は、2 種類のイベントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ee99e-106">Finance and Operations supports two types of events:</span></span>

- <span data-ttu-id="ee99e-107">変更ベースのイベントによってトリガーされたイベント。</span><span class="sxs-lookup"><span data-stu-id="ee99e-107">Events that are triggered by change-based events.</span></span> <span data-ttu-id="ee99e-108">これらのイベントは、作成/削除および更新イベントと呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-108">These events are also referred to as create/delete and update events.</span></span>
- <span data-ttu-id="ee99e-109">期日に発生するイベント。</span><span class="sxs-lookup"><span data-stu-id="ee99e-109">Events that are triggered by due dates.</span></span>

<span data-ttu-id="ee99e-110">各イベント タイプごとにバッチ処理を設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-110">You can set up batch processes for each type of event.</span></span>
        
## <a name="batch-processing-for-change-based-events"></a><span data-ttu-id="ee99e-111">変更ベースのイベントのバッチ処理</span><span class="sxs-lookup"><span data-stu-id="ee99e-111">Batch processing for change-based events</span></span>

<span data-ttu-id="ee99e-112">Finance and Operations は、バッチ処理が最後に実行されてから発生したすべての変更ベースのイベントを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-112">Finance and Operations reads all change-based events that have occurred since batch processing was last run.</span></span> <span data-ttu-id="ee99e-113">変更ベースのイベントには、フィールドの更新、レコードの削除、およびレコードの作成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-113">Change-based events include updates to fields, the deletion of records, and the creation of records.</span></span> <span data-ttu-id="ee99e-114">これらのイベントは、警告ルールに設定された条件と比較されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-114">These events are compared with the conditions that are set up in alert rules.</span></span> <span data-ttu-id="ee99e-115">イベントがルールの条件と一致すると、バッチ処理により警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-115">When an event matches the conditions in a rule, the batch process generates an alert.</span></span>

### <a name="frequency-for-change-based-events"></a><span data-ttu-id="ee99e-116">変更ベースのイベントの頻度</span><span class="sxs-lookup"><span data-stu-id="ee99e-116">Frequency for change-based events</span></span>

<span data-ttu-id="ee99e-117">変更ベースのイベントについては、システムによってイベントが記録された直後にそのイベントの処理をトリガするバッチ ジョブを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-117">For change-based events, you can set up a batch job that triggers the processing of an event soon after the event is logged by the system.</span></span> <span data-ttu-id="ee99e-118">より頻繁に繰り返すバッチ ジョブを設定する場合、変更が行われると直ちにユーザーは警告を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-118">If you set up the batch job to recur more often, users receive their alerts sooner after changes occur.</span></span> <span data-ttu-id="ee99e-119">ただし、バッチ処理の頻度の高さは、システム パフォーマンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-119">However, a high frequency for batch processing might adversely affect system performance.</span></span>

<span data-ttu-id="ee99e-120">一方で、繰り返し頻度が低く、システム負荷が低いときにスケジュールされるバッチ ジョブは、システム パフォーマンスを向上させることがあります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-120">On the other hand, a batch job that recurs less often, and that is scheduled for times when the system load is low, might help improve system performance.</span></span> <span data-ttu-id="ee99e-121">ただし、バッチ処理の頻度が低いと、時間どおりの警告についてのユーザーの要求を満たさない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-121">However, a low frequency for batch processing might not meet the users' demands for timely alerts.</span></span>

<span data-ttu-id="ee99e-122">したがって、変更ベースのイベントのバッチ処理の頻度を設定する際は、警告の適時性とシステム全体のパフォーマンス間のバランスを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-122">Therefore, when you set up the frequency of batch processing for change-based events, consider the balance between the timeliness of alerts and the performance of the whole system.</span></span> <span data-ttu-id="ee99e-123">警告ルールを作成するユーザーの数が増えるほど、この点を考慮する必要性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-123">These considerations become more relevant as the number of users who create alert rules increases.</span></span> <span data-ttu-id="ee99e-124">頻度は、処理する必要があるイベント数に影響しません。</span><span class="sxs-lookup"><span data-stu-id="ee99e-124">The frequency doesn't affect the number of events that must be processed.</span></span> <span data-ttu-id="ee99e-125">ただし、ルールを作成するユーザーが増えると、処理が必要なチェックも増加します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-125">However, if more users create rules, more checks must be done.</span></span> <span data-ttu-id="ee99e-126">このようなタイプのデータ交換はシステムのパフォーマンスに影響を与えることがあります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-126">This type of data exchange might affect system performance.</span></span>

#### <a name="the-risks-of-low-batch-frequency"></a><span data-ttu-id="ee99e-127">バッチ処理の処理頻度が低いことのリスク</span><span class="sxs-lookup"><span data-stu-id="ee99e-127">The risks of low batch frequency</span></span>

<span data-ttu-id="ee99e-128">変更ベース イベントのバッチ処理の頻度を低く設定すると、バッチが処理される前に警告ルールの条件に該当するデータが変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-128">If you set up a low frequency for batch processing for change-based events, data that is relevant to the conditions in alert rules might be changed before the batch is processed.</span></span> <span data-ttu-id="ee99e-129">したがって、警告を受信できなくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-129">Therefore, you might lose alerts.</span></span>

<span data-ttu-id="ee99e-130">たとえば、イベントが**顧客連絡先の変更**で条件が**顧客 = BB** を満たす場合に、警告をトリガーするように警告ルールを設定したとします。</span><span class="sxs-lookup"><span data-stu-id="ee99e-130">For example, an alert rule is set up to trigger an alert when the event is **customer contact changes** and the condition is **customer = BB**.</span></span> <span data-ttu-id="ee99e-131">つまり、顧客の連絡先が顧客 BB のために変更されると、イベントが記録されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-131">In other words, when the customer contact for customer BB is changed, the event is logged.</span></span> <span data-ttu-id="ee99e-132">ただし、バッチ処理システムは、バッチ処理の頻度がデータ入力より低くなるように設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-132">However, the batch processing system is set up so that batch processing occurs less often than data entry.</span></span> <span data-ttu-id="ee99e-133">イベント処理前に顧客名が **BB** から **AA** に変更される場合、データベース内のデータはルール **顧客 = BB** の条件に一致しなくなります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-133">If the customer name is changed from **BB** to **AA** before the event is processed, the data in the database no longer matches the condition in the rule, **customer = BB**.</span></span> <span data-ttu-id="ee99e-134">したがって、イベントが最終的に処理されても、警告が生成されません。</span><span class="sxs-lookup"><span data-stu-id="ee99e-134">Therefore, when the event is finally processed, no alert is generated.</span></span>

### <a name="set-up-processing-for-change-based-alerts"></a><span data-ttu-id="ee99e-135">変更ベースの警告処理を設定する</span><span class="sxs-lookup"><span data-stu-id="ee99e-135">Set up processing for change-based alerts</span></span>

1. <span data-ttu-id="ee99e-136">**システム管理** &gt; **定期処理タスク** &gt; **警告** &gt; **変更に基づく警告**に移動します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-136">Go to **System administration** &gt; **Periodic tasks** &gt; **Alerts** &gt; **Change based alerts**.</span></span>
2. <span data-ttu-id="ee99e-137">**変更に基づく警告**ダイアログ ボックスで、適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-137">In the **Change based alerts** dialog box, enter the appropriate information.</span></span>

## <a name="batch-processing-for-due-date-events"></a><span data-ttu-id="ee99e-138">期日イベントに関するバッチ処理</span><span class="sxs-lookup"><span data-stu-id="ee99e-138">Batch processing for due-date events</span></span>

<span data-ttu-id="ee99e-139">Finance and Operations のデータは、期日によって発生したすべてのイベントを検出し、これらのイベントは警告ルールに設定された条件と比較されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-139">Finance and Operations detects all events that are caused by due dates, and these events are compared with the conditions that are set up in alert rules.</span></span> <span data-ttu-id="ee99e-140">イベントがルールの条件と一致するとき、バッチ処理により警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-140">The batch process generates an alert when an event matches the conditions in a rule.</span></span>

### <a name="frequency-for-due-date-events"></a><span data-ttu-id="ee99e-141">期日イベントの頻度</span><span class="sxs-lookup"><span data-stu-id="ee99e-141">Frequency for due-date events</span></span>

<span data-ttu-id="ee99e-142">期日イベントの場合は、夜間または特定の時間帯に実行されるバッチ ジョブを設定して、システム負荷を分散できます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-142">For due-date events, you might want to set up batch jobs that are run during the night or at specific times of the day, to balance the system load.</span></span> <span data-ttu-id="ee99e-143">毎日少なくとも 1 回実行するバッチ ジョブを設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ee99e-143">We recommend that you set up the batch job so that it's run at least one time per day.</span></span> <span data-ttu-id="ee99e-144">できるだけ早く警告が送信される必要がある場合、システム日付が変わった直後にバッチ処理を実行するよう設定します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-144">If alerts should be sent as early as possible, set up the batch processing to occur immediately after the system date is changed.</span></span> <span data-ttu-id="ee99e-145">バッチ ジョブによって警告がすでに処理された後に発生する期日イベントのために警告を生成する必要がある場合は、同じ日に再度バッチ ジョブを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-145">If you want to generate alerts for due-date events that occur after a batch job has already processed alerts, you can run the batch job again on the same day.</span></span>

<span data-ttu-id="ee99e-146">たとえば、バッチ ジョブは特定の日付に実行されています。</span><span class="sxs-lookup"><span data-stu-id="ee99e-146">For example, a batch job has been run on a particular day.</span></span> <span data-ttu-id="ee99e-147">次に、その日に警告を発生させる必要がある期日がある発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-147">You then create a purchase order that has a due date that should trigger an alert on that same day.</span></span> <span data-ttu-id="ee99e-148">その日に警告を受信するには、発注書の作成後にバッチ ジョブを再度実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-148">To receive the alert on that day, you must run the batch job again after the purchase order is created.</span></span> <span data-ttu-id="ee99e-149">ただし、その日に再度バッチ ジョブを実行しない場合、翌日のバッチ ジョブは、前日までに処理されなかった期日イベントを検出します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-149">However, if you don't run the batch job again on that day, the next day's batch job detects any due-date events that weren't processed on previous days.</span></span>

> [!NOTE]
> <span data-ttu-id="ee99e-150">バッチ処理を 1 日に複数回実行しても、同じ期日イベントおよび条件によって警告が繰り返されることはありません。</span><span class="sxs-lookup"><span data-stu-id="ee99e-150">Even when the batch process is run more than one time per day, alerts aren't duplicated for the same due-date event and conditions.</span></span> <span data-ttu-id="ee99e-151">前回のバッチの実行後にシステム内に発生した変更によって期日に達した日付に対してのみ警告が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-151">Alerts are generated only for dates that have become due because of changes that occurred in the system after the last batch job was run.</span></span>

### <a name="batch-processing-window"></a><span data-ttu-id="ee99e-152">バッチ処理ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="ee99e-152">Batch processing window</span></span>

<span data-ttu-id="ee99e-153">法人の警告ルールの処理は、さまざまな理由で停止できます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-153">The processing of alert rules in a company can be stopped for several reasons.</span></span> <span data-ttu-id="ee99e-154">これらの理由には、休暇、システム エラー、またはしばらくの間バッチ ジョブの実行を妨げる他の問題が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-154">These reasons include vacations, system errors, or other issues that prevent the batch jobs from being run for some time.</span></span>

<span data-ttu-id="ee99e-155">バッチ ジョブが数日間動いていないために、期日の警告が確実でなくなることを避けるため、バッチ処理ウィンドウを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-155">To prevent due-date alerts from becoming obsolete because the batch job hasn't been run for several days, you can set up a batch processing window.</span></span> <span data-ttu-id="ee99e-156">バッチ処理ウィンドウにより、指定した日数の間、バッチ ジョブが実行されないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-156">A batch processing window can be used to prevent a batch job from being run for a specified number of days.</span></span>

<span data-ttu-id="ee99e-157">バッチ処理ウィンドウを設定する場合、期日の基準で定義された時間制限を警告が超過しても、警告ルールが処理されるときに警告が送信されます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-157">If you set up a batch processing window, an alert is sent when the alert rule is processed, even if the alert exceeds the time limit that is defined in the due-date criteria.</span></span> <span data-ttu-id="ee99e-158">この時間制限およびバッチ処理ウィンドウで定義された期間を超えていなければ、警告が送信され続けます。</span><span class="sxs-lookup"><span data-stu-id="ee99e-158">An alert continues to be sent for as long as the period that is defined by this time limit plus the batch processing window isn't exceeded.</span></span> <span data-ttu-id="ee99e-159">ただし、時間制限およびバッチ処理ウィンドウで定義された期間を超える場合、警告は送信されなくなります。</span><span class="sxs-lookup"><span data-stu-id="ee99e-159">However, when the period that is defined by the time limit plus the batch processing window is exceeded, an alert is no longer sent.</span></span>

### <a name="set-up-processing-for-due-date-alerts"></a><span data-ttu-id="ee99e-160">期日の警告処理を設定する</span><span class="sxs-lookup"><span data-stu-id="ee99e-160">Set up processing for due-date alerts</span></span>

1. <span data-ttu-id="ee99e-161">**システム管理** &gt; **定期処理タスク** &gt; **警告** &gt; **期日の警告**に移動します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-161">Go to **System administration** &gt; **Periodic tasks** &gt; **Alerts** &gt; **Due date alerts**.</span></span>
2. <span data-ttu-id="ee99e-162">**期日の警告**ダイアログ ボックスで、適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ee99e-162">In the **Due date alerts** dialog box, enter the appropriate information.</span></span>
