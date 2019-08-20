---
title: I クラス
description: 文字 I で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52171
ms.assetid: bd6df991-7b90-40f0-b342-025ab000c24c
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ab52979b7ed4c69a3a1bcd28ab0b9a70f1ed074
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833676"
---
# <a name="i-classes"></a><span data-ttu-id="31dce-103">I クラス</span><span class="sxs-lookup"><span data-stu-id="31dce-103">I classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31dce-104">文字 I で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="31dce-104">System API classes that start with the letter I.</span></span>

<a name="class-idispatcherproxy"></a><span data-ttu-id="31dce-105">クラス IDispatcherProxy</span><span class="sxs-lookup"><span data-stu-id="31dce-105">Class IDispatcherProxy</span></span>
----------------------

    class IDispatcherProxy

### <a name="remarks"></a><span data-ttu-id="31dce-106">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-107">例</span><span class="sxs-lookup"><span data-stu-id="31dce-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-108">Methods</span></span>

| <span data-ttu-id="31dce-109">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-109">Method</span></span>                                         | <span data-ttu-id="31dce-110">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-110">Description</span></span> |
|------------------------------------------------|-------------|
| <span data-ttu-id="31dce-111">public AnyType invoke(str methodName, VarArg )</span><span class="sxs-lookup"><span data-stu-id="31dce-111">public AnyType invoke(str methodName, VarArg )</span></span> |             |
| <span data-ttu-id="31dce-112">public void refresh()</span><span class="sxs-lookup"><span data-stu-id="31dce-112">public void refresh()</span></span>                          |             |

### <a name="method-invoke"></a><span data-ttu-id="31dce-113">メソッド invoke</span><span class="sxs-lookup"><span data-stu-id="31dce-113">Method invoke</span></span>

    public AnyType invoke(str methodName, VarArg )

#### <a name="parameters"></a><span data-ttu-id="31dce-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-114">Parameters</span></span>

<span data-ttu-id="31dce-115">methodName</span><span class="sxs-lookup"><span data-stu-id="31dce-115">methodName</span></span>  

<!-- -->



#### <a name="return-value"></a><span data-ttu-id="31dce-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-116">Return Value</span></span>

### <a name="method-refresh"></a><span data-ttu-id="31dce-117">メソッド refresh</span><span class="sxs-lookup"><span data-stu-id="31dce-117">Method refresh</span></span>

    public void refresh()

## <a name="class-iisapplicationobject"></a><span data-ttu-id="31dce-118">クラス IISApplicationObject</span><span class="sxs-lookup"><span data-stu-id="31dce-118">Class IISApplicationObject</span></span>
    class IISApplicationObject extends Object

<span data-ttu-id="31dce-119">IISApplicationObject クラスは、インターネット インフォメーション サービス (IIS) によって提供されるアプリケーション オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-119">The IISApplicationObject class wraps the Application object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-120">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-120">Remarks</span></span>

<span data-ttu-id="31dce-121">IISApplicationObject クラスのメソッドと、IIS によって提供される Application オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-121">There is a one-to-one connection between the methods of the IISApplicationObject class and the methods of the Application object that is offered by IIS.</span></span> <span data-ttu-id="31dce-122">したがって、IISApplicationObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-122">Therefore, for more information about the methods of the IISApplicationObject class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-123">IISApplicationObject クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-123">Use of the IISApplicationObject class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-124">例</span><span class="sxs-lookup"><span data-stu-id="31dce-124">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-125">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-125">Methods</span></span>

| <span data-ttu-id="31dce-126">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-126">Method</span></span>                                                 | <span data-ttu-id="31dce-127">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-127">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31dce-128">public IISVariantDictionary contents()</span><span class="sxs-lookup"><span data-stu-id="31dce-128">public IISVariantDictionary contents()</span></span>                 |                                                               |
| <span data-ttu-id="31dce-129">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-129">public ComInterface interface()</span></span>                        |                                                               |
| <span data-ttu-id="31dce-130">public IISVariantDictionary staticObjects()</span><span class="sxs-lookup"><span data-stu-id="31dce-130">public IISVariantDictionary staticObjects()</span></span>            |                                                               |
| <span data-ttu-id="31dce-131">public COMVariant value(str value, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-131">public COMVariant value(str value, \[COMVariant var\])</span></span> |                                                               |
| <span data-ttu-id="31dce-132">public str valueTxt(str value, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-132">public str valueTxt(str value, \[str var\])</span></span>            |                                                               |
| <span data-ttu-id="31dce-133">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-133">public void new()</span></span>                                      | <span data-ttu-id="31dce-134">IISApplicationObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-134">Initializes a new instance of the IISApplicationObject class.</span></span> |
| <span data-ttu-id="31dce-135">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-135">public void finalize()</span></span>                                 |                                                               |
| <span data-ttu-id="31dce-136">public void lock()</span><span class="sxs-lookup"><span data-stu-id="31dce-136">public void lock()</span></span>                                     |                                                               |
| <span data-ttu-id="31dce-137">public void unLock()</span><span class="sxs-lookup"><span data-stu-id="31dce-137">public void unLock()</span></span>                                   |                                                               |

### <a name="method-contents"></a><span data-ttu-id="31dce-138">メソッド contents</span><span class="sxs-lookup"><span data-stu-id="31dce-138">Method contents</span></span>

    public IISVariantDictionary contents()

#### <a name="return-value"></a><span data-ttu-id="31dce-139">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-139">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-140">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-140">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-141">Return Value</span></span>

### <a name="method-staticobjects"></a><span data-ttu-id="31dce-142">メソッド staticObjects</span><span class="sxs-lookup"><span data-stu-id="31dce-142">Method staticObjects</span></span>

    public IISVariantDictionary staticObjects()

#### <a name="return-value"></a><span data-ttu-id="31dce-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-143">Return Value</span></span>

### <a name="method-value"></a><span data-ttu-id="31dce-144">メソッド value</span><span class="sxs-lookup"><span data-stu-id="31dce-144">Method value</span></span>

    public COMVariant value(str value, [COMVariant var])

#### <a name="parameters"></a><span data-ttu-id="31dce-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-145">Parameters</span></span>

<span data-ttu-id="31dce-146">値</span><span class="sxs-lookup"><span data-stu-id="31dce-146">value</span></span>  

<!-- -->

<span data-ttu-id="31dce-147">var</span><span class="sxs-lookup"><span data-stu-id="31dce-147">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-148">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-148">Return Value</span></span>

### <a name="method-valuetxt"></a><span data-ttu-id="31dce-149">メソッド valueTxt</span><span class="sxs-lookup"><span data-stu-id="31dce-149">Method valueTxt</span></span>

    public str valueTxt(str value, [str var])

#### <a name="parameters"></a><span data-ttu-id="31dce-150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-150">Parameters</span></span>

<span data-ttu-id="31dce-151">値</span><span class="sxs-lookup"><span data-stu-id="31dce-151">value</span></span>  

<!-- -->

<span data-ttu-id="31dce-152">var</span><span class="sxs-lookup"><span data-stu-id="31dce-152">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-153">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-153">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-154">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-154">Method new</span></span>

<span data-ttu-id="31dce-155">IISApplicationObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-155">Initializes a new instance of the IISApplicationObject class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="31dce-156">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-156">Method finalize</span></span>

    public void finalize()

### <a name="method-lock"></a><span data-ttu-id="31dce-157">メソッド lock</span><span class="sxs-lookup"><span data-stu-id="31dce-157">Method lock</span></span>

    public void lock()

### <a name="method-unlock"></a><span data-ttu-id="31dce-158">メソッド unLock</span><span class="sxs-lookup"><span data-stu-id="31dce-158">Method unLock</span></span>

    public void unLock()

## <a name="class-iiscontextobject"></a><span data-ttu-id="31dce-159">クラス IISContextObject</span><span class="sxs-lookup"><span data-stu-id="31dce-159">Class IISContextObject</span></span>
    class IISContextObject extends Object

### <a name="remarks"></a><span data-ttu-id="31dce-160">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-160">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-161">例</span><span class="sxs-lookup"><span data-stu-id="31dce-161">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-162">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-162">Methods</span></span>

| <span data-ttu-id="31dce-163">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-163">Method</span></span>                                                 | <span data-ttu-id="31dce-164">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-164">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="31dce-165">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-165">public ComInterface interface()</span></span>                        |                                                           |
| <span data-ttu-id="31dce-166">public boolean isTraceEnabled()</span><span class="sxs-lookup"><span data-stu-id="31dce-166">public boolean isTraceEnabled()</span></span>                        |                                                           |
| <span data-ttu-id="31dce-167">public IISVariantDictionary items()</span><span class="sxs-lookup"><span data-stu-id="31dce-167">public IISVariantDictionary items()</span></span>                    |                                                           |
| <span data-ttu-id="31dce-168">public int traceMode(int mode)</span><span class="sxs-lookup"><span data-stu-id="31dce-168">public int traceMode(int mode)</span></span>                         |                                                           |
| <span data-ttu-id="31dce-169">public COMVariant value(str value, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-169">public COMVariant value(str value, \[COMVariant var\])</span></span> |                                                           |
| <span data-ttu-id="31dce-170">public str valueTxt(str value, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-170">public str valueTxt(str value, \[str var\])</span></span>            |                                                           |
| <span data-ttu-id="31dce-171">public void traceWrite(str category, str message)</span><span class="sxs-lookup"><span data-stu-id="31dce-171">public void traceWrite(str category, str message)</span></span>      |                                                           |
| <span data-ttu-id="31dce-172">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-172">public void finalize()</span></span>                                 |                                                           |
| <span data-ttu-id="31dce-173">public void traceWarn(str category, str message)</span><span class="sxs-lookup"><span data-stu-id="31dce-173">public void traceWarn(str category, str message)</span></span>       |                                                           |
| <span data-ttu-id="31dce-174">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-174">public void new()</span></span>                                      | <span data-ttu-id="31dce-175">IISContextObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-175">Initializes a new instance of the IISContextObject class.</span></span> |

### <a name="method-interface"></a><span data-ttu-id="31dce-176">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-176">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-177">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-177">Return Value</span></span>

### <a name="method-istraceenabled"></a><span data-ttu-id="31dce-178">メソッド isTraceEnabled</span><span class="sxs-lookup"><span data-stu-id="31dce-178">Method isTraceEnabled</span></span>

    public boolean isTraceEnabled()

#### <a name="return-value"></a><span data-ttu-id="31dce-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-179">Return Value</span></span>

### <a name="method-items"></a><span data-ttu-id="31dce-180">メソッド items</span><span class="sxs-lookup"><span data-stu-id="31dce-180">Method items</span></span>

    public IISVariantDictionary items()

#### <a name="return-value"></a><span data-ttu-id="31dce-181">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-181">Return Value</span></span>

### <a name="method-tracemode"></a><span data-ttu-id="31dce-182">メソッド traceMode</span><span class="sxs-lookup"><span data-stu-id="31dce-182">Method traceMode</span></span>

    public int traceMode(int mode)

#### <a name="parameters"></a><span data-ttu-id="31dce-183">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-183">Parameters</span></span>

<span data-ttu-id="31dce-184">モード</span><span class="sxs-lookup"><span data-stu-id="31dce-184">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-185">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-185">Return Value</span></span>

### <a name="method-value"></a><span data-ttu-id="31dce-186">メソッド value</span><span class="sxs-lookup"><span data-stu-id="31dce-186">Method value</span></span>

    public COMVariant value(str value, [COMVariant var])

#### <a name="parameters"></a><span data-ttu-id="31dce-187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-187">Parameters</span></span>

<span data-ttu-id="31dce-188">値</span><span class="sxs-lookup"><span data-stu-id="31dce-188">value</span></span>  

<!-- -->

<span data-ttu-id="31dce-189">var</span><span class="sxs-lookup"><span data-stu-id="31dce-189">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-190">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-190">Return Value</span></span>

### <a name="method-valuetxt"></a><span data-ttu-id="31dce-191">メソッド valueTxt</span><span class="sxs-lookup"><span data-stu-id="31dce-191">Method valueTxt</span></span>

    public str valueTxt(str value, [str var])

#### <a name="parameters"></a><span data-ttu-id="31dce-192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-192">Parameters</span></span>

<span data-ttu-id="31dce-193">値</span><span class="sxs-lookup"><span data-stu-id="31dce-193">value</span></span>  

<!-- -->

<span data-ttu-id="31dce-194">var</span><span class="sxs-lookup"><span data-stu-id="31dce-194">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-195">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-195">Return Value</span></span>

### <a name="method-tracewrite"></a><span data-ttu-id="31dce-196">メソッド traceWrite</span><span class="sxs-lookup"><span data-stu-id="31dce-196">Method traceWrite</span></span>

    public void traceWrite(str category, str message)

#### <a name="parameters"></a><span data-ttu-id="31dce-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-197">Parameters</span></span>

<span data-ttu-id="31dce-198">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="31dce-198">category</span></span>  

<!-- -->

<span data-ttu-id="31dce-199">メッセージ</span><span class="sxs-lookup"><span data-stu-id="31dce-199">message</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="31dce-200">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-200">Method finalize</span></span>

    public void finalize()

### <a name="method-tracewarn"></a><span data-ttu-id="31dce-201">メソッド traceWarn</span><span class="sxs-lookup"><span data-stu-id="31dce-201">Method traceWarn</span></span>

    public void traceWarn(str category, str message)

#### <a name="parameters"></a><span data-ttu-id="31dce-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-202">Parameters</span></span>

<span data-ttu-id="31dce-203">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="31dce-203">category</span></span>  

<!-- -->

<span data-ttu-id="31dce-204">メッセージ</span><span class="sxs-lookup"><span data-stu-id="31dce-204">message</span></span>  

### <a name="method-new"></a><span data-ttu-id="31dce-205">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-205">Method new</span></span>

<span data-ttu-id="31dce-206">IISContextObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-206">Initializes a new instance of the IISContextObject class.</span></span>

    public void new()

## <a name="class-iispostedfile"></a><span data-ttu-id="31dce-207">クラス IISPostedFile</span><span class="sxs-lookup"><span data-stu-id="31dce-207">Class IISPostedFile</span></span>
    class IISPostedFile extends Object

### <a name="remarks"></a><span data-ttu-id="31dce-208">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-208">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-209">例</span><span class="sxs-lookup"><span data-stu-id="31dce-209">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-210">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-210">Methods</span></span>

| <span data-ttu-id="31dce-211">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-211">Method</span></span>                                 | <span data-ttu-id="31dce-212">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-212">Description</span></span>                                            |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="31dce-213">public int contentLength()</span><span class="sxs-lookup"><span data-stu-id="31dce-213">public int contentLength()</span></span>             |                                                        |
| <span data-ttu-id="31dce-214">public str contentType()</span><span class="sxs-lookup"><span data-stu-id="31dce-214">public str contentType()</span></span>               |                                                        |
| <span data-ttu-id="31dce-215">public str fileName()</span><span class="sxs-lookup"><span data-stu-id="31dce-215">public str fileName()</span></span>                  |                                                        |
| <span data-ttu-id="31dce-216">public container read(int countToRead)</span><span class="sxs-lookup"><span data-stu-id="31dce-216">public container read(int countToRead)</span></span> |                                                        |
| <span data-ttu-id="31dce-217">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-217">public void finalize()</span></span>                 |                                                        |
| <span data-ttu-id="31dce-218">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-218">public void new()</span></span>                      | <span data-ttu-id="31dce-219">IISPostedFile クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-219">Initializes a new instance of the IISPostedFile class.</span></span> |

### <a name="method-contentlength"></a><span data-ttu-id="31dce-220">メソッド contentLength</span><span class="sxs-lookup"><span data-stu-id="31dce-220">Method contentLength</span></span>

    public int contentLength()

#### <a name="return-value"></a><span data-ttu-id="31dce-221">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-221">Return Value</span></span>

### <a name="method-contenttype"></a><span data-ttu-id="31dce-222">メソッド contentType</span><span class="sxs-lookup"><span data-stu-id="31dce-222">Method contentType</span></span>

    public str contentType()

#### <a name="return-value"></a><span data-ttu-id="31dce-223">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-223">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="31dce-224">メソッド fileName</span><span class="sxs-lookup"><span data-stu-id="31dce-224">Method fileName</span></span>

    public str fileName()

#### <a name="return-value"></a><span data-ttu-id="31dce-225">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-225">Return Value</span></span>

### <a name="method-read"></a><span data-ttu-id="31dce-226">メソッド read</span><span class="sxs-lookup"><span data-stu-id="31dce-226">Method read</span></span>

    public container read(int countToRead)

#### <a name="parameters"></a><span data-ttu-id="31dce-227">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-227">Parameters</span></span>

<span data-ttu-id="31dce-228">countToRead</span><span class="sxs-lookup"><span data-stu-id="31dce-228">countToRead</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-229">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-229">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-230">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-230">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="31dce-231">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-231">Method new</span></span>

<span data-ttu-id="31dce-232">IISPostedFile クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-232">Initializes a new instance of the IISPostedFile class.</span></span>

    public void new()

## <a name="class-iisreadcookie"></a><span data-ttu-id="31dce-233">クラス IISReadCookie</span><span class="sxs-lookup"><span data-stu-id="31dce-233">Class IISReadCookie</span></span>
    class IISReadCookie extends Object

<span data-ttu-id="31dce-234">IISReadCookie クラスは、インターネット インフォメーション サービス (IIS) によって提供される ReadCookie オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-234">The IISReadCookie class wraps the ReadCookie object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-235">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-235">Remarks</span></span>

<span data-ttu-id="31dce-236">IISReadCookie クラスのメソッドと、IIS によって提供される ReadCookie オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-236">There is a one-to-one connection between the methods of the IISReadCookie class and the methods of the ReadCookie object that is offered by IIS.</span></span> <span data-ttu-id="31dce-237">したがって、IISReadCookie クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-237">Therefore, for more information about the methods of the IISReadCookie class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-238">IISReadCookie クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-238">Use of the IISReadCookie class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-239">例</span><span class="sxs-lookup"><span data-stu-id="31dce-239">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-240">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-240">Methods</span></span>

| <span data-ttu-id="31dce-241">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-241">Method</span></span>                           | <span data-ttu-id="31dce-242">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-242">Description</span></span>                                     |
|----------------------------------|-------------------------------------------------|
| <span data-ttu-id="31dce-243">public int count()</span><span class="sxs-lookup"><span data-stu-id="31dce-243">public int count()</span></span>               |                                                 |
| <span data-ttu-id="31dce-244">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="31dce-244">public COMEnum2Variant getEnum()</span></span> |                                                 |
| <span data-ttu-id="31dce-245">public boolean hasKeys()</span><span class="sxs-lookup"><span data-stu-id="31dce-245">public boolean hasKeys()</span></span>         |                                                 |
| <span data-ttu-id="31dce-246">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-246">public ComInterface interface()</span></span>  |                                                 |
| <span data-ttu-id="31dce-247">public str item(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="31dce-247">public str item(\[str item\])</span></span>    |                                                 |
| <span data-ttu-id="31dce-248">public str key(str key)</span><span class="sxs-lookup"><span data-stu-id="31dce-248">public str key(str key)</span></span>          |                                                 |
| <span data-ttu-id="31dce-249">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-249">public void finalize()</span></span>           |                                                 |
| <span data-ttu-id="31dce-250">public void new(COM readCookie)</span><span class="sxs-lookup"><span data-stu-id="31dce-250">public void new(COM readCookie)</span></span>  | <span data-ttu-id="31dce-251">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-251">Initializes a new instance of the Object class.</span></span> |

### <a name="method-count"></a><span data-ttu-id="31dce-252">メソッド count</span><span class="sxs-lookup"><span data-stu-id="31dce-252">Method count</span></span>

    public int count()

#### <a name="return-value"></a><span data-ttu-id="31dce-253">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-253">Return Value</span></span>

### <a name="method-getenum"></a><span data-ttu-id="31dce-254">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="31dce-254">Method getEnum</span></span>

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a><span data-ttu-id="31dce-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-255">Return Value</span></span>

### <a name="method-haskeys"></a><span data-ttu-id="31dce-256">メソッド hasKeys</span><span class="sxs-lookup"><span data-stu-id="31dce-256">Method hasKeys</span></span>

    public boolean hasKeys()

#### <a name="return-value"></a><span data-ttu-id="31dce-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-257">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-258">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-258">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-259">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-259">Return Value</span></span>

### <a name="method-item"></a><span data-ttu-id="31dce-260">メソッド item</span><span class="sxs-lookup"><span data-stu-id="31dce-260">Method item</span></span>

    public str item([str item])

#### <a name="parameters"></a><span data-ttu-id="31dce-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-261">Parameters</span></span>

<span data-ttu-id="31dce-262">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-262">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-263">Return Value</span></span>

### <a name="method-key"></a><span data-ttu-id="31dce-264">メソッド key</span><span class="sxs-lookup"><span data-stu-id="31dce-264">Method key</span></span>

    public str key(str key)

#### <a name="parameters"></a><span data-ttu-id="31dce-265">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-265">Parameters</span></span>

<span data-ttu-id="31dce-266">キー</span><span class="sxs-lookup"><span data-stu-id="31dce-266">key</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-267">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-267">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-268">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-268">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="31dce-269">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-269">Method new</span></span>

<span data-ttu-id="31dce-270">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-270">Initializes a new instance of the Object class.</span></span>

    public void new(COM readCookie)

#### <a name="parameters"></a><span data-ttu-id="31dce-271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-271">Parameters</span></span>

<span data-ttu-id="31dce-272">readCookie</span><span class="sxs-lookup"><span data-stu-id="31dce-272">readCookie</span></span>  

## <a name="class-iisrequest"></a><span data-ttu-id="31dce-273">クラス IISRequest</span><span class="sxs-lookup"><span data-stu-id="31dce-273">Class IISRequest</span></span>
    class IISRequest extends Object

<span data-ttu-id="31dce-274">IISRequest クラスは、インターネット インフォメーション サービス (IIS) によって提供される Request オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-274">The IISRequest class wraps the Request object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-275">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-275">Remarks</span></span>

<span data-ttu-id="31dce-276">IISRequest クラスのメソッドと、IIS によって提供される Request オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-276">There is a one-to-one connection between the methods of the IISRequest class and the methods of the Request object that is offered by IIS.</span></span> <span data-ttu-id="31dce-277">したがって、IISRequest クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-277">Therefore, for more information about the methods of the IISRequest class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-278">IISRequest クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-278">Use of the IISRequest class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-279">例</span><span class="sxs-lookup"><span data-stu-id="31dce-279">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-280">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-280">Methods</span></span>

| <span data-ttu-id="31dce-281">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-281">Method</span></span>                                               | <span data-ttu-id="31dce-282">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-282">Description</span></span>                                         |
|------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="31dce-283">public COMVariant binaryRead(COMVariant countToRead)</span><span class="sxs-lookup"><span data-stu-id="31dce-283">public COMVariant binaryRead(COMVariant countToRead)</span></span> |                                                     |
| <span data-ttu-id="31dce-284">public IISRequestDictionary clientCertificate()</span><span class="sxs-lookup"><span data-stu-id="31dce-284">public IISRequestDictionary clientCertificate()</span></span>      |                                                     |
| <span data-ttu-id="31dce-285">public IISRequestDictionary cookies()</span><span class="sxs-lookup"><span data-stu-id="31dce-285">public IISRequestDictionary cookies()</span></span>                |                                                     |
| <span data-ttu-id="31dce-286">public IISPostedFile file(COMVariant index)</span><span class="sxs-lookup"><span data-stu-id="31dce-286">public IISPostedFile file(COMVariant index)</span></span>          |                                                     |
| <span data-ttu-id="31dce-287">public int fileCount()</span><span class="sxs-lookup"><span data-stu-id="31dce-287">public int fileCount()</span></span>                               |                                                     |
| <span data-ttu-id="31dce-288">public IISRequestDictionary form()</span><span class="sxs-lookup"><span data-stu-id="31dce-288">public IISRequestDictionary form()</span></span>                   |                                                     |
| <span data-ttu-id="31dce-289">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-289">public ComInterface interface()</span></span>                      |                                                     |
| <span data-ttu-id="31dce-290">public str item(str item)</span><span class="sxs-lookup"><span data-stu-id="31dce-290">public str item(str item)</span></span>                            |                                                     |
| <span data-ttu-id="31dce-291">public IISRequestDictionary queryString()</span><span class="sxs-lookup"><span data-stu-id="31dce-291">public IISRequestDictionary queryString()</span></span>            |                                                     |
| <span data-ttu-id="31dce-292">public IISRequestDictionary serverVariables()</span><span class="sxs-lookup"><span data-stu-id="31dce-292">public IISRequestDictionary serverVariables()</span></span>        |                                                     |
| <span data-ttu-id="31dce-293">public int totalBytes()</span><span class="sxs-lookup"><span data-stu-id="31dce-293">public int totalBytes()</span></span>                              |                                                     |
| <span data-ttu-id="31dce-294">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-294">public void finalize()</span></span>                               |                                                     |
| <span data-ttu-id="31dce-295">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-295">public void new()</span></span>                                    | <span data-ttu-id="31dce-296">IISRequest クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-296">Initializes a new instance of the IISRequest class.</span></span> |

### <a name="method-binaryread"></a><span data-ttu-id="31dce-297">メソッド binaryRead</span><span class="sxs-lookup"><span data-stu-id="31dce-297">Method binaryRead</span></span>

    public COMVariant binaryRead(COMVariant countToRead)

#### <a name="parameters"></a><span data-ttu-id="31dce-298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-298">Parameters</span></span>

<span data-ttu-id="31dce-299">countToRead</span><span class="sxs-lookup"><span data-stu-id="31dce-299">countToRead</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-300">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-300">Return Value</span></span>

### <a name="method-clientcertificate"></a><span data-ttu-id="31dce-301">メソッド clientCertificate</span><span class="sxs-lookup"><span data-stu-id="31dce-301">Method clientCertificate</span></span>

    public IISRequestDictionary clientCertificate()

#### <a name="return-value"></a><span data-ttu-id="31dce-302">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-302">Return Value</span></span>

### <a name="method-cookies"></a><span data-ttu-id="31dce-303">メソッド cookies</span><span class="sxs-lookup"><span data-stu-id="31dce-303">Method cookies</span></span>

    public IISRequestDictionary cookies()

#### <a name="return-value"></a><span data-ttu-id="31dce-304">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-304">Return Value</span></span>

### <a name="method-file"></a><span data-ttu-id="31dce-305">メソッド file</span><span class="sxs-lookup"><span data-stu-id="31dce-305">Method file</span></span>

    public IISPostedFile file(COMVariant index)

#### <a name="parameters"></a><span data-ttu-id="31dce-306">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-306">Parameters</span></span>

<span data-ttu-id="31dce-307">指数</span><span class="sxs-lookup"><span data-stu-id="31dce-307">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-308">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-308">Return Value</span></span>

### <a name="method-filecount"></a><span data-ttu-id="31dce-309">メソッド fileCount</span><span class="sxs-lookup"><span data-stu-id="31dce-309">Method fileCount</span></span>

    public int fileCount()

#### <a name="return-value"></a><span data-ttu-id="31dce-310">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-310">Return Value</span></span>

### <a name="method-form"></a><span data-ttu-id="31dce-311">メソッド form</span><span class="sxs-lookup"><span data-stu-id="31dce-311">Method form</span></span>

    public IISRequestDictionary form()

#### <a name="return-value"></a><span data-ttu-id="31dce-312">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-312">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-313">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-313">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-314">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-314">Return Value</span></span>

### <a name="method-item"></a><span data-ttu-id="31dce-315">メソッド item</span><span class="sxs-lookup"><span data-stu-id="31dce-315">Method item</span></span>

    public str item(str item)

#### <a name="parameters"></a><span data-ttu-id="31dce-316">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-316">Parameters</span></span>

<span data-ttu-id="31dce-317">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-317">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-318">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-318">Return Value</span></span>

### <a name="method-querystring"></a><span data-ttu-id="31dce-319">メソッド queryString</span><span class="sxs-lookup"><span data-stu-id="31dce-319">Method queryString</span></span>

    public IISRequestDictionary queryString()

#### <a name="return-value"></a><span data-ttu-id="31dce-320">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-320">Return Value</span></span>

### <a name="method-servervariables"></a><span data-ttu-id="31dce-321">メソッド serverVariables</span><span class="sxs-lookup"><span data-stu-id="31dce-321">Method serverVariables</span></span>

    public IISRequestDictionary serverVariables()

#### <a name="return-value"></a><span data-ttu-id="31dce-322">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-322">Return Value</span></span>

### <a name="method-totalbytes"></a><span data-ttu-id="31dce-323">メソッド totalBytes</span><span class="sxs-lookup"><span data-stu-id="31dce-323">Method totalBytes</span></span>

    public int totalBytes()

#### <a name="return-value"></a><span data-ttu-id="31dce-324">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-324">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-325">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-325">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="31dce-326">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-326">Method new</span></span>

<span data-ttu-id="31dce-327">IISRequest クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-327">Initializes a new instance of the IISRequest class.</span></span>

    public void new()

## <a name="class-iisrequestdictionary"></a><span data-ttu-id="31dce-328">クラス IISRequestDictionary</span><span class="sxs-lookup"><span data-stu-id="31dce-328">Class IISRequestDictionary</span></span>
    class IISRequestDictionary extends Object

<span data-ttu-id="31dce-329">IISRequestDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される RequestDictionary オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-329">The IISRequestDictionary class wraps the RequestDictionary object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-330">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-330">Remarks</span></span>

<span data-ttu-id="31dce-331">IISRequestDictionary クラスのメソッドと、IIS によって提供される RequestDictionary オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。</span><span class="sxs-lookup"><span data-stu-id="31dce-331">There is a one-to-one relationship between the methods of the IISRequestDictionary class and the methods of the RequestDictionary object that is offered by IIS.</span></span> <span data-ttu-id="31dce-332">したがって、IISRequestDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-332">Therefore, for more information about the methods of the IISRequestDictionary class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-333">IISRequestDictionary クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-333">Use of the IISRequestDictionary class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-334">例</span><span class="sxs-lookup"><span data-stu-id="31dce-334">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-335">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-335">Methods</span></span>

| <span data-ttu-id="31dce-336">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-336">Method</span></span>                                              | <span data-ttu-id="31dce-337">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-337">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="31dce-338">public int count()</span><span class="sxs-lookup"><span data-stu-id="31dce-338">public int count()</span></span>                                  |                                                 |
| <span data-ttu-id="31dce-339">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="31dce-339">public COMEnum2Variant getEnum()</span></span>                    |                                                 |
| <span data-ttu-id="31dce-340">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-340">public ComInterface interface()</span></span>                     |                                                 |
| <span data-ttu-id="31dce-341">public COMVariant item(COMVariant item)</span><span class="sxs-lookup"><span data-stu-id="31dce-341">public COMVariant item(COMVariant item)</span></span>             |                                                 |
| <span data-ttu-id="31dce-342">public IISReadCookie itemReadCookie(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="31dce-342">public IISReadCookie itemReadCookie(\[str item\])</span></span>   |                                                 |
| <span data-ttu-id="31dce-343">public IISStringList itemStringList(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="31dce-343">public IISStringList itemStringList(\[str item\])</span></span>   |                                                 |
| <span data-ttu-id="31dce-344">public str itemTxt(str item)</span><span class="sxs-lookup"><span data-stu-id="31dce-344">public str itemTxt(str item)</span></span>                        |                                                 |
| <span data-ttu-id="31dce-345">public IISWriteCookie itemWriteCookie(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="31dce-345">public IISWriteCookie itemWriteCookie(\[str item\])</span></span> |                                                 |
| <span data-ttu-id="31dce-346">public str key(str key)</span><span class="sxs-lookup"><span data-stu-id="31dce-346">public str key(str key)</span></span>                             |                                                 |
| <span data-ttu-id="31dce-347">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-347">public void finalize()</span></span>                              |                                                 |
| <span data-ttu-id="31dce-348">public void new(COM requestDictionary)</span><span class="sxs-lookup"><span data-stu-id="31dce-348">public void new(COM requestDictionary)</span></span>              | <span data-ttu-id="31dce-349">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-349">Initializes a new instance of the Object class.</span></span> |

### <a name="method-count"></a><span data-ttu-id="31dce-350">メソッド count</span><span class="sxs-lookup"><span data-stu-id="31dce-350">Method count</span></span>

    public int count()

#### <a name="return-value"></a><span data-ttu-id="31dce-351">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-351">Return Value</span></span>

### <a name="method-getenum"></a><span data-ttu-id="31dce-352">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="31dce-352">Method getEnum</span></span>

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a><span data-ttu-id="31dce-353">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-353">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-354">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-354">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-355">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-355">Return Value</span></span>

### <a name="method-item"></a><span data-ttu-id="31dce-356">メソッド item</span><span class="sxs-lookup"><span data-stu-id="31dce-356">Method item</span></span>

    public COMVariant item(COMVariant item)

#### <a name="parameters"></a><span data-ttu-id="31dce-357">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-357">Parameters</span></span>

<span data-ttu-id="31dce-358">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-358">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-359">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-359">Return Value</span></span>

### <a name="method-itemreadcookie"></a><span data-ttu-id="31dce-360">メソッド itemReadCookie</span><span class="sxs-lookup"><span data-stu-id="31dce-360">Method itemReadCookie</span></span>

    public IISReadCookie itemReadCookie([str item])

#### <a name="parameters"></a><span data-ttu-id="31dce-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-361">Parameters</span></span>

<span data-ttu-id="31dce-362">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-362">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-363">Return Value</span></span>

### <a name="method-itemstringlist"></a><span data-ttu-id="31dce-364">メソッド itemStringList</span><span class="sxs-lookup"><span data-stu-id="31dce-364">Method itemStringList</span></span>

    public IISStringList itemStringList([str item])

#### <a name="parameters"></a><span data-ttu-id="31dce-365">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-365">Parameters</span></span>

<span data-ttu-id="31dce-366">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-366">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-367">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-367">Return Value</span></span>

### <a name="method-itemtxt"></a><span data-ttu-id="31dce-368">メソッド itemTxt</span><span class="sxs-lookup"><span data-stu-id="31dce-368">Method itemTxt</span></span>

    public str itemTxt(str item)

#### <a name="parameters"></a><span data-ttu-id="31dce-369">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-369">Parameters</span></span>

<span data-ttu-id="31dce-370">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-370">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-371">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-371">Return Value</span></span>

### <a name="method-itemwritecookie"></a><span data-ttu-id="31dce-372">メソッド itemWriteCookie</span><span class="sxs-lookup"><span data-stu-id="31dce-372">Method itemWriteCookie</span></span>

    public IISWriteCookie itemWriteCookie([str item])

#### <a name="parameters"></a><span data-ttu-id="31dce-373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-373">Parameters</span></span>

<span data-ttu-id="31dce-374">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-374">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-375">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-375">Return Value</span></span>

### <a name="method-key"></a><span data-ttu-id="31dce-376">メソッド key</span><span class="sxs-lookup"><span data-stu-id="31dce-376">Method key</span></span>

    public str key(str key)

#### <a name="parameters"></a><span data-ttu-id="31dce-377">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-377">Parameters</span></span>

<span data-ttu-id="31dce-378">キー</span><span class="sxs-lookup"><span data-stu-id="31dce-378">key</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-379">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-379">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-380">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-380">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="31dce-381">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-381">Method new</span></span>

<span data-ttu-id="31dce-382">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-382">Initializes a new instance of the Object class.</span></span>

    public void new(COM requestDictionary)

#### <a name="parameters"></a><span data-ttu-id="31dce-383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-383">Parameters</span></span>

<span data-ttu-id="31dce-384">requestDictionary</span><span class="sxs-lookup"><span data-stu-id="31dce-384">requestDictionary</span></span>  

## <a name="class-iisresponse"></a><span data-ttu-id="31dce-385">クラス IISResponse</span><span class="sxs-lookup"><span data-stu-id="31dce-385">Class IISResponse</span></span>
    class IISResponse extends Object

<span data-ttu-id="31dce-386">IISResponse クラスは、インターネット インフォメーション サービス (IIS) によって提供される Response オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-386">The IISResponse class wraps the Response object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-387">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-387">Remarks</span></span>

<span data-ttu-id="31dce-388">IISResponse クラスのメソッドと、IIS によって提供される Response オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。</span><span class="sxs-lookup"><span data-stu-id="31dce-388">There is a one-to-one relationship between the methods of the IISResponse class and the methods of the Response object that is offered by IIS.</span></span> <span data-ttu-id="31dce-389">したがって、IISResponse クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-389">Therefore, for more information about the methods of the IISResponse class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-390">IISResponse クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-390">Use of the IISResponse class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-391">例</span><span class="sxs-lookup"><span data-stu-id="31dce-391">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-392">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-392">Methods</span></span>

| <span data-ttu-id="31dce-393">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-393">Method</span></span>                                                    | <span data-ttu-id="31dce-394">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-394">Description</span></span>                                          |
|-----------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31dce-395">public boolean buffer(\[boolean isBuffering\])</span><span class="sxs-lookup"><span data-stu-id="31dce-395">public boolean buffer(\[boolean isBuffering\])</span></span>            |                                                      |
| <span data-ttu-id="31dce-396">public str cacheControl(\[str cacheControl\])</span><span class="sxs-lookup"><span data-stu-id="31dce-396">public str cacheControl(\[str cacheControl\])</span></span>             |                                                      |
| <span data-ttu-id="31dce-397">public boolean cacheWrite(\[boolean cache\])</span><span class="sxs-lookup"><span data-stu-id="31dce-397">public boolean cacheWrite(\[boolean cache\])</span></span>              |                                                      |
| <span data-ttu-id="31dce-398">public str charSet(\[str charSet\])</span><span class="sxs-lookup"><span data-stu-id="31dce-398">public str charSet(\[str charSet\])</span></span>                       |                                                      |
| <span data-ttu-id="31dce-399">public str contentType(\[str contentType\])</span><span class="sxs-lookup"><span data-stu-id="31dce-399">public str contentType(\[str contentType\])</span></span>               |                                                      |
| <span data-ttu-id="31dce-400">public IISRequestDictionary cookies()</span><span class="sxs-lookup"><span data-stu-id="31dce-400">public IISRequestDictionary cookies()</span></span>                     |                                                      |
| <span data-ttu-id="31dce-401">public int expires(\[int expiresMinutes\])</span><span class="sxs-lookup"><span data-stu-id="31dce-401">public int expires(\[int expiresMinutes\])</span></span>                |                                                      |
| <span data-ttu-id="31dce-402">public COMVariant expiresAbsolute(\[COMVariant expires\])</span><span class="sxs-lookup"><span data-stu-id="31dce-402">public COMVariant expiresAbsolute(\[COMVariant expires\])</span></span> |                                                      |
| <span data-ttu-id="31dce-403">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-403">public ComInterface interface()</span></span>                           |                                                      |
| <span data-ttu-id="31dce-404">public boolean isClientConnected()</span><span class="sxs-lookup"><span data-stu-id="31dce-404">public boolean isClientConnected()</span></span>                        |                                                      |
| <span data-ttu-id="31dce-405">public str status(\[str status\])</span><span class="sxs-lookup"><span data-stu-id="31dce-405">public str status(\[str status\])</span></span>                         | <span data-ttu-id="31dce-406">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-406">Gets or sets the status of an object.</span></span>                |
| <span data-ttu-id="31dce-407">public void addHeader(str headerName, str headerValue)</span><span class="sxs-lookup"><span data-stu-id="31dce-407">public void addHeader(str headerName, str headerValue)</span></span>    |                                                      |
| <span data-ttu-id="31dce-408">public void writeTxt(str text)</span><span class="sxs-lookup"><span data-stu-id="31dce-408">public void writeTxt(str text)</span></span>                            |                                                      |
| <span data-ttu-id="31dce-409">public void write(COMVariant text)</span><span class="sxs-lookup"><span data-stu-id="31dce-409">public void write(COMVariant text)</span></span>                        |                                                      |
| <span data-ttu-id="31dce-410">public void clear()</span><span class="sxs-lookup"><span data-stu-id="31dce-410">public void clear()</span></span>                                       |                                                      |
| <span data-ttu-id="31dce-411">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-411">public void finalize()</span></span>                                    |                                                      |
| <span data-ttu-id="31dce-412">public void binaryWrite(COMVariant input)</span><span class="sxs-lookup"><span data-stu-id="31dce-412">public void binaryWrite(COMVariant input)</span></span>                 |                                                      |
| <span data-ttu-id="31dce-413">public void appendToLog(str logEntry)</span><span class="sxs-lookup"><span data-stu-id="31dce-413">public void appendToLog(str logEntry)</span></span>                     |                                                      |
| <span data-ttu-id="31dce-414">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-414">public void new()</span></span>                                         | <span data-ttu-id="31dce-415">IISResponse クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-415">Initializes a new instance of the IISResponse class.</span></span> |
| <span data-ttu-id="31dce-416">public void redirect(str url)</span><span class="sxs-lookup"><span data-stu-id="31dce-416">public void redirect(str url)</span></span>                             |                                                      |
| <span data-ttu-id="31dce-417">public void flush()</span><span class="sxs-lookup"><span data-stu-id="31dce-417">public void flush()</span></span>                                       |                                                      |
| <span data-ttu-id="31dce-418">public void pics(str headerValue)</span><span class="sxs-lookup"><span data-stu-id="31dce-418">public void pics(str headerValue)</span></span>                         |                                                      |
| <span data-ttu-id="31dce-419">public void end()</span><span class="sxs-lookup"><span data-stu-id="31dce-419">public void end()</span></span>                                         |                                                      |

### <a name="method-buffer"></a><span data-ttu-id="31dce-420">メソッド buffer</span><span class="sxs-lookup"><span data-stu-id="31dce-420">Method buffer</span></span>

    public boolean buffer([boolean isBuffering])

#### <a name="parameters"></a><span data-ttu-id="31dce-421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-421">Parameters</span></span>

<span data-ttu-id="31dce-422">isBuffering</span><span class="sxs-lookup"><span data-stu-id="31dce-422">isBuffering</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-423">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-423">Return Value</span></span>

### <a name="method-cachecontrol"></a><span data-ttu-id="31dce-424">メソッド cacheControl</span><span class="sxs-lookup"><span data-stu-id="31dce-424">Method cacheControl</span></span>

    public str cacheControl([str cacheControl])

#### <a name="parameters"></a><span data-ttu-id="31dce-425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-425">Parameters</span></span>

<span data-ttu-id="31dce-426">cacheControl</span><span class="sxs-lookup"><span data-stu-id="31dce-426">cacheControl</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-427">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-427">Return Value</span></span>

### <a name="method-cachewrite"></a><span data-ttu-id="31dce-428">メソッド cacheWrite</span><span class="sxs-lookup"><span data-stu-id="31dce-428">Method cacheWrite</span></span>

    public boolean cacheWrite([boolean cache])

#### <a name="parameters"></a><span data-ttu-id="31dce-429">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-429">Parameters</span></span>

<span data-ttu-id="31dce-430">cache</span><span class="sxs-lookup"><span data-stu-id="31dce-430">cache</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-431">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-431">Return Value</span></span>

### <a name="method-charset"></a><span data-ttu-id="31dce-432">メソッド charSet</span><span class="sxs-lookup"><span data-stu-id="31dce-432">Method charSet</span></span>

    public str charSet([str charSet])

#### <a name="parameters"></a><span data-ttu-id="31dce-433">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-433">Parameters</span></span>

<span data-ttu-id="31dce-434">charSet</span><span class="sxs-lookup"><span data-stu-id="31dce-434">charSet</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-435">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-435">Return Value</span></span>

### <a name="method-contenttype"></a><span data-ttu-id="31dce-436">メソッド contentType</span><span class="sxs-lookup"><span data-stu-id="31dce-436">Method contentType</span></span>

    public str contentType([str contentType])

#### <a name="parameters"></a><span data-ttu-id="31dce-437">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-437">Parameters</span></span>

<span data-ttu-id="31dce-438">contentType</span><span class="sxs-lookup"><span data-stu-id="31dce-438">contentType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-439">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-439">Return Value</span></span>

### <a name="method-cookies"></a><span data-ttu-id="31dce-440">メソッド cookies</span><span class="sxs-lookup"><span data-stu-id="31dce-440">Method cookies</span></span>

    public IISRequestDictionary cookies()

#### <a name="return-value"></a><span data-ttu-id="31dce-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-441">Return Value</span></span>

### <a name="method-expires"></a><span data-ttu-id="31dce-442">メソッド expires</span><span class="sxs-lookup"><span data-stu-id="31dce-442">Method expires</span></span>

    public int expires([int expiresMinutes])

#### <a name="parameters"></a><span data-ttu-id="31dce-443">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-443">Parameters</span></span>

<span data-ttu-id="31dce-444">expiresMinutes</span><span class="sxs-lookup"><span data-stu-id="31dce-444">expiresMinutes</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-445">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-445">Return Value</span></span>

### <a name="method-expiresabsolute"></a><span data-ttu-id="31dce-446">メソッド expiresAbsolute</span><span class="sxs-lookup"><span data-stu-id="31dce-446">Method expiresAbsolute</span></span>

    public COMVariant expiresAbsolute([COMVariant expires])

#### <a name="parameters"></a><span data-ttu-id="31dce-447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-447">Parameters</span></span>

<span data-ttu-id="31dce-448">expires</span><span class="sxs-lookup"><span data-stu-id="31dce-448">expires</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-449">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-449">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-450">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-450">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-451">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-451">Return Value</span></span>

### <a name="method-isclientconnected"></a><span data-ttu-id="31dce-452">メソッド isClientConnected</span><span class="sxs-lookup"><span data-stu-id="31dce-452">Method isClientConnected</span></span>

    public boolean isClientConnected()

#### <a name="return-value"></a><span data-ttu-id="31dce-453">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-453">Return Value</span></span>

### <a name="method-status"></a><span data-ttu-id="31dce-454">メソッド status</span><span class="sxs-lookup"><span data-stu-id="31dce-454">Method status</span></span>

<span data-ttu-id="31dce-455">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-455">Gets or sets the status of an object.</span></span>

    public str status([str status])

#### <a name="parameters"></a><span data-ttu-id="31dce-456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-456">Parameters</span></span>

<span data-ttu-id="31dce-457">ステータス</span><span class="sxs-lookup"><span data-stu-id="31dce-457">status</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-458">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-458">Return Value</span></span>

<span data-ttu-id="31dce-459">オブジェクトのステータスの現在の値。</span><span class="sxs-lookup"><span data-stu-id="31dce-459">The current value of the status of the object.</span></span>

### <a name="method-addheader"></a><span data-ttu-id="31dce-460">メソッド addHeader</span><span class="sxs-lookup"><span data-stu-id="31dce-460">Method addHeader</span></span>

    public void addHeader(str headerName, str headerValue)

#### <a name="parameters"></a><span data-ttu-id="31dce-461">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-461">Parameters</span></span>

<span data-ttu-id="31dce-462">headerName</span><span class="sxs-lookup"><span data-stu-id="31dce-462">headerName</span></span>  

<!-- -->

<span data-ttu-id="31dce-463">headerValue</span><span class="sxs-lookup"><span data-stu-id="31dce-463">headerValue</span></span>  

### <a name="method-writetxt"></a><span data-ttu-id="31dce-464">メソッド writeTxt</span><span class="sxs-lookup"><span data-stu-id="31dce-464">Method writeTxt</span></span>

    public void writeTxt(str text)

#### <a name="parameters"></a><span data-ttu-id="31dce-465">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-465">Parameters</span></span>

<span data-ttu-id="31dce-466">テキスト</span><span class="sxs-lookup"><span data-stu-id="31dce-466">text</span></span>  

### <a name="method-write"></a><span data-ttu-id="31dce-467">メソッド write</span><span class="sxs-lookup"><span data-stu-id="31dce-467">Method write</span></span>

    public void write(COMVariant text)

#### <a name="parameters"></a><span data-ttu-id="31dce-468">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-468">Parameters</span></span>

<span data-ttu-id="31dce-469">テキスト</span><span class="sxs-lookup"><span data-stu-id="31dce-469">text</span></span>  

### <a name="method-clear"></a><span data-ttu-id="31dce-470">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="31dce-470">Method clear</span></span>

    public void clear()

### <a name="method-finalize"></a><span data-ttu-id="31dce-471">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-471">Method finalize</span></span>

    public void finalize()

### <a name="method-binarywrite"></a><span data-ttu-id="31dce-472">メソッド binaryWrite</span><span class="sxs-lookup"><span data-stu-id="31dce-472">Method binaryWrite</span></span>

    public void binaryWrite(COMVariant input)

#### <a name="parameters"></a><span data-ttu-id="31dce-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-473">Parameters</span></span>

<span data-ttu-id="31dce-474">input</span><span class="sxs-lookup"><span data-stu-id="31dce-474">input</span></span>  

### <a name="method-appendtolog"></a><span data-ttu-id="31dce-475">メソッド appendToLog</span><span class="sxs-lookup"><span data-stu-id="31dce-475">Method appendToLog</span></span>

    public void appendToLog(str logEntry)

#### <a name="parameters"></a><span data-ttu-id="31dce-476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-476">Parameters</span></span>

<span data-ttu-id="31dce-477">logEntry</span><span class="sxs-lookup"><span data-stu-id="31dce-477">logEntry</span></span>  

### <a name="method-new"></a><span data-ttu-id="31dce-478">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-478">Method new</span></span>

<span data-ttu-id="31dce-479">IISResponse クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-479">Initializes a new instance of the IISResponse class.</span></span>

    public void new()

### <a name="method-redirect"></a><span data-ttu-id="31dce-480">メソッド redirect</span><span class="sxs-lookup"><span data-stu-id="31dce-480">Method redirect</span></span>

    public void redirect(str url)

#### <a name="parameters"></a><span data-ttu-id="31dce-481">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-481">Parameters</span></span>

<span data-ttu-id="31dce-482">URL</span><span class="sxs-lookup"><span data-stu-id="31dce-482">url</span></span>  

### <a name="method-flush"></a><span data-ttu-id="31dce-483">メソッド flush</span><span class="sxs-lookup"><span data-stu-id="31dce-483">Method flush</span></span>

    public void flush()

### <a name="method-pics"></a><span data-ttu-id="31dce-484">メソッド pics</span><span class="sxs-lookup"><span data-stu-id="31dce-484">Method pics</span></span>

    public void pics(str headerValue)

#### <a name="parameters"></a><span data-ttu-id="31dce-485">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-485">Parameters</span></span>

<span data-ttu-id="31dce-486">headerValue</span><span class="sxs-lookup"><span data-stu-id="31dce-486">headerValue</span></span>  

### <a name="method-end"></a><span data-ttu-id="31dce-487">メソッド end</span><span class="sxs-lookup"><span data-stu-id="31dce-487">Method end</span></span>

    public void end()

## <a name="class-iisserver"></a><span data-ttu-id="31dce-488">クラス IISServer</span><span class="sxs-lookup"><span data-stu-id="31dce-488">Class IISServer</span></span>
    class IISServer extends Object

<span data-ttu-id="31dce-489">IISServer クラスは、インターネット インフォメーション サービス (IIS) によって提供される Server オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-489">The IISServer class wraps the Server object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-490">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-490">Remarks</span></span>

<span data-ttu-id="31dce-491">IISServer クラスのメソッドと、IIS によって提供される Server オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-491">There is a one-to-one connection between the methods of the IISServer class and the methods of the Server object that is offered by IIS.</span></span> <span data-ttu-id="31dce-492">したがって、IISServer クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-492">Therefore, for more information about the methods of the IISServer class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-493">IISServer クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-493">Use of the IISServer class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-494">例</span><span class="sxs-lookup"><span data-stu-id="31dce-494">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-495">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-495">Methods</span></span>

| <span data-ttu-id="31dce-496">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-496">Method</span></span>                                           | <span data-ttu-id="31dce-497">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-497">Description</span></span>                                        |
|--------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="31dce-498">public COM createObject(str progID)</span><span class="sxs-lookup"><span data-stu-id="31dce-498">public COM createObject(str progID)</span></span>              |                                                    |
| <span data-ttu-id="31dce-499">public str htmlEncode(str txt)</span><span class="sxs-lookup"><span data-stu-id="31dce-499">public str htmlEncode(str txt)</span></span>                   |                                                    |
| <span data-ttu-id="31dce-500">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-500">public ComInterface interface()</span></span>                  |                                                    |
| <span data-ttu-id="31dce-501">public str mapPath(str logicalPath)</span><span class="sxs-lookup"><span data-stu-id="31dce-501">public str mapPath(str logicalPath)</span></span>              |                                                    |
| <span data-ttu-id="31dce-502">public int scriptTimeout(\[int timeoutSeconds\])</span><span class="sxs-lookup"><span data-stu-id="31dce-502">public int scriptTimeout(\[int timeoutSeconds\])</span></span> |                                                    |
| <span data-ttu-id="31dce-503">public str urlEncode(str txt)</span><span class="sxs-lookup"><span data-stu-id="31dce-503">public str urlEncode(str txt)</span></span>                    |                                                    |
| <span data-ttu-id="31dce-504">public str urlPathEncode(str txt)</span><span class="sxs-lookup"><span data-stu-id="31dce-504">public str urlPathEncode(str txt)</span></span>                |                                                    |
| <span data-ttu-id="31dce-505">public void execute(str logicalPath)</span><span class="sxs-lookup"><span data-stu-id="31dce-505">public void execute(str logicalPath)</span></span>             |                                                    |
| <span data-ttu-id="31dce-506">public void transfer(str logicalPath)</span><span class="sxs-lookup"><span data-stu-id="31dce-506">public void transfer(str logicalPath)</span></span>            |                                                    |
| <span data-ttu-id="31dce-507">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-507">public void new()</span></span>                                | <span data-ttu-id="31dce-508">IISServer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-508">Initializes a new instance of the IISServer class.</span></span> |
| <span data-ttu-id="31dce-509">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-509">public void finalize()</span></span>                           |                                                    |

### <a name="method-createobject"></a><span data-ttu-id="31dce-510">メソッド createObject</span><span class="sxs-lookup"><span data-stu-id="31dce-510">Method createObject</span></span>

    public COM createObject(str progID)

#### <a name="parameters"></a><span data-ttu-id="31dce-511">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-511">Parameters</span></span>

<span data-ttu-id="31dce-512">progID</span><span class="sxs-lookup"><span data-stu-id="31dce-512">progID</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-513">Return Value</span></span>

### <a name="method-htmlencode"></a><span data-ttu-id="31dce-514">メソッド htmlEncode</span><span class="sxs-lookup"><span data-stu-id="31dce-514">Method htmlEncode</span></span>

    public str htmlEncode(str txt)

#### <a name="parameters"></a><span data-ttu-id="31dce-515">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-515">Parameters</span></span>

<span data-ttu-id="31dce-516">txt</span><span class="sxs-lookup"><span data-stu-id="31dce-516">txt</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-517">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-518">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-518">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-519">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-519">Return Value</span></span>

### <a name="method-mappath"></a><span data-ttu-id="31dce-520">メソッド mapPath</span><span class="sxs-lookup"><span data-stu-id="31dce-520">Method mapPath</span></span>

    public str mapPath(str logicalPath)

#### <a name="parameters"></a><span data-ttu-id="31dce-521">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-521">Parameters</span></span>

<span data-ttu-id="31dce-522">logicalPath</span><span class="sxs-lookup"><span data-stu-id="31dce-522">logicalPath</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-523">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-523">Return Value</span></span>

### <a name="method-scripttimeout"></a><span data-ttu-id="31dce-524">メソッド scriptTimeout</span><span class="sxs-lookup"><span data-stu-id="31dce-524">Method scriptTimeout</span></span>

    public int scriptTimeout([int timeoutSeconds])

#### <a name="parameters"></a><span data-ttu-id="31dce-525">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-525">Parameters</span></span>

<span data-ttu-id="31dce-526">timeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="31dce-526">timeoutSeconds</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-527">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-527">Return Value</span></span>

### <a name="method-urlencode"></a><span data-ttu-id="31dce-528">メソッド urlEncode</span><span class="sxs-lookup"><span data-stu-id="31dce-528">Method urlEncode</span></span>

    public str urlEncode(str txt)

#### <a name="parameters"></a><span data-ttu-id="31dce-529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-529">Parameters</span></span>

<span data-ttu-id="31dce-530">txt</span><span class="sxs-lookup"><span data-stu-id="31dce-530">txt</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-531">Return Value</span></span>

### <a name="method-urlpathencode"></a><span data-ttu-id="31dce-532">メソッド urlPathEncode</span><span class="sxs-lookup"><span data-stu-id="31dce-532">Method urlPathEncode</span></span>

    public str urlPathEncode(str txt)

#### <a name="parameters"></a><span data-ttu-id="31dce-533">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-533">Parameters</span></span>

<span data-ttu-id="31dce-534">txt</span><span class="sxs-lookup"><span data-stu-id="31dce-534">txt</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-535">Return Value</span></span>

### <a name="method-execute"></a><span data-ttu-id="31dce-536">メソッド execute</span><span class="sxs-lookup"><span data-stu-id="31dce-536">Method execute</span></span>

    public void execute(str logicalPath)

#### <a name="parameters"></a><span data-ttu-id="31dce-537">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-537">Parameters</span></span>

<span data-ttu-id="31dce-538">logicalPath</span><span class="sxs-lookup"><span data-stu-id="31dce-538">logicalPath</span></span>  

### <a name="method-transfer"></a><span data-ttu-id="31dce-539">メソッド transfer</span><span class="sxs-lookup"><span data-stu-id="31dce-539">Method transfer</span></span>

    public void transfer(str logicalPath)

#### <a name="parameters"></a><span data-ttu-id="31dce-540">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-540">Parameters</span></span>

<span data-ttu-id="31dce-541">logicalPath</span><span class="sxs-lookup"><span data-stu-id="31dce-541">logicalPath</span></span>  

### <a name="method-new"></a><span data-ttu-id="31dce-542">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-542">Method new</span></span>

<span data-ttu-id="31dce-543">IISServer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-543">Initializes a new instance of the IISServer class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="31dce-544">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-544">Method finalize</span></span>

    public void finalize()

## <a name="class-iissessionobject"></a><span data-ttu-id="31dce-545">クラス IISSessionObject</span><span class="sxs-lookup"><span data-stu-id="31dce-545">Class IISSessionObject</span></span>
    class IISSessionObject extends Object

<span data-ttu-id="31dce-546">IISSessionObject クラスは、インターネット インフォメーション サービス (IIS) によって提供される Session オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-546">The IISSessionObject class wraps the Session object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-547">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-547">Remarks</span></span>

<span data-ttu-id="31dce-548">IISSessionObject クラスのメソッドと、IIS によって提供される Session オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-548">There is a one-to-one connection between the methods of the IISSessionObject class and the methods of the Session object that is offered by IIS.</span></span> <span data-ttu-id="31dce-549">したがって、IISSessionObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-549">Therefore, for more information about the methods of the IISSessionObject class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-550">IISSessionObject クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-550">Use of the IISSessionObject class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-551">例</span><span class="sxs-lookup"><span data-stu-id="31dce-551">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-552">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-552">Methods</span></span>

| <span data-ttu-id="31dce-553">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-553">Method</span></span>                                                 | <span data-ttu-id="31dce-554">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-554">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="31dce-555">public int codePage(\[int codePage\])</span><span class="sxs-lookup"><span data-stu-id="31dce-555">public int codePage(\[int codePage\])</span></span>                  |                                                           |
| <span data-ttu-id="31dce-556">public IISVariantDictionary contents()</span><span class="sxs-lookup"><span data-stu-id="31dce-556">public IISVariantDictionary contents()</span></span>                 |                                                           |
| <span data-ttu-id="31dce-557">public str getSessionID()</span><span class="sxs-lookup"><span data-stu-id="31dce-557">public str getSessionID()</span></span>                              |                                                           |
| <span data-ttu-id="31dce-558">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-558">public ComInterface interface()</span></span>                        |                                                           |
| <span data-ttu-id="31dce-559">public int lcid(\[int lcid\])</span><span class="sxs-lookup"><span data-stu-id="31dce-559">public int lcid(\[int lcid\])</span></span>                          |                                                           |
| <span data-ttu-id="31dce-560">public IISVariantDictionary staticObjects()</span><span class="sxs-lookup"><span data-stu-id="31dce-560">public IISVariantDictionary staticObjects()</span></span>            |                                                           |
| <span data-ttu-id="31dce-561">public int timeout(\[int timeout\])</span><span class="sxs-lookup"><span data-stu-id="31dce-561">public int timeout(\[int timeout\])</span></span>                    |                                                           |
| <span data-ttu-id="31dce-562">public COMVariant value(str value, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-562">public COMVariant value(str value, \[COMVariant var\])</span></span> |                                                           |
| <span data-ttu-id="31dce-563">public str valueTxt(str value, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-563">public str valueTxt(str value, \[str var\])</span></span>            |                                                           |
| <span data-ttu-id="31dce-564">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-564">public void new()</span></span>                                      | <span data-ttu-id="31dce-565">IISSessionObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-565">Initializes a new instance of the IISSessionObject class.</span></span> |
| <span data-ttu-id="31dce-566">public void abandon()</span><span class="sxs-lookup"><span data-stu-id="31dce-566">public void abandon()</span></span>                                  |                                                           |
| <span data-ttu-id="31dce-567">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-567">public void finalize()</span></span>                                 |                                                           |

### <a name="method-codepage"></a><span data-ttu-id="31dce-568">メソッド codePage</span><span class="sxs-lookup"><span data-stu-id="31dce-568">Method codePage</span></span>

    public int codePage([int codePage])

#### <a name="parameters"></a><span data-ttu-id="31dce-569">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-569">Parameters</span></span>

<span data-ttu-id="31dce-570">codePage</span><span class="sxs-lookup"><span data-stu-id="31dce-570">codePage</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-571">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-571">Return Value</span></span>

### <a name="method-contents"></a><span data-ttu-id="31dce-572">メソッド contents</span><span class="sxs-lookup"><span data-stu-id="31dce-572">Method contents</span></span>

    public IISVariantDictionary contents()

#### <a name="return-value"></a><span data-ttu-id="31dce-573">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-573">Return Value</span></span>

### <a name="method-getsessionid"></a><span data-ttu-id="31dce-574">メソッド getSessionID</span><span class="sxs-lookup"><span data-stu-id="31dce-574">Method getSessionID</span></span>

    public str getSessionID()

#### <a name="return-value"></a><span data-ttu-id="31dce-575">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-575">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-576">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-576">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-577">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-577">Return Value</span></span>

### <a name="method-lcid"></a><span data-ttu-id="31dce-578">メソッド lcid</span><span class="sxs-lookup"><span data-stu-id="31dce-578">Method lcid</span></span>

    public int lcid([int lcid])

#### <a name="parameters"></a><span data-ttu-id="31dce-579">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-579">Parameters</span></span>

<span data-ttu-id="31dce-580">lcid</span><span class="sxs-lookup"><span data-stu-id="31dce-580">lcid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-581">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-581">Return Value</span></span>

### <a name="method-staticobjects"></a><span data-ttu-id="31dce-582">メソッド staticObjects</span><span class="sxs-lookup"><span data-stu-id="31dce-582">Method staticObjects</span></span>

    public IISVariantDictionary staticObjects()

#### <a name="return-value"></a><span data-ttu-id="31dce-583">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-583">Return Value</span></span>

### <a name="method-timeout"></a><span data-ttu-id="31dce-584">メソッド timeout</span><span class="sxs-lookup"><span data-stu-id="31dce-584">Method timeout</span></span>

    public int timeout([int timeout])

#### <a name="parameters"></a><span data-ttu-id="31dce-585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-585">Parameters</span></span>

<span data-ttu-id="31dce-586">timeout</span><span class="sxs-lookup"><span data-stu-id="31dce-586">timeout</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-587">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-587">Return Value</span></span>

### <a name="method-value"></a><span data-ttu-id="31dce-588">メソッド value</span><span class="sxs-lookup"><span data-stu-id="31dce-588">Method value</span></span>

    public COMVariant value(str value, [COMVariant var])

#### <a name="parameters"></a><span data-ttu-id="31dce-589">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-589">Parameters</span></span>

<span data-ttu-id="31dce-590">値</span><span class="sxs-lookup"><span data-stu-id="31dce-590">value</span></span>  

<!-- -->

<span data-ttu-id="31dce-591">var</span><span class="sxs-lookup"><span data-stu-id="31dce-591">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-592">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-592">Return Value</span></span>

### <a name="method-valuetxt"></a><span data-ttu-id="31dce-593">メソッド valueTxt</span><span class="sxs-lookup"><span data-stu-id="31dce-593">Method valueTxt</span></span>

    public str valueTxt(str value, [str var])

#### <a name="parameters"></a><span data-ttu-id="31dce-594">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-594">Parameters</span></span>

<span data-ttu-id="31dce-595">値</span><span class="sxs-lookup"><span data-stu-id="31dce-595">value</span></span>  

<!-- -->

<span data-ttu-id="31dce-596">var</span><span class="sxs-lookup"><span data-stu-id="31dce-596">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-597">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-597">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-598">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-598">Method new</span></span>

<span data-ttu-id="31dce-599">IISSessionObject クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-599">Initializes a new instance of the IISSessionObject class.</span></span>

    public void new()

### <a name="method-abandon"></a><span data-ttu-id="31dce-600">メソッド abandon</span><span class="sxs-lookup"><span data-stu-id="31dce-600">Method abandon</span></span>

    public void abandon()

### <a name="method-finalize"></a><span data-ttu-id="31dce-601">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-601">Method finalize</span></span>

    public void finalize()

## <a name="class-iisstringlist"></a><span data-ttu-id="31dce-602">クラス IISStringList</span><span class="sxs-lookup"><span data-stu-id="31dce-602">Class IISStringList</span></span>
    class IISStringList extends Object

<span data-ttu-id="31dce-603">IISStringList クラスは、インターネット インフォメーション サービス (IIS) によって提供される StringList オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-603">The IISStringList class wraps the StringList object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-604">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-604">Remarks</span></span>

<span data-ttu-id="31dce-605">IISStringList クラスのメソッドと、IIS によって提供される StringList オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-605">There is a one-to-one connection between the methods of the IISStringList class and the methods of the StringList object that is offered by IIS.</span></span> <span data-ttu-id="31dce-606">したがって、IISStringList クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-606">Therefore, for more information about the methods of the IISStringList class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-607">IISStringList クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-607">Use of the IISStringList class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-608">例</span><span class="sxs-lookup"><span data-stu-id="31dce-608">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-609">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-609">Methods</span></span>

| <span data-ttu-id="31dce-610">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-610">Method</span></span>                           | <span data-ttu-id="31dce-611">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-611">Description</span></span>                                     |
|----------------------------------|-------------------------------------------------|
| <span data-ttu-id="31dce-612">public int count()</span><span class="sxs-lookup"><span data-stu-id="31dce-612">public int count()</span></span>               |                                                 |
| <span data-ttu-id="31dce-613">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="31dce-613">public COMEnum2Variant getEnum()</span></span> |                                                 |
| <span data-ttu-id="31dce-614">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-614">public ComInterface interface()</span></span>  |                                                 |
| <span data-ttu-id="31dce-615">public str item(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="31dce-615">public str item(\[str item\])</span></span>    |                                                 |
| <span data-ttu-id="31dce-616">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-616">public void finalize()</span></span>           |                                                 |
| <span data-ttu-id="31dce-617">public void new(COM stringList)</span><span class="sxs-lookup"><span data-stu-id="31dce-617">public void new(COM stringList)</span></span>  | <span data-ttu-id="31dce-618">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-618">Initializes a new instance of the Object class.</span></span> |

### <a name="method-count"></a><span data-ttu-id="31dce-619">メソッド count</span><span class="sxs-lookup"><span data-stu-id="31dce-619">Method count</span></span>

    public int count()

#### <a name="return-value"></a><span data-ttu-id="31dce-620">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-620">Return Value</span></span>

### <a name="method-getenum"></a><span data-ttu-id="31dce-621">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="31dce-621">Method getEnum</span></span>

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a><span data-ttu-id="31dce-622">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-622">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-623">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-623">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-624">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-624">Return Value</span></span>

### <a name="method-item"></a><span data-ttu-id="31dce-625">メソッド item</span><span class="sxs-lookup"><span data-stu-id="31dce-625">Method item</span></span>

    public str item([str item])

#### <a name="parameters"></a><span data-ttu-id="31dce-626">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-626">Parameters</span></span>

<span data-ttu-id="31dce-627">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-627">item</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-628">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-628">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-629">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-629">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="31dce-630">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-630">Method new</span></span>

<span data-ttu-id="31dce-631">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-631">Initializes a new instance of the Object class.</span></span>

    public void new(COM stringList)

#### <a name="parameters"></a><span data-ttu-id="31dce-632">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-632">Parameters</span></span>

<span data-ttu-id="31dce-633">stringList</span><span class="sxs-lookup"><span data-stu-id="31dce-633">stringList</span></span>  

## <a name="class-iisvariantdictionary"></a><span data-ttu-id="31dce-634">クラス IISVariantDictionary</span><span class="sxs-lookup"><span data-stu-id="31dce-634">Class IISVariantDictionary</span></span>
    class IISVariantDictionary extends Object

<span data-ttu-id="31dce-635">IISVariantDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される VariantDictionary オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-635">The IISVariantDictionary class wraps the VariantDictionary object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-636">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-636">Remarks</span></span>

<span data-ttu-id="31dce-637">IISVariantDictionary クラスのメソッドと、IIS によって提供される VariantDictionary オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-637">There is a one-to-one connection between the methods of the IISVariantDictionary class and the methods of the VariantDictionary object that is offered by IIS.</span></span> <span data-ttu-id="31dce-638">したがって、IISVariantDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-638">Therefore, for more information about the methods of the IISVariantDictionary class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-639">IISVariantDictionary クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-639">Use of the IISVariantDictionary class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-640">例</span><span class="sxs-lookup"><span data-stu-id="31dce-640">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-641">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-641">Methods</span></span>

| <span data-ttu-id="31dce-642">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-642">Method</span></span>                                                      | <span data-ttu-id="31dce-643">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-643">Description</span></span>                                     |
|-------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="31dce-644">public int count()</span><span class="sxs-lookup"><span data-stu-id="31dce-644">public int count()</span></span>                                          |                                                 |
| <span data-ttu-id="31dce-645">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="31dce-645">public COMEnum2Variant getEnum()</span></span>                            |                                                 |
| <span data-ttu-id="31dce-646">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-646">public ComInterface interface()</span></span>                             |                                                 |
| <span data-ttu-id="31dce-647">public COMVariant item(COMVariant item, \[COMVariant var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-647">public COMVariant item(COMVariant item, \[COMVariant var\])</span></span> |                                                 |
| <span data-ttu-id="31dce-648">public COM itemObj(str item, \[COM var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-648">public COM itemObj(str item, \[COM var\])</span></span>                   |                                                 |
| <span data-ttu-id="31dce-649">public str itemTxt(str item, \[str var\])</span><span class="sxs-lookup"><span data-stu-id="31dce-649">public str itemTxt(str item, \[str var\])</span></span>                   |                                                 |
| <span data-ttu-id="31dce-650">public str key(str key)</span><span class="sxs-lookup"><span data-stu-id="31dce-650">public str key(str key)</span></span>                                     |                                                 |
| <span data-ttu-id="31dce-651">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-651">public void finalize()</span></span>                                      |                                                 |
| <span data-ttu-id="31dce-652">public void remove(str key)</span><span class="sxs-lookup"><span data-stu-id="31dce-652">public void remove(str key)</span></span>                                 |                                                 |
| <span data-ttu-id="31dce-653">public void removeAll()</span><span class="sxs-lookup"><span data-stu-id="31dce-653">public void removeAll()</span></span>                                     |                                                 |
| <span data-ttu-id="31dce-654">public void new(COM variantDictionary)</span><span class="sxs-lookup"><span data-stu-id="31dce-654">public void new(COM variantDictionary)</span></span>                      | <span data-ttu-id="31dce-655">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-655">Initializes a new instance of the Object class.</span></span> |

### <a name="method-count"></a><span data-ttu-id="31dce-656">メソッド count</span><span class="sxs-lookup"><span data-stu-id="31dce-656">Method count</span></span>

    public int count()

#### <a name="return-value"></a><span data-ttu-id="31dce-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-657">Return Value</span></span>

### <a name="method-getenum"></a><span data-ttu-id="31dce-658">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="31dce-658">Method getEnum</span></span>

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a><span data-ttu-id="31dce-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-659">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-660">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-660">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-661">Return Value</span></span>

### <a name="method-item"></a><span data-ttu-id="31dce-662">メソッド item</span><span class="sxs-lookup"><span data-stu-id="31dce-662">Method item</span></span>

    public COMVariant item(COMVariant item, [COMVariant var])

#### <a name="parameters"></a><span data-ttu-id="31dce-663">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-663">Parameters</span></span>

<span data-ttu-id="31dce-664">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-664">item</span></span>  

<!-- -->

<span data-ttu-id="31dce-665">var</span><span class="sxs-lookup"><span data-stu-id="31dce-665">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-666">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-666">Return Value</span></span>

### <a name="method-itemobj"></a><span data-ttu-id="31dce-667">メソッド itemObj</span><span class="sxs-lookup"><span data-stu-id="31dce-667">Method itemObj</span></span>

    public COM itemObj(str item, [COM var])

#### <a name="parameters"></a><span data-ttu-id="31dce-668">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-668">Parameters</span></span>

<span data-ttu-id="31dce-669">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-669">item</span></span>  

<!-- -->

<span data-ttu-id="31dce-670">var</span><span class="sxs-lookup"><span data-stu-id="31dce-670">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-671">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-671">Return Value</span></span>

### <a name="method-itemtxt"></a><span data-ttu-id="31dce-672">メソッド itemTxt</span><span class="sxs-lookup"><span data-stu-id="31dce-672">Method itemTxt</span></span>

    public str itemTxt(str item, [str var])

#### <a name="parameters"></a><span data-ttu-id="31dce-673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-673">Parameters</span></span>

<span data-ttu-id="31dce-674">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-674">item</span></span>  

<!-- -->

<span data-ttu-id="31dce-675">var</span><span class="sxs-lookup"><span data-stu-id="31dce-675">var</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-676">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-676">Return Value</span></span>

### <a name="method-key"></a><span data-ttu-id="31dce-677">メソッド key</span><span class="sxs-lookup"><span data-stu-id="31dce-677">Method key</span></span>

    public str key(str key)

#### <a name="parameters"></a><span data-ttu-id="31dce-678">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-678">Parameters</span></span>

<span data-ttu-id="31dce-679">キー</span><span class="sxs-lookup"><span data-stu-id="31dce-679">key</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-680">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-680">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-681">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-681">Method finalize</span></span>

    public void finalize()

### <a name="method-remove"></a><span data-ttu-id="31dce-682">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="31dce-682">Method remove</span></span>

    public void remove(str key)

#### <a name="parameters"></a><span data-ttu-id="31dce-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-683">Parameters</span></span>

<span data-ttu-id="31dce-684">キー</span><span class="sxs-lookup"><span data-stu-id="31dce-684">key</span></span>  

### <a name="method-removeall"></a><span data-ttu-id="31dce-685">メソッド removeAll</span><span class="sxs-lookup"><span data-stu-id="31dce-685">Method removeAll</span></span>

    public void removeAll()

### <a name="method-new"></a><span data-ttu-id="31dce-686">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-686">Method new</span></span>

<span data-ttu-id="31dce-687">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-687">Initializes a new instance of the Object class.</span></span>

    public void new(COM variantDictionary)

#### <a name="parameters"></a><span data-ttu-id="31dce-688">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-688">Parameters</span></span>

<span data-ttu-id="31dce-689">variantDictionary</span><span class="sxs-lookup"><span data-stu-id="31dce-689">variantDictionary</span></span>  

## <a name="class-iisviewstate"></a><span data-ttu-id="31dce-690">クラス IISViewState</span><span class="sxs-lookup"><span data-stu-id="31dce-690">Class IISViewState</span></span>
    class IISViewState extends Object

### <a name="remarks"></a><span data-ttu-id="31dce-691">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-691">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-692">例</span><span class="sxs-lookup"><span data-stu-id="31dce-692">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-693">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-693">Methods</span></span>

| <span data-ttu-id="31dce-694">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-694">Method</span></span>                                         | <span data-ttu-id="31dce-695">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-695">Description</span></span>                                           |
|------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="31dce-696">public boolean viewStateContains(str key)</span><span class="sxs-lookup"><span data-stu-id="31dce-696">public boolean viewStateContains(str key)</span></span>      |                                                       |
| <span data-ttu-id="31dce-697">public str viewStateItem(str key, \[str val\])</span><span class="sxs-lookup"><span data-stu-id="31dce-697">public str viewStateItem(str key, \[str val\])</span></span> |                                                       |
| <span data-ttu-id="31dce-698">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-698">public void finalize()</span></span>                         |                                                       |
| <span data-ttu-id="31dce-699">public void viewStateDelete(str key)</span><span class="sxs-lookup"><span data-stu-id="31dce-699">public void viewStateDelete(str key)</span></span>           |                                                       |
| <span data-ttu-id="31dce-700">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-700">public void new()</span></span>                              | <span data-ttu-id="31dce-701">IISViewState クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-701">Initializes a new instance of the IISViewState class.</span></span> |

### <a name="method-viewstatecontains"></a><span data-ttu-id="31dce-702">メソッド viewStateContains</span><span class="sxs-lookup"><span data-stu-id="31dce-702">Method viewStateContains</span></span>

    public boolean viewStateContains(str key)

#### <a name="parameters"></a><span data-ttu-id="31dce-703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-703">Parameters</span></span>

<span data-ttu-id="31dce-704">キー</span><span class="sxs-lookup"><span data-stu-id="31dce-704">key</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-705">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-705">Return Value</span></span>

### <a name="method-viewstateitem"></a><span data-ttu-id="31dce-706">メソッド viewStateItem</span><span class="sxs-lookup"><span data-stu-id="31dce-706">Method viewStateItem</span></span>

    public str viewStateItem(str key, [str val])

#### <a name="parameters"></a><span data-ttu-id="31dce-707">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-707">Parameters</span></span>

<span data-ttu-id="31dce-708">キー</span><span class="sxs-lookup"><span data-stu-id="31dce-708">key</span></span>  

<!-- -->

<span data-ttu-id="31dce-709">val</span><span class="sxs-lookup"><span data-stu-id="31dce-709">val</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-710">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-710">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-711">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-711">Method finalize</span></span>

    public void finalize()

### <a name="method-viewstatedelete"></a><span data-ttu-id="31dce-712">メソッド viewStateDelete</span><span class="sxs-lookup"><span data-stu-id="31dce-712">Method viewStateDelete</span></span>

    public void viewStateDelete(str key)

#### <a name="parameters"></a><span data-ttu-id="31dce-713">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-713">Parameters</span></span>

<span data-ttu-id="31dce-714">キー</span><span class="sxs-lookup"><span data-stu-id="31dce-714">key</span></span>  

### <a name="method-new"></a><span data-ttu-id="31dce-715">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-715">Method new</span></span>

<span data-ttu-id="31dce-716">IISViewState クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-716">Initializes a new instance of the IISViewState class.</span></span>

    public void new()

## <a name="class-iiswritecookie"></a><span data-ttu-id="31dce-717">クラス IISWriteCookie</span><span class="sxs-lookup"><span data-stu-id="31dce-717">Class IISWriteCookie</span></span>
    class IISWriteCookie extends Object

<span data-ttu-id="31dce-718">IISWriteCookie クラスは、インターネット インフォメーション サービス (IIS) によって提供される WriteCookie オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="31dce-718">The IISWriteCookie class wraps the WriteCookie object that is offered by Internet Information Services (IIS).</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-719">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-719">Remarks</span></span>

<span data-ttu-id="31dce-720">IISWriteCookie クラスのメソッドと、IIS によって提供される WriteCookie オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-720">There is a one-to-one connection between the methods of the IISWriteCookie class and the methods of the WriteCookie object that is offered by IIS.</span></span> <span data-ttu-id="31dce-721">したがって、IISWriteCookie クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-721">Therefore, for more information about the methods of the IISWriteCookie class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="31dce-722">IISWriteCookie クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-722">Use of the IISWriteCookie class is valid only when code is run by the Finance and Operations Internet Connector under IIS.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-723">例</span><span class="sxs-lookup"><span data-stu-id="31dce-723">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-724">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-724">Methods</span></span>

| <span data-ttu-id="31dce-725">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-725">Method</span></span>                                  | <span data-ttu-id="31dce-726">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-726">Description</span></span>                                     |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="31dce-727">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="31dce-727">public COMEnum2Variant getEnum()</span></span>        |                                                 |
| <span data-ttu-id="31dce-728">public boolean hasKeys()</span><span class="sxs-lookup"><span data-stu-id="31dce-728">public boolean hasKeys()</span></span>                |                                                 |
| <span data-ttu-id="31dce-729">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="31dce-729">public ComInterface interface()</span></span>         |                                                 |
| <span data-ttu-id="31dce-730">public void new(COM writeCookie)</span><span class="sxs-lookup"><span data-stu-id="31dce-730">public void new(COM writeCookie)</span></span>        | <span data-ttu-id="31dce-731">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-731">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="31dce-732">public void secure(boolean secure)</span><span class="sxs-lookup"><span data-stu-id="31dce-732">public void secure(boolean secure)</span></span>      |                                                 |
| <span data-ttu-id="31dce-733">public void path(str path)</span><span class="sxs-lookup"><span data-stu-id="31dce-733">public void path(str path)</span></span>              |                                                 |
| <span data-ttu-id="31dce-734">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-734">public void finalize()</span></span>                  |                                                 |
| <span data-ttu-id="31dce-735">public void domain(str domain)</span><span class="sxs-lookup"><span data-stu-id="31dce-735">public void domain(str domain)</span></span>          |                                                 |
| <span data-ttu-id="31dce-736">public void expires(COMVariant expires)</span><span class="sxs-lookup"><span data-stu-id="31dce-736">public void expires(COMVariant expires)</span></span> |                                                 |
| <span data-ttu-id="31dce-737">public void item(str item, str value)</span><span class="sxs-lookup"><span data-stu-id="31dce-737">public void item(str item, str value)</span></span>   |                                                 |

### <a name="method-getenum"></a><span data-ttu-id="31dce-738">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="31dce-738">Method getEnum</span></span>

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a><span data-ttu-id="31dce-739">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-739">Return Value</span></span>

### <a name="method-haskeys"></a><span data-ttu-id="31dce-740">メソッド hasKeys</span><span class="sxs-lookup"><span data-stu-id="31dce-740">Method hasKeys</span></span>

    public boolean hasKeys()

#### <a name="return-value"></a><span data-ttu-id="31dce-741">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-741">Return Value</span></span>

### <a name="method-interface"></a><span data-ttu-id="31dce-742">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="31dce-742">Method interface</span></span>

    public ComInterface interface()

#### <a name="return-value"></a><span data-ttu-id="31dce-743">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-743">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-744">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-744">Method new</span></span>

<span data-ttu-id="31dce-745">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-745">Initializes a new instance of the Object class.</span></span>

    public void new(COM writeCookie)

#### <a name="parameters"></a><span data-ttu-id="31dce-746">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-746">Parameters</span></span>

<span data-ttu-id="31dce-747">writeCookie</span><span class="sxs-lookup"><span data-stu-id="31dce-747">writeCookie</span></span>  

### <a name="method-secure"></a><span data-ttu-id="31dce-748">メソッド secure</span><span class="sxs-lookup"><span data-stu-id="31dce-748">Method secure</span></span>

    public void secure(boolean secure)

#### <a name="parameters"></a><span data-ttu-id="31dce-749">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-749">Parameters</span></span>

<span data-ttu-id="31dce-750">secure</span><span class="sxs-lookup"><span data-stu-id="31dce-750">secure</span></span>  

### <a name="method-path"></a><span data-ttu-id="31dce-751">メソッド path</span><span class="sxs-lookup"><span data-stu-id="31dce-751">Method path</span></span>

    public void path(str path)

#### <a name="parameters"></a><span data-ttu-id="31dce-752">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-752">Parameters</span></span>

<span data-ttu-id="31dce-753">path</span><span class="sxs-lookup"><span data-stu-id="31dce-753">path</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="31dce-754">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-754">Method finalize</span></span>

    public void finalize()

### <a name="method-domain"></a><span data-ttu-id="31dce-755">メソッド domain</span><span class="sxs-lookup"><span data-stu-id="31dce-755">Method domain</span></span>

    public void domain(str domain)

#### <a name="parameters"></a><span data-ttu-id="31dce-756">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-756">Parameters</span></span>

<span data-ttu-id="31dce-757">domain</span><span class="sxs-lookup"><span data-stu-id="31dce-757">domain</span></span>  

### <a name="method-expires"></a><span data-ttu-id="31dce-758">メソッド expires</span><span class="sxs-lookup"><span data-stu-id="31dce-758">Method expires</span></span>

    public void expires(COMVariant expires)

#### <a name="parameters"></a><span data-ttu-id="31dce-759">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-759">Parameters</span></span>

<span data-ttu-id="31dce-760">expires</span><span class="sxs-lookup"><span data-stu-id="31dce-760">expires</span></span>  

### <a name="method-item"></a><span data-ttu-id="31dce-761">メソッド item</span><span class="sxs-lookup"><span data-stu-id="31dce-761">Method item</span></span>

    public void item(str item, str value)

#### <a name="parameters"></a><span data-ttu-id="31dce-762">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-762">Parameters</span></span>

<span data-ttu-id="31dce-763">項目</span><span class="sxs-lookup"><span data-stu-id="31dce-763">item</span></span>  

<!-- -->

<span data-ttu-id="31dce-764">値</span><span class="sxs-lookup"><span data-stu-id="31dce-764">value</span></span>  

## <a name="class-image"></a><span data-ttu-id="31dce-765">クラス イメージ</span><span class="sxs-lookup"><span data-stu-id="31dce-765">Class Image</span></span>
    class Image extends BinData

<span data-ttu-id="31dce-766">読み込み、保存、および画像を操作するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="31dce-766">Provides methods for loading, saving, and manipulating images.</span></span> <span data-ttu-id="31dce-767">複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="31dce-767">If you want to manipulate several images at the same time, use the Imagelist Class.</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-768">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-768">Remarks</span></span>

<span data-ttu-id="31dce-769">次のファイル タイプからイメージ オブジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-769">You can construct Image objects from the following file types:</span></span>

-   <span data-ttu-id="31dce-770">ラスター (ビットマップ) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif</span><span class="sxs-lookup"><span data-stu-id="31dce-770">Raster (bitmap) formats - .bmp, .gif, .jpg, .png, .tiff, and .exif</span></span>
-   <span data-ttu-id="31dce-771">ベクター形式 - .emf および .wmf</span><span class="sxs-lookup"><span data-stu-id="31dce-771">Vector formats - .emf and .wmf</span></span>

<span data-ttu-id="31dce-772">複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="31dce-772">If you want to work with several images at the same time, use the Imagelist class.</span></span> <span data-ttu-id="31dce-773">次のファイル タイプからイメージ オブジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-773">You can construct the Image objects from the following file types:</span></span>

-   <span data-ttu-id="31dce-774">ラスター (ビットマップである) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif</span><span class="sxs-lookup"><span data-stu-id="31dce-774">Raster, which is a bitmap, formats - .bmp, .gif, .jpg, .png, .tiff, and .exif</span></span>
-   <span data-ttu-id="31dce-775">ベクター形式 - .emf および .wmf</span><span class="sxs-lookup"><span data-stu-id="31dce-775">Vector formats - .emf and .wmf</span></span>

<span data-ttu-id="31dce-776">Finance and Operations では、イメージ クラスはクライアントにバインドされています。</span><span class="sxs-lookup"><span data-stu-id="31dce-776">In Finance and Operations, the Image class is bound to the client.</span></span> <span data-ttu-id="31dce-777">ファイル操作に伴うセキュリティ上のリスクのため、クラスをサーバーから実行できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="31dce-777">The class can no longer be run from the server because of the security risks that are associated with file handling.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-778">例</span><span class="sxs-lookup"><span data-stu-id="31dce-778">Examples</span></span>

<span data-ttu-id="31dce-779">次の例では、Picture.jpg の高さをピクセル単位で出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-779">The following example prints the height of Picture.jpg in pixels.</span></span>

    Image img = new  Image(); 
    img.loadFile(@'C:\MyPictures\Picture.jpg'); 
    print img.height(); 
    pause;

### <a name="methods"></a><span data-ttu-id="31dce-780">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-780">Methods</span></span>

| <span data-ttu-id="31dce-781">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-781">Method</span></span>                                                                                                      | <span data-ttu-id="31dce-782">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-782">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-783">public int captureScreen(int left, int top, int right, int bottom)</span><span class="sxs-lookup"><span data-stu-id="31dce-783">public int captureScreen(int left, int top, int right, int bottom)</span></span>                                          | <span data-ttu-id="31dce-784">パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="31dce-784">Captures an image from the screen by using the coordinates that are supplied in the parameter list.</span></span>                                           |
| <span data-ttu-id="31dce-785">public int captureWindow(int hWnd)</span><span class="sxs-lookup"><span data-stu-id="31dce-785">public int captureWindow(int hWnd)</span></span>                                                                          | <span data-ttu-id="31dce-786">パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="31dce-786">Captures a window as an image, using the handle that is supplied as a parameter.</span></span>                                                              |
| <span data-ttu-id="31dce-787">public int clipboardCopy()</span><span class="sxs-lookup"><span data-stu-id="31dce-787">public int clipboardCopy()</span></span>                                                                                  | <span data-ttu-id="31dce-788">イメージをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="31dce-788">Copies an image to the clipboard.</span></span>                                                                                                             |
| <span data-ttu-id="31dce-789">public int clipboardPaste()</span><span class="sxs-lookup"><span data-stu-id="31dce-789">public int clipboardPaste()</span></span>                                                                                 | <span data-ttu-id="31dce-790">システムのクリップボードの内容で既存のイメージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="31dce-790">Overwrites an existing image with the content of the system clipboard.</span></span>                                                                        |
| <span data-ttu-id="31dce-791">public int copyImage(Image image)</span><span class="sxs-lookup"><span data-stu-id="31dce-791">public int copyImage(Image image)</span></span>                                                                           | <span data-ttu-id="31dce-792">現在のイメージ オブジェクトをコピーします。</span><span class="sxs-lookup"><span data-stu-id="31dce-792">Copies the current image object.</span></span>                                                                                                              |
| <span data-ttu-id="31dce-793">public int createImage(int Width, int Height, int BitsPerPixel)</span><span class="sxs-lookup"><span data-stu-id="31dce-793">public int createImage(int Width, int Height, int BitsPerPixel)</span></span>                                             | <span data-ttu-id="31dce-794">パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-794">Creates an empty bitmap image with the width, height, and color depth as specified by the parameters.</span></span>                                         |
| <span data-ttu-id="31dce-795">public int crop(int x, int y, int w, int h)</span><span class="sxs-lookup"><span data-stu-id="31dce-795">public int crop(int x, int y, int w, int h)</span></span>                                                                 | <span data-ttu-id="31dce-796">画像をトリミングします。</span><span class="sxs-lookup"><span data-stu-id="31dce-796">Crops the image.</span></span>                                                                                                                              |
| <span data-ttu-id="31dce-797">public int displayImage(Int64 HDC, \[int Mode\], \[int Xpos\], \[int Ypos\], \[int Width\], \[int Height\])</span><span class="sxs-lookup"><span data-stu-id="31dce-797">public int displayImage(Int64 HDC, \[int Mode\], \[int Xpos\], \[int Ypos\], \[int Width\], \[int Height\])</span></span> | <span data-ttu-id="31dce-798">HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。</span><span class="sxs-lookup"><span data-stu-id="31dce-798">Draws an image with the device context specified by the HDC parameter.</span></span>                                                                        |
| <span data-ttu-id="31dce-799">public Int64 exportBitmap()</span><span class="sxs-lookup"><span data-stu-id="31dce-799">public Int64 exportBitmap()</span></span>                                                                                 | <span data-ttu-id="31dce-800">画像のハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-800">Gets a handle for the image.</span></span>                                                                                                                  |
| <span data-ttu-id="31dce-801">public int flip(FlipType FlipType)</span><span class="sxs-lookup"><span data-stu-id="31dce-801">public int flip(FlipType FlipType)</span></span>                                                                          | <span data-ttu-id="31dce-802">画像を垂直または水平方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-802">Rotates the image 180 degrees in a vertical or horizontal direction.</span></span>                                                                          |
| <span data-ttu-id="31dce-803">public container getImageDimensionUnits()</span><span class="sxs-lookup"><span data-stu-id="31dce-803">public container getImageDimensionUnits()</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="31dce-804">public int getPixel(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31dce-804">public int getPixel(int x, int y)</span></span>                                                                           | <span data-ttu-id="31dce-805">パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-805">Retrieves the ARGB color value of the pixel at the point that is specified by the parameters.</span></span>                                                 |
| <span data-ttu-id="31dce-806">public int height()</span><span class="sxs-lookup"><span data-stu-id="31dce-806">public int height()</span></span>                                                                                         | <span data-ttu-id="31dce-807">ピクセル単位の画像の高さを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-807">Retrieves the height of the image in pixels.</span></span>                                                                                                  |
| <span data-ttu-id="31dce-808">public container imageInfo()</span><span class="sxs-lookup"><span data-stu-id="31dce-808">public container imageInfo()</span></span>                                                                                | <span data-ttu-id="31dce-809">画像の幅、高さ、色深度を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-809">Retrieves the width, height, and color depth of the image.</span></span>                                                                                    |
| <span data-ttu-id="31dce-810">public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)</span><span class="sxs-lookup"><span data-stu-id="31dce-810">public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)</span></span>                           | <span data-ttu-id="31dce-811">センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-811">Produces a spotlight effect within the circle that is defined by radius with center coordinates x and y.</span></span>                                      |
| <span data-ttu-id="31dce-812">public int importBitmap(Int64 hBitmap)</span><span class="sxs-lookup"><span data-stu-id="31dce-812">public int importBitmap(Int64 hBitmap)</span></span>                                                                      | <span data-ttu-id="31dce-813">hBitmap パラメータで指定されたイメージからビットマップをクローンします。</span><span class="sxs-lookup"><span data-stu-id="31dce-813">Clones a bitmap from the image that is specified by the hBitmap parameter.</span></span>                                                                    |
| <span data-ttu-id="31dce-814">public int importFileIcon(str fileName)</span><span class="sxs-lookup"><span data-stu-id="31dce-814">public int importFileIcon(str fileName)</span></span>                                                                     | <span data-ttu-id="31dce-815">ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-815">Creates an icon from the file specified by the fileName parameter by copying the icon that is used for the file.</span></span>                              |
| <span data-ttu-id="31dce-816">public int importIcon(str fileName, int iconIdx)</span><span class="sxs-lookup"><span data-stu-id="31dce-816">public int importIcon(str fileName, int iconIdx)</span></span>                                                            | <span data-ttu-id="31dce-817">Finance and Operations の実行可能ファイルからアイコンへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-817">Retrieves a handle to an icon from an executable file in Finance and Operations.</span></span> <span data-ttu-id="31dce-818">このアイコンは、fileName および iconIdx パラメーターで指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-818">The icon is specified by the fileName and iconIdx parameters.</span></span> |
| <span data-ttu-id="31dce-819">public int loadImage(str fileName)</span><span class="sxs-lookup"><span data-stu-id="31dce-819">public int loadImage(str fileName)</span></span>                                                                          | <span data-ttu-id="31dce-820">fileName パラメーターで指定されたファイルからイメージを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="31dce-820">Loads an image from the file specified by the fileName parameter.</span></span>                                                                             |
| <span data-ttu-id="31dce-821">public int loadResource(int id)</span><span class="sxs-lookup"><span data-stu-id="31dce-821">public int loadResource(int id)</span></span>                                                                             | <span data-ttu-id="31dce-822">Ax32.exe からリソースを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="31dce-822">Loads a resource from Ax32.exe.</span></span>                                                                                                               |
| <span data-ttu-id="31dce-823">public int promoteColor(int noOfColorBits)</span><span class="sxs-lookup"><span data-stu-id="31dce-823">public int promoteColor(int noOfColorBits)</span></span>                                                                  | <span data-ttu-id="31dce-824">画像の色深度を向上させます。</span><span class="sxs-lookup"><span data-stu-id="31dce-824">Increases the color depth of the image.</span></span>                                                                                                       |
| <span data-ttu-id="31dce-825">public int reduceColorOctree(int maxColors)</span><span class="sxs-lookup"><span data-stu-id="31dce-825">public int reduceColorOctree(int maxColors)</span></span>                                                                 | <span data-ttu-id="31dce-826">画像の色深度を減少させます。</span><span class="sxs-lookup"><span data-stu-id="31dce-826">Reduces the color depth of an image.</span></span>                                                                                                          |
| <span data-ttu-id="31dce-827">public int removeImage()</span><span class="sxs-lookup"><span data-stu-id="31dce-827">public int removeImage()</span></span>                                                                                    | <span data-ttu-id="31dce-828">画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。</span><span class="sxs-lookup"><span data-stu-id="31dce-828">Removes the data about an image; the object still exists, but has no data.</span></span>                                                                    |
| <span data-ttu-id="31dce-829">public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)</span><span class="sxs-lookup"><span data-stu-id="31dce-829">public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)</span></span>                         | <span data-ttu-id="31dce-830">newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。</span><span class="sxs-lookup"><span data-stu-id="31dce-830">Resizes the image to the size that is specified by the newWidth and newHeight parameters.</span></span>                                                     |
| <span data-ttu-id="31dce-831">public int rotate(RotateType RotateType)</span><span class="sxs-lookup"><span data-stu-id="31dce-831">public int rotate(RotateType RotateType)</span></span>                                                                    | <span data-ttu-id="31dce-832">画像を回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-832">Rotates the image.</span></span>                                                                                                                            |
| <span data-ttu-id="31dce-833">public int saveImage(str fileName, \[ImageSaveType Type\])</span><span class="sxs-lookup"><span data-stu-id="31dce-833">public int saveImage(str fileName, \[ImageSaveType Type\])</span></span>                                                  | <span data-ttu-id="31dce-834">指定されたファイル名に画像を保存します。</span><span class="sxs-lookup"><span data-stu-id="31dce-834">Saves the image to the specified file name.</span></span>                                                                                                   |
| <span data-ttu-id="31dce-835">public ImageSaveType saveType(\[ImageSaveType Type\])</span><span class="sxs-lookup"><span data-stu-id="31dce-835">public ImageSaveType saveType(\[ImageSaveType Type\])</span></span>                                                       | <span data-ttu-id="31dce-836">イメージ デコーダを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-836">Gets or sets the image decoder.</span></span>                                                                                                               |
| <span data-ttu-id="31dce-837">public int setPixel(int x, int y, int pixel)</span><span class="sxs-lookup"><span data-stu-id="31dce-837">public int setPixel(int x, int y, int pixel)</span></span>                                                                | <span data-ttu-id="31dce-838">x と y パラメーターで指定されているピクセルの色を設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-838">Sets the color for the pixel that is specified by the x and y parameters.</span></span>                                                                     |
| <span data-ttu-id="31dce-839">public int transparent(\[boolean Set\], \[int RValue\], \[int GValue\], \[int BValue\])</span><span class="sxs-lookup"><span data-stu-id="31dce-839">public int transparent(\[boolean Set\], \[int RValue\], \[int GValue\], \[int BValue\])</span></span>                     | <span data-ttu-id="31dce-840">画像の透明な色を設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-840">Sets the transparent color for the image.</span></span>                                                                                                     |
| <span data-ttu-id="31dce-841">public int width()</span><span class="sxs-lookup"><span data-stu-id="31dce-841">public int width()</span></span>                                                                                          | <span data-ttu-id="31dce-842">ピクセル単位の画像の幅を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-842">Retrieves the width of the image in pixels.</span></span>                                                                                                   |
| <span data-ttu-id="31dce-843">::public static int canLoad(str filename)</span><span class="sxs-lookup"><span data-stu-id="31dce-843">::public static int canLoad(str filename)</span></span>                                                                   | <span data-ttu-id="31dce-844">画像ファイルが存在し、開くことができるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-844">Determines whether an image file exists and can be opened.</span></span>                                                                                    |
| <span data-ttu-id="31dce-845">::public static container loadExt(int idx)</span><span class="sxs-lookup"><span data-stu-id="31dce-845">::public static container loadExt(int idx)</span></span>                                                                  | <span data-ttu-id="31dce-846">Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-846">Retrieves a list of the extensions of the file formats that are supported by the Image class.</span></span>                                                 |
| <span data-ttu-id="31dce-847">::public static int resourceType(int resourceIdx)</span><span class="sxs-lookup"><span data-stu-id="31dce-847">::public static int resourceType(int resourceIdx)</span></span>                                                           | <span data-ttu-id="31dce-848">特定のリソースがビットマップかアイコンかを判別します。</span><span class="sxs-lookup"><span data-stu-id="31dce-848">Determines whether a particular resource is a bitmap or an icon.</span></span>                                                                              |
| <span data-ttu-id="31dce-849">::public static int rgb(int R, int G, int B)</span><span class="sxs-lookup"><span data-stu-id="31dce-849">::public static int rgb(int R, int G, int B)</span></span>                                                                | <span data-ttu-id="31dce-850">RGB 値を ARGB 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="31dce-850">Converts an RGB value to an ARGB value.</span></span>                                                                                                       |
| <span data-ttu-id="31dce-851">::public static int validResource(int id)</span><span class="sxs-lookup"><span data-stu-id="31dce-851">::public static int validResource(int id)</span></span>                                                                   | <span data-ttu-id="31dce-852">id パラメータで指定されたリソースが有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-852">Determines whether the resource specified by the id parameter is valid.</span></span>                                                                       |
| <span data-ttu-id="31dce-853">public void new(\[AnyType image\], \[int width\], \[int height\])</span><span class="sxs-lookup"><span data-stu-id="31dce-853">public void new(\[AnyType image\], \[int width\], \[int height\])</span></span>                                           | <span data-ttu-id="31dce-854">新しい画像を作成します</span><span class="sxs-lookup"><span data-stu-id="31dce-854">Creates a new image.</span></span>                                                                                                                          |
| <span data-ttu-id="31dce-855">public void displayOrign(int Xpos, int Ypos)</span><span class="sxs-lookup"><span data-stu-id="31dce-855">public void displayOrign(int Xpos, int Ypos)</span></span>                                                                | <span data-ttu-id="31dce-856">オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="31dce-856">Enables you to specify an offset (X, Y) from the original origin (0, 0).</span></span>                                                                      |
| <span data-ttu-id="31dce-857">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-857">public void finalize()</span></span>                                                                                      |                                                                                                                                               |

### <a name="method-capturescreen"></a><span data-ttu-id="31dce-858">メソッド captureScreen</span><span class="sxs-lookup"><span data-stu-id="31dce-858">Method captureScreen</span></span>

<span data-ttu-id="31dce-859">パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="31dce-859">Captures an image from the screen by using the coordinates that are supplied in the parameter list.</span></span>

    public int captureScreen(int left, int top, int right, int bottom)

#### <a name="parameters"></a><span data-ttu-id="31dce-860">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-860">Parameters</span></span>

<span data-ttu-id="31dce-861">left</span><span class="sxs-lookup"><span data-stu-id="31dce-861">left</span></span>  
<span data-ttu-id="31dce-862">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="31dce-862">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

<!-- -->

<span data-ttu-id="31dce-863">戻る</span><span class="sxs-lookup"><span data-stu-id="31dce-863">top</span></span>  
<span data-ttu-id="31dce-864">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="31dce-864">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

<!-- -->

<span data-ttu-id="31dce-865">権限</span><span class="sxs-lookup"><span data-stu-id="31dce-865">right</span></span>  
<span data-ttu-id="31dce-866">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="31dce-866">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

<!-- -->

<span data-ttu-id="31dce-867">bottom</span><span class="sxs-lookup"><span data-stu-id="31dce-867">bottom</span></span>  
<span data-ttu-id="31dce-868">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="31dce-868">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-869">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-869">Return Value</span></span>

<span data-ttu-id="31dce-870">0 は、成功を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-870">0 indicates success.</span></span> <span data-ttu-id="31dce-871">その他の値はエラーを示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-871">Other values indicate failure.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-872">例</span><span class="sxs-lookup"><span data-stu-id="31dce-872">Examples</span></span>

<span data-ttu-id="31dce-873">次の例では、画面の一部をキャプチャし、test.bmp という名前のファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="31dce-873">The following example captures a part of the screen and saves it to a file that is named test.bmp.</span></span>

    Image img = new Image(); 
    img.captureScreen(0, 0, 100, 100); 
    img.saveFile(@'C:\test.bmp');

### <a name="method-capturewindow"></a><span data-ttu-id="31dce-874">メソッド captureWindow</span><span class="sxs-lookup"><span data-stu-id="31dce-874">Method captureWindow</span></span>

<span data-ttu-id="31dce-875">パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="31dce-875">Captures a window as an image, using the handle that is supplied as a parameter.</span></span>

    public int captureWindow(int hWnd)

#### <a name="parameters"></a><span data-ttu-id="31dce-876">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-876">Parameters</span></span>

<span data-ttu-id="31dce-877">hWnd</span><span class="sxs-lookup"><span data-stu-id="31dce-877">hWnd</span></span>  
<span data-ttu-id="31dce-878">キャプチャするウィンドウのハンドル。整数として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-878">The handle to the window that you want to capture which must be supplied as an integer.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-879">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-879">Return Value</span></span>

<span data-ttu-id="31dce-880">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-880">0 indicates success; otherwise, failure.</span></span>

### <a name="method-clipboardcopy"></a><span data-ttu-id="31dce-881">メソッド clipboardCopy</span><span class="sxs-lookup"><span data-stu-id="31dce-881">Method clipboardCopy</span></span>

<span data-ttu-id="31dce-882">イメージをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="31dce-882">Copies an image to the clipboard.</span></span>

    public int clipboardCopy()

#### <a name="return-value"></a><span data-ttu-id="31dce-883">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-883">Return Value</span></span>

<span data-ttu-id="31dce-884">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-884">0 indicates success; otherwise, failure.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-885">例</span><span class="sxs-lookup"><span data-stu-id="31dce-885">Examples</span></span>

<span data-ttu-id="31dce-886">次の例では、Test.bmp という名前のファイルからコンテンツをコピーします。</span><span class="sxs-lookup"><span data-stu-id="31dce-886">The following example copies the content from a file that is named Test.bmp.</span></span>

    Image img = new Image(); 
    img.loadFile(@'C:\Test.bmp'); 
    img.clipboardCopy(); 
    // Image can now be pasted into an application.

### <a name="method-clipboardpaste"></a><span data-ttu-id="31dce-887">メソッド clipboardPaste</span><span class="sxs-lookup"><span data-stu-id="31dce-887">Method clipboardPaste</span></span>

<span data-ttu-id="31dce-888">システムのクリップボードの内容で既存のイメージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="31dce-888">Overwrites an existing image with the content of the system clipboard.</span></span>

    public int clipboardPaste()

#### <a name="return-value"></a><span data-ttu-id="31dce-889">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-889">Return Value</span></span>

<span data-ttu-id="31dce-890">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-890">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-891">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-891">Remarks</span></span>

<span data-ttu-id="31dce-892">正常に使用されるメソッドについては、クリップボードにコンテンツが必要です。</span><span class="sxs-lookup"><span data-stu-id="31dce-892">For the method to be used successfully, the clipboard must have content.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-893">例</span><span class="sxs-lookup"><span data-stu-id="31dce-893">Examples</span></span>

<span data-ttu-id="31dce-894">次の例では、以前にクリップボードにコピーされたコンテンツを使用して新しいイメージ ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-894">The following example creates a new image file by using contents previously copied to the clipboard.</span></span>

    Image img = new Image();
    // Copy an image to the clipboard before this test 
    img.clipboardPaste(); 
    img.saveFile(@'C:\test.jpg');

### <a name="method-copyimage"></a><span data-ttu-id="31dce-895">メソッド copyImage</span><span class="sxs-lookup"><span data-stu-id="31dce-895">Method copyImage</span></span>

<span data-ttu-id="31dce-896">現在のイメージ オブジェクトをコピーします。</span><span class="sxs-lookup"><span data-stu-id="31dce-896">Copies the current image object.</span></span>

    public int copyImage(Image image)

#### <a name="parameters"></a><span data-ttu-id="31dce-897">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-897">Parameters</span></span>

<span data-ttu-id="31dce-898">image</span><span class="sxs-lookup"><span data-stu-id="31dce-898">image</span></span>  
<span data-ttu-id="31dce-899">コピーする画像。</span><span class="sxs-lookup"><span data-stu-id="31dce-899">The image to be copied.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-900">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-900">Return Value</span></span>

<span data-ttu-id="31dce-901">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-901">0 indicates success; otherwise, failure.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-902">例</span><span class="sxs-lookup"><span data-stu-id="31dce-902">Examples</span></span>

<span data-ttu-id="31dce-903">次の例では、2 つの新しいイメージを作成し、1 つのイメージの内容をもう一方のイメージの内容で上書きします。</span><span class="sxs-lookup"><span data-stu-id="31dce-903">The following example creates two new images and then overwrites the contents of one image with the contents of the other.</span></span>

    Image img =  new Image(); 
    Image img2 = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    img2.loadFile(@'C:\test2.bmp'); 
    img2.copyImage(img); //img2 now the same as img

### <a name="method-createimage"></a><span data-ttu-id="31dce-904">メソッド createImage</span><span class="sxs-lookup"><span data-stu-id="31dce-904">Method createImage</span></span>

<span data-ttu-id="31dce-905">パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-905">Creates an empty bitmap image with the width, height, and color depth as specified by the parameters.</span></span>

    public int createImage(int Width, int Height, int BitsPerPixel)

#### <a name="parameters"></a><span data-ttu-id="31dce-906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-906">Parameters</span></span>

<span data-ttu-id="31dce-907">幅</span><span class="sxs-lookup"><span data-stu-id="31dce-907">Width</span></span>  
<span data-ttu-id="31dce-908">画像の色深度。</span><span class="sxs-lookup"><span data-stu-id="31dce-908">The color depth of the image.</span></span> <span data-ttu-id="31dce-909">有効値は 1、4、8、16、24、32 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-909">Possible values are 1, 4, 8, 16, 24, and 32.</span></span>

<!-- -->

<span data-ttu-id="31dce-910">高さ</span><span class="sxs-lookup"><span data-stu-id="31dce-910">Height</span></span>  
<span data-ttu-id="31dce-911">画像の色深度。</span><span class="sxs-lookup"><span data-stu-id="31dce-911">The color depth of the image.</span></span> <span data-ttu-id="31dce-912">有効値は 1、4、8、16、24、32 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-912">Possible values are 1, 4, 8, 16, 24, and 32.</span></span>

<!-- -->

<span data-ttu-id="31dce-913">BitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="31dce-913">BitsPerPixel</span></span>  
<span data-ttu-id="31dce-914">画像の色深度。</span><span class="sxs-lookup"><span data-stu-id="31dce-914">The color depth of the image.</span></span> <span data-ttu-id="31dce-915">有効値は 1、4、8、16、24、32 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-915">Possible values are 1, 4, 8, 16, 24, and 32.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-916">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-916">Return Value</span></span>

<span data-ttu-id="31dce-917">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-917">0 indicates success; otherwise, failure.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-918">例</span><span class="sxs-lookup"><span data-stu-id="31dce-918">Examples</span></span>

<span data-ttu-id="31dce-919">次の例では、高さと幅が 16 ピクセル、色深度がピクセルあたり 32 ビットのイメージを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-919">The following example creates an image with a height and width of 16 pixels, and a color depth of 32 bits per pixel.</span></span>

    int i;
    int j;
    Image image;
    image.createImage(
        Imagelist::smallIconWidth(),
        Imagelist::smallIconHeight(),
        32);
    for (i=0; i < Imagelist::smallIconWidth(); i++)
    {
        for (j=0; j < Imagelist::smallIconHeight(); j++)
        {
            if (i >= Imagelist::smallIconWidth()-2)
            {
                image.setPixel(i, j, WinAPI::RGB2int(0, 255, 255));
            }
            else
            {
                image.setPixel(i, j, WinAPI::imageTransparentColor());
            }
        }
    }

### <a name="method-crop"></a><span data-ttu-id="31dce-920">メソッド crop</span><span class="sxs-lookup"><span data-stu-id="31dce-920">Method crop</span></span>

<span data-ttu-id="31dce-921">画像をトリミングします。</span><span class="sxs-lookup"><span data-stu-id="31dce-921">Crops the image.</span></span>

    public int crop(int x, int y, int w, int h)

#### <a name="parameters"></a><span data-ttu-id="31dce-922">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-922">Parameters</span></span>

<span data-ttu-id="31dce-923">x</span><span class="sxs-lookup"><span data-stu-id="31dce-923">x</span></span>  
<span data-ttu-id="31dce-924">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="31dce-924">The height of the region that you want to crop from the point (x, y).</span></span>

<!-- -->

<span data-ttu-id="31dce-925">y</span><span class="sxs-lookup"><span data-stu-id="31dce-925">y</span></span>  
<span data-ttu-id="31dce-926">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="31dce-926">The height of the region that you want to crop from the point (x, y).</span></span>

<!-- -->

<span data-ttu-id="31dce-927">w</span><span class="sxs-lookup"><span data-stu-id="31dce-927">w</span></span>  
<span data-ttu-id="31dce-928">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="31dce-928">The height of the region that you want to crop from the point (x, y).</span></span>

<!-- -->

<span data-ttu-id="31dce-929">h</span><span class="sxs-lookup"><span data-stu-id="31dce-929">h</span></span>  
<span data-ttu-id="31dce-930">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="31dce-930">The height of the region that you want to crop from the point (x, y).</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-931">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-931">Return Value</span></span>

<span data-ttu-id="31dce-932">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-932">0 indicates success; otherwise, failure.</span></span>

### <a name="method-displayimage"></a><span data-ttu-id="31dce-933">メソッド displayImage</span><span class="sxs-lookup"><span data-stu-id="31dce-933">Method displayImage</span></span>

<span data-ttu-id="31dce-934">HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。</span><span class="sxs-lookup"><span data-stu-id="31dce-934">Draws an image with the device context specified by the HDC parameter.</span></span>

    public int displayImage(Int64 HDC, [int Mode], [int Xpos], [int Ypos], [int Width], [int Height])

#### <a name="parameters"></a><span data-ttu-id="31dce-935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-935">Parameters</span></span>

<span data-ttu-id="31dce-936">HDC</span><span class="sxs-lookup"><span data-stu-id="31dce-936">HDC</span></span>  
<span data-ttu-id="31dce-937">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="31dce-937">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="31dce-938">モード</span><span class="sxs-lookup"><span data-stu-id="31dce-938">Mode</span></span>  
<span data-ttu-id="31dce-939">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="31dce-939">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="31dce-940">Xpos</span><span class="sxs-lookup"><span data-stu-id="31dce-940">Xpos</span></span>  
<span data-ttu-id="31dce-941">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="31dce-941">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="31dce-942">Ypos</span><span class="sxs-lookup"><span data-stu-id="31dce-942">Ypos</span></span>  
<span data-ttu-id="31dce-943">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="31dce-943">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="31dce-944">幅</span><span class="sxs-lookup"><span data-stu-id="31dce-944">Width</span></span>  
<span data-ttu-id="31dce-945">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="31dce-945">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="31dce-946">高さ</span><span class="sxs-lookup"><span data-stu-id="31dce-946">Height</span></span>  
<span data-ttu-id="31dce-947">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="31dce-947">Optional parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-948">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-948">Return Value</span></span>

<span data-ttu-id="31dce-949">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-949">0 indicates success; otherwise, failure.</span></span>

### <a name="method-exportbitmap"></a><span data-ttu-id="31dce-950">メソッド exportBitmap</span><span class="sxs-lookup"><span data-stu-id="31dce-950">Method exportBitmap</span></span>

<span data-ttu-id="31dce-951">画像のハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-951">Gets a handle for the image.</span></span>

    public Int64 exportBitmap()

#### <a name="return-value"></a><span data-ttu-id="31dce-952">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-952">Return Value</span></span>

<span data-ttu-id="31dce-953">画像のハンドル を表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-953">An integer that represents the handle for the image.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-954">例</span><span class="sxs-lookup"><span data-stu-id="31dce-954">Examples</span></span>

<span data-ttu-id="31dce-955">次の例では、イメージのハンドルを取得し、ハンドルを使用してイメージを複製します。</span><span class="sxs-lookup"><span data-stu-id="31dce-955">The following example retrieves the handle for an image and then uses the handle to clone the image.</span></span>

    { 
        int hdlBitmap; 
        Image img = new Image(); 
        Image img2 = new Image(); 
        img.loadImage(@'C:\MyImage.bmp'); 
        //Set hdlBitmap to handle for MyImage.bmp 
        hdlBitmap = img.exportBitmap(); 
        //Load MyImage.bmp to img2 using image handle 
        if (hdlBitmap) 
        { 
            img2.importBitmap(hdlBitmap); 
        } 
    }

### <a name="method-flip"></a><span data-ttu-id="31dce-956">メソッド flip</span><span class="sxs-lookup"><span data-stu-id="31dce-956">Method flip</span></span>

<span data-ttu-id="31dce-957">画像を垂直または水平方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-957">Rotates the image 180 degrees in a vertical or horizontal direction.</span></span>

    public int flip(FlipType FlipType)

#### <a name="parameters"></a><span data-ttu-id="31dce-958">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-958">Parameters</span></span>

<span data-ttu-id="31dce-959">FlipType</span><span class="sxs-lookup"><span data-stu-id="31dce-959">FlipType</span></span>  
<span data-ttu-id="31dce-960">イメージを反転させる方法を決定する FlipType 列挙。</span><span class="sxs-lookup"><span data-stu-id="31dce-960">A FlipType enumeration that determines the way in which the image is flipped.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-961">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-961">Return Value</span></span>

<span data-ttu-id="31dce-962">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-962">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-963">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-963">Remarks</span></span>

<span data-ttu-id="31dce-964">FlipType パラメーターの使用可能な値は FlipType システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="31dce-964">The possible values for the FlipType parameter are those available in the FlipType system enum:</span></span>

|     |                    |                                                          |
|-----|--------------------|----------------------------------------------------------|
| <span data-ttu-id="31dce-965">0</span><span class="sxs-lookup"><span data-stu-id="31dce-965">0</span></span>   | <span data-ttu-id="31dce-966">RotateNoneFlipNone</span><span class="sxs-lookup"><span data-stu-id="31dce-966">RotateNoneFlipNone</span></span> | <span data-ttu-id="31dce-967">反転なし</span><span class="sxs-lookup"><span data-stu-id="31dce-967">No flip</span></span>                                                  |
| <span data-ttu-id="31dce-968">1</span><span class="sxs-lookup"><span data-stu-id="31dce-968">1</span></span>   | <span data-ttu-id="31dce-969">RotateNoneFlipX</span><span class="sxs-lookup"><span data-stu-id="31dce-969">RotateNoneFlipX</span></span>    | <span data-ttu-id="31dce-970">画像を水平方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-970">Rotates the image 180 degrees in a horizontal direction.</span></span> |
| <span data-ttu-id="31dce-971">2</span><span class="sxs-lookup"><span data-stu-id="31dce-971">2</span></span>   | <span data-ttu-id="31dce-972">RotateNoneFlipX</span><span class="sxs-lookup"><span data-stu-id="31dce-972">RotateNoneFlipY</span></span>    | <span data-ttu-id="31dce-973">画像を垂直方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-973">Rotates the image 180 degrees in a vertical direction.</span></span>   |

### <a name="method-getimagedimensionunits"></a><span data-ttu-id="31dce-974">メソッド getImageDimensionUnits</span><span class="sxs-lookup"><span data-stu-id="31dce-974">Method getImageDimensionUnits</span></span>

    public container getImageDimensionUnits()

#### <a name="return-value"></a><span data-ttu-id="31dce-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-975">Return Value</span></span>

### <a name="method-getpixel"></a><span data-ttu-id="31dce-976">メソッド getPixel</span><span class="sxs-lookup"><span data-stu-id="31dce-976">Method getPixel</span></span>

<span data-ttu-id="31dce-977">パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-977">Retrieves the ARGB color value of the pixel at the point that is specified by the parameters.</span></span>

    public int getPixel(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="31dce-978">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-978">Parameters</span></span>

<span data-ttu-id="31dce-979">x</span><span class="sxs-lookup"><span data-stu-id="31dce-979">x</span></span>  
<span data-ttu-id="31dce-980">ピクセルの垂直座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-980">The vertical coordinate of the pixel.</span></span>

<!-- -->

<span data-ttu-id="31dce-981">y</span><span class="sxs-lookup"><span data-stu-id="31dce-981">y</span></span>  
<span data-ttu-id="31dce-982">ピクセルの垂直座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-982">The vertical coordinate of the pixel.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-983">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-983">Return Value</span></span>

<span data-ttu-id="31dce-984">ピクセルの ARGB 値である整数 (RGB カラーの 32 ビット表示) 。</span><span class="sxs-lookup"><span data-stu-id="31dce-984">An integer that is the ARGB value of the pixel (a 32-bit representation of an RGB color).</span></span>

### <a name="method-height"></a><span data-ttu-id="31dce-985">メソッド height</span><span class="sxs-lookup"><span data-stu-id="31dce-985">Method height</span></span>

<span data-ttu-id="31dce-986">ピクセル単位の画像の高さを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-986">Retrieves the height of the image in pixels.</span></span>

    public int height()

#### <a name="return-value"></a><span data-ttu-id="31dce-987">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-987">Return Value</span></span>

<span data-ttu-id="31dce-988">画像の高さをピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-988">An integer that represents the height of the image in pixels.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-989">例</span><span class="sxs-lookup"><span data-stu-id="31dce-989">Examples</span></span>

<span data-ttu-id="31dce-990">次の例では、test.bmp に含まれるイメージの高さを出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-990">The following example prints out the height of the image that is contained in test.bmp.</span></span>

    Image img = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    print img.height(); 
    pause;

### <a name="method-imageinfo"></a><span data-ttu-id="31dce-991">メソッド imageInfo</span><span class="sxs-lookup"><span data-stu-id="31dce-991">Method imageInfo</span></span>

<span data-ttu-id="31dce-992">画像の幅、高さ、色深度を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-992">Retrieves the width, height, and color depth of the image.</span></span>

    public container imageInfo()

#### <a name="return-value"></a><span data-ttu-id="31dce-993">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-993">Return Value</span></span>

<span data-ttu-id="31dce-994">画像の幅、画像の高さ、およびピクセルあたりのビット数を指定する値を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="31dce-994">A container that holds values that specify the width of the image, the height of the image, and the number of bits per pixel.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-995">例</span><span class="sxs-lookup"><span data-stu-id="31dce-995">Examples</span></span>

<span data-ttu-id="31dce-996">次の例では、イメージ test.bmp の幅と高さを出力し、ピクセルあたりのビット数で色深度を指定しています。</span><span class="sxs-lookup"><span data-stu-id="31dce-996">The following example prints out the width and height of the image test.bmp, and specifies the color depth in bits per pixel.</span></span>

    Image img = new Image(); 
    container c; 
    img.loadFile(@'C:\Test.bmp'); 
    c = img.imageInfo(); 
    print con2str(c); 
    pause;

### <a name="method-imagespotlight"></a><span data-ttu-id="31dce-997">メソッド imageSpotlight</span><span class="sxs-lookup"><span data-stu-id="31dce-997">Method imageSpotlight</span></span>

<span data-ttu-id="31dce-998">センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-998">Produces a spotlight effect within the circle that is defined by radius with center coordinates x and y.</span></span>

    public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)

#### <a name="parameters"></a><span data-ttu-id="31dce-999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-999">Parameters</span></span>

<span data-ttu-id="31dce-1000">x</span><span class="sxs-lookup"><span data-stu-id="31dce-1000">x</span></span>  
<span data-ttu-id="31dce-1001">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="31dce-1001">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="31dce-1002">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1002">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="31dce-1003">y</span><span class="sxs-lookup"><span data-stu-id="31dce-1003">y</span></span>  
<span data-ttu-id="31dce-1004">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="31dce-1004">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="31dce-1005">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1005">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="31dce-1006">radius</span><span class="sxs-lookup"><span data-stu-id="31dce-1006">radius</span></span>  
<span data-ttu-id="31dce-1007">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="31dce-1007">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="31dce-1008">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1008">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="31dce-1009">平滑化</span><span class="sxs-lookup"><span data-stu-id="31dce-1009">smoothing</span></span>  
<span data-ttu-id="31dce-1010">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="31dce-1010">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="31dce-1011">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1011">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="31dce-1012">intensity</span><span class="sxs-lookup"><span data-stu-id="31dce-1012">intensity</span></span>  
<span data-ttu-id="31dce-1013">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="31dce-1013">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="31dce-1014">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1014">The possible values are between 0 and 100 (%).</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1015">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1015">Return Value</span></span>

<span data-ttu-id="31dce-1016">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1016">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1017">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1017">Remarks</span></span>

<span data-ttu-id="31dce-1018">円内のピクセルは変更されませんが、イメージ内の他のピクセルはその明度を減らすことで暗くなります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1018">The pixels within the circle are unchanged, but the other pixels in the image are darkened by reducing their intensity.</span></span>

### <a name="method-importbitmap"></a><span data-ttu-id="31dce-1019">メソッド importBitmap</span><span class="sxs-lookup"><span data-stu-id="31dce-1019">Method importBitmap</span></span>

<span data-ttu-id="31dce-1020">hBitmap パラメータで指定されたイメージからビットマップをクローンします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1020">Clones a bitmap from the image that is specified by the hBitmap parameter.</span></span>

    public int importBitmap(Int64 hBitmap)

#### <a name="parameters"></a><span data-ttu-id="31dce-1021">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1021">Parameters</span></span>

<span data-ttu-id="31dce-1022">hBitmap</span><span class="sxs-lookup"><span data-stu-id="31dce-1022">hBitmap</span></span>  
<span data-ttu-id="31dce-1023">複製する画像のハンドルです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1023">The handle to the image that you clone.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1024">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1024">Return Value</span></span>

<span data-ttu-id="31dce-1025">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1025">0 indicates success; otherwise, failure.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1026">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1026">Examples</span></span>

<span data-ttu-id="31dce-1027">次の例では、イメージのハンドルを取得してから、importBitmap メソッドを使用してイメージを複製します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1027">The following example retrieves the handle for an image and then uses the importBitmap method to clone the image.</span></span>

    { 
        int hdlBitmap; 
        Image img = new Image(); 
        Image img2 = new Image(); 
        img.loadImage(@'C:\MyImage.bmp'); 
        //Set hdlBitmap to handle for MyImage.bmp 
        hdlBitmap = img.exportBitmap(); 
        //Load MyImage.bmp to img2 using image handle 
        if (hdlBitmap) 
        { 
            img2.importBitmap(hdlBitmap); 
        } 
    }

### <a name="method-importfileicon"></a><span data-ttu-id="31dce-1028">メソッド importFileIcon</span><span class="sxs-lookup"><span data-stu-id="31dce-1028">Method importFileIcon</span></span>

<span data-ttu-id="31dce-1029">ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1029">Creates an icon from the file specified by the fileName parameter by copying the icon that is used for the file.</span></span>

    public int importFileIcon(str fileName)

#### <a name="parameters"></a><span data-ttu-id="31dce-1030">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1030">Parameters</span></span>

<span data-ttu-id="31dce-1031">fileName</span><span class="sxs-lookup"><span data-stu-id="31dce-1031">fileName</span></span>  
<span data-ttu-id="31dce-1032">アイコンを作成するファイルの名前とパス。</span><span class="sxs-lookup"><span data-stu-id="31dce-1032">The name and the path of the file from which you create an icon.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1033">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1033">Return Value</span></span>

<span data-ttu-id="31dce-1034">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1034">0 indicates success; otherwise, failure.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1035">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1035">Examples</span></span>

<span data-ttu-id="31dce-1036">次の例では、ファイル test.bmp に使用されているアイコンをコピーします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1036">The following example copies the icon that is used for the file test.bmp.</span></span>

    Image img = new Image(); 
    img.importFileIcon(@'C:\test.bmp'); 
    img.clipboardCopy(); 
    // Icon used for test.bmp can now be pasted into an application.

### <a name="method-importicon"></a><span data-ttu-id="31dce-1037">メソッド importIcon</span><span class="sxs-lookup"><span data-stu-id="31dce-1037">Method importIcon</span></span>

<span data-ttu-id="31dce-1038">Finance and Operations の実行可能ファイルからアイコンへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1038">Retrieves a handle to an icon from an executable file in Finance and Operations.</span></span> <span data-ttu-id="31dce-1039">このアイコンは、fileName および iconIdx パラメーターで指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1039">The icon is specified by the fileName and iconIdx parameters.</span></span>

    public int importIcon(str fileName, int iconIdx)

#### <a name="parameters"></a><span data-ttu-id="31dce-1040">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1040">Parameters</span></span>

<span data-ttu-id="31dce-1041">fileName</span><span class="sxs-lookup"><span data-stu-id="31dce-1041">fileName</span></span>  
<span data-ttu-id="31dce-1042">指定したファイル内のリソース。</span><span class="sxs-lookup"><span data-stu-id="31dce-1042">The resource within the specified file.</span></span>

<!-- -->

<span data-ttu-id="31dce-1043">iconIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1043">iconIdx</span></span>  
<span data-ttu-id="31dce-1044">指定したファイル内のリソース。</span><span class="sxs-lookup"><span data-stu-id="31dce-1044">The resource within the specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1045">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1045">Return Value</span></span>

<span data-ttu-id="31dce-1046">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1046">0 indicates success; otherwise, failure.</span></span>

### <a name="method-loadimage"></a><span data-ttu-id="31dce-1047">メソッド loadImage</span><span class="sxs-lookup"><span data-stu-id="31dce-1047">Method loadImage</span></span>

<span data-ttu-id="31dce-1048">fileName パラメーターで指定されたファイルからイメージを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1048">Loads an image from the file specified by the fileName parameter.</span></span>

    public int loadImage(str fileName)

#### <a name="parameters"></a><span data-ttu-id="31dce-1049">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1049">Parameters</span></span>

<span data-ttu-id="31dce-1050">fileName</span><span class="sxs-lookup"><span data-stu-id="31dce-1050">fileName</span></span>  
<span data-ttu-id="31dce-1051">画像を読み込む元となるリソース。</span><span class="sxs-lookup"><span data-stu-id="31dce-1051">The resource from which you want to load the image.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1052">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1052">Return Value</span></span>

<span data-ttu-id="31dce-1053">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1053">0 indicates success; otherwise, failure.</span></span>

### <a name="method-loadresource"></a><span data-ttu-id="31dce-1054">メソッド loadResource</span><span class="sxs-lookup"><span data-stu-id="31dce-1054">Method loadResource</span></span>

<span data-ttu-id="31dce-1055">Ax32.exe からリソースを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1055">Loads a resource from Ax32.exe.</span></span>

    public int loadResource(int id)

#### <a name="parameters"></a><span data-ttu-id="31dce-1056">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1056">Parameters</span></span>

<span data-ttu-id="31dce-1057">id</span><span class="sxs-lookup"><span data-stu-id="31dce-1057">id</span></span>  
<span data-ttu-id="31dce-1058">読み込むリソースの ID。</span><span class="sxs-lookup"><span data-stu-id="31dce-1058">The ID of the resource that you want to load.</span></span> <span data-ttu-id="31dce-1059">リソースの値は、Resources マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1059">Values of resources can be found in the Resources macro.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1060">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1060">Return Value</span></span>

<span data-ttu-id="31dce-1061">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1061">0 indicates success; otherwise, failure.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1062">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1062">Examples</span></span>

<span data-ttu-id="31dce-1063">次の例では、イメージ リストに 2つ のリソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1063">The following example adds two resources to an image list.</span></span>

    #Resource 
    Image img; 
    ImageList imageList; 
    imageList = new Imagelist( 
        Imagelist::smallIconWidth(), 
        Imagelist::smallIconHeight()); 
    img = new Image(); 
    img.loadResource(#RES_NODE_CLOSED); 
    imageList.add(img); 
    img = new Image(); 
    img.loadResource(#RES_NODE_OPEN); 
    imageList.add(img);

### <a name="method-promotecolor"></a><span data-ttu-id="31dce-1064">メソッド promoteColor</span><span class="sxs-lookup"><span data-stu-id="31dce-1064">Method promoteColor</span></span>

<span data-ttu-id="31dce-1065">画像の色深度を向上させます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1065">Increases the color depth of the image.</span></span>

    public int promoteColor(int noOfColorBits)

#### <a name="parameters"></a><span data-ttu-id="31dce-1066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1066">Parameters</span></span>

<span data-ttu-id="31dce-1067">noOfColorBits</span><span class="sxs-lookup"><span data-stu-id="31dce-1067">noOfColorBits</span></span>  
<span data-ttu-id="31dce-1068">イメージのレベルを上げるビット数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1068">The number of bits that you want to promote the image to.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1069">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1069">Return Value</span></span>

<span data-ttu-id="31dce-1070">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1070">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1071">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1071">Remarks</span></span>

<span data-ttu-id="31dce-1072">このメソッドは次を推進します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1072">The method promotes:</span></span>

-   <span data-ttu-id="31dce-1073">8 ビット画像を 24、32 ビットに。</span><span class="sxs-lookup"><span data-stu-id="31dce-1073">8-bit images to 24 or 32 bits.</span></span>
-   <span data-ttu-id="31dce-1074">4 ビット画像を 8、24、32 ビットに。</span><span class="sxs-lookup"><span data-stu-id="31dce-1074">4-bit images to 8, 24, or 32 bits.</span></span>
-   <span data-ttu-id="31dce-1075">1 ビット画像を 4、8、24、32 ビットに。</span><span class="sxs-lookup"><span data-stu-id="31dce-1075">1-bit images to 4, 8, 24, or 32 bits.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1076">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1076">Examples</span></span>

<span data-ttu-id="31dce-1077">次の例では、イメージの色深度が 8 ビット以上でない場合は、ピクセルあたり 8 ビットに増やしています。</span><span class="sxs-lookup"><span data-stu-id="31dce-1077">The following example increases the color depth of an image to 8 bits per pixel, unless it is already 8 or more.</span></span>

    Image img = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    if (conpeek(img.imageInfo(),3) <8) 
    { 
        img.promoteColor(8); 
    }

### <a name="method-reducecoloroctree"></a><span data-ttu-id="31dce-1078">メソッド reduceColorOctree</span><span class="sxs-lookup"><span data-stu-id="31dce-1078">Method reduceColorOctree</span></span>

<span data-ttu-id="31dce-1079">画像の色深度を減少させます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1079">Reduces the color depth of an image.</span></span>

    public int reduceColorOctree(int maxColors)

#### <a name="parameters"></a><span data-ttu-id="31dce-1080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1080">Parameters</span></span>

<span data-ttu-id="31dce-1081">maxColors</span><span class="sxs-lookup"><span data-stu-id="31dce-1081">maxColors</span></span>  
<span data-ttu-id="31dce-1082">最大色数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1082">The maximum number of colors.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1083">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1083">Return Value</span></span>

<span data-ttu-id="31dce-1084">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1084">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1085">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1085">Remarks</span></span>

<span data-ttu-id="31dce-1086">このメソッドは、他の指示が maxColors パラメーターで指定されていない限り、24 ビット イメージを 8 ビットに、または 8 ビット イメージを 4 ビットに縮小します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1086">The method reduces a 24-bit image to 8 bits, or an 8-bit image to 4 bits, unless other instructions are specified in the maxColors parameter.</span></span> <span data-ttu-id="31dce-1087">MaxColors パラメーターが 16 以下の場合は、4 ビット イメージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1087">If the maxColors parameter is less than or equal to 16, a 4-bit image is produced.</span></span> <span data-ttu-id="31dce-1088">MaxColors が 16 を超える場合は、8 ビット画像が生成されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1088">If maxColors is more than 16, an 8-bit image is produced.</span></span>

### <a name="method-removeimage"></a><span data-ttu-id="31dce-1089">メソッド removeImage</span><span class="sxs-lookup"><span data-stu-id="31dce-1089">Method removeImage</span></span>

<span data-ttu-id="31dce-1090">画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1090">Removes the data about an image; the object still exists, but has no data.</span></span>

    public int removeImage()

#### <a name="return-value"></a><span data-ttu-id="31dce-1091">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1091">Return Value</span></span>

<span data-ttu-id="31dce-1092">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1092">0 indicates success; otherwise, failure.</span></span>

### <a name="method-resize"></a><span data-ttu-id="31dce-1093">メソッド resize</span><span class="sxs-lookup"><span data-stu-id="31dce-1093">Method resize</span></span>

<span data-ttu-id="31dce-1094">newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1094">Resizes the image to the size that is specified by the newWidth and newHeight parameters.</span></span>

    public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)

#### <a name="parameters"></a><span data-ttu-id="31dce-1095">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1095">Parameters</span></span>

<span data-ttu-id="31dce-1096">newWidth</span><span class="sxs-lookup"><span data-stu-id="31dce-1096">newWidth</span></span>  
<span data-ttu-id="31dce-1097">resizing メソッド。</span><span class="sxs-lookup"><span data-stu-id="31dce-1097">The resizing method.</span></span>

<!-- -->

<span data-ttu-id="31dce-1098">newHeight</span><span class="sxs-lookup"><span data-stu-id="31dce-1098">newHeight</span></span>  
<span data-ttu-id="31dce-1099">resizing メソッド。</span><span class="sxs-lookup"><span data-stu-id="31dce-1099">The resizing method.</span></span>

<!-- -->

<span data-ttu-id="31dce-1100">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="31dce-1100">InterpolationMode</span></span>  
<span data-ttu-id="31dce-1101">resizing メソッド。</span><span class="sxs-lookup"><span data-stu-id="31dce-1101">The resizing method.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1102">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1102">Return Value</span></span>

<span data-ttu-id="31dce-1103">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1103">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1104">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1104">Remarks</span></span>

<span data-ttu-id="31dce-1105">InterpolationMode パラメーターの使用可能な値は InterpolationMode システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1105">The possible values for the InterpolationMode parameter are those available in the InterpolationMode system enum:</span></span>

|     |                                      |                                                                                                                                                                        |
|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-1106">0</span><span class="sxs-lookup"><span data-stu-id="31dce-1106">0</span></span>   | <span data-ttu-id="31dce-1107">InterpolationModeDefault</span><span class="sxs-lookup"><span data-stu-id="31dce-1107">InterpolationModeDefault</span></span>             | <span data-ttu-id="31dce-1108">既定の補間モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1108">Specifies the default interpolation mode.</span></span>                                                                                                                              |
| <span data-ttu-id="31dce-1109">1</span><span class="sxs-lookup"><span data-stu-id="31dce-1109">1</span></span>   | <span data-ttu-id="31dce-1110">InterpolationModeLowQuality</span><span class="sxs-lookup"><span data-stu-id="31dce-1110">InterpolationModeLowQuality</span></span>          | <span data-ttu-id="31dce-1111">低品質モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1111">Specifies a low-quality mode.</span></span>                                                                                                                                          |
| <span data-ttu-id="31dce-1112">2</span><span class="sxs-lookup"><span data-stu-id="31dce-1112">2</span></span>   | <span data-ttu-id="31dce-1113">InterpolationModeHighQuality</span><span class="sxs-lookup"><span data-stu-id="31dce-1113">InterpolationModeHighQuality</span></span>         | <span data-ttu-id="31dce-1114">高品質モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1114">Specifies a high-quality mode.</span></span>                                                                                                                                         |
| <span data-ttu-id="31dce-1115">3</span><span class="sxs-lookup"><span data-stu-id="31dce-1115">3</span></span>   | <span data-ttu-id="31dce-1116">InterpolationModeBilinear</span><span class="sxs-lookup"><span data-stu-id="31dce-1116">InterpolationModeBilinear</span></span>            | <span data-ttu-id="31dce-1117">線状補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1117">Specifies bilinear interpolation.</span></span> <span data-ttu-id="31dce-1118">事前フィルター処理は行われません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1118">No pre-filtering is done.</span></span> <span data-ttu-id="31dce-1119">このメソッドは、画像を元のサイズの 50％ 以下に縮小するのには適していません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1119">This method is not suitable for shrinking an image below 50% of its original size.</span></span>                         |
| <span data-ttu-id="31dce-1120">4</span><span class="sxs-lookup"><span data-stu-id="31dce-1120">4</span></span>   | <span data-ttu-id="31dce-1121">InterpolationModeBicubic</span><span class="sxs-lookup"><span data-stu-id="31dce-1121">InterpolationModeBicubic</span></span>             | <span data-ttu-id="31dce-1122">バイキュービック補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1122">Specifies bicubic interpolation.</span></span> <span data-ttu-id="31dce-1123">事前フィルター処理は行われません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1123">No pre-filtering is done.</span></span> <span data-ttu-id="31dce-1124">このメソッドは、画像を元のサイズの 25％ 以下に縮小するのには適していません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1124">This method is not suitable for shrinking an image below 25% of its original size.</span></span>                          |
| <span data-ttu-id="31dce-1125">5</span><span class="sxs-lookup"><span data-stu-id="31dce-1125">5</span></span>   | <span data-ttu-id="31dce-1126">InterpolationModeNearestNeighbor</span><span class="sxs-lookup"><span data-stu-id="31dce-1126">InterpolationModeNearestNeighbor</span></span>     | <span data-ttu-id="31dce-1127">ニアレストネイバー補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1127">Specifies nearest-neighbor interpolation.</span></span>                                                                                                                              |
| <span data-ttu-id="31dce-1128">6</span><span class="sxs-lookup"><span data-stu-id="31dce-1128">6</span></span>   | <span data-ttu-id="31dce-1129">InterpolationModeHighQualityBilinear</span><span class="sxs-lookup"><span data-stu-id="31dce-1129">InterpolationModeHighQualityBilinear</span></span> | <span data-ttu-id="31dce-1130">高品質な線状補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1130">Specifies high-quality, bilinear interpolation.</span></span> <span data-ttu-id="31dce-1131">高品質圧縮を確実に行うため、事前フィルター処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1131">Pre-filtering is performed to ensure high-quality shrinking.</span></span>                                                           |
| <span data-ttu-id="31dce-1132">7</span><span class="sxs-lookup"><span data-stu-id="31dce-1132">7</span></span>   | <span data-ttu-id="31dce-1133">InterpolationModeHighQualityBicubic</span><span class="sxs-lookup"><span data-stu-id="31dce-1133">InterpolationModeHighQualityBicubic</span></span>  | <span data-ttu-id="31dce-1134">高品質なバイキュービック補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1134">Specifies high-quality, bicubic interpolation.</span></span> <span data-ttu-id="31dce-1135">高品質圧縮を確実に行うため、事前フィルター処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1135">Pre-filtering is performed to ensure high-quality shrinking.</span></span> <span data-ttu-id="31dce-1136">このモードでは、最高品質の変換画像が生成されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1136">This mode produces the highest quality transformed images.</span></span> |

### <a name="method-rotate"></a><span data-ttu-id="31dce-1137">メソッド rotate</span><span class="sxs-lookup"><span data-stu-id="31dce-1137">Method rotate</span></span>

<span data-ttu-id="31dce-1138">画像を回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1138">Rotates the image.</span></span>

    public int rotate(RotateType RotateType)

#### <a name="parameters"></a><span data-ttu-id="31dce-1139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1139">Parameters</span></span>

<span data-ttu-id="31dce-1140">RotateType</span><span class="sxs-lookup"><span data-stu-id="31dce-1140">RotateType</span></span>  
<span data-ttu-id="31dce-1141">イメージを回転する量。</span><span class="sxs-lookup"><span data-stu-id="31dce-1141">The amount to rotate the image by.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1142">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1142">Return Value</span></span>

<span data-ttu-id="31dce-1143">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1143">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1144">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1144">Remarks</span></span>

<span data-ttu-id="31dce-1145">RotateType パラメーターの使用可能な値は RotateType システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1145">The possible values for the RotateType parameter are those available in the RotateType system enum:</span></span>

|     |                    |                          |
|-----|--------------------|--------------------------|
| <span data-ttu-id="31dce-1146">0</span><span class="sxs-lookup"><span data-stu-id="31dce-1146">0</span></span>   | <span data-ttu-id="31dce-1147">RotateNoneFlipNone</span><span class="sxs-lookup"><span data-stu-id="31dce-1147">RotateNoneFlipNone</span></span> | <span data-ttu-id="31dce-1148">回転なし。</span><span class="sxs-lookup"><span data-stu-id="31dce-1148">No rotation.</span></span>             |
| <span data-ttu-id="31dce-1149">1</span><span class="sxs-lookup"><span data-stu-id="31dce-1149">1</span></span>   | <span data-ttu-id="31dce-1150">Rotate90FlipNone</span><span class="sxs-lookup"><span data-stu-id="31dce-1150">Rotate90FlipNone</span></span>   | <span data-ttu-id="31dce-1151">90 度回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1151">Rotation by 90 degrees.</span></span>  |
| <span data-ttu-id="31dce-1152">2</span><span class="sxs-lookup"><span data-stu-id="31dce-1152">2</span></span>   | <span data-ttu-id="31dce-1153">Rotate180FlipNone</span><span class="sxs-lookup"><span data-stu-id="31dce-1153">Rotate180FlipNone</span></span>  | <span data-ttu-id="31dce-1154">180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1154">Rotation by 180 degrees.</span></span> |
| <span data-ttu-id="31dce-1155">3</span><span class="sxs-lookup"><span data-stu-id="31dce-1155">3</span></span>   | <span data-ttu-id="31dce-1156">Rotate270FlipNone</span><span class="sxs-lookup"><span data-stu-id="31dce-1156">Rotate270FlipNone</span></span>  | <span data-ttu-id="31dce-1157">270 度回転します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1157">Rotation by 270 degrees.</span></span> |

### <a name="method-saveimage"></a><span data-ttu-id="31dce-1158">メソッド saveImage</span><span class="sxs-lookup"><span data-stu-id="31dce-1158">Method saveImage</span></span>

<span data-ttu-id="31dce-1159">指定されたファイル名に画像を保存します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1159">Saves the image to the specified file name.</span></span>

    public int saveImage(str fileName, [ImageSaveType Type])

#### <a name="parameters"></a><span data-ttu-id="31dce-1160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1160">Parameters</span></span>

<span data-ttu-id="31dce-1161">fileName</span><span class="sxs-lookup"><span data-stu-id="31dce-1161">fileName</span></span>  
<span data-ttu-id="31dce-1162">ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31dce-1162">An ImageSaveType that enables you to specify that the file should be saved as a different format from that specified by the file extension; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1163">種類</span><span class="sxs-lookup"><span data-stu-id="31dce-1163">Type</span></span>  
<span data-ttu-id="31dce-1164">ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31dce-1164">An ImageSaveType that enables you to specify that the file should be saved as a different format from that specified by the file extension; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1165">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1165">Return Value</span></span>

<span data-ttu-id="31dce-1166">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1166">0 if the method was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1167">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1167">Remarks</span></span>

<span data-ttu-id="31dce-1168">Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1168">The possible values for the Type parameter are those available in the ImageSaveType system enum.</span></span> <span data-ttu-id="31dce-1169">たとえば、.jpg ファイルとして test.bmp を保存することができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1169">For example, you could save test.bmp as a .jpg file.</span></span>

|     |                |
|-----|----------------|
| <span data-ttu-id="31dce-1170">0</span><span class="sxs-lookup"><span data-stu-id="31dce-1170">0</span></span>   | <span data-ttu-id="31dce-1171">\_エクステンションの使用</span><span class="sxs-lookup"><span data-stu-id="31dce-1171">Use\_Extension</span></span> |
| <span data-ttu-id="31dce-1172">1</span><span class="sxs-lookup"><span data-stu-id="31dce-1172">1</span></span>   | <span data-ttu-id="31dce-1173">BMP</span><span class="sxs-lookup"><span data-stu-id="31dce-1173">BMP</span></span>            |
| <span data-ttu-id="31dce-1174">2</span><span class="sxs-lookup"><span data-stu-id="31dce-1174">2</span></span>   | <span data-ttu-id="31dce-1175">GIF</span><span class="sxs-lookup"><span data-stu-id="31dce-1175">GIF</span></span>            |
| <span data-ttu-id="31dce-1176">3</span><span class="sxs-lookup"><span data-stu-id="31dce-1176">3</span></span>   | <span data-ttu-id="31dce-1177">JPG</span><span class="sxs-lookup"><span data-stu-id="31dce-1177">JPG</span></span>            |
| <span data-ttu-id="31dce-1178">4</span><span class="sxs-lookup"><span data-stu-id="31dce-1178">4</span></span>   | <span data-ttu-id="31dce-1179">PNG</span><span class="sxs-lookup"><span data-stu-id="31dce-1179">PNG</span></span>            |
| <span data-ttu-id="31dce-1180">5</span><span class="sxs-lookup"><span data-stu-id="31dce-1180">5</span></span>   | <span data-ttu-id="31dce-1181">TIFF</span><span class="sxs-lookup"><span data-stu-id="31dce-1181">TIFF</span></span>           |
| <span data-ttu-id="31dce-1182">6</span><span class="sxs-lookup"><span data-stu-id="31dce-1182">6</span></span>   | <span data-ttu-id="31dce-1183">BMP\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="31dce-1183">BMP\_UNCOMP</span></span>    |
| <span data-ttu-id="31dce-1184">7</span><span class="sxs-lookup"><span data-stu-id="31dce-1184">7</span></span>   | <span data-ttu-id="31dce-1185">TIF\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="31dce-1185">TIF\_UNCOMP</span></span>    |

#### <a name="examples"></a><span data-ttu-id="31dce-1186">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1186">Examples</span></span>

<span data-ttu-id="31dce-1187">次の例では、画面の一部をファイルにキャプチャし、その画像をロードします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1187">The following example captures part of the screen to a file, and then loads that image.</span></span>

    Image img = new Image(); 
    img.captureScreen(0, 0, 100, 100); 
    img.saveImage(@'C:\test.bmp'); 
    img.loadFile(@'C:\test.bmp');

### <a name="method-savetype"></a><span data-ttu-id="31dce-1188">メソッド saveType</span><span class="sxs-lookup"><span data-stu-id="31dce-1188">Method saveType</span></span>

<span data-ttu-id="31dce-1189">イメージ デコーダを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1189">Gets or sets the image decoder.</span></span>

    public ImageSaveType saveType([ImageSaveType Type])

#### <a name="parameters"></a><span data-ttu-id="31dce-1190">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1190">Parameters</span></span>

<span data-ttu-id="31dce-1191">種類</span><span class="sxs-lookup"><span data-stu-id="31dce-1191">Type</span></span>  
<span data-ttu-id="31dce-1192">設定するデコーダのタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31dce-1192">The type of decoder that you want to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1193">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1193">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1194">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1194">Remarks</span></span>

<span data-ttu-id="31dce-1195">Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1195">The possible values for the Type parameter are those available in the ImageSaveType system enum:</span></span>

|     |                |
|-----|----------------|
| <span data-ttu-id="31dce-1196">0</span><span class="sxs-lookup"><span data-stu-id="31dce-1196">0</span></span>   | <span data-ttu-id="31dce-1197">\_エクステンションの使用</span><span class="sxs-lookup"><span data-stu-id="31dce-1197">Use\_Extension</span></span> |
| <span data-ttu-id="31dce-1198">1</span><span class="sxs-lookup"><span data-stu-id="31dce-1198">1</span></span>   | <span data-ttu-id="31dce-1199">BMP</span><span class="sxs-lookup"><span data-stu-id="31dce-1199">BMP</span></span>            |
| <span data-ttu-id="31dce-1200">2</span><span class="sxs-lookup"><span data-stu-id="31dce-1200">2</span></span>   | <span data-ttu-id="31dce-1201">GIF</span><span class="sxs-lookup"><span data-stu-id="31dce-1201">GIF</span></span>            |
| <span data-ttu-id="31dce-1202">3</span><span class="sxs-lookup"><span data-stu-id="31dce-1202">3</span></span>   | <span data-ttu-id="31dce-1203">JPG</span><span class="sxs-lookup"><span data-stu-id="31dce-1203">JPG</span></span>            |
| <span data-ttu-id="31dce-1204">4</span><span class="sxs-lookup"><span data-stu-id="31dce-1204">4</span></span>   | <span data-ttu-id="31dce-1205">PNG</span><span class="sxs-lookup"><span data-stu-id="31dce-1205">PNG</span></span>            |
| <span data-ttu-id="31dce-1206">5</span><span class="sxs-lookup"><span data-stu-id="31dce-1206">5</span></span>   | <span data-ttu-id="31dce-1207">TIFF</span><span class="sxs-lookup"><span data-stu-id="31dce-1207">TIFF</span></span>           |
| <span data-ttu-id="31dce-1208">6</span><span class="sxs-lookup"><span data-stu-id="31dce-1208">6</span></span>   | <span data-ttu-id="31dce-1209">BMP\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="31dce-1209">BMP\_UNCOMP</span></span>    |
| <span data-ttu-id="31dce-1210">7</span><span class="sxs-lookup"><span data-stu-id="31dce-1210">7</span></span>   | <span data-ttu-id="31dce-1211">TIF\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="31dce-1211">TIF\_UNCOMP</span></span>    |

### <a name="method-setpixel"></a><span data-ttu-id="31dce-1212">メソッド setPixel</span><span class="sxs-lookup"><span data-stu-id="31dce-1212">Method setPixel</span></span>

<span data-ttu-id="31dce-1213">x と y パラメーターで指定されているピクセルの色を設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1213">Sets the color for the pixel that is specified by the x and y parameters.</span></span>

    public int setPixel(int x, int y, int pixel)

#### <a name="parameters"></a><span data-ttu-id="31dce-1214">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1214">Parameters</span></span>

<span data-ttu-id="31dce-1215">x</span><span class="sxs-lookup"><span data-stu-id="31dce-1215">x</span></span>  
<span data-ttu-id="31dce-1216">使用する色の ARGB 値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1216">The ARGB value of the color that you want to use.</span></span>

<!-- -->

<span data-ttu-id="31dce-1217">y</span><span class="sxs-lookup"><span data-stu-id="31dce-1217">y</span></span>  
<span data-ttu-id="31dce-1218">使用する色の ARGB 値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1218">The ARGB value of the color that you want to use.</span></span>

<!-- -->

<span data-ttu-id="31dce-1219">pixel</span><span class="sxs-lookup"><span data-stu-id="31dce-1219">pixel</span></span>  
<span data-ttu-id="31dce-1220">使用する色の ARGB 値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1220">The ARGB value of the color that you want to use.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1221">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1221">Return Value</span></span>

<span data-ttu-id="31dce-1222">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1222">0 indicates success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1223">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1223">Remarks</span></span>

<span data-ttu-id="31dce-1224">RGB カラー値を ARGB 値に変換するには、Image::rgb メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1224">To convert an RGB color value to an ARGB value, use the Image::rgb Method.</span></span>

### <a name="method-transparent"></a><span data-ttu-id="31dce-1225">メソッド transparent</span><span class="sxs-lookup"><span data-stu-id="31dce-1225">Method transparent</span></span>

<span data-ttu-id="31dce-1226">画像の透明な色を設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1226">Sets the transparent color for the image.</span></span>

    public int transparent([boolean Set], [int RValue], [int GValue], [int BValue])

#### <a name="parameters"></a><span data-ttu-id="31dce-1227">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1227">Parameters</span></span>

<span data-ttu-id="31dce-1228">セット</span><span class="sxs-lookup"><span data-stu-id="31dce-1228">Set</span></span>  
<span data-ttu-id="31dce-1229">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1229">Blue value of the color that you want to set; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1230">RValue</span><span class="sxs-lookup"><span data-stu-id="31dce-1230">RValue</span></span>  
<span data-ttu-id="31dce-1231">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1231">Blue value of the color that you want to set; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1232">GValue</span><span class="sxs-lookup"><span data-stu-id="31dce-1232">GValue</span></span>  
<span data-ttu-id="31dce-1233">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1233">Blue value of the color that you want to set; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1234">BValue</span><span class="sxs-lookup"><span data-stu-id="31dce-1234">BValue</span></span>  
<span data-ttu-id="31dce-1235">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1235">Blue value of the color that you want to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1236">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1236">Return Value</span></span>

<span data-ttu-id="31dce-1237">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1237">0 to indicate success; otherwise, failure.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1238">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1238">Remarks</span></span>

<span data-ttu-id="31dce-1239">入力パラメーターのいずれかがない場合は、画像内の位置 (0, 0) での色が使用されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1239">If any of the input parameters are missing, the color at the point (0,0) in the image is used.</span></span> <span data-ttu-id="31dce-1240">色を指定する場合、パラメーター 2 から 4 を使用すると、RGB カラーとして表記されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1240">If you want to specify a color, this is expressed as an RGB color by using parameters 2 to 4.</span></span>

### <a name="method-width"></a><span data-ttu-id="31dce-1241">メソッド width</span><span class="sxs-lookup"><span data-stu-id="31dce-1241">Method width</span></span>

<span data-ttu-id="31dce-1242">ピクセル単位の画像の幅を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1242">Retrieves the width of the image in pixels.</span></span>

    public int width()

#### <a name="return-value"></a><span data-ttu-id="31dce-1243">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1243">Return Value</span></span>

<span data-ttu-id="31dce-1244">画像の幅をピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1244">An integer that represents the width of the image in pixels.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1245">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1245">Examples</span></span>

<span data-ttu-id="31dce-1246">次の例では、test.bmp ファイル内のイメージの幅を出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1246">The following example prints out the width of the image in the test.bmp file.</span></span>

    Image img = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    print img.width(); 
    pause;

### <a name="method-canload"></a><span data-ttu-id="31dce-1247">メソッド canLoad</span><span class="sxs-lookup"><span data-stu-id="31dce-1247">Method canLoad</span></span>

<span data-ttu-id="31dce-1248">画像ファイルが存在し、開くことができるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1248">Determines whether an image file exists and can be opened.</span></span>

    public static int canLoad(str filename)

#### <a name="parameters"></a><span data-ttu-id="31dce-1249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1249">Parameters</span></span>

<span data-ttu-id="31dce-1250">filename</span><span class="sxs-lookup"><span data-stu-id="31dce-1250">filename</span></span>  
<span data-ttu-id="31dce-1251">確認するファイルの名前とパス。</span><span class="sxs-lookup"><span data-stu-id="31dce-1251">The name and path of the file to check.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1252">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1252">Return Value</span></span>

<span data-ttu-id="31dce-1253">画像が検索され、開くことができる場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1253">1 if the image is found and can be opened; otherwise, 0.</span></span>

### <a name="method-loadext"></a><span data-ttu-id="31dce-1254">メソッド loadExt</span><span class="sxs-lookup"><span data-stu-id="31dce-1254">Method loadExt</span></span>

<span data-ttu-id="31dce-1255">Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1255">Retrieves a list of the extensions of the file formats that are supported by the Image class.</span></span>

    public static container loadExt(int idx)

#### <a name="parameters"></a><span data-ttu-id="31dce-1256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1256">Parameters</span></span>

<span data-ttu-id="31dce-1257">idx</span><span class="sxs-lookup"><span data-stu-id="31dce-1257">idx</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1258">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1258">Return Value</span></span>

<span data-ttu-id="31dce-1259">サポートされているファイル形式の一覧を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1259">A container that holds a list of the supported file formats.</span></span>

### <a name="method-resourcetype"></a><span data-ttu-id="31dce-1260">メソッド resourceType</span><span class="sxs-lookup"><span data-stu-id="31dce-1260">Method resourceType</span></span>

<span data-ttu-id="31dce-1261">特定のリソースがビットマップかアイコンかを判別します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1261">Determines whether a particular resource is a bitmap or an icon.</span></span>

    public static int resourceType(int resourceIdx)

#### <a name="parameters"></a><span data-ttu-id="31dce-1262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1262">Parameters</span></span>

<span data-ttu-id="31dce-1263">resourceIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1263">resourceIdx</span></span>  
<span data-ttu-id="31dce-1264">読み込むリソースの ID。</span><span class="sxs-lookup"><span data-stu-id="31dce-1264">The ID of the resource that you want to load.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1265">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1265">Return Value</span></span>

<span data-ttu-id="31dce-1266">画像がビットマップの場合は 0、アイコンの場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1266">0 if the image is a bitmap; 1 if it is an icon.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1267">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1267">Remarks</span></span>

<span data-ttu-id="31dce-1268">リソースの値は、Resources マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1268">The values of resources can be found in the Resources macro.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1269">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1269">Examples</span></span>

<span data-ttu-id="31dce-1270">次の例では、リソース 3020 がアイコンかビットマップかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1270">The following example tests whether resource 3020 is an icon or a bitmap.</span></span>

    #Resource 
    print Image::resourceType(3020); 
    pause;

### <a name="method-rgb"></a><span data-ttu-id="31dce-1271">メソッド rgb</span><span class="sxs-lookup"><span data-stu-id="31dce-1271">Method rgb</span></span>

<span data-ttu-id="31dce-1272">RGB 値を ARGB 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1272">Converts an RGB value to an ARGB value.</span></span>

    public static int rgb(int R, int G, int B)

#### <a name="parameters"></a><span data-ttu-id="31dce-1273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1273">Parameters</span></span>

<span data-ttu-id="31dce-1274">R</span><span class="sxs-lookup"><span data-stu-id="31dce-1274">R</span></span>  
<span data-ttu-id="31dce-1275">色の青の値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1275">The blue value of the color.</span></span>

<!-- -->

<span data-ttu-id="31dce-1276">G</span><span class="sxs-lookup"><span data-stu-id="31dce-1276">G</span></span>  
<span data-ttu-id="31dce-1277">色の青の値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1277">The blue value of the color.</span></span>

<!-- -->

<span data-ttu-id="31dce-1278">B</span><span class="sxs-lookup"><span data-stu-id="31dce-1278">B</span></span>  
<span data-ttu-id="31dce-1279">色の青の値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1279">The blue value of the color.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1280">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1280">Return Value</span></span>

<span data-ttu-id="31dce-1281">パラメーターで指定された色の ARGB 値を表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1281">An integer that represents the ARGB value of the color that is specified by the parameters.</span></span>

### <a name="method-validresource"></a><span data-ttu-id="31dce-1282">メソッド validResource</span><span class="sxs-lookup"><span data-stu-id="31dce-1282">Method validResource</span></span>

<span data-ttu-id="31dce-1283">id パラメータで指定されたリソースが有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1283">Determines whether the resource specified by the id parameter is valid.</span></span>

    public static int validResource(int id)

#### <a name="parameters"></a><span data-ttu-id="31dce-1284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1284">Parameters</span></span>

<span data-ttu-id="31dce-1285">id</span><span class="sxs-lookup"><span data-stu-id="31dce-1285">id</span></span>  
<span data-ttu-id="31dce-1286">チェックするリソースの ID。</span><span class="sxs-lookup"><span data-stu-id="31dce-1286">The ID of the resource that you want to check.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1287">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1287">Return Value</span></span>

<span data-ttu-id="31dce-1288">ID が有効な場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1288">0 if the ID is valid.</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1289">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1289">Method new</span></span>

<span data-ttu-id="31dce-1290">新しい画像を作成します</span><span class="sxs-lookup"><span data-stu-id="31dce-1290">Creates a new image.</span></span>

    public void new([AnyType image], [int width], [int height])

#### <a name="parameters"></a><span data-ttu-id="31dce-1291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1291">Parameters</span></span>

<span data-ttu-id="31dce-1292">image</span><span class="sxs-lookup"><span data-stu-id="31dce-1292">image</span></span>  
<span data-ttu-id="31dce-1293">ピクセル単位の画像の高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31dce-1293">The height of the image in pixels; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1294">width</span><span class="sxs-lookup"><span data-stu-id="31dce-1294">width</span></span>  
<span data-ttu-id="31dce-1295">ピクセル単位の画像の高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31dce-1295">The height of the image in pixels; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1296">height</span><span class="sxs-lookup"><span data-stu-id="31dce-1296">height</span></span>  
<span data-ttu-id="31dce-1297">ピクセル単位の画像の高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31dce-1297">The height of the image in pixels; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1298">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1298">Remarks</span></span>

<span data-ttu-id="31dce-1299">パラメーターを指定する必要はありませんが、イメージの内容とサイズを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1299">You do not need to specify any parameters, but it is possible to specify the image contents and size.</span></span> <span data-ttu-id="31dce-1300">画像パラメーターについては、ファイル名および場所、リソース、配列での特定の画像、または別の画像オブジェクトを指定できます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1300">For the image parameter, you can specify a file name and location, a resource, a particular image in an array, or another Image object.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1301">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1301">Examples</span></span>

<span data-ttu-id="31dce-1302">次の例は、新しいイメージ オブジェクトの既存のコンテンツをオプションで指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31dce-1302">The following examples illustrate how you can optionally specify the existing content for the new image object.</span></span>

    Image img1 = new Image(@"C:\MyPicture.jpg", 100, 100); 
    Image img2 = new Image(121,100, 100); // Uses resource 121 in Ax32.exe 
    Image img4 = new Image(img1, 200, 200);

### <a name="method-displayorign"></a><span data-ttu-id="31dce-1303">メソッド displayOrign</span><span class="sxs-lookup"><span data-stu-id="31dce-1303">Method displayOrign</span></span>

<span data-ttu-id="31dce-1304">オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1304">Enables you to specify an offset (X, Y) from the original origin (0, 0).</span></span>

    public void displayOrign(int Xpos, int Ypos)

#### <a name="parameters"></a><span data-ttu-id="31dce-1305">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1305">Parameters</span></span>

<span data-ttu-id="31dce-1306">Xpos</span><span class="sxs-lookup"><span data-stu-id="31dce-1306">Xpos</span></span>  
<span data-ttu-id="31dce-1307">原点に対する新しい Y (垂直) 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1307">New Y (vertical) coordinate for the origin.</span></span>

<!-- -->

<span data-ttu-id="31dce-1308">Ypos</span><span class="sxs-lookup"><span data-stu-id="31dce-1308">Ypos</span></span>  
<span data-ttu-id="31dce-1309">原点に対する新しい Y (垂直) 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1309">New Y (vertical) coordinate for the origin.</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-1310">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-1310">Method finalize</span></span>

    public void finalize()

## <a name="class-imagelist"></a><span data-ttu-id="31dce-1311">クラス Imagelist</span><span class="sxs-lookup"><span data-stu-id="31dce-1311">Class Imagelist</span></span>
    class Imagelist extends BinData

<span data-ttu-id="31dce-1312">Imagelist クラスを使用すると、イメージの一覧を操作できます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1312">The Imagelist class lets you work with a list of images.</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-1313">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1313">Remarks</span></span>

<span data-ttu-id="31dce-1314">1 つの画像を操作するには、イメージ クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1314">To work with a single image, use the Image class.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1315">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1315">Examples</span></span>

<span data-ttu-id="31dce-1316">次の例では、イメージ リストを作成し、Shell32.dll ファイルにアイコンを追加します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1316">The following example creates an image list and adds the icons in the Shell32.dll file.</span></span> <span data-ttu-id="31dce-1317">一覧の 4 番目のメンバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1317">It then deletes the fourth member of the list.</span></span>

    Imagelist list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight() ); 
    list.loadIcons('shell32.dll'); 
    print list.count(); 
    list.remove(4); 
    print list.count(); 
    pause;

### <a name="methods"></a><span data-ttu-id="31dce-1318">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1318">Methods</span></span>

| <span data-ttu-id="31dce-1319">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1319">Method</span></span>                                                                         | <span data-ttu-id="31dce-1320">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1320">Description</span></span>                                                                                                                        |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-1321">public int add(Image image)</span><span class="sxs-lookup"><span data-stu-id="31dce-1321">public int add(Image image)</span></span>                                                    | <span data-ttu-id="31dce-1322">イメージ リストに新しい画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1322">Adds a new image to the image list.</span></span>                                                                                                |
| <span data-ttu-id="31dce-1323">public boolean autoResize(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1323">public boolean autoResize(\[boolean value\])</span></span>                                   | <span data-ttu-id="31dce-1324">新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1324">Sets the Boolean autoResize flag, which determines whether new images are automatically resized.</span></span>                                   |
| <span data-ttu-id="31dce-1325">public int clear()</span><span class="sxs-lookup"><span data-stu-id="31dce-1325">public int clear()</span></span>                                                             | <span data-ttu-id="31dce-1326">イメージ リストからすべての画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1326">Removes all images from the image list.</span></span>                                                                                            |
| <span data-ttu-id="31dce-1327">public int count()</span><span class="sxs-lookup"><span data-stu-id="31dce-1327">public int count()</span></span>                                                             | <span data-ttu-id="31dce-1328">画像リスト内のイメージの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1328">Retrieves the number of images in an image list.</span></span>                                                                                   |
| <span data-ttu-id="31dce-1329">public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)</span><span class="sxs-lookup"><span data-stu-id="31dce-1329">public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)</span></span>             | <span data-ttu-id="31dce-1330">イメージのドラッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1330">Begins dragging an image.</span></span>                                                                                                          |
| <span data-ttu-id="31dce-1331">public boolean dragEnd()</span><span class="sxs-lookup"><span data-stu-id="31dce-1331">public boolean dragEnd()</span></span>                                                       | <span data-ttu-id="31dce-1332">ドラッグ操作を終了します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1332">Ends a drag operation.</span></span>                                                                                                             |
| <span data-ttu-id="31dce-1333">public boolean dragEnter(int hWnd, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31dce-1333">public boolean dragEnter(int hWnd, int x, int y)</span></span>                               | <span data-ttu-id="31dce-1334">ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1334">Locks updates to the specified window during a drag operation and displays the drag image at the specified position in the window.</span></span> |
| <span data-ttu-id="31dce-1335">public boolean dragLeave(int hWnd)</span><span class="sxs-lookup"><span data-stu-id="31dce-1335">public boolean dragLeave(int hWnd)</span></span>                                             | <span data-ttu-id="31dce-1336">指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1336">Unlocks the specified window and hides the drag image, so that the window to be updated.</span></span>                                           |
| <span data-ttu-id="31dce-1337">public boolean dragMove(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31dce-1337">public boolean dragMove(int x, int y)</span></span>                                          | <span data-ttu-id="31dce-1338">ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1338">Moves the image that is being dragged during a drag-and-drop operation.</span></span>                                                            |
| <span data-ttu-id="31dce-1339">public boolean dragShowImage(boolean show)</span><span class="sxs-lookup"><span data-stu-id="31dce-1339">public boolean dragShowImage(boolean show)</span></span>                                     | <span data-ttu-id="31dce-1340">ドラッグされている画像の表示と非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1340">Shows or hides the image that is being dragged.</span></span>                                                                                    |
| <span data-ttu-id="31dce-1341">public int height()</span><span class="sxs-lookup"><span data-stu-id="31dce-1341">public int height()</span></span>                                                            | <span data-ttu-id="31dce-1342">イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1342">Retrieves the height, in pixels, of the images in the image list.</span></span>                                                                  |
| <span data-ttu-id="31dce-1343">public int loadIcons(str moduleName)</span><span class="sxs-lookup"><span data-stu-id="31dce-1343">public int loadIcons(str moduleName)</span></span>                                           | <span data-ttu-id="31dce-1344">イメージ リストに、指定されたリソースからアイコンを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1344">Loads icons from the specified resource into the image list.</span></span>                                                                       |
| <span data-ttu-id="31dce-1345">public int remove(int imageIdx)</span><span class="sxs-lookup"><span data-stu-id="31dce-1345">public int remove(int imageIdx)</span></span>                                                | <span data-ttu-id="31dce-1346">イメージ リストから画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1346">Removes an image from an image list.</span></span>                                                                                               |
| <span data-ttu-id="31dce-1347">public int replace(int imageIdx, Image image)</span><span class="sxs-lookup"><span data-stu-id="31dce-1347">public int replace(int imageIdx, Image image)</span></span>                                  | <span data-ttu-id="31dce-1348">リスト内の既存の画像を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1348">Replaces an existing image in the list.</span></span>                                                                                            |
| <span data-ttu-id="31dce-1349">public boolean setOverlayImage(int imageIdx, int overlayIdx)</span><span class="sxs-lookup"><span data-stu-id="31dce-1349">public boolean setOverlayImage(int imageIdx, int overlayIdx)</span></span>                   | <span data-ttu-id="31dce-1350">オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1350">Adds an image to the list of images to use as overlay masks.</span></span>                                                                       |
| <span data-ttu-id="31dce-1351">public int width()</span><span class="sxs-lookup"><span data-stu-id="31dce-1351">public int width()</span></span>                                                             | <span data-ttu-id="31dce-1352">イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1352">Retrieves the width, in pixels, of the images in the image list.</span></span>                                                                   |
| <span data-ttu-id="31dce-1353">::public static int iconHeight()</span><span class="sxs-lookup"><span data-stu-id="31dce-1353">::public static int iconHeight()</span></span>                                               | <span data-ttu-id="31dce-1354">標準アイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1354">Retrieves the system metrics for the height of a standard icon.</span></span>                                                                    |
| <span data-ttu-id="31dce-1355">::public static int iconWidth()</span><span class="sxs-lookup"><span data-stu-id="31dce-1355">::public static int iconWidth()</span></span>                                                | <span data-ttu-id="31dce-1356">標準アイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1356">Retrieves the system metrics for the width of a standard icon.</span></span>                                                                     |
| <span data-ttu-id="31dce-1357">::public static int smallIconHeight()</span><span class="sxs-lookup"><span data-stu-id="31dce-1357">::public static int smallIconHeight()</span></span>                                          | <span data-ttu-id="31dce-1358">小さなアイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1358">Retrieves the system metrics for the height of a small icon.</span></span>                                                                       |
| <span data-ttu-id="31dce-1359">::public static int smallIconWidth()</span><span class="sxs-lookup"><span data-stu-id="31dce-1359">::public static int smallIconWidth()</span></span>                                           | <span data-ttu-id="31dce-1360">小さなアイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1360">Retrieves the system metrics for the width of a small icon.</span></span>                                                                        |
| <span data-ttu-id="31dce-1361">public void maskColor(int Color)</span><span class="sxs-lookup"><span data-stu-id="31dce-1361">public void maskColor(int Color)</span></span>                                               | <span data-ttu-id="31dce-1362">マスキング色を設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1362">Sets the masking color.</span></span>                                                                                                            |
| <span data-ttu-id="31dce-1363">public void draw(int HDC, int imageIdx, int x, int y, \[boolean transparent\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1363">public void draw(int HDC, int imageIdx, int x, int y, \[boolean transparent\])</span></span> | <span data-ttu-id="31dce-1364">指定されたデバイス コンテキストで画像リスト項目を描画します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1364">Draws an image list item in the specified device context.</span></span>                                                                          |
| <span data-ttu-id="31dce-1365">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-1365">public void finalize()</span></span>                                                         |                                                                                                                                    |
| <span data-ttu-id="31dce-1366">public void new(int cx, int cy, \[boolean transparent\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1366">public void new(int cx, int cy, \[boolean transparent\])</span></span>                       | <span data-ttu-id="31dce-1367">画像を保持する新しい空のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1367">Creates a new empty list to hold images.</span></span>                                                                                           |

### <a name="method-add"></a><span data-ttu-id="31dce-1368">メソッド add</span><span class="sxs-lookup"><span data-stu-id="31dce-1368">Method add</span></span>

<span data-ttu-id="31dce-1369">イメージ リストに新しい画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1369">Adds a new image to the image list.</span></span>

    public int add(Image image)

#### <a name="parameters"></a><span data-ttu-id="31dce-1370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1370">Parameters</span></span>

<span data-ttu-id="31dce-1371">image</span><span class="sxs-lookup"><span data-stu-id="31dce-1371">image</span></span>  
<span data-ttu-id="31dce-1372">リストに追加する新しい画像。</span><span class="sxs-lookup"><span data-stu-id="31dce-1372">The new image to add to the list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1373">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1373">Return Value</span></span>

<span data-ttu-id="31dce-1374">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1374">0 if the method is successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1375">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1375">Remarks</span></span>

<span data-ttu-id="31dce-1376">autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1376">You can use the autoResize method to automatically resize images when you add them to the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1377">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1377">Examples</span></span>

<span data-ttu-id="31dce-1378">次の例では、新しいイメージ リストを作成し、3 つのイメージを追加します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1378">The following example creates a new image list and adds three images to it.</span></span>

    ImageList list = new Imagelist( 
        Imagelist::smallIconWidth(), 
        Imagelist::smallIconHeight()); 
    list.add(new Image(3104)); 
    list.add(new Image(1097)); 
    list.add(new Image(1200)); 
    // Prints 3 
    print list.count(); 
    pause;

### <a name="method-autoresize"></a><span data-ttu-id="31dce-1379">メソッド autoResize</span><span class="sxs-lookup"><span data-stu-id="31dce-1379">Method autoResize</span></span>

<span data-ttu-id="31dce-1380">新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1380">Sets the Boolean autoResize flag, which determines whether new images are automatically resized.</span></span>

    public boolean autoResize([boolean value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1381">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1381">Parameters</span></span>

<span data-ttu-id="31dce-1382">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1382">value</span></span>  
<span data-ttu-id="31dce-1383">autoResize フラグが設定されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1383">A Boolean value that determines whether the autoResize flag is set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1384">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1384">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1385">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1385">Remarks</span></span>

<span data-ttu-id="31dce-1386">autoResize フラッグが true に設定されている場合、リストに追加する任意の画像サイズは、画像リストの作成時に指定された分析コードに自動的に再調整されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1386">If the autoResize flag is set to true, any image that you add to the list is automatically resized to the dimensions that were specified when you created the image list.</span></span>

### <a name="method-clear"></a><span data-ttu-id="31dce-1387">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="31dce-1387">Method clear</span></span>

<span data-ttu-id="31dce-1388">イメージ リストからすべての画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1388">Removes all images from the image list.</span></span>

    public int clear()

#### <a name="return-value"></a><span data-ttu-id="31dce-1389">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1389">Return Value</span></span>

<span data-ttu-id="31dce-1390">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1390">0 if the method is successful.</span></span>

### <a name="method-count"></a><span data-ttu-id="31dce-1391">メソッド count</span><span class="sxs-lookup"><span data-stu-id="31dce-1391">Method count</span></span>

<span data-ttu-id="31dce-1392">画像リスト内のイメージの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1392">Retrieves the number of images in an image list.</span></span>

    public int count()

#### <a name="return-value"></a><span data-ttu-id="31dce-1393">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1393">Return Value</span></span>

<span data-ttu-id="31dce-1394">リスト内の画像の数を表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1394">An integer that represents the number of images in the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1395">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1395">Examples</span></span>

<span data-ttu-id="31dce-1396">次の例では、イメージ リストを作成し、shell.dll ファイルからアイコンを読み込み、リスト内のイメージの数を出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1396">The following example creates an image list, loads icons from the shell.dll file, and then prints the number of images in the list.</span></span>

    Imagelist list; 
    int       counter; 
    list = new Imagelist( 
       Imagelist::iconWidth(), 
       Imagelist::iconHeight() ); 
    list.loadIcons('shell32.dll'); 
    print list.count(); 
    pause;

### <a name="method-dragbegin"></a><span data-ttu-id="31dce-1397">メソッド dragBegin</span><span class="sxs-lookup"><span data-stu-id="31dce-1397">Method dragBegin</span></span>

<span data-ttu-id="31dce-1398">イメージのドラッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1398">Begins dragging an image.</span></span>

    public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)

#### <a name="parameters"></a><span data-ttu-id="31dce-1399">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1399">Parameters</span></span>

<span data-ttu-id="31dce-1400">imageIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1400">imageIdx</span></span>  
<span data-ttu-id="31dce-1401">画像の左上隅を基準とした、ドラッグ位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1401">The Y-coordinate of the drag position, relative to the upper-left corner of the image.</span></span>

<!-- -->

<span data-ttu-id="31dce-1402">hotSpotX</span><span class="sxs-lookup"><span data-stu-id="31dce-1402">hotSpotX</span></span>  
<span data-ttu-id="31dce-1403">画像の左上隅を基準とした、ドラッグ位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1403">The Y-coordinate of the drag position, relative to the upper-left corner of the image.</span></span>

<!-- -->

<span data-ttu-id="31dce-1404">hotSpotY</span><span class="sxs-lookup"><span data-stu-id="31dce-1404">hotSpotY</span></span>  
<span data-ttu-id="31dce-1405">画像の左上隅を基準とした、ドラッグ位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1405">The Y-coordinate of the drag position, relative to the upper-left corner of the image.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1406">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1406">Return Value</span></span>

<span data-ttu-id="31dce-1407">メソッドが成功した場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1407">1 if the method is successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1408">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1408">Remarks</span></span>

<span data-ttu-id="31dce-1409">残りのドラッグ操作は、dragEnter、dragMove、dragLeave、dragEnd の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1409">The rest of the drag operation is specified by the dragEnter, dragMove, dragLeave, and dragEnd methods.</span></span>

### <a name="method-dragend"></a><span data-ttu-id="31dce-1410">メソッド dragEnd</span><span class="sxs-lookup"><span data-stu-id="31dce-1410">Method dragEnd</span></span>

<span data-ttu-id="31dce-1411">ドラッグ操作を終了します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1411">Ends a drag operation.</span></span>

    public boolean dragEnd()

#### <a name="return-value"></a><span data-ttu-id="31dce-1412">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1412">Return Value</span></span>

<span data-ttu-id="31dce-1413">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1413">1 if the method is successful; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1414">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1414">Remarks</span></span>

<span data-ttu-id="31dce-1415">残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragLeave の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1415">The rest of the drag operation is specified by the dragBegin, dragEnter, dragMove, and dragLeave methods.</span></span>

### <a name="method-dragenter"></a><span data-ttu-id="31dce-1416">メソッド dragEnter</span><span class="sxs-lookup"><span data-stu-id="31dce-1416">Method dragEnter</span></span>

<span data-ttu-id="31dce-1417">ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1417">Locks updates to the specified window during a drag operation and displays the drag image at the specified position in the window.</span></span>

    public boolean dragEnter(int hWnd, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="31dce-1418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1418">Parameters</span></span>

<span data-ttu-id="31dce-1419">hWnd</span><span class="sxs-lookup"><span data-stu-id="31dce-1419">hWnd</span></span>  
<span data-ttu-id="31dce-1420">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1420">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

<!-- -->

<span data-ttu-id="31dce-1421">x</span><span class="sxs-lookup"><span data-stu-id="31dce-1421">x</span></span>  
<span data-ttu-id="31dce-1422">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1422">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

<!-- -->

<span data-ttu-id="31dce-1423">y</span><span class="sxs-lookup"><span data-stu-id="31dce-1423">y</span></span>  
<span data-ttu-id="31dce-1424">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1424">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1425">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1425">Return Value</span></span>

<span data-ttu-id="31dce-1426">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1426">1 if the method is successful; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1427">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1427">Remarks</span></span>

<span data-ttu-id="31dce-1428">ドラッグ操作を開始するには、dragBegin メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1428">To start the drag operation, call the dragBegin method.</span></span> <span data-ttu-id="31dce-1429">残りのドラッグ操作は、dragMove、dragLeave、dragEnd の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1429">The rest of the drag operation is specified by the dragMove, dragLeave, and dragEnd methods.</span></span>

### <a name="method-dragleave"></a><span data-ttu-id="31dce-1430">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="31dce-1430">Method dragLeave</span></span>

<span data-ttu-id="31dce-1431">指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1431">Unlocks the specified window and hides the drag image, so that the window to be updated.</span></span>

    public boolean dragLeave(int hWnd)

#### <a name="parameters"></a><span data-ttu-id="31dce-1432">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1432">Parameters</span></span>

<span data-ttu-id="31dce-1433">hWnd</span><span class="sxs-lookup"><span data-stu-id="31dce-1433">hWnd</span></span>  
<span data-ttu-id="31dce-1434">ドラッグ イメージを所有するウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1434">The handle to the window that owns the drag image.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1435">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1435">Return Value</span></span>

<span data-ttu-id="31dce-1436">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1436">1 if the method is successful; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1437">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1437">Remarks</span></span>

<span data-ttu-id="31dce-1438">残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragEnd の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1438">The rest of the drag operation is specified by the dragBegin, dragEnter, dragMove, and dragEnd methods.</span></span>

### <a name="method-dragmove"></a><span data-ttu-id="31dce-1439">メソッド dragMove</span><span class="sxs-lookup"><span data-stu-id="31dce-1439">Method dragMove</span></span>

<span data-ttu-id="31dce-1440">ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1440">Moves the image that is being dragged during a drag-and-drop operation.</span></span>

    public boolean dragMove(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="31dce-1441">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1441">Parameters</span></span>

<span data-ttu-id="31dce-1442">x</span><span class="sxs-lookup"><span data-stu-id="31dce-1442">x</span></span>  
<span data-ttu-id="31dce-1443">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1443">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

<!-- -->

<span data-ttu-id="31dce-1444">y</span><span class="sxs-lookup"><span data-stu-id="31dce-1444">y</span></span>  
<span data-ttu-id="31dce-1445">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="31dce-1445">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1446">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1446">Return Value</span></span>

<span data-ttu-id="31dce-1447">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1447">1 if the method is successful; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1448">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1448">Remarks</span></span>

<span data-ttu-id="31dce-1449">ドラッグ操作を開始するには、dragBegin メソッドを呼び出してから dragEnter メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1449">To start the drag operation, call the dragBegin method and then the dragEnter method.</span></span> <span data-ttu-id="31dce-1450">残りのドラッグ操作は、dragLeave メソッドおよび dragEnd メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1450">The rest of the drag operation is specified by the dragLeave and dragEnd methods.</span></span>

### <a name="method-dragshowimage"></a><span data-ttu-id="31dce-1451">メソッド dragShowImage</span><span class="sxs-lookup"><span data-stu-id="31dce-1451">Method dragShowImage</span></span>

<span data-ttu-id="31dce-1452">ドラッグされている画像の表示と非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1452">Shows or hides the image that is being dragged.</span></span>

    public boolean dragShowImage(boolean show)

#### <a name="parameters"></a><span data-ttu-id="31dce-1453">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1453">Parameters</span></span>

<span data-ttu-id="31dce-1454">show</span><span class="sxs-lookup"><span data-stu-id="31dce-1454">show</span></span>  
<span data-ttu-id="31dce-1455">画像を表示するかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1455">A value that specifies whether to show the image.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1456">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1456">Return Value</span></span>

### <a name="method-height"></a><span data-ttu-id="31dce-1457">メソッド height</span><span class="sxs-lookup"><span data-stu-id="31dce-1457">Method height</span></span>

<span data-ttu-id="31dce-1458">イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1458">Retrieves the height, in pixels, of the images in the image list.</span></span>

    public int height()

#### <a name="return-value"></a><span data-ttu-id="31dce-1459">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1459">Return Value</span></span>

<span data-ttu-id="31dce-1460">画像の高さをピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1460">An integer that represents the height of the images in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1461">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1461">Remarks</span></span>

<span data-ttu-id="31dce-1462">リスト内の画像の高さは、リストをインスタンス化するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1462">The height of the images in the list is set when you instantiate the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1463">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1463">Examples</span></span>

<span data-ttu-id="31dce-1464">次の例では、イメージ リストを作成し、イメージの高さと幅を iconWidth メソッドと iconHeight メソッドで指定された寸法に設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1464">The following example creates an image list, and sets the height and width of the images to the dimensions that are specified by the iconWidth and iconHeight methods.</span></span> <span data-ttu-id="31dce-1465">一覧内のイメージの高さを出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1465">It then prints the height of images in the list.</span></span>

    Imagelist list; 
    list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight()); 
    print list.height();   
    pause;

### <a name="method-loadicons"></a><span data-ttu-id="31dce-1466">メソッド loadIcons</span><span class="sxs-lookup"><span data-stu-id="31dce-1466">Method loadIcons</span></span>

<span data-ttu-id="31dce-1467">イメージ リストに、指定されたリソースからアイコンを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1467">Loads icons from the specified resource into the image list.</span></span>

    public int loadIcons(str moduleName)

#### <a name="parameters"></a><span data-ttu-id="31dce-1468">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1468">Parameters</span></span>

<span data-ttu-id="31dce-1469">moduleName</span><span class="sxs-lookup"><span data-stu-id="31dce-1469">moduleName</span></span>  
<span data-ttu-id="31dce-1470">イメージの読み込み元ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="31dce-1470">The name of the file from which to load images.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1471">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1471">Return Value</span></span>

<span data-ttu-id="31dce-1472">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1472">0 if the method is successful.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1473">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1473">Examples</span></span>

<span data-ttu-id="31dce-1474">次の例では、イメージのリストを作成し、shell32.dll ファイルに含まれるイメージをロードします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1474">The following example creates a list of images and then loads the images that are contained in the shell32.dll file.</span></span>

    Imagelist list; 
    list = new Imagelist(Imagelist::iconWidth(),Imagelist::iconHeight()); 
    list.loadIcons('shell32.dll');

### <a name="method-remove"></a><span data-ttu-id="31dce-1475">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="31dce-1475">Method remove</span></span>

<span data-ttu-id="31dce-1476">イメージ リストから画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1476">Removes an image from an image list.</span></span>

    public int remove(int imageIdx)

#### <a name="parameters"></a><span data-ttu-id="31dce-1477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1477">Parameters</span></span>

<span data-ttu-id="31dce-1478">imageIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1478">imageIdx</span></span>  
<span data-ttu-id="31dce-1479">一覧から削除する画像の位置。</span><span class="sxs-lookup"><span data-stu-id="31dce-1479">The position of the image to remove from the list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1480">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1480">Return Value</span></span>

<span data-ttu-id="31dce-1481">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1481">0 if the method is successful.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1482">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1482">Examples</span></span>

<span data-ttu-id="31dce-1483">次の例では、イメージ リストを作成し、アイコンを shell32.dll ファイルに追加して、リストの 4 番目のメンバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1483">The following example creates an image list, adds the icons in shell32.dll file, and then deletes the fourth member of the list.</span></span>

    Imagelist list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight() ); 
    list.loadIcons('shell32.dll'); 
    print list.count(); 
    list.remove(4); 
    print list.count(); 
    pause;

### <a name="method-replace"></a><span data-ttu-id="31dce-1484">メソッド replace</span><span class="sxs-lookup"><span data-stu-id="31dce-1484">Method replace</span></span>

<span data-ttu-id="31dce-1485">リスト内の既存の画像を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1485">Replaces an existing image in the list.</span></span>

    public int replace(int imageIdx, Image image)

#### <a name="parameters"></a><span data-ttu-id="31dce-1486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1486">Parameters</span></span>

<span data-ttu-id="31dce-1487">imageIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1487">imageIdx</span></span>  
<span data-ttu-id="31dce-1488">既存のイメージを置き換えるために使用するイメージ。</span><span class="sxs-lookup"><span data-stu-id="31dce-1488">The image to use to replace the existing image.</span></span>

<!-- -->

<span data-ttu-id="31dce-1489">image</span><span class="sxs-lookup"><span data-stu-id="31dce-1489">image</span></span>  
<span data-ttu-id="31dce-1490">既存のイメージを置き換えるために使用するイメージ。</span><span class="sxs-lookup"><span data-stu-id="31dce-1490">The image to use to replace the existing image.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1491">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1491">Return Value</span></span>

<span data-ttu-id="31dce-1492">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1492">0 if the method is successful.</span></span>

### <a name="method-setoverlayimage"></a><span data-ttu-id="31dce-1493">メソッド setOverlayImage</span><span class="sxs-lookup"><span data-stu-id="31dce-1493">Method setOverlayImage</span></span>

<span data-ttu-id="31dce-1494">オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1494">Adds an image to the list of images to use as overlay masks.</span></span>

    public boolean setOverlayImage(int imageIdx, int overlayIdx)

#### <a name="parameters"></a><span data-ttu-id="31dce-1495">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1495">Parameters</span></span>

<span data-ttu-id="31dce-1496">imageIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1496">imageIdx</span></span>  
<span data-ttu-id="31dce-1497">オーバーレイ マスクの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="31dce-1497">The one-based index of the overlay mask.</span></span>

<!-- -->

<span data-ttu-id="31dce-1498">overlayIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1498">overlayIdx</span></span>  
<span data-ttu-id="31dce-1499">オーバーレイ マスクの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="31dce-1499">The one-based index of the overlay mask.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1500">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1500">Return Value</span></span>

<span data-ttu-id="31dce-1501">メソッドが成功した場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1501">1 if the method is successful.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1502">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1502">Examples</span></span>

<span data-ttu-id="31dce-1503">次の例では、3 つのイメージを持つイメージ リストを作成し、最後のイメージをオーバーレイ マスクとして設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1503">The following example creates an image list that has three images and then sets the last image as an overlay mask.</span></span>

    Imagelist list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight() ); 
    list.add(new Image(824)); // Image 0 
    list.add(new Image(815)); // Image 1 
    list.add(new Image(936)); //Image 2 
    list.setOverlayImage (2,1);

### <a name="method-width"></a><span data-ttu-id="31dce-1504">メソッド width</span><span class="sxs-lookup"><span data-stu-id="31dce-1504">Method width</span></span>

<span data-ttu-id="31dce-1505">イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1505">Retrieves the width, in pixels, of the images in the image list.</span></span>

    public int width()

#### <a name="return-value"></a><span data-ttu-id="31dce-1506">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1506">Return Value</span></span>

<span data-ttu-id="31dce-1507">画像の幅をピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1507">An integer that represents the width of the images in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1508">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1508">Remarks</span></span>

<span data-ttu-id="31dce-1509">リスト内の画像の幅は、リストをインスタンス化するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1509">The width of the images in the list is set when you instantiate the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1510">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1510">Examples</span></span>

<span data-ttu-id="31dce-1511">次の例では、アイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1511">The following example creates an image list that has the standard height and width for icons, and then prints the width of images in the list.</span></span>

    Imagelist list; 
    list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight()); 
    print list.width();   
    pause;

### <a name="method-iconheight"></a><span data-ttu-id="31dce-1512">メソッド iconHeight</span><span class="sxs-lookup"><span data-stu-id="31dce-1512">Method iconHeight</span></span>

<span data-ttu-id="31dce-1513">標準アイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1513">Retrieves the system metrics for the height of a standard icon.</span></span>

    public static int iconHeight()

#### <a name="return-value"></a><span data-ttu-id="31dce-1514">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1514">Return Value</span></span>

<span data-ttu-id="31dce-1515">標準アイコンの高さを表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1515">An integer that represents the height of a standard icon.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1516">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1516">Examples</span></span>

<span data-ttu-id="31dce-1517">次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1517">The following example creates a list of images, and then sets them to the standard icon width and height.</span></span>

    ImageList list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight());

### <a name="method-iconwidth"></a><span data-ttu-id="31dce-1518">メソッド iconWidth</span><span class="sxs-lookup"><span data-stu-id="31dce-1518">Method iconWidth</span></span>

<span data-ttu-id="31dce-1519">標準アイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1519">Retrieves the system metrics for the width of a standard icon.</span></span>

    public static int iconWidth()

#### <a name="return-value"></a><span data-ttu-id="31dce-1520">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1520">Return Value</span></span>

<span data-ttu-id="31dce-1521">標準アイコンの幅を表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1521">An integer that represents the width of a standard icon.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1522">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1522">Examples</span></span>

<span data-ttu-id="31dce-1523">次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1523">The following example creates a list of images, and then sets them to the standard icon width and height.</span></span>

    ImageList list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight());

### <a name="method-smalliconheight"></a><span data-ttu-id="31dce-1524">メソッド smallIconHeight</span><span class="sxs-lookup"><span data-stu-id="31dce-1524">Method smallIconHeight</span></span>

<span data-ttu-id="31dce-1525">小さなアイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1525">Retrieves the system metrics for the height of a small icon.</span></span>

    public static int smallIconHeight()

#### <a name="return-value"></a><span data-ttu-id="31dce-1526">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1526">Return Value</span></span>

<span data-ttu-id="31dce-1527">小さなアイコンの高さを表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1527">An integer that represents the height of a small icon.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1528">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1528">Examples</span></span>

<span data-ttu-id="31dce-1529">次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの高さをリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1529">The following example creates an image list that has the standard height and width for small icons, and then prints the height of images in the list.</span></span>

    Imagelist list = new Imagelist( 
        Imagelist::smallIconWidth(), 
        Imagelist::smallIconHeight()); 
    print list.height();   
    pause;

### <a name="method-smalliconwidth"></a><span data-ttu-id="31dce-1530">メソッド smallIconWidth</span><span class="sxs-lookup"><span data-stu-id="31dce-1530">Method smallIconWidth</span></span>

<span data-ttu-id="31dce-1531">小さなアイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1531">Retrieves the system metrics for the width of a small icon.</span></span>

    public static int smallIconWidth()

#### <a name="return-value"></a><span data-ttu-id="31dce-1532">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1532">Return Value</span></span>

<span data-ttu-id="31dce-1533">小さなアイコンの幅を表す整数。</span><span class="sxs-lookup"><span data-stu-id="31dce-1533">An integer that represents the width of a small icon.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1534">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1534">Examples</span></span>

<span data-ttu-id="31dce-1535">次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1535">The following example creates an image list that has the standard height and width for small icons, and then prints the width of images in the list.</span></span>

    Imagelist list = new Imagelist( 
       Imagelist::smallIconWidth(), 
       Imagelist::smallIconHeight()); 
    print list.width();   
    pause;

### <a name="method-maskcolor"></a><span data-ttu-id="31dce-1536">メソッド maskColor</span><span class="sxs-lookup"><span data-stu-id="31dce-1536">Method maskColor</span></span>

<span data-ttu-id="31dce-1537">マスキング色を設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1537">Sets the masking color.</span></span>

    public void maskColor(int Color)

#### <a name="parameters"></a><span data-ttu-id="31dce-1538">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1538">Parameters</span></span>

<span data-ttu-id="31dce-1539">色</span><span class="sxs-lookup"><span data-stu-id="31dce-1539">Color</span></span>  
<span data-ttu-id="31dce-1540">ARGB 値としての色。</span><span class="sxs-lookup"><span data-stu-id="31dce-1540">The color as an ARGB value.</span></span>

### <a name="method-draw"></a><span data-ttu-id="31dce-1541">メソッド draw</span><span class="sxs-lookup"><span data-stu-id="31dce-1541">Method draw</span></span>

<span data-ttu-id="31dce-1542">指定されたデバイス コンテキストで画像リスト項目を描画します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1542">Draws an image list item in the specified device context.</span></span>

    public void draw(int HDC, int imageIdx, int x, int y, [boolean transparent])

#### <a name="parameters"></a><span data-ttu-id="31dce-1543">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1543">Parameters</span></span>

<span data-ttu-id="31dce-1544">HDC</span><span class="sxs-lookup"><span data-stu-id="31dce-1544">HDC</span></span>  
<span data-ttu-id="31dce-1545">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1545">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1546">imageIdx</span><span class="sxs-lookup"><span data-stu-id="31dce-1546">imageIdx</span></span>  
<span data-ttu-id="31dce-1547">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1547">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1548">x</span><span class="sxs-lookup"><span data-stu-id="31dce-1548">x</span></span>  
<span data-ttu-id="31dce-1549">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1549">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1550">y</span><span class="sxs-lookup"><span data-stu-id="31dce-1550">y</span></span>  
<span data-ttu-id="31dce-1551">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1551">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="31dce-1552">透明</span><span class="sxs-lookup"><span data-stu-id="31dce-1552">transparent</span></span>  
<span data-ttu-id="31dce-1553">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31dce-1553">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-1554">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-1554">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="31dce-1555">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1555">Method new</span></span>

<span data-ttu-id="31dce-1556">画像を保持する新しい空のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1556">Creates a new empty list to hold images.</span></span>

    public void new(int cx, int cy, [boolean transparent])

#### <a name="parameters"></a><span data-ttu-id="31dce-1557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1557">Parameters</span></span>

<span data-ttu-id="31dce-1558">cx</span><span class="sxs-lookup"><span data-stu-id="31dce-1558">cx</span></span>  

<!-- -->

<span data-ttu-id="31dce-1559">cy</span><span class="sxs-lookup"><span data-stu-id="31dce-1559">cy</span></span>  

<!-- -->

<span data-ttu-id="31dce-1560">透明</span><span class="sxs-lookup"><span data-stu-id="31dce-1560">transparent</span></span>  

#### <a name="remarks"></a><span data-ttu-id="31dce-1561">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1561">Remarks</span></span>

<span data-ttu-id="31dce-1562">autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1562">You can use the autoResize method to automatically resize images when you add them to the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1563">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1563">Examples</span></span>

<span data-ttu-id="31dce-1564">次の例では、標準アイコンの幅と高さの項目を保持するイメージ リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1564">The following example creates an image list to hold items of the standard icon width and height.</span></span>

    Imagelist list; 
    list = new Imagelist( 
       Imagelist::iconWidth(), 
       Imagelist::iconHeight());

## <a name="class-importtabledatainfo"></a><span data-ttu-id="31dce-1565">クラス ImportTableDataInfo</span><span class="sxs-lookup"><span data-stu-id="31dce-1565">Class ImportTableDataInfo</span></span>
    class ImportTableDataInfo extends Object

### <a name="remarks"></a><span data-ttu-id="31dce-1566">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1566">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1567">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1567">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1568">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1568">Methods</span></span>

| <span data-ttu-id="31dce-1569">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1569">Method</span></span>                                                  | <span data-ttu-id="31dce-1570">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1570">Description</span></span>                                     |
|---------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="31dce-1571">public int addColumnData(str szColName, AnyType colVal)</span><span class="sxs-lookup"><span data-stu-id="31dce-1571">public int addColumnData(str szColName, AnyType colVal)</span></span> |                                                 |
| <span data-ttu-id="31dce-1572">public int copyDataRow()</span><span class="sxs-lookup"><span data-stu-id="31dce-1572">public int copyDataRow()</span></span>                                |                                                 |
| <span data-ttu-id="31dce-1573">public void new(int usTableId)</span><span class="sxs-lookup"><span data-stu-id="31dce-1573">public void new(int usTableId)</span></span>                          | <span data-ttu-id="31dce-1574">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1574">Initializes a new instance of the Object class.</span></span> |

### <a name="method-addcolumndata"></a><span data-ttu-id="31dce-1575">メソッド addColumnData</span><span class="sxs-lookup"><span data-stu-id="31dce-1575">Method addColumnData</span></span>

    public int addColumnData(str szColName, AnyType colVal)

#### <a name="parameters"></a><span data-ttu-id="31dce-1576">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1576">Parameters</span></span>

<span data-ttu-id="31dce-1577">szColName</span><span class="sxs-lookup"><span data-stu-id="31dce-1577">szColName</span></span>  

<!-- -->

<span data-ttu-id="31dce-1578">colVal</span><span class="sxs-lookup"><span data-stu-id="31dce-1578">colVal</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1579">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1579">Return Value</span></span>

### <a name="method-copydatarow"></a><span data-ttu-id="31dce-1580">メソッド copyDataRow</span><span class="sxs-lookup"><span data-stu-id="31dce-1580">Method copyDataRow</span></span>

    public int copyDataRow()

#### <a name="return-value"></a><span data-ttu-id="31dce-1581">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1581">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1582">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1582">Method new</span></span>

<span data-ttu-id="31dce-1583">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1583">Initializes a new instance of the Object class.</span></span>

    public void new(int usTableId)

#### <a name="parameters"></a><span data-ttu-id="31dce-1584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1584">Parameters</span></span>

<span data-ttu-id="31dce-1585">usTableId</span><span class="sxs-lookup"><span data-stu-id="31dce-1585">usTableId</span></span>  

## <a name="class-importtableschemainfo"></a><span data-ttu-id="31dce-1586">クラス ImportTableSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="31dce-1586">Class ImportTableSchemaInfo</span></span>
    class ImportTableSchemaInfo extends Object

### <a name="remarks"></a><span data-ttu-id="31dce-1587">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1587">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1588">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1588">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1589">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1589">Methods</span></span>

| <span data-ttu-id="31dce-1590">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1590">Method</span></span>                                                                             | <span data-ttu-id="31dce-1591">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1591">Description</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="31dce-1592">public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)</span><span class="sxs-lookup"><span data-stu-id="31dce-1592">public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)</span></span> |                                                 |
| <span data-ttu-id="31dce-1593">public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)</span><span class="sxs-lookup"><span data-stu-id="31dce-1593">public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)</span></span>        |                                                 |
| <span data-ttu-id="31dce-1594">public int hasEqualityCriteria(boolean fHasEqualityCriteria)</span><span class="sxs-lookup"><span data-stu-id="31dce-1594">public int hasEqualityCriteria(boolean fHasEqualityCriteria)</span></span>                       |                                                 |
| <span data-ttu-id="31dce-1595">public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)</span><span class="sxs-lookup"><span data-stu-id="31dce-1595">public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)</span></span>                 |                                                 |
| <span data-ttu-id="31dce-1596">public void new(int usTableId)</span><span class="sxs-lookup"><span data-stu-id="31dce-1596">public void new(int usTableId)</span></span>                                                     | <span data-ttu-id="31dce-1597">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1597">Initializes a new instance of the Object class.</span></span> |

### <a name="method-addcolumninfo"></a><span data-ttu-id="31dce-1598">メソッド addColumnInfo</span><span class="sxs-lookup"><span data-stu-id="31dce-1598">Method addColumnInfo</span></span>

    public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)

#### <a name="parameters"></a><span data-ttu-id="31dce-1599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1599">Parameters</span></span>

<span data-ttu-id="31dce-1600">szColName</span><span class="sxs-lookup"><span data-stu-id="31dce-1600">szColName</span></span>  

<!-- -->

<span data-ttu-id="31dce-1601">eColType</span><span class="sxs-lookup"><span data-stu-id="31dce-1601">eColType</span></span>  

<!-- -->

<span data-ttu-id="31dce-1602">eColRole</span><span class="sxs-lookup"><span data-stu-id="31dce-1602">eColRole</span></span>  

<!-- -->

<span data-ttu-id="31dce-1603">lColOrd</span><span class="sxs-lookup"><span data-stu-id="31dce-1603">lColOrd</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1604">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1604">Return Value</span></span>

### <a name="method-addcolumnmapping"></a><span data-ttu-id="31dce-1605">メソッド addColumnMapping</span><span class="sxs-lookup"><span data-stu-id="31dce-1605">Method addColumnMapping</span></span>

    public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)

#### <a name="parameters"></a><span data-ttu-id="31dce-1606">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1606">Parameters</span></span>

<span data-ttu-id="31dce-1607">szRefRecIdColName</span><span class="sxs-lookup"><span data-stu-id="31dce-1607">szRefRecIdColName</span></span>  

<!-- -->

<span data-ttu-id="31dce-1608">szRefTableIdColName</span><span class="sxs-lookup"><span data-stu-id="31dce-1608">szRefTableIdColName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1609">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1609">Return Value</span></span>

### <a name="method-hasequalitycriteria"></a><span data-ttu-id="31dce-1610">メソッド hasEqualityCriteria</span><span class="sxs-lookup"><span data-stu-id="31dce-1610">Method hasEqualityCriteria</span></span>

    public int hasEqualityCriteria(boolean fHasEqualityCriteria)

#### <a name="parameters"></a><span data-ttu-id="31dce-1611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1611">Parameters</span></span>

<span data-ttu-id="31dce-1612">fHasEqualityCriteria</span><span class="sxs-lookup"><span data-stu-id="31dce-1612">fHasEqualityCriteria</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1613">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1613">Return Value</span></span>

### <a name="method-shreddedmetadatatable"></a><span data-ttu-id="31dce-1614">メソッド shreddedMetadataTable</span><span class="sxs-lookup"><span data-stu-id="31dce-1614">Method shreddedMetadataTable</span></span>

    public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)

#### <a name="parameters"></a><span data-ttu-id="31dce-1615">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1615">Parameters</span></span>

<span data-ttu-id="31dce-1616">fIsShreddedMetadataTable</span><span class="sxs-lookup"><span data-stu-id="31dce-1616">fIsShreddedMetadataTable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1617">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1617">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1618">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1618">Method new</span></span>

<span data-ttu-id="31dce-1619">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1619">Initializes a new instance of the Object class.</span></span>

    public void new(int usTableId)

#### <a name="parameters"></a><span data-ttu-id="31dce-1620">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1620">Parameters</span></span>

<span data-ttu-id="31dce-1621">usTableId</span><span class="sxs-lookup"><span data-stu-id="31dce-1621">usTableId</span></span>  

## <a name="class-infopart"></a><span data-ttu-id="31dce-1622">クラス InfoPart</span><span class="sxs-lookup"><span data-stu-id="31dce-1622">Class InfoPart</span></span>
    class InfoPart extends TreeNode

### <a name="remarks"></a><span data-ttu-id="31dce-1623">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1623">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1624">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1624">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1625">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1625">Methods</span></span>

| <span data-ttu-id="31dce-1626">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1626">Method</span></span>                                   | <span data-ttu-id="31dce-1627">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1627">Description</span></span>                                                                                                                               |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-1628">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1628">public str caption(\[str value\])</span></span>        | <span data-ttu-id="31dce-1629">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1629">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="31dce-1630">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1630">public str changedBy(\[str value\])</span></span>      | <span data-ttu-id="31dce-1631">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1631">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="31dce-1632">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1632">public Date changedDate(\[Date value\])</span></span>  | <span data-ttu-id="31dce-1633">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1633">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="31dce-1634">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1634">public str changedTime(\[str value\])</span></span>    | <span data-ttu-id="31dce-1635">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1635">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="31dce-1636">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1636">public str createdBy(\[str value\])</span></span>      | <span data-ttu-id="31dce-1637">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1637">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="31dce-1638">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1638">public Date creationDate(\[Date value\])</span></span> | <span data-ttu-id="31dce-1639">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1639">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="31dce-1640">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1640">public str creationTime(\[str value\])</span></span>   |                                                                                                                                           |
| <span data-ttu-id="31dce-1641">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1641">public str name(\[str value\])</span></span>           | <span data-ttu-id="31dce-1642">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1642">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="31dce-1643">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1643">public Guid origin(\[Guid value\])</span></span>       |                                                                                                                                           |
| <span data-ttu-id="31dce-1644">public str query(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1644">public str query(\[str value\])</span></span>          |                                                                                                                                           |
| <span data-ttu-id="31dce-1645">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-1645">public void new()</span></span>                        | <span data-ttu-id="31dce-1646">InfoPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1646">Initializes a new instance of the InfoPart class.</span></span>                                                                                         |

### <a name="method-caption"></a><span data-ttu-id="31dce-1647">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="31dce-1647">Method caption</span></span>

<span data-ttu-id="31dce-1648">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1648">Gets or set the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1649">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1649">Parameters</span></span>

<span data-ttu-id="31dce-1650">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1650">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1651">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1651">Return Value</span></span>

<span data-ttu-id="31dce-1652">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="31dce-1652">The string that is used as the caption of the control.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="31dce-1653">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="31dce-1653">Method changedBy</span></span>

<span data-ttu-id="31dce-1654">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1654">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1655">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1655">Parameters</span></span>

<span data-ttu-id="31dce-1656">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1656">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1657">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1657">Return Value</span></span>

<span data-ttu-id="31dce-1658">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="31dce-1658">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="31dce-1659">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="31dce-1659">Method changedDate</span></span>

<span data-ttu-id="31dce-1660">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1660">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1661">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1661">Parameters</span></span>

<span data-ttu-id="31dce-1662">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1662">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1663">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1663">Return Value</span></span>

<span data-ttu-id="31dce-1664">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="31dce-1664">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="31dce-1665">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="31dce-1665">Method changedTime</span></span>

<span data-ttu-id="31dce-1666">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1666">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1667">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1667">Parameters</span></span>

<span data-ttu-id="31dce-1668">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1668">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1669">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1669">Return Value</span></span>

<span data-ttu-id="31dce-1670">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="31dce-1670">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="31dce-1671">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="31dce-1671">Method createdBy</span></span>

<span data-ttu-id="31dce-1672">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1672">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1673">Parameters</span></span>

<span data-ttu-id="31dce-1674">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1674">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1675">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1675">Return Value</span></span>

<span data-ttu-id="31dce-1676">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="31dce-1676">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="31dce-1677">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="31dce-1677">Method creationDate</span></span>

<span data-ttu-id="31dce-1678">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1678">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1679">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1679">Parameters</span></span>

<span data-ttu-id="31dce-1680">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1680">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1681">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1681">Return Value</span></span>

<span data-ttu-id="31dce-1682">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="31dce-1682">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="31dce-1683">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="31dce-1683">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1684">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1684">Parameters</span></span>

<span data-ttu-id="31dce-1685">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1685">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1686">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1686">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="31dce-1687">メソッド名</span><span class="sxs-lookup"><span data-stu-id="31dce-1687">Method name</span></span>

<span data-ttu-id="31dce-1688">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1688">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1689">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1689">Parameters</span></span>

<span data-ttu-id="31dce-1690">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1690">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1691">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1691">Return Value</span></span>

<span data-ttu-id="31dce-1692">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="31dce-1692">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1693">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1693">Remarks</span></span>

<span data-ttu-id="31dce-1694">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1694">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="31dce-1695">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1695">Begins with a letter.</span></span>
-   <span data-ttu-id="31dce-1696">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="31dce-1696">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="31dce-1697">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1697">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="31dce-1698">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1698">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="31dce-1699">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1699">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="31dce-1700">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="31dce-1700">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1701">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1701">Parameters</span></span>

<span data-ttu-id="31dce-1702">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1702">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1703">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1703">Return Value</span></span>

### <a name="method-query"></a><span data-ttu-id="31dce-1704">メソッド query</span><span class="sxs-lookup"><span data-stu-id="31dce-1704">Method query</span></span>

    public str query([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1705">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1705">Parameters</span></span>

<span data-ttu-id="31dce-1706">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1706">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1707">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1707">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1708">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1708">Method new</span></span>

<span data-ttu-id="31dce-1709">InfoPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1709">Initializes a new instance of the InfoPart class.</span></span>

    public void new()

## <a name="class-infopartfield"></a><span data-ttu-id="31dce-1710">クラス InfoPartField</span><span class="sxs-lookup"><span data-stu-id="31dce-1710">Class InfoPartField</span></span>
    class InfoPartField extends TreeNode

### <a name="remarks"></a><span data-ttu-id="31dce-1711">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1711">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1712">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1712">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1713">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1713">Methods</span></span>

| <span data-ttu-id="31dce-1714">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1714">Method</span></span>                                            | <span data-ttu-id="31dce-1715">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1715">Description</span></span>                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-1716">public str dataField(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1716">public str dataField(\[str value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="31dce-1717">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1717">public str dataMethod(\[str value\])</span></span>              |                                                                                                                                           |
| <span data-ttu-id="31dce-1718">public str dataSource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1718">public str dataSource(\[str value\])</span></span>              | <span data-ttu-id="31dce-1719">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1719">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="31dce-1720">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1720">public str label(\[str value\])</span></span>                   | <span data-ttu-id="31dce-1721">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1721">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="31dce-1722">public boolean manualRetrieval(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1722">public boolean manualRetrieval(\[boolean value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="31dce-1723">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1723">public str name(\[str value\])</span></span>                    | <span data-ttu-id="31dce-1724">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1724">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="31dce-1725">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1725">public int style(\[int value\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="31dce-1726">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-1726">public void new()</span></span>                                 | <span data-ttu-id="31dce-1727">InfoPartField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1727">Initializes a new instance of the InfoPartField class.</span></span>                                                                                    |

### <a name="method-datafield"></a><span data-ttu-id="31dce-1728">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="31dce-1728">Method dataField</span></span>

    public str dataField([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1729">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1729">Parameters</span></span>

<span data-ttu-id="31dce-1730">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1730">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1731">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1731">Return Value</span></span>

### <a name="method-datamethod"></a><span data-ttu-id="31dce-1732">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="31dce-1732">Method dataMethod</span></span>

    public str dataMethod([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1733">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1733">Parameters</span></span>

<span data-ttu-id="31dce-1734">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1734">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1735">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1735">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="31dce-1736">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="31dce-1736">Method dataSource</span></span>

<span data-ttu-id="31dce-1737">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1737">Gets or sets a data source that will be used by the control or the form.</span></span>

    public str dataSource([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1738">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1738">Parameters</span></span>

<span data-ttu-id="31dce-1739">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1739">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1740">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1740">Return Value</span></span>

<span data-ttu-id="31dce-1741">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="31dce-1741">The identifier of the data source that will be used.</span></span>

### <a name="method-label"></a><span data-ttu-id="31dce-1742">メソッド label</span><span class="sxs-lookup"><span data-stu-id="31dce-1742">Method label</span></span>

<span data-ttu-id="31dce-1743">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1743">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1744">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1744">Parameters</span></span>

<span data-ttu-id="31dce-1745">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1745">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1746">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1746">Return Value</span></span>

<span data-ttu-id="31dce-1747">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="31dce-1747">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1748">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1748">Remarks</span></span>

<span data-ttu-id="31dce-1749">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1749">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="31dce-1750">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1750">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-manualretrieval"></a><span data-ttu-id="31dce-1751">メソッド manualRetrieval</span><span class="sxs-lookup"><span data-stu-id="31dce-1751">Method manualRetrieval</span></span>

    public boolean manualRetrieval([boolean value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1752">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1752">Parameters</span></span>

<span data-ttu-id="31dce-1753">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1753">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1754">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1754">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="31dce-1755">メソッド名</span><span class="sxs-lookup"><span data-stu-id="31dce-1755">Method name</span></span>

<span data-ttu-id="31dce-1756">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1756">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1757">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1757">Parameters</span></span>

<span data-ttu-id="31dce-1758">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1758">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1759">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1759">Return Value</span></span>

<span data-ttu-id="31dce-1760">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="31dce-1760">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1761">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1761">Remarks</span></span>

<span data-ttu-id="31dce-1762">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1762">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="31dce-1763">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1763">Begins with a letter.</span></span>
-   <span data-ttu-id="31dce-1764">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="31dce-1764">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="31dce-1765">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1765">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="31dce-1766">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1766">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="31dce-1767">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1767">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-style"></a><span data-ttu-id="31dce-1768">メソッド style</span><span class="sxs-lookup"><span data-stu-id="31dce-1768">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1769">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1769">Parameters</span></span>

<span data-ttu-id="31dce-1770">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1770">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1771">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1771">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1772">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1772">Method new</span></span>

<span data-ttu-id="31dce-1773">InfoPartField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1773">Initializes a new instance of the InfoPartField class.</span></span>

    public void new()

## <a name="class-infopartgroup"></a><span data-ttu-id="31dce-1774">クラス InfoPartGroup</span><span class="sxs-lookup"><span data-stu-id="31dce-1774">Class InfoPartGroup</span></span>
    class InfoPartGroup extends TreeNode

### <a name="remarks"></a><span data-ttu-id="31dce-1775">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1775">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1776">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1776">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1777">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1777">Methods</span></span>

| <span data-ttu-id="31dce-1778">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1778">Method</span></span>                                                         | <span data-ttu-id="31dce-1779">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1779">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-1780">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1780">public str caption(\[str value\])</span></span>                              | <span data-ttu-id="31dce-1781">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1781">Gets or sets the caption of the control.</span></span>                                                                                                      |
| <span data-ttu-id="31dce-1782">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1782">public str dataGroup(\[str value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="31dce-1783">public str dataSource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1783">public str dataSource(\[str value\])</span></span>                           | <span data-ttu-id="31dce-1784">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1784">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                      |
| <span data-ttu-id="31dce-1785">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1785">public int labelPosition(\[int value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="31dce-1786">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1786">public str name(\[str value\])</span></span>                                 | <span data-ttu-id="31dce-1787">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1787">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="31dce-1788">public boolean repeating(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1788">public boolean repeating(\[boolean value\])</span></span>                    |                                                                                                                                               |
| <span data-ttu-id="31dce-1789">public int rowCountWhenSmall(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1789">public int rowCountWhenSmall(\[int value\], \[AutoMode mode\])</span></span> |                                                                                                                                               |
| <span data-ttu-id="31dce-1790">public AutoMode rowCountWhenSmallMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1790">public AutoMode rowCountWhenSmallMode(\[AutoMode mode\])</span></span>       |                                                                                                                                               |
| <span data-ttu-id="31dce-1791">public int rowCountWhenSmallValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1791">public int rowCountWhenSmallValue(\[int value\])</span></span>               |                                                                                                                                               |
| <span data-ttu-id="31dce-1792">public boolean showCaption(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1792">public boolean showCaption(\[boolean value\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="31dce-1793">public boolean showLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1793">public boolean showLabels(\[boolean value\])</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="31dce-1794">public int showWhenPartSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1794">public int showWhenPartSize(\[int value\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="31dce-1795">public boolean verticalSpacing(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1795">public boolean verticalSpacing(\[boolean value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="31dce-1796">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-1796">public void new()</span></span>                                              | <span data-ttu-id="31dce-1797">InfoPartGroup クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1797">Initializes a new instance of the InfoPartGroup class.</span></span>                                                                                        |

### <a name="method-caption"></a><span data-ttu-id="31dce-1798">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="31dce-1798">Method caption</span></span>

<span data-ttu-id="31dce-1799">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1799">Gets or sets the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1800">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1800">Parameters</span></span>

<span data-ttu-id="31dce-1801">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1801">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1802">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1802">Return Value</span></span>

<span data-ttu-id="31dce-1803">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="31dce-1803">The string that is used as the caption of the control.</span></span>

### <a name="method-datagroup"></a><span data-ttu-id="31dce-1804">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="31dce-1804">Method dataGroup</span></span>

    public str dataGroup([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1805">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1805">Parameters</span></span>

<span data-ttu-id="31dce-1806">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1806">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1807">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1807">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="31dce-1808">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="31dce-1808">Method dataSource</span></span>

<span data-ttu-id="31dce-1809">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1809">Gets or sets a data source that will be used by the control or the form.</span></span>

    public str dataSource([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1810">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1810">Parameters</span></span>

<span data-ttu-id="31dce-1811">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1811">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1812">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1812">Return Value</span></span>

<span data-ttu-id="31dce-1813">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="31dce-1813">The identifier of the data source that will be used.</span></span>

### <a name="method-labelposition"></a><span data-ttu-id="31dce-1814">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="31dce-1814">Method labelPosition</span></span>

    public int labelPosition([int value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1815">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1815">Parameters</span></span>

<span data-ttu-id="31dce-1816">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1816">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1817">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1817">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="31dce-1818">メソッド名</span><span class="sxs-lookup"><span data-stu-id="31dce-1818">Method name</span></span>

<span data-ttu-id="31dce-1819">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1819">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1820">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1820">Parameters</span></span>

<span data-ttu-id="31dce-1821">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1821">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1822">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1822">Return Value</span></span>

<span data-ttu-id="31dce-1823">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="31dce-1823">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1824">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1824">Remarks</span></span>

<span data-ttu-id="31dce-1825">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1825">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="31dce-1826">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1826">Begins with a letter.</span></span>
-   <span data-ttu-id="31dce-1827">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="31dce-1827">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="31dce-1828">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1828">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="31dce-1829">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1829">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="31dce-1830">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="31dce-1830">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-repeating"></a><span data-ttu-id="31dce-1831">メソッド repeating</span><span class="sxs-lookup"><span data-stu-id="31dce-1831">Method repeating</span></span>

    public boolean repeating([boolean value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1832">Parameters</span></span>

<span data-ttu-id="31dce-1833">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1833">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1834">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1834">Return Value</span></span>

### <a name="method-rowcountwhensmall"></a><span data-ttu-id="31dce-1835">メソッド rowCountWhenSmall</span><span class="sxs-lookup"><span data-stu-id="31dce-1835">Method rowCountWhenSmall</span></span>

    public int rowCountWhenSmall([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="31dce-1836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1836">Parameters</span></span>

<span data-ttu-id="31dce-1837">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1837">value</span></span>  

<!-- -->

<span data-ttu-id="31dce-1838">モード</span><span class="sxs-lookup"><span data-stu-id="31dce-1838">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1839">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1839">Return Value</span></span>

### <a name="method-rowcountwhensmallmode"></a><span data-ttu-id="31dce-1840">メソッド rowCountWhenSmallMode</span><span class="sxs-lookup"><span data-stu-id="31dce-1840">Method rowCountWhenSmallMode</span></span>

    public AutoMode rowCountWhenSmallMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="31dce-1841">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1841">Parameters</span></span>

<span data-ttu-id="31dce-1842">モード</span><span class="sxs-lookup"><span data-stu-id="31dce-1842">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1843">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1843">Return Value</span></span>

### <a name="method-rowcountwhensmallvalue"></a><span data-ttu-id="31dce-1844">メソッド rowCountWhenSmallValue</span><span class="sxs-lookup"><span data-stu-id="31dce-1844">Method rowCountWhenSmallValue</span></span>

    public int rowCountWhenSmallValue([int value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1845">Parameters</span></span>

<span data-ttu-id="31dce-1846">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1846">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1847">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1847">Return Value</span></span>

### <a name="method-showcaption"></a><span data-ttu-id="31dce-1848">メソッド showCaption</span><span class="sxs-lookup"><span data-stu-id="31dce-1848">Method showCaption</span></span>

    public boolean showCaption([boolean value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1849">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1849">Parameters</span></span>

<span data-ttu-id="31dce-1850">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1850">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1851">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1851">Return Value</span></span>

### <a name="method-showlabels"></a><span data-ttu-id="31dce-1852">メソッド showLabels</span><span class="sxs-lookup"><span data-stu-id="31dce-1852">Method showLabels</span></span>

    public boolean showLabels([boolean value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1853">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1853">Parameters</span></span>

<span data-ttu-id="31dce-1854">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1854">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1855">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1855">Return Value</span></span>

### <a name="method-showwhenpartsize"></a><span data-ttu-id="31dce-1856">メソッド showWhenPartSize</span><span class="sxs-lookup"><span data-stu-id="31dce-1856">Method showWhenPartSize</span></span>

    public int showWhenPartSize([int value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1857">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1857">Parameters</span></span>

<span data-ttu-id="31dce-1858">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1858">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1859">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1859">Return Value</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="31dce-1860">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="31dce-1860">Method verticalSpacing</span></span>

    public boolean verticalSpacing([boolean value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1861">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1861">Parameters</span></span>

<span data-ttu-id="31dce-1862">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1862">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1863">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1863">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1864">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1864">Method new</span></span>

<span data-ttu-id="31dce-1865">InfoPartGroup クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1865">Initializes a new instance of the InfoPartGroup class.</span></span>

    public void new()

## <a name="class-infopartlayout"></a><span data-ttu-id="31dce-1866">クラス InfoPartLayout</span><span class="sxs-lookup"><span data-stu-id="31dce-1866">Class InfoPartLayout</span></span>
    class InfoPartLayout extends TreeNode

### <a name="remarks"></a><span data-ttu-id="31dce-1867">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1867">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1868">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1868">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1869">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1869">Methods</span></span>

| <span data-ttu-id="31dce-1870">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1870">Method</span></span>                                       | <span data-ttu-id="31dce-1871">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1871">Description</span></span>                                             |
|----------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="31dce-1872">public boolean showMore(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1872">public boolean showMore(\[boolean value\])</span></span>   |                                                         |
| <span data-ttu-id="31dce-1873">public str showMoreDataSource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1873">public str showMoreDataSource(\[str value\])</span></span> |                                                         |
| <span data-ttu-id="31dce-1874">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-1874">public void new()</span></span>                            | <span data-ttu-id="31dce-1875">InfoPartLayout クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1875">Initializes a new instance of the InfoPartLayout class.</span></span> |

### <a name="method-showmore"></a><span data-ttu-id="31dce-1876">メソッド showMore</span><span class="sxs-lookup"><span data-stu-id="31dce-1876">Method showMore</span></span>

    public boolean showMore([boolean value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1877">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1877">Parameters</span></span>

<span data-ttu-id="31dce-1878">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1878">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1879">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1879">Return Value</span></span>

### <a name="method-showmoredatasource"></a><span data-ttu-id="31dce-1880">メソッド showMoreDataSource</span><span class="sxs-lookup"><span data-stu-id="31dce-1880">Method showMoreDataSource</span></span>

    public str showMoreDataSource([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-1881">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1881">Parameters</span></span>

<span data-ttu-id="31dce-1882">値</span><span class="sxs-lookup"><span data-stu-id="31dce-1882">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1883">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1883">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1884">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1884">Method new</span></span>

<span data-ttu-id="31dce-1885">InfoPartLayout クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1885">Initializes a new instance of the InfoPartLayout class.</span></span>

    public void new()

## <a name="class-initialqueryparameter"></a><span data-ttu-id="31dce-1886">クラス InitialQueryParameter</span><span class="sxs-lookup"><span data-stu-id="31dce-1886">Class InitialQueryParameter</span></span>
    class InitialQueryParameter extends Object

### <a name="remarks"></a><span data-ttu-id="31dce-1887">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1887">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1888">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1888">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1889">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1889">Methods</span></span>

| <span data-ttu-id="31dce-1890">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1890">Method</span></span>                                                                                                       | <span data-ttu-id="31dce-1891">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1891">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="31dce-1892">public boolean applyQuery(FormDataSource datasource)</span><span class="sxs-lookup"><span data-stu-id="31dce-1892">public boolean applyQuery(FormDataSource datasource)</span></span>                                                         |                                                                |
| <span data-ttu-id="31dce-1893">public str dataSourceName(\[str dataSourceName\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1893">public str dataSourceName(\[str dataSourceName\])</span></span>                                                            |                                                                |
| <span data-ttu-id="31dce-1894">public str modeledQueryName(\[str modeledQueryName\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1894">public str modeledQueryName(\[str modeledQueryName\])</span></span>                                                        |                                                                |
| <span data-ttu-id="31dce-1895">public Query query(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1895">public Query query(\[Query query\])</span></span>                                                                          |                                                                |
| <span data-ttu-id="31dce-1896">::public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, \[str dataSourceName\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1896">::public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, \[str dataSourceName\])</span></span> |                                                                |
| <span data-ttu-id="31dce-1897">::public static InitialQueryParameter createByQuery(Query query, \[str dataSourceName\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1897">::public static InitialQueryParameter createByQuery(Query query, \[str dataSourceName\])</span></span>                     |                                                                |
| <span data-ttu-id="31dce-1898">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-1898">public void finalize()</span></span>                                                                                       |                                                                |
| <span data-ttu-id="31dce-1899">public void new()</span><span class="sxs-lookup"><span data-stu-id="31dce-1899">public void new()</span></span>                                                                                            | <span data-ttu-id="31dce-1900">InitialQueryParameter クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1900">Initializes a new instance of the InitialQueryParameter class.</span></span> |

### <a name="method-applyquery"></a><span data-ttu-id="31dce-1901">メソッド applyQuery</span><span class="sxs-lookup"><span data-stu-id="31dce-1901">Method applyQuery</span></span>

    public boolean applyQuery(FormDataSource datasource)

#### <a name="parameters"></a><span data-ttu-id="31dce-1902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1902">Parameters</span></span>

<span data-ttu-id="31dce-1903">datasource</span><span class="sxs-lookup"><span data-stu-id="31dce-1903">datasource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1904">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1904">Return Value</span></span>

### <a name="method-datasourcename"></a><span data-ttu-id="31dce-1905">メソッド dataSourceName</span><span class="sxs-lookup"><span data-stu-id="31dce-1905">Method dataSourceName</span></span>

    public str dataSourceName([str dataSourceName])

#### <a name="parameters"></a><span data-ttu-id="31dce-1906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1906">Parameters</span></span>

<span data-ttu-id="31dce-1907">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="31dce-1907">dataSourceName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1908">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1908">Return Value</span></span>

### <a name="method-modeledqueryname"></a><span data-ttu-id="31dce-1909">メソッド modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="31dce-1909">Method modeledQueryName</span></span>

    public str modeledQueryName([str modeledQueryName])

#### <a name="parameters"></a><span data-ttu-id="31dce-1910">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1910">Parameters</span></span>

<span data-ttu-id="31dce-1911">modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="31dce-1911">modeledQueryName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1912">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1912">Return Value</span></span>

### <a name="method-query"></a><span data-ttu-id="31dce-1913">メソッド query</span><span class="sxs-lookup"><span data-stu-id="31dce-1913">Method query</span></span>

    public Query query([Query query])

#### <a name="parameters"></a><span data-ttu-id="31dce-1914">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1914">Parameters</span></span>

<span data-ttu-id="31dce-1915">クエリ</span><span class="sxs-lookup"><span data-stu-id="31dce-1915">query</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1916">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1916">Return Value</span></span>

### <a name="method-createbymodeledqueryname"></a><span data-ttu-id="31dce-1917">メソッド createByModeledQueryName</span><span class="sxs-lookup"><span data-stu-id="31dce-1917">Method createByModeledQueryName</span></span>

    public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, [str dataSourceName])

#### <a name="parameters"></a><span data-ttu-id="31dce-1918">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1918">Parameters</span></span>

<span data-ttu-id="31dce-1919">modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="31dce-1919">modeledQueryName</span></span>  

<!-- -->

<span data-ttu-id="31dce-1920">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="31dce-1920">dataSourceName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1921">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1921">Return Value</span></span>

### <a name="method-createbyquery"></a><span data-ttu-id="31dce-1922">メソッド createByQuery</span><span class="sxs-lookup"><span data-stu-id="31dce-1922">Method createByQuery</span></span>

    public static InitialQueryParameter createByQuery(Query query, [str dataSourceName])

#### <a name="parameters"></a><span data-ttu-id="31dce-1923">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1923">Parameters</span></span>

<span data-ttu-id="31dce-1924">クエリ</span><span class="sxs-lookup"><span data-stu-id="31dce-1924">query</span></span>  

<!-- -->

<span data-ttu-id="31dce-1925">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="31dce-1925">dataSourceName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-1926">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1926">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="31dce-1927">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-1927">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="31dce-1928">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1928">Method new</span></span>

<span data-ttu-id="31dce-1929">InitialQueryParameter クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1929">Initializes a new instance of the InitialQueryParameter class.</span></span>

    public void new()

## <a name="class-interoppermission"></a><span data-ttu-id="31dce-1930">クラス InteropPermission</span><span class="sxs-lookup"><span data-stu-id="31dce-1930">Class InteropPermission</span></span>
    class InteropPermission extends CodeAccessPermission

<span data-ttu-id="31dce-1931">InteropPermission クラスは、アンマネージド コードとマネージド コードを呼び出す機能を制御します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1931">The InteropPermission class controls the ability to call unmanaged and managed code.</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-1932">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1932">Remarks</span></span>

<span data-ttu-id="31dce-1933">InteropPermission クラスは、特定の API のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="31dce-1933">The InteropPermission class is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="31dce-1934">アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-1934">For a list of all APIs that are protected by permissions, see Secured APIs.</span></span> <span data-ttu-id="31dce-1935">保護された API を実行する前に、対応する CodeAccessPermission::demand メソッドが呼び出されている同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1935">Before the protected API is run, you must call the assert method on the same tier (usually the server tier) that the corresponding CodeAccessPermission::demand method is called on.</span></span> <span data-ttu-id="31dce-1936">次のいずれかの方法でサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="31dce-1936">Call a method on the server tier from one of the following methods:</span></span>

-   <span data-ttu-id="31dce-1937">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1937">A server static method</span></span>
-   <span data-ttu-id="31dce-1938">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。</span><span class="sxs-lookup"><span data-stu-id="31dce-1938">A class instance method that is set to run on the server by using the RunOn class property.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1939">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1939">Examples</span></span>

<span data-ttu-id="31dce-1940">次のコード例は、InteropPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="31dce-1940">The following code example shows a new instance of the InteropPermission class.</span></span> <span data-ttu-id="31dce-1941">assert メソッドが呼び出され、コードが、Microsoft Windows ダイナミックリンク ライブラリ (DLL) と通信する機能を提供する DLL クラスをインスタンス化できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-1941">The assert method is called to declare that the code can then instantiate the DLL class that provides the ability to communicate with a Microsoft Windows dynamic-link library (DLL).</span></span>

    server static void main(Args args) 
    { 
        InteropPermission _perm; 
        DLL _dll; 
        _perm = new InteropPermission(InteropKind::DllInterop); 
        _perm.assert(); 
        // Invoke the protected API. 
        _dll = new DLL('cfx2032.dll'); 
        // Optionally, call revertAssert() to limit the scope of assert. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a><span data-ttu-id="31dce-1942">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1942">Methods</span></span>

| <span data-ttu-id="31dce-1943">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1943">Method</span></span>                                                 | <span data-ttu-id="31dce-1944">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1944">Description</span></span>                                                                        |
|--------------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-1945">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="31dce-1945">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="31dce-1946">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1946">Creates and returns a copy of the current permission class object.</span></span>                 |
| <span data-ttu-id="31dce-1947">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="31dce-1947">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="31dce-1948">現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1948">Determines whether the current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="31dce-1949">public void new(InteropKind kind)</span><span class="sxs-lookup"><span data-stu-id="31dce-1949">public void new(InteropKind kind)</span></span>                      | <span data-ttu-id="31dce-1950">InteropPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1950">Creates a new instance of the InteropPermission class.</span></span>                            |

### <a name="method-copy"></a><span data-ttu-id="31dce-1951">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="31dce-1951">Method copy</span></span>

<span data-ttu-id="31dce-1952">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1952">Creates and returns a copy of the current permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="31dce-1953">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1953">Return Value</span></span>

<span data-ttu-id="31dce-1954">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="31dce-1954">A copy of the current permission object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1955">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1955">Remarks</span></span>

<span data-ttu-id="31dce-1956">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1956">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="31dce-1957">詳細については、「メソッドのコピー」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-1957">For more information, see the copy method.</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="31dce-1958">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="31dce-1958">Method isSubsetOf</span></span>

<span data-ttu-id="31dce-1959">現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1959">Determines whether the current permission is a subset of the specified permission.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="31dce-1960">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1960">Parameters</span></span>

<span data-ttu-id="31dce-1961">target</span><span class="sxs-lookup"><span data-stu-id="31dce-1961">target</span></span>  
<span data-ttu-id="31dce-1962">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="31dce-1962">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-1963">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-1963">Return Value</span></span>

<span data-ttu-id="31dce-1964">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31dce-1964">true if the current permission is a subset of the specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-1965">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1965">Remarks</span></span>

<span data-ttu-id="31dce-1966">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="31dce-1966">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="31dce-1967">詳細については、「isSubsetOf メソッド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-1967">For more information, see the isSubsetOf method.</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-1968">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-1968">Method new</span></span>

<span data-ttu-id="31dce-1969">InteropPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1969">Creates a new instance of the InteropPermission class.</span></span>

    public void new(InteropKind kind)

#### <a name="parameters"></a><span data-ttu-id="31dce-1970">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-1970">Parameters</span></span>

<span data-ttu-id="31dce-1971">kind</span><span class="sxs-lookup"><span data-stu-id="31dce-1971">kind</span></span>  
<span data-ttu-id="31dce-1972">マネージドまたはアンマネージド コードへのアクセスを指定する InteropKind システム列挙値です。</span><span class="sxs-lookup"><span data-stu-id="31dce-1972">An InteropKind system enumeration value that specifies access to managed or unmanaged code.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-1973">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1973">Examples</span></span>

<span data-ttu-id="31dce-1974">次のコード例は、Win32 DLL へのアクセス許可を指定する InteropPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="31dce-1974">The following code example shows a new instance of the InteropPermission class that specifies access to Win32 DLLs.</span></span>

    server static void main(Args args) 
    { 
        InteropPermission _perm; 
        _perm = new InteropPermission(InteropKind::DllInterop); 
    }

## <a name="class-io"></a><span data-ttu-id="31dce-1975">クラス入出力</span><span class="sxs-lookup"><span data-stu-id="31dce-1975">Class Io</span></span>
    class Io extends Object

<span data-ttu-id="31dce-1976">Io クラスは、外部ファイルにアクセスするための、ファイル固有の Io クラスの基本クラスとして機能します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1976">The Io class serves as the base class for the format-specific Io classes, which are used to access external files.</span></span>

### <a name="remarks"></a><span data-ttu-id="31dce-1977">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-1977">Remarks</span></span>

<span data-ttu-id="31dce-1978">基本的な Io クラスには、実際のデータ入出力機能はありませんが、形式固有の Io クラスの基本クラスとして動作します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1978">The basic Io class features no actual data I/O but works as base class for the format-specific Io classes.</span></span> <span data-ttu-id="31dce-1979">ここでは、すべての Io クラスに共通するメソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1979">The methods that are common to all Io classes are described here.</span></span> <span data-ttu-id="31dce-1980">形式固有の機能およびメンバー機能の動作については、各 I/O クラスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31dce-1980">For format-specific features and behavior of the member functions, refer to the documentation for each of the I/O classes.</span></span> <span data-ttu-id="31dce-1981">異なるフォーマットの外部ファイルの読み書きをサポートするため、MorphX はコンマで区切られたファイル、コンマで区切られた 7 ビット ファイル、バイナリ ファイル、およびプレーン テキスト ファイルのためのさまざまな Io クラスを備えています。</span><span class="sxs-lookup"><span data-stu-id="31dce-1981">To support reading and writing of different formats of external files, MorphX features a range of different Io classes for comma-separated files, for comma-separated 7 bit files, for binary files, and for plain-text files.</span></span>

### <a name="examples"></a><span data-ttu-id="31dce-1982">例</span><span class="sxs-lookup"><span data-stu-id="31dce-1982">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="31dce-1983">メソッド</span><span class="sxs-lookup"><span data-stu-id="31dce-1983">Methods</span></span>

| <span data-ttu-id="31dce-1984">方法</span><span class="sxs-lookup"><span data-stu-id="31dce-1984">Method</span></span>                                       | <span data-ttu-id="31dce-1985">説明</span><span class="sxs-lookup"><span data-stu-id="31dce-1985">Description</span></span>                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dce-1986">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1986">public str inFieldDelimiter(\[str value\])</span></span>   | <span data-ttu-id="31dce-1987">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1987">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>                                    |
| <span data-ttu-id="31dce-1988">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1988">public str inRecordDelimiter(\[str value\])</span></span>  | <span data-ttu-id="31dce-1989">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1989">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>  |
| <span data-ttu-id="31dce-1990">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1990">public int inRecordLength(\[int value\])</span></span>     | <span data-ttu-id="31dce-1991">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1991">Gets or sets the number of characters to read for each record in a file.</span></span>                                                     |
| <span data-ttu-id="31dce-1992">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1992">public str outFieldDelimiter(\[str value\])</span></span>  | <span data-ttu-id="31dce-1993">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1993">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>          |
| <span data-ttu-id="31dce-1994">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31dce-1994">public str outRecordDelimiter(\[str value\])</span></span> | <span data-ttu-id="31dce-1995">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1995">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span> |
| <span data-ttu-id="31dce-1996">public container read()</span><span class="sxs-lookup"><span data-stu-id="31dce-1996">public container read()</span></span>                      | <span data-ttu-id="31dce-1997">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="31dce-1997">Reads the next full record from the Io object.</span></span>                                                                               |
| <span data-ttu-id="31dce-1998">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="31dce-1998">public IO\_Status status()</span></span>                   | <span data-ttu-id="31dce-1999">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-1999">Retrieves the status of the last operation performed on the Io object.</span></span>                                                       |
| <span data-ttu-id="31dce-2000">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="31dce-2000">public boolean write(VarArg values)</span></span>          | <span data-ttu-id="31dce-2001">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2001">Writes values of a simple type.</span></span>                                                                                              |
| <span data-ttu-id="31dce-2002">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="31dce-2002">public boolean writeExp(container data)</span></span>      | <span data-ttu-id="31dce-2003">コンテナのコンテンツをそのファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2003">Writes the content of a container to the file.</span></span>                                                                               |
| <span data-ttu-id="31dce-2004">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="31dce-2004">public void finalize()</span></span>                       | <span data-ttu-id="31dce-2005">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="31dce-2005">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                                  |
| <span data-ttu-id="31dce-2006">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="31dce-2006">public void new(str filename, str mode)</span></span>      | <span data-ttu-id="31dce-2007">Io クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2007">Creates a new instance of the Io class.</span></span>                                                                                      |

### <a name="method-infielddelimiter"></a><span data-ttu-id="31dce-2008">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="31dce-2008">Method inFieldDelimiter</span></span>

<span data-ttu-id="31dce-2009">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2009">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-2010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2010">Parameters</span></span>

<span data-ttu-id="31dce-2011">値</span><span class="sxs-lookup"><span data-stu-id="31dce-2011">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-2012">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2012">Return Value</span></span>

<span data-ttu-id="31dce-2013">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。</span><span class="sxs-lookup"><span data-stu-id="31dce-2013">The delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

### <a name="method-inrecorddelimiter"></a><span data-ttu-id="31dce-2014">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="31dce-2014">Method inRecordDelimiter</span></span>

<span data-ttu-id="31dce-2015">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2015">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-2016">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2016">Parameters</span></span>

<span data-ttu-id="31dce-2017">値</span><span class="sxs-lookup"><span data-stu-id="31dce-2017">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-2018">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2018">Return Value</span></span>

<span data-ttu-id="31dce-2019">完全なレコードが読み込まれたかどうかを示す文字。</span><span class="sxs-lookup"><span data-stu-id="31dce-2019">The character or characters that indicate whether a full record has been read.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2020">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2020">Remarks</span></span>

<span data-ttu-id="31dce-2021">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="31dce-2021">For standard text, the delimiter is a newline character.</span></span>

### <a name="method-inrecordlength"></a><span data-ttu-id="31dce-2022">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="31dce-2022">Method inRecordLength</span></span>

<span data-ttu-id="31dce-2023">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2023">Gets or sets the number of characters to read for each record in a file.</span></span>

    public int inRecordLength([int value])

#### <a name="parameters"></a><span data-ttu-id="31dce-2024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2024">Parameters</span></span>

<span data-ttu-id="31dce-2025">値</span><span class="sxs-lookup"><span data-stu-id="31dce-2025">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-2026">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2026">Return Value</span></span>

<span data-ttu-id="31dce-2027">ファイル内の各レコードを読み取る文字数。</span><span class="sxs-lookup"><span data-stu-id="31dce-2027">The number of characters to read for each record in the file.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2028">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2028">Remarks</span></span>

<span data-ttu-id="31dce-2029">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2029">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="31dce-2030">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="31dce-2030">If the record format is overruled by a specified inRecordDelimiter property value , that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no additional data is read.</span></span> <span data-ttu-id="31dce-2031">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2031">To guarantee that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="31dce-2032">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="31dce-2032">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="31dce-2033">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2033">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

### <a name="method-outfielddelimiter"></a><span data-ttu-id="31dce-2034">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="31dce-2034">Method outFieldDelimiter</span></span>

<span data-ttu-id="31dce-2035">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2035">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-2036">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2036">Parameters</span></span>

<span data-ttu-id="31dce-2037">値</span><span class="sxs-lookup"><span data-stu-id="31dce-2037">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-2038">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2038">Return Value</span></span>

<span data-ttu-id="31dce-2039">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="31dce-2039">The sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

### <a name="method-outrecorddelimiter"></a><span data-ttu-id="31dce-2040">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="31dce-2040">Method outRecordDelimiter</span></span>

<span data-ttu-id="31dce-2041">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2041">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span>

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="31dce-2042">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2042">Parameters</span></span>

<span data-ttu-id="31dce-2043">値</span><span class="sxs-lookup"><span data-stu-id="31dce-2043">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="31dce-2044">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2044">Return Value</span></span>

<span data-ttu-id="31dce-2045">出力ファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="31dce-2045">The sequence of characters that is written to the output files.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2046">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2046">Remarks</span></span>

<span data-ttu-id="31dce-2047">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="31dce-2047">For standard text files, the delimiter is a newline character.</span></span>

### <a name="method-read"></a><span data-ttu-id="31dce-2048">メソッド read</span><span class="sxs-lookup"><span data-stu-id="31dce-2048">Method read</span></span>

<span data-ttu-id="31dce-2049">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="31dce-2049">Reads the next full record from the Io object.</span></span>

    public container read()

#### <a name="return-value"></a><span data-ttu-id="31dce-2050">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2050">Return Value</span></span>

<span data-ttu-id="31dce-2051">入出力オブジェクトから次の完全なレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="31dce-2051">A container that holds the next full record from the Io object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2052">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2052">Remarks</span></span>

<span data-ttu-id="31dce-2053">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2053">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength method properties.</span></span> <span data-ttu-id="31dce-2054">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2054">The record is returned as a container.</span></span> <span data-ttu-id="31dce-2055">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="31dce-2055">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="31dce-2056">それぞれの特殊な Io クラスは、inFieldDelimiter、inRecordDelimiter、および inRecordLength のデフォルト設定を使用し、最も一般的な形式の入出力を可能にします。</span><span class="sxs-lookup"><span data-stu-id="31dce-2056">Each of the specialized Io classes has default settings for inFieldDelimiter, inRecordDelimiter, and inRecordLength enabling input and output of the most common formats.</span></span> <span data-ttu-id="31dce-2057">目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="31dce-2057">You might have to adjust these to support the wanted format.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-2058">例</span><span class="sxs-lookup"><span data-stu-id="31dce-2058">Examples</span></span>

<span data-ttu-id="31dce-2059">このメソッドは、run メソッドの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2059">This method demonstrates the use of the run method.</span></span> <span data-ttu-id="31dce-2060">ただし、次の例は、クラス、フォーム、またはその他のオブジェクトのコンテキストで実行される必要があるため、ジョブはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="31dce-2060">However, the following example will not compile in a job as it must be run in the context of a class, form, or other object.</span></span>

    static void Job1(Args _args) 
    { 
        FileIoPermission _perm; 
        AsciiIo myfileio; 
        Container c; 
        _perm = new FileIoPermission("myfile.txt","r"); 
        myfileio = new AsciiIo("myfile.txt","r"); 
        while(myfileio.status()==IO_Status::OK) 
        { 
            c = myfileio.read(); 
            // ...do something with the container 
        } 
    }

### <a name="method-status"></a><span data-ttu-id="31dce-2061">メソッド status</span><span class="sxs-lookup"><span data-stu-id="31dce-2061">Method status</span></span>

<span data-ttu-id="31dce-2062">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2062">Retrieves the status of the last operation performed on the Io object.</span></span>

    public IO_Status status()

#### <a name="return-value"></a><span data-ttu-id="31dce-2063">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2063">Return Value</span></span>

<span data-ttu-id="31dce-2064">IO\_Status システム列挙値としての最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="31dce-2064">The status of the last operation, as an IO\_Status system enumeration value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2065">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2065">Remarks</span></span>

<span data-ttu-id="31dce-2066">返される可能性のある IO\_Status 値の範囲はクラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="31dce-2066">The range of possible IO\_Status values returned varies among Io Classes.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-2067">例</span><span class="sxs-lookup"><span data-stu-id="31dce-2067">Examples</span></span>

    static void myExample(Args _args) 
    { 
        Io myIo; 
        //.. create io object and perform some operations 
        if (myIo.status()==IO_Status::OK) 
        { 
            // ...go ahead - last operation was successful 
        } 
    }

### <a name="method-write"></a><span data-ttu-id="31dce-2068">メソッド write</span><span class="sxs-lookup"><span data-stu-id="31dce-2068">Method write</span></span>

<span data-ttu-id="31dce-2069">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2069">Writes values of a simple type.</span></span>

    public boolean write(VarArg values)

#### <a name="parameters"></a><span data-ttu-id="31dce-2070">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2070">Parameters</span></span>

<span data-ttu-id="31dce-2071">値</span><span class="sxs-lookup"><span data-stu-id="31dce-2071">values</span></span>  
<span data-ttu-id="31dce-2072">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="31dce-2072">The simple types are string, integer, real, enum, and date.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-2073">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2073">Return Value</span></span>

<span data-ttu-id="31dce-2074">書き込み操作が成功する場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31dce-2074">true if the write operation succeeds; otherwise false.</span></span> <span data-ttu-id="31dce-2075">書き込みが失敗した場合は、ステータス メソッドがその原因を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2075">If the write failed, the status method could be checked for the cause.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2076">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2076">Remarks</span></span>

<span data-ttu-id="31dce-2077">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2077">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="31dce-2078">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2078">Each value specified is put into the output record as a field.</span></span> <span data-ttu-id="31dce-2079">最初のフィールドとしての最初の引数、2 番目のフィールドとしての 2 番目の引数など。</span><span class="sxs-lookup"><span data-stu-id="31dce-2079">The first argument as the first field, the second argument as the second field, and so on.</span></span> <span data-ttu-id="31dce-2080">フィールドは、outFieldDelimiter メソッドで指定されたフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2080">The fields are separated with the field delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="31dce-2081">各レコードは、outRecordDelimiter 方法で区切られます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2081">Each record is separated by the outRecordDelimiter method.</span></span> <span data-ttu-id="31dce-2082">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2082">To write complete containers, use the writeExp method.</span></span>

### <a name="method-writeexp"></a><span data-ttu-id="31dce-2083">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="31dce-2083">Method writeExp</span></span>

<span data-ttu-id="31dce-2084">コンテナのコンテンツをそのファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2084">Writes the content of a container to the file.</span></span>

    public boolean writeExp(container data)

#### <a name="parameters"></a><span data-ttu-id="31dce-2085">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2085">Parameters</span></span>

<span data-ttu-id="31dce-2086">データ</span><span class="sxs-lookup"><span data-stu-id="31dce-2086">data</span></span>  
<span data-ttu-id="31dce-2087">レコードのデータを含むコンテナー。</span><span class="sxs-lookup"><span data-stu-id="31dce-2087">The container with data for the record.</span></span>

#### <a name="return-value"></a><span data-ttu-id="31dce-2088">戻り値</span><span class="sxs-lookup"><span data-stu-id="31dce-2088">Return Value</span></span>

<span data-ttu-id="31dce-2089">操作が成功した場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31dce-2089">true if the operation succeeded; otherwise false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2090">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2090">Remarks</span></span>

<span data-ttu-id="31dce-2091">このメソッドが false を返す場合、ステータス メソッドで原因を確認します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2091">If this method returns false, check the status method for the cause.</span></span> <span data-ttu-id="31dce-2092">コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2092">The entries in the container are treated as fields, and the container is treated as a full record.</span></span> <span data-ttu-id="31dce-2093">フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。</span><span class="sxs-lookup"><span data-stu-id="31dce-2093">The field separator is defined in the outFieldDelimiter method.</span></span> <span data-ttu-id="31dce-2094">レコード区切りは outRecordDelimiter メソッドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2094">The record separator is defined in the outRecordDelimiter method.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-2095">例</span><span class="sxs-lookup"><span data-stu-id="31dce-2095">Examples</span></span>

    static void testMethod(Args _args) 
    { 
        FileIOPermission _perm; 
        container c; 
        CommaIo myfile; 
        _perm = new FileIOPermission("myfile.txt","w"); 
        _perm.assert(); 
        myfile = new CommaIo("myfile.txt","w"); 
        // Assign the entries in the container according to record layout. 
        c = [1,"MyText",1.324,"Last field"]; 
        // write this record according to file format (record/field delimiters). 
        myfile.writeExp(c); 
    }

### <a name="method-finalize"></a><span data-ttu-id="31dce-2096">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="31dce-2096">Method finalize</span></span>

<span data-ttu-id="31dce-2097">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="31dce-2097">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

    public void finalize()

#### <a name="remarks"></a><span data-ttu-id="31dce-2098">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2098">Remarks</span></span>

<span data-ttu-id="31dce-2099">オブジェクトは、通常、スコープから離れることによって確定されるため、確定は通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="31dce-2099">The object is typically finalized by leaving the scope, so finalize is typically not called directly.</span></span> <span data-ttu-id="31dce-2100">記述された出力はオブジェクトの終了前は無効です。</span><span class="sxs-lookup"><span data-stu-id="31dce-2100">Written output will not be valid before the object is finalized.</span></span>

### <a name="method-new"></a><span data-ttu-id="31dce-2101">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31dce-2101">Method new</span></span>

<span data-ttu-id="31dce-2102">Io クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2102">Creates a new instance of the Io class.</span></span>

    public void new(str filename, str mode)

#### <a name="parameters"></a><span data-ttu-id="31dce-2103">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31dce-2103">Parameters</span></span>

<span data-ttu-id="31dce-2104">filename</span><span class="sxs-lookup"><span data-stu-id="31dce-2104">filename</span></span>  
<span data-ttu-id="31dce-2105">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="31dce-2105">The mode in which the file should be opened.</span></span>

<!-- -->

<span data-ttu-id="31dce-2106">モード</span><span class="sxs-lookup"><span data-stu-id="31dce-2106">mode</span></span>  
<span data-ttu-id="31dce-2107">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="31dce-2107">The mode in which the file should be opened.</span></span>

#### <a name="remarks"></a><span data-ttu-id="31dce-2108">備考</span><span class="sxs-lookup"><span data-stu-id="31dce-2108">Remarks</span></span>

<span data-ttu-id="31dce-2109">mode パラメーターは、次のモードのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="31dce-2109">The mode parameter can be one of the following modes:</span></span>

-   <span data-ttu-id="31dce-2110">R – 読み取り</span><span class="sxs-lookup"><span data-stu-id="31dce-2110">R – read</span></span>
-   <span data-ttu-id="31dce-2111">W – 書き込み</span><span class="sxs-lookup"><span data-stu-id="31dce-2111">W – write</span></span>
-   <span data-ttu-id="31dce-2112">A – 追加 (意味 W)</span><span class="sxs-lookup"><span data-stu-id="31dce-2112">A – append (implies W)</span></span>
-   <span data-ttu-id="31dce-2113">T – 翻訳 (テキスト)</span><span class="sxs-lookup"><span data-stu-id="31dce-2113">T – translate (text)</span></span>
-   <span data-ttu-id="31dce-2114">B – バイナリ</span><span class="sxs-lookup"><span data-stu-id="31dce-2114">B – binary</span></span>

<span data-ttu-id="31dce-2115">ランタイム エラーは、現在開いているモードに対応しないメソッドでファイルにアクセスすると発生します (たとえば、読み取りモード ファイルに書き込もうとした場合など)。</span><span class="sxs-lookup"><span data-stu-id="31dce-2115">A run-time error occurs if the file is accessed with a method that does not correspond to the current opened mode (for example, if an attempt is made to write to a read-mode file).</span></span> <span data-ttu-id="31dce-2116">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2116">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="31dce-2117">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2117">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="31dce-2118">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="31dce-2118">Calls to this method on the server require permission.</span></span> <span data-ttu-id="31dce-2119">.</span><span class="sxs-lookup"><span data-stu-id="31dce-2119">.</span></span> <span data-ttu-id="31dce-2120">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="31dce-2120">Ensure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="31dce-2121">例</span><span class="sxs-lookup"><span data-stu-id="31dce-2121">Examples</span></span>

<span data-ttu-id="31dce-2122">この例では、Io クラスを使用して ExampleFile に書き込みます。</span><span class="sxs-lookup"><span data-stu-id="31dce-2122">This example uses the Io class to write to ExampleFile.</span></span>

    void IoExample() 
    { 
        Io io; 
        container con; 
        FileIoPermission perm; 
        #define.ExampleFile(@"c:\test.txt") 
        #define.ExampleOpenMode("w") 
        // Grants permission to execute the 
        // Io.new method. 
        // Io.new runs under code access security. 
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
        io = new Io(#ExampleFile, #ExampleOpenMode); 
        if (io != null) 
        { 
            io.write("Test"); 
        } 
        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }



