---
title: "CacheService タイプ"
description: "デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。"
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
ms.sourcegitcommit: ed6cabcc8c76fba3d4414cd4b564b720c54169e0
ms.openlocfilehash: 5eb916a10a8751ccd51b2282ec3af1d44a6d5fa9
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="cacheservice-type"></a><span data-ttu-id="15279-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="15279-103">CacheService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="15279-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="15279-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="15279-105">階層</span><span class="sxs-lookup"><span data-stu-id="15279-105">Hierarchy</span></span>

<span data-ttu-id="15279-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="15279-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="15279-107">指数</span><span class="sxs-lookup"><span data-stu-id="15279-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="15279-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="15279-108">Methods</span></span>

* [<span data-ttu-id="15279-109">getData</span><span class="sxs-lookup"><span data-stu-id="15279-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="15279-110">setData</span><span class="sxs-lookup"><span data-stu-id="15279-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="15279-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="15279-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="15279-112">getData</span><span class="sxs-lookup"><span data-stu-id="15279-112">getData</span></span>


<span data-ttu-id="15279-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="15279-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="15279-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15279-114">Parameters</span></span>

| <span data-ttu-id="15279-115">氏名</span><span class="sxs-lookup"><span data-stu-id="15279-115">Name</span></span> | <span data-ttu-id="15279-116">種類</span><span class="sxs-lookup"><span data-stu-id="15279-116">Type</span></span> | <span data-ttu-id="15279-117">説明</span><span class="sxs-lookup"><span data-stu-id="15279-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="15279-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="15279-118">cacheKey</span></span>|<span data-ttu-id="15279-119">string</span><span class="sxs-lookup"><span data-stu-id="15279-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="15279-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="15279-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="15279-121">setData</span><span class="sxs-lookup"><span data-stu-id="15279-121">setData</span></span>


<span data-ttu-id="15279-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="15279-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="15279-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15279-123">Parameters</span></span>

| <span data-ttu-id="15279-124">氏名</span><span class="sxs-lookup"><span data-stu-id="15279-124">Name</span></span> | <span data-ttu-id="15279-125">種類</span><span class="sxs-lookup"><span data-stu-id="15279-125">Type</span></span> | <span data-ttu-id="15279-126">説明</span><span class="sxs-lookup"><span data-stu-id="15279-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="15279-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="15279-127">cacheKey</span></span>|<span data-ttu-id="15279-128">string</span><span class="sxs-lookup"><span data-stu-id="15279-128">string</span></span>||
| <span data-ttu-id="15279-129">データ</span><span class="sxs-lookup"><span data-stu-id="15279-129">data</span></span>|<span data-ttu-id="15279-130">any</span><span class="sxs-lookup"><span data-stu-id="15279-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="15279-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="15279-131">Returns any</span></span>


