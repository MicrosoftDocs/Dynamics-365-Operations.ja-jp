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
ms.openlocfilehash: b6df3d7d53403feafe69ee32140de230ea5c9718
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893385"
---
# <a name="performance-timer"></a><span data-ttu-id="e1b80-103">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="e1b80-103">Performance timer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1b80-104">このトピックでは、パフォーマンス タイマーの概要を示します。このタイマーは、システムのパフォーマンスが低下する原因を特定するのに役立つツールです。</span><span class="sxs-lookup"><span data-stu-id="e1b80-104">This topic provides an overview of the Performance timer, which is a tool that helps you to determine why your system's performance might be slow.</span></span> 

<span data-ttu-id="e1b80-105">パフォーマンス タイマーを開くには、追加パラメーター debug=develop: https://<em>yoursite</em>.cloud.test.dynamics.com/en/?cmp=USMF&debug=develop を使用して Web ページを開きます。注: デバッグ モードで実行すると、パフォーマンスが低下することがわかります。</span><span class="sxs-lookup"><span data-stu-id="e1b80-105">To open the Performance timer, open your webpage with the added parameter debug=develop: https://<em>yoursite</em>.cloud.test.dynamics.com/en/?cmp=USMF&debug=develop Note: When you run in debug mode you will notice slower performance.</span></span> <span data-ttu-id="e1b80-106">F12 キーを押して、ブラウザーで使用可能なデバッグ ツールを使用し、パフォーマンスの大半の問題の概要を素早く取得することができます。</span><span class="sxs-lookup"><span data-stu-id="e1b80-106">You can quickly get an overview of most performance issues by pressing F12 and working with the debugging tools that are available in your browser.</span></span> <span data-ttu-id="e1b80-107">タイマーはここで表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1b80-107">The timer will show up here.</span></span> 

<span data-ttu-id="e1b80-108">[![画面上部に配置されたタイマーの例](./media/timer.png)](./media/timer.png)</span><span class="sxs-lookup"><span data-stu-id="e1b80-108">[![Example of timer located at top of screen](./media/timer.png)](./media/timer.png)</span></span> 

<span data-ttu-id="e1b80-109">発注書一覧ページなどの一覧ページを開くには、[パフォーマンス タイマー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1b80-109">To open a list page, for example, such as the purchase order list page, click the Performance timer.</span></span> <span data-ttu-id="e1b80-110">次のスクリーン ショットは、クライアント時間とサーバー時間の区切り、および合計時間を示しています。</span><span class="sxs-lookup"><span data-stu-id="e1b80-110">The following screenshot shows the separation between client time and server time, and the total time.</span></span> <span data-ttu-id="e1b80-111">また、一連のパフォーマンス カウンターと高価なサーバー呼び出しを確認できます。</span><span class="sxs-lookup"><span data-stu-id="e1b80-111">Additionally, you can see a set of performance counters and expensive server calls.</span></span> 

<span data-ttu-id="e1b80-112">[![サーバー パフォーマンス カウンターを示すスクリーン ショット](./media/2_timer.png)](./media/2_timer.png)</span><span class="sxs-lookup"><span data-stu-id="e1b80-112">[![Screen shot showing server performance counters](./media/2_timer.png)](./media/2_timer.png)</span></span> 

<span data-ttu-id="e1b80-113">サーバー パフォーマンス カウンターの詳細については、リンクのいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1b80-113">For more information about the server performance counters, click on any of the links.</span></span>

-   <span data-ttu-id="e1b80-114">**フォーム** - フォームには、現在開いているフォームの数と、それらが開いたり閉じられたりした割合 (秒ごと) と、作成されたフォームまたは閉じられたフォームの合計数などの一連のカウンターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1b80-114">**Forms** - Forms will show how many forms are currently open, plus the rate at which they opened and closed (per second), and a set of counters, such as the total amount of created or closed forms.</span></span>
-   <span data-ttu-id="e1b80-115">**GC** - これは、サーバー上のガベージ コレクション プロセスに関する情報です。</span><span class="sxs-lookup"><span data-stu-id="e1b80-115">**GC** - This is information about the garbage collection processes on the server.</span></span>
-   <span data-ttu-id="e1b80-116">**Web クライアント セッション** - これは、現在持っている Web クライアント セッションの数と使用中の Web クライアント セッションの数を示します。</span><span class="sxs-lookup"><span data-stu-id="e1b80-116">**Web client session** - This shows how many web client sessions you currently have and how many are in use.</span></span>
-   <span data-ttu-id="e1b80-117">**サービス セッション プロバイダー** - これは、作成したセッションの合計数です。</span><span class="sxs-lookup"><span data-stu-id="e1b80-117">**Services Session provider** - This is the total number of sessions created.</span></span>

<span data-ttu-id="e1b80-118">詳細については、リンクをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="e1b80-118">For more information, click a link.</span></span> <span data-ttu-id="e1b80-119">次の画面で、個別の呼び出しによってトリガーされた SQL クエリの数、および価値が高い SQL クエリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e1b80-119">In the next screen, you can see how many SQL queries were triggered by this individual call and which SQL query was the most expensive.</span></span> 

<span data-ttu-id="e1b80-120">[![呼び出しによってトリガーされた SQL クエリのリストの例](./media/3_timer.png)](./media/3_timer.png)</span><span class="sxs-lookup"><span data-stu-id="e1b80-120">[![Example of list of SQL queries triggered by call](./media/3_timer.png)](./media/3_timer.png)</span></span> 

<span data-ttu-id="e1b80-121">この情報は、トレースする内容とトラブルシューティングの開始場所の理解に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e1b80-121">This information can help you to understand what to trace and where to start troubleshooting.</span></span> 
