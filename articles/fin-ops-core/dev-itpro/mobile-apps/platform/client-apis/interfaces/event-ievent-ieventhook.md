---
title: EventHook タイプ<T>
description: EventHook タイプ
author: tonyafehr
ms.date: 05/24/2022
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 7b641e164eab9b22c9fa96f743d3a7e63e7ad76a
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811448"
---
# <a name="eventhook-typelttgt"></a>EventHook タイプ&lt;T&gt;

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

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
