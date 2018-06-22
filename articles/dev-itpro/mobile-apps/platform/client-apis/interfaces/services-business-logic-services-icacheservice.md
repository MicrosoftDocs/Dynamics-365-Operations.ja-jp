---
title: CacheService
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a5047537759406e1ab07b8ebb1bbf1ae85abdd4f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="cacheservice-type"></a><span data-ttu-id="ddc23-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="ddc23-103">CacheService Type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="ddc23-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="ddc23-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="ddc23-105">階層</span><span class="sxs-lookup"><span data-stu-id="ddc23-105">Hierarchy</span></span>

<span data-ttu-id="ddc23-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="ddc23-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="ddc23-107">指数</span><span class="sxs-lookup"><span data-stu-id="ddc23-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="ddc23-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="ddc23-108">Methods</span></span>

* [<span data-ttu-id="ddc23-109">getData</span><span class="sxs-lookup"><span data-stu-id="ddc23-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="ddc23-110">setData</span><span class="sxs-lookup"><span data-stu-id="ddc23-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="ddc23-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="ddc23-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="ddc23-112">getData</span><span class="sxs-lookup"><span data-stu-id="ddc23-112">getData</span></span>


<span data-ttu-id="ddc23-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="ddc23-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="ddc23-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ddc23-114">Parameters</span></span>

| <span data-ttu-id="ddc23-115">氏名</span><span class="sxs-lookup"><span data-stu-id="ddc23-115">Name</span></span> | <span data-ttu-id="ddc23-116">種類</span><span class="sxs-lookup"><span data-stu-id="ddc23-116">Type</span></span> | <span data-ttu-id="ddc23-117">説明</span><span class="sxs-lookup"><span data-stu-id="ddc23-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="ddc23-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="ddc23-118">cacheKey</span></span>|<span data-ttu-id="ddc23-119">string</span><span class="sxs-lookup"><span data-stu-id="ddc23-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="ddc23-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="ddc23-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="ddc23-121">setData</span><span class="sxs-lookup"><span data-stu-id="ddc23-121">setData</span></span>


<span data-ttu-id="ddc23-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="ddc23-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="ddc23-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ddc23-123">Parameters</span></span>

| <span data-ttu-id="ddc23-124">氏名</span><span class="sxs-lookup"><span data-stu-id="ddc23-124">Name</span></span> | <span data-ttu-id="ddc23-125">種類</span><span class="sxs-lookup"><span data-stu-id="ddc23-125">Type</span></span> | <span data-ttu-id="ddc23-126">説明</span><span class="sxs-lookup"><span data-stu-id="ddc23-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="ddc23-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="ddc23-127">cacheKey</span></span>|<span data-ttu-id="ddc23-128">string</span><span class="sxs-lookup"><span data-stu-id="ddc23-128">string</span></span>||
| <span data-ttu-id="ddc23-129">データ</span><span class="sxs-lookup"><span data-stu-id="ddc23-129">data</span></span>|<span data-ttu-id="ddc23-130">any</span><span class="sxs-lookup"><span data-stu-id="ddc23-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="ddc23-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="ddc23-131">Returns any</span></span>


