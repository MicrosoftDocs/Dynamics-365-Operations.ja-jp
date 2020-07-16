---
title: IISWriteCookie クラス
description: このトピックでは、IISWriteCookie クラスについて説明します。
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
ms.openlocfilehash: a6500260b30867958bad1528ba6803f4c1ecf07a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502599"
---
# <a name="class-iiswritecookie"></a><span data-ttu-id="a67a1-103">クラス IISWriteCookie</span><span class="sxs-lookup"><span data-stu-id="a67a1-103">Class IISWriteCookie</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISWriteCookie extends Object
```

<span data-ttu-id="a67a1-104">IISWriteCookie クラスは、インターネット インフォメーション サービス (IIS) によって提供される WriteCookie オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="a67a1-104">The IISWriteCookie class wraps the WriteCookie object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="a67a1-105">備考</span><span class="sxs-lookup"><span data-stu-id="a67a1-105">Remarks</span></span>

<span data-ttu-id="a67a1-106">IISWriteCookie クラスのメソッドと、IIS によって提供される WriteCookie オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="a67a1-106">There is a one-to-one connection between the methods of the IISWriteCookie class and the methods of the WriteCookie object that is offered by IIS.</span></span> <span data-ttu-id="a67a1-107">したがって、IISWriteCookie クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a67a1-107">Therefore, for more information about the methods of the IISWriteCookie class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="a67a1-108">IISWriteCookie クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="a67a1-108">Use of the IISWriteCookie class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="a67a1-109">例</span><span class="sxs-lookup"><span data-stu-id="a67a1-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a67a1-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="a67a1-110">Methods</span></span>

| <span data-ttu-id="a67a1-111">方法</span><span class="sxs-lookup"><span data-stu-id="a67a1-111">Method</span></span>                                  | <span data-ttu-id="a67a1-112">説明</span><span class="sxs-lookup"><span data-stu-id="a67a1-112">Description</span></span>                                     |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="a67a1-113">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="a67a1-113">public COMEnum2Variant getEnum()</span></span>        |                                                 |
| <span data-ttu-id="a67a1-114">public boolean hasKeys()</span><span class="sxs-lookup"><span data-stu-id="a67a1-114">public boolean hasKeys()</span></span>                |                                                 |
| <span data-ttu-id="a67a1-115">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="a67a1-115">public ComInterface interface()</span></span>         |                                                 |
| <span data-ttu-id="a67a1-116">public void new(COM writeCookie)</span><span class="sxs-lookup"><span data-stu-id="a67a1-116">public void new(COM writeCookie)</span></span>        | <span data-ttu-id="a67a1-117">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a67a1-117">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="a67a1-118">public void secure(boolean secure)</span><span class="sxs-lookup"><span data-stu-id="a67a1-118">public void secure(boolean secure)</span></span>      |                                                 |
| <span data-ttu-id="a67a1-119">public void path(str path)</span><span class="sxs-lookup"><span data-stu-id="a67a1-119">public void path(str path)</span></span>              |                                                 |
| <span data-ttu-id="a67a1-120">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="a67a1-120">public void finalize()</span></span>                  |                                                 |
| <span data-ttu-id="a67a1-121">public void domain(str domain)</span><span class="sxs-lookup"><span data-stu-id="a67a1-121">public void domain(str domain)</span></span>          |                                                 |
| <span data-ttu-id="a67a1-122">public void expires(COMVariant expires)</span><span class="sxs-lookup"><span data-stu-id="a67a1-122">public void expires(COMVariant expires)</span></span> |                                                 |
| <span data-ttu-id="a67a1-123">public void item(str item, str value)</span><span class="sxs-lookup"><span data-stu-id="a67a1-123">public void item(str item, str value)</span></span>   |                                                 |

## <a name="method-getenum"></a><span data-ttu-id="a67a1-124">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="a67a1-124">Method getEnum</span></span>

```xpp
public COMEnum2Variant getEnum()
```

### <a name="return-value---getenum"></a><span data-ttu-id="a67a1-125">戻り値 - getEnum</span><span class="sxs-lookup"><span data-stu-id="a67a1-125">Return Value - getEnum</span></span>

## <a name="method-haskeys"></a><span data-ttu-id="a67a1-126">メソッド hasKeys</span><span class="sxs-lookup"><span data-stu-id="a67a1-126">Method hasKeys</span></span>

```xpp
public boolean hasKeys()
```

### <a name="return-value---haskeys"></a><span data-ttu-id="a67a1-127">戻り値 - hasKeys</span><span class="sxs-lookup"><span data-stu-id="a67a1-127">Return Value - hasKeys</span></span>

## <a name="method-interface"></a><span data-ttu-id="a67a1-128">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="a67a1-128">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="a67a1-129">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="a67a1-129">Return Value - interface</span></span>

## <a name="method-new"></a><span data-ttu-id="a67a1-130">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a67a1-130">Method new</span></span>

<span data-ttu-id="a67a1-131">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a67a1-131">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(COM writeCookie)
```

### <a name="parameters---new"></a><span data-ttu-id="a67a1-132">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="a67a1-132">Parameters - new</span></span>

<span data-ttu-id="a67a1-133">writeCookie</span><span class="sxs-lookup"><span data-stu-id="a67a1-133">writeCookie</span></span>  

## <a name="method-secure"></a><span data-ttu-id="a67a1-134">メソッド secure</span><span class="sxs-lookup"><span data-stu-id="a67a1-134">Method secure</span></span>

```xpp
public void secure(boolean secure)
```

### <a name="parameters---secure"></a><span data-ttu-id="a67a1-135">パラメーター - secure</span><span class="sxs-lookup"><span data-stu-id="a67a1-135">Parameters - secure</span></span>

<span data-ttu-id="a67a1-136">secure</span><span class="sxs-lookup"><span data-stu-id="a67a1-136">secure</span></span>  

## <a name="method-path"></a><span data-ttu-id="a67a1-137">メソッド path</span><span class="sxs-lookup"><span data-stu-id="a67a1-137">Method path</span></span>

```xpp
public void path(str path)
```

### <a name="parameters---path"></a><span data-ttu-id="a67a1-138">パラメーター - path</span><span class="sxs-lookup"><span data-stu-id="a67a1-138">Parameters - path</span></span>

<span data-ttu-id="a67a1-139">path</span><span class="sxs-lookup"><span data-stu-id="a67a1-139">path</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="a67a1-140">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="a67a1-140">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-domain"></a><span data-ttu-id="a67a1-141">メソッド domain</span><span class="sxs-lookup"><span data-stu-id="a67a1-141">Method domain</span></span>

```xpp
public void domain(str domain)
```

### <a name="parameters---domain"></a><span data-ttu-id="a67a1-142">パラメーター - domain</span><span class="sxs-lookup"><span data-stu-id="a67a1-142">Parameters - domain</span></span>

<span data-ttu-id="a67a1-143">domain</span><span class="sxs-lookup"><span data-stu-id="a67a1-143">domain</span></span>  

## <a name="method-expires"></a><span data-ttu-id="a67a1-144">メソッド expires</span><span class="sxs-lookup"><span data-stu-id="a67a1-144">Method expires</span></span>

```xpp
public void expires(COMVariant expires)
```

### <a name="parameters---expires"></a><span data-ttu-id="a67a1-145">パラメーター - expires</span><span class="sxs-lookup"><span data-stu-id="a67a1-145">Parameters - expires</span></span>

<span data-ttu-id="a67a1-146">expires</span><span class="sxs-lookup"><span data-stu-id="a67a1-146">expires</span></span>  

## <a name="method-item"></a><span data-ttu-id="a67a1-147">メソッド item</span><span class="sxs-lookup"><span data-stu-id="a67a1-147">Method item</span></span>

```xpp
public void item(str item, str value)
```

### <a name="parameters---item"></a><span data-ttu-id="a67a1-148">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="a67a1-148">Parameters - item</span></span>

<span data-ttu-id="a67a1-149">品目</span><span class="sxs-lookup"><span data-stu-id="a67a1-149">item</span></span>  

<!-- -->

<span data-ttu-id="a67a1-150">値</span><span class="sxs-lookup"><span data-stu-id="a67a1-150">value</span></span>  

