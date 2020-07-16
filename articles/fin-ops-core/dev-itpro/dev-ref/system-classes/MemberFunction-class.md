---
title: MemberFunction クラス
description: このトピックでは、MemberFunction クラスについて説明します。
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
ms.openlocfilehash: 0c838cd651a9bf80f4d2e8a9019ba132e986e078
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502574"
---
# <a name="class-memberfunction"></a>クラス MemberFunction

[!include [banner](../../includes/banner.md)]

```xpp
class MemberFunction extends TreeNode
```

MemberFunction クラスは、フォーム、レポート、クラスなどのアプリケーション オブジェクト ツリー (AOT) で指定されたノードに関する情報を提供します。

## <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 ::findNode メソッドを使用すると MemberFunction クラスのインスタンスにノードを割り当てることができます。

## <a name="examples"></a>例

次の例では、TreeNode::findNode メソッドを使用して、AddressSelectForm.callerDataSource メソッドのノードを MemberFunction クラスのインスタンスに割り当てます。 MemberFunction.AOTgetSource メソッドは、メソッドのソース コードを返します。

```xpp
void getMemberFunction() 
{ 
    MemberFunction memberFunction; 
    str name; 
    boolean isStatic; 
    str source; 
    try 
    { 
        memberFunction = TreeNode::findNode( 
           '\\Classes\\AddressSelectForm\\callerDataSource'); 
        if(!memberFunction) 
        { 
            throw exception::Error; 
        } 
        source = memberFunction.AOTgetSource(); 
        print source; 
        pause; 
    } 
    catch (exception::Error) 
    { 
        print "The specified node does not exist."; 
        pause; 
        } 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。                                                    |
| public boolean canAddEventHandler()                        |                                                                                                                                         |
| public boolean isEvent()                                   |                                                                                                                                         |
| public boolean isStatic()                                  | メソッドが静的かどうかを示します。                                                                                                   |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public void AOTedit(\[int Line\], \[int Column\])          | AOT で指定したノードの適切なエディタを開きます。                                                                           |
| public void new()                                          | MemberFunction クラスの新しいインスタンスを初期化します。                                                                                 |
| public void AOTsetSource(str source, \[boolean isStatic\]) | クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。                                                        |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ソース コードの文字列値、ノードにソース コードが含まれていない場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

## <a name="method-canaddeventhandler"></a>メソッド canAddEventHandler

```xpp
public boolean canAddEventHandler()
```

### <a name="return-value---canaddeventhandler"></a>戻り値 - canAddEventHandler

## <a name="method-isevent"></a>メソッド isEvent

```xpp
public boolean isEvent()
```

### <a name="return-value---isevent"></a>戻り値 - isEvent

## <a name="method-isstatic"></a>メソッド isStatic

メソッドが静的かどうかを示します。

```xpp
public boolean isStatic()
```

### <a name="return-value---isstatic"></a>戻り値 - isStatic

メソッドが静的である場合は true。それ以外の場合は、false。

### <a name="remarks---isstatic"></a>備考 - isStatic

このメソッドは、AOT の指定されたノード (フォーム、レポート、クラスなど) に関連付けられます。 このメソッドは、主に MemberFunction::AOTsetSource メソッドと組み合わせて使用されます。

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  
ノードを指定する文字列、オプション。

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えていません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-aotedit"></a>メソッド AOTedit

AOT で指定したノードの適切なエディタを開きます。

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a>パラメーター - AOTedit

折れ線  
カーソルの列の位置を指定する整数。オプション。

<!-- -->

円柱  
カーソルの列の位置を指定する整数。オプション。

## <a name="method-new"></a>メソッド new

MemberFunction クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-aotsetsource"></a>メソッド AOTsetSource

クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a>パラメーター - AOTsetSource

ソース  
ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。

<!-- -->

isStatic  
ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。

