---
title: 画像タイプ
description: モバイル アプリ内のイメージを表すためのイメージ コントロール インターフェイス。
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
ms.openlocfilehash: 9b77308dca5691fbd33d9dda7124549148915ed0
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129265"
---
# <a name="image-type"></a><span data-ttu-id="cb798-103">画像タイプ</span><span class="sxs-lookup"><span data-stu-id="cb798-103">Image type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="cb798-104">モバイル アプリ内のイメージを表すためのイメージ コントロール インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="cb798-104">Image control interface for representing images in the mobile app.</span></span>
<span data-ttu-id="cb798-105">イメージは、次のいずれかの種類を使用できます。DataUri、Base64、URL、AOTResource、または Symbol。</span><span class="sxs-lookup"><span data-stu-id="cb798-105">Images can be of any of the following types: DataUri, Base64, URL, AOTResource, or Symbol.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="cb798-106">階層</span><span class="sxs-lookup"><span data-stu-id="cb798-106">Hierarchy</span></span>

[<span data-ttu-id="cb798-107">コントロール</span><span class="sxs-lookup"><span data-stu-id="cb798-107">Control</span></span>](view-model-control-basecontrol-icontrol-icontrol.md) <br><span data-ttu-id="cb798-108">&nbsp;&nbsp;&nbsp;└─ 画像</span><span class="sxs-lookup"><span data-stu-id="cb798-108">&nbsp;&nbsp;&nbsp;└─ Image</span></span> <br>

## <a name="index"></a><span data-ttu-id="cb798-109">指数</span><span class="sxs-lookup"><span data-stu-id="cb798-109">Index</span></span>

### <a name="properties"></a><span data-ttu-id="cb798-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb798-110">Properties</span></span>

* [<span data-ttu-id="cb798-111">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cb798-111">container</span></span>](view-model-control-image-iimage-iimage.md#container)
* [<span data-ttu-id="cb798-112">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="cb798-112">generic</span></span>](view-model-control-image-iimage-iimage.md#generic)
* [<span data-ttu-id="cb798-113">getDataSource</span><span class="sxs-lookup"><span data-stu-id="cb798-113">getDataSource</span></span>](view-model-control-image-iimage-iimage.md#getdatasource)
* [<span data-ttu-id="cb798-114">非表示</span><span class="sxs-lookup"><span data-stu-id="cb798-114">hidden</span></span>](view-model-control-image-iimage-iimage.md#hidden)
* [<span data-ttu-id="cb798-115">imageSource</span><span class="sxs-lookup"><span data-stu-id="cb798-115">imageSource</span></span>](view-model-control-image-iimage-iimage.md#imagesource)
* [<span data-ttu-id="cb798-116">imageView</span><span class="sxs-lookup"><span data-stu-id="cb798-116">imageView</span></span>](view-model-control-image-iimage-iimage.md#imageview)
* [<span data-ttu-id="cb798-117">placeholderClass</span><span class="sxs-lookup"><span data-stu-id="cb798-117">placeholderClass</span></span>](view-model-control-image-iimage-iimage.md#placeholderclass)
* [<span data-ttu-id="cb798-118">記号</span><span class="sxs-lookup"><span data-stu-id="cb798-118">symbol</span></span>](view-model-control-image-iimage-iimage.md#symbol)

### <a name="methods"></a><span data-ttu-id="cb798-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="cb798-119">Methods</span></span>

* [<span data-ttu-id="cb798-120">applyDesign</span><span class="sxs-lookup"><span data-stu-id="cb798-120">applyDesign</span></span>](view-model-control-image-iimage-iimage.md#applydesign)
* [<span data-ttu-id="cb798-121">dataContext</span><span class="sxs-lookup"><span data-stu-id="cb798-121">dataContext</span></span>](view-model-control-image-iimage-iimage.md#datacontext)
* [<span data-ttu-id="cb798-122">getDesign</span><span class="sxs-lookup"><span data-stu-id="cb798-122">getDesign</span></span>](view-model-control-image-iimage-iimage.md#getdesign)
* [<span data-ttu-id="cb798-123">isEditable</span><span class="sxs-lookup"><span data-stu-id="cb798-123">isEditable</span></span>](view-model-control-image-iimage-iimage.md#iseditable)
* [<span data-ttu-id="cb798-124">メタデータ</span><span class="sxs-lookup"><span data-stu-id="cb798-124">metadata</span></span>](view-model-control-image-iimage-iimage.md#metadata)
* [<span data-ttu-id="cb798-125">親</span><span class="sxs-lookup"><span data-stu-id="cb798-125">parent</span></span>](view-model-control-image-iimage-iimage.md#parent)
* [<span data-ttu-id="cb798-126">ルート</span><span class="sxs-lookup"><span data-stu-id="cb798-126">root</span></span>](view-model-control-image-iimage-iimage.md#root)

## <a name="properties"></a><span data-ttu-id="cb798-127">プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb798-127">Properties</span></span>

### <a name="container"></a><span data-ttu-id="cb798-128">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cb798-128">container</span></span>

<span data-ttu-id="cb798-129">container: ブール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="cb798-129">container: boolean (optional)</span></span> 

<span data-ttu-id="cb798-130">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="cb798-130">True if the control is a container.</span></span>

> <span data-ttu-id="cb798-131">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-131">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="generic"></a><span data-ttu-id="cb798-132">generic</span><span class="sxs-lookup"><span data-stu-id="cb798-132">generic</span></span>

<span data-ttu-id="cb798-133">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="cb798-133">generic: boolean (optional)</span></span> 



> <span data-ttu-id="cb798-134">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-134">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="cb798-135">getDataSource</span><span class="sxs-lookup"><span data-stu-id="cb798-135">getDataSource</span></span>

<span data-ttu-id="cb798-136">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="cb798-136">getDataSource: function(): any</span></span>



> <span data-ttu-id="cb798-137">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-137">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="cb798-138">hidden</span><span class="sxs-lookup"><span data-stu-id="cb798-138">hidden</span></span>

<span data-ttu-id="cb798-139">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="cb798-139">hidden: boolean</span></span>

<span data-ttu-id="cb798-140">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="cb798-140">True if the control is hidden.</span></span>

> <span data-ttu-id="cb798-141">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-141">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


### <a name="imagesource"></a><span data-ttu-id="cb798-142">imageSource</span><span class="sxs-lookup"><span data-stu-id="cb798-142">imageSource</span></span>

<span data-ttu-id="cb798-143">imageSource: string</span><span class="sxs-lookup"><span data-stu-id="cb798-143">imageSource: string</span></span>

<span data-ttu-id="cb798-144">ImageSource を定義します。</span><span class="sxs-lookup"><span data-stu-id="cb798-144">Defines the imageSource.</span></span>


### <a name="imageview"></a><span data-ttu-id="cb798-145">imageView</span><span class="sxs-lookup"><span data-stu-id="cb798-145">imageView</span></span>

<span data-ttu-id="cb798-146">imageView: string</span><span class="sxs-lookup"><span data-stu-id="cb798-146">imageView: string</span></span>

<span data-ttu-id="cb798-147">画像のスタイルを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb798-147">Dictates the style of the image.</span></span>


### <a name="placeholderclass"></a><span data-ttu-id="cb798-148">placeholderClass</span><span class="sxs-lookup"><span data-stu-id="cb798-148">placeholderClass</span></span>

<span data-ttu-id="cb798-149">placeholderClass: string</span><span class="sxs-lookup"><span data-stu-id="cb798-149">placeholderClass: string</span></span>




### <a name="symbol"></a><span data-ttu-id="cb798-150">symbol</span><span class="sxs-lookup"><span data-stu-id="cb798-150">symbol</span></span>

<span data-ttu-id="cb798-151">symbol: string</span><span class="sxs-lookup"><span data-stu-id="cb798-151">symbol: string</span></span>

<span data-ttu-id="cb798-152">イメージがシンボル型である場合、シンボルを定義します。</span><span class="sxs-lookup"><span data-stu-id="cb798-152">Defines the symbol if the image is of type symbol.</span></span>


## <a name="methods"></a><span data-ttu-id="cb798-153">メソッド</span><span class="sxs-lookup"><span data-stu-id="cb798-153">Methods</span></span>

### <a name="applydesign"></a><span data-ttu-id="cb798-154">applyDesign</span><span class="sxs-lookup"><span data-stu-id="cb798-154">applyDesign</span></span>


<span data-ttu-id="cb798-155">applyDesign(design: [ImageDesign](view-model-control-image-iimage-iimagedesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="cb798-155">applyDesign(design: [ImageDesign](view-model-control-image-iimage-iimagedesign.md)): void</span></span>

<span data-ttu-id="cb798-156">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="cb798-156">Applies given design to the design on the control.</span></span>
<span data-ttu-id="cb798-157">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="cb798-157">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="cb798-158">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="cb798-158">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="cb798-159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cb798-159">Parameters</span></span>

| <span data-ttu-id="cb798-160">氏名</span><span class="sxs-lookup"><span data-stu-id="cb798-160">Name</span></span> | <span data-ttu-id="cb798-161">種類</span><span class="sxs-lookup"><span data-stu-id="cb798-161">Type</span></span> | <span data-ttu-id="cb798-162">説明</span><span class="sxs-lookup"><span data-stu-id="cb798-162">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="cb798-163">design</span><span class="sxs-lookup"><span data-stu-id="cb798-163">design</span></span>|[<span data-ttu-id="cb798-164">ImageDesign</span><span class="sxs-lookup"><span data-stu-id="cb798-164">ImageDesign</span></span>](view-model-control-image-iimage-iimagedesign.md)|<span data-ttu-id="cb798-165">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="cb798-165">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="cb798-166">void を返します</span><span class="sxs-lookup"><span data-stu-id="cb798-166">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="cb798-167">dataContext</span><span class="sxs-lookup"><span data-stu-id="cb798-167">dataContext</span></span>


<span data-ttu-id="cb798-168">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="cb798-168">dataContext(): any</span></span>



> <span data-ttu-id="cb798-169">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-169">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="cb798-170">any を返します</span><span class="sxs-lookup"><span data-stu-id="cb798-170">Returns any</span></span>

### <a name="getdesign"></a><span data-ttu-id="cb798-171">getDesign</span><span class="sxs-lookup"><span data-stu-id="cb798-171">getDesign</span></span>


<span data-ttu-id="cb798-172">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="cb798-172">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="cb798-173">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-173">Returns the design object of this control.</span></span>

> <span data-ttu-id="cb798-174">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-174">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-design"></a><span data-ttu-id="cb798-175">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="cb798-175">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="iseditable"></a><span data-ttu-id="cb798-176">isEditable</span><span class="sxs-lookup"><span data-stu-id="cb798-176">isEditable</span></span>


<span data-ttu-id="cb798-177">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="cb798-177">isEditable(): boolean</span></span>

<span data-ttu-id="cb798-178">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="cb798-178">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="cb798-179">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-179">Returns false when either the control or its parent is not editable.</span></span>
<span data-ttu-id="cb798-180">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-180">Returns true when both the control and its parent are editable.</span></span>
<span data-ttu-id="cb798-181">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-181">Returns true when either the control or its parent is editable and the other is undefined.</span></span>
<span data-ttu-id="cb798-182">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-182">Returns undefined if both the control's edit-ability and its parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="cb798-183">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-183">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="cb798-184">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="cb798-184">Returns boolean</span></span>



### <a name="metadata"></a><span data-ttu-id="cb798-185">metadata</span><span class="sxs-lookup"><span data-stu-id="cb798-185">metadata</span></span>


<span data-ttu-id="cb798-186">metadata(): [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="cb798-186">metadata(): [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)</span></span>

<span data-ttu-id="cb798-187">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-187">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="cb798-188">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="cb798-188">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata)</span></span>

#### <a name="returns-imagemetadata"></a><span data-ttu-id="cb798-189">[ImageMetadata](view-model-control-image-iimage-iimagemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="cb798-189">Returns [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="cb798-190">parent</span><span class="sxs-lookup"><span data-stu-id="cb798-190">parent</span></span>


<span data-ttu-id="cb798-191">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="cb798-191">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="cb798-192">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-192">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="cb798-193">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-193">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-control-124-page"></a><span data-ttu-id="cb798-194">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="cb798-194">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="root"></a><span data-ttu-id="cb798-195">root</span><span class="sxs-lookup"><span data-stu-id="cb798-195">root</span></span>


<span data-ttu-id="cb798-196">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="cb798-196">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="cb798-197">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="cb798-197">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="cb798-198">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="cb798-198">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-page"></a><span data-ttu-id="cb798-199">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="cb798-199">Returns [Page](view-model-ipage-ipage.md)</span></span>



