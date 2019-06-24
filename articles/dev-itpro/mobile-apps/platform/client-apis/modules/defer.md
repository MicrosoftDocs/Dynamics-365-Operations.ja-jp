---
title: 延期モジュール
description: 延期タイプ
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b1762e999010f87dbac3ac6186e79a19d445f44c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547342"
---
# <a name="defer-module"></a>延期モジュール

[!include [banner](../../../../includes/banner.md)]

## <a name="index"></a>指数

### <a name="types"></a>種類

* [Deferred](../interfaces/defer-ideferred.md)

### <a name="functions"></a>関数

* [すべて](defer.md#all)
* [延期](defer.md)
* [否認](defer.md#reject)
* [解決](defer.md#resolve)

## <a name="types"></a>種類


### <a name="deferred"></a>繰延

#### <a name="hierarchy"></a>階層

繰延 <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [promise](../interfaces/defer-ideferred.md#promise) |promise: Promise &lt;T&gt; <br>|  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [否認](../interfaces/defer-ideferred.md#reject) |reject(error?: any): void|  |
| [解決](../interfaces/defer-ideferred.md#resolve) |resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void|  |

## <a name="functions"></a>ファンクション


### <a name="all"></a>すべて
all(...args: any [ ]): Promise &lt;any [ ]&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| ...args|any [ ]||

#### <a name="returns-promise-ltany--gt"></a>Promise &lt;any [ ]&gt; を返します


### <a name="defer"></a>defer
defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;



#### <a name="returns-deferredinterfacesdefer-ideferredmd-lttgt"></a>[Deferred](../interfaces/defer-ideferred.md) &lt;T&gt; を返します


### <a name="reject"></a>否認
reject(error?: any): Promise &lt;any&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| エラー?|any||

#### <a name="returns-promise-ltanygt"></a>Promise &lt;any&gt; を返します


### <a name="resolve"></a>解決
resolve &lt;T&gt; (value?: T &#124; PromiseLike &lt;T&gt;) : Promise &lt;T&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 型 | 説明 |
| ---- | ---- | ----------- |
| value?|T &#124; PromiseLike &lt;T&gt;||

#### <a name="returns-promise-lttgt"></a>Promise &lt;T&gt; を返します

