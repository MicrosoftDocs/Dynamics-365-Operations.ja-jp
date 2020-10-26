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
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5f00ec58f360e650730cf21e1956051c9cee9dbe
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978194"
---
# <a name="event-module"></a><span data-ttu-id="26a7c-103">イベント モジュール</span><span class="sxs-lookup"><span data-stu-id="26a7c-103">Event module</span></span>

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a><span data-ttu-id="26a7c-104">指数</span><span class="sxs-lookup"><span data-stu-id="26a7c-104">Index</span></span>

### <a name="types"></a><span data-ttu-id="26a7c-105">種類</span><span class="sxs-lookup"><span data-stu-id="26a7c-105">Types</span></span>

* [<span data-ttu-id="26a7c-106">EventHook</span><span class="sxs-lookup"><span data-stu-id="26a7c-106">EventHook</span></span>](../interfaces/event-ievent-ieventhook.md)

### <a name="type-aliases"></a><span data-ttu-id="26a7c-107">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="26a7c-107">Type aliases</span></span>

* [<span data-ttu-id="26a7c-108">IEventListener</span><span class="sxs-lookup"><span data-stu-id="26a7c-108">IEventListener</span></span>](event-ievent.md#ieventlistener)

## <a name="types"></a><span data-ttu-id="26a7c-109">種類</span><span class="sxs-lookup"><span data-stu-id="26a7c-109">Types</span></span>


### <a name="eventhook"></a><span data-ttu-id="26a7c-110">EventHook</span><span class="sxs-lookup"><span data-stu-id="26a7c-110">EventHook</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="26a7c-111">階層</span><span class="sxs-lookup"><span data-stu-id="26a7c-111">Hierarchy</span></span>

<span data-ttu-id="26a7c-112">EventHook</span><span class="sxs-lookup"><span data-stu-id="26a7c-112">EventHook</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="26a7c-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="26a7c-113">Methods</span></span>

| <span data-ttu-id="26a7c-114">氏名</span><span class="sxs-lookup"><span data-stu-id="26a7c-114">Name</span></span> | <span data-ttu-id="26a7c-115">署名</span><span class="sxs-lookup"><span data-stu-id="26a7c-115">Signature</span></span> | <span data-ttu-id="26a7c-116">説明</span><span class="sxs-lookup"><span data-stu-id="26a7c-116">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="26a7c-117">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="26a7c-117">subscribe</span></span>](../interfaces/event-ievent-ieventhook.md#subscribe) |<span data-ttu-id="26a7c-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="26a7c-118">subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="26a7c-119">このイベントにリスナーをサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="26a7c-119">Subscribe a listener to this event.</span></span><br>  |
| [<span data-ttu-id="26a7c-120">unsubscribe</span><span class="sxs-lookup"><span data-stu-id="26a7c-120">unsubscribe</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribe) |<span data-ttu-id="26a7c-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span><span class="sxs-lookup"><span data-stu-id="26a7c-121">unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void</span></span>|<span data-ttu-id="26a7c-122">このイベントからリスナーを解除します。</span><span class="sxs-lookup"><span data-stu-id="26a7c-122">Unsubscribe a listener from this event.</span></span><br>  |
| [<span data-ttu-id="26a7c-123">unsubscribeAll</span><span class="sxs-lookup"><span data-stu-id="26a7c-123">unsubscribeAll</span></span>](../interfaces/event-ievent-ieventhook.md#unsubscribeall) |<span data-ttu-id="26a7c-124">unsubscribeAll(): void</span><span class="sxs-lookup"><span data-stu-id="26a7c-124">unsubscribeAll(): void</span></span>|<span data-ttu-id="26a7c-125">このイベントからすべてのリスナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="26a7c-125">Remove all listeners from this event.</span></span><br>  |

## <a name="type-aliases"></a><span data-ttu-id="26a7c-126">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="26a7c-126">Type aliases</span></span>


### <a name="ieventlistener"></a><span data-ttu-id="26a7c-127">IEventListener</span><span class="sxs-lookup"><span data-stu-id="26a7c-127">IEventListener</span></span>
<span data-ttu-id="26a7c-128">IEventListener: 機能</span><span class="sxs-lookup"><span data-stu-id="26a7c-128">IEventListener: function</span></span>




