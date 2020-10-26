---
title: 値の型
description: 値コントロール型 これは、単一の値のコントロールの基本クラスです。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 535e0c035309ac99f56a5630ba9ce36d8bc79f5b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982759"
---
# <a name="value-type"></a><span data-ttu-id="3eda8-104">値の型</span><span class="sxs-lookup"><span data-stu-id="3eda8-104">Value type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="3eda8-105">値コントロール型</span><span class="sxs-lookup"><span data-stu-id="3eda8-105">Value control type.</span></span> <span data-ttu-id="3eda8-106">これは、単一の値のコントロールの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="3eda8-106">This is the base class for single value controls.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="3eda8-107">階層</span><span class="sxs-lookup"><span data-stu-id="3eda8-107">Hierarchy</span></span>

[<span data-ttu-id="3eda8-108">InputControl</span><span class="sxs-lookup"><span data-stu-id="3eda8-108">InputControl</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br><span data-ttu-id="3eda8-109">&nbsp;&nbsp;&nbsp;└─ 値</span><span class="sxs-lookup"><span data-stu-id="3eda8-109">&nbsp;&nbsp;&nbsp;└─ Value</span></span> <br><span data-ttu-id="3eda8-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span><span class="sxs-lookup"><span data-stu-id="3eda8-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span></span> <br><span data-ttu-id="3eda8-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ハイパーリンク](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span><span class="sxs-lookup"><span data-stu-id="3eda8-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [HyperLink](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span></span> <br><span data-ttu-id="3eda8-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span><span class="sxs-lookup"><span data-stu-id="3eda8-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="3eda8-113">指数</span><span class="sxs-lookup"><span data-stu-id="3eda8-113">Index</span></span>

### <a name="properties"></a><span data-ttu-id="3eda8-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3eda8-114">Properties</span></span>

* [<span data-ttu-id="3eda8-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="3eda8-115">container</span></span>](view-model-control-value-ivalue-ivalue.md#container)
* [<span data-ttu-id="3eda8-116">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="3eda8-116">generic</span></span>](view-model-control-value-ivalue-ivalue.md#generic)
* [<span data-ttu-id="3eda8-117">getDataSource</span><span class="sxs-lookup"><span data-stu-id="3eda8-117">getDataSource</span></span>](view-model-control-value-ivalue-ivalue.md#getdatasource)
* [<span data-ttu-id="3eda8-118">非表示</span><span class="sxs-lookup"><span data-stu-id="3eda8-118">hidden</span></span>](view-model-control-value-ivalue-ivalue.md#hidden)

### <a name="methods"></a><span data-ttu-id="3eda8-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="3eda8-119">Methods</span></span>

* [<span data-ttu-id="3eda8-120">applyDesign</span><span class="sxs-lookup"><span data-stu-id="3eda8-120">applyDesign</span></span>](view-model-control-value-ivalue-ivalue.md#applydesign)
* [<span data-ttu-id="3eda8-121">dataContext</span><span class="sxs-lookup"><span data-stu-id="3eda8-121">dataContext</span></span>](view-model-control-value-ivalue-ivalue.md#datacontext)
* [<span data-ttu-id="3eda8-122">getDesign</span><span class="sxs-lookup"><span data-stu-id="3eda8-122">getDesign</span></span>](view-model-control-value-ivalue-ivalue.md#getdesign)
* [<span data-ttu-id="3eda8-123">getValue</span><span class="sxs-lookup"><span data-stu-id="3eda8-123">getValue</span></span>](view-model-control-value-ivalue-ivalue.md#getvalue)
* [<span data-ttu-id="3eda8-124">isEditable</span><span class="sxs-lookup"><span data-stu-id="3eda8-124">isEditable</span></span>](view-model-control-value-ivalue-ivalue.md#iseditable)
* [<span data-ttu-id="3eda8-125">メタデータ</span><span class="sxs-lookup"><span data-stu-id="3eda8-125">metadata</span></span>](view-model-control-value-ivalue-ivalue.md#metadata)
* [<span data-ttu-id="3eda8-126">親</span><span class="sxs-lookup"><span data-stu-id="3eda8-126">parent</span></span>](view-model-control-value-ivalue-ivalue.md#parent)
* [<span data-ttu-id="3eda8-127">ルート</span><span class="sxs-lookup"><span data-stu-id="3eda8-127">root</span></span>](view-model-control-value-ivalue-ivalue.md#root)
* [<span data-ttu-id="3eda8-128">setValue</span><span class="sxs-lookup"><span data-stu-id="3eda8-128">setValue</span></span>](view-model-control-value-ivalue-ivalue.md#setvalue)

### <a name="events"></a><span data-ttu-id="3eda8-129">イベント</span><span class="sxs-lookup"><span data-stu-id="3eda8-129">Events</span></span>

* [<span data-ttu-id="3eda8-130">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="3eda8-130">onDataChanged</span></span>](view-model-control-value-ivalue-ivalue.md#ondatachanged)

## <a name="properties"></a><span data-ttu-id="3eda8-131">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3eda8-131">Properties</span></span>

### <a name="container"></a><span data-ttu-id="3eda8-132">コンテナー</span><span class="sxs-lookup"><span data-stu-id="3eda8-132">container</span></span>

<span data-ttu-id="3eda8-133">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="3eda8-133">container: boolean (optional)</span></span> 

<span data-ttu-id="3eda8-134">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="3eda8-134">True if the control is a container.</span></span>

> <span data-ttu-id="3eda8-135">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-135">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="3eda8-136">generic</span><span class="sxs-lookup"><span data-stu-id="3eda8-136">generic</span></span>

<span data-ttu-id="3eda8-137">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="3eda8-137">generic: boolean (optional)</span></span> 



> <span data-ttu-id="3eda8-138">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-138">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="3eda8-139">getDataSource</span><span class="sxs-lookup"><span data-stu-id="3eda8-139">getDataSource</span></span>

<span data-ttu-id="3eda8-140">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="3eda8-140">getDataSource: function(): any</span></span>



> <span data-ttu-id="3eda8-141">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-141">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="3eda8-142">hidden</span><span class="sxs-lookup"><span data-stu-id="3eda8-142">hidden</span></span>

<span data-ttu-id="3eda8-143">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="3eda8-143">hidden: boolean</span></span>

<span data-ttu-id="3eda8-144">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="3eda8-144">True if the control is hidden.</span></span>

> <span data-ttu-id="3eda8-145">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-145">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="3eda8-146">メソッド</span><span class="sxs-lookup"><span data-stu-id="3eda8-146">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="3eda8-147">applyDesign</span><span class="sxs-lookup"><span data-stu-id="3eda8-147">applyDesign</span></span>


<span data-ttu-id="3eda8-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="3eda8-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="3eda8-149">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-149">Applies given design to the design on the control.</span></span>
<span data-ttu-id="3eda8-150">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="3eda8-150">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="3eda8-151">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-151">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="3eda8-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3eda8-152">Parameters</span></span>

| <span data-ttu-id="3eda8-153">氏名</span><span class="sxs-lookup"><span data-stu-id="3eda8-153">Name</span></span> | <span data-ttu-id="3eda8-154">種類</span><span class="sxs-lookup"><span data-stu-id="3eda8-154">Type</span></span> | <span data-ttu-id="3eda8-155">説明</span><span class="sxs-lookup"><span data-stu-id="3eda8-155">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="3eda8-156">design</span><span class="sxs-lookup"><span data-stu-id="3eda8-156">design</span></span>|[<span data-ttu-id="3eda8-157">Design</span><span class="sxs-lookup"><span data-stu-id="3eda8-157">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="3eda8-158">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="3eda8-158">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="3eda8-159">void を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-159">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="3eda8-160">dataContext</span><span class="sxs-lookup"><span data-stu-id="3eda8-160">dataContext</span></span>


<span data-ttu-id="3eda8-161">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="3eda8-161">dataContext(): any</span></span>



> <span data-ttu-id="3eda8-162">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-162">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="3eda8-163">any を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-163">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="3eda8-164">getDesign</span><span class="sxs-lookup"><span data-stu-id="3eda8-164">getDesign</span></span>


<span data-ttu-id="3eda8-165">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="3eda8-165">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="3eda8-166">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-166">Returns the design object of this control.</span></span>

> <span data-ttu-id="3eda8-167">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-167">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-design"></a><span data-ttu-id="3eda8-168">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-168">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="getvalue"></a><span data-ttu-id="3eda8-169">getValue</span><span class="sxs-lookup"><span data-stu-id="3eda8-169">getValue</span></span>


<span data-ttu-id="3eda8-170">getValue(): string</span><span class="sxs-lookup"><span data-stu-id="3eda8-170">getValue(): string</span></span>

<span data-ttu-id="3eda8-171">コントロールの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-171">Returns the value of the control.</span></span>

#### <a name="returns-string"></a><span data-ttu-id="3eda8-172">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-172">Returns string</span></span>



### <a name="iseditable"></a><span data-ttu-id="3eda8-173">isEditable</span><span class="sxs-lookup"><span data-stu-id="3eda8-173">isEditable</span></span>


<span data-ttu-id="3eda8-174">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="3eda8-174">isEditable(): boolean</span></span>

<span data-ttu-id="3eda8-175">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3eda8-175">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="3eda8-176">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-176">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="3eda8-177">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-177">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="3eda8-178">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-178">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="3eda8-179">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-179">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="3eda8-180">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-180">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="3eda8-181">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-181">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="3eda8-182">metadata</span><span class="sxs-lookup"><span data-stu-id="3eda8-182">metadata</span></span>


<span data-ttu-id="3eda8-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="3eda8-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>

<span data-ttu-id="3eda8-184">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-184">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="3eda8-185">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3eda8-185">Overrides [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)</span></span>

#### <a name="returns-valuemetadata"></a><span data-ttu-id="3eda8-186">[ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-186">Returns [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="3eda8-187">parent</span><span class="sxs-lookup"><span data-stu-id="3eda8-187">parent</span></span>


<span data-ttu-id="3eda8-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="3eda8-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="3eda8-189">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-189">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="3eda8-190">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-190">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-control-124-page"></a><span data-ttu-id="3eda8-191">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-191">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="3eda8-192">root</span><span class="sxs-lookup"><span data-stu-id="3eda8-192">root</span></span>


<span data-ttu-id="3eda8-193">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="3eda8-193">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="3eda8-194">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-194">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="3eda8-195">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-195">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-page"></a><span data-ttu-id="3eda8-196">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-196">Returns [Page](view-model-ipage-ipage.md)</span></span>



### <a name="setvalue"></a><span data-ttu-id="3eda8-197">setValue</span><span class="sxs-lookup"><span data-stu-id="3eda8-197">setValue</span></span>


<span data-ttu-id="3eda8-198">setValue(value: string): void</span><span class="sxs-lookup"><span data-stu-id="3eda8-198">setValue(value: string): void</span></span>

<span data-ttu-id="3eda8-199">コントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="3eda8-199">Sets the value of the control.</span></span>


#### <a name="parameters"></a><span data-ttu-id="3eda8-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3eda8-200">Parameters</span></span>

| <span data-ttu-id="3eda8-201">氏名</span><span class="sxs-lookup"><span data-stu-id="3eda8-201">Name</span></span> | <span data-ttu-id="3eda8-202">種類</span><span class="sxs-lookup"><span data-stu-id="3eda8-202">Type</span></span> | <span data-ttu-id="3eda8-203">説明</span><span class="sxs-lookup"><span data-stu-id="3eda8-203">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="3eda8-204">値</span><span class="sxs-lookup"><span data-stu-id="3eda8-204">value</span></span>|<span data-ttu-id="3eda8-205">string</span><span class="sxs-lookup"><span data-stu-id="3eda8-205">string</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="3eda8-206">void を返します</span><span class="sxs-lookup"><span data-stu-id="3eda8-206">Returns void</span></span>

## <a name="events"></a><span data-ttu-id="3eda8-207">イベント</span><span class="sxs-lookup"><span data-stu-id="3eda8-207">Events</span></span>

### <a name="ondatachanged"></a><span data-ttu-id="3eda8-208">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="3eda8-208">onDataChanged</span></span>

<span data-ttu-id="3eda8-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span><span class="sxs-lookup"><span data-stu-id="3eda8-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span></span>

<span data-ttu-id="3eda8-210">入力コントロールのデータが変更されたときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="3eda8-210">An event that is triggered when the input control's data changes.</span></span>

> <span data-ttu-id="3eda8-211">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承</span><span class="sxs-lookup"><span data-stu-id="3eda8-211">Inherited from [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)</span></span>


