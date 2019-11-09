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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183118"
---
# <a name="event-module"></a><span data-ttu-id="5c82f-103">イベント モジュール</span><span class="sxs-lookup"><span data-stu-id="5c82f-103">Event module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="5c82f-104">指数</span><span class="sxs-lookup"><span data-stu-id="5c82f-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="5c82f-105">種類</span><span class="sxs-lookup"><span data-stu-id="5c82f-105">Types</span></span>

* [<span data-ttu-id="5c82f-106">EventHook</span><span class="sxs-lookup"><span data-stu-id="5c82f-106">EventHook</span></span>](../interfaces/event-ievent-ieventhook.md)

### <a name="type-aliases"></a><span data-ttu-id="5c82f-107">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="5c82f-107">Type aliases</span></span>

* [<span data-ttu-id="5c82f-108">IEventListener</span><span class="sxs-lookup"><span data-stu-id="5c82f-108">IEventListener</span></span>](event-ievent.md#ieventlistener)

## <a name="types"></a><span data-ttu-id="5c82f-109">種類</span><span class="sxs-lookup"><span data-stu-id="5c82f-109">Types</span></span>


### <a name="eventhook"></a><span data-ttu-id="5c82f-110">EventHook</span><span class="sxs-lookup"><span data-stu-id="5c82f-110">EventHook</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="5c82f-111">階層</span><span class="sxs-lookup"><span data-stu-id="5c82f-111">Hierarchy</span></span>

<span data-ttu-id="5c82f-112">EventHook</span><span class="sxs-lookup"><span data-stu-id="5c82f-112">EventHook</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="5c82f-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="5c82f-113">Methods</span></span>

| <span data-ttu-id="5c82f-114">氏名</span><span class="sxs-lookup"><span data-stu-id="5c82f-114">Name</span></span> | <span data-ttu-id="5c82f-115">署名</span><span class="sxs-lookup"><span data-stu-id="5c82f-115">Signature</span></span> | <span data-ttu-id="5c82f-116">説明</span><span class="sxs-lookup"><span data-stu-id="5c82f-116">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="5c82f-117">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="5c82f-117">subscribe</span></span>](../interfaces/event-ievent-ieventhook.md#subscribe) |<span data-ttu-id="5c82f-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="5c82f-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="5c82f-119">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="5c82f-119">Subscribe a listener to this event.</span></span><br>  |
| [<span data-ttu-id="5c82f-120">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="5c82f-120">unsubscribe</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribe) |<span data-ttu-id="5c82f-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="5c82f-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="5c82f-122">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="5c82f-122">Unsubscribe a listener from this event.</span></span><br>  |
| [<span data-ttu-id="5c82f-123">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="5c82f-123">unsubscribeAll</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribeall) |<span data-ttu-id="5c82f-124">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="5c82f-124">unsubscribeAll(): void</span></span>|<span data-ttu-id="5c82f-125">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="5c82f-125">Remove all listeners from this event.</span></span><br>  |

## <a name="type-aliases"></a><span data-ttu-id="5c82f-126">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="5c82f-126">Type aliases</span></span>


### <a name="ieventlistener"></a><span data-ttu-id="5c82f-127">IEventListener</span><span class="sxs-lookup"><span data-stu-id="5c82f-127">IEventListener</span></span>
<span data-ttu-id="5c82f-128">IEventListener: 機能</span><span class="sxs-lookup"><span data-stu-id="5c82f-128">IEventListener: function</span></span>



