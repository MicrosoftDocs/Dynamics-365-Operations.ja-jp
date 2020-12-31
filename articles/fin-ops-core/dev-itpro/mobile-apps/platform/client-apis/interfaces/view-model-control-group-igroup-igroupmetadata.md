---
title: GroupMetadata タイプ
description: グループ メタデータ タイプ。
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
ms.openlocfilehash: 1e2ecbfb0961c11a3f9df73722e245dd49e1d276
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685011"
---
# <a name="groupmetadata-type"></a><span data-ttu-id="d6d75-103">GroupMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="d6d75-103">GroupMetadata type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="d6d75-104">グループ メタデータ タイプ。</span><span class="sxs-lookup"><span data-stu-id="d6d75-104">Group metadata type.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="d6d75-105">階層</span><span class="sxs-lookup"><span data-stu-id="d6d75-105">Hierarchy</span></span>

[<span data-ttu-id="d6d75-106">ContainerControlMetadata</span><span class="sxs-lookup"><span data-stu-id="d6d75-106">ContainerControlMetadata</span></span>](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br><span data-ttu-id="d6d75-107">&nbsp;&nbsp;&nbsp;└─ GroupMetadata</span><span class="sxs-lookup"><span data-stu-id="d6d75-107">&nbsp;&nbsp;&nbsp;└─ GroupMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="d6d75-108">指数</span><span class="sxs-lookup"><span data-stu-id="d6d75-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="d6d75-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d6d75-109">Properties</span></span>

* [<span data-ttu-id="d6d75-110">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="d6d75-110">BoundEntity</span></span>](view-model-control-group-igroup-igroupmetadata.md#boundentity)
* [<span data-ttu-id="d6d75-111">BoundField</span><span class="sxs-lookup"><span data-stu-id="d6d75-111">BoundField</span></span>](view-model-control-group-igroup-igroupmetadata.md#boundfield)
* [<span data-ttu-id="d6d75-112">子</span><span class="sxs-lookup"><span data-stu-id="d6d75-112">Children</span></span>](view-model-control-group-igroup-igroupmetadata.md#children)
* [<span data-ttu-id="d6d75-113">説明</span><span class="sxs-lookup"><span data-stu-id="d6d75-113">Description</span></span>](view-model-control-group-igroup-igroupmetadata.md#description)
* [<span data-ttu-id="d6d75-114">編集可能</span><span class="sxs-lookup"><span data-stu-id="d6d75-114">Editable</span></span>](view-model-control-group-igroup-igroupmetadata.md#editable)
* [<span data-ttu-id="d6d75-115">ExtType</span><span class="sxs-lookup"><span data-stu-id="d6d75-115">ExtType</span></span>](view-model-control-group-igroup-igroupmetadata.md#exttype)
* [<span data-ttu-id="d6d75-116">HelpText</span><span class="sxs-lookup"><span data-stu-id="d6d75-116">HelpText</span></span>](view-model-control-group-igroup-igroupmetadata.md#helptext)
* [<span data-ttu-id="d6d75-117">非表示</span><span class="sxs-lookup"><span data-stu-id="d6d75-117">Hidden</span></span>](view-model-control-group-igroup-igroupmetadata.md#hidden)
* [<span data-ttu-id="d6d75-118">ID</span><span class="sxs-lookup"><span data-stu-id="d6d75-118">Id</span></span>](view-model-control-group-igroup-igroupmetadata.md#id)
* [<span data-ttu-id="d6d75-119">ラベル</span><span class="sxs-lookup"><span data-stu-id="d6d75-119">Label</span></span>](view-model-control-group-igroup-igroupmetadata.md#label)
* [<span data-ttu-id="d6d75-120">名前</span><span class="sxs-lookup"><span data-stu-id="d6d75-120">Name</span></span>](view-model-control-group-igroup-igroupmetadata.md#name)
* [<span data-ttu-id="d6d75-121">注文</span><span class="sxs-lookup"><span data-stu-id="d6d75-121">Order</span></span>](view-model-control-group-igroup-igroupmetadata.md#order)
* <span data-ttu-id="d6d75-122">[[タイプ](view-model-control-group-igroup-igroupmetadata.md#type)]</span><span class="sxs-lookup"><span data-stu-id="d6d75-122">[Type](view-model-control-group-igroup-igroupmetadata.md#type)</span></span>

## <a name="properties"></a><span data-ttu-id="d6d75-123">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d6d75-123">Properties</span></span>

### <a name="boundentity"></a><span data-ttu-id="d6d75-124">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="d6d75-124">BoundEntity</span></span>

<span data-ttu-id="d6d75-125">BoundEntity: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-125">BoundEntity: string (optional)</span></span> 

<span data-ttu-id="d6d75-126">コントロールがバインドされるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="d6d75-126">The entity to which the control is bound.</span></span>

> <span data-ttu-id="d6d75-127">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-127">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity)</span></span>


### <a name="boundfield"></a><span data-ttu-id="d6d75-128">BoundField</span><span class="sxs-lookup"><span data-stu-id="d6d75-128">BoundField</span></span>

<span data-ttu-id="d6d75-129">BoundField: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-129">BoundField: string (optional)</span></span> 



> <span data-ttu-id="d6d75-130">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-130">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield)</span></span>


### <a name="children"></a><span data-ttu-id="d6d75-131">子</span><span class="sxs-lookup"><span data-stu-id="d6d75-131">Children</span></span>

<span data-ttu-id="d6d75-132">子: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) \[ \] (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-132">Children: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) \[ \] (optional)</span></span> 

<span data-ttu-id="d6d75-133">各子コントロールの管理メタデータのリスト。</span><span class="sxs-lookup"><span data-stu-id="d6d75-133">List of control metadata for each child control.</span></span>


### <a name="description"></a><span data-ttu-id="d6d75-134">説明</span><span class="sxs-lookup"><span data-stu-id="d6d75-134">Description</span></span>

<span data-ttu-id="d6d75-135">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-135">Description: string (optional)</span></span> 

<span data-ttu-id="d6d75-136">コントロールの説明。</span><span class="sxs-lookup"><span data-stu-id="d6d75-136">Description of the control.</span></span>

> <span data-ttu-id="d6d75-137">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-137">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description)</span></span>


### <a name="editable"></a><span data-ttu-id="d6d75-138">編集可能</span><span class="sxs-lookup"><span data-stu-id="d6d75-138">Editable</span></span>

<span data-ttu-id="d6d75-139">編集可能: プール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="d6d75-139">Editable: boolean (optional)</span></span> 

<span data-ttu-id="d6d75-140">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d6d75-140">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="d6d75-141">コントロールまたはその親が編集可能でない場合は、False です。</span><span class="sxs-lookup"><span data-stu-id="d6d75-141">False when either the control or its parent is not editable.</span></span>
<span data-ttu-id="d6d75-142">コントロールとその親の両方が編集可能な場合、true です。</span><span class="sxs-lookup"><span data-stu-id="d6d75-142">True when both the control and its parent are editable.</span></span>
<span data-ttu-id="d6d75-143">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="d6d75-143">True when either the control or its parent is editable and the other is undefined.</span></span>
<span data-ttu-id="d6d75-144">コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="d6d75-144">Undefined if both the control's edit-ability and its parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="d6d75-145">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-145">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable)</span></span>


### <a name="exttype"></a><span data-ttu-id="d6d75-146">ExtType</span><span class="sxs-lookup"><span data-stu-id="d6d75-146">ExtType</span></span>

<span data-ttu-id="d6d75-147">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="d6d75-147">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="d6d75-148">拡張されたコントロール タイプです。</span><span class="sxs-lookup"><span data-stu-id="d6d75-148">The extended control type.</span></span> <span data-ttu-id="d6d75-149">たとえば、コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d6d75-149">For example, a control of type Input might have an extended type of Barcode.</span></span>

> <span data-ttu-id="d6d75-150">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-150">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype)</span></span>


### <a name="helptext"></a><span data-ttu-id="d6d75-151">HelpText</span><span class="sxs-lookup"><span data-stu-id="d6d75-151">HelpText</span></span>

<span data-ttu-id="d6d75-152">HelpText: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-152">HelpText: string (optional)</span></span> 

<span data-ttu-id="d6d75-153">コマンドのキーボード ショートカットです。</span><span class="sxs-lookup"><span data-stu-id="d6d75-153">The keyboard shortcut for a command.</span></span> <span data-ttu-id="d6d75-154">たとえば、「(Shift + F5)」</span><span class="sxs-lookup"><span data-stu-id="d6d75-154">For example, "(Shift+F5)"</span></span>

> <span data-ttu-id="d6d75-155">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-155">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext)</span></span>


### <a name="hidden"></a><span data-ttu-id="d6d75-156">非表示</span><span class="sxs-lookup"><span data-stu-id="d6d75-156">Hidden</span></span>

<span data-ttu-id="d6d75-157">非表示: ブール値 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-157">Hidden: boolean (optional)</span></span> 

<span data-ttu-id="d6d75-158">コントロールを非表示にするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d6d75-158">Boolean indicating if the control is hidden or not.</span></span>

> <span data-ttu-id="d6d75-159">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-159">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden)</span></span>


### <a name="id"></a><span data-ttu-id="d6d75-160">ID</span><span class="sxs-lookup"><span data-stu-id="d6d75-160">Id</span></span>

<span data-ttu-id="d6d75-161">Id: string (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-161">Id: string (optional)</span></span> 

<span data-ttu-id="d6d75-162">コントロールの ID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="d6d75-162">Identification string for a control.</span></span>

> <span data-ttu-id="d6d75-163">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-163">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id)</span></span>


### <a name="label"></a><span data-ttu-id="d6d75-164">ラベル</span><span class="sxs-lookup"><span data-stu-id="d6d75-164">Label</span></span>

<span data-ttu-id="d6d75-165">ラベル: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="d6d75-165">Label: string (optional)</span></span> 

<span data-ttu-id="d6d75-166">コントロールのラベル。</span><span class="sxs-lookup"><span data-stu-id="d6d75-166">Label for a control.</span></span> <span data-ttu-id="d6d75-167">たとえば、個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d6d75-167">For example, a control representing a person's first name might have a label "First Name".</span></span>

> <span data-ttu-id="d6d75-168">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-168">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label)</span></span>


### <a name="name"></a><span data-ttu-id="d6d75-169">氏名</span><span class="sxs-lookup"><span data-stu-id="d6d75-169">Name</span></span>

<span data-ttu-id="d6d75-170">Name: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="d6d75-170">Name: string (optional)</span></span> 

<span data-ttu-id="d6d75-171">コントロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="d6d75-171">Name of a control.</span></span>

> <span data-ttu-id="d6d75-172">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-172">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name)</span></span>


### <a name="order"></a><span data-ttu-id="d6d75-173">注文</span><span class="sxs-lookup"><span data-stu-id="d6d75-173">Order</span></span>

<span data-ttu-id="d6d75-174">注文: 番号 (オプション)</span><span class="sxs-lookup"><span data-stu-id="d6d75-174">Order: number (optional)</span></span> 

<span data-ttu-id="d6d75-175">コントロールがページに表示される順序を示す番号。</span><span class="sxs-lookup"><span data-stu-id="d6d75-175">Number indicating the order in which a control will appear on a page.</span></span>

> <span data-ttu-id="d6d75-176">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-176">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order)</span></span>


### <a name="type"></a><span data-ttu-id="d6d75-177">種類</span><span class="sxs-lookup"><span data-stu-id="d6d75-177">Type</span></span>

<span data-ttu-id="d6d75-178">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="d6d75-178">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="d6d75-179">コントロール タイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="d6d75-179">String indicating the control type.</span></span>

> <span data-ttu-id="d6d75-180">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承</span><span class="sxs-lookup"><span data-stu-id="d6d75-180">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)</span></span>


