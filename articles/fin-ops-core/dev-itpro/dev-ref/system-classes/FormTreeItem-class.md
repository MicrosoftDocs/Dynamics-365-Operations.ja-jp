---
title: FormTreeItem クラス
description: このトピックでは、FormTreeItem クラスについて説明します。
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
ms.openlocfilehash: 43ab30c19eaaffb3f379971e548b32567c68d714
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502909"
---
# <a name="class-formtreeitem"></a><span data-ttu-id="7716b-103">クラス FormTreeItem</span><span class="sxs-lookup"><span data-stu-id="7716b-103">Class FormTreeItem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormTreeItem extends Object
```

## <a name="remarks"></a><span data-ttu-id="7716b-104">備考</span><span class="sxs-lookup"><span data-stu-id="7716b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7716b-105">例</span><span class="sxs-lookup"><span data-stu-id="7716b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7716b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="7716b-106">Methods</span></span>

| <span data-ttu-id="7716b-107">方法</span><span class="sxs-lookup"><span data-stu-id="7716b-107">Method</span></span>                                                                           | <span data-ttu-id="7716b-108">説明</span><span class="sxs-lookup"><span data-stu-id="7716b-108">Description</span></span>                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="7716b-109">public int children(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-109">public int children(\[int value\])</span></span>                                               |                                                                            |
| <span data-ttu-id="7716b-110">public AnyType data(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-110">public AnyType data(\[AnyType value\])</span></span>                                           |                                                                            |
| <span data-ttu-id="7716b-111">public int idx()</span><span class="sxs-lookup"><span data-stu-id="7716b-111">public int idx()</span></span>                                                                 |                                                                            |
| <span data-ttu-id="7716b-112">public int image(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-112">public int image(\[int value\])</span></span>                                                  |                                                                            |
| <span data-ttu-id="7716b-113">public int overlayImage(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-113">public int overlayImage(\[int value\])</span></span>                                           |                                                                            |
| <span data-ttu-id="7716b-114">public int selectedImage(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-114">public int selectedImage(\[int value\])</span></span>                                          |                                                                            |
| <span data-ttu-id="7716b-115">public boolean stateBold(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-115">public boolean stateBold(\[boolean value\])</span></span>                                      |                                                                            |
| <span data-ttu-id="7716b-116">public FormTreeCheckedState stateChecked(\[FormTreeCheckedState value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-116">public FormTreeCheckedState stateChecked(\[FormTreeCheckedState value\])</span></span>         |                                                                            |
| <span data-ttu-id="7716b-117">public boolean stateCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-117">public boolean stateCut(\[boolean value\])</span></span>                                       |                                                                            |
| <span data-ttu-id="7716b-118">public boolean stateDropHilited(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-118">public boolean stateDropHilited(\[boolean value\])</span></span>                               |                                                                            |
| <span data-ttu-id="7716b-119">public boolean stateExpanded(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-119">public boolean stateExpanded(\[boolean value\])</span></span>                                  |                                                                            |
| <span data-ttu-id="7716b-120">public boolean stateExpandedOnce(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-120">public boolean stateExpandedOnce(\[boolean value\])</span></span>                              |                                                                            |
| <span data-ttu-id="7716b-121">public int stateImage(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-121">public int stateImage(\[int value\])</span></span>                                             |                                                                            |
| <span data-ttu-id="7716b-122">public boolean stateSelected(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-122">public boolean stateSelected(\[boolean value\])</span></span>                                  |                                                                            |
| <span data-ttu-id="7716b-123">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7716b-123">public str text(\[str value\])</span></span>                                                   | <span data-ttu-id="7716b-124">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7716b-124">Sets or returns the text for the control.</span></span>                                  |
| <span data-ttu-id="7716b-125">public str toString()</span><span class="sxs-lookup"><span data-stu-id="7716b-125">public str toString()</span></span>                                                            | <span data-ttu-id="7716b-126">FormTreeItem クラスのインスタンスの文字列表現を返します。</span><span class="sxs-lookup"><span data-stu-id="7716b-126">Returns a string representation of the instance of the FormTreeItem class.</span></span> |
| <span data-ttu-id="7716b-127">public void new(\[str Text\], \[int Image\], \[int children\], \[AnyType Data\])</span><span class="sxs-lookup"><span data-stu-id="7716b-127">public void new(\[str Text\], \[int Image\], \[int children\], \[AnyType Data\])</span></span> | <span data-ttu-id="7716b-128">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7716b-128">Initializes a new instance of the Object class.</span></span>                            |
| <span data-ttu-id="7716b-129">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="7716b-129">public void finalize()</span></span>                                                           |                                                                            |

## <a name="method-children"></a><span data-ttu-id="7716b-130">メソッド children</span><span class="sxs-lookup"><span data-stu-id="7716b-130">Method children</span></span>

```xpp
public int children([int value])
```

### <a name="parameters---children"></a><span data-ttu-id="7716b-131">パラメーター - children</span><span class="sxs-lookup"><span data-stu-id="7716b-131">Parameters - children</span></span>

<span data-ttu-id="7716b-132">値</span><span class="sxs-lookup"><span data-stu-id="7716b-132">value</span></span>  

### <a name="return-value---children"></a><span data-ttu-id="7716b-133">戻り値 - children</span><span class="sxs-lookup"><span data-stu-id="7716b-133">Return Value - children</span></span>

## <a name="method-data"></a><span data-ttu-id="7716b-134">メソッド data</span><span class="sxs-lookup"><span data-stu-id="7716b-134">Method data</span></span>

```xpp
public AnyType data([AnyType value])
```

### <a name="parameters---data"></a><span data-ttu-id="7716b-135">パラメーター - data</span><span class="sxs-lookup"><span data-stu-id="7716b-135">Parameters - data</span></span>

<span data-ttu-id="7716b-136">値</span><span class="sxs-lookup"><span data-stu-id="7716b-136">value</span></span>  

### <a name="return-value---data"></a><span data-ttu-id="7716b-137">戻り値 - data</span><span class="sxs-lookup"><span data-stu-id="7716b-137">Return Value - data</span></span>

## <a name="method-idx"></a><span data-ttu-id="7716b-138">メソッド idx</span><span class="sxs-lookup"><span data-stu-id="7716b-138">Method idx</span></span>

```xpp
public int idx()
```

### <a name="return-value---idx"></a><span data-ttu-id="7716b-139">戻り値 - idx</span><span class="sxs-lookup"><span data-stu-id="7716b-139">Return Value - idx</span></span>

## <a name="method-image"></a><span data-ttu-id="7716b-140">メソッド image</span><span class="sxs-lookup"><span data-stu-id="7716b-140">Method image</span></span>

```xpp
public int image([int value])
```

### <a name="parameters---image"></a><span data-ttu-id="7716b-141">パラメーター - image</span><span class="sxs-lookup"><span data-stu-id="7716b-141">Parameters - image</span></span>

<span data-ttu-id="7716b-142">値</span><span class="sxs-lookup"><span data-stu-id="7716b-142">value</span></span>  

### <a name="return-value---image"></a><span data-ttu-id="7716b-143">戻り値 - image</span><span class="sxs-lookup"><span data-stu-id="7716b-143">Return Value - image</span></span>

## <a name="method-overlayimage"></a><span data-ttu-id="7716b-144">メソッド overlayImage</span><span class="sxs-lookup"><span data-stu-id="7716b-144">Method overlayImage</span></span>

```xpp
public int overlayImage([int value])
```

### <a name="parameters---overlayimage"></a><span data-ttu-id="7716b-145">パラメーター - overlayImage</span><span class="sxs-lookup"><span data-stu-id="7716b-145">Parameters - overlayImage</span></span>

<span data-ttu-id="7716b-146">値</span><span class="sxs-lookup"><span data-stu-id="7716b-146">value</span></span>  

### <a name="return-value---overlayimage"></a><span data-ttu-id="7716b-147">戻り値 - overlayImage</span><span class="sxs-lookup"><span data-stu-id="7716b-147">Return Value - overlayImage</span></span>

## <a name="method-selectedimage"></a><span data-ttu-id="7716b-148">メソッド selectedImage</span><span class="sxs-lookup"><span data-stu-id="7716b-148">Method selectedImage</span></span>

```xpp
public int selectedImage([int value])
```

### <a name="parameters---selectedimage"></a><span data-ttu-id="7716b-149">パラメーター - selectedImage</span><span class="sxs-lookup"><span data-stu-id="7716b-149">Parameters - selectedImage</span></span>

<span data-ttu-id="7716b-150">値</span><span class="sxs-lookup"><span data-stu-id="7716b-150">value</span></span>  

### <a name="return-value---selectedimage"></a><span data-ttu-id="7716b-151">戻り値 - selectedImage</span><span class="sxs-lookup"><span data-stu-id="7716b-151">Return Value - selectedImage</span></span>

## <a name="method-statebold"></a><span data-ttu-id="7716b-152">メソッド stateBold</span><span class="sxs-lookup"><span data-stu-id="7716b-152">Method stateBold</span></span>

```xpp
public boolean stateBold([boolean value])
```

### <a name="parameters---statebold"></a><span data-ttu-id="7716b-153">パラメーター - stateBold</span><span class="sxs-lookup"><span data-stu-id="7716b-153">Parameters - stateBold</span></span>

<span data-ttu-id="7716b-154">値</span><span class="sxs-lookup"><span data-stu-id="7716b-154">value</span></span>  

### <a name="return-value---statebold"></a><span data-ttu-id="7716b-155">戻り値 - stateBold</span><span class="sxs-lookup"><span data-stu-id="7716b-155">Return Value - stateBold</span></span>

## <a name="method-statechecked"></a><span data-ttu-id="7716b-156">メソッド stateChecked</span><span class="sxs-lookup"><span data-stu-id="7716b-156">Method stateChecked</span></span>

```xpp
public FormTreeCheckedState stateChecked([FormTreeCheckedState value])
```

### <a name="parameters---statechecked"></a><span data-ttu-id="7716b-157">パラメーター - stateChecked</span><span class="sxs-lookup"><span data-stu-id="7716b-157">Parameters - stateChecked</span></span>

<span data-ttu-id="7716b-158">値</span><span class="sxs-lookup"><span data-stu-id="7716b-158">value</span></span>  

### <a name="return-value---statechecked"></a><span data-ttu-id="7716b-159">戻り値 - stateChecked</span><span class="sxs-lookup"><span data-stu-id="7716b-159">Return Value - stateChecked</span></span>

## <a name="method-statecut"></a><span data-ttu-id="7716b-160">メソッド stateCut</span><span class="sxs-lookup"><span data-stu-id="7716b-160">Method stateCut</span></span>

```xpp
public boolean stateCut([boolean value])
```

### <a name="parameters---statecut"></a><span data-ttu-id="7716b-161">パラメーター - stateCut</span><span class="sxs-lookup"><span data-stu-id="7716b-161">Parameters - stateCut</span></span>

<span data-ttu-id="7716b-162">値</span><span class="sxs-lookup"><span data-stu-id="7716b-162">value</span></span>  

### <a name="return-value---statecut"></a><span data-ttu-id="7716b-163">戻り値 - stateCut</span><span class="sxs-lookup"><span data-stu-id="7716b-163">Return Value - stateCut</span></span>

## <a name="method-statedrophilited"></a><span data-ttu-id="7716b-164">メソッド stateDropHilited</span><span class="sxs-lookup"><span data-stu-id="7716b-164">Method stateDropHilited</span></span>

```xpp
public boolean stateDropHilited([boolean value])
```

### <a name="parameters---statedrophilited"></a><span data-ttu-id="7716b-165">パラメーター - stateDropHilited</span><span class="sxs-lookup"><span data-stu-id="7716b-165">Parameters - stateDropHilited</span></span>

<span data-ttu-id="7716b-166">値</span><span class="sxs-lookup"><span data-stu-id="7716b-166">value</span></span>  

### <a name="return-value---statedrophilited"></a><span data-ttu-id="7716b-167">戻り値 - stateDropHilited</span><span class="sxs-lookup"><span data-stu-id="7716b-167">Return Value - stateDropHilited</span></span>

## <a name="method-stateexpanded"></a><span data-ttu-id="7716b-168">メソッド stateExpanded</span><span class="sxs-lookup"><span data-stu-id="7716b-168">Method stateExpanded</span></span>

```xpp
public boolean stateExpanded([boolean value])
```

### <a name="parameters---stateexpanded"></a><span data-ttu-id="7716b-169">パラメーター - stateExpanded</span><span class="sxs-lookup"><span data-stu-id="7716b-169">Parameters - stateExpanded</span></span>

<span data-ttu-id="7716b-170">値</span><span class="sxs-lookup"><span data-stu-id="7716b-170">value</span></span>  

### <a name="return-value---stateexpanded"></a><span data-ttu-id="7716b-171">戻り値 - stateExpanded</span><span class="sxs-lookup"><span data-stu-id="7716b-171">Return Value - stateExpanded</span></span>

## <a name="method-stateexpandedonce"></a><span data-ttu-id="7716b-172">メソッド stateExpandedOnce</span><span class="sxs-lookup"><span data-stu-id="7716b-172">Method stateExpandedOnce</span></span>

```xpp
public boolean stateExpandedOnce([boolean value])
```

### <a name="parameters---stateexpandedonce"></a><span data-ttu-id="7716b-173">戻り値 - stateExpandedOnce</span><span class="sxs-lookup"><span data-stu-id="7716b-173">Parameters - stateExpandedOnce</span></span>

<span data-ttu-id="7716b-174">値</span><span class="sxs-lookup"><span data-stu-id="7716b-174">value</span></span>  

### <a name="return-value---stateexpandedonce"></a><span data-ttu-id="7716b-175">戻り値 - stateExpandedOnce</span><span class="sxs-lookup"><span data-stu-id="7716b-175">Return Value - stateExpandedOnce</span></span>

## <a name="method-stateimage"></a><span data-ttu-id="7716b-176">メソッド stateImage</span><span class="sxs-lookup"><span data-stu-id="7716b-176">Method stateImage</span></span>

```xpp
public int stateImage([int value])
```

### <a name="parameters---stateimage"></a><span data-ttu-id="7716b-177">パラメーター - stateImage</span><span class="sxs-lookup"><span data-stu-id="7716b-177">Parameters - stateImage</span></span>

<span data-ttu-id="7716b-178">値</span><span class="sxs-lookup"><span data-stu-id="7716b-178">value</span></span>  

### <a name="return-value---stateimage"></a><span data-ttu-id="7716b-179">戻り値 - stateImage</span><span class="sxs-lookup"><span data-stu-id="7716b-179">Return Value - stateImage</span></span>

## <a name="method-stateselected"></a><span data-ttu-id="7716b-180">メソッド stateSelected</span><span class="sxs-lookup"><span data-stu-id="7716b-180">Method stateSelected</span></span>

```xpp
public boolean stateSelected([boolean value])
```

### <a name="parameters---stateselected"></a><span data-ttu-id="7716b-181">パラメーター - stateSelected</span><span class="sxs-lookup"><span data-stu-id="7716b-181">Parameters - stateSelected</span></span>

<span data-ttu-id="7716b-182">値</span><span class="sxs-lookup"><span data-stu-id="7716b-182">value</span></span>  

### <a name="return-value---stateselected"></a><span data-ttu-id="7716b-183">戻り値 - stateSelected</span><span class="sxs-lookup"><span data-stu-id="7716b-183">Return Value - stateSelected</span></span>

## <a name="method-text"></a><span data-ttu-id="7716b-184">メソッド text</span><span class="sxs-lookup"><span data-stu-id="7716b-184">Method text</span></span>

<span data-ttu-id="7716b-185">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7716b-185">Sets or returns the text for the control.</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="7716b-186">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="7716b-186">Parameters - text</span></span>

<span data-ttu-id="7716b-187">値</span><span class="sxs-lookup"><span data-stu-id="7716b-187">value</span></span>  
<span data-ttu-id="7716b-188">コントロールのテキストとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7716b-188">The value to assign as the text for the control; optional.</span></span>

### <a name="return-value---text"></a><span data-ttu-id="7716b-189">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="7716b-189">Return Value - text</span></span>

<span data-ttu-id="7716b-190">コントロールのテキスト。コントロールにテキストが割り当てられていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7716b-190">The text for the control; an empty string if no text has been assigned to the control.</span></span>

## <a name="method-tostring"></a><span data-ttu-id="7716b-191">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="7716b-191">Method toString</span></span>

<span data-ttu-id="7716b-192">FormTreeItem クラスのインスタンスの文字列表現を返します。</span><span class="sxs-lookup"><span data-stu-id="7716b-192">Returns a string representation of the instance of the FormTreeItem class.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="7716b-193">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="7716b-193">Return Value - toString</span></span>

<span data-ttu-id="7716b-194">FormTreeItem クラスのインスタンスの説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="7716b-194">A string that contains a description of the instance of the FormTreeItem class.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="7716b-195">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="7716b-195">Remarks - toString</span></span>

<span data-ttu-id="7716b-196">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="7716b-196">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="7716b-197">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7716b-197">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="7716b-198">例 - toString</span><span class="sxs-lookup"><span data-stu-id="7716b-198">Examples - toString</span></span>

<span data-ttu-id="7716b-199">次の例は、toString メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7716b-199">The following example shows how to use the toString method.</span></span>

```xpp
print objFormTreeItem.toString();
```

## <a name="method-new"></a><span data-ttu-id="7716b-200">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7716b-200">Method new</span></span>

<span data-ttu-id="7716b-201">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7716b-201">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([str Text], [int Image], [int children], [AnyType Data])
```

### <a name="parameters---new"></a><span data-ttu-id="7716b-202">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="7716b-202">Parameters - new</span></span>

<span data-ttu-id="7716b-203">テキスト</span><span class="sxs-lookup"><span data-stu-id="7716b-203">Text</span></span>  

<!-- -->

<span data-ttu-id="7716b-204">画像</span><span class="sxs-lookup"><span data-stu-id="7716b-204">Image</span></span>  

<!-- -->

<span data-ttu-id="7716b-205">children</span><span class="sxs-lookup"><span data-stu-id="7716b-205">children</span></span>  

<!-- -->

<span data-ttu-id="7716b-206">データ</span><span class="sxs-lookup"><span data-stu-id="7716b-206">Data</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="7716b-207">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="7716b-207">Method finalize</span></span>

```xpp
public void finalize()
```

