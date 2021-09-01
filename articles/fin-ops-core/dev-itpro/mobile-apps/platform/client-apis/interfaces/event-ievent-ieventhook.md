---
title: EventHook タイプ<T>
description: EventHook タイプ
author: robinarh
ms.date: 08/01/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.openlocfilehash: 660c392e2725d2522760a0c24d26742e1f50ff5120a7129481bb2b901cacfb17
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712548"
---
# <a name="eventhook-typelttgt"></a>EventHook タイプ&lt;T&gt;

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a>階層

EventHook <br>

## <a name="index"></a>指数

### <a name="methods"></a>メソッド

* [サブスクライブ](event-ievent-ieventhook.md#subscribe)
* [unsubscribe](event-ievent-ieventhook.md#unsubscribe)
* [unsubscribeAll](event-ievent-ieventhook.md#unsubscribeall)

## <a name="methods"></a>メソッド

### <a name="subscribe"></a>subscribe


subscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void

このイベントにリスナーをサブスクライブします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| listener|[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;||

#### <a name="returns-void"></a>void を返します

### <a name="unsubscribe"></a>unsubscribe


unsubscribe(listener: [IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;): void

このイベントからリスナーを解除します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| listener|[IEventListener](../modules/event-ievent.md#ieventlistener) &lt;T&gt;||

#### <a name="returns-void"></a>void を返します

### <a name="unsubscribeall"></a>unsubscribeAll


unsubscribeAll(): void

このイベントからすべてのリスナーを削除します。

#### <a name="returns-void"></a>void を返します



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]