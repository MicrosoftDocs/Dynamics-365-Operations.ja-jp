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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191868"
---
# <a name="deferred-typelttgt"></a><span data-ttu-id="7a094-103">延期されたタイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="7a094-103">Deferred type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="7a094-104">階層</span><span class="sxs-lookup"><span data-stu-id="7a094-104">Hierarchy</span></span>

<span data-ttu-id="7a094-105">繰延</span><span class="sxs-lookup"><span data-stu-id="7a094-105">Deferred</span></span> <br>

## <a name="index"></a><span data-ttu-id="7a094-106">指数</span><span class="sxs-lookup"><span data-stu-id="7a094-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="7a094-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a094-107">Properties</span></span>

* [<span data-ttu-id="7a094-108">promise</span><span class="sxs-lookup"><span data-stu-id="7a094-108">promise</span></span>](defer-ideferred.md#promise)

### <a name="methods"></a><span data-ttu-id="7a094-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="7a094-109">Methods</span></span>

* [<span data-ttu-id="7a094-110">否認</span><span class="sxs-lookup"><span data-stu-id="7a094-110">reject</span></span>](defer-ideferred.md#reject)
* [<span data-ttu-id="7a094-111">解決</span><span class="sxs-lookup"><span data-stu-id="7a094-111">resolve</span></span>](defer-ideferred.md#resolve)

## <a name="properties"></a><span data-ttu-id="7a094-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a094-112">Properties</span></span>

### <a name="promise"></a><span data-ttu-id="7a094-113">promise</span><span class="sxs-lookup"><span data-stu-id="7a094-113">promise</span></span>

<span data-ttu-id="7a094-114">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="7a094-114">promise: Promise &lt;T&gt;</span></span>




## <a name="methods"></a><span data-ttu-id="7a094-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="7a094-115">Methods</span></span>

### <a name="reject"></a><span data-ttu-id="7a094-116">否認</span><span class="sxs-lookup"><span data-stu-id="7a094-116">reject</span></span>


<span data-ttu-id="7a094-117">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="7a094-117">reject(error?: any): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="7a094-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a094-118">Parameters</span></span>

| <span data-ttu-id="7a094-119">氏名</span><span class="sxs-lookup"><span data-stu-id="7a094-119">Name</span></span> | <span data-ttu-id="7a094-120">種類</span><span class="sxs-lookup"><span data-stu-id="7a094-120">Type</span></span> | <span data-ttu-id="7a094-121">説明</span><span class="sxs-lookup"><span data-stu-id="7a094-121">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="7a094-122">エラー?</span><span class="sxs-lookup"><span data-stu-id="7a094-122">error?</span></span>|<span data-ttu-id="7a094-123">any</span><span class="sxs-lookup"><span data-stu-id="7a094-123">any</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="7a094-124">void を返します</span><span class="sxs-lookup"><span data-stu-id="7a094-124">Returns void</span></span>

### <a name="resolve"></a><span data-ttu-id="7a094-125">解決</span><span class="sxs-lookup"><span data-stu-id="7a094-125">resolve</span></span>


<span data-ttu-id="7a094-126">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="7a094-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="7a094-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a094-127">Parameters</span></span>

| <span data-ttu-id="7a094-128">氏名</span><span class="sxs-lookup"><span data-stu-id="7a094-128">Name</span></span> | <span data-ttu-id="7a094-129">型</span><span class="sxs-lookup"><span data-stu-id="7a094-129">Type</span></span> | <span data-ttu-id="7a094-130">説明</span><span class="sxs-lookup"><span data-stu-id="7a094-130">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="7a094-131">value?</span><span class="sxs-lookup"><span data-stu-id="7a094-131">value?</span></span>|<span data-ttu-id="7a094-132">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="7a094-132">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="7a094-133">void を返します</span><span class="sxs-lookup"><span data-stu-id="7a094-133">Returns void</span></span>

