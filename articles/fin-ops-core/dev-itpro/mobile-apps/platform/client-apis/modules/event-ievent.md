---
title: イベント モジュール
description: イベント モジュール
author: tonyafehr
ms.date: 08/01/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 4159bbeb13a649cd4d92ce9edae134f208f976d2
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781726"
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