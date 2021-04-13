---
title: ControlMetadata タイプ
description: コントロールのメタデータのインターフェイス。 コントロール メタデータをオーバーライドすると、コントロール&#x27;の外観と動作を変更できます。
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
ms.openlocfilehash: 3a10a9f9a0264284db5173fe3be8a5db9c395e43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752696"
---
# <a name="controlmetadata-type"></a><span data-ttu-id="3f5d0-104">ControlMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="3f5d0-104">ControlMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="3f5d0-105">コントロールのメタデータのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-105">Interface for the metadata of a control.</span></span> <span data-ttu-id="3f5d0-106">コントロール メタデータをオーバーライドすると、コントロールの外観と動作を変更できます。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-106">Overriding control metadata can modify a controls' look and behavior.</span></span>
<span data-ttu-id="3f5d0-107">変更できるプロパティはコントロールによって異なりますが、すべてのコントロールにここに表示される基準のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-107">Properties that can be modified vary by control but every control will have the base properties listed here.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="3f5d0-108">階層</span><span class="sxs-lookup"><span data-stu-id="3f5d0-108">Hierarchy</span></span>

<span data-ttu-id="3f5d0-109">ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="3f5d0-109">ControlMetadata</span></span> <br><span data-ttu-id="3f5d0-110">&nbsp;&nbsp;&nbsp;└─ [PageLinkMetadata](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-110">&nbsp;&nbsp;&nbsp;└─ [PageLinkMetadata](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md)</span></span> <br><span data-ttu-id="3f5d0-111">&nbsp;&nbsp;&nbsp;└─ [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-111">&nbsp;&nbsp;&nbsp;└─ [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md)</span></span> <br><span data-ttu-id="3f5d0-112">&nbsp;&nbsp;&nbsp;└─ [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-112">&nbsp;&nbsp;&nbsp;└─ [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span></span> <br><span data-ttu-id="3f5d0-113">&nbsp;&nbsp;&nbsp;└─ [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-113">&nbsp;&nbsp;&nbsp;└─ [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="3f5d0-114">指数</span><span class="sxs-lookup"><span data-stu-id="3f5d0-114">Index</span></span>

### <a name="properties"></a><span data-ttu-id="3f5d0-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3f5d0-115">Properties</span></span>

* [<span data-ttu-id="3f5d0-116">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="3f5d0-116">BoundEntity</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity)
* [<span data-ttu-id="3f5d0-117">BoundField</span><span class="sxs-lookup"><span data-stu-id="3f5d0-117">BoundField</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield)
* [<span data-ttu-id="3f5d0-118">説明</span><span class="sxs-lookup"><span data-stu-id="3f5d0-118">Description</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description)
* [<span data-ttu-id="3f5d0-119">編集可能</span><span class="sxs-lookup"><span data-stu-id="3f5d0-119">Editable</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable)
* [<span data-ttu-id="3f5d0-120">ExtType</span><span class="sxs-lookup"><span data-stu-id="3f5d0-120">ExtType</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype)
* [<span data-ttu-id="3f5d0-121">HelpText</span><span class="sxs-lookup"><span data-stu-id="3f5d0-121">HelpText</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext)
* [<span data-ttu-id="3f5d0-122">非表示</span><span class="sxs-lookup"><span data-stu-id="3f5d0-122">Hidden</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden)
* [<span data-ttu-id="3f5d0-123">ID</span><span class="sxs-lookup"><span data-stu-id="3f5d0-123">Id</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id)
* [<span data-ttu-id="3f5d0-124">ラベル</span><span class="sxs-lookup"><span data-stu-id="3f5d0-124">Label</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label)
* [<span data-ttu-id="3f5d0-125">名前</span><span class="sxs-lookup"><span data-stu-id="3f5d0-125">Name</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name)
* [<span data-ttu-id="3f5d0-126">注文</span><span class="sxs-lookup"><span data-stu-id="3f5d0-126">Order</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order)
* <span data-ttu-id="3f5d0-127">[[タイプ](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)]</span><span class="sxs-lookup"><span data-stu-id="3f5d0-127">[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)</span></span>

## <a name="properties"></a><span data-ttu-id="3f5d0-128">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3f5d0-128">Properties</span></span>

### <a name="boundentity"></a><span data-ttu-id="3f5d0-129">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="3f5d0-129">BoundEntity</span></span>

<span data-ttu-id="3f5d0-130">BoundEntity: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-130">BoundEntity: string (optional)</span></span> 

<span data-ttu-id="3f5d0-131">コントロールがバインドされるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-131">The entity to which the control is bound.</span></span>


### <a name="boundfield"></a><span data-ttu-id="3f5d0-132">BoundField</span><span class="sxs-lookup"><span data-stu-id="3f5d0-132">BoundField</span></span>

<span data-ttu-id="3f5d0-133">BoundField: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-133">BoundField: string (optional)</span></span> 




### <a name="description"></a><span data-ttu-id="3f5d0-134">説明</span><span class="sxs-lookup"><span data-stu-id="3f5d0-134">Description</span></span>

<span data-ttu-id="3f5d0-135">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-135">Description: string (optional)</span></span> 

<span data-ttu-id="3f5d0-136">コントロールの説明。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-136">Description of the control.</span></span>


### <a name="editable"></a><span data-ttu-id="3f5d0-137">編集可能</span><span class="sxs-lookup"><span data-stu-id="3f5d0-137">Editable</span></span>

<span data-ttu-id="3f5d0-138">編集可能: プール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-138">Editable: boolean (optional)</span></span> 

<span data-ttu-id="3f5d0-139">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-139">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="3f5d0-140">コントロールまたはその親が編集可能でない場合は、False です。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-140">False when either the control or its parent is not editable.</span></span>
<span data-ttu-id="3f5d0-141">コントロールとその親の両方が編集可能な場合、true です。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-141">True when both the control and its parent are editable.</span></span>
<span data-ttu-id="3f5d0-142">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-142">True when either the control or its parent is editable and the other is undefined.</span></span>
<span data-ttu-id="3f5d0-143">コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-143">Undefined if both the control's edit-ability and its parent's edit-ability is undefined.</span></span>


### <a name="exttype"></a><span data-ttu-id="3f5d0-144">ExtType</span><span class="sxs-lookup"><span data-stu-id="3f5d0-144">ExtType</span></span>

<span data-ttu-id="3f5d0-145">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-145">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="3f5d0-146">拡張されたコントロール タイプです。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-146">The extended control type.</span></span> <span data-ttu-id="3f5d0-147">たとえば、コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-147">For example, a control of type Input might have an extended type of Barcode.</span></span>


### <a name="helptext"></a><span data-ttu-id="3f5d0-148">HelpText</span><span class="sxs-lookup"><span data-stu-id="3f5d0-148">HelpText</span></span>

<span data-ttu-id="3f5d0-149">HelpText: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-149">HelpText: string (optional)</span></span> 

<span data-ttu-id="3f5d0-150">コマンドのキーボード ショートカットです。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-150">The keyboard shortcut for a command.</span></span> <span data-ttu-id="3f5d0-151">たとえば、「(Shift + F5)」</span><span class="sxs-lookup"><span data-stu-id="3f5d0-151">For example, "(Shift+F5)"</span></span>


### <a name="hidden"></a><span data-ttu-id="3f5d0-152">非表示</span><span class="sxs-lookup"><span data-stu-id="3f5d0-152">Hidden</span></span>

<span data-ttu-id="3f5d0-153">非表示: ブール値 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-153">Hidden: boolean (optional)</span></span> 

<span data-ttu-id="3f5d0-154">コントロールを非表示にするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-154">Boolean indicating if the control is hidden or not.</span></span>


### <a name="id"></a><span data-ttu-id="3f5d0-155">ID</span><span class="sxs-lookup"><span data-stu-id="3f5d0-155">Id</span></span>

<span data-ttu-id="3f5d0-156">Id: string (オプション)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-156">Id: string (optional)</span></span> 

<span data-ttu-id="3f5d0-157">コントロールの ID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-157">Identification string for a control.</span></span>


### <a name="label"></a><span data-ttu-id="3f5d0-158">ラベル</span><span class="sxs-lookup"><span data-stu-id="3f5d0-158">Label</span></span>

<span data-ttu-id="3f5d0-159">ラベル: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-159">Label: string (optional)</span></span> 

<span data-ttu-id="3f5d0-160">コントロールのラベル。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-160">Label for a control.</span></span> <span data-ttu-id="3f5d0-161">たとえば、個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-161">For example, a control representing a person's first name might have a label "First Name".</span></span>


### <a name="name"></a><span data-ttu-id="3f5d0-162">氏名</span><span class="sxs-lookup"><span data-stu-id="3f5d0-162">Name</span></span>

<span data-ttu-id="3f5d0-163">Name: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-163">Name: string (optional)</span></span> 

<span data-ttu-id="3f5d0-164">コントロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-164">Name of a control.</span></span>


### <a name="order"></a><span data-ttu-id="3f5d0-165">注文</span><span class="sxs-lookup"><span data-stu-id="3f5d0-165">Order</span></span>

<span data-ttu-id="3f5d0-166">注文: 番号 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-166">Order: number (optional)</span></span> 

<span data-ttu-id="3f5d0-167">コントロールがページに表示される順序を示す番号。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-167">Number indicating the order in which a control will appear on a page.</span></span>


### <a name="type"></a><span data-ttu-id="3f5d0-168">種類</span><span class="sxs-lookup"><span data-stu-id="3f5d0-168">Type</span></span>

<span data-ttu-id="3f5d0-169">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="3f5d0-169">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="3f5d0-170">コントロール タイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="3f5d0-170">String indicating the control type.</span></span>




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]