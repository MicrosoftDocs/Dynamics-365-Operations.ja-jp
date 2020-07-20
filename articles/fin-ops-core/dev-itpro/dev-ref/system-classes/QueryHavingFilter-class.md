---
title: QueryHavingFilter クラス
description: このトピックでは、QueryHavingFilter クラスについて説明します。
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
ms.openlocfilehash: 5dbbb78e39a0692044c91db8c35ad46c2946cf43
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502861"
---
# <a name="class-queryhavingfilter"></a>クラス QueryHavingFilter

[!include [banner](../../includes/banner.md)]

```xpp
class QueryHavingFilter extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                          | 説明                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public AggregateFunction aggregateFunction()    |                                                                                                                                           |
| public QueryBuildDataSource dataSource()        |                                                                                                                                           |
| public boolean enabled(\[boolean value\])       | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public FieldId field(\[FieldId value\])         | オブジェクトに関連付けられているフィールド ID を取得または設定します。                                                                                     |
| public int fieldArrayIndex()                    |                                                                                                                                           |
| public FieldName fieldName()                    |                                                                                                                                           |
| public str label(\[str value\])                 | コントロールのラベルを取得または設定します。                                                                                                     |
| public str name(\[str value\])                  | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str prompt()                             |                                                                                                                                           |
| public int status(\[int value\])                | オブジェクトの状態を取得または設定します。                                                                                                     |
| public TableId table(\[TableId value\])         | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                             |
| public TableId tableSelector(\[TableId value\]) |                                                                                                                                           |
| public str toString()                           | 現在のオブジェクトを表す文字列を返します。                                                                                      |
| public int typeof()                             |                                                                                                                                           |
| public boolean valid()                          |                                                                                                                                           |
| public str value(\[str value\])                 |                                                                                                                                           |
| public void finalize()                          |                                                                                                                                           |

## <a name="method-aggregatefunction"></a>メソッド aggregateFunction

```xpp
public AggregateFunction aggregateFunction()
```

### <a name="return-value---aggregatefunction"></a>戻り値 - aggregateFunction

## <a name="method-datasource"></a>メソッド dataSource

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a>戻り値 - dataSource

## <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

## <a name="method-field"></a>メソッド field

オブジェクトに関連付けられているフィールド ID を取得または設定します。

```xpp
public FieldId field([FieldId value])
```

### <a name="parameters---field"></a>パラメーター - field

値  

### <a name="return-value---field"></a>戻り値 - field

オブジェクトに関連付けられたフィールド ID の現在の値。

## <a name="method-fieldarrayindex"></a>メソッド fieldArrayIndex

```xpp
public int fieldArrayIndex()
```

### <a name="return-value---fieldarrayindex"></a>戻り値 - fieldArrayIndex

## <a name="method-fieldname"></a>メソッド fieldName

```xpp
public FieldName fieldName()
```

### <a name="return-value---fieldname"></a>戻り値 - fieldName

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

## <a name="method-prompt"></a>メソッド prompt

```xpp
public str prompt()
```

### <a name="return-value---prompt"></a>戻り値 - prompt

## <a name="method-status"></a>メソッド status

オブジェクトの状態を取得または設定します。

```xpp
public int status([int value])
```

### <a name="parameters---status"></a>パラメーター - status

値  

### <a name="return-value---status"></a>戻り値 - status

オブジェクトのステータスの現在の値。

## <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a>パラメーター - table

値  

### <a name="return-value---table"></a>戻り値 - toBlob

オブジェクトに関連付けられたテーブル ID の現在の値。

## <a name="method-tableselector"></a>メソッド tableSelector

```xpp
public TableId tableSelector([TableId value])
```

### <a name="parameters---tableselector"></a>パラメーター - tableSelector

値  

### <a name="return-value---tableselector"></a>戻り値 - tableSelector

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-typeof"></a>メソッド typeof

```xpp
public int typeof()
```

### <a name="return-value---typeof"></a>戻り値 - typeof

## <a name="method-valid"></a>メソッド valid

```xpp
public boolean valid()
```

### <a name="return-value---valid"></a>戻り値 - valid

## <a name="method-value"></a>メソッド value

```xpp
public str value([str value])
```

### <a name="parameters---value"></a>パラメーター - value

値  

### <a name="return-value---value"></a>戻り値 - value

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

