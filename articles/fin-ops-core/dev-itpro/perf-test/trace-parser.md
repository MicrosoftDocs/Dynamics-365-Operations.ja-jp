---
title: Trace Parser を使用した問題点の診断およびパフォーマンスの分析
description: このトピックでは、トレース パーサーを使用してトレースを操作し、展開におけるパフォーマンスを分析する方法について説明します。
author: RobinARH
ms.date: 10/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 13441
ms.assetid: eb0fbbaf-07d4-4a02-85e8-0d4f7920a0b9
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2dcdc54605bf7488bf8452a2f145f6201a2c57c
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189802"
---
# <a name="diagnose-issues-and-analyze-performance-by-using-trace-parser"></a><span data-ttu-id="cacf9-103">Trace Parser を使用した問題点の診断およびパフォーマンスの分析</span><span class="sxs-lookup"><span data-stu-id="cacf9-103">Diagnose issues and analyze performance by using Trace parser</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cacf9-104">このトピックでは、トレース パーサーを使用してトレースを操作し、展開におけるパフォーマンスを分析する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cacf9-104">This topic explains how you can use the Trace parser to consume traces and analyze performance in your deployment.</span></span> <span data-ttu-id="cacf9-105">Trace Parser を使用すると、さまざまな種類のエラーを見つけて診断することができます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-105">You can use the Trace Parser to find and diagnose various types of errors.</span></span> <span data-ttu-id="cacf9-106">また、ツールを使用して X++ メソッドの実行、および実行コール ツリーを視覚化することができます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-106">You can also use the tool to visualize execution of X++ methods, as well as the execution call tree.</span></span>

> [!NOTE]
> <span data-ttu-id="cacf9-107">Trace parser には Microsoft Dynamics AX 2012 と類似する機能が多数あります。</span><span class="sxs-lookup"><span data-stu-id="cacf9-107">There are many more features in the Trace parser are similar to Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="cacf9-108">詳細については、 [Dynamics Ax Performance チーム ブログ](/archive/blogs/axperf/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cacf9-108">See the [Dynamics Ax Performance Team Blog](/archive/blogs/axperf/) for more information.</span></span>

## <a name="finding-the-trace-parser"></a><span data-ttu-id="cacf9-109">Trace Parser の検索</span><span class="sxs-lookup"><span data-stu-id="cacf9-109">Finding the Trace parser</span></span>
<span data-ttu-id="cacf9-110">トレース パーサーには、開発者展開または VHD があらかじめインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cacf9-110">Trace parser should be preinstalled with your developer deployment or VHD.</span></span> <span data-ttu-id="cacf9-111">インストール場所は **C:\\Program Files (x86)\\Microsoft Dynamics Trace Parser** です。</span><span class="sxs-lookup"><span data-stu-id="cacf9-111">The install location is here: **C:\\Program Files (x86)\\Microsoft Dynamics Trace Parser**.</span></span> <span data-ttu-id="cacf9-112">インストールされていない場合は、インストーラーを **C:\\PerfSDK\\PerfTools\\traceparser.msi** から実行することができます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-112">If it's not installed, you can run the installer from **C:\\PerfSDK\\PerfTools\\traceparser.msi**.</span></span>

## <a name="capturing-events"></a><span data-ttu-id="cacf9-113">イベントのキャプチャ</span><span class="sxs-lookup"><span data-stu-id="cacf9-113">Capturing events</span></span>
<span data-ttu-id="cacf9-114">トレース パーサーで分析するデータを取得するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="cacf9-114">There are two ways that you can obtain the data that you will analyze in the Trace parser.</span></span> <span data-ttu-id="cacf9-115">次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-115">They include:</span></span>

-   <span data-ttu-id="cacf9-116">ローカルのインストールからイベントをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="cacf9-116">Capture events from the local installation.</span></span>
    -   <span data-ttu-id="cacf9-117">**トレースの選択** ウィンドウが開いていない場合、**ファイル** メニューに移動し、**トレースを開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cacf9-117">If the **Select Trace** window isn’t already open, go to the **File** menu and click **Open trace**.</span></span> <span data-ttu-id="cacf9-118">**追跡の選択** ウィンドウで、**イベントのキャプチャ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cacf9-118">In the **Select Trace** window, click **Capture Events**.</span></span> <span data-ttu-id="cacf9-119">プロバイダーを選択して、**開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cacf9-119">After selecting your providers, click **Start**.</span></span> <span data-ttu-id="cacf9-120">Trace Parser ツールは、すべてのプロバイダーのリッスンとイベントのキャプチャを開始します。</span><span class="sxs-lookup"><span data-stu-id="cacf9-120">The Trace Parser tool will start listening to all the providers and capturing the events.</span></span> <span data-ttu-id="cacf9-121">**停止およびインポート** をクリックするとキャプチャは停止します。</span><span class="sxs-lookup"><span data-stu-id="cacf9-121">Capturing stops when you click **Stop and Import**.</span></span>
-   <span data-ttu-id="cacf9-122">Logman などのツールを使用してキャプチャされた、既存の ETL(Windows イベント) ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-122">Open an existing ETL (Windows Event) file that was captured using tools such as Logman.</span></span> 

    <span data-ttu-id="cacf9-123">[![開いている Windows イベントのファイルの例](./media/1_desktop.png)](./media/1_desktop.png)</span><span class="sxs-lookup"><span data-stu-id="cacf9-123">[![Example of opened Windows Event file](./media/1_desktop.png)](./media/1_desktop.png)</span></span>

## <a name="viewing-traces"></a><span data-ttu-id="cacf9-124">トレースの表示</span><span class="sxs-lookup"><span data-stu-id="cacf9-124">Viewing traces</span></span>
<span data-ttu-id="cacf9-125">**タイムライン ビュー** タイムライン タブは、Trace Parser にトレースをインポートした後に表示される最初のタブです。</span><span class="sxs-lookup"><span data-stu-id="cacf9-125">**Timeline view** The Timeline tab is the first tab that you see after you import a trace into the Trace Parser.</span></span> <span data-ttu-id="cacf9-126">このタブは、次の図に表示されます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-126">This tab is shown in the following illustration.</span></span> 

<span data-ttu-id="cacf9-127">[![[タイムライン] タブの情報の例](./media/2_desktop.png)](./media/2_desktop.png)</span><span class="sxs-lookup"><span data-stu-id="cacf9-127">[![Example of information in the Timeline tab](./media/2_desktop.png)](./media/2_desktop.png)</span></span> 

<span data-ttu-id="cacf9-128">**タイムライン** タブには、次の主要なコンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="cacf9-128">The **Timeline** tab has the following major components:</span></span>

-   <span data-ttu-id="cacf9-129">**グループ化を選択** ドロップダウンでは、さまざまなカテゴリ (顧客 ID、ユーザー名、セッション名など) に基づいてグループ化できます。[グループ化] には、イベントの最大および最小タイムスタンプ、イベントの合計数、グループ内の最下位イベント レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-129">The **Select Grouping** drop-down allows you to group based on a variety of categories, such as Customer ID, Username, Session Name, etc. Groupings will display maximum and minimum timestamp of events, total number of events, and lowest event level within the grouping.</span></span>
-   <span data-ttu-id="cacf9-130">スレッドまたはスレッドではないビューのすべてのイベントのリスト。</span><span class="sxs-lookup"><span data-stu-id="cacf9-130">List of all events in a threaded or unthreaded view.</span></span>
-   <span data-ttu-id="cacf9-131">選択したイベントに表示されるプロパティ グリッド。</span><span class="sxs-lookup"><span data-stu-id="cacf9-131">Property grid displayed for the selected event.</span></span>
-   <span data-ttu-id="cacf9-132">選択したすべてのイベントのタイムライン チャートです。</span><span class="sxs-lookup"><span data-stu-id="cacf9-132">Timeline chart for all the selected events.</span></span>
-   <span data-ttu-id="cacf9-133">イベントのフィルター処理。</span><span class="sxs-lookup"><span data-stu-id="cacf9-133">Filtering of events.</span></span>
-   <span data-ttu-id="cacf9-134">セッション分析メモ。</span><span class="sxs-lookup"><span data-stu-id="cacf9-134">Session analysis notes.</span></span>

<span data-ttu-id="cacf9-135">**呼び出しツリーの表示** **呼び出しツリー** タブを選択すると、すべての X++ メソッドの呼び出しツリーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-135">**Call tree view** By selecting the **Call Tree** tab, you can see the call tree for all X++ methods.</span></span> <span data-ttu-id="cacf9-136">タブは、次に示します。</span><span class="sxs-lookup"><span data-stu-id="cacf9-136">The tab is shown below.</span></span> 

<span data-ttu-id="cacf9-137">[呼び出しツリー タブに表示される情報の例](./media/3_desktop.png)](./media/3_desktop.png)</span><span class="sxs-lookup"><span data-stu-id="cacf9-137">[Example of information shown in the Call Tree tab](./media/3_desktop.png)](./media/3_desktop.png)</span></span> 

<span data-ttu-id="cacf9-138">デスクトップ同様に、**X++** タブを表示し、すべての X++ メソッドの一覧を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-138">Similarly, you can display the **X++** tab to view a list of all the X++ methods.</span></span> <span data-ttu-id="cacf9-139">包括的/排他的な期間、RPC、データベース呼び出しなどのフィールドでソートされます。</span><span class="sxs-lookup"><span data-stu-id="cacf9-139">They will be sorted by fields such as Inclusive/Exclusive durations, RPC, or Database calls.</span></span> <span data-ttu-id="cacf9-140">これらは Trace Parser の対応するタブに類似しており、同じ動作をすることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cacf9-140">Note that these are similar to the corresponding tabs in Trace Parser and have the same behavior.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cacf9-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cacf9-141">Additional resources</span></span>

[<span data-ttu-id="cacf9-142">開発およびカスタマイズのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="cacf9-142">Develop and customize home page</span></span>](../dev-tools/developer-home-page.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]