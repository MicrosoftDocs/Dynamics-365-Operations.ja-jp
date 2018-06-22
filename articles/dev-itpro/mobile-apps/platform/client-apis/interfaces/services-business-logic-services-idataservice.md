---
title: DataService
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d21e377029e07454e56c1f41be1c78747b85b9fd
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="dataservice-type"></a><span data-ttu-id="f45fe-103">DataService タイプ</span><span class="sxs-lookup"><span data-stu-id="f45fe-103">DataService Type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="f45fe-104">アプリケーション ワークスペースの下でデータ アクセス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="f45fe-104">Provides ability access data under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="f45fe-105">階層</span><span class="sxs-lookup"><span data-stu-id="f45fe-105">Hierarchy</span></span>

<span data-ttu-id="f45fe-106">DataService</span><span class="sxs-lookup"><span data-stu-id="f45fe-106">DataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="f45fe-107">指数</span><span class="sxs-lookup"><span data-stu-id="f45fe-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="f45fe-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f45fe-108">Methods</span></span>

* [<span data-ttu-id="f45fe-109">findEntityData</span><span class="sxs-lookup"><span data-stu-id="f45fe-109">findEntityData</span></span>](services-business-logic-services-idataservice.md#findentitydata)
* [<span data-ttu-id="f45fe-110">getEntityData</span><span class="sxs-lookup"><span data-stu-id="f45fe-110">getEntityData</span></span>](services-business-logic-services-idataservice.md#getentitydata)
* [<span data-ttu-id="f45fe-111">getPageData</span><span class="sxs-lookup"><span data-stu-id="f45fe-111">getPageData</span></span>](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a><span data-ttu-id="f45fe-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="f45fe-112">Methods</span></span>

### <a name="findentitydata"></a><span data-ttu-id="f45fe-113">findEntityData</span><span class="sxs-lookup"><span data-stu-id="f45fe-113">findEntityData</span></span>


<span data-ttu-id="f45fe-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="f45fe-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="f45fe-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f45fe-115">Parameters</span></span>

| <span data-ttu-id="f45fe-116">氏名</span><span class="sxs-lookup"><span data-stu-id="f45fe-116">Name</span></span> | <span data-ttu-id="f45fe-117">種類</span><span class="sxs-lookup"><span data-stu-id="f45fe-117">Type</span></span> | <span data-ttu-id="f45fe-118">説明</span><span class="sxs-lookup"><span data-stu-id="f45fe-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f45fe-119">entityType</span><span class="sxs-lookup"><span data-stu-id="f45fe-119">entityType</span></span>|<span data-ttu-id="f45fe-120">any</span><span class="sxs-lookup"><span data-stu-id="f45fe-120">any</span></span>||
| <span data-ttu-id="f45fe-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="f45fe-121">propertyName</span></span>|<span data-ttu-id="f45fe-122">string</span><span class="sxs-lookup"><span data-stu-id="f45fe-122">string</span></span>||
| <span data-ttu-id="f45fe-123">propertyValue</span><span class="sxs-lookup"><span data-stu-id="f45fe-123">propertyValue</span></span>|<span data-ttu-id="f45fe-124">any</span><span class="sxs-lookup"><span data-stu-id="f45fe-124">any</span></span>||
| <span data-ttu-id="f45fe-125">includeChanges?</span><span class="sxs-lookup"><span data-stu-id="f45fe-125">includeChanges?</span></span>|<span data-ttu-id="f45fe-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="f45fe-126">boolean</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="f45fe-127">any を返します</span><span class="sxs-lookup"><span data-stu-id="f45fe-127">Returns any</span></span>

### <a name="getentitydata"></a><span data-ttu-id="f45fe-128">getEntityData</span><span class="sxs-lookup"><span data-stu-id="f45fe-128">getEntityData</span></span>


<span data-ttu-id="f45fe-129">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="f45fe-129">getEntityData(entityType: any, entityId: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="f45fe-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f45fe-130">Parameters</span></span>

| <span data-ttu-id="f45fe-131">氏名</span><span class="sxs-lookup"><span data-stu-id="f45fe-131">Name</span></span> | <span data-ttu-id="f45fe-132">種類</span><span class="sxs-lookup"><span data-stu-id="f45fe-132">Type</span></span> | <span data-ttu-id="f45fe-133">説明</span><span class="sxs-lookup"><span data-stu-id="f45fe-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f45fe-134">entityType</span><span class="sxs-lookup"><span data-stu-id="f45fe-134">entityType</span></span>|<span data-ttu-id="f45fe-135">any</span><span class="sxs-lookup"><span data-stu-id="f45fe-135">any</span></span>||
| <span data-ttu-id="f45fe-136">entityId</span><span class="sxs-lookup"><span data-stu-id="f45fe-136">entityId</span></span>|<span data-ttu-id="f45fe-137">string</span><span class="sxs-lookup"><span data-stu-id="f45fe-137">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="f45fe-138">any を返します</span><span class="sxs-lookup"><span data-stu-id="f45fe-138">Returns any</span></span>

### <a name="getpagedata"></a><span data-ttu-id="f45fe-139">getPageData</span><span class="sxs-lookup"><span data-stu-id="f45fe-139">getPageData</span></span>


<span data-ttu-id="f45fe-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="f45fe-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="f45fe-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f45fe-141">Parameters</span></span>

| <span data-ttu-id="f45fe-142">氏名</span><span class="sxs-lookup"><span data-stu-id="f45fe-142">Name</span></span> | <span data-ttu-id="f45fe-143">種類</span><span class="sxs-lookup"><span data-stu-id="f45fe-143">Type</span></span> | <span data-ttu-id="f45fe-144">説明</span><span class="sxs-lookup"><span data-stu-id="f45fe-144">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="f45fe-145">pageId</span><span class="sxs-lookup"><span data-stu-id="f45fe-145">pageId</span></span>|<span data-ttu-id="f45fe-146">string</span><span class="sxs-lookup"><span data-stu-id="f45fe-146">string</span></span>||
| <span data-ttu-id="f45fe-147">context</span><span class="sxs-lookup"><span data-stu-id="f45fe-147">context</span></span>|<span data-ttu-id="f45fe-148">any</span><span class="sxs-lookup"><span data-stu-id="f45fe-148">any</span></span>||
| <span data-ttu-id="f45fe-149">フィルタ</span><span class="sxs-lookup"><span data-stu-id="f45fe-149">filter</span></span>|<span data-ttu-id="f45fe-150">any</span><span class="sxs-lookup"><span data-stu-id="f45fe-150">any</span></span>||
| <span data-ttu-id="f45fe-151">allowedStaleness</span><span class="sxs-lookup"><span data-stu-id="f45fe-151">allowedStaleness</span></span>|<span data-ttu-id="f45fe-152">数値</span><span class="sxs-lookup"><span data-stu-id="f45fe-152">number</span></span>||

#### <a name="returns-promise-ltpagedataservices-business-logic-services-ipagedatamdgt"></a><span data-ttu-id="f45fe-153">Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="f45fe-153">Returns Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>


