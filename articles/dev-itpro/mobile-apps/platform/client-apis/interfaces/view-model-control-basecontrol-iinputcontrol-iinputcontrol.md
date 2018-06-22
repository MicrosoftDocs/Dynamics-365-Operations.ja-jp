---
title: InputControl
description: "すべてのコントロールのメソッドと属性を持つ入力コントロール インターフェイス。 入力コントロールは、たとえば新しいコントロールに対するユーザー入力を収集するために通常はタスク ページで使用されます。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6c7c6cfa8b9e1ac76e09b8efc91936095498bbb7
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="inputcontrol-type"></a><span data-ttu-id="41c98-104">InputControl タイプ</span><span class="sxs-lookup"><span data-stu-id="41c98-104">InputControl Type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="41c98-105">すべてのコントロールのメソッドと属性を持つ入力コントロール インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="41c98-105">Input control interface with methods and attributes for all input controls.</span></span>
<span data-ttu-id="41c98-106">入力コントロールは、たとえば新しいコントロールに対するユーザー入力を収集するために通常はタスク ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="41c98-106">Input controls are typically used on task pages for collecting user input, for example, for a new control.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="41c98-107">階層</span><span class="sxs-lookup"><span data-stu-id="41c98-107">Hierarchy</span></span>

[<span data-ttu-id="41c98-108">コントロール</span><span class="sxs-lookup"><span data-stu-id="41c98-108">Control</span></span>](view-model-control-basecontrol-icontrol-icontrol.md) <br><span data-ttu-id="41c98-109">&nbsp;&nbsp;&nbsp;└─ InputControl</span><span class="sxs-lookup"><span data-stu-id="41c98-109">&nbsp;&nbsp;&nbsp;└─ InputControl</span></span> <br><span data-ttu-id="41c98-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Field](view-model-control-field-ifield-ifield.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Field](view-model-control-field-ifield-ifield.md)</span></span> <br><span data-ttu-id="41c98-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ルックアップ](view-model-control-lookup-ilookup-ilookup.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Lookup](view-model-control-lookup-ilookup-ilookup.md)</span></span> <br><span data-ttu-id="41c98-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookup](view-model-control-lookup-imultilookup-imultilookup.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookup](view-model-control-lookup-imultilookup-imultilookup.md)</span></span> <br><span data-ttu-id="41c98-113">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [値](view-model-control-value-ivalue-ivalue.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-113">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Value](view-model-control-value-ivalue-ivalue.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="41c98-114">指数</span><span class="sxs-lookup"><span data-stu-id="41c98-114">Index</span></span>

### <a name="properties"></a><span data-ttu-id="41c98-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="41c98-115">Properties</span></span>

* [<span data-ttu-id="41c98-116">コンテナー</span><span class="sxs-lookup"><span data-stu-id="41c98-116">container</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#container)
* [<span data-ttu-id="41c98-117">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="41c98-117">generic</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#generic)
* [<span data-ttu-id="41c98-118">getDataSource</span><span class="sxs-lookup"><span data-stu-id="41c98-118">getDataSource</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdatasource)
* [<span data-ttu-id="41c98-119">非表示</span><span class="sxs-lookup"><span data-stu-id="41c98-119">hidden</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#hidden)

### <a name="methods"></a><span data-ttu-id="41c98-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="41c98-120">Methods</span></span>

* [<span data-ttu-id="41c98-121">applyDesign</span><span class="sxs-lookup"><span data-stu-id="41c98-121">applyDesign</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#applydesign)
* [<span data-ttu-id="41c98-122">dataContext</span><span class="sxs-lookup"><span data-stu-id="41c98-122">dataContext</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#datacontext)
* [<span data-ttu-id="41c98-123">getDesign</span><span class="sxs-lookup"><span data-stu-id="41c98-123">getDesign</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdesign)
* [<span data-ttu-id="41c98-124">isEditable</span><span class="sxs-lookup"><span data-stu-id="41c98-124">isEditable</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#iseditable)
* [<span data-ttu-id="41c98-125">メタデータ</span><span class="sxs-lookup"><span data-stu-id="41c98-125">metadata</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)
* [<span data-ttu-id="41c98-126">親</span><span class="sxs-lookup"><span data-stu-id="41c98-126">parent</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#parent)
* [<span data-ttu-id="41c98-127">ルート</span><span class="sxs-lookup"><span data-stu-id="41c98-127">root</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#root)

### <a name="events"></a><span data-ttu-id="41c98-128">イベント</span><span class="sxs-lookup"><span data-stu-id="41c98-128">Events</span></span>

* [<span data-ttu-id="41c98-129">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="41c98-129">onDataChanged</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)

## <a name="properties"></a><span data-ttu-id="41c98-130">プロパティ</span><span class="sxs-lookup"><span data-stu-id="41c98-130">Properties</span></span>

### <a name="container"></a><span data-ttu-id="41c98-131">コンテナー</span><span class="sxs-lookup"><span data-stu-id="41c98-131">container</span></span>

<span data-ttu-id="41c98-132">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="41c98-132">container: boolean (optional)</span></span> 

<span data-ttu-id="41c98-133">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="41c98-133">True if the control is a container.</span></span>

> <span data-ttu-id="41c98-134">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-134">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="41c98-135">generic</span><span class="sxs-lookup"><span data-stu-id="41c98-135">generic</span></span>

<span data-ttu-id="41c98-136">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="41c98-136">generic: boolean (optional)</span></span> 



> <span data-ttu-id="41c98-137">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-137">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="41c98-138">getDataSource</span><span class="sxs-lookup"><span data-stu-id="41c98-138">getDataSource</span></span>

<span data-ttu-id="41c98-139">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="41c98-139">getDataSource: function(): any</span></span>



> <span data-ttu-id="41c98-140">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-140">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="41c98-141">hidden</span><span class="sxs-lookup"><span data-stu-id="41c98-141">hidden</span></span>

<span data-ttu-id="41c98-142">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="41c98-142">hidden: boolean</span></span>

<span data-ttu-id="41c98-143">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="41c98-143">True if the control is hidden.</span></span>

> <span data-ttu-id="41c98-144">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-144">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="41c98-145">メソッド</span><span class="sxs-lookup"><span data-stu-id="41c98-145">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="41c98-146">applyDesign</span><span class="sxs-lookup"><span data-stu-id="41c98-146">applyDesign</span></span>


<span data-ttu-id="41c98-147">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="41c98-147">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="41c98-148">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="41c98-148">Applies given design to the design on the control.</span></span>
<span data-ttu-id="41c98-149">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="41c98-149">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="41c98-150">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-150">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="41c98-151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="41c98-151">Parameters</span></span>

| <span data-ttu-id="41c98-152">氏名</span><span class="sxs-lookup"><span data-stu-id="41c98-152">Name</span></span> | <span data-ttu-id="41c98-153">種類</span><span class="sxs-lookup"><span data-stu-id="41c98-153">Type</span></span> | <span data-ttu-id="41c98-154">説明</span><span class="sxs-lookup"><span data-stu-id="41c98-154">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="41c98-155">design</span><span class="sxs-lookup"><span data-stu-id="41c98-155">design</span></span>|[<span data-ttu-id="41c98-156">Design</span><span class="sxs-lookup"><span data-stu-id="41c98-156">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="41c98-157">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="41c98-157">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="41c98-158">void を返します</span><span class="sxs-lookup"><span data-stu-id="41c98-158">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="41c98-159">dataContext</span><span class="sxs-lookup"><span data-stu-id="41c98-159">dataContext</span></span>


<span data-ttu-id="41c98-160">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="41c98-160">dataContext(): any</span></span>



> <span data-ttu-id="41c98-161">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-161">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="41c98-162">any を返します</span><span class="sxs-lookup"><span data-stu-id="41c98-162">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="41c98-163">getDesign</span><span class="sxs-lookup"><span data-stu-id="41c98-163">getDesign</span></span>


<span data-ttu-id="41c98-164">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-164">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="41c98-165">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-165">Returns the design object of this control.</span></span>

> <span data-ttu-id="41c98-166">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-166">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-designview-model-ipage-idesignmd"></a><span data-ttu-id="41c98-167">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="41c98-167">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="iseditable"></a><span data-ttu-id="41c98-168">isEditable</span><span class="sxs-lookup"><span data-stu-id="41c98-168">isEditable</span></span>


<span data-ttu-id="41c98-169">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="41c98-169">isEditable(): boolean</span></span>

<span data-ttu-id="41c98-170">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="41c98-170">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="41c98-171">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-171">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="41c98-172">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-172">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="41c98-173">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-173">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="41c98-174">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-174">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="41c98-175">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-175">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="41c98-176">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="41c98-176">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="41c98-177">metadata</span><span class="sxs-lookup"><span data-stu-id="41c98-177">metadata</span></span>


<span data-ttu-id="41c98-178">metadata(): [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-178">metadata(): [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span></span>

<span data-ttu-id="41c98-179">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-179">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="41c98-180">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="41c98-180">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata)</span></span>

#### <a name="returns-inputcontrolmetadataview-model-control-basecontrol-iinputcontrol-iinputcontrolmetadatamd"></a><span data-ttu-id="41c98-181">[InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="41c98-181">Returns [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="41c98-182">parent</span><span class="sxs-lookup"><span data-stu-id="41c98-182">parent</span></span>


<span data-ttu-id="41c98-183">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-183">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="41c98-184">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-184">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="41c98-185">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-185">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a><span data-ttu-id="41c98-186">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="41c98-186">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="41c98-187">root</span><span class="sxs-lookup"><span data-stu-id="41c98-187">root</span></span>


<span data-ttu-id="41c98-188">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="41c98-188">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="41c98-189">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="41c98-189">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="41c98-190">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="41c98-190">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-pageview-model-ipage-ipagemd"></a><span data-ttu-id="41c98-191">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="41c98-191">Returns [Page](view-model-ipage-ipage.md)</span></span>



## <a name="events"></a><span data-ttu-id="41c98-192">イベント</span><span class="sxs-lookup"><span data-stu-id="41c98-192">Events</span></span>

### <a name="ondatachanged"></a><span data-ttu-id="41c98-193">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="41c98-193">onDataChanged</span></span>

<span data-ttu-id="41c98-194">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span><span class="sxs-lookup"><span data-stu-id="41c98-194">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span></span>

<span data-ttu-id="41c98-195">入力コントロールのデータが変更されたときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="41c98-195">An event that is triggered when the input control's data changes.</span></span>



