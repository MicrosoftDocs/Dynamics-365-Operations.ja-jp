---
title: EventHook
description: "EventHook タイプ"
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
ms.openlocfilehash: 9aff4e6e2c875264d083f56e70774f27de20fcfb
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="eventhook-typelttgt"></a><span data-ttu-id="1bfbd-103">EventHook Type&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="1bfbd-103">EventHook Type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="1bfbd-104">階層</span><span class="sxs-lookup"><span data-stu-id="1bfbd-104">Hierarchy</span></span>

<span data-ttu-id="1bfbd-105">EventHook</span><span class="sxs-lookup"><span data-stu-id="1bfbd-105">EventHook</span></span> <br>

## <a name="index"></a><span data-ttu-id="1bfbd-106">指数</span><span class="sxs-lookup"><span data-stu-id="1bfbd-106">Index</span></span>

### <a name="methods"></a><span data-ttu-id="1bfbd-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="1bfbd-107">Methods</span></span>

* [<span data-ttu-id="1bfbd-108">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="1bfbd-108">subscribe</span></span>](event-ievent-ieventhook.md#subscribe)
* [<span data-ttu-id="1bfbd-109">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1bfbd-109">unsubscribe</span></span>](event-ievent-ieventhook.md#unsubscribe)
* [<span data-ttu-id="1bfbd-110">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="1bfbd-110">unsubscribeAll</span></span>](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a><span data-ttu-id="1bfbd-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="1bfbd-111">Methods</span></span>

### <a name="subscribe"></a><span data-ttu-id="1bfbd-112">subscribe</span><span class="sxs-lookup"><span data-stu-id="1bfbd-112">subscribe</span></span>


<span data-ttu-id="1bfbd-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="1bfbd-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="1bfbd-114">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="1bfbd-114">Subscribe a listener to this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="1bfbd-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1bfbd-115">Parameters</span></span>

| <span data-ttu-id="1bfbd-116">氏名</span><span class="sxs-lookup"><span data-stu-id="1bfbd-116">Name</span></span> | <span data-ttu-id="1bfbd-117">種類</span><span class="sxs-lookup"><span data-stu-id="1bfbd-117">Type</span></span> | <span data-ttu-id="1bfbd-118">説明</span><span class="sxs-lookup"><span data-stu-id="1bfbd-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="1bfbd-119">listener</span><span class="sxs-lookup"><span data-stu-id="1bfbd-119">listener</span></span>|<span data-ttu-id="1bfbd-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="1bfbd-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="1bfbd-121">void を返します</span><span class="sxs-lookup"><span data-stu-id="1bfbd-121">Returns void</span></span>

### <a name="unsubscribe"></a><span data-ttu-id="1bfbd-122">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1bfbd-122">unsubscribe</span></span>


<span data-ttu-id="1bfbd-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="1bfbd-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="1bfbd-124">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="1bfbd-124">Unsubscribe a listener from this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="1bfbd-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1bfbd-125">Parameters</span></span>

| <span data-ttu-id="1bfbd-126">氏名</span><span class="sxs-lookup"><span data-stu-id="1bfbd-126">Name</span></span> | <span data-ttu-id="1bfbd-127">種類</span><span class="sxs-lookup"><span data-stu-id="1bfbd-127">Type</span></span> | <span data-ttu-id="1bfbd-128">説明</span><span class="sxs-lookup"><span data-stu-id="1bfbd-128">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="1bfbd-129">listener</span><span class="sxs-lookup"><span data-stu-id="1bfbd-129">listener</span></span>|<span data-ttu-id="1bfbd-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="1bfbd-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="1bfbd-131">void を返します</span><span class="sxs-lookup"><span data-stu-id="1bfbd-131">Returns void</span></span>

### <a name="unsubscribeall"></a><span data-ttu-id="1bfbd-132">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="1bfbd-132">unsubscribeAll</span></span>


<span data-ttu-id="1bfbd-133">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="1bfbd-133">unsubscribeAll(): void</span></span>

<span data-ttu-id="1bfbd-134">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="1bfbd-134">Remove all listeners from this event.</span></span>

#### <a name="returns-void"></a><span data-ttu-id="1bfbd-135">void を返します</span><span class="sxs-lookup"><span data-stu-id="1bfbd-135">Returns void</span></span>


