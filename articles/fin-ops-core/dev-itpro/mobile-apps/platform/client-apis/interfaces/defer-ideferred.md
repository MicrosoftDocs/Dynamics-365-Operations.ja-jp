---
title: 繰延タイプ<T>
description: 繰延タイプ
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
ms.openlocfilehash: 281099e81d87146cf539c489c1c68d87ee84e96f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685431"
---
# <a name="deferred-typelttgt"></a><span data-ttu-id="72dc3-103">延期されたタイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="72dc3-103">Deferred type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="72dc3-104">階層</span><span class="sxs-lookup"><span data-stu-id="72dc3-104">Hierarchy</span></span>

<span data-ttu-id="72dc3-105">繰延</span><span class="sxs-lookup"><span data-stu-id="72dc3-105">Deferred</span></span> <br>

## <a name="index"></a><span data-ttu-id="72dc3-106">指数</span><span class="sxs-lookup"><span data-stu-id="72dc3-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="72dc3-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="72dc3-107">Properties</span></span>

* [<span data-ttu-id="72dc3-108">promise</span><span class="sxs-lookup"><span data-stu-id="72dc3-108">promise</span></span>](defer-ideferred.md#promise)

### <a name="methods"></a><span data-ttu-id="72dc3-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="72dc3-109">Methods</span></span>

* [<span data-ttu-id="72dc3-110">否認</span><span class="sxs-lookup"><span data-stu-id="72dc3-110">reject</span></span>](defer-ideferred.md#reject)
* [<span data-ttu-id="72dc3-111">解決</span><span class="sxs-lookup"><span data-stu-id="72dc3-111">resolve</span></span>](defer-ideferred.md#resolve)

## <a name="properties"></a><span data-ttu-id="72dc3-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="72dc3-112">Properties</span></span>

### <a name="promise"></a><span data-ttu-id="72dc3-113">promise</span><span class="sxs-lookup"><span data-stu-id="72dc3-113">promise</span></span>

<span data-ttu-id="72dc3-114">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="72dc3-114">promise: Promise &lt;T&gt;</span></span>




## <a name="methods"></a><span data-ttu-id="72dc3-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="72dc3-115">Methods</span></span>

### <a name="reject"></a><span data-ttu-id="72dc3-116">否認</span><span class="sxs-lookup"><span data-stu-id="72dc3-116">reject</span></span>


<span data-ttu-id="72dc3-117">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="72dc3-117">reject(error?: any): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="72dc3-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="72dc3-118">Parameters</span></span>

| <span data-ttu-id="72dc3-119">氏名</span><span class="sxs-lookup"><span data-stu-id="72dc3-119">Name</span></span> | <span data-ttu-id="72dc3-120">種類</span><span class="sxs-lookup"><span data-stu-id="72dc3-120">Type</span></span> | <span data-ttu-id="72dc3-121">説明</span><span class="sxs-lookup"><span data-stu-id="72dc3-121">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="72dc3-122">エラー?</span><span class="sxs-lookup"><span data-stu-id="72dc3-122">error?</span></span>|<span data-ttu-id="72dc3-123">any</span><span class="sxs-lookup"><span data-stu-id="72dc3-123">any</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="72dc3-124">void を返します</span><span class="sxs-lookup"><span data-stu-id="72dc3-124">Returns void</span></span>

### <a name="resolve"></a><span data-ttu-id="72dc3-125">解決</span><span class="sxs-lookup"><span data-stu-id="72dc3-125">resolve</span></span>


<span data-ttu-id="72dc3-126">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="72dc3-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="72dc3-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="72dc3-127">Parameters</span></span>

| <span data-ttu-id="72dc3-128">氏名</span><span class="sxs-lookup"><span data-stu-id="72dc3-128">Name</span></span> | <span data-ttu-id="72dc3-129">型</span><span class="sxs-lookup"><span data-stu-id="72dc3-129">Type</span></span> | <span data-ttu-id="72dc3-130">説明</span><span class="sxs-lookup"><span data-stu-id="72dc3-130">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="72dc3-131">value?</span><span class="sxs-lookup"><span data-stu-id="72dc3-131">value?</span></span>|<span data-ttu-id="72dc3-132">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="72dc3-132">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="72dc3-133">void を返します</span><span class="sxs-lookup"><span data-stu-id="72dc3-133">Returns void</span></span>

