---
title: TreeNodeType クラス
description: このトピックでは、TreeNodeType クラスについて説明します。
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
ms.openlocfilehash: e61c9b5596df888f092e2f7b1cb8c2cb475f8c3b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502787"
---
# <a name="class-treenodetype"></a><span data-ttu-id="dfbbe-103">クラス TreeNodeType</span><span class="sxs-lookup"><span data-stu-id="dfbbe-103">Class TreeNodeType</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class TreeNodeType extends Object
```

<span data-ttu-id="dfbbe-104">TreeNodeType クラスは、TreeNode クラスのタイプに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-104">The TreeNodeType class retrieves information about types of TreeNode classes.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfbbe-105">備考</span><span class="sxs-lookup"><span data-stu-id="dfbbe-105">Remarks</span></span>

<span data-ttu-id="dfbbe-106">このクラスを使用すると、TreeNode クラスのインスタンスを反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-106">This class enable you to reflect on a TreeNode class instance.</span></span> <span data-ttu-id="dfbbe-107">リフレクション情報は、TreeNode クラスのインスタンスに固有ではありません。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-107">The reflection information is not specific to an instance of a TreeNode class.</span></span> <span data-ttu-id="dfbbe-108">同じ NodeType を持つすべての TreeNode インスタンスは、同じ TreeNodeType を共有します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-108">All TreeNode instances with the same NodeType share the same TreeNodeType.</span></span> <span data-ttu-id="dfbbe-109">TreeNode.TreeNodeType メソッドは、リフレクション情報を含む treeNodeType オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-109">The TreeNode.TreeNodeType method return a treeNodeType object with the reflection information.</span></span>

## <a name="examples"></a><span data-ttu-id="dfbbe-110">例</span><span class="sxs-lookup"><span data-stu-id="dfbbe-110">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="dfbbe-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="dfbbe-111">Methods</span></span>

| <span data-ttu-id="dfbbe-112">方法</span><span class="sxs-lookup"><span data-stu-id="dfbbe-112">Method</span></span>                                     | <span data-ttu-id="dfbbe-113">説明</span><span class="sxs-lookup"><span data-stu-id="dfbbe-113">Description</span></span>                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbbe-114">public int id()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-114">public int id()</span></span>                            | <span data-ttu-id="dfbbe-115">タイプの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-115">Returns the type's ID.</span></span>                                                                                 |
| <span data-ttu-id="dfbbe-116">public boolean isConsumingMemory()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-116">public boolean isConsumingMemory()</span></span>         | <span data-ttu-id="dfbbe-117">このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-117">Indicates whether instances of this node type are consuming memory that needs to be manually released.</span></span> |
| <span data-ttu-id="dfbbe-118">public boolean isGetNodeInLayerSupported()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-118">public boolean isGetNodeInLayerSupported()</span></span> | <span data-ttu-id="dfbbe-119">このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-119">Indicates whether instances of this node type support the TreeNode.GetNodeInLayer method.</span></span>              |
| <span data-ttu-id="dfbbe-120">public boolean isLayerAware()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-120">public boolean isLayerAware()</span></span>              | <span data-ttu-id="dfbbe-121">このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-121">Indicates whether instances of this node type are decorated with layers in the AOT.</span></span>                    |
| <span data-ttu-id="dfbbe-122">public boolean isModelElement()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-122">public boolean isModelElement()</span></span>            | <span data-ttu-id="dfbbe-123">このノード タイプのインスタンスがモデル要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-123">Indicates whether instances of this node type are model-elements.</span></span>                                      |
| <span data-ttu-id="dfbbe-124">public boolean isRootElement()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-124">public boolean isRootElement()</span></span>             | <span data-ttu-id="dfbbe-125">このノード タイプのインスタンスがルート要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-125">Indicates whether instances of this node type are root-elements.</span></span>                                       |
| <span data-ttu-id="dfbbe-126">public boolean isUtilElement()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-126">public boolean isUtilElement()</span></span>             | <span data-ttu-id="dfbbe-127">このノード タイプのインスタンスがユーティリティ要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-127">Indicates whether instances of this node type are util-elements.</span></span>                                       |
| <span data-ttu-id="dfbbe-128">public boolean isVCSControllableElement()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-128">public boolean isVCSControllableElement()</span></span>  |                                                                                                        |
| <span data-ttu-id="dfbbe-129">private void new()</span><span class="sxs-lookup"><span data-stu-id="dfbbe-129">private void new()</span></span>                         | <span data-ttu-id="dfbbe-130">TreeNodeType クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-130">Initializes a new instance of the TreeNodeType class.</span></span>                                                  |

## <a name="method-id"></a><span data-ttu-id="dfbbe-131">メソッド id</span><span class="sxs-lookup"><span data-stu-id="dfbbe-131">Method id</span></span>

<span data-ttu-id="dfbbe-132">タイプの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-132">Returns the type's ID.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="dfbbe-133">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="dfbbe-133">Return Value - id</span></span>

<span data-ttu-id="dfbbe-134">TreeNodeType の ID。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-134">The ID of the TreeNodeType.</span></span>

## <a name="method-isconsumingmemory"></a><span data-ttu-id="dfbbe-135">メソッド isConsumingMemory</span><span class="sxs-lookup"><span data-stu-id="dfbbe-135">Method isConsumingMemory</span></span>

<span data-ttu-id="dfbbe-136">このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-136">Indicates whether instances of this node type are consuming memory that needs to be manually released.</span></span>

```xpp
public boolean isConsumingMemory()
```

### <a name="return-value---isconsumingmemory"></a><span data-ttu-id="dfbbe-137">戻り値 - isConsumingMemory</span><span class="sxs-lookup"><span data-stu-id="dfbbe-137">Return Value - isConsumingMemory</span></span>

<span data-ttu-id="dfbbe-138">このタイプのツリー ノードがメモリを消費する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-138">true if tree nodes of this type consumes memory; otherwise, false.</span></span>

### <a name="remarks---isconsumingmemory"></a><span data-ttu-id="dfbbe-139">備考 - isConsumingMemory</span><span class="sxs-lookup"><span data-stu-id="dfbbe-139">Remarks - isConsumingMemory</span></span>

<span data-ttu-id="dfbbe-140">このタイプの TreeNode インスタンスで作業した後は、TreeNode.TreeNodeRelease メソッドを呼び出して、消費されたメモリを解放することが重要です。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-140">After working with TreeNode instances of this type it is important to call the TreeNode.TreeNodeRelease method to release any consumed memory.</span></span> <span data-ttu-id="dfbbe-141">これを行わないと、メモリ不足の例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-141">Failure to do this will result in out-of-memory exceptions.</span></span> <span data-ttu-id="dfbbe-142">構成階層における TreeNode クラスの全てのインスタンスがガベージ コレクションになる前に、TreeNode.TreeNodeRelease メソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-142">Do not call the TreeNode.TreeNodeRelease method before all instances of TreeNode classes in the composition hierarchy has been garbage collected.</span></span> <span data-ttu-id="dfbbe-143">たとえば、MyClass.myMethod の TreeNode がまだある場合、MyClass で TreeNode.TreeNodeRelease() メソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-143">For example, do not call the TreeNode.TreeNodeRelease() method on MyClass, if you still have a TreeNode instance of MyClass.myMethod.</span></span>

## <a name="method-isgetnodeinlayersupported"></a><span data-ttu-id="dfbbe-144">メソッド isGetNodeInLayerSupported</span><span class="sxs-lookup"><span data-stu-id="dfbbe-144">Method isGetNodeInLayerSupported</span></span>

<span data-ttu-id="dfbbe-145">このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-145">Indicates whether instances of this node type support the TreeNode.GetNodeInLayer method.</span></span>

```xpp
public boolean isGetNodeInLayerSupported()
```

### <a name="return-value---isgetnodeinlayersupported"></a><span data-ttu-id="dfbbe-146">戻り値 - isGetNodeInLayerSupported</span><span class="sxs-lookup"><span data-stu-id="dfbbe-146">Return Value - isGetNodeInLayerSupported</span></span>

<span data-ttu-id="dfbbe-147">このタイプのツリー ノードが TreeNode.GetNodeInLayer メソッドをサポートする場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-147">true if tree nodes of this type support the TreeNode.GetNodeInLayer method; otherwise, false.</span></span>

## <a name="method-islayeraware"></a><span data-ttu-id="dfbbe-148">メソッド isLayerAware</span><span class="sxs-lookup"><span data-stu-id="dfbbe-148">Method isLayerAware</span></span>

<span data-ttu-id="dfbbe-149">このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-149">Indicates whether instances of this node type are decorated with layers in the AOT.</span></span>

```xpp
public boolean isLayerAware()
```

### <a name="return-value---islayeraware"></a><span data-ttu-id="dfbbe-150">戻り値 - isLayerAware</span><span class="sxs-lookup"><span data-stu-id="dfbbe-150">Return Value - isLayerAware</span></span>

<span data-ttu-id="dfbbe-151">このタイプのツリー ノードがレイヤーで修飾された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-151">true if tree nodes of this type are decorated with layers; otherwise, false.</span></span>

### <a name="remarks---islayeraware"></a><span data-ttu-id="dfbbe-152">備考 - isLayerAware</span><span class="sxs-lookup"><span data-stu-id="dfbbe-152">Remarks - isLayerAware</span></span>

<span data-ttu-id="dfbbe-153">このタイプのツリー ノードは、AOTLayer メソッドと AOTLayers メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-153">Tree nodes of this type support the AOTLayer and AOTLayers methods.</span></span>

## <a name="method-ismodelelement"></a><span data-ttu-id="dfbbe-154">メソッド isModelElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-154">Method isModelElement</span></span>

<span data-ttu-id="dfbbe-155">このノード タイプのインスタンスがモデル要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-155">Indicates whether instances of this node type are model-elements.</span></span>

```xpp
public boolean isModelElement()
```

### <a name="return-value---ismodelelement"></a><span data-ttu-id="dfbbe-156">備考 - isModelElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-156">Return Value - isModelElement</span></span>

<span data-ttu-id="dfbbe-157">このタイプのツリー ノードがモデル要素である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-157">true if tree nodes of this type are model-elements; otherwise, false.</span></span>

### <a name="remarks---ismodelelement"></a><span data-ttu-id="dfbbe-158">備考 - isModelElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-158">Remarks - isModelElement</span></span>

<span data-ttu-id="dfbbe-159">モデル要素は、モデル ストアに保持される (または保持できる) ツリー ノードです。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-159">A model-element is a tree node that is (or can be) persisted in the model store.</span></span> <span data-ttu-id="dfbbe-160">各モデル要素ツリー ノードについては、1 つのレコードはモデル ストアの ModelElements テーブル内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-160">For each model-element tree node one record can be found in the ModelElements table in the model store.</span></span> <span data-ttu-id="dfbbe-161">モデル要素は、AOT 内で含まれているモデルの名前で視覚的に修飾されます。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-161">Model-elements are visually decorated with the name of the Model they are contained by in the AOT.</span></span>

## <a name="method-isrootelement"></a><span data-ttu-id="dfbbe-162">メソッド isRootElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-162">Method isRootElement</span></span>

<span data-ttu-id="dfbbe-163">このノード タイプのインスタンスがルート要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-163">Indicates whether instances of this node type are root-elements.</span></span>

```xpp
public boolean isRootElement()
```

### <a name="return-value---isrootelement"></a><span data-ttu-id="dfbbe-164">戻り値 - isRootElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-164">Return Value - isRootElement</span></span>

<span data-ttu-id="dfbbe-165">このタイプのツリー ノードがルート要素である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-165">true if tree nodes of this type are root-elements; otherwise, false.</span></span>

### <a name="remarks---isrootelement"></a><span data-ttu-id="dfbbe-166">備考 - isRootElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-166">Remarks - isRootElement</span></span>

<span data-ttu-id="dfbbe-167">ルート要素は、ツリー ノードの構成階層のルートです。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-167">A root-element is the root in a composition hierarchy of tree nodes.</span></span> <span data-ttu-id="dfbbe-168">ルート要素は、モデル要素の親を持つことはありません。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-168">A root-element never has a model-element parent.</span></span> <span data-ttu-id="dfbbe-169">例には、MyTable、MyClass、MyForm が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-169">Examples include MyTable, MyClass, MyForm.</span></span>

## <a name="method-isutilelement"></a><span data-ttu-id="dfbbe-170">メソッド isUtilElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-170">Method isUtilElement</span></span>

<span data-ttu-id="dfbbe-171">このノード タイプのインスタンスがユーティリティ要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-171">Indicates whether instances of this node type are util-elements.</span></span>

```xpp
public boolean isUtilElement()
```

### <a name="return-value---isutilelement"></a><span data-ttu-id="dfbbe-172">戻り値 - isUtilElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-172">Return Value - isUtilElement</span></span>

<span data-ttu-id="dfbbe-173">このタイプのツリー ノードがユーティリティ要素である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-173">true if tree nodes of this type are util-elements; otherwise, false.</span></span>

### <a name="remarks---isutilelement"></a><span data-ttu-id="dfbbe-174">備考 - isUtilElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-174">Remarks - isUtilElement</span></span>

<span data-ttu-id="dfbbe-175">ユーティリティ要素は UtilElements と UtilIdElements ビューからアクセスできるツリー ノードです。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-175">An util-element is a tree node that can be accessed via the UtilElements and UtilIdElements views.</span></span> <span data-ttu-id="dfbbe-176">Util 要素はモデル要素のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-176">Util-elements are a subset of model-elements.</span></span>

## <a name="method-isvcscontrollableelement"></a><span data-ttu-id="dfbbe-177">メソッド isVCSControllableElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-177">Method isVCSControllableElement</span></span>

```xpp
public boolean isVCSControllableElement()
```

### <a name="return-value---isvcscontrollableelement"></a><span data-ttu-id="dfbbe-178">戻り値 - isVCSControllableElement</span><span class="sxs-lookup"><span data-stu-id="dfbbe-178">Return Value - isVCSControllableElement</span></span>

## <a name="method-new"></a><span data-ttu-id="dfbbe-179">メソッド new</span><span class="sxs-lookup"><span data-stu-id="dfbbe-179">Method new</span></span>

<span data-ttu-id="dfbbe-180">TreeNodeType クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="dfbbe-180">Initializes a new instance of the TreeNodeType class.</span></span>

```xpp
private void new()
```


