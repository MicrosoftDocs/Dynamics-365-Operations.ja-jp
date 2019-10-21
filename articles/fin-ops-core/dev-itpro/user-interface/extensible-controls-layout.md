---
title: 拡張可能なコントロール レイアウトのガイドライン
description: この記事では、拡張可能なコントロールのレイアウトとサイズを指定するときに従うガイドラインについて説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 11354
ms.assetid: 53d1f66a-1e69-4548-9fd2-a87a3b370882
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e9d38894a5b83da5302a36903c4467785ea94a2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183056"
---
# <a name="extensible-control-layout-guidelines"></a><span data-ttu-id="d71cd-103">拡張可能なコントロール レイアウトのガイドライン</span><span class="sxs-lookup"><span data-stu-id="d71cd-103">Extensible control layout guidelines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d71cd-104">この記事では、拡張可能なコントロールのレイアウトとサイズを指定するときに従うガイドラインについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d71cd-104">This article provides guidelines that you should follow when you specify the layout and sizing of extensible controls.</span></span>

<a name="dos-and-donts-for-achieving-the-desired-layout"></a><span data-ttu-id="d71cd-105">目的のレイアウトを実現するための注意事項</span><span class="sxs-lookup"><span data-stu-id="d71cd-105">Dos and don'ts for achieving the desired layout</span></span>
-----------------------------------------------

-   <span data-ttu-id="d71cd-106">コントロールのレイアウト クラスを直接使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d71cd-106">Don't use the layout classes on your control directly.</span></span> <span data-ttu-id="d71cd-107">(たとえば、**layout-container** および **layout-horizontal** は、DOM のコントロールに表示されるクラスです。) 代わりに、レイアウト バインディング ハンドラーを使用して、これらのクラスを適用します。</span><span class="sxs-lookup"><span data-stu-id="d71cd-107">(For example, **layout-container** and **layout-horizontal** are classes that you might see on controls in the DOM.) Instead, use the layout binding handlers to apply these classes.</span></span> <span data-ttu-id="d71cd-108">Internet Explorer は異なるレイアウト フレームワークを使用しており、要素にいくつかのインライン スタイルを追加するには、このフレームワークにハンドラーが提供する予備のバインディング情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="d71cd-108">Internet Explorer uses a different layout framework, and to add some inline styles to elements, this framework requires the extra binding information that the handlers provide.</span></span> <span data-ttu-id="d71cd-109">したがって、クラスがコントロールにハードコードされて**いない**ことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d71cd-109">Therefore, make sure that the classes are **not** hard-coded into the controls.</span></span>
-   <span data-ttu-id="d71cd-110">レイアウト バインディング ハンドラーを使うコンテナーの子である要素に、絶対配置 (**position: absolute** and **top**/**bottom**/**left**/**right** positions) を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d71cd-110">Don't use absolute positioning (**position: absolute** and **top**/**bottom**/**left**/**right** positions) for elements that are children of a container that uses the layout binding handler.</span></span> <span data-ttu-id="d71cd-111">これらの要素の絶対配置は、正しく物事をレイアウトすることに適用される CSS クラスを妨げます。</span><span class="sxs-lookup"><span data-stu-id="d71cd-111">Absolute positioning of these elements prevents the CSS classes that are applied from laying things out correctly.</span></span>
-   <span data-ttu-id="d71cd-112">**幅: 100%** と**高さ: 100%** の使用には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="d71cd-112">Be careful about using **width: 100%** and **height: 100%**.</span></span> <span data-ttu-id="d71cd-113">これらの設定は、レイアウト CSS クラスと組み合わせて使用すると、必ずしも機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-113">These settings might not always work when they are combined with our layout CSS classes.</span></span> <span data-ttu-id="d71cd-114">塗りつぶし動作を使用する場合、代わりにサイズ変更バインディング ハンドラーの **$dyn.layout.Size.available** オプションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d71cd-114">If you want filling behavior, it's a good idea to use the **$dyn.layout.Size.available** option of the sizing binding handler instead.</span></span>

## <a name="layout-binding-handlers"></a><span data-ttu-id="d71cd-115">レイアウト バインディング ハンドラー</span><span class="sxs-lookup"><span data-stu-id="d71cd-115">Layout binding handlers</span></span>
### <a name="layout"></a><span data-ttu-id="d71cd-116">レイアウト</span><span class="sxs-lookup"><span data-stu-id="d71cd-116">Layout</span></span>

<span data-ttu-id="d71cd-117">**ArrangeMethod** 属性と **Columns** 属性をコンテナーの **arrangeMethod**、**Columns**、**Children** オプションに適用するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d71cd-117">Used to apply **ArrangeMethod** and **Columns** attributes to containers Options: **arrangeMethod**, **Columns**, **Children**</span></span>

#### <a name="arrangemethod"></a><span data-ttu-id="d71cd-118">ArrangeMethod</span><span class="sxs-lookup"><span data-stu-id="d71cd-118">ArrangeMethod</span></span>

-   <span data-ttu-id="d71cd-119">$dyn.layout.ArrangeMethod.vertical</span><span class="sxs-lookup"><span data-stu-id="d71cd-119">$dyn.layout.ArrangeMethod.vertical</span></span>
-   <span data-ttu-id="d71cd-120">$dyn.layout.ArrangeMethod.horizontalLeft</span><span class="sxs-lookup"><span data-stu-id="d71cd-120">$dyn.layout.ArrangeMethod.horizontalLeft</span></span>
-   <span data-ttu-id="d71cd-121">$dyn.layout.ArrangeMethod.horizontalWrap</span><span class="sxs-lookup"><span data-stu-id="d71cd-121">$dyn.layout.ArrangeMethod.horizontalWrap</span></span>
-   <span data-ttu-id="d71cd-122">$dyn.layout.ArrangeMethod.horizontalRight</span><span class="sxs-lookup"><span data-stu-id="d71cd-122">$dyn.layout.ArrangeMethod.horizontalRight</span></span>
-   <span data-ttu-id="d71cd-123">$dyn.layout.ArrangeMethod.none (レイアウト CSS クラスは要素に適用されません。)</span><span class="sxs-lookup"><span data-stu-id="d71cd-123">$dyn.layout.ArrangeMethod.none (No layout CSS classes should be applied to the element.)</span></span>

#### <a name="columns"></a><span data-ttu-id="d71cd-124">列</span><span class="sxs-lookup"><span data-stu-id="d71cd-124">Columns</span></span>

-   <span data-ttu-id="d71cd-125">**$dyn.layout.Columns.fill** - この定数を使用します。</span><span class="sxs-lookup"><span data-stu-id="d71cd-125">**$dyn.layout.Columns.fill** – Use this constant.</span></span> <span data-ttu-id="d71cd-126">コントロールに応じて、「塗りつぶし」と「バランス」のいずれかの列が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d71cd-126">Depending on the control, either "fill" and "balanced" columns are used.</span></span>
-   <span data-ttu-id="d71cd-127">**$dyn.layout.Columns.fixed** - **1**、**2**、**3** のような固定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d71cd-127">**$dyn.layout.Columns.fixed** – Use a fixed value, such as **1**, **2**, or **3**.</span></span>

#### <a name="children"></a><span data-ttu-id="d71cd-128">子</span><span class="sxs-lookup"><span data-stu-id="d71cd-128">Children</span></span>

-   <span data-ttu-id="d71cd-129">このコンテナを介して子を追加するためにコンテンツ ハンドラー (追加、置換) を使用する場合は、**$ data.Children** を使用します。</span><span class="sxs-lookup"><span data-stu-id="d71cd-129">Use \*\*$data.Children \*\*if the content handlers (append, replace) will be used to append children through this container.</span></span> <span data-ttu-id="d71cd-130">このコントロールがコンテナーである場合にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-130">It should be used only if this control is a container.</span></span>

<span data-ttu-id="d71cd-131">**使用例:**</span><span class="sxs-lookup"><span data-stu-id="d71cd-131">**Example usage:**</span></span>

    <div data-dyn-bind="layout: { arrangeMethod: $dyn.layout.ArrangeMethod.vertical, columns: '1' }"> </div>

### <a name="sizing"></a><span data-ttu-id="d71cd-132">サイズ変更</span><span class="sxs-lookup"><span data-stu-id="d71cd-132">Sizing</span></span>

#### <a name="heightwidth"></a><span data-ttu-id="d71cd-133">高さ/幅</span><span class="sxs-lookup"><span data-stu-id="d71cd-133">Height/width</span></span>

-   <span data-ttu-id="d71cd-134">**$dyn.layout.Size.available (SizeToAvailable)** - その方向に使用可能領域を入力します。</span><span class="sxs-lookup"><span data-stu-id="d71cd-134">**$dyn.layout.Size.available (SizeToAvailable)** – Fill the available space in that direction.</span></span>
-   <span data-ttu-id="d71cd-135">**$dyn.layout.Size.content (SizeToContent)** - その方向のコンテンツへのサイズ。</span><span class="sxs-lookup"><span data-stu-id="d71cd-135">**$dyn.layout.Size.content (SizeToContent)** – Size to the contents in that direction.</span></span>
-   <span data-ttu-id="d71cd-136">**$dyn.layout.Size.fixed (手動)** - 固定ピクセル値。</span><span class="sxs-lookup"><span data-stu-id="d71cd-136">**$dyn.layout.Size.fixed (Manual)** – A fixed pixel value.</span></span>

<span data-ttu-id="d71cd-137">**使用例:**</span><span class="sxs-lookup"><span data-stu-id="d71cd-137">**Example usage:**</span></span>

    <div data-dyn-bind="sizing: { height: $dyn.layout.Size.available, width: $dyn.layout.Size.content }"> </div>

<span data-ttu-id="d71cd-138">**サイズ変更バインディング ハンドラーに関する注意事項:**</span><span class="sxs-lookup"><span data-stu-id="d71cd-138">**Things to note about the sizing binding handler:**</span></span>

-   <span data-ttu-id="d71cd-139">サイジング バインディング ハンドラーを **SizeToAvailable** オプション (**$dyn.layout.Size.available**) と組み合わせて使用するとき、レイアウト バインディング ハンドラーを親の **&lt;div&gt;**/DOM 要素使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-139">When you use the sizing binding handler in combination with the **SizeToAvailable** option (**$dyn.layout.Size.available**), the layout binding handler must be used on the parent **&lt;div&gt;**/DOM element.</span></span> <span data-ttu-id="d71cd-140">これにより、どの軸 (水平または垂直方向) に沿って満たされるかがわかります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-140">This is how we know which axis to fill along (horizontal or vertical).</span></span>

<span data-ttu-id="d71cd-141">**レイアウト/サイズ ハンドラーを使用すべきですか、または直接プロパティを設定する必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="d71cd-141">**Should you use layout/sizing handlers or set the properties directly?**</span></span>

-   <span data-ttu-id="d71cd-142">拡張可能コントロールがクライアント コントロール (グループまたは PivotItem など) から継承している場合、バインディングが既に存在するため、直接そのコントロールに関連付けられている **&lt;div&gt;** でバインディング ハンドラーを使用しません。</span><span class="sxs-lookup"><span data-stu-id="d71cd-142">If your extensible control inherits from a client control (such as Group or PivotItem), you won't use the binding handlers directly on the **&lt;div&gt;** that is associated with that control, because the binding is already there.</span></span> <span data-ttu-id="d71cd-143">ただし、**data-dyn-bind** 属性にプロパティが直接入れるように、プロパティを設定する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-143">However, you might have to set the properties as you want them directly in the **data-dyn-bind** attribute.</span></span>

<span data-ttu-id="d71cd-144">**例 :**</span><span class="sxs-lookup"><span data-stu-id="d71cd-144">**Example:**</span></span>

    <div data-dyn-role="Group" data-dyn-bind="ArrangeMethod: $dyn.layout.ArrangeMethod.vertical, Columns: $dyn.layout.Columns.fill, Height: $dyn.layout.Size.available"></div>

<a name="faq"></a><span data-ttu-id="d71cd-145">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d71cd-145">FAQ</span></span>
---

#### <a name="is-my-control-being-laid-out-as-expected"></a><span data-ttu-id="d71cd-146">自分のコントロールが期待どおりにレイアウトされているか。</span><span class="sxs-lookup"><span data-stu-id="d71cd-146">Is my control being laid out as expected?</span></span>

<span data-ttu-id="d71cd-147">指示に適した方法は、要素を検査し、目的のクラスを探すことです。</span><span class="sxs-lookup"><span data-stu-id="d71cd-147">A good way to tell is to inspect the element and look for the desired classes.</span></span>

-   <span data-ttu-id="d71cd-148">適用されるオプションに応じて検索するレイアウト クラス:</span><span class="sxs-lookup"><span data-stu-id="d71cd-148">Layout classes to look for, depending on the options applied:</span></span>
    -   <span data-ttu-id="d71cd-149">layout-container</span><span class="sxs-lookup"><span data-stu-id="d71cd-149">layout-container</span></span>
    -   <span data-ttu-id="d71cd-150">layout-vertical</span><span class="sxs-lookup"><span data-stu-id="d71cd-150">layout-vertical</span></span>
    -   <span data-ttu-id="d71cd-151">layout-horizontal</span><span class="sxs-lookup"><span data-stu-id="d71cd-151">layout-horizontal</span></span>
-   <span data-ttu-id="d71cd-152">検索するクラスのサイズ設定:</span><span class="sxs-lookup"><span data-stu-id="d71cd-152">Sizing classes to look for:</span></span>
    -   <span data-ttu-id="d71cd-153">**$dyn.layout.Size.available** で、**入力幅**または**入力高さ**のいずれかを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-153">For **$dyn.layout.Size.available**,  you should see either **fill-width** or **fill-height**.</span></span>
    -   <span data-ttu-id="d71cd-154">手動サイズについては、**固定高さ**または**固定幅**のいずれかを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-154">For manual size, you should see either **fixed-height** or **fixed-width**.</span></span>
    -   <span data-ttu-id="d71cd-155">**$dyn.layout.Size.content** では、追加のクラスは存在すべきでなく、手動の高さと幅は要素で特定されたインラインである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d71cd-155">For **$dyn.layout.Size.content**, there should be no extra classes, and the manual height/width should be specified inline on the element.</span></span>

<span data-ttu-id="d71cd-156">これらのクラスが予期したとおりに表示されない場合、拘束力のあるハンドラーの使用状況を確認し、このページの注意事項の一覧を読んだことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d71cd-156">If these classes don't appear as you expected, examine the usage of your binding handlers, and make sure that you've read through the list of dos and don'ts on this page.</span></span>



