---
title: IISRequestDictionary クラス
description: このトピックでは、IISRequestDictionary クラスについて説明します。
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
ms.openlocfilehash: fe8377139e71521a62b59517ab8bb44353cb093e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502905"
---
# <a name="class-iisrequestdictionary"></a><span data-ttu-id="c5b33-103">クラス IISRequestDictionary</span><span class="sxs-lookup"><span data-stu-id="c5b33-103">Class IISRequestDictionary</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISRequestDictionary extends Object
```

<span data-ttu-id="c5b33-104">IISRequestDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される RequestDictionary オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="c5b33-104">The IISRequestDictionary class wraps the RequestDictionary object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5b33-105">備考</span><span class="sxs-lookup"><span data-stu-id="c5b33-105">Remarks</span></span>

<span data-ttu-id="c5b33-106">IISRequestDictionary クラスのメソッドと、IIS によって提供される RequestDictionary オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。</span><span class="sxs-lookup"><span data-stu-id="c5b33-106">There is a one-to-one relationship between the methods of the IISRequestDictionary class and the methods of the RequestDictionary object that is offered by IIS.</span></span> <span data-ttu-id="c5b33-107">したがって、IISRequestDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5b33-107">Therefore, for more information about the methods of the IISRequestDictionary class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="c5b33-108">IISRequestDictionary クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="c5b33-108">Use of the IISRequestDictionary class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="c5b33-109">例</span><span class="sxs-lookup"><span data-stu-id="c5b33-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c5b33-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="c5b33-110">Methods</span></span>

| <span data-ttu-id="c5b33-111">方法</span><span class="sxs-lookup"><span data-stu-id="c5b33-111">Method</span></span>                                              | <span data-ttu-id="c5b33-112">説明</span><span class="sxs-lookup"><span data-stu-id="c5b33-112">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="c5b33-113">public int count()</span><span class="sxs-lookup"><span data-stu-id="c5b33-113">public int count()</span></span>                                  |                                                 |
| <span data-ttu-id="c5b33-114">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="c5b33-114">public COMEnum2Variant getEnum()</span></span>                    |                                                 |
| <span data-ttu-id="c5b33-115">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="c5b33-115">public ComInterface interface()</span></span>                     |                                                 |
| <span data-ttu-id="c5b33-116">public COMVariant item(COMVariant item)</span><span class="sxs-lookup"><span data-stu-id="c5b33-116">public COMVariant item(COMVariant item)</span></span>             |                                                 |
| <span data-ttu-id="c5b33-117">public IISReadCookie itemReadCookie(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="c5b33-117">public IISReadCookie itemReadCookie(\[str item\])</span></span>   |                                                 |
| <span data-ttu-id="c5b33-118">public IISStringList itemStringList(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="c5b33-118">public IISStringList itemStringList(\[str item\])</span></span>   |                                                 |
| <span data-ttu-id="c5b33-119">public str itemTxt(str item)</span><span class="sxs-lookup"><span data-stu-id="c5b33-119">public str itemTxt(str item)</span></span>                        |                                                 |
| <span data-ttu-id="c5b33-120">public IISWriteCookie itemWriteCookie(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="c5b33-120">public IISWriteCookie itemWriteCookie(\[str item\])</span></span> |                                                 |
| <span data-ttu-id="c5b33-121">public str key(str key)</span><span class="sxs-lookup"><span data-stu-id="c5b33-121">public str key(str key)</span></span>                             |                                                 |
| <span data-ttu-id="c5b33-122">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="c5b33-122">public void finalize()</span></span>                              |                                                 |
| <span data-ttu-id="c5b33-123">public void new(COM requestDictionary)</span><span class="sxs-lookup"><span data-stu-id="c5b33-123">public void new(COM requestDictionary)</span></span>              | <span data-ttu-id="c5b33-124">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c5b33-124">Initializes a new instance of the Object class.</span></span> |

## <a name="method-count"></a><span data-ttu-id="c5b33-125">メソッド count</span><span class="sxs-lookup"><span data-stu-id="c5b33-125">Method count</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="c5b33-126">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="c5b33-126">Return Value - count</span></span>

## <a name="method-getenum"></a><span data-ttu-id="c5b33-127">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="c5b33-127">Method getEnum</span></span>

```xpp
public COMEnum2Variant getEnum()
```

### <a name="return-value---getenum"></a><span data-ttu-id="c5b33-128">戻り値 - getEnum</span><span class="sxs-lookup"><span data-stu-id="c5b33-128">Return Value - getEnum</span></span>

## <a name="method-interface"></a><span data-ttu-id="c5b33-129">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="c5b33-129">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="c5b33-130">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="c5b33-130">Return Value - interface</span></span>

## <a name="method-item"></a><span data-ttu-id="c5b33-131">メソッド item</span><span class="sxs-lookup"><span data-stu-id="c5b33-131">Method item</span></span>

```xpp
public COMVariant item(COMVariant item)
```

### <a name="parameters---item"></a><span data-ttu-id="c5b33-132">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="c5b33-132">Parameters - item</span></span>

<span data-ttu-id="c5b33-133">品目</span><span class="sxs-lookup"><span data-stu-id="c5b33-133">item</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="c5b33-134">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="c5b33-134">Return Value - item</span></span>

## <a name="method-itemreadcookie"></a><span data-ttu-id="c5b33-135">メソッド itemReadCookie</span><span class="sxs-lookup"><span data-stu-id="c5b33-135">Method itemReadCookie</span></span>

```xpp
public IISReadCookie itemReadCookie([str item])
```

### <a name="parameters---itemreadcookie"></a><span data-ttu-id="c5b33-136">パラメーター - itemReadCookie</span><span class="sxs-lookup"><span data-stu-id="c5b33-136">Parameters - itemReadCookie</span></span>

<span data-ttu-id="c5b33-137">品目</span><span class="sxs-lookup"><span data-stu-id="c5b33-137">item</span></span>  

### <a name="return-value---itemreadcookie"></a><span data-ttu-id="c5b33-138">戻り値 - itemReadCookie</span><span class="sxs-lookup"><span data-stu-id="c5b33-138">Return Value - itemReadCookie</span></span>

## <a name="method-itemstringlist"></a><span data-ttu-id="c5b33-139">メソッド itemStringList</span><span class="sxs-lookup"><span data-stu-id="c5b33-139">Method itemStringList</span></span>

```xpp
public IISStringList itemStringList([str item])
```

### <a name="parameters---itemstringlist"></a><span data-ttu-id="c5b33-140">パラメーター - itemStringList</span><span class="sxs-lookup"><span data-stu-id="c5b33-140">Parameters - itemStringList</span></span>

<span data-ttu-id="c5b33-141">品目</span><span class="sxs-lookup"><span data-stu-id="c5b33-141">item</span></span>  

### <a name="return-value---itemstringlist"></a><span data-ttu-id="c5b33-142">戻り値 - itemStringList</span><span class="sxs-lookup"><span data-stu-id="c5b33-142">Return Value - itemStringList</span></span>

## <a name="method-itemtxt"></a><span data-ttu-id="c5b33-143">メソッド itemTxt</span><span class="sxs-lookup"><span data-stu-id="c5b33-143">Method itemTxt</span></span>

```xpp
public str itemTxt(str item)
```

### <a name="parameters---itemtxt"></a><span data-ttu-id="c5b33-144">パラメーター - itemTxt</span><span class="sxs-lookup"><span data-stu-id="c5b33-144">Parameters - itemTxt</span></span>

<span data-ttu-id="c5b33-145">品目</span><span class="sxs-lookup"><span data-stu-id="c5b33-145">item</span></span>  

### <a name="return-value---itemtxt"></a><span data-ttu-id="c5b33-146">戻り値 - itemTxt</span><span class="sxs-lookup"><span data-stu-id="c5b33-146">Return Value - itemTxt</span></span>

## <a name="method-itemwritecookie"></a><span data-ttu-id="c5b33-147">メソッド itemWriteCookie</span><span class="sxs-lookup"><span data-stu-id="c5b33-147">Method itemWriteCookie</span></span>

```xpp
public IISWriteCookie itemWriteCookie([str item])
```

### <a name="parameters---itemwritecookie"></a><span data-ttu-id="c5b33-148">パラメーター - itemWriteCookie</span><span class="sxs-lookup"><span data-stu-id="c5b33-148">Parameters - itemWriteCookie</span></span>

<span data-ttu-id="c5b33-149">品目</span><span class="sxs-lookup"><span data-stu-id="c5b33-149">item</span></span>  

### <a name="return-value---itemwritecookie"></a><span data-ttu-id="c5b33-150">戻り値 - itemWriteCookie</span><span class="sxs-lookup"><span data-stu-id="c5b33-150">Return Value - itemWriteCookie</span></span>

## <a name="method-key"></a><span data-ttu-id="c5b33-151">メソッド key</span><span class="sxs-lookup"><span data-stu-id="c5b33-151">Method key</span></span>

```xpp
public str key(str key)
```

### <a name="parameters---key"></a><span data-ttu-id="c5b33-152">パラメーター - key</span><span class="sxs-lookup"><span data-stu-id="c5b33-152">Parameters - key</span></span>

<span data-ttu-id="c5b33-153">キー</span><span class="sxs-lookup"><span data-stu-id="c5b33-153">key</span></span>  

### <a name="return-value---key"></a><span data-ttu-id="c5b33-154">戻り値 - key</span><span class="sxs-lookup"><span data-stu-id="c5b33-154">Return Value - key</span></span>

## <a name="method-finalize"></a><span data-ttu-id="c5b33-155">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="c5b33-155">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="c5b33-156">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c5b33-156">Method new</span></span>

<span data-ttu-id="c5b33-157">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c5b33-157">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(COM requestDictionary)
```

### <a name="parameters---new"></a><span data-ttu-id="c5b33-158">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c5b33-158">Parameters - new</span></span>

<span data-ttu-id="c5b33-159">requestDictionary</span><span class="sxs-lookup"><span data-stu-id="c5b33-159">requestDictionary</span></span>  

