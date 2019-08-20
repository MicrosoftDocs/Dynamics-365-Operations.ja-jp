---
title: セッション アイドル タイムアウトの設定
description: このトピックでは、セッションアイドルタイムアウトを設定する方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 07/30/2019
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
ms.search.validFrom: 2019-08-02
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ccb32e1393e3fe776f2878a6a34bef97bbc12f0
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863645"
---
# <a name="set-the-session-idle-timeout"></a><span data-ttu-id="4de79-103">セッション アイドル タイムアウトの設定</span><span class="sxs-lookup"><span data-stu-id="4de79-103">Set the session idle timeout</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4de79-104">この機能は、Platform 更新 29 以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="4de79-104">This feature is available in Platform update 29 and later.</span></span>

<span data-ttu-id="4de79-105">セッション アイドル タイムアウト設定は、ユーザーのセッションがタイムアウトして閉じる前にユーザーが非アクティブになれる時間の長さを表します。</span><span class="sxs-lookup"><span data-stu-id="4de79-105">The session idle timeout setting represents the amount of time a user can be inactive before the user's session times out and closes.</span></span> <span data-ttu-id="4de79-106">ユーザーブラウザセッションにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="4de79-106">It only affects user browser sessions.</span></span>

<span data-ttu-id="4de79-107">この値は、5 分から 60 分の間で設定できます。</span><span class="sxs-lookup"><span data-stu-id="4de79-107">You can set the values from 5 minutes to 60 minutes.</span></span>

<span data-ttu-id="4de79-108">この機能は UI に公開されており、既定値は 30 分です。</span><span class="sxs-lookup"><span data-stu-id="4de79-108">This function is exposed to the UI and has a default value of 30 minutes.</span></span> <span data-ttu-id="4de79-109">最大 60 分まで値を設定できますが、これによりシステムに余分な負荷が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4de79-109">You can set the value up to 60 minutes, but doing so might cause extra load on the system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4de79-110">以前 web.config (**WebClientStatefulSessionTimeoutInSeconds**キー) でセッションアイドルタイムアウトを設定していた場合には、サポート要求を通じて、その以前の値が引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="4de79-110">If you previously set a session idle timeout in the web.config (**WebClientStatefulSessionTimeoutInSeconds** key) through a support request, then that old value will still be honored.</span></span> <span data-ttu-id="4de79-111">既定の変更では、web config で新しいセッションアイドルタイムアウトを明示的に設定していない人にのみ変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="4de79-111">The change in default will only affect those who had not explicitly set a new session idle timeout in the web config.</span></span>

<span data-ttu-id="4de79-112">UI の値を変更するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4de79-112">To change the value from the UI, follow these steps:</span></span>

1. <span data-ttu-id="4de79-113">Finance and Operations ダッシュボードから、**システム管理**ワークスペースをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4de79-113">From the Finance and Operations Dashboard, click on the **System Administration** workspace.</span></span>
2. <span data-ttu-id="4de79-114">**システム設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4de79-114">Click on **System Settings**.</span></span> <span data-ttu-id="4de79-115">これにより、**システムパラメータ** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="4de79-115">This opens the **System parameters** form.</span></span>
3. <span data-ttu-id="4de79-116">**セッション管理** セクションで、**セッションアイドルタイムアウトを分**単位で目的の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="4de79-116">In the **Session management** section, set the **Session idle timout in minutes** to the desired value.</span></span>
4. <span data-ttu-id="4de79-117">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4de79-117">Click **Save**.</span></span> 

    <span data-ttu-id="4de79-118">この値を 30 より大きい値に設定すると、選択を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4de79-118">If you set the value greater than 30, you will be prompted to confirm your selection.</span></span> <span data-ttu-id="4de79-119">「アイドルセッションタイムアウトの増加によって、システムに余分な負荷が発生することがある」という確認を求めるメッセージが表示され、これにより、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4de79-119">The confirmation prompt is "Increasing the idle session timeout can cause extra load on your system, which can lead to a decrease in performance.</span></span> <span data-ttu-id="4de79-120">本当に続行しますか？</span><span class="sxs-lookup"><span data-stu-id="4de79-120">Are you sure you want to continue?"</span></span> <span data-ttu-id="4de79-121">値が高くなるほど負荷が高くなり、負荷がシステムパフォーマンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4de79-121">The higher the value is, the higher the load will be, and the load can affect system performance negatively.</span></span> <span data-ttu-id="4de79-122">**はい**をクリックして変更を保存するか、**いいえ**をクリックして既存の値に戻します。</span><span class="sxs-lookup"><span data-stu-id="4de79-122">Click **Yes** to save the changes, or **No** to revert to the existing value.</span></span>

