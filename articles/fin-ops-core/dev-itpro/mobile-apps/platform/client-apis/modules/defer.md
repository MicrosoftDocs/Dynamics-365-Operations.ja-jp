---
title: 延期モジュール
description: 延期タイプ
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f25d94acdeb31e37547d9111bfd799840ac35642
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986909"
---
# <a name="defer-module"></a><span data-ttu-id="a3810-103">延期モジュール</span><span class="sxs-lookup"><span data-stu-id="a3810-103">Defer module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="a3810-104">指数</span><span class="sxs-lookup"><span data-stu-id="a3810-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="a3810-105">種類</span><span class="sxs-lookup"><span data-stu-id="a3810-105">Types</span></span>

* [<span data-ttu-id="a3810-106">Deferred</span><span class="sxs-lookup"><span data-stu-id="a3810-106">Deferred</span></span>](../interfaces/defer-ideferred.md)

### <a name="functions"></a><span data-ttu-id="a3810-107">関数</span><span class="sxs-lookup"><span data-stu-id="a3810-107">Functions</span></span>

* [<span data-ttu-id="a3810-108">すべて</span><span class="sxs-lookup"><span data-stu-id="a3810-108">all</span></span>](defer.md#all)
* [<span data-ttu-id="a3810-109">延期</span><span class="sxs-lookup"><span data-stu-id="a3810-109">defer</span></span>](defer.md)
* [<span data-ttu-id="a3810-110">否認</span><span class="sxs-lookup"><span data-stu-id="a3810-110">reject</span></span>](defer.md#reject)
* [<span data-ttu-id="a3810-111">解決</span><span class="sxs-lookup"><span data-stu-id="a3810-111">resolve</span></span>](defer.md#resolve)

## <a name="types"></a><span data-ttu-id="a3810-112">種類</span><span class="sxs-lookup"><span data-stu-id="a3810-112">Types</span></span>


### <a name="deferred"></a><span data-ttu-id="a3810-113">繰延</span><span class="sxs-lookup"><span data-stu-id="a3810-113">Deferred</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="a3810-114">階層</span><span class="sxs-lookup"><span data-stu-id="a3810-114">Hierarchy</span></span>

<span data-ttu-id="a3810-115">繰延</span><span class="sxs-lookup"><span data-stu-id="a3810-115">Deferred</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="a3810-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="a3810-116">Properties</span></span>

| <span data-ttu-id="a3810-117">氏名</span><span class="sxs-lookup"><span data-stu-id="a3810-117">Name</span></span> | <span data-ttu-id="a3810-118">署名</span><span class="sxs-lookup"><span data-stu-id="a3810-118">Signature</span></span> | <span data-ttu-id="a3810-119">説明</span><span class="sxs-lookup"><span data-stu-id="a3810-119">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="a3810-120">promise</span><span class="sxs-lookup"><span data-stu-id="a3810-120">promise</span></span>](../interfaces/defer-ideferred.md#promise) |<span data-ttu-id="a3810-121">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="a3810-121">promise: Promise &lt;T&gt;</span></span> <br>|  |

#### <a name="methods"></a><span data-ttu-id="a3810-122">メソッド</span><span class="sxs-lookup"><span data-stu-id="a3810-122">Methods</span></span>

| <span data-ttu-id="a3810-123">氏名</span><span class="sxs-lookup"><span data-stu-id="a3810-123">Name</span></span> | <span data-ttu-id="a3810-124">署名</span><span class="sxs-lookup"><span data-stu-id="a3810-124">Signature</span></span> | <span data-ttu-id="a3810-125">説明</span><span class="sxs-lookup"><span data-stu-id="a3810-125">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="a3810-126">否認</span><span class="sxs-lookup"><span data-stu-id="a3810-126">reject</span></span>](../interfaces/defer-ideferred.md#reject) |<span data-ttu-id="a3810-127">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="a3810-127">reject(error?: any): void</span></span>|  |
| [<span data-ttu-id="a3810-128">解決</span><span class="sxs-lookup"><span data-stu-id="a3810-128">resolve</span></span>](../interfaces/defer-ideferred.md#resolve) |<span data-ttu-id="a3810-129">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="a3810-129">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>|  |

## <a name="functions"></a><span data-ttu-id="a3810-130">ファンクション</span><span class="sxs-lookup"><span data-stu-id="a3810-130">Functions</span></span>


### <a name="all"></a><span data-ttu-id="a3810-131">すべて</span><span class="sxs-lookup"><span data-stu-id="a3810-131">all</span></span>
<span data-ttu-id="a3810-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="a3810-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="a3810-133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a3810-133">Parameters</span></span>

| <span data-ttu-id="a3810-134">氏名</span><span class="sxs-lookup"><span data-stu-id="a3810-134">Name</span></span> | <span data-ttu-id="a3810-135">種類</span><span class="sxs-lookup"><span data-stu-id="a3810-135">Type</span></span> | <span data-ttu-id="a3810-136">説明</span><span class="sxs-lookup"><span data-stu-id="a3810-136">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="a3810-137">...args</span><span class="sxs-lookup"><span data-stu-id="a3810-137">...args</span></span>|<span data-ttu-id="a3810-138">any [ ]</span><span class="sxs-lookup"><span data-stu-id="a3810-138">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="a3810-139">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="a3810-139">Returns Promise &lt;any [ ]&gt;</span></span>


### <a name="defer"></a><span data-ttu-id="a3810-140">defer</span><span class="sxs-lookup"><span data-stu-id="a3810-140">defer</span></span>
<span data-ttu-id="a3810-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="a3810-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>



#### <a name="returns-deferred-lttgt"></a><span data-ttu-id="a3810-142">[Deferred](../interfaces/defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="a3810-142">Returns [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>


### <a name="reject"></a><span data-ttu-id="a3810-143">否認</span><span class="sxs-lookup"><span data-stu-id="a3810-143">reject</span></span>
<span data-ttu-id="a3810-144">reject(error?: any): Promise &lt;any&gt;</span><span class="sxs-lookup"><span data-stu-id="a3810-144">reject(error?: any): Promise &lt;any&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="a3810-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a3810-145">Parameters</span></span>

| <span data-ttu-id="a3810-146">氏名</span><span class="sxs-lookup"><span data-stu-id="a3810-146">Name</span></span> | <span data-ttu-id="a3810-147">種類</span><span class="sxs-lookup"><span data-stu-id="a3810-147">Type</span></span> | <span data-ttu-id="a3810-148">説明</span><span class="sxs-lookup"><span data-stu-id="a3810-148">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="a3810-149">エラー?</span><span class="sxs-lookup"><span data-stu-id="a3810-149">error?</span></span>|<span data-ttu-id="a3810-150">any</span><span class="sxs-lookup"><span data-stu-id="a3810-150">any</span></span>||

#### <a name="returns-promise-ltanygt"></a><span data-ttu-id="a3810-151">Promise &lt;any&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="a3810-151">Returns Promise &lt;any&gt;</span></span>


### <a name="resolve"></a><span data-ttu-id="a3810-152">解決</span><span class="sxs-lookup"><span data-stu-id="a3810-152">resolve</span></span>
<span data-ttu-id="a3810-153">resolve &lt;T&gt; (value?: T &#124; PromiseLike &lt;T&gt;) : Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="a3810-153">resolve &lt;T&gt;(value?: T &#124; PromiseLike &lt;T&gt;): Promise &lt;T&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="a3810-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a3810-154">Parameters</span></span>

| <span data-ttu-id="a3810-155">氏名</span><span class="sxs-lookup"><span data-stu-id="a3810-155">Name</span></span> | <span data-ttu-id="a3810-156">型</span><span class="sxs-lookup"><span data-stu-id="a3810-156">Type</span></span> | <span data-ttu-id="a3810-157">説明</span><span class="sxs-lookup"><span data-stu-id="a3810-157">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="a3810-158">value?</span><span class="sxs-lookup"><span data-stu-id="a3810-158">value?</span></span>|<span data-ttu-id="a3810-159">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="a3810-159">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-promise-lttgt"></a><span data-ttu-id="a3810-160">Promise &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="a3810-160">Returns Promise &lt;T&gt;</span></span>

