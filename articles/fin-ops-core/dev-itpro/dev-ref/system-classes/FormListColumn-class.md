---
title: FormListColumn クラス
description: このトピックでは、FormListColumn クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bb4e5433514521e310182ddb33c7b4bbaf4e46e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502931"
---
# <a name="class-formlistcolumn"></a><span data-ttu-id="fdf66-103">クラス FormListColumn</span><span class="sxs-lookup"><span data-stu-id="fdf66-103">Class FormListColumn</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormListColumn extends Object
```

<span data-ttu-id="fdf66-104">FormListColumn クラスは、フォームのリスト列機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-104">The FormListColumn class provides list column functionality for a form.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdf66-105">備考</span><span class="sxs-lookup"><span data-stu-id="fdf66-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fdf66-106">例</span><span class="sxs-lookup"><span data-stu-id="fdf66-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fdf66-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="fdf66-107">Methods</span></span>

| <span data-ttu-id="fdf66-108">方法</span><span class="sxs-lookup"><span data-stu-id="fdf66-108">Method</span></span>                                                      | <span data-ttu-id="fdf66-109">説明</span><span class="sxs-lookup"><span data-stu-id="fdf66-109">Description</span></span>                                               |
|-------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="fdf66-110">public FormListFormat format(\[FormListFormat value\])</span><span class="sxs-lookup"><span data-stu-id="fdf66-110">public FormListFormat format(\[FormListFormat value\])</span></span>      |                                                           |
| <span data-ttu-id="fdf66-111">public int image(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fdf66-111">public int image(\[int value\])</span></span>                             |                                                           |
| <span data-ttu-id="fdf66-112">public int order(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fdf66-112">public int order(\[int value\])</span></span>                             |                                                           |
| <span data-ttu-id="fdf66-113">public int subItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fdf66-113">public int subItem(\[int value\])</span></span>                           |                                                           |
| <span data-ttu-id="fdf66-114">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fdf66-114">public str text(\[str value\])</span></span>                              |                                                           |
| <span data-ttu-id="fdf66-115">public str toString()</span><span class="sxs-lookup"><span data-stu-id="fdf66-115">public str toString()</span></span>                                       | <span data-ttu-id="fdf66-116">クラス ハンドルと名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-116">Returns a string that contains the class handle and name.</span></span> |
| <span data-ttu-id="fdf66-117">public int width(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fdf66-117">public int width(\[int value\])</span></span>                             | <span data-ttu-id="fdf66-118">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-118">Gets or sets the width of the control.</span></span>                    |
| <span data-ttu-id="fdf66-119">public void new(\[str Text\], \[int ColNo\], \[int Width\])</span><span class="sxs-lookup"><span data-stu-id="fdf66-119">public void new(\[str Text\], \[int ColNo\], \[int Width\])</span></span> | <span data-ttu-id="fdf66-120">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-120">Initializes a new instance of the Object class.</span></span>           |
| <span data-ttu-id="fdf66-121">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="fdf66-121">public void finalize()</span></span>                                      |                                                           |

## <a name="method-format"></a><span data-ttu-id="fdf66-122">メソッド format</span><span class="sxs-lookup"><span data-stu-id="fdf66-122">Method format</span></span>

```xpp
public FormListFormat format([FormListFormat value])
```

### <a name="parameters---format"></a><span data-ttu-id="fdf66-123">パラメーター - format</span><span class="sxs-lookup"><span data-stu-id="fdf66-123">Parameters - format</span></span>

<span data-ttu-id="fdf66-124">値</span><span class="sxs-lookup"><span data-stu-id="fdf66-124">value</span></span>  

### <a name="return-value---format"></a><span data-ttu-id="fdf66-125">戻り値 - format</span><span class="sxs-lookup"><span data-stu-id="fdf66-125">Return Value - format</span></span>

## <a name="method-image"></a><span data-ttu-id="fdf66-126">メソッド image</span><span class="sxs-lookup"><span data-stu-id="fdf66-126">Method image</span></span>

```xpp
public int image([int value])
```

### <a name="parameters---image"></a><span data-ttu-id="fdf66-127">パラメーター - image</span><span class="sxs-lookup"><span data-stu-id="fdf66-127">Parameters - image</span></span>

<span data-ttu-id="fdf66-128">値</span><span class="sxs-lookup"><span data-stu-id="fdf66-128">value</span></span>  

### <a name="return-value---image"></a><span data-ttu-id="fdf66-129">戻り値 - image</span><span class="sxs-lookup"><span data-stu-id="fdf66-129">Return Value - image</span></span>

## <a name="method-order"></a><span data-ttu-id="fdf66-130">メソッド order</span><span class="sxs-lookup"><span data-stu-id="fdf66-130">Method order</span></span>

```xpp
public int order([int value])
```

### <a name="parameters---order"></a><span data-ttu-id="fdf66-131">パラメーター - order</span><span class="sxs-lookup"><span data-stu-id="fdf66-131">Parameters - order</span></span>

<span data-ttu-id="fdf66-132">値</span><span class="sxs-lookup"><span data-stu-id="fdf66-132">value</span></span>  

### <a name="return-value---order"></a><span data-ttu-id="fdf66-133">戻り値 - order</span><span class="sxs-lookup"><span data-stu-id="fdf66-133">Return Value - order</span></span>

## <a name="method-subitem"></a><span data-ttu-id="fdf66-134">メソッド subItem</span><span class="sxs-lookup"><span data-stu-id="fdf66-134">Method subItem</span></span>

```xpp
public int subItem([int value])
```

### <a name="parameters---subitem"></a><span data-ttu-id="fdf66-135">パラメーター - subItem</span><span class="sxs-lookup"><span data-stu-id="fdf66-135">Parameters - subItem</span></span>

<span data-ttu-id="fdf66-136">値</span><span class="sxs-lookup"><span data-stu-id="fdf66-136">value</span></span>  

### <a name="return-value---subitem"></a><span data-ttu-id="fdf66-137">戻り値 - subItem</span><span class="sxs-lookup"><span data-stu-id="fdf66-137">Return Value - subItem</span></span>

## <a name="method-text"></a><span data-ttu-id="fdf66-138">メソッド text</span><span class="sxs-lookup"><span data-stu-id="fdf66-138">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="fdf66-139">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="fdf66-139">Parameters - text</span></span>

<span data-ttu-id="fdf66-140">値</span><span class="sxs-lookup"><span data-stu-id="fdf66-140">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="fdf66-141">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="fdf66-141">Return Value - text</span></span>

## <a name="method-tostring"></a><span data-ttu-id="fdf66-142">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="fdf66-142">Method toString</span></span>

<span data-ttu-id="fdf66-143">クラス ハンドルと名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-143">Returns a string that contains the class handle and name.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="fdf66-144">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="fdf66-144">Return Value - toString</span></span>

<span data-ttu-id="fdf66-145">クラスのテキスト表現。</span><span class="sxs-lookup"><span data-stu-id="fdf66-145">A text representation of the class.</span></span>

## <a name="method-width"></a><span data-ttu-id="fdf66-146">メソッド width</span><span class="sxs-lookup"><span data-stu-id="fdf66-146">Method width</span></span>

<span data-ttu-id="fdf66-147">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-147">Gets or sets the width of the control.</span></span>

```xpp
public int width([int value])
```

### <a name="parameters---width"></a><span data-ttu-id="fdf66-148">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="fdf66-148">Parameters - width</span></span>

<span data-ttu-id="fdf66-149">値</span><span class="sxs-lookup"><span data-stu-id="fdf66-149">value</span></span>  
<span data-ttu-id="fdf66-150">リストの列幅として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fdf66-150">The value to assign as the width of the list column; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="fdf66-151">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="fdf66-151">Return Value - width</span></span>

<span data-ttu-id="fdf66-152">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="fdf66-152">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="fdf66-153">備考 - width</span><span class="sxs-lookup"><span data-stu-id="fdf66-153">Remarks - width</span></span>

<span data-ttu-id="fdf66-154">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fdf66-154">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="fdf66-155">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-155">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="fdf66-156">モード</span><span class="sxs-lookup"><span data-stu-id="fdf66-156">Mode</span></span>             | <span data-ttu-id="fdf66-157">幅計算</span><span class="sxs-lookup"><span data-stu-id="fdf66-157">Width calculation</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf66-158">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="fdf66-158">-1 � Exact</span></span>       | <span data-ttu-id="fdf66-159">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fdf66-159">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="fdf66-160">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="fdf66-160">0 � Auto</span></span>         | <span data-ttu-id="fdf66-161">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fdf66-161">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fdf66-162">1 � 列の幅</span><span class="sxs-lookup"><span data-stu-id="fdf66-162">1 � Column width</span></span> | <span data-ttu-id="fdf66-163">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="fdf66-163">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="fdf66-164">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fdf66-164">The width and the width calculation mode can be set separately.</span></span>

## <a name="method-new"></a><span data-ttu-id="fdf66-165">メソッド new</span><span class="sxs-lookup"><span data-stu-id="fdf66-165">Method new</span></span>

<span data-ttu-id="fdf66-166">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fdf66-166">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([str Text], [int ColNo], [int Width])
```

### <a name="parameters---new"></a><span data-ttu-id="fdf66-167">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="fdf66-167">Parameters - new</span></span>

<span data-ttu-id="fdf66-168">テキスト</span><span class="sxs-lookup"><span data-stu-id="fdf66-168">Text</span></span>  

<!-- -->

<span data-ttu-id="fdf66-169">ColNo</span><span class="sxs-lookup"><span data-stu-id="fdf66-169">ColNo</span></span>  

<!-- -->

<span data-ttu-id="fdf66-170">Width</span><span class="sxs-lookup"><span data-stu-id="fdf66-170">Width</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="fdf66-171">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="fdf66-171">Method finalize</span></span>

```xpp
public void finalize()
```

