---
title: コードの移行 - コンテキスト メニュー コード
description: このトピックでは、コンテキスト メニュー ( ショートカット メニュー) に必要なプログラミング モデルの詳細情報を提供します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 16301
ms.assetid: 8f3b62f2-4de6-4ea3-b3e6-1101d0fe308e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6976bdc38c1595c805f624a50c2e136548ebd8ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688515"
---
# <a name="code-migration---context-menu-code"></a><span data-ttu-id="cb9fe-103">コードの移行 - コンテキスト メニュー コード</span><span class="sxs-lookup"><span data-stu-id="cb9fe-103">Code migration - Context menu code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb9fe-104">プログラミング モデルには、コンテキスト メニュー (ショートカット メニュー) が必要です。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-104">A programming model is required for context menus (shortcut menus).</span></span> <span data-ttu-id="cb9fe-105">このトピックでは、Microsoft Dynamics AX 2012 から Finance and Operations へのコンテキスト メニュー コードの移行移行プロセスの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-105">This topic outlines the process for migrating context menu code from Microsoft Dynamics AX 2012 to Finance and Operations.</span></span> <span data-ttu-id="cb9fe-106">また、コンテキスト メニューのユーザー エクスペリエンス (UX) ガイドラインも含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-106">It also includes user experience (UX) guidelines for context menus.</span></span>

<span data-ttu-id="cb9fe-107">Dynamics AX 2012 およびそれ以前のバージョンでは、開発者が **PopupMenu** クラスを使用して右クリック コンテキスト メニュー (ショートカット メニュー) を変更していました。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-107">In Dynamics AX 2012 and earlier versions, developers modified right-click context menus (shortcut menus) by using the **PopupMenu** class.</span></span> <span data-ttu-id="cb9fe-108">このクラスは、Web 上で利用できない Microsoft Windows アプリケーション プログラミング インターフェイス (API) に依存していました。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-108">This class relied on Microsoft Windows application programming interfaces (APIs) that aren't available on the web.</span></span> <span data-ttu-id="cb9fe-109">Finance and Operations では、同様の機能を提供する代わりに,**ContextMenu** API が作成されました。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-109">In Finance and Operations, the **ContextMenu** APIs have been created as replacements to provide similar functionality.</span></span> <span data-ttu-id="cb9fe-110">以前は、**context()** メソッドと **showContextMenu()** メソッドのオーバーライドは、特定のコントロールのコンテキスト メニューを変更するためのエントリ ポイントでした。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-110">Previously, the **context()** and **showContextMenu()** method overrides were the entry points for modifying context menus for specific controls.</span></span> <span data-ttu-id="cb9fe-111">これらの上書きには通常、コンテキスト メニューにオプションを追加したり、ユーザーの選択を処理するためのコードが含まれていました。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-111">These overrides typically contained code to add options to the context menu, and also to process the user’s selection.</span></span> <span data-ttu-id="cb9fe-112">ユーザーの選択を処理するコードは、待機モデルを使用していました。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-112">The code for processing the user's selection used a wait model.</span></span> <span data-ttu-id="cb9fe-113">これらの上書きが削除され、待機モデルが消去されるため、開発者は次の 2 つの上書きを作成する必要があります。**getContextMenuOptions()** によりコンテキスト メニューのオプションを追加し、**selectedMenuOption()** によりユーザーの選択を処理します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-113">Because these overrides are being removed and the wait model is being eliminated, developers must now create two overrides: **getContextMenuOptions()** to add options to the context menu and **selectedMenuOption()** to process the user’s selection.</span></span>

## <a name="migrate-context-menu-code"></a><span data-ttu-id="cb9fe-114">コンテキスト メニュー コードの移行</span><span class="sxs-lookup"><span data-stu-id="cb9fe-114">Migrate context menu code</span></span> 
<span data-ttu-id="cb9fe-115">**PopupMenu** API から **ContextMenu** API への移行は、3 つの主な段階に分けることができます。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-115">Migration from the **PopupMenu** APIs to the **ContextMenu** APIs can be broken down into three main steps.</span></span>

### <a name="step-1-add-a-constant-for-each-menu-option-that-must-be-added"></a><span data-ttu-id="cb9fe-116">手順 1</span><span class="sxs-lookup"><span data-stu-id="cb9fe-116">Step 1.</span></span> <span data-ttu-id="cb9fe-117">追加する必要のあるメニュー オプションごとの定数の追加</span><span class="sxs-lookup"><span data-stu-id="cb9fe-117">Add a constant for each menu option that must be added</span></span>

<span data-ttu-id="cb9fe-118">**PopupMenu** クラスの古い **insertItem()** メソッドは、追加されたメニュー オプションの識別子を返しました。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-118">The old **insertItem()** method in the **PopupMenu** class returned an identifier for the menu option that was being added.</span></span> <span data-ttu-id="cb9fe-119">この識別子は、将来の参照のために変数に保存されました。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-119">This identifier was saved into a variable for future reference.</span></span> <span data-ttu-id="cb9fe-120">開発者はメニュー識別子を定義するため、各オプションの定数を定義してコードの可読性を高めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-120">Because developers will define the menu identifier, it's a good idea to define constants for each option to help with code readability.</span></span>

-   <span data-ttu-id="cb9fe-121">フォーム レベルでは、コンテキスト メニューに追加されている各メニュー オプションの定数を追加します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-121">At the form level, add a constant for each menu option that is being added to the context menu.</span></span> <span data-ttu-id="cb9fe-122">値は各コンテキスト メニュー内で一意でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-122">The value must be unique within each context menu.</span></span> <span data-ttu-id="cb9fe-123">フォームまたはコントロールで別の変数と競合する場合、古い変数名を変更する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-123">Note that you must modify the old variable name if it conflicts with another variable on the form or control.</span></span>

#### <a name="before"></a><span data-ttu-id="cb9fe-124">以前</span><span class="sxs-lookup"><span data-stu-id="cb9fe-124">Before</span></span>

```xpp
public void context()
{
    ...
    int listCreateRoot = listMenu.insertItem("@SYS5480");
    ...
```

#### <a name="after"></a><span data-ttu-id="cb9fe-125">変更後</span><span class="sxs-lookup"><span data-stu-id="cb9fe-125">After</span></span>

```xpp
[Form]
public class MainAccount extends FormRun
{
    ...
    public const int listCreateRoot = 1;
    ...
```

### <a name="step-2-build-the-context-menu"></a><span data-ttu-id="cb9fe-126">手順 2</span><span class="sxs-lookup"><span data-stu-id="cb9fe-126">Step 2.</span></span> <span data-ttu-id="cb9fe-127">コンテキスト メニューの構築</span><span class="sxs-lookup"><span data-stu-id="cb9fe-127">Build the context menu</span></span>

<span data-ttu-id="cb9fe-128">サブメニューとメニュー オプションのリストを構築し、コントロールのコンテキスト メニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-128">Construct the list of submenus and menu options, and add it to the control’s context menu.</span></span>

1.  <span data-ttu-id="cb9fe-129">コントロールの **getContextMenuOptions()** メソッドの上書きを追加します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-129">Add the **getContextMenuOptions()** method override on the control.</span></span>
2.  <span data-ttu-id="cb9fe-130">新しいコンテキスト メニューと、メニューに追加するオプションを保持するリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-130">Create a new context menu and a list to hold the options that you will add to the menu:</span></span>
    -   <span data-ttu-id="cb9fe-131">ContextMenu メニュー = 新しい ContextMenu();</span><span class="sxs-lookup"><span data-stu-id="cb9fe-131">ContextMenu menu = new ContextMenu();</span></span>
    -   <span data-ttu-id="cb9fe-132">List menuOptions = new List(Types::Class);</span><span class="sxs-lookup"><span data-stu-id="cb9fe-132">List menuOptions = new List(Types::Class);</span></span>

3.  <span data-ttu-id="cb9fe-133">一覧にメニュー オプションを追加:</span><span class="sxs-lookup"><span data-stu-id="cb9fe-133">Add menu options to the list:</span></span>
    -   <span data-ttu-id="cb9fe-134">ContextMenuOption option = ContextMenuOption::Create(label,identifier);</span><span class="sxs-lookup"><span data-stu-id="cb9fe-134">ContextMenuOption option = ContextMenuOption::Create(label,identifier);</span></span>
    -   <span data-ttu-id="cb9fe-135">menuOptions.addEnd(option);</span><span class="sxs-lookup"><span data-stu-id="cb9fe-135">menuOptions.addEnd(option);</span></span>

4.  <span data-ttu-id="cb9fe-136">メニューにオプションのリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-136">Add the list of options to the menu.</span></span>
    -   <span data-ttu-id="cb9fe-137">menu.ContextMenuOptions(menuOptions);</span><span class="sxs-lookup"><span data-stu-id="cb9fe-137">menu.ContextMenuOptions(menuOptions);</span></span>

5.  <span data-ttu-id="cb9fe-138">**return** ステートメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-138">Modify the **return** statement.</span></span>
    -   <span data-ttu-id="cb9fe-139">return menu.Serialize();</span><span class="sxs-lookup"><span data-stu-id="cb9fe-139">return menu.Serialize();</span></span>

### <a name="step-3-process-the-user-selection-from-the-context-menu"></a><span data-ttu-id="cb9fe-140">手順 3</span><span class="sxs-lookup"><span data-stu-id="cb9fe-140">Step 3.</span></span> <span data-ttu-id="cb9fe-141">コンテキスト メニューからのユーザーの選択を処理</span><span class="sxs-lookup"><span data-stu-id="cb9fe-141">Process the user selection from the context menu</span></span>

1.  <span data-ttu-id="cb9fe-142">コントロールの **selectedMenuOption()** メソッドの上書きを追加します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-142">Add the **selectedMenuOption()** method override on the control.</span></span>
2.  <span data-ttu-id="cb9fe-143">オプション処理用の **switch()** ステートメントを、このオーバーライドに移動します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-143">Move the **switch()** statement for processing options into this override.</span></span>

## <a name="code-example"></a><span data-ttu-id="cb9fe-144">コードの例</span><span class="sxs-lookup"><span data-stu-id="cb9fe-144">Code example</span></span>
<span data-ttu-id="cb9fe-145">このセクションでは、Dynamics AX 2012 から Finance and Operations へのコンテキスト メニューの移行について説明します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-145">This section illustrates the migration of a context menu from Dynamics AX 2012 to Finance and Operations.</span></span> <span data-ttu-id="cb9fe-146">**MainAccount** フォームが例として使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-146">The **MainAccount** form is used as an example.</span></span>

### <a name="original-code"></a><span data-ttu-id="cb9fe-147">オリジナル コピー</span><span class="sxs-lookup"><span data-stu-id="cb9fe-147">Original code</span></span>

```xpp
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
```

### <a name="migrated-code"></a><span data-ttu-id="cb9fe-148">移行されたコード</span><span class="sxs-lookup"><span data-stu-id="cb9fe-148">Migrated code</span></span>

```xpp
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
```

## <a name="ux-guidelines-for-context-menus"></a><span data-ttu-id="cb9fe-149">コンテキスト メニューの UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="cb9fe-149">UX guidelines for context menus</span></span>
<span data-ttu-id="cb9fe-150">コンテキスト メニューを移行する際、次のガイドラインを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-150">As you migrate context menus, consider the following guidelines:</span></span>

-   <span data-ttu-id="cb9fe-151">最も重要なコマンドは、メニューの先頭にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-151">The most important commands should be at the top of the menu.</span></span>
-   <span data-ttu-id="cb9fe-152">右クリックの対象となる要素の現在の状態に適用されないコマンドを削除します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-152">Remove commands that don't apply to the current state of the element that is the target of the right-click.</span></span>
-   <span data-ttu-id="cb9fe-153">右クリックはショートカットです。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-153">Right-click is a shortcut.</span></span> <span data-ttu-id="cb9fe-154">したがって、コンテキスト メニューのコマンドは、**常に** ページの他の場所で利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-154">Therefore, the commands on the context menu should **always** be available in other places on the page.</span></span>
-   <span data-ttu-id="cb9fe-155">コンテキスト メニューのサブメニューを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-155">Don't create submenus of context menus.</span></span> <span data-ttu-id="cb9fe-156">サブメニューは使いにくくタッチ対応ではありません。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-156">Submenus are hard to use and aren't touch-friendly.</span></span>
-   <span data-ttu-id="cb9fe-157">メニュー項目の数を 5 に制限します。</span><span class="sxs-lookup"><span data-stu-id="cb9fe-157">Limit the number of menu items to five.</span></span>


