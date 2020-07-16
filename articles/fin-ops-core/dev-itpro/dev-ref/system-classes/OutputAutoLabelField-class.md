---
title: OutputAutoLabelField クラス
description: このトピックでは、OutputAutoLabelField クラスについて説明します。
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
ms.openlocfilehash: 83f4aa9bbada5797c8946614267df76458afae94
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502559"
---
# <a name="class-outputautolabelfield"></a><span data-ttu-id="23b69-103">クラス OutputAutoLabelField</span><span class="sxs-lookup"><span data-stu-id="23b69-103">Class OutputAutoLabelField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OutputAutoLabelField extends OutputField
```

## <a name="remarks"></a><span data-ttu-id="23b69-104">備考</span><span class="sxs-lookup"><span data-stu-id="23b69-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="23b69-105">例</span><span class="sxs-lookup"><span data-stu-id="23b69-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="23b69-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="23b69-106">Methods</span></span>

| <span data-ttu-id="23b69-107">方法</span><span class="sxs-lookup"><span data-stu-id="23b69-107">Method</span></span>                  | <span data-ttu-id="23b69-108">説明</span><span class="sxs-lookup"><span data-stu-id="23b69-108">Description</span></span>                                                   |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="23b69-109">public boolean leadIn()</span><span class="sxs-lookup"><span data-stu-id="23b69-109">public boolean leadIn()</span></span> |                                                               |
| <span data-ttu-id="23b69-110">public str toString()</span><span class="sxs-lookup"><span data-stu-id="23b69-110">public str toString()</span></span>   | <span data-ttu-id="23b69-111">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="23b69-111">Returns a string that represents the current object.</span></span>          |
| <span data-ttu-id="23b69-112">public str value()</span><span class="sxs-lookup"><span data-stu-id="23b69-112">public str value()</span></span>      |                                                               |
| <span data-ttu-id="23b69-113">public void new()</span><span class="sxs-lookup"><span data-stu-id="23b69-113">public void new()</span></span>       | <span data-ttu-id="23b69-114">OutputAutoLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="23b69-114">Initializes a new instance of the OutputAutoLabelField class.</span></span> |

## <a name="method-leadin"></a><span data-ttu-id="23b69-115">メソッド leadIn</span><span class="sxs-lookup"><span data-stu-id="23b69-115">Method leadIn</span></span>

```xpp
public boolean leadIn()
```

### <a name="return-value---leadin"></a><span data-ttu-id="23b69-116">戻り値 - leadIn</span><span class="sxs-lookup"><span data-stu-id="23b69-116">Return Value - leadIn</span></span>

## <a name="method-tostring"></a><span data-ttu-id="23b69-117">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="23b69-117">Method toString</span></span>

<span data-ttu-id="23b69-118">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="23b69-118">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="23b69-119">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="23b69-119">Return Value - toString</span></span>

<span data-ttu-id="23b69-120">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="23b69-120">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="23b69-121">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="23b69-121">Remarks - toString</span></span>

<span data-ttu-id="23b69-122">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="23b69-122">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="23b69-123">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="23b69-123">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="23b69-124">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="23b69-124">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

## <a name="method-value"></a><span data-ttu-id="23b69-125">メソッド value</span><span class="sxs-lookup"><span data-stu-id="23b69-125">Method value</span></span>

```xpp
public str value()
```

### <a name="return-value---value"></a><span data-ttu-id="23b69-126">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="23b69-126">Return Value - value</span></span>

## <a name="method-new"></a><span data-ttu-id="23b69-127">メソッド new</span><span class="sxs-lookup"><span data-stu-id="23b69-127">Method new</span></span>

<span data-ttu-id="23b69-128">OutputAutoLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="23b69-128">Initializes a new instance of the OutputAutoLabelField class.</span></span>

```xpp
public void new()
```

