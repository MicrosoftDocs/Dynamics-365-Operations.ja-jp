---
title: Set クラス
description: このトピックでは、Set クラスについて説明します。
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
ms.openlocfilehash: b2ada346c1917d3efcb04b9c6018111661843e0c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502805"
---
# <a name="class-set"></a>クラスのセット

[!include [banner](../../includes/banner.md)]

```xpp
class Set extends Object
```

Set クラスは、格納されている要素の値が固有であり、自動的に並べ替えられるデータに応じたキー値として機能するコレクションからデータを格納して取得ために使用されます。

## <a name="remarks"></a>備考

値は任意の X++ 型にできます。 セット内のすべての値には同じタイプが必要です。 セットにすでに保存されている値が追加されると、その値は無視され、セット内の要素の数を増加させません。 セットに格納された値は、SetEnumerator 型のオブジェクトを使用してスキャンできます。 セットのコンテンツは、要素の効率的な検索を容易にする方法で格納されます。

## <a name="examples"></a>例

次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。 見つかった場合は、yesConfigs セットから削除されます。

```xpp
Set             noConfigs; 
Set             yesConfigs; 
ConfigId        configId; 
SetEnumerator   se; 
; 
se = noConfigs.getEnumerator(); 
while (se.moveNext()) 
{ 
    configId    = se.current(); 
    if (yesConfigs.in(configId)) 
    { 
        yesConfigs.remove(configId); 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                               | 説明                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public boolean add(AnyType arg)                      | セットに要素を追加します。                                                                                                       |
| public str definitionString()                        | セット内のすべての要素のタイプの説明を返します。                                                                     |
| public int elements()                                | セット内の要素の数を返します。                                                                                        |
| public boolean empty()                               | セットが空であるかどうかを判定します。                                                                                              |
| public boolean equal(Set set)                        | セットが現在のセットと同一かどうかを判定します。                                                                         |
| public SetEnumerator getEnumerator()                 | セット内のスキャンを可能にする、セットの列挙子を作成します。                                                            |
| public boolean in(AnyType arg)                       | 指定された要素がセットのメンバーであるかどうかを判定します。                                                                    |
| public container pack()                              | Set クラスの現在のインスタンスをシリアル化します。                                                                                 |
| public boolean remove(AnyType arg)                   | セットから要素を削除します。                                                                                                  |
| public str toString()                                | 設定の内容を説明する文字列を返します。                                                                              |
| public Types typeId()                                | セット内の値のタイプを返します。                                                                                        |
| public str xml(\[int indent\])                       | 現在のオブジェクトを表す XML 文字列を返します。                                                                         |
| ::public static Set create(container container)      | 以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。                                               |
| ::public static Set createFromXML(Object xmlnode)    |                                                                                                                                   |
| ::public static Set difference(Set set1, Set set2)   | set2 で検出されない set1 の要素を含むセットを計算および取得します。                                    |
| ::public static Set intersection(Set set1, Set set2) | 2 つのセット内で検出される同一の値を計算して返します。                                                                    |
| ::public static Set union(Set set1, Set set2)        | 指定された 2 つのセットの和集合を計算および取得します これは、少なくとも 1 つのセットにある値を含むセットです。 |
| public void new(Types Type)                          | 指定した型の要素を含めることができるセットを作成します。                                                                    |

## <a name="method-add"></a>メソッド add

セットに要素を追加します。

```xpp
public boolean add(AnyType arg)
```

### <a name="parameters---add"></a>パラメーター - add

arg  
セットに追加する要素。

### <a name="return-value---add"></a>戻り値 - add

要素がセットに追加された場合は true。それ以外の場合は、false。

### <a name="remarks---add"></a>備考 - add

セットに追加される要素は、セットの作成時にセットに割り当てられたタイプと同じタイプでなければなりません。 既にセットに存在する場合、要素は追加されません。

### <a name="examples---add"></a>例 - add

次の例では、セットを作成し、いくつかの整数を追加してから、セットの内容を出力します。

```xpp
{ 
    // Create a set of integers 
    Set is = new Set (Types::Integer); 
    int i; 
    ;  
    // Add values 0 to 9 to the set 
    for (i = 0; i < 10; i++) 
    { 
        is.add(i); 
    } 
    print is.toString(); 
    pause; 
}
```

## <a name="method-definitionstring"></a>メソッド definitionString

セット内のすべての要素のタイプの説明を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

設定の定義を含む文字列。

### <a name="remarks---definitionstring"></a>備考 - definitionString

セット内の値の一覧を印刷するには、Set.toString を使用します。

### <a name="examples---definitionstring"></a>例 - definitionString

次の例では、整数のセットを作成します。 definitionString メソッドを使用して、セットの説明を出力します。

```xpp
{ 
    // Declare a set of integers 
    Set is = new Set (Types::Integer);  
    ; 
    // Add some integers to the set 
    print is.add(1); 
    print is.add(2); 
    print is.add(1); 
    // Print a description of the set 
    print is.definitionString(); 
    // Print a description of the set elements 
    print is.toString(); 
    pause; 
}
```

## <a name="method-elements"></a>メソッド elements

セット内の要素の数を返します。

```xpp
public int elements()
```

### <a name="return-value---elements"></a>戻り値 - elements

セット内の要素の数。

### <a name="examples---elements"></a>例 - elements

次の例では、セットの内容をコンテナーにパックします。 要素メソッドは、セットに任意のコンテンツが含まれているかどうかをテストするために使用されます。 コンテンツがない場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなしになる) コンテナーが返されます。

```xpp
public static container intSet2Con(Set _intSet) 
{ 
    SetEnumerator se; 
    container     intCon; 
    ; 
    if (!_intSet || !_intSet.elements()) 
    { 
        return conNull(); 
    } 
    se = _intSet.getEnumerator(); 
    while (se.moveNext()) 
    { 
        intCon += se.current(); 
    } 
    return intCon; 
}
```

## <a name="method-empty"></a>メソッド empty

セットが空であるかどうかを判定します。

```xpp
public boolean empty()
```

### <a name="return-value---empty"></a>戻り値 - empty

セットが空の場合は true。それ以外の場合は、false。

### <a name="remarks---empty"></a>備考 - empty

これは、(elements() == 0) と等価です。

### <a name="examples---empty"></a>例 - empty

次の例では、セットに要素があるかどうかをテストします。

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    ; 
    // ... 
    if (mySet.empty()) 
    { 
        print "There are no values in the set"; 
    } 
}
```

## <a name="method-equal"></a>メソッド equal

セットが現在のセットと同一かどうかを判定します。

```xpp
public boolean equal(Set set)
```

### <a name="parameters---equal"></a>パラメーター - equal

set  
現在のセットと比較されるセット。

### <a name="return-value---equal"></a>戻り値 - equal

そのセットが現在のセットと同じである場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

2 つのセットが等しくなるためには、それらには同じタイプおよび同じ数の要素があり、すべての要素は同じである必要があります。

### <a name="examples---equal"></a>例 - equal

次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加し、それらを比較してセットが同じかどうかを確認します。

```xpp
{ 
    Set is1 = new Set (Types::Integer); 
    Set is2 = new Set (Types::Integer); 
    ; 
    is1.add(1); 
    is1.add(2); 
    is1.add(3); 
    is2.add(2); 
    is2.add(4); 
    if (is1.equal(is2)) 
    { 
        print "The sets are equal"; 
        pause; 
    } 
    else 
    { 
         print "The sets are not equal"; 
         pause; 
     } 
}
```

## <a name="method-getenumerator"></a>メソッド getEnumerator

セット内のスキャンを可能にする、セットの列挙子を作成します。

```xpp
public SetEnumerator getEnumerator()
```

### <a name="return-value---getenumerator"></a>戻り値 - getEnumerator

現在のセットの SetEnumerator オブジェクト。

### <a name="examples---getenumerator"></a>例 - getEnumerator

次の例では、セットの内容をコンテナーにパックします。 getEnumerator メソッドは、セットの列挙子を作成するために使用されます。 したがって、セット内の要素を横断してコンテナーに追加することができます。

```xpp
public static container intSet2Con(Set _intSet) 
{ 
    SetEnumerator se; 
    container     intCon; 
    ; 
    if (!_intSet || !_intSet.elements()) 
    { 
        return conNull(); 
    } 
    se = _intSet.getEnumerator(); 
    while (se.moveNext()) 
    { 
        intCon += se.current(); 
    } 
    return intCon; 
}
```

## <a name="method-in"></a>メソッド in

指定された要素がセットのメンバーであるかどうかを判定します。

```xpp
public boolean in(AnyType arg)
```

### <a name="parameters---in"></a>パラメーター - in

arg  
チェックする要素。 要素のタイプは、セットの指定されたタイプと同じである必要があります。

### <a name="return-value---in"></a>戻り値 - in

指定した要素がセット内で見つかる場合は true。それ以外の場合は、false。

### <a name="examples---in"></a>例 - in

次の例では、in メソッドが false を返す場合、バージョン コントロール システム内の特定の変更リストの内容を読み込みます。 changeSet セットには、コンテンツが既にロードされている変更リスト番号のリストが含まれています。

```xpp
public void pageActivated() 
{ 
    SysVersionControlTmpItem contentsAddition; 
    if (!changeSet.in(changes.ChangeNumber)) 
    { 
        startLengthyOperation(); 
        contentsAddition = versioncontrol.getChangeNumberContents( 
            changes.ChangeNumber); 
        while select contentsAddition 
        { 
            contentsItem.data(contentsAddition); 
            contentsItem.insert(); 
        } 
        contents_ds.executeQuery(); 
        changeSet.add(changes.ChangeNumber); 
    } 
    super(); 
}
```

## <a name="method-pack"></a>メソッド pack

Set クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

Set クラスの現在のインスタンスを含むコンテナーです。

### <a name="remarks---pack"></a>備考 - pack

このメソッドで作成されたコンテナーには、セットの最初の要素の前に 3 つの要素が含まれます。

-   コンテナのバージョン番号
-   セット要素のデータ型を識別する整数
-   セット内の要素の数。

キーまたは値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを作成します。 Set::create method を使用することにより、結果のコンテナから新しいセットを作成することができます。

### <a name="examples---pack"></a>例 - pack

次の例では、10 個の整数のセットを作成し、それをコンテナーにパックし、元の内容と同じ内容の新しいセットを作成します。

```xpp
{ 
    Set is1, is = new Set (Types::Integer); 
    int i; 
    container packedSet; 
    ; 
    // Create a set containing the first 10 integers. 
    for (i = 1; i <= 10; i++) 
    { 
        is.add(i); 
    } 
    // Pack it down in a container... 
    packedSet = is.pack(); 
    // ... and restore it 
    is1 = Set::create(packedSet); 
    print is1.toString(); 
    pause; 
}
```

## <a name="method-remove"></a>メソッド remove

セットから要素を削除します。

```xpp
public boolean remove(AnyType arg)
```

### <a name="parameters---remove"></a>パラメーター - remove

arg  
削除する要素。

### <a name="return-value---remove"></a>戻り値 - remove

要素が見つかり削除された場合は true。それ以外の場合は、false。

### <a name="examples---remove"></a>例 - remove

次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。 見つかった場合は、yesConfigs セットから削除されます。

```xpp
Set             noConfigs; 
Set             yesConfigs; 
ConfigId        configId; 
SetEnumerator   se; 
; 
se = noConfigs.getEnumerator(); 
while (se.moveNext()) 
{ 
    configId    = se.current(); 
    if (yesConfigs.in(configId)) 
    { 
        yesConfigs.remove(configId); 
    } 
}
```

## <a name="method-tostring"></a>メソッド toString

設定の内容を説明する文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

設定の内容を説明する文字列。

### <a name="remarks---tostring"></a>備考 - toString

を使用して、セット内の単一要素の説明を取得します。

### <a name="examples---tostring"></a>例 - toString

次の例では、文字列のセットを作成し、そのセットの説明とセット内容の説明を出力します。

```xpp
{ 
    // Declare a set of strings 
    Set names = new Set (Types::String); 
    ; 
    // Add some values to the set. 
    names.add("Peter"); 
    names.add("Paul"); 
    names.add("Mary"); 
    print names.definitionString(); 
    print names.toString(); 
    pause; 
}
```

## <a name="method-typeid"></a>メソッド typeId

セット内の値のタイプを返します。

```xpp
public Types typeId()
```

### <a name="return-value---typeid"></a>戻り値 - typeId

セット内の値のタイプ。

### <a name="remarks---typeid"></a>備考 - typeId

構成要素のタイプは、そのセットが作成されるときに決定される。

### <a name="examples---typeid"></a>例 - typeId

次の例では、既存のセットと同じタイプの新しいセットをインスタンス化します。

```xpp
{ 
    Set set1 = new Set(Types::Integer); 
    Set set2; 
   ; 
    set2 = new Set(set1.typeId()); 
    print set2.typeId(); 
    pause; 
}
```

## <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a>パラメーター - xml

インデント  
返された XML 文字列のインデントの量 (省略可能)。

### <a name="return-value---xml"></a>戻り値 - xml

現在のオブジェクトを表す XML 文字列です。

### <a name="remarks---xml"></a>備考 - xml

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

## <a name="method-create"></a>メソッド create

以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。

```xpp
public static Set create(container container)
```

### <a name="parameters---create"></a>パラメーター - create

コンテナー  
パックされたセットを保持するコンテナー。

### <a name="return-value---create"></a>戻り値 - create

コンテナーに梱包されたものと同じセット。

### <a name="remarks---create"></a>備考 - create

値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。

### <a name="examples---create"></a>例 - create

次の例では、セットを作成し、それをコンテナーにパックします。 次に、create メソッドを使用してコンテナーを展開し、元のセットと同じセットを作成します。

```xpp
{ 
    Set is1, is = new Set (Types::Integer); 
    int i; 
    container packedSet; 
    ; 
    // Add 10 integers (0 - 9) to the set 
    for (i = 1; i <= 10; i++) 
    { 
        is.add(i); 
    } 
    // Pack the set into a container... 
    packedSet = is.pack(); 
    // ... and restore it 
    is1 = Set::create(packedSet); 
    print is1.toString(); 
    pause; 
}
```

## <a name="method-createfromxml"></a>メソッド createFromXML

```xpp
public static Set createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a>パラメータ - createFromXML

xmlnode  

### <a name="return-value---createfromxml"></a>戻り値 - createFromXML

## <a name="method-difference"></a>メソッド difference

set2 で検出されない set1 の要素を含むセットを計算および取得します。

```xpp
public static Set difference(Set set1, Set set2)
```

### <a name="parameters---difference"></a>パラメーター - difference

set1  
チェックするセット。

<!-- -->

set2  
チェックするセット。

### <a name="return-value---difference"></a>戻り値 - difference

set2 で検出されない set1 の要素を含むセット。

### <a name="remarks---difference"></a>備考 - difference

比較される 2 つのセットは、同じタイプでなければなりません。

### <a name="examples---difference"></a>例 - difference

次の例では、整数 1､2 および 3 を含む 1 つのセットと、整数 2 および 4 を含む 1 つのセットを作成します。 差異メソッドは、最初のセット内の 2 番目のセット (1 および 3) にない要素を含むセットを作成するために使用されます。

```xpp
{ 
    Set is = new Set (Types::Integer); 
    Set is2, is1 = new Set (Types::Integer); 
    ; 
    is.add(1); 
    is.add(2); 
    is.add(3); 
    is1.add(2); 
    is1.add(4); 
    is2 = Set::difference(is, is1); 
    // prints "{1, 3}" 
    print is2.toString(); 
    pause; 
}
```

## <a name="method-intersection"></a>メソッド intersection

2 つのセット内で検出される同一の値を計算して返します。

```xpp
public static Set intersection(Set set1, Set set2)
```

### <a name="parameters---intersection"></a>パラメーター - intersection

set1  
比較する 2 番目のセット。

<!-- -->

set2  
比較する 2 番目のセット。

### <a name="return-value---intersection"></a>戻り値 - intersection

両方のセットで検出された要素を含むセット。

### <a name="examples---intersection"></a>例 - intersection

次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。 両方のセットに含まれている値の一覧を出力します。

```xpp
{ 
    Set is = new Set (Types::Integer); 
    Set is2, is1 = new Set (Types::Integer); 
    ; 
    is.add(1); 
    is.add(2); 
    is.add(3); 
    is1.add(2); 
    is1.add(4); 
    is2 = Set::intersection(is, is1); 
    // Prints "{2}" because 2 is contained in both is and is2. 
    print is2.toString(); 
}
```

## <a name="method-union"></a>メソッド union

指定された 2 つのセットの和集合を計算および取得します これは、少なくとも 1 つのセットにある値を含むセットです。

```xpp
public static Set union(Set set1, Set set2)
```

### <a name="parameters---union"></a>パラメーター - union

set1  
比較される 2 つのセットのうちの 2 番目のセット。

<!-- -->

set2  
比較される 2 つのセットのうちの 2 番目のセット。

### <a name="return-value---union"></a>戻り値 - union

set1 または set2 で検出された要素を含むセット。

### <a name="remarks---union"></a>備考 - union

比較される 2 つのセットは、同じタイプでなければなりません。

### <a name="examples---union"></a>例 - union

次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。 セットのいずれかに含まれるすべての値を含む新しいセットを作成します。

```xpp
{ 
    Set is = new Set (Types::Integer); 
    Set is2, is1 = new Set (Types::Integer); 
    ; 
    is.add(1); 
    is.add(2); 
    is.add(3); 
    is1.add(2); 
    is1.add(4); 
    is2 = Set::union(is, is1); 
    // Prints "{1, 2, 3, 4}". 
    print is2.toString(); 
    pause; 
}
```

## <a name="method-new"></a>メソッド new

指定した型の要素を含めることができるセットを作成します。

```xpp
public void new(Types Type)
```

### <a name="parameters---new"></a>パラメーター - new

種類  
セット内の要素のタイプ。

### <a name="remarks---new"></a>備考 - new

セットが作成された後、セットのタイプを変更することはできません。

### <a name="examples---new"></a>例 - new

次の例では、一連の整数とオブジェクトのセットを作成します。

```xpp
{ 
    // Create a set of integers. 
    Set is = new Set (Types::Integer); 
    // Create a set of objects. 
    Set os = new Set (Types::Class); 
}
```

