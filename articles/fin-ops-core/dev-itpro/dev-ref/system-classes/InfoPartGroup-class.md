---
title: InfoPartGroup クラス
description: このトピックでは、InfoPartGroup クラスについて説明します。
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
ms.openlocfilehash: 740c0e2bf55f89d5e4cb01e471697c1b246f522e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502899"
---
# <a name="class-infopartgroup"></a>クラス InfoPartGroup

[!include [banner](../../includes/banner.md)]

```xpp
class InfoPartGroup extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                         | 説明                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str caption(\[str value\])                              | コントロールのキャプションを取得または設定します。                                                                                                      |
| public str dataGroup(\[str value\])                            |                                                                                                                                               |
| public str dataSource(\[str value\])                           | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                      |
| public int labelPosition(\[int value\])                        |                                                                                                                                               |
| public str name(\[str value\])                                 | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public boolean repeating(\[boolean value\])                    |                                                                                                                                               |
| public int rowCountWhenSmall(\[int value\], \[AutoMode mode\]) |                                                                                                                                               |
| public AutoMode rowCountWhenSmallMode(\[AutoMode mode\])       |                                                                                                                                               |
| public int rowCountWhenSmallValue(\[int value\])               |                                                                                                                                               |
| public boolean showCaption(\[boolean value\])                  |                                                                                                                                               |
| public boolean showLabels(\[boolean value\])                   |                                                                                                                                               |
| public int showWhenPartSize(\[int value\])                     |                                                                                                                                               |
| public boolean verticalSpacing(\[boolean value\])              |                                                                                                                                               |
| public void new()                                              | InfoPartGroup クラスの新しいインスタンスを初期化します。                                                                                        |

## <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a>パラメーター - caption

値  

### <a name="return-value---caption"></a>戻り値 - caption

コントロールのキャプションとして使用される文字列。

## <a name="method-datagroup"></a>メソッド dataGroup

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a>パラメーター - dataGroup

値  

### <a name="return-value---datagroup"></a>戻り値 - dataGroup

## <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

```xpp
public str dataSource([str value])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

値  

### <a name="return-value---datasource"></a>戻り値 - dataSource

使用されるデータ ソースの ID。

## <a name="method-labelposition"></a>メソッド labelPosition

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a>パラメーター - labelPosition

値  

### <a name="return-value---labelposition"></a>戻り値 - labelPosition

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

## <a name="method-repeating"></a>メソッド repeating

```xpp
public boolean repeating([boolean value])
```

### <a name="parameters---repeating"></a>パラメーター - repeating

値  

### <a name="return-value---repeating"></a>戻り値 - repeating

## <a name="method-rowcountwhensmall"></a>メソッド rowCountWhenSmall

```xpp
public int rowCountWhenSmall([int value], [AutoMode mode])
```

### <a name="parameters---rowcountwhensmall"></a>パラメーター - rowCountWhenSmall

値  

<!-- -->

モード  

### <a name="return-value---rowcountwhensmall"></a>戻り値 - rowCountWhenSmall

## <a name="method-rowcountwhensmallmode"></a>メソッド rowCountWhenSmallMode

```xpp
public AutoMode rowCountWhenSmallMode([AutoMode mode])
```

### <a name="parameters---rowcountwhensmallmode"></a>パラメーター - rowCountWhenSmallMode

モード  

### <a name="return-value---rowcountwhensmallmode"></a>戻り値 - rowCountWhenSmallMode

## <a name="method-rowcountwhensmallvalue"></a>メソッド rowCountWhenSmallValue

```xpp
public int rowCountWhenSmallValue([int value])
```

### <a name="parameters---rowcountwhensmallvalue"></a>パラメーター - rowCountWhenSmallValue

値  

### <a name="return-value---rowcountwhensmallvalue"></a>戻り値 - rowCountWhenSmallValue

## <a name="method-showcaption"></a>メソッド showCaption

```xpp
public boolean showCaption([boolean value])
```

### <a name="parameters---showcaption"></a>パラメーター - showCaption

値  

### <a name="return-value---showcaption"></a>戻り値 - showCaption

## <a name="method-showlabels"></a>メソッド showLabels

```xpp
public boolean showLabels([boolean value])
```

### <a name="parameters---showlabels"></a>パラメーター - showLabels

値  

### <a name="return-value---showlabels"></a>戻り値 - showLabels

## <a name="method-showwhenpartsize"></a>メソッド showWhenPartSize

```xpp
public int showWhenPartSize([int value])
```

### <a name="parameters---showwhenpartsize"></a>パラメーター - showWhenPartSize

値  

### <a name="return-value---showwhenpartsize"></a>戻り値 - showWhenPartSize

## <a name="method-verticalspacing"></a>メソッド verticalSpacing

```xpp
public boolean verticalSpacing([boolean value])
```

### <a name="parameters---verticalspacing"></a>パラメーター - verticalSpacing

値  

### <a name="return-value---verticalspacing"></a>戻り値 - verticalSpacing

## <a name="method-new"></a>メソッド new

InfoPartGroup クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

