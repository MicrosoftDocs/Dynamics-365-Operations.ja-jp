---
title: "[新しいウィンドウで開く] アイコンを使用してページを並べて表示します"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations でページを並べて表示する方法を説明します。"
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f19ca5e9642b5a8222ee7bf23fdd228ab75d2ed1
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a><span data-ttu-id="fbdd8-103">[新しいウィンドウで開く] アイコンを使用してページを並べて表示する</span><span class="sxs-lookup"><span data-stu-id="fbdd8-103">Display pages side-by-side using the Open in New Window icon</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fbdd8-104">この記事は、Microsoft Dynamics 365 for Finance and Operations でページを並べて表示する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-104">This article explains how to display pages side-by-side in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="fbdd8-105">Microsoft Dynamics 365 for Finance and Operations により、効率的にタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-105">Microsoft Dynamics 365 for Finance and Operations helps you perform tasks efficiently.</span></span> <span data-ttu-id="fbdd8-106">場合によっては、タスクをすばやく完了するために複数ページを並べて表示することができます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-106">In some cases, you may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="fbdd8-107">たとえば、複数の仕訳帳で明細行を検証または入力することができます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-107">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="fbdd8-108">通常、そのためには、仕訳帳の一覧が表示されたページや特定の仕訳帳の明細行が表示されたページの間を行き来する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-108">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="fbdd8-109">ただし、[新しいウィンドウで開く] 機能は、タスクをすばやく実行できるように、これらのページを並べて表示できます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-109">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span> 

<span data-ttu-id="fbdd8-110">引き続き上記の例で考えてみると、明細行を表示した場合には、[新しいウィンドウで開く] アイコンをクリックできます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-110">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span> 

<span data-ttu-id="fbdd8-111">[![新しいウィンドウで開くアイコン](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="fbdd8-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span> 

<span data-ttu-id="fbdd8-112">[新しいウィンドウで開く] アイコンをクリックすると新しいポップアップ ブラウザーに明細行ページが開き、元のブラウザーは履歴をさかのぼり仕訳帳の一覧が表示されたページに移動します。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-112">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="fbdd8-113">その後、両方のページを並べて表示できます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-113">You can then display both pages side-by-side.</span></span> <span data-ttu-id="fbdd8-114">仕訳帳の表示が終了すると、仕訳帳リスト ページで選択された仕訳帳を変更できます。また、ポップアップ ウィンドウの明細行ページには、新しく選択された仕訳帳の明細行が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-114">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span> 

<span data-ttu-id="fbdd8-115">[![ページを並べて表示する](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="fbdd8-115">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span> 

<span data-ttu-id="fbdd8-116">これらのページをバッキングしているデータ間に存在する関係により、動的リンクと動的更新が発生します。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-116">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="fbdd8-117">システムがデータ間の関係を認識しない場合、ポップアップ ウィンドウはそれが生成されたウィンドウでの変更に対して自動的に更新されません。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-117">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span> 

<span data-ttu-id="fbdd8-118">一部のページには、グリッド ビュー、ヘッダー ビュー、詳細ビューなどの複数のビューがあります。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-118">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="fbdd8-119">[新しいウィンドウで開く] アイコンにより、ページ全体を新しいブラウザー ウィンドウで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-119">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="fbdd8-120">したがって、[新しいウィンドウで開く] 機能では、同じページの 2 つのビューを並べて表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-120">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="fbdd8-121">ただし、このようなページのほとんどすべてには、レコードの切り替えや同様の操作を達成するために使用できるナビゲーション リストがあります。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-121">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span> 

<span data-ttu-id="fbdd8-122">[新しいウィンドウで開く] 機能を使用する前に、ブラウザーのポップアップ ブロッカーをコンフィギュレーションして、Dynamics 365 for Finance and Operations サイトの URL からのポップアップを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-122">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the Finance and Operations site.</span></span> <span data-ttu-id="fbdd8-123">たとえば、「\*.dynamics.com」からのポップアップを許可することができます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-123">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span> 

<span data-ttu-id="fbdd8-124">[新しいウィンドウで開く] 機能は、ウィンドウで 1 つ以上のページが開いている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-124">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="fbdd8-125">また、ポップアップ ウィンドウは、開いているページがなくなると (つまり、そのウィンドウで最後のページが閉じると) 自動的に閉じます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-125">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="fbdd8-126">アプリケーションの別の領域に移動すると、Finance and Operations も開いているページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-126">Finance and Operations also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="fbdd8-127">したがって、ポップアップ ウィンドウが開いているときに、アプリケーションで別の領域に移動すると、システムがそれらのウィンドウ内のページを閉じるので、ポップアップ ウィンドウは自動的に閉じます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-127">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span> 

<span data-ttu-id="fbdd8-128">ポップアップ ウィンドウの上部バーは読み取り専用で、その中にページが開かれ、会社に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-128">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="fbdd8-129">また、ポップアップ ウィンドウは、メインの Finance and Operations ブラウザー ウィンドウに依存します。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-129">The pop-up windows also rely on the main Finance and Operations browser window.</span></span> <span data-ttu-id="fbdd8-130">メイン ウィンドウが閉じるか、または更新されると、開いているすべてのポップアップ ウィンドウは、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-130">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="fbdd8-131">これは、これらのウィンドウに情報を表示することはできますが、その情報とやり取りができないことを示します。</span><span class="sxs-lookup"><span data-stu-id="fbdd8-131">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>




