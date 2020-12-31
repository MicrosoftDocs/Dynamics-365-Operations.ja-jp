---
title: DataService タイプ
description: アプリケーション ワークスペースの下でデータ アクセス機能を提供します。
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
ms.openlocfilehash: 10ef31bcff5eee93b3f0925ce3d8b34a999e275a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687853"
---
# <a name="dataservice-type"></a><span data-ttu-id="21936-103">DataService タイプ</span><span class="sxs-lookup"><span data-stu-id="21936-103">DataService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="21936-104">アプリケーション ワークスペースの下でデータ アクセス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="21936-104">Provides ability access data under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="21936-105">階層</span><span class="sxs-lookup"><span data-stu-id="21936-105">Hierarchy</span></span>

<span data-ttu-id="21936-106">DataService</span><span class="sxs-lookup"><span data-stu-id="21936-106">DataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="21936-107">指数</span><span class="sxs-lookup"><span data-stu-id="21936-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="21936-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="21936-108">Methods</span></span>

* [<span data-ttu-id="21936-109">findEntityData</span><span class="sxs-lookup"><span data-stu-id="21936-109">findEntityData</span></span>](services-business-logic-services-idataservice.md#findentitydata)
* [<span data-ttu-id="21936-110">getEntityData</span><span class="sxs-lookup"><span data-stu-id="21936-110">getEntityData</span></span>](services-business-logic-services-idataservice.md#getentitydata)
* [<span data-ttu-id="21936-111">getPageData</span><span class="sxs-lookup"><span data-stu-id="21936-111">getPageData</span></span>](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a><span data-ttu-id="21936-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="21936-112">Methods</span></span>

### <a name="findentitydata"></a><span data-ttu-id="21936-113">findEntityData</span><span class="sxs-lookup"><span data-stu-id="21936-113">findEntityData</span></span>


<span data-ttu-id="21936-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="21936-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="21936-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21936-115">Parameters</span></span>

| <span data-ttu-id="21936-116">氏名</span><span class="sxs-lookup"><span data-stu-id="21936-116">Name</span></span> | <span data-ttu-id="21936-117">種類</span><span class="sxs-lookup"><span data-stu-id="21936-117">Type</span></span> | <span data-ttu-id="21936-118">説明</span><span class="sxs-lookup"><span data-stu-id="21936-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="21936-119">entityType</span><span class="sxs-lookup"><span data-stu-id="21936-119">entityType</span></span>|<span data-ttu-id="21936-120">any</span><span class="sxs-lookup"><span data-stu-id="21936-120">any</span></span>||
| <span data-ttu-id="21936-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="21936-121">propertyName</span></span>|<span data-ttu-id="21936-122">string</span><span class="sxs-lookup"><span data-stu-id="21936-122">string</span></span>||
| <span data-ttu-id="21936-123">propertyValue</span><span class="sxs-lookup"><span data-stu-id="21936-123">propertyValue</span></span>|<span data-ttu-id="21936-124">any</span><span class="sxs-lookup"><span data-stu-id="21936-124">any</span></span>||
| <span data-ttu-id="21936-125">includeChanges?</span><span class="sxs-lookup"><span data-stu-id="21936-125">includeChanges?</span></span>|<span data-ttu-id="21936-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="21936-126">boolean</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="21936-127">any を返します</span><span class="sxs-lookup"><span data-stu-id="21936-127">Returns any</span></span>

### <a name="getentitydata"></a><span data-ttu-id="21936-128">getEntityData</span><span class="sxs-lookup"><span data-stu-id="21936-128">getEntityData</span></span>


<span data-ttu-id="21936-129">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="21936-129">getEntityData(entityType: any, entityId: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="21936-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21936-130">Parameters</span></span>

| <span data-ttu-id="21936-131">氏名</span><span class="sxs-lookup"><span data-stu-id="21936-131">Name</span></span> | <span data-ttu-id="21936-132">種類</span><span class="sxs-lookup"><span data-stu-id="21936-132">Type</span></span> | <span data-ttu-id="21936-133">説明</span><span class="sxs-lookup"><span data-stu-id="21936-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="21936-134">entityType</span><span class="sxs-lookup"><span data-stu-id="21936-134">entityType</span></span>|<span data-ttu-id="21936-135">any</span><span class="sxs-lookup"><span data-stu-id="21936-135">any</span></span>||
| <span data-ttu-id="21936-136">entityId</span><span class="sxs-lookup"><span data-stu-id="21936-136">entityId</span></span>|<span data-ttu-id="21936-137">string</span><span class="sxs-lookup"><span data-stu-id="21936-137">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="21936-138">any を返します</span><span class="sxs-lookup"><span data-stu-id="21936-138">Returns any</span></span>

### <a name="getpagedata"></a><span data-ttu-id="21936-139">getPageData</span><span class="sxs-lookup"><span data-stu-id="21936-139">getPageData</span></span>


<span data-ttu-id="21936-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="21936-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="21936-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21936-141">Parameters</span></span>

| <span data-ttu-id="21936-142">氏名</span><span class="sxs-lookup"><span data-stu-id="21936-142">Name</span></span> | <span data-ttu-id="21936-143">種類</span><span class="sxs-lookup"><span data-stu-id="21936-143">Type</span></span> | <span data-ttu-id="21936-144">説明</span><span class="sxs-lookup"><span data-stu-id="21936-144">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="21936-145">pageId</span><span class="sxs-lookup"><span data-stu-id="21936-145">pageId</span></span>|<span data-ttu-id="21936-146">string</span><span class="sxs-lookup"><span data-stu-id="21936-146">string</span></span>||
| <span data-ttu-id="21936-147">context</span><span class="sxs-lookup"><span data-stu-id="21936-147">context</span></span>|<span data-ttu-id="21936-148">any</span><span class="sxs-lookup"><span data-stu-id="21936-148">any</span></span>||
| <span data-ttu-id="21936-149">フィルタ</span><span class="sxs-lookup"><span data-stu-id="21936-149">filter</span></span>|<span data-ttu-id="21936-150">any</span><span class="sxs-lookup"><span data-stu-id="21936-150">any</span></span>||
| <span data-ttu-id="21936-151">allowedStaleness</span><span class="sxs-lookup"><span data-stu-id="21936-151">allowedStaleness</span></span>|<span data-ttu-id="21936-152">数値</span><span class="sxs-lookup"><span data-stu-id="21936-152">number</span></span>||

#### <a name="returns-promise-ltpagedatagt"></a><span data-ttu-id="21936-153">Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="21936-153">Returns Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>

