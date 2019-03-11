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
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c654bc705bfc5a45e38a255e2ffb567c9e4186b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369309"
---
# <a name="deferred-typelttgt"></a><span data-ttu-id="72583-103">延期されたタイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="72583-103">Deferred type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="72583-104">階層</span><span class="sxs-lookup"><span data-stu-id="72583-104">Hierarchy</span></span>

<span data-ttu-id="72583-105">繰延</span><span class="sxs-lookup"><span data-stu-id="72583-105">Deferred</span></span> <br>

## <a name="index"></a><span data-ttu-id="72583-106">指数</span><span class="sxs-lookup"><span data-stu-id="72583-106">Index</span></span>

### <a name="properties"></a><span data-ttu-id="72583-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="72583-107">Properties</span></span>

* [<span data-ttu-id="72583-108">promise</span><span class="sxs-lookup"><span data-stu-id="72583-108">promise</span></span>](defer-ideferred.md#promise)

### <a name="methods"></a><span data-ttu-id="72583-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="72583-109">Methods</span></span>

* [<span data-ttu-id="72583-110">否認</span><span class="sxs-lookup"><span data-stu-id="72583-110">reject</span></span>](defer-ideferred.md#reject)
* [<span data-ttu-id="72583-111">解決</span><span class="sxs-lookup"><span data-stu-id="72583-111">resolve</span></span>](defer-ideferred.md#resolve)

## <a name="properties"></a><span data-ttu-id="72583-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="72583-112">Properties</span></span>

### <a name="promise"></a><span data-ttu-id="72583-113">promise</span><span class="sxs-lookup"><span data-stu-id="72583-113">promise</span></span>

<span data-ttu-id="72583-114">promise: Promise &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="72583-114">promise: Promise &lt;T&gt;</span></span>




## <a name="methods"></a><span data-ttu-id="72583-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="72583-115">Methods</span></span>

### <a name="reject"></a><span data-ttu-id="72583-116">否認</span><span class="sxs-lookup"><span data-stu-id="72583-116">reject</span></span>


<span data-ttu-id="72583-117">reject(error?: any): void</span><span class="sxs-lookup"><span data-stu-id="72583-117">reject(error?: any): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="72583-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="72583-118">Parameters</span></span>

| <span data-ttu-id="72583-119">氏名</span><span class="sxs-lookup"><span data-stu-id="72583-119">Name</span></span> | <span data-ttu-id="72583-120">種類</span><span class="sxs-lookup"><span data-stu-id="72583-120">Type</span></span> | <span data-ttu-id="72583-121">説明</span><span class="sxs-lookup"><span data-stu-id="72583-121">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="72583-122">エラー?</span><span class="sxs-lookup"><span data-stu-id="72583-122">error?</span></span>|<span data-ttu-id="72583-123">any</span><span class="sxs-lookup"><span data-stu-id="72583-123">any</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="72583-124">void を返します</span><span class="sxs-lookup"><span data-stu-id="72583-124">Returns void</span></span>

### <a name="resolve"></a><span data-ttu-id="72583-125">解決</span><span class="sxs-lookup"><span data-stu-id="72583-125">resolve</span></span>


<span data-ttu-id="72583-126">resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void</span><span class="sxs-lookup"><span data-stu-id="72583-126">resolve(value?: T &#124; PromiseLike &lt;T&gt;): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="72583-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="72583-127">Parameters</span></span>

| <span data-ttu-id="72583-128">氏名</span><span class="sxs-lookup"><span data-stu-id="72583-128">Name</span></span> | <span data-ttu-id="72583-129">型</span><span class="sxs-lookup"><span data-stu-id="72583-129">Type</span></span> | <span data-ttu-id="72583-130">説明</span><span class="sxs-lookup"><span data-stu-id="72583-130">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="72583-131">value?</span><span class="sxs-lookup"><span data-stu-id="72583-131">value?</span></span>|<span data-ttu-id="72583-132">T &#124; PromiseLike &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="72583-132">T &#124; PromiseLike &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="72583-133">void を返します</span><span class="sxs-lookup"><span data-stu-id="72583-133">Returns void</span></span>

