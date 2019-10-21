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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183145"
---
# <a name="cacheservice-type"></a><span data-ttu-id="ef456-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="ef456-103">CacheService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="ef456-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="ef456-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="ef456-105">階層</span><span class="sxs-lookup"><span data-stu-id="ef456-105">Hierarchy</span></span>

<span data-ttu-id="ef456-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="ef456-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="ef456-107">指数</span><span class="sxs-lookup"><span data-stu-id="ef456-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="ef456-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="ef456-108">Methods</span></span>

* [<span data-ttu-id="ef456-109">getData</span><span class="sxs-lookup"><span data-stu-id="ef456-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="ef456-110">setData</span><span class="sxs-lookup"><span data-stu-id="ef456-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="ef456-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="ef456-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="ef456-112">getData</span><span class="sxs-lookup"><span data-stu-id="ef456-112">getData</span></span>


<span data-ttu-id="ef456-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="ef456-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="ef456-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ef456-114">Parameters</span></span>

| <span data-ttu-id="ef456-115">氏名</span><span class="sxs-lookup"><span data-stu-id="ef456-115">Name</span></span> | <span data-ttu-id="ef456-116">種類</span><span class="sxs-lookup"><span data-stu-id="ef456-116">Type</span></span> | <span data-ttu-id="ef456-117">説明</span><span class="sxs-lookup"><span data-stu-id="ef456-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="ef456-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="ef456-118">cacheKey</span></span>|<span data-ttu-id="ef456-119">string</span><span class="sxs-lookup"><span data-stu-id="ef456-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="ef456-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="ef456-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="ef456-121">setData</span><span class="sxs-lookup"><span data-stu-id="ef456-121">setData</span></span>


<span data-ttu-id="ef456-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="ef456-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="ef456-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ef456-123">Parameters</span></span>

| <span data-ttu-id="ef456-124">氏名</span><span class="sxs-lookup"><span data-stu-id="ef456-124">Name</span></span> | <span data-ttu-id="ef456-125">種類</span><span class="sxs-lookup"><span data-stu-id="ef456-125">Type</span></span> | <span data-ttu-id="ef456-126">説明</span><span class="sxs-lookup"><span data-stu-id="ef456-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="ef456-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="ef456-127">cacheKey</span></span>|<span data-ttu-id="ef456-128">string</span><span class="sxs-lookup"><span data-stu-id="ef456-128">string</span></span>||
| <span data-ttu-id="ef456-129">データ</span><span class="sxs-lookup"><span data-stu-id="ef456-129">data</span></span>|<span data-ttu-id="ef456-130">any</span><span class="sxs-lookup"><span data-stu-id="ef456-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="ef456-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="ef456-131">Returns any</span></span>

