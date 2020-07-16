---
title: XDSServices クラス
description: このトピックでは、XDSServices クラスについて説明します。
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
ms.openlocfilehash: 75e51246809898b3c85be2a8c19f40fb4fe87352
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502684"
---
# <a name="class-xdsservices"></a><span data-ttu-id="35626-103">クラス XDSServices</span><span class="sxs-lookup"><span data-stu-id="35626-103">Class XDSServices</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class XDSServices extends Object
```

<span data-ttu-id="35626-104">XDSServices クラスは、拡張可能なデータ セキュリティ (XDS) 動作を管理するための API を提供します。</span><span class="sxs-lookup"><span data-stu-id="35626-104">The XDSServices class provides APIs to manage the extensible data security (XDS) behavior.</span></span>

## <a name="remarks"></a><span data-ttu-id="35626-105">備考</span><span class="sxs-lookup"><span data-stu-id="35626-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="35626-106">例</span><span class="sxs-lookup"><span data-stu-id="35626-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="35626-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="35626-107">Methods</span></span>

| <span data-ttu-id="35626-108">方法</span><span class="sxs-lookup"><span data-stu-id="35626-108">Method</span></span>                                                                 | <span data-ttu-id="35626-109">説明</span><span class="sxs-lookup"><span data-stu-id="35626-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35626-110">public int flushXDSMyConstructs(int reserved, str tablename)</span><span class="sxs-lookup"><span data-stu-id="35626-110">public int flushXDSMyConstructs(int reserved, str tablename)</span></span>           | <span data-ttu-id="35626-111">XDS で使用される MyConstruct テーブルをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="35626-111">Flushes the MyConstruct table that is used with XDS.</span></span>                                                                              |
| <span data-ttu-id="35626-112">public str getQuerySQL(str queryname)</span><span class="sxs-lookup"><span data-stu-id="35626-112">public str getQuerySQL(str queryname)</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="35626-113">public str getTableSQL(str tablename, \[str policyname\])</span><span class="sxs-lookup"><span data-stu-id="35626-113">public str getTableSQL(str tablename, \[str policyname\])</span></span>              |                                                                                                                                   |
| <span data-ttu-id="35626-114">public str getXDSBinding(str name)</span><span class="sxs-lookup"><span data-stu-id="35626-114">public str getXDSBinding(str name)</span></span>                                     |                                                                                                                                   |
| <span data-ttu-id="35626-115">public str getXDSContext(int reserved)</span><span class="sxs-lookup"><span data-stu-id="35626-115">public str getXDSContext(int reserved)</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="35626-116">public int getXDSToFlushPerServiceSession(int reserved)</span><span class="sxs-lookup"><span data-stu-id="35626-116">public int getXDSToFlushPerServiceSession(int reserved)</span></span>                | <span data-ttu-id="35626-117">サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="35626-117">Checks whether the MyConstruct tables will be flushed when the service session is returned to the pool.</span></span>                           |
| <span data-ttu-id="35626-118">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="35626-118">public void finalize()</span></span>                                                 |                                                                                                                                   |
| <span data-ttu-id="35626-119">public void new()</span><span class="sxs-lookup"><span data-stu-id="35626-119">public void new()</span></span>                                                      | <span data-ttu-id="35626-120">XDSServices クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35626-120">Initializes a new instance of the XDSServices class.</span></span>                                                                              |
| <span data-ttu-id="35626-121">public void setXDSContext(int reserved, str contextstring)</span><span class="sxs-lookup"><span data-stu-id="35626-121">public void setXDSContext(int reserved, str contextstring)</span></span>             |                                                                                                                                   |
| <span data-ttu-id="35626-122">public void setXDSBinding(str name, str value)</span><span class="sxs-lookup"><span data-stu-id="35626-122">public void setXDSBinding(str name, str value)</span></span>                         |                                                                                                                                   |
| <span data-ttu-id="35626-123">public void setXDSState(int finalState)</span><span class="sxs-lookup"><span data-stu-id="35626-123">public void setXDSState(int finalState)</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="35626-124">public void setXDSToFlushPerServiceSession(int reserved, int newstate)</span><span class="sxs-lookup"><span data-stu-id="35626-124">public void setXDSToFlushPerServiceSession(int reserved, int newstate)</span></span> | <span data-ttu-id="35626-125">サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかを決定する設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="35626-125">Sets the setting that determines whether the MyConstruct tables will be flushed when the service session is returned to the pool.</span></span> |
| <span data-ttu-id="35626-126">public void setXDSTrace(int flag, str value)</span><span class="sxs-lookup"><span data-stu-id="35626-126">public void setXDSTrace(int flag, str value)</span></span>                           |                                                                                                                                   |

## <a name="method-flushxdsmyconstructs"></a><span data-ttu-id="35626-127">メソッド flushXDSMyConstructs</span><span class="sxs-lookup"><span data-stu-id="35626-127">Method flushXDSMyConstructs</span></span>

<span data-ttu-id="35626-128">XDS で使用される MyConstruct テーブルをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="35626-128">Flushes the MyConstruct table that is used with XDS.</span></span>

```xpp
public int flushXDSMyConstructs(int reserved, str tablename)
```

### <a name="parameters---flushxdsmyconstructs"></a><span data-ttu-id="35626-129">パラメーター - flushXDSMyConstructs</span><span class="sxs-lookup"><span data-stu-id="35626-129">Parameters - flushXDSMyConstructs</span></span>

<span data-ttu-id="35626-130">reserved</span><span class="sxs-lookup"><span data-stu-id="35626-130">reserved</span></span>  
<span data-ttu-id="35626-131">フラッシュする MyConstruct テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="35626-131">The name of the MyConstruct table to flush.</span></span> <span data-ttu-id="35626-132">値が渡されない場合、または空の文字列が渡される場合、すべての MyConstruct テーブルがフラッシュされます。</span><span class="sxs-lookup"><span data-stu-id="35626-132">It no value is passed in, or if an empty string is passed in, all MyConstruct tables are flushed.</span></span>

<!-- -->

<span data-ttu-id="35626-133">tablename</span><span class="sxs-lookup"><span data-stu-id="35626-133">tablename</span></span>  
<span data-ttu-id="35626-134">フラッシュする MyConstruct テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="35626-134">The name of the MyConstruct table to flush.</span></span> <span data-ttu-id="35626-135">値が渡されない場合、または空の文字列が渡される場合、すべての MyConstruct テーブルがフラッシュされます。</span><span class="sxs-lookup"><span data-stu-id="35626-135">It no value is passed in, or if an empty string is passed in, all MyConstruct tables are flushed.</span></span>

### <a name="return-value---flushxdsmyconstructs"></a><span data-ttu-id="35626-136">戻り値 - flushXDSMyConstructs</span><span class="sxs-lookup"><span data-stu-id="35626-136">Return Value - flushXDSMyConstructs</span></span>

## <a name="method-getquerysql"></a><span data-ttu-id="35626-137">メソッド getQuerySQL</span><span class="sxs-lookup"><span data-stu-id="35626-137">Method getQuerySQL</span></span>

```xpp
public str getQuerySQL(str queryname)
```

### <a name="parameters---getquerysql"></a><span data-ttu-id="35626-138">パラメーター - getQuerySQL</span><span class="sxs-lookup"><span data-stu-id="35626-138">Parameters - getQuerySQL</span></span>

<span data-ttu-id="35626-139">queryname</span><span class="sxs-lookup"><span data-stu-id="35626-139">queryname</span></span>  

### <a name="return-value---getquerysql"></a><span data-ttu-id="35626-140">戻り値 - getQuerySQL</span><span class="sxs-lookup"><span data-stu-id="35626-140">Return Value - getQuerySQL</span></span>

## <a name="method-gettablesql"></a><span data-ttu-id="35626-141">メソッド getTableSQL</span><span class="sxs-lookup"><span data-stu-id="35626-141">Method getTableSQL</span></span>

```xpp
public str getTableSQL(str tablename, [str policyname])
```

### <a name="parameters---gettablesql"></a><span data-ttu-id="35626-142">パラメーター - getTableSQL</span><span class="sxs-lookup"><span data-stu-id="35626-142">Parameters - getTableSQL</span></span>

<span data-ttu-id="35626-143">tablename</span><span class="sxs-lookup"><span data-stu-id="35626-143">tablename</span></span>  

<!-- -->

<span data-ttu-id="35626-144">policyname</span><span class="sxs-lookup"><span data-stu-id="35626-144">policyname</span></span>  

### <a name="return-value---gettablesql"></a><span data-ttu-id="35626-145">戻り値 - getTableSQL</span><span class="sxs-lookup"><span data-stu-id="35626-145">Return Value - getTableSQL</span></span>

## <a name="method-getxdsbinding"></a><span data-ttu-id="35626-146">メソッド getXDSBinding</span><span class="sxs-lookup"><span data-stu-id="35626-146">Method getXDSBinding</span></span>

```xpp
public str getXDSBinding(str name)
```

### <a name="parameters---getxdsbinding"></a><span data-ttu-id="35626-147">パラメーター - getXDSBinding</span><span class="sxs-lookup"><span data-stu-id="35626-147">Parameters - getXDSBinding</span></span>

<span data-ttu-id="35626-148">名前</span><span class="sxs-lookup"><span data-stu-id="35626-148">name</span></span>  

### <a name="return-value---getxdsbinding"></a><span data-ttu-id="35626-149">戻り値 - getXDSBinding</span><span class="sxs-lookup"><span data-stu-id="35626-149">Return Value - getXDSBinding</span></span>

## <a name="method-getxdscontext"></a><span data-ttu-id="35626-150">メソッド getXDSContext</span><span class="sxs-lookup"><span data-stu-id="35626-150">Method getXDSContext</span></span>

```xpp
public str getXDSContext(int reserved)
```

### <a name="parameters---getxdscontext"></a><span data-ttu-id="35626-151">パラメーター - getXDSContext</span><span class="sxs-lookup"><span data-stu-id="35626-151">Parameters - getXDSContext</span></span>

<span data-ttu-id="35626-152">reserved</span><span class="sxs-lookup"><span data-stu-id="35626-152">reserved</span></span>  

### <a name="return-value---getxdscontext"></a><span data-ttu-id="35626-153">戻り値 - getXDSContext</span><span class="sxs-lookup"><span data-stu-id="35626-153">Return Value - getXDSContext</span></span>

## <a name="method-getxdstoflushperservicesession"></a><span data-ttu-id="35626-154">メソッド getXDSToFlushPerServiceSession</span><span class="sxs-lookup"><span data-stu-id="35626-154">Method getXDSToFlushPerServiceSession</span></span>

<span data-ttu-id="35626-155">サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="35626-155">Checks whether the MyConstruct tables will be flushed when the service session is returned to the pool.</span></span>

```xpp
public int getXDSToFlushPerServiceSession(int reserved)
```

### <a name="parameters---getxdstoflushperservicesession"></a><span data-ttu-id="35626-156">パラメーター - getXDSToFlushPerServiceSession</span><span class="sxs-lookup"><span data-stu-id="35626-156">Parameters - getXDSToFlushPerServiceSession</span></span>

<span data-ttu-id="35626-157">reserved</span><span class="sxs-lookup"><span data-stu-id="35626-157">reserved</span></span>  
<span data-ttu-id="35626-158">予約済フラグ、現在使用されていません。</span><span class="sxs-lookup"><span data-stu-id="35626-158">A reserved flag; not currently used.</span></span>

### <a name="return-value---getxdstoflushperservicesession"></a><span data-ttu-id="35626-159">戻り値 - getXDSToFlushPerServiceSession</span><span class="sxs-lookup"><span data-stu-id="35626-159">Return Value - getXDSToFlushPerServiceSession</span></span>

<span data-ttu-id="35626-160">サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされる場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="35626-160">1 if the MyConstruct tables will be flushed when the service session is returned to the pool; otherwise, 0.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="35626-161">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="35626-161">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="35626-162">メソッド new</span><span class="sxs-lookup"><span data-stu-id="35626-162">Method new</span></span>

<span data-ttu-id="35626-163">XDSServices クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35626-163">Initializes a new instance of the XDSServices class.</span></span>

```xpp
public void new()
```

## <a name="method-setxdscontext"></a><span data-ttu-id="35626-164">メソッド setXDSContext</span><span class="sxs-lookup"><span data-stu-id="35626-164">Method setXDSContext</span></span>

```xpp
public void setXDSContext(int reserved, str contextstring)
```

### <a name="parameters---setxdscontext"></a><span data-ttu-id="35626-165">パラメーター - setXDSContext</span><span class="sxs-lookup"><span data-stu-id="35626-165">Parameters - setXDSContext</span></span>

<span data-ttu-id="35626-166">reserved</span><span class="sxs-lookup"><span data-stu-id="35626-166">reserved</span></span>  

<!-- -->

<span data-ttu-id="35626-167">contextstring</span><span class="sxs-lookup"><span data-stu-id="35626-167">contextstring</span></span>  

## <a name="method-setxdsbinding"></a><span data-ttu-id="35626-168">メソッド setXDSBinding</span><span class="sxs-lookup"><span data-stu-id="35626-168">Method setXDSBinding</span></span>

```xpp
public void setXDSBinding(str name, str value)
```

### <a name="parameters---setxdsbinding"></a><span data-ttu-id="35626-169">パラメーター - setXDSBinding</span><span class="sxs-lookup"><span data-stu-id="35626-169">Parameters - setXDSBinding</span></span>

<span data-ttu-id="35626-170">名前</span><span class="sxs-lookup"><span data-stu-id="35626-170">name</span></span>  

<!-- -->

<span data-ttu-id="35626-171">値</span><span class="sxs-lookup"><span data-stu-id="35626-171">value</span></span>  

## <a name="method-setxdsstate"></a><span data-ttu-id="35626-172">メソッド setXDSState</span><span class="sxs-lookup"><span data-stu-id="35626-172">Method setXDSState</span></span>

```xpp
public void setXDSState(int finalState)
```

### <a name="parameters---setxdsstate"></a><span data-ttu-id="35626-173">パラメーター - setXDSState</span><span class="sxs-lookup"><span data-stu-id="35626-173">Parameters - setXDSState</span></span>

<span data-ttu-id="35626-174">finalState</span><span class="sxs-lookup"><span data-stu-id="35626-174">finalState</span></span>  

## <a name="method-setxdstoflushperservicesession"></a><span data-ttu-id="35626-175">メソッド setXDSToFlushPerServiceSession</span><span class="sxs-lookup"><span data-stu-id="35626-175">Method setXDSToFlushPerServiceSession</span></span>

<span data-ttu-id="35626-176">サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかを決定する設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="35626-176">Sets the setting that determines whether the MyConstruct tables will be flushed when the service session is returned to the pool.</span></span>

```xpp
public void setXDSToFlushPerServiceSession(int reserved, int newstate)
```

### <a name="parameters---setxdstoflushperservicesession"></a><span data-ttu-id="35626-177">パラメーター - setXDSToFlushPerServiceSession</span><span class="sxs-lookup"><span data-stu-id="35626-177">Parameters - setXDSToFlushPerServiceSession</span></span>

<span data-ttu-id="35626-178">reserved</span><span class="sxs-lookup"><span data-stu-id="35626-178">reserved</span></span>  
<span data-ttu-id="35626-179">サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュするかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="35626-179">A value that indicates whether to flush the MyConstruct tables when the service session is returned to the pool.</span></span> <span data-ttu-id="35626-180">テーブルにフラッシュする場合は 1 を、フラッシュしない場合は 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="35626-180">Pass 1 to flush the tables and 0 not to flush them.</span></span>

<!-- -->

<span data-ttu-id="35626-181">newstate</span><span class="sxs-lookup"><span data-stu-id="35626-181">newstate</span></span>  
<span data-ttu-id="35626-182">サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュするかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="35626-182">A value that indicates whether to flush the MyConstruct tables when the service session is returned to the pool.</span></span> <span data-ttu-id="35626-183">テーブルにフラッシュする場合は 1 を、フラッシュしない場合は 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="35626-183">Pass 1 to flush the tables and 0 not to flush them.</span></span>

## <a name="method-setxdstrace"></a><span data-ttu-id="35626-184">メソッド setXDSTrace</span><span class="sxs-lookup"><span data-stu-id="35626-184">Method setXDSTrace</span></span>

```xpp
public void setXDSTrace(int flag, str value)
```

### <a name="parameters---setxdstrace"></a><span data-ttu-id="35626-185">パラメーター - setXDSTrace</span><span class="sxs-lookup"><span data-stu-id="35626-185">Parameters - setXDSTrace</span></span>

<span data-ttu-id="35626-186">flag</span><span class="sxs-lookup"><span data-stu-id="35626-186">flag</span></span>  

<!-- -->

<span data-ttu-id="35626-187">値</span><span class="sxs-lookup"><span data-stu-id="35626-187">value</span></span>  

