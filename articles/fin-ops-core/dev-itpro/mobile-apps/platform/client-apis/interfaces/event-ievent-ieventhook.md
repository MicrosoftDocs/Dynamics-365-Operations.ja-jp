---
title: EventHook タイプ<T>
description: EventHook タイプ
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
ms.openlocfilehash: a09dd098169faa845ae34d3d534bef493d526427
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745219"
---
# <a name="eventhook-typelttgt"></a><span data-ttu-id="4c200-103">EventHook タイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="4c200-103">EventHook type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="4c200-104">階層</span><span class="sxs-lookup"><span data-stu-id="4c200-104">Hierarchy</span></span>

<span data-ttu-id="4c200-105">EventHook</span><span class="sxs-lookup"><span data-stu-id="4c200-105">EventHook</span></span> <br>

## <a name="index"></a><span data-ttu-id="4c200-106">指数</span><span class="sxs-lookup"><span data-stu-id="4c200-106">Index</span></span>

### <a name="methods"></a><span data-ttu-id="4c200-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="4c200-107">Methods</span></span>

* [<span data-ttu-id="4c200-108">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="4c200-108">subscribe</span></span>](event-ievent-ieventhook.md#subscribe)
* [<span data-ttu-id="4c200-109">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="4c200-109">unsubscribe</span></span>](event-ievent-ieventhook.md#unsubscribe)
* [<span data-ttu-id="4c200-110">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="4c200-110">unsubscribeAll</span></span>](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a><span data-ttu-id="4c200-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="4c200-111">Methods</span></span>

### <a name="subscribe"></a><span data-ttu-id="4c200-112">subscribe</span><span class="sxs-lookup"><span data-stu-id="4c200-112">subscribe</span></span>


<span data-ttu-id="4c200-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="4c200-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="4c200-114">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="4c200-114">Subscribe a listener to this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="4c200-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c200-115">Parameters</span></span>

| <span data-ttu-id="4c200-116">氏名</span><span class="sxs-lookup"><span data-stu-id="4c200-116">Name</span></span> | <span data-ttu-id="4c200-117">種類</span><span class="sxs-lookup"><span data-stu-id="4c200-117">Type</span></span> | <span data-ttu-id="4c200-118">説明</span><span class="sxs-lookup"><span data-stu-id="4c200-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="4c200-119">listener</span><span class="sxs-lookup"><span data-stu-id="4c200-119">listener</span></span>|<span data-ttu-id="4c200-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="4c200-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="4c200-121">void を返します</span><span class="sxs-lookup"><span data-stu-id="4c200-121">Returns void</span></span>

### <a name="unsubscribe"></a><span data-ttu-id="4c200-122">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="4c200-122">unsubscribe</span></span>


<span data-ttu-id="4c200-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="4c200-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="4c200-124">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="4c200-124">Unsubscribe a listener from this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="4c200-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c200-125">Parameters</span></span>

| <span data-ttu-id="4c200-126">氏名</span><span class="sxs-lookup"><span data-stu-id="4c200-126">Name</span></span> | <span data-ttu-id="4c200-127">種類</span><span class="sxs-lookup"><span data-stu-id="4c200-127">Type</span></span> | <span data-ttu-id="4c200-128">説明</span><span class="sxs-lookup"><span data-stu-id="4c200-128">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="4c200-129">listener</span><span class="sxs-lookup"><span data-stu-id="4c200-129">listener</span></span>|<span data-ttu-id="4c200-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="4c200-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="4c200-131">void を返します</span><span class="sxs-lookup"><span data-stu-id="4c200-131">Returns void</span></span>

### <a name="unsubscribeall"></a><span data-ttu-id="4c200-132">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="4c200-132">unsubscribeAll</span></span>


<span data-ttu-id="4c200-133">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="4c200-133">unsubscribeAll(): void</span></span>

<span data-ttu-id="4c200-134">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="4c200-134">Remove all listeners from this event.</span></span>

#### <a name="returns-void"></a><span data-ttu-id="4c200-135">void を返します</span><span class="sxs-lookup"><span data-stu-id="4c200-135">Returns void</span></span>



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]