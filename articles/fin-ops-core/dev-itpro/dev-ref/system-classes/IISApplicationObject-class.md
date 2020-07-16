---
title: IISApplicationObject クラス
description: このトピックでは、IISApplicationObject クラスについて説明します。
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
ms.openlocfilehash: 484ac76d5c519fb6d20d2e4fa48bdea52580d2c0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502605"
---
# <a name="class-iisapplicationobject"></a><span data-ttu-id="9d453-103">クラス IISApplicationObject</span><span class="sxs-lookup"><span data-stu-id="9d453-103">Class IISApplicationObject</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISApplicationObject extends Object
```

<span data-ttu-id="9d453-104">IISApplicationObject クラスは、インターネット インフォメーション サービス (IIS) によって提供されるアプリケーション オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="9d453-104">The IISApplicationObject class wraps the Application object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d453-105">備考</span><span class="sxs-lookup"><span data-stu-id="9d453-105">Remarks</span></span>

<span data-ttu-id="9d453-106">IISApplicationObject クラスのメソッドと、IIS によって提供される Application オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="9d453-106">There is a one-to-one connection between the methods of the IISApplicationObject class and the methods of the Application object that is offered by IIS.</span></span> <span data-ttu-id="9d453-107">したがって、IISApplicationObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d453-107">Therefore, for more information about the methods of the IISApplicationObject class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="9d453-108">IISApplicationObject クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="9d453-108">Use of the IISApplicationObject class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="9d453-109">例</span><span class="sxs-lookup"><span data-stu-id="9d453-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9d453-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="9d453-110">Methods</span></span>

| <span data-ttu-id="9d453-111">方法</span><span class="sxs-lookup"><span data-stu-id="9d453-111">Method</span></span>                                                 | <span data-ttu-id="9d453-112">説明</span><span class="sxs-lookup"><span data-stu-id="9d453-112">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9d453-113">public IISVariantDictionary contents()</span><span class="sxs-lookup"><span data-stu-id="9d453-113">public IISVariantDictionary contents()</span></span>                 |                                                               |
| <span data-ttu-id="9d453-114">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="9d453-114">public ComInterface interface()</span></span>                        |                                                               |
| <span data-ttu-id="9d453-115">public IISVariantDictionary staticObjects()</span><span class="sxs-lookup"><span data-stu-id="9d453-115">public IISVariantDictionary staticObjects()</span></span>            |                                                               |
| <span data-ttu-id="9d453-116">public COMVariant value(str value, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="9d453-116">public COMVariant value(str value, \[COMVariant var\])</span></span> |                                                               |
| <span data-ttu-id="9d453-117">public str valueTxt(str value, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="9d453-117">public str valueTxt(str value, \[str var\])</span></span>            |                                                               |
| <span data-ttu-id="9d453-118">public void new()</span><span class="sxs-lookup"><span data-stu-id="9d453-118">public void new()</span></span>                                      | <span data-ttu-id="9d453-119">IISApplicationObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9d453-119">Initializes a new instance of the IISApplicationObject class.</span></span> |
| <span data-ttu-id="9d453-120">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="9d453-120">public void finalize()</span></span>                                 |                                                               |
| <span data-ttu-id="9d453-121">public void lock()</span><span class="sxs-lookup"><span data-stu-id="9d453-121">public void lock()</span></span>                                     |                                                               |
| <span data-ttu-id="9d453-122">public void unLock()</span><span class="sxs-lookup"><span data-stu-id="9d453-122">public void unLock()</span></span>                                   |                                                               |

## <a name="method-contents"></a><span data-ttu-id="9d453-123">メソッド contents</span><span class="sxs-lookup"><span data-stu-id="9d453-123">Method contents</span></span>

```xpp
public IISVariantDictionary contents()
```

### <a name="return-value---contents"></a><span data-ttu-id="9d453-124">戻り値 - contents</span><span class="sxs-lookup"><span data-stu-id="9d453-124">Return Value - contents</span></span>

## <a name="method-interface"></a><span data-ttu-id="9d453-125">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="9d453-125">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="9d453-126">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="9d453-126">Return Value - interface</span></span>

## <a name="method-staticobjects"></a><span data-ttu-id="9d453-127">メソッド staticObjects</span><span class="sxs-lookup"><span data-stu-id="9d453-127">Method staticObjects</span></span>

```xpp
public IISVariantDictionary staticObjects()
```

### <a name="return-value---staticobjects"></a><span data-ttu-id="9d453-128">戻り値 - staticObjects</span><span class="sxs-lookup"><span data-stu-id="9d453-128">Return Value - staticObjects</span></span>

## <a name="method-value"></a><span data-ttu-id="9d453-129">メソッド value</span><span class="sxs-lookup"><span data-stu-id="9d453-129">Method value</span></span>

```xpp
public COMVariant value(str value, [COMVariant var])
```

### <a name="parameters---value"></a><span data-ttu-id="9d453-130">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="9d453-130">Parameters - value</span></span>

<span data-ttu-id="9d453-131">値</span><span class="sxs-lookup"><span data-stu-id="9d453-131">value</span></span>  

<!-- -->

<span data-ttu-id="9d453-132">var</span><span class="sxs-lookup"><span data-stu-id="9d453-132">var</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="9d453-133">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="9d453-133">Return Value - value</span></span>

## <a name="method-valuetxt"></a><span data-ttu-id="9d453-134">メソッド valueTxt</span><span class="sxs-lookup"><span data-stu-id="9d453-134">Method valueTxt</span></span>

```xpp
public str valueTxt(str value, [str var])
```

### <a name="parameters---valuetxt"></a><span data-ttu-id="9d453-135">パラメーター - valueTxt</span><span class="sxs-lookup"><span data-stu-id="9d453-135">Parameters - valueTxt</span></span>

<span data-ttu-id="9d453-136">値</span><span class="sxs-lookup"><span data-stu-id="9d453-136">value</span></span>  

<!-- -->

<span data-ttu-id="9d453-137">var</span><span class="sxs-lookup"><span data-stu-id="9d453-137">var</span></span>  

### <a name="return-value---valuetxt"></a><span data-ttu-id="9d453-138">戻り値 - valueTxt</span><span class="sxs-lookup"><span data-stu-id="9d453-138">Return Value - valueTxt</span></span>

## <a name="method-new"></a><span data-ttu-id="9d453-139">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9d453-139">Method new</span></span>

<span data-ttu-id="9d453-140">IISApplicationObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9d453-140">Initializes a new instance of the IISApplicationObject class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="9d453-141">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="9d453-141">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-lock"></a><span data-ttu-id="9d453-142">メソッド lock</span><span class="sxs-lookup"><span data-stu-id="9d453-142">Method lock</span></span>

```xpp
public void lock()
```

## <a name="method-unlock"></a><span data-ttu-id="9d453-143">メソッド unLock</span><span class="sxs-lookup"><span data-stu-id="9d453-143">Method unLock</span></span>

```xpp
public void unLock()
```

