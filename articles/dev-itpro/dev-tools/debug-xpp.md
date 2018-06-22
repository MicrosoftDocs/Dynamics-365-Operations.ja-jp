---
title: "X++ コードのデバッグ"
description: "このトピックでは、Microsoft Visual Studio のデバッグ機能を使用して X++ コードをデバッグする方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 23921
ms.assetid: 6be739c0-30da-4f91-97be-a8764fb8078c
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f0a0e988b59a76fe3869b7789733b5e9061eb188
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="debug-x-code"></a><span data-ttu-id="4674b-103">X++ コードのデバッグ</span><span class="sxs-lookup"><span data-stu-id="4674b-103">Debug X++ code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4674b-104">このトピックでは、Microsoft Visual Studio のデバッグ機能を使用して X++ コードをデバッグする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4674b-104">This topic reviews how you can debug X++ code by using the debugging feature in Microsoft Visual Studio.</span></span> 

<span data-ttu-id="4674b-105">X++ コードをデバッグするには、Microsoft Visual Studio でデバッガを使用します。</span><span class="sxs-lookup"><span data-stu-id="4674b-105">To debug X++ code, you use the debugger in Microsoft Visual Studio.</span></span> <span data-ttu-id="4674b-106">このプロセスは、Visual Studio で作成される他のアプリケーションで使用されるプロセスに似ています。</span><span class="sxs-lookup"><span data-stu-id="4674b-106">The process is similar to the process that is used for any other application that is created in Visual Studio.</span></span> <span data-ttu-id="4674b-107">たとえば、コードがブレークポイントで停止するときに、アプリケーションを検証する標準のツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4674b-107">For example, the standard tools for examining the application are available when your code is stopped at a breakpoint.</span></span>

## <a name="debug-your-code"></a><span data-ttu-id="4674b-108">コードのデバッグ</span><span class="sxs-lookup"><span data-stu-id="4674b-108">Debug your code</span></span>
<span data-ttu-id="4674b-109">X++ コードをデバッグするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4674b-109">To debug X++ code, follow these steps.</span></span>

1. <span data-ttu-id="4674b-110">Visual Studio で、デバッグする X++ コードを開きます。</span><span class="sxs-lookup"><span data-stu-id="4674b-110">In Visual Studio, open the X++ code to debug.</span></span>
2. <span data-ttu-id="4674b-111">停止を実行する行または明細行を検索し、それらの明細行でブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="4674b-111">Find the line or lines where you want execution to stop, and set breakpoints in those lines.</span></span> <span data-ttu-id="4674b-112">行にブレークポイントを設定するには、コード エディターの左の列をクリックするか、カーソルがその行にある間に F9 を押します。</span><span class="sxs-lookup"><span data-stu-id="4674b-112">To set a breakpoint in a line, click in the left column of the code editor or press F9 while the cursor is on that line.</span></span> <span data-ttu-id="4674b-113">赤いドットは、ブレークポイントが設定されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="4674b-113">A red dot indicates that a breakpoint has been set.</span></span> 

   <span data-ttu-id="4674b-114">[![赤い丸](./media/32_DevoToolsConcept.png)](./media/32_DevoToolsConcept.png)</span><span class="sxs-lookup"><span data-stu-id="4674b-114">[![Red dot](./media/32_DevoToolsConcept.png)](./media/32_DevoToolsConcept.png)</span></span>

3. <span data-ttu-id="4674b-115">スタートアップ プロジェクトおよびスタートアップ オブジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="4674b-115">Set a startup project and a startup object.</span></span> <span data-ttu-id="4674b-116">スタートアップ オブジェクトは、任意のフォーム、**main** メソッドを持つ任意のクラス、または任意のメニュー項目にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4674b-116">Startup objects can be any form, any class that has the **main** method, or any menu item.</span></span> <span data-ttu-id="4674b-117">スタートアップ オブジェクトはプロジェクトの **プロパティ** ウィンドウで設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4674b-117">You can set the startup object in the **Properties** pane for the project.</span></span> <span data-ttu-id="4674b-118">または、ソリューション エクスプローラーで要素を右クリックし、その後**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4674b-118">Alternatively, right-click the element in Solution Explorer, and then click **Set as Startup Object**.</span></span>

   ![スタートアップ オブジェクトとして設定](./media/setasstartupobject.jpg)

4. <span data-ttu-id="4674b-120">**デバッグ**メニューで、**デバッグの開始**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4674b-120">On the **Debug** menu, click **Start Debugging**.</span></span>
5. <span data-ttu-id="4674b-121">アプリケーションで、目的のコードを実行させるアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="4674b-121">In the application, perform the action that causes the code that you're interested in to run.</span></span> <span data-ttu-id="4674b-122">標準的なアクションには、フォームを開くことが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4674b-122">Typical actions include opening a form.</span></span> <span data-ttu-id="4674b-123">処理は、設定したブレークポイントで停止します。</span><span class="sxs-lookup"><span data-stu-id="4674b-123">Processing stops at the breakpoints that you set.</span></span> 

   <span data-ttu-id="4674b-124">[![実行](./media/33_DevoToolsConcept.png)](./media/33_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="4674b-124">[![Run](./media/33_DevoToolsConcept.png)](./media/33_devotoolsconcept.png)</span></span>

6. <span data-ttu-id="4674b-125">Visual Studio のツールを使用して、アプリケーションを調べます。</span><span class="sxs-lookup"><span data-stu-id="4674b-125">Use the tools in Visual Studio to examine the application.</span></span> <span data-ttu-id="4674b-126">たとえば、その値を表示するため、X++ コード内の変数をポイントします。</span><span class="sxs-lookup"><span data-stu-id="4674b-126">For example, you can hover over variables in the X++ code to see their values.</span></span> <span data-ttu-id="4674b-127">また、**デバッグ** メニュー上のコマンドを使用してコードを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="4674b-127">You can also use commands on the **Debug** menu to step through the code.</span></span> <span data-ttu-id="4674b-128">また、Visual Studio の **Autos** ウィンドウのようなツールは、アプリケーションの状態に関する重要な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4674b-128">Additionally, tools such as the **Autos** pane in Visual Studio will show important information about the state of the application.</span></span> 

   <span data-ttu-id="4674b-129">[![ホバー](./media/34_DevoToolsConcept.png)](./media/34_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="4674b-129">[![Hover](./media/34_DevoToolsConcept.png)](./media/34_devotoolsconcept.png)</span></span>

   <span data-ttu-id="4674b-130">Finance and Operations に固有の、もう 1 つのツールは情報ログです。</span><span class="sxs-lookup"><span data-stu-id="4674b-130">Another tool that is specific to Finance and Operations is the Infolog.</span></span> <span data-ttu-id="4674b-131">多くの場合、**info()** ステートメントは、アプリケーションの実行中に、ログ ステータス メッセージのコードに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4674b-131">Often, **info()** statements are added to code to log status messages while the application is running.</span></span> <span data-ttu-id="4674b-132">これらの情報ログ メッセージは、Visual Studio で直接表示できます。</span><span class="sxs-lookup"><span data-stu-id="4674b-132">You can view these Infolog messages directly in Visual Studio.</span></span> <span data-ttu-id="4674b-133">**表示**メニューで、**情報ログ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4674b-133">On the **View** menu, click **Infolog**.</span></span> 

   <span data-ttu-id="4674b-134">[![情報ログ](./media/35_DevoToolsConcept.png)](./media/35_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="4674b-134">[![Infolog](./media/35_DevoToolsConcept.png)](./media/35_devotoolsconcept.png)</span></span>

7. <span data-ttu-id="4674b-135">アプリケーションのデバッグが終了した後、Finance and Operations を終了します。</span><span class="sxs-lookup"><span data-stu-id="4674b-135">After you've finished debugging the application, exit Finance and Operations .</span></span> <span data-ttu-id="4674b-136">Visual Studio はデバッグ モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="4674b-136">Visual Studio will exit debugging mode.</span></span>


<a name="additional-resources"></a><span data-ttu-id="4674b-137">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="4674b-137">Additional resources</span></span>
--------

[<span data-ttu-id="4674b-138">開発者ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="4674b-138">Developer home page</span></span>](developer-home-page.md)





