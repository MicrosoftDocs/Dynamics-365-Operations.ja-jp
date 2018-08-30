---
title: "AsyncService タイプ"
description: "ビジネス ロジック コードから非同期操作を実行する機能を提供します。"
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
ms.sourcegitcommit: ed6cabcc8c76fba3d4414cd4b564b720c54169e0
ms.openlocfilehash: 4b40b40dad7c7c49cb0b073f729f5920a1ec45d3
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="asyncservice-type"></a>AsyncService タイプ

[!include [banner](../../../../includes/banner.md)]

ビジネス ロジック コードから非同期操作を実行する機能を提供します。

### <a name="hierarchy"></a>階層

AsyncService <br>

## <a name="index"></a>指数

### <a name="methods"></a>メソッド

* [すべて](services-business-logic-services-iasyncservice.md#all)
* [延期](services-business-logic-services-iasyncservice.md#defer)

## <a name="methods"></a>メソッド

### <a name="all"></a>すべて


all(...args: any [ ]): Promise &lt;any [ ]&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| ...args|any [ ]||

#### <a name="returns-promise-ltany--gt"></a>Promise &lt;any [ ]&gt; を返します

### <a name="defer"></a>defer


defer &lt;T&gt;(): [Deferred](defer-ideferred.md) &lt;T&gt;

イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを解決/拒否するために使用できる遅延オブジェクトを作成します。

#### <a name="returns-deferreddefer-ideferredmd-lttgt"></a>[Deferred](defer-ideferred.md) &lt;T&gt; を返します


