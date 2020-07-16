---
title: OutputDateField クラス
description: このトピックでは、OutputDateField クラスについて説明します。
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
ms.openlocfilehash: 419d82635f8fc35117dc4b8a0015bc7cad466e21
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502553"
---
# <a name="class-outputdatefield"></a><span data-ttu-id="6a81d-103">クラス OutputDateField</span><span class="sxs-lookup"><span data-stu-id="6a81d-103">Class OutputDateField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OutputDateField extends OutputField
```

## <a name="remarks"></a><span data-ttu-id="6a81d-104">備考</span><span class="sxs-lookup"><span data-stu-id="6a81d-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="6a81d-105">例</span><span class="sxs-lookup"><span data-stu-id="6a81d-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6a81d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="6a81d-106">Methods</span></span>

| <span data-ttu-id="6a81d-107">方法</span><span class="sxs-lookup"><span data-stu-id="6a81d-107">Method</span></span>                | <span data-ttu-id="6a81d-108">説明</span><span class="sxs-lookup"><span data-stu-id="6a81d-108">Description</span></span>                                              |
|-----------------------|----------------------------------------------------------|
| <span data-ttu-id="6a81d-109">public str toString()</span><span class="sxs-lookup"><span data-stu-id="6a81d-109">public str toString()</span></span> | <span data-ttu-id="6a81d-110">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6a81d-110">Returns a string that represents the current object.</span></span>     |
| <span data-ttu-id="6a81d-111">public Date value()</span><span class="sxs-lookup"><span data-stu-id="6a81d-111">public Date value()</span></span>   |                                                          |
| <span data-ttu-id="6a81d-112">public void new()</span><span class="sxs-lookup"><span data-stu-id="6a81d-112">public void new()</span></span>     | <span data-ttu-id="6a81d-113">OutputDateField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6a81d-113">Initializes a new instance of the OutputDateField class.</span></span> |

## <a name="method-tostring"></a><span data-ttu-id="6a81d-114">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="6a81d-114">Method toString</span></span>

<span data-ttu-id="6a81d-115">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6a81d-115">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="6a81d-116">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="6a81d-116">Return Value - toString</span></span>

<span data-ttu-id="6a81d-117">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6a81d-117">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="6a81d-118">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="6a81d-118">Remarks - toString</span></span>

<span data-ttu-id="6a81d-119">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="6a81d-119">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="6a81d-120">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6a81d-120">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="6a81d-121">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="6a81d-121">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

## <a name="method-value"></a><span data-ttu-id="6a81d-122">メソッド value</span><span class="sxs-lookup"><span data-stu-id="6a81d-122">Method value</span></span>

```xpp
public Date value()
```

### <a name="return-value---value"></a><span data-ttu-id="6a81d-123">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="6a81d-123">Return Value - value</span></span>

## <a name="method-new"></a><span data-ttu-id="6a81d-124">メソッド new</span><span class="sxs-lookup"><span data-stu-id="6a81d-124">Method new</span></span>

<span data-ttu-id="6a81d-125">OutputDateField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6a81d-125">Initializes a new instance of the OutputDateField class.</span></span>

```xpp
public void new()
```

