---
title: "GenericValue タイプ"
description: "コントロール タイプの一般的な値。"
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
ms.openlocfilehash: 9b1ebea19e0fbb21b32c047579b2d56866a1358e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="genericvalue-type"></a><span data-ttu-id="2f130-103">GenericValue タイプ</span><span class="sxs-lookup"><span data-stu-id="2f130-103">GenericValue type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="2f130-104">コントロール タイプの一般的な値。</span><span class="sxs-lookup"><span data-stu-id="2f130-104">Generic value control type.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="2f130-105">階層</span><span class="sxs-lookup"><span data-stu-id="2f130-105">Hierarchy</span></span>

[<span data-ttu-id="2f130-106">値</span><span class="sxs-lookup"><span data-stu-id="2f130-106">Value</span></span>](view-model-control-value-ivalue-ivalue.md) <br><span data-ttu-id="2f130-107">&nbsp;&nbsp;&nbsp;└─ GenericValue</span><span class="sxs-lookup"><span data-stu-id="2f130-107">&nbsp;&nbsp;&nbsp;└─ GenericValue</span></span> <br>

## <a name="index"></a><span data-ttu-id="2f130-108">指数</span><span class="sxs-lookup"><span data-stu-id="2f130-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="2f130-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2f130-109">Properties</span></span>

* [<span data-ttu-id="2f130-110">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2f130-110">container</span></span>](view-model-control-value-ivalue-igenericvalue.md#container)
* [<span data-ttu-id="2f130-111">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="2f130-111">generic</span></span>](view-model-control-value-ivalue-igenericvalue.md#generic)
* [<span data-ttu-id="2f130-112">getDataSource</span><span class="sxs-lookup"><span data-stu-id="2f130-112">getDataSource</span></span>](view-model-control-value-ivalue-igenericvalue.md#getdatasource)
* [<span data-ttu-id="2f130-113">非表示</span><span class="sxs-lookup"><span data-stu-id="2f130-113">hidden</span></span>](view-model-control-value-ivalue-igenericvalue.md#hidden)

### <a name="methods"></a><span data-ttu-id="2f130-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="2f130-114">Methods</span></span>

* [<span data-ttu-id="2f130-115">applyDesign</span><span class="sxs-lookup"><span data-stu-id="2f130-115">applyDesign</span></span>](view-model-control-value-ivalue-igenericvalue.md#applydesign)
* [<span data-ttu-id="2f130-116">dataContext</span><span class="sxs-lookup"><span data-stu-id="2f130-116">dataContext</span></span>](view-model-control-value-ivalue-igenericvalue.md#datacontext)
* [<span data-ttu-id="2f130-117">getDesign</span><span class="sxs-lookup"><span data-stu-id="2f130-117">getDesign</span></span>](view-model-control-value-ivalue-igenericvalue.md#getdesign)
* [<span data-ttu-id="2f130-118">getValue</span><span class="sxs-lookup"><span data-stu-id="2f130-118">getValue</span></span>](view-model-control-value-ivalue-igenericvalue.md#getvalue)
* [<span data-ttu-id="2f130-119">isEditable</span><span class="sxs-lookup"><span data-stu-id="2f130-119">isEditable</span></span>](view-model-control-value-ivalue-igenericvalue.md#iseditable)
* [<span data-ttu-id="2f130-120">メタデータ</span><span class="sxs-lookup"><span data-stu-id="2f130-120">metadata</span></span>](view-model-control-value-ivalue-igenericvalue.md#metadata)
* [<span data-ttu-id="2f130-121">親</span><span class="sxs-lookup"><span data-stu-id="2f130-121">parent</span></span>](view-model-control-value-ivalue-igenericvalue.md#parent)
* [<span data-ttu-id="2f130-122">ルート</span><span class="sxs-lookup"><span data-stu-id="2f130-122">root</span></span>](view-model-control-value-ivalue-igenericvalue.md#root)
* [<span data-ttu-id="2f130-123">setValue</span><span class="sxs-lookup"><span data-stu-id="2f130-123">setValue</span></span>](view-model-control-value-ivalue-igenericvalue.md#setvalue)

### <a name="events"></a><span data-ttu-id="2f130-124">イベント</span><span class="sxs-lookup"><span data-stu-id="2f130-124">Events</span></span>

* [<span data-ttu-id="2f130-125">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="2f130-125">onDataChanged</span></span>](view-model-control-value-ivalue-igenericvalue.md#ondatachanged)

## <a name="properties"></a><span data-ttu-id="2f130-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2f130-126">Properties</span></span>

### <a name="container"></a><span data-ttu-id="2f130-127">コンテナー</span><span class="sxs-lookup"><span data-stu-id="2f130-127">container</span></span>

<span data-ttu-id="2f130-128">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="2f130-128">container: boolean (optional)</span></span> 

<span data-ttu-id="2f130-129">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="2f130-129">True if the control is a container.</span></span>

> <span data-ttu-id="2f130-130">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-130">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="2f130-131">generic</span><span class="sxs-lookup"><span data-stu-id="2f130-131">generic</span></span>

<span data-ttu-id="2f130-132">generic: boolean</span><span class="sxs-lookup"><span data-stu-id="2f130-132">generic: boolean</span></span>

<span data-ttu-id="2f130-133">コントロールがジェネリックの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="2f130-133">True if the control is a generic.</span></span>

> <span data-ttu-id="2f130-134">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="2f130-134">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="2f130-135">getDataSource</span><span class="sxs-lookup"><span data-stu-id="2f130-135">getDataSource</span></span>

<span data-ttu-id="2f130-136">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="2f130-136">getDataSource: function(): any</span></span>



> <span data-ttu-id="2f130-137">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-137">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="2f130-138">hidden</span><span class="sxs-lookup"><span data-stu-id="2f130-138">hidden</span></span>

<span data-ttu-id="2f130-139">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="2f130-139">hidden: boolean</span></span>

<span data-ttu-id="2f130-140">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="2f130-140">True if the control is hidden.</span></span>

> <span data-ttu-id="2f130-141">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-141">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="2f130-142">メソッド</span><span class="sxs-lookup"><span data-stu-id="2f130-142">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="2f130-143">applyDesign</span><span class="sxs-lookup"><span data-stu-id="2f130-143">applyDesign</span></span>


<span data-ttu-id="2f130-144">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="2f130-144">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="2f130-145">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="2f130-145">Applies given design to the design on the control.</span></span>
<span data-ttu-id="2f130-146">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="2f130-146">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="2f130-147">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-147">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="2f130-148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2f130-148">Parameters</span></span>

| <span data-ttu-id="2f130-149">氏名</span><span class="sxs-lookup"><span data-stu-id="2f130-149">Name</span></span> | <span data-ttu-id="2f130-150">種類</span><span class="sxs-lookup"><span data-stu-id="2f130-150">Type</span></span> | <span data-ttu-id="2f130-151">説明</span><span class="sxs-lookup"><span data-stu-id="2f130-151">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="2f130-152">design</span><span class="sxs-lookup"><span data-stu-id="2f130-152">design</span></span>|[<span data-ttu-id="2f130-153">Design</span><span class="sxs-lookup"><span data-stu-id="2f130-153">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="2f130-154">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="2f130-154">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="2f130-155">void を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-155">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="2f130-156">dataContext</span><span class="sxs-lookup"><span data-stu-id="2f130-156">dataContext</span></span>


<span data-ttu-id="2f130-157">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="2f130-157">dataContext(): any</span></span>



> <span data-ttu-id="2f130-158">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-158">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="2f130-159">any を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-159">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="2f130-160">getDesign</span><span class="sxs-lookup"><span data-stu-id="2f130-160">getDesign</span></span>


<span data-ttu-id="2f130-161">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="2f130-161">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="2f130-162">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-162">Returns the design object of this control.</span></span>

> <span data-ttu-id="2f130-163">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-163">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-designview-model-ipage-idesignmd"></a><span data-ttu-id="2f130-164">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-164">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="getvalue"></a><span data-ttu-id="2f130-165">getValue</span><span class="sxs-lookup"><span data-stu-id="2f130-165">getValue</span></span>


<span data-ttu-id="2f130-166">getValue(): string</span><span class="sxs-lookup"><span data-stu-id="2f130-166">getValue(): string</span></span>

<span data-ttu-id="2f130-167">コントロールの値を返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-167">Returns the value of the control.</span></span>

> <span data-ttu-id="2f130-168">[Value](view-model-control-value-ivalue-ivalue.md).[getValue](view-model-control-value-ivalue-ivalue.md#getvalue) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-168">Inherited from [Value](view-model-control-value-ivalue-ivalue.md).[getValue](view-model-control-value-ivalue-ivalue.md#getvalue)</span></span>

#### <a name="returns-string"></a><span data-ttu-id="2f130-169">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-169">Returns string</span></span>



### <a name="iseditable"></a><span data-ttu-id="2f130-170">isEditable</span><span class="sxs-lookup"><span data-stu-id="2f130-170">isEditable</span></span>


<span data-ttu-id="2f130-171">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="2f130-171">isEditable(): boolean</span></span>

<span data-ttu-id="2f130-172">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2f130-172">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="2f130-173">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-173">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="2f130-174">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-174">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="2f130-175">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-175">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="2f130-176">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-176">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="2f130-177">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-177">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="2f130-178">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-178">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="2f130-179">metadata</span><span class="sxs-lookup"><span data-stu-id="2f130-179">metadata</span></span>


<span data-ttu-id="2f130-180">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="2f130-180">metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>

<span data-ttu-id="2f130-181">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-181">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="2f130-182">[Value](view-model-control-value-ivalue-ivalue.md).[metadata](view-model-control-value-ivalue-ivalue.md#metadata) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-182">Inherited from [Value](view-model-control-value-ivalue-ivalue.md).[metadata](view-model-control-value-ivalue-ivalue.md#metadata)</span></span>
> 
> <span data-ttu-id="2f130-183">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="2f130-183">Overrides [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)</span></span>

#### <a name="returns-valuemetadataview-model-control-value-ivalue-ivaluemetadatamd"></a><span data-ttu-id="2f130-184">[ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-184">Returns [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="2f130-185">parent</span><span class="sxs-lookup"><span data-stu-id="2f130-185">parent</span></span>


<span data-ttu-id="2f130-186">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="2f130-186">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="2f130-187">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-187">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="2f130-188">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-188">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a><span data-ttu-id="2f130-189">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-189">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="2f130-190">root</span><span class="sxs-lookup"><span data-stu-id="2f130-190">root</span></span>


<span data-ttu-id="2f130-191">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="2f130-191">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="2f130-192">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="2f130-192">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="2f130-193">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-193">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-pageview-model-ipage-ipagemd"></a><span data-ttu-id="2f130-194">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-194">Returns [Page](view-model-ipage-ipage.md)</span></span>



### <a name="setvalue"></a><span data-ttu-id="2f130-195">setValue</span><span class="sxs-lookup"><span data-stu-id="2f130-195">setValue</span></span>


<span data-ttu-id="2f130-196">setValue(value: string): void</span><span class="sxs-lookup"><span data-stu-id="2f130-196">setValue(value: string): void</span></span>

<span data-ttu-id="2f130-197">コントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2f130-197">Sets the value of the control.</span></span>

> <span data-ttu-id="2f130-198">[Value](view-model-control-value-ivalue-ivalue.md).[setValue](view-model-control-value-ivalue-ivalue.md#setvalue) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-198">Inherited from [Value](view-model-control-value-ivalue-ivalue.md).[setValue](view-model-control-value-ivalue-ivalue.md#setvalue)</span></span>


#### <a name="parameters"></a><span data-ttu-id="2f130-199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2f130-199">Parameters</span></span>

| <span data-ttu-id="2f130-200">氏名</span><span class="sxs-lookup"><span data-stu-id="2f130-200">Name</span></span> | <span data-ttu-id="2f130-201">種類</span><span class="sxs-lookup"><span data-stu-id="2f130-201">Type</span></span> | <span data-ttu-id="2f130-202">説明</span><span class="sxs-lookup"><span data-stu-id="2f130-202">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="2f130-203">値</span><span class="sxs-lookup"><span data-stu-id="2f130-203">value</span></span>|<span data-ttu-id="2f130-204">string</span><span class="sxs-lookup"><span data-stu-id="2f130-204">string</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="2f130-205">void を返します</span><span class="sxs-lookup"><span data-stu-id="2f130-205">Returns void</span></span>

## <a name="events"></a><span data-ttu-id="2f130-206">イベント</span><span class="sxs-lookup"><span data-stu-id="2f130-206">Events</span></span>

### <a name="ondatachanged"></a><span data-ttu-id="2f130-207">onDataChanged</span><span class="sxs-lookup"><span data-stu-id="2f130-207">onDataChanged</span></span>

<span data-ttu-id="2f130-208">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span><span class="sxs-lookup"><span data-stu-id="2f130-208">onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;</span></span>

<span data-ttu-id="2f130-209">入力コントロールのデータが変更されたときに発生するイベントです。</span><span class="sxs-lookup"><span data-stu-id="2f130-209">An event that is triggered when the input control's data changes.</span></span>

> <span data-ttu-id="2f130-210">[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承</span><span class="sxs-lookup"><span data-stu-id="2f130-210">Inherited from [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)</span></span>



