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






[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]