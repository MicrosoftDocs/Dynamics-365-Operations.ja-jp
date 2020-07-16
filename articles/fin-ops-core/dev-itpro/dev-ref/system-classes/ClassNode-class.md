---
title: ClassNode クラス
description: このトピックでは、ClassNode クラスについて説明します。
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
ms.openlocfilehash: 83cda89cf097ef5e78884aa311a9cfec0cfd3ab4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502712"
---
# <a name="class-classnode"></a>クラス ClassNode

[!include [banner](../../includes/banner.md)]


```xpp
class ClassNode extends TreeNode
```

ClassNode クラスは、アプリケーション オブジェクト ツリー (AOT) のクラスを表す TreeNode クラスの特殊な形式です。

## <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                            | 説明                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public TreeNode AOToverrideMethod(str methodName) |                                                                                                                                               |
| public str changedBy(\[str value\])               | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])           | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])             | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])               | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])          | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])            |                                                                                                                                               |
| public str extends(\[str value\])                 |                                                                                                                                               |
| public int iD(\[int value\])                      |                                                                                                                                               |
| public boolean isDetached()                       |                                                                                                                                               |
| public int legacyId(\[int value\])                |                                                                                                                                               |
| public str name(\[str value\])                    | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                |                                                                                                                                               |
| public int runOn(\[int value\])                   |                                                                                                                                               |
| public void AOTedit(\[int Line\], \[int Column\]) | クラスを開き、エディターで変更することもできるようにします。                                                                                     |

## <a name="method-aotoverridemethod"></a>メソッド AOToverrideMethod

```xpp
public TreeNode AOToverrideMethod(str methodName)
```

### <a name="parameters---aotoverridemethod"></a>パラメーター - AOToverrideMethod

methodName  

### <a name="return-value---aotoverridemethod"></a>戻り値 - AOToverrideMethod

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

## <a name="method-extends"></a>メソッド extends

```xpp
public str extends([str value])
```

### <a name="parameters---extends"></a>パラメーター - extends

値  

### <a name="return-value---extends"></a>戻り値 - extends

## <a name="method-id"></a>メソッド iD

```xpp
public int iD([int value])
```

### <a name="parameters---id"></a>パラメーター - iD

値  

### <a name="return-value---id"></a>戻り値 - iD

## <a name="method-isdetached"></a>メソッド isDetached

```xpp
public boolean isDetached()
```

### <a name="return-value---isdetached"></a>戻り値 - isDetached

## <a name="method-legacyid"></a>メソッド legacyId

```xpp
public int legacyId([int value])
```

### <a name="parameters---legacyid"></a>パラメーター - legacyId

値  

### <a name="return-value---legacyid"></a>戻り値 - legacyId

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

## <a name="method-runon"></a>メソッド runOn

```xpp
public int runOn([int value])
```

### <a name="parameters---runon"></a>パラメーター - runOn

値  

### <a name="return-value---runon"></a>戻り値 - runOn

## <a name="method-aotedit"></a>メソッド AOTedit

クラスを開き、エディターで変更することもできるようにします。

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a>パラメーター - AOTedit

折れ線  
無視される値、オプション。

<!-- -->

円柱  
無視される値、オプション。

### <a name="remarks---aotedit"></a>備考 - AOTedit

すべてのメソッドはエディターに読み込まれます。 引数は、下位互換性のためにのみ署名に含まれているため、無視されます。

### <a name="examples---aotedit"></a>例 - AOTedit

```xpp
static void example() 
{ 
    ClassNode classNode; 
```

```xpp
    classNode = infolog.findNode('\Classes\SysClassWizard'); 
    classNode.AOTedit(); 
}
```

