---
title: Trace Parser を使用してトレースを実行
description: このチュートリアルでは、トレースする方法についてのガイドラインを示します。
author: RobinARH
ms.date: 10/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 25471
ms.assetid: 607c1810-f872-4b23-a2c7-ee01522d90e3
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e5604625a8e974d96781341da889bdca362036be
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745139"
---
# <a name="take-traces-by-using-trace-parser"></a><span data-ttu-id="7a297-103">Trace Parser を使用してトレースを実行</span><span class="sxs-lookup"><span data-stu-id="7a297-103">Take traces by using Trace parser</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a297-104">このチュートリアルでは、トレースする方法についてのガイドラインを示します。</span><span class="sxs-lookup"><span data-stu-id="7a297-104">This tutorial provides guidelines on how to take traces.</span></span>

<span data-ttu-id="7a297-105">このチュートリアルでは、トレースの収集およびダウンロード方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a297-105">In this tutorial, you'll take a tour of how to collect and download traces.</span></span> <span data-ttu-id="7a297-106">トレース分析ツールは、Microsoft Dynamics AX 2012 バージョンとほぼ同じように機能しますが、後方互換性はなく、AX 2012 トレースの分析には使用できません。</span><span class="sxs-lookup"><span data-stu-id="7a297-106">The trace analysis tool works largely similar to the Microsoft Dynamics AX 2012 version, but it is not backward compatible and can't be used to analyze AX 2012 traces.</span></span> <span data-ttu-id="7a297-107">トレース パーサー ツールは、開発環境の PerfSDK フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="7a297-107">The trace parser tool can be found in the PerfSDK folder on your development deployments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7a297-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="7a297-108">Prerequisites</span></span>

<span data-ttu-id="7a297-109">このチュートリアルでは、インスタンスの管理者として環境にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a297-109">This tutorial requires that you access the environment as an administrator on the instance.</span></span> <span data-ttu-id="7a297-110">管理者は、トレースを実行する権限を他のユーザーに付与することもできます。</span><span class="sxs-lookup"><span data-stu-id="7a297-110">The administrator can also grant rights to other users to take a trace.</span></span> <span data-ttu-id="7a297-111">このようにして、管理者権限では再現できないシナリオをトレースできます。</span><span class="sxs-lookup"><span data-stu-id="7a297-111">In this way, you can trace scenarios that can't be reproduced with administrative rights.</span></span>

## <a name="capture-the-trace"></a><span data-ttu-id="7a297-112">トレースをキャプチャする</span><span class="sxs-lookup"><span data-stu-id="7a297-112">Capture the trace</span></span>

1. <span data-ttu-id="7a297-113">トレースする前に、シナリオがウォーム状態にあることを確認してください。つまり、トレースを実行する前に、トレースするシナリオを一度実行することを意味します。</span><span class="sxs-lookup"><span data-stu-id="7a297-113">Before you trace make sure your scenario is in a warm state, meaning that you have run the scenario you want to trace once before you take the trace.</span></span> <span data-ttu-id="7a297-114">ウォーム状態にあると、メタデータの読み込みやその他の可能なウォームアップ タスクなどがトレースに含まれなくなります。</span><span class="sxs-lookup"><span data-stu-id="7a297-114">Being in a warm state prevents things like metadata loading and other possible warm-up tasks from being in the trace.</span></span>
2. <span data-ttu-id="7a297-115">ナビゲーションバーで、**ヘルプ**、**トレース** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="7a297-115">In the navigation bar, select **Help**, and then select **Trace**.</span></span> 
3. <span data-ttu-id="7a297-116">キャプチャしようとしているトレースに名前を付けて、**トレースの開始** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a297-116">Name the trace that you are about to capture, and then select **Start trace**.</span></span>
4. <span data-ttu-id="7a297-117">分析が必要なアクションを実行します。たとえば、**買掛金勘定 &gt; ベンダー &gt; すべてのベンダー** を開きます。</span><span class="sxs-lookup"><span data-stu-id="7a297-117">Perform actions that need to be analyzed, for example, opening **Accounts payable &gt; Vendors &gt; All vendors**.</span></span>
5. <span data-ttu-id="7a297-118">終了したら、**トレースの停止** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a297-118">When you are finished, select **Stop trace**.</span></span> <span data-ttu-id="7a297-119">その後、次のいずれかのオプションを選択できます (このチュートリアルでは、2 番目のオプションを選択します)。</span><span class="sxs-lookup"><span data-stu-id="7a297-119">Then, you can select one of the following options (for this tutorial, select the second option):</span></span>
    - <span data-ttu-id="7a297-120">**トレースのダウンロード** - キャプチャしたトレースをローカル マシンに保存します。</span><span class="sxs-lookup"><span data-stu-id="7a297-120">**Download trace** – Store the captured trace on a local machine.</span></span> <span data-ttu-id="7a297-121">Trace Parser のデスクトップ バージョンでダウンロードしたトレースを分析することができます。</span><span class="sxs-lookup"><span data-stu-id="7a297-121">You can analyze a downloaded trace with the desktop version of Trace Parser.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7a297-122">注記: トレースをダウンロードすると、後でアップロードすることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="7a297-122">If you download a trace it will not be available for later uploading.</span></span>

    - <span data-ttu-id="7a297-123">**トレースのアップロード** – トレースをクラウドに保存して、後で管理者などがダウンロードできるようにします。7 日後に自動的に削除され、キャプチャされたトレース フォームから手動で削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="7a297-123">**Upload trace** – Store the trace in the cloud for later downloading by, for example, the admin, it will be automatically deleted after 7 days and can also be deleted manually from the captured traces form.</span></span>

> [!NOTE]
> <span data-ttu-id="7a297-124">シナリオに 1 〜 2 分以上かかる場合は、トレースが大きくなりすぎて簡単に分析できず、トレースが大きくなりすぎるとデータが失われるリスクがあるため、それぞれ 30 秒の小さなトレースを複数取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7a297-124">If your scenario takes more than 1-2 minutes it is better to try to take multiple smaller traces of 30 seconds each as the trace will likely get too big to be easily analyzed and there is a risk for losing data if the trace gets too big.</span></span>

## <a name="assign-trace-rights-to-user"></a><span data-ttu-id="7a297-125">ユーザーにトレース権限を割り当てます</span><span class="sxs-lookup"><span data-stu-id="7a297-125">Assign trace rights to user</span></span>

1. <span data-ttu-id="7a297-126">ユーザーにトレースをキャプチャする権利を与えるには、 **システム管理&gt; ユーザー &gt;ユーザー** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a297-126">To give a user rights to capture a trace, go to **System administration &gt; Users &gt; Users**.</span></span>
2. <span data-ttu-id="7a297-127">ユーザーを選択し、**システム追跡ユーザー** ロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a297-127">Select the user and assign the **System tracing user** role.</span></span> 

    <span data-ttu-id="7a297-128">[![ユーザーへのトレース権限の割り当ての例](./media/trace2-284x300.jpg)](./media/trace2.jpg)</span><span class="sxs-lookup"><span data-stu-id="7a297-128">[![Example of assigning trace rights to a user](./media/trace2-284x300.jpg)](./media/trace2.jpg)</span></span>

    <span data-ttu-id="7a297-129">ユーザーが不要なトレースを回避するために追跡を行ったら、ユーザー ロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="7a297-129">Remove the user role again once the user is done with tracing to avoid unwanted tracing.</span></span>

## <a name="open-captured-trace"></a><span data-ttu-id="7a297-130">キャプチャされたトレースを開く</span><span class="sxs-lookup"><span data-stu-id="7a297-130">Open captured trace</span></span>

1. <span data-ttu-id="7a297-131">ナビゲーションバーで、**ヘルプ**、**トレース** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="7a297-131">In the navigation bar, select **Help**, and then select **Trace**.</span></span>
2. <span data-ttu-id="7a297-132">キャプチャされたトレースを選択します。</span><span class="sxs-lookup"><span data-stu-id="7a297-132">Select Captured traces.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7a297-133">注記: キャプチャされたトレース ボタンは、管理者権限を持つユーザーだけが表示できます。</span><span class="sxs-lookup"><span data-stu-id="7a297-133">The captured traces button can only be seen by users with administrative rights.</span></span>

3. <span data-ttu-id="7a297-134">ダウンロードするトレース名を選択して開き、デスクトップ バージョンのトレース パーサーで分析または</span><span class="sxs-lookup"><span data-stu-id="7a297-134">Select the trace name to download to open and analyze it with the desktop version of trace parser or</span></span>
4. <span data-ttu-id="7a297-135">ユーザー名を選択して、ユーザー オプションを表示します。</span><span class="sxs-lookup"><span data-stu-id="7a297-135">Select the user name to get to the user options.</span></span>
5. <span data-ttu-id="7a297-136">必要に応じてトレースを削除します。</span><span class="sxs-lookup"><span data-stu-id="7a297-136">Delete the trace if you want.</span></span> <span data-ttu-id="7a297-137">トレースをダウンロードした場合は、削除する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7a297-137">You might do delete the trace if you have downloaded it.</span></span>

> [!NOTE]
> <span data-ttu-id="7a297-138">注記: トレースは、7 日後に削除されます。</span><span class="sxs-lookup"><span data-stu-id="7a297-138">The trace will be deleted after 7 days.</span></span> <span data-ttu-id="7a297-139">Trace Parser のデスクトップ バージョンの詳細については、[Trace Parser を使用して問題を診断し、パフォーマンスを分析します](trace-parser.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a297-139">For more information about the desktop version of trace parser, see [Diagnose issues and analyze performance by using Trace parser](trace-parser.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]