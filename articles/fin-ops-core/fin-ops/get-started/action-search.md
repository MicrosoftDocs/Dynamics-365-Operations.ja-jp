---
title: アクション検索
description: この記事では、アクション検索機能について説明します。 アクション検索でページのアクションを検索して実行できます。
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d01247aa356625cb759306e5ead2afd3cdeb840f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191319"
---
# <a name="action-search"></a><span data-ttu-id="37f44-104">アクション検索</span><span class="sxs-lookup"><span data-stu-id="37f44-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37f44-105">この記事では、アクション検索機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="37f44-105">This article describes the action search functionality.</span></span> <span data-ttu-id="37f44-106">アクション検索でページのアクションを検索して実行できます。</span><span class="sxs-lookup"><span data-stu-id="37f44-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="37f44-107">はじめに</span><span class="sxs-lookup"><span data-stu-id="37f44-107">Introduction</span></span>

<span data-ttu-id="37f44-108">ページでは、ページの上部に表示される標準アクション ウィンドウおよびページのさまざまなセクションに表示されるツール バーの両方のアクション ウィンドウでコマンドが主として公開されます。</span><span class="sxs-lookup"><span data-stu-id="37f44-108">Pages primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="37f44-109">以前のバージョンでは、キー ヒント機能は、Alt キーおよび一連の文字を押して、アクション ウィンドウのボタンをすばやくアクセスできました。</span><span class="sxs-lookup"><span data-stu-id="37f44-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="37f44-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="37f44-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="37f44-111">キー ヒントは使用できなくなりますが、アクション検索機能によって置き換えられています。</span><span class="sxs-lookup"><span data-stu-id="37f44-111">Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="37f44-112">この新しい機能ですぐに検索でき、表示されているどのアクション ウィンドウのボタンからも実行できます。</span><span class="sxs-lookup"><span data-stu-id="37f44-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="37f44-113">アクション検索の使用</span><span class="sxs-lookup"><span data-stu-id="37f44-113">Using action search</span></span>

<span data-ttu-id="37f44-114">アクション検索機能を使用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="37f44-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="37f44-115">アクション ウィンドウで、**アクション検索**フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="37f44-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="37f44-116">(**アクション検索**フィールドには、虫眼鏡アイコンが含まれます)。</span><span class="sxs-lookup"><span data-stu-id="37f44-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="37f44-117">自分が実行するボタンの名前の全体または一部を入力します。</span><span class="sxs-lookup"><span data-stu-id="37f44-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="37f44-118">ボタンの「パス」の単語を使用しても検索できます。</span><span class="sxs-lookup"><span data-stu-id="37f44-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="37f44-119">(詳細については、この記事の次のセクションを参照してください)。通常、2 から 4 文字を入力するとボタンが結果一覧の先頭の近くに表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f44-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="37f44-120">検索して、結果リストのボタンを実行します (マウスまたはキーボードを使用して)。</span><span class="sxs-lookup"><span data-stu-id="37f44-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="37f44-121">ボタンの実行後、作業し続けることができるように、フォーカスはページの最後の位置に戻されます。</span><span class="sxs-lookup"><span data-stu-id="37f44-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="37f44-122">[![アクション検索フィールド](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="37f44-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="37f44-123">Ctrl + /、または Alt + Q を押しても、アクション検索を開始できます。</span><span class="sxs-lookup"><span data-stu-id="37f44-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="37f44-124">ページの最後の位置にフォーカスを返すには、キーボード ショートカットを再度押します。</span><span class="sxs-lookup"><span data-stu-id="37f44-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="37f44-125">結果一覧の理解</span><span class="sxs-lookup"><span data-stu-id="37f44-125">Understanding the results list</span></span>

<span data-ttu-id="37f44-126">多くの場合、ボタンの目的を完全に理解するためには、ボタンの場所とコンテキストの両方を把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f44-126">Often, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="37f44-127">したがって、リストに表示されるボタンを完全に理解するために、結果一覧の各項目に追加情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f44-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="37f44-128">特に、ボタンの「パス」が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f44-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="37f44-129">このパスは、必要に応じて、次の UI 要素のラベルを含む場合があります:</span><span class="sxs-lookup"><span data-stu-id="37f44-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="37f44-130">アクション ウィンドウ タブ</span><span class="sxs-lookup"><span data-stu-id="37f44-130">Action Pane tab</span></span>
- <span data-ttu-id="37f44-131">ボタン グループ</span><span class="sxs-lookup"><span data-stu-id="37f44-131">Button group</span></span>
- <span data-ttu-id="37f44-132">メニュー ボタン (ボタンがメニュー ボタンの中にある場合)</span><span class="sxs-lookup"><span data-stu-id="37f44-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="37f44-133">メニュー区切り (ボタンがメニュー ボタンの中の名前を付けられたグループの中にある場合)</span><span class="sxs-lookup"><span data-stu-id="37f44-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="37f44-134">ページのグループあるいはタブ (たとえば、クイック タブの名前)</span><span class="sxs-lookup"><span data-stu-id="37f44-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="37f44-135">たとえば、**tot**と**アクション検索**フィールドに入力し、現在結果一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="37f44-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="37f44-136">最初の入力で、**合計**と名付けられるボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f44-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="37f44-137">**販売注文** &gt; **ビュー**のボタンのパスも表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f44-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="37f44-138">**販売注文**の部分は、アクション ウィンドウの**販売注文**タブに対応し、**ビュー**の部分は、そのタブの**ビュー**グループに対応します。同様に、**割引合計**ボタン (**販売** &gt; **計算**) は、このボタンがアクション ウィンドウの**販売**タブの**計算**グループに位置することを示します。</span><span class="sxs-lookup"><span data-stu-id="37f44-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="37f44-139">したがって、この情報はどのボタンがアクション検索にトリガされたかを理解するのに役立ちます (結果一覧でそのボタンを選択した場合)。</span><span class="sxs-lookup"><span data-stu-id="37f44-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="37f44-140">[![データ付アクション検索フィールド](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="37f44-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="37f44-141">前の例では、アクション検索はページ上部の標準アクション ウィンドウから結果を表示しました。</span><span class="sxs-lookup"><span data-stu-id="37f44-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="37f44-142">ただし、アクション検索は、ページの他の領域に表示されるツール バーの結果も表示します。</span><span class="sxs-lookup"><span data-stu-id="37f44-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="37f44-143">たとえば、**販売注文明細行**クイック タブに位置する**手持在庫**ボタンを検索しているとします。</span><span class="sxs-lookup"><span data-stu-id="37f44-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="37f44-144">この場合、結果一覧のボタンのパス (**販売注文明細行** &gt; **在庫** &gt; **ビュー**) はそのボタンが**販売注文明細行**クイック タブの、**在庫**メニュー ボタンの、**ビュー**ヘッダーに位置することを示します。</span><span class="sxs-lookup"><span data-stu-id="37f44-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="37f44-145">[![手持在庫](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="37f44-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="37f44-146">アクション検索対ナビゲーション検索</span><span class="sxs-lookup"><span data-stu-id="37f44-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="37f44-147">アクション検索がページで検索し実行するアクションであるのに対し、複数のページを検索し移動する別の検索メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="37f44-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages.</span></span> <span data-ttu-id="37f44-148">この機能の詳細については、「[ナビゲーション検索](navigation-search.md)」の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37f44-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>
