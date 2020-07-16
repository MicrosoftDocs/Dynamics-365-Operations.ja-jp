---
title: 配列クラス
description: このトピックでは、配列クラスについて説明します。
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
ms.openlocfilehash: 24f977b1e6d6936173f303c0eb582d0bdafb5c39
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502747"
---
# <a name="class-array"></a>クラス配列

[!include [banner](../../includes/banner.md)]

```xpp
class Array extends Object
```

## <a name="remarks"></a>備考

配列では、オブジェクトやレコードなど単一タイプの値を保持できます (X++ 言語に組み込まれている配列のデータ タイプとは異なります) 。 このタイプのオブジェクトは、関数やメソッドに転送することができます。 値は、順番に格納されます。 配列は、必要に応じて展開されます。 したがって、配列の特定の分析コードは提供されません。

## <a name="examples"></a>例

次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。

```xpp
{ 
    Array oarray = new Array (Types::Class); 
```

```xpp
    oarray.value(1, new query()); 
    oarray.value(2, new query()); 
    oarray.value(4, new query());  
    print oarray.toString(); 
    print oarray.definitionString(); 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                                         |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| public str definitionString()                       | 配列の定義を含む文字列を返します。                                         |
| public boolean exists(int index)                    | 特定の配列要素が有効かどうかを判定します。                                             |
| public int lastIndex()                              | 配列に値を格納するために使用する最上位のインデックスを取得します。                             |
| public container pack()                             | Array クラスの現在のインスタンスをシリアル化します。                                                 |
| public str toString()                               | 配列の内容を説明する文字列を返します。                                          |
| public Types typeId()                               | 配列の値のデータ型を返します。                                                   |
| public AnyType value(int index, \[AnyType arg\])    | 指定したインデックスに格納される配列要素の値を取得または設定します。                  |
| public str xml(\[int indent\])                      | 現在のオブジェクトを表す XML 文字列を返します。                                           |
| ::public static Array create(container container)   | 以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。 |
| ::public static Array createFromXML(Object xmlnode) |                                                                                                     |
| public void new(Types Type)                         | 各要素が指定されたタイプを持つ配列を作成します。                                      |

## <a name="method-definitionstring"></a>メソッド definitionString

配列の定義を含む文字列を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

配列の定義を含む文字列。

### <a name="examples---definitionstring"></a>例 - definitionString

次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。 definitionString メソッドを使用して、配列の定義を出力します。

```xpp
{ 
    Array oarray = new Array (Types::Class); 
```

```xpp
    oarray.value(1, new query()); 
    oarray.value(2, new query()); 
    oarray.value(4, new query());  
    print oarray.definitionString(); 
    pause; 
}
```

## <a name="method-exists"></a>メソッド exists

特定の配列要素が有効かどうかを判定します。

```xpp
public boolean exists(int index)
```

### <a name="parameters---exists"></a>パラメーター - exists

指数  
テスト対象の配列要素。

### <a name="return-value---exists"></a>戻り値 - exists

インデックスにより指定される配列要素が有効な場合は true。それ以外の場合は、false。

### <a name="examples---exists"></a>例 - exists

次の例では、exists メソッドを使用して、配列内のさまざまな要素が有効かどうかをテストします。

```xpp
{ 
    array a = new array(types::Integer); 
```

```xpp
    a.value(1, 23); 
```

```xpp
    print a.value(1); 
    pause; 
    if (a.exists(7)) // No, only element 1 is initialized 
    { 
        print a.value(7); 
```

```xpp
    } 
    else  
    { 
        print "Value does not exist"; 
    } 
    pause; 
```

```xpp
    //Array positions 2 to 9 padded with default values 
    a.value(10, 55); 
```

```xpp
    if (a.exists(7)) // Yes, elements 1..10 now initialized 
    { 
        print a.value(7); 
    } 
    else  
    { 
        print "Value does not exist"; 
    } 
    pause; 
}
```

## <a name="method-lastindex"></a>メソッド lastIndex

配列に値を格納するために使用する最上位のインデックスを取得します。

```xpp
public int lastIndex()
```

### <a name="return-value---lastindex"></a>戻り値 - lastIndex

値を格納するために使用する最上位のインデックスを表す整数。

### <a name="examples---lastindex"></a>例 - lastIndex

次の例では、lastIndex メソッドを使用して配列の最後の要素を見つけ、この要素の後に新しい値を追加します。

```xpp
{ 
    Array myArray = new Array(Types::Integer); 
    int newValue; 
```

```xpp
    // Other code - values are added to myArray 
    // and a value is assigned to newValue 
```

```xpp
    myArray.value(myArray.lastIndex()+1, newValue); 
}
```

## <a name="method-pack"></a>メソッド pack

Array クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

Array クラスの現在のインスタンスを含むコンテナーです。

### <a name="remarks---pack"></a>備考 - pack

このメソッドで作成されたコンテナーには、配列の最初の要素の前に 3 つの要素が含まれます。

-   コンテナのバージョン番号。
-   配列要素のデータ型を識別する整数。
-   この配列の要素の数。

配列の値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを取得します。

### <a name="examples---pack"></a>例 - pack

次の例では、整数の配列を作成し、それにいくつかの値を追加します。 pack メソッドを使用して配列をコンテナーにパックし、コンテナーを使用して新しい配列を作成します。

```xpp
{ 
    int i; 
    container packedArray; 
    // Create an integer array 
    Array ia = new Array (Types::Integer); 
    Array iacopy; 
```

```xpp
    // Write some elements in it 
    for (i = 1; i< 10; i++) 
    { 
        ia.value(i, i*2); 
    } 
```

```xpp
    // Pack the array 
    packedArray = ia.pack(); 
```

```xpp
    // Unpack the array  
    iacopy = Array::create(packedArray); 
```

```xpp
    // Check the values 
    for (i = 1; i< 10; i++) 
    { 
        if (iacopy.value(i) != 2*i) 
        { 
            print "Error!"; 
        } 
    } 
    pause; 
}
```

## <a name="method-tostring"></a>メソッド toString

配列の内容を説明する文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

配列の内容を説明する文字列。

### <a name="examples---tostring"></a>例 - toString

次の例では、整数の配列を作成し、それにいくつかの値を追加します。 toString メソッドは、配列が保持する値を出力するために使用されます。

```xpp
{ 
    Array     myArray; 
```

```xpp
    Set set1 = new Set(Types::Integer); 
    Set set2 = new Set(Types::Integer); 
    int i; 
```


```xpp
    myArray = new Array(Types::Integer); 
```

```xpp
    // Add some values to the array. 
    for (i = 1; i< 10; i++) 
    { 
        myArray.value(i, i*2); 
    } 
```

```xpp
    // Print out the values in the array. 
    print myArray.toString(); 
    pause; 
}
```

## <a name="method-typeid"></a>メソッド typeId

配列の値のデータ型を返します。

```xpp
public Types typeId()
```

### <a name="return-value---typeid"></a>戻り値 - typeId

配列の要素のデータ型。

### <a name="remarks---typeid"></a>備考 - typeId

タイプは配列の寿命を通して同じままです。 タイプは、配列の作成時に指定されます。

### <a name="examples---typeid"></a>例 - typeId

次の例では、特定の配列要素が存在するかどうかをテストします。 存在しない場合、配列に追加する必要がある新しい値のタイプを指定するために typeId メソッドが使用されます。

```xpp
public anytype getArrayValue(Array a, int _index) 
{ 
    if (! a.exists(_index)) 
    { 
        a.value(_index,nullValueFromType(a.typeId())); 
    } 
```

```xpp
    return a.value(_index); 
}
```

## <a name="method-value"></a>メソッド value

指定したインデックスに格納される配列要素の値を取得または設定します。

```xpp
public AnyType value(int index, [AnyType arg])
```

### <a name="parameters---value"></a>パラメーター - value

指数  
指定されたオフセットで配列要素に割り当てる値 (オプション)。

<!-- -->

arg  
指定されたオフセットで配列要素に割り当てる値 (オプション)。

### <a name="return-value---value"></a>戻り値 - value

指定したオフセットに格納されている値。

### <a name="remarks---value"></a>備考 - value

戻り値のタイプは、配列のタイプと同じです。 値を持つ最後のインデックスを超えるインデックスで値を読み取ろうとすると、例外がスローされます。 値が実在しない位置に書き込まれる場合、前の要素とその実在しない位置との間にあるすべての位置に既定値が入力され、配列が展開されます。

### <a name="examples---value"></a>例 - value

次の例では、整数の配列を作成し、value メソッドを使用して値を配列に追加します。 値のメソッドを使用して配列内で格納されている値を取得し、それらをテストします。

```xpp
{ 
     int i; 
    // Create an integer array 
    Array ia = new Array (Types::Integer); 
```

```xpp
    // Write some elements in it 
    for (i = 1; i< 10; i++) 
    { 
        ia.value(i, i*2); 
    } 
```

```xpp
    // Check the values 
    for (i = 1; i< 10; i++) 
    { 
        if (ia.value(i) != 2*i) 
        { 
            print "Error!"; 
        } 
    } 
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

このメソッドをオーバーライドして、特定の型に対して意味のある値を返すことができます。

## <a name="method-create"></a>メソッド create

以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。

```xpp
public static Array create(container container)
```

### <a name="parameters---create"></a>パラメーター - create

コンテナー  
Array.pack メソッドを使用して作成されるコンテナーです。 コンテナーを展開して配列を作成します。

### <a name="return-value---create"></a>戻り値 - create

指定したコンテナーの内容を保持する配列です。

### <a name="remarks---create"></a>備考 - create

配列の値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出される Array.unpack メソッドが必要です。

### <a name="examples---create"></a>例 - create

次の例では、配列を作成し、2 つのセットを追加します。 配列がパックされ、それを使用して、新しい配列が作成されます。

```xpp
{ 
    Array     myArray; 
    Array     newArray; 
    container packedArray; 
```

```xpp
    Set set1 = new Set(Types::Integer); 
    Set set2 = new Set(Types::Integer); 
    int i; 
    int j; 
```

```xpp
    myArray = new Array(Types::Class); 
```

```xpp
    // Add some values to the set1 and set2 
    for (i = 0; i < 10; i++) 
    { 
        set1.add(i); 
        j = i+3; 
        set2.add(j); 
    } 
```

```xpp
    // Add set1 and set2 to myArray 
    myArray.value(1, set1); 
    myArray.value(2, set2); 
```

```xpp
    // Pack the myArray into a container 
    packedArray = myArray.pack(); 
```

```xpp
    // Create a new array from the container 
    if(packedArray != connull()) 
    { 
        newArray = Array::create(packedArray); 
    } 
```

```xpp
    // Test that newArray has same contents as myArray 
    print newArray.definitionString(); 
    print newArray.toString(); 
    pause; 
}
```

## <a name="method-createfromxml"></a>メソッド createFromXML

```xpp
public static Array createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a>パラメータ - createFromXML

xmlnode  

### <a name="return-value---createfromxml"></a>戻り値 - createFromXML

## <a name="method-new"></a>メソッド new

各要素が指定されたタイプを持つ配列を作成します。

```xpp
public void new(Types Type)
```

### <a name="parameters---new"></a>パラメーター - new

種類  
配列要素のデータ型。

### <a name="remarks---new"></a>備考 - new

可能な値は、Types システム列挙に使用可能な値です。

-   AnyType
-   BLOB
-   クラス
-   コンテナー
-   日
-   日時
-   Enum
-   Guid
-   Int64
-   整数

### <a name="examples---new"></a>例 - new

次の例では、整数の配列を作成します。

```xpp
Array intArray = new Array(Types::Integer);
```

