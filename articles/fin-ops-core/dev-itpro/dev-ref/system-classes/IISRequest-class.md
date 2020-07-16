---
title: IISRequest クラス
description: このトピックでは、IISRequest クラスについて説明します。
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
ms.openlocfilehash: 40e951d8a42d14cd6399d324414d2264010036dd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502603"
---
# <a name="class-iisrequest"></a><span data-ttu-id="e47c4-103">クラス IISRequest</span><span class="sxs-lookup"><span data-stu-id="e47c4-103">Class IISRequest</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISRequest extends Object
```

<span data-ttu-id="e47c4-104">IISRequest クラスは、インターネット インフォメーション サービス (IIS) によって提供される Request オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="e47c4-104">The IISRequest class wraps the Request object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="e47c4-105">備考</span><span class="sxs-lookup"><span data-stu-id="e47c4-105">Remarks</span></span>

<span data-ttu-id="e47c4-106">IISRequest クラスのメソッドと、IIS によって提供される Request オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="e47c4-106">There is a one-to-one connection between the methods of the IISRequest class and the methods of the Request object that is offered by IIS.</span></span> <span data-ttu-id="e47c4-107">したがって、IISRequest クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e47c4-107">Therefore, for more information about the methods of the IISRequest class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="e47c4-108">IISRequest クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="e47c4-108">Use of the IISRequest class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="e47c4-109">例</span><span class="sxs-lookup"><span data-stu-id="e47c4-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e47c4-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="e47c4-110">Methods</span></span>

| <span data-ttu-id="e47c4-111">方法</span><span class="sxs-lookup"><span data-stu-id="e47c4-111">Method</span></span>                                               | <span data-ttu-id="e47c4-112">説明</span><span class="sxs-lookup"><span data-stu-id="e47c4-112">Description</span></span>                                         |
|------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="e47c4-113">public COMVariant binaryRead(COMVariant countToRead)</span><span class="sxs-lookup"><span data-stu-id="e47c4-113">public COMVariant binaryRead(COMVariant countToRead)</span></span> |                                                     |
| <span data-ttu-id="e47c4-114">public IISRequestDictionary clientCertificate()</span><span class="sxs-lookup"><span data-stu-id="e47c4-114">public IISRequestDictionary clientCertificate()</span></span>      |                                                     |
| <span data-ttu-id="e47c4-115">public IISRequestDictionary cookies()</span><span class="sxs-lookup"><span data-stu-id="e47c4-115">public IISRequestDictionary cookies()</span></span>                |                                                     |
| <span data-ttu-id="e47c4-116">public IISPostedFile file(COMVariant index)</span><span class="sxs-lookup"><span data-stu-id="e47c4-116">public IISPostedFile file(COMVariant index)</span></span>          |                                                     |
| <span data-ttu-id="e47c4-117">public int fileCount()</span><span class="sxs-lookup"><span data-stu-id="e47c4-117">public int fileCount()</span></span>                               |                                                     |
| <span data-ttu-id="e47c4-118">public IISRequestDictionary form()</span><span class="sxs-lookup"><span data-stu-id="e47c4-118">public IISRequestDictionary form()</span></span>                   |                                                     |
| <span data-ttu-id="e47c4-119">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="e47c4-119">public ComInterface interface()</span></span>                      |                                                     |
| <span data-ttu-id="e47c4-120">public str item(str item)</span><span class="sxs-lookup"><span data-stu-id="e47c4-120">public str item(str item)</span></span>                            |                                                     |
| <span data-ttu-id="e47c4-121">public IISRequestDictionary queryString()</span><span class="sxs-lookup"><span data-stu-id="e47c4-121">public IISRequestDictionary queryString()</span></span>            |                                                     |
| <span data-ttu-id="e47c4-122">public IISRequestDictionary serverVariables()</span><span class="sxs-lookup"><span data-stu-id="e47c4-122">public IISRequestDictionary serverVariables()</span></span>        |                                                     |
| <span data-ttu-id="e47c4-123">public int totalBytes()</span><span class="sxs-lookup"><span data-stu-id="e47c4-123">public int totalBytes()</span></span>                              |                                                     |
| <span data-ttu-id="e47c4-124">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="e47c4-124">public void finalize()</span></span>                               |                                                     |
| <span data-ttu-id="e47c4-125">public void new()</span><span class="sxs-lookup"><span data-stu-id="e47c4-125">public void new()</span></span>                                    | <span data-ttu-id="e47c4-126">IISRequest クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e47c4-126">Initializes a new instance of the IISRequest class.</span></span> |

## <a name="method-binaryread"></a><span data-ttu-id="e47c4-127">メソッド binaryRead</span><span class="sxs-lookup"><span data-stu-id="e47c4-127">Method binaryRead</span></span>

```xpp
public COMVariant binaryRead(COMVariant countToRead)
```

### <a name="parameters---binaryread"></a><span data-ttu-id="e47c4-128">パラメーター - binaryRead</span><span class="sxs-lookup"><span data-stu-id="e47c4-128">Parameters - binaryRead</span></span>

<span data-ttu-id="e47c4-129">countToRead</span><span class="sxs-lookup"><span data-stu-id="e47c4-129">countToRead</span></span>  

### <a name="return-value---binaryread"></a><span data-ttu-id="e47c4-130">戻り値-binaryRead</span><span class="sxs-lookup"><span data-stu-id="e47c4-130">Return Value - binaryRead</span></span>

## <a name="method-clientcertificate"></a><span data-ttu-id="e47c4-131">メソッド clientCertificate</span><span class="sxs-lookup"><span data-stu-id="e47c4-131">Method clientCertificate</span></span>

```xpp
public IISRequestDictionary clientCertificate()
```

### <a name="return-value---clientcertificate"></a><span data-ttu-id="e47c4-132">戻り値 - clientCertificate</span><span class="sxs-lookup"><span data-stu-id="e47c4-132">Return Value - clientCertificate</span></span>

## <a name="method-cookies"></a><span data-ttu-id="e47c4-133">メソッド cookies</span><span class="sxs-lookup"><span data-stu-id="e47c4-133">Method cookies</span></span>

```xpp
public IISRequestDictionary cookies()
```

### <a name="return-value---cookies"></a><span data-ttu-id="e47c4-134">戻り値 - cookie</span><span class="sxs-lookup"><span data-stu-id="e47c4-134">Return Value - cookies</span></span>

## <a name="method-file"></a><span data-ttu-id="e47c4-135">メソッド file</span><span class="sxs-lookup"><span data-stu-id="e47c4-135">Method file</span></span>

```xpp
public IISPostedFile file(COMVariant index)
```

### <a name="parameters---file"></a><span data-ttu-id="e47c4-136">パラメーター - file</span><span class="sxs-lookup"><span data-stu-id="e47c4-136">Parameters - file</span></span>

<span data-ttu-id="e47c4-137">指数</span><span class="sxs-lookup"><span data-stu-id="e47c4-137">index</span></span>  

### <a name="return-value---file"></a><span data-ttu-id="e47c4-138">戻り値 - file</span><span class="sxs-lookup"><span data-stu-id="e47c4-138">Return Value - file</span></span>

## <a name="method-filecount"></a><span data-ttu-id="e47c4-139">メソッド fileCount</span><span class="sxs-lookup"><span data-stu-id="e47c4-139">Method fileCount</span></span>

```xpp
public int fileCount()
```

### <a name="return-value---filecount"></a><span data-ttu-id="e47c4-140">戻り値 - fileCount</span><span class="sxs-lookup"><span data-stu-id="e47c4-140">Return Value - fileCount</span></span>

## <a name="method-form"></a><span data-ttu-id="e47c4-141">メソッド form</span><span class="sxs-lookup"><span data-stu-id="e47c4-141">Method form</span></span>

```xpp
public IISRequestDictionary form()
```

### <a name="return-value---form"></a><span data-ttu-id="e47c4-142">戻り値 - form</span><span class="sxs-lookup"><span data-stu-id="e47c4-142">Return Value - form</span></span>

## <a name="method-interface"></a><span data-ttu-id="e47c4-143">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="e47c4-143">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="e47c4-144">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="e47c4-144">Return Value - interface</span></span>

## <a name="method-item"></a><span data-ttu-id="e47c4-145">メソッド item</span><span class="sxs-lookup"><span data-stu-id="e47c4-145">Method item</span></span>

```xpp
public str item(str item)
```

### <a name="parameters---item"></a><span data-ttu-id="e47c4-146">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="e47c4-146">Parameters - item</span></span>

<span data-ttu-id="e47c4-147">品目</span><span class="sxs-lookup"><span data-stu-id="e47c4-147">item</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="e47c4-148">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="e47c4-148">Return Value - item</span></span>

## <a name="method-querystring"></a><span data-ttu-id="e47c4-149">メソッド queryString</span><span class="sxs-lookup"><span data-stu-id="e47c4-149">Method queryString</span></span>

```xpp
public IISRequestDictionary queryString()
```

### <a name="return-value---querystring"></a><span data-ttu-id="e47c4-150">戻り値 - queryString</span><span class="sxs-lookup"><span data-stu-id="e47c4-150">Return Value - queryString</span></span>

## <a name="method-servervariables"></a><span data-ttu-id="e47c4-151">メソッド serverVariables</span><span class="sxs-lookup"><span data-stu-id="e47c4-151">Method serverVariables</span></span>

```xpp
public IISRequestDictionary serverVariables()
```

### <a name="return-value---servervariables"></a><span data-ttu-id="e47c4-152">戻り値 - serverVariables</span><span class="sxs-lookup"><span data-stu-id="e47c4-152">Return Value - serverVariables</span></span>

## <a name="method-totalbytes"></a><span data-ttu-id="e47c4-153">メソッド totalBytes</span><span class="sxs-lookup"><span data-stu-id="e47c4-153">Method totalBytes</span></span>

```xpp
public int totalBytes()
```

### <a name="return-value---totalbytes"></a><span data-ttu-id="e47c4-154">戻り値 - totalBytes</span><span class="sxs-lookup"><span data-stu-id="e47c4-154">Return Value - totalBytes</span></span>

## <a name="method-finalize"></a><span data-ttu-id="e47c4-155">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="e47c4-155">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="e47c4-156">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e47c4-156">Method new</span></span>

<span data-ttu-id="e47c4-157">IISRequest クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e47c4-157">Initializes a new instance of the IISRequest class.</span></span>

```xpp
public void new()
```

