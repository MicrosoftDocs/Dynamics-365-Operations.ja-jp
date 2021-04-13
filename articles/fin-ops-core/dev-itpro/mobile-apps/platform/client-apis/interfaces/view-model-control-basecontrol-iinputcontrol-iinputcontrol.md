---
title: InputControl タイプ
description: すべてのコントロールのメソッドと属性を持つ入力コントロール インターフェイス。
author: robinarh
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 32e902a9a113f0f4735ce63bb10d5cefecf0f9a8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748085"
---
# <a name="inputcontrol-type"></a><span data-ttu-id="10607-103">InputControl タイプ</span><span class="sxs-lookup"><span data-stu-id="10607-103">InputControl type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="10607-104">すべてのコントロールのメソッドと属性を持つ入力コントロール インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="10607-104">Input control interface with methods and attributes for all input controls.</span></span>
<span data-ttu-id="10607-105">入力コントロールは、たとえば新しいコントロールに対するユーザー入力を収集するために通常はタスク ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="10607-105">Input controls are typically used on task pages for collecting user input, for example, for a new control.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="10607-106">階層</span><span class="sxs-lookup"><span data-stu-id="10607-106">Hierarchy</span></span>

[<span data-ttu-id="10607-107">コントロール</span><span class="sxs-lookup"><span data-stu-id="10607-107">Control</span></span>](view-model-control-basecontrol-icontrol-icontrol.md) <br><span data-ttu-id="10607-108">&nbsp;&nbsp;&nbsp;└─ InputControl</span><span class="sxs-lookup"><span data-stu-id="10607-108">&nbsp;&nbsp;&nbsp;└─ InputControl</span></span> <br><span data-ttu-id="10607-109">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Field](view-model-control-field-ifield-ifield.md)</span><span class="sxs-lookup"><span data-stu-id="10607-109">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Field](view-model-control-field-ifield-ifield.md)</span></span> <br><span data-ttu-id="10607-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ルックアップ](view-model-control-lookup-ilookup-ilookup.md)</span><span class="sxs-lookup"><span data-stu-id="10607-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Lookup](view-model-control-lookup-ilookup-ilookup.md)</span></span> <br><span data-ttu-id="10607-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookup](view-model-control-lookup-imultilookup-imultilookup.md)</span><span class="sxs-lookup"><span data-stu-id="10607-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookup](view-model-control-lookup-imultilookup-imultilookup.md)</span></span> <br><span data-ttu-id="10607-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [値](view-model-control-value-ivalue-ivalue.md)</span><span class="sxs-lookup"><span data-stu-id="10607-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Value](view-model-control-value-ivalue-ivalue.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="10607-113">指数</span><span class="sxs-lookup"><span data-stu-id="10607-113">Index</span></span>

### <a name="properties"></a><span data-ttu-id="10607-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="10607-114">Properties</span></span>

* [<span data-ttu-id="10607-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="10607-115">container</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#container)
* [<span data-ttu-id="10607-116">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="10607-116">generic</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#generic)
* [<span data-ttu-id="10607-117">getDataSource</span><span class="sxs-lookup"><span data-stu-id="10607-117">getDataSource</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdatasource)
* [<span data-ttu-id="10607-118">非表示</span><span class="sxs-lookup"><span data-stu-id="10607-118">hidden</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#hidden)

### <a name="methods"></a><span data-ttu-id="10607-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="10607-119">Methods</span></span>

* [<span data-ttu-id="10607-120">applyDesign</span><span class="sxs-lookup"><span data-stu-id="10607-120">applyDesign</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#applydesign)
* [<span data-ttu-id="10607-121">dataContext</span><span class="sxs-lookup"><span data-stu-id="10607-121">dataContext</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#datacontext)
* [<span data-ttu-id="10607-122">getDesign</span><span class="sxs-lookup"><span data-stu-id="10607-122">getDesign</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdesign)
* [<span data-ttu-id="10607-123">isEditable</span><span class="sxs-lookup"><span data-stu-id="10607-123">isEditable</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#iseditable)
* [<span data-ttu-id="10607-124">メタデータ</span><span class="sxs-lookup"><span data-stu-id="10607-124">metadata</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)
* [<span data-ttu-id="10607-125">親</span><span class="sxs-lookup"><span data-stu-id="10607-125">parent</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#parent)
* [<span data-ttu-id="10607-126">ルート</span><span class="sxs-lookup"><span data-stu-id="10607-126">root</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#root)

### <a name="events"></a><span data-ttu-id="10607-127">イベント</span><span class="sxs-lookup"><span data-stu-id="10607-127">Events</span></span>

* [<span data-ttu-id="10607-128">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="10607-128">onDataChanged</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)

## <a name="properties"></a><span data-ttu-id="10607-129">プロパティ</span><span class="sxs-lookup"><span data-stu-id="10607-129">Properties</span></span>

### <a name="container"></a><span data-ttu-id="10607-130">コンテナー</span><span class="sxs-lookup"><span data-stu-id="10607-130">container</span></span>

<span data-ttu-id="10607-131">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="10607-131">container: boolean (optional)</span></span> 

<span data-ttu-id="10607-132">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="10607-132">True if the control is a container.</span></span>

> <span data-ttu-id="10607-133">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-133">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="10607-134">generic</span><span class="sxs-lookup"><span data-stu-id="10607-134">generic</span></span>

<span data-ttu-id="10607-135">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="10607-135">generic: boolean (optional)</span></span> 



> <span data-ttu-id="10607-136">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-136">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="10607-137">getDataSource</span><span class="sxs-lookup"><span data-stu-id="10607-137">getDataSource</span></span>

<span data-ttu-id="10607-138">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="10607-138">getDataSource: function(): any</span></span>



> <span data-ttu-id="10607-139">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-139">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="10607-140">hidden</span><span class="sxs-lookup"><span data-stu-id="10607-140">hidden</span></span>

<span data-ttu-id="10607-141">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="10607-141">hidden: boolean</span></span>

<span data-ttu-id="10607-142">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="10607-142">True if the control is hidden.</span></span>

> <span data-ttu-id="10607-143">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-143">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="10607-144">メソッド</span><span class="sxs-lookup"><span data-stu-id="10607-144">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="10607-145">applyDesign</span><span class="sxs-lookup"><span data-stu-id="10607-145">applyDesign</span></span>


<span data-ttu-id="10607-146">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="10607-146">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="10607-147">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="10607-147">Applies given design to the design on the control.</span></span>
<span data-ttu-id="10607-148">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="10607-148">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="10607-149">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-149">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="10607-150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="10607-150">Parameters</span></span>

| <span data-ttu-id="10607-151">氏名</span><span class="sxs-lookup"><span data-stu-id="10607-151">Name</span></span> | <span data-ttu-id="10607-152">種類</span><span class="sxs-lookup"><span data-stu-id="10607-152">Type</span></span> | <span data-ttu-id="10607-153">説明</span><span class="sxs-lookup"><span data-stu-id="10607-153">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="10607-154">design</span><span class="sxs-lookup"><span data-stu-id="10607-154">design</span></span>|[<span data-ttu-id="10607-155">Design</span><span class="sxs-lookup"><span data-stu-id="10607-155">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="10607-156">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="10607-156">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="10607-157">void を返します</span><span class="sxs-lookup"><span data-stu-id="10607-157">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="10607-158">dataContext</span><span class="sxs-lookup"><span data-stu-id="10607-158">dataContext</span></span>


<span data-ttu-id="10607-159">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="10607-159">dataContext(): any</span></span>



> <span data-ttu-id="10607-160">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-160">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="10607-161">any を返します</span><span class="sxs-lookup"><span data-stu-id="10607-161">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="10607-162">getDesign</span><span class="sxs-lookup"><span data-stu-id="10607-162">getDesign</span></span>


<span data-ttu-id="10607-163">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="10607-163">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="10607-164">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="10607-164">Returns the design object of this control.</span></span>

> <span data-ttu-id="10607-165">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-165">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-design"></a><span data-ttu-id="10607-166">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="10607-166">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="iseditable"></a><span data-ttu-id="10607-167">isEditable</span><span class="sxs-lookup"><span data-stu-id="10607-167">isEditable</span></span>


<span data-ttu-id="10607-168">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="10607-168">isEditable(): boolean</span></span>

<span data-ttu-id="10607-169">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="10607-169">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="10607-170">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="10607-170">Returns false when either the control or its parent is not editable.</span></span>
<span data-ttu-id="10607-171">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="10607-171">Returns true when both the control and its parent are editable.</span></span>
<span data-ttu-id="10607-172">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="10607-172">Returns true when either the control or its parent is editable and the other is undefined.</span></span>
<span data-ttu-id="10607-173">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="10607-173">Returns undefined if both the control's edit-ability and its parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="10607-174">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-174">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="10607-175">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="10607-175">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="10607-176">metadata</span><span class="sxs-lookup"><span data-stu-id="10607-176">metadata</span></span>


<span data-ttu-id="10607-177">metadata(): [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="10607-177">metadata(): [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span></span>

<span data-ttu-id="10607-178">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="10607-178">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="10607-179">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="10607-179">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata)</span></span>

#### <a name="returns-inputcontrolmetadata"></a><span data-ttu-id="10607-180">[InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="10607-180">Returns [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="10607-181">parent</span><span class="sxs-lookup"><span data-stu-id="10607-181">parent</span></span>


<span data-ttu-id="10607-182">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="10607-182">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="10607-183">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="10607-183">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="10607-184">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-184">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-control-124-page"></a><span data-ttu-id="10607-185">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="10607-185">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="10607-186">root</span><span class="sxs-lookup"><span data-stu-id="10607-186">root</span></span>


<span data-ttu-id="10607-187">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="10607-187">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="10607-188">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="10607-188">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="10607-189">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="10607-189">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-page"></a><span data-ttu-id="10607-190">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="10607-190">Returns [Page](view-model-ipage-ipage.md)</span></span>



## <a name="events"></a><span data-ttu-id="10607-191">イベント</span><span class="sxs-lookup"><span data-stu-id="10607-191">Events</span></span>

### <a name="ondatachanged"></a><span data-ttu-id="10607-192">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="10607-192">onDataChanged</span></span>

<span data-ttu-id="10607-193">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span><span class="sxs-lookup"><span data-stu-id="10607-193">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span></span>

<span data-ttu-id="10607-194">入力コントロールのデータが変更されたときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="10607-194">An event that is triggered when the input control's data changes.</span></span>




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]