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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191837"
---
# <a name="defer-module"></a><span data-ttu-id="8b3fa-103">延期モジュール</span><span class="sxs-lookup"><span data-stu-id="8b3fa-103">Defer module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="8b3fa-104">指数</span><span class="sxs-lookup"><span data-stu-id="8b3fa-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="8b3fa-105">種類</span><span class="sxs-lookup"><span data-stu-id="8b3fa-105">Types</span></span>

* [<span data-ttu-id="8b3fa-106">Deferred</span><span class="sxs-lookup"><span data-stu-id="8b3fa-106">Deferred</span></span>](../interfaces/defer-ideferred.md)

### <a name="functions"></a><span data-ttu-id="8b3fa-107">関数</span><span class="sxs-lookup"><span data-stu-id="8b3fa-107">Functions</span></span>

* [<span data-ttu-id="8b3fa-108">すべて</span><span class="sxs-lookup"><span data-stu-id="8b3fa-108">all</span></span>](defer.md#all)
* [<span data-ttu-id="8b3fa-109">延期</span><span class="sxs-lookup"><span data-stu-id="8b3fa-109">defer</span></span>](defer.md)
* [<span data-ttu-id="8b3fa-110">否認</span><span class="sxs-lookup"><span data-stu-id="8b3fa-110">reject</span></span>](defer.md#reject)
* [<span data-ttu-id="8b3fa-111">解決</span><span class="sxs-lookup"><span data-stu-id="8b3fa-111">resolve</span></span>](defer.md#resolve)

## <a name="types"></a><span data-ttu-id="8b3fa-112">種類</span><span class="sxs-lookup"><span data-stu-id="8b3fa-112">Types</span></span>


### <a name="deferred"></a><span data-ttu-id="8b3fa-113">繰延</span><span class="sxs-lookup"><span data-stu-id="8b3fa-113">Deferred</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="8b3fa-114">階層</span><span class="sxs-lookup"><span data-stu-id="8b3fa-114">Hierarchy</span></span>

<span data-ttu-id="8b3fa-115">繰延</span><span class="sxs-lookup"><span data-stu-id="8b3fa-115">Deferred</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="8b3fa-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8b3fa-116">Properties</span></span>

| <span data-ttu-id="8b3fa-117">氏名</span><span class="sxs-lookup"><span data-stu-id="8b3fa-117">Name</span></span> | <span data-ttu-id="8b3fa-118">署名</span><span class="sxs-lookup"><span data-stu-id="8b3fa-118">Signature</span></span> | <span data-ttu-id="8b3fa-119">説明</span><span class="sxs-lookup"><span data-stu-id="8b3fa-119">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="8b3fa-120">promise</span><span class="sxs-lookup"><span data-stu-id="8b3fa-120">promise</span></span>](../interfaces/defer-ideferred.md#promise) |<span data-ttu-id="8b3fa-121">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="8b3fa-121">promise: Promise &lt;T&gt;</span></span> <br>|  |

#### <a name="methods"></a><span data-ttu-id="8b3fa-122">メソッド</span><span class="sxs-lookup"><span data-stu-id="8b3fa-122">Methods</span></span>

| <span data-ttu-id="8b3fa-123">氏名</span><span class="sxs-lookup"><span data-stu-id="8b3fa-123">Name</span></span> | <span data-ttu-id="8b3fa-124">署名</span><span class="sxs-lookup"><span data-stu-id="8b3fa-124">Signature</span></span> | <span data-ttu-id="8b3fa-125">説明</span><span class="sxs-lookup"><span data-stu-id="8b3fa-125">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="8b3fa-126">否認</span><span class="sxs-lookup"><span data-stu-id="8b3fa-126">reject</span></span>](../interfaces/defer-ideferred.md#reject) |<span data-ttu-id="8b3fa-127">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="8b3fa-127">reject(error?: any): void</span></span>|  |
| [<span data-ttu-id="8b3fa-128">解決</span><span class="sxs-lookup"><span data-stu-id="8b3fa-128">resolve</span></span>](../interfaces/defer-ideferred.md#resolve) |<span data-ttu-id="8b3fa-129">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="8b3fa-129">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>|  |

## <a name="functions"></a><span data-ttu-id="8b3fa-130">ファンクション</span><span class="sxs-lookup"><span data-stu-id="8b3fa-130">Functions</span></span>


### <a name="all"></a><span data-ttu-id="8b3fa-131">すべて</span><span class="sxs-lookup"><span data-stu-id="8b3fa-131">all</span></span>
<span data-ttu-id="8b3fa-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="8b3fa-132">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="8b3fa-133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b3fa-133">Parameters</span></span>

| <span data-ttu-id="8b3fa-134">氏名</span><span class="sxs-lookup"><span data-stu-id="8b3fa-134">Name</span></span> | <span data-ttu-id="8b3fa-135">種類</span><span class="sxs-lookup"><span data-stu-id="8b3fa-135">Type</span></span> | <span data-ttu-id="8b3fa-136">説明</span><span class="sxs-lookup"><span data-stu-id="8b3fa-136">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="8b3fa-137">...args</span><span class="sxs-lookup"><span data-stu-id="8b3fa-137">...args</span></span>|<span data-ttu-id="8b3fa-138">any [ ]</span><span class="sxs-lookup"><span data-stu-id="8b3fa-138">any [ ]</span></span>||

#### <a name="returns-promise-ltany--gt"></a><span data-ttu-id="8b3fa-139">Promise &lt;any [ ]&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="8b3fa-139">Returns Promise &lt;any [ ]&gt;</span></span>


### <a name="defer"></a><span data-ttu-id="8b3fa-140">defer</span><span class="sxs-lookup"><span data-stu-id="8b3fa-140">defer</span></span>
<span data-ttu-id="8b3fa-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="8b3fa-141">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>



#### <a name="returns-deferredinterfacesdefer-ideferredmd-lttgt"></a><span data-ttu-id="8b3fa-142">[Deferred](../interfaces/defer-ideferred.md) &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="8b3fa-142">Returns [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>


### <a name="reject"></a><span data-ttu-id="8b3fa-143">否認</span><span class="sxs-lookup"><span data-stu-id="8b3fa-143">reject</span></span>
<span data-ttu-id="8b3fa-144">reject(error?: any): Promise &lt;any&gt;</span><span class="sxs-lookup"><span data-stu-id="8b3fa-144">reject(error?: any): Promise &lt;any&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="8b3fa-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b3fa-145">Parameters</span></span>

| <span data-ttu-id="8b3fa-146">氏名</span><span class="sxs-lookup"><span data-stu-id="8b3fa-146">Name</span></span> | <span data-ttu-id="8b3fa-147">種類</span><span class="sxs-lookup"><span data-stu-id="8b3fa-147">Type</span></span> | <span data-ttu-id="8b3fa-148">説明</span><span class="sxs-lookup"><span data-stu-id="8b3fa-148">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="8b3fa-149">エラー?</span><span class="sxs-lookup"><span data-stu-id="8b3fa-149">error?</span></span>|<span data-ttu-id="8b3fa-150">any</span><span class="sxs-lookup"><span data-stu-id="8b3fa-150">any</span></span>||

#### <a name="returns-promise-ltanygt"></a><span data-ttu-id="8b3fa-151">Promise &lt;any&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="8b3fa-151">Returns Promise &lt;any&gt;</span></span>


### <a name="resolve"></a><span data-ttu-id="8b3fa-152">解決</span><span class="sxs-lookup"><span data-stu-id="8b3fa-152">resolve</span></span>
<span data-ttu-id="8b3fa-153">resolve &lt;T&gt; (value?: T &#124; PromiseLike &lt;T&gt;) : Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="8b3fa-153">resolve &lt;T&gt;(value?: T &#124; PromiseLike &lt;T&gt;): Promise &lt;T&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="8b3fa-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b3fa-154">Parameters</span></span>

| <span data-ttu-id="8b3fa-155">氏名</span><span class="sxs-lookup"><span data-stu-id="8b3fa-155">Name</span></span> | <span data-ttu-id="8b3fa-156">型</span><span class="sxs-lookup"><span data-stu-id="8b3fa-156">Type</span></span> | <span data-ttu-id="8b3fa-157">説明</span><span class="sxs-lookup"><span data-stu-id="8b3fa-157">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="8b3fa-158">value?</span><span class="sxs-lookup"><span data-stu-id="8b3fa-158">value?</span></span>|<span data-ttu-id="8b3fa-159">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="8b3fa-159">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-promise-lttgt"></a><span data-ttu-id="8b3fa-160">Promise &lt;T&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="8b3fa-160">Returns Promise &lt;T&gt;</span></span>

