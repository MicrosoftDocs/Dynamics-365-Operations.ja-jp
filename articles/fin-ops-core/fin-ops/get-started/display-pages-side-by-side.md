---
title: '[新しいウィンドウで開く] 機能を使用してページを並べて表示する'
description: この記事では、ページを並べて表示する方法を説明します。
author: aneesmsft
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ba583c2c9bcaaf106af75f8ac41f79bebc2c363
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748396"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a><span data-ttu-id="53efe-103">[新しいウィンドウで開く] 機能を使用してページを並べて表示する</span><span class="sxs-lookup"><span data-stu-id="53efe-103">Show pages side-by-side using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53efe-104">この記事では、ページを並べて表示する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="53efe-104">This article explains how to display pages side by side.</span></span>

<span data-ttu-id="53efe-105">タスクをすばやく完了するために複数ページを並べて表示することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="53efe-105">You may want to view multiple pages side by side to complete tasks quickly.</span></span> <span data-ttu-id="53efe-106">たとえば、複数の仕訳帳で明細行を検証または入力することができます。</span><span class="sxs-lookup"><span data-stu-id="53efe-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="53efe-107">通常、複数の仕訳の行を検証したり入力したりするには、仕訳の一覧を表示するページと、特定の仕訳の行を表示するページを行き来する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53efe-107">Typically, to validate or enter lines in more than one journal, you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="53efe-108">ただし、**新しいウィンドウで開く** 機能は、タスクをすばやく実行できるように、これらのページを並べて表示できます。</span><span class="sxs-lookup"><span data-stu-id="53efe-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="53efe-109">引き続き上記の例で考えてみると、明細行を表示した場合には、**新しいウィンドウで開く** アイコンをクリックできます。</span><span class="sxs-lookup"><span data-stu-id="53efe-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="53efe-110">[![新しいウィンドウで開くをクリックする](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="53efe-110">[![Click the Open in new window icon.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="53efe-111">**新しいウィンドウで開く** アイコンをクリックすると新しいポップアップ ブラウザーに明細行ページが開き、元のブラウザーは履歴をさかのぼり仕訳帳の一覧が表示されたページに移動します。</span><span class="sxs-lookup"><span data-stu-id="53efe-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="53efe-112">その後、両方のページを並べて表示できます。</span><span class="sxs-lookup"><span data-stu-id="53efe-112">You can then display both pages side by side.</span></span> <span data-ttu-id="53efe-113">仕訳帳の表示後、仕訳帳リスト ページで選択された仕訳帳を変更できます。また、ポップアップ ウィンドウの明細行ページには、新しく選択された仕訳帳の明細行が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="53efe-113">After viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="53efe-114">[![両方のページを並べて表示できます。](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="53efe-114">[![You can display pages side-by-side.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="53efe-115">これらのページをバッキングしているデータ間に存在する関係により、動的リンクと動的更新が発生します。</span><span class="sxs-lookup"><span data-stu-id="53efe-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="53efe-116">システムがデータ間の関係を認識しない場合、ポップアップ ウィンドウはそれが生成されたウィンドウでの変更に対して自動的に更新されません。</span><span class="sxs-lookup"><span data-stu-id="53efe-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="53efe-117">一部のページには、グリッド ビュー、ヘッダー ビュー、詳細ビューなどの複数のビューがあります。</span><span class="sxs-lookup"><span data-stu-id="53efe-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="53efe-118">**新しいウィンドウで開く** アイコンにより、ページ全体を新しいブラウザー ウィンドウで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="53efe-118">The **Open in new window** icon causes the entire page to open in the new browser window.</span></span> <span data-ttu-id="53efe-119">したがって、**新しいウィンドウで開く** 機能では、同じページの 2 つのビューを並べて表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="53efe-119">Therefore, you cannot keep two views of the same page side by side using the **Open in new window** feature.</span></span> <span data-ttu-id="53efe-120">このようなページのほとんどすべてには、レコードの切り替えや同様の操作を達成するために使用できるナビゲーション リストがあります。</span><span class="sxs-lookup"><span data-stu-id="53efe-120">Almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="53efe-121">**新しいウィンドウで開く** 機能を使用する前に、ブラウザーのポップアップ ブロッカーを設定して、サイトの URL からポップアップを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53efe-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="53efe-122">たとえば、「\*.dynamics.com」からのポップアップを許可することができます。</span><span class="sxs-lookup"><span data-stu-id="53efe-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="53efe-123">**新しいウィンドウで開く** 機能は、ウィンドウで 1 つ以上のページが開いている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="53efe-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="53efe-124">また、ポップアップ ウィンドウは、開いているページがなくなると (つまり、そのウィンドウで最後のページが閉じると) 自動的に閉じます。</span><span class="sxs-lookup"><span data-stu-id="53efe-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when you close the last page in that window).</span></span> <span data-ttu-id="53efe-125">アプリケーションの別の領域に移動すると、システムも開いているページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53efe-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="53efe-126">したがって、ポップアップ ウィンドウを開いてアプリケーションの別の領域に移動すると、システムがそれらのウィンドウ内のページを閉じるので、ポップアップ ウィンドウは自動的に閉じます。</span><span class="sxs-lookup"><span data-stu-id="53efe-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows close automatically because the system closed the pages in those windows.</span></span>

<span data-ttu-id="53efe-127">ポップアップ ウィンドウの上部バーは読み取り専用で、その中にページが開かれ、会社に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="53efe-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="53efe-128">また、ポップアップ ウィンドウは、メインのブラウザー ウィンドウに依存します。</span><span class="sxs-lookup"><span data-stu-id="53efe-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="53efe-129">メイン ウィンドウが閉じるか、または更新されると、開いているすべてのポップアップ ウィンドウは、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="53efe-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="53efe-130">これが発生する場合、これらのウィンドウに情報を表示することはできますが、その情報を使用した作業が行えないことを示します。</span><span class="sxs-lookup"><span data-stu-id="53efe-130">If this situation occurs, you can still view the information in these windows, but you will not be able to interact with it.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]