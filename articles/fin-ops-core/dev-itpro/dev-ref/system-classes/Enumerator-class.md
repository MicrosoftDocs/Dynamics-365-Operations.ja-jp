---
title: Enumerator クラス
description: このトピックでは、Enumerator クラスについて説明します。
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
ms.openlocfilehash: e3c5d3f2fcf69fd8ae298308ccdde686db568617
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502981"
---
# <a name="class-enumerator"></a><span data-ttu-id="c72b9-103">クラス列挙子</span><span class="sxs-lookup"><span data-stu-id="c72b9-103">Class Enumerator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Enumerator extends Object
```

## <a name="remarks"></a><span data-ttu-id="c72b9-104">備考</span><span class="sxs-lookup"><span data-stu-id="c72b9-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c72b9-105">例</span><span class="sxs-lookup"><span data-stu-id="c72b9-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c72b9-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c72b9-106">Methods</span></span>

| <span data-ttu-id="c72b9-107">方法</span><span class="sxs-lookup"><span data-stu-id="c72b9-107">Method</span></span>                        | <span data-ttu-id="c72b9-108">説明</span><span class="sxs-lookup"><span data-stu-id="c72b9-108">Description</span></span>                                          |
|-------------------------------|------------------------------------------------------|
| <span data-ttu-id="c72b9-109">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="c72b9-109">public AnyType current()</span></span>      |                                                      |
| <span data-ttu-id="c72b9-110">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="c72b9-110">public str definitionString()</span></span> |                                                      |
| <span data-ttu-id="c72b9-111">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="c72b9-111">public boolean moveNext()</span></span>     |                                                      |
| <span data-ttu-id="c72b9-112">public str toString()</span><span class="sxs-lookup"><span data-stu-id="c72b9-112">public str toString()</span></span>         | <span data-ttu-id="c72b9-113">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="c72b9-113">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="c72b9-114">public void reset()</span><span class="sxs-lookup"><span data-stu-id="c72b9-114">public void reset()</span></span>           |                                                      |

## <a name="method-current"></a><span data-ttu-id="c72b9-115">メソッド current</span><span class="sxs-lookup"><span data-stu-id="c72b9-115">Method current</span></span>

```xpp
public AnyType current()
```

### <a name="return-value---current"></a><span data-ttu-id="c72b9-116">戻り値 - current</span><span class="sxs-lookup"><span data-stu-id="c72b9-116">Return Value - current</span></span>

## <a name="method-definitionstring"></a><span data-ttu-id="c72b9-117">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="c72b9-117">Method definitionString</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="c72b9-118">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="c72b9-118">Return Value - definitionString</span></span>

## <a name="method-movenext"></a><span data-ttu-id="c72b9-119">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="c72b9-119">Method moveNext</span></span>

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a><span data-ttu-id="c72b9-120">戻り値 - moveNext</span><span class="sxs-lookup"><span data-stu-id="c72b9-120">Return Value - moveNext</span></span>

## <a name="method-tostring"></a><span data-ttu-id="c72b9-121">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="c72b9-121">Method toString</span></span>

<span data-ttu-id="c72b9-122">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="c72b9-122">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="c72b9-123">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="c72b9-123">Return Value - toString</span></span>

<span data-ttu-id="c72b9-124">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="c72b9-124">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="c72b9-125">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="c72b9-125">Remarks - toString</span></span>

<span data-ttu-id="c72b9-126">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="c72b9-126">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="c72b9-127">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c72b9-127">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="c72b9-128">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="c72b9-128">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-reset"></a><span data-ttu-id="c72b9-129">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="c72b9-129">Method reset</span></span>

```xpp
public void reset()
```

