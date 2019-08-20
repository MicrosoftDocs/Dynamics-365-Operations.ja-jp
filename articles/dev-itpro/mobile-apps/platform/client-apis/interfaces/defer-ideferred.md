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
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4e8304ed0427db1862cfc04163b132f6e7f0b322
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851637"
---
# <a name="deferred-typelttgt"></a><span data-ttu-id="63fd1-103">延期されたタイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="63fd1-103">Deferred type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="63fd1-104">階層</span><span class="sxs-lookup"><span data-stu-id="63fd1-104">Hierarchy</span></span>

<span data-ttu-id="63fd1-105">繰延</span><span class="sxs-lookup"><span data-stu-id="63fd1-105">Deferred</span></span> <br>

## <a name="index"></a><span data-ttu-id="63fd1-106">指数</span><span class="sxs-lookup"><span data-stu-id="63fd1-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="63fd1-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="63fd1-107">Properties</span></span>

* [<span data-ttu-id="63fd1-108">promise</span><span class="sxs-lookup"><span data-stu-id="63fd1-108">promise</span></span>](defer-ideferred.md#promise)

### <a name="methods"></a><span data-ttu-id="63fd1-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="63fd1-109">Methods</span></span>

* [<span data-ttu-id="63fd1-110">否認</span><span class="sxs-lookup"><span data-stu-id="63fd1-110">reject</span></span>](defer-ideferred.md#reject)
* [<span data-ttu-id="63fd1-111">解決</span><span class="sxs-lookup"><span data-stu-id="63fd1-111">resolve</span></span>](defer-ideferred.md#resolve)

## <a name="properties"></a><span data-ttu-id="63fd1-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="63fd1-112">Properties</span></span>

### <a name="promise"></a><span data-ttu-id="63fd1-113">promise</span><span class="sxs-lookup"><span data-stu-id="63fd1-113">promise</span></span>

<span data-ttu-id="63fd1-114">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="63fd1-114">promise: Promise &lt;T&gt;</span></span>




## <a name="methods"></a><span data-ttu-id="63fd1-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="63fd1-115">Methods</span></span>

### <a name="reject"></a><span data-ttu-id="63fd1-116">否認</span><span class="sxs-lookup"><span data-stu-id="63fd1-116">reject</span></span>


<span data-ttu-id="63fd1-117">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="63fd1-117">reject(error?: any): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="63fd1-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63fd1-118">Parameters</span></span>

| <span data-ttu-id="63fd1-119">氏名</span><span class="sxs-lookup"><span data-stu-id="63fd1-119">Name</span></span> | <span data-ttu-id="63fd1-120">種類</span><span class="sxs-lookup"><span data-stu-id="63fd1-120">Type</span></span> | <span data-ttu-id="63fd1-121">説明</span><span class="sxs-lookup"><span data-stu-id="63fd1-121">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="63fd1-122">エラー?</span><span class="sxs-lookup"><span data-stu-id="63fd1-122">error?</span></span>|<span data-ttu-id="63fd1-123">any</span><span class="sxs-lookup"><span data-stu-id="63fd1-123">any</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="63fd1-124">void を返します</span><span class="sxs-lookup"><span data-stu-id="63fd1-124">Returns void</span></span>

### <a name="resolve"></a><span data-ttu-id="63fd1-125">解決</span><span class="sxs-lookup"><span data-stu-id="63fd1-125">resolve</span></span>


<span data-ttu-id="63fd1-126">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="63fd1-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="63fd1-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63fd1-127">Parameters</span></span>

| <span data-ttu-id="63fd1-128">氏名</span><span class="sxs-lookup"><span data-stu-id="63fd1-128">Name</span></span> | <span data-ttu-id="63fd1-129">型</span><span class="sxs-lookup"><span data-stu-id="63fd1-129">Type</span></span> | <span data-ttu-id="63fd1-130">説明</span><span class="sxs-lookup"><span data-stu-id="63fd1-130">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="63fd1-131">value?</span><span class="sxs-lookup"><span data-stu-id="63fd1-131">value?</span></span>|<span data-ttu-id="63fd1-132">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="63fd1-132">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="63fd1-133">void を返します</span><span class="sxs-lookup"><span data-stu-id="63fd1-133">Returns void</span></span>

