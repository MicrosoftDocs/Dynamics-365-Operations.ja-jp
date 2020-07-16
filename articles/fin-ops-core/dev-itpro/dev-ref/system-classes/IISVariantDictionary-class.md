---
title: IISVariantDictionary クラス
description: このトピックでは、IISVariantDictionary クラスについて説明します。
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
ms.openlocfilehash: 95c68565667495ddda16ae5fd53f75972df00d43
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502600"
---
# <a name="class-iisvariantdictionary"></a><span data-ttu-id="b55c4-103">クラス IISVariantDictionary</span><span class="sxs-lookup"><span data-stu-id="b55c4-103">Class IISVariantDictionary</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISVariantDictionary extends Object
```

<span data-ttu-id="b55c4-104">IISVariantDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される VariantDictionary オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="b55c4-104">The IISVariantDictionary class wraps the VariantDictionary object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="b55c4-105">備考</span><span class="sxs-lookup"><span data-stu-id="b55c4-105">Remarks</span></span>

<span data-ttu-id="b55c4-106">IISVariantDictionary クラスのメソッドと、IIS によって提供される VariantDictionary オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="b55c4-106">There is a one-to-one connection between the methods of the IISVariantDictionary class and the methods of the VariantDictionary object that is offered by IIS.</span></span> <span data-ttu-id="b55c4-107">したがって、IISVariantDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b55c4-107">Therefore, for more information about the methods of the IISVariantDictionary class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="b55c4-108">IISVariantDictionary クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="b55c4-108">Use of the IISVariantDictionary class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="b55c4-109">例</span><span class="sxs-lookup"><span data-stu-id="b55c4-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b55c4-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="b55c4-110">Methods</span></span>

| <span data-ttu-id="b55c4-111">方法</span><span class="sxs-lookup"><span data-stu-id="b55c4-111">Method</span></span>                                                      | <span data-ttu-id="b55c4-112">説明</span><span class="sxs-lookup"><span data-stu-id="b55c4-112">Description</span></span>                                     |
|-------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="b55c4-113">public int count()</span><span class="sxs-lookup"><span data-stu-id="b55c4-113">public int count()</span></span>                                          |                                                 |
| <span data-ttu-id="b55c4-114">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="b55c4-114">public COMEnum2Variant getEnum()</span></span>                            |                                                 |
| <span data-ttu-id="b55c4-115">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="b55c4-115">public ComInterface interface()</span></span>                             |                                                 |
| <span data-ttu-id="b55c4-116">public COMVariant item(COMVariant item, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="b55c4-116">public COMVariant item(COMVariant item, \[COMVariant var\])</span></span> |                                                 |
| <span data-ttu-id="b55c4-117">public COM itemObj(str item, \[COM var\])</span><span class="sxs-lookup"><span data-stu-id="b55c4-117">public COM itemObj(str item, \[COM var\])</span></span>                   |                                                 |
| <span data-ttu-id="b55c4-118">public str itemTxt(str item, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="b55c4-118">public str itemTxt(str item, \[str var\])</span></span>                   |                                                 |
| <span data-ttu-id="b55c4-119">public str key(str key)</span><span class="sxs-lookup"><span data-stu-id="b55c4-119">public str key(str key)</span></span>                                     |                                                 |
| <span data-ttu-id="b55c4-120">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="b55c4-120">public void finalize()</span></span>                                      |                                                 |
| <span data-ttu-id="b55c4-121">public void remove(str key)</span><span class="sxs-lookup"><span data-stu-id="b55c4-121">public void remove(str key)</span></span>                                 |                                                 |
| <span data-ttu-id="b55c4-122">public void removeAll()</span><span class="sxs-lookup"><span data-stu-id="b55c4-122">public void removeAll()</span></span>                                     |                                                 |
| <span data-ttu-id="b55c4-123">public void new(COM variantDictionary)</span><span class="sxs-lookup"><span data-stu-id="b55c4-123">public void new(COM variantDictionary)</span></span>                      | <span data-ttu-id="b55c4-124">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b55c4-124">Initializes a new instance of the Object class.</span></span> |

## <a name="method-count"></a><span data-ttu-id="b55c4-125">メソッド count</span><span class="sxs-lookup"><span data-stu-id="b55c4-125">Method count</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="b55c4-126">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="b55c4-126">Return Value - count</span></span>

## <a name="method-getenum"></a><span data-ttu-id="b55c4-127">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="b55c4-127">Method getEnum</span></span>

```xpp
public COMEnum2Variant getEnum()
```

### <a name="return-value---getenum"></a><span data-ttu-id="b55c4-128">戻り値 - getEnum</span><span class="sxs-lookup"><span data-stu-id="b55c4-128">Return Value - getEnum</span></span>

## <a name="method-interface"></a><span data-ttu-id="b55c4-129">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="b55c4-129">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="b55c4-130">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="b55c4-130">Return Value - interface</span></span>

## <a name="method-item"></a><span data-ttu-id="b55c4-131">メソッド item</span><span class="sxs-lookup"><span data-stu-id="b55c4-131">Method item</span></span>

```xpp
public COMVariant item(COMVariant item, [COMVariant var])
```

### <a name="parameters---item"></a><span data-ttu-id="b55c4-132">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="b55c4-132">Parameters - item</span></span>

<span data-ttu-id="b55c4-133">品目</span><span class="sxs-lookup"><span data-stu-id="b55c4-133">item</span></span>  

<!-- -->

<span data-ttu-id="b55c4-134">var</span><span class="sxs-lookup"><span data-stu-id="b55c4-134">var</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="b55c4-135">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="b55c4-135">Return Value - item</span></span>

## <a name="method-itemobj"></a><span data-ttu-id="b55c4-136">メソッド itemObj</span><span class="sxs-lookup"><span data-stu-id="b55c4-136">Method itemObj</span></span>

```xpp
public COM itemObj(str item, [COM var])
```

### <a name="parameters---itemobj"></a><span data-ttu-id="b55c4-137">パラメーター - itemObj</span><span class="sxs-lookup"><span data-stu-id="b55c4-137">Parameters - itemObj</span></span>

<span data-ttu-id="b55c4-138">品目</span><span class="sxs-lookup"><span data-stu-id="b55c4-138">item</span></span>  

<!-- -->

<span data-ttu-id="b55c4-139">var</span><span class="sxs-lookup"><span data-stu-id="b55c4-139">var</span></span>  

### <a name="return-value---itemobj"></a><span data-ttu-id="b55c4-140">戻り値 - itemObj</span><span class="sxs-lookup"><span data-stu-id="b55c4-140">Return Value - itemObj</span></span>

## <a name="method-itemtxt"></a><span data-ttu-id="b55c4-141">メソッド itemTxt</span><span class="sxs-lookup"><span data-stu-id="b55c4-141">Method itemTxt</span></span>

```xpp
public str itemTxt(str item, [str var])
```

### <a name="parameters---itemtxt"></a><span data-ttu-id="b55c4-142">パラメーター - itemTxt</span><span class="sxs-lookup"><span data-stu-id="b55c4-142">Parameters - itemTxt</span></span>

<span data-ttu-id="b55c4-143">品目</span><span class="sxs-lookup"><span data-stu-id="b55c4-143">item</span></span>  

<!-- -->

<span data-ttu-id="b55c4-144">var</span><span class="sxs-lookup"><span data-stu-id="b55c4-144">var</span></span>  

### <a name="return-value---itemtxt"></a><span data-ttu-id="b55c4-145">戻り値 - itemTxt</span><span class="sxs-lookup"><span data-stu-id="b55c4-145">Return Value - itemTxt</span></span>

## <a name="method-key"></a><span data-ttu-id="b55c4-146">メソッド key</span><span class="sxs-lookup"><span data-stu-id="b55c4-146">Method key</span></span>

```xpp
public str key(str key)
```

### <a name="parameters---key"></a><span data-ttu-id="b55c4-147">パラメーター - key</span><span class="sxs-lookup"><span data-stu-id="b55c4-147">Parameters - key</span></span>

<span data-ttu-id="b55c4-148">キー</span><span class="sxs-lookup"><span data-stu-id="b55c4-148">key</span></span>  

### <a name="return-value---key"></a><span data-ttu-id="b55c4-149">戻り値 - key</span><span class="sxs-lookup"><span data-stu-id="b55c4-149">Return Value - key</span></span>

## <a name="method-finalize"></a><span data-ttu-id="b55c4-150">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="b55c4-150">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-remove"></a><span data-ttu-id="b55c4-151">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="b55c4-151">Method remove</span></span>

```xpp
public void remove(str key)
```

### <a name="parameters---remove"></a><span data-ttu-id="b55c4-152">パラメーター - remove</span><span class="sxs-lookup"><span data-stu-id="b55c4-152">Parameters - remove</span></span>

<span data-ttu-id="b55c4-153">キー</span><span class="sxs-lookup"><span data-stu-id="b55c4-153">key</span></span>  

## <a name="method-removeall"></a><span data-ttu-id="b55c4-154">メソッド removeAll</span><span class="sxs-lookup"><span data-stu-id="b55c4-154">Method removeAll</span></span>

```xpp
public void removeAll()
```

## <a name="method-new"></a><span data-ttu-id="b55c4-155">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b55c4-155">Method new</span></span>

<span data-ttu-id="b55c4-156">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b55c4-156">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(COM variantDictionary)
```

### <a name="parameters---new"></a><span data-ttu-id="b55c4-157">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="b55c4-157">Parameters - new</span></span>

<span data-ttu-id="b55c4-158">variantDictionary</span><span class="sxs-lookup"><span data-stu-id="b55c4-158">variantDictionary</span></span>  

