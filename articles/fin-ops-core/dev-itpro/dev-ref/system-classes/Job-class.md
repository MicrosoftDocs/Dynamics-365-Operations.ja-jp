---
title: Job クラス
description: このトピックでは、Job クラスについて説明します。
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
ms.openlocfilehash: e73a68e3243da4ac17a8f97985d56f9a754e1145
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502593"
---
# <a name="class-job"></a>クラス ジョブ

[!include [banner](../../includes/banner.md)]


```xpp
class Job extends TreeNode
```

Job クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | このノードのソース コードを返します。                                                                                                         |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                            |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                            |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                 |
| public str creationTime(\[str value\])                     |                                                                                                                                               |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                         |                                                                                                                                               |
| public void AOTsetSource(str source, \[boolean isStatic\]) | このノードのソース コードを設定します。                                                                                                            |
| public void AOTrun()                                       | アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。                                                |
| public void AOTedit(\[int Line\], \[int Column\])          | このノードの適切なエディタを開きます。                                                                                                   |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null を参照 (Visual Basic にはなし)。

### <a name="remarks---aotgetsource"></a>備考 - AOTgetSource

この関数はソース コードを持つノードによってオーバーライドされます。

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

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a>パラメーター - AOTsetSource 

ソース  
メソッドが静的かどうかを指定する値、オプション。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値、オプション。

### <a name="remarks---aotsetsource"></a>備考 - AOTgetSource

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="method-aotrun"></a>メソッド AOTrun

アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

```xpp
public void AOTrun()
```

## <a name="method-aotedit"></a>メソッド AOTedit

このノードの適切なエディタを開きます。

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a>パラメーター - AOTedit

折れ線  
カーソル位置の列 (オプション)。

<!-- -->

円柱  
カーソル位置の列 (オプション)。

### <a name="remarks---aotedit"></a>備考 - AOTedit

ノードがメソッドである場合は、コード エディタが開きます。 ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。


