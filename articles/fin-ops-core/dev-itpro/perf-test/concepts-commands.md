---
title: 承認テスト ライブラリのコマンド
description: このトピックでは承認テスト ライブラリとコマンドの使用法に関する情報を提供します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 06de21bb2a8f842c3fcd397a5c834766e5a91ed5
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866210"
---
# <a name="acceptance-test-library-commands"></a>承認テスト ライブラリのコマンド

[!include [banner](../includes/banner.md)]

コマンド クラスは事業運営の実行を処理します。 Fluent アプリケーション プログラミング インターフェイス (API) を使用して、これらの操作のパラメーターを設定します。

## <a name="naming-convention"></a>名前付け規則

`AtlCommand<ModuleName><EntityName><ExecuteBusinessOperation>`

この命名規則で:

+ `<ModuleName>` はメイン メニュー上のモジュール名に基づいています。 短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。
+ `<EntityName>` はオプションであり、コマンドが異なる種類のエンティティに適用される場合に使用されます。
+ `<ExecuteBusinessOperation>` は事業運営の名前を表す動詞です。

## <a name="examples"></a>例

```xpp
AtlCommandInventMark

AtlCommandSalesReturnOrderLineRegister
```

## <a name="implementation"></a>実装

返されるコマンド オブジェクトは、`AtlICommand` インターフェイスを実装し `AtlCommand` クラスから継承する必要があります。

コマンド オブジェクトは、コマンドのパラメータの設定に使用する Fluent セッター メソッドを提供する必要があります。

### <a name="example"></a>例

```xpp
salesLine.pick().setInventDims([locationOut]).setQty(pickedQty).execute();
```

## <a name="fluent-setter-methods"></a>Fluent セッター メソッド

コマンドは 2 種類の Fluent セッター メソッドを許可します、`for` メソッドと `set` メソッド:

+ **for** – これらのメソッドはコマンドが適用されるエンティティを表すコマンド パラメータに使用されます。

    たとえば、請求書コマンドは販売注文に適用できます。 したがって、`for` メソッドは請求書コマンドが適用される販売注文の設定に使用されます。

+ **set** – これらのメソッドはコマンドの他のすべてのパラメータに使用されます。 

    たとえば、販売明細行を予約するときに通常は数量を指定します。 数量はコマンドが適用されるものではありませんが、コマンドの単純なパラメータです。 したがって、`set` メソッドは予約コマンドの数量パラメータの指定に使用されます。

### <a name="naming-convention"></a>名前付け規則

`for<CommandParameterName>`

`set<CommandParameterName>`

この命名規則では、`<CommandParameterName>` は Fluent メソッドを使用してコマンドに設定されるパラメーター名です。

### <a name="examples"></a>例

```xpp
onHandAdjustment.forItem(item).setQuantity(10).execute();
    
picking.forSalesLine(salesLine).setInventDims([warehouse, batch1]).setQuantity(10).execute();
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]