---
title: "延期"
description: "延期タイプ"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 33032b03106391577cb423a5d855dc48c93d14e2
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="defer"></a>延期 

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
| [解決](../interfaces/defer-ideferred.md#resolve) |resolve(value?: T &#124; PromiseLike &lt;T&gt;): void|  |

## <a name="functions"></a>関数


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
resolve &lt;T&gt;(value?: T &#124; PromiseLike &lt;T&gt;): Promise &lt;T&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| value?|T &#124; PromiseLike &lt;T&gt;||

#### <a name="returns-promise-lttgt"></a>Promise &lt;T&gt; を返します


