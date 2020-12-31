---
title: CacheService タイプ
description: デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 04153cc483e092214267239b61e7f3adb7c249ef
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679240"
---
# <a name="cacheservice-type"></a><span data-ttu-id="13b12-103">CacheService タイプ</span><span class="sxs-lookup"><span data-stu-id="13b12-103">CacheService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="13b12-104">デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="13b12-104">Provides ability to access data from the device cache and update data into the device cache.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="13b12-105">階層</span><span class="sxs-lookup"><span data-stu-id="13b12-105">Hierarchy</span></span>

<span data-ttu-id="13b12-106">CacheService</span><span class="sxs-lookup"><span data-stu-id="13b12-106">CacheService</span></span> <br>

## <a name="index"></a><span data-ttu-id="13b12-107">指数</span><span class="sxs-lookup"><span data-stu-id="13b12-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="13b12-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="13b12-108">Methods</span></span>

* [<span data-ttu-id="13b12-109">getData</span><span class="sxs-lookup"><span data-stu-id="13b12-109">getData</span></span>](services-business-logic-services-icacheservice.md#getdata)
* [<span data-ttu-id="13b12-110">setData</span><span class="sxs-lookup"><span data-stu-id="13b12-110">setData</span></span>](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a><span data-ttu-id="13b12-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="13b12-111">Methods</span></span>

### <a name="getdata"></a><span data-ttu-id="13b12-112">getData</span><span class="sxs-lookup"><span data-stu-id="13b12-112">getData</span></span>


<span data-ttu-id="13b12-113">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="13b12-113">getData(cacheKey: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="13b12-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="13b12-114">Parameters</span></span>

| <span data-ttu-id="13b12-115">氏名</span><span class="sxs-lookup"><span data-stu-id="13b12-115">Name</span></span> | <span data-ttu-id="13b12-116">種類</span><span class="sxs-lookup"><span data-stu-id="13b12-116">Type</span></span> | <span data-ttu-id="13b12-117">説明</span><span class="sxs-lookup"><span data-stu-id="13b12-117">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="13b12-118">cacheKey</span><span class="sxs-lookup"><span data-stu-id="13b12-118">cacheKey</span></span>|<span data-ttu-id="13b12-119">string</span><span class="sxs-lookup"><span data-stu-id="13b12-119">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="13b12-120">any を返します</span><span class="sxs-lookup"><span data-stu-id="13b12-120">Returns any</span></span>

### <a name="setdata"></a><span data-ttu-id="13b12-121">setData</span><span class="sxs-lookup"><span data-stu-id="13b12-121">setData</span></span>


<span data-ttu-id="13b12-122">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="13b12-122">setData(cacheKey: string, data: any): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="13b12-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="13b12-123">Parameters</span></span>

| <span data-ttu-id="13b12-124">氏名</span><span class="sxs-lookup"><span data-stu-id="13b12-124">Name</span></span> | <span data-ttu-id="13b12-125">種類</span><span class="sxs-lookup"><span data-stu-id="13b12-125">Type</span></span> | <span data-ttu-id="13b12-126">説明</span><span class="sxs-lookup"><span data-stu-id="13b12-126">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="13b12-127">cacheKey</span><span class="sxs-lookup"><span data-stu-id="13b12-127">cacheKey</span></span>|<span data-ttu-id="13b12-128">string</span><span class="sxs-lookup"><span data-stu-id="13b12-128">string</span></span>||
| <span data-ttu-id="13b12-129">データ</span><span class="sxs-lookup"><span data-stu-id="13b12-129">data</span></span>|<span data-ttu-id="13b12-130">any</span><span class="sxs-lookup"><span data-stu-id="13b12-130">any</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="13b12-131">any を返します</span><span class="sxs-lookup"><span data-stu-id="13b12-131">Returns any</span></span>

