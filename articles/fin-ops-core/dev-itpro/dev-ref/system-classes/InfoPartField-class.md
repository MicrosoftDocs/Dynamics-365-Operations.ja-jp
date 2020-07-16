---
title: InfoPartField クラス
description: このトピックでは、InfoPartField クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1dfa6717154f7d2a49a679617cd1f1bff83e3e70
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502595"
---
# <a name="class-infopartfield"></a>クラス InfoPartField

[!include [banner](../../includes/banner.md)]

```xpp
class InfoPartField extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                            | 説明                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str dataField(\[str value\])               |                                                                                                                                           |
| public str dataMethod(\[str value\])              |                                                                                                                                           |
| public str dataSource(\[str value\])              | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                  |
| public str label(\[str value\])                   | コントロールのラベルを取得または設定します。                                                                                                     |
| public boolean manualRetrieval(\[boolean value\]) |                                                                                                                                           |
| public str name(\[str value\])                    | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int style(\[int value\])                   |                                                                                                                                           |
| public void new()                                 | InfoPartField クラスの新しいインスタンスを初期化します。                                                                                    |

## <a name="method-datafield"></a>メソッド dataField

```xpp
public str dataField([str value])
```

### <a name="parameters---datafield"></a>パラメーター - dataField

値  

### <a name="return-value---datafield"></a>戻り値 - dataField

## <a name="method-datamethod"></a>メソッド dataMethod

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a>パラメーター - dataMethod

値  

### <a name="return-value---datamethod"></a>戻り値 - dataMethod

## <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

```xpp
public str dataSource([str value])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

値  

### <a name="return-value---datasource"></a>戻り値 - dataSource

使用されるデータ ソースの ID。

## <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

```xpp
public str label([str value])
```

### <a name="parameters---label"></a>パラメーター - label

値  

### <a name="return-value---label"></a>戻り値 - label

ラベル文字列の現在の値。

### <a name="remarks---label"></a>備考 - label

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

## <a name="method-manualretrieval"></a>メソッド manualRetrieval

```xpp
public boolean manualRetrieval([boolean value])
```

### <a name="parameters---manualretrieval"></a>パラメーター - manualRetrieval

値  

### <a name="return-value---manualretrieval"></a>戻り値 - manualRetrieval

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-style"></a>メソッド style

```xpp
public int style([int value])
```

### <a name="parameters---style"></a>パラメーター - style

値  

### <a name="return-value---style"></a>戻り値 - style

## <a name="method-new"></a>メソッド new

InfoPartField クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

