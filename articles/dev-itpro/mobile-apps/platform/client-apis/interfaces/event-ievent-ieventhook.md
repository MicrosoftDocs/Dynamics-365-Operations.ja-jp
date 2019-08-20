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
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1761172fac9f51e9039d4eac58c02ca856051324
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851635"
---
# <a name="eventhook-typelttgt"></a><span data-ttu-id="4c23e-103">EventHook タイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="4c23e-103">EventHook type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="4c23e-104">階層</span><span class="sxs-lookup"><span data-stu-id="4c23e-104">Hierarchy</span></span>

<span data-ttu-id="4c23e-105">EventHook</span><span class="sxs-lookup"><span data-stu-id="4c23e-105">EventHook</span></span> <br>

## <a name="index"></a><span data-ttu-id="4c23e-106">指数</span><span class="sxs-lookup"><span data-stu-id="4c23e-106">Index</span></span>

### <a name="methods"></a><span data-ttu-id="4c23e-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="4c23e-107">Methods</span></span>

* [<span data-ttu-id="4c23e-108">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="4c23e-108">subscribe</span></span>](event-ievent-ieventhook.md#subscribe)
* [<span data-ttu-id="4c23e-109">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="4c23e-109">unsubscribe</span></span>](event-ievent-ieventhook.md#unsubscribe)
* [<span data-ttu-id="4c23e-110">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="4c23e-110">unsubscribeAll</span></span>](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a><span data-ttu-id="4c23e-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="4c23e-111">Methods</span></span>

### <a name="subscribe"></a><span data-ttu-id="4c23e-112">subscribe</span><span class="sxs-lookup"><span data-stu-id="4c23e-112">subscribe</span></span>


<span data-ttu-id="4c23e-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="4c23e-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="4c23e-114">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="4c23e-114">Subscribe a listener to this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="4c23e-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c23e-115">Parameters</span></span>

| <span data-ttu-id="4c23e-116">氏名</span><span class="sxs-lookup"><span data-stu-id="4c23e-116">Name</span></span> | <span data-ttu-id="4c23e-117">種類</span><span class="sxs-lookup"><span data-stu-id="4c23e-117">Type</span></span> | <span data-ttu-id="4c23e-118">説明</span><span class="sxs-lookup"><span data-stu-id="4c23e-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="4c23e-119">listener</span><span class="sxs-lookup"><span data-stu-id="4c23e-119">listener</span></span>|<span data-ttu-id="4c23e-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="4c23e-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="4c23e-121">void を返します</span><span class="sxs-lookup"><span data-stu-id="4c23e-121">Returns void</span></span>

### <a name="unsubscribe"></a><span data-ttu-id="4c23e-122">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="4c23e-122">unsubscribe</span></span>


<span data-ttu-id="4c23e-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="4c23e-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="4c23e-124">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="4c23e-124">Unsubscribe a listener from this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="4c23e-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c23e-125">Parameters</span></span>

| <span data-ttu-id="4c23e-126">氏名</span><span class="sxs-lookup"><span data-stu-id="4c23e-126">Name</span></span> | <span data-ttu-id="4c23e-127">種類</span><span class="sxs-lookup"><span data-stu-id="4c23e-127">Type</span></span> | <span data-ttu-id="4c23e-128">説明</span><span class="sxs-lookup"><span data-stu-id="4c23e-128">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="4c23e-129">listener</span><span class="sxs-lookup"><span data-stu-id="4c23e-129">listener</span></span>|<span data-ttu-id="4c23e-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="4c23e-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="4c23e-131">void を返します</span><span class="sxs-lookup"><span data-stu-id="4c23e-131">Returns void</span></span>

### <a name="unsubscribeall"></a><span data-ttu-id="4c23e-132">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="4c23e-132">unsubscribeAll</span></span>


<span data-ttu-id="4c23e-133">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="4c23e-133">unsubscribeAll(): void</span></span>

<span data-ttu-id="4c23e-134">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="4c23e-134">Remove all listeners from this event.</span></span>

#### <a name="returns-void"></a><span data-ttu-id="4c23e-135">void を返します</span><span class="sxs-lookup"><span data-stu-id="4c23e-135">Returns void</span></span>

