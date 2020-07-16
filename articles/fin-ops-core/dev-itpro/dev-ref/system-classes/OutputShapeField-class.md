---
title: OutputShapeField クラス
description: このトピックでは、OutputShapeField クラスについて説明します。
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
ms.openlocfilehash: 9afdc6732f011f88cacf37f450303d96c8833081
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502882"
---
# <a name="class-outputshapefield"></a><span data-ttu-id="89a21-103">クラス OutputShapeField</span><span class="sxs-lookup"><span data-stu-id="89a21-103">Class OutputShapeField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OutputShapeField extends OutputField
```

## <a name="remarks"></a><span data-ttu-id="89a21-104">備考</span><span class="sxs-lookup"><span data-stu-id="89a21-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="89a21-105">例</span><span class="sxs-lookup"><span data-stu-id="89a21-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="89a21-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="89a21-106">Methods</span></span>

| <span data-ttu-id="89a21-107">方法</span><span class="sxs-lookup"><span data-stu-id="89a21-107">Method</span></span>                       | <span data-ttu-id="89a21-108">説明</span><span class="sxs-lookup"><span data-stu-id="89a21-108">Description</span></span>                                               |
|------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="89a21-109">public int borderWidth()</span><span class="sxs-lookup"><span data-stu-id="89a21-109">public int borderWidth()</span></span>     |                                                           |
| <span data-ttu-id="89a21-110">public LineType lineType()</span><span class="sxs-lookup"><span data-stu-id="89a21-110">public LineType lineType()</span></span>   |                                                           |
| <span data-ttu-id="89a21-111">public ShapeType shapeType()</span><span class="sxs-lookup"><span data-stu-id="89a21-111">public ShapeType shapeType()</span></span> |                                                           |
| <span data-ttu-id="89a21-112">public str toString()</span><span class="sxs-lookup"><span data-stu-id="89a21-112">public str toString()</span></span>        | <span data-ttu-id="89a21-113">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="89a21-113">Returns a string that represents the current object.</span></span>      |
| <span data-ttu-id="89a21-114">public int value()</span><span class="sxs-lookup"><span data-stu-id="89a21-114">public int value()</span></span>           |                                                           |
| <span data-ttu-id="89a21-115">public void new()</span><span class="sxs-lookup"><span data-stu-id="89a21-115">public void new()</span></span>            | <span data-ttu-id="89a21-116">OutputShapeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89a21-116">Initializes a new instance of the OutputShapeField class.</span></span> |

## <a name="method-borderwidth"></a><span data-ttu-id="89a21-117">メソッド borderWidth</span><span class="sxs-lookup"><span data-stu-id="89a21-117">Method borderWidth</span></span>

```xpp
public int borderWidth()
```

### <a name="return-value---borderwidth"></a><span data-ttu-id="89a21-118">戻り値 - borderWidth</span><span class="sxs-lookup"><span data-stu-id="89a21-118">Return Value - borderWidth</span></span>

## <a name="method-linetype"></a><span data-ttu-id="89a21-119">メソッド lineType</span><span class="sxs-lookup"><span data-stu-id="89a21-119">Method lineType</span></span>

```xpp
public LineType lineType()
```

### <a name="return-value---linetype"></a><span data-ttu-id="89a21-120">戻り値 - lineType</span><span class="sxs-lookup"><span data-stu-id="89a21-120">Return Value - lineType</span></span>

## <a name="method-shapetype"></a><span data-ttu-id="89a21-121">メソッド shapeType</span><span class="sxs-lookup"><span data-stu-id="89a21-121">Method shapeType</span></span>

```xpp
public ShapeType shapeType()
```

### <a name="return-value---shapetype"></a><span data-ttu-id="89a21-122">戻り値 - shapeType</span><span class="sxs-lookup"><span data-stu-id="89a21-122">Return Value - shapeType</span></span>

## <a name="method-tostring"></a><span data-ttu-id="89a21-123">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="89a21-123">Method toString</span></span>

<span data-ttu-id="89a21-124">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="89a21-124">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="89a21-125">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="89a21-125">Return Value - toString</span></span>

<span data-ttu-id="89a21-126">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="89a21-126">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="89a21-127">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="89a21-127">Remarks - toString</span></span>

<span data-ttu-id="89a21-128">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="89a21-128">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="89a21-129">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="89a21-129">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="89a21-130">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="89a21-130">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

## <a name="method-value"></a><span data-ttu-id="89a21-131">メソッド value</span><span class="sxs-lookup"><span data-stu-id="89a21-131">Method value</span></span>

```xpp
public int value()
```

### <a name="return-value---value"></a><span data-ttu-id="89a21-132">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="89a21-132">Return Value - value</span></span>

## <a name="method-new"></a><span data-ttu-id="89a21-133">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89a21-133">Method new</span></span>

<span data-ttu-id="89a21-134">OutputShapeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89a21-134">Initializes a new instance of the OutputShapeField class.</span></span>

```xpp
public void new()
```

