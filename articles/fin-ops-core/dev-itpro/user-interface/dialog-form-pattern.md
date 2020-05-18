---
title: ダイアログのフォーム パターン
description: このトピックでは、ダイアログ フォームのパターンについて説明します。 ダイアログ ボックスは、ユーザーが明示的にコミットまたはキャンセルできる活動またはアクションを表します。
author: jasongre
manager: AnnBe
ms.date: 10/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 16061
ms.assetid: 80c93e91-1952-44ce-af93-a17965ee476a
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5883d2316f5a6d896349f19ebc70ced581fbf8
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329924"
---
# <a name="dialog-form-pattern"></a><span data-ttu-id="b4fe4-104">ダイアログのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-104">Dialog form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4fe4-105">このトピックでは、ダイアログ フォームのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-105">This topic provides information about the Dialog form pattern.</span></span> <span data-ttu-id="b4fe4-106">ダイアログ ボックスは、ユーザーが明示的にコミットまたはキャンセルできる活動またはアクションを表します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-106">A dialog box represents an action or activity that users can explicitly commit or cancel.</span></span> <span data-ttu-id="b4fe4-107">これは、ユーザーが特定のタスクやプロセスを開始し、システムが続行方法または続行するかどうかに関するユーザー入力を必要とする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-107">It's used when a user initiates a specific task or process, and the system requires user input about how or whether to proceed.</span></span>

<a name="usage"></a><span data-ttu-id="b4fe4-108">用途</span><span class="sxs-lookup"><span data-stu-id="b4fe4-108">Usage</span></span>
-----

<span data-ttu-id="b4fe4-109">ダイアログ ボックスは、ユーザーが明示的にコミットまたはキャンセルできる活動またはアクションを表します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-109">A dialog box represents an action or activity that users can explicitly commit or cancel.</span></span> <span data-ttu-id="b4fe4-110">これは、ユーザーが特定のタスクやプロセスを開始し、システムが続行方法または続行するかどうかに関するユーザー入力を必要とする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-110">It's used when a user initiates a specific task or process, and the system requires user input about how or whether to proceed.</span></span> <span data-ttu-id="b4fe4-111">ダイアログはモーダルであり、ユーザーが親ページに戻る前にダイアログ内のコントロールと対話する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-111">Dialogs are modal and require that users interact with the controls in the dialog before they can return to the parent page.</span></span> <span data-ttu-id="b4fe4-112">ダイアログも複数のサイズを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-112">Dialogs also can have multiple sizes.</span></span> <span data-ttu-id="b4fe4-113">ダイアログ サイズの選択は主観的なものであり、ダイアログ ボックスでモデル化したフォームの要素によって変化します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-113">Selection of a dialog size is subjective, and will vary, depending on the form elements that you've modeled on the dialog.</span></span> <span data-ttu-id="b4fe4-114">次のサイズがあります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-114">The sizes are as follows:</span></span>

-   <span data-ttu-id="b4fe4-115">**小** – このサイズは 1 列幅のダイアログです。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-115">**Small** – This size is a one-column-wide dialog.</span></span> <span data-ttu-id="b4fe4-116">ダイアログに比較的少量のコンテンツ (幅テーブルまたはその他の幅要素はなく、すべての単純なフィールド) が含まれている場合、このサイズを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-116">If your dialog contains a relatively small amount of content (all simple fields, and no wide tables or other wide elements), you can probably use this size.</span></span>
-   <span data-ttu-id="b4fe4-117">**中** – このサイズは 2 列幅のダイアログです。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-117">**Medium** – This size is a two-column-wide dialog.</span></span> <span data-ttu-id="b4fe4-118">ダイアログに、小型ダイアログ内にうまく収まらない多くのコンテンツが含まれているが、全幅ダイアログは必要ではない場合、このサイズを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-118">If your dialog contains more content than can comfortably fit within a small dialog, but a full-width dialog isn’t required, you should use this size.</span></span>
-   <span data-ttu-id="b4fe4-119">**大** – このサイズは 3 列幅のダイアログです。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-119">**Large** – This size is a three-column-wide dialog.</span></span> <span data-ttu-id="b4fe4-120">ダイアログに、中間ダイアログ内にうまく収まらない多くのコンテンツが含まれているが、全幅ダイアログは必要ではない場合、このサイズを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-120">If your dialog contains more content than can comfortably fit within a medium dialog, but a full-width dialog isn’t required, you should use this size.</span></span>
-   <span data-ttu-id="b4fe4-121">**最大** – 大きなダイアログはブラウザのビューポートのほぼ全幅です。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-121">**Full** – A large dialog is nearly the full width of the browser viewport.</span></span> <span data-ttu-id="b4fe4-122">そのサイズはビューポートの幅に応じて異なり、必ず最大ダイアログ サイズ オプションになります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-122">Its size varies, depending on the viewport width, and it will always be the largest dialog size option.</span></span> <span data-ttu-id="b4fe4-123">このサイズは、ダイアログに幅の広い要素が多数ある場合、または異常に大きな水平スペース幅が必要な場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-123">Use this size if your dialog has a lot of wide elements, or if it requires an unusually large amount of horizontal space.</span></span>

<span data-ttu-id="b4fe4-124">さまざまなダイアログ サイズに関する詳細については、「正しいダイアログ サイズを選択」で、このトピックの付録にあるテーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-124">For more detail about the various dialog sizes, see the table in the appendix of this topic, under “Selecting the correct dialog size.”</span></span> <span data-ttu-id="b4fe4-125">そのテーブルをレビューすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-125">We strongly recommend that you review that table.</span></span> <span data-ttu-id="b4fe4-126">このドキュメントでは、5 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-126">Five patterns are described in this document:</span></span>

-   <span data-ttu-id="b4fe4-127">**ダイアログ** - これは、基本的なダイアログ パターンです。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-127">**Dialog** – This is the basic dialog pattern.</span></span> <span data-ttu-id="b4fe4-128">このダイアログは、他のダイアログ パターンのどれかを使用する必要がない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-128">Use this dialog if you don't have a reason to use one of the other Dialog patterns.</span></span>
-   <span data-ttu-id="b4fe4-129">**タブ付きダイアログ** - これは、ダイアログ パターンのさらに特定のバージョンです。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-129">**Dialog w/tabs** – This is a more specific version of the Dialog pattern.</span></span> <span data-ttu-id="b4fe4-130">これには、ダイアログのタブ コントロールが組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-130">It incorporates a Tab control in the dialog.</span></span> <span data-ttu-id="b4fe4-131">また、必要に応じて、タブのヘッダー、およびフッターを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-131">You can also optionally provide a header for the Tab, and also a footer.</span></span>
-   <span data-ttu-id="b4fe4-132">**クイック タブ付きダイアログ** - これはタブ付きダイアログ パターンとよく似ていますが、情報を整理するために通常タブの代わりにクイック タブを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-132">**Dialog w/FastTabs** – This closely resembles the Dialog w/tabs pattern but uses FastTabs instead of regular tabs to organize the information.</span></span>
-   <span data-ttu-id="b4fe4-133">**二重タブ付きダイアログ** - これはタブ付きダイアログ パターンによく似ていますが、最初のタブ コントロールの直後に 2 番目のタブ コントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-133">**Dialog w/double tabs** – This closely resembles the Dialog w/tabs pattern but has a second Tab control immediately after the first one.</span></span>
-   <span data-ttu-id="b4fe4-134">**ダイアログ (読み取り専用)** - このパターンは、編集できない情報フォーム用です。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-134">**Dialog (read only)** – This pattern is for informational forms that aren't editable.</span></span> <span data-ttu-id="b4fe4-135">ユーザーはタブまたはビュー セレクターを切り替えることはできますが、入力フィールドの直接操作は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-135">The user can still switch between tabs or a view selector, but direct manipulation of input fields isn't allowed.</span></span> <span data-ttu-id="b4fe4-136">このダイアログには、**OK** および **Cancel** ボタンの代わりに **Close** ボタンも含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-136">This dialog variation also includes a **Close** button instead of **OK** and **Cancel** buttons.</span></span>

## <a name="wireframe"></a><span data-ttu-id="b4fe4-137">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="b4fe4-137">Wireframe</span></span>
<span data-ttu-id="b4fe4-138">次のセクションでは、この記事に含まれている 4 つのダイアログ タイプのワイヤーフレームを示します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-138">The following sections show the wireframes for the four dialog types that are included in this article.</span></span>

### <a name="dialog"></a><span data-ttu-id="b4fe4-139">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-139">Dialog</span></span>

<span data-ttu-id="b4fe4-140">[![ダイアログのワイヤーフレーム](./media/dialogform1.png)](./media/dialogform1.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-140">[![Wireframe for dialog](./media/dialogform1.png)](./media/dialogform1.png)</span></span>

### <a name="dialog-wtabs-and-dialog-wfasttabs"></a><span data-ttu-id="b4fe4-141">タブ付きダイアログおよびクイック タブ付きダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-141">Dialog w/tabs and Dialog w/FastTabs</span></span>

<span data-ttu-id="b4fe4-142">[![タブとクイックタブによるダイアログのワイヤフレーム](./media/dialogform2.png)](./media/dialogform2.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-142">[![Wireframe for dialog with tabs and FastTabs](./media/dialogform2.png)](./media/dialogform2.png)</span></span>

### <a name="dialog-wdouble-tabs"></a><span data-ttu-id="b4fe4-143">二重タブ付きダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-143">Dialog w/double tabs</span></span>

<span data-ttu-id="b4fe4-144">[![ダブル タブによるダイアログのワイヤフレーム](./media/dialogform3.png)](./media/dialogform3.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-144">[![Wireframe for dialog with double tabs](./media/dialogform3.png)](./media/dialogform3.png)</span></span>

### <a name="dialog-read-only"></a><span data-ttu-id="b4fe4-145">ダイアログ (読み取り専用)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-145">Dialog (read only)</span></span>

<span data-ttu-id="b4fe4-146">[![ダイアログのワイヤーフレーム (読み取り専用)](./media/dialogform4.png)](./media/dialogform4.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-146">[![Wireframe for dialog (read only)](./media/dialogform4.png)](./media/dialogform4.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="b4fe4-147">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="b4fe4-147">Pattern changes</span></span>
<span data-ttu-id="b4fe4-148">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-148">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="b4fe4-149">フォームのキャプションは MainInstruction として機能します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-149">The form caption serves as the MainInstruction.</span></span> <span data-ttu-id="b4fe4-150">したがって、モデル化された MainInstruction コントロールは必要なくなりました。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-150">Therefore, a modeled MainInstruction control is no longer required.</span></span>
-   <span data-ttu-id="b4fe4-151">エラー メッセージの手動処理が必要なくなりました。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-151">Manual handling of error messages is no longer required.</span></span>
-   <span data-ttu-id="b4fe4-152">場合によっては、フォームのコンテンツが使用可能な高さを超えた場合にボタンでスライダーの一番下までスクロールできます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-152">In some cases, buttons will scroll off the bottom of the slider if the form content exceeds the available height.</span></span>
-   <span data-ttu-id="b4fe4-153">スライダー ダイアログ ボックスには、独自のメッセージ バーがあります (スライダーが開いたときに主要なメッセージ バーが半透明になるため)。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-153">Slider dialogs have their own message bar (because the main message bar is obscured when a slider is open).</span></span>

## <a name="model"></a><span data-ttu-id="b4fe4-154">モデル</span><span class="sxs-lookup"><span data-stu-id="b4fe4-154">Model</span></span>
### <a name="dialog-basic--high-level-structure"></a><span data-ttu-id="b4fe4-155">ダイアログ (basic) – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="b4fe4-155">Dialog (basic) – High-level structure</span></span>

- <span data-ttu-id="b4fe4-156">デザイン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-156">Design</span></span>

    - <span data-ttu-id="b4fe4-157">*SecondaryInstruction (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-157">*SecondaryInstruction (StaticText) \[Optional\]*</span></span>

        - <span data-ttu-id="b4fe4-158">*ActionPane (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-158">*ActionPane (ActionPane) \[Optional\]*</span></span>
        - <span data-ttu-id="b4fe4-159">*DialogHeader (グループ、繰り返し可) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-159">*DialogHeader (Group, can repeat) \[Optional\]*</span></span>
        - <span data-ttu-id="b4fe4-160">DialogContent (Group、1..Nを繰り返す)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-160">DialogContent (Group, repeats 1..N)</span></span>
        - <span data-ttu-id="b4fe4-161">DialogCommitContainer (ButtonGroup)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-161">DialogCommitContainer (ButtonGroup)</span></span>

            - <span data-ttu-id="b4fe4-162">OKButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-162">OKButton ($Button)</span></span>
            - <span data-ttu-id="b4fe4-163">*OtherButton ($ ボタン、繰り返し可) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-163">*OtherButton ($Button, can repeat) \[Optional\]*</span></span>
            - <span data-ttu-id="b4fe4-164">CancelButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-164">CancelButton ($Button)</span></span>

###  <a name="dialog-wtabs-and-dialog-wfasttabs--high-level-structure"></a><span data-ttu-id="b4fe4-165">タブ付きダイアログおよびクイック タブ付きダイアログ – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="b4fe4-165">Dialog w/Tabs and Dialog w/FastTabs – High-level structure</span></span>

- <span data-ttu-id="b4fe4-166">デザイン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-166">Design</span></span>

    - <span data-ttu-id="b4fe4-167">*SecondaryInstruction (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-167">*SecondaryInstruction (StaticText) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-168">*ActionPane (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-168">*ActionPane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-169">*DialogHeader (グループ、繰り返し可) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-169">*DialogHeader (Group, can repeat) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-170">TabContent (タブ)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-170">TabContent (Tab)</span></span>

        - <span data-ttu-id="b4fe4-171">TabPage (TabPage。1..N を繰り返し)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-171">TabPage (TabPage, repeats 1..N)</span></span>

    - <span data-ttu-id="b4fe4-172">*DialogFooter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-172">*DialogFooter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-173">DialogCommitContainer (ButtonGroup)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-173">DialogCommitContainer (ButtonGroup)</span></span>

        - <span data-ttu-id="b4fe4-174">OKButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-174">OKButton ($Button)</span></span>
        - <span data-ttu-id="b4fe4-175">*OtherButton ($ ボタン、繰り返し可) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-175">*OtherButton ($Button, can repeat) \[Optional\]*</span></span>
        - <span data-ttu-id="b4fe4-176">CancelButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-176">CancelButton ($Button)</span></span>

### <a name="dialog-wdouble-tabs--high-level-structure"></a><span data-ttu-id="b4fe4-177">二重タブ付きダイアログ – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="b4fe4-177">Dialog w/double tabs – High-level structure</span></span>

- <span data-ttu-id="b4fe4-178">デザイン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-178">Design</span></span>

    - <span data-ttu-id="b4fe4-179">*SecondaryInstruction (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-179">*SecondaryInstruction (StaticText) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-180">*ActionPane (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-180">*ActionPane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-181">*DialogHeader (グループ、繰り返し可) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-181">*DialogHeader (Group, can repeat) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-182">TabContent (タブ)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-182">TabContent (Tab)</span></span>

        - <span data-ttu-id="b4fe4-183">TabPage (TabPage) \[1..\*\]</span><span class="sxs-lookup"><span data-stu-id="b4fe4-183">TabPage (TabPage) \[1..\*\]</span></span>

    - <span data-ttu-id="b4fe4-184">TabContent (タブ)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-184">TabContent (Tab)</span></span>

        - <span data-ttu-id="b4fe4-185">TabPage (TabPage) \[1..\*\]</span><span class="sxs-lookup"><span data-stu-id="b4fe4-185">TabPage (TabPage) \[1..\*\]</span></span>

    - <span data-ttu-id="b4fe4-186">*DialogFooter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-186">*DialogFooter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-187">DialogCommitContainer (ButtonGroup)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-187">DialogCommitContainer (ButtonGroup)</span></span>

        - <span data-ttu-id="b4fe4-188">OKButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-188">OKButton ($Button)</span></span>
        - <span data-ttu-id="b4fe4-189">*OtherButton ($ ボタン、繰り返し可) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-189">*OtherButton ($Button, can repeat) \[Optional\]*</span></span>
        - <span data-ttu-id="b4fe4-190">CancelButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-190">CancelButton ($Button)</span></span>

### <a name="dialog-read-only--high-level-structure"></a><span data-ttu-id="b4fe4-191">ダイアログ (読み取り専用) – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="b4fe4-191">Dialog (read only) – High-level structure</span></span>

- <span data-ttu-id="b4fe4-192">デザイン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-192">Design</span></span>

    - <span data-ttu-id="b4fe4-193">*SecondaryInstruction (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-193">*SecondaryInstruction (StaticText) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-194">*ActionPane (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-194">*ActionPane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-195">*DialogHeader (グループ、繰り返し可) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b4fe4-195">*DialogHeader (Group, can repeat) \[Optional\]*</span></span>
    - <span data-ttu-id="b4fe4-196">DialogContent (Group、1..Nを繰り返す)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-196">DialogContent (Group, repeats 1..N)</span></span>
    - <span data-ttu-id="b4fe4-197">DialogCommitContainer (ButtonGroup)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-197">DialogCommitContainer (ButtonGroup)</span></span>

        <span data-ttu-id="b4fe4-198">CloseButton ($Button)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-198">CloseButton ($Button)</span></span>

### <a name="core-components"></a><span data-ttu-id="b4fe4-199">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b4fe4-199">Core components</span></span>

-   <span data-ttu-id="b4fe4-200">**Form.Design** にダイアログ パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-200">Apply the Dialog pattern on **Form.Design**.</span></span>
-   <span data-ttu-id="b4fe4-201">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-201">Address BP Warnings:</span></span>
    -   <span data-ttu-id="b4fe4-202">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-202">**Design.Caption** isn't empty.</span></span>
    -   <span data-ttu-id="b4fe4-203">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-203">The form must be referenced by at least one menu item.</span></span>
    -   <span data-ttu-id="b4fe4-204">**StaticText.Text** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-204">**StaticText.Text** isn't empty.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="b4fe4-205">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-205">Related patterns</span></span>

-   [<span data-ttu-id="b4fe4-206">ドロップ ダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-206">Drop Dialog</span></span>](drop-dialog-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="b4fe4-207">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-207">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="b4fe4-208">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-208">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="b4fe4-209">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="b4fe4-209">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="b4fe4-210">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="b4fe4-210">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   [<span data-ttu-id="b4fe4-211">テキスト入力</span><span class="sxs-lookup"><span data-stu-id="b4fe4-211">Fill Text</span></span>](fill-text-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="b4fe4-212">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="b4fe4-212">UX guidelines</span></span>
<span data-ttu-id="b4fe4-213">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-213">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="b4fe4-214">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-214">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="b4fe4-215">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-215">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="b4fe4-216">**標準フォーム** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="b4fe4-216">**Standard form** **guidelines:**</span></span>

-   <span data-ttu-id="b4fe4-217">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-217">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="b4fe4-218">**ダイアログ ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="b4fe4-218">**Dialog guidelines:**</span></span>

-   <span data-ttu-id="b4fe4-219">ダイアログ ボックスが最初に開いたときに、フォーカスは、ダイアログ ボックスの最初の編集可能なフィールドにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-219">Focus should be in the first editable field in the dialog box when the dialog box is first opened.</span></span>
    -   <span data-ttu-id="b4fe4-220">**例外:** ダイアログが読み取り専用の場合、フォーカスは**閉じる**ボタンにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-220">**Exception:** If the dialog is read-only, focus should be on the **Close** button.</span></span>
-   <span data-ttu-id="b4fe4-221">ダイアログには、上部に**主な指示**がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-221">A dialog must have a **main instruction** at the top.</span></span>
    -   <span data-ttu-id="b4fe4-222">指示が明細書である場合、最終的な期間を含めません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-222">A final period should not be included if the instruction is a statement.</span></span> <span data-ttu-id="b4fe4-223">指示が質問である場合、疑問符が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-223">If the instruction is a question, a question mark should be included.</span></span>
-   <span data-ttu-id="b4fe4-224">ユーザーへの二次命令は、オプションで含めることができ、ユーザーがダイアログ ボックスを理解また使用するのに役立つ追加情報を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-224">A secondary instruction to the user can optionally be included, and it should present additional information that will help the user understand or use the dialog box.</span></span> <span data-ttu-id="b4fe4-225">2 番目の指示は、大文字小文字の完全な文で構成する必要があり、文末の句点を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-225">The secondary instruction should consist of a complete sentence in sentence case and should have end punctuation.</span></span>
-   <span data-ttu-id="b4fe4-226">ダイアログには、**コンテンツ**領域が必要です。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-226">A dialog must have a **content** area.</span></span>
-   <span data-ttu-id="b4fe4-227">編集可能なダイアログ対象:</span><span class="sxs-lookup"><span data-stu-id="b4fe4-227">For editable dialogs:</span></span>
    -   <span data-ttu-id="b4fe4-228">コンテンツ領域には、タスクを完了するために必要なコントロールのみが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-228">The content area should contain only the controls that are required in order to complete the task.</span></span>
    -   <span data-ttu-id="b4fe4-229">検証エラーを回避するには、選択リスト、チェック ボックス、ラジオ ボタン、コマンド リンクなどの制約された入力コントロールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-229">Constrained input controls, such as selection lists, check boxes, radio buttons, and command links, should be used to avoid validation errors.</span></span>
    -   <span data-ttu-id="b4fe4-230">可能な場合は、入力ごとに適切な既定値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-230">Reasonable default values for each input should be provided whenever possible.</span></span>
    -   <span data-ttu-id="b4fe4-231">コントロールでは、検証中に別のダイアログが表示しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-231">Controls should not cause another dialog to appear during validation.</span></span>
        -   <span data-ttu-id="b4fe4-232">検証の問題を示す警告メッセージを、できるだけ早く メッセージ バーに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-232">Warning messages for validation issues should be displayed in a message bar as soon as possible.</span></span>
-   <span data-ttu-id="b4fe4-233">読み取り専用ダイアログ用:</span><span class="sxs-lookup"><span data-stu-id="b4fe4-233">For read-only dialogs:</span></span>
    -   <span data-ttu-id="b4fe4-234">コンテンツ領域には、編集不可能なコントロールや、ビュー セレクターなど、ユーザーが表示するデータを切り替えることのみを許可するコントロールが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-234">The content area should only contain controls that are non-editable or only allow the user to switch the data is displayed, such as a view selector.</span></span>
    -   <span data-ttu-id="b4fe4-235">フィールドの値をプログラムにより変更しても、検証エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-235">Programmatically changing the value of a field should not cause validation errors.</span></span>
    -   <span data-ttu-id="b4fe4-236">ダイアログに複数のタブがある場合、最も多くのコンテンツがあるタブはダイアログの幅の選択を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-236">If your dialog has multiple tabs, the tab that has the most content must define the selection of the dialog width.</span></span>
-   <span data-ttu-id="b4fe4-237">ダイアログには、**コミット**ボタン領域が必要です。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-237">A dialog must have a **commit** button area:</span></span>
    -   <span data-ttu-id="b4fe4-238">編集可能なダイアログ ボックスのみに、主要な指示によって黙示されるアクションを起動するコミット ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-238">For an editable dialog only, there is a commit button that starts the action that is implied by the main instruction.</span></span>
    -   <span data-ttu-id="b4fe4-239">ラベルはそれ自体が意味のあるのものである必要があり、主な指示への応答でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-239">The labels should make sense on their own and should be a response to the main instruction.</span></span>
    -   <span data-ttu-id="b4fe4-240">編集可能および読み取り専用両方のダイアログについては、右端のボタンは、副作用なしで操作をキャンセルする**キャンセル**ボタンです。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-240">For both editable and read-only dialogs, the right-most button is a **Cancel** button that cancels the operation without side-effects.</span></span>
    -   <span data-ttu-id="b4fe4-241">ダイアログの既定のボタンとしてマークされたボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-241">There is a button that is marked as the default button for the dialog.</span></span>
    -   <span data-ttu-id="b4fe4-242">デフォルトボタンとして選択されているボタンは、ダイアログまたはドロップダイアログの主な指示など、ユーザーが実行しているタスクに対して最も安全で保護された応答でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-242">The button that is selected as the default button should be the safest, most secure response to the task that the user is performing, such as the main instruction of a Dialog or Drop Dialog.</span></span>
        -   <span data-ttu-id="b4fe4-243">安全性とセキュリティの要素でない場合は、クリックされる可能性が最も高いボタンまたはユーザーにとって最も便利なボタンをデフォルト ボタンとして選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-243">If safety and security aren't factors, the button that is most likely to be clicked or that is most convenient for the user should be selected as the default button.</span></span>
        -   <span data-ttu-id="b4fe4-244">**例外:** コマンドを取り消す簡単で明白な方法がない限り、破壊応答を既定として選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-244">**Exception:** Don't select a destructive response as the default unless there is an easy, obvious way to undo the command.</span></span>

<span data-ttu-id="b4fe4-245">ダイアログには、これらの要素が**ない**必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-245">A dialog should **not** have these elements:</span></span>

-   <span data-ttu-id="b4fe4-246">情報ボックス</span><span class="sxs-lookup"><span data-stu-id="b4fe4-246">FactBoxes</span></span>

## <a name="examples"></a><span data-ttu-id="b4fe4-247">例</span><span class="sxs-lookup"><span data-stu-id="b4fe4-247">Examples</span></span>
### <a name="dialog-basic"></a><span data-ttu-id="b4fe4-248">ダイアログ (basic)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-248">Dialog (basic)</span></span>

<span data-ttu-id="b4fe4-249">フォーム: **ProjTableCreate** (**プロジェクト管理と会計** &gt; **共通** &gt; **プロジェクト** &gt; **すべてのプロジェクト**の順にクリックし、**新規**をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-249">Form: **ProjTableCreate** (Click **Project management and accounting** &gt; **Common** &gt; **Projects** &gt; **All projects**, and then click **New**.)</span></span> 

<span data-ttu-id="b4fe4-250">[![基本ダイアログの例](./media/dialogform5.png)](./media/dialogform5.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-250">[![Example of basic dialog](./media/dialogform5.png)](./media/dialogform5.png)</span></span>

### <a name="dialog-wtabs"></a><span data-ttu-id="b4fe4-251">タブ付きダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-251">Dialog w/tabs</span></span>

<span data-ttu-id="b4fe4-252">フォーム: **CaseDetailCreate** (**共通** &gt; **共通** &gt; **ケース** &gt; **すべてのケース**の順にクリックして、**新規**をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-252">Form: **CaseDetailCreate** (Click **Common** &gt; **Common** &gt; **Cases** &gt; **All cases**, and then click **New**.)</span></span> 

<span data-ttu-id="b4fe4-253">[![タブによるダイアログの例](./media/dialogform6.png)](./media/dialogform6.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-253">[![Example of dialog with tabs](./media/dialogform6.png)](./media/dialogform6.png)</span></span>

### <a name="dialog-wfasttabs"></a><span data-ttu-id="b4fe4-254">クイック タブ付きダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-254">Dialog w/FastTabs</span></span>

<span data-ttu-id="b4fe4-255">この例では、このパターンを使用するフォームの例は現在含まれていないため、**CaseDetailCreate** フォームの修正バージョンを示しています。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-255">This example shows a modified version of the **CaseDetailCreate** form, because the product currently includes no examples of forms that use this pattern.</span></span> 

<span data-ttu-id="b4fe4-256">[![クイックタブによるダイアログの例](./media/dialogform7.png)](./media/dialogform7.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-256">[![Example of dialog with FastTabs](./media/dialogform7.png)](./media/dialogform7.png)</span></span>

### <a name="dialog-wdouble-tabs"></a><span data-ttu-id="b4fe4-257">二重タブ付きダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-257">Dialog w/double tabs</span></span>

<span data-ttu-id="b4fe4-258">フォーム: **PurchTableReferences** (**買掛金勘定** &gt; **共通** &gt; **発注書** &gt; **すべての発注書**の順にクリックし、**一般** &gt; **関連情報** &gt; **関連する注文**の順にクリックします。)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-258">Form: **PurchTableReferences** (Click **Accounts payable** &gt; **Common** &gt; **Purchase orders** &gt; **All purchase orders**, and then click **General** &gt; **Related information** &gt; **Related orders**.)</span></span> 

<span data-ttu-id="b4fe4-259">[![ダブル タブによるダイアログの例](./media/dialogform8.png)](./media/dialogform8.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-259">[![Example of dialog with double tabs](./media/dialogform8.png)](./media/dialogform8.png)</span></span>

### <a name="dialog-read-only"></a><span data-ttu-id="b4fe4-260">ダイアログ (読み取り専用)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-260">Dialog (read only)</span></span>

<span data-ttu-id="b4fe4-261">フォーム: **SalesTablePostings** (**売掛金勘定** &gt; **共通** &gt; **販売注文** &gt; **すべての販売注文**の順にクリックし、**一般** &gt; **関連情報** &gt; **転記**の順にクリックします。)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-261">Form: **SalesTablePostings** (Click **Accounts receivable** &gt; **Common** &gt; **Sales orders** &gt; **All sales orders**, and then click **General** &gt; **Related information** &gt; **Postings**.)</span></span> 

<span data-ttu-id="b4fe4-262">[![ダイアログの例 (読み取り専用)](./media/dialogform9.png)](./media/dialogform9.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-262">[![Example of dialog (read only)](./media/dialogform9.png)](./media/dialogform9.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="b4fe4-263">付録</span><span class="sxs-lookup"><span data-stu-id="b4fe4-263">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="b4fe4-264">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b4fe4-264">Frequently asked questions</span></span>

<span data-ttu-id="b4fe4-265">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-265">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="b4fe4-266">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="b4fe4-266">Open issues</span></span>

-   <span data-ttu-id="b4fe4-267">**このパターンはダイアログの詳細リンクをどのように処理しますか。**</span><span class="sxs-lookup"><span data-stu-id="b4fe4-267">**How does this pattern handle the More info link in dialogs?**</span></span>
    -   <span data-ttu-id="b4fe4-268">**詳細**使用状況は、新しいパターンの追加を正当化する十分なケースがない限り、カスタム パターンと見なされます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-268">**More info** usage is assumed to be a custom pattern unless we have enough cases to justify the addition of a new pattern.</span></span>
-   <span data-ttu-id="b4fe4-269">**どのボタンでも使用するのではなく、CommandButtons を使用するよう強制的に OK/Cancel ボタンのパターンを修正する必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="b4fe4-269">**Should the pattern be modified to force OK/Cancel buttons to use CommandButtons instead of any button type?**</span></span>
    -   <span data-ttu-id="b4fe4-270">将来のこの変更の実行を検討しています。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-270">We will be looking at making this change in the future.</span></span>

### <a name="selecting-the-correct-dialog-width"></a><span data-ttu-id="b4fe4-271">正しいダイアログの幅を選択</span><span class="sxs-lookup"><span data-stu-id="b4fe4-271">Selecting the correct dialog width</span></span>

| <span data-ttu-id="b4fe4-272">コンテンツのタイプ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-272">Type of content</span></span>     | <span data-ttu-id="b4fe4-273">小さいダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-273">Small dialog</span></span>                                                                                                           | <span data-ttu-id="b4fe4-274">中間ダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-274">Medium dialog</span></span>                           | <span data-ttu-id="b4fe4-275">大きなダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-275">Large dialog</span></span>                              | <span data-ttu-id="b4fe4-276">完全なダイアログ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-276">Full dialog</span></span>                                                          | <span data-ttu-id="b4fe4-277">摘要</span><span class="sxs-lookup"><span data-stu-id="b4fe4-277">Notes</span></span>                                                                                                                                                                                                    |
|---------------------|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|-------------------------------------------|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fe4-278">コンテンツの列</span><span class="sxs-lookup"><span data-stu-id="b4fe4-278">Columns of content</span></span>  | <span data-ttu-id="b4fe4-279">スライダーは、コンテンツの 1 つの列を合わせます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-279">The slider fits one column of content.</span></span>                                                                                 | <span data-ttu-id="b4fe4-280">スライダーは 2 列のコンテンツに適合します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-280">The slider fits two columns of contents</span></span> | <span data-ttu-id="b4fe4-281">スライダーは 3 列のコンテンツに適合します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-281">The slider fits three columns of content.</span></span> | <span data-ttu-id="b4fe4-282">スライダーは、ビューポート幅からピークを引いた値に適合します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-282">The slider fits the viewport width minus peek.</span></span>                       | <span data-ttu-id="b4fe4-283">列の最大数は、列内のフィールドの幅に依存します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-283">The maximum number of columns depends on the width of the fields in the column.</span></span> <span data-ttu-id="b4fe4-284">したがって、幅は、*x* × 100% のフィールド サイズとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-284">Therefore, the width is defined as *x* × 100% field size.</span></span>                                                                |
| <span data-ttu-id="b4fe4-285">水平スクロール</span><span class="sxs-lookup"><span data-stu-id="b4fe4-285">Horizontal scroll</span></span>   | <span data-ttu-id="b4fe4-286">水平スクロールなし</span><span class="sxs-lookup"><span data-stu-id="b4fe4-286">No horizontal scrolling</span></span>                                                                                                | <span data-ttu-id="b4fe4-287">水平スクロールを避けてください。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-287">Avoid horizontal scrolling.</span></span>             | <span data-ttu-id="b4fe4-288">水平スクロールを避けてください。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-288">Avoid horizontal scrolling.</span></span>               | <span data-ttu-id="b4fe4-289">OK、コントロール ボタンおよびコミット ボタンが表示されている場合</span><span class="sxs-lookup"><span data-stu-id="b4fe4-289">OK, provided that the control buttons and commit buttons are visible</span></span> |                                                                                                                                                                                                          |
| <span data-ttu-id="b4fe4-290">垂直スクロール</span><span class="sxs-lookup"><span data-stu-id="b4fe4-290">Vertical scroll</span></span>     | <span data-ttu-id="b4fe4-291">一般的なシナリオでは垂直スクロールがありません (クイック タブは特殊なケースで展開できます)。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-291">No vertical scroll for typical scenarios (FastTabs can be expanded for special cases).</span></span> <span data-ttu-id="b4fe4-292">それ以外の場合、中規模なダイアログを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-292">Otherwise, use a Medium dialog.</span></span> | <span data-ttu-id="b4fe4-293">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-293">Yes</span></span>                                     | <span data-ttu-id="b4fe4-294">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-294">Yes</span></span>                                       | <span data-ttu-id="b4fe4-295">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-295">Yes</span></span>                                                                  | <span data-ttu-id="b4fe4-296">コンテンツの垂直スクロールを引き起こすためダイアログ内に大量のコンテンツを配置しないでください。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-296">Avoid putting so much content in the dialog that you cause vertical scrolling of the contents.</span></span> <span data-ttu-id="b4fe4-297">ダイアログが標準的な画面解像度で垂直方向にスクロールしている場合、ダイアログを大きくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-297">If your dialog is vertically scrolling at a typical screen resolution, you should make the dialog larger.</span></span> |
| <span data-ttu-id="b4fe4-298">クイック タブ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-298">FastTabs</span></span>            | <span data-ttu-id="b4fe4-299">強く非推奨</span><span class="sxs-lookup"><span data-stu-id="b4fe4-299">Strongly discouraged</span></span>                                                                                                   | <span data-ttu-id="b4fe4-300">OK だが非推奨</span><span class="sxs-lookup"><span data-stu-id="b4fe4-300">OK but discouraged</span></span>                      | <span data-ttu-id="b4fe4-301">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-301">Yes</span></span>                                       | <span data-ttu-id="b4fe4-302">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-302">Yes</span></span>                                                                  |                                                                                                                                                                                                          |
| <span data-ttu-id="b4fe4-303">タブ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-303">Tabs</span></span>                | <span data-ttu-id="b4fe4-304">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-304">Yes</span></span>                                                                                                                    | <span data-ttu-id="b4fe4-305">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-305">Yes</span></span>                                     | <span data-ttu-id="b4fe4-306">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-306">Yes</span></span>                                       | <span data-ttu-id="b4fe4-307">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-307">Yes</span></span>                                                                  | <span data-ttu-id="b4fe4-308">タブを切り替えたりクイック タブを展開したりしても、ダイアログ サイズがジャンプすることはありません。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-308">Switching tabs or expanding FastTabs should never cause jumps in the dialog size.</span></span> <span data-ttu-id="b4fe4-309">最大のタブ コンテンツは、ダイアログ サイズの選択を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-309">The largest tab content must define the choice of the dialog size.</span></span>                                                     |
| <span data-ttu-id="b4fe4-310">リスト/階層</span><span class="sxs-lookup"><span data-stu-id="b4fe4-310">List/hierarchy</span></span>      | <span data-ttu-id="b4fe4-311">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-311">Yes</span></span>                                                                                                                    | <span data-ttu-id="b4fe4-312">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-312">Yes</span></span>                                     | <span data-ttu-id="b4fe4-313">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-313">Yes</span></span>                                       | <span data-ttu-id="b4fe4-314">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-314">Yes</span></span>                                                                  |                                                                                                                                                                                                          |
| <span data-ttu-id="b4fe4-315">フィールド グループ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-315">Field groups</span></span>        | <span data-ttu-id="b4fe4-316">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-316">Yes</span></span>                                                                                                                    | <span data-ttu-id="b4fe4-317">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-317">Yes</span></span>                                     | <span data-ttu-id="b4fe4-318">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-318">Yes</span></span>                                       | <span data-ttu-id="b4fe4-319">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-319">Yes</span></span>                                                                  |                                                                                                                                                                                                          |
| <span data-ttu-id="b4fe4-320">入れ子になったフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-320">Nested field groups</span></span> | <span data-ttu-id="b4fe4-321">入り混じったレイアウト方向 (マトリックスまたは表形式のレイアウト) を持つ入れ子のフィールド グループなし</span><span class="sxs-lookup"><span data-stu-id="b4fe4-321">No nested field groups that have a mixed layout direction (matrix or tabular layout)</span></span>                                   | <span data-ttu-id="b4fe4-322">複数行レイアウト</span><span class="sxs-lookup"><span data-stu-id="b4fe4-322">Multiple-column layout</span></span>                  | <span data-ttu-id="b4fe4-323">複数行レイアウト</span><span class="sxs-lookup"><span data-stu-id="b4fe4-323">Multiple-column layout</span></span>                    | <span data-ttu-id="b4fe4-324">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-324">Yes</span></span>                                                                  |                                                                                                                                                                                                          |
| <span data-ttu-id="b4fe4-325">カスタム コントロール</span><span class="sxs-lookup"><span data-stu-id="b4fe4-325">Custom controls</span></span>     | <span data-ttu-id="b4fe4-326">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-326">Yes</span></span>                                                                                                                    | <span data-ttu-id="b4fe4-327">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-327">Yes</span></span>                                     | <span data-ttu-id="b4fe4-328">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-328">Yes</span></span>                                       | <span data-ttu-id="b4fe4-329">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-329">Yes</span></span>                                                                  |                                                                                                                                                                                                          |
| <span data-ttu-id="b4fe4-330">グリッド</span><span class="sxs-lookup"><span data-stu-id="b4fe4-330">Grid</span></span>                | <span data-ttu-id="b4fe4-331">はい、ただし水平スクロールなし</span><span class="sxs-lookup"><span data-stu-id="b4fe4-331">Yes, but no horizontal scrolling</span></span>                                                                                       | <span data-ttu-id="b4fe4-332">はい、ただし水平スクロールなし</span><span class="sxs-lookup"><span data-stu-id="b4fe4-332">Yes, but no horizontal scrolling</span></span>        | <span data-ttu-id="b4fe4-333">はい、ただし水平スクロールなし</span><span class="sxs-lookup"><span data-stu-id="b4fe4-333">Yes, but no horizontal scrolling</span></span>          | <span data-ttu-id="b4fe4-334">有</span><span class="sxs-lookup"><span data-stu-id="b4fe4-334">Yes</span></span>                                                                  | <span data-ttu-id="b4fe4-335">列の最大数は、列内のフィールドの幅に依存します。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-335">The maximum number of columns depends on the width of the fields in the column.</span></span> <span data-ttu-id="b4fe4-336">したがって、幅は、*x* × 100% のフィールド サイズにより定義されます。</span><span class="sxs-lookup"><span data-stu-id="b4fe4-336">Therefore, the width is defined by *x* × 100% field size.</span></span>                                                                |

### 

### <a name="ax-2012-content"></a><span data-ttu-id="b4fe4-337">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="b4fe4-337">AX 2012 content</span></span>

<span data-ttu-id="b4fe4-338">[![以前のバージョン コンテンツ](./media/dialogform10.png)](./media/dialogform10.png)</span><span class="sxs-lookup"><span data-stu-id="b4fe4-338">[![Previous version content](./media/dialogform10.png)](./media/dialogform10.png)</span></span>
