---
title: PartList クラス
description: このトピックでは、PartList クラスについて説明します。
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
ms.openlocfilehash: d95ebc00a2b19d63e4b34cce95b580ed33de657e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502537"
---
# <a name="class-partlist"></a><span data-ttu-id="891b2-103">クラス PartList</span><span class="sxs-lookup"><span data-stu-id="891b2-103">Class PartList</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PartList extends Object
```

## <a name="remarks"></a><span data-ttu-id="891b2-104">備考</span><span class="sxs-lookup"><span data-stu-id="891b2-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="891b2-105">例</span><span class="sxs-lookup"><span data-stu-id="891b2-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="891b2-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="891b2-106">Methods</span></span>

| <span data-ttu-id="891b2-107">方法</span><span class="sxs-lookup"><span data-stu-id="891b2-107">Method</span></span>                                        | <span data-ttu-id="891b2-108">説明</span><span class="sxs-lookup"><span data-stu-id="891b2-108">Description</span></span>                                     |
|-----------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="891b2-109">public xFormRun getPartById(int id)</span><span class="sxs-lookup"><span data-stu-id="891b2-109">public xFormRun getPartById(int id)</span></span>           |                                                 |
| <span data-ttu-id="891b2-110">public FormControl getPartControlById(int id)</span><span class="sxs-lookup"><span data-stu-id="891b2-110">public FormControl getPartControlById(int id)</span></span> |                                                 |
| <span data-ttu-id="891b2-111">public int partCount()</span><span class="sxs-lookup"><span data-stu-id="891b2-111">public int partCount()</span></span>                        |                                                 |
| <span data-ttu-id="891b2-112">public void new(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="891b2-112">public void new(xFormRun form)</span></span>                | <span data-ttu-id="891b2-113">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="891b2-113">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="891b2-114">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="891b2-114">public void finalize()</span></span>                        |                                                 |

## <a name="method-getpartbyid"></a><span data-ttu-id="891b2-115">メソッド getPartById</span><span class="sxs-lookup"><span data-stu-id="891b2-115">Method getPartById</span></span>

```xpp
public xFormRun getPartById(int id)
```

### <a name="parameters---getpartbyid"></a><span data-ttu-id="891b2-116">パラメーター - getPartById</span><span class="sxs-lookup"><span data-stu-id="891b2-116">Parameters - getPartById</span></span>

<span data-ttu-id="891b2-117">id</span><span class="sxs-lookup"><span data-stu-id="891b2-117">id</span></span>  

### <a name="return-value---getpartbyid"></a><span data-ttu-id="891b2-118">戻り値 - getPartById</span><span class="sxs-lookup"><span data-stu-id="891b2-118">Return Value - getPartById</span></span>

## <a name="method-getpartcontrolbyid"></a><span data-ttu-id="891b2-119">メソッド getPartControlById</span><span class="sxs-lookup"><span data-stu-id="891b2-119">Method getPartControlById</span></span>

```xpp
public FormControl getPartControlById(int id)
```

### <a name="parameters---getpartcontrolbyid"></a><span data-ttu-id="891b2-120">パラメーター - getPartControlById</span><span class="sxs-lookup"><span data-stu-id="891b2-120">Parameters - getPartControlById</span></span>

<span data-ttu-id="891b2-121">id</span><span class="sxs-lookup"><span data-stu-id="891b2-121">id</span></span>  

### <a name="return-value---getpartcontrolbyid"></a><span data-ttu-id="891b2-122">戻り値 - getPartControlById</span><span class="sxs-lookup"><span data-stu-id="891b2-122">Return Value - getPartControlById</span></span>

## <a name="method-partcount"></a><span data-ttu-id="891b2-123">メソッド partCount</span><span class="sxs-lookup"><span data-stu-id="891b2-123">Method partCount</span></span>

```xpp
public int partCount()
```

### <a name="return-value---partcount"></a><span data-ttu-id="891b2-124">戻り値 - partCount</span><span class="sxs-lookup"><span data-stu-id="891b2-124">Return Value - partCount</span></span>

## <a name="method-new"></a><span data-ttu-id="891b2-125">メソッド new</span><span class="sxs-lookup"><span data-stu-id="891b2-125">Method new</span></span>

<span data-ttu-id="891b2-126">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="891b2-126">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(xFormRun form)
```

### <a name="parameters---new"></a><span data-ttu-id="891b2-127">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="891b2-127">Parameters - new</span></span>

<span data-ttu-id="891b2-128">フォーム</span><span class="sxs-lookup"><span data-stu-id="891b2-128">form</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="891b2-129">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="891b2-129">Method finalize</span></span>

```xpp
public void finalize()
```

