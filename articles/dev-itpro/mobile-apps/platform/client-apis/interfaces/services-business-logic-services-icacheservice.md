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
ms.openlocfilehash: 97c09131d964a7a9d1affc5cd03696e4581b0e0d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506049"
---
# <a name="cacheservice-type"></a><span data-ttu-id="0fca4-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="0fca4-103">CacheService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="0fca4-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="0fca4-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="0fca4-105">階層</span><span class="sxs-lookup"><span data-stu-id="0fca4-105">Hierarchy</span></span>

<span data-ttu-id="0fca4-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="0fca4-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="0fca4-107">指数</span><span class="sxs-lookup"><span data-stu-id="0fca4-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="0fca4-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="0fca4-108">Methods</span></span>

* [<span data-ttu-id="0fca4-109">getData</span><span class="sxs-lookup"><span data-stu-id="0fca4-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="0fca4-110">setData</span><span class="sxs-lookup"><span data-stu-id="0fca4-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="0fca4-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="0fca4-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="0fca4-112">getData</span><span class="sxs-lookup"><span data-stu-id="0fca4-112">getData</span></span>


<span data-ttu-id="0fca4-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="0fca4-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="0fca4-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0fca4-114">Parameters</span></span>

| <span data-ttu-id="0fca4-115">氏名</span><span class="sxs-lookup"><span data-stu-id="0fca4-115">Name</span></span> | <span data-ttu-id="0fca4-116">種類</span><span class="sxs-lookup"><span data-stu-id="0fca4-116">Type</span></span> | <span data-ttu-id="0fca4-117">説明</span><span class="sxs-lookup"><span data-stu-id="0fca4-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0fca4-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="0fca4-118">cacheKey</span></span>|<span data-ttu-id="0fca4-119">string</span><span class="sxs-lookup"><span data-stu-id="0fca4-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="0fca4-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="0fca4-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="0fca4-121">setData</span><span class="sxs-lookup"><span data-stu-id="0fca4-121">setData</span></span>


<span data-ttu-id="0fca4-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="0fca4-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="0fca4-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0fca4-123">Parameters</span></span>

| <span data-ttu-id="0fca4-124">氏名</span><span class="sxs-lookup"><span data-stu-id="0fca4-124">Name</span></span> | <span data-ttu-id="0fca4-125">種類</span><span class="sxs-lookup"><span data-stu-id="0fca4-125">Type</span></span> | <span data-ttu-id="0fca4-126">説明</span><span class="sxs-lookup"><span data-stu-id="0fca4-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0fca4-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="0fca4-127">cacheKey</span></span>|<span data-ttu-id="0fca4-128">string</span><span class="sxs-lookup"><span data-stu-id="0fca4-128">string</span></span>||
| <span data-ttu-id="0fca4-129">データ</span><span class="sxs-lookup"><span data-stu-id="0fca4-129">data</span></span>|<span data-ttu-id="0fca4-130">any</span><span class="sxs-lookup"><span data-stu-id="0fca4-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="0fca4-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="0fca4-131">Returns any</span></span>

