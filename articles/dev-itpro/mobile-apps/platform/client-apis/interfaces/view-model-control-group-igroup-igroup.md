---
title: グループ タイプ
description: グループ コンテナーのコントロール タイプ。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5b1ef0ed797e3546701a81b8013a76df71796d24
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369299"
---
# <a name="group-type"></a><span data-ttu-id="d1bee-103">グループ タイプ</span><span class="sxs-lookup"><span data-stu-id="d1bee-103">Group type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="d1bee-104">グループ コンテナーのコントロール タイプ。</span><span class="sxs-lookup"><span data-stu-id="d1bee-104">Group container control type.</span></span>
<span data-ttu-id="d1bee-105">グループ コントロールは、任意の数のコントロールを子として持つコンテナー コントロールです。</span><span class="sxs-lookup"><span data-stu-id="d1bee-105">A group control is a container control that has any number of controls as children.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="d1bee-106">階層</span><span class="sxs-lookup"><span data-stu-id="d1bee-106">Hierarchy</span></span>

[<span data-ttu-id="d1bee-107">ContainerControl</span><span class="sxs-lookup"><span data-stu-id="d1bee-107">ContainerControl</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md) <br><span data-ttu-id="d1bee-108">&nbsp;&nbsp;&nbsp;└─ グループ</span><span class="sxs-lookup"><span data-stu-id="d1bee-108">&nbsp;&nbsp;&nbsp;└─ Group</span></span> <br>

## <a name="index"></a><span data-ttu-id="d1bee-109">指数</span><span class="sxs-lookup"><span data-stu-id="d1bee-109">Index</span></span>

### <a name="properties"></a><span data-ttu-id="d1bee-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1bee-110">Properties</span></span>

* [<span data-ttu-id="d1bee-111">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d1bee-111">container</span></span>](view-model-control-group-igroup-igroup.md#container)
* [<span data-ttu-id="d1bee-112">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="d1bee-112">generic</span></span>](view-model-control-group-igroup-igroup.md#generic)
* [<span data-ttu-id="d1bee-113">getDataSource</span><span class="sxs-lookup"><span data-stu-id="d1bee-113">getDataSource</span></span>](view-model-control-group-igroup-igroup.md#getdatasource)
* [<span data-ttu-id="d1bee-114">非表示</span><span class="sxs-lookup"><span data-stu-id="d1bee-114">hidden</span></span>](view-model-control-group-igroup-igroup.md#hidden)

### <a name="methods"></a><span data-ttu-id="d1bee-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="d1bee-115">Methods</span></span>

* [<span data-ttu-id="d1bee-116">applyDesign</span><span class="sxs-lookup"><span data-stu-id="d1bee-116">applyDesign</span></span>](view-model-control-group-igroup-igroup.md#applydesign)
* [<span data-ttu-id="d1bee-117">dataContext</span><span class="sxs-lookup"><span data-stu-id="d1bee-117">dataContext</span></span>](view-model-control-group-igroup-igroup.md#datacontext)
* [<span data-ttu-id="d1bee-118">getChildren</span><span class="sxs-lookup"><span data-stu-id="d1bee-118">getChildren</span></span>](view-model-control-group-igroup-igroup.md#getchildren)
* [<span data-ttu-id="d1bee-119">getControl</span><span class="sxs-lookup"><span data-stu-id="d1bee-119">getControl</span></span>](view-model-control-group-igroup-igroup.md#getcontrol)
* [<span data-ttu-id="d1bee-120">getControlById</span><span class="sxs-lookup"><span data-stu-id="d1bee-120">getControlById</span></span>](view-model-control-group-igroup-igroup.md#getcontrolbyid)
* [<span data-ttu-id="d1bee-121">getDesign</span><span class="sxs-lookup"><span data-stu-id="d1bee-121">getDesign</span></span>](view-model-control-group-igroup-igroup.md#getdesign)
* [<span data-ttu-id="d1bee-122">isEditable</span><span class="sxs-lookup"><span data-stu-id="d1bee-122">isEditable</span></span>](view-model-control-group-igroup-igroup.md#iseditable)
* [<span data-ttu-id="d1bee-123">メタデータ</span><span class="sxs-lookup"><span data-stu-id="d1bee-123">metadata</span></span>](view-model-control-group-igroup-igroup.md#metadata)
* [<span data-ttu-id="d1bee-124">親</span><span class="sxs-lookup"><span data-stu-id="d1bee-124">parent</span></span>](view-model-control-group-igroup-igroup.md#parent)
* [<span data-ttu-id="d1bee-125">ルート</span><span class="sxs-lookup"><span data-stu-id="d1bee-125">root</span></span>](view-model-control-group-igroup-igroup.md#root)

## <a name="properties"></a><span data-ttu-id="d1bee-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d1bee-126">Properties</span></span>

### <a name="container"></a><span data-ttu-id="d1bee-127">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d1bee-127">container</span></span>

<span data-ttu-id="d1bee-128">container: ブール値</span><span class="sxs-lookup"><span data-stu-id="d1bee-128">container: boolean</span></span>

<span data-ttu-id="d1bee-129">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="d1bee-129">True if the control is a container.</span></span>

> <span data-ttu-id="d1bee-130">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-130">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container)</span></span>
> 
> <span data-ttu-id="d1bee-131">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="d1bee-131">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="d1bee-132">generic</span><span class="sxs-lookup"><span data-stu-id="d1bee-132">generic</span></span>

<span data-ttu-id="d1bee-133">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="d1bee-133">generic: boolean (optional)</span></span> 



> <span data-ttu-id="d1bee-134">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-134">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="d1bee-135">getDataSource</span><span class="sxs-lookup"><span data-stu-id="d1bee-135">getDataSource</span></span>

<span data-ttu-id="d1bee-136">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="d1bee-136">getDataSource: function(): any</span></span>



> <span data-ttu-id="d1bee-137">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-137">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="d1bee-138">hidden</span><span class="sxs-lookup"><span data-stu-id="d1bee-138">hidden</span></span>

<span data-ttu-id="d1bee-139">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="d1bee-139">hidden: boolean</span></span>

<span data-ttu-id="d1bee-140">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="d1bee-140">True if the control is hidden.</span></span>

> <span data-ttu-id="d1bee-141">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-141">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


## <a name="methods"></a><span data-ttu-id="d1bee-142">メソッド</span><span class="sxs-lookup"><span data-stu-id="d1bee-142">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="d1bee-143">applyDesign</span><span class="sxs-lookup"><span data-stu-id="d1bee-143">applyDesign</span></span>


<span data-ttu-id="d1bee-144">applyDesign(IDesign: [GroupDesign](view-model-control-group-igroup-igroupdesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="d1bee-144">applyDesign(IDesign: [GroupDesign](view-model-control-group-igroup-igroupdesign.md)): void</span></span>

<span data-ttu-id="d1bee-145">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-145">Applies given design to the design on the control.</span></span>
<span data-ttu-id="d1bee-146">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="d1bee-146">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="d1bee-147">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="d1bee-147">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="d1bee-148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1bee-148">Parameters</span></span>

| <span data-ttu-id="d1bee-149">氏名</span><span class="sxs-lookup"><span data-stu-id="d1bee-149">Name</span></span> | <span data-ttu-id="d1bee-150">種類</span><span class="sxs-lookup"><span data-stu-id="d1bee-150">Type</span></span> | <span data-ttu-id="d1bee-151">説明</span><span class="sxs-lookup"><span data-stu-id="d1bee-151">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="d1bee-152">IDesign</span><span class="sxs-lookup"><span data-stu-id="d1bee-152">IDesign</span></span>|[<span data-ttu-id="d1bee-153">GroupDesign</span><span class="sxs-lookup"><span data-stu-id="d1bee-153">GroupDesign</span></span>](view-model-control-group-igroup-igroupdesign.md)|<span data-ttu-id="d1bee-154">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d1bee-154">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="d1bee-155">void を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-155">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="d1bee-156">dataContext</span><span class="sxs-lookup"><span data-stu-id="d1bee-156">dataContext</span></span>


<span data-ttu-id="d1bee-157">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="d1bee-157">dataContext(): any</span></span>



> <span data-ttu-id="d1bee-158">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-158">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="d1bee-159">any を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-159">Returns any</span></span>

### <a name="getchildren"></a><span data-ttu-id="d1bee-160">getChildren</span><span class="sxs-lookup"><span data-stu-id="d1bee-160">getChildren</span></span>


<span data-ttu-id="d1bee-161">getChildren(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) [ ]</span><span class="sxs-lookup"><span data-stu-id="d1bee-161">getChildren(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) [ ]</span></span>

<span data-ttu-id="d1bee-162">このグループ コントロールに関連付けられている子のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-162">Returns the list of children associated with this group control.</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd--"></a><span data-ttu-id="d1bee-163">[Control](view-model-control-basecontrol-icontrol-icontrol.md) [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-163">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) [ ]</span></span>



### <a name="getcontrol"></a><span data-ttu-id="d1bee-164">getControl</span><span class="sxs-lookup"><span data-stu-id="d1bee-164">getControl</span></span>


<span data-ttu-id="d1bee-165">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="d1bee-165">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="d1bee-166">コントロールの名前の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-166">Given the name of a control, returns the control instance.</span></span>

> <span data-ttu-id="d1bee-167">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-167">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol)</span></span>


#### <a name="parameters"></a><span data-ttu-id="d1bee-168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1bee-168">Parameters</span></span>

| <span data-ttu-id="d1bee-169">氏名</span><span class="sxs-lookup"><span data-stu-id="d1bee-169">Name</span></span> | <span data-ttu-id="d1bee-170">種類</span><span class="sxs-lookup"><span data-stu-id="d1bee-170">Type</span></span> | <span data-ttu-id="d1bee-171">説明</span><span class="sxs-lookup"><span data-stu-id="d1bee-171">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="d1bee-172">controlName</span><span class="sxs-lookup"><span data-stu-id="d1bee-172">controlName</span></span>|<span data-ttu-id="d1bee-173">string</span><span class="sxs-lookup"><span data-stu-id="d1bee-173">string</span></span>|<span data-ttu-id="d1bee-174">コントロール名</span><span class="sxs-lookup"><span data-stu-id="d1bee-174">control name</span></span>|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="d1bee-175">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-175">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getcontrolbyid"></a><span data-ttu-id="d1bee-176">getControlById</span><span class="sxs-lookup"><span data-stu-id="d1bee-176">getControlById</span></span>


<span data-ttu-id="d1bee-177">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="d1bee-177">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="d1bee-178">コントロールの ID の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-178">Given the ID of a control, returns the control instance.</span></span>

> <span data-ttu-id="d1bee-179">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-179">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid)</span></span>


#### <a name="parameters"></a><span data-ttu-id="d1bee-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1bee-180">Parameters</span></span>

| <span data-ttu-id="d1bee-181">氏名</span><span class="sxs-lookup"><span data-stu-id="d1bee-181">Name</span></span> | <span data-ttu-id="d1bee-182">種類</span><span class="sxs-lookup"><span data-stu-id="d1bee-182">Type</span></span> | <span data-ttu-id="d1bee-183">説明</span><span class="sxs-lookup"><span data-stu-id="d1bee-183">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="d1bee-184">id</span><span class="sxs-lookup"><span data-stu-id="d1bee-184">id</span></span>|<span data-ttu-id="d1bee-185">string</span><span class="sxs-lookup"><span data-stu-id="d1bee-185">string</span></span>|<span data-ttu-id="d1bee-186">コントロール ID</span><span class="sxs-lookup"><span data-stu-id="d1bee-186">control ID</span></span>|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="d1bee-187">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-187">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getdesign"></a><span data-ttu-id="d1bee-188">getDesign</span><span class="sxs-lookup"><span data-stu-id="d1bee-188">getDesign</span></span>


<span data-ttu-id="d1bee-189">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="d1bee-189">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="d1bee-190">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-190">Returns the design object of this control.</span></span>

> <span data-ttu-id="d1bee-191">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-191">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-designview-model-ipage-idesignmd"></a><span data-ttu-id="d1bee-192">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-192">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="iseditable"></a><span data-ttu-id="d1bee-193">isEditable</span><span class="sxs-lookup"><span data-stu-id="d1bee-193">isEditable</span></span>


<span data-ttu-id="d1bee-194">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="d1bee-194">isEditable(): boolean</span></span>

<span data-ttu-id="d1bee-195">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d1bee-195">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="d1bee-196">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-196">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="d1bee-197">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-197">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="d1bee-198">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-198">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="d1bee-199">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-199">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="d1bee-200">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-200">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="d1bee-201">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-201">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="d1bee-202">metadata</span><span class="sxs-lookup"><span data-stu-id="d1bee-202">metadata</span></span>


<span data-ttu-id="d1bee-203">metadata(): [GroupMetadata](view-model-control-group-igroup-igroupmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="d1bee-203">metadata(): [GroupMetadata](view-model-control-group-igroup-igroupmetadata.md)</span></span>

<span data-ttu-id="d1bee-204">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-204">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="d1bee-205">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="d1bee-205">Overrides [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata)</span></span>

#### <a name="returns-groupmetadataview-model-control-group-igroup-igroupmetadatamd"></a><span data-ttu-id="d1bee-206">[GroupMetadata](view-model-control-group-igroup-igroupmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-206">Returns [GroupMetadata](view-model-control-group-igroup-igroupmetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="d1bee-207">parent</span><span class="sxs-lookup"><span data-stu-id="d1bee-207">parent</span></span>


<span data-ttu-id="d1bee-208">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="d1bee-208">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="d1bee-209">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-209">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="d1bee-210">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-210">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a><span data-ttu-id="d1bee-211">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-211">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="d1bee-212">root</span><span class="sxs-lookup"><span data-stu-id="d1bee-212">root</span></span>


<span data-ttu-id="d1bee-213">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="d1bee-213">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="d1bee-214">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="d1bee-214">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="d1bee-215">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="d1bee-215">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-pageview-model-ipage-ipagemd"></a><span data-ttu-id="d1bee-216">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="d1bee-216">Returns [Page](view-model-ipage-ipage.md)</span></span>



