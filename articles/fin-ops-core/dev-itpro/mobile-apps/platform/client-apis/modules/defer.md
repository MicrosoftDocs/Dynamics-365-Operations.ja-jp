---
title: 延期モジュール
description: 延期タイプ
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 513eadb369379672b34dd3ecb6f8d087c907efbf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682567"
---
# <a name="defer-module"></a><span data-ttu-id="0e367-103">延期モジュール</span><span class="sxs-lookup"><span data-stu-id="0e367-103">Defer module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="0e367-104">指数</span><span class="sxs-lookup"><span data-stu-id="0e367-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="0e367-105">種類</span><span class="sxs-lookup"><span data-stu-id="0e367-105">Types</span></span>

* [<span data-ttu-id="0e367-106">Deferred</span><span class="sxs-lookup"><span data-stu-id="0e367-106">Deferred</span></span>](../interfaces/defer-ideferred.md)

### <a name="functions"></a><span data-ttu-id="0e367-107">関数</span><span class="sxs-lookup"><span data-stu-id="0e367-107">Functions</span></span>

* [<span data-ttu-id="0e367-108">すべて</span><span class="sxs-lookup"><span data-stu-id="0e367-108">all</span></span>](defer.md#all)
* [<span data-ttu-id="0e367-109">延期</span><span class="sxs-lookup"><span data-stu-id="0e367-109">defer</span></span>](defer.md)
* [<span data-ttu-id="0e367-110">否認</span><span class="sxs-lookup"><span data-stu-id="0e367-110">reject</span></span>](defer.md#reject)
* [<span data-ttu-id="0e367-111">解決</span><span class="sxs-lookup"><span data-stu-id="0e367-111">resolve</span></span>](defer.md#resolve)

## <a name="types"></a><span data-ttu-id="0e367-112">種類</span><span class="sxs-lookup"><span data-stu-id="0e367-112">Types</span></span>


### <a name="deferred"></a><span data-ttu-id="0e367-113">繰延</span><span class="sxs-lookup"><span data-stu-id="0e367-113">Deferred</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="0e367-114">階層</span><span class="sxs-lookup"><span data-stu-id="0e367-114">Hierarchy</span></span>

<span data-ttu-id="0e367-115">繰延</span><span class="sxs-lookup"><span data-stu-id="0e367-115">Deferred</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="0e367-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0e367-116">Properties</span></span>

| <span data-ttu-id="0e367-117">氏名</span><span class="sxs-lookup"><span data-stu-id="0e367-117">Name</span></span> | <span data-ttu-id="0e367-118">署名</span><span class="sxs-lookup"><span data-stu-id="0e367-118">Signature</span></span> | <span data-ttu-id="0e367-119">説明</span><span class="sxs-lookup"><span data-stu-id="0e367-119">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="0e367-120">promise</span><span class="sxs-lookup"><span data-stu-id="0e367-120">promise</span></span>](../interfaces/defer-ideferred.md#promise) |<span data-ttu-id="0e367-121">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="0e367-121">promise: Promise &lt;T&gt;</span></span> <br>|  |

#### <a name="methods"></a><span data-ttu-id="0e367-122">メソッド</span><span class="sxs-lookup"><span data-stu-id="0e367-122">Methods</span></span>

| <span data-ttu-id="0e367-123">氏名</span><span class="sxs-lookup"><span data-stu-id="0e367-123">Name</span></span> | <span data-ttu-id="0e367-124">署名</span><span class="sxs-lookup"><span data-stu-id="0e367-124">Signature</span></span> | <span data-ttu-id="0e367-125">説明</span><span class="sxs-lookup"><span data-stu-id="0e367-125">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="0e367-126">否認</span><span class="sxs-lookup"><span data-stu-id="0e367-126">reject</span></span>](../interfaces/defer-ideferred.md#reject) |<span data-ttu-id="0e367-127">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="0e367-127">reject(error?: any): void</span></span>|  |
| [<span data-ttu-id="0e367-128">解決</span><span class="sxs-lookup"><span data-stu-id="0e367-128">resolve</span></span>](../interfaces/defer-ideferred.md#resolve) |<span data-ttu-id="0e367-129">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="0e367-129">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>|  |

## <a name="functions"></a><span data-ttu-id="0e367-130">関数</span><span class="sxs-lookup"><span data-stu-id="0e367-130">Functions</span></span>


### <a name="all"></a><span data-ttu-id="0e367-131">すべて</span><span class="sxs-lookup"><span data-stu-id="0e367-131">all</span></span>
<span data-ttu-id="0e367-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="0e367-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="0e367-133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e367-133">Parameters</span></span>

| <span data-ttu-id="0e367-134">氏名</span><span class="sxs-lookup"><span data-stu-id="0e367-134">Name</span></span> | <span data-ttu-id="0e367-135">種類</span><span class="sxs-lookup"><span data-stu-id="0e367-135">Type</span></span> | <span data-ttu-id="0e367-136">説明</span><span class="sxs-lookup"><span data-stu-id="0e367-136">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0e367-137">...args</span><span class="sxs-lookup"><span data-stu-id="0e367-137">...args</span></span>|<span data-ttu-id="0e367-138">any [ ]</span><span class="sxs-lookup"><span data-stu-id="0e367-138">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="0e367-139">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="0e367-139">Returns Promise &lt;any [ ]&gt;</span></span>


### <a name="defer"></a><span data-ttu-id="0e367-140">defer</span><span class="sxs-lookup"><span data-stu-id="0e367-140">defer</span></span>
<span data-ttu-id="0e367-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="0e367-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>



#### <a name="returns-deferred-lttgt"></a><span data-ttu-id="0e367-142">[Deferred](../interfaces/defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="0e367-142">Returns [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>


### <a name="reject"></a><span data-ttu-id="0e367-143">否認</span><span class="sxs-lookup"><span data-stu-id="0e367-143">reject</span></span>
<span data-ttu-id="0e367-144">reject(error?: any): Promise &lt;any&gt;</span><span class="sxs-lookup"><span data-stu-id="0e367-144">reject(error?: any): Promise &lt;any&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="0e367-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e367-145">Parameters</span></span>

| <span data-ttu-id="0e367-146">氏名</span><span class="sxs-lookup"><span data-stu-id="0e367-146">Name</span></span> | <span data-ttu-id="0e367-147">種類</span><span class="sxs-lookup"><span data-stu-id="0e367-147">Type</span></span> | <span data-ttu-id="0e367-148">説明</span><span class="sxs-lookup"><span data-stu-id="0e367-148">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0e367-149">エラー?</span><span class="sxs-lookup"><span data-stu-id="0e367-149">error?</span></span>|<span data-ttu-id="0e367-150">any</span><span class="sxs-lookup"><span data-stu-id="0e367-150">any</span></span>||

#### <a name="returns-promise-ltanygt"></a><span data-ttu-id="0e367-151">Promise &lt;any&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="0e367-151">Returns Promise &lt;any&gt;</span></span>


### <a name="resolve"></a><span data-ttu-id="0e367-152">解決</span><span class="sxs-lookup"><span data-stu-id="0e367-152">resolve</span></span>
<span data-ttu-id="0e367-153">resolve &lt;T&gt; (value?: T &#124; PromiseLike &lt;T&gt;) : Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="0e367-153">resolve &lt;T&gt;(value?: T &#124; PromiseLike &lt;T&gt;): Promise &lt;T&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="0e367-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e367-154">Parameters</span></span>

| <span data-ttu-id="0e367-155">氏名</span><span class="sxs-lookup"><span data-stu-id="0e367-155">Name</span></span> | <span data-ttu-id="0e367-156">型</span><span class="sxs-lookup"><span data-stu-id="0e367-156">Type</span></span> | <span data-ttu-id="0e367-157">説明</span><span class="sxs-lookup"><span data-stu-id="0e367-157">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0e367-158">value?</span><span class="sxs-lookup"><span data-stu-id="0e367-158">value?</span></span>|<span data-ttu-id="0e367-159">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="0e367-159">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-promise-lttgt"></a><span data-ttu-id="0e367-160">Promise &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="0e367-160">Returns Promise &lt;T&gt;</span></span>

