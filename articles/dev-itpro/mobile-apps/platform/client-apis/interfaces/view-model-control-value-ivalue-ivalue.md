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
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14b1ca86f287897aa197618288ccdf1206aecf93
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851537"
---
# <a name="value-type"></a><span data-ttu-id="80425-104">値の型</span><span class="sxs-lookup"><span data-stu-id="80425-104">Value type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="80425-105">値コントロール型</span><span class="sxs-lookup"><span data-stu-id="80425-105">Value control type.</span></span> <span data-ttu-id="80425-106">これは、単一の値のコントロールの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="80425-106">This is the base class for single value controls.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="80425-107">階層</span><span class="sxs-lookup"><span data-stu-id="80425-107">Hierarchy</span></span>

[<span data-ttu-id="80425-108">InputControl</span><span class="sxs-lookup"><span data-stu-id="80425-108">InputControl</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br><span data-ttu-id="80425-109">&nbsp;&nbsp;&nbsp;└─ 値</span><span class="sxs-lookup"><span data-stu-id="80425-109">&nbsp;&nbsp;&nbsp;└─ Value</span></span> <br><span data-ttu-id="80425-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span><span class="sxs-lookup"><span data-stu-id="80425-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FileUploader](view-model-control-fileuploader-ifileuploader-ifileuploader.md)</span></span> <br><span data-ttu-id="80425-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ハイパーリンク](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span><span class="sxs-lookup"><span data-stu-id="80425-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [HyperLink](view-model-control-hyperlink-ihyperlink-ihyperlink.md)</span></span> <br><span data-ttu-id="80425-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span><span class="sxs-lookup"><span data-stu-id="80425-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [GenericValue](view-model-control-value-ivalue-igenericvalue.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="80425-113">指数</span><span class="sxs-lookup"><span data-stu-id="80425-113">Index</span></span>

### <a name="properties"></a><span data-ttu-id="80425-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="80425-114">Properties</span></span>

* [<span data-ttu-id="80425-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="80425-115">container</span></span>](view-model-control-value-ivalue-ivalue.md#container)
* [<span data-ttu-id="80425-116">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="80425-116">generic</span></span>](view-model-control-value-ivalue-ivalue.md#generic)
* [<span data-ttu-id="80425-117">getDataSource</span><span class="sxs-lookup"><span data-stu-id="80425-117">getDataSource</span></span>](view-model-control-value-ivalue-ivalue.md#getdatasource)
* [<span data-ttu-id="80425-118">非表示</span><span class="sxs-lookup"><span data-stu-id="80425-118">hidden</span></span>](view-model-control-value-ivalue-ivalue.md#hidden)

### <a name="methods"></a><span data-ttu-id="80425-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="80425-119">Methods</span></span>

* [<span data-ttu-id="80425-120">applyDesign</span><span class="sxs-lookup"><span data-stu-id="80425-120">applyDesign</span></span>](view-model-control-value-ivalue-ivalue.md#applydesign)
* [<span data-ttu-id="80425-121">dataContext</span><span class="sxs-lookup"><span data-stu-id="80425-121">dataContext</span></span>](view-model-control-value-ivalue-ivalue.md#datacontext)
* [<span data-ttu-id="80425-122">getDesign</span><span class="sxs-lookup"><span data-stu-id="80425-122">getDesign</span></span>](view-model-control-value-ivalue-ivalue.md#getdesign)
* [<span data-ttu-id="80425-123">getValue</span><span class="sxs-lookup"><span data-stu-id="80425-123">getValue</span></span>](view-model-control-value-ivalue-ivalue.md#getvalue)
* [<span data-ttu-id="80425-124">isEditable</span><span class="sxs-lookup"><span data-stu-id="80425-124">isEditable</span></span>](view-model-control-value-ivalue-ivalue.md#iseditable)
* [<span data-ttu-id="80425-125">メタデータ</span><span class="sxs-lookup"><span data-stu-id="80425-125">metadata</span></span>](view-model-control-value-ivalue-ivalue.md#metadata)
* [<span data-ttu-id="80425-126">親</span><span class="sxs-lookup"><span data-stu-id="80425-126">parent</span></span>](view-model-control-value-ivalue-ivalue.md#parent)
* [<span data-ttu-id="80425-127">ルート</span><span class="sxs-lookup"><span data-stu-id="80425-127">root</span></span>](view-model-control-value-ivalue-ivalue.md#root)
* [<span data-ttu-id="80425-128">setValue</span><span class="sxs-lookup"><span data-stu-id="80425-128">setValue</span></span>](view-model-control-value-ivalue-ivalue.md#setvalue)

### <a name="events"></a><span data-ttu-id="80425-129">イベント</span><span class="sxs-lookup"><span data-stu-id="80425-129">Events</span></span>

* [<span data-ttu-id="80425-130">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="80425-130">onDataChanged</span></span>](view-model-control-value-ivalue-ivalue.md#ondatachanged)

## <a name="properties"></a><span data-ttu-id="80425-131">プロパティ</span><span class="sxs-lookup"><span data-stu-id="80425-131">Properties</span></span>

### <a name="container"></a><span data-ttu-id="80425-132">コンテナー</span><span class="sxs-lookup"><span data-stu-id="80425-132">container</span></span>

<span data-ttu-id="80425-133">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="80425-133">container: boolean (optional)</span></span> 

<span data-ttu-id="80425-134">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="80425-134">True if the control is a container.</span></span>

> <span data-ttu-id="80425-135">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-135">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="80425-136">generic</span><span class="sxs-lookup"><span data-stu-id="80425-136">generic</span></span>

<span data-ttu-id="80425-137">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="80425-137">generic: boolean (optional)</span></span> 



> <span data-ttu-id="80425-138">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-138">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="80425-139">getDataSource</span><span class="sxs-lookup"><span data-stu-id="80425-139">getDataSource</span></span>

<span data-ttu-id="80425-140">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="80425-140">getDataSource: function(): any</span></span>



> <span data-ttu-id="80425-141">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-141">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="80425-142">hidden</span><span class="sxs-lookup"><span data-stu-id="80425-142">hidden</span></span>

<span data-ttu-id="80425-143">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="80425-143">hidden: boolean</span></span>

<span data-ttu-id="80425-144">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="80425-144">True if the control is hidden.</span></span>

> <span data-ttu-id="80425-145">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-145">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="80425-146">メソッド</span><span class="sxs-lookup"><span data-stu-id="80425-146">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="80425-147">applyDesign</span><span class="sxs-lookup"><span data-stu-id="80425-147">applyDesign</span></span>


<span data-ttu-id="80425-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="80425-148">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="80425-149">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="80425-149">Applies given design to the design on the control.</span></span>
<span data-ttu-id="80425-150">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="80425-150">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="80425-151">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-151">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="80425-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="80425-152">Parameters</span></span>

| <span data-ttu-id="80425-153">氏名</span><span class="sxs-lookup"><span data-stu-id="80425-153">Name</span></span> | <span data-ttu-id="80425-154">種類</span><span class="sxs-lookup"><span data-stu-id="80425-154">Type</span></span> | <span data-ttu-id="80425-155">説明</span><span class="sxs-lookup"><span data-stu-id="80425-155">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="80425-156">design</span><span class="sxs-lookup"><span data-stu-id="80425-156">design</span></span>|[<span data-ttu-id="80425-157">Design</span><span class="sxs-lookup"><span data-stu-id="80425-157">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="80425-158">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="80425-158">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="80425-159">void を返します</span><span class="sxs-lookup"><span data-stu-id="80425-159">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="80425-160">dataContext</span><span class="sxs-lookup"><span data-stu-id="80425-160">dataContext</span></span>


<span data-ttu-id="80425-161">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="80425-161">dataContext(): any</span></span>



> <span data-ttu-id="80425-162">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-162">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="80425-163">any を返します</span><span class="sxs-lookup"><span data-stu-id="80425-163">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="80425-164">getDesign</span><span class="sxs-lookup"><span data-stu-id="80425-164">getDesign</span></span>


<span data-ttu-id="80425-165">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="80425-165">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="80425-166">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="80425-166">Returns the design object of this control.</span></span>

> <span data-ttu-id="80425-167">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-167">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-designview-model-ipage-idesignmd"></a><span data-ttu-id="80425-168">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="80425-168">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="getvalue"></a><span data-ttu-id="80425-169">getValue</span><span class="sxs-lookup"><span data-stu-id="80425-169">getValue</span></span>


<span data-ttu-id="80425-170">getValue(): string</span><span class="sxs-lookup"><span data-stu-id="80425-170">getValue(): string</span></span>

<span data-ttu-id="80425-171">コントロールの値を返します。</span><span class="sxs-lookup"><span data-stu-id="80425-171">Returns the value of the control.</span></span>

#### <a name="returns-string"></a><span data-ttu-id="80425-172">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="80425-172">Returns string</span></span>



### <a name="iseditable"></a><span data-ttu-id="80425-173">isEditable</span><span class="sxs-lookup"><span data-stu-id="80425-173">isEditable</span></span>


<span data-ttu-id="80425-174">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="80425-174">isEditable(): boolean</span></span>

<span data-ttu-id="80425-175">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="80425-175">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="80425-176">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="80425-176">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="80425-177">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="80425-177">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="80425-178">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="80425-178">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="80425-179">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="80425-179">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="80425-180">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-180">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="80425-181">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="80425-181">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="80425-182">metadata</span><span class="sxs-lookup"><span data-stu-id="80425-182">metadata</span></span>


<span data-ttu-id="80425-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="80425-183">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>

<span data-ttu-id="80425-184">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="80425-184">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="80425-185">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="80425-185">Overrides [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)</span></span>

#### <a name="returns-valuemetadataview-model-control-value-ivalue-ivaluemetadatamd"></a><span data-ttu-id="80425-186">[ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="80425-186">Returns [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="80425-187">parent</span><span class="sxs-lookup"><span data-stu-id="80425-187">parent</span></span>


<span data-ttu-id="80425-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="80425-188">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="80425-189">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="80425-189">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="80425-190">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-190">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a><span data-ttu-id="80425-191">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="80425-191">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="80425-192">root</span><span class="sxs-lookup"><span data-stu-id="80425-192">root</span></span>


<span data-ttu-id="80425-193">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="80425-193">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="80425-194">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="80425-194">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="80425-195">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-195">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-pageview-model-ipage-ipagemd"></a><span data-ttu-id="80425-196">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="80425-196">Returns [Page](view-model-ipage-ipage.md)</span></span>



### <a name="setvalue"></a><span data-ttu-id="80425-197">setValue</span><span class="sxs-lookup"><span data-stu-id="80425-197">setValue</span></span>


<span data-ttu-id="80425-198">setValue(value: string): void</span><span class="sxs-lookup"><span data-stu-id="80425-198">setValue(value: string): void</span></span>

<span data-ttu-id="80425-199">コントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="80425-199">Sets the value of the control.</span></span>


#### <a name="parameters"></a><span data-ttu-id="80425-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="80425-200">Parameters</span></span>

| <span data-ttu-id="80425-201">氏名</span><span class="sxs-lookup"><span data-stu-id="80425-201">Name</span></span> | <span data-ttu-id="80425-202">種類</span><span class="sxs-lookup"><span data-stu-id="80425-202">Type</span></span> | <span data-ttu-id="80425-203">説明</span><span class="sxs-lookup"><span data-stu-id="80425-203">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="80425-204">値</span><span class="sxs-lookup"><span data-stu-id="80425-204">value</span></span>|<span data-ttu-id="80425-205">string</span><span class="sxs-lookup"><span data-stu-id="80425-205">string</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="80425-206">void を返します</span><span class="sxs-lookup"><span data-stu-id="80425-206">Returns void</span></span>

## <a name="events"></a><span data-ttu-id="80425-207">イベント</span><span class="sxs-lookup"><span data-stu-id="80425-207">Events</span></span>

### <a name="ondatachanged"></a><span data-ttu-id="80425-208">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="80425-208">onDataChanged</span></span>

<span data-ttu-id="80425-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span><span class="sxs-lookup"><span data-stu-id="80425-209">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span></span>

<span data-ttu-id="80425-210">入力コントロールのデータが変更されたときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="80425-210">An event that is triggered when the input control's data changes.</span></span>

> <span data-ttu-id="80425-211">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承</span><span class="sxs-lookup"><span data-stu-id="80425-211">Inherited from [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)</span></span>


