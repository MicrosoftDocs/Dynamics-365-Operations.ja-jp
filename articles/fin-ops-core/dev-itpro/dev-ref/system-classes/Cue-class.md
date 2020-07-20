---
title: キュー クラス
description: このトピックでは、キュー クラスについて説明します。
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
ms.openlocfilehash: f5b9ff7c933b2c0394ab0cb5fb4e48f09e814566
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502701"
---
# <a name="class-cue"></a>クラス キュー

[!include [banner](../../includes/banner.md)]

```xpp
class Cue extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                         | 説明                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])            | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])        | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])          | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])            | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])       | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])         |                                                                                                                                           |
| public int cueMax(\[int value\])               |                                                                                                                                           |
| public str dataField(\[str value\])            |                                                                                                                                           |
| public str label(\[str value\])                | コントロールのラベルを取得または設定します。                                                                                                     |
| public str LabelId()                           |                                                                                                                                           |
| public str menuItemName(\[str value\])         |                                                                                                                                           |
| public str name(\[str value\])                 | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])             |                                                                                                                                           |
| public str previewPartReference(\[str value\]) |                                                                                                                                           |
| public boolean showAlert(\[boolean value\])    |                                                                                                                                           |
| public int showAlertValue(\[int value\])       |                                                                                                                                           |
| public int showAlertWhen(\[int value\])        |                                                                                                                                           |
| public boolean showSum(\[boolean value\])      |                                                                                                                                           |
| public str table(\[str value\])                | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                                     |
| public void new(str cueName)                   | TreeNode クラスの新しいインスタンスを初期化します。                                                                                         |

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-cuemax"></a>メソッド cueMax

```xpp
public int cueMax([int value])
```

### <a name="parameters---cuemax"></a>パラメーター - cueMax

値  

### <a name="return-value---cuemax"></a>戻り値 - cueMax

## <a name="method-datafield"></a>メソッド dataField

```xpp
public str dataField([str value])
```

### <a name="parameters---datafield"></a>パラメーター - dataField

値  

### <a name="return-value---datafield"></a>戻り値 - dataField

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

## <a name="method-labelid"></a>メソッド LabelId

```xpp
public str LabelId()
```

### <a name="return-value---labelid"></a>戻り値 - LabelId

## <a name="method-menuitemname"></a>メソッド menuItemName

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a>パラメーター - menuItemName

値  

### <a name="return-value---menuitemname"></a>戻り値 - menuItemName

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - 名前

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - 名前

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-previewpartreference"></a>メソッド previewPartReference

```xpp
public str previewPartReference([str value])
```

### <a name="parameters---previewpartreference"></a>パラメーター - previewPartReference

値  

### <a name="return-value---previewpartreference"></a>戻り値 - previewPartReference

## <a name="method-showalert"></a>メソッド showAlert

```xpp
public boolean showAlert([boolean value])
```

### <a name="parameters---showalert"></a>パラメーター - showAlert

値  

### <a name="return-value---showalert"></a>戻り値 - showAlert

## <a name="method-showalertvalue"></a>メソッド showAlertValue

```xpp
public int showAlertValue([int value])
```

### <a name="parameters---showalertvalue"></a>パラメーター - showAlertValue

値  

### <a name="return-value---showalertvalue"></a>戻り値 - showAlertValue

## <a name="method-showalertwhen"></a>メソッド showAlertWhen

```xpp
public int showAlertWhen([int value])
```

### <a name="parameters---showalertwhen"></a>パラメーター - showAlertWhen

値  

### <a name="return-value---showalertwhen"></a>戻り値 - showAlertWhen

## <a name="method-showsum"></a>メソッド showSum

```xpp
public boolean showSum([boolean value])
```

### <a name="parameters---showsum"></a>パラメーター - showSum

値  

### <a name="return-value---showsum"></a>戻り値 - showSum

## <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

```xpp
public str table([str value])
```

### <a name="parameters---table"></a>パラメーター - table

値  

### <a name="return-value---table"></a>戻り値 - toBlob

オブジェクトに関連付けられたテーブル ID の現在の値。

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new(str cueName)
```

### <a name="parameters---new"></a>パラメーター - new

cueName  

