---
title: ContainerClass クラス
description: このトピックでは、ContainerClass クラスについて説明します。
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
ms.openlocfilehash: fef01fdb5faf6fa6ad52dd7b02694b3aa57639b5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502704"
---
# <a name="class-containerclass"></a><span data-ttu-id="373f5-103">クラス ContainerClass</span><span class="sxs-lookup"><span data-stu-id="373f5-103">Class ContainerClass</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ContainerClass extends Object
```

## <a name="remarks"></a><span data-ttu-id="373f5-104">備考</span><span class="sxs-lookup"><span data-stu-id="373f5-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="373f5-105">例</span><span class="sxs-lookup"><span data-stu-id="373f5-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="373f5-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="373f5-106">Methods</span></span>

| <span data-ttu-id="373f5-107">方法</span><span class="sxs-lookup"><span data-stu-id="373f5-107">Method</span></span>                                                              | <span data-ttu-id="373f5-108">説明</span><span class="sxs-lookup"><span data-stu-id="373f5-108">Description</span></span>                                          |
|---------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="373f5-109">public int length()</span><span class="sxs-lookup"><span data-stu-id="373f5-109">public int length()</span></span>                                                 |                                                      |
| <span data-ttu-id="373f5-110">public container toBlob()</span><span class="sxs-lookup"><span data-stu-id="373f5-110">public container toBlob()</span></span>                                           |                                                      |
| <span data-ttu-id="373f5-111">public str toString()</span><span class="sxs-lookup"><span data-stu-id="373f5-111">public str toString()</span></span>                                               | <span data-ttu-id="373f5-112">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="373f5-112">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="373f5-113">public container value()</span><span class="sxs-lookup"><span data-stu-id="373f5-113">public container value()</span></span>                                            |                                                      |
| <span data-ttu-id="373f5-114">::public static container blob2Container(container blob\_container)</span><span class="sxs-lookup"><span data-stu-id="373f5-114">::public static container blob2Container(container blob\_container)</span></span> |                                                      |
| <span data-ttu-id="373f5-115">::public static int containerLength(container container)</span><span class="sxs-lookup"><span data-stu-id="373f5-115">::public static int containerLength(container container)</span></span>            |                                                      |
| <span data-ttu-id="373f5-116">public void new(container container)</span><span class="sxs-lookup"><span data-stu-id="373f5-116">public void new(container container)</span></span>                                | <span data-ttu-id="373f5-117">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="373f5-117">Initializes a new instance of the Object class.</span></span>      |

## <a name="method-length"></a><span data-ttu-id="373f5-118">メソッド length</span><span class="sxs-lookup"><span data-stu-id="373f5-118">Method length</span></span>

```xpp
public int length()
```

### <a name="return-value---length"></a><span data-ttu-id="373f5-119">戻り値 - length</span><span class="sxs-lookup"><span data-stu-id="373f5-119">Return Value - length</span></span>

## <a name="method-toblob"></a><span data-ttu-id="373f5-120">メソッド toBlob</span><span class="sxs-lookup"><span data-stu-id="373f5-120">Method toBlob</span></span>

```xpp
public container toBlob()
```

### <a name="return-value---toblob"></a><span data-ttu-id="373f5-121">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="373f5-121">Return Value - toBlob</span></span>

## <a name="method-tostring"></a><span data-ttu-id="373f5-122">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="373f5-122">Method toString</span></span>

<span data-ttu-id="373f5-123">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="373f5-123">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="373f5-124">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="373f5-124">Return Value - toString</span></span>

<span data-ttu-id="373f5-125">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="373f5-125">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="373f5-126">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="373f5-126">Remarks - toString</span></span>

<span data-ttu-id="373f5-127">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="373f5-127">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="373f5-128">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="373f5-128">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="373f5-129">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="373f5-129">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-value"></a><span data-ttu-id="373f5-130">メソッド value</span><span class="sxs-lookup"><span data-stu-id="373f5-130">Method value</span></span>

```xpp
public container value()
```

### <a name="return-value---value"></a><span data-ttu-id="373f5-131">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="373f5-131">Return Value - value</span></span>

## <a name="method-blob2container"></a><span data-ttu-id="373f5-132">メソッド blob2Container</span><span class="sxs-lookup"><span data-stu-id="373f5-132">Method blob2Container</span></span>

```xpp
public static container blob2Container(container blob_container)
```

### <a name="parameters---blob2container"></a><span data-ttu-id="373f5-133">パラメーター - blob2Container</span><span class="sxs-lookup"><span data-stu-id="373f5-133">Parameters - blob2Container</span></span>

<span data-ttu-id="373f5-134">blob\_container</span><span class="sxs-lookup"><span data-stu-id="373f5-134">blob\_container</span></span>  

### <a name="return-value---blob2container"></a><span data-ttu-id="373f5-135">戻り値 - blob2Container</span><span class="sxs-lookup"><span data-stu-id="373f5-135">Return Value - blob2Container</span></span>

## <a name="method-containerlength"></a><span data-ttu-id="373f5-136">メソッド containerLength</span><span class="sxs-lookup"><span data-stu-id="373f5-136">Method containerLength</span></span>

```xpp
public static int containerLength(container container)
```

### <a name="parameters---containerlength"></a><span data-ttu-id="373f5-137">パラメーター - containerLength</span><span class="sxs-lookup"><span data-stu-id="373f5-137">Parameters - containerLength</span></span>

<span data-ttu-id="373f5-138">コンテナー</span><span class="sxs-lookup"><span data-stu-id="373f5-138">container</span></span>  

### <a name="return-value---containerlength"></a><span data-ttu-id="373f5-139">戻り値 - containerLength</span><span class="sxs-lookup"><span data-stu-id="373f5-139">Return Value - containerLength</span></span>

## <a name="method-new"></a><span data-ttu-id="373f5-140">メソッド new</span><span class="sxs-lookup"><span data-stu-id="373f5-140">Method new</span></span>

<span data-ttu-id="373f5-141">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="373f5-141">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(container container)
```

### <a name="parameters---new"></a><span data-ttu-id="373f5-142">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="373f5-142">Parameters - new</span></span>

<span data-ttu-id="373f5-143">コンテナー</span><span class="sxs-lookup"><span data-stu-id="373f5-143">container</span></span>  

