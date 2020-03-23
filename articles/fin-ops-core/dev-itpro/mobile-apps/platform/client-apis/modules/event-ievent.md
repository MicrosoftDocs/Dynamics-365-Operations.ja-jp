---
title: イベント モジュール
description: イベント モジュール
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
ms.openlocfilehash: ac91434fce54c1b8342e1b5154fc81e48baa1910
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124838"
---
# <a name="event-module"></a><span data-ttu-id="c9a0d-103">イベント モジュール</span><span class="sxs-lookup"><span data-stu-id="c9a0d-103">Event module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="c9a0d-104">指数</span><span class="sxs-lookup"><span data-stu-id="c9a0d-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="c9a0d-105">種類</span><span class="sxs-lookup"><span data-stu-id="c9a0d-105">Types</span></span>

* [<span data-ttu-id="c9a0d-106">EventHook</span><span class="sxs-lookup"><span data-stu-id="c9a0d-106">EventHook</span></span>](../interfaces/event-ievent-ieventhook.md)

### <a name="type-aliases"></a><span data-ttu-id="c9a0d-107">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="c9a0d-107">Type aliases</span></span>

* [<span data-ttu-id="c9a0d-108">IEventListener</span><span class="sxs-lookup"><span data-stu-id="c9a0d-108">IEventListener</span></span>](event-ievent.md#ieventlistener)

## <a name="types"></a><span data-ttu-id="c9a0d-109">種類</span><span class="sxs-lookup"><span data-stu-id="c9a0d-109">Types</span></span>


### <a name="eventhook"></a><span data-ttu-id="c9a0d-110">EventHook</span><span class="sxs-lookup"><span data-stu-id="c9a0d-110">EventHook</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="c9a0d-111">階層</span><span class="sxs-lookup"><span data-stu-id="c9a0d-111">Hierarchy</span></span>

<span data-ttu-id="c9a0d-112">EventHook</span><span class="sxs-lookup"><span data-stu-id="c9a0d-112">EventHook</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="c9a0d-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="c9a0d-113">Methods</span></span>

| <span data-ttu-id="c9a0d-114">氏名</span><span class="sxs-lookup"><span data-stu-id="c9a0d-114">Name</span></span> | <span data-ttu-id="c9a0d-115">署名</span><span class="sxs-lookup"><span data-stu-id="c9a0d-115">Signature</span></span> | <span data-ttu-id="c9a0d-116">説明</span><span class="sxs-lookup"><span data-stu-id="c9a0d-116">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="c9a0d-117">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="c9a0d-117">subscribe</span></span>](../interfaces/event-ievent-ieventhook.md#subscribe) |<span data-ttu-id="c9a0d-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="c9a0d-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="c9a0d-119">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="c9a0d-119">Subscribe a listener to this event.</span></span><br>  |
| [<span data-ttu-id="c9a0d-120">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="c9a0d-120">unsubscribe</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribe) |<span data-ttu-id="c9a0d-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="c9a0d-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="c9a0d-122">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="c9a0d-122">Unsubscribe a listener from this event.</span></span><br>  |
| [<span data-ttu-id="c9a0d-123">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="c9a0d-123">unsubscribeAll</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribeall) |<span data-ttu-id="c9a0d-124">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="c9a0d-124">unsubscribeAll(): void</span></span>|<span data-ttu-id="c9a0d-125">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="c9a0d-125">Remove all listeners from this event.</span></span><br>  |

## <a name="type-aliases"></a><span data-ttu-id="c9a0d-126">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="c9a0d-126">Type aliases</span></span>


### <a name="ieventlistener"></a><span data-ttu-id="c9a0d-127">IEventListener</span><span class="sxs-lookup"><span data-stu-id="c9a0d-127">IEventListener</span></span>
<span data-ttu-id="c9a0d-128">IEventListener: 機能</span><span class="sxs-lookup"><span data-stu-id="c9a0d-128">IEventListener: function</span></span>




