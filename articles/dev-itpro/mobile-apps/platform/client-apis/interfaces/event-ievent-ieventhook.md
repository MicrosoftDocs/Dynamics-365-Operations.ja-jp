---
title: EventHook タイプ<T>
description: EventHook タイプ
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
ms.openlocfilehash: a08a44a7c107d4c4207711a28ee855b91c5616df
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369190"
---
# <a name="eventhook-typelttgt"></a><span data-ttu-id="230f3-103">EventHook タイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="230f3-103">EventHook type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="230f3-104">階層</span><span class="sxs-lookup"><span data-stu-id="230f3-104">Hierarchy</span></span>

<span data-ttu-id="230f3-105">EventHook</span><span class="sxs-lookup"><span data-stu-id="230f3-105">EventHook</span></span> <br>

## <a name="index"></a><span data-ttu-id="230f3-106">指数</span><span class="sxs-lookup"><span data-stu-id="230f3-106">Index</span></span>

### <a name="methods"></a><span data-ttu-id="230f3-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="230f3-107">Methods</span></span>

* [<span data-ttu-id="230f3-108">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="230f3-108">subscribe</span></span>](event-ievent-ieventhook.md#subscribe)
* [<span data-ttu-id="230f3-109">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="230f3-109">unsubscribe</span></span>](event-ievent-ieventhook.md#unsubscribe)
* [<span data-ttu-id="230f3-110">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="230f3-110">unsubscribeAll</span></span>](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a><span data-ttu-id="230f3-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="230f3-111">Methods</span></span>

### <a name="subscribe"></a><span data-ttu-id="230f3-112">subscribe</span><span class="sxs-lookup"><span data-stu-id="230f3-112">subscribe</span></span>


<span data-ttu-id="230f3-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="230f3-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="230f3-114">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="230f3-114">Subscribe a listener to this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="230f3-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="230f3-115">Parameters</span></span>

| <span data-ttu-id="230f3-116">氏名</span><span class="sxs-lookup"><span data-stu-id="230f3-116">Name</span></span> | <span data-ttu-id="230f3-117">種類</span><span class="sxs-lookup"><span data-stu-id="230f3-117">Type</span></span> | <span data-ttu-id="230f3-118">説明</span><span class="sxs-lookup"><span data-stu-id="230f3-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="230f3-119">listener</span><span class="sxs-lookup"><span data-stu-id="230f3-119">listener</span></span>|<span data-ttu-id="230f3-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="230f3-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="230f3-121">void を返します</span><span class="sxs-lookup"><span data-stu-id="230f3-121">Returns void</span></span>

### <a name="unsubscribe"></a><span data-ttu-id="230f3-122">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="230f3-122">unsubscribe</span></span>


<span data-ttu-id="230f3-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="230f3-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="230f3-124">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="230f3-124">Unsubscribe a listener from this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="230f3-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="230f3-125">Parameters</span></span>

| <span data-ttu-id="230f3-126">氏名</span><span class="sxs-lookup"><span data-stu-id="230f3-126">Name</span></span> | <span data-ttu-id="230f3-127">種類</span><span class="sxs-lookup"><span data-stu-id="230f3-127">Type</span></span> | <span data-ttu-id="230f3-128">説明</span><span class="sxs-lookup"><span data-stu-id="230f3-128">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="230f3-129">listener</span><span class="sxs-lookup"><span data-stu-id="230f3-129">listener</span></span>|<span data-ttu-id="230f3-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="230f3-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="230f3-131">void を返します</span><span class="sxs-lookup"><span data-stu-id="230f3-131">Returns void</span></span>

### <a name="unsubscribeall"></a><span data-ttu-id="230f3-132">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="230f3-132">unsubscribeAll</span></span>


<span data-ttu-id="230f3-133">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="230f3-133">unsubscribeAll(): void</span></span>

<span data-ttu-id="230f3-134">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="230f3-134">Remove all listeners from this event.</span></span>

#### <a name="returns-void"></a><span data-ttu-id="230f3-135">void を返します</span><span class="sxs-lookup"><span data-stu-id="230f3-135">Returns void</span></span>

