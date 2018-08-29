---
title: "コードの移行 - コンテキスト メニュー コード"
description: "新しいプログラミング モデルには、コンテキスト メニュー (ショートカット メニュー) が必要です。 この記事では、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations へのコンテキスト メニュー コードのマイグレーション プロセスについて説明します。 また、コンテキスト メニューの UX ガイドラインも含まれます。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 16301
ms.assetid: 8f3b62f2-4de6-4ea3-b3e6-1101d0fe308e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 52be3047cdd20ca7f17d9d980164c1a43bf0d2f8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="code-migration---context-menu-code"></a><span data-ttu-id="d131c-105">コードの移行 - コンテキスト メニュー コード</span><span class="sxs-lookup"><span data-stu-id="d131c-105">Code migration - Context menu code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d131c-106">新しいプログラミング モデルには、コンテキスト メニュー (ショートカット メニュー) が必要です。</span><span class="sxs-lookup"><span data-stu-id="d131c-106">A new programming model is required for context menus (shortcut menus).</span></span> <span data-ttu-id="d131c-107">この記事では、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations へのコンテキスト メニュー コードのマイグレーション プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d131c-107">This article outlines the process for migrating context menu code from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d131c-108">また、コンテキスト メニューの UX ガイドラインも含まれます。</span><span class="sxs-lookup"><span data-stu-id="d131c-108">It also includes UX guidelines for context menus.</span></span>

<span data-ttu-id="d131c-109">Microsoft Dynamics AX 2012 以前のバージョンでは、開発者が **PopupMenu** クラスを使用して右クリックのコンテキスト メニュー (ショートカット メニュー) を変更していました。</span><span class="sxs-lookup"><span data-stu-id="d131c-109">In Microsoft Dynamics AX 2012 and earlier versions, developers modified right-click context menus (shortcut menus) by using the **PopupMenu** class.</span></span> <span data-ttu-id="d131c-110">このクラスは、Web 上で利用できない Microsoft Windows アプリケーション プログラミング インターフェイス (API) に依存していました。</span><span class="sxs-lookup"><span data-stu-id="d131c-110">This class relied on Microsoft Windows application programming interfaces (APIs) that aren't available on the web.</span></span> <span data-ttu-id="d131c-111">Finance and Operations では、同様の機能を提供する代わりに **ContextMenu** API が作成されました。</span><span class="sxs-lookup"><span data-stu-id="d131c-111">In Finance and Operations, the **ContextMenu** APIs have been created as replacements to provide similar functionality.</span></span> <span data-ttu-id="d131c-112">以前は、**context()** メソッドと **showContextMenu()** メソッドのオーバーライドは、特定のコントロールのコンテキスト メニューを変更するためのエントリ ポイントでした。</span><span class="sxs-lookup"><span data-stu-id="d131c-112">Previously, the **context()** and **showContextMenu()** method overrides were the entry points for modifying context menus for specific controls.</span></span> <span data-ttu-id="d131c-113">これらの上書きには通常、コンテキスト メニューにオプションを追加したり、ユーザーの選択を処理するためのコードが含まれていました。</span><span class="sxs-lookup"><span data-stu-id="d131c-113">These overrides typically contained code to add options to the context menu, and also to process the user’s selection.</span></span> <span data-ttu-id="d131c-114">ユーザーの選択を処理するコードは、待機モデルを使用していました。</span><span class="sxs-lookup"><span data-stu-id="d131c-114">The code for processing the user's selection used a wait model.</span></span> <span data-ttu-id="d131c-115">Finance and Operations では、これらのオーバーライドが削除され、待機モデルは消去されています。</span><span class="sxs-lookup"><span data-stu-id="d131c-115">In Finance and Operations, these overrides are being removed, and the wait model is being eliminated.</span></span> <span data-ttu-id="d131c-116">代わりに、開発者はオプションにコンテキスト メニューを追加する **getContextMenuOptions()** およびユーザーの選択を処理する **selectedMenuOption()** の 2 つのオーバーライドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d131c-116">Instead, developers must create two overrides: **getContextMenuOptions()** to add options to the context menu and **selectedMenuOption()** to process the user’s selection.</span></span>

## <a name="migrate-context-menu-code-in-finance-and-operations"></a><span data-ttu-id="d131c-117">Finance and Operations でのコンテキスト メニュー コードの移行</span><span class="sxs-lookup"><span data-stu-id="d131c-117">Migrate context menu code in Finance and Operations</span></span>
<span data-ttu-id="d131c-118">**PopupMenu** API から **ContextMenu** API への移行は、3 つの主な段階に分けることができます。</span><span class="sxs-lookup"><span data-stu-id="d131c-118">Migration from the **PopupMenu** APIs to the **ContextMenu** APIs can be broken down into three main steps.</span></span>

### <a name="step-1-add-a-constant-for-each-menu-option-that-must-be-added"></a><span data-ttu-id="d131c-119">手順 1</span><span class="sxs-lookup"><span data-stu-id="d131c-119">Step 1.</span></span> <span data-ttu-id="d131c-120">追加する必要のあるメニュー オプションごとの定数の追加</span><span class="sxs-lookup"><span data-stu-id="d131c-120">Add a constant for each menu option that must be added</span></span>

<span data-ttu-id="d131c-121">**PopupMenu** クラスの古い **insertItem()** メソッドは、追加されたメニュー オプションの識別子を返しました。</span><span class="sxs-lookup"><span data-stu-id="d131c-121">The old **insertItem()** method in the **PopupMenu** class returned an identifier for the menu option that was being added.</span></span> <span data-ttu-id="d131c-122">この識別子は、将来の参照のために変数に保存されました。</span><span class="sxs-lookup"><span data-stu-id="d131c-122">This identifier was saved into a variable for future reference.</span></span> <span data-ttu-id="d131c-123">開発者は Finance and Operations でメニュー識別子を定義するため、各オプションの定数を定義してコードの可読性を高めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d131c-123">Because developers will define the menu identifier for themselves in Finance and Operations, it's a good idea to define constants for each option to help with code readability.</span></span>

-   <span data-ttu-id="d131c-124">フォーム レベルでは、コンテキスト メニューに追加されている各メニュー オプションの定数を追加します。</span><span class="sxs-lookup"><span data-stu-id="d131c-124">At the form level, add a constant for each menu option that is being added to the context menu.</span></span> <span data-ttu-id="d131c-125">値は各コンテキスト メニュー内で一意でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d131c-125">The value must be unique within each context menu.</span></span> <span data-ttu-id="d131c-126">フォームまたはコントロールで別の変数と競合する場合、古い変数名を変更する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d131c-126">Note that you must modify the old variable name if it conflicts with another variable on the form or control.</span></span>

#### <a name="before"></a><span data-ttu-id="d131c-127">以前</span><span class="sxs-lookup"><span data-stu-id="d131c-127">Before</span></span>

    public void context()
    {
        ...
        int listCreateRoot = listMenu.insertItem("@SYS5480");
        ...

#### <a name="after"></a><span data-ttu-id="d131c-128">変更後</span><span class="sxs-lookup"><span data-stu-id="d131c-128">After</span></span>

    [Form]
    public class MainAccount extends FormRun
    {
        ...
        public const int listCreateRoot = 1;
        ...

### <a name="step-2-build-the-context-menu"></a><span data-ttu-id="d131c-129">手順 2</span><span class="sxs-lookup"><span data-stu-id="d131c-129">Step 2.</span></span> <span data-ttu-id="d131c-130">コンテキスト メニューの構築</span><span class="sxs-lookup"><span data-stu-id="d131c-130">Build the context menu</span></span>

<span data-ttu-id="d131c-131">サブメニューとメニュー オプションのリストを構築し、コントロールのコンテキスト メニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="d131c-131">Construct the list of submenus and menu options, and add it to the control’s context menu.</span></span>

1.  <span data-ttu-id="d131c-132">コントロールの **getContextMenuOptions()** メソッドの上書きを追加します。</span><span class="sxs-lookup"><span data-stu-id="d131c-132">Add the **getContextMenuOptions()** method override on the control.</span></span>
2.  <span data-ttu-id="d131c-133">新しいコンテキスト メニューと、メニューに追加するオプションを保持するリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="d131c-133">Create a new context menu and a list to hold the options that you will add to the menu:</span></span>
    -   <span data-ttu-id="d131c-134">ContextMenu メニュー = 新しい ContextMenu();</span><span class="sxs-lookup"><span data-stu-id="d131c-134">ContextMenu menu = new ContextMenu();</span></span>
    -   <span data-ttu-id="d131c-135">List menuOptions = new List(Types::Class);</span><span class="sxs-lookup"><span data-stu-id="d131c-135">List menuOptions = new List(Types::Class);</span></span>

3.  <span data-ttu-id="d131c-136">一覧にメニュー オプションを追加:</span><span class="sxs-lookup"><span data-stu-id="d131c-136">Add menu options to the list:</span></span>
    -   <span data-ttu-id="d131c-137">ContextMenuOption オプション = ContextMenuOption::Create(label,identifier);</span><span class="sxs-lookup"><span data-stu-id="d131c-137">ContextMenuOption option = ContextMenuOption::Create(label,identifier);</span></span>
    -   <span data-ttu-id="d131c-138">menuOptions.addEnd(option);</span><span class="sxs-lookup"><span data-stu-id="d131c-138">menuOptions.addEnd(option);</span></span>

4.  <span data-ttu-id="d131c-139">メニューにオプションのリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="d131c-139">Add the list of options to the menu.</span></span>
    -   <span data-ttu-id="d131c-140">menu.ContextMenuOptions(menuOptions);</span><span class="sxs-lookup"><span data-stu-id="d131c-140">menu.ContextMenuOptions(menuOptions);</span></span>

5.  <span data-ttu-id="d131c-141">**return** ステートメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="d131c-141">Modify the **return** statement.</span></span>
    -   <span data-ttu-id="d131c-142">return menu.Serialize();</span><span class="sxs-lookup"><span data-stu-id="d131c-142">return menu.Serialize();</span></span>

### <a name="step-3-process-the-user-selection-from-the-context-menu"></a><span data-ttu-id="d131c-143">手順 3</span><span class="sxs-lookup"><span data-stu-id="d131c-143">Step 3.</span></span> <span data-ttu-id="d131c-144">コンテキスト メニューからのユーザーの選択を処理</span><span class="sxs-lookup"><span data-stu-id="d131c-144">Process the user selection from the context menu</span></span>

1.  <span data-ttu-id="d131c-145">コントロールの **selectedMenuOption()** メソッドの上書きを追加します。</span><span class="sxs-lookup"><span data-stu-id="d131c-145">Add the **selectedMenuOption()** method override on the control.</span></span>
2.  <span data-ttu-id="d131c-146">オプション処理用の **switch()** ステートメントを、このオーバーライドに移動します。</span><span class="sxs-lookup"><span data-stu-id="d131c-146">Move the **switch()** statement for processing options into this override.</span></span>

## <a name="code-example"></a><span data-ttu-id="d131c-147">コードの例</span><span class="sxs-lookup"><span data-stu-id="d131c-147">Code example</span></span>
<span data-ttu-id="d131c-148">このセクションでは、Dynamics AX 2012 から Finance and Operations へのコンテキスト メニューの移行について説明します。</span><span class="sxs-lookup"><span data-stu-id="d131c-148">This section illustrates the migration of a context menu from Dynamics AX 2012 to Finance and Operations.</span></span> <span data-ttu-id="d131c-149">**MainAccount** フォームが例として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d131c-149">The **MainAccount** form is used as an example.</span></span>

### <a name="original-code"></a><span data-ttu-id="d131c-150">オリジナル コピー</span><span class="sxs-lookup"><span data-stu-id="d131c-150">Original code</span></span>

    public void context()
    {       
        PopupMenu  listMenu        = new PopupMenu(element.hWnd());
        int        listCreateRoot  = listMenu.insertItem("@SYS5480");
        int        selectedMenu;
        selectedMenu = listMenu.draw();
        switch (selectedMenu)
        {
            case -1:
                break;
            case listCreateRoot:
                mainAccount_ds.create();
                break;
            default:
                break;
        }
    }

### <a name="migrated-code"></a><span data-ttu-id="d131c-151">移行されたコード</span><span class="sxs-lookup"><span data-stu-id="d131c-151">Migrated code</span></span>

    // Define new form-level constant for each context menu option
    public const int listCreateRoot = 1;
    // Define new override on the control for building the context menu
    public str getContextMenuOptions()
    {
        str ret;
        ContextMenu menu = new ContextMenu(); 
        ContextMenuOption option = ContextMenuOption::Create("@SYS5480", listCreateRoot);
        List menuOptions = new List(Types::Class); 
        // Add label and ID of menu option
        menuOptions.addEnd(option); 
        menu.ContextMenuOptions(menuOptions);
        return menu.Serialize();
    }
    // Define new override on the control for processing the user selection
    public void selectedMenuOption(int selectedOption)
    {
        switch (selectedOption)
        {
            case -1:
                break;
            case listCreateRoot:
                mainAccount_ds.create();
                break;
            default:
                break;
        }
    }

## <a name="ux-guidelines-for-context-menus"></a><span data-ttu-id="d131c-152">コンテキスト メニューの UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="d131c-152">UX guidelines for context menus</span></span>
<span data-ttu-id="d131c-153">コンテキスト メニューを移行する際、次のガイドラインを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="d131c-153">As you migrate context menus, consider the following guidelines:</span></span>

-   <span data-ttu-id="d131c-154">最も重要なコマンドは、メニューの先頭にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="d131c-154">The most important commands should be at the top of the menu.</span></span>
-   <span data-ttu-id="d131c-155">右クリックの対象となる要素の現在の状態に適用されないコマンドを削除します。</span><span class="sxs-lookup"><span data-stu-id="d131c-155">Remove commands that don't apply to the current state of the element that is the target of the right-click.</span></span>
-   <span data-ttu-id="d131c-156">右クリックはショートカットです。</span><span class="sxs-lookup"><span data-stu-id="d131c-156">Right-click is a shortcut.</span></span> <span data-ttu-id="d131c-157">したがって、コンテキスト メニューのコマンドは、**常に**ページの他の場所で利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d131c-157">Therefore, the commands on the context menu should **always** be available in other places on the page.</span></span>
-   <span data-ttu-id="d131c-158">コンテキスト メニューのサブメニューを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="d131c-158">Don't create submenus of context menus.</span></span> <span data-ttu-id="d131c-159">サブメニューは使いにくくタッチ対応ではありません。</span><span class="sxs-lookup"><span data-stu-id="d131c-159">Submenus are hard to use and aren't touch-friendly.</span></span>
-   <span data-ttu-id="d131c-160">メニュー項目の数を 5 に制限します。</span><span class="sxs-lookup"><span data-stu-id="d131c-160">Limit the number of menu items to five.</span></span>





