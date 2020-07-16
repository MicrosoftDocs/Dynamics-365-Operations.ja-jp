---
title: IISResponse クラス
description: このトピックでは、IISResponse クラスについて説明します。
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
ms.openlocfilehash: e339d0d9d7d93a68b8d0ea268a430e1854e8c97c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502602"
---
# <a name="class-iisresponse"></a><span data-ttu-id="50f24-103">クラス IISResponse</span><span class="sxs-lookup"><span data-stu-id="50f24-103">Class IISResponse</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISResponse extends Object
```

<span data-ttu-id="50f24-104">IISResponse クラスは、インターネット インフォメーション サービス (IIS) によって提供される Response オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="50f24-104">The IISResponse class wraps the Response object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="50f24-105">備考</span><span class="sxs-lookup"><span data-stu-id="50f24-105">Remarks</span></span>

<span data-ttu-id="50f24-106">IISResponse クラスのメソッドと、IIS によって提供される Response オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。</span><span class="sxs-lookup"><span data-stu-id="50f24-106">There is a one-to-one relationship between the methods of the IISResponse class and the methods of the Response object that is offered by IIS.</span></span> <span data-ttu-id="50f24-107">したがって、IISResponse クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="50f24-107">Therefore, for more information about the methods of the IISResponse class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="50f24-108">IISResponse クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="50f24-108">Use of the IISResponse class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="50f24-109">例</span><span class="sxs-lookup"><span data-stu-id="50f24-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="50f24-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="50f24-110">Methods</span></span>

| <span data-ttu-id="50f24-111">方法</span><span class="sxs-lookup"><span data-stu-id="50f24-111">Method</span></span>                                                    | <span data-ttu-id="50f24-112">説明</span><span class="sxs-lookup"><span data-stu-id="50f24-112">Description</span></span>                                          |
|-----------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50f24-113">public boolean buffer(\[boolean isBuffering\])</span><span class="sxs-lookup"><span data-stu-id="50f24-113">public boolean buffer(\[boolean isBuffering\])</span></span>            |                                                      |
| <span data-ttu-id="50f24-114">public str cacheControl(\[str cacheControl\])</span><span class="sxs-lookup"><span data-stu-id="50f24-114">public str cacheControl(\[str cacheControl\])</span></span>             |                                                      |
| <span data-ttu-id="50f24-115">public boolean cacheWrite(\[boolean cache\])</span><span class="sxs-lookup"><span data-stu-id="50f24-115">public boolean cacheWrite(\[boolean cache\])</span></span>              |                                                      |
| <span data-ttu-id="50f24-116">public str charSet(\[str charSet\])</span><span class="sxs-lookup"><span data-stu-id="50f24-116">public str charSet(\[str charSet\])</span></span>                       |                                                      |
| <span data-ttu-id="50f24-117">public str contentType(\[str contentType\])</span><span class="sxs-lookup"><span data-stu-id="50f24-117">public str contentType(\[str contentType\])</span></span>               |                                                      |
| <span data-ttu-id="50f24-118">public IISRequestDictionary cookies()</span><span class="sxs-lookup"><span data-stu-id="50f24-118">public IISRequestDictionary cookies()</span></span>                     |                                                      |
| <span data-ttu-id="50f24-119">public int expires(\[int expiresMinutes\])</span><span class="sxs-lookup"><span data-stu-id="50f24-119">public int expires(\[int expiresMinutes\])</span></span>                |                                                      |
| <span data-ttu-id="50f24-120">public COMVariant expiresAbsolute(\[COMVariant expires\])</span><span class="sxs-lookup"><span data-stu-id="50f24-120">public COMVariant expiresAbsolute(\[COMVariant expires\])</span></span> |                                                      |
| <span data-ttu-id="50f24-121">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="50f24-121">public ComInterface interface()</span></span>                           |                                                      |
| <span data-ttu-id="50f24-122">public boolean isClientConnected()</span><span class="sxs-lookup"><span data-stu-id="50f24-122">public boolean isClientConnected()</span></span>                        |                                                      |
| <span data-ttu-id="50f24-123">public str status(\[str status\])</span><span class="sxs-lookup"><span data-stu-id="50f24-123">public str status(\[str status\])</span></span>                         | <span data-ttu-id="50f24-124">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50f24-124">Gets or sets the status of an object.</span></span>                |
| <span data-ttu-id="50f24-125">public void addHeader(str headerName, str headerValue)</span><span class="sxs-lookup"><span data-stu-id="50f24-125">public void addHeader(str headerName, str headerValue)</span></span>    |                                                      |
| <span data-ttu-id="50f24-126">public void writeTxt(str text)</span><span class="sxs-lookup"><span data-stu-id="50f24-126">public void writeTxt(str text)</span></span>                            |                                                      |
| <span data-ttu-id="50f24-127">public void write(COMVariant text)</span><span class="sxs-lookup"><span data-stu-id="50f24-127">public void write(COMVariant text)</span></span>                        |                                                      |
| <span data-ttu-id="50f24-128">public void clear()</span><span class="sxs-lookup"><span data-stu-id="50f24-128">public void clear()</span></span>                                       |                                                      |
| <span data-ttu-id="50f24-129">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="50f24-129">public void finalize()</span></span>                                    |                                                      |
| <span data-ttu-id="50f24-130">public void binaryWrite(COMVariant input)</span><span class="sxs-lookup"><span data-stu-id="50f24-130">public void binaryWrite(COMVariant input)</span></span>                 |                                                      |
| <span data-ttu-id="50f24-131">public void appendToLog(str logEntry)</span><span class="sxs-lookup"><span data-stu-id="50f24-131">public void appendToLog(str logEntry)</span></span>                     |                                                      |
| <span data-ttu-id="50f24-132">public void new()</span><span class="sxs-lookup"><span data-stu-id="50f24-132">public void new()</span></span>                                         | <span data-ttu-id="50f24-133">IISResponse クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50f24-133">Initializes a new instance of the IISResponse class.</span></span> |
| <span data-ttu-id="50f24-134">public void redirect(str url)</span><span class="sxs-lookup"><span data-stu-id="50f24-134">public void redirect(str url)</span></span>                             |                                                      |
| <span data-ttu-id="50f24-135">public void flush()</span><span class="sxs-lookup"><span data-stu-id="50f24-135">public void flush()</span></span>                                       |                                                      |
| <span data-ttu-id="50f24-136">public void pics(str headerValue)</span><span class="sxs-lookup"><span data-stu-id="50f24-136">public void pics(str headerValue)</span></span>                         |                                                      |
| <span data-ttu-id="50f24-137">public void end()</span><span class="sxs-lookup"><span data-stu-id="50f24-137">public void end()</span></span>                                         |                                                      |

## <a name="method-buffer"></a><span data-ttu-id="50f24-138">メソッド buffer</span><span class="sxs-lookup"><span data-stu-id="50f24-138">Method buffer</span></span>

```xpp
public boolean buffer([boolean isBuffering])
```

### <a name="parameters---buffer"></a><span data-ttu-id="50f24-139">パラメーター - buffer</span><span class="sxs-lookup"><span data-stu-id="50f24-139">Parameters - buffer</span></span>

<span data-ttu-id="50f24-140">isBuffering</span><span class="sxs-lookup"><span data-stu-id="50f24-140">isBuffering</span></span>  

### <a name="return-value---buffer"></a><span data-ttu-id="50f24-141">戻り値 - buffer</span><span class="sxs-lookup"><span data-stu-id="50f24-141">Return Value - buffer</span></span>

## <a name="method-cachecontrol"></a><span data-ttu-id="50f24-142">メソッド cacheControl</span><span class="sxs-lookup"><span data-stu-id="50f24-142">Method cacheControl</span></span>

```xpp
public str cacheControl([str cacheControl])
```

### <a name="parameters---cachecontrol"></a><span data-ttu-id="50f24-143">パラメーター - cacheControl</span><span class="sxs-lookup"><span data-stu-id="50f24-143">Parameters - cacheControl</span></span>

<span data-ttu-id="50f24-144">cacheControl</span><span class="sxs-lookup"><span data-stu-id="50f24-144">cacheControl</span></span>  

### <a name="return-value---cachecontrol"></a><span data-ttu-id="50f24-145">戻り値 - cacheControl</span><span class="sxs-lookup"><span data-stu-id="50f24-145">Return Value - cacheControl</span></span>

## <a name="method-cachewrite"></a><span data-ttu-id="50f24-146">メソッド cacheWrite</span><span class="sxs-lookup"><span data-stu-id="50f24-146">Method cacheWrite</span></span>

```xpp
public boolean cacheWrite([boolean cache])
```

### <a name="parameters---cachewrite"></a><span data-ttu-id="50f24-147">パラメーター - cacheWrite</span><span class="sxs-lookup"><span data-stu-id="50f24-147">Parameters - cacheWrite</span></span>

<span data-ttu-id="50f24-148">cache</span><span class="sxs-lookup"><span data-stu-id="50f24-148">cache</span></span>  

### <a name="return-value---cachewrite"></a><span data-ttu-id="50f24-149">戻り値 - cacheWrite</span><span class="sxs-lookup"><span data-stu-id="50f24-149">Return Value - cacheWrite</span></span>

## <a name="method-charset"></a><span data-ttu-id="50f24-150">メソッド charSet</span><span class="sxs-lookup"><span data-stu-id="50f24-150">Method charSet</span></span>

```xpp
public str charSet([str charSet])
```

### <a name="parameters---charset"></a><span data-ttu-id="50f24-151">パラメーター - charSet</span><span class="sxs-lookup"><span data-stu-id="50f24-151">Parameters - charSet</span></span>

<span data-ttu-id="50f24-152">charSet</span><span class="sxs-lookup"><span data-stu-id="50f24-152">charSet</span></span>  

### <a name="return-value---charset"></a><span data-ttu-id="50f24-153">戻り値 - charSet</span><span class="sxs-lookup"><span data-stu-id="50f24-153">Return Value - charSet</span></span>

## <a name="method-contenttype"></a><span data-ttu-id="50f24-154">メソッド contentType</span><span class="sxs-lookup"><span data-stu-id="50f24-154">Method contentType</span></span>

```xpp
public str contentType([str contentType])
```

### <a name="parameters---contenttype"></a><span data-ttu-id="50f24-155">パラメーター - contentType</span><span class="sxs-lookup"><span data-stu-id="50f24-155">Parameters - contentType</span></span>

<span data-ttu-id="50f24-156">contentType</span><span class="sxs-lookup"><span data-stu-id="50f24-156">contentType</span></span>  

### <a name="return-value---contenttype"></a><span data-ttu-id="50f24-157">戻り値 - contentType</span><span class="sxs-lookup"><span data-stu-id="50f24-157">Return Value - contentType</span></span>

## <a name="method-cookies"></a><span data-ttu-id="50f24-158">メソッド cookies</span><span class="sxs-lookup"><span data-stu-id="50f24-158">Method cookies</span></span>

```xpp
public IISRequestDictionary cookies()
```

### <a name="return-value---cookies"></a><span data-ttu-id="50f24-159">戻り値 - cookie</span><span class="sxs-lookup"><span data-stu-id="50f24-159">Return Value - cookies</span></span>

## <a name="method-expires"></a><span data-ttu-id="50f24-160">メソッド expires</span><span class="sxs-lookup"><span data-stu-id="50f24-160">Method expires</span></span>

```xpp
public int expires([int expiresMinutes])
```

### <a name="parameters---expires"></a><span data-ttu-id="50f24-161">パラメーター - expires</span><span class="sxs-lookup"><span data-stu-id="50f24-161">Parameters - expires</span></span>

<span data-ttu-id="50f24-162">expiresMinutes</span><span class="sxs-lookup"><span data-stu-id="50f24-162">expiresMinutes</span></span>  

### <a name="return-value---expires"></a><span data-ttu-id="50f24-163">戻り値 - expires</span><span class="sxs-lookup"><span data-stu-id="50f24-163">Return Value - expires</span></span>

## <a name="method-expiresabsolute"></a><span data-ttu-id="50f24-164">メソッド expiresAbsolute</span><span class="sxs-lookup"><span data-stu-id="50f24-164">Method expiresAbsolute</span></span>

```xpp
public COMVariant expiresAbsolute([COMVariant expires])
```

### <a name="parameters---expiresabsolute"></a><span data-ttu-id="50f24-165">パラメーター - expiresAbsolute</span><span class="sxs-lookup"><span data-stu-id="50f24-165">Parameters - expiresAbsolute</span></span>

<span data-ttu-id="50f24-166">expires</span><span class="sxs-lookup"><span data-stu-id="50f24-166">expires</span></span>  

### <a name="return-value---expiresabsolute"></a><span data-ttu-id="50f24-167">戻り値 - expiresAbsolute</span><span class="sxs-lookup"><span data-stu-id="50f24-167">Return Value - expiresAbsolute</span></span>

## <a name="method-interface"></a><span data-ttu-id="50f24-168">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="50f24-168">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="50f24-169">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="50f24-169">Return Value - interface</span></span>

## <a name="method-isclientconnected"></a><span data-ttu-id="50f24-170">メソッド isClientConnected</span><span class="sxs-lookup"><span data-stu-id="50f24-170">Method isClientConnected</span></span>

```xpp
public boolean isClientConnected()
```

### <a name="return-value---isclientconnected"></a><span data-ttu-id="50f24-171">戻り値 - isClientConnected</span><span class="sxs-lookup"><span data-stu-id="50f24-171">Return Value - isClientConnected</span></span>

## <a name="method-status"></a><span data-ttu-id="50f24-172">メソッド status</span><span class="sxs-lookup"><span data-stu-id="50f24-172">Method status</span></span>

<span data-ttu-id="50f24-173">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50f24-173">Gets or sets the status of an object.</span></span>

```xpp
public str status([str status])
```

### <a name="parameters---status"></a><span data-ttu-id="50f24-174">パラメーター - status</span><span class="sxs-lookup"><span data-stu-id="50f24-174">Parameters - status</span></span>

<span data-ttu-id="50f24-175">状態</span><span class="sxs-lookup"><span data-stu-id="50f24-175">status</span></span>  

### <a name="return-value---status"></a><span data-ttu-id="50f24-176">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="50f24-176">Return Value - status</span></span>

<span data-ttu-id="50f24-177">オブジェクトのステータスの現在の値。</span><span class="sxs-lookup"><span data-stu-id="50f24-177">The current value of the status of the object.</span></span>

## <a name="method-addheader"></a><span data-ttu-id="50f24-178">メソッド addHeader</span><span class="sxs-lookup"><span data-stu-id="50f24-178">Method addHeader</span></span>

```xpp
public void addHeader(str headerName, str headerValue)
```

### <a name="parameters---addheader"></a><span data-ttu-id="50f24-179">パラメーター - addHeader</span><span class="sxs-lookup"><span data-stu-id="50f24-179">Parameters - addHeader</span></span>

<span data-ttu-id="50f24-180">headerName</span><span class="sxs-lookup"><span data-stu-id="50f24-180">headerName</span></span>  

<!-- -->

<span data-ttu-id="50f24-181">headerValue</span><span class="sxs-lookup"><span data-stu-id="50f24-181">headerValue</span></span>  

## <a name="method-writetxt"></a><span data-ttu-id="50f24-182">メソッド writeTxt</span><span class="sxs-lookup"><span data-stu-id="50f24-182">Method writeTxt</span></span>

```xpp
public void writeTxt(str text)
```

### <a name="parameters---writetxt"></a><span data-ttu-id="50f24-183">パラメーター - writeTxt</span><span class="sxs-lookup"><span data-stu-id="50f24-183">Parameters - writeTxt</span></span>

<span data-ttu-id="50f24-184">テキスト</span><span class="sxs-lookup"><span data-stu-id="50f24-184">text</span></span>  

## <a name="method-write"></a><span data-ttu-id="50f24-185">メソッド write</span><span class="sxs-lookup"><span data-stu-id="50f24-185">Method write</span></span>

```xpp
public void write(COMVariant text)
```

### <a name="parameters---write"></a><span data-ttu-id="50f24-186">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="50f24-186">Parameters - write</span></span>

<span data-ttu-id="50f24-187">テキスト</span><span class="sxs-lookup"><span data-stu-id="50f24-187">text</span></span>  

## <a name="method-clear"></a><span data-ttu-id="50f24-188">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="50f24-188">Method clear</span></span>

```xpp
public void clear()
```

## <a name="method-finalize"></a><span data-ttu-id="50f24-189">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="50f24-189">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-binarywrite"></a><span data-ttu-id="50f24-190">メソッド binaryWrite</span><span class="sxs-lookup"><span data-stu-id="50f24-190">Method binaryWrite</span></span>

```xpp
public void binaryWrite(COMVariant input)
```

### <a name="parameters---binarywrite"></a><span data-ttu-id="50f24-191">パラメーター - binaryWrite</span><span class="sxs-lookup"><span data-stu-id="50f24-191">Parameters - binaryWrite</span></span>

<span data-ttu-id="50f24-192">入力</span><span class="sxs-lookup"><span data-stu-id="50f24-192">input</span></span>  

## <a name="method-appendtolog"></a><span data-ttu-id="50f24-193">メソッド appendToLog</span><span class="sxs-lookup"><span data-stu-id="50f24-193">Method appendToLog</span></span>

```xpp
public void appendToLog(str logEntry)
```

### <a name="parameters---appendtolog"></a><span data-ttu-id="50f24-194">パラメーター - appendToLog</span><span class="sxs-lookup"><span data-stu-id="50f24-194">Parameters - appendToLog</span></span>

<span data-ttu-id="50f24-195">logEntry</span><span class="sxs-lookup"><span data-stu-id="50f24-195">logEntry</span></span>  

## <a name="method-new"></a><span data-ttu-id="50f24-196">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50f24-196">Method new</span></span>

<span data-ttu-id="50f24-197">IISResponse クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50f24-197">Initializes a new instance of the IISResponse class.</span></span>

```xpp
public void new()
```

## <a name="method-redirect"></a><span data-ttu-id="50f24-198">メソッド redirect</span><span class="sxs-lookup"><span data-stu-id="50f24-198">Method redirect</span></span>

```xpp
public void redirect(str url)
```

### <a name="parameters---redirect"></a><span data-ttu-id="50f24-199">パラメーター - redirect</span><span class="sxs-lookup"><span data-stu-id="50f24-199">Parameters - redirect</span></span>

<span data-ttu-id="50f24-200">URL</span><span class="sxs-lookup"><span data-stu-id="50f24-200">url</span></span>  

## <a name="method-flush"></a><span data-ttu-id="50f24-201">メソッド flush</span><span class="sxs-lookup"><span data-stu-id="50f24-201">Method flush</span></span>

```xpp
public void flush()
```

## <a name="method-pics"></a><span data-ttu-id="50f24-202">メソッド pics</span><span class="sxs-lookup"><span data-stu-id="50f24-202">Method pics</span></span>

```xpp
public void pics(str headerValue)
```

### <a name="parameters---pics"></a><span data-ttu-id="50f24-203">パラメーター - pics</span><span class="sxs-lookup"><span data-stu-id="50f24-203">Parameters - pics</span></span>

<span data-ttu-id="50f24-204">headerValue</span><span class="sxs-lookup"><span data-stu-id="50f24-204">headerValue</span></span>  

## <a name="method-end"></a><span data-ttu-id="50f24-205">メソッド end</span><span class="sxs-lookup"><span data-stu-id="50f24-205">Method end</span></span>

```xpp
public void end()
```

