---
title: TreeNodeIterator クラス
description: このトピックでは、TreeNodeIterator クラスについて説明します。
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
ms.openlocfilehash: 7ffdfd18a6b913052d06b78d741e44ef8970b278
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502786"
---
# <a name="class-treenodeiterator"></a><span data-ttu-id="81d10-103">クラス TreeNodeIterator</span><span class="sxs-lookup"><span data-stu-id="81d10-103">Class TreeNodeIterator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class TreeNodeIterator extends Object
```

<span data-ttu-id="81d10-104">TreeNodeIterator クラスは、ツリー ノードの子ノード上を移動します。</span><span class="sxs-lookup"><span data-stu-id="81d10-104">The TreeNodeIterator class traverses the child nodes of a tree node.</span></span>

## <a name="remarks"></a><span data-ttu-id="81d10-105">備考</span><span class="sxs-lookup"><span data-stu-id="81d10-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="81d10-106">例</span><span class="sxs-lookup"><span data-stu-id="81d10-106">Examples</span></span>

<span data-ttu-id="81d10-107">次の例では、ルート ノードのすべての子ノードの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="81d10-107">The following example prints the names of all child nodes of the root node.</span></span>

```xpp
static void example()  
{ 
    treeNode myTreeNode; 
    xInfo xi = new xInfo(); 
    void printChildNames (treeNode t) 
    { 
        treeNode child; 
        treenodeIterator it; 
        it = t.AOTiterator(); 
        child = it.next(); 
        while (child) 
        { 
            print child.treeNodeName(); 
            child = it.next(); 
        } 
    } 
    myTreeNode = xi.rootNode(); 
    printChildNames(myTreeNode); 
    pause; 
}
```

## <a name="methods"></a><span data-ttu-id="81d10-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="81d10-108">Methods</span></span>

| <span data-ttu-id="81d10-109">方法</span><span class="sxs-lookup"><span data-stu-id="81d10-109">Method</span></span>                 | <span data-ttu-id="81d10-110">説明</span><span class="sxs-lookup"><span data-stu-id="81d10-110">Description</span></span>                                                                                            |
|------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d10-111">public TreeNode next()</span><span class="sxs-lookup"><span data-stu-id="81d10-111">public TreeNode next()</span></span> | <span data-ttu-id="81d10-112">子ノードの一覧の次の要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="81d10-112">Retrieves the next element in the list of child nodes.</span></span>                                                 |
| <span data-ttu-id="81d10-113">public void reset()</span><span class="sxs-lookup"><span data-stu-id="81d10-113">public void reset()</span></span>    | <span data-ttu-id="81d10-114">次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="81d10-114">Resets the iterator so that the next call to the next method returns the first child node in the list.</span></span> |

## <a name="method-next"></a><span data-ttu-id="81d10-115">メソッド next</span><span class="sxs-lookup"><span data-stu-id="81d10-115">Method next</span></span>

<span data-ttu-id="81d10-116">子ノードの一覧の次の要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="81d10-116">Retrieves the next element in the list of child nodes.</span></span>

```xpp
public TreeNode next()
```

### <a name="return-value---next"></a><span data-ttu-id="81d10-117">戻り値 - next</span><span class="sxs-lookup"><span data-stu-id="81d10-117">Return Value - next</span></span>

<span data-ttu-id="81d10-118">ツリー内の次の子ノード。</span><span class="sxs-lookup"><span data-stu-id="81d10-118">The next child node in the tree.</span></span>

## <a name="method-reset"></a><span data-ttu-id="81d10-119">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="81d10-119">Method reset</span></span>

<span data-ttu-id="81d10-120">次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="81d10-120">Resets the iterator so that the next call to the next method returns the first child node in the list.</span></span>

```xpp
public void reset()
```

