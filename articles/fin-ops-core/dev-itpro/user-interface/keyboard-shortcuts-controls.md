---
title: 拡張可能なコントロールのキーボード ショートカット
description: このトピックでは、拡張可能なコントロールのキーボード ショートカットを実装するための推奨される方法について説明します。
author: robinarh
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: C0E2E0F9-19C1-4CE0-A81C-1ACFA841F6AB
ms.search.region: Global
ms.author: robinarh
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: a071d08fcc97ebe18b89ab404b37ecd27d39797e
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329880"
---
# <a name="keyboard-shortcuts-for-extensible-controls"></a><span data-ttu-id="0c70d-103">拡張可能なコントロールのキーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="0c70d-103">Keyboard shortcuts for extensible controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c70d-104">キーボード ショートカットは、拡張可能コントロールを作成するときの重要な考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="0c70d-104">Keyboard shortcuts are an important consideration when you create any extensible control.</span></span> <span data-ttu-id="0c70d-105">このトピックでは、拡張可能なコントロールのキーボード ショートカットを選択するのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-105">This topic provides information that will help you choose keyboard shortcuts for your extensible controls.</span></span> <span data-ttu-id="0c70d-106">また、拡張可能なコントロールのキーボード ショートカットを実装するための推奨される方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-106">It also outlines the recommended method for implementing keyboard shortcuts for extensible controls.</span></span>

## <a name="overview"></a><span data-ttu-id="0c70d-107">概要</span><span class="sxs-lookup"><span data-stu-id="0c70d-107">Overview</span></span>
<span data-ttu-id="0c70d-108">アクセシビリティに関しては、キーボード専用ユーザーがコントロールを使用できることが重要です。</span><span class="sxs-lookup"><span data-stu-id="0c70d-108">For accessibility, it's essential that keyboard-only users be able to use controls.</span></span> <span data-ttu-id="0c70d-109">したがって、キーボード ショートカットは、拡張可能コントロールを作成するときの重要な考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="0c70d-109">Therefore, keyboard shortcuts are an important consideration when you create any extensible control.</span></span> <span data-ttu-id="0c70d-110">このトピックでは、キーボード ショートカットとして使用するキーの組み合わせを選択するのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-110">This topic provides information that will help you choose key combinations to use as keyboard shortcuts.</span></span> <span data-ttu-id="0c70d-111">ここでは、Finance and Operations アプリおよびサポートされているブラウザーで使用されているショートカット、実装を計画しているショートカット、1 つ以上のブラウザーがオーバーライドを許可しないショートカットを取り上げます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-111">It highlights the shortcuts that are currently used by Finance and Operations apps and supported browsers, shortcuts that are planned for implementation, and shortcuts that one or more browsers don't allow to be overridden.</span></span> <span data-ttu-id="0c70d-112">このトピックは、拡張可能なコントロールのキーボード ショートカットを実装するための推奨の方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-112">This topic also outlines the recommended way to implement keyboard shortcuts for extensible controls.</span></span>

## <a name="choosing-a-key-combination"></a><span data-ttu-id="0c70d-113">キーの組み合わせの選択</span><span class="sxs-lookup"><span data-stu-id="0c70d-113">Choosing a key combination</span></span>
<span data-ttu-id="0c70d-114">キーボード ショートカットとして使用するキーの組み合わせを選択するときは、その他の既存のショートカットを分かっていることが重要です。</span><span class="sxs-lookup"><span data-stu-id="0c70d-114">When you're trying to choose a key combination to use as a keyboard shortcut, it's important that you be aware of other existing shortcuts.</span></span> <span data-ttu-id="0c70d-115">この方法で、ショートカットが既存のショートカットと重複しないことを保証できます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-115">In this way, you help guarantee that your shortcut won't overlap an existing shortcut.</span></span> <span data-ttu-id="0c70d-116">既存のショートカットと衝突しようとすると、次のいずれかの結果が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c70d-116">If you try to collide with an existing shortcut, one of the following outcomes might occur:</span></span>

- <span data-ttu-id="0c70d-117">この新しいキーボード ショートカットは、ブラウザーがそのキーの組み合わせを上書きすることを許可していないか、フレームワーク提供のショートカットが新しいショートカットよりも優先されるため動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c70d-117">The new keyboard shortcut might not work, because a browser doesn't allow that key combination to be overridden, or a framework-provided shortcut takes precedence over the new shortcut.</span></span>
- <span data-ttu-id="0c70d-118">新しいキーボード ショートカットを使用すると、想定されているキーボード機能が削除されることがあります。これは、ユーザーが特定のキーの組み合わせによってブラウザー内の特定の機能を実行するためです。</span><span class="sxs-lookup"><span data-stu-id="0c70d-118">The new keyboard shortcut might remove expected keyboard functionality, because users expect specific key combinations to perform specific functions in a browser.</span></span> <span data-ttu-id="0c70d-119">または、フレームワークによって指定されたショートカットまたはその他のコントロール ショートカットを上書きすることによって、キーボード専用のユーザーは使用いようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-119">Alternatively, you might override framework-provided shortcuts or other control shortcuts, so that keyboard-only users can't use them.</span></span>

<span data-ttu-id="0c70d-120">これらの潜在的な問題のため、キーの組み合わせを選択する際はこのガイダンスに従うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0c70d-120">Because of these potential issues, we recommend that you adhere to this guidance when you choose a key combination:</span></span>

- <span data-ttu-id="0c70d-121">現在、Finance and Operations アプリで使用されているか、または今後の実装が計画されているキーの組み合わせを選択**しない**でください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-121">**Don't** choose any key combination that is currently used by Finance and Operations apps, or that is planned for future implementation.</span></span>
- <span data-ttu-id="0c70d-122">サポートされているすべてのブラウザーで機能するためのキーの組み合わせを選択**します**。</span><span class="sxs-lookup"><span data-stu-id="0c70d-122">**Do** pick key combinations that will work in all supported browsers.</span></span>
- <span data-ttu-id="0c70d-123">サポートされているブラウザで使用されているショートカットを上書きするときは**よく**注意してください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-123">**Do** be careful when you override shortcuts that are used by a supported browser.</span></span> <span data-ttu-id="0c70d-124">重要な、または頻繁に使用されるブラウザー機能のショートカットを無効にしないでください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-124">You should not suppress shortcuts for important or frequently used browser functionality.</span></span>
- <span data-ttu-id="0c70d-125">コントロール固有の動作のために、より長いキーの組み合わせ (3 つのキー) を使用**します**。</span><span class="sxs-lookup"><span data-stu-id="0c70d-125">**Do** use longer key combinations (three keys) for control-specific behavior.</span></span> <span data-ttu-id="0c70d-126">ユーザー定義のキーボード ショートカット用に、短い組み合わせを予約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c70d-126">Shorter combinations should be reserved for user-defined keyboard shortcuts.</span></span>
- <span data-ttu-id="0c70d-127">この組み合わせはいくつかの東ヨーロッパ言語の Alt+Gr にマップされ、他のショートカットと競合するため、Ctrl+Alt を含むキーの組み合わせを選択**しない**でください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-127">**Don't** choose any key combination that involves Ctrl+Alt, because this combination maps to Alt+Gr for some Eastern European languages and will conflict with other shortcuts.</span></span>

### <a name="keyboard-shortcut-links"></a><span data-ttu-id="0c70d-128">キーボード ショートカットのリンク</span><span class="sxs-lookup"><span data-stu-id="0c70d-128">Keyboard shortcut links</span></span>
<span data-ttu-id="0c70d-129">Finance and Operations アプリおよびサポートされているブラウザーに記載されているキーボード ショートカットへのリンクを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-129">Here are links to the keyboard shortcuts that are documented for Finance and Operations apps and supported browsers:</span></span>

- <span data-ttu-id="0c70d-130"><a href="../../fin-ops/get-started/shortcut-keys.md">キーボード ショートカット</a></span><span class="sxs-lookup"><span data-stu-id="0c70d-130"><a href="../../fin-ops/get-started/shortcut-keys.md">Keyboard shortcuts</a></span></span>
- <span data-ttu-id="0c70d-131"><a href="https://support.microsoft.com/help/13805">Microsoft Edge</a></span><span class="sxs-lookup"><span data-stu-id="0c70d-131"><a href="https://support.microsoft.com/help/13805">Microsoft Edge</a></span></span>
- <span data-ttu-id="0c70d-132"><a href="https://support.google.com/chrome/answer/157179">Google Chrome</a></span><span class="sxs-lookup"><span data-stu-id="0c70d-132"><a href="https://support.google.com/chrome/answer/157179">Google Chrome</a></span></span>
- <span data-ttu-id="0c70d-133"><a href="https://support.microsoft.com/help/15357/windows-internet-explorer-11-keyboard-shortcuts">Internet Explorer 11</a></span><span class="sxs-lookup"><span data-stu-id="0c70d-133"><a href="https://support.microsoft.com/help/15357/windows-internet-explorer-11-keyboard-shortcuts">Internet Explorer 11</a></span></span>
- <span data-ttu-id="0c70d-134"><a href="https://support.apple.com/kb/PH21483">Apple Safari</a></span><span class="sxs-lookup"><span data-stu-id="0c70d-134"><a href="https://support.apple.com/kb/PH21483">Apple Safari</a></span></span>

### <a name="planned-keyboard-shortcuts"></a><span data-ttu-id="0c70d-135">計画されているキーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="0c70d-135">Planned keyboard shortcuts</span></span> 
<span data-ttu-id="0c70d-136">使用されているキーボード ショートカットに加えて、今後の実装が計画されているいくつかのショートカットがあります。</span><span class="sxs-lookup"><span data-stu-id="0c70d-136">In addition to the keyboard shortcuts that are currently used, there are several shortcuts that are planned for future implementation.</span></span> <span data-ttu-id="0c70d-137">フレームワークによって指定されたショートカットと競合を避けるために、拡張可能なコントロールには以下のキーの組み合わせを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-137">To avoid conflicts with framework-provided shortcuts, you should not choose the following key combinations for extensible controls.</span></span>
<table>
<tbody>
<tr>
<th><span data-ttu-id="0c70d-138">ショートカット</span><span class="sxs-lookup"><span data-stu-id="0c70d-138">Shortcut</span></span></th>
<th><span data-ttu-id="0c70d-139">機能</span><span class="sxs-lookup"><span data-stu-id="0c70d-139">Functionality</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="0c70d-140">F3</span><span class="sxs-lookup"><span data-stu-id="0c70d-140">F3</span></span></td>
<td><span data-ttu-id="0c70d-141">最も近い QuickFilter に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-141">Move to the nearest QuickFilter.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-142">Alt + F3</span><span class="sxs-lookup"><span data-stu-id="0c70d-142">Alt+F3</span></span></td>
<td><span data-ttu-id="0c70d-143">現在のコントロールの値に基づくフィルターを追加します (値によるフィルター)。</span><span class="sxs-lookup"><span data-stu-id="0c70d-143">Add a filter that is based on the value of the current control (Filter by value).</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-144">Alt + Shift + F3</span><span class="sxs-lookup"><span data-stu-id="0c70d-144">Alt+Shift+F3</span></span></td>
<td><span data-ttu-id="0c70d-145">すべてのユーザー定義のフィルターをクリアします。</span><span class="sxs-lookup"><span data-stu-id="0c70d-145">Clear all user-defined filters.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-146">F6</span><span class="sxs-lookup"><span data-stu-id="0c70d-146">F6</span></span></td>
<td><span data-ttu-id="0c70d-147">最も近いツール バーに移動します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-147">Move to the nearest toolbar.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-148">Shift + F7</span><span class="sxs-lookup"><span data-stu-id="0c70d-148">Shift+F7</span></span></td>
<td><span data-ttu-id="0c70d-149">トースト メッセージに移動します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-149">Move to the toast message.</span></span></td>
</tr>
</tbody>
</table>

### <a name="browseroperating-system-keyboard-shortcuts-to-avoid"></a><span data-ttu-id="0c70d-150">ブラウザーおよびオペレーティング システムのキーボード ショートカットを回避</span><span class="sxs-lookup"><span data-stu-id="0c70d-150">Browser/operating system keyboard shortcuts to avoid</span></span>

#### <a name="keyboard-shortcuts-that-correspond-to-important-functionality"></a><span data-ttu-id="0c70d-151">重要な機能に対応するキーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="0c70d-151">Keyboard shortcuts that correspond to important functionality</span></span>
<span data-ttu-id="0c70d-152">以下のテーブルは、ブラウザーまたはオペレーティング システムの重要な機能に対応するキーボード ショートカットの包括的ではない、簡潔なリストです。</span><span class="sxs-lookup"><span data-stu-id="0c70d-152">The following table provides a short, non-exhaustive list of keyboard shortcuts that correspond to important functionality in a browser or operating system.</span></span> <span data-ttu-id="0c70d-153">この表では、キーの組み合わせを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-153">You should not choose the key combinations in this table.</span></span>
<table>
<tbody>
<tr>
<th><span data-ttu-id="0c70d-154">ショートカット</span><span class="sxs-lookup"><span data-stu-id="0c70d-154">Shortcut</span></span></th>
<th><span data-ttu-id="0c70d-155">機能</span><span class="sxs-lookup"><span data-stu-id="0c70d-155">Functionality</span></span></th>
</tr>
</tbody>
<tbody>
<tr>
<td><span data-ttu-id="0c70d-156">Ctrl + A</span><span class="sxs-lookup"><span data-stu-id="0c70d-156">Ctrl+A</span></span></td>
<td><span data-ttu-id="0c70d-157">現在のフィールドのすべてのテキストを選択するか、ページ上のすべてのコンテンツを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-157">Select all the text in the current field, or select all content on the page.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-158">Ctrl+C</span><span class="sxs-lookup"><span data-stu-id="0c70d-158">Ctrl+C</span></span></td>
<td><span data-ttu-id="0c70d-159">コピー。</span><span class="sxs-lookup"><span data-stu-id="0c70d-159">Copy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-160">Ctrl + V</span><span class="sxs-lookup"><span data-stu-id="0c70d-160">Ctrl+V</span></span></td>
<td><span data-ttu-id="0c70d-161">貼り付け。</span><span class="sxs-lookup"><span data-stu-id="0c70d-161">Paste.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-162">Ctrl + X</span><span class="sxs-lookup"><span data-stu-id="0c70d-162">Ctrl+X</span></span></td>
<td><span data-ttu-id="0c70d-163">切り取り。</span><span class="sxs-lookup"><span data-stu-id="0c70d-163">Cut.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-164">F5</span><span class="sxs-lookup"><span data-stu-id="0c70d-164">F5</span></span></td>
<td><span data-ttu-id="0c70d-165">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-165">Refresh the page.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-166">Ctrl + F5</span><span class="sxs-lookup"><span data-stu-id="0c70d-166">Ctrl+F5</span></span></td>
<td><span data-ttu-id="0c70d-167">ページを更新し、キャッシュされたコンテンツを無視します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-167">Refresh the page, and ignore cached content.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-168">Shift + F10</span><span class="sxs-lookup"><span data-stu-id="0c70d-168">Shift+F10</span></span></td>
<td><span data-ttu-id="0c70d-169">右クリックをシミュレートします。</span><span class="sxs-lookup"><span data-stu-id="0c70d-169">Simulate a right-click.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-170">Tab または Shift+Tab</span><span class="sxs-lookup"><span data-stu-id="0c70d-170">Tab / Shift+Tab</span></span></td>
<td><span data-ttu-id="0c70d-171">前後のコントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-171">Move to the next/previous control.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-172">Ctrl + Tab / Ctrl + Shift + Tab</span><span class="sxs-lookup"><span data-stu-id="0c70d-172">Ctrl+Tab / Ctrl+Shift+Tab</span></span></td>
<td><span data-ttu-id="0c70d-173">前後のブラウザー タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-173">Move to the next/previous browser tab.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-174">Alt+Tab / Alt+Shift+Tab</span><span class="sxs-lookup"><span data-stu-id="0c70d-174">Alt+Tab / Alt+Shift+Tab</span></span></td>
<td><span data-ttu-id="0c70d-175">前後のアプリケーションに移動します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-175">Move to the next/previous application.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-176">Alt + 右矢印/Alt + 左矢印</span><span class="sxs-lookup"><span data-stu-id="0c70d-176">Alt+Right arrow / Alt + Left arrow</span></span></td>
<td><span data-ttu-id="0c70d-177">ブラウザ履歴で、前後のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-177">Go to the next/previous page in the browser history.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="keyboard-shortcuts-that-cant-be-overridden-by-some-browsers"></a><span data-ttu-id="0c70d-178">ブラウザーによってオーバーライドできないキーボード ショートカット</span><span class="sxs-lookup"><span data-stu-id="0c70d-178">Keyboard shortcuts that can't be overridden by some browsers</span></span>
<span data-ttu-id="0c70d-179">ブラウザーによっては、以下のキーボード ショートカットを上書きできません。</span><span class="sxs-lookup"><span data-stu-id="0c70d-179">Some browsers don't allow the following keyboard shortcuts to be overridden.</span></span> <span data-ttu-id="0c70d-180">したがって、ショートカットは一部のブラウザーで機能しないため、次のキーの組み合わせは選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-180">Therefore, you should not choose the following key combinations, because the shortcut won't work in all browsers.</span></span>
<table>
<tbody>
<tr>
<td><span data-ttu-id="0c70d-181">Alt+A</span><span class="sxs-lookup"><span data-stu-id="0c70d-181">Alt+A</span></span></td>
<td><span data-ttu-id="0c70d-182">Alt+T</span><span class="sxs-lookup"><span data-stu-id="0c70d-182">Alt+T</span></span></td>
<td><span data-ttu-id="0c70d-183">Ctrl + F4</span><span class="sxs-lookup"><span data-stu-id="0c70d-183">Ctrl+F4</span></span></td>
<td><span data-ttu-id="0c70d-184">Alt+Tab</span><span class="sxs-lookup"><span data-stu-id="0c70d-184">Alt+Tab</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-185">Alt+C</span><span class="sxs-lookup"><span data-stu-id="0c70d-185">Alt+C</span></span></td>
<td><span data-ttu-id="0c70d-186">Alt+V</span><span class="sxs-lookup"><span data-stu-id="0c70d-186">Alt+V</span></span></td>
<td><span data-ttu-id="0c70d-187">Alt + F5</span><span class="sxs-lookup"><span data-stu-id="0c70d-187">Alt+F5</span></span></td>
<td><span data-ttu-id="0c70d-188">Alt+Shift+Tab</span><span class="sxs-lookup"><span data-stu-id="0c70d-188">Alt+Shift+Tab</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-189">Alt+D</span><span class="sxs-lookup"><span data-stu-id="0c70d-189">Alt+D</span></span></td>
<td><span data-ttu-id="0c70d-190">Ctrl + W</span><span class="sxs-lookup"><span data-stu-id="0c70d-190">Ctrl+W</span></span></td>
<td><span data-ttu-id="0c70d-191">Alt + F6</span><span class="sxs-lookup"><span data-stu-id="0c70d-191">Alt+F6</span></span></td>
<td><span data-ttu-id="0c70d-192">スペース バー</span><span class="sxs-lookup"><span data-stu-id="0c70d-192">Spacebar</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-193">Alt+Shift+D</span><span class="sxs-lookup"><span data-stu-id="0c70d-193">Alt+Shift+D</span></span></td>
<td><span data-ttu-id="0c70d-194">Ctrl + Shift + W</span><span class="sxs-lookup"><span data-stu-id="0c70d-194">Ctrl+Shift+W</span></span></td>
<td><span data-ttu-id="0c70d-195">Alt + Shift + F6</span><span class="sxs-lookup"><span data-stu-id="0c70d-195">Alt+Shift+F6</span></span></td>
<td><span data-ttu-id="0c70d-196">Alt+Shift+Backspace</span><span class="sxs-lookup"><span data-stu-id="0c70d-196">Alt+Shift+Backspace</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-197">Alt+E</span><span class="sxs-lookup"><span data-stu-id="0c70d-197">Alt+E</span></span></td>
<td><span data-ttu-id="0c70d-198">Alt+X</span><span class="sxs-lookup"><span data-stu-id="0c70d-198">Alt+X</span></span></td>
<td><span data-ttu-id="0c70d-199">F12</span><span class="sxs-lookup"><span data-stu-id="0c70d-199">F12</span></span></td>
<td><span data-ttu-id="0c70d-200">Ctrl + Pause/Break</span><span class="sxs-lookup"><span data-stu-id="0c70d-200">Ctrl+Pause/Break</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-201">Alt+F</span><span class="sxs-lookup"><span data-stu-id="0c70d-201">Alt+F</span></span></td>
<td><span data-ttu-id="0c70d-202">Ctrl + Shift + 0</span><span class="sxs-lookup"><span data-stu-id="0c70d-202">Ctrl+Shift+0</span></span></td>
<td><span data-ttu-id="0c70d-203">Ctrl + Esc</span><span class="sxs-lookup"><span data-stu-id="0c70d-203">Ctrl+Esc</span></span></td>
<td><span data-ttu-id="0c70d-204">Ctrl + Shift + Pause/Break</span><span class="sxs-lookup"><span data-stu-id="0c70d-204">Ctrl+Shift+Pause/Break</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-205">Alt+H</span><span class="sxs-lookup"><span data-stu-id="0c70d-205">Alt+H</span></span></td>
<td><span data-ttu-id="0c70d-206">Ctrl + Shift + 7</span><span class="sxs-lookup"><span data-stu-id="0c70d-206">Ctrl+Shift+7</span></span></td>
<td><span data-ttu-id="0c70d-207">Ctrl + Shift + Esc</span><span class="sxs-lookup"><span data-stu-id="0c70d-207">Ctrl+Shift+Esc</span></span></td>
<td><span data-ttu-id="0c70d-208">Ctrl + Page up</span><span class="sxs-lookup"><span data-stu-id="0c70d-208">Ctrl+Page up</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-209">Ctrl + N</span><span class="sxs-lookup"><span data-stu-id="0c70d-209">Ctrl+N</span></span></td>
<td><span data-ttu-id="0c70d-210">F1</span><span class="sxs-lookup"><span data-stu-id="0c70d-210">F1</span></span></td>
<td><span data-ttu-id="0c70d-211">Alt+Esc</span><span class="sxs-lookup"><span data-stu-id="0c70d-211">Alt+Esc</span></span></td>
<td><span data-ttu-id="0c70d-212">Ctrl + Page down</span><span class="sxs-lookup"><span data-stu-id="0c70d-212">Ctrl+Page down</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-213">Ctrl + Shift + N</span><span class="sxs-lookup"><span data-stu-id="0c70d-213">Ctrl+Shift+N</span></span></td>
<td><span data-ttu-id="0c70d-214">Ctrl + F1</span><span class="sxs-lookup"><span data-stu-id="0c70d-214">Ctrl+F1</span></span></td>
<td><span data-ttu-id="0c70d-215">Alt+Shift+Esc</span><span class="sxs-lookup"><span data-stu-id="0c70d-215">Alt+Shift+Esc</span></span></td>
<td><span data-ttu-id="0c70d-216">Ctrl + プラス記号 (+)</span><span class="sxs-lookup"><span data-stu-id="0c70d-216">Ctrl+Plus sign (+)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-217">Ctrl + Shift + Q</span><span class="sxs-lookup"><span data-stu-id="0c70d-217">Ctrl+Shift+Q</span></span></td>
<td><span data-ttu-id="0c70d-218">Ctrl + Shift + F1</span><span class="sxs-lookup"><span data-stu-id="0c70d-218">Ctrl+Shift+F1</span></span></td>
<td><span data-ttu-id="0c70d-219">Ctrl + Tab</span><span class="sxs-lookup"><span data-stu-id="0c70d-219">Ctrl+Tab</span></span></td>
<td><span data-ttu-id="0c70d-220">Shift + プラス記号 (+)</span><span class="sxs-lookup"><span data-stu-id="0c70d-220">Shift+Plus sign (+)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c70d-221">Ctrl + T</span><span class="sxs-lookup"><span data-stu-id="0c70d-221">Ctrl+T</span></span></td>
<td><span data-ttu-id="0c70d-222">Shift + F1</span><span class="sxs-lookup"><span data-stu-id="0c70d-222">Shift+F1</span></span></td>
<td><span data-ttu-id="0c70d-223">Ctrl + Shift + Tab</span><span class="sxs-lookup"><span data-stu-id="0c70d-223">Ctrl+Shift+Tab</span></span></td>
<td><span data-ttu-id="0c70d-224">Ctrl + マイナス記号 (-)</span><span class="sxs-lookup"><span data-stu-id="0c70d-224">Ctrl+Minus sign (–)</span></span></td>
</tr>
</tbody>
</table>

## <a name="implementing-keyboard-shortcuts"></a><span data-ttu-id="0c70d-225">キーボード ショートカットの実装</span><span class="sxs-lookup"><span data-stu-id="0c70d-225">Implementing keyboard shortcuts</span></span>
<span data-ttu-id="0c70d-226">このセクションに記載されている登録メカニズムを使用して、キーボード ショートカットを実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0c70d-226">We recommend that you use the registration mechanism that is described in this section to implement keyboard shortcuts.</span></span> <span data-ttu-id="0c70d-227">この方法でコントロールのショートカットを登録すると、いくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="0c70d-227">There are several benefits to registering a control's shortcuts in this manner:</span></span>

- <span data-ttu-id="0c70d-228">必要な修飾子キーのみを指定します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-228">You specify only the modifier keys that you want.</span></span> <span data-ttu-id="0c70d-229">その他のモディファイアーを押すと、ショートカットは実行されません。</span><span class="sxs-lookup"><span data-stu-id="0c70d-229">If any other modifiers are pressed, the shortcut won't run.</span></span> <span data-ttu-id="0c70d-230">したがって、Ctrl + Shift +下向き矢印を押しても、Ctrl +下向き矢印に定義されたキーボード ショートカットはトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="0c70d-230">Therefore, a keyboard shortcut that is defined for Ctrl+Down arrow won't be triggered if Ctrl+Shift+Down arrow is pressed.</span></span></li>
- <span data-ttu-id="0c70d-231">コードは再利用することができます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-231">You can reuse code.</span></span>
- <span data-ttu-id="0c70d-232"><strong>false</strong> をハンドラー関数で返す場合、伝達はイベントで停止しません。</span><span class="sxs-lookup"><span data-stu-id="0c70d-232">If you return <strong>false</strong> from the handler function, propagation won't stop on the event.</span></span> <span data-ttu-id="0c70d-233"><strong>true</strong> を返す場合、(または戻り値を指定しない場合)、伝達は停止されます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-233">If you return <strong>true</strong> (or if you don't specify a return value), propagation will stop.</span></span>
- <span data-ttu-id="0c70d-234">Ctrl およびメタの変更要因は同じように処理されます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-234">Ctrl and Meta modifiers are treated the same.</span></span> <span data-ttu-id="0c70d-235">したがって、iOS と Microsoft Windows の両方で動作するキーボード ショートカットを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-235">Therefore, you can specify keyboard shortcuts that will work for both iOS and Microsoft Windows.</span></span> <span data-ttu-id="0c70d-236">たとえば、Windows でのショートカット Ctrl + G は、iOS で Meta + G に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-236">For example, the shortcut Ctrl+G on Windows will be translated to Meta+G on iOS.</span></span>
- <span data-ttu-id="0c70d-237">キーボード ショートカット用の組み込みテレメトリが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-237">Built-in telemetry for the keyboard shortcuts is used.</span></span>

### <a name="define-a-keyboard-shortcut"></a><span data-ttu-id="0c70d-238">キーボード ショートカットを定義する</span><span class="sxs-lookup"><span data-stu-id="0c70d-238">Define a keyboard shortcut</span></span>

1. <span data-ttu-id="0c70d-239">コントロールのプロトタイプにショートカット オブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-239">Define a Shortcuts object on the control's prototype.</span></span> <span data-ttu-id="0c70d-240">次に、ショートカット オブジェクト内のキーボード ショートカットを定義します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-240">Then define the keyboard shortcuts inside the Shortcuts object.</span></span> <span data-ttu-id="0c70d-241">これらのショートカットは、次の構造が必要です。</span><span class="sxs-lookup"><span data-stu-id="0c70d-241">These shortcuts should have the following structure.</span></span> <span data-ttu-id="0c70d-242">使用しようとしているキー コードが、$dyn.ui.KeyCodes オブジェクトで定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-242">Make sure that the key code that you're trying to use is defined in the $dyn.ui.KeyCodes object.</span></span>

    ```Text
    Shortcuts: {
        Name: {
            Keys: { modifier1: true, modifier2:true, 
                keyCode: $dyn.ui.KeyCodes.* }, 
            // Only specify the modifiers you need 
            // (between alt, ctrl/meta, shift)
            Handler: function (evt) {
                // Code to handle shortcut.
            },
            // Additional code.
    }
    ```

    <span data-ttu-id="0c70d-243">キーボード ショートカットに 1 つ以上のキー コードを適用する必要がある場合は、次のように、コードの配列で渡します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-243">If more than one key code should apply to your keyboard shortcut, pass in an array of codes, as shown here.</span></span>

    ```Text
    Keys: {modifier1:true, 
        keyCode:[$dyn.ui.KeyCodes.*, $dyn.ui.KeyCodes.*, ... ] } 
    // Note: If any of these keyCodes match then the handler is called. I.E. 
    // The keyCodes in the array are OR'd not AND'd
    ```
2. <span data-ttu-id="0c70d-244">次のコードを使用して keyDown ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-244">Add the keydown handler by using the following code.</span></span>

    ```Text
    keydown: function (event) {
        $dyn.util.handleShortcuts(this, event);
    },
    ```

3. <span data-ttu-id="0c70d-245">keyDown ハンドラーをバインドします。</span><span class="sxs-lookup"><span data-stu-id="0c70d-245">Bind the keyDown handler.</span></span> <span data-ttu-id="0c70d-246">keyDown ハンドラーは自動的にフォーム オブジェクトにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-246">The keyDown handler is automatically bound for form objects.</span></span> <span data-ttu-id="0c70d-247">その他のコントロールは、通常のバインドに関してだけ、keyDown ハンドラーに手動でバインドしてください。</span><span class="sxs-lookup"><span data-stu-id="0c70d-247">Other controls must be manually bound to the keyDown handler, as for any regular binding.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="0c70d-248">「keyDown」では、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="0c70d-248">"keyDown" is case sensitive.</span></span>

    ```Text
    <div data-dyn-bind="keyDown: $data.keydown"></div>;
    ```

### <a name="examples"></a><span data-ttu-id="0c70d-249">例</span><span class="sxs-lookup"><span data-stu-id="0c70d-249">Examples</span></span>
<span data-ttu-id="0c70d-250">次にフォーム例を示します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-250">Here is a Form example.</span></span>

```Text
Shortcuts: {
    Save: {
        Keys: { ctrl: true, keyCode: $dyn.ui.KeyCodes.letterS },
        Handler: function (evt) {
            var control = evt ? $dyn.context(evt.target) : undefined;
            this.executeShortcuts(true, "SaveRecord", control);
        },
    },
    New: {
        Keys: { alt: true, keyCode: $dyn.ui.KeyCodes.letterN },
        Handler: function (evt) {
            var control = evt ? $dyn.context(evt.target) : undefined;
            this.executeShortcuts(true, "NewRecord", control);
        },
    },
    Delete: {
        Keys: { alt: true, keyCode: $dyn.ui.KeyCodes.deleteKey },
        Handler: function (evt) {
            this.executeShortcuts(false, "DeleteRecord");
        },
    },
    // Additional code
}
```

<span data-ttu-id="0c70d-251">フォーム コントロールを拡張するダイアログの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0c70d-251">Here is a Dialogs example that extends the Form control.</span></span>

```Text
Shortcuts: $dyn.extendPrototype($dyn.controls.Form.prototype.Shortcuts, {
    InvokeDefaultButton: {
        Keys: { keyCode: $dyn.ui.KeyCodes.enter },
        Handler: function (evt) {
            this.executeShortcuts(false, "InvokeDefaultButton");
        }
    },
})
```


