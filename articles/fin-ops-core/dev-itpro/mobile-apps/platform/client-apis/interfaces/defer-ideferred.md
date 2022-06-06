---
title: 繰延タイプ<T>
description: 繰延タイプ
author: tonyafehr
ms.date: 05/24/2022
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 6b6339f8467a97ae91e132b433eadacfb32f988e
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811189"
---
# <a name="deferred-typelttgt"></a>延期されたタイプ&lt;T&gt;

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

### <a name="hierarchy"></a>階層

繰延 <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [promise](defer-ideferred.md#promise)

### <a name="methods"></a>メソッド

* [否認](defer-ideferred.md#reject)
* [解決](defer-ideferred.md#resolve)

## <a name="properties"></a>プロパティ

### <a name="promise"></a>promise

promise: Promise &lt;T&gt;




## <a name="methods"></a>メソッド

### <a name="reject"></a>否認


reject(error?: any): void




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| エラー?|any||

#### <a name="returns-void"></a>void を返します

### <a name="resolve"></a>解決


resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void




#### <a name="parameters"></a>パラメーター

| 氏名 | 型 | 説明 |
| ---- | ---- | ----------- |
| value?|T &#124; PromiseLike &lt;T&gt;||

#### <a name="returns-void"></a>void を返します



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
