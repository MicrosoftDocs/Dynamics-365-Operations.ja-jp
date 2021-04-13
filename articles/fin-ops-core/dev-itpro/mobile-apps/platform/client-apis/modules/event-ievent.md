---
title: イベント モジュール
description: イベント モジュール
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
ms.openlocfilehash: e750ba8e13ceb01844b6d9fb36bbf0cf2fb14f60
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748081"
---
# <a name="event-module"></a><span data-ttu-id="6e38b-103">イベント モジュール</span><span class="sxs-lookup"><span data-stu-id="6e38b-103">Event module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="6e38b-104">指数</span><span class="sxs-lookup"><span data-stu-id="6e38b-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="6e38b-105">種類</span><span class="sxs-lookup"><span data-stu-id="6e38b-105">Types</span></span>

* [<span data-ttu-id="6e38b-106">EventHook</span><span class="sxs-lookup"><span data-stu-id="6e38b-106">EventHook</span></span>](../interfaces/event-ievent-ieventhook.md)

### <a name="type-aliases"></a><span data-ttu-id="6e38b-107">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="6e38b-107">Type aliases</span></span>

* [<span data-ttu-id="6e38b-108">IEventListener</span><span class="sxs-lookup"><span data-stu-id="6e38b-108">IEventListener</span></span>](event-ievent.md#ieventlistener)

## <a name="types"></a><span data-ttu-id="6e38b-109">種類</span><span class="sxs-lookup"><span data-stu-id="6e38b-109">Types</span></span>


### <a name="eventhook"></a><span data-ttu-id="6e38b-110">EventHook</span><span class="sxs-lookup"><span data-stu-id="6e38b-110">EventHook</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="6e38b-111">階層</span><span class="sxs-lookup"><span data-stu-id="6e38b-111">Hierarchy</span></span>

<span data-ttu-id="6e38b-112">EventHook</span><span class="sxs-lookup"><span data-stu-id="6e38b-112">EventHook</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="6e38b-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="6e38b-113">Methods</span></span>

| <span data-ttu-id="6e38b-114">氏名</span><span class="sxs-lookup"><span data-stu-id="6e38b-114">Name</span></span> | <span data-ttu-id="6e38b-115">署名</span><span class="sxs-lookup"><span data-stu-id="6e38b-115">Signature</span></span> | <span data-ttu-id="6e38b-116">説明</span><span class="sxs-lookup"><span data-stu-id="6e38b-116">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="6e38b-117">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="6e38b-117">subscribe</span></span>](../interfaces/event-ievent-ieventhook.md#subscribe) |<span data-ttu-id="6e38b-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="6e38b-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="6e38b-119">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="6e38b-119">Subscribe a listener to this event.</span></span><br>  |
| [<span data-ttu-id="6e38b-120">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="6e38b-120">unsubscribe</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribe) |<span data-ttu-id="6e38b-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="6e38b-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="6e38b-122">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="6e38b-122">Unsubscribe a listener from this event.</span></span><br>  |
| [<span data-ttu-id="6e38b-123">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="6e38b-123">unsubscribeAll</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribeall) |<span data-ttu-id="6e38b-124">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="6e38b-124">unsubscribeAll(): void</span></span>|<span data-ttu-id="6e38b-125">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="6e38b-125">Remove all listeners from this event.</span></span><br>  |

## <a name="type-aliases"></a><span data-ttu-id="6e38b-126">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="6e38b-126">Type aliases</span></span>


### <a name="ieventlistener"></a><span data-ttu-id="6e38b-127">IEventListener</span><span class="sxs-lookup"><span data-stu-id="6e38b-127">IEventListener</span></span>
<span data-ttu-id="6e38b-128">IEventListener: 機能</span><span class="sxs-lookup"><span data-stu-id="6e38b-128">IEventListener: function</span></span>






[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]