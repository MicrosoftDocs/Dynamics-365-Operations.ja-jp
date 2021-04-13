---
title: 繰延タイプ<T>
description: 繰延タイプ
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
ms.openlocfilehash: c13595a2bef37a403b7e6d79accc30fd4e98a6b2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748083"
---
# <a name="deferred-typelttgt"></a><span data-ttu-id="ca524-103">延期されたタイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="ca524-103">Deferred type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="ca524-104">階層</span><span class="sxs-lookup"><span data-stu-id="ca524-104">Hierarchy</span></span>

<span data-ttu-id="ca524-105">繰延</span><span class="sxs-lookup"><span data-stu-id="ca524-105">Deferred</span></span> <br>

## <a name="index"></a><span data-ttu-id="ca524-106">指数</span><span class="sxs-lookup"><span data-stu-id="ca524-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="ca524-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca524-107">Properties</span></span>

* [<span data-ttu-id="ca524-108">promise</span><span class="sxs-lookup"><span data-stu-id="ca524-108">promise</span></span>](defer-ideferred.md#promise)

### <a name="methods"></a><span data-ttu-id="ca524-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="ca524-109">Methods</span></span>

* [<span data-ttu-id="ca524-110">否認</span><span class="sxs-lookup"><span data-stu-id="ca524-110">reject</span></span>](defer-ideferred.md#reject)
* [<span data-ttu-id="ca524-111">解決</span><span class="sxs-lookup"><span data-stu-id="ca524-111">resolve</span></span>](defer-ideferred.md#resolve)

## <a name="properties"></a><span data-ttu-id="ca524-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca524-112">Properties</span></span>

### <a name="promise"></a><span data-ttu-id="ca524-113">promise</span><span class="sxs-lookup"><span data-stu-id="ca524-113">promise</span></span>

<span data-ttu-id="ca524-114">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="ca524-114">promise: Promise &lt;T&gt;</span></span>




## <a name="methods"></a><span data-ttu-id="ca524-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="ca524-115">Methods</span></span>

### <a name="reject"></a><span data-ttu-id="ca524-116">否認</span><span class="sxs-lookup"><span data-stu-id="ca524-116">reject</span></span>


<span data-ttu-id="ca524-117">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="ca524-117">reject(error?: any): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="ca524-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca524-118">Parameters</span></span>

| <span data-ttu-id="ca524-119">氏名</span><span class="sxs-lookup"><span data-stu-id="ca524-119">Name</span></span> | <span data-ttu-id="ca524-120">種類</span><span class="sxs-lookup"><span data-stu-id="ca524-120">Type</span></span> | <span data-ttu-id="ca524-121">説明</span><span class="sxs-lookup"><span data-stu-id="ca524-121">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="ca524-122">エラー?</span><span class="sxs-lookup"><span data-stu-id="ca524-122">error?</span></span>|<span data-ttu-id="ca524-123">any</span><span class="sxs-lookup"><span data-stu-id="ca524-123">any</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="ca524-124">void を返します</span><span class="sxs-lookup"><span data-stu-id="ca524-124">Returns void</span></span>

### <a name="resolve"></a><span data-ttu-id="ca524-125">解決</span><span class="sxs-lookup"><span data-stu-id="ca524-125">resolve</span></span>


<span data-ttu-id="ca524-126">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="ca524-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="ca524-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca524-127">Parameters</span></span>

| <span data-ttu-id="ca524-128">氏名</span><span class="sxs-lookup"><span data-stu-id="ca524-128">Name</span></span> | <span data-ttu-id="ca524-129">型</span><span class="sxs-lookup"><span data-stu-id="ca524-129">Type</span></span> | <span data-ttu-id="ca524-130">説明</span><span class="sxs-lookup"><span data-stu-id="ca524-130">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="ca524-131">value?</span><span class="sxs-lookup"><span data-stu-id="ca524-131">value?</span></span>|<span data-ttu-id="ca524-132">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="ca524-132">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="ca524-133">void を返します</span><span class="sxs-lookup"><span data-stu-id="ca524-133">Returns void</span></span>



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]