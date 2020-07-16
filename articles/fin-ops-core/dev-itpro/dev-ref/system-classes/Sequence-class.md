---
title: Sequence クラス
description: このトピックでは、Sequence クラスについて説明します。
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
ms.openlocfilehash: 0e656a131b2058f8f155d42a4ace5bc578221894
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502806"
---
# <a name="class-sequence"></a><span data-ttu-id="35c21-103">クラスの順序</span><span class="sxs-lookup"><span data-stu-id="35c21-103">Class Sequence</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Sequence extends Object
```

<span data-ttu-id="35c21-104">Sequence クラスを使用すると、通常は何らかの順序または伝票番号の生成のために、主要なトランザクション スコープ外でトランザクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="35c21-104">The Sequence class lets you perform transactions outside the main transaction scope, typically for some kind of sequence, or voucher number generation.</span></span>

## <a name="remarks"></a><span data-ttu-id="35c21-105">備考</span><span class="sxs-lookup"><span data-stu-id="35c21-105">Remarks</span></span>

<span data-ttu-id="35c21-106">接続には、メインユーザー接続、補助システム接続、ユーザー接続の 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="35c21-106">There are three kinds of connections: The main user connection, an auxiliary system connection, and user connections.</span></span> <span data-ttu-id="35c21-107">最初のものはアプリケーション ロジック用に使用されます。</span><span class="sxs-lookup"><span data-stu-id="35c21-107">The first is used for the application logic.</span></span> <span data-ttu-id="35c21-108">2 番目は、内部シーケンス番号の生成 (特に組み込みフィールド RecId) に使用されます。</span><span class="sxs-lookup"><span data-stu-id="35c21-108">The second is used for internal sequence number generation (specifically the built-in field RecId).</span></span> <span data-ttu-id="35c21-109">3 番目はアプリケーションが別々の接続を維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="35c21-109">The third is used for the application maintained separate connections.</span></span> <span data-ttu-id="35c21-110">このクラスは、番号生成のための補助システム接続へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="35c21-110">This class provides an interface to the auxiliary system connection for number generation.</span></span> <span data-ttu-id="35c21-111">ただし、これはアプリケーションの使用するメソッドまたは柔軟性、さらにカーネルの順序番号の生成で同時実行の問題を回避するため、UserConnection クラスを使用する方がより良いソリューションになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="35c21-111">However, it may be a better solution to use the UserConnection class, as this is the method the application uses or flexibility, and to avoid concurrency problems with the kernel's sequence number generation.</span></span>

## <a name="examples"></a><span data-ttu-id="35c21-112">例</span><span class="sxs-lookup"><span data-stu-id="35c21-112">Examples</span></span>

```xpp
static void example() 
{ 
    Sequence S = new Sequence("mySequence",1,100,10000); 
    print S.nextval(10);           // 100 in current company (the subkey) 
    print S.nextval(10);           // 110 in current company (the subkey) 
    print S.nextval(1,"MMM");      // 100 in subkey "MMM" 
    print S.nextval(1,"MMM");      // 101 in subkey "MMM" 
}
```

## <a name="methods"></a><span data-ttu-id="35c21-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="35c21-113">Methods</span></span>

| <span data-ttu-id="35c21-114">方法</span><span class="sxs-lookup"><span data-stu-id="35c21-114">Method</span></span>                                                                                                        | <span data-ttu-id="35c21-115">説明</span><span class="sxs-lookup"><span data-stu-id="35c21-115">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c21-116">public Int64 currval(\[str Subkey1\], \[int Subkey2\])</span><span class="sxs-lookup"><span data-stu-id="35c21-116">public Int64 currval(\[str Subkey1\], \[int Subkey2\])</span></span>                                                        | <span data-ttu-id="35c21-117">カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="35c21-117">Gets the current sequence number from the sequence, without incrementing the counter value.</span></span> |
| <span data-ttu-id="35c21-118">public Int64 nextval(Int64 Increment, \[str Subkey1\], \[int Subkey2\])</span><span class="sxs-lookup"><span data-stu-id="35c21-118">public Int64 nextval(Int64 Increment, \[str Subkey1\], \[int Subkey2\])</span></span>                                       | <span data-ttu-id="35c21-119">シーケンスから次の順序番号を返し、カウンター値を増分します。</span><span class="sxs-lookup"><span data-stu-id="35c21-119">Returns the next sequence number from the sequence and then increments the counter value.</span></span>   |
| <span data-ttu-id="35c21-120">public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, \[boolean Cycle\], \[Int64 CacheSize\])</span><span class="sxs-lookup"><span data-stu-id="35c21-120">public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, \[boolean Cycle\], \[Int64 CacheSize\])</span></span> | <span data-ttu-id="35c21-121">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35c21-121">Initializes a new instance of the Object class.</span></span>                                             |

## <a name="method-currval"></a><span data-ttu-id="35c21-122">メソッド currval</span><span class="sxs-lookup"><span data-stu-id="35c21-122">Method currval</span></span>

<span data-ttu-id="35c21-123">カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="35c21-123">Gets the current sequence number from the sequence, without incrementing the counter value.</span></span>

```xpp
public Int64 currval([str Subkey1], [int Subkey2])
```

### <a name="parameters---currval"></a><span data-ttu-id="35c21-124">パラメーター - currval</span><span class="sxs-lookup"><span data-stu-id="35c21-124">Parameters - currval</span></span>

<span data-ttu-id="35c21-125">Subkey1</span><span class="sxs-lookup"><span data-stu-id="35c21-125">Subkey1</span></span>  

<!-- -->

<span data-ttu-id="35c21-126">Subkey2</span><span class="sxs-lookup"><span data-stu-id="35c21-126">Subkey2</span></span>  

### <a name="return-value---currval"></a><span data-ttu-id="35c21-127">戻り値 - currval</span><span class="sxs-lookup"><span data-stu-id="35c21-127">Return Value - currval</span></span>

<span data-ttu-id="35c21-128">シーケンスの現在のシーケンス番号。</span><span class="sxs-lookup"><span data-stu-id="35c21-128">The current sequence number from the sequence.</span></span>

## <a name="method-nextval"></a><span data-ttu-id="35c21-129">メソッド nextval</span><span class="sxs-lookup"><span data-stu-id="35c21-129">Method nextval</span></span>

<span data-ttu-id="35c21-130">シーケンスから次の順序番号を返し、カウンター値を増分します。</span><span class="sxs-lookup"><span data-stu-id="35c21-130">Returns the next sequence number from the sequence and then increments the counter value.</span></span>

```xpp
public Int64 nextval(Int64 Increment, [str Subkey1], [int Subkey2])
```

### <a name="parameters---nextval"></a><span data-ttu-id="35c21-131">パラメーター - nextval</span><span class="sxs-lookup"><span data-stu-id="35c21-131">Parameters - nextval</span></span>

<span data-ttu-id="35c21-132">増分</span><span class="sxs-lookup"><span data-stu-id="35c21-132">Increment</span></span>  

<!-- -->

<span data-ttu-id="35c21-133">Subkey1</span><span class="sxs-lookup"><span data-stu-id="35c21-133">Subkey1</span></span>  

<!-- -->

<span data-ttu-id="35c21-134">Subkey2</span><span class="sxs-lookup"><span data-stu-id="35c21-134">Subkey2</span></span>  

### <a name="return-value---nextval"></a><span data-ttu-id="35c21-135">戻り値 - nextval</span><span class="sxs-lookup"><span data-stu-id="35c21-135">Return Value - nextval</span></span>

<span data-ttu-id="35c21-136">利用可能な次の順序番号。</span><span class="sxs-lookup"><span data-stu-id="35c21-136">The next sequence number available.</span></span>

## <a name="method-new"></a><span data-ttu-id="35c21-137">メソッド new</span><span class="sxs-lookup"><span data-stu-id="35c21-137">Method new</span></span>

<span data-ttu-id="35c21-138">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35c21-138">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, [boolean Cycle], [Int64 CacheSize])
```

### <a name="parameters---new"></a><span data-ttu-id="35c21-139">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="35c21-139">Parameters - new</span></span>

<span data-ttu-id="35c21-140">氏名</span><span class="sxs-lookup"><span data-stu-id="35c21-140">Name</span></span>  

<!-- -->

<span data-ttu-id="35c21-141">ID</span><span class="sxs-lookup"><span data-stu-id="35c21-141">Id</span></span>  

<!-- -->

<span data-ttu-id="35c21-142">InitialValue</span><span class="sxs-lookup"><span data-stu-id="35c21-142">InitialValue</span></span>  

<!-- -->

<span data-ttu-id="35c21-143">MaxValue</span><span class="sxs-lookup"><span data-stu-id="35c21-143">MaxValue</span></span>  

<!-- -->

<span data-ttu-id="35c21-144">サイクル</span><span class="sxs-lookup"><span data-stu-id="35c21-144">Cycle</span></span>  

<!-- -->

<span data-ttu-id="35c21-145">CacheSize</span><span class="sxs-lookup"><span data-stu-id="35c21-145">CacheSize</span></span>  

