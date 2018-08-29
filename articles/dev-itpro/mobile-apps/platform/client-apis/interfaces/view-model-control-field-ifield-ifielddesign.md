---
title: "FieldDesign タイプ"
description: "フィールド コントロール用のデザイン オブジェクト インターフェイス。"
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
ms.sourcegitcommit: ed6cabcc8c76fba3d4414cd4b564b720c54169e0
ms.openlocfilehash: 68f505ea6d5a2a543d41ce3a6fa6840a61d2359f
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="fielddesign-type"></a><span data-ttu-id="704dc-103">FieldDesign タイプ</span><span class="sxs-lookup"><span data-stu-id="704dc-103">FieldDesign type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="704dc-104">フィールド コントロール用のデザイン オブジェクト インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="704dc-104">Design object interface for a field control.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="704dc-105">階層</span><span class="sxs-lookup"><span data-stu-id="704dc-105">Hierarchy</span></span>

[<span data-ttu-id="704dc-106">InputControlDesign</span><span class="sxs-lookup"><span data-stu-id="704dc-106">InputControlDesign</span></span>](view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md) <br><span data-ttu-id="704dc-107">&nbsp;&nbsp;&nbsp;└─ FieldDesign</span><span class="sxs-lookup"><span data-stu-id="704dc-107">&nbsp;&nbsp;&nbsp;└─ FieldDesign</span></span> <br>

## <a name="index"></a><span data-ttu-id="704dc-108">指数</span><span class="sxs-lookup"><span data-stu-id="704dc-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="704dc-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="704dc-109">Properties</span></span>

* [<span data-ttu-id="704dc-110">alignItems</span><span class="sxs-lookup"><span data-stu-id="704dc-110">alignItems</span></span>](view-model-control-field-ifield-ifielddesign.md#alignitems)
* [<span data-ttu-id="704dc-111">alignSelf</span><span class="sxs-lookup"><span data-stu-id="704dc-111">alignSelf</span></span>](view-model-control-field-ifield-ifielddesign.md#alignself)
* [<span data-ttu-id="704dc-112">バインディング</span><span class="sxs-lookup"><span data-stu-id="704dc-112">bindings</span></span>](view-model-control-field-ifield-ifielddesign.md#bindings)
* [<span data-ttu-id="704dc-113">枠線</span><span class="sxs-lookup"><span data-stu-id="704dc-113">border</span></span>](view-model-control-field-ifield-ifielddesign.md#border)
* [<span data-ttu-id="704dc-114">色</span><span class="sxs-lookup"><span data-stu-id="704dc-114">color</span></span>](view-model-control-field-ifield-ifielddesign.md#color)
* [<span data-ttu-id="704dc-115">flexFlow</span><span class="sxs-lookup"><span data-stu-id="704dc-115">flexFlow</span></span>](view-model-control-field-ifield-ifielddesign.md#flexflow)
* [<span data-ttu-id="704dc-116">flexSize</span><span class="sxs-lookup"><span data-stu-id="704dc-116">flexSize</span></span>](view-model-control-field-ifield-ifielddesign.md#flexsize)
* [<span data-ttu-id="704dc-117">fontSize</span><span class="sxs-lookup"><span data-stu-id="704dc-117">fontSize</span></span>](view-model-control-field-ifield-ifielddesign.md#fontsize)
* [<span data-ttu-id="704dc-118">fontWeight</span><span class="sxs-lookup"><span data-stu-id="704dc-118">fontWeight</span></span>](view-model-control-field-ifield-ifielddesign.md#fontweight)
* [<span data-ttu-id="704dc-119">justifyItems</span><span class="sxs-lookup"><span data-stu-id="704dc-119">justifyItems</span></span>](view-model-control-field-ifield-ifielddesign.md#justifyitems)
* [<span data-ttu-id="704dc-120">ラベル</span><span class="sxs-lookup"><span data-stu-id="704dc-120">label</span></span>](view-model-control-field-ifield-ifielddesign.md#label)
* [<span data-ttu-id="704dc-121">labelPosition</span><span class="sxs-lookup"><span data-stu-id="704dc-121">labelPosition</span></span>](view-model-control-field-ifield-ifielddesign.md#labelposition)
* [<span data-ttu-id="704dc-122">名前</span><span class="sxs-lookup"><span data-stu-id="704dc-122">name</span></span>](view-model-control-field-ifield-ifielddesign.md#name)
* [<span data-ttu-id="704dc-123">スペース</span><span class="sxs-lookup"><span data-stu-id="704dc-123">padding</span></span>](view-model-control-field-ifield-ifielddesign.md#padding)
* [<span data-ttu-id="704dc-124">タイプ</span><span class="sxs-lookup"><span data-stu-id="704dc-124">type</span></span>](view-model-control-field-ifield-ifielddesign.md#type)

## <a name="properties"></a><span data-ttu-id="704dc-125">プロパティ</span><span class="sxs-lookup"><span data-stu-id="704dc-125">Properties</span></span>

### <a name="alignitems"></a><span data-ttu-id="704dc-126">alignItems</span><span class="sxs-lookup"><span data-stu-id="704dc-126">alignItems</span></span>

<span data-ttu-id="704dc-127">alignItems: string (optional)</span><span class="sxs-lookup"><span data-stu-id="704dc-127">alignItems: string (optional)</span></span> 

<span data-ttu-id="704dc-128">このプロパティは、CSS プロパティ「align-items」のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="704dc-128">This property is an alias for the CSS property "align-items".</span></span>
<span data-ttu-id="704dc-129">"align-items" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="704dc-129">Please refer to [this web page](https://css-tricks.com/snippets/css/a-guide-to-flexbox) for documentation on the "align-items" property.</span></span>

> <span data-ttu-id="704dc-130">[Design](view-model-ipage-idesign.md).[alignItems](view-model-ipage-idesign.md#alignitems) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-130">Inherited from [Design](view-model-ipage-idesign.md).[alignItems](view-model-ipage-idesign.md#alignitems)</span></span>


### <a name="alignself"></a><span data-ttu-id="704dc-131">alignSelf</span><span class="sxs-lookup"><span data-stu-id="704dc-131">alignSelf</span></span>

<span data-ttu-id="704dc-132">alignSelf: string (optional)</span><span class="sxs-lookup"><span data-stu-id="704dc-132">alignSelf: string (optional)</span></span> 



> <span data-ttu-id="704dc-133">[Design](view-model-ipage-idesign.md).[alignSelf](view-model-ipage-idesign.md#alignself) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-133">Inherited from [Design](view-model-ipage-idesign.md).[alignSelf](view-model-ipage-idesign.md#alignself)</span></span>


### <a name="bindings"></a><span data-ttu-id="704dc-134">bindings</span><span class="sxs-lookup"><span data-stu-id="704dc-134">bindings</span></span>

<span data-ttu-id="704dc-135">bindings: any (optional)</span><span class="sxs-lookup"><span data-stu-id="704dc-135">bindings: any (optional)</span></span> 



> <span data-ttu-id="704dc-136">[Design](view-model-ipage-idesign.md).[bindings](view-model-ipage-idesign.md#bindings) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-136">Inherited from [Design](view-model-ipage-idesign.md).[bindings](view-model-ipage-idesign.md#bindings)</span></span>


### <a name="border"></a><span data-ttu-id="704dc-137">border</span><span class="sxs-lookup"><span data-stu-id="704dc-137">border</span></span>

<span data-ttu-id="704dc-138">border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (optional)</span><span class="sxs-lookup"><span data-stu-id="704dc-138">border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (optional)</span></span> 

<span data-ttu-id="704dc-139">コントロールの境界動作。</span><span class="sxs-lookup"><span data-stu-id="704dc-139">The border behavior of a control.</span></span> <span data-ttu-id="704dc-140">このプロパティは、子によって継承されません。</span><span class="sxs-lookup"><span data-stu-id="704dc-140">This property will not be inherited by the children.</span></span>

> <span data-ttu-id="704dc-141">[Design](view-model-ipage-idesign.md).[border](view-model-ipage-idesign.md#border) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-141">Inherited from [Design](view-model-ipage-idesign.md).[border](view-model-ipage-idesign.md#border)</span></span>


### <a name="color"></a><span data-ttu-id="704dc-142">色</span><span class="sxs-lookup"><span data-stu-id="704dc-142">color</span></span>

<span data-ttu-id="704dc-143">color: string (optional)</span><span class="sxs-lookup"><span data-stu-id="704dc-143">color: string (optional)</span></span> 

<span data-ttu-id="704dc-144">コンテナーの前景色。</span><span class="sxs-lookup"><span data-stu-id="704dc-144">The foreground color of the container.</span></span>
<span data-ttu-id="704dc-145">これにより、コンテナ内のすべてのヘッダー、アイテム、ラベル、アイコンの色が変更されます。</span><span class="sxs-lookup"><span data-stu-id="704dc-145">This will modify the color of all headers, items, labels, and icons within the container.</span></span><br>
<span data-ttu-id="704dc-146">この属性を設定するときは、必要に応じて背景色を同時に設定することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="704dc-146">Consider setting the background color at the same time as necessary when setting this attribute.</span></span><br>
<span data-ttu-id="704dc-147">注記: 色が「テーマ」に設定されている場合、アプリケーションのテーマ色が使用されます。</span><span class="sxs-lookup"><span data-stu-id="704dc-147">Note: if color is set to "theme", the theme color of the app will be used.</span></span><br>
<span data-ttu-id="704dc-148">使用可能な色は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="704dc-148">The following colors are available:</span></span> <br>
<span data-ttu-id="704dc-149">![サンプル画像](../../../media/colors.PNG)</span><span class="sxs-lookup"><span data-stu-id="704dc-149">![sample image](../../../media/colors.PNG)</span></span>

> <span data-ttu-id="704dc-150">[Design](view-model-ipage-idesign.md).[color](view-model-ipage-idesign.md#color) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-150">Inherited from [Design](view-model-ipage-idesign.md).[color](view-model-ipage-idesign.md#color)</span></span>


### <a name="flexflow"></a><span data-ttu-id="704dc-151">flexFlow</span><span class="sxs-lookup"><span data-stu-id="704dc-151">flexFlow</span></span>

<span data-ttu-id="704dc-152">flexFlow: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-152">flexFlow: string (optional)</span></span> 

<span data-ttu-id="704dc-153">このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。</span><span class="sxs-lookup"><span data-stu-id="704dc-153">Specifying this property makes the component a flex container component.</span></span>
<span data-ttu-id="704dc-154">このプロパティは、CSS プロパティ「flex-flow」のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="704dc-154">This property is an alias for the CSS property "flex-flow".</span></span>
<span data-ttu-id="704dc-155">"flex-flow" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="704dc-155">Please refer to [this web page](https://css-tricks.com/snippets/css/a-guide-to-flexbox) for documentation on the "flex-flow" property.</span></span>

> <span data-ttu-id="704dc-156">[Design](view-model-ipage-idesign.md).[flexFlow](view-model-ipage-idesign.md#flexflow) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-156">Inherited from [Design](view-model-ipage-idesign.md).[flexFlow](view-model-ipage-idesign.md#flexflow)</span></span>


### <a name="flexsize"></a><span data-ttu-id="704dc-157">flexSize</span><span class="sxs-lookup"><span data-stu-id="704dc-157">flexSize</span></span>

<span data-ttu-id="704dc-158">flexSize: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-158">flexSize: string (optional)</span></span> 

<span data-ttu-id="704dc-159">1 つの番号または 2 つの番号が文字列として書き込まれています。</span><span class="sxs-lookup"><span data-stu-id="704dc-159">One number or two numbers written as a string.</span></span> <span data-ttu-id="704dc-160">E.g.</span><span class="sxs-lookup"><span data-stu-id="704dc-160">E.g.</span></span> <span data-ttu-id="704dc-161">「(サイズを拡大) [(サイズの縮小)]」して、即時フレックス コンテナの使用可能領域に対応します。</span><span class="sxs-lookup"><span data-stu-id="704dc-161">"(size to grow) [(size-to-shrink)]" to accommodate available space in the immediate flex container.</span></span>
<span data-ttu-id="704dc-162">このプロパティは、CSS プロパティ「flex」のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="704dc-162">This property is an alias for the CSS property "flex".</span></span> <span data-ttu-id="704dc-163">"flex" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="704dc-163">Please refer to [this web page](https://css-tricks.com/snippets/css/a-guide-to-flexbox) for documentation on the "flex" property.</span></span>

> <span data-ttu-id="704dc-164">[Design](view-model-ipage-idesign.md).[flexSize](view-model-ipage-idesign.md#flexsize) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-164">Inherited from [Design](view-model-ipage-idesign.md).[flexSize](view-model-ipage-idesign.md#flexsize)</span></span>


### <a name="fontsize"></a><span data-ttu-id="704dc-165">fontSize</span><span class="sxs-lookup"><span data-stu-id="704dc-165">fontSize</span></span>

<span data-ttu-id="704dc-166">fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-166">fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (optional)</span></span> 

<span data-ttu-id="704dc-167">比例テキスト サイズ</span><span class="sxs-lookup"><span data-stu-id="704dc-167">The proportional text size</span></span>

> <span data-ttu-id="704dc-168">[Design](view-model-ipage-idesign.md).[fontSize](view-model-ipage-idesign.md#fontsize) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-168">Inherited from [Design](view-model-ipage-idesign.md).[fontSize](view-model-ipage-idesign.md#fontsize)</span></span>


### <a name="fontweight"></a><span data-ttu-id="704dc-169">fontWeight</span><span class="sxs-lookup"><span data-stu-id="704dc-169">fontWeight</span></span>

<span data-ttu-id="704dc-170">fontWeight: "normal" &#124; "bold" (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-170">fontWeight: "normal" &#124; "bold" (optional)</span></span> 

<span data-ttu-id="704dc-171">標準または太字のテキスト。</span><span class="sxs-lookup"><span data-stu-id="704dc-171">Normal or bold text.</span></span>

> <span data-ttu-id="704dc-172">[Design](view-model-ipage-idesign.md).[fontWeight](view-model-ipage-idesign.md#fontweight) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-172">Inherited from [Design](view-model-ipage-idesign.md).[fontWeight](view-model-ipage-idesign.md#fontweight)</span></span>


### <a name="justifyitems"></a><span data-ttu-id="704dc-173">justifyItems</span><span class="sxs-lookup"><span data-stu-id="704dc-173">justifyItems</span></span>

<span data-ttu-id="704dc-174">justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-174">justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (optional)</span></span> 

<span data-ttu-id="704dc-175">このプロパティは CSS プロパティ「justify-content」のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="704dc-175">This property is an alias for the CSS property "justify-content".</span></span>
<span data-ttu-id="704dc-176">"justify-content" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="704dc-176">Please refer to [this web page](https://css-tricks.com/snippets/css/a-guide-to-flexbox) for documentation on the "justify-content" property.</span></span>

> <span data-ttu-id="704dc-177">[Design](view-model-ipage-idesign.md).[justifyItems](view-model-ipage-idesign.md#justifyitems) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-177">Inherited from [Design](view-model-ipage-idesign.md).[justifyItems](view-model-ipage-idesign.md#justifyitems)</span></span>


### <a name="label"></a><span data-ttu-id="704dc-178">ラベル</span><span class="sxs-lookup"><span data-stu-id="704dc-178">label</span></span>

<span data-ttu-id="704dc-179">label: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-179">label: string (optional)</span></span> 



> <span data-ttu-id="704dc-180">[Design](view-model-ipage-idesign.md).[label](view-model-ipage-idesign.md#label) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-180">Inherited from [Design](view-model-ipage-idesign.md).[label](view-model-ipage-idesign.md#label)</span></span>


### <a name="labelposition"></a><span data-ttu-id="704dc-181">labelPosition</span><span class="sxs-lookup"><span data-stu-id="704dc-181">labelPosition</span></span>

<span data-ttu-id="704dc-182">labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-182">labelPosition: "stacked" &#124; "hidden" &#124; "inline" (optional)</span></span> 

<span data-ttu-id="704dc-183">ラベルの配置方法を決定します (行われる場合)。</span><span class="sxs-lookup"><span data-stu-id="704dc-183">Determines how a label is positioned, if at all.</span></span> <span data-ttu-id="704dc-184">既定では、labelPosition が stacked に設定されています。</span><span class="sxs-lookup"><span data-stu-id="704dc-184">By default, labelPosition is set to stacked.</span></span>

> <span data-ttu-id="704dc-185">[Design](view-model-ipage-idesign.md).[labelPosition](view-model-ipage-idesign.md#labelposition) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-185">Inherited from [Design](view-model-ipage-idesign.md).[labelPosition](view-model-ipage-idesign.md#labelposition)</span></span>


### <a name="name"></a><span data-ttu-id="704dc-186">名前</span><span class="sxs-lookup"><span data-stu-id="704dc-186">name</span></span>

<span data-ttu-id="704dc-187">name: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-187">name: string (optional)</span></span> 



> <span data-ttu-id="704dc-188">[Design](view-model-ipage-idesign.md).[name](view-model-ipage-idesign.md#name) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-188">Inherited from [Design](view-model-ipage-idesign.md).[name](view-model-ipage-idesign.md#name)</span></span>


### <a name="padding"></a><span data-ttu-id="704dc-189">padding</span><span class="sxs-lookup"><span data-stu-id="704dc-189">padding</span></span>

<span data-ttu-id="704dc-190">padding: "none" &#124; "small" &#124; "std" (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-190">padding: "none" &#124; "small" &#124; "std" (optional)</span></span> 

<span data-ttu-id="704dc-191">コンポーネントのスペース動作を指定できるように許可します。</span><span class="sxs-lookup"><span data-stu-id="704dc-191">Allows specifying the component's padding behavior.</span></span>
<span data-ttu-id="704dc-192">コンポーネントは、親コンテナー コンポーネントによって指定されたスペース動作を継承します。</span><span class="sxs-lookup"><span data-stu-id="704dc-192">A component will inherit the padding behavior specified by its parent container components.</span></span>

> <span data-ttu-id="704dc-193">[Design](view-model-ipage-idesign.md).[padding](view-model-ipage-idesign.md#padding) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-193">Inherited from [Design](view-model-ipage-idesign.md).[padding](view-model-ipage-idesign.md#padding)</span></span>


### <a name="type"></a><span data-ttu-id="704dc-194">タイプ</span><span class="sxs-lookup"><span data-stu-id="704dc-194">type</span></span>

<span data-ttu-id="704dc-195">type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="704dc-195">type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="704dc-196">文字列としてのコントロールのタイプ。</span><span class="sxs-lookup"><span data-stu-id="704dc-196">The type of the control as a string.</span></span>

> <span data-ttu-id="704dc-197">[Design](view-model-ipage-idesign.md).[type](view-model-ipage-idesign.md#type) から継承</span><span class="sxs-lookup"><span data-stu-id="704dc-197">Inherited from [Design](view-model-ipage-idesign.md).[type](view-model-ipage-idesign.md#type)</span></span>



