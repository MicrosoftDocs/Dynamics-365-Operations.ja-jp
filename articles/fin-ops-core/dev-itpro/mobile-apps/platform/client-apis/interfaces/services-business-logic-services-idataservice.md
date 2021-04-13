---
title: DataService タイプ
description: アプリケーション ワークスペースの下でデータ アクセス機能を提供します。
author: robinarh
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c004f816909d972f9756910fd5a8bee6499f9e90
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744509"
---
# <a name="dataservice-type"></a><span data-ttu-id="92841-103">DataService タイプ</span><span class="sxs-lookup"><span data-stu-id="92841-103">DataService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="92841-104">アプリケーション ワークスペースの下でデータ アクセス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="92841-104">Provides ability access data under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="92841-105">階層</span><span class="sxs-lookup"><span data-stu-id="92841-105">Hierarchy</span></span>

<span data-ttu-id="92841-106">DataService</span><span class="sxs-lookup"><span data-stu-id="92841-106">DataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="92841-107">指数</span><span class="sxs-lookup"><span data-stu-id="92841-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="92841-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="92841-108">Methods</span></span>

* [<span data-ttu-id="92841-109">findEntityData</span><span class="sxs-lookup"><span data-stu-id="92841-109">findEntityData</span></span>](services-business-logic-services-idataservice.md#findentitydata)
* [<span data-ttu-id="92841-110">getEntityData</span><span class="sxs-lookup"><span data-stu-id="92841-110">getEntityData</span></span>](services-business-logic-services-idataservice.md#getentitydata)
* [<span data-ttu-id="92841-111">getPageData</span><span class="sxs-lookup"><span data-stu-id="92841-111">getPageData</span></span>](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a><span data-ttu-id="92841-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="92841-112">Methods</span></span>

### <a name="findentitydata"></a><span data-ttu-id="92841-113">findEntityData</span><span class="sxs-lookup"><span data-stu-id="92841-113">findEntityData</span></span>


<span data-ttu-id="92841-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="92841-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="92841-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92841-115">Parameters</span></span>

| <span data-ttu-id="92841-116">氏名</span><span class="sxs-lookup"><span data-stu-id="92841-116">Name</span></span> | <span data-ttu-id="92841-117">種類</span><span class="sxs-lookup"><span data-stu-id="92841-117">Type</span></span> | <span data-ttu-id="92841-118">説明</span><span class="sxs-lookup"><span data-stu-id="92841-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="92841-119">entityType</span><span class="sxs-lookup"><span data-stu-id="92841-119">entityType</span></span>|<span data-ttu-id="92841-120">any</span><span class="sxs-lookup"><span data-stu-id="92841-120">any</span></span>||
| <span data-ttu-id="92841-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="92841-121">propertyName</span></span>|<span data-ttu-id="92841-122">string</span><span class="sxs-lookup"><span data-stu-id="92841-122">string</span></span>||
| <span data-ttu-id="92841-123">propertyValue</span><span class="sxs-lookup"><span data-stu-id="92841-123">propertyValue</span></span>|<span data-ttu-id="92841-124">any</span><span class="sxs-lookup"><span data-stu-id="92841-124">any</span></span>||
| <span data-ttu-id="92841-125">includeChanges?</span><span class="sxs-lookup"><span data-stu-id="92841-125">includeChanges?</span></span>|<span data-ttu-id="92841-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="92841-126">boolean</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="92841-127">any を返します</span><span class="sxs-lookup"><span data-stu-id="92841-127">Returns any</span></span>

### <a name="getentitydata"></a><span data-ttu-id="92841-128">getEntityData</span><span class="sxs-lookup"><span data-stu-id="92841-128">getEntityData</span></span>


<span data-ttu-id="92841-129">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="92841-129">getEntityData(entityType: any, entityId: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="92841-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92841-130">Parameters</span></span>

| <span data-ttu-id="92841-131">氏名</span><span class="sxs-lookup"><span data-stu-id="92841-131">Name</span></span> | <span data-ttu-id="92841-132">種類</span><span class="sxs-lookup"><span data-stu-id="92841-132">Type</span></span> | <span data-ttu-id="92841-133">説明</span><span class="sxs-lookup"><span data-stu-id="92841-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="92841-134">entityType</span><span class="sxs-lookup"><span data-stu-id="92841-134">entityType</span></span>|<span data-ttu-id="92841-135">any</span><span class="sxs-lookup"><span data-stu-id="92841-135">any</span></span>||
| <span data-ttu-id="92841-136">entityId</span><span class="sxs-lookup"><span data-stu-id="92841-136">entityId</span></span>|<span data-ttu-id="92841-137">string</span><span class="sxs-lookup"><span data-stu-id="92841-137">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="92841-138">any を返します</span><span class="sxs-lookup"><span data-stu-id="92841-138">Returns any</span></span>

### <a name="getpagedata"></a><span data-ttu-id="92841-139">getPageData</span><span class="sxs-lookup"><span data-stu-id="92841-139">getPageData</span></span>


<span data-ttu-id="92841-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="92841-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="92841-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92841-141">Parameters</span></span>

| <span data-ttu-id="92841-142">氏名</span><span class="sxs-lookup"><span data-stu-id="92841-142">Name</span></span> | <span data-ttu-id="92841-143">種類</span><span class="sxs-lookup"><span data-stu-id="92841-143">Type</span></span> | <span data-ttu-id="92841-144">説明</span><span class="sxs-lookup"><span data-stu-id="92841-144">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="92841-145">pageId</span><span class="sxs-lookup"><span data-stu-id="92841-145">pageId</span></span>|<span data-ttu-id="92841-146">string</span><span class="sxs-lookup"><span data-stu-id="92841-146">string</span></span>||
| <span data-ttu-id="92841-147">context</span><span class="sxs-lookup"><span data-stu-id="92841-147">context</span></span>|<span data-ttu-id="92841-148">any</span><span class="sxs-lookup"><span data-stu-id="92841-148">any</span></span>||
| <span data-ttu-id="92841-149">フィルタ</span><span class="sxs-lookup"><span data-stu-id="92841-149">filter</span></span>|<span data-ttu-id="92841-150">any</span><span class="sxs-lookup"><span data-stu-id="92841-150">any</span></span>||
| <span data-ttu-id="92841-151">allowedStaleness</span><span class="sxs-lookup"><span data-stu-id="92841-151">allowedStaleness</span></span>|<span data-ttu-id="92841-152">数値</span><span class="sxs-lookup"><span data-stu-id="92841-152">number</span></span>||

#### <a name="returns-promise-ltpagedatagt"></a><span data-ttu-id="92841-153">Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="92841-153">Returns Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]