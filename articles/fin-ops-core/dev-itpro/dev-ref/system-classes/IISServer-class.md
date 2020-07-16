---
title: IISServer クラス
description: このトピックでは、IISServer クラスについて説明します。
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
ms.openlocfilehash: 26334a1111979ccb686b7693fa8eb054625aeb5f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502907"
---
# <a name="class-iisserver"></a><span data-ttu-id="db837-103">クラス IISServer</span><span class="sxs-lookup"><span data-stu-id="db837-103">Class IISServer</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISServer extends Object
```

<span data-ttu-id="db837-104">IISServer クラスは、インターネット インフォメーション サービス (IIS) によって提供される Server オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="db837-104">The IISServer class wraps the Server object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="db837-105">備考</span><span class="sxs-lookup"><span data-stu-id="db837-105">Remarks</span></span>

<span data-ttu-id="db837-106">IISServer クラスのメソッドと、IIS によって提供される Server オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="db837-106">There is a one-to-one connection between the methods of the IISServer class and the methods of the Server object that is offered by IIS.</span></span> <span data-ttu-id="db837-107">したがって、IISServer クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="db837-107">Therefore, for more information about the methods of the IISServer class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="db837-108">IISServer クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="db837-108">Use of the IISServer class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="db837-109">例</span><span class="sxs-lookup"><span data-stu-id="db837-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="db837-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="db837-110">Methods</span></span>

| <span data-ttu-id="db837-111">方法</span><span class="sxs-lookup"><span data-stu-id="db837-111">Method</span></span>                                           | <span data-ttu-id="db837-112">説明</span><span class="sxs-lookup"><span data-stu-id="db837-112">Description</span></span>                                        |
|--------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="db837-113">public COM createObject(str progID)</span><span class="sxs-lookup"><span data-stu-id="db837-113">public COM createObject(str progID)</span></span>              |                                                    |
| <span data-ttu-id="db837-114">public str htmlEncode(str txt)</span><span class="sxs-lookup"><span data-stu-id="db837-114">public str htmlEncode(str txt)</span></span>                   |                                                    |
| <span data-ttu-id="db837-115">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="db837-115">public ComInterface interface()</span></span>                  |                                                    |
| <span data-ttu-id="db837-116">public str mapPath(str logicalPath)</span><span class="sxs-lookup"><span data-stu-id="db837-116">public str mapPath(str logicalPath)</span></span>              |                                                    |
| <span data-ttu-id="db837-117">public int scriptTimeout(\[int timeoutSeconds\])</span><span class="sxs-lookup"><span data-stu-id="db837-117">public int scriptTimeout(\[int timeoutSeconds\])</span></span> |                                                    |
| <span data-ttu-id="db837-118">public str urlEncode(str txt)</span><span class="sxs-lookup"><span data-stu-id="db837-118">public str urlEncode(str txt)</span></span>                    |                                                    |
| <span data-ttu-id="db837-119">public str urlPathEncode(str txt)</span><span class="sxs-lookup"><span data-stu-id="db837-119">public str urlPathEncode(str txt)</span></span>                |                                                    |
| <span data-ttu-id="db837-120">public void execute(str logicalPath)</span><span class="sxs-lookup"><span data-stu-id="db837-120">public void execute(str logicalPath)</span></span>             |                                                    |
| <span data-ttu-id="db837-121">public void transfer(str logicalPath)</span><span class="sxs-lookup"><span data-stu-id="db837-121">public void transfer(str logicalPath)</span></span>            |                                                    |
| <span data-ttu-id="db837-122">public void new()</span><span class="sxs-lookup"><span data-stu-id="db837-122">public void new()</span></span>                                | <span data-ttu-id="db837-123">IISServer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="db837-123">Initializes a new instance of the IISServer class.</span></span> |
| <span data-ttu-id="db837-124">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="db837-124">public void finalize()</span></span>                           |                                                    |

## <a name="method-createobject"></a><span data-ttu-id="db837-125">メソッド createObject</span><span class="sxs-lookup"><span data-stu-id="db837-125">Method createObject</span></span>

```xpp
public COM createObject(str progID)
```

### <a name="parameters---createobject"></a><span data-ttu-id="db837-126">パラメーター - createObject</span><span class="sxs-lookup"><span data-stu-id="db837-126">Parameters - createObject</span></span>

<span data-ttu-id="db837-127">progID</span><span class="sxs-lookup"><span data-stu-id="db837-127">progID</span></span>  

### <a name="return-value---createobject"></a><span data-ttu-id="db837-128">戻り値 - createObject</span><span class="sxs-lookup"><span data-stu-id="db837-128">Return Value - createObject</span></span>

## <a name="method-htmlencode"></a><span data-ttu-id="db837-129">メソッド htmlEncode</span><span class="sxs-lookup"><span data-stu-id="db837-129">Method htmlEncode</span></span>

```xpp
public str htmlEncode(str txt)
```

### <a name="parameters---htmlencode"></a><span data-ttu-id="db837-130">パラメーター - htmlEncode</span><span class="sxs-lookup"><span data-stu-id="db837-130">Parameters - htmlEncode</span></span>

<span data-ttu-id="db837-131">txt</span><span class="sxs-lookup"><span data-stu-id="db837-131">txt</span></span>  

### <a name="return-value---htmlencode"></a><span data-ttu-id="db837-132">戻り値 - htmlEncode</span><span class="sxs-lookup"><span data-stu-id="db837-132">Return Value - htmlEncode</span></span>

## <a name="method-interface"></a><span data-ttu-id="db837-133">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="db837-133">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="db837-134">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="db837-134">Return Value - interface</span></span>

## <a name="method-mappath"></a><span data-ttu-id="db837-135">メソッド mapPath</span><span class="sxs-lookup"><span data-stu-id="db837-135">Method mapPath</span></span>

```xpp
public str mapPath(str logicalPath)
```

### <a name="parameters---mappath"></a><span data-ttu-id="db837-136">パラメーター - mapPath</span><span class="sxs-lookup"><span data-stu-id="db837-136">Parameters - mapPath</span></span>

<span data-ttu-id="db837-137">logicalPath</span><span class="sxs-lookup"><span data-stu-id="db837-137">logicalPath</span></span>  

### <a name="return-value---mappath"></a><span data-ttu-id="db837-138">戻り値 - mapPath</span><span class="sxs-lookup"><span data-stu-id="db837-138">Return Value - mapPath</span></span>

## <a name="method-scripttimeout"></a><span data-ttu-id="db837-139">メソッド scriptTimeout</span><span class="sxs-lookup"><span data-stu-id="db837-139">Method scriptTimeout</span></span>

```xpp
public int scriptTimeout([int timeoutSeconds])
```

### <a name="parameters---scripttimeout"></a><span data-ttu-id="db837-140">パラメーター - scriptTimeout</span><span class="sxs-lookup"><span data-stu-id="db837-140">Parameters - scriptTimeout</span></span>

<span data-ttu-id="db837-141">timeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="db837-141">timeoutSeconds</span></span>  

### <a name="return-value---scripttimeout"></a><span data-ttu-id="db837-142">戻り値 - scriptTimeout</span><span class="sxs-lookup"><span data-stu-id="db837-142">Return Value - scriptTimeout</span></span>

## <a name="method-urlencode"></a><span data-ttu-id="db837-143">メソッド urlEncode</span><span class="sxs-lookup"><span data-stu-id="db837-143">Method urlEncode</span></span>

```xpp
public str urlEncode(str txt)
```

### <a name="parameters---urlencode"></a><span data-ttu-id="db837-144">パラメーター - urlEncode</span><span class="sxs-lookup"><span data-stu-id="db837-144">Parameters - urlEncode</span></span>

<span data-ttu-id="db837-145">txt</span><span class="sxs-lookup"><span data-stu-id="db837-145">txt</span></span>  

### <a name="return-value---urlencode"></a><span data-ttu-id="db837-146">戻り値 - urlEncode</span><span class="sxs-lookup"><span data-stu-id="db837-146">Return Value - urlEncode</span></span>

## <a name="method-urlpathencode"></a><span data-ttu-id="db837-147">メソッド urlPathEncode</span><span class="sxs-lookup"><span data-stu-id="db837-147">Method urlPathEncode</span></span>

```xpp
public str urlPathEncode(str txt)
```

### <a name="parameters---urlpathencode"></a><span data-ttu-id="db837-148">パラメーター - urlPathEncode</span><span class="sxs-lookup"><span data-stu-id="db837-148">Parameters - urlPathEncode</span></span>

<span data-ttu-id="db837-149">txt</span><span class="sxs-lookup"><span data-stu-id="db837-149">txt</span></span>  

### <a name="return-value---urlpathencode"></a><span data-ttu-id="db837-150">戻り値 - urlPathEncode</span><span class="sxs-lookup"><span data-stu-id="db837-150">Return Value - urlPathEncode</span></span>

## <a name="method-execute"></a><span data-ttu-id="db837-151">メソッド execute</span><span class="sxs-lookup"><span data-stu-id="db837-151">Method execute</span></span>

```xpp
public void execute(str logicalPath)
```

### <a name="parameters---execute"></a><span data-ttu-id="db837-152">パラメーター - execute</span><span class="sxs-lookup"><span data-stu-id="db837-152">Parameters - execute</span></span>

<span data-ttu-id="db837-153">logicalPath</span><span class="sxs-lookup"><span data-stu-id="db837-153">logicalPath</span></span>  

## <a name="method-transfer"></a><span data-ttu-id="db837-154">メソッド transfer</span><span class="sxs-lookup"><span data-stu-id="db837-154">Method transfer</span></span>

```xpp
public void transfer(str logicalPath)
```

### <a name="parameters---transfer"></a><span data-ttu-id="db837-155">パラメーター - transfer</span><span class="sxs-lookup"><span data-stu-id="db837-155">Parameters - transfer</span></span>

<span data-ttu-id="db837-156">logicalPath</span><span class="sxs-lookup"><span data-stu-id="db837-156">logicalPath</span></span>  

## <a name="method-new"></a><span data-ttu-id="db837-157">メソッド new</span><span class="sxs-lookup"><span data-stu-id="db837-157">Method new</span></span>

<span data-ttu-id="db837-158">IISServer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="db837-158">Initializes a new instance of the IISServer class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="db837-159">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="db837-159">Method finalize</span></span>

```xpp
public void finalize()
```

