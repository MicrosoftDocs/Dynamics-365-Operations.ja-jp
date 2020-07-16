---
title: OutputIntegerField クラス
description: このトピックでは、OutputIntegerField クラスについて説明します。
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
ms.openlocfilehash: 06cfd2d27f24581ba7b8e267705dd0f4c8baddd3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502548"
---
# <a name="class-outputintegerfield"></a><span data-ttu-id="43633-103">クラス OutputIntegerField</span><span class="sxs-lookup"><span data-stu-id="43633-103">Class OutputIntegerField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OutputIntegerField extends OutputField
```

## <a name="remarks"></a><span data-ttu-id="43633-104">備考</span><span class="sxs-lookup"><span data-stu-id="43633-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="43633-105">例</span><span class="sxs-lookup"><span data-stu-id="43633-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="43633-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="43633-106">Methods</span></span>

| <span data-ttu-id="43633-107">方法</span><span class="sxs-lookup"><span data-stu-id="43633-107">Method</span></span>                        | <span data-ttu-id="43633-108">説明</span><span class="sxs-lookup"><span data-stu-id="43633-108">Description</span></span>                                                 |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="43633-109">public int displaceNegative()</span><span class="sxs-lookup"><span data-stu-id="43633-109">public int displaceNegative()</span></span> |                                                             |
| <span data-ttu-id="43633-110">public boolean negative()</span><span class="sxs-lookup"><span data-stu-id="43633-110">public boolean negative()</span></span>     |                                                             |
| <span data-ttu-id="43633-111">public str toString()</span><span class="sxs-lookup"><span data-stu-id="43633-111">public str toString()</span></span>         | <span data-ttu-id="43633-112">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="43633-112">Returns a string that represents the current object.</span></span>        |
| <span data-ttu-id="43633-113">public int value()</span><span class="sxs-lookup"><span data-stu-id="43633-113">public int value()</span></span>            |                                                             |
| <span data-ttu-id="43633-114">public void new()</span><span class="sxs-lookup"><span data-stu-id="43633-114">public void new()</span></span>             | <span data-ttu-id="43633-115">OutputIntegerField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="43633-115">Initializes a new instance of the OutputIntegerField class.</span></span> |

## <a name="method-displacenegative"></a><span data-ttu-id="43633-116">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="43633-116">Method displaceNegative</span></span>

```xpp
public int displaceNegative()
```

### <a name="return-value---displacenegative"></a><span data-ttu-id="43633-117">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="43633-117">Return Value - displaceNegative</span></span>

## <a name="method-negative"></a><span data-ttu-id="43633-118">メソッド negative</span><span class="sxs-lookup"><span data-stu-id="43633-118">Method negative</span></span>

```xpp
public boolean negative()
```

### <a name="return-value---negative"></a><span data-ttu-id="43633-119">戻り値 - negative</span><span class="sxs-lookup"><span data-stu-id="43633-119">Return Value - negative</span></span>

## <a name="method-tostring"></a><span data-ttu-id="43633-120">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="43633-120">Method toString</span></span>

<span data-ttu-id="43633-121">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="43633-121">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="43633-122">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="43633-122">Return Value - toString</span></span>

<span data-ttu-id="43633-123">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="43633-123">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="43633-124">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="43633-124">Remarks - toString</span></span>

<span data-ttu-id="43633-125">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="43633-125">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="43633-126">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="43633-126">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="43633-127">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="43633-127">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

## <a name="method-value"></a><span data-ttu-id="43633-128">メソッド value</span><span class="sxs-lookup"><span data-stu-id="43633-128">Method value</span></span>

```xpp
public int value()
```

### <a name="return-value---value"></a><span data-ttu-id="43633-129">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="43633-129">Return Value - value</span></span>

## <a name="method-new"></a><span data-ttu-id="43633-130">メソッド new</span><span class="sxs-lookup"><span data-stu-id="43633-130">Method new</span></span>

<span data-ttu-id="43633-131">OutputIntegerField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="43633-131">Initializes a new instance of the OutputIntegerField class.</span></span>

```xpp
public void new()
```

