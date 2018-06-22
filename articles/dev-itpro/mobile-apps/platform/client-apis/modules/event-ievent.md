---
title: "イベント"
description: "イベント モジュール"
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
ms.openlocfilehash: 5ede3c2b2996ac5de615fa9f2cb33f4bbeacc1d5
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="event"></a><span data-ttu-id="b939d-103">イベント</span><span class="sxs-lookup"><span data-stu-id="b939d-103">Event</span></span> 

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="b939d-104">指数</span><span class="sxs-lookup"><span data-stu-id="b939d-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="b939d-105">種類</span><span class="sxs-lookup"><span data-stu-id="b939d-105">Types</span></span>

* [<span data-ttu-id="b939d-106">EventHook</span><span class="sxs-lookup"><span data-stu-id="b939d-106">EventHook</span></span>](../interfaces/event-ievent-ieventhook.md)

### <a name="type-aliases"></a><span data-ttu-id="b939d-107">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="b939d-107">Type aliases</span></span>

* [<span data-ttu-id="b939d-108">IEventListener</span><span class="sxs-lookup"><span data-stu-id="b939d-108">IEventListener</span></span>](event-ievent.md#ieventlistener)

## <a name="types"></a><span data-ttu-id="b939d-109">種類</span><span class="sxs-lookup"><span data-stu-id="b939d-109">Types</span></span>


### <a name="eventhook"></a><span data-ttu-id="b939d-110">EventHook</span><span class="sxs-lookup"><span data-stu-id="b939d-110">EventHook</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="b939d-111">階層</span><span class="sxs-lookup"><span data-stu-id="b939d-111">Hierarchy</span></span>

<span data-ttu-id="b939d-112">EventHook</span><span class="sxs-lookup"><span data-stu-id="b939d-112">EventHook</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="b939d-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="b939d-113">Methods</span></span>

| <span data-ttu-id="b939d-114">氏名</span><span class="sxs-lookup"><span data-stu-id="b939d-114">Name</span></span> | <span data-ttu-id="b939d-115">署名</span><span class="sxs-lookup"><span data-stu-id="b939d-115">Signature</span></span> | <span data-ttu-id="b939d-116">説明</span><span class="sxs-lookup"><span data-stu-id="b939d-116">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="b939d-117">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="b939d-117">subscribe</span></span>](../interfaces/event-ievent-ieventhook.md#subscribe) |<span data-ttu-id="b939d-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="b939d-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="b939d-119">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="b939d-119">Subscribe a listener to this event.</span></span><br>  |
| [<span data-ttu-id="b939d-120">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="b939d-120">unsubscribe</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribe) |<span data-ttu-id="b939d-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="b939d-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="b939d-122">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="b939d-122">Unsubscribe a listener from this event.</span></span><br>  |
| [<span data-ttu-id="b939d-123">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="b939d-123">unsubscribeAll</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribeall) |<span data-ttu-id="b939d-124">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="b939d-124">unsubscribeAll(): void</span></span>|<span data-ttu-id="b939d-125">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="b939d-125">Remove all listeners from this event.</span></span><br>  |

## <a name="type-aliases"></a><span data-ttu-id="b939d-126">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="b939d-126">Type aliases</span></span>


### <a name="ieventlistener"></a><span data-ttu-id="b939d-127">IEventListener</span><span class="sxs-lookup"><span data-stu-id="b939d-127">IEventListener</span></span>
<span data-ttu-id="b939d-128">IEventListener: 機能</span><span class="sxs-lookup"><span data-stu-id="b939d-128">IEventListener: function</span></span>





