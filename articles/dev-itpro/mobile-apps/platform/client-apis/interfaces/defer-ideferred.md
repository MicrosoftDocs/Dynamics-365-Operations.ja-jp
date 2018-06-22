---
title: "繰延"
description: "繰延タイプ"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a52c2d5a992f11f69daa949223e4e2ef69ec562a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="deferred-typelttgt"></a><span data-ttu-id="35e6b-103">延期されたタイプ &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="35e6b-103">Deferred Type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="35e6b-104">階層</span><span class="sxs-lookup"><span data-stu-id="35e6b-104">Hierarchy</span></span>

<span data-ttu-id="35e6b-105">繰延</span><span class="sxs-lookup"><span data-stu-id="35e6b-105">Deferred</span></span> <br>

## <a name="index"></a><span data-ttu-id="35e6b-106">指数</span><span class="sxs-lookup"><span data-stu-id="35e6b-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="35e6b-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="35e6b-107">Properties</span></span>

* [<span data-ttu-id="35e6b-108">promise</span><span class="sxs-lookup"><span data-stu-id="35e6b-108">promise</span></span>](defer-ideferred.md#promise)

### <a name="methods"></a><span data-ttu-id="35e6b-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="35e6b-109">Methods</span></span>

* [<span data-ttu-id="35e6b-110">否認</span><span class="sxs-lookup"><span data-stu-id="35e6b-110">reject</span></span>](defer-ideferred.md#reject)
* [<span data-ttu-id="35e6b-111">解決</span><span class="sxs-lookup"><span data-stu-id="35e6b-111">resolve</span></span>](defer-ideferred.md#resolve)

## <a name="properties"></a><span data-ttu-id="35e6b-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="35e6b-112">Properties</span></span>

### <a name="promise"></a><span data-ttu-id="35e6b-113">promise</span><span class="sxs-lookup"><span data-stu-id="35e6b-113">promise</span></span>

<span data-ttu-id="35e6b-114">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="35e6b-114">promise: Promise &lt;T&gt;</span></span>




## <a name="methods"></a><span data-ttu-id="35e6b-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="35e6b-115">Methods</span></span>

### <a name="reject"></a><span data-ttu-id="35e6b-116">否認</span><span class="sxs-lookup"><span data-stu-id="35e6b-116">reject</span></span>


<span data-ttu-id="35e6b-117">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="35e6b-117">reject(error?: any): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="35e6b-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35e6b-118">Parameters</span></span>

| <span data-ttu-id="35e6b-119">氏名</span><span class="sxs-lookup"><span data-stu-id="35e6b-119">Name</span></span> | <span data-ttu-id="35e6b-120">種類</span><span class="sxs-lookup"><span data-stu-id="35e6b-120">Type</span></span> | <span data-ttu-id="35e6b-121">説明</span><span class="sxs-lookup"><span data-stu-id="35e6b-121">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="35e6b-122">エラー?</span><span class="sxs-lookup"><span data-stu-id="35e6b-122">error?</span></span>|<span data-ttu-id="35e6b-123">any</span><span class="sxs-lookup"><span data-stu-id="35e6b-123">any</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="35e6b-124">void を返します</span><span class="sxs-lookup"><span data-stu-id="35e6b-124">Returns void</span></span>

### <a name="resolve"></a><span data-ttu-id="35e6b-125">解決</span><span class="sxs-lookup"><span data-stu-id="35e6b-125">resolve</span></span>


<span data-ttu-id="35e6b-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="35e6b-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="35e6b-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35e6b-127">Parameters</span></span>

| <span data-ttu-id="35e6b-128">氏名</span><span class="sxs-lookup"><span data-stu-id="35e6b-128">Name</span></span> | <span data-ttu-id="35e6b-129">種類</span><span class="sxs-lookup"><span data-stu-id="35e6b-129">Type</span></span> | <span data-ttu-id="35e6b-130">説明</span><span class="sxs-lookup"><span data-stu-id="35e6b-130">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="35e6b-131">value?</span><span class="sxs-lookup"><span data-stu-id="35e6b-131">value?</span></span>|<span data-ttu-id="35e6b-132">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="35e6b-132">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="35e6b-133">void を返します</span><span class="sxs-lookup"><span data-stu-id="35e6b-133">Returns void</span></span>


