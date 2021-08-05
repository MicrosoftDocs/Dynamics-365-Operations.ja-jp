---
title: AsyncService タイプ
description: ビジネス ロジック コードから非同期操作を実行する機能を提供します。
author: robinarh
ms.date: 08/01/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.openlocfilehash: 7fc425d2f36d440c6da710954e13347fd0bc8036
ms.sourcegitcommit: ff5e892a91a1585472af2191ae45d6291cceb7f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2021
ms.locfileid: "6661510"
---
# <a name="asyncservice-type"></a>AsyncService タイプ

[!include [banner](../../../../includes/banner.md)]

ビジネス ロジック コードから非同期操作を実行する機能を提供します。

### <a name="hierarchy"></a>階層

AsyncService

## <a name="index"></a>指数

### <a name="method-list"></a>メソッド リスト

* [すべて](services-business-logic-services-iasyncservice.md#all)
* [延期](services-business-logic-services-iasyncservice.md#defer)

## <a name="methods"></a>メソッド

### <a name="all"></a>すべて

`all(...args: any [ ]): Promise <any [ ]>`

#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| ...args|any [ ]||

#### <a name="returns-promise-ltany--gt"></a>Promise &lt;any [ ]&gt; を返します

### <a name="defer"></a>defer

`defer <>(): [Deferred](defer-ideferred.md) <>`

イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを拒否または解決するために使用できる遅延オブジェクトを作成します。

#### <a name="returns-deferred-lttgt"></a>[Deferred](defer-ideferred.md) &lt;T&gt; を返します


[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]