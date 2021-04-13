---
title: 値の型
description: 値コントロール型 これは、単一の値のコントロールの基本クラスです。
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
ms.openlocfilehash: 55772fbf4be36413900914255841989d805a96b5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752692"
---
# <a name="value-type"></a><span data-ttu-id="7bf89-104">値の型</span><span class="sxs-lookup"><span data-stu-id="7bf89-104">Value type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="7bf89-105">値コントロール型</span><span class="sxs-lookup"><span data-stu-id="7bf89-105">Value control type.</span></span> <span data-ttu-id="7bf89-106">これは、単一の値のコントロールの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="7bf89-106">This is the base class for single value controls.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="7bf89-107">階層</span><span class="sxs-lookup"><span data-stu-id="7bf89-107">Hierarchy</span></span>

[<span data-ttu-id="7bf89-108">InputControl</span><span class="sxs-lookup"><span data-stu-id="7bf89-108">InputControl</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br><span data-ttu-id="7bf89-109">&nbsp;&nbsp;&nbsp;└─ 値</span><span class="sxs-lookup"><span data-stu-id="7bf89-109">&nbsp;&nbsp;&nbsp;└─ Value</span></span> <br><span data-ttu-id="7bf89-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span><span class="sxs-lookup"><span data-stu-id="7bf89-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span></span> <br><span data-ttu-id="7bf89-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ハイパーリンク](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span><span class="sxs-lookup"><span data-stu-id="7bf89-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [HyperLink](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span></span> <br><span data-ttu-id="7bf89-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span><span class="sxs-lookup"><span data-stu-id="7bf89-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="7bf89-113">指数</span><span class="sxs-lookup"><span data-stu-id="7bf89-113">Index</span></span>

### <a name="properties"></a><span data-ttu-id="7bf89-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bf89-114">Properties</span></span>

* [<span data-ttu-id="7bf89-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7bf89-115">container</span></span>](view-model-control-value-ivalue-ivalue.md#container)
* [<span data-ttu-id="7bf89-116">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="7bf89-116">generic</span></span>](view-model-control-value-ivalue-ivalue.md#generic)
* [<span data-ttu-id="7bf89-117">getDataSource</span><span class="sxs-lookup"><span data-stu-id="7bf89-117">getDataSource</span></span>](view-model-control-value-ivalue-ivalue.md#getdatasource)
* [<span data-ttu-id="7bf89-118">非表示</span><span class="sxs-lookup"><span data-stu-id="7bf89-118">hidden</span></span>](view-model-control-value-ivalue-ivalue.md#hidden)

### <a name="methods"></a><span data-ttu-id="7bf89-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="7bf89-119">Methods</span></span>

* [<span data-ttu-id="7bf89-120">applyDesign</span><span class="sxs-lookup"><span data-stu-id="7bf89-120">applyDesign</span></span>](view-model-control-value-ivalue-ivalue.md#applydesign)
* [<span data-ttu-id="7bf89-121">dataContext</span><span class="sxs-lookup"><span data-stu-id="7bf89-121">dataContext</span></span>](view-model-control-value-ivalue-ivalue.md#datacontext)
* [<span data-ttu-id="7bf89-122">getDesign</span><span class="sxs-lookup"><span data-stu-id="7bf89-122">getDesign</span></span>](view-model-control-value-ivalue-ivalue.md#getdesign)
* [<span data-ttu-id="7bf89-123">getValue</span><span class="sxs-lookup"><span data-stu-id="7bf89-123">getValue</span></span>](view-model-control-value-ivalue-ivalue.md#getvalue)
* [<span data-ttu-id="7bf89-124">isEditable</span><span class="sxs-lookup"><span data-stu-id="7bf89-124">isEditable</span></span>](view-model-control-value-ivalue-ivalue.md#iseditable)
* [<span data-ttu-id="7bf89-125">メタデータ</span><span class="sxs-lookup"><span data-stu-id="7bf89-125">metadata</span></span>](view-model-control-value-ivalue-ivalue.md#metadata)
* [<span data-ttu-id="7bf89-126">親</span><span class="sxs-lookup"><span data-stu-id="7bf89-126">parent</span></span>](view-model-control-value-ivalue-ivalue.md#parent)
* [<span data-ttu-id="7bf89-127">ルート</span><span class="sxs-lookup"><span data-stu-id="7bf89-127">root</span></span>](view-model-control-value-ivalue-ivalue.md#root)
* [<span data-ttu-id="7bf89-128">setValue</span><span class="sxs-lookup"><span data-stu-id="7bf89-128">setValue</span></span>](view-model-control-value-ivalue-ivalue.md#setvalue)

### <a name="events"></a><span data-ttu-id="7bf89-129">イベント</span><span class="sxs-lookup"><span data-stu-id="7bf89-129">Events</span></span>

* [<span data-ttu-id="7bf89-130">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="7bf89-130">onDataChanged</span></span>](view-model-control-value-ivalue-ivalue.md#ondatachanged)

## <a name="properties"></a><span data-ttu-id="7bf89-131">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bf89-131">Properties</span></span>

### <a name="container"></a><span data-ttu-id="7bf89-132">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7bf89-132">container</span></span>

<span data-ttu-id="7bf89-133">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="7bf89-133">container: boolean (optional)</span></span> 

<span data-ttu-id="7bf89-134">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="7bf89-134">True if the control is a container.</span></span>

> <span data-ttu-id="7bf89-135">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-135">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="7bf89-136">generic</span><span class="sxs-lookup"><span data-stu-id="7bf89-136">generic</span></span>

<span data-ttu-id="7bf89-137">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="7bf89-137">generic: boolean (optional)</span></span> 



> <span data-ttu-id="7bf89-138">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-138">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="7bf89-139">getDataSource</span><span class="sxs-lookup"><span data-stu-id="7bf89-139">getDataSource</span></span>

<span data-ttu-id="7bf89-140">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="7bf89-140">getDataSource: function(): any</span></span>



> <span data-ttu-id="7bf89-141">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-141">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="7bf89-142">hidden</span><span class="sxs-lookup"><span data-stu-id="7bf89-142">hidden</span></span>

<span data-ttu-id="7bf89-143">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="7bf89-143">hidden: boolean</span></span>

<span data-ttu-id="7bf89-144">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="7bf89-144">True if the control is hidden.</span></span>

> <span data-ttu-id="7bf89-145">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-145">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="7bf89-146">メソッド</span><span class="sxs-lookup"><span data-stu-id="7bf89-146">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="7bf89-147">applyDesign</span><span class="sxs-lookup"><span data-stu-id="7bf89-147">applyDesign</span></span>


<span data-ttu-id="7bf89-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="7bf89-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="7bf89-149">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-149">Applies given design to the design on the control.</span></span>
<span data-ttu-id="7bf89-150">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="7bf89-150">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="7bf89-151">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-151">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="7bf89-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7bf89-152">Parameters</span></span>

| <span data-ttu-id="7bf89-153">氏名</span><span class="sxs-lookup"><span data-stu-id="7bf89-153">Name</span></span> | <span data-ttu-id="7bf89-154">種類</span><span class="sxs-lookup"><span data-stu-id="7bf89-154">Type</span></span> | <span data-ttu-id="7bf89-155">説明</span><span class="sxs-lookup"><span data-stu-id="7bf89-155">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="7bf89-156">design</span><span class="sxs-lookup"><span data-stu-id="7bf89-156">design</span></span>|[<span data-ttu-id="7bf89-157">Design</span><span class="sxs-lookup"><span data-stu-id="7bf89-157">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="7bf89-158">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="7bf89-158">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="7bf89-159">void を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-159">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="7bf89-160">dataContext</span><span class="sxs-lookup"><span data-stu-id="7bf89-160">dataContext</span></span>


<span data-ttu-id="7bf89-161">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="7bf89-161">dataContext(): any</span></span>



> <span data-ttu-id="7bf89-162">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-162">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="7bf89-163">any を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-163">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="7bf89-164">getDesign</span><span class="sxs-lookup"><span data-stu-id="7bf89-164">getDesign</span></span>


<span data-ttu-id="7bf89-165">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="7bf89-165">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="7bf89-166">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-166">Returns the design object of this control.</span></span>

> <span data-ttu-id="7bf89-167">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-167">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-design"></a><span data-ttu-id="7bf89-168">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-168">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="getvalue"></a><span data-ttu-id="7bf89-169">getValue</span><span class="sxs-lookup"><span data-stu-id="7bf89-169">getValue</span></span>


<span data-ttu-id="7bf89-170">getValue(): string</span><span class="sxs-lookup"><span data-stu-id="7bf89-170">getValue(): string</span></span>

<span data-ttu-id="7bf89-171">コントロールの値を返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-171">Returns the value of the control.</span></span>

#### <a name="returns-string"></a><span data-ttu-id="7bf89-172">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-172">Returns string</span></span>



### <a name="iseditable"></a><span data-ttu-id="7bf89-173">isEditable</span><span class="sxs-lookup"><span data-stu-id="7bf89-173">isEditable</span></span>


<span data-ttu-id="7bf89-174">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="7bf89-174">isEditable(): boolean</span></span>

<span data-ttu-id="7bf89-175">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7bf89-175">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="7bf89-176">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-176">Returns false when either the control or its parent is not editable.</span></span>
<span data-ttu-id="7bf89-177">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-177">Returns true when both the control and its parent are editable.</span></span>
<span data-ttu-id="7bf89-178">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-178">Returns true when either the control or its parent is editable and the other is undefined.</span></span>
<span data-ttu-id="7bf89-179">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-179">Returns undefined if both the control's edit-ability and its parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="7bf89-180">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-180">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="7bf89-181">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-181">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="7bf89-182">metadata</span><span class="sxs-lookup"><span data-stu-id="7bf89-182">metadata</span></span>


<span data-ttu-id="7bf89-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="7bf89-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>

<span data-ttu-id="7bf89-184">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-184">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="7bf89-185">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="7bf89-185">Overrides [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)</span></span>

#### <a name="returns-valuemetadata"></a><span data-ttu-id="7bf89-186">[ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-186">Returns [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="7bf89-187">parent</span><span class="sxs-lookup"><span data-stu-id="7bf89-187">parent</span></span>


<span data-ttu-id="7bf89-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="7bf89-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="7bf89-189">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-189">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="7bf89-190">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-190">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-control-124-page"></a><span data-ttu-id="7bf89-191">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-191">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="7bf89-192">root</span><span class="sxs-lookup"><span data-stu-id="7bf89-192">root</span></span>


<span data-ttu-id="7bf89-193">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="7bf89-193">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="7bf89-194">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-194">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="7bf89-195">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-195">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-page"></a><span data-ttu-id="7bf89-196">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-196">Returns [Page](view-model-ipage-ipage.md)</span></span>



### <a name="setvalue"></a><span data-ttu-id="7bf89-197">setValue</span><span class="sxs-lookup"><span data-stu-id="7bf89-197">setValue</span></span>


<span data-ttu-id="7bf89-198">setValue(value: string): void</span><span class="sxs-lookup"><span data-stu-id="7bf89-198">setValue(value: string): void</span></span>

<span data-ttu-id="7bf89-199">コントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="7bf89-199">Sets the value of the control.</span></span>


#### <a name="parameters"></a><span data-ttu-id="7bf89-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7bf89-200">Parameters</span></span>

| <span data-ttu-id="7bf89-201">氏名</span><span class="sxs-lookup"><span data-stu-id="7bf89-201">Name</span></span> | <span data-ttu-id="7bf89-202">種類</span><span class="sxs-lookup"><span data-stu-id="7bf89-202">Type</span></span> | <span data-ttu-id="7bf89-203">説明</span><span class="sxs-lookup"><span data-stu-id="7bf89-203">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="7bf89-204">値</span><span class="sxs-lookup"><span data-stu-id="7bf89-204">value</span></span>|<span data-ttu-id="7bf89-205">string</span><span class="sxs-lookup"><span data-stu-id="7bf89-205">string</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="7bf89-206">void を返します</span><span class="sxs-lookup"><span data-stu-id="7bf89-206">Returns void</span></span>

## <a name="events"></a><span data-ttu-id="7bf89-207">イベント</span><span class="sxs-lookup"><span data-stu-id="7bf89-207">Events</span></span>

### <a name="ondatachanged"></a><span data-ttu-id="7bf89-208">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="7bf89-208">onDataChanged</span></span>

<span data-ttu-id="7bf89-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span><span class="sxs-lookup"><span data-stu-id="7bf89-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span></span>

<span data-ttu-id="7bf89-210">入力コントロールのデータが変更されたときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="7bf89-210">An event that is triggered when the input control's data changes.</span></span>

> <span data-ttu-id="7bf89-211">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承</span><span class="sxs-lookup"><span data-stu-id="7bf89-211">Inherited from [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)</span></span>




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]