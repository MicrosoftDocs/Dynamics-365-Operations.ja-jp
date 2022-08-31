---
title: 延期モジュール
description: 延期タイプ
author: jasongre
ms.date: 05/26/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: 13a62c1600868b6adcda0bdb2a86844f248080c4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282525"
---
# <a name="defer-module"></a>延期モジュール

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

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



#### <a name="returns-deferred-lttgt"></a>[Deferred](../interfaces/defer-ideferred.md) &lt;T&gt; を返します


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



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
