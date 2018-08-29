---
title: "値の型"
description: "値コントロール型 これは、単一の値のコントロールの基本クラスです。"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 592fadfc4e095e7a52d6ad52db0c32a41c79d756
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="value-type"></a><span data-ttu-id="f3013-104">値の型</span><span class="sxs-lookup"><span data-stu-id="f3013-104">Value type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="f3013-105">値コントロール型</span><span class="sxs-lookup"><span data-stu-id="f3013-105">Value control type.</span></span> <span data-ttu-id="f3013-106">これは、単一の値のコントロールの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="f3013-106">This is the base class for single value controls.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="f3013-107">階層</span><span class="sxs-lookup"><span data-stu-id="f3013-107">Hierarchy</span></span>

[<span data-ttu-id="f3013-108">InputControl</span><span class="sxs-lookup"><span data-stu-id="f3013-108">InputControl</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br><span data-ttu-id="f3013-109">&nbsp;&nbsp;&nbsp;└─ 値</span><span class="sxs-lookup"><span data-stu-id="f3013-109">&nbsp;&nbsp;&nbsp;└─ Value</span></span> <br><span data-ttu-id="f3013-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span><span class="sxs-lookup"><span data-stu-id="f3013-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span></span> <br><span data-ttu-id="f3013-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ハイパーリンク](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span><span class="sxs-lookup"><span data-stu-id="f3013-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [HyperLink](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span></span> <br><span data-ttu-id="f3013-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span><span class="sxs-lookup"><span data-stu-id="f3013-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="f3013-113">指数</span><span class="sxs-lookup"><span data-stu-id="f3013-113">Index</span></span>

### <a name="properties"></a><span data-ttu-id="f3013-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3013-114">Properties</span></span>

* [<span data-ttu-id="f3013-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f3013-115">container</span></span>](view-model-control-value-ivalue-ivalue.md#container)
* [<span data-ttu-id="f3013-116">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="f3013-116">generic</span></span>](view-model-control-value-ivalue-ivalue.md#generic)
* [<span data-ttu-id="f3013-117">getDataSource</span><span class="sxs-lookup"><span data-stu-id="f3013-117">getDataSource</span></span>](view-model-control-value-ivalue-ivalue.md#getdatasource)
* [<span data-ttu-id="f3013-118">非表示</span><span class="sxs-lookup"><span data-stu-id="f3013-118">hidden</span></span>](view-model-control-value-ivalue-ivalue.md#hidden)

### <a name="methods"></a><span data-ttu-id="f3013-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="f3013-119">Methods</span></span>

* [<span data-ttu-id="f3013-120">applyDesign</span><span class="sxs-lookup"><span data-stu-id="f3013-120">applyDesign</span></span>](view-model-control-value-ivalue-ivalue.md#applydesign)
* [<span data-ttu-id="f3013-121">dataContext</span><span class="sxs-lookup"><span data-stu-id="f3013-121">dataContext</span></span>](view-model-control-value-ivalue-ivalue.md#datacontext)
* [<span data-ttu-id="f3013-122">getDesign</span><span class="sxs-lookup"><span data-stu-id="f3013-122">getDesign</span></span>](view-model-control-value-ivalue-ivalue.md#getdesign)
* [<span data-ttu-id="f3013-123">getValue</span><span class="sxs-lookup"><span data-stu-id="f3013-123">getValue</span></span>](view-model-control-value-ivalue-ivalue.md#getvalue)
* [<span data-ttu-id="f3013-124">isEditable</span><span class="sxs-lookup"><span data-stu-id="f3013-124">isEditable</span></span>](view-model-control-value-ivalue-ivalue.md#iseditable)
* [<span data-ttu-id="f3013-125">メタデータ</span><span class="sxs-lookup"><span data-stu-id="f3013-125">metadata</span></span>](view-model-control-value-ivalue-ivalue.md#metadata)
* [<span data-ttu-id="f3013-126">親</span><span class="sxs-lookup"><span data-stu-id="f3013-126">parent</span></span>](view-model-control-value-ivalue-ivalue.md#parent)
* [<span data-ttu-id="f3013-127">ルート</span><span class="sxs-lookup"><span data-stu-id="f3013-127">root</span></span>](view-model-control-value-ivalue-ivalue.md#root)
* [<span data-ttu-id="f3013-128">setValue</span><span class="sxs-lookup"><span data-stu-id="f3013-128">setValue</span></span>](view-model-control-value-ivalue-ivalue.md#setvalue)

### <a name="events"></a><span data-ttu-id="f3013-129">イベント</span><span class="sxs-lookup"><span data-stu-id="f3013-129">Events</span></span>

* [<span data-ttu-id="f3013-130">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="f3013-130">onDataChanged</span></span>](view-model-control-value-ivalue-ivalue.md#ondatachanged)

## <a name="properties"></a><span data-ttu-id="f3013-131">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3013-131">Properties</span></span>

### <a name="container"></a><span data-ttu-id="f3013-132">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f3013-132">container</span></span>

<span data-ttu-id="f3013-133">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="f3013-133">container: boolean (optional)</span></span> 

<span data-ttu-id="f3013-134">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="f3013-134">True if the control is a container.</span></span>

> <span data-ttu-id="f3013-135">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-135">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="f3013-136">generic</span><span class="sxs-lookup"><span data-stu-id="f3013-136">generic</span></span>

<span data-ttu-id="f3013-137">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="f3013-137">generic: boolean (optional)</span></span> 



> <span data-ttu-id="f3013-138">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-138">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="f3013-139">getDataSource</span><span class="sxs-lookup"><span data-stu-id="f3013-139">getDataSource</span></span>

<span data-ttu-id="f3013-140">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="f3013-140">getDataSource: function(): any</span></span>



> <span data-ttu-id="f3013-141">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-141">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="f3013-142">hidden</span><span class="sxs-lookup"><span data-stu-id="f3013-142">hidden</span></span>

<span data-ttu-id="f3013-143">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="f3013-143">hidden: boolean</span></span>

<span data-ttu-id="f3013-144">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="f3013-144">True if the control is hidden.</span></span>

> <span data-ttu-id="f3013-145">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-145">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="f3013-146">メソッド</span><span class="sxs-lookup"><span data-stu-id="f3013-146">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="f3013-147">applyDesign</span><span class="sxs-lookup"><span data-stu-id="f3013-147">applyDesign</span></span>


<span data-ttu-id="f3013-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="f3013-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="f3013-149">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="f3013-149">Applies given design to the design on the control.</span></span>
<span data-ttu-id="f3013-150">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="f3013-150">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="f3013-151">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-151">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="f3013-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f3013-152">Parameters</span></span>

| <span data-ttu-id="f3013-153">氏名</span><span class="sxs-lookup"><span data-stu-id="f3013-153">Name</span></span> | <span data-ttu-id="f3013-154">種類</span><span class="sxs-lookup"><span data-stu-id="f3013-154">Type</span></span> | <span data-ttu-id="f3013-155">説明</span><span class="sxs-lookup"><span data-stu-id="f3013-155">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f3013-156">design</span><span class="sxs-lookup"><span data-stu-id="f3013-156">design</span></span>|[<span data-ttu-id="f3013-157">Design</span><span class="sxs-lookup"><span data-stu-id="f3013-157">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="f3013-158">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="f3013-158">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="f3013-159">void を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-159">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="f3013-160">dataContext</span><span class="sxs-lookup"><span data-stu-id="f3013-160">dataContext</span></span>


<span data-ttu-id="f3013-161">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="f3013-161">dataContext(): any</span></span>



> <span data-ttu-id="f3013-162">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-162">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="f3013-163">any を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-163">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="f3013-164">getDesign</span><span class="sxs-lookup"><span data-stu-id="f3013-164">getDesign</span></span>


<span data-ttu-id="f3013-165">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="f3013-165">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="f3013-166">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-166">Returns the design object of this control.</span></span>

> <span data-ttu-id="f3013-167">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-167">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-designview-model-ipage-idesignmd"></a><span data-ttu-id="f3013-168">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-168">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="getvalue"></a><span data-ttu-id="f3013-169">getValue</span><span class="sxs-lookup"><span data-stu-id="f3013-169">getValue</span></span>


<span data-ttu-id="f3013-170">getValue(): string</span><span class="sxs-lookup"><span data-stu-id="f3013-170">getValue(): string</span></span>

<span data-ttu-id="f3013-171">コントロールの値を返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-171">Returns the value of the control.</span></span>

#### <a name="returns-string"></a><span data-ttu-id="f3013-172">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-172">Returns string</span></span>



### <a name="iseditable"></a><span data-ttu-id="f3013-173">isEditable</span><span class="sxs-lookup"><span data-stu-id="f3013-173">isEditable</span></span>


<span data-ttu-id="f3013-174">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="f3013-174">isEditable(): boolean</span></span>

<span data-ttu-id="f3013-175">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3013-175">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="f3013-176">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-176">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="f3013-177">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-177">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="f3013-178">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-178">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="f3013-179">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-179">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="f3013-180">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-180">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="f3013-181">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-181">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="f3013-182">metadata</span><span class="sxs-lookup"><span data-stu-id="f3013-182">metadata</span></span>


<span data-ttu-id="f3013-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="f3013-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>

<span data-ttu-id="f3013-184">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-184">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="f3013-185">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="f3013-185">Overrides [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)</span></span>

#### <a name="returns-valuemetadataview-model-control-value-ivalue-ivaluemetadatamd"></a><span data-ttu-id="f3013-186">[ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-186">Returns [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="f3013-187">parent</span><span class="sxs-lookup"><span data-stu-id="f3013-187">parent</span></span>


<span data-ttu-id="f3013-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="f3013-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="f3013-189">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-189">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="f3013-190">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-190">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a><span data-ttu-id="f3013-191">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-191">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="f3013-192">root</span><span class="sxs-lookup"><span data-stu-id="f3013-192">root</span></span>


<span data-ttu-id="f3013-193">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="f3013-193">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="f3013-194">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="f3013-194">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="f3013-195">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-195">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-pageview-model-ipage-ipagemd"></a><span data-ttu-id="f3013-196">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-196">Returns [Page](view-model-ipage-ipage.md)</span></span>



### <a name="setvalue"></a><span data-ttu-id="f3013-197">setValue</span><span class="sxs-lookup"><span data-stu-id="f3013-197">setValue</span></span>


<span data-ttu-id="f3013-198">setValue(value: string): void</span><span class="sxs-lookup"><span data-stu-id="f3013-198">setValue(value: string): void</span></span>

<span data-ttu-id="f3013-199">コントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="f3013-199">Sets the value of the control.</span></span>


#### <a name="parameters"></a><span data-ttu-id="f3013-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f3013-200">Parameters</span></span>

| <span data-ttu-id="f3013-201">氏名</span><span class="sxs-lookup"><span data-stu-id="f3013-201">Name</span></span> | <span data-ttu-id="f3013-202">種類</span><span class="sxs-lookup"><span data-stu-id="f3013-202">Type</span></span> | <span data-ttu-id="f3013-203">説明</span><span class="sxs-lookup"><span data-stu-id="f3013-203">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f3013-204">値</span><span class="sxs-lookup"><span data-stu-id="f3013-204">value</span></span>|<span data-ttu-id="f3013-205">string</span><span class="sxs-lookup"><span data-stu-id="f3013-205">string</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="f3013-206">void を返します</span><span class="sxs-lookup"><span data-stu-id="f3013-206">Returns void</span></span>

## <a name="events"></a><span data-ttu-id="f3013-207">イベント</span><span class="sxs-lookup"><span data-stu-id="f3013-207">Events</span></span>

### <a name="ondatachanged"></a><span data-ttu-id="f3013-208">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="f3013-208">onDataChanged</span></span>

<span data-ttu-id="f3013-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span><span class="sxs-lookup"><span data-stu-id="f3013-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span></span>

<span data-ttu-id="f3013-210">入力コントロールのデータが変更されたときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="f3013-210">An event that is triggered when the input control's data changes.</span></span>

> <span data-ttu-id="f3013-211">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承</span><span class="sxs-lookup"><span data-stu-id="f3013-211">Inherited from [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)</span></span>



