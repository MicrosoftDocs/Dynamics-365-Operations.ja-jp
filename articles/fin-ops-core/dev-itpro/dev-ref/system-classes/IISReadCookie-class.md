---
title: IISReadCookie クラス
description: このトピックでは、IISReadCookie クラスについて説明します。
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
ms.openlocfilehash: ecb916ae72e70b622006a1f838cd1f65187eb789
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502906"
---
# <a name="class-iisreadcookie"></a><span data-ttu-id="16b10-103">クラス IISReadCookie</span><span class="sxs-lookup"><span data-stu-id="16b10-103">Class IISReadCookie</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISReadCookie extends Object
```

<span data-ttu-id="16b10-104">IISReadCookie クラスは、インターネット インフォメーション サービス (IIS) によって提供される ReadCookie オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="16b10-104">The IISReadCookie class wraps the ReadCookie object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="16b10-105">備考</span><span class="sxs-lookup"><span data-stu-id="16b10-105">Remarks</span></span>

<span data-ttu-id="16b10-106">IISReadCookie クラスのメソッドと、IIS によって提供される ReadCookie オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="16b10-106">There is a one-to-one connection between the methods of the IISReadCookie class and the methods of the ReadCookie object that is offered by IIS.</span></span> <span data-ttu-id="16b10-107">したがって、IISReadCookie クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="16b10-107">Therefore, for more information about the methods of the IISReadCookie class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="16b10-108">IISReadCookie クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="16b10-108">Use of the IISReadCookie class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="16b10-109">例</span><span class="sxs-lookup"><span data-stu-id="16b10-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="16b10-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="16b10-110">Methods</span></span>

| <span data-ttu-id="16b10-111">方法</span><span class="sxs-lookup"><span data-stu-id="16b10-111">Method</span></span>                           | <span data-ttu-id="16b10-112">説明</span><span class="sxs-lookup"><span data-stu-id="16b10-112">Description</span></span>                                     |
|----------------------------------|-------------------------------------------------|
| <span data-ttu-id="16b10-113">public int count()</span><span class="sxs-lookup"><span data-stu-id="16b10-113">public int count()</span></span>               |                                                 |
| <span data-ttu-id="16b10-114">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="16b10-114">public COMEnum2Variant getEnum()</span></span> |                                                 |
| <span data-ttu-id="16b10-115">public boolean hasKeys()</span><span class="sxs-lookup"><span data-stu-id="16b10-115">public boolean hasKeys()</span></span>         |                                                 |
| <span data-ttu-id="16b10-116">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="16b10-116">public ComInterface interface()</span></span>  |                                                 |
| <span data-ttu-id="16b10-117">public str item(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="16b10-117">public str item(\[str item\])</span></span>    |                                                 |
| <span data-ttu-id="16b10-118">public str key(str key)</span><span class="sxs-lookup"><span data-stu-id="16b10-118">public str key(str key)</span></span>          |                                                 |
| <span data-ttu-id="16b10-119">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="16b10-119">public void finalize()</span></span>           |                                                 |
| <span data-ttu-id="16b10-120">public void new(COM readCookie)</span><span class="sxs-lookup"><span data-stu-id="16b10-120">public void new(COM readCookie)</span></span>  | <span data-ttu-id="16b10-121">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="16b10-121">Initializes a new instance of the Object class.</span></span> |

## <a name="method-count"></a><span data-ttu-id="16b10-122">メソッド count</span><span class="sxs-lookup"><span data-stu-id="16b10-122">Method count</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="16b10-123">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="16b10-123">Return Value - count</span></span>

## <a name="method-getenum"></a><span data-ttu-id="16b10-124">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="16b10-124">Method getEnum</span></span>

```xpp
public COMEnum2Variant getEnum()
```

### <a name="return-value---getenum"></a><span data-ttu-id="16b10-125">戻り値 - getEnum</span><span class="sxs-lookup"><span data-stu-id="16b10-125">Return Value - getEnum</span></span>

## <a name="method-haskeys"></a><span data-ttu-id="16b10-126">メソッド hasKeys</span><span class="sxs-lookup"><span data-stu-id="16b10-126">Method hasKeys</span></span>

```xpp
public boolean hasKeys()
```

### <a name="return-value---haskeys"></a><span data-ttu-id="16b10-127">戻り値 - hasKeys</span><span class="sxs-lookup"><span data-stu-id="16b10-127">Return Value - hasKeys</span></span>

## <a name="method-interface"></a><span data-ttu-id="16b10-128">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="16b10-128">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="16b10-129">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="16b10-129">Return Value - interface</span></span>

## <a name="method-item"></a><span data-ttu-id="16b10-130">メソッド item</span><span class="sxs-lookup"><span data-stu-id="16b10-130">Method item</span></span>

```xpp
public str item([str item])
```

### <a name="parameters---item"></a><span data-ttu-id="16b10-131">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="16b10-131">Parameters - item</span></span>

<span data-ttu-id="16b10-132">品目</span><span class="sxs-lookup"><span data-stu-id="16b10-132">item</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="16b10-133">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="16b10-133">Return Value - item</span></span>

## <a name="method-key"></a><span data-ttu-id="16b10-134">メソッド key</span><span class="sxs-lookup"><span data-stu-id="16b10-134">Method key</span></span>

```xpp
public str key(str key)
```

### <a name="parameters---key"></a><span data-ttu-id="16b10-135">パラメーター - key</span><span class="sxs-lookup"><span data-stu-id="16b10-135">Parameters - key</span></span>

<span data-ttu-id="16b10-136">キー</span><span class="sxs-lookup"><span data-stu-id="16b10-136">key</span></span>  

### <a name="return-value---key"></a><span data-ttu-id="16b10-137">戻り値 - key</span><span class="sxs-lookup"><span data-stu-id="16b10-137">Return Value - key</span></span>

## <a name="method-finalize"></a><span data-ttu-id="16b10-138">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="16b10-138">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="16b10-139">メソッド new</span><span class="sxs-lookup"><span data-stu-id="16b10-139">Method new</span></span>

<span data-ttu-id="16b10-140">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="16b10-140">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(COM readCookie)
```

### <a name="parameters---new"></a><span data-ttu-id="16b10-141">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="16b10-141">Parameters - new</span></span>

<span data-ttu-id="16b10-142">readCookie</span><span class="sxs-lookup"><span data-stu-id="16b10-142">readCookie</span></span>  

