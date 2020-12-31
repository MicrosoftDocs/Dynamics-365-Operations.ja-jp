---
title: イベント モジュール
description: イベント モジュール
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b622c39b9647a0a534b2a83f059578a4d1b5204
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682565"
---
# <a name="event-module"></a><span data-ttu-id="004f8-103">イベント モジュール</span><span class="sxs-lookup"><span data-stu-id="004f8-103">Event module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="004f8-104">指数</span><span class="sxs-lookup"><span data-stu-id="004f8-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="004f8-105">種類</span><span class="sxs-lookup"><span data-stu-id="004f8-105">Types</span></span>

* [<span data-ttu-id="004f8-106">EventHook</span><span class="sxs-lookup"><span data-stu-id="004f8-106">EventHook</span></span>](../interfaces/event-ievent-ieventhook.md)

### <a name="type-aliases"></a><span data-ttu-id="004f8-107">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="004f8-107">Type aliases</span></span>

* [<span data-ttu-id="004f8-108">IEventListener</span><span class="sxs-lookup"><span data-stu-id="004f8-108">IEventListener</span></span>](event-ievent.md#ieventlistener)

## <a name="types"></a><span data-ttu-id="004f8-109">種類</span><span class="sxs-lookup"><span data-stu-id="004f8-109">Types</span></span>


### <a name="eventhook"></a><span data-ttu-id="004f8-110">EventHook</span><span class="sxs-lookup"><span data-stu-id="004f8-110">EventHook</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="004f8-111">階層</span><span class="sxs-lookup"><span data-stu-id="004f8-111">Hierarchy</span></span>

<span data-ttu-id="004f8-112">EventHook</span><span class="sxs-lookup"><span data-stu-id="004f8-112">EventHook</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="004f8-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="004f8-113">Methods</span></span>

| <span data-ttu-id="004f8-114">氏名</span><span class="sxs-lookup"><span data-stu-id="004f8-114">Name</span></span> | <span data-ttu-id="004f8-115">署名</span><span class="sxs-lookup"><span data-stu-id="004f8-115">Signature</span></span> | <span data-ttu-id="004f8-116">説明</span><span class="sxs-lookup"><span data-stu-id="004f8-116">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="004f8-117">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="004f8-117">subscribe</span></span>](../interfaces/event-ievent-ieventhook.md#subscribe) |<span data-ttu-id="004f8-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="004f8-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="004f8-119">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="004f8-119">Subscribe a listener to this event.</span></span><br>  |
| [<span data-ttu-id="004f8-120">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="004f8-120">unsubscribe</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribe) |<span data-ttu-id="004f8-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="004f8-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="004f8-122">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="004f8-122">Unsubscribe a listener from this event.</span></span><br>  |
| [<span data-ttu-id="004f8-123">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="004f8-123">unsubscribeAll</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribeall) |<span data-ttu-id="004f8-124">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="004f8-124">unsubscribeAll(): void</span></span>|<span data-ttu-id="004f8-125">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="004f8-125">Remove all listeners from this event.</span></span><br>  |

## <a name="type-aliases"></a><span data-ttu-id="004f8-126">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="004f8-126">Type aliases</span></span>


### <a name="ieventlistener"></a><span data-ttu-id="004f8-127">IEventListener</span><span class="sxs-lookup"><span data-stu-id="004f8-127">IEventListener</span></span>
<span data-ttu-id="004f8-128">IEventListener: 機能</span><span class="sxs-lookup"><span data-stu-id="004f8-128">IEventListener: function</span></span>




