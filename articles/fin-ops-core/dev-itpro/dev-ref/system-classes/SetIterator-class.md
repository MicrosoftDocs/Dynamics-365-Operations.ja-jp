---
title: SetIterator クラス
description: このトピックでは、SetIterator クラスについて説明します。
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
ms.openlocfilehash: c2a1fef139dee2773f94d8581e2509ef4bb70e79
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502803"
---
# <a name="class-setiterator"></a>クラス SetIterator

[!include [banner](../../includes/banner.md)]

```xpp
class SetIterator extends Object
```

SetIterator クラスを使用すると、セット内の要素を反復処理できます。

## <a name="remarks"></a>備考

セットの反復子は、反復処理する対象となるセットにポインターとして表示することができます。 繰り返しを開始し、より多くの要素が利用可能であるかどうかを決定し、さらに繰り返しによりポイントされる要素をフェッチする機能が利用可能です。 新しく作成されるセット反復子は、セットの最初の要素に配置されます。 繰り返し中に要素が出現する順序は、要素が挿入される順序ではなく、要素の順序によって定義されます。 より下位の値の要素は、上位の値の要素の前に表示されます。 型の通常の順序が使用されます。 構成要素がオブジェクトである場合、順序を指定するのにオブジェクトのアドレスが使用されます。 特定の注文が推測される可能性はありません。 オブジェクトのアドレスは、本来、一時的です。 SetIterator クラスではなく、そのクラスを使用することをお勧めします。 これにより、別の層の反復子を使用して 1 つの層のセットにアクセスする場合に問題を回避できます。 セット反復子および反復処理するセットは、同じクライアント/サーバー側にある必要があります。 SetIterator を使用し、コードが Called from としてマークされている場合、セットと反復子が別の層で終了しており、コードが失敗する可能性があります。 SetEnumerator を使用する場合、列挙子はセットと同じ層に自動的に作成されます。 また、セット内の次のアイテムに移動するには、反復子セットを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。 SetEnumerator を使用する場合、moveNext メソッドを呼び出すだけです。

## <a name="examples"></a>例

次の例では、整数のセットを作成し、4 つの値をその中に追加します。 各セット要素に関する情報を出力しているセットを通じて反復処理します。

```xpp
    Set s1 = new Set (Types::Integer); 
    int theElement; 
    SetIterator it; 
    ; 
    // Add some elements. 
    s1.add(3); 
    s1.add(4); 
    s1.add(13); 
    s1.add(1); 
    // Start a traversal of the elements in the set. 
    it = new SetIterator(s1); 
    // Prints "(begin)[1]". 
    print it.toString(); 
    // The elements are fetched in the order: 1, 3, 4, 13. 
    while (it.more()) 
    { 
        theElement = it.value(); 
        print theElement; 
         // Fetch the next element. 
        it.next(); 
    } 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------|
| public str definitionString() | 反復子のタイプのテキスト表現を返します。                                          |
| public boolean more()         | 反復子が有効なセット要素を示すかどうかを決定します。                                           |
| public str toString()         | 反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。 |
| public AnyType value()        | 反復子がポイントしている値を取得します。                                                  |
| public void next()            | 次の要素に反復子を移動します。                                                                |
| public void new(Set set)      | セットに対する新しい反復子を作成します。                                                                      |
| public void begin()           | 反復子をセットの先頭に移動します。                                                            |
| public void delete()          | セットの反復子によってポイントされている要素を削除します。                                     |
| public void end()             | セットで最後の要素の後に反復子を移動します。                                                   |

## <a name="method-definitionstring"></a>メソッド definitionString

反復子のタイプのテキスト表現を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

反復子のタイプを示す文字列。

## <a name="method-more"></a>メソッド more

反復子が有効なセット要素を示すかどうかを決定します。

```xpp
public boolean more()
```

### <a name="return-value---more"></a>戻り値 - more

反復子が有効な要素を表す場合は true。それ以外の場合は、false。

### <a name="remarks---more"></a>備考 - more

このメソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。 このメソッドは、反復子が有効な要素を指しているかどうかだけをチェックします。 セットにより多くの要素があるかどうかは確認されません。

### <a name="examples---more"></a>例 - more

次の例では、SetIterator.more メソッドを使用して、while ループを実行する前にセット内に要素があるかどうかを確認します。これにより、奇数要素がすべてセットから削除されます。

```xpp
{ 
    Set iset = new Set (Types::Integer); 
    SetIterator it; 
    int i; 
    ; 
    for (i = 1; i <= 10; i++) 
    { 
        iset.add(i); 
    } 
    // Delete all odd elements 
    it = new SetIterator(iset); 
    while (it.more()) 
    { 
        if (it.value() mod 2 != 0) 
        { 
            // The value is odd. Delete and skip to next element. 
            it.delete(); 
        } 
        else 
        { 
            it.next(); 
        } 
    } 
    print iset.toString(); 
    pause; 
}
```

## <a name="method-tostring"></a>メソッド toString

反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

設定の現在の要素のテキスト形式表記である文字列。

### <a name="remarks---tostring"></a>備考 - toString

反復子がセット内の最初の要素を指している場合、その文字列には "(開始)\[値\]" という形式の指示が含まれます。反復子が要素を指していない場合(つまり、more() が false を返す場合)、返される文字列は "(終了)" になります。反復子が値を指す場合、文字列は "\[値\]" になります。値は要素値の文字列表現です。

### <a name="examples---tostring"></a>例 - toString

次の例では、SetIterator.toString メソッドを使用して、反復子がセットのスキャンを開始する前にポイントする、そのセットの値の説明を出力します。

```xpp
{ 
    Set s1 = new Set (Types::Integer); 
    int theElement; 
    SetIterator it; 
    // Add some elements 
    s1.add(3); 
    s1.add(4); 
    s1.add(13); 
    s1.add(1);  
    // Start a traversal of the elements in the set 
    it = new SetIterator(s1); 
    // The elements are fetched in the order: 1, 3, 4, 13 
    print it.toString(); // Prints "(begin)[1]" 
    while (it.more()) 
    { 
        theElement = it.value(); 
        print theElement; 
        // Fetch the next element 
        it.next(); 
    } 
    pause; 
}
```

## <a name="method-value"></a>メソッド value

反復子がポイントしている値を取得します。

```xpp
public AnyType value()
```

### <a name="return-value---value"></a>戻り値 - value

反復子で示される値。

### <a name="remarks---value"></a>備考 - value

SetIterator.more を使用して、set 要素のキー値を取得する前に要素が存在するかどうかを確認します。

### <a name="examples---value"></a>例 - value

次の例では、SetIterator.value メソッドを使用して、セット内の現在の項目の値を出力します。

```xpp
{ 
    Set s1 = new Set (Types::Integer); 
    SetIterator it; 
    // Add some elements 
    s1.add(3); 
    s1.add(4); 
    s1.add(13); 
    s1.add(1);  
    // Start a traversal of the elements in the set 
    it = new SetIterator(s1); 
    // Prints "(begin)[1]" 
    print it.toString();  
    // The elements are fetched in the order: 1, 3, 4, 13 
    while (it.more()) 
    { 
        print it.value(); 
        // Fetch the next element 
        it.next(); 
    } 
    pause; 
}
```

## <a name="method-next"></a>メソッド next

次の要素に反復子を移動します。

```xpp
public void next()
```

### <a name="remarks---next"></a>備考 - next

SetIterator.more を使用して、反復子が有効な要素を指しているかどうかを判断します。

### <a name="examples---next"></a>例 - next

次の例では、SetIterator.next メソッドを使用して、反復子をセット内の次の要素に移動し、別の要素が存在するかどうかをテストし、別の要素がある場合はその値をコンテナーに追加します。

```xpp
static public void saveSequence(classId _classId, Set _sequence) 
{ 
    SysCheckListItemTable sysCheckListItemTable; 
    SetIterator           si; 
    container             con = connull(); 
    if (_sequence) 
    { 
        si = new SetIterator(_sequence); 
        si.begin(); 
        while (si.more()) 
        { 
             con += si.value(); 
             si.next(); 
        } 
    } 
    //... 
}
```

## <a name="method-new"></a>メソッド new

セットに対する新しい反復子を作成します。

```xpp
public void new(Set set)
```

### <a name="parameters---new"></a>パラメーター - new

set  
繰り返し処理するセット。

### <a name="remarks---new"></a>備考 - new

反復子は、セットが空でない場合、セットの最初の値に配置されます。

### <a name="examples---new"></a>例 - new

次の例では、整数のセットを作成し、セットの反復子を作成します。

```xpp
Set s1 = new Set (Types::Integer); 
SetIterator it; 
it = new SetIterator(s1);
```

## <a name="method-begin"></a>メソッド begin

反復子をセットの先頭に移動します。

```xpp
public void begin()
```

### <a name="remarks---begin"></a>備考 - begin

新しく作成されるセット反復子は、セットの最初の要素に配置されます。 通常はセットを反復処理する前に begin メソッドを呼び出す必要はありません。後でポインタをリセットしたい場合にのみ、その操作を行う必要があります。

### <a name="examples---begin"></a>例 - begin

次の例では、指定されたインターフェイス、つまり \_id クラスを実装するクラスのクラス ID のセットを返します。 スーパークラスの場合、反復子は設定からクラスを削除するために使用され、\_onlyLeafClasses パラメーターは true に設定されます。 開始メソッドを使用して、セットからスーパークラスが削除された後に反復子をリセットします。

```xpp
public static Set getImplements( 
    classId _id,  
    boolean _onlyLeafClasses = true) 
{ 
    Dictionary dictionary = new Dictionary(); 
    SysDictClass sysDictClass; 
    boolean removed; 
    Set set = new Set(Types::Integer); 
    SetIterator setIterator = new SetIterator(set); 
    int i; 
    for (i=1;i<=dictionary.classCnt();i++) 
    { 
        sysDictClass = new SysDictClass(dictionary.classCnt2Id(i)); 
        if (sysDictClass.isImplementing(_id)) 
        { 
            set.add(sysDictClass.id()); 
        } 
    } 
    //No superclasses included in return set 
    if (_onlyLeafClasses) 
    { 
        // begin method not needed here; only for clarity 
        setIterator.begin();  
        while (setIterator.more()) 
        { 
            removed = false; 
            sysDictClass = new SysDictClass(setIterator.value()); 
            while (sysDictClass.extend()) 
            { 
                removed = removed | set.remove(sysDictClass.extend()); 
                sysDictClass = new SysDictClass(sysDictClass.extend()); 
            } 
            if (removed) 
            { 
                // Restart search 
                setIterator.begin();  
            } 
            else 
            { 
                setIterator.next(); 
            } 
        } 
    } 
    return set; 
}
```

## <a name="method-delete"></a>メソッド delete

セットの反復子によってポイントされている要素を削除します。

```xpp
public void delete()
```

### <a name="remarks---delete"></a>備考 - delete

反復子は、このメソッドを呼び出した後に次の要素を指します。

### <a name="examples---delete"></a>例 - delete

次の例では、すべての奇数要素をセットから削除します。

```xpp
{ 
    Set iset = new Set (Types::Integer); 
    SetIterator it; 
    int i; 
    for (i = 1; i <= 10; i++) 
    { 
        iset.add(i); 
    } 
    // Delete all odd elements 
    it = new SetIterator(iset); 
    while (it.more()) 
    { 
        if (it.value() mod 2 != 0) 
        { 
            // The value is odd. Delete and skip to next element. 
            it.delete(); 
        } 
        else 
        { 
            it.next(); 
        } 
    } 
    print iset.toString(); 
    pause; 
}
```

## <a name="method-end"></a>メソッド end

セットで最後の要素の後に反復子を移動します。

```xpp
public void end()
```

### <a name="remarks---end"></a>備考 - end

このメソッドを実行した後、より多くのメソッドは false を返します。

