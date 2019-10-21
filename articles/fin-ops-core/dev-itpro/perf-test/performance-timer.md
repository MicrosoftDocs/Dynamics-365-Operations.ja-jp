---
title: パフォーマンス タイマー
description: このトピックでは、パフォーマンス タイマーの概要を示します。このタイマーは、システムのパフォーマンスが低下する原因を特定するのに役立つツールです。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 27191
ms.assetid: 64b8f266-a9e1-48ee-93c7-e082f21ddfa7
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0274a5b984b4f56dc436fbc70c230acf7ab0a01
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183092"
---
# <a name="performance-timer"></a><span data-ttu-id="8f485-103">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="8f485-103">Performance timer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f485-104">このトピックでは、パフォーマンス タイマーの概要を示します。このタイマーは、システムのパフォーマンスが低下する原因を特定するのに役立つツールです。</span><span class="sxs-lookup"><span data-stu-id="8f485-104">This topic provides an overview of the Performance timer, which is a tool that helps you to determine why your system's performance might be slow.</span></span> 

<span data-ttu-id="8f485-105">パフォーマンス タイマーを開くには、追加パラメータ debug=develop: https://<em>yoursite</em>.cloud.test.dynamics.com/en/?cmp=USMF&debug=develop を使用して Web ページを開きます。**注:** デバッグ モードで実行すると、パフォーマンスが低下することがわかります。</span><span class="sxs-lookup"><span data-stu-id="8f485-105">To open the Performance timer, open your webpage with the added parameter debug=develop: https://<em>yoursite</em>.cloud.test.dynamics.com/en/?cmp=USMF&debug=develop \*\*Note: \*\*When you run in debug mode you will notice slower performance.</span></span> <span data-ttu-id="8f485-106">F12 キーを押して、ブラウザーで使用可能なデバッグ ツールを使用し、パフォーマンスの大半の問題の概要を素早く取得することができます。</span><span class="sxs-lookup"><span data-stu-id="8f485-106">You can quickly get an overview of most performance issues by pressing F12 and working with the debugging tools that are available in your browser.</span></span> <span data-ttu-id="8f485-107">タイマーはここで表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f485-107">The timer will show up here.</span></span> 

<span data-ttu-id="8f485-108">[![タイマー](./media/timer.png)](./media/timer.png)</span><span class="sxs-lookup"><span data-stu-id="8f485-108">[![timer](./media/timer.png)](./media/timer.png)</span></span> 

<span data-ttu-id="8f485-109">発注書一覧ページなどの一覧ページを開くには、[パフォーマンス タイマー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f485-109">To open a list page, for example, such as the purchase order list page, click the Performance timer.</span></span> <span data-ttu-id="8f485-110">次のスクリーン ショットは、クライアント時間とサーバー時間の区切り、および合計時間を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f485-110">The following screenshot shows the separation between client time and server time, and the total time.</span></span> <span data-ttu-id="8f485-111">また、一連のパフォーマンス カウンターと高価なサーバー呼び出しを確認できます。</span><span class="sxs-lookup"><span data-stu-id="8f485-111">Additionally, you can see a set of performance counters and expensive server calls.</span></span> 

<span data-ttu-id="8f485-112">[![2\_タイマー](./media/2_timer.png)](./media/2_timer.png)</span><span class="sxs-lookup"><span data-stu-id="8f485-112">[![2\_Timer](./media/2_timer.png)](./media/2_timer.png)</span></span> 

<span data-ttu-id="8f485-113">サーバー パフォーマンス カウンターの詳細については、リンクのいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f485-113">For more information about the server performance counters, click on any of the links.</span></span>

-   <span data-ttu-id="8f485-114">**フォーム** - フォームには、現在開いているフォームの数と、それらが開いたり閉じられたりした割合 (秒ごと) と、作成されたフォームまたは閉じられたフォームの合計数などの一連のカウンターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f485-114">**Forms** - Forms will show how many forms are currently open, plus the rate at which they opened and closed (per second), and a set of counters, such as the total amount of created or closed forms.</span></span>
-   <span data-ttu-id="8f485-115">**GC** - これは、サーバー上のガベージ コレクション プロセスに関する情報です。</span><span class="sxs-lookup"><span data-stu-id="8f485-115">**GC** - This is information about the garbage collection processes on the server.</span></span>
-   <span data-ttu-id="8f485-116">**Web クライアント セッション** - これは、現在持っている Web クライアント セッションの数と使用中の Web クライアント セッションの数を示します。</span><span class="sxs-lookup"><span data-stu-id="8f485-116">**Web client session** - This shows how many web client sessions you currently have and how many are in use.</span></span>
-   <span data-ttu-id="8f485-117">**サービス セッション プロバイダー** - これは、作成したセッションの合計数です。</span><span class="sxs-lookup"><span data-stu-id="8f485-117">**Services Session provider** - This is the total number of sessions created.</span></span>

<span data-ttu-id="8f485-118">詳細については、リンクをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="8f485-118">For more information, click a link.</span></span> <span data-ttu-id="8f485-119">次の画面で、個別の呼び出しによってトリガーされた SQL クエリの数、および価値が高い SQL クエリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8f485-119">In the next screen, you can see how many SQL queries were triggered by this individual call and which SQL query was the most expensive.</span></span> 

<span data-ttu-id="8f485-120">[![3\_タイマー](./media/3_timer.png)](./media/3_timer.png)</span><span class="sxs-lookup"><span data-stu-id="8f485-120">[![3\_Timer](./media/3_timer.png)](./media/3_timer.png)</span></span> 

<span data-ttu-id="8f485-121">この情報は、トレースする内容とトラブルシューティングの開始場所の理解に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8f485-121">This information can help you to understand what to trace and where to start troubleshooting.</span></span> 

<!--In addition to this topic, you can watch this video for more information: [PERF The Performance Timer and Other Tools](https://mix.office.com/watch/ij5cqidra5q3)-->



