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
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6cc7cffdad7f10d1be49ae408490b0189bbcf799
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191866"
---
# <a name="dataservice-type"></a><span data-ttu-id="7b363-103">DataService タイプ</span><span class="sxs-lookup"><span data-stu-id="7b363-103">DataService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="7b363-104">アプリケーション ワークスペースの下でデータ アクセス機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="7b363-104">Provides ability access data under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="7b363-105">階層</span><span class="sxs-lookup"><span data-stu-id="7b363-105">Hierarchy</span></span>

<span data-ttu-id="7b363-106">DataService</span><span class="sxs-lookup"><span data-stu-id="7b363-106">DataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="7b363-107">指数</span><span class="sxs-lookup"><span data-stu-id="7b363-107">Index</span></span>

### <a name="methods"></a><span data-ttu-id="7b363-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b363-108">Methods</span></span>

* [<span data-ttu-id="7b363-109">findEntityData</span><span class="sxs-lookup"><span data-stu-id="7b363-109">findEntityData</span></span>](services-business-logic-services-idataservice.md#findentitydata)
* [<span data-ttu-id="7b363-110">getEntityData</span><span class="sxs-lookup"><span data-stu-id="7b363-110">getEntityData</span></span>](services-business-logic-services-idataservice.md#getentitydata)
* [<span data-ttu-id="7b363-111">getPageData</span><span class="sxs-lookup"><span data-stu-id="7b363-111">getPageData</span></span>](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a><span data-ttu-id="7b363-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b363-112">Methods</span></span>

### <a name="findentitydata"></a><span data-ttu-id="7b363-113">findEntityData</span><span class="sxs-lookup"><span data-stu-id="7b363-113">findEntityData</span></span>


<span data-ttu-id="7b363-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="7b363-114">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="7b363-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b363-115">Parameters</span></span>

| <span data-ttu-id="7b363-116">氏名</span><span class="sxs-lookup"><span data-stu-id="7b363-116">Name</span></span> | <span data-ttu-id="7b363-117">種類</span><span class="sxs-lookup"><span data-stu-id="7b363-117">Type</span></span> | <span data-ttu-id="7b363-118">説明</span><span class="sxs-lookup"><span data-stu-id="7b363-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="7b363-119">entityType</span><span class="sxs-lookup"><span data-stu-id="7b363-119">entityType</span></span>|<span data-ttu-id="7b363-120">any</span><span class="sxs-lookup"><span data-stu-id="7b363-120">any</span></span>||
| <span data-ttu-id="7b363-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="7b363-121">propertyName</span></span>|<span data-ttu-id="7b363-122">string</span><span class="sxs-lookup"><span data-stu-id="7b363-122">string</span></span>||
| <span data-ttu-id="7b363-123">propertyValue</span><span class="sxs-lookup"><span data-stu-id="7b363-123">propertyValue</span></span>|<span data-ttu-id="7b363-124">any</span><span class="sxs-lookup"><span data-stu-id="7b363-124">any</span></span>||
| <span data-ttu-id="7b363-125">includeChanges?</span><span class="sxs-lookup"><span data-stu-id="7b363-125">includeChanges?</span></span>|<span data-ttu-id="7b363-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="7b363-126">boolean</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="7b363-127">any を返します</span><span class="sxs-lookup"><span data-stu-id="7b363-127">Returns any</span></span>

### <a name="getentitydata"></a><span data-ttu-id="7b363-128">getEntityData</span><span class="sxs-lookup"><span data-stu-id="7b363-128">getEntityData</span></span>


<span data-ttu-id="7b363-129">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="7b363-129">getEntityData(entityType: any, entityId: string): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="7b363-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b363-130">Parameters</span></span>

| <span data-ttu-id="7b363-131">氏名</span><span class="sxs-lookup"><span data-stu-id="7b363-131">Name</span></span> | <span data-ttu-id="7b363-132">種類</span><span class="sxs-lookup"><span data-stu-id="7b363-132">Type</span></span> | <span data-ttu-id="7b363-133">説明</span><span class="sxs-lookup"><span data-stu-id="7b363-133">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="7b363-134">entityType</span><span class="sxs-lookup"><span data-stu-id="7b363-134">entityType</span></span>|<span data-ttu-id="7b363-135">any</span><span class="sxs-lookup"><span data-stu-id="7b363-135">any</span></span>||
| <span data-ttu-id="7b363-136">entityId</span><span class="sxs-lookup"><span data-stu-id="7b363-136">entityId</span></span>|<span data-ttu-id="7b363-137">string</span><span class="sxs-lookup"><span data-stu-id="7b363-137">string</span></span>||

#### <a name="returns-any"></a><span data-ttu-id="7b363-138">any を返します</span><span class="sxs-lookup"><span data-stu-id="7b363-138">Returns any</span></span>

### <a name="getpagedata"></a><span data-ttu-id="7b363-139">getPageData</span><span class="sxs-lookup"><span data-stu-id="7b363-139">getPageData</span></span>


<span data-ttu-id="7b363-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="7b363-140">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>




#### <a name="parameters"></a><span data-ttu-id="7b363-141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b363-141">Parameters</span></span>

| <span data-ttu-id="7b363-142">氏名</span><span class="sxs-lookup"><span data-stu-id="7b363-142">Name</span></span> | <span data-ttu-id="7b363-143">種類</span><span class="sxs-lookup"><span data-stu-id="7b363-143">Type</span></span> | <span data-ttu-id="7b363-144">説明</span><span class="sxs-lookup"><span data-stu-id="7b363-144">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="7b363-145">pageId</span><span class="sxs-lookup"><span data-stu-id="7b363-145">pageId</span></span>|<span data-ttu-id="7b363-146">string</span><span class="sxs-lookup"><span data-stu-id="7b363-146">string</span></span>||
| <span data-ttu-id="7b363-147">context</span><span class="sxs-lookup"><span data-stu-id="7b363-147">context</span></span>|<span data-ttu-id="7b363-148">any</span><span class="sxs-lookup"><span data-stu-id="7b363-148">any</span></span>||
| <span data-ttu-id="7b363-149">フィルタ</span><span class="sxs-lookup"><span data-stu-id="7b363-149">filter</span></span>|<span data-ttu-id="7b363-150">any</span><span class="sxs-lookup"><span data-stu-id="7b363-150">any</span></span>||
| <span data-ttu-id="7b363-151">allowedStaleness</span><span class="sxs-lookup"><span data-stu-id="7b363-151">allowedStaleness</span></span>|<span data-ttu-id="7b363-152">数値</span><span class="sxs-lookup"><span data-stu-id="7b363-152">number</span></span>||

#### <a name="returns-promise-ltpagedataservices-business-logic-services-ipagedatamdgt"></a><span data-ttu-id="7b363-153">Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します</span><span class="sxs-lookup"><span data-stu-id="7b363-153">Returns Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;</span></span>

