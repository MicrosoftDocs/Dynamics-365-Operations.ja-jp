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
ms.openlocfilehash: aad614dc41cc682e21768fe6324ea849a2680fcc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506217"
---
# <a name="eventhook-typelttgt"></a><span data-ttu-id="39c84-103">EventHook タイプ&lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="39c84-103">EventHook type&lt;T&gt;</span></span>

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a><span data-ttu-id="39c84-104">階層</span><span class="sxs-lookup"><span data-stu-id="39c84-104">Hierarchy</span></span>

<span data-ttu-id="39c84-105">EventHook</span><span class="sxs-lookup"><span data-stu-id="39c84-105">EventHook</span></span> <br>

## <a name="index"></a><span data-ttu-id="39c84-106">指数</span><span class="sxs-lookup"><span data-stu-id="39c84-106">Index</span></span>

### <a name="methods"></a><span data-ttu-id="39c84-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="39c84-107">Methods</span></span>

* [<span data-ttu-id="39c84-108">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="39c84-108">subscribe</span></span>](event-ievent-ieventhook.md#subscribe)
* [<span data-ttu-id="39c84-109">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="39c84-109">unsubscribe</span></span>](event-ievent-ieventhook.md#unsubscribe)
* [<span data-ttu-id="39c84-110">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="39c84-110">unsubscribeAll</span></span>](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a><span data-ttu-id="39c84-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="39c84-111">Methods</span></span>

### <a name="subscribe"></a><span data-ttu-id="39c84-112">subscribe</span><span class="sxs-lookup"><span data-stu-id="39c84-112">subscribe</span></span>


<span data-ttu-id="39c84-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="39c84-113">subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="39c84-114">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="39c84-114">Subscribe a listener to this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="39c84-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="39c84-115">Parameters</span></span>

| <span data-ttu-id="39c84-116">氏名</span><span class="sxs-lookup"><span data-stu-id="39c84-116">Name</span></span> | <span data-ttu-id="39c84-117">種類</span><span class="sxs-lookup"><span data-stu-id="39c84-117">Type</span></span> | <span data-ttu-id="39c84-118">説明</span><span class="sxs-lookup"><span data-stu-id="39c84-118">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="39c84-119">listener</span><span class="sxs-lookup"><span data-stu-id="39c84-119">listener</span></span>|<span data-ttu-id="39c84-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="39c84-120">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="39c84-121">void を返します</span><span class="sxs-lookup"><span data-stu-id="39c84-121">Returns void</span></span>

### <a name="unsubscribe"></a><span data-ttu-id="39c84-122">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="39c84-122">unsubscribe</span></span>


<span data-ttu-id="39c84-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="39c84-123">unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>

<span data-ttu-id="39c84-124">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="39c84-124">Unsubscribe a listener from this event.</span></span>


#### <a name="parameters"></a><span data-ttu-id="39c84-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="39c84-125">Parameters</span></span>

| <span data-ttu-id="39c84-126">氏名</span><span class="sxs-lookup"><span data-stu-id="39c84-126">Name</span></span> | <span data-ttu-id="39c84-127">種類</span><span class="sxs-lookup"><span data-stu-id="39c84-127">Type</span></span> | <span data-ttu-id="39c84-128">説明</span><span class="sxs-lookup"><span data-stu-id="39c84-128">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="39c84-129">listener</span><span class="sxs-lookup"><span data-stu-id="39c84-129">listener</span></span>|<span data-ttu-id="39c84-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="39c84-130">[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="39c84-131">void を返します</span><span class="sxs-lookup"><span data-stu-id="39c84-131">Returns void</span></span>

### <a name="unsubscribeall"></a><span data-ttu-id="39c84-132">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="39c84-132">unsubscribeAll</span></span>


<span data-ttu-id="39c84-133">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="39c84-133">unsubscribeAll(): void</span></span>

<span data-ttu-id="39c84-134">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="39c84-134">Remove all listeners from this event.</span></span>

#### <a name="returns-void"></a><span data-ttu-id="39c84-135">void を返します</span><span class="sxs-lookup"><span data-stu-id="39c84-135">Returns void</span></span>

