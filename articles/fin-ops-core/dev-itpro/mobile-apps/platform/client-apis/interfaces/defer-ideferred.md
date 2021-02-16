---
title: 繰延タイプ<T>
description: 繰延タイプ
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 281099e81d87146cf539c489c1c68d87ee84e96f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685431"
---
# <a name="deferred-typelttgt"></a>延期されたタイプ&lt;T&gt;

[!include [banner](../../../../includes/banner.md)]

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

