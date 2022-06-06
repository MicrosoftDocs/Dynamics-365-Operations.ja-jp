---
title: AsyncService タイプ
description: ビジネス ロジック コードから非同期操作を実行する機能を提供します。
author: tonyafehr
ms.date: 05/24/2022
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 733ab5c37f851cd1b041d281e13d3f53294502dc
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811143"
---
# <a name="asyncservice-type"></a>AsyncService タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

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
