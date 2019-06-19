---
title: ControlMetadata タイプ
description: コントロールのメタデータのインターフェイス。 コントロール メタデータをオーバーライドすると、コントロール&#x27;の外観と動作を変更できます。
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
ms.openlocfilehash: b521ec2b1881fa5dcbb44667775a817ae75a87d3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554372"
---
# <a name="controlmetadata-type"></a><span data-ttu-id="0c156-104">ControlMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="0c156-104">ControlMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="0c156-105">コントロールのメタデータのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="0c156-105">Interface for the metadata of a control.</span></span> <span data-ttu-id="0c156-106">コントロール メタデータをオーバーライドすると、コントロールの外観と動作を変更できます。</span><span class="sxs-lookup"><span data-stu-id="0c156-106">Overriding control metadata can modify a controls' look and behavior.</span></span>
<span data-ttu-id="0c156-107">変更できるプロパティはコントロールによって異なりますが、すべてのコントロールにここに表示される基準のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="0c156-107">Properties that can be modified vary by control but every control will have the base properties listed here.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="0c156-108">階層</span><span class="sxs-lookup"><span data-stu-id="0c156-108">Hierarchy</span></span>

<span data-ttu-id="0c156-109">ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="0c156-109">ControlMetadata</span></span> <br><span data-ttu-id="0c156-110">&nbsp;&nbsp;&nbsp;└─ [PageLinkMetadata](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="0c156-110">&nbsp;&nbsp;&nbsp;└─ [PageLinkMetadata](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md)</span></span> <br><span data-ttu-id="0c156-111">&nbsp;&nbsp;&nbsp;└─ [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="0c156-111">&nbsp;&nbsp;&nbsp;└─ [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md)</span></span> <br><span data-ttu-id="0c156-112">&nbsp;&nbsp;&nbsp;└─ [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="0c156-112">&nbsp;&nbsp;&nbsp;└─ [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)</span></span> <br><span data-ttu-id="0c156-113">&nbsp;&nbsp;&nbsp;└─ [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="0c156-113">&nbsp;&nbsp;&nbsp;└─ [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)</span></span> <br>

## <a name="index"></a><span data-ttu-id="0c156-114">指数</span><span class="sxs-lookup"><span data-stu-id="0c156-114">Index</span></span>

### <a name="properties"></a><span data-ttu-id="0c156-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c156-115">Properties</span></span>

* [<span data-ttu-id="0c156-116">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="0c156-116">BoundEntity</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity)
* [<span data-ttu-id="0c156-117">BoundField</span><span class="sxs-lookup"><span data-stu-id="0c156-117">BoundField</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield)
* [<span data-ttu-id="0c156-118">説明</span><span class="sxs-lookup"><span data-stu-id="0c156-118">Description</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description)
* [<span data-ttu-id="0c156-119">編集可能</span><span class="sxs-lookup"><span data-stu-id="0c156-119">Editable</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable)
* [<span data-ttu-id="0c156-120">ExtType</span><span class="sxs-lookup"><span data-stu-id="0c156-120">ExtType</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype)
* [<span data-ttu-id="0c156-121">HelpText</span><span class="sxs-lookup"><span data-stu-id="0c156-121">HelpText</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext)
* [<span data-ttu-id="0c156-122">非表示</span><span class="sxs-lookup"><span data-stu-id="0c156-122">Hidden</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden)
* [<span data-ttu-id="0c156-123">ID</span><span class="sxs-lookup"><span data-stu-id="0c156-123">Id</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id)
* [<span data-ttu-id="0c156-124">ラベル</span><span class="sxs-lookup"><span data-stu-id="0c156-124">Label</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label)
* [<span data-ttu-id="0c156-125">名前</span><span class="sxs-lookup"><span data-stu-id="0c156-125">Name</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name)
* [<span data-ttu-id="0c156-126">注文</span><span class="sxs-lookup"><span data-stu-id="0c156-126">Order</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order)
* <span data-ttu-id="0c156-127">[[タイプ](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)]</span><span class="sxs-lookup"><span data-stu-id="0c156-127">[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)</span></span>

## <a name="properties"></a><span data-ttu-id="0c156-128">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c156-128">Properties</span></span>

### <a name="boundentity"></a><span data-ttu-id="0c156-129">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="0c156-129">BoundEntity</span></span>

<span data-ttu-id="0c156-130">BoundEntity: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0c156-130">BoundEntity: string (optional)</span></span> 

<span data-ttu-id="0c156-131">コントロールがバインドされるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="0c156-131">The entity to which the control is bound.</span></span>


### <a name="boundfield"></a><span data-ttu-id="0c156-132">BoundField</span><span class="sxs-lookup"><span data-stu-id="0c156-132">BoundField</span></span>

<span data-ttu-id="0c156-133">BoundField: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0c156-133">BoundField: string (optional)</span></span> 




### <a name="description"></a><span data-ttu-id="0c156-134">説明</span><span class="sxs-lookup"><span data-stu-id="0c156-134">Description</span></span>

<span data-ttu-id="0c156-135">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0c156-135">Description: string (optional)</span></span> 

<span data-ttu-id="0c156-136">コントロールの説明。</span><span class="sxs-lookup"><span data-stu-id="0c156-136">Description of the control.</span></span>


### <a name="editable"></a><span data-ttu-id="0c156-137">編集可能</span><span class="sxs-lookup"><span data-stu-id="0c156-137">Editable</span></span>

<span data-ttu-id="0c156-138">編集可能: プール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="0c156-138">Editable: boolean (optional)</span></span> 

<span data-ttu-id="0c156-139">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0c156-139">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="0c156-140">コントロールまたはその親が編集可能でない場合は、False です。</span><span class="sxs-lookup"><span data-stu-id="0c156-140">False when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="0c156-141">コントロールとその親の両方が編集可能な場合、true です。</span><span class="sxs-lookup"><span data-stu-id="0c156-141">True when both the control and it's parent are editable.</span></span>
<span data-ttu-id="0c156-142">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="0c156-142">True when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="0c156-143">コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="0c156-143">Undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>


### <a name="exttype"></a><span data-ttu-id="0c156-144">ExtType</span><span class="sxs-lookup"><span data-stu-id="0c156-144">ExtType</span></span>

<span data-ttu-id="0c156-145">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="0c156-145">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="0c156-146">拡張されたコントロール タイプです。</span><span class="sxs-lookup"><span data-stu-id="0c156-146">The extended control type.</span></span> <span data-ttu-id="0c156-147">E.g.</span><span class="sxs-lookup"><span data-stu-id="0c156-147">E.g.</span></span> <span data-ttu-id="0c156-148">コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0c156-148">a control of type Input might have an extended type of Barcode.</span></span>


### <a name="helptext"></a><span data-ttu-id="0c156-149">HelpText</span><span class="sxs-lookup"><span data-stu-id="0c156-149">HelpText</span></span>

<span data-ttu-id="0c156-150">HelpText: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0c156-150">HelpText: string (optional)</span></span> 

<span data-ttu-id="0c156-151">コマンドのキーボード ショートカットです。</span><span class="sxs-lookup"><span data-stu-id="0c156-151">The keyboard shortcut for a command.</span></span> <span data-ttu-id="0c156-152">E.g.</span><span class="sxs-lookup"><span data-stu-id="0c156-152">E.g.</span></span> <span data-ttu-id="0c156-153">「(Shift + F5)」</span><span class="sxs-lookup"><span data-stu-id="0c156-153">"(Shift+F5)"</span></span>


### <a name="hidden"></a><span data-ttu-id="0c156-154">非表示</span><span class="sxs-lookup"><span data-stu-id="0c156-154">Hidden</span></span>

<span data-ttu-id="0c156-155">非表示: ブール値 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0c156-155">Hidden: boolean (optional)</span></span> 

<span data-ttu-id="0c156-156">コントロールを非表示にするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0c156-156">Boolean indicating if the control is hidden or not.</span></span>


### <a name="id"></a><span data-ttu-id="0c156-157">ID</span><span class="sxs-lookup"><span data-stu-id="0c156-157">Id</span></span>

<span data-ttu-id="0c156-158">Id: string (オプション)</span><span class="sxs-lookup"><span data-stu-id="0c156-158">Id: string (optional)</span></span> 

<span data-ttu-id="0c156-159">コントロールの ID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="0c156-159">Identification string for a control.</span></span>


### <a name="label"></a><span data-ttu-id="0c156-160">ラベル</span><span class="sxs-lookup"><span data-stu-id="0c156-160">Label</span></span>

<span data-ttu-id="0c156-161">ラベル: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="0c156-161">Label: string (optional)</span></span> 

<span data-ttu-id="0c156-162">コントロールのラベル。</span><span class="sxs-lookup"><span data-stu-id="0c156-162">Label for a control.</span></span> <span data-ttu-id="0c156-163">E.g.</span><span class="sxs-lookup"><span data-stu-id="0c156-163">E.g.</span></span> <span data-ttu-id="0c156-164">個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。</span><span class="sxs-lookup"><span data-stu-id="0c156-164">a control representing a person's first name might have a label "First Name".</span></span>


### <a name="name"></a><span data-ttu-id="0c156-165">氏名</span><span class="sxs-lookup"><span data-stu-id="0c156-165">Name</span></span>

<span data-ttu-id="0c156-166">Name: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="0c156-166">Name: string (optional)</span></span> 

<span data-ttu-id="0c156-167">コントロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="0c156-167">Name of a control.</span></span>


### <a name="order"></a><span data-ttu-id="0c156-168">注文</span><span class="sxs-lookup"><span data-stu-id="0c156-168">Order</span></span>

<span data-ttu-id="0c156-169">注文: 番号 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0c156-169">Order: number (optional)</span></span> 

<span data-ttu-id="0c156-170">コントロールがページに表示される順序を示す番号。</span><span class="sxs-lookup"><span data-stu-id="0c156-170">Number indicating the order in which a control will appear on a page.</span></span>


### <a name="type"></a><span data-ttu-id="0c156-171">種類</span><span class="sxs-lookup"><span data-stu-id="0c156-171">Type</span></span>

<span data-ttu-id="0c156-172">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="0c156-172">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="0c156-173">コントロール タイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="0c156-173">String indicating the control type.</span></span>


