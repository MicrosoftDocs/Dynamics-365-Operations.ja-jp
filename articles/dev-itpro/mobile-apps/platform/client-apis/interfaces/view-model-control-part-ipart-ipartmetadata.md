---
title: "PartMetadata タイプ"
description: "パーツ メタデータ タイプ。"
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
ms.openlocfilehash: 020ce3277b756f2adc185bdf7b1b0652bbd5c3d6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="partmetadata-type"></a><span data-ttu-id="3b024-103">PartMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="3b024-103">PartMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="3b024-104">パーツ メタデータ タイプ。</span><span class="sxs-lookup"><span data-stu-id="3b024-104">Part metadata type.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="3b024-105">階層</span><span class="sxs-lookup"><span data-stu-id="3b024-105">Hierarchy</span></span>

[<span data-ttu-id="3b024-106">ContainerControlMetadata</span><span class="sxs-lookup"><span data-stu-id="3b024-106">ContainerControlMetadata</span></span>](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br><span data-ttu-id="3b024-107">&nbsp;&nbsp;&nbsp;└─ PartMetadata</span><span class="sxs-lookup"><span data-stu-id="3b024-107">&nbsp;&nbsp;&nbsp;└─ PartMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="3b024-108">指数</span><span class="sxs-lookup"><span data-stu-id="3b024-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="3b024-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b024-109">Properties</span></span>

* [<span data-ttu-id="3b024-110">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="3b024-110">BoundEntity</span></span>](view-model-control-part-ipart-ipartmetadata.md#boundentity)
* [<span data-ttu-id="3b024-111">BoundField</span><span class="sxs-lookup"><span data-stu-id="3b024-111">BoundField</span></span>](view-model-control-part-ipart-ipartmetadata.md#boundfield)
* [<span data-ttu-id="3b024-112">説明</span><span class="sxs-lookup"><span data-stu-id="3b024-112">Description</span></span>](view-model-control-part-ipart-ipartmetadata.md#description)
* [<span data-ttu-id="3b024-113">Design</span><span class="sxs-lookup"><span data-stu-id="3b024-113">Design</span></span>](view-model-control-part-ipart-ipartmetadata.md#design)
* [<span data-ttu-id="3b024-114">編集可能</span><span class="sxs-lookup"><span data-stu-id="3b024-114">Editable</span></span>](view-model-control-part-ipart-ipartmetadata.md#editable)
* [<span data-ttu-id="3b024-115">ExtType</span><span class="sxs-lookup"><span data-stu-id="3b024-115">ExtType</span></span>](view-model-control-part-ipart-ipartmetadata.md#exttype)
* [<span data-ttu-id="3b024-116">HelpText</span><span class="sxs-lookup"><span data-stu-id="3b024-116">HelpText</span></span>](view-model-control-part-ipart-ipartmetadata.md#helptext)
* [<span data-ttu-id="3b024-117">非表示</span><span class="sxs-lookup"><span data-stu-id="3b024-117">Hidden</span></span>](view-model-control-part-ipart-ipartmetadata.md#hidden)
* [<span data-ttu-id="3b024-118">ID</span><span class="sxs-lookup"><span data-stu-id="3b024-118">Id</span></span>](view-model-control-part-ipart-ipartmetadata.md#id)
* [<span data-ttu-id="3b024-119">ラベル</span><span class="sxs-lookup"><span data-stu-id="3b024-119">Label</span></span>](view-model-control-part-ipart-ipartmetadata.md#label)
* [<span data-ttu-id="3b024-120">名前</span><span class="sxs-lookup"><span data-stu-id="3b024-120">Name</span></span>](view-model-control-part-ipart-ipartmetadata.md#name)
* [<span data-ttu-id="3b024-121">注文</span><span class="sxs-lookup"><span data-stu-id="3b024-121">Order</span></span>](view-model-control-part-ipart-ipartmetadata.md#order)
* [<span data-ttu-id="3b024-122">ターゲット</span><span class="sxs-lookup"><span data-stu-id="3b024-122">Target</span></span>](view-model-control-part-ipart-ipartmetadata.md#target)
* <span data-ttu-id="3b024-123">[[タイプ](view-model-control-part-ipart-ipartmetadata.md#type)]</span><span class="sxs-lookup"><span data-stu-id="3b024-123">[Type](view-model-control-part-ipart-ipartmetadata.md#type)</span></span>

## <a name="properties"></a><span data-ttu-id="3b024-124">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b024-124">Properties</span></span>

### <a name="boundentity"></a><span data-ttu-id="3b024-125">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="3b024-125">BoundEntity</span></span>

<span data-ttu-id="3b024-126">BoundEntity: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-126">BoundEntity: string (optional)</span></span> 

<span data-ttu-id="3b024-127">コントロールがバインドされるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="3b024-127">The entity to which the control is bound.</span></span>

> <span data-ttu-id="3b024-128">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-128">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity)</span></span>


### <a name="boundfield"></a><span data-ttu-id="3b024-129">BoundField</span><span class="sxs-lookup"><span data-stu-id="3b024-129">BoundField</span></span>

<span data-ttu-id="3b024-130">BoundField: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-130">BoundField: string (optional)</span></span> 



> <span data-ttu-id="3b024-131">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-131">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield)</span></span>


### <a name="description"></a><span data-ttu-id="3b024-132">説明</span><span class="sxs-lookup"><span data-stu-id="3b024-132">Description</span></span>

<span data-ttu-id="3b024-133">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-133">Description: string (optional)</span></span> 

<span data-ttu-id="3b024-134">コントロールの説明。</span><span class="sxs-lookup"><span data-stu-id="3b024-134">Description of the control.</span></span>

> <span data-ttu-id="3b024-135">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-135">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description)</span></span>


### <a name="design"></a><span data-ttu-id="3b024-136">デザイン</span><span class="sxs-lookup"><span data-stu-id="3b024-136">Design</span></span>

<span data-ttu-id="3b024-137">デザイン: [PartDesign](view-model-control-part-ipart-ipartdesign.md) (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-137">Design: [PartDesign](view-model-control-part-ipart-ipartdesign.md) (optional)</span></span> 

<span data-ttu-id="3b024-138">ターゲット ページの設計をします。</span><span class="sxs-lookup"><span data-stu-id="3b024-138">Design for the target page.</span></span>


### <a name="editable"></a><span data-ttu-id="3b024-139">編集可能</span><span class="sxs-lookup"><span data-stu-id="3b024-139">Editable</span></span>

<span data-ttu-id="3b024-140">編集可能: プール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="3b024-140">Editable: boolean (optional)</span></span> 

<span data-ttu-id="3b024-141">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3b024-141">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="3b024-142">コントロールまたはその親が編集可能でない場合は、False です。</span><span class="sxs-lookup"><span data-stu-id="3b024-142">False when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="3b024-143">コントロールとその親の両方が編集可能な場合、true です。</span><span class="sxs-lookup"><span data-stu-id="3b024-143">True when both the control and it's parent are editable.</span></span>
<span data-ttu-id="3b024-144">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="3b024-144">True when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="3b024-145">コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="3b024-145">Undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="3b024-146">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-146">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable)</span></span>


### <a name="exttype"></a><span data-ttu-id="3b024-147">ExtType</span><span class="sxs-lookup"><span data-stu-id="3b024-147">ExtType</span></span>

<span data-ttu-id="3b024-148">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="3b024-148">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="3b024-149">拡張されたコントロール タイプです。</span><span class="sxs-lookup"><span data-stu-id="3b024-149">The extended control type.</span></span> <span data-ttu-id="3b024-150">E.g.</span><span class="sxs-lookup"><span data-stu-id="3b024-150">E.g.</span></span> <span data-ttu-id="3b024-151">コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b024-151">a control of type Input might have an extended type of Barcode.</span></span>

> <span data-ttu-id="3b024-152">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-152">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype)</span></span>


### <a name="helptext"></a><span data-ttu-id="3b024-153">HelpText</span><span class="sxs-lookup"><span data-stu-id="3b024-153">HelpText</span></span>

<span data-ttu-id="3b024-154">HelpText: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-154">HelpText: string (optional)</span></span> 

<span data-ttu-id="3b024-155">コマンドのキーボード ショートカットです。</span><span class="sxs-lookup"><span data-stu-id="3b024-155">The keyboard shortcut for a command.</span></span> <span data-ttu-id="3b024-156">E.g.</span><span class="sxs-lookup"><span data-stu-id="3b024-156">E.g.</span></span> <span data-ttu-id="3b024-157">「(Shift + F5)」</span><span class="sxs-lookup"><span data-stu-id="3b024-157">"(Shift+F5)"</span></span>

> <span data-ttu-id="3b024-158">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-158">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext)</span></span>


### <a name="hidden"></a><span data-ttu-id="3b024-159">非表示</span><span class="sxs-lookup"><span data-stu-id="3b024-159">Hidden</span></span>

<span data-ttu-id="3b024-160">非表示: ブール値 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-160">Hidden: boolean (optional)</span></span> 

<span data-ttu-id="3b024-161">コントロールを非表示にするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3b024-161">Boolean indicating if the control is hidden or not.</span></span>

> <span data-ttu-id="3b024-162">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-162">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden)</span></span>


### <a name="id"></a><span data-ttu-id="3b024-163">ID</span><span class="sxs-lookup"><span data-stu-id="3b024-163">Id</span></span>

<span data-ttu-id="3b024-164">Id: string (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-164">Id: string (optional)</span></span> 

<span data-ttu-id="3b024-165">コントロールの ID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="3b024-165">Identification string for a control.</span></span>

> <span data-ttu-id="3b024-166">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-166">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id)</span></span>


### <a name="label"></a><span data-ttu-id="3b024-167">ラベル</span><span class="sxs-lookup"><span data-stu-id="3b024-167">Label</span></span>

<span data-ttu-id="3b024-168">ラベル: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="3b024-168">Label: string (optional)</span></span> 

<span data-ttu-id="3b024-169">コントロールのラベル。</span><span class="sxs-lookup"><span data-stu-id="3b024-169">Label for a control.</span></span> <span data-ttu-id="3b024-170">E.g.</span><span class="sxs-lookup"><span data-stu-id="3b024-170">E.g.</span></span> <span data-ttu-id="3b024-171">個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b024-171">a control representing a person's first name might have a label "First Name".</span></span>

> <span data-ttu-id="3b024-172">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-172">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label)</span></span>


### <a name="name"></a><span data-ttu-id="3b024-173">氏名</span><span class="sxs-lookup"><span data-stu-id="3b024-173">Name</span></span>

<span data-ttu-id="3b024-174">Name: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="3b024-174">Name: string (optional)</span></span> 

<span data-ttu-id="3b024-175">コントロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="3b024-175">Name of a control.</span></span>

> <span data-ttu-id="3b024-176">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-176">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name)</span></span>


### <a name="order"></a><span data-ttu-id="3b024-177">注文</span><span class="sxs-lookup"><span data-stu-id="3b024-177">Order</span></span>

<span data-ttu-id="3b024-178">注文: 番号 (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-178">Order: number (optional)</span></span> 

<span data-ttu-id="3b024-179">コントロールがページに表示される順序を示す番号。</span><span class="sxs-lookup"><span data-stu-id="3b024-179">Number indicating the order in which a control will appear on a page.</span></span>

> <span data-ttu-id="3b024-180">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-180">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order)</span></span>


### <a name="target"></a><span data-ttu-id="3b024-181">ターゲット</span><span class="sxs-lookup"><span data-stu-id="3b024-181">Target</span></span>

<span data-ttu-id="3b024-182">ターゲット: [PageTarget](view-model-ipage-ipagetarget.md) (オプション)</span><span class="sxs-lookup"><span data-stu-id="3b024-182">Target: [PageTarget](view-model-ipage-ipagetarget.md) (optional)</span></span> 

<span data-ttu-id="3b024-183">パーツのターゲット ページ。</span><span class="sxs-lookup"><span data-stu-id="3b024-183">Target page of the part.</span></span>


### <a name="type"></a><span data-ttu-id="3b024-184">種類</span><span class="sxs-lookup"><span data-stu-id="3b024-184">Type</span></span>

<span data-ttu-id="3b024-185">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="3b024-185">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="3b024-186">コントロール タイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="3b024-186">String indicating the control type.</span></span>

> <span data-ttu-id="3b024-187">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承</span><span class="sxs-lookup"><span data-stu-id="3b024-187">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)</span></span>



