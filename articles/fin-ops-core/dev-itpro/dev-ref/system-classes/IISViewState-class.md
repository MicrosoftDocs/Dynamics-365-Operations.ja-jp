---
title: IISViewState クラス
description: このトピックでは、IISViewState クラスについて説明します。
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
ms.openlocfilehash: df5acdeb301ed7881515d8f5a4d8da9f2667acc1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502903"
---
# <a name="class-iisviewstate"></a><span data-ttu-id="0bf9f-103">クラス IISViewState</span><span class="sxs-lookup"><span data-stu-id="0bf9f-103">Class IISViewState</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISViewState extends Object
```

## <a name="remarks"></a><span data-ttu-id="0bf9f-104">備考</span><span class="sxs-lookup"><span data-stu-id="0bf9f-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="0bf9f-105">例</span><span class="sxs-lookup"><span data-stu-id="0bf9f-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="0bf9f-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="0bf9f-106">Methods</span></span>

| <span data-ttu-id="0bf9f-107">方法</span><span class="sxs-lookup"><span data-stu-id="0bf9f-107">Method</span></span>                                         | <span data-ttu-id="0bf9f-108">説明</span><span class="sxs-lookup"><span data-stu-id="0bf9f-108">Description</span></span>                                           |
|------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="0bf9f-109">public boolean viewStateContains(str key)</span><span class="sxs-lookup"><span data-stu-id="0bf9f-109">public boolean viewStateContains(str key)</span></span>      |                                                       |
| <span data-ttu-id="0bf9f-110">public str viewStateItem(str key, \[str val\])</span><span class="sxs-lookup"><span data-stu-id="0bf9f-110">public str viewStateItem(str key, \[str val\])</span></span> |                                                       |
| <span data-ttu-id="0bf9f-111">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="0bf9f-111">public void finalize()</span></span>                         |                                                       |
| <span data-ttu-id="0bf9f-112">public void viewStateDelete(str key)</span><span class="sxs-lookup"><span data-stu-id="0bf9f-112">public void viewStateDelete(str key)</span></span>           |                                                       |
| <span data-ttu-id="0bf9f-113">public void new()</span><span class="sxs-lookup"><span data-stu-id="0bf9f-113">public void new()</span></span>                              | <span data-ttu-id="0bf9f-114">IISViewState クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0bf9f-114">Initializes a new instance of the IISViewState class.</span></span> |

## <a name="method-viewstatecontains"></a><span data-ttu-id="0bf9f-115">メソッド viewStateContains</span><span class="sxs-lookup"><span data-stu-id="0bf9f-115">Method viewStateContains</span></span>

```xpp
public boolean viewStateContains(str key)
```

### <a name="parameters---viewstatecontains"></a><span data-ttu-id="0bf9f-116">パラメーター - viewStateContains</span><span class="sxs-lookup"><span data-stu-id="0bf9f-116">Parameters - viewStateContains</span></span>

<span data-ttu-id="0bf9f-117">キー</span><span class="sxs-lookup"><span data-stu-id="0bf9f-117">key</span></span>  

### <a name="return-value---viewstatecontains"></a><span data-ttu-id="0bf9f-118">戻り値 - viewStateContains</span><span class="sxs-lookup"><span data-stu-id="0bf9f-118">Return Value - viewStateContains</span></span>

## <a name="method-viewstateitem"></a><span data-ttu-id="0bf9f-119">メソッド viewStateItem</span><span class="sxs-lookup"><span data-stu-id="0bf9f-119">Method viewStateItem</span></span>

```xpp
public str viewStateItem(str key, [str val])
```

### <a name="parameters---viewstateitem"></a><span data-ttu-id="0bf9f-120">パラメーター - viewStateItem</span><span class="sxs-lookup"><span data-stu-id="0bf9f-120">Parameters - viewStateItem</span></span>

<span data-ttu-id="0bf9f-121">キー</span><span class="sxs-lookup"><span data-stu-id="0bf9f-121">key</span></span>  

<!-- -->

<span data-ttu-id="0bf9f-122">val</span><span class="sxs-lookup"><span data-stu-id="0bf9f-122">val</span></span>  

### <a name="return-value---viewstateitem"></a><span data-ttu-id="0bf9f-123">戻り値 - viewStateItem</span><span class="sxs-lookup"><span data-stu-id="0bf9f-123">Return Value - viewStateItem</span></span>

## <a name="method-finalize"></a><span data-ttu-id="0bf9f-124">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="0bf9f-124">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-viewstatedelete"></a><span data-ttu-id="0bf9f-125">メソッド viewStateDelete</span><span class="sxs-lookup"><span data-stu-id="0bf9f-125">Method viewStateDelete</span></span>

```xpp
public void viewStateDelete(str key)
```

### <a name="parameters---viewstatedelete"></a><span data-ttu-id="0bf9f-126">パラメーター - viewStateDelete</span><span class="sxs-lookup"><span data-stu-id="0bf9f-126">Parameters - viewStateDelete</span></span>

<span data-ttu-id="0bf9f-127">キー</span><span class="sxs-lookup"><span data-stu-id="0bf9f-127">key</span></span>  

## <a name="method-new"></a><span data-ttu-id="0bf9f-128">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0bf9f-128">Method new</span></span>

<span data-ttu-id="0bf9f-129">IISViewState クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0bf9f-129">Initializes a new instance of the IISViewState class.</span></span>

```xpp
public void new()
```

