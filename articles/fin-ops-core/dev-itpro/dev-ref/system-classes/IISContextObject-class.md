---
title: IISContextObject クラス
description: このトピックでは、IISContextObject クラスについて説明します。
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
ms.openlocfilehash: d5d1d513ba3c70be4b3e7670c47c917ce896008c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502606"
---
# <a name="class-iiscontextobject"></a><span data-ttu-id="d456e-103">クラス IISContextObject</span><span class="sxs-lookup"><span data-stu-id="d456e-103">Class IISContextObject</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISContextObject extends Object
```

## <a name="remarks"></a><span data-ttu-id="d456e-104">備考</span><span class="sxs-lookup"><span data-stu-id="d456e-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d456e-105">例</span><span class="sxs-lookup"><span data-stu-id="d456e-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d456e-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d456e-106">Methods</span></span>

| <span data-ttu-id="d456e-107">方法</span><span class="sxs-lookup"><span data-stu-id="d456e-107">Method</span></span>                                                 | <span data-ttu-id="d456e-108">説明</span><span class="sxs-lookup"><span data-stu-id="d456e-108">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d456e-109">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="d456e-109">public ComInterface interface()</span></span>                        |                                                           |
| <span data-ttu-id="d456e-110">public boolean isTraceEnabled()</span><span class="sxs-lookup"><span data-stu-id="d456e-110">public boolean isTraceEnabled()</span></span>                        |                                                           |
| <span data-ttu-id="d456e-111">public IISVariantDictionary items()</span><span class="sxs-lookup"><span data-stu-id="d456e-111">public IISVariantDictionary items()</span></span>                    |                                                           |
| <span data-ttu-id="d456e-112">public int traceMode(int mode)</span><span class="sxs-lookup"><span data-stu-id="d456e-112">public int traceMode(int mode)</span></span>                         |                                                           |
| <span data-ttu-id="d456e-113">public COMVariant value(str value, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="d456e-113">public COMVariant value(str value, \[COMVariant var\])</span></span> |                                                           |
| <span data-ttu-id="d456e-114">public str valueTxt(str value, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="d456e-114">public str valueTxt(str value, \[str var\])</span></span>            |                                                           |
| <span data-ttu-id="d456e-115">public void traceWrite(str category, str message)</span><span class="sxs-lookup"><span data-stu-id="d456e-115">public void traceWrite(str category, str message)</span></span>      |                                                           |
| <span data-ttu-id="d456e-116">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d456e-116">public void finalize()</span></span>                                 |                                                           |
| <span data-ttu-id="d456e-117">public void traceWarn(str category, str message)</span><span class="sxs-lookup"><span data-stu-id="d456e-117">public void traceWarn(str category, str message)</span></span>       |                                                           |
| <span data-ttu-id="d456e-118">public void new()</span><span class="sxs-lookup"><span data-stu-id="d456e-118">public void new()</span></span>                                      | <span data-ttu-id="d456e-119">IISContextObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d456e-119">Initializes a new instance of the IISContextObject class.</span></span> |

## <a name="method-interface"></a><span data-ttu-id="d456e-120">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="d456e-120">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="d456e-121">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="d456e-121">Return Value - interface</span></span>

## <a name="method-istraceenabled"></a><span data-ttu-id="d456e-122">メソッド isTraceEnabled</span><span class="sxs-lookup"><span data-stu-id="d456e-122">Method isTraceEnabled</span></span>

```xpp
public boolean isTraceEnabled()
```

### <a name="return-value---istraceenabled"></a><span data-ttu-id="d456e-123">戻り値 - isTraceEnabled</span><span class="sxs-lookup"><span data-stu-id="d456e-123">Return Value - isTraceEnabled</span></span>

## <a name="method-items"></a><span data-ttu-id="d456e-124">メソッド items</span><span class="sxs-lookup"><span data-stu-id="d456e-124">Method items</span></span>

```xpp
public IISVariantDictionary items()
```

### <a name="return-value---items"></a><span data-ttu-id="d456e-125">戻り値 - items</span><span class="sxs-lookup"><span data-stu-id="d456e-125">Return Value - items</span></span>

## <a name="method-tracemode"></a><span data-ttu-id="d456e-126">メソッド traceMode</span><span class="sxs-lookup"><span data-stu-id="d456e-126">Method traceMode</span></span>

```xpp
public int traceMode(int mode)
```

### <a name="parameters---tracemode"></a><span data-ttu-id="d456e-127">パラメーター - traceMode</span><span class="sxs-lookup"><span data-stu-id="d456e-127">Parameters - traceMode</span></span>

<span data-ttu-id="d456e-128">モード</span><span class="sxs-lookup"><span data-stu-id="d456e-128">mode</span></span>  

### <a name="return-value---tracemode"></a><span data-ttu-id="d456e-129">戻り値 - traceMode</span><span class="sxs-lookup"><span data-stu-id="d456e-129">Return Value - traceMode</span></span>

## <a name="method-value"></a><span data-ttu-id="d456e-130">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d456e-130">Method value</span></span>

```xpp
public COMVariant value(str value, [COMVariant var])
```

### <a name="parameters---value"></a><span data-ttu-id="d456e-131">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="d456e-131">Parameters - value</span></span>

<span data-ttu-id="d456e-132">値</span><span class="sxs-lookup"><span data-stu-id="d456e-132">value</span></span>  

<!-- -->

<span data-ttu-id="d456e-133">var</span><span class="sxs-lookup"><span data-stu-id="d456e-133">var</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="d456e-134">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="d456e-134">Return Value - value</span></span>

## <a name="method-valuetxt"></a><span data-ttu-id="d456e-135">メソッド valueTxt</span><span class="sxs-lookup"><span data-stu-id="d456e-135">Method valueTxt</span></span>

```xpp
public str valueTxt(str value, [str var])
```

### <a name="parameters---valuetxt"></a><span data-ttu-id="d456e-136">パラメーター - valueTxt</span><span class="sxs-lookup"><span data-stu-id="d456e-136">Parameters - valueTxt</span></span>

<span data-ttu-id="d456e-137">値</span><span class="sxs-lookup"><span data-stu-id="d456e-137">value</span></span>  

<!-- -->

<span data-ttu-id="d456e-138">var</span><span class="sxs-lookup"><span data-stu-id="d456e-138">var</span></span>  

### <a name="return-value---valuetxt"></a><span data-ttu-id="d456e-139">戻り値 - valueTxt</span><span class="sxs-lookup"><span data-stu-id="d456e-139">Return Value - valueTxt</span></span>

## <a name="method-tracewrite"></a><span data-ttu-id="d456e-140">メソッド traceWrite</span><span class="sxs-lookup"><span data-stu-id="d456e-140">Method traceWrite</span></span>

```xpp
public void traceWrite(str category, str message)
```

### <a name="parameters---tracewrite"></a><span data-ttu-id="d456e-141">パラメーター - traceWrite</span><span class="sxs-lookup"><span data-stu-id="d456e-141">Parameters - traceWrite</span></span>

<span data-ttu-id="d456e-142">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="d456e-142">category</span></span>  

<!-- -->

<span data-ttu-id="d456e-143">メッセージ</span><span class="sxs-lookup"><span data-stu-id="d456e-143">message</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="d456e-144">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d456e-144">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-tracewarn"></a><span data-ttu-id="d456e-145">メソッド traceWarn</span><span class="sxs-lookup"><span data-stu-id="d456e-145">Method traceWarn</span></span>

```xpp
public void traceWarn(str category, str message)
```

### <a name="parameters---tracewarn"></a><span data-ttu-id="d456e-146">パラメーター - traceWarn</span><span class="sxs-lookup"><span data-stu-id="d456e-146">Parameters - traceWarn</span></span>

<span data-ttu-id="d456e-147">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="d456e-147">category</span></span>  

<!-- -->

<span data-ttu-id="d456e-148">メッセージ</span><span class="sxs-lookup"><span data-stu-id="d456e-148">message</span></span>  

## <a name="method-new"></a><span data-ttu-id="d456e-149">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d456e-149">Method new</span></span>

<span data-ttu-id="d456e-150">IISContextObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d456e-150">Initializes a new instance of the IISContextObject class.</span></span>

```xpp
public void new()
```

