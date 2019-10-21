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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183147"
---
# <a name="eventhook-typelttgt"></a><span data-ttu-id="e66e8-103">EventHook タイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="e66e8-103">EventHook type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="e66e8-104">階層</span><span class="sxs-lookup"><span data-stu-id="e66e8-104">Hierarchy</span></span>

<span data-ttu-id="e66e8-105">EventHook</span><span class="sxs-lookup"><span data-stu-id="e66e8-105">EventHook</span></span> <br>

## <a name="index"></a><span data-ttu-id="e66e8-106">指数</span><span class="sxs-lookup"><span data-stu-id="e66e8-106">Index</span></span>

### <a name="methods"></a><span data-ttu-id="e66e8-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="e66e8-107">Methods</span></span>

* [<span data-ttu-id="e66e8-108">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="e66e8-108">subscribe</span></span>](event-ievent-ieventhook.md#subscribe)
* [<span data-ttu-id="e66e8-109">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="e66e8-109">unsubscribe</span></span>](event-ievent-ieventhook.md#unsubscribe)
* [<span data-ttu-id="e66e8-110">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="e66e8-110">unsubscribeAll</span></span>](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a><span data-ttu-id="e66e8-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="e66e8-111">Methods</span></span>

### <a name="subscribe"></a><span data-ttu-id="e66e8-112">subscribe</span><span class="sxs-lookup"><span data-stu-id="e66e8-112">subscribe</span></span>


<span data-ttu-id="e66e8-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="e66e8-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="e66e8-114">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="e66e8-114">Subscribe a listener to this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="e66e8-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e66e8-115">Parameters</span></span>

| <span data-ttu-id="e66e8-116">氏名</span><span class="sxs-lookup"><span data-stu-id="e66e8-116">Name</span></span> | <span data-ttu-id="e66e8-117">種類</span><span class="sxs-lookup"><span data-stu-id="e66e8-117">Type</span></span> | <span data-ttu-id="e66e8-118">説明</span><span class="sxs-lookup"><span data-stu-id="e66e8-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="e66e8-119">listener</span><span class="sxs-lookup"><span data-stu-id="e66e8-119">listener</span></span>|<span data-ttu-id="e66e8-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="e66e8-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="e66e8-121">void を返します</span><span class="sxs-lookup"><span data-stu-id="e66e8-121">Returns void</span></span>

### <a name="unsubscribe"></a><span data-ttu-id="e66e8-122">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="e66e8-122">unsubscribe</span></span>


<span data-ttu-id="e66e8-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="e66e8-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="e66e8-124">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="e66e8-124">Unsubscribe a listener from this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="e66e8-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e66e8-125">Parameters</span></span>

| <span data-ttu-id="e66e8-126">氏名</span><span class="sxs-lookup"><span data-stu-id="e66e8-126">Name</span></span> | <span data-ttu-id="e66e8-127">種類</span><span class="sxs-lookup"><span data-stu-id="e66e8-127">Type</span></span> | <span data-ttu-id="e66e8-128">説明</span><span class="sxs-lookup"><span data-stu-id="e66e8-128">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="e66e8-129">listener</span><span class="sxs-lookup"><span data-stu-id="e66e8-129">listener</span></span>|<span data-ttu-id="e66e8-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="e66e8-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="e66e8-131">void を返します</span><span class="sxs-lookup"><span data-stu-id="e66e8-131">Returns void</span></span>

### <a name="unsubscribeall"></a><span data-ttu-id="e66e8-132">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="e66e8-132">unsubscribeAll</span></span>


<span data-ttu-id="e66e8-133">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="e66e8-133">unsubscribeAll(): void</span></span>

<span data-ttu-id="e66e8-134">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="e66e8-134">Remove all listeners from this event.</span></span>

#### <a name="returns-void"></a><span data-ttu-id="e66e8-135">void を返します</span><span class="sxs-lookup"><span data-stu-id="e66e8-135">Returns void</span></span>

