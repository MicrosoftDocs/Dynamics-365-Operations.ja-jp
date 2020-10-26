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
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e9210c5c35bf3a3d7d99b08af782c47ffa49c632
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980572"
---
# <a name="dataservice-type"></a><span data-ttu-id="53ecd-103">DataService タイプ</span><span class="sxs-lookup"><span data-stu-id="53ecd-103">DataService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="53ecd-104">アプリケーション ワークスペースの下でデータ アクセス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="53ecd-104">Provides ability access data under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="53ecd-105">階層</span><span class="sxs-lookup"><span data-stu-id="53ecd-105">Hierarchy</span></span>

<span data-ttu-id="53ecd-106">DataService</span><span class="sxs-lookup"><span data-stu-id="53ecd-106">DataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="53ecd-107">指数</span><span class="sxs-lookup"><span data-stu-id="53ecd-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="53ecd-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="53ecd-108">Methods</span></span>

* [<span data-ttu-id="53ecd-109">findEntityData</span><span class="sxs-lookup"><span data-stu-id="53ecd-109">findEntityData</span></span>](services-business-logic-services-idataservice.md#findentitydata)
* [<span data-ttu-id="53ecd-110">getEntityData</span><span class="sxs-lookup"><span data-stu-id="53ecd-110">getEntityData</span></span>](services-business-logic-services-idataservice.md#getentitydata)
* [<span data-ttu-id="53ecd-111">getPageData</span><span class="sxs-lookup"><span data-stu-id="53ecd-111">getPageData</span></span>](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a><span data-ttu-id="53ecd-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="53ecd-112">Methods</span></span>

### <a name="findentitydata"></a><span data-ttu-id="53ecd-113">findEntityData</span><span class="sxs-lookup"><span data-stu-id="53ecd-113">findEntityData</span></span>


<span data-ttu-id="53ecd-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="53ecd-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="53ecd-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53ecd-115">Parameters</span></span>

| <span data-ttu-id="53ecd-116">氏名</span><span class="sxs-lookup"><span data-stu-id="53ecd-116">Name</span></span> | <span data-ttu-id="53ecd-117">種類</span><span class="sxs-lookup"><span data-stu-id="53ecd-117">Type</span></span> | <span data-ttu-id="53ecd-118">説明</span><span class="sxs-lookup"><span data-stu-id="53ecd-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="53ecd-119">entityType</span><span class="sxs-lookup"><span data-stu-id="53ecd-119">entityType</span></span>|<span data-ttu-id="53ecd-120">any</span><span class="sxs-lookup"><span data-stu-id="53ecd-120">any</span></span>||
| <span data-ttu-id="53ecd-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="53ecd-121">propertyName</span></span>|<span data-ttu-id="53ecd-122">string</span><span class="sxs-lookup"><span data-stu-id="53ecd-122">string</span></span>||
| <span data-ttu-id="53ecd-123">propertyValue</span><span class="sxs-lookup"><span data-stu-id="53ecd-123">propertyValue</span></span>|<span data-ttu-id="53ecd-124">any</span><span class="sxs-lookup"><span data-stu-id="53ecd-124">any</span></span>||
| <span data-ttu-id="53ecd-125">includeChanges?</span><span class="sxs-lookup"><span data-stu-id="53ecd-125">includeChanges?</span></span>|<span data-ttu-id="53ecd-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="53ecd-126">boolean</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="53ecd-127">any を返します</span><span class="sxs-lookup"><span data-stu-id="53ecd-127">Returns any</span></span>

### <a name="getentitydata"></a><span data-ttu-id="53ecd-128">getEntityData</span><span class="sxs-lookup"><span data-stu-id="53ecd-128">getEntityData</span></span>


<span data-ttu-id="53ecd-129">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="53ecd-129">getEntityData(entityType: any, entityId: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="53ecd-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53ecd-130">Parameters</span></span>

| <span data-ttu-id="53ecd-131">氏名</span><span class="sxs-lookup"><span data-stu-id="53ecd-131">Name</span></span> | <span data-ttu-id="53ecd-132">種類</span><span class="sxs-lookup"><span data-stu-id="53ecd-132">Type</span></span> | <span data-ttu-id="53ecd-133">説明</span><span class="sxs-lookup"><span data-stu-id="53ecd-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="53ecd-134">entityType</span><span class="sxs-lookup"><span data-stu-id="53ecd-134">entityType</span></span>|<span data-ttu-id="53ecd-135">any</span><span class="sxs-lookup"><span data-stu-id="53ecd-135">any</span></span>||
| <span data-ttu-id="53ecd-136">entityId</span><span class="sxs-lookup"><span data-stu-id="53ecd-136">entityId</span></span>|<span data-ttu-id="53ecd-137">string</span><span class="sxs-lookup"><span data-stu-id="53ecd-137">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="53ecd-138">any を返します</span><span class="sxs-lookup"><span data-stu-id="53ecd-138">Returns any</span></span>

### <a name="getpagedata"></a><span data-ttu-id="53ecd-139">getPageData</span><span class="sxs-lookup"><span data-stu-id="53ecd-139">getPageData</span></span>


<span data-ttu-id="53ecd-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="53ecd-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="53ecd-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53ecd-141">Parameters</span></span>

| <span data-ttu-id="53ecd-142">氏名</span><span class="sxs-lookup"><span data-stu-id="53ecd-142">Name</span></span> | <span data-ttu-id="53ecd-143">種類</span><span class="sxs-lookup"><span data-stu-id="53ecd-143">Type</span></span> | <span data-ttu-id="53ecd-144">説明</span><span class="sxs-lookup"><span data-stu-id="53ecd-144">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="53ecd-145">pageId</span><span class="sxs-lookup"><span data-stu-id="53ecd-145">pageId</span></span>|<span data-ttu-id="53ecd-146">string</span><span class="sxs-lookup"><span data-stu-id="53ecd-146">string</span></span>||
| <span data-ttu-id="53ecd-147">context</span><span class="sxs-lookup"><span data-stu-id="53ecd-147">context</span></span>|<span data-ttu-id="53ecd-148">any</span><span class="sxs-lookup"><span data-stu-id="53ecd-148">any</span></span>||
| <span data-ttu-id="53ecd-149">フィルタ</span><span class="sxs-lookup"><span data-stu-id="53ecd-149">filter</span></span>|<span data-ttu-id="53ecd-150">any</span><span class="sxs-lookup"><span data-stu-id="53ecd-150">any</span></span>||
| <span data-ttu-id="53ecd-151">allowedStaleness</span><span class="sxs-lookup"><span data-stu-id="53ecd-151">allowedStaleness</span></span>|<span data-ttu-id="53ecd-152">数値</span><span class="sxs-lookup"><span data-stu-id="53ecd-152">number</span></span>||

#### <a name="returns-promise-ltpagedatagt"></a><span data-ttu-id="53ecd-153">Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="53ecd-153">Returns Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>

