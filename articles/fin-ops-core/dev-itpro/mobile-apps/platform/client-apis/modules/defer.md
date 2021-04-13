---
title: 延期モジュール
description: 延期タイプ
author: robinarh
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49376e2049c2c2b2b4e947d9122e4253e02b371a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743391"
---
# <a name="defer-module"></a><span data-ttu-id="085cb-103">延期モジュール</span><span class="sxs-lookup"><span data-stu-id="085cb-103">Defer module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="085cb-104">指数</span><span class="sxs-lookup"><span data-stu-id="085cb-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="085cb-105">種類</span><span class="sxs-lookup"><span data-stu-id="085cb-105">Types</span></span>

* [<span data-ttu-id="085cb-106">Deferred</span><span class="sxs-lookup"><span data-stu-id="085cb-106">Deferred</span></span>](../interfaces/defer-ideferred.md)

### <a name="functions"></a><span data-ttu-id="085cb-107">関数</span><span class="sxs-lookup"><span data-stu-id="085cb-107">Functions</span></span>

* [<span data-ttu-id="085cb-108">すべて</span><span class="sxs-lookup"><span data-stu-id="085cb-108">all</span></span>](defer.md#all)
* [<span data-ttu-id="085cb-109">延期</span><span class="sxs-lookup"><span data-stu-id="085cb-109">defer</span></span>](defer.md)
* [<span data-ttu-id="085cb-110">否認</span><span class="sxs-lookup"><span data-stu-id="085cb-110">reject</span></span>](defer.md#reject)
* [<span data-ttu-id="085cb-111">解決</span><span class="sxs-lookup"><span data-stu-id="085cb-111">resolve</span></span>](defer.md#resolve)

## <a name="types"></a><span data-ttu-id="085cb-112">種類</span><span class="sxs-lookup"><span data-stu-id="085cb-112">Types</span></span>


### <a name="deferred"></a><span data-ttu-id="085cb-113">繰延</span><span class="sxs-lookup"><span data-stu-id="085cb-113">Deferred</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="085cb-114">階層</span><span class="sxs-lookup"><span data-stu-id="085cb-114">Hierarchy</span></span>

<span data-ttu-id="085cb-115">繰延</span><span class="sxs-lookup"><span data-stu-id="085cb-115">Deferred</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="085cb-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="085cb-116">Properties</span></span>

| <span data-ttu-id="085cb-117">氏名</span><span class="sxs-lookup"><span data-stu-id="085cb-117">Name</span></span> | <span data-ttu-id="085cb-118">署名</span><span class="sxs-lookup"><span data-stu-id="085cb-118">Signature</span></span> | <span data-ttu-id="085cb-119">説明</span><span class="sxs-lookup"><span data-stu-id="085cb-119">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="085cb-120">promise</span><span class="sxs-lookup"><span data-stu-id="085cb-120">promise</span></span>](../interfaces/defer-ideferred.md#promise) |<span data-ttu-id="085cb-121">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="085cb-121">promise: Promise &lt;T&gt;</span></span> <br>|  |

#### <a name="methods"></a><span data-ttu-id="085cb-122">メソッド</span><span class="sxs-lookup"><span data-stu-id="085cb-122">Methods</span></span>

| <span data-ttu-id="085cb-123">氏名</span><span class="sxs-lookup"><span data-stu-id="085cb-123">Name</span></span> | <span data-ttu-id="085cb-124">署名</span><span class="sxs-lookup"><span data-stu-id="085cb-124">Signature</span></span> | <span data-ttu-id="085cb-125">説明</span><span class="sxs-lookup"><span data-stu-id="085cb-125">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="085cb-126">否認</span><span class="sxs-lookup"><span data-stu-id="085cb-126">reject</span></span>](../interfaces/defer-ideferred.md#reject) |<span data-ttu-id="085cb-127">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="085cb-127">reject(error?: any): void</span></span>|  |
| [<span data-ttu-id="085cb-128">解決</span><span class="sxs-lookup"><span data-stu-id="085cb-128">resolve</span></span>](../interfaces/defer-ideferred.md#resolve) |<span data-ttu-id="085cb-129">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="085cb-129">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>|  |

## <a name="functions"></a><span data-ttu-id="085cb-130">ファンクション</span><span class="sxs-lookup"><span data-stu-id="085cb-130">Functions</span></span>


### <a name="all"></a><span data-ttu-id="085cb-131">すべて</span><span class="sxs-lookup"><span data-stu-id="085cb-131">all</span></span>
<span data-ttu-id="085cb-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="085cb-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="085cb-133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="085cb-133">Parameters</span></span>

| <span data-ttu-id="085cb-134">氏名</span><span class="sxs-lookup"><span data-stu-id="085cb-134">Name</span></span> | <span data-ttu-id="085cb-135">種類</span><span class="sxs-lookup"><span data-stu-id="085cb-135">Type</span></span> | <span data-ttu-id="085cb-136">説明</span><span class="sxs-lookup"><span data-stu-id="085cb-136">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="085cb-137">...args</span><span class="sxs-lookup"><span data-stu-id="085cb-137">...args</span></span>|<span data-ttu-id="085cb-138">any [ ]</span><span class="sxs-lookup"><span data-stu-id="085cb-138">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="085cb-139">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="085cb-139">Returns Promise &lt;any [ ]&gt;</span></span>


### <a name="defer"></a><span data-ttu-id="085cb-140">defer</span><span class="sxs-lookup"><span data-stu-id="085cb-140">defer</span></span>
<span data-ttu-id="085cb-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="085cb-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>



#### <a name="returns-deferred-lttgt"></a><span data-ttu-id="085cb-142">[Deferred](../interfaces/defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="085cb-142">Returns [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>


### <a name="reject"></a><span data-ttu-id="085cb-143">否認</span><span class="sxs-lookup"><span data-stu-id="085cb-143">reject</span></span>
<span data-ttu-id="085cb-144">reject(error?: any): Promise &lt;any&gt;</span><span class="sxs-lookup"><span data-stu-id="085cb-144">reject(error?: any): Promise &lt;any&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="085cb-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="085cb-145">Parameters</span></span>

| <span data-ttu-id="085cb-146">氏名</span><span class="sxs-lookup"><span data-stu-id="085cb-146">Name</span></span> | <span data-ttu-id="085cb-147">種類</span><span class="sxs-lookup"><span data-stu-id="085cb-147">Type</span></span> | <span data-ttu-id="085cb-148">説明</span><span class="sxs-lookup"><span data-stu-id="085cb-148">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="085cb-149">エラー?</span><span class="sxs-lookup"><span data-stu-id="085cb-149">error?</span></span>|<span data-ttu-id="085cb-150">any</span><span class="sxs-lookup"><span data-stu-id="085cb-150">any</span></span>||

#### <a name="returns-promise-ltanygt"></a><span data-ttu-id="085cb-151">Promise &lt;any&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="085cb-151">Returns Promise &lt;any&gt;</span></span>


### <a name="resolve"></a><span data-ttu-id="085cb-152">解決</span><span class="sxs-lookup"><span data-stu-id="085cb-152">resolve</span></span>
<span data-ttu-id="085cb-153">resolve &lt;T&gt; (value?: T &#124; PromiseLike &lt;T&gt;) : Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="085cb-153">resolve &lt;T&gt;(value?: T &#124; PromiseLike &lt;T&gt;): Promise &lt;T&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="085cb-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="085cb-154">Parameters</span></span>

| <span data-ttu-id="085cb-155">氏名</span><span class="sxs-lookup"><span data-stu-id="085cb-155">Name</span></span> | <span data-ttu-id="085cb-156">型</span><span class="sxs-lookup"><span data-stu-id="085cb-156">Type</span></span> | <span data-ttu-id="085cb-157">説明</span><span class="sxs-lookup"><span data-stu-id="085cb-157">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="085cb-158">value?</span><span class="sxs-lookup"><span data-stu-id="085cb-158">value?</span></span>|<span data-ttu-id="085cb-159">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="085cb-159">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-promise-lttgt"></a><span data-ttu-id="085cb-160">Promise &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="085cb-160">Returns Promise &lt;T&gt;</span></span>



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]