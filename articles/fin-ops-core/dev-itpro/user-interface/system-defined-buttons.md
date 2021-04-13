---
title: システム定義ボタン
description: このトピックでは、システム定義のボタンについて説明します。
author: jasongre
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28271
ms.assetid: 23b4dade-cb99-4c61-bd1e-cf2aeafddea4
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a1f16c3441eff80a5edb5ce547577c9da16d142
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744181"
---
# <a name="system-defined-buttons"></a><span data-ttu-id="3ea71-103">システム定義ボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-103">System-defined buttons</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ea71-104">このトピックでは、システム定義のボタンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-104">This topic describes the system-defined buttons.</span></span>

## <a name="overview"></a><span data-ttu-id="3ea71-105">概要</span><span class="sxs-lookup"><span data-stu-id="3ea71-105">Overview</span></span>

<span data-ttu-id="3ea71-106">システム定義のいくつかのボタンが、アクション ウィンドウに自動的に存在します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-106">Several system-defined buttons are automatically present on the Action Pane.</span></span> <span data-ttu-id="3ea71-107">一般に、これらのシステム定義ボタンは、エンドユーザーに適用され、使用可能な状態を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-107">In general, these system-defined buttons should be applicable and should kept available to the end user.</span></span> <span data-ttu-id="3ea71-108">ただし、まれなケースでは (たとえば、より専門的な管理が必要な場合、またはシステム定義ボタンが特定のフォームには役立たないまたは該当しない)、開発者は明確に抑制するまたはシステム定義ボタンを上書きする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-108">However, in rare cases (for example, if a more specialized control is required, or if a system-defined button isn't useful or applicable for a particular form), developers might have to explicitly suppress or override a system-defined button.</span></span> <span data-ttu-id="3ea71-109">たとえば、ある状況では、複数の「新規」オプションからユーザーが選択できるようにするメニュー ボタンは、システム定義された **新規** ボタンの方が望ましい場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-109">For example, in some situations, a MenuButton that lets the user select from multiple “New” options might be preferable to the system-defined **New** button.</span></span>

## <a name="list-of-system-defined-buttons"></a><span data-ttu-id="3ea71-110">システム定義ボタンのリスト</span><span class="sxs-lookup"><span data-stu-id="3ea71-110">List of system-defined buttons</span></span>
<span data-ttu-id="3ea71-111">次のテーブルは、システム定義ボタンの完全な一覧を示しています。</span><span class="sxs-lookup"><span data-stu-id="3ea71-111">The following tables give the full list of system-defined buttons.</span></span> <span data-ttu-id="3ea71-112">これらのテーブルは、条件付きまたは完全に抑制または上書きする必要がある場合に役立つ情報も提供します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-112">The tables also provide information that will be useful if these buttons must be conditionally or completely suppressed or overridden.</span></span>

### <a name="common-buttons"></a><span data-ttu-id="3ea71-113">一般的なボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-113">Common buttons</span></span>

| <span data-ttu-id="3ea71-114">ボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-114">Button</span></span>       | <span data-ttu-id="3ea71-115">ボタン名マクロ\*</span><span class="sxs-lookup"><span data-stu-id="3ea71-115">Button name macro\*</span></span>              | <span data-ttu-id="3ea71-116">コメント</span><span class="sxs-lookup"><span data-stu-id="3ea71-116">Comments</span></span>                                                                                             |
|--------------|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea71-117">輸出</span><span class="sxs-lookup"><span data-stu-id="3ea71-117">Export</span></span>       |                                  | <span data-ttu-id="3ea71-118">このボタンを抑制しないでください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-118">Don't suppress this button.</span></span>                                                                          |
| <span data-ttu-id="3ea71-119">添付</span><span class="sxs-lookup"><span data-stu-id="3ea71-119">Attach</span></span>       | <span data-ttu-id="3ea71-120">\#SystemDefinedAttachButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-120">\#SystemDefinedAttachButton</span></span>      | <span data-ttu-id="3ea71-121">添付ファイル用に設定されていないフォームでは表示しないため、このボタンを抑制しないでください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-121">Don't suppress this button, because we will suppress it on forms that aren't set up for attachments.</span></span> |
| <span data-ttu-id="3ea71-122">フィルターの表示</span><span class="sxs-lookup"><span data-stu-id="3ea71-122">Show filters</span></span> | <span data-ttu-id="3ea71-123">\#SystemDefinedShowFiltersButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-123">\#SystemDefinedShowFiltersButton</span></span> | <span data-ttu-id="3ea71-124">既定では、目次フォームは **表示**=**いいえ** になっています。</span><span class="sxs-lookup"><span data-stu-id="3ea71-124">By default, **Visible**=**No** on TOC forms.</span></span>                                                         |

<span data-ttu-id="3ea71-125">\* システム定義のボタン名マクロは、 SysSystemDefinedButtons マクロ ファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-125">\* System-defined button name macros are found in the SysSystemDefinedButtons macro file.</span></span>

### <a name="buttons-that-are-specific-to-details-forms"></a><span data-ttu-id="3ea71-126">詳細フォームに固有のボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-126">Buttons that are specific to Details forms</span></span>

<span data-ttu-id="3ea71-127">これらのボタンは、詳細フォームの経験の不可欠な部分です。</span><span class="sxs-lookup"><span data-stu-id="3ea71-127">These buttons are an integral part of the Details form experience.</span></span> <span data-ttu-id="3ea71-128">したがって、これらのボタンを非表示にする必要はほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-128">Therefore, it's very unlikely that you'll have to suppress these buttons.</span></span>

| <span data-ttu-id="3ea71-129">ボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-129">Button</span></span>              | <span data-ttu-id="3ea71-130">ボタン名マクロ\*</span><span class="sxs-lookup"><span data-stu-id="3ea71-130">Button name macro\*</span></span>                    | <span data-ttu-id="3ea71-131">コメント</span><span class="sxs-lookup"><span data-stu-id="3ea71-131">Comments</span></span>                                                |
|---------------------|----------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3ea71-132">ビューの変更</span><span class="sxs-lookup"><span data-stu-id="3ea71-132">Change view</span></span>         | <span data-ttu-id="3ea71-133">\#SystemDefinedShowMenuButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-133">\#SystemDefinedShowMenuButton</span></span>          | <span data-ttu-id="3ea71-134">このボタンは、**オプション** アクション ペイン タブの下にあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-134">This button exists under the **Options** Action Pane tab.</span></span> |
| <span data-ttu-id="3ea71-135">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="3ea71-135">Grid view</span></span>           | <span data-ttu-id="3ea71-136">\#SystemDefinedGridViewButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-136">\#SystemDefinedGridViewButton</span></span>          |                                                         |
| <span data-ttu-id="3ea71-137">詳細ビュー</span><span class="sxs-lookup"><span data-stu-id="3ea71-137">Details view</span></span>        | <span data-ttu-id="3ea71-138">\#SystemDefinedDetailsViewButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-138">\#SystemDefinedDetailsViewButton</span></span>       |                                                         |
| <span data-ttu-id="3ea71-139">行の詳細の表示</span><span class="sxs-lookup"><span data-stu-id="3ea71-139">Line details view</span></span>   | <span data-ttu-id="3ea71-140">\#SystemDefinedLineDetailsViewButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-140">\#SystemDefinedLineDetailsViewButton</span></span>   |                                                         |
| <span data-ttu-id="3ea71-141">ヘッダーの詳細ビュー</span><span class="sxs-lookup"><span data-stu-id="3ea71-141">Header details view</span></span> | <span data-ttu-id="3ea71-142">\#SystemDefinedHeaderDetailsViewButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-142">\#SystemDefinedHeaderDetailsViewButton</span></span> |                                                         |
| <span data-ttu-id="3ea71-143">リストを表示</span><span class="sxs-lookup"><span data-stu-id="3ea71-143">Show list</span></span>           | <span data-ttu-id="3ea71-144">\#SystemDefinedShowListButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-144">\#SystemDefinedShowListButton</span></span>          |                                                         |

<span data-ttu-id="3ea71-145">\* システム定義のボタン名マクロは、 SysSystemDefinedButtons マクロ ファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-145">\* System-defined button name macros are found in the SysSystemDefinedButtons macro file.</span></span>

## <a name="form-styles-that-have-no-system-defined-buttons"></a><span data-ttu-id="3ea71-146">システム定義ボタンのないフォーム スタイル</span><span class="sxs-lookup"><span data-stu-id="3ea71-146">Form styles that have no system-defined buttons</span></span>
<span data-ttu-id="3ea71-147">さまざまなフォーム スタイルについては、システム定義されたボタンの追加に意味がない主な理由は、これらのフォームが標準のアクション ウィンドウを持っていないことです。</span><span class="sxs-lookup"><span data-stu-id="3ea71-147">For several form styles, it doesn't make sense to add system-defined buttons, primarily because these forms don't have standard Action Panes.</span></span> <span data-ttu-id="3ea71-148">次のフォーム スタイルは、システム定義のボタンを受け取ることはありません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-148">The following form styles never receive system-defined buttons:</span></span>

-   <span data-ttu-id="3ea71-149">ダッシュボード</span><span class="sxs-lookup"><span data-stu-id="3ea71-149">Dashboard</span></span>
-   <span data-ttu-id="3ea71-150">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="3ea71-150">Dialog</span></span>
-   <span data-ttu-id="3ea71-151">DropDialog</span><span class="sxs-lookup"><span data-stu-id="3ea71-151">DropDialog</span></span>
-   <span data-ttu-id="3ea71-152">FormPart</span><span class="sxs-lookup"><span data-stu-id="3ea71-152">FormPart</span></span>
-   <span data-ttu-id="3ea71-153">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="3ea71-153">Lookup</span></span>
-   <span data-ttu-id="3ea71-154">サイトマップ</span><span class="sxs-lookup"><span data-stu-id="3ea71-154">Sitemap</span></span>
-   <span data-ttu-id="3ea71-155">ウィザード</span><span class="sxs-lookup"><span data-stu-id="3ea71-155">Wizard</span></span>

## <a name="suppressing-most-or-all-of-the-system-defined-buttons"></a><span data-ttu-id="3ea71-156">システム定義のボタンの大部分またはすべてを非表示</span><span class="sxs-lookup"><span data-stu-id="3ea71-156">Suppressing most or all of the system-defined buttons</span></span>
<span data-ttu-id="3ea71-157">フォーム上のシステム定義ボタンのほとんどまたはすべてを非表示にしている場合は、フォームのスタイル (**Form.Design.Style**) またはパターンを再確認し、フォームの目的を再検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-157">If you find that you're suppressing most or all of the system-defined buttons on a form, you should reexamine your form style (**Form.Design.Style**) or pattern, and reconsider the purpose of the form.</span></span> <span data-ttu-id="3ea71-158">代わりにフォームをダイアログにすべきでしょうか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-158">Should the form be a dialog instead?</span></span> <span data-ttu-id="3ea71-159">(デフォルトでは、ダイアログにはシステム定義のボタンは表示されません。) 多くの場合、このような状況でのフォームは **スタイル**=**自動** であり、ダイアログとしてはより適切です。</span><span class="sxs-lookup"><span data-stu-id="3ea71-159">(By default, dialogs don't receive any system-defined buttons.) Often, forms that are in this situation have **Style**=**Auto** and would be more appropriate as dialogs.</span></span> <span data-ttu-id="3ea71-160">フォームを技術的にダイアログにする必要がある場合、同時にすべてのシステム定義されたボタンを自動的に非表示にできるメタデータまたはコードは現在ありません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-160">If your form should not technically be a dialog, there is no currently no metadata or code that can automatically suppress all the system-defined buttons at the same time.</span></span> <span data-ttu-id="3ea71-161">フォームをシステム定義のボタンを受け取らないフォーム スタイルに切り替える場合を除き、各ボタンを個別に抑制/オーバーライドにする必要があります (この記事の他のセクションを参照)。</span><span class="sxs-lookup"><span data-stu-id="3ea71-161">Unless you switch the form to a form style that doesn't receive any system-defined buttons, you must to suppress/override each button individually (see the other sections in this article).</span></span> <span data-ttu-id="3ea71-162">このシナリオは非常に稀です。</span><span class="sxs-lookup"><span data-stu-id="3ea71-162">This scenario should be extremely rare.</span></span>

## <a name="new-and-delete-system-buttons"></a><span data-ttu-id="3ea71-163">新規システムおよびシステムの削除のボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-163">New and Delete system buttons</span></span>
<span data-ttu-id="3ea71-164">**新規** および **削除** ボタンは、現在カーネルによって追加され、特殊なメタデータ プロパティを使用して制御されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-164">The **New** and **Delete** buttons are currently added by the kernel, and are controlled via special metadata properties.</span></span> <span data-ttu-id="3ea71-165">これらのボタンは、常にフォーム上の最初のマスター データソースで機能します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-165">These buttons always work on the first master data source on the form.</span></span>

### <a name="when-are-these-buttons-available-by-default"></a><span data-ttu-id="3ea71-166">これらのボタンは既定ではいつ有効になりますか</span><span class="sxs-lookup"><span data-stu-id="3ea71-166">When are these buttons available by default?</span></span>

<span data-ttu-id="3ea71-167">フォームには通常、システム定義された **新規** および **削除** ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-167">Forms usually have system-defined **New** and **Delete** buttons.</span></span> <span data-ttu-id="3ea71-168">これらのボタンは、次の条件でフォームに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-168">These buttons appear on a form under the following conditions:</span></span>

-   <span data-ttu-id="3ea71-169">フォームには、システム定義のボタンを使用できるスタイルがあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-169">The form has a style that allows for system-defined buttons.</span></span>
-   <span data-ttu-id="3ea71-170">フォームには 1 つ以上のデータ ソースがあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-170">There is at least one data source on the form.</span></span>

### <a name="how-do-i-affect-the-visibility-of-the-new-and-delete-buttons-on-a-form-but-still-allow-the-standard-new-and-delete-tasks-to-fire-via-keyboard-shortcuts"></a><span data-ttu-id="3ea71-171">フォームの新規および削除ボタンの表示にどのように影響を与えますか。ただしキーボードのショートカットを介して標準の新規および削除タスクを起動できますか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-171">How do I affect the visibility of the New and Delete buttons on a form, but still allow the standard New and Delete tasks to fire via keyboard shortcuts?</span></span>

<span data-ttu-id="3ea71-172">フォームでの **新規** ボタンと **削除** ボタンの表示/非表示を制御するには、**Form.Design** の **ShowNewButton** および **ShowDeleteButton** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-172">Use the **ShowNewButton** and **ShowDeleteButton** properties on **Form.Design** to control the visibility of the **New** and **Delete** buttons on a form.</span></span> <span data-ttu-id="3ea71-173">データ ソースでユーザーがまだレコードを作成して削除できる場合、キーボード ショートカットはシステム ボタンが表示されない場合でも引き続き機能することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-173">Note that if the data sources still let the user create and delete records, the keyboard shortcuts will continue to work even if the system buttons aren't visible.</span></span>

| <span data-ttu-id="3ea71-174">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ea71-174">Property</span></span>                     | <span data-ttu-id="3ea71-175">先頭値</span><span class="sxs-lookup"><span data-stu-id="3ea71-175">Value</span></span> | <span data-ttu-id="3ea71-176">説明</span><span class="sxs-lookup"><span data-stu-id="3ea71-176">Description</span></span>                                                |
|------------------------------|-------|------------------------------------------------------------|
| <span data-ttu-id="3ea71-177">Form.Design.ShowNewButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-177">Form.Design.ShowNewButton</span></span>    | <span data-ttu-id="3ea71-178">無</span><span class="sxs-lookup"><span data-stu-id="3ea71-178">No</span></span>    | <span data-ttu-id="3ea71-179">フォーム上でシステム定義の **新規** ボタンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-179">Suppress the system-defined **New** button on the form.</span></span>    |
| <span data-ttu-id="3ea71-180">Form.Design.ShowDeleteButton</span><span class="sxs-lookup"><span data-stu-id="3ea71-180">Form.Design.ShowDeleteButton</span></span> | <span data-ttu-id="3ea71-181">無</span><span class="sxs-lookup"><span data-stu-id="3ea71-181">No</span></span>    | <span data-ttu-id="3ea71-182">フォーム上でシステム定義の **削除** ボタンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-182">Suppress the system-defined **Delete** button on the form.</span></span> |

### <a name="how-do-i-affect-the-state-enableddisabled-of-the-new-and-delete-buttons-and-the-associated-task-behavior-on-a-form"></a><span data-ttu-id="3ea71-183">新規および削除ボタンの状態 (有効/無効)、およびフォームで関連するタスクの動作にどのように影響しますか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-183">How do I affect the state (enabled/disabled) of the New and Delete buttons, and the associated task behavior on a form?</span></span>

<span data-ttu-id="3ea71-184">フォーム上の **新規** および **削除** ボタンの状態と、関連するタスクの動作の両方に影響を及ぼすには、**AllowCreate** と **AllowDelete** のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-184">To affect both the state of the **New** and **Delete** buttons and the associated task behavior on a form, use the **AllowCreate** and **AllowDelete** properties on the first master data source.</span></span> <span data-ttu-id="3ea71-185">また、このアプローチを使用して、**新規** と **削除** ボタンを無効にする場合、関連付けられているキーボード ショートカットは無効になります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-185">Additionally, the associated keyboard shortcuts will have no effect if you use this approach to disable the **New** and **Delete** buttons.</span></span>

| <span data-ttu-id="3ea71-186">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ea71-186">Property</span></span>                                                   | <span data-ttu-id="3ea71-187">先頭値</span><span class="sxs-lookup"><span data-stu-id="3ea71-187">Value</span></span> | <span data-ttu-id="3ea71-188">説明</span><span class="sxs-lookup"><span data-stu-id="3ea71-188">Description</span></span>                                                                                                  |
|------------------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea71-189">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowCreate</span><span class="sxs-lookup"><span data-stu-id="3ea71-189">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowCreate</span></span> | <span data-ttu-id="3ea71-190">無</span><span class="sxs-lookup"><span data-stu-id="3ea71-190">No</span></span>    | <span data-ttu-id="3ea71-191">フォームはレコードの作成を許可しません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-191">The form doesn't allow record creation.</span></span> <span data-ttu-id="3ea71-192">フォームに無効なシステム定義の **新規** ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-192">The form has a disabled system-defined **New** button.</span></span>               |
| <span data-ttu-id="3ea71-193">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowCreate</span><span class="sxs-lookup"><span data-stu-id="3ea71-193">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowCreate</span></span> | <span data-ttu-id="3ea71-194">有</span><span class="sxs-lookup"><span data-stu-id="3ea71-194">Yes</span></span>   | <span data-ttu-id="3ea71-195">このフォームはレコードの作成を可能にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-195">The form allows record creation.</span></span> <span data-ttu-id="3ea71-196">フォームには、システム定義の **新規** ボタンが有効になっています (表示されている場合)。</span><span class="sxs-lookup"><span data-stu-id="3ea71-196">The form has an enabled system-defined **New** button (if it's visible).</span></span>    |
| <span data-ttu-id="3ea71-197">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowDelete</span><span class="sxs-lookup"><span data-stu-id="3ea71-197">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowDelete</span></span> | <span data-ttu-id="3ea71-198">無</span><span class="sxs-lookup"><span data-stu-id="3ea71-198">No</span></span>    | <span data-ttu-id="3ea71-199">フォームはレコードの削除を許可しません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-199">The form doesn't allow record deletion.</span></span> <span data-ttu-id="3ea71-200">フォームに無効なシステム定義の **削除** ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-200">The form has a disabled system-defined **Delete** button.</span></span>            |
| <span data-ttu-id="3ea71-201">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowDelete</span><span class="sxs-lookup"><span data-stu-id="3ea71-201">Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowDelete</span></span> | <span data-ttu-id="3ea71-202">有</span><span class="sxs-lookup"><span data-stu-id="3ea71-202">Yes</span></span>   | <span data-ttu-id="3ea71-203">このフォームはレコードの削除を可能にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-203">The form allows record deletion.</span></span> <span data-ttu-id="3ea71-204">フォームには、システム定義の **削除** ボタンが有効になっています (表示されている場合)。</span><span class="sxs-lookup"><span data-stu-id="3ea71-204">The form has an enabled system-defined **Delete** button (if it's visible).</span></span> |

> [!NOTE]
> <span data-ttu-id="3ea71-205">フォームに新規レコード アクションがある場合、ボタン コントロールはシステム定義の **新規** ボタンの有効状態を上書きします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-205">If the form has a New record action, that button control overrides the enabled state of the system-defined **New** button.</span></span>

### <a name="how-do-i-change-the-behavior-of-the-new-task-either-by-clicking-the-button-or-by-using-the-keyboard-shortcut"></a><span data-ttu-id="3ea71-206">新しいタスク (ボタンをクリックするまたはキーボード ショートカットを使用するかのいずれか) の動作をどのように変更しますか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-206">How do I change the behavior of the New task (either by clicking the button or by using the keyboard shortcut)?</span></span>

<span data-ttu-id="3ea71-207">新しいタスクの動作を変更するメカニズムは 3 つあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-207">There are three mechanisms for changing the behavior of the New task:</span></span>

- <span data-ttu-id="3ea71-208">**新しいレコード アクション** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-208">Use the **New Record Action** property.</span></span> <span data-ttu-id="3ea71-209">このプロパティは、現在、**Form.Design** でのみ使用可能であり、フォーム上で **New** コマンドを呼び出す **すべての** CommandButton (セカンダリ コレクションにバインドされている CommandButtons も含まれる) に対して参照されたアクションがトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-209">This property is currently available only on **Form.Design**, and the referenced action will be triggered for **all** CommandButtons that call the **New** command on the form, even CommandButtons that are bound to secondary collections.</span></span> <span data-ttu-id="3ea71-210">今後、**新しいレコード アクション** プロパティがすべてのコンテナー コントロールに配置され、プロパティのスコープにわたるコントロールが向上します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-210">In the future, the **New Record Action** property will be placed on all container controls to provide better control over the property's scope.</span></span> <span data-ttu-id="3ea71-211">現時点では、**新しいレコード アクション** プロパティもメニュー ボタンまたはドロップ ダイアログ ボタンとして定義できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-211">Note that, currently, the **New Record Action** property also can't be defined as a Menu Button or Drop Dialog Button.</span></span>

  |          <span data-ttu-id="3ea71-212">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ea71-212">Property</span></span>           |             <span data-ttu-id="3ea71-213">先頭値</span><span class="sxs-lookup"><span data-stu-id="3ea71-213">Value</span></span>              |                              <span data-ttu-id="3ea71-214">説明</span><span class="sxs-lookup"><span data-stu-id="3ea71-214">Description</span></span>                              |
  |-----------------------------|--------------------------------|-----------------------------------------------------------------------|
  | <span data-ttu-id="3ea71-215">Form.Design.NewRecordAction</span><span class="sxs-lookup"><span data-stu-id="3ea71-215">Form.Design.NewRecordAction</span></span> | <span data-ttu-id="3ea71-216">フォームからのコントロール名</span><span class="sxs-lookup"><span data-stu-id="3ea71-216">The control name from the form</span></span> | <span data-ttu-id="3ea71-217">このプロパティは、指定されたアクションを実行するための新規タスクをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-217">This property overrides the New task to perform the specified action.</span></span> |


- <span data-ttu-id="3ea71-218">(推奨)イベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-218">(Recommended) Use eventing.</span></span> <span data-ttu-id="3ea71-219">特に、レコードの作成と削除の前後に実行することを意図したコードを配置できる場合、これらのアクションのプリイベントとポストイベントがあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-219">In particular, there are pre-events and post-events for record creation and deletion, where you can put code that is meant to run before and after these actions.</span></span> <span data-ttu-id="3ea71-220">以下のコード例をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-220">See the following code example.</span></span>

    ```xpp
    [Form]
    public class Form1 extends FormRun
    {
        public void init()
        {
            super();
            element.dataHelper().RecordCreating += eventhandler(this.PreRecordCreate);
            element.dataHelper().RecordCreated  += eventhandler(this.PostRecordCreate);
            // similar methods exist for deletion:
            // element.dataHelper().RecordDeleting, element.dataHelper().RecordDeleted
            //
            // explicit actions can be triggered via:
            // element.dataHelper().RecordCreate(), element.dataHelper().RecordDelete()        
        }
        public void PreRecordCreate(FormRunServiceArgs _cancellableArgs)
        {
            //  I can add my logic here that gets invoked before the global creation task
            // if I need to, I can cancel the "super" of the task by doing:
            // _cancellableArgs.cancel()
        }
        public void PostRecordCreate()
        {
            //  I can add my logic here that gets invoked after the global creation task
        }
    }
    ```

- <span data-ttu-id="3ea71-221">対応するデータ ソースの、**create()** または **delete()** メソッドで上書きを作成します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-221">Create an override on the **create()** or **delete()** method on the corresponding data source.</span></span>

### <a name="how-do-i-change-the-behavior-of-the-new-button-but-not-the-task"></a><span data-ttu-id="3ea71-222">新しいボタン (ただしタスクではない) の動作をどのように変更しますか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-222">How do I change the behavior of the New button (but not the task)?</span></span>

<span data-ttu-id="3ea71-223">システム定義された **新規** ボタンを、複数の「新規」オプションからユーザーに選択させるメニュー ボタンに置き変える場合を考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="3ea71-223">Imagine that you want to replace the system-defined **New** button with a menu button that lets the user select among several "New" options.</span></span> <span data-ttu-id="3ea71-224">したがって、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-224">Therefore, you complete the following tasks:</span></span>

1.  <span data-ttu-id="3ea71-225">システム定義された **新規** ボタンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-225">Hide the system-defined **New** button.</span></span>
2.  <span data-ttu-id="3ea71-226">新しいアクションに対する独自のボタンをモデル化します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-226">Model your own button for the New action.</span></span>

<span data-ttu-id="3ea71-227">ただし、この時点で、キーボード ショートカットが呼び出されると、新規のシステム動作も起動します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-227">However, at this point, the system-behavior for New still fires when the keyboard shortcut is invoked.</span></span> <span data-ttu-id="3ea71-228">キーボード ショートカットを押したときにモデル化された **新規** ボタンを起動するようにするには、このボタンを **Form.Design** の NewRecordAction として設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-228">If you want to make this modeled **New** button fire when the keyboard shortcut is pressed, you must set this button as the NewRecordAction on **Form.Design**.</span></span> <span data-ttu-id="3ea71-229">前のセクションで触れたように、アクションは現在フォーム上の新しいタスクを呼び出すすべての CommandButtons に対して起動されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-229">As we noted in the previous section, the action will currently be fired for all CommandButtons that call the New task on the form.</span></span> <span data-ttu-id="3ea71-230">したがって、このアプローチは、複数のデータソースを持つフォームでは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-230">Therefore, you should not use this approach on forms that have multiple data sources.</span></span>

## <a name="edit-done-save-and-restore-system-buttons"></a><span data-ttu-id="3ea71-231">編集、実行、保存、およびシステム ボタンを復元</span><span class="sxs-lookup"><span data-stu-id="3ea71-231">Edit, Done, Save, and Restore system buttons</span></span>

<span data-ttu-id="3ea71-232">**編集**、**実行**、**保存**、および **復元** ボタンでは、ユーザーが必要に応じてフォームの編集モードを切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-232">The **Edit**, **Done**, **Save**, and **Restore** buttons let users switch the edit mode of the form as they require.</span></span> <span data-ttu-id="3ea71-233">この機能は重要であるため、これらのボタンは現在抑制できません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-233">Because this capability is critical, these buttons can't currently be suppressed.</span></span> <span data-ttu-id="3ea71-234">ただし、フォームが常に **編集** モードまたは **表示** モードである必要がある場合、**ViewEditMode** プロパティを使用して効果を達成でき、ボタンはフォームに表示されません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-234">However, if a form should always be in **Edit** mode or should always be in **View** mode, you can use the **ViewEditMode** property to achieve that effect, and the buttons won't appear on the form.</span></span> <span data-ttu-id="3ea71-235">ほとんどのフォームが **ViewEditMode**=**Auto** のままになることに注意してください。フォームが読み取り専用の場合、または常に編集可能になる場合を除いて、純粋に外観上の理由で **ViewEditMode**=**View** または **ViewEditMode=Edit** に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-235">Note that most forms should be left as **ViewEditMode**=**Auto**. Don't set **ViewEditMode**=**View** or **ViewEditMode=Edit** for purely cosmetic reasons, but only if the form will always be read-only or will always be editable.</span></span>

| <span data-ttu-id="3ea71-236">Form.Design.ViewEditMode</span><span class="sxs-lookup"><span data-stu-id="3ea71-236">Form.Design.ViewEditMode</span></span> | <span data-ttu-id="3ea71-237">フォーム動作</span><span class="sxs-lookup"><span data-stu-id="3ea71-237">Form behavior</span></span>                                                     | <span data-ttu-id="3ea71-238">システム定義ボタンの動作</span><span class="sxs-lookup"><span data-stu-id="3ea71-238">System-defined button behavior</span></span>                                                                                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea71-239">表示</span><span class="sxs-lookup"><span data-stu-id="3ea71-239">View</span></span>                     | <span data-ttu-id="3ea71-240">フォームは常に **表示** モードです。</span><span class="sxs-lookup"><span data-stu-id="3ea71-240">The form is always in **View** mode.</span></span>                              | <span data-ttu-id="3ea71-241">フレームワークが必要ではないとみなすため、これらのボタン (**編集**、**完了**、**保存**、および **復元**) のいずれも表示されません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-241">None of these buttons (**Edit**, **Done**, **Save**, and **Restore**) are shown, because the framework assumes that they aren't needed.</span></span>                                                                                               |
| <span data-ttu-id="3ea71-242">編集</span><span class="sxs-lookup"><span data-stu-id="3ea71-242">Edit</span></span>                     | <span data-ttu-id="3ea71-243">フォームは常に **編集** モードです。</span><span class="sxs-lookup"><span data-stu-id="3ea71-243">The form is always in **Edit** mode.</span></span>                              | <span data-ttu-id="3ea71-244">**保存** および **元に戻す** ボタンのみが表示されるのは、ユーザーが **編集** モードを終了することができないからです。</span><span class="sxs-lookup"><span data-stu-id="3ea71-244">Only the **Save** and **Revert** buttons are shown, because the user can't exit **Edit** mode.</span></span> <span data-ttu-id="3ea71-245">**元に戻す** ボタンは、フレームワークによって指定された **オプション** タブにあります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-245">The **Revert** button is on the framework-provided **Options** tab.</span></span>                                                                    |
| <span data-ttu-id="3ea71-246">自動</span><span class="sxs-lookup"><span data-stu-id="3ea71-246">Auto</span></span>                     | <span data-ttu-id="3ea71-247">フォームは、**表示** モードと **編集** モードの間で切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-247">The form can be switched between **View** mode and **Edit** mode.</span></span> | <span data-ttu-id="3ea71-248">**表示** モードでは、**編集** ボタンはアクション ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-248">In **View** mode, the **Edit** button is shown on the Action Pane.</span></span> <span data-ttu-id="3ea71-249">**編集** モードでは、**保存** ボタンはアクション ウィンドウに表示されており、**読み取りモード** および **元に戻す** ボタンはフレームワークによって指定された **オプション** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-249">In **Edit** mode, the **Save** button is shown on the Action Pane, and the **Read mode** and **Revert** buttons are shown on the framework-provided **Options** tab.</span></span> |

### <a name="can-i-conditionally-suppress-or-show-the-edit-button"></a><span data-ttu-id="3ea71-250">条件付きで 編集ボタンを隠すまたは表示できますか？</span><span class="sxs-lookup"><span data-stu-id="3ea71-250">Can I conditionally suppress or show the Edit button?</span></span>

<span data-ttu-id="3ea71-251">あるポイントでフォームが編集可能で、他のポイントで読み取り専用にすると、ユーザーがフォームを編集できるかどうかを判断するロジックを使用して、実行時に **ViewEditMode** プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-251">If a form is editable at some points and read-only at other points, the logic that is used to determine whether the user can edit the form can be used to set the **ViewEditMode** property at run time.</span></span> <span data-ttu-id="3ea71-252">フォームを読み取り専用にする必要があるときは、**ViewEditMode**=**表示** を設定します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-252">When the form should be read-only, set **ViewEditMode**=**View**.</span></span> <span data-ttu-id="3ea71-253">フォームの編集または表示のいずれかができるとき、**ViewEditMode**=**自動** を設定します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-253">When the form can be either edited or viewed, set **ViewEditMode**=**Auto**.</span></span>

### <a name="how-do-i-run-additional-code-when-the-edit-button-is-clicked"></a><span data-ttu-id="3ea71-254">編集ボタンをクリックするときに追加コードを実行するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-254">How do I run additional code when the Edit button is clicked?</span></span>

<span data-ttu-id="3ea71-255">**編集** ボタンをクリックしたときに追加のコードを実行させるには、イベントを使用します (「新しいタスクの動作を変更する方法 (ボタンをクリックするか、キーボード ショートカットを使用する)」の例を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="3ea71-255">To have additional code run when the user clicks the **Edit** button, use eventing (see the example in the "How do I change the behavior of the New task (either by clicking the button or by using the keyboard shortcut)?"</span></span> <span data-ttu-id="3ea71-256">この記事の前半のセクション)。</span><span class="sxs-lookup"><span data-stu-id="3ea71-256">section earlier in this article).</span></span> <span data-ttu-id="3ea71-257">具体的には、次のイベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-257">Specifically, use the following events:</span></span>

-   <span data-ttu-id="3ea71-258">現在の表示/編集モードの切替えをサブスクライブするには、次のイベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-258">To subscribe to view/edit mode switching, use these events:</span></span>
    -   <span data-ttu-id="3ea71-259">element.viewEditModeHelper().EditModeSwitching</span><span class="sxs-lookup"><span data-stu-id="3ea71-259">element.viewEditModeHelper().EditModeSwitching</span></span>
    -   <span data-ttu-id="3ea71-260">element.viewEditModeHelper().EditModeSwitche</span><span class="sxs-lookup"><span data-stu-id="3ea71-260">element.viewEditModeHelper().EditModeSwitche</span></span>
-   <span data-ttu-id="3ea71-261">現在の表示/編集モードを照会するには、次のイベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-261">To query the current view/edit mode, use these events:</span></span>
    -   <span data-ttu-id="3ea71-262">element.viewEditModeHelper().isInEditMode()</span><span class="sxs-lookup"><span data-stu-id="3ea71-262">element.viewEditModeHelper().isInEditMode()</span></span>
    -   <span data-ttu-id="3ea71-263">element.viewEditModeHelper().IsInViewMode()</span><span class="sxs-lookup"><span data-stu-id="3ea71-263">element.viewEditModeHelper().IsInViewMode()</span></span>
-   <span data-ttu-id="3ea71-264">現在の表示/編集モードの切替えをトリガーするには、次のイベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-264">To trigger view/edit mode switching, use these events:</span></span>
    -   <span data-ttu-id="3ea71-265">element.viewEditModeHelper().setViewEditMode(ViewEditMode::Edit)</span><span class="sxs-lookup"><span data-stu-id="3ea71-265">element.viewEditModeHelper().setViewEditMode(ViewEditMode::Edit)</span></span>

## <a name="refresh-popout-and-close-system-buttons"></a><span data-ttu-id="3ea71-266">[更新]、[ポップアウト]、[閉じる] システム ボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-266">Refresh, Popout, and Close system buttons</span></span>
<span data-ttu-id="3ea71-267">**更新**、**ポップアウト**、および **閉じる** ボタンは、アクション ウィンドウの右側にあるシステム ボタンです。</span><span class="sxs-lookup"><span data-stu-id="3ea71-267">The **Refresh**, **Popout**, and **Close** buttons are system buttons that are located on the right side of the Action Pane.</span></span> <span data-ttu-id="3ea71-268">**更新** ボタンは、フォーム上のすべてのデータを更新するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-268">The **Refresh** button is used to refresh all data on the form.</span></span> <span data-ttu-id="3ea71-269">**ポップアウト** ボタンを使用すると、現在のフォームが別のウィンドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-269">The **Popout** button is used to move the current form into a separate window.</span></span> <span data-ttu-id="3ea71-270">**閉じる** ボタンは、フォームを閉じます (基本的に、このボタンはブラウザの **戻る** ボタンをクリックします)。</span><span class="sxs-lookup"><span data-stu-id="3ea71-270">The **Close** button closes the form (essentially, this button clicks the browser's **Back** button).</span></span> <span data-ttu-id="3ea71-271">これらのシステム ボタンは不可欠なコンポーネントであり、現時点では抑制することはできません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-271">These system buttons are integral components and can't currently be suppressed.</span></span>

## <a name="other-system-defined-buttons"></a><span data-ttu-id="3ea71-272">他のシステム定義ボタン</span><span class="sxs-lookup"><span data-stu-id="3ea71-272">Other system-defined buttons</span></span>
<span data-ttu-id="3ea71-273">残りのシステム定義のボタンは **Form.Init** 中に追加されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-273">The remaining system-defined buttons are added during **Form.Init**.</span></span> <span data-ttu-id="3ea71-274">同じ名前のコントロールが存在しない場合にのみ追加されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-274">They are added only if a control of the same name doesn't already exist.</span></span>

### <a name="how-do-i-run-additional-code-together-with-a-system-defined-button-or-change-the-behavior-of-the-button"></a><span data-ttu-id="3ea71-275">システム定義されたボタンと共に追加コードを実行する、またはボタンの動作を変更するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-275">How do I run additional code together with a system-defined button or change the behavior of the button?</span></span>

-   <span data-ttu-id="3ea71-276">表示切り替えボタン (たとえば、グリッド ビュー、詳細ビュー、ヘッダービュー、または明細行ビューに切り替えるボタン) については、個々の TabPage で **pageActivated()** メソッドを上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-276">For view switching buttons (for example, buttons that switch to the grid view, details view, header view, or lines view), you should override the **pageActivated()** method on the individual TabPage.</span></span>
-   <span data-ttu-id="3ea71-277">プリイベント/ポストイベントを持つシステム定義されたボタン (たとえば、**新規**、**削除**、および **編集**) については、適切なイベントにサブスクライブすることができます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-277">For system-defined buttons that have pre-eventing/post-eventing (for example, **New**, **Delete**, and **Edit**), you can subscribe to the appropriate events.</span></span> <span data-ttu-id="3ea71-278">これらのボタンの特定のイベントについては、**新規作成**/**削除** ボタンと **編集** ボタンの対応するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ea71-278">See the corresponding sections for **New**/**Delete** and **Edit** buttons for information about specific events for those buttons.</span></span>
-   <span data-ttu-id="3ea71-279">タスクを直接呼び出さないシステム定義のボタン (たとえば、**SystemDefinedShowMenuButton** および **SystemDefinedShowListButton**) については、**registerOverrideMethod()** の呼び出しを通してボタンの上書きを登録でき、システム定義ボタンをクリックしたときに追加コードが実行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-279">For system-defined buttons that don't call a task directly (for example, **SystemDefinedShowMenuButton** and **SystemDefinedShowListButton**), you can register an override on the button through a **registerOverrideMethod()** call to have additional code run when the system-defined button is clicked.</span></span>

    ```xpp
    public void overrideFunction(FormCommandButtonControl _command)
        {
            // Put any pre-super code here 
            // This serves as the call to super()
            _command.clicked(); 
            // Put any post-super code here
        }
    ```

### <a name="how-do-i-suppress-any-of-these-system-defined-buttons-on-a-form-but-without-suppressing-any-corresponding-task"></a><span data-ttu-id="3ea71-280">対応するタスクを抑制することなく、フォーム上のこれらのシステム定義されたボタンのいずれかを抑制するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="3ea71-280">How do I suppress any of these system-defined buttons on a form, but without suppressing any corresponding task?</span></span>

<span data-ttu-id="3ea71-281">一般に、システム ボタンのいずれかを非表示にすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="3ea71-281">In general, we don't recommend that you suppress any of the system buttons.</span></span> <span data-ttu-id="3ea71-282">それらの存在は、フォーム上のアクションに一貫性をもたらします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-282">Their presence provides consistency to actions on forms.</span></span> <span data-ttu-id="3ea71-283">ただし、それが役立たないある状況によっては、ボタンが現在表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-283">However, the buttons currently appear in some situations where they aren't as useful.</span></span> <span data-ttu-id="3ea71-284">これらの状況の多くに対処する将来の作業項目があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-284">We have future work items to address many of these situations.</span></span> <span data-ttu-id="3ea71-285">たとえば、次のタスクの作業項目があります。</span><span class="sxs-lookup"><span data-stu-id="3ea71-285">For example, have work items for the following tasks:</span></span>

-   <span data-ttu-id="3ea71-286">添付ファイルを許可するように構成されていないフォームで **添付** ボタンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-286">Suppress the **Attach** button on forms that aren't configured to allow attachments.</span></span>
-   <span data-ttu-id="3ea71-287">グリッドがないフォームで **エクスポート** ボタンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-287">Suppress the **Export** button on forms that have no grids.</span></span>
-   <span data-ttu-id="3ea71-288">メイン グリッドがないフォームで **フィルターを表示する** ボタンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3ea71-288">Suppress the **Show filters** button on forms that don't have a main grid.</span></span>

<span data-ttu-id="3ea71-289">ただし、これらのボタンのいずれかを抑制する必要がある場合 (決して推奨しません)、次のコード例に示すように、コードを通してコントロールを検索し、可視性を **false** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3ea71-289">However, if you must suppress one of these buttons (strongly discouraged), you can find the control via code and set its visibility to **false**, as shown in the following code example.</span></span> <span data-ttu-id="3ea71-290">利用可能な場合、SysSystemDefinedButtons マクロを使用して、ボタン名を参照します。</span><span class="sxs-lookup"><span data-stu-id="3ea71-290">Use SysSystemDefinedButtons macros, where they are available, to reference the button names.</span></span>

```xpp
FormCommandButtonControl attachButton;

    public void init()
    {
        #SysSystemDefinedButtons

        super();

        attachButton= this.control(this.controlId(#SystemDefinedAttachButton)) as FormCommandButtonControl; 
        attachButton.visible(false); 
    }
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]