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
# <a name="event-module"></a>イベント モジュール

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a>指数

### <a name="types"></a>種類

* [EventHook](../interfaces/event-ievent-ieventhook.md)

### <a name="type-aliases"></a>型のエイリアス

* [IEventListener](event-ievent.md#ieventlistener)

## <a name="types"></a>種類


### <a name="eventhook"></a>EventHook

#### <a name="hierarchy"></a>階層

EventHook <br>

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [サブスクライブ](../interfaces/event-ievent-ieventhook.md#subscribe) |subscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void|このイベントにリスナーをサブスクライブします。<br>  |
| [unsubscribe](../interfaces/event-ievent-ieventhook.md#unsubscribe) |unsubscribe(listener: [IEventListener](event-ievent.md#ieventlistener) &lt;T&gt;): void|このイベントからリスナーを解除します。<br>  |
| [unsubscribeAll](../interfaces/event-ievent-ieventhook.md#unsubscribeall) |unsubscribeAll(): void|このイベントからすべてのリスナーを削除します。<br>  |

## <a name="type-aliases"></a>型のエイリアス


### <a name="ieventlistener"></a>IEventListener
IEventListener: 機能




