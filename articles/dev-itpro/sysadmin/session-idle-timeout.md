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
ms.openlocfilehash: fe6cd67291363b6056987a8bc46f7e9a021acf79
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866968"
---
# <a name="set-the-session-idle-timeout"></a><span data-ttu-id="fe338-103">セッション アイドル タイムアウトの設定</span><span class="sxs-lookup"><span data-stu-id="fe338-103">Set the session idle timeout</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="fe338-104">セッション アイドル タイムアウト設定は、ユーザーのセッションがタイムアウトして閉じる前にユーザーが非アクティブになれる時間の長さを表します。</span><span class="sxs-lookup"><span data-stu-id="fe338-104">The session idle timeout setting represents the amount of time a user can be inactive before the user's session times out and closes.</span></span> <span data-ttu-id="fe338-105">ユーザーブラウザセッションにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="fe338-105">It only affects user browser sessions.</span></span>

<span data-ttu-id="fe338-106">この値は、5 分から 60 分の間で設定できます。</span><span class="sxs-lookup"><span data-stu-id="fe338-106">You can set the values from 5 minutes to 60 minutes.</span></span>

<span data-ttu-id="fe338-107">この機能には、30 分の既定値があります。</span><span class="sxs-lookup"><span data-stu-id="fe338-107">This function has a default value of 30 minutes.</span></span> <span data-ttu-id="fe338-108">最大 60 分まで値を設定できますが、これによりシステムに余分な負荷が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fe338-108">You can set the value up to 60 minutes, however doing so might cause extra load on the system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe338-109">以前 web.config (**WebClientStatefulSessionTimeoutInSeconds**キー) でセッションアイドルタイムアウトを設定していた場合には、サポート要求を通じて、その以前の値が引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="fe338-109">If you previously set a session idle timeout in the web.config (**WebClientStatefulSessionTimeoutInSeconds** key) through a support request, then that old value will still be honored.</span></span> <span data-ttu-id="fe338-110">既定の変更では、web config で新しいセッションアイドルタイムアウトを明示的に設定していない人にのみ変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="fe338-110">The change in default will only affect those who had not explicitly set a new session idle timeout in the web config.</span></span>

<span data-ttu-id="fe338-111">この値を変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fe338-111">To change the value, follow these steps:</span></span>

1. <span data-ttu-id="fe338-112">Finance and Operations ダッシュボードから、**システム管理** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe338-112">From the Finance and Operations dashboard, select the **System Administration** workspace.</span></span>
2. <span data-ttu-id="fe338-113">**システム設定** の選択</span><span class="sxs-lookup"><span data-stu-id="fe338-113">Select **System Settings**.</span></span> <span data-ttu-id="fe338-114">これにより、**システム パラメーター** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="fe338-114">This opens the **System parameters** page.</span></span>
3. <span data-ttu-id="fe338-115">**セッション管理** セクションで、**セッション アイドル タイムアウトを分単位で** 設定します。</span><span class="sxs-lookup"><span data-stu-id="fe338-115">In the **Session management** section, set **Session idle timeout in minutes**.</span></span>
4. <span data-ttu-id="fe338-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe338-116">Select **Save**.</span></span> 

    <span data-ttu-id="fe338-117">この値を 30 より大きい値に設定すると、選択を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe338-117">If you set the value to greater than 30, you will be prompted to confirm your selection.</span></span> <span data-ttu-id="fe338-118">「アイドル セッション タイムアウトの増加によって、システムに余分な負荷が発生することがあります」 という確認メッセージが表示され、これにより、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fe338-118">The confirmation prompt says "Increasing the idle session timeout can cause extra load on your system, which can lead to a decrease in performance.</span></span> <span data-ttu-id="fe338-119">本当に続行しますか？</span><span class="sxs-lookup"><span data-stu-id="fe338-119">Are you sure you want to continue?"</span></span> <span data-ttu-id="fe338-120">この値が大きくなるほど負荷が大きくなり、システム パフォーマンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fe338-120">The higher the value, the higher the load will be, which can affect negatively system performance.</span></span> <span data-ttu-id="fe338-121">**はい**を選択して変更を保存するか、**いいえ**を選択して既存値に戻します。</span><span class="sxs-lookup"><span data-stu-id="fe338-121">Select **Yes** to save the changes, or **No** to revert to the existing value.</span></span>

