---
title: Retail での時間と出勤管理
description: このトピックでは、Dynamics 365 Commerce の時間と出勤管理でサポートされているシナリオについて説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e28df09ecb592ae7df360d1b2d0bf06339c1410d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989380"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="5a47b-103">Retail での時間と出勤管理</span><span class="sxs-lookup"><span data-stu-id="5a47b-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a47b-104">このトピックでは、Dynamics 365 Commerce の時間と出勤管理でサポートされているシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="5a47b-105">作業者設定およびスケジュールの管理</span><span class="sxs-lookup"><span data-stu-id="5a47b-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="5a47b-106">初期コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5a47b-106">Initial configuration</span></span>

- <span data-ttu-id="5a47b-107">コンフィギュレーション ウィザードを実行します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="5a47b-108">時間登録作業者としての作業者を登録します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="5a47b-109">作業者のスケジュールを計画する</span><span class="sxs-lookup"><span data-stu-id="5a47b-109">Plan worker schedules</span></span>

- <span data-ttu-id="5a47b-110">ワーク プランナーを使用したプロファイルを適用します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="5a47b-111">詳細については、 [ワーク プランナーを使用したプロファイルの適用](https://technet.microsoft.com/library/aa551234.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a47b-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="5a47b-112">コンフィギュレーションの手順については、[時刻と出勤の設定](https://technet.microsoft.com/library/aa496971.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a47b-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="5a47b-113">コマース固有のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5a47b-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="5a47b-114">時間登録を有効にする作業者のタイム レコーダーの機能プロファイルを有効にします。</span><span class="sxs-lookup"><span data-stu-id="5a47b-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="5a47b-115">**POS機能プロファイル** &gt; **機能** &gt; **POS 時間登録** &gt; **時間登録の有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a47b-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="5a47b-116">販売時点管理 (POS) のアクセス許可グループをコンフィギュレーションして、[タイム レコーダー エントリの表示] のアクセス許可を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5a47b-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="5a47b-117">このアクセス許可により、ユーザーが、その店舗 (およびアドレス帳を介してユーザーが関連付けられている他のすべての店舗から) の他の作業者のタイム レコーダー登録を表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5a47b-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="5a47b-118">レジ担当者ロールではなくマネージャー ロールに対してこのアクセス許可を有効にする場合があります。</span><span class="sxs-lookup"><span data-stu-id="5a47b-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="5a47b-119">**POS アクセス許可グループ** &gt; **タイム レコーダー エントリの表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a47b-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="5a47b-120">時刻の登録</span><span class="sxs-lookup"><span data-stu-id="5a47b-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="5a47b-121">レジ担当者と非レジ担当者の時間登録</span><span class="sxs-lookup"><span data-stu-id="5a47b-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="5a47b-122">POS で:</span><span class="sxs-lookup"><span data-stu-id="5a47b-122">On POS:</span></span>

    - <span data-ttu-id="5a47b-123">出勤操作:</span><span class="sxs-lookup"><span data-stu-id="5a47b-123">Clock-in operations:</span></span>

        - <span data-ttu-id="5a47b-124">非ドロワー操作または新しいシフトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="5a47b-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="5a47b-125">タイム レコーダーの操作を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="5a47b-126">必要な操作を選択します:</span><span class="sxs-lookup"><span data-stu-id="5a47b-126">Select a desired operation:</span></span>

            - <span data-ttu-id="5a47b-127">出勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-127">Clock-in</span></span>
            - <span data-ttu-id="5a47b-128">休憩</span><span class="sxs-lookup"><span data-stu-id="5a47b-128">Break for Work</span></span>
            - <span data-ttu-id="5a47b-129">昼休み</span><span class="sxs-lookup"><span data-stu-id="5a47b-129">Break for Lunch</span></span>
            - <span data-ttu-id="5a47b-130">退勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="5a47b-131">現在の状態</span><span class="sxs-lookup"><span data-stu-id="5a47b-131">Current state</span></span></th>
        <th><span data-ttu-id="5a47b-132">使用可能な操作</span><span class="sxs-lookup"><span data-stu-id="5a47b-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="5a47b-133">出勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="5a47b-134">休憩</span><span class="sxs-lookup"><span data-stu-id="5a47b-134">Break for Work</span></span></li>
        <li><span data-ttu-id="5a47b-135">昼休み</span><span class="sxs-lookup"><span data-stu-id="5a47b-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="5a47b-136">退勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="5a47b-137">休憩</span><span class="sxs-lookup"><span data-stu-id="5a47b-137">Break for Work</span></span></td>
        <td><span data-ttu-id="5a47b-138">出勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="5a47b-139">昼休み</span><span class="sxs-lookup"><span data-stu-id="5a47b-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="5a47b-140">出勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="5a47b-141">退勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-141">Clock-out</span></span></td>
        <td><span data-ttu-id="5a47b-142">出勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="5a47b-143">[![タイム レコーダーの状態](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="5a47b-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="5a47b-144">確認メッセージを表示して、現在の活動時間が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="5a47b-145">ログ帳:</span><span class="sxs-lookup"><span data-stu-id="5a47b-145">Logbook:</span></span>

    - <span data-ttu-id="5a47b-146">**ログ帳** をクリックして、タイム レコーダーの活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="5a47b-147">タイム フィルターを使用して、異なる時間枠を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="5a47b-148">複数の店舗の場所で作業する場合、時間を記録したすべての店舗からの時間登録が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a47b-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="5a47b-149">店舗フィルターを使用して、選択した店舗からの時間登録を表示できます。</span><span class="sxs-lookup"><span data-stu-id="5a47b-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="5a47b-150">異なるタイム ゾーン:</span><span class="sxs-lookup"><span data-stu-id="5a47b-150">Different time zones:</span></span>

    - <span data-ttu-id="5a47b-151">別の場所からの時間を表示する場合で (レジ担当者ログ帳に対して、またはマネージャーのシナリオの **タイム レコーダー エントリの表示** を使用して)、その場所が別のタイム ゾーンである場合、表示される時刻記録はローカル タイム ゾーンに変換されます。</span><span class="sxs-lookup"><span data-stu-id="5a47b-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="5a47b-152">たとえば、アリゾナとネバダの 2 つの店舗のマネージャだと仮定します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="5a47b-153">レジ担当者は午前 9 時に</span><span class="sxs-lookup"><span data-stu-id="5a47b-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="5a47b-154">アリゾナで出勤を登録します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-154">in Arizona.</span></span> <span data-ttu-id="5a47b-155">その時点で、ネバダの時刻は午前 8 時です。</span><span class="sxs-lookup"><span data-stu-id="5a47b-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="5a47b-156">したがって、ネバダの店舗にいて時間登録のレコードを見ている場合、時間登録は 8 A.M としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="5a47b-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="5a47b-157">作業者の時間登録の表示</span><span class="sxs-lookup"><span data-stu-id="5a47b-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="5a47b-158">作業者の時間登録を表示して、店舗または活動のタイプごとにフィルター処理をする</span><span class="sxs-lookup"><span data-stu-id="5a47b-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="5a47b-159">POS で:</span><span class="sxs-lookup"><span data-stu-id="5a47b-159">On POS:</span></span>

- <span data-ttu-id="5a47b-160">**タイム レコーダー エントリの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a47b-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="5a47b-161">あなたが割り当てられている同じ店舗に割り当てられているすべての作業者のタイム レコーダーの登録活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a47b-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="5a47b-162">活動タイプを使用して、時間登録をフィルター処理するフィルターを保存できます。</span><span class="sxs-lookup"><span data-stu-id="5a47b-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="5a47b-163">時間登録の処理と管理</span><span class="sxs-lookup"><span data-stu-id="5a47b-163">Process and manage time registrations</span></span>

<span data-ttu-id="5a47b-164">コマース ユーザーは、計算、承認および給与への時間登録の転送のためのワークフローに従います。</span><span class="sxs-lookup"><span data-stu-id="5a47b-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="5a47b-165">基本工程</span><span class="sxs-lookup"><span data-stu-id="5a47b-165">Primary operations</span></span>

- <span data-ttu-id="5a47b-166">計算</span><span class="sxs-lookup"><span data-stu-id="5a47b-166">Calculate</span></span>
- <span data-ttu-id="5a47b-167">承認</span><span class="sxs-lookup"><span data-stu-id="5a47b-167">Approve</span></span>
- <span data-ttu-id="5a47b-168">給与に送信</span><span class="sxs-lookup"><span data-stu-id="5a47b-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="5a47b-169">他の共通の操作</span><span class="sxs-lookup"><span data-stu-id="5a47b-169">Other common operations</span></span>

- <span data-ttu-id="5a47b-170">一括退勤</span><span class="sxs-lookup"><span data-stu-id="5a47b-170">Bulk Clock-out</span></span>
- <span data-ttu-id="5a47b-171">休暇の登録</span><span class="sxs-lookup"><span data-stu-id="5a47b-171">Register Absence</span></span>

<span data-ttu-id="5a47b-172">時刻と出勤の登録の処理方法については、[時刻と出勤の登録を処理](https://technet.microsoft.com/library/aa573180.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a47b-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
