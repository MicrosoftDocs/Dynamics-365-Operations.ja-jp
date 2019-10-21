---
title: ContainerControl タイプ
description: すべてのコンテナー コントロールのメソッドと属性を持つコンテナー コントロール インターフェイス。 コンテナー コントロールは、コントロールの任意の数を含めることができます。
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
ms.openlocfilehash: 2ac2503edd033844fb454f3b26e4b0a97798846a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183140"
---
# <a name="containercontrol-type"></a><span data-ttu-id="85d70-104">ContainerControl タイプ</span><span class="sxs-lookup"><span data-stu-id="85d70-104">ContainerControl type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="85d70-105">すべてのコンテナー コントロールのメソッドと属性を持つコンテナー コントロール インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="85d70-105">Container control interface with methods and attributes for all container controls.</span></span>
<span data-ttu-id="85d70-106">コンテナー コントロールは、コントロールの任意の数を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="85d70-106">A container control can contain any number of controls.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="85d70-107">階層</span><span class="sxs-lookup"><span data-stu-id="85d70-107">Hierarchy</span></span>

[<span data-ttu-id="85d70-108">コントロール</span><span class="sxs-lookup"><span data-stu-id="85d70-108">Control</span></span>](view-model-control-basecontrol-icontrol-icontrol.md) <br><span data-ttu-id="85d70-109">&nbsp;&nbsp;&nbsp;└─ ContainerControl</span><span class="sxs-lookup"><span data-stu-id="85d70-109">&nbsp;&nbsp;&nbsp;└─ ContainerControl</span></span> <br><span data-ttu-id="85d70-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [グループ](view-model-control-group-igroup-igroup.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Group](view-model-control-group-igroup-igroup.md)</span></span> <br><span data-ttu-id="85d70-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [リスト](view-model-control-list-ilist-ilist.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [List](view-model-control-list-ilist-ilist.md)</span></span> <br><span data-ttu-id="85d70-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [パート](view-model-control-part-ipart-ipart.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Part](view-model-control-part-ipart-ipart.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="85d70-113">指数</span><span class="sxs-lookup"><span data-stu-id="85d70-113">Index</span></span>

### <a name="properties"></a><span data-ttu-id="85d70-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="85d70-114">Properties</span></span>

* [<span data-ttu-id="85d70-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="85d70-115">container</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#container)
* [<span data-ttu-id="85d70-116">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="85d70-116">generic</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#generic)
* [<span data-ttu-id="85d70-117">getDataSource</span><span class="sxs-lookup"><span data-stu-id="85d70-117">getDataSource</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#getdatasource)
* [<span data-ttu-id="85d70-118">非表示</span><span class="sxs-lookup"><span data-stu-id="85d70-118">hidden</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#hidden)

### <a name="methods"></a><span data-ttu-id="85d70-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="85d70-119">Methods</span></span>

* [<span data-ttu-id="85d70-120">applyDesign</span><span class="sxs-lookup"><span data-stu-id="85d70-120">applyDesign</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#applydesign)
* [<span data-ttu-id="85d70-121">dataContext</span><span class="sxs-lookup"><span data-stu-id="85d70-121">dataContext</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#datacontext)
* [<span data-ttu-id="85d70-122">getControl</span><span class="sxs-lookup"><span data-stu-id="85d70-122">getControl</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol)
* [<span data-ttu-id="85d70-123">getControlById</span><span class="sxs-lookup"><span data-stu-id="85d70-123">getControlById</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid)
* [<span data-ttu-id="85d70-124">getDesign</span><span class="sxs-lookup"><span data-stu-id="85d70-124">getDesign</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#getdesign)
* [<span data-ttu-id="85d70-125">isEditable</span><span class="sxs-lookup"><span data-stu-id="85d70-125">isEditable</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#iseditable)
* [<span data-ttu-id="85d70-126">メタデータ</span><span class="sxs-lookup"><span data-stu-id="85d70-126">metadata</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata)
* [<span data-ttu-id="85d70-127">親</span><span class="sxs-lookup"><span data-stu-id="85d70-127">parent</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#parent)
* [<span data-ttu-id="85d70-128">ルート</span><span class="sxs-lookup"><span data-stu-id="85d70-128">root</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md#root)

## <a name="properties"></a><span data-ttu-id="85d70-129">プロパティ</span><span class="sxs-lookup"><span data-stu-id="85d70-129">Properties</span></span>

### <a name="container"></a><span data-ttu-id="85d70-130">コンテナー</span><span class="sxs-lookup"><span data-stu-id="85d70-130">container</span></span>

<span data-ttu-id="85d70-131">container: ブール値</span><span class="sxs-lookup"><span data-stu-id="85d70-131">container: boolean</span></span>

<span data-ttu-id="85d70-132">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="85d70-132">True if the control is a container.</span></span>

> <span data-ttu-id="85d70-133">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="85d70-133">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="85d70-134">generic</span><span class="sxs-lookup"><span data-stu-id="85d70-134">generic</span></span>

<span data-ttu-id="85d70-135">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="85d70-135">generic: boolean (optional)</span></span> 



> <span data-ttu-id="85d70-136">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-136">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="85d70-137">getDataSource</span><span class="sxs-lookup"><span data-stu-id="85d70-137">getDataSource</span></span>

<span data-ttu-id="85d70-138">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="85d70-138">getDataSource: function(): any</span></span>



> <span data-ttu-id="85d70-139">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-139">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="85d70-140">hidden</span><span class="sxs-lookup"><span data-stu-id="85d70-140">hidden</span></span>

<span data-ttu-id="85d70-141">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="85d70-141">hidden: boolean</span></span>

<span data-ttu-id="85d70-142">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="85d70-142">True if the control is hidden.</span></span>

> <span data-ttu-id="85d70-143">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-143">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="85d70-144">メソッド</span><span class="sxs-lookup"><span data-stu-id="85d70-144">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="85d70-145">applyDesign</span><span class="sxs-lookup"><span data-stu-id="85d70-145">applyDesign</span></span>


<span data-ttu-id="85d70-146">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="85d70-146">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="85d70-147">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="85d70-147">Applies given design to the design on the control.</span></span>
<span data-ttu-id="85d70-148">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="85d70-148">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="85d70-149">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-149">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="85d70-150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85d70-150">Parameters</span></span>

| <span data-ttu-id="85d70-151">氏名</span><span class="sxs-lookup"><span data-stu-id="85d70-151">Name</span></span> | <span data-ttu-id="85d70-152">種類</span><span class="sxs-lookup"><span data-stu-id="85d70-152">Type</span></span> | <span data-ttu-id="85d70-153">説明</span><span class="sxs-lookup"><span data-stu-id="85d70-153">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="85d70-154">design</span><span class="sxs-lookup"><span data-stu-id="85d70-154">design</span></span>|[<span data-ttu-id="85d70-155">Design</span><span class="sxs-lookup"><span data-stu-id="85d70-155">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="85d70-156">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="85d70-156">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="85d70-157">void を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-157">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="85d70-158">dataContext</span><span class="sxs-lookup"><span data-stu-id="85d70-158">dataContext</span></span>


<span data-ttu-id="85d70-159">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="85d70-159">dataContext(): any</span></span>



> <span data-ttu-id="85d70-160">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-160">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="85d70-161">any を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-161">Returns any</span></span>

### <a name="getcontrol"></a><span data-ttu-id="85d70-162">getControl</span><span class="sxs-lookup"><span data-stu-id="85d70-162">getControl</span></span>


<span data-ttu-id="85d70-163">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-163">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="85d70-164">コントロールの名前の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-164">Given the name of a control, returns the control instance.</span></span>


#### <a name="parameters"></a><span data-ttu-id="85d70-165">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85d70-165">Parameters</span></span>

| <span data-ttu-id="85d70-166">氏名</span><span class="sxs-lookup"><span data-stu-id="85d70-166">Name</span></span> | <span data-ttu-id="85d70-167">種類</span><span class="sxs-lookup"><span data-stu-id="85d70-167">Type</span></span> | <span data-ttu-id="85d70-168">説明</span><span class="sxs-lookup"><span data-stu-id="85d70-168">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="85d70-169">controlName</span><span class="sxs-lookup"><span data-stu-id="85d70-169">controlName</span></span>|<span data-ttu-id="85d70-170">string</span><span class="sxs-lookup"><span data-stu-id="85d70-170">string</span></span>|<span data-ttu-id="85d70-171">コントロール名</span><span class="sxs-lookup"><span data-stu-id="85d70-171">control name</span></span>|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="85d70-172">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-172">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getcontrolbyid"></a><span data-ttu-id="85d70-173">getControlById</span><span class="sxs-lookup"><span data-stu-id="85d70-173">getControlById</span></span>


<span data-ttu-id="85d70-174">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-174">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="85d70-175">コントロールの ID の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-175">Given the ID of a control, returns the control instance.</span></span>


#### <a name="parameters"></a><span data-ttu-id="85d70-176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85d70-176">Parameters</span></span>

| <span data-ttu-id="85d70-177">氏名</span><span class="sxs-lookup"><span data-stu-id="85d70-177">Name</span></span> | <span data-ttu-id="85d70-178">種類</span><span class="sxs-lookup"><span data-stu-id="85d70-178">Type</span></span> | <span data-ttu-id="85d70-179">説明</span><span class="sxs-lookup"><span data-stu-id="85d70-179">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="85d70-180">id</span><span class="sxs-lookup"><span data-stu-id="85d70-180">id</span></span>|<span data-ttu-id="85d70-181">string</span><span class="sxs-lookup"><span data-stu-id="85d70-181">string</span></span>|<span data-ttu-id="85d70-182">コントロール ID</span><span class="sxs-lookup"><span data-stu-id="85d70-182">control ID</span></span>|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="85d70-183">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-183">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getdesign"></a><span data-ttu-id="85d70-184">getDesign</span><span class="sxs-lookup"><span data-stu-id="85d70-184">getDesign</span></span>


<span data-ttu-id="85d70-185">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-185">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="85d70-186">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-186">Returns the design object of this control.</span></span>

> <span data-ttu-id="85d70-187">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-187">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-designview-model-ipage-idesignmd"></a><span data-ttu-id="85d70-188">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-188">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="iseditable"></a><span data-ttu-id="85d70-189">isEditable</span><span class="sxs-lookup"><span data-stu-id="85d70-189">isEditable</span></span>


<span data-ttu-id="85d70-190">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="85d70-190">isEditable(): boolean</span></span>

<span data-ttu-id="85d70-191">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="85d70-191">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="85d70-192">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-192">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="85d70-193">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-193">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="85d70-194">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-194">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="85d70-195">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-195">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="85d70-196">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-196">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="85d70-197">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-197">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="85d70-198">metadata</span><span class="sxs-lookup"><span data-stu-id="85d70-198">metadata</span></span>


<span data-ttu-id="85d70-199">metadata(): [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-199">metadata(): [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md)</span></span>

<span data-ttu-id="85d70-200">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-200">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="85d70-201">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="85d70-201">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata)</span></span>

#### <a name="returns-containercontrolmetadataview-model-control-container-icontainercontrol-icontainercontrolmetadatamd"></a><span data-ttu-id="85d70-202">[ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-202">Returns [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="85d70-203">parent</span><span class="sxs-lookup"><span data-stu-id="85d70-203">parent</span></span>


<span data-ttu-id="85d70-204">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-204">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="85d70-205">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-205">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="85d70-206">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-206">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a><span data-ttu-id="85d70-207">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-207">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="85d70-208">root</span><span class="sxs-lookup"><span data-stu-id="85d70-208">root</span></span>


<span data-ttu-id="85d70-209">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="85d70-209">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="85d70-210">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="85d70-210">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="85d70-211">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="85d70-211">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-pageview-model-ipage-ipagemd"></a><span data-ttu-id="85d70-212">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="85d70-212">Returns [Page](view-model-ipage-ipage.md)</span></span>



