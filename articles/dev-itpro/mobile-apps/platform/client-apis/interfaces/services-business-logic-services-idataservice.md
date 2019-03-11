---
title: DataService タイプ
description: アプリケーション ワークスペースの下でデータ アクセス機能を提供します。
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
ms.openlocfilehash: 4310a829bbfb1861966b7adebac1c43b6b007653
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369486"
---
# <a name="dataservice-type"></a><span data-ttu-id="2ea72-103">DataService タイプ</span><span class="sxs-lookup"><span data-stu-id="2ea72-103">DataService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="2ea72-104">アプリケーション ワークスペースの下でデータ アクセス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ea72-104">Provides ability access data under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="2ea72-105">階層</span><span class="sxs-lookup"><span data-stu-id="2ea72-105">Hierarchy</span></span>

<span data-ttu-id="2ea72-106">DataService</span><span class="sxs-lookup"><span data-stu-id="2ea72-106">DataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="2ea72-107">指数</span><span class="sxs-lookup"><span data-stu-id="2ea72-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="2ea72-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="2ea72-108">Methods</span></span>

* [<span data-ttu-id="2ea72-109">findEntityData</span><span class="sxs-lookup"><span data-stu-id="2ea72-109">findEntityData</span></span>](services-business-logic-services-idataservice.md#findentitydata)
* [<span data-ttu-id="2ea72-110">getEntityData</span><span class="sxs-lookup"><span data-stu-id="2ea72-110">getEntityData</span></span>](services-business-logic-services-idataservice.md#getentitydata)
* [<span data-ttu-id="2ea72-111">getPageData</span><span class="sxs-lookup"><span data-stu-id="2ea72-111">getPageData</span></span>](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a><span data-ttu-id="2ea72-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="2ea72-112">Methods</span></span>

### <a name="findentitydata"></a><span data-ttu-id="2ea72-113">findEntityData</span><span class="sxs-lookup"><span data-stu-id="2ea72-113">findEntityData</span></span>


<span data-ttu-id="2ea72-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="2ea72-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="2ea72-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ea72-115">Parameters</span></span>

| <span data-ttu-id="2ea72-116">氏名</span><span class="sxs-lookup"><span data-stu-id="2ea72-116">Name</span></span> | <span data-ttu-id="2ea72-117">種類</span><span class="sxs-lookup"><span data-stu-id="2ea72-117">Type</span></span> | <span data-ttu-id="2ea72-118">説明</span><span class="sxs-lookup"><span data-stu-id="2ea72-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="2ea72-119">entityType</span><span class="sxs-lookup"><span data-stu-id="2ea72-119">entityType</span></span>|<span data-ttu-id="2ea72-120">any</span><span class="sxs-lookup"><span data-stu-id="2ea72-120">any</span></span>||
| <span data-ttu-id="2ea72-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="2ea72-121">propertyName</span></span>|<span data-ttu-id="2ea72-122">string</span><span class="sxs-lookup"><span data-stu-id="2ea72-122">string</span></span>||
| <span data-ttu-id="2ea72-123">propertyValue</span><span class="sxs-lookup"><span data-stu-id="2ea72-123">propertyValue</span></span>|<span data-ttu-id="2ea72-124">any</span><span class="sxs-lookup"><span data-stu-id="2ea72-124">any</span></span>||
| <span data-ttu-id="2ea72-125">includeChanges?</span><span class="sxs-lookup"><span data-stu-id="2ea72-125">includeChanges?</span></span>|<span data-ttu-id="2ea72-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="2ea72-126">boolean</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="2ea72-127">any を返します</span><span class="sxs-lookup"><span data-stu-id="2ea72-127">Returns any</span></span>

### <a name="getentitydata"></a><span data-ttu-id="2ea72-128">getEntityData</span><span class="sxs-lookup"><span data-stu-id="2ea72-128">getEntityData</span></span>


<span data-ttu-id="2ea72-129">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="2ea72-129">getEntityData(entityType: any, entityId: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="2ea72-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ea72-130">Parameters</span></span>

| <span data-ttu-id="2ea72-131">氏名</span><span class="sxs-lookup"><span data-stu-id="2ea72-131">Name</span></span> | <span data-ttu-id="2ea72-132">種類</span><span class="sxs-lookup"><span data-stu-id="2ea72-132">Type</span></span> | <span data-ttu-id="2ea72-133">説明</span><span class="sxs-lookup"><span data-stu-id="2ea72-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="2ea72-134">entityType</span><span class="sxs-lookup"><span data-stu-id="2ea72-134">entityType</span></span>|<span data-ttu-id="2ea72-135">any</span><span class="sxs-lookup"><span data-stu-id="2ea72-135">any</span></span>||
| <span data-ttu-id="2ea72-136">entityId</span><span class="sxs-lookup"><span data-stu-id="2ea72-136">entityId</span></span>|<span data-ttu-id="2ea72-137">string</span><span class="sxs-lookup"><span data-stu-id="2ea72-137">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="2ea72-138">any を返します</span><span class="sxs-lookup"><span data-stu-id="2ea72-138">Returns any</span></span>

### <a name="getpagedata"></a><span data-ttu-id="2ea72-139">getPageData</span><span class="sxs-lookup"><span data-stu-id="2ea72-139">getPageData</span></span>


<span data-ttu-id="2ea72-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="2ea72-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="2ea72-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ea72-141">Parameters</span></span>

| <span data-ttu-id="2ea72-142">氏名</span><span class="sxs-lookup"><span data-stu-id="2ea72-142">Name</span></span> | <span data-ttu-id="2ea72-143">種類</span><span class="sxs-lookup"><span data-stu-id="2ea72-143">Type</span></span> | <span data-ttu-id="2ea72-144">説明</span><span class="sxs-lookup"><span data-stu-id="2ea72-144">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="2ea72-145">pageId</span><span class="sxs-lookup"><span data-stu-id="2ea72-145">pageId</span></span>|<span data-ttu-id="2ea72-146">string</span><span class="sxs-lookup"><span data-stu-id="2ea72-146">string</span></span>||
| <span data-ttu-id="2ea72-147">context</span><span class="sxs-lookup"><span data-stu-id="2ea72-147">context</span></span>|<span data-ttu-id="2ea72-148">any</span><span class="sxs-lookup"><span data-stu-id="2ea72-148">any</span></span>||
| <span data-ttu-id="2ea72-149">フィルタ</span><span class="sxs-lookup"><span data-stu-id="2ea72-149">filter</span></span>|<span data-ttu-id="2ea72-150">any</span><span class="sxs-lookup"><span data-stu-id="2ea72-150">any</span></span>||
| <span data-ttu-id="2ea72-151">allowedStaleness</span><span class="sxs-lookup"><span data-stu-id="2ea72-151">allowedStaleness</span></span>|<span data-ttu-id="2ea72-152">数値</span><span class="sxs-lookup"><span data-stu-id="2ea72-152">number</span></span>||

#### <a name="returns-promise-ltpagedataservices-business-logic-services-ipagedatamdgt"></a><span data-ttu-id="2ea72-153">Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="2ea72-153">Returns Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>

