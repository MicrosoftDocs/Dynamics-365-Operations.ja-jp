---
title: QueryFilter クラス
description: このトピックでは、QueryFilter クラスについて説明します。
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
ms.openlocfilehash: d3ef7ac6dcdccddd7d7f2c25d7ef1627351bdce6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502862"
---
# <a name="class-queryfilter"></a><span data-ttu-id="20d9b-103">クラス QueryFilter</span><span class="sxs-lookup"><span data-stu-id="20d9b-103">Class QueryFilter</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryFilter extends Object
```

## <a name="remarks"></a><span data-ttu-id="20d9b-104">備考</span><span class="sxs-lookup"><span data-stu-id="20d9b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="20d9b-105">例</span><span class="sxs-lookup"><span data-stu-id="20d9b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="20d9b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="20d9b-106">Methods</span></span>

| <span data-ttu-id="20d9b-107">方法</span><span class="sxs-lookup"><span data-stu-id="20d9b-107">Method</span></span>                                                        | <span data-ttu-id="20d9b-108">説明</span><span class="sxs-lookup"><span data-stu-id="20d9b-108">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20d9b-109">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="20d9b-109">public QueryBuildDataSource dataSource()</span></span>                      |                                                      |
| <span data-ttu-id="20d9b-110">public FieldName field()</span><span class="sxs-lookup"><span data-stu-id="20d9b-110">public FieldName field()</span></span>                                      |                                                      |
| <span data-ttu-id="20d9b-111">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="20d9b-111">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span></span> |                                                      |
| <span data-ttu-id="20d9b-112">public int status(\[int status\])</span><span class="sxs-lookup"><span data-stu-id="20d9b-112">public int status(\[int status\])</span></span>                             |                                                      |
| <span data-ttu-id="20d9b-113">public str toString()</span><span class="sxs-lookup"><span data-stu-id="20d9b-113">public str toString()</span></span>                                         | <span data-ttu-id="20d9b-114">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20d9b-114">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="20d9b-115">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20d9b-115">public str value(\[str value\])</span></span>                               |                                                      |
| <span data-ttu-id="20d9b-116">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="20d9b-116">public void finalize()</span></span>                                        |                                                      |

## <a name="method-datasource"></a><span data-ttu-id="20d9b-117">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="20d9b-117">Method dataSource</span></span>

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="20d9b-118">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="20d9b-118">Return Value - dataSource</span></span>

## <a name="method-field"></a><span data-ttu-id="20d9b-119">メソッド field</span><span class="sxs-lookup"><span data-stu-id="20d9b-119">Method field</span></span>

```xpp
public FieldName field()
```

### <a name="return-value---field"></a><span data-ttu-id="20d9b-120">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="20d9b-120">Return Value - field</span></span>

## <a name="method-rangetype"></a><span data-ttu-id="20d9b-121">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="20d9b-121">Method rangeType</span></span>

```xpp
public QueryRangeType rangeType([QueryRangeType rangeType])
```

### <a name="parameters---rangetype"></a><span data-ttu-id="20d9b-122">パラメーター - rangeType</span><span class="sxs-lookup"><span data-stu-id="20d9b-122">Parameters - rangeType</span></span>

<span data-ttu-id="20d9b-123">rangeType</span><span class="sxs-lookup"><span data-stu-id="20d9b-123">rangeType</span></span>  

### <a name="return-value---rangetype"></a><span data-ttu-id="20d9b-124">戻り値 - rangeType</span><span class="sxs-lookup"><span data-stu-id="20d9b-124">Return Value - rangeType</span></span>

## <a name="method-status"></a><span data-ttu-id="20d9b-125">メソッド status</span><span class="sxs-lookup"><span data-stu-id="20d9b-125">Method status</span></span>

```xpp
public int status([int status])
```

### <a name="parameters---status"></a><span data-ttu-id="20d9b-126">パラメーター - status</span><span class="sxs-lookup"><span data-stu-id="20d9b-126">Parameters - status</span></span>

<span data-ttu-id="20d9b-127">状態</span><span class="sxs-lookup"><span data-stu-id="20d9b-127">status</span></span>  

### <a name="return-value---status"></a><span data-ttu-id="20d9b-128">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="20d9b-128">Return Value - status</span></span>

## <a name="method-tostring"></a><span data-ttu-id="20d9b-129">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="20d9b-129">Method toString</span></span>

<span data-ttu-id="20d9b-130">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20d9b-130">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="20d9b-131">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="20d9b-131">Return Value - toString</span></span>

<span data-ttu-id="20d9b-132">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20d9b-132">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="20d9b-133">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="20d9b-133">Remarks - toString</span></span>

<span data-ttu-id="20d9b-134">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="20d9b-134">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="20d9b-135">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="20d9b-135">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="20d9b-136">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="20d9b-136">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-value"></a><span data-ttu-id="20d9b-137">メソッド value</span><span class="sxs-lookup"><span data-stu-id="20d9b-137">Method value</span></span>

```xpp
public str value([str value])
```

### <a name="parameters---value"></a><span data-ttu-id="20d9b-138">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="20d9b-138">Parameters - value</span></span>

<span data-ttu-id="20d9b-139">値</span><span class="sxs-lookup"><span data-stu-id="20d9b-139">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="20d9b-140">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="20d9b-140">Return Value - value</span></span>

## <a name="method-finalize"></a><span data-ttu-id="20d9b-141">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="20d9b-141">Method finalize</span></span>

```xpp
public void finalize()
```

