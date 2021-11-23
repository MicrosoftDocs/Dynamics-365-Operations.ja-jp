---
title: 承認テスト ライブラリの作成者
description: このトピックでは承認テスト ライブラリの作成者に関する情報を提供します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 8a5f22d4e6a567b822d25765d4f59280bf31c44e
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783154"
---
# <a name="creators-in-the-acceptance-test-library"></a>承認テスト ライブラリの作成者

[!include [banner](../includes/banner.md)]

作成者クラスは、テスト データの作成に使用される Fluent アプリケーション プログラミング インターフェイス (API) を提供します。

## <a name="naming-convention"></a>名前付け規則

`AtlCreator<ModuleName><EntityName>`

この命名規則で:

+ `<ModuleName>` はオプションで、メイン メニューのモジュール名に基づいています。 短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。
+ `<EntityName>` はオプションであり、コマンドが異なる種類のエンティティに適用される場合に使用されます。

## <a name="examples"></a>例

```xpp
AtlCreatorCostGroup

AtlCreatorCustomer
```

## <a name="fluent-setter-methods"></a>Fluent セッター メソッド

作成者クラスは、構築中のエンティティのプロパティの設定に使用する Fluent セッター メソッドを提供する必要があります。

### <a name="naming-convention"></a>名前付け規則

`set<EntityPropertyName>`

この命名規則では、`<EntityPropertyName>` は Fluent メソッドを使用してエンティティに設定されるプロパティ名です。

### <a name="example"></a>例

```xpp
item = new AtlCreatorProductsReleasedVariant()
    .setItemId('DemoItem')
    .setColor(ecoResColor)
    .setStyle(ecoResStyle)
    .setConfig(ecoResConfig)
    .setSize(ecoResSize)
    .create();
```

## <a name="when-should-creators-be-used-instead-of-entities"></a>エンティティの代わりに作成者を使用するのはいつですか。

エンティティと作成者を選択するのに役立つ情報は、[エンティティまたは作成者クラスを実装する必要があるか](atl-faq.md#should-i-implement-an-entity-or-a-creator-class) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]