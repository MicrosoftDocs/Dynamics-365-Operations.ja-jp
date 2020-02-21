---
title: セッション アイドル タイムアウトの設定
description: このトピックでは、セッション アイドル タイムアウトの設定方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 08/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 13531
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: Platform update 29
ms.openlocfilehash: 112027eee5ecfb1b8989c0cc107d5bb5ad64209b
ms.sourcegitcommit: 9f4719e2be75cdfc6c59617a3141ba2fa1da00dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2020
ms.locfileid: "3033786"
---
# <a name="set-the-session-idle-timeout"></a><span data-ttu-id="9ebbe-103">セッション アイドル タイムアウトの設定</span><span class="sxs-lookup"><span data-stu-id="9ebbe-103">Set the session idle timeout</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9ebbe-104">セッション アイドル タイムアウト設定は、ユーザーのセッションがタイムアウトして閉じる前にユーザーが非アクティブになれる時間の長さを表します。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-104">The session idle timeout setting represents the amount of time a user can be inactive before the user's session times out and closes.</span></span> <span data-ttu-id="9ebbe-105">ユーザーブラウザセッションにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-105">It only affects user browser sessions.</span></span>

<span data-ttu-id="9ebbe-106">この値は、5 分から 60 分の間で設定できます。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-106">You can set the values from 5 minutes to 60 minutes.</span></span>

<span data-ttu-id="9ebbe-107">この機能には、30 分の既定値があります。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-107">This function has a default value of 30 minutes.</span></span> <span data-ttu-id="9ebbe-108">最大 60 分まで値を設定できますが、これによりシステムに余分な負荷が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-108">You can set the value up to 60 minutes, however doing so might cause extra load on the system.</span></span>

> [!NOTE] 
> <span data-ttu-id="9ebbe-109">この機能は、Platform update 29 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-109">This feature is available as of Platform update 29.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ebbe-110">以前 web.config (**WebClientStatefulSessionTimeoutInSeconds**キー) でセッションアイドルタイムアウトを設定していた場合には、サポート要求を通じて、その以前の値が引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-110">If you previously set a session idle timeout in the web.config (**WebClientStatefulSessionTimeoutInSeconds** key) through a support request, then that old value will still be honored.</span></span> <span data-ttu-id="9ebbe-111">既定の変更では、web config で新しいセッションアイドルタイムアウトを明示的に設定していない人にのみ変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-111">The change in default will only affect those who had not explicitly set a new session idle timeout in the web config.</span></span>

<span data-ttu-id="9ebbe-112">この値を変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-112">To change the value, follow these steps:</span></span>

1. <span data-ttu-id="9ebbe-113">ダッシュボードから、**システム管理**ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-113">From the dashboard, select the **System Administration** workspace.</span></span>
2. <span data-ttu-id="9ebbe-114">**システム設定** の選択</span><span class="sxs-lookup"><span data-stu-id="9ebbe-114">Select **System Settings**.</span></span> <span data-ttu-id="9ebbe-115">これにより、**システム パラメーター** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-115">This opens the **System parameters** page.</span></span>
3. <span data-ttu-id="9ebbe-116">**セッション管理** セクションで、**セッション アイドル タイムアウトを分単位で** 設定します。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-116">In the **Session management** section, set **Session idle timeout in minutes**.</span></span>
4. <span data-ttu-id="9ebbe-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-117">Select **Save**.</span></span> 

    <span data-ttu-id="9ebbe-118">この値を 30 より大きい値に設定すると、選択を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-118">If you set the value to greater than 30, you will be prompted to confirm your selection.</span></span> <span data-ttu-id="9ebbe-119">「アイドル セッション タイムアウトの増加によって、システムに余分な負荷が発生することがあります」 という確認メッセージが表示され、これにより、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-119">The confirmation prompt says "Increasing the idle session timeout can cause extra load on your system, which can lead to a decrease in performance.</span></span> <span data-ttu-id="9ebbe-120">本当に続行しますか？</span><span class="sxs-lookup"><span data-stu-id="9ebbe-120">Are you sure you want to continue?"</span></span> <span data-ttu-id="9ebbe-121">この値が大きくなるほど負荷が大きくなり、システム パフォーマンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-121">The higher the value, the higher the load will be, which can affect negatively system performance.</span></span> <span data-ttu-id="9ebbe-122">**はい**を選択して変更を保存するか、**いいえ**を選択して既存値に戻します。</span><span class="sxs-lookup"><span data-stu-id="9ebbe-122">Select **Yes** to save the changes, or **No** to revert to the existing value.</span></span>

