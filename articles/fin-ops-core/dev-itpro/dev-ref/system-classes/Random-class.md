---
title: Random クラス
description: このトピックでは、Random クラスについて説明します。
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
ms.openlocfilehash: e2203d2f8d3ecfb952e5a77e2cb4d5077115ad45
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502857"
---
# <a name="class-random"></a><span data-ttu-id="5f403-103">クラス ランダム</span><span class="sxs-lookup"><span data-stu-id="5f403-103">Class Random</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Random extends Object
```

<span data-ttu-id="5f403-104">Random クラスは、ランダムな番号を生成します。</span><span class="sxs-lookup"><span data-stu-id="5f403-104">The Random class generates random numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f403-105">備考</span><span class="sxs-lookup"><span data-stu-id="5f403-105">Remarks</span></span>

<span data-ttu-id="5f403-106">このクラスはグローバル ランダム ジェネレーターで機能するため、個々のランダム オブジェクトは相互に干渉します。</span><span class="sxs-lookup"><span data-stu-id="5f403-106">Because this class operates on a global random generator, the individual random objects will interfere with each other.</span></span> <span data-ttu-id="5f403-107">したがって、特定のランダム オブジェクトの数列を予測することはできません。</span><span class="sxs-lookup"><span data-stu-id="5f403-107">Therefore, it is not possible to predict the sequence of numbers for a specific random object.</span></span>

## <a name="examples"></a><span data-ttu-id="5f403-108">例</span><span class="sxs-lookup"><span data-stu-id="5f403-108">Examples</span></span>

<span data-ttu-id="5f403-109">次の例では、100 個のランダムな番号を出力します。</span><span class="sxs-lookup"><span data-stu-id="5f403-109">The following example prints 100 random numbers.</span></span>

```xpp
static void example() 
{ 
    Random myRand = new Random(); 
    int i; 
    for(i=0;i<100;i++) 
    { 
        print myRand.nextInt(); 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="5f403-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="5f403-110">Methods</span></span>

| <span data-ttu-id="5f403-111">方法</span><span class="sxs-lookup"><span data-stu-id="5f403-111">Method</span></span>               | <span data-ttu-id="5f403-112">説明</span><span class="sxs-lookup"><span data-stu-id="5f403-112">Description</span></span>                                               |
|----------------------|-----------------------------------------------------------|
| <span data-ttu-id="5f403-113">public int nextInt()</span><span class="sxs-lookup"><span data-stu-id="5f403-113">public int nextInt()</span></span> | <span data-ttu-id="5f403-114">ランダム ジェネレーターの次のランダムな数を返します。</span><span class="sxs-lookup"><span data-stu-id="5f403-114">Returns the next random number from the random generator.</span></span> |
| <span data-ttu-id="5f403-115">public void new()</span><span class="sxs-lookup"><span data-stu-id="5f403-115">public void new()</span></span>    | <span data-ttu-id="5f403-116">Random クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5f403-116">Initializes a new instance of the Random class.</span></span>           |

## <a name="method-nextint"></a><span data-ttu-id="5f403-117">メソッド nextInt</span><span class="sxs-lookup"><span data-stu-id="5f403-117">Method nextInt</span></span>

<span data-ttu-id="5f403-118">ランダム ジェネレーターの次のランダムな数を返します。</span><span class="sxs-lookup"><span data-stu-id="5f403-118">Returns the next random number from the random generator.</span></span>

```xpp
public int nextInt()
```

### <a name="return-value---nextint"></a><span data-ttu-id="5f403-119">戻り値 - nextInt</span><span class="sxs-lookup"><span data-stu-id="5f403-119">Return Value - nextInt</span></span>

<span data-ttu-id="5f403-120">ランダム ジェネレーターの次のランダムな整数。</span><span class="sxs-lookup"><span data-stu-id="5f403-120">The next random integer number from the random generator.</span></span>

### <a name="remarks---nextint"></a><span data-ttu-id="5f403-121">備考 - nextInt</span><span class="sxs-lookup"><span data-stu-id="5f403-121">Remarks - nextInt</span></span>

<span data-ttu-id="5f403-122">値は 0 〜 32767 (0x7FFF) の範囲内になります。</span><span class="sxs-lookup"><span data-stu-id="5f403-122">The value will be in the range from 0 to 32767 (0x7FFF).</span></span>

## <a name="method-new"></a><span data-ttu-id="5f403-123">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5f403-123">Method new</span></span>

<span data-ttu-id="5f403-124">Random クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5f403-124">Initializes a new instance of the Random class.</span></span>

```xpp
public void new()
```

