---
title: PartMetadata タイプ
description: パーツ メタデータ タイプ。
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
ms.openlocfilehash: 10df7c6257c228b39ba369b1e0dd354510cd007c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686622"
---
# <a name="partmetadata-type"></a><span data-ttu-id="34229-103">PartMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="34229-103">PartMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="34229-104">パーツ メタデータ タイプ。</span><span class="sxs-lookup"><span data-stu-id="34229-104">Part metadata type.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="34229-105">階層</span><span class="sxs-lookup"><span data-stu-id="34229-105">Hierarchy</span></span>

[<span data-ttu-id="34229-106">ContainerControlMetadata</span><span class="sxs-lookup"><span data-stu-id="34229-106">ContainerControlMetadata</span></span>](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br><span data-ttu-id="34229-107">&nbsp;&nbsp;&nbsp;└─ PartMetadata</span><span class="sxs-lookup"><span data-stu-id="34229-107">&nbsp;&nbsp;&nbsp;└─ PartMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="34229-108">指数</span><span class="sxs-lookup"><span data-stu-id="34229-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="34229-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="34229-109">Properties</span></span>

* [<span data-ttu-id="34229-110">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="34229-110">BoundEntity</span></span>](view-model-control-part-ipart-ipartmetadata.md#boundentity)
* [<span data-ttu-id="34229-111">BoundField</span><span class="sxs-lookup"><span data-stu-id="34229-111">BoundField</span></span>](view-model-control-part-ipart-ipartmetadata.md#boundfield)
* [<span data-ttu-id="34229-112">説明</span><span class="sxs-lookup"><span data-stu-id="34229-112">Description</span></span>](view-model-control-part-ipart-ipartmetadata.md#description)
* [<span data-ttu-id="34229-113">Design</span><span class="sxs-lookup"><span data-stu-id="34229-113">Design</span></span>](view-model-control-part-ipart-ipartmetadata.md#design)
* [<span data-ttu-id="34229-114">編集可能</span><span class="sxs-lookup"><span data-stu-id="34229-114">Editable</span></span>](view-model-control-part-ipart-ipartmetadata.md#editable)
* [<span data-ttu-id="34229-115">ExtType</span><span class="sxs-lookup"><span data-stu-id="34229-115">ExtType</span></span>](view-model-control-part-ipart-ipartmetadata.md#exttype)
* [<span data-ttu-id="34229-116">HelpText</span><span class="sxs-lookup"><span data-stu-id="34229-116">HelpText</span></span>](view-model-control-part-ipart-ipartmetadata.md#helptext)
* [<span data-ttu-id="34229-117">非表示</span><span class="sxs-lookup"><span data-stu-id="34229-117">Hidden</span></span>](view-model-control-part-ipart-ipartmetadata.md#hidden)
* [<span data-ttu-id="34229-118">ID</span><span class="sxs-lookup"><span data-stu-id="34229-118">Id</span></span>](view-model-control-part-ipart-ipartmetadata.md#id)
* [<span data-ttu-id="34229-119">ラベル</span><span class="sxs-lookup"><span data-stu-id="34229-119">Label</span></span>](view-model-control-part-ipart-ipartmetadata.md#label)
* [<span data-ttu-id="34229-120">名前</span><span class="sxs-lookup"><span data-stu-id="34229-120">Name</span></span>](view-model-control-part-ipart-ipartmetadata.md#name)
* [<span data-ttu-id="34229-121">注文</span><span class="sxs-lookup"><span data-stu-id="34229-121">Order</span></span>](view-model-control-part-ipart-ipartmetadata.md#order)
* [<span data-ttu-id="34229-122">ターゲット</span><span class="sxs-lookup"><span data-stu-id="34229-122">Target</span></span>](view-model-control-part-ipart-ipartmetadata.md#target)
* <span data-ttu-id="34229-123">[[タイプ](view-model-control-part-ipart-ipartmetadata.md#type)]</span><span class="sxs-lookup"><span data-stu-id="34229-123">[Type](view-model-control-part-ipart-ipartmetadata.md#type)</span></span>

## <a name="properties"></a><span data-ttu-id="34229-124">プロパティ</span><span class="sxs-lookup"><span data-stu-id="34229-124">Properties</span></span>

### <a name="boundentity"></a><span data-ttu-id="34229-125">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="34229-125">BoundEntity</span></span>

<span data-ttu-id="34229-126">BoundEntity: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-126">BoundEntity: string (optional)</span></span> 

<span data-ttu-id="34229-127">コントロールがバインドされるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="34229-127">The entity to which the control is bound.</span></span>

> <span data-ttu-id="34229-128">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-128">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity)</span></span>


### <a name="boundfield"></a><span data-ttu-id="34229-129">BoundField</span><span class="sxs-lookup"><span data-stu-id="34229-129">BoundField</span></span>

<span data-ttu-id="34229-130">BoundField: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-130">BoundField: string (optional)</span></span> 



> <span data-ttu-id="34229-131">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-131">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield)</span></span>


### <a name="description"></a><span data-ttu-id="34229-132">説明</span><span class="sxs-lookup"><span data-stu-id="34229-132">Description</span></span>

<span data-ttu-id="34229-133">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-133">Description: string (optional)</span></span> 

<span data-ttu-id="34229-134">コントロールの説明。</span><span class="sxs-lookup"><span data-stu-id="34229-134">Description of the control.</span></span>

> <span data-ttu-id="34229-135">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-135">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description)</span></span>


### <a name="design"></a><span data-ttu-id="34229-136">デザイン</span><span class="sxs-lookup"><span data-stu-id="34229-136">Design</span></span>

<span data-ttu-id="34229-137">デザイン: [PartDesign](view-model-control-part-ipart-ipartdesign.md) (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-137">Design: [PartDesign](view-model-control-part-ipart-ipartdesign.md) (optional)</span></span> 

<span data-ttu-id="34229-138">ターゲット ページの設計をします。</span><span class="sxs-lookup"><span data-stu-id="34229-138">Design for the target page.</span></span>


### <a name="editable"></a><span data-ttu-id="34229-139">編集可能</span><span class="sxs-lookup"><span data-stu-id="34229-139">Editable</span></span>

<span data-ttu-id="34229-140">編集可能: プール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="34229-140">Editable: boolean (optional)</span></span> 

<span data-ttu-id="34229-141">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="34229-141">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="34229-142">コントロールまたはその親が編集可能でない場合は、False です。</span><span class="sxs-lookup"><span data-stu-id="34229-142">False when either the control or its parent is not editable.</span></span>
<span data-ttu-id="34229-143">コントロールとその親の両方が編集可能な場合、true です。</span><span class="sxs-lookup"><span data-stu-id="34229-143">True when both the control and its parent are editable.</span></span>
<span data-ttu-id="34229-144">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="34229-144">True when either the control or its parent is editable and the other is undefined.</span></span>
<span data-ttu-id="34229-145">コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="34229-145">Undefined if both the control's edit-ability and its parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="34229-146">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-146">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable)</span></span>


### <a name="exttype"></a><span data-ttu-id="34229-147">ExtType</span><span class="sxs-lookup"><span data-stu-id="34229-147">ExtType</span></span>

<span data-ttu-id="34229-148">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="34229-148">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="34229-149">拡張されたコントロール タイプです。</span><span class="sxs-lookup"><span data-stu-id="34229-149">The extended control type.</span></span> <span data-ttu-id="34229-150">たとえば、コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="34229-150">For example, a control of type Input might have an extended type of Barcode.</span></span>

> <span data-ttu-id="34229-151">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-151">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype)</span></span>


### <a name="helptext"></a><span data-ttu-id="34229-152">HelpText</span><span class="sxs-lookup"><span data-stu-id="34229-152">HelpText</span></span>

<span data-ttu-id="34229-153">HelpText: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-153">HelpText: string (optional)</span></span> 

<span data-ttu-id="34229-154">コマンドのキーボード ショートカットです。</span><span class="sxs-lookup"><span data-stu-id="34229-154">The keyboard shortcut for a command.</span></span> <span data-ttu-id="34229-155">たとえば、「(Shift + F5)」</span><span class="sxs-lookup"><span data-stu-id="34229-155">For example, "(Shift+F5)"</span></span>

> <span data-ttu-id="34229-156">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-156">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext)</span></span>


### <a name="hidden"></a><span data-ttu-id="34229-157">非表示</span><span class="sxs-lookup"><span data-stu-id="34229-157">Hidden</span></span>

<span data-ttu-id="34229-158">非表示: ブール値 (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-158">Hidden: boolean (optional)</span></span> 

<span data-ttu-id="34229-159">コントロールを非表示にするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="34229-159">Boolean indicating if the control is hidden or not.</span></span>

> <span data-ttu-id="34229-160">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-160">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden)</span></span>


### <a name="id"></a><span data-ttu-id="34229-161">ID</span><span class="sxs-lookup"><span data-stu-id="34229-161">Id</span></span>

<span data-ttu-id="34229-162">Id: string (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-162">Id: string (optional)</span></span> 

<span data-ttu-id="34229-163">コントロールの ID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="34229-163">Identification string for a control.</span></span>

> <span data-ttu-id="34229-164">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-164">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id)</span></span>


### <a name="label"></a><span data-ttu-id="34229-165">ラベル</span><span class="sxs-lookup"><span data-stu-id="34229-165">Label</span></span>

<span data-ttu-id="34229-166">ラベル: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="34229-166">Label: string (optional)</span></span> 

<span data-ttu-id="34229-167">コントロールのラベル。</span><span class="sxs-lookup"><span data-stu-id="34229-167">Label for a control.</span></span> <span data-ttu-id="34229-168">たとえば、個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。</span><span class="sxs-lookup"><span data-stu-id="34229-168">For example, a control representing a person's first name might have a label "First Name".</span></span>

> <span data-ttu-id="34229-169">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-169">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label)</span></span>


### <a name="name"></a><span data-ttu-id="34229-170">氏名</span><span class="sxs-lookup"><span data-stu-id="34229-170">Name</span></span>

<span data-ttu-id="34229-171">Name: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="34229-171">Name: string (optional)</span></span> 

<span data-ttu-id="34229-172">コントロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="34229-172">Name of a control.</span></span>

> <span data-ttu-id="34229-173">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-173">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name)</span></span>


### <a name="order"></a><span data-ttu-id="34229-174">注文</span><span class="sxs-lookup"><span data-stu-id="34229-174">Order</span></span>

<span data-ttu-id="34229-175">注文: 番号 (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-175">Order: number (optional)</span></span> 

<span data-ttu-id="34229-176">コントロールがページに表示される順序を示す番号。</span><span class="sxs-lookup"><span data-stu-id="34229-176">Number indicating the order in which a control will appear on a page.</span></span>

> <span data-ttu-id="34229-177">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-177">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order)</span></span>


### <a name="target"></a><span data-ttu-id="34229-178">ターゲット</span><span class="sxs-lookup"><span data-stu-id="34229-178">Target</span></span>

<span data-ttu-id="34229-179">ターゲット: [PageTarget](view-model-ipage-ipagetarget.md) (オプション)</span><span class="sxs-lookup"><span data-stu-id="34229-179">Target: [PageTarget](view-model-ipage-ipagetarget.md) (optional)</span></span> 

<span data-ttu-id="34229-180">パーツのターゲット ページ。</span><span class="sxs-lookup"><span data-stu-id="34229-180">Target page of the part.</span></span>


### <a name="type"></a><span data-ttu-id="34229-181">種類</span><span class="sxs-lookup"><span data-stu-id="34229-181">Type</span></span>

<span data-ttu-id="34229-182">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="34229-182">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="34229-183">コントロール タイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="34229-183">String indicating the control type.</span></span>

> <span data-ttu-id="34229-184">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承</span><span class="sxs-lookup"><span data-stu-id="34229-184">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)</span></span>


