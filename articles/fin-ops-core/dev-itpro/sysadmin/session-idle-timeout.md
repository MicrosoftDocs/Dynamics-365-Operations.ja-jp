---
title: セッション非活動タイムアウトの設定
description: このトピックでは、セッション非活動タイムアウトを設定する方法について説明します。
author: paulliew
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: IT Pro
ms.reviewer: sericks
ms.custom: 13531
ms.search.region: Global
ms.author: paulliew
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: Platform update 29
ms.openlocfilehash: 1669eaa11c7b134ada09d8e2804df8ef9bae5a40
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690114"
---
# <a name="set-the-session-inactivity-timeout"></a><span data-ttu-id="e513a-103">セッション非活動タイムアウトの設定</span><span class="sxs-lookup"><span data-stu-id="e513a-103">Set the session inactivity timeout</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e513a-104">セッション非活動タイムアウト設定は、ユーザーのセッションがタイムアウトして閉じる前にユーザーが非活動になれる時間の長さを表します。</span><span class="sxs-lookup"><span data-stu-id="e513a-104">The session inactivity timeout setting represents the amount of time a user can be inactive before the user's session times out and closes.</span></span> <span data-ttu-id="e513a-105">ユーザーブラウザセッションにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="e513a-105">It only affects user browser sessions.</span></span>

<span data-ttu-id="e513a-106">この値は、5 分から 60 分の間で設定できます。</span><span class="sxs-lookup"><span data-stu-id="e513a-106">You can set the values from 5 minutes to 60 minutes.</span></span>

<span data-ttu-id="e513a-107">この機能には、30 分の既定値があります。</span><span class="sxs-lookup"><span data-stu-id="e513a-107">This function has a default value of 30 minutes.</span></span> <span data-ttu-id="e513a-108">最大 60 分まで値を設定できますが、これによりシステムに余分な負荷が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e513a-108">You can set the value up to 60 minutes, however doing so might cause extra load on the system.</span></span>

> [!NOTE] 
> <span data-ttu-id="e513a-109">この機能は、Platform update 29 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="e513a-109">This feature is available as of Platform update 29.</span></span>
>
> <span data-ttu-id="e513a-110">以前 web.config (**WebClientStatefulSessionTimeoutInSeconds** キー) でセッション非活動タイムアウトを設定していた場合には、サポート要求を通じて、その以前の値が引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="e513a-110">If you previously set a session inactivity timeout in the web.config (**WebClientStatefulSessionTimeoutInSeconds** key) through a support request, then that old value will still be honored.</span></span> <span data-ttu-id="e513a-111">既定の変更では、web config で新しいセッション非活動タイムアウトを明示的に設定していない人にのみ変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="e513a-111">The change in default will only affect those who had not explicitly set a new session inactivity timeout in the web config.</span></span>

<span data-ttu-id="e513a-112">この値を変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e513a-112">To change the value, follow these steps:</span></span>

1. <span data-ttu-id="e513a-113">**システム管理 > 設定 > システム パラメーター** を選択して、**システム パラメーター** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e513a-113">Select **System administration > Setup > System parameters** to open the **System parameters** page.</span></span>
2. <span data-ttu-id="e513a-114">**一般** タブの **セッションの管理** セクションで、**セッション非活動タイムアウト (分)** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e513a-114">On the **General** tab, in the **Session management** section, enter a value in the **Session inactivity timeout in minutes** field.</span></span>
3. <span data-ttu-id="e513a-115">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e513a-115">Select **Save**.</span></span> 

    <span data-ttu-id="e513a-116">この値を 30 より大きい値に設定すると、選択を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e513a-116">If you set the value to greater than 30, you will be prompted to confirm your selection.</span></span> <span data-ttu-id="e513a-117">以下のような確認を求めるメッセージが表示されます。「非活動セッションタイムアウトの増加によって、システムに余分な負荷が発生することがあり、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e513a-117">The confirmation prompt says "Increasing the inactivity session timeout can cause extra load on your system, which can lead to a decrease in performance.</span></span> <span data-ttu-id="e513a-118">本当に続行しますか？</span><span class="sxs-lookup"><span data-stu-id="e513a-118">Are you sure you want to continue?"</span></span> <span data-ttu-id="e513a-119">この値が大きくなるほど負荷が大きくなり、システム パフォーマンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e513a-119">The higher the value, the higher the load will be, which can affect negatively system performance.</span></span> <span data-ttu-id="e513a-120">**はい** を選択して変更を保存するか、**いいえ** を選択して既存値に戻します。</span><span class="sxs-lookup"><span data-stu-id="e513a-120">Select **Yes** to save the changes, or **No** to revert to the existing value.</span></span>
    
### <a name="alerting-users-before-sessions-end-due-to-inactivity"></a><span data-ttu-id="e513a-121">非操作時間の経過によりセッションが終了する前にユーザーに警告する</span><span class="sxs-lookup"><span data-stu-id="e513a-121">Alerting users before sessions end due to inactivity</span></span>
<span data-ttu-id="e513a-122">非活動によりセッションが中断されることをユーザーに認識させ、保存されていない変更をユーザーが失わないようにするために、非活動によるセッションの終了が設定される前にユーザーに通知され、再接続の機会が与えられます。</span><span class="sxs-lookup"><span data-stu-id="e513a-122">To give users awareness of an impending session suspension due to inactivity and to help prevent users from losing any unsaved changes when this occurs, users will be notified before their sessions are set to be terminated due to inactivity and given an opportunity to reconnect.</span></span> <span data-ttu-id="e513a-123">ユーザーへの通知は、**セッション非活動タイムアウト** の設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e513a-123">The notice given to the user is dependent on the **Session inactivity timeout** setting.</span></span> 

-  <span data-ttu-id="e513a-124">**セッション非活動タイムアウト** が 30 分を超える場合は、セッションが終了に設定される **5 分** 前にカウントダウン通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e513a-124">If the **Session inactivity timeout** is more than 30 minutes, the user will see a countdown notification starting **5 minutes** before the session is set to close.</span></span> 
-  <span data-ttu-id="e513a-125">**セッション非活動タイムアウト** が 10 分～30 分の間である場合は、セッションが終了に設定される **2 分** 前にカウントダウン通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e513a-125">If the **Session inactivity timeout** is between 10 and 30 minutes, the user will see a countdown notification starting **2 minutes** before the session is set to close.</span></span> 
-  <span data-ttu-id="e513a-126">**セッション非活動タイムアウト** が 10 分以下の場合は、セッションが終了に設定される **30 秒** 前にカウントダウン通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e513a-126">If the **Session inactivity timeout** is less than 10 minutes, the user will see a countdown notification starting **30 seconds** before the session is set to close.</span></span>

