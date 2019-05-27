---
title: 繰延タイプ<T>
description: 繰延タイプ
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
ms.openlocfilehash: 5fe5bf6b296a935b39af5ba719421fc65ac9d754
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537158"
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

