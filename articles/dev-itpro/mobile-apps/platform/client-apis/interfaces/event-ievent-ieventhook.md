---
title: "EventHook タイプ<T>"
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
ms.sourcegitcommit: ed6cabcc8c76fba3d4414cd4b564b720c54169e0
ms.openlocfilehash: a08a44a7c107d4c4207711a28ee855b91c5616df
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="eventhook-typelttgt"></a><span data-ttu-id="1fad8-103">EventHook タイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="1fad8-103">EventHook type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="1fad8-104">階層</span><span class="sxs-lookup"><span data-stu-id="1fad8-104">Hierarchy</span></span>

<span data-ttu-id="1fad8-105">EventHook</span><span class="sxs-lookup"><span data-stu-id="1fad8-105">EventHook</span></span> <br>

## <a name="index"></a><span data-ttu-id="1fad8-106">指数</span><span class="sxs-lookup"><span data-stu-id="1fad8-106">Index</span></span>

### <a name="methods"></a><span data-ttu-id="1fad8-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="1fad8-107">Methods</span></span>

* [<span data-ttu-id="1fad8-108">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="1fad8-108">subscribe</span></span>](event-ievent-ieventhook.md#subscribe)
* [<span data-ttu-id="1fad8-109">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1fad8-109">unsubscribe</span></span>](event-ievent-ieventhook.md#unsubscribe)
* [<span data-ttu-id="1fad8-110">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="1fad8-110">unsubscribeAll</span></span>](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a><span data-ttu-id="1fad8-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="1fad8-111">Methods</span></span>

### <a name="subscribe"></a><span data-ttu-id="1fad8-112">subscribe</span><span class="sxs-lookup"><span data-stu-id="1fad8-112">subscribe</span></span>


<span data-ttu-id="1fad8-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="1fad8-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="1fad8-114">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="1fad8-114">Subscribe a listener to this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="1fad8-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fad8-115">Parameters</span></span>

| <span data-ttu-id="1fad8-116">氏名</span><span class="sxs-lookup"><span data-stu-id="1fad8-116">Name</span></span> | <span data-ttu-id="1fad8-117">種類</span><span class="sxs-lookup"><span data-stu-id="1fad8-117">Type</span></span> | <span data-ttu-id="1fad8-118">説明</span><span class="sxs-lookup"><span data-stu-id="1fad8-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="1fad8-119">listener</span><span class="sxs-lookup"><span data-stu-id="1fad8-119">listener</span></span>|<span data-ttu-id="1fad8-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="1fad8-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="1fad8-121">void を返します</span><span class="sxs-lookup"><span data-stu-id="1fad8-121">Returns void</span></span>

### <a name="unsubscribe"></a><span data-ttu-id="1fad8-122">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1fad8-122">unsubscribe</span></span>


<span data-ttu-id="1fad8-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="1fad8-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="1fad8-124">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="1fad8-124">Unsubscribe a listener from this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="1fad8-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fad8-125">Parameters</span></span>

| <span data-ttu-id="1fad8-126">氏名</span><span class="sxs-lookup"><span data-stu-id="1fad8-126">Name</span></span> | <span data-ttu-id="1fad8-127">種類</span><span class="sxs-lookup"><span data-stu-id="1fad8-127">Type</span></span> | <span data-ttu-id="1fad8-128">説明</span><span class="sxs-lookup"><span data-stu-id="1fad8-128">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="1fad8-129">listener</span><span class="sxs-lookup"><span data-stu-id="1fad8-129">listener</span></span>|<span data-ttu-id="1fad8-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="1fad8-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="1fad8-131">void を返します</span><span class="sxs-lookup"><span data-stu-id="1fad8-131">Returns void</span></span>

### <a name="unsubscribeall"></a><span data-ttu-id="1fad8-132">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="1fad8-132">unsubscribeAll</span></span>


<span data-ttu-id="1fad8-133">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="1fad8-133">unsubscribeAll(): void</span></span>

<span data-ttu-id="1fad8-134">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="1fad8-134">Remove all listeners from this event.</span></span>

#### <a name="returns-void"></a><span data-ttu-id="1fad8-135">void を返します</span><span class="sxs-lookup"><span data-stu-id="1fad8-135">Returns void</span></span>


