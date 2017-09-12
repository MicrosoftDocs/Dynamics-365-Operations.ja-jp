---
title: "小売タイムと出勤"
description: "このトピックでは、Microsoft Dynamics 365 for Retail の時間と出勤管理でサポートされているシナリオについて説明します。"
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ebbf3c72b4c34cba95ecd2fb3ce506af393acc34
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="retail-time-and-attendance"></a><span data-ttu-id="24cb6-103">小売タイムと出勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-103">Retail time and attendance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="24cb6-104">このトピックでは、Microsoft Dynamics 365 for Retail の時間と出勤管理でサポートされているシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="24cb6-105">作業者設定およびスケジュールの管理</span><span class="sxs-lookup"><span data-stu-id="24cb6-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="24cb6-106">初期コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="24cb6-106">Initial configuration</span></span>

-   <span data-ttu-id="24cb6-107">コンフィギュレーション ウィザードを実行します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="24cb6-108">時間登録作業者としての作業者を登録します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="24cb6-109">作業者のスケジュールを計画する</span><span class="sxs-lookup"><span data-stu-id="24cb6-109">Plan worker schedules</span></span>

-   <span data-ttu-id="24cb6-110">ワーク プランナーを使用したプロファイルを適用します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="24cb6-111">詳細については、<https://technet.microsoft.com/en-us/library/aa551234.aspx>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24cb6-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="24cb6-112">コンフィギュレーション手順については、<https://technet.microsoft.com/en-us/library/aa496971.aspx>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24cb6-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="24cb6-113">小売固有のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="24cb6-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="24cb6-114">時間登録を有効にする作業者のタイム レコーダーの機能プロファイルを有効にします。</span><span class="sxs-lookup"><span data-stu-id="24cb6-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="24cb6-115">[**POS機能プロファイル**] &gt; [**機能**] &gt; [**POS 時間登録**] &gt; [**時間登録の有効化**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="24cb6-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="24cb6-116">販売時点管理 (POS) のアクセス許可グループをコンフィギュレーションして、[タイム レコーダー エントリの表示] のアクセス許可を有効にします。</span><span class="sxs-lookup"><span data-stu-id="24cb6-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="24cb6-117">このアクセス許可により、ユーザーが、その店舗 (およびアドレス帳を介してユーザーが関連付けられている他のすべての店舗から) の他の作業者のタイム レコーダー登録を表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="24cb6-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="24cb6-118">レジ担当者ロールではなくマネージャー ロールに対してこのアクセス許可を有効にする場合があります。</span><span class="sxs-lookup"><span data-stu-id="24cb6-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="24cb6-119">[**POS アクセス許可グループ**] &gt; [**タイム レコーダー エントリの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="24cb6-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="24cb6-120">時刻の登録</span><span class="sxs-lookup"><span data-stu-id="24cb6-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="24cb6-121">レジ担当者と非レジ担当者の時間登録</span><span class="sxs-lookup"><span data-stu-id="24cb6-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="24cb6-122">POS で:</span><span class="sxs-lookup"><span data-stu-id="24cb6-122">On POS:</span></span>
    -   <span data-ttu-id="24cb6-123">出勤操作:</span><span class="sxs-lookup"><span data-stu-id="24cb6-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="24cb6-124">非ドロワー操作または新しいシフトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="24cb6-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="24cb6-125">タイム レコーダーの操作を選択します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="24cb6-126">必要な操作を選択します:</span><span class="sxs-lookup"><span data-stu-id="24cb6-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="24cb6-127">出勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-127">Clock-in</span></span>
            -   <span data-ttu-id="24cb6-128">休憩</span><span class="sxs-lookup"><span data-stu-id="24cb6-128">Break for Work</span></span>
            -   <span data-ttu-id="24cb6-129">昼休み</span><span class="sxs-lookup"><span data-stu-id="24cb6-129">Break for Lunch</span></span>
            -   <span data-ttu-id="24cb6-130">退勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="24cb6-131">現在の状態</span><span class="sxs-lookup"><span data-stu-id="24cb6-131">Current state</span></span></th>
    <th><span data-ttu-id="24cb6-132">使用可能な操作</span><span class="sxs-lookup"><span data-stu-id="24cb6-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="24cb6-133">出勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="24cb6-134">休憩</span><span class="sxs-lookup"><span data-stu-id="24cb6-134">Break for Work</span></span></li>
    <li><span data-ttu-id="24cb6-135">昼休み</span><span class="sxs-lookup"><span data-stu-id="24cb6-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="24cb6-136">退勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="24cb6-137">休憩</span><span class="sxs-lookup"><span data-stu-id="24cb6-137">Break for Work</span></span></td>
    <td><span data-ttu-id="24cb6-138">出勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="24cb6-139">昼休み</span><span class="sxs-lookup"><span data-stu-id="24cb6-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="24cb6-140">出勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="24cb6-141">退勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-141">Clock-out</span></span></td>
    <td><span data-ttu-id="24cb6-142">出勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="24cb6-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="24cb6-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="24cb6-144">確認メッセージを表示して、現在の活動時間が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="24cb6-145">ログ帳:</span><span class="sxs-lookup"><span data-stu-id="24cb6-145">Logbook:</span></span>
    -   <span data-ttu-id="24cb6-146">[**ログ帳**] をクリックして、タイム レコーダーの活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="24cb6-147">タイム フィルターを使用して、異なる時間枠を選択します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="24cb6-148">複数の店舗の場所で作業する場合、時間を記録したすべての店舗からの時間登録が表示されます。</span><span class="sxs-lookup"><span data-stu-id="24cb6-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="24cb6-149">店舗フィルターを使用して、選択した店舗からの時間登録を表示できます。</span><span class="sxs-lookup"><span data-stu-id="24cb6-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="24cb6-150">異なるタイム ゾーン:</span><span class="sxs-lookup"><span data-stu-id="24cb6-150">Different time zones:</span></span>
    -   <span data-ttu-id="24cb6-151">別の場所からの時間を表示する場合で (レジ担当者ログ帳に対して、またはマネージャーのシナリオの [**タイム レコーダー エントリの表示**] を使用して)、その場所が別のタイム ゾーンである場合、表示される時刻記録はローカル タイム ゾーンに変換されます。</span><span class="sxs-lookup"><span data-stu-id="24cb6-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="24cb6-152">たとえば、アリゾナとネバダの 2 つの店舗のマネージャだと仮定します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="24cb6-153">レジ担当者は午前 9 時に</span><span class="sxs-lookup"><span data-stu-id="24cb6-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="24cb6-154">アリゾナで出勤を登録します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-154">in Arizona.</span></span> <span data-ttu-id="24cb6-155">その時点で、ネバダの時刻は午前 8 時です。</span><span class="sxs-lookup"><span data-stu-id="24cb6-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="24cb6-156">したがって、ネバダの店舗にいて時間登録のレコードを見ている場合、時間登録は 8 A.M としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="24cb6-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="24cb6-157">作業者の時間登録の表示</span><span class="sxs-lookup"><span data-stu-id="24cb6-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="24cb6-158">作業者の時間登録を表示して、店舗または活動のタイプごとにフィルター処理をする</span><span class="sxs-lookup"><span data-stu-id="24cb6-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="24cb6-159">POS で:</span><span class="sxs-lookup"><span data-stu-id="24cb6-159">On POS:</span></span>

-   <span data-ttu-id="24cb6-160">[**タイム レコーダー エントリの表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="24cb6-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="24cb6-161">あなたが割り当てられている同じ店舗に割り当てられているすべての作業者のタイム レコーダーの登録活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="24cb6-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="24cb6-162">活動タイプを使用して、時間登録をフィルター処理するフィルターを保存できます。</span><span class="sxs-lookup"><span data-stu-id="24cb6-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="24cb6-163">時間登録の処理と管理</span><span class="sxs-lookup"><span data-stu-id="24cb6-163">Process and manage time registrations</span></span>
<span data-ttu-id="24cb6-164">Dynamics 365 for Retail ユーザーは、計算、承認および給与への時間登録の転送のためのワークフローに従います。</span><span class="sxs-lookup"><span data-stu-id="24cb6-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="24cb6-165">基本工程</span><span class="sxs-lookup"><span data-stu-id="24cb6-165">Primary operations</span></span>

-   <span data-ttu-id="24cb6-166">計算</span><span class="sxs-lookup"><span data-stu-id="24cb6-166">Calculate</span></span>
-   <span data-ttu-id="24cb6-167">承認</span><span class="sxs-lookup"><span data-stu-id="24cb6-167">Approve</span></span>
-   <span data-ttu-id="24cb6-168">給与に送信</span><span class="sxs-lookup"><span data-stu-id="24cb6-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="24cb6-169">他の共通の操作</span><span class="sxs-lookup"><span data-stu-id="24cb6-169">Other common operations</span></span>

-   <span data-ttu-id="24cb6-170">一括退勤</span><span class="sxs-lookup"><span data-stu-id="24cb6-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="24cb6-171">休暇の登録</span><span class="sxs-lookup"><span data-stu-id="24cb6-171">Register Absence</span></span>

<span data-ttu-id="24cb6-172">時刻と出勤の登録の処理方法の詳細については、<https://technet.microsoft.com/en-us/library/aa573180.aspx> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24cb6-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




