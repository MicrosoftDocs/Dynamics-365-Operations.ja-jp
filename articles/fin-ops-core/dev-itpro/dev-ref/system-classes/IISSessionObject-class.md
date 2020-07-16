---
title: IISSessionObject クラス
description: このトピックでは、IISSessionObject クラスについて説明します。
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
ms.openlocfilehash: 2803da002fdbaf3dd3f62176019f8fdb102ba4a5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502601"
---
# <a name="class-iissessionobject"></a><span data-ttu-id="db3ad-103">クラス IISSessionObject</span><span class="sxs-lookup"><span data-stu-id="db3ad-103">Class IISSessionObject</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISSessionObject extends Object
```

<span data-ttu-id="db3ad-104">IISSessionObject クラスは、インターネット インフォメーション サービス (IIS) によって提供される Session オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="db3ad-104">The IISSessionObject class wraps the Session object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="db3ad-105">備考</span><span class="sxs-lookup"><span data-stu-id="db3ad-105">Remarks</span></span>

<span data-ttu-id="db3ad-106">IISSessionObject クラスのメソッドと、IIS によって提供される Session オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="db3ad-106">There is a one-to-one connection between the methods of the IISSessionObject class and the methods of the Session object that is offered by IIS.</span></span> <span data-ttu-id="db3ad-107">したがって、IISSessionObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="db3ad-107">Therefore, for more information about the methods of the IISSessionObject class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="db3ad-108">IISSessionObject クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="db3ad-108">Use of the IISSessionObject class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="db3ad-109">例</span><span class="sxs-lookup"><span data-stu-id="db3ad-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="db3ad-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="db3ad-110">Methods</span></span>

| <span data-ttu-id="db3ad-111">方法</span><span class="sxs-lookup"><span data-stu-id="db3ad-111">Method</span></span>                                                 | <span data-ttu-id="db3ad-112">説明</span><span class="sxs-lookup"><span data-stu-id="db3ad-112">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="db3ad-113">public int codePage(\[int codePage\])</span><span class="sxs-lookup"><span data-stu-id="db3ad-113">public int codePage(\[int codePage\])</span></span>                  |                                                           |
| <span data-ttu-id="db3ad-114">public IISVariantDictionary contents()</span><span class="sxs-lookup"><span data-stu-id="db3ad-114">public IISVariantDictionary contents()</span></span>                 |                                                           |
| <span data-ttu-id="db3ad-115">public str getSessionID()</span><span class="sxs-lookup"><span data-stu-id="db3ad-115">public str getSessionID()</span></span>                              |                                                           |
| <span data-ttu-id="db3ad-116">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="db3ad-116">public ComInterface interface()</span></span>                        |                                                           |
| <span data-ttu-id="db3ad-117">public int lcid(\[int lcid\])</span><span class="sxs-lookup"><span data-stu-id="db3ad-117">public int lcid(\[int lcid\])</span></span>                          |                                                           |
| <span data-ttu-id="db3ad-118">public IISVariantDictionary staticObjects()</span><span class="sxs-lookup"><span data-stu-id="db3ad-118">public IISVariantDictionary staticObjects()</span></span>            |                                                           |
| <span data-ttu-id="db3ad-119">public int timeout(\[int timeout\])</span><span class="sxs-lookup"><span data-stu-id="db3ad-119">public int timeout(\[int timeout\])</span></span>                    |                                                           |
| <span data-ttu-id="db3ad-120">public COMVariant value(str value, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="db3ad-120">public COMVariant value(str value, \[COMVariant var\])</span></span> |                                                           |
| <span data-ttu-id="db3ad-121">public str valueTxt(str value, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="db3ad-121">public str valueTxt(str value, \[str var\])</span></span>            |                                                           |
| <span data-ttu-id="db3ad-122">public void new()</span><span class="sxs-lookup"><span data-stu-id="db3ad-122">public void new()</span></span>                                      | <span data-ttu-id="db3ad-123">IISSessionObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="db3ad-123">Initializes a new instance of the IISSessionObject class.</span></span> |
| <span data-ttu-id="db3ad-124">public void abandon()</span><span class="sxs-lookup"><span data-stu-id="db3ad-124">public void abandon()</span></span>                                  |                                                           |
| <span data-ttu-id="db3ad-125">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="db3ad-125">public void finalize()</span></span>                                 |                                                           |

## <a name="method-codepage"></a><span data-ttu-id="db3ad-126">メソッド codePage</span><span class="sxs-lookup"><span data-stu-id="db3ad-126">Method codePage</span></span>

```xpp
public int codePage([int codePage])
```

### <a name="parameters---codepage"></a><span data-ttu-id="db3ad-127">パラメーター - codePage</span><span class="sxs-lookup"><span data-stu-id="db3ad-127">Parameters - codePage</span></span>

<span data-ttu-id="db3ad-128">codePage</span><span class="sxs-lookup"><span data-stu-id="db3ad-128">codePage</span></span>  

### <a name="return-value---codepage"></a><span data-ttu-id="db3ad-129">戻り値 - codePage</span><span class="sxs-lookup"><span data-stu-id="db3ad-129">Return Value - codePage</span></span>

## <a name="method-contents"></a><span data-ttu-id="db3ad-130">メソッド contents</span><span class="sxs-lookup"><span data-stu-id="db3ad-130">Method contents</span></span>

```xpp
public IISVariantDictionary contents()
```

### <a name="return-value---contents"></a><span data-ttu-id="db3ad-131">戻り値 - contents</span><span class="sxs-lookup"><span data-stu-id="db3ad-131">Return Value - contents</span></span>

## <a name="method-getsessionid"></a><span data-ttu-id="db3ad-132">メソッド getSessionID</span><span class="sxs-lookup"><span data-stu-id="db3ad-132">Method getSessionID</span></span>

```xpp
public str getSessionID()
```

### <a name="return-value---getsessionid"></a><span data-ttu-id="db3ad-133">戻り値 - getSessionID</span><span class="sxs-lookup"><span data-stu-id="db3ad-133">Return Value - getSessionID</span></span>

## <a name="method-interface"></a><span data-ttu-id="db3ad-134">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="db3ad-134">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="db3ad-135">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="db3ad-135">Return Value - interface</span></span>

## <a name="method-lcid"></a><span data-ttu-id="db3ad-136">メソッド lcid</span><span class="sxs-lookup"><span data-stu-id="db3ad-136">Method lcid</span></span>

```xpp
public int lcid([int lcid])
```

### <a name="parameters---lcid"></a><span data-ttu-id="db3ad-137">パラメーター - lcid</span><span class="sxs-lookup"><span data-stu-id="db3ad-137">Parameters - lcid</span></span>

<span data-ttu-id="db3ad-138">lcid</span><span class="sxs-lookup"><span data-stu-id="db3ad-138">lcid</span></span>  

### <a name="return-value---lcid"></a><span data-ttu-id="db3ad-139">戻り値 - lcid</span><span class="sxs-lookup"><span data-stu-id="db3ad-139">Return Value - lcid</span></span>

## <a name="method-staticobjects"></a><span data-ttu-id="db3ad-140">メソッド staticObjects</span><span class="sxs-lookup"><span data-stu-id="db3ad-140">Method staticObjects</span></span>

```xpp
public IISVariantDictionary staticObjects()
```

### <a name="return-value---staticobjects"></a><span data-ttu-id="db3ad-141">戻り値 - staticObjects</span><span class="sxs-lookup"><span data-stu-id="db3ad-141">Return Value - staticObjects</span></span>

## <a name="method-timeout"></a><span data-ttu-id="db3ad-142">メソッド timeout</span><span class="sxs-lookup"><span data-stu-id="db3ad-142">Method timeout</span></span>

```xpp
public int timeout([int timeout])
```

### <a name="parameters---timeout"></a><span data-ttu-id="db3ad-143">パラメーター - timeout</span><span class="sxs-lookup"><span data-stu-id="db3ad-143">Parameters - timeout</span></span>

<span data-ttu-id="db3ad-144">timeout</span><span class="sxs-lookup"><span data-stu-id="db3ad-144">timeout</span></span>  

### <a name="return-value---timeout"></a><span data-ttu-id="db3ad-145">戻り値 - timeout</span><span class="sxs-lookup"><span data-stu-id="db3ad-145">Return Value - timeout</span></span>

## <a name="method-value"></a><span data-ttu-id="db3ad-146">メソッド value</span><span class="sxs-lookup"><span data-stu-id="db3ad-146">Method value</span></span>

```xpp
public COMVariant value(str value, [COMVariant var])
```

### <a name="parameters---value"></a><span data-ttu-id="db3ad-147">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="db3ad-147">Parameters - value</span></span>

<span data-ttu-id="db3ad-148">値</span><span class="sxs-lookup"><span data-stu-id="db3ad-148">value</span></span>  

<!-- -->

<span data-ttu-id="db3ad-149">var</span><span class="sxs-lookup"><span data-stu-id="db3ad-149">var</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="db3ad-150">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="db3ad-150">Return Value - value</span></span>

## <a name="method-valuetxt"></a><span data-ttu-id="db3ad-151">メソッド valueTxt</span><span class="sxs-lookup"><span data-stu-id="db3ad-151">Method valueTxt</span></span>

```xpp
public str valueTxt(str value, [str var])
```

### <a name="parameters---valuetxt"></a><span data-ttu-id="db3ad-152">パラメーター - valueTxt</span><span class="sxs-lookup"><span data-stu-id="db3ad-152">Parameters - valueTxt</span></span>

<span data-ttu-id="db3ad-153">値</span><span class="sxs-lookup"><span data-stu-id="db3ad-153">value</span></span>  

<!-- -->

<span data-ttu-id="db3ad-154">var</span><span class="sxs-lookup"><span data-stu-id="db3ad-154">var</span></span>  

### <a name="return-value---valuetxt"></a><span data-ttu-id="db3ad-155">戻り値 - valueTxt</span><span class="sxs-lookup"><span data-stu-id="db3ad-155">Return Value - valueTxt</span></span>

## <a name="method-new"></a><span data-ttu-id="db3ad-156">メソッド new</span><span class="sxs-lookup"><span data-stu-id="db3ad-156">Method new</span></span>

<span data-ttu-id="db3ad-157">IISSessionObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="db3ad-157">Initializes a new instance of the IISSessionObject class.</span></span>

```xpp
public void new()
```

## <a name="method-abandon"></a><span data-ttu-id="db3ad-158">メソッド abandon</span><span class="sxs-lookup"><span data-stu-id="db3ad-158">Method abandon</span></span>

```xpp
public void abandon()
```

## <a name="method-finalize"></a><span data-ttu-id="db3ad-159">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="db3ad-159">Method finalize</span></span>

```xpp
public void finalize()
```

