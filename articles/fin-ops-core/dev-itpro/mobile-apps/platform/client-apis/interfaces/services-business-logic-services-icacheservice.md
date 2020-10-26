---
title: CacheService タイプ
description: デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。
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
ms.openlocfilehash: 41a33662aa0d8015891717a5919f8cc2de3d466d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980574"
---
# <a name="cacheservice-type"></a><span data-ttu-id="f2380-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="f2380-103">CacheService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="f2380-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2380-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="f2380-105">階層</span><span class="sxs-lookup"><span data-stu-id="f2380-105">Hierarchy</span></span>

<span data-ttu-id="f2380-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="f2380-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="f2380-107">指数</span><span class="sxs-lookup"><span data-stu-id="f2380-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="f2380-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f2380-108">Methods</span></span>

* [<span data-ttu-id="f2380-109">getData</span><span class="sxs-lookup"><span data-stu-id="f2380-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="f2380-110">setData</span><span class="sxs-lookup"><span data-stu-id="f2380-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="f2380-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="f2380-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="f2380-112">getData</span><span class="sxs-lookup"><span data-stu-id="f2380-112">getData</span></span>


<span data-ttu-id="f2380-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="f2380-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="f2380-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2380-114">Parameters</span></span>

| <span data-ttu-id="f2380-115">氏名</span><span class="sxs-lookup"><span data-stu-id="f2380-115">Name</span></span> | <span data-ttu-id="f2380-116">種類</span><span class="sxs-lookup"><span data-stu-id="f2380-116">Type</span></span> | <span data-ttu-id="f2380-117">説明</span><span class="sxs-lookup"><span data-stu-id="f2380-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f2380-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="f2380-118">cacheKey</span></span>|<span data-ttu-id="f2380-119">string</span><span class="sxs-lookup"><span data-stu-id="f2380-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="f2380-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="f2380-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="f2380-121">setData</span><span class="sxs-lookup"><span data-stu-id="f2380-121">setData</span></span>


<span data-ttu-id="f2380-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="f2380-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="f2380-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2380-123">Parameters</span></span>

| <span data-ttu-id="f2380-124">氏名</span><span class="sxs-lookup"><span data-stu-id="f2380-124">Name</span></span> | <span data-ttu-id="f2380-125">種類</span><span class="sxs-lookup"><span data-stu-id="f2380-125">Type</span></span> | <span data-ttu-id="f2380-126">説明</span><span class="sxs-lookup"><span data-stu-id="f2380-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f2380-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="f2380-127">cacheKey</span></span>|<span data-ttu-id="f2380-128">string</span><span class="sxs-lookup"><span data-stu-id="f2380-128">string</span></span>||
| <span data-ttu-id="f2380-129">データ</span><span class="sxs-lookup"><span data-stu-id="f2380-129">data</span></span>|<span data-ttu-id="f2380-130">any</span><span class="sxs-lookup"><span data-stu-id="f2380-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="f2380-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="f2380-131">Returns any</span></span>

