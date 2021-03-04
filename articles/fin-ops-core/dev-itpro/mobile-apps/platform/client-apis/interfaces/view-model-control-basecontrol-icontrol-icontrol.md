---
title: コントロール タイプ
description: すべてのコントロールの基準メソッドと属性を持つコントロール インターフェイス。 これは、コントロールのランタイムのインスタンスを表します。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 213c9f244421ef37e3382bfa60efb39ee27d6d8a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130787"
---
# <a name="control-type"></a><span data-ttu-id="92162-104">コントロール タイプ</span><span class="sxs-lookup"><span data-stu-id="92162-104">Control type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="92162-105">すべてのコントロールの基準メソッドと属性を持つコントロール インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="92162-105">Control interface with base methods and attributes for all controls.</span></span>
<span data-ttu-id="92162-106">これは、コントロールのランタイムのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="92162-106">This represents the runtime instance of a control.</span></span> <span data-ttu-id="92162-107">プロパティの変更は、UI にすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="92162-107">Modifying the properties are immediately reflected in the UI.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="92162-108">階層</span><span class="sxs-lookup"><span data-stu-id="92162-108">Hierarchy</span></span>

<span data-ttu-id="92162-109">状態</span><span class="sxs-lookup"><span data-stu-id="92162-109">Control</span></span> <br><span data-ttu-id="92162-110">&nbsp;&nbsp;&nbsp;└─ [PageLink](view-model-control-pagelink-ipagelink-ipagelink.md)</span><span class="sxs-lookup"><span data-stu-id="92162-110">&nbsp;&nbsp;&nbsp;└─ [PageLink](view-model-control-pagelink-ipagelink-ipagelink.md)</span></span> <br><span data-ttu-id="92162-111">&nbsp;&nbsp;&nbsp;└─ [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md)</span><span class="sxs-lookup"><span data-stu-id="92162-111">&nbsp;&nbsp;&nbsp;└─ [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md)</span></span> <br><span data-ttu-id="92162-112">&nbsp;&nbsp;&nbsp;└─ [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="92162-112">&nbsp;&nbsp;&nbsp;└─ [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md)</span></span> <br><span data-ttu-id="92162-113">&nbsp;&nbsp;&nbsp;└─ [画像](view-model-control-image-iimage-iimage.md)</span><span class="sxs-lookup"><span data-stu-id="92162-113">&nbsp;&nbsp;&nbsp;└─ [Image](view-model-control-image-iimage-iimage.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="92162-114">指数</span><span class="sxs-lookup"><span data-stu-id="92162-114">Index</span></span>

### <a name="properties"></a><span data-ttu-id="92162-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="92162-115">Properties</span></span>

* [<span data-ttu-id="92162-116">コンテナー</span><span class="sxs-lookup"><span data-stu-id="92162-116">container</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#container)
* [<span data-ttu-id="92162-117">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="92162-117">generic</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#generic)
* [<span data-ttu-id="92162-118">getDataSource</span><span class="sxs-lookup"><span data-stu-id="92162-118">getDataSource</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)
* [<span data-ttu-id="92162-119">非表示</span><span class="sxs-lookup"><span data-stu-id="92162-119">hidden</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#hidden)

### <a name="methods"></a><span data-ttu-id="92162-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="92162-120">Methods</span></span>

* [<span data-ttu-id="92162-121">applyDesign</span><span class="sxs-lookup"><span data-stu-id="92162-121">applyDesign</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)
* [<span data-ttu-id="92162-122">dataContext</span><span class="sxs-lookup"><span data-stu-id="92162-122">dataContext</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)
* [<span data-ttu-id="92162-123">getDesign</span><span class="sxs-lookup"><span data-stu-id="92162-123">getDesign</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)
* [<span data-ttu-id="92162-124">isEditable</span><span class="sxs-lookup"><span data-stu-id="92162-124">isEditable</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)
* [<span data-ttu-id="92162-125">メタデータ</span><span class="sxs-lookup"><span data-stu-id="92162-125">metadata</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#metadata)
* [<span data-ttu-id="92162-126">親</span><span class="sxs-lookup"><span data-stu-id="92162-126">parent</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#parent)
* [<span data-ttu-id="92162-127">ルート</span><span class="sxs-lookup"><span data-stu-id="92162-127">root</span></span>](view-model-control-basecontrol-icontrol-icontrol.md#root)

## <a name="properties"></a><span data-ttu-id="92162-128">プロパティ</span><span class="sxs-lookup"><span data-stu-id="92162-128">Properties</span></span>

### <a name="container"></a><span data-ttu-id="92162-129">コンテナー</span><span class="sxs-lookup"><span data-stu-id="92162-129">container</span></span>

<span data-ttu-id="92162-130">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="92162-130">container: boolean (optional)</span></span> 

<span data-ttu-id="92162-131">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="92162-131">True if the control is a container.</span></span>


### <a name="generic"></a><span data-ttu-id="92162-132">generic</span><span class="sxs-lookup"><span data-stu-id="92162-132">generic</span></span>

<span data-ttu-id="92162-133">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="92162-133">generic: boolean (optional)</span></span> 




### <a name="getdatasource"></a><span data-ttu-id="92162-134">getDataSource</span><span class="sxs-lookup"><span data-stu-id="92162-134">getDataSource</span></span>

<span data-ttu-id="92162-135">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="92162-135">getDataSource: function(): any</span></span>




### <a name="hidden"></a><span data-ttu-id="92162-136">hidden</span><span class="sxs-lookup"><span data-stu-id="92162-136">hidden</span></span>

<span data-ttu-id="92162-137">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="92162-137">hidden: boolean</span></span>

<span data-ttu-id="92162-138">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="92162-138">True if the control is hidden.</span></span>


## <a name="methods"></a><span data-ttu-id="92162-139">メソッド</span><span class="sxs-lookup"><span data-stu-id="92162-139">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="92162-140">applyDesign</span><span class="sxs-lookup"><span data-stu-id="92162-140">applyDesign</span></span>


<span data-ttu-id="92162-141">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="92162-141">applyDesign(design: [Design](view-model-ipage-idesign.md)): void</span></span>

<span data-ttu-id="92162-142">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="92162-142">Applies given design to the design on the control.</span></span>
<span data-ttu-id="92162-143">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="92162-143">If a design already exists, the prototype chain of the design will be preserved.</span></span>


#### <a name="parameters"></a><span data-ttu-id="92162-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92162-144">Parameters</span></span>

| <span data-ttu-id="92162-145">氏名</span><span class="sxs-lookup"><span data-stu-id="92162-145">Name</span></span> | <span data-ttu-id="92162-146">種類</span><span class="sxs-lookup"><span data-stu-id="92162-146">Type</span></span> | <span data-ttu-id="92162-147">説明</span><span class="sxs-lookup"><span data-stu-id="92162-147">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="92162-148">design</span><span class="sxs-lookup"><span data-stu-id="92162-148">design</span></span>|[<span data-ttu-id="92162-149">Design</span><span class="sxs-lookup"><span data-stu-id="92162-149">Design</span></span>](view-model-ipage-idesign.md)|<span data-ttu-id="92162-150">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="92162-150">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="92162-151">void を返します</span><span class="sxs-lookup"><span data-stu-id="92162-151">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="92162-152">dataContext</span><span class="sxs-lookup"><span data-stu-id="92162-152">dataContext</span></span>


<span data-ttu-id="92162-153">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="92162-153">dataContext(): any</span></span>



#### <a name="returns-any"></a><span data-ttu-id="92162-154">any を返します</span><span class="sxs-lookup"><span data-stu-id="92162-154">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="92162-155">getDesign</span><span class="sxs-lookup"><span data-stu-id="92162-155">getDesign</span></span>


<span data-ttu-id="92162-156">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="92162-156">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="92162-157">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="92162-157">Returns the design object of this control.</span></span>

#### <a name="returns-design"></a><span data-ttu-id="92162-158">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="92162-158">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="iseditable"></a><span data-ttu-id="92162-159">isEditable</span><span class="sxs-lookup"><span data-stu-id="92162-159">isEditable</span></span>


<span data-ttu-id="92162-160">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="92162-160">isEditable(): boolean</span></span>

<span data-ttu-id="92162-161">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="92162-161">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="92162-162">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="92162-162">Returns false when either the control or its parent is not editable.</span></span>
<span data-ttu-id="92162-163">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="92162-163">Returns true when both the control and its parent are editable.</span></span>
<span data-ttu-id="92162-164">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="92162-164">Returns true when either the control or its parent is editable and the other is undefined.</span></span>
<span data-ttu-id="92162-165">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="92162-165">Returns undefined if both the control's edit-ability and its parent's edit-ability is undefined.</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="92162-166">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="92162-166">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="92162-167">metadata</span><span class="sxs-lookup"><span data-stu-id="92162-167">metadata</span></span>


<span data-ttu-id="92162-168">metadata(): [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="92162-168">metadata(): [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span></span>

<span data-ttu-id="92162-169">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="92162-169">Returns the metadata object of this control.</span></span>

#### <a name="returns-controlmetadata"></a><span data-ttu-id="92162-170">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="92162-170">Returns [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="92162-171">parent</span><span class="sxs-lookup"><span data-stu-id="92162-171">parent</span></span>


<span data-ttu-id="92162-172">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="92162-172">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="92162-173">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="92162-173">Returns the parent (control or page) of this control.</span></span>

#### <a name="returns-control-124-page"></a><span data-ttu-id="92162-174">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="92162-174">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="92162-175">root</span><span class="sxs-lookup"><span data-stu-id="92162-175">root</span></span>


<span data-ttu-id="92162-176">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="92162-176">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="92162-177">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="92162-177">Returns the root form instance (page) of this control.</span></span>

#### <a name="returns-page"></a><span data-ttu-id="92162-178">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="92162-178">Returns [Page](view-model-ipage-ipage.md)</span></span>



