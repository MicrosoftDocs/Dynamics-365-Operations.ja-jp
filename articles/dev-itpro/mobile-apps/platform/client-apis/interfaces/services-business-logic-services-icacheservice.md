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
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5eb916a10a8751ccd51b2282ec3af1d44a6d5fa9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368439"
---
# <a name="cacheservice-type"></a><span data-ttu-id="c4578-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="c4578-103">CacheService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="c4578-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4578-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="c4578-105">階層</span><span class="sxs-lookup"><span data-stu-id="c4578-105">Hierarchy</span></span>

<span data-ttu-id="c4578-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="c4578-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="c4578-107">指数</span><span class="sxs-lookup"><span data-stu-id="c4578-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="c4578-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="c4578-108">Methods</span></span>

* [<span data-ttu-id="c4578-109">getData</span><span class="sxs-lookup"><span data-stu-id="c4578-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="c4578-110">setData</span><span class="sxs-lookup"><span data-stu-id="c4578-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="c4578-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="c4578-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="c4578-112">getData</span><span class="sxs-lookup"><span data-stu-id="c4578-112">getData</span></span>


<span data-ttu-id="c4578-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="c4578-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="c4578-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4578-114">Parameters</span></span>

| <span data-ttu-id="c4578-115">氏名</span><span class="sxs-lookup"><span data-stu-id="c4578-115">Name</span></span> | <span data-ttu-id="c4578-116">種類</span><span class="sxs-lookup"><span data-stu-id="c4578-116">Type</span></span> | <span data-ttu-id="c4578-117">説明</span><span class="sxs-lookup"><span data-stu-id="c4578-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="c4578-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="c4578-118">cacheKey</span></span>|<span data-ttu-id="c4578-119">string</span><span class="sxs-lookup"><span data-stu-id="c4578-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="c4578-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="c4578-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="c4578-121">setData</span><span class="sxs-lookup"><span data-stu-id="c4578-121">setData</span></span>


<span data-ttu-id="c4578-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="c4578-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="c4578-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4578-123">Parameters</span></span>

| <span data-ttu-id="c4578-124">氏名</span><span class="sxs-lookup"><span data-stu-id="c4578-124">Name</span></span> | <span data-ttu-id="c4578-125">種類</span><span class="sxs-lookup"><span data-stu-id="c4578-125">Type</span></span> | <span data-ttu-id="c4578-126">説明</span><span class="sxs-lookup"><span data-stu-id="c4578-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="c4578-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="c4578-127">cacheKey</span></span>|<span data-ttu-id="c4578-128">string</span><span class="sxs-lookup"><span data-stu-id="c4578-128">string</span></span>||
| <span data-ttu-id="c4578-129">データ</span><span class="sxs-lookup"><span data-stu-id="c4578-129">data</span></span>|<span data-ttu-id="c4578-130">any</span><span class="sxs-lookup"><span data-stu-id="c4578-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="c4578-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="c4578-131">Returns any</span></span>

