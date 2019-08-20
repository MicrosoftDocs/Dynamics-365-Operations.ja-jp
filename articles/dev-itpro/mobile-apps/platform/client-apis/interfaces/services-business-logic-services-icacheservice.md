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
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8dc85a58a26e86b784cc3547d4eaa3d00178f870
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851627"
---
# <a name="cacheservice-type"></a><span data-ttu-id="38e0c-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="38e0c-103">CacheService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="38e0c-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="38e0c-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="38e0c-105">階層</span><span class="sxs-lookup"><span data-stu-id="38e0c-105">Hierarchy</span></span>

<span data-ttu-id="38e0c-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="38e0c-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="38e0c-107">指数</span><span class="sxs-lookup"><span data-stu-id="38e0c-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="38e0c-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="38e0c-108">Methods</span></span>

* [<span data-ttu-id="38e0c-109">getData</span><span class="sxs-lookup"><span data-stu-id="38e0c-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="38e0c-110">setData</span><span class="sxs-lookup"><span data-stu-id="38e0c-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="38e0c-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="38e0c-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="38e0c-112">getData</span><span class="sxs-lookup"><span data-stu-id="38e0c-112">getData</span></span>


<span data-ttu-id="38e0c-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="38e0c-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="38e0c-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38e0c-114">Parameters</span></span>

| <span data-ttu-id="38e0c-115">氏名</span><span class="sxs-lookup"><span data-stu-id="38e0c-115">Name</span></span> | <span data-ttu-id="38e0c-116">種類</span><span class="sxs-lookup"><span data-stu-id="38e0c-116">Type</span></span> | <span data-ttu-id="38e0c-117">説明</span><span class="sxs-lookup"><span data-stu-id="38e0c-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="38e0c-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="38e0c-118">cacheKey</span></span>|<span data-ttu-id="38e0c-119">string</span><span class="sxs-lookup"><span data-stu-id="38e0c-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="38e0c-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="38e0c-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="38e0c-121">setData</span><span class="sxs-lookup"><span data-stu-id="38e0c-121">setData</span></span>


<span data-ttu-id="38e0c-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="38e0c-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="38e0c-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38e0c-123">Parameters</span></span>

| <span data-ttu-id="38e0c-124">氏名</span><span class="sxs-lookup"><span data-stu-id="38e0c-124">Name</span></span> | <span data-ttu-id="38e0c-125">種類</span><span class="sxs-lookup"><span data-stu-id="38e0c-125">Type</span></span> | <span data-ttu-id="38e0c-126">説明</span><span class="sxs-lookup"><span data-stu-id="38e0c-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="38e0c-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="38e0c-127">cacheKey</span></span>|<span data-ttu-id="38e0c-128">string</span><span class="sxs-lookup"><span data-stu-id="38e0c-128">string</span></span>||
| <span data-ttu-id="38e0c-129">データ</span><span class="sxs-lookup"><span data-stu-id="38e0c-129">data</span></span>|<span data-ttu-id="38e0c-130">any</span><span class="sxs-lookup"><span data-stu-id="38e0c-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="38e0c-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="38e0c-131">Returns any</span></span>

