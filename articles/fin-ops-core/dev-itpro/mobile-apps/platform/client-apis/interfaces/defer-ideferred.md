---
title: 繰延タイプ<T>
description: 繰延タイプ
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
ms.openlocfilehash: 86d58e79110df88c5a96c8f62f739dd06c19a8c7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983967"
---
# <a name="deferred-typelttgt"></a><span data-ttu-id="3ad88-103">延期されたタイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="3ad88-103">Deferred type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="3ad88-104">階層</span><span class="sxs-lookup"><span data-stu-id="3ad88-104">Hierarchy</span></span>

<span data-ttu-id="3ad88-105">繰延</span><span class="sxs-lookup"><span data-stu-id="3ad88-105">Deferred</span></span> <br>

## <a name="index"></a><span data-ttu-id="3ad88-106">指数</span><span class="sxs-lookup"><span data-stu-id="3ad88-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="3ad88-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ad88-107">Properties</span></span>

* [<span data-ttu-id="3ad88-108">promise</span><span class="sxs-lookup"><span data-stu-id="3ad88-108">promise</span></span>](defer-ideferred.md#promise)

### <a name="methods"></a><span data-ttu-id="3ad88-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="3ad88-109">Methods</span></span>

* [<span data-ttu-id="3ad88-110">否認</span><span class="sxs-lookup"><span data-stu-id="3ad88-110">reject</span></span>](defer-ideferred.md#reject)
* [<span data-ttu-id="3ad88-111">解決</span><span class="sxs-lookup"><span data-stu-id="3ad88-111">resolve</span></span>](defer-ideferred.md#resolve)

## <a name="properties"></a><span data-ttu-id="3ad88-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3ad88-112">Properties</span></span>

### <a name="promise"></a><span data-ttu-id="3ad88-113">promise</span><span class="sxs-lookup"><span data-stu-id="3ad88-113">promise</span></span>

<span data-ttu-id="3ad88-114">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="3ad88-114">promise: Promise &lt;T&gt;</span></span>




## <a name="methods"></a><span data-ttu-id="3ad88-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="3ad88-115">Methods</span></span>

### <a name="reject"></a><span data-ttu-id="3ad88-116">否認</span><span class="sxs-lookup"><span data-stu-id="3ad88-116">reject</span></span>


<span data-ttu-id="3ad88-117">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="3ad88-117">reject(error?: any): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="3ad88-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3ad88-118">Parameters</span></span>

| <span data-ttu-id="3ad88-119">氏名</span><span class="sxs-lookup"><span data-stu-id="3ad88-119">Name</span></span> | <span data-ttu-id="3ad88-120">種類</span><span class="sxs-lookup"><span data-stu-id="3ad88-120">Type</span></span> | <span data-ttu-id="3ad88-121">説明</span><span class="sxs-lookup"><span data-stu-id="3ad88-121">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="3ad88-122">エラー?</span><span class="sxs-lookup"><span data-stu-id="3ad88-122">error?</span></span>|<span data-ttu-id="3ad88-123">any</span><span class="sxs-lookup"><span data-stu-id="3ad88-123">any</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="3ad88-124">void を返します</span><span class="sxs-lookup"><span data-stu-id="3ad88-124">Returns void</span></span>

### <a name="resolve"></a><span data-ttu-id="3ad88-125">解決</span><span class="sxs-lookup"><span data-stu-id="3ad88-125">resolve</span></span>


<span data-ttu-id="3ad88-126">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="3ad88-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="3ad88-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3ad88-127">Parameters</span></span>

| <span data-ttu-id="3ad88-128">氏名</span><span class="sxs-lookup"><span data-stu-id="3ad88-128">Name</span></span> | <span data-ttu-id="3ad88-129">型</span><span class="sxs-lookup"><span data-stu-id="3ad88-129">Type</span></span> | <span data-ttu-id="3ad88-130">説明</span><span class="sxs-lookup"><span data-stu-id="3ad88-130">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="3ad88-131">value?</span><span class="sxs-lookup"><span data-stu-id="3ad88-131">value?</span></span>|<span data-ttu-id="3ad88-132">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="3ad88-132">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="3ad88-133">void を返します</span><span class="sxs-lookup"><span data-stu-id="3ad88-133">Returns void</span></span>

