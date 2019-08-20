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
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f41a6ef2a14cdcdb78323121071fa012ecc9db58
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851513"
---
# <a name="defer-module"></a><span data-ttu-id="f19e0-103">延期モジュール</span><span class="sxs-lookup"><span data-stu-id="f19e0-103">Defer module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="f19e0-104">指数</span><span class="sxs-lookup"><span data-stu-id="f19e0-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="f19e0-105">種類</span><span class="sxs-lookup"><span data-stu-id="f19e0-105">Types</span></span>

* [<span data-ttu-id="f19e0-106">Deferred</span><span class="sxs-lookup"><span data-stu-id="f19e0-106">Deferred</span></span>](../interfaces/defer-ideferred.md)

### <a name="functions"></a><span data-ttu-id="f19e0-107">関数</span><span class="sxs-lookup"><span data-stu-id="f19e0-107">Functions</span></span>

* [<span data-ttu-id="f19e0-108">すべて</span><span class="sxs-lookup"><span data-stu-id="f19e0-108">all</span></span>](defer.md#all)
* [<span data-ttu-id="f19e0-109">延期</span><span class="sxs-lookup"><span data-stu-id="f19e0-109">defer</span></span>](defer.md)
* [<span data-ttu-id="f19e0-110">否認</span><span class="sxs-lookup"><span data-stu-id="f19e0-110">reject</span></span>](defer.md#reject)
* [<span data-ttu-id="f19e0-111">解決</span><span class="sxs-lookup"><span data-stu-id="f19e0-111">resolve</span></span>](defer.md#resolve)

## <a name="types"></a><span data-ttu-id="f19e0-112">種類</span><span class="sxs-lookup"><span data-stu-id="f19e0-112">Types</span></span>


### <a name="deferred"></a><span data-ttu-id="f19e0-113">繰延</span><span class="sxs-lookup"><span data-stu-id="f19e0-113">Deferred</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="f19e0-114">階層</span><span class="sxs-lookup"><span data-stu-id="f19e0-114">Hierarchy</span></span>

<span data-ttu-id="f19e0-115">繰延</span><span class="sxs-lookup"><span data-stu-id="f19e0-115">Deferred</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="f19e0-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f19e0-116">Properties</span></span>

| <span data-ttu-id="f19e0-117">氏名</span><span class="sxs-lookup"><span data-stu-id="f19e0-117">Name</span></span> | <span data-ttu-id="f19e0-118">署名</span><span class="sxs-lookup"><span data-stu-id="f19e0-118">Signature</span></span> | <span data-ttu-id="f19e0-119">説明</span><span class="sxs-lookup"><span data-stu-id="f19e0-119">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="f19e0-120">promise</span><span class="sxs-lookup"><span data-stu-id="f19e0-120">promise</span></span>](../interfaces/defer-ideferred.md#promise) |<span data-ttu-id="f19e0-121">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="f19e0-121">promise: Promise &lt;T&gt;</span></span> <br>|  |

#### <a name="methods"></a><span data-ttu-id="f19e0-122">メソッド</span><span class="sxs-lookup"><span data-stu-id="f19e0-122">Methods</span></span>

| <span data-ttu-id="f19e0-123">氏名</span><span class="sxs-lookup"><span data-stu-id="f19e0-123">Name</span></span> | <span data-ttu-id="f19e0-124">署名</span><span class="sxs-lookup"><span data-stu-id="f19e0-124">Signature</span></span> | <span data-ttu-id="f19e0-125">説明</span><span class="sxs-lookup"><span data-stu-id="f19e0-125">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="f19e0-126">否認</span><span class="sxs-lookup"><span data-stu-id="f19e0-126">reject</span></span>](../interfaces/defer-ideferred.md#reject) |<span data-ttu-id="f19e0-127">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="f19e0-127">reject(error?: any): void</span></span>|  |
| [<span data-ttu-id="f19e0-128">解決</span><span class="sxs-lookup"><span data-stu-id="f19e0-128">resolve</span></span>](../interfaces/defer-ideferred.md#resolve) |<span data-ttu-id="f19e0-129">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="f19e0-129">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>|  |

## <a name="functions"></a><span data-ttu-id="f19e0-130">ファンクション</span><span class="sxs-lookup"><span data-stu-id="f19e0-130">Functions</span></span>


### <a name="all"></a><span data-ttu-id="f19e0-131">すべて</span><span class="sxs-lookup"><span data-stu-id="f19e0-131">all</span></span>
<span data-ttu-id="f19e0-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="f19e0-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="f19e0-133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f19e0-133">Parameters</span></span>

| <span data-ttu-id="f19e0-134">氏名</span><span class="sxs-lookup"><span data-stu-id="f19e0-134">Name</span></span> | <span data-ttu-id="f19e0-135">種類</span><span class="sxs-lookup"><span data-stu-id="f19e0-135">Type</span></span> | <span data-ttu-id="f19e0-136">説明</span><span class="sxs-lookup"><span data-stu-id="f19e0-136">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f19e0-137">...args</span><span class="sxs-lookup"><span data-stu-id="f19e0-137">...args</span></span>|<span data-ttu-id="f19e0-138">any [ ]</span><span class="sxs-lookup"><span data-stu-id="f19e0-138">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="f19e0-139">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="f19e0-139">Returns Promise &lt;any [ ]&gt;</span></span>


### <a name="defer"></a><span data-ttu-id="f19e0-140">defer</span><span class="sxs-lookup"><span data-stu-id="f19e0-140">defer</span></span>
<span data-ttu-id="f19e0-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="f19e0-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>



#### <a name="returns-deferredinterfacesdefer-ideferredmd-lttgt"></a><span data-ttu-id="f19e0-142">[Deferred](../interfaces/defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="f19e0-142">Returns [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>


### <a name="reject"></a><span data-ttu-id="f19e0-143">否認</span><span class="sxs-lookup"><span data-stu-id="f19e0-143">reject</span></span>
<span data-ttu-id="f19e0-144">reject(error?: any): Promise &lt;any&gt;</span><span class="sxs-lookup"><span data-stu-id="f19e0-144">reject(error?: any): Promise &lt;any&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="f19e0-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f19e0-145">Parameters</span></span>

| <span data-ttu-id="f19e0-146">氏名</span><span class="sxs-lookup"><span data-stu-id="f19e0-146">Name</span></span> | <span data-ttu-id="f19e0-147">種類</span><span class="sxs-lookup"><span data-stu-id="f19e0-147">Type</span></span> | <span data-ttu-id="f19e0-148">説明</span><span class="sxs-lookup"><span data-stu-id="f19e0-148">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f19e0-149">エラー?</span><span class="sxs-lookup"><span data-stu-id="f19e0-149">error?</span></span>|<span data-ttu-id="f19e0-150">any</span><span class="sxs-lookup"><span data-stu-id="f19e0-150">any</span></span>||

#### <a name="returns-promise-ltanygt"></a><span data-ttu-id="f19e0-151">Promise &lt;any&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="f19e0-151">Returns Promise &lt;any&gt;</span></span>


### <a name="resolve"></a><span data-ttu-id="f19e0-152">解決</span><span class="sxs-lookup"><span data-stu-id="f19e0-152">resolve</span></span>
<span data-ttu-id="f19e0-153">resolve &lt;T&gt; (value?: T &#124; PromiseLike &lt;T&gt;) : Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="f19e0-153">resolve &lt;T&gt;(value?: T &#124; PromiseLike &lt;T&gt;): Promise &lt;T&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="f19e0-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f19e0-154">Parameters</span></span>

| <span data-ttu-id="f19e0-155">氏名</span><span class="sxs-lookup"><span data-stu-id="f19e0-155">Name</span></span> | <span data-ttu-id="f19e0-156">型</span><span class="sxs-lookup"><span data-stu-id="f19e0-156">Type</span></span> | <span data-ttu-id="f19e0-157">説明</span><span class="sxs-lookup"><span data-stu-id="f19e0-157">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f19e0-158">value?</span><span class="sxs-lookup"><span data-stu-id="f19e0-158">value?</span></span>|<span data-ttu-id="f19e0-159">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="f19e0-159">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-promise-lttgt"></a><span data-ttu-id="f19e0-160">Promise &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="f19e0-160">Returns Promise &lt;T&gt;</span></span>

