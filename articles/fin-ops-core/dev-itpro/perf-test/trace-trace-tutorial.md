---
title: Trace Parser を使用してトレースを実行
description: このチュートリアルでは、トレースする方法についてのガイドラインを示します。
author: RobinARH
manager: AnnBe
ms.date: 10/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 25471
ms.assetid: 607c1810-f872-4b23-a2c7-ee01522d90e3
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53bca1d43646ac43a8689308879a03e50685f9d4
ms.sourcegitcommit: 4925136bd9bbeeb1db5aa35ed174e8342a3a300e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2019
ms.locfileid: "2673386"
---
# <a name="take-traces-by-using-trace-parser"></a><span data-ttu-id="474be-103">Trace Parser を使用してトレースを実行</span><span class="sxs-lookup"><span data-stu-id="474be-103">Take traces by using Trace parser</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="474be-104">このチュートリアルでは、トレースする方法についてのガイドラインを示します。</span><span class="sxs-lookup"><span data-stu-id="474be-104">This tutorial provides guidelines on how to take traces.</span></span>

<span data-ttu-id="474be-105">このチュートリアルでは、トレースの収集およびダウンロード方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="474be-105">In this tutorial, you'll take a tour of how to collect and download traces.</span></span> <span data-ttu-id="474be-106">トレース分析ツールは、Microsoft Dynamics AX 2012 バージョンとほぼ同じように機能しますが、後方互換性はなく、AX 2012 トレースの分析には使用できません。</span><span class="sxs-lookup"><span data-stu-id="474be-106">The trace analysis tool works largely similar to the Microsoft Dynamics AX 2012 version, but it is not backward compatible and can't be used to analyze AX 2012 traces.</span></span> <span data-ttu-id="474be-107">トレース パーサー ツールは、開発環境の PerfSDK フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="474be-107">The trace parser tool can be found in the PerfSDK folder on your development deployments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="474be-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="474be-108">Prerequisites</span></span>
<span data-ttu-id="474be-109">このチュートリアルでは、インスタンスの管理者として環境にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="474be-109">This tutorial requires that you access the environment as an administrator on the instance.</span></span> <span data-ttu-id="474be-110">管理者は、トレースを実行する権限を他のユーザーに付与することもできます。</span><span class="sxs-lookup"><span data-stu-id="474be-110">The administrator can also grant rights to other users to take a trace.</span></span> <span data-ttu-id="474be-111">この方法では、管理者権限で再現できないシナリオを追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="474be-111">In this way you can trace scenarios which can't be reproduced with administrative rights.</span></span>

## <a name="capture-the-trace"></a><span data-ttu-id="474be-112">トレースをキャプチャする</span><span class="sxs-lookup"><span data-stu-id="474be-112">Capture the trace</span></span>
1.  <span data-ttu-id="474be-113">トレースする前にシナリオが「ウォーム」状態になっていることを確認します。トレースを取得する前に一度トレースするシナリオを実行したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="474be-113">Before you trace make sure your scenario is in a "Warm" state meaning you executed the scenario you want to trace once before you take the trace.</span></span> <span data-ttu-id="474be-114">メタデータの読み込みや他の考えられるウォームアップ タスクなどの操作が、トレースで行われることがなくなります。</span><span class="sxs-lookup"><span data-stu-id="474be-114">That will prevent things like metadata loading and other possible warm up tasks from being in the trace.</span></span>
2.  <span data-ttu-id="474be-115">ナビゲーション バーで、**ヘルプ**を選択して**トレース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474be-115">In the navigation bar, select **Help**, and then click **Trace**.</span></span> 
3.  <span data-ttu-id="474be-116">キャプチャするトレースに名前を付けてから、**追跡の開始**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474be-116">Name the trace that you are about to capture, and then click **Start trace**.</span></span>
4.  <span data-ttu-id="474be-117">たとえば [買掛金勘定] &gt; [仕入先] &gt; [すべての仕入先] を開くなど、分析する必要があるアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="474be-117">Perform actions that need to be analyzed like for example opening "Accounts payable &gt; Vendors &gt; All vendors".</span></span>
5.  <span data-ttu-id="474be-118">完了したら、**追跡の停止** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474be-118">When you are finished, click **Stop trace**.</span></span> <span data-ttu-id="474be-119">その後、次のいずれかのオプションを選択できます (このチュートリアルでは、2 番目のオプションを選択します)。</span><span class="sxs-lookup"><span data-stu-id="474be-119">Then, you can select one of the following options (for this tutorial, select the second option):</span></span>
    -   <span data-ttu-id="474be-120">**トレースのダウンロード** - キャプチャしたトレースをローカル マシンに保存します。</span><span class="sxs-lookup"><span data-stu-id="474be-120">**Download trace** – Store the captured trace on a local machine.</span></span> <span data-ttu-id="474be-121">Trace Parser のデスクトップ バージョンでダウンロードしたトレースを分析することができます。</span><span class="sxs-lookup"><span data-stu-id="474be-121">You can analyze a downloaded trace with the desktop version of Trace Parser.</span></span> <span data-ttu-id="474be-122">**注記**: トレースをダウンロードすると、後でアップロードすることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="474be-122">**Note**: If you download a trace it will not be available for later uploading.</span></span>
    -   <span data-ttu-id="474be-123">**トレースのアップロード** – 管理者などによって後でダウンロードするためにクラウドに追跡が保存され、7 日後に自動的に削除され、キャプチャされたトレース フォームから手動でも削除することができます。</span><span class="sxs-lookup"><span data-stu-id="474be-123">**Upload trace** – Store the trace in the cloud for later downloading by for example the admin, it will be automatically deleted after 7 days and can also be deleted manually from the captured traces form.</span></span>

<span data-ttu-id="474be-124">**注意してください:** シナリオが 1 〜 2 分以上かかる場合は、トレースが大きすぎて分析しにくく、トレースが大きくなりすぎるとデータを失う危険があるため、それぞれ 30 秒の複数の小さなトレースを取ることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="474be-124">**Please note:** If your scenario takes more than 1-2 minutes it is better to try to take multiple smaller traces of 30 seconds each as the trace will likely get too big to be easily analyzed and there is a risk for losing data if the trace gets too big.</span></span>

## <a name="assign-trace-rights-to-user"></a><span data-ttu-id="474be-125">ユーザーにトレース権限を割り当てます</span><span class="sxs-lookup"><span data-stu-id="474be-125">Assign trace rights to user</span></span>
1.  <span data-ttu-id="474be-126">ユーザーにトレースをキャプチャする権利を与えるには、"システム管理&gt;ユーザー&gt;ユーザー" を参照してください。</span><span class="sxs-lookup"><span data-stu-id="474be-126">To give a user rights to capture a trace, go to "System administration &gt; Users &gt; Users".</span></span>
2.  <span data-ttu-id="474be-127">ユーザーを選択し、"システム追跡ユーザー" ロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="474be-127">Select the user and assign the "System tracing user" role.</span></span> 

    <span data-ttu-id="474be-128">[![ユーザーへのトレース権限の割り当ての例](./media/trace2-284x300.jpg)](./media/trace2.jpg)</span><span class="sxs-lookup"><span data-stu-id="474be-128">[![Example of assigning trace rights to a user](./media/trace2-284x300.jpg)](./media/trace2.jpg)</span></span>

    <span data-ttu-id="474be-129">ユーザーが不要なトレースを回避するために追跡を行ったら、ユーザー ロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="474be-129">Remove the user role again once the user is done with tracing to avoid unwanted tracing.</span></span>

## <a name="open-captured-trace"></a><span data-ttu-id="474be-130">キャプチャされたトレースを開く</span><span class="sxs-lookup"><span data-stu-id="474be-130">Open captured trace</span></span>
1.  <span data-ttu-id="474be-131">ナビゲーション バーで、**ヘルプ**を選択して**トレース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474be-131">In the navigation bar, select **Help**, and then click **Trace**.</span></span>
2.  <span data-ttu-id="474be-132">キャプチャされたトレースをクリックします。</span><span class="sxs-lookup"><span data-stu-id="474be-132">Click on Captured traces.</span></span> <span data-ttu-id="474be-133">**注記:** キャプチャされたトレース ボタンは、管理者権限を持つユーザーだけが表示できます。</span><span class="sxs-lookup"><span data-stu-id="474be-133">**Note:** The captured traces button can only be seen by users with administrative rights.</span></span>
3.  <span data-ttu-id="474be-134">ダウンロードする追跡名をクリックして、デスクトップ バージョンの Trace Parser または で開いて分析します</span><span class="sxs-lookup"><span data-stu-id="474be-134">Click on the trace name to download to open and analyze it with the desktop version of trace parser or</span></span>
4.  <span data-ttu-id="474be-135">ユーザー オプションを表示するには、ユーザー名をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474be-135">Click on the user name to get to the user options.</span></span>
5.  <span data-ttu-id="474be-136">必要に応じてトレースを削除します。</span><span class="sxs-lookup"><span data-stu-id="474be-136">Delete the trace if you want.</span></span> <span data-ttu-id="474be-137">ダウンロードした場合には、これを行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="474be-137">You might do this if you have downloaded it.</span></span>

<span data-ttu-id="474be-138">**注記:** トレースは、7 日後に削除されます。</span><span class="sxs-lookup"><span data-stu-id="474be-138">**Note:** The trace will be deleted after 7 days.</span></span> <span data-ttu-id="474be-139">Trace Parser のデスクトップ バージョンの詳細については、[Trace parser: デスクトップ バージョンを使用した問題点の診断およびパフォーマンスの問題の分析](trace-parser.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="474be-139">For more information about the desktop version of trace parser, see [Trace parser: Using the desktop version to diagnose problems and analyze performance issues](trace-parser.md).</span></span>


