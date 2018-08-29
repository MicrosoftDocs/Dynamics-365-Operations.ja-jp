---
title: "DataService タイプ"
description: "アプリケーション ワークスペースの下でデータ アクセス機能を提供します。"
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
ms.openlocfilehash: 4310a829bbfb1861966b7adebac1c43b6b007653
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="dataservice-type"></a><span data-ttu-id="929db-103">DataService タイプ</span><span class="sxs-lookup"><span data-stu-id="929db-103">DataService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="929db-104">アプリケーション ワークスペースの下でデータ アクセス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="929db-104">Provides ability access data under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="929db-105">階層</span><span class="sxs-lookup"><span data-stu-id="929db-105">Hierarchy</span></span>

<span data-ttu-id="929db-106">DataService</span><span class="sxs-lookup"><span data-stu-id="929db-106">DataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="929db-107">指数</span><span class="sxs-lookup"><span data-stu-id="929db-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="929db-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="929db-108">Methods</span></span>

* [<span data-ttu-id="929db-109">findEntityData</span><span class="sxs-lookup"><span data-stu-id="929db-109">findEntityData</span></span>](services-business-logic-services-idataservice.md#findentitydata)
* [<span data-ttu-id="929db-110">getEntityData</span><span class="sxs-lookup"><span data-stu-id="929db-110">getEntityData</span></span>](services-business-logic-services-idataservice.md#getentitydata)
* [<span data-ttu-id="929db-111">getPageData</span><span class="sxs-lookup"><span data-stu-id="929db-111">getPageData</span></span>](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a><span data-ttu-id="929db-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="929db-112">Methods</span></span>

### <a name="findentitydata"></a><span data-ttu-id="929db-113">findEntityData</span><span class="sxs-lookup"><span data-stu-id="929db-113">findEntityData</span></span>


<span data-ttu-id="929db-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="929db-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="929db-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="929db-115">Parameters</span></span>

| <span data-ttu-id="929db-116">氏名</span><span class="sxs-lookup"><span data-stu-id="929db-116">Name</span></span> | <span data-ttu-id="929db-117">種類</span><span class="sxs-lookup"><span data-stu-id="929db-117">Type</span></span> | <span data-ttu-id="929db-118">説明</span><span class="sxs-lookup"><span data-stu-id="929db-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="929db-119">entityType</span><span class="sxs-lookup"><span data-stu-id="929db-119">entityType</span></span>|<span data-ttu-id="929db-120">any</span><span class="sxs-lookup"><span data-stu-id="929db-120">any</span></span>||
| <span data-ttu-id="929db-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="929db-121">propertyName</span></span>|<span data-ttu-id="929db-122">string</span><span class="sxs-lookup"><span data-stu-id="929db-122">string</span></span>||
| <span data-ttu-id="929db-123">propertyValue</span><span class="sxs-lookup"><span data-stu-id="929db-123">propertyValue</span></span>|<span data-ttu-id="929db-124">any</span><span class="sxs-lookup"><span data-stu-id="929db-124">any</span></span>||
| <span data-ttu-id="929db-125">includeChanges?</span><span class="sxs-lookup"><span data-stu-id="929db-125">includeChanges?</span></span>|<span data-ttu-id="929db-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="929db-126">boolean</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="929db-127">any を返します</span><span class="sxs-lookup"><span data-stu-id="929db-127">Returns any</span></span>

### <a name="getentitydata"></a><span data-ttu-id="929db-128">getEntityData</span><span class="sxs-lookup"><span data-stu-id="929db-128">getEntityData</span></span>


<span data-ttu-id="929db-129">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="929db-129">getEntityData(entityType: any, entityId: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="929db-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="929db-130">Parameters</span></span>

| <span data-ttu-id="929db-131">氏名</span><span class="sxs-lookup"><span data-stu-id="929db-131">Name</span></span> | <span data-ttu-id="929db-132">種類</span><span class="sxs-lookup"><span data-stu-id="929db-132">Type</span></span> | <span data-ttu-id="929db-133">説明</span><span class="sxs-lookup"><span data-stu-id="929db-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="929db-134">entityType</span><span class="sxs-lookup"><span data-stu-id="929db-134">entityType</span></span>|<span data-ttu-id="929db-135">any</span><span class="sxs-lookup"><span data-stu-id="929db-135">any</span></span>||
| <span data-ttu-id="929db-136">entityId</span><span class="sxs-lookup"><span data-stu-id="929db-136">entityId</span></span>|<span data-ttu-id="929db-137">string</span><span class="sxs-lookup"><span data-stu-id="929db-137">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="929db-138">any を返します</span><span class="sxs-lookup"><span data-stu-id="929db-138">Returns any</span></span>

### <a name="getpagedata"></a><span data-ttu-id="929db-139">getPageData</span><span class="sxs-lookup"><span data-stu-id="929db-139">getPageData</span></span>


<span data-ttu-id="929db-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="929db-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="929db-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="929db-141">Parameters</span></span>

| <span data-ttu-id="929db-142">氏名</span><span class="sxs-lookup"><span data-stu-id="929db-142">Name</span></span> | <span data-ttu-id="929db-143">種類</span><span class="sxs-lookup"><span data-stu-id="929db-143">Type</span></span> | <span data-ttu-id="929db-144">説明</span><span class="sxs-lookup"><span data-stu-id="929db-144">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="929db-145">pageId</span><span class="sxs-lookup"><span data-stu-id="929db-145">pageId</span></span>|<span data-ttu-id="929db-146">string</span><span class="sxs-lookup"><span data-stu-id="929db-146">string</span></span>||
| <span data-ttu-id="929db-147">context</span><span class="sxs-lookup"><span data-stu-id="929db-147">context</span></span>|<span data-ttu-id="929db-148">any</span><span class="sxs-lookup"><span data-stu-id="929db-148">any</span></span>||
| <span data-ttu-id="929db-149">フィルタ</span><span class="sxs-lookup"><span data-stu-id="929db-149">filter</span></span>|<span data-ttu-id="929db-150">any</span><span class="sxs-lookup"><span data-stu-id="929db-150">any</span></span>||
| <span data-ttu-id="929db-151">allowedStaleness</span><span class="sxs-lookup"><span data-stu-id="929db-151">allowedStaleness</span></span>|<span data-ttu-id="929db-152">数値</span><span class="sxs-lookup"><span data-stu-id="929db-152">number</span></span>||

#### <a name="returns-promise-ltpagedataservices-business-logic-services-ipagedatamdgt"></a><span data-ttu-id="929db-153">Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="929db-153">Returns Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>


