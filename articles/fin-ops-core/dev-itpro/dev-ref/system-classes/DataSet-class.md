---
title: DataSet クラス
description: このトピックでは、DataSet クラスについて説明します。
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
ms.openlocfilehash: 8de93053ace905a2e8fa5ba44e5ef84e97c1d429
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502736"
---
# <a name="class-dataset"></a>クラス データセット

[!include [banner](../../includes/banner.md)]

```xpp
class DataSet extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                  | 説明                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public FormBuildDataSource addDataSource(str name)      |                                                                                                                                   |
| public str changedBy(\[str value\])                     | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                        |
| public Date changedDate(\[Date value\])                 | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                     |
| public str changedTime(\[str value\])                   | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                     |
| public str createdBy(\[str value\])                     | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                             |
| public Date creationDate(\[Date value\])                | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                          |
| public str creationTime(\[str value\])                  |                                                                                                                                   |
| public FormBuildDataSource dataSource(int dataSourceNo) |                                                                                                                                   |
| public int dataSourceCount()                            |                                                                                                                                   |
| public str name(\[str value\])                          | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                      |                                                                                                                                   |
| public void load(str name, \[boolean buildMode\])       |                                                                                                                                   |
| public void finalize()                                  |                                                                                                                                   |
| public void new(\[str name\], \[boolean buildMode\])    | TreeNode クラスの新しいインスタンスを初期化します。                                                                                 |
| public void save()                                      |                                                                                                                                   |

## <a name="method-adddatasource"></a>メソッド addDataSource

```xpp
public FormBuildDataSource addDataSource(str name)
```

### <a name="parameters---adddatasource"></a>パラメーター - addDataSource

名前  

### <a name="return-value---adddatasource"></a>戻り値 - addDataSource

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

## <a name="method-datasource"></a>メソッド dataSource

```xpp
public FormBuildDataSource dataSource(int dataSourceNo)
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

dataSourceNo  

### <a name="return-value---datasource"></a>戻り値 - dataSource

## <a name="method-datasourcecount"></a>メソッド dataSourceCount

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a>戻り値 - dataSourceCount

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
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-load"></a>メソッド load

```xpp
public void load(str name, [boolean buildMode])
```

### <a name="parameters---load"></a>パラメーター - load

名前  

<!-- -->

buildMode  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new([str name], [boolean buildMode])
```

### <a name="parameters---new"></a>パラメーター - new

名前  

<!-- -->

buildMode  

## <a name="method-save"></a>メソッド save

```xpp
public void save()
```

